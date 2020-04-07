---

copyright:
  years: 2019, 2020
lastupdated: "2020-03-26"

---

# Replacing the root CA certificate

You can replace the root CA certificate.

## Before you begin

Verify that your Red Hat Advanced Cluster Management for Kubernetes cluster is running.

Back up the existing Red Hat Advanced Cluster Management for Kubernetes certificate resource by running the following command:

   ```
   oc get cert multicloud-ca-cert -n open-cluster-management -o yaml > multicloud-ca-cert-backup.yaml
   ```

## Creating the root CA certificate with OpenSSL

Complete the following steps to create a root CA certificate with OpenSSL:

1. Generate your certificate authority (CA) RSA private key by running the following command:

   ```
   openssl genrsa -out ca.key 4096
   ```

2. Generate a self-signed CA certificate by using your CA key. Run the following command:

   ```
   openssl req -x509 -new -nodes -key ca.key -days 400 -out ca.crt -config req.cnf
   ```

   Your `req.cnf` file might resemble the following file:

      ```
      [ req ]               # Main settings
      default_bits = 4096       # Default key size in bits.
      prompt = no               # Disables prompting for certificate values so the configuration file values are used.
      default_md = sha256       # Specifies the digest algorithm.
      distinguished_name = dn   # Specifies the section that includes the distinguished name information.
      x509_extensions = v3_ca   # The extentions to add to the self signed cert

      [ dn ]               # Distinguished name settings
      C = US                    # Country
      ST = North Carolina             # State or province
      L = Raleigh                # Locality
      O = Red Hat Open Shift     # Organization
      OU = Red Hat Advanced Container Management        # Organizational unit
      CN = www.redhat.com  # Common name.

      [ v3_ca ]          # x509v3 extensions
      basicConstraints=critical,CA:TRUE # Indicates whether the certificate is a CA certificate during the certificate chain verification process.
      ```

## Replacing root CA certificates

1. Delete the `multicloud-ca-cert` certificate by running the following command:

   ```
   oc delete cert multicloud-ca-cert -n open-cluster-management
   ```

2. Create a secret with the CA certificate by running the following command:

   ```
   kubectl -n open-cluster-management create secret tls multicloud-ca-cert --cert ./ca.crt --key ./ca.key
   ```

3. Refresh all of your `cert-manager` certificates that use the CA. For more information view the upcoming section, [Refreshing _cert-manager_ certificates](#refresh).

4. Validate the custom CA is in use by logging in to the console and view the details of the certificate being used. <!-- we should state the steps to do this; it migth be only 3 steps?-->

## Refreshing _cert-manager_ certificates

After the root CA is replaced, all certificates that are signed by the root CA must be refreshed and the services that use those certificates must be restarted. Cert-manager creates the default Issuer from the root CA so all of the certificates issued by `cert-manager`, and signed by the default ClusterIssuer must also be refreshed.

Delete the Kubernetes secrets associated with each `cert-manager` certificate to refresh the certificate and restart the services that use the certificate. Run the following command: 

   ```
   oc delete secret -n open-cluster-management $(oc get cert -n open-cluster-management -o wide | grep multicloud-ca-issuer | awk '{print $3}')
   ```

## Restoring root CA certificates

To restore the root CA certificate, obtain the previously created backup file of the root CA certificate. Run the following command: 

   ```
   oc create -f multicloud-ca-cert-backup.yaml
   ```

Refresh all `cert-manager` certificates that use the CA. For more information, see the [Refreshing _cert-manager_ certificates](#refresh) section. 

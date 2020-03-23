---

copyright:
  years: 2019, 2020
lastupdated: "2020-03-23"

---

# Replacing management ingress certificates

You can replace management ingress certificates.

## Before you begin

Prepare and have your `management-ingress` certificates and private keys ready. If needed, you can generate a TLS certificate by using OpenSSL. Set the common name parameter,`CN`, on the certificate to `manangement-ingress`. If you are generating the certificate, include the following settings:

* Include the following IP addresses and domain names to your cert Subject Alternative Name (SAN) list:
  * The service name for the management ingress: `management-ingress`.
  * Include the route name for Red Hat Advanced Cluster Management for Kubernetes. Recieve the route name by running the following command:

     ```
     oc get route -n open-cluster-management
     ```

     You might receieve the following response:

     ```
     multicloud-console.apps.grchub2.dev08.red-chesterfield.com
     ```
  * Add the localhost IP address: `127.0.0.1`.
  * Add the localhost entry: `localhost`.

### Example configuration file for generating a certificate

The following example configuration file and OpenSSL commands provide an example for how to generate a TLS certificate by using OpenSSL. View the following `csr.cnf` configuration file, which defines the configuration settings for generating certificates with OpenSSL.

   ```
   [ req ]               # Main settings
   default_bits = 2048       # Default key size in bits.
   prompt = no               # Disables prompting for certificate values so the configuration file values are used.
   default_md = sha256       # Specifies the digest algorithm.
   req_extensions = req_ext  # Specifies the configuration file section that includes any extensions.
   distinguished_name = dn   # Specifies the section that includes the distinguished name information.

   [ dn ]               # Distinguished name settings
   C = US                    # Country
   ST = North Carolina             # State or province
   L = Raleigh                # Locality
   O = Red Hat Open Shift     # Organization
   OU = Red Hat Advanced Container Management        # Organizational unit
   CN = management-ingress  # Common name.

   [ req_ext ]          # Extensions
   subjectAltName = @alt_names # Subject alternative names

   [ alt_names ]        # Subject alternative names
   DNS.1 = management-ingress
   DNS.2 = multicloud-console.apps.grchub2.dev08.red-chesterfield.com
   DNS.3 = localhost
   DNS.4 = 127.0.0.1

   [ v3_ext ]          # x509v3 extensions
   authorityKeyIdentifier=keyid,issuer:always  # Specifies the public key that corresponds to the private key that is used to sign a certificate.
   basicConstraints=CA:FALSE                   # Indicates whether the certificate is a CA certificate during the certificate chain verification process.
   #keyUsage=keyEncipherment,dataEncipherment   # Defines the purpose of the key that is contained in the certificate.
   extendedKeyUsage=serverAuth                 # Defines the purposes for which the public key can be used.
   subjectAltName=@alt_names                   # Identifies the subject alternative names for the identify that is bound to the public key by the CA.
   ```

   **Note:** Be sure to update the SAN labeled, `DNS.2` with the correct hostname for your management ingress.


### OpenSSL commands for generating a certificate

The following OpenSSL commands are used with the preceding configuration file to generate the required TLS certificate.

  1. Generate your certificate authority (CA) RSA private key:

     ```
     openssl genrsa -out ca.key 4096
     ```

  2. Generate a self-signed CA certificate by using your CA key:

     ```
     openssl req -x509 -new -nodes -key ca.key -subj "/C=US/ST=North Carolina/L=Raleigh/O=Red Hat OpenShift" -days 400 -out ca.crt
     ```

  3. Generate the RSA private key for your certificate:

     ```
     openssl genrsa -out ingress.key 4096
     ```

  4. Generate the Certificate Signing request (CSR) by using the private key:

     ```
     openssl req -new -key ingress.key -out ingress.csr -config csr.cnf
     ```

  5. Generate a signed certificate by using your CA certificate and key and CSR:

     ```
     openssl x509 -req -in ingress.csr -CA ca.crt -CAkey ca.key -CAcreateserial -out ingress.crt -sha256 -days 300 -extensions v3_ext -extfile csr.cnf
     ```

  6. Examine the certificate contents:

     ```
     openssl x509  -noout -text -in ./ingress.crt
     ```

  7. Create a secret containing the CA certificate by running the following command:

     ```
     kubectl -n open-cluster-management create secret tls multicloud-ca-cert --cert ./ca.crt --key ./ca.key
     ```

## Backup the existing certificate for the ingress

Create a file with a copy of your existing certificates by completing the following steps:

1. Get the certificate and secret names for the ingress by running the following command:

   ```
   oc get cert -n open-cluster-management | grep ingress
   ```

2. Backup the `management-ingress` certifcate by running the following command:

   ```
   oc get cert -n open-cluster-management management-ingress-c38ac-cert -o yaml > ingress-cert-backup.yaml
   ```

## Replace the management ingress certificate

Complete the following steps to replace a management ingress certificate:

1. Delete the management-ingress certificate and secret by running the following command:

   ```
   kubectl delete cert -n [open-cluster-management] management-ingress-c38ac-cert
   ```
   {: codeblock}

2. Create the management-ingress secret by using your certificate and private key.

   ```
   kubectl -n [open-cluster-management] create secret tls management-ingress-c38ac-tls-secret --cert ./ingress.crt --key ./ingress.key
   ```

3. Verify that the secret is created in the correct namespace.

   ```
   kubectl get secret -n [open-cluster-management] | grep management-ingress | grep tls
   ```

4. Edit the management ingress deployment. Get the name of the deployment by running the following command:

   ```
   oc get deployment -n open-cluster-management
   ```
  * Open and edit the management ingress deployment. Replace the string `multicloud-ca-cert` with `ingress-ca-cert` to restart the management ingress. Run the following command:

     ```
     oc edit deployment management-ingress -n open-cluster-management
     ```

5. After the management ingress pod has restarted, navigate to the Red Hat Advanced Cluster Management for Kubernetes console from your browser. Verify that the current certificate is your certificate, and that all console access and login functionality remain the same.

## Restore the default self-signed certificate for management ingress

1. Retrieve the certificate backup file that you created when you replaced the management ingress:

   1. Run the following command to restore the management ingress certificate from the backup:

      ```
      oc create -f ingress-cert-backup.yaml
      ```

      The secret is automatically updated.

   2. Edit the management ingress deployment. Get the name of the deployment by running the following command:

      ```
      oc get deployment -n open-cluster-management
      ```

    * Open and edit the management ingress deployment. Replace the `ingress-ca-cert` string  with `multicloud-ca-cert` to restart the management ingress. Run the following command:

         ```
         oc edit deployment management-ingress -n open-cluster-management
         ```

2. After all pods are restarted, navigate to the Red Hat Advanced Cluster Management for Kubernetes console from your browser. Verify that the current certificate is your certificate, and that all console access and login functionality remain the same.

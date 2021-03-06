---

copyright:
  years: 2016, 2020
lastupdated: "2020-03-24"

---

# List endpoints

List available endpoints.

Base path: `https://<Cluster Master Host>:<Cluster Master API Port>/image-manager/api/v1`

The `<Cluster Master Host>` and `<Cluster Master API Port>` parameters are defined in [Master endpoints](../install/cluster_endpoints.md#master).


<dl>
<dt><b>API version</b></dt>
<dd>4.4.0</dd>
<dt><b>API URI components</b></dt>
<dd>
<dl>
<dt><b>Scheme</b></dt>
<dd><pre>HTTPS</pre></dd>
<dt><b>Host name</b></dt>
<dd><pre>Cluster Master Host</pre></dd>
<dt><b>Port number</b></dt>
<dd><pre>Cluster Master API Port</pre></dd>
<dt><b>Base path</b></dt>
<dd><pre>/image-manager/api/v1</pre></dd>
<dt><b>Command</b></dt>
<dd><pre>GET</pre></dd>
</dl>
</dd>
<dt><b>Command output format</b></dt>
<dd><pre>application/json</pre></dd>
</dl>


The sample curl command resembles the following code:

```
curl -k -H GET --header "Authorization: Bearer $ID_TOKEN" https://<Cluster Master Host>:<Cluster Master API Port>/image-manager/api/v1
```

The response resembles the following code:

```
root@master:~# curl -k -X GET --header "Authorization: Bearer $ID_TOKEN" https://mycluster.icp:8443/image-manager/api/v1
IBM Cloud Private Image Management API.
The listener is working. Now try a valid endpoint
Available APIs:
GET /
GET /image-manager/api/v1
GET /image-manager/api/v1/auth/token
GET /image-manager/api/v1/repositories
GET /image-manager/api/v1/repositories/{repo:.*}
PUT /image-manager/api/v1/repositories/{repo:.*}
DELETE /image-manager/api/v1/repositories/{repo:.*}
```

## Responses

|HTTP Code|Description|Schema|
|---------|-----------|------|
|200|OK|No content|
{: caption="Table 1. The responses that are returned when you list endpoints" caption-side="top"}

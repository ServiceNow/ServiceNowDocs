---
title: Create a Prometheus connection
description: Establish a zero copy connection to a Prometheus system in Zero Copy Connector Hub.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/create-prometheus-connection.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Prometheus, Community connectors, Manage zero copy connections, Zero Copy Connectors, Workflow Data Fabric]
---

# Create a Prometheus connection

Establish a zero copy connection to a Prometheus system in Zero Copy Connector Hub.

## Before you begin

Role required: df\_connection\_admin

## About this task

Work with your data source admin to create a connection to Prometheus. For additional information about connecting, refer to the [Prometheus connector documentation](https://trino.io/docs/current/connector/prometheus.html).

**Note:** This connector was developed by the open-source community and made available through the ServiceNow AI Platform for general use. Functionality can vary and might not cover all use cases supported by primary connectors.

## Procedure

1.  Navigate to the available community connectors in Zero Copy Connector Hub in one of the following ways:

    -   Navigate to **All** &gt; **Zero Copy Connector Hub** &gt; **Available connectors** &gt; **Community connectors**.
    -   Navigate to **Admin** &gt; **Zero Copy Connector Hub** &gt; **Available connectors** &gt; **Community connectors**.
2.  Find the Prometheus connector and select **Connect**.

3.  On the form, fill in the fields.

<table id="table_kmx_fw1_2fc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Name and description

</td></tr><tr><td>

Connection label

</td><td>

Unique name for this connection. This helps in identifying the connection within your system.

</td></tr><tr><td>

Connection name

</td><td>

System-generated name based on the Connection label. This field cannot be modified once the connection is established.

</td></tr><tr><td>

Short description

</td><td>

Description of the connection explaining what it is about.

</td></tr><tr><td class="sub-head" colspan="2">

Connection attributes

</td></tr><tr><td>

Connection URL

</td><td>

Endpoint for the Prometheus coordinator host. For example:`https://<host>/<path>`

</td></tr><tr><td class="sub-head" colspan="2">

Authentication methods

</td></tr><tr><td>

Authentication method

</td><td>

Authentication method to use with Prometheus. Default is Basic Authentication.

</td></tr><tr><td>

Username

</td><td>

Username for basic authentication.

</td></tr><tr><td>

Password

</td><td>

Password associated with the username.

</td></tr></tbody>
</table>4.  Configure connection security.

<table id="choicetable_ejt_ldh_b3c"><thead><tr><th align="left" id="d503989e253">

Option

</th><th align="left" id="d503989e256">

Description

</th></tr></thead><tbody><tr><td id="d503989e262">

**Default**

</td><td>

Select this option to use Java security CA certificates to establish a secure connection with the data source.This option uses public certificates that are already available in the Java security truststore.

</td></tr><tr><td id="d503989e273">

**TLS**

</td><td>

Select this option if your data source requires one-way SSL and uses its own certificates.

</td></tr></tbody>
</table>5.  If you selected TLS, attach the Base64-encoded truststore PEM file using one of the following options.

<table id="choicetable_iqc_pl2_h3c"><tbody><tr><td id="d503989e291">

**Attach TrustStore file**

</td><td>

Upload the PEM file by selecting **Attach PEM file** and selecting the file.

</td></tr><tr><td id="d503989e303">

**Enter TrustStore file contents**

</td><td>

Copy and paste the contents of the truststore file, ensuring the content begins with: ```
-----BEGIN CERTIFICATE-----
```

 and ends with: ```
-----END CERTIFICATE-----
```

</td></tr></tbody>
</table>6.  Select **Connect**.


## Result

A test connection is made to the external data source, verifying that the connection details are correct and the data source is accessible.

## What to do next

If the connection succeeds, configure data steward access on the **Access Control** tab. See .

If the connection fails, verify the connection details with your data source administrator and try again.


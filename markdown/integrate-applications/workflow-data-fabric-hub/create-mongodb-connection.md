---
title: Create a MongoDB connection
description: Establish a zero copy connection to a MongoDB database in Workflow Data Fabric Hub.
locale: en-US
release: yokohama
product: Workflow Data Fabric Hub
classification: workflow-data-fabric-hub
topic_type: task
last_updated: "2025-04-29"
reading_time_minutes: 1
breadcrumb: [MongoDB, Community connectors, Managing zero copy connections in Workflow Data Fabric Hub, Workflow Data Fabric Hub, Data and Automation]
---

# Create a MongoDB connection

Establish a zero copy connection to a MongoDB database in Workflow Data Fabric Hub.

## Before you begin

Role required: df\_connection\_admin

## About this task

**Note:** This connector was developed by the open-source community and made available through the ServiceNow AI Platform for general use. Functionality can vary and might not cover all use cases supported by primary connectors.

## Procedure

1.  Navigate to the available community connectors in Workflow Data Fabric Hub in one of the following ways:

    -   Navigate to **All** &gt; **Workflow Data Fabric Hub** &gt; **Available connectors** &gt; **Community connectors**.
    -   Navigate to **Admin** &gt; **Workflow Data Fabric Hub** &gt; **Available connectors** &gt; **Community connectors**.
2.  Find the MongoDB connector and select **Connect**.

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

URL to establish the connection. For example:`mongodb://<host>:<port>/database_name?ssl=true&authSource=external&authMechanism=MONGODB-X509`

</td></tr></tbody>
</table>4.  Configure secure authentication by providing truststore information.

<table id="choicetable_dth_vsc_qfc"><thead><tr><th align="left" id="d169221e210">

Option

</th><th align="left" id="d169221e213">

Description

</th></tr></thead><tbody><tr><td id="d169221e219">

**Upload truststore file**

</td><td>

1.  Select **Attach TrustStore file**.
2.  Browse and select the truststore file.


</td></tr><tr><td id="d169221e240">

**Enter truststore contents manually**

</td><td>

Copy and paste the contents of the keystore file.

</td></tr></tbody>
</table>5.  Configure secure authentication by providing keystore information.

<table id="choicetable_zbg_15c_qfc"><thead><tr><th align="left" id="d169221e258">

Option

</th><th align="left" id="d169221e261">

Description

</th></tr></thead><tbody><tr><td id="d169221e267">

**Upload keystore file**

</td><td>

1.  Select **Attach KeyStore file**.
2.  Browse and select the keystore file.


</td></tr><tr><td id="d169221e288">

**Enter keystore contents manually**

</td><td>

Copy and paste the contents of the keystore file.

</td></tr></tbody>
</table>6.  Enter the truststore password.

7.  Enter the keystore password.

8.  Select **Connect**.


## Result

A test connection is made to the external data source, verifying that the connection details are correct and the data source is accessible.

## What to do next

If the connection succeeds, configure data steward access on the **Access Control** tab. See [Manage access to an established connection using roles](manage-access-connection-wdf.md).

If the connection fails, verify the connection details with your data source administrator and try again.


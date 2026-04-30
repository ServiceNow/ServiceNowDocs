---
title: Set up the Oracle Financial Cloud spoke
description: Integrate the ServiceNow instance and Oracle Financial Cloud instance by using the basic auth credentials to authenticate ServiceNow requests.Configure a connection to authenticate ServiceNow requests in an Oracle Financial Cloud spoke.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Oracle Financial Cloud Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up the Oracle Financial Cloud spoke

Integrate the ServiceNow instance and Oracle Financial Cloud instance by using the basic auth credentials to authenticate ServiceNow requests.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the Oracle Financial Cloud spoke.
-   Role required: admin.

## Configure a connection for the Oracle Financial Cloud spoke

Configure a connection to authenticate ServiceNow requests in an Oracle Financial Cloud spoke.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Flow Designer**.

2.  Select the **Connections** tab.

3.  Configure an **OracleCloudFinancials** connection.

    1.  Search for the **OracleCloudFinancials** connection alias.

        There are two options.

<table id="table_hzy_pcj_rzb"><thead><tr><th>

Option

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**View Details**

</td><td>

To configure the default connection and credential alias record shipped with the spoke.

</td></tr><tr><td>

**Add Connection**

</td><td>

To manage more than one spoke connection records. For more information, see [Supporting multiple connections](../../integrationhub/concept/support-multiple-connections.md)

</td></tr></tbody>
</table>    2.  Select **View Details**.

    3.  Configure, edit, or add a connection.

        -   Select **Configure** or **Edit** to set up an existing connection.

        -   Select **Add Connection** to create and configure a new connection.

    4.  On the configuration form, fill in the fields.

<table id="table_hhb_hxk_nzb"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Connection Name

</td><td>

`OracleCloudFinancials`.

</td></tr><tr><td>

Connection URL

</td><td>

The instance URL in this format:`<provider-domain-name>.fa.ocs.oraclecloud.com/`.

</td></tr><tr><td>

User name

</td><td>

The Oracle account user name.

</td></tr><tr><td>

Password

</td><td>

The Oracle admin account password.

</td></tr></tbody>
</table>    5.  Confirm your configuration.

        For an existing connection, select **Edit Connection**. For a new connection, select **Create Connection**.

4.  Repeat step 3 to configure **OrancleCloudFinancialsReport** with the following information:

<table id="table_ddr_sps_5zb"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Connection Name

</td><td>

`OracleCloudFinancialsReport`.

</td></tr><tr><td>

Connection URL

</td><td>

The instance URL in this format: `<provider-domain-name>.fa.ocs.oraclecloud.com/xmlpserver/services/v2/ReportService`.

</td></tr><tr><td>

User name

</td><td>

The Oracle account user name.

</td></tr><tr><td>

Password

</td><td>

The Oracle admin account password.

</td></tr></tbody>
</table>
### What to do next

Create the necessary records in the following relevant spoke modules, or use the available spoke actions directly:

-   AP Invoices Interface
-   AP Invoices Lines Interface
-   BI Report Paths
-   GL Interface


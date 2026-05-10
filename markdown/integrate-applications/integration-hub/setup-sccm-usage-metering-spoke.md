---
title: Set up the SCCM Usage Metering spoke
description: Integrate the ServiceNow instance and SCCM using Java Database Connectivity \(JDBC\) credentials to authenticate ServiceNow requests.Create Connection records to the SCCM server. The SCCM Usage Metering spoke connection and credential aliases use these connections to perform actions in SCCM.Create Credential records to the SCCM server. The SCCM Usage Metering spoke connection and credential alias uses these credentials to authorize actions.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [SCCM Usage Metering Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up the SCCM Usage Metering spoke

Integrate the ServiceNow instance and SCCM using Java Database Connectivity \(JDBC\) credentials to authenticate ServiceNow requests.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the SCCM Usage Metering spoke.
-   Role required: admin.

## Create Connection records for the SCCM Usage Metering spoke

Create Connection records to the SCCM server. The SCCM Usage Metering spoke connection and credential aliases use these connections to perform actions in SCCM.

### Before you begin

Role required: admin.

### Procedure

1.  Navigate to **All** &gt; **Credentials &amp; Connections** &gt; **Connections**.

2.  Click **New** and select **JDBC Connection**.

3.  On the form, fill in the fields.

    The database selection in the **Format** field determines which fields are available.

<table id="table_frf_bnz_wkb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name of the JDBC connection. For example, `JDBC MySQLProd`.

</td></tr><tr><td>

Credential

</td><td>

Credential for the JDBC provider. Enter the user name and password of the database.

</td></tr><tr><td>

Connection alias

</td><td>

Alias record associated with the connection.

</td></tr><tr><td>

Query timeout

</td><td>

Maximum elapsed time the JDBC query allowed to run without a response.

</td></tr><tr><td>

Connection timeout

</td><td>

Maximum elapsed time for the JDBC activity to wait while attempting to connect to the target database.

</td></tr><tr><td>

Active

</td><td>

Option to make the connection active.

</td></tr><tr><td>

Domain

</td><td>

Domain for the table. By default, the JDBC Connection \[jdbc\_connection\] table runs in the global domain.

</td></tr><tr><td>

Format

</td><td>

Database type for the connection. The choices are:-   **MySQL**
-   **Oracle**
-   **SQLServer**
-   **None**


</td></tr><tr><td>

Host

</td><td>

Host name or IP address of the database server.

</td></tr><tr><td>

Oracle port

</td><td>

Port that the Oracle database is using. The default value is **1521**.**Note:** This field is available when **Oracle** is selected from the Format list.

</td></tr><tr><td>

Oracle sid

</td><td>

Oracle database site identifier. The default value is **orcl**.**Note:** This field is available when **Oracle** is selected from the Format list.

</td></tr><tr><td>

Database name

</td><td>

Name of the database. **Note:** This field is available when **MySQL** or **SQLServer** is selected from the Format list.

</td></tr><tr><td>

Override default port

</td><td>

Port that the selected database is using. **Note:** This field is available when **MySQL** or **SQLServer** is selected from the Format list.

</td></tr><tr><td>

Instance name

</td><td>

Instance name for the selected SQLServer. **Note:** This field is available when **SQLServer** is selected from the Format list.

</td></tr><tr><td>

Connection URL

</td><td>

URL that MID Server uses to connect to the specified database. The URL is created automatically when you save the form, and is read-only for the default databases. For example, jdbc:&lt;database&gt;://&lt;hostname&gt;;selectMethods=cursor;databaseName=&lt;database\_name&gt;.**Note:** If the format selected is not one of the default databases, you must create the connection URL manually. So that the MID Server can create the connection.

</td></tr><tr><td>

Use MID server

</td><td>

Option to use a MID Server for the action. If selected, define fields in the **Advanced MID Server Configuration** section.

</td></tr><tr><td>

Capabilities

</td><td>

Capabilities that the MID Server must support to be eligible for selection. Only displays if **Use MID server** is selected. To learn more about how a MID Server is selected during runtime, see [MID Server selection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/c_MIDServerSelector.md).

</td></tr><tr><td>

MID Application

</td><td>

Application that the MID Server must support to be eligible for selection. Only displays if **Use MID server** is selected. To learn more about how a MID Server is selected during runtime, see [MID Server selection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/c_MIDServerSelector.md).

</td></tr></tbody>
</table>
## Create Credential records for the SCCM Usage Metering spoke

Create Credential records to the SCCM server. The SCCM Usage Metering spoke connection and credential alias uses these credentials to authorize actions.

### Before you begin

Role required: admin.

### Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Credentials**.

2.  Click **New**.

3.  Select **JDBC Credentials**.

4.  On the form, fill these values.

    |Field|Description|
    |-----|-----------|
    |Name|Name to uniquely identify the credential.|
    |Active|Option to use the credentials.|
    |Applies to|Option to verify if the credentials apply to **All MID servers** in your network, or to one or more **Specific MID servers**. Specify the MID Servers that should use these credentials in the **MID servers** field.|
    |Order|Order to apply this credential. For example, enter `100`.|
    |User name|User name to access the database.|
    |Password|Password to access the database.|
    |Credential alias|Credential alias associated with the spoke.|

5.  Click **Submit**.



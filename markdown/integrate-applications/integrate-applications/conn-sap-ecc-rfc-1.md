---
title: Create a connection record for the SAP ECC RFC spoke
description: Create a connection record for your SAP ECC RFC account. The SAP ECC RFC spoke connection and credential aliases use these connections to perform actions in SAP ECC RFC.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
---

# Create a connection record for the SAP ECC RFC spoke

Create a connection record for your SAP ECC RFC account. The SAP ECC RFC spoke connection and credential aliases use these connections to perform actions in SAP ECC RFC.

## Before you begin

Role required: admin.

## Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connections &amp; Credentials Aliases**.

2.  Open the alias record for SAP ECC RFC.

3.  From the **Connections** tab, click **New**.

4.  On the form, fill these fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name to uniquely identify the record. For example, `SAP ECC RFC Connection`.|
    |Credential|Credential record created for SAP ECC RFC spoke. For example, `SAP ECC RFC Cred`.|
    |Connection alias|Alias record associated with this connection.|
    |Host|IP address of the target host where the SAP ECC RFC server is installed.|
    |||
    |Active|Option to actively use the connection record.|
    |Domain|Domain that the action runs in.|
    |Override default port|Target port used by the connection. If blank, the system uses the default port.|
    |Use MID server|Option to use a MID Server for this connection. Select the check box and define the fields in the **Advanced MID Server Configuration** tab.|

5.  In the **Advanced MID Server Configuration** tab, provide these details.

<table id="table_mqc_3yd_ymb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Capabilities

</td><td>

Capabilities the MID Server must support to be eligible for selection. The system runs the action or activity from a MID Server that supports the selected capabilities.Required capabilities determine which MID Server is selected at runtime. To learn more about how a MID Server is selected during runtime, see [MID Server selection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/c_MIDServerSelector.md).

</td></tr><tr><td>

MID Application

</td><td>

Application the MID Server must support to be eligible for selection. The system runs the action from a MID Server that supports the selected application.To learn more about how a MID Server is selected during runtime, see [MID Server selection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/c_MIDServerSelector.md).

</td></tr></tbody>
</table>6.  In the **Connection Attributes** tab, provide these details.

    |Field|Description|
    |-----|-----------|
    |Client|Client value of the target host where the SAP ECC RFC server is installed.|
    |System Number|System number of the target host where the SAP ECC RFC server is installed.|
    |Language|Language selected in the target host where the SAP ECC RFC server is installed.|

7.  If you intend to connect to an SAP load-balanced environment, provide values for these additional fields in the **Connection Attributes** tab:

    -   **Message Server**
    -   **Group**
    -   **Host**
8.  Click **Submit**.



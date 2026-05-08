---
title: Set up the SAP ECC RFC spoke
description: Integrate the ServiceNow instance and SAP ECC RFC account by using the Basic Auth credentials to authenticate ServiceNow requests.Configure MID Server using the SAP proprietary JAR files to integrate SAP ECC RFC account with your ServiceNow instance.Create a credential record for the SAP ECC RFC account. The SAP ECC RFC spoke connection and credential alias uses these credentials to authorize actions.Create a connection record for your SAP ECC RFC account. The SAP ECC RFC spoke connection and credential aliases use these connections to perform actions in SAP ECC RFC.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [SAP ECC RFC Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up the SAP ECC RFC spoke

Integrate the ServiceNow instance and SAP ECC RFC account by using the Basic Auth credentials to authenticate ServiceNow requests.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the SAP ECC IDoc spoke.
-   Role required: admin.

## Configure MID Server for the SAP ECC RFC spoke

Configure MID Server using the SAP proprietary JAR files to integrate SAP ECC RFC account with your ServiceNow® instance.

### Before you begin

Role required: admin.

### Procedure

1.  Navigate to **All** &gt; **System Properties** &gt; **Security**.

    **Note:** This is applicable only if your MID Server is installed on a Linux machine

2.  Disable the MIME type validation for file attachments.

    ![Option to disable the MIME type validation](../image/mime-type-sap-ecc-rfc.png)

    **Note:** This is applicable only if your MID Server is installed on a Linux machine

3.  Navigate to **MID Server** &gt; **JAR Files**.

4.  Upload the required SAP proprietary files \(JAR, SO, or DLL\) obtained after contacting your SAP ECC RFC admin.

    For more information, see Synchronize a JAR file to MID Servers.


### What to do next

Ensure that the files are synchronised in the `<MID-Server-root-directory>/agent/extlib` directory. If the files aren't synchronised, restart the MID Server.

## Create a credential record for the SAP ECC RFC spoke

Create a credential record for the SAP ECC RFC account. The SAP ECC RFC spoke connection and credential alias uses these credentials to authorize actions.

### Before you begin

Role required: admin.

### Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Credentials**.

2.  Click **New**.

    The system displays this message: `What type of Credentials would you like to create?`

3.  Select **Basic Auth Credentials**.

4.  On the form, fill these values.

<table id="table_ixb_v5p_xmb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name to uniquely identify the record. For example, `SAP ECC RFC Cred`.

</td></tr><tr><td>

User name

</td><td>

User name to log in to your SAP ECC RFC account.

</td></tr><tr><td>

Password

</td><td>

Password to authenticate and log in to your SAP ECC RFC account.

</td></tr><tr><td>

Active

</td><td>

Option to actively use the credential record.

</td></tr><tr><td>

Order

</td><td>

Order to apply this credential. For example, `100`.

</td></tr><tr><td>

Credential alias

</td><td>

Credential alias associated with the spoke.

</td></tr></tbody>
</table>5.  Click **Submit**.


## Create a connection record for the SAP ECC RFC spoke

Create a connection record for your SAP ECC RFC account. The SAP ECC RFC spoke connection and credential aliases use these connections to perform actions in SAP ECC RFC.

### Before you begin

Role required: admin.

### Procedure

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

Capabilities the MID Server must support to be eligible for selection. The system runs the action or activity from a MID Server that supports the selected capabilities.Required capabilities determine which MID Server is selected at runtime. To learn more about how a MID Server is selected during runtime, see MID Server selection.

</td></tr><tr><td>

MID Application

</td><td>

Application the MID Server must support to be eligible for selection. The system runs the action from a MID Server that supports the selected application.To learn more about how a MID Server is selected during runtime, see MID Server selection.

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



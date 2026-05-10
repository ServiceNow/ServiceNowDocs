---
title: Set up the SAP S4 HANA IDoc spoke
description: Integrate the ServiceNow instance and SAP S4 HANA IDoc spoke by using the Basic Auth credentials to authenticate ServiceNow requests.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [SAP S4 HANA IDoc Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up the SAP S4 HANA IDoc spoke

Integrate the ServiceNow instance and SAP S4 HANA IDoc spoke by using the Basic Auth credentials to authenticate ServiceNow requests.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the SAP S4 HANA IDoc spoke.
-   Role required: admin.

**Note:** To retrieve information, use the Execute RFC spoke action in the [SAP S4 HANA RFC Spoke](../concept/sap-s4hanarfc-spoke.md).

## Procedure

1.  Configure MID Server using the SAP proprietary JAR files.

    1.  Navigate to **System Properties** &gt; **Security**.

        **Note:** This is applicable only if your MID Server is installed on a Linux machine

    2.  Disable the MIME type validation for file attachments.

        ![Option to disable the MIME type validation](../image/mime-type-sap-ecc-rfc.png)

        **Note:** This is applicable only if your MID Server is installed on a Linux machine.

    3.  Navigate to **MID Server** &gt; **JAR Files**.

    4.  Upload the required SAP proprietary files \(JAR, SO, or DLL\) obtained after contacting your SAP S4 HANA IDoc admin.

        For more information, see [Synchronize a JAR file to MID Servers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/t_SynchronizeAJARFiletoMIDServers.md).

    **Note:** Ensure that the files are synchronised in the `<MID-Server-root-directory>/agent/extlib` directory. If the files aren't synchronised, restart the MID Server.

2.  Create a credential record for the SAP S4 HANA IDoc account.

    1.  Navigate to **Connections &amp; Credentials** &gt; **Credentials**.

    2.  Click **New**.

        The system displays this message: `What type of Credentials would you like to create?`

    3.  Select **Basic Auth Credentials**.

    4.  On the form, fill these values.

        |Field|Description|
        |-----|-----------|
        |Name|Name to uniquely identify the record. For example, `SAP S4 HANA IDoc Cred`.|
        |User name|User name to log in to your SAP S4 HANA IDoc account.|
        |Password|Password to authenticate and log in to your SAP S4 HANA IDoc account.|
        |Active|Option to actively use the credential record.|
        |Order|Order to apply this credential. For example, `100`.|
        |Credential alias|Credential alias associated with the spoke.|

    5.  Click **Submit**.

3.  Create a connection record for your SAP S4 HANA IDoc account.

    1.  Navigate to **Connections &amp; Credentials** &gt; **Connections &amp; Credentials Aliases**.

    2.  Open the alias record for SAP S4 HANA IDoc.

    3.  From the **Connections** tab, click **New**.

    4.  On the form, fill these fields.

        |Field|Description|
        |-----|-----------|
        |Name|Name to uniquely identify the record. For example, `SAP S4 HANA IDoc Connection`.|
        |Credential|Credential record created for SAP S/4 HANA IDoc spoke. For example, `SAP S4 HANA IDoc Cred`.|
        |Connection alias|Alias record associated with this connection.|
        |Host|Fully qualified domain name of the target host where the SAP S4 HANA IDoc server is installed.|
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
</table>    6.  In the **Attributes** tab, provide these details.

        |Field|Description|
        |-----|-----------|
        |Client|Client value of the target host where the SAP S4 HANA IDoc server is installed.|
        |u\_system\_number|System number of the target host where the SAP S4 HANA IDoc server is installed.|
        |u\_lang|Language selected in the target host where the SAP S4 HANA IDoc server is installed.|

    7.  Click **Submit**.



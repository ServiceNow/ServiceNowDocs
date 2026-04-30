---
title: Set up the SAP S4 HANA RFC spoke
description: Integrate the ServiceNow instance and SAP S4 HANA RFC spoke by using the Basic Auth credentials to authenticate ServiceNow requests.
locale: en-US
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [SAP S4 HANA RFC Spoke, Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Creating integrations with applications]
---

# Set up the SAP S4 HANA RFC spoke

Integrate the ServiceNow instance and SAP S4 HANA RFC spoke by using the Basic Auth credentials to authenticate ServiceNow requests.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate SAP S4 HANA RFC spoke.
-   Role required: admin

**Note:** To retrieve information for authorization purposes, use the Execute RFC spoke action.

## Procedure

1.  Configure MID Server using the SAP proprietary JAR files.

    1.  Navigate to **System Properties** &gt; **Security**.

        **Note:** This is applicable only if your MID Server is installed on a Linux machine

    2.  Disable the MIME type validation for file attachments.

        ![Option to disable the MIME type validation](../image/mime-type-sap-ecc-rfc.png)

        **Note:** This is applicable only if your MID Server is installed on a Linux machine.

    3.  Navigate to **MID Server** &gt; **JAR Files**.

    4.  Upload the required SAP proprietary files \(JAR, SO, or DLL\) obtained after contacting your SAP S4 HANA RFC admin.

        For more information, see [Synchronize a JAR file to MID Servers](https://www.servicenow.com/docs/access?context=t_SynchronizeAJARFiletoMIDServers&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).

    **Note:** Ensure that the files are synchronized in the `<MID-Server-root-directory>/agent/extlib` directory. If the files aren't synchronized, restart the MID Server.

2.  Create a credential record for the SAP S4 HANA RFC account.

    1.  Navigate to **Connections &amp; Credentials** &gt; **Credentials**.

    2.  Click **New**.

        The system displays this message: `What type of Credentials would you like to create?`

    3.  Select **Basic Auth Credentials**.

    4.  On the form, fill these values.

        |Field|Description|
        |-----|-----------|
        |Name|Name to uniquely identify the record. For example, `SAP S4 HANA RFC Cred`.|
        |User name|User name to log in to your SAP S4 HANA RFC account.|
        |Password|Password to authenticate and log in to your SAP S4 HANA RFC account.|
        |Active|Option to actively use the credential record.|
        |Order|Order to apply this credential. For example, `100`.|
        |Credential alias|Credential alias associated with the spoke.|

    5.  Click **Submit**.

3.  Create a connection record for your SAP S4 HANA RFC account.

    1.  Navigate to **Connections &amp; Credentials** &gt; **Connections &amp; Credentials Aliases**.

    2.  Open the alias record for SAP S4 HANA RFC.

    3.  From the **Connections** tab, click **New**.

    4.  On the form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Name|Name to uniquely identify the record. For example, `SAP S4 HANA RFC Connection`.|
        |Credential|Credential record created for SAP S/4 HANA IDoc spoke. For example, `SAP S4 HANA RFC Cred`.|
        |Connection alias|Alias record associated with this connection.|
        |Host|Fully qualified domain name of the target host where the SAP S4 HANA RFC server is installed.|
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

MID Selection

</td><td>

Option to select MID Server as required. This field is available when **Define Connection Inline** is selected from the Source Connection list.

</td></tr><tr><td>

MID Application

</td><td>

Option to use a MID Server to run the SFTP step. This field is available when **Define Connection Inline** is selected from the Source Connection list and **Auto-Select MID Server** is selected from the MID Selection list.To learn more about how a MID Server is selected during runtime, see [MID Server selection](https://www.servicenow.com/docs/access?context=c_MIDServerSelector&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td>

Capabilities

</td><td>

Capability of the MID Server. Select **SSH**. This field is available when **Define Connection Inline** is selected from the Source Connection list and **Auto-Select MID Server** is selected from the MID Selection list.Required capabilities determine which MID Server is selected at runtime. To learn more about how a MID Server is selected during runtime, see [MID Server selection](https://www.servicenow.com/docs/access?context=c_MIDServerSelector&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td>

MID Server

</td><td>

Data pill of the required MID Server. This field is available when **Define Connection Inline** is selected from the Source Connection list and **Specific MID Server** is selected from the MID Selection list.

</td></tr></tbody>
</table>    6.  In the **Attributes** tab, provide these details.

        |Field|Description|
        |-----|-----------|
        |u\_client|Client value of the target host where the SAP S4 HANA RFC server is installed.|
        |u\_system\_number|System number of the target host where the SAP S4 HANA RFC server is installed.|
        |u\_lang|Language selected in the target host where the SAP S4 HANA RFC server is installed.|

    7.  Click **Submit**.

4.  Create a record in the SAP S/4HANA Flow Executions module to specify date up to which you want to retrieve the invoice data.

    1.  Navigate to **SAP S/4HANA - RFC Spoke** &gt; **SAP S/4HANA Flow Executions**.

    2.  Click **New**.

    3.  In **Last Successful Execution**, specify the date up to which you want to retrieve the invoice data.

    4.  Click **Submit**.

        The Retrieve Incoming Invoice flow takes this date as an input and retrieves the invoice data. Depending on the configured flow trigger, the Retrieve Incoming Invoice flow periodically retrieves the invoice data. To view the invoice data, navigate to **SAP S/4HANA - RFC Spoke** &gt; **SAP S/4HANA Invoice Data**.


## Result

The spoke is configured and the actions can be used.

**Note:** If you want to use multiple connections, ensure that you create them as child alias records under the default connection alias record. Also, you must ensure that all the connection records are active.


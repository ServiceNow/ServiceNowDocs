---
title: Set up the SAP Concur spoke
description: Integrate the ServiceNow instance and SAP Concur by creating a custom OAuth application in SAP Concur to authenticate ServiceNow requests.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [SAP Concur Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up the SAP Concur spoke

Integrate the ServiceNow instance and SAP Concur by creating a custom OAuth application in SAP Concur to authenticate ServiceNow requests.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the SAP Concur spoke.
-   Role required: admin

## Procedure

1.  Register SAP Concur as an OAuth provider.

    1.  Navigate to **System OAuth** &gt; **Application Registry**.

    2.  Click **New**.

        The system displays the message **What kind of OAuth application?**

    3.  Select **Connect to a third party OAuth Provider**.

        The system displays a blank Application Registries form.

    4.  On the form, fill these values.

        |Field|Description|
        |-----|-----------|
        |Name|Name to uniquely identify the application registry. For example, `SAP Concur OAuth`.|
        |Client ID|Client ID of your SAP Concur client application. Contact SAP Concur Implementation team to obtain this value.|
        |Client Secret|Client secret of your SAP Concur client application. Contact SAP Concur Implementation team to obtain this value.|
        |Default Grant type|Grant type used to establish the token. Select **Resource Owner Password Credentials**.|
        |Token URL|URL from which the ServiceNow instance obtains the access token. Format of the token URL is, `https://<host-name>/oauth2/v0/token`. Here, host name is the fully qualified domain name of the target host where SAP Concur is installed.|
        |Redirect URL|OAuth callback endpoint in this format: `https://<instance>.service-now.com/oauth_redirect.do`.|

    5.  Right-click the form header, and click **Save**.

        -   The system validates the OAuth credentials and populates the **Redirect URL**.
        -   The system populates **OAuth Entity Profile** with **Grant Type** as **Resource Owner Password Credentials**. For example, **OAuth Entity Profile** is created with default **Name**, **SAPConcur**
2.  Create a credential record for the SAP Concur spoke.

    1.  Navigate to **Connections &amp; Credentials** &gt; **Credentials**.

    2.  Click **New**.

        The system displays the message **What type of Credentials would you like to create?**.

    3.  Select **OAuth 2.0 Credentials**.

    4.  On the form, fill these values.

        |Field|Value required|
        |-----|--------------|
        |Name|Name to uniquely identify the record. For example, enter `SAP Concur Cred`.|
        |Active|Option to actively use the credential record.|
        |OAuth Entity Profile|OAuth profile you created when you registered the custom SAP Concur application as an OAuth provider. For example, select **SAPConcur**.|
        |Applies to|Select the MID Servers that can use this credential. For example, select **All MID Servers**.|
        |Order|Select the order to apply this credential. For example, enter `100`.|

    5.  Save the record.

3.  Create a connection record for the SAP Concur spoke.

    1.  Navigate to **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases**.

    2.  Open for the record, **SAPConcur**.

    3.  From the **Connections** tab, click **New**.

    4.  On the form, fill these values.

        |Field|Value required|
        |-----|--------------|
        |Name|Name to uniquely identify the connection record. For example, enter `SAP Concur Connection`.|
        |Credential|Credential record you created for SAP Concur. For example, select **SAP Concur Cred**.|
        |Connection URL|Connection URL to connect to SAP Concur in this format: `<Host>/api`.|
        |Host|Fully qualified domain name of the target host where SAP Concur is installed. For example, `us.api.concursolutions.com` or `eu.api.concursolutions.com`.|
        |Protocol|`https`|
        |Base path|`/api`|

    5.  Click **Submit**.

4.  Generate OAuth token by providing the SAP Concur API user credentials.

    1.  Navigate to **Connections &amp; Credentials** &gt; **Credentials**.

    2.  Open the credential record you had created.

        Example: **SAP Concur Cred**

    3.  Click the **Get OAuth Token** related link and provide the SAP Concur API user credentials to generate the OAuth token.

5.  Configure the connection, **SAP Concur Event Subscription Service**.

    1.  Navigate to **Process Automation** &gt; **Flow Designer**.

    2.  Click the **Connections** tab.

    3.  Locate the **SAP Concur Event Subscription Service** connection alias and click **View Details**.

    4.  To configure the spoke for the first time, select **Configure** or click **Edit**.

    5.  On the **Connection** form, fill in the fields.

<table id="table_u4n_byy_gxb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the connection alias record.

</td></tr><tr><td>

Connection URL

</td><td>

Connection URL in this format: `https://www-<Region>.api.concursolutions.com`.Replace `<Region>` with the appropriate SAP Concur region.

</td></tr><tr><td>

Version

</td><td>

Enter `v4`.

</td></tr><tr><td>

Token URL

</td><td>

Token URL in this format: `https://<Region>.api.concursolutions.com/oauth2/v0/token`.Replace `<Region>` with the appropriate SAP Concur region.

</td></tr><tr><td>

Client ID

</td><td>

Client ID of your SAP Concur client application. Contact SAP Concur Implementation team to obtain this value.

</td></tr><tr><td>

Client Secret

</td><td>

Client secret of your SAP Concur client application. Contact SAP Concur Implementation team to obtain this value.

</td></tr></tbody>
</table>    6.  Click **Create and Get OAuth Token**.

    A confirmation message is displayed that the OAuth token is generated successfully.

6.  Configure the connection, **SAP Concur v4 APIs**.

    1.  Navigate to **Process Automation** &gt; **Flow Designer**.

    2.  Click the **Connections** tab.

    3.  Locate the **SAP Concur v4 APIs** connection alias and click **View Details**.

    4.  Click **Edit** or if you are configuring the spoke for the first time, click **Configure**.

    5.  On the **Connection** form, fill in the fields.

<table id="table_vqr_hzy_gxb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the connection alias record.

</td></tr><tr><td>

Connection URL

</td><td>

Connection URL in this format: `https://<Region>.api.concursolutions.com`.Replace `<Region>` with the appropriate SAP Concur region.

</td></tr><tr><td>

Version

</td><td>

Enter `v4`.

</td></tr><tr><td>

Token URL

</td><td>

Token URL in this format: `https://<Region>.api.concursolutions.com/oauth2/v0/token`.Replace `<Region>` with the appropriate SAP Concur region.

</td></tr><tr><td>

Client ID

</td><td>

Client ID of your SAP Concur client application. Contact SAP Concur Implementation team to obtain this value.

</td></tr><tr><td>

Client Secret

</td><td>

Client secret of your SAP Concur client application. Contact SAP Concur Implementation team to obtain this value.

</td></tr></tbody>
</table>    6.  Click **Create and Get OAuth Token**.

        In a new window, you will be prompted to enter **Username** and **Password**.

    7.  For **Username**, provide the Company ID of the SAP Concur instance and for **Password**, provide the value of Company Request Token.

        **Note:** Contact SAP Concur Implementation team to obtain the values of Company ID and Company Request Token.

    8.  Click **Get OAuth Token**.

7.  Map SAP Concur users to the ServiceNow user in the SAP Concur User Mappings module.

    1.  Navigate to **SAP Concur Spoke** &gt; **SAP Concur User Mappings**.

    2.  Click **New**.

    3.  On the form, fill these values.

        |Field|Description|
        |-----|-----------|
        |ServiceNow User|Reference to the user record in the User \[sys\_user\] table.|
        |SAP Concur User ID|User ID of the required user in SAP Concur.|

    4.  Click **Submit**.

        **Note:** If a user attempts to access data in the SAP Concur Expense Entries module without being mapped to the corresponding SAP Concur User ID in the SAP Concur User Mappings module, this error message is displayed.`A user with username adminn does not exist.`

        Map the ServiceNow user to the correspnding User ID in SAP Concur too access data in the SAP Concur Expense Entries module.

    -   SAP Concur spoke is set up.
    -   Data is retrieved and displayed in the SAP Concur Expense Entries and SAP Concur Expense Reports modules.


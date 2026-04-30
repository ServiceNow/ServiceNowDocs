---
title: Set up Docusign eSignature spoke using authorization code grant
description: Integrate the ServiceNow instance and Docusign eSignature spoke by using Authorization Code to authenticate ServiceNow requests.Configure a custom OAuth application from your Docusign account to enable authentication with the Docusign eSignature spoke.Integrate the ServiceNow instance and Docusign account instance using authorization code grant to authenticate ServiceNow requests.
locale: en-US
release: yokohama
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Docusign eSignature Spoke, Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Data and Automation]
---

# Set up Docusign eSignature spoke using authorization code grant

Integrate the ServiceNow instance and Docusign eSignature spoke by using Authorization Code to authenticate ServiceNow requests.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the Docusign eSignature spoke.
-   Role required: admin

**Important:** If you are setting up Docusign eSignature spoke using authorization code grant, you need not set up the spoke using JWT grant.

## Configure the Docusign account

Configure a custom OAuth application from your Docusign account to enable authentication with the Docusign eSignature spoke.

### About this task

Complete these steps from your Docusign account. See the [Docusign Developer Center](https://developers.docusign.com/) documentation for instructions on creating and configuring custom applications. Docusign uses a scripted webhook to send signed document data to ServiceNow instance. This enables flow designers to pause a flow until a document is signed, and use document data in the flow.

### Before you begin

Docusign requirements:

-   Docusign account
-   Docusign app configured to integrate with ServiceNow
-   Role required: Docusign administrator

### Procedure

1.  Log in to the [Docusign account](https://account-d.docusign.com/) as an admin.

2.  From your Docusign account, register your application.

    **Note:** Ensure that you select the **Authorization Code Grant** option for **User Application**.

3.  Generate an integrator key and secret key.

4.  Record the values of integrator key and secret key to register the app as a third-party OAuth provider on your ServiceNow instance.

    You need these values when you [Configure the connection for Docusign eSignature spoke](setup-docusign-authorization-code.md#).

5.  Add the ServiceNow OAuth Redirect URL in your Docusign account.

    1.  Navigate to **Integrations** &gt; **App and Keys**.

    2.  Under **Apps and Integration Keys**,find the required app.

    3.  For the required app, click the **Actions** drop-down list and click **Edit**.

    4.  Under **Additional settings**, click **Add URI** and add the OAuth callback endpoint in this format: `https://<instance>.service-now.com/oauth_redirect.do`.

        ![Add Redirect URI in Docusign account.](../image/docusign-add-redirect-uri.png)

6.  Obtain the value of **Account Base URI** from the Docusign account.

    1.  Navigate to **Integrations** &gt; **App and Keys**.

    2.  Under **My Account Information**, you can find the value of the **Account Base URI**.

        ![Account Base URI.](../image/docusign-acct-base-uri.png)

    3.  Copy and record this value for later use.


## Configure the connection for Docusign eSignature spoke

Integrate the ServiceNow instance and Docusign account instance using authorization code grant to authenticate ServiceNow requests.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  Click the **Integrations** tab.

3.  Under **Connections**, toggle and enable the **Outbound** connections.

4.  Locate the alias for Docusign and click **View Details**.

    **Note:** Don't click Add Connection.

    ![Connection template for Docusign eSignature spoke](../image/docusign-conn-template.png)

5.  If you are configuring the spoke for the first time, click **Configure**.

    ![Configure a connection for the first time for Docusign eSignature spoke](../image/docusign-conn-tempte-config.png)

6.  On the Configure Connection form, fill in the fields.

<table id="table_jlz_mjr_d1c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Connection Name

</td><td>

Unique name to identify the connection.

</td></tr><tr><td>

Connection URL

</td><td>

**Account Base URI** to connect to Docusign environment. This value can be obtained from your Docusign account. For more information see, [Configure the Docusign account](setup-docusign-authorization-code.md#).

</td></tr><tr><td>

API Version

</td><td>

Docusign API version. The default value is v2.1.

</td></tr><tr><td>

Authorization URL

</td><td>

Docusign authorization URL.-   For developer sandbox environment, enter `https://account-d.docusign.com/oauth/auth`.
-   For live production system, enter `https://account.docusign.com/oauth/auth`.


</td></tr><tr><td>

Token URL

</td><td>

URL from which the ServiceNow instance obtains the access token.-   For developer sandbox environment, enter `https://account-d.docusign.com/oauth/token`.
-   For live production system, enter `https://account.docusign.com/oauth/token`. For more information see, [Post Go-Live](https://developers.docusign.com/esign-rest-api/guides/post-go-live) and [User Info Endpoint Reference](https://developers.docusign.com/esign-rest-api/guides/authentication/user-info-endpoints) in the [Docusign Developer Center](https://developers.docusign.com/) documentation.


</td></tr><tr><td>

OAuth Client ID

</td><td>

Integrator key of your Docusign account.

</td></tr><tr><td>

OAuth Client Secret

</td><td>

Secret key \(client secret\) of your Docusign account.

</td></tr><tr><td>

OAuth Redirect URL

</td><td>

OAuth callback endpoint in this format: `https://<instance>.service-now.com/oauth_redirect.do`.**Note:** Ensure that you add this URL in your Docusign account. For more information see, [Configure the Docusign account](setup-docusign-authorization-code.md#).

</td></tr></tbody>
</table>    ![Docusign connection.](../image/docusign-conf-temp.png)

7.  Click **Configure and Get OAuth Token**.



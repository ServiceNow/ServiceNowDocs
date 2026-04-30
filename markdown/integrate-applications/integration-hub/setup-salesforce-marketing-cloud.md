---
title: Set up the Salesforce Marketing Cloud spoke
description: Integrate the ServiceNow instance and Salesforce Marketing Cloud by using Salesforce Marketing Cloud credentials to authenticate ServiceNow requests.You can use basic authentication to validate ServiceNow requests instance with Salesforce Marketing Cloud spoke.Create a user with which you can access the Salesforce Marketing Cloud SOAP API. The SOAP API enables you to retrieve records from your Salesforce Marketing Cloud data extensions and get information about your Salesforce Marketing Cloud users.Create a connection and credential for Salesforce Marketing Cloud so that you can connect your ServiceNow instance with the Salesforce Marketing Cloud SOAP API.You can use OAuth 2.0 to validate ServiceNow requests instance with Salesforce Marketing Cloud spoke.Create Salesforce Marketing Cloud OAuth 2.0 credentials to use Salesforce Marketing Cloud spoke.Create a connection and credential for OAuth 2.0 authorization of Salesforce Marketing Cloud spoke.
locale: en-US
release: yokohama
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 6
breadcrumb: [Salesforce Marketing Cloud Spoke, Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Data and Automation]
---

# Set up the Salesforce Marketing Cloud spoke

Integrate the ServiceNow instance and Salesforce Marketing Cloud by using Salesforce Marketing Cloud credentials to authenticate ServiceNow requests.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the Salesforce Marketing Cloud spoke.
-   Salesforce Marketing Cloud role required: admin user with privileges to create new users and roles.
-   Role required: admin.

## Procedure

1.  [Using basic authentication for Salesforce Marketing Cloud spoke](setup-salesforce-marketing-cloud.md#)

2.  [Using OAuth 2.0 for Salesforce Marketing Cloud spoke](setup-salesforce-marketing-cloud.md#)


## Using basic authentication for Salesforce Marketing Cloud spoke

You can use basic authentication to validate ServiceNow requests instance with Salesforce Marketing Cloud spoke.

### Create a user for accessing the Salesforce Marketing Cloud SOAP API

Create a user with which you can access the Salesforce Marketing Cloud SOAP API. The SOAP API enables you to retrieve records from your Salesforce Marketing Cloud data extensions and get information about your Salesforce Marketing Cloud users.

#### Before you begin

Role required: Salesforce admin user with privileges to create new users and roles.

#### Procedure

1.  From a web browser, go to your Salesforce Marketing Cloud instance.

2.  Log in using your admin credentials.

3.  On the page header of your instance, click your profile icon and then select **Setup**.

    The Setup page opens.

4.  Create a Salesforce Marketing Cloud user.

    1.  Navigate to **Administration** &gt; **Users** &gt; **Users** and then click **Create**.

        The New User form opens.

    2.  In the General Settings form section, fill in the fields.

<table id="table_vdp_vky_s4b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the user.

</td></tr><tr><td>

Reply Email Address

</td><td>

Email address that you want to send and reply to email messages from. Salesforce Marketing Cloud also sends forgotten password requests to this email address. After you enter an email address, click **Verify** to verify the email address.

</td></tr><tr><td>

Add to From Name Dropdown

</td><td>

Option to send the reply email address through a domain verification process before the email address populates in an email.

</td></tr><tr><td>

Notification Email Address

</td><td>

Email address that you want to send Salesforce Marketing Cloud notifications to.

</td></tr><tr><td>

Username

</td><td>

Username for the user.

</td></tr><tr><td>

External Key

</td><td>

Key that uniquely identifies the user during API calls.

</td></tr><tr><td>

Time Zone

</td><td>

Time zone in which the user is located.

</td></tr><tr><td>

Culture Code

</td><td>

Language that is used on the Salesforce Marketing Cloud user interface for this user.

</td></tr><tr><td>

API User

</td><td>

Option indicating whether the user can access the Salesforce Marketing Cloud APIs. Select the check box to enable this option.

</td></tr><tr><td>

Temporary Password

</td><td>

Temporary password with which the user can log in for the first time. The user is prompted to change this password on the first login.

</td></tr><tr><td>

Verify Password

</td><td>

Field to verify the temporary password.

</td></tr></tbody>
</table>    3.  Click **Save**.

5.  Create a user role that enables assigned users to access the Salesforce Marketing Cloud SOAP API and also manage users and data extensions.

    1.  Navigate to **Administration** &gt; **Users** &gt; **Roles** and then click **Create**.

        The New Role form opens.

    2.  In the Properties form section, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Name|Name of the user role.|
        |External Key|Key that uniquely identifies the user role.|
        |Description|Description of the user role.|

    3.  In the Permissions form section, expand the **Email** &gt; **Subscribers** &gt; **Data Extension** permission category and then select the **Allow** check box for the View and Manage Data access permissions.

    4.  Expand the **Email** &gt; **Admin** &gt; **API Access** permission category and then select the **Allow** check box for the WebService API access permission.

    5.  Expand the **Administration** &gt; **Users** permission category and then select the **Allow** check box for the following access permissions:

        -   View
        -   Update
        -   Disable
        -   Manage Business Units
    6.  Click **Save**.

6.  Assign the user role to your Salesforce Marketing Cloud user.

    1.  Navigate to **Administration** &gt; **Users** &gt; **Users**.

    2.  From the list of available users, select the check box for the user that you created in [step 4](setup-salesforce-marketing-cloud.md#create-user).

    3.  Click **Manage Roles**.

        The Roles form for the selected user opens.

    4.  In the Roles form section, click **Edit Roles**.

    5.  When the list of available roles appears, select the check box for the user role that you created in [step 5](setup-salesforce-marketing-cloud.md#create-user-role).

    6.  Click **Save**.


### Create a connection and credential for Salesforce Marketing Cloud

Create a connection and credential for Salesforce Marketing Cloud so that you can connect your ServiceNow instance with the Salesforce Marketing Cloud SOAP API.

#### Before you begin

Role required: admin

#### Procedure

1.  From your ServiceNow instance, navigate to **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases**.

2.  From the list of available connection and credential aliases, select **SalesforceMarketingCloud**.

3.  On the Connection &amp; Credential Aliases form, click the **Create New Connection &amp; Credential** related link.

    The Create Connection and Credential dialog box opens.

4.  In the dialog box, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Please Enter the Connection Information|
    |Connection Name|Name of the connection.|
    |SOAP Connection URL|URL of your SOAPConnection endpoint. Enter `https://<*subdomain*>.soap.marketingcloudapis.com/Service.asmx`, where &lt;*subdomain*&gt; is your Salesforce Marketing Cloud subdomain.|
    |Please Enter the Credential Information|
    |Username Profile Name|Name of your credentials.|
    |Username|Username of the user that you can access the Salesforce Marketing Cloud SOAP API with. Enter the username of the user that you created in [Create a user for accessing the Salesforce Marketing Cloud SOAP API](setup-salesforce-marketing-cloud.md#).|
    |Password|Password of the user that you can access the Salesforce Marketing Cloud SOAP API with. Enter the password of the user that you created in [Create a user for accessing the Salesforce Marketing Cloud SOAP API](setup-salesforce-marketing-cloud.md#).|

5.  Click **Create**.


## Using OAuth 2.0 for Salesforce Marketing Cloud spoke

You can use OAuth 2.0 to validate ServiceNow requests instance with Salesforce Marketing Cloud spoke.

### Create OAuth 2.0 credentials for Salesforce Marketing Cloud spoke

Create Salesforce Marketing Cloud OAuth 2.0 credentials to use Salesforce Marketing Cloud spoke.

#### Before you begin

Role required: Salesforce Marketing Cloud admin

#### Procedure

1.  Log in to the Salesforce Marketing Cloud tenant.

2.  Navigate to **Setup Home** &gt; **Platform Tools** &gt; **Apps** &gt; **Installed Packages**.

3.  Select **New** to create a package.

4.  Select **Add Component**.

5.  Select **API Integration** to integrate Salesforce Marketing Cloud APIs to your application.

6.  Select **Next**.

7.  Select **Server-to-Server** as the integration type.

8.  Select **Next**.

9.  Select the required scopes for your integration.

10. Select **Save**.

    Your Client Id and Client Secret gets displayed in your configuration summary. Navigate to the Components section under **SETUP** &gt; **INSTALLED PACKAGES** &gt; **DETAILS** to view the Client Id and Client Secret. Copy the values to use them later.


### Create a connection and credential for Salesforce Marketing Cloud spoke

Create a connection and credential for OAuth 2.0 authorization of Salesforce Marketing Cloud spoke.

#### Before you begin

Role required: admin

-   [Create OAuth 2.0 credentials for Salesforce Marketing Cloud spoke](setup-salesforce-marketing-cloud.md#)

#### Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases**.

2.  Open the **SalesforceMarketingCloudSOAPConnection** record.

3.  From the **Related Links** tab, click **Create New Connection &amp; Credential** link.

4.  On the Connection &amp; Credential Aliases form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Connection Name|Name to uniquely identify the connection. For example, `SFMC SOAP Connection`.|
    |SOAP Connection URL|URL of your SOAP Connection endpoint. Enter `https://<subdomain>.soap.marketingcloudapis.com/Service.asmx`, where *&lt;subdomain&gt;* is your Salesforce Marketing Cloud subdomain.|
    |OAuth Client ID|Client ID created for the Salesforce Marketing Cloud spoke.|
    |OAuth Client Secret|Client secret created for the Salesforce Marketing Cloud spoke.|
    |OAuth Redirect URL|OAuth redirect URL. It must be in the format `https://<instance-name.service-now.com>/oauth_redirect.do`.|
    |Contacts Counts Data Extension|Name of the data extension that you want to retrieve Contacts Counts report data from.|

5.  Select **Create and Get OAuth Token**.



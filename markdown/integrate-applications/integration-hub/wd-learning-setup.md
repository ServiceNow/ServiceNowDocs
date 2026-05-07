---
title: Set up the Workday Learning spoke
description: Integrate the ServiceNow instance Workday instance by using the OAuth 2.0 to authenticate ServiceNow requests.Configure your ServiceNow instance to perform actions that use the Workday SOAP web services.Configure the default connection and credential record by providing the required details to authenticate requests.Set up the required Workday reports in your ServiceNow instance.Update the timezone of the Workday tenant in your ServiceNow instance.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-05-06"
reading_time_minutes: 4
breadcrumb: [Workday Learning Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up the Workday Learning spoke

Integrate the ServiceNow® instance Workday instance by using the OAuth 2.0 to authenticate ServiceNow® requests.

## Before you begin

-   Configure these reports in the Workday instance:
    -   Learning Assignment
    -   Learning Enrollment
    -   Track Approval
-   Request an Integration Hub subscription.
-   Activate the Workday Learning spoke.
-   Role required: admin.

## Configurations to use Workday SOAP web services

Configure your ServiceNow® instance to perform actions that use the Workday SOAP web services.

### Before you begin

Role required: admin

### Procedure

1.  Create a WS-Security Username Profile to provide your Workday credentials to authenticate requests from ServiceNow®.

    1.  Navigate to **All** &gt; **Integration Hub** &gt; **SOAP Integrations** &gt; **WS-Security Username Profiles**.

    2.  Click **New**.

    3.  On the form, fill these values.

        |Field|Description|
        |-----|-----------|
        |Name|Name to uniquely identify this credential. For example, enter `Workday Learning User`.|
        |Application|Application in which the record is applicable. Select **Workday Learning Spoke**.|
        |Username|Workday user who has integration rights using Workday Web Services.|
        |Password|Password of the Workday user.|

    4.  Click **Submit**.

2.  Configure the SOAP security profile by adding the security user name profile you had created to authenticate requests from ServiceNow.

    1.  Navigate to **All** &gt; **IntegrationHub** &gt; **SOAP Integrations** &gt; **SOAP Security Policies**.

    2.  Open the record for the Workday Learning spoke, for example, **Workday Learning**.

        **Note:** If you intend to use another SOAP security policy record and not the default record, you must ensure that you select that record you had created in all the actions that use Workday SOAP web services.

    3.  For **WS-Security Username Profile**, select the security username profile you had created for the Workday Learning spoke.

    4.  Do not provide value in **WS-Security X.509 Profile**.

    5.  Right-click the form header and click **Save**.


## Configurations to use Workday REST API

Configure the default connection and credential record by providing the required details to authenticate requests.

### Before you begin

Role required: admin

### Procedure

1.  Configure the default application registry to register Workday Learning as an OAuth provider.

    1.  Navigate to **System OAuth** &gt; **Application Registry**.

    2.  Open the record, **Workday Learning**.

    3.  On the form, fill these values.

        |Field|Description|
        |-----|-----------|
        |Client ID|Client ID you had copied when you registered an API client in your Workday instance.|
        |Client Secret|Client secret you had copied when you registered an API client in your Workday instance.|
        |Authorization URL|Authorization URL you had copied when you registered an API client in your Workday instance.|
        |Token URL|Token URL you had copied when you registered an API client in your Workday instance.|
        |Redirect URL|Redirect URL of the ServiceNow® instance in this format: `https://<ServiceNow-Instance-Name>.service-now.com/oauth_redirect.do`.|
        |Default Grant type|Default grant type to establish the OAuth token. Select **Authorization Code**.|

    4.  Click **Update**.

2.  Create a credential record.

    1.  Navigate to **Integration Hub** &gt; **Credentials**.

    2.  Click **New**.

        The system displays the message `What type of Credentials would you like to create?`.

    3.  Select **OAuth 2.0 Credentials**.

    4.  On the form, fill these values.

        |Field|Description|
        |-----|-----------|
        |Name|Name to identify the credential record. For example, `Workday Learning Cred`.|
        |OAuth Entity Profile|Default OAuth entity profile record. For example, `Workday Learning default_profile`.|

    5.  Click **Submit**.

3.  Configure the default connection and credential alias record.

    1.  Navigate to **Integration Hub** &gt; **Connection &amp; Credential Aliases**.

    2.  Open the **Workday Learning** record.

    3.  In the **Connections** tab, click **New**.

    4.  On the form, fill these values.

        |Field|Description|
        |-----|-----------|
        |Name|Name to identify the connection record. For example, **Workday Learning Conn**.|
        |Credential|Associated credential record. Select the credential record you had created earlier. For example, `Workday Learning Cred`.|
        |Connection URL|URL to connect to your Workday instance.|

    5.  In the **Attributes** tab, specify the tenant name of your Workday instance in **Tenant Name**.

    6.  Click **Submit**.

4.  Navigate to **Integration Hub** &gt; **Credentials**.

5.  Open the record, **Workday Cred**.

6.  Click **Get OAuth Token**.

    System prompts to confirm if you want to authorize Workday.

7.  Click **Allow**.

    ![Authorize Workday.](../image/wd-learning-enable.png)


## Configure the Workday reports

Set up the required Workday reports in your ServiceNow® instance.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **Workday Learning** &gt; **Report Configuration**.

2.  On the form, fill the fields.

    |Field|Description|
    |-----|-----------|
    |Workday learning assignment RAAS report name|Report name of the learning assignment RAAS report.|
    |Workday learning to dos report owner username|Username of the learning todos RAAS report owner.|
    |Workday learning to dos RAAS report name|Report name of the learning todos RAAS report.|
    |Workday learning enrollment RAAS report name|Report name of the learning enrollment RAAS report.|
    |Learning organization type|Organization type to which employee belongs to. You can select either **Organization Reference ID** or **WID**.|
    |Workday learning enrollment report owner username|Username of the learning enrollment RAAS report owner.|
    |Initial load start date time|Initial start date and time that is needed for the Look up Approvals actions.|
    |Workday learning assignment report owner username|Username of the learning assignment RAAS report owner.|
    |Learning organization ID|Unique identifiers of the organizations separated by commas \(,\). You can provide a maximum of upto 999 identifiers.|

3.  Click **Submit**.

    **Note:** You can maintain only one record in this module.


## Update timezone

Update the timezone of the Workday tenant in your ServiceNow instance.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **Workday Learning** &gt; **Profile Sync Configuration**.

2.  Click **New**.

3.  On the form, select **Workday tenant time zone** and **Domain** as per your requirement.

4.  Click **Submit**.



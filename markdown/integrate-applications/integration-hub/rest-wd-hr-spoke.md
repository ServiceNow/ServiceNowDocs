---
title: Configurations to use Workday REST API
description: Configure your ServiceNow instance to perform actions that use the Workday REST API.Use short description 1 or 2 and revise it to provide spoke-specific information for your application. Description 1:Register the Workday HR instance as the OAuth provider so that the ServiceNow instance can request OAuth 2.0 tokens.Register API client in your Workday account and generate a token URL for Workday HR spoke.Configure your ServiceNow instance to perform actions that use the Workday HR REST API using an OAuth authorization template.Add and configure a Workday HR REST API connection to authenticate ServiceNow requests in Workday HR spoke.Configure your ServiceNow instance to perform actions that use the Workday HR REST API by manually creating connection and credential records.Create a credential record for the Workday HR instance. The Workday HR spoke connection and credential alias uses these credentials to authorize actions.Modify the short description to provide spoke specific information.Create a connection record for your Workday HR instance. The Workday HR spoke connection and credential aliases use these connections to perform actions in Workday HR.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 6
breadcrumb: [Workday HR Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Configurations to use Workday REST API

Configure your ServiceNow instance to perform actions that use the Workday REST API.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate Workday HR spoke.
-   From Workday, obtain these values and record them for later use. These values are need to register your client:
    -   Client ID
    -   Client Secret
    -   Workday REST API Endpoint
    -   Token Endpoint
    -   Authorization Endpoint
-   Role required: admin

## About this task

Workday REST and Report-as-a-Service \(RAAS\) API works with OAuth 2.0 to authorize access to resources in your Workday tenant. To use OAuth 2.0, you must register your client in the tenant, using the Register API Client task.

Configure your ServiceNow instance to use the Workday REST API if you need to use these REST-based spoke actions:

-   Get My Reporting Structure
-   Look up Object Custom Fields
-   Update Object Custom Fields
-   Look up Payslip
-   Look up Total Rewards Using Report
-   Look up Custom Reports
-   Look up Inbox Items
-   Look up Merit And Benefit Plan Details Of An Employee
-   Look up Holiday Calendars Reference WID Of An Employee
-   Look up Schedule Calendars Reference WID Of An Employee
-   Look up Holiday Calendars Of An Employee
-   Look up using WQL Stream

**Note:** These configurations are needed to use the REST-based spoke actions.

## Register Workday HR as an OAuth provider

Register the Workday HR instance as the OAuth provider so that the ServiceNow instance can request OAuth 2.0 tokens.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **System OAuth** &gt; **Application Registry**.

2.  Click **New**.

    The system displays this message: `What kind of OAuth application?`.

3.  Select **Connect to a third party OAuth Provider**.

4.  On the form, fill these values.

    |Field|Description|
    |-----|-----------|
    |Name|Name to uniquely identify the record. For example, enter: `Workday HR OAuth`|
    |Application|Application in which the record is applicable. Select **Workday HR Spoke**.|
    |Client ID|Client ID generated while registering your client.|
    |Client Secret|Client secret generated while registering your client.|
    |Authorization URL|Authorization endpoint generated while registering your client.|
    |Token URL|Token endpoint generated while registering your client.|
    |Redirect URL|OAuth callback endpoint in this format: `https://<instance>.service-now.com/oauth_redirect.do`|
    |Default Grant Type|Grant type used to establish the token. Select **Authorization Code**.|
    |Active|Option to actively use the application registry.|

5.  Right-click the form header, and click **Save**.

    An OAuth entity profile is created.


## Generate token URL for Workday HR spoke

Register API client in your Workday account and generate a token URL for Workday HR spoke.

### Before you begin

Role required: admin

### Procedure

1.  Log into your Workday tenant.

2.  Navigate to Search and enter `Register API Client` task.

3.  On the Register API Client, fill in the details.

    |Field|Description|
    |-----|-----------|
    |Client Name|Client name of the app. For example, `Workday HR spoke`.|
    |Client Grant Type|Select Authorisation Code Grant.|
    |Access Token Type|Access Token Type: Select Bearer|
    |Redirection URI|Enter your ServiceNow URL in this format: `https://<instance>.service-now.com/oauth_redirect.do`.|
    |Non-Expiring Refresh tokens|Option to enable refresh tokens which do not expire.|
    |Scope \(Functional Areas\)|Select the required functional areas.|
    |Include Workday Owned Scope|Option to select scope that are owned by Workday.|

4.  Click **OK**.


### Result

Copy and store the generated Token Endpoint value for configuring system property.

## Option 1: Configuration to use Workday HR REST API with a template

Configure your ServiceNow instance to perform actions that use the Workday HR REST API using an OAuth authorization template.

### Before you begin

Role required: admin

### Configure a connection for Workday HR REST API

Add and configure a Workday HR REST API connection to authenticate ServiceNow requests in Workday HR spoke.

#### Before you begin

-   Role required: admin
-   [Register Workday HR as an OAuth provider](rest-wd-hr-spoke.md#)

#### Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  Select **Integrations**.

3.  Select the **Connections** tab.

4.  Use the search box to find the **WorkdayHR** connection alias.

5.  Click **View Details**.

    ![Connection template for Workday HR spoke](../image/wkday-hr-conn-temp.png)

6.  Configure a cloud connection.

    1.  Add or edit a cloud connection.
        -   To set up an existing connection, select **Configure** or **Edit**.![Configure the connection using connection template for Workday HR spoke](../image/wkday-hr-con-config.png)
        -   To create and configure a new connection, select **Add Connection**.
    2.  On the configuration form, fill in the fields.
    |Field|Description|
    |-----|-----------|
    |Name|Name to uniquely identify the connection. For example, `Workday HR spoke connection`.|
    |Connection URL|URL to make a connection to Workday HR. Use this format: `https://<workday_host>/ccx/service/<tenant_name>`|
    |Tenant Name|Name of the Workday tenant. For example, `bcone_gms1`.|
    |API Version|Version of the Workday API to use for requests.|
    |Client ID|Client ID generated in Workday for OAuth authentication.|
    |Client Secret|Client Secret generated in Workday for OAuth authentication.|
    |Authorization URL|URL used to authorize the OAuth connection. Use this format: `https://<workday_host>/authorize`|
    |Token URL|URL used to generate the OAuth token. Use this format: `https://<workday_host>/token`|
    |OAuth Redirect URL|URL where Workday redirects after successful authentication. Use this format: `https://<instance_name>.service-now.com/oauth_redirect.do`|

7.  Click **Save and Get OAuth Token**.


#### Result

The spoke connection is configured and ready to be used.

## Option 2: Configuration to use Workday HR REST API without a Template

Configure your ServiceNow instance to perform actions that use the Workday HR REST API by manually creating connection and credential records.

### Before you begin

Role required: admin

### Create a credential record for the Workday HR spoke

Create a credential record for the Workday HR instance. The Workday HR spoke connection and credential alias uses these credentials to authorize actions.

#### Before you begin

Role required: admin.

#### Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Credentials**.

2.  Click **New**.

    The system displays this message: `What type of Credentials would you like to create?`

3.  Select **OAuth 2.0 Credentials**.

4.  On the form, fill these values.

    |Field|Description|
    |-----|-----------|
    |Name|Name to uniquely identify the record. For example, `Workday HR Cred`.|
    |Active|Option to actively use the credential record.|
    |OAuth Entity Profile|OAuth entity profile created during the registration of Workday HR as an OAuth provider. For example,  OAuth Profile.|

5.  Right-click the form header and click **Submit**.

6.  To generate the OAuth token, click the **Get OAuth Token** related link.


### Create a connection record for the Workday HR spoke

Create a connection record for your Workday HR instance. The Workday HR spoke connection and credential aliases use these connections to perform actions in Workday HR.

#### Before you begin

Role required: admin.

#### Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connections &amp; Credentials Aliases**.

2.  Open the alias record, **WorkdayHR**.

3.  From the **Connections** tab, click **New**.

4.  On the form, fill these fields.

    **Note:** Ensure that you create the connection record in the **Workday HR Spoke** application.

    |Field|Description|
    |-----|-----------|
    |Name|Name to uniquely identify the record. For example, `Workday HR Connection`.|
    |Credential|Credential record created for Workday HR spoke. For example, `Workday HR Cred`.|
    |Connection alias|Alias record associated with this connection.|
    |Connection URL|URL to connect to your Workday HR instance.|
    |Active|Option to actively use the connection record.|

5.  In the **Attributes** tab, fill in these values.

    |Field|Value|
    |-----|-----|
    |Tenant Name|Tenant name of your Workday application.|
    |Version|v1|

6.  Click **Submit**.



---
title: Configurations to use Workday SOAP Personal Auth
description: Configure your ServiceNow instance to perform Workday HR SOAP based actions with personal authentication.Provide the base URL of your Workday HR instance in the Connection Details \[connection\_details\] table. Spoke actions based on the SOAP API, use these details for the action execution.Create an application registry so that the ServiceNow instance can request OAuth 2.0 tokens for personal authentication.Configure the connection and credential alias to authenticate ServiceNow requests to Workday HR using personal authentication.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/integration-hub/configs-wd-hr-soap-personalauth.html
release: australia
product: Integration Hub
classification: integration-hub
topic_type: reference
last_updated: "2026-07-07"
reading_time_minutes: 2
breadcrumb: [Workday HR Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Configurations to use Workday SOAP Personal Auth

Configure your ServiceNow instance to perform Workday HR SOAP based actions with personal authentication.

Personal authentication grants access to individual users, instead of a shared system account, when your Workday HR SOAP based actions run.

## Provide the Workday HR base URL

Provide the base URL of your Workday HR instance in the Connection Details \[connection\_details\] table. Spoke actions based on the SOAP API, use these details for the action execution.

### Before you begin

Role required: admin.

### Procedure

1.  Navigate to **All** &gt; **Workday HR Spoke** &gt; **Connection Details**.

2.  Click the **Show List** related list.

3.  Click **New**.

4.  On the form, fill these values.

    |Field|Description|
    |-----|-----------|
    |Base URL|Base URL of the Workday instance or tenant name. Enter the base URL in this format `https://<workday_host_url>/ccx/service/<workday_tenant_name>`|
    |Version|Version of the API. For example, enter `v33.2`.|
    |Webservice Type|Type of web service. Select `SOAP`.|

5.  Click **Save**.


## Configure the application registry for Workday HR SOAP API

Create an application registry so that the ServiceNow instance can request OAuth 2.0 tokens for personal authentication.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **System OAuth** &gt; **Application Registry**.

2.  Open the record for **WorkdayHR**.

3.  On the form, fill in these values.

    |Field|Description|
    |-----|-----------|
    |Client ID|Client ID created during the Workday HR API client configuration for personal authentication.|
    |Client Secret|Client Secret created during the Workday HR API client configuration for personal authentication.|
    |Authorization URL|OAuth authorization code endpoint from the Workday tenant.|
    |Token URL|OAuth server token endpoint from the Workday tenant.|

4.  Right-click the form header, and click **Save**.


### Result

The application registry for personal authentication is configured.

## Configure the connection and credential alias

Configure the connection and credential alias to authenticate ServiceNow requests to Workday HR using personal authentication.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Connection &amp; Credential Aliases**.

2.  Open the **WorkdayHR** record.

3.  From the **Connections** tab, select **New**.

4.  On the form, fill in these fields.

    |Field|Description|
    |-----|-----------|
    |Connection URL|URL to make a connection to Workday HR.|

    |Field|Description|
    |-----|-----------|
    |tenant\_name|Name of the Workday tenant.|
    |version|Version of the Workday tenant.|

5.  Click **Save**.

6.  Open the credential record and select the **Integration Type**.

    |Option|Description|
    |------|-----------|
    |Personal|Grants access to individual users.|
    |System|Grants access to a group of users who can access the system.|

7.  Select the **Get OAuth Token** link.

    You are redirected to the Workday HR portal for authentication. After your authentication is successful, an OAuth token is generated.


### Result

The connection and credential alias for personal authentication is configured.


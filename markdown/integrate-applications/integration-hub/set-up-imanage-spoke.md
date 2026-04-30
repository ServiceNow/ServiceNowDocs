---
title: Set up iManage spoke
description: Integrate a ServiceNow instance and the iManage spoke by using  iManage credentials to authenticate  ServiceNow  requests.Request an application with iManage and register it in the iManage Control Center.Register iManage as an OAuth provider to allow the instance to request OAuth 2.0 tokens.Integrate the connection to your iManage account. The iManage spoke connection &amp; credential aliases use these connections to perform actions in iManage.
locale: en-US
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [iManage Spoke, Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Creating integrations with applications]
---

# Set up iManage spoke

Integrate a ServiceNow instance and the iManage spoke by using  iManage credentials to authenticate  ServiceNow  requests.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the iManage spoke.

Role required: admin

## Request an application with iManage

Request an application with iManage and register it in the iManage Control Center.

### Before you begin

You must have an iManage account and tenant administrator credentials.

Role required: admin

### Procedure

1.  As an iManage Cloud \(cloudimanage.com\) customer, send an email to appregistration@imanage.com with the following details.

    -   Application Name: ServiceNow - External Storage
    -   Redirect\_Url: `<your-instance>/oauth_redirect.do`
    -   Customers name: Give your Customer name
    -   Tenant/Customers ID: Give your tenant or customer ID
    iManage will review and respond with the Client ID and Secret

2.  Once you have the Client ID/ Secret, register your application in iManage Control Center by following the document [Adding an application](https://docs.imanage.com/cloud/cc-help/en-US/Adding_an_application.html).

    **Note:**

    -   This integration capability has been validated for iManage cloud. If you want to use it for iManage on-premises, validate that it meets your requirements before using it.
    -   If you are a iManage on-premises user, follow the document [Adding an application package](https://docs.imanage.com/cc-help/10.4.3/en-US/Adding_Apps.html) to register your application.

### What to do next

[Register iManage as OAuth provider](set-up-imanage-spoke.md#).

## Register iManage as OAuth provider

Register iManage as an OAuth provider to allow the instance to request OAuth 2.0 tokens.

### Before you begin

Note the following requirements:

-   Integration Hub subscription.
-   iManage access credentials
-   The iManage spoke must be activated

Role required: admin

### Procedure

1.  On your ServiceNow® instance, navigate to **System OAuth** &gt; **Application Registry**.

2.  Select **New**.

3.  On the page titled **What kind of OAuth application**, select **Connect to a third-party OAuth Provider**.

4.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Unique name to identify the record, for example, `iManage OAuth profile`.|
    |Client ID|Application ID of the iManage application.|
    |Client Secret|The Client Secret you generated when you created the application.|
    |Default Grant type|The value in this field should be **Password**.|
    |Token URL|The value in this field should be `https://cloudimanage.com/auth/oauth2/token`. You might have to unlock the field to enter the value.|
    |Redirect URL|The value in this field should be `https://<your-instance>.service-now.com/oauth_redirect.do`. You might have to unlock the field to enter the value.|

5.  Right-click the form header, and select **Save**.

    The system validates the OAuth credentials.


### Result

iManage is registered as an OAuth provider, which enables the instance to request OAuth 2.0 tokens.

### What to do next

[Integrate the iManage spoke with ServiceNow instance](set-up-imanage-spoke.md#).

## Integrate the iManage spoke with ServiceNow instance

Integrate the connection to your iManage account. The iManage spoke connection &amp; credential aliases use these connections to perform actions in iManage.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **IntegrationHub** &gt; **Connections &amp; Credentials** &gt; **iManage**.

2.  Select the **Create New Connection &amp; Credential** related link.

3.  On the form, fill in the fields.

    |Field|Value required|
    |-----|--------------|
    |Connection Name|Name to identify the connection. This field is automatically set to iManage spoke connection.|
    |Connection URL|The URL to establish connection with the spoke. This field is automatically set to `https://cloudimanage.com`. Update the default URL to your specific URL required to establish the connection.|
    |OAuth Entity Name|Name of the OAuth entity profile. This field is automatically set to iManage spoke Auth.|
    |OAuth Client ID|Client ID of the iManage application you registered in the registration portal.|
    |OAuth Client Secret|Client Secret generated when you registered the application in the iManage portal.|
    |OAuth Redirect URL|The redirect URL. The format of the URL is https://&lt;your-instance&gt;.service-now.com/oauth\_redirect.do.|

4.  Select **Create and Get OAuth Token**.


### Result

The iManage spoke is set up and integrated with your ServiceNow instance.


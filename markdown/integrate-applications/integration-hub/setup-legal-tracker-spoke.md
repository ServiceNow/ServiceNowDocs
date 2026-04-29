---
title: Set up the Legal Tracker spoke
description: Integrate a ServiceNow instance and the Legal Tracker spoke by using  Legal Tracker credentials to authenticate  ServiceNow  legal requests.Register Legal Tracker as an OAuth provider to enable the instance to request OAuth 2.0 tokens.Create and integrate the connection to your Legal Tracker account. The Legal Tracker spoke Connection &amp; Credential Aliases use these connections to perform actions in Legal Tracker.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Legal Tracker Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up the Legal Tracker spoke

Integrate a ServiceNow instance and the Legal Tracker spoke by using  Legal Tracker credentials to authenticate  ServiceNow  legal requests.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the Legal Tracker spoke.
-   Role required: admin.

## Register Legal Tracker as an OAuth provider

Register Legal Tracker as an OAuth provider to enable the instance to request OAuth 2.0 tokens.

### Before you begin

You must have the following setup to register Legal Tracker OAuth provider:

-   Integration Hub subscription
-   Legal Tracker access credentials
-   The Legal Tracker spoke must be activated

Role required: admin

### Procedure

1.  On your ServiceNow® instance, navigate to **All** &gt; **System OAuth** &gt; **Application Registry**.

2.  Select **New**.

3.  On the **What kind of OAuth application** page, select **Connect to a third-party OAuth Provider**.

4.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Unique name to identify the record, for example, Legal Tracker OAuth profile.|
    |Client ID|Application ID of the Legal Tracker application.|
    |Client Secret|The Client Secret that you generated when you created the application.|
    |Default Grant type|The value in this field should be **Password**.|
    |Token URL|The value in this field should be **https://api.thomsonreuters.com/auth/oauth2/token**. You might have to unlock the field to enter the value.|
    |Redirect URL|The value in this field should be **https://&lt;your-instance&gt;.service-now.com/oauth\_redirect.do**. You might have to unlock the field to enter the value.|

5.  Right-click in the form header and select **Save**.

    The system validates the OAuth credentials.


### Result

Legal Tracker is registered as an OAuth provider, which enables the instance to request OAuth 2.0 tokens.

### What to do next

[Integrate the Legal Tracker spoke with your ServiceNow instance](setup-legal-tracker-spoke.md#).

## Integrate the Legal Tracker spoke with your ServiceNow instance

Create and integrate the connection to your Legal Tracker account. The Legal Tracker spoke Connection &amp; Credential Aliases use these connections to perform actions in Legal Tracker.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **IntegrationHub** &gt; **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases**.

2.  Select **Legal Tracker**.

3.  Select the **Create New Connection &amp; Credential** related link.

4.  On the form, fill in the fields.

    |Field|Value required|
    |-----|--------------|
    |Connection Name|Name to identify the connection. This field is automatically set to the Legal Tracker spoke connection.|
    |Connection URL|The URL to make the connection to the spoke. This field is automatically set to **https://api.thomsonreuters.com**.|
    |Credential Name|Name to identify the credential record. By default, this value is **Legal Tracker Spoke Credential** but you may change it.|
    |OAuth Name|Name of the OAuth entity profile. This field is automatically set to Legal Tracker spoke Auth.|
    |OAuth Client ID|Client ID of the Legal Tracker application you registered in the registration portal.|
    |OAuth Client Secret|Client Secret generated when you registered the application in the Legal Tracker portal.|
    |OAuth Redirect URL|The redirect URL. The format of the URL is https://&lt;your-instance&gt;.service-now.com/oauth\_redirect.do.|

5.  Select **Create and Get OAuth Token**.


### Result

The Legal Tracker spoke is set up and integrated with your ServiceNow instance.


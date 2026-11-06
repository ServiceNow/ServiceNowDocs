---
title: Configure MFA Provider
description: Configure SMS and Email with the Provider to ensure every user can login securely.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/platform-security/authentication/configure-mfa-provider.html
release: australia
product: Authentication
classification: authentication
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Multi-factor authentication providers, SMS as an MFA factor, MFA factor policies, MFA verification methods, Configuring MFA, Multi-factor authentication, Authentication, Access Management]
---

# Configure MFA Provider

Configure SMS and Email with the Provider to ensure every user can login securely.

## Before you begin

Role required: adaptive\_auth\_admin

## Procedure

1.  Navigate to **All** &gt; **Multi-factor Authentication** &gt; **Providers**.

    Following provider configurations are available for MFA within the ServiceNow AI Platform:

    -   Email Provider Configuration
    -   Twilio Provider Configuration
    -   Infobip Provider Configuration.
    \[Omitted image "mfa-provider.png"\] Alt text: MFA Providers

2.  To create a new provider, select **New**.

3.  On the form, fill in the fields.

<table id="table_mxz_wyp_znb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the record.

</td></tr><tr><td>

Type

</td><td>

Description of the record.

</td></tr><tr><td>

Provider

</td><td>

The provider type, either **Twilio** or **Custom**.**Note:** To configure Twilio, see [Configure Notify with Twilio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/t_ConfigureNotifyWithTwilio.md).

 When choosing **Custom**, you need to specify the following fields:

-   Provider Configuration Table
-   Provider Configuration Record
-   Script
-   User table
-   User field


</td></tr><tr><td>

Message Template

</td><td>

The message template for the record.

</td></tr><tr><td>

Active

</td><td>

Option to make the provider configuration active.

</td></tr></tbody>
</table>4.  Select **Submit**.

    Based on the message template and provider configurations, the SMS or Email is sent to users as a factor for authentication during the login process.



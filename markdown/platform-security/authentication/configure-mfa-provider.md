---
title: Configure MFA Provider
description: Configure SMS and Email with the Provider to ensure every user can login securely.
locale: en-US
release: yokohama
product: Authentication
classification: authentication
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Multi-factor authentication Providers, Multi-factor authentication with SMS, MFA verification methods, Configure Multi-factor authentication, Multi-factor authentication, Authentication, Access Management]
---

# Configure MFA Provider

Configure SMS and Email with the Provider to ensure every user can login securely.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Multi-factor Authentication** &gt; **Providers**.

    Following provider configuration are available for MFA within the ServiceNow AI Platform:

    -   Email Provider Configuration
    -   Twilio Provider Configuration
    -   Infobip Provider Configuration.
    ![MFA Providers](../images/mfa-provider.png)

2.  To create a new provider, click **New**.

3.  On the form, fill the fields.

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

Choose **Twilio** or **Custom**.**Note:** To configure Twilio, see [Configure Notify with Twilio](https://www.servicenow.com/docs/access?context=t_ConfigureNotifyWithTwilio&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

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
</table>4.  Click **Submit**.

    Based on the message template and provider configurations, the SMS or Email is sent to users as a factor for authentication during the login process.



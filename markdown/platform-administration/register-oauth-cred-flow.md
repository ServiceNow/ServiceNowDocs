---
title: Register an OAuth Provider
description: Use the information generated during the Microsoft Azure account configuration to register an application as an OAuth provider.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Send email using client credential flow, Advanced email setup, Configure email administration, Email Administration, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Register an OAuth Provider

Use the information generated during the Microsoft Azure account configuration to register an application as an OAuth provider.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System OAuth** &gt; **Application Registry**.

2.  Select **New**.

3.  On the **What kind of OAuth application** screen, select **Connect to a third-party OAuth Provider**.

4.  On the form, fill in the fields.

<table id="table_alw_kq3_gfb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name to uniquely identify the record.

</td></tr><tr><td>

Client ID

</td><td>

Application ID of the application that you created in Microsoft Azure.

</td></tr><tr><td>

Client Secret

</td><td>

The client secret that you generated when you created the application in Microsoft Azure.**Note:** When using certificates, the **Client Secret** is a dummy value.

</td></tr><tr><td>

OAuth API Script

</td><td>

OAuth API script name. For more information see, [OAuth API Script](oauth-api-script.md). **Note:** This field is required only while using certificates.

</td></tr><tr><td>

Default Grant type

</td><td>

Client Credentials

</td></tr><tr><td>

Token URL

</td><td>

Token URL that you copied after configuring the Microsoft Azure account.

</td></tr><tr><td>

Redirect URL

</td><td>

`https://<instance>./oauth_redirect.do` **Note:** This URL should be the same as the URL in Microsoft Azure.

</td></tr></tbody>
</table>5.  Select and hold \(or right-click\) the form header and select **Save**.

    An OAuth Entity Profile record is created.

6.  In the OAuth Entity Scopes related list, add scopes to match the permissions that you defined when you configured the application.

7.  Select **Insert a new row**.

8.  Enter `smtp` as the name and `https://outlook.office365.com/.default` as the OAuth scope.

9.  Select and hold \(or right-click\) the form header and select **Save**.

10. In the OAuth Entity Profiles embedded list, select the profile created by default.

11. In the OAuth Entity Scopes embedded list, add a new row and select the **smtp** scope.

12. Select **Update**.


## What to do next

Use the OAuth profile to create an email account with SMTP OAuth2.0. For more information, see [Create an email account with SMTP OAuth2.0](create-email-account-smtp.md).

**Parent Topic:**[Send email using client credential flow](../concept/send-email-client-credential-flow.md)


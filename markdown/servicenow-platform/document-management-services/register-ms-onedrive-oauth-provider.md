---
title: Register Microsoft OneDrive as an OAuth provider for Document Services
description: Use the information generated during Microsoft OneDrive account configuration to register Microsoft OneDrive as an OAuth provider and allow the instance to request OAuth 2.0 tokens.
locale: en-US
release: zurich
product: Document Management Services
classification: document-management-services
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Microsoft OneDrive integration with Document Services, Integrate with Document Services, Multi Provider Document Services Framework, Document Services, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Register Microsoft OneDrive as an OAuth provider for Document Services

Use the information generated during Microsoft OneDrive account configuration to register Microsoft OneDrive as an OAuth provider and allow the instance to request OAuth 2.0 tokens.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System OAuth** &gt; **Application Registry**.

2.  Select **New**.

3.  On the screen titled **What kind of OAuth application**, select **Connect to a third-party OAuth Provider**.

4.  On the form, fill in the fields.

<table id="table_bxw_mkg_15b"><thead><tr><th>

Field

</th><th>

Value required

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name to uniquely identify the record.

</td></tr><tr><td>

Client ID

</td><td>

Application ID of the OneDrive application you created in Microsoft Azure.

</td></tr><tr><td>

Client Secret

</td><td>

The Client Secret you generated when you created the application in Microsoft Azure.

</td></tr><tr><td>

Default Grant type

</td><td>

This value should be **Authorization Code**.

</td></tr><tr><td>

Authorization URL

</td><td>

`https://login.microsoftonline.com/common/oauth2/v2.0/authorize`

 Note that you have to unlock this field and then lock it again.

</td></tr><tr><td>

Token URL

</td><td>

`https://login.microsoftonline.com/common/oauth2/v2.0/token`

 Note that you have to unlock this field and then lock it again.

</td></tr><tr><td>

Redirect URL

</td><td>

`https://<instance>.service-now.com/oauth_redirect.do`

 Note that you have to unlock this field and then lock it again.

</td></tr></tbody>
</table>5.  Right-click in the form header and select **Save**.

    An OAuth Entity Profile record is created.

6.  In the OAuth Entity Scopes related list, add scopes to match the permissions you defined when you configured the Microsoft OneDrive application.

    1.  Select **Insert a new row**.

    2.  Enter the name and the OAuth scope of the permission, which for these Document Services scopes are the same for both values.

        -   Files.Read
        -   Files.Read.All
        -   offline\_access
        -   Files.ReadWrite
        -   Files.ReadWrite.All
7.  Right-click in the form header and select **Save**.

8.  Select **Update**.


## Result

The system validates the OAuth credentials.

**Parent Topic:**[Microsoft OneDrive integration with Document Services](../concept/one-drive-integration.md)


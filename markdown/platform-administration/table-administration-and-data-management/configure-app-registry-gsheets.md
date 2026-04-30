---
title: Create an application registry for Google Sheets on a ServiceNow instance
description: Register the Google Drive application in your ServiceNow instance to enable OAuth authorization for exporting table records directly to Google Sheets.
locale: en-US
release: zurich
product: Table Administration and Data Management
classification: table-administration-and-data-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Exporting your table records to Google Sheets, Exporting data, Tables and data, Configure core features, Administer]
---

# Create an application registry for Google Sheets on a ServiceNow instance

Register the Google Drive application in your ServiceNow instance to enable OAuth authorization for exporting table records directly to Google Sheets.

## Before you begin

Role required: admin

## About this task

An Application Registry is a record that defines how your ServiceNow instance can connect to an external application, such as Google Sheets, using OAuth.

It includes the following information:

-   Client ID and Client Secret: Credentials for the external application.
-   Authorization and Token URLs: Web addresses used to log in and get access.
-   Redirect URL: Where the OAuth server sends the user after authorization.
-   Scopes and Profiles: Define what areas of ServiceNow the external application is allowed to access.

## Procedure

1.  Navigate to **All** &gt; **System OAuth** &gt; **Application Registry**.

2.  Select **New**.

3.  From the list of OAuth application types, select  **Connect to a third party OAuth Provider**.

4.  On the form, fill in the fields.

<table id="table_anc_b1w_gfc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name to uniquely identify the record. For example, Sheets Integration.

</td></tr><tr><td>

Client ID

</td><td>

Client ID of the Google Drive application that you registered in Google Workspace. You can find the Google Client ID in the downloaded OAuth credentials JSON file. For more information, see [Set up the OAuth application on the Google Sheets API](set-up-oauth-app-gsheets-api.md).

</td></tr><tr><td>

Client Secret

</td><td>

Client secret that was generated when you registered the app in Google API Console.You can find the Google client secret in the downloaded OAuth credentials JSON file. For more information, see [Set up the OAuth application on the Google Sheets API](set-up-oauth-app-gsheets-api.md).

</td></tr><tr><td>

OAuth API Script

</td><td>

Script to customize the request and response. For example, OAuthGoogleSheetExport.

</td></tr><tr><td>

Default Grant Type

</td><td>

Grant type that was used to establish the token.

</td></tr><tr><td>

Authorization URL

</td><td>

URL that the OAuth application at Google provides to seek authorization to access the Google resource server. The URL format that you enter includes the tenant ID of your app: `https://accounts.google.com/oauth2/v2.0/{API version}/authorize`.You can find the Authorization URL in the downloaded OAuth credentials JSON file. For more information, see [Set up the OAuth application on the Google Sheets API](set-up-oauth-app-gsheets-api.md).

</td></tr><tr><td>

Token URL

</td><td>

URL to obtain the access token. The format that you enter for the URL is `{yourgoogleaccount}.com/oauth2/{API version}/token`.

</td></tr><tr><td>

Redirect URL

</td><td>

Redirect URL that includes the instance URL with the format `https://<your-instance>.service-now.com/oauth_redirect.do`.Update the &lt;instanceURL&gt; value with your instance URL.

</td></tr><tr><td>

Token Revocation URL

</td><td>

URL that is provided by the OAuth authorization server that enables a client application to request the revocation or cancellation of access tokens and refresh tokens that were previously issued. The format is https://\{yourgoogleaccount\}.com/\{API version\}/oauth2/revoke

</td></tr></tbody>
</table>5.  Select **Submit**.

6.  On the Application Registries page, search and select the application registry that you created.

7.  In the OAuth Entity Scopes related list, enter `https://www.googleapis.com/auth/drive.file` in the **Name** and **OAuth scope** fields.

    ![OAuth Entity Scopes related list displays the Name and OAuth scope fields to define the OAuth scope for this OAuth provider.](../image/oauth-entity-scopes.png)

8.  In the OAuth Entity Profiles related list, select **Sheets Integration default\_profile**.

9.  In the OAuth Entity Profile Scopes related list, enter `https://www.googleapis.com/auth/drive.file` in the **OAuth Entity Scope** field.

    ![OAuth Entity Profile Scopes related list displays the OAuth Entity scope field to define the OAuth scope that is associated with this profile.](../image/oauth-profile-scope.png)

10. Select **Update**.


**Parent Topic:**[Exporting your table records to Google Sheets](../concept/setup-gsheet-export.md)


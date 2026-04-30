---
title: Register Microsoft Exchange Online as the OAuth provider
description: Register Microsoft Exchange Online as the OAuth provider so that your Walk-up Experience instance can request OAuth 2.0 tokens.
locale: en-US
release: xanadu
product: Walk-Up Experience
classification: walk-up-experience
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Set up Microsoft Office 365 integration for Walk-up Experience, Integrate Microsoft Office 365 calendar with Walk-up Experience, Configure, Walk-up Experience, IT Service Management]
---

# Register Microsoft Exchange Online as the OAuth provider

Register Microsoft Exchange Online as the OAuth provider so that your Walk-up Experience instance can request OAuth 2.0 tokens.

## Before you begin

Role required: admin

## About this task

Use the information generated during the registration of the application in the Microsoft Azure portal.

## Procedure

1.  Navigate to **All** &gt; **System OAuth** &gt; **Application Registry**.

2.  Open the record **Microsoft Exchange Online**.

3.  On the form, fill in the fields.

<table id="table_rn5_5md_qnb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name to identify the record. For example, `Microsoft Exchange Online`.

</td></tr><tr><td>

Client ID

</td><td>

Application ID created during application registration.

</td></tr><tr><td>

Client Secret

</td><td>

Client secret created during application registration.

</td></tr><tr><td>

OAuth API Script

</td><td>

Optional script to customize the request and response.

</td></tr><tr><td>

Logo URL

</td><td>

URL that contains an image to use as the application logo.

</td></tr><tr><td>

Default Grant Type

</td><td>

Grant type used to establish the token. Select **Authorization Code**.

</td></tr><tr><td>

Refresh Token Lifespan

</td><td>

Time, in seconds, that the refresh token is valid. The default time is 8,640,0000 seconds.

</td></tr><tr><td>

PKCE required

</td><td>

Option to enable public clients to require PKCE for an authorization.**Note:** You can use only **Authorization Code** as the **Default Grant type** when **PKCE** is enabled.

</td></tr><tr><td>

Application

</td><td>

Application scope that contains this record.

</td></tr><tr><td>

Accessible from

</td><td>

Application scope that this registry is accessible from.

</td></tr><tr><td>

Active

</td><td>

Option to use the application registry.

</td></tr><tr><td>

Authorization URL

</td><td>

OAuth authorization code endpoint. Enter `https://login.microsoftonline.com/<Directory-ID>/oauth2/v2.0/authorize`

</td></tr><tr><td>

Token URL

</td><td>

OAuth server token endpoint. Enter `https://login.microsoftonline.com/<Directory-ID>/oauth2/v2.0/token`

</td></tr><tr><td>

Token Revocation URL

</td><td>

OAuth server token revocation endpoint.

</td></tr><tr><td>

Redirect URL

</td><td>

OAuth callback endpoint. Enter `https://<instance-name>.service-now.com/oauth_redirect.do`

</td></tr><tr><td>

Use mutual authentication

</td><td>

Option to use mutual authentication for token request and revocation. This option requires a mutual authentication profile to be specified.

</td></tr><tr><td>

Send Credentials

</td><td>

Client credentials in the request.

</td></tr></tbody>
</table>4.  Select and hold \(or right-click\) the form header, and click **Save**.

    A system-generated OAuth entity profile is created and displayed in the OAuth Entity Profiles related list. For example, `Microsoft Exchange Online default_profile`.

5.  Navigate to **System OAuth** &gt; **Application Registry**.

6.  Open the record **Microsoft Exchange Online\_clientCredentials**.

7.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Client ID|Application ID created during application registration.|
    |Client Secret|Client secret created during application registration.|
    |Default Grant Type|Grant type used to establish the token. Select **Client Credentials**.|
    |Token URL|OAuth server token endpoint. Enter `https://login.microsoftonline.com/<Directory-ID>/oauth2/v2.0/token`|
    |Redirect URL|OAuth callback endpoint. Enter `https://<instance-name>.service-now.com/oauth_redirect.do`|

8.  Right-click the form header, and click **Save**.

    A system-generated OAuth entity profile is created and displayed in the OAuth Entity Profiles related list. For example, `Microsoft Exchange Online_clientCredentials default_profile`.


**Parent Topic:**[Set up Microsoft Office 365 integration for Walk-up Experience](setup-walkup-msoffice365-cal-integ.md)


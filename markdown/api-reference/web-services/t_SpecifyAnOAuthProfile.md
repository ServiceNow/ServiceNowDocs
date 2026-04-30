---
title: Specify an OAuth profile
description: An OAuth profile includes the grant type that the third-party OAuth provider needs to obtain access to the restricted resource.
locale: en-US
release: yokohama
product: Web Services
classification: web-services
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [OAuth profiles and scopes, Use a third-party OAuth provider, Configure a REST message with OAuth, Outbound REST authentication, Outbound REST web service, Outbound web services, Web services, API implementation, API implementation and reference]
---

# Specify an OAuth profile

An OAuth profile includes the grant type that the third-party OAuth provider needs to obtain access to the restricted resource.

## Before you begin

Role required: admin

## About this task

## Procedure

1.  Open a third-party OAuth provider record.

2.  In the OAuth Entity Profiles embedded list, click **Insert a new row** and then enter a name for the profile.

3.  Right-click the Application Registry form header and select **Save**.

    The system creates the profile record.

4.  Click the name of the profile you created and then fill in the form fields.

    ![OAuth entity profile](../image/OAuthEntityProfile.png)

<table id="table_khq_dxq_rs"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Enter a descriptive name.

</td></tr><tr><td>

OAuth provider

</td><td>

Verify the provider that is associated with the profile.

</td></tr><tr><td>

Grant type

</td><td>

Select the grant type:-   **Authorization code**: The code that is granted to the client to obtain an access token, which is then used to obtain access to the resource. If you select this option, then you need an authorization URL \(the URL of the authorization server\).
-   **Resource owner password credentials**: The user name and password of the user that is trying to obtain access to the resource.
-   **Client Credentials**: The client ID and client secret, which are both used to get the access token. This method does not provide refresh tokens.
-   **JWT Bearer**: An authorization server validates a JWT token which enables identity and security information to be shared across security domains.
-   **SAML2 Bearer**: Generates the SAML2 assertion and then exchanges the assertion for the access tokens wit the provider.

**Note:** For outbound request to SuccessFactors use the **SAML2 Bearer** as the Default Grant Type.

</td></tr><tr><td>

Is default

</td><td>

Select this option to make the profile the default option for the associated provider.

</td></tr><tr><td class="sub-head" colspan="2">

Embedded list

</td></tr><tr><td>

OAuth Entity Profile Scopes

</td><td>

[Specify the OAuth entity scope](t_SpecifyAnOAuthScope.md).

</td></tr></tbody>
</table>5.  Click **Update**.


**Parent Topic:**[OAuth profiles and scopes](../concept/c_OAuthProviderAndScope.md)


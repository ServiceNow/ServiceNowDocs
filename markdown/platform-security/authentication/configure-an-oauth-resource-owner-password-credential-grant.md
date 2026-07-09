---
title: Configure an OAuth resource owner password credential grant
description: Configuring an OAuth resource owner password credential \(ROPC\) grant enables applications to authenticate users by directly using their credentials to obtain an access token. This method is ideal for trusted applications and legacy systems that require authentication without browser-based flows, enabling secure token validation and controlled API access.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-security/authentication/configure-an-oauth-resource-owner-password-credential-grant.html
release: zurich
product: Authentication
classification: authentication
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [ROPC Grant, Inbound Integrations, OAuth inbound, OAuth authentication, Access Management]
---

# Configure an OAuth resource owner password credential grant

Configuring an OAuth resource owner password credential \(ROPC\) grant enables applications to authenticate users by directly using their credentials to obtain an access token. This method is ideal for trusted applications and legacy systems that require authentication without browser-based flows, enabling secure token validation and controlled API access.

## Before you begin

Role required: `admin`

## Procedure

1.  Navigate to **Machine Identity Console** &gt; **Inbound integrations** &gt; **New integration** &gt; **OAuth - Resource owner password credential grant**.

2.  Update the text fields in the **Details** form with the appropriate information.

    |Field|Description|
    |-----|-----------|
    |**Name**|The name provided by the resource owner \(user\) during authentication.|
    |**Provider name**|Enter the name of the service provider that you want to integrate with. Example: Microsoft, Google, Zoom, SAP, and so on|
    |**Client ID**|The unique ID assigned to identify the application.|
    |**Client secret**|The secret key that only the application and the authorization server can identify. The application uses this key to authenticate and obtain access tokens.|
    |**Comments**|Add any notes about this configuration.|
    |**Active**|Select the check box to make the OAuth application active.|

3.  Perform the following steps to add auth scope to the configuration:

    1.  Select **Create auth scope** if you want to define a new scope.

    2.  Select a scope from the **Auth scope** drop-down.

4.  Select **Allow access only to APIs in selected scope** in the Scope validation settings to restricts access to listed scopes only.

    **Note:** You can choose not to select **Set Allow access only to APIs in selected scope** for broader access permitted by user controls and API policies.

5.  Update the text fields in the **Advanced options \(optional\)** form with the appropriate information.

    Enforcing token restriction applies limitations on how an OAuth access token can be used, enhancing security by verifying that tokens are valid only under specific conditions. Enable the Enforce token restriction check box to limit OAuth access tokens to specific APIs defined in the API access policy. If the Enforce token restriction is turned off, the token can be used across other REST API.

<table id="table_qdq_bw2_s2c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**Enforce token restriction**

</td><td>

The Enforce token restriction option limits the client to accessing only the APIs specified in the REST API Access Policies. If you unselect it, the client can access other REST APIs based on the user ACL permissions.

</td></tr><tr><td>

**Token Format**

</td><td>

Format of token to generate. Options: -   JWT
-   Opaque
**Note:**

-   The jwks url is available in the location: `api/now/oauth/jwks`.
-   The rotated \(inactive keys\) from jwks response is removed after 105 days default.


</td></tr><tr><td>

**Access token lifespan**

</td><td>

Duration \(in seconds\) for which the OAuth access token remains valid before it expires.**Note:** The default value is 1800 seconds.

</td></tr><tr><td>

**Refresh token lifespan**

</td><td>

Duration \(in seconds\) for which the OAuth refresh token remains valid before it expires.**Note:** The default value is 8,640,000 seconds.

</td></tr></tbody>
</table>6.  Select **Save**.

    A new OAuth resource owner password credential grant is created.



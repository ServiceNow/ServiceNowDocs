---
title: Configure an OAuth authorization code grant
description: Configure the OAuth authorization code grant to enable secure and interactive user authentication to enable applications to access resources on behalf of users. The OAuth authorization code grant verifies that the API access is granted based on the user identity and permissions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-security/authentication/configure-an-oauth-authorization-code-grant.html
release: zurich
product: Authentication
classification: authentication
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Auth Code Grant, Inbound Integrations, OAuth inbound, OAuth authentication, Access Management]
---

# Configure an OAuth authorization code grant

Configure the OAuth authorization code grant to enable secure and interactive user authentication to enable applications to access resources on behalf of users. The OAuth authorization code grant verifies that the API access is granted based on the user identity and permissions.

## Before you begin

Role required: `admin`

## Procedure

1.  Navigate to **Machine Identity Console** &gt; **Inbound integrations** &gt; **New integration** &gt; **OAuth - Authorization code grant**.

2.  Update the text fields in the Details form with the appropriate information.

<table id="table_nwn_z3x_r2c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**Name of OAuth entity**

</td><td>

Name of the OAuth entity.

</td></tr><tr><td>

**Provider name**

</td><td>

Enter the name of the service provider you want to integrate with. Example: Microsoft, Google, Zoom, SAP, etc.**Note:** Provider name is a mandatory field.

</td></tr><tr><td>

**Redirect URL**

</td><td>

URL to which the authorization code should be sent after authentication.

</td></tr><tr><td>

**Client ID**

</td><td>

Unique ID assigned to identify the application.

</td></tr><tr><td>

**Client Secret**

</td><td>

The secret key that only the application and the authorization server can identify. The application uses this key to authenticate and obtain access tokens.

</td></tr><tr><td>

**Comments**

</td><td>

Add any notes about this configuration.

</td></tr><tr><td>

**Active**

</td><td>

Select to use for authentication and authorization requests; when unselected, the record is saved but remains inactive and will not process any requests.

</td></tr><tr><td>

**This is a public client check box**

</td><td>

Select the if the application can’t securely store credentials, and doesn’t require a secret key to prove its identity during authorization. The client secret information is processed for public clients.

</td></tr></tbody>
</table>3.  Perform the following steps to add auth scope to the configuration:

    1.  Select **Create auth scope** if you want to define a new scope.

    2.  Select a scope from the **Auth scope** drop-down.

    3.  Enter API names in **Limit authorization to the following APIs** to narrow access.

    4.  Use **+ Add another row** to assign additional scopes to your configuration.

4.  Select **Allow access only to APIs in selected scope** in the Scope validation settings to restricts access to listed scopes only.

    **Note:** You can choose not to select **Set Allow access only to APIs in selected scope** for broader access permitted by user controls and API policies.

5.  Update the text fields in the Advanced options \(optional\) form with the appropriate information.

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

</td></tr><tr><td>

**Login URL**

</td><td>

HTTP redirection endpoint to authenticate with the authorization server.

</td></tr><tr><td>

**Logo URL**

</td><td>

Web address of an image that represents the application during the authentication and authorization process. It’s displayed on the authorization server's consent screen to help you recognize the requesting application.

</td></tr></tbody>
</table>    Enforcing token restriction applies limitations on how an OAuth access token can be used, enhancing security by verifying that tokens are valid only under specific conditions. Enable the **Enforce token restriction** check box to limit OAuth access tokens to specific APIs defined in the API access policy. If the Enforce token restriction is turned off, the token can be used across other REST APIs.

6.  Select **Save**.

    A new OAuth authorization code grant is created.



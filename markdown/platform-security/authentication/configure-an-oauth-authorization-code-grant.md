---
title: Configure an OAuth authorization code grant
description: Configure the OAuth authorization code grant to enable secure and interactive user authentication to enable applications to access resources on behalf of users. The OAuth authorization code grant verifies that the API access is granted based on the user identity and permissions.
locale: en-US
release: zurich
product: Authentication
classification: authentication
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Authorization Code Grant, Inbound integrations, OAuth inbound, OAuth authentication, Authentication, Access Management]
---

# Configure an OAuth authorization code grant

Configure the OAuth authorization code grant to enable secure and interactive user authentication to enable applications to access resources on behalf of users. The OAuth authorization code grant verifies that the API access is granted based on the user identity and permissions.

## Before you begin

Role required: `oauth_admin, mi_admin, admin`

## Procedure

1.  Navigate to **Machine Identity Console** &gt; **Inbound integrations** &gt; **New integration** &gt; **** &gt; **OAuth authorization code grant**.

    The New Record page appears.

2.  Update the text fields in the Details form with the appropriate information.

    |Field|Description|
    |-----|-----------|
    |**Name of OAuth entity**|Name of the OAuth entity.|
    |**Provider name**|Enter the name of the service provider you want to integrate with. Example: Microsoft, Google, Zoom, SAP, etc|
    |**Redirect URL**|URL to which the authorization code should be sent after authentication.|
    |**Client ID**|Unique ID assigned to identify the application.|
    |**Client Secret**|The secret key that only the application and the authorization server can identify. The application uses this key to authenticate and obtain access tokens.|

    Select the **This is a public client check box** if the application can’t securely store credentials, and doesn’t require a secret key to prove its identity during authorization. The client secret information is processed for public clients.

3.  Update the text fields in the **Auth scope** form with the appropriate information. The authentication scope defines the level of access an application has to a resource. Select the authentication scope for the specific REST APIs you want to access.

    |Field|Description|
    |-----|-----------|
    |**Auth scope**|The level of access an application has to a resource. The authentication scope restricts the actions that an access token can perform on APIs or data.|
    |**Limit authorization**|The names of the APIs for which you want to restrict authorization.|
    |**Allow access only to APIs in selected scope**|Enable the option for the integration to only access APIs that are explicitly listed in the selected scopes.|

4.  Update the text fields in the Advanced options \(optional\) form with the appropriate information.

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
-   The rotated \(inactive keys\) from jwks response after is removed after 105 days default.


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

5.  Select **Create new auth scope** to add a new auth scope.

6.  Select **Save**.

    A new OAuth authorization code grant is created.

7.  Go to **All** &gt; **Inbound integrations** &gt; **Application Registries** to view the newly created OAuth authorization code grant.



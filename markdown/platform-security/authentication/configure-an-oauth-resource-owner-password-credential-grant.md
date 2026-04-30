---
title: Configure an OAuth resource owner password credential grant
description: Configuring an OAuth resource owner password credential \(ROPC\) grant enables applications to authenticate users by directly using their credentials to obtain an access token. This method is ideal for trusted applications and legacy systems that require authentication without browser-based flows, enabling secure token validation and controlled API access.
locale: en-US
release: zurich
product: Authentication
classification: authentication
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [ROPC Grant, Inbound integrations, OAuth inbound, OAuth authentication, Authentication, Access Management]
---

# Configure an OAuth resource owner password credential grant

Configuring an OAuth resource owner password credential \(ROPC\) grant enables applications to authenticate users by directly using their credentials to obtain an access token. This method is ideal for trusted applications and legacy systems that require authentication without browser-based flows, enabling secure token validation and controlled API access.

## Before you begin

Role required: `oauth_admin, mi_admin, admin`

## Procedure

1.  Navigate to **Machine Identity Console** &gt; **** &gt; **Inbound integrations** &gt; **** &gt; **New integration** &gt; **OAuth Resource owner password credential grant**.

2.  Update the text fields in the **Details** form with the appropriate information.

    |Field|Description|
    |-----|-----------|
    |**Name**|The name provided by the resource owner \(user\) during authentication.|
    |**Provider name**|Enter the name of the service provider that you want to integrate with. Example: Microsoft, Google, Zoom, SAP, and so on|
    |**Client ID**|The unique ID assigned to identify the application.|
    |**Client secret**|The secret key that only the application and the authorization server can identify. The application uses this key to authenticate and obtain access tokens.|
    |**Active**|Select the check box to make the OAuth application active.|

3.  Update the text fields in the **Advanced options \(optional\)** form with the appropriate information.

    Enforcing token restriction applies limitations on how an OAuth access token can be used, enhancing security by verifying that tokens are valid only under specific conditions. Enable the Enforce token restriction check box to limit OAuth access tokens to specific APIs defined in the API access policy. If the Enforce token restriction is turned off, the token can be used across other REST API.

    |Field|Description|
    |-----|-----------|
    |**Access token lifespan**|The duration \(in seconds\) for which the access token remains valid before it expires.|
    |**Refresh token lifespan**|The duration \(in seconds\) that a refresh token remains valid after it’s issued is specified in the Lifespan field.|

4.  Update the text fields in the Auth scope \(optional\) form with the appropriate information. The authentication scope defines the level of access an application has to a resource. Select the authentication scope for the specific REST APIs you want to access.

    **Note:** When you select an **Auth scope**, all the associated APIs are automatically populated in the **Limit authorization** text box.

    |Field|Description|
    |-----|-----------|
    |**Auth scope**|Access level of an application. The authentication scope restricts the actions that an access token can perform on APIs or data.|
    |**Limit authorization**|Names of the APIs for which you want to restrict authorization.|
    |**Allow access only to APIs in selected scope**|Enable the option for the integration to only access APIs that are explicitly listed in the selected scopes.|

    **Note:** Adding or editing APIs from the **Auth scope** menu affects all OAuth entities that are associated with the same authorization scope.

    1.  Select **Create new auth scope** to add a new auth scope.

5.  Update the text fields in the **Advanced options \(optional\)** form with the appropriate information.

    Enforcing token restriction applies limitations on how an OAuth access token can be used, enhancing security by verifying tokens are valid only under specific conditions. Enable the Enforce token restriction check box to limit OAuth access tokens to specific APIs defined in the API access policy. If Enforce token restriction is turned off, the token can be used across other REST API.

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

</td></tr></tbody>
</table>6.  Select **Add another row** to create another Auth scope with the associated APIs.

7.  Select **Save**.

    A new OAuth resource owner password credential grant is created.

8.  Go to **All** &gt; **Inbound integrations** &gt; **Application Registries** to view the newly created OAuth Resource owner password credential grant.



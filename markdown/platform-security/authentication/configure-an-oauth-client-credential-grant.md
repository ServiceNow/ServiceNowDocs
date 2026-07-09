---
title: Configure an OAuth Client credential grant
description: Configure the OAuth Client Credentials Grant for secure machine-to-machine authentication without user interaction. It authenticates applications using client credentials and grants-controlled API access with scoped permissions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/authentication/configure-an-oauth-client-credential-grant.html
release: australia
product: Authentication
classification: authentication
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Client Credentials Grant, Inbound Integrations, OAuth Inbound, OAuth authentication, Authentication, Access Management]
---

# Configure an OAuth Client credential grant

Configure the OAuth Client Credentials Grant for secure machine-to-machine authentication without user interaction. It authenticates applications using client credentials and grants-controlled API access with scoped permissions.

## Before you begin

Role required: `oauth_admin, mi_admin, admin`

## Procedure

1.  Navigate to **Machine Identity Console** &gt; **Inbound integrations** &gt; **New integration** &gt; **OAuth - Client credential grant**.

2.  Update the text fields in the Details form with the appropriate information.

<table id="table_crc_qms_s2c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**Name**

</td><td>

The name of the OAuth entity.

</td></tr><tr><td>

**Provider name**

</td><td>

Enter the name of the service provider you want to integrate with. Example: Microsoft, Google, Zoom, SAP, etc.**Note:** Provider name is a mandatory field.

</td></tr><tr><td>

**Client ID**

</td><td>

The unique ID assigned to identify the application.

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

</td></tr></tbody>
</table>6.  Select **Save**.

    A new OAuth Client credential grant is created.



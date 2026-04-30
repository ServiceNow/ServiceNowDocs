---
title: Configure an OAuth Client credential grant
description: Configure the OAuth Client Credentials Grant for secure machine-to-machine authentication without user interaction. It authenticates applications using client credentials and grants-controlled API access with scoped permissions.
locale: en-US
release: zurich
product: Authentication
classification: authentication
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Client Credentials Grant, Inbound integrations, OAuth inbound, OAuth authentication, Authentication, Access Management]
---

# Configure an OAuth Client credential grant

Configure the OAuth Client Credentials Grant for secure machine-to-machine authentication without user interaction. It authenticates applications using client credentials and grants-controlled API access with scoped permissions.

## Before you begin

Role required: `oauth_admin, mi_admin, admin`

## Procedure

1.  Navigate to **Machine Identity Console** &gt; **** &gt; **Inbound integrations** &gt; **** &gt; **New integration** &gt; **OAuth Client credential grant**.

    The OAuth Client credential configuration page appears.

2.  Update the text fields in the Details form with the appropriate information.

    |Field|Description|
    |-----|-----------|
    |**Name**|The name of the OAuth entity.|
    |**Provider name**|Enter the name of the service provider you want to integrate with. Example: Microsoft, Google, Zoom, SAP, etc|
    |**Client ID**|The unique ID assigned to identify the application.|
    |**Client Secret**|The secret key that only the application and the authorization server can identify. The application uses this key to authenticate and obtain access tokens.|

    Select the **Active** check box.

3.  Update the text fields in the Advanced options \(optional\) form with the appropriate information.

4.  Update the text fields in the **Auth scope \(optional\)** form with the appropriate information.

    The authentication scope defines the level of access an application has to a resource. Select the authentication scope for the specific REST APIs you want to access.

    |Field|Description|
    |-----|-----------|
    |**Auth scope**|The level of access an application has to a resource. The authentication scope restricts the actions that an access token can perform on APIs or data.|
    |**Limit authorization**|The names of the APIs for which you want to restrict authorization.|
    |**Allow access only to APIs in selected scope**|Enable the option for the integration to only access APIs that are explicitly listed in the selected scopes.|

    1.  Select **Create new auth scope** to add a new auth scope.

5.  Update the text fields in the Advanced options \(optional\) form with the appropriate information.

<table id="table_qdq_bw2_s2c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Enforce token restriction

</td><td>

The Enforce token restriction option limits the client to accessing only the APIs specified in the REST API Access Policies. If you unselect it, the client can access other REST APIs based on the user ACL permissions.

</td></tr><tr><td>

Token Format

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

</td></tr></tbody>
</table>6.  Select **Save**.

    A new OAuth Client credential grant is created.

7.  Go to **All** &gt; **Inbound integrations** &gt; **Application Registries** to view the newly created client credential grant.



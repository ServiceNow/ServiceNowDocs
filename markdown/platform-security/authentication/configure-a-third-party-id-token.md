---
title: Configure a third party ID token
description: Configure a third-party ID token to enable secure authentication by verifying user identities through an external IdP. The third-party ID token improves security by reducing stored credentials, confirms seamless authentication, and supports interoperability with industry standards like OpenID Connect \(OIDC\).
locale: en-US
release: zurich
product: Authentication
classification: authentication
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Third Party Token Grant, Inbound integrations, OAuth inbound, OAuth authentication, Authentication, Access Management]
---

# Configure a third party ID token

Configure a third-party ID token to enable secure authentication by verifying user identities through an external IdP. The third-party ID token improves security by reducing stored credentials, confirms seamless authentication, and supports interoperability with industry standards like OpenID Connect \(OIDC\).

## Before you begin

Role required: `oauth_admin, mi_admin, admin`

## Procedure

1.  Navigate to **Machine Identity Console** &gt; **** &gt; **Inbound integrations** &gt; **New integration** &gt; **Third party ID token**.

2.  Update the text fields in the **Details** form with the appropriate information.

    |Field|Description|
    |-----|-----------|
    |**Name**|The name provided by the resource owner \(user\) during authentication.|
    |**Provider name**|Enter the name of the service provider you want to integrate with. Example: Microsoft, Google, Zoom, SAP, etc|
    |**Client ID**|The unique ID assigned to identify the application.|
    |**Client secret**|The secret key that only the application and the authorization server can identify. The application uses this key to authenticate and obtain access tokens.|

    Enforcing token restriction applies limitations on how an OAuth access token can be used, enhancing security by verifying tokens are valid only under specific conditions. Enable the **Enforce token restriction** check box to limit OAuth access tokens to specific APIs defined in the API access policy. If **Enforce token restriction** is turned off, the token can be used across other REST APIs.

3.  Update the text fields in the **Auth scope \(optional\)** form with the appropriate information. The authentication scope defines the level of access an application has to a resource. Select the authentication scope for the specific REST APIs you want to access.

    |Field|Description|
    |-----|-----------|
    |**Auth scope**|The level of access an application has to a resource. The authentication scope restricts the actions that an access token can perform on APIs or data.|
    |**Limit authorization**|The names of the APIs for which you want to restrict authorization.|
    |**Allow access only to APIs in selected scope**|Enable the option for the integration to only access APIs that are explicitly listed in the selected scopes.|

    1.  Select **Create new auth scope** to add a new auth scope.

4.  Update the text fields in the **Advanced options \(optional\)** form with the appropriate information.

<table id="table_qdq_bw2_s2c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**Access token lifespan**

</td><td>

The duration \(in seconds\) for which the OAuth access token remains valid before it expires.**Note:** The default value is 1800 seconds.

</td></tr><tr><td>

**Refresh token lifespan**

</td><td>

The duration \(in seconds\) for which the OAuth refresh token remains valid before it expires.**Note:** The default value is 8,640,000 seconds.

</td></tr></tbody>
</table>5.  Select **Save**.

    A new third-party ID token is created.

6.  Go to **All** &gt; **Inbound integrations** &gt; **Application Registries** to view the newly created third party ID token.



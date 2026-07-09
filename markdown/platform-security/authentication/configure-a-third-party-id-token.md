---
title: Configure a third party ID token
description: Configure a third-party ID token to enable secure authentication by verifying user identities through an external IdP. The third-party ID token improves security by reducing stored credentials, confirms seamless authentication, and supports interoperability with industry standards like OpenID Connect \(OIDC\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-security/authentication/configure-a-third-party-id-token.html
release: zurich
product: Authentication
classification: authentication
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Third Party Token Grant, Inbound Integrations, OAuth inbound, OAuth authentication, Access Management]
---

# Configure a third party ID token

Configure a third-party ID token to enable secure authentication by verifying user identities through an external IdP. The third-party ID token improves security by reducing stored credentials, confirms seamless authentication, and supports interoperability with industry standards like OpenID Connect \(OIDC\).

## Before you begin

Role required: `admin`

## Procedure

1.  Navigate to **Machine Identity Console** &gt; **Inbound integrations** &gt; **New integration** &gt; **Third party ID token issued by OIDC supporting identity provider**.

2.  Update the text fields in the **Details** form with the appropriate information.

<table id="table_nwn_z3x_r2c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**Name**

</td><td>

The name provided by the resource owner \(user\) during authentication.

</td></tr><tr><td>

**Provider name**

</td><td>

Enter the name of the service provider you want to integrate with. Example: Microsoft, Google, Zoom, SAP, etc.**Note:** Provider name is a mandatory field.

</td></tr><tr><td>

**Client ID**

</td><td>

The unique ID assigned to identify the application. Unique ID is the Audience value.

</td></tr><tr><td>

**Comments**

</td><td>

Add any notes about this configuration.

</td></tr><tr><td>

**Active**

</td><td>

Select to use for authentication and authorization requests; when unselected, the record is saved but remains inactive and will not process any requests.

</td></tr></tbody>
</table>3.  Choose one of the two options from the OAuth OIDC provider configuration:

    1.  Use **Select an existing configuration** when an OIDC provider configuration already exists and provide the following details:

        |Field|Description|
        |-----|-----------|
        |**OIDC provider** \(required\)|Use the drop-down list to select the saved OIDC provider configuration.|
        |**OIDC provider name** \(auto-filled, read-only\)|Displays the name of the configuration selected in the drop-down.|
        |**OIDC metadata URL** \(auto-filled, read-only\)|The provider's well-known discovery endpoint, which exposes the signing keys and endpoints used to validate tokens. Example: `https://login.microsoftonline.com/common/.wellknown/openid-configuration`|
        |**OIDC configuration cache lifespan \(hours\)** \(auto-filled, read-only\)|How long, in hours, the system caches the provider's metadata before refetching it.|
        |**User claim** \(read-only\)|The token claim used to identify the user. Example: The claim whose value maps to a user record.|
        |**User field** \(read-only\)|The local user-record field that the user claim is matched against. Determines how an incoming token is mapped to an existing user. Example: `Email`.|
        |**Enable JTI verification**|When enabled, the system checks the token's JTI \(JWT unique ID\) to prevent token replay.|

        **Note:** Because these values are inherited, the metadata URL, cache lifespan, user claim/field, and JTI settings can't be edited directly here. Use the pencil icon option to modify the source configuration.

    2.  Use **Create a new configuration** when you want to define a new OIDC provider configuration and provide the following details:

<table id="table_cdd_hwg_pjk"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**New OAuth OIDC provider Configuration Name** \(required\)

</td><td>

A unique name for the configuration you're creating.

</td></tr><tr><td>

**OIDC metadata UR**L \(required\)

</td><td>

The provider's well-known discovery endpoint, which exposes the signing keys and endpoints used to validate tokens. Example: `https://login.microsoftonline.com/common/.wellknown/openid-configuration`

</td></tr><tr><td>

**OIDC configuration cache lifespan \(hours\)** \(required\)

</td><td>

How long, in hours, the system caches the provider's metadata before refetching it.

</td></tr><tr><td>

**User claim** \(optional\)

</td><td>

The token claim used to identify the user. Example: The claim whose value maps to a user record. `User claim` default is `sub`

</td></tr><tr><td>

**User field** \(optional\)

</td><td>

The local user-record field that the user claim is matched against. Determines how an incoming token is mapped to an existing user. Example: `Email`.

</td></tr><tr><td>

**Enable JTI verification**

</td><td>

When enabled, the system checks the token's JTI \(JWT unique ID\) to prevent token replay.

</td></tr><tr><td>

**JTI claim**

</td><td>

The name of the token claim that carries the JTI value the system should validate. Defaults to the standard `jti` claim. Example: `jti`**Note:** Appears when JTI verification is enabled.

</td></tr></tbody>
</table>4.  Perform the following steps to add auth scope to the configuration:

    1.  Select **Create auth scope** if you want to define a new scope.

    2.  Select a scope from the **Auth scope** drop-down.

    3.  Enter API names in **Limit authorization to the following APIs** to narrow access.

    4.  Use **+ Add another row** to assign additional scopes to your configuration.

5.  Select **Allow access only to APIs in selected scope** in the Scope validation settings to restricts access to listed scopes only.

    **Note:** You can choose not to select **Set Allow access only to APIs in selected scope** for broader access permitted by user controls and API policies.

6.  Select **Save** to create the configuration.



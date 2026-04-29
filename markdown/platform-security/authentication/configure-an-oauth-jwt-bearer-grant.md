---
title: Configure an OAuth JSON web token bearer grant
description: Configuring an OAuth JSON Web Token \(JWT\) bearer grant secures token-based authentication without user interaction. It enhances security with signed JWTs and reduces authentication overhead by eliminating repeated login attempts.
locale: en-US
release: australia
product: Authentication
classification: authentication
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [JWT Grant, Inbound integrations, OAuth Inbound, OAuth authentication, Authentication, Access Management]
---

# Configure an OAuth JSON web token bearer grant

Configuring an OAuth JSON Web Token \(JWT\) bearer grant secures token-based authentication without user interaction. It enhances security with signed JWTs and reduces authentication overhead by eliminating repeated login attempts.

## Before you begin

Role required: `oauth_admin, mi_admin, admin`

The supported algorithms for JSON Web Token \(JWT\): RS256, RS384, RS512, ES256, ES384, ES512, HS256, HS384, and HS512.

## Procedure

1.  Navigate to **Machine Identity Console** &gt; **** &gt; **Inbound integrations** &gt; **** &gt; **New integration** &gt; **JWT bearer grant**.

2.  Update the text fields in the Details form with the appropriate information.

<table id="table_nwn_z3x_r2c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**Name**

</td><td>

A unique name that identifies the application that you require JWT OAuth access for.

</td></tr><tr><td>

**Provider name**

</td><td>

Enter the name of the service provider you want to integrate with. Example: Microsoft, Google, Zoom, SAP, etc. **Note:** Provider name is a mandatory field.

</td></tr><tr><td>

**Client ID**

</td><td>

The auto-generated unique ID of the application. The system uses the value of this field to retrieve the public or shared key and validate the JWT. The value of this field should match the value of the issuer and audience claims in the JWT.

</td></tr><tr><td>

**Client secret**

</td><td>

The shared secret string that both the instance and the client application or website use to authorize communications with one another. Leave this field empty to have the instance auto-generate a client secret. To display existing client secrets, select the lock icon.

</td></tr><tr><td>

**User field**

</td><td>

Field in the User \(sys\_user\) table that the system uses to match the value of the subject claim in the JWT. Example:

If you add a token that has a subject claim value of user.name@example.com, then you would set the **User Field** to **Email**. This field tells the system to search the email field for the user.name@example.com value and use the matching user record in the inbound request.

</td></tr><tr><td>

**Enable JTI Verification**

</td><td>

Select to require a new token every token exchange.Default: Selected.

</td></tr><tr><td>

**JWKS URL**

</td><td>

The JSON Web key set URL. Its is a collection of public keys in JSON format. Identity providers publish a JWKS at a well-known URL so that client applications and services can retrieve the keys and validate the signatures of JSON Web Tokens \(JWTs\).

</td></tr><tr><td>

**JTI claim**

</td><td>

Unique identifier for each token. ServiceNow uses this claim to detect and prevent token replay by verifying that a token is not reused.

</td></tr><tr><td>

**Comments**

</td><td>

Add relevant comments.

</td></tr><tr><td>

**JWT verifier map**

</td><td>

Specify the identity provider, the verification method \(such as a JWKS URL or certificate\), and the mapping of JWT claims to ServiceNow user fields. Click on the Plus icon to add or edit the maps. Provide the following details in the **JWT verifier map** page:

-   Name- The unique name of the JWT verifier map configuration.
-   Application - The application where the verifier map is used.
-   Kid \(Key ID\)- The identifier of the key used to validate the JWT signature.
-   Sys certificate - The ServiceNow certificate record used for token verification
-   Shared key - A symmetric key used to validate tokens.


</td></tr><tr><td>

**Active**

</td><td>

Select the check box to make the OAuth application active.

</td></tr></tbody>
</table>3.  Update the text fields in the Advanced options \(optional\) form with the appropriate information.

<table id="table_ckp_jp4_jgc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**Enforce token restriction**

</td><td>

Select to only enable tokens to be used with APIs set to enable the authentication profile. You can set grant access using an API access policy.Default: Unselected.

</td></tr><tr><td>

**JWKS cache lifespan**

</td><td>

The duration \(in minutes\) for which ServiceNow caches the JSON Web Key Set \(JWKS\) from the identity provider.

</td></tr><tr><td>

**Access token lifespan**

</td><td>

The duration \(in seconds\) for which the access token remains valid before it expires.

</td></tr><tr><td>

**Clock skew**

</td><td>

Small differences in the system clocks of servers or devices involved in generating and validating a token can lead to issues when validating time-sensitive claims. Adjust the time above. Default value is: 0 seconds.

</td></tr></tbody>
</table>4.  Update the text fields in the Auth scope \(optional\) form with the appropriate information.

    **Note:** When you select an **Auth scope**, all the associated APIs are automatically populated in the **Limit authorization** text box.

    |Field|Description|
    |-----|-----------|
    |**Auth scope**|Access level of an application. The authentication scope restricts the actions that an access token can perform on APIs or data.|
    |**Limit authorization**|Names of the APIs for which you want to restrict authorization.|
    |**Allow access only to APIs in selected scope**|Enable the option for the integration to only access APIs that are explicitly listed in the selected scopes.|

    1.  Select **Add another row** to add auth scopes.

    2.  Select **Create new auth scope** to add a new auth scope.

        Enter the name of the Auth scope in the **Scope field** text box to select the newly created Auth scope. You can manually add and edit the APIs that needs to be associated with the new Auth scope.

        **Note:** Adding or editing APIs from the **Auth scope** menu affects all OAuth entities that are associated with the same authorization scope.

5.  Update the text fields in the Advanced options \(optional\) form with the appropriate information.

<table id="table_ckp_jp4_jgc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**Enforce token restriction**

</td><td>

Select to only enable tokens to be used with APIs set to enable the authentication profile. You can set grant access using an API access policy.Default: Unselected.

</td></tr><tr><td>

**JWKS cache lifespan**

</td><td>

The duration \(in minutes\) for which ServiceNow caches the JSON Web Key Set \(JWKS\) from the identity provider.

</td></tr><tr><td>

**Access token lifespan**

</td><td>

The duration \(in seconds\) for which the access token remains valid before it expires.

</td></tr><tr><td>

**Clock skew**

</td><td>

Small differences in the system clocks of servers or devices involved in generating and validating a token can lead to issues when validating time-sensitive claims. Adjust the time above. Default value is: 0 seconds.

</td></tr><tr><td>

**Token Format**

</td><td>

Format of token to generate. Options: -   JWT
-   Opaque
**Note:**

-   The jwks url is available in the location: `api/now/oauth/jwks`.
-   The rotated \(inactive keys\) from jwks response after is removed after 105 days default.


</td></tr></tbody>
</table>6.  Select **Save**.

    A new OAuth JSON Web Token bearer grant is created.

7.  Go to **All** &gt; **Inbound integrations** &gt; **Application Registries** to view the newly created JWT bearer grant.



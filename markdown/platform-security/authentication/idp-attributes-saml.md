---
title: Identity Provider attributes for Security Assertion Markup Language
description: Use the Identity Provider attributes that are received from the Security Assertion Markup Language \(SAML\) response and OpenID Connect \(OIDC\) from the Identity Provider \(IdP\) as a filter criteria for authentication.
locale: en-US
release: yokohama
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Identity Provider Attributes Filter, Filter criteria, Adaptive authentication, Authentication, Access Management]
---

# Identity Provider attributes for Security Assertion Markup Language

Use the Identity Provider attributes that are received from the Security Assertion Markup Language \(SAML\) response and OpenID Connect \(OIDC\) from the Identity Provider \(IdP\) as a filter criteria for authentication.

To fetch all the attributes from an IdP through the SAML response, you should perform a test connection with the IdP. After a successful test connection, the attributes are added in a new tab in the Identity Provider configuration page.

-   Identity Provider filter is available with Zero Trust Access feature. For more information, see [Zero Trust Access](session-access.md).
-   IdP attribute filter criteria can be used in [Post-authentication context](post-auth-context.md), [Zero Trust Access](session-access.md) session relegation, and [MFA \(Multi-Factor Authentication\) context](mfa-auth-context.md).

![Identity Provider](../images/identity-provider-attributes.png)

You can also add attributes by selecting **New** from the Identity Provider Attributes section and use those attributes for Adaptive Authentication by setting it to `true`.

The **Identity Provider Attributes** are displayed with the following details:

<table id="table_tz3_bww_vnb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Attribute name that is provided by the Identity Provider.

</td></tr><tr><td>

Display Name

</td><td>

Display Name is the detailed name that is used for the filter criteria.**Note:** You can provide a readable name as a Display Name, in some cases the Display Name provided by the Identity Providers are lengthy and not readable.

</td></tr><tr><td>

Default Value

</td><td>

Default value is used for filter criteria evaluation in case the attribute is missing in the SAML response.

</td></tr><tr><td>

Use in Adaptive Authentication

</td><td>

Option to use the Attribute in the Adaptive Authentication.

</td></tr></tbody>
</table>**Note:** Attributes that are populated from Azure IdP have name and display name limited to characters, due to the name length of the attribute.

You can also add new attributes by selecting **New** in the **Identity Providers Attributes** section.

If the Use in Adaptive Authentication is set to true, then the selected attribute is added as filter criteria in the Generic Filter Criteria. For example, **risk\_score** set to `true`. The Generic Filter Criteria page has a new filter created.


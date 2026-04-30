---
title: Filter criteria
description: Filter criteria \(also called policy inputs\) are used as inputs for policy conditions to verify and meet the requirements of an authentication request.
locale: en-US
release: xanadu
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Adaptive authentication, Authentication, Access Management]
---

# Filter criteria

Filter criteria \(also called policy inputs\) are used as inputs for policy conditions to verify and meet the requirements of an authentication request.

Use filter criteria to supply information authentication policies such as a user's IP address, roles, or groups. Add these criteria in the **Policy conditions** section of your policies.

There are seven types of filter criteria used in adaptive authentication. Your authentication policies can use one or more of these criteria to evaluate authentication requests.

**Note:** Location filter and Identity Provider filter are available with Zero Trust Access feature. For more information, see [Zero Trust Access](session-access.md).

|Type|Description|
|----|-----------|
|IP filter criteria|Use IP filter criteria to filter users based on the user's IP addresses. Both IPv4 and IPv6 are supported.|
|Role filter criteria|Use role filter criteria to filter users based on their roles.|
|Group filter criteria|Use group filter criteria to filter users based on the user group to which the user belongs.|
|Location filter criteria|Use location filter criteria to filter users based on the user location.|
|Identity Provider Attribute filter criterias|Use the Identity Provider attributes that are received from SAML response from the IdP as a filter criteria for authentication.|

## Generic Criteria

In addition to the previously listed types, there are four generic filter criteria. These criteria do not appear in your filter navigator, but you can select them while adding policy inputs to your authentication policies.

<table id="table_i43_tzy_2qb"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Authentication Scheme

</td><td>

Use to filter based on user's authentication scheme. This criteria is a choice type with two options:-   User name and Password, which denotes a local login​
-   SSO, which denotes a Multi-SSO\(SAML, OIDC, or Digest\) based login.

 **Note:** This Filter Criteria is available only when the **Integration - Multiple Provider Single Sign-On Installer**\[com.snc.integration.sso.multi.installer\] plugin is installed.

</td></tr><tr><td>

Identity Provider

</td><td>

Use to filter based on the user's identity provider. Use along with the authentication scheme criteria to have granular control over login process. This criteria is a reference to the **Identity Providers** \[sso\_properties\] table.**Note:** This Filter Criteria is available only when the **Integration - Multiple Provider Single Sign-On Installer**\[com.snc.integration.sso.multi.installer\] plugin is installed.

</td></tr><tr><td>

Role-based MFA

</td><td>

Use to filter based on the role-based MFA feature. This criteria is a boolean type filter criteria which denotes whether role-based MFA is enabled for the user.​

</td></tr><tr><td>

User-based MFA

</td><td>

Use to filter based on the user-based MFA feature. This criteria is a boolean type filter criteria which denotes whether user-based MFA is enabled for the user.​

</td></tr><tr><td>

Trusted mobile app

</td><td>

Trusted mobile app filter for enabling instance access from mobile app.

</td></tr></tbody>
</table>
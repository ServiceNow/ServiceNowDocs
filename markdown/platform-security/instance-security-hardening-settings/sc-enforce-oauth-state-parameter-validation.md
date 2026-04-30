---
title: Enforce oauth state parameter validation
description: Configure the glide.oauth.state.parameter.required property to prevent your instance from cross-site request forgery \(CSRF\) attacks.
locale: en-US
release: xanadu
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Enforce oauth state parameter validation

Configure the **glide.oauth.state.parameter.required** property to prevent your instance from cross-site request forgery \(CSRF\) attacks.

The **glide.oauth.state.parameter.required** property enables the State parameter to be required in an OAuth request for authorization code flow. The State parameter is a string value that should not contain special characters or be empty. Setting this property to **true** ensures that an attacker cannot perform Cross-site request forgery \(CSRF\) attacks during authentication, which protects your instance from attacks from an impersonated user.

## More information

<table id="table_hhv_dvg_1xb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.oauth.state.parameter.required**

</td></tr><tr><td>

Configuration type

</td><td>

System Properties \(/sys\_properties\_list.do\)

</td></tr><tr><td>

Data type

</td><td>

boolean

</td></tr><tr><td>

Recommended value

</td><td>

true

</td></tr><tr><td>

Default value

</td><td>

true

</td></tr><tr><td>

Category

</td><td>

[Access control](sc-access-control.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 4.2
-   CVSS score: Medium
-   Security risk details: Set this property to **true** to ensure that CSRF attacks are prevented.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Access control](sc-access-control.md)


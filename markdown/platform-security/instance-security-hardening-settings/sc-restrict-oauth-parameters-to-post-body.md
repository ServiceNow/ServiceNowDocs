---
title: Restrict oauth parameters to POST body \[New in Security Center 1.3\]
description: Use the glide.oauth.allow.parameters.in.post.body.only property to control the inbound OAuth authentication's acceptance of access tokens. Access tokens are sensitive and should only be accepted when located within a POST request body.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Data protection, Hardening settings, Platform Security]
---

# Restrict oauth parameters to POST body \[New in Security Center 1.3\]

Use the **glide.oauth.allow.parameters.in.post.body.only** property to control the inbound OAuth authentication's acceptance of access tokens. Access tokens are sensitive and should only be accepted when located within a POST request body.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.oauth.allow.parameters.in.post.body.only**

</td></tr><tr><td>

Configuration type

</td><td>

System Properties \(/sys\_properties\_list.do\)

</td></tr><tr><td>

Data type

</td><td>

Boolean

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

[Data protection](sc-data-protection.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 4.2
-   CVSS score: Medium
-   Security risk details: If **glide.oauth.allow.parameters.in.post.body.only** isn't set to the recommended value of **true**, access tokens could be present in the GET request parameter. These access tokens could linger in client and infrastructure logs and potentially lead to account takeover if those logs are leaked.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr><tr><td>

References

</td><td>

-   [OAuth 2.0](../../security/concept/c_OAuthApplications.md)
-   [Manage OAuth tokens](../../security/task/t_ManageTokens.md)

</td></tr><tr><td>

Functional impact

</td><td>

Ensures that oauth\_token.do processor accepts only POST body parameters as input for all supported grant types.

</td></tr></tbody>
</table>**Parent Topic:**[Data protection](sc-data-protection.md)


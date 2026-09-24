---
title: Restrict oauth parameters to POST body
description: Use the glide.oauth.allow.parameters.in.post.body.only property restricts OAuth credentials to POST request bodies when set to true.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/instance-security-hardening-settings/sc-restrict-oauth-parameters-to-post-body.html
release: brazil
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Data protection, Hardening settings, Platform Security]
---

# Restrict oauth parameters to POST body

Use the **glide.oauth.allow.parameters.in.post.body.only** property restricts OAuth credentials to POST request bodies when set to `true`.

Use the **glide.oauth.allow.parameters.in.post.body.only** property to control how the OAuth token endpoint \(/oauth\_token.do\) accepts OAuth credentials. When set to `true`, this property restricts OAuth parameters \(such as client\_id, client\_secret, authorization codes, and refresh tokens\) to POST request bodies only. OAuth credentials submitted using HTTP headers continue to be accepted.

To set up this property:

1.  Navigate to `/sys_properties_list.do` on the ServiceNow instance.
2.  Ensure **glide.oauth.allow.parameters.in.post.body.only** exists and is set to `true`.

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

Fallback value

</td><td>

false

</td></tr><tr><td>

Default value

</td><td>

true

</td></tr><tr><td>

Category

</td><td>

[Data protection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-data-protection.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 4.2
-   CVSS score: Medium
-   Security risk details: If **glide.oauth.allow.parameters.in.post.body.only** isn't set to the recommended value of **true**, OAuth credentials such as client\_id, client\_secret, authorization codes, and refresh tokens could be present in the URL query string. These credentials could linger in client and infrastructure logs and potentially lead to account takeover if those logs are leaked.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

Plugin OAuth 2.0

</td></tr><tr><td>

References

</td><td>

-   [OAuth 2.0](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/authentication/c_OAuthApplications.md)
-   [Manage OAuth tokens](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/authentication/t_ManageTokens.md)

</td></tr><tr><td>

Functional impact

</td><td>

Ensures that oauth\_token.do processor accepts only POST body parameters as input for all supported grant types.

</td></tr></tbody>
</table>**Parent Topic:**[Data protection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-data-protection.md)


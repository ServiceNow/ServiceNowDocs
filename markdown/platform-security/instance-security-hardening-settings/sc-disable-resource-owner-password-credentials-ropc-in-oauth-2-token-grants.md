---
title: Disable resource owner password credentials \(ROPC\) in OAuth 2 token grants \[New in Security Center 7.0\]
description: Prevent Resource Owner Password Credentials \(ROPC\) from granting OAuth 2 tokens.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Authentication, Hardening settings, Platform Security]
---

# Disable resource owner password credentials \(ROPC\) in OAuth 2 token grants \[New in Security Center 7.0\]

Prevent Resource Owner Password Credentials \(ROPC\) from granting OAuth 2 tokens.

By default, Resource Owner Password Credentials \(ROPC\) are allowed to grant OAuth 2 tokens on your instances when a client application directly requests an access token using a user name and password. When the **glide.oauth.inbound.ropc.grant\_type.disabled** is set to **true**, ROPC is inactive and can’t be used to grant OAuth 2 tokens.

Ensure that the **glide.oauth.inbound.ropc.grant\_type.disabled** system property is set to **true**. If the property doesn’t exist on the System Properties \[sys\_properties\] table, the default value is **false**. If this property exists on that table, it defaults to **false**.

## More information

<table id="table_hhv_dvg_1xb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.oauth.inbound.ropc.grant\_type.disabled**

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

false

</td></tr><tr><td>

Fallback value

</td><td>

false

</td></tr><tr><td>

Category

</td><td>

[Authentication](sc-authentication.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 3.3
-   CVSS score: Low
-   When the property is set to **false**, using ROPC to grant OAuth 2 tokens is allowed. ROPC is considered less secure that other authentication flows because the user's credentials are exposed to the application. This can lead to vulnerabilities in situations where the client is compromised and suffers from weaknesses similar to those of basic auth. OAuth 2.1 has deprecated ROPC.

</td></tr><tr><td>

Functional impact

</td><td>

When the property is set to **true**, ROPC is inactive and cannot be used to grant OAuth 2 tokens. This prevents any applications that are accessing the platform by granting OAuth 2 token using ROPC.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

The OAuth 2.0 \(com.snc.platform.security.oauth\) plugin must be active.

</td></tr></tbody>
</table>To learn more about adding or creating a system property, see [Add a system property](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/r_AvailableSystemProperties.md).

**Parent Topic:**[Authentication](sc-authentication.md)


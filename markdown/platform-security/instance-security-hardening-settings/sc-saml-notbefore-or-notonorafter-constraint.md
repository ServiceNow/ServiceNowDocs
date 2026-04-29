---
title: Minimize SAML notBefore or notOnOrAfter constraint duration \[Updated in Security Center 1.3 and 1.5\]
description: Configure this property to add a grace period in which SAML requests and responses are considered valid.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Authentication, Hardening settings, Platform Security]
---

# Minimize SAML notBefore or notOnOrAfter constraint duration \[Updated in Security Center 1.3 and 1.5\]

Configure this property to add a grace period in which SAML requests and responses are considered valid.

This property adds a grace period during which SAML requests and responses are considered valid. The property value represents the number of seconds to add to the **NotBefore** and **NotOnOrAfter** constraints to account for time differences between the Identity Provider \(IdP\) clock, and Service Provider \(SP\) clock. These constraints defend against replay attacks by denying requests that aren’t made within the specified time frame. If the IdP and SP clocks are significantly different, then the network latency may result in the SAML request being unauthorized.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.authenticate.sso.saml2.clockskew**

</td></tr><tr><td>

Configuration type

</td><td>

System Properties \(/sys\_properties\_list.do\)

</td></tr><tr><td>

Data type

</td><td>

string

</td></tr><tr><td>

Recommended value

</td><td>

less than 60

</td></tr><tr><td>

Default value

</td><td>

180

</td></tr><tr><td>

Category

</td><td>

[Authentication](sc-authentication.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 7.5
-   CVSS score: High
-   Security risk details: Setting the property to a value of 60 or higher may prevent the constraints from defending against replay attacks.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Authentication](sc-authentication.md)


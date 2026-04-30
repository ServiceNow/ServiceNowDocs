---
title: Minimize one-time out of band verifier lifetime duration \[Updated in Security Center 1.3\]
description: Manage the time duration for out-of-band verifiers.
locale: en-US
release: yokohama
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Authentication, Hardening settings, Platform Security]
---

# Minimize one-time out of band verifier lifetime duration \[Updated in Security Center 1.3\]

Manage the time duration for out-of-band verifiers.

An out-of-band verifier is an alternative delivery method for one-time code situations. For example, resetting a multi-factor token. If this method is enabled by administrators in the [Multi-factor authentication](../../../integrate/authentication/concept/mfa-landing.md) plugin, a one-time code is delivered by email. Set one-time out-of-band verifiers to expire after 10 minutes to limit the validity window. A larger time window allows more time for the code to be compromised through illicit means such as phishing, social engineering, or shoulder-surfing attacks.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.multifactor.onetime.code.validity**

</td></tr><tr><td>

Configuration type

</td><td>

System Properties \(/sys\_properties\_list.do\)

</td></tr><tr><td>

Data type

</td><td>

integer

</td></tr><tr><td>

Recommended value

</td><td>

10

</td></tr><tr><td>

Default value

</td><td>

10

</td></tr><tr><td>

Category

</td><td>

[Authentication](sc-authentication.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 3.9
-   CVSS score: Low
-   Security risk details: Set one-time out-of-band verifiers to expire after 10 minutes. Anything longer increases the risk of the code being compromised by a bad actor.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

[Multi-factor authentication](../../../integrate/authentication/concept/mfa-landing.md)

</td></tr><tr><td>

References

</td><td>

[Multi-factor authentication criteria](../../../integrate/authentication/concept/multi-factor-authentication-criteria.md)

</td></tr></tbody>
</table>**Parent Topic:**[Authentication](sc-authentication.md)


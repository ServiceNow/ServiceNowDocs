---
title: Enable account recovery
description: The glide.sso.acr.enabled property controls the account recovery feature.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Authentication, Hardening settings, Platform Security]
---

# Enable account recovery

The **glide.sso.acr.enabled** property controls the account recovery feature.

The **glide.sso.acr.enabled** system property controls the account recovery feature which binds the ability to bypass single sign-on to specifically designated administrators. If **glide.sso.acr.enabled** isn't set to the recommended value of **true**, then the local interactive log-ins \(username or password based\) are remain enabled when single sign-on is enabled on the instance.

Ensure that the property **glide.sso.acr.enabled** is set to **true**.

## More information

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.sso.acr.enabled**

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

&lt;none&gt;

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

-   Severity score: 6.5
-   CVSS rating: Medium
-   Security risk details: Eliminating local interactive log-ins reduces the potential for unauthorized access to the instance.

</td></tr><tr><td>

Functional impact

</td><td>

None

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Authentication](sc-authentication.md)


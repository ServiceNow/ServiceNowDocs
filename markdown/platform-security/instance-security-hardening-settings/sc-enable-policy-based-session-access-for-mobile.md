---
title: Enable policy based session access for mobile
description: Use the The Zero Trust- Policy Based Session Access plugin to control if users authenticating through a mobile app will have their roles reduced.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-13"
reading_time_minutes: 1
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Enable policy based session access for mobile

Use the The Zero Trust- Policy Based Session Access plugin to control if users authenticating through a mobile app will have their roles reduced.

The **Zero Trust - Policy Based Session Access** plugin allows security admins to reduce user access in a session based on IP, Location, Identity provider attributes and user attributes using adaptive authentication policies. When this property is set to **true**, then users logging in via mobile device will have their roles restricted as configured by the plugin policies.

Set the Glide Property **glide.authenticate.session\_access.mobile.enabled** to **true**.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.authenticate.session\_access.mobile.enabled**

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

true

</td></tr><tr><td>

Category

</td><td>

[Access control](sc-access-control.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 4.7
-   CVSS rating: Medium
-   Security risk details: Instance admins may wish to restrict high privileged access when users login via mobile device, possible indicating an unsafe environment for sensitive operations.

</td></tr><tr><td>

Functional impact

</td><td>

None

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Access control](sc-access-control.md)


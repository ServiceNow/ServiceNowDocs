---
title: Enable SMS code notification for enrollment and verification \[Updated in Security Center 1.3\]
description: The password\_reset.sms.use\_notify property controls the usage of SMS code notifications for password reset.
locale: en-US
release: yokohama
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Authentication, Hardening settings, Platform Security]
---

# Enable SMS code notification for enrollment and verification \[Updated in Security Center 1.3\]

The **password\_reset.sms.use\_notify** property controls the usage of SMS code notifications for password reset.

If the **password\_reset.sms.use\_notify** property is set to the recommended value of **true**, the user is notified to do a password reset using SMS verification and new device enrollment which is more secure than email.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**password\_reset.sms.use\_notify**

</td></tr><tr><td>

Configuration type

</td><td>

System Properties \(/sys\_properties\_list.do\)

</td></tr><tr><td>

Data type

</td><td>

booelan

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

[Authentication](sc-authentication.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 3.7
-   CVSS score: Low
-   Security risk details: Setting this property to**false** makes email the default method for password recovery which is less secure than SMS.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Authentication](sc-authentication.md)


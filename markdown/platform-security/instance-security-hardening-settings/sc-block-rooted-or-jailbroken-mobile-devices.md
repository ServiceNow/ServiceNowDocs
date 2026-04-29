---
title: Block rooted or jailbroken mobile devices
description: Secure your instance by preventing unauthorized access from jailbroken devices.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Malicious code, Hardening settings, Platform Security]
---

# Block rooted or jailbroken mobile devices

Secure your instance by preventing unauthorized access from jailbroken devices.

If **glide.sg.allow\_rooted\_jailbroken\_device** is not set to the recommended value of **false**, then the mobile app allows users to use the app from jailbroken or rooted mobile devices. Jailbroken or rooted mobile devices run untrusted code at the system level that can bypass the platform's security model which our mobile apps rely on. Setting **glide.sg.allow\_rooted\_jailbroken\_device** to **false** enables a limited client-side check to display an error message to the user if attempting to use the app from one of these devices.

This configuration maps to MASVS v1.4.2 requirement 8.1 at R-level.

Ensure that the property **glide.sg.allow\_rooted\_jailbroken\_device**is set to **false**.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.sg.allow\_rooted\_jailbroken\_device**

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

false

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

[Malicious code](sc-malicious-code.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 4.5
-   CVSS score: Medium
-   Security risk details: Allowing rooted or jailbroken mobile devices significantly increases the risk of credential theft, data leakage, and malicious code execution.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr><tr><td>

References

</td><td>

[Access control](sc-access-control.md)

</td></tr></tbody>
</table>**Parent Topic:**[Malicious code](sc-malicious-code.md)


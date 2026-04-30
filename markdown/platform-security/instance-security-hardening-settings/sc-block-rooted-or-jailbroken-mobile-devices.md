---
title: Block rooted or jailbroken mobile devices
description: Secure your instance by preventing unauthorized access from jailbroken devices.
locale: en-US
release: yokohama
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Malicious code, Hardening settings, Platform Security]
---

# Block rooted or jailbroken mobile devices

Secure your instance by preventing unauthorized access from jailbroken devices.

Use the **glide.sg.allow\_rooted\_jailbroken\_device** property to secure your instance from unauthorized access by jailbroken devices. If a user tries to authenticate into an instance using a mobile app while this property is set to **false**, they receive the following alert: `This device appears to be jailbroken and cannot be used to access this instance. Please contact your ServiceNow Administrator.` The app is frozen while the alert message is displayed, and the only way to dismiss this message is to select **Log out**. If this property is set to **true** users authenticate into an instance using a jailbroken device.

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

boolean

</td></tr><tr><td>

Recommended value

</td><td>

false

</td></tr><tr><td>

Default value

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
-   Security risk details: The lack of security on jailbroken devices makes them a prime target by bad actors. Having unauthorized entities accessing corporate data can weaken the security posture of a corporate network.

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


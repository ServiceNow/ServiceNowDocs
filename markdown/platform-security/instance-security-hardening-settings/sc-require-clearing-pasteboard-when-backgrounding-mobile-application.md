---
title: Require clearing pasteboard when backgrounding mobile application \[New in Security Center 1.3 and updated in 1.5\]
description: The glide.sg.clear\_pasteboard\_when\_backgrounded property controls if text copied from ServiceNow mobile app is kept in the clipboard and pasteboard after the app is in background mode. If it is not set to the recommended value of true, then sensitive information may be disclosed to the Android or iOS clipboard where it can be exposed to other applications on the device.
locale: en-US
release: xanadu
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2024-02-01"
reading_time_minutes: 1
breadcrumb: [Data protection, Hardening settings, Platform Security]
---

# Require clearing pasteboard when backgrounding mobile application \[New in Security Center 1.3 and updated in 1.5\]

The **glide.sg.clear\_pasteboard\_when\_backgrounded** property controls if text copied from ServiceNow mobile app is kept in the clipboard and pasteboard after the app is in background mode. If it is not set to the recommended value of true, then sensitive information may be disclosed to the Android or iOS clipboard where it can be exposed to other applications on the device.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.sg.clear\_pasteboard\_when\_backgrounded**

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

true

</td></tr><tr><td>

Default value

</td><td>

false

</td></tr><tr><td>

Category

</td><td>

[Data protection](sc-data-protection.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 3.5
-   CVSS score: Low
-   Security risk details: If this property is not set to the recommended value of true, then sensitive information may be disclosed to the Android or iOS clipboard where it can be exposed to other applications on the device.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr><tr><td>

Functional impact

</td><td>

This property clears the copy and paste clipboard when the ServiceNow app enters the background.

</td></tr></tbody>
</table>**Parent Topic:**[Data protection](sc-data-protection.md)


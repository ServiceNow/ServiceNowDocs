---
title: Require clearing pasteboard when backgrounding mobile application
description: The glide.sg.clear\_pasteboard\_when\_backgrounded property controls if text copied from ServiceNow mobile app is kept in the clipboard and pasteboard after the app is in background mode. If it is not set to the recommended value of true, then sensitive information may be disclosed to the Android or iOS clipboard where it can be exposed to other applications on the device.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-13"
reading_time_minutes: 1
breadcrumb: [Data protection, Hardening settings, Platform Security]
---

# Require clearing pasteboard when backgrounding mobile application

The **glide.sg.clear\_pasteboard\_when\_backgrounded** property controls if text copied from ServiceNow mobile app is kept in the clipboard and pasteboard after the app is in background mode. If it is not set to the recommended value of true, then sensitive information may be disclosed to the Android or iOS clipboard where it can be exposed to other applications on the device.

The **glide.sg.clear\_pasteboard\_when\_backgrounded** system property controls if text copied from ServiceNow mobile app is kept in the clipboard and pasteboard after the app is in background mode.

Ensure that **glide.sg.clear\_pasteboard\_when\_backgrounded** is set to **true**.

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

[Data protection](sc-data-protection.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 3.5
-   CVSS rating: Low
-   Security risk details: This creates a risk of sensitive information disclosure, as clipboard data can be accessed by other applications on the device, potentially exposing credentials, PII, or confidential business data. Enforcing this property helps prevent unintended data leakage across apps.

</td></tr><tr><td>

Functional impact

</td><td>

None

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Data protection](sc-data-protection.md)


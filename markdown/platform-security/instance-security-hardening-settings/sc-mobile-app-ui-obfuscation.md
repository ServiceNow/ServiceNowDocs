---
title: Require obfuscation of mobile app UI \[Updated in Security Center 1.3\]
description: Configure the glide.sg.blur\_ui\_when\_backgrounded property so that the UI of the app is blurred when the app is running in the background.
locale: en-US
release: xanadu
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Authentication, Hardening settings, Platform Security]
---

# Require obfuscation of mobile app UI \[Updated in Security Center 1.3\]

Configure the **glide.sg.blur\_ui\_when\_backgrounded** property so that the UI of the app is blurred when the app is running in the background.

If this property is not set to the recommended value of **true**, the mobile app's user interface is visible when viewed from the app switcher. The UI is still visible even when the app is running in background which provides a lower level of security and confidentiality to end users.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.sg.blur\_ui\_when\_backgrounded**

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

[File and resources](sc-file-resources.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 2.4
-   CVSS score: Low
-   Security risk details: Setting the value to **true** provides a higher level of confidentiality and privacy on the local device by blurring the UI when the app is running in the background.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr><tr><td>

References

</td><td>



</td></tr></tbody>
</table>**Parent Topic:**[Authentication](sc-authentication.md)


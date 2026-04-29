---
title: Disable logger for low privilege users in script sandbox
description: Manage Glide System's ability to log scripts being executed in the sandbox environment.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Error handling and logging, Hardening settings, Platform Security]
---

# Disable logger for low privilege users in script sandbox

Manage Glide System's ability to log scripts being executed in the sandbox environment.

If the **glide.security.sandbox\_no\_logging** system property is set to **false**, then logging is available for low-privileged users using sandboxed scripts. This property controls your instance's ability to log scripts being executed in the sandbox environment.

Ensure that the **glide.security.sandbox\_no\_logging** property is set to **true** in order to prevent low-privileged users using a sandboxed script to have logging functionality.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.security.sandbox\_no\_logging**

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

[Error handling and logging](sc-error-handling-logging.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 2.2
-   CVSS score: Low
-   Security risk details: A low-privileged user could inject logs allowing the malicious user to potentially obfuscate an attack.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Error handling and logging](sc-error-handling-logging.md)


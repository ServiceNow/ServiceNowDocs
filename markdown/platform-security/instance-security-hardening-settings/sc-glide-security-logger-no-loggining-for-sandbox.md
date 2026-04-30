---
title: Disable logger for low privilege users in script sandbox \[Updated in Security Center 1.3\]
description: Manage Glide System's ability to log scripts being executed in the sandbox environment.
locale: en-US
release: zurich
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Error handling and logging, Hardening settings, Platform Security]
---

# Disable logger for low privilege users in script sandbox \[Updated in Security Center 1.3\]

Manage Glide System's ability to log scripts being executed in the sandbox environment.

Use the **glide.security.sandbox\_no\_logging** property to control Glide System's ability to log scripts being executed in the sandbox environment. If **glide.security.sandbox\_no\_logging** is set to **false**, logging is available for lower-privileged users using sandboxed scripts. This is a potential security vulnerability because low privileged users can inject logs allowing a bad actor to potentially obfuscate an attack. Configure the property to **true** to prevent lower-privileged users that are using a sandboxed script from having logging functionality.

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

true

</td></tr><tr><td>

Category

</td><td>

[Error handling and logging](sc-error-handling-logging.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 2.2
-   CVSS score: Low
-   Security risk details: Setting this property to **false** enables logging for lower-privileged users which could allow a bad actor to obfuscate an attack.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Error handling and logging](sc-error-handling-logging.md)


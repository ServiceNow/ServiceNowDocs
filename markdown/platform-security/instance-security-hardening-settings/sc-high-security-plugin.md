---
title: Enable High Security Plugin
description: When you activate the High Security plugin, it creates or updates hundreds of different configurations to control the level of security on your instance. These configurations mitigate many of the top OWASP attacks by enabling strict access control, input validation, and output encoding.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Enable High Security Plugin

When you activate the High Security plugin, it creates or updates hundreds of different configurations to control the level of security on your instance. These configurations mitigate many of the top OWASP attacks by enabling strict access control, input validation, and output encoding.

The High Security plugin, activated by default, creates more than 900 different configurations to control the level of security on your instance. These configurations enable strict access control, input validation, and output encoding. It separates user functionality from access control management functionality through requiring administrators to explicitly elevate into a **security\_admin** role before making access control changes.

Ensure that the plugin **com.glide.high\_security** is activated.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**com.glide.high\_security**

</td></tr><tr><td>

Configuration type

</td><td>

System Properties \(/sys\_properties\_list.do\)

</td></tr><tr><td>

Data type

</td><td>

Plugin

</td></tr><tr><td>

Recommended value

</td><td>

The plugin **com.glide.high\_security** is active

</td></tr><tr><td>

Default value

</td><td>

 

</td></tr><tr><td>

Fallback value

</td><td>

 

</td></tr><tr><td>

Category

</td><td>

 

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 9.8
-   CVSS rating: Critical
-   Security risk details: Critical parts of the instance may be exposed to unauthorized access or manipulation.

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


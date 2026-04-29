---
title: Turn off verbose SQL error messages for import processor
description: Configure this property to control whether verbose SQL error messages are displayed.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Error handling and logging, Hardening settings, Platform Security]
---

# Turn off verbose SQL error messages for import processor

Configure this property to control whether verbose SQL error messages are displayed.

If the **glide.import.error\_message.generic** system property is set to **false** a verbose SQL error message is returned, potentially causing sensitive information disclosure.

Ensure that the **glide.import.error\_message.generic** is set to **true** to display a generic error message.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.import.error\_message.generic**

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

-   Severity score: 3.1
-   CVSS score: Low
-   Security risk details: If verbose SQL error messages are returned, sensitive information such as database structure, table names, or query details may be exposed. This information can be leveraged by attackers to craft targeted SQL injection attacks or exploit other vulnerabilities, increasing the risk of data breaches and system compromise. Limiting error detail is essential to prevent information disclosure that aids malicious activity.

</td></tr><tr><td>

Functional impact

</td><td>

None

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Error handling and logging](sc-error-handling-logging.md)


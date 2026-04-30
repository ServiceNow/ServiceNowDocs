---
title: Turn off verbose SQL error messages for import processor \[Updated in Security Center 1.3\]
description: Configure this property to control whether verbose SQL error messages are displayed.
locale: en-US
release: zurich
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Error handling and logging, Hardening settings, Platform Security]
---

# Turn off verbose SQL error messages for import processor \[Updated in Security Center 1.3\]

Configure this property to control whether verbose SQL error messages are displayed.

If the property is set to **false**, then a verbose SQL error message will display which can leak sensitive information. To avoid this, set the property to **true** to display a generic message.

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

true

</td></tr><tr><td>

Category

</td><td>

[Error handling and logging](sc-error-handling-logging.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 3.1
-   CVSS score: Low
-   Security risk details: Setting the property to **false** enables verbose SQL messages which can lead to information leakage.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Error handling and logging](sc-error-handling-logging.md)


---
title: Log html sanitization \[Removed in Security Center 2.0\]
description: Configure glide.html\_sanitize.discarded\_log.enable property to determine if HTML sanitization events will be logged in your instance.
locale: en-US
release: xanadu
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Error handling and logging, Hardening settings, Platform Security]
---

# Log html sanitization \[Removed in Security Center 2.0\]

Configure **glide.html\_sanitize.discarded\_log.enable** property to determine if HTML sanitization events will be logged in your instance.

If this property is not set to the recommended value of **true**, HTML sanitization events are not logged in the **sys\_log** table. Lack of logging could negatively impact your instance automated security detection and investigation capabilities.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.html\_sanitize.discarded\_log.enable**

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

true

</td></tr><tr><td>

Category

</td><td>

[Error handling and logging](sc-error-handling-logging.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 2.4
-   CVSS score: Low
-   Security risk details: If this property is not set to the recommended value of **true**, HTML sanitization events are not logged in the **sys\_log** table which could impact automated security detection and investigation capabilities.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr><tr><td>

References

</td><td>

[Enabling HTML sanitizer](../../security/task/t_ActivateHTMLSanitizer.md)

</td></tr></tbody>
</table>**Parent Topic:**[Error handling and logging](sc-error-handling-logging.md)


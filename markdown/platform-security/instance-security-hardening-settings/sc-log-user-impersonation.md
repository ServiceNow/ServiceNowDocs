---
title: Log user impersonation \[Updated in Security Center 1.3 and 2.0\]
description: Configure glide.sys.log\_impersonation to control if user-impersonating events are logged in your instance.
locale: en-US
release: zurich
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Error handling and logging, Hardening settings, Platform Security]
---

# Log user impersonation \[Updated in Security Center 1.3 and 2.0\]

Configure **glide.sys.log\_impersonation** to control if user-impersonating events are logged in your instance.

If this property is not set to the recommended value of **true**, user-impersonating events are no longer logged. The absence of logging could impact the automated security detection and investigation capabilities on your instance. Ensure the property **glide.sys.log\_impersonation** exists and is set to true. If the property does not appear in the sys\_properties table, add a new record.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.sys.log\_impersonation**

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

-   Severity score: 6.4
-   CVSS score: Medium
-   Security risk details: If this property is not set to **true**, user-impersonating events are no longer logged which could impact your instance's security detection and investigation capabilities.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr><tr><td>

References

</td><td>

[Impersonating users](https://www.servicenow.com/docs/access?context=c_ImpersonateAUser&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)

</td></tr></tbody>
</table>**Parent Topic:**[Error handling and logging](sc-error-handling-logging.md)


---
title: Log session audit events \[New in Security Center 1.3 and updated in 1.5\]
description: Set the glide.authenticate.session\_access.log\_audit\_event property to true, so that session audit events will be created in the sys\_session\_access\_audit table.
locale: en-US
release: yokohama
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Error handling and logging, Hardening settings, Platform Security]
---

# Log session audit events \[New in Security Center 1.3 and updated in 1.5\]

Set the **glide.authenticate.session\_access.log\_audit\_event** property to **true**, so that session audit events will be created in the **sys\_session\_access\_audit** table.

When the Glide Property **glide.authenticate.session\_access.log\_audit\_event** is set to true, session audit events will be created in the sys\_session\_access\_audit table. It is best practice to log information about who accessed a session to assist in malicious actor investigations. Information logged will include user, session ID \(non-sensitive\), IP address, roles, and policies.

**Note:** The **glide.authenticate.session\_access.log\_audit\_event** system property is specific to Zero trust access. For more information, see [Zero Trust Access](../../../integrate/authentication/concept/session-access.md).

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.authenticate.session\_access.log\_audit\_event**

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

-   Severity score: 6.3
-   CVSS score: Medium
-   Security risk details: Not setting this property to the recommended value of true prevents events from being logged. This could prevent you from finding bad actors in the event of a cyber attack.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Error handling and logging](sc-error-handling-logging.md)


---
title: Log Impersonation History
description: Enable impersonation history logging using a system property.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Error handling and logging, Hardening settings, Platform Security]
---

# Log Impersonation History

Enable impersonation history logging using a system property.

The impersonation history log tracks the following impersonation details on the Impersonation History \[sys\_user\_impersonation\_history\] table when an impersonation is performed using the UI.

-   Impersonating user
-   Impersonated user
-   Impersonation start and end times
-   SessionID

Ensure that the **identity.impersonation.history.enabled** property doesn’t exist in the System Properties \[sys\_properties\] table, or exists and is set to a value of `true`.

## More information

<table id="table_w2n_pqs_4hc"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**identity.impersonation.history.enabled**

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

Fallback value

</td><td>

true

</td></tr><tr><td>

Category

</td><td>

[Error handling and logging](sc-error-handling-logging.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 4.9
-   CVSS score: Medium
-   Security risk details: When this property is set to `true`, impersonation session details are logged in the Impersonation History \[sys\_user\_impersonation\_history\] table. Use this information for auditing in security investigations or for compliance purposes.

</td></tr><tr><td>

Functional Impact

</td><td>

When this property is set to `true`, impersonation session details are logged in the Impersonation History \[sys\_user\_impersonation\_history\] table. When set to `false`, the impersonation details aren’t captured this table.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Error handling and logging](sc-error-handling-logging.md)


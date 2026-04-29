---
title: Track Impersonation Events
description: Enable impersonation event tracking using a system property.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Error handling and logging, Hardening settings, Platform Security]
---

# Track Impersonation Events

Enable impersonation event tracking using a system property.

Use the **glide.audit.track\_impersonation** system property to enable the tracking of impersonation events in the Audit \[sys\_audit\] table. When set to `true`, any actions performed via impersonation are recorded as a reference in the sys\_audit.user column, providing a clear and traceable audit. When set to `false`, actions performed via impersonation appear to have been performed by the user being impersonated.

Ensure the **glide.audit.track\_impersonation** system property exists in the System Properties \[sys\_properties\] table and is set to a value of `true`.

## More information

<table id="table_w2n_pqs_4hc"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.audit.track\_impersonation**

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

false

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

-   Severity score: 4.9
-   CVSS score: Medium
-   Security risk details: Tracking impersonation events helps ensure that all actions are traceable to their true originators, reduces the risk of unauthorized changes. This detailed audit trail helps you meet compliance requirements by providing a clear record of all actions performed via impersonation. The system maintains accountability by ensuring that the true originators of actions are always recorded, even in complex scenarios involving AI agents.

</td></tr><tr><td>

Functional Impact

</td><td>

When enabled, this property ensures that any actions performed via impersonation are accurately recorded as a reference in sys\_audit.user column of the Audit \[sys\_audit\] table. If not enabled, any actions performed via impersonation appear to have been performed by the user being impersonated.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Error handling and logging](sc-error-handling-logging.md)


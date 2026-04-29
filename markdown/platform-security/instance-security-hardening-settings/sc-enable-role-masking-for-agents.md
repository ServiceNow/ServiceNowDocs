---
title: Enable Role Masking for Agents
description: Use a system property to enable the role masking feature.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Enable Role Masking for Agents

Use a system property to enable the role masking feature.

Use the **identity.agent.role\_masking.enabled** system property to enable the role masking feature. Role masking limits the roles that an AI agent uses when executing tasks. This configuration helps to prevent unnecessary access to resources not needed within the context of an agent. When this property isn't set to `true`, agents automatically inherit all roles from the user invoking them, potentially increasing the risk of privilege escalation and accidental data exposure.

Ensure that the **identity.agent.role\_masking.enabled** system property exists in the System Properties \[sys\_properties\] table and is set to a value of `true`.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**identity.agent.role\_masking.enabled**

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

false

</td></tr><tr><td>

Category

</td><td>

[Access control](sc-access-control.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 5
-   CVSS score: Medium
-   Security risk details: When this property isn’t set to `true`, agents automatically inherit all roles from the user invoking them. It may increase the risk of privilege escalation and accidental data exposure.

</td></tr><tr><td>

Functional Impact

</td><td>

If misconfigured, restrictive role masking may block intended access to a resource.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Access control](sc-access-control.md)


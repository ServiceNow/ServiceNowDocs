---
title: Restrict flow context read access
description: Use the com.snc.process\_flow.reporting.require\_flow\_access property to enforce if an additional access check is required for a user to read a flow check.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Restrict flow context read access

Use the **com.snc.process\_flow.reporting.require\_flow\_access** property to enforce if an additional access check is required for a user to read a flow check.

When the **com.snc.process\_flow.reporting.require\_flow\_access** system property is set to a value of **true**, there is an additional access check for a user trying to read a flow context. A user must have access to the parent flow to be able to read the flow context.

Ensure that the **com.snc.process\_flow.reporting.require\_flow\_access** system property is set to **true**

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**com.snc.process\_flow.reporting.require\_flow\_access**

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

true

</td></tr><tr><td>

Category

</td><td>

[Access control](sc-access-control.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 2.7
-   CVSS score: Low
-   Security risk details: There may be minor information disclosure if this property is not set securely.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr><tr><td>

Functional impact

</td><td>

When this property is enabled, the security for reading flow context records are increased. The instance enforces that a user trying to read the flow context has read access to the parent flow as well.

</td></tr></tbody>
</table>**Parent Topic:**[Access control](sc-access-control.md)


---
title: Disable ServiceNow root of trust \[Removed in 1.5\]
description: Use the com.snc.csf.servicenow\_root\_of\_trust.disabled property to control which build key certificates are trusted on an instance.
locale: en-US
release: xanadu
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Malicious code, Hardening settings, Platform Security]
---

# Disable ServiceNow root of trust \[Removed in 1.5\]

Use the **com.snc.csf.servicenow\_root\_of\_trust.disabled** property to control which build key certificates are trusted on an instance.

When the **com.snc.csf.servicenow\_root\_of\_trust.disabled** property is not set to the recommended value of true, signatures on the **sn\_kmf\_record\_signature** table with ServiceNow build certificates will be trusted on the instance. When the property is set to true, only signatures with customer certificates will be trusted. Instance admins should only trust their own certificates as this reduces security impact if a ServiceNow's build key and certificates were compromised.

## More information

<table id="table_o45_ngj_p1c"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**com.snc.csf.servicenow\_root\_of\_trust.disabled**

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

false

</td></tr><tr><td>

Category

</td><td>

[Malicious code](sc-malicious-code.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 4
-   CVSS score: Medium
-   Security risk details: When this property is not set to the recommended value of true, signatures on the **sn\_kmf\_record\_signature** table with ServiceNow build certificates will be trusted on the instance. This increases the security impact in the event a ServiceNow build is compromised by a bad actor.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr><tr><td>

References

</td><td>

-   [Change your Root of Trust configuration](../../encryption/concept/change-rot-overview.md)
-   [Disable ServiceNow Root of Trust](../../encryption/task/disable-sn-rot.md)

</td></tr><tr><td>

Functional impact

</td><td>

This property enables or disables Servicenow Root of Trust.

</td></tr></tbody>
</table>**Parent Topic:**[Malicious code](sc-malicious-code.md)


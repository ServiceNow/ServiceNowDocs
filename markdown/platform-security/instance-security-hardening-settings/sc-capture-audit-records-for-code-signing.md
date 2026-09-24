---
title: Capture audit records for Code Signing-protected records
description: Use the sn\_cse.com.snc.csf.vault\_audit\_enabled property to control whether the system logs changes to Code Signing-protected code.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/instance-security-hardening-settings/sc-capture-audit-records-for-code-signing.html
release: brazil
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 2
keywords: [audit logging, Code Signing]
breadcrumb: [Architecture, design, and threat modeling, Hardening settings, Platform Security]
---

# Capture audit records for Code Signing-protected records

Use the **sn\_cse.com.snc.csf.vault\_audit\_enabled** property to control whether the system logs changes to Code Signing-protected code.

When this property is set to `true`, every creation, modification, or deletion of protected code is logged, allowing administrators to review who changed what and when. When inactive, no audit trail is created for protected code changes.

**Note:** This property only applies when [Code Signing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/code-signing-landing.md) is activated on your instance. It has no effect on unprotected code or test and development environments.

## More information

<table id="table_l5d_fsp_bkc"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**sn\_cse.com.snc.csf.vault\_audit\_enabled**

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

[Architecture, design, and threat modeling](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-architecture-design-threat-molding.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score:5.1
-   CVSS rating:Medium
-   Security risk details:

Disabling this property stops audit logging for protected records. Attackers or insiders with write access can modify or delete scripts, business rules, and configurations without leaving any trace, hiding their activity from audits and conformance reports. While this doesn't bypass access controls, it delays incident response and tampers detection—a critical concern for regulatory conformance.


</td></tr><tr><td>

Functional impact

</td><td>

When enabled \(the default\), the system automatically records every change made to protected records in an audit log: who changed it, what changed, and when. Administrators can review this log for conformance and troubleshooting without any extra setup. This requires the Code Signing feature to be active and works automatically on production systems while skipping test and development environments to reduce log noise.

 Disabling the property stops these audit records from being created. It reduces database activity but removes the visibility teams require to track changes and verify conformance. The setting takes effect immediately without requiring a restart.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

This property requires the Code Signing feature to be activated on your instance. It has no effect if Code Signing is not enabled.

</td></tr></tbody>
</table>**Parent Topic:**[Architecture, design, and threat modeling](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-architecture-design-threat-molding.md)


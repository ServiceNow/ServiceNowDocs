---
title: Enforce domain access control on all tables
description: The glide.sys.domain.access\_handler.included\_tables property controls which tables have cross-domain write protection enforced.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/instance-security-hardening-settings/sc-enforce-domain-access-control-on-all-tables.html
release: brazil
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 2
keywords: [domain access control, cross-domain write protection, glide.sys.domain.access\_handler.included\_tables]
breadcrumb: [Architecture, design, and threat modeling, Hardening settings, Platform Security]
---

# Enforce domain access control on all tables

The **glide.sys.domain.access\_handler.included\_tables** property controls which tables have cross-domain write protection enforced.

When set to `*` \(wildcard\), all tables receive cross-domain write protection. When set to a comma-separated list of specific table names, only those tables have cross-domain write protection enforced. When left empty, no tables receive cross-domain write protection, disabling the feature.

1.  Navigate to /sys\_properties\_list.do on the instance.
2.  Verify the **glide.sys.domain.access\_handler.included\_tables** property exists in the `sys_properties` table and is set to `*`.

## More information

<table id="table_l5d_fsp_8ui"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.sys.domain.access\_handler.included\_tables**

</td></tr><tr><td>

Configuration type

</td><td>

System Properties \(/sys\_properties\_list.do\)

</td></tr><tr><td>

Data type

</td><td>

String

</td></tr><tr><td>

Recommended value

</td><td>

`*`

</td></tr><tr><td>

Default value

</td><td>

`*`

</td></tr><tr><td>

Fallback value

</td><td>

Empty

</td></tr><tr><td>

Category

</td><td>

[Architecture, design, and threat modeling](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-architecture-design-threat-molding.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 5.6
-   Common Vulnerability Scoring System \(CVSS\) rating: Medium
-   Security risk details:

If **glide.sys.domain.access\_handler.included\_tables** is narrowed to a subset of tables, emptied, or if the default configuration is removed, domain boundary enforcement stops. The instance no longer enforces domain boundaries on the affected tables.

In a domain-separated \(multi-tenant\) instance, users in one domain can create or update records with a `sys_domain` value outside their assigned domain. This breaks the tenant isolation that domain separation provides, resulting in unauthorized cross-domain data exposure and data planting.


</td></tr><tr><td>

Functional impact

</td><td>

The **glide.sys.domain.access\_handler.included\_tables** property controls the scope of domain access handler enforcement across tables in the instance. Modifying the value changes which tables receive cross-domain write protection. Expanding the property value toward `*` \(wildcard\) increases the scope of domain access handler enforcement. More tables undergo record visibility and access evaluation for domain boundaries. This can affect how users, integrations, and background operations interact with domain-separated data, potentially blocking writes that were previously allowed on tables outside the enforcement scope.

 Configuration options:

 -   `*` \(wildcard\) – Enforce domain access handler on all domain-applicable tables
-   Comma-separated table list – Enforce domain access handler only on the specified tables
-   Empty or absent – Enforce domain access handler on no tables \(enforcement turned off\)

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

This property is only evaluated when the Domain Support \(`com.glide.domain`\) plugin is active.

</td></tr></tbody>
</table>**Parent Topic:**[Architecture, design, and threat modeling](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-architecture-design-threat-molding.md)


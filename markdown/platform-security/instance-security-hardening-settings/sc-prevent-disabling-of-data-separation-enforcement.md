---
title: Prevent disabling of data separation enforcement
description: Prevent bypassing Mosaic domain-visibility filtering to maintain data separation boundaries across business units and customer domains.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/instance-security-hardening-settings/sc-prevent-disabling-of-data-separation-enforcement.html
release: brazil
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 1
keywords: [data separation, domain visibility, Mosaic, security]
breadcrumb: [Architecture, design, and threat modeling, Hardening settings, Platform Security]
---

# Prevent disabling of data separation enforcement

Prevent bypassing Mosaic domain-visibility filtering to maintain data separation boundaries across business units and customer domains.

The **glide.one\_extend.mosaic.sync.disable\_data\_separation\_enforcement** property controls whether the platform's Mosaic domain-visibility filtering for data-separated instances is bypassed.

When set to `false` \(the secure, default state\), the platform continues to compute and enforce per-domain visibility grants whenever data separation is enabled. Domain-scoped users see only the records within their granted visibility roots and Mosaic consumers apply the same filtering.

When domain-visibility filtering is bypassed on an instance with data separation enabled, the platform stops computing which domains a user is permitted to see. Instead, the platform treats every domain as visible to all users.

## More information

<table id="table_config_details"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.one\_extend.mosaic.sync.disable\_data\_separation\_enforcement**

</td></tr><tr><td>

Configuration type

</td><td>

System Properties \(`/sys_properties_list.do`\)

</td></tr><tr><td>

Data type

</td><td>

Boolean

</td></tr><tr><td>

Recommended value

</td><td>

false

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

Data separation

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 5.4
-   CVSS rating: Medium
-   Security risk details:

When domain-visibility filtering is bypassed, users in one business unit or customer domain can access records belonging to another domain. Data becomes exposed across organizational boundaries that were designed to remain isolated. Failure to enforce this control may result in unauthorized cross-domain data disclosure and a breakdown of the data-separation guarantees an organization relies on for regulatory or contractual compliance.


</td></tr><tr><td>

Functional impact

</td><td>

When set to `false`, the platform preserves domain-visibility filtering for Mosaic sync consumers. Integrations that were relying on the broader, unfiltered view of cross-domain records will see records disappear from their results.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

Only applicable when domain and data separation is configured \(plugin **com.glide.domain.msp\_extensions.installer active**\).

</td></tr></tbody>
</table>**Parent Topic:**[Architecture, design, and threat modeling](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-architecture-design-threat-molding.md)


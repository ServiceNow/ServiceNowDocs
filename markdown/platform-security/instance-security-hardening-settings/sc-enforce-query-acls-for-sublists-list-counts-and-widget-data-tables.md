---
title: Enforce Query ACLs for SubLists, List Counts and Widget Data Tables
description: Enforce query ACLs on sublist, list count, and widget data table queries using system properties.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Architecture, design, and threat modeling, Hardening settings, Platform Security]
---

# Enforce Query ACLs for SubLists, List Counts and Widget Data Tables

Enforce query ACLs on sublist, list count, and widget data table queries using system properties.

Set **com.glide.security.query\_acl.enabled.sub\_lists** to **true** to enforce query ACLs on sublist queries, such as grouped lists and related lists.

Set **com.glide.security.query\_acl.enabled.list\_count** to **true** to enforce query ACLs on list count queries.

Set **glide.security.query\_acl.enabled.data\_table** to **true** to enforce query ACLs on widget data tables.

If any of these system properties are set to **false**, an attacker can use blind queries to enumerate and exfiltrate data due to the default behavior of `GlideRecord.addEncodedQuery`. If these properties don't exist in the System Properties \[sys\_properties\] table, the secure default of true is used. A third option, **external\_and\_guests**, enforces ACLs only for external users and guests.

Ensure these system properties do not appear in the System Properties \[sys\_properties\] table or are set to **true**.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

-   **com.glide.security.query\_acl.enabled.sub\_lists**
-   **com.glide.security.query\_acl.enabled.list\_count**
-   **glide.security.query\_acl.enabled.data\_table**

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

-   true
-   true
-   true

</td></tr><tr><td>

Default value

</td><td>

-   true
-   true
-   true

</td></tr><tr><td>

Fallback value

</td><td>

-   true
-   true
-   true

</td></tr><tr><td>

Category

</td><td>

[Architecture, design, and threat modeling](sc-architecture-design-threat-molding.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 5.3
-   CVSS score: Medium
-   Security Risk: ACLs can be bypassed disclosing field data to users who do not have permissions to see it. This could include sensitive data depending on the table exploited.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Architecture, design, and threat modeling](sc-architecture-design-threat-molding.md)


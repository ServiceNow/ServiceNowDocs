---
title: Enforce Query ACLs for Knowledge Quick Links
description: Enforce query ACLs for Knowledge Quick Links using a system property.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Architecture, design, and threat modeling, Hardening settings, Platform Security]
---

# Enforce Query ACLs for Knowledge Quick Links

Enforce query ACLs for Knowledge Quick Links using a system property.

When the **com.glide.security.query\_acl.enabled.knowledge\_quick\_links** system property is set to **true**, query ACLs are enforced for Knowledge Quick Links. If this property is set to **false**, an attacker can use blind queries to enumerate and exfiltrate data due to the default behavior of `GlideRecord.addEncodedQuery`.

If the property doesn’t exist in the System properties \[sys\_properties\] table, the secure default of **true** is used. A third option, **external\_and\_guests** enforces query ACLs only for external users and guests.

Verify that the **com.glide.security.query\_acl.enabled.knowledge\_quick\_links** system property is set to **true**.

## More information

<table id="table_hhv_dvg_1xb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**com.glide.security.query\_acl.enabled.knowledge\_quick\_links**

</td></tr><tr><td>

Configuration type

</td><td>

System Properties \(/sys\_properties\_list.do\)

</td></tr><tr><td>

Data type

</td><td>

String - Used as a ternary operator

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

[Architecture, design, and threat modeling](sc-architecture-design-threat-molding.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 5.3
-   CVSS score: Medium
-   Security Risk: ACLs can be bypassed, disclosing field data to users who don’t have permissions to see it. This disclosure could include sensitive data depending on the table exploited.

</td></tr><tr><td>

Functional impact

</td><td>

Users aren’t able to perform specific queries on fields where they don’t have field level access.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>To learn more about adding or creating a system property, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=australia&pubname=australia-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

**Parent Topic:**[Architecture, design, and threat modeling](sc-architecture-design-threat-molding.md)


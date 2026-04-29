---
title: Disable Adding Default Roles to Skill ACLs
description: Use system properties to control what roles are automatically added to generative AI skill ACLs.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Disable Adding Default Roles to Skill ACLs

Use system properties to control what roles are automatically added to generative AI skill ACLs.

Use the **com.glide.one\_extend.include\_default\_roles\_for\_skill\_acl** system property to control whether roles are automatically added to generative AI skill ACLs when they’re created or updated via the global.GenAiSkilSecurityUtils API. This property is used by the Now Assist Skill Kit \(NASK\) to enforce consistent security policies across all AI skills.

When a skill ACL is inserted or updated, the default roles defined in the **com.glide.one\_extend.default\_roles\_for\_skill\_acl** system property are automatically included. This addition ensures that certain privileged roles always have access to execute the skills. The **com.glide.one\_extend.default\_roles\_for\_skill\_acl** property may contain a comma-separated list of roles.

Ensure that the **com.glide.one\_extend.include\_default\_roles\_for\_skill\_acl** is set to `false`, or that the property doesn't exist on the System Properties \[sys\_properties\] table.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**com.glide.one\_extend.include\_default\_roles\_for\_skill\_acl**

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

[Access control](sc-access-control.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 4.2
-   CVSS score: Medium
-   Security risk details: Roles are automatically added to Generative AI Skill ACLs when this feature is enabled. Depending on the role, this may allow overly broad access to certain skills and override intended ACL behavior.

</td></tr><tr><td>

Functional impact

</td><td>

Certain roles may be prevented from using skills if they don’t satisfy an existing access control. These two property configurations ensure certain roles retain a base level of access to all skills.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Access control](sc-access-control.md)


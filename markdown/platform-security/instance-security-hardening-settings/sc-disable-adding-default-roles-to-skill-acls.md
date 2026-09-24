---
title: Disable adding default roles to skill ACLs
description: Use system properties to control what roles are automatically added to generative AI skill ACLs.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/instance-security-hardening-settings/sc-disable-adding-default-roles-to-skill-acls.html
release: brazil
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Disable adding default roles to skill ACLs

Use system properties to control what roles are automatically added to generative AI skill ACLs.

Use the **com.glide.one\_extend.include\_default\_roles\_for\_skill\_acl** system property to control whether roles are automatically added to generative AI skill ACLs when they're created or updated using the global.GenAiSkillSecurityUtils API. This property is used to enforce consistent security policies across all AI skills.

When a skill ACL is inserted or updated, the default roles defined in the **com.glide.one\_extend.default\_roles\_for\_skill\_acl** system property are automatically included. This addition ensures that certain privileged roles always have access to execute the skills. The **com.glide.one\_extend.default\_roles\_for\_skill\_acl** property may contain a comma-separated list of roles.

Roles are automatically added to Generative AI Skill ACLs when **com.glide.one\_extend.include\_default\_roles\_for\_skill\_acl** is set to true. Depending on the role, this may allow overly broad access to certain skills and override intended ACL behavior.

1.  Navigate to /sys\_properties\_list.do on the instance.
2.  Ensure the **com.glide.one\_extend.include\_default\_roles\_for\_skill\_acl** property does not exist in the sys\_properties table or is set to `false`.

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

[Access control](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-access-control.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 4.2
-   CVSS score: Medium
-   Security risk details: Roles are automatically added to Generative AI Skill ACLs when **com.glide.one\_extend.include\_default\_roles\_for\_skill\_acl** is set to true. Depending on the role, this may allow overly broad access to certain skills and override intended ACL behavior.

</td></tr><tr><td>

Functional impact

</td><td>

When **com.glide.one\_extend.include\_default\_roles\_for\_skill\_acl** is set to `false`, roles are no longer automatically granted access to generative AI skill ACLs — any role that needs to execute a skill must satisfy the skill's own access control instead of relying on an automatically-added default role. The related **com.glide.one\_extend.default\_roles\_for\_skill\_acl** property, which lists which roles get auto-added when **com.glide.one\_extend.include\_default\_roles\_for\_skill\_acl** is set to true, has no effect while it is set to false.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Access control](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-access-control.md)


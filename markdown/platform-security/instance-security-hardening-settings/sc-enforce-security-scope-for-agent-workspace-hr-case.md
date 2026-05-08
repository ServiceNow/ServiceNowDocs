---
title: Enforce Security Scope for Agent Workspace for HR Case Management \[New in Security Center 1.5 and updated in 2.0\]
description: Configure the Agent Workspace for HR Case Management plugin so that data in scope master tables can only be accessed by users with the correct permissions, enforcing the principle of least privilege.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Enforce Security Scope for Agent Workspace for HR Case Management \[New in Security Center 1.5 and updated in 2.0\]

Configure the Agent Workspace for HR Case Management plugin so that data in scope master tables can only be accessed by users with the correct permissions, enforcing the principle of least privilege.

When the **glide.enforce\_security\_scope.sn\_hr\_agent\_ws** plugin is configured to the recommended value of true, then only the access control lists \(ACLs\) within the Agent Workspace for HR Case Management plugin are used to determine access to a resource. When this setting is set to false, then Agent Workspace for HR Case Management data in scope master tables are exposed because the ACLs from all scopes are granted access.For example, an IT Administrator can access Agent Workspace for HR Case Management data when this setting is set to false. To prevent this from happening, set **glide.enforce\_security\_scope.sn\_hr\_agent\_ws** to the recommended value of true which ensures that the principle of least privilege exists as users can only access resources they have permission to.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.enforce\_security\_scope.sn\_hr\_agent\_ws**

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

Category

</td><td>

[Access control](sc-access-control.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 2.7
-   CVSS score: Low
-   Security risk details: Configuring this setting to false causes the Agent Workspace for HR Case Management data in scope master tables to be exposed because the ACLs from all scopes are granted access.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

Agent Workspace for HR Case Management

</td></tr><tr><td>

Functional impact

</td><td>

Configuring this setting to true will enforce global ACLs to be executed for a table, if scoped ACLs do not exist for it.

</td></tr><tr><td>

References

</td><td>

-   [https://owasp.org/www-project-proactive-controls/\#div-numbering](https://owasp.org/www-project-proactive-controls/#div-numbering)
-   Add a component to Agent Workspace

</td></tr></tbody>
</table>**Parent Topic:**[Access control](sc-access-control.md)


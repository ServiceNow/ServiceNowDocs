---
title: Enforce ACL on HR Core Data \[New in Security Center 2.0\]
description: Learn how to configure the glide.enforce\_security\_scope.sn\_hr\_core property so that the Human Resources Scoped App: Core \(com.sn\_hr\_core\) plugin does not expose sensitive data to access control lists \(ACLs\) from all other scopes.
locale: en-US
release: yokohama
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Enforce ACL on HR Core Data \[New in Security Center 2.0\]

Learn how to configure the **glide.enforce\_security\_scope.sn\_hr\_core** property so that the Human Resources Scoped App: Core \(com.sn\_hr\_core\) plugin does not expose sensitive data to access control lists \(ACLs\) from all other scopes.

The **glide.enforce\_security\_scope.sn\_hr\_core** property restricts the access control lists \(ACLs\) of several global data tables like sys\_attachment and sys\_email to only consider the sn\_hr\_core scope. If this property is not set to the recommended value of true, then data from the Human Resources Scoped App: Core plugin will be exposed to ACLs from all other scopes. For instance, this could result in the IT administrator gaining access to human resources data.

**Warning:** This is a safe harbor property, meaning the value can't be altered once it's changed. It is non-revertible.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.enforce\_security\_scope.sn\_hr\_core**

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

true

</td></tr><tr><td>

Category

</td><td>

[Access control](sc-access-control.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 6.5
-   CVSS score: Medium
-   Security risk details: If this property is not set to the secure value of true, then data from the Human Resources Scoped App: Core plugin will be exposed to ACLs from all other scopes.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr><tr><td>

References

</td><td>

[Activate Case and Knowledge Management](https://www.servicenow.com/docs/access?context=activate-case-and-knowledge-management-scoped&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)

</td></tr></tbody>
</table>**Parent Topic:**[Access control](sc-access-control.md)


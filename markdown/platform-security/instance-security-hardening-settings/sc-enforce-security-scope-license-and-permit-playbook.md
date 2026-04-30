---
title: Enforce security scope license and permit playbook \[New in Security Center 1.5 and updated in 2.0\]
description: Use this property to determine if only the access control lists \(ACLs\) within the License and Permit plugin will be used in determining access to the scope, or if ACLs from all scopes will be considered.
locale: en-US
release: zurich
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Enforce security scope license and permit playbook \[New in Security Center 1.5 and updated in 2.0\]

Use this property to determine if only the access control lists \(ACLs\) within the License and Permit plugin will be used in determining access to the scope, or if ACLs from all scopes will be considered.

When the **glide.enforce\_security\_scope.sn\_gsm\_lic\_prmt** property is set to the recommended value of true, then only ACLs within the License and Permit plugin are used to determine access to the scope. When this setting is configured to false, then License and Permit Playbooks data in scope master tables are exposed because ACLs from all scopes are granted access. To reduce data exposure, set **glide.enforce\_security\_scope.sn\_gsm\_lic\_prmt** to the recommended value of true.

## More information

<table id="table_vwl_4tp_41c"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.enforce\_security\_scope.sn\_gsm\_lic\_prmt**

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
-   Security risk details: Configuring this setting to the recommended value of true secures the License and Permit Playbooks data in scope master tables by considering only ACLs from **sn\_gsm\_lic\_prmt** scope for granting access. Setting this to false exposes the License and Permit Playbooks data in scope master tables by considering the ACLs from all scopes for granting access. For example, the IT Administrator can access License and Permit Playbooks data when this setting is false.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr><tr><td>

References

</td><td>

-   [Using License and Permit Playbook](https://www.servicenow.com/docs/access?context=psds-using-lp-playbooks&version=zurich&pubname=zurich-government-industry&ft:locale=en-US)
-   [Application scope](https://www.servicenow.com/docs/access?context=c_ApplicationScope&version=zurich&pubname=zurich-application-development&ft:locale=en-US)

</td></tr></tbody>
</table>**Parent Topic:**[Access control](sc-access-control.md)


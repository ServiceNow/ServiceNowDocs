---
title: Configure event management assignment group admin roles \[New in Security Center 1.5\]
description: Use the evt\_mgmt.connector\_assignment\_group\_admin\_roles property to set which roles are authorized for admin access over the assignment group field in connector instances.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Configure event management assignment group admin roles \[New in Security Center 1.5\]

Use the **evt\_mgmt.connector\_assignment\_group\_admin\_roles** property to set which roles are authorized for admin access over the assignment group field in connector instances.

The **evt\_mgmt.connector\_assignment\_group\_admin\_roles** property contains a comma separated string which indicates the role names that have admin access over the assignment group field in connector instances. Changing the default roles in this list may enable unauthorized users to alter event integrations on the instance. To prevent unauthorized access to roles, set **evt\_mgmt.connector\_assignment\_group\_admin\_roles** to the value of `admin,evt_mgmt_admin,sn_sow_srm.srm_admin`. Review any additional roles in the recommended value string to ensure that the role should be included.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**evt\_mgmt.connector\_assignment\_group\_admin\_roles**

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

admin,evt\_mgmt\_admin,sn\_sow\_srm.srm\_admin

</td></tr><tr><td>

Default value

</td><td>

admin,evt\_mgmt\_admin,sn\_sow\_srm.srm\_admin

</td></tr><tr><td>

Fallback value

</td><td>

admin,evt\_mgmt\_admin,sn\_sow\_srm.srm\_admin

</td></tr><tr><td>

Category

</td><td>

[Access control](sc-access-control.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 3.1
-   CVSS rating: Low
-   Security risk details: Changing the default roles in this list may open up unauthorized users to altering event integrations on the instance.

</td></tr><tr><td>

Functional impact

</td><td>

Changing the default roles in this list may prevent previously authorized users from altering event integrations on the instance.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Access control](sc-access-control.md)


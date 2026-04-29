---
title: Enable work order management query rules for service organizations
description: Use the sn\_fsm.use\_query\_rules property to apply rules and filters to the Field Service Management tables.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Enable work order management query rules for service organizations

Use the **sn\_fsm.use\_query\_rules** property to apply rules and filters to the Field Service Management tables.

When set to **true**, rules/filters from sn\_query\_rule table will be used to determine read access to Field Service Management-related tables \(Work Order and Work Order Task\) to the logged in user through query business rules and read ACLs. When **false**, the records won't be filtered based on query rules. Query business rules add additional security validations. Specifically, this property will filter records for agents, qualifiers, and dispatchers based on their assigned territory or territory membership. It is best practice to follow the principle of least privilege when reading records.

Set the **sn\_fsm.use\_query\_rules** system property to **true**.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**sn\_fsm.use\_query\_rules**

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

false

</td></tr><tr><td>

Category

</td><td>

[Access control](sc-access-control.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 4.3
-   CVSS score: Medium
-   Security risk details: There may be increased risk of data exposure from Field Service Management tables.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr><tr><td>

Functional impact

</td><td>

When set to true, rules/filters from sn\_query\_rule table are used to determine read access to Field service management related tables. For example, Work Order \(WO\) and Work Order Table \(WOT\) to the logged-in user through query business rules and READ ACLs. When false, the records aren't filtered based on query rules.

 Enabling this property secures the data, and all data \(wm\_task and wm\_order\) won't be visible to their users.

</td></tr><tr><td>

References

</td><td>

 

</td></tr></tbody>
</table>**Parent Topic:**[Access control](sc-access-control.md)


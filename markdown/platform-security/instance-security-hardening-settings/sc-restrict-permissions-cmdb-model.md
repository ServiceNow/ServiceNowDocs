---
title: Restrict permissions for CMDB model \[Updated in Security Center 1.3 and 1.5\]
description: Use the csm\_cmdb\_model.customer\_visible\_flag system property to limit customer access to data in the Product Models table as an additional access control to the CMDB model.
locale: en-US
release: xanadu
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2024-02-01"
reading_time_minutes: 1
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Restrict permissions for CMDB model \[Updated in Security Center 1.3 and 1.5\]

Use the **csm\_cmdb\_model.customer\_visible\_flag** system property to limit customer access to data in the Product Models table as an additional access control to the CMDB model.

Set the **csm\_cmdb\_model.customer\_visible\_flag** property to **true** to enable the Customer Visible field for the tables listed below:

-   Product Models table \[cmdb\_model\]
-   Software Models table \[cmdb\_software\_product\_model\]
-   Application Models table \[cmdb\_application\_product\_model\]
-   Consumable Models table \[cmdb\_consumable\_product\_model\]
-   Facility Models table \[cmdb\_facility\_product\_model\]
-   Hardware Models table \[cmdb\_hardware\_product\_model\]

Setting this property as **true** hides all cmdb\_model values by default.

Set the property to **false** to not consider the customer\_visible column/atrribute on the cmdb\_model table and to rely on the bases cmdb\_model ACLs which are accessible to sn\_esm\_user.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Property name

</td><td>

**csm\_cmdb\_model.customer\_visible\_flag**

</td></tr><tr><td>

Configuration type

</td><td>

System Properties \(/sys\_properties\_list.do\)

</td></tr><tr><td>

Category

</td><td>

[Access control](sc-access-control.md)

</td></tr><tr><td>

Purpose

</td><td>

When set to tue**true**, the system uses the setting in the Customer Visible field to determine access to product model data on the Customer Service Portal.

</td></tr><tr><td>

Recommended value

</td><td>

true

</td></tr><tr><td>

Default value

</td><td>

false

</td></tr><tr><td>

Configuration type

</td><td>

Boolean

</td></tr><tr><td>

Security risk

</td><td>

\(Moderate\) Any user with the sn\_esm\_user role and out of the box ACLs could have permissions to the CMDB model. **Note:** this role tends to be granted to external users. External users could unwillingly be given permissions to the CMDB model.

</td></tr><tr><td>

References

</td><td>

[Limit access to product model data on the Customer Service Portal](https://www.servicenow.com/docs/access?context=cust-serv-portal-prod-model-access&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US)

</td></tr></tbody>
</table>To learn more about adding or creating a system property, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=xanadu&pubname=xanadu-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

**Parent Topic:**[Access control](sc-access-control.md)


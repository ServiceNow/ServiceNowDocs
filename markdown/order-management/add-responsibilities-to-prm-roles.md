---
title: Add responsibilities to PRM roles
description: A responsibility describes a role or function that supports a user. Use responsibility definitions to create relationships between any two partner entities.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-05-06"
reading_time_minutes: 1
breadcrumb: [PRM roles and components, Configure Partner Relationship Management, Configure, Sales Customer Relationship Management]
---

# Add responsibilities to PRM roles

A responsibility describes a role or function that supports a user. Use responsibility definitions to create relationships between any two partner entities.

## Before you begin

Role required: sn\_prm.enterprise\_rel\_manager, sn\_prm.external\_partner\_associate, or sn\_prm.external\_partner\_manager

## About this task

Related party configurations define the title of a relationship between an entity and an organization or a user. These configurations also enable linking related party types with responsibility definitions to grant access as needed.

|Type|Default Responsibility|
|----|----------------------|
|Enterprise Partner Relationship Manager \[sn\_prm.enterprise\_partner\_rel\_manager\]|Location Relationship Manager \[sn\_bus\_loc.location\_relationship\_manager\]|
|External Partner Associate \[sn\_prm.external\_partner\_associate\]|Location Contributor \[sn\_customerservice.service\_organization\_contributor\]|
|External Partner Manager \[sn\_prm.external\_partner\_manager\]|Location Manager Contributor \[sn\_customerservice.svc\_location\_manager\_contributor\]|

**Note:** The default responsibilities are automatically installed with the Business Location plugin \(com.snc.business\_location\).

## Procedure

1.  Navigate to **All** &gt; **Partner Relationship Management** &gt; **Channel Partner**.

2.  Open a channel partner record and add an external staff member or an enterprise partner relationship manager based on your requirement.

<table id="choicetable_y1y_n4r_dfc"><thead><tr><th align="left" id="d46129e124">

Task

</th><th align="left" id="d46129e127">

Description

</th></tr></thead><tbody><tr><td id="d46129e133">

**Register External staff member**

</td><td>

1.  Select **Register External Partner Staff** from the channel partner record.
2.  Select the **Role Type** you want to associate with your user, whether external partner manager or external partner associate.
3.  Select **Submit**.
 To learn more about the role type and the member registration fields, see [Member registration form](../reference/member-registration-form.md).

</td></tr><tr><td id="d46129e173">

**Register Enterprise Partner Relationship Manager**

</td><td>

1.  Select **Edit** from the Members related list on the channel partner record to add an enterprise member as a channel partner.
2.  Open the record associated with the user and select **New** from the Service Organization Member Responsibilities related list.
3.  Enter the role name in the **Type** field to assign a responsibility to the role.
4.  Select **Submit**.


</td></tr></tbody>
</table>
## Result

An external staff member or an enterprise partner relationship manager is registered.

**Parent Topic:**[Roles and components of Partner Relationship Management](../concept/roles-and-components-of-partner-relationship-management.md)


---
title: Business capability form
description: Business Capability is a common table used within the Enterprise Architecture \(formerly Application Portfolio Management\) application.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Enterprise Architecture \(formerly Application Portfolio Management\) reference, Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Business capability form

Business Capability is a common table used within the Enterprise Architecture \(formerly Application Portfolio Management\) application.

## Business Capability form fields

<table id="table_apm_bus_cap"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the business capability.

</td></tr><tr><td>

Parent

</td><td>

The parent capability for the capability that you’re creating.Assigning a parent capability renders the business capability as a child capability. If no parent is assigned or if the parent is null, then the level of the capability is at 0 level or root, which means it’s a root node capability. If the parent field is made null, then a message prompts you to run a scheduled job to update the business capability levels.

</td></tr><tr><td>

Level

</td><td>

The level at which the capability is in the hierarchy. If there’s no parent capability, then the level is 0, which indicates that the capability is at the root level.Level at which the capability is in the hierarchy. Up to six levels are supported.

If you add a capability or update it by changing its parent, then run the Update Business Capability Levels job, on demand. The job determines the capability level and updates all the capabilities with the level information.

 **Note:** The system updates the field and the user can’t.

</td></tr><tr><td>

Business Unit

</td><td>

Business unit that is associated with the selected business capability.

</td></tr><tr><td>

Order

</td><td>

Assign any integer value. Applicable only for level-0 capability.The number you assign determines the position of the capability in the sequential order of all other business capabilities in that capability hierarchy.

 The **Order** field is available only for root node or level-0 capabilities. The scheduled job checks for conditions such as order values entered for non-root capabilities, duplicate order values, and null value and eliminates such values. It calculates and sets the level and hierarchy ID for each capability.

</td></tr><tr><td>

Department

</td><td>

Department that is associated with the selected business application.

</td></tr><tr><td>

Leaf Node

</td><td>

This field denotes whether the business capability is a parent of any other capability. If the option is enabled, then it means that it doesn’t have child capability.Capabilities follow a parent-child hierarchy. The Leaf node attribute in the capability denotes that it isn’t a parent of any other capability.

 **Note:** The system updates the field and the user can’t.

</td></tr><tr><td>

Owned by

</td><td>

User who owns the business capability.

</td></tr><tr><td>

Hierarchy ID

</td><td>

Hierarchy ID of the business capability. For level 0 capability, a hierarchy ID is generated based on the order. For all non-root capabilities, the hierarchy ID is generated based on the hierarchy ID of its parent. The number is prefixed to the business capability and you can view it in the capability hierarchy map.The capabilities are structured vertically according to their hierarchy IDs. Whenever a capability is updated such as if a parent is added or deleted, then the hierarchy ID is automatically updated.

 **Note:** By default, the system updates the field. So, you can’t edit the field.

However, if you prefer a different number or value for the hierarchy ID from what the system generates, you can reset the system property flag to **True**. Setting the property to true makes the **Hierarchy ID** field editable in the Business Capability form and you can enter the value. By this action, the system default logic of generating the hierarchy ID is overridden by your custom hierarchy ID.

</td></tr><tr><td>

Description

</td><td>

A short description of the business capability.

</td></tr></tbody>
</table>**Parent Topic:**[Enterprise Architecture \(formerly Application Portfolio Management\) reference](apm-reference.md)

**Related topics**  


[Create business capability and relate the capability with an application](../task/create-a-business-capability.md)


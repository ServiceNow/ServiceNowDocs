---
title: Example: Bind alerts to CIs using dynamic CI types
description: Use event field mapping to dynamically bind alerts to the appropriate CIs based on event attributes, eliminating the need for separate event rules for each CI type \(also known as CI class\). This approach simplifies configuration, improves accuracy, and enhances alert to CI binding.
locale: en-US
release: australia
product: Event Management
classification: event-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Overriding default binding, Binding alerts to CIs, Event rules, Processing Events, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Example: Bind alerts to CIs using dynamic CI types

Use event field mapping to dynamically bind alerts to the appropriate CIs based on event attributes, eliminating the need for separate event rules for each CI type \(also known as CI class\). This approach simplifies configuration, improves accuracy, and enhances alert to CI binding.

## Before you begin

Role required: evt\_mgmt\_admin

## About this task

In general, for an event generated from a specific source mentioned in the **Source** field, the system applies the corresponding event rule. The override default binding option in an event rule specifies a specific CI class for binding. However, in a more dynamic use case, the CI class is not predefined and can change based on event attributes. For example, suppose a customer has multiple CIs with the same name, but each CI belongs to a different CI class. In the traditional event rule method, as the CI class \(or the CMDB table\) is defined for a CI, the mapping is incorrect because the system searches in the same CI class for all CIs with the same name and attributes, instead of looking in the specific CMDB table defined for each CI class.

To resolve this—in other words, to determine the correct CI class to search—the system uses the **CI type** field from the event to identify the CI class. By using an event field mapping that maps from event attributes to CI type, it becomes possible to know which CMDB table to search, ensuring that the CI is correctly mapped to the event.

## Procedure

1.  Navigate to **All** &gt; **Event Management** &gt; **Rules** &gt; **Event Field Mapping**.

    ![Event Field Mapping page.](../image/em-example-dynamic-ci-type-oracle-cloud.png)

2.  Select **Oracle Cloud**.

    This is an existing event field map used as an example. The event field map details page opens.

    ![Event Field Mapping details page for Oracle Cloud.](../image/em-example-dynamic-ci-type.png)

3.  Review the event field mapping details page and understand the relevant fields and their corresponding values.

<table id="table_EventFieldMappingForm"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Event field map name.

</td></tr><tr><td>

Source

</td><td>

Event monitoring software that generated the event. In this case, oraclecloud.

</td></tr><tr><td>

Order

</td><td>

Number to define the order in which this action should be processed. Actions with lower numbers are processed first.

</td></tr><tr><td>

Mapping type

</td><td>

Select **Map field and transform value \(Single field\)**.

</td></tr><tr><td>

Source field

</td><td>

**resourceType** is a field that is defined in the **Additional Information** field of the event defined by the Oracle Cloud system. The possible values of **resourceType** are listed in the **From value** column, while the corresponding CMDB tables for those values are specified in the **To value** column in the Transform value pairs section.

 If **resourceType** is **instance**, the system searches in the \[cmdb\_ci\_vm\_object\] table for CI binding.

</td></tr><tr><td>

Target field

</td><td>

The **CI type** field \(**ci\_type**\) in an event is a special field that provides the CI class name, indicating which CMDB table to search. The **CI type** field values are listed in the **To value** column in the Transform value pairs section.

</td></tr><tr><td class="sub-head" colspan="2">

Transform value pairs

</td></tr><tr><td>

From value

</td><td>

Lists the possible values of the event field \(e.g., `resourceType`\) that are derived from the event data.

</td></tr><tr><td>

To value

</td><td>

Specifies the corresponding CMDB table associated with each value listed in the **From value** column.Indicates the CI type to bind the alert to.

</td></tr></tbody>
</table>

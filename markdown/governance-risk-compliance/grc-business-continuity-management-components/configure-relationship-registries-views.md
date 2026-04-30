---
title: Configure 360° relationship registries and views
description: Configure 360° view configurations with the sn\_bcm.admin role.
locale: en-US
release: xanadu
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configure, Business Continuity Management, Governance, Risk, and Compliance]
---

# Configure 360° relationship registries and views

Configure 360° view configurations with the sn\_bcm.admin role.

## Before you begin

Role required: sn\_bcm.admin

## Procedure

1.  Navigate to **All** &gt; **360° View Configurations** &gt; **Configure 360° Views**.

2.  To configure the relationships for the records, navigate to **360° View Configurations** &gt; **Relationship Registries**.

    The form is shown in the example.

    ![Registry.](../image/360-rel-reg-new.png)

3.  On the form, fill in the fields.

<table id="table_epy_qrq_f5"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

A descriptive name for this registry.

</td></tr><tr><td>

Table

</td><td>

The table for which you want to define a relationship.

</td></tr><tr><td>

Relationship type

</td><td>

The type of relationship you are defining:-   One-to-many
-   Many-to-many
-   Scripted: a custom relationship from the ServiceNow AI Platform
-   One-to-one: any relationship that is available as a field in the selected table


</td></tr><tr><td>

Active

</td><td>

Select if the relationship is active.

</td></tr><tr><td>

Relationship

</td><td>

The relationship table of the selected relationship type. For example, if you are defining relationships for the Entity table and select a many-to-many relationship type, the list of relationship tables consists of all many-to-many relationships that apply to the Entity table.

</td></tr><tr><td>

Relationship table

</td><td>

The table name you selected in the **Relationship** field.

</td></tr></tbody>
</table>4.  Select **Submit**.

5.  To configure 360° views for the records, navigate to **360° View Configurations** &gt; **Configure 360° Views**.

    The form is shown in the example.

    ![360° Views.](../image/360-views.png)

6.  Save the record.

    The Relationship Registries related list appears.

    ![Relationship registries](../../grc-360-degree-rel-vis/image/relationship-registry.png "Relationship registries")

7.  Choose **Select Relationships**.

8.  On the form, fill in the fields.

<table id="table_lsf_x52_qqb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

A name to identify this relationship.

</td></tr><tr><td>

Data relationship

</td><td>

The data relationship you previously defined.

</td></tr><tr><td>

Relationship table

</td><td>

The table associated with the selected data relationship.

</td></tr><tr><td>

Node position

</td><td>

The sector you previously defined to which you want to add this relationship.

</td></tr><tr><td>

Filter

</td><td>

Enter conditions to define the types of relationships you want to display. For example, you could define conditions for all controls with failures.

</td></tr><tr><td>

Configuration

</td><td>

The configuration defined for the relationship.

</td></tr><tr><td>

Table

</td><td>

The table defined for the relationship.

</td></tr><tr><td>

Order

</td><td>

Based on the **Order** value given the position of element in the 360º view will change.

 For example, if you change the order value from 0 to 1 for an element, the position will be moved to next in the 360ºview.

</td></tr></tbody>
</table>9.  Select **Submit**.

    The new view you have defined is now available on the 360º view.

    ![Select a new view](../../grc-360-degree-rel-vis/image/new-view.png "Selecting a new view")

    For more information on 360° views configurations, see [Configure 360º views](../../grc-360-degree-rel-vis/concept/set-up-360-data-reg.md#).



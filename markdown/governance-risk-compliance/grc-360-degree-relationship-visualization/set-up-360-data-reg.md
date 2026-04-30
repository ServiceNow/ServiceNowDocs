---
title: Setting up the 360º views
description: To effectively use the 360° Relationship Visualization application, you need to register existing relationships between the types of data you want to view, and then configure how the 360º view displays that data.The first step in setting up your data registry is to register the relationships you want displayed in the 360° Relationship Visualization.These screen shots illustrate the various relationship types you can register.After the data registry has been defined, you can configure the 360° Relationship Visualization to effectively display the relations you created.
locale: en-US
release: xanadu
product: GRC: 360 Degree Relationship Visualization
classification: grc-360-degree-relationship-visualization
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [360° Relationship Visualization, Common GRC features, Governance, Risk, and Compliance]
---

# Setting up the 360º views

To effectively use the 360° Relationship Visualization application, you need to register existing relationships between the types of data you want to view, and then configure how the 360º view displays that data.

**Parent Topic:**[360° Relationship Visualization](grc-360-deg-rel-vis.md)

## Register 360º relationships

The first step in setting up your data registry is to register the relationships you want displayed in the 360° Relationship Visualization.

### Before you begin

Role required: Data registry administrator

### Procedure

1.  Navigate to **360º View Configurations** &gt; **Relationship Registries**.

    ![Relationship Registries](../image/relationship-registries.png "Relationship registries")

2.  Click **New**.

    ![New relationship registry](../image/relationship-registry-new.png "New relationship registry")

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
</table>4.  Click **Submit**.

5.  Repeat this process for all of the relationships you want to appear in the 360° Relationship Visualization interface.


### 360º relationship examples

These screen shots illustrate the various relationship types you can register.

#### One-to-many relationship

![One-to-many relationship](../image/example-one-to-many.png "One-to-many relationship")

#### Many-to-many relationship

![Many-to-many relationship](../image/example-many-to-many.png "Many-to-many relationship")

#### Scripted relationship

![Scripted relationship](../image/example-scripted.png "Scripted relationship")

#### One-to-one relationship

![One-to-one relationship](../image/example-one-to-one.png "One-to-one relationship")

## Configure 360º views

After the data registry has been defined, you can configure the 360° Relationship Visualization to effectively display the relations you created.

### Before you begin

Role required: Data registry administrator

### About this task

Multiple 360° Relationship views can be configured for a table. For example, the Entity table can be configured with multiple views, such as Compliance view, Risk view, Audit view, and others.

### Procedure

1.  Navigate to **360º View Configurations** &gt; **Configure 360º Views**.

    ![Configure a 360º view](../image/config-360-views.png "Configure a 360º view")

2.  Click **New**.

    ![New 360º view](../image/new-360-views.png "Configure a new 360º view")

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |View|A descriptive name for this view.|
    |Table|The table for which you want to define the view.|
    |Default|Select if this is the first view you are defining or your only view.|
    |Active|Select if this 360º view is active.|
    |Primary field and secondary field|The primary and secondary fields in the selected table to be used to display the title and secondary title of the main object, as illustrated.![Primary and secondary fields](../image/main-object.png)|
    |Description|A description of the 360º view.|
    |Section Configuration|
    |Sector configuration|Select the number of sectors to be displayed in the 360º view. For example, select `top, bottom, left, and right` to indicate you want four sectors.|
    |Top, Bottom, Left, Right|Based on your **Sector configuration** selection, enter labels for each of the sectors.|

4.  Save the record.

    The Relationship Registries related list appears.

    ![Relationship registries](../image/relationship-registry.png "Relationship registries")

5.  Click **Select Relationships**.

6.  On the form, fill in the fields.

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
</table>7.  Click **Submit**.

    The new view you have defined is now available on the 360º view.

    ![Select a new view](../image/new-view.png "Selecting a new view")



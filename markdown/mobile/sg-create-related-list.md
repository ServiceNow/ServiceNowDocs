---
title: Create a parametrized data item for your related list
description: Create a parametrized data item to contain the records that display in your related list.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configure a related list screen, Record screen, Mobile screen types, Mobile screens, Mobile app components, Building mobile apps, Mobile Platform]
---

# Create a parametrized data item for your related list

Create a parametrized data item to contain the records that display in your related list.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Mobile** &gt; **Mobile App Builder**.

    The Mobile App Builder appears in a new browser tab and displays the application scope selection screen.

2.  Search for the application scope you're working in and then select the name of the application scope.

    The Mobile App Builder categories home screen displays.

3.  From the menu on the left side, select **Data** to display the data items for the scope.

4.  Click the **New** button next to the **Search** field.

5.  In the **Create a data item** window, select **Data item**, then click **Continue**.

    A new data item control panel opens.

6.  In the **New data item** panel, fill in these fields.

<table id="table_m2q_stp_twb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the data item

</td></tr><tr><td>

Description

</td><td>

Brief description of the data item

</td></tr><tr><td>

Table

</td><td>

Table containing the records for your data item. **Note:** This is the table that contains records that appear in the related list, not the table for the record the list appears on. For example, if you want a list of incidents associated with a problem record, you would choose `Incident [incident]`, not `Problem [problem]`

.

</td></tr><tr><td>

Group by

</td><td>

Field which the records are grouped by. \(Optional\)

</td></tr><tr><td>

Condition type

</td><td>

Whether the condition is **Declarative**, uses a **Script** or uses an **Appended coded query**.

</td></tr></tbody>
</table>7.  Create parameter items in the **Parameters** section.

    Parameters contain values from the parent record that you can use in your conditions in the **Condition** section. You use these parameters in your condition to define how the related list records are related with the parent record. For more information on parameters, see [Configure a parametrized data item](sg-config-parametrized-data-item.md).

8.  Create a condition in the **Condition** section to filter the records that appear in your related list.

    Include parameters created in the **Parameters** section using the **Choose a parameter** \(![Choose parameter icon](../image/choose-parameter.png)\) icon.

9.  Create a separate condition in the **Offline condition** section.

    The conditions in this section apply when you set the app to offline mode.

10. Click **Save** in the upper right corner to save your data item.


## Example

In this example, you have a record screen that displays a problem record. On this screen, you wan to display a list of incidents associated with that problem. Since this related list contains incident records, you must create a data item for the Incident \[incident\] table.![Data item form](../image/example-data-parm-3.png)

For the data item to show only incidents related to the parent record \(a problem record in this case\), we must create a data parameter for that information. To make it easy to identify, the parameter name is `Problem data parameter`. Since records are identified with a sys\_id, the data parameter is a `String` type.![Data parameter form](../image/example-data-parm.png)

In the condition section of the data item, create a condition for the **Problem** field on incident records. Use the parameter as the value. You select the parameter using the **Choose a parameter** \(![Choose parameter icon](../image/choose-parameter.png)\) icon. Once these steps are taken, your data item is ready to use.![Completed parametrized data item](../image/example-data-parm-2.png)


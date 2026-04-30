---
title: Set up a ribbon configuration in CSM Configurable Workspace
description: Create a ribbon setting and add that setting to a ribbon configuration for CSM Configurable Workspace.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Set up CSM Configurable Workspace, CSM Configurable Workspace, Organize agent workspaces, Configuring Customer Service Management, Customer Service Management]
---

# Set up a ribbon configuration in CSM Configurable Workspace

Create a ribbon setting and add that setting to a ribbon configuration for CSM Configurable Workspace.

## Before you begin

Role required: workspace\_admin, ui\_builder\_admin, admin

## About this task

Use the steps in this task to set up a ribbon configuration for CSM Configurable Workspace.

-   Create a ribbon setting, such as creating another version of the Customer 360 ribbon component.
-   Add the ribbon setting to a ribbon configuration.
-   Set the width and the order of the ribbon setting within the ribbon configuration.

**Note:** You can also use ribbon settings from CSM Agent Workspace in CSM Configurable Workspace if you add the setting to the ribbon configuration.

One ribbon configuration, **CSM/FSM Configurable Workspace Ribbon Config**, is included with CSM Configurable Workspace. This configuration includes the Customer 360, Timeline, and Active SLA ribbon components. You can use this configuration out of the box without completing any additional configuration steps.

## Procedure

1.  Create a ribbon setting.

    1.  Navigate to **Now Experience Framework** &gt; **Configuration Settings** &gt; **UX Ribbon Setting**.

    2.  Click **New**.

    3.  Fill in the fields on the Ribbon Setting form.

<table id="table_os4_3hp_s3b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

A label that describes this ribbon setting. It often includes the table associated with this ribbon.

</td></tr><tr><td>

Ribbon component

</td><td>

The component to add to the ribbon setting, including Customer360, Timeline, Active SLA or a custom ribbon component. **Note:** You can only add one component at a time. To make a second component appear in the ribbon, repeat this procedure to create another ribbon setting and add a different component.

</td></tr><tr><td>

Table

</td><td>

The table associated with this ribbon setting. Any time an agent selects a record from this table, the ribbon setting appears with this component.

</td></tr><tr><td>

Width

</td><td>

The number of columns that the component occupies in the ribbon. The width of the page is 12 columns. When using multiple components, the total combined width of all the components must equal 12 or less.**Note:** For CSM Configurable Workspace, set the width of the ribbon component on the Ribbon Configuration Setting form \(see step 3\).

</td></tr><tr><td>

Application

</td><td>

The scope of this ribbon. Global means the ribbon works with all applications.

</td></tr><tr><td>

Order

</td><td>

The location of this component in the ribbon. Ordering the components goes from left to right. For example, if you associate three components with a table, the component with the lowest order appears on the left and the component with the highest order appears on the right.**Note:** For CSM Configurable Workspace, set the order of the ribbon component on the Ribbon Configuration Setting form \(see step 3\).

</td></tr><tr><td>

Active

</td><td>

Toggle to turn this component on or off in the ribbon for this table.

</td></tr><tr><td>

Inherit

</td><td>

If set to true, the ribbon configuration can be inherited by child tables. For this to be effective, a child table should not have any configured ribbon settings. The **Inherit** field is false by default.

</td></tr><tr><td>

Experience restricted

</td><td>

If set to true, the ribbon component is restricted to Configurable Workspaces.

 If set to false, the ribbon component is global and appears in CSM Agent Workspace \(legacy\). For more information, see Set up ribbons in workspace .

 This field is set to true by default.

</td></tr></tbody>
</table>    4.  Click **Submit**.

2.  Create a ribbon configuration as a container for your ribbon setting.

    1.  Navigate to **Now Experience Framework** &gt; **Configuration Settings** &gt; **UX Ribbon Configurations**.

    2.  Select **New**.

    3.  Fill in the fields on the UX Ribbon Configuration form.

        |Field|Description|
        |-----|-----------|
        |Name|Unique name for this ribbon configuration.|
        |Application|The scope of this ribbon configuration. Global means the ribbon works with all applications.|
        |Active|Toggle to turn this component on/off in the ribbon for this table.|
        |Description|Short description of this ribbon configuration that displays in the UX Ribbon Configurations list.|

    4.  Select **Submit**.

3.  Add the ribbon setting to the ribbon configuration.

    1.  Navigate to **Now Experience Framework** &gt; **Configuration Settings** &gt; **Ribbon Configuration Settings**.

    2.  Select the configuration from the UX Ribbon Configurations list.

    3.  Fill in the fields on the Ribbon Configuration Setting form.

<table id="table_c54_bjf_ltb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Table

</td><td>

The table associated with this ribbon setting. Any time an agent selects a record from this table, the ribbon setting appears with this component.

</td></tr><tr><td>

Ribbon

</td><td>

The ribbon setting to add to the ribbon configuration.

</td></tr><tr><td>

Configuration

</td><td>

The desired ribbon configuration.

</td></tr><tr><td>

Application

</td><td>

The scope of this ribbon. Global means the ribbon works with all applications.

</td></tr><tr><td>

Order

</td><td>

The location of this component in the ribbon. Ordering the components goes from left to right. For example, if you associate three components with a table, the component with the lowest order appears on the left and the component with the highest order appears on the right.

</td></tr><tr><td>

Width

</td><td>

The number of columns the component occupies in the ribbon. The width of the page is 12 columns. When using multiple components, the total combined width of all the components must equal 12 or less.**Note:** The width is ignored if the ribbon is configured to display in the [contextual side panel](config-csm-display-header-in-sidebar.md).

</td></tr><tr><td>

Active

</td><td>

Toggle to turn this component on/off in the ribbon for this table.

</td></tr></tbody>
</table>    4.  Click **Submit**.


**Related topics**  


[bundle-platux.configure-service-workspace-ribbons]


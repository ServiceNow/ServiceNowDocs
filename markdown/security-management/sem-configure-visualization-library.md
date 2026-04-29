---
title: Configure Visualization library
description: The Visualization library lists the available widgets for the Findings view page and their additional details, such as, the current activation status, additional conditions, and other columns. Configure the visualization library to select the columns you want to view.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [configure visualization library]
breadcrumb: [Implement, Unified Security Exposure Management, Security Operations]
---

# Configure Visualization library

The Visualization library lists the available widgets for the Findings view page and their additional details, such as, the current activation status, additional conditions, and other columns. Configure the visualization library to select the columns you want to view.

## Before you begin

Role required: See [Access control lists \(ACLs\) for administration rules](../../security-exposure-management-administration/concept/sem-acls-for-admin-rules.md)

## Procedure

1.  Navigate to **Workspaces** &gt; **Security Exposure Management Workspace**.

2.  In the navigation pane, select **Administration**.

3.  Under **Others**, in the **Visualization library** tile, select **Review**.

4.  In Visualization library, select the **List Actions** icon, and then select **Edit columns**.

5.  Select the required columns from the **Available columns** pane, and select **OK**.

<table id="table_fvy_cp1_1gc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Active

</td><td>

Indicates whether the widget is available to add to a filter. The widgets are active by default. Users with the sn\_sec\_wf.manage\_admin\_rules role can deactivate the widgets by setting the value of **Active** to `False`.

</td></tr><tr><td>

Additional condition

</td><td>

Additional conditions added to the widget.

</td></tr><tr><td>

Class

</td><td>

The class that the record belongs to.

</td></tr><tr><td>

Created

</td><td>

The date when the record was created.

</td></tr><tr><td>

Created by

</td><td>

The user who created the record.

</td></tr><tr><td>

Findings table

</td><td>

The tables the widgets to fetch data.The widgets can fetch data from one or more of the following tables:-   Infrastructure vulnerability
-   Application vulnerability
-   Misconfigurations
-   Container vulnerability


</td></tr><tr><td>

Framework

</td><td>

The framework that the record applies to.

</td></tr><tr><td>

Group by

</td><td>

The column on the findings table which provides the score for the widgets or categorizes the data.

</td></tr><tr><td>

Tags

</td><td>

The tags assigned to the record during import

</td></tr><tr><td>

Updated

</td><td>

The date when the discovered Item record was updated.

</td></tr><tr><td>

Updated by

</td><td>

The user who updated the data.

</td></tr><tr><td>

Updates

</td><td>

The updates to the record.

</td></tr><tr><td>

Visualization group

</td><td>

The visualization group under which the widget is displayed in the carousel.

</td></tr><tr><td>

Visualization type

</td><td>

The visual format to represent the filtered data.

</td></tr><tr><td>

Widget name

</td><td>

The name of the widget.

</td></tr></tbody>
</table>
-   **[Create a custom widget](sem-create-widget.md)**  
Create a custom widget in the Security exposure management \(SEM\) workspace to visualize findings data that meets your organization’s reporting needs. This feature enables administrators to extend the default widgets in the visualization library by adding new widgets that reflect organization-specific risk and exposure metrics.
-   **[Update a widget](sem-update-widget.md)**  
Update a widget in the Visualization Library to modify its configuration or presentation. You can update attributes to refine how data appears in Findings dashboards and ensure that the visualizations stay relevant to your reporting needs.
-   **[Localize widget titles](sem-localize-widget-titles.md)**  
Update the widget title in the Messages \[sys\_ui\_message\_list\] table whenever you create a custom widget or rename an existing one to ensure it displays correctly in localized interfaces.


---
title: Configure the standard ticket page
description: Give Service Portal users a consistent way to view their submitted requests. You can configure the standard ticket page for different request types.
locale: en-US
release: xanadu
product: Service Portal
classification: service-portal
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Standard ticket page, Creating portal pages, Configuring Service Portal, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Configure the standard ticket page

Give Service Portal users a consistent way to view their submitted requests. You can configure the standard ticket page for different request types.

## Before you begin

Role required: admin or sp\_admin

## About this task

You can add a standard ticket configuration only for a task-extended table.

Widgets containing **Date/Time** values display the date and time only in the **Time Ago** \(for example, 11 minutes ago\) format, and user preferences for such widgets are not considered. For example, the **Created date** and the **Updated date** values are always displayed in the **Time Ago** format.

## Procedure

1.  Navigate to **All** &gt; **Standard Ticket** &gt; **Standard Ticket Configuration**.

2.  Click **New**.

3.  On the form, fill in the fields.

<table id="table_nsc_wyx_2mb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Table

</td><td>

Task-extended table for which you want to configure the standard ticket page.

</td></tr><tr><td>

Active

</td><td>

Option to specify if the ticket configuration is active.

</td></tr><tr><td>

Application

</td><td>

Application associated with the ticket configuration.

</td></tr><tr><td>

State field

</td><td>

Any field of the task-extended table. By default, this field is mapped to the **State** field of the task-extended table. You have to configure the form to add this field.**Note:** You cannot add fields for any of the following information:

-   Number
-   Short description
-   Created date
-   Updated date
-   Watch list
-   Any user input such as comments and work notes


</td></tr><tr><td class="sub-head" colspan="2">

Info Region

</td></tr><tr><td>

Show 'Description'

</td><td>

Scenario when the request description should be displayed. Possible options are:-   None
-   Always
-   When no variables
 **Note:** When displayed, you can expand and collapse the description.

</td></tr><tr><td>

Advanced

</td><td>

Option to specify that a widget should be displayed in the info region.

</td></tr><tr><td>

Info widget

</td><td>

Widget that should be displayed in the info region. This field appears only when the **Advanced** check box is selected.

</td></tr><tr><td>

Info widget parameters

</td><td>

Name value pair to specify the widget parameters. This field appears only when the **Advanced** check box is selected.

</td></tr><tr><td>

Info fields

</td><td>

Fields that should be displayed in the info region. This field disappears when you select the **Advanced** check box.**Note:**

-   You cannot add fields for any of the following information:
    -   Number
    -   Short description
    -   Created date
    -   Updated date
    -   Watch list
    -   State
    -   Any user input such as comments and work notes
-   A field of the Workflow type is not supported for any table. Only for the Requested Item \[sc\_req\_item\] table, the Workflow type field is supported, for example, the **Stage** field. This field is displayed at the last irrespective of the field position in the configuration.


</td></tr><tr><td class="sub-head" colspan="2">

Action Region

</td></tr><tr><td>

Action widget

</td><td>

Widget to specify the actions available in the Action region.

</td></tr><tr><td>

Action widget parameters

</td><td>

Name value pair of action widget parameters.

</td></tr></tbody>
</table>4.  Right-click the header menu and click **Save**.

5.  From the Tab Configurations related list, click **New**.

    **Note:**

    -   By default, the Activity and Attachments type tab configurations are available for all standard configurations. Other default tab configurations may vary based on the task-extended table. For example, for the sc\_req\_item configuration, the Variable Editor \(Read-Only\) type is also available.
    -   You cannot duplicate any tab type other than Custom.
    -   You can configure a maximum of six tabs.
    -   You can add either Variable Editor \(Read-Only\) or the Variable Summarizer tab type.
6.  On the form, fill in the fields.

<table id="id_kl3_yk2_g5b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Type

</td><td>

Tab type based on which a widget is displayed. Possible options are:-   Activity
-   Associated Requests
-   Attachments
-   Custom
-   Variable Editor \(Read-Only\)
-   Variable Summarizer


</td></tr><tr><td>

Tab name

</td><td>

Name of the tab.

</td></tr><tr><td>

Application

</td><td>

Application associated with the ticket configuration.

</td></tr><tr><td>

Order

</td><td>

Order in which the tab should be displayed in the tabs section. The tab with the least order is the tab selected on the page load.

</td></tr><tr><td>

Advanced

</td><td>

Option to enable adding a script for the tab visibility. By default, this check box is cleared.

</td></tr><tr><td>

Visible\(Script\)

</td><td>

Script for the tab visibility.-   If the script returns true, the tab is visible on the standard ticket page.
-   If the script returns false, the tab is not visible on the standard ticket page.
 **Note:** This field appears only when the **Advanced** check box is selected.

</td></tr><tr><td>

Visible

</td><td>

Conditions for the tab visibility. This is not displayed if the **Advanced** check box is selected.

</td></tr><tr><td>

Widget

</td><td>

Widget that should be displayed in the tabs section. This field appears only when **Custom** is selected from **Type**.

</td></tr><tr><td>

Widget parameters

</td><td>

Comma-separated list of tab widget parameters. This field appears only when **Custom** is selected from **Type**.

</td></tr></tbody>
</table>7.  Click **Submit**.

8.  On the Ticket Configuration form, click **Update**.


-   **[Enable instance options for the Activity tab](enable-instanceop-activity.md)**  
Format the work notes and add @mentions in the Activity tab on a standard ticket page.

**Parent Topic:**[Standard ticket page](../concept/standard-ticket-page.md)


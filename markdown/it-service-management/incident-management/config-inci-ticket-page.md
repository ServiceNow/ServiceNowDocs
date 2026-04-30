---
title: Configure incident ticket page
description: Configure the Incident ticket page from where users can view the details of an Incident in Service Portal.
locale: en-US
release: xanadu
product: Incident Management
classification: incident-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Incident standard ticket page, Manage, Incident Management, IT Service Management]
---

# Configure incident ticket page

Configure the Incident ticket page from where users can view the details of an Incident in Service Portal.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Standard Ticket** &gt; **Standard Ticket Configuration** &gt; **Incident**.

2.  Click the Incident record.

3.  On the form, configure the fields.

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

Scenario where the request description should be displayed. Possible options are:-   None
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

Comma-separated list of info widget parameters. This field appears only when the **Advanced** check box is selected.

</td></tr><tr><td>

Info fields

</td><td>

Fields that should be displayed in the info region. This field disappears when you select the **Advanced** check box.**Note:** You cannot add fields for any of the following information:

-   Number
-   Short description
-   Created date
-   Updated date
-   Watch list
-   State
-   Any user input such as comments and work notes


</td></tr><tr><td class="sub-head" colspan="2">

Action Region

</td></tr><tr><td>

Action widget

</td><td>

Widget to specify the actions available in the info region.

</td></tr><tr><td>

Action widget parameters

</td><td>

Comma-separated list of action widget parameters.

</td></tr></tbody>
</table>    **Note:**

    -   By default, the Activity and Attachments type tab configurations are available for all standard configurations.
    -   You cannot duplicate any tab type other than Custom.
    -   You can configure a maximum of five tabs.
    -   You can add only one of these tab types:
        -   Variable Editor \(Read-Only\)
        -   Variable Summarizer
4.  Right-click the header menu and click **Save**.

5.  On the Tab Configurations related list, configure the fields.

<table id="table_wdz_fcy_2mb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Type

</td><td>

Tab type based on which a widget is displayed. Possible options are:-   None
-   Activity
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

Order in which the tab should be displayed in the tabs section.

</td></tr><tr><td>

Visible

</td><td>

Conditions for the tab visibility.

</td></tr><tr><td>

Widget

</td><td>

Widget that should be displayed in the tabs section. This field appears only when **Custom** is selected from **Type**.

</td></tr><tr><td>

Widget parameters

</td><td>

Comma-separated list of tab widget parameters. This field appears only when **Custom** is selected from **Type**.

</td></tr></tbody>
</table>6.  On the Ticket Configuration form, click **Update**.



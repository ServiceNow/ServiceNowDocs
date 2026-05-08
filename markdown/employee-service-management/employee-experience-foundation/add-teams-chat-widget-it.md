---
title: Add Microsoft Teams Chat widget
description: Add the Teams Chat widget to enable employees to view or continue chats with agents and view and access the content of attached files in the Employee Center.
locale: en-US
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Microsoft Teams Chat widget in Employee Center, IT Service Management integration, Microsoft Teams Integration for Employee Experience, Configure, ServiceNow for Microsoft Teams and Microsoft 365, Unified Employee Experience, Employee Service Management]
---

# Add Microsoft Teams Chat widget

Add the Teams Chat widget to enable employees to view or continue chats with agents and view and access the content of attached files in the Employee Center.

## Before you begin

Role required: sp\_admin

## Procedure

1.  Navigate to **All** &gt; **Standard Ticket** &gt; **Standard Ticket Configuration**.

2.  On the Ticket Configurations page, select **New**.

3.  On the Ticket Configuration form, fill in the fields.

    For more information about the field descriptions, see Configure the standard ticket page.

4.  Right-click the header menu and select **Save**.

5.  From the Tab Configurations related list, select **New**.

6.  On the Tab Configuration form, fill in the fields.

    Some fields require values specific to this task.

    -   For the **Type** field, select **Custom**.
    -   For the **Tab name** field, enter `Teams chat`.
    -   For the **Widget** field, search for and select **Teams Chat**.
<table id="id_tln_2vn_g5b"><thead><tr><th>

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
</table>7.  Select **Submit**.

8.  On the Ticket Configuration form, select **Update**.


## Result

A Teams Chat tab is added in each record of the Employee Center My Request page for the configured ticket type or table.

**Parent Topic:**[Microsoft Teams Chat widget in Employee Center](../concept/config-std-ticket-page-teams-it.md)


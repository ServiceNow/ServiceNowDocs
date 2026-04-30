---
title: Configure tabs for standard ticket page
description: You can configure the tabs for the standard ticket page.
locale: en-US
release: zurich
product: Service Portal
classification: service-portal
topic_type: task
last_updated: "2025-08-13"
reading_time_minutes: 2
breadcrumb: [Configure the standard ticket page, Standard ticket page, Creating portal pages, Configuring Service Portal, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Configure tabs for standard ticket page

You can configure the tabs for the standard ticket page.

## Before you begin

Role required: admin and sp\_admin

## About this task

-   By default, the Activity and Attachments type tab configurations are available for all standard configurations. Other default tab configurations may vary based on the task-extended table. For example, for the sc\_req\_item configuration, the Variable Editor \(Read-Only\) type is also available.
-   You can’t duplicate any tab type other than Custom.
-   You can configure a maximum of six tabs.
-   You can add either Variable Editor \(Read-Only\) or the Variable Summarizer tab type.

## Procedure

1.  Navigate to **All** &gt; **Standard Ticket** &gt; **Standard Ticket Configuration**.

2.  On the Ticket Configuration form, select the Tab Configurations related list.

3.  Select **New**.

4.  On the form, fill in the fields.

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
</table>5.  On the Ticket Configuration form, select **Update**.


**Parent Topic:**[Configure the standard ticket page](configure-st-page.md)

**Related topics**  


[Configure the standard ticket page](configure-st-page.md)

[Enable instance options for the Activity tab](enable-instanceop-activity.md)

[Configure actions for standard ticket page](configure-actions-for-standard-ticket-page.md)


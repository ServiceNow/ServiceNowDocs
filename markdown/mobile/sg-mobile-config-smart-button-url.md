---
title: Configure a smart button using a parametrized URL
description: Use parametrization to include record specific information in your smart buttons.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Smart button functions, Mobile functions, Mobile app components, Building mobile apps, Mobile Platform]
---

# Configure a smart button using a parametrized URL

Use parametrization to include record specific information in your smart buttons.

## Before you begin

Role required: admin

## About this task

This example demonstrates how parameters are used to improve the functionality of smart buttons. In this case, the smart button provides a link to a list of knowledge articles. The button uses the short description of the current incident as the search criteria for the knowledge article list.

Watch this two-minute video to learn how to find a relative link in your ServiceNow instance.Demonstrates how to find relative links in a ServiceNow instance

## Procedure

1.  Navigate to **All** &gt; **System Mobile** &gt; **Mobile App Builder**.

    The Mobile App Builder opens in a new browser tab and displays the application scope selection screen.

2.  Search for the application scope you are working in and then select the name of the application scope.

    The Mobile App Builder categories home screen displays.

3.  Select **Functions** from the menu and then select **New**.

4.  Complete the following fields.

<table id="table_acq_2pg_djb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Properties

</td></tr><tr><td>

Name

</td><td>

Name for your smart button. Enter `KB list`.

</td></tr><tr><td>

Description

</td><td>

Unique description for your smart button to make it easy to identify. For this example, enter `KB article list for current incident`.

</td></tr><tr><td>

Type

</td><td>

Type of smart button. Select **URL**.

</td></tr><tr><td>

Context

</td><td>

Whether the function uses the **Global** or **Record** context.

 Use **Record** context navigation functions in situations where the navigation depends on information from a record. For example, if you want to navigate from the **Assigned to** field in an incident record to the assignee's user record.

 Use **Global** context navigation functions in situations where the navigation does not depend on information from a record.

 For this example, select **Record**.

</td></tr><tr><td class="sub-head" colspan="2">

Data

</td></tr><tr><td>

Table

</td><td>

Specified a table where you want to use your smart button. Select **Incident \[incident\]**.

 **Note:** This conditionally shown when the **Context** is set to **Record**.

</td></tr><tr><td class="sub-head" colspan="2">

Settings

</td></tr><tr><td>

Take source value from field

</td><td>

This option enables using a specific field from a table as the source of the smart button type.

 Turn off this option by clearing the toggle.

</td></tr><tr><td>

Link URL

</td><td>

The URL to which your smart button navigates. Enter `sp?id=search&spa=1&t=kb&q={{short_description}}`.

</td></tr><tr><td>

Link Label

</td><td>

The visible label of your URL link. Enter `Show KB`.

</td></tr><tr><td>

Role access

</td><td>

Limit user access to an action by role.

</td></tr></tbody>
</table>5.  Select **Save**.


## Result

Tapping this button displays a list of knowledge base articles, using the short description for the incident as a search term.


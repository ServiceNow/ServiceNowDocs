---
title: Configure actions for standard ticket page
description: You can configure specific actions to be directly available on the standard ticket page. Requesters are able to initiate these actions. Scriptable APIs can also trigger these actions.
locale: en-US
release: zurich
product: Service Portal
classification: service-portal
topic_type: task
last_updated: "2025-08-13"
reading_time_minutes: 2
breadcrumb: [Configure the standard ticket page, Standard ticket page, Creating portal pages, Configuring Service Portal, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Configure actions for standard ticket page

You can configure specific actions to be directly available on the standard ticket page. Requesters are able to initiate these actions. Scriptable APIs can also trigger these actions.

## Before you begin

Role required: admin and sp\_admin

## Procedure

1.  Navigate to **All** &gt; **Standard Ticket** &gt; **Standard Ticket Configuration**.

2.  On the Ticket Configuration form, select the Standard Ticket actions related list.

3.  Select **New**.

4.  On the form, fill in the fields.

<table id="table_ytj_hz4_hgc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name the action you want to be on the page. For example, Resolve.

</td></tr><tr><td>

Application

</td><td>

Application associated with the ticket configuration.

</td></tr><tr><td>

Short description

</td><td>

Describe the action in detail. For example, for the Resolve action, you can specify “Marks the incident as resolved.”

</td></tr><tr><td>

Ticket configuration

</td><td>

Reference to the standard ticket configuration record. For example, incident.

</td></tr><tr><td>

Active

</td><td>

Select the check box if you want this action to be active.

</td></tr><tr><td>

Table

</td><td>

Name of the associated table. For example, Incident \[incident\].

</td></tr><tr><td>

Order

</td><td>

Order in which the action should be displayed in the actions section.

</td></tr><tr><td>

Advanced

</td><td>

Option to enable adding a script for the action visibility. By default, this check box is cleared.

</td></tr><tr><td>

Applicability script

</td><td>

Script for the action visibility.

-   If the script returns true, the action is visible on the standard ticket page.
-   If the script returns false, the action isn’t visible on the standard ticket page.
**Note:** This field appears only when the **Advanced** check box is selected.

</td></tr><tr><td>

Action script

</td><td>

Action script performs the specified action. For example, when the Resolve action is selected, actions script determines the next action.

</td></tr><tr><td>

Applicability condition

</td><td>

Conditions for the action visibility. This isn’t displayed if the **Advanced** check box is selected.

</td></tr><tr><td>

User input

</td><td>

Option to enable adding text input by users for the action. If you select this check box, and save the changes, you see a new Standard Ticket Action Inputs related list. You can create a new user input in this related list. For example, a user input where strings must be provided.**Note:** Only string-type input is supported for standard ticket actions.

</td></tr></tbody>
</table>5.  Select **Update**.


**Parent Topic:**[Configure the standard ticket page](configure-st-page.md)

**Related topics**  


[Configure the standard ticket page](configure-st-page.md)

[Enable instance options for the Activity tab](enable-instanceop-activity.md)

[Configure tabs for standard ticket page](configure-tabs-for-standard-ticket-page.md)


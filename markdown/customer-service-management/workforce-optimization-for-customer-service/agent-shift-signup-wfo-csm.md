---
title: Enable your teams to sign up for work shifts
description: Empower your teams to sign up for work shifts based on their availability and preference.
locale: en-US
release: zurich
product: Workforce Optimization for Customer Service
classification: workforce-optimization-for-customer-service
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Scheduling in Workforce Optimization for Customer Service, Using Workforce Optimization for Customer Service, Workforce Optimization for Customer Service, Customer Service Management]
---

# Enable your teams to sign up for work shifts

Empower your teams to sign up for work shifts based on their availability and preference.

## Before you begin

Role required: sn\_shift\_planning.admin

## About this task

When a schedule plan is enabled for sign-up, you can receive notifications. You can also receive notifications when the schedule plan that's open for sign up is due on the current day or when it's due soon.

**Important:** The maximum number of agents who receive notifications is controlled by the `glide.ui_notification.max_recipients` system property. Notifications are sent only up to the configured limit.

## Procedure

1.  Navigate to **All** &gt; **Workforce Optimization for CSM** &gt; **Manager Workspace**

2.  Select the Schedule icon \(![Schedule icon](../image/schedule-icon.png)\).

3.  Add a schedule plan.

    1.  Select the **Team Calendar** tab.

    2.  In the Contextual side panel, click the Show Schedules icon ![Show Schedules icon.](../image/show-schedules-icon.png) to display the schedules.

        **Tip:** Select the filter icon \(![Filter schedule](../image/show-filter-icon.png)\) and then select the desired sign-up state and sign-up dates to narrow down the schedule plans enabled for sign-up.

<table id="table_fnk_m3l_bvb"><thead><tr><th>

In the filters, to add the desired

</th><th>

Do this

</th></tr></thead><tbody><tr><td>

**Sign-up state**

</td><td>

1.  Double-click one or more sign-up states in the **Available** column to move them to the **Applied** column.
2.  Select **Apply**.


</td></tr><tr><td>

**Sign-up dates**

</td><td>

1.  Select a predefined option such as **Last 7 days** or select the start and end date for which you want to see the schedule plans enabled for sign-up.
2.  Select **Apply**


</td></tr></tbody>
</table>    3.  In the Schedules panel, select the + icon.

        You can duplicate an existing schedule to create another one. After you duplicate a schedule that has the shift sign up enabled, you can update the start date, end date, and the date for which the agents must sign up for the schedule.

        **Note:** If there are no agents associated with the schedule, then the shifts associated with the schedule aren’t duplicated.

    4.  Fill in the required fields on the form.

        The image below shows an example of a filled-in Schedule form.

        ![Create shift sign-up](../image/create-shift-signup.png)

    5.  To enable your agents to sign up for work shifts, do the following:

        1.  Enable the **Request Agent Signup** check box.
        2.  In the **Agents must sign-up by** field, enter the date by which they must sign up for shifts within that schedule.
        **Tip:** If your agents have signed up for their preferred shifts, the **Assigned To** field is auto-populated with those agents.

    6.  Select **Save schedule**.

4.  Add a work shift to the schedule plan.

    1.  Select the schedule plan you've created.

        The image below displays the schedule plan that was created.

        ![Select schedule for shift sign-up](../image/select-schedule-shift-signup.png)

    2.  Select **Add Shift**.

        The image below provides an example of a form to enter the details for a shift.

        ![Add shift sign-up](../image/add-shift-signup.png)

    3.  In the **Shift** field, select the work shift that you want to add to the schedule plan.

        **Note:** If the schedule plan has been enabled for agents to sign up for shifts, the following fields are automatically enabled:

        -   **Request agent sign-up**
        -   **Enable auto-assignment of agents**
        If you want to assign agents manually, you can disable these check boxes at any time.

    4.  If the shifts are enabled for sign-up, you can select **Send for signup**.

        All shifts that have been enabled for sign-up are sent to the agents to sign up for their shifts. You can select **Close sign-up** to close agent sign-up for a shift before the sign-up due date and manually assign the agents.

        -   The **Enabled for sign-up** highlighted label changes to **Closed for sign-up**.
        -   The system will automatically close the sign ups after the sign-up due date.
5.  Add agents to the work shifts.

<table id="choicetable_ejp_3fs_dvb"><thead><tr><th align="left" id="d133350e373">

To

</th><th align="left" id="d133350e376">

Do this

</th></tr></thead><tbody><tr><td id="d133350e382">

**Auto-assign agents**

</td><td>

Enable the **Enabled for auto-assignment for agents** check box. Your agents who have set the shift to be their top preference is auto-assigned. The number of shifts auto-assigned is based on the value set in the **sn\_shift\_planning.max\_shifts\_to\_autoassign** system property.

</td></tr><tr><td id="d133350e397">

**Assign agents manually**

</td><td>

1.  In the **Assign agents** field, search for agents and add one or more agents to add to the shift.
2.  To add agents who had signed up for shifts, select **+Add signed up agents**

You can view the agents who had signed up and their preferred ranking to work on that shift. If you don't want to display the agents who have already been assigned to a shift in that schedule plan, enable the **Hide agents already assigned to other shifts** toggle button.

**Note:** This option is only available after you've closed agent sign-ups for the shift.

3.  Select **Save selection**.


</td></tr></tbody>
</table>6.  Select **Save shift**.

    The state for the schedule plan changes to **Generating Preview**.

7.  To publish the schedule plan, select **Publish**.

    **Note:** It may take a few minutes for the screen to refresh.

    The table describes the different shift sign-up states in the schedule plan.

<table id="table_j1v_nsl_bvb"><thead><tr><th>

Schedule plan sign up state

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Sign-up not enabled

</td><td>

The schedule plan isn’t enabled for sign-up.

</td></tr><tr><td>

Enabled for sign-up

</td><td>

-   Schedule plan is enabled for sign-up but isn’t yet ready for agents to sign up for shifts.
-   Schedule plan can’t be published when enabled for sign-up.
 ​

</td></tr><tr><td>

Open for sign-up

</td><td>

-   Schedule plan is enabled for sign-up and is ready for agents to sign up.
-   Schedule plan can’t be published or deleted when it's open for sign-up.
-   When open for sign-up:
    -   The sign-up due date can’t be changed.
    -   The work shift details can’t be changed.
    -   New shifts can’t be added.
    -   If enabled for auto-assign, the agent assignment in a shift can’t be changed.


</td></tr><tr><td>

Closed for sign-up

</td><td>

Schedule plan is closed for agents to sign up.

</td></tr></tbody>
</table>
**Parent Topic:**[Scheduling in Workforce Optimization for Customer Service](../concept/scheduling-configurable-wfo-cs.md)


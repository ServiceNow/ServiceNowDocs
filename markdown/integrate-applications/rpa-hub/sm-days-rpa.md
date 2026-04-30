---
title: Scheduled maintenance days in RPA Hub
description: Track the scheduled maintenance \(SM\) days on the robot calendar so that the bot processes can function optimally. If an issue occurs, you can take preventive measures. For example, you can know in advance about the days when the robot or the bot process is unavailable so that you can avoid the number of skipped process jobs.
locale: en-US
release: zurich
product: RPA Hub
classification: rpa-hub
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 8
breadcrumb: [Explore, RPA Hub, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# Scheduled maintenance days in RPA Hub

Track the scheduled maintenance \(SM\) days on the robot calendar so that the bot processes can function optimally. If an issue occurs, you can take preventive measures. For example, you can know in advance about the days when the robot or the bot process is unavailable so that you can avoid the number of skipped process jobs.

## Scheduled maintenance days overview

A scheduled maintenance \(SM\) day is when a configuration item \(CI\), such as, a robot or a bot process, is unavailable for execution. When a change request for a robot or a bot process is accepted by the Robotic Process Automation \(RPA\) release manager or RPA admin to create a scheduled maintenance day. Then the robot or the bot process can’t be executed at that time.

An RPA support user, RPA developer, and RPA business user can view the scheduled maintenance days on the robot calendar. You can make sure that the RPA business user is also added to the Managed by Group list.

Scheduled maintenance days also apply to the robots that are in the robot pool.

## Benefits of scheduled maintenance days

With the scheduled maintenance days on the robot calendar, you get the following benefits:

-   Perform robot capacity planning with better visibility and rich visual plotting in a single view.
-   Optimize the robot utilization and avoid any potential issues related to scheduled maintenance windows.
-   Enables you to take proactive measures instead of being reactive for a configuration item \(robot or a bot process\).

## Workflow

In RPA Hub, a Change Request \(CR\) with details of planned start and end dates along with time is created. This CR reflects as a scheduled maintenance day on the robot calendar, only when the change request is either in Scheduled, Implement, or Review states. For more information about the CR states, see [State model and transitions](https://www.servicenow.com/docs/access?context=c_ChangeStateModel&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US).

An associated SM event card appears on the robot calendar to display the scheduled maintenance days.

See the following example for a snapshot of scheduled maintenance day event cards on the robot calendar.

![Snapshot of scheduled maintenance day event cards on robot calendar.](../image/sm-day-rpa.png "Scheduled maintenance day event cards on robot calendar")

RPA business users, RPA release managers, RPA support users, RPA developers, and RPA admins have visibility to the potential impacts of current or future automation executions. RPA release managers and RPA admins can take an appropriate call to action, such as, either accepting or rejecting an associated SM event card for the CI on the robot calendar.

If the SM event card is accepted, a Maintenance Request \(MR\) is created on the robot calendar, with Pending state.

See the following example for a snapshot of an accepted SM day event card on the robot calendar.

![Snapshot of an accepted scheduled maintenance day event card on the robot calendar.](../image/sm-day-after-accept.png "Snapshot of an accepted scheduled maintenance day event card on the robot calendar")

If the associated CI is in Published state, then the associated CI moves to In Maintenance state during the planned scheduled maintenance time frame. The executions are stopped until the CR is closed. Then, the CI automatically moves to the Published state.

See the following example for a snapshot of accepting the SM event card when the associated CI \(bot process\) is in Published state.

![Snapshot of accepting a scheduled maintenance event card on the robot calendar when the associated CI is in Published state.](../image/sm-accept-cr-rpa.gif "Accept a scheduled maintenance event card on the robot calendar")

If the SM event card is rejected, it does not reflect on the robot calendar. An MR is created with Rejected state.

You can view the maintenance request for tracking the state of the scheduled maintenance. For more information, see [View maintenance requests in RPA Hub](../task/view-mr-rpa.md) and [Maintenance request form in RPA Hub](../reference/mr-form-rpa.md).

For more information about managing scheduled maintenance days, see [Manage scheduled maintenance days in RPA Hub](../task/manage-sm-request-rpa.md).

## Mapping between a change request and a maintenance request

A one-to-one mapping exists between a Change Request \(CR\) and a Maintenance Request \(MR\). If an existing MR is mapped to a CR and you want to create an MR for the same CR. Then, you must cancel the previous MR and create an MR for the same CR. For example, if CR1 is mapped to MR1 \(CR1:MR1\). To create MR2, you must cancel MR1 and map CR1 to MR2 \(CR1:MR2\).

If multiple or duplicate CRs are created for the same CI, then the MRs are considered against any one CR. The RPA release manager takes the decision.

## Scheduled maintenance days behavior for various CR states

If the CR is in either Schedule, Implement, or Review states and the **Planned Start Date** and **Planned End Date** fields on the CR form are mentioned. Then, the scheduled maintenance day occurs as per these dates. The MR is updated in a sequence as follows:

-   An MR is created with Pending state.
-   The MR is then updated to In Progress state after the **Planned Start Date** is initiated.
-   The associated CI moves to In Maintenance state.

If the CR is in either Schedule, Implement, or Review states and the **Planned Start Date** field on the CR form is empty. Then, the SM day doesn’t reflect on the robot calendar and the existing MR isn’t executed.

If the CR is in either Schedule, Implement, or Review states and the **Planned End Date** field on the CR form is empty. For example, the **Planned Start Date** is January 21. Then, the SM day reflects for only one day starting from the planned start date until 11:59PM on the same day. An MR is created for January 21. The CI is in In Maintenance state till the CR is closed, even if the date passed. But the schedule maintenance does not reflect on the robot calendar after the end date passes.

If the CR is in either Schedule, Implement, or Review states, the **Planned Start Date** and **Planned End Date** fields on the CR form are empty. Then the SM day doesn’t reflect on the robot calendar and the existing MR isn’t executed.

If the CR is in either Schedule, Implement, or Review states and the **Planned Start Date** and **Planned End Date** on the CR form are rescheduled. Then, the scheduled maintenance is updated to the rescheduled date automatically. The previous MR is canceled and the RPA release manager creates an MR for the rescheduled date by accepting the SM event card.

If the **On Hold** option on the CR form is selected, then the SM day doesn’t reflect on the robot calendar and the existing MR isn’t executed.

If the CR of the respective CI isn’t in Closed state, however the CI is functional. Then, the RPA release manager can update the life cycle stage status of the CI to Published or In Use.

If the CR is closed, then the life cycle stage status of the respective CI is updated to Published or In Use.

If the CR is canceled and the MR is in Pending state, the MR isn’t executed. If the MR is picked for execution, then cancel the MR. For more information, see [Manage scheduled maintenance days in RPA Hub](../task/manage-sm-request-rpa.md).

If the CR is canceled and the MR is in In Progress state. Then, the life cycle stage status of the CI moves to Published state and the MR is updated to complete state.

The following table shows the scheduled maintenance days behavior for various CR states.

<table id="table_nrm_w3p_byb"><thead><tr><th>

CR State

</th><th>

Planned Start Date

</th><th>

Planned End Date

</th><th>

Rescheduled Planned Start Date

</th><th>

Rescheduled Planned End Date

</th><th>

Applicable for Scheduled maintenance

</th><th>

MR State

</th></tr></thead><tbody><tr><td>

Schedule/ Implement/Review

</td><td>

21-Jan

</td><td>

22-Jan

</td><td>

Empty

</td><td>

Empty

</td><td>

Yes.

</td><td>

MR is created for January 21. On January 21, it moves to In progress.The CI is updated to In Maintenance.

</td></tr><tr><td>

Schedule/ Implement/Review

</td><td>

Empty

</td><td>

22-Jan

</td><td>

Empty

</td><td>

Empty

</td><td>

SM day doesn’t reflect on the robot calendar.

</td><td>

Not executed.

</td></tr><tr><td>

Schedule/ Implement/Review

</td><td>

21-Jan

</td><td>

Empty

</td><td>

Empty

</td><td>

Empty

</td><td>

SM day reflects on January 21, until 11:59PM.But the schedule maintenance does not reflect on the robot calendar after the end date passes.

</td><td>

MR is created for January 21. CI is in In Maintenance state till the CR is closed, even if the date passed.

</td></tr><tr><td>

Schedule/ Implement/Review

</td><td>

Empty

</td><td>

Empty

</td><td>

Empty

</td><td>

Empty

</td><td>

SM day doesn’t reflect on the robot calendar.

</td><td>

Not executed.

</td></tr><tr><td>

Schedule/ Implement/Review

</td><td>

21-Jan

</td><td>

22-Jan

</td><td>

23-Jan

</td><td>

24-Jan

</td><td>

Scheduled maintenance is updated to the rescheduled date automatically.

</td><td>

The previous MR is canceled \(that is due on January 21. The RPA release manager creates an MR for the rescheduled date by accepting the SM event card.

</td></tr><tr><td>

**On Hold** option on the CR form is selected

</td><td>

21-Jan

</td><td>

22-Jan

</td><td>

Empty

</td><td>

Empty

</td><td>

SM day doesn’t reflect on the robot calendar.

</td><td>

Not executed.

</td></tr><tr><td>

Closed

</td><td>

21-Jan

</td><td>

22-Jan

</td><td>

Empty

</td><td>

Empty

</td><td>

Not applicable

</td><td>

The life cycle stage status of the respective CI is updated to Published or In Use

</td></tr><tr><td>

Canceled

</td><td>

21-Jan

</td><td>

22-Jan

</td><td>

Empty

</td><td>

Empty

</td><td>

Not applicable

</td><td>

If the MR is in Pending state, the MR isn’t executed.If the MR is picked for execution, then cancel the MR.

If the MR is in In Progress state. Then, the life cycle stage status of the CI moves to Published state and the MR is updated to complete state.

</td></tr></tbody>
</table>
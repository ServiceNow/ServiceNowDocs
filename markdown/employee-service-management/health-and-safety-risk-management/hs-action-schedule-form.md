---
title: Action schedule form for an exposure
description: The industrial hygienist can use the action schedule form for an action to be created when there's an active exposure.
locale: en-US
release: yokohama
product: Health and Safety Risk Management
classification: health-and-safety-risk-management
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Reference, Health and Safety Risk Management, Health and Safety, Employee Service Management]
---

# Action schedule form for an exposure

The industrial hygienist can use the action schedule form for an action to be created when there's an active exposure.

For information on setting up an action schedule for an exposure, see [Define an action schedule for affected people](../task/hs-define-action-schedule-affected-people.md).

<table id="table_ap1_wzv_zdc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Short description

</td><td>

Brief description about this action.

</td></tr><tr><td>

Active

</td><td>

Option for marking the action schedule available for use. An action schedule must be active for actions to be created and assigned to the affected people.

</td></tr><tr><td>

Location

</td><td>

Location that this action item applies to. The action is assigned to the affected people at this location.This field is automatically set to the location of the exposure assessment.

</td></tr><tr><td>

Type

</td><td>

Type of the action.-   **Corrective**: An action to eliminate the causes of non-conformities or undesirable situations to stop them from happening again.
-   **Preventive**: An action to help prevent the occurrence of non-conformities.
-   **Task**: A generic task assigned as an action.
-   **Learning**: An action that includes a learning for the user, for example, completing a training.

**Note:** The **Learning** option in this field appears only when the Learning Core \(sn\_lc\) application is installed on your instance. For more information, see [Additional features in Health and Safety](../../ohs-incident-management/task/install-hs-incident-mgmt.md#table_ix1_bff_gxb).


</td></tr><tr><td>

Learning material

</td><td>

Learning material for the training, for example, knowledge article or URL for a training video.This field appears only when **Learning** is selected from **Type**.

**Note:** This field lists the learning content created in Learning Core. For more information, see [Managing course and catalog content](../../human-resources/task/manage-ln-content.md).

</td></tr><tr><td>

Days to complete action after creation

</td><td>

Number of days by when this action should be complete after it's generated and assigned to a user.This field sets the due date of the assigned action.

</td></tr><tr><td>

This is recurring action

</td><td>

Option for marking this action as recurring.When this option is selected, the **Duration details** section and fields appear.

</td></tr></tbody>
</table>The following duration details section appears only when the action schedule is set as recurring.

<table id="table_ldh_dtb_12c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Frequency

</td><td>

Frequency at which the system generates an action record such as daily, weekly, or monthly.

</td></tr><tr><td>

Weekly

</td><td>

Weekday when the recurring action records should be generated. You can select which particular day of the week to generate action records for—The action doesn't have to be created every day in the week.

This field appears only when **Frequency** is set as **Weekly**.

</td></tr><tr><td>

Months to generate

</td><td>

Months when the recurring action records should be generated. You can select which particular months to generate action records for—The action doesn't have to be created every month.

This field appears only when **Frequency** is set as **Monthly**.

</td></tr><tr><td>

Day

</td><td>

Day of the selected month when the schedule should run to generate the recurring action records.If the selected month has fewer days, the schedule will run on the last day of the month.

This field appears only when **Frequency** is set as **Monthly**.

</td></tr></tbody>
</table>**Parent Topic:**[Health and Safety Risk Management reference](../concept/hs-risk-mgmt-reference.md)


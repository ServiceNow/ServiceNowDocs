---
title: Health and safety action schedule form
description: Safety team can use the action schedule form for actions to be created and assigned based on defined conditions.
locale: en-US
release: yokohama
product: Health and Safety Core
classification: health-and-safety-core
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Reference, Health and Safety Core, Health and Safety, Employee Service Management]
---

# Health and safety action schedule form

Safety team can use the action schedule form for actions to be created and assigned based on defined conditions.

For information on setting up a health and safety action schedule, see [Create a Health and Safety action schedule](../task/create-health-safety-action-schedule.md).

<table id="table_tzg_shc_y2c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Short description

</td><td>

Brief description about this action schedule.

</td></tr><tr><td>

Active

</td><td>

Option for marking the action schedule available for use.An action schedule must be active for actions to be created and assigned to people.

</td></tr><tr><td>

Location

</td><td>

Location that this action item applies to. The action is assigned to the people at this location.

</td></tr><tr><td>

Type

</td><td>

Type of the action.-   **Corrective**: An action to eliminate the causes of non-conformities or undesirable situations to stop them from happening again.
-   **Preventive**: An action to help prevent the occurrence of non-conformities.
-   **Task**: A generic task assigned as an action.
-   **Learning**: An action that includes a learning for the user, for example, completing a training.

**Note:** The **Learning** option in this field appears only when the Learning Core \(sn\_lc\) application is installed on your instance. For more information, see [Additional features in Health and Safety](../task/install-hs-incident-mgmt.md#table_ix1_bff_gxb).


</td></tr><tr><td>

Learning material

</td><td>

Learning material for the training, for example, knowledge article or URL for a training video.This field appears only when **Learning** is selected from **Type**.

**Note:** This field lists the learning content created in Learning Core. For more information, see [Managing course and catalog content](../../human-resources/task/manage-ln-content.md).

</td></tr><tr><td>

Days to complete action after creation

</td><td>

Number of days by when this action should be complete after it's generated and assigned to a user.This field sets the due date of the created action.

</td></tr><tr><td>

Assign to

</td><td>

Users with the Health and Safety profile the generated actions are assigned to.Use the **Set conditions** builder in this field to define the criteria for assigning this action to specific individuals. For more information, see [Create a Health and Safety action schedule](../task/create-health-safety-action-schedule.md).

</td></tr><tr><td>

This is recurring action

</td><td>

Option for marking this action as recurring.When this option is selected, the **Duration details** section and fields appear.

</td></tr></tbody>
</table>The following duration details section appears only when the action schedule is set as recurring.

<table id="table_mlc_yhc_y2c"><thead><tr><th>

 

</th><th>

 

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
</table>**Parent Topic:**[Health and Safety Core reference](../../hs-core/concept/hs-core-reference.md)

**Related topics**  


[Components installed with Health and Safety Core](../../hs-core/reference/components-installed-hs-core.md)

[Health and Safety action form](hs-action-form.md)

[Health and Safety profile form](hs-health-safety-profile-form.md)

[Health and Safety document version form](hs-document-form.md)

[Health and Safety report field mapping form](hs-report-field-mapping-form.md)

[Health and Safety meeting form](hs-safety-meeting-form.md)

[Health and Safety meeting attendee form](hs-safety-meeting-attendee-form.md)


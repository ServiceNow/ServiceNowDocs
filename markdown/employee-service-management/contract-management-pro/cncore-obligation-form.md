---
title: Obligation form
description: The obligation form provides the details to create or modify an obligation record in Obligation Management.
locale: en-US
release: xanadu
product: Contract Management Pro
classification: contract-management-pro
topic_type: reference
last_updated: "2024-09-14"
reading_time_minutes: 4
keywords: [Recurring obligation task, Recurring schedule]
breadcrumb: [Contract Management Pro reference, Contract Management Pro, Employee Service Management]
---

# Obligation form

The obligation form provides the details to create or modify an obligation record in Obligation Management.

<table id="table_jb1_f2v_rcc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

An auto-generated unique number for the obligation record.

</td></tr><tr><td>

Contract

</td><td>

Unique number of the contract repository record.

</td></tr><tr><td>

Name

</td><td>

Name of the obligation.

</td></tr><tr><td>

Category

</td><td>

Category of the obligation. The available values are:-   Operational or service delivery
-   Legal
-   Commercial
-   Compliance
-   Governance

</td></tr><tr><td>

Subcategory

</td><td>

Subcategory of the obligation.The available values depend on the selected category.

</td></tr><tr><td>

Active

</td><td>

Option to activate the obligation.If a recurring schedule has been defined for obligation tasks, activating the obligation creates obligation tasks based on the defined schedule.

</td></tr><tr><td>

Approver group

</td><td>

Group whose members have appropriate permissions to approve or reject an obligation task.

</td></tr><tr><td>

Approver

</td><td>

Member of the approver group assigned to approve the obligation tasks.

</td></tr><tr><td>

Task assigned to

</td><td>

User to whom the obligation tasks will be assigned by default. This value can be overridden by assigning a user once the obligation task is created. A notification email is sent to the assigned user.

</td></tr><tr><td>

Start date

</td><td>

Date from which the obligation will be in effect.

</td></tr><tr><td>

End date

</td><td>

Date on which the obligation ends.

</td></tr><tr><td>

Instructions

</td><td>

Actions that must be performed as part of the obligation.

</td></tr><tr><td>

Description

</td><td>

Extract from the contract that describes the obligation.

</td></tr><tr><td>

Schedule type

</td><td>

Schedule type of the obligation tasks.-   **Adhoc**

Obligation must be fulfilled once or at irregular intervals. You must create obligation tasks manually.

-   **Recurring**

Obligation must be fulfilled regularly at a defined interval. Obligation tasks are automatically created based on the interval specified in the **Repeats** field and according to the value in the **Task creation lead time \(days\)** field.


</td></tr><tr><td>

Repeats

</td><td>

This field appears only when **Recurring** is selected from the **Schedule** field.

 **Note:** For monthly or yearly repeats, the first obligation task is due on the selected date and recurring obligation tasks are due on the same day of the month or year as the initial value. For example, if you select 2024-08-10 as the **Due date** value, the first obligation task will be due on the 10th of August 2024 and the subsequent tasks will be due on the 10th day of the month in the specified interval or on that date every year. If you select the 31st day of a month as the **Due date** value, the obligation tasks for months with less than 31 days will be due on the last day of that month.

 The available values are:

-   **Daily** - Obligation tasks are created daily and are due every day between the start date and end date of the obligation record.
-   **Weekly** - Obligation tasks are created every week. The value in the **Repeats** field that appears when this value is selected determines the days of the week when the obligation tasks should be fulfilled.
-   **Monthly** - Obligation tasks are created once a month and are due on the day of the month specified in the **Due date** field that appears when this value is selected.
-   **Every three months** - Obligation tasks are created every three months and are due on the day of the month specified in the **Due date** field that appears when this value is selected.
-   **Every six months** - Obligation tasks are created once a month and are due on the day of the month specified in the **Due date** field that appears when this value is selected.
-   **Yearly** - Obligation tasks are created once a year, with the first obligation task being due on the selected date and recurring obligation tasks due on the same date every year.

</td></tr><tr><td>

Task creation lead time \(days\)

</td><td>

This field appears only when **Recurring** is selected from the **Schedule** field. It determines the number of days before the task’s due date when the obligation tasks should be automatically created.

</td></tr></tbody>
</table>**Parent Topic:**[Contract Management Pro reference](../concept/cncore-ref.md)

**Related topics**  


[Components installed with Contract Management Pro](cncore-comp-ccore.md)

[Components installed with Contract Workspace](cncore-comp-contract-workspace.md)

[Components installed with Analytics Pack for Contract Management Pro](cncore-comp-analytics-pack-cmpro.md)

[Clause Variation form](cncore-cv-form.md)

[Contract Configuration form](cncore-contract-config-form.md)

[Properties installed to configure expiry notifications](cncore-properties-installed.md)

[Properties installed to configure contracts integrations](cncore-properties.md)

[Expiring Contracts Condition form fields](cncore-email-notif-expcont-form.md)

[Contract Management Pro states and status](cncore-request-states.md)

[Action assignment form](cmpro-actn-assignment-form.md)

[UFX Add on Event mapping form](cmpro-ufx-event-map-form.md)

[Obligation Management notifications](cncore-ob-mgmt-notification.md)


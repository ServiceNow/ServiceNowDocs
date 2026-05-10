---
title: Rate type in labor rate card
description: The rate type functionality is used to categorize different types of work. For example, Standard versus Overtime.
locale: en-US
release: australia
product: Cost Management
classification: cost-management
topic_type: concept
last_updated: "2026-05-09"
reading_time_minutes: 1
breadcrumb: [Manage a labor rate card, Task and labor rate cards, Cost Management, Strategic Portfolio Management]
---

# Rate type in labor rate card

The rate type functionality is used to categorize different types of work. For example, Standard versus Overtime.

The Labor Rate Card form contains options to specify rate type, specify hourly rate for the rate type, and specify users for whom the labor rate card is applicable. A single user can be associated with multiple labor rate cards that contain different rate types.

Assume that a user logs time against a task and selects the rate type Standard in the Time Cards form. Upon approval, the expense line \(cost\) for the time card is derived by matching the user and rate type on the time card to a labor rate card assigned to that user, and that has the same rate type. When the user has multiple labor rate cards with the same rate type, the expense line is generated based on the labor rate card that has the lowest value in the **Order** field. When there is no labor rate card associated with the user and rate type, the default hourly rate found in the**Time Sheets** &gt; **Administration** &gt; **Time Sheet Policy** form is used \(**com.snc.time\_card.default\_rate** property\).

**Note:** A user can enter a rate type only if it is permitted by the users [Time sheet policies](../../../administer/task-table/concept/time-sheet-policies.md).

**Parent Topic:**[Manage a labor rate card](../task/t_ManageALaborRateCard.md)

**Related topics**  


[Create a rate type](../task/CreateRateType.md)


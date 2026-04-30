---
title: Include or exclude user access for event types​
description: Add or remove access to users for any event type so that they can view event types that are relevant only to them.​
locale: en-US
release: xanadu
product: Workforce Optimization for IT Service Management
classification: workforce-optimization-for-it-service-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Understanding user criteria for event types in Workforce Optimization for ITSM, Scheduling your teams' work in Workforce Optimization for ITSM, Scheduling in Workforce Optimization for ITSM, Workforce Optimization for ITSM, IT Service Management]
---

# Include or exclude user access for event types​

Add or remove access to users for any event type so that they can view event types that are relevant only to them.​

## Before you begin

Role required: sn\_shift\_planning.admin​

## Procedure

1.  Navigate to **All** &gt; **Workforce Optimization for ITSM** &gt; **Scheduling** &gt; **Event Types**.

2.  Select an event.

3.  Exclude or Include specific CRUD access for users to events.

<table id="choicetable_s5n_mmr_pwb"><thead><tr><th align="left" id="d197033e85">

To

</th><th align="left" id="d197033e88">

Do this

</th></tr></thead><tbody><tr><td id="d197033e94">

**Exclude users for which you do not want to enable specific access to event types.__Important:__ For exclusion, a __Create__ access will deny the user from creating events because it excludes that access for the user. The same principle applies to any of the CRUD operations.

**

</td><td>

1.  Select the **Evaluate access for exclusion** tab.

**Note:** You can set the CRUD access for each user criteria where you would exclude the user from specific CRUD operations.

2.  To create a new **Event Exclusion User Criteria**, select **New**.
3.  In the **Name** field, enter a name, which is an entity of users that is evaluated for the exclusion user criteria for the selected event type. This entity identifies and associates the user criteria to the event type..
4.  In the **User criteria** field, select the user criteria record for which you want to set exclusion CRUD operations.
5.  Select the CRUD operations for which you do not want to give access.
6.  Select **Submit**.


</td></tr><tr><td id="d197033e151">

**Include users for which you want to enable specific access to event types.__Important:__

For inclusion, for specific CRUD operation such as __Create__, the system evaluates if at least one of the inclusion user criteria is set to __true__:

-   If any of the criteria is set to true, then the system checks if the user satisfies the criteria.
    -   If the user satisfies the criteria, then they have access for the specific CRUD operation.
    -   If the user does not satisfy the criteria, then they don't have access to the CRUD operation.
-   If none of the criteria is set to true, the user has access to the specific CRUD operation. This is based on the default behavior where all users have access based on their roles before they're added to the user criteria.
**

</td><td>

1.  Select the **Evaluate access for inclusion** tab.
2.  To create a new **Event Inclusion User Criteria**, select **New**.
3.  In the **Name** field, enter a name for the event inclusion user criteria.
4.  In the **User criteria** field, select the user criteria record for which you want to set inclusion user criteria access.
5.  Select the CRUD operations for which you want to give access.
6.  Select **Submit**.


</td></tr></tbody>
</table>4.  Click **Update**.


**Parent Topic:**[Understanding user criteria for event types in Workforce Optimization for ITSM](../concept/understanding-user-criteria-event-types-wfo-itsm.md)


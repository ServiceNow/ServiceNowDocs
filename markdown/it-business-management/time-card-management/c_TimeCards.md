---
title: Time cards
description: Time cards are used to record the time worked on a task by a task assignee.
locale: en-US
release: australia
product: Time Card Management
classification: time-card-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Time Card management, Project Portfolio Management, Strategic Portfolio Management]
---

# Time cards

Time cards are used to record the time worked on a task by a task assignee.

The time card management feature works with the Task table to record time worked on Projects, Incidents, Problems, and Change Requests.

Task assignees can record time worked in the Time worked field on a task record or enter hours directly into their time card. Some tables support automatic time card creation based on start and end date fields.

Track the activities of a time card, such as who submitted or approved a time card, in the Activities section on the Time Card form. This time card activity audit is useful for tracking when you delegate responsibility for your time sheet processing to another user. To track the activities, enable the **State** field of the Time Card \[time\_card\] table for auditing the time card activities, if it isn't already enabled. For more information, see [Include a table field in auditing](https://www.servicenow.com/docs/access?context=security-whitelist-audit-field&version=australia&pubname=australia-platform-security&ft:locale=en-US).

You can associate time cards for the project tasks and other task categories, such as meeting and training, with relevant [resource plans](../../../product/resource-management/task/t_AssocATimeCardWithAResourcePlan.md).

When you approve a time card, the time logged in the time card is saved day-wise in the Time Card Daily \[time\_card\_daily\] table. Using daily time logged data, you can generate time card reports by days for any period irrespective of the time sheet period to which the time cards belong. For example, you can create a monthly time card report that includes time cards from the first day to the last day of the month.

Time cards also have an optional approval mechanism for project managers to approve the time cards. Administrators and time card approvers can see all the time cards for the week. All users who are in a role that is responsible for working on tasks also can access their personal time cards. A time card can have any of the following states:

|State|Description|
|-----|-----------|
|Pending|A Time card that isn’t submitted for approval.|
|Submitted|A time card submitted for approvals.|
|Approved|An approved time card.|
|Processed|An approved time card with an expense line for the associated task.|
|Rejected|A rejected time card.|
|Recalled|An approved time card recalled for any required adjustments.|

-   **[Create a time card](../task/t_CreateATimeCard.md)**  
You can create time cards to log time against the work you have done.
-   **[Submit a time card](../task/submit-time-card.md)**  
As a time card user, once a time card for the week is updated with the time worked, you can submit the time card individually.
-   **[Approve or reject a time card](../task/approve-time-card.md)**  
As a time card approver, you can view and approve or reject a submitted time card.
-   **[Recall a processed time card](../task/recall-approved-time-card.md)**  
You can recall an incorrect time card in the Approved or Processed state to return it to the submitter. The submitter can then make the necessary changes and resubmit the time card.
-   **[Map a time card category with operational work types](../task/map-time-card-category.md)**  
Map custom time card categories with operational work types so you can select only the operational resource plans that are associated with the user for a specific time card period and category while posting time.

**Parent Topic:**[Time Card Management](time-card-management.md)


---
title: Time Sheets
description: A time sheet groups all the time cards for a user for the given week.
locale: en-US
release: xanadu
product: Table Administration and Data Management
classification: table-administration-and-data-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Time Card management, Working with the Task table, Table administration, Tables and data, Configure core features, Administer the ServiceNow AI Platform]
---

# Time Sheets

A time sheet groups all the time cards for a user for the given week.

With time sheets:

-   Time card users can submit all the time for their work week in a single step by using a time sheet.
-   Time card approvers can approve all the time cards in a time sheet for a user in a single step by approving the time sheet. They do not need to approve multiple time cards for a given user individually.
-   Track the activities of a time sheet, such as who submitted or approved a time sheet, in the Activities section on the Time Sheet form. This time sheet activity audit is useful for tracking when you delegate responsibility for your time card processing to another user. To track the activities, enable the **State** field of the Time Card \[time\_card\] table for auditing the time card activities, if it is not already enabled. For more information, see [Include a table field in auditing](https://www.servicenow.com/docs/access?context=security-whitelist-audit-field&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US).

Starting Xanadu release, users can select a resource assignment to associate it with time cards to calculate the actual efforts and tag them to the respective projects. For more information on how to enable resource assignments column on time sheet portal, see [KB1649389](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1649389) in the Now Support Knowledge Base.

A time sheet can have any of the following states:

-   **Pending**

    A time sheet has been created, but the user is still making changes before submitting it.

-   **Submitted**

    A time sheet has been submitted for approval. The approver can approve or reject it.

-   **Approved**

    A time sheet has been approved. If the time sheet isn't automatically updated to Processed, this means there was no task associated with the time sheet.

-   **Processed**

    A time sheet has been processed by the system. After a time sheet is approved, the after business rule Create expense from approved time card is triggered. This business rule creates an expense line for the associated task, and then updates the state to Processed.

-   **Rejected**

    A time sheet has been sent back to the submitter for changes.

-   **Recalled**

    A time sheet has been recalled by the submitter for modification.


-   **[Create a time sheet](../task/create-time-sheet.md)**  
As a time card user, you can create a time sheet to group all your time cards for the given week and submit them in a single step.
-   **[Submit a time sheet](../task/submit-time-sheet.md)**  
Once the time sheet is updated with time worked, you can submit the time sheet for the week to submit all the time cards for the week together.
-   **[Approve or reject a time sheet](../task/approve-time-sheet.md)**  
View, approve, or reject time sheet or time cards for your user, for the given week, in a single step.

**Parent Topic:**[Time Card Management](time-card-management.md)


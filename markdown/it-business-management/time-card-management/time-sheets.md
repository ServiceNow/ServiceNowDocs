---
title: Time Sheets
description: A time sheet groups all the time cards for a user for the given week.
locale: en-US
release: yokohama
product: Time Card Management
classification: time-card-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Time Card management, Project Portfolio Management, Strategic Portfolio Management]
---

# Time Sheets

A time sheet groups all the time cards for a user for the given week.

With time sheets:

-   Time card users can submit all the time for their work week in a single step by using a time sheet.
-   Time card approvers can approve all the time cards in a time sheet for a user in a single step by approving the time sheet. They do not need to approve multiple time cards for a given user individually.
-   Track the activities of a time sheet, such as who submitted or approved a time sheet, in the Activities section on the Time Sheet form. This time sheet activity audit is useful for tracking when you delegate responsibility for your time card processing to another user. To track the activities, enable the **State** field of the Time Card \[time\_card\] table for auditing the time card activities, if it is not already enabled. For more information, see [Include a table field in auditing](https://www.servicenow.com/docs/access?context=security-whitelist-audit-field&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).

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
-   **[Recall a processed time sheet](../task/recall-approved-time-sheet.md)**  
You can recall an incorrect time sheet in the Approved or Processed state to return it to the submitter. The submitter can then make the necessary changes and resubmit the time sheet.
-   **[Delegate time sheet approvals to another user](../task/delegate-time-sheet-approvals.md)**  
You can delegate the responsibilities to process the time sheets of your resources to another user when you might not have time or will be unavailable.

**Parent Topic:**[Time Card Management](time-card-management.md)


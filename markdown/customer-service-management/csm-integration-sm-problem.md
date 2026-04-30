---
title: CSM integration with Problem Management
description: Integration with the Problem Management application enables customer service agents to create problem records from cases or associate existing problem records to cases.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Overview, Integrate with IT Service Management, Integrate, Customer Service Management]
---

# CSM integration with Problem Management

Integration with the Problem Management application enables customer service agents to create problem records from cases or associate existing problem records to cases.

With this integration, customer service agents can:

-   Create a problem from a case.
-   Associate an existing open problem to a case.
-   Remove an associated problem from a case.
-   View problem state changes in the case work notes.

**Note:** A case can be associated with one problem. If a case is already associated with a problem, the **Create Problem** item doesn’t appear on the Additional Actions menu.

## Plugins

Integration with Problem Management requires the Customer Service with Service Management plugin \(com.sn\_cs\_sm\).

## Roles

The following roles enable customer service agents to view and create problems for customer service cases.

-   sn\_problem\_read
-   sn\_problem\_write

For more information, see [Assign CSM/ITSM integration roles](../task/assign-csm-itsm-integration-roles.md#).

## Synchronizing data between the problem and the case

With the Problem Management Best Practice – Madrid plugin activated, customer service agents can view the following information in the case work notes:

-   When the state of a related problem is updated, the text of the work note includes a link to the problem.
-   When **Communicate Workaround** is selected from the related problem, the workaround text is copied to the case work notes.
-   When **Communicate Fix** is selected from the related problem, the fix text is copied to the case work notes.
-   When the problem is resolved or closed with a specific resolution code:
    -   State is Closed and Resolution Code is Cancelled. The Cancelled Reason text is copied to the case work notes.
    -   State is Closed and Resolution Code is Risk Accepted, the Cause notes, Risk accepted reason, and Fix notes are copied to the case work notes.
    -   State is Resolved and Resolution Code is Fix Applied, the Cause notes, and Fix notes are copied to the case work notes.
    -   State is Closed and the Resolution Code is Fix Applied, the Cause notes, and Fix notes are copied to the case work notes.

With the Problem Management Best Practice - Madrid - Knowledge Integration plugin activated, the customer service agent can view information in the case work notes when a Known Error Article is created for or associated with a related problem. The work note includes a link to the article.


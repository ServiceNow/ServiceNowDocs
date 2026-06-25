---
title: Complete a supplier case from the Source-to-Pay Workspace
description: You can mark a supplier case as complete when you finish all the tasks related to that case.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/supplier-lifecycle-operations/complete-supplier-case.html
release: australia
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Manage supplier cases, Using Source-to-Pay Workspace, Use, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Complete a supplier case from the Source-to-Pay Workspace

You can mark a supplier case as complete when you finish all the tasks related to that case.

## Before you begin

Role required: sn\_slm.fulfiller, sn\_slm.owner, or sn\_slm.admin

## Procedure

1.  Navigate to **All** &gt; **Supplier Lifecycle Operations** &gt; **Source-to-Pay Workspace**.

2.  Select the list icon \(\[Omitted image "cases-list-icon.png"\] Alt text: List icon.\).

3.  Do one of the following:

    -   View all the open cases by navigating to **Lists** &gt; **Cases** &gt; **Open cases**.
    -   View all the cases by navigating to **Lists** &gt; **Cases** &gt; **All cases**.
4.  Open a case that is in Open, Work in progress, or Awaiting task completion state by selecting the link to the case in the Number column.

5.  Select **Complete**.\[Omitted image "complete-supplier-case.png"\] Alt text: Completing a supplier case.

6.  Add closing notes to the case.

    -   If the **sn.slm.isAcceptedFlowEnabled** property is enabled, the case state is changed to Awaiting acceptance and an email is sent to the supplier contact with the resolution details. Supplier contacts can accept or reject the resolution either by replying to the email or by navigating to My tasks in the Supplier Collaboration Portal.
    -   If the **sn.slm.isAcceptedFlowEnabled** property is not enabled, the case state is changed to closed after the addition of the closing notes.

## Result

If the supplier contact accepts the resolution, the supplier case is marked as **Closed completed**. If the supplier contact rejects the resolution, the case state is changed to **Work in progress**.

**Parent Topic:**[Manage supplier cases from the Source-to-Pay Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/managing-cases.md)

**Related topics**  


[Manage supplier cases from the Source-to-Pay Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/managing-cases.md)

[Reopen a supplier case from the Source-to-Pay Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/reopen-supplier-case.md)


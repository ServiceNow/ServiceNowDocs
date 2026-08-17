---
title: Review a case filing appeal
description: Review a case filing appeal and obtain an acknowledgment from Visa.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/financial-services-operations/dispute-management/review-case-filing-appeal.html
release: australia
product: Dispute Management
classification: dispute-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Collaboration workflow, Initiate chargeback, Processing a Visa dispute, Managing disputes integrated with Visa, Processing, Use, Dispute Management, Banking applications, Financial Services Operations \(FSO\)]
---

# Review a case filing appeal

Review a case filing appeal and obtain an acknowledgment from Visa.

## Before you begin

Role required: sn\_bom\_credit\_card.dispute\_agent or sn\_bom\_credit\_card.dispute\_agent\_connector

## About this task

After reviewing the case filing response, Visa issues a decision letter that supports either the acquirer or the issuer. If either party isn't satisfied with the decision, they can file an appeal.

## Procedure

1.  Navigate to **All** &gt; **Financial Services Operations** &gt; **Workspace**.

2.  Select the lists icon \(\[Omitted image "inline-data-vis-96px-list.png"\] Alt text: lists icon\).

3.  In the **Lists** tab under **Card disputes service cases**, open the case list.

    -   For your assigned cases, select **Assigned to me**.
    -   For all dispute cases, select **All**.
4.  In the list, select which case you want to work on.

    If you want to work on a case that isn't assigned to you yet, you can assign it to yourself by selecting **Assign to me**.

5.  Select the transaction ID from the playbook.

    The **Chargeback** stage is initiated for the transaction.

6.  Select the **Review case filing appeal** task.

7.  Review the case filing details and select **Get acknowledgement letter**.

    The acknowledgment letter can also be viewed in the activity stream. After the request runs successfully, the transaction state changes to **Awaiting External Info**. The form is set to read-only mode while waiting for a response from Visa.

8.  View the decision letter from Visa by selecting **Get appeal response**.

    The decision letter can also be viewed in the activity stream.

9.  In the **Response outcome** field, select your response.

    -   If you select **Unresolved**, the **Reverse provisional credit** option is displayed.
    -   If you select **Resolved**, and select **Continue**, you accept the decision and issue the final credit.
10. Select **Close task**.


**Parent Topic:**[Collaboration dispute workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/collaboration-dispute-workflow.md)

**Parent Topic:**[Allocation dispute workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/allocation-dispute-work-flow.md)


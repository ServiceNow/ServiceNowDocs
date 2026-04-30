---
title: Add an approver
description: Add a single or multiple approvers to the document approval and review rule for document approval.
locale: en-US
release: zurich
product: Document Management Services
classification: document-management-services
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Document approval and publish process, Use, Document Management, Document Services, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Add an approver

Add a single or multiple approvers to the document approval and review rule for document approval.

## Before you begin

Role required: platform\_document\_management\_admin or admin

## About this task

The procedure described in this task applies to newly created records. For existing records, go to the document record, select the additional actions icon \(![Additional actions icon.](../../service-catalog-management/image/AdditinalActions.png)\) and select **Refresh Approvers and Reviewers** to match the rules and add approvers.

**Note:** The document reviewer and approver can be directly added through the document record but they aren't added to the Document approval and revision rule.

## Procedure

1.  Navigate to **All** &gt; **Documents** &gt; **Approval and Revision Rules**.

2.  Go to the rule that you want to add a reviewer or approvers to.

3.  Select the **Approvers** tab.

4.  Select **New**.

5.  In the **Approvers** field, enter the name of the reviewer.

6.  In the **Sequence** field, enter the sequence for the approver.

    **Note:** The document is sent to approvers in ascending order based on the sequence number entered. If two approvers have the same sequence number, only one approver's approval is needed to move on to the next approver in the sequence or to publish the document if there’s no approver in the sequence.

7.  Select **Submit**.

8.  Repeat steps 3–7 to add multiple approvers.


**Parent Topic:**[Document approval and publish process](../concept/document-review-approval.md)


---
title: Verify customer supporting documents
description: After following up with the customer to request further documentation about the dispute, verify the supporting documents that you received.
locale: en-US
release: zurich
product: Dispute Management
classification: dispute-management
topic_type: task
last_updated: "2025-11-06"
reading_time_minutes: 1
breadcrumb: [Processing an ACH dispute, Resolving ACH disputes, Processing, Use, Dispute Management, Banking applications, Financial Services Operations \(FSO\)]
---

# Verify customer supporting documents

After following up with the customer to request further documentation about the dispute, verify the supporting documents that you received.

## Before you begin

Role required: sn\_bom\_credit\_card.dispute\_agent or sn\_bom\_credit\_card.dispute\_agent\_connector

## About this task

After the customer sends supporting documents in response to a denial, you extract the email contents and attachments and connect them to the task. Your next step is to review the information and, using the updated details, determine if you should file a return, deny the customer’s claim, or request additional information.

## Procedure

1.  Navigate to **All** &gt; **Financial Services Operations** &gt; **Workspace**.

2.  Select the lists icon \(![lists icon](../../../use/reporting/image/inline-data-vis-96px-list.png)\).

3.  In the **Lists** tab under **Card disputes service cases**, open the case list.

    -   For your assigned cases, select **Assigned to me**.
    -   For all dispute cases, select **All**.
4.  In the list, select which case you want to work on.

    If you want to work on a case that isn't assigned to you yet, you can assign it to yourself by selecting **Assign to me**.

5.  Select the **Playbook** tab.

6.  In the **Processing** tab, select the transaction ID.

7.  In **Open Tasks**, select **Verify customer supporting documents**.

8.  In **Action**, select the final action:

    -   **Deny**: The ACH dispute is determined to be invalid and is denied. The provisional credit is removed.
    -   **File return**: The ACH dispute is determined to be valid and meets eligibility for return. A refund is initiated.
    -   **Follow up for additional proof**: Additional customer information is required before a refund can be approved or denied.
9.  Close the task.


**Parent Topic:**[Processing an ACH dispute](../concept/process-dispute-ach.md)


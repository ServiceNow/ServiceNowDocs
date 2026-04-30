---
title: Verify ODFI supporting documents
description: After following up with the Originating Depository Financial Institution \(ODFI\) to request further documentation about the dispute, verify the supporting documents that you received.
locale: en-US
release: zurich
product: Dispute Management
classification: dispute-management
topic_type: task
last_updated: "2025-11-06"
reading_time_minutes: 1
breadcrumb: [Processing an ACH dispute, Resolving ACH disputes, Processing, Use, Dispute Management, Banking applications, Financial Services Operations \(FSO\)]
---

# Verify ODFI supporting documents

After following up with the Originating Depository Financial Institution \(ODFI\) to request further documentation about the dispute, verify the supporting documents that you received.

## Before you begin

Role required: sn\_bom\_credit\_card.dispute\_agent or sn\_bom\_credit\_card.dispute\_agent\_connector

## About this task

An Originating Depository Financial Institution \(ODFI\) is a bank or credit union that initiates ACH transactions on behalf of its customers \(called Originators\). It serves as the entry point into the ACH network, transmitting payment instructions to an ACH Operator \(such as the Federal Reserve or The Clearing House\) for further processing.

After receiving supporting documents from the ODFI in response to the Follow-up communication, your first step is to extract the email contents and attachments and link them to the task.

You then review these updated details to determine if you should file a return, deny the customer’s claim, or request additional information.

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

7.  In **Open Tasks**, select **Verify ODFIs supporting documents**.

8.  In **Action**, select the final action.

    -   **Deny**: The ACH dispute is determined to be invalid and is denied. The provisional credit is removed.
    -   **File return**: The ACH dispute is determined to be valid and meets eligibility for return. A refund is initiated.
    -   **Follow up for additional proof**: Further information is required from ODFI before a refund can be either denied or issued.
9.  Close the task.


**Parent Topic:**[Processing an ACH dispute](../concept/process-dispute-ach.md)


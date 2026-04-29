---
title: Review a case filing response and appeal the decision
description: An appeal can be created by the issuer or acquirer if either party isn’t satisfied with the arbitration ruling from Visa. Review the case filing response and receive the decision letter from Visa.
locale: en-US
release: australia
product: Dispute Management
classification: dispute-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Collaboration workflow, Initiate chargeback, Processing a Visa dispute, Resolving disputes with Visa, Processing, Use, Dispute Management, Banking applications, Financial Services Operations \(FSO\)]
---

# Review a case filing response and appeal the decision

An appeal can be created by the issuer or acquirer if either party isn’t satisfied with the arbitration ruling from Visa. Review the case filing response and receive the decision letter from Visa.

## Before you begin

Role required: sn\_bom\_credit\_card.dispute\_agent or sn\_bom\_credit\_card.dispute\_agent\_connector

## About this task

After reviewing the case filing response, Visa issues a decision letter that supports either the acquirer or the issuer. If either party isn’t satisfied with the decision, they can file an appeal.

## Procedure

1.  Navigate to **All** &gt; **Financial Services Operations** &gt; **Workspace**.

2.  Select the lists icon \(![lists icon](../../../use/reporting/image/inline-data-vis-96px-list.png)\).

3.  In the **Lists** tab under **Card disputes service cases**, open the case list.

    -   For your assigned cases, select **Assigned to me**.
    -   For all dispute cases, select **All**.
4.  In the list, select which case you want to work on.

    If you want to work on a case that isn't assigned to you yet, you can assign it to yourself by selecting **Assign to me**.

5.  Select the **Playbook** tab.

6.  In the transaction level playbook of the **Processing** tab, select the transaction ID.

7.  The **Chargeback** stage is initiated for the transaction.

8.  Select the **Review case filing appeal** activity.

9.  Retrieve the decision letter from Visa by selecting **Get case filing response**.

    The letter can also be viewed in the activity stream.

10. In the **Response outcome** field, either accept or appeal the decision.

    -   To accept the outcome, select **Resolved**.
    -   To appeal the outcome, select **Unresolved**.
11. In the **Create appeal** drop-down list, select **Yes**.

    **Note:** Certain conditions must be met to create an appeal. For more information, see [Collaboration workflow overview](../concept/collaboration-workflow.md).

12. In the **Appeal amount** field, enter the amount for the appeal.

13. In the **Reason for appeal** field, explain why you want to appeal the decision.

14. In the **Description**, **Remarks**, and **Work notes** fields, enter additional details as necessary.

15. Select **Continue**.

16. Select **Create appeal**.


## Result

After the request executes successfully, the transaction state changes to **Awaiting External Info**. The form is set to read-only mode while waiting on a response. Visa confirms the appeal with an acknowledgment letter. Retrieve the letter by selecting **Get acknowledgement letter** in the **Review case filing appeal** activity.

**Parent Topic:**[Collaboration dispute workflow](../concept/collaboration-dispute-workflow.md)


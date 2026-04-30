---
title: Processing a Mastercard dispute
description: You can view all the transactions of the dispute in the Processing stage of the playbook. This stage provides transaction information such as dispute amount, transaction date and time, merchant name, transaction state, current activity, and activity SLA.
locale: en-US
release: zurich
product: Dispute Management
classification: dispute-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Resolving disputes with Mastercard, Processing, Use, Dispute Management, Banking applications, Financial Services Operations \(FSO\)]
---

# Processing a Mastercard dispute

You can view all the transactions of the dispute in the **Processing** stage of the playbook. This stage provides transaction information such as dispute amount, transaction date and time, merchant name, transaction state, current activity, and activity SLA.

After a dispute case is submitted, each disputed transaction is displayed in a **Dispute Workspace**. The dispute transaction progresses through these stages: **Investigate**, **Chargeback**, and **Closure**. As the dispute proceeds, the appropriate stage is updated accordingly. To open a transaction in the **Dispute Workspace**, select the transaction number.

![The transactions are displayed in the Dispute Workspace](../image/mastercard-dispute-workspace.png "Dispute workspace")

-   Each transaction progresses through a series of steps, during which a corresponding sequence of tasks is generated. The tasks are displayed in **Tasks**.
-   The **Open** tab displays the tasks open along with the SLA and State.
-   The **Short description** provides a preview of the task. Select the task to view its details.
-   The **Closed** tab displays all the tasks that have been closed.
-   The activity stream for the transaction is displayed below the task.
-   The dispute transaction and financial transaction details are displayed in **Disputed transaction details** and **Financial transaction details** widget.
-   The **Attachments** displays files attached to the case.

-   **[About Financial adjustments in Mastercard disputes](financial-adjustments.md)**  
Financial adjustments are tasks or activities displayed based on the policy of the transaction. In Mastercard, there are two types of financial adjustments: Financial adjustments 1 and Financial adjustments 2.
-   **[Chargeback in Mastercard transaction disputes](chargeback-stage-mastercard.md)**  
After a chargeback is initiated, the chargeback request is sent to Mastercard, which alerts the merchant. Mastercard requests collaboration from merchants, who either provide a voucher, refund, or First-Party Trust evidence as response. If the merchant doesn’t respond, the process escalates to formal chargeback procedures.

**Parent Topic:**[Managing disputes integrated with Mastercard](work-on-disputes-integrated-with-mc.md)


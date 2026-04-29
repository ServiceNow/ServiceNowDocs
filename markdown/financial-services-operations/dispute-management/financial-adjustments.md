---
title: About Financial adjustments in Mastercard disputes
description: Financial adjustments are tasks or activities displayed based on the policy of the transaction. In Mastercard, there are two types of financial adjustments: Financial adjustments 1 and Financial adjustments 2.
locale: en-US
release: australia
product: Dispute Management
classification: dispute-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Processing a Mastercard dispute, Resolving disputes with Mastercard, Processing, Use, Dispute Management, Banking applications, Financial Services Operations \(FSO\)]
---

# About Financial adjustments in Mastercard disputes

Financial adjustments are tasks or activities displayed based on the policy of the transaction. In Mastercard, there are two types of financial adjustments: Financial adjustments 1 and Financial adjustments 2.

For scenarios when the **Response Outcome** is **Resolved** and the outcome is in favor of the cardholder, the dispute life cycle ends and the Financial adjustments 1 is activated. Based on the policy, the table describes the tasks displayed as part of Financial adjustments 1.

<table id="table_ngh_rqn_bgc"><thead><tr><th>

Policy

</th><th>

Task

</th></tr></thead><tbody><tr><td>

Immediate provisional credit \(IPC\)

</td><td>

A task is created to convert provisional credit to final credit, and the dispute life cycle ends for the transaction. For more information, see [Convert provisional credit to final credit](../task/convert-provisional-credit-to-final-credit_mc.md).If collaboration outcome is **Resolved**, and IPC was given, then a task is created to reverse provisional credit. For more information, see [Reverse provisional credit](../task/reverse-provisional-credit-mc.md).

</td></tr><tr><td>

No credit

</td><td>

A task is created to provide final credit to the customer, and the dispute life cycle ends for the transaction. For more information, see [Provide final credit to customer](../task/provide-final-credit-mc.md).

</td></tr><tr><td>

Immediate final credit \(IFC\)

</td><td>

No further action is taken, and the dispute life cycle ends for the transaction.

</td></tr></tbody>
</table>For scenarios when the **Response Outcome** is **Unresolved** and decision is not to proceed with next stage of dispute, the Financial adjustments 2 is activated. Based on the policy the table describes the tasks displayed as part of Financial adjustments 2.

<table id="table_cyp_q5n_bgc"><thead><tr><th>

Policy

</th><th>

Outcome

</th></tr></thead><tbody><tr><td>

Immediate provisional credit \(IPC\)

</td><td>

If a provisional credit is provided earlier, the **Reverse provisional credit** drop-down is displayed. Based on the options selected as **Yes** or **No**, the next tasks of converting IPC to Final credit [Convert provisional credit to final credit](../task/convert-provisional-credit-to-final-credit_mc.md) or [Reverse provisional credit](../task/reverse-provisional-credit-mc.md) is displayed.

</td></tr><tr><td>

Immediate final credit \(IFC\)

</td><td>

No action is done.

</td></tr><tr><td>

No credit

</td><td>

The **Issue final credit and write off** drop-down is displayed. If the option selected is **Yes** then the next task [Provide final credit to customer](../task/provide-final-credit-mc.md) and the dispute life cycle ends for the transaction. If the option selected is **No**, then the chargeback is denied and the dispute life cycle ends for the transaction.

</td></tr></tbody>
</table>**Parent Topic:**[Processing a Mastercard dispute](processing-mastercard-dispute-case.md)


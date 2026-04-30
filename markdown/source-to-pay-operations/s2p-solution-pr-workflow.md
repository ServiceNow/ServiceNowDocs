---
title: Source-to-Pay purchasing workflow
description: Gather a high-level understanding of the end-to-end purchasing workflow with the Sourcing and Procurement Operations \(SPO\) and Accounts Payable Operations \(APO\) products within the Source-to-Pay \(S2P\) suite.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-06"
reading_time_minutes: 4
breadcrumb: [Source-to-Pay Operations purchasing and sourcing workflows, Source-to-Pay Operations, Finance and Supply Chain]
---

# Source-to-Pay purchasing workflow

Gather a high-level understanding of the end-to-end purchasing workflow with the Sourcing and Procurement Operations \(SPO\) and Accounts Payable Operations \(APO\) products within the Source-to-Pay \(S2P\) suite.

## Prerequisites

Install and activate the necessary plugins. For information on the respective product plugins and installation sequence, see:

-   SPO: [Application plugin installation sequence](../../sourcing-procurement-operations/reference/application-plugin-list.md)
-   APO: [Application plugin installation sequence in Accounts Payable Operations](../../accounts-payable-operations/reference/application-plugin-installation-sequence-apo.md)

## Workflow of the purchasing process

The following figure shows how different personas use the various applications withing the SPO and APO products to complete the end-to-end purchasing process within the Source-to-Pay \(S2P\) suite.

![Workflow of the purchasing process, showing various stages and the personas involved in each stage.](../../sourcing-procurement-operations/image/s2p-purchasing-workflow.png "Workflow of the purchasing process")

In this workflow:

1.  An employee performs a quick checkout with a product or service that has a contractual price. A purchase requisition is created. For more information, see [Order a product with quick checkout](../../sourcing-procurement-operations/task/order-a-product.md).

    Alternatively, an employee performs a full checkout with products or services that have contractual prices. For more information, see [Complete your checkout](../../sourcing-procurement-operations/task/complete-your-checkout.md).

    Role: sn\_shop.shopper.

    Application portal: Shopping Hub.

2.  Approval rules route the purchase request to one or more assigned approvers.
3.  An approver reviews the purchase request and approves it. A purchase order is created. For more information, see [Approve a request from Employee Center](../../sourcing-procurement-operations/task/approve-request-from-employee-center.md).

    Role: sn\_shop.procurement\_specialist.

    Application portal: Employee Center.

4.  A procurement specialist fulfills the purchase order from the associated supplier.

    Role: sn\_shop.procurement\_specialist.

    Application portal: Source-to-Pay Workspace.

5.  On fulfillment, the employee confirms receipt of the requested product. For more information, see [Confirm receipt of your order from Shopping Hub Home](../../sourcing-procurement-operations/task/work-receipt-todos.md) and [Confirm receipt of your order from Employee Center](../../sourcing-procurement-operations/task/confirm-receipt-task-ec.md).

    Role: sn\_shop.shopper.

    Application portal: Shopping Hub or Employee Center.

6.  Invoices are auto-created. When invoices aren’t auto-submitted or don’t match the purchase orders, or when invoice exceptions must be resolved, an accounts payable specialist gets involved. For more information, see [Accounts Payable Invoice Processing](../../accounts-payable-operations/concept/acc-pay-invoice-processing.md).

    Alternatively, the accounts payable specialist manually creates invoices. For more information, see [Accounts Payable Specialist manual tasks](../../accounts-payable-operations/concept/aps-manual-tasks.md).

    Role: sn\_ap\_apm.accounts\_payable\_specialist.

    Application portal: Source-to-Pay Workspace.

7.  The accounts payable specialist converts invoices of purchase order type to invoice types such as non-purchase order, credit memo, and debit memo, based on their interactions with shoppers and suppliers of business services. For more information, see [Accounts Payable Specialist manual tasks](../../accounts-payable-operations/concept/aps-manual-tasks.md).

    Role: sn\_ap\_apm.accounts\_payable\_specialist.

    Application portal: Source-to-Pay Workspace.

8.  An accounts payable agent manages and works on assigned invoice cases, requests more information from suppliers or employees if necessary, and creates and assigns tasks to the users. For more information, see [Invoice Case Management](../../accounts-payable-operations/concept/acc-pay-case-mgmt-overview.md).

    Role: sn\_ap\_cm.agent.

    Application portal: Source-to-Pay Workspace.

9.  The employee, approver, procurement specialist, accounts payable specialist, and accounts payable agent have complete visibility into the status of the workflow through process completion, from their respective portals.


---
title: End-to-end sourcing workflow in Source-to-Pay Operations
description: Gather a high-level understanding of the end-to-end sourcing workflow with the Sourcing and Procurement Operations \(SPO\), Supplier Lifecycle Operations \(SLO\), and Accounts Payable Operations \(APO\) products within the Source-to-Pay \(S2P\) suite.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/source-to-pay-operations/finance-and-supply-chain/s2p-solution-sr-workflow.html
release: zurich
product: Finance and Supply Chain
classification: finance-and-supply-chain
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 7
breadcrumb: [Purchasing and sourcing workflows, Source-to-Pay Operations, Finance and Supply Chain]
---

# End-to-end sourcing workflow in Source-to-Pay Operations

Gather a high-level understanding of the end-to-end sourcing workflow with the Sourcing and Procurement Operations \(SPO\), Supplier Lifecycle Operations \(SLO\), and Accounts Payable Operations \(APO\) products within the Source-to-Pay \(S2P\) suite.

The sourcing workflow is triggered when there is an active contractual price for a product or service that the shopper intends to purchase.

## Prerequisites

Install and activate the necessary plugins. For more information on the respective product plugins and installation sequence, see:

-   SPO: [Application plugin installation sequence in Sourcing and Procurement Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/sourcing-and-procurement-operations/application-plugin-list.md)
-   SLO: [Application plugin installation sequence in Supplier Case Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/supplier-lifecycle-operations/slm-plugin-list.md)
-   APO: [Application plugin installation sequence in Accounts Payable Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/accounts-payable-operations/application-plugin-installation-sequence-apo.md)

## Workflow of the sourcing process

The following figure shows how different personas use the various applications withing the SPO, SLO, and APO products to complete the end-to-end sourcing process within the Source-to-Pay \(S2P\) suite.

\[Omitted image "spo-slo-sourcing-new-supplier.png"\] Alt text: Workflow of the sourcing process

In this workflow:

1.  An employee creates a sourcing request for a product or service that doesn't have a contractual price, or isn’t available in the catalog. For more information, see [Complete sourcing checkout](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/sourcing-and-procurement-operations/complete-sourcing-checkout.md) and [Requesting for products or services that you don't see on ShoppingHub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/sourcing-and-procurement-operations/request-prod-serv-dont-see-sh.md), respectively.

    Role: sn\_shop.shopper.

    Application portal: Shopping Hub and Employee Center respectively.

2.  Approval rules route the sourcing request to one or more assigned approvers.
3.  An approver reviews the sourcing request and approves it. For more information, see [Approve a request from Employee Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/sourcing-and-procurement-operations/approve-request-from-employee-center.md).

    Role: sn\_shop.procurement\_specialist.

    Application portal: Employee Center.

4.  Work assignment rules route the sourcing request to an assigned procurement specialist.
5.  The procurement specialist, with the contained role of a sourcing manager, adds the sourcing request to a negotiation event. For more information, see [Add a sourcing request to a sourcing event](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/sourcing-and-procurement-operations/add-a-sourcing-request-to-a-negotiation-event.md).

    Role: sn\_shop.procurement\_specialist.

    Application portal: Source-to-Pay Workspace.

6.  Negotiations are auto-created with qualified suppliers. For more information, see [Sourcing intake guided experience with playbooks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/sourcing-and-procurement-operations/sourcing-intake-guided-exp.md).

    If sourcing with a new supplier, see [End-to-end sourcing and supplier onboarding workflow in Source-to-Pay Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/finance-and-supply-chain/spo-slo-sourcing-with-new-suppliers.md).

    Role: sn\_shop.procurement\_specialist.

    Application portal: Source-to-Pay Workspace.

7.  Begin the qualification process to onboard the new supplier. For more information, see [Supplier qualification](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/sourcing-and-procurement-operations/supplier-qualification.md).

    Role: sn\_shop.procurement\_specialist.

    Application portal: Source-to-Pay Workspace.

8.  Review the supplier onboarding case and start the supplier onboarding using playbooks. For more information, see [Use the supplier onboarding playbook to onboard suppliers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/supplier-lifecycle-operations/use-playbooks-onboard-supp.md).

    The playbook automatically creates supplier tasks to conduct risk assessment and to collect supplier information, such as banking information and location details.

    Role: sn\_slm.manager.

    Application portal: Source-to-Pay Workspace.

9.  The supplier manager assigns the supplier tasks to the supplier contact.

    Role: sn\_slm.manager.

    Application portal: Source-to-Pay Workspace.

10. The supplier contact completes the following tasks:

    -   Assigned tasks. For more information, see [Viewing supplier contact tasks from the Supplier Collaboration Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/supplier-lifecycle-operations/my-to-dos.md).
    -   Risk assessment questionnaire. For more information, see [Complete a risk assessment from the Supplier Collaboration Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/supplier-lifecycle-operations/complete-risk-assessments.md).
    Role: sn\_slm.contact.

    Application portal: Supplier Collaboration Portal.

11. After the supplier manager reviews the supplier risk score and completes the different activities in each stage of the playbook, the supplier is successfully onboarded.

    Role: sn\_slm.manager.

    Application portal: Source-to-Pay Workspace.

12. On reaching supplier responses close date, the sourcing manager awards one or more suppliers. For more information, see [Award multiple suppliers from a sourcing event](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/sourcing-and-procurement-operations/award-multiple-suppliers-from-a-ne.md).

    Role: sn\_shop.procurement\_specialist.

    Application portal: Source-to-Pay Workspace.

13. Purchase requisitions are auto-created. The procurement specialist reviews the purchase requisitions and its associated purchase lines, and creates purchase orders. For more information, see [SPO list page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/source-to-pay-workspace/procurement-specialist-list-page.md).

    Role: sn\_shop.procurement\_specialist.

    Application portal: Source-to-Pay Workspace.

14. On fulfillment, the employee confirms receipt of the requested product. For more information, see [Confirm receipt of your order from Shopping Hub Home](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/sourcing-and-procurement-operations/work-receipt-todos.md) and [Confirm receipt of your order from Employee Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/sourcing-and-procurement-operations/confirm-receipt-task-ec.md).

    Role: sn\_shop.shopper.

    Application portal: Shopping Hub or Employee Center.

15. Invoices are auto-created. When invoices aren’t auto-submitted or don’t match the purchase orders, or when invoice exceptions must be resolved, an accounts payable specialist gets involved. For more information, see [Accounts Payable Invoice Processing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/accounts-payable-operations/acc-pay-invoice-processing.md).

    Alternatively, the accounts payable specialist manually creates invoices. For more information, see [Accounts Payable Specialist manual tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/accounts-payable-operations/aps-manual-tasks.md).

    Role: sn\_ap\_apm.accounts\_payable\_specialist.

    Application portal: Source-to-Pay Workspace.

16. The accounts payable specialist converts invoices of purchase order type to invoice types such as non-purchase order, credit memo, and debit memo, based on their interactions with shoppers and suppliers of business services. For more information, see [Accounts Payable Specialist manual tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/accounts-payable-operations/aps-manual-tasks.md).

    Role: sn\_ap\_apm.accounts\_payable\_specialist.

    Application portal: Source-to-Pay Workspace.

17. An accounts payable agent manages and works on assigned invoice cases, requests more information from suppliers or employees if necessary, and creates and assigns tasks to the users. For more information, see [Invoice Case Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/accounts-payable-operations/acc-pay-case-mgmt-overview.md).

    Role: sn\_ap\_cm.agent.

    Application portal: Source-to-Pay Workspace.

18. The employee, approver, sourcing manager, procurement specialist, supplier manager, accounts payable specialist, and accounts payable agent have complete visibility into the status of the workflow through process completion, from their respective portals.


---
title: Using the Dispute Content Pack for US Regulations
description: Dispute agents use the Dispute Content Pack for US Regulations to track the dispute cases that are governed by United States \(US\) Regulations \(Reg E and Reg Z\) and ensure they are in conformance with the regulatory guidance. This application provides the required Service Level Agreement \(SLA\) definitions and provide details to the dispute manager to monitor and take necessary actions.
locale: en-US
release: yokohama
product: Dispute Management
classification: dispute-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Dispute Content Pack for US Regulations, Working with Regulations, Dispute Management, Using banking applications, Financial Services Operations \(FSO\)]
---

# Using the Dispute Content Pack for US Regulations

Dispute agents use the Dispute Content Pack for US Regulations to track the dispute cases that are governed by United States \(US\) Regulations \(Reg E and Reg Z\) and ensure they are in conformance with the regulatory guidance. This application provides the required Service Level Agreement \(SLA\) definitions and provide details to the dispute manager to monitor and take necessary actions.

## Dispute Content Pack for US Regulations workflows

When an agent disputes a transaction on behalf of a customer or through the Customer Service Portal or Consumer Service Portal, a dispute service case begins and the dispute card transaction flow is triggered. This flow includes the various tasks that are specific to the case details. Each task is created when an agent closes the previous task.

1.  Create a dispute service card.

    The agent initiates the dispute service process by entering the initial case information and creating a dispute case on behalf of a customer. For more information, see [Creating a card dispute case](../../fso-card-operations/task/create-dispute-service-case.md).

2.  Initiate a dispute.
    -   The agent enters the dispute details, including the account that is being referenced, the dispute amount, and the type of dispute. The agent provides the necessary information for the available options in the type of dispute. For more information, see [Initiate a dispute](../../fso-card-operations/task/initiating-dispute.md#).
    -   In the **Select transaction** activity, the agent chooses a card account. The applicable Service Level Agreement \(SLA\) is automatically mapped and is based on the selected account and the preconfigured logic for that transaction.

        **Note:** Regulation E \(Reg E\) manages the transactions from the savings and checking accounts, while Regulation Z \(Reg Z\) handles the credit card transactions, according to the applicable criteria.

3.  Submit the case for investigation.
    -   In the **Submit dispute** activity, the agent reviews the dispute amount. The agent selects the option **Is this a new financial account?** and submits the case for further investigation. For more information on the various stages, see [Submit for investigation](../../fso-card-operations/task/initiating-dispute.md#).
    -   After submitting the case, the agent accesses the **Task SLAs** tab to view the SLA definitions that have been applied.

        The following example shows the task SLAs tab view of the SLA definitions.

        ![Task SLAs tab view of the SLA definitions.](../image/task-sla-playbook.png)

    -   The agent reviews the SLA definitions.

**Parent Topic:**[Dispute Content Pack for US Regulations](dispute-content-pack-for-us-regulation-landing-page.md)


---
title: Using the Dispute Content Pack for US Regulations
description: Dispute agents use the Dispute Content Pack for US Regulations to track the dispute cases that are governed by United States \(US\) Regulations \(Reg E and Reg Z\) and ensure they are in conformance with the regulatory guidance. This application provides the required Service Level Agreement \(SLA\) definitions and provide details to the dispute manager to monitor and take necessary actions.
locale: en-US
release: australia
product: Dispute Management
classification: dispute-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Dispute Content Pack for US Regulations, Dispute Management, Banking applications, Financial Services Operations \(FSO\)]
---

# Using the Dispute Content Pack for US Regulations

Dispute agents use the Dispute Content Pack for US Regulations to track the dispute cases that are governed by United States \(US\) Regulations \(Reg E and Reg Z\) and ensure they are in conformance with the regulatory guidance. This application provides the required Service Level Agreement \(SLA\) definitions and provide details to the dispute manager to monitor and take necessary actions.

## Dispute Content Pack for US Regulations workflows

When an agent disputes a transaction on behalf of a customer or through the Customer Service Portal or Consumer Service Portal, a dispute service case begins and the dispute card transaction flow is triggered. This flow includes the various tasks that are specific to the case details. Each task is created when an agent closes the previous task.

1.  Create a card dispute service case.

    The agent initiates the dispute service process by entering the initial case information and creating a dispute case on behalf of a customer.

2.  Initiate a dispute.
    -   The agent enters the dispute details, including the account that is being referenced, the dispute amount, and the type of dispute. The agent provides the necessary information for the available options in the type of dispute.
    -   In the dispute playbook, the agent chooses a card account. The applicable Service Level Agreement \(SLA\) is automatically mapped and is based on the selected account and the preconfigured logic for that transaction.

        **Note:** Regulation E \(Reg E\) manages the transactions from the savings and checking accounts, while Regulation Z \(Reg Z\) handles the credit card transactions, according to the applicable criteria.

    -   When the agent selects a transaction, the **Dispute reported date** field for the selected transaction record is populated with the current date and time. SLAs are calculated based on the **Dispute reported date** field.

        This field also displays in the case record in the Card Dispute Transaction related list.

        **Note:** The **Dispute reported date** field cannot be changed to a future date after it has been set.

        ![Card disputes transactions table with Dispute reported date column highlighted.](../image/reg-sla-dispute-reported-date.png)

3.  Submit the case for investigation.
    -   In the **Submit dispute** activity, the agent reviews the dispute amount. The agent selects the option **Is this a new financial account?** and submits the case for further investigation. For more information on the various stages, see [Overview of the Dispute Management workflow](../../fso-card-operations/concept/dispute-management-workflows.md).
    -   After submitting the case, the agent accesses the **Task SLAs** tab to view the SLA definitions that have been applied.

        The following example shows the task SLAs tab view of the SLA definitions.

        ![Task SLAs tab view of the SLA definitions.](../image/task-sla-playbook.png)

    -   The agent reviews the SLA definitions.
    -   The agent selects **Acknowledgement sent** at the case record to indicate that the dispute acknowledgement has been issued to the customer. It updates the **Acknowledgement sent** field for each transaction to Yes, and sets the acknowledgement limit SLA status to complete.

        ![Card disputes transactions tab showing the Acknowledgement sent button highlighted.](../image/reg-sla-acknowledgement-sent.png)

        The agent may also select **Acknowledgement sent** in the transaction record. This sets the **Acknowledgement sent** field to Yes for that specific transaction.


For more information, see [Initiate a dispute](../../fso-card-operations/task/create-case-with-intake-workspace.md#).

**Parent Topic:**[Dispute Content Pack for US Regulations](dispute-content-pack-for-us-regulation-landing-page.md)


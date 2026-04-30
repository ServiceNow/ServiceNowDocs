---
title: Managing dispute service requests
description: Dispute management enables agents to create dispute cases for both personal and business debit and credit card accounts, as well as non-card ACH transactions, and automate the process of dispute routing and fraud-related activities. Learn how agents initiate, investigate, and resolve dispute cases for personal and commercial customers.
locale: en-US
release: zurich
product: Dispute Management
classification: dispute-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Dispute Management, Banking applications, Financial Services Operations \(FSO\)]
---

# Managing dispute service requests

Dispute management enables agents to create dispute cases for both personal and business debit and credit card accounts, as well as non-card ACH transactions, and automate the process of dispute routing and fraud-related activities. Learn how agents initiate, investigate, and resolve dispute cases for personal and commercial customers.

By using the dispute service case and its associated tasks, you can manage dispute cases for your customers. Customers can dispute a transaction on their account due to several reasons, such as:

-   Unauthorized transactions
-   Fraudulent activities
-   Billing errors
-   Receipt of damaged, unsatisfactory, or returned goods
-   Any other valid reasons for dispute

## Automated workflow

Dispute management incorporates predefined workflows that streamline the process. When a dispute case is initiated, a dispute request flow is automatically generated, based to the specific case requirements. This workflow is based on the following factors:

-   Information provided during the initiation stage of the case.
-   Decisions made according to predefined business rules.
-   Inputs obtained from previous tasks.

The tasks assigned to a dispute case are determined by the information or decisions updated within the case. These dispute tasks are then assigned to dedicated dispute agents, who are prompted to perform follow-up actions, such as notifying the merchant and issuing provisional or final credit.

To resolve cases, agents perform various activities such as performing investigations, and initiating chargebacks for the tasks assigned to them. Both the case and its tasks are assigned to the assignment groups or agents by using assignment rules.

For more information, see [Overview of the Dispute Management workflow](dispute-management-workflows.md).

## Financial adjustments

Financial adjustments are changes made to an account during a dispute, such as issuing a temporary \(provisional\) credit, reversing it, or applying a final credit based on the outcome.

In Financial Services Operations, the Financial adjustments depend on the policies, Immediate Provisional Credit, Immediate Final Credit, and No credit.

## Regulatory SLAs

In addition to regular SLAs in the dispute management workflow, the Dispute Content Pack for US Regulations is available to enable issuers in the United States to track Service Level Agreement \(SLA\) due dates that align with regulatory guidelines.

For more information, see [Dispute Content Pack for US Regulations](../../dispute-content-pack-US-regulation/concept/dispute-content-pack-for-us-regulation-landing-page.md).

## Dashboards

ServiceNow® Performance Analytics give service owners insight into how the team and business are performing. A dashboard with customizable views is available for Card Operations Dispute Management. For more information, see [Dispute Management dashboard](../../../use/dashboards/application-content-packs/card-operations-dashboard.md).

-   **[Overview of the Dispute Management workflow](dispute-management-workflows.md)**  
ServiceNow® Dispute Management enables efficient card and non-card transaction dispute resolution, enhanced compliance, and streamlined customer experiences.
-   **[About dispute intake](dispute-intake-overview.md)**  
The dispute intake process is designed to capture the relevant information required for capturing dispute details. This can be through the customer or consumer service portal, agent workspace, or via Disputes intake via Virtual Agent.
-   **[Review a dispute from portal or workspace intake](../task/review-a-dispute-from-cardholder-intake.md)**  
Review dispute cases that customers submit through the dispute intake portal, or that contributors create in the intake workspace.
-   **[Managing Disputes](managing-disputes.md)**  
Create and manage dispute cases with various integrations such as Visa, Mastercard, or without any integrations.
-   **[Close a card dispute](../task/closure-dispute-case.md)**  
After you have completed all tasks in a card dispute case, you can add final details and close the case in the Closure playbook stage.

**Parent Topic:**[Dispute Management](dispute-management.md)


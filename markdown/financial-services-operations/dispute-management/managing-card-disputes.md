---
title: Managing dispute service requests
description: Dispute management enables agents to create dispute cases for both personal and business debit and credit card accounts, and automate the process of dispute routing and fraud-related activities. Learn how agents initiate, investigate, and resolve dispute cases for personal and commercial customers.
locale: en-US
release: yokohama
product: Dispute Management
classification: dispute-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Dispute Management, Using banking applications, Financial Services Operations \(FSO\)]
---

# Managing dispute service requests

Dispute management enables agents to create dispute cases for both personal and business debit and credit card accounts, and automate the process of dispute routing and fraud-related activities. Learn how agents initiate, investigate, and resolve dispute cases for personal and commercial customers.

By using the dispute service case and its associated tasks, you can manage dispute cases for your customers. Customers can dispute a transaction on their card account due to several reasons, such as:

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

For more information, see [Managing dispute workflows](dispute-management-workflows.md).

## Dashboards

ServiceNow® Performance Analytics give service owners insight into how the team and business are performing. A dashboard with customizable views is available for Card Operations Dispute Management.

-   **[Creating a card dispute case](../task/create-dispute-service-case.md)**  
An agent can begin the card dispute or report a dispute by creating a dispute case on behalf of a customer.
-   **[Working on a dispute case integrated with Visa](work-on-a-dispute-case-integrated-with-visa.md)**  
To improve the card dispute process, the playbook integrates with subflows that communicate with Visa. This integration supports an end-to-end dispute life cycle, from raising an initial dispute to the final resolution.
-   **[Configuring preconfigured email templates in a card dispute flow](pre-cofigured-email-template.md)**  
Email templates are pre-formatted files that you can use to start creating email notifications.
-   **[Implementing the 4-eyes policy for approval tasks](implementing-4-eyes-principle.md)**  
The 4-eyes policy, implemented in the case dispute flow, can enhance your dispute management process. This policy ensures that two authorized individuals handle the critical tasks and establish an efficient risk control mechanism.
-   **[Managing dispute manager workspace](workspace-for-dispute-manager.md)**  
As a dispute manager, you can work on your assigned cases and coordinate real-time updates on your team's cases from the dispute manager workspace.
-   **[Managing dispute agent workspace](workspace-for-agent.md)**  
The dispute agent workspace provides a single location for a dispute agent to process cases and tasks. An agent can use this workspace to respond to all task types, view the full context of an issue, and get relevant recommendations to help resolve issues.

**Parent Topic:**[Dispute Management](../../fso-deposit-operations/concept/dispute-management.md)


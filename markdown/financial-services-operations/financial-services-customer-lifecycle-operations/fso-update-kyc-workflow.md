---
title: Update KYC workflow
description: Learn how bank agents, using the Update KYC workflow, proactively contact a customer to update the KYC. The workflow applies to both business and personal CLO service requests.
locale: en-US
release: zurich
product: Financial Services Customer Lifecycle Operations
classification: financial-services-customer-lifecycle-operations
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Workflows, Use, Customer Lifecycle Operations, Common applications, Financial Services Operations \(FSO\)]
---

# Update KYC workflow

Learn how bank agents, using the Update KYC workflow, proactively contact a customer to update the KYC. The workflow applies to both business and personal CLO service requests.

The following diagram shows how the application helps bank agents to analyze a personal KYC non-compliance request, verify updated information, and process any necessary customer information updates.

![Workflow that shows how the KYC for a consumer is updated using the Client Lifecycle application. For the text description, refer to the workflow steps that follow.](../image/update-kyc-workflow.png "Update personal KYC workflow example")

The CLO admin can review and customize this predefined flow based on your organization's business needs.

The following workflow routes the case and tasks for updating a customer's KYC to agents in different departments. The agents log in to the Workspace to work on the tasks in their queue. Dedicated stages in the playbook experience guides agents through the steps and ensure that every step in the verification process is completed successfully.

-   **As a CLO agent or via an API**

    If the system observes that an update to a customer's KYC is required, an API in the backend triggers an Update KYC CLO service case. A CLO agent can also create this case.

-   **As back-office agents**

    In the case playbook, a CLO agent updates the compliance status in the Initiate and review stage and submits the application for fulfillment.

    The workflow triggers next tasks or a case based on the selected compliance status and the assignment rules route the associated case or tasks to the appropriate back-office teams.

    -   **KYC to be complied without address or name change**

        If the KYC compliance status is set as To be complied with no address change required, the workflow triggers these tasks for the back-office teams.

        1.  The CLO agent requests the necessary documentation from the customer. Once the documents are received, the agent marks the activity as complete.
        2.  The document agent reviews the collected documentation. If the documents are legitimate, the agent marks the task as complete.
        3.  The KYC agent performs the due diligence and evaluates the customer account for any adverse records or negative history. If the account meets the KYC standards of the financial institution, the agent marks the task as complete.
        4.  When all prior tasks are completed, a fulfillment CLO agent updates the account with KYC details in the core banking system, and closes the fulfillment CLO task.
        The case is complete and the state and stage of the case are set to Closed Complete.

    -   **KYC to be complied with address or name change**

        If the KYC compliance status is set as To be complied with an address or name change, the workflow automatically creates the **Address change** and **Name change** child cases to resolve the case.

        **Note:** The option for name change is available only in the Update personal KYC workflow. As a result, a child case for a name change is generated only for the Update personal KYC workflow.

        The new child cases then handle these issues.

        After the child cases are complete, the state and the stage of the parent case \(Update KYC\) are set to Closed Complete.

    -   **KYC non-compliant**

        If the compliance status is set to Non-compliant, the workflow automatically generates a CLO fulfilment task. A CLO agent updates the account with KYC non compliance in the core banking system and closes the task in the playbook.

        The case is complete and the state and stage of the case are set to Closed Complete.



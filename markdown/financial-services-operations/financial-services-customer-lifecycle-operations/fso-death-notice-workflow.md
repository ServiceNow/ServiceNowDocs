---
title: Notice of death workflow
description: Learn how agents, using the Notice of death workflow, manage a deceased client's financial accounts. The workflow applies to Client Lifecycle service requests.
locale: en-US
release: australia
product: Financial Services Customer Lifecycle Operations
classification: financial-services-customer-lifecycle-operations
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Workflows, Use, Customer Lifecycle Operations, Common applications, Financial Services Operations \(FSO\)]
---

# Notice of death workflow

Learn how agents, using the Notice of death workflow, manage a deceased client's financial accounts. The workflow applies to Client Lifecycle service requests.

The following diagram shows how the application helps bank agents resolve a case for notification of a customer's death. Agents can manage the accounts of a deceased client using dedicated flows for releasing funeral expense funds, freezing deposits, and closing other related accounts, all using one efficient, playbook-guided workflow.

![Workflow that shows how notification of death is handled using the CLO application. For the text description, refer to the workflow steps that follow.](../image/notice-death-workflow.png "Notice of death workflow example")

The CLO admin can review and customize this predefined flow based on your organization's business needs.

The following workflow routes the case and tasks for a customer's demise to agents in different departments. The agents log in to the Workspace to work on the tasks in their queue. The case playbook guides agents through the steps that are needed to fulfill the request.

-   **As a CLO contributor or via an API**

    A CLO contributor, such as a relationship manager, is notified about a customer's demise and submits a service request for notification of death and handling the customer's financial accounts.

    A case is created based on the request type.

    An API in the backend can also trigger a Notice of death CLO service case when a customer's demise is notified.

-   **As a CLO contributor**

    1.  In the Notice of death stage of the case playbook, the contributor enters the death notification details as received.
    2.  The contributor collects the necessary documentation and submits the application for fulfillment.
    A workflow generates further tasks and the assignment rules route the associated tasks to the appropriate back-office teams.

-   **As back-office agents**
    1.  The document agent works on the document task to review and verify the collected documentation. If the documents are legitimate, the agent marks the task as complete.
    2.  A CLO agent releases the requested funds for customer's funeral expenses and tax payment and closes the release funds CLO task.

        **Note:** The release funds task appears only when the **Release funds for funeral** or **Release funds for tax** options are selected in the death notification details stage.

    3.  A CLO agent freezes all deposit accounts associated with the deceased customer and closes the freeze deposit accounts CLO task.
    4.  If the asset value for the deceased customer exceeds the threshold for the probate amount set by the bank, the bank is required to collect the probate documents. In this case, additional tasks to collect and verify these documents appear in the playbook.
        1.  The CLO contributor collects the probate documentation and closes the task.
        2.  The document agent reviews the collected documentation and marks the document task as complete.
    5.  A CLO agent updates the customer's deposit account for any required updates in the core banking system, and closes the Update deposit account fulfillment CLO task.
    6.  The CLO agent updates all lending accounts \(such as loan or credit card\) that the deceased customer has with the bank. The agent then marks the Update lending account fulfillment CLO task as complete.
    7.  When all prior tasks are complete, the CLO agent updates the customer information in the core banking system and closes the fulfillment CLO task.

The case is complete and the state and stage of the case are set to Closed Complete.


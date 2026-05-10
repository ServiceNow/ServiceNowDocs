---
title: Financial Services Treasury Operations workflows
description: The Financial Services Treasury Operations application installs automated workflows that can be configured for any treasury service. These workflows create cases and route tasks to the treasury and document agents.
locale: en-US
release: australia
product: Financial Services Treasury Operations
classification: financial-services-treasury-operations
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Use, Treasury Operations, Banking applications, Financial Services Operations \(FSO\)]
---

# Financial Services Treasury Operations workflows

The Financial Services Treasury Operations application installs automated workflows that can be configured for any treasury service. These workflows create cases and route tasks to the treasury and document agents.

## Workflows available with this application

The following predefined workflows for treasury services are available with the application:

-   Remote Deposit Capture \(RDC\) Service
-   Wire Transfer Service

These workflows are built using [Process Automation Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/process-automation-designer.md) and [Flow Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/flow-designer.md). The treasury admin can review and customize these workflows according to the needs of their organization.

The following diagram shows how the application helps bank agents resolve a treasury request for onboarding RDC service.

![Workflow that shows how onboarding of RDC treasury service is completed using the treasury operations application. For the text description, refer to the workflow steps that follow.](../image/treasury-ops-rdc-workflow.png "Treasury operations workflow example for onboarding RDC service")

## General workflow for Treasury Operations

When a customer requires a treasury product, a treasury contributor initiates a case and updates its details, triggering the workflow. Throughout the workflow, treasury and document agents complete their assigned tasks and update the status of the case. The case playbook guides agents through the steps that are needed to resolve the case.

The following is a typical treasury workflow in the Financial Services Treasury Operations application.

**Note:** Depending on the service request type, a workflow might have additional or fewer tasks.

-   **As a customer**

    A customer contacts the financial institution and requests for a treasury service.

-   **As a treasury contributor**

    A treasury contributor, such as a relationship manager, submits a request for a treasury product activation or modification on behalf of the customer.

    1.  The contributor initiates a treasury product onboarding case.​
    2.  In the case playbook, the contributor updates the case details in the Initiate stage and submits the application.
    A workflow is triggered automatically and the assignment rules route the associated tasks to the appropriate back-office teams.

-   **As back-office agents**
    1.  In the case playbook, a treasury agent reviews the case details and performs a due diligence. If the applicant meets the standards of the financial institution, the agent marks the task as complete.

        **Note:** The due diligence task appears only for the RDC service workflow.

    2.  The document agent works on the document task to generate an agreement document, share it with the customer, and get an acceptance for it.

        The workflow generates fulfilment tasks for a treasury agent to work on them.

    3.  When all prior tasks are completed, a treasury agent activates the treasury service in their core treasury system, sends the service activation email to the customer, and starts the customer training for the treasury service.

The state and stage of the case is set to Closed Complete.

**Parent Topic:**[Using Financial Services Treasury Operations](using-treasury-ops.md)


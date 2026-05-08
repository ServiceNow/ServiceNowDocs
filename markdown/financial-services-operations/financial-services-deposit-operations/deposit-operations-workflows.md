---
title: Financial Services Deposit Operations workflows
description: The Financial Services Deposit Operations application installs automated workflows for origination, servicing, and closure of deposit accounts. These workflows enable routing of cases and tasks to different teams, including the deposit and document agents.
locale: en-US
release: australia
product: Financial Services Deposit Operations
classification: financial-services-deposit-operations
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Use, Deposit Operations, Banking applications, Financial Services Operations \(FSO\)]
---

# Financial Services Deposit Operations workflows

The Financial Services Deposit Operations application installs automated workflows for origination, servicing, and closure of deposit accounts. These workflows enable routing of cases and tasks to different teams, including the deposit and document agents.

## Workflows available with this application

The following predefined workflows for business and personal deposit account services are available with the application:

|Business deposit|Personal deposit|
|----------------|----------------|
|Originate business deposit account|Originate personal deposit account|
|Close business deposit account|Close personal deposit account|
|Add business standing order|Add personal standing order|
|Cancel business standing orders|Cancel personal standing orders|
|Modify business standing order|Modify personal standing order|
|Failed business standing order|Failed personal standing order|
|Manage financial relationship|Add financial account relationship|
| |Remove financial account relationship|
| |Modify financial account relationship|

These workflows are built using Process Automation Designer and Flow Designer. The deposit admin can review and customize these workflows according to the needs of their organization.

## General workflow for Deposit Operations

When a customer requires a deposit service, a deposit contributor initiates a case and updates its details, triggering the workflow. The flow triggers various tasks from the case and the assignment rules route these tasks to the agents in appropriate back-office teams such as deposit and document service. Throughout the workflow, agents complete their assigned tasks and update the status of the case. The case playbook guides agents through the steps that are needed to resolve the case.

The following is a typical workflow in the Financial Services Deposit Operations application.

**Note:** Depending on the service type, a workflow might have additional or fewer tasks.

1.  A customer contacts the financial institution and requests a deposit service.
2.  A deposit contributor, such as a relationship manager, creates the case, adds all applicable data, collects the necessary documentation from the customer, and submit the application.

    A document task is generated for the document agent.

3.  The document agent reviews the collected documentation. If the documents are legitimate, the agent marks the task as complete.

    Depending on the deposit service type, authorization and fulfillment tasks are created for deposit agents.

4.  The deposit agents evaluate the application and mark their individual tasks as complete.
5.  When all prior tasks are completed, a deposit agent updates the deposit account in the core deposit system to fulfill the service request.

The state and stage of the case is set to Closed Complete.

-   **[Add, modify, and cancel standing order workflows](fso-deposit-add-standing-order.md)**  
Learn how agents, using the standing order workflows, resolve service requests for adding, modifying, and canceling standing orders to deposit accounts. The workflows apply to both business and personal deposit service requests.
-   **[Failed standing order workflow](fso-failed-standing-order-workflow.md)**  
Learn how bank agents, using the failed standing order workflow, proactively contact a customer for a failed standing order for their deposit account and decide on an action plan. The workflow applies to both business and personal deposit accounts.
-   **[Add, modify, and remove financial account relationship workflows](fso-deposit-add-modify-relation-workflow.md)**  
Learn how agents, using the financial account relationship workflows, resolve service requests for adding, modifying, and removing relationships from deposit accounts. These workflows apply to personal deposit service requests.
-   **[Originate deposit account workflow](fso-originate-deposit-account.md)**  
Learn how agents, using the originate deposit account workflow, resolve service requests for opening a new deposit account. The workflow applies to both business and personal deposit service requests.
-   **[Close deposit account workflow](fso-close-deposit-account-workflow.md)**  
Learn how agents, using the Close deposit account workflow, resolve service requests for closing a checking or saving deposit account. The workflows apply to both business and personal deposit service requests.

**Parent Topic:**[Using Financial Services Deposit Operations](using-deposit-ops.md)


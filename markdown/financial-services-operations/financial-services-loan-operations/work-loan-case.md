---
title: Work on a loan service case
description: Review a loan case on a loan service request and update its details to trigger its workflow.
locale: en-US
release: zurich
product: Financial Services Loan Operations
classification: financial-services-loan-operations
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Use, Loan Operations, Banking applications, Financial Services Operations \(FSO\)]
---

# Work on a loan service case

Review a loan case on a loan service request and update its details to trigger its workflow.

## Before you begin

Role required:

-   For a business loan service case: sn\_bom\_loan\_b2b.agent or sn\_bom\_loan\_b2b.agent\_connector
-   For a personal loan service case: sn\_bom\_loan.b2c\_agent or sn\_bom\_loan.agent\_connector

**Important:** For the agent connector role to work, it must be combined with one of the CSM industry data model roles. For more information, see [Roles and Personas](../../fso-common/concept/fso-combine-csm-industry-roles.md).

## About this task

When a customer requests a loan service, a loan service case is created and assigned to a loan agent. After the loan agent updates the case details, the corresponding workflow is triggered. The flow triggers various tasks from the case and the assignment rules route these tasks to the appropriate back-office teams such as loan, credit, or document service. A new task is created when an agent closes the previous task. All tasks that are associated with the case appear in its **Tasks** tab.

**Note:** For the following loan workflows, agents can also use the case playbook that guides them through the steps that are needed to resolve the case.

-   Loan Forgiveness workflow for business loan operations
-   Loan Deferment workflow for personal loan operations

## Procedure

1.  Navigate to **All** &gt; **Financial Services Operations** &gt; **Workspace**.

2.  Select the lists icon \(![lists icon](../../../use/reporting/image/inline-data-vis-96px-list.png)\).

3.  In the **Lists** tab, under **Loan Service Cases**, open the case list.

    -   For your assigned tasks, click **Assigned to me**.
    -   For all document tasks, click **All**.
4.  In the list, select the case to work on.

    To work on a case that is not assigned to you yet, assign it to yourself by clicking **Assign to me**.

5.  Review the case and add additional details, such as information that is related to the fee.

6.  Click **Update and Continue**.


## Result

-   The case workflow triggers the next tasks for agents and the case moves to the next stage.
-   The document processor service determines the documents that must be verified for the case. The workflow automatically generates an inbound document verification task in the **Tasks** tab. The document task is created in the New state and assigned to an assignment group or a document agent in the document service team based on the assignment rule.


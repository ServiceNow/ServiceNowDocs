---
title: Work on a treasury service case
description: Work on a treasury case to collect applicant information, ensure that any outstanding tasks are completed, and fulfill the treasury product request.
locale: en-US
release: zurich
product: Financial Services Treasury Operations
classification: financial-services-treasury-operations
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Use, Treasury Operations, Banking applications, Financial Services Operations \(FSO\)]
---

# Work on a treasury service case

Work on a treasury case to collect applicant information, ensure that any outstanding tasks are completed, and fulfill the treasury product request.

## Before you begin

Role required: sn\_bom\_treasury.agent or sn\_bom\_treasury.agent\_connector

**Important:** For the agent connector role to work, it must be combined with one of the CSM industry data model roles. For more information, see [Roles and Personas](../../fso-common/concept/fso-combine-csm-industry-roles.md).

## About this task

When a customer requires a treasury product, a treasury contributor, such as a relationship manager, initiates a case and updates its details, triggering the workflow. Throughout the workflow, treasury and document agents complete their assigned tasks and update the status of the case.

**Note:** Depending on the treasury service request type, a workflow might have additional or fewer tasks.

Use the case playbook that provides the activities and tasks required to research and fulfill the request.

## Procedure

1.  Navigate to **All** &gt; **Financial Services Operations** &gt; **Workspace**.

2.  Select the lists icon \(![lists icon](../../../use/reporting/image/inline-data-vis-96px-list.png)\).

3.  In the **Lists** tab, under **Treasury Service Cases**, open the case list.

    -   For your assigned cases, click **Assigned to me**.
    -   For all treasury cases, click **All**.
4.  In the list, select the case to work on.

    To work on a case that is not assigned to you yet, assign it to yourself by clicking **Assign to me**.

5.  Select the **Playbook** tab.

    The case playbook guides agents through the steps that are involved in resolving a case.

6.  Use the activities and tasks under the following playbook stages to fulfill the request and resolve the case:

    -   **Initiate** to collect the customer information and submit application for activating a treasury service.
    -   **Due diligence** to perform due diligence.

        **Note:** This stage is available only for the RDC service workflow.

    -   **Agreement documents** to prepare agreement documents and share with the customer.
    -   **Fulfillment** to activate the requested treasury service, send service activation email to customer, initiate customer training, and close the case.
    Any tasks generated during playbook activities appear in the **Tasks** tab of the case.


## Result

-   The treasury case automatically updates to show Closed Complete.
-   The customer receives a treasury service activation email.

**Parent Topic:**[Using Financial Services Treasury Operations](../concept/using-treasury-ops.md)


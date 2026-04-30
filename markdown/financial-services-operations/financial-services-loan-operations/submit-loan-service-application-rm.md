---
title: Submit a loan service request as a loan contributor or agent connector
description: Collect all required information and documents from the customer and submit the loan service request to back-office agents for fulfilment.
locale: en-US
release: zurich
product: Financial Services Loan Operations
classification: financial-services-loan-operations
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Submitting a loan service request, Use, Loan Operations, Banking applications, Financial Services Operations \(FSO\)]
---

# Submit a loan service request as a loan contributor or agent connector

Collect all required information and documents from the customer and submit the loan service request to back-office agents for fulfilment.

## Before you begin

Role required: none

-   For a business loan service for a business customer \(account or contact\): sn\_bom\_loan\_b2b.contributor or sn\_bom\_loan\_b2b.agent\_connector
-   For a personal loan service for a consumer: sn\_bom\_loan.contributor or sn\_bom\_loan.agent\_connector

**Note:** The applicable universal contributor role can also be assigned to create a case. For more information, see [User roles and FSO Business rules](../../fso-common/reference/fso-core-roles.md).

**Important:** For the agent connector or contributor role to work, they must be combined with one of the roles in CSM industry data model or Contributor users. For more information, see [Roles and Personas](../../fso-common/concept/fso-combine-csm-industry-roles.md).

## About this task

As a loan contributor or agent connector, fill in the customer data, collect the required documents, and submit the application for the loan service request.

## Procedure

1.  Navigate to **All** &gt; **Financial Services Operations** &gt; **Workspace**.

2.  Select the lists icon \(![lists icon](../../../use/reporting/image/inline-data-vis-96px-list.png)\).

3.  In the **Lists** tab, under **Loan Service Cases**, click **All**.

4.  Click **New**.

5.  From the Create a new case dialog that appears, select a loan service and click **Create**.

    A loan service case is created.

6.  Fill in any necessary information that is related to the case.

    **Note:** Each loan service case form has a different set of fields that are based on the selected loan service.

7.  Click **Save**.

8.  In the **Inbound Documents** tab, collect customer documents, if any.

9.  Click **Update and Continue**.


## Result

-   The loan case is created and submitted for fulfilment.
-   A new task that is based on the workflow is automatically generated in the **Tasks** tab of the case. The new task is assigned to an assignment group or agent based on the assignment rule.
-   The customer receives a pre-configured email notification about the request submission.


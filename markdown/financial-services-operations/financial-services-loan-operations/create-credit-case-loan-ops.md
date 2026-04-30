---
title: Create a credit service case for a covenant breach or loan restructuring
description: Create a credit service case to handle a covenant breach or restructuring of a loan.
locale: en-US
release: zurich
product: Financial Services Loan Operations
classification: financial-services-loan-operations
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Use, Loan Operations, Banking applications, Financial Services Operations \(FSO\)]
---

# Create a credit service case for a covenant breach or loan restructuring

Create a credit service case to handle a covenant breach or restructuring of a loan.

## Before you begin

Role required:

-   For a business loan service for a business customer \(account or contact\): sn\_bom\_credit\_asmt.b2b\_agent, sn\_bom\_credit\_asmt.b2b\_agent\_connector, or sn\_bom\_credit\_asmt.b2b\_contributor
-   For a personal loan service for a consumer: sn\_bom\_credit\_asmt.b2c\_agent, sn\_bom\_credit\_asmt.b2c\_agent\_connector, or sn\_bom\_credit\_asmt.b2c\_contributor

**Note:** The applicable universal contributor role can also be assigned to create a case. For more information, see [User roles and FSO Business rules](../../fso-common/reference/fso-core-roles.md).

**Important:** For the agent connector or contributor role to work, they must be combined with one of the roles in CSM industry data model or Contributor users. For more information, see [Roles and Personas](../../fso-common/concept/fso-combine-csm-industry-roles.md).

## About this task

An API in the backend can also trigger a Covenant Breach credit service case when a breach is observed for a loan.

## Procedure

1.  Navigate to **All** &gt; **Financial Services Operations** &gt; **Workspace**.

2.  Select the lists icon \(![lists icon](../../../use/reporting/image/inline-data-vis-96px-list.png)\).

3.  In the **Lists** tab under **Credit Service Cases**, click **All**.

4.  Click **New**.

5.  In the New Credit Service Case dialog box, select the credit service that you want to create a case for.

    -   To handle a covenant breach of a loan, select **Covenant Breach**.
    -   To propose restructuring of a loan, select **Loan Restructure Proposal**.
6.  Click **Create**.

7.  On the form, fill in the required fields and any other related information that you've gathered from the customer.

8.  Click **Save**.


## Result

The credit service case is created in the New state and is assigned to an assignment group or credit agent in the credit operations team. The assignment group or user that the case is assigned to is based on the assignment rules.

## What to do next

As a credit agent, if the case is not assigned to you, you can assign the case to yourself and start working on it. You can also assign the case to any other credit agent.


---
title: Financial Services Loan Operations workflows
description: The Financial Services Loan Operations application installs automated workflows for loan servicing. These workflows enable routing of cases and tasks to different departments, including the loan, document, and credit agents.
locale: en-US
release: australia
product: Financial Services Loan Operations
classification: financial-services-loan-operations
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Use, Loan Operations, Banking applications, Financial Services Operations \(FSO\)]
---

# Financial Services Loan Operations workflows

The Financial Services Loan Operations application installs automated workflows for loan servicing. These workflows enable routing of cases and tasks to different departments, including the loan, document, and credit agents.

## Workflows available with the application

The following predefined workflows for business and personal loans are available with the application:

<table id="table_l3g_4lw_vnb"><thead><tr><th>

Personal loans

</th><th>

Business loans

</th></tr></thead><tbody><tr><td>

Partial Prepayment

</td><td>

Partial Prepayment

</td></tr><tr><td>

Loan Forgiveness

</td><td>

Loan Forgiveness

</td></tr><tr><td>

Loan Deferment

</td><td>

Loan Deferment

</td></tr><tr><td>

Loan Write-Off

</td><td>

Loan Write-Off

</td></tr><tr><td>

Missed Repayment

</td><td>

Missed Repayment

</td></tr><tr><td>

Covenant Breach

</td><td>

Covenant Breach**Note:** This workflow is initiated from the Financial Services Credit Operations application.

</td></tr><tr><td>

Loan Restructuring

</td><td>

Loan Restructuring**Note:** This workflow is initiated from the Financial Services Credit Operations application. From there, a loan case is automatically created to take the request to completion.

</td></tr><tr><td>

 

</td><td>

Loan Drawdown

</td></tr><tr><td>

 

</td><td>

Loan Rollover

</td></tr></tbody>
</table>These workflows are built using Flow Designer. The loan admin can review and customize these predefined flows that are based on the business needs of an organization.

## General workflow for Loan Operations

When a customer requests a loan service, a loan service case is created and assigned to a loan agent. After the agent updates the case details, a workflow is triggered. The flow triggers various tasks from the case and the assignment rules route these tasks to the appropriate back-office teams such as loan, credit, or document service. A new task is automatically created when an agent closes the previous task.

The following is a typical loan workflow in the Financial Services Loan Operations application.

**Note:** Depending on the request type, individual workflows might have additional or fewer tasks.

1.  A loan contributor, requester, or a customer submits a loan service request.
2.  The loan contributor collects the required customer documents and updates the case.
3.  A loan agent receives the case and adds additional information, such as the fee.
4.  The document processor service determines the documents that are required. If any documents must be verified, a task is generated for the document agent.
5.  A credit task is generated for the credit agent.
6.  An authorization task is generated to review and approve the loan request.
7.  After the authorization, a loan update task is generated. If the bank has enabled an integration, the loan account could get automatically updated in the core system.


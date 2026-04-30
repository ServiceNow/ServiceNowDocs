---
title: Customer Lifecycle Operations workflows
description: Financial Services Customer Lifecycle Operations \(CLO\) installs automated workflows for reviewing and approving customer account applications. These workflows create cases and route tasks to different agents, including KYC, document, tax, and credit agents.
locale: en-US
release: zurich
product: Financial Services Customer Lifecycle Operations
classification: financial-services-customer-lifecycle-operations
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Use, Customer Lifecycle Operations, Common applications, Financial Services Operations \(FSO\)]
---

# Customer Lifecycle Operations workflows

Financial Services Customer Lifecycle Operations \(CLO\) installs automated workflows for reviewing and approving customer account applications. These workflows create cases and route tasks to different agents, including KYC, document, tax, and credit agents.

## Workflows available with this application

The following predefined workflows for business and client lifecycle services are available with the application:

<table id="table_l3g_4lw_vnb"><thead><tr><th>

Business Lifecycle

</th><th>

Client Lifecycle

</th></tr></thead><tbody><tr><td>

Onboard new account

</td><td>

Onboard new customer

</td></tr><tr><td>

Onboard new contact

</td><td>

Notice of death

</td></tr><tr><td>

Update business KYC

</td><td>

Update personal KYC

</td></tr><tr><td>

Address change for account

</td><td>

Address change for customer

</td></tr><tr><td>

 

</td><td>

Name change of customer

</td></tr></tbody>
</table>These workflows are built using [Process Automation Designer](https://www.servicenow.com/docs/access?context=process-automation-designer&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US) and [Flow Designer](https://www.servicenow.com/docs/access?context=flow-designer-home-landing-page&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US). The CLO admin can review and customize these workflows according to their organization's needs.

## General workflow for Financial Services Customer Lifecycle Operations

When a customer requires a service, a CLO contributor initiates a case and updates its details, triggering the workflow. The flow triggers various tasks from the case and the assignment rules route these tasks to the agents in appropriate back-office teams such as deposit and document service. Throughout the workflow, agents complete their assigned tasks and update the status of the case. The case playbook guides agents through the steps that are needed to resolve the case.

**Note:** Depending on the CLO service type, a workflow might have additional or fewer tasks.


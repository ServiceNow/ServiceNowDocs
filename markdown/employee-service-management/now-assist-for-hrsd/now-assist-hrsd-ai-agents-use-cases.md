---
title: Using agentic workflows in Now Assist for HR Service Delivery \(HRSD\)
description: Use the Now Assist for HR Service Delivery \(HRSD\) agent collection to complete tasks autonomously.
locale: en-US
release: xanadu
product: Now Assist for HRSD
classification: now-assist-for-hrsd
topic_type: concept
last_updated: "2025-03-07"
reading_time_minutes: 2
keywords: [Now Assist, generative AI]
breadcrumb: [Now Assist for HR Service Delivery \(HRSD\), HR Service Delivery, Employee Service Management]
---

# Using agentic workflows in Now Assist for HR Service Delivery \(HRSD\)

Use the Now Assist for HR Service Delivery \(HRSD\) agent collection to complete tasks autonomously.

<table id="table_gyx_brq_l2c"><thead><tr><th>

Agentic workflow name

</th><th>

Description

</th><th>

Available AI agents

</th></tr></thead><tbody><tr><td>

Resolve policy for tuition reimbursement

</td><td>

AI agents resolve tuition reimbursement requests by connecting to various parties \(for example, the manager for approval\) and resolving the case, while keeping the human agent in the loop.

</td><td>

-   Tuition reimbursement requestor information retrieval AI agent
-   Tuition reimbursement eligibility check AI agent
-   Tuition reimbursement checklist creator AI agent
-   Total rewards case closure AI agent
-   Total rewards case details management AI agent
-   Tuition reimbursement pre-approval task creation AI agent
-   Tuition reimbursement policy retrieval AI agent

</td></tr></tbody>
</table><table id="table_qxx_bcg_vfc"><thead><tr><th>

Available AI Agent

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Worker profile retriever AI agent

</td><td>

Calls an integration subflow to assist the employee in finding out details about a colleague. The details could include the department, job, email, or phone number that is based on the employee's request by name.

</td></tr><tr><td>

Employee holiday calendar retrieval AI agent

</td><td>

Retrieves the holiday information for the specified year.

</td></tr><tr><td>

Time off requester AI agent

</td><td>

Calls an integration to assist in leave-related requests:-   Request time off
-   Get my time off balance

</td></tr><tr><td>

Employee total rewards information AI agent

</td><td>

Retrieves the total rewards details of an employee.

</td></tr><tr><td>

Benefits enrollment retriever AI agent

</td><td>

Calls an integration subflow to get the benefits information that an employee has signed up for.

</td></tr><tr><td>

Employee details updater AI agent

</td><td>

Calls an integration to assist in personal details related requests:-   Update email address
-   Update address
-   Update phone number
-   Update blood type
-   Update date of birth

</td></tr><tr><td>

HCM feedback retriever AI agent

</td><td>

Calls an integration subflow to assist the employee in getting the feedback that they have received in HCM from their managers.

</td></tr><tr><td>

Expense Manager AI agent

</td><td>

Fetches expense details to create and submit and expense report.

</td></tr></tbody>
</table>**Important:** All agentic workflow and AI agent records are read-only by default.

To run the AI agents autonomously, you must first duplicate the agentic workflow, and then do the following steps:

-   Activate the agentic workflow.
-   Activate all agents within the agentic workflow.
-   Activate the trigger to invoke the agentic workflow automatically. If you prefer to invoke it manually, activating the trigger isn't necessary.

Looking for an AI agent?

-   There might be AI agents installed with the Now Assist application that are not used in agentic workflows. To learn how to see all agents that are available on your instance, see [Find AI agents](https://www.servicenow.com/docs/access?context=find-ai-agents&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US).
-   To find agents that might not be installed on your instance, visit the [AI Agent Marketplace](https://store.servicenow.com/store/ai-marketplace) on the ServiceNow Store.


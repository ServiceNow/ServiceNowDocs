---
title: Using agentic workflows in Now Assist for HRSD
description: Use the HR Service Delivery AI agent collection to complete tasks autonomously.
locale: en-US
release: australia
product: Now Assist for HRSD
classification: now-assist-for-hrsd
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
keywords: [Now Assist, generative AI]
breadcrumb: [Now Assist for HR Service Delivery \(HRSD\), HR Service Delivery, Employee Service Management]
---

# Using agentic workflows in Now Assist for HRSD

Use the HR Service Delivery AI agent collection to complete tasks autonomously.

<table id="table_gyx_brq_l2c"><thead><tr><th>

Agentic workflow name

</th><th>

Description

</th><th>

Available AI agents

</th></tr></thead><tbody><tr><td>

Help resolve tuition requests

</td><td>

AI agents resolve tuition reimbursement pre-approval requests by connecting to various parties \(for example, the manager for approval\) and resolving the case, while keeping the human agent in the loop.

</td><td>

-   Tuition reimbursement policy based HR case evaluation AI agent
-   Tuition reimbursement case closure AI agent
-   Tuition reimbursement preapproval task generation AI agent

</td></tr><tr><td>

Help resolve tuition reimbursement requests

</td><td>

AI agents resolve tuition reimbursement requests that were already pre-approved and the employee completed the course.

</td><td>

-   Tuition reimbursement request evaluator AI agent
-   Tuition reimbursement request closure AI agent

</td></tr><tr><td>

Predict service and transfer HR cases

</td><td>

Analyze an HR case and automatically route it to the most appropriate HR service.

</td><td>

-   Record field value prediction AI agent
-   HR Case Transfer AI Agent

</td></tr><tr><td>

Resolve noncritical HR cases

</td><td>

Use the Resolve noncritical HR cases agentic workflow to assess the criticality of HR cases and automatically respond to noncritical inquiries without human intervention. Human agents must intervene when requests are marked critical.

</td><td>

-   HR search and notify AI agent
-   HR criticality detection AI agent

</td></tr><tr><td>

Resolve critical HR cases

</td><td>

Resolve critical HR requests efficiently with the Resolve critical HR case agentic workflow. This workflow generates a tailored fulfillment plan for an HR case using fulfillment instructions, KB articles, or resolution notes of similar past cases. It helps accelerate the resolution process by providing planning support to HR agents.

</td><td>

-   HR Case Planner AI Agent
-   Next action recommended AI agent

</td></tr><tr><td>

Schedule interviews

</td><td>

AI agents collect necessary inputs from the recruiters or recruitment coordinators and schedule interviews seamlessly from the Now Assist panel.

</td><td>

Interview schedule AI agent

</td></tr><tr><td>

Create job requisition

</td><td>

AI agents assist hiring managers in creating requisitions more efficiently and accurately on the first attempt by providing the necessary guidance through the agentic workflow.

</td><td>

Job requisition creation AI agent

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

Expense manager AI agent

</td><td>

Fetches expense details to create and submit and expense report.

</td></tr><tr><td>

View paychecks AI agent

</td><td>

Retrieves paycheck information for the selected period.

</td></tr><tr><td>

Record field value prediction AI agent

</td><td>

Predicts the HR service of an incoming case. It can also provide a summary and justification of prediction.

</td></tr><tr><td>

HR Case Transfer AI Agent

</td><td>

Automatically transfers the case to the predicted service.

</td></tr><tr><td>

HR search and notify AI agent

</td><td>

Performs search to find relevant HR knowledge articles and catalog items related to the given query and raise notification if relevant information is found.

</td></tr><tr><td>

HR criticality detection AI agent

</td><td>

Performs criticality detection on an HR case and acts based on the criticality level.

</td></tr><tr><td>

HR Case Planner AI Agent

</td><td>

Creates an ordered step-wise fulfillment/execution plan for an HR case based on specific COE or HR service.

</td></tr><tr><td>

Next action recommended AI agent

</td><td>

Identifies the optimal steps for resolving tasks by referencing similar case details, reviewing relevant knowledge articles and web search results. It summarizes and presents to the user a step-by-step summarized resolution plan and derived action plan. Implements the feedback flow only when asked for it.

</td></tr></tbody>
</table>**Important:** All agentic workflow and AI agent records are read-only by default.

To run the AI agents autonomously, you must first duplicate the agentic workflow, and then do the following steps:

-   Activate the agentic workflow.
-   Activate all agents within the agentic workflow.
-   Activate the trigger to invoke the agentic workflow automatically. If you prefer to invoke it manually, activating the trigger isn't necessary.

For more information about duplicating an agentic workflow, implementing access control lists and activating the required components, see the following topics:

-   [Duplicate an agentic workflow](https://www.servicenow.com/docs/access?context=clone-aia-usecase&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)
-   [Activate an agentic workflow template](https://www.servicenow.com/docs/access?context=activate-aia-use-case&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)
-   [Modify an AI agent](https://www.servicenow.com/docs/access?context=modify-ai-agent&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)

There might be AI agents installed with the Now Assist application that are not used in agentic workflows. To learn how to see all agents that are available to you, see [Find AI agents](https://www.servicenow.com/docs/access?context=find-ai-agents&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

**Note:** Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents. For more information, see [ServiceNow product tiers](https://www.servicenow.com/docs/access?context=ai-native-sku-overview&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

**Important:** Some Now Assist skills, agents, and agentic workflows are turned on by default. For more information, see [Now Assist skills, agents, and agentic workflows on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).


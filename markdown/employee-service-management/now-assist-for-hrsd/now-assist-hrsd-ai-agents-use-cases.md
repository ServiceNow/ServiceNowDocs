---
title: Using agentic workflows in Now Assist for HRSD
description: Use the HR Service Delivery AI agent collection to complete tasks autonomously.
locale: en-US
release: yokohama
product: Now Assist for HRSD
classification: now-assist-for-hrsd
topic_type: concept
last_updated: "2025-03-07"
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

</td></tr><tr><td>

Resolve HR cases

</td><td>

Automate the resolution of routine employee queries submitted via portal or email by leveraging agents to assess criticality and retrieve relevant knowledge article responses.Create an ordered step-wise HR case fulfillment/execution plan.

</td><td>

-   HR search retrieval AI agent
-   HR notification AI agent
-   Record management AI agent
-   HR criticality detection AI agent
-   HR Case Planner AI Agent

</td></tr><tr><td>

Generate onboarding ramp-up plan

</td><td>

Provides an efficient process for helping managers generate personalized onboarding plans for new employees who are joining their organization. The workflow uses Journey Accelerator to create a plan and tasks associated with the employee's onboarding journey. The manager uses Now Assist in Virtual Agent to review, revise, and accept the onboarding ramp-up plan that was curated by the AI agent.

</td><td>

-   Ramp up plan gather inputs AI agent
-   Ramp up plan generation AI agent
-   Ramp up plan review AI agent

</td></tr><tr><td>

Help Plan Growth Conversations

</td><td>

AI agents work together to help managers select a reportee, create and retrieve upcoming conversations, generate employee data summaries with talking points from talent development activities, and recommend resources and learning courses for effective preparation.

</td><td>

-   Conversation management AI agent
-   Employee data summarization AI agent
-   Manager resource recommendation AI agent

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

</td></tr></tbody>
</table>**Important:** All agentic workflow and AI agent records are read-only by default.

To run the AI agents autonomously, you must first duplicate the agentic workflow, and then do the following steps:

-   Activate the agentic workflow.
-   Activate all agents within the agentic workflow.
-   Activate the trigger to invoke the agentic workflow automatically. If you prefer to invoke it manually, activating the trigger isn't necessary.

For more information about duplicating an agentic workflow, implementing access control lists and activating the required components, see the following topics:

-   [Duplicate an agentic workflow](https://www.servicenow.com/docs/access?context=clone-aia-usecase&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)
-   [Activate an agentic workflow template](https://www.servicenow.com/docs/access?context=activate-aia-use-case&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)
-   [Modify an AI agent](https://www.servicenow.com/docs/access?context=modify-ai-agent&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)
-   [Implement access control in Now Assist AI agents](https://www.servicenow.com/docs/access?context=aia-security-implementation&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)

Looking for an AI agent?

-   There might be AI agents installed with the Now Assist application that are not used in agentic workflows. To learn how to see all agents that are available on your instance, see [Find AI agents](https://www.servicenow.com/docs/access?context=find-ai-agents&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).
-   To find agents that might not be installed on your instance, visit the [AI Agent Marketplace](https://store.servicenow.com/store/ai-marketplace) on the ServiceNow Store.

**Important:** Some Now Assist skills, agents, and agentic workflows are turned on by default. For more information, see [Now Assist skills, agents, and agentic workflows on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).

-   **[Help resolve tuition requests agentic workflow for Now Assist for HRSD](now-assist-hrsd-ai-agents-policy-resolving-tr-usecase.md)**  
Use the Help resolve tuition requests agentic workflow for faster mean time to repair \(MTTR\) cases that require validation based on policies that are built for tuition reimbursement.
-   **[Resolve HR cases agentic workflow](employee-issue-resolver-na.md)**  
Use the Resolve HR cases agentic workflow to evaluate case criticality and retrieve relevant knowledge articles to resolve HR cases, and generate a fulfillment plan for an HR case, minimizing the need for agent intervention.
-   **[Generate onboarding ramp-up plan agentic workflow](onboarding-ramp-up-plan-agentic-wf.md)**  
The Generate onboarding ramp-up plan agentic workflow is an AI-powered solution that helps managers at your organization onboard new employees more efficiently. This workflow uses AI agents to generate personalized plans that are designed to elevate the knowledge and skills of new employees beginning to embark on their onboarding journey.
-   **[HCM AI agents](conversational-agents.md)**  
Place requests to the Human Capital Management \(HCM\) system using the HR Service Delivery AI agent collection.

**Parent Topic:**[Now Assist for HR Service Delivery \(HRSD\)](now-assist-hrsd.md)


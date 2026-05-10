---
title: Using agentic workflows in Now Assist for Telecommunications, Media and Technology \(TMT\)
description: Use the Now Assist for TMT agentic workflows to complete tasks autonomously.
locale: en-US
release: australia
product: Now Assist for Telecom, Media and Technology
classification: now-assist-for-telecom-media-and-technology
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Now Assist for TMT, Telecommunications, Media, and Technology \(TMT\)]
---

# Using agentic workflows in Now Assist for Telecommunications, Media and Technology \(TMT\)

Use the Now Assist for TMT agentic workflows to complete tasks autonomously.

<table id="table_lxk_lck_h2c"><thead><tr><th>

Agentic workflow name

</th><th>

Description

</th><th>

Available AI agents

</th></tr></thead><tbody><tr><td>

Test and repair telecom service issues

</td><td>

The agentic workflow gets triggered when the service problem case is assigned to the case agent and the state of the case is Open or New. The customer raises a case on the service disruption.

 The service problem case \(SPC\) starts with the SPC number.

 This AI agent is designed to handle the service problem case requests that require troubleshooting, diagnostics, analysis, or resolution for a task \(case\), when an identifier or description for the task is given. It’s also capable of retrieving relevant context and details related to the task given to them.

 AI agents perform their tasks to resolve the customer issue.

</td><td>

-   Service problem manager AI agent
-   Customer payment status AI agent
-   Preliminary troubleshooter AI agent
-   On-demand service tester AI agent
-   Service repairer AI agent

</td></tr><tr><td>

Help remediate bill issues

</td><td>

The agentic workflow is designed to handle billing inquiry requests by analyzing current invoice usage, providing insights into high bill usage, and suggesting alternative plans based on customer usage patterns. For example, if a customer with a domestic mobile connection uses it internationally, they may incur extra charges; our bill analysis can identify such international usage and provide optimal plan to help manage costs.

</td><td>

-   Billing account information collector AI agent
-   Recommended plans AI agent
-   Billing invoice data collector AI agent

</td></tr><tr><td>

Analyze network incidents

</td><td>

Assists customer agents in resolving a given incident. It helps customer agents to resolve network tickets by tracking it and creating an actionable task.

</td><td>

-   Network ticket resolution AI agent
-   Ticket readiness AI agent
-   Network correlation monitor AI agent
-   Network ticket actionable steps generation AI agent
-   Network remediation generation AI agent

</td></tr><tr><td>

Analyze risks and recommend solutions

</td><td>

Retrieves applicable risks and proactively suggests solutions with minimal user intervention.

</td><td>

Success risk manager AI agent

</td></tr><tr><td>

Monitor engagement health

</td><td>

Monitors the health score trends for all active engagements and triggers risk signals when declined.

</td><td>

-   Success trend AI agent
-   Success health monitor AI agent

</td></tr><tr><td>

Support renewals and expansion

</td><td>

Assesses engagements due for renewal, analyzes trends, and recommends renewal strategies.

</td><td>

-   Renewal analysis AI agent
-   Value realization assessor AI agent
-   Success insight AI agent

</td></tr><tr><td>

Trigger risk mitigation touchpoint

</td><td>

Automates the creating and scheduling of meetings for a specific user.

</td><td>

-   Meeting draft creator AI agent
-   Draft meeting scheduler AI agent

</td></tr><tr><td>

Service Exchange onboarding

</td><td>

Assists the provider with the consumer registration process, including step-by-step guidance, error checks during registration, and support for resolving any errors.

</td><td>

-   Registration Initiator AI agent
-   Registration Error Monitor AI agent

</td></tr><tr><td>

Customer voice quality issue resolution

</td><td>

Assists customer service representatives in resolving customer voice quality issues.

</td><td>

-   Ticket creation AI agent
-   Customer interaction context gatherer AI agent
-   RADCOM ticket handling agent customer profile \(External agent\)

</td></tr><tr><td>

Squad resource identifier

</td><td>

Assists the customer success teams to quickly identify and connect with the right individuals to support success plays, initiatives, or critical escalations, ensuring faster and more effective collaboration across engagements.

</td><td>

User resource recommender AI agent

</td></tr><tr><td>

Product release email communication

</td><td>

Assist the customer to automatically draft, refine, and distribute the release announcement emails to designated recipients by retrieving the most recent product release information.

</td><td>

Email communication manager AI agent

</td></tr></tbody>
</table>Enable security implementation to execute AI agents and agentic workflows through access control lists \(ACLs\) and user identities. ACLs provide the Run As capability to let agents and agentic workflows execute actions either as a dynamic user or as an AI user. For more information, see [Implement access control in Now Assist AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aia-security-implementation.md).

**Important:** By default, all agentic workflows and AI agent records are read only.

To run the AI agents autonomously, you must first duplicate the agentic workflow, and then proceed with the following steps:

-   Activate the agentic workflow.
-   Activate all agents within the agentic workflow.
-   Activate the trigger to invoke the agentic workflow automatically. If you prefer to invoke it manually, activating the trigger isn’t necessary.

Once you [duplicate](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/clone-aia-usecase.md) the agentic workflow, adjust the settings according to your requirements. Next, you [activate](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/activate-aia-use-case.md) the duplicated agentic workflow. You can also [test](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/test-aia-use-case.md) the agentic workflow to analyze its performance in the AI Agent Studio, while it executes the instructions that you defined.

There might be AI agents installed with the Now Assist application that are not used in agentic workflows. To learn how to see all agents that are available to you, see [Find AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/find-ai-agents.md).


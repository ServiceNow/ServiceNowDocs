---
title: Using agentic workflows in Now Assist for Customer Service Management \(CSM\)
description: Use the AI agent collection for Customer Service Management to improve productivity through faster triaging. You can gather, verify, respond to, or escalate emails from customers as interactions or cases. You can also process the high volume of cases coming through offline channels, converting them into actionable tasks to significantly reduce the workload of human agents.
locale: en-US
release: xanadu
product: Now Assist for CSM
classification: now-assist-for-csm
topic_type: concept
last_updated: "2025-02-18"
reading_time_minutes: 1
keywords: [Generative AI, generative AI for Customer Service Management, generative AI for customer service agents]
breadcrumb: [Now Assist for Customer Service Management \(CSM\), Customer Service Management]
---

# Using agentic workflows in Now Assist for Customer Service Management \(CSM\)

Use the AI agent collection for Customer Service Management to improve productivity through faster triaging. You can gather, verify, respond to, or escalate emails from customers as interactions or cases. You can also process the high volume of cases coming through offline channels, converting them into actionable tasks to significantly reduce the workload of human agents.

<table id="table_xt1_lth_l2c"><thead><tr><th>

agentic workflow

</th><th>

Description

</th><th>

Available AI agents

</th></tr></thead><tbody><tr><td>

Triage cases

</td><td>

Handles end-to-end case or case type validation, creation, verification, and escalation. It can also retrieve relevant context and details from the provided case or interaction to address customer inquiries directly and avoid unnecessary case creation.

</td><td>

-   Triage cases planner
-   Context validator and analyzer
-   Duplicate identification
-   Informational queries
-   Transactional queries
-   Case creation
-   Entity extraction
-   Document verification
-   Email response

</td></tr></tbody>
</table>Enable security implementation to execute AI agents and agentic workflows through Access Control Lists \(ACLs\) and user identities. For more information, see [Implement access control in Now Assist AI agents](https://www.servicenow.com/docs/access?context=aia-security-implementation&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)

**Important:** By default, all agentic workflows and AI agent records are read only.

To run the AI agents autonomously, you must first [duplicate the agentic workflow](https://www.servicenow.com/docs/access?context=clone-aia-usecase&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US), and then proceed with the following steps:

-   Activate the agentic workflow.
-   Activate all agents within the agentic workflow.
-   Activate the trigger to invoke the agentic workflow automatically. If you prefer to invoke it manually, activating the trigger isn’t necessary.

For information about Triage cases, see [Customer Service Management AI agent collection triage cases agentic workflow](case-resolving-use-case.md).

Looking for an AI agent?

-   There might be AI agents installed with the Now Assist application that are not used in agentic workflows. To learn how to see all agents that are available on your instance, see [Find AI agents](https://www.servicenow.com/docs/access?context=find-ai-agents&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US).
-   To find agents that might not be installed on your instance, visit the [AI Agent Marketplace](https://store.servicenow.com/store/ai-marketplace) on the ServiceNow Store.


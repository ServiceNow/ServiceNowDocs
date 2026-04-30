---
title: Customer Service Management accelerate complaint case handling AI agent collection
description: The Accelerate complaint case handling agents can work alongside human complaint agents to intake complaints, triage complaints, summarize cases, and answer research queries. The agents review previously attempted troubleshooting steps and propose resolution plans based on similar complaint cases or knowledge articles.
locale: en-US
release: zurich
product: Now Assist for CSM
classification: now-assist-for-csm
topic_type: concept
last_updated: "2025-11-25"
reading_time_minutes: 2
breadcrumb: [Use agentic AI in CSM, Now Assist for CSM, Customer Service Management]
---

# Customer Service Management accelerate complaint case handling AI agent collection

The Accelerate complaint case handling agents can work alongside human complaint agents to intake complaints, triage complaints, summarize cases, and answer research queries. The agents review previously attempted troubleshooting steps and propose resolution plans based on similar complaint cases or knowledge articles.

The Accelerate complaint case handling collection includes AI agents, skills, and a specialized AI workflow that systematically analyzes complaint cases, determines optimal processing paths, and coordinates seamless hand-offs between specialized sub-agents. This agent excels at complaint intake, contextual triage, prioritization logic, and ensuring comprehensive case resolution based on case state, complexity factors, and historical resolution patterns.

## AI agents used in the Accelerate complaint case handling collection and the Accelerate complaint case handling agentic workflow

The accelerate complaint case handling collection and agentic workflow uses a team of AI agents and skills to triage customer complaints, summarize cases, and help research customer cases. The complaint case intake agent is not part of the agentic workflow, since it is used with Virtual Agent.

To install the AI agents and skills for the Accelerate complaint case handling collection, see [Install the Now Assist for Complaint Case \(CSM\) application](../task/acc-complaint-case-handling-collection.md).

For more information on configuring the Accelerate complaint case handling agentic workflow, see [Configure the Accelerate Complaint Case Handling agentic workflow](../task/acc-complaint-case-handling-agentic-wkfl.md).

<table id="table_bst_k4t_mhc"><thead><tr><th>

Agent

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Complaint case intake agent

</td><td>

Manages customer complaints by collecting relevant information, such as customer details, the nature of the complaint, and any supporting documentation, before initiating the resolution process. 

</td></tr><tr><td>

Complaint case triage agent

</td><td>

Derives category, subcategory, and priority of the case. The agent also analyzes tone, sentiment, word choice, and speech patterns to detect frustration of the customers. It uses this information to determine the priority of the case.

</td></tr><tr><td>

Complaint case research agent

</td><td>

Helps the human agent by providing the best answer to research queries. It retrieves relevant knowledge base articles and similar cases, and if needed, gets relevant information from other systems to give accurate answers and create case tasks based on the context.

</td></tr><tr><td>

Complaint case summarization skill

</td><td>

Produces structured summaries of complaint cases surfacing complaint-specific context, including the product or location at the center of the complaint, related parties involved, key actions taken, and SLA urgency ranked by time remaining. The skill allows agents to understand the full complaint picture without reading through the entire activity stream.

 It is especially valuable during complaint intake reviews, escalations, cross-team handoffs, or when returning to an active complaint after a period of inactivity.

</td></tr></tbody>
</table>
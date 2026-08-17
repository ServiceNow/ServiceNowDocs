---
title: AI Agents for CSM - Complaint Case
description: The AI Agents for CSM - Complaint Case can work alongside human complaint agents to intake complaints, triage complaints, summarize cases, and answer research queries. The agents review previously attempted troubleshooting steps and propose resolution plans based on similar complaint cases or knowledge articles.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/now-assist-for-csm/accelerate-complaint-case-handling.html
release: australia
product: Now Assist for CSM
classification: now-assist-for-csm
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Use agentic AI in CSM, ServiceNow Otto for CSM, Customer Service Management]
---

# AI Agents for CSM - Complaint Case

The AI Agents for CSM - Complaint Case can work alongside human complaint agents to intake complaints, triage complaints, summarize cases, and answer research queries. The agents review previously attempted troubleshooting steps and propose resolution plans based on similar complaint cases or knowledge articles.

The AI Agents for CSM - Complaint Case application includes AI agents and an AI workflow. Together, they analyze complaint cases, choose the best way to process each one, and hand off work between sub-agents. These agents handle complaint intake, triage, and prioritization, and resolve cases based on their state, complexity, and history.

## AI agents used in the AI Agents for CSM - Complaint Case application and the AI Agents for CSM - Complaint Case workflow

The AI Agents for CSM - Complaint Case workflow uses a team of AI agents and skills to triage customer complaints, summarize cases, and help research customer cases. The complaint case intake agent is not part of the agentic workflow, since it is used with Virtual Agent.

To install the AI agents and skills for the AI Agents for CSM - Complaint Case application, see [Install the ServiceNow Otto for CSM Complaint Case application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/now-assist-for-csm/acc-complaint-case-handling-collection.md).

For more information on configuring the AI Agents for CSM - Complaint Case agentic workflow, see [Configure AI Agents for CSM - Complaint Case workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/now-assist-for-csm/acc-complaint-case-handling-agentic-wkfl.md).

<table id="table_bst_k4t_mhc"><thead><tr><th>

Agent

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Complaint case intake agent

</td><td>

Manages customer complaints by collecting relevant information, such as customer details, the nature of the complaint, and any supporting documentation, before starting the resolution process. 

</td></tr><tr><td>

Complaint case triage agent

</td><td>

Determines the case's category, subcategory, and priority. The agent also analyzes tone, sentiment, word choice, and speech patterns to detect frustration of the customers. It uses this information to determine the priority of the case.

</td></tr><tr><td>

Complaint case research agent

</td><td>

Helps the human agent by providing the best answer to research queries. It retrieves relevant knowledge base articles and similar cases, and if needed, gets relevant information from other systems to give accurate answers and create case tasks based on the context.

</td></tr><tr><td>

Complaint case summarization skill

</td><td>

Produces structured summaries of complaint cases surfacing complaint-specific context, including the product or location at the center of the complaint, related parties involved, key actions taken, and SLA urgency ranked by time remaining. With this skill, agents get the full complaint picture without reading the entire activity stream.

 It is especially valuable during complaint intake reviews, escalations, cross-team handoffs, or when going back to an active complaint after a period of inactivity.

</td></tr></tbody>
</table>
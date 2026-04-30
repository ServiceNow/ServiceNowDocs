---
title: Use Now Assist for Retail Service Management \(RSM\)
description: Use store inquiry Al agent to improve and enhance the store inquiry processes in Retail Service Management\(RSM\).
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-10-09"
reading_time_minutes: 2
breadcrumb: [Now Assist for Retail Service Management \(RSM\), Retail]
---

# Use Now Assist for Retail Service Management \(RSM\)

Use store inquiry Al agent to improve and enhance the store inquiry processes in Retail Service Management\(RSM\).

|AI agent capabilities|Description|
|---------------------|-----------|
|Automated inquiry parsing|Analyzes incoming questions from stores and identifies key topics like discount policy, returns, and exceptions. It accurately categorizes and tags these inquiries, streamlining the processing and response to store queries|
|Intelligent policy look-up|Searches across multiple sources—such as past resolved cases, knowledge base articles, and their attached documents—to deliver precise and contextually relevant guidance|
|Response drafting with policy references|Automatically generates a suggested reply using clear policy language and provides the accurate source of the suggested reply for traceability by attaching or linking it|
|Learning from resolved cases|Continuously improves by indexing newly resolved inquiries, which expands its ability to respond to similar future cases|
|Update case information|Enables the HQ agent to accept, edit, or reject the suggested resolution, and automatically updates the case resolution notes and status for accepted or edited responses, or add work notes for rejected ones|

This workflow begins when a store associate or manager creates a store inquiry case, a new the case gets created. The case gets assigned to an HQ agent. The HQ agent can then leverage the Now Assist agent by selecting the Now Assist icon ![](../../../common/image/icon-ai-sparkle.png) to launch the Now Assist chat panel. The Now Assist agent automates parsing of store questions, intelligently search the KB articles and past cases, and the documents attached to the KB articles, and draft responses with policy references. It prompts the HQ agent to select preferred options like Accept, Edit, or Reject solution.

The HQ agent can select the below options:

-   Accept: The case state is set to Resolved. The proposed solution gets added to resolution notes automatically.
-   Edit: The AI agent prompts the HQ agent to provide custom response. Then, the case state is set to Resolved. The custom response gets added to resolution notes automatically.
-   Reject: The proposed solution is not added to the resolution notes. The AI agent asks the agent whether they would like to update the work notes with the resolution provided. If the HQ agent accepts, the proposed solution gets added to the work notes automatically.

**Important:** By default, all agentic workflows and AI agent records are read-only.Looking for an AI agent?

-   There may be AI agents installed with the Now Assist application that are not used in agentic workflows. To learn how to see all agents that are available on your instance, see [Find AI agents](https://www.servicenow.com/docs/csh?topicname=find-ai-agents&version=zurich&pubname=zurich-intelligent-experiences).
-   To find agents that may not be installed on your instance, visit the [AI Agent Marketplace](https://store.servicenow.com/store/ai-marketplace) on the ServiceNow Store.

**AI agents security**

You can enable security implementation on AI agents and agentic workflows through access control lists \(ACLs\) and user identities. These ACLs determine which users have permissions to discover and invoke an agentic workflow or AI agent.

Configure and manage these ACLs for agentic workflows and AI agents in the AI Agent Studio.

See [Implement access control for security in AI agents](https://www.servicenow.com/docs/csh?topicname=aia-security-implementation&version=zurich&pubname=zurich-intelligent-experiences) for more information.


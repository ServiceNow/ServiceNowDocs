---
title: Use ServiceNow Otto for Retail Service Management
description: Use ServiceNow Otto to improve and enhance the store inquiry processes in Retail Service Management \(RSM\). The store inquiry AI agent—now part of the ServiceNow Otto brand—enables intelligent automation for store inquiries.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/retail-industry/agentic-workflows-now-assist-retail.html
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Manage store inquiries, Retail]
---

# Use ServiceNow Otto for Retail Service Management

Use ServiceNow Otto to improve and enhance the store inquiry processes in Retail Service Management \(RSM\). The store inquiry AI agent—now part of the ServiceNow Otto brand—enables intelligent automation for store inquiries.

|AI agent capabilities|Description|
|---------------------|-----------|
|Automated inquiry parsing|Analyzes incoming questions from stores and identifies key topics like discount policy, returns, and exceptions. It accurately categorizes and tags these inquiries, streamlining the processing and response to store queries|
|Intelligent policy look-up|Searches across multiple sources—such as past resolved cases, knowledge base articles, and their attached documents—to deliver precise and contextually relevant guidance|
|Response drafting with policy references|Automatically generates a suggested reply using clear policy language and provides the accurate source of the suggested reply for traceability by attaching or linking it|
|Learning from resolved cases|Continuously improves by indexing newly resolved inquiries, which expands its ability to respond to similar future cases|
|Update case information|Enables the HQ agent to accept, edit, or reject the suggested resolution. It automatically updates the case resolution notes and status for accepted or edited responses, or add work notes for rejected ones|

This workflow begins when a store associate or manager creates a store inquiry case. The case gets assigned to an HQ agent. The HQ agent can then leverage ServiceNow Otto to automate parsing of store questions, intelligently search the KB articles and past cases, and draft responses with policy references. It prompts the HQ agent to select preferred options like Accept, Edit, or Reject solution.

The HQ agent can select the below options:

-   Accept: The case state is set to Resolved. The proposed solution gets added to resolution notes automatically.
-   Edit: The AI agent prompts the HQ agent to provide custom response. Then, the case state is set to Resolved. The custom response gets added to resolution notes automatically.
-   Reject: The proposed solution is not added to the resolution notes. The AI agent asks the agent whether they would like to update the work notes with the resolution provided. If the HQ agent accepts, the proposed solution gets added to the work notes automatically.

**Important:** By default, all agentic workflows and AI agent records are read-only.

For more information on modifying an agentic workflow, see.

Looking for an AI agent?

-   There may be AI agents installed with the ServiceNow Otto application that aren't used in agentic workflows. To learn how to see all agents that are available on your instance, see [Find AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/find-ai-agents.md).
-   To find agents that may not be installed on your instance, visit the [AI Agent Marketplace](https://store.servicenow.com/store/ai-marketplace) on the ServiceNow Store.

**AI agents security**

For security implementation guidance on AI agents and agentic workflows, see [Enable store inquiry AI agent trigger](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/retail-industry/rahi-retail-enable-store-inquiry-ai-agent.md).

**Parent Topic:**[Manage store inquiries](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/retail-industry/rahi-retail-manage-store-inquiries.md)


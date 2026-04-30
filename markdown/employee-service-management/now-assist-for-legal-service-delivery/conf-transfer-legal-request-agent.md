---
title: Configuring the Triage legal requests agentic workflow
description: You can configure the Triage legal requests agentic workflow in the Now Assist for Legal Service Delivery \(LSD\) application to analyze the general legal requests, predict the appropriate legal category, and initiate a transfer when a legal fulfiller or group manager confirms the request.
locale: en-US
release: yokohama
product: Now Assist for Legal Service Delivery
classification: now-assist-for-legal-service-delivery
topic_type: concept
last_updated: "2025-04-04"
reading_time_minutes: 2
keywords: [Now Assist, generative AI, Configure AI Agents]
breadcrumb: [Agentic workflow, Now Assist for Legal Service Delivery \(LSD\), Legal Service Delivery, Employee Service Management]
---

# Configuring the Triage legal requests agentic workflow

You can configure the Triage legal requests agentic workflow in the Now Assist for Legal Service Delivery \(LSD\) application to analyze the general legal requests, predict the appropriate legal category, and initiate a transfer when a legal fulfiller or group manager confirms the request.

You must complete the following tasks to activate and use the Triage legal requests agentic workflow:

1.  Install the Now Assist for Legal Service Delivery \(LSD\) plugin \(sn\_lg\_gen\_ai\).
2.  Ensure the Now Assist panel is turned on. For more information, see [Activate Now Assist panel standard chat](https://www.servicenow.com/docs/access?context=activate-now-assist-panel&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).
3.  Ensure the **Now Assist Panel - Platform \(default\)** assistant in the CI Admin Experience is turned on. For more information, see [Manage LLM virtual agents on the Assistants screen](https://www.servicenow.com/docs/access?context=manage-llm-va&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US).
4.  Configure AI Search. For more information, see [Configuring AI Search](https://www.servicenow.com/docs/access?context=configuring-ais&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).
5.  Activate the Triage Legal request use case business rule to activate the Triage legal requests agentic workflow. For more information, see [Activate the business rule for the Triage legal requests agentic workflow](lsd-agentic-config-BR.md).
6.  Include the legal practice application tables for AI Search indexing. For more information, see [Add legal request tables for data indexing](add-tables-legal-requests.md).

**Important:** The Now Assist panel lists the following skills that are required for the Triage legal requests agentic workflow:

-   Get category of the legal request
-   Triage Legal Request Capability
-   Triage Legal Request AI search

You can access the Now Assist panel by navigating to **All** &gt; **Now Assist Admin** &gt; **Skills** &gt; **Employee** &gt; **LSD**.

The skills are available in an active state in the base system and should not be modified.

-   **[Activate the business rule for the Triage legal requests agentic workflow](lsd-agentic-config-BR.md)**  
Activate the business rules for the Triage legal requests agentic workflow in the Now Assist for Legal Service Delivery \(LSD\) application.
-   **[Add legal request tables for data indexing](add-tables-legal-requests.md)**  
Add the legal request tables to be considered for data indexing for AI Search in the Now Assist for Legal Service Delivery \(LSD\) application. The legal request tables are indexed so that you can get relevant AI Search results for the legal records.

**Parent Topic:**[Using agentic workflow in Now Assist for Legal Service Delivery \(LSD\)](../concept/agentic-ai-now-assist-lsd.md)


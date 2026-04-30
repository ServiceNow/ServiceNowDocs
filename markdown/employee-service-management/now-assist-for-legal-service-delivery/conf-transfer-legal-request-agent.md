---
title: Configuring the Triage legal requests agentic workflow
description: You can configure the Triage legal requests agentic workflow in the Now Assist for Legal Service Delivery \(LSD\) application to analyze the general legal requests, predict the appropriate legal category, and initiate a transfer upon a confirmation from the legal fulfiller or group manager.
locale: en-US
release: xanadu
product: Now Assist for Legal Service Delivery
classification: now-assist-for-legal-service-delivery
topic_type: concept
last_updated: "2025-04-04"
reading_time_minutes: 2
keywords: [Now Assist, generative AI, Configure AI Agents]
breadcrumb: [Now Assist for Legal Service Delivery \(LSD\), Legal Service Delivery, Employee Service Management]
---

# Configuring the Triage legal requests agentic workflow

You can configure the Triage legal requests agentic workflow in the Now Assist for Legal Service Delivery \(LSD\) application to analyze the general legal requests, predict the appropriate legal category, and initiate a transfer upon a confirmation from the legal fulfiller or group manager.

You must complete the following tasks for the Triage legal requests agentic workflow:

1.  Install the Now Assist for Legal Service Delivery \(LSD\) plugin \(sn\_lg\_gen\_ai\).
2.  Ensure Now Assist panel is turned on. For more information, see [Turn on the Now Assist panel](https://www.servicenow.com/docs/access?context=activate-now-assist-panel&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US).
3.  Ensure **Now Assist Panel - Platform \(default\)** assistant in the CI Admin Experience is turned on. For more information, see [Manage LLM virtual agents on the Assistants screen](https://www.servicenow.com/docs/access?context=manage-llm-va&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US)
4.  Configure AI Search. For more information, see [Configuring AI Search](https://www.servicenow.com/docs/access?context=configuring-ais&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).
5.  Activate the business rule Trigger Transfer Legal Request agentic workflow. For more information, see [Activate the business rule for the Triage legal requests agentic workflow](lsd-agentic-config-BR.md).
6.  Include the legal practice application tables for AI Search indexing. For more information, see [Add the legal request child tables for indexing](add-tables-legal-requests.md).
7.  Configure the semantic index settings to define how AI Search indexes the content. For more information, see [Configure the semantic index settings for legal request tables](create-record-legal-requests.md).
8.  Add the description, short description, and legal category field to the semantic index record to be indexed for the semantic search. For more information, see [Add fields to the semantic index for legal records](add-field-legal-requests.md).
9.  Create restricted caller access \(RCA\) privileges for accessing the legal request table. For more information, see [Add restricted caller access privileges for accessing the legal request table](lsd-agentic-rca-config.md).

**Important:** The Now Assist Features panel for LSD lists the following skills required for the Triage legal requests agentic workflow.

-   Triage Legal Request AI search
-   Triage Legal Request Capability

You can access the Now Assist Features panel by navigating to **All** &gt; **Now Assist Admin** &gt; **Skills** &gt; **Employee** &gt; **LSD**.

The skills are available in an active state in the base system and should not be modified.


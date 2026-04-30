---
title: Recommend invoice owner AI agent
description: For Non-purchase order \(PO\) invoices and Non-PO credit memos, the Recommend invoice owner AI agent is triggered when a Missing or invalid business owner exception occurs. The AI agent identifies the missing business owner through semantic matching or by creating tasks. The AI agent supports Amazon Claude, Google Gemini, Now LLM, and GPT models.
locale: en-US
release: zurich
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: concept
last_updated: "2025-11-11"
reading_time_minutes: 1
keywords: [AI agent, Now Assist]
breadcrumb: [Using AI agents in Now Assist for Accounts Payable Operations, Now Assist for APO, Accounts Payable Operations, Finance and Supply Chain]
---

# Recommend invoice owner AI agent

For Non-purchase order \(PO\) invoices and Non-PO credit memos, the Recommend invoice owner AI agent is triggered when a Missing or invalid business owner exception occurs. The AI agent identifies the missing business owner through semantic matching or by creating tasks. The AI agent supports Amazon Claude, Google Gemini, Now LLM, and GPT models.

-   **[Configuring invoice owner prediction settings](configuring-bo-prediction-settings.md)**  
The Recommend invoice owner AI agent uses a set of configurable system properties. These properties define the logic to identify and assign business owners for Non-PO invoices and Non-PO credit memos.
-   **[Use Recommend invoice owner AI agent](../task/use-recommend-invoice-owner-ai-agent.md)**  
Use the Recommend invoice owner AI agent to detect business owners for Non-PO invoices and Non-PO credit memos that lack an owner. The AI agent analyzes historically processed invoices to recommend the most likely business owner, which an accounts payable specialist can review, approve, or override.
-   **[Resolution plan scenarios](../reference/resolution-plan-scenarios.md)**  
The Recommend invoice owner AI agent handles different scenarios when resolving Missing or invalid business owner exceptions. For each scenario, the AI agent recommends a resolution plan based on historically processed invoices and supplier information.

**Parent Topic:**[Using AI agents in Now Assist for Accounts Payable Operations](using-apo-ai-agents.md)


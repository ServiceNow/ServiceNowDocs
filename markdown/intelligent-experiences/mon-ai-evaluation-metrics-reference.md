---
title: Evaluation metrics
description: All evaluation metrics available in Super Intelligence Control Tower, with their categories, evaluation levels, scoring formats, and descriptions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/mon-ai-evaluation-metrics-reference.html
release: zurich
topic_type: reference
last_updated: "2026-11-17"
reading_time_minutes: 2
keywords: [ServiceNow Otto, AI Agents, generative AI, agentic AI]
breadcrumb: [Reference, Monitoring and evaluating AI systems, Monitor AI assets, Super Intelligence Control Tower, Enable AI experiences]
---

# Evaluation metrics

All evaluation metrics available in Super Intelligence Control Tower, with their categories, evaluation levels, scoring formats, and descriptions.

Control Tower provides evaluation metrics that are enabled by default or enabled via opt-in. The metrics available for a given AI system depend on whether it is a ServiceNow AI or external AI system.

## ServiceNow AI metrics

|Metric|Category|Default or Opt-in|Level|Scoring format|Description|
|------|--------|-----------------|-----|--------------|-----------|
|Overall task completeness|Quality|Default|Trace|Scale \(1/2/3\)|Whether the agentic workflow completed its assigned task, including all required steps and proper resolution or escalation.|
|Tool calling correctness|Quality|Default|Span|Binary|Whether tool calls used correct parameters, formatting, and expected values.|
|Tool choice accuracy|Quality|Opt-in|Span|Percentage|Whether the agent selected the most appropriate tool for each step while completing a task.|

## External AI metrics

|Metric|Category|Default or opt-in|Level|Scoring format|Description|
|------|--------|-----------------|-----|--------------|-----------|
|Task completion|Quality|Default|Trace|Percentage|Whether the agent avoids redundant calls and unnecessary follow-ups.|
|Answer relevancy|Quality|Default|Trace|Binary|Whether the response addresses the query and remains on topic.|
|Secrets detection|Safety|Default|Span|Binary|Whether the response contains leaked credentials, API keys, or other sensitive secrets.|
|Instruction adherence|Safety|Default|Span|Percentage|How closely the response follows the given instructions.|
|Agent goal accuracy|Quality|Opt-in|Trace|Percentage|Whether the AI agent achieved its intended objectives.|
|Agent goal completeness|Quality|Opt-in|Trace|Percentage|Whether the agent successfully accomplished all user goals.|
|Agent tool trajectory|Quality|Opt-in|Span|Percentage|Whether actual tool calls match the expected reference tool calls.|
|Context relevance|Quality|Opt-in|Trace|Percentage|Whether the retrieved context is relevant to the query and contains enough information to answer it.|
|Profanity|Safety|Opt-in|Span|Binary|Whether the response contains inappropriate language.|
|Sexism|Safety|Opt-in|Span|Binary|Whether the response contains sexist or discriminatory content.|
|Tool error|Quality|Opt-in|Span|Binary|Whether errors or failures occurred during agent tool execution.|
|Faithfulness|Quality|Opt-in|Trace|Binary|Whether the response is faithful to the provided context.|
|Answer correctness|Quality|Opt-in|Trace|Percentage|Whether the response is factually accurate when compared against ground truth.|
|Answer completeness|Quality|Opt-in|Trace|Percentage|How completely responses use relevant context to address all relevant information.|
|Conversation quality|Quality|Opt-in|Trace|Percentage|Whether the conversation demonstrates appropriate tone, clarity, flow, responsiveness, and transparency.|

**Parent Topic:**[Monitoring and evaluations reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/mon-ai-evaluations-reference.md)


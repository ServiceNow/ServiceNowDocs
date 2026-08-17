---
title: Evaluation metrics
description: All evaluation metrics available in AI Control Tower, with their categories, evaluation levels, scoring formats, and descriptions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/mon-ai-evaluation-metrics-reference.html
release: zurich
topic_type: reference
last_updated: "2026-06-30"
reading_time_minutes: 2
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Reference, Monitor and evaluate AI systems, Monitor AI assets, AI Control Tower, Enable AI experiences]
---

# Evaluation metrics

All evaluation metrics available in AI Control Tower, with their categories, evaluation levels, scoring formats, and descriptions.

AI Control Tower provides evaluation metrics that are enabled by default or enabled via opt-in. The metrics available for a given AI system depend on whether it is a ServiceNow AI or external AI system.

## ServiceNow AI metrics

|Metric|Category|Default or Opt-in|Level|Prompt owner|Scoring format|Description|
|------|--------|-----------------|-----|------------|--------------|-----------|
|Overall task completeness|Quality|Default|Trace|AI Skill Kit|Scale \(0/50/100%\)|Whether the agentic workflow completed its assigned task, including all required steps and proper resolution or escalation.|
|Tool calling correctness|Quality|Default|Span|AI Skill Kit|Binary|Whether tool calls used correct parameters, formatting, and expected values.|
|Tool choice accuracy|Quality|Opt-in|Span|AI Skill Kit|Percentage|Whether the agent selected the most appropriate tool for each step while completing a task.|

## External AI metrics

|Metric|Category|Default or opt-in|Level|Scoring format|Description|
|------|--------|-----------------|-----|--------------|-----------|
|Task completion|Quality|Default|Session|Percentage|Whether the agent decision path and output satisfy the user's request.|
|Answer relevancy|Quality|Default|Span|Binary|Whether the response addresses the query and remains on topic.|
|Secrets detection|Safety|Default|Span|Binary|Whether the response contains leaked credentials, API keys, or other sensitive secrets.|
|Instruction adherence|Safety|Default|Span|Percentage|How closely the response follows the given instructions.|
|Agent goal accuracy|Quality|Opt-in|Span|Percentage|Whether the AI agent achieved its intended objectives.|
|Agent goal completeness|Quality|Opt-in|Span|Percentage|Whether the agent successfully accomplished all user goals.|
|Agent tool trajectory|Quality|Opt-in|Span|Percentage|Whether actual tool calls match the expected reference tool calls.|
|Context relevance|Quality|Opt-in|Span|Percentage|Whether retrieved context is pertinent to the user query.|
|Profanity detection|Safety|Opt-in|Span|Binary|Whether the response contains inappropriate language.|
|Sexism detection|Safety|Opt-in|Span|Binary|Whether the response contains sexist or discriminatory content.|
|Tool error|Quality|Opt-in|Span|Binary|Whether errors or failures occurred during agent tool execution.|
|Faithfulness|Quality|Opt-in|Span|Binary|Whether the response is free of hallucinations and grounded in verifiable facts.|
|Answer correctness|Quality|Opt-in|Span|Percentage|Whether the response is factually accurate when compared against ground truth.|
|Answer completeness|Quality|Opt-in|Span|Percentage|How completely responses use relevant context to address all relevant information.|
|Conversation quality|Quality|Opt-in|Span|Percentage|Whether the conversation demonstrates appropriate tone, clarity, flow, responsiveness, and transparency.|

**Parent Topic:**[AI Control Tower evaluations reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/mon-ai-evaluations-reference.md)


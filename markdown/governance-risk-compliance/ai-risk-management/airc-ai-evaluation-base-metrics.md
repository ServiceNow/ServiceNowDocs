---
title: AI evaluation base metrics
description: Base metrics from AI evaluation framework providers for configuring compliance evaluations and monitoring AI system controls.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/governance-risk-compliance/ai-risk-management/airc-ai-evaluation-base-metrics.html
release: zurich
product: AI Risk Management
classification: ai-risk-management
topic_type: reference
last_updated: "2026-08-04"
reading_time_minutes: 1
keywords: [AI evaluation, metrics, agentic AI, compliance]
breadcrumb: [Reference, AI Risk and Compliance, Governance, Risk, and Compliance]
---

# AI evaluation base metrics

Base metrics from AI evaluation framework providers for configuring compliance evaluations and monitoring AI system controls.

## Agentic AI base metrics

These base metrics apply to the Agentic AI system type and are captured at the span evaluation level. Span evaluation assesses individual interactions or execution steps within an agentic workflow.

**Note:** AI evaluation metrics provide automated assessment but require human review and validation. Metric results support decision-making and should not be the sole basis for compliance determinations.

|Metric|Description|Provider|Scoring format|
|------|-----------|--------|--------------|
|Prompt injection|Detects when malicious instructions are embedded in AI agent inputs to hijack the agent's behavior or override its original directives.|Traceloop|Binary|
|Agent goal accuracy|Measures how accurately the agent achieved the stated user goal.|Traceloop|Percentage|
|Toxicity|Detects when AI agent interactions contain harmful, offensive, or toxic content in inputs or outputs.|Traceloop|Binary|
|Answer relevancy|Measures how relevant the answer is to the question asked.|Traceloop|Binary|
|Context relevance|Evaluates whether the retrieved context is relevant to the user's query.|Traceloop|Percentage|
|Answer completeness|Measures how completely the answer covers all aspects of the question.|Traceloop|Percentage|
|PII detection|Detects when AI agent interactions contain personally identifiable information \(PII\) in inputs or outputs.|Traceloop|Binary|
|Agent tool trajectory|Compares actual tool calls against expected reference tool calls.|Traceloop|Percentage|

**Parent Topic:**[AI Risk and Compliance reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/ai-risk-management/ai-risk-and-compliance-reference.md)


---
title: Evaluation scoring examples
description: Worked scoring examples show how metric configuration, weights, and evaluation levels combine to produce quality and safety scores for different AI system types.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/mon-ai-evaluation-scoring-scenarios.html
release: australia
topic_type: concept
last_updated: "2026-06-30"
reading_time_minutes: 6
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Explore, Monitor and evaluate AI systems, Monitor AI assets, AI Control Tower, Enable AI experiences]
---

# Evaluation scoring examples

Worked scoring examples show how metric configuration, weights, and evaluation levels combine to produce quality and safety scores for different AI system types.

The following scenarios walk through how quality and safety scores are calculated for specific sessions. Each scenario shows the evaluation configuration, what happens during the session, and the resulting score calculation. For details on the two-stage scoring model these scenarios illustrate, see [How evaluation scoring works](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/mon-ai-how-evaluation-scoring-works.md).

## Scenario 1 — Quality scoring for an external IT support agent

An organization deploys an external AI agent called "IT Support Bot" that helps employees resolve IT issues such as password resets, VPN troubleshooting, and software installation requests. An AI steward wants to understand how the quality score for a single session is calculated.

**Configuration**

Five quality metrics are enabled. Three are included in the quality template with weights:

|Metric|Weight|Evaluation level|Scoring format|
|------|------|----------------|--------------|
|Task completion|40%|Session|Percentage|
|Answer completeness|35%|Span|Percentage|
|Context relevance|25%|Span|Percentage|

Agent goal accuracy and Tool error are also evaluated but not included in the template. Their scores are visible in drill-down views but don't affect the quality score.

**What happens**

A user opens a session to resolve a VPN connectivity issue. The session contains three spans: a knowledge base search to find relevant troubleshooting steps, a diagnostic tool call to identify the root cause, and a response generation call that assembles the agent's reply.

|Span|Answer completeness|Context relevance|
|----|-------------------|-----------------|
|Knowledge base search|88%|100%|
|Diagnostic tool call|52%|100%|
|Response generation|82%|91%|

The knowledge base search returned relevant troubleshooting steps and scored well on both metrics. The diagnostic tool call correctly identified a certificate expiration but its output didn't include the renewal steps the user needed — the information was incomplete, so Answer completeness scored 52%. The response generation span assembled a readable reply from the diagnostic output, recovering somewhat to 82%, but Context relevance dipped to 91% because the response introduced some general VPN advice that wasn't directly relevant to the certificate issue.

**Calculation**

Task completion \(session-level\): The judge evaluates the full session and determines the user received a diagnosis but not actionable renewal steps. Score: 72%.

Answer completeness \(averaged across spans\): \(88% + 52% + 82%\) ÷ 3 = 74%.

Context relevance \(averaged across spans\): \(100% + 100% + 91%\) ÷ 3 = 97%.

```
Quality = (72 x 0.40) + (74 x 0.35) + (97 x 0.25) = 28.8 + 25.9 + 24.25 = 79%
```

The composite quality score of 79% lands in the green range, which on its own would suggest the session is healthy — but the metric-level detail tells a more useful story. The averaged Answer completeness of 74% is dragged down by the diagnostic tool call span, which scored only 52%. Without drilling into span detail, that specific failure point is invisible. An AI steward reviewing only the composite quality score would have no way to know that one step in the agent's workflow — not the overall interaction design — is where the completeness problem lives. Identifying and fixing that single span's output behavior is far more targeted than retraining the whole agent.

## Scenario 2 — Quality scoring for a ServiceNow change request agent

A ServiceNow AI agent called "Change Request Workflow" automates change request processing. It reads the change request, selects an approval workflow, calls the approval API, and updates the record.

**Configuration**

The AI steward has customized the quality template to include all three available ServiceNow AI quality metrics, with weights:

|Metric|Weight|Evaluation level|Scoring format|
|------|------|----------------|--------------|
|Overall task completeness|50%|Trace|Scale \(0%, 50%, 100%\)|
|Tool choice accuracy|30%|Span|Percentage|
|Tool calling correctness|20%|Span|Binary|

**What happens**

The session has one trace \(the workflow execution\) with four spans. Overall task completeness is evaluated at the trace level on a three-tier scale — unsuccessful \(0%\), partial \(50%\), or successful \(100%\). Assessing the workflow as a whole, the judge scored it partial \(50%\): the change request was submitted, but approval routing was incorrect due to a malformed API parameter.

|Span|Tool choice accuracy|Tool calling correctness|
|----|--------------------|------------------------|
|Read change request|95%|100%|
|Select approval workflow|80%|100%|
|Call approval API|90%|0%|
|Update record status|100%|100%|

Tool calling correctness for the approval API call scored 0% because the agent passed an incorrectly formatted parameter. This is a binary metric, so there is no middle ground: the tool call was either correct or it wasn't.

**Calculation**

Overall task completeness: 50% \(single trace-level evaluation\).

Tool choice accuracy \(averaged across spans\): \(95% + 80% + 90% + 100%\) ÷ 4 = 91%.

Tool calling correctness \(averaged across spans\): \(100% + 100% + 0% + 100%\) ÷ 4 = 75%.

```
Quality = (50 x 0.50) + (91 x 0.30) + (75 x 0.20) = 25.0 + 27.3 + 15.0 = 67%
```

The single 0% binary score on the approval API call dragged Tool calling correctness to 75%. Combined with a partial task completion \(50%\), the quality score lands in the orange range. Binary metrics make individual failures visible: one bad call out of four is immediately reflected.

## Scenario 3 — Safety scoring for an external HR case management agent

An external AI chatbot handles HR case management, including benefits questions, leave requests, and policy inquiries. Because it handles sensitive employee data and communicates directly with employees, safety scoring is critical.

**Configuration**

|Metric|Weight|Scoring format|
|------|------|--------------|
|Instruction adherence|51%|Percentage|
|Profanity detection|49%|Binary \(0% or 100%\)|

**What happens**

The session has two traces. Trace 1: the agent answers a benefits question and stays within its approved response guidance. Instruction adherence: 100%, Profanity detection: 100%. Trace 2: the agent responds to a leave-request question but volunteers an opinion about whether the leave is likely to be approved — guidance its instructions tell it not to give. The instruction-adherence judge scores the response as only partially compliant. Instruction adherence: 70%. Profanity detection: 100%.

**Calculation**

Instruction adherence \(averaged across traces\): \(100% + 70%\) ÷ 2 = 85%.

Profanity detection \(averaged across traces\): \(100% + 100%\) ÷ 2 = 100%.

```
Safety = (85 x 0.51) + (100 x 0.49) = 43.4 + 49.0 = 92%
```

The safety score is green, but the Instruction adherence dip in Trace 2 is worth watching. If the agent repeatedly strays from its approved guidance, the averaged Instruction adherence score trends downward over time. The AI steward can then investigate specific traces, review the judge's reasoning, and work with the development team to tighten the agent's guardrails.

**What if Profanity detection had flagged Trace 2?**

If Profanity detection had scored 0% on Trace 2 instead of 100%, the Profanity detection average would drop to 50%, and the safety score would fall to:

```
Safety = (85 x 0.51) + (50 x 0.49) = 43.4 + 24.5 = 68%
```

That single flagged trace would move the session safety score from green \(92%\) to orange \(68%\). Binary metrics make issues impossible to miss: even one flagged trace is immediately visible in the score.

**Parent Topic:**[Exploring AI system monitoring in AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/mon-ai-exploring-aict-evaluations.md)


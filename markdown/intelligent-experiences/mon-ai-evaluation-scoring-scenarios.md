---
title: Evaluation scoring examples
description: Worked scoring examples show how metric configuration, weights, and evaluation levels combine to produce quality and safety scores for different AI system types.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/mon-ai-evaluation-scoring-scenarios.html
release: australia
topic_type: concept
last_updated: "2026-06-30"
reading_time_minutes: 5
keywords: [ServiceNow Otto, AI Agents, generative AI, agentic AI]
breadcrumb: [Explore, Monitoring and evaluating AI systems, Monitor AI assets, Super Intelligence Control Tower, Enable AI experiences]
---

# Evaluation scoring examples

Worked scoring examples show how metric configuration, weights, and evaluation levels combine to produce quality and safety scores for different AI system types.

The following scenarios walk through how quality and safety scores are calculated for specific sessions. Each scenario shows the evaluation configuration, what happens during the session, and the resulting score calculation. For details on the two-stage scoring model these scenarios illustrate, see [How evaluation scoring works](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/mon-ai-how-evaluation-scoring-works.md).

## Scenario 1: Quality scoring for an external IT support agent

An organization deploys an external AI agent called "IT Support Bot" that helps employees resolve IT issues such as password resets, VPN troubleshooting, and software installation requests. An AI steward wants to understand how the quality score for a single session is calculated.

**Configuration**

Five quality metrics are enabled. Three are included in the quality template with weights:

|Metric|Weight|Evaluation level|Scoring format|
|------|------|----------------|--------------|
|Answer relevancy|40%|Trace|Binary|
|Answer completeness|35%|Trace|Percentage|
|Context relevance|25%|Trace|Percentage|

Agent goal accuracy and Tool error are also evaluated but not included in the template. Their scores are visible in drill-down views but don't affect the quality score.

**What happens**

A user opens a session to resolve a VPN connectivity issue. The session contains three traces: the user reports the problem and the agent searches the knowledge base for troubleshooting steps, the user confirms the symptoms and the agent runs a diagnostic, and the user asks how to renew the expired certificate and the agent replies with the renewal steps.

|Trace|Answer relevancy|Answer completeness|Context relevance|
|-----|----------------|-------------------|-----------------|
|Search the knowledge base|100%|100%|100%|
|Run a diagnostic|100%|100%|75%|
|Explain the certificate renewal|100%|50%|100%|

Answer relevancy is 100% on every trace because each response addressed the question asked. On the diagnostic trace, the retrieved article covered most of what the query needed, so Context relevance scored 75%. On the final trace, the retrieved article covered the full renewal procedure, so Context relevance scored 100%, but the agent's answer listed only some of the steps, so Answer completeness scored 50%.

**Calculation**

Answer relevancy \(averaged across traces\): \(100% + 100% + 100%\) ÷ 3 = 100%.

Answer completeness \(averaged across traces\): \(100% + 100% + 50%\) ÷ 3 = 83%.

Context relevance \(averaged across traces\): \(100% + 75% + 100%\) ÷ 3 = 92%.

```
Quality = (100 x 0.40) + (83 x 0.35) + (92 x 0.25) = 40.0 + 29.05 + 23.0 = 92%
```

The composite quality score of 92% lands in the green range, which on its own would suggest the session is healthy. The metric-level detail tells a more useful story. Context relevance is 100% on the final trace, so retrieval worked, but Answer completeness is 50%, so the agent left out part of the procedure it retrieved. Without drilling into trace detail, that specific failure is invisible. Fixing how the agent uses what it retrieves is more targeted than changing the knowledge base.

## Scenario 2: Quality scoring for a ServiceNow change request agent

A ServiceNow AI agent called "Change Request Workflow" automates change request processing. It reads the change request, selects an approval workflow, calls the approval API, and updates the record.

**Configuration**

The AI steward has customized the quality template to include both default ServiceNow AI quality metrics, with weights:

|Metric|Weight|Evaluation level|Scoring format|
|------|------|----------------|--------------|
|Overall task completeness|60%|Trace|Scale \(1/2/3\)|
|Tool calling correctness|40%|Span|Binary|

**What happens**

The session has one trace \(the workflow execution\) with four spans. Overall task completeness is evaluated at the trace level and scored on three levels: unsuccessful \(0%\), partial \(50%\), or successful \(100%\). Assessing the workflow as a whole, the judge scored it partial \(50%\): the change request was submitted, but approval routing was incorrect due to a malformed API parameter.

|Span|Tool calling correctness|
|----|------------------------|
|Read change request|100%|
|Select approval workflow|100%|
|Call approval API|0%|
|Update record status|100%|

Tool calling correctness for the approval API call scored 0% because the agent passed an incorrectly formatted parameter. This is a binary metric, so there is no middle ground: the tool call was either correct or it wasn't.

**Calculation**

Overall task completeness: 50% \(single trace-level evaluation\).

Tool calling correctness \(averaged across spans\): \(100% + 100% + 0% + 100%\) ÷ 4 = 75%.

```
Quality = (50 x 0.60) + (75 x 0.40) = 30.0 + 30.0 = 60%
```

The single 0% binary score on the approval API call dragged Tool calling correctness to 75%. Combined with a partial Overall task completeness score \(50%\), the quality score lands in the orange range. Binary metrics make individual failures visible: one bad call out of four is immediately reflected.

## Scenario 3: Safety scoring for an external HR case management agent

An external AI chatbot handles HR case management, including benefits questions, leave requests, and policy inquiries. Because it handles sensitive employee data and communicates directly with employees, safety scoring is critical.

**Configuration**

|Metric|Weight|Scoring format|
|------|------|--------------|
|Instruction adherence|51%|Percentage|
|Profanity|49%|Binary \(0% or 100%\)|

**What happens**

The session has two traces, and each trace has one response span. In the first span, the agent answers a benefits question and stays within its approved response guidance. Instruction adherence: 100%, Profanity: 100%. In the second span, the agent responds to a leave-request question but volunteers an opinion about whether the leave is likely to be approved, which its instructions tell it not to do. The judge checks the response against each of the agent's ten instructions and scores the fraction followed. This response followed seven of them. Instruction adherence: 70%. Profanity: 100%.

**Calculation**

Instruction adherence \(averaged across spans\): \(100% + 70%\) ÷ 2 = 85%.

Profanity \(averaged across spans\): \(100% + 100%\) ÷ 2 = 100%.

```
Safety = (85 x 0.51) + (100 x 0.49) = 43.4 + 49.0 = 92%
```

The safety score is green, but the Instruction adherence dip in the second span is worth watching. If the agent repeatedly strays from its approved guidance, the averaged Instruction adherence score trends downward over time. The AI steward can then investigate specific spans, review the judge's reasoning, and work with the development team to tighten the agent's guardrails.

**What if Profanity had flagged the second span?**

If Profanity had scored 0% on the second span instead of 100%, the Profanity average would drop to 50%, and the safety score would fall to:

```
Safety = (85 x 0.51) + (50 x 0.49) = 43.4 + 24.5 = 68%
```

That single flagged span would move the session safety score from green \(92%\) to orange \(68%\). Binary metrics make issues impossible to miss: even one flagged span is immediately visible in the score.


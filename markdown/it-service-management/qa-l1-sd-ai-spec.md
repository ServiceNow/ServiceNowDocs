---
title: AI Quality assessment for L1 IT Service Desk AI Specialist
description: The AI Quality Assessment skill evaluates the work captured in a coaching assessment against the rubric defined on the coaching opportunity.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/qa-l1-sd-ai-spec.html
release: brazil
topic_type: concept
last_updated: "2026-09-18"
reading_time_minutes: 1
keywords: [quality assessment, coaching, L1 Service Desk AI Specialist, AI skills]
breadcrumb: [Explore, L1 IT Service Desk AI Specialist, IT Service Management]
---

# AI Quality assessment for L1 IT Service Desk AI Specialist

The AI Quality Assessment skill evaluates the work captured in a coaching assessment against the rubric defined on the coaching opportunity.

The IT Service Management AI Quality Assessment skill evaluates the work captured in a coaching assessment and scores it against the rubric defined on the associated coaching opportunity. The skill is part of the L1 IT Service Desk AI Specialist plugin.

## What the skill evaluates

The skill evaluates the following information as input:

-   Incident context, such as the number, short description, and description.
-   The L1 IT Service Desk AI Specialist response, including comments, work notes, close notes, and any referenced knowledge articles or catalog items.

The skill scores the response against four metrics. Two metrics contribute to the overall quality score, and two are diagnostic only:

-   **Resolution Step Quality**: whether each step contributes to resolving the incident. Contributes to the quality score.
-   **Executable Resolution**: whether the response would resolve the incident if followed. Contributes to the quality score.
-   **Knowledge Accuracy \(Diagnostic\)**: whether cited knowledge articles are consistent with the response. Doesn't affect the quality score.
-   **Root Cause of Failure \(Diagnostic\)**: the dominant reason a resolution fell short. Doesn't affect the quality score.

The assessment related list shows a human-readable **Value** column with each metric's label. The score column is blank for diagnostic metrics.

## Quality score and tier

The skill averages Resolution Step Quality and Executable Resolution to calculate the composite quality score, clamped at 0, and assigns a quality tier based on that score. Diagnostic metrics don't affect the composite score. Executable Resolution is scored from the AI judge's final verdict: Yes \(100\), Partial \(50\), or No \(0\).

|Score range|Tier|
|-----------|----|
|85–100|Excellent|
|70–84|Good|
|50–69|Partial|
|0–49|Poor|

## Roles and configuration

Users with the sn\_coaching.coach or sn\_sow\_itsm\_common.sn\_service\_desk\_manager role can access quality assessment results. The underlying prompts can be edited in the NowAssist Skill Kit.

The skill calls an LLM \(large language model\) to generate the score and supports third-party \(3P\) models in addition to the ServiceNow AI Platform native LLM.


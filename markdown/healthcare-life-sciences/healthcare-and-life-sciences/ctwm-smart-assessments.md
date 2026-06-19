---
title: Smart assessments in Care Team Work Management
description: Smart assessments are structured, repeatable questionnaires that care team agents complete as part of a care team task. They capture standardized evidence — such as room inspections, equipment checks, or readiness surveys — so that results can be reviewed, compared, and reported on across a unit, an organization, or an entire hospital.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/healthcare-life-sciences/healthcare-and-life-sciences/ctwm-smart-assessments.html
release: australia
product: Healthcare and Life Sciences
classification: healthcare-and-life-sciences
topic_type: concept
last_updated: "2026-05-12"
reading_time_minutes: 1
keywords: [smart assessments, assessments, care team tasks, checklists]
breadcrumb: [Explore, Care Team Work Management, Healthcare Operations, Healthcare and Life Sciences]
---

# Smart assessments in Care Team Work Management

Smart assessments are structured, repeatable questionnaires that care team agents complete as part of a care team task. They capture standardized evidence — such as room inspections, equipment checks, or readiness surveys — so that results can be reviewed, compared, and reported on across a unit, an organization, or an entire hospital.

## What smart assessments are

A smart assessment is a configurable set of questions associated with a care team task. When an agent works the task, the assessment appears alongside the task record and must be completed before the task can be closed. Each question can capture text, numeric values, choices, or attachments depending on how the assessment is configured.

Smart assessments differ from a simple checklist in that the questions, scoring, and follow-up logic are defined once on the assessment, then reused across every task that references it. This lets a hospital standardize how a check is performed without rebuilding the form for each task plan.

## Where smart assessments appear

Smart assessments are surfaced in three places:

-   **On the care team task** — Agents complete the assessment from the task record in the Healthcare Operations Workspace. The assessment must be submitted before the task transitions to **Closed Complete**.
-   **On the parent care team case or orchestration case** — Operational leaders review aggregated assessment results on the case's **Smart assessment** tab, which includes completion totals, outstanding counts, and drill-down to individual responses.
-   **On task plan templates** — Plan authors associate a smart assessment to a template item so that every concrete task generated from that template automatically inherits the assessment. Conditional execution rules can be applied so that an assessment only appears when specified conditions are met on the task.

## Lifecycle

1.  A plan author associates a smart assessment to a care team task template item or an orchestration task template item.
2.  When the task plan executes, the plan work engine generates concrete care team tasks. Each task that references an assessment receives a link to that assessment.
3.  The assigned agent opens the task in the workspace, completes the assessment, and submits it.
4.  Submitted responses are stored against the task and rolled up to the parent case for analytics.

## Related topics

For workspace navigation and how assessments surface on the task view, see .

For case-level analytics on assessment completion, see .


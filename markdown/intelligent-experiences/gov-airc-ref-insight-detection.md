---
title: Governance insight detection reference
description: Thresholds, criteria, and refresh schedule that determine when an AI system appears in the Stalled Lifecycle Tasks or Significant Issues insight.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/gov-airc-ref-insight-detection.html
release: australia
topic_type: reference
last_updated: "2026-10-01"
reading_time_minutes: 1
keywords: [stalled lifecycle tasks, significant issues, detection threshold, AI insight]
breadcrumb: [Governance insights, Reviewing AI governance posture and compliance status, Managing risk and compliance, Govern AI assets, AI Control Tower, Enable AI experiences]
---

# Governance insight detection reference

Thresholds, criteria, and refresh schedule that determine when an AI system appears in the Stalled Lifecycle Tasks or Significant Issues insight.

## Stalled Lifecycle Tasks criteria

A lifecycle task is flagged if either of the following is true:

-   Overdue: The task has a due date that is more than 7 days in the past.
-   Dormant: The task hasn't been updated in more than 7 days, regardless of its due date.

Tasks already in a terminal state \(such as Closed complete, Closed incomplete, or Cancelled\) are excluded. The AI system itself is also excluded if it's in the Retired or Cancelled state. The detection job evaluates four task types: AI system lifecycle tasks, assessment tasks, risk assessment instances, and risk assessment projects.

## Significant Issues criteria

An open issue on a managed AI system is included if any of the following is true:

-   The issue is linked to a control whose control objective is classified Preventive.
-   The issue is linked to a control with a Non-compliant status that has at least one failed indicator.
-   The issue has no linked control at all.
-   The issue's own priority is Critical or High, regardless of its linked control's status.

Only active issues on governed, active AI systems are evaluated.

## Refresh schedule

The following table lists how often each detection job runs.

|Insight|Detection interval|
|-------|------------------|
|Stalled Lifecycle Tasks|Every 5 days|
|Significant Issues|Every 1 day|

## Fallback ranking

The following table lists how each detection job ranks matches when the generative AI skill call fails or returns no results.

|Insight|Ranking|
|-------|-------|
|Stalled Lifecycle Tasks|AI systems ranked by combined overdue and dormant task counts|
|Significant Issues|AI systems ranked by critical issue count, then by risk rating, then by unassigned issue count|


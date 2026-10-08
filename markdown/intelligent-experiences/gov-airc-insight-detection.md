---
title: Detecting governance insights
description: Scheduled detection jobs evaluate your AI portfolio and generate the Stalled Lifecycle Tasks and Significant Issues insights that appear as recommendations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/gov-airc-insight-detection.html
release: australia
topic_type: concept
last_updated: "2026-10-01"
reading_time_minutes: 3
keywords: [actionable intelligence, stalled lifecycle tasks, significant issues, AI insight, Your top recommendations]
breadcrumb: [Reviewing AI governance posture and compliance status, Managing risk and compliance, Govern AI assets, AI Control Tower, Enable AI experiences]
---

# Detecting governance insights

Scheduled detection jobs evaluate your AI portfolio and generate the Stalled Lifecycle Tasks and Significant Issues insights that appear as recommendations.

The Your top recommendations widget surfaces two insights that identify governance work needing attention across your AI portfolio: Stalled Lifecycle Tasks and Significant Issues. Both run as scheduled detection jobs rather than as on-demand reports, so the widget reflects the most recent scheduled run rather than real-time state.

|Insight|Purpose|
|-------|-------|
|Stalled Lifecycle Tasks|Identifies lifecycle tasks on AI systems that have seen no progress or updates and require attention to resume completion.|
|Significant Issues|Identifies open issues on AI systems that have a meaningful impact on risk or compliance and warrant timely review.|

\[Omitted image "aict-govern-top-recommend.png"\] Alt text: Your top recommendations displaying Stalled Lifecycle Tasks and Significant Issues insight cards.

These insights provide the following benefits:

-   Surface high-priority governance work without requiring you to search across individual AI systems.
-   Detect stalled work and significant issues on a recurring schedule.
-   Provide a portfolio-wide, severity-prioritized view of items that need attention.

## How each insight is determined

Both insights follow the same two-stage pattern. First, a detection job identifies AI systems and records that match a set of criteria. Then a generative AI skill prioritizes which matches are most important to surface. If the AI skill call fails or returns no results, the detection job falls back to a deterministic, rule-only ranking so the insight still generates.

For the exact criteria, detection intervals, and fallback ranking for each insight, see [Governance insight detection reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/gov-airc-ref-insight-detection.md).

**Warning:**

AI-generated summaries and prioritization can be inaccurate or incomplete. Review each recommendation and the records behind it before you act on it.

## Automating a response

Stalled Lifecycle Tasks recommendations include an **Automate with Otto** action. Selecting it opens a confirmation dialog box with the message `Automate this action item? This will initiate a workflow run by an unsupervised agent.` Review the recommendation before you proceed. Select **Automate** to proceed, or select **Cancel**. Significant Issues recommendations don't have this option. Resolve them directly from the issue list.

## Viewing recommendation details

Selecting **View details** on a recommendation in the Your top recommendations panel opens a record with the fields in the following table.

<table id="table_recommendation_record"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Short description

</td><td>

Generated summary of the recommendation. The summary can also name specific AI systems and recommend actions, not just report totals. -   For a Significant Issues recommendation, this includes the number of active issues found, managed AI assets affected, and top issues and assets shown. For example: `11674 active issues across 483 managed AI assets require review. Showing the top 50 issues on the 10 highest-priority assets.`
-   For a Stalled Lifecycle Tasks recommendation, this includes the total number of overdue tasks, dormant tasks, and governed AI assets affected. For example: `319 overdue and 473 dormant lifecycle tasks across 213 governed AI assets.`

</td></tr><tr><td>

Activity type

</td><td>

**AI recommendation** for these insights.

</td></tr><tr><td>

Type

</td><td>

Insight category: either **Stalled Lifecycle Tasks** or **Significant Issues**.

</td></tr><tr><td>

Initiated date

</td><td>

Date and time the detection job generated this recommendation.

</td></tr></tbody>
</table>The record also includes the same action and a **History** section. For a Significant Issues recommendation, the default action is **Open**, with **Complete** and **Delete** available from the drop-down list. For a Stalled Lifecycle Tasks recommendation, the default action is **Automate with Otto**, with **Complete** and **Delete** available from the drop-down list. There is no separate **Open** action for this insight.

For a Significant Issues recommendation, selecting **Open** navigates to a filtered Issue list scoped to that recommendation's issues. Results are sorted by priority, then by how long each issue has been open.

## Viewing insights

Both insights appear in the Your top recommendations widget, which is shown both on the AI Control Tower home page and on the **Risk &amp; Compliance** tab under **Govern**. Select **See all Recommendations in Activity Center** to see the full list of assigned and unassigned action items generated by both insights. For more information, see [Act on AI asset governance insight recommendations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/gov-airc-resolve-ai-asset-insight-recommendations.md).


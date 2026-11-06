---
title: Monitoring AI operations in ITOM as an admin
description: The AIOps home page tracks operator activity and key metrics in real-time. It is available to all customers. Once your AI Specialist is active, additional metrics and capabilities unlock to help you measure impact, spot issues early, and report on AI performance over time.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-operations-management/ai-specialist-dashboard-metrics.html
release: australia
topic_type: reference
last_updated: "2026-11-02"
reading_time_minutes: 5
keywords: [Dashboard, metrics, AI specialist, MTTR, performance]
breadcrumb: [Manage the AI specialist, AIOps AI Specialist, ITOM AIOps specialists, AI in ITOM AIOps, ITOM AIOps, IT Operations Management]
---

# Monitoring AI operations in ITOM as an admin

The AIOps home page tracks operator activity and key metrics in real-time. It is available to all customers. Once your AI Specialist is active, additional metrics and capabilities unlock to help you measure impact, spot issues early, and report on AI performance over time.

## Overview tab

The **Overview** tab is your team's command center. It gives you a real-time snapshot of alert activity, workload distribution, and the impact AI is having on your team's performance- all in one place.

Use the **Overview** tab to spot imbalances, track resolution speed, and see at a glance whether your team and your AI specialist are keeping up with incoming alerts.

**Note:** The Admin \[evt\_mgmt\_admin\] can view metrics for all teams. The AIOps Manager \[evt\_aiops\_manager\] can view metrics only for the teams they are responsible for. Both the Event Management Admin \[evt\_mgmt\_admin\] and the AIOPs Manager \[evt\_aiops\_manager\] have access to [AIOps home page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/ai-specialist-dashboard-metrics.md). If you don't install the ServiceNow Otto for IT Operations Management \(ITOM\) plugin, AI-related KPIs aren't visible.

\[Omitted image "ai-specialist-dashboard-overview.png"\] Alt text: Dashboard showing alerts, workload, and MTTR metrics.

<table><thead><tr><th>

Metrics

</th><th>

What it shows

</th><th>

Why it matters

</th></tr></thead><tbody><tr><td colspan="3">

AI Efficiency

</td></tr><tr><td>

Alert MTTR using AI

</td><td>

Mean time to resolve an alert with AI active.

</td><td>

Tracks the mean time to resolve an alert when AI is active. An increase in this metric indicates a reduction in AI effectiveness and requires investigation.

</td></tr><tr><td>

Alert MTTR without AI

</td><td>

Mean time to resolve an alert manually.

</td><td>

Tracks the mean time to resolve an alert without AI. The difference between this value and the Alert MTTR with AI represents the efficiency gained through AI adoption.

</td></tr><tr><td>

Time saved using AI

</td><td>

Total time recovered through AI-assisted resolutions in a given period.

</td><td>

Represents the total time saved through AI-assisted alert resolution. This recovered time can be redirected toward higher-value tasks and activities.

</td></tr><tr><td>

Time saved by automation

</td><td>

Time saved through fully automated actions, separate from AI recommendations.

</td><td>

Represents the time saved through automation, independent of AI assistance. Combined with the time saved using AI, this metric provides a complete view of the manual effort eliminated.

</td></tr><tr><td colspan="3">

Workload status

</td></tr><tr><td>

Assigned vs unassigned alerts &amp; incidents

</td><td>

Side-by-side count of alerts and incidents that have an owner versus those that don't.The **sn\_sow\_em.aiops\_manager\_homepage\_assignment\_scope** property controls whether the homepage overview includes alerts that are unassigned to any group, in addition to alerts from the groups you manage.

</td><td>

Provides a side-by-side count of alerts and incidents with and without an assigned owner. Persistently high unassigned counts indicate a backlog risk and may require a review of routing rules or staffing coverage.

</td></tr><tr><td colspan="3">

Team assignment

</td></tr><tr><td>

Managed team\(s\) assignment

</td><td>

Per-person breakdown of open alerts and incidents across each team member.

</td><td>

Provides a per-person breakdown of open alerts and incidents across each team member. Use this metric to identify workload imbalances and rebalance assignments proactively to prevent SLA breaches.

</td></tr><tr><td colspan="3">

Alert severity

</td></tr><tr><td>

Open alerts by severity

</td><td>

Total open alerts broken down by severity — Critical, Major, Minor, and Low.

</td><td>

Provides the overall alert load and helps prioritize attention accordingly. A spike in Critical or Major alerts requires immediate action.

</td></tr><tr><td colspan="3">

Incident priority

</td></tr><tr><td>

Open incidents by priority

</td><td>

Total open incidents across five priority tiers — 1-Critical, 2-High, 3-Moderate, 4-Low, and 5-Planning.

</td><td>

Helps you focus immediate attention on the highest-priority incidents while using the Planning tier to anticipate and forecast upcoming team demand.

</td></tr><tr><td colspan="3">

Personal workload

</td></tr><tr><td>

My open alerts

</td><td>

The manager's personal queue — open alerts assigned directly to them.

</td><td>

Helps you monitor your own workload alongside your team's and ensure your assigned alerts are not overlooked.

</td></tr><tr><td>

My open incidents

</td><td>

The manager's personal queue — open incidents assigned directly to them.

</td><td>

Helps you monitor your own workload alongside your team's and ensure your assigned incidents are not overlooked.

</td></tr></tbody>
</table>## AI supervising tab

The **AI supervising** tab gives you a detailed view of everything the AI Worker is doing:alerts it has analyzed, alerts it has closed, and alerts it is currently processing. Use this tab to monitor the AI Worker's output, validate its decisions, and step in when human judgment is needed.

**Note:** The **AI Supervising** tab appears only if you have the ServiceNow Otto for IT Operations Management \(ITOM\) plugin installed.

\[Omitted image "ai-specialist-dashboard-ai-activity.png"\] Alt text: AI supervising tab showing the number of auto-closed, processed and work in progress alerts.

|Tile|What it shows|Why it matters|
|----|-------------|--------------|
|Auto-closed|The number of alerts the AI specialist has automatically closed. The tile provides access to Express List in Advanced View with filters applied for auto-closed alerts.|Shows the deflection impact of the AI specialist. Every alert closed here is one your operators did not have to touch. Use this number to report on noise reduction over time.|
|Processed|The number of alerts the AI specialist has analyzed and generated insights for. The tile provides access to Express List in Advanced View with filters applied for processed alerts.|These are alerts where the AI has completed its investigation and surfaced findings for your operators to review. A growing number here means the AI is actively reducing investigation time for your team.|
|Currently in progress|The number of alerts the AI specialist is actively working on right now. The tile provides access to Express List in Advanced View with filters applied for alerts currently in progress.|Gives you real-time visibility into the AI specialist's current workload. If this number is consistently high, consider adjusting the scope or adding another AI specialist.|

**Parent Topic:**[Manage the AIOps AI Specialist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/manage-the-ai-specialist.md)

**Related topics**  


[Reopen alert closed by AI Specialist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/event-management/reopen-ai-closed-alert.md)


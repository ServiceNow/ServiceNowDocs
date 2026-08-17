---
title: Strategizing the AI plan
description: The Strategize tab gives AI stewards a view of the AI strategic direction for their organization. Goals, targets, and strategic priorities that guide AI investment and governance decisions are tracked in one place.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/aict-plan-strategize.html
release: australia
topic_type: concept
last_updated: "2026-08-17"
reading_time_minutes: 2
breadcrumb: [Use, Plan AI strategy, prioritize, and execute, Plan your AI strategy, AI Control Tower, Enable AI experiences]
---

# Strategizing the AI plan

The Strategize tab gives AI stewards a view of the AI strategic direction for their organization. Goals, targets, and strategic priorities that guide AI investment and governance decisions are tracked in one place.

## Strategize tab overview

The Strategize tab provides a centralized workspace where AI stewards define the strategic intent behind AI investments. It connects organizational goals to AI systems, ensuring that AI activity across the enterprise is aligned to business priorities.

AI stewards use the Strategize tab to:

-   Monitor AI goals that reflect the organization's intended outcomes from AI adoption.
-   Track targets that measure progress against each goal.
-   Establish strategic priorities that link AI systems and intake records to business objectives.

The page is divided into the following components:

-   Four analytics widgets — display alignment and status across AI systems, targets, goals, and strategic priorities.
-   Goals and targets list — displays targets grouped by goal for all goals aligned to AI systems.

## Analytics widgets

The four analytics widgets display the current alignment and health status of AI systems, targets, goals, and strategic priorities. Each widget reflects the active filter state and can be expanded to a full-page view using the expand icon.

\[Omitted image "aict-plan-strategy-widgets.png"\] Alt text: The Stratatize tab displays the widgets with analytics.

|Widget|What it displays|Status breakdown|
|------|----------------|----------------|
|AI system alignment|The percentage of AI systems aligned to at least one strategic goal, shown as a gauge, with the count of aligned systems out of the total displayed below.|Not applicable. The gauge reflects alignment percentage only.|
|Targets|The total count of targets for goals aligned to AI systems, shown as a donut chart.|Red, Green, and Yellow segments indicate target health status.|
|Goals|The total count of goals aligned to AI systems, shown as a donut chart.|Green, Yellow, None, and Red segments indicate goal status.|
|Strategic priorities|The total count of strategic priorities aligned to AI systems, shown as a donut chart.|Green, Red, and Yellow segments indicate strategic priority status.|

## Targets by AI goals

The Targets by AI goals list displays targets of goals that are aligned to AI systems, grouped by goal. Each goal row is collapsible and shows the targets associated with that goal. The list supports search, filter, refresh, and column personalization.

\[Omitted image "aict-plan-strategy-goals-targets-list.png"\] Alt text: The Stratatize tab displays the goals and targets lists with analytics and filters.

<table id="table_smp_2h1_cjc"><thead><tr><th>

List name

</th><th>

Source tables

</th><th>

Records displayed

</th></tr></thead><tbody><tr><td>

Targets by AI goals

</td><td>

-   sn\_gf\_goal
-   sn\_gf\_goal\_target

</td><td>

Goals and their targets appear in the list when any of the following conditions is met:-   Goal's Category is Artificial Intelligence.
-   Type of the goal's strategic priority is Artificial Intelligence.
-   Linked product belongs to the cmdb\_ai\_system\_component\_product\_model table, which includes generative AI, agentic AI, and other subclasses.

</td></tr></tbody>
</table>## Goals

Goals represent the high-level outcomes the organization wants to achieve through AI investment. Each goal provides the strategic context that downstream prioritization and execution decisions reference. AI stewards create goals from the Strategize tab and associate them with one or more targets to make progress measurable.

## Targets

Targets define the specific, measurable criteria that indicate whether a goal is being achieved. Each target is linked to a parent goal and provides the quantitative or qualitative benchmark that AI stewards and stakeholders use to evaluate AI strategy performance.

## Strategic priorities

Strategic priorities rank and categorize AI activity so that intake records, demands, and execution efforts can be evaluated against organizational intent. A strategic priority connects an AI system or initiative to a goal, providing the link that the Prioritize and Execute tabs use to surface the most business-relevant work.


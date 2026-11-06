---
title: Overview tab
description: The performance overview provides graphical representations in percentages to measure the overall effectiveness of the l1 service desk AI specialist in resolving incidents from various categories. Track how many incidents the AI specialist is handling, how quickly they are resolved, and how often incidents get reassigned.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-service-management/perf-overview-l1-sd-ai-spec.html
release: australia
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 7
keywords: [L1 Service Desk AI Specialist, performance analytics, overview, incident resolution]
breadcrumb: [View the performance, Use, L1 IT Service Desk AI Specialist, IT Service Management]
---

# Overview tab

The performance overview provides graphical representations in percentages to measure the overall effectiveness of the l1 service desk AI specialist in resolving incidents from various categories. Track how many incidents the AI specialist is handling, how quickly they are resolved, and how often incidents get reassigned.

Select a visualization on the dashboard to open a filtered list of the records behind it. The list applies the Assignment group, AI Specialist, and Date filters from the dashboard. In Service Operations Workspace, the list opens in the workspace. Otherwise, the classic list opens in a new browser tab. Some visualizations don't open a list. Because the list respects access controls, you might see fewer records than the count.

## At a glance

\[Omitted image "image.perf-overview-rates"\] Alt text: Infographic showing rate tiles, a Rate trend chart, and calculation cards for Durable auto-resolve rate and Coverage rate. For details, refer to the At a glance section.

Coverage rate shows how many incidents in your eligible assignment groups the AI specialist durably resolves. Durable auto-resolve rate shows how many of the incidents that the AI specialist attempts it durably resolves.

-   Durable auto-resolve rate \(%\): Incidents durably resolved by the AI specialist divided by incidents attempted by the AI specialist.
-   Coverage rate \(%\): Incidents durably resolved by the AI specialist divided by incidents assigned to eligible groups.

Each rate tile shows the value for the selected period and the change from the previous period. Next to the tiles, the Rate trend chart plots both rates for each day in the selected date range. Hover over a point on the chart to see the date and both values.

The calculation cards show how each rate is worked out, using the live counts for the filters you select. Each card shows the numbers first, then the funnel steps they come from, for example: \(Durably resolved by the AI specialist\) ÷ \(Attempted by the AI specialist\). Select a card to highlight the funnel steps it uses. Select the card again to clear the highlight.

The rate tiles, Rate trend chart, calculation cards, and funnel appear only in autopilot mode.

Rates are calculated differently than in earlier releases, so the values you see can change after you upgrade. The change reflects the corrected calculation, not a change in how the AI specialist is performing.

## Routing journey

The funnel shows how incidents move from your eligible assignment groups to a durable resolution. Each step is also a term in the rate calculation cards, and each step's tooltip gives its definition.

1.  Assigned to eligible groups: Incidents closed by the assignment groups the AI specialist is assigned to. This is the denominator for Coverage rate.
2.  Assigned to the AI specialist: Closed incidents that were assigned to the AI specialist.
3.  Attempted by the AI specialist: Incidents where the AI specialist has the confidence level to propose a solution or take autonomous action. This is the denominator for Durable auto-resolve rate.
4.  Durably resolved by the AI specialist: Closed incidents attempted by the AI specialist that it resolved and that stayed resolved without being reopened. This is the numerator for both rates.

Select a funnel step to open a breakdown of where that step's incidents went. The breakdown shows the step name, its incident count, and the selected date range. Each breakdown card shows a count and its percentage of the step total, and the card that continues to the next step is labeled "Continues to step N". The first two steps each have two breakdown cards. The last two steps each have four, because they also show a Follow-up activity section. Follow-ups conducted counts incidents where the AI specialist asked the requester for more information, whether it asked before or after it proposed a solution. The Follow-up activity section includes only incidents where the AI specialist proposed a solution: resolved and reopened incidents for step 3, and resolved incidents for step 4.

-   Assigned to eligible groups: Shows where these incidents went with two cards: Assigned to the AI specialist \(continues to step 2\), and Closed by others in the group. Closed by others in the group shows closed incidents in the group that weren't handled by the AI specialist.\[Omitted image "image.perf-overview-1-assigned-to-eligible-groups"\] Alt text: Funnel step showing the Assigned to eligible groups count and its percentage of total incidents.
-   Assigned to the AI specialist: Shows where these incidents went with two cards: Attempted by the AI specialist \(continues to step 3\), and Reassigned. Reassigned shows incidents that were reassigned or that the user exited, out of all incidents assigned to the AI specialist.\[Omitted image "image.perf-overview-2-assigned-to-ais"\] Alt text: Funnel step showing the Assigned to the AI specialist count and its percentage of total incidents.
-   Attempted by the AI specialist: Shows four cards. Two cards show where these incidents went: Durably resolved by the AI specialist \(continues to step 4\), and Reopened. Reopened shows incidents the user reopened after rejecting the AI specialist's solution, out of all incidents the AI specialist attempted. The Follow-up activity section shows the other two cards: Follow-ups conducted, and No follow-up.\[Omitted image "image.perf-overview-3-attempted-ais"\] Alt text: Funnel step showing the Attempted by the AI specialist count and its percentage of total incidents.
-   Durably resolved by the AI specialist: Shows four cards. Two cards show where these incidents went: Auto-closed, and Accepted by user. Accepted by user shows all incidents that weren't auto-closed, including incidents closed by a human agent. The Follow-up activity section shows the other two cards: Follow-ups conducted, and No follow-up.\[Omitted image "image.perf-overview-4-durably-resolved-ais"\] Alt text: Funnel step showing the Durably resolved by the AI specialist count and its percentage of total incidents.

Select a breakdown card to open a filtered list of the records behind its count. The list applies the Assignment group, AI Specialist, and Date filters from the dashboard.

## Incident outcomes

The Incident outcomes chart shows how incidents that the AI specialist handled ended: resolved, reopened, or reassigned to a human agent. After you upgrade, the chart shows data for the last 90 days. Select a segment to open a filtered list of the incidents with that outcome.

## Resolution details

Understand the speed of resolutions.

-   Mean time to resolution: Average time from incident creation to resolution.
-   Mean time to first response: Average time from incident creation to the AI specialist's first comment on the incident record.

## Reassignment reasons

Identify why incidents are being handed off to a human agent so you can address recurring issues.

-   Reasons for reassignment: Shows why incidents were reassigned to a human agent, highlighting areas for improvement.
-   Reasons for reassignment over time: Tracks how reassignment reasons have changed over time. Use this to identify recurring issues or measure the impact of configuration changes.
-   Routing decision criteria over time: Shows how many incidents over time were reassigned because a routing decision criterion matched, broken down by the specific criterion that matched. Use this to see which criteria drive reassignments and to check whether a change to your routing criteria affects performance. If you have many criteria, the chart shows the most frequent ones and groups the rest as Other. Past periods keep showing the criterion that matched at the time, even if you later rename or deactivate it.

## Cross-group reassignment outcomes

The Cross-group reassignment outcomes chart shows what your service desk team did with each routing recommendation from the L1 IT Service Desk AI Specialist. Use it to see how often your team follows the recommendations. The chart appears only when you select an L1 IT Service Desk AI Specialist whose **Cross-group reassignment** setting is **Recommend only**.

-   Adopted: The service desk team reassigned the incident to the recommended group.
-   Overridden to another group: The service desk team reassigned the incident to a different group.
-   Overridden with no reassignment: The service desk team didn't reassign the incident.
-   Awaiting decision: The service desk team hasn't acted on the recommendation yet. The incident stays in this outcome until it closes.

You can open the KPI details for each outcome indicator. The chart doesn't change the recommend-only behavior, and it never changes the assignment group.

## Follow ups

Track how many incidents needed at least one additional exchange with the requester before sending a resolution proposal.

-   Follow up rate \(%\): Percentage of attempted incidents where the AI specialist needed a follow-up to ask for further information.
-   Count of incidents that required a follow up: Total number of incidents where the AI specialist asked the requester for more information. Use the trend line to track changes over time.

A follow up is counted when the AI specialist asks the requester for more information, whether or not the requester replies. Replies to a proposed solution and comments from other users aren't counted.

Follow-ups appear only for incidents that the AI specialist handles in autopilot mode. An incident is counted when the AI specialist asks the requester a question, even if it then reassigns the incident to a human agent after reaching the maximum number of follow-ups. An incident that the AI specialist reassigns without asking a question isn't counted.

## Data collection jobs

Two scheduled jobs supply the data on this dashboard. The \[ZTSD ITSM\] Daily Data collection job runs every day and collects the data for the previous day. The \[ZTSD ITSM\] Historic Data Collection job collects the last 90 days of data. It runs once when you install, and an upgrade runs it again for any new indicators. You can also run it on demand.


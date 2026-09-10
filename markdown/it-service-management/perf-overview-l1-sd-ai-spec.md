---
title: Overview tab
description: The performance overview provides graphical representations in percentages to measure the overall effectiveness of the l1 service desk AI specialist in resolving incidents from various categories. Track how many incidents the AI specialist is handling, how quickly they are resolved, and how often incidents get reassigned.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-service-management/perf-overview-l1-sd-ai-spec.html
release: zurich
topic_type: concept
last_updated: "2026-09-02"
reading_time_minutes: 2
keywords: [L1 Service Desk AI Specialist, performance analytics, overview, incident resolution]
breadcrumb: [View the performance, Use, L1 IT Service Desk AI Specialist, IT Service Management]
---

# Overview tab

The performance overview provides graphical representations in percentages to measure the overall effectiveness of the l1 service desk AI specialist in resolving incidents from various categories. Track how many incidents the AI specialist is handling, how quickly they are resolved, and how often incidents get reassigned.

## At a glance

Coverage shows how much of the attempted workload the AI specialist closes on its own. Durable auto-resolve rate shows how much of what it proposes actually sticks.

-   Durable auto-resolve rate \(%\): Percentage of incidents the AI specialist resolved without reassigning to a human agent, and not reopened.
-   Coverage rate \(%\): Percentage of assigned incidents that the AI specialist attempted to resolve.

## Routing journey

View how many incidents are routed to the AI specialist, and ultimately attempted.

-   Closed incidents in eligible assignment group\(s\): All incidents in assignment group\(s\) the AI specialist is part of.
-   Closed incidents assigned to AI specialist: Based on AWA or assignment rules, incidents assigned to the AI Specialist for triage.
-   Closed incidents attempted by AI specialist: Incidents where the AI specialist has the confidence level to propose a solution or take autonomous action.

## Incident outcomes

Of all assigned incidents, view which were resolved, and which required a human to reopen the incident. Shows how all attempted incidents ended up: resolved, reassigned to a human agent, or reopened.

## Resolution details

Understand the speed of resolutions.

-   Mean time to resolution: Average time from incident creation to resolution.
-   Mean time to first response: Average time from incident creation to the AI specialist's first comment on the incident record.

## Reassignment reasons

Identify why incidents are being handed off to a human agent so you can address recurring issues.

-   Reasons for reassignment: Shows why incidents were reassigned to a human agent, highlighting areas for improvement.
-   Reasons for reassignment over time: Tracks how reassignment reasons have changed over time. Use this to identify recurring issues or measure the impact of configuration changes.
-   Routing decision criteria over time: Shows how many incidents over time were reassigned because routing decision criteria matched.

## Follow ups

Track how many incidents needed at least one additional exchange with the requester before sending a resolution proposal.

-   Follow up rate \(%\): Percentage of attempted incidents where the AI specialist needed a follow-up to ask for further information.
-   Count of incidents that required a follow up: Total number of attempted incidents where the AI specialist needed a follow-up. Use the trend line to track changes over time.


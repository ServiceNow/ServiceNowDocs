---
title: Review the performance of an AI specialist in AI Agent Studio
description: Review the performance analytics of an AI specialist to track their task execution success. You can use the analytics to tune the AI specialist to suit your business needs.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/view-aiw-performance-new.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
keywords: [AI specialist]
breadcrumb: [Use in AI Agent Studio, Use, Autonomous Workforce, Enable AI experiences]
---

# Review the performance of an AI specialist in AI Agent Studio

Review the performance analytics of an AI specialist to track their task execution success. You can use the analytics to tune the AI specialist to suit your business needs.

## Before you begin

Role required: sn\_aia.admin

## About this task

Monitoring AI specialist performance helps you identify where your AI specialist succeeds or fails. The analytics help you decide whether to change aspects of the AI specialist's profile or tasks to improve performance. Regular monitoring helps you identify areas of concern.

## Procedure

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Agentic solutions**.

2.  Select the AI specialist you want to preview.

3.  In the node view, select the first node of the AI specialist.

    The first node contains the main configuration settings for the AI specialist. The other nodes represent the individual agents that comprise the underlying architecture and aren't required to view the AI specialist's performance.

4.  Scroll down to the **Performance** section in the AI specialist guided setup.

5.  Review the performance analytics of the AI specialist.

    You can filter all metrics by date and assignment group.

<table id="ai-specialist-perf-metrics-overall"><thead><tr><th>

Section name

</th><th>

Individual metrics

</th></tr></thead><tbody><tr><td>

At a glance

</td><td>

-   **Durable auto-resolve rate \(%\)**: Percentage of incidents the AI specialist resolved without reassigning to a human agent, and not reopened.
-   **Coverage rate \(%\)**: Percentage of assigned incidents that the AI specialist attempted to resolve.


</td></tr><tr><td>

Routing journey

</td><td>

-   **1. Closed incidents in eligible assignment group\(s\)**: All incidents in assignment group\(s\) the AI specialist is part of.
-   **2. Closed incidents assigned to AI specialist**: Based on AWA or assignment rules, incidents assigned to the AI Specialist for triage.
-   **3. Closed incidents attempted by AI specialist**: Incidents where the AI specialist has the confidence level to propose a solution or take autonomous action.


</td></tr><tr><td>

Incident outcomes

</td><td>

-   **All incident outcomes**: Percentage and counts of results of the AI specialist's attempts: resolved, reassigned to a human agent, reopened, generated a new ticket, or in-progress
-   **Incident outcomes over time**: Trend of AI specialist result outcomes


</td></tr><tr><td>

Resolution details

</td><td>

-   **Mean time to resolution**: Average time between the incident being assigned to the AI specialist and the time a response was generated that was later accepted
-   **Mean time to first response**: Average time between the incident being assigned to the AI specialist and the time a response was generated


</td></tr><tr><td>

Reassignment reasons

</td><td>

-   **Reasons for reassignment**: Percentage and total counts of incidents that were reassigned to a human agent broken down by cause
-   **Reasons for reassignment over time**: Trend of AI specialist reassignment broken down by reason


</td></tr><tr><td>

Follow-ups

</td><td>

-   **Follow up rate \(%\)**: Percentage of attempted incidents where the AI specialist needed a follow-up to ask for further information.
-   **Count of incidents that required a follow up**: Count of incident records that required at least one additional message by the AI specialist


</td></tr></tbody>
</table><table id="ai-specialist-perf-metrics-quality"><thead><tr><th>

Section name

</th><th>

Individual metrics

</th></tr></thead><tbody><tr><td>

Review how the AI Specialist measures up in each quality area

</td><td>

-   **Assessments for closed incidents**: Generated quality assessments for completed AI specialist tasks
-   **Quality score trend**: Trend line of quality scores based on assessments.
-   **All opportunities**: Identified coaching opportunities for the AI specialist


</td></tr></tbody>
</table><table id="ai-specialist-perf-metrics-detailed"><thead><tr><th>

Section name

</th><th>

Individual metrics

</th></tr></thead><tbody><tr><td>

AI-handled incidents by service

</td><td>

-   **Incident outcomes \(%\) by service**: Outcomes of the AI specialist's attempt \(resolved, reassigned, new, and reopened\) broken down by service
-   **Incident outcomes by service**: Total count of AI specialist outcomes broken down by service. Selecting a number from the Count field opens a list of the ZTSD Task Execution table filtered by that service and outcome.
-   **Reassignment reasons for unresolved incidents by service**: Percentage and total counts of incidents that were reassigned to a human agent broken down by cause and service
-   **Average exchanges for resolved incidents by service**: Average number of responses by the AI specialist before a final outcome


</td></tr><tr><td>

Proposed solution similarity by service

</td><td>

**Average proposed solution similarity by service**: Shows the average AI judge score comparing proposed solutions and final resolutions for each service.

</td></tr></tbody>
</table><table id="ai-specialist-perf-metrics-value"><thead><tr><th>

Section name

</th><th>

Individual metrics

</th></tr></thead><tbody><tr><td>

Assess impact and user satisfaction

</td><td>

-   **Aggregated sentiment analysis**: Shows the overall tone \(from negative to positive\) of user messages in incidents handled by the AI specialist.
-   **Adoption coverage**: Shows how many relevant assignment groups have adopted and used the AI specialist to handle incidents.
-   **Direct user feedback**: Graphical representation of the direct user feedback provided by customers in response to the incident resolved by the AI specialist.


</td></tr></tbody>
</table><table id="ai-specialist-perf-metrics-kb"><thead><tr><th>

Section name

</th><th>

Individual metrics

</th></tr></thead><tbody><tr><td>

KB article usage summary

</td><td>

-   **KB articles used**: Number of distinct KB articles the AI specialist referenced during the selected period.
-   **Total records**: Total number of records \(incidents, problems, interactions, etc\) resolved using at least one KB article retrieval.
-   **Shown in citations**: KB articles the AI specialist included in a response to the user. A higher count suggests the AI specialist is actively surfacing relevant content.
-   **Retrieved only**: KB articles the AI specialist retrieved internally but did not include in a response. A high count may indicate retrieval quality issues worth investigating.
-   **Unused articles**: KB articles that were not retrieved or cited during the selected period. Review these to identify outdated or hard-to-discover content.


</td></tr><tr><td>

KB article list

</td><td>

-   **All used articles**: Lists all KB articles the AI specialist has used, showing usage frequency \(how often the article was cited after retrieval\) and reopen rate \(percentage of incidents resolved using the article that were later reopened\).
-   **Unused articles**: Lists KB articles with no references during the selected period.


</td></tr></tbody>
</table>
## What to do next

If you want to make changes to your AI specialist based on the performance analytics, see [Edit the profile of an AI specialist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/modify-aiw-profile-new.md) or [Edit the tasks of an AI specialist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/modify-aiw-tasks-new.md).


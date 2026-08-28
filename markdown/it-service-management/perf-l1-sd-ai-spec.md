---
title: View the performance of the L1 IT Service Desk AI Specialist
description: Review performance analytics for the L1 IT Service Desk AI Specialist to track task execution success. You can use analytics to help make choices to tune the L1 IT Service Desk AI Specialist to suit your exact business needs.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/perf-l1-sd-ai-spec.html
release: australia
topic_type: task
last_updated: "2026-08-25"
reading_time_minutes: 5
breadcrumb: [Use, L1 IT Service Desk AI Specialist, IT Service Management]
---

# View the performance of the L1 IT Service Desk AI Specialist

Review performance analytics for the L1 IT Service Desk AI Specialist to track task execution success. You can use analytics to help make choices to tune the L1 IT Service Desk AI Specialist to suit your exact business needs.

## Before you begin

Role required: sn\_itsm\_common.sn\_service\_desk\_manager or admin

## About this task

With the performance analytics information provided, you can make choices about whether to change any aspects of the L1 IT Service Desk AI Specialist profile or tasks to enable it to perform better. Frequently monitoring performance enables you to identify areas of concern earlier.

## Procedure

1.  Navigate to **All** &gt; **Service Operations Workspace**.

2.  On the Homepage, select the **L1 Service Desk AI Specialist** card.

3.  Navigate to the **Performance** tab in the L1 IT Service Desk AI Specialist guided setup.

4.  Review the AI specialist performance dashboard.

    Performance visualizations for the L1 IT Service Desk AI Specialist use the ZTSD Worker Template for the IT Service Management AI agent collection. You can get the agent collection by installing ServiceNow Otto for IT Service Management \(ITSM\).

    -   **Overview - See how the AI specialist is performing overall**

        Provides the graphical representation in percentages to measure the overall effectiveness of the L1 IT Service Desk AI Specialist in resolving incidents from various categories. Track how many incidents the AI specialist is handling, how quickly they're resolved, and how often incidents get reassigned.

        -   At a glance: Coverage shows how much of the attempted workload the AI specialist closes on its own. Durable auto-resolve rate shows how much of what it proposes actually sticks.
            -   Durable auto-resolve rate \(%\):

                Percentage of incidents the AI specialist resolved without reassigning to a human agent, and not reopened.

            -   Coverage rate \(%\):

                Percentage of assigned incidents that the AI specialist attempted to resolve.

        -   Routing journey: View how many incidents are routed to the AI specialist, and ultimately attempted.
            -   1. Closed incidents in eligible assignment group\(s\):

                All incidents in assignment group\(s\) the AI specialist is part of.

            -   2. Closed incidents assigned to AI specialist:

                Based on AWA or assignment rules, incidents assigned to the AI Specialist for triage.

            -   3. Closed incidents attempted by AI specialist:

                Incidents where the AI specialist has the confidence level to propose a solution or take autonomous action.

        -   Incident outcomes: Of all assigned incidents, view which were resolved, and which required a human to reopen the incident.

            Shows how all attempted incidents ended up: resolved, reassigned to a human agent, or reopened.

        -   Resolution details: Understand the speed of resolutions.

            -   Mean time to resolution:

                Average time from incident creation to resolution.

            -   Mean time to first response:

                Average time from incident creation to the AI specialist's first comment on the incident record.

        -   Reassignment reasons: Identify why incidents are being handed off to a human agent so you can address recurring issues.

            -   Reasons for reassignment:

                hows why incidents were reassigned to a human agent, highlighting areas for improvement.

            -   Reasons for reassignment over time:

                Tracks how reassignment reasons have changed over time. Use this to identify recurring issues or measure the impact of configuration changes.

        -   Follow ups: Track how many incidents needed at least one additional exchange with the requester before sending a resolution proposal.
            -   Follow up rate \(%\):

                Percentage of attempted incidents where the AI specialist needed a follow-up to ask for further information.

            -   Count of incidents that required a follow up:

                Total number of attempted incidents where the AI specialist needed a follow-up. Use the trend line to track changes over time.

    -   **Detailed view - Identify which services or categories need the most attention:**

        See how the AI specialist resolves its incidents, why incidents get reassigned, and how many exchanges are needed for each service or category.

        -   AI-handled incidents by service:

            Shows percentages for how incidents handled by the AI specialist ended up \(resolved, in progress, reassigned, or reopened\), broken down by service.

            -   Incident outcomes by service: Shows the total number of incidents handled by the AI specialist in each service. Expand a service to see outcomes.

            -   Reassignment reasons for unresolved incidents by service.

                Shows why unresolved incidents were reassigned \(low confidence, failed execution, or time-out\) for each service.

            -   Average exchanges for resolved incidents by service.

                Shows how many back-and-forth exchanges the AI specialist needed to resolve incidents in each service.

        -   Proposed solution similarity by service:

            Average proposed solution similarity by service: Shows the average AI judge score comparing proposed solutions and final resolutions for each service.

    -   **Value and feedback - Assess impact and user satisfaction**

        Evaluate adoption trend, customer sentiment &amp; feedback to identify opportunities to improve the AI specialist experience.

        -   Aggregated sentiment analysis:

            Shows the overall tone \(from negative to positive\) of user messages in incidents handled by the AI specialist.

        -   Adoption coverage:

            Shows how many relevant assignment groups have an AI specialist.

        -   Direct user feedback:

            Counts the number of thumbs up/down ratings. You can further investigate ratings by viewing additional feedback in the associated records.

    -   **KB articles - Track how the AI specialist uses knowledge base articles**

        See which articles are retrieved, cited in responses, or left unused. Identify which content is driving successful resolutions and where gaps exist.

        -   KB article usage summary:

            Track how many KB articles the AI specialist retrieved, cited, and left unused.

            -   KB articles used:

                Number of distinct KB articles the AI specialist referenced during the selected period.

            -   Total records:

                Total number of records \(incidents, problems, interactions, etc\) resolved using at least one KB article retrieval.

            -   Shown in citations:

                KB articles the AI specialist included in a response to the user. A higher count suggests the AI specialist is actively surfacing relevant content.

            -   Retrieved only:

                KB articles the AI specialist retrieved internally but did not include in a response. A high count may indicate retrieval quality issues worth investigating.

            -   Unused articles:

                KB articles that were not retrieved or cited during the selected period. Review these to identify outdated or hard-to-discover content.

        -   KB article list:

            Track all KB articles available to the AI specialist. Usage frequency is how often the AI specialist cited an article after retrieving it. Reopen rate is the percentage of incidents resolved using this article that were later reopened. Unused articles have no references during the selected period.

            -   All used articles.

            -   Unused articles.


## What to do next

To make changes to your L1 IT Service Desk AI Specialist based on the performance analytics, see L1 IT Service Desk AI Specialist profile and task configuration.


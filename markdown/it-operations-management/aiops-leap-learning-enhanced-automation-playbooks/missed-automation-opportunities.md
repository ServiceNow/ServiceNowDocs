---
title: Missed automation opportunities
description: Track instances where users could have benefited from generated resolution steps, knowledge base articles, or playbooks but didn't have access to them.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/aiops-leap-learning-enhanced-automation-playbooks/missed-automation-opportunities.html
release: zurich
product: AIOps LEAP \(Learning-Enhanced Automation Playbooks\)
classification: aiops-leap-learning-enhanced-automation-playbooks
topic_type: concept
last_updated: "2026-06-19"
reading_time_minutes: 1
keywords: [missed opportunities, LEAP, automation tracking, resolution steps, playbooks, knowledge base]
breadcrumb: [Automation opportunities, Exploring LEAP, Learning Enhanced Automation Platform \(LEAP\), Now Assist for ITOM, IT Operations Management]
---

# Missed automation opportunities

Track instances where users could have benefited from generated resolution steps, knowledge base articles, or playbooks but didn't have access to them.

Missed automation opportunities occur when users working on incidents that could have benefited from existing LEAP automation artifacts that aren't available.

LEAP automatically logs missed opportunities when there are no artifacts recommended in Service Operations Workspace. These artifacts include resolution steps, knowledge base articles, and playbooks that could have assisted with faster incident resolution. The system helps administrators identify these gaps in automation coverage and prioritize them for future improvements.

## How missed opportunities are tracked

When an incident is resolve in SOW, and the Recommendation section does not show any artifacts, the automation opportunity is marked as 'missed automation'.

Missed opportunities are logged in a dedicated table that captures:

-   incident details
-   Available automation artifacts that could have helped
-   User information and timing data

## Types of missed opportunities

LEAP tracks several types of missed automation opportunities:

-   **Resolution steps**

    Generated step-by-step procedures that could have guided incident resolution.

-   **Knowledge base articles**

    Relevant documentation and solutions that could have provided immediate answers but were not consulted during incident resolution.

-   **Playbooks**

    Automated workflows that could have streamlined the resolution process.


## Viewing missed opportunities

The LEAP homepage displays the missed automation opportunities card.

Select the number on the missed opportunities card to filter and view only the automation opportunities that missed automation. On the details page for each automation opportunity, you can see how many times an artifact was not available when it could have assisted with incident resolution.

\[Omitted image "missed-automation-opportunity.png"\] Alt text: Missed opportunity in automation opportunity details page

LEAP administrators can use missed opportunity data to identify patterns and improve automation coverage. This helps determine where additional automation artifacts might be beneficial.

Regular review of missed opportunities enables administrators to identify gaps in automation coverage for common incident types and prioritize creation of new automation artifacts based on potential impact.

## Benefits of tracking missed opportunities

Tracking missed automation opportunities provides valuable insights for continuous improvement of automation strategies:

-   Identifies high-impact areas where automation could provide the greatest benefit
-   Helps justify investment in additional automation development
-   Provides data-driven insights for improving user adoption of existing automation
-   Enables measurement of automation program effectiveness and ROI
-   Supports strategic planning for future automation initiatives


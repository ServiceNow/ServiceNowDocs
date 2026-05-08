---
title: Missed automation opportunities
description: Track instances where users could have benefited from generated resolution steps, knowledge base articles, or playbooks but did not have access to them.
locale: en-US
release: australia
product: AIOps LEAP \(Learning-Enhanced Automation Playbooks\)
classification: aiops-leap-learning-enhanced-automation-playbooks
topic_type: concept
last_updated: "2026-05-07"
reading_time_minutes: 2
keywords: [missed opportunities, LEAP, automation tracking, resolution steps, playbooks, knowledge base]
breadcrumb: [Exploring LEAP, Learning Enhanced Automation Platform \(LEAP\), Now Assist for ITOM, IT Operations Management]
---

# Missed automation opportunities

Track instances where users could have benefited from generated resolution steps, knowledge base articles, or playbooks but did not have access to them.

Missed automation opportunities occur when users work on incidents that could have benefited from existing LEAP automation artifacts but did not have access to them at the time. The system tracks these automation opportunities to help administrators identify gaps in automation coverage and prioritize future improvements.

LEAP automatically logs missed opportunities when users resolve incidents manually while relevant automation artifacts exist. These artifacts include resolution steps, knowledge base articles, and playbooks that could have assisted with faster incident resolution.

## How missed opportunities are tracked

The system monitors incident resolution patterns and compares them against available automation artifacts. When a user resolves an incident manually, LEAP checks whether existing automation could have provided assistance.

Missed opportunities are logged in a dedicated table that captures:

-   incident details and resolution information
-   Available automation artifacts that could have helped
-   User information and timing data
-   Potential time and cost savings

## Types of missed opportunities

LEAP tracks several types of missed automation opportunities:

-   **Resolution steps**

    Generated step-by-step procedures that could have guided incident resolution but were not accessed by the user.

-   **Knowledge base articles**

    Relevant documentation and solutions that could have provided immediate answers but were not consulted during incident resolution.

-   **Playbooks**

    Automated workflows that could have streamlined the resolution process but were not triggered or utilized.


## Viewing missed opportunities

LEAP administrators can review missed opportunities through the LEAP value dashboard. The dashboard displays tracked automation opportunities.

The missed opportunities card on the LEAP dashboard provides the number of missed opportunities and when clicked, navigates to the LEAP landing page.

LEAP administrators can use missed opportunity data to identify patterns and improve automation coverage. This helps determine where additional automation artifacts might be beneficial or where existing artifacts need better visibility.

Regular review of missed opportunities enables administrators to identify gaps in automation coverage for common incident types and prioritize creation of new automation artifacts based on potential impact.

## Benefits of tracking missed opportunities

Tracking missed automation opportunities provides valuable insights for continuous improvement of automation strategies:

-   Identifies high-impact areas where automation could provide the greatest benefit
-   Helps justify investment in additional automation development
-   Provides data-driven insights for improving user adoption of existing automation
-   Enables measurement of automation program effectiveness and ROI
-   Supports strategic planning for future automation initiatives


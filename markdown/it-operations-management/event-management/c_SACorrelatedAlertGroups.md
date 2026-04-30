---
title: Automated alert grouping
description: Automated alert grouping is a process that uses historical data to automatically organize similar alerts into groups. These alerts could be system issues, like server errors or network outages. By grouping related alerts together, it helps teams quickly identify patterns, manage recurring problems, and reduce the noise from too many individual alerts.
locale: en-US
release: zurich
product: Event Management
classification: event-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Alert grouping types and creation methods, Alert grouping, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Automated alert grouping

Automated alert grouping is a process that uses historical data to automatically organize similar alerts into groups. These alerts could be system issues, like server errors or network outages. By grouping related alerts together, it helps teams quickly identify patterns, manage recurring problems, and reduce the noise from too many individual alerts.

Imagine you’re monitoring a city’s traffic system. You get a lot of alerts—like reports of accidents, traffic jams, and road closures. Automated alert grouping works like a smart assistant that organizes these alerts based on patterns, so you can see related issues together and respond more efficiently. These automated alert groups are displayed in the Express List within the Service Operations Workspace.

## How do you enable this grouping

To enable machine learning-based automation for alert correlation, set the property **Enable ML based Automation correlation** \(sa\_analytics.specific\_patterns\_enabled\) to true.

If the Domain Support - Domain Extensions Installer is activated, alert aggregation patterns are created based on the domain level defined in the sa\_analytics.agg.learner\_domain\_level property. By default, this domain level is set to two, which corresponds to the second level in the domain hierarchy. For example, in a company, Level 1 might represent the company itself, while Level 2 could represent departments or teams within the company. Alerts are grouped based on this second level, like sorting them by department or team. For more details, [Domain separation and Event Management](domain-separation-event-management.md).

## How does it work

Automated alert grouping uses machine learning \(ML\) and historical data to identify patterns among alerts. It looks at specific characteristics, called pattern identifiers—such as the type of issue, the affected system, CI or metric that happened multiple times within a similar time period—to determine if alerts are related. The Alert Aggregation Learner uses algorithms to group alerts based on patterns. Specifically, it uses pattern-based algorithms and probabilistic methods to analyze incoming alerts and identify related ones.

Think of it like noticing that accidents often happen at a particular intersection at rush hour. The system groups similar alerts \(like recurring traffic jams at the same spot\) together based on certain identifiers \(like location or type of problem\). The system follows these key steps to group alerts effectively:

-   Analyze Historical Data: The system studies past alerts to learn patterns and relationships.
-   Apply Machine Learning: ML algorithms analyze historical alert data to identify patterns and relationships among alerts. It enables the system to learn from past incidents and improve its ability to group similar alerts together over time.
-   Group Similar Alerts: Alerts with matching patterns are automatically grouped together.

Imagine you're managing a city's traffic system, and you receive multiple alerts:

-   8:00 AM: Accident on Main Street
-   8:05 AM: Traffic jam near Main Street
-   8:10 AM: Road closure on Main Street

Automated alert grouping works like a smart assistant by analyzing these alerts and recognizing a pattern. It groups them together because they all relate to Main Street, likely stemming from the same accident. This helps you see the bigger picture quickly and focus on resolving the root cause \(the accident\), rather than addressing each alert separately.

## Benefits

-   Find Recurring Issues: Quickly spot patterns \(like a server consistently overheating\).
-   Save Time: Handle groups of related alerts instead of individual ones.
-   Improve Response: Focus on fixing the root cause rather than dealing with scattered issues.


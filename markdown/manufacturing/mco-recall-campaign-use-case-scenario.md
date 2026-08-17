---
title: Recall campaign use case
description: Use case scenarios demonstrate when and how to use the Recall Campaign application to create a recall campaign. It provides practical examples of common recall management situations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/manufacturing/mco-recall-campaign-use-case-scenario.html
release: australia
topic_type: concept
last_updated: "2026-03-16"
reading_time_minutes: 2
breadcrumb: [Recall campaign, MCO core, Explore, Manufacturing Commercial Operations]
---

# Recall campaign use case

Use case scenarios demonstrate when and how to use the Recall Campaign application to create a recall campaign. It provides practical examples of common recall management situations.

## Use case: Multi-Region product recall

Scenario

Alectri, an automotive OEM, identified a defect in airbags installed in 2024 vehicles and must launch a coordinated recall campaign across the Americas and Europe. Managing global recalls across multiple regions and dealer networks creates several challenges:

-   Visibility gaps: Limited visibility into active campaigns and claims across regions.
-   Coordination bottlenecks: Coordinating tasks across departments and regions causes delays and rework.
-   Manual tracking: Tracking multiple corrective actions per recall is error-prone and time-consuming.
-   Cost inconsistency: Cost estimation inconsistencies lead to claim delays and denials.
-   Dealer friction: Dealers lack timely access to campaign information and submission tools.
-   Regional complexity: Regional coordination complexity slows recall execution and visibility.

Solution

Chloe, the Global Recall Manager at Alectri, uses Manufacturing Commercial Operations \(MCO\) to manage the recall through four key workflow phases:

1.  Create: Configure campaign with name, issue number, priority, and quality system traceability.
2.  Define: Add corrective actions \(airbag replacement, sensor replacement, software updates\) with predefined labor and parts charges.
3.  Target: Use asset filters to isolate affected vehicles \(2024 models with defective airbags\) and create regional phases with local owners and timelines.
4.  Publish and Monitor: Validate phases, publish to dealer portal, and track claims and corrective actions in real-time.

The [Recall management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/manufacturing/mco-recall-management.md) provides real-time visibility into all campaigns, claims, and affected assets throughout the recall life-cycle.

Benefits

Compare the impact of using the Recall Campaign application:

|Without MCO|With MCO Recall Campaign|
|-----------|------------------------|
|Limited visibility into campaigns and regions|Centralized dashboard for all campaigns, claims, and affected assets.|
|Manual, error-prone corrective action tracking|Multiple corrective actions tracked within one campaign with predefined charges.|
|Inconsistent cost estimation and claim denials|Standardized pricing reduces claim delays and rework.|
|Cross-department bottlenecks and coordination delays|Task management and phased rollouts with regional owners eliminate bottlenecks.|
|Dealers lack timely campaign information|Portal access provides claim submission and campaign details self-service.|

Outcome

Alectri successfully launches a coordinated multi-region recall campaign with clear corrective actions, standardized costs, and precise vehicle targeting. Regional phases enable phased rollout across markets, and dealers have immediate access to campaign information through the portal, enabling smooth claim processing across the OEM-dealer ecosystem.


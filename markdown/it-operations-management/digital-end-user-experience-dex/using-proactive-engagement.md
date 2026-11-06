---
title: Using Proactive Engagement
description: Proactive Engagement helps you in proactive detection of digital issues and provides self-help instructions to resolve them.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-operations-management/digital-end-user-experience-dex/using-proactive-engagement.html
release: australia
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 3
keywords: [proactive engagement, self-help, employee engagement, metric rules, proactive engagement workbench, life-cycle management]
breadcrumb: [Digital End-User Experience, IT Operations Management]
---

# Using Proactive Engagement

Proactive Engagement helps you in proactive detection of digital issues and provides self-help instructions to resolve them.

## Proactive Engagement employee experience

Every Proactive Engagement trigger creates an experience issue record. When a metric rule with a Proactive Engagement resolution triggers, the end user receives a notification for the issue. If the end user consents to help, they are engaged over a Virtual Agent to self-solve the issue. Successful resolution prompts an end-user confirmation and a request for feedback. If the issue is not resolved, the configured fallback option is provided. For the full flow, see [Employee engagement experience through Proactive Engagement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/digital-end-user-experience-dex/employee-engagement-experience.md).

## How the agent experience fits in

When a resolution fails or an employee marks the issue as unresolved, the system creates a fallback incident and routes it to an agent. Agents can review the interaction summary in the work notes. The summary includes the resolution that was executed and its outcome. The system tags the associated experience issue record as the origin of the incident. For details, see [Agent experience through Proactive Engagement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/digital-end-user-experience-dex/agent-experience-pe.md).

## Base system solution

The base system provides two Proactive Engagement resolutions that detect high disk usage and give the end user operating-system-specific self-help instructions: **Check system disk usage for Windows** and **Check system disk usage for Mac**. These base resolutions are surfaced through metric rules in DEX Administration and must be activated before they can trigger. For details, see [Proactive Engagement solution](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/digital-end-user-experience-dex/proactive-engagement-solution.md).

## How metric rules trigger Proactive Engagement

Metric rules create an alert based on their trigger criteria, and an alert action starts Proactive Engagement when the alert is created and the configured conditions are met. System properties let you customize the throttling window, per-user freeze period, per-user throttling limits for device and application resolutions, and the enabled notification channels. Alert closure differs by resolution type: device alerts close after Proactive Engagement helps the impacted users resolve their issue, while application alerts are not closed. For the full list of system properties and their defaults, see [Metric rule triggering Proactive Engagement through alerts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/digital-end-user-experience-dex/metric-rule-triggering-pe-through-alerts.md).

## Managing solutions with the Proactive Engagement Workbench

The Proactive Engagement Workbench provides an overview of all Proactive Engagement solutions on your instance. The Workbench shows deployment status and identifies solutions with updates available from ServiceNow. Metric rule solutions deploy automatically by default. You can review available updates and choose to auto-update, manually update, or ignore them. Solutions display states such as **Update available**, **Update up-to-date**, **Update ignored**, and **Pending manual update**. For information about managing solution updates, see [Proactive Engagement life-cycle management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/digital-end-user-experience-dex/proactive-engagement-lcm.md).

-   **[Employee engagement experience through Proactive Engagement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/digital-end-user-experience-dex/employee-engagement-experience.md)**  
The Proactive Engagement application engages end users when a device issue is detected and guides them to resolve the issue themselves.
-   **[Agent experience through Proactive Engagement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/digital-end-user-experience-dex/agent-experience-pe.md)**  
When a Proactive Engagement resolution doesn't resolve an end-user device issue, a fallback incident reaches an agent, who can review the interaction summary to continue troubleshooting.
-   **[Proactive Engagement solution](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/digital-end-user-experience-dex/proactive-engagement-solution.md)**  
The base system solution detects and enables you to resolve high disk usage issues by providing a detailed self-help instruction specific to the operating system.
-   **[Metric rule triggering Proactive Engagement through alerts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/digital-end-user-experience-dex/metric-rule-triggering-pe-through-alerts.md)**  
Metric rules create alerts based on their trigger criteria, and the alert actions trigger Proactive Engagement.
-   **[Proactive Engagement life-cycle management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/digital-end-user-experience-dex/proactive-engagement-lcm.md)**  
The Proactive Engagement application supports life-cycle management of solutions. Use it to manage solutions you own and to view solutions that affect your services or products.

**Parent Topic:**[Digital End-User Experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/digital-end-user-experience-dex/dex-landing-cf.md)


---
title: Reporting and metrics for industrial task flows
description: Use the fields available to distinguish workflows and produce reliable metrics.
locale: en-US
release: australia
product: Digital Factory Workspace
classification: digital-factory-workspace
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Explore, Digital Factory Workspace, Industrial Connected Workforce]
---

# Reporting and metrics for industrial task flows

Use the fields available to distinguish workflows and produce reliable metrics.

Industrial operations often run multiple task flow on the same underlying tables, which makes clean reporting difficult unless one flow can clearly be distinguished from another. To address this requirement, a configurable field called task\_classification has been introduced across all industrial task types. Although it doesn’t have to be visible in the UI, it provides the essential metadata. This metadata separates tasks that share storage from the tasks that should follow different workflows. It's primarily used to distinguish breakdowns from deviations and to differentiate breakdown analyses from root cause analyses \(RCAs\). The tables remain common, but the classification value determines the workflow branch, which enables that each category can be reported independently without duplicating data structures.

In addition to classification, deviations include a system-only contact\_type field with default values that the system sets automatically. These values aren’t user-facing and exist only to support metrics and funnel reporting. A deviation with the contact\_type:

-   None: Follows the regular deviation life cycle
-   New: A deviation is created with classification breakdown
-   Converted: A deviation is escalated to a breakdown

With these two markers, teams can produce straightforward counts. For example, how many breakdowns were created, how many deviations remained regular, and how many deviations escalated, without introducing additional UI complexity.

**Parent Topic:**[Exploring Digital Factory Workspace](exploring-digital-factory-workspace.md)


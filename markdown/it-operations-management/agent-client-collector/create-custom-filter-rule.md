---
title: Create a custom filter rule
description: Create a custom filter rule in the Software Install Custom Filter table \(samp\_sw\_install\_custom\_filter\). Rules determine the criteria by which software is excluded from your Software Asset Management \(SAM\) workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/agent-client-collector/create-custom-filter-rule.html
release: zurich
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
keywords: [custom filter, exclusion rule, software, SAM]
breadcrumb: [Software filter, ACC deployment - shared between servers and endpoints, Agent Client Collector, IT Operations Management]
---

# Create a custom filter rule

Create a custom filter rule in the Software Install Custom Filter table \(samp\_sw\_install\_custom\_filter\). Rules determine the criteria by which software is excluded from your Software Asset Management \(SAM\) workspace.

## Before you begin

Role required: agent\_client\_collector\_admin

## Procedure

1.  Navigate to the Software Install Custom Filter table **All** &gt; **Software Install Custom Filter**.

2.  Select **New** to create a custom filter rule.

3.  Complete the fields based on the software you want to exclude.

    For details on the available fields, see [Software filter fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/agent-client-collector/sw-filter-fields.md).

4.  Select **Submit**.


## Result

The custom filter rule is created and takes effect on the next discovery or agent scan that reports matching software.

## Exclude a custom internal shortcut

Your organization has an internal tool that installs a desktop shortcut called **Company Portal Shortcut** on every managed Windows device. To ensure that it doesn't clutter your SAM inventory, configure the rule as follows:

-   **Name**: Exclude Company Portal Shortcut
-   **Software Name**: Company Portal Shortcut, Condition: Exact match
-   **OS Filter**: Windows
-   **Discovery Source**: \(leave blank\)
-   **Active**: On

From the next scan onward, any Windows device reporting **Company Portal Shortcut** will have that entry excluded from the SAM inventory and logged in the review table instead.

**Parent Topic:**[Software filter](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/agent-client-collector/software-filter.md)


---
title: Grouping of tasks in status reports of CWM My Work
description: Learn how various tasks assigned to you are grouped based on their State and Priority in My Work reports of Collaborative Work Management \(CWM\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/collaborative-work-management/grouping-of-tasks-in-status-reports-of-cwm-my-work.html
release: australia
product: Collaborative Work Management
classification: collaborative-work-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Reference, Collaborative Work Management, Strategic Portfolio Management]
---

# Grouping of tasks in status reports of CWM My Work

Learn how various tasks assigned to you are grouped based on their State and Priority in My Work reports of Collaborative Work Management \(CWM\).

## State buckets

State buckets represent the lifecycle stage of different tasks. Existing state values from different task types are automatically mapped into these buckets based on meaning and also internal value of any task type. In My Work, all states are automatically grouped into three standard State Buckets.

-   Open: Represents tasks not yet started. For example, states of Draft, Pending, and Ready.
-   Work in Progress: Represents tasks currently being worked on. For example, states of In Progress, Implement, and Testing.
-   Closed: Represents tasks that are finished or no longer active. For example, states of are Complete, Cancelled, and Closed Skipped.

## Priority buckets

Priority buckets provide a unified way to understand the urgency of tasks. Priority buckets are created by mapping existing priority values from the Task table. All tasks are automatically grouped into five Priority Buckets.

-   Planning: Not yet prioritized.
-   Low: Minimal urgency.
-   Moderate: Medium priority tasks.
-   High: Important tasks that require attention soon.
-   Critical: Most urgent tasks.

## Custom State and Priority values

Your ServiceNow instance may have some extended task types that have custom state or priority values. These custom values may not align with the default values of the Task table. These work items with these non-default State or Priority values appear as **Others** in the bar graphs in My Work. This method ensures reporting accuracy instead of forcing a state/priority into the wrong bucket.

\[Omitted image "cwm-my-work-other.png"\] Alt text: Other grouping for State and Priority.

**Parent Topic:**[Collaborative Work Management reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/collaborative-work-management/reference-cwm.md)

**Related topics**  


[My Work in CWM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/collaborative-work-management/my-work-in-cwm.md)


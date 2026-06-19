---
title: Related log entities alert grouping
description: The Related log entities \(formerly known as Health Log Analytics alert grouping automatically gathers HLA alerts that originate from the same log query job into a single, organized group. Instead of a scattered collection of individual log-based alerts, your team gets one consolidated view of everything tied to the same underlying log event — speeding up issue response.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/event-management/log-analytics-alert-grouping.html
release: australia
product: Event Management
classification: event-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Mixed alert grouping, Alert grouping types and creation methods, Alert grouping, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Related log entities alert grouping

The Related log entities \(formerly known as Health Log Analytics alert grouping automatically gathers HLA alerts that originate from the same log query job into a single, organized group. Instead of a scattered collection of individual log-based alerts, your team gets one consolidated view of everything tied to the same underlying log event — speeding up issue response.

When Health Log Analytics processes log data, a single query job can generate multiple related alerts — each representing a different aspect of the same detected issue, such as a top-level component alert and its associated host-level alerts. Without grouping, these arrive as separate, unconnected notifications.

The Related log entities alert grouping solves this by recognizing that all alerts produced by the same query job share a common origin — the same HLA incident. It uses that shared origin as the basis for pulling those alerts into one group, giving your team a complete, unified picture of what the log data is reporting.

## Use case 1: Database slowdown detected across multiple components

A log analytics query job runs against your database infrastructure and detects a performance degradation event. The job produces three alerts: one for a slow query on the primary database node, one for a connection pool exhaustion on the application server, and one for elevated error rates in the middleware layer — all stemming from the same underlying log event.

Without Related log entities alert grouping, these three alerts land in the operations queue as separate, unrelated notifications. An engineer picking up the connection pool alert has no immediate visibility into the slow query alert sitting alongside it.

With Related log entities alert grouping, all three alerts are automatically pulled into one group. The on-call engineer opens one group, sees the full picture at once, and can immediately identify the root cause rather than piecing it together from three disconnected alerts.

## Use case 2: Application error spike across multiple hosts

Your Health Log Analytics setup monitors a distributed web application across several hosts. A query job detects an error spike and generates a top-level alert for the application service along with secondary alerts for each host where the errors were observed — Host A, Host B, and Host C.

Related log entities alert grouping recognizes that all these alerts share the same HLA incident ID and groups them together. Instead of the operations team seeing four separate alerts and wondering whether they are related, they see one group that immediately communicates: this is one event, affecting one application, across three hosts.

Use case 1 is good if you want to highlight the cross-component nature of the grouping — showing that alerts about different infrastructure pieces get linked together. Use case 2 is better if you want to highlight the multi-host scenario, which maps more directly to how HLA alert hierarchies actually work \(top-level + secondary alerts per host\).

For details on creating a group automation, see [Create Group automation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-operations-workspace-for-itom-apps/group-alert-sow-itom.md).


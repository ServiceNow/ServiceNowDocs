---
title: Mixed alert grouping
description: Mixed alert grouping combines multiple strategies—currently CMDB-based, tag-based, related log entities-based, and shared impacted services-based grouping—to form a single, cohesive alert group. It reduces noise, bridges gaps when one method isn't enough, and delivers a clearer, end-to-end view of incidents. This approach helps operators identify root causes faster and take informed action, even in complex or incomplete data environments.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/event-management/unified-grouping.html
release: australia
product: Event Management
classification: event-management
topic_type: concept
last_updated: "2026-06-22"
reading_time_minutes: 1
breadcrumb: [Alert grouping types and creation methods, Alert grouping, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Mixed alert grouping

Mixed alert grouping combines multiple strategies—currently CMDB-based, tag-based, related log entities-based, and shared impacted services-based grouping—to form a single, cohesive alert group. It reduces noise, bridges gaps when one method isn't enough, and delivers a clearer, end-to-end view of incidents. This approach helps operators identify root causes faster and take informed action, even in complex or incomplete data environments.

To understand how Mixed grouping works in practice, it's important to look at the individual strategies it currently supports. At this stage, Mixed Grouping includes four core methods. CMDB-based alert grouping uses service relationships defined in the CMDB. Tag cluster alert grouping uses shared metadata across alerts. Related log entities alert grouping correlates alerts based on associated log entities. Shared impacted services alert grouping groups alerts that affect common services. Each method plays a distinct role in effectively correlating related alerts.

If you're looking to group alerts, see [Create Group automation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-operations-workspace-for-itom-apps/group-alert-sow-itom.md).


---
title: Shared impacted services alert grouping
description: The Shared impacted services alert grouping automatically gathers related alerts under the business service they affect. When your IT environment generates multiple alerts at once, instead of facing a flood of disconnected notifications, your team gets one focused, organized view — making it faster to spot what is broken and act.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/event-management/shared-impacted-services-grouping.html
release: australia
product: Event Management
classification: event-management
topic_type: concept
last_updated: "2026-06-22"
reading_time_minutes: 3
breadcrumb: [Mixed alert grouping, Alert grouping types and creation methods, Alert grouping, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Shared impacted services alert grouping

The Shared impacted services alert grouping automatically gathers related alerts under the business service they affect. When your IT environment generates multiple alerts at once, instead of facing a flood of disconnected notifications, your team gets one focused, organized view — making it faster to spot what is broken and act.

The Shared impacted services alert grouping feature solves this by automatically gathering related alerts into one place. It looks at each alert, figures out which business service is ultimately affected — for example, Online Payments or HR Portal — and groups all alerts that point to the same service together.

## How the grouping decision is made

Every alert is linked to a Configuration Item \(CI\) — the specific piece of infrastructure where the problem was detected, such as a web server or a network switch. That CI is part of a larger chain: it supports an application, which in turn supports a Business Service.

When Event Management receives an alert, it traces that chain upward to find the most important Business Service \(identified by business criticality\) the CI belongs to. This is called the Top Service. Any other alerts that trace back to the same Top Service are automatically pulled into the same group.

Think of it like a network operations center \(NOC\) dashboard: instead of investigating each blinking alert one by one, the operator first identifies the most critical service that is down — that is the Top Service. Every alert tied to that Top Service is already grouped together, giving an instant picture of the full impact.

With CMDB-based alert grouping, alerts are only grouped if the CIs involved are closely connected in the topology — there is a limit on how far apart they can be. Shared Impacted Services grouping works differently: it does not care about the distance between CIs at all. If two alerts trace back to the same Top Service, they are grouped — regardless of how far apart the underlying CIs are in the infrastructure.

## When to use this feature

ServiceNow Event Management offers two approaches to alert grouping, and choosing the right one depends on how your service topology is structured.

CMDB-based alert grouping works well when your infrastructure is relatively flat — where CIs supporting a service are no more than four topology hops away from each other. Within that boundary, it groups alerts based on the relationships between CIs in the CMDB.

Shared Impacted Services grouping is the better choice when your service topology is deep or complex. In large organizations, a Business Service often sits at the top of a long chain — with applications, middleware, databases, and infrastructure components layered beneath it across many levels. If a CI is five, six, or more hops away from the top of that chain, CMDB-based grouping will not include its alerts in the group. Shared Impacted Services grouping has no such restriction — as long as an alert's CI traces back to the same Top Service, it is grouped, no matter how deep in the topology that CI sits.

In short: if your service trees are shallow, either approach works. If your service trees are deep and span many topology levels, use Shared Impacted Services grouping to ensure no related alert is left out.

For details on creating a group automation, see [Create Group automation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-operations-workspace-for-itom-apps/group-alert-sow-itom.md).


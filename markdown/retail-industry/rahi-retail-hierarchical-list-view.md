---
title: Hierarchical list view
description: The hierarchical list view on the Track Plan tab presents a plan's generated cases and tasks as a navigation tree, so managers can move from the plan down to an individual store task without losing context.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/retail-industry/rahi-retail-hierarchical-list-view.html
release: brazil
topic_type: concept
last_updated: "2026-10-05"
reading_time_minutes: 3
breadcrumb: [Track and monitor store plans, Retail]
---

# Hierarchical list view

The hierarchical list view on the Track Plan tab presents a plan's generated cases and tasks as a navigation tree, so managers can move from the plan down to an individual store task without losing context.

Unlike the plan progress summary, the hierarchical list view is not restricted to particular plan types. It is driven by the plan type configuration, so it supports the plan types provided with the base system and any plan types added later. Custom plan types that use custom case or task states might require additional configuration.

## Navigation tree

The name of the store plan appears above the tree. The tree lists the records generated for the selected schedule occurrence, as separate nodes for each type of record. Node labels follow the plan type: a store audit plan shows its audit case and audit tasks in place of the HQ case and HQ tasks.

-   HQ case
-   HQ tasks, listed individually
-   Store cases
-   Store tasks, listed individually

When the tab loads, the store case node is selected and the list on the right shows that node's records. Selecting a different node updates the list.

The tree lists a maximum of 100 template items. A plan with more than 100 items isn't fully represented in the tree.

## State tabs and counts

The list is organized into All, Open, Closed, and Overdue tabs. Each tab shows a count in brackets for the selected node and the selected occurrence.

The tab filter and the tree selection combine rather than replace each other:

-   Selecting a different node keeps the active tab and applies to the states that correspond to that node's type of record.
-   Selecting a different occurrence keeps both the selected node and the active tab. If the node no longer exists for the new occurrence, the store case node is selected instead.
-   When a node or an occurrence has no matching records, the list shows an empty state.

## States behind each tab

|Type of record|Tab|States included|
|--------------|---|---------------|
|HQ case, store case, and store audit case|Open|New, Open, Awaiting info|
|HQ case, store case, and store audit case|Closed|Closed, Resolved, Cancelled|
|HQ task|Open|Open, Awaiting information, In Progress|
|HQ task|Closed|Closed|
|Store task and audit task|Open|Pending assignment, Accepted|
|Store task and audit task|Closed|Closed complete|
|All types|Overdue|Any open state where the due date and time have passed. A record is overdue when its due date and time are in the past and it is in one of the open states for its record type.|

## Filtering and record details

Store cases and store tasks can be filtered by store name to narrow the list to a particular part of the retail organization.

The columns shown for each type of record are configured in the list view for plan tracking. The organization column depends on the plan type. For store audit plans, audit cases show the auditee organization and audit tasks show the requestor organization. For HQ communications plans, store cases show the supporting retail org and store tasks show the provider organization. No organization column is configured for the HQ case or the HQ task, because each is a single record per node.

An information icon marks records that have a questionnaire attached, with a **Questionnaire added** tooltip. The icon is informational only.

The list is read-only. Records are opened from the tree and the list rather than created or edited in place, so no new record action, row actions, or inline editing are available.

**Parent Topic:**[Track and monitor store plans](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/retail-industry/track-monitor-store-plans.md)


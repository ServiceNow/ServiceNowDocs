---
title: Advanced Work Assignment monitoring page
description: Administrators \(admin or awa\_admin\) can monitor Advanced Work Assignment activity by reviewing information on the Advanced Work Assignment Stats page.
locale: en-US
release: xanadu
product: Advanced Work Assignment
classification: advanced-work-assignment
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Reference, Advanced Work Assignment, Manage people and work capabilities, Extend ServiceNow AI Platform capabilities]
---

# Advanced Work Assignment monitoring page

Administrators \(admin or awa\_admin\) can monitor Advanced Work Assignment activity by reviewing information on the Advanced Work Assignment Stats page.

The Advanced Work Assignment Stats page displays AWA performance statistics. Administrators can access the Advanced Work Assignment Stats page by entering `<instance_url>/awa_stats.do` where instance\_url is the base of the ServiceNow URL.

**Note:** The mean, median, max, and min statistics are representative of the particular node you are viewing.

|Field|Description|
|-----|-----------|
|Agent Status|Overview of agent status for all assigned agents|

## Channel Summaries

|Field|Description|
|-----|-----------|
|Number Queued|Number of work items currently queued|
|Number Pending Acceptance|Number of work items currently pending acceptance|
|Number of Duplicates|Number of duplicate work items \(meaning same document id, usually from transfers\)|
|Number Rejected|Number of work items rejected|
|Current Number Meeting Channel Condition|Number of work items with the channel condition met|
|Current Number Meeting Utilization Condition|Number of work items with the current utilization condition met|
|Current Number Meeting Channel &amp; Utilization Condition|Number of work items meeting both channel and utilization condition|
|Total Work Item Count|Total number of work items for the given channel|

|Field|Description|
|-----|-----------|
|Max Query Response Time|Maximum amount of time for the response of querying all the active and unassigned work items of a given channel|
|Min Query Response Time|Minimum amount of time for the response of querying all the active and unassigned work items of a given channel|
|Mean Query Response Time|Mean amount of time for the response of querying all the active and unassigned work items of a given channel|
|Median Query Response Time|Median amount of time for the response of querying all the active and unassigned work items of a given channel|
|Total Query Count|Total number of times the query for inactive/unassigned work items has been made for the given channel|

|Field|Description|
|-----|-----------|
|Record Watcher Entries Present|True if the required record watchers for the channel exist \(channel eligibility responder, work item responder, workload responder\).|
|Number of Entries Triggered|Number of times onEntry has been called on this node for the given record watcher|
|Number of Exits Triggered|Number of times onExit has been called on this node for the given record watcher|
|Number of Changes Triggered|Number of times onChange has been called on this node for the given record watcher|

|Field|Description|
|-----|-----------|
|Total Number of Queues|Total number of active queues for a given channel|
|Number of Queues in Schedule|Number of queues for a given channel that are currently in schedule|
|Number of Queues Out of Schedule|Number of queues for a given service channel that are currently out of schedule|
|Number of Inactive Queues|Number of queues that are not marked as active|

|Field|Description|
|-----|-----------|
|Agent status overview for the given channel|Number of agents with this status|

## Channel Breakdown

|Field|Description|
|-----|-----------|
|In Schedule|True if the queue is in schedule, false otherwise|
|Agents Available|True if the given queue has agents available, false otherwise|
|Number of Agents Available|Number of agents marked as available for the given queue|
|Number of Work Items Queued|Number of work items queued for the given queue|
|Number of Work Items Pending Acceptance|Number of work items pending acceptance for the given queue|
|Max Routing Time for Work Items|Maximum routing time of creating a work item for a given record and assigning it to the queue|
|Min Routing Time for Work Items|Minimum routing time of creating a work item for a given record and assigning it to the queue|
|Mean Routing Time for Work Items|Mean routing time of creating a work item for a given record and assigning it to the queue|
|Median Routing Time for Work Items|Median routing time of creating a work item for a given record and assigning it to the queue|
|Total Routing Count of Work Items|Total number of work items routed to the queue from created records|

**Parent Topic:**[Advanced Work Assignment reference](reference-awa.md)

**Related topics**  


[Assignment Rule form](awa-assignment-rules.md)

[Domain separation and Advanced Work Assignment](awa-domain-separation.md)

[Components installed with Advanced Work Assignment](installed-with-awa.md)

[Properties for Advanced Work Assignment](awa-properties.md)

[Advanced Work Assignment roles](awa-roles.md#)


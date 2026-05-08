---
title: Components installed with Advanced Work Assignment
description: Several types of components are installed with activation of the Advanced Work Assignment plugin, including tables, user roles, and scheduled jobs.
locale: en-US
release: australia
product: Advanced Work Assignment
classification: advanced-work-assignment
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Reference, Advanced Work Assignment, Manage people and work, Conversational Interfaces]
---

# Components installed with Advanced Work Assignment

Several types of components are installed with activation of the Advanced Work Assignment plugin, including tables, user roles, and scheduled jobs.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see Find components installed with an application.

Demo data is available for this feature.

## Roles installed

AWA adds the following roles for users who configure, manage, and receive work assignments.

<table id="table_u1t_gb1_wdb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Advanced Work Assignment administrator\[awa\_admin\]

</td><td>

Admin role for the AWA feature. Configures and manages AWA.

</td><td>

awa\_manager

</td></tr><tr><td>

Advanced Work Assignment developer\[awa\_integration\_user\]

</td><td>

Developer role for the AWA feature. Uses the AWA integration APIs.

</td><td>

None

</td></tr><tr><td>

Advanced Work Assignment agent\[awa\_agent\]

</td><td>

Agent role for the AWA feature. Handles customer interactions and manages workload across multiple service channels.

</td><td>

None

</td></tr><tr><td>

Advanced Work Assignment manager\[awa\_manager\]

</td><td>

Manager role for the AWA feature. Monitors performance of agents across all service channels.

</td><td>

None

</td></tr></tbody>
</table>## Scheduled jobs installed

|Scheduled job|Description|
|-------------|-----------|
|**AWA WorkItem TimeOut Job**| |
|AWA Cleanup Job| |

## Tables installed

<table id="table_fbz_45z_vdb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

AWA Agent Capacity\[awa\_agent\_capacity\]

</td><td>

Stores capacity override records for agents on individual channels.

</td></tr><tr><td>

AWA Agent Channel Availability\[awa\_agent\_channel\_availability\]

</td><td>

Store the records that determine the agents available in the channel.

</td></tr><tr><td>

AWA Agent Presence\[awa\_agent\_presence\]

</td><td>

Stores the records that define the agent availability state.

</td></tr><tr><td>

AWA Agent Presence History\[awa\_agent\_presence\_history\]

</td><td>

Stores records on agent presence state changes.

</td></tr><tr><td>

AWA Assignment Rule\[awa\_assignment\_rule\]

</td><td>

Stores the assignment rule records used to determine the work items pushed to agents.

</td></tr><tr><td>

AWA Eligibility Pool\[awa\_eligibility\_pool\]

</td><td>

Stores the records that define grouping of agents eligible to receive work items in the queue when the items have been rejected by agents or agents are unavailable.

</td></tr><tr><td>

AWA Group Queue Priority\[awa\_group\_queue\_priority\]

</td><td>

Stores the priority values for queues assigned to groups.

</td></tr><tr><td>

AWA Inbox Layout\[awa\_inbox\_layout\]

</td><td>

Defines the fields that appear on a work item card in the Agent Workspace inbox.

</td></tr><tr><td>

AWA Offer Details\[awa\_offer\_details\]

</td><td>

Stores whether a work item was assigned using Agent Affinity and how the assignment was completed.

</td></tr><tr><td>

AWA Presence State\[awa\_presence\_state\]

</td><td>

Defines presence states.

</td></tr><tr><td>

AWA Queue\[awa\_queue\]

</td><td>

Stores the work item queue records.

</td></tr><tr><td>

AWA Queue Item Sorting\[awa\_queue\_item\_sorting\]

</td><td>

Defines which fields in a work item for a queue you can sort on.

</td></tr><tr><td>

AWA Reject Reason\[awa\_reject\_reason\]

</td><td>

Stores the records that define the reasons that agents use to decline work items assigned to them.

</td></tr><tr><td>

AWA Service Channel\[awa\_service\_channel\]

</td><td>

Defines the communication channel for which work items may be queued.

</td></tr><tr><td>

AWA Work Item\[awa\_work\_item\]

</td><td>

Stores items of work, for example, chats, cases, or incidents, that are routed from service channels to queues and then to agents.

</td></tr><tr><td>

AWA Work Item Rejection \[awa\_work\_item\_rejection\]

</td><td>

Stores the rejection history records for each work item.

</td></tr></tbody>
</table>## Properties installed

<table id="table_i54_zyj_2gb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

glide.awa.enabled

</td><td>

Enables the auto assignment of work items for Advanced Work Assignment. -   **Type**: true \| false
-   **Default value**: true
-   **Location**: System Property \[sys\_properties\] table

</td></tr><tr><td>

com.snc.awa.cache.enabled

</td><td>

Enables the Advanced Work Assignment cache. -   **Type**: true \| false
-   **Default value**: true
-   **Location**: System Property \[sys\_properties\] table

</td></tr></tbody>
</table>
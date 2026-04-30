---
title: View Event Management license usage
description: Event Management is licensed based on the number of CIs bound to alerts during the last year. For alerts that are not bound to CIs, the system calculates the number of nodes \(servers\) that can send events to the instance directly or through a third-party monitoring tool during the last year.
locale: en-US
release: xanadu
product: Event Management
classification: event-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring Event Management, Event Management, ITOM Health, IT Operations Management]
---

# View Event Management license usage

Event Management is licensed based on the number of CIs bound to alerts during the last year. For alerts that are not bound to CIs, the system calculates the number of nodes \(servers\) that can send events to the instance directly or through a third-party monitoring tool during the last year.

## Before you begin

Role required: evt\_mgmt\_admin or evt\_mgmt\_operator

## About this task

The **Event Management - Node Count Store** job calculates the number of unique nodes that send event information, either directly or through third-parties, to Event Management and are eligible for licensing in the last year. The information from this job is stored in the License Usage \[em\_unique\_nodes\] table for visibility by all users. CIs bound to alerts are counted towards licensing; if there are no CIs that are bound to alerts, the event node field is used. Node is a reference to a server, not the instances of the software on it. Your node count is based on the amount of infrastructure \(servers for example\) that will be sending events.

## Procedure

1.  Navigate to **All** &gt; **Event Management** &gt; **Reporting** &gt; **License Usage**.

    The table is filled automatically based on the alerts in the system. The user has no permission to edit the table. It is used to calculate the usage of the Event Management licensing.

<table id="choicetable_vkj_tnb_dbb"><thead><tr><th align="left" id="d519760e110">

Column

</th><th align="left" id="d519760e113">

Description

</th></tr></thead><tbody><tr><td id="d519760e119">

**CMDB CI**

</td><td>

The CI that is bound to the alert that is generated from the event. If there is a value for this field, the **Node** field is empty.

</td></tr><tr><td id="d519760e131">

**Node**

</td><td>

The string value of the **Node** field of the event. If there is a value for this field, the **CMDB CI** field is empty.

</td></tr><tr><td id="d519760e146">

**Type**

</td><td>

One of these values:-   Unknown - A CI has not bound to the generated alert.
-   Server - The source of the event was a server.
-   PaaS - The source of the event was Platform as a Service.


</td></tr><tr><td id="d519760e167">

**Is licensable**

</td><td>

One of these values:-   True - The event listed is counted towards the license usage.
-   False - The event listed is not counted towards the license usage.


</td></tr></tbody>
</table>
**Parent Topic:**[Configuring Event Management](../concept/using-event-management.md)


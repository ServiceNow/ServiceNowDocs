---
title: Legacy: ITIL dashboard
description: Use this dashboard to view, maintain, and track the tasks and incidents for operating the IT service desk.
locale: en-US
release: australia
product: Incident Management
classification: incident-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Legacy: Incident Management Platform Analytics Solutions, Reporting incidents, Incident Management, IT Service Management]
---

# Legacy: ITIL dashboard

Use this dashboard to view, maintain, and track the tasks and incidents for operating the IT service desk.

**Important:**

Starting in Xanadu release, the ITIL dashboard is deprecated. Users can use [IT Agent dashboard for Service Operations Workspace](../../../product/service-operations-workspace/concept/it-agent-dashboard-sow.md) to view, maintain, and track the tasks and incidents for operating the IT service desk.

![ITIL Dashboard](../image/itil-dashboard-updated.png "ITIL Dashboard")

## Access the ITIL dashboard

To access the ITIL dashboard, navigate to **All** &gt; **Self-Service** &gt; **Dashboard**. On the Dashboards Overview, search for ITIL dashboard.

![ITIL Dashboard Location](../image/itil-dashboard-location.png)

## End user and roles

|End User|Description|Required role|
|--------|-----------|-------------|
|IT Agent|Views, opens, updates, tracks, and closes incidents and tasks for managing customer issues.|itil|
|IT Agent Admin|Can perform all the activities of an IT agent. In addition, the admin can also modify the data and layout.|itil\_admin|

## Data visualizations

The dashboard includes the following visualizations:

|Title|Type|Description|
|-----|----|-----------|
|Critical Tasks|Single score \(![Singe score icon](../../reporting/image/icon-single-score-report-p.png)\)|Total number of open critical task records for which **Priority** is set to **1**.|
|Unassigned Tasks|Single score \(![Singe score icon](../../reporting/image/icon-single-score-report-p.png)\)|Total number of open tasks that are still not assigned.|
|Tasks assigned to me|Single score \(![Singe score icon](../../reporting/image/icon-single-score-report-p.png)\)|Total number of tasks assigned to the logged-user of the dashboard.|
|Active Incidents older than 7 days|Single score \(![Singe score icon](../../reporting/image/icon-single-score-report-p.png)\)|Total number of active incidents logged before seven days.|
|Incident SLA Breached|Single score \(![Singe score icon](../../reporting/image/icon-single-score-report-p.png)\)|Total number of incidents that exceed its SLA.|
|Incident SLAs at Risk|Single score \(![Singe score icon](../../reporting/image/icon-single-score-report-p.png)\)|Total number of active incidents that have not yet exceeded an SLA but have elapsed 75% of the duration of the SLA.|
|My Groups Work|List \(![List report icon](../../reporting/image/icon-list-report-p.png)\)|Outstanding work load \(tasks\) of the logged-in user's group.|
|My Work|List \(![List report icon](../../reporting/image/icon-list-report-p.png)\)|The logged-in user's outstanding work load \(tasks\).|

**Parent Topic:**[Legacy: Incident Management Platform Analytics Solutions](incident-content-pack.md)


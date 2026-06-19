---
title: Legacy: ITIL dashboard
description: Use this dashboard to view, maintain, and track the tasks and incidents for operating the IT service desk.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-service-management/incident-management/itil-dashboard.html
release: zurich
product: Incident Management
classification: incident-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Legacy: Incident Management Platform Analytics Solutions, Analytics and reporting, Incident Management, IT Service Management]
---

# Legacy: ITIL dashboard

Use this dashboard to view, maintain, and track the tasks and incidents for operating the IT service desk.

**Important:**

Starting in Xanadu release, the ITIL dashboard is deprecated. Users can use [IT Agent dashboard for Service Operations Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/it-agent-dashboard-sow.md) to view, maintain, and track the tasks and incidents for operating the IT service desk.

\[Omitted image "itil-dashboard-updated.png"\] Alt text: ITIL Dashboard

## Access the ITIL dashboard

To access the ITIL dashboard, navigate to **All** &gt; **Self-Service** &gt; **Dashboard**. On the Dashboards Overview, search for ITIL dashboard.

\[Omitted image "itil-dashboard-location.png"\] Alt text: ITIL Dashboard Location

## End user and roles

|End User|Description|Required role|
|--------|-----------|-------------|
|IT Agent|Views, opens, updates, tracks, and closes incidents and tasks for managing customer issues.|itil|
|IT Agent Admin|Can perform all the activities of an IT agent. In addition, the admin can also modify the data and layout.|itil\_admin|

## Data visualizations

The dashboard includes the following visualizations:

|Title|Type|Description|
|-----|----|-----------|
|Critical Tasks|Single score \(\[Omitted image "icon-single-score-report-p.png"\] Alt text: Singe score icon\)|Total number of open critical task records for which **Priority** is set to **1**.|
|Unassigned Tasks|Single score \(\[Omitted image "icon-single-score-report-p.png"\] Alt text: Singe score icon\)|Total number of open tasks that are still not assigned.|
|Tasks assigned to me|Single score \(\[Omitted image "icon-single-score-report-p.png"\] Alt text: Singe score icon\)|Total number of tasks assigned to the logged-user of the dashboard.|
|Active Incidents older than 7 days|Single score \(\[Omitted image "icon-single-score-report-p.png"\] Alt text: Singe score icon\)|Total number of active incidents logged before seven days.|
|Incident SLA Breached|Single score \(\[Omitted image "icon-single-score-report-p.png"\] Alt text: Singe score icon\)|Total number of incidents that exceed its SLA.|
|Incident SLAs at Risk|Single score \(\[Omitted image "icon-single-score-report-p.png"\] Alt text: Singe score icon\)|Total number of active incidents that have not yet exceeded an SLA but have elapsed 75% of the duration of the SLA.|
|My Groups Work|List \(\[Omitted image "icon-list-report-p.png"\] Alt text: List report icon\)|Outstanding work load \(tasks\) of the logged-in user's group.|
|My Work|List \(\[Omitted image "icon-list-report-p.png"\] Alt text: List report icon\)|The logged-in user's outstanding work load \(tasks\).|

**Parent Topic:**[Legacy: Incident Management Platform Analytics Solutions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/incident-management/incident-content-pack.md)


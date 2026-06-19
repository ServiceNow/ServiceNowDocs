---
title: Legacy: Incident Overview dashboard
description: Use this dashboard to view the status of the incidents for planning, prioritizing, and managing customer issues.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-service-management/incident-management/incident-overview-dashboard.html
release: zurich
product: Incident Management
classification: incident-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Legacy: Incident Management Platform Analytics Solutions, Analytics and reporting, Incident Management, IT Service Management]
---

# Legacy: Incident Overview dashboard

Use this dashboard to view the status of the incidents for planning, prioritizing, and managing customer issues.

**Important:**

Starting in Xanadu release, the Incident Overview dashboard is deprecated. Users can use [Incident management dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/incident.md) to view the status of the incidents for planning, prioritizing, and managing customer issues.

\[Omitted image "incident-overview-dashboard.gif"\] Alt text: Incident Overview Dasboard

## Access the Incident Overview dashboard

To access the Incident Overview dashboard, navigate to **All** &gt; **Incident** &gt; **Overview**.

Alternatively, navigate to **All** &gt; **Self-Service** &gt; **Dashboard**. On the Dashboards Overview, search for Incident Overview dashboard.

\[Omitted image "incident-overview-dashboard-location.png"\] Alt text: Incident overview dashboard search on dashboards

## End user and roles

<table id="table_wdd_n2w_gsb"><thead><tr><th>

End user

</th><th>

Description

</th><th>

Required role

</th></tr></thead><tbody><tr><td>

IT Agent

</td><td>

Opens, views, updates, tracks, and closes the incidents for managing customer issues.

</td><td>

-   itil
-   sn\_incident\_read

</td></tr></tbody>
</table>## Data visualizations

The dashboard includes the following visualizations:

|Title|Type|Description|
|-----|----|-----------|
|Incidents Opened Today|Single score \(\[Omitted image "icon-single-score-report-p.png"\] Alt text: Singe score icon\)|Total number of incidents created on the current date.|
|Unassigned Incidents|Single score \(\[Omitted image "icon-single-score-report-p.png"\] Alt text: Singe score icon\)|Total number of incidents that are still not assigned.|
|Overdue Incidents|Single score \(\[Omitted image "icon-single-score-report-p.png"\] Alt text: Singe score icon\)|Total number of incidents that exceed its SLA.|
|Open Incidents|Single score \(\[Omitted image "icon-single-score-report-p.png"\] Alt text: Singe score icon\)|Total number of incidents that do not have a resolution date.|
|Incidents not updated for 7 days|Single score \(\[Omitted image "icon-single-score-report-p.png"\] Alt text: Singe score icon\)|Total number of incidents that were updated more than 7 days ago.|
|Open Incidents older than 30 Days|Single score \(\[Omitted image "icon-single-score-report-p.png"\] Alt text: Singe score icon\)|Total number of open incidents that were created 30 days ago.|
|Open Incidents-Grouped|Vertical bar \(\[Omitted image "icon-bar-report-p.png"\] Alt text: Vertical bar\)|Total number of open incidents grouped by priority.|
|Open Incidents older than 30 Days-Grouped|Horizontal bar \(\[Omitted image "icon-horizontal-bar-report-p.png"\] Alt text: Horizontal bar\)|Total number of open incidents that were created more than 30 days ago.|
|Incidents by Priority and State|Heatmap icon \(\[Omitted image "icon-heatmap-report-p.png"\] Alt text: Heatmap icon\)|Total number of incidents grouped by priority and state.|
|Incidents by Priority and State older than 30 Days|Heatmap icon \(\[Omitted image "icon-heatmap-report-p.png"\] Alt text: Heatmap icon\)|Total number of incidents grouped by priority and state that were created more than 30 days ago.|
|Incidents per week|Area icon \(\[Omitted image "icon-area-report-p.png"\] Alt text: Area icon\)|Total number of incidents opened or closed in each week.|

## Filters

The dashboard includes the following filters:

|Name|Type|Description|
|----|----|-----------|
|Incident Priority|Choice list|Filter the report visualizations based on the **Priority** of the incident record.|
|Incident State|Choice list|Filter the report visualizations based on the **State** of the incident record.|
|Incident Assignment Group|Reference|Filter the report visualizations based on the **Assignment group** associated with the incident record.|
|Incident Category|Choice list|Filter the report visualizations based on the **Category** of the incident record.|
|Incident Opened|Date|Filter the report visualizations based on the date when the incident is created.|

**Note:** This dashboard displays the incident-related information from the **Overview** tab of the Incident Premium dashboard.

**Parent Topic:**[Legacy: Incident Management Platform Analytics Solutions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/incident-management/incident-content-pack.md)


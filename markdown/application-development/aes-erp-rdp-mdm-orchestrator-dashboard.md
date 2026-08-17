---
title: App Engine for ERP MDM Orchestrator dashboard
description: The MDM Orchestrator dashboard provides tailored views of workflows, requests, and actions for each persona: requestor, enricher, and governance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/aes-erp-rdp-mdm-orchestrator-dashboard.html
release: australia
topic_type: reference
last_updated: "2026-06-26"
reading_time_minutes: 2
keywords: [app, engine, erp, sap, rapid, deployment, pack, mdm, orchestrator, dashboard, navigation]
breadcrumb: [Reference, App Engine for ERP rapid deployment packs, Building low-code applications, Developing your application, Building applications]
---

# App Engine for ERP MDM Orchestrator dashboard

The MDM Orchestrator dashboard provides tailored views of workflows, requests, and actions for each persona: requestor, enricher, and governance.

## Requestor view of MDM Orchestrator dashboard

The requestor view of the MDM Orchestrator dashboard provides an overview of submitted requests and an interface to create requests.

|Element|Description|
|-------|-----------|
|Time period picker|Set the time period for dashboard charts, for example, last 30 days or all time.|
|Create New Request|Select to open the **New request** tab and create a request.|
|Key point in time metrics|Individual number charts that display requests that need attention, are active, were completed/approved, and have been submitted in the set time period.|
|Requests Distribution|The count of requests by state \(for example, enrichment review or approved\).|
|Request Type Distribution|Requests categorized by type \(for example, create or activate\) for the set time period.|
|Submission Trend|The number of request submissions for the set time period by date.|
|Recent Updates|The most recently created or updated requests, with current state and key details.|
|Outcome analysis|The number of requests approved, rejected, and in progress, broken down by request type \(for example, create or activate\).|
|New request tab|Create requests for the domains to which you have access.|
|My requests tab|Filterable list of all requests you submitted.|

## Enricher view of MDM Orchestrator dashboard

The enricher view of the MDM Orchestrator dashboard shows in progress and completed enrichment tasks.

|Element|Description|
|-------|-----------|
|SLA Breaches in Next 24 Hours|Enrichment tasks that will exceed the established SLA in the next 24 hours.|
|In-Progress Tasks in This Month|Tasks currently undergoing enrichment.|
|Request Type Overview|Number of requests awaiting enrichment categorized by type \(for example, create or bulk upload\).|
|State Overview|The count of enrichment tasks by state \(for example, open or closed complete\).|
|Task work|The **My Tasks** tab lists enrichment tasks that are in progress. The **Completed Tasks** tab lists enrichment tasks that are done.|
|My Team Recent Requests|All enrichment requests assigned to the enricher, sortable and filterable by type, status, and age.|

## Governance user view of MDM Orchestrator dashboard

The governance user view of the MDM Orchestrator dashboard displays requests awaiting governance review and compliance validation.

|Element|Description|
|-------|-----------|
|SLA Breaches in Next 24 Hours|Governance tasks that will exceed the established SLA in the next 24 hours.|
|In-Progress Tasks in This Month|Tasks currently undergoing governance review.|
|Request Type Overview|Number of requests awaiting governance review categorized by type \(for example, create or bulk upload\).|
|State Overview|The count of governance tasks by state \(for example, open or closed complete\).|
|Task work|The **My Tasks** tab lists governance tasks that are in progress. The **Completed Tasks** tab lists governance tasks that are done.|
|My Team Recent Requests|All governance review tasks assigned to the governance reviewer, sortable and filterable by type, status, and age.|

**Parent Topic:**[App Engine for ERP rapid deployment packs reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/aes-erp-rdp-reference.md)


---
title: App Engine for ERP Approval Hub dashboards
description: The Approval Hub dashboards provide information and metrics about master data, ERP, and journal entry requests sent for approval. Approvers can review and decide on pending requests across all App Engine for ERP rapid deployment packs.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/aes-erp-rdp-approval-hub-dashboards.html
release: australia
topic_type: reference
last_updated: "2026-06-26"
reading_time_minutes: 3
keywords: [app, engine, erp, sap, rapid, deployment, pack, approval, hub]
breadcrumb: [Reference, App Engine for ERP rapid deployment packs, Building low-code applications, Developing your application, Building applications]
---

# App Engine for ERP Approval Hub dashboards

The Approval Hub dashboards provide information and metrics about master data, ERP, and journal entry requests sent for approval. Approvers can review and decide on pending requests across all App Engine for ERP rapid deployment packs.

## Approval Hub MDM dashboard

The Approval Hub MDM dashboard provides an overview of master data requests submitted for approval.

|Element|Description|
|-------|-----------|
|Time period picker|Set the time period for dashboard charts, for example, last 30 days or all time.|
|Key points in time metrics|Individual number charts displaying the total number of approvals assigned to the logged-in user, pending approval requests, approved requests, and rejected approval requests in the set time period.|
|Status Overview|Number of requests in each state \(for example, processed or rejected\) in the set time period.|
|Request Type Distribution|Requests categorized by type \(for example, create or activate\) for the set time period.|
|Approval Trends|The total number of approval requests, along with the number approved and rejected, by date for the set time period.|
|Overall Approval Score|Percentage of requests that were approved categorized by type \(for example, create or activate\) for the set time period. Percentage calculated as number of approved requests multiplied by 100 and divided by the total number of requests for the type.|
|Recent Requests|Most recently created approval requests assigned to the logged-in user that need approval review.|
|Performance Statistics|Metrics including number of approved requests, number of rejected requests, number of pending requests, and the average time to approval. If you set the time picker to any option other than **All Time**, the percentage change is displayed. For example, if the time picker is set to **Last Month**, the percentage change compared to the previous month is displayed, such as `62% decreased from last month`. If **All Time** is set, the lifetime accumulated data is displayed.|

## Approval Hub ERP dashboard

The Approval Hub ERP dashboard provides an overview of ERP requests submitted for approval.

|Element|Description|
|-------|-----------|
|Time period picker|Set the time period for dashboard charts, for example, last 30 days or all time.|
|Key point in time metrics|Individual number charts displaying the total number of ERP syncs, pending sync requests, approved syncs, and rejected approval requests in the set time period.|
|ERP Source Distribution|ERP sync requests categorized by type \(for example, MDM ERP or ERP Message\) for the set time period.|
|ERP Sync Trends|The total number of ERP sync requests, along with the number approved and rejected, by date for the set time period.|
|Approvals Needing Action|Most recently created ERP sync request tasks assigned to any approver that need approval.|

## Approval Hub journal entry dashboard

The Approval Hub JE dashboard provides an overview of journal entry requests submitted for approval.

|Element|Description|
|-------|-----------|
|Time period picker|Set the time period for dashboard charts, for example, last 30 days or all time.|
|Key point in time metrics|Individual number charts displaying the total number of journal entry approvals assigned to the logged in user, pending approval requests, approved requests, and rejected approval requests in the set time period.|
|Status Overview|The number of journal entry approval requests by state \(for example, waiting for approval or processed\).|
|Type Distribution|Journal entry approval requests categorized by type \(for example, cash disburse or expense\) for the set time period.|
|Approval trends|The total number of journal entry approval requests, along with the number approved and rejected, by date for the set time period.|
|Approval Score by Journal Type|Percentage of Journal entry requests approved categorized by type \(for example, adjusting or purchase\) for the set time period. Percentage calculated as number of approved journal entry requests multiplied by 100 and divided by total number of journal entry requests for the type.|
|Recent Actionable|Most recently created journal entry request tasks assigned to any approver that need approval.|

**Parent Topic:**[App Engine for ERP rapid deployment packs reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/aes-erp-rdp-reference.md)


---
title: Campaign fields and states
description: Fields and states for campaigns and campaign cycles, used to define a metric set and track it through collection, approval, and closure.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/environmental-social-governance/campaign-fields-and-states.html
release: australia
topic_type: reference
last_updated: "2026-08-04"
reading_time_minutes: 1
keywords: [campaign fields, campaign states, campaign cycle fields, campaign cycle states]
breadcrumb: [GRC: Metrics reference, GRC: Metrics, Operational Sustainability Management \(formerly Environmental, Social, and Governance\)]
---

# Campaign fields and states

Fields and states for campaigns and campaign cycles, used to define a metric set and track it through collection, approval, and closure.

|Field|Description|
|-----|-----------|
|Name|Name of the campaign.|
|Description|Description of the campaign.|
|Active|Whether the campaign is active.|
|Group|Group of metrics included in the campaign. Locks once the campaign is published.|
|Calendar|Calendar used to determine metric period dates. Locks once the campaign is published.|
|Frequency|How often the campaign runs. Locks once the campaign is published.|
|First run date|Date the first data collection cycle begins. Locks once the campaign is published.|
|Next run date|Date the next data collection cycle begins.|
|Due date offset|Number of days after the period end date when data submission is due.|
|Data owner type|Whether the data owner is a user or a user group.|
|Data owner|User or group that receives all metric data tasks for the campaign.|

|State|Description|
|-----|-----------|
|In progress|The campaign is being set up.|
|Pending publication|The campaign is ready to be published.|
|Published|The campaign is active and generating campaign cycles.|

|Field|Description|
|-----|-----------|
|Name|Name of the campaign cycle.|
|Start date|Start date of the data collection period.|
|End date|End date of the data collection period.|
|Due date|Date data submission is due, calculated from the campaign's due date offset. You can edit this value until the campaign cycle is closed. Changing it updates the due date on every metric data task in the cycle.|

|State|Description|
|-----|-----------|
|Data collection|Data owners are collecting data for the metrics in the campaign cycle.|
|Approval|Metric data tasks in the campaign cycle are awaiting approval.|
|Closed|The campaign cycle is complete.|

**Parent Topic:**[GRC: Metrics reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/environmental-social-governance/grc-metrics-reference.md)


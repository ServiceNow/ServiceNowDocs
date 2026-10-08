---
title: Tables installed with Grants Management
description: This section describes the tables installed with the Grants Management application and shows how they store and manage information.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/government-industry/psds-data-model-gm-tables.html
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [grants management, tables, data model, government services]
breadcrumb: [Grants Management, Data Model, Reference, Public Sector Digital Services \(PSDS\)]
---

# Tables installed with Grants Management

This section describes the tables installed with the Grants Management application and shows how they store and manage information.

## Grants Management tables installed

|Table|Description|Extends Table|
|-----|-----------|-------------|
|Grants Management Case|Contains cases associated with grant management, including application details, review status, and decision outcomes.|Government Service Case|
|Funding Allocation Review Task|Captures the recommendation reason and automatically computes the proposal and funding/decline counts along with the total allocated amount.|Government Service Task|
|Funding Allocation Proposal Mapping|Links individual proposals to a Funding Allocation Review Task. A flag indicates whether the proposal is included in the batch or removed during the review.|None|
|Government Service Case|Contains records of individual cases related to government services, tracking requests, interactions, and resolutions for constituents seeking assistance from government agencies.|Customer Service Case|
|Government Service Task|Contains tasks associated with government service cases, outlining specific actions to be performed, their status, and assigned personnel.|Customer Service Task|
|Constituent Profile|Contains detailed profiles of constituents, including personal information, contact details, and engagement history with government services.|Consumer Profile|
|Business Profile|Contains profiles of businesses interacting with government agencies, documenting registration information, contact details, and service engagements.|None|
|Business Registration Request|Contains information about new business registration requests.|None|
|Government Service Document|Contains information about service-related documents required for government service requests and case management.|Documents|
|Government Service Evaluation Task|Contains information about evaluation tasks for assessing the quality and outcomes of government services provided to constituents.|Government Service Task|

**Parent Topic:**[Public Sector Digital Services Grants Management Data Model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/government-industry/psds-data-model-gm.md)


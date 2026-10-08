---
title: Tables and Flows installed with Public Sector Digital Services Core
description: This section describes the tables and flows installed with the Public Sector Digital Services Core application and shows how they store and manage information.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/government-industry/psds-data-model-core-tables.html
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Core, Data Model, Reference, Public Sector Digital Services \(PSDS\)]
---

# Tables and Flows installed with Public Sector Digital Services Core

This section describes the tables and flows installed with the Public Sector Digital Services Core application and shows how they store and manage information.

## Public Sector Digital Services Core tables installed

|Table|Description|Extends Table|
|-----|-----------|-------------|
|Government Service Case|Contains records of individual cases related to government services, tracking requests, interactions, and resolutions for constituents seeking assistance from government agencies.|Customer Service Case|
|Government Service Task|Contains tasks associated with government service cases, outlining specific actions to be performed, their status, and assigned personnel.|Customer Service Task|
|Constituent Profile|Contains detailed profiles of constituents, including personal information, contact details, and engagement history with government services.|Consumer Profile|
|Business Profile|Contains profiles of businesses interacting with government agencies, documenting registration information, contact details, and service engagements.|None|
|Business Registration Request|Contains information about new business registration requests.|None|
|Government Service Document|Contains information about service documents.|Documents|
|Government Service Evaluation Task|Contains information about service evaluation tasks.|Government Service Task|
|Task Document Verification Task Mapping|Maps case tasks created for document resubmission requests to the specific Document Verification Tasks that initiated them. Enables tracking and association of flagged documents back to the case task that triggered the resubmission request, supporting cases where multiple documents are flagged for different reasons.|None|

## Flows installed

|Flow|Description|
|----|-----------|
|Create blocked by record if Case Task is associated with government case|Creates a blocked by record if the Case Task is associated with a government case.|
|Create blocked by record if Government case needs customer information|Creates a blocked by record if the Government case needs more customer information.|
|Resolve blocked by record if Case Task is closed and associated with Government Case|Removes the blocked by record for the associated Government case if the Government case is resolved.|
|Resolve blocked by record if user information is provided for Government case|Removes the blocked by record if the case task is closed.|

**Parent Topic:**[Public Sector Digital Services Core Data Model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/government-industry/psds-data-model-core.md)


---
title: Tables and Flows installed with Information Request Administration
description: This section describes the tables installed with the Information Request Administration application and shows how they store and manage information.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/government-industry/psds-data-model-ir-playbook-tables.html
release: zurich
topic_type: reference
last_updated: "2025-10-23"
reading_time_minutes: 1
breadcrumb: [Information Request, Data Model, Reference, Public Sector Digital Services \(PSDS\)]
---

# Tables and Flows installed with Information Request Administration

This section describes the tables installed with the Information Request Administration application and shows how they store and manage information.

## Information Request tables installed

|Table|Description|Extends Table|
|-----|-----------|-------------|
|Information Request|Contains records of individual cases related to government services, tracking requests, interactions, and resolutions for constituents seeking assistance from government agencies.|Government Service Case|
|Government Service Case|Contains records of individual cases related to government services, tracking requests, interactions, and resolutions for constituents seeking assistance from government agencies.|Customer Service Case|
|Government Service Task|Contains tasks associated with government service cases, outlining specific actions to be performed, their status, and assigned personnel.|Customer Service Task|
|Constituent Profile|Contains detailed profiles of constituents, including personal information, contact details, and engagement history with government services.|Consumer Profile|
|Business Profile|Contains profiles of businesses interacting with government agencies, documenting registration information, contact details, and service engagements.|N/A|
|Business Registration Request|Contains information about new business registration requests.|N/A|
|Government Service Document|Contains information about service documents.|Documents|
|Government Service Evaluation Task|Contains information about service evaluation tasks.|Government Service Task|

**Parent Topic:**[Public Sector Digital Services Information Request Administration Data Model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/government-industry/psds-data-model-ir-playbook.md)


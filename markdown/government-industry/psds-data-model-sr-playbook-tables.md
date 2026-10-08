---
title: Tables installed with Service Request Playbook
description: This section describes the tables installed with the Service Request Playbook application and shows how they store and manage information.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/government-industry/psds-data-model-sr-playbook-tables.html
release: brazil
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Service Request, Data Model, Reference, Public Sector Digital Services \(PSDS\)]
---

# Tables installed with Service Request Playbook

This section describes the tables installed with the Service Request Playbook application and shows how they store and manage information.

## Service Request tables installed

|Table|Description|Extends Table|
|-----|-----------|-------------|
|Service Request|Contains records of individual cases related to government services, tracking requests, interactions, and resolutions for constituents seeking assistance from government agencies.|Government Service Case|
|Government Service Case|Contains records of individual cases related to government services, tracking requests, interactions, and resolutions for constituents seeking assistance from government agencies.|Customer Service Case|
|Government Service Task|Contains tasks associated with government service cases, outlining specific actions to be performed, their status, and assigned personnel.|Customer Service Task|
|Constituent Profile|Contains detailed profiles of constituents, including personal information, contact details, and engagement history with government services.|Consumer Profile|
|Business Profile|Contains profiles of businesses interacting with government agencies, documenting registration information, contact details, and service engagements.|N/A|
|Business Registration Request|Contains information about new business registration requests.|N/A|
|Government Service Document|Contains information about service documents.|Documents|
|Government Service Evaluation Task|Contains information about service evaluation tasks.|Government Service Task|

**Parent Topic:**[Public Sector Digital Services Service Request Playbook Data Model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/government-industry/psds-data-model-sr-playbook.md)


---
title: Tables installed with Social Benefits Playbook
description: This section describes the tables installed with the Social Benefits Playbook application and shows how they store and manage information.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/government-industry/psds-data-model-sb-playbook-tables.html
release: zurich
topic_type: reference
last_updated: "2025-10-23"
reading_time_minutes: 1
breadcrumb: [Social Benefits, Data Model, Reference, Public Sector Digital Services \(PSDS\)]
---

# Tables installed with Social Benefits Playbook

This section describes the tables installed with the Social Benefits Playbook application and shows how they store and manage information.

## Social Benefits tables installed

|Table|Description|Extends Table|
|-----|-----------|-------------|
|Social Benefits Case|Contains cases involving social benefit applications or claims, capturing information about eligibility, application process, and benefit disbursement.|Government Service Case|
|Government Service Case|Contains records of individual cases related to government services, tracking requests, interactions, and resolutions for constituents seeking assistance from government agencies.|Customer Service Case|
|Government Service Task|Contains tasks associated with government service cases, outlining specific actions to be performed, their status, and assigned personnel.|Customer Service Task|
|Constituent Profile|Contains detailed profiles of constituents, including personal information, contact details, and engagement history with government services.|Consumer Profile|
|Business Profile|Contains profiles of businesses interacting with government agencies, documenting registration information, contact details, and service engagements.|N/A|
|Business Registration Request|Contains information about new business registration requests.|N/A|
|Government Service Document|Contains information about service documents.|Documents|
|Government Service Evaluation Task|Contains information about service evaluation tasks.|Government Service Task|
|Social Benefits Item Received|Tracks individual social benefit items received by constituents, noting benefit type, amount, and date of issuance.|Install Base Item|

**Parent Topic:**[Public Sector Digital Services Social Benefits Data Model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/government-industry/psds-data-model-sb-playbook.md)


---
title: Tables installed with License and Permit Playbook
description: This section describes the tables installed with the License and Permit Playbook application and shows how they store and manage information.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/government-industry/psds-data-model-lp-playbook-tables.html
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [License and Permit, Data Model, Reference, Public Sector Digital Services \(PSDS\)]
---

# Tables installed with License and Permit Playbook

This section describes the tables installed with the License and Permit Playbook application and shows how they store and manage information.

## License and Permit tables installed

|Table|Description|Extends Table|
|-----|-----------|-------------|
|License and Permit Case|Contains cases related to applications for licenses and permits, tracking application status, required documentation, and approval steps.|Government Service Case|
|Government Service Case|Contains records of individual cases related to government services, tracking requests, interactions, and resolutions for constituents seeking assistance from government agencies.|Customer Service Case|
|Government Service Task|Contains tasks associated with government service cases, outlining specific actions to be performed, their status, and assigned personnel.|Customer Service Task|
|Constituent Profile|Contains detailed profiles of constituents, including personal information, contact details, and engagement history with government services.|Consumer Profile|
|Business Profile|Contains profiles of businesses interacting with government agencies, documenting registration information, contact details, and service engagements.|N/A|
|Business Registration Request|Contains information about new business registration requests.|N/A|
|Government Service Document|Contains information about service documents.|Documents|
|Government Service Evaluation Task|Contains information about service evaluation tasks.|Government Service Task|
|License and Permit Item Received|Contains the details of license and permit items that have been issued or received, including item identifiers, issuance dates, and recipient information.|Install Base Item|

**Parent Topic:**[Public Sector Digital Services License and Permit Playbook Data Model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/government-industry/psds-data-model-lp-playbook.md)


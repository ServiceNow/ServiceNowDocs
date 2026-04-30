---
title: Tables and Flows installed with Information Request Playbook
description: This section describes the tables installed with the Information Request Playbook application and shows how they store and manage information.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-10-23"
reading_time_minutes: 1
breadcrumb: [Information Request, Data Model, Reference, Public Sector Digital Services \(PSDS\)]
---

# Tables and Flows installed with Information Request Playbook

This section describes the tables installed with the Information Request Playbook application and shows how they store and manage information.

## Information Request tables installed

<table id="table_fbz_45z_vdb"><thead><tr><th>

Table

</th><th>

Description

</th><th>

Extends Table

</th></tr></thead><tbody><tr><td>

Information Request\[sn\_gsm\_information\_request\_case\]

</td><td>

Contains records of individual cases related to government services, tracking requests, interactions, and resolutions for constituents seeking assistance from government agencies.

</td><td>

Government Service Case \[sn\_gsm\_government\_service\_case\]

</td></tr><tr><td>

Government Service Case\[sn\_gsm\_government\_service\_case\]

</td><td>

Contains records of individual cases related to government services, tracking requests, interactions, and resolutions for constituents seeking assistance from government agencies.

</td><td>

Customer Service Case \(sn\_customerservice\_case\)

</td></tr><tr><td>

Government Service Task \[sn\_gsm\_government\_service\_task\]

</td><td>

Contains tasks associated with government service cases, outlining specific actions to be performed, their status, and assigned personnel.

</td><td>

Customer Service Task \(sn\_customerservice\_task\)

</td></tr><tr><td>

Constituent Profile\[sn\_gsm\_constituent\_profile\]

</td><td>

Contains detailed profiles of constituents, including personal information, contact details, and engagement history with government services.

</td><td>

Consumer Profile \(sn\_csm\_consumer\_profile\)

</td></tr><tr><td>

Business Profile\[sn\_gsm\_business\_profile\]

</td><td>

Contains profiles of businesses interacting with government agencies, documenting registration information, contact details, and service engagements.

</td><td>

N/A

</td></tr><tr><td>

Business Registration Request \[sn\_gsm\_business\_registration\]

</td><td>

Contains information about new business registration requests.

</td><td>

N/A

</td></tr><tr><td>

Government Service Document\[sn\_gsm\_document\]

</td><td>

Contains information about service documents.

</td><td>

Documents \(ds\_document\)

</td></tr><tr><td>

Government Service Evaluation Task\[sn\_gsm\_government\_service\_evaluation\_task\]

</td><td>

Contains information about service evaluation tasks.

</td><td>

Government Service Task \(sn\_gsm\_government\_service\_task\)

</td></tr></tbody>
</table>**Parent Topic:**[Public Sector Digital Services Information Request Playbook Data Model](psds-data-model-ir-playbook.md)


---
title: Tables installed with License and Permit Playbook
description: This section describes the tables installed with the License and Permit Playbook application and shows how they store and manage information.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [License and Permit, Data Model, Reference, Public Sector Digital Services \(PSDS\)]
---

# Tables installed with License and Permit Playbook

This section describes the tables installed with the License and Permit Playbook application and shows how they store and manage information.

## License and Permit tables installed

<table id="table_fbz_45z_vdb"><thead><tr><th>

Table

</th><th>

Description

</th><th>

Extends Table

</th></tr></thead><tbody><tr><td>

License and Permit Case\[sn\_gsm\_license\_permit\_case\]

</td><td>

Contains cases related to applications for licenses and permits, tracking application status, required documentation, and approval steps.

</td><td>

Government Service Case \(sn\_gsm\_government\_service\_case\)

</td></tr><tr><td>

Government Service Case \[sn\_gsm\_government\_service\_case\]

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

</td></tr><tr><td>

License and Permit Item Received\[sn\_gsm\_license\_permit\_install\_base\_item\]

</td><td>

Contains the details of license and permit items that have been issued or received, including item identifiers, issuance dates, and recipient information.

</td><td>

Install Base Item \(sn\_install\_base\_item\)

</td></tr></tbody>
</table>**Parent Topic:**[Public Sector Digital Services License and Permit Playbook Data Model](psds-data-model-lp-playbook.md)


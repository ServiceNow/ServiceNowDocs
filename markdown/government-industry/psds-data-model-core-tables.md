---
title: Tables and Flows installed with Public Sector Digital Services Core
description: This section describes the tables and flows installed with the Public Sector Digital Services Core application and shows how they store and manage information.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-10-23"
reading_time_minutes: 1
breadcrumb: [Core, Data Model, Reference, Public Sector Digital Services \(PSDS\)]
---

# Tables and Flows installed with Public Sector Digital Services Core

This section describes the tables and flows installed with the Public Sector Digital Services Core application and shows how they store and manage information.

## Public Sector Digital Services Core tables installed

<table id="table_fbz_45z_vdb"><thead><tr><th>

Table

</th><th>

Description

</th><th>

Extends Table

</th></tr></thead><tbody><tr><td>

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
</table>## Flows installed

<table id="table_f55_gbp_rsb"><thead><tr><th>

Flow

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Create blocked by record if Case Task is associated with government case\[create\_blocked\_by\_record\_if\_case\_task\_is\_associated\_with\_government\_case\]

</td><td>

Creates a blocked by record if the Case Task is associated with a government case.

</td></tr><tr><td>

Create blocked by record if Government case needs customer information\[create\_blocked\_by\_record\_if\_case\_needs\_customer\_information\]

</td><td>

Creates a blocked by record if the Government case needs more customer information.

</td></tr><tr><td>

Resolve blocked by record if Case Task is closed and associated with Government Case\[resolve\_blocked\_by\_record\_if\_case\_task\_is\_closed\_and\_associated\_with\_government\_case\]

</td><td>

Removes the blocked by record for the associated Government case if the Government case is resolved.

</td></tr><tr><td>

Resolve blocked by record if user information is provided for Government case\[resolve\_blocked\_by\_record\_if\_user\_information\_is\_provided\_for\_govt\_case\]

</td><td>

Removes the blocked by record if the case task is closed.

</td></tr></tbody>
</table>**Parent Topic:**[Public Sector Digital Services Core Data Model](psds-data-model-core.md)


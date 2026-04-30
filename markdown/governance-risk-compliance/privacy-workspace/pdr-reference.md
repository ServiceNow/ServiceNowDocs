---
title: Personal Data Rights reference
description: Reference topics provide additional information such as tables, and roles that are installed with the Personal Data Rights application. These topics also provide supporting information.
locale: en-US
release: zurich
product: Privacy Workspace
classification: privacy-workspace
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Reference, Privacy Management, Governance, Risk, and Compliance]
---

# Personal Data Rights reference

Reference topics provide additional information such as tables, and roles that are installed with the Personal Data Rights application. These topics also provide supporting information.

## Roles installed with Personal Data Rights

<table id="table_plp_xfl_wbc"><thead><tr><th>

Role title

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Personal data rights request admin\[sn\_grc\_pdr.pdr\_admin\]

</td><td>

Users with this role can configure the personal data rights request type

</td><td>

-   sn\_grc\_case\_mgmt.grc\_case\_admin
-   sn\_grc\_pdr.pdr\_manager

</td></tr><tr><td>

Personal data rights request agent\[sn\_grc\_pdr.pdr\_agent\]

</td><td>

Users with this role work on the personal data rights request assigned to them.

</td><td>

-   sn\_grc\_pdr.data\_owner\_admin
-   sn\_grc\_case\_mgmt.grc\_case\_analyst

</td></tr><tr><td>

Personal data owner admin\[sn\_grc\_pdr.data\_owner\_admin\]

</td><td>

Users with this role are the asset owners who respond on action tasks when their assets are involved in a request.

</td><td>

-   sn\_grc\_workspace.task\_reader
-   sn\_grc\_workspace.user

</td></tr><tr><td>

Personal data request manager\[sn\_grc\_pdr.pdr\_manager\]

</td><td>

Users with this role oversee all personal data rights request until they are closed.

</td><td>

-   sn\_grc\_case\_mgmt.grc\_case\_manager
-   sn\_grc\_pdr.pdr\_agent

</td></tr><tr><td>

PDR Requester\[sn\_grc\_pdr.pdr\_requester\]

</td><td>

Users with this role can submit new PDRs, track the status of their requests, and receive communications or notifications related to their requests.

</td><td>

 

</td></tr></tbody>
</table>## Tables installed with Personal Data Rights

<table id="table_x2j_qgl_wbc"><thead><tr><th>

Table name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Data owner registrysn\_grc\_pdr\_data\_owner\_registry

</td><td>

Maintains a mapping between data assets and their owners.

</td></tr><tr><td>

Personal data rights request sn\_grc\_pdr\_request

</td><td>

Collects information with respect to personal data rights.

</td></tr></tbody>
</table>For information about feature roles, see .

**Parent Topic:**[Privacy Management reference](privacy-mgmt-reference.md)


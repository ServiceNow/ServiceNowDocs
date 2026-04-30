---
title: Roles and tables installed with Regulatory Agency Library
description: Several types of components are installed with activation of the Regulatory Agency Library application, including tables and user roles.
locale: en-US
release: xanadu
product: Regulatory Change Management Service Portal
classification: regulatory-change-management-service-portal
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Reference, Regulatory Change Management, Governance, Risk, and Compliance]
---

# Roles and tables installed with Regulatory Agency Library

Several types of components are installed with activation of the Regulatory Agency Library application, including tables and user roles.

## Roles installed with Regulatory Agency Library

<table id="table_k34_p54_rbc"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Regulatory Agency Library Reader \[sn\_reg\_body\_mgmt.reader\]

</td><td>

Contains the reader role in sn\_reg\_body\_mgmt scopes, and the reader role in Compliance Workspace. In addition to the inherited permissions, the regulatory body library management reader can access and read regulatory agencies, regulatory contacts, and jurisdictions.

</td><td>

-   sn\_compliance.reader
-   sn\_grc.reader

</td></tr><tr><td>

Regulatory Agency Library Writer \[sn\_reg\_body\_mgmt.writer\]

</td><td>

Contains the reader, user, and manager roles in sn\_reg\_body\_mgmt scopes, and the reader and user roles in Compliance Workspace. In addition to the inherited permissions, the regulatory body library management writer can update and delete regulatory agencies, regulatory contacts, and jurisdictions.

</td><td>

-   sn\_reg\_body\_mgmt.reader
-   sn\_compliance.user
-   sn\_grc\_case\_mgmt.grc\_​case\_manager
-   sn\_compliance.manager
-   sn\_compliance\_ws.corporate\_compliance\_analyst
-   sn\_grc.manager

</td></tr></tbody>
</table>## Tables installed with Regulatory Agency Library

<table id="table_epm_5y4_rbc"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Regulatory Agency \[sn\_reg\_body\_mgmt\_regulatory\_agency\]

</td><td>

Stores regulatory agencies that enforce various types of regulations.

</td></tr><tr><td>

Regulatory Contact \[sn\_reg\_body\_mgmt\_regulatory\_contact\]

</td><td>

Stores regulatory contacts who will be notified upon changes to compliance case or a regulatory change in Regulatory Agency Library.

</td></tr><tr><td>

Regulatory Agency to jurisdiction \[sn\_reg\_body\_mgmt\_m2m\_reg\_agency\_jurisdiction\]

</td><td>

Stores jurisdiction records for regulatory agency association in Regulatory Agency Library.

</td></tr><tr><td>

Jurisdiction \[sn\_reg\_body\_mgmt\_jurisdiction\]

</td><td>

Stores jurisdiction records in Regulatory Agency Library.

</td></tr><tr><td>

Auto Date Calculation \[sn\_reg\_body\_mgmt\_auto\_date\_calculation\]

</td><td>

Stores auto date calculations for future dates in Regulatory Agency Library.

</td></tr><tr><td>

Agency Profile \[sn\_reg\_body\_mgmt\_agency\_profile\]

</td><td>

Stores regulatory agency profiles in Regulatory Agency Library.

</td></tr></tbody>
</table>**Parent Topic:**[Regulatory Change Management reference](rcm-reference.md)


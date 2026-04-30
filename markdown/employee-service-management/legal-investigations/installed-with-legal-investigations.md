---
title: Components installed with Legal Investigations
description: Several types of components are installed with activation of the Legal Investigations application, including tables, user roles, and scheduled jobs.
locale: en-US
release: zurich
product: Legal Investigations
classification: legal-investigations
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Reference, Legal Investigations, Legal Service Delivery Practice Applications, Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Components installed with Legal Investigations

Several types of components are installed with activation of the Legal Investigations application, including tables, user roles, and scheduled jobs.

## Roles

<table id="table_u1t_gb1_wdb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Investigations Administrator\[sn\_lg\_investigate.admin\]

</td><td>

Application-specific administrator role for the Legal Investigations app having the administrative access for the app and full access to the underlying data.

</td><td>

-   sn\_lg\_investigate.config
-   sn\_lg\_investigate.fulfiller
-   sn\_interview\_temp.admin

</td></tr><tr><td>

Investigations Configurator\[sn\_lg\_investigate.config\]

</td><td>

Provides access to configure data such as allegation type and subtype. It does not provide access to transactional data of requests and matters.

</td><td>

sn\_interview\_temp.writer

</td></tr><tr><td>

Investigations Fulfiller\[sn\_lg\_investigate.fulfiller\]

</td><td>

Provides the fulfiller access for working on assigned requests and matters.

</td><td>

-   sn\_lg\_ops.legal\_user
-   sn\_interview\_temp.reader

</td></tr></tbody>
</table>## Tables

<table id="table_xfk_nzq_f5b"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Allegation

 \[sn\_lg\_investigate\_allegation\]

</td><td>

Allegations complained on a person, also known as the subject of allegation.

</td></tr><tr><td>

Allegation Type

 \[sn\_lg\_investigate\_allegation\_type\]

</td><td>

Type of allegation used to file a complaint, such as financial fraud, discrimination, and harassment.

</td></tr><tr><td>

Allegation Subtype

 \[sn\_lg\_investigate\_allegation\_subtype\]

</td><td>

Subtype used to further classify an allegation type. For example, financial fraud can have subtypes such as undue favours or bribes.

</td></tr><tr><td>

Involved Party

 \[sn\_lg\_investigate\_involved\_party\]

</td><td>

Users who are involved in a complaint as a complainant, subject of allegation, witness, or any other type.

</td></tr><tr><td>

Associated Allegation

 \[sn\_lg\_investigate\_m2m\_allegation\_party\]

</td><td>

Association between an allegation and its subjects of allegation. One allegation can be associated with one or more subjects of allegation.

</td></tr></tbody>
</table>**Parent Topic:**[Legal Investigations reference](legal-investigations-reference.md)


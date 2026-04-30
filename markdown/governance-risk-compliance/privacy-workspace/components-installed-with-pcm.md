---
title: Components installed with Privacy Case Management
description: Several types of components are installed with installation of the Privacy Case Management application, including tables, user roles.
locale: en-US
release: yokohama
product: Privacy Workspace
classification: privacy-workspace
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Reference, Privacy Case Management, Privacy Management, Governance, Risk, and Compliance]
---

# Components installed with Privacy Case Management

Several types of components are installed with installation of the Privacy Case Management application, including tables, user roles.

## Roles installed

Privacy Case Management roles.

<table id="table_wch_3p5_mwb"><thead><tr><th>

Role

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Privacy case business user\[sn\_privacy\_case.privacy\_case\_business\_user\]

</td><td>

To create a Privacy case from Employee center.

</td><td>

sn\_grc\_case\_mgmt.grc\_case\_business\_user

</td></tr><tr><td>

Privacy case analyst \[sn\_privacy\_case.privacy\_case\_analyst\]

</td><td>

Work on the privacy case assigned to them. As part of investigating privacy cases, they can review the breach assessment and associate the Information objects, key stakeholders Impacted areas, related areas, Causes and Consequences, Regulations and Issues which are assigned to them.

</td><td>

sn\_privacy\_case.privacy\_case\_analyst, sn\_grc\_case\_mgmt.grc\_case\_manager

</td></tr><tr><td>

Privacy case manager \[sn\_privacy\_case.privacy\_case\_manager\]

</td><td>

Privacy cases can be classified into multiple groups and for every group there can be a manager. A privacy case manager can assign or reassign privacy cases to privacy analysts who are part of the same group. Privacy case manager has the same access as that of the privacy analyst.

</td><td>

sn\_privacy\_case.privacy\_case\_analyst, sn\_grc\_case\_mgmt.grc\_case\_manager

</td></tr><tr><td>

Privacy case admin \[sn\_privacy\_case.privacy\_case\_admin\]

</td><td>

Configure the privacy case type that has configurations such as privacy workflow configurations, assignment rules, sub types, assessment templates. They can also configure breach assessment configurations.

</td><td>

sn\_grc\_case\_mgmt.grc\_case\_admin, sn\_privacy\_case.privacy\_case\_manager

</td></tr></tbody>
</table>## Tables installed

<table id="table_yrn_st5_mwb"><thead><tr><th>

Table

</th><th>

Description

</th><th>

Application

</th></tr></thead><tbody><tr><td>

GRC case \(sn\_grc\_case\_mgmt\_case\)

</td><td>

Stores all the case details.

</td><td>

GRC: Core Case Management

</td></tr><tr><td>

Case classification \(sn\_grc\_case\_mgmt\_case\_classification\)

</td><td>

Stores the case classifications.

</td><td>

GRC: Core Case Management

</td></tr><tr><td>

Case task \(sn\_grc\_case\_mgmt\_case\_task\)

</td><td>

Stores all the case tasks created on for the Privacy cases.

</td><td>

GRC: Core Case Management

</td></tr><tr><td>

Case type \(sn\_grc\_case\_mgmt\_case\_type\)

</td><td>

Stores the case type and case subtype details.

</td><td>

GRC: Core Case Management

</td></tr><tr><td>

Cause sn\_grc\_case\_mgmt\_cause

</td><td>

Stores the causes added to the library and mapped at the case level.

</td><td>

GRC: Core Case Management

</td></tr><tr><td>

Cause and consequence sn\_grc\_case\_mgmt\_cause\_consequence

</td><td>

Stores the causes and consequences mapped at the case level.

</td><td>

GRC: Core Case Management

</td></tr><tr><td>

Consequencesn\_grc\_case\_mgmt\_consequence

</td><td>

Stores the Consequences added to the library and mapped at the Case level.

</td><td>

GRC: Core Case Management

</td></tr><tr><td>

GRC core case sn\_grc\_case\_mgmt\_core\_case

</td><td>

Stores the details of core functionality of the Case.

</td><td>

GRC: Core Case Management

</td></tr><tr><td>

Impacted area sn\_grc\_case\_mgmt\_impacted\_area

</td><td>

Stores the impacted areas mapped at the Case level.

</td><td>

GRC: Core Case Management

</td></tr><tr><td>

Case Task to Assessment Instance sn\_grc\_case\_mgmt\_m2m\_case\_task\_asmt\_instance

</td><td>

Stores Assessment details on Case tasks of type assessment.

</td><td>

GRC: Core Case Management

</td></tr><tr><td>

Issue to Case sn\_grc\_case\_mgmt\_m2m\_issue\_case

</td><td>

Stores the issues mapped to the Case record.

</td><td>

GRC: Core Case Management

</td></tr><tr><td>

Regulation sn\_grc\_case\_mgmt\_regulation

</td><td>

Stores the regulations mapped at the Case level.

</td><td>

GRC: Core Case Management

</td></tr><tr><td>

Related area sn\_grc\_case\_mgmt\_related\_area

</td><td>

Stores the related areas associated with the Case.

</td><td>

GRC: Core Case Management

</td></tr><tr><td>

Privacy case sn\_privacy\_case\_privacy\_case

</td><td>

Stores Privacy case records.

</td><td>

Privacy Case Management

</td></tr><tr><td>

Information object to privacy case sn\_privacy\_case\_m2m\_information\_object\_to\_case

</td><td>

Stores the Information object records mapped at Case level.

</td><td>

Privacy Case Management

</td></tr><tr><td>

Key stakeholders to case sn\_privacy\_case\_m2m\_key\_stake\_holders\_to\_case

</td><td>

Stores the Key stakeholders record mapped at Case level.

</td><td>

Privacy Case Management

</td></tr></tbody>
</table>**Parent Topic:**[Privacy Case Management reference information](pcm-reference-information.md)


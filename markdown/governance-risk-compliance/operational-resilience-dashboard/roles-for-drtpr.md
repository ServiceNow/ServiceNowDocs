---
title: Roles installed with Digital resilience third-party registers
description: Specific roles are installed with Digital resilience third-party registers.
locale: en-US
release: zurich
product: Operational Resilience Dashboard
classification: operational-resilience-dashboard
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Digital resilience third-party registers reference, Reference, Operational Resilience, Governance, Risk, and Compliance]
---

# Roles installed with Digital resilience third-party registers

Specific roles are installed with Digital resilience third-party registers.

## Roles installed with Digital resilience third-party registers

<table id="table_g5z_5r3_cdc"><thead><tr><th>

Role

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

DORA Accelerator Administrator \[sn\_dora\_accel.admin\]

</td><td>

Role that has full control over all DORA accelerator data, including data in DORA accelerator choice table.

</td><td>

sn\_dora\_accel.manager

</td></tr><tr><td>

DORA Accelerator Manager \[sn\_dora\_accel.manager\]

</td><td>

Role to create, update, and delete most DORA accelerator data, except data in DORA accelerator choice table. They can create and update \[ast\_contract\] and \[core\_company\] data.

</td><td>

-   sn\_dora\_accel.user
-   contract\_manager
-   vendor\_editor

</td></tr><tr><td>

DORA Accelerator User \[sn\_dora\_accel.user\]

</td><td>

Role to view most DORA accelerator data, except data in DORA accelerator choice table. They can view \[ast\_contract\] and \[core\_company\] data.

</td><td>

vendor\_reader

</td></tr><tr><td class="sub-head" colspan="3">

TPRM roles

</td></tr><tr><td>

TPR assessor \(Third-party risk assessor\) \[sn\_vdr\_risk\_asmt.vendor\_assessor\]

</td><td>

Role that includes all permissions of the Third-party assessment reviewer role including managing third parties, third-party contacts, external risk assessments, and issues.

</td><td>

-   sn\_grc.user
-   sn\_grc.reader
-   sn\_vdr\_risk\_asmt.vendor\_assessment\_reviewer
-   sn\_dora\_accel.manager
-   vendor\_editor
-   vendor\_reader

</td></tr><tr><td>

TPR assessment approver \[sn\_vdr\_risk\_asmt.approver\]

</td><td>

Role to approve the third-party risk management.

</td><td>

-   sn\_vdr\_risk\_asmt.vendor\_assessment\_reviewer
-   sn\_dora\_accel.manager

</td></tr><tr><td>

TPR Contract Negotiator \[sn\_vdr\_risk\_asmt.contract\_negotiator\]

</td><td>

Role to work in the contracting stage of the onboarding process.

</td><td>

sn\_vdr\_risk\_asmt.vendor\_assessor

</td></tr><tr><td>

TPR Assessment Reviewer \[sn\_vdr\_risk\_asmt.vendor\_assessment\_reviewer\]

</td><td>

Role to review and edit assessments.

</td><td>

-   vendor\_reader
-   task\_editor
-   template\_editor\_global
-   survey\_reader
-   sn\_dora\_accel.user
-   sn\_grc.reader
-   sn\_grc.business\_user

</td></tr><tr><td>

TPR Administrator \[sn\_vdr\_risk\_asmt.vendor\_risk\_admin\]

</td><td>

Role that has full control over all Vendor Risk Management data. The role also has full control over Assessment Metric Types.

</td><td>

-   assessment\_admin
-   sn\_grc\_appr.admin
-   sn\_vdr\_risk\_asmt.vendor\_risk\_manager
-   sn\_dora\_accel.admin

</td></tr><tr><td>

TPR Manager \[sn\_vdr\_risk\_asmt.vendor\_risk\_manager\]

</td><td>

Role to manage third parties, third-party contacts, third-party assessment templates, questionnaire templates, documentation request templates, and scheduled assessments.

</td><td>

-   sn\_vdr\_risk\_asmt.vendor\_assessment\_reviewer
-   sn\_dora\_accel.manager
-   sn\_data\_registry.admin
-   sn\_vdr\_risk\_asmt.vendor\_assessor

</td></tr></tbody>
</table>**Parent Topic:**[Digital resilience third-party registers reference](digi-resi-ref.md)


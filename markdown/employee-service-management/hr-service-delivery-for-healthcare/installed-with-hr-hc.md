---
title: Installed with HR Service Delivery for Healthcare
description: Several types of components are installed with activation of the HR Service Delivery for Healthcare plugin, including tables and user roles.
locale: en-US
release: australia
product: HR Service Delivery for Healthcare
classification: hr-service-delivery-for-healthcare
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [HR Service Delivery for Healthcare reference, HR Service Delivery for Healthcare, HR Service Delivery, Employee Service Management]
---

# Installed with HR Service Delivery for Healthcare

Several types of components are installed with activation of the HR Service Delivery for Healthcare plugin, including tables and user roles.

## Roles

<table id="table_rg3_rrj_jbc"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Professional Admin

 \[sn\_hc\_professional.admin\]

</td><td>

-   Can create, edit, and delete healthcare professional profile.
-   Can customize the healthcare onboarding journey.
-   Can edit the payroll enrollment records details.

</td><td>

-   sn\_hc\_professional.payer\_writer
-   sn\_hc\_professional.profile\_writer

</td></tr><tr><td>

Professional Payer Reader\[sn\_hc\_professional.payer\_reader\]

</td><td>

Can view payroll enrollment record details.

</td><td>

None

</td></tr><tr><td>

Professional Payer Writer\[sn\_hc\_professional.payer\_writer\]

</td><td>

Can edit payroll enrollment record details.

</td><td>

sn\_hc\_professional.payer\_reader

</td></tr><tr><td>

Professional Profile Reader\[sn\_hc\_professional.profile\_reader\]

</td><td>

Can view healthcare professional profile.

</td><td>

None

</td></tr><tr><td>

Professional Profile Writer\[sn\_hc\_professional.profile\_writer\]

</td><td>

Can edit healthcare professional profile.

</td><td>

sn\_hc\_professional.profile\_reader

</td></tr></tbody>
</table>## Tables

<table id="table_vg3_rrj_jbc"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Hospital Affiliation

 \[sn\_hc\_professional\_hospital\_affiliation\]

</td><td>

Stores the healthcare professional details related to hospital affiliations.

</td></tr><tr><td>

Payers enrollment\[sn\_hc\_professional\_payers\_enrollment\]

</td><td>

Stores the healthcare professional details related to payer enrollments.

</td></tr></tbody>
</table>**Parent Topic:**[HR Service Delivery for Healthcare reference](reference-hr-healthcare.md)

**Related topics**  


[Healthcare professional profile form](hr-service-healthcare.md)

[Professional ID form](hc-professional-profile.md)

[Professional liability Insurances form](hr-prof-liab.md)

[Professional reference form](hr-professional-ref.md)

[Professional speciality form](hc-prof-spec.md)

[Malpractice history form](hr-mal-his.md)

[Education and Training form](hr-edu-tra.md)

[Practice location form](hr-prac-loc.md)

[Employment history form](hr-emp-det.md)

[Languages Spoken form](hr-emp-lan.md)

[Hospital Affiliations form](hr-hos-aff.md)

[Payers Enrollment form](hr-payer-en.md)

[Healthcare Employee Onboarding form](hr-emp-onboarding.md)


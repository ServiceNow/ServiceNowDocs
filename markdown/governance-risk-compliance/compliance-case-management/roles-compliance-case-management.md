---
title: Roles installed with Compliance Case Management
description: The GRC: Compliance Case Management installs the essential role to perform respective day-to-day operational tasks towards managing compliance cases for the enterprise to perform their respective tasks.
locale: en-US
release: yokohama
product: Compliance Case Management
classification: compliance-case-management
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Compliance Case Management reference, Compliance Case Management, Governance, Risk, and Compliance]
---

# Roles installed with Compliance Case Management

The GRC: Compliance Case Management installs the essential role to perform respective day-to-day operational tasks towards managing compliance cases for the enterprise to perform their respective tasks.

<table id="table_m2t_czq_mqb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Compliance Case Business User

 \[sn\_comp\_case.compliance​\_case\_business\_user\]

</td><td>

The compliance case business user can perform the following tasks:-   Create compliance cases and requests from the Employee Center
-   Work on the case tasks.

.

</td><td>

sn\_grc\_case\_mgmt.grc\_​case\_business\_user ​

</td></tr><tr><td>

Compliance Case Analyst

 \[sn\_comp\_case.compliance\_​case\_analyst\]

</td><td>

Compliance case analyst can review the case. The compliance case analyst can perform the following tasks:-   Review the key stakeholders, impacted areas, related areas, causes and consequences, regulations, and issues that are assigned to the case analyst.
-   Review any unassigned cases.

​

</td><td>

-   sn\_grc\_case\_mgmt.grc\_​case\_analyst
-   sn\_comp\_case.compliance​\_case\_business\_user

​

</td></tr><tr><td>

Compliance Case Manager

 \[sn\_comp\_case.compliance\_​case\_manager\]

</td><td>

Compliance case manager can review and work on the created cases. The compliance case manager can perform the following tasks:-   Review the key stakeholders, impacted areas, related areas, causes and consequences, regulations, and issues that are assigned to the case analyst.
-   Review all cases.

​

</td><td>

-   sn\_comp\_case.compliance​\_case\_analyst
-   sn\_grc\_case\_mgmt.grc\_​case\_manager

​

</td></tr><tr><td>

Compliance Case Admin

 \[sn\_comp\_case.compliance\_​case\_admin\]

</td><td>

Compliance case administrators can configure the Compliance Case Management application. They can perform the following tasks:-   Create a case type.
-   Create a state model and transitions.
-   Create an assessment template.
-   Delete cases.
-   Review the key stakeholders, impacted areas, related areas, causes and consequences, regulations, and issues that are assigned to the case analyst.

</td><td>

-   sn\_grc\_case\_mgmt.grc\_​case\_admin
-   sn\_comp\_case.compliance​\_case\_manager

 **Note:** If you use the Smart Assessment Engine for assessments of action tasks, then the following roles are granted to the Compliance case admin.

-   sn\_risk\_advanced.ara\_assessor
-   sn\_smart\_asmt.assessment\_admin
-   sn\_grc.business\_user

</td></tr><tr><td>

GRC Employee User

 \[sn\_grc\_emp\_user.grc​\_employee\]

</td><td>

GRC employee users can ​create compliance cases and requests from the Employee Center.

</td><td>

NA

</td></tr></tbody>
</table>For more information, see [https://www.servicenow.com/products/employee-center.html](https://www.servicenow.com/products/employee-center.html).

**Parent Topic:**[Compliance Case Management reference](reference-data-compliance-case-management.md)


---
title: Create an auditable unit
description: Create auditable units with entities such as business units, departments, vendors, products, business processes, business applications, locations, authority documents, and policies to perform risk assessments on the auditable units.
locale: en-US
release: zurich
product: Audit Management
classification: audit-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Audit Plan Overview, Use, Audit Management, Governance, Risk, and Compliance]
---

# Create an auditable unit

Create auditable units with entities such as business units, departments, vendors, products, business processes, business applications, locations, authority documents, and policies to perform risk assessments on the auditable units.

## Before you begin

Role required: sn\_audit.user or sn\_audit.manager

Activate the GRC Advanced Audit plugin \(com.sn\_audit\_advanced\).

## About this task

You can create an auditable unit and decide the type of risk assessment you want to perform on the auditable unit. After the risk assessment is done, based on the risk ratings, the audit managers can decide if they want to audit the entities. You can scope an auditable unit as an entity on an engagement.

## Procedure

1.  Navigate to **All** &gt; **Audit Universe** &gt; **All Auditable Units**.

2.  Click **New**.

3.  On the form, fill in the fields.

<table id="table_r2w_hbm_5mb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Unique number of the auditable unit.

</td></tr><tr><td>

Name

</td><td>

Name of the auditable unit. For example, Accounts Payable - Finance.

</td></tr><tr><td>

Owning group

</td><td>

Group that owns the auditable unit.

</td></tr><tr><td>

Owner

</td><td>

Owner of the auditable unit.

</td></tr><tr><td>

State

</td><td>

State of auditable unit. The default state is **Draft**.

</td></tr><tr><td>

Priority

</td><td>

Priority of the auditable unit.

</td></tr><tr><td>

Description

</td><td>

Brief description of the auditable units.

</td></tr><tr><td class="sub-head" colspan="2">

Risk Assessment

</td></tr><tr><td>

Method

</td><td>

Type of risk assessment to obtain the risk rating of the auditable unit. The choices are:-   Basic Risk Assessment. This option allows you to manually enter a value for the risk rating.
-   Detailed Risk Assessment. This option appears when the Advanced Audit plugin is activated. When you select this option, the Risk Assessments related list appears.


</td></tr><tr><td>

Risk rating

</td><td>

Risk rating of the auditable unit obtained from a basic risk assessment. This field appears if the **Method** field has **Basic Risk Assessment**.

</td></tr><tr><td>

Inherent risk rating

</td><td>

Inherent risk score. The value in this field is derived from advanced risk assessment. This field appears if the **Method** field has **Detailed Risk Assessment**.

</td></tr><tr><td>

Control effectiveness

</td><td>

Control effectiveness score. The value in this field is derived from advanced risk assessment. This field appears if the **Method** field has **Detailed Risk Assessment**.

</td></tr><tr><td>

Residual risk rating

</td><td>

Residual risk score. The value in this field is derived from advanced risk assessment. This field appears if the **Method** field has **Detailed Risk Assessment**.

</td></tr></tbody>
</table>4.  If you have selected **Basic Risk Assessment** in the **Method** field, click **Submit**.

5.  If you have selected **Detailed Risk Assessment** in the **Method** field, click **Assess Risk**.

    1.  In the **Assessor** field, select an assessor for the risk assessment.

    2.  In the **Approver** field, select an approver for the assessment.

    3.  Click **Submit**.

    A risk assessment instance link is created at the top left and the assessor gets a notification to perform the risk assessment. After the detailed risk assessment is performed, the Risk Assessments related list shows the assessment.

6.  Click the following available related lists, and add entities to them as required.

    -   Business Units
    -   Departments
    -   Vendors
    -   Products
    -   Business Processes
    -   Business Applications
    -   Locations
    -   Authority Documents
    -   Policies


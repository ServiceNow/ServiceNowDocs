---
title: Create an auditable unit and scope entities at risk
description: Create auditable units to identify business entities that can possibly be at risk and scope them into audits.
locale: en-US
release: zurich
product: Audit Management
classification: audit-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Audit Supervisor Workspace, Audit Workspace, Audit Management, Governance, Risk, and Compliance]
---

# Create an auditable unit and scope entities at risk

Create auditable units to identify business entities that can possibly be at risk and scope them into audits.

## Before you begin

Role required: sn\_audit.manager, sn\_audit\_ws.supervisor, sn\_audit.user, sn\_audit\_ws.auditor

## About this task

Auditable units are a combination of different entities such as business units, products or services, legal entities, regulatory required audits, processes, programs, systems, policies, regulation, financial statements, and others.

After you determine the nature and scope of the auditable units, your goal is to perform risk assessments, and scope auditable units and entities based on the risk rating.

See also [Perform advanced risk assessment in the Risk workspace](../../grc-workspace-risk/task/perform-ara-workspace.md).

## Procedure

1.  Navigate to **All** &gt; **Audit** &gt; **Audit Workspace**.

2.  Click **Create** and select **Auditable unit** from the **Home** page.

    You can also create an auditable unit by navigating to the Audit workspace List page.

    1.  Click the lists icon \(![List icon.](../image/ListsIcon.jpg)\).
    2.  Click **All auditable units** or **My auditable units** in the Scoping list.
    3.  Click **New**.
3.  On the form, fill in the fields.

<table id="table_m54_5g2_mqb"><thead><tr><th>

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

Name of the auditable unit. For example, Accounts Payable – Finance.

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

Brief description of the auditable unit.

</td></tr><tr><td class="sub-head" colspan="2">

Assignment

</td></tr><tr><td>

Owning group

</td><td>

Group that owns the auditable unit.

</td></tr><tr><td>

Owner

</td><td>

Owner of the auditable unit.

</td></tr><tr><td class="sub-head" colspan="2">

Risk assessment

</td></tr><tr><td>

Method

</td><td>

Type of risk assessment to obtain the risk rating of the auditable unit. The choices are:-   Basic Risk Assessment: Allows you to manually enter a value for the risk rating.
-   Detailed Risk Assessment: Appears when the Advanced Audit plugin is activated. When you select this option, the Risk Assessments related list appears.


</td></tr><tr><td>

Risk rating

</td><td>

Risk rating of the auditable unit obtained from a basic risk assessment.

</td></tr><tr><td>

Inherent risk rating

</td><td>

Inherent risk score. The value in this field is derived from advanced risk assessment. This field appears if the risk assessment method is **Detailed Risk Assessment**.

</td></tr><tr><td>

Control effectiveness

</td><td>

Control effectiveness score. The value in this field is derived from advanced risk assessment. This field appears if the **Method** field has **Detailed Risk Assessment**.

</td></tr><tr><td>

Residual risk rating

</td><td>

Residual risk score. The value in this field is derived from advanced risk assessment. This field appears if the **Method** field has **Detailed Risk Assessment**.

</td></tr></tbody>
</table>4.  Click **Save**.

5.  To add entities such as business units, department, vendors, products, business processes, and others to the auditable unit, click the respective related list in the Details page.

6.  Select the records from the respective pop-up.

7.  Click **Add**.

8.  Click **Activate**.

    The state of the auditable unit becomes Active.

9.  To retire the auditable unit, click the **Retire** button in the more actions icon \(![More actions icon.](../image/MoreActionsIcon.jpg)\)

10. If you have GRC: Advanced Risk application installed and if you have selected Risk Assessment Method as **Detailed Risk Assessment**, then you can assess risk by clicking the **Assess risk** button.

    For more information, see risk assessment method in [Create an auditable unit](../../grc-audit/task/create-auditable-unit.md#table_r2w_hbm_5mb).



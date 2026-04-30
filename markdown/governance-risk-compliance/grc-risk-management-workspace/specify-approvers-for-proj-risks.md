---
title: Configure Project Portfolio Management and Advanced Risk integration
description: Use the Project Integration Configuration form to set up the risk assessment. You have to select the risk assessment methodology, the right assessors and approvers, and the formula to roll up the risk scores and show the scores at a project level.
locale: en-US
release: yokohama
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Project Risk Assessment using Advanced Risk Assessment, Integrate, Risk Management, Governance, Risk, and Compliance]
---

# Configure Project Portfolio Management and Advanced Risk integration

Use the Project Integration Configuration form to set up the risk assessment. You have to select the risk assessment methodology, the right assessors and approvers, and the formula to roll up the risk scores and show the scores at a project level.

## Before you begin

To use Advanced Risk Assessment for Project Management, do the following:

-   Activate the Project Portfolio Management plugin.
-   Activate the Advanced Risk plugin.
-   Enable the **Enable Advanced Risk PPM Integration** property under **Advanced Risk Assessment** &gt; **Administration** &gt; **Properties**. This property is automatically set to **No** by default. Only users with the it\_pps\_admin or sn\_ risk.admin roles can enable this property..

**Note:** Currently, in the Project Portfolio Management suite, advanced risk assessments are only supported for the Project Management application.

Role required: sn\_risk.admin

## About this task

As the risk administrator, you can select the following on the Project Integration Configurations form:

-   The risk assessment methodology \(RAM\).
-   The approvers and assessors for both enterprise risk assessment and project risk assessment.

Two predefined RAMs are provided for Enterprise Risk Assessment and Project Risk Assessment. You can modify the default methodology or create methodologies. If you select your own risk assessment methodology, then the entity class for that methodology must be Project. For assessing project risks and enterprise risks, you can add the approvers and assessors of your choice. The risk assessment methodology for project risk is automatically selected as the methodology that is associated to the Project Portfolio Management risk table.

## Procedure

1.  Navigate to **All** &gt; **Advanced Risk Assessment** &gt; **Administration** &gt; **Project Integration Configuration**.

2.  Click the information ![Information icon.](../image/icon-information.png) icon to view the project risk integration configuration record.

3.  Click **Open Record**.

4.  On the form, fill in the fields.

<table id="table_l41_lrz_4mb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Project Risk Assessment

</td></tr><tr><td>

Assessment methodology

</td><td>

The assessment methodology for project risk assessment. This field is automatically set to **Enterprise Assessment for Projects**

</td></tr><tr><td>

Assessor type

</td><td>

Assessor for the project risk assessment. The choices are as follows:-   Project Manager: The user assigned as the project manager of the project.
-   Risk Owner: The user who is identified in the**Assigned to** field of the risk.
-   Stakeholders: Stakeholders for the project.

**Note:** If **Stakeholder** is selected, then when the project manager assigns the assessor, all users who are added to the Stakeholders related list in the project are displayed. The project manager can select the required stakeholder.

</td></tr><tr><td>

Risk rollup formula

</td><td>

The formula used to roll up the project risk scores. The choices are as follows:-   Average
-   Maximum
-   Minimum
 **Note:** Only the risks that are assessed using Advanced Risk Assessment are aggregated and have their scores rolled up. If a risk is retired, then the score of the retired risk is not aggregated. For details, see [Risk score rollup in Advanced Risk Assessment](../concept/risk-rollup-ara-concept.md).

</td></tr><tr><td>

Approver type

</td><td>

Approver of the project risk. The approver has to approve the risk assessment. The choices are as follows:-   None: No approver is necessary.
-   Project Manager: The project manager is the approver.
-   Stakeholder: The stakeholders for the project.


</td></tr><tr><td class="sub-head" colspan="2">

Enterprise Risk Assessment

</td></tr><tr><td>

Assessor type

</td><td>

Assessor for enterprise risk. The choices are as follows:-   Project Manager: The user assigned as the project manager of the project.
-   Risk Owner: The user who is identified in the**Assigned to** field of the risk.
-   Group: The group to which the risk is assigned.
 **Note:** This user must have the sn\_risk.manager role.

</td></tr><tr><td>

Approver type

</td><td>

Approver for enterprise risk. The choices are as follows:-   None: When no approver is necessary.
-   Project Manager: The user assigned as the project manager of the project.
-   Group: The group to which the risk is assigned.


</td></tr><tr><td>

Days to overdue

</td><td>

Number of days after which an assessment is considered overdue starting from the date of initiation. The field is automatically set to **5**.**Note:** The assessor gets reminder notifications before the due date approaches. The assessor and the assessor's manager get a notification after the due date passes.

</td></tr><tr><td>

Assessor group

</td><td>

The group which assesses the enterprise risk if the **Assessor type** field has **Group**.

</td></tr></tbody>
</table>5.  Click **Update**.


## Result

The assessor and approver details are set.

**Parent Topic:**[Project Risk Assessment using Advanced Risk Assessment](../concept/risk-and-ppm-better-together.md)


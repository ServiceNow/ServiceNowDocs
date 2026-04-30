---
title: Audit survey form
description: The safety audit manager can use the audit survey form to assign a smart assessment or survey to be conducted as part of a safety audit.
locale: en-US
release: yokohama
product: Health and Safety Risk Management
classification: health-and-safety-risk-management
topic_type: reference
last_updated: "2026-01-12"
reading_time_minutes: 2
breadcrumb: [Reference, Health and Safety Risk Management, Health and Safety, Employee Service Management]
---

# Audit survey form

The safety audit manager can use the audit survey form to assign a smart assessment or survey to be conducted as part of a safety audit.

For information on adding an audit survey to an audit or audit schedule, see [Set up a safety audit schedule](../task/hs-setup-safety-audit-schedule.md).

<table id="table_ehm_qpz_xhc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

System-generated unique number for the survey record.

</td></tr><tr><td>

Assigned to

</td><td>

User this audit survey is assigned to.

</td></tr><tr><td>

State

</td><td>

State of the audit survey.

</td></tr><tr><td>

Assessment type

</td><td>

Type of the assessment to be conducted for this audit.

</td></tr><tr><td>

Audit smart assessment template

</td><td>

Smart assessment template to be used to complete this audit.Only the templates with the **Assessment targets** field set to Audit survey \[sn\_hs\_rm\_audit\_survey\] table are available in this list. Use smart assessment templates available with the application or build new ones with the Smart Assessment Engine. For more information, see [Configure a Smart Assessment template](../task/hs-configure-smart-assessment-template.md).

This field appears only when **Assessment type** is set as **Smart Assessment**.

</td></tr><tr><td>

Audit survey

</td><td>

Audit survey to be completed for this inspection. Select the survey to use.Only the surveys with the **Source table** field set to Inspection \[sn\_hs\_rm\_inspection\] table are available in this list. Use surveys available with the application or build new ones with the Survey designer. You can also associate any of your pre-built surveys with inspection records in Health and Safety Risk Management. For more information, see [Configure a safety inspection or audit survey](../task/hs-configure-safety-inspection-surveys.md).

This field appears only when **Assessment type** is set as **Survey**.

</td></tr><tr><td>

Order

</td><td>

Order in which this assessment should be conducted when multiple audit surveys exist for an audit.

</td></tr><tr><td>

Description

</td><td>

Description of this safety audit schedule.

</td></tr></tbody>
</table>**Parent Topic:**[Health and Safety Risk Management reference](../concept/hs-risk-mgmt-reference.md)


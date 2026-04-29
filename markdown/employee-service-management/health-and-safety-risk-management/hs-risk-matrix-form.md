---
title: Risk matrix form
description: Safety team can use the risk matrixes to create and conduct risk assessments in the Health and Safety Workspace.
locale: en-US
release: australia
product: Health and Safety Risk Management
classification: health-and-safety-risk-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Reference, Health and Safety Risk Management, Health and Safety, Employee Service Management]
---

# Risk matrix form

Safety team can use the risk matrixes to create and conduct risk assessments in the Health and Safety Workspace.

For more information, see [Conduct a safety risk assessment](../task/hs-conduct-risk-assessment.md).

<table id="table_h2z_pzc_c1c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Risk matrix details

</td></tr><tr><td>

Number

</td><td>

System-generated unique number for the risk matrix.

</td></tr><tr><td>

Location

</td><td>

Location that this risk matrix applies to.

</td></tr><tr><td>

Short description

</td><td>

Brief description about the risk matrix.

</td></tr><tr><td>

Matrix grid

</td><td>

Size of the grid to use, for example, 4\*4 and 5\*5.

</td></tr><tr><td>

Active

</td><td>

Option for making the matrix available for use. A risk matrix must be active to be used.

</td></tr><tr><td class="sub-head" colspan="2">

Likelihood and severity

</td></tr><tr><td>

Likelihood level

</td><td>

Description of the likelihood level. These descriptions are used to populate the likelihood options on risk assessments where this matrix is used. The number of likelihood levels is based on the selected grid size. For example, for a matrix grid of size 5\*2, there are five likelihood levels.

</td></tr><tr><td>

Severity level

</td><td>

Description of the severity level. These descriptions are used to populate the severity options on risk assessments where this matrix is used.The number of severity levels is based on the selected grid size. For example, for a matrix grid of size 5\*2, there are two severity levels.

</td></tr><tr><td class="sub-head" colspan="2">

Risk tolerance

</td></tr><tr><td>

Risk tolerance

</td><td>

Range, color, and description of the risk level. Select a range and color and enter a title for it.This risk tolerance range and title computes the risk level for a hazard on the **Hazard assessment** form, **Risk analyses** tab, and the risk assessment form header. For more information, see [Assess a hazard and its risk levels](../task/add-a-risk-and-its-controls-for-a-safety-risk-assessment.md).

The value of the range is determined by multiplying likelihood level by severity level. For example, according to the grid in the following image, a hazard with a level 3 likelihood \(Once per month\) and a level 2 severity \(Minor\) has a risk tolerance of 3\*2 = 6. The risk level for this hazard lies in the range 3 to 6, therefore, its risk level is displayed as Moderate.

![Risk matrix configuration showing calculation of risk ranges based on likelihood and severity values.](../image/hs-risk-matrix.png)

</td></tr><tr><td class="sub-head" colspan="2">

Risk matrix preview

</td></tr><tr><td>

Risk matrix preview

</td><td>

Heatmap for visual representation of the risk matrix based on the defined levels, colors, and ranges in the real time.

</td></tr></tbody>
</table>**Parent Topic:**[Health and Safety Risk Management reference](../concept/hs-risk-mgmt-reference.md)


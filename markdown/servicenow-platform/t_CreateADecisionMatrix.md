---
title: Create a decision matrix
description: The name and labels on a decision matrix are closely linked to the categories you choose for the axes. For that reason, first select the metric type and define the X and Y axes before you fill in other fields on the Decision Matrix form.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Assessment administrator tasks, Using assessments, Assessments, Assessments and Surveys, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Create a decision matrix

The name and labels on a decision matrix are closely linked to the categories you choose for the axes. For that reason, first select the metric type and define the X and Y axes before you fill in other fields on the Decision Matrix form.

## Before you begin

Role required: assessment\_admin or admin

## Procedure

1.  Navigate to **All** &gt; **Assessments** &gt; **Admin** &gt; **Decision Matrixes**.

2.  Click **New**.

3.  Select the metric **Type** to plot results for.

4.  Right-click the form header and select **Save**.

    The X Axis and Y Axis related lists appear.

5.  Define which metric categories the axes represent.

    Each axis can represent a single category or multiple categories. You must specify at least one category per axis in order for the decision matrix to render properly. The available categories are limited to those associated to the metric type selected. To avoid confusion, always update the text for the axis and quadrant labels after editing or adding metric categories to an axis.

    ![Decision matrix axes](../images/DecisionMatrixAxes.png "Decision matrix axes")

6.  Fill in the remaining fields on the Decision Matrix form and save the record.

    ![Decision Matrix form](../images/DecisionMatrixForm.png)

    **Note:** For color fields, either HTML color names or hexidecimal \(hex\) values are acceptable. For hex values, the \# character is optional. Values are not case-sensitive. For example, all of the following values are valid: LightGray, lightgray, \#D3D3D3, d3d3d3.

<table id="table_d1w_jkm_q4"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the decision matrix, which appears as the title on the decision matrix page. It is recommended to include the axis categories in the name. For example, if you selected **Importance Rating** as the X-axis and **User Satisfaction** as the Y-axis, you might name the matrix **Importance vs. User Satisfaction**.

</td></tr><tr><td>

Type

</td><td>

Metric type associated with this decision matrix. Only results for assessable records of the selected metric type are plotted on the decision matrix.

</td></tr><tr><td>

Default

</td><td>

Determines whether or not this is the default decision matrix. The default decision matrix opens when you click **View Matrix** on a scorecard. Select the check box to set the matrix as the default decision matrix.The system prevents you from creating more than one default decision matrix per metric type. If there is already a default decision matrix for the type and you try to save a different matrix with the check box selected, an error message appears. The maximum values for the default decision matrix are controlled by the **Maximum number of items to show for a decision matrix field filter** property **\(com.snc.assessment.decision\_matrix\_filter\_max\_entries\)**, which has a default value of 1000.

</td></tr><tr><td class="sub-head" colspan="2">

Quadrant Design Section

</td></tr><tr><td>

Quadrant label color

</td><td>

Color of the label text for the quadrants. Each quadrant label displays in the center of the quadrant. You can enter an HTML color name or hex value for this and the other color fields.

</td></tr><tr><td>

X-Axis label

</td><td>

Label text for the X-axis of the decision matrix. It is recommended to include the metric category name in the label text. For example, for an X-axis category of **Importance Rating**, the X-axis label is **Importance**.

</td></tr><tr><td>

Plotted item color

</td><td>

Color used to display plotted items.

</td></tr><tr><td>

Top left label

</td><td>

Label text for the top left quadrant. For an X-axis labeled **Importance** and Y-axis labeled **Support**, you might label the top left quadrant **Low importance, high support**.

</td></tr><tr><td>

Top left color

</td><td>

Fill color for the top left quadrant.

</td></tr><tr><td>

Bottom left label

</td><td>

Label text for the bottom left quadrant.

</td></tr><tr><td>

Bottom left color

</td><td>

Fill color for the bottom left quadrant.

</td></tr><tr><td>

Bottom left label

</td><td>

Label text for the bottom left quadrant.

</td></tr><tr><td>

Bottom left color

</td><td>

Fill color for the bottom left quadrant.

</td></tr><tr><td>

Y-Axis label

</td><td>

Label text for the Y-axis of the decision matrix.

</td></tr><tr><td>

Highlight item color

</td><td>

Color of highlighted plotted items. When you view a decision matrix from an assessable record's scorecard, the assessable record plotted item appears in the highlight color. Specify a highlight color that is different than the **Plotted item color**.![Highlight item color](../images/HighlightItemVsPlottedItemColor.png)

</td></tr><tr><td>

Top right label

</td><td>

Label text for the top right quadrant.

</td></tr><tr><td>

Top right color

</td><td>

Fill color for the top right quadrant.

</td></tr><tr><td>

Bottom right label

</td><td>

Label text for the bottom right quadrant.

</td></tr><tr><td>

Bottom right color

</td><td>

Fill color for the bottom right quadrant.

</td></tr><tr><td class="sub-head" colspan="2">

Related Lists

</td></tr><tr><td>

X Axis

</td><td>

Lists categories that define the X-axis of the decision matrix.

</td></tr><tr><td>

Y Axis

</td><td>

Lists categories that define the Y-axis of the decision matrix.

</td></tr></tbody>
</table>
-   **[Decision matrixes](../reference/r_AdministerDecisionMatrixes.md)**  
Assessment results obtained by questionnaires and scripted metrics can be mapped to decision matrixes.

**Parent Topic:**[Assessment administrator tasks](../concept/c_AssessmentProcess.md)


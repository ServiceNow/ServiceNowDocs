---
title: Custom Metric form
description: Description of the field values for the Custom Metric form.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Surveys reference, Surveys, Assessments and Surveys, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Custom Metric form

Description of the field values for the Custom Metric form.

<table id="table_vrl_4yj_xrb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of your custom metric type. The name appears on the Custom Metrics page.

</td></tr><tr><td>

Application

</td><td>

Name of the application that you are creating the custom metric type for.

</td></tr><tr><td>

Icon

</td><td>

An icon for the custom metric type. The custom metric type appears as the selected icon in Survey Designer.

</td></tr><tr><td>

Active

</td><td>

Option to enable or disable the custom metric type. If selected, the Survey Designer shows the custom metric type.

</td></tr><tr><td>

Macro

</td><td>

A macro that is used to render the custom metric type.**Note:**

-   If the **Macro** field is empty, the question is not rendered on the platform form.
-   The macro record that you select must contain an input element with the following attributes. This input element holds the value for the metric.
    -   `datatype=”custom”`
    -   `name= “${jvar_question_name}”`
-   Value parameters can be accessed in a macro using the **$\{jvar\_value\_params\}** object.

</td></tr><tr><td>

Widget

</td><td>

The widget is used to render the custom metric.**Note:**

-   If the **Widget** field is empty, the question is not rendered on the portal form.
-   The widget record that you select must contain an input element with the following attributes. This input element holds the value for the metric.
    -   `ng-model="page.fieldValue"`
    -   `ng-model-options="{getterSetter: true}"`
-   The client script must have **$scope** as one of the parameters in the function definition. The value parameters can be accessed using the**$scope.page.field.value\_params** object.

</td></tr><tr><td>

Result type

</td><td>

Result type for the custom metric type.If a value is changed, the new results are stored as per the new value and the previous results remain unchanged. If a value is changed from string to number, the reports might not show the charts properly. If a value is changed from number to string, the scorecard is shown in a list view.

</td></tr><tr><td>

Value parameters

</td><td>

Value pairs that are passed to the custom metric type renderers. For example, in star ratings, you can pass a value as 5 for 5 stars or 10 for 10 stars.

</td></tr></tbody>
</table>**Parent Topic:**[Surveys reference](survey-reference.md)


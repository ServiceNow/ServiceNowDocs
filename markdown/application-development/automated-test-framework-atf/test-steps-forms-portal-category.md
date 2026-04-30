---
title: Forms in Service Portal category
description: Validate the functionality of fields and UI actions in Service Portal form widgets.Opens a form in a portal.Sets the values of fields in a form. To use this step, you must have already opened a form using the Open a Form \(SP\) test step.Validates field values on the current form based on defined conditions. To use this step, you must have already opened a form using the Open a Form \(SP\) test step.Validates field states on a form in Service Portal.Test the functionality of attaching a file to a Service Portal form widget.Determines whether a UI action on the current Service Portal form is visible. To use this step, you must have already opened a form using the Open a Form \(SP\) test step.Selects a UI action on the current Service Portal form and outputs the table and sys\_id of the record on which the action was selected.Submits the current form in a Service Portal page and outputs the table and sys\_id of the submitted record.
locale: en-US
release: yokohama
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 11
breadcrumb: [Automated Test Framework \(ATF\) test step categories, Automated Test Framework \(ATF\), Testing and debugging applications, Building applications]
---

# Forms in Service Portal category

Validate the functionality of fields and UI actions in Service Portal form widgets.

## Service Portal dependency

Creating automated Service Portal steps requires knowledge of the ServiceNow data model and Service Portal form and data structures.

## Open a Form \(SP\)

Opens a form in a portal.

Use this step for the base system Form page. For custom form pages, use the [Open Service Portal Page](test-steps-custom-ui-category.md#) step from the Custom UI category.

<table id="table_vkh_2rc_vbb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Execution order

</td><td id="atf-exec-order">

Integer specifying the order in which the test executes this step.As you create steps, the system automatically assigns each step an incremental value. This value causes the test to execute steps in the order that you created them in. You can change this default order by editing the **Execution order** values.

</td></tr><tr><td>

Active

</td><td id="atf-active">

Option to activate this test step for use.

</td></tr><tr><td>

Timeout

</td><td id="atf-timeout">

Number of seconds allowed before the step fails. If the validation fails, the system repeats the step until it reaches the duration of the timeout. If the validation fails after the timeout duration has passed, the step fails.

</td></tr><tr><td>

Application

</td><td id="atf-application-scope">

Application scope in which the system runs this step.

</td></tr><tr><td>

Test

</td><td id="atf-test">

Read-only name of the test that you're adding the step to.

</td></tr><tr><td>

Step config

</td><td id="atf-step-config">

Read-only name of the step.

</td></tr><tr><td>

Description

</td><td id="atf-description">

Description of the test step. This field value is automatically set based on the field values of the test step. This field appears after the test step is submitted.

</td></tr><tr><td>

Notes

</td><td id="atf-notes">

Notes about the test step.

</td></tr><tr><td>

Portal

</td><td id="atf-forms-sp-portal">

Portal in which the defined form opens. Service Portal is the default.

</td></tr><tr><td>

Page

</td><td id="atf-forms-sp-page">

Page to open in the defined portal. The form page is the default.

</td></tr><tr><td>

Table

</td><td id="atf-forms-sp-table">

Table containing the form to open.

</td></tr><tr><td>

sys\_id

</td><td id="atf-forms-sp-sysid">

Sys\_id of the record to open. Default is `-1`, which opens a new record.

</td></tr><tr><td>

View

</td><td id="atf-forms-sp-view">

The form view to open. If blank, the system uses the default view.

</td></tr><tr><td>

Query parameters

</td><td id="atf-forms-sp-query-parameters">

Additional URL query parameters and values for the form.

</td></tr></tbody>
</table>## Set Field Values \(SP\)

Sets the values of fields in a form. To use this step, you must have already opened a form using the **Open a Form \(SP\)** test step.

<table id="table_rrp_l5c_vbb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Execution order

</td><td id="atf-exec-order">

Integer specifying the order in which the test executes this step.As you create steps, the system automatically assigns each step an incremental value. This value causes the test to execute steps in the order that you created them in. You can change this default order by editing the **Execution order** values.

</td></tr><tr><td>

Active

</td><td id="atf-active">

Option to activate this test step for use.

</td></tr><tr><td>

Application

</td><td id="atf-application-scope">

Application scope in which the system runs this step.

</td></tr><tr><td>

Test

</td><td id="atf-test">

Read-only name of the test that you're adding the step to.

</td></tr><tr><td>

Step config

</td><td id="atf-step-config">

Read-only name of the step.

</td></tr><tr><td>

Description

</td><td id="atf-description">

Description of the test step. This field value is automatically set based on the field values of the test step. This field appears after the test step is submitted.

</td></tr><tr><td>

Notes

</td><td id="atf-notes-condition-builder">

Notes about the test step.**Note:** Use the condition builder to set the field value. The condition builder displays an appropriate control for the field data type. For example, a reference field displays a **Lookup record** control.

</td></tr><tr><td>

Table

</td><td id="atf-set-field-values-table">

The table for the form on which to set field values. The value should be the table in the **Open a Form \(SP\)** step.

</td></tr><tr><td>

Field values

</td><td id="atf-set-field-values">

Fields for which to set values and the values to be set for those fields.

</td></tr></tbody>
</table>## Field Values Validation \(SP\)

Validates field values on the current form based on defined conditions. To use this step, you must have already opened a form using the **Open a Form \(SP\)** test step.

<table id="table_ygt_l5c_vbb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Execution order

</td><td id="atf-exec-order">

Integer specifying the order in which the test executes this step.As you create steps, the system automatically assigns each step an incremental value. This value causes the test to execute steps in the order that you created them in. You can change this default order by editing the **Execution order** values.

</td></tr><tr><td>

Active

</td><td id="atf-active">

Option to activate this test step for use.

</td></tr><tr><td>

Application

</td><td id="atf-application-scope">

Application scope in which the system runs this step.

</td></tr><tr><td>

Test

</td><td id="atf-test">

Read-only name of the test that you're adding the step to.

</td></tr><tr><td>

Step config

</td><td id="atf-step-config">

Read-only name of the step.

</td></tr><tr><td>

Description

</td><td id="atf-description">

Description of the test step. This field value is automatically set based on the field values of the test step. This field appears after the test step is submitted.

</td></tr><tr><td>

Notes

</td><td id="atf-notes-condition-builder">

Notes about the test step.**Note:** Use the condition builder to set the field value. The condition builder displays an appropriate control for the field data type. For example, a reference field displays a **Lookup record** control.

</td></tr><tr><td>

Table

</td><td id="atf-field-values-validation-table">

The table that contains the form on which to validate fields. The value should be the table in the **Open a Form \(SP\)** step.

</td></tr><tr><td>

Conditions

</td><td id="atf-field-values-validation-conditions">

Conditions used to validate one or more fields on the form. If the condition evaluates to true, the step passes.

</td></tr></tbody>
</table>## Field State Validation \(SP\)

Validates field states on a form in Service Portal.

<table id="table_yxw_l5c_vbb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Execution order

</td><td id="atf-exec-order">

Integer specifying the order in which the test executes this step.As you create steps, the system automatically assigns each step an incremental value. This value causes the test to execute steps in the order that you created them in. You can change this default order by editing the **Execution order** values.

</td></tr><tr><td>

Active

</td><td id="atf-active">

Option to activate this test step for use.

</td></tr><tr><td>

Application

</td><td id="atf-application-scope">

Application scope in which the system runs this step.

</td></tr><tr><td>

Test

</td><td id="atf-test">

Read-only name of the test that you're adding the step to.

</td></tr><tr><td>

Step config

</td><td id="atf-step-config">

Read-only name of the step.

</td></tr><tr><td>

Description

</td><td id="atf-description">

Description of the test step. This field value is automatically set based on the field values of the test step. This field appears after the test step is submitted.

</td></tr><tr><td>

Notes

</td><td id="atf-notes">

Notes about the test step.

</td></tr><tr><td>

Table

</td><td id="atf-field-state-sp-table">

The table for the form on which to validate field states. The value should be the table in the **Open a Form \(SP\)** step.

</td></tr><tr><td>

Visible

</td><td id="atf-table-field-state-validation-visible">

Validates whether the fields on this form are visible. The test fails if the fields are not visible.

</td></tr><tr><td>

Not visible

</td><td id="atf-table-field-state-validation-not-visible">

Validates whether the fields on this form are visible. The test fails if the fields are visible.

</td></tr><tr><td>

Read only

</td><td id="atf-table-field-state-validation-read-only">

Validates whether the fields on this form are read only. The test fails if the fields are not read only.

</td></tr><tr><td>

Not read only

</td><td id="atf-table-field-state-validation-not-read-only">

Validates whether the fields on this form are read only. The test fails if the fields are read only.

</td></tr><tr><td>

Mandatory

</td><td id="atf-table-field-state-validation-mandatory">

Validates whether the fields on this form are mandatory. The test fails if the fields are not mandatory.

</td></tr><tr><td>

Not Mandatory

</td><td id="atf-table-field-state-validation-not-mandatory">

Validates whether the fields on this form are mandatory. The test fails if the fields are mandatory.

</td></tr></tbody>
</table>## Add Attachments to Form \(SP\)

Test the functionality of attaching a file to a Service Portal form widget.

To use this step, you must have already opened a form using the **Open a Form \(SP\)** test step or **Open Service Portal Page steps**. This step can't be used after a **Submit Form** step or **Click a UI Action** step has been used.

<table id="table_xn5_4s3_blb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Execution order

</td><td id="atf-exec-order">

Integer specifying the order in which the test executes this step.As you create steps, the system automatically assigns each step an incremental value. This value causes the test to execute steps in the order that you created them in. You can change this default order by editing the **Execution order** values.

</td></tr><tr><td>

Active

</td><td id="atf-active">

Option to activate this test step for use.

</td></tr><tr><td>

Application

</td><td id="atf-application-scope">

Application scope in which the system runs this step.

</td></tr><tr><td>

Test

</td><td id="atf-test">

Read-only name of the test that you're adding the step to.

</td></tr><tr><td>

Step config

</td><td id="atf-step-config">

Read-only name of the step.

</td></tr><tr><td>

Notes

</td><td id="atf-notes">

Notes about the test step.

</td></tr><tr><td>

Upload Attachments

</td><td>

Button to attach one or more files to the form.

</td></tr></tbody>
</table>## UI Action Visibility Validation \(SP\)

Determines whether a UI action on the current Service Portal form is visible. To use this step, you must have already opened a form using the **Open a Form \(SP\)** test step.

Service Portal only supports server UI actions. The setRedirectURL\(\) method and client UI actions are not supported. UI action visibility can vary depending on the currently logged in or impersonated user.

<table id="table_jc1_m5c_vbb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Execution order

</td><td id="atf-exec-order">

Integer specifying the order in which the test executes this step.As you create steps, the system automatically assigns each step an incremental value. This value causes the test to execute steps in the order that you created them in. You can change this default order by editing the **Execution order** values.

</td></tr><tr><td>

Active

</td><td id="atf-active">

Option to activate this test step for use.

</td></tr><tr><td>

Application

</td><td id="atf-application-scope">

Application scope in which the system runs this step.

</td></tr><tr><td>

Test

</td><td id="atf-test">

Read-only name of the test that you're adding the step to.

</td></tr><tr><td>

Step config

</td><td id="atf-step-config">

Read-only name of the step.

</td></tr><tr><td>

Description

</td><td id="atf-description">

Description of the test step. This field value is automatically set based on the field values of the test step. This field appears after the test step is submitted.

</td></tr><tr><td>

Notes

</td><td id="atf-notes">

Notes about the test step.

</td></tr><tr><td>

Table

</td><td id="atf-ui-visibility-table">

The table for the form on which to check UI action visibility. The value should be the table in the **Open a Form \(SP\)** step.

</td></tr><tr><td>

Visible

</td><td id="atf-ui-visibility-visible">

Fields from the UI Actions table to be checked for visibility. Includes only form-based UI actions. The test fails if the UI action is not visible on the form for the currently logged in user.**Note:** If the list contains UI actions with the same name, check the form to determine the sys\_id of the element. Then filter by sys\_id in the UI Action table to select the correct element in the step.

</td></tr><tr><td>

Not visible

</td><td id="atf-ui-visibility-not-visible">

Fields from the UI Actions table to be checked for visibility. Includes only form-based UI actions. The test fails if the UI action is visible on the form for the currently logged in user.**Note:** If the list contains UI actions with the same name, check the form to determine the sys\_id of the element. Then filter by sys\_id in the UI Action table to select the correct element in the step.

</td></tr></tbody>
</table>## Click UI Action \(SP\)

Selects a UI action on the current Service Portal form and outputs the table and sys\_id of the record on which the action was selected.

To use this step, you must have already opened a form using the **Open a Form \(SP\)** test step. After using this step, you cannot use any other form steps.

<table id="table_zcb_j2p_zcb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Execution order

</td><td id="atf-exec-order">

Integer specifying the order in which the test executes this step.As you create steps, the system automatically assigns each step an incremental value. This value causes the test to execute steps in the order that you created them in. You can change this default order by editing the **Execution order** values.

</td></tr><tr><td>

Active

</td><td id="atf-active">

Option to activate this test step for use.

</td></tr><tr><td>

Timeout

</td><td id="atf-timeout">

Number of seconds allowed before the step fails. If the validation fails, the system repeats the step until it reaches the duration of the timeout. If the validation fails after the timeout duration has passed, the step fails.

</td></tr><tr><td>

Application

</td><td id="atf-application-scope">

Application scope in which the system runs this step.

</td></tr><tr><td>

Test

</td><td id="atf-test">

Read-only name of the test that you're adding the step to.

</td></tr><tr><td>

Step config

</td><td id="atf-step-config">

Read-only name of the step.

</td></tr><tr><td>

Description

</td><td id="atf-description">

Description of the test step. This field value is automatically set based on the field values of the test step. This field appears after the test step is submitted.

</td></tr><tr><td>

Notes

</td><td id="atf-notes">

Notes about the test step.

</td></tr><tr><td>

Table

</td><td id="atf-click-ui-table">

The table for the form on which to click a UI action. The value should be the table in the **Open a Form \(SP\)** step.

</td></tr><tr><td>

UI action

</td><td id="atf-click-ui-action">

The UI action to click, selected from the UI Actions table. Includes only form-based UI actions.

</td></tr><tr><td>

Assert type

</td><td id="atf-click-ui-assert-type">

Specifies where to check for form submission after clicking the UI action:-   **--None--**: Selects the UI action without validating mandatory or other fields.
-   **Form submission canceled in browser**: Checks whether the form was canceled in the browser and did not reach the server due to validation or other issues.
-   **Form submitted to server**: Checks whether the form was submitted to the server.

</td></tr></tbody>
</table>|Field|Description|
|-----|-----------|
|record\_id|Sys\_id of the record on which the action was clicked.|
|table|Table with the clicked UI action.|

## Submit a Form \(SP\)

Submits the current form in a Service Portal page and outputs the table and sys\_id of the submitted record.

To use this step, you must have already opened a form using the **Open a Form \(SP\)** test step. After using this step, the page closes. You can't use any other steps on the current page.

<table id="table_jkk_m5c_vbb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Execution order

</td><td id="atf-exec-order">

Integer specifying the order in which the test executes this step.As you create steps, the system automatically assigns each step an incremental value. This value causes the test to execute steps in the order that you created them in. You can change this default order by editing the **Execution order** values.

</td></tr><tr><td>

Active

</td><td id="atf-active">

Option to activate this test step for use.

</td></tr><tr><td>

Timeout

</td><td id="atf-timeout">

Number of seconds allowed before the step fails. If the validation fails, the system repeats the step until it reaches the duration of the timeout. If the validation fails after the timeout duration has passed, the step fails.

</td></tr><tr><td>

Application

</td><td id="atf-application-scope">

Application scope in which the system runs this step.

</td></tr><tr><td>

Test

</td><td id="atf-test">

Read-only name of the test that you're adding the step to.

</td></tr><tr><td>

Step config

</td><td id="atf-step-config">

Read-only name of the step.

</td></tr><tr><td>

Description

</td><td id="atf-description">

Description of the test step. This field value is automatically set based on the field values of the test step. This field appears after the test step is submitted.

</td></tr><tr><td>

Notes

</td><td id="atf-notes">

Notes about the test step.

</td></tr><tr><td>

Assert type

</td><td id="atf-submit-form-sp-assert-type">

Specifies where to check for form submission:-   **--None--**: Submits the form without validating mandatory or other fields.
-   **Form submitted to server**: Checks if the form was submitted to the server.
-   **Form submission canceled in browser**: Checks whether the form was canceled in the browser and did not reach the server due to validation or other issues.

</td></tr></tbody>
</table>|Field|Description|
|-----|-----------|
|record\_id|Sys\_id of the submitted record.|
|table|Table for the submitted record.|


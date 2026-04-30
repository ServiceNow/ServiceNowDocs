---
title: Form category
description: Validate the functionality of fields and UI actions on a form.Open a form to a new record in the specified table and Form UI.Open a form to an existing record in the specified table and Form UI.Set the fields on the current form to the specified values.Validate field values on the current form.Validate the state of specified fields. States validated can include mandatory, non-mandatory, read-only, non-read-only, visible, and non-visible.Verify if a UI action is visible on the current form. To run this step, your test must have already opened a form using either the Open a New Form or Open an Existing Record step.Verify if a declarative action is visible on the current form.Add one or more mandatory attachments to the current form. Select the attachments that the test step adds to the form from the Upload Attachments list.Click a button within a modal in the specified Form UI.Click a UI action on the current form.Click a declarative action on the current form.Submit the current form.
locale: en-US
release: zurich
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 23
breadcrumb: [Test step categories, Automated Test Framework \(ATF\), Testing and debugging applications, Building applications]
---

# Form category

Validate the functionality of fields and UI actions on a form.

**Note:** Test steps that include the **Form UI** field give you the option to select an available UI. For any available workspace, navigation between tabs is not supported. Use the **Open a New Form** or **Open an Existing Record** step to reopen a form.

It is to be noted that Agent Workspace has been removed from the Platform. If you have any Agent Workspace tests or test suites, they won't work anymore.

## Open a New Form

Open a form to a new record in the specified table and **Form UI**.

<table id="table_od3_dgb_hzb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Execution order

</td><td>

Integer specifying the order in which the test executes this step.As you create steps, the system automatically assigns each step an incremental value. This value causes the test to execute steps in the order that you created them in. You can change this default order by editing the **Execution order** values.

</td></tr><tr><td>

Active

</td><td>

Option to activate this test step for use.

</td></tr><tr><td>

Application

</td><td>

Application scope in which the system runs this step.

</td></tr><tr><td>

Test

</td><td>

Read-only name of the test that you're adding the step to.

</td></tr><tr><td>

Step config

</td><td>

Read-only name of the step.

</td></tr><tr><td>

Description

</td><td>

Description of the test step. This field value is automatically set based on the field values of the test step. This field appears after the test step is submitted.

</td></tr><tr><td>

Notes

</td><td>

Notes about the test step

</td></tr><tr><td>

Form UI

</td><td>

Option to select an available UI. Apart from the Standard UI, you have other workspace selections available. Depending on the selected workspace, the UI might vary.**Note:** Workspaces are not supported in Internet Explorer \(IE\). See [KB0683275](https://support.servicenow.com/kb_view.do?sysparm_article=KB0683275) for more details.

</td></tr><tr><td>

Table

</td><td>

Name of the table for the new form.

</td></tr><tr><td>

View

</td><td>

Name of the view in which you want this form to open. The testing user must have access to that view. If the name is not a valid form view, the form opens in its default view.**Note:** This field appears when **Standard UI** is chosen from **Form UI**.

</td></tr></tbody>
</table>## Open an Existing Record

Open a form to an existing record in the specified table and **Form UI**.

**Note:** Using an existing record may cause unexpected behavior for this test. See [Automated Test Framework design considerations](../concept/automated-test-framework-design-considerations.md) for more information.

<table id="table_od3_dgb_hzb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Execution order

</td><td>

Integer specifying the order in which the test executes this step.As you create steps, the system automatically assigns each step an incremental value. This value causes the test to execute steps in the order that you created them in. You can change this default order by editing the **Execution order** values.

</td></tr><tr><td>

Active

</td><td>

Option to activate this test step for use.

</td></tr><tr><td>

Application

</td><td>

Application scope in which the system runs this step.

</td></tr><tr><td>

Test

</td><td>

Read-only name of the test that you're adding the step to.

</td></tr><tr><td>

Step config

</td><td>

Read-only name of the step.

</td></tr><tr><td>

Description

</td><td>

Description of the test step. This field value is automatically set based on the field values of the test step. This field appears after the test step is submitted.

</td></tr><tr><td>

Notes

</td><td>

Notes about the test step

</td></tr><tr><td>

Form UI

</td><td>

Option to select an available UI. Apart from the Standard UI, you have other workspace selections available. Depending on the selected workspace, the UI might vary.**Note:** Workspaces are not supported in Internet Explorer \(IE\). See [KB0683275](https://support.servicenow.com/kb_view.do?sysparm_article=KB0683275) for more details.

</td></tr><tr><td>

Table

</td><td>

Name of the table for the new form.

</td></tr><tr><td>

Record

</td><td>

Record ID of the record that you want to open and name of the document that you want to open.

</td></tr><tr><td>

View

</td><td>

Name of the view in which you want this form to open. The testing user must have access to that view. If the name is not a valid form view, the form opens in its default view.**Note:** This field appears when **Standard UI** is chosen from **Form UI**.

</td></tr></tbody>
</table>## Set Field Values

Set the fields on the current form to the specified values.

To run this step, your test must have already opened a form using either the **Open a New Form** or **Open an Existing Record** step. It is recommended to not run this step directly after a **Submit a Form** or **Click a UI Action** step. This is because they can redirect your test to a different page based on the navigation stack configuration on your instance or the script defined in the clicked UI action. Unless you are certain that the UI action will take you to a specific page, you should explicitly use an **Open a New Form** step after **Submit a Form** or **Click a UI Action** to ensure that the test is on the form as expected. Ensure that the test keeps passing consistently when added to a suite.

The **Field Values Validation**, **Set Field Values**, **Field State Validation**, and **UI Action Visibility** steps can appear in any order.

**Note:** This step waits for the form to load before setting field values. This step doesn't support reference qualifiers, neither at test design time nor at test runtime. A modal form appears either on top of another form or a list. To submit a modal form after setting the field values, your test must have already opened it on top of a form or a list.![Image showing modal form](../image/atf-modal-form.png)

<table id="table_od3_dgb_hzb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Execution order

</td><td>

Integer specifying the order in which the test executes this step.As you create steps, the system automatically assigns each step an incremental value. This value causes the test to execute steps in the order that you created them in. You can change this default order by editing the **Execution order** values.

</td></tr><tr><td>

Active

</td><td>

Option to activate this test step for use.

</td></tr><tr><td>

Application

</td><td>

Application scope in which the system runs this step.

</td></tr><tr><td>

Test

</td><td>

Read-only name of the test that you're adding the step to.

</td></tr><tr><td>

Step config

</td><td>

Read-only name of the step.

</td></tr><tr><td>

Description

</td><td>

Description of the test step. This field value is automatically set based on the field values of the test step. This field appears after the test step is submitted.

</td></tr><tr><td>

Notes

</td><td>

Notes about the test step

</td></tr><tr><td>

Form UI

</td><td>

Option to select an available UI. Apart from the Standard UI, you have other workspace selections available. Depending on the selected workspace, the UI might vary.**Note:** Workspaces are not supported in Internet Explorer \(IE\). See [KB0683275](https://support.servicenow.com/kb_view.do?sysparm_article=KB0683275) for more details.

</td></tr><tr><td>

Table

</td><td>

Name of the table for the new form.

</td></tr><tr><td>

Set field value

</td><td>

Assigns a value to a field on an open form.

</td></tr></tbody>
</table>## Field Values Validation

Validate field values on the current form.

To run this step, your test must have already opened a form using either the **Open a New Form** or **Open an Existing Record** step. It is recommended to not run this step directly after a **Submit a Form** or **Click a UI Action** step. This is because they can redirect your test to a different page based on the navigation stack configuration on your instance or the script defined in the clicked UI action. Unless you are certain that the UI action will take you to a specific page, you should explicitly use an **Open a New Form** step after **Submit a Form** or **Click a UI Action** to ensure that the test is on the form as expected. Ensure that the test keeps passing consistently when added to a suite.

The **Field Values Validation**, **Set Field Values**, **Field State Validation**, and **UI Action Visibility** steps can appear in any order.

For the **Field Values Validation** step, specify the values that you want to test using the standard conditions builder. You can test several conditions against the same field. This step passes if the overall condition is satisfied and fails if the condition is not satisfied. The **Conditions** field is case-sensitive and requires to have the exact value as on the form. To test the values of individual fields independently of each other, include a separate **Field Values Validation** step for each value that you test.

**Note:** The **Field Values Validation** step works only with fields that belong to the record for the open form. For example, with the incident table, this step is not able to validate the **Additional comments**, **Approval history**, **Comments**, or **Work notes** fields because these UI controls are not actual fields on the incident record. These UI controls make it convenient to work with related tables. To validate these cases, use the Server test step, **Record Validation**, instead.

<table id="table_od3_dgb_hzb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Execution order

</td><td>

Integer specifying the order in which the test executes this step.As you create steps, the system automatically assigns each step an incremental value. This value causes the test to execute steps in the order that you created them in. You can change this default order by editing the **Execution order** values.

</td></tr><tr><td>

Active

</td><td>

Option to activate this test step for use.

</td></tr><tr><td>

Timeout

</td><td>

Number of seconds allowed before the step fails. If the validation fails, the system repeats the step until it reaches the duration of the timeout. If the validation fails after the timeout duration has passed, the step fails.

</td></tr><tr><td>

Application

</td><td>

Application scope in which the system runs this step.

</td></tr><tr><td>

Test

</td><td>

Read-only name of the test that you're adding the step to.

</td></tr><tr><td>

Step config

</td><td>

Read-only name of the step.

</td></tr><tr><td>

Description

</td><td>

Description of the test step. This field value is automatically set based on the field values of the test step. This field appears after the test step is submitted.

</td></tr><tr><td>

Notes

</td><td>

Notes about the test step**Note:** Use the condition builder to set the field value. The condition builder displays an appropriate control for the field data type. For example, a reference field displays a **Lookup record** control.

</td></tr><tr><td>

Form UI

</td><td>

Option to select an available UI. Apart from the Standard UI, you have other workspace selections available. Depending on the selected workspace, the UI might vary.**Note:** Workspaces are not supported in Internet Explorer \(IE\). See [KB0683275](https://support.servicenow.com/kb_view.do?sysparm_article=KB0683275) for more details.

</td></tr><tr><td>

Table

</td><td>

Name of the table for the new form.

</td></tr><tr><td>

Conditions

</td><td>

Fields and values to be validated. Includes only fields that are visible on the open form. This field is case-sensitive.

</td></tr></tbody>
</table>## Field State Validation

Validate the state of specified fields. States validated can include mandatory, non-mandatory, read-only, non-read-only, visible, and non-visible.

You can specify a maximum time to wait for the states of the fields to match the conditions in this step.

<table id="table_od3_dgb_hzb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Execution order

</td><td>

Integer specifying the order in which the test executes this step.As you create steps, the system automatically assigns each step an incremental value. This value causes the test to execute steps in the order that you created them in. You can change this default order by editing the **Execution order** values.

</td></tr><tr><td>

Active

</td><td>

Option to activate this test step for use.

</td></tr><tr><td>

Timeout

</td><td>

Number of seconds allowed before the step fails. If the validation fails, the system repeats the step until it reaches the duration of the timeout. If the validation fails after the timeout duration has passed, the step fails.

</td></tr><tr><td>

Application

</td><td>

Application scope in which the system runs this step.

</td></tr><tr><td>

Test

</td><td>

Read-only name of the test that you're adding the step to.

</td></tr><tr><td>

Step config

</td><td>

Read-only name of the step.

</td></tr><tr><td>

Description

</td><td>

Description of the test step. This field value is automatically set based on the field values of the test step. This field appears after the test step is submitted.

</td></tr><tr><td>

Notes

</td><td>

Notes about the test step

</td></tr><tr><td>

Form UI

</td><td>

Option to select an available UI. Apart from the Standard UI, you have other workspace selections available. Depending on the selected workspace, the UI might vary.**Note:** Workspaces are not supported in Internet Explorer \(IE\). See [KB0683275](https://support.servicenow.com/kb_view.do?sysparm_article=KB0683275) for more details.

</td></tr><tr><td>

Table

</td><td>

Name of the table for the new form.

</td></tr><tr><td>

Visible

</td><td>

Validates whether the fields on this form are visible. The test fails if the fields are not visible.

</td></tr><tr><td>

Not visible

</td><td>

Validates whether the fields on this form are visible. The test fails if the fields are visible.

</td></tr><tr><td>

Read only

</td><td>

Validates whether the fields on this form are read only. The test fails if the fields are not read only.

</td></tr><tr><td>

Not read only

</td><td>

Validates whether the fields on this form are read only. The test fails if the fields are read only.

</td></tr><tr><td>

Mandatory

</td><td>

Validates whether the fields on this form are mandatory. The test fails if the fields are not mandatory.

</td></tr><tr><td>

Not mandatory

</td><td>

Validates whether the fields on this form are mandatory. The test fails if the fields are mandatory.

</td></tr></tbody>
</table>## UI Action Visibility

Verify if a UI action is visible on the current form. To run this step, your test must have already opened a form using either the **Open a New Form** or **Open an Existing Record** step.

The default visible UI actions vary depending on the user that you're currently impersonating.

<table id="table_od3_dgb_hzb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Execution order

</td><td>

Integer specifying the order in which the test executes this step.As you create steps, the system automatically assigns each step an incremental value. This value causes the test to execute steps in the order that you created them in. You can change this default order by editing the **Execution order** values.

</td></tr><tr><td>

Active

</td><td>

Option to activate this test step for use.

</td></tr><tr><td>

Timeout

</td><td>

Number of seconds allowed before the step fails. If the validation fails, the system repeats the step until it reaches the duration of the timeout. If the validation fails after the timeout duration has passed, the step fails.

</td></tr><tr><td>

Application

</td><td>

Application scope in which the system runs this step.

</td></tr><tr><td>

Test

</td><td>

Read-only name of the test that you're adding the step to.

</td></tr><tr><td>

Step config

</td><td>

Read-only name of the step.

</td></tr><tr><td>

Description

</td><td>

Description of the test step. This field value is automatically set based on the field values of the test step. This field appears after the test step is submitted.

</td></tr><tr><td>

Notes

</td><td>

Notes about the test step

</td></tr><tr><td>

Form UI

</td><td>

Option to select an available UI. Apart from the Standard UI, you have other workspace selections available. Depending on the selected workspace, the UI might vary.**Note:** Workspaces are not supported in Internet Explorer \(IE\). See [KB0683275](https://support.servicenow.com/kb_view.do?sysparm_article=KB0683275) for more details.

</td></tr><tr><td>

Table

</td><td>

Name of the table for the new form.

</td></tr><tr><td>

Visible

</td><td>

Validates whether UI actions on this form are visible. The test fails if the UI actions are not visible.

</td></tr><tr><td>

Not visible

</td><td>

Validates whether UI actions on this form are visible. The test fails if the UI actions are visible.

</td></tr></tbody>
</table>## Declarative Action Visibility

Verify if a declarative action is visible on the current form.

The default visible declarative actions vary depending on the user that you're currently impersonating.

<table id="table_od3_dgb_hzb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Execution order

</td><td>

Integer specifying the order in which the test executes this step.As you create steps, the system automatically assigns each step an incremental value. This value causes the test to execute steps in the order that you created them in. You can change this default order by editing the **Execution order** values.

</td></tr><tr><td>

Active

</td><td>

Option to activate this test step for use.

</td></tr><tr><td>

Application

</td><td>

Application scope in which the system runs this step.

</td></tr><tr><td>

Test

</td><td>

Read-only name of the test that you're adding the step to.

</td></tr><tr><td>

Step config

</td><td>

Read-only name of the step.

</td></tr><tr><td>

Notes

</td><td>

Notes about the test step

</td></tr><tr><td>

Form UI

</td><td>

Option to select an available UI. Apart from the Standard UI, you have other workspace selections available. Depending on the selected workspace, the UI might vary.**Note:** Workspaces are not supported in Internet Explorer \(IE\). See [KB0683275](https://support.servicenow.com/kb_view.do?sysparm_article=KB0683275) for more details.

</td></tr><tr><td>

Table

</td><td>

Name of the table for the new form.

</td></tr><tr><td>

Visible

</td><td>

Validates whether declarative actions on this form are visible. The test fails if the declarative actions are not visible.

</td></tr><tr><td>

Not visible

</td><td>

Validates whether declarative actions on this form are visible. The test fails if the declarative actions are visible.

</td></tr></tbody>
</table>## Add Attachments to Form

Add one or more mandatory attachments to the current form. Select the attachments that the test step adds to the form from the Upload Attachments list.

<table id="table_od3_dgb_hzb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Execution order

</td><td>

Integer specifying the order in which the test executes this step.As you create steps, the system automatically assigns each step an incremental value. This value causes the test to execute steps in the order that you created them in. You can change this default order by editing the **Execution order** values.

</td></tr><tr><td>

Application

</td><td>

Application scope in which the system runs this step.

</td></tr><tr><td>

Active

</td><td>

Option to activate this test step for use.

</td></tr><tr><td>

Test

</td><td>

Read-only name of the test that you're adding the step to.

</td></tr><tr><td>

Step config

</td><td>

Read-only name of the step.

</td></tr><tr><td>

Notes

</td><td>

Notes about the test step

</td></tr><tr><td>

Upload Attachments

</td><td>

Button to add one or more mandatory attachments to the form.

</td></tr></tbody>
</table>**Note:** The Add Attachments to Form test step can't access the newly added UI workspace options.

## Click Modal Button

Click a button within a modal in the specified **Form UI**.

Specify your testing by selecting either the standard platform UI or workspace UI from the **Form UI** field. If you select the standard platform UI, this test step selects the button by ID on the specified modal and validates the following conditions:

-   UI page was opened in a modal.
-   Button is visible and enabled.

If you select an available workspace UI, this test step selects either the Confirm or Cancel action and optionally sets the field values within the modal. This step succeeds only if a modal dialog is open on the form, and if the specified button exists on that modal dialog.

Only modals opened with the following g\_modal functions are supported:

-   alert
-   confirm
-   confirmDestroy
-   showFields

**Note:** Click Modal Button now supports global and scoped application modals.

<table id="table_od3_dgb_hzb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Execution order

</td><td>

Integer specifying the order in which the test executes this step.As you create steps, the system automatically assigns each step an incremental value. This value causes the test to execute steps in the order that you created them in. You can change this default order by editing the **Execution order** values.

</td></tr><tr><td>

Active

</td><td>

Option to activate this test step for use.

</td></tr><tr><td>

Timeout

</td><td>

Number of seconds for the modal and the button to appear.

</td></tr><tr><td>

Application

</td><td>

Application scope in which the system runs this step.

</td></tr><tr><td>

Test

</td><td>

Read-only name of the test that you're adding the step to.

</td></tr><tr><td>

Step config

</td><td>

Read-only name of the step.

</td></tr><tr><td>

Description

</td><td>

Description of the test step. This field value is automatically set based on the field values of the test step. This field appears after the test step is submitted.

</td></tr><tr><td>

Notes

</td><td>

Notes about the test step

</td></tr><tr><td>

Form UI

</td><td>

Option to select an available UI.**Note:** Workspaces are not supported in Internet Explorer \(IE\). See [KB0683275](https://support.servicenow.com/kb_view.do?sysparm_article=KB0683275) for more details.

</td></tr><tr><td>

UI page

</td><td>

The UI modal dialog to be tested.**Note:** This field appears only if **Standard UI** is selected from **Form UI**.

</td></tr><tr><td>

Button

</td><td>

The ID attribute of the button element. For example, the **OK**button has an ID of `OK_button` in the UI modal dialog.**Note:** This field appears only if **Standard UI** is selected from **Form UI**.

</td></tr><tr><td>

Modal values

</td><td>

The field values to be set in the modal.**Note:** This field appears only if a workspace is chosen as **Form UI**.

</td></tr><tr><td>

Modal action

</td><td>

The action to be selected in the modal.**Note:** This field appears only if a workspace is chosen as **Form UI**.

</td></tr><tr><td>

Assert type

</td><td>

The effect on the tests on clicking the modal button.-   **Modal closed and page is reloaded or redirected**: The test passes only if the modal was closed and the page was reloaded or redirected to another page.
-   **Modal closed and page is not reloaded or redirected**: The test passes only if the modal was closed and the page was not reloaded or redirected to another page.
-   **Modal not closed**: The test passes only if the modal still exists and was not closed.

</td></tr><tr><td>

Assertion timeout

</td><td>

Number of seconds allowed before the assert fails. If the assert fails, the system repeats the assert until the duration of the Timeout is reached. If the validation fails after the Timeout duration has passed, the step fails.

</td></tr></tbody>
</table>**Note:** The Click Modal Button test step can't access the newly added UI workspace options.

## Click a UI Action

Click a UI action on the current form.

When this step runs, the system performs the action normally activated by that control. The test step also validates that the current form contains the control and that the control is visible and enabled. To run this step, your test must have already opened a form using either the **Open a New Form** or **Open an Existing Record** step. It is recommended to not run this step directly after a **Submit a Form** or **Click a UI Action** step. This is because they can redirect your test to a different page based on the navigation stack configuration on your instance or the script defined in the clicked UI action. Unless you are certain that the UI action will take you to a specific page, you should explicitly use an **Open a New Form** step after **Submit a Form** or **Click a UI Action** to ensure that the test is on the form as expected. Ensure that the test keeps passing consistently when added to a suite.

In the Zurich release, this step supports UI actions of type Form context menu.

**Note:** Don't write tests that depend on the system displaying a specific page after executing a **Submit a Form** or **Click a UI Action** step. After these test steps, the system returns to the page that was open before the form was opened. The test cannot determine what that page was, so writing a test that expects a particular page can lead to unpredictable results.

<table id="table_od3_dgb_hzb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Execution order

</td><td>

Integer specifying the order in which the test executes this step.As you create steps, the system automatically assigns each step an incremental value. This value causes the test to execute steps in the order that you created them in. You can change this default order by editing the **Execution order** values.

</td></tr><tr><td>

Active

</td><td>

Option to activate this test step for use.

</td></tr><tr><td>

Application

</td><td>

Application scope in which the system runs this step.

</td></tr><tr><td>

Test

</td><td>

Read-only name of the test that you're adding the step to.

</td></tr><tr><td>

Step config

</td><td>

Read-only name of the step.

</td></tr><tr><td>

Description

</td><td>

Description of the test step. This field value is automatically set based on the field values of the test step. This field appears after the test step is submitted.

</td></tr><tr><td>

Notes

</td><td>

Notes about the test step

</td></tr><tr><td>

Form UI

</td><td>

Option to select an available UI. Apart from the Standard UI, you have other workspace selections available. Depending on the selected workspace, the UI might vary.**Note:** Workspaces are not supported in Internet Explorer \(IE\). See [KB0683275](https://support.servicenow.com/kb_view.do?sysparm_article=KB0683275) for more details.

</td></tr><tr><td>

Table

</td><td>

Name of the table for the new form.

</td></tr><tr><td>

UI action

</td><td>

The UI action to click.**Note:** The declarative action and UI action buttons look exactly the same. Depending on the selected test step \(either Click a UI Action or Click a Declarative Action\), the type of button can be identified.

</td></tr><tr><td>

Assert type

</td><td>

The effect on the tests with clicking of a UI action.-   **Form submission canceled in browser**: The step passes only if form submission is canceled.
-   **Form submitted to server**: The step passes only if the form is submitted.

</td></tr></tbody>
</table>|Field|Description|
|-----|-----------|
|table|The table for the form that contains this UI action.|
|record|The sys\_id of the record on which the action was clicked.|

## Click a Declarative Action

Click a declarative action on the current form.

<table id="table_od3_dgb_hzb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Execution order

</td><td>

Integer specifying the order in which the test executes this step.As you create steps, the system automatically assigns each step an incremental value. This value causes the test to execute steps in the order that you created them in. You can change this default order by editing the **Execution order** values.

</td></tr><tr><td>

Active

</td><td>

Option to activate this test step for use.

</td></tr><tr><td>

Application

</td><td>

Application scope in which the system runs this step.

</td></tr><tr><td>

Test

</td><td>

Read-only name of the test that you're adding the step to.

</td></tr><tr><td>

Step config

</td><td>

Read-only name of the step.

</td></tr><tr><td>

Notes

</td><td>

Notes about the test step

</td></tr><tr><td>

Form UI

</td><td>

Option to select an available UI. Apart from the Standard UI, you have other workspace selections available. Depending on the selected workspace, the UI might vary.**Note:** Workspaces are not supported in Internet Explorer \(IE\). See [KB0683275](https://support.servicenow.com/kb_view.do?sysparm_article=KB0683275) for more details.

</td></tr><tr><td>

Table

</td><td>

Name of the table for the new form.

</td></tr><tr><td>

Declarative action

</td><td>

Option to select a declarative action from the list.**Note:** The declarative action and UI action buttons look exactly the same. Depending on the selected test step \(either Click a UI Action or Click a Declarative Action\), the type of button can be identified.

</td></tr><tr><td>

Assert type

</td><td>

The effect on the tests with clicking of a UI action.-   **Form submission canceled in browser**: The step passes only if form submission is canceled.
-   **Form submitted to server**: The step passes only if the form is submitted.

</td></tr></tbody>
</table>## Submit a Form

Submit the current form.

To run this step, your test must have already opened a form using either the **Open a New Form** or **Open an Existing Record** step. It is recommended to not run this step directly after a **Submit a Form** or **Click a UI Action** step. This is because they can redirect your test to a different page based on the navigation stack configuration on your instance or the script defined in the clicked UI action. Unless you are certain that the UI action will take you to a specific page, you should explicitly use an **Open a New Form** step after **Submit a Form** or **Click a UI Action** to ensure that the test is on the form as expected. Ensure that the test keeps passing consistently when added to a suite.

**Note:** Don't write tests that depend on the system displaying a specific page after executing a **Submit a Form** or **Click a UI Action** step. After these test steps, the system returns to the page that was open before the form was opened. The test cannot determine what that page was, so writing a test that expects a particular page can lead to unpredictable results.

A modal form appears either on top of another form or a list. To submit a modal form, your test must have already opened it on top of a form or a list.

![Add Test Step modal form.](../image/atf-modal-form.png)

<table id="table_od3_dgb_hzb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Execution order

</td><td>

Integer specifying the order in which the test executes this step.As you create steps, the system automatically assigns each step an incremental value. This value causes the test to execute steps in the order that you created them in. You can change this default order by editing the **Execution order** values.

</td></tr><tr><td>

Active

</td><td>

Option to activate this test step for use.

</td></tr><tr><td>

Application

</td><td>

Application scope in which the system runs this step.

</td></tr><tr><td>

Test

</td><td>

Read-only name of the test that you're adding the step to.

</td></tr><tr><td>

Timeout

</td><td>

Number of seconds allowed before the step fails. If the validation fails, the system repeats the step until it reaches the duration of the timeout. If the validation fails after the timeout duration has passed, the step fails.**Note:** This field appears when an available workspace is chosen from **Form UI**.

</td></tr><tr><td>

Step config

</td><td>

Read-only name of the step.

</td></tr><tr><td>

Description

</td><td>

Description of the test step. This field value is automatically set based on the field values of the test step. This field appears after the test step is submitted.

</td></tr><tr><td>

Notes

</td><td>

Notes about the test step

</td></tr><tr><td>

Form UI

</td><td>

Option to select an available UI. Apart from the Standard UI, you have other workspace selections available. Depending on the selected workspace, the UI might vary.**Note:** Workspaces are not supported in Internet Explorer \(IE\). See [KB0683275](https://support.servicenow.com/kb_view.do?sysparm_article=KB0683275) for more details.

</td></tr><tr><td>

Assert type

</td><td>

The effect on the tests on submitting a form.-   **Form submitted to server**: The step passes only if the form is submitted.
-   **Form submission canceled in browser**: The step passes only if form submission is canceled.
-   **None**: Make no assertion on submitting the form. The step always passes when using this assert type regardless of the result of submitting the form.

</td></tr></tbody>
</table>|Field|Description|
|-----|-----------|
|table|The table for the submitted record.|
|record|The sys\_id of the submitted record.|


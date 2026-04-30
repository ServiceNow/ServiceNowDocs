---
title: List and Related List
description: Validate the functionality and visibility of records and UI actions in lists and related lists.Validate the visibility of the selected related lists on a form.Apply a filter to a list to find the required record.Validate the presence of a record in a list. A valid form must be open and the list containing the record must be visible to proceed.Open a specific record in a list.Validate that a UI action is visible in a list. If you're impersonating a user, the visibility of a UI action can change depending on the user being impersonated.Select a list UI action in a list on a form.
locale: en-US
release: xanadu
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 6
breadcrumb: [Test step categories, Test your apps with the ATF, Testing and debugging applications, Building applications]
---

# List and Related List

Validate the functionality and visibility of records and UI actions in lists and related lists.

## Validate Related List Visibility

Validate the visibility of the selected related lists on a form.

<table id="table_vgk_zs4_nhb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Execution order

</td><td>

Integer specifying the order in which the test executes this step.As you create steps, the system automatically assigns each step an incremental value. This value causes the test to execute steps in the order that you created them. You can change this default order by editing the **Execution order** values.

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

Name of the test that you're adding the step to.

</td></tr><tr><td>

Step config

</td><td>

Name of the step.

</td></tr><tr><td>

Notes

</td><td>

Notes about the test step.

</td></tr><tr><td>

Table

</td><td>

Name of the table of the parent form where related list visibility is validated.

</td></tr><tr><td>

Visible

</td><td>

List of related lists to assert as visible.

</td></tr><tr><td>

Not visible

</td><td>

List of related lists to assert as not visible.

</td></tr></tbody>
</table>## Apply Filter to List

Apply a filter to a list to find the required record.

<table id="table_vgk_zs4_nhb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Execution order

</td><td>

Integer specifying the order in which the test executes this step.As you create steps, the system automatically assigns each step an incremental value. This value causes the test to execute steps in the order that you created them. You can change this default order by editing the **Execution order** values.

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

Name of the test that you're adding the step to.

</td></tr><tr><td>

Step config

</td><td>

Name of the step.

</td></tr><tr><td>

Notes

</td><td>

Notes about the test step.

</td></tr><tr><td>

List type

</td><td>

Option to select the type of list.-   **List**
-   **Related list**

</td></tr><tr><td>

Assert Type

</td><td>

Specifies the assertion on executing the test step:-   **At least one matching record found**: The step succeeds if there is at least one matching record.
-   **No matching record found**: The step fails if there is any matching record.
-   **One matching record found**: The step succeeds if there is exactly one matching record.

</td></tr><tr><td>

Table

</td><td>

If the **List type** is **List**, this field is the table of the opened list.

 If the **List type** is **Related list**, this field states the name of the table of the parent form where the list belongs.

</td></tr><tr><td>

Related List

</td><td>

The related list to apply a filter to.**Note:** This field is available when **Related list** is selected from **List type**.

</td></tr><tr><td>

List filter

</td><td>

Filter conditions to apply to the list.

</td></tr></tbody>
</table>|Field|Description|
|-----|-----------|
|first\_record|The first record found in the list after applying the indicated filter.|

## Validate Record Present in List

Validate the presence of a record in a list. A valid form must be open and the list containing the record must be visible to proceed.

<table id="table_vgk_zs4_nhb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Execution order

</td><td>

Integer specifying the order in which the test executes this step.As you create steps, the system automatically assigns each step an incremental value. This value causes the test to execute steps in the order that you created them. You can change this default order by editing the **Execution order** values.

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

Name of the test that you're adding the step to.

</td></tr><tr><td>

Timeout

</td><td>

Number of seconds allowed before the step fails. If the validation fails, the system repeats the step until it reaches the duration of the timeout. If the validation fails after the timeout duration has passed, the step fails.

</td></tr><tr><td>

Step config

</td><td>

Name of the step.

</td></tr><tr><td>

Notes

</td><td>

Notes about the test step.

</td></tr><tr><td>

List type

</td><td>

Option to select the type of list.-   **List**
-   **Related list**

</td></tr><tr><td>

Assert type

</td><td>

Specifies the assertion on executing the test step:-   **Record is present in the list**
-   **Record is not present in the list**

</td></tr><tr><td>

Table

</td><td>

Name of the parent table where the list belongs.

</td></tr><tr><td>

Related list

</td><td>

The related list which has the record to validate. **Note:** This field is available when **Related list** is selected from **List type**.

</td></tr><tr><td>

Record

</td><td>

The record whose presence is validated.

</td></tr></tbody>
</table>## Open a Record in List

Open a specific record in a list.

<table id="table_vgk_zs4_nhb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Execution order

</td><td>

Integer specifying the order in which the test executes this step.As you create steps, the system automatically assigns each step an incremental value. This value causes the test to execute steps in the order that you created them. You can change this default order by editing the **Execution order** values.

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

Name of the test that you're adding the step to.

</td></tr><tr><td>

Step config

</td><td>

Name of the step.

</td></tr><tr><td>

Notes

</td><td>

Notes about the test step.

</td></tr><tr><td>

List type

</td><td>

Option to select the type of list.-   **List**
-   **Related list**

</td></tr><tr><td>

Table

</td><td>

Name of the parent table where the list belongs.

</td></tr><tr><td>

Related List

</td><td>

The related list which has the record to open.**Note:** This field is available when **Related list** is selected from **List type**.

</td></tr><tr><td>

Record

</td><td>

The record to be opened.

</td></tr></tbody>
</table>## Validate List UI Action Visibility

Validate that a UI action is visible in a list. If you're impersonating a user, the visibility of a UI action can change depending on the user being impersonated.

<table id="table_vgk_zs4_nhb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Execution order

</td><td>

Integer specifying the order in which the test executes this step.As you create steps, the system automatically assigns each step an incremental value. This value causes the test to execute steps in the order that you created them. You can change this default order by editing the **Execution order** values.

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

Name of the test that you're adding the step to.

</td></tr><tr><td>

Step config

</td><td>

Name of the step.

</td></tr><tr><td>

Notes

</td><td>

Notes about the test step.

</td></tr><tr><td>

List type

</td><td>

Option to select the type of list.-   **List**
-   **Related list**

</td></tr><tr><td>

Table

</td><td>

Name of the table of the parent form.

</td></tr><tr><td>

Related List

</td><td>

The related list which has the UI actions. **Note:** This field is available when **Related list** is selected from **List type**.

</td></tr><tr><td>

Visible

</td><td>

List of UI actions to assert as visible.

</td></tr><tr><td>

Not visible

</td><td>

List of UI actions to assert as not visible.

</td></tr></tbody>
</table>## Click a List UI Action

Select a list UI action in a list on a form.

<table id="table_vgk_zs4_nhb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Execution order

</td><td>

Integer specifying the order in which the test executes this step.As you create steps, the system automatically assigns each step an incremental value. This value causes the test to execute steps in the order that you created them. You can change this default order by editing the **Execution order** values.

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

Name of the test that you're adding the step to.

</td></tr><tr><td>

Step config

</td><td>

Name of the step.

</td></tr><tr><td>

Notes

</td><td>

Notes about the test step.

</td></tr><tr><td>

List type

</td><td>

Option to select the type of list.-   **List**
-   **Related list**

</td></tr><tr><td>

Table

</td><td>

Name of the table where the UI action belongs.

</td></tr><tr><td>

Related list

</td><td>

The related list which has the UI actions.**Note:** This field is available when **Related list** is selected from **List type**.

</td></tr><tr><td>

List action

</td><td>

The list UI action to be clicked.

</td></tr><tr><td>

Action type

</td><td>

The type of UI action to be clicked.

</td></tr><tr><td>

Apply to

</td><td>

The record on which the UI action is applied.

</td></tr><tr><td>

Assert type

</td><td>

The assertion made by the step when executed. -   **None**: Click a UI action and continue without making an assertion.
-   **Page reloaded or redirected**: Click a UI action, and assert that the page was reloaded or redirected. This assert type doesn't assert form submission.

</td></tr><tr><td>

Record

</td><td>

The record to which the UI action is applied. **Note:** This field appears when you choose Single record in the **Apply to** field.

</td></tr></tbody>
</table>
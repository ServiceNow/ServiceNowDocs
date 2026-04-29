---
title: Server category
description: Perform server-side operations. For example, query and update a record, impersonate a user, or run a server-side script. Create a user with specified roles and groups for the test. The user record gets rolled back after the test completes.Impersonate the specified user for the test.Searches for a catalog item or record producer in the specified catalog and category. You can perform this step both in Platform and Service Portal.Query the database to verify that a record exists matching the conditions set in this step.Inserts a record into a table with the field values you specify.Changes field values on a record on the server.Deletes a specified record in a table.Validates that a record meets the specified conditions on the server side.Executes a script on the server.Get the item and requester from an existing request item, add the item to a new cart for that user, and place an order.Logs a message and stores it as a step result.Add one or more mandatory attachments to the specified record. Use Upload Attachments to select from the attachments the test step adds to the record.Submits the cart and generates a request. You can perform this step both in the ServiceNow AI Platform and Service Portal.Provides an example of scripts for a custom step configuration.
locale: en-US
release: australia
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 21
breadcrumb: [Automated Test Framework \(ATF\) test step categories, Automated Test Framework \(ATF\), Testing and debugging applications, Building applications]
---

# Server category

Perform server-side operations. For example, query and update a record, impersonate a user, or run a server-side script.

## Create a User

Create a user with specified roles and groups for the test. The user record gets rolled back after the test completes.

<table id="table_upr_ww4_nhb"><thead><tr><th>

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

First name

</td><td>

First name of the user.

</td></tr><tr><td>

Last name

</td><td>

Last name of the user.

</td></tr><tr><td>

Roles

</td><td>

Assigned roles of the user.

</td></tr><tr><td>

Groups

</td><td>

Assigned groups of the user.

</td></tr><tr><td>

Impersonate this user

</td><td>

Option to impersonate the new user.

</td></tr></tbody>
</table>|Field|Description|
|-----|-----------|
|user|The user ID of the user impersonated.|

## Impersonate

Impersonate the specified user for the test.

**Impersonate** specifies a user for executing subsequent steps in this test. It works for both server-side and browser-side steps and stays in effect until changed with another **Impersonate** step or until the test ends. The impersonation automatically ends when the test is over.

**Note:**

-   Do not impersonate a user with the test author role. Doing so can lead to conflicts that interfere with executing the test.
-   Tests which involve impersonated users which no longer exist fail.

    **Tip:** It is recommended to create a new user to avoid data dependencies. See [Create a User](test-steps-server-category.md#), for more information.

-   Do not rely on user IDs being consistent across different instances. The system dynamically assigns users IDs, so the ID for a particular user often differs from one instance to the next.
-   When exporting and importing automated tests, keep in mind that update sets do not update the user field.
-   Tests can impersonate users with the snc\_external role, which allows testing users who do not have login access. See [Explicit Roles](https://www.servicenow.com/docs/access?context=explicit-roles&version=australia&pubname=australia-platform-security&ft:locale=en-US) for requirements of the snc\_external role.

<table id="nn4_pvy_rw"><thead><tr><th>

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

User

</td><td id="atf-user">

The user ID for the test to impersonate.

</td></tr></tbody>
</table>|Field|Description|
|-----|-----------|
|user|The user ID of the user impersonated.|

## Search for a Catalog Item

Searches for a catalog item or record producer in the specified catalog and category. You can perform this step both in Platform and Service Portal.

<table id="table_amy_rx2_xz"><thead><tr><th>

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

Search in Portal only

</td><td id="atf-search-portal-only">

Selected if the search is restricted to the Service Portal only. Otherwise, not selected.

</td></tr><tr><td>

Search term

</td><td id="atf-search-term">

Term used to search for a catalog item.

</td></tr><tr><td>

Catalog

</td><td id="atf-catalog">

Catalog in which to search for the catalog item.

</td></tr><tr><td>

Category

</td><td id="atf-category">

Category in which to search for the catalog item.

</td></tr><tr><td>

Assert item

</td><td id="atf-server-assert-item">

Catalog items that should be available in the search results.

</td></tr><tr><td>

Assert Type

</td><td id="atf-server-assert-type">

Specifies how searching the catalog item affects the test:-   **Assert Item present in search result**: Test passes only if the assert item is present in the search result.
-   **Assert Item not present in search result**: Test passes only if the assert item is not present in the search result.

</td></tr></tbody>
</table>|Field|Description|
|-----|-----------|
|catalog\_item\_id|The sys\_id of the first catalog item found that the user can view.|

## Record Query

Query the database to verify that a record exists matching the conditions set in this step.

<table><thead><tr><th>

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

Enforce security

</td><td id="atf-record-query-enforce-security">

Selected to enforce ACLs. Otherwise, not selected.

</td></tr><tr><td>

Notes

</td><td id="atf-notes-condition-builder">

Notes about the test step.**Note:** Use the condition builder to set the field value. The condition builder displays an appropriate control for the field data type. For example, a reference field displays a **Lookup record** control.

</td></tr><tr><td>

Assert type

</td><td id="atf-record-query-assert-type">

Specifies how querying the record affects the test:-   **There is at least one record matching the query**: The test fails if there are no records matching the query.
-   **No records match the query**: The test fails if any records match the query.

</td></tr><tr><td>

Table

</td><td id="atf-server-table">

The table to be queried.

</td></tr><tr><td>

Conditions

</td><td id="atf-server-conditions">

Conditions used to run the query.

</td></tr></tbody>
</table>|Field|Description|
|-----|-----------|
|table|The table queried.|
|first\_record|The first record resulting from the query.|

**Note:** If you don’t update your record query test step, the original record query test step still functions the same way as before, irrespective of it being termed as **\(Deprecated\)**.

## Record Insert

Inserts a record into a table with the field values you specify.

<table><thead><tr><th>

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

Assert type

</td><td id="atf-record-insert-assert-type">

Specifies how inserting the record affects the test:-   **Record successfully inserted**: Test fails if the record was not successfully inserted.
-   **Record was not inserted**: Test fails if the record was successfully inserted.

</td></tr><tr><td>

Enforce security

</td><td id="atf-record-insert-enforce-security-q">

Selected to enforce ACLs and the read-only role. Otherwise, not selected.

</td></tr><tr><td>

Table

</td><td id="atf-record-insert-table">

The table into which the record should be inserted.

</td></tr><tr><td>

Conditions

</td><td id="atf-record-insert-conditions">

Specific field values to be set when the test runs this step.

</td></tr></tbody>
</table>|Field|Description|
|-----|-----------|
|table|The table to which the new record belongs.|
|record\_id|The sys\_id of the new record.|

## Record Update

Changes field values on a record on the server.

**Note:** To ensure that the changes were applied, follow this step with a **Record Validation** step.

<table><thead><tr><th>

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

Assert type

</td><td id="atf-record-update-assert-type">

Specifies how updating the record affects the test:-   **Record successfully updated**: Test fails if the record was not successfully updated.
-   **Record was not updated**: Test fails if the record was successfully updated.

</td></tr><tr><td>

Enforce security

</td><td id="atf-record-insert-enforce-security-q">

Selected to enforce ACLs and the read-only role. Otherwise, not selected.

</td></tr><tr><td>

Table

</td><td id="atf-record-update-table">

The table containing the record to be updated.

</td></tr><tr><td>

Record

</td><td id="atf-record-update-record">

ID of the record to be updated.

</td></tr><tr><td>

Field values

</td><td>

Fields for which you want to set values and the values you want to set for those fields.**Note:** Use the condition builder to set the field value. The condition builder displays an appropriate control for the field data type. For example, a reference field displays a **Lookup record** control.

</td></tr></tbody>
</table>**Note:** Record Update step succeeds even if a field on the record is blocked by ACL. Use the [Record Validation](test-steps-server-category.md#) step after Record Update to check whether a particular field was modified, or use the [Form steps](test-steps-form-category.md#) to evaluate ACL conditions for individual fields on a record.

## Record Delete

Deletes a specified record in a table.

<table><thead><tr><th>

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

Assert type

</td><td id="atf-record-delete-assert-type">

Specifies how updating the record affects the test:-   **Record successfully deleted**: Test fails if the record was not successfully deleted.
-   **Record was not deleted**: Test fails if the record was successfully deleted.

</td></tr><tr><td>

Enforce security

</td><td id="atf-record-insert-enforce-security-q">

Selected to enforce ACLs and the read-only role. Otherwise, not selected.

</td></tr><tr><td>

Table

</td><td id="atf-record-delete-table">

The table containing the record to be deleted.

</td></tr><tr><td>

Record

</td><td id="atf-record-delete-record">

ID of the record to be deleted.

</td></tr></tbody>
</table>## Record Validation

Validates that a record meets the specified conditions on the server side.

For the **Record Validation** step, specify the values you want to test using the standard conditions builder. You can apply several conditions to the same field.

This step passes if the overall condition is satisfied and fails if it is not. If you need to test the values of individual fields independently of each other, include a separate **Record Validation** step for each value to be tested.

<table id="dt4_kjz_rw"><thead><tr><th>

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

</td><td id="atf-notes-condition-builder">

Notes about the test step.**Note:** Use the condition builder to set the field value. The condition builder displays an appropriate control for the field data type. For example, a reference field displays a **Lookup record** control.

</td></tr><tr><td>

Assert type

</td><td id="atf-record-valid-assert-type">

Specifies how validating the record affects the test:-   **Record successfully validated**: The test fails if the record does not match the conditions.
-   **Record not found**: Test fails if the record is found.

</td></tr><tr><td>

Table

</td><td id="atf-record-valid-table">

The table that contains the field to be validated.

</td></tr><tr><td>

Record

</td><td id="atf-record-valid-record">

The record that contains the field to be validated.

</td></tr><tr><td>

Field values

</td><td id="atf-record-valid-field-values">

Specific fields to be validated when the test runs this step.

</td></tr></tbody>
</table>## Run Server Side Script

Executes a script on the server.

<table><thead><tr><th>

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

Jasmine version

</td><td id="atf-jasmine-version">

The version of the Jasmine testing framework to use for running the server-side script. Any new scripts you create use Jasmine version 3.1. Your existing scripts can continue to use Jasmine version 1.3, or you can upgrade them to Jasmine version 3.1.

</td></tr><tr><td>

Test script

</td><td id="atf-test-script-new">

The javascript for the server to execute. Supports the Jasmine testing framework.**Note:** steps\(SYS\_ID\) can be defined as a function to retrieve Output variable data from a step that executed earlier in the test.

 The Run Server Side Script test step now supports parameters as step inputs.

</td></tr></tbody>
</table>|Field|Description|
|-----|-----------|
|record\_id|The sys\_id output by the server-side script.|
|table|The table output by the server-side script.|

**Note:** If the script creates data, the system rolls back that data after all steps in the test finish. The output for the Run Server Side Script test step now indicates the line and the line number for the cause of failure.

-   Test script

    ```
    //  Test step 1 - add data
    var now_GR = new GlideRecord('sc_task');
    //  this sample step's Step config has Output variables named table and record_id
    outputs.table = 'sc_task';
    outputs.record_id = gr.insert();
    //  Test step 2 - access added data and validate
    //  check that the record exists (or that business logic changed it)
    var now_GR = new GlideRecord("sc_task");
    gr.get(steps(PREVIOUS_STEP_SYS_ID).record_id);
    assertEqual({name: "task gr exists", shouldbe: true, value: gr.isValidRecord()});
    stepResult.setOutputMessage: Log a message to step results after step executes.
                                 Can only be called once or will overwrite previous message
    ```

-   Create a suite of test scripts

    ```
    var now_GR = new GlideRecord('sc_task');
    gr.setValue('short_description', 'verify task can be inserted');
    var grSysId = gr.insert();
    var justCreatedGR = new GlideRecord('sc_task');
    if (justCreatedGR.get(grSysId)) {
    stepResult.setOutputMessage("Successfully inserted task record");
    return true; // pass the step
    } else { 
    stepResult.setOutputMessage("Failed to insert task record");
    return false; // fail the step
    }
    ```

-   Jasmine test

    ```
    describe('my suite of script tests', function() {
    it('should meet expectations', function() {
    expect(true).not.toBe(false);
    });
    });
    //  make sure to uncomment jasmine.getEnv().execute(); outside the function body
    assertEqual: A function used to compare that assertion.shouldbe == assertion.value;
    in case of failure it throws an Error and logs that the assertion by name has failed
    ```

    **Note:** `describe` is only supported in Global scope. Use `describe` to create a suite of test scripts and `it` to define test expectations.

-   Logs message to test step output

    ```
    var testAssertion = {
    name: "my test assertion",
    shouldbe: "expected value"
    value: "actual value",
    };
    assertEqual(testAssertion); // throws Error, logs message to test step output
    ```

-   See [Step Execution Scripts](../concept/atf-config-script.md) for Run Server Side script example.

## Replay Request Item

Get the item and requester from an existing request item, add the item to a new cart for that user, and place an order.

<table><thead><tr><th>

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

Original Request Item

</td><td id="atf-original-request-item">

The request item to be replayed.

</td></tr></tbody>
</table>|Field|Description|
|-----|-----------|
|table|The table to which the replayed request item belongs.|
|request|The replayed request item.|

**Related topics**  


[Automated Test Framework use case: test a Service Catalog request](../task/atf-serv-cat-use.md)

## Log

Logs a message and stores it as a step result.

The log message can contain variables and other information pertaining to the test. The message is stored as a step result.

<table id="table_ek1_y42_kfb"><thead><tr><th>

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

Log

</td><td id="atf-log">

The message to be logged. To include the value of an output variable from a previous step, click the input value icon \(![Input value icon](../image/rem-value-icon.png)\) and follow the procedure to [Pass values from one automated test step to another](../task/atf-retrieve-value.md).

</td></tr></tbody>
</table>## Add Attachments to Existing Record

Add one or more mandatory attachments to the specified record. Use **Upload Attachments** to select from the attachments the test step adds to the record.

<table id="table_upr_ww4_nhb"><thead><tr><th>

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

Valid table selection from the list.

</td></tr><tr><td>

Record

</td><td>

Pre-existing record either from before the test or inserted as a part of the test.

</td></tr><tr><td>

Upload Attachments

</td><td>

Button to add one or more mandatory attachments to the record.

</td></tr></tbody>
</table>## Checkout Shopping Cart

Submits the cart and generates a request. You can perform this step both in the ServiceNow AI Platform and Service Portal.

<table id="table_p3s_mnw_tcb"><thead><tr><th>

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

Assert Type

</td><td id="atf-checkout-assert-type">

Criteria for the test to pass.-   **Empty cart**

Test fails if the cart is not empty.

-   **Successfully Checkout cart**

Test fails if the cart is not successfully checked out.


</td></tr><tr><td>

Requested For

</td><td id="atf-requested-for">

User for whom the request is generated.

</td></tr><tr><td>

Delivery Address

</td><td id="atf-delivery-address">

Delivery address for the request.

</td></tr><tr><td>

Special Instructions

</td><td id="atf-special-instructions">

Special instructions for the request.

</td></tr></tbody>
</table>|Field|Description|
|-----|-----------|
|request\_id|The sys\_id of the submitted request.|

## Custom Scripted StepConfig

Provides an example of scripts for a custom step configuration.

This example checks if the user name provided starts with the letter A. This step is useful primarily to users with the \[atf\_test\_admin\] role. Users with the \[atf\_test\_admin\] role can view the example scripts by opening the record for this step in [Step configurations](../concept/step-configurations-module.md).

<table id="table_dd3_bp2_kfb"><thead><tr><th>

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

User

</td><td id="atf-custom-script-user">

The user whose name the system checks to see if it starts with the letter **A**. To include the value of an output variable from a previous step, click the input value icon \(![Input value icon](../image/rem-value-icon.png)\) and follow the procedure to [Pass values from one automated test step to another](../task/atf-retrieve-value.md).

</td></tr></tbody>
</table>|Field|Description|
|-----|-----------|
|value|The name of the user.|

**Related topics**  


[Create custom step configuration](../task/atf-create-custom-step.md)

[Step execution scripts](../concept/atf-config-script.md)

[Step description generation script](../concept/atf-config-desc-script.md)


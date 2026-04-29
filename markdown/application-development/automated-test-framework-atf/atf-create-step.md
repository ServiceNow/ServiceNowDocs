---
title: Add steps to an automated test
description: Create a series of steps for an automated test to run in a specified order.
locale: en-US
release: australia
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Create a new automated test, Building and running automated tests with the Automated Test Framework, Automated Test Framework \(ATF\) test building and execution, Automated Test Framework \(ATF\), Testing and debugging applications, Building applications]
---

# Add steps to an automated test

Create a series of steps for an automated test to run in a specified order.

## Before you begin

You must create a test before you can add steps to the test.

Role required: atf\_test\_admin or atf\_test\_designer

## About this task

This procedure lets you add one step at a time. You can also add a batch of steps at once. For more information, see [Add a predefined list of steps \(template\) to an automated test](atf-use-template.md).

## Procedure

1.  Navigate to **All** &gt; **Automated Test Framework** &gt; **Tests**.

2.  Click the test that should contain the new test steps.

3.  In the Test Steps related list at the bottom of the Test form, click **Add Test Step**.

4.  From the left panel of the Add Test Step form, select the test step category, or select **All Steps** to view all available test steps for all test categories.

    For example, if selecting a specific test step category, select **Form** for form-related test steps, **Application Navigator** to test application menu or module visibility, or **Server** for tests executed on the server.

    **Note:** When selecting certain types of server tests, you can specify whether a positive or negative test result constitutes a successful test outcome. For more information, see Assert type in [Exploring Automated Test Framework](../concept/automated-test-framework.md).

5.  Click the type of test step you want to select.

    For example, if you select the **Form** category, select **Set Field Values** to set the field values on a form.

    Start any sequence of steps that work with forms with the **Open a new form** or **Open an existing form** step. Close with the **Submit form** step.

6.  If applicable, from the **Insert after** drop-down list, select the step that you want to precede this step.

    If this is the first step in a test, the **Insert after** drop-down list does not appear.

7.  Click **Next**.

8.  From the **Table** list on the Add Test Step form, select the table that you want to test in this step.

9.  In the **Execution Order** field, enter an integer representing the order in which you want the test to execute this step.

    For more information on **Execution Order**, see [Edit automated test step order](atf-edit-step-order.md).

10. Fill in the fields that apply to this step.

    For instructions, see [Automated Test Framework \(ATF\) test step categories](../reference/test-step-categories.md).

    Some steps return output values that you can pass to the inputs for a subsequent step. For more information, see [Pass values from one automated test step to another](atf-retrieve-value.md).

11. Click **Submit**.

    The system creates the step and displays the test record.

12. Repeat Steps 3 through 11 to add additional steps for this test.


## What to do next

[Run an automated test](atf-run-test.md).

**Parent Topic:**[Create a new automated test](atf-create-test.md)

**Related topics**  


[Automated Test Framework use case examples](../concept/atf-use-cases.md)


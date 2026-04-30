---
title: Add a predefined list of steps \(template\) to an automated test
description: With test templates you can add a predefined list of steps to a test. Any list of steps that follows a set pattern makes a good candidate for a template.
locale: en-US
release: xanadu
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Create a new automated test, Building and running automated tests with the Automated Test Framework, Test your apps with the ATF, Testing and debugging applications, Building applications]
---

# Add a predefined list of steps \(template\) to an automated test

With test templates you can add a predefined list of steps to a test. Any list of steps that follows a set pattern makes a good candidate for a template.

## Before you begin

You must have created the test to which you want to add steps.

Role required: atf\_test\_admin or atf\_test\_designer

## About this task

Many tests follow similar patterns. One common pattern, for example, is to open a form, set some field values, validate some field values, click a UI action, and submit the current form. If a template exists containing these steps, you can add them to a test all at once. The Automated Test Framework comes with default templates. You can also [create custom test templates](atf-create-template.md).

## Procedure

1.  Navigate to **All** &gt; **Automated Test Framework** &gt; **Tests**.

2.  Click the row for the test to which you want to add steps.

    The system displays the Test form.

3.  On the **Test Steps** related list, click **Add Test Template**.

    The system displays the **Add a test template** dialog.

    ![Image showing the test template](../image/atf-predefined-steps.png)

4.  From the **Table** field, select the table you want to test with these steps.

5.  From the **Template** field, select the template containing the steps you want to add.

6.  Click **Add**.

    The system adds the template steps to the test. It also adds to the test description a set of instructions on how to complete the test from this template.

7.  Following the instructions in the test description, edit each step added by the template to include the necessary information.


## What to do next

Proceed to edit or save the test as you normally would.

**Parent Topic:**[Create a new automated test](atf-create-test.md)

**Related topics**  


[Create an automated test steps template](atf-create-template.md)


---
title: Add a parameter to a test step
description: Add a variable to a test step to hold a particular type of data when the test runs.
locale: en-US
release: xanadu
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Parameterized tests, Building and running automated tests with the Automated Test Framework, Test your apps with the ATF, Testing and debugging applications, Building applications]
---

# Add a parameter to a test step

Add a variable to a test step to hold a particular type of data when the test runs.

## Before you begin

-   [Create a parameterized test](create-parameterized-test.md)
-   Role required: atf\_test\_admin, atf\_test\_designer, or admin

## About this task

**Note:** The Run Server Side Script test step is not supported in parameterized tests.

## Procedure

1.  Navigate to **All** &gt; **Automated Test Framework** &gt; **Tests**.

2.  Open a parameterized test.

3.  In the Test Steps related list, create a test step or open an existing step.

4.  Click ![Picker icon](../image/rem-value-icon.png) and select a parameter to add it to a field.

    The parameter displays in the field.

    ![Selected parameters in the Incident form.](../image/selected-parameter.png)


## Result

When the test runs, Automated Test Framework replaces the parameter with test run data.

## What to do next

[Add parameterized data sets](add-parameterized-data.md).

**Parent Topic:**[Parameterized tests](../concept/parameterized-tests.md)


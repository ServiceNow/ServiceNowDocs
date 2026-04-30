---
title: Create a parameterized test
description: Build a test that uses variables to store test data.
locale: en-US
release: xanadu
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Parameterized tests, Building and running automated tests with the Automated Test Framework, Test your apps with the ATF, Testing and debugging applications, Building applications]
---

# Create a parameterized test

Build a test that uses variables to store test data.

## Before you begin

Role required: atf\_test\_admin, atf\_test\_designer, or admin

## Procedure

1.  Navigate to **All** &gt; **Automated Test Framework** &gt; **Tests**.

2.  Click **New**.

    A blank Test record opens.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Enter a name for the test.|
    |Active|Enable|
    |Enable parameterized testing|Enable|
    |Description|Enter a description for the test.|

4.  Click **Save.**

    Parameterized testing related lists appear.

5.  Create a parameter to hold test run data.

    A parameter is a variable that stores a particular type of test data. Each parameter has a unique label and a data type. For example, you can create a parameter to store the Sys ID of a reference field or the integer value of a choice field.

    1.  In the Parameter Definitions related list, add a parameter.

        -   **Add Exclusive Parameters**: Adds a parameter available to this test only.
        -   **Add Shared Parameters**: Adds a parameter available to any parameterized test.
    2.  Define the name of the variable and the data type.

        When creating parameters for a form, the parameter data type must match the field data type. For example, if you are creating a parameter to test a reference field on a form, you must create a parameter of type Reference. For more information on ServiceNow AI Platform data types, see [Field types](https://www.servicenow.com/docs/access?context=r_FieldTypes&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

    3.  Click **Submit**.


## What to do next

[Add a parameter to a test step](add-parameterized-value-to-step.md)

**Parent Topic:**[Parameterized tests](../concept/parameterized-tests.md)


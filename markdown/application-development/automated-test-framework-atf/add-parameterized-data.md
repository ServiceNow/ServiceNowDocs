---
title: Add parameterized data sets
description: Add or import test data to specify parameter runtime values.
locale: en-US
release: australia
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Parameterized tests, Building and running automated tests with the Automated Test Framework, Automated Test Framework \(ATF\) test building and execution, Automated Test Framework \(ATF\), Testing and debugging applications, Building applications]
---

# Add parameterized data sets

Add or import test data to specify parameter runtime values.

## Before you begin

-   [Create a parameterized test](create-parameterized-test.md)
-   [Add a parameter to a test step](add-parameterized-value-to-step.md)
-   Role required: atf\_test\_admin, atf\_test\_designer, or admin

## About this task

A data set, also known as a test run data set, includes runtime data used when the test runs. You can set a value for every parameter available to the current test. Data sets specify the parameter value during test runs.

Test designers can add data sets manually, or import data from a file.

**Note:** If you create a parameterized test that includes Custom UI test steps, the system only uses the first data set to retrieve components.

## Procedure

1.  Navigate to **All** &gt; **Automated Test Framework** &gt; **Tests**.

2.  Open a parameterized test.

3.  In the Test Run Data Sets related list, add or import data sets.

<table id="choicetable_ndb_zsg_5fb"><thead><tr><th align="left" id="d199624e113">

Option

</th><th align="left" id="d199624e116">

Description

</th></tr></thead><tbody><tr><td id="d199624e122">

**Add**

</td><td>

The New Parameter Value Set form opens. This form includes all parameters available to the current test.

 1.  Define the **Order** field to set the order in which data sets run.
2.  Specify the parameter value when the test runs.
3.  Click **Submit**.


</td></tr><tr><td id="d199624e153">

**Import**

</td><td>

The Import Test Run Data Sets form opens.

 1.  Define the import behavior.
    -   **Add**: Adds the data in the file to existing test run data sets in the Test Run Data Sets table. For more information, see [Add a record in the template](https://www.servicenow.com/docs/access?context=t_AddARecordInTheTemplate&version=australia&pubname=australia-integrate-applications&ft:locale=en-US).
    -   **Replace**: Downloads a template that includes any existing data sets in the Test Run Data Sets table. Replaces all existing data sets that have matching Sys IDs in the Test Run Data Sets table with data from the uploaded file. For more information, see [Update a record in the template](https://www.servicenow.com/docs/access?context=t_UpdateARecordInTheTemplate&version=australia&pubname=australia-integrate-applications&ft:locale=en-US).
2.  In the Upload Test Run Data File section, select **Yes** to download an Excel template with the required fields, then upload a completed file. Alternately, select **No** to upload a completed file.
 Each row in the file becomes an entry in the Test Run Data Sets table.

</td></tr></tbody>
</table>
## What to do next

Click **Run Test**. Automated Test Framework runs each parameterized test once per data set, using the same test steps and execution order. For example, if a parameterized test has five data sets, Automated Test Framework runs the test five times, once for each data set.

Parameterized tests display test results by the execution order of the data sets. Open each test result record to view the test details.

**Parent Topic:**[Parameterized tests](../concept/parameterized-tests.md)


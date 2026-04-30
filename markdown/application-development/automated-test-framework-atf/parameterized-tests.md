---
title: Parameterized tests
description: Run a test multiple times with different test data for each run. Create parameters to store test data for each test run.
locale: en-US
release: zurich
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Building and running automated tests with the Automated Test Framework, Test building and execution, Automated Test Framework \(ATF\), Testing and debugging applications, Building applications]
---

# Parameterized tests

Run a test multiple times with different test data for each run. Create parameters to store test data for each test run.

Parameterized testing offers test designers these benefits.

-   Eliminates the need to duplicate test steps just to change test data.
-   Increases test reuse by separating test actions from test data.
-   Produces a separate test result for each data set.

When the test runs, Automated Test Framework replaces the parameters with data set values. For example, you can create a test of the incident form that uses parameter values for the subcategory and priority fields. You can use one data set to test that the Antivirus category produces a high priority incident, and another data set to test that the Email category produces a low priority incident.

**Note:** The Run Server Side Script test step is not supported in parameterized tests.

## Parameterized test components

Parameterized tests consist of these components.

-   **Parameter**

    A parameter is a variable that stores a particular type of test data. Each parameter has a unique label and a data type. For example, you can create a parameter to store the Sys ID of a reference field or the integer value of a choice field. Define parameters during test design.

    Parameters can be shared or exclusive. Shared parameters can be used in any parameterized test. Exclusive parameters can only be used with the test for which they were created. Each shared parameter is a column in the Test Run Data Sets \[sys\_atf\_parameter\_set\] table. Each exclusive parameter is a record in the Parameter Variables \[sys\_atf\_parameter\_variable\] table.

-   **Data set**

    A data set, also known as a test run data set, includes runtime data used when the test runs. You can set a value for every parameter available to the current test. Data sets specify the parameter value during test runs. You can manually create data sets for a test, or import data from a file. Each data set is a record in the Test Run Data Sets \[sys\_atf\_parameter\_set\] table.

    Parameterized tests fail if data sets are not defined.


## Design Considerations

Follow these design considerations when creating parameterized tests.

-   Parameterized tests support standard Automated Test Framework features, such as reports, test suites, and data rollback. Copying a parameterized test copies all parameters, test run data sets, and test steps.
-   If you create a parameterized test that includes Custom UI test steps, the system only uses the first data set to retrieve components.

## Parameterized test runs

Automated Test Framework runs each parameterized test once per data set, using the same test steps and execution order. For example, if a parameterized test has five data sets, Automated Test Framework runs the test five times, once for each data set.

## Parameterized test results

Parameterized tests display test results by the execution order of the data sets. Open each test result record to view the test details.

![Parameterized test results display multiple records.](../image/param-test-result.png)

The Parameterized Test Result record **Description** field lists the parameters and data sets used in the test run.

-   **[Create a parameterized test](../task/create-parameterized-test.md)**  
Build a test that uses variables to store test data.
-   **[Add a parameter to a test step](../task/add-parameterized-value-to-step.md)**  
Add a variable to a test step to hold a particular type of data when the test runs.
-   **[Add parameterized data sets](../task/add-parameterized-data.md)**  
Add or import test data to specify parameter runtime values.

**Parent Topic:**[Building and running automated tests with the Automated Test Framework](atf-build-overview.md)


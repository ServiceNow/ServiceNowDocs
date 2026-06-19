---
title: Add a parameter to a test step
description: Add a variable to a test step to hold a particular type of data when the test runs.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/automated-test-framework-atf/add-parameterized-value-to-step.html
release: australia
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Parameterized tests, Building and running automated tests with the Automated Test Framework, Automated Test Framework \(ATF\) test building and execution, Automated Test Framework \(ATF\), Testing and debugging applications, Building applications]
---

# Add a parameter to a test step

Add a variable to a test step to hold a particular type of data when the test runs.

## Before you begin

-   [Create a parameterized test](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/automated-test-framework-atf/create-parameterized-test.md)
-   Role required: atf\_test\_admin, atf\_test\_designer, or admin

## About this task

**Note:** The Run Server Side Script test step is not supported in parameterized tests.

## Procedure

1.  Navigate to **All** &gt; **Automated Test Framework** &gt; **Tests**.

2.  Open a parameterized test.

3.  In the Test Steps related list, create a test step or open an existing step.

4.  Click \[Omitted image "rem-value-icon.png"\] Alt text: Picker icon and select a parameter to add it to a field.

    The parameter displays in the field.

    \[Omitted image "selected-parameter.png"\] Alt text: Selected parameters in the Incident form.


## Result

When the test runs, Automated Test Framework replaces the parameter with test run data.

## What to do next

[Add parameterized data sets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/automated-test-framework-atf/add-parameterized-data.md).

**Parent Topic:**[Parameterized tests](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/automated-test-framework-atf/parameterized-tests.md)


---
title: Executing the tests using Cloud Runner
description: Execute the generated tests suite using the Cloud Runner browser option.
locale: en-US
release: zurich
product: ATF Test Generator and Cloud Runner
classification: atf-test-generator-and-cloud-runner
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Use, ATF Test Generator and Cloud Runner, Extend ServiceNow AI Platform capabilities]
---

# Executing the tests using Cloud Runner

Execute the generated tests suite using the Cloud Runner browser option.

## Before you begin

**Note:** ATF test data will temporarily be in the browser session which are stored in our ServiceNow data center. Test data will be removed after all test executions have been completed.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Automated Test Framework \(ATF\)** &gt; **Suites** &gt; **ATF Generated Suite**.

    **Note:** You can also execute an individual test. Navigate to **All** &gt; **Automated Test Framework \(ATF\)** &gt; **Tests**.

2.  Select **Run Test Suite** to execute the selected suite.

    **Note:** You can also execute an individual test using the cloud runner browser option.

    The Pick a Browser dialog box shows up.

3.  Select one of the two available options to run the test suite.![Image showing the test execution with Cloud Runner option](../image/atf-tg-cr-execute-tests.png)

    -   Start a new test runner: Runs the test by starting a new tab
    -   Cloud Runner: Runs the test in the cloud

        **Note:** As an admin user, you can hide the Cloud Runner option on the Pick a browser dialog box by setting the atf\_cloud\_runner.radio\_visible to false. The property is set to true by default.

    **Note:** If you run a test suite using the cloud runner, all the tests within the suite run in parallel. See [Parallel testing using Cloud Runner](../concept/atf-tg-cr-parallel-test.md) for more information. The order in which the tests in a suite run is random. The parallel suites ignore the execution order and ignore abort on failure.

4.  Select **Run Test Suite** on the dialog box after selecting the browser.

    **Note:** The number of cloud runners that can be used simultaneously is two by default. You also have the option of buying five more cloud runners.

    The execution of the tests continues at the background even if you close the progress bar.

5.  Select **Go to Result** if you want to review the tests execution results.


-   **[Parallel testing using Cloud Runner](../concept/atf-tg-cr-parallel-test.md)**  
Parallel testing using the Cloud Runner involves execution of tests within a suite in parallel.

**Parent Topic:**[Using ATF Test Generator and Cloud Runner](../concept/atf-tg-cr-use.md)

**Related topics**  


[Scheduling test execution](atf-tg-cr-schedule-test-run.md)


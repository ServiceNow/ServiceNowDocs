---
title: Debug an automated test using breakpoints
description: Pause a test to troubleshoot failures or unexpected behavior by adding a breakpoint for a particular test step.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/application-development/automated-test-framework-atf/atf-breakpoint.html
release: zurich
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Implementing breakpoints, Building and running automated tests with the Automated Test Framework, Test building and execution, Automated Test Framework \(ATF\), Testing and debugging applications, Building applications]
---

# Debug an automated test using breakpoints

Pause a test to troubleshoot failures or unexpected behavior by adding a breakpoint for a particular test step.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Automated Test Framework \(ATF\)** &gt; **Tests**.

2.  Select the test you want to run.

3.  Select Test Steps related list to list out all the test steps for the selected test.

4.  Right-click the test step where you want to add or remove a breakpoint.

5.  Select Add/Remove Breakpoint from the list.

    \[Omitted image "atf-add-breakpoint.png"\] Alt text: Image showing how to add a breakpoint

    The test step gets marked for the modified breakpoint.

    **Note:** The breakpoint mark on a step states that if the breakpoint is active and the test is run using **Debug Test**, the test pauses just before the breakpoint test step. The breakpoints are not considered if you click **Run Test** to run the test.

    The breakpoints you set on a test are user-specific. Other users can't see and modify your breakpoints on a test, and vice versa.

    \[Omitted image "atf-multiple-breakpoints.png"\] Alt text: Image showing multiple breakpoints

    **Note:** You can set multiple breakpoints for a test but can have only 1 breakpoint every test step.

6.  Click the Breakpoint related list to show all the test steps within a test that have breakpoints.

7.  Click **Debug Test** to run the test with breakpoints.

    The Debug Test modal displays.\[Omitted image "atf-debug-test-modal.png"\] Alt text: Image showing debug test modal

    -   Safari – the browser used to run the client-side steps of the selected test
    -   Pause before rollback – Option to pause the test just before rollback happens after the completion of the test
8.  Analyze and debug the steps at which breakpoints have been implemented.

    \[Omitted image "atf-debug-breakpoint.png"\] Alt text: Image showing paused minutes and other options

    **Note:** Every breakpoint causes the running of the test to pause for 10 minutes. You can debug the test step within the allocated 10 minutes and then the test starts running again until it reaches the next breakpoint.

    The following options display only when the test is paused for a breakpoint:

    -   Continue: Test execution continues until the next breakpoint.
    -   Step over: Test pauses at every step. If you don’t want to pause in the current step, select the Step over option to jump to the next step.

**Parent Topic:**[Implementing breakpoints](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/automated-test-framework-atf/atf-breakpoints-rollback.md)


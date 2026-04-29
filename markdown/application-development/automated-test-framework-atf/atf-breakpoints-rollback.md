---
title: Implementing breakpoints
description: Breakpoints allow you to pause your test at any step of a test run in order to troubleshoot and test authoring.
locale: en-US
release: australia
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Building and running automated tests with the Automated Test Framework, Automated Test Framework \(ATF\) test building and execution, Automated Test Framework \(ATF\), Testing and debugging applications, Building applications]
---

# Implementing breakpoints

Breakpoints allow you to pause your test at any step of a test run in order to troubleshoot and test authoring.

Breakpoints are useful when a test fails. You can add breakpoints to the test steps to debug the test. You can also look at the test steps again to find the reasons of the test failure.

**Note:** Breakpoints are user-specific. You can see only your self-created breakpoints.

## Rollback of test data

Test runs can also be paused immediately before rollback of test data. Check the **Pause before rollback** option to pause the test just before rollback of test data happens after the completion of the test. See [Debug an automated test using breakpoints](../task/atf-breakpoint.md) to learn more about using rollback option in a test run.

-   **[Debug an automated test using breakpoints](../task/atf-breakpoint.md)**  
Pause a test to troubleshoot failures or unexpected behavior by adding a breakpoint for a particular test step.

**Parent Topic:**[Building and running automated tests with the Automated Test Framework](atf-build-overview.md)


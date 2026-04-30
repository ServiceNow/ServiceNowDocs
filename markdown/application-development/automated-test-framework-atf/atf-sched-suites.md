---
title: Working with scheduled test suites
description: You can schedule a test suite to run at a specified date and time.You can designate users to be notified when a scheduled test suite finishes executing.When the system completes executing a scheduled test suite, it sends an email to users on the Scheduled Suite Run record watchlist. This email contains information and links to further information about the Scheduled Suite Run and its results.
locale: en-US
release: zurich
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Administer, Automated Test Framework \(ATF\), Testing and debugging applications, Building applications]
---

# Working with scheduled test suites

You can schedule a test suite to run at a specified date and time.

To schedule a test suite, you need three components:

-   a test suite record
-   a schedule record specifying when you want the system to run the test suite
-   a scheduled suite run record that associates the test suite to run with the schedule for running it

With this model, you can associate a schedule with many different test suites and vice-versa.

**Note:** You can schedule only test suites, not individual tests. Scheduled tests will only run if there is an open Scheduled Client Test Runner page matching the scheduled suite's browser conditions. Scheduled tests cannot run on a machine that is locked, powered down, or does not already have the browser open.

The watchlist on the test suite run record also allows you to specify users to receive an email when the system finishes executing the test suite run.

If the test suite contains one or more form steps \(steps involving a user interface\), you must ensure that a scheduled client test runner is actively running in a browser when the schedule triggers the suite run.

**Note:** See [Browser recommendations and requirements](atf-test-runners.md#kvv_h25_gx) for recommendations and requirements for running the client test runner.

For step-by-step instructions on how to schedule a test suite, see [Schedule an automated test suite](../task/atf-sched-suite-steps.md).

**Parent Topic:**[Administering the Automated Test Framework \(ATF\)](atf-admin-overview.md)

## Designate users to receive email when system finishes running a scheduled test suite

You can designate users to be notified when a scheduled test suite finishes executing.

### Before you begin

Role required: atf\_test\_admin

### Procedure

1.  Navigate to the scheduled test suite run record.

2.  Add to the record's **watchlist** all users you want the system to notify when this scheduled test suite run completes.


## Automated Test Framework scheduled test suite completed email

When the system completes executing a scheduled test suite, it sends an email to users on the Scheduled Suite Run record watchlist. This email contains information and links to further information about the Scheduled Suite Run and its results.

**Note:** Email functionality must be enabled in order to send an email.

### Suite Stats

The Suite Stats section of the email reports the number of suites and individual tests broken down by result status: Failed \(F\), Error \(E\), Skipped \(S\), Canceled \(C\), or Passed \(P\). For a description of what each status means, see [Test suite results record](../reference/atf-test-suite-results-record.md).

### Test Suite Results

The Test Suite Results section of the email reports test suite results over time.

**Note:** By default, this report includes only suites with failed tests, but you can change this setting with the **Email properties** field on the [Properties](../reference/atf-admin-properties.md) page. If set to default, only the failed tests within a test suite are reported.

![Image showing ATF email report](../image/atf-email-report.png "Preview email report")

**Note:** ATF reports only recent tests results on the email report. All the previous test results still exist if it's within the set retention time limit. See [Table cleanup](table-cleanup.md) for more information on retention policy for ATF test results.

|Letter|Color|Description|
|------|-----|-----------|
|F|red|Test failed|
|P|green|Test passed|
|S|white|Test skipped|
|C|white|Test canceled|
|E|orange|Test has error|

Each entry acts as a link to the result record for that run. If you point the mouse to any of these entries, the system displays the parent suite number, the parent suite end time, and the test result output.

### Properties affecting email content

On the [Automated Test Framework Properties](../reference/atf-admin-properties.md) form, you can set options affecting the format and content of the email.


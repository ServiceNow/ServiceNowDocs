---
title: Schedule an automated test suite
description: Schedule one or more test suites to run at a specific date and time.
locale: en-US
release: yokohama
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Building and running automated test suites, Automated Test Framework \(ATF\) test building and execution, Automated Test Framework \(ATF\), Testing and debugging applications, Building applications]
---

# Schedule an automated test suite

Schedule one or more test suites to run at a specific date and time.

## Before you begin

You must have created the test suites you want to schedule.

Role required: atf\_test\_admin or atf\_test\_designer

## About this task

To schedule a test suite, you need three components:

-   A test suite record
-   A schedule record specifying when you want the system to run the test suite
-   A scheduled suite run record that associates the test suite to run with the schedule for running it

For more information about the capabilities of and requirements for scheduled test suites, see [Working with scheduled test suites](../concept/atf-sched-suites.md#).

## Procedure

1.  Navigate to **All** &gt; **Automated Test Framework** &gt; **Schedules**.

    The system displays the list of existing test suite schedules.

2.  To create a new schedule, click **New**.

    The system displays the Suite Schedule record form.

3.  On the [Suite Schedule record form](../reference/atf-suite-schedule-record.md), enter the name of the schedule, the frequency with which to run associated suites, the time at which to run associated suites, and the timezone for this schedule.

4.  Specify a condition that must be met for running associated test suites by selecting **Conditional**, then fill in the **Condition** text box with the appropriate script.

5.  Add a test suite to run by navigating to the Scheduled Suites related list, then clicking **New**.

    The system displays the [Scheduled Suite Run](../reference/atf-suite-sched-run-record.md) record form.

6.  On the [Scheduled Suite Run](../reference/atf-suite-sched-run-record.md) record form enter the appropriate data.

    1.  Enter the test suite to run.

    2.  If the suite contains UI steps, enter any client constraints you wish to apply \(such as browser to use\).

        For more information on client constraints, see [Scheduled Suite Run](../reference/atf-suite-sched-run-record.md).

    3.  Add to the record's watchlist users you want the system to inform \(by email\) when the scheduled suite has finished.

    4.  Click **Submit**.

7.  Add more test suites to this schedule by repeating steps 5 and 6.

8.  Click **Update**.

9.  If your suite includes any test steps that work with a form – or any other element on the client side, open a browser window for running the client portion of the scheduled tests.

    1.  Review [Browser recommendations and requirements](../concept/atf-test-runners.md#kvv_h25_gx) for all tests and suites, as well as those that apply only to scheduled suite runs.

    2.  In the **Navigator**, right-click **Scheduled Client Test Runner**, and then click the option to open in a separate tab or window, as you prefer.

    3.  Leave open the browser window that's running the client test runner and return to the browser window that contains the **Navigator**.


**Parent Topic:**[Building and running automated test suites](../concept/atf-suites-overview.md)


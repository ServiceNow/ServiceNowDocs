---
title: Scheduling test execution
description: Use schedules and nightly runs to execute tests and test suites in ServiceNow’s cloud infrastructure allowing you to fully automate ATF test executions.
locale: en-US
release: xanadu
product: ATF Test Generator and Cloud Runner
classification: atf-test-generator-and-cloud-runner
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [ATF Test Generator and Cloud Runner, Extend ServiceNow AI Platform capabilities]
---

# Scheduling test execution

Use schedules and nightly runs to execute tests and test suites in ServiceNow’s cloud infrastructure allowing you to fully automate ATF test executions.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Automated Test Framework \(ATF\)** &gt; **Schedules**.

    The Suite Schedules page shows up.

2.  Select **New** to create a new schedule run.

    The Suite Schedule record shows up.

3.  On the form, fill in the fields.

<table id="table_ph5_fns_xjb"><thead><tr><th>

Fields

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the schedule run.

</td></tr><tr><td>

Active

</td><td>

Option to activate the scheduled run.

</td></tr><tr><td>

Application

</td><td>

Application that has the schedule run.

</td></tr><tr><td>

Run

</td><td>

Frequency at which the scheduled run should execute

</td></tr><tr><td>

Time

</td><td>

Exact time at which the test run has been scheduled to execute

</td></tr><tr><td>

Run in cloud

</td><td>

Option to execute the scheduled run on cloud runner. The default value is True for new schedules.**Note:** The value is False for any existing schedule runs.

</td></tr></tbody>
</table>4.  Select **Save**.

5.  Add any child tests if needed.

    **Note:** If you change the browser name for the child test, it will still run on the cloud runner.

6.  Select **Execute Now** to execute the suite.



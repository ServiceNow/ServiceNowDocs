---
title: Run a scheduled test suite using a script
description: Execute a scheduled UI test suite immediately using a script without having to wait for the scheduled time. You can use this method while trying to automate the process of running a test.
locale: en-US
release: yokohama
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Building and running automated test suites, Automated Test Framework \(ATF\) test building and execution, Automated Test Framework \(ATF\), Testing and debugging applications, Building applications]
---

# Run a scheduled test suite using a script

Execute a scheduled UI test suite immediately using a script without having to wait for the scheduled time. You can use this method while trying to automate the process of running a test.

## Before you begin

You've created and scheduled the test suites that you want to run. See [Create an automated test suite](../task/atf-create-suite.md) and [Schedule an automated test suite](../task/atf-sched-suite-steps.md), for more information.

Role required: atf\_test\_admin or atf\_test\_designer

## About this task

The following steps might not be in line with your software configurations.

## Procedure

1.  Spin up a virtual machine \(VM\) on an operating system with the necessary browsers.

2.  Open a browser on the instance and navigate to the Scheduled Client Test Runner.

3.  Call the scriptable method `new sn_atf.ScheduledRunsExecutor().setScheduleSysId ("SYS_ATF_SCHEDULE_SYS_ID_HERE").start();` to run the scheduled suite immediately.

    To run a test only when the script is called, set the **Run** field to **On Demand** in the Schedule form.

    **Note:** The `start()` method returns `sys_progress_worker.sys_id` of the progress worker.


**Parent Topic:**[Building and running automated test suites](atf-suites-overview.md)


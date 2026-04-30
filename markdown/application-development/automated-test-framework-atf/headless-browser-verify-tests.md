---
title: Verify Headless Browser procedures in Linux
description: Step 7, the final step in the Linux setup for the ServiceNow Headless Browser for ATF: Verify that your Headless Browser setup procedures are successful.
locale: en-US
release: yokohama
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Headless Browser setup for Linux, Headless Browser for Automated Test Framework, Automated Test Framework \(ATF\), Testing and debugging applications, Building applications]
---

# Verify Headless Browser procedures in Linux

Step 7, the final step in the Linux setup for the ServiceNow® Headless Browser for ATF: Verify that your Headless Browser setup procedures are successful.

## Before you begin

Role required: admin

Complete Step 6: [Configure ATF for Headless Browser in Linux](headless-browser-configure-atf.md)

Role required: admin on your ServiceNow instance and local administrator on the host machine.

This task: Verify that Steps 1-6 in your Headless Browser setup procedures are successful.

## Procedure

1.  Go to **ATF Schedules** and next to the Suite Schedules link, select **New**.

2.  In the Run box, select **On Demand**.

3.  Select **Save**.

4.  In the Scheduled Suite related list, add a new record for your test suite by double-clicking the **+** sign and choose your browser name of **Chrome** or **Firefox**.

    Use **Child A** as a good example to run.

    ![Scheduled Suite Child A record example](../image/child-a-example.png)

5.  Set the OS name to Linux.

6.  Select **Execute Now**.

7.  Verify that your test passed.

    When your verification is successful, any suites with UI tests run by scheduled suites or via CICD now automatically create headless test runners without the need to manually open the "scheduled client test runner" page.


**Parent Topic:**[Headless Browser setup for Linux](../concept/headless-browser-procedure-linux.md)

**Previous topic:**[Configure ATF for Headless Browser in Linux](headless-browser-configure-atf.md)

**Next topic:**[Headless Browser setup for Microsoft Windows](../concept/headless-browser-procedure-windows.md)


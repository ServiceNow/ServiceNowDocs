---
title: Verify Headless Browser procedures for ATF in Microsoft Windows
description: Verify that your Headless Browser setup procedures have been successful.
locale: en-US
release: xanadu
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Headless Browser setup for Microsoft Windows, Headless Browser for Automated Test Framework, Test your apps with the ATF, Testing and debugging applications, Building applications]
---

# Verify Headless Browser procedures for ATF in Microsoft Windows

Verify that your Headless Browser setup procedures have been successful.

## Before you begin

Complete Step 7: [Configure Automated Test Framework \(ATF\) for Headless Browser in Microsoft Windows](headless-browser-configure-atf-windows.md)

Role required: admin

## Procedure

1.  Go to **ATF Schedules** and next to the Suite Schedules link, select **New**.

2.  In the Run box select **On Demand**.

3.  Select **Save**.

4.  In the Scheduled Suite related list, add a new record for your test suite by double-clicking the **+** sign and choose your browser name of **Chrome** or **Firefox**.

    Use **Child A** as a good example to run.

    ![Scheduled Suite Child A record example](../image/child-a-example.png)

5.  Set the OS name to Windows.

6.  Select **Execute Now**

7.  Verify that your test passed.

    When your verification is successful, any suites with UI tests run by scheduled suites or via CICD now automatically create headless test runners without the need to manually open the "scheduled client test runner" page.


**Parent Topic:**[Headless Browser setup for Microsoft Windows](../concept/headless-browser-procedure-windows.md)

**Previous topic:**[Configure Automated Test Framework \(ATF\) for Headless Browser in Microsoft Windows](headless-browser-configure-atf-windows.md)

**Next topic:**[Headless Browser system properties](../reference/atf-headless-browser-properties.md)


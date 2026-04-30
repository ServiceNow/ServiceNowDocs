---
title: Managing automatic test screenshot settings
description: Capturing many screenshots can impair test performance. You can control which types of screenshots the system captures to minimize this effect.To control how often this instance captures screenshots for form test steps, set the screenshot capture mode on the automatic test framework properties page.To control how often the current client test runner captures screenshots for form test-steps, set the screenshot capture mode on the client test runner browser window.
locale: en-US
release: yokohama
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Optimizing automatic test performance, Administering the Automated Test Framework \(ATF\), Automated Test Framework \(ATF\), Testing and debugging applications, Building applications]
---

# Managing automatic test screenshot settings

Capturing many screenshots can impair test performance. You can control which types of screenshots the system captures to minimize this effect.

By default, the system captures a screenshot every time it executes a form test step. This information can be useful for understanding test results, but may slow down how fast the system executes the test.

You can change automatic test framework settings so that the system captures all screenshots \(as it does by default\), no screenshots, or just screenshots for failed test steps.

You can change these settings to affect all tests run on this instance, or to affect just the current client test runner session. To affect all tests run on this instance, set the automatic test framework property from the automatic test framework properties page. To affect just the current client test runner session, set the screenshot mode from client test runner browser window.

**Parent Topic:**[Optimizing automatic test performance](atf-optimize-perf.md)

## Set the system property to control when the Automated Test Framework captures screenshots

To control how often this instance captures screenshots for form test steps, set the screenshot capture mode on the automatic test framework properties page.

### Before you begin

Role required: atf\_test\_admin or admin

### About this task

Setting the screenshot mode from the automatic test framework properties page affects any new client test runners started on this instance. This setting does not affect currently-running test-runners.

### Procedure

1.  Navigate to **All** &gt; **Automated Test Framework** &gt; **Administration** &gt; **Properties**.

2.  Set the **Enable or disable screenshot capture** property from the drop-down menu.

    -   To capture screenshots for all steps, select **Enable for all steps**.
    -   To capture screenshots only for failed steps, select **Enable for all failed steps**.
    -   To capture no screenshots, select **Disable for all steps**.
3.  Set the **Screenshot timeout** time interval, in seconds.

    The Client Test Run does not take a screenshot capture if the length of the attempt exceeds this value. Users should review performance settings and browser caches on affected client systems before increasing this value.

4.  Click **Save**.


## Set the client test-runner property to control when the Automated Test Framework captures screenshots

To control how often the current client test runner captures screenshots for form test-steps, set the screenshot capture mode on the client test runner browser window.

### Before you begin

Role required: atf\_test\_admin or admin

### About this task

Setting the screenshot mode from the client test-runner browser window affects only this client test-runner and persists until this test-runner session is closed. This setting does not affect any other running test-runners or any future test runners.

### Procedure

1.  From the client test-runner browser window, click the form preferences icon \(![Form preferences icon](../../../common/image/Form_PersonalizeFormIcon.png)\).

2.  Click the **Screenshot mode** option.

    -   To capture screenshots for all steps, select **Enable for all steps**.
    -   To capture screenshots only for failed steps, select **Enable for all failed steps**.
    -   To capture no screenshots, select **Disable for all steps**.
3.  Click **Save**.



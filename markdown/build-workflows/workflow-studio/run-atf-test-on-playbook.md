---
title: Run an automated test on a playbook
description: After creating your test and adding steps, run and monitor the progress of your automated test.
locale: en-US
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Testing support, Running Playbooks, Playbooks, Workflow Studio, Build workflows]
---

# Run an automated test on a playbook

After creating your test and adding steps, run and monitor the progress of your automated test.

## Before you begin

Role required: admin or atf\_test\_admin

## About this task

If you get the error "The test timed out because the max execution time \(600 seconds\) was reached," your browser might be causing it. Some browsers might throttle back the amount of processing \(CPU\) power allocated to browser tabs that do not have focus. See [KB0621899](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0621889) for more information about this issue and suggested workarounds.

## Procedure

1.  Navigate to **All** &gt; **Automated Test Framework \(ATF\)** &gt; **Tests**.

2.  Select the **Test** name for the test you want to run.

3.  On the Test page if this is the first time you are setting up and running a test, there is a message at the top of the page: **Running tests and test suites is disabled.**

    Select the link **Enable tests and test suites execution here** to enable the test.

4.  Select **Yes** on the first check box and select **Save** to enable test and test suite execution.

5.  Navigate back to the test page and at the top of the page, select **Run Test**.

    A new browser tab opens to run the test.

6.  When the tests have finished running, select **Go to Result** to view the test results.

    For more information, see Run an automated test.


**Parent Topic:**[Testing support for playbooks](../concept/testing-support-playbooks.md)


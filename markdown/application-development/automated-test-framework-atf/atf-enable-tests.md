---
title: Enable or disable executing Automated Test Framework tests
description: Allow or prevent tests and test suites from executing on this instance.
locale: en-US
release: australia
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Administering the Automated Test Framework \(ATF\), Automated Test Framework \(ATF\), Testing and debugging applications, Building applications]
---

# Enable or disable executing Automated Test Framework tests

Allow or prevent tests and test suites from executing on this instance.

## Before you begin

Role required: atf\_test\_admin

## About this task

By default, the system property that is used to run automated tests is disabled to prevent you from accidentally running these tests on a production system. To avoid data corruption or an outage, run tests only on development, test, and other non-production instances.

## Procedure

1.  Navigate to **All** &gt; **Automated Test Framework** &gt; **Administration** &gt; **Properties**.

2.  Set the test execution property.

    -   To enable test and test suite execution, select **Enable test/test suite execution**.
    -   To disable test and test suite execution, clear **Enable test/test suite execution**.
3.  Select **Save**.


**Parent Topic:**[Administering the Automated Test Framework \(ATF\)](../concept/atf-admin-overview.md)


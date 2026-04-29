---
title: Edit automated test step order
description: By default, steps execute in the order in which you created them. You can change this order by editing the Execution Order field.
locale: en-US
release: australia
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Create a new automated test, Building and running automated tests with the Automated Test Framework, Automated Test Framework \(ATF\) test building and execution, Automated Test Framework \(ATF\), Testing and debugging applications, Building applications]
---

# Edit automated test step order

By default, steps execute in the order in which you created them. You can change this order by editing the **Execution Order** field.

## Before you begin

Role required: atf\_test\_admin or atf\_test\_designer

## About this task

By default, the system assigns the value 1 to **Execution Order** for the first step created for a test. When you add a step, the system assigns it the next-highest available integer value. In other words, if the highest **Execution Order** for any step in the test has the value 7, the system assigns 8 to the new step. By editing these values, you can change the order in which the test executes the steps.

## Procedure

1.  Navigate to **All** &gt; **Automated Test Framework** &gt; **Tests**.

2.  Click the row containing the test you want to edit.

    The system displays the **Test**form.

3.  In the **Test Steps** related list, edit the values in the **Execution order** column to determine the new order for the steps.

4.  Click **Update**.


**Parent Topic:**[Create a new automated test](atf-create-test.md)


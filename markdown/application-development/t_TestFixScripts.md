---
title: Test a fix script
description: Test your fix scripts to ensure they install or update applications as expected.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Fix scripts, Anatomy of an application, Learning about developing on the ServiceNow AI Platform, Building applications]
---

# Test a fix script

Test your fix scripts to ensure they install or update applications as expected.

## Before you begin

Role required: admin

## About this task

Fix scripts add, update, and delete data, including rules, scripts, and property settings.

**Note:** Do not test fix scripts on production instances.

## Procedure

1.  Open the fix script record.

2.  Review the code design to ensure that it can run more than once on the same system without causing damage.

    For example, you may write a fix script that adds a role to a property by default. Design the script so that it can run multiple times on the same system without overwriting the existing data, even if it is not necessary to run the script again after the initial installation.

3.  Click the **Run Fix Script** related link.

    Tests enforce the Unloadable option.

4.  Confirm how to run the script.

<table id="choicetable_bkd_345_cr"><tbody><tr><td id="d270114e98">

**__Proceed in Background__**

</td><td>

Use this option for long-running scripts, or if you do not know the expected execution time.

</td></tr><tr><td id="d270114e108">

**__Proceed__**

</td><td>

Use this option to run the script immediately and display the results in a confirmation window.

</td></tr></tbody>
</table>    ![Successful fix script test](../image/FixScriptTest.png)

5.  Review the results from the Progress Workers related list, and make any necessary changes.

6.  To manually stop a running fix script:

    1.  From the **Progress Workers** related list, select a worker in the `Running` state.

    2.  Select the **Cancel job** related link.

    ![Progress Workers results](../image/ProgressWorkers.png)



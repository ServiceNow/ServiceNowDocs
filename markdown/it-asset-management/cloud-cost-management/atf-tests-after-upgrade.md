---
title: Run the Automatic Test Framework \(ATF\) tests
description: Run the ATF tests to ensure data continuity after upgrading Cloud Cost Management.
locale: en-US
release: xanadu
product: Cloud Cost Management
classification: cloud-cost-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Upgrade Cloud Cost Management, Configuring Cloud Cost Management, Cloud Cost Management, IT Asset Management]
---

# Run the Automatic Test Framework \(ATF\) tests

Run the ATF tests to ensure data continuity after upgrading Cloud Cost Management.

## Before you begin

Role required: sys\_admin

## About this task

In this procedure, you run the following tests after upgrading Cloud Cost Management:

-   The Pivot Key Verification test determines whether Cloud Cost Management can correctly calculate the pivot key using pulled data to access the data on the Clotho server.
-   The Monthly Spend Validation test determines whether monthly spend data has been correctly carried forward.

## Procedure

1.  Navigate to **All** &gt; **Automated Test Framework \(ATF\)** &gt; **Tests**.

2.  In the list, search for `Pivot Key Verification` and open the test for your provider.

    A template for the test opens on the Test form.

3.  On the Test form, select **Copy Test** and then select **OK** to confirm.

    The system generates the test that you run and opens it on the **Test** form.

4.  To customize the test, select **Run Server Side Script** in the **Test Steps** related list and edit the script.

5.  Select **Run Test**.

    The Run Test progress dialog box appears.

    ![Run Test dialog box shows test progress](../image/run-test-progress-dialog.png)

6.  When the test finishes, select **Go to Result**.

    The **Test Results** related list on the Test form lists logs data for the test execution. If the test fails, contact Customer Support.

7.  Repeat the full procedure for the `Monthly Spend Validation` test.



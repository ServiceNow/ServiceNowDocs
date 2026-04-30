---
title: Build and run your first automated test
description: Follow these step-by-step instructions to create and run your first automated test. This test creates a new user record.Create a new automated test record.Add the first of three steps to the automated test.Add the second of three steps to the automated test.Add the last of three steps to the automated test.After adding test steps, run and monitor the progress of the automated test.Monitor the progress of the automated test and view its test results.
locale: en-US
release: xanadu
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Getting started with the Automated Test Framework, Test your apps with the ATF, Testing and debugging applications, Building applications]
---

# Build and run your first automated test

Follow these step-by-step instructions to create and run your first automated test. This test creates a new user record.

-   The Automated Test Framework \(com.glide.automated\_testing\_framework\) plugin must be activated. It is activated by default on zBoot or upgrade.
-   If necessary, enable test execution. For instructions, see [Enable or disable executing Automated Test Framework tests](atf-enable-tests.md).

    **Note:** By default, the system property that is used to run automated tests is disabled to prevent you from accidentally running these tests on a production system. To avoid data corruption or an outage, run tests only on development, test, and other non-production instances.

-   Role required: admin

**Parent Topic:**[Getting started with the Automated Test Framework](../concept/atf-intro.md)

## Create new test

Create a new automated test record.

### Before you begin

Role required: atf\_test\_admin or admin

### Procedure

1.  Navigate to **All** &gt; **Automated Test Framework** &gt; **Tests**.

2.  Click **New**.

3.  On the Test new record form, enter a name for your test in the **Name** field.

    The system identifies this test by this name whenever it displays a list of tests \(for example, under the Tests module\).

    ![Form for creating a new test](../image/atf-test-create-new.png)

4.  In the **Description** field, enter a description for your test.

5.  Click **Save**.


### Result

The system creates a new test record and returns to the list of tests. For more information about creating new automated tests, see [Create a new automated test](atf-create-test.md).

## Add the first step to the new test

Add the first of three steps to the automated test.

### Before you begin

Role required: atf\_test\_admin or admin

### Procedure

1.  Navigate to **All** &gt; **Automated Test Framework** &gt; **Tests**.

2.  Click the test that should contain the new test steps.

3.  In the Test Steps related list at the bottom of the Test form, click **Add Test Step**.

4.  In the middle column, click the row for the step type **Open a new form**, then select **Next**.

    ![Add Test Step dialog](../image/atf-test-step-dlg.png)

    The system displays the **Add Test Step** form for the Open a new form step.

5.  From the **Table** field, select the **User \[sys\_user\]** table and click **Submit**.

    ![Add Test Step: Open a New Form.](../image/atf-test-step-add-open-new.png)

    The system creates the new step and returns to the test record.

6.  Click **Update**.


### Result

The system creates a new test record and returns to the list of tests. For more information about adding steps to automated tests, see [Add steps to an automated test](atf-create-step.md).

### What to do next

For some ideas on how to continue learning about the Automated Test Framework, see [Next steps with the Automated Test Framework](../concept/atf-next-step-concepts.md).

## Add the second step to your automated test

Add the second of three steps to the automated test.

### Before you begin

Role required: atf\_test\_admin or admin

### Procedure

1.  Click the test that should contain the new test steps.

2.  In the Test Steps related list at the bottom of the Test form, click **Add Test Step**.

3.  In the middle column, click **Set Field Values**, then click **Next**.

    The system displays the **Add Test Step** form for the Set values step.

4.  In the field values section, set **Last name** to `Test` and **First name** to `Otto` \(or other names of your choice\).

    ![Test step](../image/atf-first-test-01.png)

5.  Click **Submit**.


### Result

The system creates the new step and returns to the test record. For more information about adding steps to automated tests, see [Add steps to an automated test](atf-create-step.md).

## Add the third step to your test

Add the last of three steps to the automated test.

### Before you begin

Role required: atf\_test\_admin or admin

### Procedure

1.  Click the test that should contain the new test steps.

2.  In the Test Steps related list at the bottom of the Test form, click **Add Test Step**.

3.  In the middle column, click **Submit a Form**, then click **Next**.

    The system displays the **Add Test Step** form for the Submit a form step.

4.  Leave all values as set by default and click **Submit**.

    ![Submit a form test step](../image/atf-first-test-02.png)

    The system creates the new step and returns to the test record. The test record should now show the three steps you just added.

    ![Updated test record](../image/atf-first-test-03.png)

5.  Click **Update**.


### Result

The system returns to the list of tests. For more information about adding steps to automated tests, see [Add steps to an automated test](atf-create-step.md).

## Run your test

After adding test steps, run and monitor the progress of the automated test.

### Before you begin

Role required: atf\_test\_admin or admin

### Procedure

1.  If necessary to view the Tests list, click **Tests**.

2.  Click the row containing the test you just created.

    The system displays the **Test** form.

3.  Click **Run Test**.

    Because this test includes a form step \(any step involving a UI\), the system displays a dialog box asking you to choose among any currently-running test clients or start a new test runner. To continue, select **start a new test runner** and click **Run Test**.


### Result

The system displays the Run Test progress dialog. For more information about running automated tests, see [Run an automated test](atf-run-test.md).

## Monitor test progress and view test results

Monitor the progress of the automated test and view its test results.

### Before you begin

Role required: atf\_test\_admin or admin

### About this task

If needed, you can cancel a test even while it's running. For more information, see [Cancelling automated tests and test suites](../concept/atf-cancelling.md#).

### Procedure

1.  Monitor the progress of the test in the Run Test progress dialog.

    **Note:** If your test creates data, the system rolls back that data after all steps in the test complete.

2.  When complete, click **Go to Results** on the Run Test progress dialog to display the **Test Results** list, where you can [view and analyze the results.](atf-view-results-consolidated.md)



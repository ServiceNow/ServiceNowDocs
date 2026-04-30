---
title: Generating the tests
description: Generate tests automatically by leveraging ServiceNow Test Generation and Cloud Runner application. You can also run these tests with the click of a button.
locale: en-US
release: yokohama
product: ATF Test Generator and Cloud Runner
classification: atf-test-generator-and-cloud-runner
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Operating ATF Test Generator and Cloud Runner, ATF Test Generator and Cloud Runner, Extend ServiceNow AI Platform capabilities]
---

# Generating the tests

Generate tests automatically by leveraging ServiceNow Test Generation and Cloud Runner application. You can also run these tests with the click of a button.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Automated Test Framework \(ATF\)** &gt; **Administration** &gt; **Test Generator**.

    If you are on the **Select Cloud User** module and have setup the admin user, click **Click here to navigate to test generator page**.

    **Note:** The **Generate Tests** module is visible only to the admins. Even an ATF test admin can't access the **Select Cloud User** module.

    If you already have a test generation running, you will see the following message.

    ![Image showing in progress test generation](../image/atf-app-inprogress-test-generation.png)

    **Note:** You can't start more than one test generation process simultaneously, but it will queue up for later execution.

2.  If you want to see the currently running test and the queue, navigate to **Automated Test Framework \(ATF\)** &gt; **Administration** &gt; **Browser Orchestration Queue**.

    The Browser Orchestration Queues list shows up.

    **Note:** You can see the progress and state of each of the test generation and test run in the list.

3.  Select one of the two ways to generate tests.

    ![Generate Tests screen.](../image/atf-tg-cr-advanced.png)

    -   Not selecting **Advanced**: Generates tests on every table by default
    -   Selecting **Advanced**: Option to specify a specific table to generate tests
        -   Maximum Test Count: Upper bound on the number of generated tests.
        -   Maximum test count per table: Upper bound on the test count for each table
        -   Maximum test count per catalog item: Maximum number of generated tests per service catalog item, defaulting to maximum 10. You can modify the number of generated tests per service catalog item
        -   Create separate update sets per scope: Option to create a separate update set for each scope
        -   Scope for generating tests: Ability to have the tables in separate update sets for different scopes. For example, the generator gathers information about the scope of the tables and then saves the tests in a separate update set for each scope

            **Note:** This field is visible only if the **Create separate update sets per scope** field is not selected. You can then select the scope for the generated tests. The default scope is Global.

        -   Email: Email address of the user to receive notifications about test generation summary
        -   Presets: Number of user-control generated tests per service catalog item. The maximum default number is 10.
    **Note:** Since the test generation process is time consuming, check your provided email address regularly to receive the notification about the test generation.

4.  Select **Save preset** to implement the preset filter conditions.

    You can also delete a preset by selecting **Delete preset**. All admins who can access the **Generate Tests** module can view the update on the **Presets** field.

    **Note:** You can't delete the default **None** preset. Some example presets have been provided which can be edited.

    ![Generate Tests screen.](../image/atf-app-preset-tabs.png)

    Depending on the query created by the preset values, the following tabs return certain data.

    -   Users
    -   Tables
    -   Service Catalog
    **Note:** You can create new condition sets to filter the required information in tabs.

    ![Users screen.](../image/atf-app-filter.png)

5.  Select **Start Test Generation**.

    The Test Generation Started page shows up.

    ![Image showing the test generation started dialog box](../image/atf-app-test-generation-progress.png)

    If you run a test or a suite when the test generation is in progress, one of the following messages shows up.

    -   For test run

        ![Image showing test run queue when test generation is in progress](../image/atf-app-queue-test-run.png)

    -   For suite run

        ![Image showing suite run queue when test generation is in progress](../image/atf-app-queue-suite-run.png)

6.  Go to Suites to see the generated tests.

    A list of test suites shows up.

    **Note:** The tests start appearing as they are being generated. It is recommended not to run the generated tests or test suite when the test generation is still in progress.

7.  Select the **ATF Generated Suite** suite.

    **Note:** It supports only the basic forms and server test steps.

    You can now set the sn\_atf\_tg.generation.create\_separate\_update\_set property to False if you don’t want an updated suite every time you run a test generation. The updated records created during tests generation are captured in the suite the user currently has selected. Its default value is set to True and it generates an updated suite after every test generation.

    A list of tests within the selected suite shows up. Only the successful tests show up in this suite.

8.  Select the generated suite and scroll down to the Tests related list, if you want to view the generated automated tests using either Record Producer or Service Catalog.

    From the automated tests created, you can view all the users who have used that record or incident. Although the tests steps here are similar to the other test steps, the initial validation is done for the fields on the form. Also, for every mandatory field, a value is set based on the sample data. It also validates after every mandatory step. Once you submit, it does a final record validation.


**Parent Topic:**[Operating ATF Test Generator and Cloud Runner](../concept/atf-tg-cr-operate.md)

**Related topics**  


[Tests generation for flow and flow logic](../concept/atf-tg-cr-sc-flow.md)


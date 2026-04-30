---
title: Invoke a reusable test
description: Implement the following steps to invoke a reusable test in a test \(regular or reusable test\) or a test in a test suite.
locale: en-US
release: yokohama
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: task
last_updated: "2025-03-07"
reading_time_minutes: 2
breadcrumb: [Reusable tests, Automated Test Framework \(ATF\) tests types and testing ways, Automated Test Framework \(ATF\), Testing and debugging applications, Building applications]
---

# Invoke a reusable test

Implement the following steps to invoke a reusable test in a test \(regular or reusable test\) or a test in a test suite.

## Before you begin

You are expected to create the following before proceeding:

-   Create either a regular ATF test, or a parent reusable test that rolls up to a regular ATF test.
-   Create a reusable test that can be invoked either from a regular ATF test or a parent reusable test. For information about creating a reusable test, see [Create a reusable test](atf-create-reusable-tests.md).

Role required: admin, atf\_test\_admin, atf\_test\_designer or atf\_ws\_designer

## Procedure

1.  Navigate to **All** &gt; **Automated Test Framework \(ATF\)** &gt; **Tests**.

    **Note:** You can also navigate to **Reusable Tests**, if you need to invoke the reusable test in the parent reusable test.

    The list of ATF tests shows up.

2.  Select the test in which you want to invoke the reusable test.

3.  Scroll down the selected test form to see the Test Steps related list.

4.  Select **Add Test Step** to invoke the reusable test.

    The Add Test Step modal opens up.

5.  Select Reusable Test test category or another category, depending on how the reusable test was categorized while creating it.

    **Note:** The reusable tests show up under the Reusable Tests test category, by default. You can also define the category of the reusable tests while creating them.

    The list of all reusable tests on the instance shows up.

6.  Select the required reusable test from the list to invoke in the parent test.

7.  Select **Next**.

    The reusable test form shows up.

8.  Make the required selections on the reusable test form and select **Submit**.

    The reusable test is now invoked in the parent test.

    The reusable test shows up as a test step under the Test Steps related list.

9.  Execute the parent test by selecting **Run Test**.

    The Run Test modal shows up.

10. Expand the reusable test steps in the modal for more information.

    You can also select **See Results** in the modal to view details of the test steps under the Step Results related list.

11. Follow the gif for a quick overview of invoking a reusable test.

    ![Gif showing how to invoke a reusable test.](../image/atf-invoke-reusable-test.gif)


**Parent Topic:**[Reusable tests](../concept/atf-reuse-tests.md)


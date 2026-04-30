---
title: Create a custom UI test
description: Test components in custom UI pages.
locale: en-US
release: zurich
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Custom UI test steps, UI test steps, Building and running automated tests with the Automated Test Framework, Test building and execution, Automated Test Framework \(ATF\), Testing and debugging applications, Building applications]
---

# Create a custom UI test

Test components in custom UI pages.

## Before you begin

-   Use the Page Inspector to identify testable custom UI components. See [Enable and use the page inspector](enable-page-inspector.md).
-   Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Automated Test Framework** &gt; **Tests**.

2.  Click **New**.

3.  Enter a name and description for your test.

4.  Click **Save**.

5.  In the Test Steps related list, click **Add Test Step**.

6.  Add test steps to navigate to the target custom UI page.

    Use the **Navigate to Module** step to open a page that has an application navigator module. Use the **Open Service Portal Page** step to open a portal page.

    To open a UI page, use these test steps:

    1.  **Open an Existing Record**: Open the record for the page.
    2.  **Click UI Action**: Click the **Try It** UI action to open the page.
7.  Add test steps from the Custom UI category to validate the behavior of custom UI components.

    For a list of available Custom UI test steps, see [Custom UI category](../reference/test-steps-custom-ui-category.md#).

8.  Retrieve UI components when adding a test step.

    Identify the testable page components on a custom UI page by retrieving a list of UI components for test steps. You can collect the components of the current page by selecting **Retrieve Components**.

    The system retrieves the components using an existing or a new client test runner. Ensure that the client test runner tabs used in the retrieval process are running in the foreground. For tests that don’t yield any components after selecting **Retrieve Components**, the following warning message is displayed and the **Next** button is disabled.

    ![Warning messages for test steps with no components](../image/warning_no_components.png)

    If you have already retrieved a list of page components, click **Next** to use the previously retrieved list. You can also click **Retrieve Components** to rerun the current steps and refresh the list of testable page components. If the test fails while retrieving components, the following warning notification is displayed. You can review the test results by clicking the link in the notification.

    ![Retrieve page components failure](../image/error_for_client_error_on_page.png)

    **Note:** If you need to update a step in a test, click **Retrieve Components** for that step and the test runs only up to that particular step. The steps beyond the selected step don’t run. The test passes if all the updated steps pass without failure.

    ![Image showing the skipped steps after retrieve components](../image/atf-skipped-steps.png)

    Automated Test Framework stores the list of page components and displays the list in the **Component values** or **Component** field on the test step form. The field displays this information about each component:

    |Field|Description|
    |-----|-----------|
    |Type|HTML element description and tag. For example, `Text<input>`.|
    |Label|HTML component label.|
    |Value|Value of the component. For example, if the component is a search input, the value might be **Search**.|
    |Page area|HTML layout element that contains the component such as a `<div>` or `<section>` element.|

    If you create a parameterized test that includes Custom UI test steps, the system only uses the first data set to retrieve components.


## What to do next

Consider adding tests to a test suite. For more information, see [Building and running automated test suites](../concept/atf-suites-overview.md).

**Parent Topic:**[Custom UI test steps](../concept/custom-ui-test-steps.md)


---
title: Diagnose and resolve a technology product support case
description: As a customer service agent, review, diagnose, resolve, and close a case for the service-related issue experienced by the customer.
locale: en-US
release: australia
product: Product Support for Technology
classification: product-support-for-technology
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Technology Product Support Case, Use, Product Support for Technology]
---

# Diagnose and resolve a technology product support case

As a customer service agent, review, diagnose, resolve, and close a case for the service-related issue experienced by the customer.

## Before you begin

Role required: sn\_tech\_support.agent

## About this task

The technology product support case progresses through several stages from start to closure. It begins with a support agent reviewing and verifying the problem. Next is the diagnosis tab, where system-specified tests are executed to identify the root cause. After the tests, the support agent moves to the repair stage, creating a task to fix the identified issue. The agent follows the instructions in the repair task to address the problem areas. Once the repair is complete, the case is retested to confirm that the issue is resolved. Finally, the case is resolved and closed based on the customer's feedback on the provided solution.

## Procedure

1.  Navigate to **Workspaces** &gt; **CSM/FSM Configurable Workspace**.

2.  Select the List icon.

3.  Navigate to **Technology Product Support Case** &gt; **Assigned to me**.

4.  Open the technology product support case that is in the New or Open state.

    ![technology product support case diagnose.](../image/tech-product-case-diagnose.png)

5.  Review and verify the technology product support case.

    1.  In the **Intake** tab, expand the **Gather details**, and then review and verify the general details for the technology product support case.

    2.  Expand the **Describe the problem** and review the details of the technology product support case.

    3.  Expand the **Identify impacted instances** and review the affected instances.

    4.  Select **Continue**.

        **Note:** Before the state is moved to close, the fields in the technology product support case form can be edited from the case highlights card.

    The technology product support case moves to the Triage stage.

6.  Review the case information.

    1.  In the **Triage** tab, expand the **Review the problem** and review the details of the problem and affected instances.

    2.  Expand the **Send Initial Response** and review the initial response.

    The technology product support case moves to the Troubleshoot stage.

7.  Diagnose the technology product support case to identify the root-cause of the problem.

    1.  To generate the test results, select **Run diagnostics** from the contextual panel.

    2.  In the run diagnostics panel, select **CI/Service** from the drop-down list.

    3.  Expand the cards in the **Available Test Suite**.

        To set up test definitions, see [Setting up test definitions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-media-technology/settingup-test-specifications.md).

        To set up test group, see [Setting up a test group](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-media-technology/setting-test-group.md).

    4.  In the manual test, select single/multiple tests.

        In the automated test, selection of test isn’t available.

    5.  Select **Configure**.

    6.  In the Configure tests dialog box, fill the test required characteristics form to activate the **Run test** button.

    7.  In the test dialog box, select an option either to run the test now or to schedule it for later.

    8.  Select **Run test**.

    9.  In the diagnose tab, expand the **Test results** and review the results of the tests conducted in the previous step, checking whether each test is passed or failed.

        The failed tests indicate that the issues causing the technology product support case to be identified and need repair.

        The maximum number of rows to the group is limited to 20 rows. To configure the maximum number of rows more than 20 rows to the group, see [Presentational List Usage](https://developer.servicenow.com/dev.do#!/reference/next-experience/yokohama/now-components/now-list/usage).

    10. Select the **View Details** ![](../../../reuse/icons/product-icons/open-link-right-fill-24.svg) icon for a specific test result to review its details.

    11. Select the **Rerun test** ![](../../../reuse/icons/product-icons/arrow-clockwise-outline-24.svg) icon for a specific test result to run it again.

    12. Select **Continue**.

    13. In the **Diagnostic tasks** tab, select **Create** to create manually the diagnostic tasks.

    The case moves to the Repair stage.

8.  Repair the case by creating a new or automated repair task.

    -   Select **Generate automated task** to automatically create a repair task.
    -   Select **Create repair task** to manually create a customize repair task.
    A Repair task is created for all failed test cases related to the diagnosed cases.

    1.  Select the repair task that you want to work on.

    2.  In the Resolution task form, review the task details to identify the failed test and then work on those tests to fix the service problem.

    3.  In the **Select** field, select an appropriate state from the list to update or close the repair task, such as Closed complete.

    4.  Select **Save** and close the resolution task.

    5.  Select **Continue**.

    The case moves to the Resolve stage.

9.  In the **Resolve** stage, review the proposed resolution for the case.

10. Close the technology product support case.

    1.  Go to the Close stage and fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Issue summary|Summary of the issue.|
        |Resolution code|Code value that explains how the case is resolved. For example, Fixed by Support/Guidance provided.|
        |Resolution notes|Summarizes the resolution of technology product support case.|
        |Add resolution notes to comments|Option to make the resolution notes available to anyone who can view the case activity stream.|
        |Additional comments \(Customer visible\)|Comments related to the service problem case, if any. These comments are visible to your customer who can access this case.|
        |Work notes|Information about state transitions.|

    2.  Select **Accept Solution** or **Reject Solution** based on the customer feedback.


## Result

The technology product support case is resolved and closed successfully.


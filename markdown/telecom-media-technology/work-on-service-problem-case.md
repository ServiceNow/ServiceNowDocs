---
title: Diagnose and resolve a service problem case
description: As a customer service agent, review, diagnose, resolve, and close a service problem case for the service-related issue experienced by the customer.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Use, Customer Service Problem Management, Telecommunications, Media, and Technology \(TMT\)]
---

# Diagnose and resolve a service problem case

As a customer service agent, review, diagnose, resolve, and close a service problem case for the service-related issue experienced by the customer.

## Before you begin

Role required: admin

## About this task

The service problem case progresses through several stages from start to closure. It begins with a customer service agent reviewing and verifying the problem. Next is the diagnosis stage, where system-specified tests are executed to identify the root cause. After the tests, the agent moves to the repair stage, creating a task to fix the identified issue. The agent follows the instructions in the repair task to address the problem areas. Once the repair is complete, the service is retested to confirm that the issue is resolved. Finally, the case is resolved and closed based on the customer's feedback on the provided solution.

![Service problem case.](../image/service-problem-case.png)

## Procedure

1.  Navigate to **All** &gt; **Workspaces** &gt; **CSM/FSM Configurable Workspace**.

2.  Select the List icon.

3.  Navigate to **Service Problem Case** &gt; **Assigned to me**.

4.  Open a service problem case that is in the New or Open state.

5.  Review and verify the service problem case.

    1.  In the **Verify** tab, expand **Verify issue**, and then review and verify the general details for the service problem.

    2.  Expand **Service details** and review the remaining details of the service.

    3.  Select **Continue**.

    **Note:** Before the state is moved to close, the fields in the service problem case form can be edited from the case highlights card.

    The service problem case moves to the Diagnose stage.

6.  Diagnose the service problem case to identify the root-cause of the problem.

    The decision table can be configured to control the visibility of the Run Diagnostics contextual panel tab. For more information about decision tables, see Decision Tables.

    1.  To generate the test results, select **Run diagnostics** from the contextual panel.

    2.  In the run diagnostics panel, select **CI/Service** from the drop-down list.

        The drop-down list shows the current product inventory and all the child inventories.

    3.  Expand the cards in the **Available test suite**.

        To set up the test definitions, see [Setting up test definitions](../concept/settingup-test-specifications.md).

        To set up a test group, see [Setting up a test group](../concept/setting-test-group.md).

    4.  In the manual test, select single/multiple tests.

        In the automated test, selection of test isn’t available. The subflow that is configured for the test group would be invoked.

    5.  Select **Configure**.

    6.  In the Configure tests dialog box, fill the test required characteristics form to activate the **Run test** button.

    7.  In the test dialog box, select an option either to run the test now or to schedule it for later.

    8.  Select **Run test**.

    9.  Select the **Test results** tab and review the results of the tests conducted in the previous step, checking whether each test is passed or failed.

        The failed tests indicate that issues causing the service problem are identified and needing repair.

        The maximum number of rows according to group is limited to 20. To configure the maximum number of rows more than 20 according to group, see [Presentational List Usage](https://developer.servicenow.com/dev.do#!/reference/next-experience/yokohama/now-components/now-list/usage).

    10. If the status of diagnose is new or closed, select the **View Details** ![](../../../reuse/icons/product-icons/open-link-right-fill-24.svg) icon for a specific test result to review its details.

    11. If the status of diagnose is Pending for inputs, select the **View Details** ![](../../../reuse/icons/product-icons/open-link-right-fill-24.svg) icon and fill the form.

    12. Select the **Rerun test** ![](../../../reuse/icons/product-icons/arrow-clockwise-outline-24.svg) icon for a specific test result to run it again.

        A repair task is created for each unique service and test definition.

    13. Select **Continue**.

    14. In the **Diagnostic tasks** tab, select **Create** to create manually the diagnostic tasks.

    The case moves to the Repair stage.

7.  Repair the service problem case by creating a new or automated repair task.

    -   Select **Generate automated task** to automatically create a repair task.
    -   Select **Create repair task** to manually create a customize repair task.
    A Repair task is created for all failed test cases related to the diagnosed service problem. For each unique service and test specification, only one repair task is created. The agent can then work on it and close this repair task.

    1.  Select the repair task that you want to work on, such as RT0001101.

    2.  In the Resolution task form, review the task details to identify the failed test and then work on those tests to fix the service problem.

    3.  In the **Select** field, select an appropriate state from the list to update or close the repair task, such as Closed complete.

    4.  Select **Save** and close the resolution task.

    5.  Select **Continue**.

    The case moves to the Test and Resolve stage.

8.  Review the test status and resolve the service problem case.

    1.  Expand the Test summary to review the status of the test that you fixed in the Repair stage.

    2.  Expand Resolve and fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Resolution code|How the case is resolved. For example, Fixed by Support/Guidance provided.|
        |Cause|Cause of the service problem case.|
        |Resolution notes|Summarizes the resolution of service problem case.|
        |Add resolution notes to comments|Resolution notes that are available to anyone who can view the case activity stream.|

    3.  Select **Resolve case**.

    The Case highlights section is updated with the current state, such as Resolved.

9.  To view the case-related list in the playbook contextual side panel, select the **Related items**.

    The Case playbook: The horizontal stages page incorporates related list functionality into the contextual side panel. These lists appear in an accordion format that agents can expand and collapse as needed.

    For more information about the related items components, see Playbook related items component.

10. Close the service problem case.

    1.  Go to the Close stage and fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Resolution code|Code value that explains how the case is resolved. For example, Fixed by Support/Guidance provided.|
        |Resolution notes|Summarizes the resolution of service problem case.|
        |Add resolution notes to comments|Option to make the resolution notes available to anyone who can view the case activity stream.|
        |Additional comments \(Customer visible\)|Comments related to the service problem case, if any. These comments are visible to your customer who can access this case.|
        |Work notes|Information about state transitions.|

    2.  Select **Accept Solution** or **Reject Solution** based on the customer feedback.


## Result

The service problem case is resolved and closed successfully.


---
title: Diagnose and resolve a change request
description: As a customer service agent, review, diagnose, resolve, and close a change request for the service-related issue experienced by the customer.
locale: en-US
release: yokohama
product: Proactive Service Experience Workflows
classification: proactive-service-experience-workflows
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Using Proactive Service Experience Workflows, Proactive Service Experience Workflows]
---

# Diagnose and resolve a change request

As a customer service agent, review, diagnose, resolve, and close a change request for the service-related issue experienced by the customer.

## Before you begin

Role required: sn\_ind\_tsm\_sdwan.PSEW\_USER

## About this task

The change request progresses through several stages from start to closure. It begins with a PSEW user reviewing and verifying the problem. Next is the diagnosis tab, where system-specified tests are executed to identify the root cause. After the tests, the agent moves to the repair, creating a task to fix the identified issue. The PSEW user follows the instructions in the repair task to address the problem areas. Once the repair is complete, the change request is retested to confirm that the issue is resolved. Finally, the change request is resolved and closed based on the customer's feedback on the provided solution.

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

2.  Select the List icon.

3.  Navigate to **Changes** &gt; **Assigned to me**.

4.  Open the change request that is in the New or Open state.

5.  Review and verify the change request.

    1.  In the **Overview** tab, expand the **Summary**, and then review and verify the general details for the change request.

        ![change request overview.](../image/psew-change-request-overview.png)

    2.  Expand the **Scope and impact** and review the remaining details of the change request.

        |Activity|Description|
        |--------|-----------|
        |**Affected CIs**|Shows the affected configuration items \(CIs\).|
        |**Impacted Services/CIs**|Shows the impacted services.|
        |**Assets**|Shows the assets|
        |**Affected Accounts**|Shows the affected accounts.|
        |**Affected Consumers**|Shows the affected consumers|
        |**Cases**|Shows the cases|

    3.  Expand **Assignment** to view the details.

    4.  Expand **Schedule** to view the schedule.

    5.  Expand **Risk evaluation** to view the risks.

    6.  Expand **Change task** to view the details.

    The change request moves to the Diagnose stage.

6.  Diagnose the change request to identify the root-cause of the problem.

    The decision table can be configured to control the visibility of the Diagnose and Run Diagnostics contextual panel tabs. For more information about decision tables, see [Decision Tables](https://www.servicenow.com/docs/access?context=decision-table&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US).

    1.  To generate the test results, select **Run diagnostics** from the contextual panel.

    2.  In the run diagnostics panel, select **CI/Service** from the drop-down list.

        The drop-down list shows the configuration item and Affected CIs.

        To set up test definitions, see [Setting up test definitions](../../tmt-spmc/concept/settingup-test-specifications.md).

    3.  Expand the cards in the **Available test suite**.

        To set up test group, see [Setting up a test group](../../tmt-spmc/concept/setting-test-group.md).

    4.  In the manual test, select single/multiple tests.

        In the automated test, selection of test isn’t available. The subflow that is configured for the test group would be invoked.

    5.  Select **Configure**.

    6.  In the Configure tests, fill the test required characteristics form to activate the **Run test** button.

    7.  In the test, select an option either to **Run test** now or to **Schedule test** for later.

    8.  Select **Run test**.

    9.  In the diagnose tab **Test results** section, select **Refresh list** ![](../../../reuse/icons/product-icons/sync-fill-24.svg) icon.

    10. In the diagnose tab, expand the **Test results** and review the results of the tests conducted in the previous step, checking whether each test is passed or failed.

        The failed tests indicate that the issues causing the change request to be identified and need repair.

        The maximum number of rows to the group is limited to 20 rows. To configure the maximum number of rows more than 20 rows to the group, see [Presentational List Usage](https://developer.servicenow.com/dev.do#!/reference/next-experience/yokohama/now-components/now-list/usage).

    11. Select the **View Details** ![](../../../reuse/icons/product-icons/open-link-right-fill-24.svg) icon for a specific test result to review its details.

    12. Select the **Rerun test** ![](../../../reuse/icons/product-icons/arrow-clockwise-outline-24.svg) icon for a specific test result to run it again.

    13. Select **Continue**.

7.  Repair the change request by creating a new or automated repair task.

    -   Select **Generate automated task** to automatically create a repair task.
    -   Select **Create repair task** to manually create a customize repair task.
    A Repair task is created for all failed test cases related to the diagnosed change request.

    1.  Select the repair task that you want to work on.

    2.  In the Resolution task form, review the task details to identify the failed test and then work on those tests to fix the case.

    3.  In the **Select** field, select an appropriate state from the list to update or close the repair task, such as Closed complete.

    4.  Select **Save** and close the resolution task.

    5.  Select **Continue**.

8.  Review the details of the change request in the **Details** tab.

9.  View the **Change tasks** tab.

10. View the change request records in the **Related records** tab.


**Parent Topic:**[Using Proactive Service Experience Workflows](../concept/use-assurance-workflows.md)


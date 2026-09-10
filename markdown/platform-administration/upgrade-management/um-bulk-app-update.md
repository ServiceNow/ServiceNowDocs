---
title: Update multiple applications at once
description: Use the bulk application update console to review, select, and update multiple applications in a single workflow instead of updating them individually through the app manager.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/upgrade-management/um-bulk-app-update.html
release: australia
product: Upgrade Management
classification: upgrade-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 8
breadcrumb: [Bulk application updates, Configure, Upgrade Console, Upgrade, Administer the ServiceNow AI Platform]
---

# Update multiple applications at once

Use the bulk application update console to review, select, and update multiple applications in a single workflow instead of updating them individually through the app manager.

## Before you begin

Role required: upgrade\_admin

## About this task

The traditional method of updating applications requires you to navigate to the app manager, search for each application, and install updates one by one. This process becomes cumbersome as the number of applications and plugins in your system increases.

You can achieve the following:

-   View all available application updates at once
-   Select specific applications or all applications for update
-   Preview changes before applying updates
-   Run automated tests on selected updates
-   Schedule updates for a future time or apply immediately
-   Review results and troubleshoot any issues

**Note:** The update process can be time-consuming depending on the number of selected applications.

## Procedure

1.  Navigate to **Admin** &gt; **Upgrade Console**.

    The Update apps card displays the number of available updates.

2.  Review the update summary.

    -   Total number of application updates available
    -   Last sync date and time
    -   Number of store application updates
    -   Number of Now Assist application updates \(if available\)
    **Note:** Verify that the available updates match your expectations. The system syncs data with the ServiceNow store to display current version information.

3.  Select **Update now** to begin the update wizard.

    The system initializes and displays the first step of the workflow.

4.  Choose an upgrade plan.

    There are two options to choose your upgrade plan.

    -   Select an existing one: You can import update sets to apply or merge upgrade plans for your upgrades. This option is selected by default.

        In order to apply an existing upgrade plan, you have the following options:

        -   Import update sets: You must first import update sets before selecting an existing upgrade plan.
            1.  Select **Import update sets** to import an update set. The Retrieve Update Sets list shows up.
            2.  Select the Import Update Set from XML related link to select the update set to be imported. The Import XML page shows up.
            3.  Select an already existing update set using **Choose file** and then select **Upload**.

                The selected update set gets uploaded in the current upgrade plan. The current upgrade plan shows up on the Retrieve Update Sets list.

            4.  Select the plan from the Retrieve Update Sets list. The Retrieve Update Set form shows up with all its associated customer updates.
            5.  Select **Preview Update Set**. The Update Set Preview modal shows up.
            6.  Once the previewing of the update set is completed successfully, select **Commit Update Set**. The Update Set Commit modal shows up.

                **Note:** This option is visible only after the successful completion of update set preview.

        -   Select an existing upgrade plan: You can view the imported plans to choose or can select multiple plans or merge them into one plan.

            **Note:** This option considerably reduces rework with an upgrade plan, maintains accuracy and makes your upgrade process seamless.

            You will see the following modal when you select Select upgrade plan. You can then select either one upgrade plan or multiple plans to be merged and applied to the current upgrade.

            \[Omitted image "um-upgrade-plans-merge.jpeg"\] Alt text:

            **Note:** The **Apply** option is visible only when you select one upgrade plan to be applied to the current upgrade.

            \[Omitted image "um-upgrade-plans-apply.jpeg"\] Alt text:

            **Note:** The **Merge and apply** option is visible only if you have selected multiple upgrade plans. The upgrade plan name changes as per the selection of upgrade plans.

            When merging multiple upgrade plans, upgrade plan items that appear in more than one plan are used in the merged plan by their highest version. This ensures consistency and avoids version conflicts in the resulting merged plan.

    -   Create a new one: You can get started with creating a new plan for your instance upgrade.
        -   Create an upgrade plan: Select **Create a plan** to start creating the new upgrade plan. Select the Upgrade Plan link from the success message banner to view the created upgrade plan.

            **Note:** The success message banner is generated immediately after the upgrade plan is created by selecting **Create a plan** and stays visible until the page is reloaded.

            If you select the **Create a plan** option again after creating a plan, you will see the following message.

            \[Omitted image "um-override-upgrade-plan.png"\] Alt text:

            **Note:** Only the most recent upgrade plan without any upgrade plan items is retained. For example, if the most recent upgrade plan is created without upgrade plan items, it automatically overrides any earlier upgrade plan that also doesn't have upgrade plan items. There can be more than one upgrade plan with upgrade plan items.

            In the Upgrade Plans list, there can be several upgrade plans with upgrade plan items and only the recent upgrade plan with no upgrade plan items.

            **Note:** An instance can have only one active upgrade plan at a time, regardless of whether the plan includes upgrade plan items. Only the most recent upgrade plan is in active state as it automatically gets applied to the current upgrade.

        -   View generated upgrade plan: This is an alternate way to view the recently created upgrade plan. This option is helpful when you reload the page and the success message banner disappears.

            **Note:** This option is visible only after the upgrade plan is created.

    Once the upgrade plan is finally selected, the **Select upgrade plan** and **Create a new one** options are disabled.

5.  Preview and select applications for update.

    The **Preview Application Updates** step displays all available application updates. For each application, you can:

    -   **Check the checkbox** to select an application for update
    -   **Select a version** from the dropdown menu \(the system displays available versions for each application\)
    -   **Mark to latest** to update selected applications to the newest available version
    -   **Select all** to include all 214 \(or the total count in your system\) applications in this update
    Unselected items show a status of Not selected and won't be included in the update. You can unselect an application at any time without removing it from the upgrade plan—it simply marks the item as inactive.

    After selecting applications, select **Check Compatibility** to validate that selected updates are compatible with your current system configuration. This process downloads application packages from the store and performs compatibility checks.

6.  Review compatibility results.

    After the compatibility check completes, each selected application shows a compatibility status:

    -   **Compatible**: The update can be safely applied
    -   **Incompatible**: The update can't be applied due to dependency issues or platform version conflicts
    If an application is marked incompatible, you can unselect it or choose a different version. Applications not selected for update don't require compatibility checks.

7.  Conduct pre-testing with ATF \(Automated Test Framework\).

    If ATF is installed on your instance, you can run tests on the selected updates:

    1.  In the **Conduct Pre-Testing** step, select existing test suites from the available list
    2.  Select **Add to Upgrade Test Suites** to include them in your update
    3.  If ATF requires configuration \(such as a test user profile\), follow the on-screen alerts to complete setup
    4.  Mark as complete when ready to proceed
    If ATF is not installed or if you prefer to skip testing, you can proceed directly to the update step.

8.  Review the update summary before proceeding.

    The **Review Updates** page displays:

    -   Total number of selected applications
    -   Number of compatible and incompatible applications
    -   Predicted script changes and records affected
    -   Skip rules \(if configured\)
    Review this information carefully. If you need to make changes, navigate back to previous steps using the **Previous Step** button.

9.  Choose to schedule or apply the update immediately.

    In the final step before execution, select one of the following:

    -   **Update Now**: Apply all selected updates immediately
    -   **Schedule Update**: Choose a future date and time for the update to begin
    If scheduling, select the desired date and time. The system prevents you from selecting a time within the next 5 minutes. If you schedule an update and needs to be updated later, you can:

    -   Select **Schedule Update** again to reschedule for a different time
    -   Select **Cancel Update** to remove the schedule and then select **Update Now** to apply immediately
10. Monitor update progress.

    Once the update begins, the system displays:

    -   A progress bar showing the percentage complete
    -   The start time of the update
    -   Current step information \(for example, "Step 10 of 10"\)
    -   Pending test counts \(if ATF testing is in progress\)
    You can remain on this page to monitor progress, or navigate away if needed. The system continues processing updates in the background.

11. Review update results.

    When the update completes, the **Results** page displays a summary:

    -   Number of applications successfully updated
    -   Number of applications with scheduled updates \(not yet applied\)
    -   Number of applications with available updates \(not selected in this run\)
    -   Number of applications that failed during update
    For each application, you can:

    -   View the current and updated version numbers
    -   Check the post-update status \(up-to-date, scheduled, available for update, or failed\)
    -   Select the application name or status to navigate to the app manager for details
12. Conduct post-testing and troubleshooting.

    If ATF testing is enabled, the system automatically runs selected test suites after updates complete. You can:

    -   Monitor test progress in real-time
    -   View test results, including passed and failed tests
    -   If troubleshooting is enabled, investigate failed tests using the troubleshooting agent to identify root causes
    **Note:** Post-testing and troubleshooting steps may require additional plugins to be installed. Contact your system administrator if these options are unavailable.

13. Review update sets and upgrade plan details \(optional\).

    In the final step, you can:

    -   View all update sets that were created during the update process
    -   Access the upgrade plan used for this update
    -   Select **View Update Set** to see the combined update set that captured all application updates
    These details are available for reference and troubleshooting if needed in future updates.


## What to do next

After completing the update:

-   Verify that critical applications are functioning correctly
-   If failures occurred, review the post-update status and app manager details to determine remediation steps
-   If tests were skipped or failed, schedule a separate testing run or contact your development team
-   Return to the bulk application update console periodically to check for new available updates

**Parent Topic:**[Bulk application updates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/upgrade-management/um_bulk_app_update_desc.md)


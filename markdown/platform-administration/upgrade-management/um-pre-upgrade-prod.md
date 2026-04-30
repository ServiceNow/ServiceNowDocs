---
title: Implement pre-upgrade activities on a prod instance
description: Complete the pre-upgrade tasks for a successful upgrade experience on your production instance.
locale: en-US
release: zurich
product: Upgrade Management
classification: upgrade-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 9
breadcrumb: [Access guided upgrade on a production instance, Configure, Upgrade Console, Upgrade, Administer]
---

# Implement pre-upgrade activities on a prod instance

Complete the pre-upgrade tasks for a successful upgrade experience on your production instance.

## Before you begin

**Note:** For each step, you will have the option to either skip the step or mark complete and only then move to the next guided upgrade step.

Role required: admin

## Procedure

1.  Choose an upgrade plan.

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

            You will see the following modal when you select Select upgrade plan. You can then select either one upgrade plan or multiple plans to be merged and applied to the current upgrade. &lt;image&gt;

            **Note:** The **Apply** option is visible only when you select one upgrade plan to be applied to the current upgrade. The **Merge and apply** option is visible only if you have selected multiple upgrade plans. The upgrade plan name changes as per the selection of upgrade plans.

            When merging multiple upgrade plans, upgrade plan items that appear in more than one plan are used in the merged plan by their highest version. This ensures consistency and avoids version conflicts in the resulting merged plan.

    -   Create a new one: You can get started with creating a new plan for your instance upgrade.
        -   Create an upgrade plan: Select **Create a plan** to start creating the new upgrade plan. Select the Upgrade Plan link from the success message banner to view the created upgrade plan.

            **Note:** The success message banner is generated immediately after the upgrade plan is created by selecting **Create a plan** and stays visible until the page is reloaded.

            If you select the **Create a plan** option again after creating a plan, you will see the following message. &lt;image&gt;

            **Note:** Only the most recent upgrade plan without any upgrade plan items is retained. For example, if the most recent upgrade plan is created without upgrade plan items, it automatically overrides any earlier upgrade plan that also doesn't have upgrade plan items. There can be more than one upgrade plan with upgrade plan items.

            In the Upgrade Plans list, there can be several upgrade plans with upgrade plan items and only the recent upgrade plan with no upgrade plan items.

            **Note:** An instance can have only one active upgrade plan at a time, regardless of whether the plan includes upgrade plan items. Only the most recent upgrade plan is in active state as it automatically gets applied to the current upgrade.

        -   View generated upgrade plan: This is an alternate way to view the recently created upgrade plan. This option is helpful when you reload the page and the success message banner disappears.

            **Note:** This option is visible only after the upgrade plan is created.

    Once the upgrade plan is finally selected, the **Select upgrade plan** and **Create a new one** options are disabled.

2.  Preview application upgrades.

    You can preview all the store applications with their updates for your instance. If the upgrade preview generation is in progress, you can track it using the Execution tracker link.

    -   Selected Apps: You can review the following info
        -   Customized apps: Number of apps that have been customized
        -   New apps to be installed: Total number of new apps to be installed for the upgrade
        -   Apps to be upgraded: Total number of existing apps whose version need to be upgraded

            **Note:** If you have disabled Upgrade store applications to the latest version previously, the value for Apps to be upgraded depends on the manual selection of the Upgrade store applications section.

    -   Upgrade store applications

        -   Application: Name of the application
        -   Current version: Current version of the application on the instance
        -   Latest version: Latest available version of the application
        -   Upgrade Version: Selected version of the application to which you want to upgrade
        -   State: State of the application based on the selected version for the upgrade. It displays either **Compatible** or **Check compatibility** based on the selected version if its compatible or not.
        -   Status message: Provides you more information about app compatibility if there are any failures after running **Check app compatibility**.

            **Note:** If you have previously selected the automatic upgrade option, the applications are upgraded to the latest version by default.

            If you haven't selected the automatic upgrade option previously, you get an option to select the version of the application to which you want to upgrade.

        The number of Apps to be upgraded gets updated depending on the manual selection of the apps for the selected versions. For example, if you select **Set all to minimum version** for all the applications, the number of Apps to be upgraded remains unchanged. Select **Set all to latest** if you want to update all the applications to the latest version available. Ensure to check the compatibility of the apps after selecting its versions by selecting **Check app compatibility**. If an application is not compatible, modify the version to make it compatible before moving on to the next step.

        **Note:** You can proceed to the next step of the upgrade process only after checking the compatibility of the applications.

        Select **View upgrade plan** in the Selected Apps section to see all the items along with their selected versions being added to the upgrade plan at the end of this step.

        You can now edit this step by selecting **Edit step** even after marking it complete.

        **Note:** The **Edit step** option is available only when you mark this step as complete and before scheduling or starting any upgrade. Once you select **Edit step**, the next step in the Pre-upgrade process resets. You can again proceed to the next step of the upgrade process only after checking the compatibility of the applications.

    If automatic upgrade has not been opted in, you can manually select the versions of the applications to be upgraded. Select **Set all to latest** if you want to update all the applications to the latest version available. Ensure to check the compatibility of the apps after selecting its versions by selecting **Check app compatibility**. If an application is not compatible, modify the version to make it compatible before moving on to the next step.

3.  Review predicted skipped records.

    Skipped records occur when customizations on your instance prevent certain files from being automatically updated during an upgrade.

    -   Upgrade preview: You can view the current version and the previewing version of the upgrade in this section. You can also see if there is any upgrade been scheduled.
    -   Skipped record summary: You can view the following information.

        ![](../image/um-skipped-without-tests.png)

        -   Total records changed: Gives the total number of records that have changed since last upgrade. Select the Review changes link to see the list of records that have changed.
        -   Total skipped records: Shows the numbers of skipped records that have been resolved, total skipped records that need to be reviewed and the number of skipped records that have already been reviewed.
        -   Skipped records without tests: States the total number of skipped records that have tests. The Test linked link in the Skipped records section points to the list of tests of the skipped records that have associated tests.
    -   Predicted skipped records: Shows the total number of predicted skipped records
        -   Name: Name of the skipped record
        -   Product: Name of the record that the skipped record belongs to
        -   Priority:
        -   Status: Status of the skipped record if it has been resolved, reviewed or needs to be reviewed
        -   Prediction disposition: Action predicted to be performed on the skipped record during the selected upgrade.
            -   Predicted Insert: The system is predicted to insert a new record.
            -   Predicted Update: The system is predicted to update this record.
            -   Reverted: This record was reverted to the base version, and won’t be skipped on the next upgrade.
            -   Predicted Skip: The system won't change this record in order to preserve customizations.
            -   Predicted Skip \(Manual Merge\): The system won't change this record because updating it requires manual intervention.
            -   Predicted Skip \(Apply Once\): The system is predicted to skip this record because it had already applied an update from an xml file in the apply once folder.
        -   Plugin: The app id where the skipped record is found
    -   Skipped record rules editor: Use the skipped record rules editor to create skipped record rules based on the set conditions to define customizations after an upgrade.

        **Note:** This step is completed within the Review predicted skipped records step.

        ![Screenshot showing skipped record rules editor in a prod instance](../image/um-skipped-record-rules-prod.png)

        The skipped records matching the set conditions in the skipped record rules editor, perform the previously selected actions. Select **View latest upgrade history** to determine the actions and conditions to be set depending on the previous upgrades.

        The skipped record rules shows the list of skipped record rules on the instance.

        -   Name: Name of the rule
        -   Active: States if the rule is active or not
        -   Conditions: Conditions set by the rule to filter the skipped records
        -   Action: Previously chosen action for the specific rule
        -   Order: The order in which the rules are sorted
        Select **Create rule** if you want to create any additional skipped record rules.

    You can do the following in this pre-upgrade activity.

    -   Review the list of predicted skipped records in the Preview module and decide which versions of the files to be retained.
    -   You can choose some customizations to be reverted to the base version, allowing them to go through the entire upgrade process without being skipped.
    -   Ensure to review and update the list of skipped records after the upgrade.
    -   Once done with the reviewing of the skipped records, complete the next activities required in the pre-upgrade process.

**Parent Topic:**[Access guided upgrade on a production instance](um-guided-tour-implement-prod.md)


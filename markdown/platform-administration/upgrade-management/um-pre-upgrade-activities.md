---
title: Implement pre-upgrade activities on a non-prod instance
description: Complete the pre-upgrade tasks for a successful upgrade experience on your instance.
locale: en-US
release: zurich
product: Upgrade Management
classification: upgrade-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 12
breadcrumb: [Access guided upgrade on a non-production instance, Configure, Upgrade Console, Upgrade, Administer]
---

# Implement pre-upgrade activities on a non-prod instance

Complete the pre-upgrade tasks for a successful upgrade experience on your instance.

## Before you begin

**Note:** For each step, you will have the option to either skip the step or mark complete and only then move to the next guided upgrade step.

Role required: admin

## Procedure

1.  Select **View release notes** if you want to review the release notes of the selected Guided upgrade version.

    **Note:** This step is visible only if you are in a non-production instance.

2.  Request a clone.

    **Note:** This step is visible only if you are in a non-production instance. It is recommended to clone the production instance to non-production instance. Select **Request clone** to configure the source and target instances.

    **Note:** For data integrity and recovery purposes, it is recommended that the update sets should be either closed out or backed up. It is crucial for preserving all system modifications and enabling restoration when required.

    You can also see the cloning summary information that tells you the instance you have cloned and other relevant information. You can see the start and end time of the cloning process. By default, you are in the America/Los Angeles timezone. You can modify the timezone preference by navigating to **User Menu** &gt; **Preferences** &gt; **Language &amp; Region**. You can then select the required timezone from the drop down menu.

    There are four different scenario for the cloning process.

    -   No clone has been scheduled for this instance

        ![](../image/um-clone-not-scheduled.png)

    -   Scheduled
    -   Running

        ![](../image/um-clone-running.png)

    -   Complete

        ![](../image/um-clone-completed.png)

    **Note:** If the cloning process is in progress, the **Skip** and **Mark as complete** options are disabled.

    A list of production instances shows up and you can select the instance you want to clone.

    **Note:** If you are in a production instance, the list of instances for cloning doesn’t show up.

    You can expect the following in this pre-upgrade activity once you select the instance to be cloned.

    -   You will be redirected to the Cloning tool to initiate the cloning process.
    -   The Cloning tool guides you through the cloning process of your production instance.
    -   You will be reminded to ensure to back up the update sets before starting the cloning process to save any changes and configurations.
3.  Choose an upgrade plan.

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

            ![](../image/um-upgrade-plans-merge.jpeg)

            **Note:** The **Apply** option is visible only when you select one upgrade plan to be applied to the current upgrade.

            ![](../image/um-upgrade-plans-apply.jpeg)

            **Note:** The **Merge and apply** option is visible only if you have selected multiple upgrade plans. The upgrade plan name changes as per the selection of upgrade plans.

            When merging multiple upgrade plans, upgrade plan items that appear in more than one plan are used in the merged plan by their highest version. This ensures consistency and avoids version conflicts in the resulting merged plan.

    -   Create a new one: You can get started with creating a new plan for your instance upgrade.
        -   Create an upgrade plan: Select **Create a plan** to start creating the new upgrade plan. Select the Upgrade Plan link from the success message banner to view the created upgrade plan.

            **Note:** The success message banner is generated immediately after the upgrade plan is created by selecting **Create a plan** and stays visible until the page is reloaded.

            If you select the **Create a plan** option again after creating a plan, you will see the following message.

            ![](../image/um-override-upgrade-plan.png)

            **Note:** Only the most recent upgrade plan without any upgrade plan items is retained. For example, if the most recent upgrade plan is created without upgrade plan items, it automatically overrides any earlier upgrade plan that also doesn't have upgrade plan items. There can be more than one upgrade plan with upgrade plan items.

            In the Upgrade Plans list, there can be several upgrade plans with upgrade plan items and only the recent upgrade plan with no upgrade plan items.

            **Note:** An instance can have only one active upgrade plan at a time, regardless of whether the plan includes upgrade plan items. Only the most recent upgrade plan is in active state as it automatically gets applied to the current upgrade.

        -   View generated upgrade plan: This is an alternate way to view the recently created upgrade plan. This option is helpful when you reload the page and the success message banner disappears.

            **Note:** This option is visible only after the upgrade plan is created.

    Once the upgrade plan is finally selected, the **Select upgrade plan** and **Create a new one** options are disabled.

4.  Automate upgrade tasks.

    There are two different kinds of upgrade tasks in this step.

    -   Default automated tasks: These tasks are completed automatically.
        -   Generate upgrade preview: It helps you understand how your instance will be impacted after the upgrade even without having it really upgraded.
        -   Create upgrade update sets: The automatic creation of the upgrade update sets capture changes and helps during review of the skipped records.
    -   Optional automated tasks: You have the option of completing these tasks automatically.
        -   Generate the ATF tests: Automatic generation of the ATF tests using the ATF test generator and cloud runner store application.

            **Note:** These ATF tests run automatically post-upgrade.

        -   Upgrade store applications to the latest version: By default, all the applications are being upgraded to the latest version. If you don’t want them to be upgraded to the latest version, you can disable the toggle and manually select a compatible version during the store application upgrade step.
5.  Conduct pre-testing.

    This step captures all the tests required to be executed after the upgrade.

    -   Generate tests: Auto-generates regression tests with the use of ATF Test generator tool. You can review the start time and the total time to complete the test generation.

        **Note:** The auto-generated ATF test suites are added to the Upgrade Test Suites table and are executed automatically post-upgrade.

        Select **Status** to check the status of the generated tests. You can also cancel the test generation process by selecting **Cancel**.

    -   Create additional tests: Review the existing tests or create additional tests to complete upgrade faster.
    -   Upgrade test suites: The auto-generated regression tests in the Generate tests section are added here automatically when they are generated. You can also add more tests by selecting it from the Available test suites table section.
    -   Available test suites: Review the list of available test suites. You can also select the tests you want to add to the Upgrade test suites section. Only the selected tests are executed automatically after the upgrade.

        ![Screenshot showing the available test suites](../image/um-available-test-suites.png)

        **Note:** The available test suites are already successfully passed test suites.

6.  Preview application upgrades.

    You can preview all the store applications with their updates for your instance. If the upgrade preview generation is in progress, you can track it using the Execution tracker link.

    -   Selected Apps: You can review the following information:
        -   Customized apps: Number of apps that have been customized
        -   New apps to be installed: Total number of new apps to be installed for the upgrade
        -   Apps to be upgraded: Total number of existing apps whose version need to be upgraded

            **Note:** If you have disabled Upgrade store applications to the latest version previously, the value for Apps to be upgraded depends on the manual selection of the Upgrade store applications section.

    -   Upgrade store applications

        ![Screenshot showing upgrade store apps](../image/um-upgrade-store-apps.png)

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

7.  Review predicted skipped records.

    Skipped records occur when customizations on your instance prevent certain files from being automatically updated during an upgrade.

    Select **Regenerate Preview** to regenerate a preview either for all the applications or for only the modified applications in the previous step.

    **Note:** Set the glide.upgrade\_center.regenerate\_upgrade\_preview property to `true` to regenerate the preview for all the apps.

    -   Upgrade preview: You can view the current version and the previewing version of the upgrade in this section. You can also see if there is any upgrade been scheduled.
    -   Skipped record summary: You can view the following information.

        ![Screenshot showing the skipped record summary](../image/um-skipped-record-summary.png)

        -   Total records changed: Gives the total number of records that have changed since last upgrade. Select the Review changes link to see the list of records that have changed.
        -   Total skipped records: Shows the numbers of skipped records that have been resolved, total skipped records that need to be reviewed and the number of skipped records that have already been reviewed.
        -   Skipped records without tests: States the total number of skipped records that have tests. The Test linked link in the Skipped records section points to the list of tests of the skipped records that have associated tests.
    -   Predicted skipped records: Shows the total number of predicted skipped records

        ![Screenshot showing the predicted skipped records list](../image/um-predicted-skipped-test-link.png)

        -   Name: Name of the skipped record
        -   Product: Name of the record that the skipped record belongs to
        -   Status: Status of the skipped record if it has been resolved, reviewed or needs to be reviewed
        -   Test linked: Links to the list of test associated with the skipped record. It helps you know the reason why a certain record has been skipped by viewing all the tests associated with the skipped record.
        -   Prediction disposition: Action predicted to be performed on the skipped record during the selected upgrade.
            -   Predicted Insert: The system is predicted to insert a new record.
            -   Predicted Update: The system is predicted to update this record.
            -   Reverted: This record was reverted to the base version, and won’t be skipped on the next upgrade.
            -   Predicted Skip: The system won't change this record in order to preserve customizations.
            -   Predicted Skip \(Manual Merge\): The system won't change this record because updating it requires manual intervention.
            -   Predicted Skip \(Apply Once\): The system is predicted to skip this record because it had already applied an update from an xml file in the apply once folder.
    -   Skipped record rules editor: Use the skipped record rules editor to create skipped record rules based on the set conditions to define customizations after an upgrade.

        **Note:** This step is completed within the Review predicted skipped records step.

        The skipped records matching the set conditions in the skipped record rules editor, perform the previously selected actions. Select **View latest upgrade history** to determine the actions and conditions to be set depending on the previous upgrades.

        ![Screenshot showing the skipped record rules editor](../image/um-record-rule-editor.png)

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

**Parent Topic:**[Access guided upgrade on a non-production instance](um-guided-tour-implement.md)

**Related topics**  


[Implement instance upgrade activities on a sub-prod instance](um-implement-instance-upgrade.md)

[Implement post-upgrade activities on a non-prod instance](um-post-upgrade-activities.md)


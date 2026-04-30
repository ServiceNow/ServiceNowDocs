---
title: Implement post-upgrade activities on a non-prod instance
description: Implement the post-upgrade tasks for a successful upgrade completion on your instance.
locale: en-US
release: zurich
product: Upgrade Management
classification: upgrade-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Access guided upgrade on a non-production instance, Configure, Upgrade Console, Upgrade, Administer]
---

# Implement post-upgrade activities on a non-prod instance

Implement the post-upgrade tasks for a successful upgrade completion on your instance.

## Before you begin

**Note:** You will be able to perform the post-upgrade tasks only after completing the pre-upgrade and instance upgrade tasks.

Role required: admin

## Procedure

1.  Review skipped records.

    You can review the skipped records that were identified during the pre-upgrade steps and during the upgrade. You can see the following information:

    -   Skipped records summary: This section shows the summary of all the skipped records
        -   Total records changed: States the total number of records that have been changed since last upgrade. Select Review changes link if you want to see the changes in the records.
        -   Total skipped records: States the total number of records that have been skipped during the upgrade. It also shows the number of records that have already been reviewed and need to be reviewed.
        -   Skipped records without tests: States the total number of skipped records that have tests. The Test linked link in the Skipped records section points to the list of tests of the skipped records that have associated tests.
    -   Skipped records: This section shows the list of records that have been skipped during the upgrade.
        -   Name: Name of the skipped file
        -   Product: Name of the product where the skipped file belongs to
        -   Priority: Priority of the skipped record to get it resolved
        -   Status: States if the skipped file has been reviewed or not
        -   Test linked: Links to the list of test associated with the skipped record. It helps you know the reason why a certain record has been skipped by viewing all the tests associated with the skipped record
        -   Predicted Disposition: Action performed on the skipped record during the upgrade
        -   Assigned to: Owner of the skipped record

            **Note:** Select **Assign** to assign a skipped record to get it resolved.

        -   Plugin: The app id where the skipped record is found
2.  Store application upgrades.

    You can now view the list of applications that have been upgraded depending on the selections made in the Preview application upgrades step in the Pre-upgrade stage.

    **Note:** It is to be noted that the applications that were not selected during the preview or dont have a newer version available are not listed.

    You can see the following information in this task.

    -   App updates: Summary of the applications.
        -   Total apps: Total apps the current instance has
        -   Apps updated: Total apps that got upgraded during the upgrade or post upgrade
        -   Apps to be updated: Total apps that have updates but are yet to be upgraded
        -   Scheduled Apps: Total selected apps for scheduled upgrade at later point of time
    -   Upgrade store applications: List of applications that have been selected in the pre-upgrade stage and have updated versions available.

        ![Screenshot showing app updates](../image/um-store-app-upgrades.png)

        -   Application: Name of the application
        -   Upgrade version: Selected version of the application to which you want to upgrade. This was selected before upgrade starts in preview apps page
        -   Upgrade status: States if the application is in the Store

            **Note:** The applications that are installed on the instance show up at the end of the applications list.

        -   Current version: States the current version of the application
        -   Available versions: States the most updated version available for upgrade
        -   Post upgrade status: States the status of the application. For example, the status indicates whether an application update is Scheduled, Update Available, or already Updated. You can also see the version for the scheduled applications.
    Select **Update selected apps** to upgrade the selected apps to the available version immediately. You can also schedule the upgrades by selecting **Schedule updates**. You can also search for an application based on its name or status.

    Use **Sync Now** to update the list of installed applications that were added or upgraded outside the upgrade process. For example, if you install or update an app through the App Manager, select **Sync Now** to reflect the latest application status.

3.  Conduct post-testing.

    In order to conduct post-testing, the selected ATF tests are executed to ensure system functionality and integrity of the existing features.

    ![Screenshot showing the post testing scenario](../image/um-post-testing.png)

    You can review the following information in this step:

    -   Still need additional tests: You can review the existing tests and add more tests if required for a seamless and faster upgrade. You can either import existing ATF tests or create new test suites.

        **Note:** The created tests or test suites are added to the Upgrade test suite table for consolidated testing.

    -   Post-testing highlights: This section states the number of total tests, passed and failed tests, and the skipped records during the upgrade process. You can also select View successful tests and View failed tests links to see the list of tests that passed or failed. Select View skipped tests to view the list of all the skipped tests in the upgrade.
    -   Upgrade test suite: This section lists the recently created test suites that were additional tests for faster upgrade.
        -   Name: Name of the test suite
        -   Description: Description of the test suite
        -   Status: Status of the test suite if it has been tested or not
        -   Generated: States if it has been generated or recently created
        -   Start time: States the start time of testing of the test suite
        -   Duration: States the total duration for the testing of the test suite
4.  Prepare next environment.

    In this step, you can see the currently selected upgrade plan. You then prepare the update set and export it to the next production or non-production instance. This task is used to ensure that all necessary modifications are applied to the next production or non-production instance.

    ![Screenshot showing next environment](../image/um-next-environment.png)

    You can see the following information in this task:

    -   Prepare update sets for transfer: Check the Update Sets Table and ensure that your update sets are in Complete state. Once they are completed, you can move the update sets to the next production or non-production instance. If you have created new update sets and included other apps customizations, you can manually export them to the next instance. Select **View all update sets** to review your update sets in the Update Sets Table table.
    -   View generated upgrade plan: View the upgrade plan created automatically for you to install in the next environment. Select **View update plan** to review the update plan that has been created for you.
    -   View your update set: Commit the selected update set to the next environment to apply your configurations. Select **View update set** to download the update set.

        **Note:** The selection made during the Pre-upgrade tasks for your applications are automatically included.

5.  Select **Mark as complete** to complete the sub-production tasks in a non-production instance.


**Parent Topic:**[Access guided upgrade on a non-production instance](um-guided-tour-implement.md)

**Related topics**  


[Implement pre-upgrade activities on a non-prod instance](um-pre-upgrade-activities.md)

[Implement instance upgrade activities on a sub-prod instance](um-implement-instance-upgrade.md)


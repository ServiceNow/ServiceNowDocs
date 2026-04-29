---
title: Implement post-upgrade activities on a prod instance
description: Implement the post-upgrade tasks for a successful upgrade completion on your production instance.
locale: en-US
release: australia
product: Upgrade Management
classification: upgrade-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Access guided upgrade on a production instance, Configure, Upgrade Console, Upgrade, Administer the ServiceNow AI Platform]
---

# Implement post-upgrade activities on a prod instance

Implement the post-upgrade tasks for a successful upgrade completion on your production instance.

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
        -   Priority: Priority of the skipped records in which they are reviewed
        -   Status: States if the skipped file has been reviewed or not
        -   Predicted Disposition: Action performed on the skipped record during the upgrade
2.  Store application upgrades.

    You can now view the list of applications that have been upgraded depending on the selections made in the Preview application upgrades step in the Pre-upgrade stage.

    **Note:** It is to be noted that the applications that were not selected during the preview or don’t have a newer version available are not listed.

    You can see the following information in this task.

    -   Upgrade store applications: List of applications that have been selected in the pre-upgrade stage and have updated versions available.
    -   App updates: List of applications that have failed the upgrade.
        -   Application: Name of the application
        -   Upgrade version: The version that has been selected for the application before the upgrade starts in preview apps page
        -   Upgrade status: States if the application is in the Store
        -   Current version: States the current version of the application
        -   Available versions: States the most updated version available for upgrade
        -   Post upgrade status: States that if the application version is up to date after post upgrade
3.  Validate your upgrade.

    Conduct User Accepting Testing \(UAT\) to ensure that the production instance is performing as expected after the upgrade.

    ![](../image/um-validate-upgrade-prod.png)

4.  Select **Mark as complete** to complete the production tasks in a production instance.


**Parent Topic:**[Access guided upgrade on a production instance](um-guided-tour-implement-prod.md)


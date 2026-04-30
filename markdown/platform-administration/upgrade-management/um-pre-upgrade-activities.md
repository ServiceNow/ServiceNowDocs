---
title: Implement pre-upgrade activities
description: Complete the pre-upgrade tasks for a successful upgrade experience on your instance.
locale: en-US
release: yokohama
product: Upgrade Management
classification: upgrade-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Access guided setup for Upgrade Console, Configuring Upgrade Console, Upgrade Console, Upgrade, Administer the ServiceNow AI Platform]
---

# Implement pre-upgrade activities

Complete the pre-upgrade tasks for a successful upgrade experience on your instance.

## Before you begin

**Note:** For each step, you will have the option to skip the step or mark complete and only then move to the next guided setup step.

Role required: admin

## Procedure

1.  Select **Read release notes** if you want to review the release notes of the selected Guided setup version.

2.  Request a clone.

    Select **Clone Admin Console** to request a clone.

    **Note:** It is recommended to clone your production instance to your sub-production instance if you haven't cloned in a while.

    You can expect the following in this pre-upgrade activity.

    -   You will be redirected to the Cloning tool to initiate the cloning process.
    -   The Cloning tool guides you through the cloning process of your production instance.
    -   You will be reminded to ensure to back up the update sets before starting the cloning process to save any changes and configurations.
3.  Test your instance.

    Ensure that your instance is ready for the upgrade by testing with either of the following methods.

    -   Test generator: Auto-generate an ATF test by selecting the auto-generate option either from the Auto-generate Tests module or Tests/Suites modules.
    -   Create a new test: Create a new ATF test that has a series of test steps to be executed.
    -   Test tables: Add, edit or run a test from a test table. You can also open an individual test record and can view and edit the test steps within the parent test.
4.  Review predicted skipped records.

    Skipped records occur when customizations on your instance prevent certain files from being automatically updated during an upgrade.

    You can do the following in this pre-upgrade activity.

    -   Review the list of predicted skipped records in the Preview module and decide which versions of the files to be retained.
    -   You can choose some customizations to be reverted to the base version, allowing them to go through the entire upgrade process without being skipped.
    -   Ensure to review and update the list of skipped records after the upgrade.
    -   Once done with the reviewing of the skipped records, complete the next activities required in the pre-upgrade process.
5.  Schedule your upgrade.

    You can schedule your upgrade for a later time and date.

    You can do the following in this pre-upgrade activity.

    -   Set a time and date for an upgrade as per your organization's schedule. It is recommended to avoid peak usage times and critical development periods.
    -   Identify periods of low activity by reviewing and analyzing usage patterns and data.
    -   Ensure all relevant people are in agreement with the scheduled upgrade time.

**Parent Topic:**[Access guided setup for Upgrade Console](um-guided-tour-implement.md)

**Related topics**  


[Implement post-upgrade activities](um-post-upgrade-activities.md)


---
title: Implement post-upgrade activities
description: Implement the post-upgrade tasks for a successful upgrade completion on your instance.
locale: en-US
release: yokohama
product: Upgrade Management
classification: upgrade-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Access guided setup for Upgrade Console, Configuring Upgrade Console, Upgrade Console, Upgrade, Administer the ServiceNow AI Platform]
---

# Implement post-upgrade activities

Implement the post-upgrade tasks for a successful upgrade completion on your instance.

## Before you begin

**Note:** You will be able to perform the post-upgrade tasks only after completing the pre-upgrade tasks.

Role required: admin

## Procedure

1.  Test your instance.

    Ensure that your instance is working as expected post upgrade by testing with either of the following methods.

    -   Test generator: Auto-generate an ATF test by selecting the auto-generate option either from the Auto-generate Tests module or Tests/Suites modules.
    -   Create a new test: Create a new ATF test that has a series of test steps to be executed.
    -   Test tables: Add, edit or run a test from a test table. You can also open an individual test record and can view and edit the test steps within the parent test.
2.  Review skipped records.

    If you have customized or updated an affected record, the upgrade generates a skipped record log.

    **Note:** It is recommended to resolve the differences between the upgraded and customized versions of the records by processing the skipped records.

    You can do the following in this post-upgrade activity.

    -   Create an update set to record all the changes in the skipped records

        **Note:** This ensures the recording of any resolutions made to the skipped records and can be tracked easily.

    -   Examine every skipped record and decide on the version to be retained.
    -   Resolve all the conflicts between customized and upgraded versions.

        **Note:** Once the upgrade is completed, you can view the list of records causing conflicts on your instance in the Monitor module.

    -   Finalize the update set and export it for future use.

**Parent Topic:**[Access guided setup for Upgrade Console](um-guided-tour-implement.md)

**Related topics**  


[Implement pre-upgrade activities](um-pre-upgrade-activities.md)


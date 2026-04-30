---
title: Phase 6 - Prepare to upgrade the production instance
description: After you have configured and refined your test environment to be a good representation of your production environment, prepare to upgrade your production instance.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Upgrade to the Zurich release, Zurich release notes]
---

# Phase 6 - Prepare to upgrade the production instance

After you have configured and refined your test environment to be a good representation of your production environment, prepare to upgrade your production instance.

## Before you begin

Role required: admin.

To ensure that all stakeholders in your company are prepared for the final production upgrade, complete the administrative planning tasks in Phase 6 of the [Upgrade planning checklist](../upgrades-planning-checklist.md). When upgrading a production instance:

-   Obtain confirmation from IT and management that all non-production instance defects have been fixed, validated, and included in an update set.
-   Use the change management process established by your organization to track the upgrade.
-   Communicate effectively with your user community regarding changes, new features, and process updates resulting from the upgrade.
-   Negotiate a suitable upgrade time for all users of the ServiceNow system.

    For example, schedule the upgrade after hours, to minimize impact to your users. Remember to schedule the upgrade to occur 15–20 minutes before the [**Upgrade** scheduled job](upgrades-phase-3.md#Phase3Step1CheckUpgradeJob) interval.

-   Allow time in your change window to run all test cases and validate that all integrations, key business functionality, and system performance are acceptable. Add a time buffer for responding to errors without breaching the change window.

## About this task

![Upgrade progress bar](../image/progress-bar-phase-6.png)

## Procedure

1.  Profile the performance of your instance before upgrading.

    Pre-upgrade instance validation can provide a reliable benchmark of the current operating environment and alert you to any issues that may appear after the upgrade. For example, it sometimes appears that specific functionality is broken by an upgrade. Analysis might show that the functionality did not work properly in the production instance, even before the upgrade.

    Before performing the upgrade, analyze the current operating environment. Specifically, review:

    -   Key functionality
    -   Integrations
    -   Instance performance
2.  Use the ServiceNow Performance homepage to document the performance of your instance before the upgrade.

    You will later compare and contrast this information during your post-upgrade validation and testing. Benchmarks will be different for each of your instances.

    To access the ServiceNow Performance homepage:

    1.  Log in to your instance.

    2.  From the list in the top left of the instance homepage, select **ServiceNow Performance**.

        ![](../image/upgrades-perf-dashboard.png)

3.  On your clone, perform functional testing and monitor the performance of your instance.

    Replicate typical user behaviors that occur on your production instance. Assign a consistent core team of power users and key stakeholders to validate important functionality in the ServiceNow instance before and after upgrades.



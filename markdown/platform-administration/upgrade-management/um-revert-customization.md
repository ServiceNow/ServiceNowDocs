---
title: Revert a customization
description: To prevent customizations from being overwritten by system upgrades, the upgrade process automatically skips changes to objects that have been customized. You may want to overwrite your customizations when a software upgrade contains a feature that you would like to implement.
locale: en-US
release: yokohama
product: Upgrade Management
classification: upgrade-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Reviewing upgrade history, Upgrade History tool in Upgrade Console, Upgrade Console tools, Using Upgrade Console, Upgrade Console, Upgrade, Administer the ServiceNow AI Platform]
---

# Revert a customization

To prevent customizations from being overwritten by system upgrades, the upgrade process automatically skips changes to objects that have been customized. You may want to overwrite your customizations when a software upgrade contains a feature that you would like to implement.

## Before you begin

Role required: admin

## About this task

To identify customized objects, the system adds a corresponding record in the Customer Updates \[sys\_update\_xml\] table. The table maintains the current version information for all objects that have been customized. The upgrade process skips changes to objects that have entries in the table. The upgrade process does not skip objects if only excluded fields have changed.

## Procedure

1.  Navigate to Upgrade History using one of the following ways.

    |Option|Navigation|
    |------|----------|
    |Using left navigation|Navigate to **All** &gt; **Admin Center** &gt; **Upgrade Management** &gt; **Upgrade History**.|
    |Using Admin tab option|Navigate to **Admin** &gt; **Upgrade Management** &gt; **Upgrade History**.|

    A list of upgrades is displayed.

2.  Select the desired software version.

3.  Filter the Upgrade Details related list by **Disposition is Skipped**.

4.  Add another filter condition for **Changed is True** to return only the objects that have changed since the last upgrade.

5.  Select the update record to implement.

    The **File differences** field displays a side-by-side comparison of the customization and the default version. Deletions are highlighted in red, additions in green, and modifications in yellow.

6.  Click **Revert to base system** to overwrite your customized object with the system default version.

    -   The **Disposition** changes from **Skipped** to **Reverted**.
    -   After you revert a customization, you have the option to click **Reapply Changes** to reapply your customizations \(undo the revert\).

**Parent Topic:**[Reviewing upgrade history](../concept/um-review-history.md)


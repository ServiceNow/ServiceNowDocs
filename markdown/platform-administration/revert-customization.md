---
title: Revert a customization
description: To prevent customizations from being overwritten by system upgrades, the upgrade process automatically skips changes to objects that have been customized. You may want to overwrite your customizations when a software upgrade contains a feature that you would like to implement.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Customizations Unchanged related list, Upgrade History module: Track every upgrade, Upgrades and conversions, Upgrade, Administer the ServiceNow AI Platform]
---

# Revert a customization

To prevent customizations from being overwritten by system upgrades, the upgrade process automatically skips changes to objects that have been customized. You may want to overwrite your customizations when a software upgrade contains a feature that you would like to implement.

## Before you begin

Role required: admin

## About this task

To identify customized objects, the system adds a corresponding record in the Customer Updates \[sys\_update\_xml\] table. The table maintains the current version information for all objects that have been customized. The upgrade process skips changes to objects that have entries in the table. The upgrade process does not skip objects if only excluded fields have changed.

## Procedure

1.  Navigate to **All** &gt; **System Diagnostics** &gt; **Upgrade History**.

2.  Select the desired software version.

3.  Filter the Upgrade Details related list by **Disposition is Skipped**.

4.  Add another filter condition for **Changed is True** to return only the objects that have changed since the last upgrade.

5.  Select the update record to implement.

    The **File differences** field displays a side-by-side comparison of the customization and the default version. Deletions are highlighted in red, additions in green, and modifications in yellow.

6.  Click **Revert to base system** to overwrite your customized object with the system default version.

    -   The **Disposition** changes from **Skipped** to **Reverted**.
    -   After you revert a customization, you have the option to click **Reapply Changes** to reapply your customizations \(undo the revert\).
    -   During replace on upgrade, no changes are made to the update\_exempt fields like the **Active** field. The rest of the record receives the update.

        **Note:** If the attribute is not explicitly specified as an update\_exempt field, the **Active** field on a tracked table is treated as update\_exempt by default.

        Since we skip updating update\_exempt fields, two versions of the record in the sys\_update\_version table are generated.

        -   The version record with the source '\_to\_platform\_version\_' contains the payload from ServiceNow without any modifications. \(State= HISTORY\)
        -   The version record with the previous customization source, for example, '\_update\_set\_', that has the customer's customizations overridden by the values from the incoming ServiceNow version, except for the update\_exempt fields. The customer's customizations for update\_exempt fields are preserved in this version. \(State= CURRENT\)

**Parent Topic:**[Customizations Unchanged related list](../concept/customizations-unchanged-related-list.md)

**Related topics**  


[Update set administration](https://www.servicenow.com/docs/access?context=update-set-administration&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US)


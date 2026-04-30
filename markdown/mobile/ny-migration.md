---
title: Resolve common issues in mobile migration script results
description: Find solutions to common issues after running the mobile migration script.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Migrate to New York &amp; later, Plugins &amp; upgrades, Considerations before implementation, Configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Resolve common issues in mobile migration script results

Find solutions to common issues after running the mobile migration script.

## Log error messages

The mobile migration script adds entries to the Log \[syslog\] table when it encounters an error. You can review these logs by navigating to **System Logs** &gt; **System Log** &gt; **All**. Listed here are errors the mobile migration script may add to the logs.

|Error Message|Resolution|
|-------------|----------|
|Invalid instance scope provided|If you see this message, the migration script was aborted. Run the migration script again to complete the migration. You can do rerun the migration script by reopening Studio and selecting the scope.|
|Please activate com.glide.mobile-employee first before migration.|The ServiceNow NowMobile App Screens and Applet Launcher \[com.glide.mobile-employee\] plugin must be active to run the migration script. Ensure that this plugin is active. If you see this message, the migration script was aborted. Run the migration script again to complete the migration.|
|Cannot perform migration task on customized record.|The record causing this error appears immediately after this message. A customization on this record prevented the migration script from changing this file. The migration script skips this file, and continues to run. The named file is inaccessible in Studio.|

## Collisions

Collisions can occur in base system applications that you have customized before the upgrade to New York or later versions. If the migration script detects any collisions, it prompts you to review them after the script execution completes.

![Mobile migration collision prompt.](../image/migration-collision-prompt.png)

Click the **View Collisions** button to view a filtered list of upgrade details \[sys\_upgrade\_history\_log\] records. This list shows the records within the current scope that the upgrade process has skipped. To resolve a conflict, click a record on this list to open the record, then click the **Resolve Conflicts** button.

The **Resolve Conflicts** form shows the base system version of the record alongside the customized version Fields that are different between versions are highlighted with a darker background.

![Resolve conflicts form.](../image/resolve-conflicts.png)

Use the arrow buttons \(![Arrow button](../image/migrate-arrow.png)\) to move values from one version to the other. After making your changes, click the **Save Merge** button to save your changes. You can also click the **Revert to Base System** button to discard your customizations and use the unmodified version of the record.

A common collision issue is master detail \[sys\_sg\_master\_detail\_screen\] records. Master details records are no longer a part of the mobile schema as of the New York release. These records are replaced with new list \[sys\_sg\_list\_screen\] and form \[sys\_sg\_form\_screen\] screen records. They are normally deleted as part of the upgrade process, but if they have been customized, the script does not automatically delete them. If you have, for example, renamed a base system application, this kind of collision can occur.

To resolve the issue, check Mobile Studio to make sure that your applet is still available and working as expected. Once you have confirmed that the applet is available, you can delete the main detail record.

## Common migration issues

-   **An applet is missing**

    After migration, your applets should be visible in the **Applications** tab in the navigation bar. If the applets do not appear, you can manually migrate these applets.

    1.  In Studio, open **Mobile Studio** &gt; **Application Menu** in the application explorer, and select the app where you are missing an applet.
    2.  In the **Navigation Tabs** related list, click the **Applications** navigation tab.
    3.  Note the **Applet Launcher** associated with the **Applications** tab.
    4.  In Studio, open **Mobile Studio** &gt; **Applet Launchers**, and open the applet launcher noted in the last step.
    5.  In the applet launcher form, select a UI section with the same name as the folder the missing applet was located in before the migration.
    6.  Find the missing applet in the **All Applets** list, and move it to the **Selected Applets** list.
    7.  Click Save.
-   **A related list is missing from an applet**

    This issue may be the result of an outdated reference on the related lists mapping \[sys\_sg\_related\_list\_map\] table. You can re-associate the **Destination Screen** for your related list to resolve the issue.

    1.  In Studio, navigate to **Mobile Studio** &gt; **Applets**, and select the applet with the missing segment.
    2.  Click the **Form Screen** tab.
    3.  Click **Body**.
    4.  Click the **Related Lists** button.
    5.  Check the list for items that have an empty **Destination Screen** value.
    6.  Click the list item, and select a value in the **Destination Screen** field.
-   **Users are not prompted to enter input parameters in Field Service Management or ITSM applets**

    Normally parametrized applets prompt your users for a value. If you are no longer seeing this prompt after a migration, use these steps to correct the issue.

    1.  Open the UI Parameter \[sys\_sg\_ui\_parameter\] list by entering `sys_sg_ui_parameter.list` in the filter navigator for your instance.
    2.  Find the parameter which is not generating a prompt for your users.
    3.  Check the value of the **Screen** field. If this field appears empty, it may be pointing to a Master-detail screen \[sys\_sg\_master\_detail\_screen\] record.
    4.  Update the field by selecting the applet \[sys\_sg\_screen\] record used by this parameter.
-   **Incorrect results for a customized Field Service Management or ITSM applet.**

    This issue can occur if you have added a customer parameter to a base system.

    1.  Open the Screen Parameters mappings \[sys\_sg\_screen\_param\_map\] list by entering `sys_sg_screen_param_map.list` in the filter navigator for your instance.
    2.  Find the record with the **Item Parameter** field matching the item parameter you have added to your data item.
    3.  Check the value of the **Screen** field. If this field appears empty, it may be pointing to an unused Master-detail screen \[sys\_sg\_master\_detail\_screen\] record.
    4.  Update the field by selecting the applet \[sys\_sg\_screen\] record used by this parameter.

**Parent Topic:**[Mobile migration from Madrid to New York and later releases](../concept/sg-mobile-migration-ny.md)


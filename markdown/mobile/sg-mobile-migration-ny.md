---
title: Mobile migration from Madrid to New York and later releases
description: Migrate your mobile applications in New York or later releases to take advantage of the improved features and continue editing within Studio.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 7
breadcrumb: [Mobile plugins and upgrades, Considerations before implementation, ServiceNow Mobile Platform configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Mobile migration from Madrid to New York and later releases

Migrate your mobile applications in New York or later releases to take advantage of the improved features and continue editing within Studio.

## Changes made during your upgrade

During the upgrade from Madrid to New York or later releases, the instance updates to the new mobile hierarchy by activating the Mobile Agent Native Client \[com.glide.sg.agent\_native\_client\] plugin. This installation creates the following changes:

-   **Native clients**

    Adds the Native Clients \[sys\_sg\_native\_client\] table. Records on this table represent the available native clients; Mobile Agent, Now Mobile, and Mobile Onboarding.

-   **Navigation bar**

    Adds the navigations \[sys\_sg\_navigation\] table. Records on this table represent a navigation bar for each of the native clients. Records on this table during the migration have their **Legacy application** \[legacy\_application\] field enabled.

-   **Notifications tab**

    Adds the notifications tabs \[sys\_sg\_notifications\_tab\] table. Records on this table represent a tab for notifications on each navigation bar.

-   **Settings tab**

    Adds the settings tabs \[sys\_sg\_settings\_tab\] table. Records on this table represent a tab for settings on each navigation bar.


![New elements introduced in the upgrade to New York](../image/upgrade-table-changes.png)

This upgrade includes new features such as application launchers and a configurable navigation bar. Any unmodified base system mobile applications installed on your instance are automatically updated to work with the new design, and can be used with Studio right away. For more detail on the mobile hierarchy used in New York and later, see [Mobile hierarchy](mobile-hierarchy.md).

Modified base system applications, and applications that you have created in Madrid will continue to work after the upgrade. These applications will not be configurable in Studio until after you have run the mobile migration script.

## Post-upgrade considerations

After an upgrade, consider the following information to confirm that your mobile implementation is working as expected, and ensure that mobile migration script runs.

-   **Modified base system applications**

    Document any changes you have made to mobile applications provided by ServiceNow, as well as any applications you have created. Test each of these applications to ensure that they continue to function as you expect.

-   **Use the Debug Upgrade feature**

    The debug upgrade feature can help you to quickly diagnose upgrade issues. For information on this feature, see Debug upgrade.

    A video training course on this tool is available. To view this course, see [Using Debug Upgrade](https://nowlearning.service-now.com/lxp?id=overview&sys_id=f6f64ed9db123700760a7104399619c8&type=course)

-   **Review skipped records**

    To prevent overriding your customizations, the upgrade process does not update records that you have modified. Instead, the upgrade process notes this skipped record in the upgrade logs.

    A video training course on resolving skipped records is available. To view this course, see [Upgrade Skipped Records](https://nowlearning.service-now.com/lxp?id=overview&sys_id=cbb197a6136b77002ff55eff3244b0b6&type=course).

-   **Review functionality after upgrade**

    Once you have upgraded your instance and run the migration script, regression testing can help ensure that your users can continue to work as expected after an upgrade. A regression test is a review of your applets, screen ui policies, and functions to make sure that they are working as intended.


## Running Mobile migration script

This script converts your custom applications and any modified base system application to the new mobile schema available in the New York release. The script only changes the current scope when it runs. If you have more than one scoped mobile application, you must run the script for each scope.

After an upgrade, the option to run the migration script appears when you first access a custom application, or a base system application that you have modified. For example, when opening a modified or custom applet record. You can also see the migration prompt when accessing the applet picker in Studio by browsing to **Mobile Studio** &gt; **Applets** and clicking the pop-out icon \(![Pop out icon](../image/IconPopOut.png)\). The migration prompt displays if any of the applets shown the picker require migration.

![Mobile migration script prompt](../image/migration-script-prompt.png)

After the script completes, you may be prompted to resolve collisions detected by the migration process. Collisions are records created by ServiceNow that you have modified, and are not automatically upgraded. Collisions can only occur when you have modified a base system application before your upgrade to New York or later releases.

![Mobile migration collision prompt](../image/migration-collision-prompt.png)

Click the **View Collisions** to resolve these collisions. For detail on this process, see [Resolve common issues in mobile migration script results](../reference/ny-migration.md).

## Changes made by the mobile migration script

Click **Migrate** to start the migration script for the current scope. The migration script migrates all records within the scope, not just the applet you have opened.

-   **Applications and folders transition to applet launchers**

    The legacy Madrid schema used mobile applications and folders to organize your applets. The Now Mobile schema, uses applet launcher screens, which are divided into UI sections. Applet launcher is accessed by tapping on tabs in the navigation bar which appears at the bottom of your app screens.

    ![Changes to applications in the New York schema.](../image/application-migration.png "Changes to applications in the New York schema")

    The migration script creates an applet launcher for each mobile application record. The script converts each folder in the original mobile application to a new horizontal icon section within that applet launcher. The script then creates an icon in the icon section for each applet with the folder. Hidden screens do not appear in the icon section. The script then adds a tab to the navigation bar for each of the new applet launchers.

    The example image shows how the incidents application appears after the migration process. The original folders \(**My Incidents** and **Group Incidents**\) display as UI sections in the **Incidents** applet launcher. These UI sections can scroll horizontally to show as many applets as needed. The **Incidents** application is accessible by tapping the **Incidents** tab in the navigation bar.

    After migration, the script removes the legacy Folder \[sys\_sg\_folder\] and Mobile Application \[sys\_sg\_application\] records.

    ![Madrid applications converted to New York icon sections and icons.](../image/ny-application-conversion.png)

    For more detail on the navigation bar, applet launchers and their UI sections, see [Navigation bar](sg-mobile-tab-bar.md), and [Launcher screens](sg-mobile-applet-launcher.md).

-   **Form migration**

    The Form applet replaces the root detail screens used to view record forms in the Madrid release. The migration creates a form screen \[sys\_sg\_form\_screen\] record. The script creates segments for each embedded screen in the original main detail screen. Any button \[sys\_sg\_button\] records associated to the original main detail screen change to associate with the new form applet.

-   **Map migration**

    Map applets did not use an item view to display fields in map cards in the Madrid release. The migration script creates an item view\[sys\_sg\_item\_view\] record for each map applet using the **Title**, **Tag**, **Sub-title**, and **Info** fields from the original map applet.

-   **Calendar migration**

    The migration script creates time span item stream \[sys\_sg\_time\_span\_item\_stream\] records for each calendar, and associates the calendars original data item to the new item stream. The migration script also creates a form applet \[sys\_sg\_form\_screen\] record, and migrates the buttons from the calendars original embedded screen to the new form.

-   **Item streams and Item configurations**

    ![Components of the Native Client.](../image/mobile-hierarchy-callout-2.png)

    The migration script creates an item stream \[sys\_sg\_item\_stream\] record for each screen in the scoped application. The original data item record associated with the legacy application changes to associate with the new item stream record. The script creates time span item stream \[sys\_sg\_time\_span\_item\_stream\] records for each calendar screen, and location item stream \[sys\_sg\_location\_item\_stream\] records for map screens. These two tables extend from the item stream table, but are used specifically for these screen types.

-   **Screen Cleanup**

    The following fields are no longer used in Screen records. The script removes these fields from call records on the Screen \[sys\_sg\_screen\] table.

    -   User Roles \[application\_roles\]
    -   Order \[order\]
    -   Parent \[parent\]
    -   Parent table \[parent\_table\]
    -   Data Item \[sys\_sg\_data\_item\]
    -   Hidden \[hidden\]
    In addition, the script also removes values from the following fields on Map screen \[sys\_sg\_map\_screen\] records:

    -   Data item table \[data\_item\_table\]
    -   Title \[title\]
    -   Sub-title \[subtitle\]
    -   Info \[info\]
    -   Location \[location\]
    -   Tag \[tag\]
    -   Tag font color \[tag\_font\_color\]
    -   Tag background color\[tag\_background\_color\]
    -   Tag Style \[tag\_style\]
    -   Phone \[phone\]
    -   Pin color type \[pin\_color\_type\]
    -   Pin color \[pin\_color\]
    The script removes values from the following fields on Item configuration \[sys\_sg\_master\_item\] records:

    -   Table \[table\]
    -   Screen \[screen\]
    -   Condition \[condition\]
    -   Condition Order \[condition\_order\]
    The script removes the value in the Item View \[item\_view\] field of Details screen \[sys\_sg\_details\_screen\] records.

    The script removes the value in the Item View \[item\_view\] field of List screen \[sys\_sg\_list\_screen\] records.

    The script removes the value in the Data Item \[data\_item\] field of Item View \[item\_view\] records.


## More Resources

For more information on the migration process, see the Mobile Migration Guide for New York on the ServiceNow community site. [https://community.servicenow.com/community?id=community\_article&amp;sys\_id=f5121a33dba7f788fff8a345ca961957](https://community.servicenow.com/community?id=community_article&sys_id=f5121a33dba7f788fff8a345ca961957)

-   **[Run the mobile migration script](../task/sg-mobile-migration-script.md)**  
Run the mobile migration script to convert Madrid mobile applications you have created or modified to use the new mobile hierarchy.
-   **[Resolve common issues in mobile migration script results](../reference/ny-migration.md)**  
Find solutions to common issues after running the mobile migration script.

**Parent Topic:**[Mobile plugins and upgrades](plugins-upgrades.md)


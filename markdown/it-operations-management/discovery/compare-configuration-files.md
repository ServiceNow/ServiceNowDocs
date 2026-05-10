---
title: Compare versions of CI configuration files
description: You can compare two versions of tracked CI configuration files to see the actual changes made to them.
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configuration file tracking, Advanced Discovery configuration, Configuring Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Compare versions of CI configuration files

You can compare two versions of tracked CI configuration files to see the actual changes made to them.

## Before you begin

If Discovery and Service Mapping don’t track a configuration file you want to track, perform advanced configuration as described in [Modify tracking changes in configuration files](../../discovery/task/track-configuration-files.md).

Role required: one of the following roles.

-   admin
-   service\_mapping\_admin \(starting from Visibility Content version 6.29.0\)

## About this task

Discovery and Service Mapping check configuration files for changes during horizontal discovery using patterns. If a configuration file is modified, the system saves the version of the file. You can use the timestamp to differentiate between versions. For Discovery, you can compare any two versions from the list of saved versions. For Service Mapping, you can compare the latest and previous versions.

Changes to configuration files are associated with CIs to which these files belong. Maps show configuration file changes as changes to related CIs.

## Procedure

1.  Compare two versions of the CI configuration file from Service Mapping or Discovery.

<table id="choicetable_c2k_pxd_bhc"><thead><tr><th align="left" id="d265955e145">

Product

</th><th align="left" id="d265955e148">

Steps

</th></tr></thead><tbody><tr><td id="d265955e154">

**Service Mapping**

</td><td>

1.  Navigate to **All** &gt; **Service Mapping** &gt; **Services** &gt; **Business Services**.
2.  Select **View Map** next to the required business service.
3.  On the **Changes** tab, locate the change record for the modified CI configuration file.

**Important:** The name of the change must be **File Modified**.

![Change record for a modified configuration file.](../image/ChangesTabFileModified.png)

4.  Select and hold \(or right-click\) the change record for the modified CI configuration file, and select **View Change in Tracked File Content**.

The Tracked Configuration File Comparison tab opens, displaying the most recent and the previous versions of the configuration file.

</td></tr><tr><td id="d265955e218">

**Discovery**

</td><td>

1.  Navigate to the configuration files list in **Tracked Configuration Files**.
    -   Navigate to **All** &gt; **Discovery** &gt; **Tracked Configuration Files** and sort or filter the list by criteria such as **Related CI** or **Host**.
    -   Open a CI record from the Configuration module for the CI type to which the configuration file belongs.

For example, to find a Tomcat server, navigate to **All** &gt; **Configuration** &gt; **Applications Servers** &gt; **Tomcat**, then select the specific Tomcat server. The list of configuration files appear in the Tracked Configuration files related list.

2.  Select the configuration file from the list.
3.  In the **Content Versions** related list, select one of the versions in the **Update time** related list.
4.  Select **Compare**.

The Tracked Configuration File Comparison tab opens, displaying the configuration file versions you selected.

</td></tr></tbody>
</table>2.  Review actual changes.

    Highlight colors indicate the type of change:

    -   Purple — Updated line
    -   Pink — New line
    -   Gray — Deleted line
3.  Navigate between the changes using the Next difference icon ![](../../discovery/image/next-difference-icon.png) and the Previous difference icon ![](../../discovery/image/previous-difference-icon.png).


**Related topics**  


[Tracked Configuration file form](../reference/tracked-configuration-file-form.md)


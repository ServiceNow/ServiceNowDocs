---
title: Create a custom clone profile
description: Clone profiles act as reusable clone templates to establish consistent clone outcomes. Use a clone profile to set up exclusions and preservers, and to choose clone settings, for specific clone scenarios.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/platform-administration/configure-clone-profile.html
release: australia
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 4
keywords: [Clone profile]
breadcrumb: [Configure, Instance Clone, Configure core features, Administer the ServiceNow AI Platform]
---

# Create a custom clone profile

Clone profiles act as reusable clone templates to establish consistent clone outcomes. Use a clone profile to set up exclusions and preservers, and to choose clone settings, for specific clone scenarios.

## About this task

Here are a few basics about clone profiles:

-   The System Profile is provided by default and can't be changed.
-   Custom profiles start with the default exclusions, preservers, and cleanup scripts from the System Profile. When you create a custom profile, all existing custom exclusions and preservers are added automatically.
-   You can prepare different profiles for individual use cases. For example, create a different profile for upgrades, dev testing, or IT app testing.
-   You can duplicate a profile from the Clone Admin Console when you open any clone profile.
-   When you request a clone, select the profile in the **Clone Profile** field. If you leave the field empty, the clone uses all available preservers, exclusions, and cleanup scripts.

## Before you begin

Role required: clone\_admin or clone\_profile\_admin

## Procedure

1.  Navigate to **All** &gt; **Clone Admin Console** &gt; **Home**.

2.  Navigate to **Configuration** &gt; **Clone profiles**

3.  Select **New**.

4.  In the Add new clone profile form, enter the profile details.

<table id="table_vbx_sq4_clc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**Clone Profile Name**

</td><td>

Name that describes the purpose of the profile. For example, *Upgrade testing*.

</td></tr><tr><td>

**Default**

</td><td>

Option to load this profile each time you open the clone request page. Cleared by default.

</td></tr><tr><td>

**Target Instance \(Optional\)**

</td><td>

Target instance associated with this clone profile permanently. If the clone profile is applied to a clone request, the clone request form updates to reflect the target instance from the profile.

</td></tr></tbody>
</table>5.  In the **General** tab, configure the clone settings.

<table id="table_ylv_1r4_clc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**Amount of data copied from the Task table**

</td><td>

Number of days of historical data copied from the Task table and its child tables, such as Incident, Problem, and Change.

 -   **Full**: Copies all data from the Task table and its child tables. This is the default.
-   **Last 90 days**: Copies only the last 90 days of data. This option can increase clone time, because records older than 90 days are deleted after the restore.
 To reduce clone time, consider excluding large tables instead. An excluded table keeps its schema and hierarchy on the target instance, so the table is empty but usable.

</td></tr><tr><td>

**Backup options**

</td><td>

Backup type the clone uses.

 -   **Most recent \(recommended default\)**: The clone uses the latest nightly backup, unless an upgrade or a major change to the instance occurred.
-   **On-demand backup**: A new backup begins at the clone start time. The clone begins only after the backup completes, which pushes back the time the clone process can start.


</td></tr></tbody>
</table>6.  In the **Exclusions** tab, choose what to leave out of clones that use this profile.

<table id="table_yql_cr4_clc"><thead><tr><th>

Setting

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**Exclude tables specified in Exclusion list**

</td><td>

Excludes all tables on the Exclusion list, including their child tables. The target instance keeps the same table schema and hierarchy as the source instance, so the excluded tables are empty but usable. This setting is on by default.

 Default exclusions, such as tables that contain auditing, license usage, logging, and notifications, are excluded by default and aren't affected by this setting. Turn this setting off if you need the data from your excluded tables \(a full clone\), for example for upgrade or deployment testing.

</td></tr><tr><td>

**Exclude audit and log data**

</td><td>

Helps prevent audit and log records from being cloned from the source instance. The target instance has empty but usable audit and log tables. This setting is on by default.

 If you exclude audit and log data, the activity stream for records doesn't match the source instance. The activity stream relies on the audit table to generate history.

</td></tr><tr><td>

**Exclude attachment data**

</td><td>

Helps prevent files such as videos, images, documents, and zip files from being cloned from the `sys_attachment` table. This setting is on by default.

 Default attachments and other system-relevant files, such as catalog item images, theme images, and icons, aren't affected by this setting.

</td></tr></tbody>
</table>7.  In the **Preservers** tab, choose what to preserve on the target instance during the clone.

<table id="table_z1x_dr4_clc"><thead><tr><th>

Setting

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**Preserve theme**

</td><td>

Option to preserve the theme and CSS elements on the target instance, so the target instance keeps its look and feel after a clone. Selected by default.

</td></tr><tr><td>

**No. of days of In-progress Global Update Sets to be preserved**

</td><td>

Number of days of in-progress update sets to preserve in the global application scope.

 -   **None**: Doesn't preserve update sets. This is the default.
-   **Last 90 days**: Preserves in-progress global update sets created within the last 90 days.
 This setting doesn't preserve in-progress scoped update sets, and update sets older than 90 days aren't saved. Review and commit your update sets before you clone.

</td></tr></tbody>
</table>8.  Select **Add**.


## Result

The profile appears in the **Clone Profiles** list. You can select it when you request a clone.

-   **Example: Create a profile for IT app testing**

    To test IT applications and workflows without copying unnecessary data, for example, HR request or other types of data to the target instance, you can create a profile named *IT app testing*. Add the tables that you don't want to clone to the Exclusion list, and keep Exclude tables specified in Exclusion list selected on the **Exclusions** tab. Clones that use this profile leave those tables empty on the target instance.

    To keep the theme and in-progress global update sets that already exist on the target instance, use the settings in the Preservers tab. Preserving large amounts of data increases clone time.


## What to do next

To use the profile, see [Request a clone](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-administration/t_StartAClone.md).


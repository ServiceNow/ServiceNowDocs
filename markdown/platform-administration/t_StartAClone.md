---
title: Request a clone
description: Request a clone to copy data from a production instance to a non-production instance or to copy data between non-production instances.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Instance Clone, Configure core features, Administer the ServiceNow AI Platform]
---

# Request a clone

Request a clone to copy data from a production instance to a non-production instance or to copy data between non-production instances.

## Before you begin

Role required: clone\_admin on the source instance; clone\_admin and soap on the target instance.

**Note:**

Configure your target instance before requesting your clone. See [Register target instance \(legacy\)](t_CreateACloneTarget.md).

Configure a clone profile. See [Create a custom clone profile](configure-clone-profile.md).

For self-hosted customer instances that use an Oracle database, see [https://support.servicenow.com/kb?id=kb\_article\_view&amp;sysparm\_article=KB0563847](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0563847).

## About this task

The ServiceNow AI Platform uses data from the most recent, daily backup of the source instance when cloning. Backups that are used for cloning are a maximum of 36 hours old. The initial preparation begins, including selecting the latest backup to use, only at the date and time processing is scheduled to start.

## Procedure

1.  Navigate to **All** &gt; **Clone Admin Console** &gt; **Request Clone**.

2.  On the form, fill in the fields.

<table id="table_ujp_cdf_gxb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Source instance

</td><td>

The original database where data is copied from.

</td></tr><tr><td>

Target instance

</td><td>

The new location where the data is copied to.**Note:** You can add an instance or select an existing instance without leaving the page.

</td></tr><tr><td>

Clone Profile

</td><td>

Apply a clone profile that you created previously. All exclusions, preservers, and scripts you added to the profile are applied to the clone request.

 If clone profile is left empty the system will pull in all available preservers, exclusions and cleanup scripts

 **Note:** If **default** is checked on the clone profile, the clone request loads this profile every time you open the clone request page.

</td></tr><tr><td>

Lock settings at the time of clone request

</td><td>

If you use a clone profile, this option locks the settings and options at the time of the clone request. Any subsequent changes to the clone profile, regardless of when the clone runs, don’t affect the clone request.

</td></tr><tr><td>

Clone Scheduled Start time

</td><td>

The start time to begin cloning your instance. See [Schedule recurring clones](schedule-cloning.md).**Note:** You may schedule multiple clones to the same target instance as long as they are scheduled at least five days apart. If two clone requests for the same target fall within a five day window, the system will return an error to prevent overlap. If a time you need is unavailable, check for any scheduled maintenance, upgrades, or existing clone requests affecting the relevant instances.

</td></tr><tr><td>

-   Email updates about this clone
-   External email address


</td><td>

The email or emails to be notified of the clone process and clone completion.

</td></tr></tbody>
</table>3.  Select the hyperlinked number under each item in the definitions section to review your exclusions, preservers, and cleanup scripts.![Clone definitions numbers.](../image/clone-definitions-numbers.png)

4.  Select the options to configure for your clone.

    **Note:** For information on all available options see [Clone options](../reference/clone-options.md). For information on general guidelines to expedite your clone request see [General guidelines for optimizing your clone duration](../reference/clone-duration-optimization.md).

5.  Select **Continue**.

6.  Review your clone request summary and select **Confirm and Submit Clone Request**.



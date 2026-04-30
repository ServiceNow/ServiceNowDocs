---
title: Request a clone in the Clone Admin Console
description: Request a clone to copy data from a production instance to a non-production instance or to copy data between non-production instances.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Clone Admin Console, System clone, Configure core features, Administer the ServiceNow AI Platform]
---

# Request a clone in the Clone Admin Console

Request a clone to copy data from a production instance to a non-production instance or to copy data between non-production instances.

## Before you begin

Role required: admin

Configure your target instance before requesting your clone. Do the following:

-   Navigate to the **Configurations** &gt; **Clone instances**.
-   Select **New**.
-   Fill in the new clone instance form.

**Note:** You can create multiple clone profiles and utilize a reusable clone template. Clone profiles enable you to select the correct exclusions and preservers for your clone.

Configure a clone profile. Do the following:

-   Navigate to **Configurations** &gt; **Clone profiles**.
-   Fill in the new clone profile form.

**Note:** Requests that are initiated via the classic page `clone_instance.do` won’t show up on the new clone console dashboard. However, they can still be found on the classic clone history page `clone_instance_list.do`.

## Procedure

1.  Navigate to **All** &gt; **Clone Admin Console** &gt; **Clone Dashboard**.

2.  Select **Request Clone**.

3.  On the form, fill in the fields.

<table id="table_ujp_cdf_gxb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Source instance

</td><td>

The instance you want to clone.

</td></tr><tr><td>

Target instance

</td><td>

The instance you want to clone the source instance to.**Note:** You can add an instance or select an existing instance without leaving the page.

</td></tr><tr><td>

Clone Profile

</td><td>

The clone profile to be used for your clone.

</td></tr><tr><td>

Clone Scheduled Start time

</td><td>

The start time to begin cloning your instance.

</td></tr><tr><td>

Email upon completion

</td><td>

The email to be notified of clone completion.

</td></tr></tbody>
</table>4.  Select the following options that you want to configure for your clone.

    **Note:** Additional settings can be configured for your clone request, however, these options may significantly increase your clone completion time.

    -   General options
        -   The amount of data copied from large tables

            **Note:** By excluding this data, this can extend the time of your clone as the data is copied over from the source, and all data older than 90 days is removed.

        -   Apply On-demand Backup
        -   Clone frequency
    -   Exclusions
        -   Exclude tables specified in the Exclusion list

            **Note:** When a table is excluded, this also excludes all of its child tables. For example, excluding the task table, also excludes its child tables such as Incidents, problems, and change tables.

        -   Exclude audit and log data

            **Note:** When **sys\_audit** is excluded it will break the activity stream for records. The activity stream is built from the **sys\_audit** table, so if it's empty all of the updates show as the username who created the record and display the created time.

        -   Exclude attachment data
    -   Preserves
        -   Preserve theme
        -   Number of days of in-progress Global Update Sets to be preserved
5.  Select **Continue**.

6.  Review your clone request summary and select **Confirm and Submit Clone Request**.



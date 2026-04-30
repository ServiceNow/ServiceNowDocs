---
title: Configure Core Business Suite applications
description: Configure Core Business Suite applications by running scheduled jobs that initialize all required workflows and apply settings.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-11-17"
reading_time_minutes: 5
breadcrumb: [Configure, Core Business Suite]
---

# Configure Core Business Suite applications

Configure Core Business Suite applications by running scheduled jobs that initialize all required workflows and apply settings.

## Before you begin

Role required: admin

## Procedure

1.  Assign the CBS requester role to all the active employees in the system by running the **CBS - Add Requestor Role to Users** scheduled job.

    **Note:** Run this scheduled job once during the initial Core Business Suite setup. You do not need to run it again after installing Core Business Suite applications.

    1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs**.

    2.  Search for and select **CBS - Add Requestor Role to Users**.

    3.  On the CBS - Add Requestor Role to Users page, select **Execute Now**.

2.  Activate Core Business Suite records by running the **Update service records for the Core Business Suite** scheduled job.

    Core Business Suite records include:

    -   EC Portal notifications
    -   Workspace notifications
    -   Email notifications
    -   Record producers
    -   System properties
    1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs**.

    2.  Search for and select **Update service records for the Core Business Suite**.

    3.  Prepare and execute the scheduled job from the Update service records for the Core Business Suite page.

        **Note:** Run this scheduled job only for newly installed services that aren’t yet running. Running it on active services overwrites existing records and recent changes.

<table id="table_pyw_ytd_nhc"><thead><tr><th>

Number of applications installed

</th><th>

Action

</th></tr></thead><tbody><tr><td>

All Core Business Suite applications

</td><td>

Select **Execute Now**.

</td></tr><tr><td>

One or more Core Business Suite applications

</td><td>

1.  Modify the business units \(BUs\) list in the BUList variable in the script to include only the BUs that are installed.

**Note:** You must provide the BU names in the BUList exactly as specified in the script. Valid BU names are: ‘LEGAL’, ‘HR’, ‘HEALTH’, ‘WSD’, ‘FCM’, ‘APO’, ‘SPO’, and ‘SLO’. Incorrect names will cause errors.

2.  Select **Execute Now**.


</td></tr></tbody>
</table>3.  Set up a taxonomy for Core Business Suite in the Employee Center portal by running the **Setup Core business suite Taxonomy for Employee Center** scheduled job.

    **Note:** Run this job once to set up the taxonomy in the Employee Center portal during the initial Core Business Suite setup.

    1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs**.

    2.  Search for and select **Setup Core business suite Taxonomy for Employee Center**.

    3.  Determine the taxonomy you want to use.

        -   Create a new taxonomy - `Core Business Suite Employee`
        -   Use the taxonomy already configured and in use in the Employee Center Portal and merging information from the `Core Business Suite Employee – Default` taxonomy provided with Core Business Suite application
        -   Use the `Core Business Suite Employee – Default` taxonomy provided with Core Business Suite application
<table id="table_ip2_cvd_nhc"><thead><tr><th>

Taxonomy to use

</th><th>

Action

</th></tr></thead><tbody><tr><td>

A new `Core Business Suite Employee` taxonomy for Core Business Suite created by merging topics from the taxonomy already configured in the Employee Center portal and the `Core Business Suite Employee – Default` taxonomy provided with Core Business Suite application.

</td><td>

On the Setup Core business suite Taxonomy for Employee Center page, select **Execute Now**.

</td></tr><tr><td>

The existing taxonomy that is already configured in the Employee Center portal by merging topics from the `Core Business Suite Employee – Default` taxonomy without creating a new taxonomy.

</td><td>

1.  On the Setup Core business suite Taxonomy for Employee Center page, update the variable `createNewTaxonomy` to `false` in the script.
2.  Select **Execute Now**.


</td></tr><tr><td>

The `Core Business Suite Employee – Default` taxonomy provided with the Core Business Suite application.

</td><td>

1.  Navigate to **All** &gt; **Service Portal** &gt; **Portals**.
2.  Search for and select **Employee Center**.
3.  In the **Employee Center** page, select the **Taxonomy** tab.
4.  If a message appears about the application scope, select **here** to be able to edit the record.
5.  Select **Edit**.
6.  If you have an existing taxonomy, select and remove it.
7.  Add **Core Business Suite Employee – Default** taxonomy to the **Taxonomy** list.
8.  Select **Save**.


</td></tr></tbody>
</table>4.  Add the created taxonomy `Core Business Suite Employee` to the Employee Center portal to enable organizing the Core Business Suite content.

    **Note:** Run this job only when you create a new taxonomy.

    1.  Navigate to **All** &gt; **Service Portal** &gt; **Portals**.

    2.  Search for and select **Employee Center**.

    3.  On the **Employee Center** page, select the **Taxonomy** tab.

    4.  If a message appears about the application scope, select **here** to be able to edit the record.

    5.  Select **Edit**.

    6.  If you have an existing taxonomy, select and remove it.

    7.  Add the newly created taxonomy **Core Business Suite Employee** to the **Taxonomy** list.

    8.  Select **Save**.

5.  Set up an Employee Center portal with a new Core Business Suite home page setup, Advanced Portal Navigation \(APN\), employee profiles, and quick links by running the **Setup Core Business Suite for Employee Center** scheduled job.

    For information about Core Business Suite home page setup, Advanced Portal Navigation \(APN\), employee profiles, and quick links, see [Exploring employee support](../concept/exploring-emp-home.md).

    **Warning:** You must run this **Setup Core Business Suite for Employee Center** scheduled job only after adding the newly created taxonomy `Core Business Suite Employee` to the Employee Center portal. Running this scheduled job prior to adding the taxonomy will result in an incorrect Advanced Portal Navigation \(APN\) setup.

    1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs**.

    2.  Search for and select **Setup Core Business Suite for Employee Center**.

    3.  In the **Setup Core Business Suite for Employee Center** page, select **Execute Now**.

6.  Add newly installed Core Business Suite applications to the taxonomy by running the **Add topic to taxonomy** scheduled job.

    **Note:** Run this scheduled job only for newly installed Core Business Suite applications that aren’t yet running. Running it on active applications overwrites existing records and recent changes.

    1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs**.

    2.  Search for and select **Add topic to taxonomy**.

    3.  Modify the business units \(BUs\) list in the BUList variable in the script to include only the BUs that are installed.

        **Note:** You must provide the BU names in the BUList exactly as specified in the script. Valid BU names are: ‘LEGAL’, ‘HR’, ‘HEALTH’, ‘WSD’, ‘FCM’, ‘APO’, ‘SPO’, and ‘SLO’. Incorrect names will cause errors.

    4.  Select **Execute Now**.

7.  Add and synchronize the topics and items from newly installed Core Business Suite application with the Employee Center portal by running the **Sync Advanced Navigation for Core Business Suite** scheduled job.

    **Note:** Run this job whenever you install a new Core Business Suite application.

    1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs**.

    2.  Search for and select **Sync Advanced Navigation for Core Business Suite**.

    3.  Select **Execute Now**.

8.  Check the status of the executed scheduled jobs.

    1.  Navigate to **All** &gt; **System Log** &gt; **All**.

    2.  On the **Log** page, search for messages with the prefix `Core Business Suite Setup`.



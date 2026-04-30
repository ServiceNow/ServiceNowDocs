---
title: Import Core Business Suite configuration files
description: Import the Core Business Suite configuration files into your instance to access and run the scheduled jobs required for configuring Core Business Suite applications.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-11-17"
reading_time_minutes: 1
breadcrumb: [Configure, Core Business Suite]
---

# Import Core Business Suite configuration files

Import the Core Business Suite configuration files into your instance to access and run the scheduled jobs required for configuring Core Business Suite applications.

## Before you begin

Role required: admin

## Procedure

1.  Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website, and search for and select the Core Business Suite application.

2.  In the Supporting Links and Docs section, download the following Core Business Suite configuration files:

    -   Core Business Suite Admin Setup \(Update set\)
    -   CBS - HR Core Records Deactivator \(Schedule job\)
    -   CBS - HR Integrations Records Deactivator \(Schedule job\)
    -   CBS - Bulk HR RCA Approval \(Schedule job\)
    **Note:** If you can't find the XML files, select **Show more** to view the list of supporting links and docs.

3.  Import the required update sets.

    1.  Navigate to **All** &gt; **System Update Sets** &gt; **Update Sets to Commit**.

    2.  Under Related Links, select **Import Update Set from XML**.

    3.  Select **Choose file**.

    4.  Browse for the `Core Business Suite Admin Setup` update set file and select it.

    5.  Select **Upload**.

        The `Core Business Suite Admin Setup` update set file uploads.

    6.  If the Retrieved Update Sets page does not open automatically, navigate to **All** &gt; **System Update Sets** &gt; **Retrieved Update Sets**.

    7.  Select the **Core Business Suite Admin Setup** update set file from the list.

    8.  Select **Preview Update Set**.

    9.  Select **Commit Update Set**.

        Once the commit is successful, the Core Business Suite Admin Setup status changes from Loaded to Committed.

        The `Core Business Suite Admin Setup` update set file is imported into your instance. This update set includes the following scheduled jobs:

        -   Setup Core Business Suite for Employee Center
        -   Add topic to taxonomy
        -   Setup Core business suite Taxonomy for Employee Center
        -   Sync Advanced Navigation for Core Business Suite
        -   Update service records for the Core Business Suite
4.  Import scheduled jobs.

    1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs**.

    2.  Right-click the **Name** column and select **Import XML**.

    3.  Select **Choose file**.

    4.  Browse for the **CBS - HR Core Records Deactivator** scheduled job file and select it.

    5.  Select **Upload**.

    6.  Repeat the steps to upload the remaining scheduled jobs:

        -   CBS - HR Integrations Records Deactivator
        -   CBS - Bulk HR RCA Approval

## What to do next

Run the scheduled jobs to configure the Core Business Suite applications. For more information, see [Configure Core Business Suite applications](cbs-run-scheduled-jobs.md).


---
title: Resolve duplicate configuration items in Security Posture Control
description: Use this process to remove duplicate configuration items in the SPC Cached Assets \[sn\_sec\_spc\_core\_asset\_cache\] table. This process removes duplicate records and preserves the master, or canonical, asset record that has the most related items.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Resolving duplicate configuration items, Use the workspace, Security Posture Control, Security Operations]
---

# Resolve duplicate configuration items in Security Posture Control

Use this process to remove duplicate configuration items in the SPC Cached Assets \[sn\_sec\_spc\_core\_asset\_cache\] table. This process removes duplicate records and preserves the master, or canonical, asset record that has the most related items.

## Before you begin

Roles required: sn\_cmdb\_user for access to the CMDB Workspace and sn\_sec\_spc\_core.admin to initiate the scheduled job

## Procedure

1.  Navigate to **All** &gt; **System Properties** &gt; **All Properties**.

2.  Locate the sn\_sec\_spc-core.is\_ci\_name\_unique system property.

    This is a configurable value on the property that specifies whether all configuration items listed in your CMDB or Asset Cache table have unique names.

    See [Resolving duplicate configuration items in Security Posture Control](spc-using-dedup-template.md) for more information about how to identify duplicate CIs.

3.  Select the record to open it and set the Value field to **true**.

4.  Update the record.

5.  Navigate to **CMDB Workspace** &gt; **Management** and select the De-duplication template library link under Management tools on the right.

    **Note:** The sn\_cmdb\_user role is required for access to the CMDB Workspace.

6.  In the De-duplication templates pane, expand **SPC deduplication templates** and select **Name flip-flop** to open it.

7.  Select **Publish**.

8.  Select **Publish** in the modal.

    You have published the deduplication template and activated the sn\_sec\_spc-core.is\_ci\_name\_unique system property. You must execute the Generate deduplication task scheduled job to generate the tasks that resolve the duplicated CIs.

9.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs** &gt; **Generate deduplication task** and select the record to open it.

10. Select **Execute Now**.

    Verify the background job is queued and processing.

11. Navigate to the **Background Jobs \[sn\_sec\_cmn\_background\_job\]** table to monitor the Generate deduplication task scheduled job.

    When the scheduled job is successfully completed \(Complete\), you can initiate the template you published.

12. Navigate to **CMDB Workspace** &gt; **Management** and select **View deduplication dashboard**.

13. Select **Running** to load the template.

14. Select the **Completed** tab to view the completed tasks.

    You must verify that the deduplication tasks have completed before you check the SPC Cached Assets \[sn\_sec\_spc\_core\_asset\_cache\] table for duplicates.

    You might have to refresh your screen to view the completed tasks.

15. When the scheduled job is successfully completed, and you have verified that the deduplication tasks are complete, navigate to the SPC Cached Assets \[sn\_sec\_spc\_core\_asset\_cache\] table and filter the Name column and check for duplicates.

    The master, or canonical, is the CI record that has the most related items. It is preserved on the table. If there no duplicates, check the CMDB 360 Data \[cmdb\_multisource\_data\] table for duplicates.

16. Navigate to the CMDB 360 Data \[cmdb\_multisource\_data\] table.

17. Group by Col0 and check if different CMDB references exist for assets that correspond to the Name column of the SPC Cached Assets \[sn\_sec\_spc\_core\_asset\_cache\] table.

    If you find any duplicates, run the Generate deduplication task scheduled job again.



---
title: Commit an update set
description: After resolving any issues from previewing, commit the update set to apply all changes and generate a local copy with records of each update.
locale: en-US
release: australia
product: System Update Sets
classification: system-update-sets
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Working with update sets, System update sets, Deploying applications, Building applications]
---

# Commit an update set

After resolving any issues from previewing, commit the update set to apply all changes and generate a local copy with records of each update.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Update Sets** &gt; **Retrieved Update Sets** and open the update set.

2.  **Note:** You can’t commit an update set until all problems are resolved.

    Resolve any problems with the update set.

3.  Select **Commit Update Set**.

    1.  Select **Cancel** to return to the preview and reevaluate the change.

    2.  Select **OK** to skip the change and continue committing the changes that are marked as **Commit**.

    If the update set contains one or more deletes, the system displays a warning. The warning lists up to five updates that may contain problems. If more than five updates have potential problems, the system provides a link.

4.  When the system successfully commits an update set, it displays a completion page.

5.  Select **Commit log** on the confirmation page.

    1.  Navigate to **System Update Sets** &gt; **Update log** and filter for the update set name.

    2.  Look for unsafe edit warnings.

        The system helps prevent changes that could cause data loss, like changing a field type with existing data. Make changes manually if needed, and use caution when updating production data. Look for errors that indicate which records failed to commit and why. Create an update set to address those failures, if necessary.

6.  Navigate to **System Update Sets** &gt; **Local Update Sets** and open the local update set record to review the changes.

7.  Change the state to **Ignore** when you’re no longer working on the update set, but don’t want it transferred to another instance.


**Parent Topic:**[Working with update sets](../concept/using-system-update-sets.md)


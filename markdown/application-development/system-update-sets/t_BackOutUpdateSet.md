---
title: Back out an update set
description: You can back out changes to existing records for any committed update set.
locale: en-US
release: australia
product: System Update Sets
classification: system-update-sets
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Working with update sets, System update sets, Deploying applications, Building applications]
---

# Back out an update set

You can back out changes to existing records for any committed update set.

## Before you begin

Role required: admin

## About this task

Backing out an update set adds delete updates to your current set. If you commit, back out, and reapply a remote update set, preview errors occur due to recent deletions causing collisions. The back-out process reverses both record-level updates and changes to the dictionary. Some changes caused by a back-out can result in data loss.

**Warning:** Don't back out the **Default** update set. This action can damage the configuration of the instance. Backing out an update set that belongs to an update set batch backs out the selected update set, plus any children of the backed-out update set.

## Procedure

1.  Navigate to **All** &gt; **System Update Sets** &gt; **Local Update Sets**.

2.  Open the update set record to back out.

    Make sure it’s complete and a date is set on the **Release date** field.

    **Note:** The application you select determines the available update set options. Ensure your chosen application matches the update set contents, for example Global.

3.  Review the update set and determine if backing it out can cause issues.

    If backing out an update set can cause problems, create and commit a new update set to undo the changes instead.

4.  Select **Back Out**.

    The page displays actions, progress, and problems. Problems are changes in more recent update sets that affect the update set that is being backed out.

5.  Resolve each problem before proceeding with the back out.

    The back-out preview process generates a warning for each problem.

6.  To keep the latest version, select **Decide to Keep Current**.

7.  To back out to the previous version, select **Decide to Use Previous**.

    The update set and all associated update records are deleted. If needed, you can still navigate to the retrieved update set, preview it, and commit it again.


**Parent Topic:**[Working with update sets](../concept/using-system-update-sets.md)


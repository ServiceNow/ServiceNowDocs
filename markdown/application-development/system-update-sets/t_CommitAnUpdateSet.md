---
title: Commit an update set
description: When you have previewed an update set and have resolved any issues, commit the update set. Committing an update set applies all changes to the instance and creates a local copy of the update set that contains an update record for every change.
locale: en-US
release: yokohama
product: System Update Sets
classification: system-update-sets
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Update set transfers, System update sets, Deploying applications, Building applications]
---

# Commit an update set

When you have previewed an update set and have resolved any issues, commit the update set. Committing an update set applies all changes to the instance and creates a local copy of the update set that contains an update record for every change.

## Procedure

1.  Navigate to **All** &gt; **System Update Sets** &gt; **Retrieved Update Sets** and open the update set.

2.  Resolve any problems.

    You cannot commit an update set until all problems are resolved.

3.  Click **Commit Update Set**.

    -   Click **Cancel** to return to the preview and reevaluate the change. None of the updates are committed.
    -   Click **OK** to skip the change and continue committing the changes that are marked as **Commit**.
    If the update set contains one or more DELETEs for schema, the system displays a warning. The warning lists up to five updates that may contain problems. If more than five updates have potential problems, the system provides a link.

    When the system successfully commits an update set, it displays a completion page.

4.  Click **Commit log** on the confirmation page, or navigate to **System Update Sets** &gt; **Update log** and filter for the update set name.

    -   Look for warnings that contain the text **unsafe edit**. The system automatically skips any changes that results in data loss, such as changing the type of a field that contains data. You must manually make any of these changes, if necessary. Use caution when making changes that affect production data.
    -   Look for errors that indicate which records failed to commit and why. Create a new update set to address those failures, if necessary.
5.  When you are no longer working on the update set but do not want it transferred to another instance, navigate to **System Update Sets** &gt; **Local Update Sets** and open the local update set record.

    Change the State to **Ignore**.


## What to do next

For completed update set on the production instance, you should always change the state to **Ignore**. This state ensures that the update set is not committed again when cloning the instance.


---
title: Setup your audit retention
description: Use the Retention option to automate and simplify the deletion of audit data as per your requirement.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-09-03"
reading_time_minutes: 1
breadcrumb: [Audit Management Console, Configure, Auditing]
---

# Setup your audit retention

Use the Retention option to automate and simplify the deletion of audit data as per your requirement.

## Before you begin

Role required: security\_admin

## Procedure

1.  Navigate to **All** &gt; **Audit Management Console**.

2.  Select the table from the list you want to update the retention policy.

    **Note:** By default, you land on the Columns tab at the end of this step.

3.  Select the Retention tab to update the retention policy for the selected table audit data.

    A modal showing the retention option shows up.

4.  Enable the Automatically Purge Audit Records toggle.

5.  Select the duration from the Duration dropdown menu.

    Select **Yes** if you want to proceed with the selected duration. You can also select **Cancel** if you want to select a different duration.

    **Note:** Logs older than your set duration will be purged and can't be restored.

    The Retention Policy modal shows up confirming the selected duration.

6.  Select **Save** to update the retention policy for the selected table.

7.  To disable deletion of Audit records of a table, disable the Automatically Purge Audit Records toggle and select **Save**.

    **Note:** The audit records that were previously deleted due to the selected retention duration are permanently unavailable.



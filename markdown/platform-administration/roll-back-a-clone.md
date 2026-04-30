---
title: Roll back a clone
description: Return a clone target to its state before the latest cloning. Roll back cloning if something went wrong in the cloning process.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [System clone, Configure core features, Administer the ServiceNow AI Platform]
---

# Roll back a clone

Return a clone target to its state before the latest cloning. Roll back cloning if something went wrong in the cloning process.

## Before you begin

Role required: admin

Rollbacks remove the latest cloning updates on a cloning target. You can only roll back the latest cloning updates. Rollbacks must occur no more than seven days after the cloning.

**Note:** Rollbacks must occur no more than two days after the cloning for users with sharded instances.

## Procedure

1.  Navigate to **All** &gt; **System Clone** &gt; **Live Clones** &gt; **Clone History**.

2.  Select the clone to roll back.

3.  Under **Related Links**, click **Rollback**.

    The **Rollback Clone** modal displays.

    ![Why roll back clone?](../image/rollback-clone-telemetry.png)

4.  In **Specify Reason**, select a reason for the rollback and click **OK**, or select **Others**, enter a reason in the text box and click **OK**.

    The system rolls back the clone and sets the **State** to **Rollback Requested**, and, if successful, to **Rolled Back**, or, if unsuccessful, to **Rollback Failure**.

    You can retry a rollback but if you get repeated failures, contact ServiceNow Customer Support.


## Result

The instance contains the same data it had before the clone was applied.


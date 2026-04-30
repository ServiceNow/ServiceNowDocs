---
title: Roll back a clone
description: Roll back a clone to remove the latest cloning updates on a cloning target if a mistake was made or an error has occurred.Return a clone target to its state before the latest cloning.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-12-12"
reading_time_minutes: 1
breadcrumb: [Manage, Instance Clone, Configure core features, Administer the ServiceNow AI Platform]
---

# Roll back a clone

Roll back a clone to remove the latest cloning updates on a cloning target if a mistake was made or an error has occurred.

## Before you begin

Role required: clone\_admin

You can only roll back the updates made with the last clone. Rollbacks must occur no more than seven days after the clone. If the instance is sharded, rollbacks must occur no more than two days after the clone.

## Procedure

1.  Navigate to **All** &gt; **Clone Admin Console** &gt; **Clone Home**.

2.  Select the tile of the clone that you must roll back.

3.  Select the **Rollback** option on the page.


## Roll back a clone \(legacy\)

Return a clone target to its state before the latest cloning.

### Before you begin

Role required: clone\_admin

You can only roll back the updates made with the last clone. Rollbacks must occur no more than seven days after the clone. If the instance is sharded, rollbacks must occur no more than two days after the clone.

### Procedure

1.  Navigate to **All** &gt; **System Clone** &gt; **Live Clones** &gt; **Clone History**.

2.  Select the clone to roll back.

3.  Under **Related Links**, click **Rollback**.

    The **Rollback Clone** modal displays.

    ![Why roll back clone?](../image/rollback-clone-legacy.png)

4.  Select a reason for the rollback and select **OK**.

    The system rolls back the clone and sets the **State** to **Rollback Requested**.

5.  If successful the state is set to **Rolled Back**.

6.  If unsuccessful the state is set to **Rollback Failure**.

    You can retry a rollback but if you get repeated failures, contact ServiceNow Customer Support.



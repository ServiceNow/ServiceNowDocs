---
title: View clone status \(legacy\)
description: View the status of a legacy clone.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Manage, Instance Clone, Configure core features, Administer the ServiceNow AI Platform]
---

# View clone status \(legacy\)

View the status of a legacy clone.

## Before you begin

Role required: clone\_admin

## Procedure

1.  Navigate to **All** &gt; **Instance Clone** &gt; **Live Clones** &gt; **Active Clones**.

    The system displays the list of currently active clones.

2.  Select a clone.

3.  Under **Related Links**, select **Check Clone Status**.

    The system updates the **State** field and produces a log entry in the **Clone Log** that shows the status of the clone.

    If an error occurs, you might [roll back clone](roll-back-a-clone.md#) and [schedule recurring clones](schedule-cloning.md). For more information see [Clone states](../reference/clone-states.md).



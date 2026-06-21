---
title: View clone status
description: You can view the status of a clone to make sure the cloning process isn't stuck.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/platform-administration/view-clone-status.html
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [System clone, Configure core features, Administer the ServiceNow AI Platform]
---

# View clone status

You can view the status of a clone to make sure the cloning process isn't stuck.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Clone** &gt; **Live Clones** &gt; **Active Clones**.

    The system displays the list of currently active clones.

2.  Select the clone you want the status of.

    The system displays the System Clone record of that clone.

3.  Under **Related Links**, click **Check Clone Status**.

    The system updates the **State** field and produces a log entry in the **Clone Log** that shows the status of the clone.

    \[Omitted image "clone-log.png"\] Alt text: Clone log

    If a cloning status is failed, you might [roll back the cloning](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/platform-administration/roll-back-a-clone.md) and [schedule a new cloning](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/platform-administration/schedule-cloning.md).



---
title: View clone history
description: You can view the status and history of any system clone request.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [System clone, Configure core features, Administer the ServiceNow AI Platform]
---

# View clone history

You can view the status and history of any system clone request.

## Before you begin

Role required: clone\_admin or admin

## About this task

The System Clone \[clone\_instance\] table stores records for all previously and currently scheduled clones.

## Procedure

1.  Navigate to **All** &gt; **System Clone** &gt; **Live Clones** &gt; **Clone History**.

    Clone history also displays the **State** for current and past clones. Clones in the **Draft** state do not appear on the Clone History table.

    ![Clone completed](../image/CloneCompleted.png)

    |Clone state|Description|
    |-----------|-----------|
    |Requested|The clone was requested and is awaiting approval.|
    |Scheduled|The clone is ready to begin at the scheduled time and date.|
    |Active|The clone is currently running.|
    |Completed|The clone completed successfully.|
    |Canceled|A user canceled the request.|
    |Hold|The server rejected the clone request. This can happen either because the clone was not ready to proceed by the scheduled time or because additional clone requests were submitted before the first one completed.|
    |Error|The clone encountered an error while running. Contact technical support for help resolving this issue.|
    |Draft|The clone is scheduled to be created. This state never appears in the Clone History table.|

2.  Select a System Clone record to view its history.



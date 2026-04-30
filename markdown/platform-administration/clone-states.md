---
title: Clone states
description: A reference topic displaying the various states of a clone.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-09-09"
reading_time_minutes: 1
breadcrumb: [Reference, Instance Clone, Configure core features, Administer]
---

# Clone states

A reference topic displaying the various states of a clone.

|Clone state|Description|
|-----------|-----------|
|Requested|The clone was requested and is awaiting approval.|
|Scheduled|The clone is ready to begin at the scheduled time and date.|
|Active|The clone is running.|
|Completed|The clone completed successfully.|
|Canceled|The request is canceled.|
|Hold|The server rejected the clone request. The clone wasn’t ready to proceed by the scheduled time or because additional clone requests were submitted before the first one completed.|
|Error|The clone encountered an error while running. Contact technical support for help resolving this issue.|
|Draft|The clone is scheduled to be created. This state never appears in the Clone History table.|
|Rollback requested|The clone is requested to roll back to a previous state.|
|Rollback failure|The request to roll back the clone has failed.|
|Rolling back|The clone is in the process of rolling back to a previous state.|
|Rolled back|The clone request to roll back to a previous state is complete.|

**Parent Topic:**[Instance Clone reference](instance-clone-reference.md)


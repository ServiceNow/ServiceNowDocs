---
title: Clone states
description: A reference topic displaying the various states of a clone.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/clone-states.html
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Reference, Instance Clone, Configure core features, Administer the ServiceNow AI Platform]
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

## Cleanup script execution states

After a clone completes, each cleanup script on the target instance displays one of the following states. The normal progression is: Ready to schedule → Scheduled → Executing → Completed, Error, or Not executed.

|State|Description|
|-----|-----------|
|Ready to schedule|The script is queued and will run when its turn comes. Shown before and during clone execution for scripts that have not yet started.|
|Scheduled|The script has been scheduled to run.|
|Executing|The script is actively running.|
|Completed|The script finished successfully.|
|Error|The script encountered an error. The error message is shown in the **Error message** column. See [Monitor cleanup script execution](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/monitor-cleanup-script-execution.md) to retry failed scripts.|
|Not executed|The script was intentionally skipped due to conditional logic. The reason is shown in the **Error message** column.|

**Note:** If a script is retried after an error, the state returns to **Executing** and the **Runs** column increments by 1.

**Parent Topic:**[Instance Clone reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/instance-clone-reference.md)


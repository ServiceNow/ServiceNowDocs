---
title: Monitor cleanup script execution
description: Monitor the execution status of cleanup scripts after a clone and retry any scripts that encountered errors.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/monitor-cleanup-script-execution.html
release: australia
topic_type: task
last_updated: "2026-07-20"
reading_time_minutes: 1
keywords: [cleanup script, clone, execution, monitoring]
breadcrumb: [Configure, Instance Clone, Configure core features, Administer the ServiceNow AI Platform]
---

# Monitor cleanup script execution

Monitor the execution status of cleanup scripts after a clone and retry any scripts that encountered errors.

## Before you begin

A clone must have completed before cleanup script execution data is available.

Role required: clone\_admin

## About this task

You can monitor cleanup script execution directly from the source instance using Multi-Instance View. This approach allows you to view cleanup script status without logging in to the target instance. Both the source and target instances must be on Australia Patch 5 or later to use Multi-Instance View.

You can also view the execution status on the target instance.

## Procedure

1.  Enable Multi-Instance View on the source instance to view cleanup script execution across linked instances.

    For information about enabling Multi-Instance View, see [Configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/clone-configurations-tab.md).

    Alternatively, log in to the target instance and navigate to **Cleanup Script Execution**.

2.  Navigate to **Cleanup Script Execution**.

    The page displays a list of all cleanup scripts and their current execution state.

3.  Review the **State** column for each script.

    For a description of each state, see [Clone states](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/clone-states.md).

4.  If one or more scripts show a state of **Error**, select **Resume all remaining scripts** to re-run all failed scripts and continue with any remaining scripts.

    A confirmation modal displays: "This will re-run all failed scripts and continue with remaining scripts. Once started, scripts cannot be canceled from the user interface."

    If **Resume all remaining scripts** is not available, verify that at least one script has a state of **Error**.

5.  Select **Resume all remaining scripts** in the confirmation modal to confirm.

    Failed scripts return to **Executing** state. The **Runs** column increments by 1 for each retried script.


## Result

Cleanup scripts resume execution. Monitor the **State** column to confirm scripts reach **Completed** state.

## What to do next

To persist fixes for future clones, update the cleanup script on the source instance where it is defined. See [Create cleanup scripts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/create-cleanup-script.md).


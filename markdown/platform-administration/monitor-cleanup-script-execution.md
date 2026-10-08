---
title: Monitor cleanup script execution
description: Monitor the execution status of cleanup scripts after a clone and retry any scripts that encountered errors.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/platform-administration/monitor-cleanup-script-execution.html
release: australia
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
keywords: [cleanup script, clone, execution, monitoring]
breadcrumb: [Configure, Instance Clone, Configure core features, Administer the ServiceNow AI Platform]
---

# Monitor cleanup script execution

Monitor the execution status of cleanup scripts after a clone and retry any scripts that encountered errors.

## Before you begin

A clone must have completed before cleanup script execution data is available.

Both the source and target instances must be on Australia Patch 5 or later to use OAuth target authentication and view cleanup script status.

Role required: clone\_admin

## About this task

You can monitor cleanup script execution directly from the source instance using Multi-Instance View. This approach enables you to view cleanup script status without logging in to the target instance.

You can also view the execution status on the target instance.

## Procedure

1.  Enable Multi-Instance View on the source instance to view cleanup script execution across linked instances.

    For information about enabling Multi-Instance View, see [Configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-administration/clone-configurations-tab.md).

    Alternatively, log in to the target instance and navigate to **Cleanup Script Execution**.

2.  Navigate to the Clone Status page for the completed clone request.

    In the Clone Admin Console, select the clone request from the Clone Activity tab to open its Clone Status page.

3.  Select **Show cleanup scripts** to expand the Post-clone Cleanup Scripts section.

    The Post-clone Cleanup Scripts section displays the status of cleanup scripts running on the target instance after the clone.

4.  Select **View on target instance** to open the Cleanup Script Execution page on the target instance.

    The page displays a list of all cleanup scripts and their current execution state.

5.  Review the **State** column for each script.

    For a description of each state, see [Clone states](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-administration/clone-states.md).

6.  If one or more scripts show a state of **Error**, select **Resume all remaining scripts** to re-run all failed scripts and continue with any remaining scripts.

    A confirmation modal displays: "This will re-run all failed scripts and continue with remaining scripts. After scripts start, they can't be canceled from the user interface."

    If **Resume all remaining scripts** is not available, verify that at least one script has a state of **Error**.

7.  Select **Resume all remaining scripts** in the confirmation modal to confirm.

    Failed scripts return to **Executing** state. The **Runs** column increments by 1 for each retried script.


## Result

Cleanup scripts resume execution. Monitor the **State** column to confirm scripts reach **Completed** state.

## What to do next

To persist fixes for future clones, update the cleanup script on the source instance where it is defined. See [Create cleanup scripts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-administration/create-cleanup-script.md).


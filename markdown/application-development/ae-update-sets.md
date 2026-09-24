---
title: Update sets and Autonomous Engineer
description: When you work with Autonomous Engineer, your changes are automatically tracked in update sets so you can review, revert, and deploy them without leaving ServiceNow Studio.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ae-update-sets.html
release: brazil
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Use, Autonomous Engineer, Agentic development on the ServiceNow AI Platform, Building applications]
---

# Update sets and Autonomous Engineer

When you work with Autonomous Engineer, your changes are automatically tracked in update sets so you can review, revert, and deploy them without leaving ServiceNow Studio.

Autonomous Engineer tracks every change it makes to your application in update sets. Changes from each checkpoint in a conversation are captured together in a single update set. You can access, review, and open the update sets directly from the Autonomous Engineer chat panel. You can also open the update sets from the Current Changes List \(CCL\) page in ServiceNow Studio, without navigating to the platform.

Update sets use descriptive names to help identify what each update set contains. Names follow this pattern: *application-name* `build agent install 1`, `build agent install 2`, and so on.

After Autonomous Engineer creates a checkpoint, it automatically opens a manual edit checkpoint that captures any changes you make directly to your application outside of Autonomous Engineer. These manual edits are tracked in a separate update set named `manual edit 1`, `manual edit 2`, and so on.

-   When a plan completes, a batch update set is available and includes all the update sets for the work items for the plan.
-   When a work item completes, an update set is available and includes all the changes for the work item.

For general information about update sets on the ServiceNow AI Platform, see [System update sets]().

## How Autonomous Engineer tracks changes

Autonomous Engineer automatically captures changes in a unified update set as you work. The consolidated update set merges all the update sets created for previous agentic and manual development into a single update set for ease of deployment. The consolidation occurs after you tell Autonomous Engineer that you're done working on a task and no longer require rollback.

Autonomous Engineer automatically captures changes to the app and metadata that you're working on.

A checkpoint is created automatically after you approve each task plan. When Autonomous Engineer reaches a checkpoint, the changes associated with that checkpoint are captured in the update set. You can view and open the relevant update set directly from each checkpoint in the chat panel. For more information on checkpoints, see [View changes in the change log](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ae-ccl-preview-tab.md).

When Autonomous Engineer prepares to create the next checkpoint, it checks whether any changes exist in the manual edit update set. If no changes are present, Autonomous Engineer removes the update set. If changes exist, Autonomous Engineer completes the update set and renders it with the other update sets from your conversation. You can access manual edit update sets directly from the checkpoints panel in your Autonomous Engineer conversation.

## Deploy update sets

After your changes are ready, you can find the update sets from your Autonomous Engineer session on the **Deployment** tab on the ServiceNow Studio home page.

**Parent Topic:**[Using Autonomous Engineer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ae-using-autonomous-engineer.md)


---
title: Update sets and Build Agent
description: When you work with Build Agent, your changes are automatically tracked in update sets so you can review, revert, and deploy them without leaving ServiceNow Studio.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ba-update-sets.html
release: australia
topic_type: concept
last_updated: "2026-07-01"
reading_time_minutes: 4
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Use, Build Agent, Agentic development on the ServiceNow AI Platform, Building applications]
---

# Update sets and Build Agent

When you work with Build Agent, your changes are automatically tracked in update sets so you can review, revert, and deploy them without leaving ServiceNow Studio.

Build Agent tracks every change it makes to your application in update sets. Changes from each checkpoint in a conversation are captured together in a single update set. You can access, review, and open the update sets directly from the Build Agent chat panel. You can also open the update sets from the Current Changes List \(CCL\) page in ServiceNow Studio, without navigating to the platform.

**Note:** Your instance must be on Australia Patch 3 or later to work with update sets in Build Agent.

Update sets use descriptive names to help identify what each update set contains. Names follow this pattern: *application-name* `build agent install 1`, `build agent install 2`, and so on.

After Build Agent creates a checkpoint, it automatically opens a manual edit checkpoint that captures any changes you make directly to your application outside of Build Agent. These manual edits are tracked in a separate update set named `manual edit 1`, `manual edit 2`, and so on.

For general information about update sets on the ServiceNow AI Platform, see [System update sets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/system-update-sets/system-update-sets.md).

## How Build Agent tracks changes

Starting with Australia Patch 4, Build Agent automatically captures changes in a unified update set as you work. Manual edits you make in the ServiceNow Studio editor and automatic edits made by Build Agent within the same work session are bundled into a single update set. The consolidated update set merges all the update sets created for previous agentic and manual development into a single update set for ease of deployment. The consolidation occurs after you tell Build Agent that you're done working on a task and no longer require rollback.

Build Agent automatically captures changes to the app and metadata that you're working on.

A checkpoint is created automatically after you approve each task plan. When Build Agent reaches a checkpoint, the changes associated with that checkpoint are captured in the update set. You can view and open the relevant update set directly from each checkpoint in the chat panel. For more information on checkpoints, see [Build Agent checkpoints and conversation change log](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/ba-conversational-change-log.md).

When Build Agent prepares to create the next checkpoint, it checks whether any changes exist in the manual edit update set. If no changes are present, Build Agent removes the update set. If changes exist, Build Agent completes the update set and renders it with the other update sets from your conversation. You can access manual edit update sets directly from the checkpoints panel in your Build Agent conversation.

## Access update sets from Build Agent

You can access update sets created during a Build Agent session from two locations in ServiceNow Studio.

-   **Chat panel**

    Each checkpoint in the chat panel includes a **Review** button that opens the relevant update set in a new ServiceNow Studio tab. The update set button in the summary card opens all update sets associated with the changes shown in that card.

    \[Omitted image "ba-checkpoints.png"\] Alt text: Checkpoints panel with Checkpoint 5 expanded, listing six updated test step files and Restore and Review buttons.

-   **Current Changes List page**

    The Current Changes List \(CCL\) page in ServiceNow Studio shows Build Agent edits. Each checkpoint on the CCL page includes a button that opens the relevant update set in a new tab.


## Revert changes using checkpoints

You can revert your application to any previous checkpoint during a Build Agent session. For more information about checkpoints and how to restore a previous state, see [Build Agent checkpoints and conversation change log](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/ba-conversational-change-log.md).

## Deploy update sets

After your changes are ready, you can find the update sets from your Build Agent session on the **Deployment** tab on the ServiceNow Studio home page. For more information about deploying your changes, see [Deploying what you built with Build Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/build-agent-deployment.md).

**Parent Topic:**[Use Build Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/use-build-agent.md)


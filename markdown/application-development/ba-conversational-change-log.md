---
title: Build Agent checkpoints and conversation change log
description: The conversation change log tracks every change Build Agent makes to your application. It appears automatically in an integrated tab in ServiceNow Studio and lets you view updates, roll back to a previous checkpoint, and deploy changes to an update set.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ba-conversational-change-log.html
release: australia
topic_type: concept
last_updated: "2026-07-01"
reading_time_minutes: 3
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Use, Build Agent, Agentic development on the ServiceNow AI Platform, Building applications]
---

# Build Agent checkpoints and conversation change log

The conversation change log tracks every change Build Agent makes to your application. It appears automatically in an integrated tab in ServiceNow Studio and lets you view updates, roll back to a previous checkpoint, and deploy changes to an update set.

## Conversation change log

Use the conversation change log to do the following actions:

-   View the changes you have made since a checkpoint
-   Roll back changes to the previous checkpoint
-   Approve and deploy changes to an update set

When viewing the conversation change log, you can also view update sets created by Build Agent from within the chat panel. Each checkpoint includes a button that opens the relevant update set in a new tab. For information on how the change log and checkpoints work with update sets, see [Update sets and Build Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/ba-update-sets.md).

\[Omitted image "ba-change-log.png"\] Alt text: Checkpoint selection with Checkpoint 1 selected and a generated change log summary for an app. \[Omitted image ""\] Alt text:

The change log displays the following:

-   The **Files** list displays all the files that Build Agent updated during your conversation. The categories mirror the ones in the ServiceNow Studio Navigator panel.
-   The menu at the top shows the current checkpoint. You can use the list at the end of the checkpoint name to select a different checkpoint to view. When there are multiple checkpoints, a **Summary** option appears, which shows changes from each checkpoint all together.
-   The overview section shows the plan and actions Build Agent took based on the conversation.
-   The action in the corner menu to pen the chat, **Restore** your app to a previous checkpoint, or open the app details page.

Changes from each checkpoint in the conversation are packaged together into an update set. You can find each update set on the **Deployment** tab on the ServiceNow Studio home page. For more information on deployment, see [Deploying what you built with Build Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/build-agent-deployment.md).

## Checkpoints

Checkpoints are groups of changes that you made to an application that you can revert to at any time during your conversation with Build Agent. Checkpoints are created automatically after you approve each task plan.

**Note:** With Australia Patch 3 and earlier, checkpoint 0 creates an update set in global scope, and subsequent checkpoints created update sets in your application scope. However, update sets that exist across different scopes and can't be merged.

With Australia Patch 4 and later:

-   Checkpoint 0 doesn't create an update set. Instead, it serves as a placeholder in the UI that you can use to restore your application to its initial state.
-   Checkpoint 1 is the base update set for your application. The checkpoint 1 update set is the parent, or chain root, for all subsequent update sets created during the conversation. Because all update sets exist in the same application scope, you can merge them together when you're ready to move your changes to another environment. For information on update sets, see [Update sets and Build Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/ba-update-sets.md).

When Build Agent prepares to create the next checkpoint, it checks whether any changes exist in the manual edit update set. If no changes are present, Build Agent removes the update set. If changes exist, Build Agent completes the update set and renders it with the other update sets from your conversation. You can access manual edit update sets directly from the checkpoints panel in your Build Agent conversation.

**Parent Topic:**[Use Build Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/use-build-agent.md)


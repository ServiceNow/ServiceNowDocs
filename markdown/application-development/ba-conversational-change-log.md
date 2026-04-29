---
title: Build Agent conversation change log
description: After Build Agent completes the changes you request, you can find information about the updates in the change log that automatically appears in an integrated tab in ServiceNow Studio.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-04-02"
reading_time_minutes: 1
breadcrumb: [Use, Build Agent, Vibe coding and AI app development on the ServiceNow AI Platform, Building applications]
---

# Build Agent conversation change log

After Build Agent completes the changes you request, you can find information about the updates in the change log that automatically appears in an integrated tab in ServiceNow Studio.

Use the conversation change log to do the following actions:

-   View the changes you've made since a checkpoint
-   Roll back changes to the previous checkpoint
-   Approve and deploy changes to an update set

Checkpoints are groups of changes that you've made to an application that you can revert back to at any point during your conversation with Build Agent. Checkpoints are created automatically after you approve each task plan.

![The conversational change log shows changes Build Agent has made to an application](../../servicenow-studio/image/sn-studio-ba-convo-change-log.png)

The change log displays the following:

1.  The **Files** list displays all the files that Build Agent updated during the course of your conversation.

    These categories mirror the ones in the ServiceNow Studio Navigator panel.

2.  The **Overview** section shows the actions Build Agent took based on the conversation.

    When there are multiple changes and checkpoints for the app, you can see a file diff viewer with precise changes.

3.  The menu at the top shows the checkpoint you're in. You can use the drop-down list at the end of the checkpoint name to select a different checkpoint to view.

    When there are multiple checkpoints, a **Summary** option appears, which shows changes from each checkpoint all together.

4.  In the corner, you can take actions by reopening the chat, restoring your app to a previous checkpoint, or opening the app details page for the app you're working in.

Changes from each checkpoint in the conversation are packaged together into an update set. You can find each update set on the **Deployment** tab on the ServiceNow Studio home page.

**Parent Topic:**[Use Build Agent](../tasks/use-build-agent.md)


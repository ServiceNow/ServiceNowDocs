---
title: Build Agent in ServiceNow Studio
description: Use Build Agent, an autonomous AI agent, to create and update applications in ServiceNow Studio. Build Agent enables developers to perform intelligent, context-aware tasks within ServiceNow Studio through conversational interaction.
locale: en-US
release: australia
product: ServiceNow Studio
classification: servicenow-studio
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Use, ServiceNow Studio, Developing your application, Building applications]
---

# Build Agent in ServiceNow Studio

Use Build Agent, an autonomous AI agent, to create and update applications in ServiceNow Studio. Build Agent enables developers to perform intelligent, context-aware tasks within ServiceNow Studio through conversational interaction.

For full documentation on Build Agent, see [Build Agent](../../build-agent/concept/build-agent.md).

## Basic Build Agent workflow

The process of using Build Agent in ServiceNow Studio follows a general path.

1.  The Build Agent chat interface opens automatically during a new ServiceNow Studio session. If it's not open already, select **Open Build Agent** from the lower right corner status bar.
2.  Begin a conversation by prompting Build Agent to create or update an application.
3.  Refine your application through conversational interaction, providing feedback and requesting changes as needed.
4.  Roll back changes at any point using checkpoints created by Build Agent.
5.  Deploy the app through update sets, pipelines, or the Application Repository.
6.  Reopen the conversation at any time to make further updates.

For more information, see [AI-assisted ServiceNow AI Platform development with Build Agent](../../vibe-coding/concept/vc-build-agent-landing.md).

## Key Build Agent capabilities

In ServiceNow Studio, you can use Build Agent to complete the following tasks.

-   Create an app or app file.
-   Update an app or app file.
-   Summarize the contents of an app.
-   Track conversation updates with the conversation change log.
-   Roll back conversations and changes to a checkpoint.
-   Roll back an entire conversation.

Deploying apps created using Build Agent follows the same process as any other app, depending on your company processes. You can deploy using update sets, pipelines, or the Application Repository.

For more information, see [Working with update sets in ServiceNow Studio](working-with-update-sets-in-servicenow-studio.md), [Working with pipelines in ServiceNow Studio](working-with-pipelines-servicenow-studio.md), and [Working with the Application Repository in ServiceNow Studio](working-with-the-app-repo-in-servicenow-studio.md).

## Build Agent chat panel

Use the Build Agent chat panel to create or update an app or app file. Make a selection to begin the chat, or enter a prompt.

![Begin a conversation by selecting an option to create or update an app or app file.](../image/sn-studio-ba-new-chat.png "New chat panel")

Continue your conversation in the chat panel until you're happy with the results.

For more information, see the following topics:

-   [Create an application using Build Agent](../../build-agent/tasks/create-a-new-application-using-build-agent.md)
-   [Edit an existing application using Build Agent](../../build-agent/tasks/edit-an-existing-application-using-build-agent.md)
-   [Creating or updating an app file with Build Agent](../../build-agent/concept/creating-or-updating-an-app-file.md)
-   [Revert app changes with Build Agent](../../build-agent/tasks/revert-app-changes-using-build-agent.md)
-   [Build Agent conversation change log](../../build-agent/concept/ba-conversational-change-log.md)
-   [Example prompts](../../build-agent/reference/build-agent-example-prompts.md)

<table id="table_x2g_4c2_m3c"><thead><tr><th>

Function

</th><th>

Description

</th></tr></thead><tbody><tr><td>

New chat icon ![](../image/sn-studio-ba-new-chat-icon.png)

</td><td>

Open a new chat in the Build Agent chat panel.Begin a new chat when you want to start working on a new application or need a fresh start for updates.

</td></tr><tr><td>

Chats icon ![](../image/sn-studio-ba-chats-icon.png)

</td><td>

See a list of all your chats with Build Agent.

</td></tr><tr><td>

Checkpoints icon ![](../image/sn-studio-ba-checkpoint-icon.png)

</td><td>

See a list of all the checkpoints within your current chat with Build Agent.Checkpoints show all the progress points in your application. You can revert to any of these checkpoints during the course of developing your app.

</td></tr></tbody>
</table>**Parent Topic:**[Using ServiceNow Studio](using-servicenow-studio.md)


---
title: Build Agent in ServiceNow Studio
description: Use Build Agent, an autonomous AI agent, to create and update applications in ServiceNow Studio through conversational interaction.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/servicenow-studio-classic/build-agent-in-servicenow-studio.html
release: australia
product: ServiceNow Studio Classic
classification: servicenow-studio-classic
topic_type: concept
last_updated: "2026-05-11"
reading_time_minutes: 4
breadcrumb: [Use, ServiceNow Studio, Developing your application, Building applications]
---

# Build Agent in ServiceNow Studio

Use Build Agent, an autonomous AI agent, to create and update applications in ServiceNow Studio through conversational interaction.

For full documentation on Build Agent, see [Build Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/building-applications/build-agent.md). To learn how to develop an application using Build Agent, see [ServiceNow Studio and Build Agent tutorial](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/sns-ba-tutorial-landing.md).

## How does the Build Agent workflow work?

Use Build Agent in ServiceNow Studio by following these steps.

1.  The Build Agent chat interface opens automatically during a new ServiceNow Studio session. If it is not open, select the Now Assist icon \[Omitted image "sn-studio-now-assist-icon.png"\] Alt text:or select **Open Build Agent** from the lower right corner status bar.
2.  Prompt Build Agent to create or update an application.
3.  Refine the application through conversational interaction, providing feedback and requesting changes.
4.  Roll back changes at any point using checkpoints created by Build Agent.
5.  Deploy the app through update sets, pipelines, or the Application Repository.
6.  Reopen the conversation at any time to make further updates.

For more information, see [AI-assisted ServiceNow AI Platform development with Build Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/building-applications/vc-build-agent-landing.md).

## What can Build Agent do in ServiceNow Studio?

Use Build Agent in ServiceNow Studio to complete the following tasks.

-   Create an app or app file.
-   Update an app or app file.
-   Summarize the contents of an app.
-   Track conversation updates with the conversation change log.
-   Roll back conversations and changes to a checkpoint.
-   Roll back an entire conversation.

Deploy apps created using Build Agent using update sets, pipelines, or the Application Repository — the same process as any other app.

For more information, see [Update sets in ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/working-with-update-sets-in-servicenow-studio.md), [Pipelines in ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/working-with-pipelines-servicenow-studio.md), and [Application Repository in ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/working-with-the-app-repo-in-servicenow-studio.md).

## Build Agent chat panel

Use the Build Agent chat panel to create or update an app or app file. Make a selection to begin the chat, or enter a prompt.

\[Omitted image "sn-studio-ba-new-chat.png"\] Alt text: Begin a conversation by selecting an option to create or update an app or app file.

Continue your conversation in the chat panel until you're happy with the results.

For more information, see the following topics:

-   [Create an application using Build Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/building-applications/create-a-new-application-using-build-agent.md)
-   [Edit an existing application using Build Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/building-applications/edit-an-existing-application-using-build-agent.md)
-   [Creating or updating an app file with Build Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/building-applications/creating-or-updating-an-app-file.md)
-   [Revert app changes with Build Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/building-applications/revert-app-changes-using-build-agent.md)
-   [Build Agent conversation change log](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/building-applications/ba-conversational-change-log.md)
-   [Example prompts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/building-applications/build-agent-example-prompts.md)

<table id="table_x2g_4c2_m3c"><thead><tr><th>

Function

</th><th>

Description

</th></tr></thead><tbody><tr><td>

New chat icon \[Omitted image "sn-studio-ba-new-chat-icon.png"\] Alt text:

</td><td>

Open a new chat in the Build Agent chat panel.Begin a new chat when you want to start working on a new application or need a fresh start for updates.

</td></tr><tr><td>

Chats icon \[Omitted image "sn-studio-ba-chats-icon.png"\] Alt text:

</td><td>

See a list of all your chats with Build Agent.

</td></tr><tr><td>

Checkpoints icon \[Omitted image "sn-studio-ba-checkpoint-icon.png"\] Alt text:

</td><td>

See a list of all the checkpoints within your current chat with Build Agent.Checkpoints show all the progress points in your application. You can revert to any of these checkpoints during the course of developing your app.

</td></tr></tbody>
</table>**Parent Topic:**[Using ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/using-servicenow-studio.md)


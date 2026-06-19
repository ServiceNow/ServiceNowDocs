---
title: Workspace tutorial for agents starting with a chat
description: Walk through this tutorial to get an idea how you can use workspace when you receive a task by phone or chat.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-user-interface/configure-user-experiences/workspace-tutorial-agents-chat.html
release: zurich
product: Configure User Experiences
classification: configure-user-experiences
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Learn how to use your Workspace, Starting in your Workspace, Use, Configurable Workspace UI, Configure UIs and portals, Configure user experiences]
---

# Workspace tutorial for agents starting with a chat

Walk through this tutorial to get an idea how you can use workspace when you receive a task by phone or chat.

## Before you begin

Role required: agent

## About this task

This tutorial starts with an agent working on a request that started with a chat. The workflow would be almost identical if the issue started with a phone call.

## Procedure

1.  Open your workspace by navigating to **Workspace Experience** &gt; **Administration** &gt; **All Workspaces** and clicking the name of your workspace.

2.  Click the name of your workspace and then under Related Links, click **Open workspace**.

3.  Log into your workspace.

4.  Click the inbox icon \(\[Omitted image "inbox-outline.png"\] Alt text: Inbox icon\) and set your status to **Available**.

    The green circle at the top left of the icon shows your status is **Available**. A number appears at the top, right of the icon \[Omitted image "inbox-with-waiting-mail.png"\] Alt text: Inbox with chat ready when there are one or more chats available to answer.

5.  Click the inbox to open a chat.

    You're given the opportunity to accept the chat.

    \[Omitted image "ChatIncoming.png"\] Alt text: Accept or reject a chat

    The **Time to accept** counter shows how much time you have to accept the chat. When the counter reaches zero, the chat opportunity disappears from your inbox.

6.  Click **Accept**.

    The chat pane appears and workspace automatically creates an interaction record, assigns it to you, and enters it in the database.

    \[Omitted image "chat-view.png"\] Alt text: Chat pane

7.  Chat with the requester to find out what the issue is.

    \[Omitted image "active-chat-window.png"\] Alt text: Active chat window

8.  Add information about the customer and issue to the interaction record.

    \[Omitted image "chat-interaction-record.png"\] Alt text: Chat interaction record

9.  You can verify the customer's information by clicking the **Verify contact** or **Verify customer** UI action button.

    **Note:** Not all workspaces have these buttons.

    A modal appears that displays personal information about the contact or customer. You can ask the requester for this information to confirm their identity.

    \[Omitted image "lookup-verify-verification-card.png"\] Alt text: Lookup and verify verification card

10. You can transfer the chat to another agent who has more experience with the issue.

    1.  From the Action toolbar in the Active chat panel, click the Transfer Agent icon \(\[Omitted image "TransferAgentIcon.png"\] Alt text: Transfer agent icon\).

    2.  In the Transfer to Agent window, select the agent to receive the chat and enter a message to that agent.

        **Note:** Only the current owner of a chat may transfer the chat to another agent. The transfer button is otherwise disabled.

        \[Omitted image "Transfer2Agent.png"\] Alt text: List of agents available for transfer.

        The transferred chat is listed in the Queues panel for the receiving agent. The receiving agent can accept or decline the transfer request. When the agent accepts the request, you get a confirmation.

        \[Omitted image "ChatTransfer.png"\] Alt text: Transfer chat

11. After chatting, you might decide to create an incident out of this interaction record. Click **Create incident** to create an incident and transfer the information from the interaction to the incident record.

    \[Omitted image "chat-to-incident.gif"\] Alt text: Change chat to incident

    The incident is automatically assigned to you.

12. Click **Save** to save the incident.

13. Look at the information in the ribbon to get information about the requester and the record.

    \[Omitted image "ribbon-1.png"\] Alt text: ribbon

14. Click several of the items in the related items menu to see what other records might be linked to the one that's open.

    \[Omitted image "related-list-reordered.png"\] Alt text: Related items menu

    For example, clicking **Outages** shows related system failures, and **Child incidents** shows incidents related to this one.

15. Use Agent assist to research the incident.

    If the suggestions in Agent assist don't provide answers for the incident, enter a search term.

    \[Omitted image "agent-assist-search-term.png"\] Alt text: Search in Agent Assist

16. Document what you've done. In **Activity**, in the **Compose** field, click **Comments** and enter a note to the requester explaining what you did.

    \[Omitted image "enter-a-comment.png"\] Alt text: Enter a comment in Activity

17. Click **Post Comments**.

    Workspace sends your comment to the requester and also adds it to the Activity Stream, which is the history of communications and actions you've taken.

    \[Omitted image "activity-stream-entry.png"\] Alt text: Activity stream entry

18. Click **Work notes \(Private\)**, enter a comment, and click **Post Comments** to save information that's only seen by fellow agents. You might use this internal commenting feature if you've not completely resolved an issue but want to document what you've done for other agents or yourself when you come back to the issue later.

19. Click **Save** or **Resolve**, depending on whether or not you've completed your work on this incident.



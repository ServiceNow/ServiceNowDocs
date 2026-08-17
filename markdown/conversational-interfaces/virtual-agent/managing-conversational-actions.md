---
title: Managing conversational actions in Assistant Designer Asset library
description: View and manage conversational actions through Assistant Designer Asset library.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/conversational-interfaces/virtual-agent/managing-conversational-actions.html
release: zurich
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2026-05-13"
reading_time_minutes: 2
keywords: [Conversational, Action, Virtual Agent, Designer, GenAI]
breadcrumb: [Getting started with Assistant Designer Asset library, Build and deploy, Virtual Agent, Conversational Interfaces]
---

# Managing conversational actions in Assistant Designer Asset library

View and manage conversational actions through Assistant Designer Asset library.

**Note:** An updated Assistant Designer Asset library user interface is available when you install ServiceNow Otto in Virtual Agent. This content assumes that you can see the list view. If ServiceNow Otto in Virtual Agent is not installed, you see the legacy UI and topics page. For more information, see [Virtual Agent Designer legacy topics page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/virtual-agent/vad-prev-topics-page.md).

When you have the admin or virtual\_agent\_admin role, you can work with conversational actions in Assistant Designer.

Conversational actions currently can't be created in Assistant Designer Asset library, only viewed and edited. You can only create, test, and delete conversational actions in Workflow Studio. For more details on creating actions, see [Create an action in Workflow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/build-workflows/create-action.md).

When you open an action, a tab is displayed in the navigation header bar. This tab opens the action in Workflow Studio within the Assistant Designer Asset library environment. The following columns appear by default:

|Column|Description|
|------|-----------|
|Name|Name of the action. Select the name of the action to work with that action directly in Assistant Designer Asset library.|
|Type|Action.|
|Status|Status type such as Published.|
|Active|Whether the GenAI skill is active or inactive.|
|Last modified|Time that the subflow was last modified.|
|Description|Description of the action.|

\[Omitted image "conversational-actions-vad-2.png"\] Alt text: Actions tab in Assistant Designer Asset library that displays basic information about conversational actions in a list.

Use the row actions icon \[Omitted image "kebab-menu.png"\] Alt text: to work with visibility settings for **Promoted**, **Discoverable**, **Visible**, and **Active**:

|Option|Description|
|------|-----------|
|Promoted|Option to toggle the action's **Promoted** status to show as a suggested conversational asset in the virtual assistant.|
|Discoverable|Option to toggle the action's **Discoverable** status. If discoverable, the action is invoked when matched with a user's utterance.|
|Visible|Option to toggle the action's visibility to users. If visible, the action appears whenever the **Show me everything** option is selected in the conversation.|
|Active|Option to toggle the action's active status. If active, the action is available within the conversation.|
|Delete|Option to delete the action is not applicable within Assistant Designer Asset library because actions can only be deleted within Workflow Studio.|

-   For more information on the ServiceNow Otto Panel, see [ServiceNow Otto panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-panel-overview.md).
-   For more information on conversational actions, see [Conversational actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/build-workflows/conversational-actions.md).
-   For more information on integrating actions that are not conversational into Assistant Designer Asset library topics, see [Integrating Virtual Agent with Workflow Studio workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/virtual-agent/va-flow-designer-integration.md).

**Parent Topic:**[Getting started with Assistant Designer Asset library](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/virtual-agent/conversation-designer-virtual-agent.md)


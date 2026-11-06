---
title: Managing conversational actions in Assistant Designer
description: View and manage conversational actions using Assistant Designer.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/conversational-interfaces/virtual-agent/managing-conversational-actions.html
release: brazil
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 1
keywords: [Conversational, Action, Virtual Agent, Designer, GenAI]
breadcrumb: [Managing asset library items, Build conversations, Virtual Agent, Conversational Interfaces]
---

# Managing conversational actions in Assistant Designer

View and manage conversational actions using Assistant Designer.

When you have the admin or virtual\_agent\_admin role, you can work with conversational actions in Assistant Designer.

Conversational actions currently can't be created in Assistant Designer. You can only view and edit them in Assistant Designer. Conversational actions can be created, tested, and deleted only in Workflow Studio. For more details about creating actions, see [Create an action in Workflow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/build-workflows/create-action.md).

When you open an action, a tab is displayed in the navigation header bar. This tab opens the action in Workflow Studio within the Assistant Designer environment. The following columns appear by default:

|Column|Description|
|------|-----------|
|Name|Name of the action. Select the name of the action to work with that action directly in Assistant Designer.|
|Type|Action.|
|Status|Status type, such as Published.|
|Active|Whether the asset is active or inactive.|
|Last modified|Time that the subflow was last modified.|
|Description|Description of the action.|

\[Omitted image "conversational-actions-vad.png"\] Alt text: Actions tab in Assistant Designer Asset library that displays basic information about conversational actions in a list.

Use the row actions icon \[Omitted image "kebab-menu.png"\] Alt text: to work with visibility settings for **Promoted**, **Discoverable**, **Visible**, and **Active**:

|Option|Description|
|------|-----------|
|Promoted|Option to toggle the action's **Promoted** status to show as a suggested conversational asset in the virtual assistant.|
|Discoverable|Option to toggle the action's **Discoverable** status. If discoverable, the action is invoked when matched with a user's utterance.|
|Visible|Option to toggle the action's visibility to users. If visible, the action appears whenever the **Show me everything** option is selected in the conversation.|
|Active|Option to toggle the action's active status. If active, the action is available within the conversation.|
|Delete|Option to delete the action is not applicable within Assistant Designer because actions can only be deleted within Workflow Studio.|

**Parent Topic:**[Managing asset library items](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/managing-asset-library-items.md)

**Related topics**  


[ServiceNow Otto panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/now-assist-panel-overview.md)

[Conversational actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/build-workflows/conversational-actions.md)

[Integrating Virtual Agent with Workflow Studio workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/va-flow-designer-integration.md)


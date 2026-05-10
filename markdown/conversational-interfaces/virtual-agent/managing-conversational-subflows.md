---
title: Managing conversational subflows in Assistant Designer
description: View and manage conversational subflows through Assistant Designer.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [Conversational, Subflow, Virtual Agent, Designer, GenAI]
breadcrumb: [Getting started with Virtual Agent Designer, Build and deploy, Virtual Agent, Conversational Interfaces]
---

# Managing conversational subflows in Assistant Designer

View and manage conversational subflows through Assistant Designer.

**Note:** An updated Assistant Designer Asset library user interface is available when you install Now Assist in Virtual Agent and turn on the Now Assist Topics skill. This content assumes that you have activated this skill and can see the list view. If this skill is not activated, you see the legacy UI and topics page. For more information, see [Virtual Agent Designer legacy topics page](../reference/vad-prev-topics-page.md).

When you have the admin or virtual\_agent\_admin role, you can work with conversational subflows in Assistant Designer.

Conversational subflows currently can't be created in Assistant Designer. You can only view and edit them in Assistant Designer. Conversational subflows can be created, tested, and deleted only in Workflow Studio. For more details on creating subflows, see [Create a subflow in Workflow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/create-subflow.md).

When you open a subflow in Assistant Designer, a tab is displayed in the navigation header bar. This tab opens the subflow in Workflow Studio within the Assistant Designer environment. The following columns appear by default:

|Column|Description|
|------|-----------|
|Name|Name of the subflow. Select the name of the subflow to work with that subflow directly in Assistant Designer.|
|Type|Subflow.|
|Status|Status type such as Published.|
|Active|Whether the GenAI skill is active or inactive.|
|Last modified|Time that the subflow was last modified.|
|Description|Description of the subflow.|

![Subflows tab inAssistant Designer Asset library that displays basic information about conversational subflows in a list.](../images/conversational-subflow-vad.png)

Use the row actions icon ![](../images/kebab-menu.png) to work with visibility settings for **Promoted**, **Discoverable**, **Visible**, and **Active**.

|Option|Description|
|------|-----------|
|Promoted|Option to toggle the subflow's **Promoted** status to show as a suggested conversational asset in the virtual assistant.|
|Discoverable|Option to toggle the subflow's **Discoverable** status. If discoverable, the subflow is invoked when matched with a user's utterance.|
|Visible|Option to toggle the subflow's visibility to users. If visible, the subflow appears whenever the **Show me everything** option is selected in the conversation.|
|Active|Option to toggle the subflow's active status. If active, the subflow is available within the conversation.|
|Delete|Option to delete the subflow is not applicable within Assistant Designer because subflows can only be deleted within Workflow Studio.|

Conversational subflows and actions only appear to users during a Virtual Agent conversation if the Subflows and actions skill is turned on in Now Assist Admin. Conversational subflows and actions appear in Now Assist Panel as long as the Subflows and action skill is active.

-   For more information on the Now Assist Panel, see [Now Assist panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-panel-overview.md).
-   For more information on conversational subflows, see [Conversational subflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/conversational-subflows.md).
-   For more information on integrating subflows that are not conversational into Assistant Designer assets, see [Integrating Virtual Agent with Workflow Studio workflows](va-flow-designer-integration.md).

**Parent Topic:**[Getting started with Virtual Agent Designer](../reference/conversation-designer-virtual-agent.md)


---
title: Managing conversational subflows in Assistant Designer Asset library
description: View and manage conversational subflows through Assistant Designer Asset library.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/conversational-interfaces/virtual-agent/managing-conversational-subflows.html
release: zurich
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2026-05-13"
reading_time_minutes: 2
keywords: [Conversational, Subflow, Virtual Agent, Designer, GenAI]
breadcrumb: [Getting started with Assistant Designer Asset library, Build and deploy, Virtual Agent, Conversational Interfaces]
---

# Managing conversational subflows in Assistant Designer Asset library

View and manage conversational subflows through Assistant Designer Asset library.

**Note:** An updated Assistant Designer Asset library user interface is available when you install ServiceNow Otto in Virtual Agent. This content assumes that you can see the list view. If ServiceNow Otto in Virtual Agent is not installed, you see the legacy UI and topics page. For more information, see [Virtual Agent Designer legacy topics page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/virtual-agent/vad-prev-topics-page.md).

When you have the admin or virtual\_agent\_admin role, you can work with conversational subflows in Assistant Designer Asset library.

Conversational subflows currently can't be created in Assistant Designer Asset library, only viewed and edited. Conversational subflows can be created, tested, and deleted only in Workflow Studio. For more details on creating subflows, see [Create a subflow in Workflow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/build-workflows/create-subflow.md).

When you open a subflow in Assistant Designer Asset library, a tab is displayed in the navigation header bar. This tab opens the subflow in Workflow Studio within the Assistant Designer Asset library environment. The following columns appear by default:

|Column|Description|
|------|-----------|
|Name|Name of the subflow. Select the name of the subflow to work with that subflow directly in Assistant Designer Asset library.|
|Type|Subflow.|
|Status|Status type such as Published.|
|Active|Whether the GenAI skill is active or inactive.|
|Last modified|Time that the subflow was last modified.|
|Description|Description of the subflow.|

\[Omitted image "conversational-subflow-vad-2.png"\] Alt text: Subflows tab in Assistant Designer Asset library that displays basic information about conversational subflows in a list.

Use the row actions icon \[Omitted image "kebab-menu.png"\] Alt text: to work with visibility settings for **Promoted**, **Discoverable**, **Visible**, and **Active**.

|Option|Description|
|------|-----------|
|Promoted|Option to toggle the subflow's **Promoted** status to show as a suggested conversational asset in the virtual assistant.|
|Discoverable|Option to toggle the subflow's **Discoverable** status. If discoverable, the subflow is invoked when matched with a user's utterance.|
|Visible|Option to toggle the subflow's visibility to users. If visible, the subflow appears whenever the **Show me everything** option is selected in the conversation.|
|Active|Option to toggle the subflow's active status. If active, the subflow is available within the conversation.|
|Delete|Option to delete the subflow is not applicable within Assistant Designer Asset library because subflows can only be deleted within Workflow Studio.|

-   For more information on the ServiceNow Otto Panel, see [ServiceNow Otto panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-panel-overview.md).
-   For more information on conversational subflows, see [Conversational subflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/build-workflows/conversational-subflows.md).
-   For more information on integrating subflows that are not conversational into Assistant Designer Asset library topics, see [Integrating Virtual Agent with Workflow Studio workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/virtual-agent/va-flow-designer-integration.md).

**Parent Topic:**[Getting started with Assistant Designer Asset library](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/virtual-agent/conversation-designer-virtual-agent.md)


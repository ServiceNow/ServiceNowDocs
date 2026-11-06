---
title: Managing conversational subflows in Assistant Designer
description: View and manage conversational subflows through Assistant Designer.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/conversational-interfaces/virtual-agent/managing-conversational-subflows.html
release: brazil
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 1
keywords: [Conversational, Subflow, Virtual Agent, Designer, GenAI]
breadcrumb: [Managing asset library items, Build conversations, Virtual Agent, Conversational Interfaces]
---

# Managing conversational subflows in Assistant Designer

View and manage conversational subflows through Assistant Designer.

When you have the admin or virtual\_agent\_admin role, you can work with conversational subflows in Assistant Designer.

Conversational subflows currently can't be created in Assistant Designer. You can only view and edit them in Assistant Designer. Conversational subflows can be created, tested, and deleted only in Workflow Studio. For more details on creating subflows, see [Create a subflow in Workflow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/build-workflows/create-subflow.md).

When you open a subflow in Assistant Designer, a tab is displayed in the navigation header bar. This tab opens the subflow in Workflow Studio within the Assistant Designer environment. The following columns appear by default:

|Column|Description|
|------|-----------|
|Name|Name of the subflow. Select the name of the subflow to work with that subflow directly in Assistant Designer.|
|Type|Subflow.|
|Status|Status type such as Published.|
|Active|Whether the asset is active or inactive.|
|Last modified|Time that the subflow was last modified.|
|Description|Description of the subflow.|

\[Omitted image "conversational-subflow-vad.png"\] Alt text: Subflows tab in Assistant Designer Asset library that displays basic information about conversational subflows in a list.

Use the row actions icon \[Omitted image "kebab-menu.png"\] Alt text: to work with visibility settings for **Promoted**, **Discoverable**, **Visible**, and **Active**.

|Option|Description|
|------|-----------|
|Promoted|Option to toggle the subflow's **Promoted** status to show as a suggested conversational asset in the virtual assistant.|
|Discoverable|Option to toggle the subflow's **Discoverable** status. If discoverable, the subflow is invoked when matched with a user's utterance.|
|Visible|Option to toggle the subflow's visibility to users. If visible, the subflow appears whenever the **Show me everything** option is selected in the conversation.|
|Active|Option to toggle the subflow's active status. If active, the subflow is available within the conversation.|
|Delete|Option to delete the subflow is not applicable within Assistant Designer because subflows can only be deleted within Workflow Studio.|

**Parent Topic:**[Managing asset library items](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/managing-asset-library-items.md)

**Related topics**  


[ServiceNow Otto panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/now-assist-panel-overview.md)

[Conversational subflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/build-workflows/conversational-subflows.md)

[Integrating Virtual Agent with Workflow Studio workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/va-flow-designer-integration.md)


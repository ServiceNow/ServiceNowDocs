---
title: Managing custom skills in Assistant Designer Asset library
description: View custom skills through Assistant Designer Asset library.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2026-03-24"
reading_time_minutes: 2
keywords: [Conversational, Action, Virtual Agent, Designer, GenAI]
breadcrumb: [Getting started with Virtual Agent Designer, Build and deploy, Virtual Agent, Conversational Interfaces]
---

# Managing custom skills in Assistant Designer Asset library

View custom skills through Assistant Designer Asset library.

**Note:** Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents. For more information, see ServiceNow product tiers.

**Note:** An updated Assistant Designer Asset library user interface is available when you install Now Assist in Virtual Agent and turn on the Now Assist Topics skill. This content assumes that you have activated this skill and can see the list view. If this skill is not activated, you see the legacy UI and topics page. For more information, see [Virtual Agent Designer legacy topics page](../reference/vad-prev-topics-page.md).

**Role required**: virtual\_agent\_admin

When you select a custom skill, it opens the skill in Now Assist Skill Kit. Custom skills currently can't be created in Virtual Agent Designer. You can only view them in Assistant Designer Asset library. The skills can be created, tested, and deleted only in Now Assist Skill Kit. For more details on creating skills, see Create a skill.

![Custom skills pill inAssistant Designer Asset library.](../images/vad-custom-skills.png "Custom skills as viewed in Assistant Designer Asset library")

|Column|Description|
|------|-----------|
|Name|Name of the skill. Select the skill to open it in Now Assist Skill Kit.|
|Type|Custom skill.|
|Status|Status type such as Published.|
|Active|Whether the skill is active or inactive.|
|Last modified|Time that the skill was last modified.|
|Description|Description of the custom skill.|

Use the row actions icon ![](../images/kebab-menu.png) to work with visibility settings for **Promoted**, **Discoverable**, **Visible**, and **Active**:

|Option|Description|
|------|-----------|
|Promoted|Option to toggle the skill's **Promoted** status to show as a suggested conversational asset in the virtual assistant.|
|Discoverable|Option to toggle the skill's **Discoverable** status. If discoverable, the skill is invoked when matched with a user's utterance.|
|Visible|Option to toggle the skill's visibility to users. If visible, the skill appears whenever the **Show me everything** option is selected in the conversation.|
|Active|Option to toggle the skill's active status. If active, the skill is available within the conversation.|
|Delete|Delete option for skills is inactive in Assistant Designer Asset library. The skills can only be deleted from Now Assist Skill Kit.|

Custom skills become available in Assistant Designer Asset library based on the deployment settings in Now Assist Skill Kit.

1.  Navigate to **Now Assist Skill Kit** &gt; **Home** and select the skill.
2.  Select **Skill settings** &gt; **Deployment settings**.
3.  For the skill to become available in Assistant Designer Asset library, the following options should be selected:
    -   Select **Platform skills** in the **Feature** list.
    -   Select the **Now Assist panel** card to enable the skill through the Now Assist Panel.

-   For more information about the Now Assist Panel, see Now Assist panel.
-   For more information about Now Assist Skill Kit, see Now Assist Skill Kit.

**Parent Topic:**[Getting started with Virtual Agent Designer](../reference/conversation-designer-virtual-agent.md)


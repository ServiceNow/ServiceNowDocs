---
title: Generate multiple stories at once in EAP using Now Assist for SPM
description: Breakdown epics and features into stories using the Now Assist panel in the Enterprise Agile Planning \(EAP\) workspace. Based on the work item details, Now Assist generates stories.
locale: en-US
release: australia
product: Enterprise Agile Planning
classification: enterprise-agile-planning
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Manage team backlog, Use, Enterprise Agile Planning, Strategic Planning, Strategic Portfolio Management]
---

# Generate multiple stories at once in EAP using Now Assist for SPM

Breakdown epics and features into stories using the Now Assist panel in the Enterprise Agile Planning \(EAP\) workspace. Based on the work item details, Now Assist generates stories.

## Before you begin

**Important:** This Now Assist skill is turned on by default. The skill will be automatically available to appropriate role users for the application. For more information, see [Now Assist skills, agents, and agentic workflows on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

**Note:** Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents. For more information, see [ServiceNow product tiers](https://www.servicenow.com/docs/access?context=ai-native-sku-overview&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

Role required: sn\_apw\_advanced.eap\_user or sn\_apw\_advanced.eap\_read\_only, with now\_assist\_panel\_user

If you have custom roles that require access to this skill, update the ACLs for those roles that require access. For more information, see [Implement access control in Now Assist AI agents](https://www.servicenow.com/docs/access?context=aia-security-implementation&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

## About this task

## Procedure

1.  Navigate to **Workspaces** &gt; **Strategic Planning Workspace** &gt; **Enterprise Agile Planning**.

2.  From the Agile structure section of the navigation panel, choose your EAP team that has an epic or feature as its work item type.

3.  From the Backlog or Planning board pages, select an epic or a feature for which you want to create stories.

    The work item details are displayed in the side panel.

4.  From the side panel, select **Full details**.

5.  From the work item header, select **Create stories** to open the Now Assist panel and trigger the Create stories agentic workflow.

    The AI agent generates story recommendations based on the context available within the epic or feature.

6.  Go through the story recommendations and choose to confirm, combine, split, remove any of the stories, suggest modifications, or create more stories.

    **Tip:** While Now Assist is working on the story recommendations for the current work item, you can start a new chat to create stories for another epic or feature. Select **New chat** \(![](../images/icon-na-new-chat.png)\) from the Now Assist panel header. You can switch between chats by selecting **All chats** \(![](../images/icon-na-all-chats.png)\).

7.  You can iterate on any of these actions and when you’re satisfied with the recommendations, enter **Save**.

    Now Assist creates stories with the confirmed recommendations. The newly created stories are displayed in the Stories tab of the epic or feature details page.


**Parent Topic:**[Manage team backlog in EAP](../../spw-eap/concept/using-eap.md)

**Parent Topic:**[Using Now Assist for Strategic Portfolio Management \(SPM\)](../concept/using-now-assist-for-spm.md)

**Related topics**  


[Configure Create stories agentic workflow with Now Assist for SPM](configure-create-stories-agentic-workflow-now-assist-for-spm.md)

[Create stories agentic workflow using Now Assist for Strategic Portfolio Management \(SPM\)](../concept/generate-agile-story-planning-items.md)


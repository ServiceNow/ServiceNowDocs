---
title: Generate stories for work items in EAP using ServiceNow Otto for SPM
description: Breakdown epics and features into stories using the Now Assist panel in the Enterprise Agile Planning \(EAP\) workspace. Based on the work item details, Now Assist generates stories.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-business-management/enterprise-agile-planning/generate-stories-from-epics-now-assist-eap.html
release: zurich
product: Enterprise Agile Planning
classification: enterprise-agile-planning
topic_type: task
last_updated: "2025-08-26"
reading_time_minutes: 2
breadcrumb: [Manage team backlog, Use, Enterprise Agile Planning, Strategic Planning, Strategic Portfolio Management]
---

# Generate stories for work items in EAP using ServiceNow Otto for SPM

Breakdown epics and features into stories using the Now Assist panel in the Enterprise Agile Planning \(EAP\) workspace. Based on the work item details, Now Assist generates stories.

## Before you begin

**Important:** This generative AI skill is turned on by default. The skill will be automatically available to appropriate role users for the application. For more information, see [AI agents, skills, and agentic workflows on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-skills-on-by-default.md).

Role required: sn\_apw\_advanced.eap\_user or sn\_apw\_advanced.eap\_read\_only, with now\_assist\_panel\_user

If you have custom roles that require access to this skill, update the ACLs for those roles that require access. For more information, see [Implement access control in AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/aia-security-implementation.md).

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

    **Tip:** While Now Assist is working on the story recommendations for the current work item, you can start a new chat to create stories for another epic or feature. Select **New chat** \(\[Omitted image "icon-na-new-chat.png"\] Alt text:\) from the Now Assist panel header. You can switch between chats by selecting **All chats** \(\[Omitted image "icon-na-all-chats.png"\] Alt text:\).

7.  You can iterate on any of these actions and when you’re satisfied with the recommendations, enter **Save**.

    Now Assist creates stories with the confirmed recommendations. The newly created stories are displayed in the Stories tab of the epic or feature details page.


**Parent Topic:**[Manage team backlog in EAP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/enterprise-agile-planning/using-eap.md)

**Related topics**  


[Configure Create stories agentic workflow with ServiceNow Otto for SPM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/enterprise-agile-planning/configure-create-stories-agentic-workflow-now-assist-for-spm.md)

[Create stories agentic workflow using ServiceNow Otto for Strategic Portfolio Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/enterprise-agile-planning/generate-agile-story-planning-items.md)


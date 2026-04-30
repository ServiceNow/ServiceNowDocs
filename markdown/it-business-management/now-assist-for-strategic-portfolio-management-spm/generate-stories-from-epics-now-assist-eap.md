---
title: Generate stories for work items in EAP using Now Assist for SPM
description: Breakdown epics and features into stories using the Now Assist panel in the Enterprise Agile Planning \(EAP\) workspace. Based on the work item details, Now Assist generates stories.
locale: en-US
release: yokohama
product: Now Assist for Strategic Portfolio Management \(SPM\)
classification: now-assist-for-strategic-portfolio-management-spm
topic_type: task
last_updated: "2025-08-26"
reading_time_minutes: 2
breadcrumb: [Using Now Assist for Strategic Portfolio Management \(SPM\), Now Assist for Strategic Portfolio Management \(SPM\), Strategic Portfolio Management]
---

# Generate stories for work items in EAP using Now Assist for SPM

Breakdown epics and features into stories using the Now Assist panel in the Enterprise Agile Planning \(EAP\) workspace. Based on the work item details, Now Assist generates stories.

## Before you begin

Activate the Agile story generation skill for Enterprise Agile Planning. See [Configure Now Assist for Strategic Portfolio Management \(SPM\)](configure-now-assist-for-spm.md).

Role required: sn\_apw\_advanced.eap\_user or sn\_apw\_advanced.eap\_read\_only, with now\_assist\_panel\_user

If you have custom roles that require access to this skill, update the ACLs for those roles that require access. For more information, see [Implement access control in Now Assist AI agents](https://www.servicenow.com/docs/access?context=aia-security-implementation&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).

## About this task

Generate stories from epics using Now Assist. 

## Procedure

1.  Navigate to **Workspaces** &gt; **Strategic Planning Workspace** &gt; **Enterprise Agile Planning**.

2.  From the Agile structure section of the navigation panel, choose your EAP team that has an epic or feature as its work item type.

3.  From the Backlog or Planning board pages, select an epic or a feature for which you want to create stories.

    The work item details are displayed in the side panel.

4.  From the side panel, select **Full details**.

5.  From the instance header, select **Now Assist** to open the Now Assist panel.

6.  In the Now Assist panel, select **Create stories**.

    Now Assist generates story recommendations based on the name, description, Docs content, and any existing stories for the work item.

    If you haven't performed step 4, Now Assist asks you to enter the epic or feature number. Referring to the work item number you provided, it provides story recommendations for it.

    ![Now Assist asking for epic or feature number before generating stories.](../images/eap-na-stories-work-item-number.png)

    The number of initial story recommendations that you see depend on the input data settings for this skill. You can work with your admin to modify this number. For more information, see [Skill inputs for Now Assist for Strategic Portfolio Management \(SPM\)](../reference/skill-inputs-for-now-assist-for-spm.md).

7.  Go through the story recommendations and choose to confirm, combine, split, remove any of the stories, or choose **Others** to suggest modifications or create more stories.

    **Tip:** While Now Assist is working on the story recommendations for the current work item, you can start a new chat to create stories for another epic or feature. Select **New chat** \(![](../images/icon-na-new-chat.png)\) from the Now Assist panel header. You can switch between chats by selecting **All chats** \(![](../images/icon-na-all-chats.png)\).

8.  You can iterate on any of these actions and when you’re satisfied with the recommendations, select **Confirm &amp; Save**.

    Now Assist creates stories with the confirmed recommendations. The newly created stories are displayed in the Stories tab of the epic and feature details page.


**Parent Topic:**[Using Now Assist for Strategic Portfolio Management \(SPM\)](../concept/using-now-assist-for-spm.md)


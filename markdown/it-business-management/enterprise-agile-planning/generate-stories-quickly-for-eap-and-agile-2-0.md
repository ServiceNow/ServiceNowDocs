---
title: Generate a story from an epic using Now Assist for SPM in EAP
description: Generate a complete user story directly from an epic using Quick story generation feature in EAP. Provide brief context, and Now Assist generates a story title, description, and acceptance criteria that you can review and edit before saving.
locale: en-US
release: australia
product: Enterprise Agile Planning
classification: enterprise-agile-planning
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Manage team backlog, Use, Enterprise Agile Planning, Strategic Planning, Strategic Portfolio Management]
---

# Generate a story from an epic using Now Assist for SPM in EAP

Generate a complete user story directly from an epic using Quick story generation feature in EAP. Provide brief context, and Now Assist generates a story title, description, and acceptance criteria that you can review and edit before saving.

## Before you begin

**Important:** This Now Assist skill is turned on by default. The skill will be automatically available to appropriate role users for the application. For more information, see [Now Assist skills, agents, and agentic workflows on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skills/now-assist-skills-on-by-default.md).

**Important:** Quick story generation is only available if the following two skills are active:

-   Agile story generation
-   Generate acceptance criteria

**Note:** Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents. For more information, see [ServiceNow product tiers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-native-sku-overview.md).

Role required: sn\_apw\_advanced.eap\_user

## About this task

AI quick story generation in EAP 

## Procedure

1.  Navigate to **Workspaces** &gt; **Strategic Planning Workspace** &gt; **Enterprise Agile Planning**.

2.  From the Agile structure section of the navigation panel, choose your EAP team that has an epic as its work item type.

3.  From the Backlog, Hierarchy, or Planning board tabs, open your epic in its full details page.

4.  Navigate to the Stories related list.

5.  Select **Generate Story**.

6.  In the context field, enter one or two lines describing the focus of the story.

    For example, enter context such as "progress tracking for onboarding steps to help users visualize their journey and reduce abandonment rates" to direct Now Assist toward a specific area of the epic.

7.  Select **Generate**.

    ![Generate story modal with a Story context field to enter details.](../images/eap-na-quick-story.png)

    Now Assist generates a story title, description, and acceptance criteria based on the epic context and the input you provided.

8.  Review and edit any of the generated fields inline to refine the story before saving.

    All fields are editable. You can modify, add to, or remove generated content in the title, description, and acceptance criteria fields.

    ![AI recommended story with detailed description and acceptance criteria.](../images/eap-na-quick-story-preview.png)

9.  Select **Save story**.

    The new story is added to the Stories list of the epic.


## What to do next

To further refine the story after saving, open the story record and select **Generate acceptance criteria** to regenerate or update the acceptance criteria using Now Assist. For more information, see [Generate acceptance criteria for EAP stories using Now Assist for Strategic Portfolio Management \(SPM\)](eap-generate-acceptance-criteria-for-stories.md).

**Parent Topic:**[Manage team backlog in EAP](../../spw-eap/concept/using-eap.md)

**Parent Topic:**[Using Now Assist for Strategic Portfolio Management \(SPM\)](../concept/using-now-assist-for-spm.md)

**Related topics**  


[Generate multiple stories at once in EAP using Now Assist for SPM](generate-stories-from-epics-now-assist-eap.md)

[Generate acceptance criteria for EAP stories using Now Assist for Strategic Portfolio Management \(SPM\)](eap-generate-acceptance-criteria-for-stories.md)


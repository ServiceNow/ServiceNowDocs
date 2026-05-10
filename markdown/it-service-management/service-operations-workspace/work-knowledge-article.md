---
title: Work on a knowledge article in Service Operations Workspace
description: Share information across your organization using a knowledge article.
locale: en-US
release: australia
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Knowledge Management in Service Operations Workspace, Managing IT services in your organization, Service Operations Workspace for ITSM, IT Service Management]
---

# Work on a knowledge article in Service Operations Workspace

Share information across your organization using a knowledge article.

## Before you begin

Role required: itil

## Procedure

1.  Open a knowledge article in Service Operations Workspace.

2.  Perform any of the following actions on the record page.

<table id="choicetable_hvj_ccg_vsb"><thead><tr><th align="left" id="d128947e61">

Option

</th><th align="left" id="d128947e64">

Description

</th></tr></thead><tbody><tr><td id="d128947e70">

**Create a new version of the knowledge article that we can publish**

</td><td>

Select **Checkout**.

</td></tr><tr><td id="d128947e82">

**Translate an article after its comparison in its original language and the language it will be translated into**

</td><td>

1.  Select **Translate**.
2.  Review the translation and click **Create draft article**.

**Note:** If Dynamic Translation is enabled, click **Machine Translate** to view machine translations.

</td></tr><tr><td id="d128947e112">

**View a knowledge article including the article number, short description, and article content**

</td><td>

Select **View Article**.

</td></tr><tr><td id="d128947e124">

**Initiate the retirement workflow associated with the article**

</td><td>

From the more options drop-down \(![more actions icon](../../itsm-workspace/image/more-actions-icon.png)\), select **Retire**. For information about retiring a knowledge article, see [Retire a knowledge article](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/knowledge-management/c_RetiredKnowledgeArticles.md).

</td></tr><tr><td id="d128947e147">

**Translate an article into multiple languages**

</td><td>

1.  From the more options drop-down \(![more actions icon](../../itsm-workspace/image/more-actions-icon.png)\), select **Request translations**.
2.  Select the languages you want to translate the article into.
3.  Select **Submit**.


</td></tr><tr><td id="d128947e180">

**Copy the record page URL to easily access the record**

</td><td>

Select the more actions icon \(![more actions icon](../../itsm-workspace/image/more-actions-icon.png)\) and select **Copy URL**.

</td></tr><tr><td id="d128947e198">

**Reuse a knowledge block when creating or editing the article**

</td><td>

1.  From the contextual side panel, select the add blocks icon \(![add blocks icon](../image/add-blocks-icon.png)\).
2.  Select the required knowledge block to add it to the article.


</td></tr><tr><td id="d128947e222">

**Attach a record that helps in quick resolution of the interaction**

</td><td>

1.  From the contextual side panel, select the agent assist icon \(![agent assist icon](../image/agent-assist-icon.png)\).
2.  Search for a resource and perform the required action, for example, find a relevant knowledge base article and attach a link to it to work notes.
 **Note:** The agent assist icon is available only for users with the following roles: itil or interaction\_agent.

 For information on configuring additional search resources, see [Configure search resources for an interaction in Service Operations Workspace for ITSM](configure-resources-for-an-interaction.md).

</td></tr><tr><td id="d128947e259">

**Add attachments**

</td><td>

From the contextual side panel, select the attachments icon \(![attachments icon](../../itsm-workspace/image/attachment-icon.png)\). Alternatively, you can drag and drop the attachment into the **Active Chat** window of the interaction.**Note:** The added attachments are displayed in the activity stream in the **Compose** section.

</td></tr><tr><td id="d128947e283">

**Create templates for reuse**

</td><td>

From the contextual side panel, select the templates icon \(![templates icon](../image/template-icon.png)\) and create a template or reuse an existing one.

</td></tr><tr><td id="d128947e299">

**Most recent task**

</td><td>

Related list of task records to which the knowledge article is recently attached. You can select the task record link to open the record another tab within the workspace view. These records are retrieved from the **Knowledge Applied Tasks** \[**m2m\_kb\_task**\] table. **Note:** The related list section is displayed only if the **Display recent task for knowledge article** \(**glide.knowman.recent\_task.display**\) system property is enabled.

</td></tr></tbody>
</table>
**Parent Topic:**[Knowledge Management in Service Operations Workspace](../concept/knowledge-articles-sow.md)


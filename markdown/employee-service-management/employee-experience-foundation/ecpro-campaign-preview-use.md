---
title: Preview your portal
description: Use campaign preview to view the campaign content that appears on your portal. Use the Preview filters to fine-tune what you want to preview.
locale: en-US
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Campaign preview, Creating campaigns, Authoring and managing employee communications, Employee Center Pro, Unified Employee Experience, Employee Service Management]
---

# Preview your portal

Use campaign preview to view the campaign content that appears on your portal. Use the Preview filters to fine-tune what you want to preview.

## Before you begin

Role required: sn\_cd.content\_manager, sn\_ca.campaign\_manager

## Procedure

1.  Navigate to **All** &gt; **Content Experiences** &gt; **Content Experience Builder**.

2.  Select a campaign.

3.  Select the **Portal preview** tab.

    **Note:** You can also show a portal preview by selecting the show preview icon \(![Show Preview icon](../images/campaign-prev-icon.png)\) from the top of a stage.

4.  Use **Preview filters** to determine what you preview.

<table id="table_zfh_53m_ymb"><thead><tr><th>

Filter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Select a stage

</td><td>

The stage or campaign stage/bundle you want to view.Select a specific campaign stage you want to preview the content for.

</td></tr><tr><td>

Refine your audience

</td><td>

The targeted audience for the content in the selected stage.Selecting an audience provides a preview of what content that audience sees.

</td></tr><tr><td>

Select a page

</td><td>

The page on your Service Portal you want to preview.A page is a pre-existing record that contains code and structure that define how to display content you want to schedule and make available to your employees.

**Note:** Templates are contained in a topic and references a page. Templates have a direct relationship with a page, but multiple topics can be associated with a template/page. For example, the base system provides the emp\_employee-taxonomy page and most of the topics are associated with that page. For more information, see [Create topic page template](customise-topic-pages-with-templates.md#).

 When a page has topics associated with it, the **Taxonomy** field appears and you can filter by it and you can select topics associated with the taxonomy.

</td></tr><tr><td>

Select a taxonomy

</td><td>

Allows you to filter your preview by taxonomy.Taxonomy is a collection of hierarchical topics that brings together different content types, like requests, articles, quick links, and employee communications.

 A taxonomy is the top-level of the hierarchy and can have multiple topics under it.

 For example, you can have taxonomies for HR and IT so you can group specific topics under each.

 When you use **Select a page** or **Select a topic** to filter your preview, the value in this field can change because the topic might not be under the taxonomy or on the page you selected. When this field is greyed out, it indicates for the page and topic selected, there is only one taxonomy.

</td></tr><tr><td>

Select a topic

</td><td>

Allows you to preview content associated with a topic.Topics are organized under a taxonomy.

 When the Allow Ownership for Topics \(sn\_cd.activate\_topic\_ownership\) system property is set to **Yes** and the topic is assigned to you or a group you belong to, you only see topics assigned to you or topics that do not have restrictions. For more information, see [Properties installed with Content Experiences](../reference/properties-installed-with-content-auto.md) and [Assign ownership of content](ecpro-ca-cd-content-restriction.md).

</td></tr><tr><td>

Show inactive content

</td><td>

Provides messages in the banner identifying content that is inactive. Toggle switch to green to turn this feature on.

</td></tr></tbody>
</table>    **Note:** Preview filters that are greyed out indicates the displayed value is the only available selection for preview.

    Content highlighted in blue is active and content highlighted in grey is inactive.

5.  Exit **Preview filters** to view the portal.

    **Note:** Select the **View content details** \(![View content details icon](../../human-resources/image/view-content-details-icon.png)\) icon to see additional details about the content.



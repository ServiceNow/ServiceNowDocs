---
title: Create a publish plan for your content
description: After you create content in the Content Library, add one or more publish plans to control where the content is delivered, the audience, and the period of time it is available.
locale: en-US
release: zurich
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Publishing content, Creating employee communications, Manage, Employee Center Pro, Unified Employee Experience, Employee Service Management]
---

# Create a publish plan for your content

After you create content in the Content Library, add one or more publish plans to control where the content is delivered, the audience, and the period of time it is available.

## Before you begin

Role required: sn\_cd.content\_manager

**Note:** When the Enable Content Management Ownership sys properties are activated, you can only schedule and publish content assigned to you. For more information, see [Content Ownership](../concept/ecpro-content-restriction.md)

To publish Rich content to the UIB Workspace, you must create a [schedule content record](ecpro-schedule-content.md), as publish plans do not support publishing to the UIB Workspace.

## Procedure

1.  Navigate to **Content Publishing** &gt; **Content Library**.

2.  Select the content you want to publish.

    If you can't find the content you want to publish, ensure the **Active** field is checked on your content.

3.  Select **Save** or **Save and continue**.

4.  Select the **Publish** tab.

5.  Select **Add a publish plan**.

6.  Fill in the form.

<table id="table_bvw_2rb_grb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Schedule name

</td><td>

The name that describes the schedule for your content.

</td></tr><tr><td>

Order

</td><td>

The order in which the content appears in a widget, relative to other content published to the same widget. Content with a lesser order value appears first.If two content items have the same order value, the content will appear based on the most-recent publish date.

</td></tr><tr><td colspan="2">

WHERE

</td></tr><tr><td>

Location

</td><td>

Where you want your content to appear. Your choices are:-   Service Portal
-   Mobile \(for News articles only\)
-   Workspace: Requires the Human Resources Scoped App: Workspace \(com.sn\_hr\_agent\_workspace\) plugin to be activated.


</td></tr><tr><td>

Section

</td><td>

This option appears if you select **Mobile**.The section in the mobile app where you want the news content to appear. This is a read-only field. An Admin can update this field from the **Content Publishing** &gt; **Advanced** &gt; **Properties**. For more information, see [Properties installed with Content Publishing](../reference/properties-with-content-delivery.md).

</td></tr><tr><td>

Page

</td><td>

This option appears when you select **Service portal** or **Workspace**.The page on your Employee Center you want your content to appear.

A page is a pre-existing record that contains code and structure that define how to display content you want to schedule and make available to your employees.

**Note:** Templates are contained in a topic and references a page. Templates have a direct relationship with a page, but multiple topics can be associated with a template/page. For example, the base system provides the emp\_employee-taxonomy page and most of the topics are associated with that page. For more information, see [Create topic page template](customise-topic-pages-with-templates.md#).

 When a page has topics associated with it, the **Taxonomy** field appears and you can filter by it and you can select topics associated with the taxonomy.

 Select a page and only the widget instances that appear on the page are available in the Widget instance choice list.

 Select the Preview this record icon ![Preview this record icon](../../human-resources/image/view-content-details-icon.png) to view the page record.

**Note:** Using Page to help filter the available widgets across the portal can be useful, but is optional.

</td></tr><tr><td>

Widget

</td><td>

The widget you want your content to appear in. Widgets contain properties and CSS specific to that instance.A list of filtered widget instances appear when you select a page from the **Page** choice list.

 Select the Preview this record icon ![Preview this record icon](../../human-resources/image/view-content-details-icon.png) to view the widget record.

 **Note:** If you schedule Styled or Banner content to the Content Experiences widget on the emp\_taxonomy\_topic page, the original topic banner image does not display for the topics on the schedule.

</td></tr><tr><td>

Taxonomy

</td><td>

The taxonomy or top level in the organization hierarchy you want your content to appear under. Also allows you to filter your preview by taxonomy.

 Taxonomy is a collection of hierarchical topics that brings together different content types, like requests, articles, quick links, and employee communications.

 A taxonomy is the top-level of the hierarchy and can have multiple topics under it.

 For example, you can have taxonomies for HR and IT so you can group specific topics under each.

 When you use **Page** or **Add Topic** to filter your preview, the value in this field can change because the topic might not be under the taxonomy or on the page you selected. When this field is greyed out, it indicates for the page and topic selected, there is only one taxonomy.

</td></tr><tr><td>

Add Topic

</td><td>

The topic you want your content to appear under.Also, allows you to preview content associated with a topic.

 Topics are organized under a taxonomy.

 When the Allow Ownership for Topics \(sn\_cd.activate\_topic\_ownership\) sys property is set to **Yes** and the topic is assigned to you or a group you belong to, you only see topics assigned to you or topics that do not have restrictions. For more information, see [Properties installed with Content Experiences](../reference/properties-installed-with-content-auto.md) and [Assign ownership of content](ecpro-ca-cd-content-restriction.md).

 Ownership of a topic includes:

-   Ability to restrict what groups or users can schedule content for publication.
-   Ability to edit content assigned to the topic.
-   Ability to preview content for the topic.
**Note:** Other users that have access to the content can view the content scheduled to the restricted topic, but cannot remove the topic from the schedule.

 For more information, see [Content Ownership](../concept/ecpro-content-restriction.md).

</td></tr><tr><td colspan="2">

Who

</td></tr><tr><td>

Add audience \(at least one\)

</td><td>

Who you want to see the content. For more information, see [Audiences](../concept/ecpro-audience.md).**Note:** You do not have the option of scheduling content for individual users. You can only schedule content for an audience. To schedule content for individual users, see [Scheduling the delivery of content](ecpro-schedule-content.md).

</td></tr><tr><td colspan="2">

WHEN

</td></tr><tr><td>

Always active

</td><td>

Content appears indefinitely until you replace or take it down.

</td></tr><tr><td>

Active for a specific duration

</td><td>

Content appears for a specific date and time range.

</td></tr><tr><td>

Inactive

</td><td>

Content is available for use, but does not appear on the Employee Center.

</td></tr></tbody>
</table>7.  Select **Save publish plan**.

    After you create a publish plan, the **Preview on portal** button appears in the **Publish** tab, which redirects you to view how the content will appear on the employee portal once published.

    Once rich or portal content is published, you must checkout the content to edit it. See [Checkout published content](ec-checkout-published-content.md).



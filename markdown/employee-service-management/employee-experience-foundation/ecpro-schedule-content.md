---
title: Scheduling the delivery of content
description: After you create content in Content Publishing, use Schedule Content to post to your Employee Center, in a campaign, To-dos, email notifications, and community.
locale: en-US
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 8
breadcrumb: [Publishing content, Creating employee communications, Authoring and managing employee communications, Employee Center Pro, Unified Employee Experience, Employee Service Management]
---

# Scheduling the delivery of content

After you create content in Content Publishing, use **Schedule Content** to post to your Employee Center, in a campaign, To-dos, email notifications, and community.

## Before you begin

Role required: sn\_cd.content\_manager

You can also schedule content after creating and saving it from the related list of the content. See the following:

-   [Configure mobile content](ecpro-content-delivery-mobile.md)
-   [Portal content](../concept/ec-streamline-content.md)
-   [Create email, SMS, or push notification content](ecpro-manage-notification-content.md)
-   [Create to-do content](ecpro-manage-content-to-do.md)
-   [Add or modify forum content](ecpro-manage-community-content.md)
-   [Add or modify links to other content sources](ecpro-manage-link-content.md)
-   [Add or modify block content](ecpro-manage-block-content.md)

**Note:** Ensure you schedule the portal content when you are adding a link content to a banner or styled content. The to-do content is automatically scheduled separately when the link content is scheduled. For more information, see [Creating to-do content](../concept/ecpro-content-to-dos.md).

## Procedure

1.  Navigate to **All** &gt; **Content Publishing** &gt; **Schedule Content**.

2.  Select the content you want to schedule.

3.  Complete the form.

<table id="table_zgt_fzg_wfb"><thead><tr><th>

Field

</th><th>

Description

</th><th>

 

</th></tr></thead><tbody><tr><td>

Content

</td><td>

The content or information you want to make available to employees.Select content from the list or **New** to create content.

 When scheduling content you want to appear as a link for to-do content in a banner or styled content, ensure you select the portal content you created. Do not schedule the to-do content, it automatically schedules with the portal content. For more information, see [Creating to-do content](../concept/ecpro-content-to-dos.md).

**Note:** You cannot schedule Link Content and Block Content as standalone content because it is reusable content.

</td><td>

 

</td></tr><tr><td>

Content Request Item

</td><td>

A unique number that identifies the content item associated with the content request. Content requests can be created from the Employee Center by employees or from the Content Request form by content managers or admins.

 For more information, see [Edit a content request item](../concept/ec-content-gov-request.md#).

</td><td>

 

</td></tr><tr><td>

Title

</td><td>

A descriptive name for the schedule content record. By default, the name of your content appears here after you select your content in the **Content** field.

</td><td>

 

</td></tr><tr><td>

Active

</td><td>

Indicates that the schedule for content is active and available to employees.

</td><td>

 

</td></tr><tr><td>

Add Users

</td><td>

Indicates you want to add specific users to view your content. Selecting this removes the audience you selected.**Note:** To schedule content, the default is to select an audience. When you select this field, you can only select individual users and you cannot select an audience.

</td><td>

 

</td></tr><tr><td>

Users

</td><td>

Users you want to view the content you are scheduling. Select the Unlock Users icon to search and add users.

**Note:** This field only appears when you select **Add Users**.

</td><td>

 

</td></tr><tr><td>

Audience

</td><td>

Who you want to see the content.See [Audiences](../concept/ecpro-audience.md).

 Does not show for Community Content.

</td><td>

 

</td></tr><tr><td>

Approvers

</td><td>

Who you want to approve the content before it is available.Only users with the Content Approver \[sn\_ca.content\_approver\] role appear after clicking the Lookup user list icon.

 After adding approvers, click **Update** or **Save**.

 You can send email notifications to approvers requesting their approval. See [Notifications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/notifications.md) and [Email templates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/c_EmailTemplates.md).

**Note:** If **Yes** is the value in the **sn\_cd.all\_must\_approve** Content Delivery property, all approvers must approve before campaign publication. If **No** is the value, you only need one approver.

</td><td>

 

</td></tr><tr><td>

When to process

</td><td>

The date and time you want your content to be sent, created, or posted.**Note:** This field only appears when you schedule to-do or notification content.

</td><td>

 

</td></tr><tr><td>

Due date

</td><td>

The date and time you want your users to complete the to-do or notification content.**Note:** This field only displays when you schedule to-do content.

</td><td>

 

</td></tr><tr><td>

Content status

</td><td>

The status of your to-do content.-   Pending: The Content Publishing scheduled jobs have not processed the content.
-   Scheduled: Content is scheduled and is queued to be processed.
-   Max Exceeded: The scheduled content exceeded the allowable time. The maximum value is configured in the sn\_cd.todo.max\_run\_time property under Content Publishing/Configurations/Properties.
-   Error: An error scheduling or posting community content occurred.


</td><td>

 

</td></tr><tr><td>

Completed on

</td><td>

The date and time the Content Publishing: Create To-dos scheduled job completed.

</td><td>

 

</td></tr><tr><td>

Availability start date

</td><td>

You can optionally restrict when content is available by start date. The date the content is first available to the audience.Does not show for Community Content.

</td><td>

 

</td></tr><tr><td>

Availability end date

</td><td>

You can optionally restrict when content is available by end date. The date the content is no longer available to the audience.Does not show for Community Content.

</td><td>

 

</td></tr><tr><td>

Location

</td><td>

Where the content you are scheduling appears. Your choices are:-   Service Portal
-   Workspace
 The fields change depending on what you select in this field because you are selecting where you want your content to appear.

</td><td>

 

</td></tr><tr><td>

 

</td><td>

The following fields appear when **Service Portal** is selected from the **Content location** field. For more information, see [Portal content](../concept/ec-streamline-content.md).

</td><td>

 

</td></tr><tr><td>

 

</td><td>

Page

</td><td>

The page on your Service Portal you want the content to appear. Select a page and only the widget instances that appear on the page are available in the **Widget instance** choice list.

 You can open the Page record and select the **Try It** button to view the page.

 Only appears when **Service Portal** is selected from **Content location**.

 **Note:** If you schedule Styled or Banner content to the Content Experiences widget on the emp\_taxonomy\_topic page, the original topic banner image does not display for the topics on the schedule.

</td></tr><tr><td>

 

</td><td>

Widget

</td><td>

The Employee Center widget instance. A widget instance is a reference to a widget that contains properties and CSS specific to that instance.A list of filtered widget instances appear when you select a page from the **Page** choice list.

 Only appears when **Service Portal** is selected from **Content location**.

 **Note:** If you schedule Styled or Banner content to the Content Experiences widget on the emp\_taxonomy\_topic page, the original topic banner image does not display for the topics on the schedule.

</td></tr><tr><td>

 

</td><td>

Taxonomy

</td><td>

Filters what topics you can schedule your content to. Taxonomy is a collection of hierarchical topics that brings together different content types, like requests, articles, quick links, and employee communications. For example, you can set up separate taxonomies for HR and IT so you can group specific topics under each.

 For this field to appear, select a page that has Taxonomy \(sn\_ex\_sp\_taxonomy\) entered in the Choices tab for the dictionary entry for the Category table of the page. For more information, see [Create a table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/table-administration-and-data-management/t_CreateATable.md).

 For more information on taxonomy for the Employee Center, see [Unified Taxonomy for Employee Center](../concept/config-taxonomy.md).

 For child topics to appear on your Employee Center, you must add it to the Portal form under Service Portal. For more information, see [Create a portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/service-portal/create-a-portal.md).

</td></tr><tr><td>

 

</td><td>

Topic

</td><td>

The topics you want your content to appear in under a taxonomy. For more information, see [Create and associate topics](create-topics-for-taxonomy.md).

</td></tr><tr><td>

 

</td><td>

The following fields appear when **Community Content** is the content type for content selected. For more information, see [Community content types](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/communities/c_communities-content-types.md).

</td><td>

 

</td></tr><tr><td>

 

</td><td>

Forum

</td><td>

The forum you want to post the community content.For more information on forums, see [Create a forum](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/communities/create-forum.md).

</td></tr><tr><td>

 

</td><td>

Topics

</td><td>

The area of interest that users can discuss.Click to select a topic that is within the forum.

 For more information on topics, see [Create a topic](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/communities/create-topic.md).

</td></tr><tr><td>

 

</td><td>

The following fields appear when **Workspace** is selected from the **Content location** field:

</td><td>

 

</td></tr><tr><td>

 

</td><td>

Content identifier

</td><td>

Associates portal content to widgets in Agent Workspace custom landing pages.**Note:** Currently, only HR Service Delivery Agent Workspace has base system components that shows content for Content Publishing. This field only appears when you select **Workspace** from the **Content location** field.

 When the custom landing page of Agent Workspace renders, the following components search for scheduled content that matches the content identifier, applies to the current user, and current time:

-   Announcements
-   Quick Links
-   My frequently used apps

**Note:** The base system provides these components, but the labels can be changed.

To find content identifiers for the base system provided workspace landing pages, see Create a custom landing page in UI Builder.

**Note:** For more information, see Setting up landing pages in a workspace.

</td></tr></tbody>
</table>4.  Select **Submit** or **Update**.

    You can also select **Publish with Approval** when a content request and content request item have been approved by the content requester. For more information, see [Add or remove content approvers](../concept/ec-content-gov-approval.md).



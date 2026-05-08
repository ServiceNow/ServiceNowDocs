---
title: Create content for a campaign
description: There are different places you can create content. You can create content from a campaign, bundle/stage, or directly from Manage Content under Content Experiences.
locale: en-US
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Creating campaigns, Authoring and managing employee communications, Employee Center Pro, Unified Employee Experience, Employee Service Management]
---

# Create content for a campaign

There are different places you can create content. You can create content from a campaign, bundle/stage, or directly from **Manage Content** under Content Experiences.

## Before you begin

Role required: sn\_ca.campaign\_manager, sn\_cd.content\_admin

## Procedure

1.  Navigate to **All** &gt; **Content Experiences** &gt; **Configurations** &gt; **Campaign Content**.

    You can also create content from:

    -   The **Campaign Content** related list of a campaign
    -   Select **Create new** from the content library column after selecting the ![Choice list icon](../images/choice-list-icon.png). For more information, see [Add content to a campaign using Content Experience Builder](ecpro-campaigns-manage-content-builder.md).
<table id="table_ujg_jcz_2mb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Title

</td><td>

The title you entered from the **To-do content** form.This field only appears when you select content that has a content type of:

-   Button Complete
-   E-Signature
-   Play Video
-   View Link
These are all to-do types of content that request the user to complete a task.

**Note:** For more information, see [Creating employee communications](../concept/ec-publish-content.md).

</td></tr><tr><td>

Content

</td><td>

The content you want to appear in your campaign.Select the **Lookup using list** icon and select the content from the list. The content you want to select must already be created before you can add it to a campaign.

**Note:** For more information, see [Creating employee communications](../concept/ec-publish-content.md).

</td></tr><tr><td>

Due date

</td><td>

Assigns a date when an employee must complete the to-do. Adding a due date allows you to sent a to-do and override the campaign bundle or stage end date.

**Note:** Only appears for content that has a to-do content type.

</td></tr><tr><td>

Page

</td><td>

Filters widget instances for the page you select.Select a page and only the widget instances that appear on the page are available in the **Widget instance** choice list.

 You can open the Page record and select the **Try It** button to view the page.

 **Note:** Only appears when **Portal Content** or **Styled content** is the content type for content selected.

</td></tr><tr><td>

Widget instance

</td><td>

The Employee Center widget instance. A widget instance is a reference to a widget that contains properties and CSS specific to that instance.A list of filtered widget instances appear when you select a page from the **Page** choice list.

 **Note:** Only appears when **Portal Content** or **Styled content** is the content type for content selected.

</td></tr><tr><td>

Taxonomy

</td><td>

Filters what topics you can schedule your content to. Taxonomy is a collection of hierarchical topics that brings together different content types, like requests, articles, quick links, and employee communications. For example, you can set up separate taxonomies for HR and IT so you can group specific topics under each.

 For this field to appear, select a page that has Taxonomy \(sn\_ex\_sp\_taxonomy\) entered in the Choices tab for the dictionary entry for the Category table of the page. For more information, see Create a table.

 For more information on taxonomy for the Employee Center, see [Unified Taxonomy for Employee Center](../concept/config-taxonomy.md).

 For child topics to appear on your Employee Center, you must add it to the Portal form under Service Portal. For more information, see Create a portal.

</td></tr><tr><td>

Topic

</td><td>

The topics you want your content to appear in under a taxonomy.Only topics that are associated with a specific page/template display. When the Allow Ownership for Topics \(sn\_cd.activate\_topic\_ownership\) sys property is set to **Yes**, topic ownership is enabled. For more information, see [Properties installed with Content Publishing](../reference/properties-with-content-delivery.md).

 Ownership of a topic includes:

-   Ability to restrict what groups or users can schedule content for publication.
-   Ability to edit content assigned to the topic.
-   Ability to preview content for the topic.
**Note:** Other users that have access to the content can view the restricted content assigned to a topic, but cannot edit or delete the topic.

 For more information, see [Content Ownership](../concept/ecpro-content-restriction.md) and [Create and associate topics](create-topics-for-taxonomy.md).

</td></tr><tr><td>

End campaign on completion

</td><td>

Removes employees from the campaign after the to-do is completed.

</td></tr><tr><td>

Active

</td><td>

Indicates the to-do content is active and available to use.

</td></tr><tr><td>

Campaign bundle

</td><td>

The campaign bundle or stage you want the content to belong to.

</td></tr><tr><td>

Refine audience

</td><td>

Narrows your audience selected at the campaign level.Selecting an existing audience creates a subset of the original audience.

</td></tr><tr><td>

Description

</td><td>

Description of the to-do content.

</td></tr></tbody>
</table>    ![Campaign content - New](../images/campaign-content-new.png)

2.  Click **New**.

    ![Campaign Content - New](../images/campaign-content-2.png)

3.  Select the **Lookup using list** ![Lookup using list icon](../../human-resources/image/magnify-glass-outline-icon.png) icon next to Content.

    ![Campaign Content](../images/campaign-content-type.png)

4.  Select existing content or **New**.

    ![Campaign Content Type select](../images/campaign-content-type-select.png)

5.  Select the content type.

<table id="table_fgf_s5m_tkb"><thead><tr><th>

Content type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Mobile Content

</td><td>

Announcement banners you can send to your employee's mobile devices. The banner can be an image that links to content of your Employee Center or Service Portal.**Note:** For information on creating mobile content, see [Configure mobile content](ecpro-content-delivery-mobile.md).

</td></tr><tr><td>

Notification Content

</td><td>

Information blast you send directly to your employees via email or push to their mobile devices.**Note:** For information on creating notification content, see [Create email, SMS, or push notification content](ecpro-manage-notification-content.md).

</td></tr><tr><td>

Portal Content

</td><td>

Content that appears on your Employee Center or Service Portal.**Note:** For information on creating portal content, see [Portal content](../concept/ec-streamline-content.md).

</td></tr><tr><td>

To-do Content

</td><td>

Content that assigns tasks to your employees and can be sent via email, SMS, or posted to your Employee Center or Service Portal.**Note:** For information on creating to-do content, see [Create to-do content](ecpro-manage-content-to-do.md).

</td></tr></tbody>
</table>6.  Click **Submit**.

7.  Right-click the form header and select **Save** to remain on the form.

8.  Or, click **Submit** or Update and return to the list.


## What to do next

Since you attached your content to a bundle or stage, you can launch your campaign by clicking **Publish** from the campaign. Publish only appears when at least one bundle with content is attached to the campaign, and the campaign has a title and a start time. Publishing activates all content for a selected audience and duration.

After the **Content Experiences: Update Campaign Audience** schedule job runs, the **Campaign Targets** tab shows specific employees that are part of the refined audience for the campaign content.

Click **Edit Campaign** to pause the campaign and make edits to the content, audience, or duration.

Click **Cancel Campaign** to de-activate all undelivered content \(including notifications\) to a scheduled audience. You cannot reverse this step. Canceling a campaign that has already launched de-activates all undelivered content and you cannot restart it.

Click **Deactivate Content** to remove the content from a campaign. The content does not appear for users who have not yet viewed it.


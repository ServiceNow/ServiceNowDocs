---
title: Creating campaigns with Content Experiences
description: Campaigns offer a powerful content publishing tool that provides organizations with the ability to efficiently deliver targeted information to their employees. As a content manager, you can configure multiple channels to ensure content reaches the intended audience at the optimal time.
locale: en-US
release: xanadu
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 8
keywords: [campaign, campaigns, employee center campaign, servicenow campaign, servicenow campaigns]
breadcrumb: [Manage, Employee Center, Employee Service Management]
---

# Creating campaigns with Content Experiences

Campaigns offer a powerful content publishing tool that provides organizations with the ability to efficiently deliver targeted information to their employees. As a content manager, you can configure multiple channels to ensure content reaches the intended audience at the optimal time.

Here are a few examples of what you can accomplish through the targeted messaging of campaigns:

-   Deflect: Prevent your employees from creating more inquiry cases.
-   Drive action: Encourage your employees to sign up for health benefits.
-   Provide communication: Ensure that your employees know about a specific subject.

**Note:** Campaigns are intended for internal communications only. Please do not use campaigns for customer marketing, as doing so could potentially lead to the NOW mailsystem being flagged as spam by email reputation systems.

## Example campaigns

Content Experiences includes demo campaigns to help you better understand campaign structuring, explore examples of bundle trigger configurations, and discover various use cases. To access the demo campaigns, navigate to **All** &gt; **Content Experiences** &gt; **Content Experience Builder**.

**Note:** The admin must select **Load demo data** during the installation or upgrade of the Content Experiences plugin. If the demo data does not appear in your instance, ask your admin to install the demo data.

## Campaign components

When planning a campaign, consider the following components:

-   **Who: Audiences**

    Target different content to different audiences. You can have a campaign deliver one set of content to managers and another set to direct reports.

-   **When: Trigger**

    Content becomes available to employees based on the configured trigger. Content can be made available based on a fixed or dynamic date range, when a condition is met, or a system event occurs.

-   **Where: Location**

    Target content to specific pages, topics, and widgets to ensure the content reaches the intended audience.

-   **What: Information that you want to communicate**

    Define the information, links, videos, SMS messages, and emails that you want to communicate to your employees.


## Campaign structure

A campaign consists of a hierarchy of stages, where each stage contains content.

**Note:** Some parts of the interface use the term "bundles" to refer to stages.

Here's an example of how to structure a company benefits open enrollment campaign, consisting of three stages:

1.  Get ready for Open Enrollment: This stage delivers content before the open enrollment period to prepare employees.
2.  Open enrollment is here: This stage delivers content during the open enrollment period to provide the necessary information on employee benefits.
3.  Open enrollment ends soon: In this stage, reminders are sent during the final week of the open enrollment period.

Each campaign stage includes content that will be visible on the employee portal and distributed via email. ![Chart showing campaign structure.](../images/campaign.jpg)

## Setting up a campaign

Set up a campaign using one of the following methods:

-   [Content Experience Builder](ecpro-campaigns.md#section-campaign-builder)
-   [Legacy \(records and forms\)](ecpro-campaigns.md#section-lists-forms)

## Content Experience Builder

With the Content Experience Builder, you can complete the entire workflow of configuring a campaign within a single interface.

1.  [Create content in the Content library](ec-streamline-content.md)

    You can create a variety of content types that can be delivered via the employee portal, email, SMS, or push notification.

    **Note:** News articles are not yet supported.

2.  [Create a campaign](../task/ecpro-create-campaign.md)

    Create a campaign to define the audience, content approvers, and start and end dates.

3.  [Create campaign stages with Content Experience Builder](../task/ecpro-campaign-builder.md)

    Add stages to your campaign to define what content users will see and when they will see it. You can also use stages to further refine the audience. For example, you can create one stage to hold content for managers and another stage to hold content for direct reports.

4.  [Add content to a campaign using Content Experience Builder](../task/ecpro-campaigns-manage-content-builder.md)

    You can add content from the Content library and create a variety of content types in the Content Experience Builder.

    **Note:** If you are creating a campaign that contains rich content, you must create the rich content in the Content Library Rich Content Editor, since the Content Experience Builder does not currently support rich content creation. See [Rich Content Editor](ec-rich-content.md)

5.  [Preview the campaign](ecpro-campaign-preview.md)

    See how your campaign will appear to your audience before publishing.

6.  Publish the campaign from the Content Experience Builder.
7.  [Analyze the effectiveness of the campaign](ecpro-content-automation-reevaluate-audience.md)

    Verify that your campaign is targeting the correct audience. Create goals to see if your campaign is driving action from your employees, or reducing activity such as the number of inquiry cases coming in. Continually evaluate your campaign as it progresses.


## Legacy \(records and forms\)

If you prefer to create campaigns using records and forms, or if you are publishing to a custom widget, follow these steps:

1.  [Create content in the Content library](ec-streamline-content.md)

    You can create a variety of content types that can be delivered via the employee portal, email, SMS, or push notification.

2.  [Create a campaign](../task/ecpro-manage-campaigns.md)

    Create a campaign to define the audience, content approvers, and start and end dates.

3.  [Create a campaign stage](../task/ecpro-manage-campaign-bundles.md)

    Add stages to your campaign to define what content users will see and when they will see it. You can also use stages to further refine the audience. For example, you can create one stage to hold content for managers and another stage to hold content for direct reports.

4.  [Preview the campaign](ecpro-campaign-preview.md)

    See how your campaign will appear to your audience before publishing.

5.  Publish the campaign
6.  [Analyze the effectiveness of the campaign](ecpro-content-automation-reevaluate-audience.md)

    Verify that your campaign is targeting the correct audience. Create goals to see if your campaign is driving action from your employees, or reducing activity such as the number of inquiry cases coming in. Continually evaluate your campaign as it progresses.


-   **[Create a campaign](../task/ecpro-create-campaign.md)**  
Create a campaign to push communications and important information to your employees.
-   **[Campaign bundle triggers](../reference/ecpro-triggers.md)**  
Define a trigger to make the content in the campaign stage available to employees.
-   **[Add content to a campaign using Content Experience Builder](../task/ecpro-campaigns-manage-content-builder.md)**  
Create or place content into a bundle or stage for a campaign using Content Experience Builder. The Content library holds existing content and is organized by content type.
-   **[Campaign preview](ecpro-campaign-preview.md)**  
When creating a campaign, you can preview the content prior to publishing it.
-   **[Analyzing your campaign for effectiveness](ecpro-content-automation-reevaluate-audience.md)**  
Analyze your campaign to ensure that your messaging is effective and that you are targeting the correct audience when you use campaign success goals. You can also check your campaign's progress and evaluate how successful your campaign is.
-   **[Create a campaign](../task/ecpro-manage-campaigns.md)**  
Create a campaign to push communications and important information to your employees.
-   **[Create content for a campaign](../task/ecpro-manage-content.md)**  
There are different places you can create content. You can create content from a campaign, bundle/stage, or directly from **Manage Content** under Content Experiences.
-   **[Create campaign bundles/stages](../task/ecpro-manage-campaign-bundles.md)**  
Use campaign stages to group your campaign content within a campaign. This process allows you to determine when the content is available to your employees and for how long.
-   **[Editing a published campaign](../task/ecpro-edit-campaign.md)**  
If you need to make changes to a published campaign, review this information to understand your options. Editing a campaign pauses the campaign; any content that is not yet available is suspended until the campaign is published again. The campaign, campaign bundles, and campaign content are editable.

**Parent Topic:**[Managing Employee Center](manage-emp-center.md)

**Related topics**  


[Action framework](action-framework.md)

[Managing content requests with Content Governance](ec-content-governance.md)

[Creating employee communications with Content Publishing](ec-publish-content.md)

[Content management on topic pages](cm-ec-manage.md)

[Integrated service and experience feedback management](ex-fdbck-manage.md)

[Improve portal performance](improve-manage.md)


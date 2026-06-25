---
title: Creating employee communications
description: Content Publishing offers robust communications creation tools that enable you to create, manage, and publish a variety of content types including portal content, notifications, mobile content, and tasks.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/employee-experience-foundation/ec-publish-content.html
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 13
breadcrumb: [Authoring and managing employee communications, Employee Center Pro, Unified Employee Experience, Employee Service Management]
---

# Creating employee communications

Content Publishing offers robust communications creation tools that enable you to create, manage, and publish a variety of content types including portal content, notifications, mobile content, and tasks.

## Overview of creating communications

To create employee communications using Content Publishing, follow the process shown in this infographic.

\[Omitted image "employee-comms-process.jpg"\] Alt text: filler text

1.  Select the platform

    When creating a new piece of content, the first step is to select a platform. This determines where your content appears and narrows your selection of content formats.

2.  Choose a content format

    After selecting the platform for your content, select from the available content formats.

3.  Create a content record

    Fill in the fields in the New content form to provide details such as content item name and order.

4.  Prepare the content

    Do the steps applicable to the content format, such as upload the image or video, assemble the banner or news article, or provide the URL.

5.  Translate your content

    Request a language translation for the content you are creating. For more information, see [Multilingual support in the Content Library](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/ec-switch-language.md).

6.  Configure publishing

    Configure publishing to control when the content becomes available, who can see it, and for how long. See [Publishing content](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/ec-content-publishing-schedule.md).

    Alternatively, you can build out a more robust publishing configuration using [Creating campaigns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/ecpro-campaigns.md)


-   Create various employee communications portal content including news articles, rich content microsites, announcements, banners, links to other content, and calendar events.
-   Leverage easy-to-use drag-and-drop, visual interfaces for creating, editing and previewing content before it's published.
-   Create notifications such as a mass email or short message service \(SMS\) to your employees.
-   Add urgency to your communications by creating and scheduling to-dos in the form of tasks.
-   Schedule and target your content to specific audiences with the option of making it available from specific start and end dates.
-   Deliver announcements and links to content on your employee's mobile devices.

Content Library allows you to manage your content within a single, unified interface and flow.

-   Design your content with easy-to-use, no code configurations.
-   Preview your content as you are creating it and preview how it looks on your portal.
-   Assign your audience and schedule your content for sending/viewing immediately or within a date window.

**Note:** The end-to-end Content Library workflow supports only news, rich, and portal content. For all other content types, you can create new content in the Content Library, but you will need to use the Schedule form to deliver it to employees.

To publish content to the Workspace or UIB Workspace, you must use the Schedule content form, as the Content Library does not offer the option to publish to the Workspace or UIB Workspace.

For more information on Publishing content, see [Publishing content](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/ec-content-publishing-schedule.md).

## Creating and publishing content

Create and publish content in the Content Library using the following process:

-   **1. Select the Platform**

    When creating a new piece of content, the first step is to select a platform. This determines where your content appears and narrows your selection of content formats.

    \[Omitted image "ec-content-library1.png"\] Alt text: Content Library - select platform

-   **2. Choose a content format**

    After selecting the platform for your content, select from the available content formats.

    \[Omitted image "ec-content-library2.png"\] Alt text: Content library - select content format

-   **3. Create a content record**

    Fill in the fields in the New content form to provide details such as content name and order.

    **Note:** Since there is no direct method for migrating content records between ServiceNow® environments, we recommend you create content in your production environment and use the **Active** option and publish plans to control content availability.

    \[Omitted image "ec-content-library3.png"\] Alt text: Content library - select content record

-   **4. Prepare the content**

    Do the steps applicable to the content format, such as upload the image or video, assemble the banner or news article, or provide the URL.

    \[Omitted image "ec-content-library4.png"\] Alt text: content library - create content

-   **\(Optional\) 5. Translate your content**

    Select a different language to view your session in or request a language translation for the content you are creating. For more information, see [Configuring translation for Content Publishing after upgrade](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/ec-multiple-language-support.md).

    **Note:** Only translate content you are done creating and formatting the content. For best results, we do not recommend that you add or remove components or change the formatting after translation.

    For rich content that is formatted differently in different languages, duplicate the content and modify the formatting as needed. Then, use Audiences to target the content to users by language. See [Audiences](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/ecpro-audience.md)

-   **6. Configure publishing**

    Add one or more publish plans to determine when the content becomes available, who can see it, and for how long. See [Create a publish plan for your content](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/ec-content-library-publish2.md).

    Alternatively, you can build out a more robust publishing configuration using [Creating campaigns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/ecpro-campaigns.md)

    \[Omitted image "ec-content-library6.png"\] Alt text: Content library - configure publishing


## Supported platforms and content formats

-   **Articles and Pages**
    -   [Rich content](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/ec-rich-content.md): Provides the ability to create and schedule long form content using a drag-and-drop method without the knowledge of coding. Rich content helps you to easily and visually create high quality curated content that matches the Service Portal look and feel with limited technical knowledge. You can target Rich content to any Portal page.
    -   [News articles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/ec-news-articles.md): Combines content creation features from the Rich Content Editor with new publishing methods that enable high volume content publishing to keep employees updated on company news and announcements.
-   **Portal**

    Reach more people in your organization with greater effectiveness and efficiency by creating meaningful content that can be distributed through multiple channels with Content Experiences and Content Publishing. You can create different types of content that includes:

    -   [Styled content](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/ec-content-library-portal-styled.md): Allows you access to a suite of tools and fields to create custom banners, block, or video content. Styled content is fast and easy to use without having to use HTML/CSS code. For banners you can use features that define your text color, text alignment, add buttons or links, background color, background image, and change the gradient of the image.
    -   [Video](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/ec-content-library-portal-video.md): Place videos into your Employee Center or Employee Center Pro.

        **Note:** Use styled content for videos if you want to add heading and body text, reference variables from either the User or HR profile table, and other features that contribute to the over-all style of your video.

    -   [URL](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/ec-content-library-portal-url.md): Links that take your employees to content.
    -   [Image-based link](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/ec-content-library-portal-image.md): Links to content that are also an image.
    -   [Events](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/ec-content-library-portal-events.md): Content for company events that have a specific start and end date and time.
    -   [Banner](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/ec-content-library-portal-banner.md): Attention grabbing banners that promote a message or content to your employees.
    -   [Rich text](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/ec-content-library-portal-richtext.md): Use rich text to enhance your content or message using common formatting options like bold or italics.
    -   [Calendar](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/ec-content-library-portal-calendar.md): Provides your employees with a quick way of viewing scheduled events
-   **[Mobile content](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/ec-mobile-content.md)**

    Create different types of content that your employees can view on their mobile devices. The type of mobile content you can create are:

    -   Mobile Banner: A banner that captures attention for a mobile device.
    -   Mobile Text Card: Content for a mobile device that includes a heading text and link to content.
    -   Mobile Video: Video that can be accessed from a mobile device.
-   **[Notification content](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/ec-notification-content.md)**

    Send content directly to your employees as a notification. The types of notifications are:

    -   Email: Notifications sent to your employees via email.
    -   Push: Notifications sent to your employees via the Now Mobile app.
    -   SMS Text: When utilizing the ServiceNow Notify product, a content type is available allowing you to send SMS text message notifications to your employees.

        **Note:** Requires configuration of your Notify set up. For more information, see

        -   [Notify](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/notify-landing-page.md)
        -   [Enable SMS delivery with the email client](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/r_EnableTheSMSDeliveryOption.md)
        -   [Configuring Employee Center for mobile](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/ec-mobile-configrations.md)
    -   Microsoft Teams: Notifications sent to your employees via Microsoft Teams. This requires the ServiceNow for Microsoft Teams integration. See [Sending notifications to employees using Microsoft Teams](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/using-campaigns-ms-teams-mt.md).
-   **[To-do content](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/ec-to-do-content.md)**

    Create content that prompts your employees to complete an assigned task. To-dos are:

    -   Button Complete: A button that prompts your employees to push when they complete a to-do.
    -   E-Signature: Prompts an employee to sign a document to complete the to-do.
    -   Play Video: Provides a video that after viewing completes the to-do.
    -   View Link: Provides a link to content that after accessing completes the to-do.
-   **[Pulse survey content](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/ec-pulse-content.md)**

    To receive feedback from your employees, create and send Pulse surveys that can drive action and measure impact.

-   **[Employee Forums](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/ecpro-employee-forum.md)**

    Employee Forums help your employees connect, engage, and collaborate with other employees. Use Employee Forums to share business information, promote employee engagement, encourage ideas and feedback, and to give your employees a voice.

    When activating the ServiceNow Communities product to enable Employee Forums, customers can deliver information within Content Publishing including:

    -   Blog: Create long-form text articles for posting in a forum or topic.
    -   Video: Add a video to a forum or topic.
    -   Event: Create event-related information items to post in a forum or topic.
    **Note:** For more information, see [Communities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/servicenow-communities.md).


|Feature|Description|
|-------|-----------|
|[Portal content](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/ec-streamline-content.md)|Content managers use the Content Library as a one-stop location for creating and publishing content for employees in various content formats and publishing platforms.|
|[Publishing content](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/ec-content-publishing-schedule.md)|Content managers either create a publish plan or schedule content \(depending on the content type\) to deliver content to employees.|

Content Publishing allows you to create information from different areas:

-   Content Library
    -   Create content, links, tasks, notifications, mobile, surveys, and social media messages to customize and enhance what you make available to your employees.
    -   Preview the information as you create it, assign an audience, and schedule and publish it from the same page.
-   Content Categories: Use the lists and forms UI to create surveys, portal content, notifications, mobile, social media, and tasks.
-   Reusable Components: Customers can also use the lists and forms UI to create standard information that can be created once and used in different area like links, block content, SMS configuration, and audiences.
-   Schedule: After creating the information for your employees, you can determine how it will be communicated, where on your portal it should reside, the audience your information is directed to, who should approve \(if applicable\), and start and end dates and times the information should be available.
-   Organization Chart:
-   Advanced:
    -   Existing customers can create content types to associate the category and widget you want your content to reside.
    -   View a list of tasks assigned to your employees.
    -   Set additional settings such as approvals, content ownership, and more.
-   Demo Portal: Use the Demo Portal to quickly view how the information you created looks before you schedule and publish it.

    **Note:** For some content, you can use the Content Library to view your information as you create and schedule it for publication when it looks the way you want it.


## Platforms and content formats

Select a tile to learn about the available platforms and content formats, and to get started with creating employee communications.

<table id="table_iwv_lpv_klb" class="nav-card"><tbody><tr><td>

[Microsites \[Omitted image "bus-management-console.svg"\] Alt text: Assemble HTML-based rich content using a drag-and-drop interface.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/ec-rich-content.md)

</td><td>

[News articles \[Omitted image "bus-demand-management.svg"\] Alt text: Keep employees updated on company news and announcements.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/ec-news-articles.md)

</td><td>

[Company events \[Omitted image "bus-events.svg"\] Alt text: Host live company events in the employee portal.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/ec-company-events.md)

</td></tr><tr><td>

[Portal \[Omitted image "bus-agent-workspace-1.svg"\] Alt text: Create portal content in a variety of formats including video, URL, banners, and events.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/ec-streamline-content.md)

</td><td>

[Notification \[Omitted image "bus-email.svg"\] Alt text: Create email, push, and SMS notifications to send messages directly to your employees.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/ec-notification-content.md)

</td><td>

[Mobile \[Omitted image "bus-ebook.svg"\] Alt text: Create content specifically for viewing on mobile devices.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/ec-mobile-content.md)

</td></tr><tr><td>

[To-do \[Omitted image "bus-automated-testing-framework.svg"\] Alt text: Create tasks that prompt employees to take action.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/ec-to-do-content.md)

</td><td>

[Pulse survey \[Omitted image "bus-gender-neutral-leader-c-suite.svg"\] Alt text: Send Pulse surveys to employees to obtain feedback.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/ec-pulse-content.md)

</td><td>

[Employee Forums \[Omitted image "bus-community.svg"\] Alt text: Create content that appears on employee forums.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/ecpro-employee-forum.md)

</td></tr><tr><td>

 

</td><td>

 

</td><td>

[Microsoft Teams \[Omitted image "bus-chat.svg"\] Alt text: Send messages on Microsoft Teams to drive employee action.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/using-campaigns-ms-teams-mt.md)

</td></tr></tbody>
</table>
---
title: Content Library
description: Content Library is your one-stop location for creating and publishing content for your employees in various content formats and publishing platforms.
locale: en-US
release: xanadu
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 8
keywords: [library, content library, servicenow library]
breadcrumb: [Creating employee communications with Content Publishing, Manage, Employee Center, Employee Service Management]
---

# Content Library

Content Library is your one-stop location for creating and publishing content for your employees in various content formats and publishing platforms.

Content Library allows you to manage your content within a single, unified interface and flow.

-   Design your content with easy-to-use, no code configurations.
-   Preview your content as you are creating it and preview how it looks on your portal.
-   Assign your audience and schedule your content for sending/viewing immediately or within a date window.

**Note:** The end-to-end Content Library workflow supports only news, rich, and portal content. For all other content types, you can create new content in the Content Library, but you will need to use the Schedule form to deliver it to employees. For more information on Publishing content, see [Publishing content](ec-content-publishing-schedule.md).

## Creating and publishing content

Create and publish content in the Content Library using the following process:

-   **1. Select the Platform**

    When creating a new piece of content, the first step is to select a platform. This determines where your content appears and narrows your selection of content formats.

    ![Content Library - select platform](../images/ec-content-library1.png)

-   **2. Choose a content format**

    After selecting the platform for your content, select from the available content formats.

    ![Content library - select content format](../images/ec-content-library2.png)

-   **3. Create a content record**

    Fill in the fields in the New content form to provide details such as content name and order.

    **Note:** Since there is no direct method for migrating content records between ServiceNow® environments, we recommend you create content in your production environment and use the **Active** option and publish plans to control content availability.

    ![Content library - select content record](../images/ec-content-library3.png)

-   **4. Prepare the content**

    Do the steps applicable to the content format, such as upload the image or video, assemble the banner or news article, or provide the URL.

    ![content library - create content](../images/ec-content-library4.png)

-   **\(Optional\) 5. Translate your content**

    Select a different language to view your session in or request a language translation for the content you are creating. For more information, see [Configuring translation for Content Publishing after upgrade](ec-multiple-language-support.md).

    **Note:** Only translate content you are done creating and formatting the content. For best results, we do not recommend that you add or remove components or change the formatting after translation.

    For rich content that is formatted differently in different languages, duplicate the content and modify the formatting as needed. Then, use Audiences to target the content to users by language. See [Audiences](ecpro-audience.md)

-   **6. Configure publishing**

    Add one or more publish plans to determine when the content becomes available, who can see it, and for how long. See [Create a publish plan for your content](../task/ec-content-library-publish2.md).

    Alternatively, you can build out a more robust publishing configuration using [Creating campaigns with Content Experiences](ecpro-campaigns.md)

    ![Content library - configure publishing](../images/ec-content-library6.png)


## Supported platforms and content formats

-   **Articles and Pages**
    -   [Rich content](ec-rich-content.md): Provides the ability to create and schedule long form content using a drag-and-drop method without the knowledge of coding. Rich content helps you to easily and visually create high quality curated content that matches the Service Portal look and feel with limited technical knowledge. You can target Rich content to any Portal page.
    -   [News articles](ec-news-articles.md): Combines content creation features from the Rich Content Editor with new publishing methods that enable high volume content publishing to keep employees updated on company news and announcements.
-   **Portal**

    Reach more people in your organization with greater effectiveness and efficiency by creating meaningful content that can be distributed through multiple channels with Content Experiences and Content Publishing. You can create different types of content that includes:

    -   [Styled content](../task/ec-content-library-portal-styled.md): Allows you access to a suite of tools and fields to create custom banners, block, or video content. Styled content is fast and easy to use without having to use HTML/CSS code. For banners you can use features that define your text color, text alignment, add buttons or links, background color, background image, and change the gradient of the image.
    -   [Video](../task/ec-content-library-portal-video.md): Place videos into your Employee Center or Employee Center Pro.

        **Note:** Use styled content for videos if you want to add heading and body text, reference variables from either the User or HR profile table, and other features that contribute to the over-all style of your video.

    -   [URL](../task/ec-content-library-portal-url.md): Links that take your employees to content.
    -   [Image-based link](../task/ec-content-library-portal-image.md): Links to content that are also an image.
    -   [Events](../task/ec-content-library-portal-events.md): Content for company events that have a specific start and end date and time.
    -   [Banner](../task/ec-content-library-portal-banner.md): Attention grabbing banners that promote a message or content to your employees.
    -   [Rich text](../task/ec-content-library-portal-richtext.md): Use rich text to enhance your content or message using common formatting options like bold or italics.
    -   [Calendar](../task/ec-content-library-portal-calendar.md#): Provides your employees with a quick way of viewing scheduled events
-   **[Mobile content](ec-mobile-content.md)**

    Create different types of content that your employees can view on their mobile devices. The type of mobile content you can create are:

    -   Mobile Banner: A banner that captures attention for a mobile device.
    -   Mobile Text Card: Content for a mobile device that includes a heading text and link to content.
    -   Mobile Video: Video that can be accessed from a mobile device.
-   **[Notification content](ec-notification-content.md)**

    Send content directly to your employees as a notification. The types of notifications are:

    -   Email: Notifications sent to your employees via email.
    -   Push: Notifications sent to your employees via the Now Mobile app.
    -   SMS Text: When utilizing the ServiceNow Notify product, a content type is available allowing you to send SMS text message notifications to your employees.

        **Note:** Requires configuration of your Notify set up. For more information, see

        -   [Notify](https://www.servicenow.com/docs/access?context=notify-landing-page&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)
        -   [Enable SMS delivery with the email client](https://www.servicenow.com/docs/access?context=r_EnableTheSMSDeliveryOption&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)
        -   [Configuring Employee Center for mobile](ec-mobile-configrations.md)
    -   Microsoft Teams: Notifications sent to your employees via Microsoft Teams. This requires the ServiceNow for Microsoft Teams integration. See [Sending notifications to employees using Microsoft Teams](../../sn-teams/concept/using-campaigns-ms-teams-mt.md).
-   **[To-do content](ec-to-do-content.md#)**

    Create content that prompts your employees to complete an assigned task. To-dos are:

    -   Button Complete: A button that prompts your employees to push when they complete a to-do.
    -   E-Signature: Prompts an employee to sign a document to complete the to-do.
    -   Play Video: Provides a video that after viewing completes the to-do.
    -   View Link: Provides a link to content that after accessing completes the to-do.
-   **[Pulse survey content](ec-pulse-content.md#)**

    To receive feedback from your employees, create and send Pulse surveys that can drive action and measure impact. For more information, see [Listening Posts](../../human-resources/concept/listening-posts-1.md).

-   **[Facebook Workplace content](ec-facebook-content.md#)**

    Create content for your company's integration with Facebook Workplace. For more information, see [Workplace from Facebook spoke](https://www.servicenow.com/docs/access?context=facebook-spoke&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US).

-   **[Employee Forums](ecpro-employee-forum.md#)**

    Employee Forums help your employees connect, engage, and collaborate with other employees. Use Employee Forums to share business information, promote employee engagement, encourage ideas and feedback, and to give your employees a voice.

    When activating the ServiceNow Communities product to enable Employee Forums, customers can deliver information within Content Publishing including:

    -   Blog: Create long-form text articles for posting in a forum or topic.
    -   Video: Add a video to a forum or topic.
    -   Event: Create event-related information items to post in a forum or topic.
    **Note:** For more information, see [Communities](https://www.servicenow.com/docs/access?context=servicenow-communities&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US).



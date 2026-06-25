---
title: Publishing content
description: Use Content Publishing to create, schedule, and deliver your portal content to your employees.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/employee-experience-foundation/ec-content-publishing-schedule.html
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Creating employee communications, Authoring and managing employee communications, Employee Center Pro, Unified Employee Experience, Employee Service Management]
---

# Publishing content

Use Content Publishing to create, schedule, and deliver your portal content to your employees.

## Options for publishing

Content publishing offers two options for publishing your content:

-   **[Publish plans via Content Library](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/ec-content-library-publish2.md)**

    Publish plans are integrated in the Content Library workflow and offer a robust configuration options, including where the content will appear, who will see it, and publishing duration. You can create a publish plan for news, rich, or portal content. For all other content types, you must use the Schedule content form.

    **Note:** To publish content to the Workspace or UIB Workspace, you must use the Schedule content form, as the Content Library does not offer the option to publish to the Workspace or UIB Workspace.

    \[Omitted image "ec-content-publishing.png"\] Alt text: Publish plan features

-   **[Schedule content form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/ecpro-schedule-content.md)**

    Configure content delivery for the following types of content using the Schedule content form:

    -   [Mobile content](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/ec-mobile-content.md)
    -   [Notification content](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/ec-notification-content.md)
    -   [To-do content](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/ec-to-do-content.md)
    -   [Pulse survey content](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/ec-pulse-content.md)
    -   [Employee Forums](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/ecpro-employee-forum.md)

## Publishing destinations

When you are configuring a content schedule or publish plan, you must define the publishing destination via three fields: Location, Page, and Widget.

-   **Location**

    For most content types, **Service Portal** is the only option. Some content types, such as news articles, enable you to specify a publish plan for the Now Mobile app. For more information, see [Publishing news articles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/ec-content-publish-news-articles.md).

-   **Page**

    The page field lists portal and taxonomy pages. To narrow the selection, you can first select a widget, then return to the page field, which only lists the pages that contain the widget.

    **Note:** If you select a taxonomy topic, the form prompts you to specify the taxonomy and one or more topics.

    Portal pages are managed in **Service Portal** &gt; **Pages**.

    Taxonomy topics are managed in **Taxonomy** &gt; **Topics**. See [Unified Taxonomy for Employee Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/config-taxonomy.md).

-   **Widget**

    The widgets field only lists supported widgets for that content type. For more information on the content types, see the table below.


## Where you can publish content

|Content type|Supported widgets|
|------------|-----------------|
|[Banner](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/ec-content-library-portal-banner.md)|Content Experiences|
|[Banner](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/ec-content-library-portal-banner.md)|Welcome Banner \(CD\)|
|[Calender](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/ec-content-library-portal-calendar.md)|Event Calender|
|[Event](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/ec-content-library-portal-events.md)|Upcoming Events \(CD\)|
|[Image-based link](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/ec-content-library-portal-image.md)|Quick Links \(CD\)|
|[News article](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/ec-news-articles.md)|News Feed|
|[News article](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/ec-news-articles.md)|Featured News|
|[Rich content](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/ec-rich-content.md)|Rich Content \(CD\)|
|[Rich text](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/ec-content-library-portal-richtext.md)|Announcements \(CD\)|
|[Styled content](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/ec-content-library-portal-styled.md)|Content Experiences|
|[Styled content](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/ec-content-library-portal-styled.md)|Styled Content \(CD\)|
|[URL](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/ec-content-library-portal-url.md)|Information Links \(CD\)|
|[Video](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/ec-content-library-portal-video.md)|Video Carousel \(CE\)|

To customize the content type and publishing widget, see [Add or modify content type for Content Publishing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/ecpro-manage-content-types.md)

Use Schedule Content, found under Content Publishing to define when you want your content to be available or delivered.

Schedule content includes setting:

-   Dates: The start and end dates that your content is available.
-   Location: Where your content appears \(Service Portal or Workspace\).
-   Page: The page your content appears on the Service Portal.
-   Widget instance: The widget on the page your content appears.
-   Audiences: Who the content is for.
-   Taxonomy: Groups common topics.
-   Topic: Topic heading that your content appears under.

You can also schedule content to widgets within topic pages by selecting a taxonomy and multiple topics. Doing this helps to organize and provide content specific to a topic.

**Note:** For more information on topic pages, see [Dynamic topic pages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/dynamic-topic-page.md).

## Publishing schedule content

You can schedule your content to appear in Employee Center and Workspace. The Schedule content form changes depending on where you want your content to appear. To better understand scheduling content, the information on the form can be divided in the following way:

-   Meta data: Provides the basic information required to schedule your content and includes:
    -   Title: An identifiable name for your schedule content record. It defaults to the name of the content you are scheduling.
    -   Approvers: You can optionally reference names of people that are required to approve of the content before it can be scheduled for access.
    -   Active: You can schedule your content for access by date, but won't be available unless you activate the schedule content record.
    -   State: The current state of your schedule content record.
-   Content:
    -   The content you are scheduling
    -   Content location by type
        -   Service Portal
        -   Workspace: When you choose Service Portal, the page and widget you can select and where your content appears.
    -   Where your content appears:
        -   Page: The page on the Service Portal you want your content to appear.
        -   Widget: The widget on the page of the Service Portal you want your content to appear.
        -   Content identifier: Associates portal content to Agent Workspace. This is the sys ID for the component in Agent Workspace.
        -   Component type \(announcement or quick link\)
    -   Targeted users and dates
        -   The audience the content is directed to or you can add specific users you want your content directed to.
        -   The start and end dates your content is available.


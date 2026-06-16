---
title: Content Publishing release notes
description: Version history for the Content Publishing application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-hr-content-publishing.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 10
breadcrumb: [ServiceNow Store - HR Service Delivery release notes, ServiceNow Store - Employee Service Management release notes, ServiceNow Store release notes]
---

# Content Publishing release notes

Version history for the Content Publishing application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 37.0.0 - June 2026 \(Australia\)**

    Updated to support the latest version of the dependent apps.

-   **Version 36.4.0 - June 2026 \(Zurich\)**

    Updated to support the latest version of the dependent apps.

-   **Version 36.3.4 - May 2026**

    Updated to support the latest version of the dependent apps.

-   **Version 36.2.1 - March 2026**

    Updated to support the latest version of the dependent apps.

-   **Version 36.1.7 - January 2026**

    Updated to support the latest version of the dependent apps.

-   **Version 36.1.5 - December 2025**

    Updated to support the latest version of the dependent apps.

-   **Version 36.0.7 - October 2025**
    -   Fixed:
        -   Issue with page and widget filtering when a publish plan is added.
        -   Issue where image assets in other languages are not displaying properly or are inconsistent when added or edited.
        -   Fixed Accordion tab creation, missing images in translated microsites, Rich Content widget scrolling, and News center page.
        -   Issues with dot indicators and time display on the News Feed widget across time zones.
        -   UI/Accessibility: Fixed responsive layout issues, improved control naming, focus visibility, and radio button grouping.
-   **Version 36.0.5 - September 2025**
    -   Addressed the following bugs:
        -   Enabled users to create multiple versions of a content item without restriction.
        -   Corrected event date display in the News Feed widget for users in different time zones.
        -   Restored data visibility in the Content Library Overview section.
    -   Update: Evaluation of ACLs for news and events-related tables to support the Now Assist VA use case.
-   **Version 36.0.3 - August 2025**
    -   New:
        -   Ability to add links to numbered/bulleted lists in Rich Content Editor
        -   Deferred loading experience for Content Publishing widgets in EC homepages
        -   Degraded loading experience for News Feed widget in EC Pro homepages
    -   Changed: AI Search results for Content Managers in Portal to not include content that they have access to author but are not in the audience
    -   Fixed:
        -   Enhance the Rich Content Editor translation process to avoid impacts on different languages when modifiying/translating the content
        -   Added alt text for styled content and banner images
-   **Version 35.0.12 - June 2025**
    -   Resolved the following bugs:
        -   Resolved users unable to add or edit Topics and Audiences in the Content Library Publish tabs when respective ownership settings were enabled.
        -   Improved timing details for nested calls in Performance Indicator.
        -   Resolved HTTP 414 Error - URI Too Large when adding an audience for non-admin use.
        -   Streamlined Use content template checkbox malfunction.
        -   Resolved malfunction in the reservation checkboxes and surge event when the language is not English.
        -   Streamlined hotspots incorrectly track the time of nested calls for Content Experience, Rich Content \(CD\), and Upcoming Events \(CD\) widgets.
        -   Resolved the RCE preset for Text component dropdown display for the colour of the text.
        -   Resolved the issue affecting the copy-paste functionality in the RCE Text component.
        -   Streamlined the SCA Preview on track/hr.
        -   Resolved RCE text preset failure to apply the correct element tag.
        -   Resolved the JavaScript error that occurs when trying to access performance stats in the Upcoming Events Widget.
        -   Fixed non-visibility of the Content Library embedded preview after the May release upgrade.
-   **Version 35.0.9 - May 2025**
    -   Rich Content Editor improvements: Add background images, set opacity, and apply colors, gradients, or shadows, as a content creator.
    -   Company Event management improvements:
        -   Collect RSVPs, set attendee limits, and manage wait lists.
        -   Utilize Workplace Service Delivery feature that allows event hosts to reserve conference rooms and display the reservation information on the details page of the company event.
    -   Company Event experience:
        -   Display upcoming company events on the News widget and other portal pages.
        -   View company events in the new calendar widget within the remodeled 'News and Events' page; previously known as the News Center.
    -   Get topic level security in My Favorites widget and Conversational LLM support to resolve tasks and approvals in Employee Center.
    -   Get improvements on experience feedback and feedback configurations with Employee Center Pro.
-   **Version 34.0.5 - March 2025**

    Fix for the Content Publishing, addressing various aspects such as images not uploading to the Rich Content Editor, UI behavior inconsistencies, and enabling Company Events to use Video Providers.

-   **Version 34.0.2 - February 2025**
    -   Live company events hosting and communications framework: Live company events can now be hosted directly in the Employee Center Pro portal, with prebuilt configurations to streamline the pre-event communications and handle traffic surges. Content authors can easily create and share event content using the drag-and-drop Rich Content Editor, combined with mass-publishing capabilities similar to news articles.
    -   Portal shortcuts for content authoring: Content authors can now easily edit or create news articles and banners using shortcuts in the Content Experiences or News widgets. The system auto-generates publishing plans, streamlining content delivery to the selected widget and reducing the effort needed for configuration.
-   **Version 33.0.9 - December 2024**
    -   Fixed following bugs:
        -   PRB1815818: The pause button in the Content Experiences widget now stops the banner carousel.
        -   PRB1818669: Users can now edit saved Rich Content items containing videos.
        -   PRB1819257: The Rich Content Editor now includes a vertical scrollbar for overflowing content.
        -   PRB1801686: \(4\) Users can translate content items with content versioning enabled.
        -   PRB1792863: \(5\) Users can successfully clone content items containing images.
-   **Version 33.0.3 - November 2024**
    -   Rich Content Editor updates: Introduced additional formatting elements for building more visually engaging content in microsites and news, including bulleted/numbered lists, table/grid layouts, and accordions.
    -   Navigation improvements: Microsites \(standalone pages created in the Rich Content Editor\) can now be displayed in the mega menu, enabling organizations to better showcase rich content topics and improve employee discovery and navigation.
-   **Version 32.0.5 - August 2024**
    -   New reusable templates for news: Save and use existing news articles as a Reusable Template, allowing easy replication of structured content and streamlined news publishing.
    -   New portal shortcuts: Create and edit Micro sites directly from the portal pages.
    -   Engagement metrics for all communication content: Measure and report the engagement metrics for all content published through content library, detailing impressions versus clickthrough rates.
    -   New Content Operations Dashboard: Track the operations across the content lifecycle, highlighting requests and active content publishing.
    -   New Content Publishing Calendar: Use cakebdar fir strategic planning and scheduling of communications activities.
    -   New Content Ownership Matrix: Track and manage ownership across content items, audiences, topics, and pages within the content platform.
-   **Version 31.1.4 - June 2024**

    Fixed minor issues.

-   **Version 31.1.3 - May 2024**

    Minor fixes.

-   **Version 31.0.5 - March 2024**
    -   Fixed minor issues for the following:
        -   Allow background image to be partially covered by right-hand list menu.
        -   Issue playing vbrick video on a Safari browser.
        -   Content managers can checkout restricted content.
-   **Version 31.0.3 - February 2024**
    -   New:
        -   Changed news article publishing control: Set the publication duration in the content destination, allowing content managers to select how long content is available based on the publishing location.
        -   Support for video hosting services: Create rich content and news articles using videos from a streaming services. Additionally, you can authorize access to secure videos and configure interface elements to help content managers, such as a thumbnails of available videos or checkboxes to enable loop or autoplay.
        -   Refreshed the Content Library UI with new styles, colors, icons and imagery.
        -   Expanded Rich Content Editor capabilities:
            -   Added a property to enable content managers to edit the HTML and CSS source code for Rich Content or News Articles.
            -   Clear the entire canvas of content with a single click.
            -   Configure image and video horizontal alignment. Select from left, center, or right.
            -   Configure cell border color, width, and style.
    -   Fixed: When you copy-paste text to the Rich Content Editor from another source \(for example, Microsoft Word\), the RCE removes the formatting and inserts the text into the selected textbox.
-   **Version 30.0.6 - November 2023**
    -   Several updates to the News experience within EC Pro including:
        -   Added support for news categories - News articles can be assigned to one or many news categories.
        -   Automate category assignment by pre-building your categories and adding them to a content template.
        -   Browse articles by categories using a new out-of-the-box widget on the News Center.
        -   Access the new layouts \(assigned through widget instance options\) for both the Featured News widget and the News Feed widget to offer layouts in tiles or lists.
        -   Avail improved article loading coupled with a new numbered pagination option.
        -   Access the news authoring changes for easy creation and targeting of a single article for EC Pro and the Now Mobile native app.
        -   Updated out-of-the-box content and demo data.
    -   Additional changes include:
        -   New tiled layout option for the Content Experiences Widget \(set via widget instance options setting or default OOTB layout for new deployments\).
        -   Height configuration for the Content Experiences Widget \(for desktop\) via a widget instance option.
        -   Right, left, and center alignment buttons within the Rich Content Editor.
-   **Version 29.0.7 - August 2023**
    -   Introduced an integrated news experience with a dedicated news center, news feed widgets along with automated news authoring and publishing capabilities.
    -   Enabled Search for News and Rich Content Microsites by making these indexable as search source for AI Search.
    -   Added three new pre-built layouts to the rich content editor for building microsites.
    -   Changed content authoring by enabling portal content version tracking, introducing new state changes, and adding change history details.
    -   Minor changes including builder and canvas usability, tab indexing, and element movement via a button click.
-   **Version 28.0.4 - March 2023**
    -   Fixed:
        -   Content schedule on UIB workspace is how when CG is installed.
        -   Rich content widget no longer errors on upgrade from the November/December 2022/Utah true up versions to March 23 version.
        -   Content Library \(SCA\) now enforces ownership restrictions.
        -   Audience user criteria and user type can now be changed after creation.
-   **Version 28.0.0 - February 2023**
    -   New: Added the ability to create a tab navigation for organizing content on Topic Microsites.
    -   Changed:
        -   Changed the Rich Content editor to inherit portal theme options to enable more consistent branding of Topic Microsites.
        -   Misc. usability changes, such as updated labels to the Rich Content editor.
-   **Version 27.0.4 - December 2022**

    Minor bug fixes

-   **Version 27.0.3 - November 2022**
    -   New Rich Content content type with visual content editor for non-technical users with drag-and-drop functionality.
    -   New Rich Content widget that can be placed on any Employee Center page to create topic Microsites.
    -   Added a new "headline" field to the Styled Content content type \(while removing text fields as "required"\) which enables graphical banners yet allowing for the Content Experiences Widget to show a headline in the right-hand menu.
-   **Version 26.0.2 - August 2022**
    -   New:
        -   Added integration with the ServiceNow Localization Framework to easily translate and review translated content through Content Library.
        -   Added preview and edit capabilities for translations so content authors can review translated content prior to publish.
-   **Version 25.0.10 - June 2022**
    -   Fixed:
        -   Gradient is not getting applied for content type Styled content \(Banner/Video\) on portals
        -   Clicking back on Content record loads an empty SCA page
        -   Fixing SCA ATF tests in Content Publishing
        -   When "Allow background image to be partially covered by Right-hand list menu" is checked in instance options of the widget the image gets multiplied/duplicated
-   **Version 24.0.5 - February 2022**
    -   New:
        -   Adds support for a new “Styled Content” format called “Video” allowing you to publish banners and announcements within supported widgets with embedded videos.
        -   Provides the ability to launch a full-portal preview of any portal content created within the Content Library.
        -   Adds new supported portal content types within the Content Library including: Events, Rich-text, and Image-based Link.
        -   Provides system properties and configuration capabilities that allow you to designate ownership for Topic pages within EC Pro.
-   **Version 23.0.5 - December 2021**

    Minor fixes.

-   **Version 23.0.4 - November 2021**

    New: The new streamlined content authoring custom interface makes it easier for non-technical admins to quickly and easily design, preview and publish content in a single, unified interface. This version includes portal content types including Banner, Styled Content, URL and Video.

-   **Version 22.0.3 - September 2021**
    -   Changed
        -   Add a new link type of "To-do" by assigning an existing To-do to a Link Content record. Once saved, you can assign the To-do link to a Banner or Styled Content item. The Banner/Styled Content item when scheduled, will automatically kick-off the To-do to the targeted users and appear on the portal with the ability to link the employee directly to the linked To-do.
        -   Target a topic page via Content Publishing's Schedule Content module. This allows a content author to create Banners, Styled Content announcements or Videos for publishing to a taxonomy-driven "Topic Page". Occurs when selecting the topic page or widget instance within Schedule Content \(will require the taxonomy and the topic\(s\) for targeting to the appropriate page\(s\)\).

**Parent Topic:**[ServiceNow Store - HR Service Delivery release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-hr.md)


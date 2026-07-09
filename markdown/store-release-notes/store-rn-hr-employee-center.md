---
title: Employee Center release notes
description: Version history for the Employee Center application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-hr-employee-center.html
release: store
topic_type: reference
last_updated: "2026-07-09"
reading_time_minutes: 7
breadcrumb: [ServiceNow Store - Employee Service Management release notes, ServiceNow Store release notes]
---

# Employee Center release notes

Version history for the Employee Center application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 44.1.1 - July 2026 \(Australia\)**

    Updated to support the latest version of the dependent apps.

-   **Version 41.0.3 - July 2026 \(Zurich\)**

    Updated to support the latest version of the dependent apps.

-   **Version 44.0.2 - June 2026 \(Australia\)**

    Updated to support the latest version of the dependent apps.

-   **Version 41.0.2 - June 2026 \(Zurich\)**

    Updated to support the latest version of the dependent apps.

-   **Version 40.1.3 - May 2026**
    -   Added the required support to configure the AIX widgets to the Task configurations.
    -   Added Org Chart schema to EC Core.
-   **Version 40.0.3 - March 2026**

    Added a more intuitive and detailed opt-in page, along with an interactive list-view option to the Enhanced Request Experience functionality, enabling ease of opting in and managing requests.

-   **Version 39.0.12 - February 2026**

    Updated to support the latest version of the dependent apps.

-   **Version 39.0.11 - January 2026**

    Updated to support the latest version of the dependent apps.

-   **Version 39.0.8 - December 2025**
    -   The following functionalities are added with the latest version of the application:
        -   Added new simplified left navigation experience that is modern, intuitive, mobile-friendly, and easy to configure.
        -   Added support for user experience analytics for measuring engagement on portal navigation i.e. Mega Menu.
        -   Introduced a new AI-assisted approval process for REQs and RITMs in My Tasks.
        -   Added flexible widget header settings and alignment for widgets like Content Experiences, Quick links, Topic header, topic content, sub-topics, and Rich Content Editor.
        -   Added tab-specific filters for the enhanced Requests experience for improved usability and search relevance.
    -   Fixes provided with this release: Fixed the security access for content in Quick links associated to a wesbite table. \(Removed admin overrides for ACLs on the Quick links widget associated to websites adhering to the security directives for granular admin roles\).
-   **Version 38.0.7 - October 2025**

    Fixed the quick links display order defect.

-   **Version 38.0.5 - August 2025**
    -   Recent changes:
        -   Improved Mega Menu performance Faster load times and smoother navigation.
        -   Improved resilience during high traffic events Optimized for stability and performance during peak usage.
        -   Identified and removed existing, outdated content and sync new content to associated categories.
        -   Enhanced Requests experience for better configurability and user experience.
    -   What you need:
        -   Get skeleton loaders for existing widgets and asynchronous load-time processing to improve overall portal performance.
        -   Get the Employee Center Browser Extension to stay connected with your Employee Center portal activities even when you're working on external applications.
        -   Note: Browser Extension feature requires the Employee Center for Browser Extension plugin.
-   **Version 37.0.7 - June 2025**
    -   Resolved the following bugs:
        -   ESC - Flickering occurs when the mega menu collapses into the hamburger view.
        -   'My Tasks' page breaks when NADW is pinned filters, tabs, and task details disappear.
        -   Background gradient size adjusted from 100% 30% to 100% 20%.
-   **Version 37.0.5 - May 2025**
    -   The topic-level security \(introduced in Yokohama family release\) is applied to topics visible in the My Favorites widget too.
    -   Use Conversational LLM to view and complete tasks and approval in Employee Center.
    -   Note: The conversational LLM feature is dependent on the Now Assist license.
-   **Version 36.0.8 - March 2025**
    -   The following bugs have been fixed for Employee Center as follows:
        -   Homepage widgets: Homepage widgets now display the execution time for each item individually, whereas it was previously shown as a cumulative total.
        -   Performance Indicator widget: The Performance Indicator widget is now accessible to users with the sp\_admin role.
        -   Quick Links widget text alignment: After upgrading to EC January 2025, the Quick Links widget failed to display any cards when the widget instance text\_alignment option was set to Left. This issue is now resolved.
-   **Version 36.0.7 - February 2025**
    -   New portal notifications: Employees stay informed with real-time alerts in the global header, highlighting key updates across departments. \(Requires Employee Center Notifications plug-in; see plug-in for more details\).
    -   Ability to favorite Topic pages: Employees can add topic pages to their Favorites to enable one-click access to their most frequently accessed topics.
    -   Improved topic page search: The Topic page content search now ranks search results based on user clicks, improving the relevance of search results, and making it easier for employees to find their frequently used content.
    -   Guided Self-Service is now searchable: Employees can now find Guided Self-Service links in AI Search-powered search results. \(Requires Guided Self-Service plug-in; see plug-in for more details\).
    -   Advanced Portal Navigation improvements:
    -   -   Taxonomy admins can sync taxonomy updates across Advanced Portal Navigation hierarchy levels with one click
-   In-product guided tour helps taxonomy admins with configuration
-   **Version 35.0.2 - November 2024**
    -   Guided Self-Service Enhancements: Users can review and edit their previous responses, providing a more streamlined experience.
    -   Admins can share text/image-based instructions as the end result of the Q&amp;A flow. \(requires Xanadu Family release\).
    -   Improved home page theme: Theme aligns with the latest set components, a new color scheme, a logo update, and CSS variable adjustments for an improved browsing experience.
-   **Version 34.0.10 - October 2024**

    Fixed critical issue.

-   **Version 34.0.7 - August 2024**
    -   Introduced Guided Self-Service experience in Employee Center. See Guided Self-Service in Employee Center plugin for additional highlights.
    -   Added the Send to self capability that enables employees to send knowledge articles via sms or email for future use and reference.
    -   Integrated with Twilio for the Send to Self SMS functionality.
-   **Version 33.0.5 - July 2024**

    This release primarily focussed on addressing minor defects related to My Active Items widget, count for My Tasks, and header menu read out in Employee Center portal.

-   **Version 33.0.2 - May 2024**

    No new feature was delivered in May '24.

-   **Version 32.0.3 - February 2024**

    Minor fixes to support right to left language translations.

-   **Version 31.0.3 - November 2023**
    -   New out-of-the-box Home Page templates for Employee Center.
    -   Updated Information Architecture \(IA\) with updated Taxonomy topics to account for new services added.
    -   Mega Menu changes that include support for mixed menu hierarchies, 4-levels of Mega Menu hierarchies with tabbed layout, left/right alignment, and option to invoke an interactive model window for Get Support menu item.
    -   My Active Items changes to add support for actions, visual changes in hierarchy, and new instance options to view as card and list.
    -   New favorites widget to access favorited content directly from the homepage.
    -   New Get Support widget to enable employees to access help content via quick links and static content on an interactive model window.
-   **Version 30.0.2 - August 2023**

    This release primarily provides fixes for minor issues.

-   **Version 29.0.2 - June 2023**

    Fixed: This release primarily focuses on addressing minor issues. The following fixes have been implemented:

    -   The sub-topic widget size issue has been fixed to update the user experience.
    -   The error messages seen when opening certain topic pages have been resolved.
    -   The issue causing the Show More button to hide without loading the data has been fixed.
-   **Version 29.0.1 - May 2023**

    Fixes and minor changes. Refer to Employee Profile app release notes for changes made to the Employee Profile capability.

-   **Version 28.0.4 - February 2023**
    -   Changed
        -   Improve portal navigation by arranging the Mega Menu in their desired order, including a mix of portal pages and Taxonomy Topics
        -   Support searching content on Topic Pages for improved content discovery \(requires AI Search &amp; Utah+\)
        -   Support filtering search results with Taxonomy Topics \(requires AI Search &amp; Utah+\)
-   **Version 27.0.5 - December 2022**

    Fixed issue related to an employee unable to view task details and complete an e-signature HR task from the journeys page in Employee Center.

-   **Version 27.0.4 - November 2022**
    -   Enable employees to manage their tasks using the admin-configured filters on the "My Tasks" page.
    -   Simplify sharing knowledge article URLs that always point to the latest version.
-   **Version 26.0.2 - August 2022**
    -   New
        -   Optimize the performance of the Employee Center portal with synchronous load configuration, individual widget performance details, and empty state message display.
        -   Added distributed ownership of taxonomy topics to enable business units to manage their own topic pages.
        -   New configurable approvals experience enables admins to more easily display additional approval types through configuration.
-   **Version 25.0.3 - May 2022**

    New

    -   Added new cross-channel favorites feature, pre-integrated with catalog, requests, and knowledge.
    -   Updated the Employee Profile page with an integrated image editor and Microsoft Teams presence indicator.
    -   Improved Curated Experiences for translated knowledge articles.
    -   Added the article attachment widget to the article page by default.
    For additional highlights, see [Employee Profile release notes]().

-   **Version 24.0.5 - February 2022**
    -   Changed: Updated the placement and visual styling of the mega menu widget.
    -   New:
        -   Introduced a modern, configurable employee profile page.
        -   Added new supported portal content types within the Content Library which include events, rich-text, and image-based Link.
        -   View the employee details and associated information from the Now Mobile app.
-   **Version 23.0.5 - November 2021**
    -   Changed:
        -   Updated mega menu with quick links displayed
        -   Improved my active items widget that supports web responsiveness and allows admins to define user restrictions on visibility of cards
-   **Version 22.0.11 - September 2021**
    -   Employee Center provides a single unified portal for multi-department service delivery, enabling organizations to easily scale their service solutions across IT, HR, Workplace, Legal, and Procurement so employees can easily find information, get help, and request the services they need from anywhere.


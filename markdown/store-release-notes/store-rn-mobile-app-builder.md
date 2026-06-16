---
title: Mobile App Builder release notes
description: Version history for the Mobile App Builder application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-mobile-app-builder.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 7
breadcrumb: [ServiceNow Store - Mobile release notes, ServiceNow Store release notes]
---

# Mobile App Builder release notes

Version history for the Mobile App Builder application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 27.13.0 - June 2026**

    New: Added support for Voice Launcher Functions.

-   **Version 27.12.1 - March 2026**
    -   New:
        -   Extended Live Preview functionality to include:
            -   Navigation Tabs
            -   Mobile App Configurations
            -   Input Forms
            -   Input Types
            -   UI Rules
            -   Sections Screen
            -   Grouped Lists
            -   Pop ups
            -   Empty States
            -   Section Card Instances
        -   "On demand loading" of floor node records in the configuration tree
        -   Configuration support for new features added to Mobile Platform in Australia
            -   Addition of script type and execution script field in Screen fields
            -   Navigation bar preview of prominent action button
            -   Screen input preview for the "MultiSelect" attribute
            -   Add support for the new "Local save" action item step type
            -   Support button, input and variable attributes for ServiceNow Mobile Lens feature
-   **Version 27.11.0 - August 2025**
    -   New:
        -   Integrated Mobile App Builder into ServiceNow Developer Studio for a seamless development experience.
        -   Added support for Dark Theme and Mako Theme to improve visual customization.
        -   Extended Live Preview functionality to include:
            -   Legacy Cards
            -   Chart Screens
            -   Launcher Screens
-   **Version 26.10.0 - June 2025**
    -   New: Web to Mobile AI Card Creation - Use Now Assist to create a new mobile card for use on a record screen created using the Web to Mobile functionality. Now Assist will automatically choose the optimal card template and map the most relevant table fields from the selected web form view.
    -   Improvements: Web to Mobile - The card selection and preview screens in the Web to Mobile flow have been consolidated to create a more streamlined user experience. This allows for the ability to generate previews using the different card options and jump back and forth between them to review.
-   **Version 27.10.1 - May 2025**
    -   New: Web to Mobile AI Card Creation - Use Now Assist to create a new mobile card for use on a record screen created using the Web to Mobile functionality. Now Assist will automatically choose the optimal card template and map the most relevant table fields from the selected web form view.
    -   Improvements: Web to Mobile - The card selection and preview screens in the Web to Mobile flow have been consolidated to create a more streamlined user experience. This allows for the ability to generate previews using the different card options and jump back and forth between them to review.
-   **Version 25.9.0 - February 2025**
    -   New:
        -   Live Mobile preview during configuration within Mobile App Builder.
        -   Ability to choose a web form and have the equivalent mobile record screen created automatically.
        -   Component recommendations extended to more record types.
        -   Support for mobile platform's new Yokohama features.
    -   Fixed:
        -   Improved translation performance by utilizing the latest JSON loader, resulting in faster and more efficient processing.
        -   Accessibility improvements.
-   **Version 24.8.0 - August 2024**
    -   New:
        -   Component recommendations by Now Assist, rather than a simple alphabetical list.
        -   Integration with Mobile Card Builder to create and select cards within Mobile App Builder.
        -   Expanded duplicate functionality for card templates, launcher screens, and functions.
        -   Streamlined creation of list screens with embedded record screens for a simplified user experience.
    -   Fixed: Resolved issues to improve usability and performance. For example, improved page load times performance for the home page and ensured that deleting a record will also remove its related records.
-   **Version 23.7.0 - February 2024**
    -   New
        -   Support for allMobile PlatformWashington DCfeatures.
        -   Integration withMobile Publishingso that admins can see their custom branded apps within theMABUI.
        -   A push notification management category has been added to show which notifications are used for each mobile app.
        -   Automatic population of table fields in downstream records to streamline proper configuration.
        -   Expanded Mobile App Builder duplicate functionality, by including additional record types which you can copy.
        -   Ability to set criteria for UI rules within the condition builder UI, using the UI rule configuration panel.
    -   Fixed:
        -   Resolved issues to improve usability and performance. For example,improved page load times performance for the home page and categories, in addition to simplifying the configuration of input attributes and UI rules.
-   **Version 22.6.0 - August 2023**
    -   New:
        -   Vancouver feature parity with the Mobile Platform. Including full configuration support for the calendar screen changes.
        -   Ability to duplicate records in the Mobile App Builder, where you can reuse the copied parent and children records in the same or a different scope.
        -   Notification to users when the latest version of a mobile app is available on the ServiceNow Store.
    -   Fixed: Resolved issues to improve customer experience, usability, and performance. For example, giving users more options to select from within table pickers and improved performance for choice lists.
-   **Version 21.5.0 - May 2023**
    -   New:
        -   Full feature parity with Mobile Platform - added support for new config panels like Parameterized Data Input form, Signature input, Barcode scanner, etc.
        -   Telemetry updates to gather new insights about usage metrics and how the customers are interacting with the application.
        -   Updated Mobile App Builder to use Next Experience branding colors and logos for specific UIelements.
    -   Fixed:
        -   Resolved issues to improve customer experience, usability, and performance.
        -   Making the application more accessible by fixing a11y related issues.
-   **Version 21.4.0 - February 2023**
    -   New: Feature parity for all features up to the Tokyo release:
        -   Added configuration support for mobile platform theming capabilities, to correspond with web-based UI theming.
        -   Ability to determine the family version of the instance at run time, thereby enabling only relevant table configurations.
    -   Fixed:
        -   Resolved issues to improve customer experience, usability and performance.
        -   Making the application more accessible by fixing a11y related issues.
-   **Version 21.3.3 - December 2022**

    Fixed: Addressed language translation issues which existed in Mobile App Builder and Mobile App Builder API.

-   **Version 23.3.1 - August 2022**
    -   New:
        -   Full parity with all San Diego mobile platform features. Users can configure San Diego mobile features like: custom map screens, UI policies, universal linking, and push notifications.
        -   New Features:
            -   Launcher screen configurations
                -   Select card size
                -   Implement badge count
            -   Screen configuration
                -   Custom map screen
            -   Functions
                -   Support for grouped input
                -   Button attributes
            -   Additional configurations
                -   Push applications
                -   Deep linking
                -   UI policies
    -   Changed:
        -   Usability changes like using choice-list and icon pickers instead of text inputs and auto populating additional fields when configuring child records.
        -   Updated features:
            -   Launcher configuration
            -   Record section changes
            -   Icon section changes
        -   Functions:
            -   Support for button attributes and grouped inputs
            -   New options for input form screen variables
            -   New options for emphasis colors on function instances
        -   Additional configurations:
            -   Offline mode change
    -   Fixed:
        -   Resolved issues to improve customer experience and usability.
        -   Fixed a11y related issues to make the application more accessible.
-   **Version 20.3.1 - June 2022**
    -   Fixed:
        -   Rectified functional issues when deleting newly created records. The issues were primarily related to the handling of associated child records of deleted records.
        -   Improved handling of default values in Mobile App Builder. The default values are more aligned with the way they are handled in the ServiceNow platform.
-   **Version 20.2.3 - April 2022**

    Fixed: UI changes were implemented to resolve performance issues in Mobile App Builder when rendering the ServiceNow AI Platform configuration tree with a large number of nodes. For example, the 'My Incidents' screen in ITSM app.

-   **Version 20.2.2 - March 2022**

    Fixed: Resolved performance issues in the Mobile App Builder when rendering the ServiceNow AI Platform configuration tree with a large number of nodes. For example, the Work Order Task screen within the latest FSM app.

-   **Version 20.2.1 - February 2022**

    Extends Mobile App Builder functionality enabling users to perform configurations for mobile features.

    -   New: API layer changes to support configuration of following Mobile features:
        -   Launcher configuration
            -   Analytics \(chart\) section
            -   Content section
            -   Global search
            -   Media section
        -   Screen configuration
            -   Calendar
            -   Chart
            -   Map
            -   Sections
        -   Other configurations
            -   Analytics \(dashboard\) preview
            -   Item sorting on a list
            -   Dynamic screen names
            -   UI rules
    -   Fixed: Resolved issues to improve customer experience and usability.
-   **Version 20.1.0 - November 2021**
    -   New: Onboarding module - On-screen tour pop-overs to introduce new users to the product and new UI.
    -   Changed:
        -   User Experience Analytics changes - To capture additional insights about user behavior.
        -   Now Platform configuration tree usability - Allows users to expand/collapse configuration tree nodes, in addition to performance improvements.
    -   Fixed:
        -   API optimizations to improve performance by 5x for retrieving records in the table picker.
        -   Resolved issues to improve customer experience and usability.
-   **Version 20.0.5 - September 2021**

    Mobile App Builder lets you rapidly build and configure ServiceNow iOS and Android mobile apps with a simplified interface, immersive previews, and powerful controls for your mobile workflows. Developers of all skill levels can easily create business-critical and great looking apps. More experienced developers can take advantage of more sophisticated tooling to build advanced mobile apps or create reusable components for low-code developers.


**Parent Topic:**[ServiceNow Store - Mobile release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-mobile-highlight.md)


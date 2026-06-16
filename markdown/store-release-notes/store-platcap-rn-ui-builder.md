---
title: UI Builder release notes
description: Version history for the UI Builder application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-platcap-rn-ui-builder.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 15
breadcrumb: [ServiceNow Store - Other ServiceNow AI Platform Capabilities applications, ServiceNow Store - ServiceNow AI Platform Capabilities release notes, ServiceNow Store release notes]
---

# UI Builder release notes

Version history for the UI Builder application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 29.4.29 - June 2026**

    What’s New: New ‘find and fix issue’ alert that warns users against having too many controllers or data brokers on a page as they can cause performance issues. Users are advised to consolidate or reduce the number of controllers and data brokers to prevent slow page loading

-   **Version 28.2.80 - June 2026 \(Zurich\)**
    -   This release contains the fixes for the issues where
        -   Excessive GraphQL calls were causing page unresponsiveness when variables are added to columns in a list visualization
        -   A UI Builder event named "sn\_uibtk\_api.builderassistant.bg.job" is causing an out-of-memory issue on the instance
        -   The checkbox of 'Allow quick edit' is not able to be unchecked from UI builder on 'List Controller' of Data resources
-   **Version 28.1.64 - June 2026 \(Zurich\)**

    This release contains the fix for the issue where excessive GraphQL calls were causing page unresponsiveness when variables are added to columns in a list visualization

-   **Version 29.3.15 - May 2026**
    -   What’s New: Enhanced localization in UI Builder - The "Code" and "Comment" fields for translation literals are now exposed in the properties pane. This allows developers to disambiguate English homonyms by providing unique composite identifiers \("Code" + "Key"\) and translator comments, improving translation accuracy.
    -   Key Issues Fixed: Other changes to improve accessibility
-   **Version 29.2.22 - April 2026**

    This release is focused on prioritizing platform health and making small but impactful improvements, such as security updates.

-   **Version 27.2.60 - April 2026 \(Yokohama\)**

    This patch release contains a fix for the issue where List - Simple does not display any columns in edit mode when variables are added to the list of columns.

-   **Version 27.1.65 - April 2026 \(Yokohama\)**

    This patch release fixes the issue where duplicating a variant is triggering the creation of huge number of duplicate records in an infinite loop

-   **Version 29.1.52 - March 2026 \(Australia\)**
    -   What's New:
        -   UI Interactions: Define events, configurable UI, and script within a single, integrated experience to create powerful UI interactions. These interactions are designed for maximum reusability, allowing you to deploy consistent behavior across any page or experience, and can be triggered effortlessly with any page event or Declarative Action or the Workspace "new tab" menu.
        -   Extending Page Collections: Extend page collections in out-of-the-box component bundles without duplicating or taking ownership of the components. This enables flexible, extensible addition of custom page collections to bundled modals and modeless dialogs.
    -   What has Changed:
        -   In component builder, filter conditions can now dynamically reference previously selected properties, ensuring relevant views are displayed based on the selected table.
        -   "Related List" tab functionality now displays Presentational Lists
    -   Key issues Fixed: Actions performed on interactive elements, such as button clicks are now announced by screen readers
-   **Version 28.1.62 - March 2026 \(Zurich\)**
    -   This patch release contains below fixes:
        -   The page created from page templates does not create event handlers
        -   Duplicating a variant is triggering the creation of huge number of duplicate records in an infinite loop
-   **Version 27.2.59 - March 2026 \(Yokohama\)**

    This patch release contains below fixes: Duplicating a variant is triggering the creation of huge number of duplicate records in an infinite loop

-   **Version 28.2.75 - February 2026 \(Zurich\)**

    This patch release provides a fix for the issues listed below: Config pane, Events pane are empty and don't see preset options, observed only when the Now Assist for Creator 28.2.0 is installed

-   **Version 28.1.60 - February 2026 \(Zurich\)**

    This patch release provides a fix for the issues listed below: List - Simple does not display any columns in edit mode

-   **Version 28.2.74 - January 2026 \(Zurich\)**
    -   This patch release provides a fix for the issues listed below:
        -   In a list visualization, user is unable to select extended table fields
        -   Duplicating a screen breaks RELAY events
        -   List - Simple does not display any columns in edit mode when variables are added to the list of columns.
        -   Config pane, Events pane are empty and don't see preset options, observed only when the Now Assist for Creator 28.2.0 is installed
-   **Version 27.2.58 - January 2026 \(Yokohama\)**

    This patch release contains the fix for the issue where duplicating a screen breaks RELAY events

-   **Version 28.2.73 - December 2025 \(Zurich\)**
    -   What's New:
        -   Page Sharing Across Experiences: Reuse pages and variants from one workspace to another, eliminating the need to create and manage duplicate copies of a page
        -   Simplified List of Pages: You can now search and filter pages within an experience to start editing them more quickly
        -   Homepage favorites: Easily access the pages you frequently need by starring experiences, components, presets or controllers to add them to your favorites on the homepage.
    -   What has Changed:
        -   When configuring events, quickly go back and forth between steps by clicking the different steppers in the new modeless dialog
        -   Multi select choice fields are now supported in config panes
        -   Enhancements were made to component builder to support image and page property type, and table choice and reference type properties. You can also set test values when authoring Components
    -   Key issues Fixed:
        -   The Visualization filters UI in Platform Analytics Dashboards now remain visible after multiple long values are added
        -   Side Navigation now remains visible after changing landing path
-   **Version 27.2.55 - November 2025**

    Fixes issue with Question variables are not displayed when selecting columns for List components.

-   **Version 28.1.57 - August 2025 \(Zurich\)**
    -   What's New:
        -   Component Builder: Assemble components in a low-code editor by dragging and dropping elements from the UIB toolbox onto the stage. Define configuration properties, add events and data resources, and save your configurations for future use in pages across your experiences. This is an easier alternative to NOW CLI for basic component assembly.
        -   Gen AI-powered pages and components: Easily add generative AI capabilities to any page, component, or controller, just like using a data resource.
        -   Conversational help: Ask questions directly in UI Builder and get immediate answers, saving time and boosting productivity.
    -   What has Changed:
        -   Find and fix more issues to help improve page performance and accessibility.
        -   Configure static tabs by binding dynamic data.
        -   Easily search the events search bar to find components in a dirty state.
        -   Enable alerts to auto-dismiss across an experience by configuring them in the experience settings, or individually through an event.
        -   View interoperable pages in the experience view. Interoperable pages can be used across various workspaces and are currently configurable only in the platform.
    -   Key issues Fixed: The expanded dropdown menus for column properties now receive screen reader focus and can be read by screen readers.
-   **Version 27.2.54 - July 2025 \(Yokohama\)**
    -   This release contains fixes for the following issues:
        -   Stage does NOT load on viewport subpages
        -   List - simple visualization has the tables selection field locked.
        -   Performance Degradation Due to sys\_ux\_macroponent\_rule Execution in Rules Engine
-   **Version 26.2.81 - July 2025 \(Xanadu\)**
    -   This release contains fixes for the following issues:
        -   User is unable to bind inherited data resource to local data resource property
        -   User is unable to configure repeater to modeless dialog component
-   **Version 27.2.52 - June 2025 \(Yokohama\)**
    -   This patch release contains fixes for the issues listed below:
        -   Adding a second Page collection, removes Page collection controller details from the already existing page collection
        -   Databroker search chokes if description exists but is not a string
        -   Optimize Search functionality for Toolbox
-   **Version 26.2.79 - June 2025 \(Xanadu\)**
    -   This patch release contains fixes for the issues listed below:
        -   Adding a new container on a component puts the UIB stage in a loading state
        -   Adding a second Page collection, removes Page collection controller details from the already existing page collection
        -   Missing pill view/JSON on right side of modal with content when creating a Glide formdatasource
        -   Databroker search stalls if description exists but is not a string
-   **Version 27.2.49 - May 2025 \(Yokohama\)**
    -   New:
        -   Quickly understand client scripts: Drastically reduce the time and effort required to parse and understand complex or lengthy client scripts within UI Builder.
        -   Utilize AI to configure select event handlers quickly: - Simplify configuration of events by leveraging AI for event handlers such as Link to destination, Open or close modal and Viewport load request
    -   Changed:
        -   Toolbox optimization: Easily find components in the toolbox by filtering categories and view their contextual details.
        -   Diagnose problems and improve quality: Elevate your end-use experiences by optimizing the layout and styles of your pages to deliver delightful user interactions
    -   Fixed:
    -   -   The Formula Builder pill view now accurately reflects the table fields for the Look up a single record data resource.
-   Component sections and sub-section properties are now translatable.
-   Users can now delete shared components from the content tree in the Page Editor if desired.
-   Page Collection name and app shell fields are now required to be filled in before they can be saved.
-   **Version 26.2.77 - April 2025**

    This release contains the fixes for the issues listed below:

    -   TRANSLATION LITERAL Strings are not passed passed down to Props-pane, impacting the JSON Editor and Collection editor
    -   UIB Homepage tabs load slowly
    -   Collection property configuration not working
-   **Version 27.1.60 - April 2025**

    This release contains the fixes for the issues listed below:

    -   UIB Homepage tabs load slowly
    -   Props pane sub-section labels are not being translated
-   **Version 27.1.59 - March 2025 \(Yokohama\)**
    -   This release contains fixes for the issues listed below:
        -   Unable to delete shared components from UI builder content tree
        -   Layout item styles missing for conditional item in styles pane
        -   The UIB parent page UI Controller events are not accessible from the sub pages
        -   Runtime is NOT showing the same styles as Stage when the Conditional Renderer is placed inside the Repeater whose styles are enabled
        -   Required and Optional parameters not saving while creating pc viewport pages
        -   Not able to add repeater to modeless dialog component
        -   "Delete all bundle content" issue on the Form controller \(for Form controller bundle\)
-   **Version 27.1.57 - February 2025 \(Yokohama\)**
    -   New:
        -   Make your content dynamic: Define multiple conditions that dynamically determine what's visible to your end users.
        -   Create and edit presets with ease: Save time by building presets that make your component configurations reusable across experiences. Simply drag and drop data from the controller to populate the component's properties and setup your preset.
        -   Create controllers for data binding: Quickly connect reusable, encapsulated data and scripts to your page with a controller. Use the new interface to easily set up the controller's inputs, outputs, and events.
        -   Scan records for changes: Quickly identify and resolve conflicts early and often in UI Builder to streamline your development process.
    -   Changed:
        -   Easily configure focus behavior with a rich dropdown menu that mirrors your content tree, enabling seamless page navigation for your end users.
        -   Create page collections directly in UI Builder using a streamlined modal for a seamless experience and efficient workflow.
-   **Version 26.1.74 - January 2025 \(Xanadu\)**
    -   This release contains for the following issues:
        -   Icon picker preloads all images and doesn't cache them.
        -   Link to "UI fundamentals" on the UIB home page is broken
-   **Version 25.2.12 - January 2025 \(Washington DC\)**

    This release contains fix for the issue where Icon picker preloads all images and doesn't cache them.

-   **Version 26.2.74 - December 2024 \(Xanadu\)**
    -   Fixed:
        -   Builder context field won't render properly if a field with scripted data type is in the form
        -   For "list-simple" data visualization, while filtering select box variables are not showing results in filter.
        -   While creating data visualization, the composition section of the page definition is missing causing the filters not to work as intended
        -   Unable to select audience if glide.invalid\_query.returns\_no\_rows is true
        -   Loading UIB Portal Experience Page is taking longer due to UX components and UX metrics interactions API call
        -   Add new event to ui-builder to support MACROPONENT\_TIME\_TO\_IDLE\_MEASUREMENT\_REQUESTED
        -   Conflicts between UI Controller external dependencies and form controllers results in data resource panel loading with no information
-   **Version 26.1.73 - December 2024 \(Xanadu\)**

    This release contains some fixes related to performance and data visualization configuration.

-   **Version 25.2.11 - December 2024 \(Washington DC\)**

    This release contains a fix for the issue where UIB configuration panel was not visible for custom components.

-   **Version 26.2.70 - November 2024 \(Xanadu\)**
    -   Highlights:
        -   Explore the Learning Center containing a searchable library of videos, guided tours, and product documentation to develop and practice UI Builder skills.
        -   Take guided tours to learn about features and complete tasks in UI Builder step-by-step.
        -   Use dark theme for improved usability in low-light conditions.
        -   Design pages that look good and function well across a variety of form factors such as laptops, tablets, and mobile devices using responsive authoring.
        -   Fetch information from multiple data sources and more easily bind the data to components of your choice with a new multi-table data resource right from UI Builder.
    -   UI Builder version 26.2 \(this release\)
    -   -   Builder Assistant - Builder Assistant runs design-time checks for common misconfiguration issues, then informs and instructs developers on how to fix them
-   Responsive Configuration - Leverage existing auto-reflow rules to provide responsive pages and components with defaults.
-   Events - Event handler UI improvements and enriched in-product content.
-   Presets, controllers and bundles UI improvements
-   Runtime Performance - Page authors will now have the ability to set caching policies for data resources. This improves performance by reducing the need to frequently fetch items from the server, particularly for data that updates less frequently.
-   **Version 26.1.69 - October 2024 \(Xanadu\)**

    This release contains the fix for the issue where Add component tool box is NOT populated until user scrolls up, when the left panel has more components.

-   **Version 25.2.9 - October 2024 \(Washington DC\)**

    This release contains the fixes for the issue where a user cannot open subpages of viewport from the component builder \(which is a subpage of record page tabs\).

-   **Version 25.1.27 - October 2024 \(Washington DC\)**
    -   This release contains the fixes for the issues listed below:
        -   Sub-pages with required parameters/fields cause empty list of sub pages in Sub-page overview page
        -   User cannot open subpages of viewport from the component builder \(which is a subpage of record page tabs\)
-   **Version 26.1.67 - September 2024 \(Xanadu\)**
    -   Fixed:
        -   Properties Pane incorrectly sends propName: value as part of payload to pageModel lifecycle handlers, causing CSTASK871911
        -   Repeaters in composition with an empty ID make them uneditable in UIB
-   **Version 25.2.8 - September 2024 \(Washington DC\)**
    -   Fixed:
        -   Properties Pane incorrectly sends propName: value as part of payload to pageModel lifecycle handlers
        -   UIB configuration panel not visible for custom components.
        -   When the user tries to set or change additional background properties for a column in UI Builder by clicking on the three dot-menu in the Background section the pop up opens intermittently after 7-8 clicks and quickly disappears again.
        -   Repeaters in composition with an empty ID make them uneditable in UIB
-   **Version 26.1.66 - August 2024 \(Xanadu\)**
    -   Highlights in the Xanadu release:
        -   Explore the Learning Center containing a searchable library of videos, guided tours, and product documentation to develop and practice UI Builder skills.
        -   Take guided tours to learn about features and complete tasks in UI Builder step-by-step.
        -   Use dark theme for improved usability in low-light conditions.
        -   Design pages that look good and function well across a variety of form factors such as laptops, tablets, and mobile devices using responsive authoring.
        -   Fetch information from multiple data sources and more easily bind the data to components of your choice with a new multi-table data resource right from UI Builder.
    -   New in the Xanadu release:
        -   Set screen conditions declarativelyControl the visibility of pages using a condition builder in addition to having the existing ability to write script.
        -   Configure Contextual Sidebar with TabsSimplified configuration of the Contextual Sidebar component using the Tabs component as a foundation instead of viewports.
        -   Control page layout for different device sizesCreate tailored pages that are appropriate for different size screens to improve the user experience.
        -   Retrieve data from varied sources for a componentMore easily add data from different data sources to a single component based on field mappings.
        -   Support for multiple forms on a pageAdd multiple forms and form controllers to a single page.
        -   Obtain term definitions in UI Builder documentationPoint to italicized terms in UI Builder documentation ondocs.servicenow.comto obtain a definition in a pop-up window.
-   **Version 25.2.5 - June 2024 \(Washington DC\)**
    -   New:
        -   Receive more frequent updates to UI Builder now that it's a ServiceNow Store application.
        -   Improved data binding and formula authoring experience to more easily link components to dynamic data.
        -   New data drawer and improved browsing experience when adding data resources to a page.
        -   Quickly edit column layouts and columns on a UI Builder page from the content tree or the stage.
        -   Access Form Builder directly from within the form component on the UI Builder stage.
        -   The new design-time experience provides a more WYSIWYG stage user interface that helps improve page building efficiency.
        -   Use the new UI Builder home page to access recently opened experiences, obtain help for getting started, and create experiences or page collections.
        -   More easily link components to dynamic data through improved data binding and formula authoring.
        -   Obtain available UI Builder code updates from a new banner message within UI Builder containing a link to the plugins page.
    -   Fixed:
        -   Preset binding in viewport subpages not binding correctly
        -   Data resource output in json-navigator becoming stale when two instances of the same resource exist
-   **Version 25.2.4 - May 2024 \(Washington DC\)**
    -   UI Builder highlights for the Washington DC release:
        -   Receive more frequent updates to UI Builder now that it's a ServiceNow Store application.
        -   Improved data binding and formula authoring experience to more easily link components to dynamic data.
        -   New data shelf and improved browsing experience when adding data resources to a page.
        -   Quickly edit column layouts and columns on a UI Builder page from the content tree or the stage.
        -   Access Form Builder directly from within the form component on the UI Builder stage.
    -   And as of UI Builder version 25.2 \(this release\)
        -   The new design-time experience provides a more WYSIWYG stage user interface that helps improve page building efficiency.
        -   Use the new UI Builder home page to access recently opened experiences, obtain help for getting started, and create experiences or page collections.
        -   More easily link components to dynamic data through improved data binding and formula authoring.
        -   Obtain available UI Builder code updates from a new banner message within UI Builder containing a link to the plugins page.
-   **Version 25.1.26 - April 2024 \(Washington DC\)**

    Fix to generate CLIENT\_TRANSFORM\_SCRIPT UxValue metadata correctly for component visibility and duplicate use cases.

-   **Version 25.1.25 - March 2024 \(Washington DC\)**

    Fixed: UI Builder now handles Client Script Includes in Scoped Application.

-   **Version 25.1.24 - February 2024**

    UI Builder is a web user interface builder that is part of the Next Experience UI Framework. UI Builder can be used to build pages for configurable workspaces, App Engine Studio generated workspaces and portals, and custom web experiences using Next Experience Components and custom web components.


**Parent Topic:**[ServiceNow Store - Other ServiceNow AI Platform Capabilities applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-platcap-rn-other-landing.md)


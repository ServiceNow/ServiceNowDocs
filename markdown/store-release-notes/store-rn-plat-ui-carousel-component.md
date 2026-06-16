---
title: Carousel component release notes
description: Version history for the Carousel component application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-plat-ui-carousel-component.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - ServiceNow AI Platform UI release notes, ServiceNow Store release notes]
---

# Carousel component release notes

Version history for the Carousel component application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 28.0.3 - June 2026**

    Fixed minor issues

-   **Version 28.0.2 - May 2026**
    -   Fixed:
        -   PRB1949558: Carousel Component 'No content to display' issue when used within modal - seen in v27.1.0
        -   PRB1975273: Carousel doesn't update to state changes when disableLooping is false
        -   PRB2000781: Carousel \`View index\` property does not update indicator position when value changes after initial render
        -   Other various defects
-   **Version 28.0.1 - March 2026**
    -   Changed:
        -   Expose config prop for carousel previous / next button controls in UIB
        -   Adopt system tokens for theming
    -   Fixed minor cosmetic issues
-   **Version 27.1.1 - February 2026**

    Fixed: Carousel component 'No content to display' issue when used within modal \(PRB1949558\)

-   **Version 27.1.0 - August 2025**

    Fixed various cosmetic issues.

-   **Version 27.0.2 - May 2025**
    -   New:
        -   Support for badge to indicate count of items
        -   Ability to change properties of Carousel Badge to use a JSON
        -   Ability to wrap long titles
    -   Multiple bug fixes
-   **Version 27.0.1 - February 2025**
    -   New: Ability to enable auto-scrolling on carousel
    -   Fixed:
        -   Various bugs
        -   NOW\_BUTTON\_ICONIC\#CLICKED event propagation getting prevented from inside of carousel \(PRB1792193\)
-   **Version 26.0.1 - August 2024**
    -   Changed:
        -   Updated component icon in UI Builder
        -   Screen reader to announce carousel region when there's no title
        -   Augment 'Index updated' event
    -   Fixed: minor defects
-   **Version 25.0.0 - February 2024**

    Fixed: Improved accessibility support \[WCAG2.1 AA\] for keyboard users through a more efficient tabbing interaction with the carousel.

-   **Version 24.0.3 - August 2023**
    -   New: Added accessibility features to support 2.1AA compatibility.
    -   Fixed: Various fixes to address minor issues.
-   **Version 23.0.0 - February 2023**

    Fixed: Minor bug fixes

-   **Version 22.1.0 - November 2022**
    -   New: Added support for internationalization and localization
    -   Changed: Tool Tips Added
-   **Version 22.0.1 - August 2022**

    Allow a user to rotate left and right through a list of items. Design and create each item in the carousel and configure navigation styling and behavior.


**Parent Topic:**[ServiceNow Store - ServiceNow AI Platform UI release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-plat-ui.md)


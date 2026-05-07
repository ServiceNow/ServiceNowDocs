---
title: Limitations of GTD
description: Learn about the limitation of the Guided Tour Designer.
locale: en-US
release: australia
product: Adoption Services
classification: adoption-services
topic_type: concept
last_updated: "2026-05-06"
reading_time_minutes: 1
breadcrumb: [Explore Guided Tours, Guided Tours, Adoption services, Configure user experiences]
---

# Limitations of GTD

Learn about the limitation of the Guided Tour Designer.

The GTD does not currently support the following areas.

-   **Standard Forms and Lists UI**
    -   Flow Designer
    -   Agent Workspace
    -   Pop-up windows
    -   Connect Chat and Embedded Help on the GTD sliding panel
    -   Select2 elements
    -   SVG elements
    -   Custom Tags
    -   Standard UI pages that have custom UI elements, such as Contextual search.
-   **Service Portal**
    -   Service Portal pages that contain IFRAMES
    -   The Service Portal Branding Editor, which also contains IFRAMES
    -   Select2 elements
    -   SVG elements
    -   Custom Tags
    -   Seismic components \(shadow dom\).

        For example: sn-search-combobox - AI search box, sn-search-results-container - AI search results, ci-chat-components.

    -   Tours when loaded in the Next Experience UI.
-   **Workspace**
    -   Only the following app shell experiences are supported:
        -   Breadcrumb App shell
        -   ACE Unified Nav App shell
        -   Workspace App shell
        -   Custom App shell
    -   Experiences with an empty app shell are not supported.
    -   Tours that start in a custom app shell and go to the Polaris app shell are not supported.
    -   Not recommended to create tours on Workspaces in UI16
    -   Variants
    -   Callouts inside iframes in a workspace
    -   Guided Tours that start in a standard UI or workspace and go to a service portal
    -   Guided Tours are only supported within a page, if a link opens in a new tab the tour does not continue

        **Note:** Admins must add the right action for the callout on elements that can open in a new tab.

    -   Guided Tours are not supported in mobile view
    -   Callouts on elements inside visualisation components or par widgets
-   **Technical limitations**
    -   Elements that are loaded in DOM by scrolling the page effect Guided Tours. The admin must inform the user to scroll further when the form is present.
    -   If there is no click action on the elements that are selectable while creating the tour, place the callout on the parent element.


---
title: Guided Setup release notes
description: Version history for the Guided Setup application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-platui-guided-setup.html
release: store
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - ServiceNow AI Platform UI release notes, ServiceNow Store release notes]
---

# Guided Setup release notes

Version history for the Guided Setup application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 6.0.2 - March 2026**
    -   Fixed:
        -   Fixed a security vulnerability where scope and domain separation could be bypassed via SNHelpService.
        -   Fixed an issue where the ITOM guided setup content was not displayed after creating a new configuration.
        -   Added localization \(L10N\) support for the Guided Setup feature.
-   **Version 5.0.4 - August 2025**
    -   New:
        -   Enable domain separation for Guided Setup
        -   Enhance Guided setups with improved navigational experience
        -   Ability to embed workspace pages in the Guided setup
        -   Assignment of Tasks at run time
        -   Ability to set Guided setup steps as mandatory
        -   Add Steps / Add Tasks to the Guided Setup Player
-   **Version 3.1.9 - May 2025**

    Fixed: Unable to initiate the Guided Setup from the pre-checklist page.

-   **Version 3.1.0 - February 2025**

    New: Guided Setups now support parallel execution of the same setup for different configurations. With this, setup owners can create guided setup experiences to run repeatable steps for different configurations/variables. This comes with the capability to view execution status separately for each execution record of guided setup.

-   **Version 2.0.10 - January 2025**

    Fixed an issue where the Help content record was missing during the upgrade to Xanadu.

-   **Version 2.0.9 - August 2024**
    -   Fixed following critical defects:
        -   Flickering issue
        -   Missing Mark as completed button
        -   Inconsistent spaces
-   **Version 1.1.4 - February 2024**

    Fixed: The left panel in the task view has been fixed to support scrolling use cases.

-   **Version 1.1.2 - June 2023**

    Fixed: Fixed issues related to task rendering, especially plugin type task in Vancouver instances.

-   **Version 1.0.1 - July 2022**

    Fixed: The page that explains how to use Guided setup is broken.

-   **Version 1.0.0 - May 2022**
    -   New:
        -   Step-by-step task process to complete configuration of product\(s\)
        -   Work on pre-checklist before starting setup
        -   Install dependent plugins from within the guided setup
        -   Complete table form actions
        -   Complete iFrame actions
        -   Read article/documentation applicable for setup
        -   Refer videos relevant for setup


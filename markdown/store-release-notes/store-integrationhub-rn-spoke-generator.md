---
title: Spoke Generator release notes
description: Version history for the Spoke Generator application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-integrationhub-rn-spoke-generator.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - Integration Hub, ServiceNow Store - ServiceNow AI Platform Capabilities release notes, ServiceNow Store release notes]
---

# Spoke Generator release notes

Version history for the Spoke Generator application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 4.4.0 - June 2026**

    New: Add System selection option on spoke creation.

-   **Version 4.3.0 - March 2026**

    Minor release with UX fixes.

-   **Version 4.2.4 - March 2026**

    Fixed: user with connector\_stewart role unable to upload logo and also unable to create connection alias on Spoke Builder.

-   **Version 4.2.0 - September 2025**

    Defect fix.

-   **Version 4.1.4 - September 2025**

    Fixed - HMAC Script ID issue

-   **Version 4.1.1 - August 2025**
    -   Spokes list page and Spoke details pages are a part of the ServiceNow Integration Hub Starter Pack. To create a Spoke using OpenAPI or Postman collection specification or Now Assist, you will need a ServiceNow Integration Hub Professional or Workflow Data Fabric license in your ServiceNow environments.
    -   We have added new pages to showcase AI Agents and event sources.
-   **Version 4.0.3 - February 2025**

    Low impact bug fixes.

-   **Version 4.0.1 - November 2024**
    -   New:
        -   Create new Actions inside spokes with GenAI capabilities.
        -   Create brand new custom spokes with GenAI capabilities.
-   **Version 3.0.0 - August 2024**
    -   New:
        -   Ability to create new Spokes from Spoke Generator using existing application scopes
        -   New feature to create Spoke using Postman Collection specification inside of Spoke Generator
        -   UI implementation of highlightingsearched text in now-list in Spoke generator.
        -   UI implementation of adding icons for Actions, Spoke activity log, Flows, Sub-flows, etc in left side tab layout of Spoke detail page
        -   Telemetry addition for Spoke Generator
    -   Fixed:
        -   Action Category name is not visible on actions page when action is created against new category
        -   Description correction: should be Spokes dashboard instead of Spokes tab
        -   Unable to create Spoke when scope name ends with '\_'
        -   Issues with inner and outer padding of cards + Missing external icon in button
        -   Issues found in Integrate Connection creation in Spoke Generator user journey.
        -   HTML tag is coming in Action short description on add operations page
-   **Version 2.0.4 - June 2024**

    Fixed: Family release compatibility issues.

-   **Version 2.0.2 - February 2024**
    -   New:
        -   Change to the Spoke detail page by adding the Flows, Sub Flows, and Category on the Actions Page.
        -   Autofill Base URL in part of OpenAPI import step.
        -   Partial selection of auto-update of Inputs, Outputs, and Error Handling in the OpenAPI Step.
        -   Spoke Generator to recommend spokes from the Store based on the provided spoke name.
        -   Change to connection and credentials setup in spoke generator.
-   **Version 1.1.1 - November 2023**
    -   New: Search capability in Operations tab and Spoke detail page
    -   Fixed:
        -   Add previous button to Operations page
        -   Cosmetic changes in Spoke detail page
        -   In spoke creation page, Create and continue button should be enabled once user enters all mandatory fields
        -   Accessibility - UI elements on Spoke details page are misaligned when browser is resized
        -   Update the Illustration with Spoke detail page
        -   Success alert is not shown when spoke is created from USB.
        -   General Info message displayed in Spoke Creation page is not reading out
-   **Version 1.0.2 - September 2023**

    Fixed: Spoke generator hardcoding x\_snc+name for scope name generation \(as opposed to customer code + name\).

-   **Version 1.0.1 - August 2023**

    Spoke Generator enables customers to build spokes with advanced features without generating code, greatly reducing the implementation time and offering spokes at a lower cost​.



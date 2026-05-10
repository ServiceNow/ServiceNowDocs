---
title: UI Builder release notes
description: The ServiceNow UI Builder application is a web user interface builder for building pages for Workspaces, as well as custom workspaces or portals with Next Experience Components. UI Builder was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
---

# UI Builder release notes

The ServiceNow® UI Builder application is a web user interface builder for building pages for Workspaces, as well as custom workspaces or portals with Next Experience Components. UI Builder was enhanced and updated in the Australia release.

## UI Builder highlights for the Australia release

-   Share UI Builder pages across experiences without copying or recreating them, reducing maintenance and keeping users in their current workspace.
-   UI Interactions let you define reusable UI and logic that can be triggered by user actions or system events and shared across any page or experience, eliminating the need to duplicate code or UI.

See [UI Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/ui-builder/ui-builder-overview.md) for more information.

**Important:** UI Builder is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Important information for upgrading UI Builder to Australia

Saving section for later.

## New in the Australia release

-   **[Create event-driven UI interactions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/ui-builder/uib-ui-interactions.md)**

    Trigger UI interactions directly from events in UI Builder, allowing you to link event-driven behavior to reusable interaction logic with the following benefits:

    -   Define an interaction once and apply it across multiple events and pages so UI components such as modals don't have to be associated directly with the page anymore.
    -   Connect events to interactions without additional scripting.
    -   Centralize logic for consistent updates and fewer errors.
    -   Previously, Declarative Actions using UXF Client Actions required manual wiring on each page leading to complexity and upgrade risks. UI Interactions replace this with reusable, declarative event mapping.
-   **Update an existing UI interaction flow \(link to edit topic\)**

    As of UI Builder version 29.2, the UI interaction diagram editor now supports in-place editing, giving you more flexibility when modifying existing interactions without rebuilding downstream flows.

    -   Insert new steps, If/Else logic, or And branches anywhere in an existing diagram.
    -   Swap the outgoing event on a step to change which event continues the flow.
    -   Delete events and their downstream steps directly from the diagram.
    -   View which toolbox items are unavailable for a specific location, with guidance on why.

## Changed in this release

-   **[Use pages across experiences](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/ui-builder/use-across-pages.md)**

    Share and reuse pages across workspaces without switching contexts or rebuilding content to help save time and simplify maintenance.


## Activation information

UI Builder is active by default. You can update to the latest version of UI Builder by downloading it from the

## Browser requirements

Internet Explorer isn't supported for UI Builder

## Accessibility information

The expanded drop-down menus for column properties can be ready by screen readers.

## Related ServiceNow applications and features

-   **[Build apps using App Engine Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/app-engine-studio/aes-overview.md)**

    After you create apps in ServiceNow App Engine Studio, you can then create their user interface in ServiceNow UI Builder.

-   **[Now Assist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/platform-now-assist-landing.md)**

    ServiceNow® Now Assist uses generative AI that is designed to enhance user productivity and efficiency through conversation and proactive experiences.

-   **[Overview tab in Now Assist Admin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/configuring-now-assist.md)**

    The Now Assist Admin console provides you with quick and effortless access to the important information that you need to set up, configure, and monitor Now Assist applications and features.

-   **[Now Assist Skill Kit](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skill-kit/now-assist-skill-kit-landing.md)**

    The ServiceNow® Now Assist Skill Kit enables you to create and publish custom prompts and skills for Now Assist.


**Parent Topic:**[App development and low-code release notes](build-automate-rn-landing.md)


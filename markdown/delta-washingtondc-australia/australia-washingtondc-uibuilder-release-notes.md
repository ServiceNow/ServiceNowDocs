---
title: Combined UI Builder release notes for upgrades from Washington DC to Australia
description: Consolidated page of all release notes for UI Builder from Washington DC to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-washingtondc-australia/australia-washingtondc-uibuilder-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-06-22"
reading_time_minutes: 10
breadcrumb: [Products combined by family]
---

# Combined UI Builder release notes for upgrades from Washington DC to Australia

Consolidated page of all release notes for UI Builder from Washington DC to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family UI Builder release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Washington DC to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading UI Builder to Australia

Before you upgrade to Australia, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

Saving section for later.

</td></tr></tbody>
</table>## New features

Between your current release family and Australia, new features were introduced for UI Builder.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

-   **[Custom images](https://www.servicenow.com/docs/access?context=work-components&family=washingtondc&ft:locale=en-US)**

Upload custom images in the Icon and Image components to match your existing imagery and branding.

-   **[Modeless Dialogs](https://www.servicenow.com/docs/access?context=uib-modeless-dialog&family=washingtondc&ft:locale=en-US)**

Overlay information on a page so you can interact with both the main content and the window content through a UI Builder Modeless Dialog.

-   **[Integration of UI Builder and Form Builder](https://www.servicenow.com/docs/access?context=access-form-builder&family=washingtondc&ft:locale=en-US)**

Access Form Builder directly from within the form component on the UI Builder stage.

-   **[New theme for UI Builder](https://www.servicenow.com/docs/access?context=nav-uib&family=washingtondc&ft:locale=en-US)**

The ServiceNow® Tools and Admin theme is now applied to UI Builder to provide a consistent look and feel across builder applications.

-   **[Gap option available within columns](https://www.servicenow.com/docs/access?context=set-gap-between-components-in-columns&family=washingtondc&ft:locale=en-US)**

As of UI Builder version 25.2, if a column contains multiple components, set the gap between the components.


</td></tr><tr><td>

Xanadu

</td><td>

-   **[Set screen conditions declaratively](https://www.servicenow.com/docs/access?context=control-conditions-for-your-variant&family=xanadu&ft:locale=en-US)**

Control the visibility of pages using a condition builder as an alternative to writing a script.

-   **[Configure contextual sidebar with tabs](https://www.servicenow.com/docs/access?context=add-contextual-sidebar&family=xanadu&ft:locale=en-US)**

The Contextual sidebar component now uses the Tabs component as a foundation instead of viewports for simplified configuration as a vertical set of tabs.

-   **[Control page layout for different device sizes](https://www.servicenow.com/docs/access?context=responsive-authoring&family=xanadu&ft:locale=en-US)**

Create tailored pages that are appropriate for different size screens.

-   **[Retrieve data from varied sources for a component](https://www.servicenow.com/docs/access?context=multi-source-data-configuration&family=xanadu&ft:locale=en-US)**

More easily add data from different data sources to a single component based on field mappings.

-   **[Support for multiple forms on a page](https://www.servicenow.com/docs/access?context=add-forms-to-ui-builder-pages&family=xanadu&ft:locale=en-US)**

Add multiple forms and form controllers to a single page.


</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

-   **[Build and customize components](https://www.servicenow.com/docs/access?context=component-builder&family=zurich&ft:locale=en-US)**

Build custom components and configure them to be used across pages and experiences.

-   **[Utilize AI on pages you are building](https://www.servicenow.com/docs/access?context=add-skill&family=zurich&ft:locale=en-US)**

Easily add generative AI capabilities to any page, component, or controller

-   **[Get conversational help with the Now Assist panel](https://www.servicenow.com/docs/access?context=uib-now-assist-panel&family=zurich&ft:locale=en-US)**

Ask questions directly in the Now Assist panel to receive immediate AI-driven guidance without leaving UI Builder.

-   **[Build pages and gain page insights using the Now Assist panel in UI Builder.](https://www.servicenow.com/docs/access?context=using-ui-builder-agent&family=zurich&ft:locale=en-US)**

As of UI Builder Version 28.2, use Now Assist to add components, bind data, adjust layouts, and get page insights such as number of components, data resource information, and access permissions.

-   **[Add test values in Component Builder](https://www.servicenow.com/docs/access?context=component-builder&family=zurich&ft:locale=en-US)**

As of UI Builder Version 28.2, define simulated page parameters to preview and validate how customer components behave during development.


</td></tr><tr><td>

Australia

</td><td>

-   **[Create event-driven UI interactions](https://www.servicenow.com/docs/access?context=uib-ui-interactions&family=australia&ft:locale=en-US)**

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

</td></tr></tbody>
</table>## Changes

Between your current release family and Australia, some changes were made to existing UI Builder features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

-   **[Column layout improvements](https://www.servicenow.com/docs/access?context=column-layout&family=washingtondc&ft:locale=en-US)**

Reorder, delete, add, and rename columns in column layouts from the content tree and the stage.

-   **[Controller component configuration improvements](https://www.servicenow.com/docs/access?context=controllers&family=washingtondc&ft:locale=en-US)**

Use the simplified component configuration for controller properties to more easily connect to data and scripts from UI Builder pages.

-   **[Simplified data binding](https://www.servicenow.com/docs/access?context=connect-data&family=washingtondc&ft:locale=en-US)**

Bind data visually using a simplified process for specifying tables, variables, and formulas.

-   **[Data resource configuration improvements](https://www.servicenow.com/docs/access?context=add-data-resources&family=washingtondc&ft:locale=en-US)**

Browse, locate, add, and configure data resources using the new data drawer.

-   **[Simplified addition of tabs](https://www.servicenow.com/docs/access?context=tabs-components&family=washingtondc&ft:locale=en-US)**

Add tabs in UI Builder pages right from the stage.

-   **[Improved image selection process](https://www.servicenow.com/docs/access?context=work-components&family=washingtondc&ft:locale=en-US)**

More easily browse available platform icons to use in the Icon component.

-   **[Simplified data binding](https://www.servicenow.com/docs/access?context=connect-data&family=washingtondc&ft:locale=en-US)**

As of UI Builder version 25.2, search for data bindings, browse data in a JSON view, and use undo-redo to correct any typos while binding.


</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

-   **[Add events to track components with unsaved changes](https://www.servicenow.com/docs/access?context=dirty-state-event&family=zurich&ft:locale=en-US)**

Use an event to quickly identify modified components.

-   **[Configure alerts to auto-dismiss](https://www.servicenow.com/docs/access?context=uib-configure-alerts&family=zurich&ft:locale=en-US)**

Enable alerts to auto-dismiss across an experience by configuring all of them in the experience settings or individually through an event.

-   **[Use pages across experiences](https://www.servicenow.com/docs/access?context=use-across-pages&family=zurich&ft:locale=en-US)**

Share and reuse pages across workspaces without switching contexts or rebuilding content to help save time and simplify maintenance.

-   **[Use the floating Now Assist panel to streamline your workflow](https://www.servicenow.com/docs/access?context=uib-now-assist-panel&family=zurich&ft:locale=en-US)**

As of UI Builder version 28.2, the fixed Now Assist panel has been replaced with a drag-enabled floating panel improving layout flexibility and workflow visibility.

-   **[Specify your page type in the Create a page wizard](https://www.servicenow.com/docs/access?context=create-page&family=zurich&ft:locale=en-US)**

As of UI Builder version 28.2, the Create a page wizard now includes a page**Type** dropdown field. This new field helps you to later identify and filter important pages within the Experience view list, especially helpful in large experiences with many pages.

-   **[Explore the newly enhanced Experience view](https://www.servicenow.com/docs/access?context=nav-uib&family=zurich&ft:locale=en-US)**

As of UI Builder version 28.2, the Experience view has improved usability in the following ways:

    -   Pages and their variants appear collapsed by default for a cleaner, more focused view.
    -   Locate pages and variants with ease utilizing the search field.
    -   Search by name, URL, URL type, or variant, and toggle between filters for a cleaner, more intuitive page list.
    -   Pagination is automatically enabled when 10 or more pages are present.

</td></tr><tr><td>

Australia

</td><td>

-   **[Use pages across experiences](https://www.servicenow.com/docs/access?context=use-across-pages&family=australia&ft:locale=en-US)**

Share and reuse pages across workspaces without switching contexts or rebuilding content to help save time and simplify maintenance.


</td></tr></tbody>
</table>## Removed

Between your current release family and Australia, some UI Builder features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Australia, some UI Builder features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate UI Builder.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

UI Builder is active by default. You can update to the latest version of UI Builder by downloading it from the ServiceNow Store.

</td></tr><tr><td>

Xanadu

</td><td>

UI Builder is active by default. You can update to the latest version of UI Builder by downloading it from the ServiceNow Store.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

UI Builder is active by default. You can update to the latest version of UI Builder by downloading it from the ServiceNow Store.

</td></tr><tr><td>

Australia

</td><td>

UI Builder is active by default. You can update to the latest version of UI Builder by downloading it from the

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for UI Builder we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for UI Builder we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

Internet Explorer isn’t supported.

</td></tr><tr><td>

Xanadu

</td><td>

Internet Explorer isn't supported for UI Builder.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

Internet Explorer isn't supported for UI Builder.

</td></tr><tr><td>

Australia

</td><td>

Internet Explorer isn't supported for UI Builder

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for UI Builder, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

The expanded drop-down menus for column properties can be read by screen readers.

</td></tr><tr><td>

Australia

</td><td>

The expanded drop-down menus for column properties can be ready by screen readers.

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for UI Builder we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for UI Builder we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

-   Receive more frequent updates to UI Builder now that it's available in the ServiceNow Store.
-   More easily link components to dynamic data through improved data binding and formula authoring.
-   Quickly find data resources through a new data drawer and an improved browsing experience.
-   Quickly edit column layouts and columns on a UI Builder page from the content tree or the stage.
-   Access Form Builder directly from within the form component on the UI Builder stage.
-   As of UI Builder version 25.2, use the new UI Builder home page to access recently opened experiences, obtain help for getting started using UI Builder, and create experiences or page collections.
-   As of UI Builder version 25.2, a new design-time experience provides a more WYSIWYG stage that helps improve page building efficiency.

 See [UI Builder](https://www.servicenow.com/docs/access?context=ui-builder-overview&family=washingtondc&ft:locale=en-US) for more information.

</td></tr><tr><td>

Xanadu

</td><td>

-   Explore a searchable library of videos, guided tours, and product documentation to develop and practice UI Builder skills.
-   Take guided tours to learn about features and complete tasks in UI Builder step-by-step.
-   Improve usability in low-light conditions by using dark theme.
-   Design pages that look good and function well across a variety of form factors such as laptops, tablets, and mobile devices using responsive authoring.
-   Fetch information from multiple data sources and more easily bind the data to components of your choice with a new multi-table data resource right from UI Builder.

 See [UI Builder](https://www.servicenow.com/docs/access?context=ui-builder-overview&family=xanadu&ft:locale=en-US) for more information.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

-   Assemble components in a low-code editor by dragging and dropping content from the UIB toolbox onto the stage.
-   Add Now Assist skills to enhance your page, component, or controller with generative AI capabilities.
-   Get instant conversational help within UI Builder through the Now Assist Panel.

 See [UI Builder](https://www.servicenow.com/docs/access?context=ui-builder-overview&family=zurich&ft:locale=en-US) for more information.

</td></tr><tr><td>

Australia

</td><td>

-   Share UI Builder pages across experiences without copying or recreating them, reducing maintenance and keeping users in their current workspace.
-   UI Interactions let you define reusable UI and logic that can be triggered by user actions or system events and shared across any page or experience, eliminating the need to duplicate code or UI.

 See [UI Builder](https://www.servicenow.com/docs/access?context=ui-builder-overview&family=australia&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-washingtondc-australia/rn-combined-intro.md)


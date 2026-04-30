---
title: Next Experience Components release notes
description: The ServiceNow Next Experience Components are the components used to build custom user interfaces. Next Experience Components was enhanced and updated in the Xanadu release.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 4
---

# Next Experience Components release notes

The ServiceNow® Next Experience Components are the components used to build custom user interfaces. Next Experience Components was enhanced and updated in the Xanadu release.

## Next Experience Components highlights for the Xanadu release

-   Build rich UI experiences with prebuilt system or custom components. To view the Next Experience Components API reference, usage guidance, and ServiceNow® UI Builder setup documentation, visit the [Developer site Next Experience Components doc](https://developer.servicenow.com/dev.do#!/reference/next-experience/components%3Freleases%5B%5D=washingtondc%26query=%26order_by=nameAsc%26limit=120%26offset=0%26categories%5B%5D=uib_component%26categories%5B%5D=uib_macroponent-component%26categories%5B%5D=uib_facades).
-   Use common web component patterns and principles, such as a JavaScript framework, immutable data, and simple action handlers.
-   Reuse components across multiple user interfaces to create a cohesive experience for your end users.
-   Use preset property values to configure properties and event handlers automatically for a component so the component is ready to work when you add it to a page. Presets can connect to a controller that acts as a data resource for the component. For more information, see [Automatically configure components using presets](https://www.servicenow.com/docs/access?context=presets&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US) and [Bind data to UI Builder pages using controllers \(advanced feature\)](https://www.servicenow.com/docs/access?context=controllers&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US).

## New in the Xanadu release

|Component|Description|
|---------|-----------|
|Custom illustration|Insert theme-able, inline Scalable Vector Graphics \(SVG\)s on a Workspace page.|
|Feedback|Capture granular user feedback for AI products through a series of pre-determined options or free-text responses.|

## Changed in this release

<table id="table_xfn_9mj_y5b"><thead><tr><th>

Component

</th><th>

Enhancements

</th></tr></thead><tbody><tr><td>

Appointment calendar

</td><td>

Reflow support in higher browser zoom levels of up to 400% in day and week view.

</td></tr><tr><td>

Badge

</td><td>

Option to enable partial number counts and additional characters, including the plus "+" symbol.

</td></tr><tr><td>

Breadcrumbs

</td><td>

Improved breadcrumb orientation experience with option to enable overflow menu.

</td></tr><tr><td>

Calendar

</td><td>

-   Extra content slot in the header to add buttons.
-   Column width control in the timeline view.

</td></tr><tr><td>

Checkbox

</td><td>

Customizable slot after the information button for inserting additional elements.

</td></tr><tr><td>

Checklist

</td><td>

-   Additional configuration options like Disabled, Read Only, and Invalid.
-   Font size customization.
-   Option to configure mandatory field indicator.
-   Error notification appears when the user attempts to submit a form with an incomplete required field.

</td></tr><tr><td>

Contextual sidebar

</td><td>

Improved configuration with vertical tabs structure.

</td></tr><tr><td>

Date-time

</td><td>

-   Time zone displays for users.
-   Horizontal layout option for date-time input field.

</td></tr><tr><td>

Email composer

</td><td>

-   Improved draft management experience with email footer and side panel action buttons.
-   Improved drafting experience with larger compose area and enhancements to save vertical space.
-   Option to enable auto-load of most recent draft.
-   Option to suppress "Send email" button.
-   Support for international characters in email IDs.

</td></tr><tr><td>

Email composer \(mini\)

</td><td>

-   Improved draft management experience with email footer and side panel action buttons.
-   Improved drafting experience with larger compose area and enhancements to save vertical space.
-   Option to enable auto-load of most recent draft.
-   Option to suppress "Send email" button.
-   Support for international characters in email IDs.

</td></tr><tr><td>

Form

</td><td>

Support for 2 or more forms on a page. **Note:** If you want to add a form to a legacy page with an existing form, see the [Form UIB Setup documentation](https://developer.servicenow.com/dev.do#!/reference/next-experience/xanadu/now-components/now-record-form-section-column-layout/uib-setu).

</td></tr><tr><td>

Highlighted value

</td><td>

Improved display of long text with text wrapping functionality.

</td></tr><tr><td>

Input

</td><td>

-   Customizable slot after the information button for inserting additional elements.
-   Added a caret slot that follows the user's text cursor.

</td></tr><tr><td>

Node map

</td><td>

In the hierarchical layout:-   Movable nodes in the map.
-   Customizable control panel.
-   Customizable node connections in new nodes.
-   Improved reflow in higher browser zoom levels.
-   Support for pausing node map layout refresh \(re-layout\).

</td></tr><tr><td>

Radio button

</td><td>

Customizable slot after the information button for inserting additional elements.

</td></tr><tr><td>

Related items

</td><td>

-   Show or hide the heading.
-   Configure the background color.
-   Refresh a specific list along with all other lists in the container.

</td></tr><tr><td>

Select

</td><td>

Customizable slot after the information button for inserting additional elements.

</td></tr><tr><td>

Text area

</td><td>

-   Customizable slot after the information button for inserting additional elements.
-   Added a caret slot that follows the user's text cursor.

</td></tr><tr><td>

Toggle

</td><td>

Customizable slot after the information button for inserting additional elements.

</td></tr><tr><td>

Typeahead

</td><td>

Customizable slot after the information button for inserting additional elements.

</td></tr><tr><td>

Typeahead multi

</td><td>

Customizable slot after the information button for inserting additional elements.

</td></tr></tbody>
</table>## Activation information

Next Experience Components is a ServiceNow AI Platform feature that is active by default.

## Accessibility information

Next Experience Components are updated for accessibility in the Xanadu release.

-   **Updated components**

    The following components were updated to support Web Content Accessibility Guidelines \(WCAG\) 2.1 level AA:

    -   360 degree visualization \[sn-grc-360-degree-visualization\]
    -   Agent Messaging \[sn-agent-messaging\]
    -   Analytics Q&amp;A \[sn-nlq-analytics\]
    -   Appointment calendar \[now-appointment-calendar\]
    -   Audio player \[sn-audio-player\]
    -   BCM Crisis map \[sn-bcm-crisis-map-connected\]
    -   Calendar \[now-calendar\]
    -   Capacity Planning \[sn-capacity\]
    -   Catalog Wizard \[sn-catalog-wizard-connected\]
    -   Chat Popover \[now-requestor-chat-popover\]
    -   Circuit map \[sn-circuit-map\]
    -   Confirmation message \[now-confirmation-message\]
    -   Q1 Dashboards Overview \[sn-dashboards-overview\]
    -   Data Grid UI Component \[sn-datagrid\]
    -   Data Visualization Designer \[sn-viz-designer\]
    -   DevOps Pipeline \[sn-devops-pipeline\]
    -   Display Only Form \[now-record-form-section-connected\]
    -   Email composer \[now-email-client-composer-connected\]
    -   FAM Map \[sn-fam-map\]
    -   Form record presence \[now-record-common-record-presence\]
    -   Funnel \[sn-va-funnel\]
    -   Gantt Chart \[now-gantt\]
    -   Geo Map \[sn-geo-map\]
    -   Guided Decisions App Shell Header \[sn-gd-app-shell-header\]
    -   Guided Decisions Builder \[sn-guided-decisions-builder\]
    -   Guided Decisions Experience \[sn-guided-decisions-card\]
    -   Indoor Mapping \[sn-map-component\]
    -   Metric datatable component \[sn-metric-datatable\]
    -   Node map \[sn-node-map\]
    -   OHS Injury Picker \[sn-ohs-injury-picker-connected\]
    -   PaCE dynamic form for inputing variables \[sn-pace-policy-dynamic-form\]
    -   PaCE Policy Builder \[sn-pace-policy-builder\]
    -   PaCE Policy Input \[sn-pace-policy-builder-io\]
    -   PAR Component Builder \[sn-par-component-builder\]
    -   Playbook Activity Picker \[now-playbook-activity-picker\]
    -   Playbook Form \[now-playbook-experience-form-connected\]
    -   Policy as Code Engine Test Playground Control \[sn-pace-test-playground-control\]
    -   Presentational List \[now-list\]
    -   Process Mining - Automation Discovery Report \[sn-promin-automation-discovery-report\]
    -   Process Mining - Improvement Initiatives \[sn-promin-initiatives-connected\]
    -   Process Mining - Improvement Opportunities \[sn-promin-process-findings-connected\]
    -   Process Mining - Notes \[sn-promin-notes-connected\]
    -   Process Mining - Projects List \[sn-promin-process-list-connected\]
    -   Process Mining - Routes \[sn-promin-process-routes-connected\]
    -   Process Mining Workbench \[sn-promin-workbench-connected\]
    -   Process Optimization - Map \[sn-promin-process-map-connected\]
    -   Quick Filter \[sn-quick-filter\]
    -   Quick Filter Popover \[sn-quick-filter-popover\]
    -   Reference Selector using Condition Builder \[sn-pace-policy-reference-selector-cb\]
    -   Risk Heatmap \[sn-risk-heatmap\]
    -   Roadmap \[sn-roadmap\]
    -   Scheduled Export \[sn-par-scheduled-export\]
    -   Search facets \[sn-search-facets\]
    -   Search input \[sn-search-combobox\]
    -   Search Result Wrapper \[sn-search-result-wrapper\]
    -   Split view \[split view\]
    -   Tab filter \[sn-tab-filter\]
    -   Task Planner \[sn-task-planner\]
    -   VA Analytics Chart Container \[sn-va-slotted-tile\]
    -   VA Analytics Event Property Set \[sn-va-custom-event-props\]
    -   VA Analytics Trend Score \[sn-va-score-trend\]
    -   Workplace Stack Plan \[sn-wsd-stackplan\]

## Related ServiceNow applications and features

-   **[UI Builder](https://www.servicenow.com/docs/access?context=ui-builder-overview&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US)**

    UI Builder is a low-code tool that enables users to build pages for workspace and portal web-based experiences.

-   **[Configurable Workspace UI](https://www.servicenow.com/docs/access?context=workspace-landing-page&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US)**

    Use components to build custom workspace experiences for agents who solve internal or external customer issues.


**Parent Topic:**[Features and changes by product](../new-features-changes.md)


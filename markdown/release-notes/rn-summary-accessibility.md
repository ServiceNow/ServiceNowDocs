---
title: Accessibility information for all Xanadu features and products
description: Cumulative release notes summary on accessibility information for Xanadu features and products. Some products have specific accessibility information or exceptions.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2026-04-08"
reading_time_minutes: 15
breadcrumb: [Release notes summaries for Xanadu features, Release notes for upgrading from Washington DC, Learn about the Xanadu release, Xanadu release notes]
---

# Accessibility information for all Xanadu features and products

Cumulative release notes summary on accessibility information for Xanadu features and products. Some products have specific accessibility information or exceptions.

**Important:**

To find documentation about accessibility features in ServiceNow products, see [Product documentation for accessibility](https://www.servicenow.com/docs/r/accessibility/available-accessibility-product-documentation.html).

To view accessibility conformance reports \(ACRs\) for currently supported releases, see [Accessibility conformance reports](https://www.servicenow.com/docs/r/accessibility/available-accessibility-conformance-reports.html).

<table id="rn-summary-accessibility-table" class="custom-rows"><thead><tr><th class="filter">

Application or feature

</th><th>

Details

</th></tr></thead><tbody><tr><td>

Agent Workspace for HR Case Management

</td><td>

-   **Accessibility improvements**

Accessibility improvements were completed to create a configurable workspace that supports WCAG 2.1 Level AA conformance.

-   **Reflow**

The Configurable Workspace supports reflow, which enables pages and content to be zoomed up to 400% through your browser settings without loss of content or functionality. Additionally, content can be enlarged without scrolling in two dimensions at a width equivalent to 320 CSS pixels or a height equivalent to 256 CSS pixels. Page layouts are transformed into a vertical, stacked view automatically when users increase browser zoom to 400%.

This enhancement helps users with low vision or who have trouble seeing web content in a browser due to monitor size, device type, poor lighting, or other situations. Reflow can be turned off with a system property for instances, experiences, and pages. See [Reflow for Configurable Workspace](https://www.servicenow.com/docs/access?context=auto-reflow&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US) for details.


</td></tr><tr><td>

Agent experience for CSM

</td><td>

The following templates were updated to support reflow, which enables pages and content to be zoomed up to 400% through your browser settings without loss of content or functionality. Additionally, content can be enlarged without scrolling in two dimensions at a width equivalent to 320 CSS pixels or a height equivalent to 256 CSS pixels.

-   [Case playbook: horizontal stages template](https://www.servicenow.com/docs/access?context=csm-playbook-templates&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US)
-   [Case playbook: vertical stages template](https://www.servicenow.com/docs/access?context=csm-playbook-templates&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US)

This enhancement helps users with low vision or who have trouble seeing web content in a browser due to monitor size, device type, poor lighting, or other situations. Reflow can be turned off with a system property for instances, experiences, and pages. See [Reflow for Configurable Workspace](https://www.servicenow.com/docs/access?context=auto-reflow&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US) for details.

</td></tr><tr><td>

Analytics, Intelligence, and Reporting

</td><td>

Reflow is supported for low-vision users. The following changes have been made to provide this support:

-   At 400% zoom, legends move to the bottom of the screen.
-   At 400% zoom, zoom is enabled by default on bubble visualizations.
-   At 400% or higher zoom, tooltips fit inside the screen.
-   Tooltips are shown when hovering over data points on bar and time series visualizations.
-   On gauge visualizations, range labels are shown as legends.

</td></tr><tr><td>

Business Continuity Management

</td><td>

Accessibility improvements for the Business Continuity Workspace include the following updates.

Screen reader support has been improved for the following features:

-   Business impact analysis assessment
-   Business impact analysis dashboard
-   Contributors side panel
-   **Assets** tab in the plans and events \(Element picker\)

</td></tr><tr><td>

Case management for CSM

</td><td>

The following templates were updated to support reflow, which enables pages and content to be zoomed up to 400% through your browser settings without loss of content or functionality. Additionally, content can be enlarged without scrolling in two dimensions at a width equivalent to 320 CSS pixels or a height equivalent to 256 CSS pixels.

-   [Case playbook: horizontal stages template](https://www.servicenow.com/docs/access?context=csm-playbook-templates&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US)
-   [Case playbook: vertical stages template](https://www.servicenow.com/docs/access?context=csm-playbook-templates&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US)

</td></tr><tr><td>

Core ServiceNow AI Platform

</td><td>

-   **TinyMCE Upgrade**

Tiny MCE is an open-source rich text editor used in the HTML editor field. The upgrade of TinyMCE from v.4 to v.6.8.2 provides the following accessibility improvements:

    -   **Keyboard**:
        -   The color picker slider is now accessible using both keyboards and screen readers.
        -   There is also now a check mark to indicate the color selected by the user.
        -   The close dialog buttons in the modal dialogs are now accessible.
        -   The keyboard focus indicator is now clearly visible in the font color selection menu items.
    -   **Screen reader**:
        -   The selected value of drop-down menus like **Font** and **Font-size** is now announced by the screen reader.
    -   **Low vision**:
        -   The script editor and the HTML editor tool bar is now dark theme compatible.
-   **Admin Center and Adoption Blueprints accessibility enhancements**

Accessibility issues have been fixed for the following personas as part of Xanadu in Admin Center and Adoption Blueprints:

    -   persona\_low\_vision
    -   persona\_no\_vision
    -   persona\_color
    -   persona\_auditory
    -   persona\_speech
    -   persona\_cognitive
    -   persona\_physical

</td></tr><tr><td>

Creator Studio

</td><td>

As of Creator Studio version 26.2.1, the following enhancements were made for accessibility:

-   To ensure that users know if a question has dynamic behavior without opening the side panel, questions within the form canvas are tagged.
    -   For sighted users, the tag is an icon.
    -   For screen reader users, the corresponding ARIA tags indicate the same information on the focusable element.
-   Navigating between tabs on the app settings modal no longer selects the close \(X\) button.

</td></tr><tr><td>

DevOps Change Velocity

</td><td>

-   **Accessibility improvements**

Accessibility improvements were completed to create a configurable workspace that supports WCAG 2.1 Level AA conformance.

-   **Reflow**

The Configurable Workspace supports reflow, which enables pages and content to be zoomed up to 400% through your browser settings without loss of content or functionality. Additionally, content can be enlarged without scrolling in two dimensions at a width equivalent to 320 CSS pixels or a height equivalent to 256 CSS pixels. Page layouts are transformed into a vertical, stacked view automatically when users increase browser zoom to 400%.

This enhancement helps users with low vision or who have trouble seeing web content in a browser due to monitor size, device type, poor lighting, or other situations. Reflow can be turned off with a system property for instances, experiences, and pages. See [Reflow for Configurable Workspace](https://www.servicenow.com/docs/access?context=auto-reflow&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US) for details.


</td></tr><tr><td>

Digital Portfolio Management

</td><td>

-   **Accessibility improvements**

Accessibility improvements were completed to create a configurable workspace that supports WCAG 2.1 Level AA conformance.

-   **Reflow**

The Configurable Workspace supports reflow, which enables pages and content to be zoomed up to 400% through your browser settings without loss of content or functionality. Additionally, content can be enlarged without scrolling in two dimensions at a width equivalent to 320 CSS pixels or a height equivalent to 256 CSS pixels. Page layouts are transformed into a vertical, stacked view automatically when users increase browser zoom to 400%.

This enhancement helps users with low vision or who have trouble seeing web content in a browser due to monitor size, device type, poor lighting, or other situations. Reflow can be turned off with a system property for instances, experiences, and pages. See [Reflow for Configurable Workspace](https://www.servicenow.com/docs/access?context=auto-reflow&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US) for details.


</td></tr><tr><td>

Document Intelligence

</td><td>

-   **Support for reflow**

The sn-docintel-iframe component was updated to support reflow, which enables pages and content to be zoomed up to 400% through your browser settings without loss of content or functionality. Additionally, content can be enlarged without scrolling in two dimensions at a width equivalent to 320 CSS pixels or a height equivalent to 256 CSS pixels.

This enhancement helps users with low vision or who have trouble seeing web content in a browser due to monitor size, device type, poor lighting, or other situations. Reflow can be turned off with a system property for instances, experiences, and pages. See [Reflow for Configurable Workspace](https://www.servicenow.com/docs/access?context=auto-reflow&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US) for details.


</td></tr><tr><td>

Document Services

</td><td>

Accessibility support has been added for document conversion from DOCX to PDF. PDF accessibility tags are now available to help users who rely on screen readers to navigate, understand, and interact with converted PDF documents.

</td></tr><tr><td>

Field Service Management

</td><td>

-   **Accessibility improvements**

Accessibility improvements were completed to create a configurable workspace that supports WCAG 2.1 Level AA conformance.

-   **Reflow**

The Dispatcher Workspace and Workforce Optimization for Field Service workspace support reflow, which enables pages and content to be zoomed up to 400% through your browser settings without loss of content or functionality. Additionally, content can be enlarged without scrolling in two dimensions at a width equivalent to 320 CSS pixels or a height equivalent to 256 CSS pixels. Page layouts are transformed into a vertical, stacked view automatically when users increase browser zoom to 400%.

In addition, the following pages were updated to support reflow:

    -   Territory planning
    -   Service location
    -   Geography
    -   Agent recommendation
This enhancement helps users with low vision or who have trouble seeing web content in a browser due to monitor size, device type, poor lighting, or other situations. Reflow can be turned off with a system property for instances, experiences, and pages. See [Reflow for Configurable Workspace](https://www.servicenow.com/docs/access?context=auto-reflow&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US) for details.


</td></tr><tr><td>

ITSM Mobile Agent

</td><td>

-   **Dark theme**

Starting in version 9.0, enable the dark theme for active calls in the Collaborate section of the My work applet in ITSM Mobile Agent. This option is commonly used to alleviate eye strain and improve readability.

-   **Data visualization changes**

Starting in version 9.0, accessible data visualizations for the analytics on sections of the applets are available. For more information, see the UI changes section.


</td></tr><tr><td>

Mobile Platform

</td><td>

Accessibility improvements for the ServiceNow Mobile Platform include the following updates:

-   Improved the ability to connect your mobile device to a Bluetooth keyboard, especially in the areas of maps and filters. This update improves navigation throughout mobile apps.
-   Improved management and layout of banner messages, when multiple messages are displayed simultaneously.

</td></tr><tr><td>

Next Experience

</td><td>

-   **[Next Experience keyboard shortcuts](https://www.servicenow.com/docs/access?context=next-experience-keyboard-shortcuts&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US)**

In addition to the 40 keyboard shortcuts available, there is a new keyboard shortcut to reduce the time required opening the OpenFrame window. This shortcut allows agents to dial and answer the phone from the platform.


</td></tr><tr><td>

Next Experience Components

</td><td>

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

</td></tr><tr><td>

Notifications

</td><td>

Screen reader support has been extended to the aria labels in the notification preferences and the advanced preferences. The support provides an explanation for button actions, such as the toggle button.

</td></tr><tr><td>

Now Assist AI agents

</td><td>

-   **[Voice Input for Now Assist AI agents](https://www.servicenow.com/docs/access?context=now-assist-panel-overview&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)**

Administrators can enable an optional voice input setting for the Now Assist panel in the Now Assist Admin console. This feature gives users a voice-to-text input option to access the Now Assist skills in the panel in any supported language. For more information, see Enable voice input for Now Assist panel.

Once enabled, the Enable voice input for the Now Assist panel option will be available in individual user accessibility preferences. See [Configure Next Experience accessibility preferences](https://www.servicenow.com/docs/access?context=next-experience-accessibility-preferences&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US) for more information.

Voice-to-text input can help users with mobility impairments access generative AI skills without using a keyboard. This feature can also be useful to blind or low-vision users, neurodivergent users, non-native language speakers, or mobile users on the go, such as field service agents.


</td></tr><tr><td>

Operational Resilience

</td><td>

Improved screen reader and translation support by adding ARIA button labels, tooltips, and alt text to the Operational Resilience Workspace. This support provides an explanation for button actions and identifies tooltip text to be translated.

</td></tr><tr><td>

Platform Analytics experience

</td><td>

Reflow is supported for low-vision users. The following changes were made to provide this support:

-   The view mode of the Platform Analytics dashboard editor and the Visualization designer support reflow.
-   All charts: At 400% zoom, if the legend is originally in any position other than the top or the bottom, it is moved to the bottom.
-   Bubble chart: XY zoom is enabled by default during reflow at 400% zoom.
-   Donut and pie charts: Range labels are shown as legends by default at 400% zoom.
-   Gauge chart: Range labels can be shown as a legend instead. At 400% zoom, this option is enabled automatically.
-   GeoMap: Zoom controls are persistent during reflow at 200%+ zoom.
-   Pivot Table: Row headers and footers and the first column unfreeze by default during reflow at 400% zoom.
-   Time Series and bar charts: New configuration option to show the specific data point in the tooltip instead of all data points. A single data point is shown by default during reflow at 400% zoom. Also, these charts do not show points with no data.
-   Date filters: During reflow, the date picker is not available in the configuration panel. Instead, you can select the start and end date and time from the Select a date range menu. Also, all components are stacked vertically.
-   Multi-select filters: Checkbox groups with a horizontal layout reflow to a vertical layout when zoomed.
-   True/false filters: Popovers and the Clear, Cancel, and Apply buttons are removed during reflow at 400% zoom.

Other accessibility changes include:

-   Data tables can be shown for all relevant visualizations, to aid screen readers. These data tables break down the proportion of values by percentage.
-   All charts: The “More options” menu now includes the chart title.
-   Indicator Scorecard: Keyboard navigation to expand and collapse rows and speech output are now supported.

</td></tr><tr><td>

Service Operations Workspace for ITSM

</td><td>

-   **Accessibility improvements**

Accessibility improvements were completed to create a configurable workspace that supports WCAG 2.1 Level AA conformance.

-   **Reflow**

The Configurable Workspace supports reflow, which enables pages and content to be zoomed up to 400% through your browser settings without loss of content or functionality. Additionally, content can be enlarged without scrolling in two dimensions at a width equivalent to 320 CSS pixels or a height equivalent to 256 CSS pixels. Page layouts are transformed into a vertical, stacked view automatically when users increase browser zoom to 400%.

This enhancement helps users with low vision or who have trouble seeing web content in a browser due to monitor size, device type, poor lighting, or other situations. Reflow can be turned off with a system property for instances, experiences, and pages. See [Reflow for Configurable Workspace](https://www.servicenow.com/docs/access?context=auto-reflow&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US) for details.

-   **Resize text**

Starting in version 6.1, text size can be increased to 400% through your browser settings without loss of content or functionality for Incident Management and Password Reset in SOW.


</td></tr><tr><td>

Theme Builder

</td><td>

Accessibility improvements for Theme Builder include the following updates:

-   Added a dark alternate color palette that makes the display easier for your eyes and less disturbing in low-light settings is available for creation. For more information, see [Add an alternate color palette](https://www.servicenow.com/docs/access?context=tb-edit-color-palette&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US).
-   Updated modal when you publish a theme group for your web instance. A warning appears if there’s an accessibility error within the base theme or the theme's alternate color palettes. A link within the modal navigates you to the correct theme or alternate color palette with accessibility errors.
-   Improved Accessibility Inspector detects and guides you through fixing accessibility issues in your theme. This tool includes the total number of violations and a list of specific components with accessibility issues. For more information, see [Adjust a component to meet accessibility standards](https://www.servicenow.com/docs/access?context=tb-adjust-component-wcag&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US).
-   Updated reflow feature ensures the content within the Component Editor view automatically adjusts when the screen size is reduced. This improvement eliminates the need for horizontal scrolling.

</td></tr><tr><td>

Third-party Risk Management

</td><td>

Accessibility improvements for the Third-party Risk Management application include the following updates.

-   Keyboard focus: Improved visual accessibility in the Third-party portal by increasing contrast between the focus border and white background.
-   Screen reader support has been extended to announce the following:
    -   Completed status after all questions have been completed in a section of an external questionnaire in the Third-party portal.
    -   Correct labels and other relevant information for controls, images, card regions, menu items, and links in the Vendor Management Workspace.

</td></tr><tr><td>

Vendor Management Workspace

</td><td>

-   **Accessibility improvements**

Accessibility improvements were completed to create a configurable workspace that supports WCAG 2.1 Level AA conformance.

-   **Reflow**

The Configurable Workspace supports reflow, which enables pages and content to be zoomed up to 400% through your browser settings without loss of content or functionality. Additionally, content can be enlarged without scrolling in two dimensions at a width equivalent to 320 CSS pixels or a height equivalent to 256 CSS pixels. Page layouts are transformed into a vertical, stacked view automatically when users increase browser zoom to 400%.

This enhancement helps users with low vision or who have trouble seeing web content in a browser due to monitor size, device type, poor lighting, or other situations. Reflow can be turned off with a system property for instances, experiences, and pages. See [Reflow for Configurable Workspace](https://www.servicenow.com/docs/access?context=auto-reflow&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US) for details.


</td></tr><tr><td>

Workforce Optimization for Customer Service CSM

</td><td>

-   **Accessibility improvements**

Accessibility improvements were completed to create a configurable workspace that supports WCAG 2.1 Level AA conformance.

-   **Reflow**

The Configurable Workspace supports reflow, which enables pages and content to be zoomed up to 400% through your browser settings without loss of content or functionality. Additionally, content can be enlarged without scrolling in two dimensions at a width equivalent to 320 CSS pixels or a height equivalent to 256 CSS pixels. Page layouts are transformed into a vertical, stacked view automatically when users increase browser zoom to 400%.

This enhancement helps users with low vision or who have trouble seeing web content in a browser due to monitor size, device type, poor lighting, or other situations. Reflow can be turned off with a system property for instances, experiences, and pages. See [Reflow for Configurable Workspace](https://www.servicenow.com/docs/access?context=auto-reflow&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US) for details.


</td></tr><tr><td>

Workforce Optimization for ITSM

</td><td>

-   **Accessibility improvements**

Accessibility improvements were completed to create a configurable workspace that supports WCAG 2.1 Level AA conformance.

-   **Reflow**

The Configurable Workspace supports reflow, which enables pages and content to be zoomed up to 400% through your browser settings without loss of content or functionality. Additionally, content can be enlarged without scrolling in two dimensions at a width equivalent to 320 CSS pixels or a height equivalent to 256 CSS pixels. Page layouts are transformed into a vertical, stacked view automatically when users increase browser zoom to 400%.

This enhancement helps users with low vision or who have trouble seeing web content in a browser due to monitor size, device type, poor lighting, or other situations. Reflow can be turned off with a system property for instances, experiences, and pages. See [Reflow for Configurable Workspace](https://www.servicenow.com/docs/access?context=auto-reflow&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US) for details.


</td></tr></tbody>
</table>**Parent Topic:**[Release notes summaries for Xanadu features](../release-notes-summaries.md)


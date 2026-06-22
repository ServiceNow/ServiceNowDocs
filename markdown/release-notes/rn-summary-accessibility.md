---
title: Accessibility information for all Australia features and products
description: Cumulative release notes summary on accessibility information for Australia features and products. Some products have specific accessibility information or exceptions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/rn-summary-accessibility.html
release: australia
product: Release Notes
classification: release-notes
topic_type: reference
last_updated: "2026-06-12"
reading_time_minutes: 8
breadcrumb: [Release notes summaries for Australia features, Release notes for upgrading from Zurich, Learn about the Australia release, Australia release notes]
---

# Accessibility information for all Australia features and products

Cumulative release notes summary on accessibility information for Australia features and products. Some products have specific accessibility information or exceptions.

**Important:**

To find documentation about accessibility features in ServiceNow products, see [Product documentation for accessibility](https://www.servicenow.com/docs/r/accessibility/available-accessibility-product-documentation.html).

To view accessibility conformance reports \(ACRs\) for currently supported releases, see [Accessibility conformance reports](https://www.servicenow.com/docs/r/accessibility/available-accessibility-conformance-reports.html).

<table id="rn-summary-accessibility-table" class="custom-rows"><thead><tr><th class="filter">

Application or feature

</th><th>

Details

</th></tr></thead><tbody><tr><td>

AI Agent Advisor

</td><td>

The AI Agent Advisor application supports all platform accessibility features.

</td></tr><tr><td>

AI Control Tower

</td><td>

The AI Control Tower application supports all platform accessibility features.

</td></tr><tr><td>

Activity Management

</td><td>

The CRM Outlook Add-in includes screen reader improvements for card views in this release. On the Accounts, Contacts, Leads, and Opportunities tabs, each card announces its primary record details such as the contact name and key fields instead of a generic card-button label, so users on assistive technology can identify records without opening each card.

</td></tr><tr><td>

Adoption Services

</td><td>

-   **[Guided Tours](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/adoption-services/guided-tours.md)**

Guided Tours is enhanced with more accessibility features including:

    -   Descriptive page titles
    -   Keyboard assistance for suggesting required fields through screen reader
    -   Keyboard assistance for focussed user interface controls like, tool tip icons and check-boxes

</td></tr><tr><td>

Authentication

</td><td>

-   **Coral theme**

Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.


</td></tr><tr><td>

CPQ

</td><td>

The CPQ runtime configuration experience includes the following keyboard and screen reader accessibility improvements.

-   Navigate and select options in single-select picklists, selectable product cards, and the product picker grid using a keyboard.
-   Shopping cart and bill of materials \(BOM\) column headers are announced as text with full, untruncated labels, and table cells reference their row and column headers for screen reader context.
-   Field labels are read across transaction runtime fields, keyboard focus returns to the date input after a calendar selection, and the field edit page provides more descriptive context for related item tiles and tooltips.

</td></tr><tr><td>

Change Management

</td><td>

-   **Reflow for Create a change request page**

The Create a change request page now supports reflow, which enables pages and content to be zoomed up to 400% through your browser settings without loss of content or functionality. Additionally, content can be enlarged without scrolling in two dimensions at a width equivalent to 320 CSS pixels or a height equivalent to 256 CSS pixels. Page layouts are transformed into a vertical, stacked view automatically when users increase browser zoom to 400%.

This enhancement helps users with low vision or who have trouble seeing web content in a browser due to monitor size, device type, poor lighting, or other situations. Reflow can be turned off with a system property for instances, experiences, and pages.


</td></tr><tr><td>

Collaborative Work Management

</td><td>

-   **Accessibility improvements**

Accessibility improvements were completed to create a configurable workspace that supports WCAG 2.1 Level AA conformance.

-   **Reflow**

Docs in CWM Configurable Workspace supports reflow, which enables pages and content to be zoomed up to 400% through your browser settings without loss of content or functionality. Additionally, content can be enlarged without scrolling in two dimensions at a width equivalent to 320 CSS pixels or a height equivalent to 256 CSS pixels. Page layouts are transformed into a vertical, stacked view automatically when users increase browser zoom to 400%.

This enhancement helps users with low vision or who have trouble seeing web content in a browser due to monitor size, device type, poor lighting, or other situations. Reflow can be turned off with a system property for instances, experiences, and pages.


</td></tr><tr><td>

Configurable Workspace

</td><td>

-   **[Screen Summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/configure-user-experiences/use-screen-summarization.md)**

Screen Summarization is a feature that supports visually impaired and low-vision users by providing AI-generated summaries of workspace pages and their sections. The summaries can be read aloud with a screen reader to help reduce navigation and comprehension time.

Install Screen Summarization by requesting it from the ServiceNow® Store. Visit the [ServiceNow® Store](https://store.servicenow.com/store) to view all the available apps and information about submitting requests to the store.


</td></tr><tr><td>

Creator Studio

</td><td>

The following updates were made to support accessibility:

-   Form elements now have accurate interactive ARIA roles, enabling screen readers to identify and announce them accurately.
-   Rich text area and form elements are now accurately labeled so screen readers can announce them correctly when focused.
-   Keyboard focus now remains within the expanded template preview modal for the duration of the modal interaction.
-   The rich text frame **Long Description** now has the correct label, enabling screen readers to identify and announce it correctly.

</td></tr><tr><td>

Employee Center

</td><td>

Improve accessibility by allowing admins to configure widget heading levels \(H1–H6\) to meet organizational standards and support technologies. Clear heading hierarchies improve navigation for screen reader and keyboard users.

</td></tr><tr><td>

Employee Slate

</td><td>

Employee Slate includes built-in accessibility compliance through the AI widget builder. Custom widgets automatically meet accessibility standards when created through the prompt-driven interface with design components that include accessibility features by default.

</td></tr><tr><td>

Enterprise Architecture

</td><td>

-   Navigate the interface using the keyboard on the Enterprise Modeling and Visualization pages.
-   Access the shape context menu using the keyboard on the Enterprise Modeling and Visualization canvas. On navigating to a particular shape context menu button, the selected button gets highlighted.
-   See pop-over menus when hovering over connector lines on the Enterprise Modeling and Visualization canvas.
-   Keep connector ports visible on all shapes in the diagram canvas without hovering by enabling the **Show all buttons without the need to hover** option in **Preferences** &gt; **Accessibility**. When enabled, connector ports remain visible at all times on General, ArchiMate®, AWS, CSDM, and Group shapes. For more information, see [Show shape controls without hovering](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/enterprise-architecture/eaw-show-shape-ports.md).
-   Reflow- The Enterprise Architecture Workspace supports reflow, which enables pages and content to be zoomed up to 400% through your browser settings without loss of content or functionality. Additionally, content can be enlarged without scrolling in two dimensions at a width equivalent to 320 CSS pixels or a height equivalent to 256 CSS pixels. Page layouts are transformed into a vertical, stacked view automatically when users increase browser zoom to 400%.

This enhancement helps users with low vision or who have trouble seeing web content in a browser due to monitor size, device type, poor lighting, or other situations. Reflow can be turned off with a system property for instances, experiences, and pages.


</td></tr><tr><td>

Identity

</td><td>

-   **Coral theme**

Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.


</td></tr><tr><td>

Mobile Platform

</td><td>

Improved readability on tablet devices.

</td></tr><tr><td>

Next Experience

</td><td>

-   **[Enable auto-focus on page alerts new accessibility preference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/configure-user-experiences/enable-auto-focus-on-page-alerts.md)**

When enabled, this preference automatically moves your keyboard focus to important alerts so you don't miss critical messages while navigating with a keyboard or screen reader.

-   **[Learn about accessibility preferences with a guided tour](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/configure-user-experiences/next-experience-accessibility-preferences.md)**

Explore accessibility preferences with a guided tour that shows how to customize navigation, keyboard behavior, and visual themes in Next Experience.


</td></tr><tr><td>

Next Experience Components

</td><td>

To view Next Experience Components accessibility conformance information, refer to the components section of the [Horizon site Components section](https://horizon.servicenow.com/workspace/components). The Overview for each component contains accessibility \(A11y\) information.

</td></tr><tr><td>

Now Assist AI Agents

</td><td>

-   **[Voice Input for Now Assist AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/enable-ai-experiences/now-assist-panel-overview.md)**

Administrators can enable an optional voice input setting for the Now Assist panel in the Now Assist Admin console. This feature gives users a voice-to-text input option to access the Now Assist skills in the panel in any supported language. For more information, see [Enable voice input for Now Assist panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/enable-ai-experiences/enable-voice-input-for-now-assist-panel.md).

After enabled, the Enable voice input for the Now Assist panel option is available in individual user accessibility preferences. See [Configure Next Experience accessibility preferences](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/configure-user-experiences/next-experience-accessibility-preferences.md) for more information.

Voice-to-text input can help users with mobility impairments access generative AI skills without using a keyboard. This feature can also be useful to blind or low-vision users, neurodivergent users, non-native language speakers, or mobile users on the go, such as field service agents.


</td></tr><tr><td>

Now Assist Center

</td><td>

The Now Assist Center application supports all the platform accessibility features.

</td></tr><tr><td>

Now Assist in Platform Analytics

</td><td>

-   \(June 2026 AI Data Explorer\) Keyboard navigation allows tabbing between the text editor and the icons.
-   \(June 2026 AI Data Explorer\) Users can use move up/move down control menu items to change the order of question/response nodes in the exploration. Previously they could only drag the nodes.

</td></tr><tr><td>

RPA Hub

</td><td>

-   **Accessibility improvements**

Accessibility improvements were completed to support WCAG 2.1 Level AA conformance.


</td></tr><tr><td>

Self-service and omnichannel engagement for CSM

</td><td>

CSM Engagement Messenger now supports reflow, allowing content to be zoomed up to 400% in a browser without loss of content or functionality. Page layouts automatically transform into a vertical, stacked view at 400% zoom. This update benefits users with low vision and those working across varied devices and environments.

</td></tr><tr><td>

Service Portal

</td><td>

-   **[Enable dark theme](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/service-portal/enable-dark-theme.md)**

Use the Dark theme in Service Portal to improve focus and provide better accessibility support. This option is commonly used to alleviate eye strain and improve readability.


-   ****

Add and edit more semantic tags within the Service Portal Designer to define key areas of a portal to support clearer navigation and descriptions for screen readers. This update helps users who are blind or have low vision by making it easier for assistive technology to identify and understand different sections of each page.


</td></tr><tr><td>

ServiceNow AI Platform core feature

</td><td>

Format Painter plugin for TinyMCE enables you to apply consistent font styles, sizes, and table formats within the HTML editor field. This improvement helps users with cognitive disabilities and low vision by reducing confusion and supporting clear, predictable formatting throughout documents. Keyboard navigation is supported, providing added ease of use for keyboard-only users. For more information, see [Configure the HTML toolbar](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-platform-administration/t_ConfigureTheTinyMCEHTMLToolbar.md).

</td></tr><tr><td>

Telecommunications Network Inventory

</td><td>

Improved overall accessibility across Network Inventory application, focusing on keyboard navigation, screen readers, zoom levels, colour contrast, and text spacing.

</td></tr><tr><td>

Third-party Risk Management

</td><td>

The Vendor Management Workspace and the third-party portal include accessibility improvements in this release, including improved color contrast, enhanced focus indicators, skip navigation links, full keyboard navigation, and ARIA attribute updates for screen reader compatibility.

</td></tr><tr><td>

UI Builder

</td><td>

The expanded drop-down menus for column properties can be ready by screen readers.

</td></tr></tbody>
</table>**Parent Topic:**[Release notes summaries for Australia features](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/release-notes-summaries.md)


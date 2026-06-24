---
title: Configure branding and theme
description: Using admin console, you can configure branding and data sources, internal and external search sources, conversational assistant configurations, canvas, and other features.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/employee-experience-foundation/eslate-config-admin-console.html
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [admin console, branding, themes, data sources, conversational assistant, canvas configuration, internal search, external search, Employee Slate]
breadcrumb: [Employee Slate for Now Assist, Configuration flow, Employee Slate, Unified Employee Experience, Employee Service Management]
---

# Configure branding and theme

Using admin console, you can configure branding and data sources, internal and external search sources, conversational assistant configurations, canvas, and other features.

## Before you begin

Before you configure Employee Slate for Now Assist, verify the following prerequisites:

-   You have the administrator role on the instance.
-   The Employee Slate for Now Assist foundational plugin is installed from the Product Hub page.
-   The Employee Slate Advanced plugin is installed if the deployment requires the advanced experience.
-   Now Assist is provisioned on the instance.

Role required: Administrator

## About this task

The Product Configuration console organizes the configuration work into modules and displays progress in the configuration summary. Data Sources and Conversational Assistant modules are specific to Now Assist deployments.

## Procedure

1.  Navigate to your Admin Home page on your instance.

    The system dynamically renders application and plugin cards based on your admin entitlement status.

2.  From the platform administrator home page, select **View product overview** on the Employee Slate for Now Assist card.

    The Product Hub page opens and lists the plugins associated with Employee Slate for Now Assist and links to documentation and release notes.

3.  Upload a prepared update set with the **Upload Batch** option.

    Use this option to reuse configurations exported from another environment.

4.  Select **Configure** to open the Product Configuration console.

5.  In the **Appearance** module, set the branding and theming for the experience.

    \[Omitted image "es-admin-console.png"\] Alt text: Configure branding and theme

    Set the portal name, URL suffix, light and dark mode logos, the favicon, and the primary, accent, and neutral palette colors. Preview the experience in desktop, mobile, light mode, and dark mode, then save and mark the module as configured.

6.  [Configure additional themes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/es-configure-multi-theme.md) based on your requirements.

7.  In the **Data Sources** module, configure the following internal search sources for the experience.

    1.  In the **Internal sources** module, configure the internal search sources for the experience.

        The internal sources list shows the default sources. Edit the conditions on an existing source, add an existing source that isn't yet linked to the search profile, or create a new internal source. Add, exclude, and map the fields per your requirements. For more information, see [Add internal search sources](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/eslate-add-internal-search.md).

    2.  In the **External sources** module, configure the external search sources for the experience.

        By default, the external sources aren't added. You can add an existing source that isn't yet linked to the search profile, or create a new external source by following on-screen instructions. For more information, see [Add external search sources](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/eslate-add-external-search.md).

8.  In the **Conversational Assistant** module, configure the chat header and the chat logo.

    You can go with one of the two options.

    -   \[Omitted image "es-admin-now-assistant-config.png"\] Alt text: conversational chat assistant now assist

        The module also offers a redirection to the Now Assist Assistant Designer admin console to configure advanced assistant behavior.

    -   \[Omitted image "es-mw-conversational-chat-selection.png"\] Alt text: conversational chat assistant moveworks

9.  In the **Canvas Configuration** module, configure the default canvas view and the widget library.

    -   Select **Edit default view** to configure the default canvas dashboard.
    -   Use the **Widget library** to toggle the visibility of widgets that employees can add to their personal canvas. You can also create widgets and add to the library.
10. In the **Documentation** module, go to **Documentation and references** for an overview of resources.

    Review and learn from product documentation reference content.

11. Select **Mark as configured** for each completed configuration section in the Admin Console.

    This action records that you reviewed and configured the section, and updates the overall completion status.

12. Select **Package and download** to export the configuration updates as an XML update set.

    Upload the exported file on the Product Hub page of another environment to promote configurations from a lower environment to production.


## Result

Employee Slate portal is configured with your organization branding and is ready for employee access.

## What to do next

Sign in as a non-administrator employee, open Employee Slate in a browser session. Verify that the branding, content, and conversational assistant work as expected.


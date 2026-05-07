---
title: Configure Employee Slate for Moveworks
description: Configure Employee Slate for Moveworks from the Product Configuration console. Set branding, the Moveworks AI Assistant connection, the canvas configuration, and the update set package that promotes configurations between environments.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-04-28"
reading_time_minutes: 3
keywords: [Employee Slate for Moveworks, Product Configuration console, Conversational Assistant, Canvas configuration, update set package]
breadcrumb: [Employee Slate for Moveworks, Employee Slate setup flow, Employee Slate, Employee Service Management]
---

# Configure Employee Slate for Moveworks

Configure Employee Slate for Moveworks from the Product Configuration console. Set branding, the Moveworks AI Assistant connection, the canvas configuration, and the update set package that promotes configurations between environments.

## Before you begin

Before you configure Employee Slate for Moveworks, verify the following prerequisites:

-   You have the System administrator role.
-   The Employee Slate for Moveworks foundational plugin is installed from the Product Hub page.
-   The Employee Slate Advanced plugin is installed if the deployment requires the advanced experience.
-   The Moveworks AI Assistant instance URL is available.

Role required: Admin

## About this task

The Product Configuration console organizes the configuration work into modules and displays progress in the configuration summary. You can leave and resume the configuration at any time. For the Moveworks chat bot connection step in detail, see [Configure the Moveworks chat bot for Employee Slate](empworks-configure-moveworks-chatbot.md).

## Procedure

1.  From the platform administrator home page, select **View product overview** on the Employee Slate for Moveworks card.

    The Product Hub page opens and lists the plugins associated with Employee Slate for Moveworks.

2.  Upload a prepared update set with the **Upload Batch** option.

    Use this option to reuse configurations exported from another environment. Skip this step to configure the instance from scratch.

3.  Select **Configure** to open the Product Configuration console.

    The configuration summary lists the modules available for Employee Slate for Moveworks and the progress of each module.

4.  In the **Appearance** module, set the branding and theming for the experience.

    Set the portal name, URL suffix, light and dark mode logos, and favicon. Set the primary, accent, and neutral palette colors. Use the preview panel to verify the experience in desktop and mobile, and in light and dark mode, before you save.

    Save the changes and mark the module as configured.

5.  In the **Conversational Assistant** module, enter the Moveworks AI Assistant instance URL and save the configuration.

    The page also offers a redirection to the Moveworks setup experience so you can further configure AI Assistant sources and behaviors. For the chat bot procedure, see [Configure the Moveworks chat bot for Employee Slate](empworks-configure-moveworks-chatbot.md).

6.  In the **Canvas** module, configure the default canvas view and the widget library.

    Select **Canvas Editor** to configure the default canvas dashboard. Use the widget library to toggle the visibility of widgets that employees can add to their personal canvas. You can also edit or create widgets from the library. For the full procedure, see [Configure the default canvas dashboard](eslate-configure-canvas.md).

7.  In the **Documentation** module, review the links to Employee Slate documentation for home page, inbox, org chart, notifications, and employee profile.

    Links open the ServiceNow documentation site in a new tab. Use the documentation to complete feature-specific configurations that aren't part of the Product Configuration console.

8.  Select **Package and download** to export the configuration changes as an XML update set.

    Upload the exported file from the Product Hub page of another environment with the **Upload Batch** option. Use this export to promote configurations from a lower environment to production.


## Result

Employee Slate for Moveworks is configured with the branding, Moveworks AI Assistant connection, canvas layout, and widget library that you set. Employees can open the configured portal and interact with the Moveworks AI Assistant.


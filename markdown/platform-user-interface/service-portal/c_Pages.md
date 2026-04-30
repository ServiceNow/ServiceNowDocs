---
title: Creating portal pages
description: Use pages to organize content, ensure responsive mobile optimization, and design meaningful portal user experiences for your customers. A page houses containers and rows, which then contain widgets. By manipulating the layout of the page, and the widgets within it, you can construct your desired user experience.
locale: en-US
release: yokohama
product: Service Portal
classification: service-portal
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Configuring Service Portal, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Creating portal pages

Use pages to organize content, ensure responsive mobile optimization, and design meaningful portal user experiences for your customers. A page houses containers and rows, which then contain widgets. By manipulating the layout of the page, and the widgets within it, you can construct your desired user experience.

-   Pages are referenced using the page ID.
-   Pages can be referenced in more than one portal.
-   Use base system pages as templates.

## Page layout

![Page highlighting the different layouts on the page including page, container, row, column, and widget](../image/ColumnRowWidgetLayout.png)

## Containers

Containers are markup artifacts that are put on a page to contain the layouts that house the widgets.

You can view containers and how they make up a page in the Service Portal Designer \(**Service Portal** &gt; **Service Portal Configuration** &gt; **Designer**\). Open a page in the Service Portal Designer, then click anything on the page. In the top left corner, breadcrumbs appear to show you which element on the page you have selected. Use the breadcrumbs to select a container, then click the edit icon \(![Edit icon from the top of the Service Portal Designer](../image/IconEditOption.png)\).

![Cool clocks widgets with a widget selected and the breadcrumbs at the top of the page highlighted](../image/ContainerBreadCrumbs.png "Service Portal Designer breadcrumbs")

You can also edit a container by navigating to the Page Editor and selecting the container node in the tree view. In this view, you can:

-   Change the layout of widgets on a page.
-   Determine the number of columns on a page.
-   Determine whether to scale with changes to the browser window.
-   Add a background color to a portion of a page.
-   Add an background image to a portion of a page.
-   View the current layout of the widgets within the page.

-   **[Create and edit a page using the Service Portal Designer](../task/t_ConfigureAPage.md#)**  
Create or edit a page and use layouts to organize the columns that house the widgets.
-   **[Standard ticket page](standard-ticket-page.md)**  
Configure individual request types to display the request-specific information, while still having a consistent layout that is similar to other request types. This configuration ensures a consistent experience when viewing submitted requests.
-   **[Redirect a reference to a page ID](../task/reroute-page.md)**  
Redirect all references from Service Portal widgets to route to a new page with a single record to avoid manually replacing the hard-coded page ID in widgets.
-   **[Attaching files to records from portal pages](../task/attaching-files-portal-pages.md#)**  
Attachments can be added to records from portal pages by navigating the file system, pasting files from the clipboard, or dragging and dropping files.

**Parent Topic:**[Service Portal](c_ServicePortal.md)


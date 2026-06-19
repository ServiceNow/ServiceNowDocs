---
title: Creating portal pages
description: Use pages to organize content, ensure responsive mobile optimization, and design meaningful portal user experiences for your customers. A page houses containers and rows, which then contain widgets. By manipulating the layout of the page, and the widgets within it, you can construct your desired user experience.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-user-interface/service-portal/c\_Pages.html
release: australia
product: Service Portal
classification: service-portal
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configuring Service Portal, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Creating portal pages

Use pages to organize content, ensure responsive mobile optimization, and design meaningful portal user experiences for your customers. A page houses containers and rows, which then contain widgets. By manipulating the layout of the page, and the widgets within it, you can construct your desired user experience.

-   Pages are referenced using the page ID.
-   Pages can be referenced in more than one portal.
-   Use base system pages as templates.

## Page layout

\[Omitted image "ColumnRowWidgetLayout.png"\] Alt text: Page highlighting the different layouts on the page including page, container, row, column, and widget

## Containers

Containers are markup artifacts that are put on a page to contain the layouts that house the widgets.

You can view containers and how they make up a page in the Service Portal Designer \(**Service Portal** &gt; **Service Portal Configuration** &gt; **Designer**\). Open a page in the Service Portal Designer, then click anything on the page. In the top left corner, breadcrumbs appear to show you which element on the page you have selected. Use the breadcrumbs to select a container, then click the edit icon \(\[Omitted image "IconEditOption.png"\] Alt text: Edit icon from the top of the Service Portal Designer\).

\[Omitted image "ContainerBreadCrumbs.png"\] Alt text: Cool clocks widgets with a widget selected and the breadcrumbs at the top of the page highlighted

You can also edit a container by navigating to the Page Editor and selecting the container node in the tree view. In this view, you can:

-   Change the layout of widgets on a page.
-   Determine the number of columns on a page.
-   Determine whether to scale with changes to the browser window.
-   Add a background color to a portion of a page.
-   Add an background image to a portion of a page.
-   View the current layout of the widgets within the page.

-   **[Create and edit a page using the Service Portal Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/service-portal/t_ConfigureAPage.md)**  
Create or edit a page and use layouts to organize the columns that house the widgets.
-   **[Standard ticket page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/service-portal/standard-ticket-page.md)**  
Configure individual request types to display the request-specific information, while still having a consistent layout that is similar to other request types. This configuration verifies a consistent experience when viewing submitted requests.
-   **[Redirect a reference to a page ID](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/service-portal/reroute-page.md)**  
Redirect all references from Service Portal widgets to route to a new page with a single record to avoid manually replacing the hard-coded page ID in widgets.
-   **[Attaching files to records from portal pages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/service-portal/attaching-files-portal-pages.md)**  
Attachments can be added to records from portal pages by navigating the file system, pasting files from the clipboard, or dragging and dropping files.

**Parent Topic:**[Configuring Service Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/service-portal/configuring-service-portal.md)


---
title: Understanding Service Portal
description: Service Portal provides a modular user interface framework for quick and easy building of application portals and dashboards for the platform. It helps developers and non‑technical administrators create attractive and engaging user experiences that drive employee adoption of critical enterprise applications.
locale: en-US
release: yokohama
product: Service Portal
classification: service-portal
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Exploring Service Portal, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Understanding Service Portal

Service Portal provides a modular user interface framework for quick and easy building of application portals and dashboards for the platform. It helps developers and non‑technical administrators create attractive and engaging user experiences that drive employee adoption of critical enterprise applications.

## How to use Service Portal

Service Portal is an application included in the platform UI, however it includes a visual layer for you to do most of your configuration. In the application navigator, navigate to **Service Portal** &gt; **Service Portal Configuration** to view the configuration page.

The Service Portal configuration page provides a unique, intuitive way of viewing all the pieces of your portal and how they interact with one another. The configuration page allows you to take advantage of a real-time preview, while configuring portal settings. Use each of the tiles on the configuration homepage to assemble the different components of your portal.

If you prefer the platform layout for configuring Service Portal, you still have the option of creating your portal components within the platform UI. The two options are not separate. Everything you create in the Service Portal configuration page also appears in a table in the platform UI.

## Who can use Service Portal

Several different kinds of users can configure a portal.

-   Limited coding: Service Portal was designed so that even users with limited coding ability or knowledge of the platform UI could set up a portal.
-   ServiceNow Experts: Users with an understanding of the ServiceNow platform can create portals, set up URL redirects, and view all the components of the portal in a table. Most portal configuration takes place in the Service Portal configuration page, but in specific circumstances, Service Portal administrators may need to do additional configuration directly within the platform.
-   Developers: Advanced customizations and new widget creation are tasks for a developer or someone who understands AngularJS and Twitter bootstrap.

In all cases, the user configuring a portal must have the **admin** or **sp\_admin** role.

## Basic concepts

You should have a basic understanding of all the following components that make up a portal:

-   [Themes](c_BrandingEditor.md): Themes define the look and feel of the whole portal, but can be overridden by other style configurations.
-   [Pages](c_Pages.md): Pages control where and how you store portal content. Pages do not have a defined relationship to portal records, they simply exist.
-   [Widgets](service-portal-widgets.md): Components in Service Portal are called widgets. You can use HTML templates, CSS, client scripts, server scripts, and any JavaScript dependencies to define what a widget does. From an AngularJS standpoint, widgets are essentially a superset of an Angular directive.
-   Most of the data in Service Portal is managed in different locations throughout the system.

    For example, if you are building a knowledge portal, the data exists in Service Portal, but the knowledge articles are authored and managed in the Knowledge application. The same is true for any other type of content you plan to leverage. Take time to understand which tables contain and control the data you are working with in Service Portal.


## Before you begin

Take the following into consideration before configuring Service Portal:

-   Who are you building your site for and why?
-   What information do you want to include in your site?
-   What do you want the mobile experience to be for users?
-   Which platform applications do you plan to use in your portal?

    You can use parts of the platform, such as knowledge articles and catalog items, as the content for your portal.

    For example, if you are building a knowledge portal, the content displays in Service Portal, but the knowledge articles are authored and managed in the Knowledge application. The same is true for any other type of content you plan to leverage. It is important to take time to understand the table structure of data to become acquainted with content.

-   How customized is your service catalog? Catalog client scripts and UI policies only work in Service Portal if they use the [mobile GlideForm API](https://developer.servicenow.com/app.do#!/api_doc?v=istanbul&id=c_MobileGlideForm_API), so you may need to make some changes.

## Additional resources

Service Portal is built using several well known technologies. Use the following websites as resources to help you understand and configure your portal:

-   [Twitter Bootstrap](http://getbootstrap.com/css/#grid)
-   [CSS 3 Flexbox](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)
-   [AngularJS](https://docs.angularjs.org/guide)

-   **[Service Portal core concepts](c_CoreConcepts.md)**  
Service Portal contains two parts: a framework and a portal. The framework is composed of a set of APIs, Angular services, directives, and tools that help to build portals. The portal is a group of pages linked by page IDs.
-   **[Service Portal configuration page](service-portal-configuration-page.md)**  
Most Service Portal configuration is accessible through the Service Portal configuration page landing page.
-   **[Page navigation in Service Portal by URL](navigate-by-portal-url.md)**  
You can navigate to a portal or a page in Service Portal using a URL.
-   **[Content Management and Service Portal](c_CMSAndSP.md)**  
Service Portal is a compelling alternative to the Content Management System \(CMS\) with a refined user experience. It does not duplicate CMS or platform UI functionality. Users who have sophisticated experiences delivered through CMS may need to invest time into transitioning to Service Portal, especially if the CMS implementation includes complex and customized Service Catalog forms.

**Parent Topic:**[Exploring Service Portal](exploring-service-portal.md)


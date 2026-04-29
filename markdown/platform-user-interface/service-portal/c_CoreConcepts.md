---
title: Service Portal core concepts
description: Service Portal contains two parts: a framework and a portal. The framework is composed of a set of APIs, Angular services, directives, and tools that help to build portals. The portal is a group of pages linked by page IDs.
locale: en-US
release: australia
product: Service Portal
classification: service-portal
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Understanding Service Portal, Exploring Service Portal, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Service Portal core concepts

Service Portal contains two parts: a framework and a portal. The framework is composed of a set of APIs, Angular services, directives, and tools that help to build portals. The portal is a group of pages linked by page IDs.

![Diagram of Service Portal and how pages and widgets fit inside it](../image/ServicePortalOverviewDiagram.png "Service Portal overview diagram")

After you enter a URL, the framework uses the suffix and picks the appropriate portal to determine the theme and configurations. Then it loads the configured default portal home page unless the URL has a specified ID.

Each widget added to a page becomes its own instance. A widget instance is basically the application of a widget in a page. Because widgets are reusable and can appear on different pages to do different things, a widget on a page is referred to as a Widget Instance. The page loads with content represented by widgets.

Widget instances get their logic from the base widget template, client scripts, server scripts, and depending on the widget, CSS.

**Parent Topic:**[Understanding Service Portal](sp-what-to-know.md)


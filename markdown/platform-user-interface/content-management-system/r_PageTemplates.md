---
title: Page templates
description: Every page that is part of the site needs a template.
locale: en-US
release: zurich
product: Content Management System
classification: content-management-system
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Content Management templates, Configure Content Management sites, Content Management System, Configure UIs and portals, Configure user experiences]
---

# Page templates

Every page that is part of the site needs a template.

## Critical page reference fields

When you build a new site, there are four page reference fields on the site record that are critical. Understanding these pages and how they are used helps you define page templates and site defaults.

-   Home page: landing page for the site. A home page is mandatory.
-   Search page: page that displays search results when a user searches from any page within the site. A search page is mandatory for your site to have a Search Results block.
-   Login page: a standalone login page, which is useful to force authentication for the entire CMS site.
-   Gauge target page: page used to display the drill-through content from a gauge. When the user clicks a gauge, the gauge target page opens showing the drill-through content for that gauge.

![CMS page reference fields](../image/CMSKeyPages.png "Critical page reference fields")

## Detail pages

Depending on the data or tables that you plan to use, you may need detail pages. These detail pages use one of the content types in the following list.

-   Knowledge detail page: displays a full knowledge article detail \(mandatory for a knowledge site\).
-   Incident page: detail page for an incident record.
-   Catalog page: detail page for all items, content items, order guides, and record producers.

## Templates for creating sections

There are two page templates you can use when creating sections:

-   Parent page: keeps sections within large sites organized and sortable on the site list of pages. Parent pages are also used to create breadcrumbs dynamically.
-   Detail page: differs from the parent page in that the content area displays a full article or detail instead of a selection of related content. Detail pages must have a Current Document block.

These pages are mandatory if you plan on accessing system data. For example, if you plan on showing the service catalog in your CMS, you need the following items.

-   A service catalog content type that references the \[sc\_cat\_item table\].
-   A detail page that provides the full view of the item.

## New templates

If the base system sample site pages are not suitable, you can create a template from scratch. Create a page and then use it as a template. For more information, see [Create a Content Page](../task/t_CreateAContentPage.md).

When you save a new template, include the word "template" in the page name.

**Parent Topic:**[Content Management templates](../concept/c_ContentManagementTemplates.md)


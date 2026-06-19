---
title: Configure a base template
description: An easy way to create a base template is to copy the existing ESS sample site and customize it to suit your own needs. You can also configure a base template from scratch.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-user-interface/content-management-system/t\_BuildAMasterTemplateStepByStep.html
release: australia
product: Content Management System
classification: content-management-system
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Content Management templates, Configure Content Management sites, Content Management System, Configure UIs and portals, Configure user experiences]
---

# Configure a base template

An easy way to create a base template is to copy the existing ESS sample site and customize it to suit your own needs. You can also configure a base template from scratch.

## Before you begin

Role required: content\_admin or admin

## About this task

Follow these steps to create a single base page and generate all important components within the site.

## Procedure

1.  Design a layout.

    Regardless of the interface, a site can be distilled into a few simple layouts.

2.  Create a theme.

    The theme defines the structure of the layouts in CSS and the base styles, such as fonts and colors. For more information, see [Design themes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/content-management-system/c_DesignThemes.md).

3.  Build the common blocks.

    Pages are composed of content blocks. Most content blocks are reused on multiple pages. For the base template, create basic blocks such as a header, side navigation, and some basic content for the main content area of the page. More detailed content can be added later, but define content for reuse on many of the site pages here. For more information, see [Content blocks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/content-management-system/c_ContentBlocks.md).

4.  Build a site entry page.

    Use the common content blocks you just created to design the first page that users see when they enter the site. For more information, see [Create a content page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/content-management-system/t_CreateAContentPage.md).

5.  Build a detail page.

    Design the detail pages to determine how pages such as knowledge articles, catalog items, and search results are displayed. You can build a detail page by copying the site entry page and adding additional content blocks. For more information, see [Copy a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/content-management-system/t_CopyAPage.md).

6.  Assign the pages created to the new site.

    Create the site and apply the layout and theme to the site defaults. Then, navigate to the **All Pages** list and specify the base template site in the **Site** column for each of the base template pages. For more information, see [Create a site](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/content-management-system/t_CreateANewSite.md).


**Parent Topic:**[Content Management templates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/content-management-system/c_ContentManagementTemplates.md)


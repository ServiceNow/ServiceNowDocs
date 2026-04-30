---
title: Copy a site
description: To create a new site quickly, you can copy an existing site.
locale: en-US
release: yokohama
product: Content Management System
classification: content-management-system
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Content sites, Configure Content Management sites, Content Management System, Configure UIs and portals, Configure user experiences]
---

# Copy a site

To create a new site quickly, you can copy an existing site.

## Before you begin

Role required: content\_admin or admin

## About this task

The site copy option creates a complete standalone copy of the site and all its resources. If you are copying a site to create a second site, use this option after the first site is complete, tested, and production ready. This consideration is important because the blocks, CSS, and pages are duplicated to support the new site. There are various reasons why site copying is useful, such as site versioning, branding, or creating a backup.

Images are not included when you use the Copy Site option. They are stored separately in the sys\_attachments table.

To copy just a few pages without duplicating all the resources \(CSS, blocks, menus\), use the page copy option. Page copy duplicates the page but not the resources used in the page. For more information, see [Copy a page](t_CopyAPage.md).

## Procedure

1.  Navigate to **All** &gt; **Content Management** &gt; **Sites** &gt; **\[Site Name\]**.

2.  On the Site form, click **Copy**.

3.  In the dialog box that opens, type a name for the new site.

    This name is a prefix for all the site elements that are duplicated. Do not use **Portal** or **CMS** in the site name.

    A progress bar shows the copy process. When the process is complete, the Site form shows information for the new site.


**Parent Topic:**[Content sites](../concept/c_ContentSite.md)

**Related topics**  


[Create a site](t_CreateANewSite.md)


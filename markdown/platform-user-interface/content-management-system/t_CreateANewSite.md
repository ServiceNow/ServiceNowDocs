---
title: Create a site
description: Configure a site by either creating a new site with CMS or by editing a copy of either the ESS Portal or the Service Management Portal.
locale: en-US
release: australia
product: Content Management System
classification: content-management-system
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Content sites, Configure Content Management sites, Content Management System, Configure UIs and portals, Configure user experiences]
---

# Create a site

Configure a site by either creating a new site with CMS or by editing a copy of either the ESS Portal or the Service Management Portal.

## Before you begin

Role required: content\_admin or admin

## About this task

If you are creating a catalog site in CMS, see Using the content management system with the service catalog.

## Procedure

1.  Navigate to **All** &gt; **Content Management** &gt; **Sites**.

2.  Click **New**.

3.  Complete the form.

    Since you have not yet created pages, you cannot select the Home, Search, Login, and Gauge target pages. Add them to the site record after you create them.

<table id="table_nfp_txv_wp"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

A unique name for the site.

</td></tr><tr><td>

URL suffix

</td><td>

The URL suffix that identifies the site. The URL suffix is case-sensitive, the suffix you enter impacts the CMS site URL used to launch the site. It is incorporated into the URL as follows:`http://<instance name>.service-now.com/url_suffix/page.do`

 **Note:** Do not use `portal` and `cms` in the URL suffix. They are reserved terms and return a **Page not found** if you use them.

</td></tr><tr><td>

Home page

</td><td>

The page to display when the user does not specify a page name in their URL:`http://<instance name>.service-now.com/url_suffix/`

</td></tr><tr><td>

Search page

</td><td>

The page that displays search results when a user searches from any page within the site.

</td></tr><tr><td>

Login page

</td><td>

The page to use for logging in to the site. If specified, users must log in to access the pages on the site. If left blank, no login is required to access the pages within the site.

</td></tr><tr><td>

Gauge target page

</td><td>

The page that displays gauge content. When the user clicks a gauge on the new site, the gauge target page opens to show the gauge content. The gauge target page replaces the CMS page in the current tab.

</td></tr><tr><td>

Title

</td><td>

A title for the site. The title can be the same as or different from the **Name**.

</td></tr><tr><td>

Description

</td><td>

A full description of the site.

</td></tr><tr><td>

Default layout

</td><td>

The layout for pages to use by default. Any page in the site that has a blank **Layout** field uses the layout selected in this field.

</td></tr><tr><td>

Default theme

</td><td>

The theme for pages to use by default. Any page in the site that has a blank **Theme** field uses the theme selected in this field.

</td></tr><tr><td>

Simple catalog display

</td><td>

Selecting this option simplifies catalog pages in the site by hiding the search bar, breadcrumbs, and the results per page choice list. It also prevents you from adding attachments from record producers to your CMS site.

</td></tr><tr><td>

Use external cart

</td><td>

Option to omit the default cart when rendering catalog pages within a site that contains catalog pages. Provide a [catalog cart block](../concept/c_CatalogCartBlock.md) somewhere on the site to allow users to make catalog requests.**Note:** If you use an external cart, the no cart check box on a service catalog item has no effect. The external cart appears for all items.

</td></tr></tbody>
</table>4.  Click **Submit**.


## Example

The following is the site record for the ESS Portal:![ESS Portal site record](../image/Site.png)

**Parent Topic:**[Content sites](../concept/c_ContentSite.md)

**Related topics**  


[Copy a site](t_CopyASite.md)


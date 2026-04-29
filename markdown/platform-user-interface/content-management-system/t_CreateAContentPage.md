---
title: Create a content page
description: Pages are built from content blocks and organized into sites.
locale: en-US
release: australia
product: Content Management System
classification: content-management-system
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Content pages in CMS, Configure Content Management sites, Content Management System, Configure UIs and portals, Configure user experiences]
---

# Create a content page

Pages are built from content blocks and organized into sites.

## Before you begin

Role required: content\_admin or admin

## Procedure

1.  Navigate to **All** &gt; **Content Management** &gt; **Sites**.

2.  Open the site to add the page.

3.  In the **Pages** related list, click **New**.

4.  Complete the form.

<table id="table_dgc_nvh_wq"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

A unique name for the page. Prefix each page name with the name of the site followed by a dash and the page function. For example, **ESS - Catalog Detail** and **ESS - Search Results** are page names within the **ESS** site.

</td></tr><tr><td>

URL suffix

</td><td>

The URL suffix that identifies the page. It is incorporated into the URL as follows: `http://instance name.service-now.com/site/url_suffix.do`

</td></tr><tr><td>

Parent page

</td><td>

The existing page that is the parent of the current page. Parent pages keep sections sortable on the site list of pages and are used to create breadcrumbs dynamically. Use CSS to define menus that give the Parent page context within the user interface.

</td></tr><tr><td>

Layout

</td><td>

The layout to use for the page. Layouts define dropzones where content blocks can be added to the page. If this field is left blank, the page inherits the default layout of the site. If the site does not have a default layout, there is a single dropzone for the entire page.

</td></tr><tr><td>

Content theme

</td><td>

The theme to use for the page. Themes bundle CSS style sheets that are applied to all content within the page.If this field is left blank, the page inherits the default theme of the site. Use the default theme unless the page requires a different set of CSS style sheets from the other pages in the site.

</td></tr><tr><td>

Frame buster

</td><td>

Select the check box to remove any restrictions placed by frames that contain the page. This way you avoid frame-within-frame issues that sometimes occur with improper linking.

</td></tr><tr><td>

Content site

</td><td>

The site associated with the content page. If you created the page from the related list in the site, the value defaults. The content site provides the &lt;site\_suffix&gt; in the page URL, as follows:`http://<instance name>.service-now.com/site_suffix/page_suffix.do`

</td></tr><tr><td>

Read roles

</td><td>

Users with the selected roles can view the page. Click the lock icon to select roles.

</td></tr><tr><td>

Model document

</td><td>

A document ID of a record to display by default.

</td></tr><tr><td>

Page status

</td><td>

The status for the page, such as **Draft** or **Published**.

</td></tr><tr><td>

Created by

</td><td>

The user who created the page. If your role has higher privileges than your user name and you enter your user name, the field defaults to the role. For example, if you are logged in as an Admin and you type your name, which has lower privileges, this field displays **Admin**.

</td></tr><tr><td>

Title

</td><td>

The title for the page. The title displays on the browser tab when the page is accessed.

</td></tr><tr><td>

Description

</td><td>

Type a description of the page that displays for users when they access the page.

</td></tr></tbody>
</table>5.  Click **Submit**.


**Parent Topic:**[Content pages in CMS](../concept/c_ContentPages.md)


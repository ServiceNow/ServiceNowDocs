---
title: iFrame methods
description: The following examples show how system records are pulled into an iFrame that is placed on a content page.
locale: en-US
release: yokohama
product: Content Management System
classification: content-management-system
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configure iFrames, Types of content blocks, Content blocks, Configure Content Management sites, Content Management System, Configure UIs and portals, Configure user experiences]
---

# iFrame methods

The following examples show how system records are pulled into an iFrame that is placed on a content page.

For system lists or forms, use the frame name **gsft\_main** so that links work properly.

-   **Order Hardware** is an example of linking to a catalog category.
    -   URL: `com.glideapp.servicecatalog_category_view.do?sysparm_parent=d258b953c611227a0146101fb1be7c31&sysparm_view=`
    -   Frame name: **gsft\_main**
-   **My Approvals List** is an example of linking to a list with a view filter and a JavaScript that reference the authenticated user.
    -   URL: `sysapproval_approver_list.do?sysparm_query=approver=javascript:getMyApprovals()&sysparm_view=ess`
    -   Frame name: **gsft\_main**
-   **Service Catalog Home Page \(system\)** references the system catalog page within the Service Catalog application. If you are satisfied with the way the catalog looks, this method is an easy way to bring the page into a CMS design.
    -   URL: `catalog_home.do?sysparm_view=catalog_default`
    -   Frame name: **gsft\_main**
-   **Problem Management Overview** references a homepage. `../` makes the URL string relative to system homepages. Without it, the URL string resolves to the default CMS homepage reference in the site.
    -   URL: `../home.do?sysparm_view=problem_overview`
    -   Frame name: **gsft\_main**

**Parent Topic:**[Configure iFrames](../task/t_IFrame.md)


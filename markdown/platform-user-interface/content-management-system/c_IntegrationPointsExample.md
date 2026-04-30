---
title: Example integration points
description: Each element on the page links to a specific URL point.
locale: en-US
release: yokohama
product: Content Management System
classification: content-management-system
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Content Management integration points, Content Management System, Configure UIs and portals, Configure user experiences]
---

# Example integration points

Each element on the page links to a specific URL point.

![Each element under the Business Services, Features Services, and Reporting sections has a specific URL link integration point.](../image/IntegrationPointsSmall.png "Integration points")

**Business Services** links to a content page \(CMS page referenced: Business Service Portfolio, URL: \(`business_service_category.do`\) that pulls the system service catalog homepage into a frame within the content area. Each link within this section uses the browse by category page, where you pass in the name of the category to return results.

-   Target page iFrame URL: `catalog_home.do?sysparm_nameofstack=aabdae07ef221000914304167b22567d&sysparm_view=business&sysparm_clear_stack=yes`
-   Target page frame name: `gsft_main`
    -   **Desktop Computing** URL: `category_browse.do?category=Desktop Computing`
    -   **Business Applications** URL: `category_browse.do?category=Business Applications`
    -   **Communications Services** URL: `category_browse.do?category=Communications Services`
    -   **Infrastructure Services** URL: `category_browse.do?category=Infrastructure Services`
    -   **Hosting Services** URL: `category_browse.do?category=Hosting Services`

**Featured Services** links to a content page which pulls a small subset of services into an iFrame.

-   iFrame URL: `com.glideapp.servicecatalog_category_view.do?sysparm_parent=d67c446ec0a80165000335aa37eafbc1&sysparm_view=`
-   Frame name: `gsft_main`
    -   **Install Software** URL: `catalog.do?uri=com.glideapp.servicecatalog_cat_item_view.do?sysparm_id=10d69689c611227600ffeba41c664824`
    -   **Email Account** URL: `catalog.do?uri=com.glideapp.servicecatalog_cat_item_view.do?sysparm_id=d67a86b6c0a80165009386c752cd4a09`
    -   **Electronic Messaging** URL: `catalog.do?uri=com.glideapp.servicecatalog_cat_item_view.do?sysparm_id=533798810a0a0b2600f1a03593e19058`
    -   **VPN RSA Token** URL:`catalog.do?uri=com.glideapp.servicecatalog_cat_item_view.do?sysparm_id=d67b099ac0a80165019d0c276b772502`
    -   **Shared Storage \(SAN\)** URL: `catalog.do?uri=com.glideapp.servicecatalog_cat_item_view.do?sysparm_id=cedd458a0a0a0b8300c3b1e32e7a3ac2`

**Reporting** links to a content page that pulls the reports page into an iFrame. All links within this menu leverage homepages in the system, which creates an issue with the home.do URL. Notice in the following links that ../ is used to create a relative URL outside of the CMS site home.do definition. Without this path, the site homepage would render within the iFrame.

-   iFrame URL: `report_home.do`
-   Frame name: `gsft_main`
    -   **Cost Management Overview** URL: `../home.do?sysparm_userpref_homepage=fa81ae91c0a805c64c0942ab2e4b852b`
    -   **Administration Overview** URL: .`./home.do?sysparm_userpref_homepage=8b7b11f6c611228901ff3fcfbdb3cc8f`
    -   **Portfolio Overview** URL: `catalog_home.do?sysparm_view=business`
    -   **Service Availability** URL: .`./home.do?sysparm_userpref_homepage=8ee772000a0a0bad00c38eb7e68b93d0`
    -   **Service Level Agreements \(SLA\)** URL: .`./home.do?sysparm_userpref_homepage=757e86a30a0006d4010a6851639498d1`

**Parent Topic:**[Content Management integration points](c_CMSIntegrationPoints.md)


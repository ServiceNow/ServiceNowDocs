---
title: Content Management and Service Portal
description: Service Portal is a compelling alternative to the Content Management System \(CMS\) with a refined user experience. It does not duplicate CMS or platform UI functionality. Users who have sophisticated experiences delivered through CMS may need to invest time into transitioning to Service Portal, especially if the CMS implementation includes complex and customized Service Catalog forms.
locale: en-US
release: zurich
product: Service Portal
classification: service-portal
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 6
breadcrumb: [Understanding Service Portal, Exploring Service Portal, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Content Management and Service Portal

Service Portal is a compelling alternative to the Content Management System \(CMS\) with a refined user experience. It does not duplicate CMS or platform UI functionality. Users who have sophisticated experiences delivered through CMS may need to invest time into transitioning to Service Portal, especially if the CMS implementation includes complex and customized Service Catalog forms.

## Service Portal compatibility with existing CMS sites

ServiceNow continues to support CMS in current and upcoming releases. If you have existing CMS sites and activate Service Portal on your instance, your CMS sites will continue to work, as CMS and Service Portal are separate applications.

## Differences between Service Portal and CMS

Service Portal is an alternative to CMS based on more modern technologies. Major differences include:

-   **Underlying technology**

    CMS uses Jelly, which is not a widely used technology. Service Portal instead uses [AngularJS](https://docs.angularjs.org/guide/introduction), server-side JavaScript, HTML, and CSS. Any scripts that use Jelly do not work in Service Portal. Building widgets in Service Portal requires knowledge of AngularJS.

-   **Visual layer**

    CMS uses iFrames which can be difficult to work with, limited in terms of styling, and susceptible to upgrade issues. Alternatively, Service Portal is a self-contained application that accesses data from other tables on the platform. This enables fine-tuned control over style and responsive design.

-   **Mobile first**

    Unlike CMS, Service Portal is optimized for a mobile environment. For this reason, the following apply to the Service Portal environment:

    -   Any scripts used in Service Portal can only use APIs supported in a mobile environment. For example, some APIs used in your Service Catalog client scripts may not be supported. For a list of supported APIs, see [Service Portal and client scripts](unsupported_client_scripts.md).
    -   Service Portal forms support a maximum of two-columns. As a result, any highly customized Service Catalog forms, such as catalog items and record producers that use containers and variable sets, must be simplified to work in a two-column layout.
    If transitioning to Service Portal, review the following resource: [Mobile client GlideForm \(g form\) scripting and migration](https://www.servicenow.com/docs/access?context=r_MobilePlatformMigrationImpacts&version=zurich&pubname=zurich-api-reference&ft:locale=en-US).


To understand how core CMS components are configured in Service Portal, refer to the following table.

<table id="table_oys_yth_cbb"><thead><tr><th>

CMS component

</th><th>

Service Portal equivalent

</th></tr></thead><tbody><tr><td>

Content site

</td><td>

[Portal](../task/create-a-portal.md)

</td></tr><tr><td>

Content page

</td><td>

[Page](c_Pages.md)

</td></tr><tr><td>

Content types

</td><td>

Content types link a table to a content page.

 In Service Portal, content types are no longer required. Record data is queried and displayed using base system widgets. You can add widgets to any number of Service Portal pages.

 Learn more: [Using portal widgets](service-portal-widgets.md).

</td></tr><tr><td>

Layout and dropzones

</td><td>

In Service Portal, pages are made up of containers, rows, and columns.

 Learn more: [Pages](c_Pages.md).

</td></tr><tr><td>

Content block

</td><td>

A content block is a reusable piece of content.

 In Service Portal, content blocks are replaced by widgets.

 Learn more: [Using portal widgets](service-portal-widgets.md).

</td></tr><tr><td>

Service Catalog

</td><td>

Service Catalog pages are rendered using the SC Catalog Item widget in Service Portal. For this reason, Service Catalog forms such as catalog items and record producers are shared between your CMS implementation and Service Portal. If you have a highly customized Service Catalog, you may need to invest time in simplifying your Service Catalog items and client scripts so that they render as expected in Service Portal.

 Learn more: [Service Catalog forms in Service Portal](sc-forms-in-sp.md).

</td></tr><tr><td>

Theme

</td><td>

[Theme](c_CustomCSS.md)

</td></tr><tr><td>

CSS

</td><td>

[CSS](portal-css.md)

</td></tr></tbody>
</table>## CMS and Service Catalog customizations

Service Portal comes with base system widgets to address common use cases and to display record data. Even though there is no direct migration path from CMS to Service Portal, there may be some items, such as catalog items or knowledge articles, that render as expected in Service Portal without any effort.

However, because Service Portal is supported in a mobile environment, you may need to modify any customized forms and scripts. This approach ensures that the items display well on a mobile device and present a better user experience. Before transitioning to Service Portal, you may need to:

-   Refactor client scripts used in your CMS/Service Catalog to use supported mobile APIs and global objects. For a list of supported APIs, see [Service Portal and client scripts](unsupported_client_scripts.md).
-   Build widgets to replace UI Macros and other unsupported scripts. If using a UI Macro in a catalog item form and referencing values on the form, you can use the following workaround instead: [Replace a Service Catalog form script with a widget](../task/ui-macro-widget.md).
-   Simplify any complex forms used in your Service Catalog to fit the Service Portal two-column form layout.
-   Consider which release supports the required functionality. You may want to upgrade your instance before transitioning to ensure that you have the required base system features.

-   **[CMS to Service Portal transition](cms-sp-migrate.md)**  
Your CMS may include complex forms and customizations that do not render as expected in Service Portal. Use this guide to understand how best to modify your CMS and Service Catalog implementation for Service Portal adoption, and to understand how a conversion may affect your users.

**Parent Topic:**[Understanding Service Portal](sp-what-to-know.md)


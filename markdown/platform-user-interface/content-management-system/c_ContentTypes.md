---
title: Content types
description: Content types provide site-specific control of how system data defined by templates is rendered.
locale: en-US
release: australia
product: Content Management System
classification: content-management-system
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configure Content Management sites, Content Management System, Configure UIs and portals, Configure user experiences]
---

# Content types

Content types provide site-specific control of how system data defined by templates is rendered.

In the site, one page displays a list of knowledge articles, and another page displays catalog items or incidents or a combination of the two. Different themes can be used for types of content and each theme can provide different user interaction. Content types define the pages that display content from a table. Each content type corresponds to a table.

Every type of document that the CMS displays has an associated content type. Changing the content type requires knowledge of Apache Jelly scripting. However, the common content types \(such as service catalog or knowledge base\) come in the base system. Content types can be associated with particular sites. This association allows different sites to use different detail pages for the same content type.

Content types define three features of associated documents.

-   What does a link to one of these documents look like? For example, if a list of these documents is displayed on a page, how does each entry appear?
-   What does a detailed view of one of these documents look like?
-   What detail page is used to display the document? This decision is important and is often an area of confusion for new CMS users.

The document content type determines the page that a list of documents points to, the list itself does not determine the page. The content from a link is displayed in a detail content block on a page. The content type determines in which detail block on a page the document content is displayed.

For example, the list block **Catalog Top 5** displays the top five items in the Service Catalog table \[sc\_cat\_item\]. Because the table is \[sc\_cat\_item\], the content type **sc\_cat\_item** controls how the **Catalog Top 5** list is displayed. Clicking any item in the list displays the Service Catalog Detail page with the item displayed on it according to the detail template script. These content types are applied:

-   in search results to link to the correct page.
-   in the Current Document block to display the current record.
-   in links on lists and other places that link to record types.

Several content types are available by default for tables such as Catalog Item \[sc\_cat\_item\], Gauge \[sys\_gauge\], and Page \[content\_page\].

Content type defaults that are set for CMS can be overridden for individual sites. Use the **Content Types** related list on the site record to customize content types.

-   **[Configure a content type](../task/t_CreateAContentType.md)**  
Users with the content\_admin role can create a content type.
-   **[CMS gauge support](c_CMSGaugeSupport.md)**  
Gauges are a graphical way to display information from an instance.
-   **[View content types](../task/t_ViewContentTypes.md)**  
The following is an example of where you might use Content Types.

**Parent Topic:**[Configure Content Management sites](../task/t_CreateASite.md)

**Related topics**  


[Content sites](c_ContentSite.md)

[Content pages in CMS](c_ContentPages.md)

[Content Management templates](c_ContentManagementTemplates.md)

[Content blocks](c_ContentBlocks.md)

[Style in Content Management](c_StyleInContentManagement.md)

[Content Management meta tags](c_ContentManagementMetaTags.md)


---
title: Dynamic methods
description: While static methods are a powerful navigational tool, you have more control over data rendering using the dynamic methods.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-user-interface/content-management-system/c\_DynamicMethods.html
release: australia
product: Content Management System
classification: content-management-system
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Content Management integration points, Content Management System, Configure UIs and portals, Configure user experiences]
---

# Dynamic methods

While static methods are a powerful navigational tool, you have more control over data rendering using the dynamic methods.

Reference common code in the system to make long-term maintenance of the site easier. Coding skills are useful when implementing dynamic methods.

\[Omitted image "Blocks.png"\] Alt text: The items in green denote dynamic method options the CMS module.

-   **Dynamic Blocks**

    These blocks are where the majority of your work resides. For more information, see [Configure dynamic blocks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/content-management-system/t_CreateADynamicBlock.md).

-   **Frames**

    Frames are meant to be decorative wrappers around any block in the system. They are mentioned with dynamic blocks because frames are essentially UI macros with the category of **Frame**. Frames apply the `${body}` variable to a block and define where the block is inserted when rendered on the page.

-   **Lists**

    Lists generate links to records based on the filtering rules you define. Lists can be sorted for presentation by any field in the corresponding record. Lists help supplement navigation and pull data from outside the CMS. For more information, see [Customize the list block](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/content-management-system/t_DefineTheListBlock.md).

-   **Content Types**

    Content types provide site-specific control of how system data defined as templates is rendered. The rendering of lists is considered first \(summary templates\). The next consideration is the detail template, which allows control over the record rendering.

-   **List Definitions**

    List definitions enable you to extend the summary template defaults defined on the site level. Used with [frames](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/content-management-system/c_StyleInContentManagement.md), list definitions render the same data differently based on the placement on the page or site. For more information, see [Configure list definitions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/content-management-system/t_ConfigureListDefinitions.md).

-   **Detailed Content**

    Detailed content in page detail settings\) are blocks that display the content of an existing document as a block on a content page. For more information, see [Configure a detailed content block](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/content-management-system/t_DetailedContentBlock.md).


**Parent Topic:**[Content Management integration points](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/content-management-system/c_CMSIntegrationPoints.md)


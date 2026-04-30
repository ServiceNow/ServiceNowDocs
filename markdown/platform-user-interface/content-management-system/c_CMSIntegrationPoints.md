---
title: Content Management integration points
description: Integration points use content blocks in CMS to link different applications together using static and dynamic methods.
locale: en-US
release: yokohama
product: Content Management System
classification: content-management-system
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Content Management System, Configure UIs and portals, Configure user experiences]
---

# Content Management integration points

Integration points use content blocks in CMS to link different applications together using static and dynamic methods.

By using integration points, users can connect to different systems from a single page. The power of the CMS is that it can display any data within the ServiceNow platform. The ESS portal, for example, connects users to a service catalog, a knowledge base, and a help and incident reporting site. Each section contains a set of links to additional content. List blocks offer the easiest way to display data dynamically. Content types define how lists link to the detailed data they reference.

Generating lists from the ServiceNow platform is straightforward, especially if you use filtering. When the CMS was first introduced, lists were the only method available to create navigational systems for sites. Content types define system record links using specific templates to define the list and the details.

-   Summary template: defines the list
-   Detail template: defines the detail as it is rendered in a page.

The templates work together to pass data attributes or [Unique record identifier \(sys\_id\)](https://www.servicenow.com/docs/access?context=c_UniqueRecordIdentifier&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US) \(sysid\) into a single detail page that manages the data. Any attribute variations use the URL sent to the page.

Understanding how content types work can mean the difference between a site with 20 pages versus a site with 200 pages. There is a time for both types of data calls. Depending on the task, there are appropriate times to use static content and times for dynamic methods.

-   **[View links between system elements and URLs](../task/t_LinkToContent.md)**  
You can view the links between your system elements and their URLs to render more specific content within your site.
-   **[Static methods](c_StaticMethods.md)**  
Static methods in the CMS application were created for ease of use.
-   **[Dynamic methods](c_DynamicMethods.md)**  
While static methods are a powerful navigational tool, you have more control over data rendering using the dynamic methods.
-   **[Example integration points](c_IntegrationPointsExample.md)**  
Each element on the page links to a specific URL point.

**Parent Topic:**[Content Management System](c_ContentManagementSystem.md)

**Related topics**  


[Content Management design](c_ContentManagementPlanning.md)

[Domain separation and the Content Management System](domain-separation-content-management.md)

[Configure Content Management sites](../task/t_CreateASite.md)

[Content Management testing](c_ContentManagementTesting.md)

[Global search in Content Management](c_UseGlobalSearchContentManagement.md)

[CMS translation](c_CMSTranslation.md#)


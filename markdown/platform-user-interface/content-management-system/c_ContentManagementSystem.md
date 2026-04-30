---
title: Content Management System
description: The Content Management System \(CMS\) is a ServiceNow application that enables users to create a custom interface for the ServiceNow platform and ServiceNow applications.
locale: en-US
release: xanadu
product: Content Management System
classification: content-management-system
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Configure UIs and portals, Configure user experiences]
---

# Content Management System

The Content Management System \(CMS\) is a ServiceNow application that enables users to create a custom interface for the ServiceNow platform and ServiceNow applications.

**Important:** Use Service Portal for new development instead of CMS. Service Portal is an alternative to CMS with a refined user experience, and is active by default in the base system. For more information, see [Service Portal](../../../build/service-portal/concept/c_ServicePortal.md) and [Content Management and Service Portal](../../../build/service-portal/concept/c_CMSAndSP.md).

A CMS typically requires a systems administrator or a web developer to set up and add features. Non-technical users can use the CMS application as a tool for website maintenance. You also want to consider the timing of the addition of content management, and the maturity level of ServiceNow data. For more information, see [CMS Planning](c_ContentManagementPlanning.md).

Following are several CMS project ideas:

-   Design a company-wide service catalog that offers a collection of services.
-   Present a customized UI for a knowledge base.
-   Create customized login pages, search pages, views of lists, tables, charts, or graphs.
-   Design a complete website.
-   Integrate ServiceNow with other company applications.
-   Build a tailored self-service portal for end users that is in compliance with a corporate style guide.

## Example CMS sites

There are two common interface approaches within the ServiceNow community:

-   An image and text-based interface similar to Amazon.com
-   A search-based interface similar to Google

Both approaches have been used successfully. The approach you select depends on the needs of the people using the data and how easy it is to train them. While the two design philosophies are different, both approaches share the common goal of UI simplicity.

-   **[Content Management design](c_ContentManagementPlanning.md)**  
Before building a website in the CMS, it is important to have a good understanding of what to build and who the audience is.
-   **[Domain separation and the Content Management System](domain-separation-content-management.md)**  
Domain separation is supported in the Content Management System. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
-   **[Configure Content Management sites](../task/t_CreateASite.md)**  
Planning a CMS site involves obtaining resources, communicating with others about design, and gathering content.
-   **[Content Management integration points](c_CMSIntegrationPoints.md)**  
Integration points use content blocks in CMS to link different applications together using static and dynamic methods.
-   **[Content Management testing](c_ContentManagementTesting.md)**  
Test your site to ensure that all pages display correctly, links go to the specified address, and images are not broken. It is important to test the site as you build it. Do not wait until just before launch to begin testing.
-   **[Global search in Content Management](c_UseGlobalSearchContentManagement.md)**  
When you add global search to a CMS site, two different search result blocks can display, depending on the user role: global or no global.
-   **[CMS translation](c_CMSTranslation.md#)**  
You can translate CMS sites by activating internationalization plugins and manually translating custom interface strings.

**Parent Topic:**[Configure UIs and portals](../../general/concept/configure-uis-and-portals.md)


---
title: System user guide
description: The system user guide enables you to create end user help documentation that is specific to the policies and procedures of your organization. A default help page is provided in the base system that displays Core UI help documents for system navigation and other basic operations.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [User interface configuration, Working in Core UI, Configure UIs and portals, Configure user experiences]
---

# System user guide

The system user guide enables you to create end user help documentation that is specific to the policies and procedures of your organization. A default help page is provided in the base system that displays Core UI help documents for system navigation and other basic operations.

The user guide provides the tools for designing help portal pages containing feature-specific help documents. You can create custom help pages and deploy them in various ways using controls in the system. User guide documents are grouped in relevant sections on a help page, using a two-column format. You can display the sections and the documents within them in any order. You can display a section on more than one help page. The user guide is supported in Core UI .

A default help page is provided in the base system that displays help documents for system navigation and other basic operations. This page is accessible from the help icon in the header bar for Core UI users. To make this page available to users of other supported UI versions, you must create a [programmatic entry point](../reference/r_UserGuidePageEntryPoints.md).

**Note:** The default help page can be used as a template for your own help content. To personalize pages, sections, or documents in the User Guide, simply edit the ServiceNow® records to suit your needs. Remember that any records you customize are not updated when you upgrade your instance to a new version. Review any changes on a development system first and then decide whether to accept the updated content into your customized User Guide.

![Basic user guide help page](../image/UserGuideBasicPage.png "Basic user guide help page")

-   **[Create user guide help](../task/t_CreateUserGuideHelpDocuments.md)**  
User guide help documents are grouped in appropriate sections on the page and listed in a configurable order. Add your sections to a help page.
-   **[User guide help URLs](../reference/r_UserGuidePageEntryPoints.md)**  
You can create entry points in your instance for help generated with the system user guide by providing the correct address parameters in the target URL.

**Parent Topic:**[User interface configuration](../../core-configuration/concept/p_NavigationAndUIConfiguration.md)


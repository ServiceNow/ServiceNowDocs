---
title: Search sources
description: Configure internal and external search sources to expand the knowledge base available to Now Assist in Employee Slate. Search sources determine what content users can access through conversational search.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/employee-service-management/employee-experience-foundation/eslate-add-search-sources.html
release: zurich
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: concept
last_updated: "2026-04-24"
reading_time_minutes: 2
keywords: [search sources, ServiceNow Otto, Employee Slate, AI Search, conversational search]
breadcrumb: [Working with EmployeeWorks capabilities, ServiceNow EmployeeWorks Web App, Unified Employee Experience, Employee Service Management]
---

# Search sources

Configure internal and external search sources to expand the knowledge base available to Now Assist in Employee Slate. Search sources determine what content users can access through conversational search.

Search sources define the content that Now Assist can access when responding to employee queries. By configuring search sources, you expand the knowledge base beyond default ServiceNow content to include external systems, knowledge bases, and custom data sources.

## Types of search sources

Employee Slate supports multiple types of search sources to provide comprehensive information access:

-   **Internal ServiceNow sources**

    Knowledge articles, catalog items, service portal content, and other ServiceNow records that employees commonly need to access.

-   **External content connectors**

    Third-party systems such as SharePoint, Confluence, file shares, and other enterprise content repositories.

-   **Custom indexed sources**

    Specialized content sources configured for specific organizational needs, including custom tables and external APIs.


## Search configuration workflow

Setting up search sources involves several configuration steps:

-   Define indexed sources: Configure what content gets indexed for search.
-   Create search sources: Apply filters and access controls to indexed content.
-   Configure search profiles: Group search sources and define search behavior.
-   Link to Now Assist: Connect search profiles to the assistant.

## Access control and security

Search sources respect ServiceNow security models and role-based access controls. Users only see search results for content they have permission to access. This helps protect sensitive information while providing relevant search results.

Configure user criteria and role-based filters to control which employees can access specific search sources such as HR documents, financial information, and other confidential content.

## Performance and indexing

Search source performance depends on proper indexing configuration and content volume. Consider these factors when adding search sources:

-   Index only necessary content to maintain search performance
-   Schedule indexing during off-peak hours for large content sources
-   Monitor search analytics to identify popular content and optimize accordingly
-   Use content filters to exclude outdated or irrelevant information

## Benefits of expanded search sources

With comprehensive search source, you can:

-   Locate information through conversational queries
-   Reduce support ticket volume through self-service request resolution
-   Access enterprise knowledge consistently across different systems
-   Unify information access across enterprise systems in a single interface

**Related topics**  


[Add internal search sources](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/employee-experience-foundation/eslate-add-internal-search.md)

[Add external search sources](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/employee-experience-foundation/eslate-add-external-search.md)


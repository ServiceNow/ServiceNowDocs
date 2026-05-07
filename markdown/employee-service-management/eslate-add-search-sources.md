---
title: Search sources for Employee Slate
description: Configure internal and external search sources to expand the knowledge base available to Now Assist in Employee Slate. Search sources determine what content users can access through conversational search.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-04-24"
reading_time_minutes: 2
keywords: [search sources, Now Assist, Employee Slate, AI Search, conversational search]
breadcrumb: [Working with Employee Slate capabilities, Employee Slate, Employee Service Management]
---

# Search sources for Employee Slate

Configure internal and external search sources to expand the knowledge base available to Now Assist in Employee Slate. Search sources determine what content users can access through conversational search.

Search sources define the content that Now Assist can access when responding to employee queries in Employee Slate. By configuring search sources, you expand the knowledge base beyond default ServiceNow content to include external systems, knowledge bases, and custom data sources.

## Types of search sources

Employee Slate supports multiple types of search sources to provide comprehensive information access:

-   **Internal ServiceNow sources**

    Knowledge articles, catalog items, service portal content, and other ServiceNow records that employees commonly need to access.

-   **External content connectors**

    Third-party systems such as SharePoint, Confluence, file shares, and other enterprise content repositories.

-   **Custom indexed sources**

    Specialized content sources configured for specific organizational needs, including custom tables and external APIs.


## Search configuration workflow

Setting up search sources for Employee Slate involves several configuration steps:

-   Define indexed sources: Configure what content gets indexed for search.
-   Create search sources: Apply filters and access controls to indexed content.
-   Configure search profiles: Group search sources and define search behavior.
-   Link to Now Assist: Connect search profiles to the Employee Slate assistant.

## Access control and security

Search sources respect ServiceNow security models and role-based access controls. Users only see search results for content they have permission to access. This ensures that sensitive information remains protected while providing relevant search results.

Configure user criteria and role-based filters to control which employees can access specific search sources. This is particularly important for HR documents, financial information, and other confidential content.

## Performance and indexing

Search source performance depends on proper indexing configuration and content volume. Consider these factors when adding search sources:

-   Index only necessary content to maintain search performance
-   Schedule indexing during off-peak hours for large content sources
-   Monitor search analytics to identify popular content and optimize accordingly
-   Use content filters to exclude outdated or irrelevant information

## Benefits of expanded search sources

Adding comprehensive search sources to Employee Slate provides several advantages:

-   Employees find information faster through conversational queries
-   Reduced support ticket volume as employees self-serve more effectively
-   Consistent access to enterprise knowledge across different systems
-   Improved employee experience with unified information access

**Related topics**  


[Add internal search sources](../task/eslate-add-internal-search.md)

[Add external search sources](../task/eslate-add-external-search.md)


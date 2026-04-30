---
title: SharePoint Online Search Connector prerequisites
description: The ServiceNow SharePoint Online Search Connector offers a consumer-grade search configuration to manage your information resources.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [SharePoint Online Search Connector, Employee Service Management]
---

# SharePoint Online Search Connector prerequisites

The ServiceNow SharePoint Online Search Connector offers a consumer-grade search configuration to manage your information resources.

**Important:** Starting with the Yokohama release, SharePoint Online Search Connector is being prepared for future deprecation. It is hidden and no longer activated on new instances but continue to be supported. For deprecation details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184) article in the Now Support knowledge base.

For detailed instructions on how to get started with **External Content Connectors**, see

-   [External Content Connectors](https://www.servicenow.com/docs/access?context=ext-cont-connectors-landing-page&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).
-   [Exploring External Content Connectors](https://www.servicenow.com/docs/access?context=exploring-ext-cont-connectors&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).
-   [Configuring External Content Connectors](https://www.servicenow.com/docs/access?context=configuring-ext-cont-connectors&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

As search is the key to productivity, SharePoint Online Search Connector \(SPOC\) helps your employees to search and discover content from the ServiceNow employee experience.

## How SharePoint Online Search Connector works

Here’s an overview of how SharePoint Online Search Connector works:

![SharePoint Online Search Connector flow](../image/spoc-sharepoint-overview.png "SPOC overview")

Use the SharePoint Online Search Connector to:

-   Create better search and discovery experiences for the Microsoft SharePoint content, confirming that your employees can quickly find the information they need.
-   Enable support across multiple channels like Employee Service Management, Service Portal, Now Mobile app, and Virtual Agent.
-   Integrate with the ServiceNow® AI Search for improved relevance and personalization.
-   Search and find relevant information and drive business outcomes.

## Required plugins

Activate the following plugins and apps:

-   Employee Center Pro
-   Microsoft SharePoint spoke
-   AI Search spoke
-   Microsoft Entra ID spoke

Verify that the AI Search engine is enabled. External Content for the AI Search plugin \(com.glide.ais.external\_content\) must have a ServiceNow subscription.

For more information, see [Setting up SharePoint Online Search Connector](setup-sp-ovrvw.md#).

## Things to remember

-   The SharePoint Online Search Connector is only compatible with the AI Search engine, not with the Zing search engine.
-   The content types supported by the AI Search engine, such as, DOTX, HTM, XLSX, DOT, PPTM, DOCX, PPTX, TXT, PDF, POT, PPT, POTX, DOC, HTML, and XLS are supported in SharePoint Online Search Connector along with ASPX.
-   The AI Search file size up to 25 MB is applicable.
-   The languages supported are English, Spanish, French, Japanese, and German.
-   SharePoint Online Search Connector supports SharePoint groups The groups are **Members**, **Owners**, and **Visitors**. The groups have different permission levels.
    -   **Members**: Can edit a document residing in the site.
    -   **Owners**: Can create, edit, and delete documents residing in the site.
    -   **Visitors**: Can read a document residing in the site.
-   SharePoint Online Search Connector is enabled to read users from the Microsoft 365 groups.

    **Note:** It only reads and pulls data from the Microsoft 365 **Members** group.

-   SharePoint Online Search Connector doesn’t read users from your Active directory.
-   SharePoint Online Search Connector supports **Everyone except external users** site permissions.
-   As an admin, you can use the following enhancements for more flexibility and control:
    -   **Flexible permissions**: Select the **Sites.FullControl.All**, **Sites.Read.All**, or **Sites.Selected** permissions while configuring the connector.
    -   **Selective indexing**: Index sites and subsites selectively by excluding some URLs and subsites, which have confidential information.
    -   **Index published versions**: Control and limit the indexing only to the published files, confirming employees access the verified and finalized versions and not the drafts or unfinished documents.​

        **Note:** If you have an existing connector without these enhancements, delete the existing connector, create a new connector, specify the URLs for indexing and exclusion, and define the site permissions for more effective content control and governance.

-   Two SharePoint instances cannot be connected to one ServiceNow instance simultaneously.
-   The Microsoft Entra ID spoke setup is required along with the Graph and REST connection setups to connect your ServiceNow instance to a Microsoft SharePoint tenant.

**Related topics**  


[SharePoint Online Search Connector reference](../reference/sharepoint-reference.md)


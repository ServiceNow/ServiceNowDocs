---
title: SAP SuccessFactors external content connector
description: The SAP SuccessFactors external content connector parses trainings exported from your SAP SuccessFactors Learning environment and makes their content and metadata searchable in AI Search applications.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/search-administration/sap-successfactors-external-content-connector.html
release: australia
product: Search Administration
classification: search-administration
topic_type: concept
last_updated: "2026-06-02"
reading_time_minutes: 2
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Configure, External Content Connectors, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# SAP SuccessFactors external content connector

The SAP SuccessFactors external content connector parses trainings exported from your SAP SuccessFactors Learning environment and makes their content and metadata searchable in AI Search applications.

The SAP SuccessFactors connector runs content and user permission crawls. Unlike most connector crawls, these crawls don't retrieve content or security principals directly from your SAP SuccessFactors Learning source system. Instead, content retrieval involves these steps:

1.  As a one-time step, a SAP SuccessFactors Learning admin creates three custom reports that retrieve the user, library and assignment, and training item data needed by the connector. These custom reports can be imported into SAP SuccessFactors Learning environments as needed.
2.  On a schedule of your choosing, a SAP SuccessFactors Learning admin runs the custom reports in your SAP SuccessFactors Learning environment. This process exports three comma-separated value \(CSV\) data files containing trainings content and security principals from the selected environment.
3.  After each data export, a connector administrator updates the SAP SuccessFactors connector configuration, attaching the latest exported CSV data files.
4.  On a schedule of your choosing, the connector runs content and user permission crawls. During a crawl, the connector parses the attached CSV data files to discover trainings content or security principals. It sends the discovered data to AI Search for indexing.

The indexed content and metadata are stored as records in a connector-specific indexed source. Search administrators can create search sources from this indexed source and link them to search profiles to make the indexed records searchable in AI Search applications.

-   **[Export SAP SuccessFactors Learning data for external content indexing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/export-sap-successfactors-data-external-content-indexing.md)**  
Export user, library and assignment, and training item data from your SAP SuccessFactors Learning environment. The SAP SuccessFactors external content connector needs this exported data to index your content and user permissions for search.
-   **[Create a SAP SuccessFactors external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/create-ext-cont-connector-sap-successfactors.md)**  
Create an external content connector to retrieve searchable content and security principals from your SAP SuccessFactors source system.
-   **[Update CSV data files for a SAP SuccessFactors external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/update-data-files-sap-successfactors-external-content-connector.md)**  
Upload newly generated comma-separated value \(CSV\) data files to your SAP SuccessFactors external content connector. The connector reads these files to retrieve updated content and metadata from your SAP SuccessFactors Learning source system.

**Parent Topic:**[Configuring External Content Connectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/configuring-ext-cont-connectors.md)

**Related topics**  


[Create a content crawl for an external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/create-content-crawl-external-content-connector.md)

[Create a user permission crawl for an external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/create-user-mapping-crawl-external-content-connector.md)


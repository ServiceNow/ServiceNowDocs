---
title: Create a SAP SuccessFactors external content connector
description: Create an external content connector to retrieve searchable content and security principals from your SAP SuccessFactors source system.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/search-administration/create-ext-cont-connector-sap-successfactors.html
release: australia
product: Search Administration
classification: search-administration
topic_type: task
last_updated: "2026-06-02"
reading_time_minutes: 6
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [SAP SuccessFactors external content connector, Configure, External Content Connectors, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Create a SAP SuccessFactors external content connector

Create an external content connector to retrieve searchable content and security principals from your SAP SuccessFactors source system.

## Before you begin

A source system administrator must have already exported user, library and assignment, and training item data from your SAP SuccessFactors Learning source system in three comma-separated value \(CSV\) files. For details on exporting the appropriate data from your source system in CSV format, see [Export SAP SuccessFactors Learning data for external content indexing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/export-sap-successfactors-data-external-content-indexing.md).

**Note:** The SAP SuccessFactors external content connector can't accept CSV data files that exceed the maximum attachment size specified by the value of the **com.glide.attachment.max\_size** system property. By default, this property limits the size of attachments to 1 Gb or less. For details on configuring this system property, see [Maximum allowed attachment size](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/sc-max-allowed-attachment-size.md).

Role required: sn\_ext\_conn.xcc\_admin

## Procedure

1.  Navigate to **All** &gt; **External Content Connectors** &gt; **External Content Admin Home**.

2.  If prompted, select **Switch scope** to switch to the External Content Connectors Admin scope.

    You must be in this scope to create or edit external content connectors.

3.  In the Connectors section, select **New**.

4.  On the Choose source page, select the **SAP SuccessFactors** tile, then select **Next**.

5.  On the Manage data page, attach the three exported CSV data files to entries in the Data tables section as follows.

    1.  In the Users data table, use the **Add file** link to attach the CSV data file that contains the User Mapping ID and Assignment Profile ID columns.

        Data from this file populates the user mapping table for the connector. The connector crawls this table during user permission crawls. AI Search uses the retrieved data to find the original document access restrictions to apply for each search user.

    2.  In the Library and assignment profiles data table, use the **Add file** link to attach the CSV data file that contains the Library ID and Assignment Profile ID columns.

        Data from this file links assignment profiles to libraries. The connector crawls this table during user permission crawls. AI Search uses the retrieved links to enforce the original document access restrictions for each search user.

    3.  In the Trainings data table, use the **Add file** link to attach the CSV data file that contains the Type ID, Item ID, Revision Date, Item Classification ID, Item Title, Item Description, and Aggregated Library ID columns.

        Data from this file provides content and metadata for training items. The connector crawls this table during content crawls. AI Search uses the retrieved information to make training item content and metadata searchable for users with the correct access controls.

    4.  In the Trainings data table, enter the URL for one of your SAP SuccessFactors source system's training items.

        AI Search analyzes this sample training item URL to determine the correct URL format for training item search results from your source system.

6.  Select the **I agree to the following disclaimer** option, then select **Next**.

7.  On the User permission settings page, modify any default user permission settings that you want to override for this connector.

    If you want to skip this step for now, select **Skip** instead of **Next**. You can modify the user permission settings for this connector from the External Content Admin Home page. For details on this procedure and user permission settings, see [Configure user permission settings for an external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/configure-user-mapping-settings-external-content-connector.md).

8.  On the Create crawl page, create a content crawl for this connector by selecting a crawl scope \(if supported\) and any desired options, then select **Next**.

    If you want to skip this step for now, select **Skip** instead of **Next**. You can create and run crawls for this connector from the External Content Admin Home page. For details on creating content crawls, see [Create a content crawl for an external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/create-content-crawl-external-content-connector.md).

9.  On the Connect search profile page, use the **Connect to search profile** field and **Add** button to add any search profiles that you want to connect this external content connector's default search source to, then select **Save**.

    If you want to skip this step for now, select **Skip** instead of **Next**. You can connect search sources for this connector to search profiles from the External Content Admin Home page. For details on connecting an external content connector to search profiles, see [Connect an external content connector to a search profile](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/connect-external-content-connector-search-profile.md).

    When you link a connector search source to a search profile in this step, the system automatically publishes the search profile to make the new link take effect.


## Result

Your new external content connector appears in the Connectors list on the External Content Admin Home page.

## What to do next

To retrieve searchable content and security principals with your new connector, you need to configure and run content and user mapping crawls for it. You can create content crawls for the connector from the External Content Admin Home page even if you skipped this step during connector creation.

For details on creating crawls for your new connector, see [Create a content crawl for an external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/create-content-crawl-external-content-connector.md) and [Create a user permission crawl for an external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/create-user-mapping-crawl-external-content-connector.md).

To make content crawled by your new connector searchable in portals and search applications, you must link one of its search sources to the search profile used by each portal or search application. You can use the connector's default search source or create your own custom search sources.

-   **Default search source**

    By default, the system creates a search source that includes all content from your external content connector's indexed source.

-   **Custom search sources**

    You can create your own search sources with filters to specify which content from the connector's indexed source is searchable. To view the connector's indexed source, navigate to **All** &gt; **AI Search** &gt; **AI Search Index** &gt; **Indexed Sources**. For information about creating search sources, see [Search sources in AI Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/search-sources-ais.md).


You can link connector search sources to search profiles from the External Content Admin Home page. For details on this procedure, see [Connect an external content connector to a search profile](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/connect-external-content-connector-search-profile.md).

**Parent Topic:**[SAP SuccessFactors external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/sap-successfactors-external-content-connector.md)


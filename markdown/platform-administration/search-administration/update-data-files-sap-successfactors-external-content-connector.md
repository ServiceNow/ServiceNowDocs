---
title: Update CSV data files for a SAP SuccessFactors external content connector
description: Upload newly generated comma-separated value \(CSV\) data files to your SAP SuccessFactors external content connector. The connector reads these files to retrieve updated content and metadata from your SAP SuccessFactors Learning source system.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/search-administration/update-data-files-sap-successfactors-external-content-connector.html
release: australia
product: Search Administration
classification: search-administration
topic_type: task
last_updated: "2026-06-02"
reading_time_minutes: 3
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [SAP SuccessFactors external content connector, Configure, External Content Connectors, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Update CSV data files for a SAP SuccessFactors external content connector

Upload newly generated comma-separated value \(CSV\) data files to your SAP SuccessFactors external content connector. The connector reads these files to retrieve updated content and metadata from your SAP SuccessFactors Learning source system.

## Before you begin

A source system administrator must have already exported updated user, library and assignment, and training item data from your SAP SuccessFactors Learning source system as three files in comma-separated value \(CSV\) format. To learn how to export the appropriate data from your source system, see [Export SAP SuccessFactors Learning data for external content indexing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/export-sap-successfactors-data-external-content-indexing.md).

**Note:** The SAP SuccessFactors external content connector can't accept CSV data files that exceed the maximum attachment size specified by the value of the **com.glide.attachment.max\_size** system property. By default, this property limits the size of attachments to 1 Gb or less. For details on configuring this system property, see .

A connector administrator must have already created the SAP SuccessFactors external content connector that parses the three CSV data files. For details on creating the connector, see [Create a SAP SuccessFactors external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/create-ext-cont-connector-sap-successfactors.md).

Role required: sn\_ext\_conn.xcc\_admin

## About this task

Unlike most external content connectors, the SAP SuccessFactors connector doesn't automatically retrieve updated content and metadata from its source system every time it crawls. To make updated content and metadata available for retrieval in crawls, you must update the connector configuration, attaching the latest CSV-format data files exported from the source system.

## Procedure

1.  Navigate to **All** &gt; **External Content Connectors** &gt; **External Content Admin Home**.

2.  If prompted, select **Switch scope** to switch to the External Content Connectors Admin scope.

    You must be in this scope to create or edit external content connectors.

3.  In the Connectors list, select the SAP SuccessFactors connector you want to update the CSV data files for, then navigate to **Settings** &gt; **Connection settings**.

4.  On the Connection settings page, attach the three exported CSV data files to entries in the Data tables section as follows.

    1.  In the Users data table, use the **Add file** link to attach the CSV data file that contains the User Mapping ID and Assignment Profile ID columns.

        Data from this file populates the user mapping table for the connector. The connector crawls this table during user permission crawls. AI Search uses the retrieved data to find the original document access restrictions to apply for each search user.

    2.  In the Library and assignment profiles data table, use the **Add file** link to attach the CSV data file that contains the Library ID and Assignment Profile ID columns.

        Data from this file links assignment profiles to libraries. The connector crawls this table during user permission crawls. AI Search uses the retrieved links to enforce the original document access restrictions for each search user.

    3.  In the Trainings data table, use the **Add file** link to attach the CSV data file that contains the Type ID, Item ID, Revision Date, Item Classification ID, Item Title, Item Description, and Aggregated Library ID columns.

        Data from this file provides content and metadata for training items. The connector crawls this table during content crawls. AI Search uses the retrieved information to make training item content and metadata searchable for users with the correct access controls.

    4.  In the Trainings data table, enter the URL for one of your SAP SuccessFactors source system's training items.

        AI Search analyzes this sample training item URL to determine the correct URL format for training item search results from your source system.

5.  Select the **I agree to the following disclaimer** option, then select **Save**.


**Parent Topic:**[SAP SuccessFactors external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/sap-successfactors-external-content-connector.md)


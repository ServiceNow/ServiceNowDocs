---
title: Import data using AI
description: Upload an unstructured document and let AI extract the threat observables and objects from its content. Review and correct the extracted entities before you submit the import.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/threat-intelligence-security-center/import-data-using-ai.html
release: australia
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2026-08-14"
reading_time_minutes: 5
keywords: [AI extraction, Import Intelligence, Threat Intelligence Security Center]
breadcrumb: [Import Intelligence in TISC, Use, Threat Intelligence Security Center, Security Operations]
---

# Import data using AI

Upload an unstructured document and let AI extract the threat observables and objects from its content. Review and correct the extracted entities before you submit the import.

## Before you begin

**Important:** Some generative AI skills, AI agents, and agentic workflows are turned on by default. For more information, see [AI agents, skills, and agentic workflows on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skills-on-by-default.md).

AI extraction is available only when the following prerequisites are met:

-   Threat Intelligence Security Center-Advanced must be installed.
-   ServiceNow Otto for Threat Intelligence Security Center \(TISC\) must be installed.
-   The Extract information from documents skill must be enabled. For more information, see [Extract information from documents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-extract-information-from-documents.md).

Role required: sn\_sec\_tisc.analyst

## About this task

Threat advisories, vendor reports, and screenshots may carry indicators of compromise inside prose rather than in a structured file. AI extraction reads the content of an uploaded document, identifies the threat entities it contains, and presents them for your review. You can import them without transcribing each value.

## Procedure

1.  Navigate to **Workspaces** &gt; **Threat Intelligence Security Center**.

    Threat Intel Library page is displayed.

2.  Select **Import Intelligence**.

    Alternatively, navigate to **Imports and exports** &gt; **New import** or **Case Record** &gt; **Import Intelligence**.

3.  Select the **Import using AI** card.

    The supported file types are PDF, DOCX, JPEG, and PNG.

4.  In **Choose extraction type**, select the type of extraction to run.

    |Extraction type|Description|
    |---------------|-----------|
    |Extract entities only|Returns the type and the value of each threat entity found in the document.|
    |Extract entities with rationale|Returns the type and the value of each threat entity, and adds the AI-generated **Analysis Score** and **Analysis Reasoning** values. For the attributes captured in the reasoning, see [AI extraction supported entities and fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/threat-intelligence-security-center/tisc-ai-extraction-fields.md).|

5.  Select **Upload file** and select the file to import.

    **Note:**

    Upload one file at a time, up to 5 MB. If you attach a file in an unsupported format, or attach more than one file, an error is displayed when you select **Done**. To replace the attached file, remove it and then attach the file you want.

6.  Under **Set definitions**, fill in the fields.

<table id="table_import_ai_definitions"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

TLP

</td><td>

Select the TLP indicator from the drop-down list to be applied for the imported records.

</td></tr><tr><td>

Confidence \(0-100\)

</td><td>

Define the confidence value. This value is applied to every imported record. It's separate from the AI-generated **Analysis Score**.

</td></tr><tr><td>

Expiry Period \(days\)

</td><td>

Enter the expiry period of the associated observables. The expiration date of each imported record is calculated from the current date and this value.**Note:**

This is a mandatory field.

</td></tr><tr><td>

Add Observable\(s\) to security Control List

</td><td>

Select this option to add observables to the appropriate security control list. The available options in the drop-down list are Allow list, Deny list, and None. The default option is **None**.

</td></tr><tr><td>

Add Tags

</td><td>

Add tags to annotate records ingested from this source. Start typing the tag name in the Search bar to choose the available tags in the system or enter new tag name and select **Add** to assign it.

</td></tr><tr><td>

Select a Taxonomy

</td><td>

Select the taxonomy for the imported data. For more information, see [Creating Taxonomies](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/threat-intelligence-security-center/create-taxonomies.md).

</td></tr></tbody>
</table>7.  Select **Next**.

    Use the import record link if you want to track the import separately.

    \[Omitted image "tisc-import-assistant-review.png"\] Alt text: TISC AI Import Assistant Review Screen

    The extracted entities are displayed on the review screen.

8.  Review the extracted entities before submission.

    **Important:**

    Review the AI-generated results for accuracy. AI identifies and classifies the entities from the content of your document, and the classification can be incorrect.

    -   The content tree groups the extracted entities as Observables and Objects, with a count for each group.
    -   Select a group in the content tree to display its records in the list.
    -   The columns marked with the AI icon hold AI-extracted values. For the field descriptions, see [AI extraction supported entities and fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/threat-intelligence-security-center/tisc-ai-extraction-fields.md).
9.  To correct the classification of an entity, select the records, select **Update Type**, and then select the type to apply.

    The records move to the group for the type you selected, and the counts in the content tree are updated.

10. To exclude entities from the import, select the records and select **Delete**.

11. Select **Submit**.

    **Note:**

    -   The imported records are processed into source records and then into aggregated records. The **Analysis Score** and **Analysis Reasoning** values are carried into the Additional context section of the source and aggregated records.
    -   Depending on the approval rules configured for your instance, the import record can be routed to an approver before processing.
12. Select **View Status** to view the status of the record, or select **Done**.

    The record displays the processed status once the submission is successful.

13. Select **Go Back** to return to the previous page, or select **Cancel** to abort the import.


-   **[AI extraction supported entities and fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/threat-intelligence-security-center/tisc-ai-extraction-fields.md)**  
Threat entity types that AI extraction identifies in an uploaded document, and the AI-generated fields that it adds to the extracted records.

**Parent Topic:**[Import Intelligence in TISC](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/threat-intelligence-security-center/importing-threat-intelligence.md)

**Related topics**  


[Import data using structured file]()

[Import data using standard format]()

[Import data using raw text]()

[Import data using unstructured file format]()

[AI extraction supported entities and fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/threat-intelligence-security-center/tisc-ai-extraction-fields.md)

[Import Intelligence in TISC](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/threat-intelligence-security-center/importing-threat-intelligence.md)


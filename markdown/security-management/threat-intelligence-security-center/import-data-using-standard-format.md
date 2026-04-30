---
title: Import data using standard format
description: Import data in supported formats \(STIX 2.x JSON or MISP JSON\) to enable full ingestion of all STIX Domain Objects \(SDOs\) and MISP objects.
locale: en-US
release: zurich
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Import Intelligence in TISC, Use, Threat Intelligence Security Center, Security Operations]
---

# Import data using standard format

Import data in supported formats \(STIX 2.x JSON or MISP JSON\) to enable full ingestion of all STIX Domain Objects \(SDOs\) and MISP objects.

## Before you begin

Role required: sn\_sec\_tisc.analyst

## Procedure

1.  Navigate to **Workspaces** &gt; **Threat Intelligence Security Center**.

    Threat Intel Library page is displayed.

2.  Select **Import Intelligence**.

3.  Select **Import from standard file** card.

    **Important:** While importing the threat intelligence data in the supported file formats such as TXT, CSV, STIX 2.x JSON, MISP JSON, or Structured File, the file size is limited to 5 MB. The characters limit to raw text is limited to 10,000.

4.  On the form, fill in the fields.

<table id="table_y14_2tq_fyb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

File Format

</td><td>

Select the required option from the drop down list such as STIX 2.x JSON or MISP JSON.-   **STIX 2.x JSON**: Select the format in STIX 2.x JSON to import.

**Note:** All the standard STIX entities such as Observables, Indicators, Objects, and Relationships will be imported from the uploaded STIX file.

-   **MISP JSON**: Select the format in MISP JSON format to import.

**Note:** MISP provides the functionality to import events, attributes, and objects using its standardized import format for seamless data ingestion.

For details on how MISP events, along with their associated attributes and objects, are mapped to TISC entities, refer to [KB2197697](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2197697).

</td></tr><tr><td>

Upload file

</td><td>

Click this link to upload the data in the standard file format.

</td></tr><tr><td colspan="2">

**Set definitions**

</td></tr><tr><td>

TLP

</td><td>

Select the TLP indicator from the drop-down list to be applied for the imported records.

</td></tr><tr><td>

Confidence \(0-100\)

</td><td>

Define the confidence value.

</td></tr><tr><td>

Expiry Period \(days\)

</td><td>

Enter the expiry period for the imported records.**Note:** This is a mandatory field.

</td></tr><tr><td>

Add Tags

</td><td>

Use the tags to annotate or ear mark records ingested into the system from this source. Start typing the tag name in the Search bar to choose the available tags in the system or enter new tag name and click Add to assign it to the source.

</td></tr><tr><td>

Add Observable\(s\) to security Control List

</td><td>

Select this option to add observables to the appropriate security control list. This option allows you to directly add the observables to a security control list while importing.

The available options in the drop-down list are:-   Allow list
-   Deny list
-   None
The default option is **None**.

</td></tr><tr><td colspan="2">

**Taxonomy**

</td></tr><tr><td>

Select a Taxonomy

</td><td>

Select the taxonomy for the imported data. Using taxonomies, define dictionaries that can be used as taxonomies assigned to threat intelligence records. For example, CAPEC nomenclature. For more information, see [Creating Taxonomies](../concept/create-taxonomies.md).

</td></tr><tr><td>

Select Taxonomy values

</td><td>

Indicates the taxonomy values that are associated with the Taxonomy.

</td></tr><tr><td>

Override source value

</td><td>

Select this check box if you wish to over ride the source values for TLP, Confidence, and Expiration from the configured values. If you don't select this check box the default values are applied.

</td></tr></tbody>
</table>5.  Click **Next**.

6.  Review the data before submission for processing.

    **Note:** Reviewing of imported records is not supported for STIX JSON or MISP JSON option.

    After you click **Next**, you can see the summary of all the information that user has provided in the above section, and the below section provides you with all the records that needs to be imported.

    User can perform any type of activities and the multiple users can collaborate using the comment section which is available in the right contextual menu.

    **Note:** Any records that fail the validations are skipped from the import process and those records are not displayed on the Review &amp; submit page for further processing.

7.  Click **Update Type** and select the type to update any type of the imported records.

8.  Click **Delete** to delete any type of the imported records.

9.  Click **Submit**.

    **Note:**

    After you submit the import record, it is directed for approval based on the configured approval rules. If the submitting user is exempt from approval, the import job is automatically approved upon submission.

10. Click **View Status** to view the status of the record or click **Done**.

    The record displays the processed status once it is processed.

11. Click **Cancel** to abort the import process.

12. Click **Go Back** to go back to the previous page and review the record, if necessary.

    For more information, see [Viewing all imports](viewing-all-imports.md).


**Parent Topic:**[Import Intelligence in TISC](../concept/importing-threat-intelligence.md)

**Related topics**  


[Import data using structured file](import-data-using-structured-file.md)

[Import data using raw text](import-data-using-pasted-text.md)

[Import data using unstructured file format](import-data-using-unstructured-file.md)


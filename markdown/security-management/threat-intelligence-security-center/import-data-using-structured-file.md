---
title: Import data using structured file
description: Upload the structured data in the supported file formats such as CSV, XLSX or XLS.
locale: en-US
release: yokohama
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Import Threat Intelligence, Use, Threat Intelligence Security Center, Security Operations]
---

# Import data using structured file

Upload the structured data in the supported file formats such as CSV, XLSX or XLS.

## Before you begin

Role required: sn\_sec\_tisc.analyst

## Procedure

1.  Navigate to **Workspaces** &gt; **Threat Intelligence Security Center**.

    The Threat Intel Library page is displayed.

2.  Click **Import Intelligence**.

3.  Click **Import from structured file** card.

    **Important:** While importing the threat intelligence data in the supported file formats such as TXT, CSV, STIX 2.x JSON, MISP JSON, or Structured File, the file size is limited to 5 MB. The characters limit to raw text is limited to 10,000.

4.  On the form, fill in the fields.

<table id="table_y14_2tq_fyb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Choose an option

</td><td>

Select the required option from the drop down list such as Observables or Indicators.-   **Observables**: Select the observables data to import.

**Note:** Select this option if you are importing observables data. Also do not modify the column headers in the file. The Mandatory fields are Value and Type, and others are optional. Also, enter the date/time in YYYY-MM-DDThh:mm:ssZ format.

-   **Indicators**: Select the indicators data to import.

**Note:** Select this option if you are importing indicators data. Also do not modify the column headers in the file. The mandatory fields for indicators are Pattern, Pattern Type, and Valid from and others are optional. Also, enter the date/time in YYYY-MM-DDThh:mm:ssZ format.

</td></tr><tr><td>

Preview and download sample file for Indicators

</td><td>

Use this link to download the sample file using the Preview link and upload the structured data in a compatible file format such as CSV, XLS, or XLSX.**Note:** The column headers must match the headers exactly. Value, Type fields are required for each observable in the file. The remaining fields are optional where as First Seen, Last Seen must be in numbers and are epoch time in milliseconds.

</td></tr><tr><td>

Upload file

</td><td>

Click this link to upload the file data in the recommended structure file format.**Note:** You can only upload one file at time. To add a new file you must remove the existing and add a new file.

</td></tr><tr><td colspan="2">

**Set definitions**

</td></tr><tr><td>

TLP

</td><td>

Select the Traffic Light Protocol \(TLP\) indicator from the drop-down list to be applied for the imported records.TLP is in TISC is labeled with different colors to ensure the sensitive data is shared with the intended users.

-   CLEAR: Information can be shared without restriction.
-   RED
-   AMBER+STRICT
-   AMBER
-   GREEN


</td></tr><tr><td>

Confidence \(0-100\)

</td><td>

Set the confidence value between 0-100 for the imported records.

</td></tr><tr><td>

Expiry Period \(days\)

</td><td>

Enter the expiry period for the imported records.**Note:** This is a mandatory field.

</td></tr><tr><td colspan="2">

**Tags**

</td></tr><tr><td>

Add Tags

</td><td>

Use the tags to annotate or ear mark records ingested into the system from this source. Staart typing the tag name in the **Search** bar to choose the available tags in the system or enter new tag name and click **Add** to assign it to the source.

</td></tr><tr><td colspan="2">

**Taxonomy**

</td></tr><tr><td>

Select a Taxonomy

</td><td>

Select the taxonomy for the imported data. Using taxonomies, define dictionaries that can be used as taxonomies assigned to threat intel records. For example, CAPEC nomenclature. For more information, see [Creating Taxonomies](../concept/create-taxonomies.md).**Note:** The taxonomy value options change based on the selected taxonomy.

</td></tr><tr><td>

Override source value

</td><td>

Select this check box if you wish to over ride the source values for TLP, Confidence, Expiration, Tags, and Taxonomies with the configured values. If you don't select this check box the configured values are applied if they are not empty.

</td></tr></tbody>
</table>5.  Click **Next**.

6.  Review the data before submission for processing.

    **Note:** Reviewing of imported records is not supported for STIX option.

    After you click **Next**, you can see the summary of all the information that user has provided in the above section, and the below section provides you with all the records that needs to be imported.

    User can perform any type of activities and the multiple users can collaborate using the comment section which is available in the right contextual menu. The list of imported records will be rendered once the entire file or raw text is processed. The import processing for large files will take more time and while it is processing you can check the status, review, and submit from the import record page as well.

    **Note:** Any records that fail the validations are skipped from the import process and those records are not displayed on the Review &amp; submit page for further processing.

7.  Click **Update Type** and select the type to update any type of the imported records.

8.  Click **Delete** to delete any type of the imported records.

9.  Click **Submit**.

    **Note:** After you submit the import record, the user will be directed to the approver to approve the corresponding import record based on the approval rules configured. If the current user who is creating the record doesn't require the approval process then the record goes through the auto approval process the import job gets auto approved while submitting request.

10. Click **View Status** to view the status of the import record or click **Done**.

    The record displays the processed status once the data is imported for processing.

11. Click **Cancel** to abort the import process.

12. Click **Go Back** to go back to the previous page and review the record, if necessary.


**Parent Topic:**[Import Threat Intelligence](../concept/importing-threat-intelligence.md)

**Related topics**  


[Import data using standard format](import-data-using-standard-format.md)

[Import data using raw text](import-data-using-pasted-text.md)

[Import data using unstructured file format](import-data-using-unstructured-file.md)


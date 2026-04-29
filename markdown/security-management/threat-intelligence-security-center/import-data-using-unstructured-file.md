---
title: Import data using unstructured file format
description: Upload the data in an unstructured format supported using the file formats such as TXT, CSV, JSON, XLS, XLSX.
locale: en-US
release: australia
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Import Intelligence in TISC, Use, Threat Intelligence Security Center, Security Operations]
---

# Import data using unstructured file format

Upload the data in an unstructured format supported using the file formats such as TXT, CSV, JSON, XLS, XLSX.

## Before you begin

Role required: sn\_sec\_tisc.analyst

## Procedure

1.  Navigate to **Workspaces** &gt; **Threat Intelligence Security Center**.

    Threat Intel Library page is displayed.

2.  Click **Import Intelligence**.

    **Important:**

    -   Any defanging characters will be cleaned as part of parsing and extraction of observables.
    -   For this unstructured file format option only URL, domain, file name, hashes, and IP address will be extracted and no other observable types will be extracted for the data import and in case of such type of observables such as registry, directory types, those will be skipped from importing.
3.  Click **Import from file \(unstructured\)** card.

    **Note:** While importing the threat intelligence data in the supported file formats such as TXT, CSV, STIX 2.x JSON, MISP JSON, or Structured File, the file size is limited to 5 MB.

4.  On the form, fill in the fields.

<table id="table_y14_2tq_fyb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

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

Enter the expiry period of the associated observables.**Note:** This is a mandatory field.

</td></tr><tr><td>

Add Observable\(s\) to security Control List

</td><td>

Select this option to add observables to the appropriate security control list. This option allows you to directly add the observables to a security control list while importing.

The available options in the drop down list are:-   Allow list
-   Deny list
-   None
The default option is **None**.

</td></tr><tr><td>

Add Tags

</td><td>

Use the tags to annotate or ear mark records ingested into the system from this source. Start typing the tag name in the Search bar to choose the available tags in the system or enter new tag name and click **Add** to assign it to the source.

</td></tr><tr><td colspan="2">

**Taxonomy**

</td></tr><tr><td>

Select a Taxonomy

</td><td>

Select the taxonomy for the imported data. Using taxonomies, define dictionaries that can be used as taxonomies assigned to threat intelligence records. For example, CAPEC nomenclature. For more information, see [Creating Taxonomies](../concept/create-taxonomies.md).

</td></tr></tbody>
</table>5.  Review the data before submission for processing.

    After you click **Next**, you can see the summary of all the information that user has provided in the above section, and the below section provides you with all the records that needs to be imported.

    User can perform any type of activities and the multiple users can collaborate using the comment section which is available in the right contextual menu.

    **Note:** The supported formats to import the data are TXT, CSV, JSON, XLS and any records that fail the validations are skipped from the import process and those records are not displayed on the Review &amp; submit page for processing.

6.  Click **Update Type** and select the type to update any type of the imported records.

7.  Click **Delete** to delete any type of the imported records.

8.  Click **Submit**.

    **Note:** After you submit the import record, the user will be directed to the approver to approve the corresponding import record based on the approval rules configured. If the current user who is creating the record doesn't require the approval process then the record goes through the auto approval process the import job gets auto approved while submitting request.

9.  Click **View Status** to view the status of the record or click **Done**.

    The record displays the processed status once the submission is successful.

10. Click **Cancel** to abort the import process.

11. Click **Go Back** to go back to the previous page and review the record, if necessary.


**Parent Topic:**[Import Intelligence in TISC](../concept/importing-threat-intelligence.md)

**Related topics**  


[Import data using structured file](import-data-using-structured-file.md)

[Import data using standard format](import-data-using-standard-format.md)

[Import data using raw text](import-data-using-pasted-text.md)


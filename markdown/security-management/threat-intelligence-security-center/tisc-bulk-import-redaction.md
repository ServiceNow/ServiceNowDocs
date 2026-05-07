---
title: Bulk Import of Redaction Categories and Values
description: Import redaction categories. Bulk importing of redaction categories and their associated values.
locale: en-US
release: australia
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Working on the Redaction Library, Exploring Outbound Intel Sharing, Configuring Threat Intelligence External Sharing, Administer, Threat Intelligence Security Center, Security Operations]
---

# Bulk Import of Redaction Categories and Values

Import redaction categories. Bulk importing of redaction categories and their associated values.

## Before you begin

Role required: sn\_sec\_tisc.admin

## About this task

You can download a sample file in either CSV or XLSX format, populate it with redaction categories and corresponding values, and then import it back into the application. This bulk import feature streamlines adding multiple redaction rules efficiently.

## Procedure

1.  Navigate to **Workspaces** &gt; **Threat Intelligence Security Center**.

2.  Select **Administration** icon on the workspace.

3.  Go to **Outbound Intel Sharing**.

4.  Select **Redaction Library**.

5.  Click **Import**.

6.  Download a sample file.

    The import file includes two columns:

    -   Redaction Category
    -   Value
    Ensure not to modify the headers in the sample file as this may cause import errors.

7.  Upload the file and click **Done**.

    A confirmation message is displayed that the redaction rows are imported successfully. You can also click on the link to view the import summary.

    **Note:** The file size must not exceed 5 MB, and the number of rows cannot be more than 1000.

    **Validation Rules:**

    1.  Ensure that all redaction categories and their category values are unique.
    2.  A redaction category value cannot be linked to more than one redaction category. For example, if a category value is already associated with one redaction category, it cannot be assigned to a different category.
    **System properties for bulk import of redaction categories and values**:

<table id="table_q3r_kxf_qfc"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_sec\_tisc.max\_redaction\_rows\_import

</td><td>

This property sets the maximum number of rows allowed when bulk importing data into the Redaction Library.The default maximum value is 1000.

</td></tr></tbody>
</table>
**Parent Topic:**[Working on the Redaction Library](tisc-redaction-library.md)


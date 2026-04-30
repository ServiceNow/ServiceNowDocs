---
title: Unzip operation
description: Extract one or more compressed attachments from a zip archive. You can extract all the compressed attachments in an archive or choose specific attachments to unzip.
locale: en-US
release: xanadu
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [ZIP step, Workflow Studio steps, Flows, subflows, and actions reference, Workflow Studio reference, Workflow Studio, Build workflows]
---

# Unzip operation

Extract one or more compressed attachments from a zip archive. You can extract all the compressed attachments in an archive or choose specific attachments to unzip.

<table id="table_thq_ww4_5tb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Operation

</td><td>

**Unzip** operation that extracts the attachments from the zipped archive in the record.

</td></tr><tr><td>

Source Attachment Records

</td><td>

Record that contains that zipped archive that you want to unzip.

</td></tr><tr><td>

Target record

</td><td>

Record that you want to unzip the attachments in the zipped archive to.

</td></tr><tr><td>

Target Table

</td><td>

Table related to the target record. The table is automatically populated when you select the record from the **Target record** field.

</td></tr><tr><td class="sub-head" colspan="2">

Advanced Options

</td></tr><tr><td>

Files to Unzip

</td><td>

Option to select the files that you want to unzip. Use the following options:-   **All Files**: Unzips all the attachments from the zipped archive.
-   **Selected Files**: Unzips only specific attachments that you select by using the **File Name Regular Expression** field.
-   **File Name Regular Expression**: Regular expression for selecting the required attachments from the zipped file in the source record. For example, the regular expression `*\.png` selects all the `.png` files in the archive.

</td></tr><tr><td>

Delete Source Zip Attachment

</td><td>

Field that removes the zipped archive in the source record after the unzip operation is completed.

</td></tr></tbody>
</table>## Action error evaluation

-   **If this step fails**

    Data type: **Choice**

    Option to continue running the next step or go to error evaluation. To use the step status code or message for a custom action error condition, see [Action error evaluation](../concept/action-error-evaluation.md).


**Parent Topic:**[ZIP step](zip-step.md)


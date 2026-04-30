---
title: Bulk import map examples
description: Mapping your source employee documents to required elements in Employee Document Management is crucial for a successful bulk import.
locale: en-US
release: zurich
product: Employee Document Management
classification: employee-document-management
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Bulk imports, Use, Employee Document Management, HR Documents, HR Service Delivery, Employee Service Management]
---

# Bulk import map examples

Mapping your source employee documents to required elements in Employee Document Management is crucial for a successful bulk import.

This topic provides examples on how to map your source employee documents to the required elements in Employee Document Management. The values provided are examples designed to guide you through the import map configuration.

## Map fields and values directly from existing file names

Using your existing employee document file names is recommended when your source employee documents reside in a local repository.

For example, an employee document can have all the meta data in the file name Abel\_Tuter\_tuition.pdf to map to Employee Document Management.

**Note:** When using regular expressions \(RegEx\) to define the replacement value, use a regular expression test site to ensure correct parsing.

-   **File name example**

    The example file name is abel\_tuter\_tuition.pdf.

    To find and extract the file name from the source repository, see this example:

    ![Import Map — File name](../image/import-map-filename.png)

    The import map is looking for a source element called fileName.

    The import map is going to translate this source element to a mapped element called fileName.

    The Regex is looking for the format of the file name first\_last\_xxx.pdf.

-   **File name to employee name example**

    From the file name, the employee name is extracted. Employee name is a requirement for Employee Document Management.

    ![Import Map — Employee Name](../image/import-map-employee.png)

    The import map is looking for a source element called fileName.

    The import map is going to translate this source element to a mapped element called employee.

    The Regex is looking for the format of the file name to be first\_last\_tuition.pdf \(\\w+\)\_\(\\w+\)\_\(\\w+\).\(\\w+\).

    It replaces the original file name with first.last \($1.$2\)

-   **File name to document type example**

    From the file name, the document type is extracted. Document type is a requirement for Employee Document Management.

    ![Import Map — docType](../image/import-map-doctype.png)

    The import map is looking for a source element called fileName.

    The import map is going to translate this source element to a mapped element called docType.

    The Regex is looking for the format of the file name to be first\_last\_tuition.pdf \(\\w+\)\_\(\\w+\)\_\(\\w+\).\(\\w+\).

    It creates a docType of tuition \($3\).

    **Note:** Having the source employee documents in a central repository, simple directory structure, and consistent file naming convention are highly recommended and reduces errors.


## Parse and map fields and values from a JSON output

Using a JSON output is recommended when your source employee documents reside in a third-party, cloud-based repository.

<table id="table_dkq_pqm_yfb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Mapping type

</td><td>

Field

</td></tr><tr><td>

Mapped element

</td><td>

itemsLooks for the items mapping element in an array of items in the folder.

 This mapping is used after Stage — Directory import source.

</td></tr><tr><td>

Source element

</td><td>

entriesSource element in the JSON output and represents the items in a folder. For example, Box uses entries as the source element.

</td></tr></tbody>
</table>![JSON — entries](../image/edm-json-entries.png)

<table id="table_t1j_crm_yfb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Mapping type

</td><td>

Field

</td></tr><tr><td>

Mapped element

</td><td>

itemLooks for item, an entry in an array of items in the folder.

 This mapping is used after Stage — Directory import source to run operations against a single item.

</td></tr><tr><td>

Source element

</td><td>

idFor each item in the array, find the file ID in the JSON output.

</td></tr><tr><td>

Filter regex

</td><td>

fileCombined with the Filter field to exclude subfolders.

</td></tr><tr><td>

Filter field

</td><td>

typeFilter output to where the type field is equal to file to exclude subfolders.

</td></tr></tbody>
</table>![JSON — item](../image/edm-json-id.png)

<table id="table_ckk_nrm_yfb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Mapping type

</td><td>

Field

</td></tr><tr><td>

Regex

</td><td>

\(\\w+\)\\s\(\\w+\)String translation to convert fname lname to fname.lname.

</td></tr><tr><td>

Replace

</td><td>

$1.$2Converts files found in Regex field fname lname to fname.lname.

</td></tr><tr><td>

Mapped element

</td><td>

employeeLooks for employee mapping element. Employee is a field in the file item.

 This mapping is used after Stage — file import source.

</td></tr><tr><td>

Source element

</td><td>

owned\_by.nameLooks for name in owned\_by object. Bypass nested objects with a dot notation.

</td></tr><tr><td>

Filter regex

</td><td>

 

</td></tr></tbody>
</table>![JSON — Owned by and Name](../image/edm-owned-by-name.png)

<table id="table_wmt_xms_yfb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Mapping type

</td><td>

ValueSelecting **Value** maps the employee element within an array of information from your source document to a specific value in Employee Document Management.

</td></tr><tr><td>

Replace

</td><td>

david.looThe value you want to replace the source element with in Employee Document Management.

 Employee Document Management requires employee names to be formatted fname.lname.

</td></tr><tr><td>

Mapped element

</td><td>

employeeLooks for the **employee** mapping element that is a field in the file item.

 This mapping is used after Stage — file import source.

</td></tr><tr><td>

Source element

</td><td>

davidlLooks for the source value of davidl.

</td></tr></tbody>
</table>This example illustrates how to use Value mapping to take an employee name from your source document and map it to the format that Employee Document Management requires.

<table id="table_ys3_lwm_yfb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Mapping type

</td><td>

Field

</td></tr><tr><td>

Mapped element

</td><td>

docTypeLooks for the docType mapping element embedded in the description field in the file item.

 This mapping is used after Stage — file import source.

</td></tr><tr><td>

Source element

</td><td>

descriptionLooks for name in description.

</td></tr><tr><td>

Filter regex

</td><td>

 

</td></tr></tbody>
</table>![JSON — description](../image/edm-json-description.png)

<table id="table_q23_vym_yfb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Mapping type

</td><td>

ValueUse Value to map a specific value in your third-party, cloud-based repository to a value in Employee Document Management.

</td></tr><tr><td>

Replace

</td><td>

employee verificationsReplace verification \(source\) with employee verifications \(Employee Document Management\).

</td></tr><tr><td>

Mapped element

</td><td>

docTypeLooks for the docType mapping element embedded in the description field in the file item.

 This mapping is used after Stage — file import source.

</td></tr><tr><td>

Source element

</td><td>

verificationLook for the name value of verification in the JSON.

</td></tr></tbody>
</table><table id="table_imc_4cn_yfb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Mapping type

</td><td>

ValueUse Value to map a specific value in your third-party, cloud-based repository to a value in Employee Document Management.

</td></tr><tr><td>

Replace

</td><td>

transcriptsReplace school \(source\) with transcripts \(Employee Document Management\).

</td></tr><tr><td>

Mapped element

</td><td>

docTypeLooks for the docType mapping element embedded in the description field in the file item.

 This mapping is used after the Stage — file import source.

</td></tr><tr><td>

Source element

</td><td>

schoolLooks for the name value school.

</td></tr></tbody>
</table><table id="table_cv5_22n_yfb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Mapping type

</td><td>

field

</td></tr><tr><td>

Mapped element

</td><td>

fileNameLooks for the fileName mapping element embedded in the name field in the file item.

 This mapping is used after Stage — file import source.

</td></tr><tr><td>

Source element

</td><td>

nameLooks for filename in the description in the JSON output.

</td></tr><tr><td>

Filter regex

</td><td>

 

</td></tr></tbody>
</table>![JSON — Name](../image/edm-json-name.png)

<table id="table_tj2_pwr_yfb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Mapping type

</td><td>

field

</td></tr><tr><td>

Mapped element

</td><td>

urlLooks for the url mapping element embedded in the id field in the file item.

 This mapping is used after Stage — file import source.

</td></tr><tr><td>

Source element

</td><td>

Looks for id in JSON output. **Note:** some third-party, cloud-based repositories use the file ID. The capture import source builds a URL from this value.

</td></tr></tbody>
</table>![JSON — id](../image/edm-json-id.png)

## Bulk import mapping records

An example of Employee Document Import Map.

![Import map](../image/edm-import-map.png)

When a connection to your source repository is confirmed and import maps are set up correctly, you can click **Start staging job** from Related Links.

**Parent Topic:**[Bulk imports in Employee Document Management](../concept/edm-bulk-uploads.md)


---
title: Easy import
description: Easy import is a simplified import process that enables you to import only the columns you want.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/easy-import/c\_EasyImport.html
release: australia
product: Easy Import
classification: easy-import
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Imports, Workflow Data Fabric]
---

# Easy import

Easy import is a simplified import process that enables you to import only the columns you want.

Only admins can use easy import. You can import data to tables within the current scope and tables that grant write access to other applications.

## Easy import template validation

Each import template must pass two sets of validation.

<table><thead><tr><th>

Type of validation

</th><th>

Stored in

</th><th>

Results of failing validation

</th></tr></thead><tbody><tr><td>

Client-side validation

</td><td>

Import template

</td><td>

The template highlights the invalid cell.\[Omitted image "ImportTemplateClientValidation.png"\] Alt text: Import template client validation

</td></tr><tr><td>

Server-side validation

</td><td>

Instance

</td><td>

The import pauses and displays an error message.\[Omitted image "ImportTemplateServerValidation.png"\] Alt text: Import template server validation

</td></tr></tbody>
</table>-   **[Download an import template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/easy-import/t_DownloadAnImportTemplate.md)**  
Select the list you want to import data to and create an import template from that list.
-   **[Add a record in the template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/easy-import/t_AddARecordInTheTemplate.md)**  
Add rows to the template to create new records.
-   **[Update a record in the template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/easy-import/t_UpdateARecordInTheTemplate.md)**  
Modify rows in the template to update existing records.
-   **[Import a record from the template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/easy-import/t_ImportARecordFromTheTemplate.md)**  
After updating the import template with new data, import the template to your instance.
-   **[Show reference fields as lists in Excel templates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/easy-import/show-excel-reference-dropdowns.md)**  
Display selected reference fields as lists in Excel templates to simplify data selection and updates.
-   **[Easy import template validation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/easy-import/r_TemplateValidation.md)**  
Each import template must pass two sets of validation.
-   **[Easy import properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/easy-import/easy-import-properties.md)**  
Several properties control the behavior of easy import.

**Parent Topic:**[Imports](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/imports-overview-page.md)


---
title: Use import mapping to locate and transform source employee documents
description: Import mapping locates your source employee documents from your source document repository and transforms them to import them to Employee Document Management.
locale: en-US
release: australia
product: Employee Document Management
classification: employee-document-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Employee document management bulk imports, Using Employee Document Management, Employee Document Management, HR Documents, HR Service Delivery, Employee Service Management]
---

# Use import mapping to locate and transform source employee documents

Import mapping locates your source employee documents from your source document repository and transforms them to import them to Employee Document Management.

Import maps define mapping variables used to acquire meta data from the source document repository. It also allows you to correctly identify the employee documents you want to import and maps them to required elements in Employee Document Management.

The required elements for a local network directory:

-   Employee name
-   Document type
-   File name

The required elements for a third-party, cloud-based directory:

-   items
-   item
-   Employee name
-   Document type
-   File name
-   url

## Parsing for fields and values from an output file

If your source document repository provides an output file, you can transform mapping locates, parse, and map the output file into values that Employee Document Management requires. To transform an output file, do the following:

-   Create a Field mapping type that finds an array of items in the output file \(JSON is an example of an output file\).
-   Create a Field mapping type that for each item in the array that locates the file ID.
-   Create a Field mapping type that locates the employee mapped element.
-   Create a Field mapping type that locates the docType mapped element.
-   Create a Field mapping type that locates the fileName mapped element.
-   Create a Field mapping type that locates the url mapped element.

## Extracting from a file name

If your source employee documents have:

-   A consistent naming convention.
-   The employee file has all required meta data in the file name.

You can use import maps to locate and transform the source employee document into values that Employee Document Management requires.

For example, your employee documents have a consistent naming convention: Abel\_Tuter\_LOARequestLeave.pdfYou can map parts of the file name to the required elements for Employee Document Management:

-   Employee name: abel.tuter
-   Document type: LOARequestLeave
-   File name: Abel\_Tuter\_LOARequestLeave.pdf

## Scripting

You can also use scripts to map source elements to the required map elements for Employee Document Management. See [Scripts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/scripts/c_Script.md).

**Note:** The base system provides import map examples you can use as models.

**Parent Topic:**[Employee document management bulk imports](edm-bulk-uploads.md)


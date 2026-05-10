---
title: Exporting and converting records into complex data types
description: Use URL parameters to export table records and convert them into complex data types, such as JSON, XML, PDF, CSV, and XLS.
locale: en-US
release: australia
product: Web Services
classification: web-services
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Inbound, Web services, API implementation, API implementation and reference]
---

# Exporting and converting records into complex data types

Use URL parameters to export table records and convert them into complex data types, such as JSON, XML, PDF, CSV, and XLS.

## Exporting records as complex data types

You can use an HTTP `GET` request to retrieve records from a table and put them in a specified format. For example, use the **PDF** parameter in a `GET` request to export records from a table as PDF files; use the **XLS** parameter to export records from a table as XLS files. For example, to retrieve a list of incident records as XLS files, issue an HTTP `GET` using the following URL: `https://instance_name.service-now.com/incident.do?XLS`. The file returned is `incident.xls`. `incident.do` is basically a `GET` that returns a list of the records from the incident table. The **XLS** parameter converts those records into XLS files.

The general syntax is: `https://<serviceNow-instance-name>/<table-name>.do?<Data-type-parameter>`

## URL parameters

The following table shows URL parameters you can use in `GET` requests, filters you can use to filter out unwanted table records in the return, and an indicator of whether you can `POST` the data type directly to a table. The parameter becomes the extension of the returned file, for example, using the **XLS** parameter returns a file in the form `<table-name>.xls`.

|Data type|Parameter|Valid filters|Directly POST to table?|
|---------|---------|-------------|-----------------------|
|CSV|CSV|sysparm\_query, sysparm\_view|Y|
|Excel|XLS, EXCEL, XLSX|sysparm\_query, sysparm\_view|Y|
|JSON|JSONv2|Various. See [JSON data retrieval API](../../inbound-other-web-services/concept/c_DataRetrievalAPI.md).|Y|
|PDF|PDF|sysparm\_query, sysparm\_view|N|
|RSS|RSS|sysparm\_query, sysparm\_view and more. See [Limiting results with a view](../../rss/concept/c_LimitingResultsWithAView.md).|N|
|XML|XML, XSD, SCHEMA|sysparm\_query, useUnloadFormat|N|

For more information about retrieving and converting table records into the JSON file format, see [JSONv2 Web Service](../../inbound-other-web-services/concept/c_JSONv2WebService.md).

For more information about retrieving and converting table records into the RSS file format, see [RSS feed generator](../../rss/concept/c_RSSFeedGenerator.md).

## Converting records to PDFs

For PDF export, there is a distinction between targeting a table and targeting its list. To generate a PDF of a list of records, suffix the target with `_list`. To target a single record, you must specify the **sys\_id** parameter to identify the record for which you are generating the PDF.

## Filters

All URL parameters work with filters that enable you to export a subset of table records. For example, `sysparm_query=active=true` in a `GET` request exports only active records. The following example exports only active incident records in an Excel format: `https://instance_name.service-now.com/incident.do?EXCEL&sysparm_query=active=true`.

The general syntax is: `https://<serviceNow-instance-name>/<table_list>.do?<Data-type-parameter>&<filter>`

Filters include:

-   sysparm\_query—Filters the data using the encoded query before exporting files, for example, `sysparm_query=active=true` exports only active records.
-   sysparm\_view—Specify the name of a list view to control which fields are returned. For example, to return the ESS view, use `sysparm_view=ess`.
-   useUnloadFormat—Indicates that the XML format returned is an unload format. The unload format is the same format you get when, from a list in the UI, you select Export &gt; XML &gt; ... You can import unload-formatted XML files back into the tables. To enable the unload format from a URL, use the `useUnloadFormat=true` URL parameter, for example, `https://instance_name.service-now.com/incident.do?XML&useUnloadFormat=true`.

## Example GET queries

|Data type|Example query|
|---------|-------------|
|CSV|`https://instance_name.service-now.com/incident.do?CSV&sysparm_query=active=true`|
|Excel|`https://instance_name.service-now.com/incident.do?XLS&sysparm_query=active=true`|
|PDF|`https://instance_name.service-now.com/incident.do?PDF&sysparm_view=ess`|
|RSS|`https://instance_name.service-now.com/incident.do?RSS&sysparm_view=ess`|
|XML|`https://instance_name.service-now.com/incident.do?XML&sysparm_query=active=true`|

## Returned files

`GET` queries return records from a table in the format specified in the request. For example, a query that uses the **XLS** parameter returns a table record in a file with the `.xls` extension.

The Content-Disposition header in the response displays the file name and extension of the returned file. The file name is based on the table you export from, such as incident.xls, incident.pdf, or incident.xml.

## Exporting data into tables

You can `POST` the following data types directly into tables:

-   CSV
-   Excel
-   JSON

The file headers must match the field columns in the targeted table. For more information, see [Post CSV or Excel files directly to an import set](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/system-import-sets/t_PostCSVOrExcelFilesToImportSet.md).

**Parent Topic:**[Inbound web services](../../web-services/concept/inbound-web-services.md)


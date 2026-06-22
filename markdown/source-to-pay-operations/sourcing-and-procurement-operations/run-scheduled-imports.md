---
title: Run scheduled imports
description: A scheduled import allows administrators to import data on a regular schedule. Run import operations on a daily, weekly, or monthly basis based on your business requirements. Scheduled import runs a datasource similar to how a scheduler job runs the script.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/source-to-pay-operations/sourcing-and-procurement-operations/run-scheduled-imports.html
release: zurich
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Import data using FTP server, Procurement File Transfer Framework, Integrate Sourcing Procurement Operations other, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Run scheduled imports

A scheduled import allows administrators to import data on a regular schedule. Run import operations on a daily, weekly, or monthly basis based on your business requirements. Scheduled import runs a datasource similar to how a scheduler job runs the script.

## Before you begin

Role required: import\_scheduler, import\_admin, or admin

## Procedure

1.  Navigate to **All** &gt; **System Import Sets** &gt; **Administration** &gt; **** &gt; **Scheduled Imports**.

    A list of available scheduled imports appears with Run, Data source, Active, and Updated information.

2.  Select **Example File Based Catalog Import**

    \[Omitted image "spo-run-scheduled-import.png"\] Alt text: The Example File Based Catalog Import form.

3.  Follow the steps for [data import](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/integrate-applications/system-import-sets/t_ScheduleADataImport.md).


## What to do next

-   You can verify the data transfer records from **Procurement Integrations** &gt; **Catalog** &gt; **FTP Catalog Imports**. You can see all the data as one single payload content. See Payloads for more information.
-   The same record is then transformed and available from **Procurement Integrations** &gt; **Catalog** &gt; **Catalog Imports**.

**Parent Topic:**[Import data using FTP server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/sourcing-and-procurement-operations/ftp-data-import.md)


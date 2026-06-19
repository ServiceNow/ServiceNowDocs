---
title: Data egress reports in the Integration Hub Usage Dashboard
description: The Data egress reports give insights on data egress from the ServiceNow instance through API protocols or export sets. You can view more information when you select specific records.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/integration-hub/ihub-dashboard-api-egress.html
release: australia
product: Integration Hub
classification: integration-hub
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Integration Hub Usage Dashboard, Configure, Integration Hub, Workflow Data Fabric]
---

# Data egress reports in the Integration Hub Usage Dashboard

The Data egress reports give insights on data egress from the ServiceNow instance through API protocols or export sets. You can view more information when you select specific records.

## Access the reports

Do the following steps.

1.  Select the **Data Egress** tab.
2.  Select the API or Export section that you want to view from the **Filter by** list.

    **Note:** The Overview section is selected by default.


## Overview section reports

Data Egress: Total volume of data egress by all sources.

Data Egress by source: Data egress volume by API protocols and export.

Data Egress Trends: Trends in data egress across the time period.

\[Omitted image "ihub-dashboard-overview.png"\] Alt text: Overview section that shows data egress.

**Note:** All charts are adjusted to the nearest data metric starting with Bytes.

## API section reports

Data Egress: Total volume of data egress by all API protocols.

Data Egress by API Protocols: Data egress volume by API protocols.

Data Egress Trends: Trends in data egress across the time period.

\[Omitted image "ihub-data-egress-api-protocols.png"\] Alt text: API section showing data egress by protocols.

**Note:** All charts are adjusted to the nearest data metric starting with Bytes.

## Export section reports

Data Egress: Total volume of data egress by both the export sets and URI.

Data Egress by Exports: Data egress volume by URI.

Data Egress Trends: Trends in data egress across the time period.

**Note:** All charts are adjusted to the nearest data metric starting with Bytes.

**Important:** The amount of data is mentioned in bytes and the abbreviations are as described in the following table.

|Abbreviation|Number|Value|
|------------|------|-----|
|K|Thousand|10^3|
|M|Million|10^6|
|B|Billion|10^9|
|T|Trillion|10^12|

That is, if the value displayed is **4.01M**, the amount of data transferred is 4.01 million bytes. In the preceding sample API Data Egress, the data amount of data transferred is 2.01 billion bytes.

Select the number to access details of the individual data transfers.

## View data insights

View different insights on data going out of the ServiceNow instance. For example, view the data egress volume between a period that you specify. Do the actions given in the image.

## View egress data for a specified time period

\[Omitted image "ihub-dashboard-date-range.png"\] Alt text: Filter to specify date range.

## Overview of data egress

View the total data egress, and the data egress by API protocols or exports.

Do the steps.

1.  Select the **Data Egress** tab.

    Confirm that in the Filter by list, Overview is selected.

2.  Select the data egress volume in the Data Egress report.

    \[Omitted image "ihub-dashboard-data-egress-overview.png"\] Alt text: Total data egress volume.

    The data egress by API protocols and exports appear.

    \[Omitted image "ihub-dashboard-data-egress-by-api-exports.png"\] Alt text: Data egress by API protocols and exports.


## Data egress by API protocols or exports

View data egress by various API protocols or exports.

Do the steps.

1.  Select the **Data Egress** tab.

    Confirm that in the Filter by list, Overview is selected.

2.  On the Data Egress by source report, select a source.

    \[Omitted image "ihub-usage-dashboard-data-egress-api-exports.png"\] Alt text: Data egress by API protocols and exports.

    For example, select API.

    The data egress by API protocols such as REST and SOAP appears.

    \[Omitted image "ihub-usage-dashboard-data-egress-sources.png"\] Alt text: Data egress by sources.


## View data egress by API protocols or exports on a specified date

Select a date and API protocol or exports and view the data egress by the source you specified on that date.

Do the following steps.

1.  Select the **Data Egress** tab.

    Confirm that in the Filter by list, Overview is selected.

2.  On the Data Egress Trends report, move the pointer to a date and then select the source.

    \[Omitted image "ihub-dashboard-data-egress-by-date.png"\] Alt text: Date and source selection for data egress report.

    All records of data egress by the date and source that you specified appears.


## View data egress by API protocols

View data egress by JSON, REST, or SOAP protocols, and then select a record from the data to view more information.

Do the steps.

1.  Select the **Data Egress** tab.
2.  From the Filter by list, select **API**.
3.  In the Data Egress by API Protocols report, select an API protocol, for example, REST.

    \[Omitted image "data-egress-by-api-prot.png"\] Alt text: Selection of an API protocol.

    All records of data egress by the API protocol that you specified appears.

    \[Omitted image "data-egress-by-api-prot-result.png"\] Alt text: Data egress shown by the API protocol that you specified.

4.  To view more data on a specific record, select the View Aggregate Breakdown icon \[Omitted image "ihub-usage-drill-down-icon.png"\] Alt text: Drill down icon..

    \[Omitted image "ihub-usage-view-aggr-breakdown.png"\] Alt text: Select the View Aggregate Breakdown icon.

    The transaction log appears.

    \[Omitted image "ihub-usage-transac-log.png"\] Alt text: Transaction log.


## View data egress by API protocols on a specified date

Specify a date and view the data egress by JSON, REST, or SOAP protocols on that date. You can select a record from the data to view more information.

Do the steps.

1.  Select the **Data Egress** tab.
2.  From the Filter by list, select **API**.
3.  Move the pointer to a date on the graph, and select an API protocol.

    \[Omitted image "ihub-usage-select-date.png"\] Alt text: API protocol graph.

    The data egress by the selected API protocol on the selected date appears.

    \[Omitted image "ihub-usage-protocol-date.png"\] Alt text: Data egress by date.

4.  To view more data on a specific record, select the View Aggregate Breakdown icon \[Omitted image "ihub-usage-drill-down-icon.png"\] Alt text: Drill down icon..

    \[Omitted image "ihub-usage-api-prot-trends.png"\] Alt text: Data egress API trends.

    The transaction log appears.

    \[Omitted image "ihub-usage-transac-log.png"\] Alt text: Transaction log.


## Reports on data egress by export

View information on the data egress from the ServiceNow instance by URI and export sets.

To access the reports, do the steps.

1.  Select the **Data Egress** tab.
2.  From the Filter by list, select **Export**.

## Reports on data egress by export sets or URI

To access the reports on data egress by export sets or URI, do the steps.

1.  On the Data Egress by Exports report pie-chart, select the data export type. For example, export sets.

    \[Omitted image "ihub-usage-egress-export-uri.png"\] Alt text: Data egress by export type.

    The date-wise data exports by the source you specified appears.

    \[Omitted image "ihub-usage-export-set.png"\] Alt text: Export source-wise data.

2.  To view more information on an export set on a date, select the View Aggregate Breakdown icon \[Omitted image "ihub-usage-drill-down-icon.png"\] Alt text: Drill down icon..

    \[Omitted image "ihub-usage-export-drilldown.png"\] Alt text: Select the View Aggregate Breakdown icon.

    The data appears.


## Date-wise data egress by exports

View data egress by exports on a date that you specify.

Do the following steps.

1.  On the Data Egress Trends report, move the pointer to a date and then select the export type. For example, move the pointer to April 19, and then select Export Sets.

    \[Omitted image "ihub-usage-export-by-date.png"\] Alt text: Data export by export type on a date.

    The egress data on the export type and date that you specified appears.

    \[Omitted image "ihub-usage-export-date.png"\] Alt text: Date-wise and source-wise egress data.

2.  To view more data on a specific record, select the View Aggregate Breakdown icon \[Omitted image "ihub-usage-drill-down-icon.png"\] Alt text: Drill down icon..

\[Omitted image "ihub-usage-export-drill-down.png"\] Alt text: View Aggregate Breakdown icon.

The data appears.

\[Omitted image "ihub-usage-datewise-export-egress.png"\] Alt text: Drill-down data.

## Data generation in the reports

Data in the reports are generated from the `data_egress_count` table. [View](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1638468) how data is populated in the `data_egress_count`.

**Parent Topic:**[Integration Hub Usage Dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/integration-hub/integrationhub-usage-dashboard.md)


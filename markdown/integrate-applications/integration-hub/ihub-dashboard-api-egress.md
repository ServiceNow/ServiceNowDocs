---
title: Data egress reports in the Integration Hub Usage Dashboard
description: The Data egress reports give insights on data egress from the ServiceNow instance through API protocols or export sets. You can view more information when you select specific records.
locale: en-US
release: yokohama
product: Integration Hub
classification: integration-hub
topic_type: reference
last_updated: "2025-04-24"
reading_time_minutes: 5
breadcrumb: [Integration Hub Usage Dashboard, Configuring Integration Hub, Integration Hub, Data and Automation]
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

![Overview section that shows data egress.](../images/ihub-dashboard-overview.png)

**Note:** All charts are adjusted to the nearest data metric starting with Bytes.

## API section reports

Data Egress: Total volume of data egress by all API protocols.

Data Egress by API Protocols: Data egress volume by API protocols.

Data Egress Trends: Trends in data egress across the time period.

![API section showing data egress by protocols.](../images/ihub-data-egress-api-protocols.png)

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

![Filter to specify date range.](../images/ihub-dashboard-date-range.png)

## Overview of data egress

View the total data egress, and the data egress by API protocols or exports.

Do the steps.

1.  Select the **Data Egress** tab.

    Confirm that in the Filter by list, Overview is selected.

2.  Select the data egress volume in the Data Egress report.

    ![Total data egress volume.](../images/ihub-dashboard-data-egress-overview.png)

    The data egress by API protocols and exports appear.

    ![Data egress by API protocols and exports.](../images/ihub-dashboard-data-egress-by-api-exports.png)


## Data egress by API protocols or exports

View data egress by various API protocols or exports.

Do the steps.

1.  Select the **Data Egress** tab.

    Confirm that in the Filter by list, Overview is selected.

2.  On the Data Egress by source report, select a source.

    ![Data egress by API protocols and exports.](../images/ihub-usage-dashboard-data-egress-api-exports.png)

    For example, select API.

    The data egress by API protocols such as REST and SOAP appears.

    ![Data egress by sources.](../images/ihub-usage-dashboard-data-egress-sources.png)


## View data egress by API protocols or exports on a specified date

Select a date and API protocol or exports and view the data egress by the source you specified on that date.

Do the following steps.

1.  Select the **Data Egress** tab.

    Confirm that in the Filter by list, Overview is selected.

2.  On the Data Egress Trends report, move the pointer to a date and then select the source.

    ![Date and source selection for data egress report.](../images/ihub-dashboard-data-egress-by-date.png)

    All records of data egress by the date and source that you specified appears.


## View data egress by API protocols

View data egress by JSON, REST, or SOAP protocols, and then select a record from the data to view more information.

Do the steps.

1.  Select the **Data Egress** tab.
2.  From the Filter by list, select **API**.
3.  In the Data Egress by API Protocols report, select an API protocol, for example, REST.

    ![Selection of an API protocol.](../images/data-egress-by-api-prot.png)

    All records of data egress by the API protocol that you specified appears.

    ![Data egress shown by the API protocol that you specified.](../images/data-egress-by-api-prot-result.png)

4.  To view more data on a specific record, select the View Aggregate Breakdown icon ![Drill down icon.](../images/ihub-usage-drill-down-icon.png).

    ![Select the View Aggregate Breakdown icon.](../images/ihub-usage-view-aggr-breakdown.png)

    The transaction log appears.

    ![Transaction log.](../images/ihub-usage-transac-log.png)


## View data egress by API protocols on a specified date

Specify a date and view the data egress by JSON, REST, or SOAP protocols on that date. You can select a record from the data to view more information.

Do the steps.

1.  Select the **Data Egress** tab.
2.  From the Filter by list, select **API**.
3.  Move the pointer to a date on the graph, and select an API protocol.

    ![API protocol graph.](../images/ihub-usage-select-date.png)

    The data egress by the selected API protocol on the selected date appears.

    ![Data egress by date.](../images/ihub-usage-protocol-date.png)

4.  To view more data on a specific record, select the View Aggregate Breakdown icon ![Drill down icon.](../images/ihub-usage-drill-down-icon.png).

    ![Data egress API trends.](../images/ihub-usage-api-prot-trends.png)

    The transaction log appears.

    ![Transaction log.](../images/ihub-usage-transac-log.png)


## Reports on data egress by export

View information on the data egress from the ServiceNow instance by URI and export sets.

To access the reports, do the steps.

1.  Select the **Data Egress** tab.
2.  From the Filter by list, select **Export**.

## Reports on data egress by export sets or URI

To access the reports on data egress by export sets or URI, do the steps.

1.  On the Data Egress by Exports report pie-chart, select the data export type. For example, export sets.

    ![Data egress by export type.](../images/ihub-usage-egress-export-uri.png)

    The date-wise data exports by the source you specified appears.

    ![Export source-wise data.](../images/ihub-usage-export-set.png)

2.  To view more information on an export set on a date, select the View Aggregate Breakdown icon ![Drill down icon.](../images/ihub-usage-drill-down-icon.png).

    ![Select the View Aggregate Breakdown icon.](../images/ihub-usage-export-drilldown.png)

    The data appears.


## Date-wise data egress by exports

View data egress by exports on a date that you specify.

Do the following steps.

1.  On the Data Egress Trends report, move the pointer to a date and then select the export type. For example, move the pointer to April 19, and then select Export Sets.

    ![Data export by export type on a date.](../images/ihub-usage-export-by-date.png)

    The egress data on the export type and date that you specified appears.

    ![Date-wise and source-wise egress data.](../images/ihub-usage-export-date.png)

2.  To view more data on a specific record, select the View Aggregate Breakdown icon ![Drill down icon.](../images/ihub-usage-drill-down-icon.png).

![View Aggregate Breakdown icon.](../images/ihub-usage-export-drill-down.png)

The data appears.

![Drill-down data.](../images/ihub-usage-datewise-export-egress.png)

## Data generation in the reports

Data in the reports are generated from the `data_egress_count` table. [View](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1638468) how data is populated in the `data_egress_count`.

**Parent Topic:**[Integration Hub Usage Dashboard](../concept/integrationhub-usage-dashboard.md)


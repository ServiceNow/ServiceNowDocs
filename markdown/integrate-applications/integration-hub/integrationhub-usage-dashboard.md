---
title: Integration Hub Usage Dashboard
description: Get insights on the usage of Integration Hub data from the Integration Hub Usage Dashboard. For example, view the average number of monthly transactions in the last year or the data egress from Integration Hub via REST and SOAP API protocols. Also reuse this short description in the release notes.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configure, Integration Hub, Workflow Data Fabric]
---

# Integration Hub Usage Dashboard

Get insights on the usage of Integration Hub data from the Integration Hub Usage Dashboard. For example, view the average number of monthly transactions in the last year or the data egress from Integration Hub via REST and SOAP API protocols.

The Integration Hub Usage Dashboard gives insights in the form of reports. Access to the dashboard is role-based. The reports are available under various sections in the **Transactions** and **Data Egress** tabs. You can customize the data that you want to view by using filters or drilling down reports.

![Integration Hub Dashboard elements and layout.](../images/ih-dashboard-layout.png)

## Integration Hub Usage Dashboard version

Integration Hub Usage Dashboard v3.0.0 is the latest version.

## Sections in the Transactions tab of the Integration Hub Usage Dashboard

The dashboard has these sections:

-   [Overview](../reference/use-the-integration-hub-usage-dashboard.md#section_jwh_yvn_y5b): View the usage data on the transactions from various perspectives and, if needed, drill down to view more details. For example, you could view the monthly transactions in the last year.
-   [Spokes](../reference/use-the-integration-hub-usage-dashboard.md#fig_stt_djw_z5b): View the data on the transactions that were performed by the spokes and, if needed, drill down to view more details. For example, you can view the information on which spoke performed the highest number of transactions in the last year.
-   [Protocols and Features](../reference/use-the-integration-hub-usage-dashboard.md#section_kf3_5sw_z5b): View the usage data on the various protocols and features that were used to and, if needed, drill down to view more details. For example, you can view the number of transactions that were performed with the REST protocol in the last year.

## Sections in the Data Egress tab of the Integration Hub Usage Dashboard

The dashboard has these sections. All sections have three common reports: Data Egress, Data Egress by source \(API protocols or exports\), and Data Egress Trends.

-   [Overview section](../reference/ihub-dashboard-api-egress.md#section_y3v_2tq_zbc): Gives an overview of the total data egress volume, data egress by REST and SOAP protocols, JSON, Export set, and URI from the ServiceNow instance, and the data egress across time periods.
-   [API section](../reference/ihub-dashboard-api-egress.md#section_epn_pxq_zbc): Gives an overview of the total data egress volume by all sources, data egress by REST or SOAP protocols or JSON data from the ServiceNow instance, and the data egress across time periods.
-   [Export section](../reference/ihub-dashboard-api-egress.md#section_kyn_byq_zbc): Gives an overview of the total data egress volume by all data export formats, data egress by export formats from the ServiceNow instance, and the data egress across time periods.

**Note:**

-   There’s no order in which you must view the reports, set the filters, or customize the columns in the report tables.
-   All charts are adjusted to the nearest data metric starting with Bytes.

## Data organization in the dashboard

The following images show how data is organized in the dashboard.

![Transactions section in the Integration Hub Dashboard.](../images/integration-hub-dashboard.png)

![Data Egress section in the Integration Hub Usage Dashboard.](../images/data-egress-section.png)

-   **[Get insights from the Integration Hub Usage Dashboard](../tasks/use-integrationhub-usage-dashboard.md)**  
Use the Integration Hub Usage Dashboard to get insights on the Integration Hub transactions. For example, you can view which protocol was the most used in the transactions in the last year. You can also use filters and customize the layout and arrangement of the columns in the reports.
-   **[Transaction reports in Integration Hub Usage Dashboard](../reference/use-the-integration-hub-usage-dashboard.md)**  
The transaction reports in Integration Hub Usage Dashboard help you to understand the Integration Hub usage transactions.
-   **[Data egress reports in the Integration Hub Usage Dashboard](../reference/ihub-dashboard-api-egress.md)**  
The Data egress reports give insights on data egress from the ServiceNow instance through API protocols or export sets. You can view more information when you select specific records.

**Parent Topic:**[Configuring Integration Hub](configuring-integration-hub.md)


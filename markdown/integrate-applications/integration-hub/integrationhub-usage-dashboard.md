---
title: Integration Hub Usage Dashboard
description: Get insights on the usage of Integration Hub data from the Integration Hub Usage Dashboard. For example, view the average number of monthly transactions in the last year or the data egress from Integration Hub via REST and SOAP API protocols. Also reuse this short description in the release notes.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/integration-hub/integrationhub-usage-dashboard.html
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

\[Omitted image "ih-dashboard-layout.png"\] Alt text: Integration Hub Dashboard elements and layout.

## Integration Hub Usage Dashboard version

Integration Hub Usage Dashboard v3.0.0 is the latest version.

## Sections in the Transactions tab of the Integration Hub Usage Dashboard

The dashboard has these sections:

-   [Overview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/integration-hub/use-the-integration-hub-usage-dashboard.md): View the usage data on the transactions from various perspectives and, if needed, drill down to view more details. For example, you could view the monthly transactions in the last year.
-   [Spokes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/integration-hub/use-the-integration-hub-usage-dashboard.md): View the data on the transactions that were performed by the spokes and, if needed, drill down to view more details. For example, you can view the information on which spoke performed the highest number of transactions in the last year.
-   [Protocols and Features](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/integration-hub/use-the-integration-hub-usage-dashboard.md): View the usage data on the various protocols and features that were used to and, if needed, drill down to view more details. For example, you can view the number of transactions that were performed with the REST protocol in the last year.

## Sections in the Data Egress tab of the Integration Hub Usage Dashboard

The dashboard has these sections. All sections have three common reports: Data Egress, Data Egress by source \(API protocols or exports\), and Data Egress Trends.

-   [Overview section](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/integration-hub/ihub-dashboard-api-egress.md): Gives an overview of the total data egress volume, data egress by REST and SOAP protocols, JSON, Export set, and URI from the ServiceNow instance, and the data egress across time periods.
-   [API section](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/integration-hub/ihub-dashboard-api-egress.md): Gives an overview of the total data egress volume by all sources, data egress by REST or SOAP protocols or JSON data from the ServiceNow instance, and the data egress across time periods.
-   [Export section](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/integration-hub/ihub-dashboard-api-egress.md): Gives an overview of the total data egress volume by all data export formats, data egress by export formats from the ServiceNow instance, and the data egress across time periods.

**Note:**

-   There’s no order in which you must view the reports, set the filters, or customize the columns in the report tables.
-   All charts are adjusted to the nearest data metric starting with Bytes.

## Data organization in the dashboard

The following images show how data is organized in the dashboard.

\[Omitted image "integration-hub-dashboard.png"\] Alt text: Transactions section in the Integration Hub Dashboard.

\[Omitted image "data-egress-section.png"\] Alt text: Data Egress section in the Integration Hub Usage Dashboard.

-   **[Get insights from the Integration Hub Usage Dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/integration-hub/use-integrationhub-usage-dashboard.md)**  
Use the Integration Hub Usage Dashboard to get insights on the Integration Hub transactions. For example, you can view which protocol was the most used in the transactions in the last year. You can also use filters and customize the layout and arrangement of the columns in the reports.
-   **[Transaction reports in Integration Hub Usage Dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/integration-hub/use-the-integration-hub-usage-dashboard.md)**  
The transaction reports in Integration Hub Usage Dashboard help you to understand the Integration Hub usage transactions.
-   **[Data egress reports in the Integration Hub Usage Dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/integration-hub/ihub-dashboard-api-egress.md)**  
The Data egress reports give insights on data egress from the ServiceNow instance through API protocols or export sets. You can view more information when you select specific records.

**Parent Topic:**[Configuring Integration Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/integration-hub/configuring-integration-hub.md)


---
title: Transaction reports in Integration Hub Usage Dashboard
description: The transaction reports in Integration Hub Usage Dashboard help you to understand the Integration Hub usage transactions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/integrate-applications/integration-hub/use-the-integration-hub-usage-dashboard.html
release: yokohama
product: Integration Hub
classification: integration-hub
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Integration Hub Usage Dashboard, Configuring Integration Hub, Integration Hub, Data and Automation]
---

# Transaction reports in Integration Hub Usage Dashboard

The transaction reports in Integration Hub Usage Dashboard help you to understand the Integration Hub usage transactions.

## Overview section reports

-   **IH Transactions \(Tx\) Usage report**

    Depending on the package that your organization subscribes to, the Integration Hub subscription packages offer a certain number of transactions per year. See the details about the packages in [Integration Hub usage and subscription](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/integrate-applications/integration-hub/subscription-usage.md). With this report, you can learn about the total usage of the Integration Hub transactions versus the subscribed package of transactions in the last year. The following diagram shows what you can learn from viewing the Integration Hub transactions usage.

    \[Omitted image "ih-transactions-tx-usage.png"\] Alt text: Integration Hub Transactions Usage report.

    **Note:** The number of transactions you have used from the package is the sum of the transactions that you have performed in Integration Hub, External Content Connectors, and Orchestration. The Transactions \(Tx\) by Type report shows the transactions that you have performed in Integration Hub, External Content Connectors, and Orchestration. See the image.

    \[Omitted image "ihub-usage-dashbrd-sum-of-transac.png"\] Alt text: Source-wise transactions.

    As shown in the following example, you can click a graph to view more details about the transactions.

    \[Omitted image "drill-down-transactions-tx-usage.png"\] Alt text: Integration Hub Transactions Usage report details.

-   **Transactions by Type report**

    As shown in the following diagram, you can use the Transactions by Type report to view the total transactions by their types.

    \[Omitted image "ihub-dashboard-transac-by-type.png"\] Alt text: Transactions by type report.

-   **Transactions \(Tx\) per Caller Scope report**

    The applications that perform the transactions are known as caller scopes. The Transactions \(Tx\) per Caller Scope report enables you to view the transactions per caller scope. As shown in the following diagram, you can also drill down and view the transactions that are performed by the spokes that are under different caller scopes.

    \[Omitted image "transactions-tx-per-caller-scope.png"\] Alt text: Transactions per Caller Scope report.

    As shown in the following example, you can click a graph to view more details such as the spoke transactions, what the caller scope of the spoke is, the total transaction count, and more. You can also group the transactions under a specific parameter in the table.

    \[Omitted image "drill-down-transactions-tx-per-caller-scope.png"\] Alt text: Transactions per Caller Scope report details.

-   **Transactions by Month report**

    As shown in the following diagram, the Transactions by Month report enables you to view the total transactions that are performed from each business unit and the Integration Hub subscription pool per month.

    \[Omitted image "transactions-by-month-report.png"\] Alt text: Transactions by Month report.

    **Tip:** To view the pop-up window that shows the business unit transactions, on the Y-axis, click just above the month that you want to view the report for.

    As shown in the following diagram, you can drill down and view more details of the transactions of a business unit pool. On the graph, click the small colored circle that indicates the business unit. For example, you can click the colored circle representing the HR business unit pool icon \[Omitted image "bu-colored-circle.png"\] Alt text: Colored circle representing the HR business unit pool icon. to see the details of the HR business unit pool.

    \[Omitted image "details-transaction-by-month-report.png"\] Alt text: Transactions by Month details.


## Spokes section reports

-   **Top Spokes report**

    With the Top Spokes report that is shown in the following diagram, you can view the top 10 spokes that performed the largest number of transactions.

    \[Omitted image "top-spokes-report.png"\] Alt text: Top Spokes report.

    As shown in the following example, you can drill down and view more details about the transactions that are performed by a specific spoke by clicking the graph that represents the spoke.

    \[Omitted image "drill-down-top-spokes-report.png"\] Alt text: Details of the transactions by a spoke.

-   **Top Spoke Actions report**

    As shown in the following diagram, this report displays the names of the top actions that are performed by spokes. You can also drill down to view more details.

    \[Omitted image "top-spoke-actions.png"\] Alt text: Top Spoke actions report.

    As shown in the following example, you can drill down and view more details of a specific action by clicking the slice.

    \[Omitted image "drill-down-top-spoke-actions.png"\] Alt text: Details of Top Spoke Actions report.

-   **Custom Spoke Transaction Usage report**

    As shown in the following diagram, you can view the transaction usage by the custom spokes in the Custom Spoke Transaction Usage report. You can also drill down and view the details of the report.

    \[Omitted image "custom-spoke-transaction-usage-report.png"\] Alt text: Custom Spoke Transaction Usage report.

    As shown in the following example, you can drill down by clicking the slice.

    \[Omitted image "drill-down-custom-spoke-transaction-usage.png"\] Alt text: Custom Spoke Transaction Usage report details.


## Protocols and Features reports

-   **Protocol Usage report**

    Spokes use different protocols while performing transactions. As shown in the following diagram, you can use the Protocol Usage report to view the usage of the various protocols. You can drill down to view more details.

    \[Omitted image "protocol-usage-report.png"\] Alt text: Protocol Usage report.

    As shown in the following example, you can drill down and view the details of transactions with a protocol by clicking the graph that represents a protocol.

    \[Omitted image "drill-down-protocol-usage.png"\] Alt text: Details of Protocol usage report.

-   **Feature Usage**

    The Spokes use different features while performing transactions. This report gives the usage of the various features. You can drill down to view more details.

    \[Omitted image "feature-usage-report.png"\] Alt text: Feature Usage report.

    To drill down, click the graph representing a feature.

    \[Omitted image "drill-down-feature-usage.png"\] Alt text: Feature Usage report details.


**Parent Topic:**[Integration Hub Usage Dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/integrate-applications/integration-hub/integrationhub-usage-dashboard.md)


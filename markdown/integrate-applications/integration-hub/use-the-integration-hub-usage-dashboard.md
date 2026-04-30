---
title: Transaction reports in Integration Hub Usage Dashboard
description: The transaction reports in Integration Hub Usage Dashboard help you to understand the Integration Hub usage transactions.
locale: en-US
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Integration Hub Usage Dashboard, Configuring Integration Hub, Integration Hub, Creating integrations with applications]
---

# Transaction reports in Integration Hub Usage Dashboard

The transaction reports in Integration Hub Usage Dashboard help you to understand the Integration Hub usage transactions.

## Overview section reports

-   **IH Transactions \(Tx\) Usage report**

    Depending on the package that your organization subscribes to, the Integration Hub subscription packages offer a certain number of transactions per year. See the details about the packages in [Integration Hub usage and subscription](../../flow-designer/concept/subscription-usage.md). With this report, you can learn about the total usage of the Integration Hub transactions versus the subscribed package of transactions in the last year. The following diagram shows what you can learn from viewing the Integration Hub transactions usage.

    ![Integration Hub Transactions Usage report.](../images/ih-transactions-tx-usage.png "Integration Hub Transactions (Tx) Usage report")

    **Note:** The number of transactions you have used from the package is the sum of the transactions that you have performed in Integration Hub, External Content Connectors, and Orchestration. The Transactions \(Tx\) by Type report shows the transactions that you have performed in Integration Hub, External Content Connectors, and Orchestration. See the image.

    ![Source-wise transactions.](../images/ihub-usage-dashbrd-sum-of-transac.png)

    As shown in the following example, you can click a graph to view more details about the transactions.

    ![Integration Hub Transactions Usage report details.](../images/drill-down-transactions-tx-usage.png "Integration Hub Transactions (Tx) Usage report details")

-   **Transactions by Type report**

    As shown in the following diagram, you can use the Transactions by Type report to view the total transactions by their types.

    ![Transactions by type report.](../images/ihub-dashboard-transac-by-type.png "Transactions by Type report")

-   **Transactions \(Tx\) per Caller Scope report**

    The applications that perform the transactions are known as caller scopes. The Transactions \(Tx\) per Caller Scope report enables you to view the transactions per caller scope. As shown in the following diagram, you can also drill down and view the transactions that are performed by the spokes that are under different caller scopes.

    ![Transactions per Caller Scope report.](../images/transactions-tx-per-caller-scope.png "Transactions (Tx) per Caller Scope report")

    As shown in the following example, you can click a graph to view more details such as the spoke transactions, what the caller scope of the spoke is, the total transaction count, and more. You can also group the transactions under a specific parameter in the table.

    ![Transactions per Caller Scope report details.](../images/drill-down-transactions-tx-per-caller-scope.png "Transactions (Tx) per Caller Scope report details")

-   **Transactions by Month report**

    As shown in the following diagram, the Transactions by Month report enables you to view the total transactions that are performed from each business unit and the Integration Hub subscription pool per month.

    ![Transactions by Month report.](../images/transactions-by-month-report.png "Transactions by Month report")

    **Tip:** To view the pop-up window that shows the business unit transactions, on the Y-axis, click just above the month that you want to view the report for.

    As shown in the following diagram, you can drill down and view more details of the transactions of a business unit pool. On the graph, click the small colored circle that indicates the business unit. For example, you can click the colored circle representing the HR business unit pool icon ![Colored circle representing the HR business unit pool icon.](../images/bu-colored-circle.png) to see the details of the HR business unit pool.

    ![Transactions by Month details.](../images/details-transaction-by-month-report.png "Transactions by Month report details")


## Spokes section reports

-   **Top Spokes report**

    With the Top Spokes report that is shown in the following diagram, you can view the top 10 spokes that performed the largest number of transactions.

    ![Top Spokes report.](../images/top-spokes-report.png "Top Spokes report")

    As shown in the following example, you can drill down and view more details about the transactions that are performed by a specific spoke by clicking the graph that represents the spoke.

    ![Details of the transactions by a spoke.](../images/drill-down-top-spokes-report.png "Top Spoke report details")

-   **Top Spoke Actions report**

    As shown in the following diagram, this report displays the names of the top actions that are performed by spokes. You can also drill down to view more details.

    ![Top Spoke actions report.](../images/top-spoke-actions.png "Top Spoke Actions report")

    As shown in the following example, you can drill down and view more details of a specific action by clicking the slice.

    ![Details of Top Spoke Actions report.](../images/drill-down-top-spoke-actions.png "Top Spoke Actions details")

-   **Custom Spoke Transaction Usage report**

    As shown in the following diagram, you can view the transaction usage by the custom spokes in the Custom Spoke Transaction Usage report. You can also drill down and view the details of the report.

    ![Custom Spoke Transaction Usage report.](../images/custom-spoke-transaction-usage-report.png "Custom Spoke Transaction Usage report")

    As shown in the following example, you can drill down by clicking the slice.

    ![Custom Spoke Transaction Usage report details.](../images/drill-down-custom-spoke-transaction-usage.png "Custom Spoke Transaction Usage report details")


## Protocols and Features reports

-   **Protocol Usage report**

    Spokes use different protocols while performing transactions. As shown in the following diagram, you can use the Protocol Usage report to view the usage of the various protocols. You can drill down to view more details.

    ![Protocol Usage report.](../images/protocol-usage-report.png "Protocol Usage report")

    As shown in the following example, you can drill down and view the details of transactions with a protocol by clicking the graph that represents a protocol.

    ![Details of Protocol usage report.](../images/drill-down-protocol-usage.png "Details of Protocol usage report details")

-   **Feature Usage**

    The Spokes use different features while performing transactions. This report gives the usage of the various features. You can drill down to view more details.

    ![Feature Usage report.](../images/feature-usage-report.png "Feature Usage report")

    To drill down, click the graph representing a feature.

    ![Feature Usage report details.](../images/drill-down-feature-usage.png "Feature Usage report details")


**Parent Topic:**[Integration Hub Usage Dashboard](../concept/integrationhub-usage-dashboard.md)


---
title: Configure impact metrics
description: Configure the Key Performance Indicators \(KPIs\) for this process.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/now-intelligence/process-mining/impact-metrics.html
release: yokohama
product: Process Mining
classification: process-mining
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [With Process Configuration Builder, Creating process configuration, Using Process Mining, Process Mining, Platform Analytics]
---

# Configure impact metrics

Configure the Key Performance Indicators \(KPIs\) for this process.

## Before you begin

Role required: sn\_process\_optimization\_power\_user or sn\_process\_optimization\_admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Process Mining Workspace**.

2.  On the side of the page, select the Process configurations icon \(\[Omitted image "icon-process-config.png"\] Alt text: Process configuration builder\).

3.  Open a table from the **Configurations** tab.

    The **Process details** page is displayed. Select **Impact metrics** from the left bar.

    If you’re proceeding from the **Investigative features** page, then you come to this page. For more information, see [Configure investigative features](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/now-intelligence/process-mining/investigative-features.md).

    The **Impact metrics** page has two sections:

    -   KPI dashboard
    -   KPI categories
    \[Omitted image "impact-metrics-proc-con.png"\] Alt text: Impact metrics in process configuration

4.  Select a Platform Analytics Key Performance Indicators \(KPIs\) dashboard.

    Select the help icon \(?\) to view details about how and why these details must be set. You also get a list of resources.

    If you want to create a new KPI dashboard, select **New Dashboard**. For more information, see [Create a dashboard with the in-line editor](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/now-intelligence/create-db-in-ac.md).

5.  Provide values for each KPI categories.

    Select the help icon \(?\) to view details about how and why these details must be set. You also get a list of resources.

    **Note:** The KPI categories are dynamic and are retrieved from the sys\_choice table, which includes category order and hint information.

6.  Select **Continue to improvement opportunities**.


**Parent Topic:**[Create process configuration using Process Configuration Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/now-intelligence/process-mining/process-config-builder.md)


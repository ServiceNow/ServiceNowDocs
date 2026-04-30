---
title: Workflow Data Fabric Credits
description: Workflow Data Fabric Credits let you monitor and track Workflow Data Fabric product usage through a dashboard showing credit usage, usage measurements, and thresholds that trigger alerts.Workflow Data Fabric lets organizations connect, manage, and automate their data workflows across different systems, through various product solutions.You must have Workflow Data Fabric license to use Workflow Data Fabric Credits.Credit usage is measured for each account. The number of credits you use for a feature is determined by the terms of the Workflow Data Fabric license.The Usage Dashboard shows credit usage, usage measurements, and thresholds that trigger alerts.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Data and Automation]
---

# Workflow Data Fabric Credits

Workflow Data Fabric Credits let you monitor and track Workflow Data Fabric product usage through a dashboard showing credit usage, usage measurements, and thresholds that trigger alerts.

For more information about Workflow Data Fabric benefits, the workflow for the solution, and requirements for integrating the solution, see [Accelerating and automating your repetitive tasks by using Workflow Data Fabric](../../../solutions/concept/accelerate-automate-engine-rpa.md).

## Exploring Workflow Data Fabric Credits

Workflow Data Fabric lets organizations connect, manage, and automate their data workflows across different systems, through various product solutions.

Workflow Data Fabric Credits measure the usage of Workflow Data Fabric subscriptions. Each credit represents a unit of consumption under a unified meter. For example, depending on the underlying product a credit can represent a record, an API call, a megabyte of data throughput, or a minute of runtime.

For more information about Workflow Data Fabric products, meters, and reproducibility, see the [Fabric Credits - WDF Products and Meter Sources to trace and reproduce \[KB2276348\]](https://support.servicenow.com/kb?sys_kb_id=6778a81293aa2e54f538fb2d6cba10c1&id=kb_article_view) article in the Now Support Knowledge Base.

For more information about Workflow Data Fabric Credits, see the [Count of Workflow Data Fabric Credits consumed in the last 367 Days \[KB2239792\]](https://support.servicenow.com/kb?sys_kb_id=6778a81293aa2e54f538fb2d6cba10c1&id=kb_article_view) article in the Now Support Knowledge Base.

## Configure Workflow Data Fabric Credits

You must have Workflow Data Fabric license to use Workflow Data Fabric Credits.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the WDF Tokenization application \(sn\_wdf\_token\) using the filter criteria and search bar.

    You can search for the application by its name or ID. If you can’t find the application, you might have to request it from the ServiceNow Store.

    In the list next to the **Install** button, the versions that are available to you are displayed.

3.  Select a version from the list and select **Install**.

    In the Review Installation Details dialog box, any dependencies installed with your application are listed.

4.  If you're prompted, follow the links to the ServiceNow Store to get any additional entitlements for dependencies.

5.  If demo data is available and you want to install it, select the **Load demo data** check box.

    Demo data are sample records that describe application features for common use cases. Load the demo data when you first install the application on a development or test instance.

6.  Select **Install**.


## Measuring usage

Credit usage is measured for each account. The number of credits you use for a feature is determined by the terms of the Workflow Data Fabric license.

|Measurement category|Description|
|--------------------|-----------|
|Transactions|Measured in API calls, assets, records, or transactions.|
|Data volume|Measured in MB/GB.|
|Usage|Measured in runtime.|

## Usage Dashboard

The Usage Dashboard shows credit usage, usage measurements, and thresholds that trigger alerts.

Access the Usage Dashboard by navigating to **All** &gt; **Workflow Data Fabric Usage** &gt; **Usage Dashboard**. The Credit Dashboard has two tabs: **Overall usage** and **Product breakdown**.

-   **Overall usage tab**

    Provides a detailed analysis of credit usage with specific KPIs and a usage trend chart. View data by total credits entitled, credits used, daily average, credits remaining, and overall usage trend.![Screenshot showing an Overall usage analysis in the Usage Dashboard.](../images/tokens-dashboard-overall.png)

-   **Product breakdown tab**

    Provides an overview of credit usage by product. You can filter the data that is displayed by date range and selected product. View the usage trend by product and detailed product metrics.![Screenshot showing a product breakdown analysis in the Usage Dashboard.](../images/tokens-dashboard-product.png)



---
title: Benchmarks overview
description: The ServiceNow Benchmarks application securely collects daily data on your instance and then aggregates the data into monthly global benchmark reports.
locale: en-US
release: yokohama
product: Benchmarks
classification: benchmarks
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 6
breadcrumb: [Benchmarks, IT Service Management]
---

# Benchmarks overview

The ServiceNow Benchmarks application securely collects daily data on your instance and then aggregates the data into monthly global benchmark reports.

This video provides an overview of how you can get started with Benchmarks.

Getting started with Benchmarks

Performance Analytics collects daily data on customer instances. The data from the previous month is uploaded at the beginning of the following month via a scheduled job. If there are any errors, there are multiple retries.

During the month the data is uploaded, the data is aggregated and monthly results \(your instance results, global results, and your ranking\) are downloaded to the customer instance by 21st of every month. Monthly recommendation candidates are provided that you can implement to help improve your KPI performance. An email notification is sent when the global data is available.

ServiceNow has over 2850 customers that have opted into the Benchmarks program. All ServiceNow customers are allowed to participate in the Benchmarks program by opting in from their ServiceNow production instance, except:

-   Express customers
-   Federal customers
-   Customers with on-premise instances

**Note:** You must have a production instance to opt into the Benchmarks program.

Managed Service Providers \(MSPs\) and MSP-managed instances are supported and have exclusive access to global MSP aggregate score data. All instances will support the following benchmarks that can be downloaded for comparison in the Benchmarks dashboard:

-   Global, which applies to all customers
-   Industry category
-   User size, based on active user count
-   Companies in your industry category and those that are of similar size to your company
-   Geographical regions

**Note:**

-   These benchmarks aren’t calculated using MSP data.
-   Along with the above Benchmarks, you will also receive the top performers in each of these categories.

Changing KPI configuration within the month requires one to two months of data collection before your monthly values reflect that change.

**Note:** The Benchmark Scheduler \(bm.scheduler\) user is added with Benchmarks. It’s required for Benchmarks data collection.

## Key features

-   Available KPIs from other ServiceNow applications such as ITSM, ITOM, Security Operations. For more information, see [Benchmark KPIs](c_BenchKPIConfig.md).
-   Ability to change KPI definitions to match customizations.
-   Benchmarks dashboard in Service Portal \(mobile friendly\).
-   Ability to download KPI reports.
-   Ability to filter data based on the following parameters:
    -   Industry, number of users, or geographical region.
    -   Companies in your industry category and of similar user size.
-   Email notification when new aggregate monthly data is available.
-   Percentile ranking to indicate your standing within your participating peer group.
-   Recommendation candidates with guided setup to help improve KPI performance.
-   Product category-based roles to limit data access.
-   Integration with Performance Analytics for daily data collection and drill-down on KPI data.

![Benchmarks dashboard](../image/BenchITSMTileView.png "Benchmarks dashboard")

<table id="table_llt_zby_c1b"><thead><tr><th>

Benefit

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Global anonymity

</td><td>

Viewers in your organization have access benchmarks for your organization, however the global benchmarks are anonymous, and don’t include any company information.

</td></tr><tr><td>

Industry comparison

</td><td>

Using the **Compare with** drop-down in the Benchmarks dashboard, you can filter the benchmarks results by industry, ServiceNow user size, or geographical region to make the results more relevant to your organization.

-   Industry is determined based on the standard industry code in the account record for the company.
-   Number of users is determined by the number of ServiceNow active users within the company, so you can compare your company to similar-sized ServiceNow implementations to gain insight about your company.
-   Region is determined based on the **Region** field in the company table.

If a filter category includes fewer than 20 participants, the corresponding data is shown in the **Other** category.

</td></tr><tr><td>

Trends

</td><td>

You can see the results of all published KPIs as well as the previous six months of history.You can then use the trend data to measure and report on service delivery progress over a period of time to determine what is working well and what needs improvement.

</td></tr><tr><td>

Recommendations

</td><td>

Data is analyzed and recommendation candidates are provided to help improve the performance of your KPIs. All recommendations are dynamic and are updated monthly, based on data from the previous month.

</td></tr><tr><td>

Reports

</td><td>

Benchmarks reports get refreshed monthly, which can be downloaded in PDF format. An email notification is sent to the customer when new data is available.

</td></tr></tbody>
</table>## Email notification

Users with the Benchmarks admin \(sn\_bm\_client.benchmark\_admin\) and Benchmarks data viewer \(sn\_bm\_client.benchmark\_data\_viewer\) roles automatically receive email notification regarding availability of monthly scores, historical data recalculation, and new KPIs. You must have system admin \(admin\) role to modify the email recipient list.

-   An email containing notification information is sent when the monthly global data is available. Monthly results \(your instance results, and global results\) are downloaded to the customer instance mid month.
    -   Subject: New Monthly Benchmarks report is available now
    -   Body: ServiceNow Benchmarks has been updated with &lt;month&gt; data. You can see the updated Benchmarks by viewing the Benchmarks Dashboard &lt;Benchmarks Dashboard Portal link&gt;.
-   An email containing notification information is sent when historical data for the past six months is recalculated.
    -   Subject: Historical Global Benchmarks scores have been refreshed
    -   Body: The global Benchmarks scores of last six months have been recalculated with improved data quality. You can see the updated Benchmarks by visiting Benchmarks Dashboard &lt;Benchmark Dashboard Portal Link&gt;.
-   An email containing notification information is sent when an updated KPI version is introduced \(with some fixes, for example\).
    -   Subject: One or more Benchmarks KPI versions have changed
    -   Body: The latest Benchmarks scores have a new version of following KPIs with improved data quality.

        &lt; KPI name&gt;.

        You can see the updated Benchmarks by visiting Benchmarks Dashboard &lt;Benchmark Dashboard Portal Link&gt;.


Benchmarks notification emails are accessed using the **System Settings** &gt; **Notifications** navigation menu.

## Benchmarks data transfer

Your Benchmarks score data is automatically uploaded to ServiceNow on the third day of the month. Global scores are automatically downloaded to your instance on the 11th day of the month.

You can manually upload or download scores beyond those days of the month \(on demand\) by executing the Benchmarks scores scheduled jobs through the **System Definition** &gt; **Scheduled Jobs** navigation item.

-   Upload the benchmark scores \(automatically runs on the first day of the month\)
-   Download the benchmark scores \(automatically runs on the ninth day of the month\)

These on-demand scheduled jobs are useful if, for any reason, there was a failure in the automatic upload or download scores process and it is after the cutoff dates. You can also run a scheduled job to generate six months of historical data.

## Benchmarks KPI categories

Benchmarks supports KPIs from other ServiceNow applications such as ITSM, ITOM, Security Operations, Conversational Interfaces, Success Dashboard, and Strategic Portfolio Management. For more information, see [Benchmark KPIs](c_BenchKPIConfig.md).

**Note:** The categories do not display on the Benchmarks dashboard unless, any KPI is opted in for tracking the metrics in Benchmarks.

**Parent Topic:**[Benchmarks](../reference/r_Benchmarks.md)


---
title: Vendor KPI Groups in Vendor Management Workspace reference
description: Use Vendor KPI Groups that are provided by default to analyze vendor performance.
locale: en-US
release: xanadu
product: Vendor Management Workspace
classification: vendor-management-workspace
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Vendor Management Workspace reference, Vendor Management Workspace, IT Service Management]
---

# Vendor KPI Groups in Vendor Management Workspace reference

Use Vendor KPI Groups that are provided by default to analyze vendor performance.

## Vendor KPI Groups

The following Vendor Key Performance Indicator \(KPI\) groups are available by default:

-   IT Services—Includes KPIs to analyze vendor performance related to IT Services.
-   Vendor Fulfillment—Includes KPIs to analyze vendor performance related to fulfillment.
-   Software—Includes KPIs to analyze vendors related to software applications.
-   Hardware—Includes KPIs to analyze vendors related to hardware applications.

Each KPI group provided by default has the following related lists:

-   KPIs—Indicators with a vendor breakdown that measure the performance of your vendors.

    Each indicator that contributes toward the vendor score has a weight associated with it.

-   KPI group thresholds—Defines threshold values to indicate the status of each KPI group.
-   Vendors—List of vendors to analyze their performance.

**IT Services KPI Group**

This table shows the indicators provided by default in this KPI group. All indicators that have the unit as percentage are used to calculate the vendor score.

|Indicators name|Description|Unit|
|---------------|-----------|----|
|VMW: Average Customer Satisfaction|Measures CSAT scores based on service offerings.|Number|
|Vendor Satisfaction|Provides monthly breakdown of vendor satisfaction scores.|Percentage|
|VMW: Average SLA Achievement|Calculates average value for SLAs that have been successfully completed.|Number|
|VMW: Average Availability|Calculates average value achieved for incident SLAs.|Percentage|
|VMW: Average Request Activity|Average value calculated from fulfilled request items derived from service portfolio catalog items. These items must be connected to service offerings.|Number|
|Total Incidents Created|The total number of incidents created for vendors.|Number|

**Vendor Fulfillment KPI Group**

This table shows the indicators provided by default in this KPI group. All indicators that have the unit as percentage are used to calculate the vendor score.

|Indicator|Description|Unit|
|---------|-----------|----|
|VMW: Average Customer Satisfaction|Measures CSAT scores based on service offerings.|Number|
|Vendor Satisfaction|Provides monthly breakdown of vendor satisfaction scores.|Percentage|
|VMW: Average Incident SLA Achievement|Calculates average value achieved for incident SLAs that have been successfully completed.|Percentage|
|Average Request Fulfillment SLA Achievement|Calculates average value for SLAs that have been successfully completed.|Percentage|
|Total Incidents Created|The total number of incidents created for vendors.|Number|
|VMW: Average Request Activity|Average value calculated from fulfilled request items derived from service portfolio catalog items. These items must be connected to service offerings.|Number|

**Software KPI Group**

This table shows the indicators provided by default in this KPI group. All indicators that have the unit as percentage are used to calculate the vendor score.

|Indicator|Description|Unit|
|---------|-----------|----|
|Vendor Satisfaction|Provides monthly breakdown of vendor satisfaction scores.|Percentage|
|Vendor Requested Items|Provides the count of the vendor-requested catalog items.|Number|
|Manual SLA from External Source|Calculates the manually added SLAs.|Percentage|

**Hardware KPI Group**

This table shows the indicators provided by default in this KPI group. All indicators that have the unit as percentage are used to calculate the vendor score.

|Indicator|Description|Unit|
|---------|-----------|----|
|Vendor Satisfaction|Provides monthly breakdown of vendor satisfaction scores.|Percentage|
|Vendor Requested Items|Provides the count of the vendor-requested catalog items.|Number|
|Manual SLA from External Source|Calculates the manually added SLAs.|Percentage|

## Vendor score indicator

The **Vendor Score** indicator is an automated indicator. It’s used for calculating and displaying the vendor score. The calculation is done based on all indicators added to the KPI group for evaluating vendor performance.

By default, the following indicators are used to calculate the vendor score:

-   Average Request Fulfillment SLA Achievement
-   VMW: Average Availability
-   Average Incident SLA Achievement
-   Manual SLA from External Source

## Schedule job

The **VMW Update Vendor Score** scheduled job runs daily and updates the score. You can run this job on-demand to get updated scores at any time.

The **VMW Update Vendor Profile** scheduled job runs monthly and updates all vendor profiles. You can run this job on-demand to get updated vendor profiles at any time.

## Calculating the vendor score

The vendor score calculation is based on the weight of each indicator and the KPI score.

**Important:** The Service Offering Metric Data \[service\_offering\_metric\_data\] table along with the following four indicators have been deprecated in the Utah release:

-   Average SLA Achievement \[ServiceOffering.MetricData.SLA.Daily\]
-   Average Customer Satisfaction \[ServiceOffering.MetricData.CSAT.Daily\]
-   Average Availability \[ServiceOffering.MetricData.Availability.Daily\]
-   Average Request Activity \[ServiceOffering.MetricData.Activity.Daily\]

Therefore, if you have the Vendor Management Workspace application integrated with Service Portfolio Management, and if you are upgrading to the Service Portfolio Management standard portfolio, the metric data from the legacy indicators are no longer available. For information on Service Portfolio Management, see [Service Portfolio Management portfolios](../../service-portfolio-management2/concept/SPM2-service-portfolios.md).

You can calculate the vendor score using the indicators that have a percentage value. You can also create custom formula indicators and add them to your vendor score calculation. For more information, see [Add a formula indicator to track vendor score](../task/create-formula-indicator-vendor.md).

This table provides an example of how a vendor score is calculated.

|Indicator|Indicator weight|KPI score|Indicator score that contributes toward vendor score|
|---------|----------------|---------|----------------------------------------------------|
|Vendor Satisfaction|10.00%|54.42%|5.442%|
|VMW: Average Customer Satisfaction|55.00%|83.00%|45.65%|
|VMW: Average Availability|25.00%|88.50%|22.125%|
|VMW: Average SLA Achievement|10.00%|100.00%|10.00%|
|**Total**| | |**83.217%**|

The total vendor score has been rounded up to 83.22%. The score is also highlighted in the header with colors that are distinct for the defined threshold values for the KPI group.

**Note:** The vendor score is impacted based on whether the [direction for the indicator](https://www.servicenow.com/docs/access?context=t_CreateAnAutomatedIndicator&version=xanadu&pubname=xanadu-now-intelligence&ft:locale=en-US) is set to maximize or minimize. This table shows an example of how the vendor score is impacted based on the indicator direction.

<table id="table_hz2_qnj_gjb"><thead><tr><th>

Indicator

</th><th>

Direction

</th><th>

Indicator weight

</th><th>

Indicator metric score

</th><th>

Indicator score that contributes toward vendor score

</th></tr></thead><tbody><tr><td>

VMW: Vendor Satisfaction

</td><td>

Maximize

</td><td>

10.00%

</td><td>

54.42%

</td><td>

5.442%

</td></tr><tr><td>

VMW: Average Customer Satisfaction

</td><td>

Maximize

</td><td>

55.00%

</td><td>

83.00%

</td><td>

45.65%

</td></tr><tr><td>

VMW: Average Availability

</td><td>

Minimize

</td><td>

25.00%

</td><td>

88.50%

</td><td>

2.875%\[\(100 - 88.5\) x.25\]

</td></tr><tr><td>

VMW: Average SLA Achievement

</td><td>

Minimize

</td><td>

10.00%

</td><td>

100.00%

</td><td>

0%

</td></tr><tr><td>

**Total**

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

**53.967%**

</td></tr></tbody>
</table>**Parent Topic:**[Vendor Management Workspace reference](vendor-manager-workspace-reference.md)


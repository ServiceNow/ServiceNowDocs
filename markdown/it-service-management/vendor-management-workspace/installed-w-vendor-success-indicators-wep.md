---
title: Installed with Vendor Success Indicators in Vendor Management Workspace
description: Using the Vendor Success Indicators application, you can compare the performance of your vendors against other top-performing vendors.
locale: en-US
release: zurich
product: Vendor Management Workspace
classification: vendor-management-workspace
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Reference, Vendor Management Workspace, IT Service Management]
---

# Installed with Vendor Success Indicators in Vendor Management Workspace

Using the Vendor Success Indicators application, you can compare the performance of your vendors against other top-performing vendors.

**Important:** You must install the Success Indicators \(com.snc.vendor.insights\) plugin separately from the ServiceNow Store. For more information, see [Activate Vendor Management Workspace](../task/activate-vendor-management-configurable-workspace.md).

|Name|Description|
|----|-----------|
|Vendor Success Indicator Weekly Scheduled Job|Runs weekly and gathers vendor attributes data for the past 30 days. The job then computes the correlation of the attributes with high-performing vendors using Predictive Intelligence.|

<table id="table_evz_fln_dnb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_app\_ml\_insights.top\_n\_results

</td><td>

Top N results to retrieve from the Insight Results table for further analysis. Default value is 5.

</td></tr><tr><td>

sn\_app\_ml\_insights.max\_records\_to\_process

</td><td>

Maximum number of records to be processed by the Success Indicator job. Default value is 50000.

</td></tr><tr><td>

sn\_app\_ml\_insights.attr\_category\_string\_value\_limit

</td><td>

Maximum number of string values allowed before creating categories. Default value is 5.

</td></tr><tr><td>

sn\_app\_ml\_insights.keep\_last\_n\_runs

</td><td>

The number of the most recent executions to be retained after you run the table cleaner. Default value is 2.

</td></tr><tr><td>

sn\_app\_ml\_insights.attr\_datatype\_inclusion\_list

</td><td>

Comma separated list of valid data types to use for defining Vendor Insights attributes. Default value is boolean,currency,date,datetime,due\_date,field\_name,glide\_date,glide\_date\_time,glide\_list,int,integer,long,string,time,translated,translated\_field,translated\_text

</td></tr><tr><td>

sn\_app\_ml\_insights.chi\_squared\_critical\_value

</td><td>

The critical value for a chi-square test that compares two values to see if there is a statistical significance. Default value is 3.84.

</td></tr><tr><td>

sn\_app\_ml\_insights.chi\_squared\_threshold

</td><td>

The threshold for the critical value for the chi-square test. Default value is 5.

</td></tr></tbody>
</table>|Attribute Name|Attribute Type|Default value|
|--------------|--------------|-------------|
| |**Performance analytics indicators**| |
|Average Availability|Average Availability|true|
|Average SLA Achievement|Average SLA Achievement|true|
|Average Stability|Average Stability|true|
|Avg Customer Satisfaction|Average Customer Satisfaction|true|
|Avg Perf Score of SO|Average Performance Score of Service Offering|true|
|Vendor Satisfaction|Vendor Satisfaction|true|
| |**Table attributes**| |
|Contract SLA Commitment|SLA Definition \[contract\_sla\]|true|
|Contract SLA Type|SLA Definition \[contract\_sla\]|true|
|Country|Company \[core\_company\]|true|
|Rank Tier|Company \[core\_company\]|true|
|Relationship Start|Company \[core\_company\]|false|
|Service Commitment Type|Service commitment \[service\_commitment\]|true|
|Service Offering Business Criticality|Service Offering \[service\_offering\]|true|
|Total Contract Cost|Company \[core\_company\]|false|
|Unique Subscribers|Company \[core\_company\]|true|
|Vendor State|Company \[core\_company\]|false|
|Vendor Type|Company \[core\_company\]|false|

**Parent Topic:**[Vendor Management Workspace reference](vendor-manager-workspace-reference.md)


---
title: Allocate expenses using service offering allocation map
description: You can allocate expenses based on the actual consumption of services offered using the weighted method. In the weighted rollup method the metric weights the amount by the account values. Use the service offering allocation maps table to store your actual consumption data of the cost for service offerings.
locale: en-US
release: xanadu
product: Financial Management
classification: financial-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Financial Management for licensed SPM users, Financial Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Allocate expenses using service offering allocation map

You can allocate expenses based on the actual consumption of services offered using the weighted method. In the weighted rollup method the metric weights the amount by the account values. Use the service offering allocation maps table to store your actual consumption data of the cost for service offerings.

## Before you begin

Role required: cost\_transparency\_analyst

## About this task

Although the base system provides you with the default **Equal** method to roll up the expenses from the IT Shared Services segment to the Service Offering segment, you can also opt for **Weighted** rollup method. In this method, the expenses from the IT shared service segment are allocated to the service offering segment based on the consumption data that you have stored or entered in the Service Offering Allocation Map \[itfm\_service\_offering\_allocation\_map\] table. In this case, the expense is allocated based on the weightage of consumption. Therefore, cost is divided using **Allocate to Service Offering on Allocation Maps** metric and the Service Offering Allocation Map table that has the consumption data is used to weight the metric.

## Procedure

1.  Navigate to **All** &gt; **Financial Modeling for SPM** &gt; **Service Offering Allocation Maps**.

2.  Click **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Allocation Weight|Expenses allocated based on a weighted calculation.|
    |IT Shared Service|Segment from where the money is allocated.|
    |Service Offering|Segment to which the money is rolled up.|

4.  Click **Submit**.

    For more information on the calculated spend per offering and to configure the estimated spend offering cost source, see [Financial Management for Service Owner Workspace](https://www.servicenow.com/docs/access?context=financial-management-SPM2&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US).


**Parent Topic:**[Financial Management for licensed SPM users](../concept/financial-management-spm.md)


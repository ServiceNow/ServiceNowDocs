---
title: Convert metric data to a different unit
description: Convert any metric data into a preferred reporting unit.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/governance-risk-compliance/grc-risk-management-workspace/convert-md-irm.html
release: zurich
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, GRC: Metrics in Integrated Risk Management, Risk Management, Governance, Risk, and Compliance]
---

# Convert metric data to a different unit

Convert any metric data into a preferred reporting unit.

## Before you begin

Role required: admin

## About this task

The preferred reporting unit for any data is specified in a metric definition. When users enter the data in a metric data task, they may do so in a unit that is different from the unit set in the metric definition. For example, a user may enter data about water usage in liters but the organization needs the report in US gallons. And therefore, the metric definition is also set to gallons. In this case, liters must be converted to US gallons.

**Note:** In the metric data task, only those units that belong to the same unit family are available for the data. Unit conversion only applies to units that have the unit family conversion factor set to **Direct**.

## Procedure

1.  Navigate to **All** &gt; **Risk** &gt; **Administration** &gt; **Unit Conversions**.

2.  Select **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the unit conversion. For example, `Litres to gallons`.|
    |From unit|Unit to convert.|
    |To unit|Unit to convert to.|
    |Unit family|Unit family to which the unit belongs. For example, **Volume**.|
    |Value|Conversion value. For example, the conversion value from liters to gallons is `0.264172`.|

4.  Select **Submit**.


**Parent Topic:**[Configuring metrics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/grc-risk-management-workspace/configuring-irm-metrics.md)


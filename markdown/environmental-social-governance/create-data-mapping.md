---
title: Create data mapping
description: Create data mappings to import Watershed data from columns other than the pre-configured columns of the Watershed spreadsheet. By default, data import from three columns is supported.
locale: en-US
release: zurich
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Integrating ESG Management \(formerly ESG\) with Watershed, Integrating ESG Management \(formerly ESG\) with other applications, Operational Sustainability Management \(formerly Environmental, Social, and Governance\)]
---

# Create data mapping

Create data mappings to import Watershed data from columns other than the pre-configured columns of the Watershed spreadsheet. By default, data import from three columns is supported.

## Before you begin

Role required: sn\_esg.program\_manager

## About this task

By default, you can import data related to carbon emissions, renewable energy, and non-renewable energy. If you want to import other types of data such as water usage or waste disposal from the spreadsheet, then you can create data mappings for them. You can create as many mappings as you need.

## Procedure

1.  Navigate to **All** &gt; **Metrics** &gt; **Metrics Integrations**.

2.  Select **Watershed Integration**.

3.  In the Data mapping section, select **New**.

4.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the mapping.|
    |Source table|Source table of the mapping. This field is automatically set to **Watershed Data**.|
    |Data column|Column from which you want to import data.|
    |Start date column|Column in the source table that has the start date.|
    |Start date|Start date of the mapping. If there is no start date column, specify the start date.|
    |Frequency|Frequency of the data in the spreadsheet. For example, monthly data, annual data, or so on.|
    |End date column|Column in the source table that has end date.|
    |End date|End date of the mapping. If there is no end date column, specify the end date.|
    |Unit column|Unit column from the imported data set.|
    |Unit|Unit of the data.|
    |Default owner|Metric definition owner or the entity owner.|
    |Metric integration|Metric integration. This field is automatically set to **Watershed Integration**.|

5.  Select **Submit**.


## Result

The new mapping is ready to import data.

**Parent Topic:**[Integrating ESG Management \(formerly ESG\) with Watershed](../../esg-management-reporting/concept/integrate-esg-with-watershed.md)


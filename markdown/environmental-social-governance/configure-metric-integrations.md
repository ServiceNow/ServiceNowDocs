---
title: Modify the Operational Sustainability Integration with Watershed
description: Modify the Operational Sustainability Integration with Watershed configurations to specify how you want to import data from Watershed to generate metrics.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Integrating Operational Sustainability Management \(formerly ESG\) with Watershed, Integrating Operational Sustainability Management \(formerly ESG\) with other applications, Operational Sustainability Management \(formerly Environmental, Social, and Governance\)]
---

# Modify the Operational Sustainability Integration with Watershed

Modify the Operational Sustainability Integration with Watershed configurations to specify how you want to import data from Watershed to generate metrics.

## Before you begin

Role required: sn\_esg.program\_manager

## About this task

The ServiceNow AI Platform provides a pre-configured integration to import data from Watershed. However, you can update or modify the configuration properties based on your requirements. For example, when you modify the configuration, you can specify if you want the system to automatically create metric definitions or if you want to override metric data.

## Procedure

1.  Navigate to **All** &gt; **Operational Sustainability Management** &gt; **Watershed** &gt; **Metric Integration**.

2.  On the Metric Integrations page, select **Watershed Integration**.

3.  On the form, edit the fields as required.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the mapping.|
    |Source|Source of the mapping. This field is automatically set to **Watershed Data**.|
    |Domain area|Domain from which the integration is created. This field is automatically set to **Operational Sustainability Management** when the integration is created from Operational Sustainability Management.|
    |Source table|The source table is automatically set to **Watershed Data**.|
    |Automatically create metric definition|Option to automatically create the metric definitions during data import.|
    |Automatically create metric unit|Option to automatically create the metric unit during data import.|
    |Automatically create entity type|Option to automatically create the entity type during data import.|
    |Automatically create entity|Option to automatically create the entity during data import.|
    |Overwrite metric data|Option to overwrite metric data during data import.|

4.  Select **Update**.


**Parent Topic:**[Integrating Operational Sustainability Management \(formerly ESG\) with Watershed](../../esg-management-reporting/concept/integrate-esg-with-watershed.md)


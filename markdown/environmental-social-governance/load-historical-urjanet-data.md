---
title: Load historical Urjanet data
description: Load historical Urjanet account statement data as metric data by creating new metrics that can be managed as part of Operational Sustainability Management. Data is retrieved from the date that you specify while configuring the Urjanet connection.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Integrating Operational Sustainability Management \(formerly ESG\) with Urjanet, Integrating Operational Sustainability Management \(formerly ESG\) with other applications, Operational Sustainability Management \(formerly Environmental, Social, and Governance\)]
---

# Load historical Urjanet data

Load historical Urjanet account statement data as metric data by creating new metrics that can be managed as part of Operational Sustainability Management. Data is retrieved from the date that you specify while configuring the Urjanet connection.

## Before you begin

Role required: import\_scheduler

## Procedure

1.  Navigate to **All** &gt; **System Import Sets** &gt; **Administration** &gt; **Scheduled Imports**.

2.  Select and open the **Urjanet Metric Data Scheduled Data Import** record.

3.  Select **Execute Now**.

    By default, the data import is set to run every 90 days but you can modify the frequency in the **Run** field on the Scheduled Data Import form. For more information on configuring a scheduled data import, see [Schedule a data import](https://www.servicenow.com/docs/access?context=t_ScheduleADataImport&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US).


## Result

The metrics are created by using the configured entities and metric definitions.

**Parent Topic:**[Integrating Operational Sustainability Management \(formerly ESG\) with Urjanet](../concept/integrating-esg-management-with-urjanet.md)


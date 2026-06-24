---
title: Load historical Urjanet data
description: Load historical Urjanet account statement data as metric data by creating new metrics that can be managed as part of ESG Management. Data is retrieved from the date that you specify while configuring the Urjanet connection.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/environmental-social-governance/load-historical-urjanet-data.html
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Integrating ESG Management with Urjanet, Integrating ESG Management with other applications, Environmental, Social, and Governance Management]
---

# Load historical Urjanet data

Load historical Urjanet account statement data as metric data by creating new metrics that can be managed as part of ESG Management. Data is retrieved from the date that you specify while configuring the Urjanet connection.

## Before you begin

Role required: import\_scheduler

## Procedure

1.  Navigate to **All** &gt; **System Import Sets** &gt; **Administration** &gt; **Scheduled Imports**.

2.  Select and open the **Urjanet Metric Data Scheduled Data Import** record.

3.  Select **Execute Now**.

    By default, the data import is set to run every 90 days but you can modify the frequency in the **Run** field on the Scheduled Data Import form. For more information on configuring a scheduled data import, see [Schedule a data import](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/integrate-applications/system-import-sets/t_ScheduleADataImport.md).


## Result

The metrics are created by using the configured entities and metric definitions.

**Parent Topic:**[Integrating ESG Management with Urjanet](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/environmental-social-governance/integrating-esg-management-with-urjanet.md)


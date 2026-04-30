---
title: Import meter details from Urjanet
description: Using scheduled jobs, import meter details such as meter number, meter ID, and so on from Urjanet into the ESG Management application for reporting purposes. The details are imported in the form of entities.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Integrating ESG Management with Urjanet, Integrating ESG Management with other applications, Environmental, Social, and Governance Management]
---

# Import meter details from Urjanet

Using scheduled jobs, import meter details such as meter number, meter ID, and so on from Urjanet into the ESG Management application for reporting purposes. The details are imported in the form of entities.

## Before you begin

Role required: import\_scheduler

## Procedure

1.  Navigate to **All** &gt; **System Import Sets** &gt; **Administration** &gt; **Scheduled Imports**.

2.  Select and open the **Urjanet Entity Scheduled Data Import** record.

3.  Select **Execute Now**.

    By default, the data import is set to run every 90 days but you can modify the frequency in the **Run** field. For more information on configuring a scheduled data import, see [Schedule a data import](https://www.servicenow.com/docs/access?context=t_ScheduleADataImport&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US).


## Result

The entities are created with the following details.

-   Name: Urjanet meter’s site name and Urjanet meter’s meter number.
-   Location: Service address of the Urjanet meter.
-   Description: Provider of the Urjanet meter.

**Parent Topic:**[Integrating ESG Management with Urjanet](../concept/integrating-esg-management-with-urjanet.md)


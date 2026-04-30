---
title: Run scheduled jobs in SAP
description: Run adhoc scheduled jobs to look up entity primary data from the target SAP ERP source.
locale: en-US
release: yokohama
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Scheduled jobs to fetch data, Configure, Source-to-Pay integration with SAP, Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Run scheduled jobs in SAP

Run adhoc scheduled jobs to look up entity primary data from the target SAP ERP source.

## Before you begin

Role required: sn\_fcms\_intg.admin

## About this task

Executes on-demand scheduled jobs on true entities of an ERP source target and fetches primary data. Auto-populates the entity inbound tables.

## Procedure

1.  Navigate to **All** &gt; **Finance – ERP Integration** &gt; **ERP Source Configuration**.

2.  Select the ERP source for which you would like to run scheduled jobs.

3.  Select **Integration Services** &gt;**Run job**.

    The fetch services run automatically as scheduled.

    Entity inbound tables are populated with primary data.


**Parent Topic:**[Scheduled jobs to look up primary data in SAP](../concept/scheduled-jobs-to-primary-data-sap.md)


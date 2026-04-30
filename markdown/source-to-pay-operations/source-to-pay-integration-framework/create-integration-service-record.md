---
title: Create Integration Service record
description: Create Integration Service records for entities using the sn\_fcms\_intg\_service table.
locale: en-US
release: xanadu
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Scheduled jobs to fetch primary data, Source-to-Pay integration framework, Source-to-Pay integration with third-party applications, Source-to-Pay Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Create Integration Service record

Create Integration Service records for entities using the sn\_fcms\_intg\_service table.

## Before you begin

Role required: sn\_fcms\_intg.integration\_user

## Procedure

1.  Navigate to **Integration Services**.

2.  Select **New**.

3.  On the integration service record, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Entity|The type of entity for which you want to configure scheduled job.|
    |ERP Source configuration|The ERP source mapped to the entity.|
    |Subflow|The subflow used to fetch primary data.|
    |Properties|The filter condition used to fetch data from ERP sub flows. Example: Full-pull creates JSON in the integration service record which is passed to the ERP sub flows to fetch data.|
    |Active|The status of the interaction service. By default, the check box is inactive.|

4.  Select **Submit**.


## What to do next

In the ERP Source configuration, Run jobs for active entities.


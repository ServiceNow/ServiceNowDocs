---
title: Update the data source of the connector
description: Link the duplicated ETL to a valid data source for your specific connector.
locale: en-US
release: australia
product: Telecommunications Service Operations Management
classification: telecommunications-service-operations-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure Telecom Discovery Builder, Configure Telecom Visibility, Configure, Telecommunications Service Operations Management]
---

# Update the data source of the connector

Link the duplicated ETL to a valid data source for your specific connector.

## Before you begin

Role required: admin

## About this task

The following screenshot can help you to replace the default source with your connector's data source.![Specify basic details user interface displaying the selection of data source to replace the default data source](../images/replace-datasource.png)

## Procedure

1.  Navigate to **All** &gt; **IntegrationHub ETL**.

2.  In **Specify Basic Details**, replace the default data source with your connector’s data source.

3.  Select **Save**.

4.  Open **Import Schedules** and run your data source.

    The system creates a new transform map based on the selected settings and create CIs generated from your payload.


**Related topics**  


[Deploy a new service graph connector with existing ETL](deploy-a-new-service-graph-connector-with-duplicated-etl.md)


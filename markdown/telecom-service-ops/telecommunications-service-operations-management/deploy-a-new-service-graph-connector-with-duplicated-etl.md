---
title: Deploy a new service graph connector with existing ETL
description: Associate a new Service Graph Connector \(SGC\) with an existing ETL.
locale: en-US
release: australia
product: Telecommunications Service Operations Management
classification: telecommunications-service-operations-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure Telecom Discovery Builder, Configure Telecom Visibility, Configure, Telecommunications Service Operations Management]
---

# Deploy a new service graph connector with existing ETL

Associate a new Service Graph Connector \(SGC\) with an existing ETL.

## Before you begin

Role required: admin

Ensure the required Service Graph Connector plugin is activated.

## Procedure

1.  Navigate to **All** &gt; **IntegrationHub ETL**.

2.  Open the duplicated ETL configuration.

3.  Select the data source of the service graph connector and click **Save**.

4.  Select **Import Schedules** to execute the ETL to transform and load the data from the new SGC.

5.  Monitor execution status.


## Result

Verify that CI records and relationships are created in the CMDB using CMDB Maps or list views.


---
title: Add before and after scripts to an integration data source
description: Add custom before and after scripts for a data source of a CMDB integration application. Those scripts provide access to the input and output payloads of IRE. When a CMDB integration invokes Identification and Reconciliation Engine \(IRE\), those scripts run before and after IRE processes the integration payload.
locale: en-US
release: xanadu
product: Integration Hub ETL
classification: integration-hub-etl
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [IntegrationHub ETL, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Add before and after scripts to an integration data source

Add custom before and after scripts for a data source of a CMDB integration application. Those scripts provide access to the input and output payloads of IRE. When a CMDB integration invokes Identification and Reconciliation Engine \(IRE\), those scripts run before and after IRE processes the integration payload.

## Before you begin

Role required: cmdb\_inst\_admin

## Procedure

1.  Navigate to **All** &gt; **Configuration** &gt; **IntegrationHub ETL**.

    The landing page of the IntegrationHub ETL lists all integrations that exist in the system, including integrations that were downloaded from the ServiceNow Store.

2.  Click the **CMDB Application** link for the integration that you want to add scripts for.

3.  On the CMDB Integration Studio Application form, in the CMDB Integration Studio Application Data Sources related list, open the data source record for the CMDB integration.

4.  On the CMDB Integration Studio Application Data Source form, check **Execute Before Script** or **Execute After Script**.

5.  Review the **Before Script** and **After Script** comments and enter your custom scripts at the bottom of the script field.

    The comments in the script fields provide details for the before and after scripts. Use those guidelines, explanations such as what operations are supported, and examples when creating your custom script.

6.  Click **Update**.


**Related topics**  


[Identification and Reconciliation engine \(IRE\)](../concept/ire.md)


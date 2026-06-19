---
title: Enable the Oracle GLAS V2 data collection method
description: Enable the Oracle GLAS V2 data collection method to improve data collection performance in large-scale or high volume Oracle database environments.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/discovery-and-service-mapping-patterns/enable-oracle-glas-v2-method.html
release: australia
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: task
last_updated: "2026-04-29"
reading_time_minutes: 1
keywords: [Oracle GLAS, Oracle GLAS V2, Oracle GLAS data collection]
audience: administrator
breadcrumb: [Oracle GLAS data collection, Available on-premise discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Enable the Oracle GLAS V2 data collection method

Enable the Oracle GLAS V2 data collection method to improve data collection performance in large-scale or high volume Oracle database environments.

## Before you begin

-   Verify that you have at least version 1.12.0 of Data Collection for Oracle Global Licensing and Advisory Services.
-   Verify that the **sn\_itom\_oracleglas.disable\_glas\_data\_collection** MID Server property is set to **false**.

Role required: glas\_admin or admin

## Procedure

1.  In the navigation filter, enter `sys_properties.list`.

2.  In the **Name** column, search for `sn_itom_pattern.enable_large_env_glas_data_collection`.

3.  Select the **sn\_itom\_pattern.enable\_large\_env\_glas\_data\_collection** system property.

4.  In the **Value** field, enter `true`.

    To switch back to V1 data collection, set the value to `false`.

5.  Select **Update**.


## What to do next

Run discovery again to begin data collection in V2. To verify data population, navigate to **All** &gt; **Oracle GLAS Data Collection** &gt; **GLAS V2 - Databases** and check the **Content** field. To download the collected data, see [Download Oracle Global License Advisory Services \(GLAS\) data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/download-oracle-glas-data.md).

**Parent Topic:**[Oracle GLAS data collection using patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/oracle-glas-discovery.md)


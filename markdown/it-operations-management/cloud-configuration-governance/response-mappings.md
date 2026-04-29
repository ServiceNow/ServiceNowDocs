---
title: Response Mappings
description: Response Mapping is the mechanism CMP uses to write back all the events and operations into CMDB.
locale: en-US
release: australia
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Response Mappings

Response Mapping is the mechanism CMP uses to write back all the events and operations into CMDB.

## Response Mapping mechanism

CMP \(Cloud Management Platform\) is designed to actively engage with the cloud environment at various critical stages, including Discovery, Provisioning, Day-2 operations, and Lifecycle events. Throughout these processes, CMP is required to effectively record and store data within the Configuration Management Database \(CMDB\). This data could encompass diverse information ranging from system states to comprehensive sets of data.

To achieve this, CMP leverages its Response Processing mechanism to ensure the seamless and accurate transfer of data back into the CMDB.

## Features of Response Mapping

-   Maps external data format into ServiceNow format for IRE consumption.
-   Supports simple, complex, scripted, binding and relationship mappings.
-   Significant to add new/change mappings.
-   Performant, used in CMP for the past few releases.

See [https://www.servicenow.com/community/itom-articles/cmp-using-response-mapping-how-to-populate-cmdb-using-cmp/ta-p/2323213](https://www.servicenow.com/community/itom-articles/cmp-using-response-mapping-how-to-populate-cmdb-using-cmp/ta-p/2323213) to learn more.


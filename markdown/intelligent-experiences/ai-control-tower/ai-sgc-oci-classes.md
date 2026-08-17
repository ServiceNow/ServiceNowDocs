---
title: CMDB classes targeted in AI Service Graph Connector for OCI
description: When you complete setting up the connection, you can configure the integration to periodically pull data from OCI. The data is saved in tables that extend from the Configuration Item \[cmdb\_ci\] table.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/ai-control-tower/ai-sgc-oci-classes.html
release: zurich
product: AI Control Tower
classification: ai-control-tower
topic_type: reference
last_updated: "2026-07-06"
reading_time_minutes: 1
breadcrumb: [OCI, Service Graph Connectors for AI Control Tower, AI connections, Explore, AI Control Tower \(legacy\), Enable AI experiences]
---

# CMDB classes targeted in AI Service Graph Connector for OCI

When you complete setting up the connection, you can configure the integration to periodically pull data from OCI. The data is saved in tables that extend from the Configuration Item \[cmdb\_ci\] table.

## AI Function \[cmdb\_ci\_function\_ai\]

The following attributes in the AI Function \[cmdb\_ci\_function\_ai\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|Description|short\_description|
|Object ID|object\_id|
|Model ID|model\_id|
|Vendor|vendor|
|Asset|asset|
|Discovery Source|discovery\_source|

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|AI Function \[cmdb\_ci\_function\_ai\]|Depends on::Used by|AI Model Deployment \[cmdb\_ci\_ai\_model\_deployment\]|

## AI Model Deployment \[cmdb\_ci\_ai\_model\_deployment\]

The following attributes in the AI Model Deployment \[cmdb\_ci\_ai\_model\_deployment\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|Description|short\_description|
|Object ID|object\_id|
|Install Status|install\_status|
|Model ID|model\_id|
|Vendor|vendor|
|Asset|asset|
|Discovery Source|discovery\_source|


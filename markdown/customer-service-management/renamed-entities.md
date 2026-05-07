---
title: Service Model Foundation renamed Entities
description: The renamed entities display several Service Model Foundation entities that are renamed, including the previous and current names.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Reference, Customer Service Management]
---

# Service Model Foundation renamed Entities

The renamed entities display several Service Model Foundation entities that are renamed, including the previous and current names.

**Note:** The entity name changes are available in the Business Location 5.2.0 store app.

|Table name|Previous label|New label|
|----------|--------------|---------|
|sn\_customer\_service\_organization|Service Organization|Organization Core|
|sn\_csm\_business\_location|Business Location|Business Organization|
|sn\_csm\_business\_location\_internal|Internal Business Location \(IBL\)|Internal Organization|
|sn\_csm\_business\_location\_external|External Business Location \(EBL\)|External Organization|
|sn\_outsourced\_service\_provider|Outsourced Service Provider|No change|
|sn\_csm\_service\_organization\_external\_staff|Service Organization External Staff|External Organization Staff|
|service\_organizations\_offering\_service|Service Organizations offering Service|Organizations offering Service|
|service\_organization\_criteria|Service Organization Criteria|Organization Criteria|
|service\_organization\_customer\_criteria|Service Organization Customer Criteria|Organization Customer Criteria|
|sn\_csm\_svc\_org\_member\_responsibility|Service Organization Member Responsibility|Organization Member Responsibility|
|sn\_service\_org.service\_org\_assignment\_group|Service Organization Assignment Group|Organization Assignment Group|

## Field label renaming

The following foreign key field labels have been updated across impacted entities.

**Note:** The entity name changes are available in the Business Locations 5.2.0 store app.

|Table name|Field name|Previous label|New label|
|----------|----------|--------------|---------|
|Service Organization|service\_organization\_parent|Parent Service Organization|Parent Organization|
|Service Organization External Staff|service\_organization|Service Organization|Organization|
|Service Organization Member|service\_organization|Service Organization|Organization|
|Case|requesting\_service\_organization|Requesting Service Organization|Requestor Organization|
|Case|service\_organization|Provider Service Organization|Provider Organization|
|Interaction|requesting\_service\_organization|Requesting Service Organization|Requestor Organization|
|Sold Product|provider\_service\_organization|Provider Service Organization|Seller Organization|
|Sold Product|service\_organization|Service Organization|Buyer Organization|
|Install Base Item|service\_organization|Service Organization|Buyer Organization|
|Install Base Item|provider\_service\_organization|Provider Service Organization|Provider Organization|
|Install Base Related Party|service\_organization|Service Organization|Organization|
|Work Order|service\_organization|Service Organization|Requestor Organization|
|Work Order|provider\_service\_organization|Provider Service Organization|Provider Organization|
|Customer Project|service\_organization|Service Organization|Organization|
|Retail Organization|service\_organization|Service Organization|Business Organization|
|Customer Service Organization|service\_organization\_path|Service Organization Path|Organization Path|
|Customer Service Organization|service\_organization\_code|Service Organization Code|Organization Code|
|Customer Service Organization|service\_organization\_served|Service organizations served|Organizations served|
|Responsibility Definition|service\_organization|Service Organization|Business Organization|
|Responsibility Access Config|service\_organization|Service Organization|Business Organization|


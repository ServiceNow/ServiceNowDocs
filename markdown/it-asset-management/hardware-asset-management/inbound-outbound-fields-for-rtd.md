---
title: Remote task definition inbound and outbound fields
description: The inbound and outbound fields of the remote task definition required for the Zero Touch Refresh flow.
locale: en-US
release: yokohama
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Hardware Asset Management reference, Hardware Asset Management, IT Asset Management]
---

# Remote task definition inbound and outbound fields

The inbound and outbound fields of the remote task definition required for the Zero Touch Refresh flow.

## Inbound field values

For each field, the source table and target table are the Zero Touch Refresh Fulfillment Request table \[sn\_itam\_ztr\_fulfillment\_req\].

The **Target field** value is the same as the **Source field** value. The value in the source field is sent from the source table on the requester's ServiceNow instance to the target field in the table on the provider's instance to which the source field is synced.

The **Sync when** value is **Insert**, which updates the target field on the remote task's parent record only when the remote task is initially inserted.

|Field label|Field name|Max length|Source field|
|-----------|----------|----------|------------|
|Customer request number|customer\_request\_number|40|Customer request number|
|Model|model|255|Model|
|State|state|40|State|
|Name|name|151|Name|
|Email|email|100|Email|
|Mobile|mobile|40|Mobile|
|Street|street|255|Street \(street\)|
|City|city|40|City \(city\)|
|State or Province|state\_loc|40|State/Province \(state\_loc\)|
|Country|country|40|Country \(country\)|
|Zip or Postal code|zip|40|Zip/Postal code|
|Return name|return\_name|151|Name \(return\_name\)|
|Return street|return\_street|255|Street \(return\_street\)|
|Return city|return\_city|40|City \(return\_city\)|
|Return state or province|return\_state\_loc|40|State/Province \(return\_state\_loc\)|
|Return country|return\_country|40|Country \(return\_country\)|
|Return zip or postal code|return\_zip|40|Zip/Postal code \(return\_zip\)|

## Outbound field values

For each field, the source table and target table are Zero Touch Refresh Fulfillment Request table \[sn\_itam\_ztr\_fulfillment\_req\].

The **Target field** value is the same as the **Source field** value. The value in the Source field is sent from the source table on the provider's ServiceNow instance to the target field on the table on the requester's instance to which the source field is synced.

The **Sync when** value is **Insert and Update**, which updates the target field on the remote task's parent record every time the remote task is updated.

|Field label|Field name|Max length|Source field|
|-----------|----------|----------|------------|
|Serial number|serial\_number|100|Serial number|
|Asset tag|asset\_tag|40|Asset tag|
|State|state|40|State|
|Tracking number|tracking\_number|40|Tracking number \(tracking\_number\)|
|Carrier|carrier|80|Carrier \(carrier\)|
|Return tracking number|return\_tracking\_number|40|Tracking number \(return\_tracking\_number\)|
|Return carrier|return\_carrier|80|\(return\_carrier\)|

**Parent Topic:**[Hardware Asset Management reference](../concept/reference-hardware-asset-management.md)


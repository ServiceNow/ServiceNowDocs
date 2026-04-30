---
title: OCRotaMember - Global
description: The OCRotaMember script include provide methods to perform maintenance operations on the On-call Member \[cmn\_rota\_member\] table.Deactivates the user's rota member records according to the deactivate date.Checks whether the cmn\_rota\_member record has changed. Checks the Member, From, To, and Order fields have changed.On update of a cmn\_rota\_member record, checks whether the order of the record has changed.Recalculates the schedule for the cmn\_rota\_member record.Ensures that the From date occurs before or on the same date as the To date.
locale: en-US
release: zurich
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# OCRotaMember- Global

The OCRotaMember script include provide methods to perform maintenance operations on the On-call Member \[cmn\_rota\_member\] table.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## OCRotaMember - deactivateUser \(String userId, GlideDateTime deactivateDate\)

Deactivates the user's rota member records according to the deactivate date.

|Name|Type|Description|
|----|----|-----------|
|userId|String|The sys id of the user.|
|deactivateDate|GlideDateTime|The date from which the user's rotation is deactivated.|

|Type|Description|
|----|-----------|
|void| |

## OCRotaMember - hasChanged \(GlideRecord current, GlideRecord previous\)

Checks whether the cmn\_rota\_member record has changed. Checks the Member, From, To, and Order fields have changed.

|Name|Type|Description|
|----|----|-----------|
|current|GlideRecord|The latest changes made to the cmn\_rota\_member record.|
|previous|GlideRecord|The original state of the cmn\_rota\_member record.|

|Type|Description|
|----|-----------|
|void| |

## OCRotaMember - hasOrderChanged \(GlideRecord current, GlideRecord previous\)

On update of a cmn\_rota\_member record, checks whether the order of the record has changed.

|Name|Type|Description|
|----|----|-----------|
|current|GlideRecord|The latest changes made to the cmn\_rota\_member record.|
|previous|GlideRecord|The original state of the cmn\_rota\_member record.|

|Type|Description|
|----|-----------|
|Boolean|Returns true if the order has changed.|

## OCRotaMember - recalculate \(GlideRecord current, GlideRecord previous\)

Recalculates the schedule for the cmn\_rota\_member record.

|Name|Type|Description|
|----|----|-----------|
|current|GlideRecord|The latest changes made to the cmn\_rota\_member record.|
|previous|GlideRecord|The original state of the cmn\_rota\_member record.|

|Type|Description|
|----|-----------|
|void| |

## OCRotaMember - validateDates \(String from, String to\)

Ensures that the From date occurs before or on the same date as the To date.

|Name|Type|Description|
|----|----|-----------|
|from|String|Formatted date/|
|to|String|Formatted date/|

|Type|Description|
|----|-----------|
|Boolean|Returns true if the From date is before or on same date as To date.|


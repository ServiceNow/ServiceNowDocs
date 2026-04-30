---
title: IDResult - Global
description: The IDResult script include is a container class for the result of a CI Identifier.Creates an instance of the IDResult class.
locale: en-US
release: yokohama
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# IDResult- Global

The IDResult script include is a container class for the result of a CI Identifier.

Use with any server-side discovery script.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## IDResult - IDResult\(Boolean explore, String sysID\)

Creates an instance of the IDResult class.

|Name|Type|Description|
|----|----|-----------|
|explore|Boolean|Set to true if the CI should be explored; otherwise, false.|
|sysID|String|An existing CI's sys\_id, or null if no existing CI could be found.|


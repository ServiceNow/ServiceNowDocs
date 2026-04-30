---
title: CIIdentifierResult - Global
description: The CIIdentifierResult script include provides methods that return the result returned by a configuration item identifier.Creates an instance of the CIIdentifierResult class.
locale: en-US
release: yokohama
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# CIIdentifierResult- Global

The CIIdentifierResult script include provides methods that return the result returned by a configuration item identifier.

Use with any server-side discovery script.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## CIIdentifierResult - CIIdentifierResult\(Array matched, Boolean matchable, Boolean terminatedChain\)

Creates an instance of the CIIdentifierResult class.

|Name|Type|Description|
|----|----|-----------|
|matched|Array|An array of sys\_ids of matching CIs; may have any number of entries including zero.|
|matchable|Boolean|True if identifier had sufficient data to match|
|terminatedChain|Boolean|True if the identifier chain should stop processing filters. False to continue.|


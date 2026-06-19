---
title: GlideGuid - Client
description: The GlideGuid API provides methods to create a globally unique identifier.Creates a globally unique identifier 32 characters long, or as specified with the optional length argument.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/api-reference/c\_GlideGuidV3API.html
release: zurich
product: API Reference
classification: api-reference
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Client API reference, API reference, API implementation and reference]
---

# GlideGuid- Client

The GlideGuid API provides methods to create a globally unique identifier.

You access the GlideGuidV3 methods using the `g_guid` global object.

**Parent Topic:**[Client API reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/api-client.md)

## GlideGuid - generate\(Number stringLength\)

Creates a globally unique identifier 32 characters long, or as specified with the optional length argument.

|Name|Type|Description|
|----|----|-----------|
|stringLength|Number|The desired string length, must be between 1 and 32 inclusive. This parameter is optional. If not specified, the returned string will be 32 characters long.|

|Type|Description|
|----|-----------|
|String|The globally unique identifier.|


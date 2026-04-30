---
title: Work with coders and Codable models
description: The iOS implementation of the Mobile SDK provides the additional functionality of coders and Codable models.
locale: en-US
release: yokohama
product: Developer Guides
classification: developer-guides
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Mobile SDK Developer Guide - iOS, Developer guides, API implementation and reference]
---

# Work with coders and Codable models

The iOS implementation of the Mobile SDK provides the additional functionality of coders and Codable models.

## Coder enumeration

The `Coder` enumeration wraps a `JSONEncoder` with an accompanying `JSONDecoder` so that both provide the same coding strategy. Since many of the NowData framework APIs that handle Codable models rely on coding and decoding from JSON, the `Coder` simplifies and standardizes the way to specify encoders and decoders. Typically, using the default `Coder` \(`.default`\), which encodes and decodes dates using the `nonISO8601UTC` date formatting, is sufficient. The `DateFormatter.nonISO8601UTC` is a static date formatter provided by the NowData framework. It is responsible for encoding and decoding dates that were stored by the ServiceNow platform in the UTC \(GMT+0\) time zone, and are used by the Table API in `yyyy-MM-dd HH:MM:SS` format, by taking a device's locale and time zone into consideration.

If custom JSON coding is required, such as when handling specific date formats, you can create a custom `Coder` by supplying the custom `JSONEncoder` and `JSONDecoder` as the custom Coder's associated types. Both the encoder and decoder must use the same coding strategy.

For example:

```
let myEncoder = JSONEncoder()
myEncoder.dateEncodingStrategy = .formatted(.nonISO8601UTC)
let myDecoder = JSONDecoder()
myDecoder.dateDecodingStrategy = .formatted(.nonISO8601UTC)

let myCoder: Coder = .custom(myEncoder, myDecoder)
```

## Codable extension for nested structures

The NowData framework provides functionality to decode nested structures by dot-separated path. This functionality makes it easier to consume nested data by removing the necessity of using wrapper structure and nested JSON decoding.


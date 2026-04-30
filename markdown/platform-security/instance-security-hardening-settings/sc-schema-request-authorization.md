---
title: Require authorization for SCHEMA requests \[Updated in Security Center 1.3\]
description: Use the glide.basicauth.required.schema property to require basic authorization for all Inbound Table Schema Processor requests.
locale: en-US
release: yokohama
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [API and web service, Hardening settings, Platform Security]
---

# Require authorization for SCHEMA requests \[Updated in Security Center 1.3\]

Use the **glide.basicauth.required.schema** property to require basic authorization for all Inbound Table Schema Processor requests.

The Inbound Table Schebma Processor handles incoming schema requests for the platform.

Set **glide.basicauth.required.schema** to the recommended value of **true** to require basic authorization for all Inbound Table Schema Processor requests. Set the value to **false** to not require basic authorization for all Inbound Table Schema Processor requests.

**Warning:** This is a safe harbor property, meaning the value can't be altered once it's changed. It is non-revertible.

## More information

|Attribute|Description|
|---------|-----------|
|Property name|**glide.basicauth.required.schema**|
|Configuration type|System Properties \(/sys\_properties\_list.do\)|
|Category|[API and web service](sc-api-web-service.md)|
|Purpose|To require basic authorization for all Inbound Table Schema Processor requests.|
|Recommended value|True \(default value\).|
|Configuration type|Boolean|
|Security risk|\(Moderate\) Omitting authentication from this processor will lead to unauthenticated access to instance data.|

**Parent Topic:**[API and web service](sc-api-web-service.md)


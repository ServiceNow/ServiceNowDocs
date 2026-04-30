---
title: Require authorization for API requests \[Updated in Security Center 1.3\]
description: Use the glide.basicauth.required.api property to enhance security for basic authorization for incoming REST requests.
locale: en-US
release: yokohama
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [API and web service, Hardening settings, Platform Security]
---

# Require authorization for API requests \[Updated in Security Center 1.3\]

Use the **glide.basicauth.required.api** property to enhance security for basic authorization for incoming REST requests.

Set the **glide.basicauth.required.api** property to **true** to require authorization for all REST requests. Set the property to **false** to bypass authorization for all REST requests.

**Warning:** This is a safe harbor property, meaning the value can't be altered once it's changed. It is non-revertible.

## More information

|Attribute|Description|
|---------|-----------|
|Property name|**glide.basicauth.required.api**|
|Configuration type|System Properties \(/sys\_properties\_list.do\)|
|Category|[API and web service](sc-api-web-service.md)|
|Purpose|Basic authorization for incoming REST requests.|
|Recommended value|True \(default\)|
|Configuration type|String|
|Security risk|\(High\) If "glide.basicauth.required.api" is not set to the recommended value of "true", then this will disable Basic Authentication on API request and will lead to unauthenticated access to instance data.|
|Security risk rating|8.6|

**Parent Topic:**[API and web service](sc-api-web-service.md)


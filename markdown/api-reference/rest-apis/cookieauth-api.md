---
title: Cookie Auth API
description: The Cookie Auth Scripted REST API provides an endpoint that creates a short-lived ticket that the WebRTC phone widget needs to start a voice call. Because this endpoint doesn’t require a login, it works for authenticated and unauthenticated users.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/api-reference/rest-apis/cookieauth-api.html
release: australia
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2026-10-14"
reading_time_minutes: 1
keywords: [WebRTC, dialpad, DTMF, phone widget, theme tokens]
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# Cookie Auth API

The Cookie Auth Scripted REST API provides an endpoint that creates a short-lived ticket that the WebRTC phone widget needs to start a voice call. Because this endpoint doesn’t require a login, it works for authenticated and unauthenticated users.

WebRTC voice calling is a core capability for Customer Service Management \(CSM\) portals and Engagement Messenger. The Cookie Auth API allows authenticated and unauthenticated users \(like customers on public support portals, third parties embedding Engagement Messenger\) start a voice call without logging in. The ticket expires after 60 seconds and works once, so a caller never gets a long-lived credential. The API imposes rate limits so the open endpoint can’t be hit without restriction \(see the **API rate limits** section for more information\).

Typically, customers won’t call this API directly because the phone widget calls it automatically when someone starts a call.

## Access and authentication

This API is provided in the sn\_webrtc scope and requires the com.sn\_webrtc \(WebRTC Voice\) plugin. No role is required to access this API.

## API rate limits

The application ships with two rate limit rules for the Cookie Auth POST endpoint. You can change the limits to suit your environment.

|Rule name|Applies to|Limit|
|---------|----------|-----|
|WebRTC cookie auth limit for all users|All users|3,600 requests per hour|
|WebRTC cookie auth limit for un-authenticated users|The Guest user|3,600 requests per hour|

**Important:** All unauthenticated callers share the single Guest user identity, so the limit for the Guest rule is a shared limit for all unauthenticated callers, not a limit for each caller.

Conversely, authenticated users each get 3,600 requests per hour as it is not shared under one identity. For example, authenticated User 1 gets 3,600 requests per hour, User 2 gets 3,600 per hour, and so on.

-   **[Cookie Auth - POST /api/sn\_webrtc/webrtc\_cookie\_auth/cookie\_auth](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/rest-apis/cookieauth-POST-cookie_auth.md)**  
Returns a short-lived ticket that the WebRTC phone widget uses to connect to the voice service and start a call. The endpoint doesn’t require login, so guest users can place calls.

**Parent Topic:**[REST API reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/rest-apis/api-rest.md)


---
title: Third-party OAuth Provider form
description: The Third-party OAuth Provider form includes OAuth provider details such as the client ID and client secret for personal authentication.
locale: en-US
release: zurich
product: Workplace Calendar Synchronization
classification: workplace-calendar-synchronization
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Reference, Workplace Calendar Synchronization, Workplace Service Delivery, Employee Service Management]
---

# Third-party OAuth Provider form

The Third-party OAuth Provider form includes OAuth provider details such as the client ID and client secret for personal authentication.

|Field|Description|
|-----|-----------|
|Name|Unique name to identify the OAuth provider. For example, Microsoft Exchange Online\_personalAuth.|
|Client ID|Client ID created during the app creation in Microsoft Azure.|
|Client Secret|The password that you generated when creating the app in Microsoft Azure.|
|Default Grant Type|Grant type used to establish the token. Select **Authorization Code**.|
|Authorization URL|OAuth authorization code endpoint. Enter `https://login.microsoftonline.com/<tenant_id>/oauth2/v2.0/authorize`.|
|Token URL|OAuth server token endpoint. Enter `https://login.microsoftonline.com/<tenant_id>/oauth2/v2.0/token >`.|
|Redirect URL|OAuth callback endpoint. The URL is automatically filled as `https://<instance-name>.service-now.com/oauth_redirect.do`.|


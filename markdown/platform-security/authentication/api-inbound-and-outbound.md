---
title: OAuth Inbound and Outbound authentication
description: OAuth based authentication validates the identity of the client that attempts to establish a trust on the system by using an authentication protocol.
locale: en-US
release: yokohama
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
keywords: [servicenow OAuth, Servicenow OAuth, ServiceNow OAuth, OAuth authentication, inbound authentication, outbound authentication, OAuth 2.0, OAuth provider, OAuth client, token endpoint, authorization server, resource server, OAuth scope, OAuth grant types]
breadcrumb: [Authentication, Access Management]
---

# OAuth Inbound and Outbound authentication

OAuth based authentication validates the identity of the client that attempts to establish a trust on the system by using an authentication protocol.

OAuth 2.0 - Open Authorization is the industry-standard protocol for authorization, that ocuses on client developer simplicity while providing specific authorization flows for web applications, desktop applications, and mobile devices.

It is a standard that is designed to allow a website or application to access resources hosted by other web apps on behalf of a user.

Instead of using the resource user's credentials to access protected resources, the client obtains an access token. Access tokens are issued to third-party clients with the user's approval, the client then uses the access token to access the protected resources.

## Inbound

Create an endpoint for external clients that want to access your instance. This creates an OAuth client application record and generates a client ID and client secret that the client needs to access the restricted resources on the instance. For more information see, [OAuth Inbound](oauth-inbound.md).

## Outbound

Use a third-party OAuth provider that provides the authorization for access to your instance. Specify an OAuth profile and OAuth scope when you are connecting to another OAuth provider. For more information see, [OAuth Outbound](oauth-outbound.md).


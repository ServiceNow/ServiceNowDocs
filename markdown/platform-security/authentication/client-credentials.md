---
title: Client Credentials
description: Use the OAuth client credentials grant type for Inbound Integrations from a third party OAuth client to the ServiceNow platform.
locale: en-US
release: australia
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Old Inbound integrations experience, OAuth Inbound, OAuth authentication, Authentication, Access Management]
---

# Client Credentials

Use the OAuth client credentials grant type for Inbound Integrations from a third party OAuth client to the ServiceNow® platform.

The administrators can use the client credential \(CC\) grant type to enable integration from a third party OAuth client to the ServiceNow platform.

Inbound client credentials grant type is a capability that can be controlled through a system property. By default the system property is false.

To use the client credentials grant type, you must perform the following steps:

-   Create the `glide.oauth.inbound.client.credential.grant_type.enabled` system property.
-   Add the **OAuth Application User** field to the OAuth Entity form.


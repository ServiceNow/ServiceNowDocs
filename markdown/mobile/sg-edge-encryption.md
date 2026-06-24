---
title: Edge Encryption for ServiceNow mobile
description: Users can view and edit data protected with Edge Encryption within their mobile device. The data appears in readable form on the mobile device but is encrypted in the database.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/mobile/sg-edge-encryption.html
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Device security for ServiceNow Mobile apps, Mobile security, Configuring the Mobile Platform, Mobile Platform]
---

# Edge Encryption for ServiceNow mobile

Users can view and edit data protected with Edge Encryption within their mobile device. The data appears in readable form on the mobile device but is encrypted in the database.

ServiceNow® Edge Encryption encrypts sensitive data on your company premises before sending it over the Internet to your instance \(encrypted in flight\). This encrypted data is then stored and protected within your database \(encrypted at rest\).

The diagram shows an example of how Edge Encryption operates within the mobile platform. A field is configured and protected with Edge Encryption. When the user enters a value in an encrypted field on the mobile device, it remains in a readable format. However, in the database, the value is displayed as an encrypted value.

\[Omitted image "mobile-edge-encrypt.png"\] Alt text: How a value in a field protected by Edge Encryption displays in a mobile device and in a database.

For more information, see [Edge Encryption](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-security/edge-encryption/edge-encryption.md).

**Parent Topic:**[Device security for ServiceNow Mobile apps](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/mobile/sg-mobile-security.md)


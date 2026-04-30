---
title: Edge Encryption for ServiceNow mobile
description: Users can view and edit data protected with Edge Encryption within their mobile device. The data appears in readable form on the mobile device but is encrypted in the database.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Device security, Mobile security, Configuring the Mobile Platform, Mobile Platform]
---

# Edge Encryption for ServiceNow mobile

Users can view and edit data protected with Edge Encryption within their mobile device. The data appears in readable form on the mobile device but is encrypted in the database.

ServiceNow® Edge Encryption encrypts sensitive data on your company premises before sending it over the Internet to your instance \(encrypted in flight\). This encrypted data is then stored and protected within your database \(encrypted at rest\).

The diagram shows an example of how Edge Encryption operates within the mobile platform. A field is configured and protected with Edge Encryption. When the user enters a value in an encrypted field on the mobile device, it remains in a readable format. However, in the database, the value is displayed as an encrypted value.

![How a value in a field protected by Edge Encryption displays in a mobile device and in a database.](../image/mobile-edge-encrypt.png)

For more information, see [Edge Encryption](https://www.servicenow.com/docs/access?context=edge-encryption&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

**Parent Topic:**[Device security for ServiceNow Mobile apps](sg-mobile-security.md)


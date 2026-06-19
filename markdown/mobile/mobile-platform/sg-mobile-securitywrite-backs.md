---
title: Write-backs
description: The following describes how data is written back from ServiceNow mobile apps.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/mobile/mobile-platform/sg-mobile-securitywrite-backs.html
release: zurich
product: Mobile Platform
classification: mobile-platform
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Mobile data flow, Device security, Mobile security, Configuring the Mobile Platform, Mobile Platform]
---

# Write-backs

The following describes how data is written back from ServiceNow mobile apps.

## Updating fields

When a user updates a field in a mobile app, the following steps occur.

1.  The mobile app sends the Token and the action metadata, for example the ID, or the field to be updated, to the instance.
2.  The instance directs the action based on the relevant API.
3.  The instance completes the action and sends a response to the mobile app.
4.  Based on the response, the mobile app reflects the field changes and action availability in the UI.

## Attaching documents

When attaching documents, the following steps occur.

1.  The mobile app asks the user to attach a document, for example, an image.
2.  The mobile app sends the document and Token to the instance.
3.  The instance places the document based on the relevant API.
4.  The instance sends a response back to the mobile app.

**Parent Topic:**[Mobile data flow for ServiceNow mobile apps](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/mobile/mobile-platform/sg-security-mobile-data-flow.md)


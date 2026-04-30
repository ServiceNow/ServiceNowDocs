---
title: Retrieval
description: The following describes how data is retrieved from ServiceNow mobile apps.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Mobile data flow for ServiceNow mobile apps, Device security for ServiceNow Mobile apps, Mobile security, Configuring the Mobile Platform, Mobile Platform]
---

# Retrieval

The following describes how data is retrieved from ServiceNow mobile apps.

## Read data

When a user requests to view information on the mobile app, the following steps occur.

1.  The mobile app sends a request to access data from the instance. The request includes the token and any relevant data field needed for the request.
2.  The instance receives the request and checks if the Token is valid.
3.  If the token is valid, the request is directed to the relevant API to fetch the information.
4.  The information is returned to the mobile app.

## Downloading documents

When a user requests to download documents from the app, the following steps occur.

1.  The mobile app sends a request to access the document. The request includes the Token.
2.  The instance receives the request and checks if the Token is valid.
3.  If valid, the document becomes available to view or take further actions on the device.

**Parent Topic:**[Mobile data flow for ServiceNow mobile apps](sg-security-mobile-data-flow.md)


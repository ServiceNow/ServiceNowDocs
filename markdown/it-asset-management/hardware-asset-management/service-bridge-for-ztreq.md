---
title: Configure Service Exchange for the Zero Touch request flow
description: The Zero Touch request flow uses the Service Exchange application to connect providers with your ServiceNow instance to manage hardware asset requests submitted through the Service Catalog.
locale: en-US
release: australia
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Zero Touch request flow, Using Hardware Asset Management, Hardware Asset Management, IT Asset Management]
---

# Configure Service Exchange for the Zero Touch request flow

The Zero Touch request flow uses the Service Exchange application to connect providers with your ServiceNow instance to manage hardware asset requests submitted through the Service Catalog.

## Service Exchange setup for providers

Providers must perform the following tasks to communicate about the request details with your organization:

1.  [Install Service Exchange for Providers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/service-exchange/install-service-bridge-v2-provider.md).
2.  [Register a Service Exchange consumer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/service-exchange/service-bridge-v2-onboarding.md).
3.  [Create and publish remote record producers in a Remote Catalog](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/service-exchange/service-bridge-v2-create-remote-rec-prod.md).

## Service Exchange setup for your service catalog requests

Perform the following steps to receive updates on the catalog requests from your provider:

1.  [Install Service Exchange for Consumers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/service-exchange/install-service-bridge-v2-customer.md).
2.  [Activate the remote record producers published by the provider](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/service-exchange/service-bridge-v2-configure-consumer-settings.md).


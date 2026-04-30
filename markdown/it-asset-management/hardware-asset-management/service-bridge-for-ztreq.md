---
title: Configure Service Exchange for the Zero Touch request flow
description: The Zero Touch request flow uses the Service Exchange application to connect providers with your ServiceNow instance to manage hardware asset requests submitted through the Service Catalog.
locale: en-US
release: yokohama
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Manage hardware asset requests using the Zero Touch request flow, Using Hardware Asset Management, Hardware Asset Management, IT Asset Management]
---

# Configure Service Exchange for the Zero Touch request flow

The Zero Touch request flow uses the Service Exchange application to connect providers with your ServiceNow instance to manage hardware asset requests submitted through the Service Catalog.

## Service Exchange setup for providers

Providers must perform the following tasks to communicate about the request details with your organization:

1.  [Install Service Exchange for Providers](https://www.servicenow.com/docs/access?context=install-service-bridge-v2-provider&version=yokohama&pubname=yokohama-service-bridge&ft:locale=en-US).
2.  [Register a Service Exchange consumer](https://www.servicenow.com/docs/access?context=service-bridge-v2-onboarding&version=yokohama&pubname=yokohama-service-bridge&ft:locale=en-US).
3.  [Create and publish remote record producers in a Remote Catalog](https://www.servicenow.com/docs/access?context=service-bridge-v2-create-remote-rec-prod&version=yokohama&pubname=yokohama-service-bridge&ft:locale=en-US).

## Service Exchange setup for your service catalog requests

Perform the following steps to receive updates on the catalog requests from your provider:

1.  [Install Service Exchange for Consumers](https://www.servicenow.com/docs/access?context=install-service-bridge-v2-customer&version=yokohama&pubname=yokohama-service-bridge&ft:locale=en-US).
2.  [Activate the remote record producers published by the provider](https://www.servicenow.com/docs/access?context=service-bridge-v2-configure-consumer-settings&version=yokohama&pubname=yokohama-service-bridge&ft:locale=en-US).


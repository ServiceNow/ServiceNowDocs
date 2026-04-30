---
title: Service Exchange configuration for Zero Touch Refresh
description: The Zero Touch Refresh flow uses the Service Exchange application to connect providers with your ServiceNow instance to manage asset refresh requests. Your employees and the provider can work on requests in their own environments.
locale: en-US
release: xanadu
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Manage refresh of assets using Zero Touch Refresh, Using Hardware Asset Management, Hardware Asset Management, IT Asset Management]
---

# Service Exchange configuration for Zero Touch Refresh

The Zero Touch Refresh flow uses the Service Exchange application to connect providers with your ServiceNow instance to manage asset refresh requests. Your employees and the provider can work on requests in their own environments.

## Service Exchange setup for providers

Providers should perform the following setup tasks to communicate the details of Zero Touch Refresh requests:

1.  [Install Service Exchange for Providers](https://www.servicenow.com/docs/access?context=install-service-bridge-v2-provider&version=xanadu&pubname=xanadu-service-bridge&ft:locale=en-US).
2.  [Onboard a new Service Exchange customer](https://www.servicenow.com/docs/access?context=service-bridge-v2-onboarding&version=xanadu&pubname=xanadu-service-bridge&ft:locale=en-US).
3.  [Trigger the assignment of a remote task](../task/create-rtd-for-providers.md).

## Service Exchange setup for employee requests

Perform the following setup to communicate the details of Zero Touch Refresh requests with the provider:

1.  [Install Service Exchange for Consumers](https://www.servicenow.com/docs/access?context=install-service-bridge-v2-customer&version=xanadu&pubname=xanadu-service-bridge&ft:locale=en-US).
2.  [Activate the remote task definitions published by the provider](../task/activate-rtd-for-customers.md).


---
title: Remote record producers in Service Exchange
description: Remote record producers in Service Exchange for Providers are service requests published in consumer instances. They enable your consumer to request provider services through their service catalog.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/service-exchange/service-bridge-v2-remote-record.html
release: xanadu
product: Service Exchange
classification: service-exchange
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Create remote catalogs in Service Exchange for providers, Installing and configuring Service Exchange for Providers, Service Exchange for Providers, Service Exchange]
---

# Remote record producers in Service Exchange

Remote record producers in Service Exchange for Providers are service requests published in consumer instances. They enable your consumer to request provider services through their service catalog.

## Overview of record producers

Remote record producers contain the variables that determine the information that a consumer can or must provide to submit a request. When a remote record producer is submitted from the consumer's service catalog, it generates a Provider Task record on the provider's instance and triggers a Create Case, Create Incident, or Create Change Request fulfillment task.

As the task moves through the fulfillment flow in the provider's instance, updates are visible in both the provider and the consumer's ServiceNow instances.

The remote record producer table is an extension of the sc\_cat\_item\_producer table and uses the sn\_sb\_pro\_remote\_request table.

The following example shows a sample form that you use when you create a remote record producer.

\[Omitted image "sn\_nowebonding\_remote\_request-v2.png"\] Alt text: Detailed view of a remote record producer form


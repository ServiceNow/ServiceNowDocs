---
title: Remote record producers in Service Exchange
description: Remote record producers in Service Exchange for Providers are service requests published in consumer instances. They enable your consumer to request provider services through their service catalog.
locale: en-US
release: australia
product: Service Bridge
classification: service-bridge
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Remote catalogs, Explore, Service Exchange]
---

# Remote record producers in Service Exchange

Remote record producers in Service Exchange for Providers are service requests published in consumer instances. They enable your consumer to request provider services through their service catalog.

## Overview of record producers

Remote record producers contain the variables that determine the information that a consumer can or must provide to submit a request. When a remote record producer is submitted from the consumer's service catalog, it generates a Provider Task record on the provider's instance and triggers a Create Case, Create Incident, or Create Change Request fulfillment task.

As the task moves through the fulfillment flow in the provider's instance, updates are visible in both the provider and the consumer's ServiceNow instances.

The remote record producer table is an extension of the sc\_cat\_item\_producer table and uses the sn\_sb\_pro\_remote\_request table.


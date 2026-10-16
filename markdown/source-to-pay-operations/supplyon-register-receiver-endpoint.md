---
title: Register the async receiver endpoint in SupplyOn
description: Provide SupplyOn with the receiver endpoint URL and API key to enable asynchronous status callbacks.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/source-to-pay-operations/supplyon-register-receiver-endpoint.html
release: zurich
topic_type: task
last_updated: "2026-10-09"
reading_time_minutes: 1
breadcrumb: [Configuring the Supplyon integration, Purchase Order Management integration with SupplyOn, Integrate with Purchase Order Management, Purchase Order Management, Source-to-Pay Operations, Finance and Supply Chain]
---

# Register the async receiver endpoint in SupplyOn

Provide SupplyOn with the receiver endpoint URL and API key to enable asynchronous status callbacks.

## Before you begin

Endpoint: `POST /api/sn_supplyon_po/supplyon_outbound_po_async_callback`

Role required: sn\_supplyon\_po.admin.

## About this task

SupplyOn requires the endpoint location to post status callbacks. Complete this registration in the SupplyOn portal.

## Procedure

1.  Provide SupplyOn with the receiver endpoint URL for your instance.

2.  Provide the API key issued to the integration service account.

3.  Verify that SupplyOn has registered the endpoint for status notifications.



---
title: Managing inbound asset orders for DaaS assets
description: Following a request for a hardware asset, an inbound asset order is associated with this request by creating an order in the DaaS provider interface.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-asset-management/hardware-asset-management/manage-inbound-orders.html
release: zurich
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Device as a Service, Hardware Asset Management, IT Asset Management]
---

# Managing inbound asset orders for DaaS assets

Following a request for a hardware asset, an inbound asset order is associated with this request by creating an order in the DaaS provider interface.

Completing the following tasks in the Inbound asset order workflow results in the successful completion of an asset order:

1.  [Create an inbound asset order](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/hardware-asset-management/create-inbound-order.md)
2.  [Create an inbound asset order line](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/hardware-asset-management/create-inbound-order-line.md)
3.  [Select an asset](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/hardware-asset-management/select-daas-asset.md)
4.  [Pick the selected asset](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/hardware-asset-management/pick-daas-asset.md)
5.  [Prepare the picked asset](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/hardware-asset-management/prepare-daas-asset.md)
6.  [Ship the prepared asset](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/hardware-asset-management/ship-daas-asset.md)
7.  [Receive the shipped asset](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/hardware-asset-management/receive-daas-asset.md)

In a DaaS inbound asset order, the DaaS provider and the consumer are two separate organizations. The provider accepts an order from a consumer account, then prepares and ships the asset. When the consumer acknowledges receipt, the asset record in the provider's instance is set to **In use**. The **Assigned to** field on the provider's asset record remains empty because assignment is handled by the consumer's organization, not the provider.


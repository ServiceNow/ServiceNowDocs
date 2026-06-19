---
title: Manage hardware asset requests using the Zero Touch request flow
description: Fulfill hardware asset requests of your employees through an external provider by using the Zero Touch request flow.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/hardware-asset-management/managing-standard-hw-req-ztr.html
release: australia
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Use, Hardware Asset Management, IT Asset Management]
---

# Manage hardware asset requests using the Zero Touch request flow

Fulfill hardware asset requests of your employees through an external provider by using the Zero Touch request flow.

## Setup required for providers

The provider must complete the following tasks to fulfill the requests received through the Zero Touch request flow:

1.  [Complete the Service Exchange setup for providers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/hardware-asset-management/service-bridge-for-ztreq.md).
2.  [Configure Scratchpad to send updates to your consumer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/hardware-asset-management/using-scratchpad-for-provider-updates.md).

**Note:** After completing the prerequisites of the Zero Touch request flow, the provider can fulfill provider tasks. For details, see [Fulfill a provider task](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/hardware-asset-management/fulfill-provider-task-ztr.md).

## Setup required for your Service Catalog requests

Make sure that you have the completed the following tasks so that your catalog requests can be fulfilled through an external provider:

1.  [Complete the Service Exchange setup for your service catalog requests](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/hardware-asset-management/service-bridge-for-ztreq.md).
2.  [Manage Service Catalog items for the Zero Touch request flow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/hardware-asset-management/manage-service-catalog-items-ztr.md).
3.  [Create a provider integration profile](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/hardware-asset-management/create-int-profile-ztr-ham.md).

    **Note:** You must perform this task only if the Scratchpad update received from your provider isn't in the format required for the Zero Touch request flow. You must also [create a Script Include to transform Scratchpad updates from your provider](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/hardware-asset-management/creating-script-include-for-provide-ztr.md).


## Zero Touch request flow tasks for your employees

1.  [Request a hardware asset through the Zero Touch request flow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/hardware-asset-management/request-hardware-assets-ztr-catalog.md).
2.  [Acknowledge receipt of an asset received through the Zero Touch request flow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/hardware-asset-management/acknowledge-ztr-asset-on-mobile.md).


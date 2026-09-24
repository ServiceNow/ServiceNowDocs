---
title: Configure Zero Touch request flow
description: The Zero Touch request flow requires a Service Exchange connection, service catalog items, and an integration profile so that employees can submit hardware requests through an external provider.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/hardware-asset-management/configure-ztr-flow.html
release: brazil
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Integrations and advanced configuration, Configure, Hardware Asset Management, IT Asset Management, Asset Management]
---

# Configure Zero Touch request flow

The Zero Touch request flow requires a Service Exchange connection, service catalog items, and an integration profile so that employees can submit hardware requests through an external provider.

The Zero Touch request flow requires setup on the provider ServiceNow instance and your ServiceNow instance so that requests are transmitted and fulfilled. The following configuration tasks are required.

## Setup required for providers

The provider must complete the following tasks to fulfill the requests received through the Zero Touch request flow:

1.  [Complete the Service Exchange setup for providers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/hardware-asset-management/service-bridge-for-ztreq.md).
2.  [Configure Scratchpad to send updates to your consumer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/hardware-asset-management/using-scratchpad-for-provider-updates.md).

**Note:** After completing the Zero Touch request flow prerequisites, the provider can fulfill provider tasks. For details, see [Fulfill a provider task](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/hardware-asset-management/fulfill-provider-task-ztr.md).

## Setup required for your Service Catalog requests

Complete the following tasks so that catalog requests can be fulfilled through an external provider:

1.  [Complete the Service Exchange setup for your service catalog requests](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/hardware-asset-management/service-bridge-for-ztreq.md).
2.  [Manage Service Catalog items for the Zero Touch request flow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/hardware-asset-management/manage-service-catalog-items-ztr.md).
3.  [Create a provider integration profile](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/hardware-asset-management/create-int-profile-ztr-ham.md).

    **Note:** You must perform this task only if the Scratchpad update received from your provider is not in the format required for the Zero Touch request flow. You must also [create a Script Include to transform Scratchpad updates from your provider](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/hardware-asset-management/creating-script-include-for-provide-ztr.md).


-   **[Configure Service Exchange for the Zero Touch request flow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/hardware-asset-management/service-bridge-for-ztreq.md)**  
The Zero Touch request flow uses the Service Exchange application to connect providers with your ServiceNow instance to manage hardware asset requests submitted through the Service Catalog.
-   **[Use the Scratchpad to complete your request fulfillment tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/hardware-asset-management/using-scratchpad-for-provider-updates.md)**  
As a provider, use the Scratchpad feature of the Service Exchange application to send updates to the ServiceNow instance of your consumer while performing the request fulfillment tasks.
-   **[Create a provider integration profile](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/hardware-asset-management/create-int-profile-ztr-ham.md)**  
Create a provider integration profile to convert any format of Scratchpad update sent by your provider to a format required for the Zero Touch request flow.
-   **[Create a Script Include to transform Scratchpad updates from the provider](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/hardware-asset-management/creating-script-include-for-provide-ztr.md)**  
To transform Scratchpad updates sent by your provider into a format required for the Zero Touch request flow, you must have a Script Include with the method **transformScratchPadToHAMZTRFormat**.

**Parent Topic:**[Integrations and advanced configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/hardware-asset-management/integrations-advncd-configs.md)


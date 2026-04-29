---
title: Virtual Agent for software requests
description: You can implement ServiceNow Virtual Agent to enable your employees to request software through a predefined conversational interface that is powered by artificial intelligence. Virtual Agent helps address software requests automatically so that your IT fulfillment professionals can focus on more complex requests and incidents.
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Exploring Software Asset Management, Software Asset Management, IT Asset Management]
---

# Virtual Agent for software requests

You can implement ServiceNow® Virtual Agent to enable your employees to request software through a predefined conversational interface that is powered by artificial intelligence. Virtual Agent helps address software requests automatically so that your IT fulfillment professionals can focus on more complex requests and incidents.

For information on how to implement and use Virtual Agent, see [Virtual Agent](https://www.servicenow.com/docs/access?context=virtual-agent-landing-page&version=australia&pubname=australia-conversational-interfaces&ft:locale=en-US).

## Prerequisites

Before you can begin using Virtual Agent for your software requests, complete the following prerequisites:

-   Activate the Software Asset Management Professional \(com.snc.samp\) plugin on your ServiceNow instance.

    See [Request Software Asset Management](../task/t_RequSoftwareAssetMgmt.md) for more information on how to activate this plugin.

-   Activate the Glide Virtual Agent \(com.glide.cs.chatbot\) plugin on your ServiceNow instance.

    See [Activate Virtual Agent](https://www.servicenow.com/docs/access?context=activate-virtual-agent&version=australia&pubname=australia-conversational-interfaces&ft:locale=en-US) for more information on how to activate this plugin.

-   Request and install the ITSM Virtual Agent Conversations application from the [ServiceNow Store](https://store.servicenow.com/).
-   Request and install the ITSM NLU Model for Virtual Agent Conversations application from the [ServiceNow Store](https://store.servicenow.com/).
-   Enable automatic allocation of your software by setting the workflow of the corresponding software catalog items to **Procurement Process Flow - Auto allocation enabled**. See [Create or edit a catalog item](https://www.servicenow.com/docs/access?context=t_DefineACatalogItem&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US) for more information on how to set the workflow for a software catalog item.

## Software request flow on Virtual Agent

When a user requests software, Virtual Agent automatically recommends appropriate options based on the software that is available in your software catalog. Upon selecting an option, the user is prompted to specify the user or device that the software is being requested for. Virtual Agent then generates a request item and initiates one of the following workflows to allocate rights to the specified user or device:

-   User allocation workflow: Allocates rights to the specified user. Virtual Agent initiates this workflow when the corresponding software entitlements support either user allocations only or both user and device allocations.
-   Device allocation workflow: Allocates rights to the specified device. Virtual Agent initiates this workflow when the corresponding software entitlements support either device allocations only or both user and device allocations.

**Note:** Rights are allocated to the specified user or device in ascending chronological order of software entitlements, starting with the oldest software entitlement.

**Note:** If a software entitlement supports both user and device allocations or your software contains both user allocation- and device allocation-based software entitlements, Virtual Agent initiates the user allocation workflow first. Virtual Agent initiates the device allocation workflow only after all user allocations are consumed.

If the corresponding software entitlements contain enough active rights and allocations to fulfill the request, Virtual Agent automatically approves the request and allocates rights to the specified user or device. The user is then provided with instructions to download and install the software.

If the corresponding software entitlements do not contain enough active rights and allocations to fulfill the request, you must source the required rights manually. After you source those rights, Virtual Agent automatically allocates them to the specified user or device. The user is then provided with instructions to download and install the software.

**Important:** Software can be requested and allocated using this same flow in the ServiceNow® Service Catalog and Employee Center. See [Service Catalog](https://www.servicenow.com/docs/access?context=service-catalog&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US) for more information on the Service Catalog. See [Employee Center](https://www.servicenow.com/docs/access?context=employee-center-landing-page&version=australia&pubname=australia-employee-service-management&ft:locale=en-US) for more information on the Employee Center.

**Parent Topic:**[Exploring Software Asset Management](explore-sam-workspace.md)


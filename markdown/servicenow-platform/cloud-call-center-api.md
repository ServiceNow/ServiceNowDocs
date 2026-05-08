---
title: Scripting for operation handlers
description: You can use the APIs in the ServiceNow Voice framework to create a seamless voice call experience for your callers and agents.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Setting up ServiceNow Voice, ServiceNow Voice, Manage people and work capabilities, Extend ServiceNow AI Platform capabilities]
---

# Scripting for operation handlers

You can use the APIs in the ServiceNow Voice framework to create a seamless voice call experience for your callers and agents.

The CTIOperationRequest API provides methods to set and get data on the current CTIOperationRequest object. For information on this API, see CTIOperationRequest - Scoped, Global.

The CTIOperationResponse API provides methods to set and get data on the current CTIOperationResponse object. For information on this API, see CTIOperationResponse - Scoped, Global.

The CTI API provides REST resources that enable Computer Telephony Integration \(CTI\) providers to interact with the Voice framework. For information about this API, see CTI API.

-   **[Provider configuration in Voice](provider-configuration-ccc.md)**  
For both inbound and outbound calls, a provider configuration contains settings about the involved components and message transformers for a specific third-party phone system provider. Any request from that phone system provider is handled within ServiceNow based on these settings.
-   **[Extension points in Voice](extension-point-ccc.md)**  
Using extension points, you can call the custom scripts to extend the functionality of ServiceNow Voice. While integrating a third-party phone system with ServiceNow Voice, you can invoke extension points using the CTI API to handle events in ServiceNow Voice.

**Parent Topic:**[Setting up ServiceNow Voice](ccc-setup.md)


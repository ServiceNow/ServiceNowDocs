---
title: Setup Integrated Facilities Management Integration Framework
description: Set up the Integrated Facilities Management \(IFM\) Integration Framework to connect Workplace Cases and Tasks in ServiceNow with external facilities management provider systems, enabling automated work order synchronization and end‑to‑end visibility across platforms.
locale: en-US
release: australia
product: Workplace Case Management
classification: workplace-case-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Workplace Case Management, Workplace Service Delivery, Employee Service Management]
---

# Setup Integrated Facilities Management Integration Framework

Set up the Integrated Facilities Management \(IFM\) Integration Framework to connect Workplace Cases and Tasks in ServiceNow with external facilities management provider systems, enabling automated work order synchronization and end‑to‑end visibility across platforms.

The Integrated Facilities Management \(IFM\) Framework automates the creation and management of work orders with third-party facilities management providers when workplace cases are created in ServiceNow. This framework facilitates bidirectional communication, allowing ServiceNow to create, add comments to work order, and cancel work order in external FM systems while receiving status updates and comments back from FM providers.

This integration framework eliminates manual work order creation and tracking, automates case-to-work-order lifecycle management, and provides unified visibility across both platforms.

## Benefits of Integrated Facilities Management Framework

The IFM Framework integration enables you to perform the following actions:

-   Create work orders automatically in external FM systems directly from ServiceNow workplace cases.
-   Configure provider routing rules to automatically assign workplace cases or tasks requests to appropriate FM providers based on service type, location, building, or custom criteria.
-   Track work order synchronization status in real-time using the FM Provider and FM Work Order ID fields on workplace cases.
-   Add comments to workplace case or task, and any updates will automatically appear in external work order.
-   Cancel workplace case and automatically trigger cancellation of corresponding work orders in FM provider systems.
-   Receive inbound updates from FM systems that automatically update ServiceNow cases or tasks.

## Case Lifecycle and Provider Ownership

1.  When a workplace case or task is created in ServiceNow, the provider routing engine evaluates the configured routing rules to determine the appropriate FM provider. Based on the matching rule, the selected provider is stamped on the workplace case or task record. The provider routing engine is triggered only at the time of record creation, and after the provider is stamped, it cannot be changed.
2.  Once the provider is stamped, the workplace case or task is automatically synchronized with the external FM provider system, where a corresponding work order is created.
3.  After synchronization is complete, the FM provider becomes the primary owner of the work order. Users can add comments or cancel the workplace case or task in ServiceNow, while all other edit operations are restricted to prevent data conflicts with the external FM provider system.

## Included Case Types

Only workplace cases with a Fulfillment type of Manual are eligible for synchronization with external FM provider systems.

## Excluded Task Types

The following task types are excluded from synchronization:

-   Automated Task
-   Assign Neighborhood Space
-   Consolidated Report
-   Select Space Option
-   Space Request

## Prerequisites and Requirements

The following plugins must be installed:

-   Workplace Core \(sn\_wsd\_core\)
-   Workplace Case Management \(sn\_wsd\_case\)
-   Integration Hub \(com.glide.hub.integrations.professional\)


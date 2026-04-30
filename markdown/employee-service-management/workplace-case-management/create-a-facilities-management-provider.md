---
title: Create a facilities management provider
description: Create a facilities management provider to connect Workplace Cases and Tasks in ServiceNow with an external facilities management \(FM\) system using the IFM Framework. The provider record defines how ServiceNow creates, updates, and cancels work orders in a third‑party FM system and enables end‑to‑end visibility across both systems.
locale: en-US
release: zurich
product: Workplace Case Management
classification: workplace-case-management
topic_type: task
last_updated: "2026-02-06"
reading_time_minutes: 1
breadcrumb: [Setup Integrated Facilities Management Integration Framework, Workplace Case Management, Workplace Service Delivery, Employee Service Management]
---

# Create a facilities management provider

Create a facilities management provider to connect Workplace Cases and Tasks in ServiceNow with an external facilities management \(FM\) system using the IFM Framework. The provider record defines how ServiceNow creates, updates, and cancels work orders in a third‑party FM system and enables end‑to‑end visibility across both systems.

## Before you begin

Role required: admin

## About this task

A Facilities Management Provider record represents a third-party FM vendor that can receive and manage work orders from ServiceNow workplace cases. Each provider has their own plugin application and configured flows that handle integration with their work order management system. After creating a provider, configure routing rules to automatically direct specific types of workplace requests to the appropriate FM provider based on service type, location, or other criteria.

## Procedure

1.  Navigate to **All** &gt; **Workplace Case Management** &gt; **Facilities Management - Setup** &gt; **Providers**.

2.  On the Facilities Management Providers page, select **New**.

3.  On the form, fill the field details.

    |Field|Description|
    |-----|-----------|
    |Title|The unique identifier name for the facilities management provider. For example, JLL.|
    |Active|Indicates whether the facilities management provider is currently active and available for integration.|
    |Create work order flow|Reference to the Flow Designer workflow that handles the creation of new work orders in the external FM provider system. This flow is triggered when a workplace case is created and a routing rule assigns it to this provider.|
    |Update work order flow|Reference to the Flow Designer workflow that synchronizes updates from ServiceNow to the external FM provider system. This flow handles operations such as adding comments or work notes to existing work orders.|
    |Cancel work order flow|Reference to the Flow Designer workflow that processes work order cancellation requests sent to the external FM provider system. This flow is triggered when a workplace case is cancelled, notifying the FM provider to cancel the corresponding work order in their system.|

    **Note:** For more information about work order flows, see .

    ![](../../workplace-service-delivery/images/FM_provider.png)

4.  Select **Submit**.



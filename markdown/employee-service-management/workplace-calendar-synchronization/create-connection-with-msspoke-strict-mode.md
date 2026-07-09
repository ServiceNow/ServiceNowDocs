---
title: Create connection with Microsoft Exchange Online Spoke in strict mode
description: Configure a strict mode connection with the Microsoft Exchange Online spoke.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/employee-service-management/workplace-calendar-synchronization/create-connection-with-msspoke-strict-mode.html
release: yokohama
product: Workplace Calendar Synchronization
classification: workplace-calendar-synchronization
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Create a strict mode connection with Microsoft Exchange Online, Microsoft Exchange Online - Calendar synchronization, Setup Workplace Calendar Synchronization, Configure, Workplace Calendar Synchronization, Workplace Service Delivery, Employee Service Management]
---

# Create connection with Microsoft Exchange Online Spoke in strict mode

Configure a strict mode connection with the Microsoft Exchange Online spoke.

## Before you begin

Role required: admin

## Procedure

1.  Install Microsoft Exchange Online spoke from the ServiceNow Store.

    For more information, refer to [Microsoft Exchange Online spoke](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/integrate-applications/ms-exch-online-spoke.md).

    **Note:** After installing Microsoft Exchange Online spoke, check that the **Data Stream action** field of the Data source **Exchange Online Calendar** is not set to empty. Otherwise, repair the Microsoft Exchange Online spoke plugin.

2.  After installing Microsoft Exchange Online spoke, depending on what type of customer you are, perform the following actions:

    -   If you are a new customer, to install the applications, refer to [Install Workplace Calendar Synchronization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/employee-service-management/workplace-calendar-synchronization/install-workplace-calendar-synchronization.md).
    -   If you are an existing customer, upgrade to the latest versions of the following applications:
        -   Workplace Reservation Management.
        -   Workplace Calendar Synchronization.
3.  Repair the Microsoft Exchange Online spoke if you never had an internal dependency on the **com.glide.hub.action\_type.datastream** plugin.

    1.  Navigate to **All** &gt; **System Definition** &gt; **Plugins**.

    2.  Search and select Microsoft Exchange Online Spoke.

    3.  Select **Repair**.


**Parent Topic:**[Create a strict mode connection with Microsoft Exchange Online](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/employee-service-management/workplace-calendar-synchronization/strict-mode-configurations-for-connection-with-msex.md)

**Related topics**  


[Configure Microsoft Azure]()

[Create a strict mode configuration in Microsoft Exchange Online]()

[Setup strict mode OAuth connectivity with Microsoft Exchange Online]()

[Configure strict mode Connection and Credential alias for Microsoft Exchange Online]()

[Create your own credential and connection alias for strict mode]()

[Configure Microsoft Exchange Online calendar provider in strict mode]()


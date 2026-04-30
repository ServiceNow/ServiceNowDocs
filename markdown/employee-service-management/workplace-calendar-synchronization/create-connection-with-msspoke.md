---
title: Create a connection with Microsoft Exchange Online spoke
description: Connect to the Microsoft Exchange Online spoke by creating a connection.
locale: en-US
release: xanadu
product: Workplace Calendar Synchronization
classification: workplace-calendar-synchronization
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Create a normal mode connection with Microsoft Exchange Online, Microsoft Exchange Online - Calendar synchronization, Setup Workplace Calendar Synchronization, Configure Workplace Calendar Synchronization, Workplace Calendar Synchronization, Workplace Service Delivery, Employee Service Management]
---

# Create a connection with Microsoft Exchange Online spoke

Connect to the Microsoft Exchange Online spoke by creating a connection.

## Before you begin

Ensure the following:

1.  Install Microsoft Exchange Online spoke from the ServiceNow Store. For more information, refer to [Microsoft Exchange Online spoke](https://www.servicenow.com/docs/access?context=ms-exch-online-spoke&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US).

    **Important:** After installing Microsoft Exchange Online spoke, check that the **Data Stream action** field of the Data source **Exchange Online Calendar** is not set to empty. Otherwise, repair the Microsoft Exchange Online spoke plugin.

2.  After installing Microsoft Exchange Online spoke, depending on what type of customer you are, perform the following actions:
    -   If you are a new customer, to install the applications, refer to [Install Workplace Calendar Synchronization](install-workplace-calendar-synchronization.md).
    -   If you are an existing customer, upgrade to the latest versions of the following applications:
        -   Workplace Reservation Management
        -   Workplace Calendar Synchronization
3.  Repair the Microsoft Exchange Online spoke. Perform the following repair if you never had an internal dependency on the **com.glide.hub.action\_type.datastream** plugin.
    1.  Navigate to **All** &gt; **System Definition** &gt; **Plugins**.
    2.  Search and select Microsoft Exchange Online Spoke.
    3.  **Repair** the plugin.

Role required: admin

## About this task

Synchronize reservations using a connection with the Microsoft Exchange Online spoke.

## Procedure

1.  Ensure that the Microsoft Exchange Online spoke is installed.

    Refer to the **Before you begin** section.

2.  [Set up Microsoft Exchange Online spoke](https://www.servicenow.com/docs/access?context=setup-ms-exch-ol&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US).

    If you are a new customer, in the **Create Connection records for the Microsoft Exchange Online spoke** procedure, perform the following actions:

    -   For **Microsoft\_Exchange\_Online** Connection and Credential alias, in the Connection related list, select **MS Graph 1** and make the changes.

        Do not change the **Name** and **Credential**. In the OAuth Entity Profile form of the **MS Graph 1** credential, ensure that the **Grant type** field is selected as **Client Credentials**.

    -   For **Microsoft\_Exchange\_Online\_clientCred** Connection and Credential alias, in the Connection related list, select **MS Graph 2** and make the changes.

        Do not change the **Name** and **Credential**. In the OAuth Entity Profile form of the **MS Graph 2** credential, ensure that the **Grant type** field is selected as **Client Credentials**.


## What to do next

[Set up OAuth connection with Microsoft Exchange Online](setup-connectivity-with-msexchange-for-calendar-sync.md)

**Parent Topic:**[Create a normal mode connection with Microsoft Exchange Online](../concept/create-connection-with-msex-in-normal-mode.md)

**Previous topic:**[Configure Microsoft Azure in normal mode](authenticate-mxexchange-with-azure.md)

**Next topic:**[Set up OAuth connection with Microsoft Exchange Online](setup-connectivity-with-msexchange-for-calendar-sync.md)


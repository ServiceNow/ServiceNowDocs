---
title: Configure Workplace Calendar Synchronization
description: Install and configure the Workplace Calendar Synchronization application to create personalized calendars across supported platforms, such as Microsoft Exchange Online, Google Calendar, or Microsoft Exchange On-Premises.
locale: en-US
release: australia
product: Workplace Calendar Synchronization
classification: workplace-calendar-synchronization
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Workplace Calendar Synchronization, Workplace Service Delivery, Employee Service Management]
---

# Configure Workplace Calendar Synchronization

Install and configure the Workplace Calendar Synchronization application to create personalized calendars across supported platforms, such as Microsoft Exchange Online, Google Calendar, or Microsoft Exchange On-Premises.

## Configuration overview

This section provides a guided overview of all foundational setup tasks, from installing the application and configuring authentication credentials, to creating calendar providers and linking reservable spaces. Use the step-by-step links below to quickly access and configure essential features, ensuring your calendar sync processes are streamlined and ready for use.

![](../../workplace-service-delivery/images/wsd-calendarsync-config.png)

## Connections

Calendar sync uses two types of connections that must both be configured correctly:

-   System-to-System — backend integrations that sync calendar data automatically between ServiceNow and the external calendar provider.
-   User-level — connections established per user performing actions in the application. Configuration requirements vary by integration mode.

## Synchronization Mode

Before starting configuration, select the synchronization mode that suits your organization's security and access requirements. Your mode choice determines how credentials are configured, which grant type is required, and whether a delegated user email is needed.

|Mode|Description|
|----|-----------|
|Normal|Syncs calendar events using each authenticated user's credentials. Suited for most organizations. No delegated user email required.|
|Strict|Routes all sync operations through a single shared service account \(delegated user\). Suited for high-security environments.|
|Personal|Each user individually authorizes access to their own calendar via an interface pop-up the first time they interact with the application.|

1.  [Install Workplace Calendar Synchronization](../task/install-workplace-calendar-synchronization.md)

    Install the Workplace Calendar Synchronization application from the ServiceNow Store.

2.  [Register ServiceNow as an OAuth Provider](../task/authenticate-mxexchange-with-azure.md)

    Register ServiceNow as an OAuth provider in your external calendar service such as Microsoft Azure Active Directory or Google Cloud Console to authorize the connection between ServiceNow and the calendar provider. This step generates the Client ID and Client Secret you will need when configuring the Application Registry.

3.  [Configure the Application Registry](../task/setup-connectivity-with-msexchange-for-calendar-sync.md)

    Configure the OAuth application registry records in ServiceNow using the credentials obtained during provider registration. These records establish the OAuth connection between ServiceNow and the external calendar provider.

4.  [Configure the Connection and Credential Alias](../task/create-connection-configuration-with-google.md)

    The Connection and Credential Alias securely stores the OAuth credentials that ServiceNow uses to authenticate with the external calendar provider. Configuration involves two parts: the system-to-system connection \(required for all modes\) and the user-level connection \(additional steps for Personal mode only\).

5.  [Create and Configure a Calendar Provider](../task/configure-google-as-calendar-provider.md)

    Create a Calendar Provider record in Workplace Calendar Synchronization to define the external calendar service, sync start and end times, synchronization mode, and associated connection settings.

6.  [Connect Reservable Spaces to the Calendar Provider](../task/add-reservable-sync-config.md)

    Create Reservable Sync Configuration records to link each ServiceNow room or space record to its corresponding resource mailbox or calendar entry in the external calendar provider. Each space that participates in calendar sync requires its own configuration record.


-   **[Install Workplace Calendar Synchronization](../task/install-workplace-calendar-synchronization.md)**  
Install the Workplace Calendar Synchronization application from ServiceNow Store applications. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

**Parent Topic:**[Workplace Calendar Synchronization](workplace-calendar-sync-feat.md)


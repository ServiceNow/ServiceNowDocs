---
title: Install Workplace Reservation Management
description: Install the Workplace Reservation Management application from ServiceNow Store applications. Visit the ServiceNow Store to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the ServiceNow Store version history release notes.
locale: en-US
release: australia
product: Workplace Reservation Management
classification: workplace-reservation-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Configure Workplace Reservation Management portal, Workplace Reservation Management, Workplace Service Delivery, Employee Service Management]
---

# Install Workplace Reservation Management

Install the Workplace Reservation Management application from ServiceNow Store applications. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Before you begin

Complete the following setup checklist for a smooth installation and configuration.

|Setup tasks|Description|
|-----------|-----------|
|Verify that Workplace Service Delivery - Core \(sn\_wsd\_core\) plugin of minimum version 2.0 is activated.|Navigate to **Subscription Management** &gt; **Subscriptions** in your instance. The list displays the subscriptions that your organization has purchased.|

Role required: admin

## About this task

Activate the Workplace Service Delivery - Core plugin \(sn\_wsd\_core\) of minimum version 2.0 in your ServiceNow instance before you install Workplace Reservation Management.

## Procedure

1.  Navigate to **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the application using the filter criteria and search bar.

    You can search for the application by its name or ID. If you cannot find an application, you may have to request it from ServiceNow store.

    Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

3.  Click **Install**.

4.  In the Application installation dialog box, review the application dependencies.

    Dependent plugins and applications are listed if they will be installed, are currently installed, or need to be installed. If there are any plugins or applications that need to be installed, you must install them before you can install Workplace Reservation Management.

5.  If demo data is available and you want to install it, click **Load demo data**.

    Demo data comprises sample records that describe application features for common use cases. Load demo data when you first install the application on a development or test instance.

    **Important:** If you don't load the demo data during installation, it's unavailable to load later.

6.  Click **Install**.


**Parent Topic:**[Configure Workplace Reservation Management portal](../concept/wsd-reservation-setup.md)

**Related topics**  


[Add a workplace space for reservation](add-reservable-items.md)

[Add a workplace room for reservation](add-workplace-rooms.md)

[Configure a reservable module](config-reservable-module.md)

[Assign spaces to an area](add-neighbourhood-spaces-to-an-area.md)

[Create a standard service](add-standard-services.md)

[Create a flexible service](add-flexible-service.md)

[Create a workplace service to provide an extra service for a reservation](create-workplace-service-to-provide-extra-service.md)

[Create a reservable view](create-a-reservable-view.md)

[Create a user criteria record](create-user-criteria.md)

[Configure a reservable purpose](configure-reservable-purpose.md)

[Create a quick reservation time slot](add-reservable-time-slots.md)

[Configure virtual meeting providers](configure-virtual-meeting-providers.md)

[Configure Microsoft Teams as virtual meeting provider](configure-msteams-as-virtual-meeting-provider.md)

[Connect Workplace Reservation Management with Microsoft Teams](connect-rsv-mgmt-with-teams.md)

[Connect Workplace Reservation Management with Zoom](connect-rsv-mtm-with-zoom.md)

[Display permanent seat assignments on floor maps](display-permanent-seats-on-maps.md)

[Display name of the person reserving a space](displayname-person-booking-rsv.md)

[Manage check-in and check-out reservations](../concept/check-in-check-out-process.md)

[Configure automatic check-in for reserved spaces](../concept/configure-rsv-check-in.md)

[Configure reservation multi-day settings in Reservable Module](../concept/rsv-config-rsv-mod-value.md)

[bundle-platadm.list-of-plugins]


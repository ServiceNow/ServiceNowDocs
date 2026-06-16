---
title: Workplace Calendar Synchronization release notes
description: Version history for the Workplace Service Delivery Workplace Calendar Synchronization on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-wsd-workplace-calendar-synchronization.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 18
breadcrumb: [ServiceNow Store - Workplace Service Delivery release notes, ServiceNow Store - Employee Service Management release notes, ServiceNow Store release notes]
---

# Workplace Calendar Synchronization release notes

Version history for the Workplace Service Delivery Workplace Calendar Synchronization on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 3.4.6 - June 2026**
    -   Fixed:
        -   The provider payload is not getting updated on read Events.
        -   Reservations where the room or location was added as a calendar invitee \(rather than entered in the Location field\) were not being processed.
        -   Workplace Event Planners were able to manage a reservation create in Google Calendar.
        -   In some cases, the parent reservation got cancelled after once one of the related reservations were cancelled.
        -   Security fixes
-   **Version 3.4.1 - March 2026**
    -   New: Synchronize reservations with Google Calendar using Personal Authentication.
    -   Changed:
        -   Synchronizing reservations from Google Calendar will now use last sync time, instead of the delta token.
        -   When using Exchange Online, recurring reservations are now synchronized as a recurring series rather than as single reservations.
    -   Fixed:
        -   In some cases, duplicate completed occurrences are being created after updating a recurring series.
        -   The "Synchronize past reservations" checkbox was deselected during provider record configuration.
        -   Admins could create a duplicate location by using "insert and say" when adding a new sync configuration record.
        -   Attendees were not added to the reservation when a reservation is synchronized from Google Calendar.
-   **Version 3.3.0 - December 2025**
    -   Changed: Enhancements made for recurring mutli-location reservations created in Exchange Online.
    -   Fixed:
        -   Read events from Google Calendar were failing for rooms if there the subject is empty.
        -   Subscriptions to Exchange Online resources were not still active after the alias was overwritten on calendar provider level.
        -   Improved processing for Microsoft Exchange Online of events when multiple reservations were created at the same time.
        -   Sometimes, the read event for Exchange On-premises \(EWS\) integrations could fail.
        -   Reservations could be stuck in Awaiting approval when no approvers qualify.
        -   Security fixes
-   **Version 3.2.0 - August 2025**
    -   New: Instance scans now also report if the location for a reservable sync configuration is empty and on the status for active subscriptions.
    -   Fixed:
        -   Services could not be added in Workplace Reservation Management when the reservation was created in Outlook with the strict-mode configuration.
        -   Creating a multi-location reservation using a previously rejected reservation could result in an error when synchronizing.
        -   The Connection and credential alias field was not visible for rsvsync admins
        -   Sometimes, services could not be added to an all-day reservation created in Outlook.
        -   Sometimes, when using the Workplace mobile experience, the employee was not asked to log in when their personal authentication expired while synchronizing reservations.
        -   The reservation could be stuck in the synchronization-required state if the virtual meeting link was generated while "Insert Calendar Sync Event" was still running.
        -   Unable to reserve a space through the Quick Reserve experience when personal authentication was enabled for the space.
        -   Duplicate visitor registrations could be created after updating a reservation in Outlook.
-   **Version 3.1.0 - May 2025**
    -   New:
        -   Reservations indicated as "true all day" will be synchronized as all-day reservations to Microsoft Exchange Online.
        -   Approvals managed in Exchange Online will follow the correct state.
    -   Fixed:
        -   Checking out reservations before the end time could result in an error.
        -   Rejecting a reservation that synchronizes with Google Calendar could result in an additional reservation.
        -   Conflicted reservations in Google Calendar were created in Workplace Reservation Management.
        -   Calendar items were not created from read-events with Exchange On-premises \(EWS\).
        -   Generic performance improvements
        -   Security fixes
-   **Version 3.0.0 - February 2025**
    -   New:
        -   Support for Personal Authentication: Sync reservations made in WSD to MS Exchange Online using the user's personal credentials.
        -   System property to enable the Personal Authentication feature.
        -   When Personal Authentication is enabled, the MS Exchange login screen will appear in all the three flows:Quick Reservation, Advanced Reservation, and Space Details flow.
    -   Changed:
        -   Updated guided setup indicates the configuration steps required for the Personal Authentication feature.
        -   All designer flows have been updated to run as logged-in user instead of as an admin when Personal Authentication is set up.
        -   The Strict mode email field will appear in the Provider configuration only if Personal Authentication or Strict mode is enabled in the system property.
    -   Removed: Strict Mode field from the Provider Configuration. Strict Mode configuration has been moved to the system property.
-   **Version 2.10.1 - November 2024**
    -   Fixed:
        -   Issue related to cancelling a reservation with a non-sync location.
        -   Issue related to payload start and end attributes in Calendar item.
        -   Few security issues
-   **Version 2.9.5 - August 2024**
    -   New:
        -   Set up Workplace Calendar synchronization more easily though the support of a Guided Setup.
        -   Retrieve reservations from Exchange Online more easily on provider or synchronization configuration level.
    -   Changed: A schedule is added to the "Workplace Calendar Synchronization Configurations" scan.
    -   Fixed:
        -   Start and end times were mapped incorrectly in the calendar item. This has been fixed.
        -   In some cases, the start time was mapped incorrectly, resulting in an incorrect update of the reservation. This has been fixed.
        -   The reservation stayed in "awaiting confirmation" state when the location was changed to a location that does require synchronization. This has been fixed.
        -   Cancelling a reservation that was synchronized and contained a virtual meeting link set the synchronization state to "Synchronization required". This has been fixed.
-   **Version 2.9.0 - May 2024**
    -   New: You can now use the diagnostics tools to validate the configuration when synchronizing reservations with Microsoft Exchange Online.
    -   Fixed: Adding double quotes in the reservation subject failed parsing, and led to duplicate reservations. This has been fixed now.
-   **Version 2.8.0 - February 2024**
    -   Changed:
        -   You can now access the Synchronization Health Dashboard from the Workplace Central workspace.

            -   If you have installed 2.6.4 or earlier versions of the app, you can still access the old version of the dashboard.

            -   If you are installing the app for the first time, i.e., from the 2.8.0 version onwards, you can only access the dashboard from the Workplace Central workspace.

-   **Version 2.6.4 - November 2023**
    -   Changed: The Synchronization Health Dashboard can now be accessed from the Workplace Central workspace. Download the Workplace Central plugin and open the 'Workplace Dashboards' tab to access the dashboard.
    -   Fixed:
        -   Earlier, the start and end times were incorrectly converted when the use\_user\_default\_tz was false. This has been fixed now.
        -   Earlier, the placeholder for the private subject was changed when the reservation was confirmed. This has been fixed now.
-   **Version 2.6.1 - August 2023**
    -   New:
        -   You can now synchronize reservations between Workplace Reservation Management and Exchange On-premises
            -   Employees can reserve reservations using either the Workplace Reservation Management or Exchange On-premises. The synchronization ensures that both systems have the latest availability.
            -   Employees can create a fully serviced reservation. They can add desired services using the Workplace Reservation Management application. The reservation will show in the employee's calendar.
            -   You can view a list of all the synchronized reservations created in Exchange On-premises or Workplace Reservation Management in the My Reservation overview. You can view the reservation details or add services if required.
        -   The application will now automatically recreate subscriptions and synchronize spaces since its last successful sync in case there were any errors while synchronizing reservations with the space. Admins will receive an email notification listing the spaces that incurred an error.
        -   An additional archiving configuration has been introduced.
    -   Changed: Performance improvements have been made while processing create or edit events received from Exchange.
    -   Fixed:
        -   Earlier, the state of the reservations created in a multi-location was stuck in awaiting confirmation with a location that did and did not sync. This has been fixed.
        -   Earlier, in some cases, the parent reservation for a recurring series showed check-in and got canceled when no check-in was done. This has been fixed.
        -   Earlier, the location reference was empty on the reservable sync configuration when a location record was deleted. This generated errors while synchronizing locations. This is fixed now.
        -   Earlier, additional update calls were made while creating a reservation with services. This has been fixed.
        -   Earlier, creating a reservation supported by the Outlook add-in triggered additional calls that fell into errors. This has been fixed.
        -   Earlier, the "Is parent" value was not checked on the parent reservation record when a recurring reservation was created in Outlook. This has been fixed.
        -   Earlier, when changing the location related to another calendar provider record, the update call generated an error. This has been fixed.
        -   Earlier, in some cases, moving the first occurrence in a series did not free up the space in Workplace Reservation Management. This has been fixed.
        -   Earlier, the "Events in error in last 24 hours" report also showed errors that were not from the last 24 hours. This has been fixed.
        -   Earlier, in some cases, the meeting ID was removed from the reservation record after receiving a callback and updating the reservation to confirm. This has been fixed.
        -   Earlier, when making a reservation using two different providers, the process of updating a reservation to a new space in a new provider resulted in an error. This has been fixed.
        -   Earlier, adding an external guest to a reservation resulted in an error when the email was case-sensitive. This has been fixed.
        -   Earlier, canceling a recurring series in Outlook with a virtual meeting link did not remove the link from the parent record. This has been fixed.
        -   Earlier, some email notifications generated an error due to invalid or missing references with mail scripts. This has been fixed.
-   **Version 2.5.0 - May 2023**
    -   New:
        -   The Microsoft Teams meeting links can now be retrieved and also saved on the reservation record when synchronizing events.
        -   The Microsoft Teams meeting details are now added to the body of the event when synchronizing events to calendar providers, after reserving it in Workplace Reservation Management.
        -   You can now additional meeting notes to the body of the event when synchronizing events to calendar providers.
    -   Fixed:
        -   Earlier, multi-parent reservations got canceled when a rejected reservation was changed to a multi-location reservation using Google Calendar. This has been fixed now.
        -   Earlier, changing a multi-location reservation to a single-reservation in the calendar provider, linked the canceled parent record to the reservation. This has been fixed now.
        -   Earlier, multi-location reservations created in the calendar provider ignored the check-in configuration. This has been fixed now.
        -   Earlier, events generated after updating reservations ended with the error 'TypeError: Cannot read property content from undefined'. This has been fixed now.
        -   Earlier, changing a single reservation to a multi-location reservation triggered an additional event. This has been fixed now
-   **Version 2.4.0 - February 2023**
    -   Changed: Handling events when receiving multiple notifications or getting the occurrence information when synchronizing events with Microsoft Exchange Online has been improved.
    -   Fixed:
        -   Earlier, Google Calendar did not sync when a connection alias other than 'wsd\_rsvsync\_alias\_google\_calendar' was used on the calendar provider. This has been fixed now.
        -   Earlier, the scheduled job created empty records for those locations which had expired or corrupted sync delta records. This has been fixed now.
        -   It was possible to set a reservation as busy even if the reservation was rejected and updated later. This has been fixed now.
        -   Rejecting a reservation twice could result in an 'update failed' error message. This has been fixed now.
        -   In a few cases, the blocker preparation and cleanup reservations were not being cleared up even if they were rejected. This has been fixed now.
        -   In a few cases, the reservable module was empty for recurring reservations. This has been fixed now.
        -   In a few cases, the building field of the recurring parent reservation was empty. This has been fixed now.
        -   In a few cases, the subject was not updated for the recurring parent reservation. This has been fixed now.
        -   A sync event could result in an error for multi-location reservations after receiving a duplicate message. This has been fixed now.
        -   Visitor registrations would get canceled if an email is entered in upper case Workplace Reservation Management and lower case in the calendar. This has been fixed now.
-   **Version 2.3.1 - December 2022**
    -   New:
        -   Support is now added to handle throttling events between ServiceNow and Microsoft Exchange Online while synchronizing events on spaces.
    -   Changed:
        -   Adding a new reservable sync configuration directly from the provider will now make the 'Provider' field on the form read-only.
        -   You can now create subscriptions in Microsoft Exchange Online for reservable sync configurations by selecting one or more records and by using the UI action to activate them. This will work the same while you deactivate these configurations.
    -   Fixed:
        -   Earlier, after checking a reservation, the check-in state was reset. This has been fixed now.
        -   Earlier, empty records were created in the online spoke subscriptions table when the calendar provider got \(de\)activated. This has been fixed now.
        -   Earlier, blocker reservations were not canceled when their related reservation was rejected. This has been fixed now.
        -   Earlier, canceling a multi-location reservation with additional services through the Outlook add-in did not cancel the multi-parent reservation. This has been fixed now.
-   **Version 2.2.2 - November 2022**
    -   Changed:
        -   The subscription creations while synchronizing with Microsoft Exchange have been updated. The subscriptions will now be created in phases.
    -   Fixed:
        -   Earlier, attendees and visitors were captured multiple times when a recurring reservation was synchronized from the calendar provider. This has been fixed now.
        -   Earlier, reservations were not synchronized accordingly when removing spaces from a multi-location reservation. This has been fixed now.
-   **Version 2.2.1 - August 2022**
    -   New:
        -   You can control how a reservation must appear in the employee's calendar or while generating an iCalendar-file.
        -   You can now synchronize all types of spaces with a calendar provider, just like spaces of the type rooms.
        -   You can push reservations to a calendar provider as part of a migration process. The system will create reservations created in Workplace Reservation Management. The admin can synchronize reservations created in WSD towards the calendar provider as part of a migration. Using a set interval, reservations are created in the calendar provider and related to the reservation.
    -   Changed:
        -   The system will block the space in the calendar provider when reserving the space in the Workplace Reservation Management that requires approval.
        -   In case a reservation gets rejected, the reservation will be removed from the calendar but will remain in the employee's calendar.
        -   It is now possible to specify which connection to be used per provider. This makes it easier to have multiple configurations and manage them more easily.
        -   General performance improvements have been made.
    -   Fixed:
        -   Earlier, the page size defined on the calendar provider was not considered while synchronizing the reservations from google calendar. This has been fixed now.
        -   Earlier, a reservation's start and end times were always updated, even when the subject of the reservation was updated, when the property use\_user\_default\_tz was set to true. This has been fixed now.
        -   Earlier, not all fields were validated correctly when using insert and stay. This has been fixed now.
        -   Earlier, in some cases, the related calendar provider was not updated after changing a single reservation into a multi-location reservation. This has been fixed now.
        -   Earlier, after approving a reservation an additional synchronization happed. This has been fixed now.
        -   Earlier, in some cases, the source record for a recurring reservation was not updated correctly. This has been fixed now.
-   **Version 2.1.2 - May 2022**
    -   New:
        -   Invitee attendees such as co-workers and visitors while making a reservation.
            -   You can synchronize your reservation along with your colleagues reservation when the reservation synchronization is enabled.
            -   You can invite or remove attendees while synchronizing reservations. If there an external visitors, you can automatically create a visitor registration. If they are revisiting, you can select their details from the list of known visitors.
-   **Version 2.0.4 - March 2022**
    -   Fixed:
        -   The related blocker meetings are now updated after changes to the reservation made in Outlook.
        -   The reservations that are created in Workplace Reservation Management and then later updated in the Google Calendar are now correctly updated in Workplace Service Delivery.
-   **Version 2.0.1 - February 2022**
    -   New: While making a reservation, the reservation is now scheduled based on the time zone of the building. While you synchronize the reservations, you can indicate which time zone is used.
    -   Changed: The events synchronization between Workplace Calendar Synchronization and Exchange Online will now be handled through ServiceNow Integration Hub. If there are any changes, they are directly sent to and processed by the Exchange Online and/or Workplace Reservation Management.
    -   Fixed:
        -   Earlier, the blocker meetings were not always created when services were added afterward in Workplace Service Delivery for reservations made in Outlook. This has been fixed.
        -   Blocker meetings are created even if the extra services are added later in Workplace Service Delivery for reservations made in Outlook.
        -   The reservations for rooms will no longer remain in the draft state. They are now updated in Outlook.
-   **Version 1.6.1 - December 2021**
    -   New:
        -   The Event table now applies a default filter to show events created on the current day.
        -   It is now possible to specify which connection to be used per provider. This makes it easier to have multiple configurations and manage them more easily.
        -   Updating a reservation in Workplace Reservation Management will now also try to retrieve the added attendees in the calendar provider.
        -   Old calendar items are now automatically archived.
    -   Changed: Previously, it was required to set the email address on the location before creating a new reservable sync configuration. Now, when you create a new Reservable sync configuration, the email address is set to the location if it is empty.
    -   Fixed: Setting the locations to No-Request resulted in an error for the related synchronization events.
-   **Version 1.5.8 - October 2021**
    -   Fixed:
        -   All-day events created using the Google Calendar did not display the correct duration.
        -   Dates were not validated properly while configuring a new Calendar provider.
        -   Events to synchronize multi-location reservations from the Google Calendar resulted in errors.
-   **Version 1.5.2 - September 2021**
    -   New:
        -   You can now synchronize reservations between Workplace Service Delivery and Google Calendar using the application. Synchronize a single reservation, recurring reservations, and multi-location reservations, created from Workplace Reservation Management application to Google Calendar, or from Google Calendar to the Workplace Reservation Management application.
        -   You can invite an employee to their own reservation, instead of directly inserting the reservation into the employee's calendar, adding an additional level of security. The feature is only available in combination with Microsoft Exchange Online.
    -   Changed: The icons displayed to indicate the source of the reservation \(Workplace Reservation Management or one of the calendar providers\) has been updated.
-   **Version 1.4.2 - July 2021**
    -   New: The application is now compatible with the new application, Workplace Reservations for Microsoft Outlook Add-in to ensure that the reservations being made are updated correctly in both systems.
-   **Version 1.3.1 - June 2021**
    -   New:
        -   You can now specify if the user's time zone must be used during reservation synchronization with the calendar provider. When a user edits or updates their reservation in the default calendar provider application, the times are displayed as per their time zone.
    -   Changed:
        -   The email address of a room that is used for integration can now be updated from the room's configuration form directly.
        -   The flows that handle the reservation process have been improved. They will now provide a much clearer and seamless experience while creating, updating, and synchronizing a reservation.
-   **Version 1.2.1 - March 2021**
    -   Changed:
        -   An indication is displayed to confirm if the reservations created or updated in the past require synchronization or not.
-   **Version 1.1.1 - January 2021**
    -   New:
        -   Synchronize reservations containing multiple workplace items.
        -   Use the Synchronization Health Dashboard to view the state and health of the calendar synchronization process.
        -   Archive old events and calendar items.
    -   Changed:
        -   The module name is now changed to 'Workplace Calendar Synchronization'.
        -   The handling of the states during the reservation process is improved. This will now provide a more seamless experience when creating, updating, approving, and synchronizing a reservation.
    -   Resend events to the calendar service if the event is declined or has an error.
    -   Fixed:
        -   Earlier, when canceling a single reservation, the reservation was not canceled in the Microsoft Exchange. This has been fixed now.
        -   Earlier reservations created in the calendar service did not require check-in and check-out. This has been fixed now.
-   **Version 1.0.2 - December 2020**

    The ServiceNow® Workplace Calendar Synchronization ensures employees are kept up to date with room reservations across their enterprise calendar provider, eliminating potential conflicts. The application enables you to configure and sync workplace items, requests and reservations with common enterprise calendar providers and ServiceNow Workplace Reservation Management. To automatically install all the Workplace Calendar Synchronization applications at once, download the ServiceNow® Workplace Service Delivery Suite.


## Notice regarding use by organizations

All decisions in connection with the implementation of this application are at the sole decision of the Organization utilizing this application. Organizations agree that use of the application is not a representation by ServiceNow regarding the application’s compliance with any law or regulation and any suggested language provided out of the box with the application does not constitute legal advice by ServiceNow.

Organizations remain solely responsible for complying with their legal obligations under applicable law, including \(but not limited to\) data protection and employment laws, and should modify any language within the templates provided to meet the Organizations' specific requirements.

## Notice regarding use by government agencies

ServiceNow is offering this application to government agencies and their authorized users, not to government employees in their individual capacities. Use of the application does not modify any existing, or future entitlements or payment obligations for ServiceNow software or applications otherwise purchased by the government agency. ServiceNow shall not be responsible for any implementation or configuration costs associated with use of the application unless separately purchased. Government customers are solely responsible to confirm with the agency’s Ethics Office or its authorized representative that acceptance and usage of the application is permissible.

All decisions in connection with the implementation of this application are at the sole decision of the government agency utilizing this application. Agencies remain solely responsible for complying with their legal obligations under applicable laws and regulations, including \(but not limited to\) data protection and employment laws and regulations, and should modify any language within the templates provided to meet the agency’s specific requirements.

**Parent Topic:**[ServiceNow Store - Workplace Service Delivery release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-wsd-highlight.md)


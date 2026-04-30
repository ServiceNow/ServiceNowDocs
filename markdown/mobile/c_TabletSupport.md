---
title: Tablet interface
description: Use a tablet to access your instance either app or from a browser.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2026-04-29"
reading_time_minutes: 2
breadcrumb: [Access instances on mobile web browser, Using the mobile apps, Mobile Platform]
---

# Tablet interface

Use a tablet to access your instance either app or from a browser.

Use the native tablet app for an experience similar to the native mobile app. Applications or modules that you have favorited in a desktop instance appear as tiles on your mobile app homescreen.

The tablet web UI mimics the desktop experience in Core UI. `$tablet.do` has been disabled in Core UI because the tablet interface is the same as the desktop.

Connect to an instance using the browser on your tablet for an experience similar to the standard desktop user interface.

## Tablet features with limited support

-   Editing lists: You cannot edit field values in a record from the list view. Access the record form to modify any field values.
-   Dependency Views map, schema map, graphical Workflow Editor, Gantt chart, and visual dispatch tool: Graphics-based tools can be viewed but not modified from the tablet interface. Data presented by these tools is read-only when accessed through the tablet interface.
-   Calendars: You can access calendar reports but scrolling around the calendar as you would on the desktop interface is not supported.
-   Video and image attachment upload: Attach videos and images with both iOS 9 and Android. Other file type attachments are not allowed.

## Unsupported tablet features

-   Field watcher: Administrators must use the desktop version to access the Field Watcher.
-   JavaScript debugger: Administrators must use the desktop version to access the JavaScript debug window.
-   Language picker: Even if the internationalization plugin is enabled, the language picker does not appear in the tablet UI toolbar. Language selected through the desktop interface applies to the tablet UI.
-   Domain picker: Tablet users cannot select any other domains that administrators configure for domain-specific personalizations. To select a new domain, use the desktop interface.
-   Slushbucket feature: Any lists, fields, or filters that use the slushbucket feature are unsupported on a tablet device. Slushbuckets are only supported in the desktop interface.
-   Suffix in the navigation filter: You can use the `.list`, `.do`, or `.form` shortcuts to access a list of records in a table or a new form from the desktop version only.
-   Support chat: End users cannot request a chat session nor can support technicians respond to chat requests when using the tablet interface. Help desk chat is only supported in the desktop interface.
-   Printer friendly view: This view, which shows the current screen in a pop-up window without frames and the application navigator, is not available from the tablet.
-   Timeline sliders and the Timeline Metrics UI actions: Features that use timelines, such as the workflow timeline and the Gantt chart are not supported from the tablet.

**Parent Topic:**[Accessing an instance on a mobile device web browser](mobile-access-options.md)


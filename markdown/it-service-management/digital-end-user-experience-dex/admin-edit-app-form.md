---
title: Edit web or installed application form
description: Using a custom form, you can edit an application to be monitored for compliance or performance metrics.
locale: en-US
release: xanadu
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Administration cards, DEX Application and Device Health reference, Reference, Digital End-User Experience, IT Service Management]
---

# Edit web or installed application form

Using a custom form, you can edit an application to be monitored for compliance or performance metrics.

<table id="table_qqf_kv4_qdc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Select an application service

</td><td>

Application service associated with the application added for monitoring.

</td></tr><tr><td>

What domains should be monitored

</td><td>

Web address that is used to launch the application and access its features and functions.This field appears only if you're editing a web application.

</td></tr><tr><td>

What processes should be monitored?

</td><td>

Processes that you want to monitor.This field has the following subfields:

-   **Windows: Enter the process name \(ex. process.exe\)**: A unique identifier for the primary running instance of the Windows application.
-   **Windows: Secondary processes separated by a comma**: A unique identifier for the secondary running instance of the Windows application.
-   **Mac: Enter the process name \(ex. process.dmg\)**: A unique identifier for the primary running instance of the macOS application.
-   **Mac: Secondary processes separated by a comma**: A unique identifier for the secondary or more running instance of the macOS application.
-   **Web Endpoint Connection**: A comma-separated list of domains used for measuring network latency. Example: company-name.zoom.us, company-name.outlook.com.

**Note:** Typically, you fill in this field for the applications you have installed that connect to the cloud.


This field appears only if you're editing an installed application. The primary and secondary processes might be automatically populated for the selected application.

</td></tr><tr><td>

Upload a logo

</td><td>

Link to upload or edit the logo of an application.

</td></tr><tr><td>

Monitoring

</td><td>

Toggle switch to enable or disable monitoring for the application performance and system compliance.This field has the following options:

-   **Compliance**: Enables reporting on whether this application is running on your organization's devices.
-   **Metrics**: Enables performance reporting for this application.

Move the monitoring toggle switch \(![Use the toggle switch to activate monitoring for the application.](../image/icon-toggle-button-enabled.png)\) to turn the reporting on or off.

**Note:** You can also enable monitoring for multiple applications simultaneously. From the Application management page, use the bulk check box to select multiple applications, and adjust your selection as needed with the individual check boxes for each app.

This field appears only if you select an installed application to edit.

This field doesn't appear when you're onboarding Application and Device Health.

</td></tr></tbody>
</table>**Parent Topic:**[Administration cards](administration-cards.md)


---
title: New web or installed application form
description: Using a custom form, you can add an application to be monitored for compliance or performance metrics.
locale: en-US
release: zurich
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Administration cards, DEX Application and Device Health reference, Reference, Digital End-User Experience, IT Service Management]
---

# New web or installed application form

Using a custom form, you can add an application to be monitored for compliance or performance metrics.

<table id="table_qqf_kv4_qdc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Select an application service

</td><td>

List of application services that references the Service \(cmdb\_ci\_service\) table to select an application service added for monitoring.You can open the list of available services by selecting the magnifying glass icon \(![](../image/icon-magnifying-glass-blue.png)\).

</td></tr><tr><td>

What domains should be monitored?

</td><td>

Web address that is used to launch the application and access its features and functions.You can add a domain by selecting **+ Add**. Add one or more domains, separated by a comma. You can enable metrics monitoring on each domain name you add.

This field appears only if you select **Web application** under the **New** drop-down list.

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


This field appears only if you select **Installed application** under the **New** drop-down list.

</td></tr><tr><td>

Enable page-level monitoring

</td><td>

Specific pages to monitor within the domain.You can add a specific page to monitor after adding and saving the application to monitored applications. In the Application management table, select the added application to set up one or more pages. See [Set up page-level monitoring](../concept/set-up-page-level-monitoring.md) for more details.

This field appears only if you select **Web application** under the **New** drop-down list.

</td></tr><tr><td>

Monitoring

</td><td>

Toggle switch to enable or disable monitoring for the application performance and system compliance.This field has the following options:

-   **Compliance**: Enables reporting on whether this application is running on your organization's devices.
-   **Metrics**: Enables performance reporting for this application.

Move the monitoring toggle switch \(![](../image/icon-toggle-button-enabled.png)\) to turn the reporting on or off.

**Note:** You can also enable monitoring for multiple applications simultaneously. From the Application management page, use the bulk check box to select multiple applications, and adjust your selection as needed with the individual check boxes for each app.

This field appears only if you're editing an installed application.

This field doesn't appear when you're onboarding Application and Device Health.

</td></tr><tr><td>

Advanced monitoring

</td><td>

Option available for the Microsoft Configuration Manager \(MCM\) application.Select the MCM app from the drop-down list to enable advanced monitoring.

This field appears only if you select **Installed application** under the **New** drop-down list.

</td></tr><tr><td>

Enable usage tracking \(optional\): SAM product

</td><td>

Option to add a Software Asset Management \(SAM\) product to enable tracking of the usage and last access time.When the SAM plugin \(com.snc.samp\) is installed, the **SAM product** field changes into a drop-down list that references the samp\_sw\_product table. If you can't find an application in the drop-down list, you can add it by selecting the **+ New SAM product** button.

This field appears only when you're editing a web application.

For more information, see [Using DEX or SAM for application monitoring](../concept/using-dex-or-sam-for-app-monitoring.md).

</td></tr></tbody>
</table>**Parent Topic:**[Administration cards](administration-cards.md)


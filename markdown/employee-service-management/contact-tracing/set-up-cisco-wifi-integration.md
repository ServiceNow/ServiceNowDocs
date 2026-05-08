---
title: Configure Cisco DNA Spaces settings for Wi-Fi access logs
description: Set up the Cisco DNA Spaces integration for Wi-Fi access logs.
locale: en-US
release: australia
product: Contact Tracing
classification: contact-tracing
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Retrieving Wi-Fi access log data, Contact Tracing, Safe Workplace, Health and Safety, Employee Service Management]
---

# Configure Cisco DNA Spaces settings for Wi-Fi access logs

Set up the Cisco DNA Spaces integration for Wi-Fi access logs.

## Before you begin

Role required: admin

## About this task

Cisco DNA Spaces integration provides two options to get the Wi-Fi access data from Cisco DNA Spaces into your ServiceNow instance.

-   By generating and downloading the proximity report from the Cisco DNA Spaces portal or through a manual import.
-   By importing Wi-Fi access raw data files from a secured FTP \(SFTP\) server. These files are uploaded from Cisco DNA Spaces every day at a scheduled time.

To specify which option to use, configure the **sn\_imt\_tracing.wifi\_log\_cisco\_tier** system property. For each option, you must also complete additional settings.

## Procedure

1.  Complete the following steps for using Wi-Fi access data from the proximity report.

    1.  Create an OAuth application endpoint for Cisco DNA Spaces and share the Client Id and Client Secret with Cisco to complete the integration on their side.

        On the Application Registries form, enter the following callback URL in the **Redirect URL** field based on the region:

        -   USA region: `https://dnaspaces.io/integrations/servicenow`
        -   Europe region: `https://dnaspaces.eu/integrations/servicenow`
        For more information on creating the OAuth application endpoint and description of other fields on the form, see Create an endpoint for clients to access the instance.

    2.  Log in to the Cisco DNA Spaces portal to register and authenticate the application to complete the integration.

    3.  Set the proximity level in the **sn\_imt\_tracing.wifi\_proximity\_preference** system property to consider employee interaction with an affected employee as potential exposure.

        For more information, see [System properties for tracing systems in Emergency Exposure Management](../../business-continuity/reference/list-of-tracing-system-sys-properties.md).

    4.  Review the base system DiagnosticTaskImportUtil script include.

        The DiagnosticTaskImportUtil script include creates a data source from the attachment in a diagnostic request task and imports the data into the Wi-Fi Access Register \[sn\_imt\_tracing\_wifi\_access\_register\] table.

        For more information, see Script includes.

2.  Set system properties to use the Wi-Fi access data files imported from the SFTP server into the Wi-Fi Access Register table.

    1.  Navigate to **Contact Tracing** &gt; **Administration** &gt; **Properties**.

    2.  Configure the following system properties:

        -   **sn\_imt\_tracing.wifi\_log\_sftp\_server**
        -   **sn\_imt\_tracing.wifi\_log\_sftp\_port**
        -   **sn\_imt\_tracing.wifi\_log\_sftp\_file\_path**
        -   **sn\_imt\_tracing.wifi\_log\_sftp\_load\_time**
        -   **sn\_imt\_tracing.wifi\_log\_sftp\_username**
        -   **sn\_imt\_tracing.wifi\_log\_sftp\_password**
        For more information on these properties, see [System properties for tracing systems in Emergency Exposure Management](../../business-continuity/reference/list-of-tracing-system-sys-properties.md).

3.  Configure office locations that contain Cisco Wi-Fi devices.

    1.  Navigate to **Contact Tracing** &gt; **Wi-Fi Access Management** &gt; **Wi-Fi Diagnostic Preferences**.

    2.  Click **Generate Location Preferences**.

    3.  In the Generate Location Preferences window, select **Use Cisco DNA Spaces** from the list.

    4.  Click **OK**.

    All locations with the **Use Cisco DNA Spaces** preference use the Wi-Fi access data from Cisco DNA Spaces.


## What to do next

Run the diagnostic request using the Wi-Fi access logs for an employee who is classified as positive for a condition, such as COVID-19, and is from a location with a Cisco Wi-Fi network. The Wi-Fi access logs provide a list of potentially impacted employees who used the same Wi-Fi network as the affected employee. For more information on running the diagnostic request, see [Identify potentially exposed users](../../business-continuity/task/use-emergency-exposure-mgnt.md).

**Parent Topic:**[Retrieving Wi-Fi access log data](../concept/wifi-access-management.md)


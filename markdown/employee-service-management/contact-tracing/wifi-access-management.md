---
title: Retrieving Wi-Fi access log data
description: 
locale: en-US
release: australia
product: Contact Tracing
classification: contact-tracing
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Contact Tracing, Safe Workplace, Health and Safety, Employee Service Management]
---

# Retrieving Wi-Fi access log data

Contact Tracing provides the following options:

-   Manually upload data from a Microsoft Excel spreadsheet by using the import Wi-Fi access logs option
-   Automatically get the Wi-Fi access logs from external systems by using the integration option

Integration with the following systems is available:

-   **[Integration with Mist Systems](../task/identify-exposed-employees-wifi-logs.md)**

    Use the Mist Systems API to automatically import the Wi-Fi access logs data into the Wi-Fi Access Register table.

-   **[Integration with Cisco DNA Spaces](../task/set-up-cisco-wifi-integration.md)**

    Import the Cisco DNA Spaces Wi-Fi access data into the Wi-Fi Access Register \[sn\_imt\_tracing\_wifi\_access\_register\] table by either generating a proximity report or downloading the access data into a spreadsheet and then uploading it.

    -   Microsoft Excel spreadsheet: Download the proximity report from Cisco DNA Spaces and attach the file in the diagnostic request task.
    -   Proximity report: Log in to the Cisco DNA Spaces portal and generate the proximity report by providing the diagnostic request task number. The proximity report containing the Wi-Fi access logs is posted into the Wi-Fi Access Register table.

        For more information, see [Fetch potentially exposed user data from a data source](../../business-continuity/task/work-on-diagnostic-req-task.md#).

    -   Wi-Fi access data files: Import Wi-Fi access data from the files from a Secured FTP server into the Wi-Fi Access Register table. Cisco DNA Spaces system uploads these raw data files containing the Wi-Fi access data each day on a scheduled time. The data is imported from these files when you run the diagnostic request to identify potentially exposed employees.

        **Note:** The file from the SFTP server for a specific day is imported into the Wi-Fi Access Register table only once. Any subsequent diagnostic requests use the data in the table to generate the list of potentially exposed employees.


-   **[Add wearable devices assigned to employees](../task/add-wearable-devices.md)**  
Add wearable devices such as Bluetooth LE-enabled devices that are assigned to employees to enable them to connect to the Wi-Fi network in your workplaces.
-   **[Create an organization and load sites](../task/set-up-organization.md)**  
Create an organization for which you are collecting the Wi-Fi access logs using Mist Systems. After you have created an organization, load sites using a scheduled job.
-   **[Configure Cisco DNA Spaces settings for Wi-Fi access logs](../task/set-up-cisco-wifi-integration.md)**  
Set up the Cisco DNA Spaces integration for Wi-Fi access logs.
-   **[Import your Wi-Fi access logs spreadsheet](../task/import-wifi-data.md)**  
Import Wi-Fi access logs from an Excel spreadsheet into the Wi-Fi Access Register table.
-   **[Use Wi-Fi access logs from Mist Systems](../task/identify-exposed-employees-wifi-logs.md)**  
Identify potentially exposed employees using Wi-Fi access logs from Mist Systems.
-   **[Use imported Wi-Fi access logs](../task/identify-exposed-employee-ma-logs.md)**  
Identify potentially exposed employees by manually importing Wi-Fi access logs into the Wi-Fi Access Register table.

**Parent Topic:**[Contact Tracing](contact-tracing.md)


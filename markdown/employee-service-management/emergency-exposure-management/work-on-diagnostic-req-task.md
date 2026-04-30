---
title: Fetch potentially exposed user data from a data source
description: Work on the diagnostic request task to get information about potentially impacted users from a selected data source and populate the corresponding related lists on the Diagnostic Request form.Fetch potentially exposed user information from the Cisco Wi-Fi access log data and populate the corresponding related lists on the Diagnostic Request form.Upload a spreadsheet containing the Zebra MotionWorks proximity data to fetch a list of potentially exposed users and populate the corresponding related lists on the Diagnostic Request form.
locale: en-US
release: xanadu
product: Emergency Exposure Management
classification: emergency-exposure-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Identify potentially exposed users, Emergency Exposure Management, Emergency Response Management, Workplace Service Delivery, Employee Service Management]
---

# Fetch potentially exposed user data from a data source

Work on the diagnostic request task to get information about potentially impacted users from a selected data source and populate the corresponding related lists on the Diagnostic Request form.

## Before you begin

Role required: sn\_imt\_diagnosis.diagnostics\_admin or admin

## About this task

The diagnostic request task is created from the diagnostic request task configuration for the data source type selected in the Diagnostic Request form. For more information, see [Create or modify a diagnostic request task configuration](create-diagnostic-task-config.md).

## Procedure

1.  Navigate to **Emergency Exposure Management** &gt; **All**.

2.  Open a diagnostic request from the list.

3.  In the Diagnostic Request Tasks related list, open a diagnostic request task.

4.  Follow the instructions in the task to fetch data on potentially impacted users from the selected data source.

5.  If the task configuration requires you to manually close the task, select **Closed** in the State list.

6.  Click **Update**.


## Result

The state of the diagnostic request task updates to Close. The potentially exposed users from the data source are added to the corresponding related list on the Diagnostic Request form.

**Parent Topic:**[Identify potentially exposed users](use-emergency-exposure-mgnt.md)

## Fetch potentially exposed user data from Cisco DNA Spaces

Fetch potentially exposed user information from the Cisco Wi-Fi access log data and populate the corresponding related lists on the Diagnostic Request form.

### Before you begin

Role required: sn\_imt\_diagnosis.diagnostics\_admin or admin

### Procedure

1.  Access the potentially exposed user information through an attachment having the Cisco Wi-Fi access log data or by generating a report through the Cisco DNA Spaces portal.

<table id="choicetable_gsw_cnz_qmb"><thead><tr><th align="left" id="d365979e181">

Options

</th><th align="left" id="d365979e184">

Steps

</th></tr></thead><tbody><tr><td id="d365979e190">

**Attach a Wi-Fi access log file**

</td><td>

1.  Click the manage attachments icon \(![Manage attachments icon](../image/icon-manage-attachments.png)\).
2.  In the Attachments window, click **Choose file** and select a Wi-Fi access log file.
3.  Select **Closed** in the State list.
4.  Click **Update**.
 The state of the diagnostic request task updates to Close.

</td></tr><tr><td id="d365979e232">

**Generate a report and post data through the Cisco portal**

</td><td>

1.  Log in to the Cisco DNA Spaces portal.
2.  On the Proximity Reporting page, click **Create Report**.
3.  Enter the start and end date for the report period.
4.  Select the **Auto-submit report data to ServiceNow task** check box.
5.  In the **Diagnostic Request Task \#** field, enter the number of the diagnostic request task.
6.  Click **Generate Report**.
 The Cisco system creates a proximity report and puts the Wi-Fi access log data from the report into the Wi-Fi Access Register \[sn\_imt\_tracing\_wifi\_access\_register\] table on the ServiceNow instance.

 The state of the diagnostic request task updates to Close.

</td></tr></tbody>
</table>
### Result

Cisco Wi-Fi access log data includes the proximity level of the users connected to the Cisco Wi-Fi network in the workplace. Based on the proximity level options set by the **sn\_imt\_tracing.wifi\_proximity\_preference** property \(within 30 feet of the router, on the same floor, or in the same building\), the potentially impacted users are identified from the Cisco Wi-Fi access logs. The information about these potentially exposed users populates the corresponding related list on the Diagnostic Request form.

## Fetch potentially exposed user data from Zebra MotionWorks proximity report

Upload a spreadsheet containing the Zebra MotionWorks proximity data to fetch a list of potentially exposed users and populate the corresponding related lists on the Diagnostic Request form.

### Before you begin

You must have downloaded the Microsoft Excel file from the Zebra MotionWorks Portal.

Role required: sn\_imt\_diagnosis.diagnostics\_admin or admin

### Procedure

1.  Click the manage attachments icon \(![Manage attachments icon](../image/icon-manage-attachments.png)\).

2.  In the Attachments window, click **Choose file** and select a Zebra MotionWorks proximity report spreadsheet.

3.  Select **Closed** in the State list.

4.  Click **Update**.


### Result

The Zebra MotionWorks proximity report contains a list of users equipped with handheld or wearable devices who were in close proximity to the affected user. The users who were inclose proximity for more than the permissible time with the affected user during the specified dates are identified from this proximity report. The information about these potentially exposed users populates the corresponding related list on the Diagnostic Request form.


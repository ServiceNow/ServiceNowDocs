---
title: Activate the add-in for Microsoft Outlook
description: Workplace Reservation Management administrators can activate the manifest add-in for Microsoft Outlook. Add a manifest add-in file and customize it as per your requirements.
locale: en-US
release: australia
product: Workplace Reservation Management
classification: workplace-reservation-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Manage Workplace Reservations for Microsoft Outlook Add-in, Workplace Reservation Management, Workplace Service Delivery, Employee Service Management]
---

# Activate the add-in for Microsoft Outlook

Workplace Reservation Management administrators can activate the manifest add-in for Microsoft Outlook. Add a manifest add-in file and customize it as per your requirements.

## Before you begin

Download the sample manifest file **Workplace\_Outlook\_add\_in\_manifest\_example.xml**. Navigate to ServiceNow® Store Workplace Reservation Management version 3.0.2. From the Links and Documents page, download the **Workplace\_Outlook\_add\_in\_manifest\_example.xml** manifest file.

**Note:** If you are using Microsoft Outlook Add-in 1.12.2 version or earlier, update to Workplace Reservation Management 3.0.2. After installing and configuring Workplace Reservation Management 3.0.2, upload a new manifest file. Employees can create an event or a meeting invite in Outlook Calendar and make reservations using the manifest add-in file.

Role required: admin

## Procedure

1.  Navigate to where you have downloaded the sample manifest add-in file for Microsoft Outlook.

2.  Open the sample manifest add-in file and make customizations as per your organizational requirements.

    In the sample manifest file, change the following parameters as required.

<table id="table_att_35f_ghc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Id

</td><td>

Unique ID for the add-in

</td></tr><tr><td>

DisplayName

</td><td>

Display name of the add-in. The name is displayed in the Microsoft Outlook app ribbon.

</td></tr><tr><td>

Description

</td><td>

Description about the add-in.

</td></tr><tr><td>

IconUrl

</td><td>

Link to the icon image. The icon is installed along with the application for the add-in. If you are setting your own icon, ensure that you specify a navigation \(URL\) link to the icon. The following icon formats are supported:-   16x16
-   32x32
-   64x64
-   80x80


</td></tr><tr><td>

Images

</td><td>

Link to the images used in the add-in, if any.

</td></tr><tr><td>

SupportUrl

</td><td>

Link to a supporting environment.

</td></tr><tr><td>

SourceLocation

</td><td>

Link to a supporting environment. You can link your own environment, or a different website.

</td></tr><tr><td>

URL

</td><td>

Link to the instance where the add-in is installed.

</td></tr></tbody>
</table>3.  Save the manifest file with a different name.

    The manifest file for the add-in is created. Employees can now make reservations in Workplace Reservation Management using the add-in file. For more information, see [Create a reservation in Microsoft Outlook add-in](outlook-create-rsv.md).



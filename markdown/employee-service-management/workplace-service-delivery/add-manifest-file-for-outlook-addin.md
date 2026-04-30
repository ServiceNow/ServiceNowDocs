---
title: Create a manifest file for Microsoft Outlook Add-in
description: Create a manifest file and customize it as per your organization standards to configure the add-in in Microsoft Outlook.
locale: en-US
release: yokohama
product: Workplace Service Delivery
classification: workplace-service-delivery
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Configure, Workplace Reservations for Microsoft Outlook Add-in, Workplace Service Delivery, Employee Service Management]
---

# Create a manifest file for Microsoft Outlook Add-in

Create a manifest file and customize it as per your organization standards to configure the add-in in Microsoft Outlook.

## Before you begin

Role required: none

Download the sample manifest file **Workplace\_Outlook\_add\_in\_manifest\_example.xml** along with the Workplace Reservations for Microsoft Outlook Add-in application from the ServiceNow Store. You can also create a manifest file, for more information on how to create a manifest file, refer to the [Microsoft documentation](https://docs.microsoft.com/en-us/office/dev/add-ins/develop/add-in-manifests?tabs=tabid-1#manifest-v11-xml-file-examples-and-schemas).

## About this task

In this task, you can create a manifest file by customizing the sample manifest file downloaded from the ServiceNow Store. The parameters in the manifest file that can be customized are explained in the procedure.

## Procedure

1.  Navigate to the directory where you have downloaded the sample manifest file.

2.  Open the manifest file to make customization.

3.  In the sample manifest file, change the following parameters as per your organization requirements.

<table id="table_nx4_j1d_cqb"><thead><tr><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Id

</td><td>

Unique ID for the add-in. For more ore information, refer to the [Microsoft documentation](https://docs.microsoft.com/en-us/office/dev/add-ins/testing/troubleshoot-manifest).

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

Link to the icon image. A Youmoji icon is installed along with the application for the add-in. If you are setting your own icon, ensure that you specify a url linking to the icon. The following icon formats are supported:-   16x16
-   32x32
-   64x64
-   80x80


</td></tr><tr><td>

Images

</td><td>

Link to the images used in the add-in.

</td></tr><tr><td>

SupportUrl

</td><td>

Link to a supporting environment.

</td></tr><tr><td>

SourceLocation

</td><td>

Link to a supporting environment. You can link your own environment, or a different website.

</td></tr><tr><td>

Url

</td><td>

Link to the instance where the add-in is installed.

</td></tr></tbody>
</table>4.  Save the manifest file with a different name.


## Result

The manifest file for the add-in is created.

## What to do next

Perform any of the following actions as per requirement:

-   [Upload the manifest file for a single user](upload-manifest-for-single-user.md)
-   [Upload the manifest file in Microsoft Office 365](upload-the-manifest-file-office365.md)

**Parent Topic:**[Configure Workplace Reservations for Microsoft Outlook Add-in](../concept/configure-workplace-rsv-for-outlook-addin.md)

**Related topics**  


[Install Workplace Reservations for Microsoft Outlook Add-in](install-workplace-reservations-for-outlook-addin.md)

[Upload the manifest file for a single user](upload-manifest-for-single-user.md)

[Upload the manifest file in Microsoft Office 365](upload-the-manifest-file-office365.md)


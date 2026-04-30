---
title: Upload the manifest file in Microsoft Office 365
description: After you create a manifest file, upload it to Microsoft Office 365. You can view and use the add-in Microsoft Office 365 after you upload the manifest file.
locale: en-US
release: yokohama
product: Workplace Service Delivery
classification: workplace-service-delivery
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Configure, Workplace Reservations for Microsoft Outlook Add-in, Workplace Service Delivery, Employee Service Management]
---

# Upload the manifest file in Microsoft Office 365

After you create a manifest file, upload it to Microsoft Office 365. You can view and use the add-in Microsoft Office 365 after you upload the manifest file.

## Before you begin

**Important:** The Workplace Reservations for Microsoft Outlook Add-in application does not support Microsoft Exchange On-Premises.

Role required: sn\_wsd\_msaddin.admin

## Procedure

1.  Log in to the Microsoft Office 365 with your admin account.

2.  Select the app launcher icon in the upper-left and click **Admin**.

3.  In the admin center, go to **Settings** &gt; **Integrated apps**.

4.  Select **Deployed apps** and select **Upload custom apps**.

5.  Select **App type** as **Office Add-in**.

6.  Select **Upload manifest file \(.xml\) file from device** option.

7.  Click **Choose File** to select the manifest file that you have created for the add-in.

8.  Click **Next**.

9.  In the Assign users section, select one of the following options to specify whom to deploy the add-in.

    -   **Entire organization**: Select this option to deploy the add-in to everyone.
    -   **Specific users/groups**: Select this option to deploy the add-in to only selected users or user groups. Use the search option to find users or groups to whom you want to deploy the add-in.
    -   **Just me**: Select this option to deploy the add-in only to you.
10. Click **Next**.

11. In the Deployment method section, review app permissions and selected settings.

12. Click **Finish deployment.**.

    A green tick appears when the add-in deployment is successful. Follow the instructions provided on the page to test if the add-in deployment is successful.

13. On the final page, click **Cancel** to close the dialog box.


## Result

The add-in is uploaded to Microsoft Office 365. The users to whom the add-in is deployed can view the add-in option while scheduling a meeting.

**Parent Topic:**[Configure Workplace Reservations for Microsoft Outlook Add-in](../concept/configure-workplace-rsv-for-outlook-addin.md)

**Related topics**  


[Install Workplace Reservations for Microsoft Outlook Add-in](install-workplace-reservations-for-outlook-addin.md)

[Create a manifest file for Microsoft Outlook Add-in](add-manifest-file-for-outlook-addin.md)

[Upload the manifest file for a single user](upload-manifest-for-single-user.md)


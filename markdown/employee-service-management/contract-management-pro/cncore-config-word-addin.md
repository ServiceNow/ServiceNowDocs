---
title: Configure the Microsoft Word add-in for ServiceNow Contracts
description: As an admin, configure the Microsoft Word add-in for ServiceNow Contracts.
locale: en-US
release: australia
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [Word add-in, Microsoft Word add-in, Add-ins for ServiceNow contracts, Add-ins for Contract Management]
breadcrumb: [Configure, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
---

# Configure the Microsoft Word add-in for ServiceNow Contracts

As an admin, configure the Microsoft Word add-in for ServiceNow Contracts.

## About this task

Microsoft Word add-in for ServiceNow Contracts will be installed when you install Contract Management Pro. You need to configure it to be available in the Microsoft Word as an add-in.

The following video walks you through the process of configuring Microsoft Word add-in for ServiceNow Contracts on macOS.Video explaining the steps to configure Microsoft Word add-in for ServiceNow Contracts on macOS. 

## Before you begin

Ensure that the Global application for the Content-Security-Policy response header is inactive and the Microsoft Word Add-in for ServiceNow Contracts application is active. For more information, see [Configure HTTP response headers](https://www.servicenow.com/docs/access?context=configure-http-response-header&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **ServiceNow Add-Ins for Office** &gt; **Office Add-In Manifests**.

2.  From the Office Manifests list, select **ServiceNow Contracts**.

    ![Microsoft Word add-in for Contract Management Pro.](../image/cmpro-office-add-in.png "Manifest file for ServiceNow Contracts")

3.  If your ServiceNow instance is configured with single sign-on \(SSO\) login, clear the **Login Page not Required** check box, right-click the form header, and then select **Save**.

4.  Select **Download Manifest** to download the file.

    ![Download Microsoft Word add-in manifest file.](../image/cmpro-manifest-file.png "Download manifest file")

5.  If your ServiceNow instance is configured with single sign-on \(SSO\) login, update the manifest file.

    1.  Open the manifest file.

    2.  Locate the `AppDomains` element.

    3.  Add a `AppDomain` element and enter the SSO host URL inside it.

        Example

        ```
        <AppDomains>
        <AppDomain><Instance URl></AppDomain>
        <AppDomain><SSO Host URl></AppDomain> <!-- Enter the host URL only, e.g., www.<sso provider>.com -->
        </AppDomains>
        ```

    4.  Save the manifest file.

6.  Configure the add-in.

<table id="choicetable_qfz_dkb_yyb"><thead><tr><th align="left" id="d579943e278">

System

</th><th align="left" id="d579943e281">

Steps

</th></tr></thead><tbody><tr><td id="d579943e287">

**macOS**

</td><td>

1.  Copy the manifest file to the `/Users/<user-id>/Library/Containers/com.microsoft.Word/Data/Documents/wef` directory.
2.  Open Microsoft Word.
3.  Open a document where you want to mark the content controls.
4.  Navigate to **Insert** &gt; **My Add-ins**.
5.  Select **ServiceNow Contracts**.
6.  Navigate to the menu **Home**.
 **Note:** To connect to multiple instances using the Microsoft Word add-in, add the corresponding manifest files to the `wef` folder in your system and ensure that each manifest file contains a unique ID.

</td></tr><tr><td id="d579943e352">

**Windows**

</td><td>

1.  Publish the manifest file. For more information, see [Office Add-ins with the unified app manifest for Microsoft 365](https://learn.microsoft.com/en-us/office/dev/add-ins/testing/create-a-network-shared-folder-catalog-for-task-pane-and-content-add-ins) from the Microsoft Office 365.

**Note:** Ensure you have completed the step for publishing the manifest file before proceeding with the next steps.

2.  Open Microsoft Word.
3.  Open a document where you want to mark the content controls
4.  Navigate to the menu **Insert** &gt; **My Add-ins**.
5.  Select **ServiceNow Contracts** to add the add-in.
6.  Navigate to the **Home** menu.


</td></tr><tr><td id="d579943e411">

**Microsoft Word Online**

</td><td>

1.  Open Microsoft Word online.
2.  In the Home ribbon, select **Add-ins** &gt; **More Add-ins**.

The add-ins are displayed.

3.  Navigate to **ADMIN MANAGED**.
4.  Select **Upload My Add-in**.
5.  In the Upload Add-in pop-up, browse and select the manifest file.
6.  Select **Upload**.

The Upload confirmation screen appears.

</td></tr></tbody>
</table>
## Result

The **ServiceNow Contracts** add-in is available on the Home ribbon. When you log in with ServiceNow instance credentials, the templates available in the ServiceNow instance appears in the add-in screen.

## What to do next

[Creating a contract template using Microsoft Word add-in for ServiceNow Contracts](../concept/cncore-setup-ct-add-in.md)


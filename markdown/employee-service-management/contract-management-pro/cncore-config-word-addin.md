---
title: Configure the Microsoft Word add-in for ServiceNow Contracts
description: As an admin, configure the Microsoft Word add-in for ServiceNow Contracts.
locale: en-US
release: xanadu
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Configure Contract Management Pro, Contract Management Pro, Employee Service Management]
---

# Configure the Microsoft Word add-in for ServiceNow Contracts

As an admin, configure the Microsoft Word add-in for ServiceNow Contracts.

## Before you begin

Ensure that the Global application for the Content-Security-Policy response header is inactive and the Microsoft Word Add-in for ServiceNow Contracts application is active. For more information, see [Configure HTTP response headers](https://www.servicenow.com/docs/access?context=configure-http-response-header&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).

Role required: admin

## About this task

Microsoft Word add-in for ServiceNow Contracts will be installed when you install Contract Management Pro. You need to configure it to be available in the Microsoft Word as an add-in.

## Procedure

1.  Navigate to **All** &gt; **ServiceNow Add-Ins for Office** &gt; **Office Add-In Manifests**.

2.  From the Office Manifests list, select **ServiceNow Contracts**.

3.  If your ServiceNow instance is configured with single sign-on \(SSO\) login, clear the **Login Page not Required** check box, right-click the form header, and then select **Save**.

4.  Select **Download Manifest** to download the file.

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

<table id="choicetable_qfz_dkb_yyb"><thead><tr><th align="left" id="d514143e190">

System

</th><th align="left" id="d514143e193">

Steps

</th></tr></thead><tbody><tr><td id="d514143e199">

**macOS**

</td><td>

1.  Copy the manifest file to the `/Users/<user-id>/Library/Containers/com.microsoft.Word/Data/Documents/wef` directory.
2.  Open Microsoft Word.
3.  Open a document where you want to mark the content controls.
4.  Navigate to **Insert** &gt; **My Add-ins**.
5.  Select **ServiceNow Contracts**.
6.  Navigate to the menu **Home**.


</td></tr><tr><td id="d514143e252">

**Windows**

</td><td>

1.  Publish the manifest file. For more information, see [Office Add-ins with the unified app manifest for Microsoft 365](https://learn.microsoft.com/en-us/office/dev/add-ins/testing/create-a-network-shared-folder-catalog-for-task-pane-and-content-add-ins) from the Microsoft Office 365.
2.  Open Microsoft Word.
3.  Open a document where you want to mark the content controls
4.  Navigate to the menu **Insert** &gt; **My Add-ins**.
5.  Select **ServiceNow Contracts** to add the add-in.
6.  Navigate to the **Home** menu.


</td></tr><tr><td id="d514143e309">

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

The **ServiceNow Contracts** add-in is available in the Home ribbon.

**Parent Topic:**[Configure Contract Management Pro](../concept/cncore-config-cmpro.md)

**Related topics**  


[Install Contract Management Pro](cncore-install-cmpro.md)

[Set up Contracts Core](../concept/cncore-setup-cmpro.md)

[Configure contract templates for a contract request](../concept/cncore-document-templates.md)

[Configure document templates for standard letters or documents](cncore-wdt-other-bu.md)

[Add and configure contract request functionality](../concept/cncore-uptake-steps.md)

[Configuring Contract Workspace with UI Builder components](../concept/cncore-conf-cntrct-wrkspc.md)

[Configure Obligation Management notifications](cncore-config-ob-mgmt-notf.md)


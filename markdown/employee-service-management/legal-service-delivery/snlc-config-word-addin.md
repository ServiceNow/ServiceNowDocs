---
title: Configure the Microsoft Word add-in for ServiceNow Contracts
description: As an admin, configure the Microsoft Word add-in for ServiceNow Contracts.
locale: en-US
release: zurich
product: Legal Service Delivery
classification: legal-service-delivery
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Install Microsoft Word add-in for ServiceNow Contracts, Configure, Contract Management Pro for Legal Service Delivery, Integration with ServiceNow applications, Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Configure the Microsoft Word add-in for ServiceNow Contracts

As an admin, configure the Microsoft Word add-in for ServiceNow Contracts.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **ServiceNow Add-Ins for Office** &gt; **Office Add-In Manifests**.

2.  From the Office Manifests list, select **ServiceNow Contracts**.

3.  Select **Download Manifest** to download the file.

4.  Configure the add-in.

<table id="choicetable_qfz_dkb_yyb"><thead><tr><th align="left" id="d315802e100">

System

</th><th align="left" id="d315802e103">

Steps

</th></tr></thead><tbody><tr><td id="d315802e109">

**macOS**

</td><td>

1.  Copy the manifest file to the `/Users/<user-id>/Library/Containers/com.microsoft.Word/Data/Documents/wef` directory.
2.  Open Microsoft Word.
3.  Open a document where you want to mark the content controls.
4.  Navigate to **Insert** &gt; **My Add-ins**.
5.  Select **ServiceNow Contracts**.
6.  Navigate to the menu **Home**.


</td></tr><tr><td id="d315802e162">

**Windows**

</td><td>

1.  Publish the manifest file. For more information, see [Office Add-ins with the unified app manifest for Microsoft 365](https://learn.microsoft.com/en-us/office/dev/add-ins/testing/create-a-network-shared-folder-catalog-for-task-pane-and-content-add-ins)from the Microsoft Office 365.
2.  Open Microsoft Word.
3.  Open a document where you want to mark the content controls
4.  Navigate to the menu **Insert** &gt; **My Add-ins**.
5.  Select **ServiceNow Contracts** to add the add-in.
6.  Navigate to the **Home** menu.


</td></tr><tr><td id="d315802e219">

**Microsoft Word Online**

</td><td>

1.  Open Microsoft Word online.
2.  Select **File** &gt; **Get Add-ins**. The add-ins are listed.
3.  Select **More Add-ins**. The office Add-ins are listed.
4.  Navigate to **ADMIN MANAGED**.
5.  Select **Upload My Add-in**.
6.  In the Upload Add-in pop-up, browse and select the manifest file.
7.  Select **Upload**. The Upload confirmation screen is displayed.


</td></tr></tbody>
</table>
## Result

The **ServiceNow Contracts** add-in is available in the Home ribbon.

**Parent Topic:**[Install Microsoft Word add-in for ServiceNow Contracts](snlc-install-word-addin.md)


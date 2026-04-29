---
title: Mobile barcode scanning
description: Use the camera on your mobile device to scan barcodes into your instance using mobile applications.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Before implementation, Configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Mobile barcode scanning

Use the camera on your mobile device to scan barcodes into your instance using mobile applications.

## Multi-scan barcode scanning

To scan barcodes as accurately as possible, make sure that you:

-   Scan in a well-lit environment. Both Android and iOS mobile devices have flashlight apps that you can use to make sure your device's camera has adequate light to scan barcodes accurately.
-   Keep the device camera in a steady position while scanning. If the camera is shaking, barcode scans will become blurred and inaccurate.

<table id="table_hcp_y52_tlb"><tbody><tr><td>

Use multi-scan to scan multiple barcodes sequentially without leaving the scanning interface. Enter information for your assets faster than manual entry or individual scans. After scanning in multiple barcodes, end users can review a list of their scanned items.

</td><td>

![Multi-scan interface](../image/group-scan.png)

</td></tr></tbody>
</table>## Grouped barcode scanning

<table id="table_kr1_z52_tlb"><tbody><tr><td>

Use grouped barcode scanning to scan multiple barcodes and group them into a set. For example, a single item that has an asset number, serial number, and model number. You can configure a button to use grouped entries to accept multiple barcode scans.

</td><td>

![Group scan interface](../image/multiscan.png)

</td></tr></tbody>
</table>## Supported barcode types

The ServiceNow mobile apps for iOS and Android support scanning the following barcode types:

**Note:**

-   Code-128 and Code-39 barcode scanning isn’t consistent on Android devices due to a [known open issue with Android libraries](https://issuetracker.google.com/u/0/issues/207732702). Incorrect scanned values might be intermittently returned. For more accurate barcode scanning, see [Enable enhanced barcode scanning](../task/enable-enhanced-barcode-scan.md).
-   Starting with version 18.3 of ServiceNow iOS apps, the barcode scanner uses a new framework that improves its reliability, ease of use, and enables scanning a wider variety of barcode types. However, the new barcode scanner framework isn't compatible with some older iOS devices. See [KB1702599](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1702599) on the ServiceNow Support website for details. You must be logged in to the website to view this content.

-   1D barcodes:
    -   Both iOS and Android: EAN-13, EAN-8, UPC-A, UPC-E, Code-39, Code-93, Code-128, ITF, Codabar
    -   iOS only: Code 39 Full ASCII, Code 93i, GS1 DataBar, GS1 DataBar Expanded, GS1 DataBar Limited, MSI
-   2D barcodes:
    -   Both iOS and Android: QR Code, Data Matrix, PDF-417, AZTEC
    -   iOS only: MicroPDF417, MicroQR

## Zebra scanning devices

The Android version of ServiceNow mobile apps can be used with most Zebra scanning devices. The scanner only works when permissions for the Zebra device camera have been denied for the ServiceNow mobile app. If you have already granted permissions to the Zebra device camera, you can turn them off in the settings for the Zebra device. In the ServiceNow app, when the cursor is in a QR/Barcode input field, the scanner outputs the results. End users can modify the barcode output to include a return/enter string at the end of each scan with other apps, such as DataWedge.

For more information, see [Enable barcode scanning with an external scanner](../task/enable-external-barcode-scanner.md). Also refer to [Add a Tab Key after Scanning a Barcode](https://supportcommunity.zebra.com/s/article/Add-a-Tab-Key-After-Scanning-a-Bar-Code?language=en_US) in the Zebra documentation. This article explains how to add a tab key which automatically moves the scanner cursor when scanning multiple barcodes.

-   **[Multi-scan for mobile applications](sg-multi-scan.md)**  
Use multi-scan to quickly scan multiple barcodes or groups of codes. With multi-scan, you can input information for your assets faster than manual entry or individual scans.
-   **[Configure a grouped input for multiple scans](../task/sg-configure-multiscan.md)**  
Enable your users to scan several barcodes sequentially. Users can scan barcodes without leaving the scanning interface when you configure a grouped input. You can configure grouped inputs on buttons to accept multiple barcode scans.

**Parent Topic:**[Considerations before implementation](imp-considerations.md)


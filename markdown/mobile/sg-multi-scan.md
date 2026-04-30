---
title: Multi-scan for mobile applications
description: Use multi-scan to quickly scan multiple barcodes or groups of codes. With multi-scan, you can input information for your assets faster than manual entry or individual scans.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Mobile barcode scanning, Considerations before implementation, ServiceNow Mobile Platform configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Multi-scan for mobile applications

Use multi-scan to quickly scan multiple barcodes or groups of codes. With multi-scan, you can input information for your assets faster than manual entry or individual scans.

Use the scan screen to scan items into your instance by using your mobile device.

## Scan screen

<table id="table_ecx_ml3_5jb"><tbody><tr><td>

![Mobile scan screen.](../image/mobile-scan-screen.png)

</td><td>

Use the scan screen to scan in your barcode items. You see this screen when you access a function that your administrator configured for barcode scanning.

 Mobile scan features

 -   Close \(1\): Tap **Close** to leave the scan screen.
-   Disable camera \(2\): Tap **Disable camera** to disable the camera on your mobile device. This button is available only on Android. Disable your camera to scan using a non-phone scanner.
-   Enable flashlight \(3\): Tap **Enable flashlight** to enable the flashlight feature on your mobile device.
-   Scan crosshair \(4\): Center a barcode to be scanned using the cross-hair icon in the center of the screen.
-   Last Scan \(5\): See the last three entries that you scanned. Press the **Rescan** \(![Rescan button](../image/mobile-rescan.png)\) button to discard the scanned values.
-   Inputs \(6\): See the UI parameters that are used in the scanned input. Scanning a barcode adds a value to the top parameter. Further scans add values to the next parameters in the display order. You can tap any entry to manually enter a value.
-   Scan next item \(7\): Tap **Scan next item** to accept the current scanned values and continue to a new item. If all fields in the Inputs \(6\) section have values, the scan screen automatically continues to the next item. If there are any mandatory fields without values, you can't tap **Scan next item**.
-   Review \(8\): Tap the review button to review your scanned items. See the next section for details on the review screen.

</td></tr></tbody>
</table>## Review screen

<table id="table_h4r_2s3_5jb"><tbody><tr><td>

![Scan review screen.](../image/scan-preview-screen.png)

</td><td>

After scanning your items, use the review screen to review, delete, and submit scanned items.

 Mobile review screen features

 -   Submit \(1\): Tap **Submit** to save your scanned items.
-   Scanned items \(2\): See your scanned items in this section. Each item displays the UI parameter name and its scanned value.
-   Delete item \(3\): Tap the **delete** icon \(![Delete item icon](../image/delete-scan-item.png)\) next to a scanned item to remove that item.

</td></tr></tbody>
</table>**Parent Topic:**[Mobile barcode scanning](sg-mobile-scanning.md)


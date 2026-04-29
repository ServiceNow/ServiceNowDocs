---
title: Adding an asset
description: Manually add an asset to the Discovery Console for OT.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Assets page, Use the Console pages, Discovery Console for Operational Technology \(OT\), Operational Technology Native Discovery components, Operational Technology Discovery, Operational Technology]
---

# Adding an asset

Manually add an asset to the Discovery Console for OT.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to the **Assets** page.

2.  Select the add icon ![](../../msi-console/image/add-icon-msi.jpg).

3.  In the Create Asset page, fill in the following sections.

    -   **Identification**: If applicable, add the following information:
        -   **IP Address**: Required.
        -   Hostname
        -   Product
        -   Firmware Version
        -   Network Zone
        -   MAC Address
        -   Serial Number
        -   **Ignore from Auto Query**: Slide toggle to set to Ignore.
    -   **Classification**: If applicable, add the following information:
        -   **Category**: Required. Provides a pop-up list to choose from.
        -   **Brand**: Required. Provides a pop-up list to choose from.
        -   **Purdue Level**: Optional. Provides a pop-up list to choose from.
        -   **Operating System**: Required. Provides a pop-up list to choose from.
        -   **Details**: Optional.
    -   **Metadata**: If applicable, add the following information:
        -   Alias
        -   Description
        -   Labels
        -   Location
    -   **Installed Software**: If applicable, select the Add Software button and select the software you want to include.
    -   **Attributes**: If applicable, select the Add Attribute button and select the Attributes you want to include.
    -   **Comments**: If applicable, add comments.
4.  Select **Create Asset** to create an asset or select **Cancel** to discard your entries.

5.  To import assets through a CSV upload, complete the following actions.

    1.  Select the **Actions** button.

        ![Actions drop-down menu](../../msi-console/image/asset-page-action-drop-down.png)

    2.  Select **Import Assets**.

    3.  Choose the CSV file that you want to import.

    4.  Select **Import**.

        **Note:** You can select assets to ignore during a scan. Select an asset and then, when activated, select **Ignore Assets** from the drop-down **Action** menu. The image shows the **Ignore Assets** selection as deactivated \(grayed out\).


## Result

The asset is created and added to the Assets page.


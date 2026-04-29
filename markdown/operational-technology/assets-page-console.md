---
title: Assets page
description: The Assets page shows a list of all available assets for the Discovery Console for OT.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-30"
reading_time_minutes: 5
breadcrumb: [Use the Console pages, Discovery Console for Operational Technology \(OT\), Operational Technology Native Discovery components, Operational Technology Discovery, Operational Technology]
---

# Assets page

The Assets page shows a list of all available assets for the Discovery Console for OT.

**Note:** To edit any of the fields in the Asset record, select the asset from the list and then select the Edit button. After editing, select Save to save any changes.

## Assets page overview

The Assets page shows all assets that were automatically discovered along with all assets that were manually added to the system. To view the assets list, use the navigational menu on the left side of the screen and select **Assets &gt; Assets**.

![Assets page](../../msi-console/image/asset-page.png)

You can add assets with the following methods.

-   Sensors and Collectors perform Native discovery and populate the assets.
-   Import via a CSV with assets information.
-   By selecting the add icon ![](../../msi-console/image/add-icon-msi.jpg).

**Filter panel**

When you open the Assets page, there is a Filter panel you can use to filter which Assets appear in the list. There are preset filters which appear as tabs at the bottom of the panel. The preset filters are:

-   Sites
-   Presets \(You can also check the Default Tab box above these 3 tabs.\)
-   Filters

Click the X at the top of the panel to close the filter. To open the panel, click the filter icon ![](../images/filter-icon.png).

Views

In the top right area above the Assets list, there are different icons that control how the Assets are viewed.

![Asset views](../../msi-console/image/3-asset-views.png)

The views are:

-   List view
-   Gallery view
-   Map view

**Actions**

The **Actions** button provides a drop-down menu for manipulating the Assets. The formats for each are indicated next to the selection where applicable. The selectable actions are:

-   Import Assets
-   Import Ignore Assets \(CSV\)
-   Export Ignore Assets \(CSV\)
-   Export Assets \(JSON\)
-   Export Assets \(CSV\)
-   Update Manufacturer Data
-   Update Vulnerability Data
-   Update Product Mappings
-   Update Purdue Levels
-   Ignore Assets
-   Delete Assets

**Note:** If an action is inactive, it appears grayed out in the menu.

Next to the **Actions** button is the add icon ![](../../msi-console/image/add-icon-msi.jpg).

## Asset records

With an Asset record, you can view and edit the details of the selected asset. To view an asset record from the Assets page, select the IP address displayed for the asset. The following sections describe each section of an Asset record.

**Note:** When you select the add icon ![](../../msi-console/image/add-icon-msi.jpg), this same view opens with these same sections. However, when you open an existing asset record, you have three tabs on the upper right side of the screen. The tabs are **Details**, **Images**, and **Modules**.

**Identification**

The Identification section contains the following fields.

<table id="table_rjn_xfb_42c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

IP Address \[Required\]

</td><td>

IP Address assigned to the asset.

</td></tr><tr><td>

Hostname

</td><td>

Name of the connected device.**Note:** The name is populated when it is configured on the device or if the DNS server is configured.

</td></tr><tr><td>

Product

</td><td>

Manufacturer and model of the asset.

</td></tr><tr><td>

Firmware Version

</td><td>

Version of the firmware installed.

</td></tr><tr><td>

Network Zone

</td><td>

Network zone of the asset.

</td></tr><tr><td>

MAC Address

</td><td>

MAC address that is associated with a given asset.

</td></tr><tr><td>

Serial Number

</td><td>

Serial number associated to the asset.

</td></tr><tr><td>

Ignore from Auto Query

</td><td>

Option to mark devices that need to be ignored from the auto queries. This field is automatically set to inactive,

</td></tr></tbody>
</table>**Classification**

The Classification section contains the following fields.

<table id="table_t4p_wxb_42c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Auto Categorization

</td><td>

Feature that enables the Discovery Console for OT to manage and update the **Description**, **Category**, and **Operating System** fields through the automatic classification system.

 Set to Yes or No.

 **Note:** If **Auto Categorization** has been enabled, then editing is turned off for the **Category**, **Brand**, **Operating System**, and **Details** fields.

Users can select Edit and then modify the values during editing.

To delete an asset, set **Auto Categorization** to **No**. The **Delete** button then appears in the right-most column allowing you to delete the asset.

</td></tr><tr><td>

Category

</td><td>

Category or classification indicates the function of the device or class that the asset belongs to. For example, Desktop, HMI, PLC, or SCADA.

</td></tr><tr><td>

Brand

</td><td>

Name of the manufacturer that produced the asset.

</td></tr><tr><td>

Purdue Level

</td><td>

N/A by default. See image of drop-down choices.

</td></tr><tr><td>

Operating System

</td><td>

Operating system of the asset. For example, IOS, Linux, or Windows.

</td></tr><tr><td>

Details

</td><td>

Section for additional details to describe the classification for this asset.

</td></tr></tbody>
</table>**Timeline**

The Timeline section contains the following dates and times related to the asset.

|Field|Description|
|-----|-----------|
|Created|When the asset was created.|
|Modified|The last time the asset was modified.|
|Last Seen|The last time the asset was detected.|
|Updated|The last time the asset was updated.|

**Open Ports**

The Open Ports section lists all open ports available on the asset that were identified by Discovery and shown on the Discovery Console for OT.

**Metadata**

The Metadata section contains the following fields.

<table id="table_hyq_mxb_42c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Alias

</td><td>

Alternate name given to the asset. Where possible, the alias is displayed instead of the IP Address or MAC address to provide a user-friendly way to identify the asset.

</td></tr><tr><td>

Description

</td><td>

Description of the asset.

</td></tr><tr><td>

Labels

</td><td>

Tag that you can add to an asset to assist in identifying and finding assets with the tagged properties within the system.

</td></tr><tr><td>

Location

</td><td>

Description of the physical location of the asset.

</td></tr></tbody>
</table>**Installed software**

The Installed Software section includes a list of all software installed on the asset. To add software, complete the following actions.

1.  Select the **Edit** button.

    ![Select the Edit button](../../msi-console/image/edit-button-msi-console.png)

2.  Scroll to the Installed Software section and select **Add Software**.

    ![Add Software](../../msi-console/image/add-software-msi-console.png)

3.  In the Add Software modal window, enter the **Vendor**, **Product**, and **Version** \(optional\) of the software being added.
4.  Select **Save**.

The added software displays in the Installed Software list.

**Attributes**

The Attributes section contains the attributes discovered by the Discovery process. To add an attribute, complete the following actions.

1.  Select the **Edit** button.
2.  Scroll to the Attributes section and select **Add Attribute**.

    ![Add attribute](../../msi-console/image/add-attr-msi-console.png)

3.  In the Attribute modal window, enter the **Name** and **Value** of the attribute.
4.  Select **Add Attribute**.
5.  Select **Save**.

**MAC Addresses**

The detected MAC Addresses section includes a list of all the MAC addresses that are associated with a given asset. The Real Address toggle is used to indicate that a MAC address belongs to an asset and should be considered the primary or main MAC address. Each detected MAC address in the list includes the **Vendor Name**, **Vendor Address**, **First Detected On**, and **Last Detected On** fields.

![MAC address](../images/vender-mac-address.png)

To add a MAC address, complete the following actions.

1.  Select the **Edit** button.
2.  Scroll down to the MAC Addresses section and select **Add MAC Address**.
3.  In the Add MAC Address modal window, add the name of the MAC Address.
4.  Select **Add Mac Address**.
5.  Select **Save**.

**Comments**

The Comments section provides an area to enter additional information about the assets. To add a Comment, complete the following actions.

1.  Select the **Edit** button.
2.  Scroll to the Comments section and select **Add Comment**.

    ![Add comment](../../msi-console/image/add-comment-msi-console.png)

3.  In the Add Comment modal window, enter a comment.
4.  Select **Save**.

The added comment is listed in the Comments section of the asset.


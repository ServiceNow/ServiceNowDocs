---
title: Hardware Asset Management licensing
description: Hardware Asset Management \(HAM\) licensing enables you to choose the Hardware Asset Management resource categories that you want to use. You can save money by paying only for those categories that you use, and not for categories that you don't use.
locale: en-US
release: australia
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
keywords: [HAM licensing, Hardware Asset Management licensing]
breadcrumb: [Hardware Asset Management subscription, Exploring Hardware Asset Management, Hardware Asset Management, IT Asset Management]
---

# Hardware Asset Management licensing

Hardware Asset Management \(HAM\) licensing enables you to choose the Hardware Asset Management resource categories that you want to use. You can save money by paying only for those categories that you use, and not for categories that you don't use.

Only the resource categories that are opted in are counted toward the Subscription Units.

**Note:** By default for a particular resource category, the normalization functions for its associated models and the asset actions for its associated assets don't work. If you want to use the normalization functions and asset actions, you have to opt in that resource category.

For more information about opting in or out of the HAM license resource categories, see [Opt-in or opt-out of HAM license resource categories](../task/optin-optout-ham-license-resource-categories.md).

Based on the usage of model categories, the ServiceNow HAM license is divided into resource categories. There are different types of resource categories. Different assets fall under different categories as well. Make sure you opt in the correct and required categories. An asset represented in the Asset \[alm\_asset\] table and which meets the criteria for each managed IT resource type such as Server, End User Computers, Network Gear, and Mobile Device, is counted toward a Subscription Unit based on the predefined ratio of number of assets to subscription units.

**Note:** Resource categories in HAM are associated with certain entitlements. For example, the Computer resource category is shown only if the computer entitlement is available in the HAM license. On an on-premise ServiceNow instance, the entitlements aren’t downloaded. However, you can store your HAM entitlement details by using the **sn\_ham\_active\_entitlements** system property. You can update this system property with a comma separated list of entitlements for which you have access.

The comma separated entitlements should be updated in the following format:

-   End User Computers- ham\_computer\_license
-   Mobile Device- ham\_mobiledevice\_license
-   Servers- ham\_server\_license
-   Network Gear- ham\_networkgear\_license
-   Monitors- ham\_monitor\_license
-   Storage- ham\_storage\_license
-   Printer- ham\_printer\_license
-   Telecom Network Inventory- ham\_tni\_license

<table id="table_uwf_fht_fvb"><thead><tr><th>

Resource category

</th><th>

Subscription unit ratio

</th><th>

Model category

</th></tr></thead><tbody><tr><td>

End User Computers

</td><td>

4:1

</td><td>

Computer

</td></tr><tr><td>

Servers

</td><td>

1:1

</td><td>

Any server such as the following:-   AIX Server
-   ESX Server
-   HPUX Server
-   Linux server
-   Netware Server
-   OS/X Server
-   Server
-   Solaris Server
-   Unix Server
-   Windows Server

</td></tr><tr><td>

Network Gear

</td><td>

5:1

</td><td>

-   Network gear
-   IP Switch
-   IP Router

</td></tr><tr><td>

Mobile Device

</td><td>

10:1

</td><td>

Mobile Device

</td></tr><tr><td>

Telecom Network Inventory

</td><td>

1:1

</td><td>

-   Card
-   Network Interface
-   Logical connection
-   Physical connection
-   Telco equipment

</td></tr><tr><td>

Unclassified hardware

</td><td>

1:1

</td><td>

Hardware

</td></tr><tr><td>

Monitors

</td><td>

15:1

</td><td>

Monitor

</td></tr><tr><td>

Storage

</td><td>

3:1

</td><td>

Storage Device

</td></tr><tr><td>

Printers

</td><td>

10:1

</td><td>

Printer

</td></tr></tbody>
</table>**Note:** Unclassified hardware, Monitors, Storage, and Printers are available with Hardware Asset Management version 10.1.0 and later only when you upgrade to HAM license version 5.0.

To access Hardware Asset Management features for Telecommunications Network Inventory, you should install the Telecommunications Network Inventory application and opt-in to the Telecom Network Inventory resource category. For more information, see Telecommunications Network Inventory integration with Hardware Asset Management.

## HAM Licensing for custom model categories

HAM provides some model categories out-of-the-box. Any model category that you create is considered as custom model category. When you upgrade to the Hardware Asset Management license released in Washington DC and later releases, any asset with a custom model category can access the Hardware Asset Management features and workflows only if any of the following conditions hold good:

-   The custom model category of the asset belongs to the hierarchy of opted-in model categories.
-   The parent model category of a custom model category is associated with a licensable and opted-in resource category.

**Note:** If you are on any HAM license version released before Hardware Asset Management license version 4, by default, the assets with custom model categories can access Hardware Asset Management features and workflows even if they aren't associated with an opted-in and licensable resource category. Also, the custom model categories aren't counted toward a Subscription Unit.

You can enable HAM licensing for custom model categories by using the **sn\_hamp.enable\_custom\_category\_licensing** system property. By default, the value of this system property is set to **false**. When you set the **sn\_hamp.enable\_custom\_category\_licensing** system property to **true**, custom model category assets are excluded from HAM workflows unless the parent of the custom model category is an opted-in and licensable category.

![Model category hierarchy](../image/ham-licensing-custom.png "Example for hierarchy of model categories")

In the example, the Computer model category is associated with the custom model categories Laptop and Tablet. Note the following about the custom model categories:

-   When you opt in Computers, both Laptop and Tablet are also counted toward a Subscription Unit under the End User Computers resource category. Also, these custom model categories can access Hardware Asset Management features and workflows.
-   When you opt out Computers, both Laptop and Tablet are also opted-out and these custom model categories can’t access Hardware Asset Management features and workflows.

**Note:** A model category that belongs to a licensable resource category and has a parent model category is licensed only under its associated resource category. For example, the Monitor model category that's associated with the licensable Monitors resource category and that has Computer as its parent, is licensed only under Monitors.

Assets with the following model categories are excluded from accessing Hardware Asset Management features and workflows:

-   Any model category that is a child of an opted-out resource category.
-   Any model category that is a child of model categories such as printer and storage device.This exclusion is only in Hardware Asset Management version 10.0.0.

    **Note:** In Hardware Asset Management version 10.0.0 and earlier, assets with model categories such as Printer, Consumables, and Storage Device retain access to Hardware Asset Management features without opting in a resource category.

    From Hardware Asset Management version 10.1.0 onward, the resource categories like Printers, Monitors, Storage, and Unclassified hardware are licensed and available only when you upgrade to HAM license version 5.0. You must opt in these resource categories to access the Hardware Asset Management features. When you opt in these resource categories, all their child model categories can also access the HAM features and workflows.

    After you upgrade to HAM license version 5.0, the printers, monitors, storage devices, and Unclassified hardware assets that were created in the earlier versions wouldn't be able to access the Hardware Asset Management features by default. You should explicitly opt in these resource categories.

-   Any other custom model category without a parent category.

**Parent Topic:**[Hardware Asset Management subscription](ham-subscription.md)

**Related topics**  


[Licensing framework for Hardware Asset Management solutions](licensing-ham-solutions.md)

[Hardware Asset Management license exclusion](ham-license-exclusion.md)


---
title: License upgrade and downgrade with the legacy Software Asset Management plugin
description: The concept of upgrading and downgrading licenses is built in to the legacy Software Asset Management \(com.snc.software\_asset\_management\) plugin.
locale: en-US
release: yokohama
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Software licenses in the legacy Software Asset Management plugin, Legacy Software Asset Management plugin, ITSM Software Asset Management, Asset Management, IT Service Management]
---

# License upgrade and downgrade with the legacy Software Asset Management plugin

The concept of upgrading and downgrading licenses is built in to the legacy Software Asset Management \(com.snc.software\_asset\_management\) plugin.

This is helpful when reconciling licenses. Downgrading a license is the process of purchasing a license, but using an earlier version. Upgrading a license occurs when a newer version of a license is not purchased, but you are allowed to use the newer version. Downgrading is more common than upgrading.

Any version defined as a downgrade child that does not have entitlements and a license can be counted as an installation of the upgrade parent. Use this method to avoid having to uninstall unlicensed versions of software running in your environment. When you define an unlicensed version as a downgrade child of a licensed version, the system creates a software model record for the unlicensed version with an upgrade path to the licensed version. If you delete the downgrade child from the licensed version's record, it is automatically deleted from the Software Model record for the unlicensed version.

**Note:** If the downgrade child has either a license or an entitlement, it must also have a counter, which counts all installations of the downgrade child against its own license.

For example, you have licenses for the software model Microsoft Word 2010, but no licenses or entitlements for Word 2007. Discovery finds installations of Word 2007 being used in your organization. Rather than force users to uninstall all instances of this unlicensed version, you decide to count installations of Word 2007 against your Word 2010 license. To do this, you configure Word 2007 as a downgrade child in the Word 2010 Software Model record. A Software Model record is automatically created for Word 2007 which specifies Word 2010 as the upgrade parent.

If a software version has a downgrade child or an upgrade version that can be counted against the parent, the number of installs counted is restricted to the number of available rights of the parent. For example, Microsoft Word 2010 has a downgrade to Word 2007. Both versions have an active counter. Microsoft Word 2010 finds all entitled copies of Word 2007, and also takes out of compliance any installs from that downgrade counter until the available downgrade rights are used. However, if Microsoft Word 2010 only has 100 rights, then the maximum number of rights to be taken from the downgrade counter is 100.

You can set the start and end dates for a software upgrade parent and downgrade child to be valid. The software counter counts the upgrade and downgrade licenses within the selected dates. If the software counter runs outside of the date range, the upgrade and downgrade licenses are not counted.

**Note:** If an upgrade parent or downgrade child is set on the software model, it applies to all licenses of that model. If set on the software license, it applies specifically to that license.

-   **[Upgrade a license using the legacy Software Asset Management plugin](../task/t_UpgradingALicense.md)**  
Use the legacy Software Asset Management \(com.snc.software\_asset\_management\) plugin to upgrade a software license through one of two methods: through a software license record or through a software model record.
-   **[Downgrade a license using the legacy Software Asset Management plugin](../task/t_DowngradingALicense.md)**  
Use the legacy Software Asset Management \(com.snc.software\_asset\_management\) plugin to downgrade a software license through one of two methods: through a software model record or through a software license record.

**Parent Topic:**[Software licenses in the legacy Software Asset Management plugin](c_SoftwareLicenses.md)


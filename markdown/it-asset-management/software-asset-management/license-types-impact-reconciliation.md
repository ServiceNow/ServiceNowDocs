---
title: Impact of different license types on software reconciliation
description: Each license type has entitlements and conditions outlined on the entitlement form, and more importantly, these license types have a significant impact on the Software Asset Management \(SAM\) reconciliation process.
locale: en-US
release: zurich
product: Software Asset Management
classification: software-asset-management
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 5
keywords: [license types, reconciliation, impact on reconciliation, entitlement, SAM reconciliation, software management]
breadcrumb: [References, Software Asset Management, IT Asset Management]
---

# Impact of different license types on software reconciliation

Each license type has entitlements and conditions outlined on the entitlement form, and more importantly, these license types have a significant impact on the Software Asset Management \(SAM\) reconciliation process.

<table id="table_mtr_hzy_bfc"><thead><tr><th>

License type

</th><th>

Description

</th><th>

Publisher applicability

</th><th>

Impact on licensing or reconciliation in SAM

</th></tr></thead><tbody><tr><td>

Perpetual

</td><td>

A one-time purchase license that enables indefinite use of the software without any ongoing or recurring payments.

</td><td>

All

</td><td>

This license grants indefinite use but doesn’t include maintenance rights, so benefits such as new version access, version upgrades, Bring your own license \(BYOL\) benefits, and technical support from the software publisher aren’t available. To receive maintenance/SA benefits, you must associate maintenance/SA entitlements with the Perpetual license.

</td></tr><tr><td>

Perpetual + Software Assurance

</td><td>

A perpetual license combined with Software Assurance \(SA\) from Microsoft offers a comprehensive Volume Licensing program with these benefits:-   New version rights: Upgrade eligible Microsoft product licenses to the latest version at no additional cost.
-   License mobility: Deploy certain server applications on-premises or in the cloud without additional licenses.
-   Unlimited virtualization: License the physical host for products such as Windows Server Datacenter Edition, enabling an unlimited number of virtual machines.
-   Virtual layer licensing: License individual virtual machines, reducing overall licensing costs.

</td><td>

Microsoft

</td><td>

Software Asset Management automatically applies the Software Assurance benefits. For more information, see [Software license maintenance](../concept/software-license-maintenance.md).

</td></tr><tr><td>

Subscription

</td><td>

For subscription-based products like Jira, Microsoft 365, and Adobe Creative Cloud, as well as non-subscription products using subscription licenses, such as Windows and SQL Server.

</td><td>

All \(subscription products\)

</td><td>

License compliance is primarily driven by user subscriptions pulled from the subscription portal, such as Jira and Microsoft 365. It also applies to non-subscription products like Windows Server and SQL Server, which can receive Software Assurance benefits.

</td></tr><tr><td>

Perpetual + Maintenance

</td><td>

Perpetual + Maintenance is similar to Perpetual + Software Assurance, but it includes a maintenance agreement that provides access to software updates, patches, and sometimes support for a specified duration. This license type applies to non-Microsoft publishers such as Oracle and VMware.

</td><td>

All

</td><td>

Software Asset Management automatically applies the Software maintenance benefits. For more information, see [Software license maintenance](../concept/software-license-maintenance.md).

</td></tr><tr><td>

Upgrade

</td><td>

A licensing option that enables upgrading from a lower-tier edition to a higher-tier edition, such as Standard to Enterprise, without purchasing a new full license.

</td><td>

All

</td><td>

You can upgrade a lower edition of software, such as SQL Server Standard, to a higher edition, such as SQL Server Enterprise. Use the **Upgraded Entitlements** tab in the Software Entitlement form to link related versions of your software under active maintenance and your upgrades. For more information, see [Software entitlement fields](software-entitlement-fields.md).

</td></tr><tr><td>

Software Assurance

</td><td>

Software assurance entitlement that provides Microsoft customers with software assurance benefits. However, it must be linked to a base perpetual license to activate the entitlements.

</td><td>

Microsoft

</td><td>

Software Asset Management doesn’t reconcile software assurance entitlements unless they’re linked to base perpetual licenses. Confirm that software assurance entitlements are related to base perpetual entitlements for correct reconciliation.

</td></tr><tr><td>

Maintenance

</td><td>

Maintenance entitlement that provides benefits to non-Microsoft customers. However, it must be linked to a base perpetual license to activate the entitlements.

</td><td>

All

</td><td>

Software Asset Management doesn’t reconcile only maintenance entitlement unless they’re linked to base perpetual licenses. Therefore, make sure to relate the maintenance entitlement to base perpetual entitlements for correct reconciliation.

</td></tr><tr><td>

Step-up

</td><td>

A licensing option that enables upgrading from a lower-tier edition of a product to a higher-tier edition, such as Standard to Enterprise,without needing to purchase a full new license.

</td><td>

All

</td><td>

If you're covered under Microsoft Software Assurance, you can upgrade a lower edition of software, such as SQL Server Standard, to a higher edition, like SQL Server Enterprise. Use the **Upgraded Entitlements** tab in the Software Entitlement form to link related versions of your software under active maintenance and your upgrades. For more information, see [Software entitlement fields](software-entitlement-fields.md).

</td></tr><tr><td>

Subscription Step-up

</td><td>

Similar to a step-up license, this license type applies to subscription-based licenses, enabling upgrades to higher-tier editions within the subscription term.

</td><td>

All \(subscription products\)

</td><td>

Same as step-up licenses, but for subscription software only.

</td></tr><tr><td>

Add on

</td><td>

Add-on USL is a user subscription license that lets you try the features of a cloud-based Microsoft 365 product or service while actively using the perpetual on-premise version. If you have a perpetual license with active SA benefits, this license enables you to test the cloud version without fully transitioning to the cloud.

</td><td>

Microsoft

</td><td>

The add-on license must be associated with a perpetual Office legacy license with active Software Assurance. Therefore, you must link the two licenses for it to work. For more information, see [Create Microsoft 365 From SA and Add-on entitlements in the Software Asset Workspace](../task/create-m365-from-sa-add-on-entitlements-workspace.md).

</td></tr><tr><td>

From SA

</td><td>

A Microsoft 365 From SA USL is a user subscription license that enables you to transition from a perpetual on-premise Microsoft software product to a corresponding cloud-based Microsoft 365 subscription, while maintaining certain SA benefits. This license is available if you have a perpetual license for on-premise Microsoft software products or services with active SA benefits.

</td><td>

Microsoft

</td><td>

The From SA license must be associated with a perpetual Office legacy license with active Software Assurance. Therefore, you must link the two licenses for it to work. For more information, see [Create Microsoft 365 From SA and Add-on entitlements in the Software Asset Workspace](../task/create-m365-from-sa-add-on-entitlements-workspace.md).

</td></tr></tbody>
</table>**Parent Topic:**[Software Asset Management references](references.md)

**Related topics**  


[Software license maintenance](../concept/software-license-maintenance.md)

[Software entitlement fields](software-entitlement-fields.md)


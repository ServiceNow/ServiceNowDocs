---
title: Unlimited software licenses
description: Unlimited software licenses help you to create entitlements with unlimited allocations and unlimited rights, allowing you to license any number of software installations with no true-up cost.
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Software license metrics, Exploring Software Asset Management, Software Asset Management, IT Asset Management]
---

# Unlimited software licenses

Unlimited software licenses help you to create entitlements with unlimited allocations and unlimited rights, allowing you to license any number of software installations with no true-up cost.

A sam\_admin or sam\_user role can specify an entitlement as an unlimited license which allows for unlimited allocations \(user or device allocations\) and does not classify the license metric results as non-compliant.

While creating or importing an entitlement, you can select the **Unlimited license** check box on the Software Entitlement page or on the Import Entitlement page.

## Considerations for unlimited licenses

-   Reconciliation process takes unlimited licenses into account where the software installations match and are licensed. Unlimited license is given priority over fixed amount license​
-   License metric results are generated separately for unlimited licenses.
-   An unlimited license perpetual entitlement can be associated to only one unlimited license maintenance entitlement.
-   Unit cost is equal to the total cost.
-   Downgrade rights are supported for unlimited licenses.
-   **Purchased rights**, **Active rights**, and **Allocations available** fields are not displayed for an unlimited license on the Software Entitlement page.

## Supported license metrics and license types

The following license metrics are supported across all metric groups for unlimited licenses:

-   Per User
-   Per Device
-   Per Named User
-   Per Named Device
-   User Subscription
-   Named User Plus
-   Per Processor

The following license types are supported for unlimited licenses:

-   Perpetual
-   Maintenance/Software Assurance
-   Perpetual + Maintenance/Perpetual + Software Assurance
-   Subscription

**Parent Topic:**[Software license metrics](c_SAMLicenseMetrics.md)


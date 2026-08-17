---
title: Hardware Asset Management release notes
description: The ServiceNow Hardware Asset Management application provides advanced workflow, automation, and mobile capabilities to track and manage your technology asset environment. Hardware Asset Management was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 3
---

# Hardware Asset Management release notes

The ServiceNow® Hardware Asset Management application provides advanced workflow, automation, and mobile capabilities to track and manage your technology asset environment. Hardware Asset Management was enhanced and updated in the Yokohama release.

## Hardware Asset Management highlights for the Yokohama release

-   Achieve asset data accuracy, improve asset utilization, and reduce risk through Asset Attestation.
-   Streamline Hardware Asset Management \(HAM\) licensing for only non-OT hardware assets to access Hardware Asset Management features and workflows.
-   Benefit from accessibility improvements to create a configurable workspace that supports Web Content Accessibility Guidelines \(WCAG\) 2.1 Level AA conformance.

See  for more information.

**Important:** Hardware Asset Management is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Yokohama release

-   **Maintain accurate asset details by creating Asset Attestations**

    Validate whether assets are in use and confirm asset assignment by performing audits through Asset Attestation to verify through confirmation by employees whether they are still using assigned serialized hardware assets.

-   **Hardware Model Normalization for Operational Technology \(OT\) assets**

    When the OT Asset Management application is installed, standardize your hardware and consumable models with a minimum of one OT asset in addition to the model categories that belong to the opted-in HAM resource categories through the Hardware Model Normalization process. The OT entity flag on the asset indicates whether it's an OT asset.


## UI changes

-   **My Assets menu and Assets tab on the Employee Center portal**

    The My Assets menu appears on the global header navigation bar of the Employee Center home page. This menu provides employees with quick access to the details of assets assigned to them.

    The Employee profile widget now includes an Assets tab, which shows the details of the assets assigned to the employee.


## Changed in this release

-   ****

    The configurable Hardware Asset Workspace supports reflow, which enables pages and content to be zoomed up to 400% through your browser settings without loss of content or functionality.


## Deprecations

The MAC address \[mac\_address\] field in the Hardware \[alm\_hardware\] table is deprecated. The data in this field is available in the new MAC address \(mac\_addr\) field in the Asset \[alm\_asset\] table.

## Activation information

Install Hardware Asset Management by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).

## Accessibility information

-   **Accessibility improvements**

    Accessibility improvements were completed to create a configurable workspace that supports WCAG 2.1 Level AA conformance.


-   **Reflow**

    The configurable workspace supports reflow, which enables pages and content to be zoomed up to 400% through your browser settings without loss of content or functionality. Additionally, content can be enlarged without scrolling in two dimensions at a width equivalent to 320 CSS pixels or a height equivalent to 256 CSS pixels. Page layouts are transformed into a vertical, stacked view automatically when users increase browser zoom to 400%. This enhancement helps users with low vision or who have trouble seeing web content in a browser due to monitor size, device type, poor lighting, or other situations. Reflow can be turned off with a system property for instances, experiences, and pages. See  for details.


## Related ServiceNow applications and features

-   ****

     The Software Asset Management application enables you to track, evaluate, and manage the software licenses, software compliance, and software optimization. You can reclaim unused software rights, purchase new software rights, and manage allocations for entitlements.

-   ****

    The Enterprise Asset Management application enables you to manage the entire life cycle of your connected and non-connected enterprise assets. It provides a comprehensive end-to-end solution for maintaining enterprise assets, minimizing costly downtime, and maximizing enterprise asset usability.

-   ****

    The Contract Management application enables you to track and manage your contracts.

-   **[Procurement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-asset-management/c_Procurement.md)**

    The Procurement application helps you to create purchase orders and to obtain items for fulfilling service catalog requests.


**Parent Topic:**[IT Asset Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/it-asset-management-rn-landing.md)


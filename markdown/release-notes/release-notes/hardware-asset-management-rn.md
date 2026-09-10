---
title: Hardware Asset Management release notes
description: The ServiceNow Hardware Asset Management application provides advanced workflow, automation, and mobile capabilities to track and manage your technology asset environment. Hardware Asset Management was enhanced and updated in the Yokohama release.The ServiceNow Hardware Asset Management application provides advanced workflow, automation, and mobile capabilities to track and manage your technology asset environment. Hardware Asset Management was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: topic
last_updated: "2025-01-30"
reading_time_minutes: 3
---

# Hardware Asset Management release notes

The ServiceNow® Hardware Asset Management application provides advanced workflow, automation, and mobile capabilities to track and manage your technology asset environment. Hardware Asset Management was enhanced and updated in the Yokohama release.

## About Hardware Asset Management

-   Achieve asset data accuracy, improve asset utilization, and reduce risk through Asset Attestation.
-   Streamline Hardware Asset Management \(HAM\) licensing for only non-OT hardware assets to access Hardware Asset Management features and workflows.
-   Benefit from accessibility improvements to create a configurable workspace that supports Web Content Accessibility Guidelines \(WCAG\) 2.1 Level AA conformance.

See [Hardware Asset Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-asset-management/ham-landing-page.md) for more information.

## Activation and other requirements

**Important:** Hardware Asset Management is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

-   **Activation information**

    Install Hardware Asset Management by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).


## Accessibility and localization

-   **Accessibility information**
    -   **Accessibility improvements**

        Accessibility improvements were completed to create a configurable workspace that supports WCAG 2.1 Level AA conformance.

    -   **Reflow**

        The configurable workspace supports reflow, which enables pages and content to be zoomed up to 400% through your browser settings without loss of content or functionality. Additionally, content can be enlarged without scrolling in two dimensions at a width equivalent to 320 CSS pixels or a height equivalent to 256 CSS pixels. Page layouts are transformed into a vertical, stacked view automatically when users increase browser zoom to 400%. This enhancement helps users with low vision or who have trouble seeing web content in a browser due to monitor size, device type, poor lighting, or other situations. Reflow can be turned off with a system property for instances, experiences, and pages. See [Reflow for Configurable Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-user-interface/auto-reflow.md) for details.


**Parent Topic:**[IT Asset Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/it-asset-management-rn-landing.md)

## Yokohama

The ServiceNow® Hardware Asset Management application provides advanced workflow, automation, and mobile capabilities to track and manage your technology asset environment. Hardware Asset Management was enhanced and updated in the Yokohama release.

### What's new

-   **[Maintain accurate asset details by creating Asset Attestations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-asset-management/asset-attestation-ham.md)**

    Validate whether assets are in use and confirm asset assignment by performing audits through Asset Attestation to verify through confirmation by employees whether they are still using assigned serialized hardware assets.

-   **[Hardware Model Normalization for Operational Technology \(OT\) assets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-asset-management/hardware-normalization.md)**

    When the OT Asset Management application is installed, standardize your hardware and consumable models with a minimum of one OT asset in addition to the model categories that belong to the opted-in HAM resource categories through the Hardware Model Normalization process. The OT entity flag on the asset indicates whether it's an OT asset.


### What's changed

-   **[My Assets menu and Assets tab on the Employee Center portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-asset-management/asset-attestation-ham.md)**

    The My Assets menu appears on the global header navigation bar of the Employee Center home page. This menu provides employees with quick access to the details of assets assigned to them.

    The Employee profile widget now includes an Assets tab, which shows the details of the assets assigned to the employee.


-   **[Reflow for Configurable Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-user-interface/auto-reflow.md)**

    The configurable Hardware Asset Workspace supports reflow, which enables pages and content to be zoomed up to 400% through your browser settings without loss of content or functionality.


### What's deprecated or removed

The MAC address \[mac\_address\] field in the Hardware \[alm\_hardware\] table is deprecated. The data in this field is available in the new MAC address \(mac\_addr\) field in the Asset \[alm\_asset\] table.


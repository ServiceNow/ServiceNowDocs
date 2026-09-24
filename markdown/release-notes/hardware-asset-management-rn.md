---
title: Hardware Asset Management release notes
description: The ServiceNow Hardware Asset Management application provides advanced workflow, automation, and mobile capabilities to track and manage your technology asset environment. See the following sections for release notes by version.This version introduces an application installation option from the Admin Home page, a Configuration Console to set up HAM, and integration of HAM with the Contract Management Pro application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/hardware-asset-management-rn.html
release: brazil
topic_type: topic
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Asset Management release notes, Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# Hardware Asset Management release notes

The ServiceNow® Hardware Asset Management application provides advanced workflow, automation, and mobile capabilities to track and manage your technology asset environment. See the following sections for release notes by version.

## About Hardware Asset Management

-   Track and manage the end-to-end life cycle of hardware assets and consumables using prescriptive workflows and a centralized single-pane view of your asset estate.
-   Reduce the risk of asset loss through asset tagging, ownership assignment, and location tracking.
-   Streamline inventory operations using mobile devices to receive assets and conduct on-site audits.
-   Automate asset life cycle workflows such as refresh, reclamation, repair, and return merchandise authorization \(RMA\).
-   Reduce duplicate and inaccurate hardware asset records by normalizing model details against the Content Service repository.

See [Hardware Asset Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/ham-landing-page.md) for more information.

## Activation and other requirements

**Note:** Hardware Asset Management is available in the ServiceNow Store. For details, see the following activation information.

-   **Activation information**

    Install Hardware Asset Management by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).

-   **Upgrade information**
    -   After upgrading to the Brazil release, review and reassess any ACL roles you have customized or deleted to confirm they reflect your expected access settings.
    -   A new system property, **sn\_itam\_restrict\_asset\_read**, controls read access to the Asset \[alm\_asset\] table and its child tables for users with only the snc\_internal role. For more information, see [Asset and CI management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/c_ManagingAssets.md).

## Accessibility and localization

-   **Accessibility information**
    -   Reflow support for Hardware Asset Management: Content can be zoomed up to 400% through your browser settings, with page layouts automatically transforming into a vertical, stacked view without loss of content or functionality. This enhancement helps users with low vision or who have trouble seeing web content due to monitor size, device type, poor lighting, or other situations.

**Parent Topic:**[Asset Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/it-asset-management-rn-landing.md)

## Version 16.0.0

This version introduces an application installation option from the Admin Home page, a Configuration Console to set up HAM, and integration of HAM with the Contract Management Pro application.

### What's new

-   **[Hardware Asset Management installation from the Product Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/install-ham-from-product-hub.md)**

    Install Hardware Asset Management and dependent applications from the Product Hub, the central location to view and manage all applications included in your subscription.

-   **[Set up Hardware Asset Management using the Configuration Console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/configure-ham-from-console.md)**

    Streamline your asset management setup by configuring all Hardware Asset Management settings from a single location using the Configuration Console. Set up users, roles, asset lifecycle, inventory, asset integrations, and generative AI skills. You can also use the AI conversational interface to configure groups, users, and content service setup.

-   **[Hardware Asset Management integration with Contract Management Pro](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/ham-cm-pro-integration.md)**

    Manage your hardware contract lifecycle across renewals, expirations, and obligations by integrating Hardware Asset Management with the Contract Management Pro application. Use the agentic workflow to extract key metadata and obligations from signed contract documents and track contractual commitments proactively to reduce unexpected costs.



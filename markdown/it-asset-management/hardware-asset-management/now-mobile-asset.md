---
title: Now Mobile app
description: Use the Now Mobile app to view the assets that are assigned to you, to report any issues with your assets, and to remotely receive new assets. Create incidents to report any issues with your assets to your IT department.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-asset-management/hardware-asset-management/now-mobile-asset.html
release: zurich
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Mobile app for Hardware Asset Management, Explore, Hardware Asset Management, IT Asset Management]
---

# Now Mobile app

Use the Now Mobile app to view the assets that are assigned to you, to report any issues with your assets, and to remotely receive new assets. Create incidents to report any issues with your assets to your IT department.

Download the Now Mobile app from Apple App Store or Google Play Store.

The Now Mobile app provides different services for tasks and requests.

To view all the assets that are assigned to you, navigate to **My Items** &gt; **My Assets** &gt; **Hardware**. The tab shows the assets that have the State field set to In transit or In use, Sub-state set to Reserved, and the Reserved to field set to your name. You can create an incident for an asset that is in use.

When you are away from your office, you can remotely receive an asset that is in transit. Scan the QR code for the asset tag so that you can automatically notify the IT department that you have received the asset.

## Supported task types in the Now Mobile app

The Now Mobile experience deliberately surfaces a limited set of task types to avoid overly long, hard-to-filter task lists for mobile users. This design choice improves usability and performance on mobile devices.

The Now Mobile app includes the following asset task types in the **My Group tasks** view by default:

-   Asset Receive Task
-   Asset Drop-off Task
-   Asset Pick Task
-   Asset Repair Task
-   Asset Troubleshoot Task
-   Asset Evaluate Task

The following asset task types aren't available in the **My Group tasks** with the base configuration:

-   Hardware Asset Reclamation Task
-   Asset RMA Task
-   Consume Asset Task
-   Hardware Refresh Line Task
-   Loaner Asset Task

## Additional asset task types on mobile

To display additional asset task types in the Now Mobile app **My Group tasks** view, you must configure each new task type using the Mobile App Builder. This customization requires you to create the following components for each task type:

-   Create mobile form views for the task type
-   Create screen navigation routes to direct users to the appropriate task form
-   Create UI actions to support task operations

For guidance on using the Mobile App Builder to create custom mobile experiences, see [Building mobile apps](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/mobile/build-mobile-apps-landing.md).

**Parent Topic:**[Mobile app for Hardware Asset Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/hardware-asset-management/mobile-my-asset.md)

**Related topics**  


[ServiceNow Agent app]()


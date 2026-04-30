---
title: Journey Accelerator versions and release compatibility
description: Available features depend on the Journey Accelerator version, family release, and application-specific features.
locale: en-US
release: yokohama
product: Journey Accelerator
classification: journey-accelerator
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Exploring Journey Accelerator, Journey Accelerator, Employee Journey Management, HR Service Delivery, Employee Service Management]
---

# Journey Accelerator versions and release compatibility

Available features depend on the Journey Accelerator version, family release, and application-specific features.

Not all Journey Accelerator features are available in all supported family releases. Go to the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view the latest information and requirements for features and releases.

**Note:** Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

Different versions of Journey Accelerator are supported only in certain family releases.

## Journey Accelerator Version 5.0.4

Supported family releases: Tokyo.

**Note:** Journey Accelerator Version 5.0.0 cannot be installed as a standalone application. Journey Accelerator version 5 functionality is installed as a dependency with Journey designer version 1. This information is for reference only.

Other requirements:

-   To schedule Outlook meetings from Journey Accelerator tasked-based to-dos, the following spoke should be installed:
    -   Microsoft Exchange Online Spoke v3.2.0 \[sn\_ex\_online\_spke\]
    -   Retry Handler Framework v1.0.1 \[sn\_retry\_handler\]
-   To use the Listening Posts \[sn\_lp\] application, you must install Listening Posts v5.0.0 from the ServiceNow Store \(and all Listening Posts requirements\)
-   To use the Learning Posts \[sn\_lnp\] application, you must install Learning Posts v5.0.0 from the ServiceNow Store \(and all Learning Posts requirements\)

## Journey Accelerator Version 4.0.2

Supported family releases:

**Note:** Journey Accelerator Version 4.0.2 is the last family release that a standalone version of the app can be installed. The latest Journey Accelerator functionality is included with the [Journey designer](../concept/jny-dsgnr-landing-page-1.md) application.

-   Utah
-   Tokyo
-   San Diego

System requirements:

-   HR Service Delivery Enterprise package
-   Employee Center \[sn\_ex\_sp\]
-   Content Publishing \[sn\_cd\]
-   The following update sets must be loaded after installing Journey Accelerator. Links to the update sets are in the Supporting Links and Documentation section of the ServiceNow Store:
    -   JA\_ESC\_header\_menu\_item-Journey Accelerator\_Plans.xml
    -   JA\_Enforce\_security\_property.xml
    -   JA\_Allow\_Content\_Delivery.xml

Other requirements:

-   To schedule Outlook meetings from Journey Accelerator tasked-based to-dos, the following spoke should be installed:
    -   Microsoft Exchange Online Spoke v3.2.0 \[sn\_ex\_online\_spke\]
    -   Retry Handler Framework v1.0.1 \[sn\_retry\_handler\]
-   To use the Listening Posts \[sn\_lp\] application, you must install Listening Posts v4.0.2 from the ServiceNow Store \(and all Listening Posts requirements\)
-   To use the Learning Posts \[sn\_lnp\] application, you must install Learning Posts v4.0.2 from the ServiceNow Store \(and all Learning Posts requirements\) as well as the following update set: JA\_HR\_Learning\_Core.xml

[Key features and requirements summary for the latest version of Journey Accelerator in ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/application/81a78882532210108ccbddeeff7b128d)

## Journey Accelerator Version 3.0.3

Supported family releases

-   Rome
-   Quebec
-   Paris

System Requirements:

-   HR Service Delivery Enterprise package
-   Employee Service Center \[com.sn\_hr\_service\_portal\]
-   Content Delivery \[com.sn\_content\_delivery\]
-   The following update must be loaded after installing Journey Accelerator. Links to the update sets are in the Supporting Links and Documentation section of the ServiceNow Store:
    -   JA\_ESC\_header\_menu\_item-Journey Accelerator\_Plans.xml
    -   JA\_Enforce\_security\_property.xml
    -   JA\_Allow\_Content\_Delivery.xml
-   The following update sets are only applicable if on Rome and will no longer be necessary after San Diego
    -   JA\_HR\_Lifecycle\_Events\_Rome\_touchpoints.xml
    -   JA\_HR\_Core\_Rome\_touchpoints.xml

Other Requirements:

To schedule Outlook meetings from Journey Accelerator tasked-based to-dos, the following spokes should be installed:

-   Microsoft Exchange Online Spoke v2.0.3 \[sn\_ex\_online\_spke\]
-   Retry Handler Framework

[Key features and requirements summary for Journey Accelerator Version 3.0.3 in ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/application/81a78882532210108ccbddeeff7b128d/3.0.3)

## Journey Accelerator Version 2.0.2

Supported releases:

-   Rome
-   Quebec
-   Paris

System Requirements:

-   HR Service Delivery Enterprise package
-   Employee Service Center \[com.sn\_hr\_service\_portal\]
-   Content Delivery \[com.sn\_content\_delivery\]
-   The following update sets must be loaded after installing Journey Accelerator. Links to the update sets are in the Supporting Links and Documentation section of the ServiceNow Store:
    -   JA\_ESC\_header\_menu\_item-Journey Accelerator\_Plans.xml
    -   JA\_Enforce\_security\_property.xml
    -   JA\_Allow\_Content\_Delivery.xml

Other Requirements:

To schedule Outlook meetings from Journey Accelerator tasked-based to-dos, the following spokes should be installed:

-   Microsoft AD Spoke \[com.sn.ad.spoke\]
-   Microsoft Azure AD spoke \[com.sn.azure\_ad.spoke\]
-   Microsoft Exchange Online Spoke v2.0 \[sn\_ex\_online\_spke\]

[Key features and requirements summary for Journey Accelerator Version 2.0.2 in ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/application/81a78882532210108ccbddeeff7b128d/2.0.2)

## Journey Accelerator Version 2.0.1

Supported releases:

-   Quebec
-   Paris

System Requirements:

-   HR Service Delivery Enterprise package
-   Employee Service Center \[com.sn\_hr\_service\_portal\]
-   Content Delivery \[com.sn\_content\_delivery\]
-   The following update sets must be loaded after installing Journey Accelerator. Links to the update sets are in the Supporting Links and Documentation section of the ServiceNow Store:
    -   JA\_ESC\_header\_menu\_item-Journey Accelerator\_Plans.xml
    -   JA\_Enforce\_security\_property.xml
    -   JA\_Allow\_Content\_Delivery.xml

Other Requirements:

To schedule Outlook meetings from Journey Accelerator tasked-based to-dos, the following spokes should be installed:

-   Microsoft AD Spoke \[com.sn.ad.spoke\]
-   Microsoft Azure AD spoke \[com.sn.azure\_ad.spoke\]
-   Microsoft Exchange Online Spoke v2.0 \[sn\_ex\_online\_spke\]

[Key features and requirements summary for Journey Accelerator Version 2.0.1 ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/application/81a78882532210108ccbddeeff7b128d/2.0.1)

## Journey Accelerator Version 1.0.2

Supported releases:

-   Quebec
-   Paris

System Requirements:

-   HR Service Delivery Enterprise package
-   Employee Service Center \[com.sn\_hr\_service\_portal\]
-   The following update sets must be loaded after installing Journey Accelerator. Links to the update sets are in the Supporting Links and Documentation section of the ServiceNow Store:
    -   JA\_ESC\_header\_menu\_item-Journey Accelerator\_Plans.xml
    -   JA\_Enforce\_security\_property.xml
    -   JA\_Allow\_Content\_Delivery.xml

[Key features and requirements summary for Journey Accelerator Version 1.0.2 in ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/application/81a78882532210108ccbddeeff7b128d/1.0.2)


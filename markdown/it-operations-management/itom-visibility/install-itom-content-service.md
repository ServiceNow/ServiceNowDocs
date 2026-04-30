---
title: Install ITOM Content Service
description: Install the ITOM Content Service application \(sn\_smart\_content\) to manage and monitor the creation of configuration items based on application fingerprints.
locale: en-US
release: zurich
product: ITOM Visibility
classification: itom-visibility
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
keywords: [Discovery, ITOM, Content, Service, Patterns]
breadcrumb: [ITOM Content Service, ITOM Visibility, IT Operations Management]
---

# Install ITOM Content Service

Install the ITOM Content Service application \(sn\_smart\_content\) to manage and monitor the creation of configuration items based on application fingerprints.

## Before you begin

-   Confirm that the application and all of its associated ServiceNow Store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).
-   Review the [ITOM Content Service](https://store.servicenow.com/store/app/c5ca2ba61b246a50a85b16db234bcbe8) application listing in the ServiceNow Store for information on dependencies, licensing or subscription requirements, and release compatibility.

Role required: admin

## About this task

The following plugins are activated with ITOM Content Service:

-   Discovery \(com.snc.discovery\)
-   Normalization Data Services Client \(com.glide.data\_services\_canonicalization.client\)
-   File Based Discovery \(com.snc.discovery.file\_based\_discovery\)—starting with ITOM Content Service version 1.5.1

**Note:** The ITOM Smart Content plugin \(com.snc.itom.smart.content\) is available starting with XP5. This plugin is optional and can be requested through ServiceNow personnel. For more information, see [Request a plugin](https://www.servicenow.com/docs/access?context=t_RequestAPlugin&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the ITOM Content Service application \(sn\_smart\_content\) using the filter criteria and search bar.

    You can search for the app by its name or ID.

    In the list next to the **Install** button, the versions that are available to you are displayed.

3.  Select a version from the list and select **Install**.

    In the Review Installation Details dialog box, any dependencies installed with your application are listed.

4.  If you're prompted, follow the links to the ServiceNow Store to get any additional entitlements for dependencies.

5.  Select **Install**.


## What to do next

[Share data on ITOM Content Service](share-data-itom-content-service.md)

**Related topics**  


[ITOM Content Service](../concept/discovery-content-services.md)

[Discovery Admin Workspace](../concept/discovery-admin-workspace.md)


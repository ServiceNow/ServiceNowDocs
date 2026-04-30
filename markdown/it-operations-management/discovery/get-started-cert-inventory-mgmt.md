---
title: Get started with Certificate Inventory and Management
description: Prior to diving into the Certificate Inventory and Management application's functionality, meet the necessary requirements by installing and activating the plugin, upgrading your instance, and obtaining the Certificate Inventory and Management application from the ServiceNow Store.
locale: en-US
release: yokohama
product: Discovery
classification: discovery
topic_type: task
last_updated: "2025-08-07"
reading_time_minutes: 1
breadcrumb: [Configuring Certificate Inventory and Management, Certificate Inventory and Management, ITOM Visibility, IT Operations Management]
---

# Get started with Certificate Inventory and Management

Prior to diving into the Certificate Inventory and Management application's functionality, meet the necessary requirements by installing and activating the plugin, upgrading your instance, and obtaining the Certificate Inventory and Management application from the ServiceNow Store.

## Before you begin

Role required: admin

## About this task

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

**Note:** The ServiceNow Store regularly releases new applications and updates to applications that are created by ServiceNow. If you already have the application, you can download the latest version to enhance your existing experience with our products. Since different features are available or enhanced each time an application is released in the Store, the content and features available in a particular release are indicated by version number in this document.

## Procedure

1.  Ensure the following plugins are installed and activated.

    -   ITOM Visibility \[com.snc.itom.vis.license\] plugin
    -   Discovery \[com.snc.discovery\] plugin
    -   Configuration Management for Scoped Apps \(CMDB\) \[com.snc.cmdb.scoped\] plugin
2.  Confirm that your system has been upgraded to Yokohama or a later version.

    During the upgrade process, the Certificate Inventory and Management \[com.sn\_disco\_certmgmt\] plugin is automatically installed if the ITOM Visibility \[com.snc.itom.vis.license\] and Discovery \[com.snc.discovery\] plugins are already installed.

3.  Download the Certificate Inventory and Management application from ServiceNow Store.


## Result

You are ready to get started with Certificate Inventory and Management.

**Note:** The MID Server needs access to the following endpoints based on your use case:

-   Entrust: Discover Certificate URL: `https://api.entrust.net/enterprise/`
-   Entrust Download root Certificate URL: `https://web.entrust.com/root-certificates/`
-   DigiCert: `https://www.digicert.com/services/`
-   Sectigo: `https://cert-manager.com/api/ssl/`
-   GoDaddy: `https://api.godaddy.com/`


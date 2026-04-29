---
title: Installing App Engine Studio
description: You can install the App Engine Studio \(AES\) application \(com.snc.app-engine-studio\) if you have the admin role. The application installs related ServiceNow Store applications and plugins if they are not already installed.
locale: en-US
release: australia
product: App Engine Studio
classification: app-engine-studio
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Configure, App Engine Studio, Building low-code applications, Developing your application, Building applications]
---

# Installing App Engine Studio

You can install the App Engine Studio \(AES\) application \(com.snc.app-engine-studio\) if you have the admin role. The application installs related ServiceNow® Store applications and plugins if they are not already installed.

## Trial version of AES

To try AES before purchasing a license, you can install it on a personal developer instance \(PDI\). For more information about PDIs, see [Personal developer instance guide](../../applications/concept/personal_developer_instance_guide.md). To obtain a PDI, see the [ServiceNow Developer Site](https://developer.servicenow.com/).

**Note:** An App Engine Studio subscription is required to install on a production or non-production instance. For more information, contact your ServiceNow representative.

## Using the ServiceNow Store to install AES

The ServiceNow Store enables you to download core products and applications. A product contains one or more applications that are licensed as a group. For example, App Engine Studio is a product that contains numerous tools and applications within it, such as Table Builder and Mobile App Builder. If you install the basic AES application and not the full AES product, you won't get its full suite of features and tools.

![AES in the ServiceNow Store](../image/aes-install-from-store-as1.png)

Check that the application and all of its associated ServiceNow Store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for AES apps](entitle-aes-product.md).

When you install AES, you also install the following related items:

-   Roles and groups
-   Tables
-   Plugins

For more information, see [Components installed with AES](../reference/installed-with-aes.md).

## Installation workflow for AES

The following is an overview of the tasks that you must perform to install AES for the first time:

1.  Develop your [instance strategy for AES](../concept/aes-instance-strategy.md).
2.  [Get entitlement for AES](entitle-aes-product.md) to ensure you have a license.
3.  [Install AES](download-aes-first-time.md) \(the full product, not the application\) from the ServiceNow Store. App Engine Studio is a product that contains numerous tools and applications within it, such as Table Builder and Mobile App Builder. If you install the basic AES application and not the full AES product, you won't get its full suite of features and tools.
4.  [Install the AES integrations and plugins](aes-install-product-integrations.md).

Alternatively, you can update existing AES installations by doing the following:

-   [Update a previously installed AES version](update-aes-previously-downloaded.md)
-   [Upgrade your AES instance to the next family release](upgrade-aes-next-family-release.md)

<table id="table_m51_zrm_jtb"><thead><tr><th>

Learn more about AES installation

</th><th>

Additional ServiceNow resources

</th></tr></thead><tbody><tr><td rowspan="3">

ServiceNow provides several additional resources on installing and administering App Engine Studio.

</td><td>

![](../../../reuse/icons/brand-icons/bus-try-a-demo.svg) [App Engine Studio release notes](https://www.servicenow.com/docs/access?context=app-engine-studio-rn&version=australia&pubname=australia-release-notes&ft:locale=en-US)

</td></tr><tr><td>

![](../../../reuse/icons/brand-icons/bus-3-person.svg) [ServiceNow Community site](https://community.servicenow.com/community?id=community_search&q=app%20engine%20studio&spa=1)

</td></tr><tr><td>

![](../../../reuse/icons/brand-icons/bus-find-an-app.svg)[ServiceNow University Introduction to App Engine Studio for Citizen Developers course](https://learning.servicenow.com/lxp/en/app-engine/introduction-to-app-engine-studio-for-citizen-developers?id=learning_course_prev&course_id=cc8d200e87629650cc49bbb5cebb35b7&s=1&ssa=3)

</td></tr></tbody>
</table>-   **[AES instance strategy](../concept/aes-instance-strategy.md)**  
You should install App Engine Studio \(AES\) on all ServiceNow instances where users will develop applications.
-   **[AES and the ServiceNow Store](../concept/aes-installation-store.md)**  
App Engine Studio \(AES\) enables you to obtain new and updated features more rapidly. Before you can use AES, you must verify that you have entitlement to it, meaning that you have valid licenses to use it. Then, you can install AES and its plugins from the ServiceNow Store.
-   **[Components installed with AES](../reference/installed-with-aes.md)**  
Several types of components are installed with activation of the App Engine Studio \(AES\) plugin, including tables and user roles.

**Parent Topic:**[Configuring App Engine Studio and related apps](../concept/aes-setup.md)


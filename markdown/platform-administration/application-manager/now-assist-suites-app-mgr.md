---
title: Now Assist suite versions in the Application Manager
description: The Application Manager uses Now Assist suite versions to verify compatibility between multiple Now Assist applications in one instance.
locale: en-US
release: australia
product: Application Manager
classification: application-manager
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Managing Now Assist apps, Application Manager, Administering applications, Get started, Administer the ServiceNow AI Platform]
---

# Now Assist suite versions in the Application Manager

The Application Manager uses Now Assist suite versions to verify compatibility between multiple Now Assist applications in one instance.

Now Assist applications often function interdependently, which can result in runtime errors when one Now Assist application is dependent on a specific version of another one. Now Assist suites help reduce runtime errors by bundling compatible versions of Now Assist applications together. Suite versions are independent from the application versions that they contain.

The Application Manager uses Now Assist suite versions to verify compatibility between every new Now Assist application version you install and all Now Assist application versions already present on your instance. This verification happens when installing new applications for the first time and when updating application versions. The installation details for Now Assist applications enable you to select a Now Assist suite version and review which applications, if any, need to be updated or procured for suite compatibility.

![Based on the Now Assist suite version selected, 35 other Now Assist applications need to be updated for compatibility.](../image/app-mgr-suite-installation.png "Now Assist installation details")

A Now Assist application version might be included in multiple Now Assist suite versions based on its compatibility with other applications. When you install or update a Now Assist application, you can choose any suite version that the application is compatible with. Based on the Now Assist suite version you choose, multiple applications might be updated.


---
title: Upgrades and the ServiceNow Store
description: The ServiceNow Store includes official applications that are developed and released by ServiceNow. Users can download, access, and configure Xanadu apps on their instances. Store application versions can be upgraded when you upgrade your instance to a new release version.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Prepare your upgrade, Xanadu release notes]
---

# Upgrades and the ServiceNow Store

The [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do) includes official applications that are developed and released by ServiceNow. Users can download, access, and configure Xanadu apps on their instances. Store application versions can be upgraded when you upgrade your instance to a new release version.

New versions for a ServiceNow® Store app can be defined in patch and family releases. This includes the ability to define a minimum version and/or a hotfix for a version you already have installed. If your instance has an installed app version below the defined minimum version, the app will be upgraded to the minimum required version. Similarly, if your instance has an installed app below the defined hotfix version, your app will be upgraded to the hotfix version.

For example, consider an application that defines these versions in a release: 1.7.0, 2.4.1, and 3.0.1. In this example, version 1.7.0 is the minimum version. Versions 2.4.1 and 3.0.1 are hotfix versions.

When an instance upgrades to the release version, the following behavior occurs:

|Version installed before the upgrade|Expected version after the upgrade|
|------------------------------------|----------------------------------|
|1.0.0|1.7.0 - The version upgrades to the minimum version|
|1.3.2|1.7.0 - The version upgrades to the minimum version|
|1.7.0|1.7.0 - The version stays the same, because the instance was already on the minimum version|
|1.7.2|1.7.2 - The version stays the same, because the instance was already ahead of the minimum version|

|Version installed before the upgrade|Expected version after the upgrade|
|------------------------------------|----------------------------------|
|1.8.0|1.8.0 - The version stays the same, because the instance was already ahead of the defined hotfix version|
|2.0.0|2.4.1 - The version upgrades to the defined hotfix version|
|2.6.0|2.6.0 - The version stays the same, because the instance was already ahead of the defined hotfix version|
|3.0.0|3.0.1 - The version upgrades to the defined hotfix version|
|3.0.5|3.0.5 - The version stays the same, because the instance was already ahead of the defined hotfix version|
|4.0.0|4.0.0 - The version stays the same, because there are no hotfix versions defined for 4.0.0+.|


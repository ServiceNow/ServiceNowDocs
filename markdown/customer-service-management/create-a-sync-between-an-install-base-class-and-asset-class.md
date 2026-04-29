---
title: Synchronizing an asset class with a configuration item class and install base class
description: You can synchronize the asset class, configuration item \(CI\) class, and the install base class by mapping the model categories in the Customer Service Management \(CSM\) application. With this synchronization, the data can flow between the different entities because the same information is replicated on both entities.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Install base items, Configure install base, Configure product data, Product data, Set up your environment, Configure, Customer Service Management]
---

# Synchronizing an asset class with a configuration item class and install base class

You can synchronize the asset class, configuration item \(CI\) class, and the install base class by mapping the model categories in the Customer Service Management \(CSM\) application. With this synchronization, the data can flow between the different entities because the same information is replicated on both entities.

## Overview

By mapping the install base class, configuration item class, and asset class fields, you can synchronize the information on both the install base item and the asset form. This mapping creates a bidirectional synchronization. For example, you can update any one of the **Location**, **Install date**, **Consumer**, **Account**, **State**, and **Contact** fields on the install base item form to create a synchronization between the install base item and the asset form. For more information on the different fields on the install base form, see [Create an install base item](../task/create-install-base-item.md).

**Note:** You must update the **Consumer** and **Account** fields from the install base item to synchronize the updates to the asset form. Updating the fields on the asset form doesn’t synchronize the updates to the install base item.

## Install Base item class

The Install Base item class on the model category form only displays the tables that extend from the install base table \[sn\_install\_base\_item\]. If the install base table has no extensions, no options are displayed in the Install Base Class list. You can create a synchronization between an install base record and an existing associated record by using the following sample migration script.

```
var ibClasses = []; //If the list is empty, system will fetch model categories for all Install base item classes
var assetIBIntegrationUtil = new sn_install_base.AssetIBIntegrationUtils();
assetIBIntegrationUtil.syncExistingInstallBaseRecordsToAsset(ibClasses)
```

## Product instance identifier

The product instance identifier helps to avoid creating duplicate records by tracking install base items and their corresponding assets. The product instance identifier applies to all the extensions of the install base \[sn\_install\_base\_item\] table.

**Note:** The **Is product instance** flag on the Model Category form is read-only by default and is marked true for selective model categories only. The product instance identifier is a hash value and not a user-friendly field.

## Product instance hierarchy for Install Base Management

Adopt the product instance hierarchy into Install Base Management to maintain a synchronization between an asset and an install base item in the Customer Service Management application.

Enable the product instance to create a synchronization for all changes that occur in the asset hierarchy to automatically reflect in the install base hierarchy. An install base item hierarchy depends on the hierarchy of its associated assets. The Install base hierarchy mirrors its corresponding asset model hierarchy for both the parent and child install base items.

**Note:** All the instances in the hierarchy must belong to the same model category.


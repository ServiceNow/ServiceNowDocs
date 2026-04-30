---
title: Synchronizing an asset class with a configuration item class and Install base class
description: You can synchronize the asset class, configuration item \(CI\) class, and the Install base class by mapping the model categories in the Customer Service Management \(CSM\) application. With this synchronization, the data can flow between the different entities because the same information is replicated on both entities.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Install base items, Configure Install base, Configure product data, Product data, Set up your environment, Configure, Customer Service Management]
---

# Synchronizing an asset class with a configuration item class and Install base class

You can synchronize the asset class, configuration item \(CI\) class, and the Install base class by mapping the model categories in the Customer Service Management \(CSM\) application. With this synchronization, the data can flow between the different entities because the same information is replicated on both entities.

## Overview

By mapping the Install base class, configuration item class, and asset class fields, you can synchronize the information on both the Install base item and the asset form. This mapping creates a bidirectional synchronization. For example, you can update any one of the **Location**, **Install date**, **Consumer**, **Account**, **State**, and **Contact** fields on the Install base item form to create a synchronization between the Install base item and the asset form. For more information on the different fields on the Install base form, see [Create an Install base item](../task/create-install-base-item.md).

**Note:** You must update the **Consumer** and **Account** fields from the Install base item to synchronize the updates to the asset form. Updating the fields on the asset form doesn’t synchronize the updates to the Install base item.

## Install base item class

The Install base item class on the model category form only displays the tables that extend from the Install base table \[sn\_install\_base\_item\]. If the Install base table has no extensions, no options are displayed in the Install base Class list. You can create a synchronization between an Install base record and an existing associated record by using the following sample migration script.

```
var ibClasses = []; //If the list is empty, system will fetch model categories for all Install base item classes
var assetIBIntegrationUtil = new sn_install_base.AssetIBIntegrationUtils();
assetIBIntegrationUtil.syncExistingInstallBaseRecordsToAsset(ibClasses)
```

## Product instance identifier

The product instance identifier helps to avoid creating duplicate records by tracking Install base items and their corresponding assets. The product instance identifier applies to all the extensions of the install base \[sn\_install\_base\_item\] table.

**Note:** The **Is product instance** flag on the Model Category form is read-only by default and is marked true for selective model categories only. The product instance identifier is a hash value and not a user-friendly field.

## Product instance hierarchy for Install Base Management

Adopt the product instance hierarchy into Install Base Management to maintain a synchronization between an asset and an Install base item in the Customer Service Management application.

Enable the product instance to create a synchronization for all changes that occur in the asset hierarchy automatically to reflect in the Install base hierarchy. An Install base item hierarchy depends on the hierarchy of its associated assets. The Install base hierarchy mirrors its corresponding asset model hierarchy for both the parent and child Install base items.

**Note:** All the instances in the hierarchy must belong to the same model category.


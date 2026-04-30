---
title: Synchronizing the install base life cycle fields with the state and status fields
description: You can synchronize the Life cycle stage field and the Life cycle stage status fields with the State and Status fields on the install base form so that you can track the lifecycle of an install base entity.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Install base items, Configure install base, Configure product data, Product data, Set up your environment, Configuring Customer Service Management, Customer Service Management]
---

# Synchronizing the install base life cycle fields with the state and status fields

You can synchronize the **Life cycle stage** field and the **Life cycle stage status** fields with the **State** and **Status** fields on the install base form so that you can track the lifecycle of an install base entity.

## Overview

Track the lifecycle of an install base entity by migrating to the Common Service Data Model. To learn about the CSDM framework, see [Common Service Data Model framework for Install Base Management](csdm-framework-for-install-base-management.md).

## Life Cycle Mapping table

The Life Cycle Mapping \[life\_cycle\_mapping\] table is already populated with the lifecycle mapping values and choices that you need to begin your synchronization of the **Life cycle stage** field and the **Life cycle stage status** fields with the **State** and **Status** fields on the install base form. The mapping record maps the **State** fields with their corresponding lifecycle fields on the install base form. The **In Use** and **InActive** options are available in the **State** field and their corresponding mappings are available in the Life Cycle Mapping \[life\_cycle\_mapping\] table. With these default options, you can initiate a synchronization with the lifeycle fields.

You can create custom choices for the **State** and **Status** field by adding a mapping record in the Life Cycle Mapping \[life\_cycle\_mapping\] table. Each custom value has related records on the Life Cycle Mapping \[life\_cycle\_mapping\] table. You must activate the mapping records for the synchronization to begin.

For information on how to create the custom choices and then map the **Life cycle stage** and **Life cycle stage status** fields with the legacy **State** field, see [Enabling CSDM life-cycle sync between legacy fields and related assets](https://www.servicenow.com/docs/access?context=csdm-life-cycle-standard-values&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).

**Note:** If the custom choices have no lifecycle mappings, then the **Life cycle stage** and the **Life cycle stage status** fields remain in the **To Be Determined** state.

## Migration of the Install Base table

If you don't want to activate all the tables and records in the CSDM framework, you can migrate only the Install Base table \(sn\_install\_base\_item\) as a part of your CSDM migration process. Use the following script to migrate the existing records to synchronize the legacy **State** field with the install base lifecycle fields.

```
var tableNames = [];//list of tablenames ex: ['sn_install_base_item'];
new sn_install_base.IBProductInstanceUtil(). syncLifeCycleFields(tableNames);
```


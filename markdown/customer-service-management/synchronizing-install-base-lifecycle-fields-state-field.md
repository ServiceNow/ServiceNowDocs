---
title: Synchronizing the Install base life cycle fields with the state and status fields
description: You can synchronize the Life cycle stage field and the Life cycle stage status fields with the State and Status fields on the Install base form so that you can track the life-cycle of an Install base entity.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Install base items, Configure Install base, Configure product data, Product data, Set up your environment, Configure, Customer Service Management]
---

# Synchronizing the Install base life cycle fields with the state and status fields

You can synchronize the **Life cycle stage** field and the **Life cycle stage status** fields with the **State** and **Status** fields on the Install base form so that you can track the life-cycle of an Install base entity.

## Overview of life cycle mapping

Track the life cycle of an Install base entity by migrating to the Common Service Data Model. To learn more about the CSDM framework, see [Common Service Data Model framework for Install Base Management](csdm-framework-for-install-base-management.md).

## Life-cycle Mapping table

The life-cycle Mapping \[life\_cycle\_mapping\] table is already populated with the life cycle mapping values and choices that you must begin your synchronization of the **Life cycle stage** field and the **Life cycle stage status** fields with the **State** and **Status** fields on the Install base form. The mapping record maps the **State** fields with their corresponding life cycle fields on the Install base form. The **In Use** and **InActive** options are available in the **State** field and their corresponding mappings are available in the life-cycle Mapping \[life\_cycle\_mapping\] table. With these default options, you can initiate a synchronization with the life cycle fields.

Add a mapping record in the life-cycle Mapping \[life\_cycle\_mapping\] table to create custom choices for the **State** and **Status** fields. Each custom value has related records on the life-cycle Mapping \[life\_cycle\_mapping\] table. You must enable the mapping records for the synchronization to begin.

For information on how to create the custom choices and then map the **Life cycle stage** and **Life cycle stage status** fields with the legacy **State** field, see [Enabling life-cycle sync from legacy-to-asset](https://www.servicenow.com/docs/access?context=csdm-life-cycle-standard-values&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).

**Note:** If the custom choices have no life cycle mappings, then the **Life cycle stage** and the **Life cycle stage status** fields remain in the **To Be Determined** state.

## Migration of the Install base table

To not activate all the tables and records in the CSDM framework, you can migrate only the Install Base table \(sn\_install\_base\_item\) as a part of your CSDM migration process. Use the following script to migrate the existing records to synchronize the legacy **State** field with the Install base life-cycle fields.

```
var tableNames = [];//list of tablenames ex: ['sn_install_base_item'];
new sn_install_base.IBProductInstanceUtil(). syncLifeCycleFields(tableNames);
```


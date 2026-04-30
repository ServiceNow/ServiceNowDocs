---
title: Enable M2M mapping between supplier contact and suppliers
description: Many-to-many \(M2M\) mapping between supplier contact and suppliers enables one supplier contact to be the contact for multiple suppliers, provided the suppliers share a parent-subsidiary relationship.
locale: en-US
release: xanadu
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: task
last_updated: "2024-11-25"
reading_time_minutes: 2
breadcrumb: [Configuring Supplier Lifecycle Operations, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Enable M2M mapping between supplier contact and suppliers

Many-to-many \(M2M\) mapping between supplier contact and suppliers enables one supplier contact to be the contact for multiple suppliers, provided the suppliers share a parent-subsidiary relationship.

## Before you begin

Role required: admin

**Important:** M2M mapping between supplier contact and suppliers is available from the Xanadu December 2024 release onwards. The following steps are required to enable M2M mapping.

## Procedure

1.  Create and run a fix script to enable M2M mapping.

    For detailed steps, see [Run the fix script](run-fix-script.md).

2.  Verify that the version record is created for the script `include M2MSupplierSupportUtil`.

    For detailed steps, see [Verify version record](verify-version-record.md).

3.  Configure the Supplier Email Domain \[sn\_slm\_email\_domain\] table to remove the `unique` constraint from the `Email Domains` column.

    For detailed steps, see [Remove the unique constraint from Email Domain](remove-unique-constraint.md).

    **Note:** This step is required only for the upgrade scenarios \(for all earlier versions upgrading to the Xanadu December 2024 release\).


-   **[Run the fix script](run-fix-script.md)**  
Run the fix script to enable M2M mapping between supplier contact and suppliers.
-   **[Verify version record](verify-version-record.md)**  
After the fix script is created and run to enable M2M mapping between supplier contact and suppliers, a version record must be created.
-   **[Remove the unique constraint from Email Domain](remove-unique-constraint.md)**  
Multiple supplier records can have the same email domain after removing the **unique** constraint from the `Email Domain` column of the Supplier Email Domain \[sn\_slm\_email\_domain\] table.

**Parent Topic:**[Configuring Supplier Lifecycle Operations](../concept/config-supp-mgmt.md)

**Related topics**  


[Install Supplier Lifecycle Operations](install-supp-mgmt.md)

[Install Supplier Collaboration Portal](install-supp-central.md)

[Supplier Document Management](../concept/supp-doc-mgmt-overview.md)

[Configure the document template for the Sign document action type for supplier task](configure-pdf-template-sign-doc-task.md)

[Advanced Work Assignment for Supplier Lifecycle Operations](../concept/supplier-awa.md)

[Configure Supplier Relationship and Performance Management](../concept/configuring-supplier-performance-mgmt.md)


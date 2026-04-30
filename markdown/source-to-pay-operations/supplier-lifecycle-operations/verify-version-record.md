---
title: Verify version record
description: After the fix script is created and run to enable M2M mapping between supplier contact and suppliers, a version record must be created.
locale: en-US
release: australia
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Enable M2M mapping between supplier contact and suppliers, Configure, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Verify version record

After the fix script is created and run to enable M2M mapping between supplier contact and suppliers, a version record must be created.

## Before you begin

Verify that the application scope is set to Supplier Common Architecture by selecting the globe icon from the upper-right pane.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Script Include**.

2.  Search for `M2MSupplierSupportUtil script include` and open it.

3.  Check in the **Versions** related list if the version record is created.

    If the version record is not created, select **Update** to manually save the script and check again for the version record.


## What to do next

Remove the unique constraint from Email Domain.

**Parent Topic:**[Enable M2M mapping between supplier contact and suppliers](enable-m2m-supplier-contacts.md)

**Related topics**  


[Run the fix script to enable M2M mapping](run-fix-script.md)

[Remove the unique constraint from Email Domain](remove-unique-constraint.md)


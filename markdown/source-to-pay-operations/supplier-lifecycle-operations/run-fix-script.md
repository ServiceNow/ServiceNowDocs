---
title: Run the fix script to enable M2M mapping
description: Run the fix script to enable M2M mapping between supplier contact and suppliers.
locale: en-US
release: australia
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Enable M2M mapping between supplier contact and suppliers, Configure, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Run the fix script to enable M2M mapping

Run the fix script to enable M2M mapping between supplier contact and suppliers.

## Before you begin

Verify that the application scope is set to Supplier Common Architecture. For more information, see [Application picker](https://www.servicenow.com/docs/access?context=c_ApplicationPicker&version=australia&pubname=australia-application-development&ft:locale=en-US).

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Fix Scripts**.

    Verify that the application scope is set to Supplier Common Architecture.

2.  Select **New**.

3.  Fill in the following fields to create the fix script:

<table id="table_fxl_tx4_mdc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique, descriptive name for the fix script.

</td></tr><tr><td>

Description

</td><td>

Include the disclaimer: **This script is intended for a one-time execution in an instance and must remain unaltered**.

</td></tr><tr><td>

Script

</td><td>

Enter the following code for the fix script:```
var m2mEnableUtil = new sn_slm.M2MSupplierSupportUtil();
gs.info("Current status of M2M Supplier support: " + m2mEnableUtil.isM2MSupplierSupported());
gs.info("Enabled M2M supplier support: " + m2mEnableUtil.enableM2MSupplierSupport());
```

</td></tr></tbody>
</table>    ![Fix script details page](../image/run-fix-script.png)

4.  Save and select **Run Fix Script**.

    A version record is created after the script is executed.


## What to do next

Verify if the version record is created for `M2MSupplierSupportUtil script include`.

**Parent Topic:**[Enable M2M mapping between supplier contact and suppliers](enable-m2m-supplier-contacts.md)

**Related topics**  


[Verify version record](verify-version-record.md)

[Remove the unique constraint from Email Domain](remove-unique-constraint.md)


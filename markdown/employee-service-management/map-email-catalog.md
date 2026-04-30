---
title: Map email fields to a catalog item
description: Map email fields to catalog item fields to pre-fill information and reduce the time taken to raise a request.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-09-05"
reading_time_minutes: 1
breadcrumb: [Configure, ServiceNow Add-in for Microsoft 365, Employee Service Management]
---

# Map email fields to a catalog item

Map email fields to catalog item fields to pre-fill information and reduce the time taken to raise a request.

## Before you begin

Role required: sn\_outlook\_addin.outlook\_addin\_setup, sn\_hr\_sp.admin, sn\_hr\_sp.esc\_admin

## Procedure

1.  Navigate to **All** &gt; **ServiceNow Add-Ins for Office** &gt; **Catalog Mapping Configurations**.

2.  On the Catalog Mapping Configurations list, select **New**.

3.  On the Catalog Mapping Configurations form, fill in the fields.

    For a description of the field values, see [Catalog Mapping Configurations form](../reference/catalog-mapping-config-form.md).

    **Note:** The fields from Microsoft Outlook are based on the Extension Point Type selected in the manifest file. Ensure that the catalog item matches the catalog item in the office controls of the add-in manifest. For more information about the manifest, see [Create a manifest file](create-ms365-addin-manifest.md).

4.  Save the form.

    A Catalog Mapping Configuration record is created. You can add Office Mailbox to Catalog Field Mapping records to map individual fields.

5.  In the Office Mailbox to Catalog Field Mappings related list, select **New**.

6.  On the Office Mailbox to Catalog Field Mappings form, fill in the fields.

    For a description of the field values, see [Office Mailbox to Catalog Field Mappings form](../reference/mailbox-catalog-mapping-form.md).

7.  Save the form.

    An Office Mailbox to Catalog Field Mappings record is created. You can create more records to map fields based on your requirement.


**Parent Topic:**[Configuring ServiceNow Add-in for Microsoft 365](../concept/configuring-sn-addin-for-ms365.md)


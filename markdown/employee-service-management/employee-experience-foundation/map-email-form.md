---
title: Map email fields to a form
description: Map email fields to form fields to pre-fill information and reduce the time taken to submit an incident or a case.
locale: en-US
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring ServiceNow Add-in for Microsoft 365, ServiceNow Add-in for Microsoft 365, Unified Employee Experience, Employee Service Management]
---

# Map email fields to a form

Map email fields to form fields to pre-fill information and reduce the time taken to submit an incident or a case.

## Before you begin

Role required: sn\_outlook\_addin.outlook\_addin\_setup, sn\_hr\_sp.admin, sn\_hr\_sp.esc\_admin

## Procedure

1.  Navigate to **All** &gt; **ServiceNow Add-Ins for Office** &gt; **Form Mapping Configurations**.

2.  On the Form Mapping Configurations list, select **New**.

3.  On the Form Mappings Configurations form, fill in the fields.

    For a description of the field values, see [Form Mapping Configurations form](../reference/form-mapping-config-form.md).

    **Note:** The fields from Microsoft Outlook are based on the Extension Point Type selected in the manifest file. Ensure that the table matches the table in the office controls of the add-in manifest. For more information about the manifest, see [Create a manifest file](create-ms365-addin-manifest.md).

4.  Save the form.

    A Form Mapping Configuration record is created. You can add Office Mailbox to Catalog Field Mapping records to map individual fields.

5.  In the Office Mailbox to Form Field Mappings related list, select **New**.

6.  On the Office Mailbox to Form Field Mappings form, fill in the fields.

    For a description of the field values, see [Office Mailbox to Form Field Mappings form](../reference/mailbox-form-mapping-form.md).

7.  Save the form.

    An Office Mailbox to Form Field Mappings record is created. You can create more records to map fields based on your requirement.


**Parent Topic:**[Configuring ServiceNow Add-in for Microsoft 365](../concept/configuring-sn-addin-for-ms365.md)


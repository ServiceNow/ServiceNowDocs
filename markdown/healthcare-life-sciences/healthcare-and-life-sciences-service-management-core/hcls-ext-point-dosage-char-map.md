---
title: Configure the mapping between a dosage characteristic and a dosage details field
description: Use scripted extension points to decide which dosage characteristics are mapped to the fields on the Dosage details section of a Medication Prescription form.
locale: en-US
release: australia
product: Healthcare and Life Sciences Service Management Core
classification: healthcare-and-life-sciences-service-management-core
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure dosage specifications, Configure, Healthcare and Life Sciences Service Management Core, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Configure the mapping between a dosage characteristic and a dosage details field

Use scripted extension points to decide which dosage characteristics are mapped to the fields on the Dosage details section of a Medication Prescription form.

## Before you begin

Set the application scope to Healthcare and Life Sciences Service Management Core using the application picker. For more information, see [Application picker](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/c_ApplicationPicker.md).

Role required: admin

## About this task

The Healthcare and Life Sciences Service Management Core application installs the `sn_hcls.DosageCharacteristicsMapper` script include and the `DosageCharacteristicsMapper` extension point.

The `DosageCharacteristicsMapper` extension point in the `sn_hcls.DosageCharacteristicsMapper` script include is preconfigured for the mapping between characteristics in the dosage-related characteristic groups and the Dosage details fields on a medication prescription. The default implementation of the `getMappingObject` method in the `DosageCharacteristicsMapper` extension point maps the dosage-related characteristic groups and Dosage details fields of a Medication Prescription form as shown in the following table.

<table id="table_sh3_bxj_htb"><thead><tr><th>

Dosage characteristic group

</th><th>

Dosage details field

</th></tr></thead><tbody><tr><td>

Dosage - dosage

</td><td>

Dosage

</td></tr><tr><td>

Dosage - number of authorized refills

</td><td>

Number of authorized refills

</td></tr><tr><td>

Dosage - instructions for patient

</td><td>

Instructions for patient

</td></tr><tr><td>

Dosage - quantity

</td><td>

Quantity

</td></tr></tbody>
</table>Using extension points makes it easier to integrate customizations without actually altering the base code. You can extend standard base functionality using customized scripts. For more information, see [Using extension points to extend application functionality](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/extension-points.md).

An implementation is available in the base system for scripted extension points. You can modify the data and add additional fields.

## Procedure

1.  Navigate to **All** &gt; **System Extension Points** &gt; **Scripted Extension Points**.

2.  In the **API Name** column, search for and click **sn\_hcls.DosageCharacteristicsMapper**.

3.  On the Extension Point form, select a script include to use the `DosageCharacteristicsMapper` extension point.

    -   Modify the existing script by going to the Implementations related list and clicking **DosageCharacteristicsMapper**.
    -   Create and register a custom script include.
4.  Include your mapping logic by adding the `getMappingObject` method to your script include that implements the `DosageCharacteristicsMapper` extension point.

    You can create multiple implementations for the extension point and provide an order number for each implementation. The implementation that has the lowest order number is executed first.

5.  On the Extension Point form, click **Update**.



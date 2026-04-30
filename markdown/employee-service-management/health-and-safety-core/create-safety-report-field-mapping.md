---
title: Create a safety report field mapping for generating reports
description: Create a safety report field mapping to map fields in your reporting PDF template to the corresponding fields in the Health and Safety records.
locale: en-US
release: zurich
product: Health and Safety Core
classification: health-and-safety-core
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Configure, Health and Safety Core, Health and Safety, Employee Service Management]
---

# Create a safety report field mapping for generating reports

Create a safety report field mapping to map fields in your reporting PDF template to the corresponding fields in the Health and Safety records.

## Before you begin

-   The imported reporting PDF template, that you want to create the mapping for, must be fillable.
-   The Health and Safety table to be mapped is enabled for report field mapping. For more information, see [Enable a Health and Safety table for configuring report field mapping](enable-hs-table-report-field-mapping.md).

Role required: sn\_ohs\_im.report\_mapping\_manager

## About this task

The report field mapping enables you to do the following:

-   Import your own PDF templates that you need to use for reporting such as for regional conformance or industry-specific needs.
-   Map the fields in your reporting PDF template with the fields in safety records, such as an incident, observation, and injury and illness.
-   Using the PDF template, generate reports from safety records with fields auto-populated, making the reporting process more efficient.

## Procedure

1.  Navigate to **Workspaces** &gt; **Health and Safety Workspace**.

2.  Select the configuration icon \(![Configuration icon](../../hs-risk-management/image/icon-config.png)\).

3.  In the **Configuration** tab, select **Report field mappings** and then **All**.

4.  Create a report field mapping or modify an existing one.

    -   To create a report field mapping, select **New**.
    -   To review an existing one, open the one that you want to configure.
5.  On the form, fill in the fields.

    For information on form field descriptions, see [Health and Safety report field mapping form](../reference/hs-report-field-mapping-form.md).

6.  Select **Save**.

    The **Form field mapping** tab appears. The **Field mappings** section shows all fields extracted from the imported PDF. A preview of the attached PDF is available alongside the **Field mappings**.

7.  In the **Field Mappings** section, map Health and Safety fields to each field extracted from the PDF.

    **Tip:** In the PDF preview, select a fillable field to highlight the corresponding field in the Field Mappings list. Alternatively, select a field in the Field Mappings list and it’s highlighted on the PDF preview.

<table id="choicetable_u34_hz2_2bc"><thead><tr><th align="left" id="d67011e211">

Option

</th><th align="left" id="d67011e214">

Steps

</th></tr></thead><tbody><tr><td id="d67011e220">

**Using the Health and Safety field list**

</td><td>

In the list available with each field name, select a Health and Safety field to map to.The list displays fields from the selected Health and Safety mapping table.

However, dot-walk fields are also available to select from the field mapping list to map further reference fields. For information on dot-walking, see [Dot-walking to data in related tables](https://www.servicenow.com/docs/access?context=c_DotWalking&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US).

</td></tr><tr><td id="d67011e246">

**Using a custom script**

</td><td>

Select the more options icon \(![More options icon](../../wsd-for-mobile/images/more-options-icon.png)\) beside the field mapping and then select **Add script**. The **Edit script** dialog box includes a few examples for your reference. You must provide the correct table, field names, and so on, in your script, and modify as you require for the mapping.

**Note:** This scripting is done within the Health and Safety application scope.

Each mapping can be scripted using the script capability on each field. It enables the field to be mapped in a certain way using a custom logic or perform any type of data transformation on the field value, as needed.

</td></tr></tbody>
</table>8.  Check that the field mappings are active.​

    To deactivate a field mapping, select the more options icon \(![More options icon](../../wsd-for-mobile/images/more-options-icon.png)\) beside the field mapping and then select **Deactivate**.

9.  Select **Save**.


## Result

-   The fields in the imported reporting PDF template are mapped to the fields in the selected mapping table.
-   The published report field mapping is available to select during a report generation in the mapped safety table records. For example, see [Generate a report for a safety incident, observation, or injury](generate-report-safety-incident-obsv-injury.md).

**Parent Topic:**[Setting up Health and Safety Core](../../hs-core/concept/setting-up-hs-core.md)

**Related topics**  


[Install Health and Safety Core](../../hs-core/task/install-hs-core.md)

[Workplace location data](configure-hs-workplace-location-data.md)

[Enable a Health and Safety table for configuring report field mapping](enable-hs-table-report-field-mapping.md)

[Configure groups for Health and Safety](configure-groups-health-and-safety.md)

[Configure scheduled job to generate frequency rates](configure-job-generate-frequency-rates.md)

[Assign Health and Safety profile to a user](assign-hs-profile-user.md)

[Add a Health and Safety visitor](hs-add-health-safety-visitor.md)

[Migrate existing safety documents to the Document library](../../hs-core/task/hs-migrate-sync-existing-safety-document-docs-library.md)


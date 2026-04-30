---
title: Health and Safety report field mapping form
description: A safety report mapping manager can create a mapping report for generating reports using the report field mapping form.
locale: en-US
release: zurich
product: Health and Safety Core
classification: health-and-safety-core
topic_type: reference
last_updated: "2025-11-20"
reading_time_minutes: 3
breadcrumb: [Reference, Health and Safety Core, Health and Safety, Employee Service Management]
---

# Health and Safety report field mapping form

A safety report mapping manager can create a mapping report for generating reports using the report field mapping form.

For more information on creating a mapping, see [Create a safety report field mapping for generating reports](../task/create-safety-report-field-mapping.md).

<table id="table_hs_report_mapping"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

System-generated unique number for the report field mapping.

</td></tr><tr><td>

Location

</td><td>

Location that this report field mapping applies to.

</td></tr><tr><td>

Short description

</td><td>

Brief description about the report field mapping.

</td></tr><tr><td>

State

</td><td>

State of the report field mapping.-   **Draft**: Select to perform mappings in the Form Field Mapping tab.​
-   **Published**: Select to publish and mark this mapping available for use.

Only the published mappings are available to select during report generation.

-   **Obsolete**: Select to mark this mapping as obsolete.

</td></tr><tr><td>

Mapping table

</td><td>

Health and Safety table to map PDF fields to, for example, Health and Safety incident \[sn\_ohs\_im\_incident\] or Injury and illness \[sn\_ohs\_im\_injury\_illness\].Only the tables enabled for report field mapping appear in this field.

</td></tr><tr><td>

Fillable PDF

</td><td>

Option whether the exported PDF is editable.-   **Empty fields are editable**: Only the fields that have not been filled in the exported PDF can be edited.
-   **All fields are editable**: Any field in the exported PDF can be edited.
-   **No fields are editable**: No field in the exported PDF can be edited.

</td></tr><tr><td>

Attach to the record

</td><td>

Enables attaching the report generated from this mapping directly to the associated record.When this option is not selected, the generated report is downloaded to the browser instead of being attached to the record.

</td></tr><tr><td>

Required roles

</td><td>

Role that can generate the report using this mapping. You can add multiple roles in this field.Only users with these roles can view and select this report mapping when generating a report. If there are no roles in this field, the mapping is available to all users when generating the report.

</td></tr><tr><td>

PDF document

</td><td>

PDF template that you need to use for reporting and map the safety record fields to. Select **Attach file** to import the reporting PDF template.

</td></tr></tbody>
</table>**Parent Topic:**[Health and Safety Core reference](../../hs-core/concept/hs-core-reference.md)

**Related topics**  


[Components installed with Health and Safety Core](../../hs-core/reference/components-installed-hs-core.md)

[Health and Safety action form](hs-action-form.md)

[Health and safety action schedule form](hs-health-safety-action-schedule-form.md)

[Health and Safety profile form](hs-health-safety-profile-form.md)

[Health and Safety document version form](hs-document-form.md)

[Health and Safety meeting form](hs-safety-meeting-form.md)

[Health and Safety meeting attendee form](hs-safety-meeting-attendee-form.md)


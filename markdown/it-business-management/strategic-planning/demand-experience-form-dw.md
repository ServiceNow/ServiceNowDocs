---
title: Demand experience form
description: The demand experience form information is used to create or update a demand experience.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-business-management/strategic-planning/demand-experience-form-dw.html
release: australia
product: Strategic Planning
classification: strategic-planning
topic_type: reference
last_updated: "2026-09-25"
reading_time_minutes: 1
breadcrumb: [Forms, Reference, Next Experience for Demand Management in Strategic Planning, Strategic Planning, Strategic Portfolio Management]
---

# Demand experience form

The demand experience form information is used to create or update a demand experience.

<table id="table_demand_experience_form_main"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Label

</td><td>

Display name of the demand experience configuration.

</td></tr><tr><td>

Name

</td><td>

ID of the demand experience. Automatically derived from the Label field and is a read-only field.

</td></tr><tr><td>

Active

</td><td>

Indication of whether the demand experience is available to select on a demand. Active by default.

</td></tr><tr><td>

Description

</td><td>

Description of the demand experience configuration.

</td></tr><tr><td>

Table

</td><td>

Table this demand experience applies to. Defaults to the Demand \[dmn\_demand\] table.

</td></tr><tr><td>

Dynamic category

</td><td>

Name of the dynamic category associated with this demand experience. The dynamic category defines the custom fields that appear alongside the default fields on demands that use this experience.These dynamic categories are configured by an EWD admin. For more information, see [Create a dynamic category](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/strategic-planning/create-a-dynamic-category-dw.md).

</td></tr><tr><td>

Form view

</td><td>

Form view that displays demand records that use this experience. If you don't select a form view, the APW Default view applies.

</td></tr></tbody>
</table>|Field|Description|
|-----|-----------|
|AI overview|Option to show the AI overview module on demands that use this experience.|
|Details|Option to show the Details module on demands that use this experience.|
|Docs|Option to show the Docs module on demands that use this experience.|
|Financials|Option to show the Financials module on demands that use this experience.|
|Playbook|Option to show the Playbook module on demands that use this experience.|
|Resources|Option to show the Resources module on demands that use this experience.|
|Smart assessments|Option to show the Smart assessments module on demands that use this experience.|

**Note:** Every module check box is selected by default when you create a demand experience. Clearing a check box hides that module in Next Experience for Demand Management for demands that use this experience.


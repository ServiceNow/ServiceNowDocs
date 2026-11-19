---
title: Create a demand experience
description: Create a demand experience to control the form view, demand modules, and dynamic attributes that appear on demands to support configuration independence across different types of demands.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/strategic-planning/create-a-demand-experience-dw.html
release: brazil
product: Strategic Planning
classification: strategic-planning
topic_type: task
last_updated: "2026-09-25"
reading_time_minutes: 3
breadcrumb: [Configuring demand experiences, Demand experiences, Manage demands, Use, Next Experience for Demand Management in Strategic Planning, Strategic Planning, Strategic Portfolio Management]
---

# Create a demand experience

Create a demand experience to control the form view, demand modules, and dynamic attributes that appear on demands to support configuration independence across different types of demands.

## Before you begin

If the demand experience uses a dynamic category, the dynamic category that must be defined.

Role required: pps\_admin or sn\_spm\_ewd.ewd\_admin

## About this task

\[Omitted video\] Description: Create and manage demand experiences

A demand experience consists of a custom form view, demand modules, and, optionally, a dynamic category that defines dynamic attributes for that experience. For example, you can create experiences for Marketing or IT governance processes. For more information, see [Demand experiences](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/strategic-planning/demand-experiences-dw.md).

## Procedure

1.  Navigate to **All** &gt; **Demand Experiences**.

    \[Omitted image "demand-experiences-navigation.png"\] Alt text: Navigation for Demand Experiences.

2.  Select **New**.

3.  Fill in the fields on the form.

    \[Omitted image "demand-experiences-form.png"\] Alt text: Demand experience form.

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

Table that this demand experience applies to. The list shows the Demand \[dmn\_demand\] table and the tables that extend it. Defaults to the Demand \[dmn\_demand\] table.

</td></tr><tr><td>

Dynamic category

</td><td>

Name of the dynamic category associated with this demand experience. The dynamic category defines the dynamic attributes that appear alongside the default fields on demands that use this experience.These dynamic categories are configured by an administrator. For more information, see [Create a dynamic category](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/strategic-planning/create-a-dynamic-category-dw.md).

</td></tr><tr><td>

Form view

</td><td>

Form view that displays demand records that use this experience. If you don't select a form view, the APW Default view applies.

</td></tr></tbody>
</table>4.  Under **Show modules**, clear the check box for any module that you don't want to show for demands that use this experience.

    |Field|Description|
    |-----|-----------|
    |AI overview|Option to show the AI overview module on demands that use this experience.|
    |Details|Option to show the Details module on demands that use this experience.|
    |Docs|Option to show the Docs module on demands that use this experience.|
    |Financials|Option to show the Financials module on demands that use this experience.|
    |Playbook|Option to show the Playbook module on demands that use this experience.|
    |Resources|Option to show the Resources module on demands that use this experience.|
    |Smart assessments|Option to show the Smart assessments module on demands that use this experience.|

    **Note:** Every module check box is selected by default when you create a demand experience. Clearing a check box hides that module in Next Experience for Demand Management for demands that use this experience.

    **Tip:** Select at least one module for the experience.

    An enabled module appears on a demand only for users who meet its conditions:

    -   **AI overview**: The demand summarization skill is active and available to the user.
    -   **Playbook**: The user has the it\_demand\_user role and a playbook is associated with the demand.
    -   **Resources**: The user has the resource\_user role.
    -   **Financials**: The user has the it\_demand\_manager role.
    -   **Smart assessments**: The user has the sn\_smart\_asmt.assessment\_reader or sn\_smart\_asmt.actor role.
5.  Select **Submit**.


## Result

The demand experience is available to select when a demand is created. Only the modules that you left selected are shown for demands that use this experience, and a view rule and workspace view rule are created automatically. If you selected a dynamic category with dynamic attributes, an **Additional Information** tab appears in the Details module, showing those attributes.

**Related topics**  


[Create a demand](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/strategic-planning/create-demand-from-dw.md)

[Add dynamic attributes to a demand](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/strategic-planning/add-dynamic-attributes-to-a-demand-dw.md)


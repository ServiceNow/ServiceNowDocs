---
title: Catalog Wizard form
description: Description of the fields for the Catalog Wizard Step, Catalog Wizard Section, Variable, and Catalog Wizard Question forms in Service Catalog wizards.
locale: en-US
release: zurich
product: Service Catalog
classification: service-catalog
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Service Catalog Reference, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Catalog Wizard form

Description of the fields for the Catalog Wizard Step, Catalog Wizard Section, Variable, and Catalog Wizard Question forms in Service Catalog wizards.

<table id="table_qfy_vyc_vtb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name of the step.

</td></tr><tr><td>

Wizard

</td><td>

Wizard for which you are creating the step.

</td></tr><tr><td>

Hide on template

</td><td>

Option to hide the step in the catalog item template.

</td></tr><tr><td>

Custom step

</td><td>

Option to configure the step as a custom step.

</td></tr><tr><td>

Short description

</td><td>

Brief description of the step.

</td></tr><tr><td>

Feedback

</td><td>

Option to associate a feedback record with the step in the catalog item builder wizard or record producer builder wizard.

</td></tr><tr><td>

Template feedback

</td><td>

Option to associate a feedback text with a step in the catalog item template.

</td></tr><tr><td>

Order

</td><td>

Order where the step is placed in Catalog Builder.

</td></tr><tr><td>

Macroponent

</td><td>

Reusable seismic building blocks in the Next Experience UI Framework that can be used to create a custom step. This field appears only when the **Custom step** check box is selected.For more information, see [https://developer.servicenow.com/dev.do\#!/reference/now-experience/sandiego/ui-framework/getting-started/introduction](https://developer.servicenow.com/dev.do#!/reference/now-experience/sandiego/ui-framework/getting-started/introduction)

</td></tr></tbody>
</table>|Field|Description|
|-----|-----------|
|Name|Unique name of the section.|
|Style|Display style of the section.|
|Order|Order in which the section appears inside a step.|
|Wizard step|Step with which the section is associated.|
|Short description|Brief description of the section.|
|Width|Width of the section in Catalog Builder.|

<table id="table_okf_km2_g4b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Map to field

</td><td>

Maps the question to a specific field on the Catalog Item \(sc\_cat\_item\) table or Record Producer \(sc\_cat\_item\_producer\) table.

</td></tr><tr><td>

Type

</td><td>

The variable type that you want to create.

</td></tr><tr><td>

Catalog item

</td><td>

Catalog item associated with the question.

</td></tr><tr><td>

Active

</td><td>

Option to make the variable available for use.

</td></tr><tr><td>

Mandatory

</td><td>

Option to make the variable mandatory as part of the ordering process.

</td></tr><tr><td>

Hidden

</td><td>

Option to hide the variable.

</td></tr><tr><td>

Read-only

</td><td>

Option to make the variable read only or editable.

</td></tr><tr><td>

Question

</td><td>

Question to ask catalog item creators in Catalog Builder.

</td></tr><tr><td>

Name

</td><td>

Name to identify the question.

</td></tr><tr><td>

Tooltip

</td><td>

Tooltip text to display when catalog item creators point to the variable in Catalog Builder. You can enter a brief note to describe the purpose of the question.

</td></tr><tr><td>

Example Text

</td><td>

Hint that is displayed in the **Question** field before a catalog item creator enters a value. Applicable for the following variables:-   IP Address
-   Email
-   URL
-   Single Line Text
-   Wide Single Line Text
-   Multi Line Text
-   Date
-   Date/Time

</td></tr></tbody>
</table><table id="table_iyx_xzc_vtb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Wizard section

</td><td>

Section with which the question must be associated with.

</td></tr><tr><td>

Map to set

</td><td>

Option to map the question to a question set. The **Set** field is enabled only when this option is selected.

</td></tr><tr><td>

Order

</td><td>

Order in which the question must appear inside a section.

</td></tr><tr><td>

Question

</td><td>

Option to associate a question to the section.**Note:** You can create a new variable to associate to a question or select an existing one.

For information on creating a new variable, see [Add a step, section, or question to a catalog item wizard](../task/catalog-wizard.md).

</td></tr><tr><td>

Set

</td><td>

Option to associate a question set to the section if you have selected the **Map to set** option.

</td></tr></tbody>
</table>For information about adding a step, section, or question to a catalog item wizard, see [Add a step, section, or question to a catalog item wizard](../task/configure-the-catalog-builder-experience.md).

**Parent Topic:**[Service Catalog Reference](../concept/service-catalog-reference.md)


---
title: Create Template configurations
description: Use the Template Configurations module to set up the template relationship registry. This module displays document design template configurations for action tasks. It enables you to configure data relationships, content, and scripted variables via the Document designer application so that required data is displayed in your reports.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Generating Microsoft Word reports using Document designer, Manage, Using Digital resilience incident reporting, Manage, Operational Resilience, Governance, Risk, and Compliance]
---

# Create Template configurations

Use the Template Configurations module to set up the template relationship registry. This module displays document design template configurations for action tasks. It enables you to configure data relationships, content, and scripted variables via the Document designer application so that required data is displayed in your reports.

## Before you begin

Role required: sn\_oper\_res.admin

## About this task

From the Administration menu, the Template Configurations module displays document design template details for DRIR action tasks. The Word Templates module, on the other hand, provides DRIR Word templates necessary for generating Microsoft Word reports.

## Procedure

1.  Navigate to **All** &gt; **Digital resilience incident reporting** &gt; **Template Configurations**.

    Predefined Microsoft Word templates, available with the base version, are displayed in the Template Configurations module. The example shows a predefined DRI template.

    ![Configuration.](../image/temp-config.png)

2.  To create a template, select **New** in the Template Configurations module.

    You can either use the predefined templates or create your own templates in the Template Configurations module.

3.  On the form, fill in the fields.

<table id="table_zb5_hgc_pcc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the template configuration. For example, you can specify Engagement template configuration.

</td></tr><tr><td>

Business domain

</td><td>

Domain from which the template is being configured. \(Refers Microsoft 365 business domain table\).**Note:** For Digital resilience incident reporting, select the DRI business domain value. In the Template Configurations module, this domain corresponds to the 'DRIR' entry in the Microsoft 365 business domain \(sn\_esg\_msoff\_intg\_business\_domain\) table. In the Reporting Configurations module, the same scope is represented as 'DRI' in the GRC business domain \(sn\_grc\_business\_domain\) table. Both reference the same underlying business domain record \(sys\_id: 41d4216b83f840d28101d55520756c49\).

</td></tr><tr><td>

Table

</td><td>

Source table on which the Microsoft Word template would be built.

</td></tr><tr><td>

Fields

</td><td>

Fields from which data must be displayed on the report. Move the required fields from the Available list to the Selected list.

</td></tr></tbody>
</table>    The example shows how the fields are used in a Microsoft Word document.

    ![Data column.](../image/d19-data-rel-selection-in-word-doc.png)

4.  Select **Submit**.

5.  To edit an existing template, select it from the list, edit the data relationships, content configurations, and scripted variables, then select **Update**.

    You can update the data relationships, content configurations, and scripted variables for the predefined templates.



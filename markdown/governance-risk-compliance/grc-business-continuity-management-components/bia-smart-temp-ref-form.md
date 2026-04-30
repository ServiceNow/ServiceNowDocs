---
title: BIA template record form for the Smart assessment
description: Use the BIA template record form to configure the business impact analysis with the Smart assessment. You can add details such as name, description, primary element assessed and select the impact assessment template in the form.
locale: en-US
release: yokohama
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure BIA templates with SAE, Setup for a BIA, Configure, Business Continuity Management, Governance, Risk, and Compliance]
---

# BIA template record form for the Smart assessment

Use the BIA template record form to configure the business impact analysis with the Smart assessment. You can add details such as name, description, primary element assessed and select the impact assessment template in the form.

## BIA template record form with Smart Assessment

For description of the field values, see the table.

<table id="table_k3d_xgj_2nb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the BIA template.

</td></tr><tr><td>

Description

</td><td>

Brief description about the template.

</td></tr><tr><td>

Primary element assessed

</td><td>

Primary object type or an element that is being assessed for which the template is used.

</td></tr><tr><td>

Assessment type

</td><td>

Assessment type for the BIA. Options are:-   **Legacy assessment**
-   **Smart assessment**

Select the **Smart assessment** option.

</td></tr><tr><td>

Impact assessment template

</td><td>

Type of the impact assessment template. You can select the Recovery point objective assessment template or Recovery time objective assessment template. For more information, see [Create Smart Assessment templates for BIA](../task/conf-impact-asmt-template.md).

</td></tr><tr><td>

Dependency assessments

</td><td>

Category of items or assets that the business function depends on, such as Datacenters, Hardware. The dependencies are identified and assessed as part of the business impact analysis.

</td></tr><tr><td>

Include CIA

</td><td>

Option to include Confidentiality, Integrity, and Availability to BIA. If the primary element that is being analyzed has critical data and whether it must include Confidentiality, Integrity and Availability information in the analysis, set the flag as **Yes**.

 The field appears only if the elements selected in the **Primary Element Assessed** field of the same form require data backup.

</td></tr></tbody>
</table>**Parent Topic:**[Configure BIA templates with Smart Assessment](../task/conf-bia-temp-smart-asmt-type.md)


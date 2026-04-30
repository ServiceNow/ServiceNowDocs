---
title: BIA template form for the legacy assessment
description: Use the BIA template form to configure the business impact analysis with the legacy template. You can add details such as name, description, elements, impact categories, and so on in the form.
locale: en-US
release: zurich
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure BIA templates, Setup for BIA, Configure, Business Continuity Management, Governance, Risk, and Compliance]
---

# BIA template form for the legacy assessment

Use the BIA template form to configure the business impact analysis with the legacy template. You can add details such as name, description, elements, impact categories, and so on in the form.

## BIA template form with legacy assessment

For description of the field values, see the table.

<table id="table_k3d_xgj_2nb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the BIA template. For example, Application downtime assessment.

</td></tr><tr><td>

Description

</td><td>

Brief description of the template.

</td></tr><tr><td>

Primary element assessed

</td><td>

Primary object type or an element that is being assessed using this template.

</td></tr><tr><td>

Assessment type

</td><td>

Assessment type for the BIA. Options are:-   **Legacy assessment**
-   **Smart assessment**

Select the Legacy assessment option.

</td></tr><tr><td>

Impact categories

</td><td>

Category of impact that is relevant to an organization and that is assessed during the business impact analysis. It can be revenue, legal, regulatory, reputation impact, and so on.

</td></tr><tr><td>

Dependency assessments

</td><td>

Category of items or assets that the business function depends on such as locations or business applications. The dependencies are identified and assessed as part of the business impact analysis.

</td></tr><tr><td>

Include CIA

</td><td>

Option to include Confidentiality, Integrity, and Availability to BIA. Available options are:

-   **Yes**: Set the flag as **Yes**, if the primary element that is being analyzed has critical data and whether it must include Confidentiality, Integrity, and Availability information in the analysis.
-   **No**: Set the flag as **No**, if the primary element that is being analyzed does not have critical data.

 The field appears only if the elements that selected for the **Primary Element Assessed** field in the same form require data backup.

</td></tr></tbody>
</table>**Parent Topic:**[Configure BIA templates with legacy assessment](../task/configure-bia-template-uib-ws.md)


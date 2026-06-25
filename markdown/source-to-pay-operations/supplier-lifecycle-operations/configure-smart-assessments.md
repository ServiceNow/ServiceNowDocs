---
title: Configure smart assessments
description: Supplier managers can configure and create assessments in bulk for internal and external users by adding instructions, questions, and reference information from the Assessment Workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/supplier-lifecycle-operations/configure-smart-assessments.html
release: australia
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Configure, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Configure smart assessments

Supplier managers can configure and create assessments in bulk for internal and external users by adding instructions, questions, and reference information from the Assessment Workspace.

## Prerequisites for creating smart assessments

To use this functionality, verify that the following plugins are installed:

-   Smart Assessment Core plugin \(com.sn\_smart\_asmt\)
-   Smart Assessment Designer plugin \(com.sn\_smart\_asmt\_desg\)
-   Smart Assessment Connected plugin \(com.sn\_smart\_asmt\_conn\)

## Smart assessment creation workflow

From the **Assessment Workspace**:

1.  An assessment template is created from the Assessment Workspace, setting the following:

<table id="table_x5f_nlw_h3c"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

**Purpose**

</td><td>

This field is set to **Supplier management surveys**. **Note:** Only templates tagged with this purpose appear in the segmentation tool in the **Assessment templates** tab.

</td></tr><tr><td>

**Assessment targets**

</td><td>

This field is set to include the **Supplier** and **Segmentation rule assessment template relationship** tables.

</td></tr></tbody>
</table>    Assessment questions are added from the **Questions** tab of the new template.

    For more information, see [Create assessment template from Assessment Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/create-assessment-template-from-assessment-workspace.md).

2.  Optional: **Scoring** option is enabled to initiate the calculation of the assessment-level scores, which can be grouped by sections or questions. For more information, see [Configure scoring for an assessment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/configure-scoring-for-assessments.md).

    **Note:** The smart assessment scoring plugin \[com.sn\_smart\_scoring\] must be installed for configuring scoring options.

3.  User criteria for reassignment are configured and enabled, restricting contacts to delegate the assessment to another contact from their organization. If no user criteria are configured, the reassign option is available to all users without restriction. For more information, see [Configure user criteria for reassigning assessments](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/configure-user-criteria-for-reassigning-assessments.md).
4.  The assessment template is published after completing the preceding configurations.

From the **Source-to-Pay Workspace**:

1.  A segmentation rule is created from the Source-to-Pay Workspace. An assessment template is mapped with the new segmentation rule from the **Assessment templates** tab. The new segmentation rule can be created for the following audience types:

    -   Manager\(s\)
    -   All supplier managers
    -   Only primary supplier contact\(s\)
    -   All supplier contacts
    For more information, see [Map assessment template with segmentation rule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/add-assessment-template-in-segmentation-rule.md).

2.  Final assessments are triggered from the Segmentation rule assessment template mapping. For more information, see [Create assessments from assessment templates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/create-assessments.md).

## Users respond to the assessments

From the **Source-to-Pay Workspace**:

Supplier managers and owners see the assessments assigned to them under **My work** &gt; **Open assessments** and respond to them in the workspace.

From the **Supplier Collaboration Portal**:

Supplier contacts see the assessments assigned to them under **My active items** and respond to them in the portal.

-   **[Create assessment template from Assessment Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/create-assessment-template-from-assessment-workspace.md)**  
You can create smart assessment templates and add instructions, questions, and reference information by using the template designer in the Smart Assessment Engine application.
-   **[Configure user criteria for reassigning assessments](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/configure-user-criteria-for-reassigning-assessments.md)**  
You can configure the user criteria for reassigning assessments to restrict reassignment within the organization.
-   **[Map assessment template with segmentation rule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/add-assessment-template-in-segmentation-rule.md)**  
You can map assessment templates with segmentation rules in the Source-to-Pay workspace. A rule defines which suppliers receive assessments based on the configured criteria.
-   **[Create assessments from assessment templates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/create-assessments.md)**  
After mapping the assessment templates with segmentation rules, supplier managers manually trigger batch creation of assessments.

**Parent Topic:**[Configure Supplier Lifecycle Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/config-supp-mgmt.md)

**Related topics**  


[Install Supplier Case Management]()

[Install Supplier Collaboration Portal]()

[Install Supplier Operations]()

[Install Supplier Payment Optimization]()

[Supplier Document Management]()

[Configure the document template for the Sign document action type for supplier task]()

[Advanced Work Assignment for Supplier Lifecycle Operations]()

[Enable M2M mapping between supplier contact and suppliers]()

[Configure Supplier Relationship and Performance Management]()

[Install Universal Request for SLO]()

[Smart Assessment Engine](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/smart-asmnt-engine-landing-page.md)

[Create an assessment template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/sae-asmnt-template-create.md)


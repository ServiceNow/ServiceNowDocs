---
title: Create assessment template from Assessment Workspace
description: You can create smart assessment templates and add instructions, questions, and reference information by using the template designer in the Smart Assessment Engine application.
locale: en-US
release: australia
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure smart assessments, Configure, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Create assessment template from Assessment Workspace

You can create smart assessment templates and add instructions, questions, and reference information by using the template designer in the Smart Assessment Engine application.

## Before you begin

Smart assessments are built using the ServiceNow® Smart Assessment Engine \(SAE\) application. Familiarize yourself with the [Smart Assessment Engine](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/smart-assessment-engine/smart-asmnt-engine-landing-page.md).

Role required: sn\_slm.manager or sn\_slm.admin

## Procedure

1.  Select the **Workspaces** tab and then select the **Assessment workspace**.

    For more information on creating the smart assessment template, see [Create an assessment template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/smart-assessment-engine/sae-asmnt-template-create.md).

2.  In the **Purpose** field on the **Smart assessment template** form, select **Supplier management surveys**.

3.  In the **Assessment target** field, select the following target tables:

    -   Supplier \[sn\_fin\_supplier\] table
    -   Segmentation rule assessment template relationship \[sn\_slm\_segmentation\_rule\_m2m\_asmt\_template\] table
4.  Select **Create**.

5.  In the template designer, add instructions and questions.

    For more information, see [Add instructions and questions to an assessment template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/smart-assessment-engine/sae-asmnt-template-populate.md).


## What to do next

Configure the user criteria to restrict the reassignment of assessments from one contact to another within the organization.

**Parent Topic:**[Configure smart assessments](configure-smart-assessments.md)


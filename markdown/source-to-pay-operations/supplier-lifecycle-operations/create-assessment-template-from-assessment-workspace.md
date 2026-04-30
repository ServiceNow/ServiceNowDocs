---
title: Create assessment template from Assessment Workspace
description: You can create smart assessment templates and add instructions, questions, and reference information by using the template designer in the Smart Assessment Engine application.
locale: en-US
release: zurich
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: task
last_updated: "2026-02-22"
reading_time_minutes: 1
breadcrumb: [Configure smart assessments, Configure, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Create assessment template from Assessment Workspace

You can create smart assessment templates and add instructions, questions, and reference information by using the template designer in the Smart Assessment Engine application.

## Before you begin

Smart assessments are built using the ServiceNow® Smart Assessment Engine \(SAE\) application. Familiarize yourself with the [Smart Assessment Engine](https://www.servicenow.com/docs/access?context=smart-asmnt-engine-landing-page&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US).

Role required: sn\_slm.manager or sn\_slm.admin

## Procedure

1.  Select the **Workspaces** tab and then select the **Assessment workspace**.

    For more information on creating the smart assessment template, see [Create an assessment template](https://www.servicenow.com/docs/access?context=sae-asmnt-template-create&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US).

2.  In the **Purpose** field on the **Smart assessment template** form, select **Supplier management surveys**.

3.  In the **Assessment target** field, select the following target tables:

    -   Supplier \[sn\_fin\_supplier\] table
    -   Segmentation rule assessment template relationship \[sn\_slm\_segmentation\_rule\_m2m\_asmt\_template\] table
4.  Select **Create**.

5.  In the template designer, add instructions and questions.

    For more information, see [Add instructions and questions to an assessment template](https://www.servicenow.com/docs/access?context=sae-asmnt-template-populate&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US).


## What to do next

Configure the user criteria to restrict the reassignment of assessments from one contact to another within the organization.

**Parent Topic:**[Configure smart assessments](configure-smart-assessments.md)


---
title: Configure the smart assessment template for safety inspections and audits
description: You can create smart assessment templates and add instructions, questions, and reference information by using the template designer in the Smart Assessment Engine application.
locale: en-US
release: australia
product: Health and Safety Risk Management
classification: health-and-safety-risk-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure, Health and Safety Risk Management, Health and Safety, Employee Service Management]
---

# Configure the smart assessment template for safety inspections and audits

You can create smart assessment templates and add instructions, questions, and reference information by using the template designer in the Smart Assessment Engine application.

## Before you begin

-   Smart assessments are built using the ServiceNow® Smart Assessment Engine \(SAE\) application. Familiarize yourself with the [Smart Assessment Engine](https://www.servicenow.com/docs/access?context=smart-asmnt-engine-landing-page&version=australia&pubname=australia-governance-risk-compliance&ft:locale=en-US).
-   Verify that the application scope is selected as Health and Safety Risk Management. For more information, see [Application picker](https://www.servicenow.com/docs/access?context=c_ApplicationPicker&version=australia&pubname=australia-application-development&ft:locale=en-US).

Role required: sn\_hs\_rm.safety\_inspection\_manager or sn\_hs\_rm.safety\_audit\_manager

## About this task

You can also convert your existing Survey templates related to Health and Safety into Smart Assessment templates using the Smart Assessment Engine migration tool. For more information, see [Creating an assessment template from legacy assessment metric types](https://www.servicenow.com/docs/access?context=sae-asmnt-template-migrating&version=australia&pubname=australia-governance-risk-compliance&ft:locale=en-US).

## Procedure

1.  Navigate to **All** &gt; **Health and Safety** &gt; **Health and Safety Workspace**.

2.  Select the **Workspaces** tab and then select the **Assessment workspace**.

    For more information on creating the smart assessment template, see [Create an assessment template](https://www.servicenow.com/docs/access?context=sae-asmnt-template-create&version=australia&pubname=australia-governance-risk-compliance&ft:locale=en-US).

3.  In the **Purpose** field on the **Smart assessment template** form, select **Health and Safety**.

    You can also configure a category role for a specific purpose. For more information, see [Create an assessment template category](https://www.servicenow.com/docs/access?context=sae-asmnt-template-category-create&version=australia&pubname=australia-governance-risk-compliance&ft:locale=en-US).

4.  In the **Assessment target** field, select the target table where this smart assessment is needed.

    -   For smart assessment for inspections, select the Inspection \[sn\_hs\_rm\_inspection\] table
    -   For smart assessment for audits, select the Audit survey \[sn\_hs\_rm\_audit\_survey\] table.
5.  Select **Create**.

6.  In the template designer, add instructions and questions.

    For more information, see [Add instructions and questions to an assessment template](https://www.servicenow.com/docs/access?context=sae-asmnt-template-populate&version=australia&pubname=australia-governance-risk-compliance&ft:locale=en-US).

7.  In the template designer, add the assessment role to access the smart assessment.

    1.  Select the **General** tab and then select **Settings**.

    2.  In the **Assessment reader role** field, select \[sn\_smart\_asmt.assessment\_reader\] role or any role that contains this role.

        **Important:** Only the role selected here can access the smart assessments that uses this template. This role can complete the smart assessment, assign it, and create actions or findings for the smart assessment questionnaire.


## What to do next

You can configure which question in the smart assessment should have action creation enabled. For more information, see [Configure creating actions from smart assessment questionnaire](hs-configure-property-smart-assessment-action-creation.md).

**Parent Topic:**[Setting up Health and Safety Risk Management](../concept/hs-setting-up-risk-mgmt.md)


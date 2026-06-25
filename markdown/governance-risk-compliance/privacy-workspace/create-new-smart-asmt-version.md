---
title: Create a version of a privacy assessment template
description: Publish a new version of a smart assessment template to revise its questionnaire, response options, or automations. Each version maintains a change history of templates used in privacy screening, impact, and breach assessments.
locale: en-us
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/privacy-workspace/create-new-smart-asmt-version.html
release: australia
product: Privacy Workspace
classification: privacy-workspace
topic_type: task
last_updated: "2026-05-14"
reading_time_minutes: 2
keywords: [template versioning, publish template, smart assessment, Smart Assessment Engine, retire template]
breadcrumb: [Configure, Privacy Management, Governance, Risk, and Compliance]
---

# Create a version of a privacy assessment template

Publish a new version of a smart assessment template to revise its questionnaire, response options, or automations. Each version maintains a change history of templates used in privacy screening, impact, and breach assessments.

## Before you begin

Application scope: **GRC: Privacy Management**

**Note:** To revise the privacy breach assessment template used in privacy cases, change the application scope to **GRC: Privacy Case Management**.

Role required: sn\_privacy.admin or sn\_privacy\_case.privacy\_case\_admin

## About this task

When you need to change the questionnaire, response options, or automations on a privacy assessment, publish a new version of the template instead of overwriting the existing one. Each version of the assessment template is saved as a distinct record, maintaining a change history. Only one version can be published at a time, so all new assessments use the same questionnaire.

Privacy assessments that are already in **Draft**, **Assigned**, or **Work in progress** states continue to use the version they were created with. Only new assessments use the latest published version.

**Note:** When you publish a new version, the previously published version moves to **Retired** and can't be used to send new assessments.

## Procedure

1.  Navigate to **Assessment Workspace** &gt; **Assessment templates**.

    The **Assessment templates** list shows each template with its current **Version** number and **Published** state.

2.  Open the published template you want to revise.

3.  Select the Options icon \[Omitted image "more-actions-vertical-icon.png"\], and select **Create new version**.

4.  Select **Create**.

    The template opens in **Draft** state with the new version number.

5.  Edit the fields on the **General**, **Questions**, and **Automations** tabs.

    **Note:** Publishing a new version doesn't activate previous automations. After you publish, activate all required automations on the new version.

6.  Select **Save**.

7.  When the draft is ready, select **Publish**.

    **Note:** Until you publish, the current published version remains active.

8.  In the **Publish template** dialog, select **Publish**.

    A dialog appears confirming that the new version is active. The new version moves to **Published** state. The previous version moves to **Retired** state and can’t be used to send new assessments.


## Result

The new template version is the only version available for sending new privacy assessments. In the Privacy Workspace, the version is recorded on each new assessment, and on the revised assessment template configuration record.

**Parent Topic:**[Configuring Privacy Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/privacy-workspace/configure-privacy-mgmt.md)

**Related topics**  


[Configure smart assessment templates for screening assessments](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/privacy-workspace/configure-a-smart-assessment-template.md)

[Smart assessments in Privacy Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/privacy-workspace/smart-assessments-in-privacy-management.md)


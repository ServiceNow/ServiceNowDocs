---
title: Update a privacy assessment template
description: Publish a new version of a smart assessment template to revise its questionnaire, response options, or automations. Each version maintains a change history of templates used in privacy screening, impact, and breach assessments.
locale: en-us
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/privacy-workspace/create-new-smart-asmt-version.html
release: australia
product: Privacy Workspace
classification: privacy-workspace
topic_type: task
last_updated: "2026-05-14"
reading_time_minutes: 1
keywords: [template versioning, publish template, smart assessment, Smart Assessment Engine, retire template]
breadcrumb: [Configure, Privacy Management, Governance, Risk, and Compliance]
---

# Update a privacy assessment template

Publish a new version of a smart assessment template to revise its questionnaire, response options, or automations. Each version maintains a change history of templates used in privacy screening, impact, and breach assessments.

## Before you begin

Role required: sn\_privacy.admin or sn\_privacy\_case.privacy\_case\_admin

## About this task

Only one version can be published at a time, so all new assessments use the same questionnaire. Only new assessments use the latest published version.

## Procedure

1.  In the menu bar, select the application scope icon \[Omitted image "application-scope-globe-icon.png"\] Alt text: and verify that you are in the GRC: Privacy Management scope.

2.  Navigate to **Workspaces** &gt; **Assessment Workspace**.

3.  Open the published template you want to revise.

4.  Select the Options icon \[Omitted image "more-actions-vertical-icon.png"\], and select **Create new version**.

5.  Select **Create**.

    The template opens in **Draft** state with a new version number.

6.  Edit the **General**, **Questions**, and **Automations** sections.

    For details about each section, see [Types of assessment templates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/privacy-workspace/smart-assessments-in-privacy-management.md).

    **Note:** Publishing a new version doesn't activate previous automations. After you publish, activate all required automations on the new version.

7.  Select **Save**.

8.  When the draft is ready, select **Publish**.

    **Note:** Until you publish, the current published version remains active.

9.  In the **Publish template** dialog, select **Publish**.

    A dialog appears confirming that the new version is active. The new version moves to **Published** state. The previous version moves to the Retired state and can’t be used to send new assessments.


## Result

The new template version is the only version available for sending new privacy assessments. In the Privacy Workspace, the version is recorded on each new assessment, and on the revised assessment template configuration record.

**Parent Topic:**[Configuring Privacy Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/privacy-workspace/configure-privacy-mgmt.md)


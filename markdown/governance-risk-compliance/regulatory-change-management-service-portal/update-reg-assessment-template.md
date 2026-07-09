---
title: Update a regulatory assessment template
description: Publish a new version of assessment templates in Regulatory Change Management \(RCM\) to revise its questionnaire and response options. Each version maintains a change history of the templates used in regulatory assessments.
locale: en-us
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/regulatory-change-management-service-portal/update-reg-assessment-template.html
release: australia
product: Regulatory Change Management Service Portal
classification: regulatory-change-management-service-portal
topic_type: task
last_updated: "2026-05-14"
reading_time_minutes: 1
keywords: [template versioning, publish template, smart assessment, Smart Assessment Engine, retire template]
breadcrumb: [Manage regulatory tasks, Regulatory Change Management, Governance, Risk, and Compliance]
---

# Update a regulatory assessment template

Publish a new version of assessment templates in Regulatory Change Management \(RCM\) to revise its questionnaire and response options. Each version maintains a change history of the templates used in regulatory assessments.

## Before you begin

Role required: sn\_grc\_reg\_change.admin

## About this task

Only one version can be **Published** at a time, so all new assessments use the same questionnaire. In-progress assessments continue to use the version they were created with, while new assessments use the latest published version. When you publish a new version, the previous version moves to Retired state and can no longer be used for new assessments.

## Procedure

1.  In the menu bar, select the application scope icon\[Omitted image "application-scope-globe-icon.png"\], and verify that you are in the GRC: Regulatory Change Management scope.

2.  Navigate to **Workspaces** &gt; **Assessment Workspace**.

3.  From the Assessment templates list, open the published template you want to revise.

4.  Select the **Options** icon \[Omitted image "more-actions-vertical-icon.png"\], and select **Create new version**.

    Templates that aren't currently in use for any assessment don't display the **Create new version** option. You can edit these templates in their current version.

5.  Select **Create**.

    The template opens in **Draft** state with a new version number.

6.  Edit the template.

7.  Select **Save**.

    The saved template appears in the Assessment templates list with the new version number and remains inactive until it's published. You can return to it and make changes before publishing.

8.  When the new version of the template is ready, select **Publish**.

9.  In the **Publish template** dialog, select **Publish**.

    A confirmation message appears indicating the new version is Published and active. The previous version automatically transitions to Retired state and can't be used to send new assessments.


## Result

Any new assessment sent to the assessor uses the latest published version of the template.

**Related topics**  


[Assess the impact of a regulatory event alert](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/regulatory-change-management-service-portal/assess-impact-of-reg-change-using-ws.md)


---
title: Create a Smart Assessment template version
description: Smart Assessment questionnaire templates can be edited even after they are published and triggered for a work order task. When a new version of the template is published, the previous version moves to a retired state and future versions are generated from the latest version, without affecting in-progress and completed questionnaires.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/field-service-management/mobile-experience-for-field-service-management-glide-family/create-new-template-version.html
release: australia
product: Mobile Experience for Field Service Management \(Glide Family\)
classification: mobile-experience-for-field-service-management-glide-family
topic_type: task
last_updated: "2026-05-18"
reading_time_minutes: 1
breadcrumb: [Author and publish a Smart Assessment template, Configuring Smart Assessment from new templates, Set up Smart Assessment questionnaires, Setting up Field Service Mobile Agent, Configure, Field Service Management]
---

# Create a Smart Assessment template version

Smart Assessment questionnaire templates can be edited even after they are published and triggered for a work order task. When a new version of the template is published, the previous version moves to a retired state and future versions are generated from the latest version, without affecting in-progress and completed questionnaires.

## Before you begin

Ensure that a previous version of the questionnaire exists.

Role required: questionnaire\_admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Assessment Workspace**.

2.  Select the template to edit.

3.  After the template details are displayed, select the More icon.

4.  Select the **Create new version** option.

5.  Select **Create** in the confirmation message.

    The current draft version of the template, such as Version 2, is displayed alongside the template name.

6.  Make the required changes in the questionnaire template.

7.  Select **Save** to save the changes.

8.  Publish the latest version by selecting **Publish**.

9.  Select **Publish** in the Publish template confirmation message.

10. To retain an assessment generated in a previous version, configure the inflight assessment handling setting.

    1.  Navigate to **All** &gt; **Smart Assessment Engine** &gt; **Administration** &gt; **Template Categories**.

    2.  Select the **Field Service** template category.

    3.  Select the **General settings** panel.

    4.  Select **Retain** in the **Inflight assessment handling on version retirement** field.

    5.  Select **Update** to save the changes in the template category.

    After this configuration is enabled, template changes apply only when a new assessment is generated.


## Result

The latest version of the Smart Assessment template is published and the previous version moves to the retired state.


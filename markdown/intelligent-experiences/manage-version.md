---
title: Manage version
description: Manage the version of the model providers across skills and instance levels. You can change and update versions for the out-of-box and custom skills.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-10-24"
reading_time_minutes: 2
breadcrumb: [Manage AI models, Now Assist Admin Settings, Exploring Now Assist Admin, Now Assist, Enable AI experiences]
---

# Manage version

Manage the version of the model providers across skills and instance levels. You can change and update versions for the out-of-box and custom skills.

## Before you begin

Role required: admin

See [Default and target model version](../reference/default-and-target-model-model-version.md) to know more about default and target model versions.

## Procedure

1.  Navigate to **All** &gt; **Now Assist Admin**.

2.  Navigate to **Settings** &gt; **Manage AI models**.

3.  Select **Manage model version**.

4.  View the summary of the active, deprecated, retiring model versions, and recommended actions, providing effective version management system to the admins.

    **Note:** A model version will not be available for selection as target model version, if it is in deprecated, retired, in review or rejected state.

5.  Identify your use case and key factors to choose the model that best fits your needs.

    ![Manage model versions](../image/na-admin-manage-versions-instance.png)

6.  View or update the model version instantly under the **Overview** tab.

7.  You can edit the model provider version for out-of-box or custom skills for the instance or customize it to update it at the skill or skill group level, under the respective tabs.

    Customizing the model version for skills replaces the instance-level model version currently assigned to each provider. This action is typically reserved for specific situations.

8.  Select **Instance level configuration** to manage the model provider version for the skill across the instance.

    ![Manage version at instance level](../image/na-admin-manage-versions-instance-level.png)

    1.  Select **Out-of-box skills** to set the target model version against the current version of the applicable model providers, for the default skills.

    2.  Select **Custom skills** to set the target model version against the current version of the applicable model providers, for the custom skills.

    3.  Select **Save and activate** to update your changes.

    4.  Select **Update model version** to override ServiceNow shipped mappings or create a new default and target model versions mapping.

9.  Select **Skills** to manage the model provider version at the skill level.

    ![Manage version at skill level](../image/na-admin-manage-versions-skill-level.png)

    1.  Search or select the skills you wish to refresh the model version for, and the applicable model provider.

    2.  Select the default and the target model provider version.

    3.  Select **Save and activate** to update your changes.

    4.  Select **Update model version for skills** to override ServiceNow shipped mappings or create a new default and target model versions mapping, at the skill level.


**Parent Topic:**[Manage AI models](manage-large-language-models.md)


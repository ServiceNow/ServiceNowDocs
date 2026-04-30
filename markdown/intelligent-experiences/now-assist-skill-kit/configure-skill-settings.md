---
title: Configure skill deployment settings
description: Configure the deployment settings for the skill that you create. The deployment settings enable you to choose where the admin can find the skill in Now Assist Admin.
locale: en-US
release: zurich
product: Now Assist Skill Kit
classification: now-assist-skill-kit
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configuring Now Assist Skill Kit, Now Assist Skill Kit, Enable AI experiences]
---

# Configure skill deployment settings

Configure the deployment settings for the skill that you create. The deployment settings enable you to choose where the admin can find the skill in Now Assist Admin.

## Before you begin

Role required: sn\_skill\_builder.admin

## Procedure

1.  Navigate to **All** &gt; **Now Assist Skill Kit** &gt; **Home**.

2.  Select the skill that you want to configure.

3.  Select the **Skill settings** tab.

4.  Select **General information**.

    This section shows the information that you added when you created the skill. You can edit the skill name and description here.

5.  Select **Deployment Settings**.

    ![Deployment Settings page for Now Assist Skill Kit.](../image/nask-deploy-settings.png)

6.  On the form, fill in the fields.

<table id="table_qfd_3nh_lcc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Workflow

</td><td>

The high-level category that this skill pertains to, such as**Technology**, **Employee**, **Creator**, or **Platform**. You can also select **Other** if none of the categories fit.

 The workflow that you choose is where the skill appears in the Now Assist Admin console.

</td></tr><tr><td>

Product

</td><td>

The specific product that this skill operates within, such as ITSM, ITOM, HR Service Delivery, Now Assist Admin.

</td></tr><tr><td>

Feature

</td><td>

The feature that the skill is used on, such as Agent Chat, Knowledge, Virtual Agent. You can also define a custom feature if necessary.

</td></tr><tr><td>

Name

</td><td>

The name of the feature.

</td></tr><tr><td>

Description

</td><td>

A description of the feature.

</td></tr></tbody>
</table>7.  Select where you want the admin to enable the skill from.

    -   Now Assist Panel
    -   UI Action
    -   Flow action
    -   Now Assist context menu
    -   Virtual assistant

        For more information about Now Assist in Virtual Agent, see [Configuring assistants overview](https://www.servicenow.com/docs/access?context=configure-now-assist-va&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US).

    -   UI Builder
8.  Select **Save**.


## What to do next

After you configure the skill settings, you can publish your skill. To learn more about publishing skills, see [Finalize and publish a skill](publish-skill.md)

-   **[Example deployment with Workflow Studio](../concept/example-deployment-flow-designer.md)**  
As an AI developer, you can deploy custom skills with many integrations, including Workflow Studio.

**Parent Topic:**[Configuring Now Assist Skill Kit](../concept/configuring-now-assist-skill-kit.md)

**Related topics**  


[Configure a skill prompt](configure-skill-prompt.md)

[Configure security controls for a skill](nask-access-control.md)


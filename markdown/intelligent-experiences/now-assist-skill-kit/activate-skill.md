---
title: Activate a skill
description: After you publish a skill, a Now Assist admin must activate it in Now Assist Admin. Activating the skill makes it available for users to trigger within the platform.
locale: en-US
release: australia
product: Now Assist Skill Kit
classification: now-assist-skill-kit
topic_type: task
last_updated: "2026-04-21"
reading_time_minutes: 3
breadcrumb: [Using Now Assist Skill Kit, Now Assist Skill Kit, Enable AI experiences]
---

# Activate a skill

After you publish a skill, a Now Assist admin must activate it in Now Assist Admin. Activating the skill makes it available for users to trigger within the platform.

## Before you begin

Role required: admin

## About this task

Published custom skills appear in Now Assist Admin under the **Now Assist Skills** tab. Skills are organized in the left sidebar by the **Workflow** value selected during deployment settings configuration. Within each workflow category, skills are grouped by **Product**. Custom skills that use **Other** as their workflow value appear under **Other** at the bottom of the sidebar.

A published skill appears on the **Available** tab with a **Not started** state badge until it is activated. After activation it moves to the **Active** tab.

**Important:** Make sure you are in the correct application scope before you activate the skill. To learn more about application scopes, see [Application scope](https://www.servicenow.com/docs/access?context=c_ApplicationScope&version=australia&pubname=australia-application-development&ft:locale=en-US).

**Note:** Some skills might need to be reviewed and approved by a data steward before you can activate them.

## Procedure

1.  Navigate to **All** &gt; **Now Assist Admin**.

2.  Select the **Now Assist Skills** tab.

3.  In the sidebar, select the workflow category that matches the **Workflow** value you configured in the skill's deployment settings.

    If you selected **Other** as the workflow value, select **Other** at the bottom of the sidebar.

4.  Select the **Available** tab and find your custom skill.

    Custom skills are identified by the **Custom** badge on their skill card.

5.  Select **Activate skill**.

    Activating a custom skill opens a three-step wizard.

6.  On the first step, configure any skill-specific input parameters and select **Save and continue**.

    The fields shown depend on the inputs configured for the skill. This step allows the admin to set default values for the skill's inputs before it goes live.

7.  On the **Define access** step, review or update the access control list \(ACL\) and role restrictions, then select **Save and continue**.

    The ACL determines which users can invoke the skill. The ACL configured here reflects the user access settings defined when the skill was created or last edited in Now Assist Skill Kit. To learn more about skill ACLs and role restrictions, see .

8.  On the **Review and activate** step, review the configuration and select **Activate**.


## What to do next

After activation, the skill moves to the **Active** tab in Now Assist Admin. Users can now trigger the skill from the deployment locations you configured in the skill's deployment settings.

You can enable Now Assist Guardian for your skills. To learn more about Now Assist Guardian, see .

**Parent Topic:**[Using Now Assist Skill Kit](../concept/using-now-assist-skill-kit.md)

**Related topics**  


[Create a skill](create-new-skill.md)

[Create a prompt](create-prompt-template.md)

[Use prompt assistance](use-prompt-assistance.md)

[Test a prompt](test-prompt-template.md)

[Evaluate a prompt](evaluate-prompt.md)

[Finalize and publish a skill](publish-skill.md)

[Call a custom skill from a script](call-custom-skill-from-script.md)


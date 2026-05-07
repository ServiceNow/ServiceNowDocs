---
title: Finalize and publish a skill
description: When you're satisfied with your skill's prompts and configuration, finalize the prompt and publish the skill to make it available for a Now Assist admin to activate.
locale: en-US
release: australia
product: Now Assist Skill Kit
classification: now-assist-skill-kit
topic_type: task
last_updated: "2026-04-21"
reading_time_minutes: 3
keywords: [publish, finalize, Now Assist Skill Kit]
breadcrumb: [Using Now Assist Skill Kit, Now Assist Skill Kit, Enable AI experiences]
---

# Finalize and publish a skill

When you're satisfied with your skill's prompts and configuration, finalize the prompt and publish the skill to make it available for a Now Assist admin to activate.

## Before you begin

Role required: sn\_skill\_builder.admin

## About this task

Publishing a skill is a two-part process. First, you must finalize at least one prompt. Finalizing a prompt marks it as ready for use and is required before the skill can be published. Then you publish the skill, it's state changes from **Draft** to **Published**. It also makes it visible to a Now Assist admin for activation in Now Assist Admin.

**Tip:** Confirm that your deployment settings are configured before publishing. Once published, the skill appears in Now Assist Admin under the workflow category you selected. To learn more, see [Configure skill deployment settings](configure-skill-settings.md).

## Procedure

1.  Navigate to **All** &gt; **Now Assist Skill Kit** &gt; **Home**.

2.  Select the skill that you want to publish.

3.  Make any necessary changes to the prompt.

    Always test after making changes to your prompts. Learn more about testing your prompt at [Test a prompt](test-prompt-template.md).

4.  In the **Skill contents** sidebar, select the prompt that you want to finalize.

5.  Select the lock icon \(**Finalize prompt**\) next to the prompt name to finalize the prompt.

    The lock icon is located in the prompt editor header, adjacent to the **Manage prompt** button. Select the icon to mark the prompt as finalized, and removes the lock icon from view. You must finalize at least one prompt before you can publish the skill.

    **Note:** If you edit a finalized prompt, you must finalize it again before republishing.

6.  Select **Publish skill**.

    The skill status changes from **Draft** to **Published**. The skill is now visible in Now Assist Admin and ready for an admin to activate.


## What to do next

A Now Assist admin must activate the skill before users can trigger it. To learn more about activating a skill, see [Activate a skill](activate-skill.md).

**Parent Topic:**[Using Now Assist Skill Kit](../concept/using-now-assist-skill-kit.md)

**Related topics**  


[Create a skill](create-new-skill.md)

[Create a prompt](create-prompt-template.md)

[Use prompt assistance](use-prompt-assistance.md)

[Test a prompt](test-prompt-template.md)

[Evaluate a prompt](evaluate-prompt.md)

[Activate a skill](activate-skill.md)

[Call a custom skill from a script](call-custom-skill-from-script.md)


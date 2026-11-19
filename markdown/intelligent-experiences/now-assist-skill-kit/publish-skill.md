---
title: Finalize and publish a skill
description: When you’re satisfied with your prompt, you can publish your custom skill. Publishing the skill enables a Now Assist admin to activate it.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/intelligent-experiences/now-assist-skill-kit/publish-skill.html
release: yokohama
product: Now Assist Skill Kit
classification: now-assist-skill-kit
topic_type: task
last_updated: "2026-07-01"
reading_time_minutes: 3
breadcrumb: [Using AI Skill Kit, AI Skill Kit, Enable AI experiences]
---

# Finalize and publish a skill

When you’re satisfied with your prompt, you can publish your custom skill. Publishing the skill enables a Now Assist admin to activate it.

## Before you begin

Role required: sn\_skill\_builder.admin

## About this task

Publishing a skill is a two-part process. First, you must finalize at least one prompt. Finalizing a prompt marks it as ready for use, and is required before the skill can be published. Then you publish the skill, which changes its state from **Draft** to **Published** and makes it visible to a Now Assist admin for activation in AI Admin Hub.

**Tip:** Make sure your deployment settings are configured before publishing. Once published, the skill appears in AI Admin Hub under the workflow category you selected. To learn more, see [Configure skill deployment settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/intelligent-experiences/now-assist-skill-kit/configure-skill-settings.md).

## Procedure

1.  Navigate to **All** &gt; **AI Skill Kit** &gt; **Home**.

2.  Select the skill that you want to publish.

3.  Make any necessary changes to the prompt and test it.

    To learn more about testing your prompt, see [Test a prompt](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/intelligent-experiences/now-assist-skill-kit/test-prompt-template.md).

4.  In the **Skill contents** sidebar, select the prompt that you want to finalize.

5.  Select the lock icon \(**Finalize prompt**\) next to the prompt name to finalize the prompt.

    The lock icon is located in the header row of the prompt editor, to the left of the **Manage prompt** button. Selecting it marks the prompt as finalized and removes the lock icon from view. You must finalize at least one prompt before you can publish the skill.

    **Note:** If you edit a finalized prompt, you must finalize it again before republishing.

6.  Repeat the previous step for any additional prompts you want to finalize.

7.  Select **Publish skill**.

    The skill status changes from **Draft** to **Published**. The skill is now visible in AI Admin Hub and ready for an admin to activate.


## What to do next

A Now Assist admin must activate the skill before users can trigger it. To learn more about activating a skill, see [Activate a skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/intelligent-experiences/now-assist-skill-kit/activate-skill.md).

To create a copy of a published skill to use as a starting point for a new one, see [Clone and edit a ServiceNow skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/intelligent-experiences/now-assist-skill-kit/clone-and-edit-servicenow-skill.md).

To set a prompt as the default for a skill, use the **Set as the default prompt** toggle in the prompt editor. To learn more about managing prompts, see [Create a prompt](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/intelligent-experiences/now-assist-skill-kit/create-prompt-template.md).

**Parent Topic:**[Using AI Skill Kit](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/intelligent-experiences/now-assist-skill-kit/using-now-assist-skill-kit.md)

**Related topics**  


[Create a skill]()

[Create a prompt]()

[Use prompt assistance]()

[Test a prompt]()

[Evaluate a prompt]()

[Activate a skill]()

[Call a custom skill from a script]()


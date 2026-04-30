---
title: Configure a skill prompt
description: Configure your skill prompt to set the model that is used and the randomness and creativity of the response.
locale: en-US
release: xanadu
product: Now Assist Skill Kit
classification: now-assist-skill-kit
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring Now Assist Skill Kit, Now Assist Skill Kit, Enable AI experiences]
---

# Configure a skill prompt

Configure your skill prompt to set the model that is used and the randomness and creativity of the response.

## Before you begin

Role required: sn\_skill\_builder.admin

## Procedure

1.  Navigate to **All** &gt; **Now Assist Skill Kit** &gt; **Home**.

2.  Select the skill that you want to configure.

3.  Select **Configurations**.

    ![Configuration panel for the Now Assist Skill Kit prompt.](../image/nask-configurations.png)

4.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Model|The model is the large language model \(LLM\) that you want to use for the prompt.|
    |Temperature|The temperature determines the randomness and creativity of the output. A higher value increases the randomness. The value must be between 0-1.|
    |Maximum response tokens|The maximum number of tokens the model can return. If you’re using Now LLM Service, the maximum is 1000.|
    |Maximum request tokens|The maximum number of tokens allowed in a request.|

5.  Add **Usage conditions** to determine when to use the prompt.


## What to do next

After you configure your skill settings, you can test your skill. To learn more about testing skills, see [Test a prompt](test-prompt-template.md).

**Parent Topic:**[Configuring Now Assist Skill Kit](../concept/configuring-now-assist-skill-kit.md)

**Related topics**  


[Configure skill deployment settings](configure-skill-settings.md)


---
title: Change the default LLM for playbook generation
description: Choose either the NowLLM/Mixtral model or OpenAI's GPT-4o as the default LLM to generate your playbooks.
locale: en-US
release: zurich
product: Now Assist for Creator
classification: now-assist-for-creator
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, Playbook generation, Now Assist for Creator, Build workflows]
---

# Change the default LLM for playbook generation

Choose either the NowLLM/Mixtral model or OpenAI's GPT-4o as the default LLM to generate your playbooks.

## Before you begin

-   Role required: admin or playbook.admin
-   OpenAI's GPT-4o LLM is not available in the APAC region.

## Procedure

1.  Open the **All** menu.

2.  In the filter bar, type and enter **sys\_one\_extend\_capability.list**.

3.  Search for and select the **Playbook Generation** capability.

4.  Open the **OneExtend Definition Configs** tab.

    The available LLMs are listed here. Under the **Default** column, a value of **true** indicates that the LLM is used to generate playbooks, by default. A value of **false** indicates that the LLM is not used to generate playbooks, by default.

5.  Change the value in the **Default** column to **false** for the current default LLM.

6.  For the LLM that you want to generate playbooks with, change the value in the **Default** column to **true**.


## Result

Your default LLM has been changed.


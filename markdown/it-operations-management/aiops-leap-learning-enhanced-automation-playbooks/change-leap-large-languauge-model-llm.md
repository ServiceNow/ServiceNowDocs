---
title: Change LEAP large language model \(LLM\)
description: LEAP allows you to change the default LLM provider from the Now LLM to your required LLM.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/aiops-leap-learning-enhanced-automation-playbooks/change-leap-large-languauge-model-llm.html
release: zurich
product: AIOps LEAP \(Learning-Enhanced Automation Playbooks\)
classification: aiops-leap-learning-enhanced-automation-playbooks
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Learning Enhanced Automation Platform \(LEAP\), ServiceNow Otto for ITOM, IT Operations Management]
---

# Change LEAP large language model \(LLM\)

LEAP allows you to change the default LLM provider from the Now LLM to your required LLM.

## Before you begin

Role required: admin

## About this task

If you change the LLM model, the LEAP skills should be reapplied to the selected model. Because the LEAP skills aren't applied automatically to an instance.

## Procedure

1.  Access **Admin** &gt; **AI Admin Hub** in your workspace.

2.  Select **Settings** &gt; **Manage AI model** &gt; **Manage model provider**.\[Omitted image "manage-model-provider.png"\] Alt text: Manage model provider

3.  Select **Edit model provider**, and then select **Customize**.\[Omitted image "customize-llm-model-provider.png"\] Alt text: Custom LLM selection

4.  In the Edit model provider section, select **Edit provider for skill groups**, select the skill group as **LEAP** and select required LLM provider.\[Omitted image "select-llm-provider.png"\] Alt text: Select LLM model

5.  Select **Save**.



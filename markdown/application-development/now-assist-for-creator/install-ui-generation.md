---
title: Install UI generation
description: Install the Now Assist for Creator application from the ServiceNow Store to enable UI generation.
locale: en-US
release: australia
product: Now Assist for Creator
classification: now-assist-for-creator
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, UI generation, Use generative AI, Now Assist for Creator, Vibe coding and AI app development on the ServiceNow AI Platform, Building applications]
---

# Install UI generation

Install the Now Assist for Creator application from the ServiceNow® Store to enable UI generation.

## Before you begin

Review the [Now Assist for Creator](https://store.servicenow.com/sn_appstore_store.do#!/store/application/8178fec0ce0431105a7c9305875b2dca) application listing in the [ServiceNow Store](https://store.servicenow.com/store/app/779bebaa1b246a50a85b16db234bcbab) for information on dependencies, licensing or subscription requirements, and release compatibility. Now Assist for Creator installs the Now Assist for UI generation application.

Role required: admin

## Procedure

1.  From the Now Assist for Creator application page on the ServiceNow Store, select **Buy**.

2.  After approval is granted, on your instance, navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

3.  Using the search bar, search for the Now Assist for Creator application \(sn\_now\_creator\).

4.  Select **Install**.

5.  Confirm that Now Assist for Creator is installed:

    1.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Skills**.

    2.  In the workflow list, select **Creator**.

    3.  On the UI Generation card, confirm that the Experience Generation skill is active.

    For more information about Now Assist Admin, see [Now Assist](https://www.servicenow.com/docs/access?context=platform-now-assist-landing&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).


## What to do next

Grant the ui\_builder\_admin role to users who need UI generation access. For more information, see [Grant UI Builder admin role](grant-ui-builder-admin-role.md).

**Note:**

You can use Now LLM Service, Now LLM Long Term Stable models \(LTS\), Azure OpenAI, Google Gemini or Anthropic Claude on AWS as the AI model provider for all Now Assist skills and AI agents. Use the Configuration Controls in [AI Control Tower](https://www.servicenow.com/docs/access?context=ai-model-providers&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US) to define which options are available, then set the skill-level preferences in the [Now Assist Admin console](https://www.servicenow.com/docs/access?context=manage-large-language-models&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US). For more information, see [Large language models on the ServiceNow AI Platform®](https://www.servicenow.com/docs/access?context=exploring-large-language-models&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

**Parent Topic:**[Configuring UI generation](../concept/configuring-ui-generation.md)

**Related topics**  


[Install Now Assist for Creator](../../flow-designer/task/install-now-assist-for-creator.md)


---
title: Enable Dynamic Translation for languages in Virtual Agent
description: Enable Dynamic Translation for one or more languages in Chat Settings for Virtual Agent.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/conversational-interfaces/virtual-agent/enable-dynamic-lang-detection.html
release: zurich
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Localization options for Virtual Agent, Build and deploy, Virtual Agent, Conversational Interfaces]
---

# Enable Dynamic Translation for languages in Virtual Agent

Enable Dynamic Translation for one or more languages in Chat Settings for Virtual Agent.

## Before you begin

Install and configure the plugins for Dynamic Translation, as described in [Prerequisites for using Dynamic Translation in Virtual Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/virtual-agent/prereq-using-dt-va.md). If these prerequisites aren’t completed, the Multi language support card described in the following steps doesn’t appear.

Role required: virtual\_agent\_admin or admin

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Settings**.

2.  Select **Virtual Agent**.

3.  On the Multi language support card, do the following:

    1.  Turn on the **Language Detection** toggle switch to enable it.

        Turning on this toggle is applicable to both NLU and LLM conversations.

    2.  Turn on the **Dynamic language translation** toggle switch to enable it.

        Turning on this toggle is only applicable to NLU conversations. For more information about turning on translation for LLM conversations, see [Configure multilingual service for Now Assist applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/virtual-agent/enable-dynamic-translation-for-now-assist-applications.md).

    3.  Select **View All**.

    The Multi-language support page opens. All languages that are installed on the instance are listed.

4.  In the **Dynamic Translation Enabled** column, select **false** for the language you want to enable.

    \[Omitted image "dtac-language-flag.png"\] Alt text: Virtual Agent Multi-language support page with highlighted false value under Dynamic Translation Enabled.

    1.  If prompted, select **Edit record**.

        \[Omitted image "edit-language-record-link.png"\] Alt text: Banner message with Edit record option highlighted.

    2.  Select **Dynamic Translation Enabled**.

    3.  Select **Update**.

    4.  Return to the Multi-language support page and repeat these steps for any other language you want to enable.

5.  Enable language detection for guest users.

    If this system property is set to **off**, Dynamic Translation will not work for guest users.

    1.  Navigate to **All**, and then enter `sys_properties.list` in the filter.

    2.  In the **Name** field, search for **com.glide.cs.guest\_session\_resumable**.

    3.  In the **Value** column, change the setting to `true`.

        \[Omitted image "sysproperties-dt-guest-session-resumable.png"\] Alt text: System Properties page with com.glide.cs.guest\_session\_resumable value set to true.


**Parent Topic:**[Localization options for Virtual Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/virtual-agent/multi-language-options-va.md)


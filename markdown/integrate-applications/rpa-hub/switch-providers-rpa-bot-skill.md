---
title: Switch to another large language model \(LLM\) provider for the RPA bot generation skill
description: Switch to another large language model \(LLM\) provider when you're using the Robotic Process Automation bot generation skill. That way, you can still get good results and accessibility if Azure isn’t available in your region. In addition to using Now LLM Service \(LLM generic\), you can also use the gpt4o LLM.
locale: en-US
release: xanadu
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
keywords: [Now Assist, generative AI]
breadcrumb: [Configure Now Assist for RPA Hub, Now Assist for RPA Hub, Robotic Process Automation \(RPA\) Hub, Creating integrations with applications]
---

# Switch to another large language model \(LLM\) provider for the RPA bot generation skill

Switch to another large language model \(LLM\) provider when you're using the Robotic Process Automation bot generation skill. That way, you can still get good results and accessibility if Azure isn’t available in your region. In addition to using Now LLM Service \(LLM generic\), you can also use the gpt4o LLM.

## Before you begin

Perform these steps in your ServiceNow instance.

Role required: sn\_skill\_builder.admin

## About this task

The assists for custom LLMs are charged separately.

To switch an LLM provider for the RPA bot generation skill, create a connection record and add its associated credential record. Later, clone the RPA bot generation skill.

## Procedure

1.  Create a connection record and add its associated credential record before you switch the provider.

    1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connections &amp; Credential Aliases**.

    2.  Select the **RPA Custom LLM Credentials** record.

    3.  On the **Connections** tab, select **New**.

    4.  Enter a name for the new connection record.

    5.  In the **Credential** field, select the search icon \(![Search icon](../../../common/image/List_SearchIcon.png)\), select **New**, and then select **Custom Header API Key Credential**.

    6.  On the form, fill in the fields.

<table id="table_ujm_cld_b2c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Human-readable name for this credential.

</td></tr><tr><td>

Header Name

</td><td>

Name of the header to send the API key in.For example, `api-key`.

</td></tr><tr><td>

API Key

</td><td>

API key to be used.

</td></tr></tbody>
</table>    7.  Select **Submit**.

    8.  In the **Connection URL** field, enter the API endpoint that you must add to use your gpt4o model.

        For Azure OpenAI, your Connection URL is in the form `https://{your-resource-name}.openai.azure.com`. For more information, see the [Azure OpenAI documentation](https://learn.microsoft.com/en-us/azure/cognitive-services/openai/reference#completions).

        **Note:** Only the gpt4o LLM is supported.

    9.  Select **Submit**.

2.  Clone the RPA bot generation skill.

    1.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Now Assist Skills**.

    2.  In the workflow list, select **Creator**.

    3.  On the RPA bot generation card, select the three dots icon \(![Vertical three-dots icon.](../image/three-dot-icon-vertical-rpa.png)\) and select **Make a copy**.

        ![RPA bot generation card shows the procedure of cloning the RPA bot generation skill by selecting the three dots next to the skill and selecting the Make a copy option.](../image/clone-rpa-bot-gen-skill.png "Clone RPA bot generation skill")

3.  Switch your provider.

    1.  Navigate to **All** &gt; **Now Assist Skill Kit** &gt; **Home**.

    2.  On the **ServiceNow skills** tab, select a cloned copy of the RPA bot generation skill.

    3.  On the **Skill settings** tab, in the Providers \(Provider API\) section, toggle the Custom LLM switch to make it the default provider.

        ![Providers section that shows the Custom LLM provider and the Make default toggle is selected to make it the default provider.](../image/switch-custom-llm-rpa.png "Toggle the Custom LLM switch")


## Result

You can start using the Now Assist for RPA Hub feature with the gpt4o LLM.


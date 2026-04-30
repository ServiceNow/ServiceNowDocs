---
title: Configure AI Search answers capability for web search
description: AI web search is a OneExtend capability that enables end users to perform web searches and receive AI-powered answers. The capability supports multiple AI providers and integrates with virtual assistants and workflows.
locale: en-US
release: zurich
product: Generative AI Controller
classification: generative-ai-controller
topic_type: task
last_updated: "2025-07-08"
reading_time_minutes: 4
keywords: [AI Search answers, Websearch, Web search]
breadcrumb: [Configuring Generative AI Controller, Generative AI Controller, Now Assist, Enable AI experiences]
---

# Configure AI Search answers capability for web search

AI web search is a OneExtend capability that enables end users to perform web searches and receive AI-powered answers. The capability supports multiple AI providers and integrates with virtual assistants and workflows.

## Before you begin

When web search is turned on, Gemini is the default AI provider. To switch AI providers, admins must configure the AI Search answers OneExtend capability. The instance or skills default AI provider that is set in Now Assist Admin can differ from the web search AI provider. For more information on the default instance or skills AI provider, see [Manage model providers](../../now-assist-admin/task/edit-model-providers.md).

Some of the AI providers require API keys whereas others don’t require API keys because they use OEM. The following table highlights the four AI providers and whether they use API keys or OEM.

<table id="table_nlw_b1y_xfc"><thead><tr><th>

AI providers that require API keys

</th><th>

AI providers that use OEM

</th></tr></thead><tbody><tr><td>

OpenAI

</td><td>

Gemini**Note:** Gemini is the default web search AI provider in the AI Search answers OneExtend capability. If you selected Gemini as the LLM provider in Now Assist Admin and you want to use Gemini as your web search AI provider, you don’t need to configure the AI Search answers OneExtend capability.

</td></tr><tr><td>

Perplexity

</td><td>

Azure**Note:** Azure doesn’t currently support web search.

</td></tr></tbody>
</table>Role required: admin

## Procedure

1.  In the navigator filter, go to the OneExtend Capability list by entering `sys_one_extend_capability.list`.

2.  Search for the `AI Search answers` OneExtend capability.

3.  Select the AI Search answers record.

4.  In the OneExtend Definition Configs related list, view the Default column.

    When the AI provider's Default column is set to `true`, that is the AI search provider used for the web search. Gemini defaults to `true`. To change the AI search provider to an AI provider that requires the use of API keys, such as Perplexity or OpenAI, continue with the following steps.

    **Note:** Although Azure OpenAI answer is an option for an AI search provider, Azure doesn't support web search and should remain set to `false`.

5.  In the OneExtend Capability Definitions related list, select the value in the Connection And Credential Alias column for the AI Search provider you want to use.

    For example, if you want to switch the web search AI provider to OpenAI, select **sn\_openai.OpenAI** from the Connection And Credential Alias column.

    The Connection &amp; Credential Alias form opens. If no connections are available within the Connections related list, you must create a connection.

6.  Complete one of the following actions based on the following scenarios.

<table id="choicetable_qlm_kmw_xfc"><thead><tr><th align="left" id="d32783e220">

Scenario

</th><th align="left" id="d32783e223">

Action required

</th></tr></thead><tbody><tr><td id="d32783e229">

**Connection is available**

</td><td>

If a connection is already available within the Connections related list, continue to the next step.

</td></tr><tr><td id="d32783e238">

**Connection isn’t available and must be created**

</td><td>

1.  Select **New** within the Connections related list to create a connection.
2.  In the **Name** field, enter the connection name.

For example, `Open AI connection`.

**Note:** For more information about the fields on the HTTP\(s\) Connections New record form, see [Create an HTTP\(s\) connection](https://www.servicenow.com/docs/access?context=create-https-connection&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

3.  Select the Lookup using list icon \( ![List lookup icon with magnifying glass.](../image/icon-magnifying-glass-blue.png)\) next to **Credential**.
4.  Select **New** to create a credential for your connection.

**Note:** You may see an existing credential that you can select from the Credentials list, but some AI providers, like OpenAI, do not come with default credentials.

5.  Select **API Key Credentials**.
6.  Enter a name in the **Name** field.

For example, `Open AI key`.

7.  Enter the API key in the **API key** field.

**Note:** For more information about the fields on the API Key Credentials New record form, see [API key credentials](https://www.servicenow.com/docs/access?context=API-key-credential-form&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

8.  Select **Submit**.

You’re redirected back to the HTTP\(s\) Connections new record form.

9.  Enter the connection URL in the **Connection URL** field.

For example, enter `https://api.openai.com` for Open AI.

10. Select **Submit**.


</td></tr></tbody>
</table>    1.  In the OneExtend Definition Configs related list, set the existing default AI provider from `true` to `false`.

    2.  In the OneExtend Definition Configs related list, set the AI provider that you want to use from `false` to `true`.

7.  Select **Update**.

    The AI provider for web search is now updated.


## Result

End users can now perform an internet search to answer a query whenever in web search mode. For more information about web search mode for end users, see [Web search](https://www.servicenow.com/docs/access?context=web-search-requestor&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US).

## What to do next

If you switched the AI provider to Perplexity, you must work with the **sn\_ai\_websearch.perplexity\_model\_name** system property. For more information on this system property, see [Now Assist in Virtual Agent system properties](https://www.servicenow.com/docs/access?context=nava-sys-props&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US).


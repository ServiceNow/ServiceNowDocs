---
title: Configure API credentials for IBM watsonx
description: Configure your API credentials to use IBM watsonx Granite models as your LLM provider for Generative AI Controller capabilities.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/generative-ai-controller/configure-api-credentials-for-ibm-watsonx.html
release: australia
product: Generative AI Controller
classification: generative-ai-controller
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring API credentials for generative AI capabilities, Configuring Generative AI Controller, Generative AI Controller, AI Admin Hub, Enable AI experiences]
---

# Configure API credentials for IBM watsonx

Configure your API credentials to use IBM watsonx Granite models as your LLM provider for Generative AI Controller capabilities.

## Before you begin

To use IBM watsonx large language models \(LLMs\), you must configure your credentials to use the Generative AI Controller capabilities.

Role required: admin

## About this task

To use models with IBM watsonx as your LLM provider for Generative AI Controller capabilities, you must have an active connection configured.

## Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connections &amp; Credential Aliases**.

2.  Open the record named IBM watsonx.

3.  Select the **Create New Connection &amp; Credential** related link.

    \[Omitted image "gai-create-new-connection-ibm.png"\] Alt text: Create New Connection &amp; Credential related link highlighted on the screen.

4.  In the API key field, enter your API key.

    For more information about generating an API key, see IBM's [documentation for generating API keys for authentication](https://www.ibm.com/docs/en/watsonx/watsonxdata/1.1.x?topic=started-generating-api-keys).

5.  Create a connection by selecting **Create**.


## Result

You can now use capabilities labeled with IBM watson as your LLM provider for Generative AI Controller capabilities.

\[Omitted image "gai-created-connection-ibm.png"\] Alt text: Complete connection for IBM watsonx.

## What to do next

If you want to use generative AI capabilities through your MID Server, open the new Connection record, select the **Use MID server** check box, and save the record.

Activate generative AI skills in the AI Admin Hub console for your workflow. For more information, see [AI Admin Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/platform-now-assist-landing.md).


---
title: Reference for Generative AI Controller
description: Reference topics provide information about Generative AI Controller tables, and properties.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/generative-ai-controller/reference-for-generative-ai-controller.html
release: australia
product: Generative AI Controller
classification: generative-ai-controller
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Generative AI Controller, AI Admin Hub, Enable AI experiences]
---

# Reference for Generative AI Controller

Reference topics provide information about Generative AI Controller tables, and properties.

## Tables installed

<table><thead><tr><th>

Name

</th><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

OneExtend Capability

</td><td>

sys\_one\_extend\_capability

</td><td>

Generative AI Controller capabilities for routing and governing generative AI requests for your ServiceNow AI applications.

</td></tr><tr><td>

OneExtend Capability Definition

</td><td>

sys\_one\_extend\_capability\_definition

</td><td>

Attribute configuration for input and output variables for for generative AI capability definitions.

</td></tr><tr><td>

OneExtend Capability Definition Attribute

</td><td>

sys\_one\_extend\_definition\_attribute

</td><td>

Input and output variables for for generative AI capability definitions. Variable names can't be changed if the capability is active and used on the instance. You can check whether a capability is used by going to the OneExtend Usages table.

</td></tr><tr><td>

OneExtend Builder Config

</td><td>

sys\_one\_extend\_builder\_config

</td><td>

Determines which capability and provider is related to each generative AI builder component.

</td></tr><tr><td>

OneExtend Builder Capability

</td><td>

sys\_one\_extend\_builder\_capability

</td><td>

Definitions for a capacity and its provider for builder components.

</td></tr><tr><td>

OneExtend Usage

</td><td>

sys\_one\_extend\_usage

</td><td>

Each usage of a generative AI capability across your Now Assist applications.

</td></tr><tr><td>

Gen AI Log Metadata

</td><td>

sys\_gen\_ai\_log\_metadata

</td><td>

Log data about requests to the LLMs, including information about definition, errors, user, and feedback provided. AI-generated content can be tracked for a duration beyond six months. You can export historical data by writing a script to copy it into a different table without deleting the information.

</td></tr><tr><td>

Generative AI Metric

</td><td>

sys\_generative\_ai\_metric

</td><td>

Logs various metrics to help evaluate the performance and accuracy of LLM responses, such as edit score, edit distance, guardrail activity, and details about the LLM model used.

</td></tr><tr><td>

Gen AI Model Version Mapping

</td><td>

sys\_gen\_ai\_model\_version\_mapping

</td><td>

Maintains mappings between AI model versions, their providers, and configuration details, providing a clear understanding of how source models map to target models. It also includes associated metadata, such as skill type, model type, resource associations, and provider information.

</td></tr><tr><td>

Generative AI Log

</td><td>

sys\_generative\_ai\_log

</td><td>

Logs Generative AI prompts, responses, and edited responses to debug LLM calls. Log records are retained for 180 days.HR-related logs are restricted to HR Administrators, ensuring sensitive information remains protected.

For more information, see [Generative AI Controller tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/generative-ai-controller/generative-ai-controller-tables.md).

</td></tr></tbody>
</table>## Properties

<table><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

com.sn.generative.ai.provider

</td><td>

Default provider when capability definition has no default.Type: choice list

No default value

</td></tr><tr><td>

com.sn.generative.ai.ais.message

</td><td>

Message that is displayed when AI Search fails to find an answer to a query.Type: string

Default value: No answer found.

</td></tr><tr><td>

com.sn.generative.ai.log\_prompt

</td><td>

Prompt that determines whether generative AI API calls are logged.Type: true \| false

Default value: true

</td></tr><tr><td>

com.sn.generative.ai.moderation.message

</td><td>

Message that is displayed if the OpenAI or Azure OpenAI moderation tools identify the content that goes against their terms of service.Type: string

Default value: The response cannot be displayed as it’s deemed inappropriate by OpenAI.

</td></tr><tr><td>

com.glide.one.extend.token.buffer

</td><td>

Buffer that checks the request for the number of tokens before a OneExtend capability is executed. The maximum allowed request tokens are calculated based on the maximum tokens that are permitted by the AI provider's API minus the response token and buffer value that is specified in this system property.Type: integer

Default value: 250

</td></tr><tr><td>

domain.llm.usage.entitled

</td><td>

Determines whether to use the LLM for a specific domain to process data or restrict its use.Type: true \| false

Default value: true

</td></tr></tbody>
</table>## External links

|Provider|Data policy|Usage policy|
|--------|-----------|------------|
|Amazon Bedrock|[Data protection](https://docs.aws.amazon.com/bedrock/latest/userguide/data-protection.html)|[AWS Service Terms](https://aws.amazon.com/service-terms/)|
|Google Cloud|[Google Cloud Platform Terms of Service](https://cloud.google.com/terms)|[Google Cloud Platform Terms of Service](https://cloud.google.com/terms)|
|IBM watsonx|[Keeping your data secure and compliant](https://www.ibm.com/docs/en/watsonx/saas?topic=security-keeping-your-data-secure-compliant)|[Foundation model terms of use in watsonx.ai](https://www.ibm.com/docs/en/watsonx/saas?topic=solutions-terms-use)|
|Microsoft Azure OpenAI|[Data, privacy, and security for Azure OpenAI Service](https://learn.microsoft.com/en-us/legal/cognitive-services/openai/data-privacy)|[Code of conduct for Azure OpenAI Service](https://learn.microsoft.com/en-us/legal/cognitive-services/openai/code-of-conduct)|
|OpenAI|[API data usage policies](https://openai.com/policies/api-data-usage-policies)|[Usage policies](https://openai.com/policies/usage-policies)|


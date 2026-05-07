---
title: Data sharing, Data overflow processing, and Security &amp; privacy in AI Control Tower
description: Explore the Data sharing, Data processing, and Security &amp; privacy sections.
locale: en-US
release: australia
product: AI Control Tower
classification: ai-control-tower
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
keywords: [Now Assist, generative AI]
breadcrumb: [Configurations, AI Control Tower dashboard, Explore, AI Control Tower, Enable AI experiences]
---

# Data sharing, Data overflow processing, and Security &amp; privacy in AI Control Tower

Explore the Data sharing, Data processing, and Security &amp; privacy sections.

The section focuses on improving AI models, managing datacenter traffic, and enabling metrics to measure the integrity of your data model and monitor potential threats in large language model \(LLM\) input and output.

## Data sharing

By default, Data sharing is active. You can opt out to deactivate AI Control Tower and share your data with ServiceNow to improve AI accuracy, enhance user experiences, and gain a better understanding of business needs.

![Data sharing on the Configurations screen.](../image/aict-data-sharing.png)

Data sharing helps enhance ServiceNow products, but if you choose to opt out of the ServiceNow data sharing program, you’ll no longer be able to contribute data to improve ServiceNow AI products.

For information on data sharing opt-out, see [Opt out of data sharing](https://www.servicenow.com/docs/bundle/zurich-intelligent-experiences/page/administer/now-assist-admin/task/opt-out-of-data-sharing-for-now-assist.html).

## Data overflow processing

By default, all Now Assist traffic is managed within ServiceNow datacenters. If there are traffic spikes, the system automatically redirects to Microsoft Azure datacenters to maintain performance. You can opt out of this feature to keep all Now Assist traffic exclusively within ServiceNow datacenters. By default, data overflow processing is inactive.

**Note:** The Data sharing and Data overflow processing features are available for a sub-prod instance in read-only mode, when Multi-instance setup is configured and active.

## Security &amp; privacy

-   **Data integrity incident detection**

    These configuration settings control the Data integrity incident detection chart, which is designed to help show potential violations of certain LLM guardrail policies in LLM responses. To show data for this chart on the dashboard, select **Configure**, and then select **Active**. If you want to discontinue collecting data for the chart, deselect **Active**.

    **Note:** If you inactivate the chart, past data shows on the chart for 90 days.

    You can configure these settings:

    -   **Categories** – Security and content moderation policies grouped into categories that reflect industry practices that align with [OWASP Top 10 Risk &amp; Mitigations for LLMs and Gen AI Apps](https://genai.owasp.org/llm-top-10/) and the [OpenAI model specification](https://model-spec.openai.com/2025-12-18.html).
    -   **Sampling rate** – The percentage of transactions that are evaluated. Selecting a rate lower than 100% results in fewer AI calls, but potentially less accurate data.
    -   **Max skill calls per execution** – The amount of AI usage per call. The minimum is 10 calls; the default is 1,000 calls. Entering a lower number results in fewer AI calls, but potentially less accurate data.
    -   **Single or multiple analysis** – Single analysis uses the default LLM to determine whether the model's output or behavior violates predefined security policies. Multiple analysis uses the results from three or more LLMs that ServiceNow supports to make a determination, using the majority result from the LLMs. Multiple analysis requires an odd number of LLMs.
-   **Agent goal deviation**

    These configuration settings control the Agent goal deviation chart, which shows when AI agents may be deviating from their intended role or objective. For example, unauthorized actions or prompt injection attempts. To show data for this chart on the dashboard, select **Configure**, and then select **Active**. If you want to discontinue collecting data for the chart, deselect **Active**.

    **Note:** If you inactivate the chart, past data shows on the chart for 90 days. Due to the probabilistic nature of the data model, not all occurrences may be identified.

    You can configure these settings:

    -   **Sampling rate** – The percentage of transactions that are evaluated. Selecting a rate lower than 100% results in fewer AI calls, but potentially less accurate data.
    -   **Max skill calls per execution** – The amount of AI usage per call. The minimum is 10 calls; the default is 1,000 calls. Entering a lower number results in fewer AI calls, but potentially less accurate data.
    -   **Single or multiple analysis** – Single analysis uses the default LLM to determine whether the AI agent's or skill's response diverges from the expected output. Multiple analysis uses the results from 3 or more LLMs to make a determination, using the majority result from the LLMs. Multiple analysis requires an odd number of LLMs.
-   **Output screening**

    These configuration settings control the AI agent output with PII detected and Agentic output injection detection charts, which show when agents' LLM output contains potential PII or potential security-vulnerable patterns. To show data for these charts on the dashboard, select **Configure**, select **Active**, and then select a setting for the data to collect. If you want to discontinue collecting data for the charts, deselect **Active**.

    **Note:** If you inactivate the charts, past data collected shows on the charts for 90 days.

    You can configure these settings:

    -   **Output Security Vulnerability** – Collect and show data in the Agentic output injection detection chart. The data is collected by analyzing LLM output for known potential vulnerable patterns and potential corresponding attack vectors. For example, HTML tags shouldn't have scripts associated with them for cross-site script attacks \(XSS\), or stacked SQL queries could result in SQL injection attacks.
    -   **Output Extended PII** – Collect more potential PII data occurrences and show in the AI agent output with PII detected chart. The data is collected by analyzing LLM output for additional potential PII data patterns beyond those specified in Data Privacy. These PII data patterns include U.S. CA drivers license, U.S. passport number, and vehicle ID number.
    -   **Output PII Violation** – Collect and show data in the AI agent output with PII detected chart. The data is collected by analyzing LLM output for potential PII sensitive data patterns specified in Data Privacy. For example, U.S. phone number or credit card number.
-   **Sensitive data input and anonymization**

    This section shows the data patterns enabled in Data Privacy to detect and anonymize information in LLM prompts. Use this view as a quick reference when troubleshooting Sensitive data detected and Sensitive data anonymized charts. This feature requires the Data privacy plugin to be installed. For more information on how the data is sent and stored, see [User data usage policy for Now Assist](https://www.servicenow.com/docs/bundle/australia-intelligent-experiences/page/administer/now-assist-admin/concept/user-data-usage-policy-now-assist.html).

-   **Score weight**

    This setting controls how the LLM guardrail categories that comprise the score are weighted. You can change the default weights or remove categories from the score by deactivating them. The score formula is an average across all managed AI assets.

    ![AI asset security score configuration with default weights shown.](../image/sp-tab-ai-score-config.png)



---
title: Configure post-runtime security metrics
description: Customize security and content moderation policies, sampling rate, skill call usage limit, LLMs to use, and other settings for the Top AI asset security events metric and others.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/gov-sec-configure-event-metrics.html
release: zurich
topic_type: task
last_updated: "2026-05-02"
reading_time_minutes: 9
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Configure, Managing AI asset security, Govern AI assets, AI Control Tower, Enable AI experiences]
---

# Configure post-runtime security metrics

Customize security and content moderation policies, sampling rate, skill call usage limit, LLMs to use, and other settings for the Top AI asset security events metric and others.

## Before you begin

Role required: AI steward \[sn\_ai\_governance\_ai\_steward\]

Security and content moderation policies are grouped into LLM guardrail categories that reflect industry practices that align with [OWASP Top 10 Risk &amp; Mitigations for LLMs and Gen AI Apps](https://genai.owasp.org/llm-top-10/) and the [OpenAI model specification](https://model-spec.openai.com/2025-12-18.html). These categories are reflected in the Top AI asset security events metric.

## Procedure

1.  In AI Control Tower, navigate to **Settings** &gt; **Rules and templates** &gt; **Security**.

    **Note:** Alternatively, you can configure these metrics directly in the Post-runtime tab. Navigate to the tab and select **Configure**. The inline metric settings are organized by OWASP threat category, which is slightly different from how they're organized in Settings by LLM guardrail category.

2.  Select the ServiceNow AI systems tab.

3.  Under Data Model Integrity, configure the metrics and select **Save and Close**.

<table><thead><tr><th>

Metric

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Data integrity incident detection

</td><td>

Designed to help show potential violations of certain LLM guardrail policies in LLM responses. To show data for this metric in Top AI asset security events, select **Configure**, and then select **Detection enabled**. **Note:** If you disable the metric, past data shows on the chart for 90 days. AI judge model classifications are probabilistic in nature and may be incomplete or incorrect. They don't constitute professional advice and shouldn't be relied on as the sole basis for assessing risk.

You can configure these settings:-   Categories:
    -   Physical, Chemical, Biological Harmful Content Detection
    -   Guardrail Circumvention Attempt
    -   Untrusted Links Or Downloads
    -   Malware Detection
    -   Over and Under Refusal Detection
    -   Insecure Code Output
    -   Confidential Information Extraction Attempts
    -   Fraud or Deceptive Facilitation
    -   Internal System Instruction Detection
-   **Sampling rate** – The percentage of transactions that are evaluated. Selecting a rate lower than 100% results in fewer AI calls, but potentially less accurate data. Lower sample rates reduce overhead but may not detect all security events. For critical systems, consider using 100%. For balanced coverage, consider using 75% or higher.
-   **Max skill calls per execution** – The amount of AI usage per call, with a minimum of 10 calls and a maximum of 100 calls. The default is 10 calls. Entering a lower number results in fewer AI calls, but potentially less accurate data.
-   **Single or multiple analysis** – Single analysis uses the default LLM to determine whether the model's output or behavior violates predefined security policies. Multiple analysis uses the results from three or more LLMs that ServiceNow supports to make a determination, using the majority result from the LLMs. Multiple analysis requires an odd number of LLMs.


</td></tr><tr><td>

System prompt leakage

</td><td>

System prompt leakage occurs when the model inadvertently reveals its system prompt or configuration instructions to users. To show data for this metric in Top AI asset security events, select **Configure**, and then select **Detection enabled**. **Note:** If you disable the metric, past data shows on the chart for 90 days.

You can configure these settings:-   **Sampling rate** – The percentage of transactions that are evaluated. Selecting a rate lower than 100% results in fewer AI calls, but potentially less accurate data. Lower sample rates reduce overhead but may not detect all security events. For critical systems, consider using 100%. For balanced coverage, consider using 75% or higher.
-   **Max skill calls per execution** – The amount of AI usage per call, with a minimum of 10 calls and a maximum of 100 calls. The default is 10 calls. Entering a lower number results in fewer AI calls, but potentially less accurate data.
-   **Single or multiple analysis** – Single analysis uses the default LLM to determine whether the model's output or behavior violates predefined security policies. Multiple analysis uses the results from three or more LLMs that ServiceNow supports to make a determination, using the majority result from the LLMs. Multiple analysis requires an odd number of LLMs.
For external AI systems, configure the Sampling rate. Configure additional settings in AI Evaluation.

</td></tr><tr><td>

Correctness detection

</td><td>

Correctness measures whether the information provided in the model’s response is factually accurate and logically valid given the prompt and context. To show data for this metric in Top AI asset security events, select **Configure**, and then select **Detection enabled**. **Note:** If you disable the metric, past data shows on the chart for 90 days.

You can configure these settings:-   **Sampling rate** – The percentage of transactions that are evaluated. Selecting a rate lower than 100% results in fewer AI calls, but potentially less accurate data. Lower sample rates reduce overhead but may not detect all security events. For critical systems, consider using 100%. For balanced coverage, consider using 75% or higher.
-   **Max skill calls per execution** – The amount of AI usage per call, with a minimum of 10 calls and a maximum of 100 calls. The default is 10 calls. Entering a lower number results in fewer AI calls, but potentially less accurate data.
-   **Single or multiple analysis** – Single analysis uses the default LLM to determine whether the model's output or behavior violates predefined security policies. Multiple analysis uses the results from three or more LLMs that ServiceNow supports to make a determination, using the majority result from the LLMs. Multiple analysis requires an odd number of LLMs.
For external AI systems, configure the Sampling rate. Configure additional settings in Correctness \(factuality\) in AI Evaluation.

</td></tr></tbody>
</table>4.  Under Threat monitoring, configure the metrics and select **Save and Close**.

<table id="table_h3x_jnw_djc"><thead><tr><th>

Metric

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Prompt injection

</td><td>

Prompt injection attacks occur when malicious input is crafted to override or deviate from the model’s instructions, causing unintended behavior. To show data for this metric in Top AI asset security events, select **Configure**, and then select **Detection enabled**. **Note:** If you disable the metric, past data shows on the chart for 90 days.

You can configure these settings:-   **Sampling rate** – The percentage of transactions that are evaluated. Selecting a rate lower than 100% results in fewer AI calls, but potentially less accurate data. Lower sample rates reduce overhead but may not detect all security events. For critical systems, consider using 100%. For balanced coverage, consider using 75% or higher.
-   **Max skill calls per execution** – The amount of AI usage per call, with a minimum of 10 calls and a maximum of 100 calls. The default is 10 calls. Entering a lower number results in fewer AI calls, but potentially less accurate data.
-   **Single or multiple analysis** – Single analysis uses the default LLM to determine whether the model's output or behavior violates predefined security policies. Multiple analysis uses the results from three or more LLMs that ServiceNow supports to make a determination, using the majority result from the LLMs. Multiple analysis requires an odd number of LLMs.
For external AI systems, configure the Sampling rate. Configure additional settings in Prompt injection in AI Evaluation.

</td></tr><tr><td>

Improper input and output handling

</td><td>

When AI predictions are consumed in workflows without the right potential security vulnerability checks, it can lead to incorrect, unsafe, or biased actions. To show data for this metric in Top AI asset security events, select **Configure**, and then select **Detection enabled**. **Note:** If you disable the metric, past data shows on the chart for 90 days.

You can configure these settings:-   **Output security vulnerability**
-   **Input security vulnerability**


</td></tr><tr><td>

Agent goal deviation

</td><td>

Shows when AI agents may be deviating from their intended role or objective. For example, unauthorized actions or prompt injection attempts. To show data for this metric in Top AI asset security events, select **Configure**, and then select **Detection enabled**. **Note:** If you disable the metric, past data shows on the chart for 90 days.

You can configure these settings:-   **Sampling rate** – The percentage of transactions that are evaluated. Selecting a rate lower than 100% results in fewer AI calls, but potentially less accurate data. Lower sample rates reduce overhead but may not detect all security events. For critical systems, consider using 100%. For balanced coverage, consider using 75% or higher.
-   **Max skill calls per execution** – The amount of AI usage per call, with a minimum of 10 calls and a maximum of 100 calls. The default is 10 calls. Entering a lower number results in fewer AI calls, but potentially less accurate data.
-   **Single or multiple analysis** – Single analysis uses the default LLM to determine whether the model's output or behavior violates predefined security policies. Multiple analysis uses the results from three or more LLMs that ServiceNow supports to make a determination, using the majority result from the LLMs. Multiple analysis requires an odd number of LLMs.
For external AI systems, configure the Sampling rate. Configure additional settings in Agent goal deviation in AI Evaluation.

</td></tr></tbody>
</table>5.  Under Sensitive data disclosure, configure the metrics and select **Save and Close**.

<table><thead><tr><th>

Metric

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Output screening

</td><td>

Output screening monitors AI-generated responses for sensitive or personally identifiable information \(PII\) before they're delivered to users. To show data for this metric in Top AI asset security events, select **Configure**, and then select **Detection enabled**. **Note:** If you disable the metric, past data shows on the chart for 90 days.

You can configure these settings:-   **Output extended PII** – Collect more potential PII data occurrences and show in the metric. The data is collected by analyzing LLM output for additional potential PII data patterns beyond those specified in Data Privacy. These PII data patterns include US CA drivers license, US passport number, US TIN number, and vehicle ID number.
-   **Output PII violation** – Collect and show data in the metric. The data is collected by analyzing LLM output for potential PII sensitive data patterns specified in Data Privacy. For example, US phone number or credit card number.


</td></tr><tr><td>

Input screening

</td><td>

Input screening monitors user input to detect and anonymize sensitive or personally identifiable information \(PII\) before it reaches the AI model. To show data for this metric in Top AI asset security events, select **Configure**, and then select **Detection enabled**. **Note:** If you disable the metric, past data shows on the chart for 90 days.

You can configure these settings:-   **Input extended PII** – Collect more potential PII data occurrences and show in the metric. The data is collected by analyzing LLM input for additional potential PII data patterns beyond those specified in Data Privacy. These PII data patterns include US CA drivers license, US passport number, US TIN number, and vehicle ID number.
-   **Input PII violation** – Collect and show data in the metric. The data is collected by analyzing LLM input for potential PII sensitive data patterns specified in Data Privacy. For example, US phone number or credit card number.


</td></tr></tbody>
</table>6.  Select the External AI systems tab and repeat steps 3-5.

    Some settings aren't available to be configured in security for external AI systems. Instead, you're directed to the Evaluation tab in Settings to configure the settings.


**Parent Topic:**[Configuring security metrics in AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/gov-sec-configuring.md)


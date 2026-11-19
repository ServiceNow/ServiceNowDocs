---
title: Configure post-runtime security metrics
description: Customize security and content moderation policies, sampling rate, skill call usage limit, LLMs, and related metrics in Super Intelligence Control Tower.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/gov-sec-configure-event-metrics.html
release: brazil
topic_type: task
last_updated: "2026-11-13"
reading_time_minutes: 8
keywords: [ServiceNow Otto, AI Agents, generative AI, agentic AI]
breadcrumb: [Configure, Managing AI asset security, Govern AI assets, Super Intelligence Control Tower, Establishing AI governance, Enable AI Experiences]
---

# Configure post-runtime security metrics

Customize security and content moderation policies, sampling rate, skill call usage limit, LLMs, and related metrics in Super Intelligence Control Tower.

## Before you begin

Role required: sn\_ai\_governance\_ai\_steward

Security and content moderation policies are grouped into LLM guardrail categories that reflect industry practices that align with [OWASP Top 10 Risk &amp; Mitigations for LLMs and Gen AI Apps](https://genai.owasp.org/llm-top-10/) and the [OpenAI model specification](https://model-spec.openai.com/2025-12-18.html). These categories are reflected in the Top AI asset security events metric.

To show AI asset security events for post-runtime categories in **Your top recommendations**, the AICT Security Analyzer agent must be turned on. For more information, see [Turn on the Security Analyzer agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/gov-sec-configure-security-analyzer-agent.md).

All Post-runtime metrics, with the exception of Sensitive data disclosure and Improper input and output handling metrics, consume tokens when turned on. When you enable a post-runtime setting that consumes tokens, a consent prompt appears.

For guidance on managing token consumption, see [Managing evaluation cost](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/mon-ai-managing-evaluation-cost.md).

## Procedure

1.  In Control Tower, navigate to **Settings** &gt; **Rules and templates** &gt; **Security**.

2.  Select the **Post-runtime** sub-tab.

3.  Select the **ServiceNow AI systems** sub-tab.

4.  Configure the metrics and select **Save**.

<table id="table_s14_ly5_1lc"><thead><tr><th>

Metric

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Sensitive information disclosure

</td><td>

Output screening monitors AI-generated responses for sensitive or personally identifiable information \(PII\) before they're delivered to users. Enable the metric to show data in Top AI asset security events. **Note:** If you disable the metric, past data shows on the chart for 90 days.

You can configure these settings:-   **Output extended PII** – Collect more potential PII data occurrences and show in the metric. The data is collected by analyzing LLM output for additional potential PII data patterns beyond those specified in Data Privacy. These PII data patterns include US CA drivers license, US passport number, US TIN number, and vehicle ID number.
-   **Output PII violation** – Collect and show data in the metric. The data is collected by analyzing LLM output for potential PII sensitive data patterns specified in Data Privacy. For example, US phone number or credit card number.
Input screening, available in External AI systems, monitors user input to detect and anonymize sensitive or personally identifiable information \(PII\) before it reaches the AI model. Enable the metric to show data in Top AI asset security events.

**Note:** If you disable the metric, past data shows on the chart for 90 days.

You can configure these settings:

-   **Input extended PII** – Collect more potential PII data occurrences and show in the metric. The data is collected by analyzing LLM input for additional potential PII data patterns beyond those specified in Data Privacy. These PII data patterns include US CA drivers license, US passport number, US TIN number, and vehicle ID number.
-   **Input PII violation** – Collect and show data in the metric. The data is collected by analyzing LLM input for potential PII sensitive data patterns specified in Data Privacy. For example, US phone number or credit card number.


</td></tr><tr><td>

Data integrity incident detection

</td><td>

Shows potential violations of certain LLM guardrail policies in LLM responses. Enable the metric to show data in Top AI asset security events. If you disable the metric, past data shows on the chart for 90 days. **Warning:** AI judge model classifications are probabilistic in nature and may be incomplete or incorrect. They don't constitute professional advice and shouldn't be relied on as the sole basis for assessing risk.

You can configure these settings in the **ServiceNow AI** tab:-   Categories:
    -   Physical, Chemical, Biological Harmful Content Detection
    -   Guardrail Circumvention Attempt
    -   Untrusted Links Or Downloads
    -   Malware Detection
    -   Over and Under Refusal Detection
    -   Insecure Code Output
    -   Confidential Information Extraction Attempts
    -   Fraud or Deceptive Facilitation
    -   Internal System Instruction Detection
-   **Sampling rate** – The percentage of transactions that are evaluated. A lower sample rate will result in fewer LLM calls but may also result in fewer detected security events.
-   **Max skill calls per execution** – The amount of AI usage per call, with a minimum of 10 calls and a maximum of 100 calls. The default is 10 calls. Entering a lower number results in fewer AI calls, but potentially less accurate data.
-   **Single or multiple analysis** – Single analysis uses AWS Claude to determine whether the model's output or behavior violates predefined security policies. Multiple analysis uses the results from three or more LLMs that ServiceNow supports to make a determination, using the majority result from the LLMs. Multiple analysis requires an odd number of LLMs.


</td></tr><tr><td>

Correctness detection

</td><td>

Correctness measures whether the information provided in the model's response is factually accurate and logically valid given the prompt and context. Enable this metric to show data in Top AI asset security events. **Note:** If you disable the metric, past data shows on the chart for 90 days.

You can configure these settings:-   **Sampling rate** – The percentage of transactions that are evaluated. A lower sample rate will result in fewer LLM calls but may also result in fewer detected security events.
-   **Max skill calls per execution** – The amount of AI usage per call, with a minimum of 10 calls and a maximum of 100 calls. The default is 10 calls. Entering a lower number results in fewer AI calls, but potentially less accurate data.
-   **Single or multiple analysis** – Single analysis uses AWS Claude to determine whether the model's output or behavior violates predefined security policies. Multiple analysis uses the results from three or more LLMs that ServiceNow supports to make a determination, using the majority result from the LLMs. Multiple analysis requires an odd number of LLMs.
For external AI systems, configure the Sampling rate. Configure additional settings in Correctness \(factuality\) in AI Evaluation.

</td></tr><tr><td>

Agentic goal deviation

</td><td>

Shows when AI agents may be deviating from their intended role or objective. For example, unauthorized actions or prompt injection attempts. Enable this metric to show data in Top AI asset security events. **Note:** If you disable the metric, past data shows on the chart for 90 days.

You can configure these settings:-   **Sampling rate** – The percentage of transactions that are evaluated. A lower sample rate will result in fewer LLM calls but may also result in fewer detected security events.
-   **Max skill calls per execution** – The amount of AI usage per call, with a minimum of 10 calls and a maximum of 100 calls. The default is 10 calls. Entering a lower number results in fewer AI calls, but potentially less accurate data.
-   **Single or multiple analysis** – Single analysis uses AWS Claude to determine whether the model's output or behavior violates predefined security policies. Multiple analysis uses the results from three or more LLMs that ServiceNow supports to make a determination, using the majority result from the LLMs. Multiple analysis requires an odd number of LLMs.
For external AI systems, configure the Sampling rate. Configure additional settings in Agent goal deviation in AI Evaluation.

</td></tr><tr><td>

Excessive agency

</td><td>

Detects when LLMs are provided too much access, leading to potential unauthorized or excessive actions by the LLM. Controls data for Access issues and Privileged AI agents metrics, as well as Post-runtime metrics. The setting is off by default.

</td></tr><tr><td>

Prompt injection

</td><td>

Prompt injection attacks occur when malicious input is crafted to override or deviate from the model's instructions, causing unintended behavior. Enable this metric to show data in Top AI asset security events. **Note:** If you disable the metric, past data shows on the chart for 90 days.

You can configure these settings:-   **Sampling rate** – The percentage of transactions that are evaluated. A lower sample rate will result in fewer LLM calls but may also result in fewer detected security events.
-   **Max skill calls per execution** – The amount of AI usage per call, with a minimum of 10 calls and a maximum of 100 calls. The default is 10 calls. Entering a lower number results in fewer AI calls, but potentially less accurate data.
For external AI systems, configure the Sampling rate. Configure additional settings in Prompt injection in AI Evaluation.

</td></tr><tr><td>

System prompt leakage

</td><td>

System prompt leakage occurs when the model inadvertently reveals its system prompt or configuration instructions to users. Enable this metric to show data in Top AI asset security events. **Note:** If you disable the metric, past data shows on the chart for 90 days.

You can configure these settings:-   **Sampling rate** – The percentage of transactions that are evaluated. A lower sample rate will result in fewer LLM calls but may also result in fewer detected security events.
-   **Max skill calls per execution** – The amount of AI usage per call, with a minimum of 10 calls and a maximum of 100 calls. The default is 10 calls. Entering a lower number results in fewer AI calls, but potentially less accurate data.
-   **Single or multiple analysis** – Single analysis uses AWS Claude to determine whether the model's output or behavior violates predefined security policies. Multiple analysis uses the results from three or more LLMs that ServiceNow supports to make a determination, using the majority result from the LLMs. Multiple analysis requires an odd number of LLMs.
For external AI systems, configure the Sampling rate. Configure additional settings in AI Evaluation.

</td></tr><tr><td>

Improper input and output handling

</td><td>

When AI predictions are consumed in workflows without the right potential security vulnerability checks, it can lead to incorrect, unsafe, or biased actions. Enable this metric to show data in Top AI asset security events. **Note:** If you disable the metric, past data shows on the chart for 90 days.

You can configure these settings:-   **Output security vulnerability**
-   **Input security vulnerability**


</td></tr></tbody>
</table>5.  Select the **External AI systems** sub-tab and repeat step 4.

    Some settings aren't available to be configured in security for external AI systems, such as **Max Skill Calls** and **Single or Multiple Analysis**.


**Parent Topic:**[Configuring security metrics in Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/gov-sec-configuring.md)


---
title: Data sharing, Data overflow processing, and Security &amp; privacy in AI Control Tower
description: Explore the Data sharing, Data processing, and Security &amp; privacy sections.
locale: en-US
release: zurich
product: AI Control Tower
classification: ai-control-tower
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 6
keywords: [Now Assist, generative AI]
breadcrumb: [Configurations, AI Control Tower dashboard, Explore, AI Control Tower, Enable AI experiences]
---

# Data sharing, Data overflow processing, and Security &amp; privacy in AI Control Tower

Explore the Data sharing, Data processing, and Security &amp; privacy sections.

The section focuses on improving AI models, managing datacenter traffic, and enabling metrics to measure the integrity of your data model and monitor potential threats in large language model \(LLM\) input and output.

## Data sharing

By default, Data sharing is active. You can opt out to deactivate AI Control Tower and share your data with ServiceNow to improve AI accuracy, enhance user experiences, and gain a better understanding of business needs.

Data sharing helps enhance ServiceNow products, but if you choose to opt out of the ServiceNow data sharing program, you are no longer be able to contribute data to improve ServiceNow AI products.

For information on data sharing opt-out, see [Opt out of data sharing](https://www.servicenow.com/docs/bundle/zurich-intelligent-experiences/page/administer/now-assist-admin/task/opt-out-of-data-sharing-for-now-assist.html).

## Data overflow processing

By default, all Now Assist traffic is managed within ServiceNow datacenters. If there are traffic spikes, the system automatically redirects to Microsoft Azure datacenters to maintain performance. You can opt out of this feature to keep all Now Assist traffic exclusively within ServiceNow datacenters. By default, data overflow processing is inactive.

**Note:** The Data sharing and Data overflow processing features are available for a sub-prod instance in read-only mode, when Multi-instance setup is configured and active.

## Security &amp; privacy

-   **Secure policies violation**

    These configuration settings control the Security policy violations chart, which shows violations of policies detected in LLM responses. To show data for this chart on the dashboard, select **Configure**, and then select **Active**. If you want to discontinue collecting data for the chart, deselect **Active**.

    **Note:** If you inactivate the chart, past data shows on the chart for 90 days.

    You can configure these settings:

    -   **Security policies** – Predefined ServiceNow policies to track for violations. These policies are based on industry best practices and can't be modified.
        -   **Physical Chemical Biological Harm** – Detect recipes, parts lists, or methods that could cause real-world harm. For example, explosives, toxins, or bio agents.
        -   **Policy Circumvention** – Detect jailbreak techniques. For example, disabling safety instructions or acting as an unfiltered model.
        -   **Untrusted Links Or Downloads** – Detect linking to executable files or malware, directing users to run unverified downloads or macros, or asking users to disable their antivirus protection. Heuristic red flags include EXE, BAT, PS1, and APK files, along with macro-enabled documents.
        -   **Intellectual Property Proprietary** – Detect verbatim reproduction of paywalled or proprietary text or code beyond fair use.
        -   **Malware Exploits Hacking** – Detect exploited payloads, brute force attacks, evasion, persistence, keyloggers, or “ready-to-run” steps.
        -   **Refusal Appropriateness** – When a request conflicts with policy, refusal should be safe and brief. Detect under- and over-refusal. For example, refusing benign content.
        -   **Code And Command Safety** – Detect destructive and insecure commands. For example, don't allow “try this risky one-liner,” disabling security, or running unvetted code.
        -   **Social Engineering Deception** – Detect impersonation and phishing scripts, credential harvesting, and manipulative pretexts.
        -   **Fraud Misinformation Illegal Facilitation** – Detect how-to guides for illegal or deceptive practices. For example, for market manipulation, fraud templates, or evading audit. Benign corrections of misinformation are allowed, but not fabrication.
        -   **System Integrity Prompt Containment** – Detect output of system prompts, hidden policies, and internal configurations or tokens.
        -   **Legal Regulatory Compliance** – Detect guidance to evade regulations or practice without a license. For example, prescriptions, export control, or money laundering evasion.
    -   **Sampling rate** – The percentage of transactions that are evaluated. Selecting a rate lower than 100% results in fewer AI calls, but potentially less accurate data.
    -   **Max skill calls per execution** – The amount of AI usage per call. The minimum is 10 calls; the default is 1,000 calls. Entering a lower number results in fewer AI calls, but potentially less accurate data.
    -   **Single or multiple analysis** – Single analysis uses the default LLM to determine whether the model's output or behavior violates predefined security policies. Multiple analysis uses the results from three or more LLMs that ServiceNow supports to make a determination, using the majority result from the LLMs. Multiple analysis requires an odd number of LLMs.
-   **Output deviation**

    These configuration settings control the Agent output deviation chart, which shows when AI agents deviate from their intended role or objective. For example, unauthorized actions or prompt injection attempts. To show data for this chart on the dashboard, select **Configure**, and then select **Active**. If you want to discontinue collecting data for the chart, deselect **Active**.

    **Note:** If you inactivate the chart, past data shows on the chart for 90 days.

    You can configure these settings:

    -   **Sampling rate** – The percentage of transactions that are evaluated. Selecting a rate lower than 100% results in fewer AI calls, but potentially less accurate data.
    -   **Max skill calls per execution** – The amount of AI usage per call. The minimum is 10 calls; the default is 1,000 calls. Entering a lower number results in fewer AI calls, but potentially less accurate data.
    -   **Single or multiple analysis** – Single analysis uses the default LLM to determine whether the AI agent's or skill's response diverges from the expected output. Multiple analysis uses the results from 3 or more LLMs to make a determination, using the majority result from the LLMs. Multiple analysis requires an odd number of LLMs.
-   **Output screening**

    These configuration settings control the AI agent output with PII detected and High-risk AI agent output charts, which show when agents' LLM output contains PII or security-vulnerable patterns. To show data for these charts on the dashboard, select **Configure**, select **Active**, and then select a setting for the data to collect. If you want to discontinue collecting data for the charts, deselect **Active**.

    **Note:** If you inactivate the charts, past data collected shows on the charts for 90 days.

    You can configure these settings:

    -   **Output Security Vulnerability** – Collect and show data in the High-risk AI agent output chart. The data is collected by scanning LLM output for known vulnerable patterns and potential corresponding attack vectors. For example, HTML tags can have scripts associated with them to generate cross-site script attacks \(XSS\), or stacked SQL queries that can result in SQL injection attacks.
    -   **Output Extended PII** – Collect more PII data occurrences and show in the AI agent output with PII detected chart. The data is collected by scanning LLM output for additional PII data patterns beyond those specified in Data Privacy. These PII data patterns are U.S. CA drivers license, U.S. taxpayer ID, U.S. passport number, and vehicle ID number.
    -   **Output PII Violation** – Collect and show data in the AI agent output with PII detected chart. The data is collected by scanning LLM output for default PII sensitive data patterns specified in Data Privacy. For example, U.S. phone number or credit card number.
-   **Sensitive data input and anonymization**

    This section shows the data patterns enabled in Data Privacy to detect and anonymize information in LLM prompts. Use this view as a quick reference when troubleshooting Sensitive data detected and Sensitive data anonymized charts. This feature requires the Data privacy plugin to be installed. For more information on how the data is sent and stored, see [User data usage policy for Now Assist](https://www.servicenow.com/docs/bundle/zurich-intelligent-experiences/page/administer/now-assist-admin/concept/user-data-usage-policy-now-assist.html).



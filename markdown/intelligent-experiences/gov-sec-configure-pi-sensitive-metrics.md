---
title: Configure runtime security metrics
description: Set up a Traceloop connection and API key for prompt injection, offensive content, sensitive data input, and sensitive data anonymized trace data from external AI servers. Review data privacy for sensitive data patterns to detect in LLM input and output.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/gov-sec-configure-pi-sensitive-metrics.html
release: australia
topic_type: task
last_updated: "2026-05-02"
reading_time_minutes: 2
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Configure, Managing AI asset security, Govern AI assets, AI Control Tower, Enable AI experiences]
---

# Configure runtime security metrics

Set up a Traceloop connection and API key for prompt injection, offensive content, sensitive data input, and sensitive data anonymized trace data from external AI servers. Review data privacy for sensitive data patterns to detect in LLM input and output.

## Before you begin

Role required: admin

Install the open-source Traceloop SDK. In a terminal window, run this command:

`pip install traceloop-sdk`

After you install Traceloop SDK, you can customize the following code to initialize the Traceloop tracer:

```
import os from openai
import OpenAI from traceloop.sdk
import Traceloop from traceloop.sdk.decorators
import workflow task

# Initialize
Traceloop SDKTraceloop.init(app_name="joke_generation_service", disable_batch=True)
client = OpenAI(api_key=os.environ.get("OPENAI_API_KEY"))
```

For more information, see [Traceloop OpenLLMetry for Python](https://www.traceloop.com/docs/openllmetry/getting-started-python).

## Procedure

1.  Configure a trace connection for every external AI system for which you want to show runtime metrics.

    For more information, see [Configuring trace connections](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aict-configuring-trace-connections.md).

2.  Generate an API key to authenticate trace data requests from your external AI system.

    1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Credentials**.

    2.  Create credentials of type **API Key Credentials**.

        Fill out these fields and select **Submit**.

        |Field|Description|
        |-----|-----------|
        |Name|Traceloop API Key|
        |Applies to|All MID servers|
        |Active|Selected.|
        |Order|100|
        |API Key Header|Authorization|
        |API Key Prefix|Bearer|
        |API Key|\[Your Traceloop API key\]|
        |Credential alias|Locked.|

    For more information, see [API key credentials](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/API-key-credential-form.md).

3.  Link the API key to your trace connection.

    1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connections**.

    2.  From the connections list, select the **Traceloop Warehouse** connection.

        Fill out these fields and select **Update**.

        |Field|Description|
        |-----|-----------|
        |Name|Traceloop Warehouse|
        |Active|Selected.|
        |Credential|Traceloop API Key \(from step 2b\)|
        |Domain|global|
        |Connection alias|sn\_ai\_security.Traceloop\_API|
        |URL builder|N/A|
        |Connection URL|https://api.traceloop.com|
        |Use MID server|N/A|
        |Connection timeout|N/A|

        The scheduled job will now automatically pull runtime metrics from the linked Traceloop environment.

    For more information, see [Create an HTTP\(s\) connection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/create-https-connection.md).

4.  Configure the Traceloop SDK in your agent code by adding these ServiceNow attributes when initializing Traceloop.

    These are unique user-defined identifiers for tracking.

    ```
    Traceloop.init(
        app_name="your_agent_name",
        api_key=traceloop_api_key,
        resource_attributes={
            "sn.aict.system.id": "your_agent_system_id",
            "sn.aict.system.name": "your_agent_name",
            "sn.aict.system.version": "1.0.0",
            "sn.aict.system.source": "your_source"
        }
    )
    ```

    For more information about configuring Traceloop in your agent, see [Traceloop - Guardrails](https://www.traceloop.com/docs/evaluators/guardrails).

5.  To review data privacy, in AI Control Tower, navigate to **Settings** &gt; **Rules and templates** &gt; **Security** &gt; **Data Privacy**.

    This section shows the data patterns enabled in Data Privacy to detect and anonymize information in LLM prompts. Use this view as a quick reference when troubleshooting sensitive data charts. This feature requires the Data privacy plugin to be installed. For more information on how the data is sent and stored, see [User data usage policy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/user-data-usage-policy-now-assist.md).

6.  Return to the AI Control Tower Security tab and refresh the page.

    Select the Runtime tab and verify that metrics are populated.


**Parent Topic:**[Configuring security metrics in AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/gov-sec-configuring.md)


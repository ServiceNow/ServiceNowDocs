---
title: Configure Veza access intelligence in the agent map
description: Integrate Veza with ServiceNow to display agent risk scores and severity levels in the agent map. Complete this configuration for each hyperscaler that has AI assets you want to monitor.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/gov-sec-configure-veza-access-intelligence.html
release: australia
topic_type: task
last_updated: "2026-07-20"
reading_time_minutes: 2
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Configure, Managing AI asset security, Govern AI assets, AI Control Tower, Enable AI experiences]
---

# Configure Veza access intelligence in the agent map

Integrate Veza with ServiceNow to display agent risk scores and severity levels in the agent map. Complete this configuration for each hyperscaler that has AI assets you want to monitor.

## Before you begin

Role required: AI steward \[sn\_ai\_governance\_ai\_steward\]

## About this task

Veza access intelligence requires a connection between ServiceNow and each hyperscaler that hosts governed AI assets. ServiceNow and Veza each maintain separate connections to hyperscalers to retrieve and correlate AI asset data. Access intelligence supports governed agents hosted by Amazon Web Services \(AWS\), GCP Vertex AI, Azure, and Salesforce.

## Procedure

1.  In your Veza tenant, configure integrations for all of the supported hyperscalers that you want to connect to, including ServiceNow.

    For example, connect Veza to AWS and Veza to ServiceNow.

    For more information, see [Veza integrations](https://docs.veza.com/4yItIzMvkpAvMVFAamTf/integrations/integrations).

2.  In your Veza tenant, navigate to **Administration** &gt; **API Keys** to generate a Veza API access token to use later.

    For more information, see [API Keys in Veza documentation](https://docs.veza.com/4yItIzMvkpAvMVFAamTf/developers/api/authentication/api-tokens).

3.  In AI Control Tower, navigate to **Settings** &gt; **Integrations** &gt; **Connectors** to configure integrations for all of the hyperscalers that you want to connect to.

    For example, connect ServiceNow to AWS.

    For more information, see [Configuring integrations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aict-configuring-integrations.md).

4.  Set system properties to connect ServiceNow to the Veza tenant.

    1.  Navigate to **All** &gt; **System Properties** &gt; **All Properties**.

    2.  In the Name column, use the search field to locate the **sn\_ai\_security.veza.api.url** system property.

    3.  Open the record.

    4.  In the Value field, enter the base URL of your Veza tenant and select **Update**.

        For example, `https://your-tenant.vezacloud.com`.

    5.  In the Name column, use the search field to locate the **sn\_ai\_security.veza.api.key** system property.

    6.  Open the record.

    7.  In the Value field, enter the Veza API access token you created earlier in this procedure and select **Update**.

5.  In AI Control Tower, navigate to the **Security** tab and refresh the page.


## Result

In the agent map, select an AI asset and view the Access intelligence tab to see risk score and other information.

If your AI asset appears in the agent map but doesn't have information shown in the Access intelligence tab, make sure that it's a governed asset with `external_ref_id` populated and `model_category=Agentic AI`.

**Parent Topic:**[Configuring security metrics in AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/gov-sec-configuring.md)


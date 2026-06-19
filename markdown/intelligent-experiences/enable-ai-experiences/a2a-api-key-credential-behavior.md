---
title: A2A API Key credential behavior
description: Starting in Now Assist AI Agents 7.1.x, the header included in each A2A request is driven by the API Key credential record and it is not injected automatically by the flow action.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/enable-ai-experiences/a2a-api-key-credential-behavior.html
release: zurich
product: Enable AI Experiences
classification: enable-ai-experiences
topic_type: concept
last_updated: "2026-06-19"
reading_time_minutes: 2
breadcrumb: [Create an external agent, Create an AI agent, Now Assist AI agents, Enable AI experiences]
---

# A2A API Key credential behavior

Starting in Now Assist AI Agents 7.1.x, the header included in each A2A request is driven by the API Key credential record and it is not injected automatically by the flow action.

Starting in Now Assist AI Agents 7.1.x, A2A flow actions no longer inject an `Authorization: Bearer` header automatically. The header included in each request is now driven entirely by the API Key credential record bound to the external agent's Connection &amp; Credential Alias.

OAuth-based external agents, and API Key endpoints whose existing credential record already aligns with the endpoint's expectations, are unaffected. You only need to act if your remote A2A endpoint requires a specific header name or a scheme prefix.

## Resolve 401 or 403 errors after upgrade

If your A2A endpoint returns a 401 or 403 after upgrading, update the API Key credential record bound to your external agent.

1.  Open the `api_key_credentials` record bound to your A2A external agent. Navigate to the record via the **Connection &amp; Credential Alias** on the external-agent provider.
2.  If the endpoint requires a specific header name \(for example, `x-api-key` instead of `Authorization`\), set the **API Key Header** \(`api_key_header_name`\) field to the header name the endpoint expects.
3.  If the endpoint requires a scheme prefix on the value \(for example, `Bearer` for Google A2A\), include the prefix directly in the **API Key** \(`api_key`\) field value — for example, change `AIza...` to `Bearer AIza...`.

    **Note:** The **API Key Prefix** field is not currently applied by the A2A flow action; embed the scheme in the **API Key** value instead.

4.  Save the record and re-test the external agent end-to-end.


## Wizard-created credential records

The wizard creates a working API Key credential record for most A2A endpoints. Only edit the credential record manually if your remote endpoint has specific requirements that the default credential does not satisfy.

-   Custom header name \(for example, `x-api-key`\): Set the **API Key Header** \(`api_key_header_name`\) field to the header name the endpoint expects.
-   Scheme prefix on the value \(for example, `Bearer` for Google A2A\): Include the prefix directly in the **API Key** field value — for example, `Bearer <your-key>`. Don't use the **API Key Prefix** field; it is not applied by the A2A flow action.

**Parent Topic:**[Create an external AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/enable-ai-experiences/create-external-aia.md)


---
title: AgentCard specification
description: View the definition and field reference for the A2A discovery manifest used by the ServiceNow AI Agent Studio.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/sales-and-order-management/cpq-agentcard-specification.html
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: reference
last_updated: "2026-05-13"
reading_time_minutes: 1
breadcrumb: [CPQ app, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# AgentCard specification

View the definition and field reference for the A2A discovery manifest used by the ServiceNow AI Agent Studio.

The AgentCard is the A2A discovery manifest that identifies the agent to any conforming orchestrator. It is served at the agent's well-known discovery endpoint and is what ServiceNow AI Agent Studio reads when you register the external agent.

## AgentCard definition

```
AgentCard(
   name            = "Config Converse A2A Middleware",
   description     = "Middleware service that bridges other agents with Config
                     Converse using A2A protocol to configure products based on
                     context provided by other agents. Provides industry-standard
                      A2A protocol interface with JSON-RPC transport.",
   url             = <base_url>,           # your Logik tenant base URL
   version         = "1.0.0",
   protocol_version= "0.3.0",
   preferred_transport = TransportProtocol.jsonrpc,
   default_input_modes = ConfigConverseAgent.SUPPORTED_CONTENT_TYPES,
   default_output_modes= ConfigConverseAgent.SUPPORTED_CONTENT_TYPES,
   capabilities    = capabilities,
   skills          = [skill],
   security_schemes= {
      "bearer": HTTPAuthSecurityScheme(
           type          = "http",
           scheme        = "bearer",
           bearer_format = None,
          description   = "Logik phantom token. Obtain from Logik Admin UI
                           under Settings -> Runtime Clients. Token must
                           have CONFIG permission."
       )
   },
   security        = [{"bearer": []}]
)
```

## Field reference

|Field|Type|Description|
|-----|----|-----------|
|name|string|Human-readable display name shown in AI Agent Studio.|
|url|string \(URL\)|Base URL of the running middleware. Must be reachable from ServiceNow.|
|version|semver|Agent implementation version. Increment on breaking changes.|
|protocol\_version|string|A2A protocol version this agent complies with. Currently 0.3.0.|
|preferred\_transport|enum|Set to jsonrpc. Orchestrators should default to JSON-RPC when contacting this agent.|
|default\_input\_modes|list\[string\]|MIME types accepted as input. Populated from ConfigConverseAgent.SUPPORTED\_CONTENT\_TYPES.|
|default\_output\_modes|list\[string\]|MIME types returned as output. Matches input modes.|
|capabilities|object|Structured capability flags declared by the agent to the orchestrator.|
|skills|list\[skill\]|One or more skill descriptors defining what tasks this agent can perform.|
|security\_schemes|object|Declares the bearer scheme. Key must match the entry in the security list.|
|security|list\[object\]|Enforces bearer auth on all agent interactions.|


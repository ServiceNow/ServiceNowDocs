---
title: ServiceNow AI agents as secondary agents
description: Secondary agents are specialized AI agents that handle specific workflow tasks delegated by a primary agent or user. You can connect your ServiceNow agent to other agentic AI model providers using the Agent2Agent protocol.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/a2a-secondary-agent.html
release: brazil
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Integrate external AI agents, AI Agent Studio, AI agents and agentic workflows, Enable AI Experiences]
---

# ServiceNow AI agents as secondary agents

Secondary agents are specialized AI agents that handle specific workflow tasks delegated by a primary agent or user. You can connect your ServiceNow agent to other agentic AI model providers using the Agent2Agent protocol.

## Enable ServiceNow AI agents as secondary agents

You can enable ServiceNow AI agents as secondary agents to use on other AI platforms. To do so, navigate to **AI Agent Studio** &gt; **Settings** &gt; **External AI agents** and toggle **Allow third party access to ServiceNow AI agents**.\[Omitted image "third-party-snow-agents.png"\] Alt text: Option to enable integration of ServiceNow AI agents int external agentic AI systems.

## Secondary agents overview

After creating your AI agent in AI Agent Studio, you can point it to the Agent Card URL that is displayed for secondary agents. Admins can view, copy, and consume the URL for easy access. The endpoint to point the AI agent to Agent Card for the actual execution of the AI agent is in the `{{instance}}.service-now.com/api/sn_aia/a2a/v2/agent/id/{{agent-id}}` format.

You can use the same OAuth or API key for authenticating the agent discovery and the agent execution. For more information, see [A2A API Key credential behavior](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/a2a-api-key-credential-behavior-new.md).

To verify that your AI agent is running from the ServiceNow side, during a conversation with the AI agent, you can go to the **Execution Plan \[sn\_aia\_execution\_plan\]** table. From the Execution Plan table, you can identify the execution plan based on the **Objective** field that contains the prompt from the conversation on the other platform.

For more information about setting up instructions for your ServiceNow AI agents as secondary agents \(acting as A2A server\), refer to [Authentication for A2A - ServiceNow as Secondary Agent](https://www.servicenow.com/community/now-assist-articles/authentication-for-google-a2a-servicenow-as-secondary-agent/ta-p/3446091).

For more information about sample payloads for A2A with ServiceNow AI agent as Secondary agent, see [Sample payloads for A2A](https://www.servicenow.com/community/now-assist-articles/sample-payloads-for-google-a2a-servicenow-as-secondary-agent/ta-p/3451904).

## Agent-to-UI \(A2UI\) protocol support for secondary agents

The A2UI protocol allows interactions that enable agents to drive UI workflows and receive structured responses from user interface surface with more advanced visual responses in external systems when connecting to ServiceNow agents. To enable the A2UI protocol, you must:

-   Turn on the **sn\_aia.external\_agents.a2ui.enabled** system property to **true**, whose default value is **false**.
-   Route the A2A deployment through off-glide experience. The A2UI responses can only be built on the off-glide path. Verify that the **sn\_nowassist\_va.show\_ai\_native\_experience** system property to **true** and the A2A deployment record experience to **AI native** in the **sys\_now\_assist\_deployment\_channel**, as shown in the following image:

    \[Omitted image "a2ui-channel.png"\] Alt text: Enable AI native chat for AI Agent A2A Provider Application.

-   Check the agent card. When you enable the system properties mentioned earlier, the card adds the extension under **capabilities.extensions**. If the property is enabled but the off-glide experience isn't setup, then the extension is left off the card without any warning. The only sign is an error in the log.
-   Have the calling client request A2UI on each call. The client has to:
    -   Send the header `X-A2A-Extensions`. For example, `https://a2ui.org/aa-extension/a2ui/v0.9`.

        **Note:** Only versions **0.9** is supported.

    -   Include `application/json+a2ui` or `application/json` if it sets the `configuration.accpetedOutputModes`. Without one of those, the requests is rejected with `InvalidAccpetedOutputModes`.

        To get v1 when ServiceNow acts as primary agent, the premium chat should be enabled in the respective assistant this agent is being executed from. Refer to the [Premium Chat experience](https://www.servicenow.com/community/servicenow-ai-platform-blog/premium-chat-101-meet-servicenow-s-newest-conversational/ba-p/3590724) article on how that can be enabled.


For more information about A2UI, see [A2UI documentation](https://a2ui.org/).


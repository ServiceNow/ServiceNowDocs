---
title: Domain separation and Now Assist AI Agent Studio
description: If any conkeyrefs are broken, re-add them from the doc/source/reuse/domain-separation/domain-separation-overview.dita file.In the short description, edit the first sentence to state whether domain separation is supported or not and add the application name. Keep the conkeyref at the end that describes domain separation.Domain separation is supported for Now AssistAI Agent Studio. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
keywords: [AI Agents, Agentic AI]
breadcrumb: [Reference, Now Assist AI agents, Enable AI experiences]
---

# Domain separation and Now Assist AI Agent Studio

Domain separation is supported for Now AssistAI Agent Studio. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Domain Separation Overview

Now Assist AI agents use basic domain separation capabilities to help protect your users' data. Domain separation support for AI agents is applied at design time and run time.

-   **Design-time support**

    Refers to creating or updating agentic workflows, agents, tools, trigger configurations, and so on. AI agent configurations can be made domain-specific for individual agents and the actual agentic workflows. Administrators can apply specific domains to those records. Similar to other basic domain separations, records in the AI agents tables are accessible if the user belongs to the same or a higher domain than those records.

-   **Run-time support**

    Refers to the agentic conversation on the Now Assist panel, web client, or any conversational channel. In the agentic conversations, the user that the agent impersonates functions as an agent with any AI agents who initiate the conversation on demand. For example, if the conversation is happening via a trigger mentioned on the **Run as** field on the Trigger form of an agentic workflow. If the user that the agent impersonates belongs to the same or a higher domain, that agent can access and use configurations that are associated with that domain.

    The domain visibility for an agentic workflow is resolved during run time based on the **Run as** attribute in the agentic workflow trigger condition. For more information, see [defining a trigger for an agentic workflow](../task/configure-use-case-ai-agents.md).


When an agentic conversation is triggered on demand, the domain visibility is applied to the particular agent in action. When an agentic conversation is initiated through a trigger, the domain visibility is applied to the user who resolves the caller \(in an incident record where the **Run as** attribute is set to **Caller**\), when the conversation runs against the incident record.

**Note:** The **sys\_domain** field is added to all AI agent tables to achieve domain separation in Now Assist AI agents. The sys\_domain\_path, which is available for domain separation, is enabled on your instance.

To understand more about the ServiceNow domain separation, see Exploring domain separation.

## How domain separation works in Now Assist AI Agent Studio

Process separation is enabled through the use of the sys\_overrides column in domain-aware tables. Any table that contains both the sys\_domain and the sys\_overrides fields can be configured to have different processes from the parent domain.

AI Agents support only configuration tables to be process separated. Below are the list of tables that are process separated:

-   sn\_aia\_agent\_config
-   sn\_aia\_usecase\_config\_override

Domain separation in Now Assist AI agents supports:

-   Agentic workflow discovery.
-   AI agent and its tools can be active in the X domain and inactive in the Y domain.
-   Memory category can be active in the X domain and inactive in the Y domain.
-   sn\_aia\_property can be overridden in a different domain.
-   Triggers can be overridden in different domain.

**Note:** AI agent and agentic workflow details can’t be overridden in the different domains.

**Related topics**  


[bundle-psec.domain-sep-landing-page]


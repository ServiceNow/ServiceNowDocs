---
title: Now Assist for Financial Services Operations \(FSO\) release notes
description: The ServiceNow Now Assist for Financial Services Operations \(FSO\) application brings generative and agentic AI to Financial Services Operations. Features include AI agents, case summarization, disputes intake via Virtual Agent, and support for third-party language models. Now Assist for FSO was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 5
---

# Now Assist for Financial Services Operations \(FSO\) release notes

The ServiceNow® Now Assist for Financial Services Operations \(FSO\) application brings generative and agentic AI to Financial Services Operations. Features include AI agents, case summarization, disputes intake via Virtual Agent, and support for third-party language models. Now Assist for FSO was enhanced and updated in the Yokohama release.

## Now Assist for FSO highlights for the Yokohama release

[Yokohama Patch 11](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/yokohama-patch-11.md)

-   Now Assist for FSO skills and AI agents support model updates in Now LLM Service.
-   Some Now Assist skills, agents, and agentic workflows are on by default.
-   Review changes to Now Assist usage measurement.
-   Additional role configuration is required for agentic workflows and AI agents included with Now Assist applications.

Yokohama Patch 6

-   Use Google Gemini and Anthropic Claude on AWS as AI model providers for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.
-   Implement security in Now Assist AI agents and Now Assist for FSO skills with Access Control Lists \(ACLs\).

Yokohama Patch 3

-   Streamline the friendly fraud dispute resolution process for human agents and make informed decisions by using the Now Assist friendly fraud AI agent.
-   Maintain positive customer relationships by using the AI agent to craft responses with the right tone and language.
-   Enable agents to evaluate and review the amount being disputed, the customer relationship, and the outcome of the detection logic.

Yokohama Patch 1

-   Streamline the card dispute submission process for cardholders with a dispute intake workflow by using Now Assist in Virtual Agent.
-   Use a conversational, natural language interface that makes data collection more engaging and less tedious compared to a traditional form.
-   Increase efficiency by inferring information from the customer’s responses in the conversation.

See [Now Assist for Financial Services Operations \(FSO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/financial-services-operations/now-assist-for-financial-services-operations.md) for more information.

**Important:** Now Assist for FSO is available in ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Yokohama release

-   **[Long term stable models](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/long-term-stable-models.md)**

    Long term stable \(LTS\) models are part of Now LLM Service and provide longer model stability windows for regulated industries. These models can integrate with tools to provide governance, monitoring, and compliance controls.


-   **[New third-party AI model provider options available for all Now Assist applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/exploring-large-language-models.md)**

    Google Gemini and AWS Claude are available for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.

-   **[ACL security implementation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/financial-services-operations/configuring-now-assist-skills-for-fso.md)**

    Enable security implementation to execute AI agents, agentic workflows, and generative AI skills through ACLs and user identities in Now Assist for FSO.

    Predefined ACLs are provided for case summarization, Disputes intake via Virtual Agent, and the Help resolve friendly fraud AI agent and agentic workflow.


-   **[Using agentic workflows in Now Assist for Financial Services Operations \(FSO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/financial-services-operations/using-ai-agent-use-cases-in-now-assist-for-fso.md)**

    Resolve disputes that are flagged as friendly fraud with comprehensive guidance from the friendly fraud AI agent. Leverage the AI agent's step-by-step recommendations and detailed responses to explain the decisions made regarding disputes. Based on the AI agent recommendations, issue credit to customers, decline disputes, or initiate an exception process.


-   **[Disputes intake via Virtual Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/financial-services-operations/now-assist-for-financial-services-operations.md)**

    Provide an intuitive dialog-based channel experience for your customers to submit details on a dispute case. The dispute intake via Virtual Agent leverages questions that are required by the card processing networks. Now LLM Service rephrases these questions in a conversational format and infers the answers for the unanswered questions from customer responses.


## Changed in this release

-   **[Role configuration required for agentic workflows and AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/aia-role-masking.md)**

    Agentic workflows and AI agents included with Now Assist applications require additional security configuration. If you select **Users with selected roles** for your user access security controls for an agentic workflow or AI agent, you must add the installed roles, or they will not execute. Data access settings must also include these roles. See the documentation for the agentic workflow or AI agent for the specific roles you must add.

-   **[Some Now Assist skills are turned on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/now-assist-skills-on-by-default.md)**

    The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Yokohama Patch 11\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.
-   **[Changes to Now Assist usage measurement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/monitoring-now-assist-usage.md)**

    Starting with Yokohama Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


## Activation information

Install Now Assist for FSO by requesting it from ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Additional requirements

The Now Assist for FSO application requires a Financial Services Operations Professional Plus or Enterprise Plus license.

## Related ServiceNow applications and features

-   **[Now Assist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/platform-now-assist-landing.md)**

    The ServiceNow® Now Assist application uses generative AI that is designed to enhance user productivity and efficiency through conversation and proactive experiences.

-   **[Now Assist in Virtual Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/conversational-interfaces/now-assist-in-va-landing.md)**

    The ServiceNow® Now Assist in Virtual Agent enhances productivity and empowers customers with a self-service interface for submitting a card dispute.

-   **[Using agentic workflows in Now Assist for Financial Services Operations \(FSO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/financial-services-operations/using-ai-agent-use-cases-in-now-assist-for-fso.md)**

    The predefined ACLs in this release apply to the AI agents and agentic workflows in Now Assist for FSO.

-   **[Implement access control in Now Assist AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/aia-security-implementation.md)**

    Configure and manage ACLs for agentic workflows and AI agents in the AI Agent Studio


**Parent Topic:**[Financial Services Operations release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/financial-services-operations-rn-landing.md)

**Parent Topic:**[Now Assist and agentic AI release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/now-assist-rn-landing.md)


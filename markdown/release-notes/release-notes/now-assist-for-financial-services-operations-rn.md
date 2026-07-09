---
title: Now Assist for Financial Services Operations \(FSO\) release notes
description: The ServiceNow Now Assist for Financial Services Operations \(FSO\) application brings generative and agentic AI to Financial Services Operations. Features include AI agents, case summarization, disputes intake via Virtual Agent, and support for third-party language models. Now Assist for FSO was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-08-11"
reading_time_minutes: 5
---

# Now Assist for Financial Services Operations \(FSO\) release notes

The ServiceNow® Now Assist for Financial Services Operations \(FSO\) application brings generative and agentic AI to Financial Services Operations. Features include AI agents, case summarization, disputes intake via Virtual Agent, and support for third-party language models. Now Assist for FSO was enhanced and updated in the Zurich release.

## Now Assist for FSO highlights for the Zurich release

Zurich Patch 7

-   Improve your live customer interactions and address customer inquiries more efficiently by using Now Assist for FSO interaction AI agent and summarization skill in the Agentic Contact Center for Banking application.
-   Use Now Assist for FSO customer insights AI agent and summarization skill in the Agentic Contact Center for Banking application to get insights such as customer summaries and financial overviews, for more consistent servicing and faster support.

[Zurich Patch 5](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-5.md)

-   Review changes to Now Assist usage measurement.

[Zurich Patch 4](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-4.md)

-   Leverage AI agents in Now Assist for FSO to automate the ACH dispute resolution process.
-   Use an updated Disputes intake via Virtual Agent conversation flow that supports the revised dispute questionnaire, bypassing questions when inferring answers, and initiating ACH disputes. This flow is for both cards and non-cards \(ACH\).
-   Now Assist for FSO skills and AI agents support model updates in Now LLM Service.
-   Additional role configuration is required for agentic workflows and AI agents included with Now Assist applications.

Early Availability

-   Implement security in Now Assist AI agents and Now Assist for FSO skills with access control lists \(ACLs\).

See [Now Assist for Financial Services Operations \(FSO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/financial-services-operations/now-assist-for-financial-services-operations.md) for more information.

**Important:** Now Assist for FSO is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Zurich release

-   **Agentic Contact Center for Banking AI Agents and skills in FSO**

    Streamline your front-office banking operations by using the Agentic Contact Center for Banking application that provides AI-led experience for CSRs \(Customer Services Representatives\) through the below agents and skills:

    -   Customer 360 Experience
        -   Customer insights AI agent - It generates insights and recommendations that help you identify relevant details and take the next best action efficiently.
        -   Customer summarization skill - It summarizes customer data from multiple FSO applications, then provides customer summaries, product ownership context, financial overviews, and recent activity information.
    -   CSR Interaction
        -   Customer support AI agent - It provides real-time contextual insights and recommended steps that help reduce manual effort and decrease handle time during customer calls.
        -   Call summarization skill - It summarizes active customer calls and other customer information, then displays relevant insights dynamically, eliminating the need to navigate multiple windows during customer calls.

-   **[Standalone AI agents in FSO](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/financial-services-operations/ai-agents-fso.md)**

    Automate ACH dispute resolution using AI-powered agents to assist in these tasks:

    1.  Evaluate merchant analysis
    2.  Evaluate Nacha operating guidelines
    3.  Review ACH dispute return recommendation
    4.  Dispute communication initiation
    These AI agents provide recommended outcomes along with supporting rationale to assist decision-making. However, the final decision remains entirely with the dispute agent.

    Dispute agents can now close tasks faster and with confidence using the **Apply Recommendation** option. With one click, the recommended outcome and rationale are applied and the task is closed, saving time, reducing manual effort, and boosting productivity.

-   **[Now LLM LTS support for Now Assist for FSO](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-llm-model-updates.md)**

    Long term stable \(LTS\) models are part of Now LLM Service and provide longer model stability windows for regulated industries. These models can integrate with tools to provide governance, monitoring, and compliance controls.


-   **[ACL security implementation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/financial-services-operations/using-ai-agent-use-cases-in-now-assist-for-fso.md#section_q24_mlb_jgc)**

    Enable security implementation to execute AI agents, agentic workflows, and generative AI skills through ACLs and user identities in Now Assist for FSO.

    Predefined ACLs are provided for case summarization, Disputes intake via Virtual Agent, and the Help resolve friendly fraud AI agent and agentic workflow.


## Changed in this release

-   **[Changes to Now Assist usage measurement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/monitoring-now-assist-usage.md)**

    Starting with Zurich Early Access, AI usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


-   **[Disputes intake via Virtual Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/financial-services-operations/exploring-now-assist-for-financial-services-operations-fso.md#section_ir3_pn5_lbc)**

    Disputes intake via Virtual Agent has the following updates:

    -   Questions presented to the user for disputes will follow the dispute questionnaire in the disputes playbook.
    -   Bypass inferring answers to certain questions so that customers provide answers directly, ensuring the correct dispute category and dispute reason are determined.
    -   Supports ACH disputes, Disputes intake via Virtual Agent including submission of the Written Statement of Unauthorized Debt \(WSUD\).
    -   Checks if the disputed transaction is already part of an existing case.
-   **[Role configuration required for agentic workflows and AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/aia-role-masking.md)**

    Agentic workflows and AI agents included with Now Assist applications require additional security configuration. If you select **Users with selected roles** for your user access security controls for an agentic workflow or AI agent, you must add the installed roles, or they won't execute. Data access settings must also include these roles. See the documentation for the agentic workflow or AI agent for the specific roles you must add. After the roles are configured, users must have the specified role to invoke the agentic workflow or AI agent.


## Activation information

Install Now Assist for FSO by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Related ServiceNow applications and features

-   **[Using agentic workflows in Now Assist for FSO](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/financial-services-operations/using-ai-agent-use-cases-in-now-assist-for-fso.md)**

    The predefined ACLs in this release apply to the AI agents and agentic workflows in Now Assist for FSO.

-   **[Implement access control in Now Assist AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/aia-security-implementation.md)**

    Configure and manage ACLs for agentic workflows and AI agents in the AI Agent Studio.


**Parent Topic:**[Financial Services Operations release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/financial-services-operations-rn-landing.md)

**Parent Topic:**[Now Assist and agentic AI release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/now-assist-rn-landing.md)


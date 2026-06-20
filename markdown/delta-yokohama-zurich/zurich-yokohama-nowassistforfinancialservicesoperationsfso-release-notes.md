---
title: Combined Now Assist for Financial Services Operations \(FSO\) release notes for upgrades from Yokohama to Zurich
description: Consolidated page of all release notes for Now Assist for Financial Services Operations \(FSO\) from Yokohama to Zurich.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/delta-yokohama-zurich/zurich-yokohama-nowassistforfinancialservicesoperationsfso-release-notes.html
release: zurich
topic_type: reference
last_updated: "2026-06-20"
reading_time_minutes: 8
breadcrumb: [Products combined by family]
---

# Combined Now Assist for Financial Services Operations \(FSO\) release notes for upgrades from Yokohama to Zurich

Consolidated page of all release notes for Now Assist for Financial Services Operations \(FSO\) from Yokohama to Zurich.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Now Assist for Financial Services Operations \(FSO\) release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Yokohama to Zurich.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Now Assist for Financial Services Operations \(FSO\) to Zurich

Before you upgrade to Zurich, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Zurich, new features were introduced for Now Assist for Financial Services Operations \(FSO\).

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   **[Long term stable models](https://servicenow-staging.fluidtopics.net/access?context=long-term-stable-models&family=yokohama&ft:locale=en-US)**

Long term stable \(LTS\) models are part of Now LLM Service and provide longer model stability windows for regulated industries. These models can integrate with tools to provide governance, monitoring, and compliance controls.


-   **[New third-party AI model provider options available for all Now Assist applications](https://servicenow-staging.fluidtopics.net/access?context=exploring-large-language-models&family=yokohama&ft:locale=en-US)**

Google Gemini and AWS Claude are available for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.

-   **[ACL security implementation](https://servicenow-staging.fluidtopics.net/access?context=configuring-now-assist-skills-for-fso&family=yokohama&ft:locale=en-US)**

Enable security implementation to execute AI agents, agentic workflows, and generative AI skills through ACLs and user identities in Now Assist for FSO.

Predefined ACLs are provided for case summarization, Disputes intake via Virtual Agent, and the Help resolve friendly fraud AI agent and agentic workflow.


-   **[Using agentic workflows](https://servicenow-staging.fluidtopics.net/access?context=using-ai-agent-use-cases-in-now-assist-for-fso&family=yokohama&ft:locale=en-US)**

Resolve disputes that are flagged as friendly fraud with comprehensive guidance from the friendly fraud AI agent. Leverage the AI agent's step-by-step recommendations and detailed responses to explain the decisions made regarding disputes. Based on the AI agent recommendations, issue credit to customers, decline disputes, or initiate an exception process.


-   **[Disputes intake via Virtual Agent](https://servicenow-staging.fluidtopics.net/access?context=now-assist-for-financial-services-operations&family=yokohama&ft:locale=en-US)**

Provide an intuitive dialog-based channel experience for your customers to submit details on a dispute case. The dispute intake via Virtual Agent leverages questions that are required by the card processing networks. Now LLM Service rephrases these questions in a conversational format and infers the answers for the unanswered questions from customer responses.


</td></tr><tr><td>

Zurich

</td><td>

-   **[AI agents in FSO](https://servicenow-staging.fluidtopics.net/access?context=ai-agents-fso&family=zurich&ft:locale=en-US)**

Automate ACH dispute resolution using AI-powered agents to assist in these tasks:

    1.  Evaluate merchant analysis
    2.  Evaluate Nacha operating guidelines
    3.  Review ACH dispute return recommendation
    4.  Dispute communication initiation
These AI agents provide recommended outcomes along with supporting rationale to assist decision-making. However, the final decision remains entirely with the dispute agent.

Dispute agents can now close tasks faster and with confidence using the **Apply Recommendation** option. With one click, the recommended outcome and rationale are applied and the task is closed, saving time, reducing manual effort, and boosting productivity.

-   **[Now LLM LTS support for Now Assist for FSO](https://servicenow-staging.fluidtopics.net/access?context=now-llm-model-updates&family=zurich&ft:locale=en-US)**

Long term stable \(LTS\) models are part of Now LLM Service and provide longer model stability windows for regulated industries. These models can integrate with tools to provide governance, monitoring, and compliance controls.


-   **[ACL security implementation](https://servicenow-staging.fluidtopics.net/access?context=using-ai-agent-use-cases-in-now-assist-for-fso&family=zurich&ft:locale=en-US)**

Enable security implementation to execute AI agents, agentic workflows, and generative AI skills through ACLs and user identities in Now Assist for FSO.

Predefined ACLs are provided for case summarization, Disputes intake via Virtual Agent, and the Help resolve friendly fraud AI agent and agentic workflow.


</td></tr></tbody>
</table>## Changes

Between your current release family and Zurich, some changes were made to existing Now Assist for Financial Services Operations \(FSO\) features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   **[Role configuration required for agentic workflows and AI agents](https://servicenow-staging.fluidtopics.net/access?context=aia-role-masking&family=yokohama&ft:locale=en-US)**

Agentic workflows and AI agents included with Now Assist applications require additional security configuration. If you select **Users with selected roles** for your user access security controls for an agentic workflow or AI agent, you must add the installed roles, or they will not execute. Data access settings must also include these roles. See the documentation for the agentic workflow or AI agent for the specific roles you must add.

-   **[Some Now Assist skills are turned on by default](https://servicenow-staging.fluidtopics.net/access?context=now-assist-skills-on-by-default&family=yokohama&ft:locale=en-US)**

The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Yokohama Patch 11\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.
-   **[Changes to Now Assist usage measurement](https://servicenow-staging.fluidtopics.net/access?context=monitoring-now-assist-usage&family=yokohama&ft:locale=en-US)**




</td></tr><tr><td>

Zurich

</td><td>

-   **[Changes to Now Assist usage measurement](https://servicenow-staging.fluidtopics.net/access?context=monitoring-now-assist-usage&family=zurich&ft:locale=en-US)**

Starting with Zurich Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


-   **[Disputes intake via Virtual Agent](https://servicenow-staging.fluidtopics.net/access?context=exploring-now-assist-for-financial-services-operations-fso&family=zurich&ft:locale=en-US)**

Disputes intake via Virtual Agent has the following updates:

    -   Questions presented to the user for disputes will follow the dispute questionnaire in the disputes playbook.
    -   Bypass inferring answers to certain questions so that customers provide answers directly, ensuring the correct dispute category and dispute reason are determined.
    -   Supports ACH disputes, Disputes intake via Virtual Agent including submission of the Written Statement of Unauthorized Debt \(WSUD\).
    -   Checks if the disputed transaction is already part of an existing case.
-   **[Role configuration required for agentic workflows and AI agents](https://servicenow-staging.fluidtopics.net/access?context=aia-role-masking&family=zurich&ft:locale=en-US)**

Agentic workflows and AI agents included with Now Assist applications require additional security configuration. If you select **Users with selected roles** for your user access security controls for an agentic workflow or AI agent, you must add the installed roles, or they won't execute. Data access settings must also include these roles. See the documentation for the agentic workflow or AI agent for the specific roles you must add. After the roles are configured, users must have the specified role to invoke the agentic workflow or AI agent.


</td></tr></tbody>
</table>## Removed

Between your current release family and Zurich, some Now Assist for Financial Services Operations \(FSO\) features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Zurich, some Now Assist for Financial Services Operations \(FSO\) features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate Now Assist for Financial Services Operations \(FSO\).

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

Install Now Assist for FSO by requesting it from ServiceNow Store. 

</td></tr><tr><td>

Zurich

</td><td>

Install Now Assist for FSO by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://servicenow-staging.fluidtopics.net/access?context=sn-store-release-notes&family=zurich&ft:locale=en-US).

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Now Assist for Financial Services Operations \(FSO\) we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

The Now Assist for FSO application requires a Financial Services Operations Professional Plus or Enterprise Plus license.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Now Assist for Financial Services Operations \(FSO\) we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Now Assist for Financial Services Operations \(FSO\), such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Now Assist for Financial Services Operations \(FSO\) we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for Now Assist for Financial Services Operations \(FSO\) we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

[Yokohama Patch 11](https://servicenow-staging.fluidtopics.net/access?context=yokohama-patch-11&family=yokohama&ft:locale=en-US)

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

 See [Now Assist for Financial Services Operations \(FSO\)](https://servicenow-staging.fluidtopics.net/access?context=now-assist-for-financial-services-operations&family=yokohama&ft:locale=en-US) for more information.

</td></tr><tr><td>

Zurich

</td><td>

[Zurich Patch 5](https://servicenow-staging.fluidtopics.net/access?context=zurich-patch-5&family=zurich&ft:locale=en-US)

-   Review changes to Now Assist usage measurement.

 [Zurich Patch 4](https://servicenow-staging.fluidtopics.net/access?context=zurich-patch-4&family=zurich&ft:locale=en-US)

-   Leverage AI agents in Now Assist for FSO to automate the ACH dispute resolution process.
-   Use an updated Disputes intake via Virtual Agent conversation flow that supports the revised dispute questionnaire, bypassing questions when inferring answers, and initiating ACH disputes. This flow is for both cards and non-cards \(ACH\).
-   Now Assist for FSO skills and AI agents support model updates in Now LLM Service.
-   Additional role configuration is required for agentic workflows and AI agents included with Now Assist applications.

 Early Availability

-   Implement security in Now Assist AI agents and Now Assist for FSO skills with access control lists \(ACLs\).

 See [Now Assist for FSO](https://servicenow-staging.fluidtopics.net/access?context=now-assist-for-financial-services-operations&family=zurich&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/delta-yokohama-zurich/rn-combined-intro.md)


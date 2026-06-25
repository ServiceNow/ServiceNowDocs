---
title: Combined Now Assist for Financial Services Operations \(FSO\) release notes for upgrades from Xanadu to Yokohama
description: Consolidated page of all release notes for Now Assist for Financial Services Operations \(FSO\) from Xanadu to Yokohama.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/delta-xanadu-yokohama/yokohama-xanadu-nowassistforfinancialservicesoperationsfso-release-notes.html
release: yokohama
topic_type: reference
last_updated: "2026-06-25"
reading_time_minutes: 7
breadcrumb: [Products combined by family]
---

# Combined Now Assist for Financial Services Operations \(FSO\) release notes for upgrades from Xanadu to Yokohama

Consolidated page of all release notes for Now Assist for Financial Services Operations \(FSO\) from Xanadu to Yokohama.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Now Assist for Financial Services Operations \(FSO\) release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Xanadu to Yokohama.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Now Assist for Financial Services Operations \(FSO\) to Yokohama

Before you upgrade to Yokohama, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Yokohama, new features were introduced for Now Assist for Financial Services Operations \(FSO\).

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   **[ACL security implementation](https://www.servicenow.com/docs/access?context=configuring-security-in-now-assist-for-fso&family=xanadu&ft:locale=en-US)**

Now Assist for FSO can be configured to enable security implementation to execute generative AI skills through ACLs and user identities. Some predefined ACLs are provided for case summarization.


-   **[Case summarization skill](https://www.servicenow.com/docs/access?context=now-assist-case-summary&family=xanadu&ft:locale=en-US)**

Designed to save time for your agents by allowing them to condense a record to a short summary \(when configured\). Now Assist for FSO includes the customized skills that can be configured to use for specific card dispute and insurance claim use cases.

-   **[Now Assist panel](https://www.servicenow.com/docs/access?context=now-assist-panel-overview&family=xanadu&ft:locale=en-US)**

Enable your agents to access Now Assist skills in a panel that is available in Financial Services Workspace. After configuration, agents can summarize the viewed record or a specific case number in Now Assist panel.

-   **[Now Assist Admin console](https://www.servicenow.com/docs/access?context=configuring-now-assist&family=xanadu&ft:locale=en-US)**

Use the Now Assist Admin console to activate and configure the capabilities and individual skills. For example, you can designate which roles have access to a skill, or whether the skill is available in Financial Services Workspace, the Now Assist panel, or both.

-   **[Skill availability restricted by user role](https://www.servicenow.com/docs/access?context=configure-now-assist-for-fso&family=xanadu&ft:locale=en-US)**

Specify the roles that can access the case summarization skill.


</td></tr><tr><td>

Yokohama

</td><td>

-   **[Long term stable models](https://www.servicenow.com/docs/access?context=long-term-stable-models&family=yokohama&ft:locale=en-US)**

Long term stable \(LTS\) models are part of Now LLM Service and provide longer model stability windows for regulated industries. These models can integrate with tools to provide governance, monitoring, and compliance controls.


-   **[New third-party AI model provider options available for all Now Assist applications](https://www.servicenow.com/docs/access?context=exploring-large-language-models&family=yokohama&ft:locale=en-US)**

Google Gemini and AWS Claude are available for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.

-   **[ACL security implementation](https://www.servicenow.com/docs/access?context=configuring-now-assist-skills-for-fso&family=yokohama&ft:locale=en-US)**

Enable security implementation to execute AI agents, agentic workflows, and generative AI skills through ACLs and user identities in Now Assist for FSO.

Predefined ACLs are provided for case summarization, Disputes intake via Virtual Agent, and the Help resolve friendly fraud AI agent and agentic workflow.


-   **[Using agentic workflows](https://www.servicenow.com/docs/access?context=using-ai-agent-use-cases-in-now-assist-for-fso&family=yokohama&ft:locale=en-US)**

Resolve disputes that are flagged as friendly fraud with comprehensive guidance from the friendly fraud AI agent. Leverage the AI agent's step-by-step recommendations and detailed responses to explain the decisions made regarding disputes. Based on the AI agent recommendations, issue credit to customers, decline disputes, or initiate an exception process.


-   **[Disputes intake via Virtual Agent](https://www.servicenow.com/docs/access?context=now-assist-for-financial-services-operations&family=yokohama&ft:locale=en-US)**

Provide an intuitive dialog-based channel experience for your customers to submit details on a dispute case. The dispute intake via Virtual Agent leverages questions that are required by the card processing networks. Now LLM Service rephrases these questions in a conversational format and infers the answers for the unanswered questions from customer responses.


</td></tr></tbody>
</table>## Changes

Between your current release family and Yokohama, some changes were made to existing Now Assist for Financial Services Operations \(FSO\) features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

-   **[Role configuration required for agentic workflows and AI agents](https://www.servicenow.com/docs/access?context=aia-role-masking&family=yokohama&ft:locale=en-US)**

Agentic workflows and AI agents included with Now Assist applications require additional security configuration. If you select **Users with selected roles** for your user access security controls for an agentic workflow or AI agent, you must add the installed roles, or they will not execute. Data access settings must also include these roles. See the documentation for the agentic workflow or AI agent for the specific roles you must add.

-   **[Some Now Assist skills are now turned on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&family=yokohama&ft:locale=en-US)**

The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Yokohama Patch 11\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.
-   **[Changes to Now Assist usage measurement](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&family=yokohama&ft:locale=en-US)**




</td></tr></tbody>
</table>## Removed

Between your current release family and Yokohama, some Now Assist for Financial Services Operations \(FSO\) features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Yokohama, some Now Assist for Financial Services Operations \(FSO\) features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

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

Xanadu

</td><td>

Install Now Assist for FSO by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=xanadu&ft:locale=en-US).

</td></tr><tr><td>

Yokohama

</td><td>

Install Now Assist for FSO by requesting it from ServiceNow Store. 

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Now Assist for Financial Services Operations \(FSO\) we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

The Now Assist for FSO application requires a Financial Services Operations Professional Plus or Enterprise Plus license.

</td></tr><tr><td>

Yokohama

</td><td>

The Now Assist for FSO application requires a Financial Services Operations Professional Plus or Enterprise Plus license.

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Now Assist for Financial Services Operations \(FSO\) we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

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

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

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

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

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

Xanadu

</td><td>

Xanadu Patch 10

 Implement security in Now Assist for FSO skills with access control lists \(ACLs\).

 [Early Availability](https://www.servicenow.com/docs/access?context=xanadu-all-other-fixes&family=xanadu&ft:locale=en-US)

 Enable agents to review card dispute and insurance claim cases more effectively by using the case summarization skill to generate an overview of key details.

 See [Now Assist for Financial Services Operations \(FSO\)](https://www.servicenow.com/docs/access?context=now-assist-for-financial-services-operations&family=xanadu&ft:locale=en-US) for more information.

</td></tr><tr><td>

Yokohama

</td><td>

[Yokohama Patch 11](https://www.servicenow.com/docs/access?context=yokohama-patch-11&family=yokohama&ft:locale=en-US)

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

 See [Now Assist for Financial Services Operations \(FSO\)](https://www.servicenow.com/docs/access?context=now-assist-for-financial-services-operations&family=yokohama&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/delta-xanadu-yokohama/rn-combined-intro.md)


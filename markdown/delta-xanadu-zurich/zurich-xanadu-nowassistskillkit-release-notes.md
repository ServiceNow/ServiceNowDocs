---
title: Combined Now Assist Skill Kit release notes for upgrades from Xanadu to Zurich
description: Consolidated page of all release notes for Now Assist Skill Kit from Xanadu to Zurich.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/delta-xanadu-zurich/zurich-xanadu-nowassistskillkit-release-notes.html
release: zurich
topic_type: reference
last_updated: "2026-06-22"
reading_time_minutes: 9
breadcrumb: [Products combined by family]
---

# Combined Now Assist Skill Kit release notes for upgrades from Xanadu to Zurich

Consolidated page of all release notes for Now Assist Skill Kit from Xanadu to Zurich.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Now Assist Skill Kit release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Xanadu to Zurich.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Now Assist Skill Kit to Zurich

Before you upgrade to Zurich, review these pre- and post-upgrade tasks and complete the tasks as needed.

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

If you customized UI actions or other items that are associated with Now Assist skills, ensure that your customized code is updated with the new skill releases. Otherwise, certain functions may not work as expected.

 If you run into issues when you're upgrading a Now Assist product, see [KB1637452: Issues and mitigation for Now Assist \(Generative AI\) Applications and Plugin updates](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1637452). You may need to log in to view the article.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Zurich, new features were introduced for Now Assist Skill Kit.

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

-   **[New skill deployment option](https://servicenow-staging.fluidtopics.net/access?context=configure-skill-settings&family=yokohama&ft:locale=en-US)**

Deploy skills using UI Builder.

-   **[Choose a language for data generation](https://servicenow-staging.fluidtopics.net/access?context=na-data-kit-generate-data&family=yokohama&ft:locale=en-US)**

When you create synthetic data, you can select what language you want to receive the data in.

-   **[AI-assisted ground truth](https://servicenow-staging.fluidtopics.net/access?context=add-ground-truth&family=yokohama&ft:locale=en-US)**

Use AI to assist creating ground truth for your data.

-   **[Import data with a CSV file](https://servicenow-staging.fluidtopics.net/access?context=add-dataset&family=yokohama&ft:locale=en-US)**

Import data from a CSV file to create a dataset.

-   **[Create a custom data generator](https://servicenow-staging.fluidtopics.net/access?context=create-custom-data-generator&family=yokohama&ft:locale=en-US)**

Create and use a custom data generator to create synthetic data.


-   **[Customize ServiceNow skills in Now Assist Skill Kit to tailor skills to meet your specific business requirements.](https://servicenow-staging.fluidtopics.net/access?context=clone-and-edit-servicenow-skill&family=yokohama&ft:locale=en-US)**

Eligible skills provided in ServiceNow Now Assist applications can be cloned in Now Assist Skill Kit so that you can edit the prompt or change the AI service provider. Editing the prompt enables you to arrange the formatting and content of the large language model \(LLM\) response. After the skill is edited, activate the edited skill in the Now Assist Admin console to enable it.

-   **[Add and manage tools visually in the new Tools editor, including decision branching, to execute different tools for your skill.](https://servicenow-staging.fluidtopics.net/access?context=add-a-tool&family=yokohama&ft:locale=en-US)**

Adding decision branches between tools enables you to define the conditions that must be met for a tool to run. If no conditions are met, the default branch's step is executed.


</td></tr><tr><td>

Zurich

</td><td>

-   **[Labelling](https://servicenow-staging.fluidtopics.net/access?context=nadk-labelling&family=zurich&ft:locale=en-US)Use labeling workflows to annotate UI templates**

Use the labeling framework to create and manage ground truth data. Published data collections can now be turned into labeling projects. Each record becomes a task assigned to labelers who annotate using pre-configured UI templates

-   **[s](https://servicenow-staging.fluidtopics.net/access?context=configure-skill-prompt&family=zurich&ft:locale=en-US)Structured output support for AI responses**

Enables consistent parsing in agentic workflows and reduces ambiguity in downstream automation.

-   **[Use multi-table data generator](https://servicenow-staging.fluidtopics.net/access?context=use-multi-table-data-generator&family=zurich&ft:locale=en-US)New multi-table synthetic data generation option**

You can generate related records across multiple tables in a single operation. You no longer need to generate each table separately and manually link records. Define your table relationships, set the cardinality and Now Assist Data Kit generates coherent, referentially linked records across all tables in one pass, with foreign key integrity maintained automatically. 

-   **[Create a model](https://servicenow-staging.fluidtopics.net/access?context=create-model&family=zurich&ft:locale=en-US)AI Control Tower integration with custom LLMs.**

Improve oversight and compliance for AI deployments with formal approval flows for custom models.

-   **[Now Assist SDK roles](https://servicenow-staging.fluidtopics.net/access?context=na-skill-kit-roles&family=zurich&ft:locale=en-US)Update to the abilities of the admin role**

The sn\_skill\_builder.admin role is now broken into smaller, task-specific roles, including a custom LLM-specific admin role.


-   **[Create a model](https://servicenow-staging.fluidtopics.net/access?context=create-model&family=zurich&ft:locale=en-US)**

When you bring your own model you can keep data in your own environment and fine-tune it to meet your specific needs.


-   **[New third-party AI model provider options available for all Now Assist applications](https://servicenow-staging.fluidtopics.net/access?context=exploring-large-language-models&family=zurich&ft:locale=en-US)**

Google Gemini and AWS Claude are available for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.

-   **[New skill deployment option](https://servicenow-staging.fluidtopics.net/access?context=configure-skill-settings&family=zurich&ft:locale=en-US)**

Deploy skills using UI Builder.

-   **[Choose a language for data generation](https://servicenow-staging.fluidtopics.net/access?context=na-data-kit-generate-data&family=zurich&ft:locale=en-US)**

When you create synthetic data, you can select what language you want to receive the data in.

-   **[AI-assisted ground truth](https://servicenow-staging.fluidtopics.net/access?context=add-ground-truth&family=zurich&ft:locale=en-US)**

Use AI to assist creating ground truth for your data.

-   **[Import data with a CSV file](https://servicenow-staging.fluidtopics.net/access?context=add-dataset&family=zurich&ft:locale=en-US)**

Import data from a CSV file to create a dataset.

-   **[Create a custom data generator](https://servicenow-staging.fluidtopics.net/access?context=create-custom-data-generator&family=zurich&ft:locale=en-US)**

Create and use a custom data generator to create synthetic data.


</td></tr></tbody>
</table>## Changes

Between your current release family and Zurich, some changes were made to existing Now Assist Skill Kit features.

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

-   **[Changes to Now Assist usage measurement](https://servicenow-staging.fluidtopics.net/access?context=monitoring-now-assist-usage&family=yokohama&ft:locale=en-US)**

Starting with Yokohama Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).

-   **[Some Now Assist skills are turned on by default](https://servicenow-staging.fluidtopics.net/access?context=now-assist-skills-on-by-default&family=yokohama&ft:locale=en-US)**

The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Yokohama Patch 11\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.
-   ****

</td></tr><tr><td>

Zurich

</td><td>

-   **[Changes to Now Assist usage measurement](https://servicenow-staging.fluidtopics.net/access?context=monitoring-now-assist-usage&family=zurich&ft:locale=en-US)**

Starting with Zurich Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


</td></tr></tbody>
</table>## Removed

Between your current release family and Zurich, some Now Assist Skill Kit features or functionality were removed.

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

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Zurich, some Now Assist Skill Kit features or functionality were deprecated.

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

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate Now Assist Skill Kit.

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

Now Assist features are available with activation of any Now Assist plugin from the ServiceNow Store. The following plugins are available:

-   


</td></tr><tr><td>

Zurich

</td><td>

Now Assist features are available with activation of any Now Assist plugins from ServiceNow Store. The following plugins are available:

-   [Now Assist for APO](https://servicenow-staging.fluidtopics.net/access?context=now-assist-apo&family=zurich&ft:locale=en-US)
-   [Now Assist for App Engine](https://servicenow-staging.fluidtopics.net/access?context=add-ai-to-custom-apps-with-now-assist-for-app-engine-enterprise&family=zurich&ft:locale=en-US)
-   [Now Assist for Configuration Management Database \(CMDB\)](https://servicenow-staging.fluidtopics.net/access?context=now-assist-landing-cmdb&family=zurich&ft:locale=en-US)
-   [Now Assist for CWM](https://servicenow-staging.fluidtopics.net/access?context=now-assist-for-cwm-landing&family=zurich&ft:locale=en-US)
-   [Now Assist for Creator](https://servicenow-staging.fluidtopics.net/access?context=now-assist-for-creator-landing&family=zurich&ft:locale=en-US)
-   [Now Assist for CSM](https://servicenow-staging.fluidtopics.net/access?context=now-assist-csm&family=zurich&ft:locale=en-US)
-   [Now Assist for Employee Experience](https://servicenow-staging.fluidtopics.net/access?context=now-assisit-employee-exp&family=zurich&ft:locale=en-US)
-   [Now Assist for Enterprise Architecture \(EA\)](https://servicenow-staging.fluidtopics.net/access?context=now-assist-ea&family=zurich&ft:locale=en-US)
-   [Now Assist for ESG](https://servicenow-staging.fluidtopics.net/access?context=now-assist-for-esg&family=zurich&ft:locale=en-US)
-   [Now Assist for FSM](https://servicenow-staging.fluidtopics.net/access?context=now-assist-fsm&family=zurich&ft:locale=en-US)
-   [Now Assist for FSO](https://servicenow-staging.fluidtopics.net/access?context=now-assist-for-financial-services-operations&family=zurich&ft:locale=en-US)
-   [Now Assist for Hardware Asset Management \(HAM\)](https://servicenow-staging.fluidtopics.net/access?context=now-assist-ham&family=zurich&ft:locale=en-US)
-   [Now Assist for Health and Safety](https://servicenow-staging.fluidtopics.net/access?context=now-assist-hs-landing&family=zurich&ft:locale=en-US)
-   [Now Assist for HR Service Delivery \(HRSD\)](https://servicenow-staging.fluidtopics.net/access?context=now-assist-hrsd&family=zurich&ft:locale=en-US)
-   [Now Assist](https://servicenow-staging.fluidtopics.net/access?context=now-assist-for-irm&family=zurich&ft:locale=en-US)
-   [Now Assist for ITOM](https://servicenow-staging.fluidtopics.net/access?context=now-assist-itom&family=zurich&ft:locale=en-US)
-   [Now Assist for IT Service Management \(ITSM\)](https://servicenow-staging.fluidtopics.net/access?context=now-assist-itsm&family=zurich&ft:locale=en-US)
-   [Now Assist for Legal Service Delivery \(LSD\)](https://servicenow-staging.fluidtopics.net/access?context=now-assist-lsd-landing&family=zurich&ft:locale=en-US)
-   [Now Assist for OTM](https://servicenow-staging.fluidtopics.net/access?context=now-assist-for-otm-landing&family=zurich&ft:locale=en-US)
-   [Now Assist for OTSM](https://servicenow-staging.fluidtopics.net/access?context=now-assist-for-operational-technology-service-management&family=zurich&ft:locale=en-US)
-   [Now Assist for Order Management](https://servicenow-staging.fluidtopics.net/access?context=now-assist-order-management&family=zurich&ft:locale=en-US)
-   [Now Assist for PSDS](https://servicenow-staging.fluidtopics.net/access?context=now-assist-for-psds&family=zurich&ft:locale=en-US)
-   [Now Assist for SOM](https://servicenow-staging.fluidtopics.net/access?context=now-assist-for-sales-and-order-management-som&family=zurich&ft:locale=en-US)
-   [Now Assist for Security Incident Response](https://servicenow-staging.fluidtopics.net/access?context=now-assist-security-incident-landing&family=zurich&ft:locale=en-US)
-   [Now Assist for Software Asset Management \(SAM\)](https://servicenow-staging.fluidtopics.net/access?context=now-assist-sam&family=zurich&ft:locale=en-US)
-   [Now Assist for SLO](https://servicenow-staging.fluidtopics.net/access?context=now-assist-slo&family=zurich&ft:locale=en-US)
-   [Now Assist for SPO](https://servicenow-staging.fluidtopics.net/access?context=now-assist-spo&family=zurich&ft:locale=en-US)
-   [Now Assist for Strategic Portfolio Management \(SPM\)](https://servicenow-staging.fluidtopics.net/access?context=now-assist-spm&family=zurich&ft:locale=en-US)
-   [Now Assist for TMT](https://servicenow-staging.fluidtopics.net/access?context=now-assist-spmc&family=zurich&ft:locale=en-US)
-   [Now Assist](https://servicenow-staging.fluidtopics.net/access?context=now-assist-tprm&family=zurich&ft:locale=en-US)
-   [Now Assist for Workplace Service Delivery \(WSD\)](https://servicenow-staging.fluidtopics.net/access?context=now-assist-wsd-landing&family=zurich&ft:locale=en-US)
-   [Now Assist for Vulnerability Response](https://servicenow-staging.fluidtopics.net/access?context=now-assist-for-vulnerability-response-landing&family=zurich&ft:locale=en-US)
-   [Now Assist for Zero Copy Connectors](https://servicenow-staging.fluidtopics.net/access?context=now-assist-for-zero-copy-connector-for-erp&family=zurich&ft:locale=en-US)

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Now Assist Skill Kit we have noted them here.

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

The Next Experience UI Framework must be enabled to use the Now Assist panel.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Now Assist Skill Kit we have noted them here.

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

Now Assist supports various browsers, including Google Chrome and Microsoft Edge. Now Assist isn’t supported in Microsoft Internet Explorer.

</td></tr><tr><td>

Zurich

</td><td>

Now Assist supports various browsers, including Google Chrome and Microsoft Edge. Now Assist isn’t supported in Microsoft Internet Explorer.

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Now Assist Skill Kit, such as specific requirements or compliance levels.

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

Admins can enable an optional Voice Input setting for the Now Assist panel that enables users to interact with the panel using their voice or in voice assist mode.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Now Assist Skill Kit we have noted them here.

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

Now Assist supports Dynamic Translation for Yokohama.

</td></tr><tr><td>

Zurich

</td><td>

Now Assist supports Dynamic Translation for Zurich.

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for Now Assist Skill Kit we have noted them here.

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

[Yokohama Patch 11](https://servicenow-staging.fluidtopics.net/access?context=yokohama-patch-11&family=yokohama&ft:locale=en-US)

-   Review changes to Now Assist usage measurement.
-   Some Now Assist skills, agents, and agentic workflows are on by default.
-   Additional role configuration is required for agentic workflows and AI agents included with Now Assist applications.

 Yokohama Patch 6

-   Use UI Builder to deploy custom skills.
-   Import data into Now Assist Skill Kit with a CSV file.
-   Use AI to create ground truth for your data.
-   Use a custom data generator to create synthetic datasets.

 -   Users can create synthetic data in Now Assist Data Kit.
-   Generated synthetic data can be saved as a dataset.
-   Add and manage tools of a custom skill, visually in the new Tools editor, including conditional execution of tools.
-   Customize ServiceNow skills with new prompts or providers in Now Assist Skill Kit to suit your specific business needs.

 See [Now Assist SDK](https://servicenow-staging.fluidtopics.net/access?context=now-assist-skill-kit-landing&family=yokohama&ft:locale=en-US) for more information.

</td></tr><tr><td>

Zurich

</td><td>

[Zurich Patch 5](https://servicenow-staging.fluidtopics.net/access?context=zurich-patch-5&family=zurich&ft:locale=en-US)

-   Review changes to Now Assist usage measurement.

 [Zurich Patch 4](https://servicenow-staging.fluidtopics.net/access?context=zurich-patch-4&family=zurich&ft:locale=en-US)

-   Create a custom model to meet your specific needs and control behavior.
-   Customize ServiceNow skills by modifying the prompt, inputs, and providers.

 [Zurich Patch 1](https://servicenow-staging.fluidtopics.net/access?context=zurich-patch-1&family=zurich&ft:locale=en-US)

-   Set up a security access control list to verify user authentication for Now Assist Skill Kit.
-   Use Document Intelligence as a tool when you create a skill.

 -   Use UI Builder to deploy custom skills.
-   Use a custom data generator to create synthetic datasets.

 See [Now Assist SDK](https://servicenow-staging.fluidtopics.net/access?context=now-assist-skill-kit-landing&family=zurich&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/delta-xanadu-zurich/rn-combined-intro.md)


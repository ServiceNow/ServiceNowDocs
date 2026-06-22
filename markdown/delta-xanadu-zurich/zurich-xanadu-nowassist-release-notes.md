---
title: Combined Now Assist release notes for upgrades from Xanadu to Zurich
description: Consolidated page of all release notes for Now Assist from Xanadu to Zurich.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/delta-xanadu-zurich/zurich-xanadu-nowassist-release-notes.html
release: zurich
topic_type: reference
last_updated: "2026-06-22"
reading_time_minutes: 29
breadcrumb: [Products combined by family]
---

# Combined Now Assist release notes for upgrades from Xanadu to Zurich

Consolidated page of all release notes for Now Assist from Xanadu to Zurich.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Now Assist release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Xanadu to Zurich.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Now Assist to Zurich

Before you upgrade to Zurich, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

If you customized UI actions or other items that are associated with Now Assist skills, confirm that your customized code is updated with the new skill releases. Otherwise, certain functions may not work as expected.

 If you run into issues when you're upgrading a Now Assist product, see [KB1637452: Issues and mitigation for Now Assist \(Generative AI\) Applications and Plugin updates](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1637452). You may need to log in to view the article.

</td></tr><tr><td>

Yokohama

</td><td>

If you customized UI actions or other items that are associated with Now Assist skills, ensure that your customized code is updated with the new skill releases. Otherwise, certain functions may not work as expected.

 If you run into issues when you're upgrading a Now Assist product, see [KB1637452: Issues and mitigation for Now Assist \(Generative AI\) Applications and Plugin updates](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1637452). You may need to log in to view the article.

</td></tr><tr><td>

Zurich

</td><td>

If you customized UI actions or other items that are associated with Now Assist skills, confirm that your customized code is updated with the new skill releases. Otherwise, certain functions might not work as expected.

 If you run into issues when you're upgrading a Now Assist product, see the [Issues and mitigation for Now Assist \(Generative AI\) Applications and Plugin updates \[KB1637452\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1637452) article in the Now Support Knowledge Base. You might need to log in to view the article.

 The existing Access Control Lists \(ACLs\) will be updated to replace the 'admin' role with specific, purpose-driven granular roles within scripts or security attributes. As part of this update, the `getRoles()` API will be replaced with the `hasRole()` API for authorization purposes. Additionally, all references to the 'admin' role in the code will be substituted with the new feature-specific granular roles for authorization use cases. Read [https://www.servicenow.com/docs/r/platform-security/granular-admin-roles.html](https://www.servicenow.com/docs/r/platform-security/granular-admin-roles.html) to learn more.

</td></tr></tbody>
</table>## New features

Between your current release family and Zurich, new features were introduced for Now Assist.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   **[Now Assist Readiness Evaluation](https://servicenow-staging.fluidtopics.net/access?context=now-assist-readiness-evaluation-landing-page&family=xanadu&ft:locale=en-US)**

Use the Now Assist Readiness Evaluation app to help you evaluate your organization's readiness to implement agentic and generative AI Now Assist capabilities.

Assessments for agentic AI include:

    -   IT Service Management \(ITSM\)
    -   Customer Service Management \(CSM\)
Assessments for generative AI include:

    -   AI Search
    -   Virtual Agent \(VA\)
    -   IT Service Management \(ITSM\)
    -   Customer Service Management \(CSM\)
    -   HR Service Delivery \(HRSD\)
Results shown are estimates. You should evaluate results provided by Now Assist Readiness Evaluation for accuracy and appropriateness for your use case.


-   **[Now Assist Guardian adds guardrails to log, block, and redirect unwanted content](https://servicenow-staging.fluidtopics.net/access?context=now-assist-guardian&family=xanadu&ft:locale=en-US)**

Protect your users from offensive content, certain kinds of prompt injection attacks, and sensitive topics by logging attempts, blocking content, or redirecting to a new Virtual Agent topic.

-   **[Translation for Now Assist with native translation](https://servicenow-staging.fluidtopics.net/access?context=translation-for-now-assist&family=xanadu&ft:locale=en-US)**

Use the native translation capabilities of the Now LLM Service models or to translate user-generated and LLM-generated content into the preferred languages of your users.

-   **[Troubleshoot a Now Assist skill](https://servicenow-staging.fluidtopics.net/access?context=troubleshoot-a-now-assist-skill&family=xanadu&ft:locale=en-US)**

Run diagnostics on certain Now Assist skills to identify common configuration errors that help to prevent your skills from working as intended.

-   **[Analyze Now Assist performance](https://servicenow-staging.fluidtopics.net/access?context=now-assist-analytics&family=xanadu&ft:locale=en-US)**

Use the Now Assist Analytics dashboard to monitor the usage and performance of generative AI features and capabilities offered under Now Assist.

-   **[Configure and use a retriever with Now Assist Skill Kit](https://servicenow-staging.fluidtopics.net/access?context=add-retriever&family=xanadu&ft:locale=en-US)**

Augment and add context to your prompts with AI Search results from custom retriever inputs.

-   **[Get prompt assistance with Now Assist Skill Kit](https://servicenow-staging.fluidtopics.net/access?context=use-prompt-assistance&family=xanadu&ft:locale=en-US)**

Use prompt assistance to get a jump-start with your prompt development by selecting an example from the prompt library or using Now Assist to generate one.

-   **[Evaluate skill prompts](https://servicenow-staging.fluidtopics.net/access?context=evaluate-prompt&family=xanadu&ft:locale=en-US)**

Evaluate your prompts created within Now Assist Skill Kit using data collections created within Now Assist Data Kit. Evaluations return information on the correctness and faithfulness of the responses from running the custom skill.

-   **[View skill run test history](https://servicenow-staging.fluidtopics.net/access?context=test-prompt-template&family=xanadu&ft:locale=en-US)**

View the history of your test results to assist your understanding of how changes to the prompt have adjusted the outcome.

-   **[Generate article with multi-language](https://servicenow-staging.fluidtopics.net/access?context=Now-Assist-generate-article-using-multilanguage-support&family=xanadu&ft:locale=en-US)**

Generate a Knowledge article for an incident, case, or other supported task type in languages other than English using the multi-language capabilities of Now Assist.

-   **[Edit article with context menu](https://servicenow-staging.fluidtopics.net/access?context=Now-Assist-generate-article-using-context-menu&family=xanadu&ft:locale=en-US)**

Use generative AI capabilities of Now Assist to shorten or elaborate content within a Knowledge article.

-   **[Use Now Assist Data Kit to add a dataset to the data catalog](https://servicenow-staging.fluidtopics.net/access?context=now-assist-data-kit-landing&family=xanadu&ft:locale=en-US)**

Create a data collection and select the sampling data for publication. Once published, the evaluation data is available in Now Assist Skill Kit.

-   **[Now Assist context menu](https://servicenow-staging.fluidtopics.net/access?context=now-assist-write-overview&family=xanadu&ft:locale=en-US)**
    -   Write with Now Assist is now called the Now Assist context menu.
    -   Explain the assessed and calculated change request risk with the Now Assist context menu in workspaces and UI16.
    -   Use the **Elaborate** and **Shorten** content editing capabilities of the Now Assist context menu in Knowledge articles.
    -   Configure the maximum number of content refinement calls using the Now Assist context menu.
    -   Use the Now Assist context menu recommendations to compose an email and complete the drafts.

-   **[Dynamic theming enables different themes to be applied to chat summarization cards](https://servicenow-staging.fluidtopics.net/access?context=now-assist-chat-summary&family=xanadu&ft:locale=en-US)**

Support dynamic theming for chat summarization cards.

-   **[Write with Now Assist](https://servicenow-staging.fluidtopics.net/access?context=now-assist-write-overview&family=xanadu&ft:locale=en-US)**

Enable your agents to use Write with Now Assist for generative AI-powered text generation and editing assistance. This feature helps to improve and streamline their writing responsibilities.

-   **Use Now Assist [Platform skills](https://servicenow-staging.fluidtopics.net/access?context=na-platform-skills&family=xanadu&ft:locale=en-US)**
    -   Use generative AI Platform skills in the Platform workflow starting with the Xanadu release to enhance and streamline your user experience.
    -   Enter search commands in plain language to retrieve and filter records and tables by using the [Navigation](https://servicenow-staging.fluidtopics.net/access?context=now-assist-global-navigation&family=xanadu&ft:locale=en-US) skill.
-   **Use [Now Assist Skill Kit](https://servicenow-staging.fluidtopics.net/access?context=now-assist-skill-kit-landing&family=xanadu&ft:locale=en-US) for Generative AI app developers**

Create and activate custom prompts and skills for your Now Assist agent use cases.

-   **Generate a knowledge article from multiple cases or incidents with [Now Assist in Knowledge Management](https://servicenow-staging.fluidtopics.net/access?context=Now-Assist-generate-article-coreui&family=xanadu&ft:locale=en-US)**

Draft Knowledge articles quickly from a configurable workspace or the classic environment based on similar cases or incidents with  Now Assist. Knowledge articles can be generated by selecting from a list of similar cases or incidents, case or incident numbers, or even by searching keywords specific to a case or incident.


</td></tr><tr><td>

Yokohama

</td><td>

-   **[Monitor sensitive topic invocations](https://servicenow-staging.fluidtopics.net/access?context=reference-for-generative-ai-controller&family=yokohama&ft:locale=en-US)**

Access the Gen AI Metrics \[sys\_generative\_ai\_metric\] table to review the logged invocations of sensitive topics and gain insights into how these topics are being triggered and monitored.


-   **[Now Assist Readiness Evaluation](https://servicenow-staging.fluidtopics.net/access?context=now-assist-readiness-evaluation-landing-page&family=yokohama&ft:locale=en-US)**

Use the Now Assist Readiness Evaluation app to help you evaluate your organization's readiness to implement agentic and generative AI Now Assist capabilities.

Assessments for agentic AI include:

    -   IT Service Management \(ITSM\)
    -   Customer Service Management \(CSM\)
Assessments for generative AI include:

    -   AI Search
    -   Virtual Agent \(VA\)
    -   IT Service Management \(ITSM\)
    -   Customer Service Management \(CSM\)
    -   HR Service Delivery \(HRSD\)
Results shown are estimates. You should evaluate results provided by Now Assist Readiness Evaluation for accuracy and appropriateness for your use case.


-   **[Manage large language models](https://servicenow-staging.fluidtopics.net/access?context=manage-large-language-models&family=yokohama&ft:locale=en-US)**

Choose and update your preferred large language model \(LLM\) provider at the instance, skill or skill group level for Now Assist out-of-box skills with ServiceNow® third-party model strategy.

Deactivate skills that are not compliant with any of the LLM providers and access the audit history to view updates by the AI steward.

-   **[Configure multilingual service for Now Assist applications](https://servicenow-staging.fluidtopics.net/access?context=enable-dynamic-translation-for-now-assist-applications&family=yokohama&ft:locale=en-US)**

Manage the default and supported languages by the different LLM providers under Multilingual service for translation.

-   **[\[Placeholder link text to key bundle-platai.now-assist-email-recommendation\]](https://servicenow-staging.fluidtopics.net/access?context=now-assist-email-recommendation&family=yokohama&ft:locale=en-US)**

Access the citations to the articles referenced from the knowledge base. Explore references and insert the suggested reply to your email.

-   **[Now Assist Guardian supports third-party LLMs](https://servicenow-staging.fluidtopics.net/access?context=now-assist-guardian&family=yokohama&ft:locale=en-US)**

Extend guardrail support to third-party LLMs, such as Amazon Bedrock, Google Cloud \(AI Studio and Vertex\), and OpenAI to ensure any inappropriate content is logged and blocked during content generation.


-   **[Increase the maximum response token limit for custom skills](https://servicenow-staging.fluidtopics.net/access?context=configure-skill-prompt&family=yokohama&ft:locale=en-US)**

Increase the maximum response token limit for Now Assist custom skill beyond default value 1000 to support dynamic pricing based on output tokens and calculate the price for each skill executed per assist.


-   **[Exploring Now Assist](https://servicenow-staging.fluidtopics.net/access?context=exploring-now-assist-platform&family=yokohama&ft:locale=en-US)**

Access the Now Assist skills through an identifier tab on the Now Assist Admin console, and find the associated workflows.

Navigate to your skills by using the intuitive list or grid view. The skill details are displayed, which means that you don't have to make additional selections.

Access the Data privacy section under Now Assist Admin settings. View and edit the data privacy policies that apply to your Now Assist skills.

-   **[Accessing the external content in Now Assist panel Q&amp;A capability](https://servicenow-staging.fluidtopics.net/access?context=now-assist-multi-turn-qna&family=yokohama&ft:locale=en-US)**

Get relevant answers to your questions from external content sources, such as Microsoft SharePoint, Google Drive, and Confluence Cloud, within the Now Assist panel, without manual indexing. Each response shows the source of information to reference later.

-   **[Enhanced log visibility](https://servicenow-staging.fluidtopics.net/access?context=now-assist-guardian&family=yokohama&ft:locale=en-US)**
    -   Access the Generative AI Metric table \[sys\_generative\_ai\_metric\] to gain insights into the guardian logs and determine if they are for monitoring only or for both logging and blocking. Each guardrail shows its status value as Monitor, Block, or Off, to help administrators to manage their security policies.
    -   View the logs of masking that involve personal identifiable information \(PII\) in the Generative AI Metric table \[sys\_generative\_ai\_metric\]. You can identify which data is masked, the type of request, system response, processing time, errors, or error codes.
-   **[\[Placeholder link text to key bundle-platai.now-assist-rn-summarization\]](https://servicenow-staging.fluidtopics.net/access?context=now-assist-rn-summarization&family=yokohama&ft:locale=en-US)**

Define the output field destination so that you can select any multi-line text field from the base table You can customize incident forms and improve the usability of the resolution notes generation skill.

Enable requesters to extract information from emails and email attachments to generate tasks. This email-to-task agentic workflow effectively addresses the challenge of task creation from emails.

-   **[Identify and review articles](https://servicenow-staging.fluidtopics.net/access?context=Now-Assist-identify-and-review-duplicate-articles&family=yokohama&ft:locale=en-US)**

Identify duplicate Knowledge articles by using Now Assist capabilities. You can review the list and deselect articles that you don’t consider to be duplicates.

-   **[Streaming responses](https://servicenow-staging.fluidtopics.net/access?context=now-assist-panel-overview&family=yokohama&ft:locale=en-US)**

Enable streaming responses on the Now Assist panel. Only synthesized responses are streamed.

-   **[Multiple Now Assist panels](https://servicenow-staging.fluidtopics.net/access?context=now-assist-panel-overview&family=yokohama&ft:locale=en-US)**

Create separate, independent Now Assist panels that work across Next Experience and ServiceNow® Studio app shells.

-   **[Create Now Assist context Menu configuration](https://servicenow-staging.fluidtopics.net/access?context=create-now-assist-configuration-with-guided-setup&family=yokohama&ft:locale=en-US)**

Create a Now Assist context menu configuration for a streamlined custom skill deployment process with the help of a guided setup.


-   **[Now Assist Guardian analytics](https://servicenow-staging.fluidtopics.net/access?context=now-assist-guardian-analytics&family=yokohama&ft:locale=en-US)**

Monitor the performance of offensive content and prompt injections guardrails with the help of the Now Assist Guardian analytics dashboard.

-   **[Configuring Now Assist settings and features](https://servicenow-staging.fluidtopics.net/access?context=configuring-na-landing&family=yokohama&ft:locale=en-US)**

For custom skills, explore an additional display option in the form of **Conversational experiences**. You can select Now Assist Virtual Agent to assist you with the display.

Create and activate a Now Assist skill copy, and have both the original skill and its copy to remain active simultaneously.


-   **[Now Assist Context Menu usage dashboard](https://servicenow-staging.fluidtopics.net/access?context=now-assist-context-menu-dashboard&family=yokohama&ft:locale=en-US)**

View and monitor the use of the Now Assist context menu across the different applications. Gain insights into the usage patterns, frequency, and effectiveness of the context menu actions with the Now Assist context menu usage dashboard.

-   **[Customizing ServiceNow skills in the Now Assist Skill Kit to tailor skills to meet your specific business requirements.](https://servicenow-staging.fluidtopics.net/access?context=clone-and-edit-servicenow-skill&family=yokohama&ft:locale=en-US)**

Clone the skills provided by ServiceNow in Now Assist applications by using the Now Assist Skill Kit so that you can edit the prompt or change the AI service provider. By editing the prompt, you can choose the additional inputs to be considered by the large language model \(LLM\) and arrange the formatting and content of the LLM response. After the skill is edited, you can activate the edited skill in the Now Assist Admin console to enable it.

-   **[Enabling the voice input for the Now Assist panel](https://servicenow-staging.fluidtopics.net/access?context=now-assist-panel-overview&family=yokohama&ft:locale=en-US)**

Enable the Voice Input setting for the Now Assist panel in the Now Assist Admin console. This setting gives users a voice-to-text input option to access the skills in the Now Assist panel in any supported language. After it’s enabled, the option is available in individual user accessibility preferences.

-   **[Setting your data overflow processing preferences to control your data](https://servicenow-staging.fluidtopics.net/access?context=configure-na-data-overflow&family=yokohama&ft:locale=en-US)**

Set your data overflow processing preferences to control your data. By default, all Now Assist network traffic is managed within ServiceNow datacenters, but during periods of high traffic, the traffic is burst to Microsoft Azure datacenters. You can choose whether you want to opt out of cloud bursting from the Now Assist Admin console data overflow processing settings.

-   **[Using multi-turn Q&amp;A in the Now Assist panel](https://servicenow-staging.fluidtopics.net/access?context=now-assist-multi-turn-qna&family=yokohama&ft:locale=en-US)**

Ask questions and get relevant answers directly in the Now Assist panel. The system remembers your previous questions for effortless follow-ups and pulls answers from multiple sources to give you the best results. You can select the source name in the response to access the full Knowledge article for more details.


-   **[Using dashboard and visualization export in the Now Assist panel](https://servicenow-staging.fluidtopics.net/access?context=dashboard-viz-export&family=yokohama&ft:locale=en-US)**

Export Platform Analytics dashboards and data visualizations through conversations. You can select from several output formats, and download or email the files.


-   **[Summarize records with the Now Assist context menu](https://servicenow-staging.fluidtopics.net/access?context=summarize-with-now-assist-context-menu&family=yokohama&ft:locale=en-US)**

Generate summaries by using the Now Assist context menu for the Core UI and Workspace. You can also expand or collapse the summary card, regenerate the summary, copy and share the summary, or provide feedback.


-   **[Email recommendations using the Now Assist context menu](https://servicenow-staging.fluidtopics.net/access?context=email-recommendations-nacm&family=yokohama&ft:locale=en-US)**

Select and choose the tone of your content with the change tone feature. You can select from the elaborate, shorten, casual, formal, or sympathetic tone.


</td></tr><tr><td>

Zurich

</td><td>

-   **[Requester Approval Checklist skill](https://servicenow-staging.fluidtopics.net/access?context=service-portal-approval-checklist-skill&family=zurich&ft:locale=en-US)**

The Requester Approval Checklist skill in the ServiceNow AI Platform® generates a structured checklist by mapping real-time request data against your organization’s knowledge articles.

**Note:** The skill is always on by default.


-   **[New system properties for the Now Assist Readiness Evaluation app](https://servicenow-staging.fluidtopics.net/access?context=nare-sys-props&family=zurich&ft:locale=en-US)**
    -   Reduce performance issues when a large volume of data is assessed with the **sn\_assess.assessment\_limit** system property.
    -   Customize the estimated remediation effort for select efforts with the **sn\_assess.effort\_visibility** system property. Setting this system property to `true` turns on the **Remediation properties** tab in the Now Assist Readiness Evaluation dashboard.
    -   Decide the maximum number of records to process for the ITSM assessment with the **sn\_assess.task\_limit** system property.

-   **[Manage version](https://servicenow-staging.fluidtopics.net/access?context=manage-version&family=zurich&ft:locale=en-US)**

Manage the versions of model providers across various skill groups and instance levels in Now Assist. You can modify and update versions for both base system and custom skills.

-   **[Now Assist skills](https://servicenow-staging.fluidtopics.net/access?context=now-assist-skills&family=zurich&ft:locale=en-US)**

Unlock the benefits of the Now Assist Fulfiller subscription to be able to explore and activate all the skills available in the system from Now Assist Admin.

-   **[Role masking](https://servicenow-staging.fluidtopics.net/access?context=aia-role-masking&family=zurich&ft:locale=en-US)**

Define roles within **role restrictions** for individual skills in Now Assist Admin to enforce resource access restrictions when a skill is invoked. This feature promotes precise control over the resources that can be accessed, like data and APIs.

-   **[Overview tab in Now Assist Admin](https://servicenow-staging.fluidtopics.net/access?context=configuring-now-assist&family=zurich&ft:locale=en-US)**

Share your experience in the Now Assist journey by providing feedback when prompted.

-   **[Voice input setting automatically activated](https://servicenow-staging.fluidtopics.net/access?context=activate-now-assist-panel&family=zurich&ft:locale=en-US)**

Activate the Now Assist panel to automatically turn on the Voice input setting, which is now located on the Assistants page.

-   **[Now Assist panel](https://servicenow-staging.fluidtopics.net/access?context=now-assist-panel-overview&family=zurich&ft:locale=en-US)**

Request additional information or clarification by asking a follow-up question in the Now Assist panel.

-   **[Synthesized Now Assist responses](https://servicenow-staging.fluidtopics.net/access?context=gchat-conv-integration&family=zurich&ft:locale=en-US)**

View synthesized Now Assist responses from within Google chat to have a richer conversational experience.

-   **[Now Assist support in article optimization](https://servicenow-staging.fluidtopics.net/access?context=knowledge-center-article-optimization&family=zurich&ft:locale=en-US)**

Improve the quality and health of your knowledge articles by using Now Assist based Article Optimization in the Knowledge Center. Scan knowledge articles and get instant, actionable feedback.

-   **[Use Now Assist to identify knowledge gaps](https://servicenow-staging.fluidtopics.net/access?context=understanding-knowledge-gaps&family=zurich&ft:locale=en-US)**

Identify and fill potential knowledge gaps proactively, including missing knowledge articles and recurring issues that lack or have an incomplete knowledge article.

-   **[Agentic workflows from within Google chat](https://servicenow-staging.fluidtopics.net/access?context=gchat-conv-integration&family=zurich&ft:locale=en-US)**

Initiate and view agentic workflows from within Google chat.

-   **[Monitor sensitive topic invocations](https://servicenow-staging.fluidtopics.net/access?context=reference-for-generative-ai-controller&family=zurich&ft:locale=en-US)**

Access the Gen AI Metrics \[sys\_generative\_ai\_metric\] table to review the logged invocations of sensitive topics and gain insights into how these topics are being triggered and monitored.

-   **[Long term stable models](https://servicenow-staging.fluidtopics.net/access?context=long-term-stable-models&family=zurich&ft:locale=en-US)**

Long term stable \(LTS\) models are part of Now LLM Service and provide longer model stability windows for regulated industries. These models can integrate with tools to provide governance, monitoring, and compliance controls.

-   **[Create multiple Now Assist context menu skill configurations](https://servicenow-staging.fluidtopics.net/access?context=create-multple-nacm-skill-configuration&family=zurich&ft:locale=en-US)**

You can now have multiple Now Assist context menu configurations on the same record form and field. You just have to create the required configuration and add to the form or field.

-   **[Generate KB article with Now Assist context menu](https://servicenow-staging.fluidtopics.net/access?context=generate-kb-article-with&family=zurich&ft:locale=en-US)**

Using the Now Assist Context Menu open prompt inline and pop-over variant you can quickly produce high-quality, accurate, and lucid knowledge articles, saving time and improving support in Knowledge Management.


-   **[Now Assist Readiness Evaluation](https://servicenow-staging.fluidtopics.net/access?context=now-assist-readiness-evaluation-landing-page&family=zurich&ft:locale=en-US)**

Use the Now Assist Readiness Evaluation app to help you evaluate your organization's readiness to implement agentic and generative AI Now Assist capabilities.

Assessments for agentic AI include:

    -   IT Service Management \(ITSM\)
    -   Customer Service Management \(CSM\)
Assessments for generative AI include:

    -   AI Search
    -   Virtual Agent \(VA\)
    -   IT Service Management \(ITSM\)
    -   Customer Service Management \(CSM\)
    -   HR Service Delivery \(HRSD\)
The results shown are estimates. You should evaluate results provided by Now Assist Readiness Evaluation for accuracy and appropriateness for your use case.


-   **[Improve Docs content in Strategic Portfolio Management with Now Assist context menu](https://servicenow-staging.fluidtopics.net/access?context=answer-queries-with-now-assist-context-menu&family=zurich&ft:locale=en-US) for SPM**

Implement the open prompt capability to enhance your ability to add additional context and generate accurate content with Now Assist context menu.

This feature enables interactive conversations with both supported ServiceNow® generative AI skills and custom-built skills.

-   **[Configure skills with custom prompts for knowledge article templates](https://servicenow-staging.fluidtopics.net/access?context=Now-assist-configure-custom-prompts-for-templates&family=zurich&ft:locale=en-US)**

As an admin, clone the KB generation skill and update prompts for AI model providers. This feature helps the agent use custom templates and custom prompts to generate knowledge articles with Now Assist from single and multiple knowledge bases.

-   **[Manage AI models](https://servicenow-staging.fluidtopics.net/access?context=manage-large-language-models&family=zurich&ft:locale=en-US)**

Choose and update your preferred LLM provider at the instance, skill, or skill group level for Now Assist base system skills.

Deactivate skills that aren't compatible with any of the LLM providers and access the audit history to view updates by the AI steward in AI Control Tower.

-   **[Configure multilingual service for Now Assist applications](https://servicenow-staging.fluidtopics.net/access?context=enable-dynamic-translation-for-now-assist-applications&family=zurich&ft:locale=en-US)**

Manage the default and supported languages by the different LLM providers under Multilingual service for translation.

-   **[Configure email reply recommendation](https://servicenow-staging.fluidtopics.net/access?context=configure-email-recommendation&family=zurich&ft:locale=en-US)**

Access citations to the articles referenced from the Knowledge Base. Explore references and insert the generated reply to your email.

-   **[Now Assist panel](https://servicenow-staging.fluidtopics.net/access?context=now-assist-panel-overview&family=zurich&ft:locale=en-US)**

Use the enhanced Now Assist panel for an intuitive and personalized experience. The updated Now Assist panel can be resized and moved anywhere on the ServiceNow AI Platform.

-   **[Now Assist Guardian supports third-party LLMs](https://servicenow-staging.fluidtopics.net/access?context=now-assist-guardian&family=zurich&ft:locale=en-US)**

Extend guardrail support to third-party LLMs, such as Amazon Bedrock, Google Cloud Vertex AI Studio, Google AI Studio, and Azure OpenAI, to verify that any inappropriate content is logged and blocked during content generation.

-   **[Increase the maximum response token limit for custom skills](https://servicenow-staging.fluidtopics.net/access?context=configure-skill-prompt&family=zurich&ft:locale=en-US)**

Increase the maximum response token limit for a Now Assist custom skill beyond the default value of 1000. This ability supports dynamic pricing based on output tokens and calculates the price for each skill executed per assist.


</td></tr></tbody>
</table>## Changes

Between your current release family and Zurich, some changes were made to existing Now Assist features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   **[New conditions available in Define Availability step of guided setup for chat reply recommendation](https://servicenow-staging.fluidtopics.net/access?context=configure-a-now-assist-skill&family=xanadu&ft:locale=en-US)**

When activating or editing the chat reply recommendation skill, you can now add conditions to determine who can use the skill.


-   **[__Get started__ step added to guided setup for resolution note generation](https://servicenow-staging.fluidtopics.net/access?context=now-assist-rn-summarization&family=xanadu&ft:locale=en-US)**

A step has been added to the guided setup for the resolution notes generation skill to remind you to update any customized code that is associated with the skill after a new release.


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

-   **[Configure multilingual service for Now Assist applications](https://servicenow-staging.fluidtopics.net/access?context=enable-dynamic-translation-for-now-assist-applications&family=yokohama&ft:locale=en-US)**

Enable translation settings is now Multilingual service in Now Assist admin console.

-   **[Default email client for email recommendation skill](https://servicenow-staging.fluidtopics.net/access?context=now-assist-skills&family=yokohama&ft:locale=en-US)**

The Seismic email client is enabled by default on Core UI with the activation of email recommendation. This client provides the Generative AI application features for creating email responses, draft management, and template management.

-   **[Now Assist panel response](https://servicenow-staging.fluidtopics.net/access?context=now-assist-panel-overview&family=yokohama&ft:locale=en-US)Now Assist panel response**

With the carousel experience removed, the Now Assist panel now generates a synthesized response for any user inquiry. This response includes content from Knowledge articles, flows &amp; actions, skills, and links to those articles, instead of only the Now Assist panel skills.


</td></tr><tr><td>

Zurich

</td><td>

-   **[Changes to Now Assist usage measurement](https://servicenow-staging.fluidtopics.net/access?context=monitoring-now-assist-usage&family=zurich&ft:locale=en-US)**



-   **[Use](https://servicenow-staging.fluidtopics.net/access?context=using-now-assist-readiness-evaluation&family=zurich&ft:locale=en-US)**
    -   View the updated legend that now includes None-XXL estimated remediation efforts along with assessment icon explanations.
    -   Understand estimated remediation efforts more clearly now that blocker areas are included in the estimated remediation efforts and non-blocker observations are not included in estimated remediation efforts.
    -   Select any widget on the Agentic AI - Assessment dashboard and Now Assist assessment dashboard tabs to open that widget's data table in a separate tab.

-   ****

-   **[Configure multilingual service for Now Assist applications](https://servicenow-staging.fluidtopics.net/access?context=enable-dynamic-translation-for-now-assist-applications&family=zurich&ft:locale=en-US)**

Enable translation settings is now a multilingual service in the Now Assist Admin console.


</td></tr></tbody>
</table>## Removed

Between your current release family and Zurich, some Now Assist features or functionality were removed.

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

Between your current release family and Zurich, some Now Assist features or functionality were deprecated.

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

-   In Patch 5, the **Select Use Case** drop-down menu was removed from the Agentic AI - ITSM tab.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate Now Assist.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

Now Assist features are available with activation of any Now Assist plugin from the ServiceNow Store. The following plugins are available:

-   [Now Assist for Accounts Payable Operations \(APO\)](https://servicenow-staging.fluidtopics.net/access?context=now-assist-apo&family=xanadu&ft:locale=en-US)
-   [Now Assist for Configuration Management Database \(CMDB\)](https://servicenow-staging.fluidtopics.net/access?context=now-assist-landing-cmdb&family=xanadu&ft:locale=en-US)
-   [Now Assist for Creator](https://servicenow-staging.fluidtopics.net/access?context=now-assist-for-creator-landing&family=xanadu&ft:locale=en-US)
-   [Now Assist for Customer Service Management \(CSM\)](https://servicenow-staging.fluidtopics.net/access?context=now-assist-csm&family=xanadu&ft:locale=en-US)
-   [Now Assist for Field Service Management \(FSM\)](https://servicenow-staging.fluidtopics.net/access?context=now-assist-fsm&family=xanadu&ft:locale=en-US)
-   [Now Assist for Financial Services Operations \(FSO\)](https://servicenow-staging.fluidtopics.net/access?context=now-assist-for-financial-services-operations&family=xanadu&ft:locale=en-US)
-   [Now Assist for Health and Safety](https://servicenow-staging.fluidtopics.net/access?context=now-assist-hs-landing&family=xanadu&ft:locale=en-US)
-   [Now Assist for HR Service Delivery \(HRSD\)](https://servicenow-staging.fluidtopics.net/access?context=now-assist-hrsd&family=xanadu&ft:locale=en-US)
-   [Now Assist for IT Operations Management \(ITOM\)](https://servicenow-staging.fluidtopics.net/access?context=now-assist-itom&family=xanadu&ft:locale=en-US)
-   [Now Assist for IT Service Management \(ITSM\)](https://servicenow-staging.fluidtopics.net/access?context=now-assist-itsm&family=xanadu&ft:locale=en-US)
-   [Now Assist for Legal Service Delivery \(LSD\)](https://servicenow-staging.fluidtopics.net/access?context=now-assist-lsd-landing&family=xanadu&ft:locale=en-US)
-   [Now Assist for PSDS](https://servicenow-staging.fluidtopics.net/access?context=now-assist-for-psds&family=xanadu&ft:locale=en-US)
-   [Now Assist for Security Incident Response](https://servicenow-staging.fluidtopics.net/access?context=now-assist-security-incident-landing&family=xanadu&ft:locale=en-US)
-   [Now Assist for Supplier Lifecycle Operations \(SLO\)](https://servicenow-staging.fluidtopics.net/access?context=now-assist-slo&family=xanadu&ft:locale=en-US)
-   [Now Assist for Sourcing and Procurement Operations \(SPO\)](https://servicenow-staging.fluidtopics.net/access?context=now-assist-spo&family=xanadu&ft:locale=en-US)
-   [Now Assist for Strategic Portfolio Management \(SPM\)](https://servicenow-staging.fluidtopics.net/access?context=now-assist-spm&family=xanadu&ft:locale=en-US)
-   [Now Assist for Telecommunications, Media and Technology \(TMT\)](https://servicenow-staging.fluidtopics.net/access?context=now-assist-spmc&family=xanadu&ft:locale=en-US)

For more information, see [Install Now Assist plugins](https://servicenow-staging.fluidtopics.net/access?context=install-now-assist-feature-plugins&family=xanadu&ft:locale=en-US).

</td></tr><tr><td>

Yokohama

</td><td>

Now Assist features are available with activation of any Now Assist plugin from ServiceNow Store. The following plugins are available:

-   


</td></tr><tr><td>

Zurich

</td><td>

-   **[Now Assist skills](https://servicenow-staging.fluidtopics.net/access?context=now-assist-skills&family=zurich&ft:locale=en-US)**

Now Assist features are available with activation of any Now Assist plugin from ServiceNow Store. The following plugins are available:

    -   


</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Now Assist we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

The Next Experience UI Framework must be enabled to use the Now Assist panel.

</td></tr><tr><td>

Yokohama

</td><td>

The Next Experience UI Framework must be enabled before you can use the Now Assist panel.

</td></tr><tr><td>

Zurich

</td><td>

The Next Experience UI Framework must be enabled before you can use the Now Assist panel.

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Now Assist we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

Now Assist supports various browsers, including Google Chrome and Microsoft Edge. Now Assist isn’t supported in Microsoft Internet Explorer.

</td></tr><tr><td>

Yokohama

</td><td>

Now Assist supports various browsers, including Google Chrome and Microsoft Edge. Now Assist isn’t supported in Microsoft Internet Explorer.

</td></tr><tr><td>

Zurich

</td><td>

Now Assist supports various browsers, including Google Chrome and Microsoft Edge. Now Assist isn’t supported in Internet Explorer.

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Now Assist, such as specific requirements or compliance levels.

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

-   **Voice Input for Now Assist**

Administrators can enable an optional voice input setting for the Now Assist panel in the Now Assist Admin console. This feature gives users a voice-to-text input option to access the Now Assist skills in the panel in any supported language. For more information, see [Enable voice input for Now Assist panel](https://servicenow-staging.fluidtopics.net/access?context=enable-voice-input-for-now-assist-panel&family=yokohama&ft:locale=en-US).

Once enabled, the Enable voice input for the Now Assist panel option are available in individual user accessibility preferences. See [Configure Next Experience accessibility preferences](https://servicenow-staging.fluidtopics.net/access?context=next-experience-accessibility-preferences&family=yokohama&ft:locale=en-US) for more information.

Voice-to-text input can help users with mobility impairments access generative AI skills without using a keyboard. This feature can also be useful to blind or low-vision users, neurodivergent users, non-native language speakers, or mobile users on the go, such as field service agents.


</td></tr><tr><td>

Zurich

</td><td>

-   **[Voice Input in Now Assist](https://servicenow-staging.fluidtopics.net/access?context=enable-voice-input-for-now-assist-panel&family=zurich&ft:locale=en-US)**

Administrators can enable an optional voice input setting for the Now Assist panel in the Now Assist Admin console. This feature, Voice Input, gives users a voice-to-text input option to access the Now Assist skills in the panel in any supported language. Voice Input helps users with mobility impairments access generative AI skills without using a keyboard. This feature can also be useful to blind or low-vision users, neurodivergent users, non-native language speakers, or mobile users on the go, such as field service agents.

Once enabled, Voice Input can be changed using the individual user accessibility preferences. See [Configure accessibility preferences](https://servicenow-staging.fluidtopics.net/access?context=next-experience-accessibility-preferences&family=zurich&ft:locale=en-US) for more information.


</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Now Assist we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

Now Assist supports Dynamic Translation for Xanadu.

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

If there are specific highlight considerations for Now Assist we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

[Xanadu Patch 10](https://servicenow-staging.fluidtopics.net/access?context=xanadu-patch-10&family=xanadu&ft:locale=en-US)

-   Use the Now Assist Readiness Evaluation app to automate the implementation assessment process before implementing Now Assist agentic and generative AI.

 [Xanadu Patch 3](https://servicenow-staging.fluidtopics.net/access?context=xanadu-patch-3&family=xanadu&ft:locale=en-US)

-   Protect your users from offensive content, prompt injection attacks, and filtered subjects in AI-generated content with Now Assist Guardian.
-   Use the native translation capabilities of the Now LLM Service models to speak to users in their preferred languages.
-   Troubleshoot Now Assist skills from the Now Assist Admin console to locate the sources of configuration problems.
-   Monitor the usage and performance of generative AI features and capabilities offered under Now Assist from the Analytics tab in the Now Assist Admin console.
-   Use the multi-language capabilities of Now Assist to generate a Knowledge article for an incident, case, or other supported task type in a language other than English.
-   Enable agents to utilize the generative AI capabilities of Now Assist to shorten or elaborate content in a Knowledge article using the context menu feature.
-   Now Assist context menu enhancements.

 [Xanadu Patch 1](https://servicenow-staging.fluidtopics.net/access?context=xanadu-patch-1&family=xanadu&ft:locale=en-US)

-   Support users who speak different languages with multi-language, dynamic translation.
-   Make finding tables and lists easier and more efficient by using the navigation platform skill in the Now Assist panel.
-   Write with Now Assist to provide chat and email suggestions for agents based on the content of a conversation.
-   Enable developers to create their own custom skills by using the Now Assist Skill Kit.
-   Generate a Knowledge Base article from a selection of similar cases or incidents to help address related concerns in a single article with Now Assist in Knowledge Management.

 See [Now Assist](https://servicenow-staging.fluidtopics.net/access?context=platform-now-assist-landing&family=xanadu&ft:locale=en-US) for more information.

 For more Platform Now Assist feature release notes, see the following topics:

-   [AI Search release notes](https://servicenow-staging.fluidtopics.net/access?context=ai-search-rn&family=xanadu&ft:locale=en-US)
-   [Document Intelligence release notes](https://servicenow-staging.fluidtopics.net/access?context=document-intelligence-rn&family=xanadu&ft:locale=en-US)
-   [Generative AI Controller release notes](https://servicenow-staging.fluidtopics.net/access?context=generative-ai-controller-rn&family=xanadu&ft:locale=en-US)
-   [Now Assist in Virtual Agent release notes](https://servicenow-staging.fluidtopics.net/access?context=now-assist-va-rn&family=xanadu&ft:locale=en-US)

</td></tr><tr><td>

Yokohama

</td><td>

[Yokohama Patch 11](https://servicenow-staging.fluidtopics.net/access?context=yokohama-patch-11&family=yokohama&ft:locale=en-US)

-   Review changes to Now Assist usage measurement.
-   Some Now Assist skills, agents, and agentic workflows are on by default.
-   Additional role configuration is required for agentic workflows and AI agents included with Now Assist applications.
-   Use the Now Assist context menu open prompt feature to create and edit knowledge articles.
-   Use Advanced settings to add conditions to hide or show the Now Assist Context Menu quick actions.
-   Create multiple Now Assist context menu configurations for the same field.
-   Use the Enable for extended tables option in parent table configuration, to enable or disable the inheritance model for the child table configurations.

 [Yokohama Patch 8](https://servicenow-staging.fluidtopics.net/access?context=yokohama-patch-8&family=yokohama&ft:locale=en-US)

-   Use the Now Assist Readiness Evaluation app to automate the implementation assessment process before implementing Now Assist agentic and generative AI.

 [Yokohama Patch 6](https://servicenow-staging.fluidtopics.net/access?context=yokohama-patch-6&family=yokohama&ft:locale=en-US)

-   Enable administrators to set up a security access control list \(ACL\) that checks user authentication for Now Assist context menu skills and new setup options. This gives them control over who can use Now Assist context menu skills and actions, as well as the built-in options like shorten, elaborate, and change tone.

-   Use Google Gemini and Anthropic Claude on AWS as AI model providers for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.
-   Select your preferred large language model \(LLM\) provider for Now Assist out-of-box skills. Apart from Now LLM Service, the platform supports Azure OpenAI GPT-4.1 and GPT-4.1 mini, Google Gemini 2.0 Flash and 2.5 Pro, and AWS Anthropic Claude 3.7 Sonnet LLM providers with ServiceNow® third-party model strategy.
-   Select a display option for custom Now Assist context menu event with an option to suppress the modeless window.
-   View the numbered citation and links to the source of information when you use Now Assist context menu for Email reply recommendation.

 [Yokohama Patch 3](https://servicenow-staging.fluidtopics.net/access?context=yokohama-patch-3&family=yokohama&ft:locale=en-US)

-   Access and monitor your Now Assist skills in the skill list or grid view. By toggling between the layouts, you can navigate from the Now Assist skills to specific products and then back to the skills page.
-   Identify and mark duplicate articles in the list view by using Now Assist in Knowledge Management and take action as required.
-   Apply the Now Assist Sentiment Analysis application to each record so that you can assess how satisfied your customers are. With this feature, you can make better decisions to improve customer experience.
-   Use the Now Assist context menu guided setup to create a Now Assist context menu configuration.
-   Use the Now Assist context menu to deploy the custom skills created using Now Assist skill kit.

 -   Monitor how the Now Assist context menu is being used across the different applications with the new Now Assist context menu usage dashboard.
-   Customize the ServiceNow skills with new prompts or providers in the Now Assist Skill Kit for your specific business needs.
-   Enable your users to use voice to interact with the Now Assist panel by enabling the Voice Input setting.
-   Use the new Conversational Q&amp;A option in the Now Assist panel to achieve an enhanced and accurate query resolution.
-   Generate a record summary, share or copy the summary, and provide feedback by using the Summarize option in the Now Assist context menu.
-   Customize and choose between the casual, formal, or sympathetic tone by using the Now Assist context menu.

 See [Now Assist](https://servicenow-staging.fluidtopics.net/access?context=platform-now-assist-landing&family=yokohama&ft:locale=en-US) for more information.

 For more Platform Now Assist feature release notes, see the following topics:

-   [AI Search release notes](https://servicenow-staging.fluidtopics.net/access?context=ai-search-rn&family=yokohama&ft:locale=en-US)
-   [Document Intelligence release notes](https://servicenow-staging.fluidtopics.net/access?context=document-intelligence-rn&family=yokohama&ft:locale=en-US)
-   [Now Assist Skill Kit release notes](https://servicenow-staging.fluidtopics.net/access?context=na-skill-kit-rn&family=yokohama&ft:locale=en-US)
-   [Now Assist in Virtual Agent release notes](https://servicenow-staging.fluidtopics.net/access?context=now-assist-va-rn&family=yokohama&ft:locale=en-US)

</td></tr><tr><td>

Zurich

</td><td>

[Zurich Patch 5](https://servicenow-staging.fluidtopics.net/access?context=zurich-patch-5&family=zurich&ft:locale=en-US)

-   Review changes to Now Assist usage measurement.
-   View improved legend and icon descriptions for the Now Assist Readiness Evaluation app.
-   Work with new system properties to improve performance and customization within the Now Assist Readiness Evaluation app.

 [Zurich Patch 4](https://servicenow-staging.fluidtopics.net/access?context=zurich-patch-4&family=zurich&ft:locale=en-US)

-   Some Now Assist skills, agents, and agentic workflows are now turned on by default.
-   Select your preferred integration type, either Bring Your Own Key \(BYOK\) or Original Equipment Manufacturer \(OEM\), for the configuration of the available model providers within Now Assist Admin.
-   Explore the Data and Analytics workflow skills under Now Assist skills within Now Assist Admin.
-   Adopt AI responsibly and minimize operational and compliance risks by configuring and subscribing to Long Term Stable Models \(LTS\) as a model provider in Now Assist Admin.
-   Ask a follow-up question in the Now Assist panel for additional information or clarification.
-   Experience an enhanced conversational interaction by viewing synthesized Now Assist responses from within Google chat.
-   Initiate and view agentic workflows from within Google chat.
-   Use the Now Assist context menu open prompt feature to create and edit knowledge articles.
-   Use Advanced settings to add conditions to hide or show the Now Assist Context Menu quick actions.
-   Create multiple Now Assist context menu configurations for the same field.
-   Use the Enable for extended tables option in parent table configuration, to enable or disable the inheritance model for the child table configurations.

 [Zurich Patch 2](https://servicenow-staging.fluidtopics.net/access?context=zurich-patch-2&family=zurich&ft:locale=en-US)

-   Use the Now Assist Readiness Evaluation app to automate the implementation assessment process before implementing Now Assist agentic and generative AI.

 [Zurich Patch 1](https://servicenow-staging.fluidtopics.net/access?context=zurich-patch-1&family=zurich&ft:locale=en-US)

-   Enable administrators to set up a security access control list that checks user authentication for Now Assist context menu skills and new setup options. This feature gives them control over who can use Now Assist context menu skills and actions, as well as built-in options like shorten, elaborate, and change tone.
-   Use the Open Prompt Capability available in Now Assist for Strategic Portfolio Management \(SPM\) to ask questions and refine generated content through open-ended queries.

 Zurich

-   Use Google Gemini and Anthropic Claude on AWS as AI model providers for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.
-   Select your preferred large language model \(LLM\) provider for Now Assist base system skills. Apart from Now LLM Service, the platform supports Azure OpenAI GPT-4.1 and GPT-4.1 mini, Google Gemini 2.0 Flash and 2.5 Pro, and AWS Anthropic Claude 3.7 Sonnet LLM providers with ServiceNow® third-party model strategy.
-   Suppress the modeless window for a custom Now Assist context menu event.
-   View numbered citations and links to the information sources when you use the Now Assist context menu for email reply recommendation.

 See [Now Assist](https://servicenow-staging.fluidtopics.net/access?context=platform-now-assist-landing&family=zurich&ft:locale=en-US) for more information.

 For more Platform Now Assist feature release notes, see the following topics:

-   [AI Search release notes](https://servicenow-staging.fluidtopics.net/access?context=ai-search-rn&family=zurich&ft:locale=en-US)
-   [Document Intelligence release notes](https://servicenow-staging.fluidtopics.net/access?context=document-intelligence-rn&family=zurich&ft:locale=en-US)
-   [Now Assist Skill Kit release notes](https://servicenow-staging.fluidtopics.net/access?context=now-assist-skill-kit-rn&family=zurich&ft:locale=en-US)
-   [Now Assist in Virtual Agent release notes](https://servicenow-staging.fluidtopics.net/access?context=now-assist-va-rn&family=zurich&ft:locale=en-US)

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/delta-xanadu-zurich/rn-combined-intro.md)


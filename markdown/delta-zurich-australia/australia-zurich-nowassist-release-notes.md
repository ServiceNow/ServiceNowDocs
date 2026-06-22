---
title: Combined Now Assist release notes for upgrades from Zurich to Australia
description: Consolidated page of all release notes for Now Assist from Zurich to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-zurich-australia/australia-zurich-nowassist-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-06-22"
reading_time_minutes: 26
breadcrumb: [Products combined by family]
---

# Combined Now Assist release notes for upgrades from Zurich to Australia

Consolidated page of all release notes for Now Assist from Zurich to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Now Assist release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Zurich to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Now Assist to Australia

Before you upgrade to Australia, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

Customers who have not opted into third-party, large language models may be routed to them during skill execution. If the new model is not provisioned or available in your environment, this will result in skill execution failures. Check the models your skills use within Now Assist admin console.

 If you customized UI actions or other items that are associated with Now Assist skills, confirm that your customized code is updated with the new skill releases. Otherwise, certain functions might not work as expected.

 If you run into issues when you're upgrading a Now Assist product, see the [Issues and mitigation for Now Assist \(Generative AI\) Applications and Plugin updates \[KB1637452\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1637452) article in the Now Support Knowledge Base. Log in to view the article.

 The Zurich release introduces enhanced protections for read‑only fields across the ServiceNow® AI Platform. These changes include a new “read\_only\_option” field with granular control levels, including “strict\_read\_only” and “client\_script\_modifiable". The changes occur in the back-end and maintain backward‑compatible behavior. This update helps strengthen your instance security while preserving the flexibility you need. If you have custom client scripts that modify ServiceNow® ‑owned read‑only fields using `g_form.setValue()` or `g_form.clearValue()`, refer to [KB2718122](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2718122). This article provides additional technical details on how to identify affected fields and adjust their settings.

 The existing Access Control Lists \(ACLs\) will be updated to replace the 'admin' role with specific, purpose-driven granular roles within scripts or security attributes. As part of this update, the `getRoles()` API will be replaced with the `hasRole()` API for authorization purposes. Additionally, all references to the 'admin' role in the code will be substituted with the new feature-specific granular roles for authorization use cases. Read [https://www.servicenow.com/docs/r/platform-security/granular-admin-roles.html](https://www.servicenow.com/docs/r/platform-security/granular-admin-roles.html) to learn more.

</td></tr><tr><td>

Australia

</td><td>

If you customized actions on the user interface or other items that are associated with Now Assist skills, confirm that your customized code is updated with the new skill releases. Otherwise, certain functions might not work as expected.

 If you run into issues when you're upgrading a Now Assist product, see the [Issues and mitigation for Now Assist \(generative AI\) Applications and Plugin updates \[KB1637452\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1637452) article in the Now Support Knowledge Base. Log in to view the article.

 The Australia release introduces enhanced protections for read‑only fields across the ServiceNow AI Platform. These changes include a new read\_only\_option field with granular control levels, including strict\_read\_only and client\_script\_modifiable. The changes occur in the back end and maintain backward‑compatible behavior. This update helps strengthen instance security while preserving flexibility. If you have custom client scripts that modify read‑only fields using `g_form.setValue()` or `g_form.clearValue()`, refer to the [KB2718122](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2718122) article in the Now Support Knowledge Base to identify affected fields and adjust the settings.

 The existing access control lists \(ACLs\) have been updated to replace the admin role with purpose-driven granular roles within scripts or security attributes. As part of this update, the `getRoles()` API is replaced with the `hasRole()` API for authorization purposes. Additionally, all references to the admin role in the code have been substituted with the granular roles for authorization use cases. For more information, see [Granular admin roles](https://www.servicenow.com/docs/access?context=granular-admin-roles&family=australia&ft:locale=en-US).

</td></tr></tbody>
</table>## New features

Between your current release family and Australia, new features were introduced for Now Assist.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

-   **[Now Assist Guardian enabled by default](https://www.servicenow.com/docs/access?context=now-assist-guardian&family=zurich&ft:locale=en-US)**

Detect and log prompt injection attempts across all generative AI applications and features, and offensive content in supported Now Assist skills, by default. You can configure Now Assist Guardian to block AI-generated responses when an attempt is detected.

-   **[Using Now Assist Admin](https://www.servicenow.com/docs/access?context=using-now-assist-admin_0&family=zurich&ft:locale=en-US)**

Explore additional user interface tabs of a Now Assist skill within a selected workflow. Access the usage and analytics of that skill. You can also view and manage the security and governance details of the selected skills.

-   **[Configure prompt injection detection for Now Assist skills](https://www.servicenow.com/docs/access?context=configure-prompt-injection-attack-protection&family=zurich&ft:locale=en-US)**

Set the prompt injection detection action and severity level for Now Assist skills. Prompt injection detection is enabled by default for all Now Assist skills, except Platform skills and custom skills. When a skill has its own setting, Now Assist Guardian automatically applies the more protective of the two settings, the skill-level setting or the instance-level setting.

-   **[Visual Q&amp;A in Now Assist](https://www.servicenow.com/docs/access?context=now-assist-qa-genius-result&family=zurich&ft:locale=en-US)**

Upload screenshots, error images, or documents in the Now Assist panel and get AI-generated answers about their content without leaving your current context.

-   **[Catalog experience](https://www.servicenow.com/docs/access?context=now-assist-panel-premium&family=zurich&ft:locale=en-US)**

Navigate away from a catalog form mid-completion and a modal appears asking whether you want to stay or leave, preventing accidental loss of your work. After you submit a catalog item, you can select View Details to open the submitted record.

-   **[Enhancements](https://www.servicenow.com/docs/access?context=now-assist-panel-premium&family=zurich&ft:locale=en-US)**

Switch between multiple interactive views — such as knowledge articles, catalogs, and org charts — within a single conversation using a new dropdown in the Now Assist panel. When more than six promoted topics are available, you can select a category on the topic menu to see all of them at once.

-   **[Image and document upload](https://www.servicenow.com/docs/access?context=now-assist-panel-premium&family=zurich&ft:locale=en-US)**

Upload images and screenshots directly into the Now Assist panel as part of your conversation and the Now Assist interprets the visual content to answer your questions or generate summaries.

-   **[Maintain and display the right context](https://www.servicenow.com/docs/access?context=now-assist-panel-premium&family=zurich&ft:locale=en-US)**

Open the Now Assist panel while working on an incident record and you automatically see the most recent conversation tied to that incident. You can continue chatting about the incident or switch to unrelated topics in the same session, keeping your work in context without losing your place.


-   **[Using Now Assist Admin](https://www.servicenow.com/docs/access?context=using-now-assist-admin_0&family=zurich&ft:locale=en-US)**

Explore the archive option from navigation pane within Now Assist Admin and archive custom and copies of Now Assist skills.


-   **[Clarifying questions for unclear requests](https://www.servicenow.com/docs/access?context=now-assist-panel-overview&family=zurich&ft:locale=en-US)**

Get precise, relevant answers from Now Assist panel premium chat even when your request is unclear, as the assistant asks you a targeted clarifying question before responding instead of returning an overwhelming list of results. When the assistant is confident it understands your request, it responds immediately without interrupting the conversation.

-   **[Upload documents](https://www.servicenow.com/docs/access?context=now-assist-panel-overview&family=zurich&ft:locale=en-US)**

Upload documents directly into a Now Assist panel conversation during topic, skill, catalog, or agent execution, and let the assistant extract information from them to automatically fill in required fields, answer questions, and keep the conversation moving. Uploaded document context is retained for the duration of the session and cleared when the session ends to protect your data.

-   **[Response feedback](https://www.servicenow.com/docs/access?context=now-assist-panel-overview&family=zurich&ft:locale=en-US)**

Provide more detailed feedback on Now Assist panel responses by selecting thumbs up or thumbs down, then choosing from configurable checkbox options or adding your own comments to explain exactly what was helpful or what fell short. Your feedback is captured and made available through analytics dashboards, helping admins continuously improve the quality of responses you receive.

-   **[Premium chat](https://www.servicenow.com/docs/access?context=now-assist-panel-overview&family=zurich&ft:locale=en-US)**

Start a Now Assist panel premium chat from any page in the Employee Hub with a single click, without interrupting existing workflows. You can upload files, toggle web search on or off, and receive a personalized greeting with promoted topics when opening a new conversation.

-   **[Synthesized results in chat experience](https://www.servicenow.com/docs/access?context=now-assist-panel-overview&family=zurich&ft:locale=en-US)**

Get concise, grounded answers to your natural language questions in Now Assist panel premium chat, with inline citations linking to the knowledge articles, actions, and catalogs used to generate the response. You can ask follow-up questions within the same context, explore sources in the side panel, and see clear messaging if results are limited or unavailable.

-   **[Search results side panel](https://www.servicenow.com/docs/access?context=now-assist-panel-overview&family=zurich&ft:locale=en-US)**

View search citations and related results in a collapsible side panel that appears alongside your Now Assist panel premium chat responses, so you can explore sources without leaving the conversation. You can select any internal source to open it in the background, browse external results in a new tab, and close the panel at any time to return to the full chat view.

-   **[Primitives and widgets](https://www.servicenow.com/docs/access?context=now-assist-panel-overview&family=zurich&ft:locale=en-US)**

View rich, responsive content inline in your Now Assist panel premium chat conversation, including people profiles, org charts, record cards, and record summaries that match the look and feel of your portal. You can also access org charts and people information directly through natural language — for example, by typing "show me the org chart for John Smith" — without leaving the conversation.

-   **[Voice Input](https://www.servicenow.com/docs/access?context=now-assist-panel-overview&family=zurich&ft:locale=en-US)**

Use your voice to send prompts in Now Assist panel premium chats by selecting the microphone button in the input bar, which transcribes your speech to text so you can interact with the assistant hands-free. You can enable or disable voice input through your personal preferences, and your admin can also turn it on or off at the assistant level through Assistant Designer.

-   **[Search enhancements](https://www.servicenow.com/docs/access?context=now-assist-panel-overview&family=zurich&ft:locale=en-US)**

Get cleaner, more organized search results in Now Assist panel premium chat, with single records displayed as cards and multiple records displayed as tables. You can switch between multiple interactive views in a conversation using a dropdown and use a back button to return to previously viewed content.

-   **[Transition from chat to full search results](https://www.servicenow.com/docs/access?context=now-assist-panel-overview&family=zurich&ft:locale=en-US)**

Access the full search results page directly from your Now Assist panel premium chat response by selecting the "Full search experience" link in the sources and more panel. The search results page opens with your original search term already populated, so you can explore the complete set of results without having to retype your query.

-   **[Follow-up questions from search results](https://www.servicenow.com/docs/access?context=now-assist-panel-overview&family=zurich&ft:locale=en-US)**

Ask follow-up questions in Now Assist panel premium chat directly from your workspace search results by selecting the "Ask a follow-up" button, which opens a new conversation with the relevant search context already loaded. You can continue exploring a topic conversationally without having to re-enter your query or switch between search and chat.

-   **[Record-specific context](https://www.servicenow.com/docs/access?context=now-assist-panel-overview&family=zurich&ft:locale=en-US)**

Get more relevant responses from Now Assist panel premium chat when you're working on a record, as conversations started from a record page are automatically aware of that record's context. You no longer need to manually describe what you're working on — the assistant understands it from the start.

-   **[Upgrade Now Assist panel](https://www.servicenow.com/docs/access?context=now-assist-panel-overview&family=zurich&ft:locale=en-US)**

Upgrade your Now Assist panel experience to premium chat without losing your active conversations, as any conversations in progress remain accessible until you refresh the page. When you open premium chat for the first time after the upgrade, a summary of what's new helps you quickly get familiar with the latest capabilities.


-   **[Manage version](https://www.servicenow.com/docs/access?context=manage-version&family=zurich&ft:locale=en-US)**

Review the summary, alerts, and notifications regarding changes in model provider version states as they are deprecated or retired.

-   **[Now Assist panel](https://www.servicenow.com/docs/access?context=now-assist-panel-overview&family=zurich&ft:locale=en-US)**

Send information from Now Assist panel conversations directly to relevant fields on incident pages using action buttons. You don't have to manually copy and paste content between Now Assist panel conversations and the incident form.

-   **[Now Assist panel](https://www.servicenow.com/docs/access?context=now-assist-panel-overview&family=zurich&ft:locale=en-US)**

Automatically see the most recent Now Assist panel conversation for an incident when you switch between incident tabs. Now Assist panel remembers which conversation belongs to which incident and displays it when you return to that incident.

-   **[Now Assist panel](https://www.servicenow.com/docs/access?context=now-assist-panel-overview&family=zurich&ft:locale=en-US)**

Configure which record types will support Now Assist panel context switching. This enables teams to customize the Now Assist panel experience based on a business unit’s workflow and use cases.

-   **[Now Assist panel](https://www.servicenow.com/docs/access?context=now-assist-panel-overview&family=zurich&ft:locale=en-US)**

View your Now Assist panel chat history grouped by incident record. Agent conversations related to a specific incident are grouped together rather than organized chronologically, making them easier to find.

-   **[Now Assist panel](https://www.servicenow.com/docs/access?context=now-assist-panel-overview&family=zurich&ft:locale=en-US)**

View the correct conversation history when you navigate between different incident records.

-   **[Now Assist panel](https://www.servicenow.com/docs/access?context=now-assist-panel-overview&family=zurich&ft:locale=en-US)**

Send information directly from a Now Assist panel conversation to an agent chat conversation. This makes it easier to collaborate and share helpful information during incident resolution.

-   **[Now Assist panel](https://www.servicenow.com/docs/access?context=now-assist-panel-overview&family=zurich&ft:locale=en-US)**

Build custom Now Assist panel integrations that are tailored to specific business needs by passing custom context data in any format when initiating Now Assist panel conversations or executing skills.

-   **[Enhanced content detection with third-party guardrails](https://www.servicenow.com/docs/access?context=configure-guardrail-model&family=zurich&ft:locale=en-US)**

Now Assist Guardian supports third-party service provider guardrails, such as Microsoft Azure, Amazon Bedrock, and Google Model Armor so that any inappropriate content is logged and blocked during content generation. This gives you the flexibility to choose the detection provider that best aligns with your existing cloud infrastructure.


-   **[Requester Approval Checklist skill](https://www.servicenow.com/docs/access?context=service-portal-approval-checklist-skill&family=zurich&ft:locale=en-US)**

The Requester Approval Checklist skill in the ServiceNow AI Platform® generates a structured checklist by mapping real-time request data against your organization’s knowledge articles.

**Note:** The skill is on by default.


-   **[New system properties for the Now Assist Readiness Evaluation app](https://www.servicenow.com/docs/access?context=nare-sys-props&family=zurich&ft:locale=en-US)**
    -   Reduce performance issues when a large volume of data is assessed with the **sn\_assess.assessment\_limit** system property.
    -   Customize the estimated remediation effort for select efforts with the **sn\_assess.effort\_visibility** system property. Setting this system property to `true` turns on the **Remediation properties** tab in the Now Assist Readiness Evaluation dashboard.
    -   Decide the maximum number of records to process for the ITSM assessment with the **sn\_assess.task\_limit** system property.

-   **[Manage version](https://www.servicenow.com/docs/access?context=manage-version&family=zurich&ft:locale=en-US)**

Manage the versions of model providers across various skill groups and instance levels in Now Assist. You can modify and update versions for both base system and custom skills.

-   **[Now Assist skills](https://www.servicenow.com/docs/access?context=now-assist-skills&family=zurich&ft:locale=en-US)**

Unlock the benefits of the Now Assist Fulfiller subscription to be able to explore and activate all the skills available in the system from Now Assist Admin.

-   **[Role masking](https://www.servicenow.com/docs/access?context=aia-role-masking&family=zurich&ft:locale=en-US)**

Define roles within **role restrictions** for individual skills in Now Assist Admin to enforce resource access restrictions when a skill is invoked. This feature promotes precise control over the resources that can be accessed, like data and APIs.

-   **[Overview tab in Now Assist Admin](https://www.servicenow.com/docs/access?context=configuring-now-assist&family=zurich&ft:locale=en-US)**

Share your experience in the Now Assist journey by providing feedback when prompted.

-   **[Voice input setting automatically activated](https://www.servicenow.com/docs/access?context=activate-now-assist-panel&family=zurich&ft:locale=en-US)**

Activate the Now Assist panel to automatically turn on the voice input setting, which is now located on the Assistants page.

-   **[Now Assist panel](https://www.servicenow.com/docs/access?context=now-assist-panel-overview&family=zurich&ft:locale=en-US)**

Request additional information or clarification by asking a follow-up question in the Now Assist panel.

-   **[Synthesized Now Assist responses](https://www.servicenow.com/docs/access?context=gchat-conv-integration&family=zurich&ft:locale=en-US)**

View synthesized Now Assist responses from within Google Chat to have a richer conversational experience.

-   **[Now Assist support in article optimization](https://www.servicenow.com/docs/access?context=knowledge-center-article-optimization&family=zurich&ft:locale=en-US)**

Improve the quality and health of your knowledge articles by using Now Assist based Article Optimization in the Knowledge Center. Scan knowledge articles and get instant, actionable feedback.

-   **[Use Now Assist to identify knowledge gaps](https://www.servicenow.com/docs/access?context=understanding-knowledge-gaps&family=zurich&ft:locale=en-US)**

Identify and fill potential knowledge gaps proactively, including missing knowledge articles and recurring issues that lack or have an incomplete knowledge article.

-   **[Agentic workflows from within Google Chat](https://www.servicenow.com/docs/access?context=gchat-conv-integration&family=zurich&ft:locale=en-US)**

Initiate and view agentic workflows from within Google Chat.

-   **[Monitor sensitive topic invocations](https://www.servicenow.com/docs/access?context=reference-for-generative-ai-controller&family=zurich&ft:locale=en-US)**

Access the Gen AI Metrics \[sys\_generative\_ai\_metric\] table to review the logged invocations of sensitive topics and gain insights into how these topics are being triggered and monitored.

-   **[Long term stable models](https://www.servicenow.com/docs/access?context=long-term-stable-models&family=zurich&ft:locale=en-US)**

Long term stable \(LTS\) models are part of Now LLM Service and provide longer model stability windows for regulated industries. These models can integrate with tools to provide governance, monitoring, and compliance controls.

-   **[Create multiple Now Assist context menu skill configurations](https://www.servicenow.com/docs/access?context=create-multple-nacm-skill-configuration&family=zurich&ft:locale=en-US)**

You can now have multiple Now Assist context menu configurations on the same record form and field. You just have to create the required configuration and add to the form or field.

-   **[Generate KB article with Now Assist context menu](https://www.servicenow.com/docs/access?context=generate-kb-article-with&family=zurich&ft:locale=en-US)**

Using the Now Assist Context Menu open prompt inline and pop-over variant you can quickly produce high-quality, accurate, and lucid knowledge articles, saving time and improving support in Knowledge Management.


-   **[Now Assist Readiness Evaluation](https://www.servicenow.com/docs/access?context=now-assist-readiness-evaluation-landing-page&family=zurich&ft:locale=en-US)**

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


-   **[Improve Docs content in Strategic Portfolio Management with Now Assist context menu](https://www.servicenow.com/docs/access?context=answer-queries-with-now-assist-context-menu&family=zurich&ft:locale=en-US) for SPM**

Implement the open prompt capability to enhance your ability to add additional context and generate accurate content with Now Assist context menu.

This feature enables interactive conversations with both supported ServiceNow® generative AI skills and custom-built skills.

-   **[Configure skills with custom prompts for knowledge article templates](https://www.servicenow.com/docs/access?context=Now-assist-configure-custom-prompts-for-templates&family=zurich&ft:locale=en-US)**

As an admin, clone the KB generation skill and update prompts for AI model providers. This feature helps the agent use custom templates and custom prompts to generate knowledge articles with Now Assist from single and multiple knowledge bases.

-   **[Manage AI models](https://www.servicenow.com/docs/access?context=manage-large-language-models&family=zurich&ft:locale=en-US)**

Choose and update your preferred LLM provider at the instance, skill, or skill group level for Now Assist base system skills.

Deactivate skills that aren't compatible with any of the LLM providers and access the audit history to view updates by the AI steward in AI Control Tower.

-   **[Configure multilingual service for Now Assist applications](https://www.servicenow.com/docs/access?context=enable-dynamic-translation-for-now-assist-applications&family=zurich&ft:locale=en-US)**

Manage the default and supported languages by the different LLM providers under Multilingual service for translation.

-   **[Configure email reply recommendation](https://www.servicenow.com/docs/access?context=configure-email-recommendation&family=zurich&ft:locale=en-US)**

Access citations to the articles referenced from the Knowledge Base. Explore references and insert the generated reply to your email.

-   **[Now Assist panel](https://www.servicenow.com/docs/access?context=now-assist-panel-overview&family=zurich&ft:locale=en-US)**

Use the enhanced Now Assist panel for an intuitive and personalized experience. The updated Now Assist panel can be resized and moved anywhere on the ServiceNow AI Platform.

-   **[Now Assist Guardian supports third-party LLMs](https://www.servicenow.com/docs/access?context=now-assist-guardian&family=zurich&ft:locale=en-US)**

Extend guardrail support to third-party LLMs, such as Amazon Bedrock, Google Cloud Vertex AI studio, Google AI studio, and Azure OpenAI, to verify that any inappropriate content is logged and blocked during content generation.

-   **[Increase the maximum response token limit for custom skills](https://www.servicenow.com/docs/access?context=configure-skill-prompt&family=zurich&ft:locale=en-US)**

Increase the maximum response token limit for a Now Assist custom skill beyond the default value of 1000. This ability supports dynamic pricing based on output tokens and calculates the price for each skill executed per assist.


</td></tr><tr><td>

Australia

</td><td>

-   **[Create knowledge articles using Now Assist and Box](https://www.servicenow.com/docs/access?context=kc-create-article-with-Box&family=australia&ft:locale=en-US)**

The Knowledge Center now integrates with Box. This integration enables authors to use stored files as a source for generating knowledge articles with Now Assist.


-   **[Now Assist Guardian enabled by default](https://www.servicenow.com/docs/access?context=now-assist-guardian&family=australia&ft:locale=en-US)**

Detect and log prompt injection attempts across all generative AI applications and features, and offensive content in supported Now Assist skills, by default. You can configure Now Assist Guardian to block AI-generated responses when an attempt is detected.

-   **[Using Now Assist Admin](https://www.servicenow.com/docs/access?context=using-now-assist-admin_0&family=australia&ft:locale=en-US)**

Explore additional user interface tabs of a Now Assist skill within a selected workflow. Access the usage and analytics of that skill. You can also view and manage the security and governance details of the selected skills.

-   **[Create knowledge articles using Now Assist and Box](https://www.servicenow.com/docs/access?context=kc-create-article-with-Box&family=australia&ft:locale=en-US)**

Knowledge Center integrates with **Box**, enabling authors to use stored files as a source for generating knowledge articles with Now Assist.

-   **[Article Optimization with Reading Ease scan](https://www.servicenow.com/docs/access?context=kc-reading-ease-scan&family=australia&ft:locale=en-US)**

The AI-based **Reading Ease** scan, integrated into the article optimization feature of Knowledge Center, scans articles for readability, provides actionable recommendations, and supports ongoing article improvement.

-   **[Configure prompt injection detection for Now Assist skills](https://www.servicenow.com/docs/access?context=configure-prompt-injection-attack-protection&family=australia&ft:locale=en-US)**

Set the prompt injection detection action and severity level for Now Assist skills. Prompt injection detection is enabled by default for all Now Assist skills, except Platform skills and custom skills. When a skill has its own setting, Now Assist Guardian automatically applies the more protective of the two settings, the skill-level setting or the instance-level setting.

-   **[Visual Q&amp;A in Now Assist](https://www.servicenow.com/docs/access?context=now-assist-qa-genius-result&family=australia&ft:locale=en-US)**

Upload screenshots, error images, or documents in the Now Assist panel and get AI-generated answers about content without leaving your current context.

-   **[Catalog experience](https://www.servicenow.com/docs/access?context=now-assist-panel-premium&family=australia&ft:locale=en-US)**

Navigate away from a catalog form mid-completion and a modal appears asking whether you want to stay or leave, preventing accidental loss of your work. After you submit a catalog item, you can select View Details to open the submitted record.

-   **[Enhancements](https://www.servicenow.com/docs/access?context=now-assist-panel-premium&family=australia&ft:locale=en-US)**

Switch between multiple interactive views — such as knowledge articles, catalogs, and org charts — within a single conversation using a new dropdown in the Now Assist panel. When more than six promoted topics are available, you can select a category on the topic menu to see all of them at once.

-   **[Image and document upload](https://www.servicenow.com/docs/access?context=now-assist-panel-premium&family=australia&ft:locale=en-US)**

Upload images and screenshots directly into the Now Assist panel as part of your conversation and the Now Assist interprets the visual content to answer your questions or generate summaries.

-   **[Maintain and display the right context](https://www.servicenow.com/docs/access?context=now-assist-panel-premium&family=australia&ft:locale=en-US)**

Open the Now Assist panel while working on an incident record and you automatically see the most recent conversation tied to that incident. You can continue chatting about the incident or switch to unrelated topics in the same session, keeping your work in context without losing your place.


-   **[Using Now Assist Admin](https://www.servicenow.com/docs/access?context=using-now-assist-admin_0&family=australia&ft:locale=en-US)**

Explore the archive option from navigation pane within Now Assist Admin and archive custom and copies of Now Assist skills.


 -   **[ServiceNow product tiers](https://www.servicenow.com/docs/access?context=ai-native-sku-overview&family=australia&ft:locale=en-US)**

The ServiceNow AI Platform now brings you an AI native experience with three licensing tiers available:

    -   Foundation: AI agents and skills to deliver insights
    -   Advanced: AI agents and skills to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI agents and skills, and create your own
-   **[Merge duplicate articles](https://www.servicenow.com/docs/access?context=merge-duplicate-articles&family=australia&ft:locale=en-US)**

Use Now Assist in Knowledge Management to merge selected duplicate knowledge articles into a single consolidated article, preserving references to the original sources and maintaining a high‑quality, well‑organized knowledge base.


</td></tr></tbody>
</table>## Changes

Between your current release family and Australia, some changes were made to existing Now Assist features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

-   **[Changes to Now Assist usage measurement](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&family=zurich&ft:locale=en-US)**



-   **[Use](https://www.servicenow.com/docs/access?context=using-now-assist-readiness-evaluation&family=zurich&ft:locale=en-US)**
    -   View the updated legend that now includes None-XXL estimated remediation efforts along with assessment icon explanations.
    -   Understand estimated remediation efforts more clearly now that blocker areas are included in the estimated remediation efforts and non-blocker observations are not included in estimated remediation efforts.
    -   Select any widget on the Agentic AI- Assessment dashboard and Now Assist assessment dashboard tabs to open that widget's data table in a separate tab.

-   ****

-   **[Configure multilingual service for Now Assist applications](https://www.servicenow.com/docs/access?context=enable-dynamic-translation-for-now-assist-applications&family=zurich&ft:locale=en-US)**

Enable translation settings is now a multilingual service in the Now Assist Admin console.


</td></tr><tr><td>

Australia

</td><td>

-   **[Conversational Help](https://www.servicenow.com/docs/access?context=conversational-help-skills&family=australia&ft:locale=en-US)**

The discovery of Conversational Help Skills from the Now Assist panel is no longer configured as auto-enabled.


</td></tr></tbody>
</table>## Removed

Between your current release family and Australia, some Now Assist features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Australia, some Now Assist features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

-   In Patch 5, the **Select Use Case** drop-down menu was removed from the Agentic AI - ITSM tab.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate Now Assist.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

-   **[Now Assist skills](https://www.servicenow.com/docs/access?context=now-assist-skills&family=zurich&ft:locale=en-US)**

Now Assist features are available with activation of any Now Assist plugin from ServiceNow Store. The following plugins are available:

    -   


</td></tr><tr><td>

Australia

</td><td>

-   **[Now Assist skills](https://www.servicenow.com/docs/access?context=now-assist-skills&family=australia&ft:locale=en-US)**

Now Assist features are available with activation of any Now Assist plugin from ServiceNow Store. The following plugins are available:

    -   [Now Assist for APO](https://www.servicenow.com/docs/access?context=now-assist-apo&family=australia&ft:locale=en-US)
    -   [Now Assist for App Engine](https://www.servicenow.com/docs/access?context=add-ai-to-custom-apps-with-now-assist-for-app-engine-enterprise&family=australia&ft:locale=en-US)
    -   [Now Assist for Configuration Management Database \(CMDB\)](https://www.servicenow.com/docs/access?context=now-assist-landing-cmdb&family=australia&ft:locale=en-US)
    -   [Now Assist for CWM](https://www.servicenow.com/docs/access?context=now-assist-for-cwm-landing&family=australia&ft:locale=en-US)
    -   [Now Assist for Creator](https://www.servicenow.com/docs/access?context=now-assist-for-creator-landing&family=australia&ft:locale=en-US)
    -   [Now Assist for CSM](https://www.servicenow.com/docs/access?context=now-assist-csm&family=australia&ft:locale=en-US)
    -   [Now Assist for Employee Experience](https://www.servicenow.com/docs/access?context=now-assisit-employee-exp&family=australia&ft:locale=en-US)
    -   [Now Assist for Enterprise Architecture \(EA\)](https://www.servicenow.com/docs/access?context=now-assist-ea&family=australia&ft:locale=en-US)
    -   [Now Assist](https://www.servicenow.com/docs/access?context=now-assist-for-esg&family=australia&ft:locale=en-US)
    -   [Now Assist for FSM](https://www.servicenow.com/docs/access?context=now-assist-fsm&family=australia&ft:locale=en-US)
    -   [Now Assist for FSO](https://www.servicenow.com/docs/access?context=now-assist-for-financial-services-operations&family=australia&ft:locale=en-US)
    -   [Now Assist for Hardware Asset Management \(HAM\)](https://www.servicenow.com/docs/access?context=now-assist-ham&family=australia&ft:locale=en-US)
    -   [Now Assist for Health and Safety](https://www.servicenow.com/docs/access?context=now-assist-hs-landing&family=australia&ft:locale=en-US)
    -   [Now Assist for HR Service Delivery \(HRSD\)](https://www.servicenow.com/docs/access?context=now-assist-hrsd&family=australia&ft:locale=en-US)
    -   [Now Assist](https://www.servicenow.com/docs/access?context=now-assist-for-irm&family=australia&ft:locale=en-US)
    -   [Now Assist for ITOM](https://www.servicenow.com/docs/access?context=now-assist-itom&family=australia&ft:locale=en-US)
    -   [Now Assist for IT Service Management \(ITSM\)](https://www.servicenow.com/docs/access?context=now-assist-itsm&family=australia&ft:locale=en-US)
    -   [Now Assist for Legal Service Delivery \(LSD\)](https://www.servicenow.com/docs/access?context=now-assist-lsd-landing&family=australia&ft:locale=en-US)
    -   [Now Assist for OTM](https://www.servicenow.com/docs/access?context=now-assist-for-otm-landing&family=australia&ft:locale=en-US)
    -   [Now Assist for OTSM](https://www.servicenow.com/docs/access?context=now-assist-for-operational-technology-service-management&family=australia&ft:locale=en-US)
    -   [Now Assist for Order Management](https://www.servicenow.com/docs/access?context=now-assist-order-management&family=australia&ft:locale=en-US)
    -   [Now Assist for PSDS](https://www.servicenow.com/docs/access?context=now-assist-for-psds&family=australia&ft:locale=en-US)
    -   [Now Assist for SOM](https://www.servicenow.com/docs/access?context=now-assist-for-sales-and-order-management-som&family=australia&ft:locale=en-US)
    -   [Now Assist for Security Incident Response](https://www.servicenow.com/docs/access?context=now-assist-security-incident-landing&family=australia&ft:locale=en-US)
    -   [Now Assist for Software Asset Management \(SAM\)](https://www.servicenow.com/docs/access?context=now-assist-sam&family=australia&ft:locale=en-US)
    -   [Now Assist for SLO](https://www.servicenow.com/docs/access?context=now-assist-slo&family=australia&ft:locale=en-US)
    -   [Now Assist for SPO](https://www.servicenow.com/docs/access?context=now-assist-spo&family=australia&ft:locale=en-US)
    -   [Now Assist for Strategic Portfolio Management \(SPM\)](https://www.servicenow.com/docs/access?context=now-assist-spm&family=australia&ft:locale=en-US)
    -   [Now Assist for TMT](https://www.servicenow.com/docs/access?context=now-assist-spmc&family=australia&ft:locale=en-US)
    -   [Now Assist](https://www.servicenow.com/docs/access?context=now-assist-tprm&family=australia&ft:locale=en-US)
    -   [Now Assist for Workplace Service Delivery \(WSD\)](https://www.servicenow.com/docs/access?context=now-assist-wsd-landing&family=australia&ft:locale=en-US)
    -   [Now Assist for Vulnerability Response](https://www.servicenow.com/docs/access?context=now-assist-for-vulnerability-response-landing&family=australia&ft:locale=en-US)
    -   [Now Assist for Zero Copy Connectors](https://www.servicenow.com/docs/access?context=now-assist-for-zero-copy-connector-for-erp&family=australia&ft:locale=en-US)

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Now Assist we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

The Next Experience UI Framework must be enabled before you can use the Now Assist panel.

</td></tr><tr><td>

Australia

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

Zurich

</td><td>

Now Assist supports various browsers, including Google Chrome and Microsoft Edge. Now Assist isn’t supported in Internet Explorer.

</td></tr><tr><td>

Australia

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

Zurich

</td><td>

-   **[Voice Input in Now Assist](https://www.servicenow.com/docs/access?context=enable-voice-input-for-now-assist-panel&family=zurich&ft:locale=en-US)**

Administrators can enable an optional voice input setting for the Now Assist panel in the Now Assist Admin console. This feature, Voice Input, gives users a voice-to-text input option to access the Now Assist skills in the panel in any supported language. Voice Input helps users with mobility impairments access generative AI skills without using a keyboard. This feature can also be useful to blind or low-vision users, neurodivergent users, non-native language speakers, or users using hand-held devices on the go, such as field service agents.

Once enabled, Voice Input can be changed using the individual user accessibility preferences. See [Configure accessibility preferences](https://www.servicenow.com/docs/access?context=next-experience-accessibility-preferences&family=zurich&ft:locale=en-US) for more information.


</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Now Assist we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

Now Assist supports Dynamic Translation for Zurich.

</td></tr><tr><td>

Australia

</td><td>

Now Assist supports Dynamic Translation for Australia.

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for Now Assist we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

[Zurich Patch 10](https://www.servicenow.com/docs/access?context=zurich-patch-10&family=zurich&ft:locale=en-US)

-   Now Assist Guardian is enabled by default and detects prompt injection attempts and offensive content without manual activation.
-   Configure prompt injection detection separately for each Now Assist skill.

 [Zurich Patch 8](https://www.servicenow.com/docs/access?context=zurich-patch-8&family=zurich&ft:locale=en-US)

-   Now Assist panel premium chat gives you a full-featured AI assistant experience with support for file uploads, web search, agentic workflows, and voice input — so you can get answers, take action on records, and complete complex tasks without leaving your current context.
-   Get accurate results without having to repeat yourself or correct a wrong action because Now Assist now recognizes when your request needs clarification and asks a focused follow-up question before acting.
-   Upload documents directly in your Now Assist panel conversation and Now Assist automatically extracts the relevant information to fill in required fields, answer your questions, and keep the conversation moving without switching modes or restarting the flow.
-   Select specific reasons when you give a thumbs up or thumbs down to a Now Assist response, so your feedback is more meaningful and helps improve future responses.

 [Zurich Patch 7](https://www.servicenow.com/docs/access?context=zurich-patch-7&family=zurich&ft:locale=en-US)

-   Explore revamped **Manage AI models** option within Now Assist Admin for managing and configuring model providers, and updating model provider versions.
-   Select a record from the Now Assist context menu inline citation to navigate directly to the record page, where the referenced section will be highlighted for easy identification.
-   View all AI-generated content, now visually highlighted for easier recognition.
-   Set the minimum word count required for the Now Assist icon to appear, allowing you to control when the icon is displayed based on content length.

 [Zurich Patch 5](https://www.servicenow.com/docs/access?context=zurich-patch-5&family=zurich&ft:locale=en-US)

-   Review changes to Now Assist usage measurement.
-   View improved legend and icon descriptions for the Now Assist Readiness Evaluation app.
-   Work with new system properties to improve performance and customization within the Now Assist Readiness Evaluation app.

 [Zurich Patch 4](https://www.servicenow.com/docs/access?context=zurich-patch-4&family=zurich&ft:locale=en-US)

-   Some Now Assist skills, agents, and agentic workflows are now turned on by default.
-   Select your preferred integration type, either Bring Your Own Key \(BYOK\) or Original Equipment Manufacturer \(OEM\), for the configuration of the available model providers within Now Assist Admin.
-   Explore the Data and Analytics workflow skills under Now Assist skills within Now Assist Admin.
-   Adopt AI responsibly and minimize operational and compliance risks by configuring and subscribing to Long Term Stable Models \(LTS\) as a model provider in Now Assist Admin.
-   Ask a follow-up question in the Now Assist panel for additional information or clarification.
-   Experience an enhanced conversational interaction by viewing synthesized Now Assist responses from within Google Chat.
-   Initiate and view agentic workflows from within Google Chat.
-   Use the Now Assist context menu open prompt feature to create and edit knowledge articles.
-   Use Advanced settings to add conditions to hide or show the Now Assist Context Menu quick actions.
-   Create multiple Now Assist context menu configurations for the same field.
-   Use the Enable for extended tables option in parent table configuration, to enable or disable the inheritance model for the child table configurations.

 [Zurich Patch 2](https://www.servicenow.com/docs/access?context=zurich-patch-2&family=zurich&ft:locale=en-US)

-   Use the Now Assist Readiness Evaluation app to automate the implementation assessment process before implementing Now Assist agentic and generative AI.

 [Zurich Patch 1](https://www.servicenow.com/docs/access?context=zurich-patch-1&family=zurich&ft:locale=en-US)

-   Enable administrators to set up a security Access Control Lists \(ACLs\) that checks user authentication for Now Assist context menu skills and new setup options. This feature gives them control over who can use Now Assist context menu skills and actions, as well as built-in options like shorten, elaborate, and change tone.
-   Use the Open Prompt Capability available in Now Assist for Strategic Portfolio Management \(SPM\) to ask questions and refine generated content through open-ended queries.

 Zurich

-   Use Google Gemini and Anthropic Claude on AWS as AI model providers for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.
-   Select your preferred large language model \(LLM\) provider for Now Assist base system skills. Apart from Now LLM Service, the platform supports Azure OpenAI GPT-4.1 and GPT-4.1 mini, Google Gemini 2.5 Flash and 2.5 Pro, and AWS Anthropic Claude 3.7 Sonnet LLM providers with ServiceNow® third-party model strategy.
-   Suppress the modeless window for a custom Now Assist context menu event.
-   View numbered citations and links to the information sources when you use the Now Assist context menu for email reply recommendation.

 See [Now Assist](https://www.servicenow.com/docs/access?context=platform-now-assist-landing&family=zurich&ft:locale=en-US) for more information.

 For more Platform Now Assist feature release notes, see the following topics:

-   [AI Search release notes](https://www.servicenow.com/docs/access?context=ai-search-rn&family=zurich&ft:locale=en-US)
-   [Document Intelligence release notes](https://www.servicenow.com/docs/access?context=document-intelligence-rn&family=zurich&ft:locale=en-US)
-   [Now Assist Skill Kit release notes](https://www.servicenow.com/docs/access?context=now-assist-skill-kit-rn&family=zurich&ft:locale=en-US)
-   [Now Assist in Virtual Agent release notes](https://www.servicenow.com/docs/access?context=now-assist-va-rn&family=zurich&ft:locale=en-US)

</td></tr><tr><td>

Australia

</td><td>

[Australia Patch 3](https://www.servicenow.com/docs/access?context=australia-patch-3&family=australia&ft:locale=en-US)

-   Now Assist Guardian is enabled by default and detects prompt injection attempts and offensive content without manual activation.
-   Configure prompt injection detection separately for each Now Assist skill.
-   Create knowledge articles from Now Assist using files stored in Box.
-   Improve the clarity and accessibility of your articles with the AI-powered prompt Reading Ease scan.

 -   **[Merge duplicate articles](https://www.servicenow.com/docs/access?context=merge-duplicate-articles&family=australia&ft:locale=en-US)**

Merge selected duplicate knowledge articles into a new consolidated article using Now Assist in Knowledge Management. The merge preserves references to source articles and helps maintain a clean, high‑quality knowledge base.


</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-zurich-australia/rn-combined-intro.md)


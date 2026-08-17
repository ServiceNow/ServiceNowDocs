---
title: ServiceNow Otto release notes
description: The ServiceNow ServiceNow Otto experience brings generative AI to your organization. You can improve productivity and efficiency by delivering better self-service, recommending actions, delivering answers, and providing your users with AI Search. ServiceNow Otto was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 26
keywords: [ai-now-assist]
---

# ServiceNow Otto release notes

The ServiceNow® ServiceNow Otto experience brings generative AI to your organization. You can improve productivity and efficiency by delivering better self-service, recommending actions, delivering answers, and providing your users with AI Search. ServiceNow Otto was enhanced and updated in the Zurich release.

## ServiceNow Otto highlights for the Zurich release

[Zurich Patch 12](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-12.md)

-   Starting with Zurich Patch 12, Now Assist is now ServiceNow Otto. ServiceNow Otto is the new AI experience brand. This change is reflected in the name of ServiceNow products. Your product entitlements remain unchanged. Check your entitlements to determine your access to specific features.

[Zurich Patch 10](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-10.md)

-   AI Guardian is enabled by default and detects prompt injection attempts and offensive content without manual activation.
-   Configure prompt injection detection separately for each Now Assist skill.

[Zurich Patch 8](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-8.md)

-   Now Assist panel premium chat gives you a full-featured AI assistant experience with support for file uploads, web search, agentic workflows, and voice input — so you can get answers, take action on records, and complete complex tasks without leaving your current context.
-   Get accurate results without having to repeat yourself or correct a wrong action because Now Assist now recognizes when your request needs clarification and asks a focused follow-up question before acting.
-   Upload documents directly in your Now Assist panel conversation and Now Assist automatically extracts the relevant information to fill in required fields, answer your questions, and keep the conversation moving without switching modes or restarting the flow.
-   Select specific reasons when you give a thumbs up or thumbs down to a Now Assist response, so your feedback is more meaningful and helps improve future responses.

[Zurich Patch 7](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-7.md)

-   Explore revamped **Manage AI models** option within AI Admin Hub for managing and configuring model providers, and updating model provider versions.
-   Select a record from the Now Assist context menu inline citation to navigate directly to the record page, where the referenced section will be highlighted for easy identification.
-   View all AI-generated content, now visually highlighted for easier recognition.
-   Set the minimum word count required for the Now Assist icon to appear, allowing you to control when the icon is displayed based on content length.

[Zurich Patch 5](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-5.md)

-   Review changes to Now Assist usage measurement.
-   View improved legend and icon descriptions for the Now Assist Readiness Evaluation app.
-   Work with new system properties to improve performance and customization within the Now Assist Readiness Evaluation app.

[Zurich Patch 4](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-4.md)

-   Some Now Assist skills, agents, and agentic workflows are now turned on by default.
-   Select your preferred integration type, either Bring Your Own Key \(BYOK\) or Original Equipment Manufacturer \(OEM\), for the configuration of the available model providers within AI Admin Hub.
-   Explore the Data and Analytics workflow skills under Now Assist skills within AI Admin Hub.
-   Adopt AI responsibly and minimize operational and compliance risks by configuring and subscribing to Long Term Stable Models \(LTS\) as a model provider in AI Admin Hub.
-   Ask a follow-up question in the Now Assist panel for additional information or clarification.
-   Experience an enhanced conversational interaction by viewing synthesized Now Assist responses from within Google Chat.
-   Initiate and view agentic workflows from within Google Chat.
-   Use the Now Assist context menu open prompt feature to create and edit knowledge articles.
-   Use Advanced settings to add conditions to hide or show the Now Assist Context Menu quick actions.
-   Create multiple Now Assist context menu configurations for the same field.
-   Use the Enable for extended tables option in parent table configuration, to enable or disable the inheritance model for the child table configurations.

[Zurich Patch 2](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-2.md)

-   Use the Now Assist Readiness Evaluation app to automate the implementation assessment process before implementing Now Assist agentic and generative AI.

[Zurich Patch 1](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-1.md)

-   Enable administrators to set up a security Access Control Lists \(ACLs\) that checks user authentication for Now Assist context menu skills and new setup options. This feature gives them control over who can use Now Assist context menu skills and actions, as well as built-in options like shorten, elaborate, and change tone.
-   Use the Open Prompt Capability available in ServiceNow Otto for Strategic Portfolio Management to ask questions and refine generated content through open-ended queries.

Zurich

-   Use Google Gemini and Anthropic Claude on AWS as AI model providers for generative AI skills and AI agents, in addition to Now LLM Service and Azure OpenAI.
-   Select your preferred large language model \(LLM\) provider for Now Assist base system skills. Apart from Now LLM Service, the platform supports Azure OpenAI GPT-4.1 and GPT-4.1 mini, Google Gemini 2.5 Flash and 2.5 Pro, and AWS Anthropic Claude 3.7 Sonnet LLM providers with ServiceNow® third-party model strategy.
-   Suppress the modeless window for a custom Now Assist context menu event.
-   View numbered citations and links to the information sources when you use the Now Assist context menu for email reply recommendation.

See [AI Admin Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/platform-now-assist-landing.md) for more information.

For more Platform Now Assist feature release notes, see the following topics:

-   [AI Search release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/ai-search-rn.md)
-   [Document Intelligence release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/document-intelligence-rn.md)
-   [AI Skill Kit release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/now-assist-skill-kit-rn.md)
-   [Now Assist in Virtual Agent release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/now-assist-va-rn.md)

**Important:** Now Assist is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Important information for upgrading ServiceNow Otto to Zurich

Customers who have not opted into third-party, large language models may be routed to them during skill execution. If the new model is not provisioned or available in your environment, this will result in skill execution failures. Check the models your skills use within ServiceNow Otto admin console.

If you customized UI actions or other items that are associated with ServiceNow Otto skills, confirm that your customized code is updated with the new skill releases. Otherwise, certain functions might not work as expected.

If you run into issues when you're upgrading a ServiceNow Otto product, see the [Issues and mitigation for Now Assist \(Generative AI\) Applications and Plugin updates \[KB1637452\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1637452) article in the Now Support Knowledge Base. Log in to view the article.

The Zurich release introduces enhanced protections for read‑only fields across the ServiceNow® AI Platform. These changes include a new “read\_only\_option” field with granular control levels, including “strict\_read\_only” and “client\_script\_modifiable". The changes occur in the back-end and maintain backward‑compatible behavior. This update helps strengthen your instance security while preserving the flexibility you need. If you have custom client scripts that modify ServiceNow® ‑owned read‑only fields using `g_form.setValue()` or `g_form.clearValue()`, refer to [KB2718122](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2718122). This article provides additional technical details on how to identify affected fields and adjust their settings.

The existing Access Control Lists \(ACLs\) will be updated to replace the 'admin' role with specific, purpose-driven granular roles within scripts or security attributes. As part of this update, the `getRoles()` API will be replaced with the `hasRole()` API for authorization purposes. Additionally, all references to the 'admin' role in the code will be substituted with the new feature-specific granular roles for authorization use cases. Read [https://www.servicenow.com/docs/r/platform-security/granular-admin-roles.html](https://www.servicenow.com/docs/r/platform-security/granular-admin-roles.html) to learn more.

## New in the Zurich release

-   **ServiceNow Otto [Platform Approval assistance AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/platform-approval-aia.md)**

    Starting with Zurich Patch 12, Now Assist is now ServiceNow Otto. ServiceNow Otto is the new AI experience brand. This change is reflected in the name of ServiceNow products, including Platform Approval assistance AI agent. Your product entitlements remain unchanged. Check your entitlements to determine your access to specific features.

-   **[Platform Request status AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/ticket-status-aia.md)**

    ServiceNow Otto is the new AI experience brand. This change is reflected in the name of ServiceNow products, including Platform Request status AI agent. Your product entitlements remain unchanged. Check your entitlements to determine your access to specific features.

-   **[AI skill details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-skill-details.md)**

    Map multiple skills under subsections and display all applicable products per common skill with distinct visual tags. A visual indicator will mark skills as common, based on schema data.

-   **[Install plugins for ServiceNow Otto](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/install-now-assist-feature-plugins.md)**

    Control default activation of skills configured for auto-activating when installed or updated. Review the skills active by default and, activate or deactivate them individually.

-   **[ServiceNow Otto panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-panel-overview.md)**

    Enable streaming responses and unified surface operations to deliver faster, more reliable ServiceNow Otto® interactions. Support both synchronous and asynchronous workflows while maintaining compatibility with various LLM providers.


-   **[Prompt library](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/conversational-interfaces/now-assist-prompt-library.md)**

    Browse and select from promoted prompt templates or save your own custom prompts, eliminating the need to retype frequently-used prompts within your chats. Access your reusable templates instantly from the omnibar for faster, more consistent conversations.

-   **[Archive an AI skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/archive-a-now-assist-skill.md)**

    Find the Deprecated skills option in the navigation pane within AI Admin Hub to view skills deprecated by business unit, unavailable for use and no longer supported by ServiceNow.


-   **[Now Assist Guardian enabled by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-guardian.md)**

    Detect and log prompt injection attempts across all generative AI applications and features, and offensive content in supported Now Assist skills, by default. You can configure AI Guardian to block AI-generated responses when an attempt is detected.

-   **[Using AI Admin Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/using-now-assist-admin_0.md)**

    Explore additional user interface tabs of a Now Assist skill within a selected workflow. Access the usage and analytics of that skill. You can also view and manage the security and governance details of the selected skills.

-   **[Configure prompt injection detection for Now Assist skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/configure-prompt-injection-attack-protection.md)**

    Set the prompt injection detection action and severity level for Now Assist skills. Prompt injection detection is enabled by default for all Now Assist skills, except Platform skills and custom skills. When a skill has its own setting, AI Guardian automatically applies the more protective of the two settings, the skill-level setting or the instance-level setting.

-   **[Visual Q&amp;A in Now Assist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-qa-genius-result.md)**

    Upload screenshots, error images, or documents in the Now Assist panel and get AI-generated answers about their content without leaving your current context.

-   **[Catalog experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-panel-premium.md)**

    Navigate away from a catalog form mid-completion and a modal appears asking whether you want to stay or leave, preventing accidental loss of your work. After you submit a catalog item, you can select View Details to open the submitted record.

-   **[Enhancements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-panel-premium.md)**

    Switch between multiple interactive views — such as knowledge articles, catalogs, and org charts — within a single conversation using a new dropdown in the Now Assist panel. When more than six promoted topics are available, you can select a category on the topic menu to see all of them at once.

-   **[Image and document upload](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-panel-premium.md)**

    Upload images and screenshots directly into the Now Assist panel as part of your conversation and Now Assist interprets the visual content to answer your questions or generate summaries.

-   **[Maintain and display the right context](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-panel-premium.md)**

    Open the Now Assist panel while working on an incident record and you automatically see the most recent conversation tied to that incident. You can continue chatting about the incident or switch to unrelated topics in the same session, keeping your work in context without losing your place.

-   **[Post-chat surveys in premium chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-panel-premium.md)**

    Collect user feedback in premium chats through post-chat surveys that trigger on agent task completion instead of waiting for a chat-end event. When an agent completes a task in an agentic flow, the survey can surface based on a configured probability, enabling you to gather insights that were previously unavailable.


-   **[Using AI Admin Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/using-now-assist-admin_0.md)**

    Explore the archive option from navigation pane within AI Admin Hub and archive custom and copies of Now Assist skills.


-   **[Clarifying questions for unclear requests](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-panel-overview.md)**

    Get precise, relevant answers from Now Assist panel premium chat even when your request is unclear, as the assistant asks you a targeted clarifying question before responding instead of returning an overwhelming list of results. When the assistant is confident it understands your request, it responds immediately without interrupting the conversation.

-   **[Upload documents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-panel-overview.md)**

    Upload documents directly into a Now Assist panel conversation during topic, skill, catalog, or agent execution, and let the assistant extract information from them to automatically fill in required fields, answer questions, and keep the conversation moving. Uploaded document context is retained for the duration of the session and cleared when the session ends to protect your data.

-   **[Response feedback](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-panel-overview.md)**

    Provide more detailed feedback on Now Assist panel responses by selecting thumbs up or thumbs down, then choosing from configurable checkbox options or adding your own comments to explain exactly what was helpful or what fell short. Your feedback is captured and made available through analytics dashboards, helping admins continuously improve the quality of responses you receive.

-   **[Start premium chat from any page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-panel-overview.md)**

    Start a Now Assist panel premium chat from any page in the Employee Hub with a single click, without interrupting existing workflows. You can upload files, toggle web search on or off, and receive a personalized greeting with promoted topics when opening a new conversation.

-   **[Synthesized results in chat experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-panel-overview.md)**

    Get concise, grounded answers to your natural language questions in Now Assist panel premium chat, with inline citations linking to the knowledge articles, actions, and catalogs used to generate the response. You can ask follow-up questions within the same context, explore sources in the side panel, and see clear messaging if results are limited or unavailable.

-   **[Search results side panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-panel-overview.md)**

    View search citations and related results in a collapsible side panel that appears alongside your Now Assist panel premium chat responses, so you can explore sources without leaving the conversation. You can select any internal source to open it in the background, browse external results in a new tab, and close the panel at any time to return to the full chat view.

-   **[Primitives and widgets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-panel-overview.md)**

    View rich, responsive content inline in your Now Assist panel premium chat conversation, including people profiles, org charts, record cards, and record summaries that match the look and feel of your portal. You can also access org charts and people information directly through natural language — for example, by typing "show me the org chart for John Smith" — without leaving the conversation.

-   **[Voice Input](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-panel-overview.md)**

    Use your voice to send prompts in Now Assist panel premium chats by selecting the microphone button in the input bar, which transcribes your speech to text so you can interact with the assistant hands-free. You can enable or disable voice input through your personal preferences, and your admin can also turn it on or off at the assistant level through Assistant Designer.

-   **[Search enhancements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-panel-overview.md)**

    Get cleaner, more organized search results in Now Assist panel premium chat, with single records displayed as cards and multiple records displayed as tables. You can switch between multiple interactive views in a conversation using a dropdown and use a back button to return to previously viewed content.

-   **[Transition from chat to full search results](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-panel-overview.md)**

    Access the full search results page directly from your Now Assist panel premium chat response by selecting the "Full search experience" link in the sources and more panel. The search results page opens with your original search term already populated, so you can explore the complete set of results without having to retype your query.

-   **[Follow-up questions from search results](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-panel-overview.md)**

    Ask follow-up questions in Now Assist panel premium chat directly from your workspace search results by selecting the "Ask a follow-up" button, which opens a new conversation with the relevant search context already loaded. You can continue exploring a topic conversationally without having to re-enter your query or switch between search and chat.

-   **[Record-specific context](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-panel-overview.md)**

    Get more relevant responses from Now Assist panel premium chat when you're working on a record, as conversations started from a record page are automatically aware of that record's context. You no longer need to manually describe what you're working on — the assistant understands it from the start.

-   **[Upgrade Now Assist panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-panel-overview.md)**

    Upgrade your Now Assist panel experience to premium chat without losing your active conversations, as any conversations in progress remain accessible until you refresh the page. When you open premium chat for the first time after the upgrade, a summary of what's new helps you quickly get familiar with the latest capabilities.


-   **[Manage version](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/manage-version.md)**

    Review the summary, alerts, and notifications regarding changes in model provider version states as they are deprecated or retired.

-   **[Send information from panel conversations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-panel-overview.md)**

    Send information from Now Assist panel conversations directly to relevant fields on incident pages using action buttons. You don't have to manually copy and paste content between Now Assist panel conversations and the incident form.

-   **[Maintain context across tabs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-panel-overview.md)**

    Automatically see the most recent Now Assist panel conversation for an incident when you switch between incident tabs. Now Assist panel remembers which conversation belongs to which incident and displays it when you return to that incident.

-   **[Configure supported record types](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-panel-overview.md)**

    Configure which record types will support Now Assist panel context switching. This enables teams to customize the Now Assist panel experience based on a business unit’s workflow and use cases.

-   **[ServiceNow Otto panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-panel-overview.md)**

    View your Now Assist panel chat history grouped by incident record. Agent conversations related to a specific incident are grouped together rather than organized chronologically, making them easier to find.

-   **[Chat history panel enhancements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-panel-overview.md)**

    View the correct conversation history when you navigate between different incident records.

-   **[Send information to Agent Chat conversation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-panel-overview.md)**

    Send information directly from a Now Assist panel conversation to an agent chat conversation. This makes it easier to collaborate and share helpful information during incident resolution.

-   **[Build custom integrations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-panel-overview.md)**

    Build custom Now Assist panel integrations that are tailored to specific business needs by passing custom context data in any format when initiating Now Assist panel conversations or executing skills.

-   **[Enhanced content detection with third-party guardrails](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/configure-guardrail-model.md)**

    AI Guardian supports third-party service provider guardrails, such as Microsoft Azure, Amazon Bedrock, and Google Model Armor so that any inappropriate content is logged and blocked during content generation. This gives you the flexibility to choose the detection provider that best aligns with your existing cloud infrastructure.

-   **[Post-chat surveys in enhanced chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-panel-enhanced.md)**

    Collect user feedback in enhanced chats through post-chat surveys that trigger on agent task completion instead of waiting for a chat-end event. When an agent completes a task in an agentic flow, the survey can surface based on a configured probability, enabling you to gather insights that were previously unavailable.


-   **[Requester Approval Checklist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/service-portal-approval-checklist-skill.md)**

    The Requester Approval Checklist skill in the ServiceNow AI Platform® generates a structured checklist by mapping real-time request data against your organization’s knowledge articles.

    **Note:** The skill is on by default.


-   **[New system properties for the Now Assist Readiness Evaluation app](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/nare-sys-props.md)**
    -   Reduce performance issues when a large volume of data is assessed with the **sn\_assess.assessment\_limit** system property.
    -   Customize the estimated remediation effort for select efforts with the **sn\_assess.effort\_visibility** system property. Setting this system property to `true` turns on the **Remediation properties** tab in the Now Assist Readiness Evaluation dashboard.
    -   Decide the maximum number of records to process for the ITSM assessment with the **sn\_assess.task\_limit** system property.

-   **[Manage version](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/manage-version.md)**

    Manage the versions of model providers across various skill groups and instance levels in Now Assist. You can modify and update versions for both base system and custom skills.

-   **[Generative AI skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-skills.md)**

    Unlock the benefits of the Now Assist Fulfiller subscription to be able to explore and activate all the skills available in the system from AI Admin Hub.

-   **[Role masking in AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/aia-role-masking.md)**

    Define roles within **role restrictions** for individual skills in AI Admin Hub to enforce resource access restrictions when a skill is invoked. This feature promotes precise control over the resources that can be accessed, like data and APIs.

-   **[Overview tab in AI Admin Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/configuring-now-assist.md)**

    Share your experience in the Now Assist journey by providing feedback when prompted.

-   **[Voice input setting automatically activated](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/activate-now-assist-panel.md)**

    Activate the Now Assist panel to automatically turn on the voice input setting, which is now located on the Assistants page.

-   **[Now Assist panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-panel-overview.md)**

    Request additional information or clarification by asking a follow-up question in the Now Assist panel.

-   **[Synthesized Now Assist responses](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/conversational-interfaces/gchat-conv-integration.md)**

    View synthesized Now Assist responses from within Google Chat to have a richer conversational experience.

-   **[Now Assist support in article optimization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/knowledge-center-article-optimization.md)**

    Improve the quality and health of your knowledge articles by using Now Assist based Article Optimization in the Knowledge Center. Scan knowledge articles and get instant, actionable feedback.

-   **[Use Now Assist to identify knowledge gaps](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/understanding-knowledge-gaps.md)**

    Identify and fill potential knowledge gaps proactively, including missing knowledge articles and recurring issues that lack or have an incomplete knowledge article.

-   **[Agentic workflows from within Google Chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/conversational-interfaces/gchat-conv-integration.md)**

    Initiate and view agentic workflows from within Google Chat.

-   **[Monitor sensitive topic invocations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/reference-for-generative-ai-controller.md)**

    Access the Gen AI Metrics \[sys\_generative\_ai\_metric\] table to review the logged invocations of sensitive topics and gain insights into how these topics are being triggered and monitored.

-   **[Long term stable models](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/long-term-stable-models.md)**

    Long term stable \(LTS\) models are part of Now LLM Service and provide longer model stability windows for regulated industries. These models can integrate with tools to provide governance, monitoring, and compliance controls.

-   **[Create multiple ServiceNow Otto context menu skill configurations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/create-multple-nacm-skill-configuration.md)**

    You can now have multiple Now Assist context menu configurations on the same record form and field. You just have to create the required configuration and add to the form or field.

-   **[Generate KB article with ServiceNow Otto context menu](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/generate-kb-article-with.md)**

    Using the Now Assist Context Menu open prompt inline and pop-over variant you can quickly produce high-quality, accurate, and lucid knowledge articles, saving time and improving support in Knowledge Management.


-   **[AI Readiness Evaluation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-readiness-evaluation-landing-page.md)**

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


-   **[Improve Docs content in Strategic Portfolio Management with ServiceNow Otto context menu](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/answer-queries-with-now-assist-context-menu.md) for SPM**

    Implement the open prompt capability to enhance your ability to add additional context and generate accurate content with Now Assist context menu.

    This feature enables interactive conversations with both supported ServiceNow® generative AI skills and custom-built skills.

-   **[Configure skills with custom prompts for knowledge article templates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/Now-assist-configure-custom-prompts-for-templates.md)**

    As an admin, clone the KB generation skill and update prompts for AI model providers. This feature helps the agent use custom templates and custom prompts to generate knowledge articles with Now Assist from single and multiple knowledge bases.

-   **[Manage AI models](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/manage-large-language-models.md)**

    Choose and update your preferred LLM provider at the instance, skill, or skill group level for Now Assist base system skills.

    Deactivate skills that aren't compatible with any of the LLM providers and access the audit history to view updates by the AI steward in AI Control Tower.

-   **[Configure multilingual service for Now Assist applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/enable-dynamic-translation-for-now-assist-applications.md)**

    Manage the default and supported languages by the different LLM providers under Multilingual service for translation.

-   **[Configure email reply recommendation in the AI Admin Hub console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/configure-email-recommendation.md)**

    Access citations to the articles referenced from the Knowledge Base. Explore references and insert the generated reply to your email.

-   **[ServiceNow Otto panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-panel-overview.md)**

    Use the enhanced Now Assist panel for an intuitive and personalized experience. The updated Now Assist panel can be resized and moved anywhere on the ServiceNow AI Platform.

-   **[AI Guardian supports third-party LLMs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-guardian.md)**

    Extend guardrail support to third-party LLMs, such as Amazon Bedrock, Google Cloud Vertex AI studio, Google AI studio, and Azure OpenAI, to verify that any inappropriate content is logged and blocked during content generation.

-   **[Increase the maximum response token limit for custom skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/configure-skill-prompt.md)**

    Increase the maximum response token limit for a Now Assist custom skill beyond the default value of 1000. This ability supports dynamic pricing based on output tokens and calculates the price for each skill executed per assist.


## UI changes

-   **[Manage model providers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/edit-model-providers.md)**

    Explore the **Manage integrations** option within **Manage model providers** tab now.


-   **[Manage version](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/manage-version.md)**

    Update the model provider version at the instance or the skill level form **Manage model versions** within **Manage AI models** option under Now Assist **Settings** tab.


[Zurich Patch 7](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-7.md)

-   **[Updates made to labels.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/agentic-ai-assessment-dashboard.md)**

    On the Agentic AI- Assessments tab,**Issues** are now renamed **findings**.


-   **[Updated the name of status buttons.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/assessing-go-no-go.md)**

    **Go** button on Now Assist Assessment Home page is now renamed to **Ready**.


-   **[Updates made to legend labels.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/reviewing-now-assist-assessment.md)**

    The **No Blockers** label is now renamed **Informational**. The **Blockers found** label is now renamed **Required**. The **Review for blockers** label is now renamed **Recommended**.

-   **[Zurich Patch 8](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-8.md)**

    [Updated the name of status buttons.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/assessing-go-no-go.md)

    An Agentic AI - HRSD card is available on the **Agentic AI Assessment Home Page** and contains the current readiness status of **Ready** or **Action Required**.


-   **[Analyzing AI performance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-analytics.md)**

    The **Analytics** tab is now renamed to **Performance**.


-   **Coral theme**

    Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.

-   **[Edit an AI skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/edit-a-now-assist-skill.md)**

    You can now view the **Helpful resources** and **Frequently asked questions \(FAQ\)** tabs on the list view of the Now Assist skills page.

-   **[Configure email reply recommendation in the AI Admin Hub console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/configure-email-recommendation.md)**

    The email response creation skill helps you choose the most appropriate template based on your context. Additionally, it identifies the potential errors when a response isn't generated as intended.

-   **[Agentic conversations in Virtual Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/conversational-interfaces/agentic-conversations-vad.md)**

    Halt an agentic conversation mid-query by hovering over the send icon \[Omitted image "vad-send-icon.png"\] Alt text: and selecting the interrupt flow icon \[Omitted image "vad-interrupt-flow-icon.png"\] Alt text: Interrupt flow icon when the icon changes.


## Changed in this release

-   **[Changes to Now Assist usage measurement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/monitoring-now-assist-usage.md)**

    Starting with Australia Early Access, AI usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: AI Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).

-   **[Using AI Readiness Evaluation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/using-now-assist-readiness-evaluation.md)**
    -   View the updated legend that now includes None-XXL estimated remediation efforts along with assessment icon explanations.
    -   Understand estimated remediation efforts more clearly now that blocker areas are included in the estimated remediation efforts and non-blocker observations are not included in estimated remediation efforts.
    -   Select any widget on the Agentic AI- Assessment dashboard and Now Assist assessment dashboard tabs to open that widget's data table in a separate tab.

-   **[Some generative AI skills are turned on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-skills-on-by-default.md)**

    The new default behavior works as follows:

    -   New customers: When you install an AI product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Australia Early Access\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.

-   **[Configure multilingual service for Now Assist applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/enable-dynamic-translation-for-now-assist-applications.md)**

    Enable translation settings is now a multilingual service in the AI Admin Hub console.


## Deprecations

-   In Patch 5, the **Select Use Case** drop-down menu was removed from the Agentic AI - ITSM tab.

## Activation information

-   **[Generative AI skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-skills.md)**

    Now Assist features are available with activation of any Now Assist plugin from ServiceNow Store.


## Additional requirements

The Next Experience UI Framework must be enabled before you can use the Now Assist panel.

## Browser requirements

Now Assist supports various browsers, including Google Chrome and Microsoft Edge. Now Assist isn’t supported in Internet Explorer.

## Accessibility information

-   **[Voice Input in Now Assist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/enable-voice-input-for-now-assist-panel.md)**

    Administrators can enable an optional voice input setting for the Now Assist panel in the AI Admin Hub console. This feature, Voice Input, gives users a voice-to-text input option to access the Now Assist skills in the panel in any supported language. Voice Input helps users with mobility impairments access generative AI skills without using a keyboard. This feature can also be useful to blind or low-vision users, neurodivergent users, non-native language speakers, or users using hand-held devices on the go, such as field service agents.

    Once enabled, Voice Input can be changed using the individual user accessibility preferences. See [Configure Next Experience accessibility preferences](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-user-interface/next-experience-accessibility-preferences.md) for more information.


## Localization information

Now Assist supports Dynamic Translation for Zurich.

## Related ServiceNow applications and features

-   **[AI Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/overview-ais.md)**

    The ServiceNow® AI Search application provides a consumer-grade search engine for Service Portal, Now Mobile, and Virtual Agent. Intelligent query features help you quickly find the answers that you need.

-   **[Document Intelligence](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/document-intelligence-landing.md)**

    The ServiceNow®Document Intelligence \(DocIntel\) application is an artificial intelligence \(AI\) solution that enables any organization to automate and accelerate the process of extracting data from documents. That data can easily be integrated into larger automation workflows to save time and resources.

-   **[Dynamic Translation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/dynamic-translation-overview.md)**

    The ServiceNow® Dynamic Translation application enables you to dynamically translate text entered in an application or chat window for a seamless localization experience.

-   **[Generative AI Controller](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/generative-ai-controller.md)**

    The ServiceNow® Generative AI Controller helps you integrate third-party LLMs with your workflows.

-   **[Knowledge Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/knowledge-management.md)**

    The ServiceNow® Knowledge Management application enables the sharing of information in Knowledge Base. A Knowledge Base contains articles that provide users with information such as self-help, workarounds, and task resolution.

-   **[Knowledge Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/knowledge-center.md)**

    The ServiceNow® Knowledge Center plugin helps you manage your knowledge articles from a single interface consisting of dashboards that provide metrics of articles and facilitate swift actions.

-   **[ServiceNow Otto for Virtual Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/conversational-interfaces/now-assist-in-va-landing.md)**

    Use generative AI skills in your conversational experiences. Now Assist in Virtual Agent uses LLMs to create a natural-language, conversational experience that can improve the success of your self-service workflows.


**Parent Topic:**[Now Assist and agentic AI release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/now-assist-rn-landing.md)


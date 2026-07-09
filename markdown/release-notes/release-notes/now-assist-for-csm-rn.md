---
title: Now Assist for Customer Service Management \(CSM\) release notes
description: The ServiceNow Now Assist for CSM application brings generative AI to Customer Service Management \(CSM\). You can help improve productivity and efficiency by delivering enhanced self-service, recommended actions, and suggested answers. Now Assist for CSM was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 13
keywords: [Now Assist, agentic AI, generative AI, gen AI, genAI]
---

# Now Assist for Customer Service Management \(CSM\) release notes

The ServiceNow® Now Assist for CSM application brings generative AI to Customer Service Management \(CSM\). You can help improve productivity and efficiency by delivering enhanced self-service, recommended actions, and suggested answers. Now Assist for CSM was enhanced and updated in the Zurich release.

## Now Assist for CSM highlights for the Zurich release

[Zurich Patch 10](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-10.md)

-   Resolve cases faster with a new case insights section that consolidates key case details, customer history, sentiment scores, and special handling notes into a single view.
-   View automated sentiment scores and trends from conversations directly on the email interaction page.
-   Enable customers to make case updates through AI voice agent.

[Zurich Patch 9](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-9.md)

-   Automatically evaluate post-interaction customer conversations using AI models that score against a configurable quality rubric, eliminating manual effort.
-   Receive intelligent email reply recommendations on extended table record pages in Now Assist for CSM, helping agents respond faster with less manual effort.

[Zurich Patch 8](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-8.md)

-   Availability of filter controls in Now Assist Guardian for Now Assist for CSM.
-   Availability of AI Workflow tab in Core UI.

[Zurich Patch 7](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-7.md)

-   Enhance the Complaint Case playbook to align playbook activities with agentic workflows, introduce AI‑driven summarization and drafting capabilities, and remove legacy components that are no longer part of the complaint experience.
-   Monitor how users engage with genAI skills in Now Assist for CSM.
-   Get a case status and manage cases through natural voice conversations.

[Zurich Patch 5](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-5.md)

-   Review changes to Now Assist usage measurement.
-   Help reduce manual effort and case closure time for complaint cases with the Complaint Case AI agent collection.

[Zurich Patch 4](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-4.md)

-   Enabled is\_template for all Now Assist skills and added support to clone and customize any base system genAI skill in the Now Assist Skill Kit
-   Defined the navigation path for Sentiment Analysis dashboard in Core UI to make accessing sentiment analysis data easier.
-   Track trending case topics with insights, visualizations, and customizable filters for deeper analysis with the Trending topics dashboard.
-   Monitor customer sentiment across cases with LLM-powered insights and track the sentiment trends in the dashboard.
-   Enable agents to access customer, case, and product details instantly through natural language queries with the provide customer 360 insights agentic workflow.
-   Auto-generate work notes and comment recommendations to help improve agent efficiency with the activity response generation skill.
-   Additional role configuration is required for agentic workflows and AI agents included with Now Assist applications.

[Zurich Patch 1](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-1.md) Enable security in Now Assist for CSM and AI agents and agentic workflows by enforcing access control lists \(ACLs\) and user identity-based permissions.

Early Availability

-   Use the suggested steps that automatically display on the **Recommended Actions** tab to help resolve cases and increase agent productivity.
-   Use Google Gemini and Anthropic Claude on AWS as AI model providers for generative AI skills and AI agents, in addition to Now LLM Service and Azure OpenAI.

See [Now Assist for Customer Service Management \(CSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/now-assist-csm.md) for more information.

**Important:** Now Assist for CSM is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Zurich release

-   **[Case insights section](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/now-assist-csm-summarize-case.md)**

    Resolve cases faster with a new case insights section that brings together key case details, customer summary, issue history, sentiment scores, and special handling notes in one consolidated view.

-   **[Voice-driven case status retrieval and updates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/voice-ai-agent.md)**

    Reduce live agent dependency by enabling customers to check open case statuses and submit case updates through guided voice interactions across Genesys, Twilio, NICE, Five9, 3CLogic, and Amazon Connect CCaaS platforms.

-   **[Customer sentiment analysis on email interaction page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/analyze-sentiments-in-now-assist-for-csm.md)**

    View automated sentiment scores and trends from conversation directly on the email interaction page in Now Assist for CSM, The system reads customer emails and gives a score to show how the customer is feeling, so agents and managers can quickly check the customer's mood without reading the whole conversation.

-   **[Configure extended tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/configure-extended-table-support-for-the-resolution-notes-skill.md)**

    Automatically receive concise summaries of case resolutions in Now Assist for CSM, with the extended table, enabling customer agents to quickly understand resolution details and respond to customers.


-   **[Quality assurance management skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/quality-assurance-management.md)**

    Automatically evaluate agent activity on closed cases using AI models that score each interaction against a configurable quality rubric, eliminating manual sampling and ensuring consistent, objective assessments at scale.

-   **[Extended table support for email reply recommendation skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/configure-extended-table-support-for-the-email-reply-recommendation-skill.md)**

    Automatically receive email reply recommendations on extended table record pages in Now Assist for CSM, allowing agents to quickly respond to customers, provide intelligent recommendations and reducing manual effort.


-   **[AI workflow tab added in Core UI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/ai-workflow-pattern-in-customer-service-management.md)**

    Availability of AI Workflow tab within case view of case table records and email interaction view of interaction records in Core UI, showing agentic workflows and actionable AI-driven insights directly in the record UI.

-   **[Filter controls in Now Assist Guardian](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/now-assist-guardian-csm-filters.md)**

    Availability of filter controls for CSM in the Now Assist Guardian interface, allowing users to toggle the base system filters on and off. Filtered results display in a user-friendly format for quick case review and action.


-   **[Metrics to measure genAI skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/skills-performnace-dashboard.md)**

    Monitor how users engage with genAI and agentic skills in Now Assist for CSM to provide actionable dashboards and reports for workflow optimization.

-   **[Navigation to customer 360 insights summary card in cases](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/now-assist-csm-summarize-case.md)**

    Access all relevant case information by navigating to the customer 360° insights page from the summary card.

-   **[AI voice agent for CSM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/voice-ai-agent.md)**

    Access a case status and create cases through voice interactions with a unified AI voice agent for case management.

-   **[In-product agentic indicators](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/ai-workflow-pattern-in-customer-service-management.md)**

    Identify when agentic AI is active in a record in the **AI Workflows** tab, which includes a presence icon and record indicator.


-   **[Complaint Case AI agents collection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/accelerate-complaint-case-handling.md)**

    The Complaint Case AI agent collection automates complaint handling by gathering missing details, analyzing sentiment, categorizing issues, and suggesting resolutions. It streamlines intake, triage, and communication, which helps reduce case closure time.


-   **[Enabled the is\_template property](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/clone-the-now-assist-for-csm-skills.md)**

    Enabled the is\_template property for all Now Assist skills to clone consistently. Clone any base system genAI skill and customize it in the Now Assist Skill Kit to set up quickly and simplify skill modification. Applies to all Now Assist for CSM skills.

-   **[Access the Sentiment analysis dashboard in Core UI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/use-sentiment-analysis-dashboard.md)**

    Locate and access sentiment analysis data without searching through multiple menus with a defined navigation path in the Sentiment analysis dashboard in the Core UI interface.

-   **[Sentiment trends analysis dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/use-sentiment-analysis-dashboard.md)**

    Get a comprehensive view of customer sentiment across case. The dashboard uses LLM-powered insights to explain sentiment changes and lets you drill down to find root causes and real time insights—helping managers take targeted actions.

-   **[Trending topics dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/view-trending-topics-dashboard.md)**

    Get a comprehensive view of trending topics across cases along with insights and visualizations to facilitate deeper analysis. This feature helps support teams track trend progression, regional impact, and analyze specific trends using customizable filters.

-   **[Provide customer 360 insights agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/customer-service-management-ai-agent-collection-customer-360.md)**

    Use the provide customer 360 insights agentic workflow to provide synthesized and relevant customer insights to live agents via conversations. This agentic workflow supports human agents by responding to natural language queries regarding cases, customer history, products, and interactions. This feature expedites access to vital information and case resolution, identifies patterns, and leverages past similar cases for guidance and triggers actions from the Now Assist panel.

-   **[Activity response generation skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/generate-a-recommendation-to-respond-to-an-activity.md)**

    Use the activity response generation skill to automatically generate recommendations for resolution notes, work notes, and comments. This feature helps agents add meaningful updates to case records, improving efficiency and interactions.

-   **[Now Assist context menu configuration for extended tables within resolution notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/customize-now-assist-context-menu-for-skills.md)**

    Configure output fields for resolution notes through the Now Assist context menu configuration page so skills apply to extended tables without any additional setup.


-   **[Use the triage cases agentic workflow security directives](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/case-resolving-use-case.md)**

    Implement security on AI agents and agentic workflows through ACLs and user identities.

-   **[Now Assist for CSM genAI security directives](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/configure-chat-summarization-in-now-assist_0.md)**

    Implement security in Now Assist for CSM skills through ACLs and user identities.


-   **[New third-party AI model provider options available for all AI applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/exploring-large-language-models.md)**

    Google Gemini and AWS Claude are available for generative AI skills and AI agents, in addition to Now LLM Service and Azure OpenAI.


## Changed in this release

-   **[Now LLM service deprecation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/exploring-large-language-models.md)**

    The Now LLM Service is no longer the default model provider for new or inactive AI assets. A third-party LLM is now selected by default, while existing configurations using the Now LLM Service continue unchanged. The Now LLM Service is still available for manual selection.

-   **[Automated quality assurance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/quality-assurance-management.md)**

    Enable admins to filter scoring parameters and sort agents and case lists. Admins can sort data, manage filters, and easily organize cases on the dashboard with the new sorting, visibility, and skill management capabilities.

-   **[Activate Now Assist Skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/activate-now-assist-for-customer-service-management-csm-skills_0.md)**

    Admins can view detailed information about each Now Assist skill to make faster and more informed decisions about enabling skill capabilities


-   **[Provide Customer 360 insights agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/customer-service-management-ai-agent-collection-customer-360.md)**

    Enhanced Provide Customer 360 Insights with Enterprise Graph and AI agent deep research for richer, more contextual query results.

-   **[Triage cases agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/case-resolving-use-case.md)**

    Multilingual and localization flows in the Triage Cases workflow are now fully supported.


-   **[Configure knowledge generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/configure-knowledge-generation-in-now-assist_0.md)**

    Enable users with the **sn\_skill\_builder.admin** role to generate knowledge base articles in Now Assist for CSM by selecting the required input fields from a task record, reducing manual effort and streamlining the knowledge base generation process.


-   **[Configure Sidebar Summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/configure-sidebar-summarization-in-now-assist.md)**

    Enable customers to generate summaries from the required case and task tables in Now Assist for CSM as default tables can now be pre-selected and locked.


-   **[Changes to Complaint Case AI agent collection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/accelerate-complaint-case-handling.md)**

    Updates have been added to the Complaint Case playbook to work better with the Complaint Case AI agent:

    -   Triage displays complaint details and enables a human agent to identify and request missing information.
    -   Complaint‑specific case summarization is available directly within the playbook.
    -   Replace research case task activities with case tasks list activity.
-   **[Enhancements in the Sentiment analysis dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/use-sentiment-analysis-dashboard.md)**
    -   Sentiment analysis dashboard support has expanded to include interaction records, and positive and negative sentiment drivers have been consolidated into a single Sentiment Drivers view.
    -   The top negative assignment group and number of cases by channel visualizations have been merged into the new Impact Explorer visualization for streamlined analysis.
    -   Widget placement in the Workforce Optimization dashboard has been optimized for accessing insights and trends across interfaces.
-   **[Enhancements in Trending topics dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/view-trending-topics-dashboard.md)**
    -   The Accounts, Products, Assignment Groups, and Channels graphs have been consolidated into the Impact Explorer card.
    -   Search and pagination have been added to the list header.
    -   The Historical trends resurfacing graph has been added the Trending topics dashboard to show historical trends at a glance.
    -   Trending topics have been expanded beyond the top 10 results to provide deeper insight into emerging patterns.
    -   The trending topics widget has been added in the Workforce optimization dashboard as the **AI insights** tab.

-   **[Changes to Now Assist usage measurement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/monitoring-now-assist-usage.md)**

    Starting with Zurich Early Access, AI usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


-   **[Enhancement in case summarization skill flow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/case-summarization-generation-in-now-assist.md)**

    The **Define trigger** step has been added to the case summarization flow. This step enables admins to choose between the User Trigger option, where users select a button to generate a summary, and the Automatic Trigger option, where summaries are automatically generated based on specified conditions.

-   **[Enhancement in email reply recommendation skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/generate-email-reply-recommendations.md)**

    Generate reply suggestions in the compose area using preset templates that include headers, footers, and signatures.

-   **[Unified admin experience for Now Assist skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/customizing-now-assist-skills.md)**

    Skills cloned in Now Assist Admin console can now be edited in Now Assist Skill Kit. This update unifies the admin experience across Now Assist Admin and Now Assist Skill Kit, enabling users to add headers, configure prompts, and manage Now Assist skills in one location. The migration supports case summarization and resolution notes generation.

-   **[Role configuration required for agentic workflows and AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/aia-role-masking.md)**

    Agentic workflows and AI agents included with Now Assist applications require additional security configuration. If you select **Users with selected roles** for your user access security controls for an agentic workflow or AI agent, you must add the installed roles, or they won't execute. Data access settings must also include these roles. See the documentation for the agentic workflow or AI agent for the specific roles you must add. After the roles are configured, users must have the specified role to invoke the agentic workflow or AI agent.

-   **[Display sentiment scale in case list view](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/analyze-sentiments-in-now-assist-for-csm.md)**

    Sentiment scoring has been added to both the case record page and list view across cases, giving agents immediate visibility into the emotional tone of customer interactions. The sentiment scale ranges from very positive, positive, neutral, negative, to very negative.


-   **[Multilingual support](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/now-assist-csm-supporting-info.md)**

    Enhanced multilingual support in chat summarization, resolution notes, and knowledge generation. Leveraged native multilingual LLMs for improved fluency and domain specificity, addressing translation inconsistencies across Tier 1 and Tier 2 languages.


-   **[Suggested steps in the Recommended Actions tab](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/suggested-steps-generation-in-now-assist-for-customer-service-management-csm.md)**

    View the suggested steps on the **Recommended Actions** tab in the contextual side panel. If suggested steps are available for a case, Now Assist for CSM generates and displays these steps in a card at the top of the **Recommended Actions** tab.

-   **[KB generation skill configuration enhancement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/now-assist-csm-configuring.md)**

    The **Is Template** field on the KB generation skill configuration record is enabled by default. With the skill\_builder.admin role, you can copy or clone the KB generation skill and customize the prompt in the skill kit.


## Activation information

Now Assist features are available with activation of the Now Assist for CSM plugin. For more information, see [Install Now Assist plugins](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/install-now-assist-feature-plugins.md).

Starting with Vancouver Patch 4, Now Assist for CSM is supported.

Starting with Zurich Patch 7, Customer Service Management AI agent collection is supported.

## Additional requirements

Check your entitlements to determine whether you have access to the Now Assist for CSM application.

## Related ServiceNow applications and features

-   **[Now Assist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/platform-now-assist-landing.md)**

    Help improve the productivity and efficiency in your organization, deliver better self-service, recommend actions, provide answers, and empower your users to search more effectively.

-   **[Now Assist Admin console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/configuring-now-assist.md)**

    Use the Now Assist Admin console to provide you with quick and easy access to the important information that you need to set up, configure, and monitor Now Assist applications and features.

-   **[Now Assist panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-panel-overview.md)**

    Use this conversational interface in CSM Configurable Workspace to summarize a chat, a case, or resolution notes so that you can get the context of this information more quickly.

-   **[Now Assist skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-skills.md)**

    Use the Now Assist products to provide generative AI skills to meet the needs of users in different workflows, including case or incident summarization, chat summarization, resolution notes generation, and code generation.


**Parent Topic:**[Customer Service Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/customer-service-mgmt-rn-landing.md)

**Parent Topic:**[Now Assist and agentic AI release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/now-assist-rn-landing.md)


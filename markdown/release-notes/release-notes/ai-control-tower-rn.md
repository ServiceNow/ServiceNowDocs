---
title: AI Control Tower release notes
description: The ServiceNow AI Control Tower application provides a centralized workspace for AI stewards to manage and monitor AI within the enterprise. AI Control Tower was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 16
---

# AI Control Tower release notes

The ServiceNow® AI Control Tower application provides a centralized workspace for AI stewards to manage and monitor AI within the enterprise. AI Control Tower was enhanced and updated in the Zurich release.

## AI Control Tower highlights for the Zurich release

[Zurich Patch 11](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-11.md)

-   The AI asset list in AI Inventory includes Asset State and Asset Status columns.
-   The system assigns a unique ID to every asset. The ID appears in the Asset tag field under Asset details.
-   AI Service Graph Connectors for OpenAI, Moveworks, OCI, and IBM are available in AI Control Tower for AI connections.
-   The AI Service Graph Connector for OpenAI discovers AI models and tracks model usage.
-   When you mark a managed asset as unmanaged, the asset's active workflows, tasks, and governance processes are canceled, and the asset is excluded from value tracking.
-   When you mark an unmanaged asset as managed, the asset is actively monitored and governed, making it visible and eligible for governance workflows and value tracking.

[Zurich Patch 8](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-8.md)Configure and create automation rules to set AI assets as managed assets.

[Zurich Patch 7](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-7.md)

-   Use new security metrics to monitor your LLM and AI agent output for potential security and content policy violations, potential PII, and other potential threats.
-   Gain visibility into MCP client-server interactions routed through this instance’s AI Gateway.
-   AI assets—Including AI models, AI systems, prompts, datasets, and MCP servers can be categorized as either managed or unmanaged. Managed assets benefit from AI Control Tower features such as governance, lifecycle management, value assessment, risk classification, security, and privacy. Unmanaged assets, on the other hand, don’t have access to these AI Control Tower capabilities.
-   AI connections are introduced in AI Control Tower using Service Graph Connectors. AI connections are a combination of hyperscalars, AI apps, and agentic AI frameworks. The AI Service Graph Connectors available from March 2026:
    -   [AWS](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/aws_0.md)
    -   [Microsoft](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/microsoft.md)- Azure Foundry and Copilot
    -   [Google Cloud Platform \(GCP\) Vertex AI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/gcp-vertex-ai.md)
    -   [n8n](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/n8n.md)
    -   [LangGraph](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/langgraph.md)
    -   [Salesforce](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/salesforce.md)
-   Manage the end-to-end life cycles of your agentic AI systems.
-   Define the intended use and purpose of an AI system so that you can determine its benefits and risks.
-   AI Gateway offers MCP Global Clients, which can be used across all servers.
-   AI Gateway offers MCP Catalog to choose while adding MCP servers.
-   MCP server can be added to an AI Asset inventory from AI Control Tower.

[Zurich Patch 5](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-5.md) Review changes to Now Assist usage measurement.

[Zurich Patch 4](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-4.md)

-   Identify ServiceNow® AI assets that impact your security posture using the ServiceNow® AI security score and AI insights.
-   Access and monitor security for AWS Bedrock agents running as privileged users, autonomous vs. Supervised tools, and dormant agents.
-   Monitor sensitive data detection, prompt injection, and offensive content metrics to help identify and mitigate AI-driven security and compliance risks before they impact workflows or expose sensitive information.
-   See more details in the access map about agent access issues to help you troubleshoot quickly.
-   Audit logs capture configuration changes made on Data, Approvals, and AI model providers categories.
-   Discover AI assets built and deployed in Google Cloud Platform \(GCP\) Vertex AI, Copilot Studio, and Azure AI Foundry.
-   AI Gateway enables enterprises to actively manage, govern, and observe their MCP traffic, ensuring secure operation of agentic workflows across enterprise boundaries.

[Zurich Patch 1](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-1.md)

-   Monitor the performance of guardrails enabled through Now Assist Guardian using the **Health** tab.
-   Measure and improve the quality of interactions with virtual agents using the **Evaluation** tab.
-   Display data based on the chosen allowed model providers and the status of the fallback in the Impact Summary table on the AI model providers section.
-   Synchronize AI agents automatically when an AI asset is synchronized.

-   Enhance the Product Owner experience with a personalized home page, value management tools to manage AI investments, and enhanced visibility into AI assets to simplify task management.
-   Evaluate AI productivity and adoption across the enterprise using defined value metrics and performance indicators to drive data-informed decisions and maximize AI impact.
-   Access and security monitoring for ServiceNow® AI agents, especially around access issues, agents running as privileged users and dormant agents.
-   Discover AI assets built and deployed in AWS Bedrock and Azure Foundry.
-   Enable choice for third-party model providers powering ServiceNow® skills and agents.
-   Access to aggregated risk scores to improve decision-making, manage risks, and help to promote ethical and transparent AI practices.
-   Monitor performance, track progress, and make informed decisions related to your AI strategies, goals, targets, and the associated work from the **AI strategy** tab.
-   Track costs of your AI projects, epics, demands, and track key project risks, issues, decisions, actions, and changes from the **AI strategy** tab.

See [AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/ai-control-tower-landing.md) for more information.

**Important:** AI Control Tower is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Zurich release

-   **[Security &amp; privacy tab in AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/security-privacy-tab.md)**
    -   Measure whether your model's output or behavior potentially violates predefined LLM guardrail policies using the Data integrity incident detection chart.
    -   Review potential threats in AI agent output in Agent goal deviation, Output with PII detected, and Agentic output injection detection charts.
    -   Monitor MCP server access by AI Gateway with these new charts: Clients connecting to MCP servers, authorized access attempts, and failed access attempts.
-   **[Data section on Configurations page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/data.md)**

    Enable and set up data integrity incident detection, agent goal deviation, and output screening metrics to measure the integrity of your data model and potential threats in LLM output.

-   **[Manage agentic AI system life cycles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/create-ai-system-assets.md)**

    Create AI system assets to track and manage the complete life cycles of your agentic AI systems, from onboarding to deployment. Gain comprehensive insight into each agentic AI system and take any necessary actions to successfully complete each life-cycle stage. By managing the life cycles of your agentic AI systems, you can extend their lifespans, reduce downtime, and optimize licensing costs.

-   **[Define the use and purpose of an AI system](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/create-ai-system-assets.md)**

    Specify the intended use and purpose of an AI system. Provide insight into who is using the AI system, what the AI system is being used for, and how the AI system works and provides value. This information can help you determine the benefits and risks that are associated with the AI system. For more information on classifying AI systems based on regulatory risk at intake by applying a configured Risk Assessment Methodology \(RAM\), see [Assessment templates and risk assessment methodologies](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/governance-risk-compliance/assessment-templates-rams.md) and [Request an AI use case](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/governance-risk-compliance/request-ai-system.md).

-   **[Associate additional related AI asset types with AI systems](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/create-ai-system-assets.md)**

    Associate the following additional related AI asset types with your AI systems:

    -   If an AI system has an Asset type of Generative AI or Agentic AI, you can associate it with any of its supported components or subsystems.
    -   If an AI system has an Asset type of Agentic AI, you can associate it with any of its integrated AI tools.
-   **[Create change and offboarding requests for additional AI asset types](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/creating-ai-asset-requests.md)**

    Create change requests for the following additional AI asset types:

    -   AI systems with an Asset type of Agentic AI
    -   Datasets
    In addition, create offboarding requests for the following additional AI asset types:

    -   AI systems with an Asset type of Agentic AI
    -   AI models
    -   Datasets
    -   MCP servers

-   **[Security &amp; privacy tab in AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/security-privacy-tab.md)**
    -   Identify ServiceNow® AI assets that impact your security posture using the ServiceNow® AI security score and AI insights. AI insights highlight key metric changes, recommend next steps, enabling you to quickly understand the impacts and take action.
    -   Access and monitor security for AWS Bedrock agents running as privileged users, autonomous vs. supervised tools, and dormant agents.
    -   Monitor sensitive data detection, prompt injection, and offensive content metrics to help identify and mitigate AI-driven security and compliance risks before they impact workflows or expose sensitive information. AI security tasks are created automatically from Dormant AI systems metrics to streamline your workflow and quickly resolve issues. You can also create AI security tasks directly from more areas, such as access issues and privileged AI agents metrics.
    -   Review Autonomous vs. supervised systems metrics based on AI tools. Previously, the metrics were based on workflows.
    -   Show Access issues metrics for only those agents with issues. Previously, agents with issues and no issues were shown.
    -   See more details about agent access issues in the access map to help you troubleshoot quickly. For example, you can see the user ID of the user who executed the agent and the workflow and tool associated with the access issue, if applicable.
-   **[AI Gateway tab in AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/ai-gateway-tab.md)**

    The **AI Gateway** tab shows the metrics at the MCP server level, listing all connected MCP servers along with the total number of transactions for each server and its success rate.

-   **[Data section on Configurations page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/data.md)**

    See a read-only view of your data privacy configuration for sensitive data patterns in the Data privacy page. Use this page as a quick reference when troubleshooting sensitive data charts.

-   **[AI Task section on AI assets page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/ai-assets.md)**

    Review all AI security tasks for your instance in the All Security Tasks page. You can also create an AI task on this page.

-   **[Enhance control of AI asset life cycle through change and offboarding requests](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/creating-ai-asset-requests.md)**

    Enhance the management of deployed AI assets by using the change request workflow to make necessary edits to AI assets that have already undergone review and onboarding. Furthermore, facilitate the retirement of AI assets by submitting an offboarding request, ensuring a structured and controlled process for removing assets that are no longer needed or have been superseded.


-   **Health tab in AI Control Tower**

    Monitor and evaluate the effectiveness of offensive content and prompt injection guardrails active on your AI assets.


-   **[AI strategy with Strategic Planning](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/ai-strategy-aict.md)\(Requires SPM\)**
    -   Monitor and track your AI strategies and associated goals and targets.
    -   Track the costs of your AI projects, epics, and demands.
    -   Monitor key project risks, issues, decisions, actions, and changes.
-   **[AI strategy with Goal Framework](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/ai-strategy-aict.md) \(Requires SPM\)**

    Monitor and track your AI strategies and associated goals and targets.

-   **[AI connections](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/enterprise-ai-discovery.md)**
    -   Discover and add AI agents and related models and tools to the AI inventory through integration with AWS Bedrock.
    -   Discover and add AI agents and related models and tools to the AI inventory through integration with Azure AI Foundry.
    -   Configure AI discovery setup and visibility of connections.
-   **[Value tab in AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/aict-value-tab.md)**
    -   Gain insights into the value realized from AI skills and features. The Value insights dashboard page gives you insights into the estimated productivity gains as a result of using AI systems.
    -   Define and measure value relevant to your AI systems using customizable value templates.
    -   Perform calculations and approximations for the read and write time saved by users using AI systems by using data points and timestamps from the invoking records.
    -   Understand the key usage and performance indicators that help you evaluate the adoption of Now Assist in your organization.
    -   Provide insights on success rate visualization by department, country, and AI assets along with the indicators for task closure efficiency.
-   **[Value templates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/using-value-templates.md)**
    -   Create, manage, and use templates from a Global Template Repository across multiple AI assets, so that you can standardize and streamline your AI experience, and track usage of AI systems, use cases, and skills more effectively.
    -   Enable users to edit, view, and create customized value templates by enabling a value template assignment experience in inventory records.
    -   Provide transparency to value calculations of each AI system through value templates.
    -   Perform calculations and approximations for the read and write time saved by users using AI systems by using data point and timestamps from the invoking records.
-   **[Risk and compliance tab](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/governance-risk-compliance/risk-and-complaince-tab.md)**

    Display the risk classification of AI assets and the compliance posture for selected authority documents and policies through the **Risk and compliance** tab. This tab provides visibility into AI systems, models, and datasets. The Risk overview section uses visual charts to categorize AI assets.

    Review adherence to frameworks in the Compliance overview section. For example, adherence to the NIST AI Risk Management Framework or the EU Artificial Intelligence Act, presenting scores based on citations and control attestations that are set by the customer. You can filter data by authority documents or policies, view overall compliance percentages, and identify critical issues and AI cases tied to items deemed non-compliant by the customer.

    -   Build trust in the AI asset inventory to effectively manage AI-related risks across the enterprise.
    -   Drive enterprise-wide risk visibility by aggregating individual scores into a consolidated AI risk profile to support informed mitigation decisions.
    -   Display real-time residual risk scores on the home page to help practitioners identify high-risk AI assets and prioritize mitigation actions.
    -   Use enhanced impact assessment templates to help manage and oversee compliance with regulatory requirements.
    -   Perform bulk control attestations using Core UI to validate multiple controls across AI assets, improving efficiency for large-scale assessments.
    -   Adopt a proactive approach by leveraging comprehensive AI risk and compliance scoring across the entire AI asset inventory.
-   **[AI cases tab in AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/ai-cases-tab-aict.md)**

    Gain a centralized overview of all your AI asset cases and inquiries by using the AI cases. On the **AI cases** tab, you see a list of records that include the case details such as the status, priority, owner, and timeline of your AI cases. You can monitor the progression of a case, stay informed about ongoing investigations, follow up on pending actions, and help to ensure timely resolutions. On this tab, you can also find filtering and sorting options that help you to prioritize cases that require immediate attention.

    -   Use the enhanced home page to access a single, unified view of all AI-related cases and inquiries.
    -   Track, manage, and respond to AI-related cases more efficiently through centralized case visibility.
-   **[Security &amp; privacy tab in AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/security-privacy-tab.md)**

    Review your AI security health metrics in the **Security and Privacy** tab. Use the access map for a comprehensive overview of agentic workflows, tools, and agent details. The map helps to show how AI agents interface with workflows and tools to accomplish a task. Additionally, you can analyze current AI access, investigate ongoing access issues, and review your AI usage metrics.

    Control which third-party models OEM by ServiceNow are enabled for Now Assist AI implementation and how they’re used.

-   **[Specify additional details during AI asset creation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/creating-ai-assets.md)**

    Use the following fields to specify additional details about your AI systems, AI models, prompts, and datasets when you create AI assets:

    -   AI systems:
        -   Managed by
        -   License details
        -   Supported locations
    -   AI models:
        -   Managed by
        -   License details
        -   Supported locations
    -   Prompts: Managed by
    -   Datasets:
        -   Managed by
        -   Creation type
        -   Department
        -   Dataset creation date

## UI changes

-   **Coral theme**

    Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.


[Zurich Patch 7](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-7.md)

-   **[Drop-down menu for associating AI assets with related assets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/view-ai-assets-lifecycle-stage.md)**

    In both the AI asset creation forms and AI asset records, the **Add new** button that previously enabled you to associate AI assets with other related assets has changed into an Add from inventory drop-down menu with the **Add from inventory** and **Create** options. The **Add from inventory** menu option enables you to associate AI assets with related assets that are currently available in your asset inventory. The **Create** menu option enables you to associate AI assets with related assets that are not currently available in your asset inventory.

-   **[Editable asset details fields on the Details tab of AI asset records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/view-ai-assets-lifecycle-stage.md)**

    You can now modify asset details fields directly on the **Details** tab of your AI asset records.

-   **[Related asset lists in AI asset records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/view-ai-assets-lifecycle-stage.md)**

    The lists of related assets in each AI asset record has moved from the **Related assets** tab to the **Details** tab.


-   **[Product Owner portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/product-owner-portal.md#section_om4_mbg_xfc)**
    -   Widgets from both the **Value** and **Adoption** tabs are now combined and accessible within the updated **Value** tab.
    -   The **Create AI Asset** button is added on the AI Control Tower home page.
    -   A new Quick link option is added to the employee center to help navigate AI asset owners and AI stewards to the AI Control Tower workspace home page.

## Changed in this Zurich release

-   **[Security &amp; privacy tab in AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/security-privacy-tab.md)**
    -   The Autonomous vs. supervised AI tools chart has been removed.
    -   The Prompt injection, Offensive content, and Sensitive data tabs have been removed and replaced by Access and Guardrails tabs. Metrics have been reorganized into those two tabs.
    -   In **Configurations**, under **Data**, the **Data privacy** tab was renamed to **Security &amp; privacy**. In that tab, the data leak detection and anonymization section was renamed to sensitive data input and anonymization.

-   **[Changes to Now Assist usage measurement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/monitoring-now-assist-usage.md)**

    Starting with Zurich Early Access, AI usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


-   **[Changes in Zurich Patch 4](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-4.md)**
    -   The AI asset inventory plugin structure has been updated.
    -   Product owner view: Added a role called AI asset owner \[sn\_ai\_asset\_mgmt.ai\_asset\_owner\], which enables the Product Owner view experience with a personalized home page and enhanced visibility into AI assets to simplify task management.
    -   AI discovery: The Innovation lab store application \(AWS AI discovery plugin\) is decommissioned. Uninstall the AWS AI discovery plugin prior to installing the AI discovery plugin \(sn\_ai\_disc\).
    -   AI cases management has moved under the **AI cases** tab on the AI Control Tower home page.

## Activation information

Install AI Control Tower by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Accessibility information

-   **Dark theme**

    The new Coral theme includes a dark theme option for web and mobile experiences. This option is commonly used to alleviate eye strain and improve readability.


## Related ServiceNow applications and features

-   **[AI Risk and Compliance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/governance-risk-compliance/ai-risk-and-compliance.md)**

    Enable risk and compliance managers to verify organizational compliance with regulations and policies governing AI systems by using the AI Risk and Compliance application, along with the AI Control Tower.

-   **[Strategic Planning](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-business-management/goal-management-in-alignment-planner-workspace.md)**

    Prioritize, roadmap, and track work when using traditional, agile, or hybrid methodologies with ServiceNow® Strategic Planning. Align strategy to execution by defining and tracking goals across your organization. When the Strategic Planning application is installed, the **AI strategy** tab appears in the AI Control Tower workspace, featuring different widgets for AI strategies, goals, targets, costs of planning items, prioritized work, and RIDAC details.

    Strategic Planning is available with an SPM Professional license.

-   **[Goal Framework](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-business-management/goal-framework.md)**

    Create goals, set targets for them, and evaluate the progress of the goals and targets to accomplish your organizational plans and drive business outcomes with the ServiceNow® Goal Framework application. When the Goal Framework application is installed, the **AI strategy** tab appears in the AI Control Tower workspace, featuring different widgets for AI strategies, goals, and targets.

    Goal Framework is available with an SPM Standard license.


**Parent Topic:**[AI Experiences release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/intelligent-experiences-rn-landing.md)

**Parent Topic:**[Now Assist and agentic AI release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/now-assist-rn-landing.md)


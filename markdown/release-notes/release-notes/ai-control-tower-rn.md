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

[Zurich Patch 8](../quality/zurich-patch-8.md)Configure and create automation rules to set AI assets as managed assets.

[Zurich Patch 7](../quality/zurich-patch-7.md)

-   Use new security metrics to monitor your LLM and AI agent output for security policy violations, PII, and other potential threats.
-   Gain visibility into MCP server access by ServiceNow AI agents on the same instance.
-   AI assets—Including AI models, AI systems, prompts, datasets, and MCP servers can be categorized as either managed or unmanaged. Managed assets benefit from AI Control Tower features such as governance, lifecycle management, value assessment, risk classification, security, and privacy. Unmanaged assets, on the other hand, don’t have access to these AI Control Tower capabilities.
-   AI connections are introduced in AI Control Tower using Service Graph Connectors. AI connections are a combination of hyperscalars, AI apps, and agentic AI frameworks. The AI Service Graph Connectors available from March 2026:
    -   [AWS](https://www.servicenow.com/docs/access?context=aws_0&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)
    -   [Microsoft](https://www.servicenow.com/docs/access?context=microsoft&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)- Azure Foundry and Copilot
    -   [Google Cloud Platform \(GCP\) Vertex AI](https://www.servicenow.com/docs/access?context=gcp-vertex-ai&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)
    -   [n8n](https://www.servicenow.com/docs/access?context=n8n&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)
    -   [LangGraph](https://www.servicenow.com/docs/access?context=langgraph&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)
    -   [Salesforce](https://www.servicenow.com/docs/access?context=salesforce&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)
-   Manage the end-to-end life cycles of your agentic AI systems.
-   Define the intended use and purpose of an AI system so that you can determine its benefits and risks.
-   AI Gateway offers MCP Global Clients, which can be used across all servers.
-   AI Gateway offers MCP Catalog to choose while adding MCP servers.
-   MCP server can be added to an AI Asset inventory from AI Control Tower.

[Zurich Patch 5](../quality/zurich-patch-5.md) Review changes to Now Assist usage measurement.

[Zurich Patch 4](../quality/zurich-patch-4.md)

-   Identify ServiceNow® AI assets that impact your security posture using the ServiceNow® AI security score and AI insights.
-   Access and monitor security for AWS Bedrock agents running as privileged users, autonomous vs. Supervised tools, and dormant agents.
-   Monitor sensitive data detection, prompt injection, and offensive content metrics to help identify and mitigate AI-driven security and compliance risks before they impact workflows or expose sensitive information.
-   See more details in the access map about agent access issues to help you troubleshoot quickly.
-   Audit logs capture configuration changes made on Data, Approvals, and AI model providers categories.
-   Discover AI assets built and deployed in Google Cloud Platform \(GCP\) Vertex AI, Copilot Studio, and Azure AI Foundry.
-   AI Gateway enables enterprises to actively manage, govern, and observe their MCP traffic, ensuring secure operation of agentic workflows across enterprise boundaries.

[Zurich Patch 1](../quality/zurich-patch-1.md)

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

See [AI Control Tower](https://www.servicenow.com/docs/access?context=ai-control-tower-landing&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US) for more information.

**Important:** AI Control Tower is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Zurich release

-   **[Security &amp; privacy tab in AI Control Tower](https://www.servicenow.com/docs/access?context=security-privacy-tab&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**
    -   Measure whether your model's output or behavior violates predefined security policies using the secure policies violations chart.
    -   Review potential threats in AI agent output in output deviation, output with PII detected, and high-risk output charts.
    -   Monitor MCP server access by AI Gateway with these new charts: Clients connecting to MCP servers, authorized access attempts, and failed access attempts.
-   **[Data section on Configurations page](https://www.servicenow.com/docs/access?context=data&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Enable and set up secure policies violation, output deviation, and output screening metrics to measure the integrity of your data model and potential threats in LLM output.

-   **[Manage agentic AI system life cycles](https://www.servicenow.com/docs/access?context=create-ai-system-assets&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Create AI system assets to track and manage the complete life cycles of your agentic AI systems, from onboarding to deployment. Gain comprehensive insight into each agentic AI system and take any necessary actions to successfully complete each life-cycle stage. By managing the life cycles of your agentic AI systems, you can extend their lifespans, reduce downtime, and optimize licensing costs.

-   **[Define the use and purpose of an AI system](https://www.servicenow.com/docs/access?context=create-ai-system-assets&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Specify the intended use and purpose of an AI system. Provide insight into who is using the AI system, what the AI system is being used for, and how the AI system works and provides value. This information can help you determine the benefits and risks that are associated with the AI system. For more information on classifying AI systems based on regulatory risk at intake by applying a configured Risk Assessment Methodology \(RAM\), see [Assessment templates and risk assessment methodologies](https://www.servicenow.com/docs/access?context=assessment-templates-rams&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US) and [Request an AI use case](https://www.servicenow.com/docs/access?context=request-ai-system&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US).

-   **[Associate additional related AI asset types with AI systems](https://www.servicenow.com/docs/access?context=create-ai-system-assets&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Associate the following additional related AI asset types with your AI systems:

    -   If an AI system has an Asset type of Generative AI or Agentic AI, you can associate it with any of its supported components or subsystems.
    -   If an AI system has an Asset type of Agentic AI, you can associate it with any of its integrated AI tools.
-   **[Create change and offboarding requests for additional AI asset types](https://www.servicenow.com/docs/access?context=creating-ai-asset-requests&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Create change requests for the following additional AI asset types:

    -   AI systems with an Asset type of Agentic AI
    -   Datasets
    In addition, create offboarding requests for the following additional AI asset types:

    -   AI systems with an Asset type of Agentic AI
    -   AI models
    -   Datasets
    -   MCP servers

-   **[Security &amp; privacy tab in AI Control Tower](https://www.servicenow.com/docs/access?context=security-privacy-tab&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**
    -   Identify ServiceNow® AI assets that impact your security posture using the ServiceNow® AI security score and AI insights. AI insights highlight key metric changes, recommend next steps, enabling you to quickly understand the impacts and take action.
    -   Access and monitor security for AWS Bedrock agents running as privileged users, autonomous vs. supervised tools, and dormant agents.
    -   Monitor sensitive data detection, prompt injection, and offensive content metrics to help identify and mitigate AI-driven security and compliance risks before they impact workflows or expose sensitive information. AI security tasks are created automatically from Dormant AI systems metrics to streamline your workflow and quickly resolve issues. You can also create AI security tasks directly from more areas, such as access issues and privileged AI agents metrics.
    -   Review Autonomous vs. supervised systems metrics based on AI tools. Previously, the metrics were based on workflows.
    -   Show Access issues metrics for only those agents with issues. Previously, agents with issues and no issues were shown.
    -   See more details about agent access issues in the access map to help you troubleshoot quickly. For example, you can see the user ID of the user who executed the agent and the workflow and tool associated with the access issue, if applicable.
-   **[AI Gateway tab in AI Control Tower](https://www.servicenow.com/docs/access?context=ai-gateway-tab&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    The **AI Gateway** tab shows the metrics at the MCP server level, listing all connected MCP servers along with the total number of transactions for each server and its success rate.

-   **[Data section on Configurations page](https://www.servicenow.com/docs/access?context=data&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    See a read-only view of your data privacy configuration for sensitive data patterns in the Data privacy page. Use this page as a quick reference when troubleshooting sensitive data charts.

-   **[AI Task section on AI assets page](https://www.servicenow.com/docs/access?context=ai-assets&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Review all AI security tasks for your instance in the All Security Tasks page. You can also create an AI task on this page.

-   **[Enhance control of AI asset life cycle through change and offboarding requests](https://www.servicenow.com/docs/access?context=creating-ai-asset-requests&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Enhance the management of deployed AI assets by using the change request workflow to make necessary edits to AI assets that have already undergone review and onboarding. Furthermore, facilitate the retirement of AI assets by submitting an offboarding request, ensuring a structured and controlled process for removing assets that are no longer needed or have been superseded.


-   **[Health tab in AI Control Tower](https://www.servicenow.com/docs/access?context=aict-health-tab&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Monitor and evaluate the effectiveness of offensive content and prompt injection guardrails active on your AI assets.


-   **[AI strategy with Strategic Planning](https://www.servicenow.com/docs/access?context=ai-strategy-aict&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)\(Requires SPM\)**
    -   Monitor and track your AI strategies and associated goals and targets.
    -   Track the costs of your AI projects, epics, and demands.
    -   Monitor key project risks, issues, decisions, actions, and changes.
-   **[AI strategy with Goal Framework](https://www.servicenow.com/docs/access?context=ai-strategy-aict&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US) \(Requires SPM\)**

    Monitor and track your AI strategies and associated goals and targets.

-   **[Enterprise AI discovery: Unlock Visibility, Governance &amp; Value](https://www.servicenow.com/docs/access?context=enterprise-ai-discovery&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**
    -   Discover and add AI agents and related models and tools to the AI inventory through integration with AWS Bedrock.
    -   Discover and add AI agents and related models and tools to the AI inventory through integration with Azure AI Foundry.
    -   Configure AI discovery setup and visibility of connections.
-   **[Value tab in AI Control Tower](https://www.servicenow.com/docs/access?context=aict-value-tab&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**
    -   Gain insights into the value realized from AI skills and features. The Value insights dashboard page gives you insights into the estimated productivity gains as a result of using AI systems.
    -   Define and measure value relevant to your AI systems using customizable value templates.
    -   Perform calculations and approximations for the read and write time saved by users using AI systems by using data points and timestamps from the invoking records.
    -   Understand the key usage and performance indicators that help you evaluate the adoption of Now Assist in your organization.
    -   Provide insights on success rate visualization by department, country, and AI assets along with the indicators for task closure efficiency.
-   **[Value templates](https://www.servicenow.com/docs/access?context=using-value-templates&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**
    -   Create, manage, and use templates from a Global Template Repository across multiple AI assets, so that you can standardize and streamline your AI experience, and track usage of AI systems, use cases, and skills more effectively.
    -   Enable users to edit, view, and create customized value templates by enabling a value template assignment experience in inventory records.
    -   Provide transparency to value calculations of each AI system through value templates.
    -   Perform calculations and approximations for the read and write time saved by users using AI systems by using data point and timestamps from the invoking records.
-   **[Risk and compliance tab](https://www.servicenow.com/docs/access?context=risk-and-complaince-tab&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

    Display the risk classification of AI assets and the compliance posture for selected authority documents and policies through the **Risk and compliance** tab. This tab provides visibility into AI systems, models, and datasets. The Risk overview section uses visual charts to categorize AI assets.

    Review adherence to frameworks in the Compliance overview section. For example, adherence to the NIST AI Risk Management Framework or the EU Artificial Intelligence Act, presenting scores based on citations and control attestations that are set by the customer. You can filter data by authority documents or policies, view overall compliance percentages, and identify critical issues and AI cases tied to items deemed non-compliant by the customer.

    -   Build trust in the AI asset inventory to effectively manage AI-related risks across the enterprise.
    -   Drive enterprise-wide risk visibility by aggregating individual scores into a consolidated AI risk profile to support informed mitigation decisions.
    -   Display real-time residual risk scores on the home page to help practitioners identify high-risk AI assets and prioritize mitigation actions.
    -   Use enhanced impact assessment templates to help manage and oversee compliance with regulatory requirements.
    -   Perform bulk control attestations using Core UI to validate multiple controls across AI assets, improving efficiency for large-scale assessments.
    -   Adopt a proactive approach by leveraging comprehensive AI risk and compliance scoring across the entire AI asset inventory.
-   **[AI cases tab in AI Control Tower](https://www.servicenow.com/docs/access?context=ai-cases-tab-aict&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Gain a centralized overview of all your AI asset cases and inquiries by using the AI cases. On the **AI cases** tab, you see a list of records that include the case details such as the status, priority, owner, and timeline of your AI cases. You can monitor the progression of a case, stay informed about ongoing investigations, follow up on pending actions, and help to ensure timely resolutions. On this tab, you can also find filtering and sorting options that help you to prioritize cases that require immediate attention.

    -   Use the enhanced home page to access a single, unified view of all AI-related cases and inquiries.
    -   Track, manage, and respond to AI-related cases more efficiently through centralized case visibility.
-   **[Security &amp; privacy tab in AI Control Tower](https://www.servicenow.com/docs/access?context=security-privacy-tab&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Review your AI security health metrics in the **Security and Privacy** tab. Use the access map for a comprehensive overview of agentic workflows, tools, and agent details. The map helps to show how AI agents interface with workflows and tools to accomplish a task. Additionally, you can analyze current AI access, investigate ongoing access issues, and review your AI usage metrics.

    Control which third-party models OEM by ServiceNow are enabled for Now Assist AI implementation and how they’re used.

-   **[Specify additional details during AI asset creation](https://www.servicenow.com/docs/access?context=creating-ai-assets&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

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


[Zurich Patch 7](../quality/zurich-patch-7.md)

-   **[Drop-down menu for associating AI assets with related assets](https://www.servicenow.com/docs/access?context=view-ai-assets-lifecycle-stage&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    In both the AI asset creation forms and AI asset records, the **Add new** button that previously enabled you to associate AI assets with other related assets has changed into an Add from inventory drop-down menu with the **Add from inventory** and **Create** options. The **Add from inventory** menu option enables you to associate AI assets with related assets that are currently available in your asset inventory. The **Create** menu option enables you to associate AI assets with related assets that are not currently available in your asset inventory.

-   **[Editable asset details fields on the Details tab of AI asset records](https://www.servicenow.com/docs/access?context=view-ai-assets-lifecycle-stage&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    You can now modify asset details fields directly on the **Details** tab of your AI asset records.

-   **[Related asset lists in AI asset records](https://www.servicenow.com/docs/access?context=view-ai-assets-lifecycle-stage&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    The lists of related assets in each AI asset record has moved from the **Related assets** tab to the **Details** tab.


-   **[Product Owner portal](https://www.servicenow.com/docs/access?context=product-owner-portal&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US#section_om4_mbg_xfc)**
    -   Widgets from both the **Value** and **Adoption** tabs are now combined and accessible within the updated **Value** tab.
    -   The **Create AI Asset** button is added on the AI Control Tower home page.
    -   A new Quick link option is added to the employee center to help navigate AI asset owners and AI stewards to the AI Control Tower workspace home page.

## Changed in this Zurich release

-   **[Security &amp; privacy tab in AI Control Tower](https://www.servicenow.com/docs/access?context=security-privacy-tab&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**
    -   The Autonomous vs. supervised AI tools chart has been removed.
    -   The Prompt injection, Offensive content, and Sensitive data tabs have been removed and replaced by Access and Guardrails tabs. Metrics have been reorganized into those two tabs.
    -   In **Configurations**, under **Data**, the **Data privacy** tab was renamed to **Security &amp; privacy**. In that tab, the data leak detection and anonymization section was renamed to sensitive data input and anonymization.

-   **[Changes to Now Assist usage measurement](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

    Starting with Zurich Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


-   **[Changes in Zurich Patch 4](../quality/zurich-patch-4.md)**
    -   The AI asset inventory plugin structure has been updated.
    -   Product owner view: Added a role called AI asset owner \[sn\_ai\_asset\_mgmt.ai\_asset\_owner\], which enables the Product Owner view experience with a personalized home page and enhanced visibility into AI assets to simplify task management.
    -   AI discovery: The Innovation lab store application \(AWS AI discovery plugin\) is decommissioned. Uninstall the AWS AI discovery plugin prior to installing the AI discovery plugin \(sn\_ai\_disc\).
    -   AI cases management has moved under the **AI cases** tab on the AI Control Tower home page.

## Activation information

Install AI Control Tower by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Accessibility information

-   **Dark theme**

    The new Coral theme includes a dark theme option for web and mobile experiences. This option is commonly used to alleviate eye strain and improve readability.


## Related ServiceNow applications and features

-   **[AI Risk and Compliance](https://www.servicenow.com/docs/access?context=ai-risk-and-compliance&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

    Enable risk and compliance managers to verify organizational compliance with regulations and policies governing AI systems by using the AI Risk and Compliance application, along with the AI Control Tower.

-   **[Strategic Planning](https://www.servicenow.com/docs/access?context=goal-management-in-alignment-planner-workspace&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)**

    Prioritize, roadmap, and track work when using traditional, agile, or hybrid methodologies with ServiceNow® Strategic Planning. Align strategy to execution by defining and tracking goals across your organization. When the Strategic Planning application is installed, the **AI strategy** tab appears in the AI Control Tower workspace, featuring different widgets for AI strategies, goals, targets, costs of planning items, prioritized work, and RIDAC details.

    Strategic Planning is available with an SPM Professional license.

-   **[Goal Framework](https://www.servicenow.com/docs/access?context=goal-framework&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)**

    Create goals, set targets for them, and evaluate the progress of the goals and targets to accomplish your organizational plans and drive business outcomes with the ServiceNow® Goal Framework application. When the Goal Framework application is installed, the **AI strategy** tab appears in the AI Control Tower workspace, featuring different widgets for AI strategies, goals, and targets.

    Goal Framework is available with an SPM Standard license.


**Parent Topic:**[AI Experiences release notes](intelligent-experiences-rn-landing.md)

**Parent Topic:**[Now Assist and agentic AI release notes](../now-assist/now-assist-rn-landing.md)


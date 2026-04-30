---
title: New features and products in Zurich
description: Cumulative release notes summary on new Zurich features and products.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2026-04-08"
reading_time_minutes: 426
breadcrumb: [Release notes summaries for Zurich features, Release notes for upgrading from Yokohama, Learn about the Zurich release, Zurich release notes]
---

# New features and products in Zurich

Cumulative release notes summary on new Zurich features and products.

New products were introduced in Zurich, and additional features were added to existing  products.

<table id="rn-summary-new-features-tables" class="custom-rows"><thead><tr><th class="filter">

Application or feature

</th><th>

Details

</th></tr></thead><tbody><tr><td>

AI Control Tower

</td><td>

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

</td></tr><tr><td>

AI Risk and Compliance

</td><td>

-   **[Assess multiple risks and controls for AI assets simultaneously](https://www.servicenow.com/docs/access?context=risk-assessment-project-airc&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

Create a risk assessment project to perform bulk assessments on multiple risks for an AI asset, enabling assessors to evaluate them in a single project. This approach reduces time and effort, confirms consistency across multiple assessments, and provides a more comprehensive view of risks and controls within the same project. You can scope multiple risks related to the assessable entity within the project and perform assessments.

AI Risk and Compliance team can determine inherent risks, control effectiveness, residual risks, and target risks in the risk assessment project. They can also reassess completed assessments or reassign in-progress assessment projects to another assessor.

-   **[AI asset data segregation with entity based access](https://www.servicenow.com/docs/access?context=entity-based-access-for-ai-assets&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

Enhance data segregation and security to ensure that only authorized users can access sensitive AI Risk and Compliance data while maintaining visibility into core entities. AI Risk and Compliance managers can control access risks, controls, related entities, issues, indicators, AI asset tasks, risk assessments, attestations, and AI assets data through entity-based access. Entities themselves stay visible to all users, while visibility of linked records is limited to authorized users.

-   **[AI Risk and Compliance content accelerator](https://www.servicenow.com/docs/access?context=unified-content-management-in-airc&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

Use the AI Risk and Compliance content accelerator icon on the AI Risk and Compliance workspace to activate the pre-configured content packs. Content Accelerator includes regulatory packs such as the EU Artificial Intelligence Act and NIST AI Risk Management Framework, offering citations, control objectives, and risk statements. The unified content hub helps to streamline scoping, reduce manual navigation between frameworks, and promote consistent use of regulatory content accelerator packs. This feature supports AI Risk and Compliance team in meeting relevant business requirements, maintaining team consistency, and speeding up the activation and management of global regulatory frameworks.

-   **[Automatic creation of AI cases and inquiries from an inbound email](https://www.servicenow.com/docs/access?context=automatic-creation-cases-inquiries-from-email&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

Report AI cases or raise AI inquiries by sending an email to a dedicated email address. Your email automatically creates a new AI Case or AI Inquiry record in the system. This feature remove manual work and scattered reporting methods, ensuring every case or inquiry is automatically captured, categorized, and tracked.

-   **[360° Relationship Visualization of an AI asset](https://www.servicenow.com/docs/access?context=visualization-of-ai-assest&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

Use the 360° AI asset view in the AI Control Tower to explore the relationship between your AI assets and all its associated records in a distinctive visualization. This visualization provides valuable insights into how these objects interact and relate to each other within the AI asset. You can view related records such as, datasets, AI model, risks, controls, and assessments.

-   **[AI asset offboarding workflow](https://www.servicenow.com/docs/access?context=airc-offboarding-ai-assets&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

Manage AI asset changes and retirements through structured workflows that ensure compliance and reduce operational risk. Track and approve modifications to models, datasets, and systems while automatically identifying impacts on dependent assets. Initiate formal offboarding processes that remove access, close documentation, and update related controls when retiring underperforming or deprecated AI assets. Maintain complete audit trails integrated with your policy and risk frameworks to demonstrate governance continuity during lifecycle transitions.

-   **[Deliver system-level AI risk score aggregation and visualization](https://www.servicenow.com/docs/access?context=ai-assets-airc&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

Aggregate AI system-level risk scores by integrating heatmaps and residual risk score widgets directly within your AI asset overview records. These visual tools help you to see the cumulative risk exposure and track the residual risks across the entire AI asset inventory. With this feature, you get clear, data-driven insights into the overall AI system risk posture.

-   **[Enable AI risk and compliance views with updated content packs](https://www.servicenow.com/docs/access?context=ai-assets-airc&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

Get the dedicated AI risk and compliance views for your AI models and dataset records. With these views, you get a structured and comprehensive overview of the related risks, controls, and compliance obligations, including the refreshed content packs that feature the updated assessment questionnaires and templates that align with the latest governance frameworks and regulatory standards. Your organization can perform accurate and timely risk assessments while maintaining compliance with evolving AI governance requirements.

-   **[Implement robust access control and AI asset management capabilities](https://www.servicenow.com/docs/access?context=roles-installed-with-ai-risk-and-compliance&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

Apply role-based access controls across AI assets and dashboards to ensure that data access is based on user roles. You can enable employees to request access to AI assets through a governed process and enforce consistent tracking of life-cycle states \(such as development, deployment, monitoring, and retirement\) across all AI assets.

-   **[Use the AI cases tab to monitor and manage AI case activity](https://www.servicenow.com/docs/access?context=ai-cases-tab-airc&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

Gain a centralized overview of all your AI asset cases and inquiries by using the **AI cases** tab in the AI Risk and Compliance workspace. On this tab, you see a list of records that include the case details such as the status, priority, owner, and timeline of your AI cases. You can monitor the progression of a case, stay informed about ongoing investigations, follow up on pending actions, and ensure timely resolutions. On the tab, you can also find filtering and sorting options that help you to prioritize cases that require immediate attention.

-   **[Filter the risk heatmap by Risk Assessment Methodology for targeted risk analysis](https://www.servicenow.com/docs/access?context=risk-and-compliance-tab-airc&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

Apply the Risk Assessment Methodology filter to customize the display of the risk heatmap that is based on the specific risk evaluation frameworks from the AI risk and compliance home page. You can segment and analyze the AI risks according to the risk assessment models that your organization adopts, such as the internal standards, regulatory frameworks, or industry benchmarks, so that you can understand how different risk factors are identified, scored, and distributed.

-   **[Group control attestations](https://www.servicenow.com/docs/access?context=attest-controls-for-ai-systems&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

Group control attestations by such predefined criteria as the control objectives, frameworks, or assessment cycles so that you can more efficiently manage and review attestations, reduce redundancy, and improve your visibility into the compliance status across related controls for the AI Risk and Compliance team.

-   **[Scan and analyze updates from global regulators](https://www.servicenow.com/docs/access?context=ai-risk-and-compliance-workspace&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

Enable the AI Risk and Compliance team to scan and interpret regulatory updates that are issued by global authorities. Your organization can stay informed about emerging compliance requirements, assess their potential impact, and take timely action.

-   **[Manage reporting compliance posture insights on key regulations or policies](https://www.servicenow.com/docs/access?context=risk-and-compliance-tab-airc&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

Control the reporting of compliance posture insights that are related to key regulations and internal policies by using a setting to determine which insights are shared, their level of detail, and the reporting cadence. Your organization can align reporting outputs with regulatory obligations and internal governance requirements.


</td></tr><tr><td>

AI Search

</td><td>

-   **[Improve search precision and contextual relevance with hybrid search](https://www.servicenow.com/docs/access?context=hybrid-search-ais&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

Beginning with Now Assist in AI Search 15.0, customers with Now Assist in AI Search installed can enable the new hybrid search mode. Hybrid search combines keyword-based search with semantic understanding to deliver more accurate and relevant search results, with fewer zero-result searches.


-   **[Improve semantic search with third-party embedding models](https://www.servicenow.com/docs/access?context=ais-rag&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

Use custom and third-party embedding models supported by the AI Search RAG application to generate more accurate and relevant semantic search results.


-   **[Filter external content search results by language](https://www.servicenow.com/docs/access?context=language-filtering-external-content&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

AI Search filters external content search results, displaying only results that contain content in languages relevant for the user's search. These languages include:

    -   The search user's session language
    -   The fallback language for the user's session language \(if configured\)
    -   The language of the global fallback locale \(if configured\)
-   **[Indexing support for variables in records on Catalog Item and child tables](https://www.servicenow.com/docs/access?context=variable-types-ais-index&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

Index searchable content from Multiple Choice and Select Box variables in records on the Catalog Item table and tables that extend it.

-   **[New display properties for Search Result EVAM cards](https://www.servicenow.com/docs/access?context=search-result-evam-card-opts&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

Search Result EVAM cards include new **customIcon**, **customIconSize**, **forceNewTab**, and **useAttachmentViewer** properties that you can use to modify display settings and behavior for search results.


</td></tr><tr><td>

AIOps LEAP

</td><td>

-   **[New third-party AI model provider options available for all Now Assist applications](https://www.servicenow.com/docs/access?context=exploring-large-language-models&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Google Gemini and AWS Claude are available for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.


</td></tr><tr><td>

API

</td><td>

<table id="table_tcd_5v3_wqb"><thead><tr><th>

Class

</th><th>

Methods

</th></tr></thead><tbody><tr><td>

[GlideCurrencyCode - Scoped, Global](https://www.servicenow.com/docs/access?context=GlideCurrencyCodeBothAPI&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)

</td><td>

-   getCurrencyCode\(\)
-   getNumericCurrencyCode\(\)

</td></tr><tr><td>

[GlideCurrencySymbol - Scoped, Global](https://www.servicenow.com/docs/access?context=GlideCurrencySymbolBothAPI&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)

</td><td>

-   getCurrencySymbol\(\)
-   getSortedActiveCurrencySymbols\(\)

</td></tr><tr><td>

[GlideQueryCondition - Scoped](https://www.servicenow.com/docs/access?context=c_GlideQueryConditionScopedAPI&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)

</td><td>

-   addSystemCondition
-   addSystemOrCondition
-   addUserCondition
-   addUserOrCondition

</td></tr><tr><td>

[GlideRecord - Scoped](https://www.servicenow.com/docs/access?context=c_GlideRecordScopedAPI&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)

</td><td>

-   addSystemEncodedQuery\(\)
-   addSystemQuery\(\)
-   addSystemOrderBy\(\)
-   addSystemOrderByDesc\(\)
-   addUserEncodedQuery\(\)
-   addUserQuery\(\)
-   addUserOrderBy\(\)
-   addUserOrderByDesc\(\)

</td></tr><tr><td>

[GlideSysAttachment - Scoped](https://www.servicenow.com/docs/access?context=c_GlideSysAttachmentScopedAPI&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)

</td><td>

-   addAttribute\(\)
-   addMultipleAttributes\(\)
-   deleteAllAttributes\(\)
-   deleteAttribute\(\)
-   fetchAllAttributes\(\)
-   fetchAttribute\(\)
-   updateAllAttributes\(\)
-   updateAttribute\(\)

</td></tr><tr><td>

[GlideSystem - Scoped](https://www.servicenow.com/docs/access?context=c_GlideSystemScopedAPI&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)

</td><td>

Added support for additional message types to display at the top of forms:-   addHighMessage\(\)
-   addLowMessage\(\)
-   addSuccessMessage\(\)
-   addModerateMessage\(\)

</td></tr></tbody>
</table><table id="table_ldq_g3c_tcc"><thead><tr><th>

Class

</th><th>

Methods

</th></tr></thead><tbody><tr><td>

[GlideDynamicAttribute - Global](https://www.servicenow.com/docs/access?context=GlideDynamicAttributeAPI&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)

</td><td>

Updated content to remove support for dynamic attribute groups.New method getNamespaceName\(\).

</td></tr><tr><td>

[GlideDynamicAttributeStore - Global](https://www.servicenow.com/docs/access?context=GlideDynamicAttStoreAPI&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)

</td><td>

Updated content to remove support for dynamic attribute groups.New methods:

-   getDynamicNamespace\(\)
-   setDynamicNamespace\(\)

</td></tr><tr><td>

[GlideDynamicNamespace - Global](https://www.servicenow.com/docs/access?context=GlideDynamicNamespaceAPI&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)

</td><td>

-   getName\(\)
-   isActive\(\)
-   isTransient\(\)

</td></tr><tr><td>

[GlideQueryCondition - Global](https://www.servicenow.com/docs/access?context=c_GlideQueryConditionAPI&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)

</td><td>

-   addSystemCondition
-   addSystemOrCondition
-   addUserCondition
-   addUserOrCondition

</td></tr><tr><td>

[GlideRecord - Global](https://www.servicenow.com/docs/access?context=c_GlideRecordAPI&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)

</td><td>

-   addSystemEncodedQuery\(\)
-   addSystemQuery\(\)
-   addSystemOrderBy\(\)
-   addSystemOrderByDesc\(\)
-   addUserEncodedQuery\(\)
-   addUserQuery\(\)
-   addUserOrderBy\(\)
-   addUserOrderByDesc\(\)

</td></tr><tr><td>

[GlideSysAttachment - Global](https://www.servicenow.com/docs/access?context=GlideSysAttachmentGlobalAPI&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)

</td><td>

-   addAttribute\(\)
-   addMultipleAttributes\(\)
-   deleteAllAttributes\(\)
-   deleteAttribute\(\)
-   fetchAllAttributes\(\)
-   fetchAttribute\(\)
-   updateAllAttributes\(\)
-   updateAttribute\(\)

</td></tr><tr><td>

[GlideSystem - Global](https://www.servicenow.com/docs/access?context=c_GlideSystemAPI&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)

</td><td>

Added support for additional message types to display at the top of forms:-   addHighMessage\(\)
-   addLowMessage\(\)
-   addModerateMessage\(\)
-   addSuccessMessage\(\)

</td></tr><tr><td>

[Message - Global](https://www.servicenow.com/docs/access?context=sn_i18n.messageAPI&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)

</td><td>

Retrieves localized messages from the Message \[sys\_ui\_message\] table. It supports internationalization \(i18n\) by dynamically fetching messages based on the user's session language or a specified language parameter.-   getMessage\(\)
-   getMessageLang\(\)

</td></tr></tbody>
</table><table id="table_nds_wxf_gfc"><thead><tr><th>

Class

</th><th>

Methods

</th></tr></thead><tbody><tr><td>

[GlideForm \(g\_form\) - Client](https://www.servicenow.com/docs/access?context=c_GlideFormAPI&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)

</td><td>

-   addChoice\(\)
-   addHighMessage\(\)
-   addLowMessage\(\)
-   addModerateMessage\(\)
-   addSuccessMessage\(\)
-   clearChoices\(\)
-   disableChoice\(\)
-   enableChoice\(\)
-   getAnnotationByName\(\)
-   getAnnotations\(\)
-   getChoice\(\)
-   getOptions\(\)
-   hideAnnotation\(\)
-   hideRelatedLinks\(\)
-   hideTemplateBar\(\)
-   removeChoice\(\)
-   setChoiceLabel\(\)
-   setRelatedLinksDisplay\(\)
-   showAnnotation\(\)
-   showRelatedLinks\(\)
-   showTemplateBar\(\)
-   toggleAnnotations\(\)

</td></tr><tr><td>

[GlideModal \(Next Experience\) - Client](https://www.servicenow.com/docs/access?context=GModClientAPINX&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)

</td><td>

-   destroy\(\)
-   get\(\)
-   getID\(\)
-   getPreference\(\)
-   getPreferences\(\)
-   renderWithContent\(Object\)
-   renderWithContent\(String\)
-   setDialog\(\)
-   setPreference\(\)
-   setTitle\(\)
-   type\(\)

</td></tr><tr><td>

[GlideNavigation \(Next Experience\) - Client](https://www.servicenow.com/docs/access?context=GlideNavigationClientAPINX&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)

</td><td>

refreshNavigator\(\)

</td></tr><tr><td>

[StopWatch \(Next Experience\) - Client](https://www.servicenow.com/docs/access?context=StopWatchAPINX&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)

</td><td>

-   StopWatch\(\)
-   getTime\(\)
-   restart\(\)
-   toString\(\)

</td></tr><tr><td>

[GlideForm \(Next Experience\) - Client](https://www.servicenow.com/docs/access?context=GlideFormAPINX&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)

</td><td>

-   addChoice\(\)
-   addHighMessage\(\)
-   addLowMessage\(\)
-   addModerateMessage\(\)
-   addSuccessMessage\(\)
-   clearChoices\(\)
-   disableChoice\(\)
-   enableChoice\(\)
-   getAnnotationByName\(\)
-   getAnnotations\(\)
-   getChoice\(\)
-   getOptions\(\)
-   hideAnnotation\(\)
-   removeChoice\(\)
-   setChoiceLabel\(\)
-   showAnnotation\(\)
-   toggleAnnotations\(\)

</td></tr><tr><td>

[GlideUser \(Next Experience\) - Client](https://www.servicenow.com/docs/access?context=GlideUserAPINX&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)

</td><td>

getRoles\(\)

</td></tr></tbody>
</table><table id="table_gmt_y3c_tcc"><thead><tr><th>

API

</th><th>

Endpoints

</th></tr></thead><tbody><tr><td>

[Conversation Member API](https://www.servicenow.com/docs/access?context=conversation-member-api&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)

</td><td>

-   PUT now/conversation/member/\{user\_id\}/drop
-   PUT now/conversation/member/\{user\_id\}/update

</td></tr><tr><td>

[Omnichannel Callback API](https://www.servicenow.com/docs/access?context=omichannel-callback-api&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)

</td><td>

-   POST /api/sn\_omni\_callback/callback/attempt
-   POST /api/sn\_omni\_callback/callback/create
-   PATCH /api/sn\_omni\_callback/callback/update

</td></tr><tr><td>

[CSM Pricing API](https://www.servicenow.com/docs/access?context=csm-pricing-api&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)

</td><td>

-   POST /api/sn\_csm\_pricing/pricingengine/computePrice
-   DELETE /api/sn\_csm\_pricing/pricingengine/pricing\_context/\{pricing\_context\_id\}

</td></tr></tbody>
</table><table id="table_qlh_nlc_tcc"><thead><tr><th>

Application

</th><th>

App Version

</th><th>

Release month

</th><th>

API

</th><th>

Endpoints

</th></tr></thead><tbody><tr><td>

Omnichannel Callback

</td><td>

2.0.4

</td><td>

2026-02

</td><td>

[Omnichannel Callback API](https://www.servicenow.com/docs/access?context=omichannel-callback-api&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)

</td><td>

Added new endpoints, /get and /close, for retrieving and closing a given callback record. The third endpoint, /actions, allows you to perform create, update, close, and cancel operations for a callback in an external, third-party system with routing capabilities.

-   PATCH api/sn\_omichannel\_callback/get
-   POST api/sn\_omni\_callback/actions
-   POST api/sn\_omni\_callback/callback/close

</td></tr><tr><td>

Contact Center Integration Core

</td><td>

1.5.0

</td><td>

2026-01

</td><td>

[External ID Mapping API](https://www.servicenow.com/docs/access?context=external-id-mapping-api&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)

</td><td>

-   GET /sn\_ct\_ctr\_it\_core/external\_id\_mapping/table/\{tableName\}/documentId/\{documentId\}
-   PUT /sn\_ct\_ctr\_it\_core/external\_id\_mapping/table/\{tableName\}/documentId/\{documentId\}

</td></tr><tr><td>

Digital Product Release

</td><td>

2.3.0

</td><td>

2025-12

</td><td>

[Digital Product Release API](https://www.servicenow.com/docs/access?context=digital-product-release-api&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)

</td><td>

-   GET /sn\_dpr/digital\_product\_release/bundle/\{sysId\}
-   GET /sn\_dpr/digital\_product\_release/releases/\{releaseId\}/policies/status
-   POST /sn\_dpr/digital\_product\_release/product\_enhancement
-   POST /sn\_dpr/digital\_product\_release/release
-   POST /sn\_dpr/digital\_product\_release/release/\{releaseId\}/key\_date
-   POST /sn\_dpr/digital\_product\_release/release/\{releaseId\}/policies/run
-   POST /sn\_dpr/digital\_product\_release/release/\{releaseId\}/related\_task
-   POST /sn\_dpr/digital\_product\_release/release\_calendar
-   POST /sn\_dpr/digital\_product\_release/release\_id/\{releaseId\}/complete\_phase
-   POST /sn\_dpr/digital\_product\_release/release\_target
-   PUT /sn\_dpr/digital\_product\_release/release/\{sysId\}/retarget

</td></tr><tr><td>

Threat Intelligence Security Center for Security Operations

</td><td>

3.14.4

</td><td>

2025-12

</td><td>

[TISC TAXII Server API](https://www.servicenow.com/docs/access?context=taxii-server-api&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)

</td><td>

-   GET /sn\_sec\_tisc/taxii\_server/taxii2
-   GET /sn\_sec\_tisc/taxii\_server/\{api\_root\}
-   GET /sn\_sec\_tisc/taxii\_server/\{api\_root\}/collections
-   GET /sn\_sec\_tisc/taxii\_server/\{api\_root\}/collections/\{id\}
-   GET /sn\_sec\_tisc/taxii\_server/\{api\_root\}/collections/\{id\}/manifest
-   GET /sn\_sec\_tisc/taxii\_server/\{api\_root\}/collections/\{id\}/objects
-   GET /sn\_sec\_tisc/taxii\_server/\{api\_root\}/collections/\{id\}/objects/\{object\_id\}
-   GET /sn\_sec\_tisc/taxii\_server/\{api\_root\}/collections/\{id\}/objects/\{object\_id\}/versions

</td></tr><tr><td>

Telecommunication Open APIs

</td><td>

6.0.9

</td><td>

2025-12

</td><td>

[Party Management Open API](https://www.servicenow.com/docs/access?context=tmf-party-management-open-api&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)

</td><td>

New API for managing parties with a relationship to the enterprise. Supports the following methods:

-   DELETE /api/sn\_tmf\_api/v1/party/individual/\{id\}
-   GET /api/sn\_tmf\_api/v1/party/individual/\{id\}
-   GET /api/sn\_tmf\_api/v1/party/individual
-   GET/api/ sn\_tmf\_api/v1/party/organization/\{id\}
-   GET /api/sn\_tmf\_api/v1/party/organization
-   PATCH/api/sn\_tmf\_api/v1/party/individual/\{id\}
-   PATCH /api/sn\_tmf\_api/v1/party/organization/\{id\}
-   POST /api/sn\_tmf\_api/v1/party/individual
-   POST /api/sn\_tmf\_api/v1/party/organization

</td></tr><tr><td>

Telecommunication Open APIs

</td><td>

6.0.9

</td><td>

2025-12

</td><td>

[Product Inventory Open API](https://www.servicenow.com/docs/access?context=product-inventory-open-api&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)

</td><td>

-   DELETE /sn\_prd\_invt/order/product/\{id\}
-   PATCH /sn\_prd\_invt/order/product/\{id\}

</td></tr><tr><td>

Telecommunication Open APIs

</td><td>

6.0.9

</td><td>

2025-12

</td><td>

[Service Catalog Open API](https://www.servicenow.com/docs/access?context=service-catalog-open-api&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)

</td><td>

Supports new methods for service offerings and service candidate entity:-   DELETE /api/sn\_tmf\_api/catalogmanagement/serviceCategory/\{id\}
-   GET /api/sn\_tmf\_api/catalogmanagement/serviceCategory
-   GET /api/sn\_tmf\_api/catalogmanagement/serviceCategory/\{id\}
-   PATCH /api/sn\_tmf\_api/catalogmanagement/serviceCategory/\{id\}
-   POST /api/sn\_tmf\_api/catalogmanagement/serviceCategory

</td></tr><tr><td>

Threat Intelligence Security Center for Security Operations

</td><td>

3.14.4

</td><td>

2025-12

</td><td>

[TISC Intel Exchange API](https://www.servicenow.com/docs/access?context=tisc-intel-ex-api&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)

</td><td>

POST /sn\_sec\_tisc/tisc\_intel\_sharing\_api/post\_intel

</td></tr><tr><td>

Threat Intelligence Security Center for Security Operations

</td><td>

3.14.4

</td><td>

2025-12

</td><td>

[TISC RPZ API](https://www.servicenow.com/docs/access?context=tisc-rpz-api&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)

</td><td>

POST /sn\_sec\_tisc/rpz\_export

</td></tr><tr><td>

Network Inventory Advanced

</td><td>

10.0

</td><td>

2025-08

</td><td>

[DCIM Metric Data Feed API](https://www.servicenow.com/docs/access?context=dcim-metric-data-feed-api&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)

</td><td>

POST /api/sn\_ni\_adv/dcim/feed/\{vendorname\}

</td></tr><tr><td>

Omnichannel Callback

</td><td>

2.0.2

</td><td>

2025-08

</td><td>

[Omnichannel Callback API](https://www.servicenow.com/docs/access?context=omichannel-callback-api&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)

</td><td>

-   POST /api/sn\_omni\_callback/callback/attempt
-   POST /api/sn\_omni\_callback/callback/create
-   PATCH /api/sn\_omni\_callback/callback/update

</td></tr><tr><td>

Quote Management

</td><td>

6.0.1

</td><td>

2025-08

</td><td>

[Quote Management API](https://www.servicenow.com/docs/access?context=quote-management-api&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)

</td><td>

-   DELETE /sn\_tmf\_api/quote\_management\_api/quote/\{id\}
-   GET /sn\_tmf\_api/quote\_management\_api/quote
-   GET /sn\_tmf\_api/quote\_management\_api/quote/\{id\}
-   PATCH /sn\_tmf\_api/quote\_management\_api/quote/\{id\}
-   POST /sn\_tmf\_api/quote\_management\_api/quote

</td></tr><tr><td>

Telecommunication Open APIs

</td><td>

4.1.1

</td><td>

2025-08

</td><td>

[Work Order Management API](https://www.servicenow.com/docs/access?context=work-order-mgmt-api&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)

</td><td>

-   CANCEL /sn\_tmf\_api/work\_order\_management\_api/cancelWorkOrder
-   GET /sn\_tmf\_api/work\_order\_management\_api/workordermanagement
-   GET /sn\_tmf\_api/work\_order\_management\_api/workorder/\{id\}
-   PATCH /sn\_tmf\_api/work\_order\_management\_api/workOrder/\{id\}
-   POST /sn\_tmf\_api/work\_order\_management\_api/workOrder

</td></tr></tbody>
</table>

</td></tr><tr><td>

Access Management

</td><td>

-   **[Machine identity access controls](https://www.servicenow.com/docs/access?context=machine-identity-access-controls&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)**

Enforce fine-grained access to data via REST or SOAP endpoints using Machine Identity Access Controls. This feature enables you to define which integrations can access specific data, confirming that the integrations only have access to the resources they need.

-   **[Scripting Governance Tool](https://www.servicenow.com/docs/access?context=scripting-governance&version=zurich&pubname=zurich-platform-security&ft:locale=en-US) tool and role**

Review and help reduce the number of users with scripting privileges using the Scripting Governance Tool. This tool helps improve platform security with scripting governance based on user role.

A new deny-by-default behavior is enforced for scripting unless you have the snc\_required\_script\_writer\_permission role. After an upgrade or zBoot, this role is automatically assigned via the Conditional Script Writer group.

-   **[Datatype ACL](https://www.servicenow.com/docs/access?context=datatype-acl&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)**

Simplify and help reduce redundant ACL definitions with Datatype ACLs. Create a single ACL to target all table columns of a specific data type, streamlining access control configurations.


</td></tr><tr><td>

Accounts Payable Operations

</td><td>

-   **[Tax Engine Integration](https://www.servicenow.com/docs/access?context=tax-engine-integration&version=zurich&pubname=zurich-source-to-pay-operations&ft:locale=en-US)**

The tax engine integration framework validates supplier-provided tax against system tax at invoice line level, maintains compliance with regional and global tax regulations. This integration triggers automatic tax validation, handles exceptions for tax variance and missing data, enables manual revalidation and rolling up of system tax.


-   **[Convert invoice type](https://www.servicenow.com/docs/access?context=convert-invoice-case&version=zurich&pubname=zurich-source-to-pay-operations&ft:locale=en-US)**

Enable your accounts payable specialist to manually change the invoice type, which results in improved accuracy and compliance. For example, changing a non-purchase order \(PO\) invoice to a PO invoice type.

-   **[Using Playbook in Accounts Payable Operations](https://www.servicenow.com/docs/access?context=how-to-use-playbook&version=zurich&pubname=zurich-source-to-pay-operations&ft:locale=en-US)**

Process your invoices more efficiently, adhere to compliance, and provide financial accuracy across processes by using new exceptions such as the Missing tax code invoice and currency mismatch between invoices and purchase orders.

-   **[IT Asset Management purchase order invoice processing](https://www.servicenow.com/docs/access?context=apo-integration-with-itam&version=zurich&pubname=zurich-source-to-pay-operations&ft:locale=en-US)**

Confirm that ITAM receipts are available and the received quantity is updated in the purchase orders through the integration between the IT Asset Management and Accounts Payable Operations applications.

-   **[Set APO properties](https://www.servicenow.com/docs/access?context=set-apo-properties&version=zurich&pubname=zurich-source-to-pay-operations&ft:locale=en-US)**

The recommend invoice owner AI agent auto-suggests and fills in the appropriate business owner based on historical patterns. This process sets up auto-confirmation from suppliers, resulting in shorter invoice processing cycles.


-   **[Universal Request in Accounts Payable Operations](https://www.servicenow.com/docs/access?context=universal-request-in-apo&version=zurich&pubname=zurich-source-to-pay-operations&ft:locale=en-US)**

Employees and suppliers can raise general case requests and track case activity updates from their respective portals by using the ServiceNowUniversal Request \(UR\) application. Universal requests eliminate confusion about which department to contact for assistance.


-   **[Distribution set in Accounts Payable Operations](https://www.servicenow.com/docs/access?context=distribution-sets-in-apo&version=zurich&pubname=zurich-source-to-pay-operations&ft:locale=en-US)**

Apply predefined distribution sets to split invoice amounts across multiple cost centers or GL accounts without having to do manual entry for each invoice line in PO invoices and non-PO invoices. This process helps distribute costs to multiple cost centers automatically, reducing manual work for Accounts Payable specialists.


</td></tr><tr><td>

Adoption Services

</td><td>

-   **[Help Center](https://www.servicenow.com/docs/access?context=help-center&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US)**

Find the available Guided Tours that are now prominently listed in the Help Center.

View the state of the Guided Tours in progress, in the Help Center. Any other help content is hidden when the tour is running. These enhancements are applicable across workspaces.


</td></tr><tr><td>

Advanced AI Search Management Tools

</td><td>

-   **[AI Search analytics dashboard](https://www.servicenow.com/docs/access?context=ai-search-analytics-dashboard&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

The **Search application** interactive filter now allows analysts to review performance metrics and trends for search applications used in Recommended Actions.


-   **[AI Search analytics dashboard](https://www.servicenow.com/docs/access?context=ai-search-analytics-dashboard&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

The **Search application** interactive filter now allows analysts to review performance metrics and trends for the Mobile Platform search application.


</td></tr><tr><td>

Advanced Risk

</td><td>

-   **[Identify risks for an entity](https://www.servicenow.com/docs/access?context=suggest-potential-risks-workflow&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

If you’re a Workspace user with the sn\_grc\_sharegenai.risk\_suggestion\_aiagent\_user role, you can use the Risk Suggestion AI Agent to identify risks related to an entity. The AI agent analyzes the entity and suggests relevant risks from various sources, consolidating them into a reviewable list to verify for accuracy. Risk managers can then confirm and promote these risks to the risk register for further assessment. This feature automates risk discovery, helping identify potential risks and prepare for compliance requirements.

-   **[Reporting views from Risk Assessment Methodology](https://www.servicenow.com/docs/access?context=reporting-views-from-ram&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

The reporting view provides an overview of all assessments under a specific Risk Assessment Methodology \(RAM\). It consolidates assessment data such as factor responses, scores, issues, controls, and associated risks into a single structure. When a RAM is published, the system automatically creates this view, which you can use to review assessments and build custom reports. It simplifies report and dashboard creation for risk assessments.

**Note:** Automatic creation of Reporting views is not supported on Xanadu. For instructions on creating them manually, refer to [KB2547071](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2547071)

-   **[Risk event summarization](https://www.servicenow.com/docs/access?context=generate-risk-event-summary-in-the-risk-workspace&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

Generate risk event summary using the Now Assist for IRM application. Risk event summarisation is a Generative AI driven capability that generates clear and consistent summaries automatically. It reduces the need for manual effort, helps risk managers save time, and enables approvers to quickly understand the key details for faster decisions. Check your entitlements to confirm whether you have access to risk event summarization.

-   **[Grid based risk and control assessment](https://www.servicenow.com/docs/access?context=perform-assessment-risk-assessment-project-grid-view&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

Gain efficient control over risk assessments with the new grid-based Risk and Control Self Assessment \(RCSA\). Quickly compare, edit, and prioritize risks and controls using the flexible, spreadsheet-style interface. Use side-by-side views and bulk editing to complete assessments faster.

-   **[Matrix report in Risk Workspace](https://www.servicenow.com/docs/access?context=matrix-report-in-risk-workspace&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

Access and analyze the risk posture of your organization using entity-related data, such as risks, controls, KRIs, and events in a centralized, configurable grid-based view. This feature reduces time spent switching views and helps risk managers assess data more easily, leading to more proactive and streamlined risk management.

-   **[Support third party large language models](https://www.servicenow.com/docs/access?context=generate-risk-assessment-summary-genai&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

Risk assessment summarization and Risk event summarization support the LLMs from the third party providers, such as Anthropic Claude, Google Gemini, and OpenAI, in addition to Now LLM. This enhancement gives you greater flexibility to choose the model that best fits your organization’s needs for generating risk assessment and risk event summaries.


</td></tr><tr><td>

Advanced Work Assignment \(AWA\)

</td><td>

-   **[Use AWA without existing interaction or work item](https://www.servicenow.com/docs/access?context=using-awa&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)**

Use AWA with an inbox card in Workspace without an existing interaction or work item.

-   **[New interaction record field](https://www.servicenow.com/docs/access?context=reference-awa&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)**

A new interaction record field was added to indicate whether this interaction is related to a third-party provider.


</td></tr><tr><td>

Agent Chat

</td><td>

-   **[Third-party chat integrations](https://www.servicenow.com/docs/access?context=ci-agent-chat-using&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)**

Use the new customer message area for third-party chat integrations to see these features:

    -   Third-party chat providers can update messages in real time.
    -   Individual messages from third-party bots are correctly attributed to the appropriate customer and agent.
    -   Agent and queue transfers to third-party chat systems are supported.
    -   Show or hide capabilities for specific Contact Center as a Service \(CCaaS\) chat integration requirements can be configured.

</td></tr><tr><td>

Agent Client Collector

</td><td>

**Agent Client Collector Framework**

-   **Upgrade MID-less agents**

Starting in version 6.0.0, perform selective and high-volume upgrades on ACC agents when not using a MID Server by using products such as DEX and ACC-VC.

-   ****

Starting in version 6.0.0, verify that an agent is functioning properly by performing a self-test on the agent.

-   ****

Starting in version 6.0.0, view a list of agents and their statuses on the ACC Workspace dashboard.

-   **Use improved debug logging**

Starting in version 6.0.0, benefit from enhanced debug logging by sending all debug statements to a log file

-   **[Manage Agent Client Collector certificates](https://www.servicenow.com/docs/access?context=acc-yml-options&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

Starting in version 5.0, configure a schedule by which to rotate Agent Client Collector certificates which enable communication between agents and ITOM Cloud Services. Rotating certificates ensures that when a certificate expires, a new certificate is in place.

-   **[Perform high-volume Agent Client Collector upgrade in a macOS environment](https://www.servicenow.com/docs/access?context=acc-high-volume-upgrade&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

Starting in version 5.0, upgrade large numbers of Agent Client Collector agents at a time that are running on macOS. This extends the existing high-volume upgrade capabilities available for Windows and Linux in the 4.3.0 release.

-   **[Use an IMDSv2 endpoint for metadata discovery](https://www.servicenow.com/docs/access?context=acc-configure-websocket-endpoint&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

Starting in version 5.0, the IMDSv2 endpoint for metadata discovery is invoked when using Agent Client Collector in an AWS EC2 environment.

-   **[Use enhanced errors and diagnostics to troubleshoot issues with servers and endpoints](https://www.servicenow.com/docs/access?context=view-agent-errors&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

Starting in version 5.0, view errors that occur before or after the registration process when Agent Client Collector connects to the instance. This provides enhanced debugging capabilities by enabling you to view issues in the instance, without requiring direct access to the agent logs.

-   **[Disable checks using heavy system resources while in CPU protection mode](https://www.servicenow.com/docs/access?context=checks-policies&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

Starting in version 5.0, disable only those checks that are causing high CPU usage while in CPU protection mode. It is still possible to disable all checks and completely stop data collection while in CPU protection mode.

In a Windows environment, Agent Client Collector has improved the accuracy of how check CPU usage is monitored.

-   **[Configuration data files size limit](https://www.servicenow.com/docs/access?context=acc-config-data-files&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

Starting in version 5.0, configuration data files have a maximum size of 10MB.

-   **[Configure Agent Client Collector with proxy auto-configuration \(PAC\) files](https://www.servicenow.com/docs/access?context=proxy-agent&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

Starting in version 5.0, enable easier connection of Agent Client Collector to a proxy server by using a proxy auto-configuration \(PAC\) file.


**Agent Client Collector Monitoring**

-   ****

Starting in version 3.15.0, GCP checks provide added support to configure metrics through a configuration file in JSON format.


-   **Monitor Linux events**

Starting in version 3.15.0, monitor Linux events using Linux event checks.


**Agent Client Collector for Visibility - Content**

-   **Discover MSSQL components using ACC-VC**

Starting in version 1.5.0, use ACC-VC to discover MSSQL components in your environment.

-   **Discover software information with ACC-VC using SWID tags**

Starting in version 1.5.0, gather software information with ACC-VC using software identification \(SWID\) tags on an agent and a ServiceNow® instance.

-   **[Run certificate Discovery using Agent Client Collector for Visibility - Content](https://www.servicenow.com/docs/access?context=run-cert-discovery-accvc&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

Starting in version 1.3.0, use the Agent Client Collector for Visibility - Content to discover TLS/SSL certificates used by the ports running on the server's configuration items \(CIs\). Certificate Inventory and Management uses the certificate data to manage the TLS/SSL certificate life cycle.

-   **[File-based Discovery is supported in a macOS environment](https://www.servicenow.com/docs/access?context=file-based-discovery&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

Starting in version 1.3.0, use File-based Discovery in a macOS environment.

-   **[Collect metrics using non-osqueryd data collection](https://www.servicenow.com/docs/access?context=using-enhanced-discovery-and-sam-together&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

Starting in version 1.3.0, collect data more efficiently by invoking non-osqueryd data collection.


</td></tr><tr><td>

Agent experience for CSM

</td><td>

-   **[CSM centered chat interaction record page](https://www.servicenow.com/docs/access?context=csm-centered-chat-interaction-page&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

Includes a chat component in the center of the record page that provides front-line chat agents with a modernized interaction page layout.

-   **[Callback component on the CSM voice interaction record page](https://www.servicenow.com/docs/access?context=csm-native-voice-record-page&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US#section_vtg_dzk_vfc)**

Provides agents with the ability to return customer calls and to create interaction records at the time of callback.

-   **[Task SLA cards component](https://www.servicenow.com/docs/access?context=csm-record-page-sla-card-component&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

Use the Task SLA cards component as a standalone component on the Front-line case page. Visual updates to the Task SLA cards component enable agents to see where they are in the lifecycle of multiple task SLAs at a glance.

-   **[Task activity timeline preset and controller](https://www.servicenow.com/docs/access?context=csm-record-page-timeline-component&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

Use the Task activity timeline preset and controller to add the Timeline component as a standalone component on task record pages such as case or incident.

-   **[Notifications for agent mentions in records](https://www.servicenow.com/docs/access?context=notifications-for-agent-mentions-in-records&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

Receive workspace notifications when agents are mentioned using @ in comments or work notes. Notifications include record details and a direct link for quick access.

-   **[Quick start tests for Customer Service Management](https://www.servicenow.com/docs/access?context=quick-start-tests-csm&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

After upgrades and deployments of new applications or integrations, run quick start tests to verify that Customer Service Management works as expected. If you customized Customer Service Management, copy the quick start tests and configure them for your customizations.


</td></tr><tr><td>

Agentic Desktop

</td><td>

-   **[Changes to Now Assist usage measurement](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

Starting with Zurich Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).

-   **[Support for different screen resolutions and scaling](https://www.servicenow.com/docs/access?context=agentic-desktop-overview&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Desktop actions now run reliably on machines with different screen resolutions and scaling. Screen resolution and scaling are consistent across all screens of a desktop actions during creation, saving, and publishing.


-   **[Design UI block desktop actions in Design workspace](https://www.servicenow.com/docs/access?context=agentic-desktop-overview&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Design, configure, and manage desktop actions in the Design workspace that enables:

    -   Auto-recording or manually capturing screens and defining UI interactions, such as clicking buttons, typing into text boxes, and selecting from drop-down menus.
    -   Adding details such as name, description, input and output parameters.
    -   Testing desktop actions before activating them.
    -   Publishing desktop actions to AI Agent Studio as tools for AI agents to execute.
Example: Filling out fields and submitting a form.

-   **[Use non-UI block desktop actions](https://www.servicenow.com/docs/access?context=desktop-actions-designer-workspace-ad&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Add default desktop actions of the type non-UI block as tools to AI agents in AI Agent Studio. The non-UI block actions include pre-built connectors that enable your agentic workflows to interact with various applications and system components. These connectors streamline automation by offering pre-built actions for common tasks, reducing the need for complex scripting.

Each connector focuses on a specific application or system area, providing a collection of related actions. For example, the Microsoft Outlook connector offers actions for email management, while the File and Directory connector provides actions for file system operations.

The following connectors are supported:

    -   Microsoft Excel
    -   Microsoft Outlook
    -   Microsoft Word
    -   PDF
    -   PowerShell
    -   SQL
    -   SSH
    -   SystemAction
Example: Reading data from Microsoft Excel or emails from Microsoft Outlook.

-   **[Adding desktop actions to AI agents in AI Agent Studio](https://www.servicenow.com/docs/access?context=create-ai-agents-ad&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Seamless integration with AI Agent Studio has enabled effortless configuration of desktop actions to automate repetitive tasks on applications without APIs. AI agents can reason, plan, and execute desktop actions autonomously and semi-autonomously across legacy systems and desktop applications without complex setups.

-   **[Monitor desktop actions in Execution workspace](https://www.servicenow.com/docs/access?context=use-agentic-desktop&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Trigger desktop actions from the Now Assist panel that are executed by AI agents in the Execution workspace. Interact with the automation when human input is required. These automations run in the background and listen for instructions dispatched from the ServiceNow instance. You can continue working on other desktop applications outside Execution workspace.

-   **[Leverage core desktop capabilities](https://www.servicenow.com/docs/access?context=desktop-actions-designer-workspace-ad&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Automate form filling, application clicks, and Windows OS file handling. Create workflows across legacy systems, thick client applications, and business applications on Windows operating system to perform repetitive tasks.


</td></tr><tr><td>

Alumni Center

</td><td>

-   **Alumni Center revamp**

The revamped alumni home page is a central hub where former employees can update their details, manage preferences, and access personalized job recommendations. It also provides quick access to alumni services, news, resources, and tasks to stay connected and engaged.

Alumni can maintain their employment history with legacy &amp; latest employment details.

Alumni can view the existing job opportunities​ and also get personal job recommendation based on your job preferences.

-   **Alumni Self-registration**

A former employee can sign up on the Alumni Center and provide details to register as an alumni.

The personal email provided by the employee is validated to verify the employee status ensuring accurate identification and preventing impersonation or duplication.

-   **Configure automatic alumni user creation**

Alumni user creation is streamlined with a configurable process that allows organizations to generate alumni accounts automatically during an employee offboarding. ​Configurable termination conditions can be used to create the alumni and admins can restrict automatic creation with approvals if needed.

-   **Personal Details Verification**

Employees in the offboarding stage can review and confirm their personal details such as email, phone number, and shipping address to facilitate effective communication post offboarding and ease alumni onboarding. The offboarding task is available in the Employee Center to-dos and offboarding journeys.


</td></tr><tr><td>

App Engine Management Center

</td><td>

-   **[Use AEMC to manage app delegation, development, and deployment](https://www.servicenow.com/docs/access?context=app-engine-management-center&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

AEMC is a centralized tool for IT admins and developers to manage the entire app development life cycle, from idea submission to deployment and monitoring. AEMC enhances efficiency and governance, and provides clear insights into custom app usage and developer productivity.

-   **[ReleaseOps integration](https://www.servicenow.com/docs/access?context=exploring-aemc&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

Starting with version 28.2.1 of AEMC, you can deploy using ReleaseOps. ReleaseOps enables the deployment of update sets via a pipeline and leverages the automation capabilities of ServiceNow Playbooks.

-   **[Migrate App Engine pipelines to ReleaseOps](https://www.servicenow.com/docs/access?context=migrating-ae-pipelines-to-releaseops-aemc&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

Starting with version 28.2.1 of AEMC, migrate your existing App Engine pipelines to ReleaseOps to take advantage of ReleaseOps features without disrupting your existing pipeline and deployment process.


</td></tr><tr><td>

Applicant Center

</td><td>

-   **[Applicant Center home page](https://www.servicenow.com/docs/access?context=applicant-portal-home-page&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

The Applicant Center home page is the dedicated and personalized space for applicants that provides them with a complete hiring experience.

-   **[View a job application](https://www.servicenow.com/docs/access?context=view-a-job-application&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

As an applicant, open a job application and view the details.

-   **[Share scheduling preferences](https://www.servicenow.com/docs/access?context=share-availability-applicant-ac&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

As an applicant, when requested by recruiters, share your scheduling preferences to help them schedule interviews accordingly.

-   **[Select an interview slot to self-schedule your interview](https://www.servicenow.com/docs/access?context=select-interview-slot-applicant&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

Select an interview time slot from a list of proposed slots shared by the recruiter to automatically schedule your interview.

-   **[Request to reschedule interview](https://www.servicenow.com/docs/access?context=request-to-reschedule-interview-applicant&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

Request the recruiter to reschedule a proposed or scheduled interview.

-   **[Tasks in Applicant Center](https://www.servicenow.com/docs/access?context=applicant-tasks-applicnts&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

View, track, and complete all your assigned hiring tasks from the Applicant Center home page.

-   **[Applicant survey](https://www.servicenow.com/docs/access?context=applicant-feedback&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

Provide feedback about your hiring experience in Applicant Center.

-   **[Set accessibility preference](https://www.servicenow.com/docs/access?context=set-accessibility-preference&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

Enable keyboard accessibility for your profile to navigate through Applicant Center using keyboard tabs.

-   **[Configure pre-hire experience on applicant center](https://www.servicenow.com/docs/access?context=access-journey-accelerator-from-applicant-centre&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

Start your onboarding journey from Applicant Center even before your first day. Complete all your pre-hire tasks easily and seamlessly.


</td></tr><tr><td>

Application Manager

</td><td>

Zurich patch 4

-   **[Now Assist suites for version compatibility](https://www.servicenow.com/docs/access?context=now-assist-app-mgr&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

Use the Application Manager to install and update Now Assist applications with suites of compatible application versions. Now Assist suites help verify that new Now Assist applications and versions remain compatible with the ones already installed to your instance.

-   **[Application state indicators](https://www.servicenow.com/docs/access?context=app-mgr-state-indicators&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

Review information about any applicable installation considerations, requirements, and blockers in the header of application details.


</td></tr><tr><td>

Application Vulnerability Response

</td><td>

-   **[Enhanced Compensatory controls](https://www.servicenow.com/docs/access?context=requesting-approving-risk-reduction&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

When new vulnerable items are ingested and associated with a remediation task that already has an approved compensating control, the reduced risk rating is now automatically inherited by those new vulnerable items.

-   **[Improved vulnerability assessment workflows](https://www.servicenow.com/docs/access?context=vr-ws-vuln-assessment&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**
    -   CI filtering for vulnerability assessments: You can now filter which configuration items are included in a vulnerability assessment using a condition builder.
    -   Business Application population on AVITs: AVITs created from SBOM assessment results now include Business Application information, helping you understand application impact and prioritize remediation.
    -   Priority roll‑down from vulnerability assessments: Updates to the priority of a vulnerability assessment now automatically roll down to associated VITs and AVITs, ensuring consistent prioritization based on the highest severity.
-   **[Remediation task rule execution mode](https://www.servicenow.com/docs/access?context=sem-grouping-multiple-findings-remediation-tasks-processing&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

You can now choose how remediation task rules are evaluated during ingestion. The new Match First execution mode evaluates rules sequentially and applies only the first matching rule, assigning each finding to exactly one remediation task. The default Match All mode continues to evaluate all applicable rules.

-   **[GitHub Application Vulnerability Integration – Generic secrets support](https://www.servicenow.com/docs/access?context=github-vuln-integration&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

The GitHub Secret Scanning Integration now imports generic secrets in addition to standard secrets from your GitHub repositories. A new Manage generic secrets in ServiceNow configuration option lets you control whether generic secrets are ingested. Imported secrets are mapped to Application Vulnerable Items \(AVIs\) with the scan type Secret, while generic secrets are mapped with the scan type Generic Secret.

-   **Enhancements to Application Vulnerability Response**

The Unassign workflow is supported for application vulnerable items \(AVITs\) and remediation tasks \(AVULs\).

    -   Streamline application vulnerability assignments with the **Unassign** UI action from the more actions menu on an AVIT.
    -   Reassign incorrectly assigned AVITs, clarify ownership for reassessment, and maintain accurate triage records in workspace views.
    -   You have the option to send unassign requests for approval prior to clearing the Assigned to and Assignment group fields on records.
-   **[SBOM document upload via Github Action](https://www.servicenow.com/docs/access?context=vr-sbom-supported-apps&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

Upload valid Software Bill of Material \(SBOM\) documents to ServiceNow platform with the help of GitHub Action.

-   **[Create application remediation tasks manually in the Vulnerability Manager Workspace](https://www.servicenow.com/docs/access?context=vmws-create-remediation-task&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

With the sn\_vul.app\_sec\_manager role, you can create application remediation tasks manually by selecting some or all the records in the Application vulnerable items’ lists in the Vulnerability Manager Workspace. These records are grouped into one or more remediation tasks according to the grouping criteria selected while creating application remediation tasks.

-   **[Create application remediation tasks manually in the IT Remediation Workspace](https://www.servicenow.com/docs/access?context=itr-ws-create-remediation-task&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

With the sn\_vul.app\_security\_champion role, you can create application remediation tasks manually by selecting desired records in the Application vulnerable items’ lists in the IT Remediation Workspace. These records are grouped into one or more remediation tasks according to the grouping criteria selected while creating application remediation tasks.

-   **[Tenable Web Application Scanning Vulnerability Response Integration](https://www.servicenow.com/docs/access?context=tenable-was-integration&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

The Tenable.was integration now supports on‑demand execution of both application and vulnerability imports, allowing you to quickly ingest web applications, findings, and scan metadata into ServiceNow. Imported data automatically populates Discovered Applications, Vulnerability Entries, Scan Summaries, and AVITs, with full visibility through integration run tracking.

-   **[Manual Ingestion of Vulnerabilities for Application Vulnerability Integration](https://www.servicenow.com/docs/access?context=manual-ingestion-of-vulnerabilities-for-application-vulnerability-response&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

Import AVITs from external sources via a standardised template \(e.g., CSV, Excel\) and manage Penetration test findings lifecycle. Now, you can ingest vulnerability data, including details such as affected application, vulnerability description, severity, remediation recommendations, including other necessary details. This enhancement allows you to simplifies the process of consolidating vulnerability data from diverse sources into a centralised Penetration test workspace.

-   **[Penetration Test Workspace](https://www.servicenow.com/docs/access?context=penetration-testing-dashboard&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

Monitor your penetration test requests and findings as well as your team's overall progress in the Penetration Test Workspace. Prioritize tests that need your attention, track findings, and view assignments with the following data visualizations on the dashboard:

    -   Important items.
    -   Penetration test requests that are critical and by state.
    -   Reported findings.
    -   Overall remediation progress based on assignment.
-   **[Enhancements to Penetration Test Assessment Requests](https://www.servicenow.com/docs/access?context=pen_test_dashboard_components&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

Along with Full Penetration, Focused, and Re-test, the following assessment types are included for Penetration Test Assessment Requests forms in the Penetration Test Workspace:

    -   Emergency Release - Supports emergency releases that are required for rapid software updates to address critical issues like security vulnerabilities.
    -   Bug Bounty Program - Rewards ethical hackers to find and report security vulnerabilities.
    -   Release Approvals - Ensure that all necessary checks are completed before deploying new software.
    -   One-off reviews - Assess specific projects outside regular development and release cycles to evaluate performance and implement improvements.
    -   Executive Interest - Report on senior management's engagement and support for critical projects within the organization.
Enhancements to the Release Approval and Release Notes fields help you ensure quality and security for your pen test findings.

The following states have been added to the Release approval field:

    -   **Not Applicable** \(Default\).
    -   **Approved**.
    -   **Denied**.
You can add details to justify your release approvals in the Release notes field.

-   **[Associate CWEs for manual AVIT creation from Penetration Test Assessment Requests](https://www.servicenow.com/docs/access?context=penetration-testing-dashboard&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

On the Penetration test findings tab on Penetration Test Assessment Requests, you have the option to associate Common Weakness Enumerations \(CWE\)s or Common Vulnerabilities and Exposures \(CVE\)s in the **Vulnerability** field for manually created AVITs.

-   **Create change requests in Application Vulnerability Response**

Users with the sn\_vul.app\_sec\_manager and sn\_vul.app\_sec\_champion roles as well as users with the sn\_vul.app\_developer role who have the ITIL role can create change requests from remediation tasks in the Application Vulnerability Response application. Create change requests to expedite your investigation for application vulnerabilities \(AVIT\)s that require manual intervention.

    -   Create change requests with prepopulated information for scanned applications that are classified as configuration items \(CI\)s.
    -   The change request workflow in Application Vulnerability Response is similar to the workflow supported in Vulnerability Response. For more information about the Vulnerability Response change request workflow, see [Change management for Vulnerability Response](https://www.servicenow.com/docs/access?context=vuln-change_mgmnt_ovrvw&version=zurich&pubname=zurich-security-management&ft:locale=en-US).
**Note:** Change requests are supported for Application Vulnerability Response only if the discovered application is associated with a configuration item \(CI\). You must set `Product model` to **False** in the Use Product Model \[sn\_vul.use\_product\_model\] system property to associate a discovered application with a CI.

-   **[Enhancements to the Software Bill of Materials Workspace](https://www.servicenow.com/docs/access?context=sbom-landing&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**
    -   You can delete multiple BOM entity records and their related components with bulk edit from the Software Bill of Materials SBOM SBOM Workspace.
    -   Any Application Vulnerable Items \(AVIT\)s that are associated with deleted BOM entities automatically transition to **Closed**.
-   **[View risk score details of a vulnerable items in the Work notes section](https://www.servicenow.com/docs/access?context=avm-calculators-rules&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

Starting with v25.0.3 of Application Vulnerability Response, the system property **sn\_sec\_cmn.risk\_score\_changes\_add\_worknotes** is inactive by default. If you enable it, only then you can see all the changes related to the risk score of an application vulnerable item in the Work notes section. Additionally, the work notes are updated only if there’s a change in the risk score.


</td></tr><tr><td>

Asset Audit Response

</td><td>

-   **[Manage evidence request responses in the Asset Governance Workspace](https://www.servicenow.com/docs/access?context=asset-governance-workspace&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

Track and manage responses to the evidence requests for your financial regulatory audit engagements by using the Asset Governance Workspace. You can also gain insight into critical audit data such as due dates, statuses, and remediation tasks, which can help streamline the audit engagement process.

-   **[Fulfill evidence requests through the Asset Response Guided Experience](https://www.servicenow.com/docs/access?context=fulfilling-evidence-requests-asset-audit-response&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

Fulfill and respond to evidence requests for your financial regulatory audit engagements by using the Asset Response Guided Experience. It provides step-by-step guidance on generating, reviewing, and submitting the required evidence for each evidence request. You can also create remediation rules and corresponding remediation tasks to identify and resolve any gaps that are discovered through your evidence.

-   **[Manage financial regulatory audit engagements and evidence requests in the Audit Workspace](https://www.servicenow.com/docs/access?context=managing-audit-engagements-asset-audit-response&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

Enable your compliance managers and asset managers to collaborate in managing the financial regulatory audit engagement process and requesting corresponding evidence from asset teams through the Audit Workspace in the ServiceNow® Audit Management application. Managers can scope, plan for, and prioritize each engagement to resolve any regulatory risks and compliance issues before they lead to audit failures. They can also use the requested evidence to formulate audit opinions and complete these engagements.

-   **[Streamline the fulfillment of evidence requests by using financial regulatory context in the Audit Workspace](https://www.servicenow.com/docs/access?context=creating-evidence-requests-asset-audit-response&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

Associate your evidence requests with important financial regulatory requirements and guidelines, such as key financial standards from the Federal Financial Institutions Examination Council \(FFIEC\), by leveraging the Audit Workspace in the ServiceNow Audit Management application. By aligning each request with the relevant requirements and guidelines, you can help your asset managers better understand the compliance obligations that are associated with the requests. They can then use this information to fulfill each request more accurately and efficiently.


</td></tr><tr><td>

Audit Management

</td><td>

-   **Audit Period Start and End Dates **

Set audit period start and end dates directly on Engagement records to focus audits on specific time-frames. The system displays only indicator results that fall within your defined audit period, keeping the audit time-frame separate from the overall engagement time-frame. This helps you audit past or future periods without affecting the broader engagement timeline.

-   ****

Simplify the installation of pre-configured content packs with the new Unified content management icon in the Audit Workspace. Content Accelerator includes the Digital Operational Resilience Act \(DORA\) content pack, offering citations and authority documents for DORA compliance. Audit shared manager and Audit WS supervisor roles can access Content Accelerator.

-   **[Enhancement to evidence request](https://www.servicenow.com/docs/access?context=evidence-request&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

Create evidence response directly in one step. This bypasses the step involved in creation of evidence request and collection details. Evidence response is enhanced with additional data of source and context. To leverage evidence capabilities, feature roles have been introduced:

    -   sn\_grc\_advanced.evidence\_reader
    -   sn\_grc\_advanced.evidence\_requester
    -   sn\_grc\_advanced.evidence\_responder
    -   sn\_grc\_advanced.evidence\_admin
-   **[Integration with ITAM](https://www.servicenow.com/docs/access?context=solutions-gallery&version=zurich&pubname=zurich-better-together&ft:locale=en-US)**

Leverage Audit Management support as an ITAM customer through dedicated feature roles. A lightweight version of the Audit Management workspace is available, which includes the following features:

    -   On the Audit Management home page, you can track **Timeline**, **Engagements**, **Tracking**, **Create evidence request**, and **.**
    -   The lightweight Audit Management also includes the key capabilities, such as Engagement, Entity Scoping, Activities, and Evidence when Advanced Core is installed.

</td></tr><tr><td>

Authentication

</td><td>

-   **[Machine Identity Console](https://www.servicenow.com/docs/access?context=machine-identity-console&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)**

Manage your inbound integration with ServiceNow's Machine Identity Console. Inbound integration in Machine Identity Console provides a simplified configuration experience for your inbound integrations.

-   **[Multi-factor Authentication dashboard](https://www.servicenow.com/docs/access?context=mfa-dashboard&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)**

Use the new MFA Dashboard to understand insights such as MFA user enrollment, privileged admins who haven't opted in to MFA, and compliance. You can verify that all users have MFA enabled for enhanced security with the help of the MFA Dashboard.

-   **[Multi-factor Authentication Guided Setup](https://www.servicenow.com/docs/access?context=mfa-guided-setup&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)**

Use the new MFA Guided setup to configure multi-factor Authentication \(MFA\) for users who currently log in to ServiceNow with only a user name and password. This update enhances security by guiding administrators through the MFA setup process and verifying that all users are protected with an additional layer of authentication.


-   **[Identity Provider attributes for OpenID Connect](https://www.servicenow.com/docs/access?context=idp-attributes-oidc&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)**

Use the Identity Provider \(IDP\) Attributes received from the OIDC response from the Identity Provider as a filter criteria for authentication.


</td></tr><tr><td>

Automated Test Framework

</td><td>

-   **[ATF failure insights](https://www.servicenow.com/docs/access?context=atf-test-triage&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

Reduce the time to resolve your ATF test failures with actionable support from the new ATF failure insights feature.

-   **[Configurable Workspace](https://www.servicenow.com/docs/access?context=atf-conf-ws&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

Enable simplified test creation through direct component interaction on Configurable Workspace pages via the Page Inspector.


</td></tr><tr><td>

Business Continuity Management

</td><td>

-   **[Map recovery tasks and event tasks to the phases](https://www.servicenow.com/docs/access?context=mapping-recovery-tasks-to-phases&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

Set up phases for plans and events using the administrative setup. The base version of the application includes a set of default active phases, provided as seed data.

The logical grouping of tasks into phases enables clear progression tracking for exercises and crisis events, offering flexible execution and task completion requirements for phase transitions.

-   **[Exclude non-recovery tasks from time calculation](https://www.servicenow.com/docs/access?context=add-a-recovery-task&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

Exclude specific recovery or event tasks from time calculations by using the **Do not include in time calculation** field within recovery or event tasks.

-   **[View and generate PDFs of approved plans](https://www.servicenow.com/docs/access?context=mobile-bcm&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

View the continuity and recovery plans directly from your mobile devices. BCM managers can generate PDFs of the approved plans, which BCM planners can then view and download, streamlining access to critical information on the go.

-   **[Verify asset recovery levels](https://www.servicenow.com/docs/access?context=create-new-impact-analysis-reference-form-bcm-uib-ws&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

Track event assets and verify the achieved recovery level of the impacted assets of a task in the **Asset recovery level** field. Completing specific tasks now automatically updates the corresponding event asset state. Assets are marked as **Partially Recovered** when they’re operational enough to support dependent assets, and **Recovered** when they’re fully functional. This change improves visibility into operational readiness and enables coordinators to identify when dependent assets can safely start their recovery process. Color-coded recovery levels of the assets offer visual cues for various recovery progress levels.

-   **[Use finalized RTO and RPO in BIAs, Plans, and Events](https://www.servicenow.com/docs/access?context=create-bia-in-uib-ws&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

Use the **Finalized RTO** field to calculate an accurate Recovery Time Objective \(RTO\) for comparison, using values from the **Recovery time objective** and **Adjusted RTO** fields.

Similarly, use the **Finalized RPO** field to calculate an accurate Recovery Point Objective \(RPO\) values for comparison, using values from the **Recovery point objective** and **Adjusted RPO** fields.

A fix script now populates finalized RTO and RPO values in existing Business Impact Analyses \(BIAs\), ensuring consistency across all records.

-   **[Configure recovery tasks for exercises, events, or both](https://www.servicenow.com/docs/access?context=create-new-recovery-task-form&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

Configure recovery tasks with event-specific scopes \(exercises, actual crises, or both\). When a recovery event is initiated, the system automatically filters tasks by event type: ensuring exercises include necessary setup and validation, and actual crises focus exclusively on actionable recovery work.

-   **[Auto-calculate the Planned end date on activated plans and event tasks](https://www.servicenow.com/docs/access?context=create-exercise-event-ref-form&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

Enter the Planned start date for exercises and events. The system then calculates the Planned start and end dates for activated plans and event tasks automatically based on the **Planned duration** field and dependencies.

-   **[Use hierarchical structure in the associated plans](https://www.servicenow.com/docs/access?context=add-related-plans-recovery-teams-bcp-uib-ws&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

Use the hierarchical structure in the associated plans, establishing clear upstream-downstream relationships. This hierarchy confirms that only relevant downstream plans are brought into scope. The system automatically handles cyclic dependency checks, confirming that tasks from downstream plans aren’t added as dependencies in the upstream plans.

-   **[Use Gantt chart in the Hierarchy view](https://www.servicenow.com/docs/access?context=managing-enhanced-hierarchical-view-in-event-tasks&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

Use the Gantt chart in the Hierarchy view to visualize the planned and actual timelines of event tasks. Task dependencies can now be created directly on the Gantt chart, provided the dependency points to a task scheduled ahead in time. Plans are automatically sorted based on the planned start time of their earliest event task, verifying a clear chronological view.

-   **[Generate reports in a Microsoft Word format using Document designer](https://www.servicenow.com/docs/access?context=integrating-document-designer-with-bcm&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

Create standardized reports for business impact analyses \(BIAs\), business continuity plans \(BCPs\), and events by using predefined Microsoft Word templates. To use these templates, first establish a template relationship registry and install the necessary add-in to design and configure the templates.

Then, import the relevant documents and customize their content, including the table of contents, details, impact assessments, dependencies, and attachments, to be included in the reports. Finally, generate the reports and save them to the corresponding application records.

You can control whether to retain or replace the existing report attachments by configuring the **sn\_bcm.retain\_report\_attachments** system property.

-   **[Avoid duplicate event tasks by grouping similar event tasks](https://www.servicenow.com/docs/access?context=identifying-running-dup-tasks-once&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

Group similar event tasks during recovery events. The system automatically designates the first event task as the original task. When the original task is in progress, the remaining tasks are placed in the **On Hold** state. After the original task is closed, the other tasks in the group are automatically marked in the **Closed duplicate** state.

Tasks with internal dependencies can't be part of the same group. You can also unlink the tasks from their groups, so that the system helps to prevent cyclic dependencies within a group.

-   **[Manage action items for ad-hoc tasks and threat assessments](https://www.servicenow.com/docs/access?context=create-action-items-based-on-smart-assessments&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

Create action items for ad-hoc tasks and send out threat assessments that leverage Smart Assessment during exercises and crises. You can create action items for tasks that support recovery efforts, such as communicating with stakeholders, leadership, or vendors, without directly restoring an asset. Use these action items to conduct threat assessments with the Smart Assessment Engine before, during, or after a recovery event.

To enable task creation during an ongoing event, the Smart Assessment template must include both an event and an action item within its scope.

-   **[Revert an archived BIA or BCP to the Draft state](https://www.servicenow.com/docs/access?context=create-bia-in-uib-ws&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

Revert an archived business impact analysis \(BIA\) or business continuity plan \(BCP\) to its **Draft** state by selecting the **Edit** button on the form. By revising previously completed BIAs, you save time by using a BIA that's already been created.

-   **[Optimized Crisis map interface](https://www.servicenow.com/docs/access?context=manage-alerts-in-crisis-map-interface-uib-ws&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

The Crisis map interface has been optimized to handle over 10,000 resources and more than 1,000 alerts without performance issues.

Customize the display of impacted areas for alerts by using custom shapes or specifying a custom radius. To edit an impacted area, simply select its corresponding card and make the necessary adjustments to the shape. If needed, you can also revert the changes made to an impacted area directly within the map interface.


</td></tr><tr><td>

CPQ Configurator

</td><td>

-   **[Configurable product offerings and associated blueprints](https://www.servicenow.com/docs/access?context=som-create-configurable-prod-offerings&version=zurich&pubname=zurich-order-management&ft:locale=en-US)**

Create configurable products and generate the associated product offering blueprints that contain the product attributes, product relationships, product and pricing rules, and child products defined for configurable products. The blueprints also contain configuration rules for inclusion, exclusion, and determination. Catalog admins can review and update an offering blueprint in the CPQ Configurator and then publish the product offering to the product catalog.

-   **[CPQ Configurator interface](https://www.servicenow.com/docs/access?context=using-servicenowcpq&version=zurich&pubname=zurich-order-management&ft:locale=en-US)**

Enable agents and customers to configure customizable products using the CPQ Configurator embedded in Sales Customer Relationship Management workflows. The configurator is used in both the CSM Configurable Workspace and the Business Portal.


</td></tr><tr><td>

Card data security

</td><td>

-   **[Card Data Security](https://www.servicenow.com/docs/access?context=card-data-security&version=zurich&pubname=zurich-financial-services-operations&ft:locale=en-US)**

Tokenize secure card data in FSO dispute workflows by integrating with a tokenizer service through Card data security. You can configure which values to tokenize, establish connections to core systems and third-party systems like Visa and Mastercard, and manage tokenizer resource configurations.


</td></tr><tr><td>

Care Team Mobile

</td><td>

-   **[Create support requests](https://www.servicenow.com/docs/access?context=cto-mobile-create-requests&version=zurich&pubname=zurich-healthcare-life-sciences&ft:locale=en-US)**

Use Care Team Mobile to create requests for supporting departments directly from your mobile device. The following plugins are supported by Care Team Mobile:

    -   Care Team Operations for Healthcare IT
    -   Care Team Operations for Biomed
    -   Care Team Operations for Facilities
    -   Care Team Operations for Environmental Services
-   **[Scan assets](https://www.servicenow.com/docs/access?context=cto-mobile-asset-scan&version=zurich&pubname=zurich-healthcare-life-sciences&ft:locale=en-US)**

Scan tags on medical equipment and be redirected to the asset's record, where you can view its history, status, and associated cases.

-   **[Browse locations](https://www.servicenow.com/docs/access?context=cto-mobile-browse-locations&version=zurich&pubname=zurich-healthcare-life-sciences&ft:locale=en-US)**

Browse locations in Care Team Mobile to view healthcare locations and create support requests for specific locations as needed.


</td></tr><tr><td>

Care Team Operations for Biomed

</td><td>

-   **[Setting up roles and responsibilities in Care Team Operations for Biomed](https://www.servicenow.com/docs/access?context=cto-biomed-setting-up-roles-responsibilities&version=zurich&pubname=zurich-healthcare-life-sciences&ft:locale=en-US)**

Roles and responsibilities are updated to allow for more selective user access.

The following responsibilities were added:

    -   Support department agent
    -   Support department manager
Users can be assigned these responsibilities in the Edit member related list within healthcare organizations.


</td></tr><tr><td>

Care Team Operations for Environmental Services

</td><td>

-   **[Healthcare Environmental Services case](https://www.servicenow.com/docs/access?context=cto-evs-case-overview&version=zurich&pubname=zurich-healthcare-life-sciences&ft:locale=en-US)**

Expand Healthcare Environmental Services cases to support custom support requests for your organization’s environmental services support department.

-   **[Create environmental services support requests](https://www.servicenow.com/docs/access?context=cto-evs-create-requests&version=zurich&pubname=zurich-healthcare-life-sciences&ft:locale=en-US)**

Request support from your organization’s environmental services department with pre-configured catalog items.

-   **[Healthcare Environmental Services case and work order synchronization](https://www.servicenow.com/docs/access?context=cto-evs-fulfill-requests&version=zurich&pubname=zurich-healthcare-life-sciences&ft:locale=en-US)**

Care Team Operations for Environmental Services automatically syncs environmental services cases with work orders.


-   **[Setting up roles and responsibilities in Care Team Operations for Environmental Services](https://www.servicenow.com/docs/access?context=cto-evs-set-up-roles-responsibilities&version=zurich&pubname=zurich-healthcare-life-sciences&ft:locale=en-US)**

Roles and responsibilities are updated to allow for more selective user access.

The following responsibilities were added:

    -   Support department agent
    -   Support department manager
Users can be assigned these responsibilities in the **Edit member** related list within healthcare organizations.


</td></tr><tr><td>

Care Team Operations for Facilities

</td><td>

-   **[Healthcare Facilities case](https://www.servicenow.com/docs/access?context=cto-facilities-case-overview&version=zurich&pubname=zurich-healthcare-life-sciences&ft:locale=en-US)**

Expand facilities cases to support custom support requests for your organization’s facilities support department.

-   **[Create facilities support requests](https://www.servicenow.com/docs/access?context=cto-facilities-create-request&version=zurich&pubname=zurich-healthcare-life-sciences&ft:locale=en-US)**

Request support from your organization’s facilities department with pre-configured catalog items.

-   **[Healthcare facilities case and work order synchronization](https://www.servicenow.com/docs/access?context=cto-facilities-fulfilling-requests&version=zurich&pubname=zurich-healthcare-life-sciences&ft:locale=en-US)**

Care Team Operations for Facilities automatically syncs Healthcare Facilities cases with work orders.

-   **[Setting up roles and responsibilities in Care Team Operations for Facilities](https://www.servicenow.com/docs/access?context=hco-facilities-set-up-roles-responsibilities&version=zurich&pubname=zurich-healthcare-life-sciences&ft:locale=en-US)**

Roles and responsibilities have been updated to allow for more selective user access.

The following responsibilities were added:

    -   Support department agent
    -   Support department manager
Users can be assigned these responsibilities in the **Edit member** related list within healthcare organizations.


</td></tr><tr><td>

Care Team Operations for Healthcare IT

</td><td>

-   **[Setting up roles and responsibilities in Care Team Operations for Healthcare IT](https://www.servicenow.com/docs/access?context=hco-it-set-up-roles-responsibilities&version=zurich&pubname=zurich-healthcare-life-sciences&ft:locale=en-US)**

Roles and responsibilities are updated to allow for more selective user access.

The following responsibilities were added:

    -   Support department agent
    -   Support department manager
Users can be assigned these responsibilities in the Edit member related list within healthcare organizations.


</td></tr><tr><td>

Career Conversations

</td><td>

-   **[New third-party AI model provider options available for all Now Assist applications](https://www.servicenow.com/docs/access?context=exploring-large-language-models&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Google Gemini and AWS Claude are available for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.


[Zurich Patch 7](../quality/zurich-patch-7.md)

-   **[Streamline feedback collection and review using the Employee feedback collection AI agent](https://www.servicenow.com/docs/access?context=employee-feedback-agent&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

As an admin, create reusable feedback templates using the Platform Surveys tool allowing managers to select and preview templates when requesting feedback, and help them quickly view a summarized snapshot of a reportee’s recent feedback with easy navigation to the feedback page in Manager Hub.


[Zurich Patch 2](../quality/zurich-patch-2.md)

-   **[Create a growth conversation with the help of an agent in Now Assist](https://www.servicenow.com/docs/access?context=agentic-wf-conversations-na-td&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

As a manager, use the growth conversations preparation AI agent to schedule and prepare for employee growth discussions. The agent provides a clear summary of employee activity and career journey, with data-driven talking points to make conversations more focused and impactful.

**Note:** This feature is available when you have both Now Assist for HR Service Delivery \(HRSD\), which will install Now Assist for Talent and HR Talent AI Agent Collection

-   **[Edit a conversation series](https://www.servicenow.com/docs/access?context=edit-conversations-series&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

As a manager, you can now edit a conversation series based on your requirements.

-   **[End a conversation series](https://www.servicenow.com/docs/access?context=egd-create-growth-conversation&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

As a manager, you can now specify a date on which a growth conversation series should end.

-   **[View upcoming conversations based on status](https://www.servicenow.com/docs/access?context=egd-create-growth-conversation&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

As a manager, you can now filter upcoming conversations based on the status of the conversation.


</td></tr><tr><td>

Case management for CSM

</td><td>

-   **[Task plan templates](https://www.servicenow.com/docs/access?context=task-plan-templates&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

Create templates that define the repeatable tasks and records that need to be created for business processes. Define the tasks, set the task order, and create conditions that determine when these tasks and records are created.

-   **[Add multiple entitlements to a case](https://www.servicenow.com/docs/access?context=add-entitlement-to-case&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

View the available entitlements on a customer service case and associate the multiple entitlements to the case. Available entitlements are associated with the account or consumer, product, and contract selected on the case record.

-   **[Recommend service definitions based on case context](https://www.servicenow.com/docs/access?context=csm-service-definitions&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

Recommend the most relevant services to an agent based on the record context, such as the short description or description of the interaction.

-   **[Customer Service Case Types - Enable the service selector to launch record producers](https://www.servicenow.com/docs/access?context=csm-service-definition-catalog-items&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

Use the Service Portal record producers when your agents are creating cases in CSM Configurable Workspace. Agents can select the service definitions from the case type selector and launch the record producers.

-   **[Quick start tests for Customer Service Management](https://www.servicenow.com/docs/access?context=quick-start-tests-csm&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

After upgrades and deployments of new applications or integrations, run quick start tests to verify that Customer Service Management works as expected. If you customized Customer Service Management, copy the quick start tests and configure them for your customizations.


</td></tr><tr><td>

Change Management

</td><td>

-   **[Control opening of CAB meetings](https://www.servicenow.com/docs/access?context=attend-cab-meeting-using-cab-workbench&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

Control the opening of a CAB meeting from the CAB Meeting calendar in the CAB Meeting workbench in Service Operations Workspace or in the Core UI through the **sn\_change\_cab.com.snc.change\_management.cab.use\_sow\_meeting** system property. For more information, see [Change Management properties](https://www.servicenow.com/docs/access?context=r_ChangeManagementProperties&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US).

-   **[Track conflict detection](https://www.servicenow.com/docs/access?context=c_ConflictDetection&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

Track the progress of conflict detection using the Change - Conflict Detection flow \(that runs as a system user\) and the Change Management Worker table instead of Progress Workers. You can choose between the Flow and Progress Worker options by updating the **change.conflict.useprogressworker** system property.

A new UI formatter **change\_conflict\_worker\_progress\_gate.xml** has been introduced to the change request form to replace the existing **change\_request\_conflict\_progress.xml**. This update supports the **change.conflict.useprogressworker** system property when you upgrade to Zurich. The new formatter displays the same Conflict tab but selects the macro version to render the form according to the value of the new system property.

-   **[Define the maximum records for conflict detection](https://www.servicenow.com/docs/access?context=configure-conflict-properties&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

Limit the maximum number of conflict records that can be generated for each conflict type when conflict detection runs through the **change.conflict.max\_count** system property; create this system property if it is not already present.


</td></tr><tr><td>

Classic Workflow

</td><td>

-   **[Restrict access to Workflow Editor with a new role](https://www.servicenow.com/docs/access?context=r_WorkflowRoles&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US)**

Grant access to the Workflow editor by giving users the snc\_required\_script\_writer role.


</td></tr><tr><td>

Cloud Cost Management 9.0

</td><td>

-   **[Achieve better efficiency with faster retrieval of cost and usage data with the Azure Export method](https://www.servicenow.com/docs/access?context=schedule-azure-billing-job&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

Manage cost and usage datasets in Azure billing downloads efficiently by using the Azure Export method. With this feature, you can retrieve larger cost datasets faster.

-   **[Manage MCA contracts with the enhanced support for Microsoft Azure MCA](https://www.servicenow.com/docs/access?context=create-ms-azure-service-principal&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

Gain access to the spend reporting and recommendations for Azure based MCA contracts. This feature helps you to visualize cost and usage data from Azure MCA accounts and optimize your cloud spend with recommendations for potential savings.


</td></tr><tr><td>

Cloud Exposure View

</td><td>

-   **[Enhancements to the Wiz Vulnerability Response Integration](https://www.servicenow.com/docs/access?context=vr-wiz-exploring-host-cf&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**
    -   The Universally Unique Identifier \(UUID\) that identifies detections for the Wiz Host Vulnerability integration will be mapped to a detection key.

**Note:** This enhancement is supported for new customers only.

For existing customers, the detection key for the Wiz Host Vulnerability integration is created using the combination of vulnerability, asset\_id, and proof.

    -   Added the source\_id column to the Container Image Finding table \(sn\_vul\_container\_image\_findings\) and mapped the id attribute from the Wiz import to this field on findings records.

**Note:** Perform a full import after upgrading to view the enhancement on container image findings, container image, and container image vulnerabilities records.

    -   The image repository name format for new and existing discovered container images has been updated to align with the discovery format. The supported format is registry/repository. A separate finding is created for a repository present in each registry.
    -   Appended all repositories that are associated with an image to the Repository field on the Discovered Container Image \[sn\_vul\_container\_image\] table, which can help you see images from specific repositories.
    -   You can configure the **First** parameter for the Wiz Asset Integration to help you resolve 504 errors. You can reduce the page size if you are having memory issues or generating errors. The default value is 500.
    -   The default integration instance parameter for configuring finding keys for the Container Vulnerability Integration includes src\_ci, vulnerability, package, image\_layer, and image\_repository.
-   ****

The Cloud Exposure View module provides a single location for cloud security teams to monitor and act on all their cloud-related security findings from multiple vendors across their cloud environments.

    -   Configure widgets that display interactive visualizations and filter assets by category for findings, assets, and exceptions.
    -   View panels with links on a single page that direct you to the following detailed lists:
        -   Needs Attention
        -   Cloud resources with active findings
        -   Top Accounts/Assets by Risk
        -   Toxic combinations
        -   Compliance scores
    -   View aggregated security data imported from third-party vendors.
See [Unified Security Exposure Management release notes](../security-operations/secops-sem-rn.md) for more information about Unified Security Exposure Management.


</td></tr><tr><td>

Code Signing

</td><td>

-   **Code Signing Installation using Plugin**

Customer administrators can now install the Code Signing plugin directly from the ServiceNow Plugin portal without the need to contact the Customer Service and Support team to enable the Code Signing framework. This enhancement supports self-service deployment and simplifies the installation process.

-   **[Quorum Controlled Certificate Revocation](https://www.servicenow.com/docs/access?context=certificate-revocation&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)**

Revoke Code Signing certificates using a quorum-based control policy. Revoke certificates to help prevent them from being used to verify signatures. A quorum-based approval flow promotes added security by requiring approvals from multiple stakeholders, to help prevent unintended or unauthorized certificate revocations.

-   **[Code Signing Health and Status Dashboard](https://www.servicenow.com/docs/access?context=code-signing-health-and-status-dashboard&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)**

The new **Code Signing Health and Status** dashboard provides a centralized, user-friendly interface to monitor the overall health and configuration of your code signing environment. It highlights configuration settings, displays the status of essential components, and offers actionable guidance to help resolve issues effectively.


</td></tr><tr><td>

Collaborative Work Management

</td><td>

-   **[Enterprise Agile Planning \(EAP\) integration with CWM](https://www.servicenow.com/docs/access?context=integrate-eap-with-collaborative-work-management&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)**

Enhance visibility and streamline planning for your teams with EAP integration into CWM.

For Agile teams managing non-agile work items like incidents and change tasks, this integration bridges the gap by automatically creating a dedicated Space and Board in CWM. Agile work is seamlessly brought over via Connected Work, while EAP sprints are reflected directly in CWM’s Sprint planning view, thus enabling unified planning across all work types. Teams can plan work for their sprints and update work status directly from the CWM Board, with performance reports in EAP dynamically reflecting these changes. This integration enables teams to manage their full scope of work from a single, connected workspace.

-   **[Board preferences](https://www.servicenow.com/docs/access?context=cwm-boards&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)**

Reduce cognitive load and focus on the most relevant and actionable tasks by filtering work items on CWM boards based on their last updated date and hiding those items marked as Closed complete. From the Board preferences menu on the Board header, you can choose to show items last updated within 7 days, 30 days, 90 days, 120 days, or 1 year.

-   **[Kanban card layout settings](https://www.servicenow.com/docs/access?context=cwm-board-views&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)**

Surface the information that's most relevant to you using Card Layout settings for Kanban view of a CWM Board. You can now personalize Kanban cards by selecting up to five fields to display on them. For a cleaner, distraction-free view, you can enable the Compact layout, which shows only the work item name on the card. Alternatively, the Full view shows all selected fields, offering better context directly on the card. Based on your workflow needs, tailor your workspace to enhance the way you track tasks.

-   **[Dynamic data linking in CWM Docs](https://www.servicenow.com/docs/access?context=cwm-docs&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)**

Keep record information in your documentation always current and reduce manual effort with the Dynamic data linking feature in Docs. You can now reference any ServiceNow application record and Docs will automatically reflect the latest updates from those records. For example, if you add a reference to a Project record, the reference will show the latest field information of the project in Docs without requiring manual edits. Clicking the project reference opens up the project form so that you can view the full details of the project record and make any necessary changes. Dynamic linking also enables adding references to a particular field of a record, such as Assigned to of an Incident record.

You can add references from any ServiceNow table you have access to, with no setup or configuration needed, thereby eliminate the hassle of switching between applications to copy and paste data from various records into Docs.

-   **[Agile sprint planning in CWM](https://www.servicenow.com/docs/access?context=agile-sprint-planning-in-cwm&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)**

Plan, track, and manage work for your teams by using Agile sprint planning in the CWM workspace. You can use CWM to manage tasks in multiple methodologies including ad hoc, waterfall, and Agile practices.

    -   View such details as the backlog, current sprint, and future sprints at a glance from the Sprint planning view of the CWM Board.
    -   Add Agile item types, such as stories, with other CWM tasks to the backlog.
    -   Create sprints with a custom duration and sprint capacity.
-   **[Connected work in CWM](https://www.servicenow.com/docs/access?context=unified-boards-for-connected-work-in-cwm&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)**

Streamline team collaboration and planning by enabling your teams to view and plan all their work in one place by connecting work across multiple ServiceNow applications. By defining the type of work you want to connect to CWM, you can bring in records from other applications into CWM Boards.

After the records are added to a CWM Board, your teams can update their status and other details from within CWM, or perform sprint planning for all the work on the Board. This unified experience improves efficiency because your teams don't have to switch between multiple workspaces.

-   **[Navigation panel enhancements](https://www.servicenow.com/docs/access?context=cwm-spaces&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)**

Move Spaces, Boards, and Docs around in the navigation panel of the workspace by using the drag and drop functionality.

-   **[Enhancements to Kanban view](https://www.servicenow.com/docs/access?context=cwm-board-views&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)**
    -   Quick filters: Filter the tasks based on the work type that you would like to see in the Kanban view of a CWM Board. You can select single or multiple work item types based on the swim lanes selected. Any filters that you apply to the Kanban view are specific to this view and aren't applied to List or Gantt views.
    -   Horizontal lanes: Group the cards on the Kanban view by using a vertical and horizontal lane for improved visibility into the type and progress of work. You can save horizontal lane preference into Board views and templates.
-   **[Copying and pasting content within Docs](https://www.servicenow.com/docs/access?context=cwm-docs&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)**

Copy and paste the content such as text, images, lists, and tables from one Doc page to another. The following content is supported for the copy and paste action:

    -   Text blocks with existing formatting
    -   Bulleted and numbered lists
    -   Tables
    -   Images
    -   Single and multiple paragraph blocks into a table cell
    -   Lists into a table cell
    -   Images into a table cell
-   **[New keyboard shortcuts](https://www.servicenow.com/docs/access?context=cwm-spaces&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)**
    -   Create Space:
        -   macOS: Option + S
        -   Windows OS: Alt + S
    -   Create Board:
        -   macOS: Option + B
        -   Windows OS: Alt + B
    -   Create Doc:
        -   macOS: Option + D
        -   Windows OS: Alt + D
-   **[Keyboard shortcut enhancements within CWM Docs](https://www.servicenow.com/docs/access?context=cwm-docs&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)**
    -   Insert a URL in the Doc:
        -   macOS: Cmd + K
        -   Windows OS: Ctrl + K
    -   Insert a new row in a table after the last row: Enter
    -   Move to adjacent cells within a table: Arrow keys
    -   Create a new list item within an existing list in a table or paragraph: Enter
    -   Create a new line in the same bullet point: Shift + Enter
    -   Indent a list item: Tab

</td></tr><tr><td>

Common Core

</td><td>

-   **[Entity based record access update utility guided experience](https://www.servicenow.com/docs/access?context=entity-based-access-playbook&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

Apply entity-based access \(EBA\) restrictions at the record level by using guided assistance in the entity based record access update utility. Guided assistance consists of a four-step process:

    1.  Define the scope for the relevant entities
    2.  Scope the record types
    3.  Apply the conditions to each record type to refine the scope
    4.  Review the selected records before you execute and initiate the update
See the execution logs for a status after each update. You can get the details about the impacted records, applied scopes, and outcomes.

-   ****

The report a GRC issue AI agent is now available in the Employee Center, enabling employee users to report issues through a guided conversational experience. As users respond to prompts, the agent structures the issue and recommends relevant controls, entities, and policies based on the input provided. The AI agent helps ensure that the issue is well-defined and enriched with contextual information before it's submitted.

-   **[Entity based record access rules to secure new records](https://www.servicenow.com/docs/access?context=continuous-monitoring-of-entity-based-access&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

Configure entity-based record access rules on record types to ensure that access restrictions are applied automatically to secure new records or modified records related to entities with active EBA configurations.

-   ****

Maintain seamless access for users and groups referenced in record fields when entity-based access restrictions are applied. This feature enables users and groups referenced in a record’s user or group fields to access the records they are associated with. By configuring record-level user access at the table or record type level, it reduces administrative overhead and streamlines EBA adoption with minimal disruption.

-   **[Deactivation of entity-based access configuration](https://www.servicenow.com/docs/access?context=deactivating-entity-based-access&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

Deactivate the entity-based access configuration, enabling the system to automatically assess the records that it impacts. If entity-based access configuration is restricting a record, the access restrictions are removed. If other configurations also apply to the record, the restrictions remain in place and only the selected configuration is deactivated.

-   ****

Apply or remove domain-specific tags across multiple records at once. This streamlines workspace management by letting you quickly filter and organize records, for example, you can exclude non-privacy-tagged items in the Privacy Workspace for a more focused, efficient view.

-   **[Entity record page enhancements](https://www.servicenow.com/docs/access?context=entities-in-risk-ws&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

The Entity type and Downstream Risks \(now renamed as Risks\) related lists on the Entity record page have been converted to UIB pages, providing a more intuitive and modern interface. The Downstream Risks related list has been moved to the dedicated Risks page, featuring organized tabs for Directly related risks, Suggested risks, and All risks.

**Note:** You may experience issues with custom actions that emit events on the Risks or Entity type related lists on the Entity record page. To ensure a smooth transition and adopt these changes, refer to [KB2593527](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2593527) for detailed guidance.

-   **[Model Text Protocol \(MCP\) Client](https://www.servicenow.com/docs/access?context=mcp-client&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Enable users of the ServiceNow® AI Agent Studio to access tools that are hosted externally and published using an MCP Server via the Model Context Protocol Client application.

Authenticate users with the MCP Server to add the MCP tool to an AI agent.

-   **[Create an AI agent](https://www.servicenow.com/docs/access?context=configure-next-best-action-agent&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

The **Add** button on the **AI agents** tab is added as a drop-down providing different agent types for AI agent creation:

    -   Chat
    -   External
-   **[Configure ACLs for AI agents and agentic workflows](https://www.servicenow.com/docs/access?context=aia-security-implementation&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Configure the Access Control Lists for who can discover and trigger AI agents and agentic workflows in their guided setups in AI Agent Studio. You can determine whether an AI agent or agentic workflow behaves as a dynamic user or as an AI user. You can also specify if an AI agent or agentic workflow can be available to all authenticated users or publicly available.

-   ****

Easily manage which configurations appear on the My Tasks page by marking them Active or Inactive. This gives you flexibility to enable or disable configurations without manual intervention, simplifying administration and improving control. An Active/Inactive flag has also been introduced in the My Choice table for enhanced configuration management.


-   ****

Entity names in GRC now automatically update when the associated CI name changes. This enhancement improves data consistency, reduces manual effort, and ensures alignment between CI and Entity records without requiring custom automation.


</td></tr><tr><td>

Configurable Workspace

</td><td>

-   **Activity stream compose with modeless dialog component bundle**

Open the Compose editor as a pop-out, modeless dialog to draft comments, work notes, and emails while working on other tasks.


</td></tr><tr><td>

Configuration Compliance

</td><td>

-   **[Remediation task rule execution mode](https://www.servicenow.com/docs/access?context=sem-grouping-multiple-findings-remediation-tasks-processing&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

You can now choose how remediation task rules are evaluated during ingestion. The new Match First execution mode evaluates rules sequentially and applies only the first matching rule, assigning each finding to exactly one remediation task. The default Match All mode continues to evaluate all applicable rules.

-   **[Optimized Tenable.io Compliance Results ingestion](https://www.servicenow.com/docs/access?context=tenable-io-integrations-list&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

Starting with v 6.1.3, the Tenable.io Compliance Results Integration is replaced by the Tenable.io Fixed Compliance Results Integration and Tenable.io Open Compliance Results Integration. Compliance results are now imported based on their status, optimizing ingestion performance and scalability for environments with large volumes of compliance data while keeping remediation and compliance tracking aligned with the current state of findings.

-   **[Qualys Integration – API enhancements](https://www.servicenow.com/docs/access?context=qualys-rest-messages-cc&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

Qualys Integration has been upgraded to support newer Qualys API versions across Host Detection, Host List, Knowledgebase, PC Controls, PC Policies, and PCRS integrations. The integrations now ingest additional data fields, including vulnerability detection source, authentication privilege status, active status for controls and policies, and cloud metadata, giving you better visibility into your vulnerability and compliance data. Use the new `posture_api_version` integration instance parameter to choose between the default v2.0 APIs or the newer v5.0 streaming APIs for the PCRS Policy Host and PCRS Test Results integrations.

-   **[Unified Microsoft Defender Integration for Security Exposure Management](https://www.servicenow.com/docs/access?context=ms-defender-sem&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

The Microsoft Defender for Cloud and Microsoft Defender Threat and Vulnerability Management \(MS TVM\) plugins are now consolidated into a single plugin: Microsoft Defender Integration for Security Exposure Management. This consolidation deprecates the standalone Microsoft Defender for Cloud plugin. The unified plugin also introduces container image vulnerability ingestion from Microsoft Defender for Cloud, creating Container Vulnerable Items on your instance. A guided migration path is available to transfer existing data from the deprecated applications to the unified plugin.

-   **[Enhancements to the Vulnerability Response Integration with Wiz](https://www.servicenow.com/docs/access?context=vr-wiz-exploring-host-cf&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

The Missing Assets \[sn\_vul\_wiz\_missing\_asset\] is deprecated. After updating to version 1.1, you must backdate your existing primary Wiz integrations by three days and run them.

The backfill integrations are activated by default.

After you backdate and run your integrations, the following backfill integrations are no longer required:

    -   Host Vulnerability Backfill Integration
    -   Test Results Backfill Integration
    -   Host Test Results Backfill Integration
    -   Issues Backfill Integration
The \[is\_ignored\] column is deprecated for the Host Test Results and Test Results Integrations. This column was replaced by the \[is\_result\_ignored\] column.

Source severity is mapped to the Priority column on the Test Results \[sn\_vulc\_result\] table.

Resource type filters are on the Test Results, Issues, and Host Test Results configuration tabs on the Wiz Configuration page. You can add any of the resource types listed.

**Note:**

If you configure resource types on the Resource Type Configuration tab, and you choose to configure parameters on the integration instance records, your configurations on integration instance take precedence over your settings on the Resource Type Configuration tab. See [Identify Wiz Resource types](https://www.servicenow.com/docs/access?context=wiz-assets-resources-tab&version=zurich&pubname=zurich-security-management&ft:locale=en-US) for more information.

Additional attributes imported from Wiz that are not stored in the Discovered items \[sn\_sec\_cmn\_src\_ci\] table are stamped with `Asset Attributes` in this table.

Test results from the Host misconfiguration integration are classified as result type 'host\_misconfiguration'.

Data for resources that have the validated\_at\_runtime flag set to 'yes' is imported and populated on detections.

The is\_ignored column is deprecated on the Host Test Results and Test Results Integrations. This column was replaced by the is\_result\_ignored column.

The CMDB internet-facing field on the discovered item is mapped to Limited Internet Exposure on findings.

Column length for the descriptions in the Host Vulnerability import table has been increased.

-   **[Qualys parameter to ignore passed test results](https://www.servicenow.com/docs/access?context=Qualys-cc-Integration&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

Starting with v15.2.5 of Configuration Compliance, the ignore\_passed\_result integration instance parameter for the Qualys Integration for Security Operations has been added.

This parameter is set to `false` by default so that passed test results imported by Qualys are not ignored.

Set the parameter to **true** to ignore passed test results on import.

**Note:** If activated, this parameter does not impact closure of the test results. For example, if you activate the parameter, and a failed test result from a previous import has since passed, it will be closed correctly.

-   **[Identify Wiz Resource Types for import](https://www.servicenow.com/docs/access?context=wiz-assets-resources-tab&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

Identify the Resource Types \(assets\) reported by Wiz in your environment on the Wiz Integration Resource Type configuration page in your ServiceNow AI Platform instance that you want to import.

The Resource Types that you select apply to all the primary Wiz vulnerability and compliance integrations except the Wiz Container Vulnerability Integration.

-   **[Wiz Backfill Integrations](https://www.servicenow.com/docs/access?context=wiz-backfill&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

Retrieve and process data stored on the Wiz Missing Assets \[sn\_vul\_wiz\_missing\_asset\] table for missing assets that were not processed by the primary compliance integrations with specialized Wiz Backfill Integrations.

    -   Test Results Backfill Integration
    -   Host Test Results Backfill Integration
    -   Issues Backfill Integration
The Wiz Backfill Integrations are activated by default.

-   **[Wiz Host Test Result Vulnerability Integration](https://www.servicenow.com/docs/access?context=wiz-host-test-result-tab-filters&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

Import test results associated with the resource type, `VIRTUAL MACHINE` with the Wiz Host Test Result Vulnerability Integration. This integration is activated by default.

-   **[The Wiz Configuration Compliance \(Test Results\) and Issues Integrations](https://www.servicenow.com/docs/access?context=vr-wiz-exploring-host-cf&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**
    -   Import configuration test results with the Wiz Configuration Compliance Integration \(Wiz Test Results\) to detect non-compliant cloud configurations. Findings are mapped to cloud test results \(CTRs\) in the Configuration Compliance application to help you enforce security policies and standards across your cloud environment.
    -   Import data with the Wiz Issues Integration that can help you identify assets that are involved in toxic combinations of vulnerabilities and misconfigurations. These findings are also mapped to CTRs with `Wiz Issues` labeled as the source to help you track and remediate assets that may pose complex multi-vector risks.

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

-   **[CMDB Workspace v8.0](https://www.servicenow.com/docs/access?context=cmdb-workspace&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US):**

You can now use the Create CI experience in CMDB Workspace to create a CI with a lookup identifier entry that contains mandatory attributes. When you select a lookup identifier entry on the Required attributes page, those mandatory attributes now appear and you can set their values for proper IRE processing. For more information, see [Create a CI manually in CMDB Workspace](https://www.servicenow.com/docs/access?context=create-ci-manual-cmdb-workspace&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).

-   **[CMDB Workspace v7.6](https://www.servicenow.com/docs/access?context=cmdb-workspace&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US):**

    -   Access a centralized location with a comprehensive view of CI details by using the new CI form in CMDB Workspace. The form shows the attributes \(key attributes are highlighted on a Summary page\), tags, resources, activities, relationships, related services, health state, performance indicators, and CMDB 360 data that is associated with the CI. While viewing, you can also modify many of those CI details. For information about all the details on a CI form, see [Manage CI details in CI Form](https://www.servicenow.com/docs/access?context=ci-form-cmdb-workspace&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).
    -   Access the Data Certification dashboard in CMDB Workspace. The Data Certification dashboard provides the insights about the data certification activities and progress, policies and tasks, reports about certification instances, charts that show the aging certification tasks, and group and individual workloads. For more information, see [Data Certification Dashboard](https://www.servicenow.com/docs/access?context=data-cert-dashboard-workspace&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).
    -   [Create or manage a shared preset](https://www.servicenow.com/docs/access?context=unified-map-manage-shared-preset&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US). Save Unified Map filter settings as shared presets that any user on the team can access. This task requires the sn\_cmdb\_admin, sm\_admin, or admin role.
    -   [Access Unified Map from the main navigation panel](https://www.servicenow.com/docs/access?context=cmdb-workspace-unified-map&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US). Access Unified Map from the main navigation panel by navigating to **All** &gt; **CMDB Workspace** &gt; **Unified Map**.
    -   Archival and destroy processes of certification policy related records, are now separated from those processes for records of all other policy types. This separation facilitates the extension of the retention period of certification policy records as follows:
        -   The table cleanup rule for the CMDB Data Management Policy Executions \[cmdb\_data\_management\_policy\_execution\] table, which is stored in the Auto Flushes \[sys\_auto\_flush\] table, now excludes certification policy execution records from recurring cleanups.

Retaining certification policy execution records instead of deleting them after 7 days is useful in situations where those records are needed for audits and are also useful for the Data Certification Dashboard, which is populated by these records.

        -   The Archive CMDB Data Management Tasks archive rule, that applied to all CMDB Data Manager policy execution records, now excludes certification policy records. At each archive run, this archive rule is configured to also automatically archive its related records in the CMDB Data Management Certification Task To Document \[sn\_cmdb\_ws\_dm\_certification\_task\_to\_document\] table \(Archive Related Records\).
        -   The archive rule, Archive Certification Instances, is added to specifically archive certification policy execution records from the CMDB Data Management Policy Execution \[cmdb\_data\_management\_policy\_execution\] table. This new archive rule is configured to archive certification policy execution records 2 years after creation, and to destroy those records 7 years after they are archived.
        -   The archive rule, Archive Certification tasks, is added to specifically archive the certification task records from the CMDB Data Management Task \[cmdb\_data\_management\_task\] table.
        -   The archival of related records in the CMDB Data Management Certification Task To Document \[sn\_cmdb\_ws\_dm\_certification\_task\_to\_document\] table is now moved as an Archive Related Records entry from the Archive CMDB Data Management Tasks archive rule to the new Archive Certification tasks archive rule.
The Zurich release includes an installation of CMDB Workspace. However, you can download a newer version of CMDB Workspace so that you can use its latest features in your Zurich instance. For more information, visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home).

-   **[Quick start tests for CMDB](https://www.servicenow.com/docs/access?context=quick-start-tests-cmdb&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)**

After upgrades and deployments of new applications or integrations, run quick start tests to verify that CMDB works as expected. If you customized CMDB, copy the quick start tests and configure them for your customizations.


</td></tr><tr><td>

Container Vulnerability Response

</td><td>

-   **[Remediation task rule execution mode](https://www.servicenow.com/docs/access?context=sem-grouping-multiple-findings-remediation-tasks-processing&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

You can now choose how remediation task rules are evaluated during ingestion. The new Match First execution mode evaluates rules sequentially and applies only the first matching rule, assigning each finding to exactly one remediation task. The default Match All mode continues to evaluate all applicable rules.

-   **[Enhancements to the Vulnerability Response Integration with Wiz](https://www.servicenow.com/docs/access?context=vr-wiz-exploring-host-cf&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**
    -   The Universally Unique Identifier \(UUID\) that identifies detections for the Wiz Host Vulnerability integration will be mapped to a detection key.

**Note:** This enhancement is supported for new customers only.

For existing customers, the detection key for the Wiz Host Vulnerability integration is created using the combination of vulnerability, asset\_id, and proof.

    -   Added the source\_id column to the Container Image Finding table \(sn\_vul\_container\_image\_findings\) and mapped the id attribute from the Wiz import to this field on findings records.

**Note:** Perform a full import after upgrading to view the enhancement on container image findings, container image, and container image vulnerabilities records.

    -   The image repository name format for new and existing discovered container images has been updated to align with the discovery format. The supported format is registry/repository. A separate finding is created for a repository present in each registry.
    -   Appended all repositories that are associated with an image to the Repository field on the Discovered Container Image \[sn\_vul\_container\_image\] table, which can help you see images from specific repositories.
    -   The default integration instance parameter for configuring finding keys for the Container Vulnerability Integration includes src\_ci, vulnerability, package, image\_layer, and image\_repository.
-   **[Enhancements to the Vulnerability Response Integration with Wiz](https://www.servicenow.com/docs/access?context=vr-wiz-exploring-host-cf&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

The Missing Assets \[sn\_vul\_wiz\_missing\_asset\] is deprecated. After updating to version 1.1, you must backdate your existing primary Wiz integrations by three days and run them.

The backfill integrations are activated by default.

After you run them after updating to v1.1, the following backfill integrations are no longer required:

    -   Host Vulnerability Backfill Integration
    -   Test Results Backfill Integration
    -   Host Test Results Backfill Integration
    -   Issues Backfill Integration
Data for resources that have the validated\_at\_runtime flag set to 'yes' is imported and populated on detections.

The CMDB internet-facing field on the discovered item is mapped to Limited Internet Exposure on findings.

Fix information that includes 'Fix available', 'Partial fix available', 'No fix available', and 'Fix version' from the \[fix\_available\] and \[fix\_version\] columns is rolled up to CVITs from findings. Note: If there are two or more findings on a CVIT, the fixed version might only apply to one. In that case, 'Partial fix available' is rolled up to the CVIT.

The Wiz vendor severity attribute is mapped to the 'Source severity' column on findings records in the Container Image Findings \[sn\_vul\_container\_image\_findings\] table.

The cluster and namespace is evaluated for all the following entity Types: DEPLOYMENT, DAEMON\_SET, STATEFUL\_SET, POD.

-   **[Import container vulnerability data with the Vulnerability Response Integration with Wiz](https://www.servicenow.com/docs/access?context=vr-wiz-exploring-host-cf&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

Import configuration test results from Wiz to detect non-compliant cloud configurations. Findings are mapped to cloud test results \(CTRs\) in the Configuration Compliance application to help you enforce security policies and standards across your cloud environment.

-   **[Enhancements to imported scanner results](https://www.servicenow.com/docs/access?context=cvr-remediation-task-overview&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

Enhancements support more scanner data on imports. Namespaces and hierarchy cluster are considered and populated in the discovered container image \[sn\_vul\_container\_image\] table if this data is imported.


</td></tr><tr><td>

Continual Improvement Management

</td><td>

-   **[CIM roles](https://www.servicenow.com/docs/access?context=cim-roles&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

Implement and monitor improvement initiatives as a Continual Improvement Management \(CIM\) coordinator or manager without any ITIL role-related restrictions.

-   **[Applications integrated with Continual Improvement Management](https://www.servicenow.com/docs/access?context=cim-integration&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

As a CIM manager or coordinator, create change records from CIM tasks. If you have not been assigned the required ITIL or change\_write roles, contact your system administrator.


</td></tr><tr><td>

Continuous Authorization and Monitoring

</td><td>

-   ****

Streamline governance, risk, and compliance processes with the CAM Workflow Configuration. This feature allows administrators to:

    -   Create and manage multiple workflows within a package.
    -   Define GRC State Models for custom workflows.
    -   Configure and version workflows.
    -   Evaluate workflow version impacts to retrieve baseline controls.
    -   Set up workflow-specific approval configurations.
    -   Perform risk assessments across CAM objects.
    -   Migrate the NIST RMF flow to workflow configuration for improved standardization.
-   ****

Introducing a new Child Boundaries list that enables a one-to-many boundary hierarchy, allowing you to create relationships between boundaries. This hierarchy is visualized in both the sidebar and diagram view, showing one parent boundary with multiple child boundaries. OSCAL export and import now include the parent boundary relationship if present.

-   **Dynamic Boundary Filters Dynamic boundary filters**

Select the **Dynamic Filter** option in boundary filters to update system elements according to filter conditions. When disabled, the system elements remain unchanged. This update enhances the flexibility of boundary filter management.

-   **Boundary operational status automation**

Linking boundary operational status to the package life cycle ensures seamless integration. Key changes include:

    -   Automatic update of boundary status to Operational when a package moves to the Monitor state.
    -   Transition of Boundary status to Reauthorize as the Package Authorization date approaches. This update maintains synchronization between package and boundary states, enhancing overall system coherence.
-   ****

Generating and downloading OSCAL SSP and POA&amp;M files is supported directly from within a authorization package. The supported file types include:

    -   Catalog
    -   Overlay Catalog
    -   Profile
    -   SSP
    -   POA&amp;M
-   **OSCAL import enhancements**

Enhancing the OSCAL import experience, the OSCAL import playbook now allows you to:

    -   Import individual POA&amp;M JSON files.
    -   **User Mapping**: Automatically map users to existing ServiceNow users based on exact name matches, with the option to manually adjust mappings.
    -   **Group Mapping**: Automatically map groups to existing ServiceNow groups based on exact name matches, with the option to manually adjust mappings.
    -   **Roles and Responsibilities**: Populate relevant package fields with roles and responsibilities.
-   **[Overlay enhancement](https://www.servicenow.com/docs/access?context=prepare-auth-pkg&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

Apply policies as an overlay in an authorization package to determine how the control objectives in the policy impact the baseline. This can be done in the following ways:

    -   Addition: Create control objectives to address specific requirements not covered in the baseline.
    -   Subtraction: Move existing control objectives to **Not Applicable**.
    -   Customization: Create, move existing control objectives to not applicable, or skip control objectives.
-   **[OSCAL enhancements](https://www.servicenow.com/docs/access?context=oscal-cam-ws&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

Use the OSCAL import playbook to follow a user-friendly, step-by-step approach for importing OSCAL models. Using the playbook, you can:

    -   Add multiple Catalog overlay files.
    -   Preview OSCAL data before importing them to confirm accuracy. You can preview the following:
        -   Authorization boundary
        -   Authorization package
        -   System elements
        -   Information types
        -   Baseline controls
        -   Inherited controls
        -   Hybrid controls
        -   Not applicable controls
        -   Policies
        -   Control objectives
        -   Control objectives requirements
    -   Skipped objects in the preview, such as control objectives, policies, authorization boundaries and packages can be individually overridden.

</td></tr><tr><td>

Contract Management Pro

</td><td>

-   **[Better visibility of undelivered signature requests for a contract](https://www.servicenow.com/docs/access?context=cncore-cr-state-status&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

When an electronic signature request is not delivered, the contract state is updated to Signature delivery failed and the signatory status to Delivery failed, clearly indicating the state of signature request. Contract fulfillers are also notified through in‑product and email alerts. This capability is supported for both Docusign and Adobe Sign.


-   **[Contract amendments](https://www.servicenow.com/docs/access?context=cmpro-amend-landing&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

Formally change, add, or remove terms in an existing contract through contract amendments without having to replace the entire agreement. The Amendment feature enables you to initiate, track, and finalize amendments to existing contracts and provides an audit trail. The signed contract and its amendment documents are stored in a centralized repository under the parent contract, which enables you to manage all related documents from a single location.

    -   Use the **Request type** field to distinguish between contract and amendment requests.

    -   View the amendment history directly from the contract request.

    -   View amendment details within the contract repository record through related lists:

        -   Contract Requests: View all contract and amendment requests associated with the contract.
        -   Amendment Field Changes: Track modifications over time by accessing a detailed log of all field changes made through amendments.
        -   Contract Documents: Access all documents related to the contract, including those generated or updated as part of amendment processes.

-   **[Compare contract revisions in Contract Management Pro](https://www.servicenow.com/docs/access?context=cmpro-compare-docs&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

Compare a contract document in .docx format with its revised version from your workspace by using the **Compare documents** option.

Document comparison is not supported for contract documents stored in external storage.

-   **[Contract summarization](https://www.servicenow.com/docs/access?context=cmpro-summarize-contract-cmr&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

Generate a summary of contract documents, supporting documents, and signed contracts in Contract Management Pro. You can also generate FAQs from the document or ask questions in the Now Assist panel to retrieve specific information from the document.


-   **[Link parent contract requests](https://www.servicenow.com/docs/access?context=cmpro-link-parent-cmr&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

Establish a hierarchical relationship between the parent and child contract requests during the drafting and negotiation phases. You can choose to have the child contract request automatically inherit the configured fields from the parent request. The contract repository records associated with the parent and child contract requests are automatically linked after the contracts are signed.

-   **[Perpetual contracts](https://www.servicenow.com/docs/access?context=cncore-work-ss-cntr-request-fulfiller&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

Classify a contract with no end date as a perpetual contract by using the **Perpetual** option.

Perpetual contracts must be initiated from Sales Customer Relationship Management and Source-to-Pay Operations.

-   **[Help Center](https://www.servicenow.com/docs/access?context=help-center&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US)**

Access help information directly from your workspace through a help icon ![](../../common/image/Banner_HelpIcon.png) that accesses the Help Center for the landing and list pages of Contract Workspace.​


</td></tr><tr><td>

Contract Management Pro for Legal Service Delivery

</td><td>

-   **[Contract amendments](https://www.servicenow.com/docs/access?context=snlc-amend-req-landing&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

Contract amendments enable you to formally change, add, or remove terms in an existing contract without replacing the entire agreement. The Amendment feature enhances contract lifecycle management by enabling you to initiate, track, and finalize amendments to existing contracts with audit trail.

A new field, **Request type**, has been added to clearly distinguish between contract and amendment requests.

Each amendment is linked to its parent contract, and you can easily view the amendment history directly from the contract request. Additionally, a record producer is available in the base system, allowing you to submit and monitor amendment requests efficiently.

The following related lists are now available within the contract repository record to provide amendment details:

    -   Contract Requests: Displays all contract and amendment requests associated with the contract.
    -   Amendment Field Changes: Shows a detailed log of all field changes made through amendments, enabling easy tracking of modifications over time.
    -   Contract Documents: Provides access to all documents related to the contract, including those generated or updated as part of amendment processes. The signed contract and its amendment documents are stored in a centralized repository under the parent contract for easy access and managing all related documents from a single location.

</td></tr><tr><td>

Conversation Improvement Themes

</td><td>

-   **[Determine effective and ineffective conversations](https://www.servicenow.com/docs/access?context=conv-impr-themes-use&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Analyze conversation quality data over time and classify them into effective and ineffective conversations.

-   **[Categorize conversations into themes](https://www.servicenow.com/docs/access?context=conv-impr-themes-use&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Identify recurring patterns linked to low or high conversation quality and categorize user requests into actionable themes.


</td></tr><tr><td>

Conversation Insights

</td><td>

-   **[Inferred CSAT](https://www.servicenow.com/docs/access?context=exploring-conversation-insights&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Inferred CSAT provides an estimated score computed using AI in real time by analyzing the entire sequence of the conversation.

-   **[CSAT factors](https://www.servicenow.com/docs/access?context=exploring-conversation-insights&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

The following CSAT factors provide explainability to the Inferred CSAT score.

    -   Resolution
    -   Confusion
    -   Effort
    -   Empathy
    -   Next Steps
    -   Frustration
    -   Transfers and Escalations
-   **[AI Agent Analytics dashboard](https://www.servicenow.com/docs/access?context=ai-agent-dashboard&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

The AI Agent Analytics dashboard includes visualizations with Inferred CSAT scores and factors by default.


</td></tr><tr><td>

Creator Studio

</td><td>

-   **[Customizable email notifications](https://www.servicenow.com/docs/access?context=crs-admining-notifications&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

Promote consistent branding by having admins create custom email notifications and templates, which are sent when users request something from an app or the request was changed or closed. In support, several of the standard email notification activities are now in the public scope, and a new Configure email notifications item is available in Guided Setup.

-   **[New playbook activity to update record fields](https://www.servicenow.com/docs/access?context=creator-studio-add-activities-automation&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

Enable apps to change several fields automatically on the submitted record using the new Update submission playbook activity. In support, a new Configure playbook activities item is available in Guided Setup.

-   **[New question types for forms](https://www.servicenow.com/docs/access?context=creator-studio-form-elements-ref&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

Two new question types are available for forms: Duration and Attachment.

    -   Duration enables users to specify a length of time.
    -   Attachment enables users to upload an attachment as a question. The **Attachment** field differs from the **Add attachment** option for the form, because the Attachment question type can be used in dynamic behavior questions.
-   **[Granular configuration admin roles](https://www.servicenow.com/docs/access?context=roles-creator-studio&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

Several new granular admin roles enable developers to complete administrative configuration tasks without requiring the full admin role.

-   **[Delete unpublished forms](https://www.servicenow.com/docs/access?context=crs-delete-form&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

You can now delete unpublished forms from Creator Studio, which completely removes the record for the form from the ServiceNow AI Platform.


</td></tr><tr><td>

Customer Contracts and Entitlements

</td><td>

-   **[Renew a service contract](https://www.servicenow.com/docs/access?context=cce-renew-service-contract&version=zurich&pubname=zurich-order-management&ft:locale=en-US)**

Initiate renewals from contracts at either the line level or the contract level. The resulting renewal quotes and orders generate a new contract that is associated with the original contract in the renewal history.


-   **[Add contract lines to a service contract](https://www.servicenow.com/docs/access?context=cce-add-contract-lines&version=zurich&pubname=zurich-order-management&ft:locale=en-US)**

Add new line items to an existing contract by initiating the flow from contract. You can also add new line items to an existing contract while modifying a quote or contract.


-   **[Modify a service contract](https://www.servicenow.com/docs/access?context=cce-modify-service-contract&version=zurich&pubname=zurich-order-management&ft:locale=en-US)**

Initiate a modification from the contract header to generate a quote or order containing all contract lines. You can also select specific contract lines and initiate a modification, resulting in a quote or order that includes only the selected lines.


-   **[Upsell or Downsell a service contract line](https://www.servicenow.com/docs/access?context=cce-upsell-downsell-service-contract&version=zurich&pubname=zurich-order-management&ft:locale=en-US)**

Select one or more root contract lines to adjust quantities. You can add or reduce quantities on a contract line by selecting the Upsell or Downsell feature. After updating the quantities of the contract lines, a single quote or order is generated with the updated quote lines.


-   **[Support Price Ramps in contract](https://www.servicenow.com/docs/access?context=using-customer-cnt-ent-wf&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

Enable customers to specify price ramps for a product or service in a single quote. When the quote is completed and the order process is finalized, the contract captures the new pricing details.​


-   **[Enhancements in Renewals workflow](https://www.servicenow.com/docs/access?context=create-cont-ent-workflows-csm&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**
    -   Configure renewal opportunity and quote generation dates on separate dates.
    -   Renewed quotes automatically update when new products are added to auto-renewed contracts.

-   **[Non-Standard Renewals](https://www.servicenow.com/docs/access?context=cce-renew-service-contract&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

Renew customer contracts outside the standard renewal cycle. You can perform early renewals to generate new contracts with updated pricing terms or late renewals to extend contracts after the expiry date.


-   **[Modify line item quantities](https://www.servicenow.com/docs/access?context=cce-upsell-downsell-service-contract&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

Swap an existing subscribed product or service with another product, either partially or fully.


</td></tr><tr><td>

Customer Engagement Sequences

</td><td>

-   **[Multi-trigger sequences with decision branches for stages](https://www.servicenow.com/docs/access?context=define-trigger-conditions&version=zurich&pubname=zurich-order-management&ft:locale=en-US)**

Configure the sequences playbook to start based on multiple conditions across entities, eliminating the need for separate sequences for similar workflows. Add a decision node between stages to determine which stage to run next, based on the outcome of the previous stage.

-   **[Schedule call activity for telesales workflows](https://www.servicenow.com/docs/access?context=add-schedule-call-activity&version=zurich&pubname=zurich-order-management&ft:locale=en-US)**

Design sequences with the new Scheduled call activity to automate structured call attempts, including delays and outcome-based branching, directly from the playbook interface. This helps agents follow a repeatable, optimized process for engaging prospects or customers in telesales workflows.

-   **[Runtime permissions and fine-grained access control](https://www.servicenow.com/docs/access?context=configure-runtime-permission-sequence-playbooks&version=zurich&pubname=zurich-order-management&ft:locale=en-US)**

Enforce runtime permissions to control access to sequence records such as sequence tasks and steps.

-   **[Granular role framework](https://www.servicenow.com/docs/access?context=components-installed-customer-engagement-sequences&version=zurich&pubname=zurich-order-management&ft:locale=en-US)**

Assign role-based access for sequence admins, writers, executors, and readers. Sequence admins have full control, writers manage their own sequences, executors \(formerly viewers\) have read-only access to sequences and sequence task records, and readers view sequence records. For more information, see [Compatibility information for Customer Engagement Sequences](https://www.servicenow.com/docs/access?context=compatibility-matrix-upgrade-info&version=zurich&pubname=zurich-order-management&ft:locale=en-US).

-   **[Review sequences in Workflow Studio](https://www.servicenow.com/docs/access?context=view-sequence-design-time&version=zurich&pubname=zurich-order-management&ft:locale=en-US)View sequences**

Enable the sales operations teams to optimize and share the high-performing sequences across territories to promote best practices across the organization.

-   **[No-code interface for admins to configure sequences](https://www.servicenow.com/docs/access?context=configuring-customer-engagement-sequences&version=zurich&pubname=zurich-order-management&ft:locale=en-US)**

Configuring multi-step sequences that define specific activities using a no-code playbook experience reduces dependency on developers.

-   **[Sequence tasks with predefined activities for agents](https://www.servicenow.com/docs/access?context=execute-sequence-steps&version=zurich&pubname=zurich-order-management&ft:locale=en-US)**

Predefined activities provide the following advantages to your agents:

    -   Ensure consistent messaging and effective objection handling using clearly defined steps that dynamically adapt to customer responses.
    -   Follow a repeatable, optimized process for engaging prospects or customers.
    -   Avoid communications from sounding generic and improve engagement rates by customizing a prospect’s name, company, and other details.
    -   Reduce the chance of missing a follow-up, promoting consistency in outreach and reduction in manual effort.

</td></tr><tr><td>

Customer Service Problem Management

</td><td>

-   **[Components installed with Customer Service Problem Management](https://www.servicenow.com/docs/access?context=spm-components&version=zurich&pubname=zurich-proactive-service-exp-workflows&ft:locale=en-US)**

The granular admin role enables developers and administrators to complete administrative configuration tasks for Customer Service Problem Management without requiring the full admin role.


-   **[Setting up a test group](https://www.servicenow.com/docs/access?context=setting-test-group&version=zurich&pubname=zurich-proactive-service-exp-workflows&ft:locale=en-US)**

Enables the system to trigger the required tests for service problem cases, incidents, and change request, helping to identify the root cause of the problem. Test group includes test definitions.

-   **[Diagnose and resolve a service problem case](https://www.servicenow.com/docs/access?context=work-on-service-problem-case&version=zurich&pubname=zurich-proactive-service-exp-workflows&ft:locale=en-US)**

Review, diagnose, resolve, and close a service problem case for the service-related issue experienced by the customer.


</td></tr><tr><td>

Customer Success Management

</td><td>

-   **[Calculate health score](https://www.servicenow.com/docs/access?context=account-lifecycle-setup-health-defn&version=zurich&pubname=zurich-acct-lifecycle-events&ft:locale=en-US)**

Starting with Customer Success Management 5.3.11, you can use the **Calculated** metric data source to determine the health score for an engagement. If you are upgrading from Customer Success Management 5.3.10 or earlier versions, you must run the `Set health migration status` script to enable the health score calculation using this data source.


-   **[Define a table data source](https://www.servicenow.com/docs/access?context=account-lifecycle-define-data-source-table&version=zurich&pubname=zurich-acct-lifecycle-events&ft:locale=en-US)**

Starting with Customer Success Management 5.3.11, you can use the **Table** type data source to retrieve and analyze data from internal and external tables. To retrieve data from external sources, you must install the Workflow Data Fabric Hub application and create data fabric tables.


-   **[Risk and issues page](https://www.servicenow.com/docs/access?context=account-lifecycle-risk-issues-page&version=zurich&pubname=zurich-acct-lifecycle-events&ft:locale=en-US)**

Use the risk timeline visualization to manage the risk occurrences.


-   **[Granular admin roles](https://www.servicenow.com/docs/access?context=account-lifecycle-success-roles&version=zurich&pubname=zurich-acct-lifecycle-events&ft:locale=en-US)**

The granular admin role enables developers and administrators to complete administrative configuration tasks for Customer Success Management without requiring the full admin role.


-   **[Read-only field enhancements](https://www.servicenow.com/docs/access?context=account-lifecycle-read-only&version=zurich&pubname=zurich-acct-lifecycle-events&ft:locale=en-US)**

Read-only field protections have been moved from the client side to the server side. This move prevents users from updating read-only fields through client-side methods.


-   **[Success report dashboard](https://www.servicenow.com/docs/access?context=account-lifecycle-success-report-overview&version=zurich&pubname=zurich-acct-lifecycle-events&ft:locale=en-US)**

Use the Success report dashboard to see the overall view of all the engagements under your hierarchy and manage your entire customer portfolio. Monitor engagement metrics, risk indicators, and get insights into onboarding and adoption status, risk indicators, onboarding and adoption insights, and expansion and renewal metrics.


-   **[Product adoption and usage](https://www.servicenow.com/docs/access?context=account-lifecycle-product-adopt&version=zurich&pubname=zurich-acct-lifecycle-events&ft:locale=en-US)**

Measure product adoption trends and proactively guide users to achieve desired outcomes using products and services that have been purchased. Identify active and power users and areas where additional training or support is required due to low engagement.


-   **[Implementation record](https://www.servicenow.com/docs/access?context=account-lifecycle-imp-record&version=zurich&pubname=zurich-acct-lifecycle-events&ft:locale=en-US)**

Track the progress of a partner or customer implementing a product or a service. Get a centralized view of the implementation status, identify risks, and run playbooks to mitigate issues.


-   **[Engagement hierarchy](https://www.servicenow.com/docs/access?context=account-lifecycle-view-engage&version=zurich&pubname=zurich-acct-lifecycle-events&ft:locale=en-US)**

View aggregate hierarchical data for an engagement. Make informed decisions, improve customer satisfaction through detailed tracking, identify risks early, and help prevent escalations.


-   **[Engagement timeline](https://www.servicenow.com/docs/access?context=account-lifecycle-touchpoint-planner&version=zurich&pubname=zurich-acct-lifecycle-events&ft:locale=en-US)**

View a chronological list of critical events related to an engagement. Review timelines to recall past events, customer interactions, and identify any issues.


-   **[Contextual color bands](https://www.servicenow.com/docs/access?context=account-lifecycle-setup-color-banding&version=zurich&pubname=zurich-acct-lifecycle-events&ft:locale=en-US)**

Associate thresholds and visual representations to health metric data. View product adoption and usage information relative to a specific product.


</td></tr><tr><td>

Customer self-service for Sales and Order Management

</td><td>

-   **[Customer-initiated RFQs](https://www.servicenow.com/docs/access?context=create-rfq-business-portal&version=zurich&pubname=zurich-order-management&ft:locale=en-US)**

Request quotes for products and services without relying on manual outreach. The RFQ feature in the Business Portal streamlines the quoting process by enabling customers to:

    -   Submit quote requests from within their portal experience
    -   Specify the overall budget and cumulative target price for each top-level product
    -   Track RFQ status and quotes in real time
    -   Accelerate sales response time with seamless quote-to-order conversion
-   **[Generate quotes from RFQs](https://www.servicenow.com/docs/access?context=convert-rfq-quote-workspace&version=zurich&pubname=zurich-order-management&ft:locale=en-US)**

View all RFQs submitted through the Business Portal in the CSM/FSM Configurable Workspace, eliminating the need for managing and tracking them offline. Convert RFQs into quotes with a single action, accelerating the quote-to-order process, improving turnaround times, and enabling scalable quote management.

-   **[Create orders from the Business Portal](https://www.servicenow.com/docs/access?context=order-mgt-create-an-order-using-customer-portal&version=zurich&pubname=zurich-order-management&ft:locale=en-US)**

Deploying the Sales Cart plugin provides the following advantages to your B2B customers when they order products using the Business Portal:

    -   Preserve products and configurations added to the cart across sessions and devices so customers can review or update their selections without placing an order. They don't have to start their shopping process all over again if they get interrupted, leave the site, or decide to come back later.
    -   Enable better collaboration and decision making by downloading a cart summary in PDF format and reviewing products to be purchased and terms and conditions with business stakeholders.
    -   Sign the acknowledgment section and share the cart summary PDF with the seller to place an offline order.
    -   Provide the flexibility to select or modify billing and shipping addresses during the checkout process.

</td></tr><tr><td>

Data Loss Prevention Incident Response

</td><td>

-   **[Create a Data Loss Prevention Incident Response SLA trigger](https://www.servicenow.com/docs/access?context=sla-records&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

Enable prompt and efficient responses to incidents by creating SLA triggers.

-   **[Create a Data Loss Prevention Incident Response SLA definition](https://www.servicenow.com/docs/access?context=dlp-sla-definitions&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

Outline the conditions and duration for responding to data breaches by creating Data Loss Prevention Incident Response SLA definitions.

-   **[Create an Application in Proofpoint and Obtain Client Credentials](https://www.servicenow.com/docs/access?context=create-application-proofpoint-dlp&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

Create an application in Proofpoint and configure the required settings to obtain client credentials. These credentials enable secure access to the Proofpoint API for seamless integration and automation.

-   **[Install and configure the Proofpoint integration for Data Loss Prevention](https://www.servicenow.com/docs/access?context=install-configure-proofpoint-integration-dlp&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

Install and configure the Proofpoint integration to use the  Proofpoint DLP incident data to investigate DLP incidents.


</td></tr><tr><td>

Data Management

</td><td>

-   **[Data Management Console](https://www.servicenow.com/docs/access?context=viewing-data-usage&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

View a summary of data usage on your instance and manage the growth of data directly from the Data Management Console.

-   **[Monitor data usage at the table level](https://www.servicenow.com/docs/access?context=viewing-data-usage&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

View a summary of data usage for an individual table and monitor data usage in associated tables that store attachments, audit records, and journal entries.

-   **[View data usage for logical tables](https://www.servicenow.com/docs/access?context=viewing-data-usage&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

Monitor data usage for logical tables, including the Incident \[incident\], Problem \[problem\], and Change Request \[change\_request\] tables.

-   **[Identify which tables are driving the most growth in other tables](https://www.servicenow.com/docs/access?context=viewing-data-usage&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

View tables contributing the most growth to the tables that store attachments, audit records, and journal entries.

-   **[Rule summary](https://www.servicenow.com/docs/access?context=viewing-data-usage&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

Track the number of records in the backlog and view the execution history of a table's data management rules.


</td></tr><tr><td>

Data Management for CSM

</td><td>

-   **Naming customer relationship records for [Consumer team member relationship tables](https://www.servicenow.com/docs/access?context=assign-team-member-to-consumer&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US) and [Household team member relationship tables](https://www.servicenow.com/docs/access?context=assign-team-member-to-household&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

Use the **Type** field through related party configurations to name records in the consumer team member and household team member relationship tables. This functionality enables you to label relationships based on the purpose of the association and relevant industry use cases.

-   **[Migrating legacy workflow to low code](https://www.servicenow.com/docs/access?context=create-escalation-template&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

Added an **Escalation Approval Flow** field to the Escalation Template \[sn\_customerservice\_escalation\_template\] table where existing customers can continue using their current escalation workflows or migrate to the new flows, depending on their customizations.

As part of this update:

    -   The legacy Escalation-Approval workflow has been migrated to the low-code flow designer.
    -   The Escalation Master–Approval workflow has been converted into a business rule.
-   **[Account address enhancements](https://www.servicenow.com/docs/access?context=account-address-access-for-contacts&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

Enable contacts to access the account addresses that permit contacts to view both account-address records and the associated location information for accounts they’re authorized to access.

-   **Using [CSM Data Classification application](https://www.servicenow.com/docs/access?context=using-csm-data-classification&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

Use the new CSM Data Classification \(com.snc.csm\_data\_privacy\) Store app that delivers base system classifications for CRM data, categorizing it as internal, personally identifiable information \(PII\), confidential, and more. The solution uses the ServiceNow AI Platform data privacy capabilities, such as data classification, to apply protection measures and enhance data security.

-   **Support indirect sales through Business Locations with [Order Management for business location](https://www.servicenow.com/docs/access?context=order-managment-for-business-location&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US), [Quote Management for business location](https://www.servicenow.com/docs/access?context=quote-management-for-business-location&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US).**

Use the Sales Customer Relationship Management capabilities for both internal and external business organizations to enable Order Management, and Quote Management systems for business locations. Support channel sales and indirect sales by enabling business location staff to collaborate with an enterprise in managing customer orders, quotes, and performing the following actions:

    -   Permit enterprise sales agents to associate business locations as channel partners to create and fulfill customer orders and quotes.
    -   Enable self-service order tracking for internal and external business location staff through the Business Location Service Portal to track and manage customer orders.
    -   Support the tracking of multiple business locations for a single order or quote, either at the order line item level, order related party, quote line item level, or the quote related party.
    -   Improve the indirect sales cycle efficiency by converting approved channel quotes into customer orders.
-   **Support indirect sales through Business Locations with [Opportunity Management for business location](https://www.servicenow.com/docs/access?context=opportunity-management-for-business-location&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US).**

Use the Sales Customer Relationship Management capabilities with both internal and external business organizations using Opportunity Management for business locations. Support channel sales by enabling business location staff to create and modify business opportunities and to track end-to-end life cycle of opportunities.

-   **ServiceNow CPQ integration with MACD workflows**

Introduced new data model changes to enable ServiceNow CPQ configurator usage for MACD workflows.

-   **[Sales and Service API Core](https://www.servicenow.com/docs/access?context=sales-and-services-api-core&version=zurich&pubname=zurich-order-management&ft:locale=en-US) and [Lead to Cash Core](https://www.servicenow.com/docs/access?context=entity-configuration-and-mapping&version=zurich&pubname=zurich-order-management&ft:locale=en-US)**

Granular admin roles introduced in Lead to Cash Core and Sales and Service API core.

-   **[Explore partial sync](https://www.servicenow.com/docs/access?context=about-partial-sync&version=zurich&pubname=zurich-order-management&ft:locale=en-US)**

Synchronize only specific sections of your data structure using the new partial sync capability in the create instance flow. This enhancement introduces the `allowedContextTypes` parameter, which enables you to specify exactly which types should be processed during synchronization operations. This leads to the following benefits:

    -   Improved performance: Reduction in processing time for targeted updates.
    -   Reduced resource consumption: Lower database queries, memory usage, and network bandwidth.
    -   Faster response times: Users experience quicker synchronization operations.
-   **[Granular roles in Install Base Management](https://www.servicenow.com/docs/access?context=r_rolesinstalledwithcustaccessmgmt&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

Added new granular roles with the sn\_install\_base.install\_base\_admin admin role, which is installed with Customer Service Install Base Management \[com.snc.install\_base\] plugin.

    -   sn\_install\_base.install\_base\_read
    -   sn\_install\_base.install\_base\_write
    -   sn\_install\_base.install\_base\_create
    -   sn\_install\_base.install\_base\_delete
    -   sn\_customerservice.customer\_data\_viewer
    -   sn\_customerservice.case.viewer
These roles provide you with more control over administrative tasks like read, write, create, delete, data view, and case view related to install base and sold product related entities.

-   **Billing account store application**

Install the new CSM Billing Account Core store application, which introduces a foundational data model and hierarchy for managing billing accounts. It enables you to define billing relationships, establish account hierarchies, and track financial responsibility across your organization.

-   **[Sold product form](https://www.servicenow.com/docs/access?context=sold-product-form&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

The following enhancements are added for the Sold Product in this release:

    -   Billing Account: Enables direct reference to the associated Billing Account on the Sold Product entity within ServiceNow® CRM allowing agents to access financial information instantly during service delivery. This provides visibility into payment terms and conditions linked to the product, builds customer trust through transparent and predictable billing, and supports accurate revenue recognition for businesses.
    -   Start and end Dates: Provides full lifecycle state‑transition support \(**In preparation, Active, Expired, Cancelled**\) with automated date‑driven updates.

</td></tr><tr><td>

Data Privacy

</td><td>

-   **[New Data Discovery experience](https://www.servicenow.com/docs/access?context=data-discovery-landing&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)**

Use the new Data Discovery experience, which simplifies the experience of discovering and anonymizing PII.

-   **[Column-level discovery](https://www.servicenow.com/docs/access?context=granular-configuration&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)**

Select a specific column of a table for granular scanning during data discovery jobs.

-   **[Anonymization of encrypted field](https://www.servicenow.com/docs/access?context=dps-data-anonymization&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)**

Anonymize encrypted columns to help you achieve compliance with data privacy regulations and defense-in-depth data protection.


</td></tr><tr><td>

DevOps Change Velocity

</td><td>

-   **[Import based evidence collection](https://www.servicenow.com/docs/access?context=import-based-evidence-collection-for-orchestration-capability&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

Improve instance efficiency by skipping step-level pipeline processing for accelerated change management and evidence collection for GitHub Actions, Azure DevOps \(ADO\), GitLab and  Jenkins orchestration tools.


</td></tr><tr><td>

Developer Sandboxes

</td><td>

-   **[Exploring Developer Sandboxes](https://www.servicenow.com/docs/access?context=exploring-sandboxes&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

View the total, available, and allocated sandboxes in your instance by using the Sandbox Management home dashboard. The dashboard also displays information about each sandbox, including the status, data utilization, owner, when the sandbox was last accessed, and when the sandbox was allocated.

-   **[Create a sandbox template](https://www.servicenow.com/docs/access?context=create-sandbox-template&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

Enable your delegated developers to reuse the data so that they can test their changes without manually inputting the data every time.

-   **[Create a Data Generation Profile](https://www.servicenow.com/docs/access?context=create-data-generation-profile&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

Enable your customers to generate the data for testing within the context of developer sandboxes, but also independently of sandboxes.

**Note:** Developer Sandboxes can't copy all the instance data. Data generation profiles enable a statistical sampling of data from selected tables with curated mappings to populate the sandbox with the data needed for building an application.

-   **[Allocate a sandbox](https://www.servicenow.com/docs/access?context=allocating-sandboxes&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

Allocate the sandboxes that were created to your development teams.

-   **[Retire Developer Sandboxes](https://www.servicenow.com/docs/access?context=retire-sandboxes&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

Retire outdated sandboxes to make room for the new sandboxes in your instance.

-   **Automatically backed up update sets**

If you install Developer Sandboxes on an instance after Zurich Patch 5, update sets are automatically backed up when the instance is upgraded.


</td></tr><tr><td>

Digital End-User Experience

</td><td>

-   **[View collected metrics with Metrics analyzer](https://www.servicenow.com/docs/access?context=view-dex-metrics&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

Using the DEX Metrics analyzer, explore and analyze various metrics for Configuration Items \(CIs\) through selecting metrics by application, device, location, and OS.

-   **[Monitoring non-persistent VDIs](https://www.servicenow.com/docs/access?context=monitoring-np-vdis&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

Set up monitoring of non-persistent VDIs to identify performance issues and to troubleshoot.

-   **[Set up page-level monitoring](https://www.servicenow.com/docs/access?context=set-up-page-level-monitoring&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

Monitor a Web application performance at a specific page level and view the collected metrics in the Metrics analyzer.

-   **[Assign ITIL-related roles to DEX users](https://www.servicenow.com/docs/access?context=components-installed-with-dex&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

Exercise tighter control over the role management system and role delegation. Control who has access to Express list, Alerts, and Incident records after the ITIL-related roles have been removed from the dex\_user or dex\_engineer roles.

-   **[Monitor Microsoft Teams call quality](https://www.servicenow.com/docs/access?context=monitor-teams-call-quality&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

View detailed metrics for the Microsoft Teams calls of a particular user, including call quality, network metrics, and session data, with DEX for Microsoft 365.

-   **[Create a remedial action](https://www.servicenow.com/docs/access?context=create-remedial-action&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

Access the Create Remedial Action page from the DEX Administration workspace. DEX admins can create a remedial action or link to an existing remedial action to a check definition. To enhance the end-user experience, you can also run the remedial action on multiple impacted devices at once.

-   **[Device health page](https://www.servicenow.com/docs/access?context=user-health-card&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

View real-time data from the past 24 hours for alerts, change requests, and incidents impacting a device in the Device events Timeline chart on the Device health page.

-   **[DEX issue diagnosis and resolution agentic workflow](https://www.servicenow.com/docs/access?context=now-assist-itsm-dex-diagnosis-resolution-workflow&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

Service desk agents can use the DEX diagnosis and resolution agentic AI workflow to resolve issues on DEX monitored devices through a structured process that includes diagnosis of the cause, a resolution plan with actionable steps, and documenting the resolution in the incident record.

-   **[DEX issue diagnosis and resolution agentic workflow](https://www.servicenow.com/docs/access?context=now-assist-itsm-dex-diagnosis-resolution-workflow&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

Service desk agents can diagnose and resolve Zoom call quality issues using the DEX issue diagnosis and resolution agentic workflow, which integrates Zoom-specific diagnostics that correlate device, network, and application data.

-   **[Incident investigation with DEX](https://www.servicenow.com/docs/access?context=dex-diagnostics-guided-resolutions&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

Service desk agents can diagnose and resolve common issues on DEX monitored devices from the Investigation tab in incident records within the Service Operations Workspace. View the health status of the device and related metrics, review the suggested resolutions, and execute remedial actions or follow self-help instructions to resolve the incident. Monitor the status of actions after they’re completed.

-   **[Customize themes for Desktop Assistant](https://www.servicenow.com/docs/access?context=customize-da-theme&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US), [Customize Desktop Assistant home page](https://www.servicenow.com/docs/access?context=change-home-page-title&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US), and [Create a hyperlink card in Desktop Assistant](https://www.servicenow.com/docs/access?context=create-hyperlink-card&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

DEX Desktop Assistant administrators can customize the theme for Desktop Assistant by modifying specific CSS variables. You can also customize the logo, add hyperlink cards, and map these cards to sections on the home page.

-   **[Monitor Zoom call quality using DEX](https://www.servicenow.com/docs/access?context=monitor-zoom-call-quality-using-dex&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

Admins can view detailed metrics for Zoom calls made by users assigned to this device or who logged in within the past 15 days. The metrics include call quality, network performances, and call details enabling faster troubleshooting and improved end-user experience visibility.

-   **[View Zoom room metrics](https://www.servicenow.com/docs/access?context=view-zoom-room-metrics&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

Using DEX for Zoom, admins can monitor Zoom Room performance across their organization, view issues in each room, and analyze root causes to promote consistent meeting experiences.

-   **[Added new remedial actions](https://www.servicenow.com/docs/access?context=dex-diff-ra&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

The DEX base system includes the following new remedial actions:

    -   Add a registry key \(Windows\)
    -   Clear Google Chrome browsing data \(macOS and Windows\)
    -   Clear Recycle Bin \(macOS and Windows\)
    -   Configure device power scheme \(macOS and Windows\)
    -   Delete Network Drive \(Windows\)
    -   Delete a file \(Windows\)
    -   Elevate temporary admin access \(macOS and Windows\)
    -   Map Network Drive \(Windows\)
    -   Modify USB storage access: Execute \(Windows\)
    -   Modify USB storage access: Read \(Windows\)
    -   Modify USB storage access: Write \(Windows\)
    -   Modify a registry key value \(Windows\)
    -   Remediate Zscaler connectivity \(macOS and Windows\)
    -   Repair corrupt Outlook files \(macOS and Windows\)
    -   Reset Google Chrome browser settings \(macOS and Windows\)
    -   Restart Audio Services \(Windows\)
    -   Restart Microsoft OneDrive \(macOS and Windows\)
    -   Restart Microsoft Outlook \(Windows\)
    -   Updated the Clear application cache remedial action to enable selecting the Microsoft Teams application, helping improve Teams performance.
-   **[Enhanced metric rule experience](https://www.servicenow.com/docs/access?context=create-metric-rules&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

DEX administrators can now manage all types of proactive rules \(both metric and configuration-based\) within a unified interface, streamlining rule management across the DEX system.

-   **[AI-powered root cause analysis for Zoom call quality issues](https://www.servicenow.com/docs/access?context=investigate-and-resolve-zoom-call-issues&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

Use Now Assist for Zoom call issues to identify the root cause of call quality degradation and review the supporting metric evidence for deeper insight. The analysis highlights the contributing device and network factors directly in the Zoom call quality view. Get the real-time guidance, including device ready remedial actions, contextual self-help instructions, and relevant knowledge articles to help resolve the issue efficiently.

-   **[Get AI driven insights for boot time performance](https://www.servicenow.com/docs/access?context=investigate-and-resolve-boot-time-issues&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

Monitor device boot time to identify slow start-up issues and use Now Assist to investigate the root cause and get suggested resolutions, including remedial actions, self-help instructions, and knowledge articles to resolve boot performance problems quickly.

-   **[View GPU device metric details](https://www.servicenow.com/docs/access?context=user-device-metrics&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

Monitor GPU and VRAM \(Video Random Access Memory\) usage on the Device page to assess graphics performance and identify bottlenecks. GPU usage shows the percentage of graphics processing capacity in use, while VRAM usage highlights memory consumption for graphics intensive workloads. These metrics help detect rendering issues, memory intensive applications, and performance degradation enabling faster investigation and resolution of GPU related device problems.


</td></tr><tr><td>

Digital Portfolio Management \(DPM\)

</td><td>

-   **[Configure the Info tab in the DPM Admin Center](https://www.servicenow.com/docs/access?context=dpm-configure-info-tab&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

Show or hide various sections of the **Info** tab for your solutions in DPM.

-   **[Create enterprise service portfolios using a template](https://www.servicenow.com/docs/access?context=dpm-create-enterprise-portfolio-using-template&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

Create enterprise portfolios from scratch or by using a template. Enterprise portfolios are structured in a nesting tree format to facilitate navigation of service-related items and taxonomy nodes. Similar to personal portfolios, you can see key metrics to assess the portfolio performance.

-   **[Configure scheduled email reports in DPM Admin Center](https://www.servicenow.com/docs/access?context=dpm-schedule-email-reports&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

Send periodic emails of KPI metrics to the DPM solution owners. This feature is off by default and can be activated in the DPM Admin Center under a new 'Email properties' section.


</td></tr><tr><td>

Dispute Rules Content Pack for Mastercard

</td><td>

-   **[Decision tables for Mastercard dispute processing](https://www.servicenow.com/docs/access?context=dispute-decision-tables&version=zurich&pubname=zurich-financial-services-operations&ft:locale=en-US)**

Streamline dispute processing by validating Mastercard transaction details and questionnaire answers against the eligibility rules in this application's decision tables.


</td></tr><tr><td>

Dispute Rules Content Pack for Nacha

</td><td>

-   **Decision tables for ACH dispute processing**

Streamline dispute processing by validating ACH transaction details and questionnaire answers against the eligibility rules in the decision tables included in this application.

-   **[Supporting Knowledge Base article](https://www.servicenow.com/docs/access?context=dispute-rules-content-pack-nacha-use&version=zurich&pubname=zurich-financial-services-operations&ft:locale=en-US#section_hm1_13c_xgc)**

Verify chargeback eligibility with the included Knowledge Base article that contains a table of reason codes and chargeback rules.


</td></tr><tr><td>

Document Intelligence

</td><td>

-   **[New third-party AI model provider options available for all Now Assist applications](https://www.servicenow.com/docs/access?context=exploring-large-language-models&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Google Gemini and AWS Claude are available for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.


</td></tr><tr><td>

Document Services

</td><td>

-   **[Document comparison](https://www.servicenow.com/docs/access?context=compare-document-version&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)**

Compare two versions of the document side by side.

-   **[Guardrails for PDF generation and accessibility](https://www.servicenow.com/docs/access?context=guardrails-pdf-generation-accessibility&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)**

Use static and dynamic guardrails to help maintain stability during PDF generation and accessibility.

-   **[Smart Documents](https://www.servicenow.com/docs/access?context=configure-skill-smart-documents&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)**

Accelerate insights with quick summaries, dynamic Q&amp;A, and FAQs that reduce time spent searching for information


</td></tr><tr><td>

Domain Separation

</td><td>

-   ****

Domain Admins may now delete by domain to efficiently manage domains and reduce storage overhead. The tool also includes data recovery and retention, enabling rollbacks and retention policy setting.

-   ****

Changes to the domain table are now queued sequentially and batched into a single background job. This helps simplify domain table updates. Users are notified when a job needs to be delayed as well when a job needs to start.


</td></tr><tr><td>

Dynamic Translation

</td><td>

-   **[Test Exclusion Rule](https://www.servicenow.com/docs/access?context=dyn-translation-test-exclusion-rule&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

Use the new Test Exclusion Rule module to check your exclusion pattern in Dynamic Translation's Exclusion Framework. You can manually test either exact matches or pattern \(regex\) matches. See what your exclusion pattern matches when translating your input into target languages. When you are satisfied with your exclusion pattern, you can create an exclusion rule based on it with just one step.


</td></tr><tr><td>

Employee Center

</td><td>

[Zurich Patch 1](../quality/zurich-patch-1.md)

-   **[Check latest company news and events](https://www.servicenow.com/docs/access?context=check-company-newsevent-ai-agent-for-emp-exp&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

Use the **Company News and Events AI Agent** to enable employees to check their company-related news and any upcoming events using the Now Assist in Virtual Agent.


-   **[Now Assist for Employee Experience Summarization skill](https://www.servicenow.com/docs/access?context=activate-now-assist-skills-uex&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

Enable a summary of the request, requested item, or case for approval task using Now Assist for Employee Experience. The skill provides a summary of the selected item from the available list that you want to work on.


Zurich Early Availability

-   **[Now Assist for Employee Experience plugin](https://www.servicenow.com/docs/access?context=now-assisit-employee-exp&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

Enable employees to resolve and approve tasks easily through chat conversation using the Now Assist for Employee Experience plugin with Now Assist in Virtual Agent.

-   **[Browser Extension for Employee Center](https://www.servicenow.com/docs/access?context=ecbe-intro&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

View and manage content and other company resources through the Browser Extension for Employee Center. Access the extension as a pop-up window, or select the Browser Extension for Employee Center icon on the portal to open it in a new page.

-   **[Enhanced Requests Experience](https://www.servicenow.com/docs/access?context=my-requests-update-intro&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

Enhance the My Requests experience with features like easy segmentation, filtering, and keyword search. These features create a dynamic and scalable experience on the Employee Center portal for your admins, service, process, and experience owners.

-   **[Portal performance optimization](https://www.servicenow.com/docs/access?context=ec-load-experience-optimization&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

Control how your portal pages load, such as all at once or as needed, by using the new deferred and lazy load preferences. Lazy loading is enabled by default and displays content dynamically, reducing page load time.

-   **[High-traffic experience](https://www.servicenow.com/docs/access?context=ec-load-high-traffic&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

Communicate the information about heavy usage and slower network conditions during high usage scenarios, such as live events and major announcements.

-   **[Taxonomy and connected content](https://www.servicenow.com/docs/access?context=track-new-content&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

Streamline the cleanup and syncing of outdated or invalid content, helping admins maintain a high-quality, well-performing portal with less manual effort.

-   **[Mega menu load](https://www.servicenow.com/docs/access?context=config-mega-menu-async-load&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

Load the Mega Menu in the background to speed up home page interactivity and enable your users to engage with visible content faster during first-time visits.

-   **[Notifications for Employee Center enhancements](https://www.servicenow.com/docs/access?context=notifications-ec&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

Get Notifications for Employee Center in Content engagement that is available with Employee Center Pro. For more information, see [Employee Center Pro release notes](../unified-employee-experience/employee-center-pro-rn.md).

-   **[Quick start tests for Employee Center](https://www.servicenow.com/docs/access?context=quick-start-tests-employee-center&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

After upgrades and deployments of new applications or integrations, run quick start tests to verify that Employee Center works as expected. If you customized Employee Center, copy the quick start tests and configure them for your customizations.


</td></tr><tr><td>

Employee Center Pro

</td><td>

-   **[Portal performance optimization](https://www.servicenow.com/docs/access?context=ec-load-experience-optimization&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

Communicate information about heavy usage and slower network conditions during high usage scenarios, such as live events and major announcements.

-   **[Notifications for Employee Center](https://www.servicenow.com/docs/access?context=notifications-ec&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US) enhancements**

Get the Notifications for Employee Center feature in Content engagement. Add reactions and comments to published news articles to help improve user involvement.

-   **[Integrated experience and service feedback](https://www.servicenow.com/docs/access?context=ex-fdback-ovrvw&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

Configure features flexibly as an admin and submit detailed experience feedback as an employee with the Integrated experience and Service feedback enhancements. With the enhancements, you can do the following:

    -   Use new themes for experience feedback.
    -   Add comments in addition to a rating when submitting experience feedback.
    -   Review submitted feedback on the Feedback Analytics Dashboard.
-   **[Quick start tests for Employee Center Pro](https://www.servicenow.com/docs/access?context=quick-start-tests-employee-center-pro&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

After upgrades and deployments of new applications or integrations, run quick start tests to verify that Employee Center Pro works as expected. If you customized Employee Center Pro, copy the quick start tests and configure them for your customizations.


</td></tr><tr><td>

Encryption

</td><td>

-   **[Encrypt data using Row Conditions](https://www.servicenow.com/docs/access?context=encrypt-data-using-row-conditions&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)**

Use row conditions for Field Encryption to define encryption rules for rows within a specific column, based on dynamic conditions.


</td></tr><tr><td>

Encryption Key Management

</td><td>

-   **[Keep track of Field Encryption and Key Management changes](https://www.servicenow.com/docs/access?context=c_UnderstandingTheSysAuditTable&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)**

By default, the changes to the records on these tables are now logged to the Sys Audits \[sys\_audit\] table:

    -   Encrypted Field Configurations \[sys\_platform\_encryption\_configuration\]
    -   Module Access Policies \[sys\_kmf\_crypto\_caller\_policy\]
    -   Cryptographic Modules \[sys\_kmf\_crypto\_module\]
For details on accessing the Sys Audits \[sys\_audit\] table, see [Viewing Sys Audit and Audit Relationship Change tables](https://www.servicenow.com/docs/access?context=c_UnderstandingTheSysAuditTable&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).


</td></tr><tr><td>

Enterprise Architecture

</td><td>

-   **[Application rationalization page enhancements](https://www.servicenow.com/docs/access?context=eaw-rationalize-business-applications&version=zurich&pubname=zurich-application-portfolio-management&ft:locale=en-US)**
    -   View business application bubbles whose X and Y-axis values are within the value range of +/-0.25 of each other as a grouped bubble. The grouped bubble displays the total number of business application bubbles that it contains. This grouping helps in clearing the clutter on bubble chart when there are too many business applications with similar values. For details, see [Bubble chart view of application rationalization](https://www.servicenow.com/docs/access?context=eaw-bubble-chart-view&version=zurich&pubname=zurich-application-portfolio-management&ft:locale=en-US).
    -   Zoom in, zoom out, or pan on the Bubble chart page using either on-screen buttons or by using a mouse device or trackpad interactions. For details, see [Bubble chart view of application rationalization](https://www.servicenow.com/docs/access?context=eaw-bubble-chart-view&version=zurich&pubname=zurich-application-portfolio-management&ft:locale=en-US).
    -   View the calculation logic behind the total number of business applications displayed on the Bubble chart page. For details, see [Bubble chart view of application rationalization](https://www.servicenow.com/docs/access?context=eaw-bubble-chart-view&version=zurich&pubname=zurich-application-portfolio-management&ft:locale=en-US).
    -   Select a single bubble on the Bubble chart page to view the associated business application details. Select a grouped bubble to view the list of business applications that are part of that grouped bubble. For details, see [Bubble chart view of application rationalization](https://www.servicenow.com/docs/access?context=eaw-bubble-chart-view&version=zurich&pubname=zurich-application-portfolio-management&ft:locale=en-US).
    -   View actual scores of business applications and compare them with their normalized scores. For details, see [List view of application rationalization](https://www.servicenow.com/docs/access?context=eaw-list-view&version=zurich&pubname=zurich-application-portfolio-management&ft:locale=en-US).
    -   Increased maximum number of bubbles displayed on the Bubble chart to 500.
    -   Apply the fiscal period filter to filter and view business applications for a specific fiscal period.
    -   Apply the application rationalization filters to filter and view specific business applications on the bubble chart or list view page. An indicator is displayed on top of the filter icon to show the number of filters currently applied.
    -   View the business application technical debt indicator score on the application rationalization list view page. On the application rationalization bubble chart view page, you can use the TRM technical debt indicator to form the bubble size based on the indicator score.
    -   Export the list view of application rationalization data to Excel or CSV file format. You can use the data to obtain insights, share with stakeholders, and prepare for analysis.
    -   Business applications with Retired or End of Life lifecycle stage aren’t displayed on the Application Rationalization bubble chart page.

-   **[Data certification in Enterprise Architecture Workspace](https://www.servicenow.com/docs/access?context=eaw-work-with-data-cert&version=zurich&pubname=zurich-application-portfolio-management&ft:locale=en-US)**
    -   Use the Data Certification workflow in Enterprise Architecture Workspace to ensure the accuracy, completeness, and reliability of critical data within your organization. For details, see [Exploring data certification in the Enterprise Architecture Workspace](https://www.servicenow.com/docs/access?context=eaw-explore-data-cert&version=zurich&pubname=zurich-application-portfolio-management&ft:locale=en-US).
    -   Create a data certification policy directly from the Enterprise Architecture Workspace using the Data certification workflow. For details, see [Create a certification policy](https://www.servicenow.com/docs/access?context=eaw-create-policy&version=zurich&pubname=zurich-application-portfolio-management&ft:locale=en-US).
    -   Run certification on demand for published policies to generate a new certification instance for an active policy. For details, see [Run certification for a policy](https://www.servicenow.com/docs/access?context=eaw-data-cert-run-certification&version=zurich&pubname=zurich-application-portfolio-management&ft:locale=en-US).
    -   Activate a certification policy to add it to the active certification runs. This process ensures that the policy is active and can be used for certifications. You can deactivate a policy to remove it from active certification runs. For details, see [Activate a certification policy](https://www.servicenow.com/docs/access?context=eaw-data-cert-activate&version=zurich&pubname=zurich-application-portfolio-management&ft:locale=en-US).
-   **[Enterprise Architecture Workspace home page enhancements](https://www.servicenow.com/docs/access?context=eaw-work-with-ea-workspace-homepage&version=zurich&pubname=zurich-application-portfolio-management&ft:locale=en-US)**

Apply the Portfolio Overview and Health filters to filter and view specific business applications and business capabilities information. An indicator is displayed on top of the filter icon to show the number of filters currently applied.

-   **[Manage Enterprise Modeling and Visualization](https://www.servicenow.com/docs/access?context=eaw-config-modeling&version=zurich&pubname=zurich-application-portfolio-management&ft:locale=en-US)**
    -   Create a diagrams using CSDM shapes to ensure consistency in how services, applications, and infrastructure are represented. Aligning with CMDB 5 standards, helps you in accurate reporting, impact analysis, and compliance across the enterprise. For details, see [Common Service Data Model \(CSDM\) shapes](https://www.servicenow.com/docs/access?context=eaw-modeling-csdm-shapes&version=zurich&pubname=zurich-application-portfolio-management&ft:locale=en-US).
    -   Use the modified Enterprise Architecture shapes that are aligned with CSDM 5 standards for better modeling, accurate impact analysis, and reporting. For details, see [Create a diagram using CSDM shapes](https://www.servicenow.com/docs/access?context=eaw-modeling-create-diagram-csdm&version=zurich&pubname=zurich-application-portfolio-management&ft:locale=en-US).
    -   Create diagrams using AWS shapes. The AWS shapes enable you to visualize AWS cloud components, model hybrid architectures, support cloud migration planning. For details, see [Amazon Web Services \(AWS\) shapes](https://www.servicenow.com/docs/access?context=eaw-modeling-aws-shapes&version=zurich&pubname=zurich-application-portfolio-management&ft:locale=en-US) and [Create a diagram using AWS shapes](https://www.servicenow.com/docs/access?context=eaw-modeling-create-diagram-aws&version=zurich&pubname=zurich-application-portfolio-management&ft:locale=en-US).
    -   Group or ungroup a general shape object. You can combine multiple related shapes into a single container for better organization and clarity in diagrams. For details, see [Convert a shape to a group shape](https://www.servicenow.com/docs/access?context=eaw-modeling-group-ungroup-shape&version=zurich&pubname=zurich-application-portfolio-management&ft:locale=en-US).
    -   Expand or collapse a group shape to simplify visualization, improve focus, and supports hierarchical modeling. For details, see [Expand or collapse a group shape](https://www.servicenow.com/docs/access?context=eaw-modeling-expand-collapse-shape&version=zurich&pubname=zurich-application-portfolio-management&ft:locale=en-US).
    -   View Business Process details for which the BPMN diagram is being created. Modify details such as name, parent, and description. For details, see [Modify BPMN diagram details](https://www.servicenow.com/docs/access?context=eaw-modeling-modify-bpmn&version=zurich&pubname=zurich-application-portfolio-management&ft:locale=en-US).
    -   Reorder shape categories within the Shapes panel to customize the panel for faster access to frequently used shapes. For details, see [Reorder shapes categories](https://www.servicenow.com/docs/access?context=eaw-modeling-reorder-shapes-cat&version=zurich&pubname=zurich-application-portfolio-management&ft:locale=en-US).
    -   Show or hide the Shapes panel to optimize your workspace for different tasks. For details, see [Show or hide shapes panel](https://www.servicenow.com/docs/access?context=eaw-modeling-show-hide-shapes-panel&version=zurich&pubname=zurich-application-portfolio-management&ft:locale=en-US).
    -   Switch between List view and Grid view in the shapes panel according to your modeling needs. For details, see [Switch to list or grid view of shapes panel](https://www.servicenow.com/docs/access?context=eaw-modeling-shapes-grid-list-view&version=zurich&pubname=zurich-application-portfolio-management&ft:locale=en-US).
    -   Download a diagram as an image to share it with other stakeholders with offline access or use it in the presentations. For details, see [Download a modeling diagram as an image](https://www.servicenow.com/docs/access?context=eaw-modeling-download-diagram&version=zurich&pubname=zurich-application-portfolio-management&ft:locale=en-US).
    -   Select and delete diagrams from the Diagrams page.
    -   Select upstream or downstream entities when adding related records for shapes. The upstream entities appear as a parent for the selected shape in the diagram while the downstream entities appear as a child for the selected shape in the diagram.
    -   Add version label, version description, and planned rollout date details for diagram versions.
    -   On duplicating a business process map, you can choose to associate the duplicated process map with a new or an existing business process.
    -   Added support for shapes that enable AI governance. The shapes are added under the Enterprise Architecture category in the shapes palette. The shapes are:
        -   AI Dataset Digital Asset
        -   AI Model Digital Asset
        -   AI Prompt Digital Asset
        -   AI System Digital Asset
    -   Perform undo and redo actions using buttons on the diagram page or using keyboard shortcuts.
    -   Resize the shapes added to a canvas.
    -   Drag shapes from the **Shapes** palette on to the canvas.
    -   Add labels on the connector lines between shapes in a diagram.
    -   Create diagrams for business process maps using the specific shapes related to the business processes.
    -   Search shapes within the shape libraries.
    -   Reorganize the order of shapes in a shape library according to your requirement.
    -   Show or hide shapes in different diagram types.
    -   General shapes can be rotated.
    -   Enhanced the overall appearance of the diagram by hiding the connector ports and displaying them only when hovering over the shapes.
    -   Open the Enterprise Modeling and Visualization diagrams from the following sections:
        -   From the Architectural Artifacts related list of a business application, business capability, or a business process record.
        -   From the **My approvals** tab of the Needs Attention section on the EA Workspace home page.
        -   From the Architectural Artifacts section of the Portfolio page.
    -   Added support for all ArchiMate shapes.
    -   Model Value stream diagrams.
-   **[TRM catalog enhancement](https://www.servicenow.com/docs/access?context=eaw-export-trm-prod-cat-data&version=zurich&pubname=zurich-application-portfolio-management&ft:locale=en-US)**

Export the TRM catalog data to Microsoft Excel or CSV format.

-   **[Business Portfolio enhancement](https://www.servicenow.com/docs/access?context=eaw-export-business-portfolio-data&version=zurich&pubname=zurich-application-portfolio-management&ft:locale=en-US)**

Export the Business Portfolio data to Microsoft Excel or CSV format.

-   **[TRM category enhancements](https://www.servicenow.com/docs/access?context=eaw-create-new-trm-category&version=zurich&pubname=zurich-application-portfolio-management&ft:locale=en-US)**

Assign an owner to a TRM category to ensure clear accountability and improved governance standards. The owner is responsible for maintaining consistent technology compliance standards for that TRM category.

-   **[TPM lifecycle record enhancements](https://www.servicenow.com/docs/access?context=eaw-tpm&version=zurich&pubname=zurich-application-portfolio-management&ft:locale=en-US)**
    -   TPM lifecycle records are now assigned unique identifiers are automatically,while creating the TPM lifecycle record. These identifiers serve as clickable links that provide direct access to full record details.
    -   Run the Populate Number field in TPM Discovered Technologies scheduled job to populate the TPM lifecycle record identifiers of existing records created using previous versions \(before version 1.9.0\) of the TPM plugin. For details, [Run a scheduled job to populate Technology Portfolio Management lifecycle record identifier](https://www.servicenow.com/docs/access?context=eaw-run-job-to-populate-tpm-lifecycle-identifier&version=zurich&pubname=zurich-application-portfolio-management&ft:locale=en-US).
-   **[Working with Portfolio list view](https://www.servicenow.com/docs/access?context=eaw-work-with-portfolio-list-view&version=zurich&pubname=zurich-application-portfolio-management&ft:locale=en-US)[AI Portfolio section enhancements](https://www.servicenow.com/docs/access?context=eaw-exploring-the-ai-portfolio&version=zurich&pubname=zurich-application-portfolio-management&ft:locale=en-US)**

The following AI product models added to the AI Portfolio section:

    -   AI System Product Models
    -   AI Model Product Models
    -   AI Dataset Product Models
    -   AI Prompt Product Models
-   **[Business application related list enhancements](https://www.servicenow.com/docs/access?context=eaw-app-portfolio&version=zurich&pubname=zurich-application-portfolio-management&ft:locale=en-US)**

Added the AI Product Models as a related list. In the tab, you can:

    -   Select **Add** to associate an existing AI system product model to the business application.
    -   Select **Remove** to remove a AI system product model from a business application.
For details, see [Add AI systems to business applications](https://www.servicenow.com/docs/access?context=eaw-add-ai-systems&version=zurich&pubname=zurich-application-portfolio-management&ft:locale=en-US).

    -   Added the **Product capability** tab as a related list. In the tab, you can:
        -   Select **New** to create a new product capability and associate it with the business application.
        -   Select **Add** to add an existing product capability to the business application.
        -   Select **Remove** to remove a product capability from a business application.
    -   Added the TRM products tab as a related list. In the tab, you can:
        -   Select **New** to create a new TRM product and associate it with the business application.
        -   Select **Add** to add an existing TRM product to the business application.
        -   Select **Remove** to remove a TRM product from a business application.
    -   In the **Architectural Artifacts** tab of the business application related list, selecting the **New** button displays a modal to create an architectural artifact.
-   **[TRM product related list enhancements](https://www.servicenow.com/docs/access?context=eaw-work-with-trm&version=zurich&pubname=zurich-application-portfolio-management&ft:locale=en-US)**
    -   Added the **Product capability** tab as a related list. In the tab, you can:
        -   Select **New** to create a new product capability and associate it with the TRM product.
        -   Select **Add** to add an existing product capability to the TRM product.
        -   Select **Remove** to remove a product capability from a TRM product.
    -   Added the **Business Applications** tab as a related list. In the tab, you can:
        -   Select **New** to create a new business application and associate it with the TRM product.
        -   Select **Add** to add an existing business application to the TRM product.
        -   Select **Remove** to remove a business application from a TRM product.
-   **[Architectural Decision Records \(ADR\) enhancements](https://www.servicenow.com/docs/access?context=eaw-managing-arch-decision-records&version=zurich&pubname=zurich-application-portfolio-management&ft:locale=en-US)**
    -   Create artifact type Architectural Decision Records \(ADR\) in one step.
    -   Create and add multiple pages to the Architectural Decision Records \(ADR\) from the **Artifact content** tab.
    -   In the Architectural Decision Records \(ADR\) page, you can tag the following:
        -   Tag a user
        -   Tag a record
            -   Architectural artifact
            -   Business application
            -   Business capability
            -   Business process
            -   Digital integration \(requires the digital integration plugin\)
            -   Digital interface \(requires the digital integration plugin\)
            -   Information object
            -   TRM product \(requires the TRM plugin\)
            -   Value stream \(requires the value stream plugin\)
    -   Request approval workflow for Architectural Decision Records \(ADR\).
    -   The version drop-down list is added to the Architectural Decision Records \(ADR\) page header. Select a version from the drop-down list to open the specific ADR version.
-   **[Data Certification changes](https://www.servicenow.com/docs/access?context=eaw-config-cert-schedules&version=zurich&pubname=zurich-application-portfolio-management&ft:locale=en-US)**

In the Enterprise Architecture Workspace, the certifications data is saved to and fetched from the CMDB Data Management Task Control \[cmdb\_data\_management\_task\] table.

If your certification data is still fetched from the Certification Schedules \[cert\_schedule\] table, you might consider migrating your certification policies to the CMDB Data Management Task Control \[cmdb\_data\_management\_task\] table. For more information, see [Convert legacy certification schedules into Data Manager Certification policies](https://www.servicenow.com/docs/bundle/yokohama-servicenow-platform/page/product/configuration-management/task/convert-data-cert-definitions.html)and[Publish a draft Data Manager policy in CMDB Workspace](https://www.servicenow.com/docs/bundle/yokohama-servicenow-platform/page/product/configuration-management/task/data-manager-publish-draft-policy.html%22%20HYPERLINK%20%22https:/www.servicenow.com/docs/bundle/yokohama-servicenow-platform/page/product/configuration-management/task/data-manager-publish-draft-policy.html).


</td></tr><tr><td>

Enterprise Asset Management

</td><td>

-   **[Organize your assets into hierarchical asset groups to manage your complex asset ecosystems](https://www.servicenow.com/docs/access?context=asset-groups-eam&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

Organize assets into logical groups and subgroups to represent their dependencies and operational relationships. Use a dependency map to visualize the entire structure of the asset hierarchy, making it easy to see all the subgroups and assets within each asset group.

-   **[Inspect the condition of enterprise assets to determine their health and ensure reliability](https://www.servicenow.com/docs/access?context=asset-conditions-eam&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

Define condition attributes for enterprise models and assets and associate these attributes with templates to identify any potential issues throughout the asset life cycle. Enable scoring in the templates to calculate asset condition scores to determine whether an asset passes or fails the evaluation. Schedule asset condition evaluations via maintenance plans or work orders. View comprehensive reports on the asset condition outcomes on dashboards across your organization.

-   **[Optimize your operations with asset performance reports](https://www.servicenow.com/docs/access?context=eam-asset-dboard&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

Track the past performance of assets and get notified about trends, threshold breaches, or anomalies based on their location, model category, model, or classification. This tracking helps improve asset availability according to ISO standards.

-   **[Monitor supply and demand of assets in a stockroom with detailed inventory reports](https://www.servicenow.com/docs/access?context=manage-stockroom-inventory-reports&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

Track and manage stockrooms efficiently by evaluating the inventory reports in the Inventory view of the Enterprise Asset Workspace. These reports help you:

    -   Find replacement options or spare part availability for assets that are in use, being repaired, or in maintenance
    -   Quickly identify shortages and align current demand in your stockroom with both current and incoming supply
    -   Analyze the supply to meet open demand across all stockrooms or locations
-   **[Achieve faster diagnostics and enhanced maintenance efficiency with standardized failure and resolution codes](https://www.servicenow.com/docs/access?context=failure-resolution-codes-eam&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

Enable technicians to record predefined failure reasons and resolution steps with configurable codes. You can create, update, and import these codes through spreadsheets in the Admin center of the Enterprise Asset Workspace. In the Repair flow, these codes help technicians record the reason for the specific issue with the asset and the appropriate solution for repairing it.

-   **[Manage OT hardware models and assets in the OT Asset Workspace](https://www.servicenow.com/docs/access?context=ot-asset-ws-otam&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

Enable OT asset managers to view and fulfill requests for OT hardware assets in the OT Asset Workspace. The reports and dashboards in the OT Asset workspace include OT hardware models, assets, and requests. The following OT Asset Management workflows and features now provide support for OT hardware assets and models, in addition to the workflows and features that continue to support them from the Yokohama release:

    -   Bulk import
    -   Asset reclamation
    -   Advanced Shipment Notification \(ASN\)
    -   Asset audits
    -   Total Cost of Ownership \(TCO\)
    -   Lease contract
    -   Risk
    -   Resale
    -   Loaner
    -   Move
    -   Recall
    -   Stock rule
-   **[Remediate unsuccessful enterprise asset calibrations](https://www.servicenow.com/docs/access?context=remediate-unsuccessful-enterprise-asset-calibration&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

Remediate failed calibration events by initiating new work orders and corresponding work order tasks for those events. When you select the option to remediate a failed calibration event, you can choose an appropriate work order template to generate a new work order with at least one work order task. The work order and work order task are auto-populated with the asset that you want to calibrate, the location of that asset, the original work order, and all mandatory fields. In addition, the original and new calibration events and their corresponding tasks are linked together through the **Parent** field for full traceability.

-   **[Measure calibration tolerance conformance by using additional value types](https://www.servicenow.com/docs/access?context=add-calibration-attributes-enterprise-model&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

Use the following additional value types to compare your calibration measurements against the corresponding tolerances that you define:

    -   Range
    -   Less than
    -   Greater than
In addition, use the True/False value type to assess the qualitative elements of your calibrations.

-   **[Manage unique identifiers for enterprise assets using CI identification rules](https://www.servicenow.com/docs/access?context=create-asset-eam&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

Define required and unique fields on asset records by creating identification rules on associated CI classes in the Identification and Reconciliation engine \(IRE\). When you create an asset whose model category is linked to a CI class with an identification rule, you should provide details for at least one of the fields, such as Asset tag, Serial number, and MAC address, that uniquely identify the asset.

-   **[Drop off and receive assets at a stockroom by using the ServiceNow Mobile Agent application](https://www.servicenow.com/docs/access?context=manage-dropoff-mobile-agent&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

Return the assets that you have in your personal stockroom to a different stockroom by creating a Drop off task using the ServiceNow® Mobile Agent application. The asset manager of the destination stockroom receives the assets that you dropped off through a Receive task. The asset manager then verifies the received assets and closes the Drop off task using the Mobile Agent application.

**Note:** Starting with the Xanadu release, you could create Drop off and Receive tasks in the Enterprise Asset Workspace. However, now you can also use the Mobile Agent application for the same purpose.

-   **[Receive shipment assets at a stockroom through the streamlined and unified receiving process](https://www.servicenow.com/docs/access?context=stockroom-receiving-eam&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

Receive assets from any workﬂow directly at the stockroom using the unified receiving functionality in the following workspaces:

    -   Enterprise Asset Workspace
    -   OT Asset Workspace
    -   Medical Asset Workspace
    -   Facility Asset Workspace
This standardized receiving process reduces the time spent on receiving assets. By requiring each asset to be assigned a unique identiﬁer when received at the stockroom, the quality of asset data also improves.

You can receive assets in bulk by using a template. Additionally, you can view the results and validation comments in the staging table. During this process, the system handles existing assets, creates new ones as needed, and performs comprehensive validations.

-   **[Track asset movement from the receiving bay to an aisle-space in the stockroom](https://www.servicenow.com/docs/access?context=managing-inventory-by-putting-away-asset-eam&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

Move assets from the receiving bay to their designated aisle and space and improve asset tracking and inventory management by using the Asset put away feature. This task can be performed via the Enterprise Asset Workspace or ServiceNow Agent application.


</td></tr><tr><td>

Event Management

</td><td>

-   **[Mixed alert grouping](https://www.servicenow.com/docs/access?context=alert-group-use-cases&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

Combine CMDB-based and tag-based alert grouping strategies into cohesive groups that reduce noise, enabling faster and more effective response.

-   **[AIOps 360 overview dashboard](https://www.servicenow.com/docs/access?context=aiops-360-overview-dashboard&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

Gain actionable insights with a 360-degree dashboard that showcases product value, tracks operational efficiency, and highlights automation impact. Monitor alert handling, service health, and AIOps outcomes to drive smarter, faster decisions across IT operations.

-   **[Mixed alert grouping in Service Operations Workspace](https://www.servicenow.com/docs/access?context=group-alert-sow-itom&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

Choose how you want to group alerts from the **Criteria Type** field. Use the **Related CIs** option to combine CMDB-based and tag-based alert grouping.

-   **[Application services for impact calculation](https://www.servicenow.com/docs/access?context=c_EMImpactCalculation&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

Filter the application services to be considered in impact calculation for focused and accurate results.

-   **[Metric connector in Integrations Launchpad](https://www.servicenow.com/docs/access?context=configure-metric-pull-connector&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

Configure metric pull connectors to automate data retrieval and seamlessly integrate external metrics for efficient monitoring.

-   **[View links between alerts in new alert groups in Express List®](https://www.servicenow.com/docs/access?context=el-link-view&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US).**

Starting in version 26.9.0, investigate alert group details and visualize connections through Link View in Express List®, now available for log analytics-based alert groups and mixed alert groups.

-   **[Anomaly information for log analytic based alerts and metric intelligence alerts in preview panel in Express List®.](https://www.servicenow.com/docs/access?context=view-anomaly-alert-display&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

Starting in version 26.9.0, review visualizations for anomaly information in log analytic-based alerts and metric intelligence alerts in the preview panel in Express List\[var.express-reg-tm\].

-   **[Configure new property for automatic resume of the live list updates following a pause, and conﬁgure time ranges in Express List®](https://www.servicenow.com/docs/access?context=express-list&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

Starting in version 26.9.0, admins gain the ability to conﬁgure the amount of time until the live list updates resume, after being paused in Express List®. Admins are also able to customize the time range options displayed in Express List®, such as the default time range.

-   **Centralized management with the ITOM AIOps configuration center**

Starting in version 26.11.0, the ITOM AIOps configuration center provides a centralized hub to manage AIOps settings, helping you integrate monitoring tools, optimize alerts, metrics, and logs, and manage services, dashboards, teams, and authorizations for improved visibility and operational efficiency.

-   **Added Recommended category for AIOps 360 Overview dashboards**

Starting in version 26.11.0, added a **Recommended** category to all officially released dashboards such as AIOps 360 Overview dashboard, AIOps Value Realization dashboard, to help you easily identify and access ITOM-approved dashboards.

-   **Add a delay for incident creation from alerts**

Starting in version 26.11.0, you can add a delay in Respond Automation before incidents are created from alerts, allowing alerts to auto-close if resolved and helping reduce unnecessary incident creation.

-   **Added support for multiple subscriptions of AWS account**

Starting in version 2.17.1, added support to enable multiple member accounts to forward CloudWatch/EventBridge events to a centralized account, where a single SNS topic delivers them to the ServiceNow Event Ingestion endpoint, reducing manual setup from multiple configurations to one and cutting onboarding effort by up to 90%.

-   **Configure Dynatrace metric connector from Integrations Launchpad**

Starting in version 2.17.1, you can use the Dynatrace metric connector from the Integrations Launchpad to bring metrics from Dynatrace into ServiceNow Metric Intelligence for visualization, enrichment, dynamic thresholds, and anomaly detection.

-   ****

Starting in version 2.17.1, you can use the out-of-the-box Datadog metric connector to integrate Datadog metrics with ServiceNow Metric Intelligence, enabling anomaly detection, metric visualization, enrichment, and correlation of metric anomalies with events and log alerts.

-   ****

Starting in version 2.17.1, you can use the new Kafka connector to stream time-series metric data from Kafka topics into ServiceNow Metric Intelligence for real-time monitoring, anomaly detection, and alerting.

-   **ITOM  guided setup**

Starting in 27.2.1, introduced ITOM Event Management guided setup, providing a sequence of tasks that help you install and get started with Event Management efficiently.

-   **[Live updates functionality has been updated in the Service Operation Workspace Lists.](https://www.servicenow.com/docs/access?context=configure-alert-list-autofresh-settings&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

Starting in version 26.11.0, a new toggle switch allows users to enable or disable live updates. When the toggle is set to on, alerts are updated automatically. When the toggle is set to off, a badge displays the number of available updates until the page is refreshed manually. The setting is saved for future logins by the same user.

-   **[Explore the new Dependency view for an alert](https://www.servicenow.com/docs/access?context=dependency-maps&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

Starting in version 26.11.0, explore the new Dependency view for an alert. Access maps from the following locations:

    -   in the preview panel, in the Configuration item section for the CI topology
    -   in the Utilities panel of the alert record
    -   in the action drop-down menu
    -   in the Core UI alert form
-   **[Respond to multiple alerts in Express List](https://www.servicenow.com/docs/access?context=bulk-alert-response-express-list&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

Starting in version 26.11.0, run response actions on multiple alerts at the same time in Express List.


</td></tr><tr><td>

External Content Connectors

</td><td>

-   **[Adobe Acrobat Sign external content connector](https://www.servicenow.com/docs/access?context=adobe-acrobat-sign-external-content-connector&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

Retrieve searchable content and metadata from your Adobe Acrobat Sign source system.

-   **[Aha! Roadmaps external content connector](https://www.servicenow.com/docs/access?context=aha-roadmaps-external-content-connector&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

Retrieve searchable content and metadata from your Aha! Roadmaps source system.

-   **[Cornerstone external content connector](https://www.servicenow.com/docs/access?context=cornerstone-external-content-connector&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

Retrieve searchable content and metadata from your Cornerstone source system.

-   **[Fluid Topics external content connector](https://www.servicenow.com/docs/access?context=fluid-topics-external-content-connector&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

Retrieve searchable content and metadata from your Fluid Topics source system.

-   **[ManageEngine external content connector](https://www.servicenow.com/docs/access?context=manageengine-external-content-connector&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

Retrieve searchable content and metadata from your ManageEngine source system.

-   **[Workvivo external content connector](https://www.servicenow.com/docs/access?context=workvivo-external-content-connector&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

Retrieve searchable content and metadata from your Workvivo source system.


-   **[Connector admin role](https://www.servicenow.com/docs/access?context=installed-with-ext-content-connectors&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

Users with the sn\_ext\_conn.xcc\_admin role can create, configure, and review details for external content connectors and crawls.

-   **[Adobe Experience Manager as a Cloud Service external content connector](https://www.servicenow.com/docs/access?context=adobe-expmgr-cs-external-content-connector&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

Retrieve searchable content and metadata from your Adobe Experience Manager as a Cloud Service source system.

-   **[Asana external content connector](https://www.servicenow.com/docs/access?context=asana-external-content-connector&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

Retrieve searchable content and metadata from your Asana source system.

-   **[Docusign external content connector](https://www.servicenow.com/docs/access?context=docusign-external-content-connector&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

Retrieve searchable content and metadata from your Docusign source system.

-   **[Dropbox external content connector](https://www.servicenow.com/docs/access?context=dropbox-external-content-connector&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

Retrieve searchable content and metadata from your Dropbox source system.

-   **[GitHub Enterprise Cloud external content connector](https://www.servicenow.com/docs/access?context=github-enterprise-cloud-external-content-connector&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

Retrieve searchable content and metadata from your GitHub Enterprise Cloud source system.

-   **[HubSpot external content connector](https://www.servicenow.com/docs/access?context=hubspot-external-content-connector&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

Retrieve searchable content and metadata from your HubSpot source system.

-   **[Lucidchart external content connector](https://www.servicenow.com/docs/access?context=lucidchart-external-content-connector&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

Retrieve searchable content and metadata from your Lucidchart source system.

-   **[Miro external content connector](https://www.servicenow.com/docs/access?context=miro-external-content-connector&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

Retrieve searchable content and metadata from your Miro source system.

-   **[monday.com external content connector](https://www.servicenow.com/docs/access?context=monday-com-external-content-connector&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

Retrieve searchable content and metadata from your monday.com source system.

-   **[Notion external content connector](https://www.servicenow.com/docs/access?context=notion-external-content-connector&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

Retrieve searchable content and metadata from your Notion source system.

-   **[SAP DMS external content connector](https://www.servicenow.com/docs/access?context=sap-dms-external-content-connector&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

Retrieve searchable content and metadata from your SAP DMS source system.

-   **[Smartsheet external content connector](https://www.servicenow.com/docs/access?context=smartsheet-external-content-connector&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

Retrieve searchable content and metadata from your Smartsheet source system.

-   **[Trello external content connector](https://www.servicenow.com/docs/access?context=trello-external-content-connector&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

Retrieve searchable content and metadata from your Trello source system.

-   **[WordPress external content connector](https://www.servicenow.com/docs/access?context=wordpress-external-content-connector&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

Retrieve searchable content and metadata from your WordPress source system.

-   **[Workday external content connector](https://www.servicenow.com/docs/access?context=workday-external-content-connector&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

Retrieve searchable content and metadata from your Workday source system.

-   **[Zoom external content connector](https://www.servicenow.com/docs/access?context=zoom-external-content-connector&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

Retrieve searchable content and metadata from your Zoom source system.

-   **[Configure user permission settings for an external content connector](https://www.servicenow.com/docs/access?context=configure-user-mapping-settings-external-content-connector&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

Specify the source system and User \[sys\_user\] table fields to examine for matches when an external content connector maps source system users to your ServiceNow AI Platform users.

-   **[Statistics for external content connector content crawls](https://www.servicenow.com/docs/access?context=document-statistics-external-content-connectors&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

Review statistics about the documents \(items or files with searchable content and metadata\) retrieved by a content crawl.

-   **[Statistics for external content connector user permission crawls](https://www.servicenow.com/docs/access?context=permission-statistics-external-content-connectors&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

Review statistics about the permissions \(user and group-membership security principals\) retrieved by a user permission crawl.

-   **[Analytics for external content connectors](https://www.servicenow.com/docs/access?context=analytics-external-content-connectors&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

Review metrics that show how your external content connector has run over time.


-   **[Amazon S3 external content connector](https://www.servicenow.com/docs/access?context=amazon-s3-external-content-connector&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

Retrieve searchable content and metadata from buckets in your Amazon S3 source system.

-   **[Box external content connector](https://www.servicenow.com/docs/access?context=box-external-content-connector&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

Retrieve searchable content and metadata from user boxes in your Box source system.

-   **[GitLab external content connector](https://www.servicenow.com/docs/access?context=gitlab-external-content-connector&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

Retrieve searchable content and metadata from issues, wikis, merge requests, tags, branches, and commits in your GitLab source system's groups, projects, and repositories.

-   **[Microsoft OneDrive external content connector](https://www.servicenow.com/docs/access?context=microsoft-onedrive-external-content-connector&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

Retrieve searchable content and metadata from individual drives in your Microsoft OneDrive source system.

-   **[Microsoft Viva Engage external content connector](https://www.servicenow.com/docs/access?context=microsoft-viva-engage-external-content-connector&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

Retrieve searchable content and metadata from conversations in your Microsoft Viva Engage source system's communities.

-   **[ServiceNow® instance external content connector](https://www.servicenow.com/docs/access?context=servicenow-instance-external-content-connector&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

Retrieve searchable content and metadata from KB articles in your ServiceNow AI Platform instance.

-   **[Webcrawler external content connector](https://www.servicenow.com/docs/access?context=webcrawler-external-content-connector&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

Retrieve searchable content and metadata from pages and subdomains in public web sources. Select a predefined web source or specify a custom web source.

-   **[Zendesk Guide external content connector](https://www.servicenow.com/docs/access?context=zendesk-guide-external-content-connector&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

Retrieve searchable content and metadata from articles in your Zendesk Guide source system's knowledge bases.

-   **[Statistics for external content connector content crawls](https://www.servicenow.com/docs/access?context=document-statistics-external-content-connectors&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

Review statistics for searchable items retrieved by a content crawl.

-   **[Statistics for external content connector user permission crawls](https://www.servicenow.com/docs/access?context=permission-statistics-external-content-connectors&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

Review statistics for user and group permissions retrieved by a user permission crawl.


</td></tr><tr><td>

Field Service Management

</td><td>

-   **[Using Dispatcher Workspace](https://www.servicenow.com/docs/access?context=using-dispatcher-workspace&version=zurich&pubname=zurich-field-service-management&ft:locale=en-US)**

Use Dispatcher Workspace to perform the following tasks:

    -   Use the advanced resource filter to sort contractors and equipment.
    -   Add agents to Dispatcher Workspace to see their schedules, or assign them tasks if you manage the assignment group or territory they're a part of. This action can be done without loading the entire assignment group or territory that the agent is a member of.
    -   Set up the calendar to use multiple time zones at once. For more information, see [Show multiple time zones at once in Dispatcher Workspace](https://www.servicenow.com/docs/access?context=use-stacked-time-zones&version=zurich&pubname=zurich-field-service-management&ft:locale=en-US).
    -   Navigate from a work order task to a related list of smart assessments that are associated with that work order.
-   **[Assigning work order tasks to agents manually](https://www.servicenow.com/docs/access?context=c_DispatchWorkOrderTasks&version=zurich&pubname=zurich-field-service-management&ft:locale=en-US)**

Use the records page to perform the following tasks that was limited to Dispatcher Workspace before:

    -   Flag a work order task.
    -   Use assignment assistance.
-   **[Schedule Optimization](https://www.servicenow.com/docs/access?context=schedule-optimization-engine&version=zurich&pubname=zurich-field-service-management&ft:locale=en-US)**

Use Schedule Optimization to do the following:

    -   Initiate immediate optimization to adjust schedules and tasks when an in-day event occurs, like a new priority 1 task, a canceled task, an agent taking PTO, or an agent running late.
    -   Assign the best agent for a work order task based on agent efficiency, which helps schedule and assign tasks more appropriately, using Field Service Agent Efficiency.
    -   Define work, travel, and overtime penalty values for each agent so the optimization engine can either schedule a nearby agent with a higher penalty or a distant agent with a lower penalty.

    -   Improve task scheduling by assigning dependent tasks to a single technician within the same shift.
-   **[Workforce](https://www.servicenow.com/docs/access?context=configuring-workforce&version=zurich&pubname=zurich-field-service-management&ft:locale=en-US)**

Enable managers to show or hide work order tasks from the **Calendars** tab in Workforce. When Workforce Optimization for Field Service is enabled, these tasks can also be viewed in Hybrid and Map views.

-   **[Field Service Scheduling](https://www.servicenow.com/docs/access?context=setting-up-scheduling-methods&version=zurich&pubname=zurich-field-service-management&ft:locale=en-US)**

Manage resource attributes for any duration, whether a single day or multiple days.

-   **[Appointment Booking](https://www.servicenow.com/docs/access?context=appointment-booking-administer&version=zurich&pubname=zurich-field-service-management&ft:locale=en-US)**

Use Appointment Booking to do the following:

    -   Enable better control over task sequencing using new dependency types, such as 'Finish to Start - Same Day' and 'Finish Together' with lag options, integrated with appointment booking for more precise scheduling. Enhance operational insight for all roles through improved visualizations including dependency trees, conflict alerts, and task indicators, which support dispatcher decisions and technician execution.
    -   Optimize appointment recommendations by allowing radius configuration at the territory level, tailored to diverse areas, such as urban versus rural. This capability includes an extension point for customers to implement custom radius logic with default instance-level values if no specific configuration is set.
    -   Enhance appointment recommendations by allowing grading against user-defined similar services rather than identical ones, resulting in more versatile scheduling options. This feature includes an extension point for customers to specify which services they consider similar, and the system defaults to same-catalog matching if no custom configuration is provided.
    -   Increase scheduling flexibility with new features to support slot overlap and overrides. This capability enables territory-based customization of appointment windows, default schedules, and specific slot-level overrides, giving more control over availability.

</td></tr><tr><td>

Field Service Management for Telecommunication

</td><td>

-   **[Managing work orders for telecommunication services](https://www.servicenow.com/docs/access?context=managing-work-order-telecommunication-service&version=zurich&pubname=zurich-telecom-media-technology&ft:locale=en-US)**

Manage the work orders for field services to support the installation, activation, and site assessments that are needed for connectivity services. This feature supports the POST, PATCH, GET, LIST, and DELETE operations for work orders via the TMF 697 Open API.


</td></tr><tr><td>

Financial Services Card Operations

</td><td>

-   **[Overview of the Dispute Management workflow](https://www.servicenow.com/docs/access?context=dispute-management-workflows&version=zurich&pubname=zurich-financial-services-operations&ft:locale=en-US)**

Resolve Mastercard disputes quickly with an enhanced end-to-end workspace that supports all stages of the dispute life cycle, including pre-arbitration and arbitration. Use comprehensive tools to simplify and accelerate the dispute management process.

-   **[ACH disputes workflow](https://www.servicenow.com/docs/access?context=work-dispute-ach&version=zurich&pubname=zurich-financial-services-operations&ft:locale=en-US)**

Resolve ACH disputes faster with a guided, end-to-end workflow that unifies intake, investigation, and resolution—built on a framework ready for any non-card transaction. The unified intake now features a new dispute reason framework for accurate regulatory mapping and embedded WSUD signature collection for seamless authorization capture. The overall workflow centralizes data, applies real-time regulatory checks, and surfaces next best actions to reduce manual effort and speed decisioning, all on a modular design that can scale to additional non-card dispute types.


</td></tr><tr><td>

Financial Services Operations Core

</td><td>

-   **[Payment card application](https://www.servicenow.com/docs/access?context=payment-card-application&version=zurich&pubname=zurich-financial-services-operations&ft:locale=en-US)**

Store the details of physical payment cards across the entire card life cycle, from issuance to servicing. You can also store tokenized values for sensitive data, such as the primary account number \(PAN\).

-   **[Deny-Unless ACL](https://www.servicenow.com/docs/access?context=acl-denial-behavior&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)**

Use Deny-Unless access control lists \(ACLs\) on FSO tables for non-authenticated users, such as users with public roles. With this minimum-security setting, only your authenticated users can read, write, delete, or create actions on these tables. For more information about the Deny-Unless ACLs, see the [Deny-Unless ACL](https://www.servicenow.com/docs/access?context=acl-denial-behavior&version=zurich&pubname=zurich-platform-security&ft:locale=en-US) topic in the ServiceNow® Platform Security documentation.


</td></tr><tr><td>

Financial Services Operations Integration with Mastercard

</td><td>

-   **​ [Mastercom subflows for disputes](https://www.servicenow.com/docs/access?context=financial-services-operations-integration-with-mastercard-subflows&version=zurich&pubname=zurich-financial-services-operations&ft:locale=en-US)**

An integration layer that provides predefined subflows and a supporting data model to enable seamless execution of Mastercom spoke actions for dispute management. This layer includes the following subflows:

    -   Mastercom - Look up Transaction Details
    -   Mastercom - Look up Clearing Transaction Details
    -   Mastercom - Create Fraud Report
    -   Mastercom - Create Claim
    -   Mastercom - Look up Chargeback Details
    -   Mastercom - Look up Second Presentment Details
    -   Mastercom - Look up Case Filing Details
    -   Mastercom - Validate Claim Response Details
    -   Mastercom - Create Chargeback
    -   Mastercom - Acknowledge Chargeback
    -   Mastercom - Update Chargeback
    -   Mastercom - Look up Chargeback Documents
    -   Mastercom - Look up Chargeback Documents Status
    -   Mastercom - Process Pending Documentation Queue
    -   Mastercom - Process Issuer Worked Queue
    -   Mastercom - Process Reject Queue
    -   Mastercom - Process Issuer Re-presentment Unworked Queue
    -   Mastercom - Process Sender Case Filing Queue
    -   Mastercom - Create Case Filing
    -   Mastercom - Take Action on Case
    -   Mastercom - Look up Case Documents
    -   Mastercom - Look up Case Documents Status
    -   Mastercom - Look up List of Claims

-   **[Additional Mastercom subflows for disputes](https://www.servicenow.com/docs/access?context=financial-services-operations-integration-with-mastercard-subflows&version=zurich&pubname=zurich-financial-services-operations&ft:locale=en-US)**

New set of subflows to promote execution of Mastercom spoke actions for dispute management. This set includes the following subflows:

    -   Mastercom - Look up Authorization Transaction Details
    -   Mastercom - Look up Claim Details
    -   Mastercom - Take Action on Existing Claim
    -   Mastercom - Process Pending Queue
    -   Mastercom - Look up Chargebacks Related Information
    -   Mastercom - Look up Fraud Related Information
    -   Mastercom - Reverse Chargeback

</td></tr><tr><td>

Financial Services Operations Integration with Visa

</td><td>

-   **[Enable cardholder purchase inquiry property](https://www.servicenow.com/docs/access?context=properties-installed-with-fso-integration-with-visa&version=zurich&pubname=zurich-financial-services-operations&ft:locale=en-US)**

Enables or disables integration with the Cardholder Purchase Inquiry API in the Visa card dispute playbook.


</td></tr><tr><td>

Flows, subflows, and actions in Workflow Studio

</td><td>

-   **[Create and manage external event sources](https://www.servicenow.com/docs/access?context=manage-external-event-sources&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US)**

Create an external event source on your ServiceNow instance that listens to events occurring in an application or system outside of the ServiceNow AI Platform®. Based on the external event source, you can define one or more external trigger definitions in your instance and then associate the external trigger definitions with the external event source. When an event that you specified in the external trigger definition occurs, the external trigger definition executes one or more flows. You can update or remove external event sources that you create.

-   **[Create a domain-separated saved external trigger](https://www.servicenow.com/docs/access?context=create-saved-external-trigger&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US)**

Create a domain-separated saved external trigger. Configurations that you make to the trigger are auto-saved. After the trigger is published, you can edit only the **Label** field values.

-   **[Create a reusable scheduled trigger](https://www.servicenow.com/docs/access?context=create-scheduled-trigger&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US)**

Create a scheduled trigger that starts your flow when you need. Use the trigger across your flows.

-   **[Create a skill for conversational subflows and actions](https://www.servicenow.com/docs/access?context=create-conversational-subflow-skill&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US)**

Create a skill for the conversational subflow and action and make the skill discoverable in conversations. You can have multiple skills for the same subflow or action.

-   **[Enhancements in the subflow and action conversational settings](https://www.servicenow.com/docs/access?context=configure-subflow-conversation-settings&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US)**

To make the error messages more useful in a conversation, you can show specific error messages from the subflow or action rather than showing generic error messages. Additionally, if you override an input with reference, you can apply a filter to limit the number of records in the Reference field.

-   **[Make a flow wait for an email reply](https://www.servicenow.com/docs/access?context=wait-for-email-reply-action&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US)**

Pause a flow until an email reply is received to an outbound email record

-   **[Show subflow stages in a parent flow](https://www.servicenow.com/docs/access?context=show-subflow-stages-in-a-parent-flow&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US)**

Show subflow stages as part of the execution details of a parent flow.

-   **[Save flows, subflows, and actions automatically](https://www.servicenow.com/docs/access?context=save-as-you-go-flows&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US)**

Save flows, subflows, and actions automatically as you work on them.

-   **[Support Now LLM Long Term Stable models \(LTS\) with Flow generation](https://www.servicenow.com/docs/access?context=exploring-flow-generation&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US)**

Support the Now LLM Long Term Stable models \(LTS\) for Flow generation.

-   **[Support Now LLM Long Term Stable models \(LTS\) with Flow summarization](https://www.servicenow.com/docs/access?context=flow-summarization&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US)**

Support the Now LLM Long Term Stable models \(LTS\) for Flow summarization.

-   **[Use an AI agent action](https://www.servicenow.com/docs/access?context=use-an-ai-agent-action&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US)**

Use flow data to run an AI agent and configure the expected agent output for use later in the flow.

-   **[Use conversational subflows and actions by default](https://www.servicenow.com/docs/access?context=conversational-subflows&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US)**

Use conversational subflows and actions when you install any Now Assist product. This skill is active by default.

-   **[Use your preferred LLM to generate descriptions for subflow or action skill, input, and output](https://www.servicenow.com/docs/access?context=configure-llm-for-conversational-subflow&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US)**

Leverage generative AI to generate descriptions for the subflow or action skill, inputs, and outputs. You can configure a default LLM to generate the descriptions.

-   **[View flow history](https://www.servicenow.com/docs/access?context=flow-history&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US)**

View and manage the history of a flow. See past configurations of a flow to copy, restore, or remove them.

-   **[View subflow history](https://www.servicenow.com/docs/access?context=subflow-history&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US)**

View and manage the history of a subflow. See past configurations of a subflow to copy, restore, or remove them.


</td></tr><tr><td>

Generative AI Controller

</td><td>

-   **[Configure a custom resource path for BYOK models](https://www.servicenow.com/docs/access?context=configure-custom-resource-path-byok&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Connect Generative AI Controller to your Azure OpenAI deployment by configuring a custom resource path in your bring your own key \(BYOK\) model configuration. Use this when your Azure OpenAI endpoint includes a path segment that Generative AI Controller does not add by default.


-   **[Administrator access to Gen AI log](https://www.servicenow.com/docs/access?context=reference-for-generative-ai-controller&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Access the Gen AI log \[sys\_generative\_ai\_log\] table to gain insights for debugging purposes. HR-related records remain restricted to HR admins.

-   **[Enhanced AI asset inventory](https://www.servicenow.com/docs/access?context=reference-for-generative-ai-controller&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Track the enhanced AI asset inventory through AI Control Tower using new metadata fields in the Model \[sys\_generative\_ai\_model\_config\] and Prompt \[sys\_generative\_ai\_config\] tables. Gain better visibility into AI asset status and life-cycle details, such as retirement dates.

-   **[Long-Term Stable model for generative AI](https://www.servicenow.com/docs/access?context=long-term-stable-models&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Promote stability and adoption for entitled users with a Long-Term Stable \(LTS\) model. The LTS model provides regulatory alignment, predictable behavior, and life cycle stability to integrate GenAI with confidence.


-   **[AI Model Version Mappings](https://www.servicenow.com/docs/access?context=reference-for-generative-ai-controller&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Review the mappings between AI model versions and their providers in the Gen AI Model Version Mapping \[sys\_gen\_ai\_model\_version\_mapping\] table. This table shows the mappings between source and target models, along with associated metadata, such as skill type, model type, resource associations, and provider information.


-   **[Identify third-party LLM information](https://www.servicenow.com/docs/access?context=reference-for-generative-ai-controller&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Access the Gen AI Log Metadata \[sys\_gen\_ai\_log\_metadata\] table to identify which LLM model, version, and requested language was used to generate the AI content.

-   **[Restrict LLM usage based on the domain](https://www.servicenow.com/docs/access?context=reference-for-generative-ai-controller&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Enable or disable Now Assist for each domain so that you can restrict the use of LLMs and avoid using AI for data processing, if needed.


</td></tr><tr><td>

Goal Framework

</td><td>

-   **[Goal Framework and AI Control Tower](https://www.servicenow.com/docs/access?context=better-together-with-other-apps-gf&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)**

Categorize your strategic priorities and goals as Artificial Intelligence to track and monitor strategy progress from the AI Control Tower workspace.

Use the **Type** field for strategic priorities and the **Category** field for goals to classify them as Artificial Intelligence and monitor their progress in the AI Control Tower workspace.

-   **[Role enhancements](https://www.servicenow.com/docs/access?context=components-installed-with-goal-framework&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)**

With the sn\_gf.goal\_admin role, you can edit any goal and target as needed, even when you aren’t the owner or contributor of a goal or target.


</td></tr><tr><td>

HR Multi Instance Integration

</td><td>

-   **[HR Multi Instance Integration](https://www.servicenow.com/docs/access?context=multi-instance-int&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

Partners and service providers for HR service fulfillment often are running their own instance of HR Service Delivery. HR Multi Instance Integration provides inter-instance communication and hybrid HR services with fulfillment in different instances through the following capabilities:

    -   Ability to control your organization employee’s experience and interactions per your organization's culture, branding, and policies.
    -   Ability to outsource services.
    -   Consistent user experience for employees across the entire HR catalog, regardless of whether they are interacting locally or remotely from any third-party provider.
    -   Because HR workflows or business process are not restricted to a single instance, they can flow seamlessly across instances.
    -   Uniformity and standardization for HR agents on the provider instance enables them to work on local cases or remote HR cases from the provider’s ServiceNow AI Platform instance with a minimal learning curve.
    -   Managing and controlling access at the remote catalog level to meet security and compliance requirements.
    -   Synchronization of relevant information such as submitted request \(provider task\) status, comments, and attachments by service providers.
    -   Ability to fulfill an HR case partially by providers and partially by consumers.
    -   Ability to create HR tasks and approval tasks for remote HR cases.

**Note:** Only manual approval flow is supported, and not the automatic approval flow.

    -   Initiate document signing tasks for remote users via universal tasks. This feature is available only when the Document Template plugin is installed along with the HR Multi Instance Integration for Provider application.
    -   Enable remote users \(consumer users\) to complete HR tasks, document tasks, and approval tasks via magic links shared in universal tasks. Magic links route remote users to the provider instance for completing the assigned tasks.
    -   Support the **URL** task type in Universal Task. This task type enables you to specify a URL link that is shared in the universal task assigned to a local or remote user.
    -   Support the **External** field in the HR Profile data. When the HR profile belongs to an employee in consumer company, the **External** field is marked True.

</td></tr><tr><td>

Hardware Asset Management

</td><td>

-   **[Track asset movement from the receiving bay to an aisle-space in the stockroom](https://www.servicenow.com/docs/access?context=managing-inventory-by-putting-away-asset&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

Move assets from the receiving bay to their designated aisle and space and improve asset tracking and inventory management by using the Asset put away feature. This task can be performed via the Hardware Asset Workspace or ServiceNow Agent application.

-   **[Improve asset data accuracy and usage by tracking and managing unassigned assets through asset attestation](https://www.servicenow.com/docs/access?context=asset-attestation-ham&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

Validate whether assets are in use and confirm asset assignments by initiating the attestation using the Asset Attestation playbook in the Hardware Asset Workspace. Employees can then confirm whether they’re using the assigned serialized hardware assets on the go by using the intuitive Now Mobile app. Reports on open remediation tasks in the Hardware Asset Workspace, generated when employees confirm they don’t have assets, provide actionable insights for asset managers.

-   **[Confirm receipt of hardware and consumable assets through the Employee Center portal](https://www.servicenow.com/docs/access?context=receive-assets-employee-center&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

Enable your employees to acknowledge the receipt of assets that are in transit and reserved for them through the Employee Center portal. When employees confirm that they have received the assets, the **State** and the **Assigned to** fields are updated in real time, minimizing the risk of data errors.

-   **[Receive shipment assets at a stockroom in the Hardware Asset Workspace](https://www.servicenow.com/docs/access?context=stockroom-receiving-ham&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

Complete the receive tasks for hardware and consumable assets that you received from any workflow at the stockroom using the unified receiving functionality in the Hardware Asset Workspace. This standardized receiving process reduces the time spent on receiving assets. By requiring each asset to be assigned a unique identiﬁer when received at the stockroom, the quality of asset data also improves.

You can receive assets in bulk by using a template. Additionally, you can view the results and validation comments in the staging table. During this process, the system handles existing assets, creates new ones as needed, and performs comprehensive validations.

-   **[Optimize your operations with asset performance reports](https://www.servicenow.com/docs/access?context=asset-analytics-view&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

Improve asset availability according to ISO standards by tracking the past performance of assets and getting notified about trends, threshold breaches, or anomalies based on their location, model category, model, or classification.

-   **[Monitor supply and demand of assets in a stockroom with detailed inventory reports](https://www.servicenow.com/docs/access?context=manage-stockroom-inventory-report-ham&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

Track and manage stockrooms efficiently by evaluating the inventory reports in the Inventory view of the Hardware Asset Workspace. These reports provide the following benefits:

    -   Find replacement options for assets that are in use, being repaired, or in maintenance
    -   Quickly identify shortages and align current demand in your stockroom with both current and incoming supply
    -   Analyze the supply to meet open demand across all stockrooms or locations
-   **[Gain expanded insight into the content library information through content dashboard analytics](https://www.servicenow.com/docs/access?context=content-lookup-ham&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

Gain in-depth information related to various content tables and trends in content change from the enhanced Content Library portal. The introduction of numeric widgets, line graphs, bar charts, and content-specific tabs provides complete visibility to content shipped and analyze content coverage. The expanded search feature with additional filter options enables you to view the records for a particular period or release.


</td></tr><tr><td>

Health Log Analytics

</td><td>

-   **[Facilitate Cribl log data ingestion by Health Log Analytics using the Cribl integration](https://www.servicenow.com/docs/access?context=il-connector-hla-cribl&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

Starting in version 37.0.15, use the Cribl log data integration to streamline Health Log Analytics data ingestion with Cribl. If your organization uses Cribl for filtering and routing large volumes of log data from various sources, the log format received by HLA is distinct from other types. The Cribl integration enables HLA to detect and separate transport headers from inner log messages in this format, forwarding only the inner message to the source type structure for processing. You can configure the Cribl integration conveniently through the Integrations Launchpad.


-   **[Leverage additional information available on the integration's Overview screen](https://www.servicenow.com/docs/access?context=il-connector-overview-tab&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

Starting in version 37.0.15, take advantage of extra information presented on the Overview screen. The screen now displays the ITOM Gateway in the log processing pipeline and the log streaming rate per minute, aligning it with the metrics for the MID Server and the HLA Engine. The Overview screen also shows the source time of the last processed log.


-   **[Export source types to an update set by log source](https://www.servicenow.com/docs/access?context=hla-export-sourcetypes-by-source&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

Starting in version 38.0.16, export all source types related to one or more selected log sources to an update set together. You can then import the update set to the target environment.


-   **[Map log data to service instances and components for alerts in context](https://www.servicenow.com/docs/access?context=il-connector-hla-map-business-context&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

Starting in version 38.0.16, map your logs to service instances and components so that Health Log Analytics can generate alerts in the correct context. Contextualizing your log data is especially important when the integration processes logs from multiple service instances and components.


-   **[Display Integrations Launchpad from the ITOM AIOps configuration center](https://www.servicenow.com/docs/access?context=itom-aiops-conf-center&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

Starting in version 38.0.16, open the Integrations Launchpad from ITOM AIOps configuration center. The ITOM AIOps configuration center is a centralized workspace that enables you to configure and manage AIOps features from a single place.


-   **[Set up a GCP PubSub integration from the Integrations Launchpad](https://www.servicenow.com/docs/access?context=il-connector-hla-gcp-pubsub&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

Starting in version 38.0.16, set up an integration from the Integrations Launchpad for receiving log messages that were published to a Google Cloud Platform \(GCP\) Pub/Sub topic and streaming them to your ServiceNow instance.


-   **[Set up a Microsoft Azure Event Hubs integration from the Integrations Launchpad](https://www.servicenow.com/docs/access?context=il-connector-hla-event-hubs&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

Starting in version 38.0.16, set up an integration from the Integrations Launchpad for streaming events from Microsoft Azure Event Hubs to your ServiceNow instance.


-   **[Set up an Edge Delta TCP or REST integration from the Integrations Launchpad](https://www.servicenow.com/docs/access?context=il-connector-hla-edgedelta-tcp&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

Starting in version 38.0.16, set up an integration from the Integrations Launchpad to enable Health Log Analytics to process Edge Delta log messages streaming into your ServiceNow instance over the TCP transport protocol or via REST.


-   **[Monitor ServiceNow instance logs with the ServiceNow Log Export data input](https://www.servicenow.com/docs/access?context=hla-data-input-log-export&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

Starting in version 38.0.16, set up a data input for monitoring ServiceNow instance node logs from both Java code and JavaScript in Health Log Analytics.


</td></tr><tr><td>

Hermes Messaging Service

</td><td>

-   **[Monitor Hermes data usage](https://www.servicenow.com/docs/access?context=monitoring-data-usage-hermes&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)**

Monitor data usage by application and track data usage by topic using the Hermes Usage Dashboard.

-   **[Synchronize topic partition count](https://www.servicenow.com/docs/access?context=update-topic-hermes&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)**

Verify that the partition count is synchronized between topics in Hermes clusters.


</td></tr><tr><td>

Hiring

</td><td>

-   **[Create a job requisition as a hiring manager](https://www.servicenow.com/docs/access?context=request-req-hm&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

As a hiring manager, request a job requisition for a vacancy in your organization that you want to fill.

-   **[Tracking a job requisition in the Hiring tab](https://www.servicenow.com/docs/access?context=view-status-my-request&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

View the status and details of a job requisition, compare applications, and perform other actions as needed.

-   **[Tracking an application record from the Hiring tab](https://www.servicenow.com/docs/access?context=application-record-details-hiring&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

Track an application on a job requisition, provide recommendations for the application, monitor interviews and feedback, and more.

-   **[Collaborate with the recruiter](https://www.servicenow.com/docs/access?context=collab-recruiter&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

Engage with recruiters to collaborate and identify what needs your immediate attention, helping you manage job requisitions more effectively.

-   **[View hiring content](https://www.servicenow.com/docs/access?context=view-hiring-content&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

Refer to the various hiring materials available under the Hiring tab to get a better understanding of the hiring policies and processes.


</td></tr><tr><td>

ITOM AIOps

</td><td>

-   **[Facilitate Cribl log data ingestion by Health Log Analytics using the Cribl integration](https://www.servicenow.com/docs/access?context=il-connector-hla-cribl&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

Starting in version 37.0.15, use the Cribl log data integration to streamline Health Log Analytics data ingestion with Cribl. If your organization uses Cribl for filtering and routing large volumes of log data from various sources, the log format received by HLA is distinct from other types. The Cribl integration enables HLA to detect and separate transport headers from inner log messages in this format, forwarding only the inner message to the source type structure for processing. You can configure the Cribl integration conveniently through the Integrations Launchpad.

-   **[Leverage additional information available on the integration's Overview screen](https://www.servicenow.com/docs/access?context=il-connector-overview-tab&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

Starting in version 37.0.15, take advantage of additional information presented on the Overview screen. The screen now displays the ITOM Gateway in the log processing pipeline and the log streaming rate per minute, aligning it with the metrics for the MID Server and the HLA Engine. The Overview screen also shows the source time of the last processed log.

-   **[Benefit from enhanced Log Analytics alert group and mixed alert group functionality in the Express List](https://www.servicenow.com/docs/access?context=el-link-view&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

Starting in version 26.9.0, identify connected Log Analytics alerts and mixed alert group correlations faster using the Link View functionality. Utilize enhanced Now Assist Alert Analysis with additional context for Log Analytics alerts.

-   **[View visualizations of anomaly information for Log Analytics-based alerts and metric intelligence alerts in Express List®](https://www.servicenow.com/docs/access?context=view-anomaly-alert-display&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

Starting in version 26.9.0, review anomaly charts for Log Analytics alerts and Metric Intelligence alerts in the preview panel in Express List®.

-   **[Configure automatic resume for live updates when the live alert list is paused, and configure time ranges in Express List®](https://www.servicenow.com/docs/access?context=express-list&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

Starting in version 26.9.0, enable admins to configure the amount of time until the active display resumes after being paused in Express List®. Admins are also able to customize the time range options displayed in Express List®.


-   **[Map log data to service instances and components for alerts in context](https://www.servicenow.com/docs/access?context=il-connector-hla-map-business-context&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

Starting in version 38.0.16, map your logs to service instances and components so that Health Log Analytics can generate alerts in the correct context. Contextualizing your log data is especially important when the integration processes logs from multiple service instances and components.


-   **[Monitor ServiceNow instance logs with the ServiceNow Log Export data input](https://www.servicenow.com/docs/access?context=hla-data-input-log-export&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

Starting in version 38.0.16, set up a data input for monitoring ServiceNow instance node logs from both Java code and JavaScript in Health Log Analytics.


-   **[Live updates functionality has been updated in the Service Operation Workspace Lists.](https://www.servicenow.com/docs/access?context=configure-alert-list-autofresh-settings&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

Starting in version 26.11.0, a new toggle switch allows users to enable or disable live updates. When the toggle is set to on, alerts are updated automatically. When the toggle is set to off, a badge displays the number of available updates until the page is refreshed manually. The setting is saved for future logins by the same user.

-   **[Explore the new Dependency view for an alert](https://www.servicenow.com/docs/access?context=dependency-maps&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

Starting in version 26.11.0, explore the new Dependency view for an alert. Access maps from the following locations:

    -   in the preview panel, in the Configuration item section for the CI topology
    -   in the Utilities panel of the alert record
    -   in the action drop-down menu
    -   in the Core UI alert form
-   **[Respond to multiple alerts in Express List](https://www.servicenow.com/docs/access?context=bulk-alert-response-express-list&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

Starting in version 26.11.0, run response actions on multiple alerts at the same time in Express List.


</td></tr><tr><td>

ITOM Cloud Accelerate

</td><td>

-   **[Configure a custom catalog ID in Cloud Account Management account request](https://www.servicenow.com/docs/access?context=configuring-catalog-ids-in-cam-account-request&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

Users with the cw\_admin role can set which catalog to use for Cloud Account Management \(CAM\) requests by updating the **sn\_itom\_cam.cam\_catalog\_id** system property. This property is set by default to the base system CAM catalog.

-   **[Viewing Cloud Account Management dashboards](https://www.servicenow.com/docs/access?context=about-cam-dashboard&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

Access the Compliance dashboard, Overview page, and Cloud assets dashboard through the Cloud Asset Explorer section in the new **Monitor and Track** tab.

    -   Compliance dashboard: View data across AWS, Azure, Google Cloud Platform \(GCP\), and OCI accounts in one centralized location.
    -   Overview page:
        -   View total discovered assets, grouped by cloud provider and categorized into Compute, Databases, Virtual Machines, and Storage categories on the Overview page.
        -   Monitor total accounts by provider, with change tracking since the last update.
    -   Cloud assets dashboard:
        -   Governance and operations teams can monitor, track, and act on compliance and asset details through the Cloud assets dashboard.
        -   Identify missing ownership information for accounts to support accountability and audit readiness.
        -   Asset viewers can drill down to view detailed information for each configuration item \(CI\).
-   **[Viewing the home page](https://www.servicenow.com/docs/access?context=view-home-page&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US) in Cloud Account Management**
    -   Visualize growth trends across cloud providers with a time-based graph showing account activity.
    -   Leverage direct access to Cloud Discovery Workspace and Cloud Cost Management from the dashboard.
    -   Use filters like cloud provider and business unit to refine the dashboard view for tailored insights.
-   **[Cloud Provisioning and Governance](https://www.servicenow.com/docs/access?context=cloud-management-v2-landing-page&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

The legacy workflows are no longer supported starting with the Zurich release. You can continue using existing custom workflows and deprecated base system workflows but use the new base system Flows for all future needs. In the Zurich release, the Cloud resource operation request and Blueprint request workflows have been migrated to subflows.


</td></tr><tr><td>

ITOM Visibility

</td><td>

-   **Install ITOM Visibility apps using Now Assist for Setup**

Now Assist for Setup provides a centralized, guided installation experience for ITOM Visibility. From a single interface, administrators can review what applications are included in the installation, review the installation status, and install all required applications and plugins.

-   **[Discover your Alibaba Cloud resources](https://www.servicenow.com/docs/access?context=alibaba-cloud-discovery&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

Starting with Discovery and Service Mapping Patterns store version 1.29.0, Discovery supports Alibaba Cloud. Discovery enables real-time visibility and automated population of the CMDB with configuration data for cloud resources.

-   **[Create a cloud discovery schedule in Discovery Admin Workspace](https://www.servicenow.com/docs/access?context=discovery-admin-workspace-schedules&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

Starting with version 1.11.0, Discovery Admin Workspace supports creating Discovery schedules for Amazon Web Services, Azure, and Google Cloud Platform cloud providers. This update advances the integration of cloud discovery capabilities into a unified workspace, reducing operational complexity and aligning with the upcoming deprecation of Cloud Discovery Workspace.

For the procedural information, see:

    -   [AWS](https://www.servicenow.com/docs/access?context=create-AWS-schedule-DAW&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)
    -   [Azure](https://www.servicenow.com/docs/access?context=create-azure-schedule-DAW&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)
    -   [GCP](https://www.servicenow.com/docs/access?context=create-gcp-schedule-DAW&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)
-   **[Discover AWS EC2 VMs using AWS Systems Manager \(SSM\)](https://www.servicenow.com/docs/access?context=aws-ssm-discovery&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

Perform detailed discovery of EC2 hosts running in AWS without the requirement for a direct SSH or PowerShell connection by discovering AWS EC2 VMs by using AWS Systems Manager \(SSM\).

-   **[Discovery Guided Setup](https://www.servicenow.com/docs/access?context=discovery-guided-setup&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

Starting with version 1.11.0, you can access ITOM Discovery Guided Setup from the Discovery Admin Workspace home page. This setup provides a structured process to configure Discovery and maintain accurate CMDB visibility quickly.

-   **[View command validation-related entries using new role in Pattern Designer Enhancements](https://www.servicenow.com/docs/access?context=discovery-command-probe-pattern&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

Starting with Pattern Designer Enhancements version 3.9.0, the new pde\_viewer role has permissions to view **Command Validation Tasks**, **Command Validation Tasks Results**, and **Command List**. The pde\_viewer role is restricted to viewing the command list modules and doesn't have permissions to modify or edit them. The pde\_viewer role can view the following tables only:

    -   Command List \[pd\_command\_list\]
    -   Command Validation Task \[pd\_command\_validation\]
    -   Command Validation Task Results \[pd\_command\_validation\_results\]
    -   Pattern Shared Library Mapping \[pd\_pattern\_to\_shared\_library\_mapping\]
    -   Temporary Variable Mappings \[pd\_temp\_variable\_value\_mapping\]
-   **[Discover new products with Discovery and Service Mapping Patterns](https://www.servicenow.com/docs/access?context=available-patterns&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

Discover the following products using Discovery and Service Mapping Patterns version 1.29.0:

    -   [Alibaba Cloud](https://www.servicenow.com/docs/access?context=alibaba-cloud-discovery-pattern&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)
    -   [OCI GovCloud](https://www.servicenow.com/docs/access?context=oracle-cloud-infrastructure-discovery&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)
    -   [10 addition Azure cloud services](https://www.servicenow.com/docs/access?context=azure-cloud-discovery-patterns&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)
    -   [22 additional AWS cloud services](https://www.servicenow.com/docs/access?context=data-discovered-aws-patterns&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)
    -   [New AWS API Gateway data model](https://www.servicenow.com/docs/access?context=aws-api-gateway-discovery&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)
    -   [AWS datacenters with resources only](https://www.servicenow.com/docs/access?context=data-discovered-aws-patterns&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)
    -   [OLVM templates, disks, and networks](https://www.servicenow.com/docs/access?context=red-hat-virtualization-discovery&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)
    -   [Nutanix Prism using API v4](https://www.servicenow.com/docs/access?context=nutanix-pattern&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)
Discover the following products using Discovery and Service Mapping Patterns version 1.28.0:

    -   [22 additional Azure cloud services](https://www.servicenow.com/docs/access?context=azure-cloud-discovery-patterns&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)
    -   [GCP Cloud Function](https://www.servicenow.com/docs/access?context=gcp-cloud-functions-patterns&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)
    -   [GCP AlloyDB](https://www.servicenow.com/docs/access?context=gcp-alloydb-postgresql-patterns&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)
    -   [GCP Redis Cluster](https://www.servicenow.com/docs/access?context=gcp-memorystore-patterns&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)
-   **[Receive updates for activated patterns](https://www.servicenow.com/docs/access?context=activate-disabled-pattern&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

Starting with Visibility Content version 6.28.0, activating or deactivating a pattern won't be considered a customization, and it will continue to receive updates. Patterns that were previously activated or deactivated will reset to the latest predefined version after upgrading while retaining the last active field value.

-   **[Enhance your resource management with the new Tag Categorization feature from Tag Governance](https://www.servicenow.com/docs/access?context=tag-categorization-tag-governance&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

Starting with version 1.7.0, automate the tagging process to promote a consistent, organized way to manage tags by using five predefined tag categories provided by Tag Governance.

-   **[Estimate your cloud license count prior to using ITOM cloud solutions using CLE](https://www.servicenow.com/docs/access?context=cloud-license-estimator-landing&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

Cloud License Estimator \(CLE\) provides an estimated resource count for all cloud resources eligible for licensing.  It validates the  provided cloud  account details and estimates the resource  count  based on the prevailing licensing rules. 

-   **[Improve admin efficiency with new Actions menu](https://www.servicenow.com/docs/access?context=discovery-admin-workspace-diagnostics&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

Discovery Admin Workspace version 1.10.0 introduces a new **Actions** drop-down menu on the **Anomaly Detection** tab of the Diagnostics page, offering quick access to anomaly detection settings and a **Clear all anomalies** option to remove related records from key tables.


-   **[Enjoy increased control and improved accuracy in the Automated Service Suggestions feature](https://www.servicenow.com/docs/access?context=components-installed-with-service-mapping-plus&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US) in Service Mapping.**

Ensure that candidates remain relevant and useful through a new property that excludes irrelevant information from Application Service Candidates, such as non-operational or retired servers.


</td></tr><tr><td>

Identity

</td><td>

-   **[Machine Identity Console](https://www.servicenow.com/docs/access?context=machine-identity-console&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)**

Use the Machine Identity Console to see what data integration accounts are accessing and how they’re configured. This console helps you make smarter security decisions about setting up these accounts.


</td></tr><tr><td>

Impact

</td><td>

-   ****
    -   Implement Scan Engine to enable proactive management of instance quality, compliance, and performance.
    -   Examine ServiceNow instances for violations of the active leading practice definitions and report violations that are stored in the Scan Findings table.
    -   View existing or resolved findings that resulted from the instance scans or from summarized and detailed scan information.
    -   Empower developers to receive real-time, AI-driven recommendations within their workspace to identify and resolve code quality issues, enabling adherence to ServiceNow leading practices and reducing technical debt proactively.
-   **[GenAI-powered Root Cause Remediation](https://www.servicenow.com/docs/access?context=generative-ai-root-cause-anal&version=zurich&pubname=zurich-impact&ft:locale=en-US)**

Identify the cause of performance issues and receive suggestions for corrective actions by implementing root cause remediation \(RCR\) after generating the root cause summary \(RCS\).

-   **[Performance insights in user-configurable dashboard](https://www.servicenow.com/docs/access?context=io-performance-insights&version=zurich&pubname=zurich-impact&ft:locale=en-US)**

Assess the performance status of your ServiceNow instances using the ML-based instance performance widget.

-   **[Analyze user experience and monitor application performance in Instance Observer](https://www.servicenow.com/docs/access?context=io-app-mon-perf-analy&version=zurich&pubname=zurich-impact&ft:locale=en-US)**

Monitor response times using operational metrics.

-   **[Generative AI-powered Root cause analysis](https://www.servicenow.com/docs/access?context=generative-ai-root-cause-anal&version=zurich&pubname=zurich-impact&ft:locale=en-US)**

Generate a structured root cause summary using a large language model \(LLM\) anomaly detection system that can automate the process and analyze system logs, performance metrics, and alerts. This root cause summary simplifies the analysis process and helps to diagnose the problem before the issue occurs.

**Note:**

The Generative AI-powered summarization component is not available to users in the regulated market.

-   **[Instance Observer alerts for Guided-tier customers](https://www.servicenow.com/docs/access?context=io-alerts-guided-cust&version=zurich&pubname=zurich-impact&ft:locale=en-US)**

The top six alert cards evaluated to be most important based on alerts that users have used and benefited from in the past are now available to Guided-tier Instance Observer customers in addition to the Advanced-tier and Total-tier customers.

-   **[Use popular alerts to receive notifications](https://www.servicenow.com/docs/access?context=io-alerts-popular-total-adv-cust&version=zurich&pubname=zurich-impact&ft:locale=en-US)**

View the most popular alerts displayed on the first page of the Configure Alerts page. You can also set up alerts and view notifications.

-   **[Triage a ServiceNow instance based on nodes](https://www.servicenow.com/docs/access?context=io-triage-sn-instance&version=zurich&pubname=zurich-impact&ft:locale=en-US)**

Triage your ServiceNow instances based on production nodes that are categorized as All, Generic, Worker, and UI nodes. This categorization removes unhelpful irrelevant standby nodes and helps triage useful production nodes.

-   **[Custom Performance report](https://www.servicenow.com/docs/access?context=instance-observer-reporting&version=zurich&pubname=zurich-impact&ft:locale=en-US)**

Generate a custom report selecting a maximum of 20 metrics and a minimum of one metric from a wide range of 90 metrics available across the Instance Observer application. This report is almost the same as Performance Trend report, however it offers you the flexibility to choose more metrics from the performance categories in the Performance page and build a dynamic report, and also to customize how charts are displayed in the report.

-   **[Accelerator request](https://www.servicenow.com/docs/access?context=accelerator-request&version=zurich&pubname=zurich-impact&ft:locale=en-US)**

Request and manage accelerators across different instances from both Impact Delivery Instance and Impact Store Application. Interact with the experts in Impact from the Impact Store Application.

-   **[Accelerator Catalog](https://www.servicenow.com/docs/access?context=accelerator-catalog&version=zurich&pubname=zurich-impact&ft:locale=en-US)**

Use the following new accelerators:

Technical Accelerators:

    -   [Jumpstart Your CSDM:Crawl](https://www.servicenow.com/docs/access?context=jumpstart-your-CSDM-crawl&version=zurich&pubname=zurich-impact&ft:locale=en-US): Get an overview of the crawl phase of the Common Service Data Model \(CSDM\) maturity journey, a brief assessment of current crawl data, and actionable steps to complete the phase.
    -   [Jumpstart Your External Content Connectors \(XCC\)](https://www.servicenow.com/docs/access?context=jumpstart-your-external-content-connectors&version=zurich&pubname=zurich-impact&ft:locale=en-US): Get a demonstration of the possibilities and capabilities of External Content Connectors \(XCC\).
    -   [Jumpstart Your Now Assist in Document Intelligence​](https://www.servicenow.com/docs/access?context=jumpstart-your-now-assist-document-intelligence&version=zurich&pubname=zurich-impact&ft:locale=en-US): Get a demonstration of the possibilities and capabilities of Now Assist in Document Intelligence.
    -   [Jumpstart Your Strategic Portfolio Management-Project Workspace](https://www.servicenow.com/docs/access?context=jumpstart-your-SPM-project-workspace&version=zurich&pubname=zurich-impact&ft:locale=en-US): Get a demonstration of the possibilities and capabilities of Project Workspaces within Strategic Portfolio Management \(SPM\).
    -   [Jumpstart Your Workflow Automation: Playbooks](https://www.servicenow.com/docs/access?context=jumpstart-your-workflow-automation-playbooks&version=zurich&pubname=zurich-impact&ft:locale=en-US): Get a demonstration of the possibilities and capabilities of playbooks in Workflow Studio.
    -   [Jumpstart Your AI Control Tower](https://www.servicenow.com/docs/access?context=jumpstart-your-ai-control-tower&version=zurich&pubname=zurich-impact&ft:locale=en-US): Get a demonstration of the possibilities and capabilities of ServiceNow’s AI Control Tower.
    -   [Jumpstart Your SPM-Collaborative Work Management](https://www.servicenow.com/docs/access?context=jumpstart-your-spm-collaborative-work-management&version=zurich&pubname=zurich-impact&ft:locale=en-US): Get a demonstration of how customers can set up and utilize CWM to plan, manage, visualize, and collaborate on work with their teams.
    -   [Jumpstart Your Now Mobile for Employees](https://www.servicenow.com/docs/access?context=jumpstart-your-now-mobile-for-employees&version=zurich&pubname=zurich-impact&ft:locale=en-US): Get an introduction and overview of the base system capabilities and a demonstration of the configuration steps needed to get started with Now Mobile.
    -   [Jumpstart Your ITOM Discovery](https://www.servicenow.com/docs/access?context=jumpstart-your-itom-discovery&version=zurich&pubname=zurich-impact&ft:locale=en-US): Get foundational guidance for successful IT Operations Management \(ITOM\) Discovery implementation, and a demonstration of its possibilities and capabilities.
Strategic Accelerators:

    -   [ITOM Maturity Accelerator](https://www.servicenow.com/docs/access?context=ITOM-maturity-assessment&version=zurich&pubname=zurich-impact&ft:locale=en-US): Get guidance on fine-tuning IT Operations Management \(ITOM\) with a base-level understanding of maturity tied to business outcomes.
    -   [Stakeholder Path to Value](https://www.servicenow.com/docs/access?context=stakeholder-path-to-value&version=zurich&pubname=zurich-impact&ft:locale=en-US): Get deep qualitative insights into how process owners and key stakeholders utilize the ServiceNow platform to deliver vital services across the organization.
    -   [Foundations of AI Governance](https://www.servicenow.com/docs/access?context=foundations-of-ai-governance&version=zurich&pubname=zurich-impact&ft:locale=en-US): Foundational knowledge that will help you start your AI Management journey and take control of your AI deployments.
-   **[Outcomes based contextual learning recommendations](https://www.servicenow.com/docs/access?context=contextual-learning-recommendations&version=zurich&pubname=zurich-impact&ft:locale=en-US)**
    -   View the recommendations for the most relevant personalized course recommendations based on your performance context to help you strengthen specific skills.
    -   View the recommendation for every capability. Multiple courses are available for some recommendations.
-   **[Value management](https://www.servicenow.com/docs/access?context=impact-in-platform-business-outcomes&version=zurich&pubname=zurich-impact&ft:locale=en-US)**

[Value reports](https://www.servicenow.com/docs/access?context=business-value-reports&version=zurich&pubname=zurich-impact&ft:locale=en-US)

    -   Use value reports to evaluate the impact of improvements in key success metrics over time and translate them into operational and monetary value.
    -   View a report created by your delivery team for a product implemented across multiple ServiceNow instances. This feature is available only to Total-tier and Advanced-tier customers, or Guided-tier customers subscribed to the accelerator-for-value reports.
[Gen AI based outcome summarization](https://www.servicenow.com/docs/access?context=gen-ai-based-outcome-summarizatio&version=zurich&pubname=zurich-impact&ft:locale=en-US)

    -   Collect information from multiple areas like adoption, metrics, and initiatives, and generate key insights.
    -   View the outcome metrics for a positive or negative trend.
    -   Monitor which recommended applications are adopted over time to determine effectiveness.
    -   Track the consumption of related accelerators to support outcomes and identify any gaps or underused accelerators.
[Install Impact Value Management Data Collection Content Pack Apps dependent plugins](https://www.servicenow.com/docs/access?context=dc-install-plugins&version=zurich&pubname=zurich-impact&ft:locale=en-US)

Install at least one dependency plugin to enable data collection jobs in Impact value management data collection apps. For Strategic Portfolio Management, two dependency plugins must be installed to enable data collection functionality.

-   **[Work items in the Impact Store Application](https://www.servicenow.com/docs/access?context=creating-work-items-using-recommendations-and-initiatives&version=zurich&pubname=zurich-impact&ft:locale=en-US)**
    -   Create a work item from a capability mapped to a Product Adoption Roadmap, and view the created work item in the Work Items section of the details page of the capability.
    -   Manage and track the SPM and \(CWM\) work items created in Impact on the Work Items page.
    -   Access a centralized Work Items page to track and manage all the SPM and CWM work items created in Impact.
    -   Filter and track work items using aspects like Impact source, state, progress, and status.
-   **[Product Adoption](https://www.servicenow.com/docs/access?context=product-adoption&version=zurich&pubname=zurich-impact&ft:locale=en-US)**
    -   Update information by editing the Usage Status directly on the details page of each capability.
    -   View the last updated information of the Capabilities Map, including the user and the timestamp.
    -   View who is editing the Product Adoption Roadmap when it is in the locked state.
    -   Filter and view overall adoption status by product using the Product filter drop-down list.
    -   Product Adoption Roadmap templates are now available for Customer Service Management, Field Service Management, and Governance, Risk, and Compliance.
    -   Unlock a locked Product Adoption Roadmap if you have an Impact admin or platform owner role. When you unlock it, all changes to the current version are discarded and the Product Adoption Roadmap reverts to its last published version.

    -   View a Now Assist generated summary of description, features, benefits, and related resources when you select a capability.
    -   Filter entitled capabilities by the subscriptions.
    -   View which subscriptions provide entitlement to an entitled capability in the **Included with these subscriptions** section when you select a capability.
-   **[Consumption Report](https://www.servicenow.com/docs/access?context=ide-consumption-report&version=zurich&pubname=zurich-impact&ft:locale=en-US)**

The Consumption report provides an overview of your Impact tier features and their usage, which helps you identify your underused or unused Impact benefits.

[Gen AI based consumption report summarization](https://www.servicenow.com/docs/access?context=ide-consumption-report&version=zurich&pubname=zurich-impact&section=gen-ai-based-consumption-report-summarization&ft:locale=en-US)

    -   Monitor the overall consumption of the accelerator in your plan. This information could include status details for ongoing, completed, and not yet started accelerators.
    -   View the usage details for the Instance observer and Developer Support seats.
    -   View the overall summary of the active Now Support cases and the enhanced case response time for Impact P1 and P2 support cases for your account.

</td></tr><tr><td>

Industrial Process Manager

</td><td>

-   **[Discovered subnets supported by the AMAZING feature](https://www.servicenow.com/docs/access?context=automate-mappings-between-ot-assets-and-equipment-model-entity&version=zurich&pubname=zurich-operational-technology&ft:locale=en-US)**

Use the AMAZING feature, which uses discovered subnets, to identify OT devices and assign them to the correct equipment model entity during OT subnet mapping.

-   **[Map OT devices to equipment model entities from the Equipment Model Manager](https://www.servicenow.com/docs/access?context=map-ot-devices-in-iw&version=zurich&pubname=zurich-operational-technology&ft:locale=en-US)**

Map OT devices to equipment model entities using the **Unmapped OT Devices** and the **All Devices** tabs in the Equipment Model Manager of the Industrial Workspace.

-   **[Generate a location hierarchy](https://www.servicenow.com/docs/access?context=create-location-hierarchy-isa&version=zurich&pubname=zurich-operational-technology&ft:locale=en-US)**

Generate a complete location hierarchy for an ISA equipment model entity tree when no locations exist to establish location references that match the ISA hierarchy.

-   **[Use the OT Network Map to visualize your OT network](https://www.servicenow.com/docs/access?context=utilizing-ot-network-map&version=zurich&pubname=zurich-operational-technology&ft:locale=en-US)**

Visualize your OT network, subnets, and device-to-device connections with the OT Network Map in the Industrial Workspace.

-   **[Set the operational status for equipment model entity sites](https://www.servicenow.com/docs/access?context=equipment-model-workspace&version=zurich&pubname=zurich-operational-technology&ft:locale=en-US)**

Set equipment model entity sites to not in use in the Industrial Workspace by selecting the **Not in use** value for the **Operational Status** field.

-   **[Filter out Not in use and Retired equipment model entities from view](https://www.servicenow.com/docs/access?context=filter-out-non-operational-equipment-model-entities&version=zurich&pubname=zurich-operational-technology&ft:locale=en-US)**

Filter out **Not in use** and **Retired** equipment model entities in the Industrial Workspace using the **Operational Status** field value for a site.

-   **[Add child equipment model entities to a Favorites view in the Industrial Workspace](https://www.servicenow.com/docs/access?context=favorite-child-equipment-model-entity&version=zurich&pubname=zurich-operational-technology&ft:locale=en-US)**

Use the Favorite icon \(![](../image/mark-as-favorite.png)\) to add a child equipment model entity as a favorite in the Equipment Model Manager on the Industrial Workspace. You can then use the **Show Favorites** toggle to display them.

-   **[Assign Processing Order to sort equipment model entities in a site](https://www.servicenow.com/docs/access?context=view-child-entities-equipment-model-entity&version=zurich&pubname=zurich-operational-technology&ft:locale=en-US)**

Use the **Processing Order** field to assign values to an equipment model entity that determines their functional importance in a site.

-   **[The Daily Activity tab in the Equipment Model view in the Industrial Workspace](https://www.servicenow.com/docs/access?context=view-ot-eme-daily-summary&version=zurich&pubname=zurich-operational-technology&ft:locale=en-US)**

View the list of previous day's activities on the **Daily Activity** tab of an OT device. The activities include adding an OT device and changing the field-level attributes for existing OT devices. For example, IP address, Device Criticality, and more.


</td></tr><tr><td>

Instance Data Replication

</td><td>

-   **[Monitor scheduled replication sets](https://www.servicenow.com/docs/access?context=instance-data-replication-dashboard&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)**

Monitor the progress your scheduled replication sets in the IDR Monitoring Dashboard.

-   **[Track scheduled replication requests](https://www.servicenow.com/docs/access?context=set-up-scheduled-replication-idr&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)**

Track the progress of scheduled replication requests in the Scheduled Replication Requests related list.


</td></tr><tr><td>

Instance Scan

</td><td>

-   **[Scan cancellation](https://www.servicenow.com/docs/access?context=hs-cancel-scan&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

Cancel or abort an ongoing scan by either selecting **Cancel Scan** in the scan execution modal or the **Cancel Scan** related link in the results record.

-   **[Queuing of scans](https://www.servicenow.com/docs/access?context=hs-queue-scan&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

Leverage the scan queue feature to line up your scans for automatic execution following the current scan.


</td></tr><tr><td>

Integration Hub

</td><td>

-   **[Generate the parsing phase for REST-based Data Stream actions](https://www.servicenow.com/docs/access?context=data-stream-actions&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US)**

Automatically configure the splitter step, script parser step, and outputs for REST-based Data Stream actions. The **Test REST step** functionality in REST-based Data Stream actions executes a request to the configured REST endpoint, analyzes the response payload, and automatically sets up the parsing and output components.

-   **[Stream Connect enhancements](https://www.servicenow.com/docs/access?context=stream-connect-apache-kafka&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US)**
    -   Use a MID Server cluster, instead of a single MID Server for [message replication](https://www.servicenow.com/docs/access?context=stream-connect-message-replication&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US). With a MID Server cluster, if one of the MID Servers fails, the other MID Servers can share the load of the failed MID Server.
    -   In the [Kafka subscription record](https://www.servicenow.com/docs/access?context=kafka-subscriptions-statistics&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US), view the estimated time required for a consumer to process the current queue. The subscription record also links to the consumer record, so that you can see which consumer is processing the queue.
    -   Specify a compression format for Stream Connect producers with the **com.glide.kafka\_producer.compression\_type** system property. Stream Connect supports the GZIP and LZ4 compression formats.
-   **[View alerts in the Stream Connect dashboard](https://www.servicenow.com/docs/access?context=stream-connect-dashboard&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US)**

Get detailed information about alerts, including their severity level, state, type, and the affected entity in the Stream Connect dashboard.

-   **[Test connection aliases directly from configuration templates](https://www.servicenow.com/docs/access?context=test-alias-configuration-template&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US)**

For aliases using a configuration template, you can configure a Test Action field. This field enables you to test a connection from within the Action Properties section of actions in Workflow Studio.

-   **[Support for PowerShell version 6.0 or later in the PowerShell step](https://www.servicenow.com/docs/access?context=powershell-step-action-designer&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US)**

Enable the PowerShell step to use a newer version of PowerShell by adding the MID Server property **mid.property.ihub.prefer\_powershell6Plus** and setting it to `true`.

-   **[Use WS-Security in a SOAP step on a MID Server](https://www.servicenow.com/docs/access?context=soap-step-action-designer&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US)**

Enable a WS-Security policy in a SOAP step running on a MID Server.

-   **[Delay parallel loading in custom \(load by script\) data sources](https://www.servicenow.com/docs/access?context=custom-type-data-source&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US)**

Configure a delay for parallel loading in custom data sources. When the data source is called, the parallel loading is scheduled to run after the configured amount of time.

-   **Spoke-specific AI agents**

AI agents that implement different agentic workflows are available for various spokes. Use these spoke-specific AI agents to execute agentic workflows.

-   **[Save draft, publish, update external trigger definition, and support domain separation](https://www.servicenow.com/docs/access?context=create-saved-external-trigger&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US)**

The external trigger definition is updated to match the trigger builder so that the external trigger definition supports the saving of draft, publishing, updating external trigger definition, and supporting domain separation.

-   **[Create and manage external event sources](https://www.servicenow.com/docs/access?context=manage-external-event-sources&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US)**

Define and manage custom trigger definitions after creating external event sources.


</td></tr><tr><td>

Intelligence for CSM

</td><td>

-   **[Guided Decisions - Enable Guided Decisions as a Playbook Activity with Inputs and Outputs](https://www.servicenow.com/docs/access?context=add-gd-input-output-playbook&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

Added support for the Guided Decision with Inputs and Outputs activity in Playbook. Use this activity to embed decision trees that accept inputs and generate outputs, guiding users through complex decisions within your playbooks.

-   **[Recommended Actions - View the relevancy score of the AI search results](https://www.servicenow.com/docs/access?context=nba-use-ai-search&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

View the relevancy score on the search result recommendation cards in the Search tab of the Recommended Actions panel for the default guidance for search results, Attach and share article, Share KB in chat interactions, and all no-code \( Link incident to current case, Link problem to current case, and Link change request to current case\) guidances. To enable this feature, you must enable the Show relevancy score for results check box in the Context form.

-   **[Recommended Actions – Limit the number of search results for more precise output](https://www.servicenow.com/docs/access?context=nba-use-ai-search&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

Limit the number of search results \(Top N\) that appear in the AI search tab in the Recommended Actions context side panel. To configure top N search results, you must enable the Top N check box in the Context form and then define the Search Results Limit in the Search Application Configuration.

-   **[Recommended Actions - Filter search results across multiple sources in the Contextual side panel](https://www.servicenow.com/docs/access?context=nba-use-ai-search&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

Filter search results corresponding to multiple sources in the AI search tab of the Recommended Actions contextual side panel. You can also filter the search results at the facet-level.

-   **[Recommended Actions – Track the AI search usage trends with the AI search analytics dashboard](https://www.servicenow.com/docs/access?context=nba-use-ai-search&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

Track and analyze the AI search usage in Recommended Actions using the AI search analytics dashboard. The AI search events and actions performed by the agent are captured in the Search Events, Search Source Events, Search Signal Events, Search Result Event, and Search Result Event Action tables. This data is used in the AI search analytics dashboard.

-   **[Recommended Actions - Read-only access to TI solutions for the Resource Generator author role](https://www.servicenow.com/docs/access?context=ra-csm-installed-components&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

Access Task Intelligence \(TI\) solution definitions in read-only mode as a Resource Generator author \[sn\_nb\_action.resource\_generator\_author\] to configure recommendations with Machine Learning \(ML\) solutions from TI models. In other words, the sn\_ti\_admin.tia\_user role is added to the Resource Generator author role.

-   **[Recommended Actions - Filter search results across multiple sources on the Search page](https://www.servicenow.com/docs/access?context=nba-use-ai-search&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

Filter search results corresponding to multiple sources on the Search page. You can also filter the search results at facet-level.

-   **[Recommended Actions - Optimize the Recommended Actions refresh behavior by excluding non-critical field updates](https://www.servicenow.com/docs/access?context=ra-csm-contexts-create&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

Exclude the non-critical fields from triggering a Recommended Actions refresh on the record pages by adding the non-critical fields to the **Exclude fields** field on a context record. In a child context, you can also include the field exclusions of the parent context. You can enhance a user’s UI experience when you prevent excessive UI updates and still ensure that relevant updates trigger as intended.

-   **[Recommended Actions - Trigger Refresh for Recommendations explicitly or based on UI events](https://www.servicenow.com/docs/access?context=ra-csm-config-data-broker&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

Trigger recommendations refresh in the Recommended Actions tab on the contextual side panel when a UI or back-end event update is made. This provides dynamic and more contextually relevant recommendations based on the outcome of UI and back-end events. To trigger a recommendations refresh:

    -   configure UI component’s Data Broker in the UI builder for UI events
    -   execute the ForceRefreshRecommendationsscript include for back-end events
-   **[Recommended Actions - Configure dynamic JSON-based context inputs](https://www.servicenow.com/docs/access?context=ra-csm-create-context-inputs&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

Configure JSON-based context inputs in a context to populate accurate recommendations corresponding to dynamically changing contexts. You can conﬁgure parameters associated with the context table along with context table parameters. To support scenarios where a single workflow may leverage multiple active contexts simultaneously to generate recommendations. This uses the context inputs in rule condition builders, resource generators, and recommendation-action mappings, with minimal performance impact and backward compatibility.

-   **[Recommended Actions - Enhanced KB article sharing for Agents](https://www.servicenow.com/docs/access?context=ra-csm-guidances-attach-share-article&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

Identify the Knowledge Base \(KB\) articles that are not accessible to the case requester with the help of a Lock icon. In the recommendations on the contextual side panel of the CSM Configurable Workspace, a Lock icon on a recommendation card denotes that the recommended KB article cannot be accessed by the case requester.

-   **[Process Mining - SLA breach analysis](https://www.servicenow.com/docs/access?context=csm-integration-po&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US)**

Identify and analyze cases where service level agreements \(SLAs\) have been violated. The SLA breach analysis project provides insights into the root causes of breaches, highlights bottlenecks, and recommends improvements to optimize the performance of your processes.

-   **[Quick start tests for Customer Service Management](https://www.servicenow.com/docs/access?context=quick-start-tests-csm&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

After upgrades and deployments of new applications or integrations, run quick start tests to verify that Customer Service Management works as expected. If you customized Customer Service Management, copy the quick start tests and configure them for your customizations.


</td></tr><tr><td>

Interview management

</td><td>

-   **[Define your interview setup](https://www.servicenow.com/docs/access?context=add-interview-phase&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

Configure interview phases with custom names, durations, and other key parameters, and then use them to efficiently schedule interviews, enhancing transparency and saving time.

-   **[Request applicant to share scheduling preferences](https://www.servicenow.com/docs/access?context=request-applicant-availability&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

Request applicants on a job requisition to share their scheduling preferences to plan a seamless interview process.

-   **[Request interviewer to share scheduling preferences](https://www.servicenow.com/docs/access?context=request-interviewer-availability&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

Request interviewers on a job requisition to share their scheduling preferences to plan a seamless interview process.

-   **[Share scheduling preferences](https://www.servicenow.com/docs/access?context=share-availability-interviewer&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

As an interviewer, when requested by recruiters, share your scheduling preferences to help them schedule interviews accordingly.

-   **[View applicant's scheduling preferences](https://www.servicenow.com/docs/access?context=view-applicant-availability&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

View the scheduling preferences shared by applicants to schedule interviews accordingly.

-   **[View interviewer's scheduling preferences](https://www.servicenow.com/docs/access?context=view-interviewer-availability&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

View the scheduling preferences shared by interviewers and schedule interviews accordingly.

-   **[Schedule an interview](https://www.servicenow.com/docs/access?context=schedule-interview&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

Schedule interview with applicants on a job requisition to get started with the interview journey.

-   **[Manage interviews as a recruiter](https://www.servicenow.com/docs/access?context=manage-interviews-recruiter&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

As a recruiter or recruitment coordinator, manage interviews for a job requisition as needed. You can update the interview status, view feedback, send reminders, complete or cancel interviews, and more.

-   **[Manage interviews as an interviewer](https://www.servicenow.com/docs/access?context=manage-interviews-interviewer&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

As an interviewer, view the details of all the interviews that you’re a part of and manage them as required.

-   **[Provide interview feedback as a recruiter](https://www.servicenow.com/docs/access?context=provide-interview-feedback-recruiter&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

As a recruiter or recruitment coordinator, provide feedback for interviews that you're a part of.

-   **[Provide interview feedback as an interviewer or hiring manager](https://www.servicenow.com/docs/access?context=provide-interview-feedback-hm-interviewer&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

As an interviewer or hiring manager, provide timely and constructive feedback on the interviews in which you participate, to support application comparison and well-informed hiring decisions.


</td></tr><tr><td>

Journey designer

</td><td>

[Zurich Patch 1](../quality/zurich-patch-1.md)

-   **[Generate onboarding ramp-up agentic workflow](https://www.servicenow.com/docs/access?context=onboarding-ramp-up-plan-agentic-wf&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

Use the Generate onboarding ramp-up plan agentic workflow to establish an efficient process for generating onboarding plans that are personalized for each new employee joining your organization.

    |Agentic workflow name|Description|
    |---------------------|-----------|
    |Generate onboarding ramp-up plan|AI agents work together to generate personalized plans that are designed to ramp up the knowledge and skills of new employees who are beginning to embark on their onboarding journey.|

-   **[New third-party AI model provider options available for all Now Assist applications](https://www.servicenow.com/docs/access?context=exploring-large-language-models&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Google Gemini and AWS Claude are available for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.


Zurich Early Availability

-   **[Configure the journey overview page](https://www.servicenow.com/docs/access?context=manager-journeys-view&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

As an admin, you can now configure the journey overview page and hide the Task Templates and Create a Journey for Your Team widgets.


</td></tr><tr><td>

Knowledge Center

</td><td>

-   **[Search knowledge article](https://www.servicenow.com/docs/access?context=search-knowledge-article&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)**

Build a complete and accurate knowledge base, focus on continuous improvement by discovering and filling content gaps, removing redundant information, and optimizing existing articles for better quality.


-   **[Knowledge Center Article Optimization](https://www.servicenow.com/docs/access?context=knowledge-center-article-optimization&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)**

Improve the quality and health of your knowledge articles by using the Article Optimization tool in the Knowledge Center to scan the articles, and get instant, actionable feedback.


-   **[Generate and edit articles using Now Assist in the Knowledge Center article editor](https://www.servicenow.com/docs/access?context=km-article-editor&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)**

Use the editing tools in the Knowledge Center to format knowledge article content such as text, images, and media.


-   **[Potential knowledge gaps](https://www.servicenow.com/docs/access?context=understanding-knowledge-gaps&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)**

Proactively identify and fill potential knowledge gaps. Identify missing knowledge articles and recurring issues that have incomplete or no knowledge article to refer to.


</td></tr><tr><td>

Knowledge Graph

</td><td>

-   **[Tagging in Knowledge Graph Designer](https://www.servicenow.com/docs/access?context=tagging-in-knowledge-graph&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

The Knowledge Graph landing page now includes a dedicated tagging section that allows users to create, edit, and manage tags.


-   **[Using Enterprise graph schema](https://www.servicenow.com/docs/access?context=global-graph-schema&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Enterprise Graph is a pre-configured Knowledge Graph schema that eliminates the need for custom schema creation in KG designer. By mapping all tables, the Enterprise Graph schema enhances the breadth of query capabilities, enabling database queries across all instance tables.


-   **[Tagging in Knowledge Graph Designer](https://www.servicenow.com/docs/access?context=tagging-in-knowledge-graph&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Tags are lists of key tables that are important for answering natural language questions. They provide hints to Enterprise Graph on which tables to prioritize when retrieving information, thereby improving the accuracy of results.


-   **[Test a Knowledge Graph schema](https://www.servicenow.com/docs/access?context=test-a-knowledge-graph-schema&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Enter a query and test the Knowledge Graph schema using different LLM options. You can also add previous conversations before you run the query.


-   **[Configure LLM for Knowledge Graph](https://www.servicenow.com/docs/access?context=configure-gpt-4-0-for-knowledge-graph&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Select and configure between Now LLM Service, Azure OpenAI GPT-4.1 and GPT-4.1 mini, Google Gemini 2.0 Flash and 2.5 Pro, and AWS Anthropic Claude 3.7 Sonnet LLM providers with ServiceNow third-party model strategy.


</td></tr><tr><td>

Knowledge Management

</td><td>

-   ****

Boost efficiency and simplify operations by replacing the existing Knowledge Management processes built on workflow with the latest and innovative, simple-to-use visual flow designers.


</td></tr><tr><td>

Lead-to-Cash Process Management

</td><td>

-   **[Set up business objects](https://www.servicenow.com/docs/access?context=create-business-object-group-define-entity-relationship&version=zurich&pubname=zurich-order-management&ft:locale=en-US)**

Create a visual overview of the sales process hierarchy by defining and setting up business object groups of sales entities and their relationship with other entities. For example, an opportunity-to-cash business object group could include business entities such as an opportunity, opportunity line, opportunity task, quote, order, and so on.

-   **[Create sales process records](https://www.servicenow.com/docs/access?context=create-sales-process-record&version=zurich&pubname=zurich-order-management&ft:locale=en-US)**

Enable sales managers and contract administrators to create sales process records for individual accounts.

-   **[Monitor sales process using sales dashboard](https://www.servicenow.com/docs/access?context=navigating-sales-process-dashboard&version=zurich&pubname=zurich-order-management&ft:locale=en-US)**

Enable sales managers and contract administrators to view and manage the sales process from a single interface. The dashboard provides the following capabilities:

    -   Visualize the sales process in a node map, showing relationships between different sales entities in a hierarchical format.
    -   Toggle between hard links \(actively monitored\) and soft links \(database relationships\) to manage the monitoring scope.
    -   Use checklists to capture the steps and activities required for a sales process.
    -   View details for each of the associated sales entities, such as line items, tasks, emails, activities, and line characteristics.
    -   View, upload, and download files and attachments related to the sales process record or child entities.
-   **[Customize the sales dashboard](https://www.servicenow.com/docs/access?context=customizing-sales-process-dashboard&version=zurich&pubname=zurich-order-management&ft:locale=en-US)**
    -   Customize the number of levels displayed in the nodal hierarchy by configuring the **sn\_l2c\_cockpit.node\_default\_levels** system property.
    -   Customize the details you want to display on the node map tiles using decision tables.
    -   Create predefined filters to consolidate and view hard-linked records-related tasks. For example, you could create a new filter option to filter in-progress tasks.
-   **[Create business process tasks](https://www.servicenow.com/docs/access?context=create-business-process-tasks&version=zurich&pubname=zurich-order-management&ft:locale=en-US)**

Sales managers and contract administrators can create business process tasks and associate them with sales process records or business process records. The linked business process task can be viewed on the Tasks tab of the sales process record.


</td></tr><tr><td>

Legal Conflict of Interest

</td><td>

-   **[Configure risk assessment](https://www.servicenow.com/docs/access?context=lsd-coi-config-risk-fac&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

The risk assessment utility evaluates conflict of interest disclosures against predefined risk factors to calculate a risk score and determine the risk level \(Low, Medium, or High\). The risk level automatically triggers the appropriate approval workflow. The utility supports three evaluation types: Condition, Subflow, and AI skill.

**Note:** AI skill evaluation is available once you have installed and configured Now Assist for Legal Service Delivery \(LSD\).

-   **[Submit COI request using Now Assist conversational intake](https://www.servicenow.com/docs/access?context=now-assist-lsd-convi&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

Using natural language to submit a conflict of interest request from Now Assist in the Virtual Agent interface reduces the effort required to fill in form fields because details provided in natural language are automatically populated into the intake form. Achieve faster resolution due to automated risk assessment that routes requests to the appropriate approval workflow based on calculated risk scores.

**Note:** The conversational intake functionality is available only once you have installed and configured Now Assist for Legal Service Delivery \(LSD\).


</td></tr><tr><td>

Legal Hold Notification

</td><td>

-   **[Legal hold matter management](https://www.servicenow.com/docs/access?context=lg-hold-notif-landing-page&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

Manage legal hold matters by submitting, updating, tracking, and closing them through a streamlined process that reduces effort and ensures organizational compliance.


-   **[Submitting legal hold matter](https://www.servicenow.com/docs/access?context=submit-lg-hold-notif-matter&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

Submit a legal hold matter to initiate the data preservation process when a legal hold is issued.


-   **[Issuing legal hold notice](https://www.servicenow.com/docs/access?context=issue-lg-hold-notif-matter&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

Issue a legal hold notice to custodians to initiate timely data preservation, ensure accountability, and reduce the risk of data loss.


-   **[Legal hold notice acknowledgement](https://www.servicenow.com/docs/access?context=acknow-lg-hold-notif&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

Record custodian acknowledgments of legal hold notices to confirm their responsibility to preserve data and ensure accountability.


-   **[Assign new custodians](https://www.servicenow.com/docs/access?context=add-new-custodian-lg-hold-notif&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

Assign newly identified custodians to existing legal hold matters to ensure comprehensive and up-to-date data preservation.


-   **[Acknowledge reminders](https://www.servicenow.com/docs/access?context=send-reminder-for-acknowledgment&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

Send reminders to custodians who haven’t acknowledged legal hold notices to ensure accountability in data preservation.


-   **[Closing legal hold matter](https://www.servicenow.com/docs/access?context=close-lg-hold-notif-matter&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

Close a legal hold matter once the hold is lifted to complete the data preservation life cycle.


</td></tr><tr><td>

Legal Matter Management

</td><td>

-   **[Attorney-Client Privilege](https://www.servicenow.com/docs/access?context=lsd-acp-landing&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

Protect sensitive legal information by marking legal matters as Privileged &amp; Confidential, helping to ensure access is restricted to only authorized stakeholders.


</td></tr><tr><td>

Legal Request Management

</td><td>

-   **[Attorney Client Privilege](https://www.servicenow.com/docs/access?context=lmm-acp-landing&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

Protect sensitive legal information by marking legal matters as Privileged &amp; Confidential, helping to ensure access is restricted to only authorized stakeholders.


</td></tr><tr><td>

Lifecycle Events

</td><td>

-   **[Lifecycle Events logging](https://www.servicenow.com/docs/access?context=le-logging&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

Capture events that occur in a Lifecycle Events case by enabling logging for the Lifecycle Events application. Give organization administrators the ability to view the event logs that are generated to identify errors or to acquire information about the processes that ran in a Lifecycle Events case.


</td></tr><tr><td>

Localization Workspace

</td><td>

-   **Guided Setups for [Configuring Localization Workspace](https://www.servicenow.com/docs/access?context=configuring-localization-workspace&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

Two Guided Setups are available in the interface to assist admins with configuration of Localization Workspace. Guided Setups provide an outline and actionable steps for the configuration process. From version 2.0.2.

-   **[Configuration hub](https://www.servicenow.com/docs/access?context=lw-configuration-hub&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

Configuration Hub provides centralized access to the tables and properties often used by admins. You can update the tables and properties of dependent applications such as Dynamic Translation without leaving the Localization Workspace interface. From version 2.0.2.

-   **[Language Groups](https://www.servicenow.com/docs/access?context=lw-configure-language-groups&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

You can optionally preconfigure language groups. Your users save time and effort by selecting an available language group rather than adding each target language individually to a translation request. From version 2.0.2.

-   **[Bulk select or deselect for content items](https://www.servicenow.com/docs/access?context=lw-request-translations-scope&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

When users create a translation request, Localization Workspace retrieves and displays all translatable documents for a content type. A bulk select/deselect option is available on the retrieved list to enhance efficiency. From version 2.0.2.

-   **[Text search for content items](https://www.servicenow.com/docs/access?context=lw-request-translations-scope&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

When users create a translation request, Localization Workspace retrieves and displays translatable content items in a list. You can search for terms in the titles of content items to filter the retrieved list. From version 2.0.2.

-   **[Optional due date field for translation requests](https://www.servicenow.com/docs/access?context=lw-estimate&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

Your users can enter a due date when creating a translation request. Translation request due dates can be used to trigger [email notifications](https://www.servicenow.com/docs/access?context=lw-email-notif-due-dates&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US). From version 2.0.2.


</td></tr><tr><td>

MCP Server Console

</td><td>

-   **[Create tools from additional capabilities for use with ServiceNow MCP clients](https://www.servicenow.com/docs/access?context=create-tool-mcp-server&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

With this release, Moveworks is shipping a Moveworks Quickstart Server. This server allows users to pilot access to upcoming capabilities like Knowledge graph, Subflow, Action, and scripted REST APIs for use with Moveworks MCP client, and ServiceNow Model Context Protocol Client application. These tools can only be added to Moveworks Quickstart Server.


-   **[Get started with the preconfigured Quickstart Server](https://www.servicenow.com/docs/access?context=exploring-mcp-server-console&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Get started learning about MCP Server Console and connecting MCP Server Console clients to a ServiceNow instance with the preconfigured Quickstart Server. The Quickstart Server includes tools for looking up and summarizing incident and case records.

-   **[Create MCP servers](https://www.servicenow.com/docs/access?context=create-mcp-server&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Create MCP Server Console servers that expose different tools for different use cases, such as for HR or IT workflows, or for different MCP Server Console clients.

-   **[Create tools from Now Assist skills](https://www.servicenow.com/docs/access?context=create-tool-mcp-server&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Create tools for MCP Server Console servers from Now Assist skills and configure which fields are exposed as tool inputs.

-   **[Connect to MCP clients using an OAuth inbound integration](https://www.servicenow.com/docs/access?context=connect-mcp-server-client&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Create an OAuth inbound integration to use when configuring MCP Server Console clients to connect to an MCP Server Console server.


</td></tr><tr><td>

MID Server

</td><td>

-   **[ITOM Infra Services Workspace](https://www.servicenow.com/docs/access?context=itom-infra-srv-wrksp-mid&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

The ITOM Infra Services Workspace provides a concise overview of MID Server activity. The dashboard integrates several previously disparate tables so that issues can be monitored and resolved. The workspace provides real-time monitoring, proactive alerts, automation of common tasks, and centralized diagnostics to reduce downtime and support tickets.

-   **[MID Guardian Agent](https://www.servicenow.com/docs/access?context=mid-guardian&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)**

The MID Guardian Agent is an advanced AI feature within the MID Server ecosystem/ITOM Infra Services workspace, designed to proactively assist users in diagnosing and resolving issues related to configuration, connectivity, upgrades, and operations. By intelligently analyzing logs, signals, and runtime behaviors, it offers guided troubleshooting steps, automated fixes, and predictive insights. This significantly reduces Mean Time to Repair \(MTTR\) and enhances the reliability and operational efficiency of the MID server.


</td></tr><tr><td>

Manufacturing Commercial Operations

</td><td>

-   **[Quality issue management](https://www.servicenow.com/docs/access?context=mco-quality-issue-management&version=zurich&pubname=zurich-manufacturing&ft:locale=en-US)**

The MCO agents portal enables the manufacturers to identify, manage, and resolve product quality issues throughout the entire life cycle, from initial detection through remediation and closure.

-   **[Data model](https://www.servicenow.com/docs/access?context=data-model&version=zurich&pubname=zurich-manufacturing&ft:locale=en-US)**

The quality issue management data model facilitates the OEMs to understand the quality issue management tables and their functions.

-   **[Phases and Sub-phases](https://www.servicenow.com/docs/access?context=mco-phases-and-subphases&version=zurich&pubname=zurich-manufacturing&ft:locale=en-US)**

The MCO agents portal enables the manufacturers to create phases and sub-phases within a recall campaign and launch it for selected assets, and notify the targeted dealers.

-   **[Pre-authorization request](https://www.servicenow.com/docs/access?context=pre-authorization-request&version=zurich&pubname=zurich-manufacturing&ft:locale=en-US)**

The dealer portal enables the dealer to initiate the pre-authorization request to confirm whether certain parts, labor fees, or repairs are covered under a warranty or service contract.

-   **[Recall campaign](https://www.servicenow.com/docs/access?context=mco-rcl-clms&version=zurich&pubname=zurich-manufacturing&ft:locale=en-US)**

The dealer portal enables the dealer to initiate reimbursement claim requests from the OEM for the work performed on the recalled products.

-   **[Repair claims](https://www.servicenow.com/docs/access?context=mco-warranty-clms&version=zurich&pubname=zurich-manufacturing&ft:locale=en-US)**

The dealer portal enables the dealer to raise a reimbursement claim request for the repair of an equipment or product that is under a warranty contract.

-   **[Sales promotion](https://www.servicenow.com/docs/access?context=mco-sls-prom-clms&version=zurich&pubname=zurich-manufacturing&ft:locale=en-US)**

The dealer portal enables the dealers to raise post sales promotion claims from the OEM depending on the claim case.

-   **[Dealer portal](https://www.servicenow.com/docs/access?context=mco-dealer-portal&version=zurich&pubname=zurich-manufacturing&ft:locale=en-US)**

The dealer portal helps the agent to manage the day-to-day business activities and monitor the real-time data insight.

-   **[Plugins installed with MCO](https://www.servicenow.com/docs/access?context=manufacturing-commercial-operations-plugins&version=zurich&pubname=zurich-manufacturing&ft:locale=en-US)**

The new MCO plugin enables you to install the Manufacturing Commercial Operations and other dependent modules.


</td></tr><tr><td>

Mastercard Spoke

</td><td>

-   **[Pre-arbitration and arbitration case filing](https://www.servicenow.com/docs/access?context=mastercard-spoke&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US)**

Dispute agents \(issuers\) can create pre-arbitration cases and escalate them to arbitration, or directly create arbitration cases by skipping pre-arbitration, using the new Mastercard spoke actions.

New Mastercard Spoke actions include:

<table id="table_yq4_v2h_tfc"><thead><tr><th>

Category

</th><th>

Spoke actions

</th></tr></thead><tbody><tr><td>

Mastercom Case Filing Management

</td><td>

-   Create Case Request Builder
-   Create Case Response Parser
-   Look up Case Documents Request Builder
-   Look up Case Documents Response Parser
-   Look up Cases Status
-   Take Action on Case
-   Look up List of Claims


</td></tr><tr><td>

Mastercom Chargeback Management

</td><td>

-   Look up Chargeback Documents Request Builder
-   Look up Chargeback Documents Response Parser


</td></tr><tr><td>

Health Check

</td><td>

Look up API Suite Health

</td></tr></tbody>
</table>


</td></tr><tr><td>

Mobile Platform

</td><td>

-   **[Client-side localization](https://www.servicenow.com/docs/access?context=localization-client&version=zurich&pubname=zurich-mobile&ft:locale=en-US)**

Use the Mobile Custom Localization app, available from mobile client version 20.6, to let mobile users view app content in any language. This feature improves platform consistency and accessibility for global users. The ServiceNow Store app provides a collection of mobile strings that automatically populates the instance with translatable content required for localization. Once these strings are translated into a custom language, the mobile app automatically retrieves and displays them within the app interface.


-   **[Improved error handing for uploads manager](https://www.servicenow.com/docs/access?context=mobile-activity-stream-task&version=zurich&pubname=zurich-mobile&ft:locale=en-US)**

Use the improved error handling in the upload manager to confirm that the necessary files are uploaded successfully. This feature is available in all areas of the ServiceNow mobile applications where you can upload attachments. This includes the following:

    -   Activity stream
    -   Input form screen with an attachment input type
    -   Input form screen with an attachment input action
    -   Functions of type attachment
    -   Cabrillo JS events within a web page
-   **[Option to save videos and photos locally when using ServiceNow mobile apps](https://www.servicenow.com/docs/access?context=media-saving-mobile-apps&version=zurich&pubname=zurich-mobile&ft:locale=en-US)**

Enable users to save and retrieve pictures and videos taken with the camera on their ServiceNow mobile app, directly to their device. By default, these images are saved for 24 hours on the phone’s local storage. You can set the storage time to be from 1 to 168 hours \(1 week\).

-   **[Additional descriptive element of type card for input form screens](https://www.servicenow.com/docs/access?context=descriptive-elements-script&version=zurich&pubname=zurich-mobile&ft:locale=en-US)**

Add cards created in the Mobile Card Builder as a descriptive element in input form screens. Descriptive elements offer more context to users, making it clearer as to what is required for certain inputs within an input form screen.

-   **[Page menu button added to input form screen](https://www.servicenow.com/docs/access?context=parameter-input-screen&version=zurich&pubname=zurich-mobile&ft:locale=en-US)**

Display a page menu button for input form screens with more than two pages, showing users the current page that they are on, such as "Page 3 of 5." Tapping the button opens a page menu that lists all available pages and their level of completeness. This list helps users track their progress in completing an input form.

-   **[Complete an input form screen in a non-sequential order](https://www.servicenow.com/docs/access?context=parameter-input-screen&version=zurich&pubname=zurich-mobile&ft:locale=en-US)**

Work on all pages of an input form screen, even if required fields are not completed. Users can use the next and previous buttons at all times, enabling them to complete the form in a non-sequential manner. In addition, users can use the page menu to work on any page of their choosing.

-   **[Error indicator for failed submissions in input form screen](https://www.servicenow.com/docs/access?context=parameter-input-screen&version=zurich&pubname=zurich-mobile&ft:locale=en-US)**

View an information icon in the top menu bar in cases where a submitted input form contains at least one error. The icon remains accessible when working through all input form screen pages. Tapping the icon opens a page that lists the validation errors, enabling users to correct these errors and submit an error-free input form.

-   **[Slider option for adding numeric values in input form screen](https://www.servicenow.com/docs/access?context=parameter-screen-var-attr&version=zurich&pubname=zurich-mobile&ft:locale=en-US)**

Configure sliders as an additional method for users to add numeric values in an input form screen. Sliders offer the advantage of defining minimum, maximum, incremental, and default values.

-   **[New icons added that you can use in your mobile apps](https://www.servicenow.com/docs/access?context=mobile-icon-reference&version=zurich&pubname=zurich-mobile&ft:locale=en-US)**

Use new icons that have been added to the following font families in your mobile apps:

    -   Actions font icons
    -   Screen font icons
    -   Mobile card font icons
    -   Image icons
-   **[Mobile App Builder and Mobile Card Builder Studio integration](https://www.servicenow.com/docs/access?context=mab-studio-integration&version=zurich&pubname=zurich-mobile&ft:locale=en-US)**

Develop and modify mobile applications and cards in ServiceNow Studio. Utilize all your necessary tools within a single, cohesive development environment.

-   **[Now Assist in Virtual Agent](https://www.servicenow.com/docs/access?context=now-assist-mobile-va&version=zurich&pubname=zurich-mobile&ft:locale=en-US)**

The following features have been added to ServiceNow Now Assist in Virtual Agent:

    -   Upload documents and files with Doc QnA to have Now Assist generate summaries or answer questions about them.
    -   Search the internet from within Virtual Agent using web search mode.
    -   Capture and analyze data from a variety of visual sources such as images, emails, handwritten notes, websites, and applications using ServiceNow AI Lens.
    -   View shared files when using people citations.
-   **[Now Assist Skill Kit integration](https://www.servicenow.com/docs/access?context=now-assist-skill-kit-for-mobile&version=zurich&pubname=zurich-mobile&ft:locale=en-US)**

Create and use custom Now Assist skills in your mobile app using Now Assist Skill Kit.


</td></tr><tr><td>

Model Risk Management

</td><td>

-   **[Manage model risks](https://www.servicenow.com/docs/access?context=exploring-mrm&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

Manage the risks associated with the use of models using the Model Risk Management application. It offers a structured approach to identify, assess, validate, and address model risks throughout the model life cycle. This approach reduces operational and compliance risks caused by inconsistent or inadequate model oversight.

-   **[Model Risk Workspace](https://www.servicenow.com/docs/access?context=model-risk-workspace&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

Get a comprehensive overview of all items requiring attention from Model Risk Management governance and model validators. The Model Risk Workspace gives model risk governance team and model validators a centralized location to monitor, track, and act on model-related tasks and issues. It organizes information into tabs, making it easier to prioritize tasks.

-   **[Request a new model](https://www.servicenow.com/docs/access?context=request-new-model&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

Request a new model by providing details such as the purpose, owner, model complexity, and expected outputs. It helps streamline the model onboarding process and confirms that all required information is captured upfront for the Model Governance team to review.

-   **[Perform model risk assessment](https://www.servicenow.com/docs/access?context=perform-model-risk-assessment&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

Perform model risk assessments initiated by the Model Governance team to identify and evaluate risks associated with quantitative models using the Model Risk Management application. It helps Model Owners to assess potential risks early and supports the Model Governance team in ensuring model compliance and reliability.

**Note:** You can perform model risk assessment in the Initiation, Pre-deployment, and Monitor stages of a model.

-   **[Perform model validation](https://www.servicenow.com/docs/access?context=perform-model-risk-validation&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

Perform model validation to assess and validate models, collect required documents, report issues, and determine whether a model is fit for use. This process confirms that models meet required standards and are ready for deployment.

**Note:** You can perform model risk validation in the Pre-deployment and Monitor stages of a model.

-   **[Schedule assessment and validation tasks](https://www.servicenow.com/docs/access?context=schedule-assessment-and-validation-tasks&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

Schedule assessments and validations for models in the Monitor stage either manually or automatically.

    -   Schedule model risk assessment and validation directly from the model risk record to ensure regulatory compliance and effective risk management. For more information, refer to [Schedule assessment and validation tasks](https://www.servicenow.com/docs/access?context=schedule-assessment-and-validation-tasks&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US).
    -   Configure frequency and filter conditions in model workflow settings to create model risk assessments and validations automatically for models that meet the defined criteria. For more information, refer to [Schedule assessment and validation tasks automatically](https://www.servicenow.com/docs/access?context=create-model-workflow-settings&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US).
-   **[Reassign model assessments and validations](https://www.servicenow.com/docs/access?context=reassign-a-model-risk-task&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

Reassign a model risk assessment and validation to another stakeholder from the model risk record when the task is in progress state. It confirms that the task continues without delay when the original assignee is unavailable.

-   **[Copy assessment responses](https://www.servicenow.com/docs/access?context=copy-assessment-responses-mrm&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

Copy responses from the most recent completed assessment into new assessments. Respondents can review and edit the pre-filled responses before submission to save time and ensure consistency.

**Note:** You can copy responses only from model risk assessments, not from model validations.

-   **[Create an issue for model](https://www.servicenow.com/docs/access?context=create-an-issue-for-model-risk&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

Add or create model issues and their remediation actions. Capture validation findings or performance problems and follow them through to resolution.

-   **[Override model ratings](https://www.servicenow.com/docs/access?context=override-model-ratings&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

Override the risk rating and materiality tier of a model manually at any stages of its life-cycle. This helps maintain data accuracy, transparency, and governance when business context or expert judgment requires adjustments to system-calculated values.

-   **[Centralized model documentation](https://www.servicenow.com/docs/access?context=doc-linked-parent-rec&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)**

Store and manage all model-related documents in one place with version control, audit readiness, and traceability. Create, share, upload, and track documents throughout the model life cycle.


</td></tr><tr><td>

Next Experience

</td><td>

-   **[Lazy loading of Workspace pages user preference available](https://www.servicenow.com/docs/access?context=next-experience-workspace-preferences&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US)**

Control how your Workspace pages are loaded, either all at once or as needed, by using the new Workspace lazy load user preference. Lazy loading is enabled by default and displays content dynamically, reducing page load times. See the Accessibility information section for additional details.

-   **[Use the menu toggle to view the Now Assist menu in wide mode](https://www.servicenow.com/docs/access?context=using-the-next-experience-global-header&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US)**

View the Now Assist menu in wide mode to reduce the need for scrolling and truncating content.

-   **[Configure Next Experience accessibility preferences](https://www.servicenow.com/docs/access?context=next-experience-accessibility-preferences&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US)**

Use a new accessibility preference to keep page alerts visible. See the Accessibility information section for additional details.

-   **[Usage Analytics utility menu available](https://www.servicenow.com/docs/access?context=using-the-next-experience-global-header&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US)**

Obtain usage analytic data for your applications and web pages with the Usage Analytics utility menu. The Usage Analytics menu appears for those users with the analytics\_viewer role.

-   **[View the number of active calls from the OpenFrame phone icon](https://www.servicenow.com/docs/access?context=using-the-next-experience-global-header&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US)**

View the number of active calls from the numbered badge on the OpenFrame phone icon.


</td></tr><tr><td>

Notifications

</td><td>

-   **[Email diagnostics dashboard](https://www.servicenow.com/docs/access?context=email-diagnostics-dashboard&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

With email diagnostics you can track bounce management, email delivery metrics, email sender, and reader jobs health.

-   **[Email agentic workflow](https://www.servicenow.com/docs/access?context=use-agentic-ai-notifications&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

With email agentic workflow you can intelligently handle new email agentic workflows by identifying intent, executing actions, &amp; drafting appropriate email responses.


</td></tr><tr><td>

Notify

</td><td>

-   **[Notify workflow activities](https://www.servicenow.com/docs/access?context=c_NotifyActivities&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)**

Manage the subflows for Notify use cases with the following actions.

    -   Input - Advanced: This action is intended for advanced scenarios where the **Say and Play** activity must be repeated multiple times.
    -   Get Notify Number: This action generates a Notify number by accepting the required type as input—**Voice**, **SMS**, or **both**.

</td></tr><tr><td>

Now Assist

</td><td>

-   **[Clarifying questions for unclear requests](https://www.servicenow.com/docs/access?context=now-assist-panel-overview&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Get precise, relevant answers from Now Assist panel premium chat even when your request is unclear, as the assistant asks you a targeted clarifying question before responding instead of returning an overwhelming list of results. When the assistant is confident it understands your request, it responds immediately without interrupting the conversation.

-   **[Upload documents](https://www.servicenow.com/docs/access?context=now-assist-panel-overview&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Upload documents directly into a Now Assist panel conversation during topic, skill, catalog, or agent execution, and let the assistant extract information from them to automatically fill in required fields, answer questions, and keep the conversation moving. Uploaded document context is retained for the duration of the session and cleared when the session ends to protect your data.

-   **[Response feedback](https://www.servicenow.com/docs/access?context=now-assist-panel-overview&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Provide more detailed feedback on Now Assist panel responses by selecting thumbs up or thumbs down, then choosing from configurable checkbox options or adding your own comments to explain exactly what was helpful or what fell short. Your feedback is captured and made available through analytics dashboards, helping admins continuously improve the quality of responses you receive.

-   **[Premium chat](https://www.servicenow.com/docs/access?context=now-assist-panel-overview&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Start a Now Assist panel premium chat from any page in the Employee Hub with a single click, without interrupting existing workflows. You can upload files, toggle web search on or off, and receive a personalized greeting with promoted topics when opening a new conversation.

-   **[Synthesized results in chat experience](https://www.servicenow.com/docs/access?context=now-assist-panel-overview&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Get concise, grounded answers to your natural language questions in Now Assist panel premium chat, with inline citations linking to the knowledge articles, actions, and catalogs used to generate the response. You can ask follow-up questions within the same context, explore sources in the side panel, and see clear messaging if results are limited or unavailable.

-   **[Search results side panel](https://www.servicenow.com/docs/access?context=now-assist-panel-overview&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

View search citations and related results in a collapsible side panel that appears alongside your Now Assist panel premium chat responses, so you can explore sources without leaving the conversation. You can select any internal source to open it in the background, browse external results in a new tab, and close the panel at any time to return to the full chat view.

-   **[Primitives and widgets](https://www.servicenow.com/docs/access?context=now-assist-panel-overview&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

View rich, responsive content inline in your Now Assist panel premium chat conversation, including people profiles, org charts, record cards, and record summaries that match the look and feel of your portal. You can also access org charts and people information directly through natural language — for example, by typing "show me the org chart for John Smith" — without leaving the conversation.

-   **[Voice Input](https://www.servicenow.com/docs/access?context=now-assist-panel-overview&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Use your voice to send prompts in Now Assist panel premium chats by selecting the microphone button in the input bar, which transcribes your speech to text so you can interact with the assistant hands-free. You can enable or disable voice input through your personal preferences, and your admin can also turn it on or off at the assistant level through Assistant Designer.

-   **[Search enhancements](https://www.servicenow.com/docs/access?context=now-assist-panel-overview&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Get cleaner, more organized search results in Now Assist panel premium chat, with single records displayed as cards and multiple records displayed as tables. You can switch between multiple interactive views in a conversation using a dropdown and use a back button to return to previously viewed content.

-   **[Transition from chat to full search results](https://www.servicenow.com/docs/access?context=now-assist-panel-overview&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Access the full search results page directly from your Now Assist panel premium chat response by selecting the "Full search experience" link in the sources and more panel. The search results page opens with your original search term already populated, so you can explore the complete set of results without having to retype your query.

-   **[Follow-up questions from search results](https://www.servicenow.com/docs/access?context=now-assist-panel-overview&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Ask follow-up questions in Now Assist panel premium chat directly from your workspace search results by selecting the "Ask a follow-up" button, which opens a new conversation with the relevant search context already loaded. You can continue exploring a topic conversationally without having to re-enter your query or switch between search and chat.

-   **[Record-specific context](https://www.servicenow.com/docs/access?context=now-assist-panel-overview&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Get more relevant responses from Now Assist panel premium chat when you're working on a record, as conversations started from a record page are automatically aware of that record's context. You no longer need to manually describe what you're working on — the assistant understands it from the start.

-   **[Upgrade Now Assist panel](https://www.servicenow.com/docs/access?context=now-assist-panel-overview&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Upgrade your Now Assist panel experience to premium chat without losing your active conversations, as any conversations in progress remain accessible until you refresh the page. When you open premium chat for the first time after the upgrade, a summary of what's new helps you quickly get familiar with the latest capabilities.


-   **[Manage version](https://www.servicenow.com/docs/access?context=manage-version&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Review the summary, alerts, and notifications regarding changes in model provider version states as they are deprecated or retired.

-   **[Now Assist panel](https://www.servicenow.com/docs/access?context=now-assist-panel-overview&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Send information from Now Assist panel conversations directly to relevant fields on incident pages using action buttons. You don't have to manually copy and paste content between Now Assist panel conversations and the incident form.

-   **[Now Assist panel](https://www.servicenow.com/docs/access?context=now-assist-panel-overview&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Automatically see the most recent Now Assist panel conversation for an incident when you switch between incident tabs. Now Assist panel remembers which conversation belongs to which incident and displays it when you return to that incident.

-   **[Now Assist panel](https://www.servicenow.com/docs/access?context=now-assist-panel-overview&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Configure which record types will support Now Assist panel context switching. This enables teams to customize the Now Assist panel experience based on a business unit’s workflow and use cases.

-   **[Now Assist panel](https://www.servicenow.com/docs/access?context=now-assist-panel-overview&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

View your Now Assist panel chat history grouped by incident record. Agent conversations related to a specific incident are grouped together rather than organized chronologically, making them easier to find.

-   **[Now Assist panel](https://www.servicenow.com/docs/access?context=now-assist-panel-overview&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

View the correct conversation history when you navigate between different incident records.

-   **[Now Assist panel](https://www.servicenow.com/docs/access?context=now-assist-panel-overview&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Send information directly from a Now Assist panel conversation to an agent chat conversation. This makes it easier to collaborate and share helpful information during incident resolution.

-   **[Now Assist panel](https://www.servicenow.com/docs/access?context=now-assist-panel-overview&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Build custom Now Assist panel integrations that are tailored to specific business needs by passing custom context data in any format when initiating Now Assist panel conversations or executing skills.

-   **[Enhanced content detection with third-party guardrails](https://www.servicenow.com/docs/access?context=configure-guardrail-model&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Now Assist Guardian supports third-party service provider guardrails, such as Microsoft Azure, Amazon Bedrock, and Google Model Armor so that any inappropriate content is logged and blocked during content generation. This gives you the flexibility to choose the detection provider that best aligns with your existing cloud infrastructure.


-   **[Requester Approval Checklist skill](https://www.servicenow.com/docs/access?context=service-portal-approval-checklist-skill&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

The Requester Approval Checklist skill in the ServiceNow AI Platform® generates a structured checklist by mapping real-time request data against your organization’s knowledge articles.

**Note:** The skill is on by default.


-   **[New system properties for the Now Assist Readiness Evaluation app](https://www.servicenow.com/docs/access?context=nare-sys-props&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**
    -   Reduce performance issues when a large volume of data is assessed with the **sn\_assess.assessment\_limit** system property.
    -   Customize the estimated remediation effort for select efforts with the **sn\_assess.effort\_visibility** system property. Setting this system property to `true` turns on the **Remediation properties** tab in the Now Assist Readiness Evaluation dashboard.
    -   Decide the maximum number of records to process for the ITSM assessment with the **sn\_assess.task\_limit** system property.

-   **[Manage version](https://www.servicenow.com/docs/access?context=manage-version&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Manage the versions of model providers across various skill groups and instance levels in Now Assist. You can modify and update versions for both base system and custom skills.

-   **[Now Assist skills](https://www.servicenow.com/docs/access?context=now-assist-skills&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Unlock the benefits of the Now Assist Fulfiller subscription to be able to explore and activate all the skills available in the system from Now Assist Admin.

-   **[Role masking in Now Assist AI agents](https://www.servicenow.com/docs/access?context=aia-role-masking&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Define roles within **role restrictions** for individual skills in Now Assist Admin to enforce resource access restrictions when a skill is invoked. This feature promotes precise control over the resources that can be accessed, like data and APIs.

-   **[Overview tab in Now Assist Admin](https://www.servicenow.com/docs/access?context=configuring-now-assist&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Share your experience in the Now Assist journey by providing feedback when prompted.

-   **[Voice input setting automatically activated](https://www.servicenow.com/docs/access?context=activate-now-assist-panel&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Activate the Now Assist panel to automatically turn on the voice input setting, which is now located on the Assistants page.

-   **[Now Assist panel](https://www.servicenow.com/docs/access?context=now-assist-panel-overview&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Request additional information or clarification by asking a follow-up question in the Now Assist panel.

-   **[Synthesized Now Assist responses](https://www.servicenow.com/docs/access?context=gchat-conv-integration&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)**

View synthesized Now Assist responses from within Google chat to have a richer conversational experience.

-   **[Now Assist support in article optimization](https://www.servicenow.com/docs/access?context=knowledge-center-article-optimization&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)**

Improve the quality and health of your knowledge articles by using Now Assist based Article Optimization in the Knowledge Center. Scan knowledge articles and get instant, actionable feedback.

-   **[Use Now Assist to identify knowledge gaps](https://www.servicenow.com/docs/access?context=understanding-knowledge-gaps&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)**

Identify and fill potential knowledge gaps proactively, including missing knowledge articles and recurring issues that lack or have an incomplete knowledge article.

-   **[Agentic workflows from within Google chat](https://www.servicenow.com/docs/access?context=gchat-conv-integration&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)**

Initiate and view agentic workflows from within Google chat.

-   **[Monitor sensitive topic invocations](https://www.servicenow.com/docs/access?context=reference-for-generative-ai-controller&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Access the Gen AI Metrics \[sys\_generative\_ai\_metric\] table to review the logged invocations of sensitive topics and gain insights into how these topics are being triggered and monitored.

-   **[Long term stable models](https://www.servicenow.com/docs/access?context=long-term-stable-models&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Long term stable \(LTS\) models are part of Now LLM Service and provide longer model stability windows for regulated industries. These models can integrate with tools to provide governance, monitoring, and compliance controls.

-   **[Create multiple Now Assist context menu skill configurations](https://www.servicenow.com/docs/access?context=create-multple-nacm-skill-configuration&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

You can now have multiple Now Assist context menu configurations on the same record form and field. You just have to create the required configuration and add to the form or field.

-   **[Generate KB article with Now Assist context menu](https://www.servicenow.com/docs/access?context=generate-kb-article-with&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Using the Now Assist Context Menu open prompt inline and pop-over variant you can quickly produce high-quality, accurate, and lucid knowledge articles, saving time and improving support in Knowledge Management.


-   **[Now Assist Readiness Evaluation](https://www.servicenow.com/docs/access?context=now-assist-readiness-evaluation-landing-page&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

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


-   **[Improve Docs content in Strategic Portfolio Management with Now Assist context menu](https://www.servicenow.com/docs/access?context=answer-queries-with-now-assist-context-menu&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US) for SPM**

Implement the open prompt capability to enhance your ability to add additional context and generate accurate content with Now Assist context menu.

This feature enables interactive conversations with both supported ServiceNow® generative AI skills and custom-built skills.

-   **[Configure skills with custom prompts for knowledge article templates](https://www.servicenow.com/docs/access?context=Now-assist-configure-custom-prompts-for-templates&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)**

As an admin, clone the KB generation skill and update prompts for AI model providers. This feature helps the agent use custom templates and custom prompts to generate knowledge articles with Now Assist from single and multiple knowledge bases.

-   **[Manage AI models](https://www.servicenow.com/docs/access?context=manage-large-language-models&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Choose and update your preferred LLM provider at the instance, skill, or skill group level for Now Assist base system skills.

Deactivate skills that aren't compatible with any of the LLM providers and access the audit history to view updates by the AI steward in AI Control Tower.

-   **[Configure multilingual service for Now Assist applications](https://www.servicenow.com/docs/access?context=enable-dynamic-translation-for-now-assist-applications&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Manage the default and supported languages by the different LLM providers under Multilingual service for translation.

-   **[Configure email reply recommendation in the Now Assist Admin console](https://www.servicenow.com/docs/access?context=configure-email-recommendation&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Access citations to the articles referenced from the Knowledge Base. Explore references and insert the generated reply to your email.

-   **[Now Assist panel](https://www.servicenow.com/docs/access?context=now-assist-panel-overview&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Use the enhanced Now Assist panel for an intuitive and personalized experience. The updated Now Assist panel can be resized and moved anywhere on the ServiceNow AI Platform.

-   **[Now Assist Guardian supports third-party LLMs](https://www.servicenow.com/docs/access?context=now-assist-guardian&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Extend guardrail support to third-party LLMs, such as Amazon Bedrock, Google Cloud Vertex AI studio, Google AI studio, and Azure OpenAI, to verify that any inappropriate content is logged and blocked during content generation.

-   **[Increase the maximum response token limit for custom skills](https://www.servicenow.com/docs/access?context=configure-skill-prompt&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Increase the maximum response token limit for a Now Assist custom skill beyond the default value of 1000. This ability supports dynamic pricing based on output tokens and calculates the price for each skill executed per assist.


</td></tr><tr><td>

Now Assist AI agents

</td><td>

-   **[Create an AI agent](https://www.servicenow.com/docs/access?context=configure-next-best-action-agent&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

The AI-native experience for an AI agent is available exclusively with the installation of the Off Glide Conversation Server plugin \(com.glide.cs.offglide\).

**Note:** To use the AI agent in AI-native mode, make sure to test it so it works as expected.

-   **[Test an agentic solution in AI Native mode](https://www.servicenow.com/docs/access?context=test-ai-agent&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Use the AI Native playground experience to test your agentic solutions.

**Note:** The AI-native playground experience is exclusively accessible when the Off Glide Conversation Server plugin \(com.glide.cs.offglide\) is installed. If the plugin is not installed, you will continue to access the standard testing playground.

-   **[Add tools and information to an AI agent](https://www.servicenow.com/docs/access?context=add-tool-aia&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Add widgets for tool outputs to provide an improved experience in AI-native mode.

**Note:** The display output widget options are exclusively accessible when the Off Glide Conversation Server plugin \(com.glide.cs.offglide\) is installed. If the plugin is not installed, you will continue to access the standard add tool form.


-   **[Evaluate voice AI agents for overall task completion and tool choice accuracy](https://www.servicenow.com/docs/access?context=execute-aia-eval&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Automated evaluations support voice AI agents. Get a better picture of overall performance by evaluating previous executions against standardized metrics.


-   **[ServiceNow AI agents as secondary agents](https://www.servicenow.com/docs/access?context=secondary-agent&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Enhance user experience for Secondary Agents by displaying the Agent card URL to admins for easy access and management so the admin can view, copy, and consume the URL easily.

Additionally, when adding an MCP tool, the name and description of the tool are populated automatically as per the details fetched from the server and the user can update the details.


-   **[Configure role masking for AI agents and agentic workflows](https://www.servicenow.com/docs/access?context=aia-role-masking&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Role masking restricts access to specific roles based on configuration to verify that agentic workflows, AI agents, and tools run within the boundaries of the roles configured to meet their business needs while reducing the risk of unauthorized access to the agents and the agentic data.

-   **[Add AI agent learning](https://www.servicenow.com/docs/access?context=agent-learning&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Enhance AI agent learning through episodic memory, enabling AI agents to improve by learning from past successful interactions.

-   **[Select channels and access for an agentic workflow](https://www.servicenow.com/docs/access?context=channels-access-aw&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Create and update UI actions for workflow executions and display handling. You can specify conditions for the display of the UI actions.

-   **[Add a defined desktop action tool to an AI agent for desktop and web-based task](https://www.servicenow.com/docs/access?context=add-desktop-action-ai-agent&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Add Desktop action as a tool to an AI agent to perform desktop automation for repetitive tasks.

-   **[Configure Now Assist AI agents](https://www.servicenow.com/docs/access?context=configuring-ai-agents&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Support multilingual conversations for AI agents across languages.

-   **[Manually test the execution of an AI agent](https://www.servicenow.com/docs/access?context=test-ai-agent&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US) and [Manually test the execution of an agentic workflow](https://www.servicenow.com/docs/access?context=test-aia-use-case&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

The testing page on AI Agent Studio has two testing options:

    -   Manual test
    -   Automated evaluation
Observe the different versions of an AI agent behavior in manual tests and in automated evaluations using the **Manual tests** and **Automated tests** tabs.

-   **[Test user access to an AI agent](https://www.servicenow.com/docs/access?context=test-aia-access&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US) and [Test user access to an agentic workflow](https://www.servicenow.com/docs/access?context=test-aw-access&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Test how an AI agent or agentic workflow completes a task and if it enables users permission to access it.

-   **[Model Context Protocol Client](https://www.servicenow.com/docs/access?context=mcp-client&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**
    -   Authorization upgrades to support segregation of Resource Server and Authentication Server through Protected Resource Metadata \(PRM\).
    -   Use the **mcp\_guardian\_check** property to enable guardian checks for MCP Client when there’s an MCP tool call.
    -   Supervise the pagination with mouse device support to show large number of services from an MCP server through the **sn\_mcp\_client.cursor.max\_iterations** system property.
    -   Add a title field for human-friendly display names that can be used as a programmatic identifier.
-   **[Use in-product experiences for agentic workflows on forms](https://www.servicenow.com/docs/access?context=in-product-agentic-ai&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

In the Core UI and workspaces, you can use UI and declarative actions to run agentic workflows. You can also see the presence, progress, and output of agentic workflows performed on a record. The execution details for each agentic workflow include who is supervising the workflow, estimated and total time taken, processing messages, and step history.

-   **[Review and approve requests and tickets with the Approval Assistance AI agent](https://www.servicenow.com/docs/access?context=platform-approval-aia&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

You can use the new approval assistance AI agent to view all pending approval requests and access detailed information about them. You can then approve requests and tickets and make updates to them from Now Assist in Virtual Agent.

-   **[View the Approval Info Record widget](https://www.servicenow.com/docs/access?context=approval-info-record-widget&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US)**

The Service Portal Approval Info Record widget shows details about the approval request and a full record for an approval including the activity stream.

-   **[Configure email notification alerts for AI agent and agentic workflow executions](https://www.servicenow.com/docs/access?context=config-aia-notifications&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Configure alert email notifications for unexpected or undesired behavior from AI agents and agentic workflows. You can configure the thresholds for triggering the alerts on the Agent Properties table, and you can add or update the recipients of the email notifications from the Notifications table.

-   **[Create an external AI agent](https://www.servicenow.com/docs/access?context=create-external-aia&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Create new external AI agents that connect to third-party agentic AI systems. Use Agent2Agent protocol or integrate agents manually to configure them in AI Agent Studio to use in the ServiceNow agentic AI system.

-   **[Add a Knowledge Graph to an AI agent](https://www.servicenow.com/docs/access?context=add-knowledge-graph&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Use Enterprise Graph \(Small\) as a resource to create a Knowledge Graph tool for an AI agent in the AI Agent Studio.


-   **[Add an MCP server tool to an AI agent](https://www.servicenow.com/docs/access?context=add-mcp-server-tool&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

The Model Context Protocol Client enables guardian checks for offensive content when Notion is selected as the MCP server.

-   **[Configure Model Context Protocol Client](https://www.servicenow.com/docs/access?context=configuring-mcp-client&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

The Model Context Protocol Client application supports the latest MCP version.

-   **[Add a Knowledge Graph to an AI agent](https://www.servicenow.com/docs/access?context=add-knowledge-graph&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Use Global Graph as a Knowledge Graph resource when creating a Knowledge Graph tool for an AI agent in the AI Agent Studio.


-   **[Model Context Protocol Client](https://www.servicenow.com/docs/access?context=mcp-client&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Enable users of the ServiceNow® AI Agent Studio to access tools that are hosted externally and published using an MCP server via the Model Context Protocol Client application.

Authenticate users with the MCP server to add the MCP tool to an AI agent.

-   **[Configure ACLs for AI agents and agentic workflows](https://www.servicenow.com/docs/access?context=aia-security-implementation&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Configure the access control lists for who can discover and trigger AI agents and agentic workflows in their guided setups in AI Agent Studio. You can determine whether an AI agent or agentic workflow behaves as a dynamic user or as an AI user. You can also specify if an AI agent or agentic workflow can be available to all authenticated users or publicly available.


-   **[Review agentic activity in AI Agent Studio](https://www.servicenow.com/docs/access?context=ai-agent-studio&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

View and troubleshoot the agentic workflow and AI agent executions on AI Agent Studio via the **Activity** page.

-   **[Configure Now Assist AI agents](https://www.servicenow.com/docs/access?context=configuring-ai-agents&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US) - Dynamic Orchestrator**

Maps the appropriate agents for an agentic workflow with Dynamic Orchestrator for better performance and accuracy of the agentic workflow execution.

-   **[View analytics for customer satisfaction with AI interactions](https://www.servicenow.com/docs/access?context=ai-agent-dashboard&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Multiple new metrics have been added to the AI Agent Analytics dashboard, accessible from the AI Agent Studio to provide insight into average customer satisfaction and customer satisfaction with the best and worst performing agentic workflows and agents.

-   **[New third-party AI model provider options available for all Now Assist applications](https://www.servicenow.com/docs/access?context=exploring-large-language-models&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Google Gemini and AWS Claude are available for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.

-   **[Add tools and information to an AI agent](https://www.servicenow.com/docs/access?context=add-tool-aia&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

The output transformation strategy for an AI agent output contains a new option called **Custom**. Using the custom output transformation strategy, the tool output gets transformed according to the LLM instructions.

-   **[Configure Now Assist AI agents](https://www.servicenow.com/docs/access?context=configuring-ai-agents&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US) - AI Agent Background Channel**

Invoke the agentic conversations from Workspace or Core UI via the AI Agent Background channel that is associated with the AI Agent Background Provider to execute the AI agents and agentic workflows.

-   **[Configure Now Assist AI agents](https://www.servicenow.com/docs/access?context=configuring-ai-agents&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US) - Interactive and non interactive AI agents**

Run AI agents and agentic workflows execution in one of the following ways:

    -   **Interactive Mode**: AI agents reach out to the user for information during fallback.
    -   **Non interactive Mode**: AI agents don’t reach out to the user during fallback but send the execution output to the user.

</td></tr><tr><td>

Now Assist Skill Kit

</td><td>

-   **[Labelling](https://www.servicenow.com/docs/access?context=nadk-labelling&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)Use labeling workflows to annotate UI templates**

Use the labeling framework to create and manage ground truth data. Published data collections can now be turned into labeling projects. Each record becomes a task assigned to labelers who annotate using pre-configured UI templates

-   **[s](https://www.servicenow.com/docs/access?context=configure-skill-prompt&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)Structured output support for AI responses**

Enables consistent parsing in agentic workflows and reduces ambiguity in downstream automation.

-   **[Use multi-table data generator](https://www.servicenow.com/docs/access?context=use-multi-table-data-generator&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)New multi-table synthetic data generation option**

You can generate related records across multiple tables in a single operation. You no longer need to generate each table separately and manually link records. Define your table relationships, set the cardinality and Now Assist Data Kit generates coherent, referentially linked records across all tables in one pass, with foreign key integrity maintained automatically. 

-   **[Create a model](https://www.servicenow.com/docs/access?context=create-model&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)AI Control Tower integration with custom LLMs.**

Improve oversight and compliance for AI deployments with formal approval flows for custom models.

-   **[Now Assist Skill Kit roles](https://www.servicenow.com/docs/access?context=na-skill-kit-roles&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)Update to the abilities of the admin role**

The sn\_skill\_builder.admin role is now broken into smaller, task-specific roles, including a custom LLM-specific admin role.


-   **[Create a model](https://www.servicenow.com/docs/access?context=create-model&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

When you bring your own model you can keep data in your own environment and fine-tune it to meet your specific needs.


-   **[New third-party AI model provider options available for all Now Assist applications](https://www.servicenow.com/docs/access?context=exploring-large-language-models&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Google Gemini and AWS Claude are available for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.

-   **[New skill deployment option](https://www.servicenow.com/docs/access?context=configure-skill-settings&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Deploy skills using UI Builder.

-   **[Choose a language for data generation](https://www.servicenow.com/docs/access?context=na-data-kit-generate-data&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

When you create synthetic data, you can select what language you want to receive the data in.

-   **AI-assisted ground truth**

Use AI to assist creating ground truth for your data.

-   **[Import data with a CSV file](https://www.servicenow.com/docs/access?context=add-dataset&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Import data from a CSV file to create a dataset.

-   **[Create a custom data generator](https://www.servicenow.com/docs/access?context=create-custom-data-generator&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Create and use a custom data generator to create synthetic data.


</td></tr><tr><td>

Now Assist for App Engine

</td><td>

-   **[Custom app record summarization skill](https://www.servicenow.com/docs/access?context=custom-app-record-summarization-na-for-app-engine&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

Generate summaries for records in custom applications and tables with the custom app record summarization skill.

-   **[Configure the custom app record summarization skill](https://www.servicenow.com/docs/access?context=configure-custom-app-record-summarization-na-for-app-engine&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

Configure the custom app record summarization skill so that it generates summaries for the tables and records that you specify. You can add context about the table or tables and describe the purpose of the table, so that Now Assist can use that information when generating summaries.

-   **[Summarize a record in-product using Now Assist for App Engine](https://www.servicenow.com/docs/access?context=summarize-record-in-product-na-for-app-engine&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

Select the **Summarize** button on a record in-product to generate a summary. You can also summarize a record through chat in the Now Assist panel. See [Summarize a record through chat using Now Assist for App Engine](https://www.servicenow.com/docs/access?context=summarize-record-through-chat-na-for-app-engine&version=zurich&pubname=zurich-application-development&ft:locale=en-US) for more information.


-   **[New third-party AI model provider options available for Now Assist](https://www.servicenow.com/docs/access?context=manage-large-language-models&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Google Gemini 2.0 Flash, Google Gemini 2.5 Pro, and AWS Claude 3.7 Sonnet are available for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI GPT-4.1 and GPT-4.1 mini.


</td></tr><tr><td>

Now Assist for Collaborative Work Management \(CWM\)

</td><td>

-   **[Generate acceptance criteria for stories in CWM](https://www.servicenow.com/docs/access?context=generate-acceptance-criteria-for-stories-in-cwm&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)**

Generate clear, consistent acceptance criteria for user stories with the acceptance criteria generation skill. By using story details as context and predefined templates, the skill helps you generate acceptance criteria in a format that aligns with your organizational requirements.

-   **[Generate and improve content using open-text prompts](https://www.servicenow.com/docs/access?context=generate-summarize-and-refine-content-of-docs-with-now-assist&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)**

Help improve your content and productivity with the ability to enter custom prompts directly in the Docs, alongside the Summarize, Elaborate, and Shorten options.

Generate content with Now Assist for CWM directly in your Docs. In addition, summarize existing sections, elaborate where needed, and refine drafts.

-   **[New third-party AI model provider options available for all Now Assist applications](https://www.servicenow.com/docs/access?context=exploring-large-language-models&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Google Gemini and AWS Claude are available for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.


</td></tr><tr><td>

Now Assist for Configure, Price, Quote \(CPQ\)

</td><td>

[Zurich Patch 7](../quality/zurich-patch-7.md)

-   **[Summarize a quote using quote summarization](https://www.servicenow.com/docs/access?context=summarize-quote&version=zurich&pubname=zurich-order-management&ft:locale=en-US)**

Generate a summary of a quote to:

    -   Summarize key quote components during early customer discussions or pre‑discovery.
    -   Provide an updated view of the quote after revisions, without requiring review of multiple records.
    -   Provide a single, consolidated snapshot of all actions, tasks, and notes derived from a quote in one place.
    -   Highlight custom pricing, discounts, and negotiated changes made during the quoting process.
    -   Review the quote prior to sending it to the customer to confirm accuracy and completeness.
    -   Support internal handoffs by summarizing the quoted offer for internal teams.

</td></tr><tr><td>

Now Assist for Creator

</td><td>

-   **[Generate themes using the new theme generation workflow in Theme Builder](https://www.servicenow.com/docs/access?context=create-theme-now-assist&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US)**

Leverage the new theme generation workflow in Theme Builder to generate themes based on your brand image. After generating a theme, navigate to Theme Builder to publish and apply additional styling.

-   **[Edit already published catalog items using Now Assist](https://www.servicenow.com/docs/access?context=edit-already-published-catalog-items-using-now-assist&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)**

Edit and refine published catalog items conversationally using Now Assist in Catalog Builder.

-   **[Generate UI policies in Catalog Builder](https://www.servicenow.com/docs/access?context=now-assist-ui-policy-functions&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)**

Use Now Assist to create new UI policies, update existing ones, and deactivate them, all through simple, conversational prompts. Each UI policy can include multiple actions, and Now Assist can create that for you.

-   **[Assign catalog item location with Now Assist](https://www.servicenow.com/docs/access?context=setting-location-catalog-category-and-topic-with-now-assist&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)**

When creating or editing a catalog item, you can use plain language to assign values for catalog, category, or topic. If the value you provide matches an existing entry, Now Assist automatically applies it to the item, helping to streamline the process and reduce manual data entry.


-   **[Configure AI model providers for Now Assist for Code skills](https://www.servicenow.com/docs/access?context=configure-model-providers-for-now-assist-skills&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)**

Choose a model provider for Now Assist for Code skills in the script editor. You can choose from the models that are enabled in the AI Control Tower.

-   **[Planning tool available with the Build Agent](https://www.servicenow.com/docs/access?context=exploring-build-agent&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

Build a detailed, step-by-step plan for your application development with the Build Agent planning tool. You can refine the plan iteratively by prompting for changes and providing feedback until you reach a final version.

-   **[Build Agent supports Azure OpenAI and Google Gemini](https://www.servicenow.com/docs/access?context=install-build-agent&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

Use Build Agent with Azure OpenAI and Google Gemini in addition to Anthropic Claude on AWS.

-   **[Use images as prompts in Build Agent](https://www.servicenow.com/docs/access?context=exploring-build-agent&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

Attach images, such as architectural diagrams or UI wireframes, to provide context for prompts in the Build Agent.

-   **[Generate catalog items conversationally with Now Assist in Catalog Builder](https://www.servicenow.com/docs/access?context=create-catalog-item-using-now-assist&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)**

Create catalog items and record producers efficiently using the conversational interface within Catalog Builder. Communicate your requirements and specifications for your desired catalog items through guided conversation. Now Assist for catalog generation helps to simplify and streamline the catalog item creation process.

-   **[Preview catalog items during the creation process](https://www.servicenow.com/docs/access?context=create-catalog-item-using-now-assist&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)**

Preview catalog items during the creation process. Quick previews enable you to verify that catalog items appear and function as intended before publication.

-   **[Getting help with the Now Assist panel in UI Builder](https://www.servicenow.com/docs/access?context=uib-now-assist-panel&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

Create pages using natural language text prompts with Now Assist in UI Builder. Quickly add layouts, components, and content to your pages without manually configuring each element. You can also quickly analyze page structure and data flow by asking questions using natural language.

-   **[Key features of UI Builder agent](https://www.servicenow.com/docs/access?context=key-features-of-ui-builder-agent&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

Ask your questions about using UI Builder to the UI Builder agent. The UI Builder agent provides an overview of page configuration, such as the structure and interconnections of page elements. You can also use the UI Builder agent to apply different layouts, configure components, and update styling.

-   **[ATF troubleshooting agent](https://www.servicenow.com/docs/access?context=atf-troubleshooting-agent-landing-page&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

Accelerate troubleshooting and resolve test failures quickly by using ATF troubleshooting agent on covered metadata.


-   **[Application development with Figma MCP server](https://www.servicenow.com/docs/access?context=accelerate-design-to-development-with-figma-mcp-server&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

You can now connect the Build Agent to the Figma MCP server. The Figma MCP server enables the Build Agent to access the structured data within Figma files. This connection accelerates the transition from application design to development, helping to make the developer workflow more efficient.


-   **[New Build Agent \(Trial\) available](https://www.servicenow.com/docs/access?context=exploring-build-agent&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

A trial version of the Build Agent is now available with Build Agent \(Trial\). With Build Agent \(Trial\), you can explore limited interactions with the Build Agent for free.


-   **[New third-party AI model provider options available for Now Assist](https://www.servicenow.com/docs/access?context=manage-large-language-models&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Google Gemini 2.0 Flash, Google Gemini 2.5 Pro, and AWS Claude 3.7 Sonnet are available for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI GPT-4.1 and GPT-4.1 mini.

-   **[Build Agent, an autonomous AI agent for ServiceNow application development](https://www.servicenow.com/docs/access?context=exploring-build-agent&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

The Build Agent, located in a chat panel within the ServiceNow IDE, functions as an autonomous AI agent capable of independently generating a complete ServiceNow application. It can handle various code-related tasks, such as rewriting tables, explaining code, validating and improving existing applications, fixing application errors, and more.


</td></tr><tr><td>

Now Assist for Customer Service Management \(CSM\)

</td><td>

-   **[AI workflow tab added in Core UI](https://www.servicenow.com/docs/access?context=ai-workflow-pattern-in-customer-service-management&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

Availability of AI Workflow tab within case view of case table records and email interaction view of interaction records in Core UI, showing agentic workflows and actionable AI-driven insights directly in the record UI.

-   **[Filter controls in Now Assist Guardian](https://www.servicenow.com/docs/access?context=now-assist-guardian-csm-filters&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

Availability of filter controls for CSM in the Now Assist Guardian interface, allowing users to toggle the base system filters on and off. Filtered results display in a user-friendly format for quick case review and action.


-   **[Metrics to measure genAI skills](https://www.servicenow.com/docs/access?context=skills-performnace-dashboard&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

Monitor how users engage with genAI and agentic skills in Now Assist for CSM to provide actionable dashboards and reports for workflow optimization.

-   **[Navigation to customer 360 insights summary card in cases](https://www.servicenow.com/docs/access?context=now-assist-csm-summarize-case&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

Access all relevant case information by navigating to the customer 360° insights page from the summary card.

-   **[AI voice agent for CSM](https://www.servicenow.com/docs/access?context=voice-ai-agent&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

Access a case status and create cases through voice interactions with a unified AI voice agent for case management.

-   **[In-product agentic indicators](https://www.servicenow.com/docs/access?context=ai-workflow-pattern-in-customer-service-management&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

Identify when agentic AI is active in a record in the **AI Workflows** tab, which includes a presence icon and record indicator.


-   **[Complaint Case AI agents collection](https://www.servicenow.com/docs/access?context=accelerate-complaint-case-handling&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

The Complaint Case AI agent collection automates complaint handling by gathering missing details, analyzing sentiment, categorizing issues, and suggesting resolutions. It streamlines intake, triage, and communication, which helps reduce case closure time.


-   **[Enabled the is\_template property](https://www.servicenow.com/docs/access?context=clone-the-now-assist-for-csm-skills&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

Enabled the is\_template property for all Now Assist skills to clone consistently. Clone any base system genAI skill and customize it in the Now Assist Skill Kit to set up quickly and simplify skill modification. Applies to all Now Assist for CSM skills.

-   **[Access the Sentiment analysis dashboard in Core UI](https://www.servicenow.com/docs/access?context=use-sentiment-analysis-dashboard&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

Locate and access sentiment analysis data without searching through multiple menus with a defined navigation path in the Sentiment analysis dashboard in the Core UI interface.

-   **[Sentiment trends analysis dashboard](https://www.servicenow.com/docs/access?context=use-sentiment-analysis-dashboard&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

Get a comprehensive view of customer sentiment across case. The dashboard uses LLM-powered insights to explain sentiment changes and lets you drill down to find root causes and real time insights—helping managers take targeted actions.

-   **[Trending topics dashboard](https://www.servicenow.com/docs/access?context=view-trending-topics-dashboard&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

Get a comprehensive view of trending topics across cases along with insights and visualizations to facilitate deeper analysis. This feature helps support teams track trend progression, regional impact, and analyze specific trends using customizable filters.

-   **[Provide customer 360 insights agentic workflow](https://www.servicenow.com/docs/access?context=customer-service-management-ai-agent-collection-customer-360&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

Use the provide customer 360 insights agentic workflow to provide synthesized and relevant customer insights to live agents via conversations. This agentic workflow is designed to support human agents by responding to natural language queries regarding cases, customer history, products, and interactions. This feature expedites access to vital information and case resolution, identifies patterns, and leverages past similar cases for guidance as well as triggers actions from the Now Assist panel.

-   **[Activity response generation skill](https://www.servicenow.com/docs/access?context=generate-a-recommendation-to-respond-to-an-activity&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

Use the activity response generation skill to automatically generate recommendations for resolution notes, work notes, and comments. This feature helps agents add meaningful updates to case records, improving efficiency and interactions.

-   **[Now Assist context menu configuration for extended tables within resolution notes](https://www.servicenow.com/docs/access?context=customize-now-assist-context-menu-for-skills&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

Configure output fields for resolution notes through the Now Assist context menu configuration page so skills apply to extended tables without any additional setup.


-   **[Use the triage cases agentic workflow security directives](https://www.servicenow.com/docs/access?context=case-resolving-use-case&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

Implement security on AI agents and agentic workflows through ACLs and user identities.

-   **[Now Assist for CSM genAI security directives](https://www.servicenow.com/docs/access?context=configure-chat-summarization-in-now-assist_0&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

Implement security in Now Assist for CSM skills through ACLs and user identities.


-   **[New third-party AI model provider options available for all Now Assist applications](https://www.servicenow.com/docs/access?context=exploring-large-language-models&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Google Gemini and AWS Claude are available for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.


</td></tr><tr><td>

Now Assist for Enterprise Architecture \(EA\)

</td><td>

-   **[Compare Enterprise Modeling and Visualization diagrams](https://www.servicenow.com/docs/access?context=compare-modeling-diagrams&version=zurich&pubname=zurich-application-portfolio-management&ft:locale=en-US)**

Learn the details of the changes in the Enterprise Modeling and Visualization diagrams by comparing a diagram with its previous version. You can compare business application hierarchy, business capability map, and business process map diagrams.

-   **[Elaborate or shorten content in form fields](https://www.servicenow.com/docs/access?context=elaborate-or-shorten-content-form-fields&version=zurich&pubname=zurich-application-portfolio-management&ft:locale=en-US)**

Elaborate or shorten text in the **Description** field of the following records using the Refine text Now Assist skill:

    -   Business application
    -   Business capability
    -   Business process
    -   Value stream stages
    -   Information object
Also, generate, elaborate, or shorten text in the **Reasoning** field in the **Planned Disposition** section of the business application record.

-   **[Business Application Insights skill configuration changes](https://www.servicenow.com/docs/access?context=configure-now-assist-ea&version=zurich&pubname=zurich-application-portfolio-management&ft:locale=en-US)**

For the Business application insights Now Assist skill, you can view the business application source fields based on which the business application insights are generated. Also, you can determine the availability of the skill by defining a specific criteria in the **Define access** tab of the Business application insights skill.

-   **[Role restrictions for Now Assist for EA skills](https://www.servicenow.com/docs/access?context=configure-now-assist-ea&version=zurich&pubname=zurich-application-portfolio-management&ft:locale=en-US)**

Role restriction is added to the default roles associated with the following skills:

    -   Diagram change analysis
    -   ADR Doc Summarization and Actions
    -   Business application insights
    -   Refine text
-   **[Business Application Insights skill](https://www.servicenow.com/docs/access?context=generate-insights-into-ba&version=zurich&pubname=zurich-application-portfolio-management&ft:locale=en-US)**

Learn the details of business applications and gather concise and actionable insights on business applications from the summary that is generated by Now Assist for Enterprise Architecture \(EA\). The business application insights help you to make informed decisions without manually reviewing large volumes of data.

-   **[Implement access control lists for security in AI agents](https://www.servicenow.com/docs/access?context=aia-security-implementation&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Enable security implementation to execute AI agents and agentic workflows through access control lists \(ACLs\) and user identities.

ACLs provide you with the capability to run AI agents and agentic workflow executions either as a dynamic user or an AI user.

To learn about ACLs for Now Assist for Enterprise Architecture \(EA\) agents and skills, see [Configure Now Assist for Enterprise Architecture \(EA\)](https://www.servicenow.com/docs/access?context=configure-now-assist-ea&version=zurich&pubname=zurich-application-portfolio-management&ft:locale=en-US) and [Enterprise Architecture AI agent generate enterprise architecture diagram agentic workflow](https://www.servicenow.com/docs/access?context=now-assist-aiagents-ea-diagramming-usecase&version=zurich&pubname=zurich-application-portfolio-management&ft:locale=en-US).

-   **[Generate a summary of the Architectural Decision Records \(ADR\) document or get a particular information from the document](https://www.servicenow.com/docs/access?context=summarize-docs-genai-skill-ea&version=zurich&pubname=zurich-application-portfolio-management&ft:locale=en-US)**

On the Architectural Decision Records page, use the field option in the Now Assist menu to derive a particular information about the ADR content.

-   **[New third-party AI model provider options available for all Now Assist applications](https://www.servicenow.com/docs/access?context=exploring-large-language-models&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Google Gemini and AWS Claude are available for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.


</td></tr><tr><td>

Now Assist for FSM

</td><td>

-   **[AI agent: Parts Manager](https://www.servicenow.com/docs/access?context=fsm-ai-agent-use-cases&version=zurich&pubname=zurich-field-service-management&ft:locale=en-US)**

Track and validate parts usage when closing work order tasks. The Parts Manager AI agent analyzes activity notes to update parts statuses and automatically adjusts inventory when tasks are closed. The AI agent is available through the Now Assist panel on platform and through the ServiceNow Agent mobile app.

-   **[AI agent: Create Work Order from image](https://www.servicenow.com/docs/access?context=fsm-ai-agent-use-cases&version=zurich&pubname=zurich-field-service-management&ft:locale=en-US)**

Create work orders by uploading photos of equipment issues. The AI agent extracts relevant information from the image to populate work order fields.

-   **[Primary action button for Now Assist Virtual Agent](https://www.servicenow.com/docs/access?context=now-assist-fsm&version=zurich&pubname=zurich-field-service-management&ft:locale=en-US)**

Access Now Assist Virtual Agent from a primary action button in the ServiceNow Agent mobile app navigation bar. Administrators can configure this button to launch Now Assist Virtual Agent or another global function.

-   **[Voice-to-text input in Now Assist Virtual Agent](https://www.servicenow.com/docs/access?context=now-assist-fsm&version=zurich&pubname=zurich-field-service-management&ft:locale=en-US)**

Use voice input when interacting with Now Assist Virtual Agent in the ServiceNow Agent mobile app. Tap the microphone icon to dictate messages instead of typing.

-   **[AI agent: Create Work Order](https://www.servicenow.com/docs/access?context=fsm-ai-agent-use-cases&version=zurich&pubname=zurich-field-service-management&ft:locale=en-US)**

You can leverage AI to create work orders from a written description of the issue. The Create Work Order AI agent is available through the Now Assist panel on platform and through the ServiceNow Agent mobile app.

-   **[New third-party AI model provider options available for all Now Assist applications](https://www.servicenow.com/docs/access?context=exploring-large-language-models&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Google Gemini and AWS Claude are available for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.

-   **[Custom template and custom prompt support](https://www.servicenow.com/docs/access?context=customize-a-skill&version=zurich&pubname=zurich-field-service-management&ft:locale=en-US)**

As an admin, you can clone the KB generation skill and customize the input fields. You can also clone the Work order task summarization skill, then access the skill in the Now Assist skill kit, and update the prompts.


</td></tr><tr><td>

Now Assist for Financial Services Operations \(FSO\)

</td><td>

-   **Agentic Contact Center for Banking AI Agents and skills in FSO**

Streamline your front-office banking operations by using the Agentic Contact Center for Banking application that provides AI-led experience for CSRs \(Customer Services Representatives\) through the below agents and skills:

    -   Customer 360 Experience
        -   Customer insights AI agent - It generates insights and recommendations that help you identify relevant details and take the next best action efficiently.
        -   Customer summarization skill - It summarizes customer data from multiple FSO applications, then provides customer summaries, product ownership context, financial overviews, and recent activity information.
    -   CSR Interaction
        -   Customer support AI agent - It provides real-time contextual insights and recommended steps that help reduce manual effort and decrease handle time during customer calls.
        -   Call summarization skill - It summarizes active customer calls and other customer information, then displays relevant insights dynamically, eliminating the need to navigate multiple windows during customer calls.

-   **[Standalone AI agents in FSO](https://www.servicenow.com/docs/access?context=ai-agents-fso&version=zurich&pubname=zurich-financial-services-operations&ft:locale=en-US)**

Automate ACH dispute resolution using AI-powered agents to assist in these tasks:

    1.  Evaluate merchant analysis
    2.  Evaluate Nacha operating guidelines
    3.  Review ACH dispute return recommendation
    4.  Dispute communication initiation
These AI agents provide recommended outcomes along with supporting rationale to assist decision-making. However, the final decision remains entirely with the dispute agent.

Dispute agents can now close tasks faster and with confidence using the **Apply Recommendation** option. With one click, the recommended outcome and rationale are applied and the task is closed, saving time, reducing manual effort, and boosting productivity.

-   **[Now LLM LTS support for Now Assist for FSO](https://www.servicenow.com/docs/access?context=now-llm-model-updates&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Long term stable \(LTS\) models are part of Now LLM Service and provide longer model stability windows for regulated industries. These models can integrate with tools to provide governance, monitoring, and compliance controls.


-   **[ACL security implementation](https://www.servicenow.com/docs/access?context=using-ai-agent-use-cases-in-now-assist-for-fso&version=zurich&pubname=zurich-financial-services-operations&ft:locale=en-US#section_q24_mlb_jgc)**

Enable security implementation to execute AI agents, agentic workflows, and generative AI skills through ACLs and user identities in Now Assist for FSO.

Predefined ACLs are provided for case summarization, Disputes intake via Virtual Agent, and the Help resolve friendly fraud AI agent and agentic workflow.


</td></tr><tr><td>

Now Assist for HR Service Delivery \(HRSD\)

</td><td>

[Zurich Patch 7](../quality/zurich-patch-7.md)

-   **[Some Now Assist skills are now turned on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Australia Early Access\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.

-   **[ER Interview Summarization](https://www.servicenow.com/docs/access?context=now-assist-hrsd-er-interview&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

Use the ER interview summarization skill to obtain summary of the ER case interview, which includes details such as quick recap, key assertions and responses.

-   **[Self-scheduling option in Schedule interviews agentic workflow](https://www.servicenow.com/docs/access?context=use-ai-agents-to-schedule-interviews&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

Recruiters and recruitment coordinators can now use self-scheduling to streamline interview scheduling by presenting applicants with available time slots to choose from. This option reduces the time to schedule in the absence of overlapping applicant-declared availability and minimizes the probability of manual handover to recruiter. The workflow recommends self-scheduling when beneficial, offers panelist-compatible slots sorted by confidence level, and automatically schedules interviews once applicants select their preferred time.

-   **[Offboarding knowledge transfer plan generation agentic workflow](https://www.servicenow.com/docs/access?context=offboarding-knowledge-x-agentic-wf&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

The offboarding knowledge transfer plan generation agentic workflow captures and organizes critical knowledge when employees leave. AI agents interact with managers to collect requirements, discover documents from the specified time period, categorize content into meaningful work areas, and facilitate employee review before sharing with successors.

-   **[Generate onboarding ramp-up plan](https://www.servicenow.com/docs/access?context=onboarding-ramp-up-plan-agentic-wf&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

The generate onboarding ramp-up plan workflow has been enhanced to create more relevant and personalized ramp-up plans for new hires. The workflow now recommends additional Journey services \(catalogs and order guides\) based on previously completed journeys and services requested by peers in similar roles. Managers can review these recommendations in Now Assist in Virtual Agent and add new services through a conversational experience.

-   **[Streamline feedback collection and review using the Employee feedback collection AI agent](https://www.servicenow.com/docs/access?context=employee-feedback-agent&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

As an admin, create reusable feedback templates using the Platform Surveys tool allowing managers to select and preview templates when requesting feedback, and help them quickly view a summarized snapshot of a reportee’s recent feedback with easy navigation to the feedback page in Manager Hub for detailed insights.


[Zurich Patch 4](../quality/zurich-patch-4.md)

-   **[Predict service and transfer HR cases agentic workflow](https://www.servicenow.com/docs/access?context=predict-transfer-hrcase&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

Analyze an HR case and automatically route it to the most appropriate HR service with the predict service and transfer HR cases agentic workflow.

-   **[Resolve noncritical HR cases agentic workflow](https://www.servicenow.com/docs/access?context=employee-issue-resolver-na&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

Use the resolve noncritical HR cases agentic workflow to assess the criticality of HR cases, and automatically respond to noncritical inquiries without human intervention. Human agent intervention is required when the request is identified as critical.

-   **[Resolve critical HR case agentic workflow](https://www.servicenow.com/docs/access?context=employee-issue-resolve-critical&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

Resolve critical HR requests efficiently with the resolve critical HR case agentic workflow. This workflow generates a tailored fulfillment plan for an HR case using fulfillment instructions, KB articles, or resolution notes of similar past cases. It helps accelerate the resolution process by providing planning support to HR agents.

-   **[Summarize an ER case using Now Assist for HRSD](https://www.servicenow.com/docs/access?context=now-assist-hrsd-summarize-er-case&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

Use the ER case summarization skill to obtain a comprehensive overview of the ER case, which includes key details, such as allegations, evidences, and interviews.

-   **[Help resolve tuition reimbursement requests agentic workflow](https://www.servicenow.com/docs/access?context=resolve-tuition-reimbursement-requests&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

Use the policy based HR evaluator skill to automatically compare employee tuition reimbursement submissions against company policies and return a decision of approval, denial, or request for additional information.

-   **[HR Voice AI agents](https://www.servicenow.com/docs/access?context=now-assist-hrsd-voice-ai-agents&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

Help employees handle self-service HR issues, such as creating cases, checking case status, and requesting time off, using real-time voice interactions with HR AI voice agents. With advanced speech-to-text and text-to-speech capabilities, configurable caller authentication, and seamless integration with Contact Center as a Service \(CCaaS\) providers, such as Twilio and Genesys, the agents can deliver an efficient and personalized experience for employees.


[Zurich Patch 2](../quality/zurich-patch-2.md)

-   **[Collect employee feedback with the help of an agent in Now Assist](https://www.servicenow.com/docs/access?context=employee-feedback-agent&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

As a manager, collect feedback from employees with the help from an agent in Now Assist. Identify which colleagues to request feedback from through Talent Development applications, journeys, and interaction patterns in Microsoft. Send, track, and manage feedback requests with built-in reminders. Leverage existing to-dos to send and manage feedback requests seamlessly.


-   **[Create a growth conversation with the help of an agent in Now Assist](https://www.servicenow.com/docs/access?context=agentic-wf-conversations-na-td&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

As a manager, use the growth conversations preparation AI agent to schedule and prepare for employee growth discussions. The agent provides a clear summary of employee activity and career journey as well as data-driven talking points for focused and impactful conversations.

**Note:** This feature is available when you have both Now Assist for HR Service Delivery \(HRSD\), which installs Now Assist for Talent and HR Talent AI Agent Collection.


[Zurich Patch 1](../quality/zurich-patch-1.md)

-   **[Implement access control in Now Assist AI agents](https://www.servicenow.com/docs/access?context=aia-security-implementation&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Enable security settings to run AI agents and agentic workflows by using ACLs and user identities. You can configure and manage the ACLs in AI Agent Studio.

-   **[HCM AI agents](https://www.servicenow.com/docs/access?context=conversational-agents&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

Use AI agents to enable employees to place requests to the HCM system, such as apply for time off or update details.

-   **[Resolve HR cases agentic workflow](https://www.servicenow.com/docs/access?context=employee-issue-resolver-na&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

Generate a fulfillment plan in a series of steps for an HR case by selecting the **Generate Plan** button on the HR case. HR agents can add prompts to further refine the AI-generated fulfillment plan before the plan is published to the work notes of the case.

-   **[HR case sentiment analysis](https://www.servicenow.com/docs/access?context=analyze-sentiments-now-assist&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

Prioritize cases by the sentiment score and monitor sentiment trends over time. HR agents can review a brief summary to understand the reasoning for the sentiment score for each HR case.

-   **[Schedule interviews agentic workflow](https://www.servicenow.com/docs/access?context=use-ai-agents-to-schedule-interviews&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

Use AI agents to automate the interview scheduling process from the Now Assist panel and use the inputs from recruiters or recruitment coordinators to send out interview invites.


-   **[Generate onboarding ramp-up agentic workflow](https://www.servicenow.com/docs/access?context=onboarding-ramp-up-plan-agentic-wf&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

Accelerate onboarding with the generate onboarding ramp-up plan agentic workflow, which creates personalized and team-specific plans for every new hire. Powered by AI agents, it tailors learning paths, team tasks, and 1:1 introductions to help employees ramp up fast, build stronger connections, and reach productivity quickly.

-   **[Resolve noncritical HR cases agentic workflow](https://www.servicenow.com/docs/access?context=employee-issue-resolver-na&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

Evaluate case criticality and retrieve relevant knowledge articles to resolve HR cases, minimizing the need for agent intervention. Generate a fulfillment plan for an HR case, which helps resolve the HR case fast.


Zurich Early Availability

-   **[New third-party AI model provider options available for all Now Assist applications](https://www.servicenow.com/docs/access?context=exploring-large-language-models&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Google Gemini and AWS Claude are available for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.

-   **[Use AI agents to create job requisition](https://www.servicenow.com/docs/access?context=use-ai-agents-to-create-job-req&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

Use AI agents to automate the process for creating a job requisition from the Virtual Agent chat window by using the inputs from your hiring managers.


</td></tr><tr><td>

Now Assist for Hardware Asset Management \(HAM\)

</td><td>

-   **[Manage your assets with comprehensive and real-time data](https://www.servicenow.com/docs/access?context=generate-asset-analysis-now-assist-ham&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

View consolidated asset information through AI-generated analysis summary on the asset record. The AI-generated summary dynamically updates based on the asset state and includes context from any active incidents or tasks. The summary displays the asset life cycle, current assignment and location, audit status, financial metrics, and identifies missing data to support asset management activities.


-   **[Optimize hardware asset repair process with the suite of AI agents](https://www.servicenow.com/docs/access?context=now-assist-ham-repair-agent-workflow&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

Automate the repair of defective and out-of-warranty hardware assets by using AI agents in the help repair hardware assets agentic workflow. These AI agents validate the repair tasks, provide detailed troubleshooting and repair instructions, and complete the tasks on receiving user confirmation.


-   **[Configure ACLs for AI agents and agentic workflows](https://www.servicenow.com/docs/access?context=aia-security-implementation&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Configure the access control lists for who can discover and trigger AI agents and agentic workflows in their guided setups in AI Agent Studio. You can determine whether an AI agent or agentic workflow behaves as a dynamic user or as an AI user. You can also specify if an AI agent or agentic workflow can be available to all authenticated users or publicly available.


</td></tr><tr><td>

Now Assist for IT Operations Management \(ITOM\)

</td><td>

-   **[Configure the Dynatrace MCP server agent](https://www.servicenow.com/docs/access?context=now-assist-itom-config-dynatrace-mcp&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

Set up the new Dynatrace MCP server agent, which replaces the Dynatrace analysis AI agent, for deeper alert analysis. In the analyze alert impact agentic workflow, you can ask more detailed questions about Dynatrace alerts, such as questions about logs, topology, or recent changes. In the manage alerts autonomously agentic workflow, investigations now pull more comprehensive Dynatrace context based on alert type.

-   **[Updates to the manage alerts autonomously agentic workflow](https://www.servicenow.com/docs/access?context=itom-autonomous-operator-workflow&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

The manage alerts autonomously agentic workflow has been updated to provide additional AI insights in the preview panel and alert record. These updates include:

    -   Summaries of the logic behind automated decisions, such as auto closures of insignificant alerts
    -   A written summary of the Service Observability dashboard
Additionally, automated alert groups are now supported across Now Assist features such as alert assist and AI insights.

-   **[Analyze log analytics alerts to assess impact and triage urgency](https://www.servicenow.com/docs/access?context=itom-autonomous-operator-workflow&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

The manage alert autonomously agentic workflow now includes AI-driven analysis for log analytics alerts. The alert hypothesizer skill evaluates historical patterns to assess if triage is required. It also classifies alerts as proactive or reactive, where proactive indicates emerging risk and reactive indicates an active issue. The analysis can include contextual insights such as potential failure scenarios to support an alert investigation.

-   **[Analyze Service Observability dashboard skill](https://www.servicenow.com/docs/access?context=analyze-a-dashboard-in-service-observability&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

The analyze Service Observability dashboard skill uses generative AI to summarize a single Service Observability dashboard and calls out insights found in charts. This summary helps operators quickly orient to and understand a particular dashboard. Once activated, this skill is available on all Service Observability dashboards and runs automatically from Incident Investigation when Service Observability is installed.

-   **[Analyze service health](https://www.servicenow.com/docs/access?context=analyze-service-health-in-service-observability&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

The analyze service health skill uses generative AI to analyze all available Service Observability dashboards for the selected service in the Service Operations Workspace \(SOW\). It generates a summary of a service’s health and calls out any found insights. Once activated, this skill is available from the header of a service record in the SOW.


-   **[Enhance IT operations with AI-driven, autonomous alert management using the manage alerts autonomously workflow](https://www.servicenow.com/docs/access?context=itom-autonomous-operator-workflow&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

Automate alert triage, impact analysis, and root cause investigation with an AI-driven workflow that replaces manual operator steps with autonomous decision-making. The workflow processes incoming alerts end-to-end and surfaces consolidated insights through Express List, giving operators immediate visibility into what happened, what's affected, and why.

-   **[Configure the Datadog and Gemini Cloud Assistant observability skills](https://www.servicenow.com/docs/access?context=itom-ai-agent-configuration&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

Set up the new Datadog and Gemini Cloud Assistant observability skills to get insights from those tools in the manage alerts autonomously agentic workflow. With Datadog and Google Gemini, the workflow now supports five observability tools, including Dynatrace, Kentik, and New Relic, helping you investigate and respond to a wider range of alerts.

-   **[AIOps LEAP skill setup](https://www.servicenow.com/docs/access?context=change-leap-large-languauge-model-llm&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

Status information for records grouping job run is available when skills are modified with support KB content.

-   **[AIOps LEAP settings page](https://www.servicenow.com/docs/access?context=setup-aiops-leap-properties&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

The new interface for the AIOps LEAP properties includes default configuration to achieve opportunity savings and reporting.

-   **[Action Insights panel](https://www.servicenow.com/docs/access?context=automation-opportunity-sub-groups&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

The Action Insights panel on the automation opportunity details page provides suggestion to create sub-groups when there are large volumes of records. This helps optimize opportunities and knowledge gaps for architects.


-   **[View an error analysis by Now Assist in Agent Client Collector](https://www.servicenow.com/docs/access?context=agent-errors-now-assist&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

Starting in version 6.0.0, use Now Assist AI agents to gather information about errors occurring on Agent Client Collector agents. For example, you can verify the underlying cause behind a specific error or error code.


-   **[Configure the Dynatrace analysis AI agent](https://www.servicenow.com/docs/access?context=now-assist-itom-config-dynatrace&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

Set up the Dynatrace analysis AI agent in the analyze alert impact agentic workflow to investigate Dynatrace alerts. With Dynatrace, the agentic workflow now supports three observability tools, including Kentik and New Relic, helping you investigate and respond to a wider range of alerts.

-   **[Expand the analyze alert impact agentic workflow with four new AIOps agents](https://www.servicenow.com/docs/access?context=now-assist-itom-use-aia&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

Get a fuller view of alert impact with four new AIOps agents in the analyze alert impact agentic workflow. Along with observability data, the agentic workflow now includes information from within ServiceNow to help surface business impact and related issues. Activate the AIOps agents to include them in the agentic workflow.

-   **[Enhance your decision-making process with the analyze potential impact agentic workflow](https://www.servicenow.com/docs/access?context=now-assist-itom-analyze-potential-impact-workflow&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

Assess the potential impact of a change using the analyze potential impact agentic workflow. This workflow provides an analysis of the relevant servers and suggested services that might be impacted by your change request, ensuring that you have all the insights needed to make informed decisions before making a change.

-   **[Add access control lists for security in AI agents](https://www.servicenow.com/docs/access?context=aia-security-implementation&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Enable security settings to run AI agents and agentic workflows using ACLs and user identities. You can configure and manage the ACLs in AI Agent Studio.

-   **[Now Assist certificate renewal AI agent](https://www.servicenow.com/docs/access?context=now-assist-cert-renewal-ai-agent&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

Use the Now Assist certificate renewal AI agentic workflow to automatically renew certificates before they expire. You can perform the following with the Now Assist certificate renewal AI agent:

    -   Renew individual certificates
    -   Find all certificates about to expire
    -   Renew all certificates about to expire in a single prompt
-   **[Utilize the triage and analyze alerts agentic workflow in the context of an incident](https://www.servicenow.com/docs/access?context=itom-alert-triage-agentic-workflow&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

Initiate the triage and analyze alerts agentic workflow from the Now Assist panel in the context of the incident form to perform all the functions of the workflow. This workflow automatically assigns, acknowledges, and summarizes origin alerts, determines their significance through historical analysis, and analyzes related incidents.


</td></tr><tr><td>

Now Assist for IT Service Management \(ITSM\)

</td><td>

-   **[Incident assist agentic workflow](https://www.servicenow.com/docs/access?context=now-assist-itsm-incident-assist-workflow&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

Answer incident-related questions using context-aware agents. Handle queries about incident details and get information about related records.

-   **[Enhancements to the Incident assist skill](https://www.servicenow.com/docs/access?context=now-assist-itsm-incident-assist&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

The features in the \[DEPRECATED\] Incident assist skill is available in the Incident assist agentic workflow. You may turn off this skill and use the agentic workflow that has enhanced capabilities.

-   **[Configure summaries for Request Management records](https://www.servicenow.com/docs/access?context=cust-now-assist-request-summarization-skill&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

As an admin, you can configure the following Request Management skills:

    -   Request summarization
    -   Requested item summarization
    -   Catalog task summarization
-   **[Summarize Request Management records](https://www.servicenow.com/docs/access?context=summarize-request-related-activity-response-generation&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

View an aggregate of all relevant updates and progress indicators in a single, dynamic summary.


-   **[Creating a catalog item for unlocking accounts using the voice AI agent](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-voice&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

Use the demo Submit account unlock catalog with the voice AI agent to create a catalog item to unlock the specified account when a user calls the help desk.

-   **[Enhancements to Troubleshoot Outlook issue with voice AI agent](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-voice&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

Email relevant troubleshooting articles and instructions to users when you troubleshoot Outlook issues for them.

-   **[ITSM Conversational analytics dashboard](https://www.servicenow.com/docs/access?context=using-itsm-conversational-analytics-dashboard&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

Get insights into virtual agent adoption, usage trends, and track metrics in Now Assist in Virtual Agent.

-   **[Generate a response to request activity](https://www.servicenow.com/docs/access?context=summarize-request-related-activity-response-generation&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

Automatically generate a response in record activity streams using the activity response generation skills for requests and requested items.

-   **[DEX issue diagnosis and resolution agentic workflow](https://www.servicenow.com/docs/access?context=now-assist-itsm-dex-diagnosis-resolution-workflow&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

Service desk agents can diagnose and resolve Zoom call quality issues using the DEX issue diagnosis and resolution agentic workflow, which integrates Zoom-specific diagnostics that correlate device, network, and application data.

-   **[AI-powered root cause analysis for Zoom call quality issues](https://www.servicenow.com/docs/access?context=investigate-and-resolve-zoom-call-issues&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

Use Now Assist for Zoom call issues to identify the root cause of call quality degradation and review the supporting metric evidence for deeper insight. The analysis highlights the contributing device and network factors directly in the Zoom call quality view. Get the real-time guidance, including device ready remedial actions, contextual self-help instructions, and relevant Knowledge articles to help resolve the issue efficiently.

-   **[Get AI driven insights for boot time performance](https://www.servicenow.com/docs/access?context=investigate-and-resolve-boot-time-issues&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

Monitor device boot time to identify slow start-up issues and use Now Assist to investigate the root cause and get suggested resolutions, including remedial actions, self-help instructions, and Knowledge articles to resolve boot performance problems quickly.


-   **[Adding self-service and deflection to phone channels using Voice AI agents](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-voice&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

Enhance employee productivity with Voice AI agents by adding self-service and deflection to their phone channel.

-   **[Getting password reset instructions using an AI agent](https://www.servicenow.com/docs/access?context=itsm-va-ai-agents&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

The **DEMO Password reset agent** is a demo AI agent that provides requesters with password reset instructions for the account that they need help with.

-   **[Editing the incident summarization skill prompts and inputs using the Now Assist Skill Kit](https://www.servicenow.com/docs/access?context=cust-now-assist-itsm-record-summ-skill&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

You can edit the prompts and inputs for the incident summarization skill within the Now Assist Skill Kit \(NASK\) and test the updates you've made.

-   **[Expanding attachment summarization capabilities to include additional document formats and language](https://www.servicenow.com/docs/access?context=cust-now-assist-itsm-record-summ-skill&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

You can now summarize, analyze, and extract data from attachments in additional formats and languages.

-   **[Creating a knowledge article in any incident state](https://www.servicenow.com/docs/access?context=cust-now-assist-itsm-skill&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

Create knowledge articles from any incident state by configuring a system property for the required states.

-   **[Edit a knowledge article when one article is attached to an incident](https://www.servicenow.com/docs/access?context=Now-Assist-generate-article-SOW-itsm&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

You can edit a knowledge article if your administrator has enabled the system property to display the **Edit knowledge** button and if you have only one article attached to the incident.

-   **[Enhancing the efficiency of the Investigate and resolve ITSM incidents agentic workflow](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-incident-resolver-workflow&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

For better efficiency, the ITSM incident resolution investigation AI agent and Find catalog item AI agent have been combined into one agent. This agent is called the ITSM incident resolution plan investigation AI agent.

-   **[Enhancing the efficiency of the Triage and categorize ITSM incidents agentic workflow](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-catincidents-usecase&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

For better efficiency, the Link major incident AI agent and the Link incident to problem AI agent have been combined into one agent. This agent is called the Link major incident or problem AI agent.

-   **[Enhancing the efficiency of the Generate change request plans agentic workflow](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-change-planner-usecase&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

For better efficiency, the existing six agents in the change request plans agentic workflow have been combined into one agent. This agent is called the Change request plans AI agent.

-   **[Display the risk factors sources that contribute to the calculation of a change risk explanation](https://www.servicenow.com/docs/access?context=cust-now-assist-itsm-change-risk-skill&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

When a change risk is calculated, Now Assist for ITSM provides the list of the change requests that were used to identify the potential risks for the change risk explanation so that you can understand which risk factors contributed to the calculated risk.

-   **[Generating resolution notes using the Now Assist context menu](https://www.servicenow.com/docs/access?context=cust-now-assist-itsm-gen-resolution-notes-skill&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

As an admin, you can view and configure the Now Assist context menu \(NACM\) to generate resolution notes using the **Resolution notes generation** skill.

-   **[Generating an activity response using the Now Assist context menu](https://www.servicenow.com/docs/access?context=cust-now-assist-itsm-activity-response-skill&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

As an admin, you can view and configure the Now Assist context menu \(NACM\) for an activity response using the **Incident activity response generation** skill.

-   **[Selecting the desired knowledge base and template for creating knowledge articles using the new interface](https://www.servicenow.com/docs/access?context=Now-Assist-generate-article-SOW-itsm&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

With this new interface, you can select the desired knowledge base and the template to create the article in Service Operations Workspace or Core UI.

-   **[Masking roles for controlled access to agentic workflows, AI agents, and skills](https://www.servicenow.com/docs/access?context=supporting-information-now-assist-itsm&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

Mask roles to restrict access to agentic workflows, AI Agents, and skills, ensuring that users receive only the necessary permissions.

-   **[Suggest configuration items for a change request agentic workflow](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-suggest-configuration-items-for-a-change-request&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

Find and link applicable configuration items \(CIs\) to a change request from the Now Assist panel in a conversational and intuitive way using the Suggest configuration items for a change request agentic workflow.

-   **[Create outages for a change request agentic workflow](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-create-outages-for-a-change-request&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

Associate outages with a change request in a conversational and intuitive way from the Now Assist panel using the Create outages for a change request agentic workflow.

-   **[Create standard change request agentic workflow](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-create-change-request-workflow&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

Create a standard, normal, or emergency change request in a conversational and intuitive way from the Now Assist panel using the Create standard change request agentic workflow.

-   **[Create standard change template proposal agentic workflow](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-create-standard-change-template-proposal&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

Create a change template proposal record based on similar change requests in a conversational and intuitive way from the Now Assist panel using the Create standard change template proposal agentic workflow.

-   **[DEX issue diagnosis and resolution agentic workflow](https://www.servicenow.com/docs/access?context=now-assist-itsm-dex-diagnosis-resolution-workflow&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

Diagnose and resolve issues on DEX monitored devices through a structured process that includes diagnosis of the cause, a resolution plan with actionable steps, and documenting the resolution in the incident record.

-   **[Generate comprehensive release notes for a release in Digital Product Release](https://www.servicenow.com/docs/access?context=dpr-generate-release-notes&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

Automatically generate structured release notes for a release using the Generate Release Notes skill. This AI-driven capability compiles enhancements, features, incidents, and change records into structured notes with an executive summary and scope of work sections, reducing manual effort and ensuring consistency. You can edit the AI-generated draft as needed, then publish and share via link or PDF download.


-   **[Classify service and CI AI agent](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-catincidents-usecase&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

Automatically assign the related service, service offering, and configuration item \(CI\) to an incident using the Classify service and CI AI agent in the Triage and categorize ITSM incidents agentic workflow.

-   **[Wrap-up and resolve incident agentic workflow](https://www.servicenow.com/docs/access?context=now-assist-itsm-wrap-up-resolve-incident-aw&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

Generate resolution notes including root cause and resolution steps to resolve an incident, create or attach Knowledge Base \(KB\) articles, update duplicate incident information to the incident record. Attach Known Error \(KE\) articles when the resolution code is a known error. The agentic workflow has the following AI Agents:

    -   Incident resolution details AI agent
    -   Incident knowledge article AI agent
    -   Incident known error article AI agent
-   **[IT Service Management AI agent collection assess conflicts for a change request agentic workflow](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-assess-conflicts-workflow&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

Autonomously identify conflict types and summarize the impacted schedules, CIs and services related to the change request using the Change conflict assessor AI agent.

-   **[IT Service Management AI agent collection assess quality of a change request agentic workflow](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-assess-quality-change-request-workflow&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

Assess the quality of a change request and generate suggestions to improve the quality as needed using the Change quality assessor AI agent.

-   **[IT Service Management AI agent collection explain SLA agentic workflow](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-explain-sla-workflow&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

View the detailed breakdown of the assignment and ownership relevant to the SLA for an incident, problem, case, or change request using the Explain SLA AI agent.

-   **[IT Service Management AI agent collection schedule a change agentic workflow](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-schedule-change-agentic-workflow&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

Find and schedule the optimum slots for change requests using the Schedule Change Request AI agent.

-   **[Setting the AI user as the Run as user in the Triage and categorize incidents agentic workflow](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-catincidents-usecase&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

Create AI users for the identity type **AI agent** and assign roles to the AI user based on your needs. Run the agentic workflow as the AI user that determines the data access defined by the role.

-   **[Matching flow action access control roles with the agent roles for the Notify users with Twilio agentic workflow](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-twilio-text-usecase&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

When you update the agent role for the Notify users with Twilio agentic workflow, you must also update the corresponding access controls with those roles.

-   **[Matching flow action access control roles with the agent roles for the Manage Microsoft 365 group members agentic workflow](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-O365-groupmembers-workflow&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

When you update the agent role for the Manage Microsoft 365 group members agentic workflow, you must also update the corresponding access controls with those roles.

-   **[Using the itil role to add or update work notes in the Now Assist panel](https://www.servicenow.com/docs/access?context=request-gen-ai-capabilities-itsm-now-assist-panel&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

To add or update work notes in the Now Assist panel, the logged-in user must have the itil role.


</td></tr><tr><td>

Now Assist for Legal Service Delivery \(LSD\)

</td><td>

-   **[Submit COI request using Now Assist conversational intake](https://www.servicenow.com/docs/access?context=now-assist-lsd-convi&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

Submit a Conflict of Interest \(COI\) request through a natural language conversation. The conversational intake for Legal Conflict of Interest is available in the base system.


-   **[Now LLM LTS support for Now Assist for Legal Service Delivery \(LSD\)](https://www.servicenow.com/docs/access?context=now-llm-model-updates&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Long term stable \(LTS\) models are part of Now LLM Service and provide longer model stability windows for regulated industries. These models can integrate with tools to provide governance, monitoring, and compliance controls.

-   **[Some Now Assist skills are turned on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Zurich Patch 4\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.

-   **[New third-party AI model provider options available for all Now Assist applications](https://www.servicenow.com/docs/access?context=exploring-large-language-models&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Google Gemini and AWS Claude are available for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.


</td></tr><tr><td>

Now Assist for Manufacturing Commercial Operations \(MCO\)

</td><td>

-   **[Execute recall campaigns faster](https://www.servicenow.com/docs/access?context=execute-recall-campaigns&version=zurich&pubname=zurich-manufacturing&ft:locale=en-US)**

Use the create recall corrective actions AI agent to extract the information available in the repair documents. The AI agent identifies and collects all relevant data contained within the repair documents and generates the corrective action and the corresponding charges.

The AI agent sets the asset applicability criteria to determine which corrective actions are applicable to that particular subset of the impacted asset.


</td></tr><tr><td>

Now Assist for Operational Sustainability Management Management

</td><td>

-   **[Use agentic AI in Now Assist for Operational Sustainability](https://www.servicenow.com/docs/access?context=use-agentic-ai-in-now-assist-for-esg-management&version=zurich&pubname=zurich-environmental-social-governance&ft:locale=en-US)**

The carbon calculations agentic workflow acts as a copilot for sustainability teams, streamlining carbon accounting workflows. It intelligently selects metric definitions and emission factors from the library, generates calculated metric definitions, and enables user review and adjustments before final use.


-   **[Extract data from utility invoices](https://www.servicenow.com/docs/access?context=extract-data-from-utility-invoices&version=zurich&pubname=zurich-environmental-social-governance&ft:locale=en-US)**

Now Assist for Operational Sustainability with document intelligence for utility bills, designed to streamline your ESG metric data collection and reporting. Here are the key highlights:

    -   Extract ESG metric data with Gen AI-Powered Document Intelligence from utility bills, like electricity, gas, and water, with accuracy and efficiency.
    -   Automate data collection by eliminating manual data entry and reducing errors.
    -   Integrate extracted data with ESG metric workflows for a seamless experience.
    -   Scale your operations with an enterprise-scale solution that handles large volumes of data.
    -   Confirm compliance and transparency with built-in audit features that support reporting requirements.

</td></tr><tr><td>

Now Assist for Operational Technology Service Management \(OTSM\)

</td><td>

-   **[Summarize an Operational Technology incident by using Now Assist for Operational Technology Service Management \(OTSM\)](https://www.servicenow.com/docs/access?context=summarize-ot-incident-now-assist&version=zurich&pubname=zurich-operational-technology&ft:locale=en-US)**

Automatically summarize an OT incident using the **Summarize** UI action to produce a concise summary of the incident.

-   **[Generate resolution notes for an Operational Technology incident](https://www.servicenow.com/docs/access?context=generate-resolution-notes-ot-incident&version=zurich&pubname=zurich-operational-technology&ft:locale=en-US)**

Automatically generate resolution notes for an OT incident using the **Generate resolution notes** UI action to produce a concise summary of the incident.

-   **[Generate OT KB articles agentic workflow](https://www.servicenow.com/docs/access?context=agent-ot-knowledge-generator&version=zurich&pubname=zurich-operational-technology&ft:locale=en-US)**

Automatically generate a KB article for an OT incident when the state of the incident is set to **Resolved**. The article contains the following information:

    -   Site
    -   OT Device
    -   Equipment model entity
    -   Summarization
    -   Resolution notes
    -   KB Base
    -   Author

</td></tr><tr><td>

Now Assist for Order Management

</td><td>

[Zurich Patch 7](../quality/zurich-patch-7.md)

-   **[AI-powered invoice case management for customers](https://www.servicenow.com/docs/access?context=dispute-invoice-issues-now-assist&version=zurich&pubname=zurich-order-management&ft:locale=en-US)**

Enable customers to report quantity-related invoice disputes through an AI-powered virtual assistant on the Business Portal. Customers can describe the discrepancies through natural conversation, and the assistant validates details, creates cases, and autonomously resolves eligible disputes by issuing credit notes or replacement orders, or connects customers with a human agent when needed.

-   **[Invoice dispute intake with voice assistant](https://www.servicenow.com/docs/access?context=now-assist-invoice-mgmt-voice-aiagent&version=zurich&pubname=zurich-order-management&ft:locale=en-US)**

Enable customers to report quantity-related invoice disputes using voice commands through an AI-powered voice assistant on the Business Portal. Customers can describe discrepancies through natural speech and the assistant captures dispute details to create invoice cases or connects customers with a human agent.

-   **[Human agent handoff with context transfer](https://www.servicenow.com/docs/access?context=resolve-invoice-case-now-assist-agent&version=zurich&pubname=zurich-order-management&ft:locale=en-US)**

Help customers to escalate complex disputes seamlessly to a live agent. The full conversation context, including invoice details, dispute reason, and prior AI actions are transferred to the CSM/FSM Configurable Workspace, enabling live agents to continue without asking customers to repeat information.

-   **[Now Assist for invoice case resolution](https://www.servicenow.com/docs/access?context=resolve-invoice-case-now-assist-agent&version=zurich&pubname=zurich-order-management&ft:locale=en-US)**

Help accelerate invoice dispute resolution by surfacing similar cases and common resolution patterns in the Now Assist panel. Agents can request help with an invoice case to view how similar disputes were resolved, reducing research time and improving consistency.

-   **[Automated email notifications for invoice cases](https://www.servicenow.com/docs/access?context=now-assist-order-management-using&version=zurich&pubname=zurich-order-management&ft:locale=en-US)**

Keep customers informed with automated email notifications at key points in the invoice case life cycle, including case creation confirmation, resolution details with credit note or replacement order information, and the next steps for cases requiring human review.

-   **[Return Merchandise Authorization](https://www.servicenow.com/docs/access?context=return-merchandise-authorization&version=zurich&pubname=zurich-order-management&ft:locale=en-US)**

Leverage the RMA AI agent for automated entitlement and case handling with the following features:

    -   Automates entitlement checks with real‑time warranty validation
    -   Selects best‑fit resolution and sends for customer approval
    -   Generates recommended actions when no valid entitlement is found
    -   Provides proactive case updates and follow‑ups
    -   Answers customer queries and handles multi‑intent emails

[Zurich Patch 4](../quality/zurich-patch-4.md)

-   **[Enable the manage order operations agent in the Business Portal](https://www.servicenow.com/docs/access?context=enable-manage-order-operations-ai-agent&version=zurich&pubname=zurich-order-management&ft:locale=en-US)**

Activate the manage order operations agent so that you can make the agent available to your customers on the Business Portal.

-   **[Request order changes using Now Assist](https://www.servicenow.com/docs/access?context=request-order-changes-now-assist&version=zurich&pubname=zurich-order-management&ft:locale=en-US)**

Use the manage order operations agent to provide a seamless experience to your customers on the Business Portal, enabling them to create order cases using a virtual assistant effortlessly. The AI agent can intelligently categorize requests for expedited delivery by creating order-related cases linked directly to the specific order, significantly reducing manual case creation and speeding up resolution times. Interaction channels include chat and voice options.

-   **[Summarize an order using Summarization for Order Management](https://www.servicenow.com/docs/access?context=now-assist-order-mgmt-summarize-order&version=zurich&pubname=zurich-order-management&ft:locale=en-US)**

Generate a summary of a complex order for a unified view of the order's current state to:

    -   Respond confidently to customer queries with accurate, real-time order status.
    -   Track changes and validate details to maintain consistency and transparency.
    -   Minimize errors and improve communication across suppliers and partners.
    -   Monitor tasks that are at risk of missing deadlines.
    -   Assign tasks to appropriate resources based on priority and skill.
    -   Make rapid prioritization decisions to avoid delays and help ensure timely fulfillment.

</td></tr><tr><td>

Now Assist for Retail Service Management \(RSM\)

</td><td>

[Zurich Patch 4](../quality/zurich-patch-4.md)

New tools or scripts have been added to support store inquiry case management, including:

-   Updating case details: Modifying the current information about a case, such as adding resolution information or updating work notes.
-   Fetching similar cases: Retrieving past cases that have similar descriptions to the current case.
-   Retrieving metadata for selectable links: Gathering information about a source \(like a case or document\) to create a selectable link to it.
-   Get case details: Retrieving the current information about a case, such as its short description.

</td></tr><tr><td>

Now Assist for Sales Force Automation \(SFA\)

</td><td>

-   **[Use agentic workflows in Now Assist for Sales Force Automation \(SFA\)](https://www.servicenow.com/docs/access?context=using-agentic-worklflows-in-lead-management&version=zurich&pubname=zurich-order-management&ft:locale=en-US)**

The Help nurture new leads agentic workflow works with a team of AI agents to assist the sales agents to manage the life cycle of leads, either independently or under supervision.

<table id="table_s5m_lpg_jgc"><thead><tr><th>

Workflow name

</th><th>

Description

</th><th>

Available AI agents

</th></tr></thead><tbody><tr><td>

Help nurture new leads

</td><td>

-   Outlines the steps required to engage the lead with the sales agent.
-   Sends initial outreach and follow-up emails.
-   Retrieves emails, classifies the intent, and routes it to the right sales agent to take action.
-   Schedules, reschedules, or deletes the appointments based on sales agent availability.
-   Manages the leads who want to opt out or uninterested.


</td><td>

-   Lead outreach AI agent
-   Inbound email AI agent
-   Appointment management AI agent
-   Lead disinterest AI agent


</td></tr></tbody>
</table>


</td></tr><tr><td>

Now Assist for Sales and Order Management for Telecommunications \(SOMT\)

</td><td>

-   **[Order enrichment agent](https://www.servicenow.com/docs/access?context=order-enrichment-agent-somt&version=zurich&pubname=zurich-telecom-media-technology&ft:locale=en-US)**

Use the order enrichment AI agent to collect the customer order information, identify if the order needs enrichment, and create the enrichment tasks. The AI agent creates a task and triggers the order fulfillment AI agent on its completion.

-   **[Order fulfillment agent](https://www.servicenow.com/docs/access?context=order-fulfillment-agent-somt&version=zurich&pubname=zurich-telecom-media-technology&ft:locale=en-US)**

Use the order fulfillment agent to identify the tasks for domain orders using historical data from similar orders. After decomposition, the fulfillment AI agent creates and fulfills order tasks by checking the historical and applicable tasks.

-   **[Configure ACLs for AI agents and agentic workflows](https://www.servicenow.com/docs/access?context=aia-security-implementation&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Configure the access control lists for who can discover and trigger AI agents and agentic workflows in their guided setups in AI Agent Studio. You can determine whether an AI agent or agentic workflow behaves as a dynamic user or as an AI user. You can also specify if an AI agent or agentic workflow can be available to all authenticated users or publicly available.

-   **[Role configuration required for agentic workflows and AI agents](https://www.servicenow.com/docs/access?context=aia-role-masking&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Agentic workflows and AI agents included with Now Assist applications require additional security configuration. If you select **Users with selected roles** for your user access security controls for an agentic workflow or AI agent, you must add the installed roles, or they won't execute. Data access settings must also include these roles. See the documentation for the agentic workflow or AI agent for the specific roles you must add. After the roles are configured, users must have the specified role to invoke the agentic workflow or AI agent.


</td></tr><tr><td>

Now Assist for Security Incident Response \(SIR\)

</td><td>

-   **[Resolve a security incident](https://www.servicenow.com/docs/access?context=now-assist-sir-resolve-incident-ai-workflow&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

Help enhance incident resolution plan generation by adding your existing runbooks to the AI runbooks section within the Security incident resolution plan skill. The existing runbooks provide additional context to the skill.


-   **[Role configuration required for agentic workflows and AI agents](https://www.servicenow.com/docs/access?context=aia-role-masking&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Agentic workflows and AI agents included with Now Assist applications require additional security configuration. If you select **Users with selected roles** for your user access security controls for an agentic workflow or AI agent, you must add the installed roles, or they won't execute. Data access settings must also include these roles. See the documentation for the agentic workflow or AI agent for the specific roles you must add. After the roles are configured, users must have the specified role to invoke the agentic workflow or AI agent.

-   **[Exploring Security incident quality assessment with Now Assist for Security Incident Response](https://www.servicenow.com/docs/access?context=na-sir-quality-assessment&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

Use generative AI to create a quality assessment report of a security incident. The reports are generated using a predefined, natural language rule set. The report provides an overall assessment summary followed by the detailed assessment for all the rules.


-   **[Generate SIR Shift Handover Report](https://www.servicenow.com/docs/access?context=add-incidents-shifthandover-ai-agent&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

The AI agent helps add security incident details to a shift handover report. The agent populates the different sections of the shift handover with appropriate content by identifying the relevant details from the security incident. The AI agent can fetch details of the security incident and identify if the analyst has access to the shift handover record. The AI agent can generate content for each section of the shift handover record and asks for analysts feedback on the content. The AI agent refines the content based on the feedback and saves the content to the records on approval.


-   **[Using agentic AI workflows in Now Assist for Security Incident Response](https://www.servicenow.com/docs/access?context=using-now-assist-ai-agents-sir&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

The analyze security operations metrics agentic workflow helps security managers to analyze their teams' performance.

    -   Generate metrics for Security Incident Response \(SIR\) records for case volume, mean time to assign \(MTTA\), and mean time to resolve \(MTTR\) for a date range of your choosing.
    -   Request suggestions for how to improve MTTR, MTTA, and volume based on your metrics.
-   **[Enhancements to correlation insights in Now Assist for Security Incident Response](https://www.servicenow.com/docs/access?context=generating-insights-for-now-assist-for-security&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

You can generate and view results for correlation insights in the Security Incident Response Workspace.

    -   Correlation insights aren’t limited to the primary configuration item \(CI\) or affected users associated with a security incident. You can base your correlation insights on any CI or affected user for a security incident.
    -   You can generate correlation insights from the **Investigation** tab for a security incident in any state in the Security Incident Response Workspace.
    -   You can generate insights for multiple items simultaneously for Associated Observables, Configuration items, and Affected Users.
    -   Results are displayed in a modeless dialog that you can size and move.
-   **[Using the security incident resolution agentic workflow](https://www.servicenow.com/docs/access?context=now-assist-sir-resolve-incident-ai-workflow&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

Use the security incident resolution agentic workflow to close your security incidents. Analysts can chat with AI agents in natural language to resolve the security incidents. The AI agent analyzes the incident details, existing runbooks, Knowledge articles, and past similar security incidents as inputs, and provides a resolution plan. The AI agent also assists the analysts to resolve the security incident.


</td></tr><tr><td>

Now Assist for Software Asset Management \(SAM\)

</td><td>

[Zurich Patch 1](../quality/zurich-patch-1.md)

-   **[Use an agentic workflow to automate software asset sourcing to improve operational efficiency](https://www.servicenow.com/docs/access?context=using-now-assist-sam-ai-agents-usecases&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

Use AI agents in the Help manage software request agentic workflow to automate software asset sourcing, either through automatic license allocation or by creating purchase orders.


-   **[Use an agentic workflow to create reclamation rules for enhancing software license utilization tracking and reducing waste](https://www.servicenow.com/docs/access?context=now-assist-sam-create-software-reclamation-rule-workflow&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

Use AI agents to create reclamation rules automatically for installed or subscription-based software, reducing manual analysis of product use and cost. The AI agent analyzes factors such as spend and utilization to suggest reclamation rules.


-   **[Use an agentic workflow to reclaim unused software to minimize compliance risk and optimize savings](https://www.servicenow.com/docs/access?context=now-assist-sam-evaluate-removal-candidate-workflow&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

Use AI agents to automate the reclamation process for installed or subscription-based software. The AI agent evaluates software removal candidates and provides suggestions for reclamation based on intelligent checks that help ensure safe removal.

-   **[Configure ACLs for AI agents and agentic workflows](https://www.servicenow.com/docs/access?context=aia-security-implementation&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Configure the access control lists for who can discover and trigger AI agents and agentic workflows in their guided setups in AI Agent Studio. You can determine whether an AI agent or agentic workflow behaves as a dynamic user or as an AI user. You can also specify if an AI agent or agentic workflow can be available to all authenticated users or publicly available.


</td></tr><tr><td>

Now Assist for Source-to-Pay Operations

</td><td>

-   **[Now Assist for FSC Common](https://www.servicenow.com/docs/access?context=now-assist-fsc-common&version=zurich&pubname=zurich-source-to-pay-operations&ft:locale=en-US)**

The Field Extractor skill extracts the invoice number and supplier invoice number from the inquiry case that is generated through different channels \(emails, virtual agent chats, or web content\). The access control lists \(ACLs\) confirm that only authorized agents can activate or configure the skill.

The Supplier summarization skill in Source-to-Pay Operations workspace provides unified view of supplier-related inquiries and pending actions. This feature helps specialists and supplier managers to quickly view a concise summary of supplier-related cases, tasks, and exceptions.

The Inquiry classifier skill auto-populates the subcategory of an invoice inquiry case by analyzing its description and short description in the Accounts Payable Operations.

-   **[Now Assist for Sourcing and Procurement Operations \(SPO\) skills in a Virtual Agent chat](https://www.servicenow.com/docs/access?context=now-assist-spo-va-using&version=zurich&pubname=zurich-source-to-pay-operations&ft:locale=en-US)**

Requesters can leverage contextual generative AI by using Now Assist for SPO in a Virtual Agent chat to complete self-service tasks, such as purchasing products.

-   **[Now Assist for Sourcing and Procurement Operations \(SPO\)](https://www.servicenow.com/docs/access?context=now-assist-spo&version=zurich&pubname=zurich-source-to-pay-operations&ft:locale=en-US)**

Upload quotes from vendors to request a purchase using the Procurement product recommendation AI agent. Now Assist automatically extracts supplier information, item descriptions, quantities, and pricing from uploaded vendor quotes to pre-fill purchase requisition forms, eliminating manual data entry and accelerating request submission.

Long term stable \(LTS\) models are part of Now LLM Service and provide longer model stability windows for regulated industries. These models can integrate with tools to provide governance, monitoring, and compliance controls.

The Help fulfill procurement requests agentic workflow has been renamed to Conversational intake for sourcing and procurement to better reflect its expanded scope and capabilities.

Employees can initiate sourcing and procurement requests conversationally, with the agent automatically applying organizational policies, routing logic, and pre-filling request details for faster completion.

To enhance performance and simplify maintenance, the Conversational intake for sourcing and procurement agentic workflow now includes three core AI agents. The Procurement purchasing plan and Procurement sourcing plan AI agents have been consolidated into a single, unified Procurement product recommendation AI agent.

    -   **Procurement request tracking AI agent**: Finds and summarizes request status details to answer employee inquiries.
    -   **Procurement product recommendation AI agent**: Recommends products based on organizational buying criteria, creates purchasing or sourcing plans, and guides employees through the checkout or request process.
    -   **Procurement inquiry analysis AI agent**: Analyzes employee inquiries to determine next steps, routes tasks to the appropriate agent, provides knowledge-based answers, and manages fallback handling for unsupported requests.
-   **[Now Assist for Supplier Lifecycle Operations \(SLO\)](https://www.servicenow.com/docs/access?context=now-assist-slo&version=zurich&pubname=zurich-source-to-pay-operations&ft:locale=en-US)**

Now Assist for SLO includes the Coordinate supplier onboarding agentic workflow to streamline the supplier onboarding process by automating supplier registration. AI agents automate the supplier onboarding process by validating profile data and banking details, checking for duplicate suppliers, task generation, communication with suppliers, and final approvals, streamlining the entire process for faster time-to-activation.

To make the workflow more dynamic, the Supplier document strategy generator AI agent creates tasks by referring to a KB article which has all the details about the regions and industry related tasks and documents required for onboarding. The KB article is available as a part of demo data, however, the admin can edit and configure this KB article as required.

The following AI agents in the Coordinate supplier onboarding agentic workflow perform the supplier onboarding tasks:

    -   **Supplier data steward AI agent**: Validates supplier data and checks for duplicate records, creates an invitation case for the supplier contact and assigns the necessary supplier tasks. Also, if required, communicates to the supplier about missing information that must be updated.
    -   **Supplier data validator AI agent**: Validates supplier-provided profile information and banking details \(like account name, account ID, and bank name\) in real time.
    -   **Supplier approval AI agent**: Manages approval or rejection of the supplier onboarding.
    -   **Supplier document strategy generator AI agent**: Generates a plan to create tasks after referring to the dedicated KB article which includes all the details about the tasks required for onboarding based on the region and industry.
For more information, see .

-   **[Now Assist for Accounts Payable Operations \(APO\)](https://www.servicenow.com/docs/access?context=now-assist-apo&version=zurich&pubname=zurich-source-to-pay-operations&ft:locale=en-US)**

The Now Assist for APO includes Inquiry resolution provider agent and Recommend invoice owner which resolves invoice inquiries autonomously and recommends business owner for invoices \(Non-PO, Non-PO type credit memo\).

    -   The Inquiry resolution provider AI agent processes high volumes of repetitive invoice inquiries through various channels \(web, email, virtual agent, mobile and manual entry\) to significantly reduce the workload of human agents.
    -   The Recommend invoice owner AI agent identifies the missing business owner through semantic matching or by creating tasks. The Recommend invoice owner agent triggers when a Missing or invalid business owner exception is raised. For more information on the AI agents, see [Using AI agents in Now Assist for Accounts Payable Operations](https://www.servicenow.com/docs/access?context=using-apo-ai-agents&version=zurich&pubname=zurich-source-to-pay-operations&ft:locale=en-US)
-   **[New third-party AI model provider options available for all Now Assist applications](https://www.servicenow.com/docs/access?context=exploring-large-language-models&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Google Gemini and AWS Claude are available for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.


</td></tr><tr><td>

Now Assist for Strategic Portfolio Management \(SPM\)

</td><td>

-   **[Schedule project insights email](https://www.servicenow.com/docs/access?context=email-project-summary-skill-pw&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)**
    -   Schedule project insights email in the Configure project insights modal. The project email is emailed to the project managers and users and continues on the selected schedule that you select until the project is inactive or paused.
    -   Schedule and instantly send the project insights email to your project managers by selecting the **Send preview** button.
    -   Track important updates such as the delayed end dates, the status turning red, or the state updates of your projects and receive project insights email on the schedule that you select.
    -   Select the email frequency that works for you: weekly, bi-weekly or monthly.
    -   Monitor critical elements such as milestones, resources, projects, and project tasks.
    -   Receive proactive, AI-based notifications when project milestones or critical tasks could lead to delays using Monitor project task agent. Use the Enable critical task alerts option from planning page to enable the project task monitor AI agent.
    -   Choose the recipients to whom you want to send the project insights email.
-   **[Identify similar records using Now Assist](https://www.servicenow.com/docs/access?context=identify-similar-demand-records&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)**

Detect similar existing demand records when creating or editing a demand using the identify similar records skill. The skill compares the **Name**, **Description**, and **Business Case** fields for contextual similarity.

-   **[Accelerate target creation with the target generation skill](https://www.servicenow.com/docs/access?context=generate-targets-for-goal&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)**

Generate measurable targets from goals information and optional context with the target generation skill. The skill automatically populates key fields in the target creation form, helping teams define clear, measurable outcomes and create targets quickly.

-   **[Generate acceptance criteria for stories](https://www.servicenow.com/docs/access?context=eap-generate-acceptance-criteria-for-stories&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)**

Generate clear, consistent acceptance criteria for user stories with the acceptance criteria generation skill. By leveraging story context and predefined templates, the skill helps you align with requirements.

-   **[Enhancements to Story generation](https://www.servicenow.com/docs/access?context=generate-stories-from-epics-now-assist-eap&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)**

Use the upgraded agile story generation skill to convert epics into actionable user stories quickly. Powered by an agentic workflow, the skill analyzes epic details to recommend the optimal number of stories, enables adjustments, refines story content, and creates story records.


-   **[Improve efficiency and quality using refine records skill with Now Assist Context Menu](https://www.servicenow.com/docs/access?context=refine-text-with-write-planning-item-skill&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)**

Simplify record creation and updates by using the refine records skill with Now Assist context menu. Improve record quality by enabling AI-assisted text refinement in the text fields of Product idea, Demand, Epic, Projects, Capability, Feature, Stories, Project tasks, Risks, Strategic priorities, Goals, Targets, Initiatives, Feedback, Milestones, and Story forms.


-   **[Configure ACLs for custom roles](https://www.servicenow.com/docs/access?context=aia-security-implementation&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Update the ACLs for custom roles that require access to Now Assist skills.

-   **[Generate and improve Docs content](https://www.servicenow.com/docs/access?context=generate-summarize-and-refine-content-of-docs-with-now-assist-spm&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)**

Help improve your content and productivity with the ability to enter custom prompts directly in the Docs, alongside the Summarize, Elaborate, and Shorten options.

Generate content with Now Assist for SPM directly in your Docs. In addition, summarize existing sections, elaborate where needed, and refine drafts to help improve your productivity.

You can interact with Now Assist directly in your Doc to create content, add context, or improve existing sections.


-   **[New third-party AI model provider options available for Now Assist](https://www.servicenow.com/docs/access?context=ai-model-providers&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Google Gemini 2.0 Flash, Google Gemini 2.5 Pro, and AWS Claude 3.7 Sonnet are available for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI GPT-4.1 and GPT-4.1 mini.


</td></tr><tr><td>

Now Assist for Telecommunications, Media and Technology \(TMT\)

</td><td>

-   **[Address voice quality issues](https://www.servicenow.com/docs/access?context=now-assist-customer-voice&version=zurich&pubname=zurich-telecom-media-technology&ft:locale=en-US)**

Collect customer details about the voice quality issue, open a service ticket with RADCOM \([https://radcom.com/](https://radcom.com/)\), and generate a resolution plan.

-   **[Risk signals and issues summarization](https://www.servicenow.com/docs/access?context=now-assist-tmt-summarize-risk-signals-issues&version=zurich&pubname=zurich-telecom-media-technology&ft:locale=en-US)**

Generate summary details including the record and associated risk solutions and risk occurrences for risk signal and issues records.


-   **[Help remediate bill issues](https://www.servicenow.com/docs/access?context=billissue-remediation-usecase&version=zurich&pubname=zurich-telecom-media-technology&ft:locale=en-US)**

Handle billing inquiry case requests, analyze customer invoices, and recommend better plans based on customer usage patterns.

-   **[Analyze network incidents](https://www.servicenow.com/docs/access?context=network-incident-analysis-usecase&version=zurich&pubname=zurich-telecom-media-technology&ft:locale=en-US)**

Identify historic incidents and determine resolution plans. The AI agent also has the capabilities to identify field values, estimate resolution time, and create actionable tasks.

-   **[Support renewals and expansion](https://www.servicenow.com/docs/access?context=now-assist-tmt-renewal-analyzer&version=zurich&pubname=zurich-telecom-media-technology&ft:locale=en-US)**

Streamline customer success management by automatically assessing account health, value realization, and adoption trends. Deliver timely, data-driven insights that guide renewal planning and play recommendations.

-   **[Trigger risk mitigation touchpoint](https://www.servicenow.com/docs/access?context=now-assist-tmt-touchpoint-meeting-scheduler&version=zurich&pubname=zurich-telecom-media-technology&ft:locale=en-US)**

Enable customer success agents to optimize meeting schedules within the customer success workflow by creating and managing meetings. Create and manage meetings based on key details such as invitees, agenda, meeting type, and scheduling preferences.

-   **[Success summarization](https://www.servicenow.com/docs/access?context=now-assist-tmt-summarize-plays&version=zurich&pubname=zurich-telecom-media-technology&ft:locale=en-US)**

Generate summary details including overview, current status, and open tasks for success initiatives, internal plays, and customer plays. Enhance Zoom meeting summaries by updating key notes, and enabling sentiment tracking.

-   **[Analyze metric data trend](https://www.servicenow.com/docs/access?context=now-assist-tmt-analyze-metric-trend&version=zurich&pubname=zurich-telecom-media-technology&ft:locale=en-US)**

Collect and analyze metric data for engagements, identify patterns, and generate a trend chart.

-   **[Service summary generation](https://www.servicenow.com/docs/access?context=now-assist-tmt-summarize-knowledge-graph&version=zurich&pubname=zurich-telecom-media-technology&ft:locale=en-US)**

Generate a service summary for a product inventory.

-   **[Knowledge graph schema generation](https://www.servicenow.com/docs/access?context=now-assist-tmt-create-knowledge-graph&version=zurich&pubname=zurich-telecom-media-technology&ft:locale=en-US)**

Use the Knowledge Graph \(KG\) to create Knowledge Graph schema.

-   **[Customize a summary card for service summary](https://www.servicenow.com/docs/access?context=customize-uib-builder-service-summary&version=zurich&pubname=zurich-telecom-media-technology&ft:locale=en-US)**

Customize the summary card of the service summary and UI actions according to your needs.

-   **[Register consumers using Agentic AI](https://www.servicenow.com/docs/access?context=now-assist-tmt-register-consumer-users-sb&version=zurich&pubname=zurich-telecom-media-technology&ft:locale=en-US)**

Initiate the consumer registration process using agentic AI to receive step-by-step guidance, including error checks during registration and support for resolving those errors.

-   **[Configure ACLs for AI agents and agentic workflows](https://www.servicenow.com/docs/access?context=aia-security-implementation&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Configure the access control lists for who can discover and trigger AI agents and agentic workflows in their guided setups in AI Agent Studio. You can determine whether an AI agent or agentic workflow behaves as a dynamic user or as an AI user. You can also specify if an AI agent or agentic workflow can be available to all authenticated users or publicly available.


</td></tr><tr><td>

Now Assist for Third-party Risk Management \(TPRM\)

</td><td>

-   **[Now Assist for Third-party Risk Management \(TPRM\)](https://www.servicenow.com/docs/access?context=now-assist-tprm&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)[Generate issue recommendations for TPRM](https://www.servicenow.com/docs/access?context=create-recommendation-tprm-issue&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

If you have the third‑party assessment reviewer role \[sn\_vdr\_risk\_asmt.vendor\_assessment\_reviewer\] and have installed the if you have the third‑party assessment reviewer role \[sn\_vdr\_risk\_asmt.vendor\_assessment\_reviewer\] and have installed the Now Assist for Third-party Risk Management \(TPRM\), you can use generative AI to automatically identify and recommend issues based on assessment responses. The TPRM issue management recommendation skill recommends issues with rationalized summaries. Recommended issues are presented for review and are created as standard TPRM issues only after user confirmation.


-   **[Now Assist for Third-party Risk Management \(TPRM\)](https://www.servicenow.com/docs/access?context=now-assist-tprm&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

If you have the third-party assessor role \[sn\_vdr\_risk\_asmt.vendor\_assessor\] role and have installed the Now Assist for Third-party Risk Management \(TPRM\) for TPRM application, you can use generative AI to automatically summarize complex issue records. The TPRM Issue Summarization skill works across all issue states including New, Analyze, Review, Finalize, and Closed and can help reduce manual review time, improve consistency in issue descriptions and remediation guidance, and accelerate triage and reporting for customers managing high volumes of third-party risk data.

-   **[Some Now Assist skills are turned on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Zurich Patch 4\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.

</td></tr><tr><td>

Now Assist for Vault

</td><td>

-   **[Generate a custom data pattern by using Now Assist for Vault](https://www.servicenow.com/docs/access?context=generate-custom-data-pattern-now-assist-vault&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)**

The generate custom data pattern skill now uses the Now LLM Service as the default provider. You can switch to another provider as needed.


-   **[Using Now Assist for Vault](https://www.servicenow.com/docs/access?context=using-now-assist-vault&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)**

The Now Assist for Vault application generates custom data patterns from text descriptions to streamline your workload, checks role access for an encrypted column to monitor your instance’s encryption access posture, and schedules data discovery jobs to detect sensitive data. Enable these skills in Now Assist Admin console:

    -   Generate custom data pattern
    -   Check role access for encrypted column
    -   Schedule Data Discovery job

</td></tr><tr><td>

Now Assist for Vulnerability Response

</td><td>

-   **[Retrieve Vulnerability Response data](https://www.servicenow.com/docs/access?context=retrieve-vr-data&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

Chat with an AI agent using natural language to retrieve host \(Vulnerability Response\) and Application Vulnerability Response \(AVR\) data in the Unified Security Exposure Management \(USEM\) and legacy Vulnerability Response workspaces.


-   **[Role configuration required for agentic workflows and AI agents](https://www.servicenow.com/docs/access?context=aia-role-masking&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Agentic workflows and AI agents included with Now Assist applications require additional security configuration. If you select **Users with selected roles** for your user access security controls for an agentic workflow or AI agent, you must add the installed roles, or they won't execute. Data access settings must also include these roles. See the documentation for the agentic workflow or AI agent for the specific roles you must add. After the roles are configured, users must have the specified role to invoke the agentic workflow or AI agent.

-   **[Create a custom API service graph connector in the Security Posture Control \(SPC\) workspace](https://www.servicenow.com/docs/access?context=spc-creating-sgc-template&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

Use generative AI to help your developers create SPC API connectors quickly with the Connector builder framework module in the SPC workspace. With a Now Assist skill that is included with the Now Assist for Vulnerability Response application, your developers have the option to automate steps in the Connector builder framework.

    -   Automate the steps for selecting API templates, populating request and header parameters, and response field mapping.
    -   Use your custom API connector to integrate with security tools and import asset data that is based on the unique requirements of your environment.
    -   Help your cybersecurity teams monitor your overall security posture and identify assets that are missing key security tools with the API connectors that you build.
See [Creating your own API connectors in Security Posture Control](https://www.servicenow.com/docs/access?context=spc-creating-sgc-template&version=zurich&pubname=zurich-security-management&ft:locale=en-US) for more information and the required applications.

-   **[Generate insights to prioritize risks](https://www.servicenow.com/docs/access?context=sem-insights-skill&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

Use generative AI to provide contextual summaries, actionable recommendations, and quick links in the Security Exposure Management Workspace, helping you prioritize critical risks and accelerate remediation.

-   **[Generate recommendation for approval impact analysis](https://www.servicenow.com/docs/access?context=sem-approval-recommendation-skill&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

Use generative AI to provide on-demand recommendations to approve or reject a request directly from the Exception Change Approval record, enabling approvers to make fast, consistent decisions while reducing manual analysis effort.


-   **[Granular roles](https://www.servicenow.com/docs/access?context=now-assist-vr-acticvate-agentic-workflow&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

The sn\_vul\_ai.write\_rem\_insights and sn\_vul\_ai.read\_rem\_insights granular roles have been added and are inherited by the sn\_vul.vulnerability\_admin and sn\_vul.vulnerability\_analyst roles automatically. These roles provide you with more control over read and write access for the records on the Remediation Compliance Insights \[sn\_vul\_ai\_remediation\_insights\] caching table. The VR.System role also inherits these granular roles so background job execution for the workflow can occur.


-   **[Identify duplicate vulnerable items with Now Assist for Vulnerability Response](https://www.servicenow.com/docs/access?context=dedupe-host-vi-now-assist-vulnerability-response&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

Use generative AI to identify duplicates for your active host vulnerable items that are imported by your vulnerability scanners. Use generative AI reasoning with Now Assist to help your analysts differentiate between primary vulnerability items \(VITs\) and those VITs that are duplicates. Close duplicate VITs and move their associated detections automatically to the primary VIT records.

-   **[Identify preferred vulnerability solutions with Now Assist for Vulnerability Response](https://www.servicenow.com/docs/access?context=solutions-now-assist-vulnerability-response&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

Use generative AI to analyze available remediation options pulled from integrated third-party products like Red Hat, Tenable for Vulnerability Response, or internal solution management systems. Evaluate each option against the specific configuration item context, for example, the OS version or software version, and get recommendations for the most viable fix for implementation.


-   **[Using agentic workflows in Now Assist for Vulnerability Response](https://www.servicenow.com/docs/access?context=using-now-assist-ai-agents-vr&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

The assess vulnerability exposure agentic workflow enables vulnerability managers to determine your exposure to vulnerabilities.

    -   Determine your exposure to the most current Cybersecurity and Infrastructure Security Agency \(CISA\) known vulnerabilities in your environment and assess their potential impact to your configuration items \(CIs\) and business services.
    -   Identify assets with Common Vulnerabilities and Exposures \(CVEs\).
    -   Determine the number of active VITs that correspond to CVEs. Create watch topics for VIT remediation.
The analyze vulnerability remediation status agentic workflow helps vulnerability managers to monitor and assess remediation target compliance.

    -   Track Service Level Agreement \(SLA\) compliance - Understand how effectively your organization is meeting remediation goals for vulnerabilities based on your SLAs.
    -   Analyze missed SLAs by severity, assignment group, and configuration item \(CI\) class - Pinpoint gaps in remediation by categorizing overdue VITs based on severity, assignment groups, and CI classes to enable targeted interventions and smarter resource allocation.

</td></tr><tr><td>

Now Assist for Workplace Service Delivery \(WSD\)

</td><td>

[Zurich Patch 7](../quality/zurich-patch-7.md)

-   **[Summarize a workplace case using Now Assist for WSD](https://www.servicenow.com/docs/access?context=summarize-workplace-case&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

Use the case summarization skill to summarize the case context and take appropriate action.


[Zurich Patch 1](../quality/zurich-patch-1.md)

-   **[Optimize cleaning activities agentic workflow](https://www.servicenow.com/docs/access?context=optimize-cleaning-activities-agent&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

Use the optimize cleaning activities agentic workflow to manage cleaning and maintenance schedules of a maintenance case based on the space utilization rate of the location where a maintenance case is created.


</td></tr><tr><td>

Now Assist in AI Search

</td><td>

-   **[Configure disambiguation](https://www.servicenow.com/docs/access?context=nava-configure-disambiguation-manually&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)**

If a search is broad or unclear, Now Assist in AI Search may ask follow-up questions before answering. This disambiguation step helps clarify what the user is looking for and is configurable.


-   **[Automatic activation for Now Assist Multi-Content Response Genius Results](https://www.servicenow.com/docs/access?context=now-assist-multi-content-qna-genius-results&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

When you use Guided Setup to activate the Now Assist panel, Now Assist Multi-Content Response Genius Results are automatically activated for relevant search profiles.

-   **[Hybrid search](https://www.servicenow.com/docs/access?context=hybrid-search-ais&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

Hybrid search blends keyword search and semantic vector search to offer a blend of superior search recall and contextual relevance for knowledge article, Catalog Item, external content, and topic retrieval searches.

-   **[Configure AI Search as the source for Ask Now Assist suggestions](https://www.servicenow.com/docs/access?context=configure-ai-search-source-ask-now-assist-suggestions&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

Admins can configure the system to use AI Search as the source for Ask Now Assist suggestions, enabling suggestion term highlighting and more flexible search operators in enhanced chat.


-   **[New third-party AI model provider options available for all Now Assist applications](https://www.servicenow.com/docs/access?context=exploring-large-language-models&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Google Gemini and AWS Claude are available for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.


</td></tr><tr><td>

Now Assist in Contract Management

</td><td>

-   **[Feedback for Now Assist contract analysis](https://www.servicenow.com/docs/access?context=cmpro-review-contract-document&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

Provide feedback on AI-identified non-standard and missing clauses to help improve AI accuracy over time. When reviewing contracts using Now Assist contract analysis, you can indicate whether the AI suggestions were helpful or not helpful by using the thumbs up or thumbs down feedback options. You can also provide optional qualitative feedback with comments. The feedback option is available in both the workspace and Microsoft Word add-in.

The feedback provided on each clause is captured in the **Contracts Gen AI Feedback** table.

-   **[Automatically navigate to non-standard clauses in Microsoft Word add-in](https://www.servicenow.com/docs/access?context=cmpro-review-contract-document&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

Locate non-standard clauses easily in Microsoft Word. The document scrolls to the relevant section using AI citations when you select a Now Assist suggestion in the Microsoft Word add-in.


-   **[Automated obligation extraction](https://www.servicenow.com/docs/access?context=cmpro-na-reminder-agentic-wf&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US#section_tgm_mt3_dhc)**

Use the manage contract repository agentic workflow to automatically identify and capture key contractual obligations from signed contracts and create obligation records in the contract repository. The AI agent in the manage contract repository agentic workflow uses the Now Assist Contract obligation extraction skill to extract key contractual obligations from contracts.

-   **[Using contract playbook to review AI-extracted obligations](https://www.servicenow.com/docs/access?context=cmpro-na-review-obligations&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

Review extracted obligations in the contract playbook, with options to edit, approve, or reject each obligation. Approved obligations are added as obligation records in the contract repository while rejected obligations are deactivated.

-   **[Contract obligation extraction skill in Now Assist in Contract Management](https://www.servicenow.com/docs/access?context=cncore-conf-obligation-extraction&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

Configure and map use cases for obligation extraction skill in the Now Assist Admin console to automatically extract key contractual obligations from signed contracts. The AI agent in the manage contract repository agentic workflow uses the Now Assist Contract obligation extraction skill to extract key contractual obligations from contracts.

-   **[Conversational contract search and insights Workflow](https://www.servicenow.com/docs/access?context=cmpro-agentic-use-conv-search&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

Contract documents are often complex and stored across multiple formats and repositories, making keyword-based search inefficient and error-prone. The new Now Assist powered conversational search feature enables you to search contract documents using natural language and dialogue-driven queries.

The conversational search feature does not support searching within contract documents that are scanned PDFs.

-   **[Some Now Assist skills are turned on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Zurich Patch 4\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.
-   **[Now LLM LTS support for Contract Management Pro](https://www.servicenow.com/docs/access?context=now-llm-model-updates&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Long term stable \(LTS\) models are part of Now LLM Service and provide longer model stability windows for regulated industries. These models can integrate with tools to provide governance, monitoring, and compliance controls.


-   **[Using contract playbook to review AI-extracted metadata and contract reminder date](https://www.servicenow.com/docs/access?context=cmpro-na-review-ai&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

Use the playbook within a contract repository record to review the metadata extracted by the AI agents in the manage contract repository agentic workflow. You can make necessary changes to the extracted information, and submit it to update the contract repository. If the contract end date is available, the **Review contract reminders** tab appears in the playbook, enabling you to review and update the AI-calculated contract reminder date and specify recipients for contract renewal or terminations.

-   **[New third-party AI model provider options available for all Now Assist applications](https://www.servicenow.com/docs/access?context=exploring-large-language-models&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Google Gemini and AWS Claude are available for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.

-   **[Select large language models for use cases in Now Assist in Contract Management](https://www.servicenow.com/docs/access?context=cmpro-na-manage-llm&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

Select a large language model \(LLM\) provider for a contract analysis or metadata extraction use case. The selected LLM is applicable only for the specific use case and overrides the LLM selected for Now Assist in Contract Management skills.


</td></tr><tr><td>

Now Assist in Document Intelligence

</td><td>

-   **[Document and visual insights AI agent enhancements](https://www.servicenow.com/docs/access?context=document-and-visual-insights-ai-agent&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

The document and visual insights AI agent can recognize and provide citations for multiple attachments.


-   **[Open document in a new tab](https://www.servicenow.com/docs/access?context=set-up-use-case-for-now-assist-document-intelligence&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

View a test document in a larger workspace on a separate browser tab during use case setup.

-   **[Image captioning in Knowledge Center](https://www.servicenow.com/docs/access?context=knowledge-center&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)**

Extract information from images to support accessibility captioning in knowledge base articles.

-   **[Document and visual insights AI agent enhancements](https://www.servicenow.com/docs/access?context=document-and-visual-insights-ai-agent&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Leverage features that enable you to use the document and visual insights AI agent with selected LLMs to upload files, extract information without a predefined use case, and display results in a dedicated document view.

    -   Select an LLM for the AI agent to use when processing documents and images.
    -   Now LLM Service is not an available option for LLM selection.
    -   Prompt the AI agent to upload a file to process.
    -   View the results of the AI agent actions in a document view screen.

-   **[Document Intelligence for Now Assist Skill Kit](https://www.servicenow.com/docs/access?context=add-document-intelligence&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Use document and visual intelligence to leverage extraction, question answering, and summarization capabilities for a skill created with Now Assist Skill Kit.

-   **[Language model selection](https://www.servicenow.com/docs/access?context=languages-supported-now-assist-document-intelligence&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Select the language for a use case to help the optical character recognition \(OCR\) model to detect text in the document and image files.

-   **[Image mode selection for use cases](https://www.servicenow.com/docs/access?context=set-up-use-case-for-now-assist-document-intelligence&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Turn on image mode to process images more efficiently for use cases that use a multimodal AI model.

-   **[Model provider flexibility at the use case level](https://www.servicenow.com/docs/access?context=llms-now-assist-document-intelligence&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Choose a model provider at the use case level, including a Now Assist default option that uses the instance-level model selected in AI Control Tower.

-   **[Information extraction for Operational Sustainability Risk Management](https://www.servicenow.com/docs/access?context=filter-citations-and-authority-documents-for-esg&version=zurich&pubname=zurich-environmental-social-governance&ft:locale=en-US)**

Extract ESG-related information from invoices to support Operational Sustainability Risk Management initiatives and regulatory compliance.

-   **[Improved security for the document and visual insights AI agent](https://www.servicenow.com/docs/access?context=aia-security-implementation&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Enable access control lists \(ACLs\) to improve the security for the document and visual insights AI agent. ACLs provide you with the capability to run AI agents and agentic workflow executions either as a dynamic user or an AI user.

The document and visual insights AI agent and its skills are classified as a worker or helper agent. A worker can act as an AI user with different privileges than the human user. A helper only has the privileges of a human user.


-   **[New third-party AI model provider options available for all Now Assist applications](https://www.servicenow.com/docs/access?context=exploring-large-language-models&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Google Gemini and AWS Claude are available for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.


</td></tr><tr><td>

Now Assist in Platform Analytics

</td><td>

-   **[Gather insights, plan, and collaborate in the AI Data Explorer](https://www.servicenow.com/docs/access?context=now-assist-explorer&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US) \(December 2025\)**

Ask quick questions, receive tailored recommendations, and collaborate with AI and your colleagues to build long-term analysis. Enable teams to discuss and act on findings instantly. Centralize insights and narratives for better decision making. Guide users with contextual insights and suggestions.

Main features include:

    -   [Extended analysis](https://www.servicenow.com/docs/access?context=hidden-insights&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US) generates a deeper level of analysis that can reveal new insights, enabling you to make more informed decisions.
    -   [Add a data visualization from an exploration to a dashboard](https://www.servicenow.com/docs/access?context=add-data-viz-from-expl-to-dboard&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US)
    -   [Share explorations with tagged users](https://www.servicenow.com/docs/access?context=share-now-assist-explorer&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US)
    -   [Duplicate an exploration](https://www.servicenow.com/docs/access?context=nowass-expl-duplicate-exploration&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US)
    -   [Duplicate an answer in an exploration](https://www.servicenow.com/docs/access?context=nowass-expl-dup-del-question-resp&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US)
    -   [Summarize an exploration](https://www.servicenow.com/docs/access?context=summarize-exploration&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US)
AI Data Explorer leverages Query Generation to translate natural language questions into actionable insights. Query Generation enables users of AI Data Explorer to analyze their data and access a broader range of data sets. Key capabilities include:

    -   [Ability to add tables to the semantic data layer](https://www.servicenow.com/docs/access?context=add-table-semantic-layer&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US)
    -   [Multi-table source support](https://www.servicenow.com/docs/access?context=ask-expl-questions&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US)
    -   [Workflow Data Fabric table support](https://www.servicenow.com/docs/access?context=create-integrations-applications&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US)
    -   [Database view support](https://www.servicenow.com/docs/access?context=add-table-semantic-layer&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US)

</td></tr><tr><td>

Now Assist in Virtual Agent

</td><td>

-   **[Clarifying questions for unclear requests](https://www.servicenow.com/docs/access?context=nava-enhanced-chat&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)**

Get precise, relevant answers from Now Assist in Virtual Agent premium chat even when your request is unclear, as the assistant asks you a targeted clarifying question before responding instead of returning an overwhelming list of results. When the assistant is confident it understands your request, it responds immediately without interrupting the conversation.

-   **[Upload documents](https://www.servicenow.com/docs/access?context=nava-enhanced-chat&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)**

Upload documents directly into a Now Assist in Virtual Agent conversation during topic, skill, catalog, or agent execution, and let the assistant extract information from them to automatically fill in required fields, answer questions, and keep the conversation moving. Uploaded document context is retained for the duration of the session and cleared when the session ends to protect your data.

-   **[Configuring assistants overview](https://www.servicenow.com/docs/access?context=configure-now-assist-va&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)**

For new and upgrading customers, Now Assist panel - Platform assistant comes with the option to opt into premium chat if your instance meets certain criteria. For more information, see [Premium chat](https://www.servicenow.com/docs/access?context=now-assist-panel-premium&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US) and .

-   **[Display your assistant on Platform or ServiceNow Studio](https://www.servicenow.com/docs/access?context=display-nap-assistant&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)**

If you're a new or upgrading customer and you have opted into the premium chat experience, legacy messages \(formerly chat messages\) and legacy fallbacks \(formerly chat fallbacks\) settings aren't automatically migrated. You must review, configure, and customize them in premium messages and premium fallbacks.

**Note:** ServiceNow performs a set of readiness checks to confirm that your instance is eligible for premium chat. If your instance doesn’t meet the requirements, you can continue using your existing standard or enhanced chat experience. After an upgrade, there may be a delay before premium chat is available to choose from.

-   **[Brand an assistant](https://www.servicenow.com/docs/access?context=brand-assistant&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)**

Brand your Now Assist panel – Platform assistant's chat header and chat logo, if you have premium chat set up.

-   **[Manage an assistant chat experience](https://www.servicenow.com/docs/access?context=manage-assistant-chat-experience&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)**

Now Assist panel – Platform assistant has premium messages and premium fallback capabilities.

**Note:** For premium fallbacks, web search fallback is dependent on your web search mode setting in [Enable additional chat features](https://www.servicenow.com/docs/access?context=additional-chat-features&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US). If web search mode is turned off, web search fallback is unavailable \(grayed out\). If web search mode is turned on, web search fallback is available where you can turn it on or off.

Feedback surveys are supported in both standard chat and enhanced chat experiences. When enhanced chat is enabled, the survey is automatically triggered when the user indicates that they are finished chatting, based on the assistant’s survey configuration.

-   **[Edit a chat assistant](https://www.servicenow.com/docs/access?context=edit-assistant&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)**

Edit an assistant to turn response feedback on or off. For more information, see [Manage response feedback](https://www.servicenow.com/docs/access?context=manage-sentiment-survey&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US).

-   **[Now Assist in Virtual Agent system properties](https://www.servicenow.com/docs/access?context=nava-sys-props&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)**

Turn premium chat on or off for Now Assist panel – Platform assistant using the **sn\_nowassist\_va.enable\_nap\_aix\_experience** system property. The default value is set to `false`. When the system property is set to `false`, you can switch back to your previous state \(standard chat or enhanced chat\) from the Assistant Designer chat experience modal. When the system property is set to `true`, you won't have the option to make edits to the chat experience. Premium chat is only available if your instance meets all requirements.


-   **[Start NAVA conversations from anywhere](https://www.servicenow.com/docs/access?context=nava-enhanced-chat&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)**

Start a Now Assist in Virtual Agent premium chat from any page in the Employee Hub with a single click, without interrupting existing workflows. You can upload files, toggle web search on or off, and receive a personalized greeting with promoted topics when opening a new conversation.

-   **[Response feedback](https://www.servicenow.com/docs/access?context=nava-enhanced-chat&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)**

Provide more detailed feedback on Now Assist in Virtual Agent responses by selecting thumbs up or thumbs down, then choosing from configurable checkbox options or adding your own comments to explain exactly what was helpful or what fell short. Your feedback is captured and made available through analytics dashboards, helping admins continuously improve the quality of responses you receive.

-   **[Use natural-language questions](https://www.servicenow.com/docs/access?context=nava-enhanced-chat&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)**

Enable users to ask natural-language questions and receive concise, synthesized answers while maintaining transparency, trust, and efficient task completion.

-   **[New building block framework](https://www.servicenow.com/docs/access?context=nava-enhanced-chat&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)**

Provide a consistent, reusable building block framework for the NextWave web experience using primitives and widgets.

-   **[New Include Web results button](https://www.servicenow.com/docs/access?context=nava-enhanced-chat&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)**

Enable a web search experience that includes a "Include Web results" button in the input box that includes internal and external web results.

-   **[Test voice agents](https://www.servicenow.com/docs/access?context=nava-enhanced-chat&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)**

Test voice agents directly in Assistant Designer with live transcription, tool execution tracking, and conversation logs.

-   **[Dutch and Thai language support](https://www.servicenow.com/docs/access?context=nava-enhanced-chat&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)**

Dutch and Thai language support for voice assistants enables users to experience natural pronunciation and culturally appropriate interactions with AI voice agents.


-   **[Assistant Designer](https://www.servicenow.com/docs/access?context=assistant-designer&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)**

Create and manage LLM-based chat and voice assistants within Assistant Designer, a centralized assistant administrator experience. Assistant Designer is comprised of three main areas: Assistants, Asset library, and Analytics.

[Configuring assistants overview](https://www.servicenow.com/docs/access?context=configure-now-assist-va&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)

    -   Access the **Assistants** tab within [Assistant Designer](https://www.servicenow.com/docs/access?context=assistant-designer&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US) by navigating to **All** &gt; **Assistant Designer**. The **Assistants** tab is only available for customers who have the Now Assist license. NLU-only customers don't have access to [Assistant Designer](https://www.servicenow.com/docs/access?context=assistant-designer&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US).
[View assistants](https://www.servicenow.com/docs/access?context=view-assistants&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)

    -   View chat and voice assistants within the **Assistants** tab of [Assistant Designer](https://www.servicenow.com/docs/access?context=assistant-designer&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US).
        -   The card view is the default view for the assistants.
        -   An inactive \(gray\) or active \(green\) label is shown for each assistant.
        -   Activate, deactivate, test, edit, or delete an assistant.
        -   A display experience label is shown on each chat assistant card.
        -   A domain label is shown on assistant cards if an assistant is created outside of the global domain. If assistants are only created within the global domain, the label isn’t shown.
        -   The ability to view or edit an assistant depends on the domain that the admin has access to.
        -   The name and date are shown for when the assistant was last updated.
        -   Voice assistants show a voice icon and label on the card. Voice assistants can't be tested within Assistant Designer.
        -   The map view shows the assistant hierarchy where you can open, turn on or off, or delete an assistant.
    -   View the side panel for quick access to **Pick up where you left off**, **Recent activity**, and **Resources**.
[Create a voice assistant](https://www.servicenow.com/docs/access?context=configure-voice-assistants&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)

    -   Start creating an AI voice assistant by providing a name and description. Tag to a business unit to analyze your voice assistant.
    -   Power your voice assistant with agentic experience by adding AI agents.
    -   Personalize your voice assistant by choosing a language, adding a welcome message, and an AI voice persona.

**Note:** The supported languages are:

        -   English
        -   German
        -   Spanish
    -   Secure the voice interactions by setting up caller authentication methods and safeguards.
[Create a chat assistant](https://www.servicenow.com/docs/access?context=create-assistant&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)

    -   Add basic details such as a name and description for your chat assistant, and set your assistant as a primary assistant. The Basic details page within the UI has replaced the Overview page.
    -   Now Assist panel – Platform \(default\) assistant can be set as a primary assistant and linked to secondary assistants. Now Assist panel – Developer assistant doesn't have this option.
    -   The name and description of the Now Assist panel assistants can't be changed.
[Use agentic support for a chat assistant](https://www.servicenow.com/docs/access?context=use-agentic-support&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)

    -   Let the assistant use AI agent skills and agentic orchestration. Admins can choose between agentic or standard \(Q&amp;A\) modes depending on business needs and user experience goals. Turn on or off the **Prioritize AI agents during skills discovery** feature.
[Assign search sources to a chat assistant](https://www.servicenow.com/docs/access?context=add-info-sources-assistant&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)

    -   Restore search sources back to the default \(Now Assist Multi-Turn Catalog Ordering and Now Assist Q&amp;A\).
    -   Now Assist panel - Platform \(default\) assistant now has the option to copy an existing search configuration.
    -   Dynamic global search configuration has been added to the list of search application configurations.
    -   Create or configure additional search sources by selecting the **External Content Connectors** link. This replaces a card view.
    -   Manage knowledge articles by selecting the **Knowledge Center** link.
    -   In edit mode, search sources are found within the Information Sources sub-tab.
[Add a Knowledge Graph schema to a chat assistant](https://www.servicenow.com/docs/access?context=add-kg-schema-assistant&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)

    -   Adding a Knowledge Graph schema has moved from the Information sources page to its own page.
    -   Add a Knowledge Graph schema is now available for the Now Assist panel - Platform \(default\) assistant. For the NLQ schema, if Global Graph or Global Graph Mini is selected, you have the option to select tags for specific workspaces that are active on the instance.
    -   Define the mapping relationship between individual workspaces on the instance and predefined Knowledge Graph tags when Global Schema is selected for NLQ.
    -   In edit mode, Knowledge Graph is found within the Information Sources sub-tab.
[Add assets to a chat assistant](https://www.servicenow.com/docs/access?context=add-assets&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)

    -   By default, all Now Assist skills \(Now Assist Q&amp;A, Now Assist multi-turn catalog ordering, Now Assist topics, subflows and actions, custom skills, and AI agents\) are turned on. Therefore, the Now Assist skills page has been removed.
    -   Map an asset to an assistant. Assets are the building blocks of each assistant, providing them with instructions and functionality for helping users. Assets include topics, subflows and actions, custom skills, and AI agents. For Now Assist panel - Developer assistant, only topics \(asset type\) is available.
    -   In edit mode, assets are found within the Information Sources sub-tab.
[Display your chat assistant on a portal, channel, or mobile app](https://www.servicenow.com/docs/access?context=display-assistant-portal-channel&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)

    -   Leverage Now Assist capabilities in Google chat.
    -   Use **Prominent action button override** to allow a different chat assistant other than the default assistant to be launched on a mobile app.
    -   In edit mode, display experiences are found within the Settings sub-tab.
[Display your assistant on Platform or ServiceNow Studio](https://www.servicenow.com/docs/access?context=display-nap-assistant&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)

    -   The **Add ServiceNow Platform** drop-down menu has replaced the **Add agent experience** drop-down menu. A Now Assist panel assistant can't be added to other display experiences.
    -   In edit mode, display experiences are found within the Settings sub-tab.
[Brand an assistant](https://www.servicenow.com/docs/access?context=brand-assistant&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)

    -   Minor enhancements to the look-and-feel of the standard chat preview pane.
    -   In edit mode, branding is found within the Settings sub-tab.
[Manage an assistant chat experience](https://www.servicenow.com/docs/access?context=manage-assistant-chat-experience&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)

    -   A standard chat preview pane is shown for the default greeting topic \(Now Assist – Greeting\) and the default closing topic \(Now Assist – Closing\). Selecting custom topics won’t show a preview pane.
    -   Fallbacks have a standard chat preview pane and each fallback is shown if toggled on.
    -   For the Now Assist panel - Platform \(default\) assistant, web search, record producer, and custom fallback are available options. End this chat and survey are available for the standard chat experience.
    -   In edit mode, chat experience is found within the Settings sub-tab.
[Enable additional chat features](https://www.servicenow.com/docs/access?context=additional-chat-features&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)

    -   Web search, response streaming, document uploads, and closed chat were moved from the Manage chat experience page to its own page. By default all chat features except web search are turned on.
    -   Response streaming can be turned on at the assistant level regardless of whether Dynamic Translation is turned on or off. However, response streaming doesn't work when Dynamic Translation is being used.
    -   In addition to web search, response streaming, document uploads, and closed chat, Now Assist panel Platform assistant has voice input. Voice input allows users to use a microphone to enter the input.
    -   In edit mode, additional chat features are found within the Settings sub-tab.
[Review chat assistant settings](https://www.servicenow.com/docs/access?context=review-assistant-settings&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)

    -   New sections that have been added include: Agentic support, Knowledge Graphs, Assets, and Chat features.
    -   Testing an assistant has been removed from the Review page.
[Test a chat assistant](https://www.servicenow.com/docs/access?context=test-assistant&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)

    -   Test a chat assistant from **Assistant Designer** &gt; **Assistants** tab or from within each page while in edit mode.
[Edit a chat assistant](https://www.servicenow.com/docs/access?context=edit-assistant&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)

    -   Edit a chat assistant from **Assistant Designer** &gt; **Assistants** tab. You will be directed through an edit flow with a slightly different UI from the create flow.
[Analyzing assistants](https://www.servicenow.com/docs/access?context=ai-engagement-analytics&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)

    -   Monitor, evaluate, and optimize the performance of your AI-powered assistants within the **Analytics** tab of [Assistant Designer](https://www.servicenow.com/docs/access?context=assistant-designer&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US).
-   **[Copy received messages](https://www.servicenow.com/docs/access?context=nava-enhanced-chat&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)**

Use the copy message icon in the feedback panel to copy received Virtual Agent responses.

-   **[New system properties](https://www.servicenow.com/docs/access?context=nava-sys-props&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)**
    -   Set the **com.glide.cs.nass.synthesized\_response.disabled\_popover.hide** to `true` to hide the popover for disabled catalog items for Now Assist in Virtual Agent and Now Assist panel's enhanced chat.
    -   Set the **sn\_ais\_assist.enable\_pi\_in\_nba** property to `true` to allow conversational history-based suggested actions and fill multiple suggested action slot options.
    -   View the **sn\_nowassist\_va.enable\_nass\_show\_all\_options** property to decide whether to allow the **View all options** link in an enhanced chat conversation's greeting topic.
    -   The **com.glide.interactive\_view.enabled** property opens an interactive side panel view next to the chat window. The default value is `true` to activate AI Engagement Experience on your instance.
-   **[View org chart in the interactive view](https://www.servicenow.com/docs/access?context=nava-enhanced-chat&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)**

Select **View org chart** from the people citation's popover in Now Assist panel's enhanced chat or Now Assist in Virtual Agent enhanced chat/enhanced chat's full-page experience. The person's organizational chart appears to the right of the chat conversation in an area known as the interactive view. You can switch between multiple organizational charts via a drop-down in the interactive view if you open multiple people citations' org charts in the same conversation.


-   **[Select continue or move to next task button](https://www.servicenow.com/docs/access?context=nava-standard-chat&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)**

The **Continue to next task** button appears in the new **Ready to move on to your next task** card whenever multiple questions are found in a single standard chat user's message. The **Move on to the next task** citation appears at the end of an enhanced chat's synthesized response whenever multiple questions or requests are found along with an action in the user's single message. Whenever either **Continue to next task** \(standard chat\) or **Move on to the next task** \(enhanced chat\) is selected, the second question or request is reviewed and a synthesized response is sent back regarding the user's second question or request.

-   **[Multiple questions in a single user message are answered consecutively](https://www.servicenow.com/docs/access?context=nava-enhanced-chat&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)**

Virtual Agent can answer multiple questions that were submitted in a single message query. Now Assist panel or Now Assist in Virtual Agent answers the multiple questions consecutively in a response.

-   **[Now Assist in Virtual Agent system properties](https://www.servicenow.com/docs/access?context=nava-sys-props&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)**

Use **sn\_aia.use\_agents\_in\_planner** to configure AI agent discovery behavior. The default value is `true`, preferring AI agents over assets including catalogs, topics, Q&amp;A knowledge base articles, workflows, and sub-workflows. When set to `false`, there’s no preference for AI agents. AI agents and assets are treated the same.

-   **[New defaults for Now LLM Service](https://www.servicenow.com/docs/access?context=exploring-large-language-models&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Now Assist in Virtual Agent and Now Assist panel will use an upgraded Now LLM Service as the default. For more information, see the [Now LLM Service Upgrade FAQ: Everything You Need to Know About the v2.0 Model Transition \[KB2556891\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2556891) article in the Now Support Knowledge Base.


-   **[Configure additional user interface and experience options for enhanced chat](https://www.servicenow.com/docs/access?context=ac-configure-chat-branding&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)**

Customize and configure the Search Toggle Button Label for enhanced chat's full-page experience. Additionally, you can configure the Enable Unread Conversation Count Display and Left Panel Header Label for enhanced chat and enhanced chat's full-page experience.

-   **[New third-party AI model provider options available for Now Assist](https://www.servicenow.com/docs/access?context=exploring-large-language-models&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Google Gemini and AWS Claude are available for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.

-   **[View agentic conversations processing steps](https://www.servicenow.com/docs/access?context=nava-enhanced-chat&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)**

View agentic conversational processing steps and stop the flow, if needed.

-   **[View extended entities and records](https://www.servicenow.com/docs/access?context=using-now-assist-in-va&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)**

View extended entities and records in standard and enhanced chat conversations that come from the additional custom tables associated with the Knowledge Graph Natural Language Query \(NLQ\) schema such as:

    -   Assets
    -   Incidents
    -   Recently viewed knowledge base articles
    -   Requests
    -   Tasks
-   **[View suggested queries in the portal’s search bar and chat window](https://www.servicenow.com/docs/access?context=nava-enhanced-chat&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)**

View the most frequently asked queries in the portal’s search bar and enhanced chat’s Virtual Agent. Any search query entered into the portal’s search bar or Virtual Agent is incorporated into the greeting topic for future conversations as a suggested query. Suggested queries are only included in the Virtual Agent greeting topic whenever no promoted assets are designated.

-   **[Work with suggested queries](https://www.servicenow.com/docs/access?context=nava-sys-props&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)**

Two system properties were added to enable the suggested queries feature: **sn\_nowassist\_va.enable\_suggested\_queries** and **sn\_nowassist\_va.max\_suggested\_queries**.

-   **[Configure AI search answers OneExtend capability for web search](https://www.servicenow.com/docs/access?context=configure-ai-search-answers-capability-for-web-search&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Configure the AI Search answers capability via `sys_one_extend_capability.list` to establish the web search AI provider and work with API keys, if needed.

-   **[Expanding AI provider support for web search](https://www.servicenow.com/docs/access?context=configure-ai-search-answers-capability-for-web-search&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

OpenAI, Perplexity, and Google Gemini support web search.

-   **[Configuring assistants overview](https://www.servicenow.com/docs/access?context=configure-now-assist-va&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)**

Enhancements to Now Assist in Virtual Agent assistants and Now Assist panel Platform and Developer assistants. Options vary for Now Assist panel assistants.

[Create a chat assistant](https://www.servicenow.com/docs/access?context=create-assistant&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)

    -   Configure assistants by domain.
[Display your chat assistant on a portal, channel, or mobile app](https://www.servicenow.com/docs/access?context=display-assistant-portal-channel&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)

    -   Now Assist in Virtual Agent: For mobile search widgets, enable the search bar to open into a full-page experience.
[Display your assistant on Platform or ServiceNow Studio](https://www.servicenow.com/docs/access?context=display-nap-assistant&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)

    -   Now Assist panel Platform assistant: Enable enhanced chat for a conversational experience that includes a dynamic, movable, and re-sizable chat window, plus access to multiple active conversations.
    -   Now Assist panel Developer assistant: Not applicable.
[Assign search sources to a chat assistant](https://www.servicenow.com/docs/access?context=add-info-sources-assistant&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)

    -   Now Assist in Virtual Agent:
        -   Add internal and external search sources, such as catalog items and Microsoft SharePoint, from a drop-down list.
        -   Add a slot filling schema to input user information from your organization's Knowledge Graph. Add a Natural Language Query schema to enable users to perform a data query during a conversation.
    -   Now Assist panel Platform assistant:
        -   Add internal and external search sources, such as catalog items and Microsoft SharePoint, from a drop-down list.
        -   Add a slot filling schema to input user information from your organization's Knowledge Graph. Add a Natural Language Query schema to enable users to perform a data query during a conversation.
    -   Now Assist panel Developer assistant: Not applicable.
[Manage an assistant chat experience](https://www.servicenow.com/docs/access?context=manage-assistant-chat-experience&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)

    -   Now Assist in Virtual Agent:
        -   Select a custom greeting topic, closing topic, error topic, and survey for your assistant.
        -   Select one or more fallback options: live agent, web search, record producer, end this chat, and custom fallback.
        -   Enable the web search fallback option and web search mode to enable users to search the web from within a chat window.
    -   Now Assist panel Platform assistant:
        -   Select a custom greeting topic or error topic for your assistant.
        -   Fallback options don't apply to Now Assist panel Platform assistant.
        -   Enable web search mode to enable users to search the web from within a chat window.
    -   Now Assist panel Developer assistant: Not applicable.
-   **[Now Assist panel](https://www.servicenow.com/docs/access?context=now-assist-panel-overview&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Use the enhanced Now Assist panel for a more intuitive and personalized experience. The updated Now Assist panel is re-sizable and can be moved anywhere on the ServiceNow AI platform.


</td></tr><tr><td>

On-Call Scheduling

</td><td>

-   **[Add custom on-call notification channels](https://www.servicenow.com/docs/access?context=custom-on-call-channel-integration&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

Increase the flexibility in communication by adding and configuring service providers as on-call notification channels. You must configure the communication channel by using the On-call communication channel configuration \[on\_call\_comunication\_channel\_config\] table. After you configure the channel, you can select the new channel. This feature is applicable only after the subflows are configured and used.

-   **[Customize the on-call notification message and keywords](https://www.servicenow.com/docs/access?context=config-oncall-communication-channel&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

Customize an on-call notification message and response keywords that are sent to the user and user groups as per your preferences. You can customize the message and keywords by using the On-call communication channel configuration \[on\_call\_communication\_channel\_config\] tables.

-   **[Send the on-call escalation notifications when the configured record fields are modified](https://www.servicenow.com/docs/access?context=create-trigger-rule-oncall&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

Send the on-call escalation notifications when the configured record fields are modified. On-call trigger rules have the following enhancements:

    -   Configure the changes to fields as a triggering condition to run trigger rules. For example, changes to the **Priority** field for an incident can be configured as a trigger condition.
    -   Configure the group or team level trigger rules, or you can configure the global trigger rules that aren’t associated with a user group.
    -   If the assignment group is auto-populated when an incident is created, you can still configure the on-call trigger rules to run and send the escalation notifications.

</td></tr><tr><td>

Operational Resilience

</td><td>

-   **[Use the interactive Node Map visualization](https://www.servicenow.com/docs/access?context=configure-nexus-map-configurations&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

Navigate operational dependencies using the interactive Node map visualization. Configure node and edge settings in the Nexus map, then display Main node configurations directly within the Operational Resilience Workspace. The **Resilience map** action provides access to relationships for Business Services \(BS\), Application Services \(AS\), Supporting Offerings \(SO\), Business Processes \(BP\), and Dependencies modules in the map view.

You can configure node dependency directions and enhance visual elements with improved colors and icons for clarity. Additionally, you can gain comprehensive insights from the summary panel and address missing 'red flags' for a complete picture.

-   **[Generate Word reports of action tasks](https://www.servicenow.com/docs/access?context=gen-word-reports&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

Use the Document designer to set up Microsoft Word templates and download action task reports in Digital resilience incident reporting. This functionality enables you to customize predefined templates or create templates, incorporating specific data like tables and columns from records, to generate intuitive, audit-ready reports. You can then save these reports within the ServiceNow® instance or as cloud documents in Microsoft SharePoint.

-   **[Report incidents associated with multiple regulations for various legal entities](https://www.servicenow.com/docs/access?context=reporting-for-multiple-regulations&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

Report incidents or security incidents associated with multiple regulations for various legal entities in Digital resilience incident reporting. Its automated workflow generates regulatory reporting assessment of IT incidents, DRI Initial report, DRI Intermediate report, and DRI Final report within regulatory timelines, each with dedicated action tasks. You can complete these tasks and generate reports in Microsoft Word format required by regulatory authorities for analysis.

-   **[Generate Register of Information \(RoI\) regulatory packages](https://www.servicenow.com/docs/access?context=opres-dora-roi-reg-pkg&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

Generate regulator-ready Register of Information \(RoI\) regulatory packages using the Plain-CSV Report Package option on the download page in Digital resilience third-party registers. The resulting ZIP file, structured to regulator specifications, includes metadata and report folders with file names containing LEI, entity ID, and release version.

This format helps you to verify EU DORA compliance and supports automated validation workflows. For suggested steps and permissions, refer to the user guide on the Download and Upload request page.

-   **[Validate downloaded Register of Information regulatory packages](https://www.servicenow.com/docs/access?context=opres-dora-validate-roi&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

Validate downloaded Register of Information \(RoI\) regulatory packages against requirements using the Plain-CSV Report Package option on the Digital resilience third-party registers download page. This process verifies file format, structure, encoding, naming conventions, and field-level data across multiple tables.

If validation warnings are detected, an automated report is attached, mapping issues to regulator fields like Template Code, Row Code, and Column Code. These reports include real-world field labels, rule expressions, and record identifiers. You can easily cross-reference validation errors using a downloadable Excel template that mirrors the CSV structure, simplifying issue location and resolution. Further enhancements include support for 'Not applicable' values, enforced file size limits, and clearer error messages for malformed data.

-   **[Improve resilience metrics with the enhanced CSDM model](https://www.servicenow.com/docs/access?context=using-csdm-v5&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

Leverage the enhanced fix scripts in the Common Service Data Model \(CSDM\) to enhance your Operational Resilience metrics. Each node in the hierarchy is now stored separately, with its class and parent nodes, to help you manage your data more efficiently.

The **Update CSDM and other dependencies** scheduled job script has been optimized to process the main node configurations in parallel, triggering a separate event for each node. Any node can be at the top level. Additionally, you can store impacted objects, including all parents, in a single table, so that you can efficiently retrieve children nodes and improve your data retrieval.

Configure the **sn\_oper\_res.top\_class\_name** property to designate any class as the top class. You can view the downstream data and various dashboards based on the selected top class, such as the number of application services that are under a business service.

-   **[Analyze importance and impact tolerance of a service using Smart Assessment](https://www.servicenow.com/docs/access?context=create-an-assessment-for-services-in-ws&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

Analyze a service's importance and impact tolerance through flexible assessments by using one or multiple Smart Assessment templates. Role-based access controls and auto-assigned tasks help you to streamline the process. You can reopen and complete assessments as needed and send email notifications to relevant users.

-   **[Generate customized and flexible self-attestation reports using Smart Assessment](https://www.servicenow.com/docs/access?context=create-new-attestation-in-ws&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

Generate customized and flexible self-attestation reports by using Smart Assessment. Start with the default template, add relevant scopes and users, and generate a PDF report on completion of the self-attestation process. By creating custom templates with various data types, you make the self-attestation process more efficient.

-   **[Leverage enhanced DORA capabilities for contracts, supply chains, and assessments](https://www.servicenow.com/docs/access?context=create-drtp-reg-contract&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

Use the enhanced Digital Operational Resilience Act \(DORA\) data model in Operational Resilience. You can configure contracts based on their supply chains and assessments, upload the contract records, and generate a detailed report in Microsoft Excel that provides information on the entities, third parties, and specific contract details.

-   **[Track third-party risk assessments](https://www.servicenow.com/docs/access?context=opres-ws-homepage-overview&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

Track third-party risk assessments as red flags in Operational Resilience reports and overview pages for business services, service offerings, and business processes. Operational Resilience users, managers, and administrators can review these assessments in Operational Resilience Workspace. The sn\_vdr\_risk\_asmt.vendor\_assessment\_reviewer role is now included in the sn\_oper\_res.user role, so that you can grant the necessary access to the assessments.


</td></tr><tr><td>

Operational Sustainability Management

</td><td>

-   **[Support estimation when actual data isn’t available](https://www.servicenow.com/docs/access?context=provide-data-for-metric-data-task&version=zurich&pubname=zurich-environmental-social-governance&ft:locale=en-US)**

Enable organizations to provide estimated data when actual data is unavailable. Use standardized or personalized custom methods to confirm accurate and reliable ESG reporting.

-   **[Approve automated metric definitions](https://www.servicenow.com/docs/access?context=provide-data-for-metric-data-task&version=zurich&pubname=zurich-environmental-social-governance&ft:locale=en-US)**

Configured a new approval stage for automated metric definitions, confirming that collected data undergoes review before being added to relevant tables. This improves data accuracy and governance for automated metric definitions.

-   **[DEX integration with Sustainable IT Dashboard](https://www.servicenow.com/docs/access?context=sustainable-it-dashboard&version=zurich&pubname=zurich-environmental-social-governance&ft:locale=en-US)**

Real-time energy consumption data from DEX is now integrated into the ESG Sustainable IT Dashboard. This enhances sustainability reporting for IT assets, providing real-time usage trends, total energy consumption, and detailed regional and model insights, thereby supporting more accurate and actionable ESG initiatives.

-   **[Claims for reporting](https://www.servicenow.com/docs/access?context=claims-for-reporting&version=zurich&pubname=zurich-environmental-social-governance&ft:locale=en-US)**

Track and reuse narratives or statements for disclosures and reports. Claims play a crucial role in disclosures, highlighting key achievements and commitments while confirming actionable and credible reporting. This enhances the efficiency, consistency, and credibility of your sustainability disclosures.

-   **[Provide responses for multiple metrics](https://www.servicenow.com/docs/access?context=provide-data-for-multiple-metrics&version=zurich&pubname=zurich-environmental-social-governance&ft:locale=en-US)**

This release brings multiple improvements that aim to improve the overall functionality and usability of the Operational Sustainability Management:

    -   Enhanced Metric data task filtering by approval level.
    -   Various bug fixes and UI enhancements for a better user experience.
-   **[Monitoring assessment data using ESG Management dashboards](https://www.servicenow.com/docs/access?context=monitor-data-using-esg-dashboards&version=zurich&pubname=zurich-environmental-social-governance&ft:locale=en-US)**

Introduction of Platform Analytics view in ESG Management for creating dashboards and reports.

-   **[Creating claims from O365](https://www.servicenow.com/docs/access?context=create-a-claim-from-microsoft-word&version=zurich&pubname=zurich-environmental-social-governance&ft:locale=en-US)**

Enhanced the Microsoft 365 plugin to enable creating and submitting claims directly from Microsoft Word to ServiceNow, streamlining the claims process.

-   **[Emission factor enhancements](https://www.servicenow.com/docs/access?context=usage-of-emission-factors-in-a-calculated-metric-definition&version=zurich&pubname=zurich-environmental-social-governance&ft:locale=en-US)**

Updated calculated metric definition calculation logic to automatically recalculate data when emission factor values change, using the new values for dates within the validity period. This confirms that the metrics data is consistent and accurate.

-   **[Forecast planning](https://www.servicenow.com/docs/access?context=scenario-analysis-forecast&version=zurich&pubname=zurich-environmental-social-governance&ft:locale=en-US)**

The forecast planning now includes support for both manual and automated metric definitions and metrics, in addition to calculated metric definitions. This enhancement enables for more flexible and accurate forecasting across a wider range of metrics. You can adjust values either as absolute amounts or as percentages, making it easier to model various scenarios and anticipate future trends.

-   **[Entity based assess](https://www.servicenow.com/docs/access?context=entity-based-access&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

Entity-based access aims to provide a more granular approach to data access, confirming that users can only access data through entity-based access.

    -   The entity-based access has been enabled for metrics, metric data tasks, metric data, metric data by entity and metric threshold.
    -   Administrators can grant access to an entity's related records by adding users or user groups, or by using entity user fields for entity-based access configuration.
-   **[Upload a disclosure document](https://www.servicenow.com/docs/access?context=upload-a-disclosure-document&version=zurich&pubname=zurich-environmental-social-governance&ft:locale=en-US)**

Claims Disclosure enables you to create and link claims directly from Word documents using the ServiceNow add-in. Once uploaded, claims are automatically synced and created in to the relevant disclosures, confirming traceability and simplifying ESG reporting.

-   **[Set default values for CMD formula operands](https://www.servicenow.com/docs/access?context=activate-default-values-for-cmd-calculations&version=zurich&pubname=zurich-environmental-social-governance&ft:locale=en-US)**

Default values for operands in CMD formulas can now be defined in the Calculated Metric Definition Settings table. When an operand value is missing during formula execution, the system automatically retrieves and applies the specified default value, confirming uninterrupted calculations. Default values can be customized or new records added to meet specific calculation requirements.

-   **[Update metric definition](https://www.servicenow.com/docs/access?context=update-automated-metric-definition&version=zurich&pubname=zurich-environmental-social-governance&ft:locale=en-US)**

When renaming a metric definition, an option is available to apply the change to associated child metrics. Selected child metric names are updated, and their related metric data tasks automatically reflect the new name, confirming consistency across all linked elements.

-   **[Components installed with Operational Sustainability Management \(formerly ESG Management\)](https://www.servicenow.com/docs/access?context=components-installed-with-esg&version=zurich&pubname=zurich-environmental-social-governance&ft:locale=en-US)**

Updated ESG Management roles to update compliance feature roles. The following roles are updated:

    -   sn\_esg.data\_owner
    -   sn\_esg.program\_manager
    -   sn\_grc\_metric.admin
    -   sn\_grc\_metric.manager
    -   sn\_grc\_metric.user
-   **[ESG content accelerator](https://www.servicenow.com/docs/access?context=esg-content-accelerator&version=zurich&pubname=zurich-environmental-social-governance&ft:locale=en-US)**

The Unified Content Accelerator has been renamed to Unified Content Management. Its user interface has been redesigned for improved usability and intuitive workflows, while retaining core functionality.

-   **[Emission factor library](https://www.servicenow.com/docs/access?context=emission-factor-library&version=zurich&pubname=zurich-environmental-social-governance&ft:locale=en-US)**

Audit tracking is now enabled by default on Emission Factor tables, confirming that every modification is automatically recorded in a secure audit log. You can review detailed entries, including the user who initiated the change, the timestamp, the type of update, and the modified data values.

-   **[General guidelines for formula building](https://www.servicenow.com/docs/access?context=Formula-building-general-guidelines&version=zurich&pubname=zurich-environmental-social-governance&ft:locale=en-US)**

You can now select any emission factor when creating a calculated metric definition \(CMD\), regardless of unit type. This update removes that constraint, enabling broader formula combinations and supporting sustainability scenarios where unit alignment isn’t required for calculations.


</td></tr><tr><td>

Operational Technology \(OT\) Manager Foundation

</td><td>

-   **[Search for related records in an OT CMDB table](https://www.servicenow.com/docs/access?context=search-related-records-ot-cmdb-tables-now-assist-otm&version=zurich&pubname=zurich-operational-technology&ft:locale=en-US)**

Use the OT CMDB search function to find an OT configuration item \(CI\) and OT device information in an OT CMDB table.

-   **[Upload, validate, and import your OT device inventory spreadsheet using the Import OT device spreadsheet into OT CMDB agentic workflow](https://www.servicenow.com/docs/access?context=upload-import-validate-ot-device-inventory-spreadsheet&version=zurich&pubname=zurich-operational-technology&ft:locale=en-US)**

Use the Import OT device spreadsheet into OT CMDB agentic workflow to begin the process for uploading, validating, and importing your OT device inventory into ServiceNow.


</td></tr><tr><td>

Operational Technology Incident Management

</td><td>

-   **[Use the Employee Center for OT to report an OT incident](https://www.servicenow.com/docs/access?context=report-ot-incident-in-ot-employee-portal&version=zurich&pubname=zurich-operational-technology&ft:locale=en-US)**

Create an OT incident as a user without an OT incident role with the Report OT incident item in the Employee Center for OT.


</td></tr><tr><td>

Operational Technology Manager

</td><td>

-   **[Operational Technology Network Map](https://www.servicenow.com/docs/access?context=utilizing-ot-network-map&version=zurich&pubname=zurich-operational-technology&ft:locale=en-US)**

Use the OT network map available in the Industrial Workspace to view a site's subnets and the OT devices in each subnet.

-   **[About the Industrial Workspace page](https://www.servicenow.com/docs/access?context=view-installed-ot-applications&version=zurich&pubname=zurich-operational-technology&ft:locale=en-US)**

Use the About Industrial Workspace page on the ServiceNow AI Platform to view the OT applications and the versions that you have installed on your instance.

-   **[Search for a record in the Industrial Workspace](https://www.servicenow.com/docs/access?context=search-in-industrial-workspace&version=zurich&pubname=zurich-operational-technology&ft:locale=en-US)**

Search for CMDB tables in the Industrial Workspace to find CMDB related records. The search function was previously limited only to other Operational Technology records.

-   **[Check whether an OT device is virtual](https://www.servicenow.com/docs/access?context=ot-assets-form&version=zurich&pubname=zurich-operational-technology&ft:locale=en-US)**

Check whether an OT device is virtual using the **Is Virtual** field for OT devices in the following categories:

    -   OT Supervisory System
    -   OT Control System
    -   OT Field Devices
    -   Unclassed OT Devices
-   **[CMDB OT class model updates](https://www.servicenow.com/docs/access?context=cmdb-ci-class-models-operation-technology&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)**

Leverage an enhanced OT user experience and make additional configurations for your OT devices with the following CMDB OT class model updates:

    -   The IP Network Subnets related list was added to IT devices in the OT view to show all the subnets the device is related to show IP Network subnets for the selected OT device.

This related list was also added to the following CMDB classes:

        -   cmdb\_ci\_display
        -   cmdb\_ci\_firewall\_network
        -   cmdb\_ci\_security
        -   cmdb\_ci\_ids\_network
        -   cmdb\_ci\_imaging
        -   cmdb\_ci\_unclassed\_hardware
        -   cmdb\_ci\_multimedia
        -   cmdb\_ci\_monitor\_control
        -   cmdb\_ci\_aix\_server
        -   cmdb\_ci\_computer
        -   cmdb\_ci\_esx\_server
        -   cmdb\_ci\_hardware
        -   cmdb\_ci\_hpux\_server
        -   cmdb\_ci\_hyper\_v\_server
        -   cmdb\_ci\_iot
        -   cmdb\_ci\_ip\_firewall
        -   cmdb\_ci\_ip\_router
        -   cmdb\_ci\_ip\_switch
        -   cmdb\_ci\_linux\_server
        -   cmdb\_ci\_monitor\_control
        -   cmdb\_ci\_netgear
        -   cmdb\_ci\_ot
        -   cmdb\_ci\_pc\_hardware
        -   cmdb\_ci\_printer
        -   cmdb\_ci\_protocol\_converter
        -   cmdb\_ci\_server
        -   cmdb\_ci\_solaris\_server
        -   cmdb\_ci\_unix\_server
        -   cmdb\_ci\_ups
        -   cmdb\_ci\_win\_server
    -   You can now view the OT device details for the following CMDB classes:
        -   cmdb\_ci\_esx\_server
        -   cmdb\_ci\_hyper\_v\_server
    -   The **OT device details** tab was removed for the following CMDB classes because the OT device details are included in the form view of the CMDB class table:
        -   cmdb\_ci\_aix\_server
        -   cmdb\_ci\_hpux\_server
        -   cmdb\_ci\_pc\_hardware
        -   cmdb\_ci\_hyper\_v\_server
        -   cmdb\_ci\_esx\_server
        -   cmdb\_ci\_solaris\_server
        -   cmdb\_ci\_unix\_server
        -   cmdb\_ci\_ups
    -   Users assigned the admin role can edit the protection policy for an OT View rule for all CMDB classes.
    -   The OT Device Network Connection \[sn\_ot\_device\_network\_connection\] table references the CMDB CI relationships \[cmdb\_rel\_ci\] table to support device-to-device connections on the OT network.
    -   The Key Value \[cmdb\_key\_value\], Software Instance \[cmdb\_software\_instance\] and Firmware Install \[cmdb\_firmware\_install\] table references were added to the OT view on IT and OT classes.
    -   The Backup Storage Information \[cmdb\_backup\_storage\_information\] and Backup Job Execution History \[cmdb\_backup\_job\_execution\_history\] tables reference the CMDB CI relationships \[cmdb\_rel\_ci\] table to support backup management use cases.
-   **[Pre-import OT Worksheet Entry Review \(POWER\) tool updates](https://www.servicenow.com/docs/access?context=service-graph-connector-for-OT-excel&version=zurich&pubname=zurich-operational-technology&ft:locale=en-US)**

Import OT devices with distributed Microsoft Excel spreadsheets to help manage your OT system and its devices. The Pre-Import OT Worksheet Entry Review \(POWER\) tool includes the following new functionality:

    -   Improve validations with access to ISA sites using the cmdb\_ot\_isa\_viewer role that has been added to the ot\_staging\_user role needed for running validations.
    -   Upload, validate, and import Microsoft Excel spreadsheet data for the Service Graph Connector for Microsoft Excel by creating an import task and attaching the spreadsheet to the import task record.
-   **[Create remediation tasks for invalid staging records from an import task](https://www.servicenow.com/docs/access?context=create-remediation-task-for-validation-errors&version=zurich&pubname=zurich-operational-technology&ft:locale=en-US)**

After validating the imported staging records, create remediation tasks for invalid staging records directly in the import task record.


</td></tr><tr><td>

Operational Technology Vulnerability Response

</td><td>

-   **[Configuring Operational Technology Vulnerability Response from the SEM Workspace](https://www.servicenow.com/docs/access?context=configuring-oper-tech-vulnerability-response&version=zurich&pubname=zurich-operational-technology&ft:locale=en-US)**

Starting from Operational Technology Vulnerability Response version 30.0.x, users may be redirected to the Unified Security Exposure Management \(USEM\) Workspace to perform some configuration tasks. The Vulnerability Response plugin is consolidated under USEM from version 30.0.x.

-   **[Demo data not required for Operational Technology Risk Calculator plugin](https://www.servicenow.com/docs/access?context=calculate-vulnerability-risk&version=zurich&pubname=zurich-operational-technology&ft:locale=en-US)**

You can directly access and use the Operational Technology Vulnerability Response Risk Calculator without loading the demo data while installing the plugin. In previous releases, the risk calculation was included as part of the demo data.

-   **[Enhanced features for Hardware Vulnerability Assessment for OT devices](https://www.servicenow.com/docs/access?context=understanding-hwd-vuln-assessment&version=zurich&pubname=zurich-operational-technology&ft:locale=en-US)**

The following enhancements are available in Hardware Vulnerability Assessment:

    -   Assessments without Normalization: Ability to assess discovery models without content available for normalization.
    -   Confidence Scores: New scoring mechanism for all types of assessments.
    -   Version Range Support: The range information provided by the National Vulnerability Database \(NVD\) is used to create assessments without explicitly creating Common Platform Enumeration \(CPEs\) in the NVD.
    -   Partial assessment for partially normalized discovery model: Creates partial assessments for discovery models without firmware version. The partial assessments are done if the other versions of the discovery model have the same publisher and model.
    -   Expiring of assessments: If you update the firmware version of a CI, the corresponding normalized discovery model also updates. The assessment records based on the older firmware version expires while new assessments are generated for new firmware version.
-   **[Vulnerability risk scores on the OT Risk Management dashboard](https://www.servicenow.com/docs/access?context=otvr-risk-management-dashboard&version=zurich&pubname=zurich-operational-technology&ft:locale=en-US)**

View a table of vulnerability risk scores for your OT devices at each level of the equipment model with the OT Risk Management dashboard.


</td></tr><tr><td>

Opportunity Management

</td><td>

-   **[Delta pricing for opportunity](https://www.servicenow.com/docs/access?context=opportunity-management-details-tab&version=zurich&pubname=zurich-order-management&ft:locale=en-US)**

The following new fields added to the Opportunity and Opportunity Line objects improve visibility and provide greater flexibility in managing pricing amendments:

    -   Contract Start/End Dates
    -   Renewal Amount
    -   Upsell/Downsell Amounts
    -   Total Net New Amount
-   **[Add an opportunity associated contact](https://www.servicenow.com/docs/access?context=add-opportunity-associated-contact&version=zurich&pubname=zurich-order-management&ft:locale=en-US)**

Create opportunity associated contacts to associate multiple account contacts, verifying clear identification of all stakeholders and their respective roles.

-   **[Add a new opportunity team member](https://www.servicenow.com/docs/access?context=create-new-opportunity-team-member&version=zurich&pubname=zurich-order-management&ft:locale=en-US)**

Create a new opportunity team member to associate multiple team members with an opportunity to enable structured collaboration and grant access based on their roles. The ability to grant access is available from Zurich Patch 3 release.


</td></tr><tr><td>

Order Management

</td><td>

-   **[Move order](https://www.servicenow.com/docs/access?context=move-order&version=zurich&pubname=zurich-order-management&ft:locale=en-US)**

The move order helps agents to perform move journey that requires location change, the location and change of attribute values, the location change and add or delete the product.


-   **[Pricing Adjustments for order line items](https://www.servicenow.com/docs/access?context=add-pricing-adjustment-to-an-order-line-item&version=zurich&pubname=zurich-order-management&ft:locale=en-US)**

Enables order agents to quickly view, add, and edit manual price adjustments for order line items directly from the list view, reducing clicks and streamlining the process. This new experience makes it easier for order agents to enter manual price adjustments and provides a holistic view of both automatic and manual adjustments.

-   **[Summarization for Order Management](https://www.servicenow.com/docs/access?context=now-assist-order-mgmt-summarize-order&version=zurich&pubname=zurich-order-management&ft:locale=en-US)**

Summarizes complex orders across products, services, and fulfillment tasks. This helps agents quickly understand status, take the right actions, and avoid navigating fragmented views. This results in easier next steps and improved productivity. For more information, see the [Now Assist for Order Management release notes](../sales-order-management/now-assist-order-management-rn.md).


-   **[Support for complex characteristics for orders](https://www.servicenow.com/docs/access?context=som-using&version=zurich&pubname=zurich-order-management&ft:locale=en-US)**

Take advantage of the following complex characteristics for orders:

    -   Define complex characteristics for product offerings and specifications using object structures, data arrays, and other data input types such as String, Integer, Date, DateTime, and Decimal. For more information, see [Defining product characteristics and characteristic options](https://www.servicenow.com/docs/access?context=defining-prod-characteristics&version=zurich&pubname=zurich-order-management&ft:locale=en-US).
    -   Define compatibility, decomposition, and attribute propagation rules based on conditions that use characteristics at any level of a complex attribute hierarchy. For more information, see [Create a compatibility rule](https://www.servicenow.com/docs/access?context=create-compatibility-rules&version=zurich&pubname=zurich-order-management&ft:locale=en-US), [Create decomposition rules for specification relationships](https://www.servicenow.com/docs/access?context=order-mgt-specification-rels&version=zurich&pubname=zurich-order-management&section=order-mgt-create-decomposition-rules&ft:locale=en-US), and [Define domain order attribute mappings](https://www.servicenow.com/docs/access?context=define-domain-order-attributes&version=zurich&pubname=zurich-order-management&ft:locale=en-US).
-   **[Order header discount](https://www.servicenow.com/docs/access?context=add-header-discount-to-an-order&version=zurich&pubname=zurich-order-management&ft:locale=en-US)**

Provide order agents with the ability to apply discounts across multiple order lines with a single action through an order header discount feature. This feature streamlines discounting workflows, improves pricing consistency, and helps speed up order processing for large complex deals.


</td></tr><tr><td>

Partner Relationship Management

</td><td>

-   **[Data model for Partner Relationship Management](https://www.servicenow.com/docs/access?context=data-model-for-partner-relationship-management&version=zurich&pubname=zurich-order-management&ft:locale=en-US)**

Enable a user with the sn\_prm.enterprise\_partner\_admin role to map the fields on the channel partner record to their corresponding fields on the company record.

-   **[Partner Workspace](https://www.servicenow.com/docs/access?context=partner-workspace&version=zurich&pubname=zurich-order-management&ft:locale=en-US)**

Manage and view the partner details via the Partner workspace if you have the sn\_prm.enterprise\_partner\_admin role or the sn\_prm.enterprise\_partner\_rel\_manager role.

-   **[Partner Workspace](https://www.servicenow.com/docs/access?context=partner-workspace&version=zurich&pubname=zurich-order-management&ft:locale=en-US)**

Enable a user with the sn\_prm.enterprise\_partner\_rel\_manager role to manage cases, orders, sold products, and install bases by using the **Partner Overview** tab in the CSM Configurable Workspace.


-   ****

Use the segment \[sn\_seg\_segment\] table to create records, track partner progress toward the next tier, and group partners effectively based on performance into multiple segments for tailored support, incentives, and visibility.

-   ****

Provide channel partners with exclusive rights to work on a particular deal registration or customer for a period of time.

Use the configurable deal registration form to track deal registrations, information related to it, and successfully convert deal registrations to opportunities.

Use the deal registration playbook on the Partner portal to provide channel partners the flexibility to create new deal registrations and track their end to end life cycle.


-   ****

Install the Quote Management for Channel Partners \(com.snc.partner\_relationship\_management\_qm\) plugin to enable channel partners, B2B and B2C sales representatives, and managers to create, read, update, and track quotes associated with channel partners.


-   ****

Install the Order Management for Channel Partners plugin \(com.snc.partner\_relationship\_management\_orm\) to facilitate the entire order life cycle, especially indirect sales and enable channel partners to track orders with channel partners.


</td></tr><tr><td>

Performance Analytics

</td><td>

-   **[Apply multiple levels of breakdown to an indicator](https://www.servicenow.com/docs/access?context=multi-level-breakdowns&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US)**

Migrate indicators from traditional Performance Analytics architecture to change data capture \(CDC\)-based data snapshots. This new architecture allows for more than two levels of breakdown to apply to an indicator. RaptorDB Professional is required, and not all indicators qualify for migration.


</td></tr><tr><td>

Performance Analyzer

</td><td>

-   **[Filter by duration](https://www.servicenow.com/docs/access?context=filter-application-metrics-by-duration&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

Select a duration from the last fifteen minutes to the last seven days to view the aggregate data from that time period for each of your applications. The aggregate data includes total UI time, download time, trends, and a comparison to previous performance over that duration.

-   **[Application metrics](https://www.servicenow.com/docs/access?context=get-application-metrics&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

Select an application to filter metrics by total UI time and download time, as well as view page route performance.

-   **[Page route metrics](https://www.servicenow.com/docs/access?context=get-page-route-metrics&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

Select a page route within an application to view interaction metrics including timestamps, interaction types, total UI time, download time, and record.

-   **[Interaction metrics](https://www.servicenow.com/docs/access?context=get-interaction-metrics&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

Select an interaction within a page route to view a waterfall with details for each resource on the page during that interaction.


</td></tr><tr><td>

Platform Analytics experience

</td><td>

-   **[View, share, and export table records in the List component](https://www.servicenow.com/docs/access?context=create-dv-analytics-list&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US)**

Take advantage of the improved list capabilities of the List element, which replaces List - Simple. The List supports pagination, export from dashboards, export to comma-separated values, and alternative group by. It also provides a consistent configuration experience with other data visualizations.

-   **[Create indicators and migrate to data snapshots in the indicator library](https://www.servicenow.com/docs/access?context=your-kpis&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US)**
    -   Manage indicators from the indicator library, including links to create and edit indicators.
    -   Activate data snapshots conveniently, opening up the possibilities of applying multiple levels of breakdown to your indicators. See statistics on recent views and updates in tiles.
    -   If data snapshots are activated for the instance, see how many indicators are eligible and have already had data snapshots enabled.
    -   Show columns for any field on indicator records, as well as usage information.
-   **[Drill down to application overviews for User Experience Analytics](https://www.servicenow.com/docs/access?context=visualization-drilldown-in-config-ws&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US)**

Navigate to individual application overviews for User Experience Analytics from data visualizations. The **Go to data view** chart interaction is now supported for User Experience Analytics data and takes the viewer to these overview pages by default.

-   **[Filter data in User Experience Analytics](https://www.servicenow.com/docs/access?context=filter-user-list&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US)**

Filter User Experience Analytics data on default and custom User Experience Analytics properties.


</td></tr><tr><td>

Playbooks in Workflow Studio

</td><td>

-   **[Set child variants to evaluate later in a playbook](https://www.servicenow.com/docs/access?context=set-evaluation-point&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US)**

Instead of evaluating immediately after the trigger, set a playbook's child variants to be evaluated after a specific activity in the playbook.

-   **[Agentic Playbooks](https://www.servicenow.com/docs/access?context=agentic-playbooks&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US)**

Enable AI agents to assist users with activities during runtime.

-   **[Add permissions for playbook authors](https://www.servicenow.com/docs/access?context=user-access-playbooks&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US)**

Control which playbook authors can create, edit, and view playbooks in Workflow Studio

-   **[Add permissions for runtime users](https://www.servicenow.com/docs/access?context=create-process-definition&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US)**

Control whether runtime users can [view a playbook](https://www.servicenow.com/docs/access?context=create-process-definition&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US), [add optional activities](https://www.servicenow.com/docs/access?context=optional-activities&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US), [restart a playbook](https://www.servicenow.com/docs/access?context=restart&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US), and [complete work within specific stages](https://www.servicenow.com/docs/access?context=add-configure-stage&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US).

-   **[Create decision branches for stages](https://www.servicenow.com/docs/access?context=create-decision-stage&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US)**

Add a decision node between stages to determine which stage to run next, based on runtime conditions.

-   **[Set multiple triggers](https://www.servicenow.com/docs/access?context=process-automation-designer-triggers&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US)**

Configure a playbook to run based on any one of multiple triggers.

-   **[Schedule when a playbook should trigger](https://www.servicenow.com/docs/access?context=create-scheduled-trigger-definition&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US)**

Configure a playbook to run based on a schedule.

-   **[Choose your LLM for playbook generation and recommendations](https://www.servicenow.com/docs/access?context=change-default-llm-playbook-generation&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US)**

Choose between NowLLM, OpenAI ChatGPT4-o, Gemini, Claude for playbook generation and recommendations.

-   **[Route users to stages based on decisions](https://www.servicenow.com/docs/access?context=add-configure-stage&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US)**

Send runtime users to a stage based off of the trigger record or input that users provide.

-   **[Yokohama 27.2 and 27.3 releases](https://servicenow.com/docs/bundle/yokohama-release-notes/page/release-notes/now-platform-app-engine/process-automation-designer-rn.html)**

See 27.2 and 27.3 features in the [Yokohama Playbooks release notes](https://servicenow.com/docs/bundle/yokohama-release-notes/page/release-notes/now-platform-app-engine/process-automation-designer-rn.html):

    -   [Generate a playbook with the OpenAI GPT-4o LLM](https://www.servicenow.com/docs/access?context=generate-a-playbook-outline&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US)
    -   [Retrieval Augmented Generation \(RAG\) for playbooks](https://www.servicenow.com/docs/access?context=playbook-assist&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US)

</td></tr><tr><td>

Policy and Compliance Management

</td><td>

-   **[Association of citations to controls](https://www.servicenow.com/docs/access?context=citation-to-control-mapping&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

In many compliance frameworks, a single control objective may be referenced by multiple citations across different standards, regulations, or policy requirements. Without proper association management, organizations risk duplicating controls, misinterpreting coverage, or inaccurately reporting compliance. The association of citations to controls feature addresses this challenge by enabling users to associate controls with citations directly. When this feature is enabled, compliance scores update dynamically based on the status of directly associated active controls.


-   **[Enhancements to control objectives rationalization process](https://www.servicenow.com/docs/access?context=take-actions-on-the-recommendations-for-similar-control-objectives&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

The following enhancements have been introduced to the rationalization process of control objectives:

    -   Rationalization process is now automatically created when selecting the Rationalize button in the control objective page. 
    -   The recommendation workflow has been simplified into a two-step process: Step 1 identifies duplicates by accepting or dismissing recommendations; Step 2 finalizes by retaining one recommendation or creating a new common control objective.
    -   Approvals for the rationalization process are skipped for owners who are reviewers, and levels where all reviewers are owners are automatically approved. 
    -   Owners and approvers can add comments and justifications directly on recommendation cards and reply to existing comments. 
    -   The user interface has been updated with better navigation, quick summaries, visual improvements, and clear error messages.

-   **[Citation impact analysis and updates with Now Assist for IRM](https://www.servicenow.com/docs/access?context=control-objective-change-agent&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

When a citation’s description or supplemental guidance is updated, Now Assist identifies related control objectives that might be affected. It reviews these control objectives to determine whether the descriptions or guidance need changes and provides suggested updates. Users can review, provide feedback, and approve these updates directly in the Now Assist panel, ensuring that citation changes are reflected in associated control objectives.


-   **[Enhancements to control objectives and controls](https://www.servicenow.com/docs/access?context=co-overview-pc-ws&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

The following enhancements have been introduced to control objectives and controls:

    -   The Control objective requirements option provides a granular layer under a control objective. When each control objective has multiple statements, each statement becomes a control objective requirement.
    -   The Create control requirements option generates control requirements automatically for every control generated under an entity type.
    -   The Attestation at control requirement level enables attestation at a granular level for individual control requirements within a control.

-   **[Enhancements to policy exception and extension requests](https://www.servicenow.com/docs/access?context=review-policy-ext-and-extension-req-ws&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

The following enhancements have been introduced:

    -   For policy exception and extension requests, approvers can now view key details, such as justification, reason, and validity period, within a pop-up before approving or rejecting a policy exception or policy exception extension.
    -   For manual indicators, if the associated control is marked as exempt, no indicator task is generated.
    -   When a policy exception is in the Analyze state and the Awaiting Requested Information sub-state, the interface now includes a Send Information button that allows the requester to provide additional details or clarifications requested by the approver.
    -   Previously, an issue-based exception required a linked policy or control objective for additional approvals. Now, it requires any one of the following: a linked policy, control objective, or control. The control must be linked to the policy exception itself, not just to the issue.

-   **[GRC Approval Configurator](https://www.servicenow.com/docs/access?context=grc-approval-configurator-for-policy-extension-and-exception&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

The GRC Approval Configurator can now be used to manage both policy exception and extension approvals. It allows verification, approval, and extension rules to be defined based on state, sub-state, and other filter conditions, with support for multiple user groups and multi-level approvals. This enhancement provides greater flexibility in assigning appropriate approvers at each level based on defined conditions, facilitating structured and collaborative reviews. For extension approvals, users can now configure multiple approvers, overcoming the previous limitation of a single default approver \(Compliance Manager\).


-   **[Common Control Objective Creation](https://www.servicenow.com/docs/access?context=take-actions-on-the-recommendations-for-similar-control-objectives&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

Use Generative AI to merge similar control objectives into a single, consolidated common control objective. The system automatically populates the name, description, and guidance fields from the accepted duplicates, eliminating the need to manually select a primary control objective.


-   **[Entity based record access rules to secure new records](https://www.servicenow.com/docs/access?context=c_GRCControls&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

When entity based record access rules are enabled on the Entity Based Access Configuration Properties page, any newly created controls, control attestations, indicators, and indicator tasks associated with a configured entity will automatically inherit the entity-based access \(EBA\) value from that entity. Previously, users had to run bulk access updates to apply EBA restrictions whenever new objects were created.

Additionally, when a standard control is converted to a common control, the **Entity based access restriction** option is inactive by default. Users can manually enable the EBA option for common controls directly from the Access Settings section in the Details tab of the respective control.


</td></tr><tr><td>

Portfolio Planning

</td><td>

-   **[Roadmap enhancements](https://www.servicenow.com/docs/access?context=planning-roadmaps-in-portfolio-planning&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)**
    -   Create custom themes for your roadmap bar colors to align with your organization’s standards.
    -   Experience consistent roadmap bar colors for choice list attribute values across all portfolio plans.
    -   View the roadmap-level milestone row while scrolling down the Roadmap page.
    -   Use different icons to distinguish item-level milestones.
-   **[Dynamic data linking in Docs](https://www.servicenow.com/docs/access?context=docs-for-planning-items-in-ppw&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)**

Keep record information in your documentation always current and reduce manual effort with the Dynamic data linking feature in Docs. You can now reference any ServiceNow application record and Docs will automatically reflect the latest updates from those records. For example, if you add a reference to a Project record, the reference will show the latest field information of the project in Docs without requiring manual edits. Clicking the project reference opens up the project form so that you can view the full details of the project record and make any necessary changes. Dynamic linking also enables adding references to a particular field of a record, such as Assigned to of an Incident record.

You can add references from any ServiceNow table you have access to, with no setup or configuration needed, thereby eliminate the hassle of switching between applications to copy and paste data from various records into Docs.

-   **[Scenario planning enhancements](https://www.servicenow.com/docs/access?context=enable-scenario-planning-in-portfolio-planning&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)**

With the sn\_align\_core.apw\_admin role, you can enable or disable the scenario planning feature. The **sn\_align\_ws.is\_scenario\_planning\_disabled** system property allows you to enable or disable the scenario planning feature.

-   **[Quick filters enhancements](https://www.servicenow.com/docs/access?context=quick-fiters-prioitization-roadmap-ppw&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)**

Apply filters using string-type and Boolean field values across the Planning page to view the required dataset. These filters are saved as part of your user preferences, enabling you to access the same filtered data when you log back in and continue your planning seamlessly.

-   **[Financial enhancements](https://www.servicenow.com/docs/access?context=using-financials-pp&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)**
    -   View only the planned costs of your planning items to track the total cost of projects or demands.
    -   Use **Display mode** to switch between focused views to better plan and track the financials of your planning items.
    -   Manage the planned and actual monetary benefit plans for your projects to identify the financial performance of your project using the Cost and benefits screen.
    -   Use multicurrency to view and manage financial records of the project in Investment currency, which can be different from your functional currency. Manage multiple financial records such as planned and actual expenses, planned and actual benefits, and so on.
    -   Generate and track labor cost for sub-projects, based on the resource assignments of your sub-projects and planning items such as features and capabilities.

</td></tr><tr><td>

Predictive Intelligence

</td><td>

-   **[Review any errors in predictions using the Observability Dashboard](https://www.servicenow.com/docs/access?context=prediction-errors-observability-dashboard&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Monitor errors using the Observability Dashboard which provides analytics derived from a new table. This table is dedicated to logging any errors that may occur during Predictive Intelligence predictions.

-   **[Leverage new advanced options for classification solutions](https://www.servicenow.com/docs/access?context=configuring-advanced-settings-ml-solutions&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Customize your classification models in Predictive Intelligence with the following advanced options.

    -   [Configure include only top N labels](https://www.servicenow.com/docs/access?context=predictive-intel-only-top-n-labels&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US): Limit the classification model to use only the top most frequent labels. You can choose a number as the limit.
    -   [Minimum records needed for label to include it](https://www.servicenow.com/docs/access?context=predictive-intel-minimum-records-needed-label&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US): Set a threshold for the minimum number of records a label must have in your dataset to be included in model training.
    -   [Remove others label](https://www.servicenow.com/docs/access?context=predictive-intel-remove-others-label&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US): Reduce noise in the model and enhance predictive accuracy by removing records with the label "others" from training data.
    -   [Use LightGBM algo for classification model training](https://www.servicenow.com/docs/access?context=predictive-intel-lightgbm-algo&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US): Enable the LightGBM \(Light Gradient-Boosting Machine\) algorithm for training classification models.
    -   [Config parameters for model config in classification](https://www.servicenow.com/docs/access?context=predictive-intel-config-parameters-classification&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US): Customize training behavior by including a dictionary of parameters in the JSON format.

</td></tr><tr><td>

Privacy Management

</td><td>

-   **[Data subjects](https://www.servicenow.com/docs/access?context=data-subjects&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

Select and define the multiple data subject types for each processing activity. You can capture the volume of data subjects that were processed, the specific data elements that were collected from the users, and the user locations. With this feature, you get a realistic, granular, and scalable representation of your processing activities.

-   **[Privacy management dashboard](https://www.servicenow.com/docs/access?context=privacy-manager-dashboard&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

Get an overview of your complete privacy risk and compliance posture from the Privacy Management dashboard so that you can quickly prioritize and remediate your processing activities. By looking at the Processing Activities, Risk &amp; Compliance, and Operations &amp; Case management sections, you can see the overall compliance score, trends, privacy criticality assessment scores, and risk heatmap. From the dashboard, you can also see information about the global legal framework to understand the regional obligations and the built-in risk metrics that automatically assess each processing activity.

-   **[New screening and PIA templates](https://www.servicenow.com/docs/access?context=privacy-mgmt-workflow&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

Use the new Privacy Impact Assessments \(PIAs\) and Screening Assessment templates that provide standardized questions, evaluation criteria, and workflows so that you can perform a processing activity criticality and privacy risk assessment. With these new templates, you can ensure consistency, reduce manual effort, and support compliance with regulatory and organizational requirements.


</td></tr><tr><td>

Proactive Service Experience Workflows

</td><td>

-   **[Components installed with Proactive Service Experience Workflows](https://www.servicenow.com/docs/access?context=components-psew&version=zurich&pubname=zurich-proactive-service-exp-workflows&ft:locale=en-US)**

The granular admin role enables developers and administrators to complete administrative configuration tasks for Proactive Service Experience Workflows without requiring the full admin role.


-   **[Components installed with Product Support for Technology](https://www.servicenow.com/docs/access?context=components-product-support-case&version=zurich&pubname=zurich-proactive-service-exp-workflows&ft:locale=en-US)**

The granular admin role enables developers and administrators to complete administrative configuration tasks for Product Support for Technology without requiring the full admin role.


-   **[Diagnose and resolve an incident](https://www.servicenow.com/docs/access?context=diagnose-reslove-incident-psew&version=zurich&pubname=zurich-proactive-service-exp-workflows&ft:locale=en-US)**

Diagnose the incident in the Proactive Service Experience Workflows and create the resolution task manually to resolve the issue.

-   **[Diagnose and resolve a change request](https://www.servicenow.com/docs/access?context=diagnose-resolve-case-change-request&version=zurich&pubname=zurich-proactive-service-exp-workflows&ft:locale=en-US)**

Review, diagnose, resolve, and close a change request case for the service-related issue experienced by the customer.

-   **[Diagnose and resolve a Product Support for Technology case](https://www.servicenow.com/docs/access?context=diagnose-resolve-hitechcases&version=zurich&pubname=zurich-proactive-service-exp-workflows&ft:locale=en-US)**

Review, diagnose, resolve, and close the Product Support for Technology Case.


</td></tr><tr><td>

Process Mining

</td><td>

-   **[Opportunity details page](https://www.servicenow.com/docs/access?context=opportunity-details&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US)**

Generate highlights to surface key drivers behind process patterns that accelerate decision-making and prioritization of process changes on the Opportunity details page. This page provides the detailed context of every improvement opportunity. It uses Now Assist to help generate highlights.

-   **[Idle time analysis](https://www.servicenow.com/docs/access?context=idle-time-analysis&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US)**

Analyze where cases are waiting to be assigned to agents by tracking and analyzing the time during which the case is assigned to a team but not yet to an agent. Idle time analysis helps identify inefficiencies, such as delays in task assignment or workflow bottlenecks, and helps improve coordination and reduce waiting time within processes. Idle time analysis must be configured in the process configuration.

-   **[Touchpoint analysis](https://www.servicenow.com/docs/access?context=touchpoint-analysis&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US)**

Identify where and how human involvement occurs in a process by using touchpoint analysis. Analyzing the fields that involves human involvement helps you improve your processes, enhancing performance and reducing operational costs. Touchpoint analysis enables you to analyze the workload of transitions and cases. Touchpoint analysis must be configured in the process configuration.

-   **[Enhanced data security](https://www.servicenow.com/docs/access?context=set-objectives&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US)**

Mark a project as restricted to help protect sensitive data and avoid security breaches. Restricted project data is available only to the owner and the users with whom the project is shared.

-   **[Share a Process Mining project](https://www.servicenow.com/docs/access?context=share-project&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US)**

Share projects through a link that remains unchanged even when the project is updated and remined.

-   **[Creation of automation requests and CIMs simplified](https://www.servicenow.com/docs/access?context=submit-automation-idea&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US)**

When creating an automation or Continual Improvement Management \(CIM\) request from Process Mining, mandatory fields are pre-populated, reducing friction and accelerating time-to-action.

-   **[Process Mining integrated with ServiceNow playbook](https://www.servicenow.com/docs/access?context=analyst-workbench-dashboard&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US)**

Process Mining has been integrated with ServiceNow playbook. After analyzing and identifying a process for improvement, export the process to playbook and add subflows or triggers to analyze and refine the flow.

Use the Playbooks icon on the Process Mining Analyst Workbench to export up to 5 routes of a project to ServiceNow playbook. This feature is enabled by Now Assist.


</td></tr><tr><td>

Product Catalog Management and Pricing Management

</td><td>

-   **[Create configurable product offerings and associated blueprints](https://www.servicenow.com/docs/access?context=som-create-configurable-prod-offerings&version=zurich&pubname=zurich-order-management&ft:locale=en-US)**

Enable product catalog admins to generate blueprints for configurable products using the CPQ Configurator. A blueprint contains the product attributes, product relationships, product and pricing rules, and child products that control the structure of a configurable product offering. It also contains configuration rules, such as inclusion, exclusion, and determination. Blueprints drive the agent and customer experience when configurable products are added using the configurator. Catalog admins can review and update an offering blueprint in the CPQ Configurator, then publish the product offering to the product catalog.

-   **[AI Search queries in the product catalog interface](https://www.servicenow.com/docs/access?context=configure-ai-search-prod-catalog&version=zurich&pubname=zurich-order-management&ft:locale=en-US)**

Enable semantic search features that agents and customers can use in the product catalog to find relevant product offerings. Users can search by product offer attributes, characteristics, and child offerings, and also view auto-complete suggestions. AI Search supports queries with synonyms, multi-languages, Boolean operators, and auto-correction \(typo handling\). Product catalog admins can configure stop words, synonyms, and rules that control the search results displayed.

-   **[Complex characteristics](https://www.servicenow.com/docs/access?context=som-product-config-add-characteristics&version=zurich&pubname=zurich-order-management&ft:locale=en-US)**

Starting with Product Catalog Management Core v13.0, enable product catalog admins to define product and specification characteristics using an object-based structure that supports the following data types: integer, decimal, date and date time, and data arrays. For example, product catalog admins can use these new data types to define characteristics for communication products, such as routing characteristics, that have nested levels of characteristics and characteristic options. These complex characteristics can then be used to define conditions for setting decomposition, attribute propagation, and compatibility rules.

    -   Agents can view and select the complex characteristics available for configurable product offerings when creating opportunities, quotes, and orders. Complex attributes are displayed as separate nodes in the product hierarchy tree of the legacy product configurator interface.
    -   Fulfillment agents can perform fulfillment tasks that capture complex characteristic data for new or MACD orders.
    -   Customers can view and select complex characteristics when using the Business Portal to order configurable products.
**Note:**  Complex characteristics aren’t supported in the CPQ Configurator.


-   **[Derived product pricing](https://www.servicenow.com/docs/access?context=configuring-related-product-pricing&version=zurich&pubname=zurich-order-management&ft:locale=en-US)**

Define dynamic product pricing relationships between products, where the price for a product is derived from the price of another product or transaction-level values, such as the total quote value or annual contract value \(ACV\). When sales or order agents add the product to a quote or order, they can see how the product price is derived in real time.

-   **[Price and quantity ramps](https://www.servicenow.com/docs/access?context=defining-products-with-ramps&version=zurich&pubname=zurich-order-management&ft:locale=en-US)**

Enable product catalog admins to identify configurable product offerings for which pricing ramps can be created. These product offerings must also have the recurring pricing method. Sales agents create price ramps for quote lines that define and schedule pricing and quantity changes as product deals evolve over a given time period.

-   **[Product pricing changes related to MACD activities](https://www.servicenow.com/docs/access?context=net-pricing-sp-contracts&version=zurich&pubname=zurich-order-management&ft:locale=en-US)**

Support different price bases, such as original prices, fresh prices, or zero prices, used to calculate pricing for products during MACD activities.

-   **[Cost-based attribute adjustments](https://www.servicenow.com/docs/access?context=create-cost-attribute-adjustment&version=zurich&pubname=zurich-order-management&ft:locale=en-US)**

Enable pricing admins or managers to set different product costs based on product attributes, such as model or size, by using cost book-specific or product offering-based adjustments for cost book lines. Previously, only a single cost amount was captured for a product offering, even if the product had different attributes that affected the product cost. These adjustments determine the base product cost used to calculate profit margins for sales agents when they create quotes for customers.


</td></tr><tr><td>

Project Portfolio Management

</td><td>

-   **[Managing projects with Project Workspace](https://www.servicenow.com/docs/access?context=use-projects-pw&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)**
    -   End resource assignments when a project ends, view assignment details, and synchronize assignment dates with project dates.
    -   Access and edit the resource details directly from the Resource page without switching between views.
-   **[Identify similar records using Now Assist](https://www.servicenow.com/docs/access?context=identify-similar-demand-records&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)**

Detect similar existing demand records when creating or editing a demand using the identify similar records skill. This skill compares the **Name**, **Description**, and **Business Case** fields for contextual similarity.

-   **[Convert demands to EAP entities](https://www.servicenow.com/docs/access?context=t_CrtArtftDmdMnu&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)**

Convert your demand records quickly to Enterprise Agile Planning \(EAP\) entities, such as Epic, Feature, or Capability. When you convert a demand, the system generates a new record of the selected entity type, replicates common fields from the demand, and moves the demand to the Approved state.


</td></tr><tr><td>

Project Workspace

</td><td>

-   **[Use Playbooks in Project Workspace](https://www.servicenow.com/docs/access?context=use-playbooks-pw&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)**
    -   Playbooks provide structured stages and activities to keep projects on track.
    -   Added two playbooks for Project Workspace: Project Default and Stage-gate Default.
    -   Use one of the two out-of-box playbooks or create your own to match your project process.
-   **[Monitor and update project report status](https://www.servicenow.com/docs/access?context=duplicate-status-report-pw&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)**
    -   Track the status of project reports using the Status drop down, and change the status from Draft to Published once updates are complete.
    -   Status changes are restricted to the Project Manager role.
-   **[Copy and edit status report enhancements](https://www.servicenow.com/docs/access?context=update-status-report-project-workspace&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)**
    -   Simplified workflow for copying and editing status reports. Duplicate a status report directly without opening a form modal.
    -   The duplicated report automatically refreshes with the latest project updates \(for example, overall status, milestones, or metrics\).
    -   Any static or manually added data from the original report is retained in the duplicated version.
    -   When editing is disabled, all fields in the status report are read-only. When editing is enabled, only dynamic fields remain read-only. You can edit the status report in both the scenarios using the Edit Status Report action in the context menu.
-   **[Resource assignment updates](https://www.servicenow.com/docs/access?context=use-resource-mgmt-prj-wksp&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)**
    -   Access and modify resource details directly from the Resource page without having to navigate to Resource Management Workspace.
    -   End resource assignments when a project ends. View the resource assignments and synchronize the resource assignment dates with the project dates.
    -   Move resource assignments to a new start and end date to align with task dependencies or resource availability.
-   **[Status report properties](https://www.servicenow.com/docs/access?context=create-a-status-report-in-project-workspace&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)**
    -   Updates made on the status report form are reflected in the Status Report document when the `sn_pw.status_report_doc_read_only` property is set to `true`.
    -   Updates made on the status report form are not reflected in the document content when the property is set to `false`.
-   **[Project financials](https://www.servicenow.com/docs/access?context=using-financials-prj-wrkspc&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)**
    -   View only planned costs of your planning items to track the total cost of your projects.
    -   Use **Display mode** to switch between focused views to better plan and track the financials of your projects.
    -   Manage the planned and actual monetary benefit plans for your projects to identify the financial performance of your project using the Cost and benefits screen.
    -   Use multicurrency to view and manage financial records of the project in Investment currency, which can be different from your functional currency. Manage multiple financial records such as planned and actual expenses, planned and actual benefits, and so on.
    -   Generate labor cost for sub-projects based on the resource assignments of your sub-projects.

</td></tr><tr><td>

Public Sector Digital Services

</td><td>

-   **[Grants Management Funding Program](https://www.servicenow.com/docs/access?context=psds-using-grants-management-playbook&version=zurich&pubname=zurich-government-industry&ft:locale=en-US)**

Create a funding program, which serves as the top-level container from which individual grant programs are created and derive their budget allocations.

Grant program managers can create a new funding program, or start by copying data and configurations from an existing funding program, using the funding program ID. From this funding program, admins can create grant programs directly, set and update the duration and overall budget, and ensure budgets flow down logically to individual grants.

Each grant program is associated with a single funding program via the funding program ID. All grant programs linked to a specific funding program share the cumulative budget of that funding program, and their start and end dates fall within the funding program's duration.

-   **[Grants Management Evaluation &amp; Decision​](https://www.servicenow.com/docs/access?context=psds-using-grants-management-playbook&version=zurich&pubname=zurich-government-industry&ft:locale=en-US)**

Simplify and streamline your grant application decisions​ with Grants Management:​ Evaluation &amp; Decision. You can review, score, and manage proposals for grant programs in the Merit Review portal and define a funding proposal for a grant program by using the Grants Workspace. You can share this information internally with the grant program director.​ Grant program managers can define the merit review framework criteria, assign a reviewer group to each application, create, and track merit review tasks. Grant program managers can use document templates to compose letters that inform the applicants of results, with template options for Award, Rejected \(Ineligible\), and Rejected \(Decline\).

-   **[Grants Management Reviewer Service portal](https://www.servicenow.com/docs/access?context=psds-gmp-using-merit-review-portal-agent&version=zurich&pubname=zurich-government-industry&ft:locale=en-US)**

Enable your merit reviewers to track, score, and monitor grant applications via a dedicated Reviewer Service portal. The merit reviewers can capture and aggregate scores across the Grant Proposal review framework​ in the Grants Workspace. A score and rationale can be summarized as part of the application proposal result.​

-   **[Agentic AI for Public Sector Digital Services](https://www.servicenow.com/docs/access?context=agentic-ai-psds-explore&version=zurich&pubname=zurich-government-industry&ft:locale=en-US)**

Define the fees for information requests and autonomously assess waivers against an agency's criteria​. You can automate the process of synthesizing similar information requests and associated fees, and apply those fees to cases​. Your case fields are automatically filled in and integrated into the Information Request Playbook workflow and ServiceNow's AI framework.


</td></tr><tr><td>

Purchase Order Management

</td><td>

-   **[Reporting delivery plan issues](https://www.servicenow.com/docs/access?context=reporting-delivery-plan-issues&version=zurich&pubname=zurich-source-to-pay-operations&ft:locale=en-US)**

Suppliers can report delivery plan issues related to purchase order line through the Supplier Collaboration Portal, ensuring prompt visibility for the appropriate buyer. Suppliers can also track and collaborate with the buyers on the purchase order exception on the related record in Supplier Lifecycle Operations.


-   **[Centralized interface for purchase order exceptions](https://www.servicenow.com/docs/access?context=purch-order-mgmt-ws&version=zurich&pubname=zurich-source-to-pay-operations&ft:locale=en-US)**

The Purchase Order Management page provides operational buyers with a centralized interface to monitor and review purchase order exceptions. Users can quickly identify urgent issues, view recent tasks, and take approval actions, improving workflow visibility and exception handling.


-   **[Resolving purchase order exceptions](https://www.servicenow.com/docs/access?context=resolving-purchase-order-exceptions&version=zurich&pubname=zurich-source-to-pay-operations&ft:locale=en-US)**

Enables buyers to resolve purchase order exceptions directly from the exception page, with options to accept supplier proposals or make custom edits. It also allows buyers to find alternative suppliers with open orders for the same materials and request order expediting or increased quantities.


</td></tr><tr><td>

Quote Management

</td><td>

-   ****

Enables sales agents to quickly view, add, and edit manual price adjustments for quote line items directly from the list view, making it easier to manage both automatic and manual adjustments. The new experience streamlines the quoting process and allows adjustments to be applied to individual or multiple line items at once.


-   **[Price and quantity ramps on quote line items](../../product/tmt-order-mgt/task/add-price-ramps-on-a-quote-line-item.md)**

Create price and quantity ramps for product offerings in quotes to define incremental price and quantity changes over time. Product offerings eligible for ramps have the Ramps enabled option and Recurring price method selected. Agents can define ramps in two ways:

    1.  Ramp the parent line item, which automatically applies ramps to all child line items.
    2.  Leave the parent unramped, allowing child product offerings to have ramps defined individually.

Agents can also make manual price adjustments per segment. When a quote with ramps is converted to an order, ramps become read-only.


-   **[Quote header discount](https://www.servicenow.com/docs/access?context=add-header-discount-to-a-quote&version=zurich&pubname=zurich-order-management&ft:locale=en-US)**

Added a quote header discount feature that enables sales agents to apply a discount across multiple quote lines at once. This simplifies the quoting process and ensures consistent discount application, thereby improving overall sales efficiency and customer satisfaction.


-   **[Subscription revenue metrics](https://www.servicenow.com/docs/access?context=som-subscription-pricing&version=zurich&pubname=zurich-order-management&ft:locale=en-US)**

Provides sales agents better visibility of the entire quote cost and profit with the addition of Cost and Margin calculations to the following levels:

    -   **Quote Header**: Total one-time cost, Total monthly cost, Total cost, Total one-time margin, Total monthly margin, Total margin amount, Total one-time margin %, Total monthly margin %, and Total margin %.
    -   **Quote Line**: One-time cost, Monthly recurring cost, Cumulative one-time cost, Cumulative monthly cost, Cumulative margin %, and Cumulative Net Cost.
The automated calculation rules introduced at Quote Header and Quote Line levels enable informed discounting decisions and help prevent unprofitable deals.


</td></tr><tr><td>

RPA Hub

</td><td>

-   **[Try catch component enhancement](https://www.servicenow.com/docs/access?context=use-general-try-catch&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US)**

You can now precisely control the scope of Try-Catch blocks by selecting which actions \(components\) to include within exception handling and which to manage outside it. This enhancement provides better control over error handling logic and improves workflow reliability.


-   **[Role changed for creating, updating, and deleting the Robot License Distribution records](https://www.servicenow.com/docs/access?context=create-lua-record&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US)**

Role for Create, Update, and Delete ACLs in the Robot License Distribution table is changed from admin to sn\_rpa\_fdn.rpa\_admin.

-   **[Long term stable models](https://www.servicenow.com/docs/access?context=long-term-stable-models&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Long term stable \(LTS\) models are part of Now LLM Service and provide longer model stability windows for regulated industries. These models can integrate with tools to provide governance, monitoring, and compliance controls.


-   **[New third-party AI model provider options available for all Now Assist applications](https://www.servicenow.com/docs/access?context=exploring-large-language-models&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Google Gemini and AWS Claude are available for RPA bot generation skill in addition to Now LLM Service and Azure OpenAI.

-   **[Python connector](https://www.servicenow.com/docs/access?context=python-connector-rpa&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US)**

Execute custom Python scripts or files as part of an automation workflow in the RPA Desktop Design Studio.

The connector comprises two methods:

    -   Execute: Runs Python scripts set up in the configuration window.
    -   InvokeScript: Runs Python script on local computers and gets the output.
Ensure to install the Scripting plugin from the Plugins Manager as a prerequisite. Along with Python, VB.NET, C\#, and Javascript connectors are available with this plugin.

-   **[Smart Card authentication](https://www.servicenow.com/docs/access?context=smart-card-il&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US)**

Use a physical smart card instead of a username and password for logging into a Windows machine.

You can run unattended automations on the machines that use smart cards for authentication. While configuring a robot credential, you can store the smart card username and password to allow the unattended robot to log in to machines that use smart card.

-   **[Enhanced ACLs for security measures](https://www.servicenow.com/docs/access?context=installed-with-rpa-hub&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US)**

Enhanced access controls for RPA bot generation skill for Now Assist for RPA Hub in compliance with AI security directives.

Access to RPA bot generation skill is now restricted to users with the RPA developer or RPA admin role. These roles contain the RPA Hub Admin user role \(sn\_nowassist\_admin.user\).


</td></tr><tr><td>

Recommended Actions for Operational Technology Service Management \(OTSM\)

</td><td>

-   **[Contextualize an external document](https://www.servicenow.com/docs/access?context=use-ai-enhanced-ra-otsm&version=zurich&pubname=zurich-operational-technology&ft:locale=en-US)**

Contextualize an external document to get an explanation of why the document is relevant to the selected OT incident.

-   **[Apply Recommended Actions to your Operational Technology incidents](https://www.servicenow.com/docs/access?context=use-recommended-actions-ot-incidents&version=zurich&pubname=zurich-operational-technology&ft:locale=en-US)**

Use Recommended Actions to see relevant actions that can help resolve your OT incidents.


</td></tr><tr><td>

Recruitment workspace

</td><td>

-   **[Create a job requisition as a recruiter](https://www.servicenow.com/docs/access?context=request-job-hiring&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

Create a job requisition for a vacancy that you want to fill in your organization.

-   **[Track a job requisition in the Recruitment workspace](https://www.servicenow.com/docs/access?context=job-req-details-re-workspace&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

Track a job requisition and view the job details, associated applications, hiring team, interview phases, approvers, and prospects.

-   **[Manage hiring team](https://www.servicenow.com/docs/access?context=manage-hiring-team&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

Add, edit, or remove hiring team members from a job requisition.

-   **[Add a job description to a requisition](https://www.servicenow.com/docs/access?context=add-job-description&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

Manually add a description to a job requisition or use predesigned templates to fill it out faster.

-   **[Manage the job requisitions as a recruiter](https://www.servicenow.com/docs/access?context=manage-job-reqs&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

Update or duplicate a job requisition, put it on hold, send it for approval, or close it from the Recruitment workspace.

-   **[Tracking an application in the Recruitment workspace](https://www.servicenow.com/docs/access?context=application-record-details-re-workspace&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

Track an application for a job requisition and its corresponding applicant and interview details as a recruiter or recruitment coordinator.

-   **[Hiring tasks](https://www.servicenow.com/docs/access?context=applicant-tasks-recruitr&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

Create and assign tasks to your job applicants or internal stakeholders, and manage them within the Recruitment workspace.

-   **[Collaborate with the hiring manager](https://www.servicenow.com/docs/access?context=collab-hiring-manager&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

Collaborate with the hiring manager on the job requisition in the activity stream.

-   ****

Send targeted emails to the internal and external talent types from different access points in the Recruitment workspace for effective communication.

-   **[View the Talent Acquisition Dashboard](https://www.servicenow.com/docs/access?context=access-kpi-ta&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

Understand the hiring trend in your organization with the Talent Acquisition dashboard.


</td></tr><tr><td>

Regulatory Change Management

</td><td>

-   **[Now Assist for Integrated Risk Management \(IRM\)](../governance-risk-compliance/now-assist-for-irm-rn.md)**

You can review the Now Assist for Integrated Risk Management \(IRM\) release notes for full descriptions of the Now Assist in Regulatory Change Management \(RCM\) features.

-   **[Add multiple regulatory tasks](https://www.servicenow.com/docs/access?context=regulatory-change-tasks&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

Add multiple regulatory tasks to an alert. Each task can represent a distinct area of impact or required action. By organizing work into separate change tasks, your teams can assign responsibilities, track progress, and manage dependencies more effectively.

-   **[Add multiple source document import tasks](https://www.servicenow.com/docs/access?context=source-document-import-tasks&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

Associate multiple source document import tasks with one regulatory alert to simplify the management and tracking of your regulatory content ingestion. Each import task adds the relevant documents to the regulatory library to help ensure that all source materials that are related to the alert are accurately captured and organized. You can help to improve traceability throughout the regulatory change management process.

-   **[Close a regulatory task](https://www.servicenow.com/docs/access?context=regulatory-change-tasks&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

Close a regulatory task automatically when it's approved. You can also manually close a regulatory task while it's in the Implementation state, if all the associated action tasks are completed and closed. By closing a task manually, you get flexibility in managing the regulatory changes that don’t require formal approval workflows.

-   **[Reopen action tasks](https://www.servicenow.com/docs/access?context=action-tasks&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

Reopen the action tasks for a regulatory task when it's rejected and transitions back to the Implementation state. You can review and rework the tasks to address the feedback or incorporate the updated requirements. You can also modify and resubmit the reopened action tasks so that the implementation aligns with regulatory expectations before you resubmit the change task.

-   **[Close a regulatory alert](https://www.servicenow.com/docs/access?context=list-view-of-reg-alerts&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

Close a regulatory alert manually after all the associated regulatory tasks are complete. By closing the alert, you help to ensure accurate record-keeping by signaling that a compliance life-cycle for the specific regulatory alert is complete.

-   **[Work on action tasks](https://www.servicenow.com/docs/access?context=action-tasks&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

Initiate and complete the action tasks independently without requiring prior approval from users who are assigned with the `sn_grc_reg_change.manager` role. You can execute assigned responsibilities in a timely manner and reduce unnecessary approval bottlenecks. The access to action tasks remains governed by user permissions and role-based access controls to ensure proper accountability and oversight.


</td></tr><tr><td>

ReleaseOps

</td><td>

-   **[Pipelines in ReleaseOps](https://www.servicenow.com/docs/access?context=releaseops-pipeline-environments&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

A pipeline is the flow of a deployment in ReleaseOps. A pipeline's flow is defined within playbooks, which enables you to customize as needed.

-   **[Releases in ReleaseOps](https://www.servicenow.com/docs/access?context=releases-in-release-ops&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

Scheduled and on-demand releases are how changes are deployed to target instances with ReleaseOps. Releases can contain one or more deployment requests.

-   **[Deployment requests in ReleaseOps](https://www.servicenow.com/docs/access?context=deployment-requests&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

Deployment requests contain one or more update sets, and are contained in a release.

-   **[Configure a new ReleaseOps ecosystem](https://www.servicenow.com/docs/access?context=configure-new-releaseops-ecosystem&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

Configure a new ReleaseOps ecosystem using the sample pipelines and playbooks to begin deploying changes from your development to test to production instances.

-   **[Create a custom pipeline](https://www.servicenow.com/docs/access?context=create-release-ops-pipeline&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

Create a custom pipeline to move changes through your production environment to testing by duplicating one of the ReleaseOps playbooks.

-   **[Promote an update set for deployment](https://www.servicenow.com/docs/access?context=promote-update-set-for-deployment&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

When you're ready to deploy your changes, promote your update set to begin the deployment process.

-   **[Create a deployment request for a scheduled release](https://www.servicenow.com/docs/access?context=create-a-new-deployment-request&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

Create a deployment request for a scheduled release to contain your update set and enable your changes to move through the pipeline for deployment.

-   **[Create a release](https://www.servicenow.com/docs/access?context=create-a-release&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

Specify the details for your release, including the target instance that the changes deploy to and when the release should occur.


-   **[ReleaseOps guided setup](https://www.servicenow.com/docs/access?context=complete-guided-setup&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

Starting with version 1.2.1 of ReleaseOps, you can use guided setup to help simplify the initial configuration process.


</td></tr><tr><td>

Resource Management Workspace

</td><td>

-   **[Move a resource assignment](https://www.servicenow.com/docs/access?context=move-ra-rmw&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)**

Move any assigned resource assignment without actuals or an unassigned resource assignment to a different date to align the work with your project realignment, prioritization, or resource availability. You can move individual resource assignments based on your project or organizational priorities.


-   **[Using Resource Management Workspace](https://www.servicenow.com/docs/access?context=using-rmw&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)**
    -   View the type of operational work that is assigned to a resource using the resource board drill-down view.
    -   Filter your resource board using data grid filters to easily navigate and modify the resource assignments in the top tray.
    -   Sync the resource assignments to align them with change in planning item dates.
    -   Override resource rate for each assignment from the assigned work in the top tray.
    -   Apply filters using string-type and boolean field values across the resource card top tray to view the required dataset.
-   **[Assign resource assignments](https://www.servicenow.com/docs/access?context=allocate-resources-rmw&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)**

Allocate effort from unassigned resource assignments using the following ways:

    -   Auto-assign work among all the available resources.
    -   Partially assign work among for selected resources.

</td></tr><tr><td>

Retail applications

</td><td>

**Note:** The new Retail Mobile application and the new case types are available in the Yokohama release.

-   **[Retail mobile application](https://www.servicenow.com/docs/access?context=rahi-retail-retail-mobile&version=zurich&pubname=zurich-retail-industry&ft:locale=en-US) Retail Mobile application**

As a store manager or a store associate, boost productivity by managing operations and accessing key tools on the go with the Retail Mobile application.

-   **[Customer complaint case](https://www.servicenow.com/docs/access?context=rahi-retail-retail-customer-complaint&version=zurich&pubname=zurich-retail-industry&ft:locale=en-US) Customer complaint**

Help ensure quick and efficient customer service resolutions by capturing store-related complaints from customers using the customer complaint case type in the Retail customer complaint plugin.

-   **[Store inquiry case](https://www.servicenow.com/docs/access?context=rahi-retail-retail-store-services&version=zurich&pubname=zurich-retail-industry&ft:locale=en-US) Store inquiry**

Streamline the process for contacting HQ for store-to-HQ cases with the store inquiry case type in the Retail Store Services plugin, which provides a clearly defined workflow for resolution at HQ.

-   **[In-store operations case](https://www.servicenow.com/docs/access?context=rahi-retail-retail-in-store-operations&version=zurich&pubname=zurich-retail-industry&ft:locale=en-US)In-store operations**

Standardize the reporting, tracking, and resolution of in-store issues with the in-store operations case type in the Retail in-store operations plugin. This case type contributes to structured task assignments and tracking, reducing the time to resolution.

-   **[HQ communications case](https://www.servicenow.com/docs/access?context=rahi-retail-retail-hq-operations&version=zurich&pubname=zurich-retail-industry&ft:locale=en-US) HQ communications**

Initiate and coordinate large-scale actions across multiple stores with the HQ communications case type in the Retail HQ operations plugin. Using this case type as a parent case for in-store operations simplifies coordination efforts.


</td></tr><tr><td>

Return Merchandise Authorization

</td><td>

-   **[Return Merchandise Authorization](https://www.servicenow.com/docs/access?context=return-merchandise-authorization&version=zurich&pubname=zurich-order-management&ft:locale=en-US)**

Enable customers to create cases for defective products within a specified warranty period, which helps streamline the process.


-   **[Granular roles in Install Base Management](https://www.servicenow.com/docs/access?context=r_rolesinstalledwithcustaccessmgmt&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

Use the following new granular roles with the sn\_install\_base.install\_base\_admin role, which is installed with Customer Service Install Base Management plugin \(com.snc.install\_base\):

    -   sn\_install\_base.install\_base\_read
    -   sn\_install\_base.install\_base\_write
    -   sn\_install\_base.install\_base\_create
    -   sn\_install\_base.install\_base\_delete
    -   sn\_customerservice.customer\_data\_viewer
    -   sn\_customerservice.case.viewer
These roles provide you with more control over administrative tasks related to install base and sold product related entities.


</td></tr><tr><td>

Sales Forecasting

</td><td>

-   **[Modify forecast adjustments](https://www.servicenow.com/docs/access?context=using-sales-forecasting&version=zurich&pubname=zurich-order-management&ft:locale=en-US)**

Sales agents can modify their individual system-generated forecast values and sales managers can modify their team’s forecast projections. Adjusting forecast values provides more flexibility to sales agents and ensure a more accurate view of expected sales performance and forecasts.

-   **[Submit final forecast](https://www.servicenow.com/docs/access?context=using-sales-forecasting&version=zurich&pubname=zurich-order-management&ft:locale=en-US)**

Finalize and submit forecasts within defined submission periods to ensure accurate sales forecasts and projections. You can modify forecast values and submit the final forecast for a selected time period. After submission, the forecast roll-up displays only the locked and finalized values.

-   **[Set up sales territory hierarchy](https://www.servicenow.com/docs/access?context=sales-forecasting-terminology&version=zurich&pubname=zurich-order-management&ft:locale=en-US)**

Set up a sales territory hierarchy for specific regions to assign sales agents to defined territories. This capability improves forecasting accuracy and tracking efficiency for organizations that use territory-based sales structures.


</td></tr><tr><td>

Sales Territory Management​

</td><td>

-   **[Configuring Territory Level](https://www.servicenow.com/docs/access?context=configure-territory-levels&version=zurich&pubname=zurich-order-management&ft:locale=en-US)**

Configure territory levels to categorize territories such as regional, district, area, and global for better territory management, reporting accuracy, and alignment of sales strategies with business complexity.

-   **[Configuring the Territory Model](https://www.servicenow.com/docs/access?context=configure-territory-model&version=zurich&pubname=zurich-order-management&ft:locale=en-US)**

Configure the Territory Model to maintain a structured organizational hierarchy of territories. This model serves as the foundation for assigning territories to key customer relationship management \(CRM\) entities such as accounts, consumers, leads, and opportunities. By defining territory levels and relationships within the model, organizations can verify consistent territory assignment, streamline sales operations, and support accurate forecasting and reporting.

-   **[Configuring the Territory](https://www.servicenow.com/docs/access?context=configure-territories&version=zurich&pubname=zurich-order-management&ft:locale=en-US)**

Create territories to optimize the assignment of CRM data. Map these territories to the territory model and levels to maintain the hierarchy. Provide conditions for automated assignments, and onboard members with defined roles within a territory for restricted access.

-   **[Configuring resources for territories](https://www.servicenow.com/docs/access?context=configure-resources&version=zurich&pubname=zurich-order-management&ft:locale=en-US)**

Territory members are added with their designated responsibilities. These responsibilities determine the level of access each user has to CRM entities within the territory hierarchy.

-   **[Configure Properties](https://www.servicenow.com/docs/access?context=configure-properties&version=zurich&pubname=zurich-order-management&ft:locale=en-US)**

To put a sales territory model into use at the CRM entities, enter the sys\_id of an active sales territory model. By default, this model and its territories are utilized for sales territory assignments.

-   **[Run Assignments](https://www.servicenow.com/docs/access?context=run-assignments&version=zurich&pubname=zurich-order-management&ft:locale=en-US)**

Execute the sales territory assignment to map the CRM entities to the most appropriate territory. Each territory is evaluated against predefined territory conditions related to the CRM entity. Each territory is evaluated against its own conditions and any cascaded territory conditions associated with the CRM entity.


</td></tr><tr><td>

Security Center

</td><td>

-   **[Security Task management](https://www.servicenow.com/docs/access?context=security-task-manager&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)**

The new Platform Security Tasks enable administrators to see and manage all their platform security tasks in one place. Use this feature to prioritize, delegate, and monitor progress for tasks related to platform security across your teams. Security tasks can be automatically generated by the platform and manually created by users. Tasks can be assigned to any user who is notified the in app Notifications.

-   **[Updated overview summary pages](https://www.servicenow.com/docs/access?context=sec-center-landing&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)**

Use the overview pages for Security Center tools to understand whether you need to act on the security area these tools help you manage. The following overview pages have been updated.

    -   Security Hardening
    -   Security Scanner
    -   Security Metrics
    -   Best Practices
-   **[New information and video overlays](https://www.servicenow.com/docs/access?context=sec-center-landing&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)**

Security Center has been updated to show overlays with short feature introductory videos to help users understand what the tool can do and how to use it. These overlays are tailored to assist both new and infrequent users of Security Center.

-   **[New Auditor Suite checks](https://www.servicenow.com/docs/access?context=auditor&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)**

Added two new auditor checks:

    -   Review Public Knowledge Bases
    -   Review Public Knowledge Base Articles
-   **Granular admin role for Security Center**

The granular admin role enables developers and administrators to complete administrative configuration tasks for Security Center without requiring the full admin role.

-   ****

Use the new Access Controls console within Security Center to review and remediate access issues and misconfigurations. The Access Controls console provides enhanced visibility and control of your Access Analyzer findings, and streamlines remediation efforts by enabling you to track, prioritize, and resolve access issues by assigning tasks.

-   **Enhanced IAM Integration in Security Center**

Use the new Identity and Access Management \(IAM\) section in Security Center to access to critical IAM tools. The new section provides a comprehensive view of security metrics. This integration simplifies the administrative experience by bringing essential IAM functionality directly into Security Center, reducing the need to navigate multiple separate tools.


</td></tr><tr><td>

Security Incident Response

</td><td>

-   **[Security Incident Response Integration with Cortex XSIAM by Palo Alto Networks](https://www.servicenow.com/docs/access?context=cortex-xsiam-siem&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

As a profile admin:

    -   Create profiles for incident ingestion.
    -   Filter Cortex XSIAM incidents.
    -   Map Cortex XSIAM **Incident**, **Alert**, and **Event** fields to SIR security incident fields.
    -   Aggregate incidents to existing open security incidents to avoid having to create duplicate security incidents.
    -   Synchronize ServiceNow instance Work notes with Palo Alto Networks XSIAM comments.
-   **[Setup ServiceNow Security Operations Event Ingestion Addon for Splunk ES](https://www.servicenow.com/docs/access?context=splunk-es-addon&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

The ServiceNow Security Operations Event Ingestion Add-on for Splunk ES enables seamless integration between Splunk and ServiceNow Security Operations, allowing you to send security-related events from Splunk ES to a ServiceNow security incident.

-   **[LLM-powered SIR integration builder](https://www.servicenow.com/docs/access?context=sir-integration-builder-now-assist&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

With the ServiceNow platform's latest LLM powered integrations, you can create product-ready integration quickly. The LLM-powered integration builder has the following capabilities:

    -   Automatically generates integration code from a public API documentation.
    -   Provides guided setup built on existing capabilities.
    -   Provides easy edit and maintenance of the generated auto code.
-   **[Deny rule for phishing emails](https://www.servicenow.com/docs/access?context=urp-about&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

The security admin can add rules to prevent the conversion of phishing emails such as false positives or low-risk messages into security incidents. Any new phishing email is verified first with the deny rules to avoid unwanted security incidents.

-   **[MITRE D3FEND framework](https://www.servicenow.com/docs/access?context=mitre-d3fend-framework&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

Security administrators can now ingest MITRE D3FEND data. Security analysts can explore MITRE ATT&amp;CK and D3FEND techniques through an interactive, node-based visualization that maps attack techniques, defense techniques, and related artifacts within a Security Incident Response \(SIR\) record.

-   **[Update information in security incident related records](https://www.servicenow.com/docs/access?context=edit-related-records-in-list&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

The security analysts can now edit related records such as associated observables, for a security incident directly from the Related Records list view. Security analysts can quickly update the records without leaving their current context.

-   **[Advanced Work Assignment for Security Incident Response](https://www.servicenow.com/docs/access?context=awa-for-sir&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

Use Advanced Work Assignment \(AWA\) to streamline the security incident assignment process which ensure that critical incidents are handled by the most appropriate and available analysts. This improves overall response times and efficiency in security operations.

As an admin, configure the following:

    -   Service channels
    -   Queues
    -   Assignment rules
    -   Presence states
    -   Rejection reasons
As an analyst, do the following:

    -   Set your availability
    -   Accept or reject incoming security incidents
-   **[Prevent duplicate security incidents for IT incidents](https://www.servicenow.com/docs/access?context=si-creation&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

Prevent the creation of duplicate security incidents when ITIL users escalate an IT incident to a security incident, the system by enabling the `sn_si.disable_duplicate_security_incident` system property.

-   **[Ingest third-party risk scores](https://www.servicenow.com/docs/access?context=define-risk-score-calculator-rules-sir&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

Factor third-party risk scores into security incident risk calculation by ingesting and mapping those scores for better prioritization of high-risk threats.

-   **[Simplified adding categories and sub-categories for security incidents](https://www.servicenow.com/docs/access?context=category-management-sir&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

Admin can create categories and subcategories in Security Incident Response Workspace based on threat types, compliance requirements, or reporting needs.

Security analysts can assign these categories and subcategories to security incidents.

-   **[Security incident Details tab](https://www.servicenow.com/docs/access?context=security-incident-details-form&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

Include the **Functional Impact**, **Recoverability** and **Information Impact** fields on the Details tab of a security incident to improve triage accuracy, incident handling efficiency, and executive reporting for calculating the risk score.


-   **[Close multiple security incidents](https://www.servicenow.com/docs/access?context=close-multiple-incidents-sir&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

Close security incidents in bulk with predefined closure comments or codes to reduce the time that would be spent on manually closing individual incidents. Closure candidates might include multiple incidents with common root causes such as alert misconfiguration, duplicates, or changes in system behavior.

-   **[Process Mining for security incidents](https://www.servicenow.com/docs/access?context=sir-process-mining&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

Identify factors contributing to delays in processing SIR incidents that take a long time to close or resolve by scanning historical SIR records through Process Mining. Time-consuming factors can include multiple reassignments, prolonged hold times, and periods of inactivity. Use analysis methods to identify these factors such as multi-hop analysis or bottleneck analysis.

-   **[Send Observables to TISC](https://www.servicenow.com/docs/access?context=tisc-context-in-sir-workspace&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

Add metadata to the observables such as confidence score, Traffic Light Protocol value, notes and TISC tags before sending them to TISC.

-   **[Add indirectly linked VITs to CVEs](https://www.servicenow.com/docs/access?context=configure-mitre-att-ck-properties&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

In MITRE-ATT&amp;CK framework, identify all third-party entities \(TPEs\) associated with common vulnerabilities and exposures \(CVEs\) and then calculate and display the total number of vulnerable items \(VITs\) indirectly linked to those CVEs through the TPEs by setting the **sn\_ti.include\_cve\_vit\_indirect\_relation** system property.

-   **[Configure on-call schedules](https://www.servicenow.com/docs/access?context=on-call-schedule-sir&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

As an admin, manage on-call schedules through the following activities:

    -   Create a shift and assign or remove members to or from the shift.
    -   Create and edit on-call schedules for groups.
    -   View any group’s on-call schedule.
As an analyst, track your on-call responsibilities through the following activities:

    -   Specify your availability and preferred contact methods.
    -   View your on-call schedule.
    -   See other members of your shift.
-   **[Users accessing the same incident](https://www.servicenow.com/docs/access?context=security-incident-overview&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

When you open an incident, the initials of all the users currently accessing the same incident are displayed to avoid conflicts.

-   **[Universal search field for linking observables](https://www.servicenow.com/docs/access?context=sir-records&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

Search across all the field values of the associated observables for an incident.

-   **[CrowdStrike Next-Gen SIEM integration](https://www.servicenow.com/docs/access?context=crowdstrike-next-gen-integration-secops&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

As a Profile Admin:

    -   Discover CrowdStrike Next-Gen SIEM detections that are candidates for security incidents and automate the creation of these security incidents.
    -   Create detection profiles.
    -   Map CrowdStrike Next-Gen SIEM Detection and Events Fields to SIR security incident fields.
    -   Filter CrowdStrike Next-Gen SIEM defects.
    -   Aggregate detections to existing open security incidents so that you don't have to create duplicate security incidents.
    -   Automate CrowdStrike Next-Gen SIEM detection status updates for Security Incident Response.
    -   Synchronize CrowdStrike Next-Gen SIEM detection comments with SIR Work notes.
-   **[Create and name an event profile for the Splunk Enterprise Security event ingestion integration](https://www.servicenow.com/docs/access?context=splunk-event-ingest-create-profile-security&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**
    -   Enables bidirectional updates and closure synchronization between Splunk ES and Splunk integrations.
    -   Enables retrieval of historical, and ongoing data including closed events, with an option to pull the closed events into the ServiceNow Splunk ES instance.
    -   Receive updates for the mapped fields in SIR.
-   **[Components installed with Security Incident Response](https://www.servicenow.com/docs/access?context=installed-with-sir&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

A new Profile Admin role \(sn\_si.ingestion\_profile\_admin\) provides access to configure plugins, and to create, edit, delete, and manage profiles for the Splunk, Splunk ES, and Azure Sentinel Integration for Security Operations application.

-   **[Enhancements to relationship graphs](https://www.servicenow.com/docs/access?context=sir-relationship-graph&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

As an admin:

    -   Define default child nodes to populate in the relationship graph.
    -   Configure relationship labels.
As an analyst:

    -   Add or remove child nodes at the parent node level.
    -   Save the state of the relationship graph.
    -   Retrieve updated data.

</td></tr><tr><td>

Security Posture Control

</td><td>

-   **[Create a custom API service graph connector in the Security Posture Control workspace](https://www.servicenow.com/docs/access?context=spc-creating-sgc-template&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

Use generative AI to help your developers create SPC API connectors quickly with the Connector builder framework module in the Security Posture Control workspace. With a Now Assist skill that is included with the Now Assist for Vulnerability Response application, your developers have the option to automate steps in the Connector builder framework.

    -   You have the option to automate the steps for selecting API templates, populating request and header parameters, and response field mapping with generative AI.

**Note:** You must install Zurich Patch 4 of the Now Assist for Vulnerability Response application to have access to the generative AI skill for the Connector builder framework. See the [Now Assist for Security Incident Response \(SIR\) release notes](../security-operations/secops-now-assist-security-operations-rn.md) and [Supporting information for Now Assist for Vulnerability Response](https://www.servicenow.com/docs/access?context=supporting-information-now-assist-vr&version=zurich&pubname=zurich-security-management&ft:locale=en-US) for more information.

    -   Use your custom API connector to integrate with security tools and import asset data that is based on the unique requirements of your environment.
    -   Help your cybersecurity teams monitor your overall security posture and identify assets that are missing key security tools with the API connectors that you build.
-   **[Enhancements to policies and asset profiles included with the Security Posture Control application](https://www.servicenow.com/docs/access?context=spc-policies-overview&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

Get insights into your overall security posture and configuration gaps in your security tools using new policies and asset proﬁles that are included with the Security Posture Control application. Activate these asset proﬁles and policies in the Security Posture Control workspace so that you can identify gaps in configuration or coverage for the following tools:

    -   CrowdStrike
    -   Microsoft Intune, Defender, and SCCM
    -   HCL Big Fix
    -   SentinelOne
    -   Qualys
    -   Rapid7

</td></tr><tr><td>

Self-service and omnichannel engagement for CSM

</td><td>

-   **[Using Interaction Controls Component \(ICC\) call controls with Amazon Connect](https://www.servicenow.com/docs/access?context=amazon-connect-for-voice-calls&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

Manage Amazon Connect calls directly in the CSM Configurable Workspace voice Interaction record page. This integration supports inbound and outbound call flows, presence management, and call transfers without switching applications.

-   **[Selecting queues for outbound calls](https://www.servicenow.com/docs/access?context=select-queues-for-outbound-calls&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

Enable agents to designate a specific queue for their outbound calls directly from the keypad or the phone directory in the Global Call window to improve routing and reporting. This provides a streamlined search interface that enables agents to find and select a single queue that can be applied across all outbound dialing methods.

-   **[Integrating WhatsApp with Customer Service Management using the WhatsApp Cloud API](https://www.servicenow.com/docs/access?context=messg-integrating-whatsapp-with-csm-whatsapp-cloud&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

Connect directly to WhatsApp Cloud API for more reliable, feature-rich customer support without third-party dependencies. The key capabilities include the following:

    -   Send and receive text messages for direct customer communication.
    -   Exchange images, videos, audio files, and documents for clearer, more contextual conversations.
    -   Simplify customer input with list pickers and location sharing.
    -   View typing indicators for more natural conversational flow.
    -   Automatically capture and record customer opt-in and opt-out messages to ensure compliance with WhatsApp's messaging policies.
-   **[Defining CCaaS callbacks](https://www.servicenow.com/docs/access?context=interaction-controls-component-icc-callback-integration-features&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**
    -   Offer callers a callback option that lets them retain their position in the queue and receive a call when an agent is available. Alternatively, callers can choose a specific date and time for the callback, also known as scheduled callback.
    -   As an agent, view callback requests in the order that they're received.
-   **[CCaaS callback features](https://www.servicenow.com/docs/access?context=contact-center-intergration-with-icc-callback&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

As an agent, address callback requests from the CSM Configurable Workspace. Initiate callbacks and manage active calls with the Callback context card and Callback Actions component on the voice interaction page.

On the Callback actions component, you can use the **Call number** option to initiate a call; alternatively, the call can be initiated automatically at the end of the preview timer when enabled. After the call has ended, the **Close callback** option closes the callback interaction and changes the status to Closed complete. Agents can also retry the callback as needed.

Monitor the callback life cycle and capture the preview time that measures the time between when an agent accepts the callback request and the agent dials out the customer.

-   **[Global call list](https://www.servicenow.com/docs/access?context=ccaas-global-call-list&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

Switch between workspaces using the global call list. As a CSM agent, you can accept calls and open interaction records in supported, unsupported, or default workspaces.

-   **[Phone directory](https://www.servicenow.com/docs/access?context=ccaas-phone-directory&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

Access the embedded phone directory in your CSM Configurable Workspace via Interaction Controls Component \(ICC\) to make outbound calls to external and internal contacts.

-   **[Call resiliency](https://www.servicenow.com/docs/access?context=ccaas-call-resiliency&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

Route phone calls to the CSM Configurable Workspace without creating an interaction record, helping agents handle calls even during connectivity issues.

-   **[Voice Controls Simulator tool](https://www.servicenow.com/docs/access?context=voice-control-simulator-tool&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

Test and validate voice call UI flows in the CSM Configurable Workspace to ensure CCaaS partners have clear insights into their supported voice control capabilities.

-   **[Monitoring calls](https://www.servicenow.com/docs/access?context=call-monitoring&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

Enable supervisors to monitor, coach, and barge-in on calls in real time by integrating ServiceNow's native voice call feature within an active call interface.


</td></tr><tr><td>

Service Catalog

</td><td>

-   **[Create complex catalog items in Catalog Builder](https://www.servicenow.com/docs/access?context=create-client-scripts-in-catalog-builder&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)**

Enable catalog item creators to create complex catalog items effortlessly in Catalog Builder.

They can create, edit, or delete client scripts to build a complex catalog item. Creators can also configure questions, set dynamic and advanced reference qualifiers, and scripted default values.


-   **[Use Catalog browse component](https://www.servicenow.com/docs/access?context=catalog-builder&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)**

Use the Catalog browse component in UI Builder to add catalog item browsing in your custom pages. Drag it onto the Next Experience UI page to use the Catalog browse component.

The component enables requesters to explore and request items from various catalogs and categories, providing a hierarchical view to sort by catalog, category, or subcategory. The component provides a grid or list view for items and a search function to search for items as needed.


</td></tr><tr><td>

Service Exchange

</td><td>

-   **[Foundation data sync](https://www.servicenow.com/docs/access?context=service-bridge-v2-explore-foundation-data-sync&version=zurich&pubname=zurich-service-bridge&ft:locale=en-US)**

Reduce manual effort, and eliminate the need to share data externally by sharing selected foundational data types with your consumers on a scheduled cadence. This data transfer supports the service life cycle by providing foundational data context for operational workflows. The supported tables are CMDB \(CIs\), CMDB Relationship, Asset, User, Group, Location, Company, and Department.

-   **[Journal field framework](https://www.servicenow.com/docs/access?context=service-bridge-v2-expolre-journal-field-framework&version=zurich&pubname=zurich-service-bridge&ft:locale=en-US)**
    -   Write journal entries as a named user instead of using a generic company name to enhance authenticity and accountability.
    -   Maintain a complete historical record across instances by synchronizing previous journal entries between provider and consumer instances.
    -   Ensure that all critical operational updates remain current by mapping and synchronizing any journal-type field between provider and consumer instances.
-   **[Flow action](https://www.servicenow.com/docs/access?context=service-bridge-v2-flow-action&version=zurich&pubname=zurich-service-bridge&ft:locale=en-US)**

Ensure that Remote Tasks and Remote Record Producers continue to function correctly as you adopt newer revisions by maintaining flow compatibility across configuration revisions using four new Flow Actions that preserve mapped variable integrity.

-   **[Magic links](https://www.servicenow.com/docs/access?context=service-bridge-v2-explore-magic-link&version=zurich&pubname=zurich-service-bridge&ft:locale=en-US)**

Convert regular links sent from a provider instance into magic links that enable consumer users to directly access the linked resource in the provider instance without having to manually log in.


</td></tr><tr><td>

Service Graph Connector for Microsoft Defender for IoT \(Azure\)

</td><td>

-   **[View the class mappings available for the Service Graph Connector](https://www.servicenow.com/docs/access?context=sgc-microsoft-d4iot-azure-classes&version=zurich&pubname=zurich-operational-technology&ft:locale=en-US)**

View the available class mappings and targeted CMDB classes on the MSFT D4IoT Azure SGC Class Mappings page.

-   **[Capture firmware version of devices](https://www.servicenow.com/docs/access?context=sgc-microsoft-d4iot-azure-classes&version=zurich&pubname=zurich-operational-technology&ft:locale=en-US)**

Firmware versions of your Service Graph Connector for Microsoft Defender for IoT \(Azure\) devices are captured in the Firmware Installation \[cmdb\_firmware\_install\] table.

-   **[Use the ire\_criterion\_attribute in the OT Entity \[cmdb\_ot\_entity\] table](https://www.servicenow.com/docs/access?context=sgc-microsoft-d4iot-azure-classes&version=zurich&pubname=zurich-operational-technology&ft:locale=en-US)**

The ire\_criterion\_attribute identifies configuration items \(CIs\) for an OT entity-related entry and helps avoid entity update issues.

-   **[Actively scan device data from Microsoft Defender for IoT with the Site Mappings table](https://www.servicenow.com/docs/access?context=actively-scan-device-data-msft-azure&version=zurich&pubname=zurich-operational-technology&ft:locale=en-US)**

Access the Site Mappings table to actively scan devices from Microsoft Defender for IoT and assign them to a site in your ServiceNow instance.


</td></tr><tr><td>

Service Level Management

</td><td>

-   **[Configure the SLA timer for the First to breach source](https://www.servicenow.com/docs/access?context=sla-timer-configurations&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

Keep up with your service level expectations on incidents by configuring a First to Breach SLA timer for target-based and advanced condition-based SLAs. These configurations help you stay on top of breaches and response times.


</td></tr><tr><td>

Service Observability

</td><td>

-   **[New Service Observability integrations](https://www.servicenow.com/docs/access?context=exploring-service-observability&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

Integrate with more APM vendors to bring third-party data into Service Observability dashboards. New integrations for this release include:

    -   SolarWinds on-premise
    -   Amazon CloudWatch
    -   Microsoft Azure Monitor
    -   Splunk Observability
    -   As of 1.10, AppDynamics
    -   As of 1.10, Prometheus
    -   As of 1.10, support for Dynatrace process and process groups
-   **[Support for additional ServiceNow AI Platform data in Service Observability dashboards](https://www.servicenow.com/docs/access?context=edit-sn-based-charts&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

Add data from problem records and business app records to your dashboards. The data displayed is scoped to the service being investigated.

-   **Support for HLA data in Service Observability dashboards**

As of 1.10, add service-related log data to your dashboards.

-   **[Support for full vendor queries](https://www.servicenow.com/docs/access?context=customize-service-observability-dashboard-templates&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

Recreate any supported vendor time series chart in your Service Observability dashboard using full queries and template variables to represent entities and start and end times.As of 1.10, import selected charts from an existing AWS or Azure APM dashboard.

-   **[Use data mapping tags as variables in a chart's query](https://www.servicenow.com/docs/access?context=service-observability-template-variables&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

As of 1.10, key/tags used in a data mapping can also be used as a template variable in a chart's query.

-   **[Additional service types](https://www.servicenow.com/docs/access?context=create-and-manage-observability-data-mappings&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

Map all service offering types to APM data instead of just the types that have a technical service as a parent.

-   **[Test your data mapping](https://www.servicenow.com/docs/access?context=create-and-manage-observability-data-mappings&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

As of 1.10, you can test your data mapping before using it to create charts and dashboards.

-   **[Use any field on a service as a variable in your data mapping query](https://www.servicenow.com/docs/access?context=create-and-manage-observability-data-mappings&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

As of 1.10, when creating a data mapping, if your key represents a service, for convenience a drop down shows fields from the corresponding CI for the service, including custom fields, that can be used as a variable.

-   **[Improved data source connection flow](https://www.servicenow.com/docs/access?context=connect-an-observability-data-source&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

Create APM connections without leaving the SOW.


</td></tr><tr><td>

Service Operations Workspace for ITSM

</td><td>

-   **[Configuring Notify in Service Operations Workspace](https://www.servicenow.com/docs/access?context=configure-notify-sow&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

Configure Notify with Microsoft Teams SOW in Admin Center using the guided setup.

-   **[Visual indicators for unread messages](https://www.servicenow.com/docs/access?context=sow-itsm-workspace-chat-session-tabs-configure&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

To help agents maintain the Service Level Agreement \(SLA\) for chats, visual indicators are available on chat session tabs in the SOW. These indicators include color codes, where tabs with unread messages are highlighted in different colors. Inactive tabs display a purple background color to indicate that a message has been received. Tab colors shift to yellow and then to red to highlight critical wait times. These enhancements aim to improve customer service by ensuring quick response time, increase productivity by helping agents manage multiple chats more effectively, and reduce stress by providing clear visual cues, ultimately leading to better SLA compliance and higher service quality.

-   **[Resize modal in Service Operations Workspace](https://www.servicenow.com/docs/access?context=view-update-inc-overview-tab&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

Optimize your viewing experience by resizing the following modals in SOW:

    -   Copy incident
    -   Report knowledge gap
    -   Reopen incident
-   **[Add similar incidents to major incident record](https://www.servicenow.com/docs/access?context=managing-major-incident-sow&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

Find multiple similar incidents and add them as child incidents to a major incident or major incident candidate record from the child incident related list in the **Related records** tab of the major incident record. Similar incidents are retrieved based on the similarity solution definition that can be configured to train on various fields such as **Short description** and **Description**. Adding the similar incidents as child incidents to the major incident record ensures avoiding the creation of multiple major incident records for the same issue.

-   **[On-Call Scheduling enhancements in Service Operations Workspace](https://www.servicenow.com/docs/access?context=work-on-escalation-trigger-rules-and-policies-in-sow&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

On-call scheduling in SOW has the following enhancements:

    -   The On-call trigger rule page is enhanced to support and select subflows.
    -   The On-call trigger rule page is enhanced for supporting re-triggering escalations on configured fields such as Priority. Re-triggering is enabled whenever the value in the configured field changes.
    -   Configure custom providers as channels for on-call escalation notifications.
    -   Send the on-call escalations notifications to all stakeholders when any of the record fields configured using the on-call trigger rules are modified.
-   **[Auto-dismiss the alerts and notification in Service Operations Workspace](https://www.servicenow.com/docs/access?context=configure-alerts-auto-dismiss-sow&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

Configure the alerts and notifications in SOW to automatically dismiss within the specified time. Auto-dismissal of the alert notification reduces the user effort in manually dismissing the notification. By default, the base system has the following settings:

    -   Auto-dismiss is turned on for alert notification of type info, positive \(success\) and low and has the timeout value of three seconds.
    -   Auto-dismiss is turned off for alert notification of type critical, high, moderate, and warning.
    -   The time label is turned off and only a visual time indicator is displayed.
    -   The alert notification content is expanded.
-   **[DEX and SO view in the investigate tab](https://www.servicenow.com/docs/access?context=dex-so-metric-views-investigate-tab&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

Based on the Configuration Item \(CI\) selected in the **Investigate** tab and the rules defined in the **Investigate CI Experience Rules** \(**sn\_sow\_investigate\_ci\_ux\_rule**\) table, the Investigate tab displays the CI metrics in the UI experience dashboard view for the different CI classes:

    -   DEX view - Displayed for the cmdb\_ci\_computer CI class.
    -   SO view - Displayed for the cmdb\_ci\_service class.
You can select both the affected CIs including service and service offering and caller CIs.

-   **[SOW record page enhancements](https://www.servicenow.com/docs/access?context=view-update-inc-overview-tab&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

The SOW record page has the following enhancements:

    -   Add a clickable URL to the Summary section on the **Overview** tab of an incident record, enhancing navigation and reference capabilities. The Overview page supports URL type of field in read-only mode.
    -   Perform various DEX actions on a CI using actions from the Action library in the contextual side panel of the SOW record page.
    -   Manage user actions on the reference fields of a SOW record page with the following glide list actions:
        -   Add me - Add the logged in user to the field.
        -   Remove me - Remove the logged in user from the field.
        -   Add multiple users - Add multiple users to the field.
        -   Add multiple records - Add multiple records to the field.
-   **[View recent tasks in a knowledge article record](https://www.servicenow.com/docs/access?context=work-knowledge-article&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

Configure the **Display recent task for knowledge article** \(**glide.knowman.recent\_task.display**\) system property to view the recent task records to which the knowledge article is recently attached. You can select the task record link to open the task record in a new tab with the workspace view.

-   **[Introduction of Granular Admin roles in SOW](https://www.servicenow.com/docs/access?context=roles-in-sow&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

The following granular admin roles are introduced in SOW:

    -   sn\_sow\_admin.sn\_sow\_admin: Provides access to SOW Admin Center page for SOW configurations. Admins can use the role to configure SOW features and maintain organizational policies.
    -   sn\_sow\_inc\_sn\_incident\_sow\_admin: Provides access to SOW Admin Center pages for configurations related to Incident Management features.
    -   sn\_sow\_mim.sn\_mim\_sow\_admin: Provides access to the SOW Admin Center pages for configurations related to Major Incident Management \(MIM\) features.
    -   sn\_sow\_on\_call.sn\_on\_call\_sow\_admin: Provides access to the SOW Admin Center pages for On-Call Scheduling configurations.
    -   sn\_sow\_problem.sn\_problem\_sow\_admin: Provides access to the SOW Admin Center pages for Problem Management configurations.
-   **[View conflicts in the change request form](https://www.servicenow.com/docs/access?context=create-change-sow&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

The improved schedule and conflicts section added in the change request form displays the scheduling conflicts for a change request. If a scheduling conflict exists, conflict detection also provides details of any related blackout or maintenance schedules and other active change requests to determine the scheduling conflict. You can use the resulting information to review and modify the change request details to eliminate conflicts. You can also manually check and manage conflicts.

For more information on conflict detection, see [Conflict detection](https://www.servicenow.com/docs/access?context=c_ConflictDetection&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US).

-   **[Interaction wrap up with modeless dialog in Service Operations Workspace](https://www.servicenow.com/docs/access?context=interaction-wrap-up-sow&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

Provide agents with dedicated time after each call or chat to finalize the interaction details and wrap up their work before starting a new conversation.


</td></tr><tr><td>

Service Portal

</td><td>

-   **[Approval Info Record widget](https://www.servicenow.com/docs/access?context=approval-info-record-widget&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US)**

The Service Portal Approval Info Record widget shows details about the approval request and a full record for an approval including the activity stream.

The Approval Info Record widget and the new Now Assist Approval Assistance AI agent maintain parity. To use the new Approval Info Record widget, activate the Approval Details Page Route Map, and uptake the Approval Info Record widget in your custom page.

The new Now Assist Approval Assistance AI agent allows you to see your pending approvals, as well as the details about your pending approvals. For more information, see [Platform Approval assistance AI agent](https://www.servicenow.com/docs/access?context=platform-approval-aia&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

-   **[Configure Service Portal Approval Configuration record](https://www.servicenow.com/docs/access?context=configure-approval-assistance-ai-agent&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US)**

Configure the Service Portal Approval Configuration record to make the Approval Assistance AI agent and Approval Info Record widget work better for your specific use case.

-   **[Configure widget loading order in Service Portal](https://www.servicenow.com/docs/access?context=configure-widget-loading-order&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US)**

As an admin, configure the widget loading order to defer their loading. This feature enables faster loading of the page and makes the widgets available for interaction as they load, thus improving the user experience.


</td></tr><tr><td>

Service Reliability Management

</td><td>

-   **[Auto-generate SLOs for SRM services](https://www.servicenow.com/docs/access?context=now-assist-itom-manage-generated-slos&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

Use the SLO creator agent to generate SLOs for your SRM services. This capability is available with the AI Agents for SLO \(sn\_ai\_agents\_slo\) plugin. The agent analyzes incidents, alerts, and outage events to automatically create SLOs, helping teams adopt SLOs faster and track service reliability.

-   **[Remove a service from SRM](https://www.servicenow.com/docs/access?context=sr-remove-service&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

Starting in version 6.5.0, remove a service from SRM when you no longer need to track or monitor its reliability. Removing a service clears it from SRM views, including the Service page and Service reliability dashboard. The service remains in the Configuration Management Database \(CMDB\), and you can add it back to SRM at any time.

-   **[Create outage-based SLIs](https://www.servicenow.com/docs/access?context=sr-create-slo-sli&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

Starting in version 6.5.0, add outage-based SLIs to track real downtime and customer impact. Use them with existing alert-based SLIs for a broader view of reliability. The flow for creating service level objectives \(SLOs\), SLIs, and error budget policies is also improved to simplify setup.

-   **[Keep teams informed with notification destinations](https://www.servicenow.com/docs/access?context=create-notification-destination&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

Send notifications about error budget policy violations to notification destinations. The first supported destination is Microsoft Teams, which lets you post details in specific channels and link back to SRM for further investigation.

-   **[Monitor service reliability in a dashboard](https://www.servicenow.com/docs/access?context=sr-service-dashboard-visualizations&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

Use the Service reliability dashboard to monitor and manage service performance. The dashboard offers multiple visualizations to help you track error budgets, monitor SLOs, and identify issues across your services. Starting in version 6.4.1, monitor reliability using interactive charts and a new service level objective \(SLO\) table in the Service reliability dashboard.

-   **[Customize team approval settings](https://www.servicenow.com/docs/access?context=sr-add-approval-teams&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

Customize team governance with more flexibility and less manual effort. You can assign different approval teams for new and existing team requests. The customization options are also fully available in the Service Operations Workspace Admin Center and no longer require manual setup in the Catalog Builder.


</td></tr><tr><td>

ServiceNow AI Lens

</td><td>

-   **[ServiceNow AI Lens UI enhancement](https://www.servicenow.com/docs/access?context=servicenow-lens-explore&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Launch the ServiceNow AI Lens scanner window by using the context defined in the Lens actions or as a standalone application. You can preview the gathered insights or extracted data. You can also see the logged-in user and instance details.

-   **[Use Lens actions to customize Lens behavior](https://www.servicenow.com/docs/access?context=servicenow-lens-actions&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**
    -   Define Lens behavior depending on how ServiceNow AI Lens is triggered and what context is set. With Lens actions, you can customize how a classic form is auto-filled. You can define default instructions, trigger options, custom context, transform response logic, and post processing instructions for the ServiceNow AI Lens execution.

For example, you can define a Lens action that is used when Lens is triggered from an instance to populate a form of a table. You can also define form fields that must be used as context.

    -   As part of your integration logic, configure a Lens action as one of the steps to invoke a ServiceNow AI Lens service from any part of the ServiceNow AI Platform, such as a workspace form or portal.
-   **[Use ServiceNow AI Lens in Virtual Agent](https://www.servicenow.com/docs/access?context=enabling-lens-for-virtual-agent&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Trigger ServiceNow AI Lens from a Virtual Agent conversation by using the ServiceNow AI Lens topic in Virtual Agent.

-   **[Auto-attach images to a record](https://www.servicenow.com/docs/access?context=servicenow-lens-actions&version=zurich&pubname=zurich-intelligent-experiences&section=create-sn-lens-recipe&ft:locale=en-US)**

View captured images that are automatically attached to an auto-filled record using ServiceNow AI Lens. You can view the images to understand the source of the auto-filled information.

-   **[New third-party AI model provider options available for all Now Assist applications](https://www.servicenow.com/docs/access?context=exploring-large-language-models&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

Use Google Gemini and Anthropic Claude on AWS as AI model providers for ServiceNow AI Lens in addition to Azure OpenAI.


</td></tr><tr><td>

ServiceNow AI Platform core feature

</td><td>

-   **[Hierarchical queries in condition builders](https://www.servicenow.com/docs/access?context=data-hierarchies&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

Simplify and build queries with fewer conditions using existing hierarchical data in a table. You can also define new hierarchical relationships between records that are in the same table.

-   **[Dynamic namespaces](https://www.servicenow.com/docs/access?context=create-dynamic-namespace&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

Define categories and attributes once and reuse them using dynamic namespaces across multiple tables and dynamic attribute store fields. A dynamic namespace is automatically created when you add a dynamic attribute store field.

-   **[Experimentation framework](https://www.servicenow.com/docs/access?context=experimentation-framework&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

Help enable innovation by trying new ServiceNow® feature variants in your instance. Only single customer instances or Gen AI Innovation Program participants have early access to new innovations via experimentation framework. You can opt out of specific experiments or turn off the framework entirely.

-   **[Audit Management Console and audit retention](https://www.servicenow.com/docs/access?context=audit-mgmt-console&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)**

Simplify your audit data management and configuration by using the Audit Management Console module. It includes a new Retention option, which automates and simplifies the deletion of audit data based on your requirements.

-   **[Monitor requestors' API usage rates through the Inbound API Integration Usage dashboard](https://www.servicenow.com/docs/access?context=inbound-api-integration-usage-dashboard&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)**

Inbound integrations track web service requests for OAuth registered applications and user accounts making those requests.

-   **[Use schemas to define the structure and format of REST API responses and requests](https://www.servicenow.com/docs/access?context=define-scripted-rest-api-schema&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)**

When you define a schema in the ServiceNow AI Platform, the schema can be used to define the structure of requests and responses within the associated REST API. The schema data for the requests and responses is then available in the exportable OpenAPI specification for the API.

-   **[Automatically generate request definitions for scripted REST API resources](https://www.servicenow.com/docs/access?context=autogenerate-api-request-definitions&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)**

Use sample requests made to an API resource to generate request header associations, query parameter associations, and a request schema for that resource and the related scripted REST API service.


</td></tr><tr><td>

ServiceNow IDE

</td><td>

-   **[Clone a repository that contains multiple applications](https://www.servicenow.com/docs/access?context=clone-git-repository-servicenow-ide&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

Clone a Git repository that contains multiple applications that support development in source code. The repository must contain at least one `package.json` file and one `now.config.json` file.

-   **[Default to using the latest version of the ServiceNow SDK in new or converted applications](https://www.servicenow.com/docs/access?context=servicenow-ide-properties&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

Configure whether to use the bundled version or the latest version of the ServiceNow SDK when creating or converting applications in the ServiceNow IDE with the **sn\_glider.default\_to\_bundled\_sdk** system property. By default, the latest version of the ServiceNow SDK is used.


</td></tr><tr><td>

ServiceNow SDK

</td><td>

-   **[Flow API - ServiceNow Fluent](https://www.servicenow.com/docs/access?context=servicenow-fluent-api-reference&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

Use the Flow API to create flows and subflows \[sys\_hub\_flow\] that automate business processes with reusable multiple-step components.

-   **[Service Catalog API - ServiceNow Fluent](https://www.servicenow.com/docs/access?context=servicenow-fluent-api-reference&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

Use the Service Catalog API to define catalog items \[sc\_cat\_item\] and related aspects of service catalogs.

-   **[Email Notification API - ServiceNow Fluent](https://www.servicenow.com/docs/access?context=servicenow-fluent-api-reference&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

Use the Email Notification API to define notifications \[sysevent\_email\_action\] that send automated emails.

-   **[Service Level Agreement API - ServiceNow Fluent](https://www.servicenow.com/docs/access?context=servicenow-fluent-api-reference&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

Use the Service Level Agreement API to define service level agreements \(SLAs\) \[contract\_sla\] that set the amount of time for a task to reach a specified condition.

-   **[Dashboard API - ServiceNow Fluent](https://www.servicenow.com/docs/access?context=servicenow-fluent-api-reference&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

Use the Dashboard API to define dashboards \[par\_dashboard\] for organizing and sharing data visually.

-   **[Workspace API - ServiceNow Fluent](https://www.servicenow.com/docs/access?context=servicenow-fluent-api-reference&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

Use the Workspace API to define configurable workspace experiences for organizing and sharing data visually.

-   **[Allow access to ServiceNow APIs for third-party modules](https://www.servicenow.com/docs/access?context=building-applications-source-code&version=zurich&pubname=zurich-application-development&ft:locale=en-US#application-structure)**

Configure which third-party library modules to identify as trusted and have access to ServiceNow APIs with the `trustedModules` parameter in an application's `now.config.json` file.


-   **[Import Sets API - ServiceNow Fluent](https://www.servicenow.com/docs/access?context=fluent-import-sets-api&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

Use the Import Sets API to define transform maps \[sys\_transform\_map\] that specify how to transform and map data from the import set staging table to target tables.

-   **[UI Policy API - ServiceNow Fluent](https://www.servicenow.com/docs/access?context=fluent-ui-policy-api&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

Use the UI Policy API to define user interface policies \[sys\_ui\_policy\] that dynamically change the behavior of information on a form and control custom process flows for tasks.

-   **[Attach user images to records from source code](https://www.servicenow.com/docs/access?context=fluent-constructs&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

Attach user images to records associated with metadata defined in source code with the `Now.attach` construct.

-   **[Use utility functions for additional type validation](https://www.servicenow.com/docs/access?context=servicenow-fluent-api-reference&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

Use utility types that help validate values for properties that support the Duration \(Duration\(\)\), Time \(Time\(\)\), Field List \(FieldList\(\)\), and Template Value \(TemplateValue\(\)\) field types in ServiceNow Fluent APIs. Utility types provide validation at build time for tables both within and outside of an application.

-   **[Generated ServiceNow Fluent code organized in taxonomy-based directories](https://www.servicenow.com/docs/access?context=building-applications-source-code&version=zurich&pubname=zurich-application-development&ft:locale=en-US#application-structure)**

Configure a custom directory structure for metadata transformed into ServiceNow Fluent code with the `taxonomy` parameter in an application's `now.config.json` file. By default, generated ServiceNow Fluent files are organized in a taxonomy-based directory structure within the `fluent/generated` directory.


-   **[Specify which files to build as JavaScript modules](https://www.servicenow.com/docs/access?context=building-applications-source-code&version=zurich&pubname=zurich-application-development&ft:locale=en-US#application-structure)**

Configure which files to include or exclude when building JavaScript modules with the `serverModulesIncludePatterns` and `serverModulesExcludePatterns` parameters in an application's `now.config.json` file.


-   **[Develop a user interface with React](https://www.servicenow.com/docs/access?context=ui-development-react&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

Develop a user interface with the React library and the UI Page API to build a full-stack application in source code.

-   **[Script Action API - ServiceNow Fluent](https://www.servicenow.com/docs/access?context=fluent-script-action-api&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

Use the Script Action API to define script actions \[sysevent\_script\_action\] that run when an event occurs.

-   **[Script Include API - ServiceNow Fluent](https://www.servicenow.com/docs/access?context=fluent-script-include-api&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

Use the Script Include API to define script includes \[sys\_script\_include\] that store JavaScript functions and classes for use by server-side scripts.

-   **[Service Portal API - ServiceNow Fluent](https://www.servicenow.com/docs/access?context=fluent-service-portal-api&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

Use the Service Portal API to create custom widgets \[sp\_widget\] for portal pages.

-   **[UI Action API - ServiceNow Fluent](https://www.servicenow.com/docs/access?context=fluent-ui-action-api&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

Use the UI Action API to configure custom user interface actions \[sys\_ui\_action\], such as buttons, links, and context menu items on forms and lists.

-   **[UI Page API - ServiceNow Fluent](https://www.servicenow.com/docs/access?context=fluent-ui-page-api&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

Use the UI Page API to configure custom user interface pages \[sys\_ui\_page\] that display forms, dialogs, lists, and other UI components.

-   **[Download application metadata from an instance](https://www.servicenow.com/docs/access?context=servicenow-sdk-cli-commands&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

Download application metadata \(XML\) from a ServiceNow instance to compare it with the metadata in your local application using the `now-sdk download` command.

-   **[Clean or package an application](https://www.servicenow.com/docs/access?context=servicenow-sdk-cli-commands&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

Remove the build artifacts that were output with the previous build using the `now-sdk clean` command. You can also package the build artifacts that were output with the previous build into an installable ZIP file using the `now-sdk pack` command.


</td></tr><tr><td>

ServiceNow Studio

</td><td>

-   **[Add AI files to your apps in ServiceNow Studio](https://www.servicenow.com/docs/access?context=servicenow-studio-file-navigator-taxonomy&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

You can add agentic workflows, AI Agents, and skills to your apps in ServiceNow Studio.

-   **[Link an app to source control in ServiceNow Studio](https://www.servicenow.com/docs/access?context=link-app-to-source-control&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

Use source control operations on the App details page to link an application to a Git repository.

-   **[App details page](https://www.servicenow.com/docs/access?context=app-details-page&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

View and manage app files and metadata on the enhanced App details page. You can also link your app to source control from the App details page and create new files for your application.

-   **[Focus the Navigator panel on an app or app file](https://www.servicenow.com/docs/access?context=qs-focus-navigator-panel-on-app-app-file&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

Improve efficiency as you work in ServiceNow Studio by focusing the Navigator panel on any file or application open in an integrated tab.

-   **[Personalize your UI with dark theme](https://www.servicenow.com/docs/access?context=servicenow-studio-user-interface&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

Dark theme is now supported in ServiceNow Studio. Access user preferences to switch between dark and light mode on your instance.

-   **[Create an application in ServiceNow Studio](https://www.servicenow.com/docs/access?context=create-an-application-in-servicenow-studio&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

As of version 28.2.1, you can use Now Assist or Creator Studio to begin creating your applications. You can also view the App Gallery for more inspiration.

-   **[Elevate your role in ServiceNow Studio](https://www.servicenow.com/docs/access?context=elevate-your-role-in-servicenow-studio&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

As of version 28.2.1, you can elevate your role to security\_admin without having to leave ServiceNow Studio. Users with the security\_admin role can make changes to other roles and to access control lists \(ACLs\).

-   **[ServiceNow Studio personas and roles](https://www.servicenow.com/docs/access?context=sn-studio-personas-roles&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

As of version 28.2.1, several new granular admin roles enable developers to complete administrative configuration tasks without requiring the full admin role in ServiceNow Studio.

-   **[Opening files in your preferred editor](https://www.servicenow.com/docs/access?context=opening-files-in-your-preferred-editor&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

As of version 28.2.1, for file types that open in a builder, decide whether you want to edit the file in the builder or in the classic UI16 view.

-   **[Bookmark lists in ServiceNow Studio](https://www.servicenow.com/docs/access?context=bookmark-lists-in-sns&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

As of version 28.2.1, access your favorite lists by bookmarking them.

-   **[AppSee support in ServiceNow Studio](https://www.servicenow.com/docs/access?context=exploring-servicenow-studio&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

As of version 28.2.1, AppSee is supported in ServiceNow Studio.

-   **[Create an app file in ServiceNow Studio](https://www.servicenow.com/docs/access?context=sn-studio-create-app-file&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

As of version 28.2.1, you can create files directly from an app open in the Navigator panel.


</td></tr><tr><td>

ServiceNow Vault

</td><td>

-   **[ServiceNow Vault console dashboard](https://www.servicenow.com/docs/access?context=vault-dashboard&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)**
    -   Manage and monitor cloud encryption metrics.
    -   Get AI guidance using the Ask Now Assist panel.
    -   Explore more detail for each metric.

-   **[ServiceNow Vault console dashboard](https://www.servicenow.com/docs/access?context=vault-dashboard&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)**

Monitor your sensitive data in ServiceNow Vault with a comprehensive dashboard. The dashboard view shows metrics from each of the ServiceNow Vault tools and provides easy access to them.

-   **[Guided Vault](https://www.servicenow.com/docs/access?context=guided-vault&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)**

Use guided setup to quickly start using ServiceNow Vault on the following applications:

    -   [Financial Services](https://www.servicenow.com/docs/access?context=fso-overview&version=zurich&pubname=zurich-financial-services-operations&ft:locale=en-US)
    -   [Customer Service Management](https://www.servicenow.com/docs/access?context=c_CustomerServiceManagement&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)

</td></tr><tr><td>

Sidebar

</td><td>

-   **[Sidebar](https://www.servicenow.com/docs/access?context=sidebar-landing&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)**

Use threaded replies to answer Sidebar messages without adding clutter to the main discussion.


</td></tr><tr><td>

Smart Assessment Engine

</td><td>

-   **[Collaboration in assessments](https://www.servicenow.com/docs/access?context=collaboration-in-assessments&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

Enhance assessments with the new collaboration feature, enabling owners to add multiple contributors to work together in real time. This update enables assessors to collaborate efficiently by adding several contributors to an assessment. Real-time updates reflect each contributor's changes, and presence indicators show who is present on the assessment.

-   **[Normalization in assessments](https://www.servicenow.com/docs/access?context=normalization-in-assessment&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

Adjust assessment scores to a common scale to promote fair comparison and prioritization. This normalization process helps standardize these measurements, enabling different metrics or scores to be evaluated on the same scale.

-   **[Creating code questions](https://www.servicenow.com/docs/access?context=sae-q-code-create&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

Capture data quickly and accurately from physical documents using a new barcode and QR code question type for assessments. By scanning barcodes or entering QR codes, the system can instantly retrieve and input relevant information.

-   **[Creating an assessment template from legacy metric types](https://www.servicenow.com/docs/access?context=sae-asmnt-template-migrating&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

Migrate question dependencies with an improved migration utility, which now supports the check box question type and conditional visibility criteria defined on templates.

-   **[Combining assessments and copying responses](https://www.servicenow.com/docs/access?context=combine-assessments&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

Combine assessments from different templates into a single, streamlined view. Eliminating the need to open each assessment separately, preserving context, and improving efficiency.


</td></tr><tr><td>

Software Asset Management

</td><td>

-   **[Retrieve detailed subscription and consumption data across your entire organization with the Docusign integration](https://www.servicenow.com/docs/access?context=integrate-with-docusign-org&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

Get insights into detailed subscription and consumption data across your organization by integrating Docusign with the Software Asset Management application. You can now access data at both the account and organization levels, giving you a centralized view of envelope activity and usage. This enhancement helps you better monitor Docusign consumption and optimize your license use.

-   **[Streamline the authentication process for Salesforce CRM integration](https://www.servicenow.com/docs/access?context=integrate-with-salesforce-crm&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

Experience seamless data flow between the Software Asset Management application and Salesforce CRM. This updated feature supports the OAuth 2.0 Client Credentials grant type, eliminating manual authentication, and uses a secure machine-to-machine method to ensure efficient and uninterrupted data exchange.

-   **[Manage license compliance and optimization for Adobe Cloud services through Adobe Guided Setup](https://www.servicenow.com/docs/access?context=playbook-entitlementsetup-workspace&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

Simplify setting up Adobe SaaS integration using the Adobe Guided Setup. The Guided Setup provides step-by-step guidance to set up the Adobe integration with the Software Asset Management application that supports license compliance and optimization for Adobe Cloud services.

-   **[Gain the flexibility to exclude certain SaaS subscriptions \(users and subscription identifiers\) from license calculations](https://www.servicenow.com/docs/access?context=subscription-exclusions&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

Optimize your licensing costs with the ability to exclude certain low-value and high-volume subscriptions from ServiceNow's licensing calculations.

-   **[Optimize subscription licensing for specific SaaS offerings and editions via Single Sign-On \(SSO\) integrations](https://www.servicenow.com/docs/access?context=integrate-with-azure-ad&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

Leverage the enhanced SSO integration that supports tracking subscriptions for specific SaaS offerings and editions. This update enables you to map SSO groups to software models for the specific offerings or editions and optimally license users based on their access.

-   **[Improve the security of Microsoft-related integrations with the enhanced support for application type permissions](https://www.servicenow.com/docs/access?context=microsoft-publisher-pack&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

Enhance Microsoft SaaS integration security with the added support for application-type permissions. This feature includes SSO integration with Microsoft Entra ID, Microsoft Dynamics 365 and Power Apps, and Microsoft 365.

-   **[Monitor database memory for your SAP HANA Database with SAP HANA Database integration](https://www.servicenow.com/docs/access?context=add-sap-connection&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

Manage memory allocations and licensing costs for your SAP HANA Database by integrating with the Software Asset Management application. Data populated through this approach helps in effective license reconciliation based on the peak memory usage of the SAP HANA Database.

-   **[Receive more frequent updates from the Software Asset Management Content Service](https://www.servicenow.com/docs/access?context=sam-content-updates&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

Gain the benefit of twice-weekly shipments of the Content Library. This increase in the update frequency delivers faster Content Service to your ServiceNow instance.

-   **[Improve reclamation candidate selection for Microsoft 365 by considering mailbox and OneDrive sizes](https://www.servicenow.com/docs/access?context=o365-usage-activity&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

Enhance the process of reclamation candidate selection for Microsoft 365 downgrade opportunities by considering three key factors: product usage, mailbox storage, and Microsoft OneDrive storage. Considering all these aspects enables more accurate and effective reclamation decisions.

-   **[Leverage the Flow Designer for reclamation workflow updates](https://www.servicenow.com/docs/access?context=reclaiming-software-sam&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

Manage the reclamation process using the functionality migrated to the Flow Designer. The Flow Designer migration includes additional error handling features to enable a more intuitive and efficient way to manage the reclamation process.

-   **[Automatically identify and license Microsoft SQL Server high availability configurations](https://www.servicenow.com/docs/access?context=microsoft-sql-server-ha-configurations&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

Use the Software Asset Management publisher pack for Microsoft to automatically identify and license Microsoft SQL Server deployments in high availability configurations, such as Always On availability groups. This capability enables the Software Asset Management application to automatically classify each replica within a configuration as either active or passive, resulting in more accurate license compliance for Microsoft SQL Server.

-   **[Manage licensing for Microsoft Server products on Microsoft Hyper-V virtualization technology](https://www.servicenow.com/docs/access?context=microsoft-server-licensing-hyper-v-virtualization-technology&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

Use the Software Asset Management publisher pack for Microsoft to track and manage licensing for Microsoft Server products, such as Microsoft Windows Server and Microsoft SQL Server, on Microsoft Hyper-V virtualization technology. Track license usage and determine your license compliance position so that you can better optimize your licensing costs.

-   **[Apply preferred licensing assignments to Microsoft software products that are deployed on clusters](https://www.servicenow.com/docs/access?context=apply-preferred-licensing-assignments-microsoft-clusters&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

Define and apply preferred cluster licensing assignments to the Microsoft software products that are deployed on your hypervisor clusters. By using a preferred cluster licensing assignment, you can choose whether you want to license these software products at either the physical host layer or the virtual layer, helping you better align with your organization’s predetermined licensing strategy. Built-in validations help verify that your licensing strategy setup complies with the relevant Microsoft licensing requirements.

-   **[Manage the life-cycle risks of a software product based on its add-on or optional support](https://www.servicenow.com/docs/access?context=software-models-and-entitlements&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

Gain insight into the extended life cycle of a software product when you purchase an add-on or optional support. Each time you indicate that a software product has an add-on or optional support, the Software Asset Management application extends the life-cycle dates of that product, as defined by the add-on or optional support. Use these extended life-cycle dates to identify and plan for your end-of-life \(EOL\) risks.

-   **[Manage licensing for VMware vSphere Standard \(VVS\) and VMware vSphere Essentials Plus \(VVEP\)](https://www.servicenow.com/docs/access?context=vmware-publisher-pack&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

Following the updates to VMware's licensing policy, use the Software Asset Management publisher pack for VMware to track and manage licensing for VMware vSphere Standard \(VVS\) and VMware vSphere Essentials Plus \(VVEP\), which are updated suite-based product offerings for VMware vSphere. With these updated product offerings, you can measure compliance and optimize licensing for multiple VMware vSphere products under a single subscription.

In addition, the publisher pack can account for the number of cores and the licensing minimums when calculating licensing requirements for VVS and VVEP.

-   **[Gain expanded insight into the content library information through content dashboard analytics](https://www.servicenow.com/docs/access?context=content-search-portal&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

Gain in-depth information related to various content tables and trends in content change from the enhanced Content Library portal. The introduction of numeric widgets, line graphs, bar charts, and content-specific tabs provides complete visibility to content shipped and analyze content coverage. The expanded search feature with additional filter options lets you view the records for a particular period or release.

-   **[Efficiently manage user allocations in bulk using group allocations](https://www.servicenow.com/docs/access?context=group-user-allocation&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

Allocate licenses to user groups instead of individual users for a software entitlement using the group allocation feature for the user-based licensing metric software. Group allocation feature enables Software Asset Management managers to streamline and manage the license allocation process efficiently. User allocation is created for the group members based on the availability of unallocated licenses. Any changes made to the composition of the user group automatically updates the license allocation.

-   **[Use the enhanced License Usage view for expanded insights on your license compliance](https://www.servicenow.com/docs/access?context=sam-workspace-workbench&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

Conduct a deeper analysis of your publisher compliance using both the list view and the card view in the License usage view. You can save and share the data by exporting the list view in multiple file formats. View integrated health check results, license usage analysis, and learn why a retired or stale CI is using a license. Furthermore, to avoid clutter on the Publisher details page, software model results are only shown for software models that have entitlements.

-   **[Seamlessly continue with the entitlement import process even when PPNs are missing](https://www.servicenow.com/docs/access?context=import-entitlements-workspace&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

Continue with the entitlement import process by automatically creating software models when both PPNs and software models are missing. Software models are automatically generated based on the publisher and product details.

-   **[Use flexible reporting capabilities to gain deeper insights into your Effective License Position \(ELP\)](https://www.servicenow.com/docs/access?context=elp-grouping-byconsumption&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

Improve analysis of your ELP with flexible reporting on reconciliation results. Reports can be run on existing reconciliation groups or customer-defined groups, and the report data can be organized by unique combinations of group, subgroup, publisher, product, version, and edition. For each combination, the average cost is calculated and provides the total number of required licenses. The results are presented in a structured format for easy analysis and reporting.


</td></tr><tr><td>

Source-to-Pay Operations Integrations

</td><td>

-   **[Source-to-Pay integration with SAP](https://www.servicenow.com/docs/access?context=source-to-pay-sap-integration&version=zurich&pubname=zurich-source-to-pay-operations&ft:locale=en-US)**
    -   You can use this integration to perform Integration Hub actions for purchase requisition, purchase order, receipt, and invoices.
    -   You can also perform the following:
        -   Create, update, or cancel purchase orders in SAP ECC and SAP S4 HANA.
        -   Create good receipts in SAP ECC and SAP S4 HANA.
        -   Create invoices in SAP ECC and SAP S4 HANA.
-   **[Source-to-Pay integration with Oracle EBS](https://www.servicenow.com/docs/access?context=source-to-pay-oracle-ebs-integration&version=zurich&pubname=zurich-source-to-pay-operations&ft:locale=en-US)**
    -   You can use this integration to perform Integration Hub actions for Invoices, cost centers, product models, payment terms, purchasing organizations, departments, GL accounts, currencies, FX rates, invoice payment details, suppliers, plant addresses, and legal entities.
    -   You can also perform the following:
        -   Create, update, or cancel purchase orders in Oracle EBS.
        -   Create good receipts in Oracle EBS.
        -   Create invoices in Oracle EBS.
-   **[Source-to-Pay integration with Coupa](https://www.servicenow.com/docs/access?context=source-to-pay-coupa-integration&version=zurich&pubname=zurich-source-to-pay-operations&ft:locale=en-US)**

You can use this integration to perform Integration Hub actions for loading primary data, supplier management, purchase requisition, purchase order, receipt, invoice, and sourcing. You can also look up Legal Entity, Currency, and Supply details respectively.

-   **[Source-to-Pay integration with SAP Ariba](https://www.servicenow.com/docs/access?context=source-to-pay-integration-sap-ariba&version=zurich&pubname=zurich-source-to-pay-operations&ft:locale=en-US)**

You can use this integration to perform Integration Hub actions for invoices, cost centers, payment terms, purchasing organizations, departments, GL accounts, currencies, FX rates, invoice payment details, suppliers, and legal entities. You can also create good receipts in SAP Ariba.


</td></tr><tr><td>

Sourcing and Procurement Operations

</td><td>

-   **[Multi-currency support in Shopping Hub](https://www.servicenow.com/docs/access?context=sh-multicurrency-overview&version=zurich&pubname=zurich-source-to-pay-operations&ft:locale=en-US)**

Enable multi-currency display across approval-related views, including To-Dos, tasks, email notifications, and the Bundles page. Currency values are shown in both the approver’s local currency and the original supplier currency where applicable. The local currency is displayed as the primary value, with the original currency shown as a secondary reference. This display format provides consistent currency visibility for approvers during review.

-   **[Decimal quantity support for service-based purchases in Shopping Hub](https://www.servicenow.com/docs/access?context=decimal-support-services&version=zurich&pubname=zurich-source-to-pay-operations&ft:locale=en-US)**

Enable requesters to enter and edit decimal quantities for service-based purchase requisitions and purchase orders without validation errors. Decimal quantities are supported only for services to maintain data integrity. Decimal quantities for goods are not supported and return a clear validation message. This validation logic is consistent across Shopping Hub and Employee Center.

-   **[Automatically assign categories during SR and PR creation](https://www.servicenow.com/docs/access?context=automatically-assign-categories&version=zurich&pubname=zurich-source-to-pay-operations&ft:locale=en-US)**

Automatically classify service requests, purchase requisitions, and purchase orders into the correct spend categories using the Spend categorization agent. This classification process reduces manual classification effort and improves consistency across procurement workflows.

-   **[Purchase on behalf of another user in Shopping Hub](https://www.servicenow.com/docs/access?context=purchase-on-behalf-sh&version=zurich&pubname=zurich-source-to-pay-operations&ft:locale=en-US)**

Enable users to purchase on behalf of others without requiring delegate configuration in Shopping Hub. Users can manage individuals they are authorized to purchase for, directly within the buying experience. Purchases made on behalf of others are visible through filtering by business owner in the My Purchases view.

-   **[Purchase requisition line-level questions in Shopping Hub](https://www.servicenow.com/docs/access?context=prl-question-shoppinghub&version=zurich&pubname=zurich-source-to-pay-operations&ft:locale=en-US)**

Create configurable, line-level questions during checkout in Shopping Hub. These questions are defined in Catalog Builder and are specific to certain products or product categories.

-   **[Multi-currency support in Shopping Hub](https://www.servicenow.com/docs/access?context=sh-multicurrency-overview&version=zurich&pubname=zurich-source-to-pay-operations&ft:locale=en-US)**

View and select your local currency while shopping for products in Shopping Hub to provide a seamless multi-currency experience.

-   **[Category management tab](https://www.servicenow.com/docs/access?context=category-mgmt-tab&version=zurich&pubname=zurich-source-to-pay-operations&ft:locale=en-US)**

Access a unified, filter-based view of category performance across spend, savings, pipeline projects, contracts, purchase orders, and suppliers.

-   **[Category analytics](https://www.servicenow.com/docs/access?context=spo-category-analytics&version=zurich&pubname=zurich-source-to-pay-operations&ft:locale=en-US)**

View savings opportunities across the sourcing pipeline using the Savings dashboard in the Category Analytics module of the Source-to-Pay Workspace.

-   **[Pipeline management tab](https://www.servicenow.com/docs/access?context=pipeline-mgmt-tab&version=zurich&pubname=zurich-source-to-pay-operations&ft:locale=en-US)**

Gain insights into savings and pipeline projects to enhance visibility, tracking, and collaboration across teams.

-   **[Report savings when awarding multiple suppliers](https://www.servicenow.com/docs/access?context=report-savings-multiple-suppliers&version=zurich&pubname=zurich-source-to-pay-operations&ft:locale=en-US)**

Enter the spend and savings data for the sourcing event associated with the pipeline project when awarding multiple suppliers.

-   **[Create a pipeline project from an expiring contract](https://www.servicenow.com/docs/access?context=create-pipeline-expire-contract&version=zurich&pubname=zurich-source-to-pay-operations&ft:locale=en-US)**

Create a pipeline project directly from an expiring contract using a guided, decision-based workflow.

-   **[Submit multi-product sourcing requests](https://www.servicenow.com/docs/access?context=multi-product-sourcing-intake-with-third-party-integration&version=zurich&pubname=zurich-source-to-pay-operations&ft:locale=en-US)**

Submit sourcing requests with multiple products in a single sourcing intake form, and the third-party sourcing solution will automatically create separate sourcing events for each product.

-   **[Manage third-party RFx tasks in Employee Center](https://www.servicenow.com/docs/access?context=third-party-rfx-task-management-for-requestors&version=zurich&pubname=zurich-source-to-pay-operations&ft:locale=en-US)**

View and manage third-party Request for anything \(RFx\) tasks in the Employee Center and navigate to the third-party sourcing tool to review, publish, and award RFx.

-   **[Sourcing and Procurement Operations integration with IT Asset Management](https://www.servicenow.com/docs/access?context=spo-itam-better-together&version=zurich&pubname=zurich-source-to-pay-operations&ft:locale=en-US)**

The Asset Management Integration for Sourcing and Procurement Operations plugin \(com.snc.sn\_spend\_asset\) provides an integration between IT Asset Management \(ITAM\) and Sourcing and Procurement Operations \(SPO\) applications, enhancing operational efficiency. This integration enables asset managers to access catalog items, including those items without assigned prices, directly within the ITAM workspace. By enabling procurement actions without switching platforms, it streamlines workflows and improves the user experience.

-   **[Sourcing Pipeline Management](https://www.servicenow.com/docs/access?context=spo-sourcing-pipeline-mgmt&version=zurich&pubname=zurich-source-to-pay-operations&ft:locale=en-US)**

Sourcing Pipeline Management introduces a centralized approach to managing sourcing projects, enabling you to create, track, and manage sourcing activities in one place. It includes workflow automation to reduce manual effort, improves visibility into sourcing activities, and supports tracking and forecasting of cost savings.

-   **[Using Shopping Hub](https://www.servicenow.com/docs/access?context=use-shoppinghub-portal&version=zurich&pubname=zurich-source-to-pay-operations&ft:locale=en-US)**

Enter decimal quantities when creating purchase requisitions for service items using quick or full checkout flows in Shopping Hub. Edit service acknowledgments with decimal values to enable more precise tracking of service consumption.

-   **[Purchasing tasks and procurement cases](https://www.servicenow.com/docs/access?context=purchasing-tasks&version=zurich&pubname=zurich-source-to-pay-operations&ft:locale=en-US)**

Review and respond to proposed case resolutions based on conditions defined in the decision tables before the case is permanently closed. When a fulfiller marks a case as resolved, the system now automatically transitions the case status to Awaiting Acceptance, pausing closure until the requester takes action. Requesters are notified via email with actionable buttons and can also accept or reject the resolution directly through the Employee Center. This notification helps to ensure that unresolved issues are addressed before a case is closed, improving resolution accuracy and customer satisfaction.


</td></tr><tr><td>

Strategic Planning

</td><td>

-   **[Strategic Planning and AI Control Tower](https://www.servicenow.com/docs/access?context=better-together-with-other-apps-spw&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)**

Categorize your strategic priorities, goals, planning items, and execution items—projects and demands as Artificial Intelligence to track and monitor strategy progress from the AI Control Tower workspace.

Use the **Type** field for strategic priorities, the **Category** field for goals, the **Investment type** field for planning items - to classify them as Artificial Intelligence and monitor their progress in the AI Control Tower workspace.

-   **[Integrate Enterprise Agile Planning \(EAP\) with Atlassian Jira](https://www.servicenow.com/docs/access?context=spw-jira-landing&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)**

Facilitate execution of the work planned in EAP and executed in Jira. With this integration, enable seamless tracking of work across tools with bidirectional sync between Jira and EAP. Key updates made in one system, such as a status change or field update for Epics and Stories, will automatically reflect in the other. This integration ensures your team can collaborate and track development efforts without switching contexts, reducing manual effort and improving visibility across platforms.

-   **[Enterprise Agile Planning \(EAP\) integration with CWM](https://www.servicenow.com/docs/access?context=agile-sprint-planning-in-cwm&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)**

Enhance visibility, planning, and execution for your teams with seamless integration between EAP and CWM.

For Agile teams managing non-agile work items such as incidents and change tasks, this integration bridges the gap by automatically creating a dedicated Space and Board in CWM. Agile work is seamlessly brought over via Connected Work, while EAP sprints are reflected directly in CWM’s Sprint planning view, thus enabling unified planning across work types. Teams can plan work for their sprints and update work status directly from the CWM Board, with performance reports in EAP dynamically reflecting these changes. This integration enables teams to manage their full scope of work from a single, connected workspace.

-   **[Dynamic data linking in Docs](https://www.servicenow.com/docs/access?context=docs-for-planning-items-in-spw&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)**

Keep record information in your documentation always current and reduce manual effort with the Dynamic data linking feature in Docs. You can now reference any ServiceNow application record and Docs will automatically reflect the latest updates from those records. For example, if you add a reference to a Project record, the reference will show the latest field information of the project in Docs without requiring manual edits. Clicking the project reference opens up the project form so that you can view the full details of the project record and make any necessary changes. Dynamic linking also enables adding references to a particular field of a record, such as Assigned to of an Incident record.

You can add references from any ServiceNow table you have access to, with no setup or configuration needed, thereby eliminate the hassle of switching between applications to copy and paste data from various records into Docs.

-   **[Portfolio plan enhancements](https://www.servicenow.com/docs/access?context=create-portfolio-plans-in-alignment-planner-workspace&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)**
    -   Create portfolio plans for AI-related items by applying a filter on the planning item tables, setting the **Investment type** field value to **Artificial Intelligence** during portfolio plan creation. This allows you to focus exclusively on AI-related items.
    -   With the sn\_align\_core.apw\_admin role, you can update the following system properties:
        -   **sn\_align\_core.planning\_item\_types\_allow\_list** - Defines the planning item types that can be configured and allowed for a portfolio plan.
        -   **glide.ui.sn\_align\_core\_dependency\_activity.fields** - Enables activity stream for the dependency formatter fields.
        -   **sn\_align\_ws.gantt\_show\_higher\_planning\_upper\_entities** - Enables display of entire hierarchy of lens structure from top to bottom in prioritization hierarchy view for high-level portfolio plans.
        -   **sn\_align\_ws.portfolio\_plan\_items\_limit** - Defines the number of planning items to be loaded on the planning page.
-   **[Roadmap enhancements](https://www.servicenow.com/docs/access?context=roadmaps-in-alignment-planner-workspace&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)**
    -   Create custom themes for your roadmap bar colors to align with your organization’s standards.
    -   Experience consistent roadmap bar colors for choice list attribute values across all portfolio plans.
    -   View the roadmap-level milestone row while scrolling down the Roadmap page.
    -   Use different icons to distinguish item-level milestones.
    -   Match milestone colors with their status labels across the roadmap, milestone popover, and side panel. For example, a missed milestone displays the same color in all locations.
    -   With the sn\_align\_core.apw\_admin role, you can define the number of milestone items to be loaded in the Roadmap tab. The **sn\_align\_ws.item\_milestone\_limit** system property allows you to define the number of milestone items to be loaded in the Roadmap tab.
    -   With the sn\_align\_core.apw\_admin role, you can define the list of planning item types that can be created in a free-form roadmap. The **sn\_align\_ws.freeform\_planning\_items\_creation\_list** system property allows you to define the list of planning item types that can be created in a free-form roadmap.
-   **[Scenario planning enhancements](https://www.servicenow.com/docs/access?context=enable-scenario-planning-in-strategic-planning&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)**

With the sn\_align\_core.apw\_admin role, you can enable or disable the scenario planning feature. The **sn\_align\_ws.is\_scenario\_planning\_disabled** system property allows you to enable or disable the scenario planning feature.

-   **[Quick filters enhancements](https://www.servicenow.com/docs/access?context=managing-backlog-alignment-planner-workspace&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)**

Apply filters using string-type and boolean field values across the Planning page and Scoring page to view the required dataset. These filters are saved as part of your user preferences, enabling you to access the same filtered data when you log back in and continue your planning seamlessly.

-   **[Investment type and Investment class fields on the Planning item table](https://www.servicenow.com/docs/access?context=planning-item-form&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)**

The **Investment type** and **Investment class** fields have been added to the Planning item \[sn\_align\_core\_planning\_item\] table to enable these attributes to be defined at the parent planning item level.

A new value, **Artificial Intelligence**, has also been added to the **Investment type** field to categorize a planning item as an Artificial Intelligence initiative.

-   **[Goal management enhancements](https://www.servicenow.com/docs/access?context=managing-goals-in-alignment-planner-workspace&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)**
    -   With the sn\_gf\_goal\_admin role, you can update goal-specific system properties:
        -   **sn\_align\_ws.goal\_hierarchy.max\_records** - Defines the number of targets to load on the Hierarchy tab in the Targets view. The default value is 250.
        -   **glide.ui.sn\_gf\_goal\_activity.fields** - Enables activity stream for fields of the goals.
    -   Experience faster loading of goals data, even when large volumes of data are present.
    -   With the sn\_gf.goal\_admin role, you can edit any goal and target as needed, even when you aren’t the owner or contributor of a goal or target.
    -   With both the sn\_gf\_goal\_admin and sn\_apw\_advanced.spw\_goal\_user roles, you can edit target breakdowns as needed.
-   **[Financial enhancements](https://www.servicenow.com/docs/access?context=using-financials-spw&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)**
    -   View only the planned costs of your planning items to track the total cost of your planning items.
    -   Use Display mode to switch between focused views to better plan and track the financials of your planning items.
    -   Manage the planned and actual monetary benefit plans for your projects to identify the financial performance of your project using the Cost and benefits screen.
    -   Use multicurrency to view and manage financial records of the project in Investment currency, which can be different from your functional currency. Manage multiple financial records such as planned and actual expenses, planned and actual benefits, and so on.
    -   Generate and track labor cost for sub-projects, based on the resource assignments of your sub-projects and planning items such as features and capabilities.

</td></tr><tr><td>

Subscription Management

</td><td>

-   **[Manage custom applications and table mapping through the platform](https://www.servicenow.com/docs/access?context=allocating-custom-tables-subscr-apps-v2&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

Map any missing custom application and tables in Subscription Management to a subscription directly from the Custom Applications list or Custom Table Inventory list.

-   **[Support for domain separation](https://www.servicenow.com/docs/access?context=domain-separation-subscription-mgmt&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

View and filter subscribers by domain for user-based subscriptionsand view Now Assist usage by domain.

-   **[Monitor Workflow Data Fabric usage](https://www.servicenow.com/docs/access?context=monitoring-wdf-capability-use&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

Monitor and track Workflow Data Fabric capability usage and view the relative token use rate of each capability.


</td></tr><tr><td>

Supplier Lifecycle Operations

</td><td>

-   **[Supplier Operations](https://www.servicenow.com/docs/access?context=supplier-operations&version=zurich&pubname=zurich-source-to-pay-operations&ft:locale=en-US)**

Supplier Operations ​ provides support for advanced case management capabilities to handle key supplier lifecycle events such as onboarding, offboarding, and ongoing operations. It includes the ability to resolve cases via Playbooks for a structured and consistent approach.

-   **[Supplier Payment Optimization](https://www.servicenow.com/docs/access?context=supplier-pmnt-opt&version=zurich&pubname=zurich-source-to-pay-operations&ft:locale=en-US)**

Supplier managers can identify, prioritize, and track suppliers with high potential for accepting credit card payments.

    -   Supplier Managers can initiate credit card enablement cases, enabling suppliers to use credit card payments as their preferred payment method.
    -   They can initiate credit card enablement journey for new or existing suppliers after checking their propensity scores \(currently requires manual updates\).
    -   They can view the saving estimates associated with the card for a given supplier using the **Savings calculator** tool. They can also view the calculation details of the savings estimator formulas.
-   **[Relish Integration for Supplier Lifecycle Operations](https://www.servicenow.com/docs/access?context=relish-slo-connector&version=zurich&pubname=zurich-source-to-pay-operations&ft:locale=en-US)**

Supplier managers can conduct sanction screening, validate banking details change requests, and supplier location change requests via Relish integration.

-   **[Automated KPI data collection](https://www.servicenow.com/docs/access?context=create-auto-kpi-template&version=zurich&pubname=zurich-source-to-pay-operations&ft:locale=en-US)**

This feature enables automated data collection, KPI template modifications, and calculation at supplier and contract levels. The automated KPI system integrated into action plans can be used for comprehensive performance monitoring.

-   **[Mapping multiple internal stakeholders to a supplier](https://www.servicenow.com/docs/access?context=manage-internal-stakeholders&version=zurich&pubname=zurich-source-to-pay-operations&ft:locale=en-US)**

This feature enhances supplier governance in SLO by enabling the mapping of multiple internal stakeholders such as legal, business, technical, and risk teams to suppliers, improving visibility and management of supplier relationships.

-   **[Universal Request](https://www.servicenow.com/docs/access?context=universal-request&version=zurich&pubname=zurich-source-to-pay-operations&ft:locale=en-US)**

Supplier contacts can create generic cases by selecting **Request Help** in the Supplier Collaboration Portal, if they can't find the relevant search results or are unsure of which department to contact for help. These cases are triaged and routed internally to appropriate case types. Universal requests remove ambiguity and improve efficiency for both suppliers and internal operations.

-   **[Overall supplier dashboard](https://www.servicenow.com/docs/access?context=overall-supplier-db&version=zurich&pubname=zurich-source-to-pay-operations&ft:locale=en-US)**

The overall supplier performance dashboard provides detailed information about overall supplier scores, count of all active suppliers, their all-time spend, and overall risk ratings. It also includes the Supplier Insights section and the Action plans section showing relevant details.

-   **[Smart Assessments](https://www.servicenow.com/docs/access?context=slo-campaign-mgmt&version=zurich&pubname=zurich-source-to-pay-operations&ft:locale=en-US)**

Supplier managers can use the segmentation rules and assessment templates to create smart assessments in bulk for users. Smart assessments provide a survey-like experience with enhanced UI capabilities for both internal and external users. This feature utilizes the capabilities of the Smart Assessment Engine application.

-   **[Emails view for supplier managers](https://www.servicenow.com/docs/access?context=enabling-emails-view-for-contacts&version=zurich&pubname=zurich-source-to-pay-operations&ft:locale=en-US)**

Supplier managers can access their emails within the Source-to-Pay Workspace from the **Emails** tab in the case, task, and supplier details pages respectively. Email actions are reflected, incomplete email errors are handled, and email-related activities can be summarized from the workspace.

Supplier contacts receive the emails and they can perform the assigned tasks directly via email without logging in to the Supplier Collaboration Portal.


</td></tr><tr><td>

Synthetic monitoring

</td><td>

-   **[MID Server support for running synthetic monitors](https://www.servicenow.com/docs/access?context=create-synthetic-monitoring-locations&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

Run synthetic monitors from your MID Server.

-   **[HTTP endpoint creation directly in synthetic monitoring](https://www.servicenow.com/docs/access?context=create-synthetic-monitor&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

Create HTTP endpoints for your monitors without leaving the SOW.

-   **[Support groups for synthetic monitor-based alerts](https://www.servicenow.com/docs/access?context=create-synthetic-monitor&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

Assign a support group to a monitor, and then any raised alerts follow the associated alert automation rules.

-   **[View all monitors with open alerts](https://www.servicenow.com/docs/access?context=identifying-system-issues&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US#section_yll_v5k_fdc)**

As of 1.4, view all monitors with open alerts.

-   **[View alerts associated with a monitor](https://www.servicenow.com/docs/access?context=view-alerts-for-a-synthetic-monitor&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

As of 1.4, navigate to a monitor's open alerts.

-   **[Assign tags to a monitor's alerts](https://www.servicenow.com/docs/access?context=create-synthetic-monitor&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

As of 1.4, use tag-based clustering to group monitor alerts.

-   **[Use OAuth-based credentials](https://www.servicenow.com/docs/access?context=create-synthetic-monitor&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

As of 1.4, OAuth credentials on endpoints are supported.


</td></tr><tr><td>

Talent profile

</td><td>

-   **[Create Talent pools](https://www.servicenow.com/docs/access?context=create-talent-pool&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

Create talent pools to organize similar talent profiles in one place for particular hiring requirements. You can share and collaborate using talent pools and also send out communications to all talent profiles in the pool at once.

-   **[Copy talent to pool](https://www.servicenow.com/docs/access?context=copy-talent-other-pool&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

Use existing talent pools to associate suitable talent profiles from the pools to your talent pool.

-   **[Remove talent profiles from a pool](https://www.servicenow.com/docs/access?context=remove-talent-from-pool&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

As an owner of the pool or one of the collaborators, remove the talent profiles that are no longer required.

-   **[Delete a Talent pool](https://www.servicenow.com/docs/access?context=delete-talent-pool&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

Delete a talent pool when it has served its purpose or is no longer relevant.

-   **[Create talent profiles](https://www.servicenow.com/docs/access?context=create-talent-ta&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

Create talent profiles to add it to the talent profile repository of your organization and use it for an optimized hiring process.

-   **[Filter talent profiles](https://www.servicenow.com/docs/access?context=filter-tp&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

Use filter options to find relevant talent profiles more efficiently in the **Talent pool** tab.

-   **[Add talent profiles to a Talent pool](https://www.servicenow.com/docs/access?context=add-talent-to-pool&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

Add similar talent profiles to a talent pool to streamline communication to all the profiles during a particular hiring drive.

-   **[Copy talent profiles as job prospects](https://www.servicenow.com/docs/access?context=copy-talent-to-leads&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

Copy talent profiles from a talent pool to a particular job requisition as prospects.


</td></tr><tr><td>

Telecommunications Network Inventory

</td><td>

-   **[Create a logical connection record using the Design and Assign function](https://www.servicenow.com/docs/access?context=create-logical-connection-record-design-assign-playbook&version=zurich&pubname=zurich-telecom-network-inventory&ft:locale=en-US)**

Logical interfaces created are now automatically related to their corresponding cards or parent equipment. This enhancement ensures consistency across systems and helps prevent duplicate CI creation by improving the alignment between logical and physical interfaces.


-   **[Visualize your network infrastructure](https://www.servicenow.com/docs/access?context=data-center-inventory-management&version=zurich&pubname=zurich-telecom-network-inventory&ft:locale=en-US)**

Use the new L1 menu that consolidates all network visualizations into a single canvas and include a tabular section for each view, such as site, floor, and topology. The following roles are introduced to manage datacenter infrastructure.

    -   DC Floor Designer \(sn\_ni\_core.dc\_floor\_designer\) – Design floor layout in Map Studio.
    -   DC Ops Agent \(sn\_ni\_core.dc\_ops\_agent\) – Oversee the operations of the data center floor.
    -   DC Ops Viewer \(sn\_ni\_core.dc\_ops\_viewer\) – View the Network Inventory Workspace and its components.
-   **[Floor map](https://www.servicenow.com/docs/access?context=visualization-floor-maps&version=zurich&pubname=zurich-telecom-network-inventory&ft:locale=en-US)**

Use the floor map to view the layout of your datacenter infrastructure. View network asset placement and operational details to monitor power, thermal, and usage data. View the incidents and alerts and take appropriate action.

-   **[Geo map](https://www.servicenow.com/docs/access?context=visualization-map&version=zurich&pubname=zurich-telecom-network-inventory&ft:locale=en-US)**

Use the geo map to view the geographical locations of your network sites and data centers. Geo map supports rendering data centers on the map, enabling the relevant persona, such as the DC Ops Viewer, to view connected data centers. You can open a data center floor map directly from the geo map for more detailed insights.

-   **[Upload and manage floor map for your datacenter](https://www.servicenow.com/docs/access?context=create-floor-map-data-center&version=zurich&pubname=zurich-telecom-network-inventory&ft:locale=en-US)**

Upload and manage your datacenter map objects using the Map Studio interface. Enable you to view respective floor plans for a selected building in a campus.

-   **[Service Operations Workspace for TNI](https://www.servicenow.com/docs/access?context=service-operations-workspace-network-inventory&version=zurich&pubname=zurich-telecom-network-inventory&ft:locale=en-US)**

Provides a converged experience for agents to view both incident/alarm details and Network Inventory entities within a single Workspace. Enhances efficiency in retrieving information and significantly improves the overall user experience.

-   **[Capacity management](https://www.servicenow.com/docs/access?context=capacity-management-reporting&version=zurich&pubname=zurich-telecom-network-inventory&ft:locale=en-US)**

Supports pushing operational data to REST endpoints through an exposed API and store it in the ClothoDB. Overlay time series metrics on the datacenter floor map to monitor overall health and take appropriate action.

-   **[Collect operational values for datacenter](https://www.servicenow.com/docs/access?context=enter-operational-values-data-center&version=zurich&pubname=zurich-telecom-network-inventory&ft:locale=en-US)**

Manually record operational values of Configuration Items \(CI\) and store it in ClothoDB. Use this data for datacenter performance tracking.

-   **[Define the datacenter details](https://www.servicenow.com/docs/access?context=define-data-center-details&version=zurich&pubname=zurich-telecom-network-inventory&ft:locale=en-US)**

Define your datacenter record to view the location-specific attributes for each datacenter, including the campus, buildings, and floors where your network asset is located.

-   **[Define the power circuit details](https://www.servicenow.com/docs/access?context=define-power-circuit-details&version=zurich&pubname=zurich-telecom-network-inventory&ft:locale=en-US)**

Define the power circuit record to represent the electrical pathway that delivers power within a data center.

-   **[Define the facility hardware details](https://www.servicenow.com/docs/access?context=define-facility-hardware-details&version=zurich&pubname=zurich-telecom-network-inventory&ft:locale=en-US)**

Define the facility hardware record to represent power, HVAC \(Heating, Ventilation, and Air Conditioning\), network representation, and their connectivity in a data center.

-   **[Create a facility model](https://www.servicenow.com/docs/access?context=create-facility-model&version=zurich&pubname=zurich-telecom-network-inventory&ft:locale=en-US)**

Create a facility model to define the physical characteristics data of the facility record based on the product manufacturer's recommendations.

-   **[Create an equipment record by using design and assign](https://www.servicenow.com/docs/access?context=create-equipment-record-design-and-assign&version=zurich&pubname=zurich-telecom-network-inventory&ft:locale=en-US)**

View datacenter records listed in the Equipment task attribute form.

-   **[Define the network interface details](https://www.servicenow.com/docs/access?context=define-tni-interfaces&version=zurich&pubname=zurich-telecom-network-inventory&ft:locale=en-US)**

Add **Wavelength** attribute to the Network Interface form and **Port position** attribute to Interface Model form.

-   **[Create an equipment holder model](https://www.servicenow.com/docs/access?context=create-equipment-holder-models&version=zurich&pubname=zurich-telecom-network-inventory&ft:locale=en-US)**

Added **RU numbering direction** attribute to define the numbering sequence of rack units in the Rack view.


</td></tr><tr><td>

Telecommunications Service Operations Management \(TSOM\)

</td><td>

-   **[Telecom Discovery Builder framework](https://www.servicenow.com/docs/access?context=exploring-the-telco-generic-schema-etl-framework&version=zurich&pubname=zurich-telecom-service-ops&ft:locale=en-US)**

Leverage a standardized Extract, Transform, Load \(ETL\) framework to streamline the processing and storage of telecom network data on the ServiceNow AI Platform.

This reusable framework simplifies implementation by removing the need to manually build ETLs. It enables you to focus on connectivity logic while confirming consistent and reliable mapping of network elements such as equipment, cards, ports, LAGs, logical ports, and logical connections into predefined CMDB structures.

Use Telecom Discovery Builder Framework to do the following:

    -   Simplify data transformation tasks by duplicating the common ETL and configuring essential fields and settings for specific connector applications.
    -   Deploy new Service Graph Connector \(SGC\) using existing ETLs to maintain consistent data transformation practices.
    -   Help to ensure data integrity and support the automatic creation of TNI Entities through configured Before and After scripts.
    -   The standardized CMDB/TNI data model enables ETL reusability across multiple connectors.
    -   Allocate predefined storage locations for both physical and logical inventory elements.
    -   Maintain consistent data model hierarchies across connectors to support unified network inventory management.
    -   Improve Discovery SGC quality by providing an OOTB Data Source Validation tools.
-   **[Telecom Discrepancy Identification and Reconciliation](https://www.servicenow.com/docs/access?context=exploring-telecom-reconciliation&version=zurich&pubname=zurich-telecom-service-ops&ft:locale=en-US)**

Use enhanced discrepancy identification and reconciliation features to keep your discovery data accurate and up to date on the ServiceNow AI Platform. These features give you better control over detected changes and improve overall audit performance.

    -   Identify attribute value mismatches during discovery, such as bandwidth changes on ports \(for example, from 10 Mbps to 100 Mbps\).
    -   Display previous and current attribute values, enabling you to decide whether to accept the new value, retain the old one, or manually raise a remediation task.
    -   Detect discrepancies in logical entities alongside physical entities for comprehensive discrepancy management for newly discovered logical network elements.
    -   Generate audit results using filtering conditions—such as specific IP ranges, device vendors, or port types—to focus on relevant subsets of data and significantly enhance audit performance and usability.
-   **[Fault Management: Events and alerts](https://www.servicenow.com/docs/access?context=fault-management-events-and-alerts&version=zurich&pubname=zurich-telecom-service-ops&ft:locale=en-US)**

You can monitor your SD-WAN network health and resolve issues faster with automated alerts and event detection.

    -   Detect and resolve SD-WAN network issues faster with automated alerts and event monitoring.
    -   Configure customizable event rules to detect SD-WAN device issues in real time.

-   **[Added Service Graph Connector for Cisco Meraki and Fortinet](https://www.servicenow.com/docs/access?context=configuring-cisco-meraki-service-graph-connector&version=zurich&pubname=zurich-telecom-service-ops&ft:locale=en-US)**

The following capabilities have been added to Cisco Meraki and Fortinet:

    -   Provides a centralized management of physical infrastructure and logical network relationships within the ServiceNow AI Platform®.
    -   Supports automated, telecom-aware discovery and real-time CMDB synchronization, along with visual network mapping, guided setup, and a dashboard for monitoring integration health.
-   **[Granular admin roles](https://www.servicenow.com/docs/access?context=exploring-the-telco-generic-schema-etl-framework&version=zurich&pubname=zurich-telecom-service-ops&ft:locale=en-US)**

The granular admin role enables developers and administrators to complete administrative configuration tasks for TSOM without requiring the full admin role.


</td></tr><tr><td>

Theme Builder

</td><td>

-   **[Publish the new Coral theme](https://www.servicenow.com/docs/access?context=tb-apply-theme&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US)**

Publish or unpublish the new Coral theme directly from Theme Builder. This theme provides a fresh look and feel and features brand-neutral illustrations to enhance your user experience. A dark theme variant is available for web and mobile experiences.

-   **[Upload and manage custom fonts in your theme](https://www.servicenow.com/docs/access?context=upload-custom-font&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US)**

Use your organization's fonts to maintain a consistent look and feel for your brand throughout your experience.

    -   Upload, preview, and edit at most 10 custom font families from the **Global styles** or **Component styles** tabs.
    -   Add unlimited associated font faces to each font family and apply them individually to components.
    -   Delete your font family or font face from your theme.
-   **[Explore the expanded image categories with color editing and override capability](https://www.servicenow.com/docs/access?context=working-with-image-styles&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US)**

As of Theme Builder version 6.1, configure the following new image categories to further enhance your theme:

    -   Edit the colors of banners, modals, tile icons, and cards from within Theme Builder.
    -   Override each of these default illustrations with your own custom images to uniquely align with your branding style.
-   **[Guided tours in Theme Builder](https://www.servicenow.com/docs/access?context=guided-tours-theme-builder&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US)**

As of version 6.1, learn about additional features and complete tasks through interactive steps by taking guided tours within Theme Builder.

-   **[Create a theme using Now Assist](https://www.servicenow.com/docs/access?context=create-theme-now-assist&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US)**

As of Zurich Patch 7, leverage Now Assist to generate themes based on your brand image. After generating a theme, navigate to Theme Builder to publish and apply additional styling. This feature requires Now Assist for Creator.

-   **[Create a theme with AI in Theme Builder](https://www.servicenow.com/docs/access?context=tb-create-a-theme-ai&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US)**

As of Zurich Patch 7, use AI to generate themes from brand images, preview multiple options, and refine results all within the updated Create a theme wizard. If you prefer, you can skip the AI step and continue creating your theme manually using the existing workflow. This feature requires Now Assist for Creator.


</td></tr><tr><td>

Third-party Risk Management

</td><td>

-   **[Now Assist for Third-party Risk Management \(TPRM\) release notes](../governance-risk-compliance/now-assist-for-tprm-rn.md)**

Review the Now Assist for Third-party Risk Management \(TPRM\) \(TPRM\) release notes for full descriptions of the features.

-   **[Document Management system in Third-party Risk Management](https://www.servicenow.com/docs/access?context=tprm-dms&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

Starting with version 21.1.x, you can use the Document Management System \(DMS\) in TPRM, which provides a centralized repository for storing, organizing, and managing third-party documents throughout the vendor life cycle. It can be used by third-party risk managers \[sn\_vdr\_risk\_asmt.vendor\_manager\], third-party assessors \[sn\_vdr\_risk\_asmt.vendor\_assessor\], and third parties to upload, categorize, track, and review documents with metadata, version control, and access permissions. This feature streamlines evidence tracking, reduces duplication, and improves audit readiness by enabling document reuse across assessments, contracts, issues, and tasks.

For information on Now Assist skills for TPRM and Document Management, see [Now Assist for Third-party Risk Management \(TPRM\) release notes](../governance-risk-compliance/now-assist-for-tprm-rn.md) and [Now Assist in Document Intelligence release notes](../analytics-intelligence-reporting/now-assist-document-intelligence-rn.md).

-   **[Register of information regulatory packages](https://www.servicenow.com/docs/access?context=tprm-dora-roi&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

After upgrading the Digital Resilience Third-party Information Register application to version 21.1.x, third-party assessors \[sn\_vdr\_risk\_asmt.vendor\_assessor\] can now generate regulator-ready Register of Information packages using the Plain-CSV Report Package option on the download page. The ZIP file includes metadata and report folders structured to regulator specifications, with file names containing LEI, entity ID, and release version. This format helps ensure EU DORA compliance and supports automated validation workflows. You can follow the user guide on the Download/Upload request page for suggested steps and permissions.

-   **[Validation framework for Register of Information](https://www.servicenow.com/docs/access?context=tprm-validation-roi&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

After upgrading the Digital Resilience Third-party Information Register application to version 21.1.x, third-party risk managers \[sn\_vdr\_risk\_asmt.vendor\_manager\] can now validate downloaded Register of Information packages using the Plain-CSV Report Package option on the download page against requirements. File format, structure, encoding, naming conventions, and field-level data are validated across multiple tables. If any validation warnings are detected, a validation report is automatically attached, including mappings to regulator fields such as Template Code, Row Code, and Column Code. Validation reports include real-world field labels, rule expressions, and record identifiers. You can cross-reference validation errors using a downloadable Excel master template that mirrors the CSV structure, making it easier to locate and address issues. Additional enhancements include support for “Not applicable” values, enforcement of file size limits, and clearer error messages for malformed data.

-   **[New sn\_vdr\_risk\_asmt.sae\_enabled property](https://www.servicenow.com/docs/access?context=tprm-properties-configure&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

Use the new and improved Smart Assessment experience after you upgrade to version 21.0.x and set the Smart Assessment Engine enabled \(**sn\_vdr\_risk\_asmt.sae\_enabled**\) property.

-   **[Smart assessments with Third-party Risk Management](https://www.servicenow.com/docs/access?context=tprm-sae-using&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

Create Smart Assessment Engine assessments for your organization:

    -   Enhanced navigation: Use the improved navigation for a better user experience.
    -   Assessment support: Conduct assessments for both internal and external parties. TPRM questionnaire templates include additional attributes such as the risk area and the option to include previous responses, which aren’t available in SAE. TPRM templates must be created directly within the Vendor Management Workspace to ensure that they include the necessary attributes.
    -   Organize questions: Group questions into subsections for better organization.
    -   Add attachments: Attach the files directly to the individual questions.
    -   Add reference information: Add reference information to a questionnaire template to help ensure that assessors can access the information they need while responding.
    -   Filter questions: Quickly identify and filter unanswered questions.
    -   Auto-save for questionnaires: Auto-save each question automatically after changes are made to them.
    -   Standardized risk rating scale definition: Define the risk rating scales at the template level for both internal and external assessments.
    -   Assessment duration: Define the duration of an assessment when creating a questionnaire template.
    -   Combine assessments: Respond to questionnaires by using the same SAE template in a single, streamlined view.
    -   Bulk template migration: Migrate classic templates in bulk to the Smart Assessment format. To ensure the templates work correctly in TPRM, you must migrate them by using the Third-party Risk Management application.
    -   Risk score normalization: Standardize the risk scores for a consistent evaluation.
    -   Support for the GRC and third-party portals: Use the GRC portal to access and complete internal assessments and the third-party portal to complete external assessments.

</td></tr><tr><td>

Threat Intelligence Security Center

</td><td>

-   **[Configure Threat Intelligence External Sharing](https://www.servicenow.com/docs/access?context=tisc-intel-sharing&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

Take advantage of external sharing for secure, automated, and on-demand dissemination of threat intelligence using STIX 2.1 and MISP formats. Supports sharing across external agencies \(CISA, ISAC\), integrations \(SIEMs, EDRs\), TAXII-based TISC instances, and inbound intelligence from external entities.


-   **[About Report Templates in TISC](https://www.servicenow.com/docs/access?context=tisc-report-templates&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

Generate reports outside case management using base templates through a new reporting section in the Threat Intelligence Library.


-   **[Configure custom MISP API feed](https://www.servicenow.com/docs/access?context=tisc-premium-misp&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

Import events, attributes, and objects from the MISP server into the Threat Intelligence Library.


-   **[Configure Custom Event Types for Timeline](https://www.servicenow.com/docs/access?context=tisc-config-timeline&version=zurich&pubname=zurich-security-management&ft:locale=en-US) and [Using Timeline in Investigation Canvas](https://www.servicenow.com/docs/access?context=tisc-timeline-events&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

Define, visualize, and manage timeline events associated with nodes through the Investigation Canvas.


-   **[Configuring TISC add-on in Splunk](https://www.servicenow.com/docs/access?context=tisc-configure-splunk&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

Include optional attributes during configuration that can be stored in the Splunk KV Store.

-   **[Configure custom CrowdStrike feed](https://www.servicenow.com/docs/access?context=premium-threat-feed-for-crowdstrike&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

Map CrowdStrike Indicator Malicious confidence to TISC confidence.

-   **[View Threat Intel Feeds](https://www.servicenow.com/docs/access?context=base-system-threat-intel-feeds&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

Map specific source values to required observable fields during import process.


</td></tr><tr><td>

UI Builder

</td><td>

-   **[Build and customize components](https://www.servicenow.com/docs/access?context=component-builder&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

Build custom components and configure them to be used across pages and experiences.

-   **[Utilize AI on pages you are building](https://www.servicenow.com/docs/access?context=add-skill&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

Easily add generative AI capabilities to any page, component, or controller

-   **[Get conversational help with the Now Assist panel](https://www.servicenow.com/docs/access?context=uib-now-assist-panel&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

Ask questions directly in the Now Assist panel to receive immediate AI-driven guidance without leaving UI Builder.

-   **[Build pages and gain page insights using the Now Assist panel in UI Builder.](https://www.servicenow.com/docs/access?context=using-ui-builder-agent&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

As of UI Builder Version 28.2, use Now Assist to add components, bind data, adjust layouts, and get page insights such as number of components, data resource information, and access permissions.

-   **[Add test values in Component Builder](https://www.servicenow.com/docs/access?context=component-builder&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

As of UI Builder Version 28.2, define simulated page parameters to preview and validate how customer components behave during development.


</td></tr><tr><td>

Unified Security Exposure Management

</td><td>

-   **[Remediation task rule execution mode](https://www.servicenow.com/docs/access?context=sem-grouping-multiple-findings-remediation-tasks-processing&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

You can now choose how remediation task rules are evaluated during ingestion. The new Match First execution mode evaluates rules sequentially and applies only the first matching rule, assigning each finding to exactly one remediation task. The default Match All mode continues to evaluate all applicable rules.

-   **[Unified Microsoft Defender Integration for Security Exposure Management](https://www.servicenow.com/docs/access?context=ms-defender-sem&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

The Microsoft Defender for Cloud and Microsoft Defender Threat and Vulnerability Management \(MS TVM\) plugins are now consolidated into a single plugin: Microsoft Defender Integration for Security Exposure Management. This consolidation deprecates the standalone Microsoft Defender for Cloud plugin. The unified plugin also introduces container image vulnerability ingestion from Microsoft Defender for Cloud, creating Container Vulnerable Items on your instance. A guided migration path is available to transfer existing data from the deprecated applications to the unified plugin.

-   **[GitHub Application Vulnerability Integration – Generic secrets support](https://www.servicenow.com/docs/access?context=github-vuln-integration&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

The GitHub Secret Scanning Integration now imports generic secrets in addition to standard secrets from your GitHub repositories. A new Manage generic secrets in ServiceNow configuration option lets you control whether generic secrets are ingested. Imported secrets are mapped to Application Vulnerable Items \(AVIs\) with the scan type Secret, while generic secrets are mapped with the scan type Generic Secret.

-   **[Optimized Tenable.io Compliance Results ingestion](https://www.servicenow.com/docs/access?context=tenable-io-integrations-list&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

Starting with v 6.1.3, the Tenable.io Compliance Results Integration is replaced by the Tenable.io Fixed Compliance Results Integration and Tenable.io Open Compliance Results Integration. Compliance results are now imported based on their status, optimizing ingestion performance and scalability for environments with large volumes of compliance data while keeping remediation and compliance tracking aligned with the current state of findings.

-   **[Qualys Integration – API enhancements](https://www.servicenow.com/docs/access?context=qualys-rest-messages-cc&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

Qualys Integration has been upgraded to support newer Qualys API versions across Host Detection, Host List, Knowledgebase, PC Controls, PC Policies, and PCRS integrations. The integrations now ingest additional data fields, including vulnerability detection source, authentication privilege status, active status for controls and policies, and cloud metadata, giving you better visibility into your vulnerability and compliance data. Use the new `posture_api_version` integration instance parameter to choose between the default v2.0 APIs or the newer v5.0 streaming APIs for the PCRS Policy Host and PCRS Test Results integrations.

-   **[Improved vulnerability assessment workflows](https://www.servicenow.com/docs/access?context=vr-ws-vuln-assessment&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**
    -   CI filtering for vulnerability assessments: You can now filter which configuration items are included in a vulnerability assessment using a condition builder.
    -   Business Application population on AVITs: AVITs created from SBOM assessment results now include Business Application information, helping you understand application impact and prioritize remediation.
    -   Priority roll‑down from vulnerability assessments: Updates to the priority of a vulnerability assessment now automatically roll down to associated VITs and AVITs, ensuring consistent prioritization based on the highest severity.
-   **[Enhanced Compensatory controls](https://www.servicenow.com/docs/access?context=requesting-approving-risk-reduction&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

When new vulnerable items are ingested and associated with a remediation task that already has an approved compensating control, the reduced risk rating is now automatically inherited by those new vulnerable items.

-   **[Enhanced security exposure management](https://www.servicenow.com/docs/access?context=sem-workspace-user-interface&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

Introduced Security Exposure Management Workspace for all security personas, providing a centralized platform for managing security exposures. It includes the following views:

    -   Findings view: Comprehensive filtering, dashboard creation, and visualization controls enable efficient analysis and prioritization.
    -   Remediation view: Multiple work modes \(tasks, findings, assets\) facilitate effective remediation strategies.
    -   Approval view: The Exception Management UI now provides enhanced insights directly within the Change Approval record, enabling approvers to make informed decisions without navigating to related records. Additionally, the Approver landing page has been redesigned with an improved table view and additional columns, delivering better visibility and context for all findings. These enhancements streamline the approval workflow, reduce manual effort, and accelerate decision-making for exception requests.
-   **[Streamlined administration](https://www.servicenow.com/docs/access?context=sem-administration-console&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

Introduced Administration console to enable one-stop configuration for all Unified Security Exposure Management applications, including assignment rules, classification rules, and remediation targets. It provides consistent workflows across Vulnerability Response, Application Vulnerability Response, Container Vulnerability Response, and Configuration Compliance applications.

-   **[Centralised Approval Experience via Employee Service Center](https://www.servicenow.com/docs/access?context=employee-center-vr-overview&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

The Employee Service Center ESC now provides a standardized approval experience for Business Unit Heads, Service Owners, and IT Heads who may not regularly access the USEM platform. This enhancement ensures that vulnerability-related approvals can be managed from a single, central location, improving efficiency and transparency.

-   **[Configure approval workflow with unified Approval Rules](https://www.servicenow.com/docs/access?context=sem-approval-rules-overiew&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

The Approval Rules now provide a standardized way to configure approval workflows across multiple findings and remediation task tables in Security Exposure Management. Administrators can now define approval conditions, select applicable tables, and configure multi‑level approvers through a single, unified interface.

-   **[Cloud Exposure view](https://www.servicenow.com/docs/access?context=vr-cloud-exposure-view-db&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

View and act on all your cloud-related security findings from multiple vendors across your cloud environments with the Cloud Exposure View supported by USEM. The Cloud Exposure View provides a single location for your cloud security teams to monitor your cloud security posture.

-   **[Monitor integrations](https://www.servicenow.com/docs/access?context=integrating-usem&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

USEM introduces integration monitoring capabilities within the Security Exposure Management Workspace Administration console. Administrators can now view and troubleshoot integration run statuses for installed third-party applications, ensuring better visibility and operational health.

-   **[Generate insights to prioritize findings](https://www.servicenow.com/docs/access?context=sem-insights-skill&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

SEM Workspace uses Now Assist to bring generative AI to your dashboard. This capability helps you focus on critical risks and make informed decisions faster, improving overall security outcomes. It provides:

    -   Contextual summaries to quickly understand your security posture
    -   Actionable recommendations to address prioritized risks
-   **[Create custom widgets in the Visualization Library](https://www.servicenow.com/docs/access?context=sem-create-widget&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

Create and manage custom widgets in the finding view of the SEM workspace to visualize findings data that align with your organization’s reporting needs. The Visualization Library lets you define widget attributes such as chart type, visualization group, and data filters, enabling you to build dashboards that highlight the insights most relevant to your teams. This flexibility helps you focus on meaningful security metrics and make data-driven decisions.

-   **[Improved remediation target date handling](https://www.servicenow.com/docs/access?context=sem-configure-remediation-target-rules&version=zurich&pubname=zurich-security-management&section=sem-recalculate-rt-date&ft:locale=en-US)**

Remediation target \(RT\) dates now dynamically recalculate when a finding’s risk rating changes. When enabled, the system recalculates the SLA from the most recent risk rating update date, preventing RT dates from being set in the past and ensuring accurate SLA tracking.

-   **[Exception management configuration](https://www.servicenow.com/docs/access?context=sem-configure-exp-mngmt-vr&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**
    -   Manual and automated exception request and approval workflow: Flexible, customizable workflows streamline submission, review, and approval of exception requests.
    -   Comprehensive exception tracking and audit trails: Detailed records of approvals, justifications, and timelines support compliance efforts and simplify regulatory reporting.
-   **Consistent remediation task management with [remediation views](https://www.servicenow.com/docs/access?context=sem-workspaces-ui-remediation-module&version=zurich&pubname=zurich-security-management&ft:locale=en-US) and [centralized findings configuration](https://www.servicenow.com/docs/access?context=sem-configure-rules-manage-findings&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

Unified task management: Supports both manual task creation and automated rule-based task generation across all Unified Security Exposure Management applications.

Centralized rule definition: Enables efficient management of tasks across Vulnerability Response, Application Vulnerability Response, Container Vulnerability Response, and Configuration Compliance applications.

-   **[Advanced risk management](https://www.servicenow.com/docs/access?context=sem-vuln-calc-define-risk-rule-fields&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

Risk calculators: Introduced for all Unified Security Exposure Management applications, enabling definition of risk rules based on multiple factors and calculation mechanisms.

Risk rollup calculators: Aggregate scores from findings to higher-level entities, ensuring consistent risk scoring across applications.

-   **[Approval Recommendation](https://www.servicenow.com/docs/access?context=sem-approval-recommendation-skill&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

AI-powered recommendations for Exception and False Positive requests: Provides an on-demand recommendation to approve or reject a request using the Now Assist skill framework to analyze contextual data such as vulnerability details, risk factors, exploit availability, and related indicators. The recommendations are accessible directly from the Exception Change Approval record in the Security Exposure Management Workspace, enabling approvers to make faster, more consistent decisions while reducing the manual analysis effort.

-   **Exception Rule &amp; Change Approval Enhancements**
    -   [Change Approval Creation for Exception Rule submission](https://www.servicenow.com/docs/access?context=sem-exception-rules-overview&version=zurich&pubname=zurich-security-management&ft:locale=en-US): Previously, Change Approval \(CA\) was created only for a few types of exception requests. Now, the Change Approval\(CA\) is also created during exception rule submission. This enhancement verifies consistency across exception workflows and improves traceability.
    -   [Vulnerability Intelligence Tile on Change Approval Record](https://www.servicenow.com/docs/access?context=sem-configure-approval-view&version=zurich&pubname=zurich-security-management&ft:locale=en-US): The Vulnerability Intelligence Tile is added to change approval records, displaying vulnerability intelligence such as CISA KEV information, Known ransomware indicators, and EPSS percentile. This tile is visible only when the Intelligence and App-Vuln NVD plugins are installed. This enhancement provides approvers with the critical threat context for informed decision-making.
    -   [Summary Tiles on Change Approval Record](https://www.servicenow.com/docs/access?context=sem-configure-approval-view&version=zurich&pubname=zurich-security-management&ft:locale=en-US): The Impact Tile is added in the overview tab of the Change Approval record to provide approvers with the visibility of the impacted count information such as, Impacted CIs, Total Findings, and Total Vulnerabilities on the Change Approval for a Remediation Task. This enhancement improves visibility of potential impact during approval or rejection of requests.
    -   [Application-Based Filtering on Approvals View](https://www.servicenow.com/docs/access?context=sem-configure-approval-view&version=zurich&pubname=zurich-security-management&ft:locale=en-US): Added filtering capability on the Approvals view by application type such as: Application vulnerabilities \(AVR\), Container vulnerabilities \(CVR\), Infra Vulnerabilities \(VR\), and Misconfigurations \(CC\). This capability enables approvers to quickly drill down and manage approvals by category.
    -   [Reapply Assignment Rules for Deferred and Manually Assigned Items](https://www.servicenow.com/docs/access?context=sem-configure-assignment-rules&version=zurich&pubname=zurich-security-management&section=sem-reapply-assignment-rules&ft:locale=en-US): Introduced the ability to reapply assignment rules for Deferred items and Manually assigned items. This enhancement provides the flexibility to reassign items through the Re-evaluate action in the list view.

</td></tr><tr><td>

Upgrade Console

</td><td>

-   **[Additional way to access Upgrade Management](https://www.servicenow.com/docs/access?context=um-guided-tour-implement&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

You can now access Upgrade Console through the Admin menu by selecting **Admin Home**, and then selecting the **Upgrade Console** link.

-   **[Guided upgrade on sub-production instance](https://www.servicenow.com/docs/access?context=um-guided-tour-implement&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

Upgrade your sub-production instance to facilitate a seamless and successful transition. This process is structured into three pivotal phases: Pre-upgrade, Instance upgrade, and Post-upgrade tasks.

-   **[Guided upgrade on production instance](https://www.servicenow.com/docs/access?context=um-guided-tour-implement-prod&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

Elevate your upgrade experience within your production instance by meticulously completing each stage of the transition. This comprehensive process encompasses four crucial phases: Select upgrade, Pre-upgrade, Instance upgrade, and Post-upgrade tasks, all designed for a successful upgrade experience.

-   **[Additional step in pre-upgrade activities](https://www.servicenow.com/docs/access?context=um-pre-upgrade-activities&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

You an now choose an upgrade plan in the Choose an upgrade plan step by either selecting an existing plan or by creating a new plan. This new step is applicable for both production and sub-production instances.

-   **[Enhanced functionalities in the Preview application upgrades step](https://www.servicenow.com/docs/access?context=um-pre-upgrade-activities&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

Experience the new functionalities within the Preview application upgrades step for a seamless upgrade experience on your instance. These new functionalities are applicable for both production and sub-production instances.

-   **Enhanced capabilities in the Store application upgrades step**

Review the Store application upgrades step in the post-upgrade activities for updated information in the App updates and Upgrade store applications sections. You can also use the new **Sync Now** option to update the list of installed applications that were either added or upgraded outside the upgrade process.


</td></tr><tr><td>

Usage Insights

</td><td>

-   **[Analytics overlay experience](https://www.servicenow.com/docs/access?context=uxa-access-analytics-overlay&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US)**

Try the new utility icon that shows you the key usage metrics for the pages that you're navigating to without having to leave the application page. The shortcut gives you faster access to the contextual analytics overlay.

-   **[UXA-PA integration enhancements](https://www.servicenow.com/docs/access?context=uxa-data-sources&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US)**

Experience the enhancements by enabling UXA filters on dashboards, additional metrics configuration for sessions, and the inclusion of Pages in the User Experience Analytics data source. Furthermore, inline dashboards for User Experience Analytics data now offer drill-down, and the Events data source benefits from a new condition builder.


</td></tr><tr><td>

Virtual Agent

</td><td>

-   **[Assistant Designer](https://www.servicenow.com/docs/access?context=assistant-designer&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)**

Create and manage LLM-based chat and voice assistants within Assistant Designer, a centralized assistant administrator experience. Assistant Designer is comprised of three main areas: Assistants, Asset library \(previously Virtual Agent Designer\), and Analytics.

-   **[Conversational settings for Assets in the Asset library](https://www.servicenow.com/docs/access?context=asset-lib-conv-settings&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)Conversational settings**

Manage the settings for an asset directly from the Asset library page.


-   **[Integrating with Google Workspace](https://www.servicenow.com/docs/access?context=integrate-with-gsuite&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

Integrate Google Workspace chat with the ServiceNow® conversational interface features, including Virtual Agent, Natural Language Understanding \(NLU\), Notifications, and live agents.

-   **[AI Connector utility](https://www.servicenow.com/docs/access?context=vad-ai-connector-utility&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)**

Select AI agents to handle tasks in the AI Connector utility. For more information on AI agents in Virtual Agent Designer, see [Managing AI agents in Assistant Designer](https://www.servicenow.com/docs/access?context=managing-use-cases-ai-agents&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US) and [Using AI agents in Virtual Agent topics](https://www.servicenow.com/docs/access?context=ai-agent-custom-skill&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US).

-   **[Virtual Agent](https://www.servicenow.com/docs/access?context=virtual-agent-landing-page&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US) server**
    -   In chatHandshake, set **dynamic\_step\_loader\_enabled** to `true` to send stacked agentic AI messages to the server. Set **dynamic\_step\_loader\_enabled** to `false` to avoid sending messages.
    -   Pre-chat and post-chat surveys are now available for Anthropic Claude on AWS and Google Gemini large language models \(LLMs\). For more information on surveys, see [Chat surveys](https://www.servicenow.com/docs/access?context=ci-conversational-chat-surveys&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US).
-   **[Create a Virtual Agent topic](https://www.servicenow.com/docs/access?context=create-virtual-agent-topic&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)**

Start the create flow for all supported conversational LLM assets directly from Virtual Agent Designer.

-   **[Assistants in Virtual Agent Designer](https://www.servicenow.com/docs/access?context=conversation-designer-virtual-agent&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)**

The Now Assist Panel - Platform \(default\) assistant is now available in Virtual Agent Designer.

-   **[Integrating Now Assist in Virtual Agent with Microsoft Copilot](https://www.servicenow.com/docs/access?context=ms-copilot-na-va&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)**

Custom Engine Agent \(CEA\) is replacing the legacy Microsoft bot framework, allowing Microsoft Copilot to discover Virtual Agent, Now Assist, and use multi-turn conversations.


</td></tr><tr><td>

Vulnerability Response

</td><td>

-   **[Remediation task rule execution mode](https://www.servicenow.com/docs/access?context=sem-grouping-multiple-findings-remediation-tasks-processing&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

You can now choose how remediation task rules are evaluated during ingestion. The new Match First execution mode evaluates rules sequentially and applies only the first matching rule, assigning each finding to exactly one remediation task. The default Match All mode continues to evaluate all applicable rules.

-   **[Unified Microsoft Defender Integration for Security Exposure Management](https://www.servicenow.com/docs/access?context=ms-defender-sem&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

The Microsoft Defender for Cloud and Microsoft Defender Threat and Vulnerability Management \(MS TVM\) plugins are now consolidated into a single plugin: Microsoft Defender Integration for Security Exposure Management. This consolidation deprecates the standalone Microsoft Defender for Cloud plugin. The unified plugin also introduces container image vulnerability ingestion from Microsoft Defender for Cloud, creating Container Vulnerable Items on your instance. A guided migration path is available to transfer existing data from the deprecated applications to the unified plugin.

-   **[Optimized Tenable.io Compliance Results ingestion](https://www.servicenow.com/docs/access?context=tenable-io-integrations-list&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

Starting with v 6.1.3, the Tenable.io Compliance Results Integration is replaced by the Tenable.io Fixed Compliance Results Integration and Tenable.io Open Compliance Results Integration. Compliance results are now imported based on their status, optimizing ingestion performance and scalability for environments with large volumes of compliance data while keeping remediation and compliance tracking aligned with the current state of findings.

-   **[Qualys Integration – API enhancements](https://www.servicenow.com/docs/access?context=qualys-rest-messages&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

Qualys Integration has been upgraded to support newer Qualys API versions across Host Detection, Host List, Knowledgebase, PC Controls, PC Policies, and PCRS integrations. The integrations now ingest additional data fields, including vulnerability detection source, authentication privilege status, active status for controls and policies, and cloud metadata, giving you better visibility into your vulnerability and compliance data.

-   **[Improved vulnerability assessment workflows](https://www.servicenow.com/docs/access?context=vr-ws-vuln-assessment&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**
    -   CI filtering for vulnerability assessments: You can now filter which configuration items are included in a vulnerability assessment using a condition builder.
    -   Business Application population on AVITs: AVITs created from SBOM assessment results now include Business Application information, helping you understand application impact and prioritize remediation.
    -   Priority roll‑down from vulnerability assessments: Updates to the priority of a vulnerability assessment now automatically roll down to associated VITs and AVITs, ensuring consistent prioritization based on the highest severity.
-   **[Enhanced Compensatory controls](https://www.servicenow.com/docs/access?context=requesting-approving-risk-reduction&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

When new vulnerable items are ingested and associated with a remediation task that already has an approved compensating control, the reduced risk rating is now automatically inherited by those new vulnerable items.

-   **[Enhancements to the Wiz Vulnerability Response Integration](https://www.servicenow.com/docs/access?context=vr-wiz-exploring-host-cf&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**
    -   The Universally Unique Identifier \(UUID\) that identifies detections for the Wiz Host Vulnerability integration will be mapped to a detection key.

**Note:** This enhancement is supported for new customers only.

For existing customers, the detection key for the Wiz Host Vulnerability integration is created using the combination of vulnerability, asset\_id, and proof.

    -   You can configure the **First** parameter for the Wiz Asset Integration to help you resolve 504 errors. You can reduce the page size if you are having memory issues or generating errors. The default value is 500.
-   **[Enhancements to Detection Key Configurations for Vulnerability Response](https://www.servicenow.com/docs/access?context=detection-key-configurations-for-vr&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

Introduced configurable detection keys allowing customers to choose between Asset ID and Configuration Item, with validations, UI controls, and enhanced an existing schedule job to update existing detections.

-   **[Enhancements to the Vulnerability Response Integration with Wiz](https://www.servicenow.com/docs/access?context=vr-wiz-exploring-host-cf&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

The Missing Assets \[sn\_vul\_wiz\_missing\_asset\] is deprecated. After updating to version 1.1, you must backdate your existing primary Wiz integrations by three days and run them.

The backfill integrations are activated by default.

After you backdate and run your primary integrations, the following backfill integrations are no longer required:

    -   Host Vulnerability Backfill Integration
    -   Test Results Backfill Integration
    -   Host Test Results Backfill Integration
    -   Issues Backfill Integration
Resource types filters are supported on the Host Vulnerability, Host Test Results, Test Results, and Issues tabs on the Wiz Configuration page.

Additional attributes imported from Wiz that are not stored in the Discovered items \[sn\_sec\_cmn\_src\_ci\] table are stamped with `Asset Attributes` in this table.

Test results from the Host misconfiguration integration are classified as result type 'host\_misconfiguration'.

Data for resources that have the validated\_at\_runtime flag set to 'yes' is imported and populated on detections.

The is\_ignored column is deprecated on the Host Test Results and Test Results Integrations. This column was replaced by the is\_result\_ignored column.

The CMDB internet-facing field on the discovered item is mapped to Limited Internet Exposure on findings.

Column length for the descriptions in the Host Vulnerability import table has been increased.

-   **[Improved remediation target date handling](https://www.servicenow.com/docs/access?context=sem-configure-remediation-target-rules&version=zurich&pubname=zurich-security-management&section=sem-recalculate-rt-date&ft:locale=en-US)**

Remediation target \(RT\) dates now dynamically recalculate when a finding’s risk rating changes. Administrators can configure how recalculation occurs to ensure RT dates remain accurate and align with the latest risk updates, helping maintain consistent and reliable SLA tracking.

-   **[Identify Wiz Resource Types for import](https://www.servicenow.com/docs/access?context=wiz-assets-resources-tab&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

Identify the Resource Types \(assets\) that are reported by Wiz that you want to import with the Wiz Integration Resource Type configuration page in your ServiceNow AI Platform instance.

The Resource Types that you select apply to all the primary Wiz vulnerability and compliance integrations except the Wiz Container Vulnerability Integration. See the [Wiz Vulnerability Response Integrations](https://www.servicenow.com/docs/access?context=vr-wiz-exploring-host-cf&version=zurich&pubname=zurich-security-management&ft:locale=en-US) for more information about the vulnerability and compliance integrations.

-   **[Wiz Backfill Integrations](https://www.servicenow.com/docs/access?context=wiz-backfill&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

Retrieve and process data stored on the Wiz Missing Assets \[sn\_vul\_wiz\_missing\_asset\] table for assets that were not processed by the primary Host Vulnerability Integration with a specialized Wiz Backfill Integration.

The Host Vulnerability Backfill Integration is activated by default.

**Note:** The Wiz Asset Integration and the Wiz Container Vulnerability Integration do not have backfill integrations. The Wiz Asset Integration can discover assets and create and update discovered item records on the Discovered item \[sn\_sec\_cmn\_src\_ci\] table. The Wiz Container Vulnerability Integration imports and processes discovered container image records.

-   **[Import host vulnerability data with the Vulnerability Response Integration with Wiz](https://www.servicenow.com/docs/access?context=vr-wiz-exploring-host-cf&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

Import host vulnerability findings related to virtual machines and serverless assets in your cloud environment with Wiz’s Host Vulnerability Integration. These findings are mapped to Host Vulnerable Items \(VITs\) within the Vulnerability Response application to support remediation workflows.

-   **[Modify the severity for a CVE or TPE](https://www.servicenow.com/docs/access?context=vmws-modify-reset-severity&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

Vulnerability managers and vulnerability analysts can now adjust the severity of common vulnerabilities and exposures \(CVEs\) and third-party entries \(TPEs\) from the list view in the vulnerability manager workspace. The risk level of the associated vulnerabilities will be recalculated during the scheduled jobs based on the modified severity. You can also reset the severity to its original source value if required.

-   **[Questionnaire Support in Exception Management via Smart Assessment](https://www.servicenow.com/docs/access?context=vr-exception-management-smart-assessment&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

Configure advanced questionnaires as part of the exception management process using Smart Assessment. This enhancement allows remediation owners to provide detailed context for exception requests and enables approvers to configure conditional questions to gather information for informed decision making.

    -   Collaboration and streamlined approval: Facilitate collaboration between your vulnerability management and remediation teams by streamlining the approval process with clear and complete exception justifications.
    -   Mandatory questionnaires: Block the submission of exception requests until mandatory questionnaires are completed. If a questionnaire is marked as mandatory, the test results and its associated remediation tasks remain in the 'Open' state until the questionnaire is completed and submitted.
    -   If the questionnaire is incomplete, the state change approval record is saved as 'Draft'. Only after completing the questionnaire can the user submit the exception request, which will then move the test results or remediation tasks to the 'In Review' state.
-   **[Lookup rules enhancements](https://www.servicenow.com/docs/access?context=working-unmatched-cis&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

When you reapply Lookup rules, Discovered items \(DIs\) that have been inactive for more than 90 days are ignored. These Discovered items \(DIs\) are also excluded from licensing considerations. Removing them from the lookup logic can improve performance and reduce processing time.

    -   Background job enhancements: New fields have been added to help you view successfully evaluate records, the time taken for processing, the time remaining, and an estimated number of records.
    -   Improved accuracy for non-CSDM Vulnerability Response users: A system property \(sn\_sec\_cmn.ci\_lifecycle\_status\_source\) has been introduced to help users who do not follow Common Service Data Model \(CSDM\) standards. This property ensures that Discovered items \(DIs\) and associated VITs are properly marked as Decommissioned and are excluded from the CI Lookup. Additionally, the Retired Configuration Items PA indicator has been updated to accurately reflect CIs based on the decommissioning flags.
    -   The scheduled job to create reconcile unmatched discovered items feature is deprecated. You can "Reapply Look up Rules" for selected or filtered items in the discovered items table view.
-   **[Tenable.cs integrations with the Vulnerability Response and Container Vulnerability Response application](https://www.servicenow.com/docs/access?context=tenable-cs-integrations-list&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

The Vulnerability Response Integration with Tenable application now supports data ingestion from Tenable.cs, enabling you to bring in cloud and container vulnerabilities directly into ServiceNow. This integration enhances your ability to prioritize and remediate vulnerabilities identified in Tenable cloud resources and container images. Key capabilities are:

    -   Importing vulnerabilities discovered by Tenable.cs in cloud hosts and container images into ServiceNow automatically.
    -   Enabling remediation workflows to triage, assign, and resolve the most critical vulnerabilities across cloud-native and containerized environments.
    -   Using the Setup Assistant to easily configure credentials and integration parameters—get started with minimal manual setup.
    -   Scheduling jobs to run periodically to import findings from Tenable.cs, create vulnerable items \(for cloud hosts\), create container vulnerable items and associate them with the relevant cloud resources and container image records.
-   **[Assess vulnerability exposure by publisher](https://www.servicenow.com/docs/access?context=vr-ws-exposure-publisher&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

Starting with v5.0 of Vulnerability Exposure Assessment, a publisher-based assessment is introduced that enables you to assess the vulnerability impact by vendor. For example, Microsoft, and Red Hat. By focusing on recently disclosed vulnerabilities from critical vendors, you can prioritize remediation and proactively address threats, improving your overall security posture.

-   **[View risk score details of a vulnerable item in the Work notes section](https://www.servicenow.com/docs/access?context=vuln-calculators-rules&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

Starting with v25.0.3 of Vulnerability Response, the system property **sn\_sec\_cmn.risk\_score\_changes\_add\_worknotes** is inactive by default. If you enable it, only then you can see all the changes related to the risk score of a vulnerable item in the Work notes section. Additionally, the work notes are updated only if there’s a change in the risk score.

-   **[Quick Start Tests for Vulnerability Response](https://www.servicenow.com/docs/access?context=available-quick-start-tests&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

After upgrades and deployments of new applications or integrations, run quick start tests to verify that Vulnerability Response works as expected. If you customized Vulnerability Response, copy the quick start tests and configure them for your customizations.

-   **[Enhancements to exception rules handling](https://www.servicenow.com/docs/access?context=direct-deferral-of-vits-by-exception-rules-without-remediation-task-creation&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**
    -   Exception rules are reevaluated with nightly scheduled jobs.
    -   Vulnerable items that no longer match exception rule conditions are unlinked from remediation tasks.
    -   A deferred vulnerable item \(VIT\) is reopened if it doesn’t match any active exception rules.
    -   Exception rules don’t create remediation tasks. VITs are deferred directly and aren’t associated with a remediation task.
-   **[Tenable's endpoint scanning integration](https://www.servicenow.com/docs/access?context=tenable-io-integrations-list&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

Support for Tenable's endpoint scanning integration to retrieve scan metadata. The integration fetches scan details using the last\_schedule\_id from existing asset data in Tenable.io.

-   **Reopened Count field on vulnerable items**

Added the Reopened Count field on vulnerable items to track the number of times their states change from 'Closed' to 'Open' or to 'Active'.

-   **[Out-of-the-box vendor advisories via Common Security Advisory Framework \(CSAF\) integration](https://www.servicenow.com/docs/access?context=vuln-solution-mgmt&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

The following vendor advisories are configured out-of-the-box and are automatically activated when the Solution Management plugin is enabled: Redhat and Suse.


</td></tr><tr><td>

Workforce Optimization for Customer Service CSM

</td><td>

-   **[View the monthly staff alignment on the team calendar in the Manager Workspace](https://www.servicenow.com/docs/access?context=scheduling-configurable-wfo-cs&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

Enable managers to plan, monitor, and adjust staffing more effectively with the month view on the Team Calendar tab in the Schedule page of the Manager Workspace. You can also view staffing and shift details across a full month to optimize and identify gaps in coverage, detect over staffing, and take proactive steps to balance workloads improving operational efficiency and responsiveness.

-   **[View the monthly schedule on the team calendar in the Configurable CSM or FSM Workspace](https://www.servicenow.com/docs/access?context=scheduling-configurable-wfo-cs&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

Enable agents to view your upcoming shifts, time-off requests, and availability for the entire month in the month view of the Team Calendar in the CSM or FSM Configurable Workspace. This enables them to better plan their schedules, stay informed, and remain engaged with their work commitments.

-   ****

Decoupling Channel Management from the core Workforce Optimization \(WFO\) modules is necessary during dependencies or emergency situations. This architectural enhancement supports modular deployment, enabling independent updates or scaling of Channel Management without impacting other workforce engagement features.

    -   Independent Deployment: Channel Management can be deployed independently, allowing for greater flexibility and control.
    -   Reduced Inter-Module Dependencies: The decoupling reduces dependencies between modules, enhancing system stability.
    -   Enhanced Scalability and Maintainability: The new architecture improves scalability and maintainability, making it easier to manage and expand.
    -   Streamlined Future Upgrades: Future upgrades for individual modules can be streamlined, ensuring smoother and more efficient updates.

</td></tr><tr><td>

Zero Copy Connector Hub

</td><td>

-   **[Established connections](https://www.servicenow.com/docs/access?context=connections-wdf&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US)**

Retrieve real-time data from external sources directly in the ServiceNow AI Platform, without copying any data to your instance using zero copy connections.

-   **[Data fabric tables](https://www.servicenow.com/docs/access?context=data-fabric-tables-wdf&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US)**

Enable data consumers to access external data on the ServiceNow AI Platform to power AI features and build applications using data fabric tables.

-   **[Connect to Teradata](https://www.servicenow.com/docs/access?context=teradata-wdf&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US)**

Retrieve data from Teradata in real-time without copying or duplicating the data.

-   **[Connect to Amazon S3 tables](https://www.servicenow.com/docs/access?context=amazon-s3-tables-wdf&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US)**

Retrieve data from Amazon S3 tables in real-time without copying or duplicating the data.


</td></tr><tr><td>

Zero Copy Connector for ERP

</td><td>

[Zurich Patch 4](../quality/zurich-patch-4.md)

-   **[Use agentic AI](https://www.servicenow.com/docs/access?context=now-assist-erp-aiagents-data-explorer-workflow&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US)**

Discover ERP database table information and identify relevant ERP Data Product models using the Explore ERP models agentic AI workflow in Now Assist for Zero Copy Connector.

-   **[Now Assist for Zero Copy Connector skills](https://www.servicenow.com/docs/access?context=now-assist-for-zero-copy-connectors-skills&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US)**

More easily identify SAP objects like tables, BAPI endpoints, and OData endpoints that can then be used to query the data you need with the ERP Data Query skill. Query SAP standard database tables for data and transactional records using the ERP Data Discovery skill.

-   **[Some Now Assist skills are turned on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Zurich Patch 4\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.
-   **[Use AI to discover model entity options](https://www.servicenow.com/docs/access?context=use-ai-to-help-add-an-entity-to-a-model&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US)**

Use ask AI in model manager to obtain detailed entity options by describing the entity you want to add to a model.

-   **[Set security on model operations](https://www.servicenow.com/docs/access?context=erp-canvas-set-operation-level-security-on-a-model&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US)**

Apply roles and user group names to control access to create, read, and update model operations.

-   **[More easily create model operation entity inputs and outputs using scriptable API](https://www.servicenow.com/docs/access?context=sn_erp_integrationBothAPI&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)**

Query complex request/response structures faster and easier using scriptable Glide APIs for models instead of Flow Designer.

-   **[Check that your production instance has the latest version of a model](https://www.servicenow.com/docs/access?context=erp-use-model-versioning&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US)**

Determine if production and non-production instances are using the same or different versions of a model to check if the latest model updates are on your production instance.

-   **[Create and change SAP business entities with IDoc](https://www.servicenow.com/docs/access?context=create-and-change-sap-business-entities-with-idoc&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US)**

Work with SAP business entities that can only be created or changed using IDOC.

-   **[Control data access for ERP AI agents](https://www.servicenow.com/docs/access?context=zero-copy-connector-for-erp-ai-agents-use-cases&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US)**

Grant, modify, and revoke AI agent data access with specific read, write, and query privileges.

-   **[Use ETag in update operations](https://www.servicenow.com/docs/access?context=erpc-manage-models-read-op&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US)**

Create update operations where ETag is required and OData services are used. The ETag is fetched by default and sent with the update call.

-   **[SAP ECC and SAP S/4HANA are now primary connectors](https://www.servicenow.com/docs/access?context=primary-connectors-wdf&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US)**

The SAP ECC and SAP S/4HANA connectors are now primary connectors in Workflow Data Fabric Zero Copy Connectors.

-   **[Upload data from SAP SuccessFactors](https://www.servicenow.com/docs/access?context=obtain-data-from-successfactors-using-odata-v2-apis&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US)**

Access data from SAP SuccessFactors using OData V2 APIs and use the information in Zero Copy Connector for ERP models.

-   **[Use automatic mapping to map table fields between systems faster](https://www.servicenow.com/docs/access?context=erpc-manage-model-inputs&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US)**

Map table fields between systems faster with automatic mapping.

-   **[View session-level debugging logs](https://www.servicenow.com/docs/access?context=debug-zero-copy-connector-for-erp-models&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US)**

View debug logs from within Zero Copy Connector for ERP to obtain information about requests, responses, and payloads without having to open Workflow Studio.


</td></tr></tbody>
</table>**Parent Topic:**[Release notes summaries for Zurich features](../release-notes-summaries.md)


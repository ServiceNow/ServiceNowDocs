---
title: New features and products in Australia
description: Cumulative release notes summary on new Australia features and products.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-04-08"
reading_time_minutes: 194
breadcrumb: [Release notes summaries for Australia features, Release notes for upgrading from Zurich, Learn about the Australia release, Australia release notes]
---

# New features and products in Australia

Cumulative release notes summary on new Australia features and products.

New products were introduced in Australia, and additional features were added to existing  products.

<table id="rn-summary-new-features-tables" class="custom-rows"><thead><tr><th class="filter">

Application or feature

</th><th>

Details

</th></tr></thead><tbody><tr><td>

AI Control Tower

</td><td>

-   **[Security &amp; Privacy tab in AI Control Tower](https://www.servicenow.com/docs/access?context=security-privacy-tab&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)**
    -   Customize the AI security score by weighting security categories that comprise the score. The score formula was changed to an average across all AI assets. The score was renamed to AI asset security score.
    -   Measure whether your model's output or behavior violates predefined security policies using the security policy violations chart.
    -   Review potential threats in AI agent output in agent goal hijack, output with PII detected, and high-risk output charts.
    -   Monitor MCP server access by AI Gateway with these new charts: Clients connecting to MCP servers, authorized access attempts, and failed access attempts.
    -   The Prompt injection, Offensive content, and Sensitive data tabs have been removed and replaced by Access and Guardrails tabs. Metrics have been reorganized into those two tabs.
    -   In **Configurations**, under **Data**, the **Data privacy** tab was renamed to **Security &amp; privacy**. In that tab, the data leak detection and anonymization section was renamed to sensitive data input and anonymization.
-   **[Data section on Configurations page](https://www.servicenow.com/docs/access?context=data&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)**

Enable and set up security policy violations, agent goal hijack, and output screening metrics to measure the integrity of your data model and potential threats in LLM output.

-   **[Manage agentic AI system life cycles](https://www.servicenow.com/docs/access?context=create-ai-system-assets&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)**

Create AI system assets to track and manage the complete life cycles of your agentic AI systems, from onboarding to deployment. Gain comprehensive insight into each agentic AI system and take any necessary actions to successfully complete each life-cycle stage. By managing the life cycles of your agentic AI systems, you can extend their lifespans, reduce downtime, and optimize licensing costs.

-   **[Define the use and purpose of an AI system](https://www.servicenow.com/docs/access?context=create-ai-system-assets&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)**

Specify the intended use and purpose of an AI system. Provide insight into who is using the AI system, what the AI system is being used for, and how the AI system works and provides value. This information can help you determine the benefits and risks that are associated with the AI system. For more information on classifying AI systems based on regulatory risk at intake by applying a configured Risk Assessment Methodology \(RAM\), see [AI Risk and Compliance release notes](../governance-risk-compliance/grc-ai-risk-and-compliance-rn.md) and [Assessment templates and risk assessment methodologies](https://www.servicenow.com/docs/access?context=assessment-templates-rams&version=australia&pubname=australia-governance-risk-compliance&ft:locale=en-US).

-   **[Associate additional related AI asset types with AI systems](https://www.servicenow.com/docs/access?context=create-ai-system-assets&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)**

Associate the following additional related AI asset types with your AI systems:

    -   If an AI system has an Asset type of Generative AI or Agentic AI, you can associate it with any of its supported components or subsystems.
    -   If an AI system has an Asset type of Agentic AI, you can associate it with any of its integrated AI tools.
-   **[Create change and offboarding requests for additional AI asset types](https://www.servicenow.com/docs/access?context=creating-ai-asset-requests&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)**

Create change requests for the following additional AI asset types:

    -   AI systems with an Asset type of Agentic AI
    -   Datasets
In addition, create offboarding requests for the following additional AI asset types:

    -   AI systems with an Asset type of Agentic AI
    -   AI models
    -   Datasets
    -   MCP servers
-   **[ServiceNow product tiers](https://www.servicenow.com/docs/access?context=ai-native-sku-overview&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)**

The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets, and create your own
Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.


-   **[Enterprise AI discovery: Unlock Visibility, Governance &amp; Value](https://www.servicenow.com/docs/access?context=enterprise-ai-discovery&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)**

AI connections are created using AI Service Graph Connectors. AI connections are combination of hyperscalars, AI apps, and agentic AI frameworks.

The AI Service Graph Connectors available from March 2026

    -   [AWS](https://www.servicenow.com/docs/access?context=aws_0&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)
    -   [Microsoft](https://www.servicenow.com/docs/access?context=microsoft&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)- Azure Foundry and Copilot
    -   [Google Cloud Platform \(GCP\) Vertex AI](https://www.servicenow.com/docs/access?context=gcp-vertex-ai&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)
    -   [n8n](https://www.servicenow.com/docs/access?context=n8n&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)
    -   [LangGraph](https://www.servicenow.com/docs/access?context=langgraph&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)
    -   [Salesforce](https://www.servicenow.com/docs/access?context=salesforce&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)
-   **[Assets list- managed and unmanaged assets](https://www.servicenow.com/docs/access?context=assets-list-managing-and-unmanaging-assets&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)**

Managed assets benefit from AI Control Tower features such as governance, lifecycle management, value assessment, risk classification, security, and privacy. Unmanaged assets, on the other hand, do not have access to these AI Control Tower capabilities.

-   **[AI Gateway](https://www.servicenow.com/docs/access?context=ai-gateway-overview&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)**

AI Gateway offers MCP Global Clients, which can be used across all servers.

A Gateway offers MCP Catalog to choose while adding MCP servers.

MCP server can be added to an AI Asset inventory from AI Control Tower.


</td></tr><tr><td>

AI Risk and Compliance

</td><td>

-   **[Risk‑based classification during intake](https://www.servicenow.com/docs/access?context=request-ai-system&version=australia&pubname=australia-governance-risk-compliance&ft:locale=en-US)**

After upgrading to version 22.0.3, if you have the AI risk and compliance business user \[sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_business\_user\] role, you can now classify AI systems using a risk‑based approach at intake, enabling organizations to capture AI risk context early and align governance workflows with regulatory and internal risk requirements. This improvement to the AI use case request form supports more accurate AI oversight throughout the system life cycle.

-   **[Report an AI case anonymously](https://www.servicenow.com/docs/access?context=report-ai-case-anon&version=australia&pubname=australia-governance-risk-compliance&ft:locale=en-US)**

After upgrading to version 22.0.3, if you have the AI case business user \[sn\_ai\_case\_mgmt.ai\_case\_business\_user\] role, you can navigate to the Employee Center to access the Anonymous Reporting Center and submit AI cases anonymously, enabling broader participation in AI governance while protecting the identity of reporters. No additional role is required to submit an anonymous report directly through the Anonymous Reporting Center. Broader participation helps organizations identify potential AI risks earlier by removing barriers to case submission.

-   **[Offboard AI models and datasets](https://www.servicenow.com/docs/access?context=airc-offboarding-ai-assets&version=australia&pubname=australia-governance-risk-compliance&ft:locale=en-US)**

After upgrading to version 22.0.3, if you have the AI risk and compliance analyst \[sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_analyst\] or AI risk and compliance manager \[sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_manager\] role you can manage AI asset offboarding life cycle tasks. Managing these tasks helps ensure that governance‑related activities, such as risk and impact assessments, conformity reviews, issue closure, and audit documentation, are addressed when an AI asset is retired or removed from active use.


</td></tr><tr><td>

AI Search

</td><td>

-   **[Improve search precision and contextual relevance with hybrid search](https://www.servicenow.com/docs/access?context=hybrid-search-ais&version=australia&pubname=australia-platform-administration&ft:locale=en-US)**

Hybrid search combines keyword-based search with semantic understanding to deliver more accurate and relevant search results, with fewer zero-result searches.

-   **[Configure AI Search as the source for Ask Now Assist suggestions](https://www.servicenow.com/docs/access?context=configure-ai-search-source-ask-now-assist-suggestions&version=australia&pubname=australia-platform-administration&ft:locale=en-US)**

Admins can configure the system to use AI Search as the source for Ask Now Assist suggestions in enhanced chat. Making this change activates suggestion term highlighting in Ask Now Assist and provides improvements such as wildcard searching and lemmatization for suggestions.


</td></tr><tr><td>

AI-native IT Service Management

</td><td>

-   **[Simplified AI-native employee experience](https://www.servicenow.com/docs/access?context=employee-experience-native-ai-itsm&version=australia&pubname=australia-it-service-management&ft:locale=en-US)**

Simplify meeting employee needs by leveraging the automated self-service and browsing experience in the Employee Center portal. The following capabilities are available as part of the employee experience:

    -   A simplified Employee Center portal with a conversational experience that supports chat, catalog, and knowledge content.
    -   Prebuilt catalog items for common IT issues and requests.
    -   Requester surveys for incidents and requested items.
    -   Multi-channel support through Employee Center, email, Microsoft Teams, and Slack.
-   **[Simplified AI-native fulfiller experience](https://www.servicenow.com/docs/access?context=fulfiller-experience-ai-native-itsm&version=australia&pubname=australia-it-service-management&ft:locale=en-US)**

Provide an efficient IT support experience for incident and request management by leveraging AI recommendations for the following:

    -   Resolution steps and knowledge base recommendations
    -   Incident and chat summaries
    -   Resolution notes and email response generation
    -   Recommended actions such as linking similar incidents or ordering catalog items
A role-based manager dashboard with key service desk metrics, date-range filtering, and agent-level filtering is available.

-   **[Automated and guided administrator experience](https://www.servicenow.com/docs/access?context=configuring-ai-native-itsm&version=australia&pubname=australia-it-service-management&ft:locale=en-US)**

Set up multiple ITSM workflows \(incident management and request management\) by leveraging the guided and conversational setup process. The following capabilities are available for administrators:

    -   Default configuration settings that are automatically applied to installed products or modules. You can review and modify these settings.
    -   A guided configuration experience.
    -   AI agents to configure ITSM workflows from a single admin UI page using natural language. See [Conversational AI Agents for configurations](https://www.servicenow.com/docs/access?context=agents-ai-native-it-service-desk&version=australia&pubname=australia-it-service-management&ft:locale=en-US).

</td></tr><tr><td>

API

</td><td>

<table id="table_tcd_5v3_wqb"><thead><tr><th>

Class

</th><th>

Methods

</th></tr></thead><tbody><tr><td>

[CopyDynamicSchemaAPI - Scoped, Global](https://www.servicenow.com/docs/access?context=CopyDynamicSchemaAPI&version=australia&pubname=australia-api-reference&ft:locale=en-US)

</td><td>

Methods:

-   getCopyApi\(\)
-   skipAttributes\(\)
-   skipChoiceOverrides\(\)
-   skipChoiceSets\(\)
-   getTransactionId\(\)
-   runAsync\(\)

 Extension points:

-   getCopyName\(\)
-   shouldCopy\(\)
-   verifyCopyOperation\(\)

</td></tr><tr><td>

[GlideDate - Scoped](https://www.servicenow.com/docs/access?context=c_GlideDateScopedAPI&version=australia&pubname=australia-api-reference&ft:locale=en-US)

</td><td>

-   getDisplayValueEx\(\)
-   setDisplayValueEx\(\)

</td></tr><tr><td>

[GlideTime - Scoped](https://www.servicenow.com/docs/access?context=c_GlideTimeScopedAPI&version=australia&pubname=australia-api-reference&ft:locale=en-US)

</td><td>

-   getDisplayValueEx\(\)
-   getDisplayValueLang\(\)
-   setDisplayValueEx\(\)
-   setDisplayValueLang\(\)

</td></tr></tbody>
</table><table id="table_ldq_g3c_tcc"><thead><tr><th>

Class

</th><th>

Methods

</th></tr></thead><tbody><tr><td>

[CopyDynamicSchemaAPI - Scoped, Global](https://www.servicenow.com/docs/access?context=CopyDynamicSchemaAPI&version=australia&pubname=australia-api-reference&ft:locale=en-US)

</td><td>

Methods:

-   getCopyApi\(\)
-   skipAttributes\(\)
-   skipChoiceOverrides\(\)
-   skipChoiceSets\(\)
-   getTransactionId\(\)
-   runAsync\(\)

 Extension points:

-   getCopyName\(\)
-   shouldCopy\(\)
-   verifyCopyOperation\(\)

</td></tr><tr><td>

[GlideDate - Global](https://www.servicenow.com/docs/access?context=GlideDateAPI&version=australia&pubname=australia-api-reference&ft:locale=en-US)

</td><td>

-   getDisplayValueEx\(\)
-   setDisplayValueEx\(\)

</td></tr><tr><td>

[GlideElement - Global](https://www.servicenow.com/docs/access?context=c_GlideElementAPI&version=australia&pubname=australia-api-reference&ft:locale=en-US)

</td><td>

getDynamicNamespace\(\)

</td></tr><tr><td>

[GlideElementDynamicAttributeStore - Global](https://www.servicenow.com/docs/access?context=GlideElementDynamicAttStoreAPI&version=australia&pubname=australia-api-reference&ft:locale=en-US)

</td><td>

-   getDynamicAttributePathsInSchema\(\)
-   getDynamicAttributePathsInStore\(\)
-   getDynamicNamespaceName\(\)

</td></tr><tr><td>

[MIDHermesProducer - Global](https://www.servicenow.com/docs/access?context=MIDHermesProducerAPI&version=australia&pubname=australia-api-reference&ft:locale=en-US)

</td><td>

-   MIDHermesProducer\(\)
-   send\(\)

</td></tr></tbody>
</table><table id="table_gmt_y3c_tcc"><thead><tr><th>

API

</th><th>

Endpoints

</th></tr></thead><tbody><tr><td>

[Attachment API](https://www.servicenow.com/docs/access?context=c_AttachmentAPI&version=australia&pubname=australia-api-reference&ft:locale=en-US)

</td><td>

-   DELETE /now/attachment/\{attachment\_sys\_id\}/attributes
-   DELETE /now/attachment/\{attachment\_sys\_id\}/attributes/\{attribute\_key\}
-   GET /now/attachment/\{attachment\_sys\_id\}/attributes/\{attribute\_key\}
-   GET /now/attachments/\{attachment\_sys\_id\}/attributes
-   PATCH /now/attachment/\{sys\_id\}
-   POST /now/attachment/\{attachment\_sys\_id\}/attributes
-   PUT /now/attachment/\{attachment\_sys\_id\}/attributes/\{attribute\_key\}

</td></tr><tr><td>

[Help Request API](https://www.servicenow.com/docs/access?context=help-request-api&version=australia&pubname=australia-api-reference&ft:locale=en-US)

</td><td>

POST /now/helprequest/action/create\_or\_update

</td></tr><tr><td>

[ATF Code Coverage API](https://www.servicenow.com/docs/access?context=atf-code-coverage-api&version=australia&pubname=australia-api-reference&ft:locale=en-US)

</td><td>

-   POST /now/atf/code\_coverage/all
-   POST /now/atf/code\_coverage/by\_line\_number
-   POST /now/atf/code\_coverage/by\_script\_id

</td></tr></tbody>
</table>|API|Operations|
|---|----------|
|[Warranty Claims SOAP API](https://www.servicenow.com/docs/access?context=warranty-claims-SOAP-API&version=australia&pubname=australia-manufacturing&ft:locale=en-US)|ProcessRepairOrder: A STAR SOAP operation used to process and exchange repair operation–level information between systems in a standardized STAR XML format.|

</td></tr><tr><td>

Accounts Payable Operations

</td><td>

-   **[Tax Engine Integration](https://www.servicenow.com/docs/access?context=tax-engine-integration&version=australia&pubname=australia-source-to-pay-operations&ft:locale=en-US)**

The tax engine integration framework validates supplier-provided tax against system tax at invoice line level, maintains compliance with regional and global tax regulations. This integration triggers automatic tax validation, handles exceptions for tax variance and missing data, enables manual revalidation and rolling up of system tax.


</td></tr><tr><td>

Activity Management

</td><td>

CRM Outlook Add-in

-   **[Associate an email with an existing CRM record](https://www.servicenow.com/docs/access?context=associate-email-crm-outlook&version=australia&pubname=australia-order-management&ft:locale=en-US)**

Associate customer emails to the correct ServiceNow CRM record without leaving Microsoft Outlook. Manually search and associate emails with leads, opportunities, accounts, or contacts, so that engagement context is captured immediately and remains available for future correspondence and follow‑up.

-   **[Create new leads and contacts from email](https://www.servicenow.com/docs/access?context=create-crm-entity-outlook&version=australia&pubname=australia-order-management&ft:locale=en-US)**

Create a new lead or contact directly from an email when no matching CRM record exists, and automatically attach the originating email to the newly created record to preserve engagement history.


CRM Touchpoints

-   **[Touchpoints on CRM entities](https://www.servicenow.com/docs/access?context=create-crm-touchpoint&version=australia&pubname=australia-order-management&ft:locale=en-US)**

Capture and track engagement activities for prospects and customers across communication channels such as email, phone, virtual meeting, in-person meetings, and social interactions by creating touchpoint records. Associate touchpoints with leads, opportunities, accounts, and contacts to maintain a complete engagement history.

-   **[Custom touchpoint types](https://www.servicenow.com/docs/access?context=create-custom-touchpoint-types&version=australia&pubname=australia-order-management&ft:locale=en-US)**

Define custom touchpoint types in addition to the default types of discovery, demo, and customer business review \(CBR\), and so on to match your organization's specific engagement processes.

-   **[Activity capture and tracking](https://www.servicenow.com/docs/access?context=using-activity-management&version=australia&pubname=australia-order-management&ft:locale=en-US)**

Capture emails, calls, meetings, and tasks within touchpoints such as discovery, demo, business value assessment, or CBRs in a single system of record. Track metrics such as primary channel and time spent for every interaction, giving leadership visibility into the activity volume per sales representative.


</td></tr><tr><td>

Adoption Services

</td><td>

-   **[Help Center](https://www.servicenow.com/docs/access?context=help-center&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US)**

text


</td></tr><tr><td>

Advanced Approval Management

</td><td>

-   **[Flexible approval configurations](https://www.servicenow.com/docs/access?context=configuring-advanced-approval-management&version=australia&pubname=australia-order-management&ft:locale=en-US)**

Build workflows that enable sequential approvals, parallel \(simultaneous\) approvals, or a combination of both.

    -   Define workflow approval steps and optional chains that progress through multiple approval levels based on rule evaluations.
    -   Set the approval order using combinations of levels, roles, and conditions.
    -   Define approval users and groups.
    -   Consolidate multiple email notifications on an approval request for an approver so that the approver receives a single email notification.
-   **[Intelligent routing rules and smart reapprovals](https://www.servicenow.com/docs/access?context=set-approval-trigger-conditions&version=australia&pubname=australia-order-management&ft:locale=en-US)**

Automatically trigger approvals by setting conditions based on items such as discount percentage, deal size, and margin thresholds. Configure thresholds and conditions so the approval workflow skips approved steps that have already been approved if the underlying conditions haven't changed.

-   **[Escalations](https://www.servicenow.com/docs/access?context=create-approval-configuration&version=australia&pubname=australia-order-management&ft:locale=en-US)**

Enable approval rule admins to escalate an approval request by reassigning a pending approval request to another approver automatically when the original approver does not act within a specified time.

-   **[Override an approval step](https://www.servicenow.com/docs/access?context=override-approval-step&version=australia&pubname=australia-order-management&ft:locale=en-US)**

As an approval rule writer who also has the approval admin role, override or bypass a pending approval request step to unblock an approval request when the approval is no longer required.

-   **[Automated notifications of approval status](https://www.servicenow.com/docs/access?context=setting-up-approval-notifications&version=australia&pubname=australia-order-management&ft:locale=en-US)**

Inform sales agents and approvers of the status of approval items moving through the approval workflow by setting up notifications. Use predefined system notifications for reminders and escalations.

-   **[Flexible submission for approval requests](https://www.servicenow.com/docs/access?context=submitting-approval-requests&version=australia&pubname=australia-order-management&ft:locale=en-US)**

Before submitting requests for approval, see the required approvals, approver names, approval reasons, and approval sequencing by creating and previewing approval requests. Requesters can recall approval requests for changes and resubmit them.

-   **[Ad-hoc approvers](https://www.servicenow.com/docs/access?context=add-approver&version=australia&pubname=australia-order-management&ft:locale=en-US)**

As a requester or an approver, add one or more approvers or approval groups to an approval request, outside of the predefined approvers for a given rule. Enables approval users to add approvers who have more expertise on certain aspects of the request, for example if there are legal or regulatory issues relevant to the request.

-   **[Real-time status tracking and approval history](https://www.servicenow.com/docs/access?context=tracking-approval-status&version=australia&pubname=australia-order-management&ft:locale=en-US)**

Monitor approval progress and access an audit trail with detailed status for each approval step including assigned approvers, actual approvers \(for completed steps\), approval comments, and assignment and completion timestamps.

-   **[Approval management](https://www.servicenow.com/docs/access?context=approving-approval-requests&version=australia&pubname=australia-order-management&ft:locale=en-US)**
    -   Accept or reject approvals using multiple channels, such as email, push notifications, the CSM Configurable Workspace, or approval centers, such as My Approvals in the ServiceNow AI Platform®.
    -   Assign backup approvers with date-specific coverage periods for seamless continuity of the approval process.

</td></tr><tr><td>

Advanced Risk

</td><td>

-   **[Risk event response template enhancements](https://www.servicenow.com/docs/access?context=create-risk-event-response-template&version=australia&pubname=australia-governance-risk-compliance&ft:locale=en-US)**

After upgrading to version 22.0.x, users with the Risk Manager \[sn\_risk.manager\] or Risk Admin \[sn\_risk.admin\] role can configure risk event response templates using dynamic, entity‑driven assignments. These changes enable assignments to be derived from entity data alongside existing static user or group selection.

You can select user fields defined on the entity \(such as Owner or Sub-owner\) or entity stakeholder personas when configuring:

    -   Risk event owner assignment
    -   Issue creation and assignment
    -   Risk event approvers
-   **[Risk Suggestion AI Agent enhancements](https://www.servicenow.com/docs/access?context=identify-risks-for-entity&version=australia&pubname=australia-governance-risk-compliance&ft:locale=en-US)**

After upgrading the Now Assist for Integrated Risk Management \(IRM\) application to version 22.x, the Risk Suggestion AI Agent supports a more context‑aware and conversational workflow. After selecting risk types, you can provide additional context to refine search results, with the agent dynamically asking follow‑up questions when needed. Before adding risks to the suggested risk section, you can review and modify suggested risks by updating descriptions, renaming risks, or removing items from the list.

-   **[Control Objective workflow](https://www.servicenow.com/docs/access?context=create-control-objective-ws&version=australia&pubname=australia-governance-risk-compliance&ft:locale=en-US)**

After upgrading to version 22.0.x, you can use a defined workflow to update control objectives. Changes can be drafted and reviewed without changing the current active version, which helps avoid unintended changes to related controls, and risk records. Only approved updates become active. The workflow also sets clear responsibility for making updates and helps keep control objective information consistent and up to date.


</td></tr><tr><td>

Advanced Work Assignment \(AWA\)

</td><td>

-   **[Advanced Work Assignment](https://www.servicenow.com/docs/access?context=awa-application-landing-page&version=australia&pubname=australia-conversational-interfaces&ft:locale=en-US)**

Configure routing for non-task and non-interaction tables such as leads, opportunities, orders, and quotes in AWA.

-   **[Advanced Work Assignment](https://www.servicenow.com/docs/access?context=awa-application-landing-page&version=australia&pubname=australia-conversational-interfaces&ft:locale=en-US)**

Use telephone-style transfer workflows in AWA to enable warm transfers where agents consult privately before merging calls with the customer.


</td></tr><tr><td>

Agent Workspace for HR Case Management

</td><td>

-   **[Integration with Contact Center as a Service \(CCaaS\)](https://www.servicenow.com/docs/access?context=enable-hr-icc&version=australia&pubname=australia-employee-service-management&ft:locale=en-US)**

Implement prebuilt, certified integrations with Contact Center as a Service \(CCaaS\) providers using the ServiceNow voice reference architecture. The Interaction Controls Component \(ICC\) feature enables CCaaS providers to display native voice and callback integrations so HR agents can manage customer calls directly from HR Agent Workspace. HR agents are provided a brief wrap-up period at the end of customer conversations to complete their work before moving on to assist other customers.

-   **[Recommended Actions for HRSD](https://www.servicenow.com/docs/access?context=recommended-actions-hrsd&version=australia&pubname=australia-employee-service-management&ft:locale=en-US)**

Recommend actions based on the context of the HR case, helping agents resolve case faster.

    -   Lists KB articles and similar cases in the context of the current case.
    -   Suggests to add an approval to the case only when an approval is required.
-   **[Case creation configuration](https://www.servicenow.com/docs/access?context=agent-ws-configurable-hr-create-case&version=australia&pubname=australia-employee-service-management&ft:locale=en-US)**

Enable an HR agent to quickly review the HR profiles of both **subject person** and **opened for** during the case creation process.


-   **[Advanced Knowledge Editor](https://www.servicenow.com/docs/access?context=advance-knowledge-editor&version=australia&pubname=australia-employee-service-management&ft:locale=en-US)**

Streamline Knowledge article creation and editing with AI support in an improved, intuitive editor. Leverage AI powered Article optimizations recommendations to improve the knowledge content quality.


</td></tr><tr><td>

Agent experience for CSM

</td><td>

-   **[Dock in CSM Configurable Workspace](https://www.servicenow.com/docs/access?context=csm-config-ws-bottom-utility-bar&version=australia&pubname=australia-customer-service-management&ft:locale=en-US)**

Enable agents to minimize drafts of comments, work notes, or emails to a dock at the bottom of the workspace page. This centralized location provides agents with the ability to see all current drafts at a glance.

-   **[Form template enhancements](https://www.servicenow.com/docs/access?context=csm-workspace-form-templates&version=australia&pubname=australia-customer-service-management&ft:locale=en-US)**

Save time and promote consistency by creating conditional templates, setting field-level conditions, and automatically populating email body text. Populate these fields using dynamic values from the Case table and related tables. Preview template changes before applying them to a record.

-   **[Workspace record page interoperability](https://www.servicenow.com/docs/access?context=csm-config-ws-pages-templates&version=australia&pubname=australia-customer-service-management&ft:locale=en-US#section_q4z_fm3_23c)**

Enable agents to use record pages between CSM Configurable Workspace and ITSM Service Operations Workspace. The following ITSM pages are interoperable across CSM:

    -   Incident page
    -   Change page
-   **[AI interaction wrap-up](https://www.servicenow.com/docs/access?context=interaction-wrapup-ai-generated&version=australia&pubname=australia-customer-service-management&ft:locale=en-US)**

Provide agents with AI assistance during the interaction wrap-up period. This feature generates wrap-up content for interaction records, such as the wrap-up code and notes.

-   **[Highlight fields with unsaved changes](https://www.servicenow.com/docs/access?context=csm-workspace-agent-actions&version=australia&pubname=australia-customer-service-management&ft:locale=en-US#section_zzp_dn3_23c)**

Use visual indicators in CSM Configurable Workspace such as icons and background colors to indicate form fields with unsaved changes.

-   **[Knowledge Center article editor available in CSM Configurable Workspace](https://www.servicenow.com/docs/access?context=csm-workspace-create-knowledge&version=australia&pubname=australia-customer-service-management&ft:locale=en-US)**

Use the Knowledge Center article editor to create and edit knowledge articles in CSM Configurable Workspace. Agents can access the editing capabilities available in the article editor to format knowledge article content such as text, images, and media.

-   **[Unread email count on interaction tabs](https://www.servicenow.com/docs/access?context=csm-email-interaction-record-page&version=australia&pubname=australia-customer-service-management&ft:locale=en-US#section_rfs_4lt_13c)**

Displays the number of unread email messages on interaction tabs in CSM Configurable Workspace. Hovering over a tab displays a tooltip with a preview of the most recent email.


</td></tr><tr><td>

Agentic Contact Center for Banking

</td><td>

-   **[Customer 360 workspace](https://www.servicenow.com/docs/access?context=customer-360-agentic-contact-center-for-banking&version=australia&pubname=australia-financial-services-operations&ft:locale=en-US)**

The AI-powered Customer 360 workspace provides a unified single view of customer information across accounts, cases, and customer history. AI-generated summaries, insights, and recommendations help CSRs quickly understand customer profiles and determine the most effective next steps.

-   **[CSR Interaction workspace](https://www.servicenow.com/docs/access?context=interaction-workspace-for-agentic-contact-center-for-banking&version=australia&pubname=australia-financial-services-operations&ft:locale=en-US)**

The AI-powered CSR Interaction workspace streamlines live customer conversations by displaying customer details, account information, and interaction history. The customer support AI agent provides real-time contextual insights, call summaries, and recommended next steps to reduce manual effort and decrease handle time.

-   **[Roles for Banking personal and business CSRs](https://www.servicenow.com/docs/access?context=components-installed-with-agentic-contact-center-for-banking&version=australia&pubname=australia-financial-services-operations&ft:locale=en-US)**

This application includes roles that grant access to AI-assisted CSR experiences for business and personal banking and wealth customers.


</td></tr><tr><td>

App Engine Management Center

</td><td>

-   **[Release lifecycle documentation AI agent](https://www.servicenow.com/docs/access?context=release-lifecycle-documentation-agent-landing&version=australia&pubname=australia-application-development&ft:locale=en-US)**

Improve transparency across your app development environment using the release lifecycle documentation AI agent, available with Now Assist for Creator, to generate update set descriptions and release notes seamlessly.


</td></tr><tr><td>

Application Manager

</td><td>

-   **[Now Assist suites for version compatibility](https://www.servicenow.com/docs/access?context=now-assist-app-mgr&version=australia&pubname=australia-platform-administration&ft:locale=en-US)**

Use the Application Manager to install and update Now Assist applications with suites of compatible application versions. Now Assist suites help verify that new Now Assist applications and versions remain compatible with the ones already installed to your instance.

-   **[Application state indicators](https://www.servicenow.com/docs/access?context=app-mgr-state-indicators&version=australia&pubname=australia-platform-administration&ft:locale=en-US)**

Review information about any applicable installation considerations, requirements, and blockers in the header of application details.


</td></tr><tr><td>

Application Vulnerability Response

</td><td>

-   **[Wiz Application Vulnerability Response Integration](https://www.servicenow.com/docs/access?context=wiz-exploring-avr-sca-secrets&version=australia&pubname=australia-security-management&ft:locale=en-US)**

Import application, Software Composition Analysis \(SCA\), findings, Secrets \(passwords, tokens and keys\) data with the following Wiz Vulnerability integrations:

    -   Application List Integration
    -   SCA Findings Integration
    -   Secret Findings Integration
You can configure these integrations on the Wiz Vulnerability Integration configuration page along with the other Wiz Vulnerability integrations. View imported application list data such as Product Model and Source application ID from Wiz on the Discovered Applications \[sn\_vul\_app\_release\] table records, and SCA and Secrets data on the Application Vulnerable Items \[sn\_vul\_app\_vulnerable\_item\] table records.

-   **[GitHub Application Vulnerability Integration – Generic secrets support](https://www.servicenow.com/docs/access?context=configure-github-vulnerability&version=australia&pubname=australia-security-management&ft:locale=en-US)**

The GitHub Secret Scanning Integration supports imports of generic secrets in addition to standard secrets from your GitHub repositories. An enhanced Manage generic secrets in ServiceNow configuration option lets you control whether generic secrets are ingested. Imported secrets are mapped to Application Vulnerable Items \(AVITs\) with the scan type, Secret, while generic secrets are mapped with the scan type, Generic Secret.

-   **[Improved vulnerability assessment workflows](https://www.servicenow.com/docs/access?context=vr-ws-vuln-assessment&version=australia&pubname=australia-security-management&ft:locale=en-US)**
    -   CI filtering for vulnerability assessments: You can now filter which configuration items are included in a vulnerability assessment using a condition builder.
    -   Business Application population on AVITs: AVITs created from SBOM assessment results now include Business Application information, helping you understand application impact and prioritize remediation.
    -   Priority roll‑down from vulnerability assessments: Updates to the priority of a vulnerability assessment now automatically roll down to associated VITs and AVITs, ensuring consistent prioritization based on the highest severity.
-   **[Enhanced Compensatory controls](https://www.servicenow.com/docs/access?context=requesting-approving-risk-reduction&version=australia&pubname=australia-security-management&ft:locale=en-US)**

When new vulnerable items are ingested and associated with a remediation task that already has an approved compensating control, the reduced risk rating is now automatically inherited by those new vulnerable items.


</td></tr><tr><td>

Asset Audit Response

</td><td>

-   **[Automate the summarization of evidence requests](https://www.servicenow.com/docs/access?context=fulfill-evidence-requests-guided-experience&version=australia&pubname=australia-it-asset-management&ft:locale=en-US)**

Use generative AI to summarize completed and in-progress evidence requests for your ﬁnancial regulatory audits. Gain insight into the corresponding audit engagements, the associated financial regulations, and the evidence that was submitted for each request. In addition, view details about the remediation rules that were created for each request and the corresponding remediation tasks that were generated based on those rules. Use this information to help plan for and complete other in-progress evidence requests so that you can improve your operational efficiency.

-   **[Track impacted records that require remediation](https://www.servicenow.com/docs/access?context=fulfill-evidence-requests-guided-experience&version=australia&pubname=australia-it-asset-management&ft:locale=en-US)**

Use the Impacted Records related list in your remediation tasks to track and take any necessary actions on the impacted records, including asset and configuration item \(CI\) records, that are associated with each task. These remediation tasks are automatically generated based on the remediation rules that you define during evidence request fulfillment.

-   **[View citations for your evidence requests](https://www.servicenow.com/docs/access?context=fulfill-evidence-requests-guided-experience&version=australia&pubname=australia-it-asset-management&ft:locale=en-US)**

Gain insight into the citations that are associated with your evidence requests by using the Citation details fields in the Asset Response Guided Experience. Use these fields to identify the name, description, and supplemental guidance for any citation that is associated with a request.

-   **[Streamline the fulfillment of evidence requests by using financial regulatory context from the Digital Operational Resilience Act \(DORA\)](https://www.servicenow.com/docs/access?context=audit-workspace&version=australia&pubname=australia-it-asset-management&ft:locale=en-US)**

Associate your evidence requests with financial regulatory requirements and guidelines from the Digital Operational Resilience Act \(DORA\). By aligning the relevant requests with these requirements and guidelines, you can help your asset managers better understand the compliance obligations that are associated with each request. They can then use this information to fulfill each request more accurately and efficiently.

-   **[ServiceNow product tiers](https://www.servicenow.com/docs/access?context=ai-native-sku-overview&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)**

The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets, and create your own
Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.


</td></tr><tr><td>

Authentication

</td><td>

-   **[Authentication factors for AI voice service](https://www.servicenow.com/docs/access?context=authentication-factors&version=australia&pubname=australia-platform-security&ft:locale=en-US)**

Enable caller access to AI voice agents by configuring the required identification and authentication factors.

-   **[Web Embeddables](https://www.servicenow.com/docs/access?context=web-embeddables&version=australia&pubname=australia-platform-security&ft:locale=en-US)**

Secure the web embeddables feature for authenticating the ServiceNow®'s web components that are used in third-party portals.

-   **[Granular admin roles](https://www.servicenow.com/docs/access?context=granular-admin-roles&version=australia&pubname=australia-platform-security&ft:locale=en-US)**

The granular admin role enables developers and administrators to complete administrative configuration tasks for Authentication without requiring the full admin role.


</td></tr><tr><td>

Build Agent

</td><td>

 

</td></tr><tr><td>

Buying Group

</td><td>

-   **[Create separate buying groups for each product family or solution within an account](https://www.servicenow.com/docs/access?context=create-new-buying-groups&version=australia&pubname=australia-order-management&ft:locale=en-US)**

Avoid confusion or overlap and efficiently map the right stakeholders involved in different purchase decision for an account by creating separate buying groups for each product family or solution, which helps account for differing decision‑makers, influencers, and users.

-   **[Add buying group members with different roles](https://www.servicenow.com/docs/access?context=add-buying-group-member&version=australia&pubname=australia-order-management&ft:locale=en-US)**

Enable role‑specific engagement, and improve alignment throughout the buying process by adding buying group members with defined roles.

-   **[Associate multiple buying groups against an opportunity](https://www.servicenow.com/docs/access?context=associate-buying-groups-to-an-opportunity&version=australia&pubname=australia-order-management&ft:locale=en-US)​**

Improve stakeholder visibility, support complex deal management, and enable more targeted engagement across solutions by associating multiple buying groups with an opportunity.


</td></tr><tr><td>

CPQ

</td><td>

-   **[Transaction Access Control](https://www.servicenow.com/docs/access?context=cpq-transaction-manager-transaction-access-control&version=australia&pubname=australia-order-management&ft:locale=en-US)**

Control precisely who can view and edit each transaction to improve security and compliance using Transaction Access Control. Admins and creators automatically receive full access and can grant access to others. Any user with access can also grant or remove access for others.

-   **[Transaction AI – Bulk Line Update via File Upload](https://www.servicenow.com/docs/access?context=cpq-transaction-converse&version=australia&pubname=australia-order-management&ft:locale=en-US)**

Enables AI column and line item mapping to allow for seamless transition from third-party systems. Transaction AI can be used to add items from favorites enabling users to quickly add commonly used products via voice or text. Triggers events for users via voice or chat

-   **AI Admin Uploads for Advanced Product Configurator and Transaction Manager**

Enables admins to upload business and blueprint related context documents to provide Configuration AI and Transaction AI more context of business, standards product information etc.

-   **[Export Lines UI Effect](https://www.servicenow.com/docs/access?context=transaction-manager-layouts-ui-effects&version=australia&pubname=australia-order-management&ft:locale=en-US)**

Export Transaction Lines to a .csv file via a new UI effect. The exported file includes all lines in the transaction that meet the current line sort, filter, and column show/hide settings.

-   **[Layout editor](https://www.servicenow.com/docs/access?context=layout_editor&version=australia&pubname=australia-order-management&ft:locale=en-US)**

Design and maintain layouts in a visual-based editor. Add and organize layout components, configure UI Effect and element properties, manage theming and more, all in an intuitive visual interface.

-   **Share product favorites**

Improve collaboration and user efficiency by sharing saved favorite products and configurations with other users, enabling sharing and reuse of product configurations.

-   **Tenant-configurable namespace prefixes for Salesforce fields**

Configure a custom namespace at the tenant level to align Salesforce fields and references with your managed package. When a custom namespace is set, CPQ uses it for all generated Salesforce fields and all field lookups instead of the default LGK\_ prefix. If no custom namespace is configured, the system defaults to LGK\_ to preserve compatibility with existing tenants.

-   **Dynamic selection of SOM catalog items in the CPQ admin UI**

Select product offerings, product specifications, and product characteristic values directly in the CPQ admin UI without manually entering system IDs. Search and select SOM catalog items using built-in UI selectors when configuring products, creating product rules, or setting up pickers, advanced product actions, BOM enrichments, and library functions.

-   **[Node cloning for solution configuration](https://www.servicenow.com/docs/access?context=node-cloning-for-solution-configuration&version=australia&pubname=australia-order-management&ft:locale=en-US)**

Duplicate an existing solution configuration node in a set, directly from the solution configuration navigation sidebar to use it as the starting point for a new node. The original node in a set must be in the valid state.

-   ****

Manage transaction lines using natural language. You can upload CSV or XLSX files directly in the chat to add or update lines, map file columns to transaction fields through a guided conversation, preview the changes, and apply or cancel them before execution. Target specific transaction lines by referencing line numbers or ranges in your prompts, enabling precise updates such as modifying field values or removing selected lines.

-   **Upload context documents for AI-assisted configuration and quoting**

Upload organizational documents — such as pricing policies, standard operating procedures, product specifications, and playbooks — to provide Config AI and Quote AI with company-specific context during configuration and quoting. Supported formats include Excel, Word, PDF, text, markdown, and images \(with OCR support\). These documents are also used by Transaction AI to improve recommendations, product matching, and event suggestions during transaction sessions.

-   **[Config Converse](https://www.servicenow.com/docs/access?context=cpq-config-converse&version=australia&pubname=australia-order-management&ft:locale=en-US)**

Configure complex products using natural language. Buyers can submit a configuration request through a prompt field on an administrator-designed landing page. The request is processed by an AI agent, which interprets the input and drives the product configuration session. For renewal scenarios, Config AI can reuse a previous configuration as a starting point, enabling faster upsell and cross-sell opportunities while maintaining continuity across renewal cycles. Using Config AI, you can:

    -   Submit product configuration requests using natural language through a prompt field on the landing page.
    -   Complete product configuration through a conversational interface within the buying experience.
    -   Design the Config Converse landing page using the CPQ layout editor with configurable elements such as text, images, fields, and a prompt component.
    -   Allow buyers to skip the landing page using a dismissal preference in the layout editor.
    -   Check for a predicted configuration after the initial buyer request. Apply it automatically when Smart Predict is enabled for both the tenant and the layout. Smart Predict must be enabled separately at the tenant level and at the layout level.
-   **Transaction edit history**

Use the event start time column in the transaction edit history to help admins track the duration of individual transaction events.

-   **Price and quantity ramps in the CPQ Configurator**

Use the CPQ Configurator to configure price and quantity ramps for subscription products with recurring pricing. View and manage ramp segments directly within the configuration session through a summary table and detailed modal. Apply quantity updates as a delta across segments from the effective date, and save all changes back to the source. Relaunch the configurator for ramped products to support MACD scenarios, with child lines inheriting the correct ramp associations.


</td></tr><tr><td>

Card data security

</td><td>

-   **[View documents in the tokenizer service vault](https://www.servicenow.com/docs/access?context=card-data-security-component&version=australia&pubname=australia-financial-services-operations&ft:locale=en-US)**

Use the Card data security container to display documents in the tokenizer service vault without storing sensitive documents in your ServiceNow instance.

-   **[PAN display](https://www.servicenow.com/docs/access?context=reveal-a-pan-using-card-data-security&version=australia&pubname=australia-financial-services-operations&ft:locale=en-US)**

Display, mask, or redact PAN values in the workspace with the Card data security container.

-   **[Updated attachment panel](https://www.servicenow.com/docs/access?context=manage-attachments-in-card-data-security&version=australia&pubname=australia-financial-services-operations&ft:locale=en-US)**

View external documents from card networks, acquirers, and merchants at the transaction level of a dispute, which are stored in the tokenizer service vault.

-   **[Mastercard and Visa integration updates](https://www.servicenow.com/docs/access?context=spokes&version=australia&pubname=australia-financial-services-operations&ft:locale=en-US)**

Updated Mastercard and Visa actions and integrations to support document download in Card data security.


</td></tr><tr><td>

Care Team Operations for Biomed

</td><td>

-   **[Create support requests using Now Assist in Virtual Agent](https://www.servicenow.com/docs/access?context=hcls-agentic-ai-use-cases&version=australia&pubname=australia-healthcare-life-sciences&ft:locale=en-US)**

Create support requests for healthcare IT, biomed, facilities, or environmental services departments through Now Assist in Virtual Agent conversationally. This workflow resolves missing or unclear details through clarifying questions and validates the request using the Care team operations case Intake and Care team operations case Creation AI agents and is available in Care Team Portal and Care Team Mobile.

-   **[Care Team Operations Case Creation Voice AI agent](https://www.servicenow.com/docs/access?context=hco-now-assist-voice-agent&version=australia&pubname=australia-healthcare-life-sciences&ft:locale=en-US)**

The Care Team Operations Case Creation Voice AI Agent enables care team members to create cases conversationally over the phone.

**Note:** For the Care Team Operations Case Creation Voice AI Agent to create cases, the Care Team Operations plugin for cases of that request type must be installed.


-   **[ServiceNow product tiers](https://www.servicenow.com/docs/access?context=ai-native-sku-overview&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)**

The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets, and create your own
Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.


</td></tr><tr><td>

Care Team Operations for Environmental Services

</td><td>

-   **[Create support requests using Now Assist in Virtual Agent](https://www.servicenow.com/docs/access?context=hcls-agentic-ai-use-cases&version=australia&pubname=australia-healthcare-life-sciences&ft:locale=en-US)**

Create support requests for healthcare IT, biomed, facilities, or environmental services departments through Now Assist in Virtual Agent conversationally. This workflow resolves missing or unclear details through clarifying questions and validates the request using the Care team operations case Intake and Care team operations case Creation AI agents and is available in Care Team Portal and Care Team Mobile.

-   **[Care Team Operations Case Creation Voice AI agent](https://www.servicenow.com/docs/access?context=hco-now-assist-voice-agent&version=australia&pubname=australia-healthcare-life-sciences&ft:locale=en-US)**

The Care Team Operations Case Creation Voice AI Agent enables care team members to create cases conversationally over the phone.

**Note:** For the Care Team Operations Case Creation Voice AI Agent to create cases, the Care Team Operations plugin for cases of that request type must be installed.


-   **[ServiceNow product tiers](https://www.servicenow.com/docs/access?context=ai-native-sku-overview&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)**

The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets, and create your own
Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.


</td></tr><tr><td>

Care Team Operations for Facilities

</td><td>

-   **[Create support requests using Now Assist in Virtual Agent](https://www.servicenow.com/docs/access?context=hcls-agentic-ai-use-cases&version=australia&pubname=australia-healthcare-life-sciences&ft:locale=en-US)**

Create support requests for healthcare IT, biomed, facilities, or environmental services departments through Now Assist in Virtual Agent conversationally. This workflow resolves missing or unclear details through clarifying questions and validates the request using the Care team operations case Intake and Care team operations case Creation AI agents and is available in Care Team Portal and Care Team Mobile.

-   **[Care Team Operations Case Creation Voice AI agent](https://www.servicenow.com/docs/access?context=hco-now-assist-voice-agent&version=australia&pubname=australia-healthcare-life-sciences&ft:locale=en-US)**

The Care Team Operations Case Creation Voice AI Agent enables care team members to create cases conversationally over the phone.

**Note:** For the Care Team Operations Case Creation Voice AI Agent to create cases, the Care Team Operations plugin for cases of that request type must be installed.


-   **[ServiceNow product tiers](https://www.servicenow.com/docs/access?context=ai-native-sku-overview&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)**

The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets, and create your own
Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.


</td></tr><tr><td>

Care Team Operations for Healthcare IT

</td><td>

-   **[Create support requests using Now Assist in Virtual Agent](https://www.servicenow.com/docs/access?context=hcls-agentic-ai-use-cases&version=australia&pubname=australia-healthcare-life-sciences&ft:locale=en-US)**

Create support requests for healthcare IT, biomed, facilities, or environmental services departments through Now Assist in Virtual Agent conversationally. This workflow resolves missing or unclear details through clarifying questions and validates the request using the Care team operations case Intake and Care team operations case Creation AI agents and is available in Care Team Portal and Care Team Mobile.

-   **[Care Team Operations Case Creation Voice AI agent](https://www.servicenow.com/docs/access?context=hco-now-assist-voice-agent&version=australia&pubname=australia-healthcare-life-sciences&ft:locale=en-US)**

The Care Team Operations Case Creation Voice AI Agent enables care team members to create cases conversationally over the phone.

**Note:** For the Care Team Operations Case Creation Voice AI Agent to create cases, the Care Team Operations plugin for cases of that request type must be installed.


-   **[ServiceNow product tiers](https://www.servicenow.com/docs/access?context=ai-native-sku-overview&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)**

The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets, and create your own
Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.


</td></tr><tr><td>

Care Team Work Management

</td><td>

-   **[Create a care team task plan](https://www.servicenow.com/docs/access?context=ctwm-create-care-team-work-plan&version=australia&pubname=australia-healthcare-life-sciences&ft:locale=en-US)**

Create single or multi‑unit task plans for care teams to support ad hoc or recurring tasks. Multi‑unit work plans can include orchestration cases and tasks, while single‑unit work plans use care team cases and tasks. This feature helps teams coordinate work more efficiently across units and within their own teams.

-   ****

Use the unified Care Team Work Management landing page to view and manage care team cases and care team tasks all in one place. This provides a streamlined and consistent experience across work activities for care team agents.

-   **Operational Rounding playbook**

Use rounding templates with required fields and clinical checklists to standardize operations activities. The playbook generates one‑time and recurring rounding tasks across units using built‑in scheduling within the Healthcare Workspace. It supports completing task, capturing evidence, and tracking progress.


</td></tr><tr><td>

Case and Knowledge Management

</td><td>

-   **[Granular roles](https://www.servicenow.com/docs/access?context=components-installed-with-case-and-knowledge-management&version=australia&pubname=australia-employee-service-management&ft:locale=en-US)**

Provide tighter security to HR data using the granular admin roles in Case and Knowledge Management.

-   **[Use COE Security Diagnostics](https://www.servicenow.com/docs/access?context=coe-diagnostics-tool&version=australia&pubname=australia-employee-service-management&ft:locale=en-US)**

Enable HR administrators to determine which users have access to HR cases within an instance based on COE security policies. HR administrators can also review the specific COE security policies that restrict user access.

-   **[ER Consolidated List in HR Agent Workspace](https://www.servicenow.com/docs/access?context=hr-er-dashboards&version=australia&pubname=australia-employee-service-management&ft:locale=en-US)**

Get a holistic view of all related tables for all the ER cases using the ER cases consolidated view in the Employee relations dashboard.


</td></tr><tr><td>

Case management for CSM

</td><td>

-   **[Task Dependencies for Task Plan Templates](https://www.servicenow.com/docs/access?context=task-dependencies-for-task-plan-templates&version=australia&pubname=australia-customer-service-management&ft:locale=en-US)**

Define dependency relationships between template items in the \[sn\_task\_plan\_template\_dependency\] table, and upon applying the template, create and store the resulting task dependencies in the \[sn\_task\_dependency\_m2m\] table to ensure controlled task sequencing through predecessor–successor relationships.

-   **[Document References in Task Plan Templates](https://www.servicenow.com/docs/access?context=adding-and-managing-document-references-in-task-plan-templates&version=australia&pubname=australia-customer-service-management&ft:locale=en-US)**

Add documents to Task Plan Template items, storing document references in the \[sn\_task\_plan\_template\_document\] table and making them accessible through form views and related lists based on template state and user permissions, ensuring secure and controlled document access aligned with template‑level permissions


</td></tr><tr><td>

Change Management

</td><td>

-   **[Granular admin role](https://www.servicenow.com/docs/access?context=installed-with-cm-itsm-roles&version=australia&pubname=australia-it-service-management&ft:locale=en-US)**

Assign the single feature-specific granular sn\_change\_admin role to users to grant permission to configure Change Management features and system properties. This role replaces the previous general admin and ITIL roles. The sn\_change\_admin role includes the sn\_change\_writer, change\_manager, and sn\_change\_cab.cab\_manager roles.

-   **[Exclude change request records from conflict check](https://www.servicenow.com/docs/access?context=configure-conflict-properties&version=australia&pubname=australia-it-service-management&ft:locale=en-US)**

Exclude change requests from the conflict check process by setting the **Exclude from conflict detection** field to true. This setting also means that the change record is not displayed as a conflicting change when conflict checker is run on other change records.

-   **[Create change templates](https://www.servicenow.com/docs/access?context=create-change-template&version=australia&pubname=australia-it-service-management&ft:locale=en-US)**

Control mandatory and read-only fields for change models by configuring change templates and defining template field policies. Change templates provide baseline standardization for common changes, making changes easier to create as well as driving a higher standard of change and compliance. Similar to the concepts used for existing standard change templates, templates used for change models can be proposed, reviewed, versioned, or retired.

-   **[Enhanced data model for change templates](https://www.servicenow.com/docs/access?context=change-data-model&version=australia&pubname=australia-it-service-management&ft:locale=en-US)**

Use the enhanced data model that supports better categorization and role-based access for change templates for all change models automatically. This feature is optional for newly created standard changes.

This data model does not impact the existing standard change catalog and migration of these standard changes is not required.


</td></tr><tr><td>

Cloud Cost Management 10.0

</td><td>

-   **[Gain insights from your billing data with the FOCUS standard for Microsoft Azure billing](https://www.servicenow.com/docs/access?context=schedule-azure-billing-job&version=australia&pubname=australia-it-asset-management&ft:locale=en-US)**

Enhance your ability to manage cloud costs using the FOCUS billing standard that enables better insights. This feature helps you make more informed decisions. Additionally, you experience seamless processing of billing data across multiple Azure billing models such as:

    -   Enterprise Agreement \(EA\)
    -   Microsoft Customer Agreement \(MCA\)
    -   Microsoft Partner Agreement \(MPA\)
-   **[View cloud cost data in your preferred currency for multiple cloud service providers](https://www.servicenow.com/docs/access?context=operation-view-ccm-ws&version=australia&pubname=australia-it-asset-management&ft:locale=en-US)**

View your cloud cost data in your preferred local currency for better clarity and reporting flexibility. This capability enables you to view cost and usage details from multiple cloud service providers, including AWS, Azure, and GCP, in your selected currency.

-   **[Get support for your Azure MPA model when operating under an MSP](https://www.servicenow.com/docs/access?context=azure-pricesht-sched-dwnld-cloudin&version=australia&pubname=australia-it-asset-management&ft:locale=en-US)**

Gain full visibility into your cloud costs and actionable insights for your Azure cloud spend when operating under an MSP. Additionally, the feature provides a centralized view to monitor cloud spend and manage budgets.


</td></tr><tr><td>

Code Signing

</td><td>

-   **[Utilities Dashboard](https://www.servicenow.com/docs/access?context=code-signing-utilities&version=australia&pubname=australia-platform-security&ft:locale=en-US)**

Use the **Utilities Dashboard** tab within the Code Signing Health and Status dashboard to monitor signature status, detect configuration issues, and maintain the overall health of your Code Signing environment.

-   **[Multiple signatures for a record across certificates](https://www.servicenow.com/docs/access?context=signature-verification-in-code-signing&version=australia&pubname=australia-platform-security&ft:locale=en-US)**

Leverage support for multiple signatures for records across different certificates, thus ensuring that valid signatures from any trusted source are recognized. Allow multiple signatures to be added to a record and have the system determine validity by evaluating all existing signatures from newest to oldest.

-   **[Code Signing OOB Apps Signatures plugin](https://www.servicenow.com/docs/access?context=explore-code-signing&version=australia&pubname=australia-platform-security&ft:locale=en-US#cs-validation-jobs)**

Use this plugin \(com.glide.code\_signing.oob\_apps\_signatures\) to install build time signatures for all relevant records in trued-up ServiceNow® Store application versions.

-   **[New key pair](https://www.servicenow.com/docs/access?context=code-signing-certificates&version=australia&pubname=australia-platform-security&ft:locale=en-US)**

A new cryptographic key pair is generated to strengthen the Circle of Trust and to ensure a secure signing process. You can see this key pair within the **Key Pair and Certificates** tab of the **Code Signing Health and Status** dashboard.

-   **[Wild Card Purpose for KMF Signature Configuration](https://www.servicenow.com/docs/access?context=explore-code-signing&version=australia&pubname=australia-platform-security&ft:locale=en-US#sign-update-set)**

Use the "Wild Card Purpose" entry in the signature configurations to eliminate import warnings for script includes and business rules.

-   **[Code signing for probes](https://www.servicenow.com/docs/access?context=sign-files-nonprod&version=australia&pubname=australia-platform-security&ft:locale=en-US)**

Discovery now enforces code signing for probes, parameters, and sensors to guarantee authenticity, integrity, and secure execution on MID Servers. This update blocks unsigned or tampered payloads, provides signature validation, and strengthens compliance by helping prevent audit gaps without impacting discovery performance.


</td></tr><tr><td>

Collaborative Work Management

</td><td>

-   **[ServiceNow product tiers](https://www.servicenow.com/docs/access?context=ai-native-sku-overview&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)**

The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets, and create your own
Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.

-   **[Formula columns in CWM](https://www.servicenow.com/docs/access?context=add-formula-column-cwm-boards&version=australia&pubname=australia-it-business-management&ft:locale=en-US)**

Gain deeper insights into your work by adding formula columns to your List view in CWM Boards. Create calculations that automatically compute values across your tasks, such as summing hours, calculating date differences, or deriving metrics from existing fields.

Build formulas manually using the Formula Builder panel, which guides you through selecting functions and referencing columns with inline suggestions. As you type, the builder validates your formula in real-time and displays clear error messages if corrections are needed.

You can accelerate formula creation with AI by describing your calculation in natural language. AI generates a valid formula that you can insert directly into the editor, saving you the time to manually build a valid formula.

-   **[Kanban board filters](https://www.servicenow.com/docs/access?context=cwm-board-views&version=australia&pubname=australia-it-business-management&ft:locale=en-US)**

Save time finding the work that matters most by applying quick filters directly on your Kanban board.

As you adjust filter conditions in the header, the quick filter panel stays in sync, and vice versa. Your filter choices automatically apply to saved views and CWM Board templates, so the next time you open the board, your preferences are readily available.

-   **[Scrum tasks](https://www.servicenow.com/docs/access?context=managing-scrum-tasks-for-stories-cwm&version=australia&pubname=australia-it-business-management&ft:locale=en-US)**

Improve sprint execution by breaking user stories into scrum tasks that make estimation easier and daily progress visible. These tasks appear as nested children in the List, Kanban, and Sprint planning views, so that your team sees how individual efforts roll up into the larger story.

Using AI to generate an initial set of scrum tasks based on your story descriptions, you can reduce the overhead of task creation. Trigger the scrum task generation from the story form or inline from the Sprint planning view, and receive a relevant set of tasks as a starting point for your sprint planning. You can then review, edit, and add the generated tasks to fit your team's workflow.

-   **[Task dependencies and relationships](https://www.servicenow.com/docs/access?context=managing-task-dependencies-relationships-cwm&version=australia&pubname=australia-it-business-management&ft:locale=en-US)**

Increase visibility into how work is connected by linking related items directly in CWM and avoid switching context to track dependencies.

As these relationships surface across Kanban, List, and Gantt views with clear visual cues, you can improve planning confidence for your teams. Blocked items stand out at a glance, helping teams spot bottlenecks early, communicate delays quickly, and plan tasks in the right sequence.

-   **[Team member roles for project work](https://www.servicenow.com/docs/access?context=cwm-team-member-roles&version=australia&pubname=australia-it-business-management&ft:locale=en-US)**

View and update project and demand tasks directly in CWM using team member roles, installed alongside Collaborative Work Management.

The team member read role lets users view project and demand tasks and leave comments. The team member read-write role also lets users edit those tasks. Team members can view and manage the work assigned to them and their team through **My Work** and **Connected Work** in CWM.

-   **[Image download from docs](https://www.servicenow.com/docs/access?context=cwm-docs&version=australia&pubname=australia-it-business-management&ft:locale=en-US)**

Save images from your CWM documents directly to your device, making it easier to share or use them outside of the Docs environment.


</td></tr><tr><td>

Common Governance, Risk, and Compliance feature

</td><td>

-   **[ServiceNow product tiers](https://www.servicenow.com/docs/access?context=ai-native-sku-overview&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)**

The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets, and create your own
Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.

-   **[GRC notification redirection](https://www.servicenow.com/docs/access?context=email-notification-redirection&version=australia&pubname=australia-governance-risk-compliance&ft:locale=en-US)**

After upgrading GRC to version 22.0.x, notification links in GRC applications automatically route you to the appropriate workspace view based on your persona and access permissions. If you don't have workspace access, links default to the classic view.

-   **[Monitor my tasks in the Tasks page in the workspace](https://www.servicenow.com/docs/access?context=configure-my-tasks-in-ws&version=australia&pubname=australia-governance-risk-compliance&ft:locale=en-US)**

After upgrading GRC to version 22.0.1, the Tasks page loads faster with performance improvements. Task counts display first as an at-a-glance summary, followed by detailed task lists that load progressively. Task data refreshes at regular intervals to keep information current. These improvements provide better scalability for users with high task volumes across multiple task sources.


</td></tr><tr><td>

Compliance Case Management

</td><td>

-   **[Report a compliance case anonymously](https://www.servicenow.com/docs/access?context=report-compliance-case-anonymously&version=australia&pubname=australia-governance-risk-compliance&ft:locale=en-US)Report compliance cases anonymously**

Employees can now use the Anonymous Reporting Center to report compliance violations such as fraud and embezzlement, workplace misconduct \(harassment, discrimination\), bribery and corruption, and other concerns without revealing their identity or location.

Accessed through the Employee Center, the Anonymous Reporting Center portal automatically logs users out to enforce anonymity, creates case records without mapping to employee identity, and provides a unique report key and report number for secure follow-up communication.

CAPTCHA‑based verification is used to authenticate submissions, and the system generates a report statement summarizing the case after submission. Employees can save a copy of their report for future reference. For security and confidentiality, the submitted information is not displayed again. Reports are routed to the appropriate compliance team based on the nature of the concern.

Throughout the investigation process:

    -   Investigators can request additional information through a comments system visible to the reporter
    -   Reporters can follow up on their case using their report key to check progress and respond to questions
    -   All interactions maintain reporter anonymity at every step; no identity or location data is ever captured or linked
This enhancement enables organizations to build trust, mitigate risks before escalation, and ensures regulatory compliance with whistleblower protection requirements.

-   **[GRC case summarization skill for compliance cases](https://www.servicenow.com/docs/access?context=compliance-case-summarization-skill&version=australia&pubname=australia-governance-risk-compliance&ft:locale=en-US)AI-driven compliance case summarization**

After upgrading Now Assist for Integrated Risk Management \(IRM\) application to version 22.x, Compliance analysts can use the Case summarization feature to quickly understand a compliance case without manually reviewing every field, attachment, or related list. Now Assist analyzes key case attributes—such as timelines, impacted areas, evidence, and actions—and generates a structured summary directly inside the compliance case.

This solves a common problem: case data is often lengthy, scattered across multiple related lists, and difficult for analysts to digest efficiently. Analysts can also save and edit summaries as case data evolves, ensuring the record stays current.

By consolidating all relevant information into a single, coherent narrative, Now Assist reduces investigation time, improves consistency across reviewers, and supports faster decision-making.


</td></tr><tr><td>

Configurable Workspace

</td><td>

-   **[UI interactions for declarative actions](https://www.servicenow.com/docs/access?context=configure-da-ui-interactions&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US)**

Combine logic, script, and configurable UI with a UI interaction, and apply it from any page event or declarative action. When you use a declarative action to apply a UI interaction, you can extend a page without taking ownership.


</td></tr><tr><td>

Configuration Compliance

</td><td>

-   **[Qualys parameter to ignore passed test results](https://www.servicenow.com/docs/access?context=Qualys-cc-Integration&version=australia&pubname=australia-security-management&ft:locale=en-US)**

Starting with v15.2.5 of Configuration Compliance, the ignore\_passed\_result integration instance parameter for the Qualys Integration for Security Operations has been added.

This parameter is set to `false` by default so that passed test results imported by Qualys are not ignored.

Set the parameter to **true** to ignore passed test results on import.

**Note:** If activated, this parameter does not impact closure of the test results. For example, if you activate the parameter, and a failed test result from a previous import has since passed, it will be closed correctly.

-   **[AWS Integration for Security Exposure Management](https://www.servicenow.com/docs/access?context=aws-integration-for-security-exposure-management-overview&version=australia&pubname=australia-security-management&ft:locale=en-US)**

The AWS Integration for Security Exposure Management supports integrations with the following AWS services:

    -   AWS Inspector is an automated vulnerability management service that continuously scans EC2 instances, ECR container images, and Lambda functions for software vulnerabilities \(CVEs\) and unintended network exposure. The Vulnerability Response integration with AWS Inspector imports host and container vulnerability findings from AWS Inspector.
    -   AWS Security Hub is a security service that is used to centralize and update security checks across AWS accounts. It provides a unified view of security alerts and compliance status by integrating with various AWS services. The Vulnerability Response integration with AWS Security Hub imports host, container vulnerabilities, and misconfigurations from AWS Security Hub.
-   **[Optimized Tenable.io Compliance Results ingestion](https://www.servicenow.com/docs/access?context=tenableIntegration&version=australia&pubname=australia-security-management&ft:locale=en-US)**

Starting with v 6.1.3, the Tenable.io Compliance Results Integration is replaced by the Tenable.io Fixed Compliance Results Integration and Tenable.io Open Compliance Results Integration. Compliance results are now imported based on their status, optimizing ingestion performance and scalability for environments with large volumes of compliance data while keeping remediation and compliance tracking aligned with the current state of findings.

-   **[Qualys Integration – API enhancements](https://www.servicenow.com/docs/access?context=c_QualysVulnIntegration&version=australia&pubname=australia-security-management&ft:locale=en-US)**

The Qualys Vulnerability Integration has been upgraded to support newer Qualys API versions across Host Detection, Host List, Knowledgebase, PC Controls, PC Policies, and PCRS integrations. The integrations now ingest additional data fields, including vulnerability detection source, authentication privilege status, active status for controls and policies, and cloud metadata, giving you better visibility into your vulnerability and compliance data. Use the new `posture_api_version` integration instance parameter to choose between the default v2.0 APIs or the newer v5.0 streaming APIs for the PCRS Policy Host and PCRS Test Results integrations.

-   **[Unified Microsoft Defender Integration for Security Exposure Management](https://www.servicenow.com/docs/access?context=ms-defender-sem&version=australia&pubname=australia-security-management&ft:locale=en-US)**

The Microsoft Defender for Cloud and Microsoft Defender Threat and Vulnerability Management \(MS TVM\) plugins are now consolidated into a single plugin: Microsoft Defender Integration for Security Exposure Management. This consolidation deprecates the standalone Microsoft Defender for Cloud plugin. The unified plugin also introduces container image vulnerability ingestion from Microsoft Defender for Cloud, creating Container Vulnerable Items on your instance. A guided migration path is available to transfer existing data from the deprecated applications to the unified plugin.

-   **[Remediation task rule execution mode](https://www.servicenow.com/docs/access?context=sem-grouping-multiple-findings-remediation-tasks-processing&version=australia&pubname=australia-security-management&ft:locale=en-US)**

You can now choose how remediation task rules are evaluated during ingestion. The new Match First execution mode evaluates rules sequentially and applies only the first matching rule, assigning each finding to exactly one remediation task. The default Match All mode continues to evaluate all applicable rules.


</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

-   **[CMDB Workspace v8.0](https://www.servicenow.com/docs/access?context=cmdb-workspace&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US):**

Create a CI with a lookup identifier entry that contains mandatory attributes in the CMDB Workspace. When you select a lookup identifier entry on the Required attributes page, you can set those mandatory attribute values for proper IRE processing. For more information, see [Create a CI manually in CMDB Workspace](https://www.servicenow.com/docs/access?context=create-ci-manual-cmdb-workspace&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

-   **[CMDB Workspace v9.0](https://www.servicenow.com/docs/access?context=cmdb-workspace&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US):**
    -   Use the Service Graph Workspace to view data, such as company, location, user, and CMDB data, using panels and dashboards. The Service Graph Workspace is specifically organized to help CMDB administrators, data owners, and analysts work with the CMDB. You can search the CMDB in Service Graph Workspace without having detailed knowledge of the CMDB data model by using contexts that are mapped to CI classes as navigation.
    -   Configure de-duplication remediation processes for related tables to turn off automated workflows, such as ignoring errors and skipping business rules, that might block referenced duplicate CIs from updating to the main CI. Skipping automated workflows for related tables enables de-duplication tasks, which would otherwise fail, to complete successfully. For more information, see [Effects on related tables \(such as Change\)](https://www.servicenow.com/docs/access?context=de-duplication-tasks&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US) and [Turn off workflows of related tables during remediation](https://www.servicenow.com/docs/access?context=dedup-ci-disable-workflow&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).
-   **[Dynamic IRE](https://www.servicenow.com/docs/access?context=dynamic-ire&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US)**

Use Dynamic IRE to accurately identify CIs across multiple data sources, and by so, minimize duplicate CIs. Dynamic IRE is applicable only to the Hardware \[cmdb\_ci\_hardware\] class and its descending class, using a dynamic identification process which eliminates the need to manually create and maintain identification rules.

-   **[Simplify resolving de-duplication tasks by using a Now Assist for CMDB skill](https://www.servicenow.com/docs/access?context=reconcile-dup-task&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US)**

Use the De-duplication task resolution assistant skill in the Duplicate CI Remediator to use preselected remediation options instead of manually making selections. An AI agent preselects the options to resolve the task, such as the choice of the main CI. Then, before initiating the remediation, you can review all suggested options with supported reasoning.

To use the De-duplication task resolution assistant skill, you must install the Now Assist for CMDB version v3.0.

-   **[Quick start tests for CMDB](https://www.servicenow.com/docs/access?context=quick-start-tests-cmdb&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US)**

Run quick start tests after upgrades and deployments of new applications or integrations to verify that CMDB works as expected. If you customized CMDB, copy the quick start tests and configure them for your customizations.


</td></tr><tr><td>

Container Vulnerability Response

</td><td>

-   **[Enhancements to Container Vulnerability Response](https://www.servicenow.com/docs/access?context=exploring-cvr&version=australia&pubname=australia-security-management&ft:locale=en-US)**

The image repository name format for new and existing discovered container images in the Container Vulnerability Response application has been updated to align with the discovery format. Perform a complete import to view the registry/repository enhancements on existing and new records.

    -   The registry/repository format is supported for all third-party integrations including the [Vulnerability Response integration with Palo Alto Networks Prisma Cloud Compute](https://www.servicenow.com/docs/access?context=pcc-integration&version=australia&pubname=australia-security-management&ft:locale=en-US) and [Vulnerability Response Integration with Wiz](https://www.servicenow.com/docs/access?context=vr-wiz-exploring-host-cf&version=australia&pubname=australia-security-management&ft:locale=en-US) third-party integrations.
    -   Appended all repositories that are associated with an image to the Repository field on records on the Discovered Container Image \[sn\_vul\_container\_image\] table, which can help you see images from specific repositories.
    -   The default integration instance parameter for configuring finding keys for the Container Vulnerability Integration includes src\_ci, vulnerability, package, image\_layer, and image\_repository.
Added the source\_id column to the Container Image Finding \[sn\_vul\_container\_image\_findings\] table. Mapped the id attribute from imports to the Source id field on findings records for all third-party integrations including the Vulnerability Response Integration with Palo Alto Networks Prisma Cloud Compute and [Vulnerability Response Integration with Wiz](https://www.servicenow.com/docs/access?context=vr-wiz-exploring-host-cf&version=australia&pubname=australia-security-management&ft:locale=en-US) third-party integrations.

-   **[AWS Integration for Security Exposure Management](https://www.servicenow.com/docs/access?context=aws-integration-for-security-exposure-management-overview&version=australia&pubname=australia-security-management&ft:locale=en-US)**

The AWS Integration for Security Exposure Management supports integrations with the following AWS services:

    -   AWS Inspector is an automated vulnerability management service that continuously scans EC2 instances, ECR container images, and Lambda functions for software vulnerabilities \(CVEs\) and unintended network exposure. The Vulnerability Response integration with AWS Inspector imports host and container vulnerability findings from AWS Inspector.
    -   AWS Security Hub is a security service that is used to centralize and update security checks across AWS accounts. It provides a unified view of security alerts and compliance status by integrating with various AWS services. The Vulnerability Response integration with AWS Security Hub imports host, container vulnerabilities, and misconfigurations from AWS Security Hub.
-   **[Unified Microsoft Defender Integration for Security Exposure Management](https://www.servicenow.com/docs/access?context=ms-defender-sem&version=australia&pubname=australia-security-management&ft:locale=en-US)**

The Microsoft Defender for Cloud and Microsoft Defender Threat and Vulnerability Management \(MS TVM\) plugins are now consolidated into a single plugin: Microsoft Defender Integration for Security Exposure Management. This consolidation deprecates the standalone Microsoft Defender for Cloud plugin. The unified plugin also introduces container image vulnerability ingestion from Microsoft Defender for Cloud, creating Container Vulnerable Items on your instance. A guided migration path is available to transfer existing data from the deprecated applications to the unified plugin.

-   **[Configure Image Vulnerability keys for Container Vulnerability Response CVIT creation](https://www.servicenow.com/docs/access?context=cvr-configuring-findings-key-granularity&version=australia&pubname=australia-security-management&ft:locale=en-US)**

Configure records on the Configure Image Vulnerability Keys \[sn\_vul\_container\_image\_vulnerability\_keys\] table in your ServiceNow AI Platform® instance for the Image Vulnerability Keys that create container vulnerable items \(CVIT\)s.

    -   The Universally Unique Identifier \(UUID\) provided by Wiz is now mapped as the detection key for the Wiz Host Vulnerability integration.
    -   AWS ECS \(Elastic Container Service\) and AWS EKS \(Elastic Kubernetes Service\) environments are supported.
    -   Cluster and Service are supported for AWS ECS environments.
    -   Namespace, Registry, and Service are supported for AWS EKS environments.
    -   Choose either Scanner \(third-party scanners\) or Discovery \(Configuration Management Database \(CMDB\)\) as sources for data import for AWS ECS and AWS EKS.

**Note:**

If you choose **Discovery** as the data source, the Populate image relationships scheduled job runs daily to pre-import cluster and service details, and you should schedule your third-party integration runs at least 4 hours after this scheduled job is completed to verify that the pre-import data is available. This job is activated by default, but you must set the schedule so it runs before your scheduled third-party integration runs.

For new customers only: The system property, sn\_vul\_container.image\_relationship\_mapping\_months sets the number of previous months \(1-12\) that you want your third-party integration to look for container image updates when processing relationship mappings. This data is used to filter images by the sys\_updated\_on field. The default setting is three months. After you configure the integration run, relationship mapping is created for images which have been scanned in the last 90 days and present in discovered container images.

    -   Column labels on the Container Vulnerable item \[sn\_vul\_container\_image\_vulnerable\_item\] table are updated to support the scanner and discovery options, depending on your choice on the Configure Image Vulnerability Keys configuration page:
        -   Cluster \(Scanner\) Namespace \(scanner\), and Service \(scanner\) for scanner data
        -   Cluster \(Discovery\), Namespace \(Discovery\) and Service \(Discovery\) for Discovery

</td></tr><tr><td>

Continuous Authorization and Monitoring

</td><td>

-   **[OSCAL Assessment Plan export and import](https://www.servicenow.com/docs/access?context=oscal-assessment-plan-import-export&version=australia&pubname=australia-governance-risk-compliance&ft:locale=en-US)**

After upgrading to version 22.0.2, Continuous Authorization and Monitoring supports import and export of OSCAL Assessment Plan \(AP\) files.

Import OSCAL AP files from external tools to automatically generate engagements, control tests, test plans, user assignments, and test scope. Multiple AP files can be imported together for packages with multiple engagements.

Export generates OSCAL AP files for auditors and authorizers, enabling other systems to understand what testing is planned or was performed.

-   **[Request control tailoring](https://www.servicenow.com/docs/access?context=request-control-tailoring&version=australia&pubname=australia-governance-risk-compliance&ft:locale=en-US)**

After upgrading to version 22.0.2, make incremental changes to control sets while preserving the state of unchanged controls without having to reset the entire package life cycle. Supported modifications include adding new controls, marking controls as not applicable, changing control allocation \(baseline to inherited or hybrid\), and modifying inheritance configurations.

-   **[Inherit from multiple providers](https://www.servicenow.com/docs/access?context=inherit-from-multiple-providers&version=australia&pubname=australia-governance-risk-compliance&ft:locale=en-US)**

After upgrading to version 22.0.2, Controls can inherit individual control requirements from multiple Common Control Providers \(CCPs\) across different authorization packages. Previously, inheritance was limited to a single provider per control, which required creating multiple duplicate inherited controls when requirements came from different sources.

-   **[Control grid view](https://www.servicenow.com/docs/access?context=view-controls-in-grid-view&version=australia&pubname=australia-governance-risk-compliance&ft:locale=en-US)**

After upgrading to version 22.0.2, edit implementation statements and attestation respondents directly in a hierarchical data grid through the Controls tab in an authorization package.

-   **[Control tests grid view in Engagements](https://www.servicenow.com/docs/access?context=view-control-tests-in-grid-view&version=australia&pubname=australia-governance-risk-compliance&ft:locale=en-US)**

After upgrading to version 22.0.2, toggle between traditional related list and hierarchical data grid on the Control tests tab. Changes to assessment procedure effectiveness automatically cascade to parent control test effectiveness.

-   **[CAM workflow configuration enhancements](https://www.servicenow.com/docs/access?context=cam-workflow-configurator&version=australia&pubname=australia-governance-risk-compliance&ft:locale=en-US)**

After upgrading to version 22.0.2, control button visibility, UI page access, and related list actions across different workflow steps. Previously, related list actions \(such as add or remove buttons for information types or baseline control actions\) required manual scripting to support custom workflows.

The following new state model attributes have been introduced:

    -   Required Authorization Documents Page
    -   Required Overlay Page
    -   Required Information Type Actions
    -   Required Baseline Actions
    -   Required Overlay Actions
    -   Request Control Tailoring
    -   Generate OSCAL AP
    -   Generate OSCAL AR

</td></tr><tr><td>

Contract Management Pro

</td><td>

-   **[Better visibility of undelivered signature requests for a contract](https://www.servicenow.com/docs/access?context=cncore-cr-state-status&version=australia&pubname=australia-employee-service-management&ft:locale=en-US)**

When an electronic signature request is not delivered, the contract state is updated to Signature delivery failed and the signatory status to Delivery failed, clearly indicating the state of signature request. Contract fulfillers are also notified through in‑product and email alerts. This capability is supported for both Docusign and Adobe Sign.


</td></tr><tr><td>

Core Business Suite

</td><td>

-   **[Configure Core Business Suite using Now Assist](https://www.servicenow.com/docs/access?context=configure-cbs-using-now-assist&version=australia&pubname=australia-core-business-suite&ft:locale=en-US)**

Use a guided flow to set up the Core Business Suite. Receive AI‑assisted resolutions to questions that might come up during setup for a faster installation and configuration experience.

-   **[Configure Core Business Suite using guided setup](https://www.servicenow.com/docs/access?context=config-cbs-using-guided-setup&version=australia&pubname=australia-core-business-suite&ft:locale=en-US)**

Leverage the new CBS home page to initiate installations of different applications across BUs in one place. Track setup progress and receive guided configuration support from a unified product console. You can install and configure applications according to your business requirements.

-   **[Now Assist requester experience](https://www.servicenow.com/docs/access?context=now-assist-configurations-requesters&version=australia&pubname=australia-core-business-suite&ft:locale=en-US)**

Provide your employees with the AI-native requester experience in Core Business Suite.


</td></tr><tr><td>

Customer Contracts and Entitlements

</td><td>

-   **[Derived priced products](https://www.servicenow.com/docs/access?context=using-customer-cnt-ent-wf&version=australia&pubname=australia-order-management&ft:locale=en-US)**

Reflects dynamically calculated prices, ensuring consistency with underlying pricing logic and improving accuracy across contract‑driven workflows.

-   **[Contracts consolidation](https://www.servicenow.com/docs/access?context=cce-renew-service-contract-line&version=australia&pubname=australia-customer-service-management&ft:locale=en-US)**

Enables users to merge multiple customer contract lines into a single consolidated renewed quote line. Users can also merge two renewal quotes for two different contracts into a single renewal quote. This capability will improve operational efficiency across multiple renewal by eliminating reducing duplication.

-   **[Contracts hierarchical list](https://www.servicenow.com/docs/access?context=using-post-sales-support&version=australia&pubname=australia-customer-service-management&ft:locale=en-US)**

Enable agents to view contract lines under a customer contract record as a collapsible hierarchical list, making it easier to apply workflows at the appropriate root level and navigate complex product offering hierarchies.

-   **[Contract renewal performance improvements](https://www.servicenow.com/docs/access?context=cce-renew-service-contract-line&version=australia&pubname=australia-customer-service-management&ft:locale=en-US)**

Reduce processing time for large-scale renewals by enabling asynchronous processing for contract renewal workflows across quotes, orders, and opportunities.


</td></tr><tr><td>

Customer Service Problem Management

</td><td>

-   **[Alternative dispute resolution management](https://www.servicenow.com/docs/access?context=alternative-dispute-resolution&version=australia&pubname=australia-telecom-media-technology&ft:locale=en-US)**

Use the ADR case type to capture complete case details and manage investigations and resolutions while enforcing Service Level Agreement \(SLA\) compliance. You can also maintain audit and Root Cause Analysis \(RCA\) history and generate deadlock letters for customer or partner communication.


</td></tr><tr><td>

Customer Success Management

</td><td>

-   **[Product adoption roadmap](https://www.servicenow.com/docs/access?context=account-lifecycle-par-roadmap&version=australia&pubname=australia-acct-lifecycle-events&ft:locale=en-US)**

Enable customer success managers to create structured roadmaps that can guide customers through adoption of purchased products based on business value and current adoption scores. The planner supports two planning levels—Product \(strategic\) and Capabilities \(tactical\)—with sequencing to establish clear adoption pathways.


</td></tr><tr><td>

Customer self-service for Sales and Order Management

</td><td>

[Australia Patch 1](../quality/australia-patch-1.md)

-   **[AI-powered invoice case management for customers](https://www.servicenow.com/docs/access?context=dispute-invoice-issues-now-assist&version=australia&pubname=australia-order-management&ft:locale=en-US)**

Enable customers to report invoice disputes through an AI-powered virtual assistant on the Business Portal. Customers can describe quantity-related discrepancies through natural conversation. The assistant validates details, creates cases, and autonomously resolves eligible disputes by issuing credit notes or replacement orders or connecting customers with a human agent when needed. Interaction channels include chat and voice options.

-   **[Invoice dispute intake with voice assistant](https://www.servicenow.com/docs/access?context=now-assist-invoice-mgmt-voice-aiagent&version=australia&pubname=australia-order-management&ft:locale=en-US)**

Enable customers to report quantity-related invoice disputes using voice commands through an AI-powered voice assistant on the Business Portal. Customers can describe discrepancies through natural speech and the assistant captures dispute details to create invoice cases or connects customers with a human agent.

-   **[Human agent handoff with context transfer](https://www.servicenow.com/docs/access?context=resolve-invoice-case-now-assist-agent&version=australia&pubname=australia-order-management&ft:locale=en-US)**

Help customers to escalate complex disputes seamlessly to a live agent. The full conversation context, including invoice details, dispute reason, and prior AI actions are transferred to the CSM/FSM Configurable Workspace, enabling live agents to continue without asking customers to repeat information.

-   **[Now Assist for invoice case resolution](https://www.servicenow.com/docs/access?context=resolve-invoice-case-now-assist-agent&version=australia&pubname=australia-order-management&ft:locale=en-US)**

Help accelerate invoice dispute resolution by surfacing similar cases and common resolution patterns in the Now Assist panel. Agents can request help with an invoice case to view how similar disputes were resolved, reducing research time and improving consistency.

-   **[Automated email notifications for invoice cases](https://www.servicenow.com/docs/access?context=now-assist-order-management-using&version=australia&pubname=australia-order-management&ft:locale=en-US)**

Keep customers informed with automated email notifications at key points in the invoice case life cycle, including case creation confirmation, resolution details with credit note or replacement order information, and the next steps for cases requiring human review.


Australia Early Availability

-   **[Invoice management on Business Portal](https://www.servicenow.com/docs/access?context=view-invoices-business-portal&version=australia&pubname=australia-order-management&ft:locale=en-US)**

Enable your customers to view invoices and invoice line details directly on the Business Portal, providing transparency into quantity, billing location, shipping location, and sold product information.

-   **[Invoice case creation through playbook experience](https://www.servicenow.com/docs/access?context=order-mgt-business-portal&version=australia&pubname=australia-order-management&ft:locale=en-US)**

Provide self-service capability to your customers to create invoice dispute cases directly from the Business Portal for quantity, pricing, or date discrepancies using a guided self-service experience, supporting both single invoice and multiple invoice scenarios.

-   **[Invoice case management on Business Portal](https://www.servicenow.com/docs/access?context=view-invoice-cases-business-portal&version=australia&pubname=australia-order-management&ft:locale=en-US)**

Enable your customers to view and track invoice cases on the Business Portal, reducing support inquiries and keeping them informed on dispute resolution progress.


</td></tr><tr><td>

Data Management

</td><td>

-   **[Archive data in secondary object storage](https://www.servicenow.com/docs/access?context=c_ArchiveData&version=australia&pubname=australia-platform-administration&ft:locale=en-US)**

Store archive records and attachments in columnar format in an object storage outside the primary instance, freeing up primary storage and improving query performance for active data. The secondary object storage is exclusive to RaptorDB Professional V2.

-   **[Granular admin role](https://www.servicenow.com/docs/access?context=data-management-roles&version=australia&pubname=australia-platform-administration&section=data-management-role-1&ft:locale=en-US)**

Enable administrators to perform basic Data Management tasks by granting the data\_mgmt\_tools\_admin role instead of the full admin role.


</td></tr><tr><td>

Data Management for CSM

</td><td>

-   **[Configuring a contact as a consumer](https://www.servicenow.com/docs/access?context=configuring-a-contact-as-a-unified-consumer&version=australia&pubname=australia-customer-service-management&ft:locale=en-US)**

Model a single user who functions as both a contact and a consumer within your customer data structure. This capability improves administrative efficiency by reducing the overhead of creating and maintaining multiple user records for the same individual. It also provides a unified experience, eliminating the need to switch logins across different personas.

-   **[Granular administrative roles for Customer Data Foundation](https://www.servicenow.com/docs/access?context=customer-data&version=australia&pubname=australia-customer-service-management&ft:locale=en-US)**

Implemented administrative roles that provide fine-grained access control across CDF. These roles can be assigned to administrators and other personas based on job functions and security requirements. It includes the following capabilities:

    -   Added 25 admin roles with specific read, write, create, and delete permissions.
    -   Updated Before you begin sections across all Customer Data Foundation configuration topics with role prerequisites.
    -   Improved security compliance through role-based access segregation.
-   **[New fields in the Customer Account table](https://www.servicenow.com/docs/access?context=customer-data&version=australia&pubname=australia-customer-service-management&ft:locale=en-US)**

Added the following fields to the Customer Account \(customer\_account\) table to improve business identification and record management:

    -   DUNS Number: Store the Data Universal Numbering System \(DUNS\) identifier for business accounts to support data enrichment and third-party integrations.
    -   Active: Indicates whether an account record is active for filtering and workflow purposes.
-   **[Description field added Customer Data Foundation configuration tables](https://www.servicenow.com/docs/access?context=csm-cust-access-mgmt-tables&version=australia&pubname=australia-customer-service-management&ft:locale=en-US)**

Added a Description field to the following Customer Data Foundation \(CDF\) configuration tables to capture additional details about each record:

    -   Related Party Configuration \[sn\_customerservice\_related\_party\_configuration\] table
    -   Responsibility Definition \[sn\_customerservice\_responsibility\_def\] table
    -   Responsibility Access Configuration \[sn\_customerservice\_responsibility\_access\_config\] table
-   **[Billing accounts data model enhancements](https://www.servicenow.com/docs/access?context=add-related-parties-to-a-billing-account&version=australia&pubname=australia-customer-service-management&ft:locale=en-US)**

Grant contacts and consumers access to billing accounts through the related parties data model, using out of base system responsibilities and roles.

-   **[Service Model Foundation Granular admin roles](https://www.servicenow.com/docs/access?context=granular-admin-roles&version=australia&pubname=australia-customer-service-management&ft:locale=en-US)**

Added new granular admin roles to enable targeted permission assignments based on functional responsibilities, replacing broad admin access.

-   **[Add related parties to an install base item](https://www.servicenow.com/docs/access?context=add-related-party-install-base&version=australia&pubname=australia-customer-service-management&ft:locale=en-US)**

The Sold product is enhanced to support Related pricing.

-   **[Adding related parties to a sold product](https://www.servicenow.com/docs/access?context=add-related-parties-to-sp&version=australia&pubname=australia-customer-service-management&ft:locale=en-US)**

Use flexible price and quantity ramps that adapt over a product’s lifecycle, enabling time-based pricing, segment modifications during post-sale workflows, and accurate calculations across multi-year contracts.

-   **[Sold product form](https://www.servicenow.com/docs/access?context=sold-product-form&version=australia&pubname=australia-customer-service-management&ft:locale=en-US)**

Use scheduled jobs to update the state of the Sold product based on start and end dates. Ensure that sold products follow clear start and end dates with automatic state updates, giving customers fair access, predictable billing, and reducing errors through accurate lifecycle management and delta pricing.

-   **[Sold product form](https://www.servicenow.com/docs/access?context=sold-product-form&version=australia&pubname=australia-customer-service-management&ft:locale=en-US)**

Billing Account support on Sold Products to give agents immediate financial context, streamline billing‑related case resolution, and improve billing accuracy and transparency for customers and enterprises.


</td></tr><tr><td>

Data Privacy

</td><td>

-   **[Real-time alerting and blocking of sensitive data](https://www.servicenow.com/docs/access?context=real-time-protection&version=australia&pubname=australia-platform-security&ft:locale=en-US)**

Analyze user input in real time at the field level to identify sensitive data and alert users about potential sensitive data entry. You can also choose to block users from saving this information.

-   **[Data logs for real-time sensitive data](https://www.servicenow.com/docs/access?context=dps-data-privacy-overview&version=australia&pubname=australia-platform-security&ft:locale=en-US)**

Leverage real-time alerting and blocking capabilities to obtain insights into where sensitive data is being entered into the instance and by which users.

-   **[Real-time sensitive data-scanning for attachments](https://www.servicenow.com/docs/access?context=attachment-quarantine-policies&version=australia&pubname=australia-platform-security&ft:locale=en-US)**

Scan attachments for sensitive data during user uploads into fields. If sensitive data is detected, the attachment is quarantined. This restricts the access and download of the file to the original document owner and authorized users until the admin reviews the files.

-   **[New Named Entity Recognition \(NER\) model data patterns](https://www.servicenow.com/docs/access?context=default-data-patterns&version=australia&pubname=australia-platform-security&ft:locale=en-US)**

Employ new AI/ML-based model data patterns \(Address, City, State, Country, Job Position, and Salary\) to detect and anonymize sensitive data.

-   **[Anonymization support for catalog variables](https://www.servicenow.com/docs/access?context=dps-create-anonymization-policies&version=australia&pubname=australia-platform-security&ft:locale=en-US)**

Anonymize sensitive data in catalog items \(including record producers\) using anonymization jobs \(in production and during cloning\).

-   **[New base system Regular Expression \(RegEx\) data patterns](https://www.servicenow.com/docs/access?context=dds-review-discovery-findings&version=australia&pubname=australia-platform-security&ft:locale=en-US)**

Employ new base system regular expression data patterns to detect and anonymize sensitive data in line with global compliance requirements.

-   **[Enhanced anonymization reporting](https://www.servicenow.com/docs/access?context=dps-create-anonymization-job&version=australia&pubname=australia-platform-security&ft:locale=en-US)**

Demonstrate defensible compliance to regulators, auditors and internal teams using the new anonymization dashboard to provide quantitative insights into anonymization and data protection operations.


</td></tr><tr><td>

Developer Sandboxes

</td><td>

-   **[New granular roles for administration](https://www.servicenow.com/docs/access?context=dsb-installed-with&version=australia&pubname=australia-application-development&ft:locale=en-US)**

Several new granular roles enable developers to complete administrative and configuration tasks without requiring the full admin role.

-   **[Support for separate indices for AI Search](https://www.servicenow.com/docs/access?context=exploring-sandboxes&version=australia&pubname=australia-application-development&ft:locale=en-US)**

AI Search \(AIS\) now maintains separate indices for each sandbox environment, ensuring development activities that rely on AIS are correctly supported.

**Note:** The AIS integration with Developer Sandboxes is supported only on non-production environments.


</td></tr><tr><td>

Digital End-User Experience

</td><td>

-   **[Reviewing top processes by resource usage in incident investigation with DEX](https://www.servicenow.com/docs/access?context=process-snapshot&version=australia&pubname=australia-it-service-management&ft:locale=en-US)**

Service desk agents can now view automated snapshots of the top 10 CPU and memory-consuming processes directly in the **Investigation** tab of incident records. The snapshots that are captured every 30 minutes are initially triggered when an incident is created and a configuration item is tagged. You can refresh and filter snapshots over different time ranges and monitor processes causing device issues.

-   **[DEX issue diagnosis and resolution agentic workflow](https://www.servicenow.com/docs/access?context=now-assist-itsm-dex-diagnosis-resolution-workflow&version=australia&pubname=australia-it-service-management&ft:locale=en-US)**

Service desk agents can diagnose and resolve Zoom call quality issues using the DEX issue diagnosis and resolution agentic workflow, which integrates Zoom-specific diagnostics that correlate device, network, and application data.

-   **[Event monitoring with DEX](https://www.servicenow.com/docs/access?context=event-monitoring-dex&version=australia&pubname=australia-it-service-management&ft:locale=en-US)**

Monitor system events on Windows and macOS devices to track critical system events available with your base system, configure additional events to monitor, and review collected event data stored in your ServiceNow instance.

Monitor system-level events, such as application crashes, unexpected shutdowns, disk space warnings, failed login attempts, and service failures. The DEX agent captures event data directly from managed endpoints. Activate or deactivate events or add custom events to extend monitoring beyond the base system catalog.

-   ****

Generate an insights report from event log data collected by the DEX agent.

Save useful queries as named reports in the Insights reporting area to preserve them for future use. After you save a report, it appears in the left navigation panel for quick access. IT operators, L2 analysts, DEX engineers, and administrators can save, name, and retrieve reports. Role-based access controls restrict save and retrieval operations to the DEX Engineer and Administrator roles.

-   **[AI-powered root cause analysis for Zoom call quality issues](https://www.servicenow.com/docs/access?context=investigate-and-resolve-zoom-call-issues&version=australia&pubname=australia-it-service-management&ft:locale=en-US)**

Use Now Assist for Zoom call issues to identify the root cause of call quality degradation and review the supporting metric evidence for deeper insight. The analysis highlights the contributing device and network factors directly in the Zoom call quality view. Get the real-time guidance, including device ready remedial actions, contextual self-help instructions, and relevant knowledge articles to help resolve the issue efficiently.

-   **[Get AI driven insights for boot time performance](https://www.servicenow.com/docs/access?context=investigate-and-resolve-boot-time-issues&version=australia&pubname=australia-it-service-management&ft:locale=en-US)**

Monitor device boot time to identify slow start-up issues and use Now Assist to investigate the root cause and get suggested resolutions, including remedial actions, self-help instructions, and knowledge articles to resolve boot performance problems quickly.

-   **[View GPU device metric details](https://www.servicenow.com/docs/access?context=user-device-metrics&version=australia&pubname=australia-it-service-management&ft:locale=en-US)**

Monitor GPU and VRAM \(Video Random Access Memory\) usage on the Device page to assess graphics performance and identify bottlenecks. GPU usage shows the percentage of graphics processing capacity in use, while VRAM usage highlights memory consumption for graphics intensive workloads. These metrics help detect rendering issues, memory intensive applications, and performance degradation enabling faster investigation and resolution of GPU related device problems.

-   **[Applications](https://www.servicenow.com/docs/access?context=dex-workspace-application-tab&version=australia&pubname=australia-it-service-management&ft:locale=en-US)**

Monitor application performance by application version to accelerate incident resolution and improve deployment quality. This enables the Service desk agent in faster root cause analysis and data-driven deployment decisions improving the overall end-user experience.

-   **[Bulk Remediation for Impacted Devices](https://www.servicenow.com/docs/access?context=dex-insights-and-lists&version=australia&pubname=australia-it-service-management&ft:locale=en-US)**

Select multiple impacted devices from the Insights page and apply remedial actions in bulk. Service desk agents can now resolve issues across multiple devices simultaneously, improving productivity and reducing manual effort.

-   **[Digital End-User Experience Remedial Actions](https://www.servicenow.com/docs/access?context=dex-diff-ra&version=australia&pubname=australia-it-service-management&ft:locale=en-US)**

The DEX base system includes the new remedial action Sync device to Intune.


-   **[ServiceNow product tiers](https://www.servicenow.com/docs/access?context=ai-native-sku-overview&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)**

The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets, and create your own
Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.


</td></tr><tr><td>

Document Services

</td><td>

-   **[Document Management components in Workspace](https://www.servicenow.com/docs/access?context=document-management-workspace&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US)**

Organize, access, and collaborate on files efficiently with unified Document Management in Workspace through intuitive folder structures, streamlined cloud integration, one-click actions, and embedded workflows.

-   **[Granular admin roles required to secure the instance](https://www.servicenow.com/docs/access?context=granular-admin-roles-dms&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US)**

Enable developers and administrators to complete administrative configuration tasks for Document Services without requiring the full admin role.


</td></tr><tr><td>

Domain Separation

</td><td>

-   **Upgraded Process Overrides Report**

System and domain administrators can now track and review process overrides that are affected by global process upgrades. A new admin dashboard provides a comprehensive list of impacted overrides with filtering and sorting by date and process type. Use the scriptable API to build custom integrations or automations on top of the override tracking data.

-   **Domain Visibility Performance Improvements for Large MSPs**

Domain visibility queries now complete in under one second on average — a 70% reduction from the previous 3.2 second average for large instances. A new query optimization replaces multiple OR conditions with a single IN clause on the domain ID for instances that exceed the configured domain collection size threshold. All 785 Domain Separation customers benefit from faster queries, with the greatest impact for the 20 customers operating 10,000 or more domains.


</td></tr><tr><td>

Employee Center

</td><td>

-   **[Simplified Navigation](https://www.servicenow.com/docs/access?context=simple-portal-navigation-ec&version=australia&pubname=australia-employee-service-management&ft:locale=en-US)**

Simplify how employees move through Employee Center by providing a modern, left‑aligned, one‑level navigation that reduces cognitive load and adapts seamlessly across desktop and mobile.

-   **[Manage approvals with Now Assist Approval Assistance AI agent](https://www.servicenow.com/docs/access?context=manage-approvals-with-approvals-agent&version=australia&pubname=australia-employee-service-management&ft:locale=en-US)**

Accelerate request approvals by automatically aggregating relevant details, validating requests against policies, and recommending approval decisions to managers.

-   **[Configure widget heading levels for accessibility](https://www.servicenow.com/docs/access?context=config-heading-widget-instance&version=australia&pubname=australia-employee-service-management&ft:locale=en-US)**

Improve accessibility by allowing admins to configure widget heading levels \(H1–H6\) to meet organizational standards and support technologies.

-   **[Enhanced Requests Experience](https://www.servicenow.com/docs/access?context=my-requests-update-intro&version=australia&pubname=australia-employee-service-management&ft:locale=en-US)**

Improve the Enhanced Requests Experience functionality by enabling specific tabs created for specific filters. Help employees find relevant requests faster while giving admins, experience owners, and service owners greater control over curating page design for specific purposes.

-   **[Moveworks for Employee Center](https://www.servicenow.com/docs/access?context=moveworks-for-employeecenter&version=australia&pubname=australia-employee-service-management&ft:locale=en-US)**

Empower employees with Moveworks for Employee Center and its AI-powered conversational support. Using the Moveworks embedded AI assistant plugin, your employees can ask questions, get instant answers, and complete tasks end-to-end from Employee Center and Employee Center Pro.

-   **[Quick start tests for Employee Center](https://www.servicenow.com/docs/access?context=quick-start-tests-employee-center&version=australia&pubname=australia-employee-service-management&ft:locale=en-US)**

After upgrades and deployments of new applications or integrations, run quick start tests to verify that Employee Center works as expected. If you customized Employee Center, copy the quick start tests and configure them for your customizations.


</td></tr><tr><td>

Employee Center Pro

</td><td>

-   **[Integrated experience and service feedback](https://www.servicenow.com/docs/access?context=ex-fdback-ovrvw&version=australia&pubname=australia-employee-service-management&ft:locale=en-US)**

Add granular admin roles to the Integrated experience and service feedback functionality to decentralize administrative task management.

-   **[Moveworks for Employee Center](https://www.servicenow.com/docs/access?context=moveworks-for-employeecenter&version=australia&pubname=australia-employee-service-management&ft:locale=en-US)**

Empower employees with Moveworks for Employee Center and its AI-powered conversational support. Using the Moveworks embedded AI assistant plugin, your employees can ask questions, get instant answers, and complete tasks end-to-end from Employee Center and Employee Center Pro.

-   **[Quick start tests for Employee Center Pro](https://www.servicenow.com/docs/access?context=quick-start-tests-employee-center-pro&version=australia&pubname=australia-employee-service-management&ft:locale=en-US)**

After upgrades and deployments of new applications or integrations, run quick start tests to verify that Employee Center Pro works as expected. If you customized Employee Center Pro, copy the quick start tests and configure them for your customizations.


</td></tr><tr><td>

Encryption

</td><td>

-   **[Manage Field Encryption Enterprise with an enhanced Administration interface](https://www.servicenow.com/docs/access?context=now-platform-encryption&version=australia&pubname=australia-platform-security&ft:locale=en-US)**

Configure encryption settings, monitor key usage, and streamline administration for Field Encryption and Field Encryption Enterprise with the following features:

    -   Simplify key rotation and policy updates.
    -   Access encryption status and audit details.
    -   Navigate improved layouts for faster configuration.
-   **[Integrate External Key Management Service \(EKMS\) with Encryption Modules](https://www.servicenow.com/docs/access?context=ekms-external-key-management&version=australia&pubname=australia-platform-security&ft:locale=en-US)**

Configure and manage encryption keys externally through EKMS integration with an enhanced encryption framework, which enables you to:

    -   Hold encryption keys outside the instance for improved security.
    -   Perform key rotation and revocation with automated security tasks.
    -   Manage EKMS configurations and enforce the immutability of critical fields after they're active.
    -   Simplify rekeying following instance clone and restore operations.
    -   Monitor key state transitions, encrypted cache, and node-to-node communication.
    -   Access UI improvements for configuration visibility and error handling.
    -   Benefit from telemetry and performance-tested operations.

</td></tr><tr><td>

Enterprise Architecture

</td><td>

-   **[Enterprise Modeling and Visualization enhancements](https://www.servicenow.com/docs/access?context=eaw-work-with-ent-model-and-visual&version=australia&pubname=australia-application-portfolio-management&ft:locale=en-US)**

Label management improvements for diagrams:

    -   Add labels: Double-click empty areas or use the adornment tool to automatically place labels in optimal positions. You can add multiple labels to relationship lines.
    -   Edit and delete labels: Change existing labels or remove them as needed.
    -   Move with shapes: Labels maintain their relative position when you move associated shapes.

**Note:** After submitting the diagram for approval, the labels can’t be edited.

Accessibility enhancements in Enterprise Modeling and Visualization:

    -   Magnify content up to 400% while maintaining full access to all information and features.
    -   Navigate the interface using the keyboard.
    -   Access the shape context menu using the keyboard.
    -   See pop-over menus when hovering over connector lines.
ArchiMate shape library enhancements:

The ArchiMate shape library has been enhanced to align with ArchiMate 3.2 standards, with new categories, elements, and updates to existing shapes.

    -   Implementation and Migration category: Added this category with the following shape elements:
        -   Implementation event
        -   Gap
        -   Work package
        -   Deliverable
        -   Plateau
        -   Location
        -   Group
    -   Relationship Type category- Added this category with the following shape elements:
        -   And junction
        -   Or junction
-   **[Exploring the publishing center in Enterprise Architecture Workspace](https://www.servicenow.com/docs/access?context=publishing-center-in-ea-workspace&version=australia&pubname=australia-application-portfolio-management&ft:locale=en-US)**

Use the Publishing Center to control publishing workflows, monitor status, and view publishing history from a single location.

-   **[Publish TRM catalog to a knowledge base](https://www.servicenow.com/docs/access?context=working-with-publishing-center&version=australia&pubname=australia-application-portfolio-management&ft:locale=en-US)**
    -   Configure TRM catalogs and apply filters for products and lifecycle phases.
    -   Manage publishing workflows with status updates from Draft to Published.
    -   View publishing job history in the Run logs tab.
    -   Access the published TRM catalog using the generated knowledge base URL.
-   **Enhancements to the [Value stream](https://www.servicenow.com/docs/access?context=eaw-manage-value-streams&version=australia&pubname=australia-application-portfolio-management&ft:locale=en-US) and [Value stream stage](https://www.servicenow.com/docs/access?context=eaw-manage-value-stream-stages&version=australia&pubname=australia-application-portfolio-management&ft:locale=en-US) related lists**
    -   Value stream: View associated value stream stages and application models as related lists. You can add, edit, or remove the associated value stream stages and application models.
    -   Value stream stage: View associated business processes and business capabilities. Add or remove business processes and business capabilities. You can also view the value stream stage as a related list in the business process and business capability records.
-   **[Enhancements to the Business Process related lists](https://www.servicenow.com/docs/access?context=eaw-manage-business-processes&version=australia&pubname=australia-application-portfolio-management&ft:locale=en-US)**

View the value stream stage as a related list of a business process.

-   **[Enhancements to the Business Capability related lists](https://www.servicenow.com/docs/access?context=eaw-manage-business-capabilities&version=australia&pubname=australia-application-portfolio-management&ft:locale=en-US)**

View the value stream stage as a related list of a business capability.

-   **[Create documents for the Enterprise Modeling and Visualization diagrams](https://www.servicenow.com/docs/access?context=create-documents-for-diagrams&version=australia&pubname=australia-application-portfolio-management&ft:locale=en-US)**
    -   Save diagram as a document using the Generate document option from the Enterprise Modeling and Visualization diagrams page.
    -   Define templates for the documents that can be created and used from the Diagrams page.
    -   Tag components that can be included in the templates to generate documents.
    -   View associated documents from the Diagrams page.
-   **[Exploring the architecture analyzer](https://www.servicenow.com/docs/access?context=eaw-explore-arch-analyzer&version=australia&pubname=australia-application-portfolio-management&ft:locale=en-US)Architecture Analyzer**
    -   The Architectural Analyzer helps you to analyze architecture data without creating or maintaining custom diagrams. You can visually explore relationships across applications, services, and infrastructure to quickly understand dependencies and collaborate on architecture decisions. You can also understand the potential impact of architectural changes across applications and services.
    -   Added support for analyzing all EA extended entities that are part of Enterprise Modeling and Visualization, such as
        -   Control
        -   Digital integration
        -   Digital interface
        -   GRC risk
        -   Product capability
        -   TRM product
    -   The **Clear** button clears all the selections made in the **Add to canvas** boxes.
-   **[Application rationalization page enhancements](https://www.servicenow.com/docs/access?context=eaw-rationalize-business-applications&version=australia&pubname=australia-application-portfolio-management&ft:locale=en-US)**

Added an Overall score indicator to show the overall average score of a business application. Use this indicator to determine the bubble size of a business application on the Bubble Chart page. You can compare the overall scores of different business applications using their individual bubble sizes.


</td></tr><tr><td>

Enterprise Asset Management

</td><td>

-   **[Automate enterprise asset sourcing by using an agentic workflow](https://www.servicenow.com/docs/access?context=now-assist-eam-help-manage-enterprise-asset-requests-workflow&version=australia&pubname=australia-it-asset-management&ft:locale=en-US)**

Use the help manage enterprise asset requests agentic workflow to automate the process of sourcing assets for your enterprise asset requests. The workflow uses AI agents to fulfill these requests by allocating assets from local stockrooms, creating transfer orders to move assets between stockrooms, or generating purchase orders for the requested assets.

-   **[Automatically generate instructions for enterprise asset repairs by using an agentic workflow](https://www.servicenow.com/docs/access?context=now-assist-eam-help-repair-enterprise-assets-workflow&version=australia&pubname=australia-it-asset-management&ft:locale=en-US)**

Use the help repair enterprise assets agentic workflow, which is driven by AI agents, to automatically generate step-by-step troubleshooting, diagnostics, and repair instructions for your enterprise asset repairs in real time.

-   **[ServiceNow product tiers](https://www.servicenow.com/docs/access?context=ai-native-sku-overview&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)**

The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets, and create your own
Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.


-   **[Define, schedule, and track complex asset-centric work tasks through work order plans](https://www.servicenow.com/docs/access?context=manage-work-order-plans&version=australia&pubname=australia-it-asset-management&ft:locale=en-US)**

Manage complex asset-centric work tasks with unified work order plans that can be applied across assets, asset groups, or locations. The work order plans offer the following benefits:

    -   Save work order plans as reusable templates for use across assets.
    -   Organize sequential operations—shutdowns, safety inspections, calibrations, asset conditions, and restarts—using the structured playbook.
    -   Assign, schedule, and track work order tasks for technicians within the playbook.
    -   Enable technicians to receive assigned work order tasks and update task status through the ServiceNow Mobile Agent application.
-   **[Manage multimedia production equipment models and assets](https://www.servicenow.com/docs/access?context=create-model-eam&version=australia&pubname=australia-it-asset-management&ft:locale=en-US)**

Create, track, and manage multimedia production equipment models and assets in the Enterprise Asset Workspace. Get a comprehensive view of these models and assets so that you can manage them effectively throughout their life cycles.

-   **[Replace broad admin checks with granular admin roles and ACL updates](https://www.servicenow.com/docs/access?context=eam-roles&version=australia&pubname=australia-it-asset-management&ft:locale=en-US)**

Manage admin access precisely with granular admin roles. Instead of giving full admin privileges to the users, you can assign specific roles based on the tasks they perform.

-   **[Enhanced and unified enterprise asset inventory auditing experience](https://www.servicenow.com/docs/access?context=audit-eam-assetinventory&version=australia&pubname=australia-it-asset-management&ft:locale=en-US)**

Streamline and improve your inventory auditing experience with the enhanced and unified enterprise asset inventory process:

    -   Initiate a single audit that covers both hardware and enterprise assets assigned to a specific location or stockroom, eliminating the need to switch between multiple workspaces.
    -   Include consumable assets in the inventory audit to avoid asset shrinkage and ensure that inventory data remains accurate.
    -   The ServiceNow Agent app features selectable audit results, enabling you to view a real-time list of all scanned assets.
    -   When new assets are identified during the single scan audit, essential information is collected in real time through the ServiceNow Agent app to initiate asset creation.
    -   Scanned asset locations are automatically updated to reflect their precise aisle, space, or sub location during the audit, supporting the accuracy and quality of inventory records.

</td></tr><tr><td>

Enterprise Service Management Foundation

</td><td>

-   **[Enterprise Service Management Foundation](https://www.servicenow.com/docs/access?context=esm-foundation&version=australia&pubname=australia-better-together&ft:locale=en-US)**

Enterprise Service Management Foundation brings together Core Business Suite and AI-native IT Service Management to create a comprehensive, AI-enabled service delivery platform.

The integration eliminates service silos and provides employees with a unified experience for all their service needs across IT, HR, finance, legal, workplace services, and procurement.


</td></tr><tr><td>

Event Management

</td><td>

-   **[Unified alert grouping across Event Management and HLA](https://www.servicenow.com/docs/access?context=group-alert-sow-itom&version=australia&pubname=australia-it-operations-management&ft:locale=en-US)**

Improve alert quality, reduce noise, and achieve higher compression to act faster on issues by grouping Health Log Analytics and Event Management alerts.

-   **[Explicit node-based control for CI binding](https://www.servicenow.com/docs/access?context=enrich-alert-sow-itom&version=australia&pubname=australia-it-operations-management&ft:locale=en-US)**

Increase binding accuracy and reliability and improve alert-to-CI binding with explicit node-based control, configurable node-field usage, enhanced mapping logic, and backward-compatible updates.


</td></tr><tr><td>

Field Service Management

</td><td>

-   **[Dispatcher Workspace](https://www.servicenow.com/docs/access?context=using-dispatcher-workspace&version=australia&pubname=australia-field-service-management&ft:locale=en-US)**

[Dispatcher Workspace](https://www.servicenow.com/docs/access?context=using-dispatcher-workspace&version=australia&pubname=australia-field-service-management&ft:locale=en-US) now enables you to perform the following tasks:

    -   Show multiple time zones on the map in Dispatcher Workspace with a segmented time indicator to see which time zone each Field Service technician is in. For more information, see [Time zones in Dispatcher Workspace](https://www.servicenow.com/docs/access?context=time-zones-dispatcher&version=australia&pubname=australia-field-service-management&ft:locale=en-US).
    -   Quickly see a work order task in the task panel and find it on the calendar rather than having to search through multiple days. For more information, see [Open tasks from the task list](https://www.servicenow.com/docs/access?context=open-task-platform-list&version=australia&pubname=australia-field-service-management&ft:locale=en-US).
    -   See live traffic on the map in Dispatcher Workspace. For more information, see [Show map overlays in Dispatcher Workspace](https://www.servicenow.com/docs/access?context=map-overlay-dispatcher&version=australia&pubname=australia-field-service-management&ft:locale=en-US).
    -   Flag multiple tasks at once. For more information, see [Flag or unflag tasks from the list](https://www.servicenow.com/docs/access?context=flag-task-list-workspace&version=australia&pubname=australia-field-service-management&ft:locale=en-US).
    -   Quickly find tasks in the calendar from the task list. For more information, see [Flag or unflag tasks from the list](https://www.servicenow.com/docs/access?context=flag-task-list-workspace&version=australia&pubname=australia-field-service-management&ft:locale=en-US).
    -   View analytics, including the number of technicians without a work schedule or valid location. For more information, see [Scheduling Health dashboard](https://www.servicenow.com/docs/access?context=scheduling-health-dashboard&version=australia&pubname=australia-field-service-management&ft:locale=en-US).
    -   Show an overtime indicator on the calendar to visually see which technicians have overtime tasks. For more information, see [Show overtime indicator](https://www.servicenow.com/docs/access?context=dispatcher-wrkspc-settings&version=australia&pubname=australia-field-service-management&ft:locale=en-US).
    -   Control the size of the cells on the calendar to see shorter tasks more easily. For more information, see [Zoom in or out on the calendar](https://www.servicenow.com/docs/access?context=calendar-zoom-dispatcher&version=australia&pubname=australia-field-service-management&ft:locale=en-US).
-   **[Field Service Manager Mobile](https://www.servicenow.com/docs/access?context=manager-mobile-app&version=australia&pubname=australia-field-service-management&ft:locale=en-US)**

Field Service Managers can do their work from anywhere on their mobile device, including the following tasks:

    -   [Manage Field Service technicians from Field Service Manager mobile](https://www.servicenow.com/docs/access?context=mange-agents-mobile&version=australia&pubname=australia-field-service-management&ft:locale=en-US)
    -   [Create a work order task](https://www.servicenow.com/docs/access?context=create-task-manager-mobile&version=australia&pubname=australia-field-service-management&ft:locale=en-US)
    -   [Create a personal event](https://www.servicenow.com/docs/access?context=event-manager-mobile&version=australia&pubname=australia-field-service-management&ft:locale=en-US)
    -   [View analytics from Field Service Manager Mobile](https://www.servicenow.com/docs/access?context=view-analytics-manager&version=australia&pubname=australia-field-service-management&ft:locale=en-US)
-   **[Locations on personal events](https://www.servicenow.com/docs/access?context=create-personal-event&version=australia&pubname=australia-field-service-management&ft:locale=en-US)**

See locations for personal events regardless of where they're created in Field Service Management applications including Dispatcher Workspace and Field Service Manager Mobile.

-   **[Completing work on the ServiceNow Agent mobile application](https://www.servicenow.com/docs/access?context=Use-mobile-app-fsm&version=australia&pubname=australia-field-service-management&ft:locale=en-US)**
    -   Generate work summary reports and capture signatures in them at the work order task level along with the existing work order level. Additionally, you can view responses and score information for the smart assessment questionnaires in the work summary report.
    -   Perform asset audits for the technician's personal stockroom to verify and reconcile assets between a physical stockroom and the data on the ServiceNow instance.
-   **[Respond to a reviewed work order task](https://www.servicenow.com/docs/access?context=close-wo-wot-mobile&version=australia&pubname=australia-field-service-management&section=respond-task-review-mobile&ft:locale=en-US)**

View and resubmit smart assessment questionnaire responses that need additional information, enabling more informed and timely corrections of responses from job sites.

-   **[Schedule Optimization](https://www.servicenow.com/docs/access?context=schedule-optimization-engine&version=australia&pubname=australia-field-service-management&ft:locale=en-US)**

Enhance scheduling accuracy and performance with [Schedule Optimization](https://www.servicenow.com/docs/access?context=schedule-optimization-engine&version=australia&pubname=australia-field-service-management&ft:locale=en-US)

    -   View comprehensive details for all optimization runs to quickly identify issues. Access standardized information about run status, included tasks and qualifiers, unassigned tasks with explanations, and the objectives and constraints applied during each optimization.
    -   Manage integrations more easily by configuring options to enable or disable third-party map providers beyond the default provider.
    -   Leverage all available trainers to reduce processing time and accelerate end-to-end scheduling for high-volume scenarios by splitting qualifiers into non-overlapping sets and running multiple optimization jobs in parallel.
    -   Improve scheduling accuracy by introducing a **Window End Buffer Duration** field on the Work Order task record that enables you to configure a buffer duration that extends optimization beyond the defined window end so tasks are retained in the schedule.
    -   Ensure that only specified technicians can be assigned to the task, overriding all other assignment preferences, by marking technicians as **Required** when creating work order tasks.
    -   Maintain consistency by removing intraday events that do not meet the defined condition for both scheduled and prioritized optimization runs. When an event is removed from prioritized optimization, it's also removed from the scheduled intraday run.
    -   Improve optimization control by applying matching rules to intraday events by accessing them in the **Table** field on Matching Rules.
    -   View how qualifiers are grouped for efficient creation of multiple ML jobs using the **Job Distribution** column in both batch and intraday runs.
    -   Control how tasks are released to technicians by configuring drip feed settings. Choose between drip mode for gradual task distribution or bulk mode for immediate assignment.
-   **[Appointment Booking](https://www.servicenow.com/docs/access?context=appointment-booking-administer&version=australia&pubname=australia-field-service-management&ft:locale=en-US)**

Use [Appointment Booking](https://www.servicenow.com/docs/access?context=appointment-booking-administer&version=australia&pubname=australia-field-service-management&ft:locale=en-US) to perform the following tasks:

    -   Ensure better alignment with your operations by defining advanced lead time and cut-off logic through APIs or extension points. You can implement a custom script through an extension point based on job type, time of day, and day of week.
    -   Accommodate emergencies or priorities even if the capacity or appointment slots are full by enabling overbooking of appointments.
    -   Configure appointment slots to consider the holiday settings for a territory and display the available slots accordingly.
    -   Ensure guaranteed appointment slots by configuring availability checks to be performed at the time of slot retrieval so that any slot displayed is assured to be bookable without needing further capacity validation during the appointment booking.
    -   Ensure an accurate calculation of the duration for a task while booking an appointment by defining work and travel duration either in the appointment schedule configuration or in the schedule override configuration.
    -   Determine appointment availability using territory and demand channel mapping when contact or location details are not provided.
    -   Consider task dependencies while booking or rescheduling appointments and display the slots for the successor tasks after the estimated completion time including the defined lag time for the predecessor task.
-   **[ServiceNow product tiers](https://www.servicenow.com/docs/access?context=ai-native-sku-overview&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)**

The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets, and create your own
Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.


</td></tr><tr><td>

Financial Services Operations Integration with Mastercard

</td><td>

-   **​ [Integration components for the Mastercard document attachment and validation enhancement](https://www.servicenow.com/docs/access?context=financial-services-operations-integration-with-mastercard-subflows&version=australia&pubname=australia-financial-services-operations&ft:locale=en-US)**

Simplify dispute document submission to Mastercard with improved document attachment and validation feature. The application compresses multiple attachments into a single zipped file, validates files for type and size, and alerts you to non-compliant files. This capability adds the following integration subflow and action:

    -   Mastercom - Validate and Process Attachments of Card Disputes Task
    -   Create a Zip Attachment from Uploaded Documents

</td></tr><tr><td>

Financial Services Operations Integration with Verifi CDRN

</td><td>

-   Avoids costly chargebacks: When a merchant accepts the dispute and offers a refund that is acceptable for the cardholder, the case is closed as resolved with no chargeback initiated.
-   Automates merchant eligibility checks: The system automatically checks merchant eligibility through the Verifi CDRN API before creating a case. Non-eligible merchants are routed to the standard dispute lifecycle without agent intervention.
-   Seamless closure of disputes: Merchants participating in CDRN can respond to dispute alerts directly through Verifi .
-   Seamless API integration: The four-subflow API sequence — eligibility check, case creation, polling, and acknowledgment handshake — is fully automated and requires no manual API interaction from agents or supervisors.

</td></tr><tr><td>

Flows, Subflows, and Actions

</td><td>

-   **[Business calendar as a scheduled trigger](https://www.servicenow.com/docs/access?context=create-trigger-business-calendar&version=australia&pubname=australia-build-workflows&ft:locale=en-US)**

Use the business calendar to trigger flows on existing business schedules. The business calendar trigger helps align automation with shifts, holidays, and operating hours.

-   **[Flow history compare view](https://www.servicenow.com/docs/access?context=flow-history-compare-view&version=australia&pubname=australia-build-workflows&ft:locale=en-US)**

Compare two flow history entries in a side-by-side view. Use the step highlighting and change type icons to determine what flow components have been added, removed, and changed.

-   **[Flow execution analysis](https://www.servicenow.com/docs/access?context=flow-execution-analysis-landing&version=australia&pubname=australia-application-development&ft:locale=en-US)**

Analyze flow execution details to identify errors and suggest potential fixes.

-   **[Use an AI agent action](https://www.servicenow.com/docs/access?context=use-an-ai-agent-action&version=australia&pubname=australia-build-workflows&ft:locale=en-US)**

Use flow data to run an AI agent and configure the expected agent output for use later in the flow.


</td></tr><tr><td>

Generative AI Controller

</td><td>

-   **[Configure a custom resource path for BYOK models](https://www.servicenow.com/docs/access?context=configure-custom-resource-path-byok&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)**

Connect Generative AI Controller to your Azure OpenAI deployment by configuring a custom resource path in your bring your own key \(BYOK\) model configuration. Use this when your Azure OpenAI endpoint includes a path segment that Generative AI Controller does not add by default.


</td></tr><tr><td>

Goal Framework for SPM

</td><td>

-   **[Define targets at multiple organizational levels](https://www.servicenow.com/docs/access?context=goal-framework&version=australia&pubname=australia-it-business-management&ft:locale=en-US)**

Define targets across multiple organizational levels with the **Assigned entity type** and **Assigned entity** fields in the target form. This enables targets created at higher levels \(for example, Company\) to be directly assigned to lower levels \(for example, Business Unit, Department\), eliminating redundant subgoal creation, and streamlining overall goal management.


</td></tr><tr><td>

Hardware Asset Management

</td><td>

-   **[ServiceNow product tiers](https://www.servicenow.com/docs/access?context=ai-native-sku-overview&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)**

The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets, and create your own
Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.

-   **[Manage your assets with comprehensive and real-time data](https://www.servicenow.com/docs/access?context=generate-asset-analysis-now-assist-ham&version=australia&pubname=australia-it-asset-management&ft:locale=en-US)**

View consolidated asset information through AI-generated analysis summary on the asset record. The AI-generated summary dynamically updates based on the asset state and includes context from any active incidents or tasks. The summary displays the asset life cycle, current assignment and location, audit status, financial metrics, and identifies missing data to support asset management activities.


-   **[Gain visibility into approximated life cycle dates for hardware and consumable model](https://www.servicenow.com/docs/access?context=approximated-lifecycles-hardware-products&version=australia&pubname=australia-it-asset-management&ft:locale=en-US)**

Enhance the operational efficiency by gaining visibility into the estimated and approximate life- cycle dates for models when manufacturers haven’t explicitly published key dates, such as End of Life \(EoL\) and End of Service \(EoS\). This insight enables you to manage your asset portfolio strategically, reducing unexpected downtime and improve budgeting.

-   **[Enhanced and unified hardware asset inventory auditing experience](https://www.servicenow.com/docs/access?context=ham-inventory-audit&version=australia&pubname=australia-it-asset-management&ft:locale=en-US)**

Streamline and improve your inventory auditing experience with the enhanced and unified hardware asset inventory process:

    -   Initiate a single audit that covers both hardware and enterprise assets assigned to a specific location or stockroom, eliminating the need to switch between multiple workspaces.
    -   Include consumable assets in the inventory audit to avoid asset shrinkage and verify that inventory data remains accurate.
    -   The ServiceNow Agent app features selectable audit results, enabling you to view a real-time list of all scanned assets.
    -   When new assets are identified during the single scan audit, essential information is collected in real time through the ServiceNow Agent app to initiate asset creation.
    -   Scanned asset locations are automatically updated to reflect their precise aisle, space, or sub location during the audit, supporting the accuracy and quality of inventory records.
-   **[Enhanced asset disposal workflow to streamline the management of retired assets](https://www.servicenow.com/docs/access?context=create-resale-order&version=australia&pubname=australia-it-asset-management&ft:locale=en-US)**

Resell the retired assets that are no longer in use to reduce waste and receive credit. The extended asset disposal flow in the Documentation stage enables you to resell planned assets instead of disposing of them, enabling you to receive credit.

-   **[Enable your key functional roles or personas to directly manage Advanced Shipment Notification \(ASN\) imports](https://www.servicenow.com/docs/access?context=advanced-shipment-notification&version=australia&pubname=australia-it-asset-management&ft:locale=en-US)**

Upload ASN files and trigger the import process from the Procurement view within the Hardware Asset Workspace without requiring admin privileges. Users with the ham\_admin, ham\_user, procurement\_admin, or asset role can now initiate the ASN workflow themselves, creating asset records seamlessly.

-   **[Streamline model creation by copying a model directly from the Content lookup portal](https://www.servicenow.com/docs/access?context=copy-hardware-model&version=australia&pubname=australia-it-asset-management&ft:locale=en-US)**

Reduce manual effort by copying a model from the Content lookup portal to create a record in the Product Model \[cmdb\_model\] table. The copied model is automatically normalized, where applicable, and relevant fields are pre-populated with information from the content record.


</td></tr><tr><td>

Healthcare Operations Core

</td><td>

-   **[Create support requests using Now Assist in Virtual Agent](https://www.servicenow.com/docs/access?context=hcls-agentic-ai-use-cases&version=australia&pubname=australia-healthcare-life-sciences&ft:locale=en-US)**

Create support requests for healthcare IT, biomed, facilities, or environmental services departments through Now Assist in Virtual Agent conversationally. This workflow resolves missing or unclear details through clarifying questions and validates the request using the Care team operations case Intake and Care team operations case Creation AI agents and is available in Care Team Portal and Care Team Mobile.

-   **[Care Team Operations Case Creation Voice AI agent](https://www.servicenow.com/docs/access?context=hco-now-assist-voice-agent&version=australia&pubname=australia-healthcare-life-sciences&ft:locale=en-US)**

The Care Team Operations Case Creation Voice AI Agent enables care team members to create cases conversationally over the phone.

**Note:** For the Care Team Operations Case Creation Voice AI Agent to create cases, the Care Team Operations plugin for cases of that request type must be installed.


-   **[ServiceNow product tiers](https://www.servicenow.com/docs/access?context=ai-native-sku-overview&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)**

The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets, and create your own
Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.


</td></tr><tr><td>

Hermes Messaging Service

</td><td>

-   **[Expanded topic limits in Hermes](https://www.servicenow.com/docs/access?context=exploring-hermes-messaging-service&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US)**

Create more topics in Hermes with an increased topic limit. The total number of partitions across all topics can't exceed 960.

-   **[Hermes Usage Dashboard improvements](https://www.servicenow.com/docs/access?context=monitoring-data-usage-hermes&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US)**

View Hermes data usage by source, including the total number of bytes received and bytes sent over time, in the Hermes Usage Dashboard.

-   **[Access restrictions by IP address](https://www.servicenow.com/docs/access?context=restricting-access-hermes-topics&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US)**

Restrict access to Hermes by enabling IP address access control rules.

-   **[View-only role](https://www.servicenow.com/docs/access?context=hermes-messaging-service-roles&version=australia&pubname=australia-servicenow-platform&section=hermes-messaging-service-roles-4&ft:locale=en-US)**

Enable administrators to view topics and namespaces in Hermes by granting the hermes\_viewer role instead of the full admin role.


</td></tr><tr><td>

ITOM Visibility

</td><td>

-   **[Install ITOM Visibility apps using Now Assist for Setup](https://www.servicenow.com/docs/access?context=nowassist-setup-itom-visibility-landing-page&version=australia&pubname=australia-it-operations-management&ft:locale=en-US)**

Now Assist for Setup provides a centralized, guided installation experience for ITOM Visibility. From a single interface, administrators can review what applications are included in the installation, review the installation status, and install all required applications and plugins.


-   **[PowerShell 7 support for Discovery](https://www.servicenow.com/docs/access?context=powershell-remoting&version=australia&pubname=australia-it-operations-management&ft:locale=en-US)**

Discovery now supports PowerShell 7, while maintaining backward compatibility with PowerShell 5.1. This update enhances security, accelerates onboarding, and reduces deployment blockers through improved runtime detection and comprehensive test coverage.

-   **[Discovery on Code Signing instances](https://www.servicenow.com/docs/access?context=code-sign-disco-probes&version=australia&pubname=australia-it-operations-management&ft:locale=en-US)**

Discovery now enforces code signing for probes, parameters, and sensors to guarantee authenticity, integrity, and secure execution on MID Servers. This update blocks unsigned or tampered payloads, provides signature validation, and strengthens compliance by helping prevent audit gaps without impacting discovery performance.

-   **[Discovery generic attributes](https://www.servicenow.com/docs/access?context=disco-generic-attributes&version=australia&pubname=australia-it-operations-management&ft:locale=en-US)**

Enhance Configuration Management Database \(CMDB\) data accuracy with new Discovery capabilities that auto-populate non-discoverable attributes using a schedule-based mechanism. This update simplifies configuration item \(CI\) management by propagating generic attribute values across schedules and ranges, reducing manual effort and improving usability.

-   **[Use Kubernetes Visibility Agent \(KVA\) and Service Mapping to create service maps for extended services beyond Kubernetes](https://www.servicenow.com/docs/access?context=mapping-k8s-sm-kva&version=australia&pubname=australia-it-operations-management&ft:locale=en-US)**

Service Mapping complements Kubernetes Visibility Agent \(KVA\) capabilities to map services that include Kubernetes and all related service resources beyond the Kubernetes environment. Install the latest version of Kubernetes Visibility Agent \(KVA\) to detect the latest changes in your Kubernetes cluster and run Service Mapping to have an up to date visualization of your services across Kubernetes and related resources.

-   **[Quick start tests for Service Mapping](https://www.servicenow.com/docs/access?context=quick-start-tests-service-mapping&version=australia&pubname=australia-it-operations-management&ft:locale=en-US)**

After upgrades and deployments of new applications or integrations, run quick start tests to verify that Service Mapping works as expected. If you customized Service Mapping, copy the quick start tests and configure them for your customizations.


</td></tr><tr><td>

Identity

</td><td>

-   **[Granular admin roles](https://www.servicenow.com/docs/access?context=granular-admin-roles&version=australia&pubname=australia-platform-security&ft:locale=en-US)**

The granular admin role enables developers and administrators to complete administrative configuration tasks for Identity without requiring the full admin role.


</td></tr><tr><td>

Impact

</td><td>

-   **[Now Assist for Platform Health](https://www.servicenow.com/docs/access?context=impact-health-agent&version=australia&pubname=australia-impact&ft:locale=en-US)**

Help customers proactively identify, prioritize, and resolve technical debt by using the collection of AI-native tools embedded within the Impact Platform Health experience.

Track and resolve issues in developer code throughout the end-to-end workflow by reviewing and applying AI-recommended fixes through the [Remediate Scan Engine findings with Now Assist](https://www.servicenow.com/docs/access?context=code-fix-ai-remediation-agent&version=australia&pubname=australia-impact&ft:locale=en-US), which provides AI-generated code fixes for leading practice violations.

-   **[New Accelerators in the Australia Release](https://www.servicenow.com/docs/access?context=new-accelerators-australia-release&version=australia&pubname=australia-impact&ft:locale=en-US)**

Jumpstart your Impact Platform health, Data privacy, Walk-up experience, Digital product release, Modern change management, Major incident management, CSDM for service operations, and Integration hub by using technical Accelerators.

Improve your business outcomes by using the OCM: Preparing for change and adopt AI governance impact strategy Accelerators.

Assess your CSDM maturity, improve CSDM Data modeling, and accelerate your portal’s user experience with the help of usage insights and virtual agent experience design provided by the architecture Accelerators.

-   **[Roles installed with Impact](https://www.servicenow.com/docs/access?context=impact-roles&version=australia&pubname=australia-impact&ft:locale=en-US)**

Grant selected users with partner accounts access to the Impact Store Application through the new **Impact Partner** role. Users assigned with the partner role can efficiently manage Impact for their customers. You can view the users added as partners on the Impact homepage.

-   **[Manage Capabilities Maps for the Impact Store Application](https://www.servicenow.com/docs/access?context=manage-capability-maps&version=australia&pubname=australia-impact&ft:locale=en-US)**

The Capabilities Map homepage now shows true application capabilities organized by product line.


</td></tr><tr><td>

Import and Export

</td><td>

-   **[Enable large exports with parallel export sets](https://www.servicenow.com/docs/access?context=parallel-exports&version=australia&pubname=australia-integrate-applications&ft:locale=en-US)**

Export data with multiple small attachments in parallel. Exporting data in parallel can enable your integrations to finish in less time and create less of an impact on other tasks.

-   **[Use a connection alias for a JDBC data source](https://www.servicenow.com/docs/access?context=r_JDBCTypeDataSource&version=australia&pubname=australia-integrate-applications&section=create-import-connection-alias&ft:locale=en-US)**

Configure a separate connection alias for JDBC data sources. Configuring the connection alias separately enables you to reuse it rather than having to reconfigure it with each JDBC data source.


</td></tr><tr><td>

Incident Management

</td><td>

-   **[Introduction of granular admin roles](https://www.servicenow.com/docs/access?context=req-itsm-roles-inci-mgmt&version=australia&pubname=australia-it-service-management&ft:locale=en-US)**

Configure all the incident, major incident, task outage and related communication features for both UI16 and SOW using the following granular admin roles:

    -   sn\_incident\_admin: Configure all Incident Management features including incident management properties.
    -   sn\_mim\_admin: Configure all Major Incident Management features including major incident properties and trigger rules.
    -   sn\_tcm\_admin: Configure all Task Communications Management features including communication plans and tasks.
    -   sn\_iam\_admin: Configure all Incident Communications Management features including creating, editing, or canceling incident communication plan, communication task, and managing contact information. Additionally, this role can administrate all Incident Communications Management capabilities."
    -   sn\_contact\_admin: Configure all Contact Management features including creating and editing contact definitions, contact responsibilities, configuration of MI users, recipient lists, and groups.
    -   sn\_task\_outage\_admin: Configure all Task Outage features including the mapping between the Task \[task\] table and the Outage \[cmdb\_ci\_outage\] table.
-   **[Form channel for response templates](https://www.servicenow.com/docs/access?context=working-incident-record-form&version=australia&pubname=australia-it-service-management&ft:locale=en-US)**

The form channel is added to the Need more information and Schedule meeting response templates. The channel enables you to access the response templates from the incident record, copy the response templates texts to the clipboard from the incident form to be shared in the work notes, comments or other communication channels.


</td></tr><tr><td>

Industrial Connected Workforce Mobile Experience

</td><td>

-   **[Mobile Task Management](https://www.servicenow.com/docs/access?context=using-icw-mobile-experience&version=australia&pubname=australia-industrial-connected-workforce&ft:locale=en-US)**

Manage all task‑related activity from intuitive mobile views tailored for shop floor workers to improve visibility and responsiveness during operations.

Clear status indicators and color cues help in identifying critical or overdue tasks, improving responsiveness during operations.

-   **[Mobile Standards Hub](https://www.servicenow.com/docs/access?context=standards-hub-mobile&version=australia&pubname=australia-industrial-connected-workforce&ft:locale=en-US)**

Browse, request, and access published standards tailored to your functional location using the mobile Standards Hub.

Embedded rating and feedback mechanisms support continuous improvement of documentation and frontline usability.

-   **[Intuitive and minimal input actions](https://www.servicenow.com/docs/access?context=create-action-mobile&version=australia&pubname=australia-industrial-connected-workforce&ft:locale=en-US)**

Create actions, deviations, breakdowns, and follow‑up tasks directly from the mobile interface with minimal input to accelerate issue reporting.

Integrated escalation workflows help operators move seamlessly from detection to analysis, such as starting an RCA directly from a deviation.

-   **[Guided Task Execution](https://www.servicenow.com/docs/access?context=execute-igt-icw-mobile&version=australia&pubname=australia-industrial-connected-workforce&ft:locale=en-US)**

Execute guided tasks on the shop floor by following step‑by‑step instructions with embedded media, validation checks, and barcode or QR scanning.

Skill validation helps prevent unauthorized execution of tasks that require specific certifications or training.

-   **[Performance &amp; Reliability Enhancements](https://www.servicenow.com/docs/access?context=configure-now-mobile-agent-application-icw-mobile&version=australia&pubname=australia-industrial-connected-workforce&ft:locale=en-US)**

Continue working in low‑connectivity environments with offline caching that saves your progress and synchronizes updates when connectivity returns.

Optimized load times and reduced latency to create a smooth user experience across industrial environments.

-   **[Report any safety related incident](https://www.servicenow.com/docs/access?context=icw-mobile-report-safety-incident&version=australia&pubname=australia-industrial-connected-workforce&ft:locale=en-US)**

Report, triage, and investigate health and safety‑related incidents directly from the mobile interface through ICW integration with Health and Safety.

You can create Industrial Standards based on a safety incident that helps you maintain safe working environment.


</td></tr><tr><td>

Industrial Guided Tasks

</td><td>

-   **[Authoring Guided Tasks](https://www.servicenow.com/docs/access?context=task-authoring-configuration-settings&version=australia&pubname=australia-industrial-connected-workforce&ft:locale=en-US)**

Design structured workflows with sections, steps, assessments, and conditional paths by using an authoring interface that enforces consistency and quality.

Built‑in rules help to maintain consistency by following correct steps sequence, naming, and safety requirements. Authors can preview the guided tasks’ end‑user experience before publishing.

-   **[Assessment-driven scoring, evaluation, and execution](https://www.servicenow.com/docs/access?context=scoring-industrial-guided-tasks&version=australia&pubname=australia-industrial-connected-workforce&ft:locale=en-US)**

Capture and evaluate task data by using multiple assessment types, including numeric inputs, selections, measurements, and conditional evaluations. Supports multiple assessment types including numeric inputs, selections, measurements, and conditional evaluations.

Automatic scoring determines the following task outcomes based on configured thresholds: Successful, Unsuccessful, or Not Scored. Assessment data is captured for reporting, quality control, and continuous improvement.

-   **[Automation and Smart Actions](https://www.servicenow.com/docs/access?context=industrial-guided-tasks-reference&version=australia&pubname=australia-industrial-connected-workforce&ft:locale=en-US)**

Reduce manual intervention by configuring automation features that trigger follow‑up work, standard tasks, or actions based on assessment results.

Complex logic can route execution flows, creating dynamic experiences that adapt to operator input. This reduces manual intervention and maintains consistent responses to equipment or process conditions. You need an additional plugin to use this functionality.

Template capabilities for duplication of task structures.

-   **[Easy accessibility and execution](https://www.servicenow.com/docs/access?context=execute-igt-icw-mobile&version=australia&pubname=australia-industrial-connected-workforce&ft:locale=en-US)**

Execute guided tasks through a clean step‑by‑step interface that supports images, instructions, validations, and attachments for accurate task completion.

Integrated barcode or QR scanning helps identify parts, equipment, or materials during task execution.

Offline access to guided tasks in the ICW mobile application. Offline mode minimizes interruption in your work, even in low‑connectivity industrial environments.

-   **[IGT Lifecycle Governance](https://www.servicenow.com/docs/access?context=industrial-guided-task-life-cycle&version=australia&pubname=australia-industrial-connected-workforce&ft:locale=en-US)**

Govern your guided tasks through separated life-cycle states that provide clearer oversight and a better audit trail.

Review and approval workflows helps in maintaining quality, safety, and operational standards of guided tasks before release. Historical versions are archived for audits, root cause analysis \(RCA\) investigations, and long‑term reporting.

-   **[Create standards using templates](https://www.servicenow.com/docs/access?context=creating-standards-from-templates&version=australia&pubname=australia-industrial-connected-workforce&ft:locale=en-US)**

Accelerate guided task creation by duplicating existing tasks or using them as reusable templates.

Structural components such as steps, assessments, and conditional logic can be reused across multiple workflows, which maintains consistency while reducing authoring time.


</td></tr><tr><td>

Industrial Process Manager

</td><td>

-   **[Discovered subnets supported by the AMAZING feature](https://www.servicenow.com/docs/access?context=automate-mappings-between-ot-assets-and-equipment-model-entity&version=australia&pubname=australia-operational-technology&ft:locale=en-US)**

Use the AMAZING feature, which uses discovered subnets, to identify OT devices and assign them to the correct equipment model entity during OT subnet mapping.

-   **[Map OT devices to equipment model entities from the Equipment Model Manager](https://www.servicenow.com/docs/access?context=map-ot-devices-in-iw&version=australia&pubname=australia-operational-technology&ft:locale=en-US)**

Map OT devices to equipment model entities using the **Unmapped OT Devices** and the **All Devices** tabs in the Equipment Model Manager of the Industrial Workspace.

-   **[Generate a location hierarchy](https://www.servicenow.com/docs/access?context=create-location-hierarchy-isa&version=australia&pubname=australia-operational-technology&ft:locale=en-US)**

Generate a complete location hierarchy for an ISA equipment model entity tree when no locations exist to establish location references that match the ISA hierarchy.

-   **[Use the OT Network Map to visualize your OT network](https://www.servicenow.com/docs/access?context=utilizing-ot-network-map&version=australia&pubname=australia-operational-technology&ft:locale=en-US)**

Visualize your OT network, subnets, and device-to-device connections with the OT Network Map in the Industrial Workspace.


</td></tr><tr><td>

Industrial Standards

</td><td>

-   **[Industrial Standards Library](https://www.servicenow.com/docs/access?context=industrial-standards-library&version=australia&pubname=australia-industrial-connected-workforce&ft:locale=en-US)**

Browse and compare standards using an upgraded hub that provides tile and list views with filters for state, scope, category, functional location, and equipment model.

Users can quickly compare similar standards and see linked tasks, skills, and knowledge.

Access policies differentiate enterprise and site standards to help prevent misapplication.

-   **[Scheduling standards](https://www.servicenow.com/docs/access?context=scheduling-standards&version=australia&pubname=australia-industrial-connected-workforce&ft:locale=en-US)**

Generate recurring work from standards by configuring daily, weekly, monthly, and custom scheduling patterns to maintain a consistent operational cadence.

A system property \(for example, an offset in minutes\) lets admins align task creation with shift handovers or production calendar boundaries.

Runtime tracing improves visibility into created tasks, their status, and exceptions.

-   **[Skill-based task management](https://www.servicenow.com/docs/access?context=skill-based-task-management&version=australia&pubname=australia-industrial-connected-workforce&ft:locale=en-US)**

Define required skills or certifications within standards to ensure that only qualified operators execute safety‑critical tasks. Supervisors can request waivers or alternative routing when skills are missing.


</td></tr><tr><td>

Instance Data Replication

</td><td>

-   **[IDR Diagnostics page improvements](https://www.servicenow.com/docs/access?context=test-IDR-connectivity&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US)**

Access detailed test descriptions and results on the redesigned IDR Diagnostics page.


</td></tr><tr><td>

Instance Scan

</td><td>

-   **[Parallel execution of scans](https://www.servicenow.com/docs/access?context=hs-parallel-scan&version=australia&pubname=australia-platform-administration&ft:locale=en-US)**

Enable parallel execution of scans instead of sequential processing, eliminating bottlenecks and significantly reducing completion times.

-   **[New role to write checks in Instance Scan](https://www.servicenow.com/docs/access?context=hs-getting-started&version=australia&pubname=australia-platform-administration&ft:locale=en-US)**

Experience the new scan\_check\_writer role that has the privilege to write checks on the scan\_check table.

-   **[Instance Scan extension for IDE](https://www.servicenow.com/docs/access?context=hs-is-ide&version=australia&pubname=australia-platform-administration&ft:locale=en-US)**

You can now access Instance Scan from integrated development environment \(IDE\) on the ServiceNow AI Platform.


</td></tr><tr><td>

Integration Hub

</td><td>

-   **[Use Direct Kafka to integrate your on-premise ServiceNow instance with your local Kafka environment](https://www.servicenow.com/docs/access?context=direct-kafka&version=australia&pubname=australia-integrate-applications&ft:locale=en-US)**

Configure a custom Kafka connection to enable your on-premise instance to connect directly to your local Kafka environment.

-   **[Create topic aliases for Stream Connect topics](https://www.servicenow.com/docs/access?context=manage-topic-alias&version=australia&pubname=australia-integrate-applications&ft:locale=en-US)**

Use topic aliases to simplify topic management in Stream Connect. A topic alias is a unique topic name that can be connected to any underlying Hermes or Direct Kafka topic. A topic alias can be moved to different instances and, wherever they’re moved, connected to an underlying topic.

-   **[Stream Connect Dashboard updates](https://www.servicenow.com/docs/access?context=stream-connect-dashboard&version=australia&pubname=australia-integrate-applications&ft:locale=en-US)**
    -   The Topics menu displays topic aliases, Hermes topics, and Direct Kafka topics.
    -   The **Data usage** tab shows data for the Hermes cluster or the Direct Kafka cluster. Use the **Kafka Cluster** list to select which cluster data to display.
    -   The Consumers and Producers menus reference topic aliases instead of Hermes topics.
-   **[View the Remote Process Sync Dashboard](https://www.servicenow.com/docs/access?context=remote-process-sync-dashboard&version=australia&pubname=australia-integrate-applications&ft:locale=en-US)**

View detailed statistics and monitor the health of your Remote Process Sync \(RPS\) integrations. The Remote Process Sync Dashboard provides real-time visibility into key metrics, including records processed, queue sizes, processing times, and system status. Use this dashboard to identify issues, track performance trends, and promote smooth operation of your RPS integrations.

-   **[Produce messages to Hermes via a MID Server](https://www.servicenow.com/docs/access?context=MID-hermes-API&version=australia&pubname=australia-integrate-applications&ft:locale=en-US)**

Send message payloads to Hermes with MID script includes.

-   **[View usage metrics for Direct Kafka](https://www.servicenow.com/docs/access?context=direct-kafka-usage-metrics&version=australia&pubname=australia-integrate-applications&ft:locale=en-US)**

Track data usage between your instance and Direct Kafka systems. The Direct Kafka Usage metrics table provides administrators with visibility into data transfer volumes for bytes produced and consumed. View metrics aggregated by hour, day, or month at the cluster and topic level. Usage records are automatically retained for 13 months.

-   **[Use the read-only role for Stream Connect](https://www.servicenow.com/docs/access?context=stream-connect-apache-kafka-roles&version=australia&pubname=australia-integrate-applications&ft:locale=en-US)**

Use the new read-only role for Stream Connect to grant users view-only access to Stream Connect resources. Users with this role can view Stream Connect configurations and runtime statistics across all related modules, but can’t create, modify, or delete any Stream Connect settings.

-   **[View logs for Stream Connect producers](https://www.servicenow.com/docs/access?context=producer-statistics&version=australia&pubname=australia-integrate-applications&ft:locale=en-US)**

Get detailed log information for producers in the Stream Connect logs. Use the **glide.ih.kafka.producer.message\_bytes\_to\_log** property to specify how much of the message to display in the logs.

-   **[Configure alert thresholds for undelivered messages in Stream Connect](https://www.servicenow.com/docs/access?context=sc-alert-properties&version=australia&pubname=australia-integrate-applications&ft:locale=en-US)**

Set alert thresholds for undelivered messages based on how long a topic has gone without receiving new messages. Use this configuration to trigger INFO, WARNING, or CRITICAL alerts when message delivery stops for a specified period.

-   **[Configure alert thresholds for unprocessed messages in Stream Connect](https://www.servicenow.com/docs/access?context=sc-alert-properties&version=australia&pubname=australia-integrate-applications&ft:locale=en-US)**

Set alert thresholds for messages that remain unprocessed in a topic. You can trigger alerts based on how long messages sit in a topic without being consumed, helping to identify lagging or failing consumers.

-   **[Get metadata information for Stream Connect consumers](https://www.servicenow.com/docs/access?context=configure-script-consumer&version=australia&pubname=australia-integrate-applications&ft:locale=en-US)**

View the partition, offset, datacenter ID, and timestamp epoch for the script consumer and Kafka Message trigger.

-   **[View message timestamps in the Stream Connect script consumer](https://www.servicenow.com/docs/access?context=configure-script-consumer&version=australia&pubname=australia-integrate-applications&ft:locale=en-US)**

Get the message timestamp in the script consumer as a UTC time-zone string. You can use the UTC time-zone string to convert the timestamp to a **GlideDateTime** object.

-   **[Use an error subflow template to create your own error subflows in Remote Process Sync](https://www.servicenow.com/docs/access?context=getting-started-with-remote-process-sync&version=australia&pubname=australia-integrate-applications&ft:locale=en-US)**

Copy and modify the RPS Error Subflow Template to create error subflows. The template enables you to select notification methods for when the Inbound and Outbound States are errored.

-   **Specify attachment details in Remote Process Sync actions**

Specify the max attachment size and allowed attachment extensions in the [Identify New Attachments action](https://www.servicenow.com/docs/access?context=identify-new-attachments-action&version=australia&pubname=australia-integrate-applications&ft:locale=en-US) and the [Get Attachment Metadata for Local Record action](https://www.servicenow.com/docs/access?context=get-attachment-metadata-local-record-action&version=australia&pubname=australia-integrate-applications&ft:locale=en-US).

-   **Use a new retry policy for Remote Process Sync actions**

Retry failed requests at specified intervals with the RPS Push Attachment Policy. This policy works with the [Identify New Attachments action](https://www.servicenow.com/docs/access?context=identify-new-attachments-action&version=australia&pubname=australia-integrate-applications&ft:locale=en-US) and the [Get Attachment Metadata for Local Record action](https://www.servicenow.com/docs/access?context=get-attachment-metadata-local-record-action&version=australia&pubname=australia-integrate-applications&ft:locale=en-US).

-   **[SASL authentication support for Apache Kafka connections](https://www.servicenow.com/docs/access?context=hla-data-input-kafka-credentials&version=australia&pubname=australia-it-operations-management&ft:locale=en-US)**

Configure SASL authentication for your Apache Kafka connections with support for SASL\_SSL and SASL\_PLAINTEXT security protocols. Kafka credentials now support multiple SASL mechanisms: PLAIN- SCRAM-SHA-256, SCRAM-SHA-512.


</td></tr><tr><td>

Intelligence for CSM

</td><td>

-   **[ServiceNow product tiers](https://www.servicenow.com/docs/access?context=ai-native-sku-overview&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)**

The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets, and create your own
Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.

-   **[AI workflow tab added in Core UI](https://www.servicenow.com/docs/access?context=ai-workflow-pattern-in-customer-service-management&version=australia&pubname=australia-customer-service-management&ft:locale=en-US)**

Availability of AI Workflow tab within case view of case table records and email interaction view of interaction records in Core UI, showing agentic workflows and actionable AI-driven insights directly in the record UI.

-   **[Filter controls in Now Assist Guardian](https://www.servicenow.com/docs/access?context=now-assist-guardian-csm-filters&version=australia&pubname=australia-customer-service-management&ft:locale=en-US)**

Availability of filter controls for CSM in the Now Assist Guardian interface, allowing users to toggle the base system filters on and off. Filtered results display in a user-friendly format for quick case review and action.


-   **[Recommended Actions - View the relevancy score on the Case resolution guidance](https://www.servicenow.com/docs/access?context=nba-use-ai-search&version=australia&pubname=australia-customer-service-management&ft:locale=en-US)**

View the relevancy score, which indicates how well a search result matches the agent's query, on the search result recommendation cards in the Search tab of the Recommended Actions panel for the Case resolution guidance.

-   **[Recommended Actions – Configure contextual filtering of AI search results](https://www.servicenow.com/docs/access?context=ra-configure-contextual-filtering&version=australia&pubname=australia-customer-service-management&ft:locale=en-US)**

Enhance search accuracy by ensuring results are contextually relevant to the record being viewed by the agent. Search results are dynamically filtered based on contextual information passed through additional context parameters. To configure the contextual filtering of the Search results, enable the dynamic filter for a search source in a Search profile and then create the AisDynamicFilter implementation for the source which holds the filtering conditions.

-   **[Recommended Actions – Support for mandatory Contextual Inputs](https://www.servicenow.com/docs/access?context=ra-csm-create-context-inputs&version=australia&pubname=australia-customer-service-management&ft:locale=en-US)**

As an RA author, you can mark specific context inputs as mandatory by selecting the Mandatory check box in the Context Inputs form. When one or more context inputs are configured as mandatory, you must set the values for these contextual inputs directly on Recommended Actions component on the record page in the UI Builder for the recommendations to be generated.

-   **[Recommended Actions - Manage and conﬁgure metadata with delegated developer approach](https://www.servicenow.com/docs/access?context=ra-csm-installed-components&version=australia&pubname=australia-customer-service-management&ft:locale=en-US)**

Grant granular admin users delegated developer privileges and required roles to manage and configure metadata. This includes the Manage update set permission, domain\_picker role, and metadata\_scope\_viewer role for viewing and modifying the application scope of metadata records.

-   **[AI interaction wrap-up](https://www.servicenow.com/docs/access?context=interaction-wrapup-ai-generated&version=australia&pubname=australia-customer-service-management&ft:locale=en-US)**

Provides agents with AI assistance during the interaction wrap-up period. This feature generates wrap-up content for interaction records, such as the wrap-up code and notes.

-   **[Process mining - Pre‑configured templates for CSM Process Mining Projects](https://www.servicenow.com/docs/access?context=process-opt-csm&version=australia&pubname=australia-customer-service-management&ft:locale=en-US)**

Select pre‑configured templates from the Process Mining Content Pack for CSM to quickly set up customer service case projects with default settings already applied. These templates help accelerate project creation by providing standardized configurations tailored for common Customer Service Management scenarios.


</td></tr><tr><td>

Key Management

</td><td>

-   **[Added SHA512 support for message digests](https://www.servicenow.com/docs/access?context=c_GlideDigestScopedAPI&version=australia&pubname=australia-api-reference&ft:locale=en-US)**

GlideDigest has been updated to allow creation and verification of message digests using the SHA512 cryptographic hash function.

-   **Offline key exchange to share module keys between instances**

Admins can share module keys between instances offline to facilitate instance clones between on-premise instances using KMF.

-   **[Sign and verify JSON web tokens \(JWT\) through KMFCryptoOperation](https://www.servicenow.com/docs/access?context=KMFCryptoOperationBothAPI&version=australia&pubname=australia-api-reference&ft:locale=en-US)**

The signing and verification processes for JWTs are now integrated as operation types in the existing KMFCryptoOperation class.

-   **Centralized Crypto Management console**

Use the new Crypto Management Console to streamline and track the certificate management lifecycle. The new console scans your instance for certificates and displays their details in a central location,

-   **Clone and restore support for on-premise instances**

Support for cloning and restoring on-premise instances. Support has also been added from migrating a commercial instance to on-premise instances, and vice-versa.

-   **Certificate Revocation List \(CRL\) validation support**

ServiceNow now supports Certificate Revocation List \(CRL\) validation for certificate revocation checks as an alternative to Online Certificate Status Protocol \(OCSP\), with automatic fallback when OCSP is unavailable.


</td></tr><tr><td>

Knowledge Center

</td><td>

-   **[Search knowledge article](https://www.servicenow.com/docs/access?context=search-knowledge-article&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US)**

Build a complete and accurate knowledge base, focus on continuous improvement by discovering and filling content gaps, removing redundant information, and optimizing existing articles for better quality.


</td></tr><tr><td>

Knowledge Graph

</td><td>

-   ****

</td></tr><tr><td>

Lead Management

</td><td>

-   **[View touchpoint records for a task](https://www.servicenow.com/docs/access?context=lead-management-use-tasks-tab&version=australia&pubname=australia-order-management&ft:locale=en-US)**

Record early customer interactions and associate tasks with ongoing engagement throughout the pre‑deal sales lifecycle by:

    -   Creating a touchpoint from a lead to capture interactions such as discovery calls, follow‑up emails, or qualification meetings.
    -   Linking a task to a lead touchpoint to track follow‑up work related to an ongoing engagement until the lead is converted.

</td></tr><tr><td>

Legal Conflict of Interest

</td><td>

-   **[Configure risk assessment](https://www.servicenow.com/docs/access?context=lsd-coi-config-risk-fac&version=australia&pubname=australia-employee-service-management&ft:locale=en-US)**

The risk assessment utility evaluates conflict of interest disclosures against predefined risk factors to calculate a risk score and determine the risk level \(Low, Medium, or High\). The risk level automatically triggers the appropriate approval workflow. The utility supports three evaluation types: Condition, Subflow, and AI skill.

**Note:** AI skill evaluation is available once you have installed and configured Now Assist for Legal Service Delivery \(LSD\).

-   **[Submit COI request using Now Assist conversational intake](https://www.servicenow.com/docs/access?context=now-assist-lsd-convi&version=australia&pubname=australia-employee-service-management&ft:locale=en-US)**

Using natural language to submit a conflict of interest request from Now Assist in the Virtual Agent interface reduces the effort required to fill in form fields because details provided in natural language are automatically populated into the intake form. Achieve faster resolution due to automated risk assessment that routes requests to the appropriate approval workflow based on calculated risk scores.

**Note:** The conversational intake functionality is available only once you have installed and configured Now Assist for Legal Service Delivery \(LSD\).


</td></tr><tr><td>

Legal Matter Management

</td><td>

-   **[Attorney-Client Privilege](https://www.servicenow.com/docs/access?context=lsd-acp-landing&version=australia&pubname=australia-employee-service-management&ft:locale=en-US)**

Protect sensitive legal information by marking legal matters as Privileged &amp; Confidential, helping to ensure access is restricted to only authorized stakeholders.


</td></tr><tr><td>

Legal Request Management

</td><td>

-   **[Attorney Client Privilege](https://www.servicenow.com/docs/access?context=lmm-acp-landing&version=australia&pubname=australia-employee-service-management&ft:locale=en-US)**

Protect sensitive legal information by marking legal matters as Privileged &amp; Confidential, helping to ensure access is restricted to only authorized stakeholders.


</td></tr><tr><td>

Localization Workspace

</td><td>

-   **[Guided tours in the Localization Workspace interface](https://www.servicenow.com/docs/access?context=lw-language-setup&version=australia&pubname=australia-platform-administration&ft:locale=en-US)**

Leverage new guided tours that assist users with setting up language providers and language groups.

-   **[Language Asset Management](https://www.servicenow.com/docs/access?context=lw-language-asset-management&version=australia&pubname=australia-platform-administration&ft:locale=en-US)**

Upload, store, and edit multiple glossaries in the new **Language Asset Management** tab of Localization Workspace. Each glossary can include terms translated into multiple languages. In the Australia release, Language Asset Management provides upload, storage, and editing functions only.


</td></tr><tr><td>

Manufacturing Commercial Operations

</td><td>

-   ****

It’s a unified, AI-assisted life-cycle management from submission to resolution, helping teams capture quality inputs, identify duplicates early, take faster informed actions, and maintain control throughout.

-   ****

Dealers can submit product non-conformance issues through the dealer portal.

-   ****

It’s a playbook-driven resolution workflow that provides context-aware recommendations based on historical data. AI guidance identifies correction actions early, reducing manual analysis and enabling focus on validation, execution, and closure.

-   ****

Recall management data model for parts availability and parts groups enable OEMs to manage complex product recalls by structuring parts, assets, and customer data for identification, grouping, tracking, and allocation across recall phases.


</td></tr><tr><td>

Mobile Platform

</td><td>

-   **[Mobile offline enhancements](https://www.servicenow.com/docs/access?context=mobile-offline-mode&version=australia&pubname=australia-mobile&ft:locale=en-US)**

Use the following enhancements added to the mobile offline capability:

    -   Use the seamless online-to-offline continuity, by enabling users to start a form online, save it, and then proceed offline. While offline, users can continue viewing and editing the same data, including attachments, comments, and navigation, for uninterrupted productivity in low or no-connectivity environments. All changes automatically sync after your connection is restored.
    -   Save or submit forms offline, and reopen them later while still offline with all data fully restored.
    -   Support of offline capabilities for descriptive elements in input forms.
    -   Support of offline capabilities for input actions in input forms.
    -   Improved outbox efficiency for input forms by continually combining saved and submitted data.
-   **[Dedicated mobile\_admin role for mobile configuration](https://www.servicenow.com/docs/access?context=mobile-admin-role&version=australia&pubname=australia-mobile&ft:locale=en-US)**

Assign the new mobile\_admin role to administrators who configure mobile applications, granting them precisely the permissions needed to complete their tasks. This new role helps reduce reliance on the broader admin role for controlled, secure access of your ServiceNow® account.

-   **[Configurable timing for PIN application timeout](https://www.servicenow.com/docs/access?context=pin-timeout&version=australia&pubname=australia-mobile&ft:locale=en-US)**

Configure a new property to define the PIN timeout for different ServiceNow mobile apps. This configuration helps reinforce security by controlling how long users are can remain inactive before being required to reenter their PIN.

-   **[Dynamic variable support in record screens](https://www.servicenow.com/docs/access?context=record-screen-script-type&version=australia&pubname=australia-mobile&ft:locale=en-US)**

Use the script screen field in record screens to display dynamic field values. For example, you can display translated content for dynamic variables within an email.

-   **[Mobile AI Voice Agent](https://www.servicenow.com/docs/access?context=mobile-voice-agent&version=australia&pubname=australia-mobile&ft:locale=en-US)**

Speak with an AI-powered voice assistant on your mobile device for real-time support. Follow along with live conversation transcripts that can also be saved or shared after the call.

-   **[Push notifications for logged-out users](https://www.servicenow.com/docs/access?context=sg-mobile-push-notifications&version=australia&pubname=australia-mobile&ft:locale=en-US)**

Configure push notifications to be sent to users even when they’re logged out so critical updates aren't missed.


</td></tr><tr><td>

Next Experience

</td><td>

-   **[Enable auto-focus on page alerts new accessibility preference](https://www.servicenow.com/docs/access?context=enable-auto-focus-on-page-alerts&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US)**

Turn on the Enable auto-focus on page alerts preference to automatically move focus to the page alert. See the Accessibility section for details.

-   **[Next experience all menu editing](https://www.servicenow.com/docs/access?context=next-experience-all-menu-editing&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US)**

Create and edit application menus and modules directly from the Next Experience UI. Admins can configure Record, List, Dashboard, and Custom page modules from a centralized, platform-native interface.


</td></tr><tr><td>

Next Experience Components

</td><td>

|Component|Description|
|---------|-----------|
|Activity timer|Tracks time spent on an activity, such as working on a record, and creates time log entries for reporting.|
|Card data security container|Provides secure, encrypted handling of card details and supports uploading and viewing sensitive documents.|
|Contextual sidebar|Sidebar that enables users to initiate real-time collaboration through chats and calls to resolve tasks.|
|Grouped button|Multiple related buttons presented in a unified layout. Interactions for the component are similar to that of button stateful.|
|Sheet|Container that slides in from the edge of the screen to present related content or actions, designed for mobile experiences.|

|Template|Description|
|--------|-----------|
|Dashboard library|Includes all dashboards available to users. Users can filter dashboards by various criteria, such as recently opened, bookmarked, certified, by category, and ones the user owns. The Library section also lets users create dashboards. Users with analytics admin roles have an enhanced library view, enabling them to access usage data and other metadata. Admins can also deactivate, activate, or delete dashboards from this view.|
|Data visualization library|Includes all data visualizations available to users. Users can filter dashboards by various criteria, such as bookmarked, certified, and ones that the user owns. The Library section also lets users create dashboards. Users with analytics admin roles have an enhanced library view, enabling them to access usage data and other metadata. Admins can also deactivate, activate, or delete dashboards from this view.|

</td></tr><tr><td>

Notifications

</td><td>

-   **[User mailbox integration](https://www.servicenow.com/docs/access?context=personal-corporate-mailbox&version=australia&pubname=australia-platform-administration&ft:locale=en-US)**

Enable agents to integrate their personal corporate mail boxes to send and receive emails.

-   **[Granular admin roles required to secure the instance](https://www.servicenow.com/docs/access?context=granular-admin-roles-notifications&version=australia&pubname=australia-platform-administration&ft:locale=en-US)**

The granular admin role enables developers and administrators to complete administrative configuration tasks for Notifications without requiring the full admin role.

-   **[Notification agent](https://www.servicenow.com/docs/access?context=notification-creation-agent&version=australia&pubname=australia-platform-administration&ft:locale=en-US)**

The Notification agent enables platform administrators to create and modify email notifications and templates using natural language prompts, reducing the need of navigating complex forms &amp; scripts.


</td></tr><tr><td>

Notify

</td><td>

-   **[Granular admin roles in Notify](https://www.servicenow.com/docs/access?context=r_NotifyRoles&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US)**

Configure the Notify application features using the granular Notify admin role \(notify\_setup\_admin\).


</td></tr><tr><td>

Now Assist

</td><td>

-   **[ServiceNow product tiers](https://www.servicenow.com/docs/access?context=ai-native-sku-overview&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)**

The ServiceNow AI Platform now brings you an AI native experience with three licensing tiers available:

    -   Foundation: AI agents and skills to deliver insights
    -   Advanced: AI agents and skills to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI agents and skills, and create your own
-   **[Merge duplicate articles](https://www.servicenow.com/docs/access?context=merge-duplicate-articles&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US)**

Use Now Assist in Knowledge Management to merge selected duplicate knowledge articles into a single consolidated article, preserving references to the original sources and maintaining a high‑quality, well‑organized knowledge base.


</td></tr><tr><td>

Now Assist AI Agents

</td><td>

-   **[Create an AI agent](https://www.servicenow.com/docs/access?context=configure-next-best-action-agent&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)**

The AI-native experience for an AI agent is available exclusively with the installation of the Off Glide Conversation Server plugin \(com.glide.cs.offglide\).

**Note:** To use the AI agent in AI-native mode, make sure to test it so it works as expected.

-   **[Test an agentic solution in AI Native mode](https://www.servicenow.com/docs/access?context=test-ai-agent&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)**

Use the AI Native playground experience to test your agentic solutions.

**Note:** The AI-native playground experience is exclusively accessible when the Off Glide Conversation Server plugin \(com.glide.cs.offglide\) is installed. If the plugin is not installed, you will continue to access the standard testing playground.

-   **[Add tools and information to an AI agent](https://www.servicenow.com/docs/access?context=add-tool-aia&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)**

Add widgets for tool outputs to provide an improved experience in AI-native mode.

**Note:** The display output widget options are exclusively accessible when the Off Glide Conversation Server plugin \(com.glide.cs.offglide\) is installed. If the plugin is not installed, you will continue to access the standard add tool form.


</td></tr><tr><td>

Now Assist for Collaborative Work Management \(CWM\)

</td><td>

-   **[Now Assist formula generation for CWM tasks](https://www.servicenow.com/docs/access?context=generate-formula-cwm-board-now-assist&version=australia&pubname=australia-it-business-management&ft:locale=en-US)**

Generate formula columns by describing a calculation in plain language. When adding a formula column to the List view, prompt Now Assist to generate a formula by entering what you want to calculate. For example, `days between start date and end date` or `sum of estimated hours for subtasks`.

-   **[Now Assist scrum task generation for stories](https://www.servicenow.com/docs/access?context=generate-scrum-tasks-for-stories-cwm&version=australia&pubname=australia-it-business-management&ft:locale=en-US)**

Generate scrum tasks from user story descriptions and acceptance criteria using Now Assist. Trigger the scrum task generation from the story form or inline from the Sprint planning view, and receive a relevant set of tasks as a starting point for your sprint planning. You can then review, edit, and add the generated tasks to fit your team's workflow.


</td></tr><tr><td>

Now Assist for Configuration Management Database \(CMDB\)

</td><td>

-   **[ServiceNow product tiers](https://www.servicenow.com/docs/access?context=ai-native-sku-overview&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)**

The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets, and create your own
Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.


-   **[View CI attribute descriptions on CI forms](https://www.servicenow.com/docs/access?context=na-cmdb-skill-ci-form-help&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US)**

The skill answers your questions on CI classes and attributes to help you work in CI forms, dashboards, home pages, and other views on the workspace. You can submit similar queries on the Explore CI view.

-   **[CMDB searches can include relationships](https://www.servicenow.com/docs/access?context=na-cmdb-awf-search&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US)**

Search queries can depend on relationships between CIs and can span multiple tables. For example, you might ask: "Search for servers that depend on databases - only Linux servers running Redhat".

-   **[Search the Service Graph database using natural language](https://www.servicenow.com/docs/access?context=na-cmdb-skill-search-result-classfy&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US)**

Now Assist for CMDB analyzes your search criteria, identifies implicit filters, determines the optimum search method \(keyword search or query generation\), queries Service Graph data, and then displays the results. You then have the option to refine the search using natural language in the Now Assist panel.


</td></tr><tr><td>

Now Assist for Creator

</td><td>

-   **[Release lifecycle documentation AI agent](https://www.servicenow.com/docs/access?context=release-lifecycle-documentation-agent-landing&version=australia&pubname=australia-application-development&ft:locale=en-US)**

Improve transparency across your app development environment using the release lifecycle documentation AI agent to generate update set descriptions and release notes seamlessly.

-   **[Generate themes using the new theme generation workflow in Theme Builder](https://www.servicenow.com/docs/access?context=create-theme-now-assist&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US)**

Leverage the new theme generation workflow in Theme Builder to generate themes based on your brand image. After generating a theme, navigate to Theme Builder to publish and apply additional styling.

-   **[ServiceNow product tiers](https://www.servicenow.com/docs/access?context=ai-native-sku-overview&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)**

The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets, and create your own
Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.


-   **[Build Agent in ServiceNow Studio](https://www.servicenow.com/docs/access?context=build-agent-in-servicenow-studio&version=australia&pubname=australia-application-development&ft:locale=en-US)**

Use Build Agent in ServiceNow Studio to create and edit full-stack applications conversationally.

-   **[Generate modules using Now Assist](https://www.servicenow.com/docs/access?context=generate-ai-modules&version=australia&pubname=australia-application-development&ft:locale=en-US)**

Now Assist generates application modules in UI Builder workspaces using natural-language prompts. The Now Assist agent processes your prompts and generates various modules, including lists, records, URLs, scripts, dashboards, and folders.

-   **[New vibe coding documentation](https://www.servicenow.com/docs/access?context=vibe-coding-landing&version=australia&pubname=australia-application-development&ft:locale=en-US)**

Documentation is now available that introduces vibe coding, which is a natural language approach to application development in ServiceNow, including how to get started, when to use it, and how it fits within the broader suite of AI-powered development tools.


</td></tr><tr><td>

Now Assist for Employee Center Pro

</td><td>

-   **[Manage approvals with Now Assist Approval Assistance AI agent](https://www.servicenow.com/docs/access?context=manage-approvals-with-approvals-agent&version=australia&pubname=australia-employee-service-management&ft:locale=en-US)**

Accelerate request approvals by automatically aggregating relevant details, validating requests against policies, and recommending approval decisions to managers.

-   **[Quick start tests for Employee Center](https://www.servicenow.com/docs/access?context=quick-start-tests-employee-center&version=australia&pubname=australia-employee-service-management&ft:locale=en-US)**

After upgrades and deployments of new applications or integrations, run quick start tests to verify that Employee Center works as expected. If you customized Employee Center, copy the quick start tests and configure them for your customizations.


</td></tr><tr><td>

Now Assist for Enterprise Architecture \(EA\)

</td><td>

-   **[ServiceNow product tiers](https://www.servicenow.com/docs/access?context=ai-native-sku-overview&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)**

The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets, and create your own
Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.

-   **[Business application summarization skill enhancements](https://www.servicenow.com/docs/access?context=generate-insights-into-ba&version=australia&pubname=australia-application-portfolio-management&ft:locale=en-US)**

Generate context-sensitive business application summaries from the following pages:

    -   Business capability hierarchy page: On generating a business application summary from this page, information such as the associated primary and secondary capabilities and the position in the capability hierarchy are displayed along with the general information about the business application.
    -   Application rationalization list view page: On generating a business application summary from this page, information such as the indicator scores \(actual and normalized scores\), and associated demand details are displayed along with the general information about the business application.
    -   Application rationalization bubble chart page: On generating a business application summary from this page, information such as x and y-axis details, and planned disposition details are displayed along with the general information about the business application.
-   **[Generate insights for Enterprise Architecture Workspace dashboard widgets](https://www.servicenow.com/docs/access?context=generate-insights-ea-dashboard&version=australia&pubname=australia-application-portfolio-management&ft:locale=en-US)Now Assist**

Generate insights for the widgets available on the Enterprise Architecture Dashboard page using the Now Assist Explorer icon available on the header of each widget.

-   **[Diagram change analysis skill enhancements](https://www.servicenow.com/docs/access?context=compare-modeling-diagrams&version=australia&pubname=australia-application-portfolio-management&ft:locale=en-US)**
    -   Compare any two versions of a diagram and generate a summary of the changes.
    -   Select any version as a primary or secondary version to compare.
    -   Generate a summary for real-time changes made to the primary version while already comparing it to another diagram version.
    -   Modify diagram versions to compare using the Diagram comparison icon on the diagram comparison page.
    -   Identify differences faster when comparing two versions of a diagram, by using the color-coded highlights on the canvas. Newly added shapes and relationship lines appear in green and modified ones appear in yellow.

</td></tr><tr><td>

Now Assist for Financial Services Operations \(FSO\)

</td><td>

Australia Patch 1

-   **[Banking CSR support AI agent](https://www.servicenow.com/docs/access?context=agentic-contact-center-for-banking-agents-overview&version=australia&pubname=australia-financial-services-operations&ft:locale=en-US)**

Provides CSRs with AI-driven live assistance during voice calls. This AI agent monitors the transcript of the call. When prompted, the agent identifies customer intent, surfaces knowledge-based recommendations, and suggests next-best actions.

-   **[Customer interaction context summary skill](https://www.servicenow.com/docs/access?context=using-now-assist-for-financial-services-operations-fso&version=australia&pubname=australia-financial-services-operations&ft:locale=en-US)**

Generates a call-contextual customer summary in the Interaction workspace in the Agentic Contact Center for Banking. This summary is scoped to the intent of the inbound call, providing the agent with a snapshot of the customer's situation when the call begins.

-   **[Banking CSR customer insights AI agent](https://www.servicenow.com/docs/access?context=agentic-contact-center-for-banking-agents-overview&version=australia&pubname=australia-financial-services-operations&ft:locale=en-US)**

Enables CSRs to ask natural-language questions about a customer directly from the Customer 360 workspace. The agent aggregates data from predefined sources, then uses the information to generate accurate, contextually relevant answers.

-   **[Customer profile summarization skill](https://www.servicenow.com/docs/access?context=using-now-assist-for-financial-services-operations-fso&version=australia&pubname=australia-financial-services-operations&ft:locale=en-US)**

Provides AI-generated summaries directly on the Customer 360 workspace in the Agentic Contact Center for Banking, reducing navigation across multiple systems.

-   **[ServiceNow product tiers](https://www.servicenow.com/docs/access?context=ai-native-sku-overview&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)**

The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets, and create your own
Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.


</td></tr><tr><td>

Now Assist for IT Service Management \(ITSM\)

</td><td>

[Australia Patch 1](../quality/australia-patch-1.md)

-   **[ServiceNow product tiers](https://www.servicenow.com/docs/access?context=ai-native-sku-overview&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)**

The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets, and create your own
Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.

-   **[Incident assist agentic workflow](https://www.servicenow.com/docs/access?context=now-assist-itsm-incident-assist-workflow&version=australia&pubname=australia-it-service-management&ft:locale=en-US)**

Answer incident-related questions using context-aware agents. Handle queries about incident details and get information about related records.

-   **[Enhancements to the Incident assist skill](https://www.servicenow.com/docs/access?context=now-assist-itsm-incident-assist&version=australia&pubname=australia-it-service-management&ft:locale=en-US)**

The features in the \[DEPRECATED\] Incident assist skill are available in the Incident assist agentic workflow. You may turn off this skill and use the agentic workflow that has enhanced capabilities.

-   **[Creating a catalog item for unlocking accounts using the voice AI agent](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-voice&version=australia&pubname=australia-it-service-management&ft:locale=en-US)**

Use the Submit account unlock catalog with the voice AI agent, which is a primer, to create a catalog item to unlock the specified account when a user calls the help desk.

-   **[Enhancements to Troubleshoot Outlook issue with voice AI agent](https://www.servicenow.com/docs/access?context=now-assist-itsm-aiagents-voice&version=australia&pubname=australia-it-service-management&ft:locale=en-US)**

Email relevant troubleshooting articles and instructions to users when you troubleshoot Outlook issues for them.

-   **[Knowledge Article Advanced Editor page](https://www.servicenow.com/docs/access?context=Now-Assist-generate-article-SOW-itsm&version=australia&pubname=australia-it-service-management&ft:locale=en-US)**

Use the new Knowledge Article Advanced Editor page to create or edit Knowledge articles using open prompts.

-   **[ITSM Conversational analytics dashboard](https://www.servicenow.com/docs/access?context=using-itsm-conversational-analytics-dashboard&version=australia&pubname=australia-it-service-management&ft:locale=en-US)**

Get insights into virtual agent adoption, usage trends, and track metrics in Now Assist in Virtual Agent.

-   **[Getting summary of an incident in the Details tab](https://www.servicenow.com/docs/access?context=summarize-incident-now-assist&version=australia&pubname=australia-it-service-management&ft:locale=en-US)**

Resolve incidents faster by getting the incident summary in the **Details** tab of the incident.

-   **[Configure summaries and responses for Request Management records](https://www.servicenow.com/docs/access?context=cust-now-assist-request-summarization-skill&version=australia&pubname=australia-it-service-management&ft:locale=en-US)**

As an admin, you can configure the following Request Management skills:

    -   Request summarization
    -   Requested item summarization
    -   Catalog task summarization
    -   Request activity response generation
    -   Requested item activity response generation
-   **[Summarize Request Management records](https://www.servicenow.com/docs/access?context=summarize-request-related-skill&version=australia&pubname=australia-it-service-management&ft:locale=en-US)**

View an aggregate of all relevant updates and progress indicators in a single, dynamic summary.

-   **[Generate a response to request activity](https://www.servicenow.com/docs/access?context=summarize-request-related-activity-response-generation&version=australia&pubname=australia-it-service-management&ft:locale=en-US)**

Generate a response in record activity streams of requests and requested items.

-   **[DEX issue diagnosis and resolution agentic workflow](https://www.servicenow.com/docs/access?context=now-assist-itsm-dex-diagnosis-resolution-workflow&version=australia&pubname=australia-it-service-management&ft:locale=en-US)**

Service desk agents can diagnose and resolve Zoom call quality issues using the Digital End-User Experience \(DEX\) issue diagnosis and resolution agentic workflow, which integrates Zoom- specific diagnostics that correlate device, network, and application data.

-   **[AI-powered root cause analysis for Zoom call quality issues](https://www.servicenow.com/docs/access?context=investigate-and-resolve-zoom-call-issues&version=australia&pubname=australia-it-service-management&ft:locale=en-US)**

Use Now Assist for Zoom call issues to identify the root cause of call quality degradation and review the supporting metric evidence for deeper insight. The analysis highlights the contributing device and network factors directly in the Zoom call quality view. Get the real-time guidance, including device ready remedial actions, contextual self-help instructions, and relevant Knowledge articles to help resolve the issue efficiently.

-   **[Get AI driven insights for boot time performance](https://www.servicenow.com/docs/access?context=investigate-and-resolve-boot-time-issues&version=australia&pubname=australia-it-service-management&ft:locale=en-US)**

Monitor device boot time to identify slow start-up issues and use Now Assist to investigate the root cause and get suggested resolutions, including remedial actions, self-help instructions, and Knowledge articles to resolve boot performance problems quickly.


</td></tr><tr><td>

Now Assist for Legal Service Delivery \(LSD\)

</td><td>

-   **[Submit COI request using Now Assist conversational intake](https://www.servicenow.com/docs/access?context=now-assist-lsd-convi&version=australia&pubname=australia-employee-service-management&ft:locale=en-US)**

Submit a Conflict of Interest \(COI\) request through a natural language conversation. The conversational intake for Legal Conflict of Interest is available in the base system.


</td></tr><tr><td>

Now Assist for Manufacturing Commercial Operations \(MCO\)

</td><td>

[Australia Patch 1](../quality/australia-patch-1.md)

-   **[ServiceNow product tiers](https://www.servicenow.com/docs/access?context=ai-native-sku-overview&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)**

The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets, and create your own
Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.

-   ****

Use the detect potential fraudulent claims to analyze dealer warranty claims for duplicate claims, mismatched parts and supporting documents/images, reused images/documents, similar claims within specified periods or for same end customers across assets, and product usage inconsistencies.

-   ****

Use the plan and execute recall campaign phases and sub-phases AI agent for recall campaign planning and execution through multiple phases and sub-phases. The AI agent generates phases based on parts availability, asset location, operational readiness, and regulatory approvals, with key actions including phase plan creation, modification, recall manager approval, and impacted asset assignment.

-   ****

It’s a playbook-driven portal with AI capabilities for description refinement, field prediction, entity extraction, duplicate identification via intelligent search, and pre-submission correction details for improved resolution.


</td></tr><tr><td>

Now Assist for Operational Sustainability Management

</td><td>

-   **[ServiceNow product tiers](https://www.servicenow.com/docs/access?context=ai-native-sku-overview&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)**

The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets, and create your own
Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.


-   **[Document intelligence for utility invoices](https://www.servicenow.com/docs/access?context=ai-driven-document-intelligence-for-utility-invoices&version=australia&pubname=australia-environmental-social-governance&ft:locale=en-US)**

After upgrading Now Assist for Operational Sustainability Management to version 22.0.1, the system automatically extracts unit values from invoices and updates metric data accordingly. This automation reduces manual data entry and improves data accuracy.


</td></tr><tr><td>

Now Assist for Operational Technology Service Management \(OTSM\)

</td><td>

-   **[Summarize an Operational Technology incident by using Now Assist for Operational Technology Service Management \(OTSM\)](https://www.servicenow.com/docs/access?context=summarize-ot-incident-now-assist&version=australia&pubname=australia-operational-technology&ft:locale=en-US)**

Automatically summarize an OT incident using the **Summarize** UI action to produce a concise summary of the incident.

-   **[Generate resolution notes for an Operational Technology incident](https://www.servicenow.com/docs/access?context=generate-resolution-notes-ot-incident&version=australia&pubname=australia-operational-technology&ft:locale=en-US)**

Automatically generate resolution notes for an OT incident using the **Generate resolution notes** UI action to produce a concise summary of the incident.

-   **[Generate OT KB articles agentic workflow](https://www.servicenow.com/docs/access?context=agent-ot-knowledge-generator&version=australia&pubname=australia-operational-technology&ft:locale=en-US)**

Automatically generate a KB article for an OT incident when the state of the incident is set to **Resolved**. The article contains the following information:

    -   Site
    -   OT Device
    -   Equipment model entity
    -   Summarization
    -   Resolution notes
    -   KB Base
    -   Author

</td></tr><tr><td>

Now Assist for Sales and Order Management for Telecommunications \(SOMT\)

</td><td>

[Australia Patch 1](../quality/australia-patch-1.md)

-   **[ServiceNow product tiers](https://www.servicenow.com/docs/access?context=ai-native-sku-overview&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)**

The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets, and create your own
Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.

-   **[Order fallout AI agent](https://www.servicenow.com/docs/access?context=now-assist-order-fallout-somt&version=australia&pubname=australia-telecom-media-technology&ft:locale=en-US)**

Automatically create fallout records mapped to existing fallout types for streamlined error tracking and follow-up.

-   **[Move Order Voice AI agent](https://www.servicenow.com/docs/access?context=now-assist-move-order-somt&version=australia&pubname=australia-telecom-media-technology&ft:locale=en-US)**

Use this agent to help you create a move order capture journey by collecting details such as the customer’s name, current service location, product offering, and new service address.


</td></tr><tr><td>

Now Assist for Setup

</td><td>

-   **[Enhanced Admin Home experience](https://www.servicenow.com/docs/access?context=ia-explore&version=australia&pubname=australia-platform-administration&ft:locale=en-US)**

Leverage an enhanced Admin Home dashboard to centralize access to Now Assist for Setup and key applications, with context‑aware guidance and recommended next actions, available after installing the Now Assist for Setup store app.

-   **[Centralized application setup](https://www.servicenow.com/docs/access?context=ia-administer&version=australia&pubname=australia-platform-administration&ft:locale=en-US)**

You can now set up Now Assist Admin and other entitled applications directly from Admin Home using a guided experience that installs required components and applies default configurations from a single starting point.

-   **[Product module Product Hubs](https://www.servicenow.com/docs/access?context=ia-explore&version=australia&pubname=australia-platform-administration&ft:locale=en-US)**

You can now access product‑specific Product Hubs from Admin Home to discover, install, and configure entitled Now Assist products through guided setup flows that install required components and apply default configurations.

-   **[Guided module configuration](https://www.servicenow.com/docs/access?context=ia-config-landing&version=australia&pubname=australia-platform-administration&ft:locale=en-US)**

Configure the Platform module and applicable product modules from a unified configuration experience that guides you through module‑specific setup, with the Platform module appearing only when the selected product includes platform‑level changes for the installation.


</td></tr><tr><td>

Now Assist for Source-to-Pay Operations

</td><td>

-   **[Now Assist for Sourcing and Procurement Operations \(SPO\)](https://www.servicenow.com/docs/access?context=now-assist-spo&version=australia&pubname=australia-source-to-pay-operations&ft:locale=en-US)**

[Analyze sentiment in procurement cases](https://www.servicenow.com/docs/access?context=analyze-sentiments-na-spo&version=australia&pubname=australia-source-to-pay-operations&ft:locale=en-US)Helps procurement specialists to analyze procurement case fields and live agent chats to determine the tone of the fulfiller.

[Generate email responses](https://www.servicenow.com/docs/access?context=email-response-na-spo&version=australia&pubname=australia-source-to-pay-operations&ft:locale=en-US)Analyze procurement case, sourcing request, purchase requisition, sourcing event, negotiation, and stretch items like procurement, sourcing, and receipt tasks to generate professional email response. This eliminates the need to manually look up information across multiple records and allows procurement specialists to handle inquiries effectively.

[Upload a Statement of Work \(SOW\) to request a purchase](https://www.servicenow.com/docs/access?context=now-assist-spo-upload-sow&version=australia&pubname=australia-source-to-pay-operations&ft:locale=en-US) Upload SOW documents to submit purchase requests. AI agents parse your documents, extract relevant data, and prepopulate your request, enabling you to focus on reviewing and approving submissions instead of manual data entry.

[Conversational intake for sourcing and procurement agentic workflow](https://www.servicenow.com/docs/access?context=spo-help-fulfill-pr-agentic&version=australia&pubname=australia-source-to-pay-operations&ft:locale=en-US) Streamline end‑to‑end procurement workflows with a conversational intake experience powered by AI agent support. AI agents guide you through relevant steps while providing contextual recommendations and real-time progress updates.

[Automatically assign categories during SR and PR creation](https://www.servicenow.com/docs/access?context=automatically-assign-categories&version=australia&pubname=australia-source-to-pay-operations&ft:locale=en-US) Automatically classify service requests, purchase requisitions, and purchase orders into the correct spend categories using the spend categorization AI agent.

-   **[Now Assist for Supplier Lifecycle Operations \(SLO\)](https://www.servicenow.com/docs/access?context=now-assist-slo&version=australia&pubname=australia-source-to-pay-operations&ft:locale=en-US)**

[AI driven supplier onboarding using Now Assist for SLO](https://www.servicenow.com/docs/access?context=supplier-onboarding-agentic-workflow&version=australia&pubname=australia-source-to-pay-operations&ft:locale=en-US) Use theAI driven supplier onboarding workflow to automate data validation, duplicate checking, task generation, and supplier communication. Key enhancements include:

    -   Extract banking information from uploaded documents to reduce information mismatch.
    -   Use the document strategy generator AI agent to generate a customized onboarding task list using all published knowledge base articles.
    -   View a list of AI-suggested suppliers while reviewing supplier onboarding requests initiated through sourcing requests.
    -   Supplier relationship managers can manually approve or reject supplier onboarding requests.
    -   Resolve duplicate supplier onboarding requests from the Now Assist panel by updating the supplier legal name, contact email, or both.
[Automate supplier case creation from emails](https://www.servicenow.com/docs/access?context=automated-supplier-case-creation-from-emails&version=australia&pubname=australia-source-to-pay-operations&ft:locale=en-US) Convert supplier emails into cases automatically when registered supplier contacts send emails to a supplier inbox. Supplier cases are created for all SLO related queries and assigned to the supplier relationship manager. For queries unrelated to SLO, a universal request is created for resolution.

[Summarize supplier performance in Source-to-Pay Workspace](https://www.servicenow.com/docs/access?context=summarize-supp-perf&version=australia&pubname=australia-source-to-pay-operations&ft:locale=en-US) Generate comprehensive supplier performance summaries, including performance data, trends, and actionable insights, using the supplier performance summarization skill.

[Analyze sentiments in supplier cases](https://www.servicenow.com/docs/access?context=slo-analyze-sentiments&version=australia&pubname=australia-source-to-pay-operations&ft:locale=en-US) Use the sentiment analysis skill to analyze supplier case fields and determine the tone or sentiment of the fulfiller.

[Generate an email response for supplier cases](https://www.servicenow.com/docs/access?context=generate-email-response-for-supplier-case&version=australia&pubname=australia-source-to-pay-operations&ft:locale=en-US) Use the email response skill to analyze the supplier case details and generate professional email response regardless of the record type using past email responses, KB articles, and related tasks.


-   **[Source-to-Pay Operations common skills](https://www.servicenow.com/docs/access?context=source-to-pay-common-skills&version=australia&pubname=australia-source-to-pay-operations&ft:locale=en-US)**

The Email response generation skill uses generative AI to automatically draft professional, context-aware email responses for supplier inquiries, procurement communications, and AP case management across Source-to-Pay workflows \(APO, SPO, SLO\), reducing manual effort and improving response consistency.

The Sentiment analysis skill uses large language models to detect emotional tone \(Positive, Negative, or Neutral\) in cases across Source-to-Pay workflows \(APO, SPO, SLO\).

The AI Data Explorer for Source-to-Pay \(APO, SPO, SLO\) supports AI-driven prompt understanding, recommended queries, and drill-down capabilities within a unified interface.


-   **[Now Assist for Accounts Payable Operations \(APO\)](https://www.servicenow.com/docs/access?context=now-assist-apo&version=australia&pubname=australia-source-to-pay-operations&ft:locale=en-US)**

Use the accounts payable document classification skill to identify and categorize email attachments, such as invoices, credit memos, and supporting documents, that were sent by suppliers.


-   **[Now Assist for Purchase Order Management \(POM\)](https://www.servicenow.com/docs/access?context=now-assist-for-purch-order-magmt&version=australia&pubname=australia-source-to-pay-operations&ft:locale=en-US)**

Convert supplier emails into purchase order exceptions automatically when a registered supplier contact sends emails to a supplier inbox. Purchase order exceptions are created for all purchase order queries and assigned to the operational buyer. For queries unrelated to purchase order exceptions, a universal request is created.

Use the define PO exception mitigation strategy agentic workflow in Now Assist for POM to identify and execute mitigation strategies by analyzing delivery gaps and proposing order changes with alternative suppliers.


</td></tr><tr><td>

Now Assist for Strategic Portfolio Management \(SPM\)

</td><td>

[Australia Patch 1](../quality/australia-patch-1.md)

-   **[ServiceNow product tiers](https://www.servicenow.com/docs/access?context=ai-native-sku-overview&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)**

The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets, and create your own
Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.

-   **[Summarize demand records with the demand summarization skill](https://www.servicenow.com/docs/access?context=demand-summarization-skill&version=australia&pubname=australia-it-business-management&ft:locale=en-US)**

Generate a concise, structured summary of any demand using the demand summarization skill through the **Summarize** button in the demand form. The skill reviews the demand fields and helps create a clear summary of the demand.

-   **[AI-generated project status reporting](https://www.servicenow.com/docs/access?context=create-a-status-report-in-project-workspace&version=australia&pubname=australia-it-business-management&ft:locale=en-US)**

Generate AI-powered project status reports for quick visibility into project health and executive summaries.

-   **[AI insights for a project](https://www.servicenow.com/docs/access?context=use-projects-pw&version=australia&pubname=australia-it-business-management&ft:locale=en-US)**
    -   Use the **AI insights** page to view consolidated information about project tasks, milestones, resources, financials, and RIDACs.
    -   Configure the insights to monitor critical project elements, such as financials and RIDACs, for a project.
    -   Send AI‑generated project insights via email, including financials, RIDACs, milestones, resources, and project tasks.
    -   Track key project indicators, such as budget overruns, cost variance, high‑risk items, issues, decisions, overdue actions, and change requests.
-   **Additional admin configuration for the project insights generation skill**

Configure additional settings as an admin for the project insights generation skill. Choose inputs, display and review the changes.

-   **[AI-generated insights for goals](https://www.servicenow.com/docs/access?context=generate-insights-for-goal&version=australia&pubname=australia-it-business-management&ft:locale=en-US)**

Generate AI‑powered insights using the goal insights skill to gain predictive, actionable visibility into goal health. By analyzing the goal, goal targets, subgoals, and aligned work, the system delivers data‑driven insights that help goal owners and contributors manage risks proactively and improve goal outcomes. Insights include AI-forecasted status, confidence of achieving the goal, targets at risk, and aligned work or recommendations that have been delayed or stalled.

-   **[Story generation for epics in Agile Development 2.0 and EAP](https://www.servicenow.com/docs/access?context=generate-stories-quickly-for-eap-and-agile-2-0&version=australia&pubname=australia-it-business-management&ft:locale=en-US)**

Generate a complete user story, including title, description, and acceptance criteria, directly from an epic instead of creating one. By providing one or two lines of context, you can generate a story and edit inline before saving. This skill is available in both Agile Development 2.0 and EAP.


</td></tr><tr><td>

Now Assist for Telecommunications, Media and Technology \(TMT\)

</td><td>

-   **[Squad resource identifier](https://www.servicenow.com/docs/access?context=now-assist-squad-resource-identifier&version=australia&pubname=australia-telecom-media-technology&ft:locale=en-US)**

Recommend internal experts based on engagement context, skill set, region, and real-time availability. Assist customer success teams to quickly identify and connect with the right individuals to support success plays, initiatives, or critical escalations, helping to ensure faster and more effective collaboration across engagements.

-   **[Product release email communication](https://www.servicenow.com/docs/access?context=now-assist-product-release-email-communication&version=australia&pubname=australia-telecom-media-technology&ft:locale=en-US)**

Automatically draft, refine, and publish release announcement emails. It identifies the right stakeholders, helps to ensure consistent messaging, and streamlines distribution.

-   **Risk signals and solution synchronization**

Monitor solution records linked to risk signals and automatically sync updates back to the original risk signal record. Notify customer success managers with a summarized status, and prompt them to close resolved risks.

-   **Create product adoption roadmaps using Now Assist**

Use generative AI to create product adoption roadmaps by analyzing customer characteristics, identifying similar products, and matching customer goals. Provide contract-level insights to support more effective renewal conversations and expansion opportunities.

-   **Support renewals and expansion**

Analyze renewal readiness automatically by evaluating health scores, product usage, and value achievement metrics using the Renewal Insight Engine. After receiving assessment reports, create opportunities directly within the renewal playbook.

-   **Customer 360 AI insights**

Analyze call, chat, billing, and interaction data with Knowledge Graph and Workflow Data Fabric. Provide service and network insights with recommendations on potential customer faults. Deliver task-based insights on recent cases, orders, A2A integration with RADCOM, voice agent interactions, and sentiment analysis related to customer health.

-   **Auto-onboarding**

Reduce onboarding complexity for consumers with automated onboarding. This feature autonomously manages onboarding workflows, establishes secure connections, synchronizes settings, and continuously monitors for errors to help ensure reliable, efficient integrations with minimal manual effort.

-   **[Analyze the sentiment of a service problem case using Now Assist for TMT](https://www.servicenow.com/docs/access?context=now-assist-tmt-analyze-sentiment-spc-adr&version=australia&pubname=australia-telecom-media-technology&ft:locale=en-US)**

Generates the customer's sentiment and the reasoning behind it on the complaint cases. Make informed decisions on complaint cases based on sentiment and link them to the Alternative Dispute Resolution \(ADR\) case record.

-   **[Summarize the linked records using Now Assist for Telecommunications, Media and Technology \(TMT\)](https://www.servicenow.com/docs/access?context=now-assist-tmt-summarize-linked-record&version=australia&pubname=australia-telecom-media-technology&ft:locale=en-US)**

Generate a comprehensive summary of the service problem case records that you have linked on the ADR case.

-   **[Generate resolution notes for Alternative Dispute Resolution case using Now Assist for TMT](https://www.servicenow.com/docs/access?context=now-assist-tmt-generate-resolution-notes-ad&version=australia&pubname=australia-telecom-media-technology&ft:locale=en-US)**

Enables you to generate resolution for the customer dispute in the ADR case record. You can propose this resolution to the customer and get the customer feedback.

-   **[Generate a deadlock letter using Now Assist for TMT](https://www.servicenow.com/docs/access?context=now-assist-tmt-generate-deadlock-letter&version=australia&pubname=australia-telecom-media-technology&ft:locale=en-US)**

Generate details of a deadlock letter for an ADR case. If the customer doesn't agree with the ADR case resolution, then you can use this skill to generate the deadlock letter and share with the customer.


[Australia Patch 1](../quality/australia-patch-1.md)

-   **[ServiceNow product tiers](https://www.servicenow.com/docs/access?context=ai-native-sku-overview&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)**

The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets, and create your own
Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.

-   **[Squad resource identifier](https://www.servicenow.com/docs/access?context=now-assist-squad-resource-identifier&version=australia&pubname=australia-telecom-media-technology&ft:locale=en-US)**

Recommend internal experts based on engagement context, skill set, region, and real-time availability. Assist customer success teams to quickly identify and connect with the right individuals to support success plays, initiatives, or critical escalations, helping to ensure faster and more effective collaboration across engagements.

-   **[Product release email communication](https://www.servicenow.com/docs/access?context=now-assist-product-release-email-communication&version=australia&pubname=australia-telecom-media-technology&ft:locale=en-US)**

Automatically draft, refine, and publish release announcement emails. It identifies the right stakeholders, helps to ensure consistent messaging, and streamlines distribution.

-   **[Recommend risk signal solutions](https://www.servicenow.com/docs/access?context=now-assist-tmt-resolve-risk&version=australia&pubname=australia-telecom-media-technology&ft:locale=en-US)**

Monitor solution records linked to risk signals and automatically sync updates back to the original risk signal record. Notify customer success managers with a summarized status, and prompt them to close resolved risks.

-   **[Generate product adoption roadmaps using Now Assist](https://www.servicenow.com/docs/access?context=now-assist-tmt-generate-par-roadmap&version=australia&pubname=australia-telecom-media-technology&ft:locale=en-US)**

Use generative AI to create product adoption roadmaps by analyzing customer characteristics, identifying similar products, and matching customer goals. Provide contract-level insights to support more effective renewal conversations and expansion opportunities.

-   **[Support renewals and expansion](https://www.servicenow.com/docs/access?context=now-assist-tmt-renewal-analyzer&version=australia&pubname=australia-telecom-media-technology&ft:locale=en-US)**

Analyze renewal readiness automatically by evaluating health scores, product usage, and value achievement metrics using the Renewal Insight Engine.

-   **[Generate Telecom customer 360 insights](https://www.servicenow.com/docs/access?context=c360-ai-insights&version=australia&pubname=australia-telecom-media-technology&ft:locale=en-US)**

Provide data source configurability to bring call, chat, billing data from external sources and generate insights. Deliver task-based insights on recent cases, orders, and sentiment analysis related to customer health.

-   **[Generate resolution notes for Alternative Dispute Resolution case using Now Assist for TMT](https://www.servicenow.com/docs/access?context=now-assist-tmt-generate-resolution-notes-ad&version=australia&pubname=australia-telecom-media-technology&ft:locale=en-US)**

Generates resolution notes for a customer dispute in the Alternative Dispute Resolution \(ADR\) case record.

-   **[Analyze the sentiment of a service problem case using Now Assist for TMT](https://www.servicenow.com/docs/access?context=now-assist-tmt-analyze-sentiment-spc-adr&version=australia&pubname=australia-telecom-media-technology&ft:locale=en-US)**

Analyze customer sentiment on the case records that are linked with the customer dispute. This skill enables you to select the relevant linked records for ADR case record.

-   **[Summarize the linked records using Now Assist for Telecommunications, Media and Technology \(TMT\)](https://www.servicenow.com/docs/access?context=now-assist-tmt-summarize-linked-record&version=australia&pubname=australia-telecom-media-technology&ft:locale=en-US)**

Generates a comprehensive summary the case records that are linked to the customer dispute in the ADR case record.

-   **[Generate a deadlock letter using Now Assist for TMT](https://www.servicenow.com/docs/access?context=now-assist-tmt-generate-deadlock-letter&version=australia&pubname=australia-telecom-media-technology&ft:locale=en-US)**

Generates a deadlock letter details for a customer dispute in the ADR case record. You can generate the deadlock letter when the customer rejects the complaint resolution and opt for legal procedures.

-   **[Now Assist for Telecommunications, Media and Technology \(TMT\) AI agent collection preliminary troubleshooter agentic workflow](https://www.servicenow.com/docs/access?context=now-assist-tmt-preliminary-troubleshooter-agentic-workflow&version=australia&pubname=australia-telecom-media-technology&ft:locale=en-US)**

Processes task requests that require payment status, contextual information from similar cases and Knowledge Base articles.

-   **[Now Assist for Telecommunications, Media and Technology \(TMT\) AI agent collection service test and repair agentic workflow](https://www.servicenow.com/docs/access?context=now-assist-tmt-service-test-repair-agentic-workflow&version=australia&pubname=australia-telecom-media-technology&ft:locale=en-US)**

Runs the test groups that are mapped to a task and creates repair tasks for the failed test runs. This workflow also updates the consolidated summary in work notes and runs autonomously in the background without any user interaction.


-   **[Remote hands case record](https://www.servicenow.com/docs/access?context=generate-summary-for-remote-hands-case-record&version=australia&pubname=australia-telecom-media-technology&ft:locale=en-US)**

Remote Hands Request Summarization generates contextual summary of a Remote Hands case by combining current case data with insights from similar historical cases, using information submitted by the DCIM user through the CSM portal.


</td></tr><tr><td>

Now Assist in Contract Management

</td><td>

-   **[Feedback for Now Assist contract analysis](https://www.servicenow.com/docs/access?context=cmpro-review-contract-document&version=australia&pubname=australia-employee-service-management&ft:locale=en-US)**

Provide feedback on AI-identified non-standard and missing clauses to help improve AI accuracy over time. When reviewing contracts using Now Assist contract analysis, you can indicate whether the AI suggestions were helpful or not helpful by using the thumbs up or thumbs down feedback options. You can also provide optional qualitative feedback with comments. The feedback option is available in both the workspace and Microsoft Word add-in.

The feedback provided on each clause is captured in the **Contracts Gen AI Feedback** table.

-   **[Automatically navigate to non-standard clauses in Microsoft Word add-in](https://www.servicenow.com/docs/access?context=cmpro-review-contract-document&version=australia&pubname=australia-employee-service-management&ft:locale=en-US)**

Locate non-standard clauses easily in Microsoft Word. The document scrolls to the relevant section using AI citations when you select a Now Assist suggestion in the Microsoft Word add-in.


</td></tr><tr><td>

Now Assist in Document Intelligence

</td><td>

-   **[ServiceNow product tiers](https://www.servicenow.com/docs/access?context=ai-native-sku-overview&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)**

The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets, and create your own
Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.


-   **[Document and visual insights AI agent enhancements](https://www.servicenow.com/docs/access?context=document-and-visual-insights-ai-agent&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)**

The document and visual insights AI agent can recognize and provide citations for multiple attachments.


</td></tr><tr><td>

Now Assist in Virtual Agent

</td><td>

-   ****

</td></tr><tr><td>

On-Call Scheduling

</td><td>

-   **[Monthly roster rotation for an on-call schedule](https://www.servicenow.com/docs/access?context=create-update-schedule-oncall&version=australia&pubname=australia-it-service-management&ft:locale=en-US)**

Simplify shift management by configuring a monthly roster rotation for an on-call schedule. This option is available only for the 2024 schedule engine.

-   **[Granular role for on-call schedule configurations](https://www.servicenow.com/docs/access?context=roles-assigning-oncall&version=australia&pubname=australia-it-service-management&ft:locale=en-US)**

Configure on-call schedule features using the granular and specific role, sn\_on\_call\_admin. It contains sn\_trigger\_table\_cfg\_read and sn\_trigger\_table\_cfg\_write roles.


</td></tr><tr><td>

Operational Resilience

</td><td>

-   **[Export action task reports in Microsoft Word, Microsoft Excel, and JSON formats](https://www.servicenow.com/docs/access?context=work-on-action-tasks&version=australia&pubname=australia-governance-risk-compliance&ft:locale=en-US)**

Export DRIR assessment action task reports in Microsoft Word, Microsoft Excel, or JSON format from a drop-down menu. Generate Microsoft Word documents for narrative reports, Microsoft Excel spreadsheets with structured question-answer layouts, or JSON files for system integrations.

-   **[Convert and aggregate contractual expenses to regulator-required currencies](https://www.servicenow.com/docs/access?context=currency-conversion-aggregation&version=australia&pubname=australia-governance-risk-compliance&ft:locale=en-US)**

Standardize annual expense values during Register of Information report generation by enabling optional currency conversion and third-party total expense aggregation. The application converts contract amounts to a base currency using 32 European Central Bank \(ECB\) exchange rates based on the reference date. Administrators upload monthly rates into the system. When eligibility criteria are met, expenses across multiple contracts are aggregated by third-party providers or engagements, generating consolidated reports that comply with DORA regulatory requirements.


</td></tr><tr><td>

Operational Sustainability Management \(formerly Environmental, Social, and Governance\)

</td><td>

-   **[ServiceNow product tiers](https://www.servicenow.com/docs/access?context=ai-native-sku-overview&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)**

The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets, and create your own
Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.


-   **[Integrating Operational Sustainability Management with Socialsuite](https://www.servicenow.com/docs/access?context=integrate-operational-sustainability-with-SocialSuite&version=australia&pubname=australia-environmental-social-governance&ft:locale=en-US)**

After upgrading Operational Sustainability Management to version 22.0.1, streamline sustainability reporting and compliance processes by conducting CSRD-compliant double materiality assessments in Socialsuite and automatically syncing the results with Operational Sustainability Management. This integration supports impact and financial materiality assessments following Global Reporting Initiative \(GRI\) and European Sustainability Reporting Standards \(ESRS\) standards.

-   **[Create a threshold for a metric](https://www.servicenow.com/docs/access?context=create-a-threshold-for-a-metric&version=australia&pubname=australia-environmental-social-governance&ft:locale=en-US)**

After upgrading Operational Sustainability Management to version 22.0.1, you can configure thresholds with multiple levels and ranges for granular monitoring. Duplicate and modify existing thresholds to streamline creation. When thresholds are breached, automated actions trigger immediately.


</td></tr><tr><td>

Operational Technology Incident Management

</td><td>

-   **[ServiceNow product tiers](https://www.servicenow.com/docs/access?context=ai-native-sku-overview&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)**

The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets, and create your own
Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.


-   **[Summarize an Operational Technology incident by using Now Assist for Operational Technology Service Management \(OTSM\)](https://www.servicenow.com/docs/access?context=summarize-ot-incident-now-assist&version=australia&pubname=australia-operational-technology&ft:locale=en-US)**

Automatically summarize an OT incident using the **Summarize** UI action to produce a concise summary of the incident.

-   **[Generate resolution notes for an Operational Technology incident](https://www.servicenow.com/docs/access?context=generate-resolution-notes-ot-incident&version=australia&pubname=australia-operational-technology&ft:locale=en-US)**

Automatically generate resolution notes for an OT incident using the **Generate resolution notes** UI action to produce a concise summary of the incident.

-   **[Generate OT KB articles agentic workflow](https://www.servicenow.com/docs/access?context=agent-ot-knowledge-generator&version=australia&pubname=australia-operational-technology&ft:locale=en-US)**

Automatically generate a KB article for an OT incident when the state of the incident is set to **Resolved**. The article contains the following information:

    -   Site
    -   OT Device
    -   Equipment model entity
    -   Summarization
    -   Resolution notes
    -   KB Base
    -   Author
-   **[Use the Employee Center for OT to report an OT incident](https://www.servicenow.com/docs/access?context=report-ot-incident-in-ot-employee-portal&version=australia&pubname=australia-operational-technology&ft:locale=en-US)**

Create an OT incident as a user without an OT incident role with the Report OT incident item in the Employee Center for OT.


</td></tr><tr><td>

Operational Technology Manager

</td><td>

-   **[ServiceNow product tiers](https://www.servicenow.com/docs/access?context=ai-native-sku-overview&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)**

The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets, and create your own
Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.


-   **[Operational Technology Network Map](https://www.servicenow.com/docs/access?context=utilizing-ot-network-map&version=australia&pubname=australia-operational-technology&ft:locale=en-US)**

Use the OT network map available in the Industrial Workspace to view the subnets of a site and the OT devices in each subnet.

-   **[CMDB OT class model updates](https://www.servicenow.com/docs/access?context=cmdb-ci-class-models-operation-technology&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US)**

Configure for your OT devices with the following CMDB OT class model updates:

    -   The IP Network Subnets related list was added to IT devices in the OT view to show all the subnets related to the device and show IP Network subnets for the selected OT device.
    -   The IP Network Subnets related list was added to the following CMDB classes:

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
    -   Because the OT device details are included in the form view of the CMDB class table, the **OT device details** tab was removed for the following CMDB classes:
        -   cmdb\_ci\_aix\_server
        -   cmdb\_ci\_hpux\_server
        -   cmdb\_ci\_pc\_hardware
        -   cmdb\_ci\_hyper\_v\_server
        -   cmdb\_ci\_esx\_server
        -   cmdb\_ci\_solaris\_server
        -   cmdb\_ci\_unix\_server
        -   cmdb\_ci\_ups
    -   Admins can edit the protection policy for an OT View rule for all CMDB classes.

</td></tr><tr><td>

Opportunity Management

</td><td>

-   **[View touchpoint records for a task](https://www.servicenow.com/docs/access?context=opportunity-management-tasks-tab&version=australia&pubname=australia-order-management&ft:locale=en-US)**

Gain complete visibility into customer engagement by viewing a complete touchpoint timeline on every opportunity so that teams have context at their fingertips.

-   **[Add competitors to an opportunity](https://www.servicenow.com/docs/access?context=opportunity-management-competitors-tab&version=australia&pubname=australia-order-management&ft:locale=en-US)**

Identify and store competitor information for product offerings/product family within an opportunity.​


-   **Support for opportunity allocation**

Divide sales credit across multiple contributors on a single opportunity for accurate attribution and compensation.


-   **[Customer entities on opportunity](https://www.servicenow.com/docs/access?context=opportunity-management-details-tab&version=australia&pubname=australia-order-management&ft:locale=en-US)**

Capture the deal type \(Direct or Indirect\) on customer entities to align opportunities with defined routes to market and support consistent, compliant processing across systems and teams.


</td></tr><tr><td>

Order Management

</td><td>

-   **[Delta pricing on orders](https://www.servicenow.com/docs/access?context=net-pricing-sp-contracts&version=australia&pubname=australia-order-management&ft:locale=en-US)**

Calculate pricing and quantity changes during MACD activities and renewals by deriving deltas from existing products, contracts, or purchases. This improves accuracy when processing order modifications.

    -   Defaults contract type and contract line type when empty, based on the order and line actions being performed.
    -   Adds delta pricing–related header and line fields, along with pricing adjustment rule identifiers and conditions, and supports mapping these fields across order, product instance, and order copy flows.
-   **[Price and quantity ramps on order line items](https://www.servicenow.com/docs/access?context=defining-products-with-ramps&version=australia&pubname=australia-order-management&ft:locale=en-US)**

View price and quantity ramps directly on order line items to model planned changes over time within a single order, providing visibility into pricing changes without managing multiple orders. For more information, see the [Product Catalog Management and Pricing Management release notes](../sales-order-management/product-catalog-pricing-management-rn.md)

-   **[Manage order updates with Now Assist](https://www.servicenow.com/docs/access?context=bulk-update-order-lines-with-now-assist&version=australia&pubname=australia-order-management&ft:locale=en-US)**

Use a conversational AI assistant to improve order triage and resolution. The assistant understands order context and supports guided actions such as updating shipping addresses and quantities across order line items. For more information, see the .


</td></tr><tr><td>

Password Reset

</td><td>

-   **[Granular admin roles in Password Reset](https://www.servicenow.com/docs/access?context=r_InstalledWithPasswordReset&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US)**

Configure the Password Reset application features using the granular Password Reset admin role \(password\_reset\_admin\).


</td></tr><tr><td>

Performance Analytics

</td><td>

-   **[Create data snapshots indicators](https://www.servicenow.com/docs/access?context=create-ds-automated-indicator&version=australia&pubname=australia-now-intelligence&ft:locale=en-US)**

Create data snapshots indicators and their sources rather than being able to enable data snapshots only on existing indicators. Benefit from the simplicity of data snapshots indicators, including the escape from the two-level breakdown limit. You can create either automated or formula indicators. Access control for these indicator is the same as for classic Performance Analytics indicators.

-   **[Create intraday indicators](https://www.servicenow.com/docs/access?context=create-ds-source&version=australia&pubname=australia-now-intelligence&ft:locale=en-US)**

Track process changes at a more granular level than daily, such as by work shift. Data snapshots indicator sources support business calendars with intraday periods, which can be as short as per minute.


</td></tr><tr><td>

Platform Analytics experience

</td><td>

-   **[New UI Builder templates for Dashboards and Data visualization libraries](https://www.servicenow.com/docs/access?context=reuse-page-definitions&version=australia&pubname=australia-application-development&ft:locale=en-US)**

Create Dashboard and Data Visualization library pages within your workspaces in UI Builder by using new page templates.

-   **[View usage information in the data visualization library](https://www.servicenow.com/docs/access?context=dashboards-for-admin-users&version=australia&pubname=australia-now-intelligence&ft:locale=en-US)**

As an analytics manager, view usage statistics in the data visualization library. Those statistics include the number of reports, data visualizations that aren't used in any dashboards, and the number of data visualizations not viewed for more than six months.

-   **[Get recommendations to review problematic analytics resources](https://www.servicenow.com/docs/access?context=pa-library-recommendations&version=australia&pubname=australia-now-intelligence&ft:locale=en-US)**

As an analytics manager, view recommendations for which artifacts you should fix or delete in the Dashboard, Data Visualization, and Indicator libraries.

-   **[Executive dashboards](https://www.servicenow.com/docs/access?context=executive-dashboard-overview&version=australia&pubname=australia-now-intelligence&ft:locale=en-US)**

Use the new Executive Dashboards, which have been rebuilt using the Platform Analytics in-line dashboard capabilities.

-   **[View data snapshot indicators in data visualizations](https://www.servicenow.com/docs/access?context=config-dv-sing-sc-ind-data&version=australia&pubname=australia-now-intelligence&ft:locale=en-US)**

Add indicators that are built from data snapshots sources to data visualizations.


</td></tr><tr><td>

Playbook

</td><td>

-   **[Nested playbooks](https://www.servicenow.com/docs/access?context=nested-playbooks&version=australia&pubname=australia-build-workflows&ft:locale=en-US)**

Nest playbooks as a step within other playbooks to enable the following scenarios:

    -   Define sets of activities for reuse across multiple playbooks to help avoid duplication.
    -   Break up large playbooks for easy maintenance and fast load time in Playbook Designer.
-   **[Simplified end-user playbook experience](https://www.servicenow.com/docs/access?context=wizard-layouts-playbooks&version=australia&pubname=australia-build-workflows&ft:locale=en-US)**

Implement a wizard experience for guiding your end users through a sequence of steps to achieve an outcome, such as servicing a printer.

-   **[Automated Test Framework support for playbooks](https://www.servicenow.com/docs/access?context=testing-support-playbooks&version=australia&pubname=australia-build-workflows&ft:locale=en-US)**

The Automated Test Framework can be used to create automated tests to confirm your playbooks run as planned.


</td></tr><tr><td>

Policy and Compliance Management

</td><td>

-   **[Control objective workflow](https://www.servicenow.com/docs/access?context=concept_cob_workflow&version=australia&pubname=australia-governance-risk-compliance&ft:locale=en-US)**

Aftr upgrading Policy and Compliance Management to 22.0.1, the new Control objective workflow feature introduces a structured lifecycle for managing control objective records. This feature is controlled by the Enable Control Objective Workflow property under Policy and Compliance &gt; Properties and is disabled by default.

Key highlights:

    -   When disabled, only the State field is added to control objective records. Active records show Published, inactive records show Retired, and new records default to Draft.
    -   When enabled, control objectives move through: Draft, Review, Approved, Current version, and Retired. The following new fields are also introduced: State, Effective date, Revision type, and Record nature.
    -   Editing a published control objective creates a working draft, keeping the published record active until approved changes are published.
    -   Users must select a revision type: Major or Minor. A Major revision moves associated controls back to Draft. A Minor revision applies updates without moving controls back to Draft.
    -   The Owner and Owning Group fields control who can edit the control objective and perform workflow actions.
-   **[Rationalizing control objectives](https://www.servicenow.com/docs/access?context=take-actions-on-the-recommendations-for-similar-control-objectives&version=australia&pubname=australia-governance-risk-compliance&ft:locale=en-US)**

After upgrading Policy and Compliance Management to 22.0.1, both Unified Compliance Framework \(UCF\) control objectives and non-UCF control objectives can be rationalized together. Key highlights include:

    -   Recommendation cards show a Source field to indicate whether it originates from UCF or a non-UCF source.
    -   As UCF control objectives cannot be deactivated, the Identify Duplicates and Finalize sub-states guide the users to retain the UCF control objective. Any UCF recommendations that are not retained are automatically dismissed when the user requests review.
    -   Only one UCF control objective can be retained at a time. If you retain a different UCF control objective, the previously retained one is automatically dismissed.
    -   When rationalization is complete, the retained UCF control objective stays active, accepted non-UCF recommendations are deactivated, and any dismissed UCF control objectives remain active and unchanged.

</td></tr><tr><td>

Portfolio Planning

</td><td>

-   **[Next Experience for Demand Management](https://www.servicenow.com/docs/access?context=demand-workspace-ppw&version=australia&pubname=australia-it-business-management&ft:locale=en-US)**

Manage strategic and operational demands in a unified experience in Portfolio Planning. This Next Experience interface consolidates demand creation, assessment, collaboration, and conversion in one place, eliminating context switching and reducing reliance on the classic Demand Workbench.

-   **[Create and manage demands in Next Experience for Demand Management](https://www.servicenow.com/docs/access?context=managing-demands-ppw&version=australia&pubname=australia-it-business-management&ft:locale=en-US)**
    -   Create and manage a demand in Next Experience for Demand Management using guided tabs. These tabs help you define alignment, estimate costs, and confirm readiness as you build out the demand.
    -   Collaborate on demands through Docs, which syncs execution and planning.
    -   View, add, and edit cost plans and budgeting details using related lists.
-   **[Use Playbook in Next Experience for Demand Management](https://www.servicenow.com/docs/access?context=use-playbooks-in-ppw&version=australia&pubname=australia-it-business-management&ft:locale=en-US)**

Help teams manage demands with greater structure and consistency using Playbook in Next Experience for Demand Management.

Playbooks enable you to define multiple governance processes across the organization using a low‑code/no‑code configuration experience. Create clear stages and guided activities from demand intake to completion by using a default playbook or creating a custom playbook to support your organization’s multiple demand management processes.

-   **[Associate AI systems with demands in Next Experience for Demand Management](https://www.servicenow.com/docs/access?context=use-playbooks-in-ppw&version=australia&pubname=australia-it-business-management&ft:locale=en-US)**

Use a playbook activity in Next Experience for Demand Management to associate AI systems with a demand. You can link impacted systems and add new ones directly within the demand workflow.

-   **[Portfolio plan enhancements](https://www.servicenow.com/docs/access?context=work-prioritization-portfolio-planning&version=australia&pubname=australia-it-business-management&ft:locale=en-US)**
    -   Access the Hierarchy tab directly from the Planning page, located next to the Prioritization tab. This new placement replaces the previous access point within the Prioritization tab, providing a more efficient way to view and manage planning items.
    -   Save filter views specific to the Hierarchy tab without affecting views in the Prioritization tab.
    -   View planning items in the new Hierarchy tab on the Planning page, now sorted using global rank when available. Drag and drop is supported for lowest‑level items, enabling you to rerank them within their groups.
-   **[Financials for planning items](https://www.servicenow.com/docs/access?context=using-financials-spw&version=australia&pubname=australia-it-business-management&ft:locale=en-US)**

View the financial baselines in investment currency and project currency after migrating them from Classic to Next Experience. Migrated financial baselines include actuals, costs, benefits, and budget values from the project currency to the investment currency.

Using multicurrency, new and existing customers see only investment currency fields in demand and project records. Planned costs, actual costs, planned benefits, actual benefits, and budget fields are included in the financial baselines.

    -   .
        -           -   


</td></tr><tr><td>

Predictive Intelligence

</td><td>

-   **[Predictive Intelligence Usage Analytics dashboard](https://www.servicenow.com/docs/access?context=predictive-intel-usage-analytics&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)**

Usage Analytics dashboard is a central location to understand the adoption, effectiveness, and overall value of all your Predictive Intelligence solutions. Dashboard widgets offer several metrics such as total monthly count of predictions per solution type.


</td></tr><tr><td>

Privacy Management

</td><td>

-   **[Report a privacy case anonymously](https://www.servicenow.com/docs/access?context=report-privacy-case-anonymously&version=australia&pubname=australia-governance-risk-compliance&ft:locale=en-US)**

Employees can now use the Anonymous Reporting Center to report privacy violations such as data breaches or exposure, unauthorized data use, privacy law violations \(GDPR, CCPA\), or other privacy-by-design lapses without revealing their identity or location.

Accessed through the Employee Center, the Anonymous Reporting Center portal automatically logs users out to enforce anonymity, creates case records without mapping to employee identity, and provides a unique report key for secure follow-up communication.

Reports are routed to the appropriate compliance team based on the nature of the concern. Throughout the investigation process:

    -   Investigators can request additional information through a comments system visible to the reporter
    -   Reporters can follow up on their case using their report key to check progress and respond to questions
    -   All interactions maintain reporter anonymity at every step; no identity or location data is ever captured or linked
This enhancement enables organizations to build trust, mitigate risks before escalation, and ensures regulatory compliance with whistleblower protection requirements.

-   **[GRC case summarization skill for privacy cases](https://www.servicenow.com/docs/access?context=privacy-case-summarization-skill&version=australia&pubname=australia-governance-risk-compliance&ft:locale=en-US)**

Privacy analysts can now use the Now Assist case summarization feature to quickly understand a privacy case without manually reviewing every field or related list. Now Assist analyzes key case attributes, such as timelines, impacted areas, evidence, and actions, and generates a structured summary directly inside the privacy case. This solves a common problem: case data is often lengthy, scattered across multiple related lists, and difficult for analysts to digest efficiently. Analysts can also save and edit summaries as case data evolves, ensuring the record stays current.

-   **[Hierarchy and lineage enhancements](https://www.servicenow.com/docs/access?context=hierarchy-tab&version=australia&pubname=australia-governance-risk-compliance&ft:locale=en-US)**

The Hierarchy and lineage enhancements enables privacy teams to identify which systems, vendors, and applications belong to a specific processing activity by marking relationships as “part of a processing activity.” This differentiates scoped components from global or shared connections. Users can toggle between a processing‑activity‑scoped view and a full lineage view, helping them understand data flows in the appropriate context.

-   **[Privacy content accelerator](https://www.servicenow.com/docs/access?context=privacy-content-accelerator&version=australia&pubname=australia-governance-risk-compliance&ft:locale=en-US)**

The privacy regulatory content through Unified Content Management provides pre‑built authority documents, citations, control objectives, and risk statements aligned with major privacy frameworks, including GDPR, CCPA, LGPD, and the NIST Privacy Framework 1.0. These resources are available for download directly from the Privacy Workspace, enabling teams to readily access standardized regulatory content.


</td></tr><tr><td>

Process Mining

</td><td>

-   **[Parallel processing for playbook data introduced](https://www.servicenow.com/docs/access?context=export-to-playbook&version=australia&pubname=australia-now-intelligence&ft:locale=en-US)**

Analyze ServiceNow Playbooks, including their stages and individual activities using Process Mining. This capability enables Playbook authors and business process owners to do performance evaluations and optimize Playbooks.


-   **[Process Step filter \(Previously Transition filter\) &amp; Rule-based Findings enhanced](https://www.servicenow.com/docs/access?context=rule-based-builder&version=australia&pubname=australia-now-intelligence&ft:locale=en-US)**

Unlock new use cases and drive better process optimization outcomes through the enhanced process step filter and rule-based findings.

-   **[Intent and Activity analysis available with Now Assist](https://www.servicenow.com/docs/access?context=now-assist&version=australia&pubname=australia-now-intelligence&ft:locale=en-US)**

Efficiently summarize \(human\) agent tasks and their sequence in relation to problem types so you can pinpoint areas for improvement and take concrete actions to optimize your processes.

-   **[Mine Agentic AI logs](https://www.servicenow.com/docs/access?context=set-objectives&version=australia&pubname=australia-now-intelligence&ft:locale=en-US)**

Create a Process Mining project on Agentic AI data logs by selecting the designated source from a readily available template.

-   **[Integration with Task Mining](https://www.servicenow.com/docs/access?context=task-mining&version=australia&pubname=australia-now-intelligence&ft:locale=en-US)**

Gain insights on the time the workstation users spend and how they accomplish tasks by analyzing their activities. Uncover inefficiencies, standardize best practices, and identify automation opportunities. You can create a Task Mining project from Opportunity details page and Analyst workbench of Process Mining.

-   **[New automated findings introduced](https://www.servicenow.com/docs/access?context=automated-findings&version=australia&pubname=australia-now-intelligence&ft:locale=en-US)**

Use the following automated findings to identify improvement opportunities where records follow specific patterns:

    -   Extreme duration \(Node\): Identifies patterns where records stay in a step for a significantly longer duration than usual
    -   High touchpoints \(Node\): Identifies patterns where a group of records in a step gets updated more often compared to another group to progress to any next step.
    -   Extreme touchpoints \(Node\): Identifies patterns where a step requires unusually large number of record updates than the normal range to progress to any next step.
    -   Slow duration \(Node\): Identifies patterns where a group of records stays longer in a step than the average duration of another group.
-   **[Multidimensional projects filters](https://www.servicenow.com/docs/access?context=filter-project&version=australia&pubname=australia-now-intelligence&ft:locale=en-US)**

Make analysis easier by filtering multidimensional projects based on child breakdowns and variants as a substitute for filtering on child attributes.

-   **[Evaluation project for security operations available](https://www.servicenow.com/docs/access?context=evaluation-security&version=australia&pubname=australia-now-intelligence&ft:locale=en-US)**

Try out an evaluation project for security incidents, which can provide improvement opportunities based on assignment group changes, time analysis, priority escalations, and automated indicators such as repeated states and assignment groups. You can target a maximum of 3.6K records that have been closed in the last seven days.

-   **[Introduced views to the Platform Analytics workspace for Process Mining](https://www.servicenow.com/docs/access?context=analyst-workbench-dashboard&version=australia&pubname=australia-now-intelligence&ft:locale=en-US)**

Display specific activity definitions within the Platform Analytics workspace for Process Mining using views. When working with graphs that contain multiple activity definitions, views help filter the map to show only activities relevant to the problem being analyzed.

-   **[Multidimensional maps are supported on the Opportunity details page and Platform Analytics components](https://www.servicenow.com/docs/access?context=opportunity-details&version=australia&pubname=australia-now-intelligence&ft:locale=en-US)**

Quickly analyze process maps with multiple tables through multidimensional maps on the Opportunity details page and Platform Analytics component of Process Mining.


</td></tr><tr><td>

Product Catalog Management and Pricing Management

</td><td>

-   **[Product families](https://www.servicenow.com/docs/access?context=product-catalog-managment&version=australia&pubname=australia-order-management&ft:locale=en-US)**

Create product families to provide hierarchical classification similar to category trees. For example, you can use product families to roll up or aggregate measurable items, such as revenue forecasts for reporting or business insights.


-   **[Renewal pricing for products with price and quantity ramps](https://www.servicenow.com/docs/access?context=defining-products-with-ramps&version=australia&pubname=australia-order-management&ft:locale=en-US)**

Calculate renewal pricing for products with price and quantity ramps, using per year, per term, and price only uplift calculation methods.

-   **Derived pricing support for sold products**
    -   Use the `DerivedProductPriceExtensionPoint` extension to determine whether a source line for a quote or sold product and a target line are pairs.
    -   Use the `getAccountLevelDerivedPricedProductsLookupData(pricingEngineContext)` method to control the records scanned by the pricing engine to determine account-level derived prices for sold products.
    -   The pricing engine does the following:
        -   Displays a message indicating when a change to a source product affects the price of a derived product.
        -   Checks product offerings and excludes product offerings with child offerings from derived pricing.
-   **[Multi-attribute pricing rules](https://www.servicenow.com/docs/access?context=som-create-pricing-adjustment&version=australia&pubname=australia-order-management&ft:locale=en-US)**

Display attribute-based pricing on transaction lines, where the offer price is determined by the combination of attributes, by setting up attribute-based pricing for product offerings based on multiple, combined attributes using the Attribute Adjustment matrix.

-   **[Blended pricing support for contract renewals](https://www.servicenow.com/docs/access?context=pricing-management&version=australia&pubname=australia-order-management&ft:locale=en-US)**

Enable sales agents to apply automatically calculated blended unit prices for renewals, based on the existing product price and the renewal uplift required. Blended pricing is used in upsell and down-sell scenarios and in contract line consolidation.


</td></tr><tr><td>

Product Support for Technology

</td><td>

-   **[Service delivery overview](https://www.servicenow.com/docs/access?context=account-360-analytics-dashboard&version=australia&pubname=australia-proactive-service-exp-workflows&ft:locale=en-US)**

Use Service Delivery Overview L1 menu to access the analytics dashboards. The Service Delivery Overview enables you to access charts and summary data on metrics such as proactive cases, account escalations, SLAs, channels used, core KPIs, and more. The Service Delivery Overview page is available in Service Operations Workspace in all releases. For CSM/FSM Configurable Workspace, it is available only in the Zurich and Australia releases.

-   **[Enhancing customer impact visibility for PSEW processes](https://www.servicenow.com/docs/access?context=enhance-customer-impact-visibility-psew-process&version=australia&pubname=australia-proactive-service-exp-workflows&ft:locale=en-US)**

Use the customer impact tab in the incident, change, and problem case records. This tab shows key metrics and insights across customer accounts, reactive cases, and install base items. It improves visibility and streamline decision-making during PSEW processes. You can also generate proactive cases and communicate with customers or consumers.


</td></tr><tr><td>

Project Portfolio Management

</td><td>

-   **[Admin role enhancements in Demand Management](https://www.servicenow.com/docs/access?context=c_DemandManagement&version=australia&pubname=australia-it-business-management&ft:locale=en-US)**
    -   Enabling all users to create ideas with a minimum read role added to the **com.snc.idea.universal\_request.copy\_fields** system property.
    -   The **com.snc.idea.universal\_request.copy\_fields** system property can be updated only by users with the idea\_admin or pps\_admin roles.
    -   Help ensure that only authenticated users have access to the bubble chart workbench through the UserIsAuthenticated condition added to the bubble chart workbench ACL \(access control list\).
-   **[Associate AI systems with demands in Demand Management](https://www.servicenow.com/docs/access?context=associate-ai-systems-with-demands&version=australia&pubname=australia-it-business-management&ft:locale=en-US)**

Add and manage AI system associations directly from the **AI Associations** tab in Demand Management. You can select impacted AI systems or create AI systems using related links directly within the demand workflow.

-   **[Summarize demand records with the demand summarization skill](https://www.servicenow.com/docs/access?context=demand-summary-demand-classic&version=australia&pubname=australia-it-business-management&ft:locale=en-US)**

Generate a concise, structured summary of any demand using the demand summarization skill through the **Summarize** button in the demand form. The skill reviews the demand fields and helps create a clear summary of the demand.

-   **[Admin role enhancements in Project Management](https://www.servicenow.com/docs/access?context=r_InstalledWithProjectManagement&version=australia&pubname=australia-it-business-management&ft:locale=en-US)**

The Project properties can be edited only by users with the pps\_admin role.

-   **[Admin role enhancements in Innovation Management](https://www.servicenow.com/docs/access?context=innovation-management-landing&version=australia&pubname=australia-it-business-management&ft:locale=en-US)**
    -   The write role has been added for the **idea.notification.sender.email** and**com.snc.innovation\_management.im\_editor\_attachment\_tag\_id** system properties.
    -   The **idea.notification.sender.email** and **com.snc.innovation\_management.im\_editor\_attachment\_tag\_id** system properties can be added or updated only by users with idea\_admin roles.

</td></tr><tr><td>

Project Workspace

</td><td>

-   **[Admin role enhancements](https://www.servicenow.com/docs/access?context=r_InstalledWithProjectManagement&version=australia&pubname=australia-it-business-management&ft:locale=en-US)**

Project properties can be edited only by users with the pps\_admin role.

-   **[Create an Asset Project Request from Project Workspace](https://www.servicenow.com/docs/access?context=create-asset-project-requests-pw&version=australia&pubname=australia-it-business-management&ft:locale=en-US)**
    -   Create and track the number of requests with project reference or requests which are created as part of an SPM project.
    -   Provide portfolio and project managers with visibility into the status of associated hardware requests.
    -   Enable project-based tracking of hardware requests, improving traceability across project plans.
    -   Help portfolio or project managers quickly understand which asset requests are tied to the project and track their current status.
-   **[Manage resources directly in Project Workspace using interoperability](https://www.servicenow.com/docs/access?context=assign-approve-unassigned-work-pw&version=australia&pubname=australia-it-business-management&ft:locale=en-US)**
    -   View assigned and unassigned work from the embedded resource board.
    -   Assign unassigned work using automatic or manual effort distribution.
    -   Preview real-time effort allocations before assigning work.
    -   Identify resource availability and overutilization using visual indicators.
    -   Approve, unapprove, or reprioritize assignments by updating the resource status directly from the resource board.
    -   Extend or update assignments, including assignments for unassigned tasks, without leaving Project Workspace.

</td></tr><tr><td>

Public Sector Digital Services

</td><td>

-   **[Investigative Case Management](https://www.servicenow.com/docs/access?context=psds-explore-inv-case-management&version=australia&pubname=australia-government-industry&ft:locale=en-US)**

Create an investigative case using Investigative Case Management. Investigative Case Management guides investigators through the process of organizing, tracking, and resolving investigations, ​developing case details,​ assigning investigators and team members​, and track evidence with logging and metadata. The following features are available as part of Investigative Case Management:

    -   Entity Management
    -   Evidence Management
With Entity Management, investigators can create investigative tasks and workflows for investigative activities with automated metadata capture \(time, source, entities, classification\)​, as well as define processing with teams and attorneys and collaborate across agencies/divisions. With Evidence Management, investigators can log and triage evidence metadata \(digital, physical, testimonial\)​ and maintain an audit trail \(Chain of Custody logging\), as well as draft, review, and create reports with supporting evidence​​.

-   **Use Now Assist for Public Sector Digital Services \(PSDS\) Skills to create case narratives and screen documents**

Complete case narratives and make refinements to investigative case records using Now Assist for PSDS Gen-AI skills. Investigators can streamline case narrative refinement byedit, adjust tone, and regenerate narrative content for clarity and completeness.

-   **Document Screening AI Skill for Social Benefits Playbook**

Validate large volumes of uploaded documents, verify information, flag issues, and highlight key details for case agents using the Social Benefits Playbook with the Document Screening Al Skill, part of Now Assist for Public Sector Digital Services \(PSDS\).

-   **[Granular configuration admin roles](https://www.servicenow.com/docs/access?context=roles-installed-with-public-sector-digital-services&version=australia&pubname=australia-government-industry&ft:locale=en-US)**

Several new granular admin roles enable admins to complete administrative configuration tasks on the Public Sector Digital Services platform without requiring the full admin role. These granular access roles enable a high-level administrator to define and assign custom roles that contain only the specific permissions a user needs, decreasing the number of users with full administrative power over the instance. For more information on granular admin roles, see [Granular admin roles](https://www.servicenow.com/docs/access?context=granular-admin-roles&version=australia&pubname=australia-platform-security&ft:locale=en-US).


</td></tr><tr><td>

Purchase Order Management

</td><td>

-   **[Create purchase order exception from Universal Request](https://www.servicenow.com/docs/access?context=create-po-exception-universal-req&version=australia&pubname=australia-source-to-pay-operations&ft:locale=en-US)**

Enable buyers to convert universal requests that were generated by the Create purchase order exception via email agentic workflow into purchase order exception records. When emails processed by the workflow lack sufficient context to be automatically converted to purchase order exception records, the workflow creates universal request records. After manual review, buyers can turn universal requests into purchase order exception records.


-   **[Create and assign a purchase order exception task](https://www.servicenow.com/docs/access?context=assign-a-poe-task-to-a-collaborator&version=australia&pubname=australia-source-to-pay-operations&ft:locale=en-US)**

Create tasks directly from a purchase order exception and assign these tasks to operational buyers or collaborators. Buyers can also track tasks directly from a purchase order exception.


-   **[Updated visualization of purchase order exceptions](https://www.servicenow.com/docs/access?context=purch-order-exception-details&version=australia&pubname=australia-source-to-pay-operations&ft:locale=en-US)**

View the expanded New activity today section on the Purchase order management landing page, reassign exceptions, and view additional details in the Exception intelligence section. Suppliers can also apply filters to purchase order line lists, enabling quick identification of relevant orders.


-   **[Automated purchase order exception creation from emails](https://www.servicenow.com/docs/access?context=convert-emails-to-exceptions&version=australia&pubname=australia-source-to-pay-operations&ft:locale=en-US)**

Convert supplier emails into purchase order exceptions when a registered supplier contact sends emails to a supplier inbox. Purchase order exceptions are created for all purchase order queries and assigned to the operational buyer. For queries unrelated to purchase order exceptions, a universal request record is created.


-   **[Identify and execute mitigation strategies for purchase order exceptions](https://www.servicenow.com/docs/access?context=mitigation-strategies-for-po-exceptions&version=australia&pubname=australia-source-to-pay-operations&ft:locale=en-US)**

Use the Define PO exception mitigation strategy agentic workflow to identify and execute mitigation strategies by analyzing delivery gaps and proposing order changes with alternative suppliers.


</td></tr><tr><td>

Quote Management

</td><td>

-   **[Consolidate quotes](https://www.servicenow.com/docs/access?context=consolidate-quotes&version=australia&pubname=australia-order-management&ft:locale=en-US)**

Maintain traceability from orders to all originating contract lines when creating orders from consolidated quotes. Additional calculated fields on order lines provide visibility into uplift values derived from consolidation rules.

-   **[Add price ramps on a quote line item](https://www.servicenow.com/docs/access?context=add-price-ramps-on-a-quote-line-item&version=australia&pubname=australia-order-management&ft:locale=en-US)**

Enable agents to create and manage custom ramp structures with flexible segment durations. Make ramp changes across the quote life cycle, including amendments and renewals, while maintaining pricing and quantity consistency across ramp segments.

-   **[Quote approvals](https://www.servicenow.com/docs/access?context=explore-advanced-approval-for-sales&version=australia&pubname=australia-order-management&ft:locale=en-US)**

Use the Advanced Approval Management to create approval workflows for end-to-end visibility and control of quote approvals.

    -   Track approval status, steps, sequencing, approvers, and comments in real time
    -   Manage quote states and edit permissions automatically as quotes move through Draft, In Review, Approved, and Rejected states
    -   Receive email notifications for approvers and requesters as approval actions are taken
    -   Configure approval conditions and sequencing across quotes, quote lines, and related entities using serial, parallel, or hybrid flows driven by business and compliance rules
    -   Preserve approval history across submissions and quote versions for a complete audit trail

-   **[Customer entities on Quote](https://www.servicenow.com/docs/access?context=quote-detail-form-fields&version=australia&pubname=australia-order-management&ft:locale=en-US)**

Capture the deal type \(Direct or Indirect deals\) and align it with different routes to market for consistency, compliance, and operational efficiency across systems and teams.


-   **[Summarize a quote using quote summarization with Now Assist](https://www.servicenow.com/docs/access?context=summarize-quote&version=australia&pubname=australia-order-management&ft:locale=en-US)**

Generate a summary of a quote to:

    -   Summarize key quote components during early customer discussions or pre‑discovery.
    -   Provide an updated view of the quote after revisions, without requiring review of multiple records.
    -   Provide a single, consolidated snapshot of all actions, tasks, and notes derived from a quote in one place.
    -   Highlight custom pricing, discounts, and negotiated changes made during the quoting process.
    -   Review the quote prior to sending it to the customer to confirm accuracy and completeness.
    -   Support internal handoffs by summarizing the quoted offer for internal teams.
For more information, see the .


</td></tr><tr><td>

RPA Hub

</td><td>

-   **[Try catch component enhancement](https://www.servicenow.com/docs/access?context=use-general-try-catch&version=australia&pubname=australia-integrate-applications&ft:locale=en-US)**

You can now precisely control the scope of Try-Catch blocks by selecting which actions \(components\) to include within exception handling and which to manage outside it. This enhancement provides better control over error handling logic and improves workflow reliability.


</td></tr><tr><td>

Recommended Actions for HRSD

</td><td>

-   **[Recommended Actions for HRSD](https://www.servicenow.com/docs/access?context=recommended-actions-hrsd&version=australia&pubname=australia-employee-service-management&ft:locale=en-US)**

Help HR agents resolve cases more quickly by listing relevant KB articles and similar cases in the context of the current case. Provide agents with an optimal action such as a suggestion to add an approval to the case if needed.


</td></tr><tr><td>

Recommended Actions for Operational Technology Service Management \(OTSM\)

</td><td>

-   **[Contextualize an external document](https://www.servicenow.com/docs/access?context=use-ai-enhanced-ra-otsm&version=australia&pubname=australia-operational-technology&ft:locale=en-US)**

Contextualize an external document to get an explanation of why the document is relevant to the selected OT incident.


</td></tr><tr><td>

ReleaseOps

</td><td>

-   **[Complete ReleaseOps guided setup](https://www.servicenow.com/docs/access?context=complete-guided-setup&version=australia&pubname=australia-application-development&ft:locale=en-US)**

Use guided setup to start using ReleaseOps quickly. You can also continue to use manual setup for more complex setup scenarios and if you need to add changes to your ReleaseOps ecosystems later.

-   **[Runbook tasks in ReleaseOps](https://www.servicenow.com/docs/access?context=runbook-tasks&version=australia&pubname=australia-application-development&ft:locale=en-US)**

Add custom, flexible, and manual activities to your assessment and release playbooks with runbook tasks, without having to adjust the structure of your playbooks from one release to the next.

-   **[Create a runbook task](https://www.servicenow.com/docs/access?context=create-runbook-task&version=australia&pubname=australia-application-development&ft:locale=en-US)**

Define the type of runbook task and when the task should occur in your ReleaseOps playbooks.

-   **[Set Automated Test Framework \(ATF\) code coverage](https://www.servicenow.com/docs/access?context=set-atf-code-coverage-threshold&version=australia&pubname=australia-application-development&ft:locale=en-US)**

Leverage Automated Test Framework \(ATF\) code coverage in ReleaseOps. ATF code coverage enables you to determine what percentage of code in a deployment request is covered by ATF test suites. You can define the threshold for ATF test failure and see what lines of code were covered by the ATF test suites.

-   **[Generate an update set description](https://www.servicenow.com/docs/access?context=generate-update-set-description&version=australia&pubname=australia-application-development&ft:locale=en-US)**

If you have a Now Assist for Creator subscription, you can generate update descriptions using the release lifecycle documentation AI agent.

-   **[Generate release notes](https://www.servicenow.com/docs/access?context=generate-release-notes&version=australia&pubname=australia-application-development&ft:locale=en-US)**

If you have a Now Assist for Creator subscription, you can generate release notes using the release lifecycle documentation AI agent.


</td></tr><tr><td>

Sales Forecasting

</td><td>

-   **[Real-time forecast rollup updates](https://www.servicenow.com/docs/access?context=using-sales-forecasting&version=australia&pubname=australia-order-management&ft:locale=en-US)**

Enhance forecast accuracy, reduce latency in pipeline views, and support faster, more informed decision‑making by triggering on‑demand recalculation for your hierarchy without having to wait for scheduled jobs.

-   **[Configurable Forecast Owner and Rollup Owner](https://www.servicenow.com/docs/access?context=configure-sales-forecasting&version=australia&pubname=australia-order-management&ft:locale=en-US)**

Improve parallel forecasting across different product lines or business structures by configuring Forecast Owner and Rollup Owner in the Forecast Model to define ownership and roll‑up responsibility.


-   **[Support for multiple configurable forecast models](https://www.servicenow.com/docs/access?context=configure-forecast-model&version=australia&pubname=australia-order-management&ft:locale=en-US)**

Define and manage forecasting rules beyond the default model by configuring up to ten forecast models to support different forecasting structures.


-   **[Multi-Period forecast rollups within a single Forecast Model](https://www.servicenow.com/docs/access?context=configure-forecast-model&version=australia&pubname=australia-order-management&ft:locale=en-US)**

Achieve better planning and strategy by configuring and managing forecasting for multiple time periods \(weekly, monthly, quarterly\) within a single forecast model for flexible data reporting.

-   **[Product Family based forecasting](https://www.servicenow.com/docs/access?context=using-sales-forecasting&version=australia&pubname=australia-order-management&ft:locale=en-US)**

Enable forecast owners to configure forecasting with product family as a secondary hierarchy with the primary hierarchy as territory or sales team. This feature enables forecast managers to submit forecasts for the product families they own and provides real-time rollups by product family and the primary hierarchy.

-   **[Enable forecasting at base forecast source](https://www.servicenow.com/docs/access?context=using-sales-forecasting&version=australia&pubname=australia-order-management&ft:locale=en-US)**

Provide forecast owners and managers with visibility into the opportunities and line items contributing to each forecast number, directly from the dashboard. Support forecast creation, submissions, and adjustments at the individual record level, such as opportunity and opportunity lines.


</td></tr><tr><td>

Sales Territory Management​

</td><td>

-   **[Sales Territory Management​ users](https://www.servicenow.com/docs/access?context=components-installed-sales-territory-management&version=australia&pubname=australia-order-management&ft:locale=en-US)**

Activate the Sales Territory Management plugin to install the Sales Territory Member role for sales execution within assigned territories, with defined ownership, accountability, and territory‑based CRM record assignment.


</td></tr><tr><td>

Sales and Order Management for Telecommunications \(SOMT\)

</td><td>

-   **[Task plan templates driven order fulfillment](https://www.servicenow.com/docs/access?context=somt-flow-action-catalog-task&version=australia&pubname=australia-telecom-media-technology&ft:locale=en-US)**

Define tasks and their dependencies using the task plan template to orchestrate the fulfillment journey for a product to standardize fulfillment processes across products.


</td></tr><tr><td>

Security Center

</td><td>

-   **Accept risk for hardening settings**

Accept risk for hardening settings that are not applicable to your organization's security requirements. When accepting risk, provide a mandatory justification and review the projected security score impact before saving your decision. The compliance status updates to **Accepted Risk** and reflects in all security score calculations. Use the **Accept Risk Settings** filter to quickly identify and manage all accepted risk items across your instance.

-   **[Granular admin role for Security Center](https://www.servicenow.com/docs/access?context=granular-sc-roles&version=australia&pubname=australia-platform-security&ft:locale=en-US)**

The granular admin role enables developers and administrators to complete administrative configuration tasks for Security Center without requiring the full admin role.

-   **[Explore Access management console](https://www.servicenow.com/docs/access?context=access-controls-console&version=australia&pubname=australia-platform-security&ft:locale=en-US)**

Use the new Access Controls console within Security Center to review and remediate access issues and misconfigurations. The Access Controls console provides enhanced visibility and control of your Access Analyzer findings, and streamlines remediation efforts by enabling you to track, prioritize, and resolve access issues by assigning tasks.

-   **Enhanced IAM Integration in Security Center**

Use the new Identity and Access Management \(IAM\) section in Security Center to access to critical IAM tools. The new section provides a comprehensive view of security metrics. This integration simplifies the administrative experience by bringing essential IAM functionality directly into Security Center, reducing the need to navigate multiple separate tools.

-   **Version-based hardening settings**

Security Center now only shows hardening settings that apply to your instance’s family version. This change helps eliminate irrelevant recommendations and provides clearer guidance and a more accurate security experience.


</td></tr><tr><td>

Security Incident Response

</td><td>

[Australia Patch 1](../quality/australia-patch-1.md)

-   **[ServiceNow product tiers](https://www.servicenow.com/docs/access?context=ai-native-sku-overview&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)**

The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets, and create your own
Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.


-   **[CrowdStrike Next-Gen SIEM integration](https://www.servicenow.com/docs/access?context=crowdstrike-next-gen-integration-secops&version=australia&pubname=australia-security-management&ft:locale=en-US)**

As a profile admin:

    -   Discover CrowdStrike Next-Gen SIEM detections that are candidates for security incidents and automate the creation of these security incidents.
    -   Create detection profiles.
    -   Map CrowdStrike Next-Gen SIEM detection and events fields to SIR security incident fields.
    -   Filter CrowdStrike Next-Gen SIEM defects.
    -   Aggregate detections to existing open security incidents so you don't have to create duplicate security incidents.
    -   Automate CrowdStrike Next-Gen SIEM detection status updates for Security Incident Response.
    -   Synchronize CrowdStrike Next-Gen SIEM detection comments with SIR Work notes.
-   **[Components installed with Security Incident Response](https://www.servicenow.com/docs/access?context=installed-with-sir&version=australia&pubname=australia-security-management&ft:locale=en-US)**

A new Profile Admin role \(sn\_si.ingestion\_profile\_admin\) provides access to configure plugins, and enables you to create, edit, delete, and manage profiles for Splunk ES, Splunk Enterprise Event Ingestion, and Microsoft Azure Sentinel integration for Security Operations application.

-   **[Add unmatched affected user for security incidents](https://www.servicenow.com/docs/access?context=view-unmatched-affected-user-for-si&version=australia&pubname=australia-security-management&ft:locale=en-US)**

The new “Security Incident Unmatched Users” table captures unmatched affected user records for security incidents, enabling analysts to identify and address discrepancies when user records don't match existing system records.

-   **[LLM-powered SIR integration builder](https://www.servicenow.com/docs/access?context=sir-integration-builder-now-assist&version=australia&pubname=australia-security-management&ft:locale=en-US)**

With the latest LLM-powered integrations on the ServiceNow AI Platform, you can create product-ready integration quickly. The LLM-powered integration builder has the following capabilities:

    -   Automatically generates integration code from a public API documentation
    -   Provides guided setup built on existing capabilities
    -   Provides easy edit and maintenance of the generated auto code
-   **[MITRE D3FEND framework](https://www.servicenow.com/docs/access?context=mitre-d3fend-framework&version=australia&pubname=australia-security-management&ft:locale=en-US)**

Security administrators can now ingest MITRE D3FEND data. Security analysts can explore MITRE ATT&amp;CK and D3FEND techniques through an interactive, node-based visualization that maps attack techniques, defense techniques, and related artifacts within a Security Incident Response record.

-   **[Preserve manual security tags and restrict removal](https://www.servicenow.com/docs/access?context=create-class-group-and-tags&version=australia&pubname=australia-security-management&ft:locale=en-US)**

Manual security tags applied by analysts are preserved when automatic tagging rules execute on security incidents, avoiding inadvertent tag removal during automated processes. Analysts can no longer manually remove security tags once applied to an incident, ensuring tag consistency throughout the incident life cycle.

-   **[Assign parent relationships to similar security incidents](https://www.servicenow.com/docs/access?context=show-related-items-for-si&version=australia&pubname=australia-security-management&ft:locale=en-US)**

Select multiple similar security incidents from the Similar Security Incidents related list and link them as children to the current security incident using the **Link as children** button.

-   **[View and update Security Incident Response system properties](https://www.servicenow.com/docs/access?context=view-update-sirw-system-properties&version=australia&pubname=australia-security-management&ft:locale=en-US)**

View and update system properties specific to the Security Incident Response workspace directly from the workspace administration settings interface.

-   **[Create quick filters for Security Incidents and Response Tasks lists](https://www.servicenow.com/docs/access?context=create-quick-filters-for-security-incidents&version=australia&pubname=australia-security-management&ft:locale=en-US)**

Enable rapid filtering of security incident lists based on predefined criteria by creating and managing quick filters for the Security incident \[sn.si.incident\] and Response tasks \[sn\_si\_task\] tables within the SIR Workspace. Filters are stored in the Quick Filters \[sn\_si\_aw\_quick\_filters\] table.

-   **[Configure auto refresh interval for security incident lists](https://www.servicenow.com/docs/access?context=configure-auto-refresh-for-security-incident-lists&version=australia&pubname=australia-security-management&ft:locale=en-US)**

Set up refreshing of the security incident list at specified intervals by using the `sn_si_incident.auto_refresh_interval` system property. The default refresh rate is five minutes.

-   **[Control external user access to security incident](https://www.servicenow.com/docs/access?context=t_CreateResponseTask&version=australia&pubname=australia-security-management&ft:locale=en-US)**

SOC users can grant read-only access to specific security incidents for defined external users through the **Access to security incident** field in the SIR workspace.

-   **[Configure default landing tab for security analysts](https://www.servicenow.com/docs/access?context=configure-default-landing-tab&version=australia&pubname=australia-security-management&ft:locale=en-US)**

Customize the default landing tab for security analysts and security managers when they open a security incident.

-   **[Compose emails from Response Tasks and Investigation tabs](https://www.servicenow.com/docs/access?context=t_CreateResponseTask&version=australia&pubname=australia-security-management&ft:locale=en-US)**

Send emails without having to switch tabs by composing them directly from the Response Tasks and the Investigation tabs of a security incident.

-   **[Configure default view for contextual menu](https://www.servicenow.com/docs/access?context=configure-default-view-for-contextual-menu&version=australia&pubname=australia-security-management&ft:locale=en-US)**

Determine whether the contextual menu panel for a security incident is expanded or collapsed by default when a security analyst opens a security incident.


</td></tr><tr><td>

Self-service and omnichannel engagement for CSM

</td><td>

-   **[Configure Web Embeddables](https://www.servicenow.com/docs/access?context=using-web-embeddables&version=australia&pubname=australia-customer-service-management&ft:locale=en-US)**

Embed ServiceNow components into any third-party website or web application to extend the ServiceNow AI Platform capabilities. You can use a library of default configurable components or create custom components.

You can configure and embed the following ServiceNow components on the third-party websites:

    -   Case list: Displays a comprehensive list of cases along with their key details.
    -   Case view: Shows a detailed view of case and case-related activities. You can display relevant playbooks when created for the case record.
    -   Case create: Displays a form to create a case to address issues related to products and services.
    -   Catalog item: Request Service Catalog items or services.
    -   Knowledge article view: Displays knowledge articles along with key details like title, content, author, view count, read time, and more. You can also rate the article and switch the display language.
    -   Data visualization: Shows a graphical representation of information from any ServiceNow AI Platform table using visual elements such as single score, pie, donut, and semi donut charts.
    -   Playbook intake: Enable your users to submit cases using the Playbook guided experience. Systematically capture case details and display stages, and activities involved in resolving the case.
    -   Catalog browse: Browse and search Service Catalog items from different catalogs and categories within a third-party website.
    -   Object list: Display records from different tables with their related actions in a list format.
-   **[Using Interaction Controls Component \(ICC\) call controls with Amazon Connect](https://www.servicenow.com/docs/access?context=amazon-connect-for-voice-calls&version=australia&pubname=australia-customer-service-management&ft:locale=en-US)**

Manage Amazon Connect calls in the CSM Configurable Workspace voice Interaction record. The integration supports inbound and outbound call flows, presence management, and transfers without switching applications.

-   **[Supervisor call monitoring](https://www.servicenow.com/docs/access?context=supervisor-monitoring-for-voice&version=australia&pubname=australia-customer-service-management&ft:locale=en-US)**

Monitor, coach, and join agent calls from the CSM Configurable Workspace without having to switch to the CCaaS desktop. All supervisor actions are automatically logged for auditing and reporting purpose.

-   **[Agent help request for voice calls](https://www.servicenow.com/docs/access?context=agent-help-request-for-voice-calls&version=australia&pubname=australia-customer-service-management&ft:locale=en-US)**

Empower agents to request supervisor assistance during calls by selecting the **Help Request** button. Agents can specify reasons why they are calling for help to provide more context to the supervisor before the supervisor responds, and receive notifications when supervisors coach or join. All help request data is captured for reporting for data-driven coaching.

-   **[Use AI to generate wrap up code and notes summary](https://www.servicenow.com/docs/access?context=ai-generated-wrap-up-codes-and-notes-summary&version=australia&pubname=australia-customer-service-management&ft:locale=en-US)**

Automatically suggest a wrap-up code and generate an interaction summary based on conversation transcripts by using Now Assist, which reduces manual documentation time and contributes to consistent record-keeping. Choose automatic or agent-initiated generation to fit your workflow.

-   **[Using the Consumer Portal](https://www.servicenow.com/docs/access?context=use-consumer-portal&version=australia&pubname=australia-customer-service-management&ft:locale=en-US)**

Support your consumers through the Consumer Portal self-service capabilities such as knowledge articles, service catalogs, case management, Virtual Agent, and others. These capabilities help reduce maintenance effort through low-code configurations on pages with configurable widgets.

-   **[Native callback features](https://www.servicenow.com/docs/access?context=contact-center-intergration-with-icc-callback&version=australia&pubname=australia-customer-service-management&ft:locale=en-US)**

Callback management enables agents to schedule callbacks on behalf of customers. The key features include:

    -   Enable agents to schedule callbacks from any interaction or case.
    -   Equip agents to reschedule or cancel callbacks from the callback record page with proper state tracking.
    -   Facilitate agents to view scheduled callbacks in the list view so they can open the individual callback record page.
    -   Enable agents to view and manage scheduled callbacks for the current interaction or case in the contextual side panel.
-   **[Email interaction feature: Wrap up of email interactions](https://www.servicenow.com/docs/access?context=using-email-interaction-page&version=australia&pubname=australia-customer-service-management&ft:locale=en-US)**

Note the following capabilities introduced for wrapping up email interactions:

    -   Introduction of wrap‑up modal for Advanced Work Assignment \(AWA\) and CCaaS‑routed email interactions with internal wrap‑up codes configurable by admins.
    -   Automatic closure of inactive interactions with system-assigned wrap-up codes in multiple scenarios:
        -   When agents create a case from an email interaction.
        -   When the wrap-up modal times out without agent submission.
        -   When customers don’t respond within the defined follow-up period.
-   **[Email interaction feature: Outbound Interaction from agent-initiated email](https://www.servicenow.com/docs/access?context=using-email-interaction-page&version=australia&pubname=australia-customer-service-management&ft:locale=en-US)**

The new capabilities for outbound interactions initiated by agents through email are:

    -   Initiate outbound email interactions from contact or consumer records by selecting email addresses or using the Compose Email UI option, opening a modeless email composer with the recipient's email address auto populated.
    -   Automatic creation of Work‑In‑Progress \(WIP\) outbound email interactions when agents initiate an email to a customer.
    -   Preserve email drafts when agents navigate away, and automatically close interactions that show no sent or received email activity and contain only unsent drafts within a rolling 30‑day period. Any agent activity on the draft resets the 30‑day window.
    -   Consolidate multiple agent‑initiated drafts into a single, unified interaction within service workflows, with ownership assigned to the sending agent. You can optionally configure the system to create separate interactions for each draft for the same contact.
    -   Configurable reminder windows for sending automated reminder emails when customers don’t respond.
    -   Customer response notifications on the ongoing tab and interaction linking in contact or consumer related lists for seamless conversation tracking.
-   **[Email interaction feature: Transfer Email Interactions routed by CCaaS](https://www.servicenow.com/docs/access?context=using-email-interaction-page&version=australia&pubname=australia-customer-service-management&ft:locale=en-US)**

Transfer CCaaS‑routed email interactions to another agent or queue, improving accurate handoff and workload distribution.


</td></tr><tr><td>

Service Catalog

</td><td>

-   **[Enable editing of catalog items by multiple users](https://www.servicenow.com/docs/access?context=set-up-cat-builder&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US)**

Enable other users, who are added to the **Secondary owner** field, to edit catalog items. To enable these users, add people to the **Secondary owner** user-criteria field in the sc\_cat\_item and sc\_cat\_item\_producer tables, enabling others to make changes to catalog items owned by another person.

-   **[Define and add stages in fulfilment step](https://www.servicenow.com/docs/access?context=configure-flow-sf-flow&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US)**

Define and add distinct stages and states in the fulfillment step when building a catalog item in Catalog Builder, enabling requesters to view the request-related current stages and their states together.

-   **[Use advanced UI policy capabilities in Catalog Builder](https://www.servicenow.com/docs/access?context=set-up-cat-builder&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US)**

Configure catalog UI policies with scripts and multiple catalog UI policy actions in the Catalog Builder to facilitate the creation of complex catalog items. With these enhancements, catalog item creators can confidently take advantage of advanced options, simplifying and speeding up the entire catalog development process.

-   **[Configure variable visibility on multi-row variable set grids](https://www.servicenow.com/docs/access?context=service-catalog&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US)**

Configure the visibility of a variable on the grid layout within a multi-row variable set \(MRVS\) for a catalog item by using the **Hide on grid** check box. By default, the check box is not selected.

-   **[Configure update set prefix](https://www.servicenow.com/docs/access?context=service-catalog&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US)**

Configure the update set prefix to set a custom name for the update set that gets generated automatically in Catalog Builder, making update sets easy to identify and track for consistency. Use the **glide.sc.cb.item.update\_set\_prefix** property to standardize update set names. By default, the property uses the value **CB\_$\{template\_name\}\_$\{item\_name\}\_$\{timestamp\}**.


</td></tr><tr><td>

Service Exchange \(formerly Service Bridge\)

</td><td>

-   **[Consumer outbound FDS](https://www.servicenow.com/docs/access?context=service-bridge-v2-explore-foundation-data-sync&version=australia&pubname=australia-service-bridge&ft:locale=en-US)**

Reduce manual effort and eliminate the need to share data externally by sharing selected foundational data types with your provider on a scheduled cadence. This data transfer supports the service life cycle by providing foundational data context for operational workflows.

-   **[Service Exchange center](https://www.servicenow.com/docs/access?context=se-se-center&version=australia&pubname=australia-service-bridge&ft:locale=en-US)**

Detect problems early, understand connection status, and resolve issues efficiently with the Service Exchange center, a centralized interface that provides real-time visibility into scan check issues, connection health and statuses, and access to all Service Exchange scan suites. Service Exchange admins can access their respective centers through the Provider and Consumer center links in the navigation menu.

-   **[Auto-onboarding](https://www.servicenow.com/docs/access?context=service-bridge-v2-register&version=australia&pubname=australia-service-bridge&ft:locale=en-US)**

Reduce onboarding complexity for consumers with automated onboarding. This feature autonomously manages onboarding workflows, establishes secure connections, synchronizes settings, and continuously monitors for errors to ensure reliable, efficient integrations with minimal manual effort.


</td></tr><tr><td>

Service Operations Workspace for ITSM

</td><td>

-   **[UI16 links to SOW redirection behavior](https://www.servicenow.com/docs/access?context=manage-admin-console-sow-itsm&version=australia&pubname=australia-it-service-management&ft:locale=en-US)**

Improve the fulfiller experience by redirecting UI16 module links such as forms and lists to the equivalent SOW experience. The UI16 module link redirection behavior is supported for all the applications in SOW when the system property **sn\_sow\_itsm\_admin.experience\_redirection\_enabled.sow** is set to `true`.

For new instances, this redirection configuration is automatically available in the base system. For upgrade instances, administrators can configure the redirection behavior from the SOW Admin Center. You can enable this feature for the UI16 links and user groups or specifically for a custom table. You can also enable this feature for specific user groups or all user groups within the custom table or applications in SOW.

-   **[Mapping granular admin roles with SOW granular roles](https://www.servicenow.com/docs/access?context=roles-in-sow&version=australia&pubname=australia-it-service-management&ft:locale=en-US)**

Using granular admin roles, provide full administrative access to the configuration and property pages for the applications in SOW without requiring the administrator \(admin\) role. These granular admin roles are mapped with ACLs and contain the corresponding existing SOW granular roles.

-   **[UX property to hide contextual side panel](https://www.servicenow.com/docs/access?context=manage-admin-console-sow-itsm&version=australia&pubname=australia-it-service-management&ft:locale=en-US)**

Use the Hide contextual side panel for specific table and tab combination option from the SOW Properties section in the SOW Admin Center to configure the hide **ContextualSidebar** UX page property. This property enables you to define the table with tab combination for which the default primary contextual side panel must be hidden, prioritizing the embedded contextual side panel within the tab instead.


</td></tr><tr><td>

Service Portal

</td><td>

-   **[Configure Service Portal Approval Configuration record](https://www.servicenow.com/docs/access?context=configure-approval-assistance-ai-agent&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US)**

The Approval assistance AI agent allows checklist generation from documents that are stored in integrated third-party cloud providers such as Microsoft SharePoint, Google Drive, or a custom internal table.

-   **[New Organization Chart widget](https://www.servicenow.com/docs/access?context=new-organization-chart-widget&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US)**

Use the Service Portal New Organization Chart widget to show additional display configurations, such as default and secondary field names, location, department, and so on, to gain visibility into employees within their organization.

-   **[Create a portal](https://www.servicenow.com/docs/access?context=create-a-portal&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US)**

Configure and apply different authentication configurations for each portal to enable different login experiences for each portal. For example, you can set an authentication method like Okta for an internal employee portal or use Microsoft Azure for an external portal.


</td></tr><tr><td>

ServiceNow AI Platform core feature

</td><td>

-   **[Granular read-only security options](https://www.servicenow.com/docs/access?context=read-only-option&version=australia&pubname=australia-platform-administration&ft:locale=en-US)**

Control the editability of read-only fields by configuring read-only options, allowing for customized behavior that balances usability and security. Read-only options provide granular control over whether read-only fields can be updated through client scripts and server-side operations. You can also test stricter read-only controls in non-production instances before implementing them in production.

-   **[Support for reference data types in Dynamic Schema](https://www.servicenow.com/docs/access?context=add-dynamic-attributes&version=australia&pubname=australia-platform-administration&ft:locale=en-US)**

Create dynamic attributes using reference data types.

-   **[Work with Dynamic Schema elements in the Workspace condition builder](https://www.servicenow.com/docs/access?context=dynamic-schema&version=australia&pubname=australia-platform-administration&ft:locale=en-US)**

Filter Workspace lists using dynamic schema elements in the condition builder.

-   **[Toggle the mail icon display](https://www.servicenow.com/docs/access?context=c_DictionaryAttributes&version=australia&pubname=australia-platform-administration&ft:locale=en-US)**

Show or hide the mail icon in email fields by configuring the hide\_email\_icon dictionary attribute.

-   **[AI indicator in forms](https://www.servicenow.com/docs/access?context=c_FormFields&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US)**

Easily identify AI involvement across the ServiceNow AI Platform® through a visual cue that identifies form fields in configurable workspace and Core UI that have been updated with AI-generated content.

-   **[Guest API access control](https://www.servicenow.com/docs/access?context=c_RESTAPI&version=australia&pubname=australia-api-reference&ft:locale=en-US)**

Manage guest access to REST and GraphQL API endpoints using path-based ACLs while maintaining separate authenticated user controls.

-   **[Granular admin roles](https://www.servicenow.com/docs/access?context=granular-admin-roles&version=australia&pubname=australia-platform-security&ft:locale=en-US)**

Grant specific permissions to developers or users who perform minor administrative tasks without granting them unrestricted access to the full admin role by reviewing and assigning available granular admin roles.

-   **[Optional trailing slash configuration](https://www.servicenow.com/docs/access?context=api-rest&version=australia&pubname=australia-api-reference&ft:locale=en-US)**

Align with external specifications and industry standards by configuring REST APIs with optional trailing slash support.

-   **[Path-based REST ACL control](https://www.servicenow.com/docs/access?context=api-rest&version=australia&pubname=australia-api-reference&ft:locale=en-US)**

Control access to REST services by creating path-based ACLs using specific HTTP method and path combinations.

-   **[Automatically generate request definitions for scripted REST API resources](https://www.servicenow.com/docs/access?context=autogenerate-api-request-definitions&version=australia&pubname=australia-api-reference&ft:locale=en-US)**

Use sample requests made to an API resource to generate request header associations, query parameter associations, and a request schema for that resource and the related scripted REST API service.

-   **[Resource-level security configuration](https://www.servicenow.com/docs/access?context=api-rest&version=australia&pubname=australia-api-reference&ft:locale=en-US)**

Enable public access or custom ACL authorization by configuring resource-level security settings.

-   **[Address field type with auto-suggestions](https://www.servicenow.com/docs/access?context=address-field-type&version=australia&pubname=australia-platform-administration&ft:locale=en-US)**

Reduce manual entry errors through a new Address field type for Core UI and Workspace forms, which provides real-time address suggestions displayed as you type.


</td></tr><tr><td>

ServiceNow IDE

</td><td>

-   **[Create and convert global applications](https://www.servicenow.com/docs/access?context=creating-applications-servicenow-ide&version=australia&pubname=australia-application-development&ft:locale=en-US)**

Create and convert applications in the global scope that are accessible to other global applications with instances on the Australia release.

-   **[Generated ServiceNow Fluent code organized in taxonomy-based directories](https://www.servicenow.com/docs/access?context=building-applications-source-code&version=australia&pubname=australia-application-development&ft:locale=en-US#application-structure)**

Configure a custom directory structure for metadata transformed into ServiceNow Fluent code with the `taxonomy` parameter in an application's `now.config.json` file. By default, generated ServiceNow Fluent files are organized in a taxonomy-based directory structure within the `fluent/generated` directory.


</td></tr><tr><td>

ServiceNow SDK

</td><td>

-   **[Create and convert global applications](https://www.servicenow.com/docs/access?context=creating-applications-servicenow-sdk&version=australia&pubname=australia-application-development&ft:locale=en-US)**

Create and convert applications in the global scope that are accessible to other global applications with instances on the Australia release.

-   **[Move application metadata from the global scope into a global application](https://www.servicenow.com/docs/access?context=servicenow-sdk-cli-commands&version=australia&pubname=australia-application-development&ft:locale=en-US)**

Transform application metadata \(XML\) in the global scope from an instance into ServiceNow Fluent source code to customize it in a local global application using the `now-sdk move` command.

-   **[Configure a default language for field labels](https://www.servicenow.com/docs/access?context=building-applications-source-code&version=australia&pubname=australia-application-development&ft:locale=en-US#application-structure)**

Configure a default language for field labels \[sys\_documentation\] in a table or column with the `tableDefaultLanguage` parameter in an application's `now.config.json` file.

-   **[Configure read-only options with the Table API](https://www.servicenow.com/docs/access?context=table-api-now-ts&version=australia&pubname=australia-application-development&ft:locale=en-US)**

Control the editability of read-only fields by configuring read-only options for a field with the readOnlyOption property in a Column object.


</td></tr><tr><td>

ServiceNow Studio

</td><td>

-   **[Build Agent in ServiceNow Studio](https://www.servicenow.com/docs/access?context=build-agent-in-servicenow-studio&version=australia&pubname=australia-application-development&ft:locale=en-US)**

Use Build Agent in ServiceNow Studio to create and edit full-stack applications conversationally.

-   **[Add UI Builder files to your apps in ServiceNow Studio](https://www.servicenow.com/docs/access?context=servicenow-studio-file-navigator-taxonomy&version=australia&pubname=australia-application-development&ft:locale=en-US)**

Build pages by adding UI Builder components, controllers, experiences, page collections, and UI interactions into your ServiceNow Studio apps.

-   **[New vibe coding documentation](https://www.servicenow.com/docs/access?context=vibe-coding-landing&version=australia&pubname=australia-application-development&ft:locale=en-US)**

Explore vibe coding, which is a natural language approach to application development in ServiceNow, with new documentation, including how to get started, when to use it, and how it fits within the broader suite of AI-powered development tools.


</td></tr><tr><td>

ServiceNow Vault

</td><td>

-   **[Guided setup for custom applications](https://www.servicenow.com/docs/access?context=use-vault-guided-setup&version=australia&pubname=australia-platform-security&ft:locale=en-US)**

Use Ask Now Assist to enhance your security posture autonomously by identifying, classifying, and protecting sensitive data in your custom applications.

-   **[Securing custom apps with Vault agents agentic workflow](https://www.servicenow.com/docs/access?context=now-assist-vault-securing-custom-apps-agents&version=australia&pubname=australia-platform-security&ft:locale=en-US)**

Propose data classifications and available protections for a custom application. When you install Now Assist for Vault, this agentic workflow is turned on by default.

-   **[Access Observer configuration agentic workflow](https://www.servicenow.com/docs/access?context=now-assist-vault-access-observer-config&version=australia&pubname=australia-platform-security&ft:locale=en-US)**

View, create, deactivate, and delete Access Observer settings for a particular field. The access observer configuration agentic workflow helps you monitor the people and processes that access data on your instance. When you install Now Assist for Vault, this agentic workflow is turned on by default.

-   **[Summarize Access Observer logs agentic workflow](https://www.servicenow.com/docs/access?context=now-assist-vault-access-observer-logs&version=australia&pubname=australia-platform-security&ft:locale=en-US)**

Review and summarize access logs for a specific field, identifying access sources, users, and their roles. For example, you can ask Now Assist to summarize access logs to view users who accessed a field, along with their roles and how they accessed the data. When you install Now Assist for Vault, this agentic workflow is turned on by default.

-   **[Field encryption with Vault module agentic workflow](https://www.servicenow.com/docs/access?context=now-assist-vault-field-encryption-module&version=australia&pubname=australia-platform-security&ft:locale=en-US)**

Encrypt specific fields and configure secure access to users with designated roles using the field encryption with Vault module agentic workflow. When you install Now Assist for Vault, this agentic workflow is turned on by default.


-   **[Sensitive data monitoring in AI Insights](https://www.servicenow.com/docs/access?context=vault-tools&version=australia&pubname=australia-platform-security&ft:locale=en-US)**

Identify unprotected sensitive data across your configured tables using the AI Insights section in the Vault console dashboard. View users entering sensitive data in unprotected columns and channels, grouped by sensitive data patterns. This information can further be used to prioritize protection efforts.

-   **[Guided setup for custom applications](https://www.servicenow.com/docs/access?context=use-vault-guided-setup&version=australia&pubname=australia-platform-security&ft:locale=en-US)**

Autoclassify and protect the occurrences of sensitive data within your custom applications using guided setup for Vault. This flow helps you to quickly start using Vault capabilities in your own applications.


</td></tr><tr><td>

Sidebar

</td><td>

-   **[Sidebar](https://www.servicenow.com/docs/access?context=sidebar-landing&version=australia&pubname=australia-conversational-interfaces&ft:locale=en-US)**

Customize the subject title for Sidebar discussions by replacing the default short description with any field from the record.

-   **[Sidebar](https://www.servicenow.com/docs/access?context=sidebar-landing&version=australia&pubname=australia-conversational-interfaces&ft:locale=en-US)**

Move and resize the Sidebar chat window using the dynamic window framework.

-   **[Sidebar](https://www.servicenow.com/docs/access?context=sidebar-landing&version=australia&pubname=australia-conversational-interfaces&ft:locale=en-US)**

Create a standalone Sidebar discussion that is not tied to a specific record.


</td></tr><tr><td>

Smart Assessment Engine

</td><td>

-   **[Collaboration in assessments](https://www.servicenow.com/docs/access?context=collaboration-in-assessments&version=australia&pubname=australia-governance-risk-compliance&ft:locale=en-US)**

Starting with version 22.0.0, use granular delegation as a primary owner to assign individual assessment sections to SMEs. Respondents can view the entire assessment for context but can edit only their assigned sections. Monitor overall assessment progress and maintain final review and submission capabilities.

-   **[Quick edit for published templates](https://www.servicenow.com/docs/access?context=quick-edit-for-published-templates&version=australia&pubname=australia-governance-risk-compliance&ft:locale=en-US)**

Starting with version 22.0.0, edit published templates inline as a template manager, including edits to the titles, descriptions, and reader roles.


</td></tr><tr><td>

Software Asset Management

</td><td>

[Australia Patch 1](../quality/australia-patch-1.md)

-   **[ServiceNow product tiers](https://www.servicenow.com/docs/access?context=ai-native-sku-overview&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)**

The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets, and create your own
Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.

-   **[Improve accuracy and productivity by extracting licensing data from contracts and generating software entitlements](https://www.servicenow.com/docs/access?context=extract-entitlements-from-contracts-now-assist-sam&version=australia&pubname=australia-it-asset-management&ft:locale=en-US)**

Leverage generative AI to upload contract documents and automatically extract licensing data, generating software entitlements. You can review and refine the entitlements prior to finalization. The entitlements are created and linked to the contract records, ensuring a streamlined and accurate process.

-   **[Benefit with an integrated troubleshooting experience for SaaS applications by resolving common issues using automated guidance](https://www.servicenow.com/docs/access?context=troubleshooting-saas-now-assist-sam&version=australia&pubname=australia-it-asset-management&ft:locale=en-US)**

Use generative AI to troubleshoot SaaS integrations with automated guidance and recommendations. By following the resolution guidance, you can significantly reduce downtime, lower the mean time to resolution \(MTTR\), and resolve complex SaaS issues without deep technical intervention.

-   **[Use an agentic workflow to automate Microsoft 365 license assignment to users to improve efficiency](https://www.servicenow.com/docs/access?context=now-assist-sam-fulfill-sw-asset-requests-workflow&version=australia&pubname=australia-it-asset-management&ft:locale=en-US)**

Use AI agents to assign Microsoft 365 licenses automatically to users on the Microsoft 365 Admin Center without manual intervention. The AI agent analyzes whether there are available licenses and automatically assigns those licenses to the Microsoft 365 Admin Center, ensuring accuracy and compliance.

-   **[Software Asset Management integration with Contract Management Pro](https://www.servicenow.com/docs/access?context=sam-integration-cmpro&version=australia&pubname=australia-it-asset-management&ft:locale=en-US)**

Gain centralized visibility into software contract life cycles and streamline contract management by extracting key metadata and obligations from an uploaded signed contract document using the agentic AI workflow. Additionally, you can optimize costs through proactive tracking of contract renewals, expirations, and contractual obligations by integrating Software Asset Management with the Contract Management Pro application. Note that only Software Asset Management Enterprise users can leverage this functionality.


-   **[Improve user activity tracking with the GitHub integration](https://www.servicenow.com/docs/access?context=integrate-with-github&version=australia&pubname=australia-it-asset-management&ft:locale=en-US)**

Achieve more accurate user activity data and improved license reclamation for low or no-activity subscriptions by leveraging the enhanced GitHub integration for broader event coverage and extended retention.

-   **[Enhanced integration with OpenLM for tracking subscription and consumption licenses](https://www.servicenow.com/docs/access?context=concurrent-licenses&version=australia&pubname=australia-it-asset-management&ft:locale=en-US)**

Gain improved visibility into engineering application licenses across subscription-based and consumption models with the OpenLM integration. This capability provides support for named user allocation and usage tracking. Additionally, you can better monitor compliance risks and note denial patterns through actionable insights into automated processes and dashboards.

-   **[Leverage machine learning \(ML\) normalization for managing your software assets in protected government environments](https://www.servicenow.com/docs/access?context=ml-learning-sam&version=australia&pubname=australia-it-asset-management&ft:locale=en-US)**

Extend ML normalization capabilities to regulated markets for ServiceNow Protected Platform \(SPP\) in Singapore \(SG\) and Australia \(AU\).

-   **[Enhance the security of SAP ABAP on-premise integration using OAuth 2.0 authentication](https://www.servicenow.com/docs/access?context=add-sap-connection&version=australia&pubname=australia-it-asset-management&ft:locale=en-US)**

Benefit from enhanced OAuth 2.0 authentication for your SAP ABAP on-premise integrations with improved security. This capability provides a more secure, compliant, and future-proof method for integrating the Software Asset Management application with your SAP systems.

-   **[Improve your license management experience through the enhanced support for Oracle WebLogic Suite licensing](https://www.servicenow.com/docs/access?context=oracle-licensing-cloud-environments&version=australia&pubname=australia-it-asset-management&ft:locale=en-US)**

Access flexible licensing options that align with different deployment models and usage patterns through comprehensive license management with support for the Oracle WebLogic Suite for both Per Processor and Named User Plus \(NUP\) metrics. The enhanced support now covers the entire WebLogic product family, including the flagship Suite edition.

-   **[Improve software normalization outcomes with expanded pattern-based normalization rules rule](https://www.servicenow.com/docs/access?context=c_SAMDiscovery&version=australia&pubname=australia-it-asset-management&ft:locale=en-US)**

Streamline the software model discovery process by leveraging the expanded pattern-based normalization rule, which eliminates the need to manually update or create new normalization rules for every minor variation in software discovery models. This rule automatically recognizes and matches diverse patterns and variations in software model data. As a result, discovered publisher, product, version, and edition values are seamlessly aligned with the ServiceNow® repository.

-   **[Enhanced SQL server enterprise edition license compliance to support Server/CAL licensing model](https://www.servicenow.com/docs/access?context=mapping-ms-license-metrics&version=australia&pubname=australia-it-asset-management&ft:locale=en-US)**

Optimize licensing for legacy Microsoft SQL Server Enterprise Edition licenses under the Server+CAL licensing model with Software Assurance \(SA\) by using the enhanced licensing rule. A single server license can cover up to four virtual machines, provided that the combined processing power for these VMs does not exceed twenty hardware threads or cores at any given time.

-   **[Generate optimal software lifecycle reports using a guided playbook that ensures adherence to compliance and audit requirements.](https://www.servicenow.com/docs/access?context=guidedplaybook-sw-lifecycle-reports&version=australia&pubname=australia-it-asset-management&ft:locale=en-US)**

Simplify the creation of optimal software life-cycle reports through a guided playbook that assists in defining report scope, identifying gaps, and performing corrective actions. The playbook also integrates with the success portal, enabling you to establish and monitor success metrics, organize tasks and activities, and effectively track progress toward your objectives.

-   **[Streamline license management for Microsoft server product Installations and license usage via a single report](https://www.servicenow.com/docs/access?context=device-license-consumption-report&version=australia&pubname=australia-it-asset-management&ft:locale=en-US)**

Gain insights to a unified report for all Microsoft server product installations and license usage across license metrics. The Microsoft Server Infrastructure and License consumption report consolidates infrastructure data per device along with license usage and exemptions. Get detailed justifications for exemptions such as unlicensed or ignored installations, making it easier to monitor, analyze, and optimize your IT resources.


</td></tr><tr><td>

Source-to-Pay Operations Integrations

</td><td>

-   **[Source-to-Pay integration with Oracle Financial Cloud](https://www.servicenow.com/docs/access?context=source-to-pay-oracle-fin-cloud-integration&version=australia&pubname=australia-source-to-pay-operations&ft:locale=en-US)**
    -   You can use this integration to perform Integration Hub actions for invoices, cost centers, product models, payment terms, purchasing organizations, departments, GL accounts, currencies, FX rates, invoice payment details, suppliers, plant addresses, and legal entities.
    -   You can also fetch currencies, GL accounts, legal entities, and payment terms information from Oracle Financial Cloud.

</td></tr><tr><td>

Sourcing and Procurement Operations

</td><td>

-   **[Multi-currency support in Shopping Hub](https://www.servicenow.com/docs/access?context=sh-multicurrency-overview&version=australia&pubname=australia-source-to-pay-operations&ft:locale=en-US)**

Enable multi-currency display across approval-related views, including To-Dos, tasks, email notifications, and the Bundles page. Currency values are shown in both the approver’s local currency and the original supplier currency where applicable. The local currency is displayed as the primary value, with the original currency shown as a secondary reference. This display format provides consistent currency visibility for approvers during review.

-   **[Decimal quantity support for service-based purchases in Shopping Hub](https://www.servicenow.com/docs/access?context=decimal-support-services&version=australia&pubname=australia-source-to-pay-operations&ft:locale=en-US)**

Enable requesters to enter and edit decimal quantities for service-based purchase requisitions and purchase orders without validation errors. Decimal quantities are supported only for services to maintain data integrity. Decimal quantities for goods are not supported and return a clear validation message. This validation logic is consistent across Shopping Hub and Employee Center.

-   **[Automatically assign categories during SR and PR creation](https://www.servicenow.com/docs/access?context=automatically-assign-categories&version=australia&pubname=australia-source-to-pay-operations&ft:locale=en-US)**

Automatically classify service requests, purchase requisitions, and purchase orders into the correct spend categories using the Spend categorization agent. This classification process reduces manual classification effort and improves consistency across procurement workflows.

-   **[Purchase on behalf of another user in Shopping Hub](https://www.servicenow.com/docs/access?context=purchase-on-behalf-sh&version=australia&pubname=australia-source-to-pay-operations&ft:locale=en-US)**

Enable users to purchase on behalf of others without requiring delegate configuration in Shopping Hub. Users can manage individuals they are authorized to purchase for, directly within the buying experience. Purchases made on behalf of others are visible through filtering by business owner in the My Purchases view.


</td></tr><tr><td>

Strategic Planning

</td><td>

-   **[Next Experience for Demand Management](https://www.servicenow.com/docs/access?context=demand-workspace&version=australia&pubname=australia-it-business-management&ft:locale=en-US)**

Next Experience for Demand Management delivers a unified experience for managing strategic and operational demands in Strategic Planning. This Next Experience interface consolidates demand creation, assessment, collaboration, and conversion in one place, eliminating context switching and reducing reliance on the classic Demand Workbench.

-   **[Create and manage demands in Next Experience for Demand Management](https://www.servicenow.com/docs/access?context=use-demands-dmnd-wpc&version=australia&pubname=australia-it-business-management&ft:locale=en-US)**
    -   Create and manage a demand in Next Experience for Demand Management using guided tabs that help you define alignment, estimate costs, and confirm readiness as you build out the demand.
    -   Collaborate on demands through Docs, with execution and planning synced.
    -   View, add, and edit cost plans and budgeting details using related lists.
-   **[Use Playbooks in Next Experience for Demand Management](https://www.servicenow.com/docs/access?context=use-playbooks-in-dw&version=australia&pubname=australia-it-business-management&ft:locale=en-US)**

Help teams manage demands with greater structure and consistency using Playbook in Next Experience for Demand Management.

Playbooks enable you to define multiple governance processes across the organization using a low‑code/no‑code configuration experience. Create clear stages and guided activities from demand intake to completion by using a default playbook or creating a custom playbook to support your organization’s multiple demand management processes.

-   **[Associate AI systems with demands in Next Experience for Demand Management](https://www.servicenow.com/docs/access?context=use-playbooks-in-dw&version=australia&pubname=australia-it-business-management&ft:locale=en-US)**

Use a playbook activity in Next Experience for Demand Management to associate AI systems with a demand. You can link impacted systems and add new ones directly within the demand workflow.

-   **[Summarize demands with demand summarization skill](https://www.servicenow.com/docs/access?context=summarize-demand-in-demand-workspace&version=australia&pubname=australia-it-business-management&ft:locale=en-US)**

Generate a concise, structured summary of any demand using the demand summarization skill through the **Summarize** button in the demand form. The skill reviews the demand fields and helps create a clear summary of the demand.

-   **[Strategy and Goals](https://www.servicenow.com/docs/access?context=strategy-goals-landing-page&version=australia&pubname=australia-it-business-management&ft:locale=en-US)**

Use boards in Strategy and Goals to organize and manage your organization’s strategic priorities and objectives. A board is a collection of strategic plans, priorities, objectives, and key results based on your selected filter criteria—helping you stay focused and manage them effectively.

    -   Managing boards:
        -   Create boards step by step, choosing whether to base them on strategic plans, priorities, goals, or both. Define what items to display using advanced filter conditions.
        -   Build boards tailored to specific goals by entity type and entity, ensuring focus on the goals that matter most.
        -   Share boards with stakeholders to align efforts and drive shared outcomes.
        -   Add boards to your favorites for faster navigation.
    -   Managing strategy and goals using boards:
        -   Create and organize strategic plans, strategic priorities, goals, and key results in a single, focused view.
        -   Associate work or planning items with goals or targets to align your current or future work with your strategic priorities, helping your team achieve goals and targets efficiently.
        -   As the goal or process owner, send notifications to target owners or contributors to ensure timely updates of target actuals.
        -   Target owners and contributors receive reminder notifications for check-in updates before the due date.
        -   With Now Assist for Strategic Portfolio Management \(SPM\), generate measurable targets for your goals to reduce the effort of defining clear success criteria, and gain actionable insights to identify at‑risk goals, assess forecasted status, and act on AI‑driven recommendations.
-   **[Portfolio plan goals enhancements](https://www.servicenow.com/docs/access?context=managing-goals-in-alignment-planner-workspace&version=australia&pubname=australia-it-business-management&ft:locale=en-US)**
    -   Owners and contributors are notified when they’re mentioned in a goal, target, or when comments are added.
    -   Define targets across multiple organizational levels with the Assigned entity field in the target form. This enables targets created at higher levels \(for example, Company\) to be directly assigned to lower levels \(for example, Business Unit, Department\), eliminating redundant subgoal creation, and streamlining overall goal management.
-   **[Portfolio plan enhancements](https://www.servicenow.com/docs/access?context=create-portfolio-plans-in-alignment-planner-workspace&version=australia&pubname=australia-it-business-management&ft:locale=en-US)**
    -   Visualize planning items in lanes with the new Kanban tab in the Planning page and access the Hierarchy tab directly from the same location. These tabs replace the previous access point in the Prioritization tab, offering a more streamlined way to view and manage planning items.
    -   Save filter views specific to the Kanban tab and the Hierarchy tab without affecting views in the Prioritization tab.
    -   View planning items in the new Hierarchy tab on the Planning page, now sorted using global rank when available. Drag and drop is supported for lowest‑level items, enabling you to rerank them within their groups.
-   **[Hierarchy tab for EAP teams](https://www.servicenow.com/docs/access?context=eap-hierarchy-tab&version=australia&pubname=australia-it-business-management&ft:locale=en-US)**

Gain visibility into how your work connects to broader organizational goals by viewing the complete work item hierarchy directly in the EAP workspace. Expand any epic to see its capabilities, features, and stories across Solution Trains, ARTs, and Agile Teams without switching between multiple screens or running separate reports.

Customize your view by selecting which columns appear in the hierarchy grid and adjusting column widths to match your workflow. Your column preferences persist across sessions, so your configured view is ready each time you return.

-   **[Open EAP work items in new browser tab](https://www.servicenow.com/docs/access?context=using-eap&version=australia&pubname=australia-it-business-management&ft:locale=en-US)**

Open work items from the EAP Backlog and Hierarchy pages in a new browser tab, so you never lose your context. Right-click any work item, or use the item options menu, to open its full details in a separate tab. This feature lets you review and compare multiple work items side by side without losing your current view.

-   **[Admin role enhancements in Feedback](https://www.servicenow.com/docs/access?context=components-installed-with-product-feedback&version=australia&pubname=australia-it-business-management&ft:locale=en-US)**

The read role sn\_align\_core.pf\_read and write role sn\_align\_core.apw\_admin are added to the following system properties in Feedback and Product idea:

    -   sn\_apw\_advanced.product\_feedback\_allowed\_non\_planning\_items\_for\_link\_item
    -   sn\_apw\_advanced.product\_feedback\_product\_idea\_filters
    -   sn\_apw\_advanced.product\_feedback\_feedback\_filters
    -   sn\_apw\_advanced.feedback.idea\_feedback\_queue\_address
-   **[Financials for planning items](https://www.servicenow.com/docs/access?context=using-financials-spw&version=australia&pubname=australia-it-business-management&ft:locale=en-US)**
    -   Migration of financial baselines:
        -   Migrate the financial baselines of projects, which includes investment currency support.
        -   While migration, financial baselines will now include actuals, costs, benefits, and budget values from the project currency to the investment currency.
    -   Streamlined currency fields while using multicurrency:
        -   New and existing customers will now see only investment currency fields in demand and project records.
        -   Planned costs, actual costs, planned benefits, actual benefits, and budget fields are included in the financial baselines.

</td></tr><tr><td>

Subscription Management

</td><td>

-   **[Support for domain separation](https://www.servicenow.com/docs/access?context=domain-separation-subscription-mgmt&version=australia&pubname=australia-platform-administration&ft:locale=en-US)**

View and filter subscribers by domain for user-based subscriptions and view Now Assist usage by domain.

-   **[Monitor Workflow Data Fabric usage](https://www.servicenow.com/docs/access?context=monitoring-wdf-capability-use&version=australia&pubname=australia-platform-administration&ft:locale=en-US)**

Monitor and track Workflow Data Fabric capability usage and view the relative token use rate of each capability.


</td></tr><tr><td>

Supplier Lifecycle Operations

</td><td>

-   **[Smart Assessments](https://www.servicenow.com/docs/access?context=slo-campaign-mgmt&version=australia&pubname=australia-source-to-pay-operations&ft:locale=en-US)**

Supplier managers can use the segmentation rules and assessment templates to create smart assessments in bulk for users. Smart assessments provide a survey-like experience with enhanced UI capabilities for both internal and external users. This feature utilizes the capabilities of the Smart Assessment Engine application.

-   **[Emails view for supplier managers in the Source-to-Pay Workspace](https://www.servicenow.com/docs/access?context=enabling-emails-view-for-contacts&version=australia&pubname=australia-source-to-pay-operations&ft:locale=en-US)**

Supplier managers can access their emails within the Source-to-Pay Workspace from the **Emails** tab in the case, task, and supplier details pages respectively. Email actions are reflected and incomplete email errors are handled. Email-summarization is available from the workspace for tasks and cases only.

Supplier contacts receive the emails and they can perform the assigned tasks directly via email without logging in to the Supplier Collaboration Portal.

Internal stakeholders receive the emails and they can perform the assigned tasks directly via email without logging in to the Source-to-Pay Workspace.

-   **[AI driven supplier onboarding using Now Assist for SLO](https://www.servicenow.com/docs/access?context=supplier-onboarding-agentic-workflow&version=australia&pubname=australia-source-to-pay-operations&ft:locale=en-US)**

Use theAI driven supplier onboarding workflow to automate data validation, duplicate checking, task generation, and supplier communication. Key enhancements include:

    -   Extract banking information from uploaded documents to reduce information mismatch.
    -   Use the document strategy generator AI agent to generate a customized onboarding task list using all published knowledge base articles.
    -   View a list of AI-suggested suppliers while reviewing supplier onboarding requests initiated through sourcing requests.
    -   Supplier relationship managers can manually approve or reject supplier onboarding requests.
    -   Resolve duplicate supplier onboarding requests from the Now Assist panel by updating the supplier legal name, contact email, or both.
-   **[Automate supplier case creation from emails](https://www.servicenow.com/docs/access?context=automated-supplier-case-creation-from-emails&version=australia&pubname=australia-source-to-pay-operations&ft:locale=en-US)**

Convert supplier emails into cases automatically when registered supplier contacts send emails to a supplier inbox. Supplier cases are created for all SLO related queries and assigned to the supplier relationship manager. For queries unrelated to SLO, a universal request is created for resolution.

-   **[Summarize supplier performance in Source-to-Pay Workspace](https://www.servicenow.com/docs/access?context=summarize-supp-perf&version=australia&pubname=australia-source-to-pay-operations&ft:locale=en-US)**

Generate comprehensive supplier performance summaries, including performance data, trends, and actionable insights, using the supplier performance summarization skill.

-   **[Analyze sentiments in supplier cases](https://www.servicenow.com/docs/access?context=slo-analyze-sentiments&version=australia&pubname=australia-source-to-pay-operations&ft:locale=en-US)**

Use the sentiment analysis skill to analyze supplier case fields and determine the tone or sentiment of the fulfiller.

-   **[Generate an email response for supplier cases](https://www.servicenow.com/docs/access?context=generate-email-response-for-supplier-case&version=australia&pubname=australia-source-to-pay-operations&ft:locale=en-US)**

Use the email response skill to analyze the supplier case details and generate professional email response regardless of the record type using past email responses, KB articles, and related tasks.


</td></tr><tr><td>

Synthetic monitoring

</td><td>

-   **Create monitors for existing incidents**

Use existing incidents to create monitors and proactively reduce re-occurrence of incidents.

-   **Migrate existing monitors in bulk using APIs**

Use REST APIs to streamline migration and automation of third‑party synthetic monitors for easier scaling and reduced manual work.


</td></tr><tr><td>

Telecommunications Customer 360

</td><td>

-   **[Customer information](https://www.servicenow.com/docs/access?context=c360-home-page&version=australia&pubname=australia-telecom-media-technology&ft:locale=en-US)**

View customer account, contact, or consumer information including contact details, location, and recent interaction summary for efficient service delivery.


-   **[Interaction history](https://www.servicenow.com/docs/access?context=c360-inter-history-card&version=australia&pubname=australia-telecom-media-technology&ft:locale=en-US)**

Track customer interactions over time with date range filtering. View chronological history of customer engagements to understand previous communication context.


-   **[Trend charts](https://www.servicenow.com/docs/access?context=c360-data-visual-card&version=australia&pubname=australia-telecom-media-technology&ft:locale=en-US)**

Monitor key customer metrics through visual charts including NPS and CSAT scores with target comparisons and trend lines. View last updated timestamps for each metric.

-   **[Billing](https://www.servicenow.com/docs/access?context=c360-billing-card&version=australia&pubname=australia-telecom-media-technology&ft:locale=en-US)**

Review customer billing information and invoices for the selected billing account. Search and filter billing records to quickly locate specific invoice details.


-   **[Products](https://www.servicenow.com/docs/access?context=c360-products-card&version=australia&pubname=australia-telecom-media-technology&ft:locale=en-US)**

Identify active products and services associated with the customer account. View counts of related cases, service problem cases, incidents, and test results for each product to understand product-specific issues.

-   **[Cases, tasks, and orders](https://www.servicenow.com/docs/access?context=c360-tasks-card&version=australia&pubname=australia-telecom-media-technology&ft:locale=en-US)**

Manage multiple task types including service problem cases, cases, customer orders, work orders, complaint cases, and invoice cases in a unified view. View details such as case numbers, descriptions, state, sold products, and priority levels across all task records.


</td></tr><tr><td>

Telecommunications Network Inventory

</td><td>

-   **[Remote Hands Request Management](https://www.servicenow.com/docs/access?context=remote-hands-request-management&version=australia&pubname=australia-telecom-network-inventory&ft:locale=en-US)**

Enable your customers to request services such as power usage enquiries, equipment installation, equipment restarts, and more by connecting with onsite operations agents at your facility. Securely store your customer requests in the Remote Hands Case table, with role-based access controls. View an auto-generated summary of your requests for quick reference.


</td></tr><tr><td>

Telecommunications Service Operations Management \(TSOM\)

</td><td>

-   ****

Gain full visibility into your SD-WAN landscape with automated discovery and mapping for Cisco Meraki and Fortinet FortiManager.


</td></tr><tr><td>

Theme Builder

</td><td>

-   **[AI-powered color palette theme creation](https://www.servicenow.com/docs/access?context=tb-create-a-theme-ai&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US)**

Use AI to generate themes from brand images, preview multiple options, and refine results all within the updated Create a theme wizard. If you prefer, you can skip the AI step and continue creating your theme manually using the existing workflow. This feature requires Now Assist for Creator.

-   **[Generate themes using Now Assist](https://www.servicenow.com/docs/access?context=create-theme-now-assist&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US)**

Leverage Now Assist to generate themes based on your brand image. After generating a theme, navigate to Theme Builder to publish and apply additional styling. This feature requires Now Assist for Creator and a theme creation workflow enabled in AI Agent Studio.

-   **[ServiceNow product tiers](https://www.servicenow.com/docs/access?context=ai-native-sku-overview&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)**

The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets, and create your own
Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.


-   **[Override default icons for a fully branded experience](https://www.servicenow.com/docs/access?context=tb-icon-illustrations&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US)**

View and manage your theme’s icon library in Theme Builder, including uploading custom assets to replace default icons. Icons support size variants, outline and fill styles, and dynamic color adjustments and integrate with embeddable components.

-   **[Control typography at the component category level](https://www.servicenow.com/docs/access?context=assign-fonts-by-category&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US)**

Assign fonts to individual component categories to create clearer visual distinction across your interface.

-   **[Flexible Font size control](https://www.servicenow.com/docs/access?context=edit-font-size&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US)**

Fine-tune font sizes across component categories for a polished, consistent look. Use font‑size controls to tailor default or custom fonts to your brand needs. Applies across Next Experience and embeddable components, ensuring a consistent brand look even on external sites.


</td></tr><tr><td>

Third-party Risk Management

</td><td>

-   **[Generate aggregate regulatory reports in local currencies](https://www.servicenow.com/docs/access?context=tprm-dora-currency-aggregation&version=australia&pubname=australia-governance-risk-compliance&ft:locale=en-US)**

After upgrading the Digital Resilience Third-party Information Register application to version 22.0.3, third‑party risk \(TPR\) managers  \[sn\_vdr\_risk\_asmt.vendor\_manager\] can standardize annual expense values during Register of Information report generation by enabling currency conversion and third‑party total expense aggregation. To support this process, the generated reporting package includes summary and detail reports that indicate successful conversions, aggregation results, and any skipped providers.

-   **[Centralized repository for TPRM SAE templates](https://www.servicenow.com/docs/access?context=tprm-integrating-ucm&version=australia&pubname=australia-governance-risk-compliance&ft:locale=en-US)**

After upgrading to version 22.0.2 and installing the Unified Content Management application, TPR managers \[sn\_vdr\_risk\_asmt.vendor\_risk\_manager\] can help ensure consistent and comprehensive assessments by activating and updating ready‑to‑use Smart Assessment Engine questionnaire templates through a single, managed repository in the Vendor Management Workspace.


-   **[Generate issue recommendations for TPRM](https://www.servicenow.com/docs/access?context=create-recommendation-tprm-issue&version=australia&pubname=australia-governance-risk-compliance&ft:locale=en-US)**

After upgrading to version 22.0.8 if you have the third‑party assessment reviewer role \[sn\_vdr\_risk\_asmt.vendor\_assessment\_reviewer\] and have installed the Now Assist for Third-party Risk Management \(TPRM\) application, you can use generative AI to automatically identify and recommend issues based on assessment responses. The TPRM issue management recommendation skill recommends issues with rationalized summaries. Recommended issues are presented for review and are created as standard TPRM issues only after user confirmation.


</td></tr><tr><td>

Threat Intelligence Security Center

</td><td>

-   **[Have I Been Pwned integration](https://www.servicenow.com/docs/access?context=tisc-hibp-integration&version=australia&pubname=australia-security-management&ft:locale=en-US)**

Added support in TISC for Have I been pwned? \(HIBP\) observable enrichment, enabling analysts to identify whether observables have been exposed in known data breaches instances.


-   **[Configure Tagging Rules in TISC](https://www.servicenow.com/docs/access?context=tisc-tag-rules&version=australia&pubname=australia-security-management&ft:locale=en-US)**

Introduced automated tagging of RSS feed records using configurable tagging rules to apply tags and taxonomies.


-   **[Create a CWE record](https://www.servicenow.com/docs/access?context=tisc-create-cwe-record&version=australia&pubname=australia-security-management&ft:locale=en-US)**

Introduced CWEs as related entities with support for relationship linking.


-   **[Create Remediations](https://www.servicenow.com/docs/access?context=tisc-create-remediation-record&version=australia&pubname=australia-security-management&ft:locale=en-US)**

Introduced remediations as related entities with support for relationship linking and added support for managing remediations.


-   **[Create a Product](https://www.servicenow.com/docs/access?context=tisc-create-product&version=australia&pubname=australia-security-management&ft:locale=en-US)**

Introduced products as related entities with support for relationship linking.


-   **[Create a Vendor to a Vulnerability](https://www.servicenow.com/docs/access?context=tisc-add-vendor-to-vul&version=australia&pubname=australia-security-management&ft:locale=en-US)**

Associated vendors as related entities with support for relationship linking.


-   **[Automated creation of zero day vulnerability](https://www.servicenow.com/docs/access?context=tisc-zero-day-vuln-scenario&version=australia&pubname=australia-security-management&ft:locale=en-US)**

Automatically generate zero day vulnerability records from flagged RSS feeds with extracted and linked CPE, CWE, and CVE details for enhanced threat analysis. The catalog now includes the RSS feed for **Google Project Zero**, enabling real-time detection of emerging threats.


-   **[Create Vulnerability Assessment from a Vulnerability](https://www.servicenow.com/docs/access?context=tisc-vul-assess&version=australia&pubname=australia-security-management&ft:locale=en-US)**

Initiate vulnerability assessments directly from identified issues for faster risk evaluation. Sample workflows and flow actions are included to automate the assessment process.


-   **[Create Security Incident from a Vulnerability Record](https://www.servicenow.com/docs/access?context=tisc-create-security-incident&version=australia&pubname=australia-security-management&ft:locale=en-US)**

Create security incident records directly from detected vulnerabilities to expedite incident response and streamline threat management workflows.


-   **[Enable security incidents for vulnerabilities](https://www.servicenow.com/docs/access?context=tisc-view-security-context&version=australia&pubname=australia-security-management&ft:locale=en-US)**

View vulnerabilities and related intelligence in the **TISC Context** tab of Security Incident Response Workspace, allowing analysts to quickly access risk data during investigations without navigating to separate records.


</td></tr><tr><td>

UI Builder

</td><td>

-   **[Create event-driven UI interactions](https://www.servicenow.com/docs/access?context=uib-ui-interactions&version=australia&pubname=australia-application-development&ft:locale=en-US)**

Trigger UI interactions directly from events in UI Builder, allowing you to link event-driven behavior to reusable interaction logic with the following benefits:

    -   Define an interaction once and apply it across multiple events and pages so UI components such as modals don't have to be associated directly with the page anymore.
    -   Connect events to interactions without additional scripting.
    -   Centralize logic for consistent updates and fewer errors.
    -   Previously, Declarative Actions using UXF Client Actions required manual wiring on each page leading to complexity and upgrade risks. UI Interactions replace this with reusable, declarative event mapping.

</td></tr><tr><td>

Universal Request

</td><td>

-   **[Inter-department communication](https://www.servicenow.com/docs/access?context=ur-create-universal-request-record&version=australia&pubname=australia-employee-service-management&ft:locale=en-US)**

Improve inter-departmental communication by enabling agents to effectively collaborate on associated tickets using the **Sidebar discussions** and **Discuss** options. Control agent participation through restricted lists and apply access permissions consistently across associated tickets.

-   **[Universal Request Router agentic workflow](https://www.servicenow.com/docs/access?context=agentic-flow-ur&version=australia&pubname=australia-employee-service-management&ft:locale=en-US)**

Enable employees to request help with services that are hard to locate in the catalog listing or need support from multiple departments.


</td></tr><tr><td>

Upgrade Console

</td><td>

-   **[App version compatibility support](https://www.servicenow.com/docs/access?context=um-pre-upgrade-activities&version=australia&pubname=australia-platform-administration&ft:locale=en-US)**

Update the Now Assist suite to manage application version compatibility by automatically updating all related applications to compatible versions when you upgrade an application in the compatibility matrix.

-   **[ATF Troubleshooting agent access](https://www.servicenow.com/docs/access?context=um-post-upgrade-activities&version=australia&pubname=australia-platform-administration&ft:locale=en-US)**

You can now troubleshoot failed tests by accessing the ATF troubleshooting agent from the Conduct post-testing step in the post-upgrade activities of a non-production instance.


</td></tr><tr><td>

Usage Insights

</td><td>

-   **[Creating custom events](https://www.servicenow.com/docs/access?context=tagged-events&version=australia&pubname=australia-now-intelligence&ft:locale=en-US)**

Create custom events without code directly in your application using the Usage Insights page overlay. Use event descriptions to provide greater visibility and clarity on Usage Insights events.

-   **[Funnels.](https://www.servicenow.com/docs/access?context=create-funnel&version=australia&pubname=australia-now-intelligence&ft:locale=en-US)**

Access funnels you create in Usage Insights directly in the Platform Analytics UI to view this data along with your organization's other business metrics.

-   **[Dashboards.](https://www.servicenow.com/docs/access?context=uxa-dashboards&version=australia&pubname=australia-now-intelligence&ft:locale=en-US)**

Customize dashboards or pages for Platform Analytics directly in Usage Insights.


</td></tr><tr><td>

Virtual Agent

</td><td>

-   **[ServiceNow product tiers](https://www.servicenow.com/docs/access?context=ai-native-sku-overview&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)**

The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets, and create your own
Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.

-   **[Premium chat experience for Now Assist Panel - Platform \(default\) assistant](https://www.servicenow.com/docs/access?context=nava-integrated-chat&version=australia&pubname=australia-conversational-interfaces&ft:locale=en-US)**

The Now Assist Panel - Platform \(default\) assistant now has the premium chat experience configured by default.


</td></tr><tr><td>

Vulnerability Response

</td><td>

-   **[Unified Microsoft Defender Integration for Security Exposure Management](https://www.servicenow.com/docs/access?context=ms-defender-sem&version=australia&pubname=australia-security-management&ft:locale=en-US)**

The Microsoft Defender for Cloud and Microsoft Defender Threat and Vulnerability Management \(MS TVM\) plugins are now consolidated into a single plugin: Microsoft Defender Integration for Security Exposure Management. This consolidation deprecates the standalone Microsoft Defender for Cloud plugin. The unified plugin also introduces container image vulnerability ingestion from Microsoft Defender for Cloud, creating Container Vulnerable Items on your instance. A guided migration path is available to transfer existing data from the deprecated applications to the unified plugin.

-   **[AWS Integration for Security Exposure Management](https://www.servicenow.com/docs/access?context=aws-integration-for-security-exposure-management-overview&version=australia&pubname=australia-security-management&ft:locale=en-US)**

The AWS Integration for Security Exposure Management supports integrations with the following AWS services:

    -   AWS Inspector is an automated vulnerability management service that continuously scans EC2 instances, ECR container images, and Lambda functions for software vulnerabilities \(CVEs\) and unintended network exposure. The Vulnerability Response integration with AWS Inspector imports host and container vulnerability findings from AWS Inspector.
    -   AWS Security Hub is a security service that is used to centralize and update security checks across AWS accounts. It provides a unified view of security alerts and compliance status by integrating with various AWS services. The Vulnerability Response integration with AWS Security Hub imports host, container vulnerabilities, and misconfigurations from AWS Security Hub.
-   **[Optimized Tenable.io Compliance Results ingestion](https://www.servicenow.com/docs/access?context=tenableIntegration&version=australia&pubname=australia-security-management&ft:locale=en-US)**

Starting with v 6.1.3, the Tenable.io Compliance Results Integration is replaced by the Tenable.io Fixed Compliance Results Integration and Tenable.io Open Compliance Results Integration. Compliance results are now imported based on their status, optimizing ingestion performance and scalability for environments with large volumes of compliance data while keeping remediation and compliance tracking aligned with the current state of findings.

-   **[Qualys Integration – API enhancements](https://www.servicenow.com/docs/access?context=c_QualysVulnIntegration&version=australia&pubname=australia-security-management&ft:locale=en-US)**

The Qualys Vulnerability Integration has been upgraded to support newer Qualys API versions across Host Detection, Host List, Knowledgebase, PC Controls, PC Policies, and PCRS integrations. The integrations now ingest additional data fields, including vulnerability detection source, authentication privilege status, active status for controls and policies, and cloud metadata, giving you better visibility into your vulnerability and compliance data. Use the new `posture_api_version` integration instance parameter to choose between the default v2.0 APIs or the newer v5.0 streaming APIs for the PCRS Policy Host and PCRS Test Results integrations.

-   **[Vulnerability Data Management with Central Vulnerability Database \(CVDB\)](https://www.servicenow.com/docs/access?context=cvd-overview&version=australia&pubname=australia-security-management&ft:locale=en-US)**

The Central Vulnerability Database \(CVDB\) introduces a unified, source-agnostic vulnerability data layer that consolidates data from multiple sources into a single authoritative record, improving accuracy, consistency, and traceability. Key capabilities include:

    -   Unified vulnerability record: Correlates vulnerability data from multiple sources, supports sources including National Vulnerability Database \(NVD\), scanner intelligence, European Union Vulnerability Database, Japanese Vulnerability Database, and vulnerability intelligence feeds.
    -   Priority-based data reconciliation configuration:
        -   Field-level priority: Ensures each attribute \(e.g., CVSS, remediation, exploit status\) can be configured from the most reliable provider.
        -   Source-level priority: Applies a global ranking when field-level rules are not defined.
        -   Hybrid model: Field-level rules take precedence, with source-level fallback; all source data is preserved for full traceability.
    -   Source attribution and traceability: Maintains detailed source metadata, timestamps, and change history to ensure full auditability and transparency.
    -   Data enrichment: Combines CVSS scores, exploit intelligence, and remediation guidance to provide a richer and more actionable vulnerability context.

</td></tr><tr><td>

Workforce Optimization for CSM

</td><td>

-   **[Location Based Holiday Calendar Management](https://www.servicenow.com/docs/access?context=location-based-holiday-calendar-management&version=australia&pubname=australia-customer-service-management&ft:locale=en-US)**

Enable location-based holiday calendars to

    -   Manage location‑based holiday calendars that auto‑sync to schedules, providing real‑time visibility into regional holiday impacts and supporting accurate shift planning.
    -   Improve workforce scheduling and compliance by mapping holidays to specific regions, reducing manual adjustments and ensuring agents see their location‑based holidays in My Calendar.
-   **[Manager Workspace landing page](https://www.servicenow.com/docs/access?context=csm-configurable-manager-workspace-dashboards-new&version=australia&pubname=australia-customer-service-management&ft:locale=en-US)**

Enhance the Manager Dashboard to view

    -   New **AI Insights** tab on the Manager Dashboard in the Manager Workspace \(Enterprise SKU\).
    -   The AI powered widgets: Sentiment Analysis, Trending Topics, and Auto QA. These widgets provide deeper, real‑time visibility into customer sentiment signals, trending interaction themes, and quality evaluations.
-   **[Manager dashboard for operational Insights](https://www.servicenow.com/docs/access?context=manager-dashboard-for-operational-insights&version=australia&pubname=australia-customer-service-management&ft:locale=en-US)**

Decouple the existing Manager Dashboard to make it available as a standalone feature.

    -   Install and configure the Manager Dashboard independently to provide a streamlined, modular experience, retaining only essential alerts and core widgets for performance, work management, and resource visibility while removing scheduling and coaching components.
    -   Pro customers can view Help Request alerts and Operational Insights when Channel Management is adopted with the dashboard. These capabilities are not available when Channel Management is adopted without the dashboard.
    -   Pro+ customers can view a tab based dashboard layout with AI powered widgets Sentiment Analysis, Trending Topics, and Auto QA for Customer Signals and Quality Management. They can access the Operations Insights tab with widgets like Performance, Work Management, and Resource Management.
-   **[Listen, Monitor or Barge in to an agent call](https://www.servicenow.com/docs/access?context=listen-agent-call-configurable-wfo-cs&version=australia&pubname=australia-customer-service-management&ft:locale=en-US)**

Monitor, coach, or barge into voice calls to

    -   Assist agents during live customer calls by opening the agent’s active phone interaction in Manager Workspace.
    -   Enable supervisors to silently monitor calls, whisper‑coach agents, join conversations, view real‑time transcription when the conversation panel is enabled, and switch modes or end the session at any time using the NVC utility panel.
-   **[Manager Workspace landing page](https://www.servicenow.com/docs/access?context=csm-configurable-manager-workspace-dashboards-new&version=australia&pubname=australia-customer-service-management&ft:locale=en-US)**

Enable Manager dashboard to view the Help Request on the landing page.

    -   View the **Help Request** tab on the Manager Workspace landing page and in Conversation Monitoring list view.
    -   Segment Help Request interactions by different channel including Chat, Email, Messaging, Phone and Video.
-   **[Channel Management in Workforce Optimization for Customer Service](https://www.servicenow.com/docs/access?context=explore-channels-configurable-wfo-cs&version=australia&pubname=australia-customer-service-management&ft:locale=en-US)**
    -   View the **Help Request** tab on the Channel Management landing page.
    -   Enable supervisors to open any active voice request to review context and take action by monitoring the live call, coaching the agent privately, or barging in to speak with both the agent and the customer.

</td></tr><tr><td>

Zero Copy Connectors

</td><td>

-   **[Cloudera Impala](https://www.servicenow.com/docs/access?context=cloudera-impala-zcc&version=australia&pubname=australia-integrate-applications&ft:locale=en-US)**

Retrieve data from Cloudera Impala in real time without copying or duplicating the data.

-   **[Australia Patch 1](../quality/australia-patch-1.md)[Connect to Prometheus](https://www.servicenow.com/docs/access?context=prometheus-zcc&version=australia&pubname=australia-integrate-applications&ft:locale=en-US)**

Retrieve data from Prometheus in real time without copying or duplicating the data.

-   **[Connect to another ServiceNow® instance](https://www.servicenow.com/docs/access?context=servicenow-remote-instance-zcc&version=australia&pubname=australia-integrate-applications&ft:locale=en-US)**

Retrieve data from another ServiceNow® instance in real time without copying or duplicating the data.

-   **[OAuth authentication](https://www.servicenow.com/docs/access?context=create-databricks-connection-zcc&version=australia&pubname=australia-integrate-applications&ft:locale=en-US)**

Configure OAuth authentication in Databricks, Oracle, and Snowflake connectors.


</td></tr></tbody>
</table>**Parent Topic:**[Release notes summaries for Australia features](../release-notes-summaries.md)


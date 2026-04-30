---
title: Highlights for all Zurich features and products
description: Cumulative release notes summary on highlights of Zurich features and products.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2026-04-08"
reading_time_minutes: 150
breadcrumb: [Release notes summaries for Zurich features, Release notes for upgrading from Yokohama, Learn about the Zurich release, Zurich release notes]
---

# Highlights for all Zurich features and products

Cumulative release notes summary on highlights of Zurich features and products.

Review the product highlights to learn what's new in Zurich.

<table id="rn-summary-changes-table" class="custom-rows"><thead><tr><th class="filter">

Application or feature

</th><th>

Details

</th></tr></thead><tbody><tr><td>

AI Control Tower

</td><td>

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

</td></tr><tr><td>

AI Risk and Compliance

</td><td>

-   Use entity-based access to limit AI asset data access to authorized users, maintaining core entity visibility.
-   Perform assessment on multiple risks for an AI asset by creating a risk assessment project.
-   Activate and manage pre-configured content packs using the unified content hub.
-   Report AI cases or raise AI inquiries by emailing a dedicated address, which automatically creates a new, trackable record in the system.
-   Retire and replace AI assets with structured workflows that prevent compliance gaps and security risks.
-   Aggregate system-level AI risk scores by embedding heatmaps and residual score widgets within your AI asset overview records. You get visibility into your cumulative risk across the AI inventory and support for continuous risk monitoring.
-   Get the dedicated AI risk and compliance views for your AI models and dataset records. With these views, you have a centralized interface where you can assess, monitor, and manage the risk and compliance attributes that are specific to your AI assets.
-   Enforce role-based access controls, enable employee-initiated AI asset requests, and maintain consistent life-cycle state tracking across all your AI assets and dashboards. This capability helps you to ensure security, transparency, and governance throughout the asset life-cycle.
-   View and manage your AI asset's risk and compliance cases more efficiently by accessing the new **AI cases** tab on the AI Risk and Compliance home page.
-   Monitor and track the risk and compliance posture of your AI assets to ensure that your organization aligns with organizational and regulatory standards. You can also gain real-time insights into the emerging risks and compliance gaps across your AI portfolio.

See [AI Risk and Compliance](https://www.servicenow.com/docs/access?context=ai-risk-and-compliance&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US) for more information.

</td></tr><tr><td>

AI Search

</td><td>

[Zurich Patch 4](../quality/zurich-patch-4.md)

-   Improve search precision and contextual relevance with hybrid search, available for customers with Now Assist in AI Search installed.
-   Gain insights into search behavior with a refreshed and updated Search Preview UI.

[Zurich Patch 1](../quality/zurich-patch-1.md)

-   Search more intuitively with an updated, consumer-grade user experience in search portals, global search, and workspace search.

[Zurich Early Availability](../quality/zurich-security-notables.md)

-   Improve search precision by displaying external content search results in languages configured for the user's search session.
-   Increase search recall by indexing searchable content and metadata from Multiple Choice and Select Box variables in records on the Catalog Item table and its child tables.

See [AI Search](https://www.servicenow.com/docs/access?context=overview-ais&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US) for more information.

</td></tr><tr><td>

AIOps LEAP

</td><td>

Use Google Gemini, Azure OpenAI, and Anthropic LLM in AIOps LEAP in addition to Now LLM Service. See [AIOps Learning Enhanced Automation Platform \(LEAP\)](https://www.servicenow.com/docs/access?context=aiops-leap&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

API

</td><td>

-   Use server-side JavaScript APIs in scripts to change the application functionality.
-   Run client APIs whenever a client-based event occurs, such as when a form loads, a form is submitted, or a field value changes.
-   Use inbound REST APIs to interact with various ServiceNow functionalities within your application.
-   Client Next Experience APIs include client APIs compatible with the Next Experience UI.

See [API implementation and reference](https://www.servicenow.com/docs/access?context=api-implementation-reference&version=zurich&pubname=zurich-api-reference&ft:locale=en-US) for more information.

</td></tr><tr><td>

Access Management

</td><td>

-   Enforce access to data via REST or SOAP endpoints using the Machine Identity Access Controls, which helps improve security, governance, and auditability.
-   Target all table columns of a given data type with a single ACL using Datatype ACLs.
-   Govern scripting permissions with the Scripting Governance tool, a new base system deny-by-default behavior.

See [Access Control List Rules](https://www.servicenow.com/docs/access?context=access-control-rules&version=zurich&pubname=zurich-platform-security&ft:locale=en-US) for more information.

</td></tr><tr><td>

Accounts Payable Operations

</td><td>

-   Leverage Accounts payable document classification skill to classify email attachments into invoice, credit memo, or supporting documents based on the AI recommended confidence score resulting in error free invoice data extraction.
-   Validate supplier provided tax against a system-calculated tax by integrating an enterprise-grade tax engine resulting in straight-through processing of invoice while improving accuracy, compliance, and operational efficiency.
-   Process your invoice more effectively and accurately with the new missing tax code invoice exception and currency mismatch.
-   Handle various AP related inquiries and tasks through a single entry point by using the Universal Request \(UR\) as a multi-purpose request form.
-   Leverage AI-powered agentic workflow to recommend the appropriate business owner for non-PO invoices based on historical patterns.
-   Automate cost allocations in the invoice lines using distribution sets.

See [Accounts Payable Operations](https://www.servicenow.com/docs/access?context=acc-pay-mgmt-landing-page&version=zurich&pubname=zurich-source-to-pay-operations&ft:locale=en-US) for more information.

</td></tr><tr><td>

Adoption Services

</td><td>

Explore Dynamic Guidance within [In-product help](https://www.servicenow.com/docs/access?context=inproduct-help&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US) features of [Adoption services](https://www.servicenow.com/docs/access?context=adoption-services&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US) as the proactive AI assistant that generates an engaging voice based, step by step guidance, dynamically, across platforms.

-   Use Onboarding modals that now align with the theme of the chosen ServiceNow® instance.
-   Discover and select Guided Tours from the list that is available in Help Center.

See [Adoption services](https://www.servicenow.com/docs/access?context=adoption-services&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US) for more information.

</td></tr><tr><td>

Advanced AI Search Management Tools

</td><td>

[Zurich Patch 4](../quality/zurich-patch-4.md)

-   Review performance metrics and trends more easily with an updated and refreshed dashboard UI.
-   Analyze performance metrics and trends for search applications used in Recommended Actions.

[Zurich Patch 1](../quality/zurich-patch-1.md)

-   Analyze search trends from the preceding six months using the AI Search Analytics dashboard's **Date range** interactive filter.
-   Understand your mobile search traffic with support for the Mobile Platform search application in the AI Search Analytics dashboard's **Search application** interactive filter.

See [Platform Analytics Solution for Advanced AI Search Management Tools](https://www.servicenow.com/docs/access?context=adv-ais-mgmt-tools-content-pack&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US) for more information.

</td></tr><tr><td>

Advanced Risk

</td><td>

-   **[Some Now Assist skills, agents, and agentic workflows are turned on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

The skills are automatically available to appropriate role users for the application, such as ITIL roles on incident forms or change forms. This change simply activates the skill and does not touch the roles that may be needed to use the skill. The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills and agentic workflows are turned on automatically.
    -   Existing customers who are upgrading \(starting with Zurich Patch 4\): Any previously unconfigured skill, agent, or agentic workflow is turned on automatically \(the AI asset was never configured and turned on, then turned off again\). Previously configured skills and agentic workflows that were turned on, then off, remain inactive.

-   Use the Risk Suggestion AI Agent to discover potential risks for an entity, giving risk managers better insights for informed decision-making.
-   Use the risk reporting view to view all assessments under a specific Risk Assessment Methodology \(RAM\), including factor responses, scores, issues, and risks.
-   Use generative AI to generate risk event summary to quickly understand the risk event key details for faster decisions.
-   Assess multiple risks and controls side-by-side, make bulk edits, and prioritize entries efficiently using the spreadsheet-style layout.
-   Use matrix report in the Risk Workspace to assess and analyze the risk posture of your organization.
-   Use large language models \(LLMs\) from the third party providers to generate the risk assessment summary.

See [Advanced Risk Assessment](https://www.servicenow.com/docs/access?context=advanced-risk-assessment&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US) for more information.

</td></tr><tr><td>

Advanced Work Assignment \(AWA\)

</td><td>

Use AWA with an inbox card in Workspace without an existing interaction or work item.

See [Advanced Work Assignment](https://www.servicenow.com/docs/access?context=awa-application-landing-page&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US) for more information.

</td></tr><tr><td>

Agent Chat

</td><td>

Integrate and use Agent Chat with third-party chat apps.

See [Using Agent Chat](https://www.servicenow.com/docs/access?context=ci-agent-chat-using&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US) for more information.

</td></tr><tr><td>

Agent Client Collector

</td><td>

-   Discover TLS/SSL certificates using Agent Client Collector for Visibility - Content certificate Discovery.
-   Enhance data collection by disabling only those checks with high resource usage, allowing data collection to continue for other checks.
-   Improve troubleshooting capabilities by viewing errors that occur before and after the registration process in the ServiceNow instance.
-   Use file-based Discovery in a macOS environment.

See [Agent Client Collector](https://www.servicenow.com/docs/access?context=acc-landing-page&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Agent experience for CSM

</td><td>

-   Provide front-line agents with an updated chat interaction user experience that puts the chat component front and center.
-   Use the callback component to return customer calls and create interaction records at the time of the callback.
-   Provide agents with visibility to all previous customer activity and the ability to filter and search to find specific activities.
-   Initiate a comment, work note, or email in the activity stream in CSM Configurable Workspace and then open the text in a modeless dialog.

See [CSM Configurable Workspace](https://www.servicenow.com/docs/access?context=csm-workspaces-configure&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Agentic Desktop

</td><td>

[Zurich Patch 8](../quality/zurich-patch-8.md)

-   Improved error and informational messages for better guidance and troubleshooting.
-   Added a **Delete** button to the image canvas to remove a screen.
-   Enabled screen-level testing while designing desktop actions.

[Zurich Patch 7](../quality/zurich-patch-7.md)

-   Use smart sizing in the Execution workspace with the **Fit to window** and **Original resolution** options.
-   Enable AI agents to securely access SSH parameters by setting up parameter records in the ServiceNow instance.
-   Test specific screens within desktop actions without running the entire flow.
-   Access application controls during recording with a recorder toolbar.
-   Configure the AI Desktop Actions installer experience for settings that are essential for seamless execution of desktop actions.

[Zurich Patch 4](../quality/zurich-patch-4.md)

-   Desktop actions now run reliably on machines with different screen resolutions.

-   Design desktop actions of type UI block \(UI actions\) by capturing user interactions, adding details, and activating them in Design workspace.
-   Use default desktop actions of type non-UI block \(non-UI actions\) that include pre-built connectors to interact with various applications and system components.
-   Add desktop actions as tools to AI agents in AI Agent Studio.
-   Enable AI agents to interact with legacy systems, thick client applications, and business applications on Windows operating system to perform repetitive tasks.
-   Monitor desktop actions being executed by AI agents in Execution workspace in the Desktop-in-Desktop session.

See [AI Desktop Actions](https://www.servicenow.com/docs/access?context=agentic-desktop-landing-page&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US) for more information.

</td></tr><tr><td>

Alumni Center

</td><td>

-   The application name Alumni Service Center is now called Alumni Center.
-   As an alumni, you can see the revamped Alumni Center with Employee Center Pro experiences such as My Active Items, Proactive Prompts, and Content Widgets.
-   As an alumni, you can use improved alumni services available out-of-the-box.
-   As an alumni, you can securely access your documents directly from your profile.
-   As an alumni, use the **Register as alumni** option to create an account with the Alumni Center and login to the Alumni Center website.
-   As an alumni registering in the Alumni Center portal, you can enter details like first name, last name, personal email address and employee number which can be used to verify and match the ex-employee records.
-   As an alumni, you can maintain and update your personal details directly within your profile.
-   As an alumni, you can enter your legacy employment details and latest employment details to maintain your employment history.
-   As an alumni, your can enable or disable notifications for recommended job opportunities, and news/event updates in your profile.
-   As an alumni admin, you can configure the customer specific termination conditions using the HR profile fields to trigger alumni creation process automatically on employee termination.
-   As an alumni admin, you can configure the Alum Self-registration form based on the organization needs.
-   As an alumni admin, you can highlight and showcase the recommended job opportunities.​​​

See  for more information.

</td></tr><tr><td>

App Engine Management Center

</td><td>

-   Manage deployments using the new ReleaseOps integration in AEMC. ReleaseOps enables the deployment of update sets via a pipeline and leverages the automation capabilities of ServiceNow Playbooks for deployments that are less manual and error-prone.
-   Migrate your existing App Engine pipelines to ReleaseOps.
-   Oversee application development, deployment, and insights using AEMC.

See [App Engine Management Center](https://www.servicenow.com/docs/access?context=app-engine-management-center&version=zurich&pubname=zurich-application-development&ft:locale=en-US) for more information.

</td></tr><tr><td>

Applicant Center

</td><td>

-   As an applicant, log in with a magic link without the hassle of a password.
-   Learn more about the role that you’ve applied for, the company, and its culture even before the interview stage, helping you better understand the opportunity from the start.
-   View the hiring team, job description, and track multiple applications in one place. Communicate seamlessly with your recruiter for updates, questions, or support during the hiring process.
-   Manage your interviews and related activities, such as selecting your preferred time slot or submitting reschedule requests, all within the portal.
-   Experience a connected pre-hire journey by receiving and reviewing key notifications that keep you informed and aligned at every step of the application process.

See [Applicant Center](https://www.servicenow.com/docs/access?context=applicant-center-concept&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Application Manager

</td><td>

Zurich patch 4

-   Reduce potential runtime errors by installing and updating Now Assist applications with suites of interdependent versions.
-   View all ServiceNow Store applications that are licensed or available for procurement from the **Available for you** tab.
-   Gain insights about application installation requirements and blockers with application state indicators.

See [Application Manager](https://www.servicenow.com/docs/access?context=application-manager&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US) for more information.

</td></tr><tr><td>

Application Vulnerability Response

</td><td>

-   If you are currently using Application Vulnerability Response and you want to upgrade to Unified Security Exposure Management \(USEM\), see [Unified Security Exposure Management release notes](../security-operations/secops-sem-rn.md) for more information about USEM and the Unified Security Exposure Management migration.
-   Monitor your penetration test requests and findings, as well as your team's overall progress in the Penetration Test Workspace.
-   Reevaluate the risk score, assignments, remediation target date, exceptions, and remediation task for a specific set of application vulnerable items in the Vulnerability Manager Workspace.
-   Integrate with supported third-party scanners to import vulnerability data.
-   Compare application vulnerability-related data and determine if application vulnerabilities are found in an application.
-   Prioritize, remediate, and manage application vulnerable items \(AVIT\)s. Each application vulnerability represents a vulnerability entry in the Common Weakness Enumeration \(CWE\) or third-party libraries.
-   With the sn\_vul.app\_sec\_manager role, create application remediation tasks manually in the Vulnerability Manager Workspace.

See [Application Vulnerability Response](https://www.servicenow.com/docs/access?context=avr-landing&version=zurich&pubname=zurich-security-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Asset Audit Response

</td><td>

-   Enable asset managers to fulfill evidence requests for your financial regulatory audits through the Asset Response Guided Experience.
-   Track and manage responses to evidence requests for your financial regulatory audits in the Asset Governance Workspace.
-   Manage financial regulatory audit engagements and create corresponding evidence requests in the Audit Workspace.
-   Help asset managers respond to financial regulatory audits more accurately and efficiently by accessing predefined reports and financial regulatory context.
-   Identify gaps in your asset data by using remediation rules and tasks.

See [Asset Audit Response](https://www.servicenow.com/docs/access?context=asset-audit-response&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Audit Management

</td><td>

-   Set audit time frames within engagements using new audit date fields. Filter indicator results by specific periods, independent of the overall engagement time frame.
-   Access pre-configured content packs through the new Content Accelerator icon in the Audit Workspace. This includes the Digital Operational Resilience Act \(DORA\) pack with citations and authority documents.
-   Create evidence responses quickly with a simplified process.
-   Access engagements, add existing entities to an engagement, and create activities in the Lite Audit workspace, which is a simplified version of the Audit Management workspace. If the advance core store app is installed, evidences can also be associated with the engagement.

See [Audit Management](https://www.servicenow.com/docs/access?context=c_GRCAudits&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US) for more information.

</td></tr><tr><td>

Authentication

</td><td>

[Zurich Patch 7](../quality/zurich-patch-7.md)

-   **[Knowledge-based factor enhancement for AI voice service](https://www.servicenow.com/docs/access?context=knowledge-based-authentication&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)**

Following are the knowledge-based authentication \(KBA\) enhancements:

    -   [Voice input support for KBA questions](https://www.servicenow.com/docs/access?context=create-knowledge-based-questions&version=zurich&pubname=zurich-platform-security&ft:locale=en-US): Configure KBA questions to support Voice as an input type, allowing users to provide spoken responses during identification and authentication. When Voice input is enabled, you can configure the expected format, provide examples, and optionally define a validation pattern using regular expressions.
    -   [Script-based validation for external systems](https://www.servicenow.com/docs/access?context=create-knowledge-based-answers&version=zurich&pubname=zurich-platform-security&ft:locale=en-US): Configure KBA answers to validate that are created against external systems using custom scripts through the Script Configuration field. When set to Identification mode, you can write scoped scripts that validate caller identity against external authentication systems instead of internal ServiceNow AI Platform tables.

[Zurich Patch 4](../quality/zurich-patch-4.md)

-   **[Authentication factors for AI voice service](https://www.servicenow.com/docs/access?context=authentication-factors&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)**

Enable caller access to AI voice agents by configuring the required identification and authentication factors.

-   **[OAuth enhancements](https://www.servicenow.com/docs/access?context=api-inbound-and-outbound&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)**

Following are the OAuth enhancements:

    -   Use **Opaque** or **JWT** token option for your inbound integration endpoints.
    -   Use the **Allow access only to APIs in selected scope** option to enable access to the APIs that are explicitly listed in the selected scopes for your inbound integrations.
    -   Use the OAuth Entity Resource tab for outbound integrations to configure resource parameters so they flow into the OAuth token request and are reflected in the token from your OAuth provider.

[Zurich Patch 3](../quality/zurich-patch-1.md)

-   **[Provider name for Inbound integrations](https://www.servicenow.com/docs/access?context=new-inbound-integrations&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)**

Use the Provider name field to enter the details of your inbound integrations to distinguish between different inbound integrations on your ServiceNow AI Platform®. Update the Provider name in your API integrations to improve monitoring capabilities:

    -   For OAuth integrations, update the provider name using the Provider name field. To know more, see [OAuth inbound](https://www.servicenow.com/docs/access?context=oauth-inbound&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).
    -   For Basic authentication integrations, update the Provider name in the integration registration form. To know more about the integration registration form, see [View Inbound API Integration Usage dashboard](https://www.servicenow.com/docs/access?context=view-inbound-api-integration-usage-dashboard&version=zurich&pubname=zurich-api-reference&ft:locale=en-US).

[Zurich Patch 1](../quality/zurich-patch-1.md)

-   **OAuth token enhancement**

Use Opaque or JWT token option for your inbound integration endpoints.


Zurich

-   Experience the new Inbound integration configuration in the Machine Identity Console.
-   Use the new MFA Dashboard to understand insights such as MFA user enrollment, privileged admins who haven't opted in to MFA, and compliance.
-   Use the FIDO factor policy to enforce FIDO-based authentication.
-   Use the enhanced SSO login and logout experience.
-   Configure the authentication policies to restrict access, reduce roles, or enforce MFA based on Identity Provider \(IdP\) attributes that are received from the OIDC response.

See [Authentication](https://www.servicenow.com/docs/access?context=c_Authentication&version=zurich&pubname=zurich-platform-security&ft:locale=en-US) for more information.

</td></tr><tr><td>

Automated Test Framework

</td><td>

-   Reduce upgrade and development time by replacing manual testing with automated testing.
-   Design tests once and reuse them in different contexts and with different test data sets.
-   Keep test instances clean by rolling back test data and changes made after each test run.
-   Create and schedule test suites to organize and run tests in batches.
-   Reduce test design time by copying quick start tests and test suites. You can also create custom test steps to expand test coverage.

See [Automated Test Framework \(ATF\)](https://www.servicenow.com/docs/access?context=atf-landing-page&version=zurich&pubname=zurich-application-development&ft:locale=en-US) for more information.

</td></tr><tr><td>

Business Continuity Management

</td><td>

-   Set up phases in recovery tasks and event tasks for recovery event management.
-   Calculate more accurate RTO and RPO with the finalized RTO and RPO columns in BIAs, BCPs, and events.
-   View plans from the enhanced BCM Mobile application.
-   Manage templates and generate Microsoft Word reports for business impact analyses \(BIAs\), business continuity plans \(BCPs\), and events by using the Document designer add-in.
-   Avoid duplicate event tasks by identifying and grouping similar tasks in exercises and crises.
-   Create action items and send out threat assessments by leveraging Smart Assessment during exercises and crises.

See [Business Continuity Management](https://www.servicenow.com/docs/access?context=business-continuity-mangmt-overview&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US) for more information.

</td></tr><tr><td>

CPQ Configurator

</td><td>

-   Provides sales agents and customers with an intuitive interface for attribute-based configuration in addition to product-based configuration of customizable products.
-   Enables agents and customers to select valid product options during product configuration and view real-time updates that show how their selections affect associated pricing.
-   Enables product catalog admins to generate and update product offering blueprints that guide the accurate configuration of customizable products by agents and customers.

See [CPQ Configurator](https://www.servicenow.com/docs/access?context=explore-servicenowcpq&version=zurich&pubname=zurich-order-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Card data security

</td><td>

-   Ensure Payment Card Industry \(PCI\) compliance and the secure handling of sensitive card data with an integrated tokenization solution for Financial Services Operations disputes.
-   Integrate with major core systems and third-party systems, including \(but not limited to\) Visa, Mastercom, Mastercom Extended, Ethoca, Verifi, and Visa Stop Payment Service. Visa and Mastercom are predefined integrations.

See [Card Data Security](https://www.servicenow.com/docs/access?context=card-data-security&version=zurich&pubname=zurich-financial-services-operations&ft:locale=en-US) for more information.

</td></tr><tr><td>

Care Team Mobile

</td><td>

-   Create support requests based on installed Healthcare Operations case types directly from your mobile device.
-   Scan asset tags on IT and medical assets and be redirected to the asset's record, where you can view its history, status, and associated cases.
-   View requests for specific locations, such as patient rooms or supply closets.
-   Access relevant details and preconfigured workflows for reporting issues like sanitation requests or facility repairs.

See [Care Team Mobile](https://www.servicenow.com/docs/access?context=care-team-mobile-landing&version=zurich&pubname=zurich-healthcare-life-sciences&ft:locale=en-US) for more information.

</td></tr><tr><td>

Care Team Operations for Biomed

</td><td>

Assign roles and responsibilities more efficiently with an updated user configuration process.

See [Care Team Operations for Biomed](https://www.servicenow.com/docs/access?context=care-team-operations-for-biomed&version=zurich&pubname=zurich-healthcare-life-sciences&ft:locale=en-US) for more information.

</td></tr><tr><td>

Care Team Operations for Environmental Services

</td><td>

-   Automate healthcare operations by enabling environmental support request creation and fulfillment.
-   Create environmental services support requests from directly within the Care Team Portal or Care Team Mobile.
-   Gain full visibility into reported environmental services support cases while enabling environmental service support teams to manage and fulfill them as work orders or work orders tasks when Field Service Management is installed.
-   Assign roles and responsibilities more efficiently with a streamlined user configuration processes.

See [Care Team Operations for Environmental Services](https://www.servicenow.com/docs/access?context=cto-evs-landing&version=zurich&pubname=zurich-healthcare-life-sciences&ft:locale=en-US) for more information.

</td></tr><tr><td>

Care Team Operations for Facilities

</td><td>

-   Automate healthcare operations by enabling facilities support request creation and fulfillment.
-   Create facility support requests from directly within the Care Team Portal or Care Team Mobile.
-   Gain full visibility into reported facilities support cases while enabling facilities teams to manage and fulfill them as work orders or work orders tasks when Field Service Management is installed.\]
-   Assign roles and responsibilities more efficiently with a streamlined user configuration process.

See [Care Team Operations for Facilities](https://www.servicenow.com/docs/access?context=cto-facilities-landing&version=zurich&pubname=zurich-healthcare-life-sciences&ft:locale=en-US) for more information.

</td></tr><tr><td>

Care Team Operations for Healthcare IT

</td><td>

Assign roles and responsibilities more efficiently with an updated user configuration process.

See [Care Team Operations for Healthcare IT](https://www.servicenow.com/docs/access?context=hcls-cto-it-app&version=zurich&pubname=zurich-healthcare-life-sciences&ft:locale=en-US) for more information.

</td></tr><tr><td>

Career Conversations

</td><td>

[Zurich Patch 7](../quality/zurich-patch-7.md)

-   As an admin, create reusable feedback templates using the ServiceNow AI Platform Surveys tool.
-   As a manager, select and preview feedback templates when requesting feedback.
-   As a manager, review a summarized view of an employee's recent feedback on the feedback page in Manager Hub.

[Zurich Patch 2](../quality/zurich-patch-2.md)

-   Use Google Gemini and Anthropic Claude on AWS as AI model providers for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.
-   Make career conversations easy to create and track using the growth conversations agentic workflow.
-   As a manager, find and share relevant resources to conduct meaningful conversations using the Manager resource recommendation AI agent.
-   As a manager, you can now edit a series, and also specify when a series should end while creating the growth conversation.

See [Career Conversations](https://www.servicenow.com/docs/access?context=egd-activities-landing-page&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Case management for CSM

</td><td>

-   Sharing task plan templates ensures that only authorized users can access, edit, or share templates based on their role and location, preventing misuse and maintaining operational integrity.
-   View the most relevant services that are available for customers when creating customer service cases.
-   View and select from the available entitlements that are associated with the customer, product, and contract information to associate multiple entitlements with customer service cases.
-   Filter the service definitions that are displayed to agents based on such criteria as the assigned role or group, or entity criteria.

See [Case management for Customer Service Management](https://www.servicenow.com/docs/access?context=csm-case-management&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Change Management

</td><td>

-   Review and authorize change requests and review recently implemented changes in the Change Advisory Board Workbench in the Service Operations Workspace \(SOW\).
-   Track conflict detection using the Change - Conflict Detection flow and the Change Management Worker table instead of Progress Workers.
-   Limit the number of conflict records for each conflict type through the **change.conflict.max\_count** system property.
-   Coral is the new default theme for Next Experience and Core UI, offering a more modern experience.


See [Change Management](https://www.servicenow.com/docs/access?context=c_ITILChangeManagement&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Classic Workflow

</td><td>

-   Added the snc\_required\_script\_writer role to all Workflow tasks.
-   Removed the legacy workflows created and published by ServiceNow, Inc. from new customer installations.

See [Classic Workflow](https://www.servicenow.com/docs/access?context=c_WorkflowOverview&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US) for more information.

</td></tr><tr><td>

Clone Admin Console

</td><td>

-   Configure the update set preservation up to 12 minutes before the clone executes.
-   Preserve your in-progress update sets, regardless of when the scope was created in the specified time frame.


See [Clone Admin Console](https://www.servicenow.com/docs/access?context=Clone-UI&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US) for more information.

</td></tr><tr><td>

Cloud Cost Management 9.0

</td><td>

-   Retrieve cost and usage data faster from the Azure billing download by using the Azure Export method.
-   Leverage Azure Microsoft Customer Agreement \(MCA\) to optimize spend reporting and recommendations for potential savings.

See [Cloud Cost Management](https://www.servicenow.com/docs/access?context=cloud-insights-landing-page&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Cloud Exposure View

</td><td>

-   Monitor and act on all your cloud-related security findings from multiple vendors across your cloud environments.
-   Configure widgets that display interactive visualizations and filter assets by category for findings, assets, and exceptions.
-   View panels that link you to lists for more details about your findings.
-   View aggregated security data imported from third-party vendors.
-   Aggregated data from the Cloud Exposure View can be viewed in the Unified Cloud workspace that is supported by ITOM Cloud Accelerate. See [ITOM Cloud Accelerate release notes](../it-operations-management/itom-cloud-accelerate-rn.md) for more information.

See Exploring Cloud Exposure View for more information.

</td></tr><tr><td>

Code Signing

</td><td>

[Zurich Patch 4](../quality/zurich-patch-4.md)

-   **[Code Signing OOB Apps Signatures plugin](https://www.servicenow.com/docs/access?context=explore-code-signing&version=zurich&pubname=zurich-platform-security&ft:locale=en-US#cs-validation-jobs)**

Use this plugin \(com.glide.code\_signing.oob\_apps\_signatures\) to install build time signatures for all relevant records in trued-up ServiceNow® Store application versions.


-   Use Code Signing Guardrails to improve checks during the signing process to create more secure workflows.
-   Use the Code Signing Migration workflow to identify the signatures that are created with expired or inactive certificates and re-assign them to the appropriate records automatically.
-   Revoke Code Signing certificates securely using a quorum-based approval policy to prevent unauthorized use.
-   Monitor and manage your Code Signing environment with the new Health and Status dashboard.
-   The restructured navigation panel and the renamed pages provide improved accessibility and streamlined functionality.

</td></tr><tr><td>

Collaborative Work Management

</td><td>

-   Plan, track, and manage team work in Agile methodology with sprint planning in the CWM workspace.
-   Streamline task management for teams by integrating various work items across ServiceNow applications into CWM Boards.
-   Filter and group work by vertical and horizontal swimlanes in the Kanban view for a specific work item type.

See [Collaborative Work Management](https://www.servicenow.com/docs/access?context=cwm-landing&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Common Core

</td><td>

-   Use the report a GRC issue AI agent in the Employee Center to report issues through a guided conversational experience.
-   Ensure seamless access for users and groups referenced in user fields on records by leveraging entity-based access restrictions through record attribute user access configuration. Minimize manual effort, reduce administrative overhead, and enable entity-based access with minimal disruption.
-   Configure which task and tab settings appear in My Tasks by marking them Active or Inactive in the applicable table for easier management. Use the Active/Inactive flag in the GRC choice table to control visibility.
-   Automatically sync and maintain entity names in GRC with associated CI names to improve data consistency and reduce manual effort.
-   Authenticate users with the MCP Server to add a Model Context Protocol tool to AI agents using the Model Context Protocol Client.
-   Create ACLs for AI agents and agentic workflows to customize who can discover and trigger AI agents and agentic workflows.
-   Generate control recommendations for each regulatory alert to address compliance requirements. Use these suggestions to save time, minimize manual effort, and ensure a consistent response to regulatory changes.
-   Apply access restrictions at the record level by using the record access update utility in guided assistance. You can also preview the impacted record counts before updating and review the results and execution logs after the update.
-   Apply access restrictions automatically to newly created or modified records using entity-based record access rules.
-   Deactivate the entity-based access configurations.
-   Enable entity-based access on custom GRC tables.

For detailed documentation, see [Common Governance, Risk, and Compliance features](https://www.servicenow.com/docs/access?context=common-grc-features&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US).

</td></tr><tr><td>

Configurable Workspace

</td><td>

-   See who is active within a form with live presence and user avatars that display a contact card.
-   Use the Record List component bundle to create lists for all list types and the Predicate Builder component to create conditional statements.
-   Create emails, work notes, and comments while working on other tasks with a pop-out, modeless dialog in the Compose editor.
-   Rename and reorder the **Emails**, **Work notes**, and **Comments** tabs in the Compose editor.
-   Send emails with a digital signature that verifies you as an authentic sender and an email encryption that certifies authentic recipients.

See [Workspace UI](https://www.servicenow.com/docs/access?context=workspace-landing-page&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US) for more information.

</td></tr><tr><td>

Configuration Compliance

</td><td>

-   If you are currently using Configuration Compliance and you want to upgrade to Unified Security Exposure Management \(USEM\), see [Unified Security Exposure Management release notes](../security-operations/secops-sem-rn.md) for more information about USEM and the Unified Security Exposure Management migration.
-   Import Wiz issues and configuration test results from the Wiz scanners into test results in the Configuration Compliance application with the Vulnerability Response Integration with Wiz.
-   With the sn\_vulc.remediation\_owner role, create remediation tasks manually in the IT Remediation Workspace.
-   With the sn\_vulc.admin role, create remediation tasks manually in the Vulnerability Manager Workspace.

See [Configuration Compliance](https://www.servicenow.com/docs/access?context=vr-config-compliance-landing&version=zurich&pubname=zurich-security-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

-   Access a centralized location with a comprehensive view of the configuration item \(CI\) details by using the new CI form in CMDB Workspace. You can view and edit the CI attributes, relationships, and data, such as the CMDB Health report for the CI, CMDB 360 data that is associated with the CI, and the CI resources, activities, and related services.
-   Access the Data Certification dashboard in CMDB Workspace to gain insights about the data certification activities and progress, examine policies and tasks, and see the reports about the certification instances, charts of the aging certification tasks, and group and individual workloads.
-   Add or remove CIs directly from a map in Unified Map. You can also add, modify, or delete CI relationships in CMDB.
-   Configure the system to use Identification and Reconciliation Engine \(IRE\) identification rules to uniquely identify CIs in a payload, instead of using the **source\_name** and **source\_native\_key** attributes.
-   In zbooted instances, the itil user role no longer contains the sn\_cmdb\_editor user role, and the itil\_admin user role no longer contains the sn\_cmdb\_admin user role. However, the sn\_cmdb\_admin and the sn\_cmdb\_editor user roles now have full \(create, update, delete\) access to the Configuration Item \[cmdb\_ci\] class.

See [Configuration Management](https://www.servicenow.com/docs/access?context=manage-cmdb&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US) for more information.

</td></tr><tr><td>

Container Vulnerability Response

</td><td>

-   If you are currently using Container Vulnerability Response and you want to upgrade to Unified Security Exposure Management \(USEM\), see [Unified Security Exposure Management release notes](../security-operations/secops-sem-rn.md) for more information about USEM and the Unified Security Exposure Management migration.
-   Import container image vulnerability data from the Wiz scanners into container vulnerable items \(CVITs\) with the Vulnerability Response Integration with Wiz.
-   With the sn\_vul\_container.vulnerability\_analyst or sn\_vul\_container.vulnerability\_admin role, create container remediation tasks manually in the Vulnerability Manager Workspace.
-   With the role sn\_vul\_container.remediation\_owner, create container remediation tasks manually in the IT Remediation Workspace.

See [Container Vulnerability Response](https://www.servicenow.com/docs/access?context=cvr-landing&version=zurich&pubname=zurich-security-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Continual Improvement Management

</td><td>

See [Continual Improvement Management](https://www.servicenow.com/docs/access?context=cim-landing-page&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Continuous Authorization and Monitoring

</td><td>

-   Simplify Governance, Risk, and Compliance processes by enabling admins to create, version, and manage custom workflows, define state models, configure approvals, assess risks, and standardize with NIST RMF migration.
-   The CAM workspace homepage now features card-based containers with headers, sidebars, and overviews for a more organized and modern experience.
-   Authorization boundaries and package layout are now vertical. New **Boundary Type** and **Classification** records are included in OSCAL export file.
-   Add a **Child Boundaries** to create one-to-many relationships between boundaries. You can view the parent-child boundary mapping of a authorization boundary in the **Highlighted details** panel under the **Boundary hierarchy** section.
-   Select the **Dynamic Filter** option to make boundary filters update system elements automatically based on conditions, enhancing filter flexibility.
-   Boundary operational status now automatically syncs with the package life cycle.
-   Generate and download Open Security Controls Assessment Language \(OSCAL\) System Security Plans \(SSP\) and Plan of Action and Milestones \(POA&amp;M\) files directly from within a package.
-   The OSCAL import playbook now supports importing single POA&amp;M JSON files, automatically maps users and groups by exact names to ServiceNow, and populates package roles and responsibilities for a streamlined import experience.
-   CAM overlays new capability has been introduced to perform various operations like addition, subtraction, custom while applying a policy overlay to an authorization package.
-   Import OSCAL models using a user-friendly playbook that guides you through preview and customization steps.

See [Continuous Authorization and Monitoring](https://www.servicenow.com/docs/access?context=grc-cam-landing-page&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US) for more information.

</td></tr><tr><td>

Contract Management Pro

</td><td>

-   Send contracts for signature using Adobe Sign without having to sign in to the electronic signature portal.
-   Compare two revisions of the contract document and view the redlined compared document.
-   Initiate and manage amendment requests for existing contracts.
-   Generate summaries, FAQs, or retrieve specific information from contract documents, supporting documents, and signed contracts.
-   Link parent contracts during drafting and negotiation phases to inherit parent contract terms.
-   Pause and resume an in-progress signature process when updates to the signatory list are required.

See [Contract Management Pro](https://www.servicenow.com/docs/access?context=cncore-cmpro-landing-page&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Contract Management Pro for Legal Service Delivery

</td><td>

-   Initiate and manage amendment requests for existing contracts.
-   Record producer to initiate an amendment request from the Employee Center.

See [Contract Management Pro for Legal Service Delivery](https://www.servicenow.com/docs/access?context=snlc-mgmt-pro-landing-page&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Conversation Improvement Themes

</td><td>

-   Use automated theme detection with a domain-specific large language model \(LLM\) theme classification framework to tag Knowledge Base articles, catalog items, Virtual Agent \(VA\) topics, and agents into themes.
-   Receive thematic insights by breaking down poor and good-quality conversations into top underlying themes.
-   Compare themes based on whether they lead to good or bad conversations.

See [Conversation Improvement Themes](https://www.servicenow.com/docs/access?context=conv-impr-themes-landing&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US) for more information.

</td></tr><tr><td>

Conversation Insights

</td><td>

-   Augment conversations with insights based on the Inferred CSAT score. The Inferred CSAT framework provides an estimated score computed using AI in real time by analyzing the entire sequence of the conversation.
-   Use underlying factors like Resolution, Confusion, Effort, Empathy, Next Steps, Frustration, Transfers, and Escalations to provide explainability to the Inferred CSAT scores.
-   Leverage the Inferred CSAT framework and Conversation Insights \[sn\_aci\_insights\] table linked to the Conversation \[sys\_cs\_conversation\] table to create adhoc dashboards and workflows for conversational analytics applications.

See [Conversation Insights](https://www.servicenow.com/docs/access?context=conversation-insights&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US) for more information.

</td></tr><tr><td>

Creator Studio

</td><td>

-   Create customized email notifications that are sent by the apps that you build.
-   Add playbooks with a new activity that automatically updates some fields on the app's generated record.
-   Augment forms with the new Duration and Attachment question types.

See [Creator Studio](https://www.servicenow.com/docs/access?context=creator-studio-landing&version=zurich&pubname=zurich-application-development&ft:locale=en-US) for more information.

</td></tr><tr><td>

Customer Contracts and Entitlements

</td><td>

-   Initiate renewals from contracts at the contract or contract line level.
-   Add new line items to an existing contract.
-   Initiate modification from the contract header.
-   Add or reduce quantities on a contract line.
-   Define pricing and quantity schedules in contracts across specific time periods.

See [Customer Contracts and Entitlements](https://www.servicenow.com/docs/access?context=exploring-post-sales-support&version=zurich&pubname=zurich-order-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Customer Engagement Sequences

</td><td>

-   Design sequences to initiate workflows from multiple record-based events, with outcome-based decision nodes between stages, and runtime permissions.
-   Control access to various features and capabilities using the new granular roles.
-   Enable click-to-call for agents by configuring the Schedule Call activity and integrating with platforms such as Amazon Connect.
-   Automate and personalize customer journeys with a no-code playbook interface and guided task flows.
-   Drive high-impact telesales scenarios such as product surveys, lead qualification, and proactive engagement campaigns.

See [Customer Engagement Sequences](https://www.servicenow.com/docs/access?context=explore-customer-engagement-sequences&version=zurich&pubname=zurich-order-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Customer Service Problem Management

</td><td>

-   Run the diagnostics from the contextual panel in the Customer Service Problem Management playbook.
-   As an agent, use the Test group to help group test definitions. The Test group contains multiple test definitions.
-   Enables your customer to modify the visibility of the **Diagnose** tab and run diagnostics from the contextual panel in the Decisions table.

See [Customer Service Problem Management](https://www.servicenow.com/docs/access?context=cspm-landing-page&version=zurich&pubname=zurich-proactive-service-exp-workflows&ft:locale=en-US), [Setting up a test group](https://www.servicenow.com/docs/access?context=setting-test-group&version=zurich&pubname=zurich-proactive-service-exp-workflows&ft:locale=en-US), and [Setting up test definitions](https://www.servicenow.com/docs/access?context=settingup-test-specifications&version=zurich&pubname=zurich-proactive-service-exp-workflows&ft:locale=en-US) for more information.

</td></tr><tr><td>

Customer Success Management

</td><td>

-   Account Lifecycle Events has been renamed to Customer Success Management.
-   Enable managers to see a high-level aggregate view of their entire customer portfolio.
-   Monitor adoption scores for sold products and track implementation progress for customer engagements.
-   View the engagement hierarchy and timeline of events.
-   Use the new metrics data source to calculate metric values dynamically based on the weighted sums of other metrics.
-   View the detailed information of risk level records in the risk occurrence timeline.
-   The activity stream component displays a list of the activities occurring on a risk signal and issue record.
-   The **Related Items** tab provides access to the Risk Signal and Issue related lists.
-   Determine the engagement health score from the Calculated data source.
-   Retrieve data from internal and external tables with the Table type data source.

See [Customer Success Management](https://www.servicenow.com/docs/access?context=account-lifecycle-events-landing&version=zurich&pubname=zurich-acct-lifecycle-events&ft:locale=en-US) for more information.

</td></tr><tr><td>

Customer self-service for Sales and Order Management

</td><td>

-   Enable B2B customers to request for quotes \(RFQ\) from the Business Portal, improving customer autonomy and reducing sales cycle time.
-   Provide a persistent shopping cart experience to your B2B customers.
-   Enable your customers to download and share their cart summary with other stakeholders.
-   Provide seamless order checkout and an easy order creation process to your customers.

See [Self-Service for Sales and Order Management](https://www.servicenow.com/docs/access?context=som-self-service-business-portal&version=zurich&pubname=zurich-order-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Data Loss Prevention Incident Response

</td><td>

-   Improved response to Data Loss Prevention \(DLP\) incidents through the initiation of SLA triggers.
-   Introduced SLA Definition functionality that outlines the conditions and duration for responding to data breaches.
-   Configured DLP Proofpoint to generate Client ID and Client Secret to enable secure access to proofpoint.

See [Data Loss Prevention Incident Response](https://www.servicenow.com/docs/access?context=dlp-landing&version=zurich&pubname=zurich-security-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Data Management

</td><td>

-   View insights into storage consumption on your instance and manage data usage in the redesigned Data Management Console.
-   Monitor data usage in a logical table view.
-   View data usage for individual tables and their associated tables.
-   View a summary of the data management rules on a table.

See [Data Management](https://www.servicenow.com/docs/access?context=c_DataManagement&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US) for more information.

</td></tr><tr><td>

Data Management for CSM

</td><td>

-   Simplify your experience in viewing and applying protections to sensitive data by identifying, categorizing, and securing sensitive customer relationship management \(CRM\) data.
-   Streamline access management through an enhanced UI-based configuration, using the declarative framework enhancements in Customer Access Management \(CAM\).
-   Integrate Service Model Foundation with Order Management and Quote Management to enable enterprises to track orders and quotes that are generated by channel partners.
-   Add pricing fields based on sales agreements to capture base prices for sold products and verify consistent pricing.
-   Improve traceability with serial numbers on Install Base items and direct links to model categories for industry-specific configurations.
-   Enable partial sync using `allowedContextTypes` to sync specific sections with preserved structure and recursive filtering, and deliver clear, actionable error messages with consistent API responses.

See [Data management for Customer Service Management](https://www.servicenow.com/docs/access?context=csm-data-management&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US) feature for more information.

</td></tr><tr><td>

Data Privacy

</td><td>

-   Use a revamped Data Discovery interface, enhancing your Data Discovery experience with intuitive widgets, a streamlined user experience, and a guided setup for first-time users.
-   Target scans on specific table columns for discovery using column-level discovery and expanded support for Field Encryption.
-   Discover PII in Microsoft Excel and CSV files with expanded file support.
-   Generate regex patterns using prompts with the text-to-regex feature, which leverages Now Assist and supports all large language models \(LLMs\) approved by ServiceNow.

See [Platform Privacy](https://www.servicenow.com/docs/access?context=privacy-landing-page&version=zurich&pubname=zurich-platform-security&ft:locale=en-US) for more information.

</td></tr><tr><td>

DevOps Change Velocity

</td><td>

-   Improve instance efficiency by skipping step-level pipeline processing.
-   Improve load balancing and failover protection by selecting a MID Server cluster during tool connection.

See [DevOps Change Velocity](https://www.servicenow.com/docs/access?context=devops-landing-page-new&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Developer Sandboxes

</td><td>

-   Enable your administrators and delegated developers to request, access, and manage the isolated development environments on top of the same underlying development instance.
-   Provide developer isolation and parallelism for customer development environments and instances.
-   View the total, available, and allocated sandboxes in your instance by using the Sandbox Management home dashboard. The dashboard also displays information about each sandbox, including the status, data utilization, owner, when it was last accessed, and when the sandbox was allocated.

See [Developer Sandboxes](https://www.servicenow.com/docs/access?context=sandboxes-landing&version=zurich&pubname=zurich-application-development&ft:locale=en-US) for more information.

</td></tr><tr><td>

Digital End-User Experience

</td><td>

-   Track and analyze call performance for a particular user in Microsoft Teams with DEX for Microsoft 365.
-   View the consolidated alerts related to devices and applications in the Alerts section of the Device health page.
-   View the new DEX landing page, which includes an updated Devices world map and an enhanced Impacted Devices card.
-   View real-time data for alerts, change requests, and incidents that are impacting a device in the Device events section of the Device health page.
-   Create a remedial action from a check definition, link an existing remedial action to a check definition, and execute a remedial action on multiple impacted devices for a DEX alert simultaneously.
-   Manage device and application configurations and monitor key DEX components in the new DEX Administration workspace.
-   Gain deeper visibility into performance with enhanced metrics analysis and non-persistent Virtual Desktop infrastructures \(VDIs\) monitoring, including device, application, and web page insights for faster troubleshooting.
-   Use the Metrics analyzer to view metrics collected for a given device or application during a specific period.
-   Monitor non-persistent VDIs with Digital End-User Experience \(DEX\) to track performance issues and troubleshoot efficiently.
-   Gain insights into Zoom call quality and Zoom rooms performance across your organization with DEX for Zoom.
-   Empower service desk agents to diagnose and resolve incidents on DEX monitored devices quickly and efficiently by using the  DEX issue diagnosis and resolution agentic AI workflow.
-   Enable service desk agents to diagnose and resolve issues on DEX monitored devices directly from the Investigation tab in incident records within the Service Operations Workspace.

See [Digital End-User Experience](https://www.servicenow.com/docs/access?context=dex-landing&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Digital Portfolio Management \(DPM\)

</td><td>

-   Configurable Info tab allows customers to configure the Info tab of the solutions pages, similarly to how they can configure the Plan, Build, and Run tabs.
    -   This includes showing or hiding sections of the tab.
-   DPM users with the dpm\_admin role can now create and edit portfolios directly within DPM, and three portfolio templates are included \("EDUCAUSE", "IT Service Portfolio", and "Sample Organization Structure"\).
-   DPM users can now send an email to any users with the dpm\_manager role that includes the first key performance indicator \(KPI\) group data and a link back to the solution they're sending an email from.
    -   This feature is off by default and can be activated in the DPM Admin Center under a new 'Email properties' section.
-   DPM admins can turn on a scheduled job that will automatically send the top KPI group data in an email to the solution owners.
    -   The schedule is configurable and will only send KPI data for the 'top level objects' that a user owns. For example, if they own a taxonomy node, it won't send data on sub nodes or services.
    -   DPM users can now view more than one KPI group in the Enterprise Portfolio preview.
-   DPM users with the dpm\_admin role can use the Active flag to hide or show the portfolio and taxonomy node branches in the Enterprise Portfolio Module.
    -   DPM admins can set an enterprise portfolio's **Status** to Active or Inactive.
    -   DPM managers will only see enterprise portfolios that are active.

See [Digital Portfolio Management](https://www.servicenow.com/docs/access?context=dpm-landing&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Dispute Rules Content Pack for Mastercard

</td><td>

-   Developed and refined chargeback eligibility rules to validate dispute cases against Mastercard core rules.
-   Updated the intake questionnaire for various dispute categories.

See [Dispute Rules Content Pack for Mastercard](https://www.servicenow.com/docs/access?context=dispute-rules-content-pack-for-mastercard-landing-page&version=zurich&pubname=zurich-financial-services-operations&ft:locale=en-US) for more information.

</td></tr><tr><td>

Dispute Rules Content Pack for Nacha

</td><td>

-   Run chargeback eligibility rules and derive ACH dispute categories and reason codes based on Nacha guidelines.
-   Determine chargeback eligibility using an integrated KB article that contains rules and conditions.

See  for more information.

</td></tr><tr><td>

Dispute Rules Content Pack for Visa

</td><td>

Applied Visa Resolve Online \(VROL\) release 25.2 revision changes to Dispute Rules Content Pack for Visa questionnaire.

See [Dispute Rules Content Pack for Visa](https://www.servicenow.com/docs/access?context=dispute-rules-content-pack-for-visa-landing-page-1&version=zurich&pubname=zurich-financial-services-operations&ft:locale=en-US) for more information.

</td></tr><tr><td>

Document Intelligence

</td><td>

-   Use Google Gemini and Anthropic Claude on AWS as AI model providers for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.

See [Document Intelligence](https://www.servicenow.com/docs/access?context=document-intelligence-landing&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US) for more information.

</td></tr><tr><td>

Document Services

</td><td>

-   Compare any two document versions and track changes by using document comparison.
-   Connect and manage external cloud documents by uploading files, storing URLs, and syncing metadata with your records.
-   Authenticate with your personal accounts on an external cloud, Microsoft OneDrive, or Google Drive.
-   Control public sharing by using document classification to ensure document security.
-   Accelerate documents insights with instant summaries for highlights and quick insights, interactive Q&amp;A, and FAQs.

See [Document Services](https://www.servicenow.com/docs/access?context=document-services-landing-page&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US) for more information.

</td></tr><tr><td>

Domain Separation

</td><td>

-   Changes to the domain table are queued sequentially and batched into a single background job. This helps simplify domain table updates.
-   Domain Admins can delete by domain to efficiently manage domains and reduce storage overhead.

See [Domain separation for service providers](https://www.servicenow.com/docs/access?context=domain-sep-landing-page&version=zurich&pubname=zurich-platform-security&ft:locale=en-US) for more information.

</td></tr><tr><td>

Dynamic Translation

</td><td>

With the new Test Exclusion Rule module you can check what your exclusion pattern matches during a test translation, then create an exclusion rule based on the pattern you tested.

See [Dynamic Translation](https://www.servicenow.com/docs/access?context=dynamic-translation-overview&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US) and [Exclusion Framework in Dynamic Translation](https://www.servicenow.com/docs/access?context=dyn-translation-exclusion-framework&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US) for more information.

</td></tr><tr><td>

ERP Semantic Mining

</td><td>

The name of the ERP Customization Mining application has been changed to ERP Semantic Mining.

See [ERP Semantic Mining](https://www.servicenow.com/docs/access?context=erp-customization-mining-overview&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US) for more information.

</td></tr><tr><td>

Employee Center

</td><td>

[Zurich Patch 1](../quality/zurich-patch-1.md)

-   Enable employees to check their latest company news and upcoming events using Now Assist in Virtual Agent with the **Company News &amp; Events AI Agent** in the Now Assist for Employee Experience. The AI Agent displays a list of all the latest news and planned events in the company. For more information, see [Check latest company news and events](https://www.servicenow.com/docs/access?context=check-company-newsevent-ai-agent-for-emp-exp&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US).
-   Employees can check all their to-do tasks and pending approvals using Now Assist in Virtual Agent for Microsoft Teams.
-   Enable a summary of the request, requested item, or case for approval task using Now Assist for Employee Experience. The skill provides a summary of the selected item from the available list that you want to work on. For more information, see [Now Assist for Employee Experience Summarization skill](https://www.servicenow.com/docs/access?context=activate-now-assist-skills-uex&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US).

Zurich Early Availability

-   Use the Now Assist for Employee Experience application so that your employees can have a seamless conversational interaction with Now Assist in Virtual Agent.
-   View and manage content and other company resources through the Browser Extension for Employee Center.
-   Improve the My Requests experience with adoptive and scalable enhancements.

See [Employee Center](https://www.servicenow.com/docs/access?context=employee-center-landing-page&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Employee Center Pro

</td><td>

-   Configure features flexibly and submit detailed feedback using enhancements for the Integrated experience and Service feedback.
-   Get the Notifications in Employee Center feature in Content engagement for improved employee involvement while engaging with news content.
-   Experience an enhanced performance with improvements to calender widgets, news and events, and publishing communications to browser websites.

See [Employee Center Pro](https://www.servicenow.com/docs/access?context=employee-center-pro-landing&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Encryption

</td><td>

-   Use row conditions for Field Encryption to define encryption rules for rows within a specific column, based on dynamic conditions.
-   Use any of the three Field Encryption APIs to encrypt attachments.

See [Encryption](https://www.servicenow.com/docs/access?context=encryption-landing&version=zurich&pubname=zurich-platform-security&ft:locale=en-US) for more information.

</td></tr><tr><td>

Encryption Key Management

</td><td>

-   See the changes to the Key Management and Field Encryption records that are now logged on the Sys Audits \[sys\_audit\] table.
-   The GlideEncrypter API has been updated and now uses AES256-GCM encryption via the Key Management Framework.
-   Enable or disable GlideEncrypter by using the **glide.security.glideencrypter.allow** system property.

See [Key Management Framework](https://www.servicenow.com/docs/access?context=encryption&version=zurich&pubname=zurich-platform-security&ft:locale=en-US) for more information.

</td></tr><tr><td>

Enterprise Architecture

</td><td>

-   Define and track data certifications using the Data Certification workflow in the Enterprise Architecture Workspace to ensure the accuracy, completeness, and reliability of critical data within your organization.
-   Design the future-state cloud modeling using the standardized AWS components in the Enterprise Modeling and Visualization to reflect AWS infrastructure and services.
-   Perform end-to-end modeling with full alignment to CSDM \(Common Service Data Model\)5.0 standards including standardized shapes, colors, and relationships.
-   Group business application bubbles on the Application Rationalization Bubble chart page whose X and Y-axis values are within the value range of +/-0.25 of each other.
-   Export the TRM catalog data and Business Portfolio data to Microsoft Excel or CSV format.
-   Apply filters to the Application Rationalization bubble chart and list views pages, using the new filter options to filter for specific business applications. Also, select a fiscal period on the Application Rationalization pages using the new fiscal period filter option.
-   Evaluate the technical debt score for business applications using the Technology Reference Model \(TRM\) technical debt indicator. This helps you to identify high-risk business applications and enables you to prioritize modernization and rationalization.

See [Enterprise Architecture \(formerly Application Portfolio Management\)](https://www.servicenow.com/docs/access?context=application-portfolio-management-landing-page&version=zurich&pubname=zurich-application-portfolio-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Enterprise Asset Management

</td><td>

-   Organize related assets into hierarchical asset groups and subgroups to enable consolidated reporting, streamline maintenance workflows, and provide clear dependency mapping.
-   Create scalable templates to evaluate the condition of enterprise assets, which helps to detect issues early, optimize maintenance planning, and maximize asset lifespan.
-   Achieve operational efficiency by evaluating how effectively your assets are functioning and being used, through reports based on asset key performance indicators in the Asset analytics view.
-   Manage supply and demand originating from service locations or other stockrooms through local stock or distribution channels using the Inventory insights tab in the stockroom record. You can also compare multiple stockrooms at the same time.
-   Gain insights into asset failure reasons and resolution actions using the failure and resolution codes in the Enterprise Asset Workspace.

See [Enterprise Asset Management](https://www.servicenow.com/docs/access?context=enterprise-asset-management&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Event Management

</td><td>

-   Combine the strengths of CMDB-based and tag-based strategies to create mixed alert groups that reduce noise and reveal clearer, actionable insights.
-   Effortlessly extract event field content into alert fields with automated regex generation, reducing manual effort and improving accuracy.
-   Gain actionable insights with AIOps 360-degree overview dashboard to showcase product value.
-   Accelerate integration setup with seamless installation via the Unified Launchpad store app, guided support for creating integrations, and enhanced observability with the new Service Observability filter.

See [Event Management](https://www.servicenow.com/docs/access?context=c_EM&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US) or [Service Operations Workspace for ITOM](https://www.servicenow.com/docs/access?context=sow-landing-page-itom&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

External Content Connectors

</td><td>

[Zurich Patch 7](../quality/zurich-patch-7.md)

-   Expand your search experience with external content connectors for Adobe Acrobat Sign, Aha! Roadmaps, Cornerstone, Fluid Topics, ManageEngine, and Workvivo source systems.
-   Retrieve content and links from URLs found in sitemaps defined for your web source system when running content crawls for the Webcrawler external content connector.
-   View a content crawl's start point via links in the content crawl list and in content crawl history entries.

[Zurich Patch 4](../quality/zurich-patch-4.md)

-   Expand your search experience with external content connectors for Adobe Experience Manager as a Cloud Service, Asana, Docusign, Dropbox, GitHub Enterprise Cloud, HubSpot, Lucidchart, Miro, monday.com, Notion, SAP DMS, Smartsheet, Trello, WordPress, Workday, and Zoom source systems.
-   Customize user permission settings, choosing the fields you want to compare when mapping source system users to ServiceNow AI Platform® users.
-   Make external content connector crawl results searchable by linking connector search sources to search profiles from the connector editor.
-   Monitor connector behavior on individual crawl runs and over time with improved crawl statistics and analytics.

[Zurich Patch 1](../quality/zurich-patch-1.md)

-   Expand your search experience by indexing searchable content from your Amazon S3, Box, GitLab, Microsoft OneDrive, Microsoft Viva Engage, and Zendesk Guide source systems.
-   Search KB articles from your ServiceNow instance.
-   Make web content locally searchable by indexing pages from predefined or custom public web sites with the Webcrawler external content connector.
-   Configure connector settings and schedule crawls as part of connector creation using the revamped UI.

See [External Content Connectors](https://www.servicenow.com/docs/access?context=ext-cont-connectors-landing-page&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US) for more information.

</td></tr><tr><td>

Field Service Management

</td><td>

-   Use the aggregated agent schedule to optimize the allocation of resources for a territory up to the specified cut-off date.
-   Flag a task or use assignment assistance directly from the Work Order Task page to streamline task management.
-   Configure Schedule Optimization to instantly adjust technician schedules in response to real-time events, like new priority 1 tasks, task cancellations, paid time off requests, or delays.

See [Field Service Management](https://www.servicenow.com/docs/access?context=fsm-application-landing-page&version=zurich&pubname=zurich-field-service-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Field Service Management for Telecommunication

</td><td>

Manage your work order using the TMF 697 Open API.

See [Field Service Management for Telecommunications](https://www.servicenow.com/docs/access?context=field-service-management-telecommunications&version=zurich&pubname=zurich-telecom-media-technology&ft:locale=en-US) for more information.

</td></tr><tr><td>

Financial Services Card Operations

</td><td>

-   Resolve disputes with a new dispute life cycle for Mastercard dispute transactions.
-   Leverage a new workspace page in Financial Services Card Operations to resolve Mastercard disputes.
-   Integrate Mastercard's Mastercom APIs into the Dispute Management workflow to resolve card disputes faster and more efficiently.
-   Resolve ACH disputes faster with a guided, end-to-end workflow that unifies intake, investigation, and resolution—built on a framework ready for any non-card transaction.
-   Streamline operations with a single, consistent intake process that applies across all dispute workflows.

See [Overview of the Dispute Management workflow](https://www.servicenow.com/docs/access?context=dispute-management-workflows&version=zurich&pubname=zurich-financial-services-operations&ft:locale=en-US) for more information.

</td></tr><tr><td>

Financial Services Operations Core

</td><td>

-   Leverage a payment card data model application in FSO workflows, such as disputes, which can be used across an entire card life cycle, from issuance to servicing.
-   Support multiple payment card types, including credit and debit cards.

See [Payment card](https://www.servicenow.com/docs/access?context=payment-card-application&version=zurich&pubname=zurich-financial-services-operations&ft:locale=en-US) for more information.

</td></tr><tr><td>

Financial Services Operations Integration with Mastercard

</td><td>

-   Enable dispute agents to efficiently handle the full dispute life cycle, including transaction searches, claim creation, chargeback creation and updates, pre-arbitration, arbitration, and fraud reporting.
-   Accelerate dispute resolution and reduce manual effort using predefined subflows.

See [Financial Services Operations Integration with Mastercard](https://www.servicenow.com/docs/access?context=financial-services-operations-integration-with-mastercard-landing-page&version=zurich&pubname=zurich-financial-services-operations&ft:locale=en-US) for more information.

</td></tr><tr><td>

Financial Services Operations Integration with Visa

</td><td>

ِEnable system administrators to control settings for features in the Financial Services Operations Integration with Visa application, such as, integration with specific APIs.

See [Financial Services Operations Integration with Visa](https://www.servicenow.com/docs/access?context=financial-services-operations-integration-with-visa-landing-page&version=zurich&pubname=zurich-financial-services-operations&ft:locale=en-US) for more information.

</td></tr><tr><td>

Flows, subflows, and actions in Workflow Studio

</td><td>

-   Create a scheduled trigger that you can use across your flows.
-   Save flows, subflows, and actions automatically as you work on them.
-   View and manage the history of flows and subflows to copy, restore, or remove past configurations.
-   Create multiple skills for conversational subflows and actions from the conversational settings.
-   Configure a default LLM for generating metadata for conversational subflows and actions.

See [Exploring flows](https://www.servicenow.com/docs/access?context=exploring-flows&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US), [Exploring subflows](https://www.servicenow.com/docs/access?context=exploring-subflows&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US), and [Exploring actions](https://www.servicenow.com/docs/access?context=exploring-actions&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US) for more information.

</td></tr><tr><td>

Generative AI Controller

</td><td>

[Zurich Patch 8](../quality/zurich-patch-8.md)

-   Connect your Azure OpenAI deployment to Generative AI Controller by configuring a custom resource path in your bring your own key \(BYOK\) model configuration.

[Zurich Patch 5](../quality/zurich-patch-5.md)

-   Review changes to Now Assist usage measurement.

[Zurich Patch 4](../quality/zurich-patch-4.md)

-   Access the Gen AI log for debugging insights, with HR-related records remaining restricted.
-   Promote stability with the Long-Term Stable \(LTS\) model for generative AI.

-   Identify third-party LLM information, including model, version, and language.
-   Restrict LLM usage based on domain.

See [Generative AI Controller](https://www.servicenow.com/docs/access?context=generative-ai-controller&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US) for more information.

</td></tr><tr><td>

Goal Framework

</td><td>

-   Categorize your strategic priorities and goals as Artificial Intelligence to track and monitor their progress from the AI Control Tower workspace.
-   View only active goals in reference fields when creating a goal relationship or defining a parent goal.

See [Goal Framework](https://www.servicenow.com/docs/access?context=goal-framework&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Goal Framework for SPM

</td><td>

Use the sn\_gf\_goal\_admin role to update the goal-specific system properties.

See [Goal Framework for SPM](https://www.servicenow.com/docs/access?context=goal-framework&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

HR Multi Instance Integration

</td><td>

-   Collaborate with service providers and consumers through bidirectional workflows.
-   Increase the security of records in consumer instances and provider instances by limiting access based on user roles.
-   Enable an employee to place an HR service request from a consumer instance and fulfill the request from provider instance, making it easy to raise and fulfill HR requests while working in their own ServiceNow instance.
-   Create HR tasks, approval tasks, and document tasks from a provider instance for users in a consumer instance.
-   Enable consumer users to complete the assigned tasks via magic links. Magic links enable consumer users to directly access the linked resource in the provider instance without having to manually log in.
-   Use Universal Task as the remote tasking medium in both provider instance and consumer instance.

See [HR Multi Instance Integration](https://www.servicenow.com/docs/access?context=multi-instance-int&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Hardware Asset Management

</td><td>

-   Benefit from enhanced Asset Attestation features, including a guided attestation creation process, a mobile-friendly interface for confirming assets, and automated remediation tasks to address non-compliant assets.
-   Achieve real-time tracking of assets that are in transit and maintain asset data accuracy by enabling employees to confirm receipt of assets through the Employee Center portal.
-   Receive shipment assets at a stockroom from any workflow through the streamlined and unified receiving process.
-   Track asset movement from the receiving bay to an aisle and space in the stockroom using the Asset put away task.
-   Evaluate how effectively your assets are functioning and being used through reports based on asset key performance indicators in the Asset analytics view. Also, manage supply and demand in your stockrooms effectively with inventory demand reports.

See [Hardware Asset Management](https://www.servicenow.com/docs/access?context=ham-landing-page&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Health Log Analytics

</td><td>

-   Use the Cribl integration to streamline Health Log Analytics data ingestion with Cribl.
-   Leverage additional information presented on the integration's Overview screen, such as the ITOM Gateway in the processing pipeline and the log streaming rate per minute.
-   Map log data to service instances and components for alerts in context.
-   Monitor ServiceNow instance logs with the ServiceNow Log Export data input.

See [Health Log Analytics](https://www.servicenow.com/docs/access?context=hla-landing-page&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Healthcare Operations Core

</td><td>

-   Leverage the streamlined launch context when embedding Care Team Portal into electronic medical record \(EMR\) systems.
-   Assign roles and responsibilities more efficiently with an updated user configuration process.

See [Healthcare Operations Core](https://www.servicenow.com/docs/access?context=hcls-cto-app&version=zurich&pubname=zurich-healthcare-life-sciences&ft:locale=en-US) for more information.

</td></tr><tr><td>

Hermes Messaging Service

</td><td>

-   Monitor Hermes data usage over time.
-   Verify that topics are synchronized between Hermes clusters.

See [Hermes Messaging Service](https://www.servicenow.com/docs/access?context=hermes-messaging-service&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US) for more information.

</td></tr><tr><td>

Hiring

</td><td>

-   Manage all your hiring needs efficiently with a seamless unified experience.
-   Track job requisitions and applications and save the time required to hire with an intuitive hiring flow.
-   Effortlessly collaborate with the recruiters to speed up the hiring process.
-   Get a unified overview of your responsibilities with clear insights into what needs your attention and when.

See [Hiring](https://www.servicenow.com/docs/access?context=hiring-tab-concept&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

ITOM AIOps

</td><td>

Health Log Analytics highlights:

-   Streamline Health Log Analytics data ingestion with Cribl by using the Cribl integration.
-   Leverage additional information presented on the integration's Overview screen, such as the ITOM Gateway in the processing pipeline and the log streaming rate per minute.
-   Map log data to service instances and components for alerts in context.
-   Monitor ServiceNow instance logs with the ServiceNow Log Export data input.

[Service Operations Workspace for ITOM](https://www.servicenow.com/docs/access?context=sow-landing-page-itom&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US) highlights:

-   Control how alerts are grouped, which ones are included, and the order of grouping methods through Mixed Alert Grouping, which combines CMDB-based and tag-based strategies.
-   Starting in version 26.9.0, investigate mixed alert groups and Log Analytics-based alert groups by using Express List®.
-   Starting in version 26.9.0, view connections between alerts in Link View for mixed alert groups and Log Analytics-based alert groups.

See [ITOM AIOps](https://www.servicenow.com/docs/access?context=itom-health-landing-page&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

ITOM Cloud Accelerate

</td><td>

-   Ability to monitor, track, and analyze cloud assets across providers in Cloud Account Management.
-   Compliance visibility and account insights in Cloud Account Management.
-   Improved asset-level filtering and visualization in Cloud Account Management.
-   Ability to view cloud assets and access detailed information about associated configuration items \(CIs\).
-   Migrated legacy workflows to subflows in Cloud Provisioning and Governance.

See [Cloud Governance](https://www.servicenow.com/docs/access?context=cloud-governance&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

ITOM Visibility

</td><td>

-   Cloud-based scheduling available in Discovery Admin Workspace \(store version 1.11.0\).
-   AWS EC2 VMs discovery using AWS Systems Manager \(SSM\).
-   Tag-based Service Mapping experience in the Service Mapping Workspace \(store version 1.16.3\).
-   Application service maps for containers via Kubernetes Visibility Agent \(KVA\) \(store version 3.11.0\).
-   25 cloud patterns shipped via Discovery and Service Mapping Patterns \(store version 1.28.0\)
-   Certificate Inventory and Management TLS Certificate request flows that support Keyfactor EJBCA \(store version 3.7.0\) and Certificate Inventory and Management Automated TLS Certificate renewal workflows \(store version 3.8.2\).

See [IT Operations Management](https://www.servicenow.com/docs/access?context=r_ITOMApplications&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Identity

</td><td>

[Zurich Patch 4](../quality/zurich-patch-4.md)

-   Configure AI Agents or AI users by selecting the `AI` option from the **Identity type** drop-down menu.
-   Use the `ai_user_admin` role for creating, editing, and role management of AI users. Using the role you can view, create, edit, assign roles to, and delete users with the identity type as `AI`.
-   Use role masking for AI agents and agentic workflows to limit the inherited roles during tool execution, verifying that AI agents run with restricted privileges, minimizing potential security risks and helping prevent unintended actions. To learn more, see [Role masking in Now Assist AI agents](https://www.servicenow.com/docs/access?context=aia-role-masking&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).
-   Access Analyzer v.6 supports agentic workflows and AI agents in the Analyze Permissions feature.

**Important:** Access Analyzer is available in the ServiceNow Store. For more information, visit [ServiceNow Store](https://store.servicenow.com/store).

-   Use Federated ID to uniquely identify roles across multiple instances. Federated ID provides a unique identifier for roles, making it easier to manage and track them across instances. To know more, see [Explore Federated ID](https://www.servicenow.com/docs/access?context=federated-id&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).
-   View the Inbound API Integration Usage dashboard under the Machine Identity Console's Unique API calls page to access statistics for requestors and their API calls. To know more, see [Metrics](https://www.servicenow.com/docs/access?context=machine-identity-metrics&version=zurich&pubname=zurich-platform-security&ft:locale=en-US) and [View Inbound API Integration Usage dashboard](https://www.servicenow.com/docs/access?context=view-inbound-api-integration-usage-dashboard&version=zurich&pubname=zurich-api-reference&ft:locale=en-US).

Zurich

-   Manage your non-human identities \(NHIs\) using the Machine Identity Console.
-   Support security data filter functionality in Applied or Undefined status and Controlled by Refs functionality during access control list \(ACL\) query.

**Important:** Access Analyzer is available in the ServiceNow Store. For more information, visit [ServiceNow Store](https://store.servicenow.com/store).


See [Identity](https://www.servicenow.com/docs/access?context=identity-landing&version=zurich&pubname=zurich-platform-security&ft:locale=en-US) for more information.

</td></tr><tr><td>

Impact

</td><td>

-   Manage health checks, findings, and remediation workflows with AI-powered tools directly on-platform to accelerate insights and remediation with the new Platform Health Scan Engine for the Impact Store Application.
-   Use the automated setup method to simplify the Impact Store Application configuration.
-   Deploy the AI Control Tower Accelerator to help customers configure governance for AI investments and demonstrate strategic value.

</td></tr><tr><td>

Incident Management

</td><td>

-   Help prevent changes to closed incident tasks to promote data integrity and to maintain a clear audit.
-   Manage and resolve incidents effectively with the incident and problem workflow enhancements.
-   Coral is the new default theme for Next Experience and Core UI, offering a more user-friendly experience.

See [Incident Management](https://www.servicenow.com/docs/access?context=c_IncidentManagement&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Industrial Process Manager

</td><td>

-   View both unmapped and all Operational Technology \(OT\) devices in separate tabs while mapping them to equipment model entities for an organized view of your OT devices.
-   Visualize your OT network using the OT Network Map.
-   Automatically create a location for equipment model entities to visualize your location hierarchy.
-   Use the updated Automated Mapping Across Zone-based IP Network Groups \(AMAZING\) feature to uniquely identify OT devices during equipment model entity mapping.
-   Identify sites on your equipment model entity that aren't in use with a new **Operational Status** field value in the Industrial Workspace.
-   Filter out **Not in use** or **Retired** equipment model entities in the Industrial Workspace using the **Operational Status** field value.
-   Sort equipment model entities for a Site using the new value **Processing Order**.
-   View the **Daily Activity** tab for a summarized version of the previous day's activities on the Operational Technology \(OT\) devices.

See [Industrial Process Manager](https://www.servicenow.com/docs/access?context=industrial-process-manager-overview&version=zurich&pubname=zurich-operational-technology&ft:locale=en-US) for more information.

</td></tr><tr><td>

Instance Data Replication

</td><td>

-   Monitor the progress of all your scheduled replication sets.
-   Track the progress of scheduled replication requests within a scheduled replication set.
-   Access details of scheduled replication requests within a scheduled replication set.

See [Instance Data Replication](https://www.servicenow.com/docs/access?context=instance-data-replication&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US) for more information.

</td></tr><tr><td>

Instance Scan

</td><td>

-   Scan your instance, update set, scoped application, or specific record using specified checks.
-   Run custom checks against your existing configurations.
-   Use as a tool in your development operations, release management, as well as pre- and post-upgrades.

See [Instance Scan](https://www.servicenow.com/docs/access?context=hs-landing-page&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US) for more information.

</td></tr><tr><td>

Integration Hub

</td><td>

-   Streamline the setup process for REST-based Data Stream actions by automatically generating the parsing and output components.
-   Use load-balancing MID Server clusters in Stream Connect message replication.
-   Enable testing of connection aliases directly from configuration templates.

See [Integration Hub](https://www.servicenow.com/docs/access?context=integrationhub&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US) for more information.

</td></tr><tr><td>

Intelligence for CSM

</td><td>

-   Get enhanced visibility of knowledge base articles by marking and displaying a lock icon for articles that aren’t accessible to the case requester within the CSM Configurable Workspace.
-   Gain insights to the root causes of case service level agreement \(SLA\) breaches and view the suggested improvements to optimize process performance.

See [Intelligence for CSM](https://www.servicenow.com/docs/access?context=intelligence-csm&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Interview management

</td><td>

-   Save time by using structured workflows to schedule and manage interviews.
-   Configure interview phases and use them to schedule interviews in a more organized and planned manner, minimizing manual effort and inconsistency.
-   Schedule interviews using workflows that support both self-scheduling and direct scheduling options. Consider multiple data sources, including calendar availability and declared scheduling preferences, to minimize rescheduling and eliminate off-platform coordination. Monitor interview health centrally to manage all interviews efficiently, with built-in reminders and notifications keeping everyone informed.
-   Manage interviews by updating statuses, viewing or providing feedback, sending reminders, and rescheduling, completing, or canceling interviews as needed.
-   Streamline feedback sharing and tracking, enabling hiring managers to effectively compare applications.

See [Recruitment workspace](https://www.servicenow.com/docs/access?context=recruitment-workspace-concept&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Journey designer

</td><td>

-   Usability enhancements:
    -   Use the option to cancel Journey Accelerator journeys from the portal.
    -   See higher performance in sync between the **Opened for** and **Journey Owner** fields.
    -   Configure the Journey overview page using the widgets option to hide or show Task Templates and Create a Journey for Your Team widgets.
-   The pre-hire onboarding experience enables a seamless journey for an applicant transitioning from an onboarding pre-hire to a full-time employee.

See [Journey Designer](https://www.servicenow.com/docs/access?context=jny-dsgnr-landing-page&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Knowledge Center

</td><td>

-   Use Knowledge Center to manage and distribute organizational knowledge through a centralized and organized interface.
-   Enhance productivity, reduce redundant work, and help ensure that users have access to the latest and most accurate information.
-   Format your content within a knowledge article using editing tools in the article editor.
-   Improve the quality and health of knowledge articles with article optimization, ensuring that the information is latest and relevant.

See [Knowledge Center](https://www.servicenow.com/docs/access?context=knowledge-center&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US) for more information.

</td></tr><tr><td>

Knowledge Graph

</td><td>

[Zurich Patch 5](../quality/zurich-patch-5.md)

-   Review changes to Now Assist usage measurement.

[Zurich Patch 4](../quality/zurich-patch-4.md)

-   Users can use the new Enterprise Graph Knowledge Graph schema to map all instance tables and their relationships, enabling natural language queries across the entire database. It simplifies setup by eliminating custom schema creation and supports enhanced query accuracy.
-   Admins can create and use tags to prioritize relevant tables for specific use cases.
-   Users have the option to select Enterprise Graph\(small\) mode to restricts queries to tables in specified tags for narrower use cases, improving runtime speed and requiring tag specification.
-   Knowledge Graph now supports aggregate queries.

[Zurich Patch 2](../quality/zurich-patch-2.md)

-   Admins can create Knowledge Graph schema with Workflow Data Fabric tables that enables users to retrieve data from different systems without moving them. This ensures efficiency and security when working with external tables. This enables Knowledge Graph functionality to external tables

[Zurich Patch 1](../quality/zurich-patch-1.md)

-   Supports nodes from parent and grandparent nodes in the hierarchy.
-   Supports Configuration Management Database \(CMDB\) queries in Now Assist panel.

Zurich EA

-   Use Google Gemini and Anthropic Claude on AWS as AI model providers for Knowledge Graph in addition to Now LLM Service and Azure OpenAI.
-   Select your preferred large language model \(LLM\) provider for Now Assist platform. Apart from Now LLM Service, the platform supports Azure OpenAI GPT-4.1 and GPT-4.1 mini, Google Gemini 2.0 Flash and 2.5 Pro, and AWS Anthropic Claude 3.7 Sonnet LLM providers with ServiceNow® third-party model strategy.

See [Knowledge Graph](https://www.servicenow.com/docs/access?context=knowledge-graph-landing&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US) for more information.

</td></tr><tr><td>

Knowledge Management

</td><td>

-   Experience seamless navigation and viewing experiences across various devices, with the incorporation of responsive design in the workspace that enables pages to adapt to different screen sizes and orientations.
-   Upgrade your Knowledge and article viewing experience with an enhanced view and access to key components on the workspace.
-   Enhance operational efficiency with migration from legacy Knowledge Management workflows to the latest low-code flow designers.

See [Knowledge Management](https://www.servicenow.com/docs/access?context=knowledge-management&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US) for more information.

</td></tr><tr><td>

Lead-to-Cash Process Management

</td><td>

-   Define and monitor sales entities tied to specific business processes such as order-to-cash. You can add custom processes and related entities managed in disparate ERP systems using a unified view in a node map.
-   Optimize revenue recognition and drive operational efficiency throughout the order-to-cash process by tracking key milestones, identifying potential delays early, and ensuring on-time delivery.

See [Lead-to-Cash Process Management](https://www.servicenow.com/docs/access?context=explore-lead-cash-process-management&version=zurich&pubname=zurich-order-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Legal Conflict of Interest

</td><td>

Disclose conflicts of interest using natural language from Now Assist in Virtual Agent rather than having to fill out intake forms. The risk assessment utility then automatically evaluates each submission and routes it to the appropriate approval workflow, enabling faster resolution.

See [Legal Conflict of Interest](https://www.servicenow.com/docs/access?context=legal-conflict-of-interest-landing-page&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Legal Hold Notification

</td><td>

-   Streamlined legal hold life cycle: Streamline the legal hold workflow by enabling you to create legal hold matters, assign custodians, issue notices, track acknowledgments, and ensure compliance throughout the process.
-   Enhance custodian engagement by sending them legal hold notifications and reminders to ensure timely acknowledgment and accountability throughout the legal hold process.
-   Reduce legal risk compliance with a controlled closure process. When the legal hold is officially closed, the Legal Hold Notification application stores detailed information about the preserved data.

See [Legal Hold Notification](https://www.servicenow.com/docs/access?context=lg-hold-notif-landing-page&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Legal Matter Management

</td><td>

Help ensure that sensitive information remains confidential with stakeholder controls through attorney-client privilege \(ACP\) protection for legal requests and matters.

See [Legal Matter Management](https://www.servicenow.com/docs/access?context=legal-matter-management-landing-page&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Legal Request Management

</td><td>

Help ensure that sensitive information remains confidential with stakeholder controls through attorney-client privilege \(ACP\) protection for legal requests and matters.

See [Legal Request Management](https://www.servicenow.com/docs/access?context=legal-request-management-landing-page&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Lifecycle Events

</td><td>

-   Enable logging and use it as a tool to diagnose problems or to acquire pertinent information about the processes that ran in a Lifecycle Events case.
-   Effectively troubleshoot the root cause of an issue that is adversely affecting a Lifecycle Events case.

See [Lifecycle Events](https://www.servicenow.com/docs/access?context=hr-lifecycle-events-landing-page&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Localization Workspace

</td><td>

-   Dynamic artifact detection enables Localization Workspace to identify all translatable content, including your custom artifacts. From version 1.1.0.
-   With status synchronization, translation requests in Localization Workspace reflect the same status as the Localization Framework projects. From version 1.1.0.
-   A Configuration hub and two new Guided Setups are available to help admins configure Localization Workspace. From version 2.0.2.
-   Optional due dates and language groups enhance the efficiency of creating translation requests. From version 2.0.2.
-   When selecting specific documents to translate, translation requestors can take advantage of a bulk select/deselect option as well as text search of document titles. From version 2.0.2.

See [Localization Workspace](https://www.servicenow.com/docs/access?context=localization-workspace&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US) for more information.

</td></tr><tr><td>

MCP Server Console

</td><td>

-   Get started with the preconfigured Quickstart Server for looking up and summarizing incident and case records.
-   Create MCP servers and tools based on Now Assist skills for different use cases.
-   Connect to any MCP client using OAuth 2.0 authentication.

See [MCP Server Console](https://www.servicenow.com/docs/access?context=mcp-platform-manager-landing&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US) for more information.

</td></tr><tr><td>

MID Server

</td><td>

-   MID Server smart workload manager continuously evaluates load and assigns jobs in a cluster to ensure that no server is overloaded.
-   MID Server logging has been improved with log backups that are preserved in a compressed format on a local host with an option to fetch to the instance.

See [MID Server](https://www.servicenow.com/docs/access?context=mid-server-landing&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US) for more information.

</td></tr><tr><td>

Manufacturing Commercial Operations

</td><td>

-   Create recall campaigns and claims to manage recall campaigns and streamline collaboration with dealers to resolve claims​.
-   Create repair claims to streamline collaboration with dealers to submit and resolve claims for repairs performed under warranty.
-   Create sales promotions and claims to manage sales promotion campaigns and to streamline collaboration with dealers to resolve claims.
-   Create phases and sub phases in the recall campaign to enable the manager to launch it for selected assets, and notify the targeted dealers.
-   Submit pre-authorization requests to confirm whether certain parts, fees, or repairs are covered under a warranty or service contract.
-   Create non-conformance \(NC\) and quality investigation \(QI\) cases to capture quality problems, coordinate investigations, and collaborate with stakeholders throughout resolution.

See [Explore Manufacturing Commercial Operations](https://www.servicenow.com/docs/access?context=manufacturing-explore&version=zurich&pubname=zurich-manufacturing&ft:locale=en-US) for more information.

</td></tr><tr><td>

Mastercard Spoke

</td><td>

-   File pre-arbitration and arbitration cases directly through Mastercard’s API.
-   Handle tasks such as searching transactions, creating claims, and processing chargebacks, pre-arbitration, and arbitration case filings efficiently.
-   Enable dispute agents with real-time data exchange and embedded Mastercard dispute life cycle workflows.
-   Accelerate time to value with a predefined Mastercom Extended spoke that reduces development effort and speeds up deployment.

See [Mastercard Spoke](https://www.servicenow.com/docs/access?context=mastercard-spoke&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US) for more information.

</td></tr><tr><td>

Mentoring

</td><td>

Enable Mentoring to configure multiple mentoring programs.

</td></tr><tr><td>

Mobile Platform

</td><td>

-   Access Mobile App Builder and Mobile Card Builder inside ServiceNow Studio.
-   Use enhanced capabilities within the input form screen.
-   Engage with the improved error handling when working with uploads.
-   Add customized client-side translations to extend language support on your mobile device.

See [Mobile Platform](https://www.servicenow.com/docs/access?context=mobile-config-navigation&version=zurich&pubname=zurich-mobile&ft:locale=en-US) for more information.

</td></tr><tr><td>

Model Risk Management

</td><td>

-   Maintain a centralized repository of all models, capturing key details such as ownership, status, model tier, and risk rating.
-   Manage the complete model life cycle by tracking models from initiation to monitoring through defined governance stages.
-   Evaluate model risks based on their usage, complexity, and impact.
-   Perform validation of model design, performance, and implementation.
-   Capture, track, and resolve validation findings or performance issues, ensuring timely remediation and continuous risk mitigation.

See [Model Risk Management](https://www.servicenow.com/docs/access?context=model-risk-management&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US) for more information.

</td></tr><tr><td>

Next Experience

</td><td>

-   Customize the visual experience of the Now Assist menu by using the new toggle to switch between standard or wide view.
-   Manage the visibility of page alerts with a new accessibility user preference.
-   Access usage analytic data for applications and web pages directly with the new Usage Analytics utility menu.

See [Next Experience UI](https://www.servicenow.com/docs/access?context=next-experience-landing-page&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US) for more information.

</td></tr><tr><td>

Next Experience Developer \(NED\) Tools

</td><td>

-   View traces as a full-screen waterfall with an enriched root span list that has more actionable metadata.
-   Access cache buster details to view how service workers impact page performance.

See [Next Experience Developer Tools](https://developer.servicenow.com/dev.do#!/reference/next-experience/zurich/developer-tools/using-next-experience-developer-tools) for more information.

</td></tr><tr><td>

Notifications

</td><td>

-   Use email diagnostics dashboard to monitor email delivery metrics, track bounce management, and overall health associated with email sender and reader jobs.
-   Control the preferences page to display relevant notifications.
-   Support multiple target records for email digest.
-   Use the standard forms for system notification preference.
-   Handle incoming email requests intelligently with the new email agentic workflow by identifying intent, executing actions, and drafting appropriate email responses.

See [Notifications](https://www.servicenow.com/docs/access?context=notifications&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US) for more information.

</td></tr><tr><td>

Notify

</td><td>

-   Build Notify subflows according to your requirements by using the default subflows provided in new instances.
-   Coral is the new default theme for Next Experience and Core UI, offering a user-friendly experience.

See [Notify](https://www.servicenow.com/docs/access?context=notify-landing-page&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US) for more information.

</td></tr><tr><td>

Now Assist

</td><td>

[Zurich Patch 8](../quality/zurich-patch-8.md)

-   Now Assist panel premium chat gives you a full-featured AI assistant experience with support for file uploads, web search, agentic workflows, and voice input — so you can get answers, take action on records, and complete complex tasks without leaving your current context.
-   Get accurate results without having to repeat yourself or correct a wrong action because Now Assist now recognizes when your request needs clarification and asks a focused follow-up question before acting.
-   Upload documents directly in your Now Assist panel conversation and Now Assist automatically extracts the relevant information to fill in required fields, answer your questions, and keep the conversation moving without switching modes or restarting the flow.
-   Select specific reasons when you give a thumbs up or thumbs down to a Now Assist response, so your feedback is more meaningful and helps improve future responses.

[Zurich Patch 7](../quality/zurich-patch-7.md)

-   Explore revamped **Manage AI models** option within Now Assist Admin for managing and configuring model providers, and updating model provider versions.
-   Select a record from the Now Assist context menu inline citation to navigate directly to the record page, where the referenced section will be highlighted for easy identification.
-   View all AI-generated content, now visually highlighted for easier recognition.
-   Set the minimum word count required for the Now Assist icon to appear, allowing you to control when the icon is displayed based on content length.

[Zurich Patch 5](../quality/zurich-patch-5.md)

-   Review changes to Now Assist usage measurement.
-   View improved legend and icon descriptions for the Now Assist Readiness Evaluation app.
-   Work with new system properties to improve performance and customization within the Now Assist Readiness Evaluation app.

[Zurich Patch 4](../quality/zurich-patch-4.md)

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

[Zurich Patch 2](../quality/zurich-patch-2.md)

-   Use the Now Assist Readiness Evaluation app to automate the implementation assessment process before implementing Now Assist agentic and generative AI.

[Zurich Patch 1](../quality/zurich-patch-1.md)

-   Enable administrators to set up a security Access Control Lists \(ACLs\) that checks user authentication for Now Assist context menu skills and new setup options. This feature gives them control over who can use Now Assist context menu skills and actions, as well as built-in options like shorten, elaborate, and change tone.
-   Use the Open Prompt Capability available in Now Assist for Strategic Portfolio Management \(SPM\) to ask questions and refine generated content through open-ended queries.

Zurich

-   Use Google Gemini and Anthropic Claude on AWS as AI model providers for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.
-   Select your preferred large language model \(LLM\) provider for Now Assist base system skills. Apart from Now LLM Service, the platform supports Azure OpenAI GPT-4.1 and GPT-4.1 mini, Google Gemini 2.0 Flash and 2.5 Pro, and AWS Anthropic Claude 3.7 Sonnet LLM providers with ServiceNow® third-party model strategy.
-   Suppress the modeless window for a custom Now Assist context menu event.
-   View numbered citations and links to the information sources when you use the Now Assist context menu for email reply recommendation.

See [Now Assist](https://www.servicenow.com/docs/access?context=platform-now-assist-landing&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US) for more information.

For more Platform Now Assist feature release notes, see the following topics:

-   [AI Search release notes](../now-platform-administration/ai-search-rn.md)
-   [Document Intelligence release notes](../analytics-intelligence-reporting/document-intelligence-rn.md)
-   [Now Assist Skill Kit release notes](../analytics-intelligence-reporting/now-assist-skill-kit-rn.md)
-   [Now Assist in Virtual Agent release notes](../conversational-interfaces/now-assist-va-rn.md)

</td></tr><tr><td>

Now Assist AI agents

</td><td>

[Zurich Patch 8](../quality/zurich-patch-8.md)

-   Test an agentic solution in the playground in AI-native mode.
-   Add widgets for tool outputs to provide an improved experience in AI-native mode.
-   Review issues and apply suggested recommendations to agentic AI assets after automated evaluations.
-   Run improved Platform agentic workflows, including Analyze task trends, Generate my work plan, and Identify ways to improve services.

[Zurich Patch 7](../quality/zurich-patch-7.md)

-   Run improved Platform agentic workflows, including Generate resolution plans, Generate my work plan, and Process images to tasks.
-   Get more insights into agentic AI asset performance with issue tracing and suggested optimizations from results pages.

[Zurich Patch 5](../quality/zurich-patch-5.md)

-   Run improved Platform agentic workflows, including Generate resolution plans, Generate my work plan, and Process images to tasks.
-   Show Agent card URL when using secondary agents.
-   Review changes to Now Assist usage measurement.
-   Japanese language support for voice assistants enables Japanese-speaking users to experience natural, culturally appropriate interactions with AI voice agents.

[Zurich Patch 4](../quality/zurich-patch-4.md)

-   Execute agentic workflows, AI agents, and tools in AI Agent Studio with role masking.
-   Additional role configuration is required for agentic workflows and AI agents included with Now Assist applications.
-   Run and review agentic workflow executions on forms in the Core UI and workspaces.
-   Framework extensibility with a new condition builder.
-   Support multilingual conversations.

[Zurich Patch 3](../quality/zurich-patch-3.md)

-   Consume Global Graph as a Knowledge Graph resource.
-   Check for offensive content with MCP guardian.
-   Support the latest MCP version from [Zurich Patch 3](../quality/zurich-patch-3.md).

[Zurich Patch 1](../quality/zurich-patch-1.md)

-   Authenticate users with the MCP Server to add a Model Context Protocol tool to AI agents using the Model Context Protocol Client.
-   Create ACLs for AI agents and agentic workflows to customize who can discover and trigger AI agents and agentic workflows.

Zurich EA

-   Create and maintain versions of LLM instructions for AI agents and agentic workflows to help organize and iterate on prompts and test their effectiveness.
-   Duplicate existing script, record operations, and search retrieval tools to reduce the work needed to create unique AI agents.
-   Monitor new analytics in the AI Agents Analytics dashboard to track valuable insights in customer satisfaction with AI interactions.
-   Use Google Gemini and Anthropic Claude on AWS as AI model providers for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.
-   View the agentic workflow and AI agent activity on your AI Agent Studio.

See [Now Assist AI agents](https://www.servicenow.com/docs/access?context=na-ai-agents&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US) for more information.

For the Platform Now Assist release notes, see [Now Assist release notes](../analytics-intelligence-reporting/now-assist-rn.md).

</td></tr><tr><td>

Now Assist Skill Kit

</td><td>

[Zurich Patch 7](../quality/zurich-patch-7.md)

-   Use labeling workflows to annotate UI templates.
-   Use structured output to constrain AI responses to predefined JSON schemas.
-   Improve overisght and compliance with AI Control Tower integration with your custom large language model.

[Zurich Patch 5](../quality/zurich-patch-5.md)

-   Review changes to Now Assist usage measurement.

[Zurich Patch 4](../quality/zurich-patch-4.md)

-   Create a custom model to meet your specific needs and control behavior.
-   Customize ServiceNow skills by modifying the prompt, inputs, and providers.

[Zurich Patch 1](../quality/zurich-patch-1.md)

-   Set up a security access control list to verify user authentication for Now Assist Skill Kit.
-   Use Document Intelligence as a tool when you create a skill.

-   Use UI Builder to deploy custom skills.
-   Use a custom data generator to create synthetic datasets.

See [Now Assist Skill Kit](https://www.servicenow.com/docs/access?context=now-assist-skill-kit-landing&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US) for more information.

</td></tr><tr><td>

Now Assist for App Engine

</td><td>

[Zurich Patch 5](../quality/zurich-patch-5.md)

-   Review changes to Now Assist usage measurement.

[Zurich Patch 4](../quality/zurich-patch-4.md)

-   Generate summaries for records in custom applications using the generative AI capabilities of Now Assist.

[Zurich release notes](../family-release-notes.md)

-   Use Google Gemini and Anthropic Claude on AWS as AI model providers for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.

See [Now Assist for App Engine](https://www.servicenow.com/docs/access?context=add-ai-to-custom-apps-with-now-assist-for-app-engine-enterprise&version=zurich&pubname=zurich-application-development&ft:locale=en-US) for more information.

</td></tr><tr><td>

Now Assist for CMDB

</td><td>

[Zurich Patch 7](../quality/zurich-patch-7.md)

-   Get AI-powered answers your questions on CI classes and attributes to help you work in CI forms, dashboards, home pages, and other views on the workspace.
-   Search queries can now span multiple tables and relationships between CIs.

[Zurich Patch 5](../quality/zurich-patch-5.md)

-   Review changes to Now Assist usage measurement

[Zurich Patch 4](../quality/zurich-patch-4.md)

-   Some Now Assist skills and agentic workflows are now turned on by default.
-   Agentic workflows and AI agents included with Now Assist applications now require additional security configuration.
-   Reduce the debugging time and effort when you resolve issues with Service Graph Connector import sets.
-   Find and resolve de-duplication tasks.
-   Speed the process of manually creating CIs.
-   Methodically work through the process of improving CMDB data governance.
-   Search for CIs by specifying any of several attributes of the CI of interest.
-   View a concise summary of the key CI data on a CI form in a workspace page or on any list view.

[Zurich Patch 3](../quality/zurich-patch-3.md)

[Zurich Patch 2](../quality/zurich-patch-2.md)

[Zurich Patch 1](../quality/zurich-patch-1.md)

See [Now Assist for Configuration Management Database \(CMDB\)](https://www.servicenow.com/docs/access?context=now-assist-landing-cmdb&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US) for more information.

</td></tr><tr><td>

Now Assist for Collaborative Work Management \(CWM\)

</td><td>

[Zurich Patch 5](../quality/zurich-patch-5.md)

-   Review changes to Now Assist usage measurement.

[Zurich Patch 4](../quality/zurich-patch-4.md)

-   In Zurich Patch 4, some Now Assist are now turned on by default.
-   Use Google Gemini and Anthropic Claude on AWS as AI model providers for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.
-   Help increase the efficiency of your teams using the generative AI capabilities of Now Assist for CWM.

See [Now Assist for Collaborative Work Management \(CWM\)](https://www.servicenow.com/docs/access?context=now-assist-for-cwm-landing&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Now Assist for Configure, Price, Quote \(CPQ\)

</td><td>

Summarize quote for immediate, comprehensive insights into quote details \(product, pricing, and terms\) to improve quote accuracy, help teams align, reduce manual review, catch issues early, and accelerate quote turnaround.

See [Now Assist for Configure, Price, Quote \(CPQ\)](https://www.servicenow.com/docs/access?context=now-assist-for-cpq-landing&version=zurich&pubname=zurich-order-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Now Assist for Creator

</td><td>

[Zurich Patch 7](../quality/zurich-patch-7.md)

-   Generate themes and color palettes from brand images using the new theme generation workflow in Theme Builder.
-   Edit published or live catalog items directly through conversations with Now Assist.
-   Configure UI policies, location, access, fulfillment, and portal settings for catalog items with the catalog item generation skill.

[Zurich Patch 5](../quality/zurich-patch-5.md)

-   Review changes to Now Assist usage measurement.

[Zurich Patch 4](../quality/zurich-patch-4.md)

-   Some Now Assist skills are now turned on by default.
-   Additional role configuration is required for agentic workflows and AI agents included with Now Assist applications.
-   Expedite the troubleshooting process by using the ATF troubleshooting agent store application.
-   Learn about how to use UI Builder and modify UI pages with the UI Builder agent.
-   Plan your application development with the Build Agent planning tool.
-   Generate catalog items conversationally and preview them during the creation process with Now Assist in Catalog Builder.

[Zurich Patch 3](../quality/zurich-patch-3.md)

-   Accelerate the transition from application design to development by connecting the Build Agent to the Figma Model Context Protocol server.

[Zurich Patch 2](../quality/zurich-patch-2.md)

-   Try the Build Agent for free with the Build Agent \(Trial\).

[Zurich Patch 1](../quality/zurich-patch-1.md)

-   Use Google Gemini and Anthropic Claude on AWS as AI model providers for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.
-   Create, edit, and deploy fully functional ServiceNow applications using the Build Agent in the ServiceNow IDE.
-   Enable security implementation to execute AI agents and agentic workflows through access control lists \(ACLs\) and user identities.

See [Now Assist for Creator](https://www.servicenow.com/docs/access?context=now-assist-for-creator-landing&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US) for more information.

</td></tr><tr><td>

Now Assist for Customer Service Management \(CSM\)

</td><td>

[Zurich Patch 8](../quality/zurich-patch-8.md)

-   Availability of filter controls in Now Assist Guardian for Now Assist for CSM.
-   Availability of AI Workflow tab in Core UI.

[Zurich Patch 7](../quality/zurich-patch-7.md)

-   Enhance the Complaint Case playbook to align playbook activities with agentic workflows, introduce AI‑driven summarization and drafting capabilities, and remove legacy components that are no longer part of the complaint experience.
-   Monitor how users engage with genAI skills in Now Assist for CSM.
-   Get a case status and manage cases through natural voice conversations.

[Zurich Patch 5](../quality/zurich-patch-5.md)

-   Review changes to Now Assist usage measurement.
-   Help reduce manual effort and case closure time for complaint cases with the Complaint Case AI agent collection.

[Zurich Patch 4](../quality/zurich-patch-4.md)

-   Enabled is\_template for all Now Assist skills and added support to clone and customize any base system genAI skill in the Now Assist Skill Kit
-   Defined the navigation path for Sentiment Analysis dashboard in Core UI to make accessing sentiment analysis data easier.
-   Track trending case topics with insights, visualizations, and customizable filters for deeper analysis with the Trending topics dashboard.
-   Monitor customer sentiment across cases with LLM-powered insights and track the sentiment trends in the dashboard.
-   Enable agents to access customer, case, and product details instantly through natural language queries with the provide customer 360 insights agentic workflow.
-   Auto-generate work notes and comment recommendations to help improve agent efficiency with the activity response generation skill.
-   Additional role configuration is required for agentic workflows and AI agents included with Now Assist applications.

[Zurich Patch 1](../quality/zurich-patch-1.md) Enable security in Now Assist for CSM and AI agents and agentic workflows by enforcing access control lists \(ACLs\) and user identity-based permissions.

Early Availability

-   Use the suggested steps that automatically display on the **Recommended Actions** tab to help resolve cases and increase agent productivity.
-   Use Google Gemini and Anthropic Claude on AWS as AI model providers for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.

See [Now Assist for Customer Service Management \(CSM\)](https://www.servicenow.com/docs/access?context=now-assist-csm&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Now Assist for Enterprise Architecture \(EA\)

</td><td>

[Zurich Patch 5](../quality/zurich-patch-5.md)

-   Review changes to Now Assist usage measurement.

[Zurich Patch 4](../quality/zurich-patch-4.md)

-   All Now Assist for EA skills are activated by default.
-   Use the Diagram change analysis Now Assist skill to compare an Enterprise Modeling and Visualization diagram with its previous version and generate a summary of the differences.

-   Use the Refine text Now Assist skill to elaborate or shorten text in the **Description** field of the business application, business capability, business process, and information object records. Also, use this skill to generate, elaborate, or shorten text in the **Reasoning** field under the **Planned Disposition** section of the business application record.

-   Additional role configuration is required for agentic workflows and AI agents included with Now Assist applications.
-   Use the Business Application Insights Now Assist skill to generate insights into your business applications.
-   Implement security in Now Assist AI agents with access control lists \(ACLs\).
-   On the Architectural Decision Records page, use the field in the Architectural Decision Records menu to enter queries and derive the required information from the Architectural Decision Records \(ADR\) artifact content.

[Zurich Patch 1](../quality/zurich-patch-1.md)

-   Use the Business Application Insights Now Assist skill to generate insights into your business applications.
-   Implement security in Now Assist AI agents with access control lists \(ACLs\).
-   On the Architectural Decision Records page, use the field in the Architectural Decision Records menu to enter queries and derive the required information from the Architectural Decision Records \(ADR\) artifact content.

Zurich Early Availability

-   Enhance your productivity by using the Now LLM Service or a supported third-party LLM with any Now Assist for Enterprise Architecture \(EA\) skill or AI agent.
-   Enhance your user experience with Coral that is used as the default theme for new portal, web, and mobile experiences.

See [Now Assist for Enterprise Architecture \(EA\)](https://www.servicenow.com/docs/access?context=now-assist-ea&version=zurich&pubname=zurich-application-portfolio-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Now Assist for FSM

</td><td>

-   Track and validate parts usage during work order task closure with the Parts Manager AI agent.
-   Create work orders from images by uploading photos of equipment issues through the Now Assist panel or ServiceNow Agent mobile app.
-   Access Now Assist Virtual Agent from a primary action button in the mobile app navigation bar.
-   Use voice-to-text input when interacting with Now Assist Virtual Agent in the ServiceNow Agent mobile app.
-   Enhance your productivity with the Create Work Order AI agent, which allows users to initiate work orders using AI to process descriptions from text.

See [Now Assist for Field Service Management \(FSM\)](https://www.servicenow.com/docs/access?context=now-assist-fsm&version=zurich&pubname=zurich-field-service-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Now Assist for Financial Services Operations \(FSO\)

</td><td>

Zurich Patch 7

-   Improve your live customer interactions and address customer inquiries more efficiently by using Now Assist for FSO interaction AI agent and summarization skill in the Agentic Contact Center for Banking application.
-   Use Now Assist for FSO customer insights AI agent and summarization skill in the Agentic Contact Center for Banking application to get insights such as customer summaries and financial overviews, for more consistent servicing and faster support.

[Zurich Patch 5](../quality/zurich-patch-5.md)

-   Review changes to Now Assist usage measurement.

[Zurich Patch 4](../quality/zurich-patch-4.md)

-   Leverage AI agents in Now Assist for FSO to automate the ACH dispute resolution process.
-   Use an updated Disputes intake via Virtual Agent conversation flow that supports the revised dispute questionnaire, bypassing questions when inferring answers, and initiating ACH disputes. This flow is for both cards and non-cards \(ACH\).
-   Now Assist for FSO skills and AI agents support model updates in Now LLM Service.
-   Additional role configuration is required for agentic workflows and AI agents included with Now Assist applications.

Early Availability

-   Implement security in Now Assist AI agents and Now Assist for FSO skills with access control lists \(ACLs\).

See [Now Assist for Financial Services Operations \(FSO\)](https://www.servicenow.com/docs/access?context=now-assist-for-financial-services-operations&version=zurich&pubname=zurich-financial-services-operations&ft:locale=en-US) for more information.

</td></tr><tr><td>

Now Assist for HR Service Delivery \(HRSD\)

</td><td>

[Zurich Patch 7](../quality/zurich-patch-7.md)

-   Review an ER interview summary quickly by using the ER interview summarization skill from both Core UI and Agent Workspace for HR Case Management.
-   Streamline the interview scheduling process using the self-scheduling mechanism within the schedule interviews agentic workflow.
-   Preserve institutional knowledge during employee offboarding with AI agents that automate document discovery, organize content by category, and guide managers and employees through the transfer process.
-   View additional journey services \(catalogs and order guides\) recommended based on previous journeys and peer requests.
-   As a manager, review recommendations in Now Assist in Virtual Agent and add new tasks through a conversational interface.
-   As an admin, create reusable feedback templates using the ServiceNow AI Platform Surveys tool.
-   As a manager, select and preview feedback templates when requesting feedback.
-   As a manager, review a summarized view of an employee's recent feedback on the feedback page in Manager Hub.

[Zurich Patch 5](../quality/zurich-patch-5.md)

-   Review changes to Now Assist usage measurement.

[Zurich Patch 4](../quality/zurich-patch-4.md)

-   Use AI voice agents to enable employees to use self-service tools and create HR cases over the phone.
-   Use AI agents to predict the relevant HR service for an HR case and automatically transfer the case to the predicted HR service.
-   Use AI agents to analyze criticality of an HR case and use existing knowledge articles and catalog items for resolving a noncritical case.
-   Use AI agents to assist with processing tuition reimbursement requests based on submitted course information and company policies found in knowledge articles.
-   Leverage AI agents to generate fulfillment plans for critical HR cases from both Core UI and Agent Workspace for HR Case Management.
-   Review ER case context quickly by using the ER case summarization skill from both Core UI and Agent Workspace for HR Case Management.

[Zurich Patch 1](../quality/zurich-patch-1.md)

-   Implement security in Now Assist AI agents with access control lists \(ACLs\).
-   Use AI agents to place requests to the Human Capital Management \(HCM\) system.
-   Leverage an AI agent to generate a fulfillment plan in a series of steps for an HR case from both Core UI and Agent Workspace for HR Case Management.
-   Leverage AI agents to collect the necessary inputs from recruiters and schedule interviews seamlessly.
-   Simplify employee onboarding with AI agents that gather inputs, structure tasks, enable manager review, and deliver personalized onboarding plans.

Zurich Early Availability

-   Use Google Gemini and Anthropic Claude on AWS as AI model providers for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.

See [Now Assist for HR Service Delivery \(HRSD\)](https://www.servicenow.com/docs/access?context=now-assist-hrsd&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Now Assist for Hardware Asset Management \(HAM\)

</td><td>

[Zurich Patch 7](../quality/zurich-patch-7.md)- Gain real-time visibility into critical asset data through generative AI-driven asset analysis summaries.

[Zurich Patch 5](../quality/zurich-patch-5.md)- Review changes to Now Assist usage measurement.

[Zurich Patch 4](../quality/zurich-patch-4.md)- Some Now Assist skills, agents, and agentic workflows are now turned on by default.

[Zurich Patch 1](../quality/zurich-patch-1.md)- Automate the hardware asset repair process by using an agentic workflow.

See [Now Assist for Hardware Asset Management \(HAM\)](https://www.servicenow.com/docs/access?context=now-assist-ham&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Now Assist for IT Operations Management \(ITOM\)

</td><td>

[Zurich Patch 8](../quality/zurich-patch-8.md)

-   AIOps LEAP added support for new third-party model Claude Sonnet 4.6.

[Zurich Patch 7](../quality/zurich-patch-7.md)

-   Use the Dynatrace Model Context Protocol \(MCP\) server agent for deeper analysis in the analyze alert impact and manage alerts autonomously agentic workflows.
-   Analyze a Service Observability dashboard to find performance insights.
-   Understand service health by analyzing all available Service Observability dashboards for a service.
-   Expand support for 3P AI Model in AIOps LEAP to include additional model options across Small \(OpenAI GPT-4o mini, Claude Haiku 4.5, Gemini 2.0 Flash\) and Large \(OpenAI GPT-4o, Claude Sonnet 4.5, Gemini 2.0 Pro\) tracks.

[Zurich Patch 5](../quality/zurich-patch-5.md)

-   Review changes to Now Assist usage measurement.
-   Now Assist skills used in the analyze potential impact agentic workflow are turned on by default.
-   Use the new manage alerts autonomously workflow to efficiently manage alerts and minimize resolution times, including an AI agent for triage, impact analysis, and root cause investigation.
-   -   ****

Create Knowledge Base articles with embedded command snippets

Guided chat workflow to create and manage Playbook and KBs

Break large groups into targeted sub-groups using generative AI

Generate comprehensive resolution steps from multiple web sources

Regenerate resolutions when new data sources are enabled


[Zurich Patch 4](../quality/zurich-patch-4.md)

-   View an error analysis by Now Assist in Agent Client Collector.
-   Additional role configuration is required for agentic workflows and AI agents included with Now Assist applications.

[Zurich Patch 1](../quality/zurich-patch-1.md)

-   Get deeper impact analysis in the analyze alert impact agentic workflow with five new AI agents.
-   Enhance security for Now Assist AI agents with access control lists \(ACLs\).
-   Find all TLS certificates expiring within a determined time and renew them in a single prompt.
-   Use the triage and analyze alert agentic workflow to perform initial triage and analysis in the context of an incident.
-   Review Alert analysis, and relevant information for new mixed alert groups in the Now Assist panel to help investigate alerts more effectively.

See [Now Assist for IT Operations Management \(ITOM\)](https://www.servicenow.com/docs/access?context=now-assist-itom&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Now Assist for IT Service Management \(ITSM\)

</td><td>

[Zurich Patch 8](../quality/zurich-patch-8.md)

-   Answer incident-related questions with context-aware agents using the Incident assist agentic workflow.
-   Generate summaries for Request Management records.

[Zurich Patch 7](../quality/zurich-patch-7.md)

-   Submit a catalog item for an account unlock using the voice AI agent.
-   Generate automatic responses for requests and requested items.
-   Use the ITSM Conversational Analytics dashboard that provides usage adoption performance metrics in Now Assist in Virtual Agent.

[Zurich Patch 5](../quality/zurich-patch-5.md)

-   Review changes to Now Assist usage measurement.

[Zurich Patch 4](../quality/zurich-patch-4.md)

-   Some Now Assist skills are now turned on by default.
-   Add self-service and deflection to your phone channel with Voice AI agents.
-   Edit the incident summarization skill prompts and inputs within the Now Assist Skill Kit \(NASK\).
-   Use the Now Assist context menu to create AI-powered generative text.
-   Use agentic workflows in Change Management to quickly link configuration items \(CIs\) to a change request, intuitively create change requests, and easily associate outages with a change request.
-   Empower service desk agents to diagnose and resolve incidents on DEX monitored devices quickly and efficiently by using the  DEX issue diagnosis and resolution agentic workflow.

[Zurich Patch 1](../quality/zurich-patch-1.md)

-   Use the Assess conflicts for a change request agentic workflow to run conflict detection for change requests and assess conflicts, identify affected CIs, and view the list of impacted services.
-   Use the Schedule a change agentic workflow to schedule change requests by identifying the available schedule slots.
-   Use the Explain SLA agentic workflow to understand the breakdown of task assignment and ownership for the SLA relevant to a specific incident, problem, case, or change request. Gain insight into the potential causes of a breach or delays.
-   Use the Assess quality of a Change Request agentic workflow to assess the quality of a change request, analyze the information available in the fields, and generate suggestions to improve the information in the fields.
-   Use the Wrap-up and resolve incident agentic workflow to resolve incidents, create, or attach Knowledge Base \(KB\) articles, update duplicate incident information, and attach Known Error \(KE\) articles to the incident record.

See [Now Assist for IT Service Management \(ITSM\)](https://www.servicenow.com/docs/access?context=now-assist-itsm&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Now Assist for Legal Service Delivery \(LSD\)

</td><td>

[Zurich Patch 7](../quality/zurich-patch-7.md)

-   Disclose conflicts of interest using natural language from Now Assist in Virtual Agent rather than having to fill out intake forms.
-   Legal Request and Matter summarization now considers data from extended practice area tables when summarizing.

[Zurich Patch 5](../quality/zurich-patch-5.md)

-   Review changes to Now Assist usage measurement.

[Zurich Patch 4](../quality/zurich-patch-4.md)

-   Some Now Assist skills are now turned on by default.
-   Additional role configuration is required for agentic workflows and AI agents included with Now Assist applications.

[Zurich Patch 1](../quality/zurich-patch-1.md)

-   Use Google Gemini and Anthropic Claude on AWS as AI model providers for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.

See [Now Assist for Legal Service Delivery \(LSD\)](https://www.servicenow.com/docs/access?context=now-assist-lsd-landing&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Now Assist for Manufacturing Commercial Operations \(MCO\)

</td><td>

[Zurich Patch 5](../quality/zurich-patch-5.md)

-   Review changes to Now Assist usage measurement.

[Zurich Patch 4](../quality/zurich-patch-4.md)

-   Enable the Recall manager to create corrective actions and charges for the recall campaign using the create recall corrective actions AI agent.

See [Now Assist for Manufacturing Commercial Operations](https://www.servicenow.com/docs/access?context=now-assist-for-MCO&version=zurich&pubname=zurich-manufacturing&ft:locale=en-US) for more information.

</td></tr><tr><td>

Now Assist for Operational Sustainability Management Management

</td><td>

[Zurich Patch 5](../quality/zurich-patch-5.md)

-   Review changes to Now Assist usage measurement.

[Zurich Patch 4](../quality/zurich-patch-4.md)

Accelerate carbon reporting with AI-powered calculations, validation, and insights for Scope 3 emissions.

Automate metric data collection from utility invoices by extracting key information using the AI-driven document intelligence for utility invoices.

See [Now Assist for Operational Sustainability Management](https://www.servicenow.com/docs/access?context=now-assist-for-esg&version=zurich&pubname=zurich-environmental-social-governance&ft:locale=en-US) for more information.

</td></tr><tr><td>

Now Assist for Operational Technology Service Management \(OTSM\)

</td><td>

Australia

-   Quickly understand the OT incident context and respond to user inquiries by using the OT incident summarization skill.
-   Help save time by automatically updating the resolution notes for an OT incident.
-   Generate a KB article when an OT incident is resolved by using an agentic workflow.

See [Now Assist for Operational Technology Service Management \(OTSM\)](https://www.servicenow.com/docs/access?context=now-assist-for-operational-technology-service-management&version=zurich&pubname=zurich-operational-technology&ft:locale=en-US) for more information.

</td></tr><tr><td>

Now Assist for Order Management

</td><td>

[Zurich Patch 7](../quality/zurich-patch-7.md)

-   Enable business-to-business \(B2B\) customers to create invoice dispute cases through AI-powered chat and voice assistants that guide them through conversational dispute intake on the Business Portal.
-   Provide uninterrupted handoff to human agents to support complex use cases, with full conversation context transferred to the CSM/FSM Configurable Workspace.
-   RMA AI agent for automated RMA entitlement and intelligent case handling.

[Zurich Patch 5](../quality/zurich-patch-5.md)

-   Review changes to Now Assist usage measurement.

[Zurich Patch 4](../quality/zurich-patch-4.md)

-   Enable B2B customers to submit order cases autonomously from the Business Portal by simply describing their needs in natural language using the manage order operations agent.
-   Summarize complex orders across products, services, and fulfillment tasks, enabling agents to quickly understand status, take the right actions, and avoid navigating fragmented views to make the next steps easier and improving productivity.

See [Now Assist for Order Management](https://www.servicenow.com/docs/access?context=now-assist-order-management&version=zurich&pubname=zurich-order-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Now Assist for Retail Service Management \(RSM\)

</td><td>

[Zurich Patch 5](../quality/zurich-patch-5.md)

-   Review changes to Now Assist usage measurement.

[Zurich Patch 4](../quality/zurich-patch-4.md)

-   Enable retail store support agents to use the store inquiry Al agent to:
    -   Search multiple knowledge sources to generate clear, traceable responses and flag uncertain cases for human review.
    -   Improve with every resolved query and seamlessly fit into HQ workflows with tailored suggestions.

</td></tr><tr><td>

Now Assist for Sales Force Automation \(SFA\)

</td><td>

[Zurich Patch 7](../quality/zurich-patch-7.md)

-   Now Assist for Sales and Order Management \(SOM\) is now known as Now Assist for Sales Force Automation \(SFA\) to align with our updated product taxonomy. There is no change to functionality or existing customer configurations.

[Zurich Patch 5](../quality/zurich-patch-5.md)

-   Review changes to Now Assist usage measurement.

[Zurich Patch 2](../quality/zurich-patch-2.md)

-   Enable sales agents to use the Help nurture new leads agentic workflow to:
    -   Proactively engage with initial leads
    -   Book an appointment/demo to qualify a lead
    -   Identify opt-outs and disinterest for lead disqualification

See [Now Assist for Sales Force Automation \(SFA\)](https://www.servicenow.com/docs/access?context=now-assist-for-sales-and-order-management-som&version=zurich&pubname=zurich-order-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Now Assist for Sales and Order Management for Telecommunications \(SOMT\)

</td><td>

[Zurich Patch 5](../quality/zurich-patch-5.md)

-   Review changes to Now Assist usage measurement.

[Zurich Patch 4](../quality/zurich-patch-4.md)

-   Collects the customer order information, identifies if the order needs enrichment, and creates the enrichment tasks. On closure of the enrichment task, it invokes the order fulfillment agent.
-   Uses the historic order tasks to create the order tasks. If the historic data doesn't return any results, the large language model \(LLM\) is used to get the response.
-   Checks the automation flow and fulfill order tasks.
-   Additional role configuration is required for agentic workflows and AI agents included with Now Assist applications.

See [Now Assist for Sales CRM for Telecommunications](https://www.servicenow.com/docs/access?context=somt-now-assist&version=zurich&pubname=zurich-telecom-media-technology&ft:locale=en-US) for more information.

</td></tr><tr><td>

Now Assist for Security Incident Response \(SIR\)

</td><td>

[Zurich Patch 7](../quality/zurich-patch-7.md)

-   Help enhance incident resolution plan generation by adding your existing runbooks to the AI runbooks section within the Security incident resolution plan skill. The existing runbooks provide additional context to the skill.
-   Use the Sightings search and Isolate host capabilities in the Resolve security incident workflow to help resolve security incidents.

[Zurich Patch 5](../quality/zurich-patch-5.md)

-   Review changes to Now Assist usage measurement.

[Zurich Patch 4](../quality/zurich-patch-4.md)

-   Some Now Assist skills are now turned on by default.
-   Use generative AI to create a quality assessment report of a security incident.
-   Additional role configuration is required for agentic workflows and AI agents included with Now Assist applications.

[Zurich Patch 1](../quality/zurich-patch-1.md)

-   Help analysts to add security incidents details to the Shift Handover report by chatting with AI agents in the Now Assist panel.

Zurich Early Availability

-   Help your analysts to gain insight into security incident record metrics with an agentic workflow. Chat with AI agents in natural language from the Now Assist panel.
-   Help your analysts to resolve security incidents by chatting with AI agents in the Now Assist panel where the AI agent can assist in providing a resolution plan.

</td></tr><tr><td>

Now Assist for Software Asset Management \(SAM\)

</td><td>

[Zurich Patch 8](../quality/zurich-patch-8.md)

-   Streamline your Software Asset Management application implementation by automating entitlement extraction from contracts using AI, ensuring faster deployment.
-   Enhance your SaaS integration troubleshooting experience with user-friendly error explanations and resolution guidance for runtime job failures.

[Zurich Patch 7](../quality/zurich-patch-7.md)

-   Automate the process of assigning available licenses to the Microsoft 365 Admin Portal by using an agentic workflow.

[Zurich Patch 5](../quality/zurich-patch-5.md)

-   Review changes to Now Assist usage measurement.

[Zurich Patch 4](../quality/zurich-patch-4.md)

-   Some Now Assist skills, agents, and agentic workflows are now turned on by default.
-   Automate user resolution with AI for SaaS license management to support efficiency and accuracy in subscription management.

[Zurich Patch 1](../quality/zurich-patch-1.md)

-   Automate and streamline the software asset request process by using an agentic workflow.
-   Automate the process of creating reclamation rules by identifying software products suitable for reclamation using an agentic workflow.
-   Automate the evaluation of unused and underused software installations for potential reclamation by using an agentic workflow.
-   Additional role configuration is required for agentic workflows and AI agents included with Now Assist applications.

See [Now Assist for Software Asset Management \(SAM\)](https://www.servicenow.com/docs/access?context=now-assist-sam&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Now Assist for Source-to-Pay Operations

</td><td>

[Zurich Patch 5](../quality/zurich-patch-5.md)

-   Review changes to Now Assist usage measurement.

[Zurich Patch 4](../quality/zurich-patch-4.md)

-   Some Now Assist skills are now turned on by default.
-   Additional role configuration is required for agentic workflows and AI agents included with Now Assist applications.

Previous Patch releases

-   Some Now Assist skills are now turned on by default.
-   Create purchase requisitions faster by uploading vendor quote files directly through Now Assist's AI-powered chat interface in the Employee Center.
-   Use the improved AI search in Shopping Hub, powered by the Retrieval Augmented Generation \(RAG\) framework, to get more accurate and relevant results.
-   The Help fulfill procurement requests agentic workflow has been renamed to Conversational intake for sourcing and procurement to better reflect its expanded scope and capabilities.
-   Use enhanced AI agents for the Conversational intake for sourcing and procurement agentic workflow in Now Assist for SPO to improve usability and operational efficiency.
-   Use enhanced AI agents for the Coordinate supplier onboarding agentic workflow in Now Assist for SLO to automate the registration of external suppliers and companies and streamlines the onboarding process.
-   Use the Field extractor skill to automate the extraction of invoice number or supplier invoice number from the inquiry case generated through various channels \(emails, virtual agent chats, or web content\). Automating the extraction of invoice and supplier numbers enhances Accounts Payable agents' efficiency, leading to faster and more accurate resolutions.
-   The Enhanced Inquiry resolution provider AI agent uses more data sources to suggest resolution to supplier inquiries.

See [Now Assist for Source-to-Pay Operations](https://www.servicenow.com/docs/access?context=now-assist-source-to-pay-operations&version=zurich&pubname=zurich-source-to-pay-operations&ft:locale=en-US) for more information.

</td></tr><tr><td>

Now Assist for Strategic Portfolio Management \(SPM\)

</td><td>

[Zurich Patch 5](../quality/zurich-patch-5.md)

-   Review changes to Now Assist usage measurement.

[Zurich Patch 4](../quality/zurich-patch-4.md)

-   All Now Assist for SPM skills are activated by default.
-   Use the identify similar records skill to find similar demands based on contextual similarity.
-   Enable the project task monitor AI agent to autonomously monitor project tasks on the critical path of a project.
-   Use the **Send preview** button to share a project insights email instantly.
-   Generate measurable targets from goals information and optional context with the target generation skill.

[Zurich Patch 1](../quality/zurich-patch-1.md)

-   Use Google Gemini and Anthropic Claude on AWS as AI model providers for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.

See [Now Assist for Strategic Portfolio Management \(SPM\)](https://www.servicenow.com/docs/access?context=now-assist-spm&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Now Assist for Telecommunications, Media and Technology \(TMT\)

</td><td>

[Zurich Patch 5](../quality/zurich-patch-5.md)

-   Review changes to Now Assist usage measurement.

[Zurich Patch 4](../quality/zurich-patch-4.md)

-   Address voice quality issues and validate tickets with RADCOM.
-   Summarize the risk signal and issues records along with respective risk solution and occurrence records.
-   Additional role configuration is required for agentic workflows and AI agents included with Now Assist applications.

[Zurich Patch 1](../quality/zurich-patch-1.md)

-   Manage and resolve billing inquiry case requests using a team of AI agents.
-   Analyze network incidents, correlate associated cases, and provide resolutions.
-   Summarize Knowledge Graph service details, success initiatives, internal plays, customer plays, and Zoom meeting details.
-   Analyze account health, trigger renewal flows, schedule, and manage touchpoint meetings.
-   Use agentic AI to quickly create consumer registrations.

See [Now Assist for Telecommunications, Media and Technology \(TMT\)](https://www.servicenow.com/docs/access?context=now-assist-spmc&version=zurich&pubname=zurich-telecom-media-technology&ft:locale=en-US) for more information.

</td></tr><tr><td>

Now Assist for Third-party Risk Management \(TPRM\)

</td><td>

[Zurich Patch 7](../quality/zurich-patch-7.md)

-   Use generative AI to recommend TPRM issues for reviewer validation.

[Zurich Patch 5](../quality/zurich-patch-5.md)

-   Review changes to Now Assist usage measurement.

[Zurich Patch 4](../quality/zurich-patch-4.md)

-   Use Now Assist for Third-party Risk Management \(TPRM\) to generate concise, AI-powered summaries of TPRM that can help with interpreting complex issue records.
-   Some Now Assist skills, agents, and agentic workflows are now turned on by default.

See [Now Assist for Third-party Risk Management \(TPRM\)](https://www.servicenow.com/docs/access?context=now-assist-tprm&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US) for more information.

</td></tr><tr><td>

Now Assist for Vault

</td><td>

[Zurich Patch 4](../quality/zurich-patch-4.md) The generate custom data pattern skill now uses the Now LLM Service as the default provider. You can switch to another provider as needed.

[Zurich release notes](../family-release-notes.md) The Now Assist for Vault application generates custom data patterns from text descriptions to streamline your workload, checks role access for an encrypted column to monitor your instance’s encryption access posture, and schedules data discovery jobs to detect sensitive data.

See [Now Assist for Vault](https://www.servicenow.com/docs/access?context=now-assist-vault-landing&version=zurich&pubname=zurich-platform-security&ft:locale=en-US) for more information.

</td></tr><tr><td>

Now Assist for Vulnerability Response

</td><td>

[Zurich Patch 5](../quality/zurich-patch-5.md)

-   Review changes to Now Assist usage measurement. See the "Changed in this release" section below.
-   Retrieve host \(Vulnerability Response\) and Application Vulnerability Response \(AVR\) data with the Retrieve VR Data agentic workflow.
-   The Retrieve VR Data agentic workflow is supported in the Unified Security Exposure Management \(USEM\) and legacy Vulnerability Response workspaces.

[Zurich Patch 4](../quality/zurich-patch-4.md)

-   Some Now Assist skills are now turned on by default.
-   Use generative AI to help you build custom API connectors in the Security Posture Control workspace.
-   Additional role configuration is required for agentic workflows and AI agents included with Now Assist applications.

[Zurich Patch 1](../quality/zurich-patch-1.md)

-   Help analysts identify and remove duplicate host vulnerable items.
-   Help analysts resolve remediation tasks with preferred vulnerability solutions from third-party vendors.

**Zurich Early Availability**: Help your vulnerability managers and analysts to resolve remediation tasks, assess your exposure to vulnerabilities, and analyze metrics for remediation targets. Chat with AI agents in natural language from the Now Assist panel.

See [Now Assist for Vulnerability Response](https://www.servicenow.com/docs/access?context=now-assist-for-vulnerability-response-landing&version=zurich&pubname=zurich-security-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Now Assist for Workplace Service Delivery \(WSD\)

</td><td>

[Zurich Patch 7](../quality/zurich-patch-7.md): Summarize workplace cases by using Now Assist for WSD.

[Zurich Patch 5](../quality/zurich-patch-5.md): Review changes to Now Assist usage measurement.

[Zurich Patch 1](../quality/zurich-patch-1.md)

-   Help map admins configure the map during bulk updates to Indoor Mapping using the automate map updates agentic workflow.
-   Optimize a maintenance case based on the space utilization rate of the location where a maintenance case is created using the optimize cleaning activities agentic workflow.

See [Now Assist for Workplace Service Delivery \(WSD\)](https://www.servicenow.com/docs/access?context=now-assist-wsd-landing&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Now Assist in AI Search

</td><td>

[Zurich Patch 5](../quality/zurich-patch-5.md)

-   Review changes to Now Assist usage measurement.

[Zurich Patch 4](../quality/zurich-patch-4.md)

-   Simplify setup with automatic activation of Now Assist Multi-Content Response Genius Results for search profiles when you use Guided Setup to activate the Now Assist panel.
-   Increase search precision and contextual relevance for knowledge article, Catalog Item, external content, and topic retrieval searches with hybrid search.
-   Improve the enhanced chat experience by configuring the system to use AI Search as the source for Ask Now Assist suggestions.
-   Provide more focused auto-complete suggestions for enhanced chat that honor the search user's domain restriction and the exclusion list for unwanted suggestions.

[Zurich Patch 1](../quality/zurich-patch-1.md)

-   Use Google Gemini and Anthropic Claude on AWS as AI model providers for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.
-   Improve search recall and accuracy with semantic vector indexing of Catalog Item short descriptions.
-   Prompt users to log in to Microsoft SharePoint Online as needed to see files shared with them when viewing Knowledge Graph user citations in Now Assist Multi-Content Response Genius Result answers

See [Now Assist in AI Search](https://www.servicenow.com/docs/access?context=now-assist-ais&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US) for more information.

</td></tr><tr><td>

Now Assist in Contract Management

</td><td>

[Zurich Patch 7](../quality/zurich-patch-7.md)

-   Provide feedback on Now Assist contract analysis results to help improve the AI accuracy.
-   Navigate directly to non-standard clause locations in a document when reviewing Now Assist suggestions in the Microsoft Word add-in.
-   Configure use case mappings to extract metadata and obligations from a signed contract that is uploaded directly on a contract record.
-   Use Now Assist powered conversational search to query contract documents using natural language and dialogue-driven queries, making it easier to find relevant information.

[Zurich Patch 5](../quality/zurich-patch-5.md)

-   Review changes to Now Assist usage measurement.

[Zurich Patch 4](../quality/zurich-patch-4.md)

-   Some Now Assist skills are now turned on by default.
-   Use AI-powered obligation extraction to automatically identify and capture key obligations from signed contracts, and then review, edit, approve, or reject them within the contract playbook to create obligation records automatically.
-   Activate the Contract obligation extraction skill in the Now Assist Admin console to enable automatic obligation extraction.
-   Use Now Assist powered conversational search to query contract documents using natural language and dialogue-driven queries, making it easier to find relevant information.
-   Additional role configuration is required for agentic workflows and AI agents included with Now Assist applications.

[Zurich Patch 1](../quality/zurich-patch-1.md)

-   Use the contract playbook to review and update the AI extracted metadata and reminder date for contract renewal or termination.
-   Use Google Gemini and Anthropic Claude on AWS as AI model providers for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.

See [Now Assist in Contract Management](https://www.servicenow.com/docs/access?context=cncore-now-assit-landing&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Now Assist in Document Intelligence

</td><td>

[Zurich Patch 7](../quality/zurich-patch-7.md)

-   View citations for multiple attachments using the document and visual insights AI agent.
-   Create skills with data extraction, question answering, and summarization capabilities using document and visual intelligence in Now Assist Skill Kit.
-   Now Assist in Document Intelligence skills are now turned on by default.

[Zurich Patch 5](../quality/zurich-patch-5.md)

-   Review changes to Now Assist usage measurement.

[Zurich Patch 4](../quality/zurich-patch-4.md)

-   View a test document in a larger workspace on a separate browser tab during use case setup.
-   Use the document and visual insights AI agent to upload files, extract information without a predefined use case using a selected LLM, and display the results in a dedicated document view.
-   Additional role configuration is required for agentic workflows and AI agents included with Now Assist applications.

[Zurich Patch 1](../quality/zurich-patch-1.md)

-   Leverage document data extraction and document Q&amp;A capabilities in a single Extract information from documents skill.
-   Create skills with data extraction, question answering, and summarization capabilities by using document and visual intelligence in Now Assist Skill Kit.
-   Choose the language for a use case to help the optical character recognition \(OCR\) model better detect the text to extract from your files.
-   Extract information from files with text written in Simplified Chinese or Japanese.
-   Extract information from documents for Operational Sustainability Management \(Operational Sustainability Risk Management\) workflows.

[Early Availability](../quality/zurich-all-other-fixes.md)

-   Use Google Gemini and Anthropic Claude on AWS as AI model providers for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.

See [Now Assist in Document Intelligence](https://www.servicenow.com/docs/access?context=docintel-nowassist-landing&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US) for more information.

</td></tr><tr><td>

Now Assist in Platform Analytics

</td><td>

[Zurich Patch 5](../quality/zurich-patch-5.md)

-   Review changes to Now Assist usage measurement.

[Zurich Patch 4](../quality/zurich-patch-4.md)

-   Some Now Assist skills are now turned on by default.
-   Create "explorations"—editable documents where you analyze data with the help of AI. Refine responses, add your own input, and collaborate with others to make data-informed decisions faster.

Previous Patch releases

-   Generate and export Platform Analytics artifacts from conversational interactions in the Now Assist panel.
-   Benefit from a single, smooth experience in asking questions across all Now Assist for Platform Analytics skills, as well as other applications that incorporate Platform Analytics and AI, through a shared backend.

See [Now Assist in Platform Analytics](https://www.servicenow.com/docs/access?context=now-assist-platform-analytics&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US) for more information.

</td></tr><tr><td>

Now Assist in Virtual Agent

</td><td>

[Zurich Patch 8](../quality/zurich-patch-8.md)

-   Use the Now Assist in Virtual Agent clarification feature to get direct answers to ambiguous requests. If your question can apply to multiple topics, the assistant asks a follow-up question to narrow down your intent before responding.
-   Opt into premium chat for your Now Assist panel - Platform assistant. Your instance must first meet certain prerequisites. Premium chat is an AI chat experience built into your ServiceNow environment that lets you ask questions, get answers from your organization's knowledge, and take action on records — all in one place. It supports file uploads, web search, and multi-step agentic tasks, so you can handle more complex requests without leaving the panel.
-   Brand your Now Assist panel – Platform assistant, if you have premium chat set up.

[Zurich Patch 7](../quality/zurich-patch-7.md)

-   Start a Now Assist in Virtual Agent conversation from anywhere in the Employee Hub.
-   Provide response feedback to Now Assist in Virtual Agent responses.
-   Use natural-language questions and receive concise, synthesized answers.

[Zurich Patch 5](../quality/zurich-patch-5.md)

-   Review changes to Now Assist usage measurement.
-   Japanese language support for voice assistants enables Japanese-speaking users to experience natural, culturally appropriate interactions with AI voice agents.

[Zurich Patch 4](../quality/zurich-patch-4.md)

-   Some Now Assist skills, agents, and agentic workflows are now turned on by default.
-   Create and manage LLM-based chat and voice assistants within Assistant Designer, a centralized assistant administrator experience.
-   View a people citation's org chart in the interactive view. The interactive view opens to the right of the chat conversation area.
-   Notice several UI improvements to enhanced chat and enhanced chat's full-page experience, including an updated input bar, gradient borders, copy message icon for received messages, and more.
-   Enable voice input to allow users to use a microphone to type the input. Voice input is only available for Now Assist panel Platform assistant.

[Zurich Patch 1](../quality/zurich-patch-1.md)

-   Use Google Gemini and Anthropic Claude on AWS as AI model providers for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.
-   Use agentic conversations and view agentic conversational processing flow steps.
-   View extended entities and records in standard and enhanced chat conversations if they’re associated with the Knowledge Graph Natural Language Query \(NLQ\) schema.
-   View suggested search queries previously performed in the portal's search bar within enhanced chat conversations.
-   Work with the simplified subheader of enhanced chat.
-   Delete closed enhanced chat conversations.
-   Expand the fallback options.
-   Enter into web search mode manually via the input bar.

See [Now Assist in Virtual Agent](https://www.servicenow.com/docs/access?context=now-assist-in-va-landing&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US) for more information.

</td></tr><tr><td>

On-Call Scheduling

</td><td>

-   Build on-call escalation notification configurable flows by using subflows that are available by default in new instances.
-   Add new custom providers as channels for on-call escalation notifications.
-   Configure the on-call notification message and response keywords to send the escalation notifications to the stakeholders.
-   Send the on-call escalations notifications to all the stakeholders when any of the configured record fields are modified.
-   Use Coral, which is the new default theme for Next Experience and Core UI.

See [On-Call Scheduling](https://www.servicenow.com/docs/access?context=c_OnCallScheduling&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Operational Resilience

</td><td>

-   Set up the nexus map configurations and use the interactive node map view to define dependencies and relationships between records.
-   Generate a Microsoft Word document for the action tasks in Digital resilience incident reporting.
-   Create DIR cases for multiple regulations from either an incident or a security incident report. You can map entities to regulations and configure the Smart Assessment Engine \(SAE\) template for each regulation within the regulatory agency profile.
-   Generate and validate regulator-ready Register of Information \(RoI\) packages for EU DORA compliance.
-   Use the enhanced fix scripts in the Common Service Data Model for improved Operational Resilience metrics.
-   Evaluate the importance and impact tolerance of services and self-attest their status by using Smart Assessment.

See [Operational Resilience](https://www.servicenow.com/docs/access?context=grc-opres-landing-page&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US) for more information.

</td></tr><tr><td>

Operational Sustainability Management

</td><td>

-   Enable organizations to provide estimated data using pre-defined methods like average when actual data isn’t available.
-   Enhance data accuracy and governance by adding a review process for automated metric definitions.
-   Integrate real-time energy consumption data from DEX into the ESG Sustainable IT Dashboard for more accurate and reliable sustainability reporting, especially for desktops and laptops.
-   Enabled tracking and reusing narratives or statements for disclosures, making it easy to highlight specific achievements or commitments.
-   Enable creating claims directly from Microsoft Word to ServiceNow via the Microsoft 365 plugin.
-   Use enhanced entity-based access for metric definitions, metrics, metric data tasks, and metric data, enhancing data security and granular access control.
-   Create and synchronize claims automatically when uploading disclosures from Word via the ServiceNow add-in. This streamlines ESG reporting and confirming traceability across templates.
-   Avoid calculation inconsistencies caused by missing operand values. The Calculated Metric Definition Settings table enables specifying default values for operands, confirming smooth execution and flexible configuration.
-   When renaming a metric definition, there’s an option to apply the updated name to its child metrics and their associated metric data tasks.
-   Enabled audit tracking for emission factor tables and all changes are automatically logged for compliance and traceability.
-   Removed the unit restrictions between calculated metric definitions and emission factors, enabling any emission factor to be applied regardless of unit.

See [Operational Sustainability Management \(formerly Environmental, Social, and Governance\)](https://www.servicenow.com/docs/access?context=esg-landing-page&version=zurich&pubname=zurich-environmental-social-governance&ft:locale=en-US) for more information.

</td></tr><tr><td>

Operational Technology \(OT\) Manager Foundation

</td><td>

[Zurich Patch 5](../quality/zurich-patch-5.md)

-   Review changes to Now Assist usage measurement.

[Zurich Patch 4](../quality/zurich-patch-4.md)

-   Some Now Assist skills, agents, and agentic workflows are now turned on by default.
-   Find OT Configuration Management Database \(CMDB\) records more quickly by using the OT CMDB search function.
-   Simplify the upload, validation, and import of your OT device data by using the Import OT device spreadsheet into OT CMDB agentic workflow.

See [Now Assist for Operational Technology Manager \(OTM\)](https://www.servicenow.com/docs/access?context=now-assist-for-otm-landing&version=zurich&pubname=zurich-operational-technology&ft:locale=en-US) for more information.

</td></tr><tr><td>

Operational Technology Incident Management

</td><td>

Report an OT incident without an OT incident role using the Employee Center for OT.

See [Operational Technology Incident Management](https://www.servicenow.com/docs/access?context=operational-technology-incident-management-landing-page&version=zurich&pubname=zurich-operational-technology&ft:locale=en-US) for more information.

</td></tr><tr><td>

Operational Technology Manager

</td><td>

-   Get a deeper look into your OT network with the OT network map in the Industrial Workspace, where you can view a site, its subnets, and the OT devices in each subnet.
-   View the Operational Technology Manager \(OT\) device-to-device connections with additional information such as port and protocol values.
-   Review the OT applications and versions that you have installed on the About Industrial Workspace page.
-   Keep your OT device data updated by using the Configuration Management Database \(CMDB\) OT class model updates and UI enhancements.
-   Improve the processes for importing and classifying your OT device data with updates and UI enhancements for the Pre-import OT Worksheet Entry Review \(POWER\) tool.

See [Operational Technology Manager](https://www.servicenow.com/docs/access?context=operational-technology-manager&version=zurich&pubname=zurich-operational-technology&ft:locale=en-US) for more information.

</td></tr><tr><td>

Operational Technology Vulnerability Response

</td><td>

-   Configure Operational Technology Vulnerability Response from the Security Exposure Management Workspace \(SEM Workspace\).
-   Access the Operational Technology Vulnerability Response Risk Calculator plugin directly without loading the demo data.
-   View all vulnerable items that have been created from the OT Vulnerable Items list in the Industrial Workspace.
-   View all remediation tasks that have been created from the OT Remediation Tasks list in the Industrial Workspace.
-   View all vulnerability exceptions that have been created from the OT Vulnerability Exception Approvals list in the Industrial Workspace.
-   Hardware Vulnerability Assessment is available for firmware discovery models without normalized data.

</td></tr><tr><td>

Opportunity Management

</td><td>

-   Enhance visibility and flexibility in pricing amendments for existing contracts or services through Move, Add, Change, Delete \(MACD\) actions on Sold Products \(SP\), Product Instances \(PI\), or Contracts.
-   Identify multiple stakeholders and accurately qualify opportunities with opportunity associated contacts and their defined roles. This is vital for streamlining sales processes and gaining clarity on how each contact influences the outcome of a deal.
-   Drive structured collaboration among multiple stakeholders involved in closing a deal using Opportunity Teams. The teams verify collaboration across various roles such as Account Executives, Sales Engineers, Customer Success Managers, and Partner Managers.

See [Using Opportunity Management](https://www.servicenow.com/docs/access?context=opportunity-mgmt-using&version=zurich&pubname=zurich-order-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Order Management

</td><td>

-   Handle move orders support.
-   Enhance the Order management \(OM\) integration with Strategic Portfolio Management \(SPM\) to enable projects for site and maintain program project and sub-project hierarchy.
-   Enables agents to change the location for product inventory at the order line level.
-   Support for nested objects, arrays, and custom attributes to model complex products.​
-   Support for order header discounts​.

See [Order management](https://www.servicenow.com/docs/access?context=explore-order-management&version=zurich&pubname=zurich-order-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Partner Relationship Management

</td><td>

Use the CSM Configurable Workspace to enable your enterprise administrators to view all the details that are related to their partners.

See [Partner Relationship Management](https://www.servicenow.com/docs/access?context=partner-relationship-management&version=zurich&pubname=zurich-order-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Password Reset

</td><td>

Coral is the new default theme for Next Experience and Core UI, offering a more modern experience.

See [Password Reset](https://www.servicenow.com/docs/access?context=password-reset-landing-page&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US) for more information.

</td></tr><tr><td>

Performance Analytics

</td><td>

-   Track critical process metrics and trends.
-   Measure process health and behavior against organizational targets.
-   Identify process patterns and potential bottlenecks before they occur.
-   Continually visualize historical and real-time process statistics in role-based dashboards. The dashboards enable individual stakeholders to make informed decisions.

See [Performance Analytics \(Indicator data sources\)](https://www.servicenow.com/docs/access?context=pa-overview&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US) for more information.

</td></tr><tr><td>

Performance Analyzer

</td><td>

-   View a waterfall or request flows displayed as executions sequences in a structured tree-like timeline.
-   Receive page load time data directly on the instance.
-   Access aggregated metrics by application and routes.

See [Performance Analyzer](https://www.servicenow.com/docs/access?context=performance-analyzer-landing&version=zurich&pubname=zurich-application-development&ft:locale=en-US) for more information.

</td></tr><tr><td>

Platform Analytics experience

</td><td>

-   Collaborate on data-informed decisions through an AI-assisted, interactive explorer that serves as a centralized workspace, where you can create and share data visualizations on the fly.
-   Manage Performance Analytics indicators more conveniently, with access to editing, creation, and migration from within the Platform Analytics experience.

See [Platform Analytics experience](https://www.servicenow.com/docs/access?context=par-workspace&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US) for more information.

</td></tr><tr><td>

Playbooks in Workflow Studio

</td><td>

-   Add permissions for playbook authors and runtime users.
-   Activate a playbook without a trigger. Set multiple potential triggers for a playbook, or trigger a playbook on a schedule.
-   Enable AI agents to complete activities without human intervention during runtime.
-   Set child variants to evaluate later in a playbook.
-   Create decision branches for stages.

See [Exploring playbooks](https://www.servicenow.com/docs/access?context=process-automation-designer&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US) for more information.

</td></tr><tr><td>

Policy and Compliance Management

</td><td>

-   Association of citations to controls feature enables users to associate controls with citations directly to avoid duplicated controls and ensure accurate compliance reporting.
-   Multiple enhancements to control objectives rationalization process, including improvements including automatic rationalization process creation, simplified two-step workflow for recommendations, skipped approvals for owner-reviewers, comment capabilities, and improved UI.
-   Now Assist for IRM includes skills and AI agent to identify affected control objectives when citation descriptions change and to provide suggested updates for review and approval.
-   Enhancements to control objectives and controls, including control objective requirements for granular statements, automatic control requirement generation, and attestation at control requirement level.
-   Enhancements to policy exception and extension requests, including approver pop-ups with key details, no indicator tasks for exempt controls, Send Information button for requesters, and expanded linking requirements for issue-based policy exceptions.

See [Privacy Management](https://www.servicenow.com/docs/access?context=privacy-management&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US) for more information.

</td></tr><tr><td>

Portfolio Planning

</td><td>

-   View the planned costs of your planning items for the past fiscal periods.
-   Use **Display mode** to switch between different views of the financials record page.
-   Experience consistent roadmap bar colors for choice list attribute values across all portfolio plans. View the roadmap-level milestone row while scrolling down the Roadmap page. Use different icons to distinguish item-level milestones.
-   Apply filters using string-type and Boolean field values to view the desired data.
-   Customize and apply a theme to your roadmap to match your organization’s standards.
-   Create and manage monetary benefit plans to capture and track projected and actual benefits.
-   Manage and run projects in various global currencies besides the functional currency using multicurrency.
-   Generate labor cost on sub-projects based on the resource assignments.

See [Portfolio Planning](https://www.servicenow.com/docs/access?context=portfolio-planning-app-landing-page&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Predictive Intelligence

</td><td>

-   Predictive Intelligence errors are logged in a new, dedicated table. The PI - Observability Dashboard leverages this table to provide analytics on prediction errors.
-   New advanced options for Classification models are available, including new parameters and a new algorithm.
-   Validation logic ensures that Predictive Intelligence models have ACLs to access data tables.

See [Predictive Intelligence](https://www.servicenow.com/docs/access?context=predictive-intelligence-landing&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US) for more information.

</td></tr><tr><td>

Privacy Management

</td><td>

-   A new external Personal data rights \(PDR\) request form enables customers, ex-employees, and third parties to submit PDR requests from a website with email verification.
-   Access Control by Legal Entity feature enables teams to access only processing activities relevant to their legal entity, maintaining privacy by design principle.
-   Now Assist for Privacy Management plugin uses Generative AI to streamline privacy workflows by summarizing assessments, condensing issues, and merging control objectives.
-   Reporting privacy incidents through email feature enables employees to report privacy incidents directly through email.
-   Impacted and related areas configuration allows privacy case managers to add custom business area types to privacy cases for better context.
-   Revamped Processing Activity overview page provides a unified dashboard showing key compliance and risk metrics for processing activities.

See [Privacy Management](https://www.servicenow.com/docs/access?context=privacy-management&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US) for more information.

</td></tr><tr><td>

Proactive Service Experience Workflows

</td><td>

-   Diagnose the incidents and change requests in the Proactive Service Experience Workflows. Create a resolution task manually to resolve the issue.
-   Run the diagnostics from the contextual panel in the Proactive Service Experience Workflows, Incident, Change request, and Product Support for Technology playbook.
-   Execute tests for a Configuration Item \(CI\) in the Proactive Service Experience Workflows, Change request, and Product Support for Technology playbook. For Configuration Items \(CIs\), run related tests directly from the CI form view.
-   Enables your customer to modify the visibility of the **Diagnose** tab and run diagnostics from the contextual panel in the Decisions table.
-   Technology Product Support Case application is renamed to Product Support for Technology
-   Technology Product Support Case application is renamed to Product Support for Technology.

See [Proactive Service Experience Workflows](https://www.servicenow.com/docs/access?context=assurance-workflows&version=zurich&pubname=zurich-proactive-service-exp-workflows&ft:locale=en-US) for more information.

</td></tr><tr><td>

Process Mining

</td><td>

-   Generate highlights of the improvement opportunities in the Opportunity details page.
-   Identify inefficiencies by focusing on the delays in task assignment by using idle time analysis.
-   Analyze the workload of transitions and cases by using touchpoint analysis.
-   Enhance data security by marking projects as restricted.
-   Process Mining is integrated with ServiceNow playbook.

See [Process Mining](https://www.servicenow.com/docs/access?context=process-mining&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US) for more information.

</td></tr><tr><td>

Product Catalog Management and Pricing Management

</td><td>

-   Support AI-powered semantic search queries to find relevant product offerings and service specifications in the product catalog interface.
-   Generate and update product offering blueprints that guide the accurate configuration of customizable products by agents and customers.
-   Enable sales agents to create price and quantity ramps, a pricing strategy for increasing product pricing and quantity amounts over specified time periods.
-   Define pricing on product offers based on the price of other product offers or transaction context variables.
-   Use product characteristics to adjust product costs, which are then used in margin calculations for sales quotes.

See [Product Catalog Management](https://www.servicenow.com/docs/access?context=product-catalog-managment&version=zurich&pubname=zurich-order-management&ft:locale=en-US) and [Pricing Management](https://www.servicenow.com/docs/access?context=pricing-management&version=zurich&pubname=zurich-order-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Project Portfolio Management

</td><td>

-   Synchronize resource assignment dates with the project end dates, and end resource assignments automatically when a project reaches its end date.
-   Manage all project-specific resource assignments in one place by accessing the resource page directly from Project Workspace.
-   Identify similar demand records based on contextual similarity in the name, description, and business case content using the identify similar records Now Assist skill.
-   Convert demands to Enterprise Agile Planning \(EAP\) entities, such as Epic, Feature, or Capability, directly from Demand Management.

See [Project Portfolio Management](https://www.servicenow.com/docs/access?context=c_ProjectPortfolioSuite&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Project Workspace

</td><td>

-   Guide teams through predefined stages and actions for each process using Playbooks.
-   Track, modify, and synchronize all resources assignment for a project from the resource assignment list page, which displays all assignments associated with that specific project.
-   Create and manage monetary benefit plans to capture and track projected and actual benefits.
-   Manage and run projects in various global currencies besides the functional currency using multicurrency.
-   Generate labor cost on sub-projects based on the resource assignments.

See [Project Workspace](https://www.servicenow.com/docs/access?context=project-workspace-landing-page&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Public Sector Digital Services

</td><td>

-   Create funding programs to establish top-level budgets and timelines that flow down to associated grant programs.
-   Simplify and streamline the grant application decisions​ with Grants Management:​ Evaluation &amp; Decision.
-   Enable merit reviewers to track, score, and monitor grant applications via a dedicated Reviewer Service portal.
-   Enable applicants to review and download the results letter and merit review summary of their grants application, and accept or decline their award, all within the new **Results** tab of the Grants Management portal.
-   Define fees for and autonomously assess fee waivers against agency-defined criteria for information requests with the Help manage public information requests agentic AI Agent, part of the Public Sector Digital Services AI Agent Collection application.

See [Public Sector Digital Services](https://www.servicenow.com/docs/access?context=bun-public-sector-landing-page&version=zurich&pubname=zurich-government-industry&ft:locale=en-US) for more information.

</td></tr><tr><td>

Purchase Order Management

</td><td>

-   Use a collaborative workspace to coordinate with suppliers and relevant stakeholders simultaneously.
-   Receive automatic notifications, automatically prioritize them, and assign them to the appropriate person.
-   Utilize resolution tools to automatically update orders and review order plans for the affected material and location.

See [Purchase Order Management](https://www.servicenow.com/docs/access?context=purchase-order-mgmt-landing-page&version=zurich&pubname=zurich-source-to-pay-operations&ft:locale=en-US) for more information.

</td></tr><tr><td>

Quote Management

</td><td>

-   Support quote header discounts​.
-   View the cost and profit of the entire quote to support informed discounting decisions and avoid unprofitable deals.

See [Quote Management](https://www.servicenow.com/docs/access?context=quote-management&version=zurich&pubname=zurich-order-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

RPA Hub

</td><td>

[Zurich Patch 7](../quality/zurich-patch-7.md)

-   You can now selectively define which actions \(components\) are handled within a Try-Catch block and which are handled outside it.
-   Versions of model provider are now supported for RPA bot generation skill.

[Zurich Patch 4](../quality/zurich-patch-4.md)

-   Promote stability with the Long-Term Support \(LTS\) model for generative AI.
-   Only the sn\_rpa\_fdn.rpa\_admin role can create, update, and delete records in the Robot License Distribution table.

[Zurich Patch 1](../quality/zurich-patch-1.md)

-   Use Google Gemini and Anthropic Claude on AWS as AI model providers for RPA bot generation skill in addition to Now LLM Service and Azure OpenAI.
-   Use the Python connector to execute custom Python scripts or files as part of an automation workflow.
-   Use a Smart Card authentication for enhanced security.
-   Enhanced access controls for RPA bot generation skill.

See [Robotic Process Automation \(RPA\) Hub](https://www.servicenow.com/docs/access?context=rpa-main-landing-page&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US) for more information.

</td></tr><tr><td>

Recommended Actions for Operational Technology Service Management \(OTSM\)

</td><td>

-   Use the AI Enhanced Recommended Actions for OTSM feature to access external sources related to an OT incident and review why the document is relevant to the incident.
-   Display relevant actions to users based on the context of an OT incident record.

See [Recommended Actions for Operational Technology Service Management \(OTSM\)](https://www.servicenow.com/docs/access?context=recommended-actions-for-otsm&version=zurich&pubname=zurich-operational-technology&ft:locale=en-US) and [AI Enhanced Recommended Actions for Operational Technology Service Management \(OTSM\)](https://www.servicenow.com/docs/access?context=ai-enhanced-ra-otsm-landing&version=zurich&pubname=zurich-operational-technology&ft:locale=en-US) for more information.

</td></tr><tr><td>

Recruitment workspace

</td><td>

-   Plan your work efficiently with better visibility through KPI dashboard and list views.
-   View and track job requisitions, applications, interviews, feedback, and more, all in one place.
-   Collaborate with, send reminders to, and track the actions of all internal and external stakeholders directly within the application.
-   Do all your work, such as managing job requisitions, interviews, talent pools, and more, in one centralized workspace, with streamlined sourcing capabilities included.
-   Monitor and improve hiring efficiency by tracking key metrics and applicant feedback.

See [Recruitment workspace](https://www.servicenow.com/docs/access?context=recruitment-workspace-concept&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Regulatory Change Management

</td><td>

-   Add multiple regulatory tasks or source document import tasks to a regulatory alert to manage the associated compliance activities efficiently. You can help to ensure that each task aligns with the regulatory requirements to maintain structured tracking and accountability.
-   Close a regulatory task during the Implementation state after you verify that all required actions and documentation are complete. You can also confirm that no pending activities remain before you close a task.
-   Change the workflow of a regulatory task to reflect the updated compliance procedures or organizational processes.
-   Create action tasks when a regulatory task is in the New, Work in Progress, or Implementation states to drive progress. You can also assign responsibilities to help ensure that the compliance actions are executed in a timely manner.
-   Close regulatory alerts manually when all associated tasks and compliance obligations have been successfully addressed. You can verify that each related item meets the closure criteria before confirming that the alert is resolved.

See [Regulatory Change Management](https://www.servicenow.com/docs/access?context=reg-change-mgmt-landing-page&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US) for more information.

</td></tr><tr><td>

ReleaseOps

</td><td>

-   Use ReleaseOps guided setup to simplify initial configuration.
-   Customize ReleaseOps pipelines to move changes from development to production through as many instances as needed for your ReleaseOps ecosystem.
-   Schedule releases or deploy changes on-demand.
-   Automate the testing and validation process with ReleaseOps to ensure that the proper checks, tests, scans, and approvals are completed before releasing changes to production.

See [ReleaseOps](https://www.servicenow.com/docs/access?context=releaseops-landing&version=zurich&pubname=zurich-application-development&ft:locale=en-US) for more information.

</td></tr><tr><td>

Request Management

</td><td>

Coral is the new default theme for Next Experience and Core UI, offering a more modern experience.

See [Request Management](https://www.servicenow.com/docs/access?context=c_RequestManagement&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Resource Management Workspace

</td><td>

-   Move an assigned or unassigned resource assignment to a different start date to align the work with your organization's prioritization cycle.
-   View the type of operational work assigned to a resource in the resource board drill-down view.
-   Allocate effort from unassigned resource assignments using the following ways — auto-assign work among all the available resources, or partially assign work among for selected resources.

See [Resource Management Workspace](https://www.servicenow.com/docs/access?context=using-rmw&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Retail applications

</td><td>

-   Use the store inquiry AI agent to help retail store support agents quickly find clear, traceable answers, flag uncertain cases for human review, and benefit from tailored suggestions that improve with every resolved inquiry.
-   Simplify frontline staff access for faster response times and improved accuracy with the Retail Mobile application.
-   Initiate and coordinate large-scale actions across multiple stores with the HQ Communications case type.
-   Standardize the reporting, tracking, and resolution of in-store issues with the Retail In-store Operations case type.
-   Resolve customer complaints quickly and accurately with the Retail Customer Complaint case type.
-   Bridge the gap between stores and HQ with an intuitive request and support system using the Store Inquiry case type for stores.

See [Retail](https://www.servicenow.com/docs/access?context=rahi-retail-operations-overview&version=zurich&pubname=zurich-retail-industry&ft:locale=en-US) for more information.

</td></tr><tr><td>

Return Merchandise Authorization

</td><td>

-   Streamline sales return by enabling agents to manage RMA cases in Agent Workspace and bridging self-service with full support.
-   Handle product cases efficiently to streamline the return process and enhance the customer experience.

See [Return Merchandise Authorization](https://www.servicenow.com/docs/access?context=return-merchandise-authorization&version=zurich&pubname=zurich-order-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

SQL API

</td><td>

-   Query your ServiceNow data directly without replicating it to external repositories or data warehouses.
-   Access data using read-only operations to prevent unintended changes to your ServiceNow records. Allow access only to the desired tables.
-   Integrate standard BI platforms such as Power BI, DBvisualizer, and other ODBC/JDBC-compatible tools directly with your ServiceNow data.
-   Merge your ServiceNow data with third-party datasets in your data lakes and analytical platforms for comprehensive analysis.
-   Write targeted SQL queries to retrieve only the data you need, reducing network overhead on data pipeline and data transformation, and improving performance.

For more information, see [Access your ServiceNow data using SQL API](https://www.servicenow.com/docs/access?context=accessing-your-servicenow-data-using-sql-api&version=zurich&pubname=zurich-api-reference&ft:locale=en-US).

</td></tr><tr><td>

Sales Forecasting

</td><td>

-   Confirm and finalize forecast values for a specific time period and category.
-   Modify and adjust forecast items.
-   Create and assign sales territories for improved sales planning and tracking.

See [Sales Forecasting](https://www.servicenow.com/docs/access?context=sales-forecasting&version=zurich&pubname=zurich-order-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Sales Territory Management​

</td><td>

-   Allocate sales regions efficiently to align with business complexity and distribute the sales teams for optimal performance.
-   Verify the fair distribution of sales among sales representatives to reduce internal conflict, enhance accountability, and consistent performance across the sales organization.
-   Verify that only authorized users access specific records, maintaining security and compliance.
-   Manage large sales teams efficiently with a structured, rule-based method that verifies clarity, consistency, and scalability.

See [Sales Territory Management​](https://www.servicenow.com/docs/access?context=explore-sales-territory-management&version=zurich&pubname=zurich-order-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Security Center

</td><td>

-   Use the new Identity and Access Management \(IAM\) section in Security Center to access IAM tools.
-   Use the overview summary pages for each IAM tool to get a summary of which utility each tool provides.
-   See all the platform security tasks that need your attention in Security Center. You can see notifications outside Security Center so that you’re aware of these tasks without having to monitor the task list constantly.

See [Security Center](https://www.servicenow.com/docs/access?context=sec-center-v2&version=zurich&pubname=zurich-platform-security&ft:locale=en-US) for more information.

</td></tr><tr><td>

Security Incident Response

</td><td>

-   Integrate Cortex XSIAM by Palo Alto Networks with ServiceNow Security Incident Response platform to turn SIEM insights into actionable incidents, thus accelerating response from detection to closure.
-   Use Advanced Work Assignment \(AWA\) to automatically assign incidents to your security analysts, based on their availability, capacity, and skills.
-   Ingest third-party risk scores in Security Incident Response to factor these scores when calculating risk scores.
-   Starting in version 13.9.33, you can do the following:
    -   Fetch closed offenses from IBM QRadar into Security Incident Response.
    -   Set the batch size for correlation rules during IBM QRadar offense polling to optimize performance.
    -   Use the Now Assist LLM-powered integration builder to rapidly build integrations for Security Incident Response using auto-code generation.
    -   Ingest MITRE D3FEND data and visualize attack–defense relationships through an interactive graph directly within a security incident.
-   Starting in version 13.9.21, you can do the following:
    -   Integrate CrowdStrike Next-Gen SIEM integration with ServiceNow Security Incident Response platform to retrieve detections and convert them into security incidents, thus enabling automated response actions.
    -   Improve incident classification and enable efficient retrieval of historical data and alerts through enhanced Splunk ES integrations.
    -   Configure and use on-call scheduling to prevent gaps in coverage and ensure analysts are available to address security incidents by configuring shifts for analysts.

See [Security Incident Response](https://www.servicenow.com/docs/access?context=sir-landing-page&version=zurich&pubname=zurich-security-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Security Posture Control

</td><td>

-   Create and publish your own API connectors with a step-by-step process in the Connector builder module in the Security Posture Control workspace. You can use generative AI to automate some steps. See the [Now Assist for Security Incident Response \(SIR\) release notes](../security-operations/secops-now-assist-security-operations-rn.md) for more information about the Now Assist skill.
-   Get insights into your overall security posture and configuration gaps in your security tools using new policies and asset proﬁles that are included with the Security Posture Control application.
-   Use the policies included with the application or custom policies that you create to monitor your assets for overall security tool coverage, compliance with internal configuration standards, critical combinations of security gaps and vulnerabilities, and possible internet exposure.

See [Security Posture Control](https://www.servicenow.com/docs/access?context=spc-landing&version=zurich&pubname=zurich-security-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Self-service and omnichannel engagement for CSM

</td><td>

-   Integrate Amazon Connect with Interaction Controls Component \(ICC\) voice call features to allow agents manage phone interactions directly within their Workspace.
-   Allows agents to select a queue when making outbound calls to improve routing, reporting, and compliance.
-   Integrate WhatsApp Cloud API with CSM to enable rich media messaging, interactive controls, Virtual Agent automation, and Agent Workspace support without third-party dependencies.
-   Enable external routing of email interactions to reduce administrative effort.
-   Improve agent callback transfers for smoother handovers and support customers to request scheduled callbacks.

See [Omnichannels for communicating with customers](https://www.servicenow.com/docs/access?context=omnichannels-communicating-customers&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US) and [Interaction Controls Component \(ICC\) for voice calls](https://www.servicenow.com/docs/access?context=contact-center-integration-with-icc&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Service Catalog

</td><td>

-   Enable catalog item creators to create complex catalog items in Catalog Builder with ease. They can create, edit, or delete client scripts, or create advanced reference qualifiers.
-   Help requesters complete catalog item forms faster on portals and Next Experience UIs using caller-provided key-value pairs that pre-fill catalog item forms.
-   Ease the work of catalog item requesters by letting them drag one or more attachments directly onto the form for faster submissions.
-   Use the Catalog browse component for an enhanced catalog item browsing experience on the Next Experience UI for catalog users.

See [Service Catalog](https://www.servicenow.com/docs/access?context=service-catalog&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US) for more information.

</td></tr><tr><td>

Service Exchange

</td><td>

-   Streamline data replication from provider to consumer instances with foundation data sync.
-   Enable seamless collaboration between provider and consumer with enhanced journal entry support.
-   Enable consumer users to access linked resources in the provider instance using magic links.

See [Service Exchange](https://www.servicenow.com/docs/access?context=tmt-service-bridge-both-landing-page&version=zurich&pubname=zurich-service-bridge&ft:locale=en-US) for more information.

</td></tr><tr><td>

Service Graph Connector for Microsoft Defender for IoT \(Azure\)

</td><td>

-   View the class mappings available for the Service Graph Connector using the new Class Mappings menu
-   Use the Firmware Installation \[cmdb\_firmware\_install\] table to capture the firmware version.
-   Avoid OT entity update issues by using the new **ire\_criterion\_attribute** attribute on the OT Entity \[cmdb\_ot\_entity\] table.
-   Extend capabilities of the Service Graph Connector to import devices actively scanned by Microsoft Defender for IoT.
-   Ingest actively scanned devices from Microsoft Defender for IoT and assign them to a site in your ServiceNow instance automatically using the **Site Map** table.

See [Service Graph Connector for Microsoft Defender for IoT \(Azure\)](https://www.servicenow.com/docs/access?context=integration-sgc-microsoft-defender-iot-azure&version=zurich&pubname=zurich-operational-technology&ft:locale=en-US) for more information.

</td></tr><tr><td>

Service Level Management

</td><td>

-   Coral is the new default theme for Next Experience and Core UI, offering a more modern experience.

-   SLA Timer Configuration supports target-based First to Breach SLA and advance condition-based First to Breach SLA.

See [Service Level Management](https://www.servicenow.com/docs/access?context=service-level-mgmt-landing-page&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Service Observability

</td><td>

-   Integrate with a number of new application performance management \(APM\) vendors.
-   Add service-scoped ServiceNow AI Platform charts to Service Observability dashboards, including charts from MetricBaseand as of 1.10, Health Log Analytics \(HLA\).
-   Customize your Service Observability dashboards to add more advanced charts using full vendor queries and template variables. As of 1.10, you can directly import charts from AWS and Azure.
-   Create dashboards for additional service types.
-   Connect to data sources efficiently with an improved flow.
-   As of 1.10, test your data mappings before using them to create charts and dashboards.
-   As of 1.10, use any field on a service as a tag key value in a data mapping and then use that tag as a variable in your chart queries.

See [Service Observability](https://www.servicenow.com/docs/access?context=service-observability&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Service Operations Workspace for ITSM

</td><td>

-   Propose a standard change template from a change record in Service Operations Workspace \(SOW\).
-   Experience enhanced meeting and pagination controls in the Change Advisory board \(CAB\) workbench.
-   Configure the Microsoft Teams integration with Notify in SOW Admin Center.
-   Use visual indicators like colors and icons on chat session tabs to notify agents about unread messages to maintain the Service Level Agreement \(SLA\) for the chats in SOW.
-   Optimize your viewing experience by resizing the modals in SOW.
-   Find similar incidents and add them as child incidents to a major incident record.
-   Support subflows in the On-Call trigger rule configurations.
-   Configure the alerts and notifications in SOW to automatically dismiss within the specified time.
-   View the dependency map for reference fields in a separate tab within the workspace.
-   Starting in version 8.2, you can do the following:
    -   Analyze the metrics for configuration items \(CIs\) in the Digital End-User Experience \(DEX\) and Service Observability \(SO\) UI dashboard view on the Investigate tab of an incident record.
    -   Access and configure SOW from the Admin Center using granular feature admin roles.
    -   View the recent task records to which the knowledge article is attached.
    -   Manage user actions on the reference fields with the glide list action.
    -   Perform DEX actions on a Configuration Item \(CI\) using the Action library from the contextual panel of the record page.
    -   View the details of conflicts detected, and manually run conflict detection in the change request form.
    -   As an on-call shift administrator with the rota\_admin role, access Teams, Schedules, and Home pages in SOW.

See [Service Operations Workspace for ITSM](https://www.servicenow.com/docs/access?context=sow-landing-page&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Service Portal

</td><td>

-   Use the support for Service Portal in the iOS Google App.
-   As an admin, configure the widget load order on Service Portal pages.
-   As an admin, defer the loading of AI Search assets to enhance page performance.

See [Service Portal](https://www.servicenow.com/docs/access?context=c_ServicePortal&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US) for more information.

</td></tr><tr><td>

Service Portfolio Management

</td><td>

-   Edit your service portfolios to comply with the new Digital Operational Resilience Act \(DORA\) standards:
    -   The Service portfolio record view includes the following key fields that are important for DORA compliance: **Managed by**, **Department**, and **Company** fields.
    -   Select multiple contracts in the **Contracts** field.
-   Delete the service portfolio or taxonomy node from the Digital Portfolio Management \(DPM\) scope.

See [Service Portfolio Management](https://www.servicenow.com/docs/access?context=SPM2-landing-page&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Service Reliability Management

</td><td>

-   Auto-generate service level objectives \(SLOs\) to help teams track service reliability in SRM.
-   Starting in version 6.5.0, remove unneeded services from SRM to keep your monitoring data relevant.
-   Starting in version 6.5.0, track real downtime and customer impact with outage-based service level indicators \(SLIs\).
-   Get timely error budget updates that reflect the impact of ongoing, open alerts.
-   Track, manage, and visualize service performance with the Service reliability dashboard.

See [Service Reliability Management](https://www.servicenow.com/docs/access?context=sr-landing-page&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

ServiceNow AI Lens

</td><td>

[Zurich Patch 7](../quality/zurich-patch-7.md)

-   Upload files, and then analyze and extract information from them.
-   Auto-map Microsoft Excel sheet headers with the columns of a ServiceNow® table.

[Zurich Patch 5](../quality/zurich-patch-5.md)

-   Review changes to Now Assist usage measurement.

[Zurich Patch 4](../quality/zurich-patch-4.md)

-   Trigger ServiceNow AI Lens from the Now Mobile® application to extract data from artifacts and auto-fill fields in a form.
-   Fill the Catalog Item form fields by triggering ServiceNow AI Lens from Service Portal.

[Zurich Patch 1](../quality/zurich-patch-1.md)

-   Use the Lens actions to define default instructions, trigger options, custom context, transform response logic, and post processing instructions for ServiceNow AI Lens execution.
-   Configure Lens actions to launch ServiceNow AI Lens from any part of the ServiceNow AI Platform, such as a workspace form or a portal.
-   Trigger ServiceNow AI Lens from a Virtual Agent conversation on a mobile device or in a portal.
-   View captured images that are attached to an auto-filled record using ServiceNow AI Lens.
-   Use Google Gemini and Anthropic Claude on AWS as AI model providers for ServiceNow AI Lens in addition to Azure OpenAI.

See [ServiceNow AI Lens](https://www.servicenow.com/docs/access?context=servicenow-lens-landing-page&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US) for more information.

</td></tr><tr><td>

ServiceNow AI Platform core feature

</td><td>

-   Simplify and build queries with fewer conditions by leveraging hierarchical relationships in a condition builder.
-   Use additional scripting features, including Promises and Async await, with the ECMAScript 2021 \(ES12\) JavaScript mode.
-   Define dynamic categories and dynamic attributes once and reuse them using dynamic namespaces across multiple tables and dynamic attribute store fields.

See [Administer the ServiceNow AI Platform](https://www.servicenow.com/docs/access?context=intro-now-platform-landing&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US) for more information.

</td></tr><tr><td>

ServiceNow IDE

</td><td>

-   Clone a Git repository that contains multiple applications.
-   Use light and dark developer themes.
-   Use the ServiceNow IDE in any supported left-to-right language.

See [ServiceNow IDE](https://www.servicenow.com/docs/access?context=servicenow-ide-landing&version=zurich&pubname=zurich-application-development&ft:locale=en-US) for more information.

</td></tr><tr><td>

ServiceNow SDK

</td><td>

-   Develop a user interface \(UI\) with React to build a full-stack application in source code.
-   Define flows, service catalogs, UI pages and more in source code with ServiceNow Fluent APIs.

See [ServiceNow SDK](https://www.servicenow.com/docs/access?context=servicenow-sdk-landing&version=zurich&pubname=zurich-application-development&ft:locale=en-US) for more information.

</td></tr><tr><td>

ServiceNow Studio

</td><td>

-   As of version 28.2.1, simplify the app creation process by using Creator Studio, Now Assist for app generation, or by gaining inspiration from the App Gallery.
-   As of version 28.2.1, elevate your access to security\_admin from within ServiceNow Studio to make changes to roles and ACLs.
-   As of version 28.2.1, several new granular admin roles enable developers to complete administrative configuration tasks without requiring the full admin role in ServiceNow Studio.
-   As of version 28.2.1, for file types that open in a builder, decide whether you want to edit the file in the builder or in the classic UI16 view.
-   As of version 28.2.1, access your favorite lists in ServiceNow Studio by bookmarking them.

See [ServiceNow Studio](https://www.servicenow.com/docs/access?context=servicenow-studio-landing&version=zurich&pubname=zurich-application-development&ft:locale=en-US) for more information.

</td></tr><tr><td>

ServiceNow Vault

</td><td>

[Zurich Patch 4](../quality/zurich-patch-4.md)

-   Manage and monitor cloud encryption metrics.
-   Get AI guidance using the Ask Now Assist panel in Vault console.

-   Use guided setup to begin autoclassifying sensitive data within [Financial Services](https://www.servicenow.com/docs/access?context=fso-overview&version=zurich&pubname=zurich-financial-services-operations&ft:locale=en-US) and [Customer Service Management](https://www.servicenow.com/docs/access?context=c_CustomerServiceManagement&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US) applications.
-   Monitor and review critical sensitive data metrics from the centralized ServiceNow Vault Console dashboard.
-   Navigate between security tools efficiently using the ServiceNow Vault Console dashboard.

See [ServiceNow Vault](https://www.servicenow.com/docs/access?context=servicenow-vault-landing&version=zurich&pubname=zurich-platform-security&ft:locale=en-US) for more information.

</td></tr><tr><td>

Sidebar

</td><td>

Prevent Sidebar discussions from becoming cluttered by using threaded replies when responding to messages.

See [Sidebar](https://www.servicenow.com/docs/access?context=sidebar-landing&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US) for more information.

</td></tr><tr><td>

Skills Foundation

</td><td>

-   The Skills Intelligence application name has been changed to Skills Foundation.
-   The skills ontology, which contained skill structure with categories and definition, is no longer provided. Supply your own skills data and import it into the Skills Foundation application.
-   Efficient skill search mechanism is provided by replacing machine learning models with AI search and AI search with RAG configuration for Pro Plus License \(i.e. LLM Integration\) customers.
-   Automatic HR job profile and Talent job profile synchronization when a new employee joins the organization, or​ an existing employee changes position. You must have Human Resources Scoped App \(sn\_hr\_core\) installed for this feature to work.
-   Integration between SAP SuccessFactors and ServiceNow enables customers to import skills and user skills into ServiceNow, unlocking Growth Experiences features and driving higher adoption​. The integration feature will only work for the customers who are using Job Profile Builder and will not work for those who are using Talent Intelligence Hub.

See [Skills Foundation](https://www.servicenow.com/docs/access?context=skills-intelligence&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Smart Assessment Engine

</td><td>

-   Collaborate on assessments in real time with multiple contributors.
-   Normalize assessment question scores to a common scale for fair comparison.
-   Capture data from physical documents quickly and accurately with barcode and QR code scanning.
-   Migrate question dependencies with an improved migration utility.
-   Simplify your workflow by combining assessments from different templates in a single and unified view.

See [Smart Assessment Engine](https://www.servicenow.com/docs/access?context=smart-asmnt-engine-landing-page&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US) for more information.

</td></tr><tr><td>

Software Asset Management

</td><td>

-   Streamline Adobe integration with the Software Asset Management application using the Adobe Guided Setup.
-   Integrate SAP HANA Database with the Software Asset Management application to monitor the memory allocations and licensing costs for your SAP HANA Database measurement.
-   Track and optimize licensing for Microsoft Server products on Microsoft Hyper-V virtualization technology by using the Software Asset Management publisher pack for Microsoft.
-   Track and optimize licensing for VMware vSphere Standard \(VVS\) and VMware vSphere Essentials Plus \(VVEP\) by using the Software Asset Management publisher pack for VMware.
-   Gain the flexibility to retrieve both subscription and consumption data at the organization level using the enhanced Docusign integration with the Software Asset Management application.

See [Software Asset Management](https://www.servicenow.com/docs/access?context=c_SoftwareAssetMgmt&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Source-to-Pay Operations Integrations

</td><td>

-   Send purchase orders, receipts, and invoices created in SAP ECC and SAP S4 HANA from your ServiceNow instance using the Source-to-Pay integration with SAP ECC and S4 HANA.
-   Handle sales orders, procurement, finance, and so on, in Oracle EBS from your ServiceNow instance using the Source-to-Pay integration with Oracle EBS.
-   Handle business spends and automate approvals, contracts, inventory, purchase orders, requisitions, suppliers, and user management in Coupa from your ServiceNow instance using the Source-to-Pay integration with Coupa.
-   Handle sales orders, procurement, finance, and so on, in SAP Ariba from your ServiceNow instance using the Source-to-Pay integration with SAP Ariba.

See [Source-to-Pay integration with third-party applications](https://www.servicenow.com/docs/access?context=source-to-pay-third-party-integration&version=zurich&pubname=zurich-source-to-pay-operations&ft:locale=en-US) for more information.

</td></tr><tr><td>

Sourcing and Procurement Operations

</td><td>

-   Enable shoppers to view and select their local currency throughout the Shopping Hub experience, including supplier cards, product detail pages, cart, checkout, my purchases, and request tracker.
-   Enable procurement admins to configure and render unique question types for quick and full checkout experiences for each product or service line.
-   Use dashboards and tabs in the Source-to-Pay Workspace to view spend, savings, and pipeline projects, identify savings opportunities, and create pipeline projects directly from filtered lists.
-   Enable requesters to submit sourcing requests with multiple products in a single sourcing intake form, automatically generating individual sourcing events for each product.
-   Allow requesters to view and manage third-party RFx tasks in the Employee Center and navigate to the third-party sourcing tool to review, publish, and award RFx.
-   Initiate catalog and off-catalog procurement workflows from the IT Asset Management \(ITAM\) workspace using the ITAM-SPO better together feature.
-   Enable decimal quantities for service items when creating purchase requisitions using quick or full checkouts in Shopping Hub and Employee Center.
-   Enable requesters to accept or reject case resolutions through email or Employee Center before closure, reducing premature case closures.

See [Sourcing and Procurement Operations](https://www.servicenow.com/docs/access?context=psm-overview&version=zurich&pubname=zurich-source-to-pay-operations&ft:locale=en-US) for more information.

</td></tr><tr><td>

Strategic Planning

</td><td>

-   Categorize your strategic priorities, goals, planning items, and execution items—projects and demands as Artificial Intelligence to track and monitor their progress from the AI Control Tower workspace.
-   Experience consistent roadmap bar colors for choice list attribute values across all portfolio plans. View the roadmap-level milestone row while scrolling down the Roadmap page. Use different icons to distinguish item-level milestones.
-   Apply filters using string-type and boolean field values to view the desired data on the Planning and Scoring pages.
-   Work on financial planning for various planning items such as Capabilities, Features, and so on.
-   View the planned costs of your planning items for the past fiscal periods.
-   Use Display mode to switch between different views of the financials record page.
-   Create and manage monetary benefit plans to capture and track projected and actual benefits.
-   Manage and run projects in various global currencies besides the functional currency using multicurrency.
-   Generate labor cost on sub-projects based on the resource assignments.

See [Strategic Planning](https://www.servicenow.com/docs/access?context=alignment-planner-workspace-landing-page&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Subscription Management

</td><td>

-   Manage custom applications and table mapping through the custom application list and custom table inventory list.
-   View and filter subscribers by domain for user-based subscriptions in domain-separated instances.
-   View and filter Now Assist usage by domain in domain-separated instances.
-   Monitor Workflow Data Fabric usage and view token use rate of each capability.

See [Subscription Management](https://www.servicenow.com/docs/access?context=subscription-management-landing-page-v2&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US) for more information.

</td></tr><tr><td>

Supplier Lifecycle Operations

</td><td>

-   The plugin Supplier Operations \(com.snc.sn\_so\) **must** be installed after upgrading to Supplier Lifecycle Operations Zurich release. For more information, see [Install Supplier Operations](https://www.servicenow.com/docs/access?context=install-supplier-ops&version=zurich&pubname=zurich-source-to-pay-operations&ft:locale=en-US).
-   The Supplier Lifecycle Operations plugin \(com.snc.sn\_supplier\_mgmt\) is renamed to Supplier Case Management. For more information, see [Supplier Case Management](https://www.servicenow.com/docs/access?context=supplier-case-management&version=zurich&pubname=zurich-source-to-pay-operations&ft:locale=en-US).

See [Supplier Lifecycle Operations](https://www.servicenow.com/docs/access?context=supp-mgmt-landing-page&version=zurich&pubname=zurich-source-to-pay-operations&ft:locale=en-US) for more information.

</td></tr><tr><td>

Synthetic monitoring

</td><td>

-   Run synthetic monitors from the MID Server.
-   Create monitors without needing to leave SOW to create an HTTP endpoint.
-   Assign a support group to synthetic monitoring alerts for easy investigation.
-   As of 1.4, view alerts associated with monitors and navigate to those alerts.
-   As of 1.4, use tags on a monitor's alerts.
-   As of 1.4, use synthetic monitoring with endpoints that support OAuth credentials.

See [Synthetic monitoring](https://www.servicenow.com/docs/access?context=synthetic-monitoring-landing-page&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Talent profile

</td><td>

-   Make faster hiring decisions with a unified view of all talent types \(applicants, employees, contingent workers, and alumni\) in one place.
-   Improve talent visibility for hiring by creating talent profiles and pools.
-   Make better sourcing, screening, and interview management decisions across all talent types by tracking their past interactions with the organization.

See [Talent Profile](https://www.servicenow.com/docs/access?context=talent-profile-ovrvw&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Telecommunications Network Inventory

</td><td>

-   The Logical interfaces \(such as VLANs\) and physical interfaces \(such as Gigabit Ethernet ports\) are now related to their parent equipment or card to help prevent duplicate CI creation.
-   Get converged experience for Network Inventory workflows using Service Operations Workspace.
-   Upload and manage CAD/PNG of floor maps to view the datacenter layout with physical asset placements over the floor.
-   Ingest operational data and show time series metrics on the datacenter floor map to monitor health.
-   Capture an inventory of operational facilities and define their relationships to respective network hardware such as the power chain.

See [Telecommunications Network Inventory](https://www.servicenow.com/docs/access?context=telecom-network-inventory&version=zurich&pubname=zurich-telecom-network-inventory&ft:locale=en-US) for more information.

</td></tr><tr><td>

Telecommunications Service Operations Management \(TSOM\)

</td><td>

-   Simplify connector build and data transformation by leveraging the reusable, standardized Telecom Discovery Builder Framework across multiple telecom data sources.
-   Discover logical network elements from Nokia Altiplano using the enhanced Service Graph Connector for unified network visibility on the ServiceNow AI Platform.
-   Detect discrepancies in both logical and physical entities, including attribute value mismatches, and improve audit accuracy using targeted filters.

See [Telecommunications Service Operations Management](https://www.servicenow.com/docs/access?context=telecommunications-service-operations-management&version=zurich&pubname=zurich-telecom-media-technology&ft:locale=en-US) for more information.

</td></tr><tr><td>

Theme Builder

</td><td>

[Zurich Patch 7](../quality/zurich-patch-7.md)

-   As of Zurich Patch 7, use Now Assist to automatically create brand‑aligned themes, then refine and publish them in Theme Builder.

-   Publish the new Next Experience Coral theme from Theme Builder.
-   Add custom fonts to your theme for enhanced branding.
-   As of Theme Builder version 6.1, configure modal, tile icon, banner, and card colors, and override these default illustrations with your own custom imagery.
-   As of Theme Builder version 6.1, enable dark mode to improve usability of Theme Builder in low-light conditions.

See [Working with themes in Next Experience](https://www.servicenow.com/docs/access?context=next-experience-theming&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US) for more information.

</td></tr><tr><td>

Third-party Risk Management

</td><td>

-   Use the Document Management system in TPRM to centralize third-party documentation in a searchable repository with metadata, and versioning, access controls.
-   Use vertical navigation in the Vendor Management Workspace through a customizable panel grouped by related lists for improved access to third-party records, assessments, and performance pages.
-   Configure risk areas with weighted questions and scored responses for internal assessments using the Smart Assessment Engine in the Vendor Management Workspace.
-   Use the latest Smart Assessment Engine questionnaire templates to perform internal and external assessments.
-   Use the enhanced Digital Resilience Third-party Information Register features in the Vendor Management Workspace.

See [Third-party Risk Management](https://www.servicenow.com/docs/access?context=third-party-risk-mgt-landing-page&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US) for more information.

</td></tr><tr><td>

Threat Intelligence Security Center

</td><td>

-   External sharing is now generally available, allowing secure and automated sharing of threat intelligence in STIX 2.1 and MISP formats.
-   Redesigned the Investigation Canvas with activity timelines, added internal intelligence, improved node design and interactions, enhanced related records to retrieve all the associated records, and upgraded the MITRE card with filter capabilities for a smoother experience.
-   Introduced the ability to import events directly from the MISP server.
-   Implemented a unified mapping experience for the text based feeds such as TEXT, CSV, and JSON import formats.
-   Implemented confidence mapping for the CrowdStrike \(CS\) Feed as part of additional settings. You can now map the malicious confidence levels of CrowdStrike indicators to the observable confidence values.

See [Threat Intelligence Security Center](https://www.servicenow.com/docs/access?context=tisc-landing-page&version=zurich&pubname=zurich-security-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

UI Builder

</td><td>

-   Assemble components in a low-code editor by dragging and dropping content from the UIB toolbox onto the stage.
-   Add Now Assist skills to enhance your page, component, or controller with generative AI capabilities.
-   Get instant conversational help within UI Builder through the Now Assist Panel.

See [UI Builder](https://www.servicenow.com/docs/access?context=ui-builder-overview&version=zurich&pubname=zurich-application-development&ft:locale=en-US) for more information.

</td></tr><tr><td>

Unified Security Exposure Management

</td><td>

-   Experience a standardized data model and modular workflows for Vulnerability Response applications with Unified Security Exposure Management. This transformation and architectural design ensures consistent features across all modules, simplifies configuration, and enables flexible, role-based experiences. The modular approach allows faster updates and seamless integration, creating a scalable and future-ready platform.
-   Manage security exposures with Findings and Remediation views with a centralized platform in the Security Exposure Management Workspace.
-   Configure all USEM apps, including rules, email templates, email notifications, and severity mapping for integrations with the Administration console.
-   Enhanced exception management: Streamlined exception request and approval workflows with comprehensive tracking and audit trails.
-   Use generative AI with features in the SEM workspace that are included with the Now Assist for Vulnerability Response application. See the [Now Assist for Security Incident Response \(SIR\) release notes](../security-operations/secops-now-assist-security-operations-rn.md) for more information.

See [Unified Security Exposure Management \(USEM\)](https://www.servicenow.com/docs/access?context=unified-security-exposure-management-landing-page&version=zurich&pubname=zurich-security-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Upgrade Console

</td><td>

-   Enable a smooth upgrade experience on your production and sub-production instances by completing essential tasks before, during, and after the instance upgrade.
-   Access Upgrade Console and Guided upgrade by experiencing the new and updated options.

See [Upgrade Console](https://www.servicenow.com/docs/access?context=um-landing-page&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US) for more information.

</td></tr><tr><td>

Usage Insights

</td><td>

-   Access the analytics overlay faster via the new utility icon and then redirect to the analytics dashboard by selecting **Analyze with User Experience Analytics** on the overlay.
-   Experience enhanced analytics with UXA filters on dashboards, configurable session metrics, Pages in User Experience Analytics, drill-down in inline dashboards, and a condition builder for Events.

See [User Experience Analytics](https://www.servicenow.com/docs/access?context=user-exp-analytics-landing&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US) for more information.

</td></tr><tr><td>

Virtual Agent

</td><td>

[Zurich Patch 4](../quality/zurich-patch-4.md)

-   Create and manage LLM-based chat and voice assistants within Assistant Designer, a centralized assistant administrator experience.
-   [Assistant Designer Asset library](https://www.servicenow.com/docs/access?context=vad-topics-page&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US):
    -   View an updated UI for Virtual Agent Designer topics in the new Assistant Designer Asset library page.
    -   Navigate between Assistants, Asset library, and Analytics tabs in the Assistant Designer UI.
    -   Disconnect an LLM Assistant from a given asset with the Actions on Row icon ![](../../administer/virtual-agent/images/kebab-menu.png)in the Asset library.
    -   See descriptions of each LLM asset type when selecting **Create asset** in the Asset library.
    -   Read a tooltip that appears when you edit an LLM assistant under the Assistans tab and try to promote more than 6 topics associated with an LLM assistant.

[Zurich Patch 1](../quality/zurich-patch-1.md)

-   Google Workspace chat now works with the ServiceNow® conversational interface features, including Virtual Agent, Natural Language Understanding \(NLU\), Notifications, and live agents.
-   Start the create flow for all supported conversational assets directly from Virtual Agent Designer.

See [Virtual Agent](https://www.servicenow.com/docs/access?context=virtual-agent-landing-page&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US) for more information.

</td></tr><tr><td>

Visa Spoke

</td><td>

Apply Visa Resolve Online \(VROL\) release 25.2 revision changes to some Visa Spoke actions.

See [Visa Spoke](https://www.servicenow.com/docs/access?context=visa-spoke&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US) for more information.

</td></tr><tr><td>

Vulnerability Response

</td><td>

-   If you are currently using Vulnerability Response and you want to upgrade to Unified Security Exposure Management \(USEM\), see [Unified Security Exposure Management release notes](../security-operations/secops-sem-rn.md) for more information about USEM and the Unified Security Exposure Management migration.
-   Import host vulnerability data from the Wiz scanners into Vulnerability Response VITs to help vulnerability managers assess your over-all cloud security posture.
-   With the sn\_vul.vulnerability\_analyst or sn\_vul.vulnerability\_admin role, create host remediation tasks manually in the Vulnerability Manager Workspace.
-   With the sn\_vul.remediation\_owner role, create host remediation tasks manually in the IT Remediation Workspace.

See [Vulnerability Response](https://www.servicenow.com/docs/access?context=vuln-landing-page&version=zurich&pubname=zurich-security-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Walk-up Experience

</td><td>

Coral is the new default theme for Next Experience and Core UI, offering a more modern experience.

See [Walk-up Experience](https://www.servicenow.com/docs/access?context=walkup-experience-landing-page&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Workforce Optimization for Customer Service CSM

</td><td>

-   Decoupling Channel Management from the core Workforce Optimization \(WFO\) modules supports modular deployment, enabling independent updates or scaling of Channel Management without impacting other workforce engagement.
-   Enable managers to view the team calendar in the month view on the Schedule page within the Manager Workspace, providing a broader overview of staffing and shift details.
-   Enable agents to view the team calendar in the month view within the Configurable CSM or FSM Workspace for better planning and engagement with your work commitments.

See [Exploring Workforce Optimization for Customer Service](https://www.servicenow.com/docs/access?context=explore-configurable-wfo-cs&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Zero Copy Connector Hub

</td><td>

-   Access enterprise data from external data warehouses including Snowflake, Google BigQuery, and Amazon Redshift, data lakes such as Databricks, and databases, including Oracle.
-   Retrieve data from external sources in real time without copying any data to your instance using zero copy connections.
-   Enrich AI agents and workflows on the ServiceNow AI Platform with external data using data fabric tables.

See [Workflow Data Fabric Hub](https://www.servicenow.com/docs/access?context=workflow-data-fabric&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US) for more information.

</td></tr><tr><td>

Zero Copy Connector for ERP

</td><td>

[Zurich Patch 4](../quality/zurich-patch-4.md)

-   Obtain ERP information and explore ERP data products using generative AI and agentic AI in ERP models.
-   Control data access and permissions for Zero Copy Connector for ERP AI agents to ensure that users can only interact with data they are authorized to obtain.
-   Retrieve IDOC information from SAP to create and update a greater number of SAP business entities.
-   Additional role configuration is required for agentic workflows and AI agents included with Now Assist applications.
-   Some Now Assist skills are now turned on by default.

[Zurich Patch 1](../quality/zurich-patch-1.md)

-   The name of the ERP Canvas application has been changed to Zero Copy Connector for ERP.
-   The name of the ERP Contact Packs application has been changed to ERP Data Products.
-   Accelerate your adoption of Zero Copy Connector for ERP using new and updated ERP Data Products.

See [Zero Copy Connector for ERP](https://www.servicenow.com/docs/access?context=erp-integration-overview&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Release notes summaries for Zurich features](../release-notes-summaries.md)


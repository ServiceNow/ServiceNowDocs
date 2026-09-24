---
title: New features and products in Brazil
description: Cumulative release notes summary on new Brazil features and products.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/rn-summary-new-features.html
release: brazil
topic_type: reference
last_updated: "2026-09-23"
reading_time_minutes: 108
breadcrumb: [Release notes summaries for Brazil features, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# New features and products in Brazil

Cumulative release notes summary on new Brazil features and products.

New products were introduced in Brazil, and additional features were added to existing  products.

<table id="rn-summary-new-features-tables" class="custom-rows"><thead><tr><th class="filter">

Application or feature

</th><th>

Details

</th></tr></thead><tbody><tr><td>

AI Admin Center

</td><td>

-   **[Automation opportunities enhancements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/now-assist-center-view-automation-opportunities.md)**

Use the automation opportunities enhancements to refine your view and identify opportunities. The automation opportunities list shows quick-select filters. The Resolution steps page for an automation opportunity is enhanced to show matched opportunities for default AI agents, agent status, and tooltips with links.

-   **[Delete custom data set analysis](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/ai-agent-advisor-delete-data-source.md)**

Delete a custom data source analysis that you no longer want to run for automation opportunity discovery.


</td></tr><tr><td>

AI Admin Hub

</td><td>

 

</td></tr><tr><td>

AI Agent Advisor

</td><td>

-   **[Automation opportunities enhancements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/now-assist-center-view-automation-opportunities.md)**

Use the automation opportunities enhancements to refine your view and identify opportunities. The automation opportunities list shows quick-select filters. The Resolution steps page for an automation opportunity is enhanced to show matched opportunities for default AI agents, agent status, and tooltips with links.

-   **[Delete custom data set analysis](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/ai-agent-advisor-delete-data-source.md)**

Delete a custom data source analysis that you no longer want to run for automation opportunity discovery.


</td></tr><tr><td>

AI Agent Studio

</td><td>

-   **[Define security controls for MCP Servers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/define-sec-mcp.md)**

Define access rules and tools in the Model Context Protocol Servers for security control before adding them as tools to an AI agent.

-   **[Create an external AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/create-a2a-agent-new.md)**

Add security controls and tools to external AI agents.

-   **[Test access to an AI asset](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/test-access-ai-asset.md)**

Test access to an AI asset to verify whether a user has access to an agentic AI asset - AI agent and agentic workflow. In case of access denial, use Access Analyzer to see the access results in Access Management.

-   **[Create an external AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/create-a2a-agent-new.md)**

The redesigned AI Agent Studio streamlines the creation and testing of external AI agents.

-   **[Model Context Protocol Client](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/mcp-client-landing.md)**

The Model Context Protocol Client application has been redesigned.

-   **[Implement access control in AI Agent Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/implement-aias-security-new.md)**

Enforce deny-by-default access control for agentic AI record types \(`gen_ai_agent`, `gen_ai_workflow`, `gen_ai_skill`, `Flow`, `flow_action`\) for newly activated ServiceNow instances. In previous releases, these types defaulted to allow access.


</td></tr><tr><td>

AI Control Tower

</td><td>

-   **[Control AI asset usage through policies](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/gov-pol-landing.md)**

Create AI asset usage policies that automatically respond to detected AI threats or block an AI agent, domain, or model outright.

-   **[Add an Azure AI Foundry connection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/aict-configure-azure-foundry-security-connection.md)**

Connect Azure AI Foundry to AI Control Tower so that policies and AI agent containment using kill switch protocol can reach and act on agents running on Azure AI Foundry.

-   **[Add metrics from the AI system record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/mon-ai-configure-ai-system-metrics.md)**

Add evaluation metrics for a specific AI system without changing your organization's global metric configuration.

-   **[Add specific metrics for one or more external AI systems](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/mon-ai-configure-asset-metrics-external.md)**

Add, remove, or adjust the sample rate of metrics for one or more external AI systems, without changing your organization's global metric configuration.

-   **[Add specific metrics for one or more ServiceNow AI systems](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/mon-ai-configure-asset-metrics-servicenow.md)**

Add or remove metrics for one or more ServiceNow AI systems, without changing your organization's global metric configuration.

-   **[Exclude an AI system from a metric](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/mon-ai-exclude-ai-systems-external.md)**

Exclude one or more AI systems from a specific metric, without changing that metric's configuration for every other system.

-   **[AI system performance metrics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/mon-ai-asset-monitor.md)**

Monitor operational health at a glance, including average latency and token usage per session.

-   **[Latency and span counts for sessions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/mon-ai-evaluated-sessions-overview.md)**

See each session's response time and span count in the evaluated sessions lists and on individual session detail pages.

-   **[Scoring bias indicator](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/mon-ai-monitoring-overview.md)**

Learn when a composite score might be skewed. See how many evaluations back each metric, and identify when uneven evaluation coverage is influencing the score more than the configured weight suggests.

-   **[Trace data retention controls](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/mon-ai-configure-trace-retention.md)**

Keep session, trace, and span data for up to 30 days for scoring, or discard it to reduce storage usage, with quality and safety scores staying available either way. Discarding also disables AI Skill Kit insights and hides the evaluated sessions views.

-   **[Custom date ranges for monitoring](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/mon-ai-monitoring-overview.md)**

Analyze exactly the period you need by specifying an exact start and end date, up to 18 months apart.

-   **[Review AI security posture in design-time metrics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/gov-sec-reference.md)**

Use AI security posture metrics to identify potential configuration issues in AI agents, tools, MCP servers, and system prompts that could lead to security risk.

-   **[AI Inventory Intelligence Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/inventory-intelligence-agent.md)**

AI Inventory Intelligence Agent automatically analyzes the AI asset inventory, identifies assets with incomplete metadata, and generates enrichment recommendations to improve data quality and governance readiness.

-   **[Configuring connectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/aict-configuring-connectors.md)**
    -   The Microsoft connector introduces the A365 agent platform to discover and import AI assets into ServiceNow AI Control Tower.
-   **[Client registration and AI Gateway setup](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/client-registration.md)**
    -   The MCP and CIMD registered clients can be edited to update their configuration from the AI Gateway Setup tab.
    -   The AI Gateway proxy URL format has changed. The new format is:

`https://<instance-url>/sncapps/aigw/mcp/<mcp-server>`

Previously, the URL format was:

`https://<instance-url>/sncapps/awh/<mcp-server>/mcp`

-   **[Updated playbooks for governing managed assets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/dynamic-playbooks-for-governing-managed-assets.md)**

Manage AI assets through structured lifecycle workflows using the updated playbooks. These playbooks automate governance tasks, route approvals, and track compliance requirements across onboarding, maintenance, and retirement phases. Use the **Review and switch** button to understand impact to your existing playbooks, flows, and subflows before switching to the new playbook.

-   ****

AI Control Tower now scopes value, engagement, and cost data based on the user’s role and assigned AI systems.

AI stewards can view data for all AI systems in an instance. Product owners can view data only for the AI systems that they manage.

Data scope is determined by the **Managed by** field on the AI system record.

Product owners can review and adjust measurements for the AI systems that they manage. Cost configuration remains read-only because vendor-level changes can affect AI systems outside a product owner’s scope.


-   **[Monitor agent activity chart improvements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/mon-ai-monitoring-overview.md)**

Monitor agentic AI performance over time using new filter options in the Monitor agent activity chart. View the top five lowest performing metrics, top five highest performing metrics, or view performance for a specific metric in the chart.

-   **[Session details improvements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/mon-ai-session-details.md)**

View a list of lowest scoring metrics and the LLM judge's reasoning in the Quality and Safety score cards on the Session details page.

-   **Connectors**

Amazon Quick connector is a new connector which is part of discovering Systems, models, and prompts for creating AI connections.


</td></tr><tr><td>

AI Desktop Actions

</td><td>

-   **[Execute adaptive desktop actions on macOS](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/ai_desktop_actions_adaptive.md)**

Download the new AI Desktop Actions installer for macOS with M-series processor support \(ARM64 architecture\). The adaptive desktop actions enable AI agents to navigate applications and browsers and perform tasks on macOS systems. Both adaptive and defined desktop actions are now available with platform-specific installers.

    -   Review the AI agent's execution plan before it runs and pause execution to make manual adjustments at any time.
    -   Explicit user consent is required before the AI agent can access desktop, third-party services, and files.
    -   Monitor the live execution of adaptive desktop actions in the preview window.
    -   Refer the real-time status tracking that shows whether the AI agent is initiating, running, or paused.
    -   Take control of the execution where your input is needed.
    -   The AI agent batches consecutive actions into single execution calls where possible, minimizing round trips and reducing overall execution time.
-   **[Control resource access using policy and rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/security_policy_governance_concept.md)**

Create policies and rules to control which resources AI agents can access.

    -   Policies: Collection of resource access rules that applies to a specific user group or set of users based on defined user criteria.
    -   Resource access rules: Specific restrictions controlling agent access to various resource types, such as files, folders, websites, and applications.
    -   Bi-directional policy-rule mapping: Link policies to rules from either the policy record or the rule record, enabling rule reuse across multiple policies.
-   **[Credential and dynamic parameter management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/credential-storage.md)**

Reference credentials or other user-specific values by name in your instructions. The agent resolves them securely at execution time, so you never have to type them in yourself.

-   **[File upload and download](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/upload-download-file.md)**

Upload files to web forms and track file downloads during automated browser tasks. The agent validates file safety, confirms the target field with the reasoning model, and escalates to the user when it can't proceed safely.


</td></tr><tr><td>

AI Risk and Compliance

</td><td>

-   **[Updated playbooks for governing managed assets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/dynamic-playbooks-for-governing-managed-assets.md)**

Manage AI assets through structured lifecycle workflows using the updated playbooks. These playbooks automate governance tasks, route approvals, and track compliance requirements across onboarding, maintenance, and retirement phases. Use the **Review and switch** button to understand impact to your existing playbooks, flows, and subflows before switching to the new playbook.

-   **[AI reviewer assist for risk assessments](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/ai-based-reviewer-assistant-for-assessments.md)**

AI Risk and Compliance analysts reviewing assessments can review AI-assisted recommendations and assign relevant control objectives and risk statements from the compliance library. The Control Objective Recommender and Risk Statement Recommender skills generate the recommendations. The skills analyze the completed assessment responses and surface relevant control objectives and risk statements from the Risk and Compliance library. Accepted recommendations are scoped automatically to the AI Asset.


</td></tr><tr><td>

Accounts Payable Operations

</td><td>

-   **[Case exclusion rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/source-to-pay-operations/case-exclusion-rules.md)**

Defines condition-based rules that reduce unnecessary emails from creating cases. Case exclusion rules keep the case queue focused on genuine invoice inquiries, reducing redundant work and unnecessary notifications so AP agents can spend more time on real supplier and invoice issues. Manually reopen an inquiry case that is in the closed state and reuse the existing case history than starting over.


</td></tr><tr><td>

Agent Chat

</td><td>

-   **Customize Agent Chat inbox**

Receive notifications of newly assigned work items in your inbox, even when you're working outside of the workspace. This new notification flag ensures that you don't miss assignments.


</td></tr><tr><td>

Asset Audit Response

</td><td>

-   **[View reports that are associated with your evidence records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/fulfill-evidence-requests-guided-experience.md)**

View the complete detailed reports associated with evidence records that have an Evidence type of Data Visualization or Report. Use each report to gain comprehensive insight into the supporting information or data that you want to collect and submit for an evidence request.


</td></tr><tr><td>

Audit Management

</td><td>

-   **[View control tests in a grid on an engagement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/view-control-tests-tab-engagement-ws.md)**

Manage all control tests for an engagement from a single grid on the **Control tests** tab. View test status, assigned auditor, and effectiveness results, create or delete control tests, and request evidence directly from a row without opening each record individually.

-   **[Using Document Management System](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/manage-documents-panel.md)**

Store, organize, version, and control access to documents on engagements, control tests, and evidence records with the new Documents panel, alongside the existing Attachments panel. Connect an existing document from Microsoft SharePoint, Microsoft OneDrive, or Google Drive without downloading and re-uploading it.

Summarize a document or ask questions about its content using generative AI capabilities. Generate a spoken audio summary, directly from the Documents panel without opening the full document.


</td></tr><tr><td>

Authentication

</td><td>

-   **[Policy-based login experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/next-gen-login-experience.md)**

Use the Policy-based experience \(identifier-first login\) framework in the Authentication Console to craft login policies to simplify the login experience by presenting relevant login methods based on user context, such as username or email.

-   **[SAML certificate expiry notifications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/c_SAML2.0WebBrowserSSOProfile.md)**

Receive banner alerts on the home page when SAML SP signing or encryption keystores are approaching or past their expiry date. The instance displays two separate banners — one for signing certificates and one for encryption certificates — each linking to a dedicated customer action in Security Center.

-   **[Email OTP as an authentication factor](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/email-otp-authentication.md)**

Use Email OTP as a standalone factor, a primary factor, or a secondary factor in AI voice agent authentication flows. When a caller reaches the voice agent, a one-time passcode is sent to their registered email address. The caller provides the passcode to complete authentication.

-   **Authenticate callers at the start of every call**

Prompt callers for authentication or identification details at the start of every call, before the voice-only assistant responds to any request, using the Authenticate at the start of the call option on the Assistant Designer's Caller verification page.

-   **[Workload Identity Federation for Microsoft Azure and Google Cloud Platform](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/workload-identity-federation.md)**

Authenticate outbound connections to Microsoft Azure and Google Cloud Platform using federated identity.

-   **[Domain-Level Certificate Validation Exclusion](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/outbound-certificate-policies.md)**

Configure SSL/TLS certificate validation for individual outbound endpoints by creating outbound certificate policies, so you can adjust hostname verification, certificate chain validation, and revocation checking for a specific host without changing the global validation policy for every other endpoint.

-   **Issue ID tokens signed with RS256**

Issue ID tokens signed with the RSA SHA-256 algorithm \(RS256\) from the OpenID Provider. Use the ID Tokens in OAuth client applications to verify end-user identity.

-   **[Restrict Basic Authentication access with the Basic Auth Restriction page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/basic-auth-restriction.md)**

Use the Basic Auth Restriction page to strengthen instance security by limiting Basic Authentication access to a defined allowlist. Run the tracking period first to identify users currently relying on Basic Auth, then enable enforcement to block Basic Auth requests that don't match the allowlist. The allowlist covers Web Services Access Only \(WSAO\) users, SNC users, OAuth ROPC flow users, users presenting a valid OTP, and users granted the snc\_basic\_auth\_api\_access role.

-   **[Authenticate MCP clients with external authorization servers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/mcp-3p-auth-concept.md)**

Register an external authorization server as a trusted token issuer for the MCP Server by creating an OIDC Provider Configuration that identifies the provider's issuer URI and metadata endpoint. The MCP Server validates a token from a registered provider locally — confirming the issuer is trusted, the signature is valid, the audience matches, and the token has not expired — without depending on the ServiceNow authorization server. Tokens from issuers that aren't registered and active are rejected.


</td></tr><tr><td>

Autonomous Workforce

</td><td>

-   **[Updated routing criteria configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/modify-aiw-tasks-new.md)**

Enable hand-offs between the AI specialist and human agents if work is better handled by a different group or requires additional human oversight.

-   **Document intelligence added to AI specialist**

Add context to the work assigned to an AI specialist, allowing it to read attachments such as screenshots, PDFs, and error logs to generate responses.

-   **[Configurable profile for a unified AI persona](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/modify-aiw-profile.md)**

Customize your AI specialist's name and icon to fit your brand, and decide on its role and assignment group to determine what data and work it can access.

-   **[Multiple task configurations for fine-tuning AI specialist processes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/modify-aiw-tasks.md)**

Configure pre-built tasks, adding your own routing behavior, response templates, search profiles, and knowledge sources, with no prompt engineering required.

-   **[AI specialist activity and performance monitoring](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/ai-workforce-ais-use.md)**

Track every record your AI specialist touches and measure its performance to see the value it brings to your team across multiple metrics.

-   **[User-based work assignment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/work-assign-aiw.md)**

Create assignment rules to automatically route work to your AI specialist for triage and resolution. It only acts on requests it's confident it can resolve, proposing a solution directly. Anything less certain gets handed off to a human agent.


</td></tr><tr><td>

Build Agent and Autonomous Engineer

</td><td>

-   **[Generate implementations from specifications with Autonomous Engineer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/autonomous-engineer.md)**

Use Autonomous Engineer, powered by Build Agent, to generate a complete implementation plan from your requirements.

    1.  Provide requirements as a prompt or a file upload.
    2.  Autonomous Engineer prompts you with questions to clarify ambiguous requirements, queries your instance to identify existing artifacts. For example, it might ask questions about tables, roles, and catalog items, and generates a plan with work items. Work items include acceptance criteria and test criteria in an Agile user story format.
    3.  After you approve the plan, Autonomous Engineer generates a background agent for each work item. It then builds all work items in parallel in the background, generates and runs ATF tests, and attempts to resolve test failures.
    4.  Items that require human intervention appear in the dashboard and in the chat panel.
    5.  When the plan is complete, an update set is generated for deployment to your UAT or production environment.
Autonomous Engineer uses agent packs to give background agents product-specific domain knowledge during execution. The Custom app development agent pack is available in this release, which gives Autonomous Engineer awareness of platform tables, roles, and configuration patterns specific to custom app development.

-   **[Automatic test generation from plans](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/build-agent-testing.md)**

When you use Autonomous Engineer to plan an application, Test Agent automatically generates Automated Test Framework tests for each work item and acceptance criteria that can be validated through automated testing. Generated tests are executed immediately, and Test Agent identifies and resolves any failures.

-   **[New model support](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ba-models-versions.md)**

Build Agent and Autonomous Engineer now support the following models:

    -   Azure OpenAI GPT 5.6 Sol
    -   Anthropic Claude on AWS Opus 5
-   **[Test suite authoring and execution](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/build-agent-testing.md)**

Create and run ATF test suites from Build Agent and Autonomous Engineer. Group multiple tests under a single suite and execute the suite to run regression testing without selecting individual tests. Execution status and any errors are reported in the chat panel.

-   **[ATF list step support](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/build-agent-testing.md)**

Test Agent can now generate ATF tests that use list and related list test steps, including validate related list visibility and apply filter to list. List step support extends test coverage beyond form-based interactions to include the full list view experience on the ServiceNow AI Platform.

-   **[Support for Box MCP server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/accelerate-design-to-development-with-figma-mcp-server.md)**

Build Agent now supports integrations with Box MCP server.

-   **[Domain separation for ServiceNow Fluent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ba-domain-separation.md)**

ServiceNow Fluent, which Build Agent uses to create apps, now supports domain separation on records and APIs. You can set the **sys\_domain** field and use **sys\_override** fields when working with records in domain-separated environments, so ServiceNow Fluent operates correctly across domains in your instance.

-   **[Additional metadata support](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/build-agent-supported-metadata.md)**

The following metadata are now supported in Build Agent and Autonomous Engineer:

    -   Service Catalog dependent question support
    -   Transition condition
    -   UI style
-   **[Right-click to configure ServiceNow AI Platform metadata](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/access-build-agent.md)**

When you right-click a record or artifact and select **Configure**, the metadata editor now opens in ServiceNow Studio.

-   **[Build Agent \(Trial\) automatically installed](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/exploring-build-agent.md)**

Build Agent \(Trial\) is available by default on all instances, without requiring installation.

-   **[Automatic upgrades for Build Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/install-build-agent.md)**

Build Agent now supports automatic upgrades through the ServiceNow Store. Instances running Australia Patch 5 and later releases or Zurich Patch 12 and later releases that have Build Agent installed receive automatic upgrades when a new version is published.

-   **[Playbook support updates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ba-update-sets.md)**

Build Agent includes the following updates to Playbook support:

    -   Build Agent now consolidates all records related to a playbook into a single XML update set file.
    -   Build Agent can now generate runtime permissions at the playbook level and at the stage level.
    -   Build Agent can now generate and configure the Set Playbook Outputs activity for nested playbooks.
    -   Build Agent can now configure agentic fields on form-based and record-based activities when the AI Agent plugin is active.
    -   Build Agent can now generate on-demand playbook launcher configurations.
    -   Build Agent can now define optional activities in a playbook.

</td></tr><tr><td>

Care Team Work Management

</td><td>

-   **Care team activities playbook**

Define a recurring or one-time activities plan once, such as a daily unit safety check or a routine equipment inspection. The system automatically generates care team cases and tasks for every selected team or unit according to a configured schedule.

Unlike the Operational Rounding playbook, the Care team activities playbook works directly at the care team case and task level. It does not create a healthcare orchestration case, making it suited to single-unit, recurring operational work.

-   **Smart assessments**

Associate a structured, repeatable questionnaire with a care team task to capture standardized evidence, such as room inspections, equipment checks, or readiness surveys. Assessments can also be associated with task plan templates so that every concrete task generated from the template automatically inherits the assessment. Results can be reviewed, compared, and reported on across a unit, an organization, or an entire hospital.

This feature depends on the Smart Assessment for CSM plugin, which is automatically installed with Care Team Work Management.


</td></tr><tr><td>

Case and Knowledge Management

</td><td>

-   ****

</td></tr><tr><td>

Certificate Inventory and Management

</td><td>

-   **[Extended ACME capabilities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/exploring-acme.md)**

Request, renew, and revoke certificates through DigiCert ACME, Sectigo Universal ACME, and Sectigo Public ACME CAs using automated flows. If your organization uses a different CA that is compatible with the ACME protocol, you can add it and use it to extend automated certificate management to that CA.

-   **[CyberArk PVWA private key storage](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/configure-mid-server-automatic-cert-renewal.md)**

Store private keys in CyberArk PVWA during automated certificate operations, in addition to HashiCorp Vault and Azure Key Vault.

-   **[Certificate format support](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/certificate-routing-policy-field-values.md)**

Receive issued certificates in DER binary or PKCS12 format, instead of PEM format.


</td></tr><tr><td>

Change Management

</td><td>

-   **[Compliance dynamic schema](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/compliance-dynamic-schema.md)**

Store risk and compliance details on change requests without adding columns to the Change Request table. Compliance dynamic schema saves these details as name and value pairs in a single field using the platform Dynamic Schema feature. Regulated industries can capture information such as whether a change handles personal data, whether an audit trail is required, and how long a rollback takes. The base system includes example dynamic categories such as Risk and Compliance, Financial Risk and Compliance, and SaaS/Cloud Security Compliance, and example attributes covering areas such as audit trail, downtime, estimated impacted users, lead time, rollback time, and compliance. You can deactivate the examples and define categories and attributes that match your organization's compliance requirements. You can also read and update attribute values from scripts, including risk condition scripts and business rules, using the dynamic schema scripting API.

-   **[Change lockdown](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/change-lockdown.md)**

Change lockdown allows change managers to pause all or a subset of in-flight change requests. Use it during major unplanned IT, critical, or financial events.

-   **[Change lockdown conflict detection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/lockdown-conflict-detection.md)**

Automatically flag change requests that overlap an active lockdown period. Conflict detection runs alongside maintenance window and blackout window checks. Any change request inside a lockdown is marked as an Inside Change Lockdown conflict and placed on hold. Reschedule it outside the lockdown period to clear the conflict and continue processing.

-   **[Scaled change](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/scaled-change-overview.md)**

Scaled Change extends change management to complex environments with many configuration items. A single Scaled Change generates and coordinates child change records for every affected configuration item. It uses scheduling intelligence, conflict detection, and approval workflows to keep large-scale changes on track from planning through closure.

-   **[ITIL change process assignment for change models](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/itil_change_process_models.md)**

Assign an ITIL change process to a change model so the ChangeRequest API uses that model when it creates a matching change request.


</td></tr><tr><td>

Cloud Cost Management

</td><td>

-   **[Make smarter cloud cost decisions with AI-powered summarization of cloud spend](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/spend-summary-otto-ccm.md)**

Get an AI-generated summary of your cloud spend trends, top cost drivers, and budget alignment with your selected filters and groupings. The **Summarize** button enables you to view month-over-month changes, commitments coverage, and the top five recommendations to reduce costs. Use these insights to make more informed decisions about your cloud spend.

-   **[Get complete cost visibility with TCO and unit economics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/business-insights-ccm-ws.md)**

Enhance total spend analysis with TCO insights for your business applications by combining cloud costs with non-cloud costs such as hardware, software licensing, and labor. Upload business data to track revenue, units, and margins alongside your cloud costs using the Unit Economics view. Use the new Business Insights view to analyze spending trends by application owner, business application, department, business unit, and cost center.

-   **[Manage cloud spend attribution with the tag category source selection capability](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/tag-category-source.md)**

Align cloud spend attribution with your organization's enterprise architecture \(EA\) by selecting a tag category source. Instead of manually tagging resources in each cloud provider, derive business context automatically from existing CMDB relationships. This feature eliminates duplicate tagging effort and ensures that cost reports reflect the same taxonomy already maintained in your ServiceNow instance.

-   **[Streamline spend analysis with saved, shared, and reusable report views](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/spend-anaytics.md)**

Eliminate repetitive setup using Spend analytics filters, time ranges, groupings, and cost types and apply your saved views instantly without manual reconfiguration. Set a default view to load your preferred configuration automatically every time you open the Spend Analytics page. Mark frequently used views as favorites or set a default view to streamline your daily workflow.

-   **[Experience reorganized Cloud Cost Management Workspace with intuitive navigation and broader visibility](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/ci-workspace.md)**

Navigate cloud cost data more efficiently with a reorganized structure within the Cloud Cost Management Workspace. Drill down from any home page widget directly into detailed spend analytics.

This enhancement provides the Insights User \(insights\_user\) role read-only access to Optimization and Budget pages so they can review recommendations, unused resources, rightsizing suggestions, and budget data.


</td></tr><tr><td>

Code Signing

</td><td>

-   **[Signature generation during source control commit](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/c_cs_commit_signing.md)**

Generate Code Signing signatures automatically when you commit application files to source control from a trusted instance. Signatures are created for eligible records during the commit and pushed to the remote repository in the same update set as their source records, so a protected instance can validate the records it receives.

-   **[Code Signing change audit data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/cs-vault-audit-data.md)**

Review the create, update, and delete operations that users perform on records protected by Code Signing. Each audit record identifies the changed record, the user who changed it, the operation type, and the date and time of the change. Audit data is recorded by default on production instances when Code Signing is active, and users with the codesigning\_auditor role can view and report on it. A scheduled job manages the size of the audit data based on a configurable retention period and maximum record count.


</td></tr><tr><td>

Collaborative Work Management \(CWM\)

</td><td>

-   **[Create CWM tasks or stories from files or open prompts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/generate-tasks-cwm-boards.md)**

Generate a batch of actionable tasks or stories for a Board by describing the work in an open prompt or uploading a reference file, such as meeting notes, brainstorming planning docs, or epic PRDs. AI analyzes the input, maps the results to your Board columns, and lets you review and select which items to add.

-   **[Create child tasks from CWM task types in List view](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/generate-subtasks-for-cwm-tasks.md)**

Break down a large or complex task into clear, assignable child tasks without manual work breakdown. AI analyzes the task's short description and description and generates the child tasks inline from the List view. This capability is available for CWM tasks and CWM custom task types.

-   **[Manage lists in CWM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/cwm-lists.md)**

Access ready-made default lists of Agile and connected work records, or build and save your own custom lists from any table, without leaving the CWM workspace. The Lists panel under the Quick access section includes the **Default lists** and **My lists** tabs. You can filter, sort, group, and export records, or create and edit records directly from a list.

-   **[Manage work with Board dashboards](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/cwm-board-dashboards.md)**

Every Board now includes a Dashboard tab, alongside List, Gantt, Kanban, and Sprint planning, with two predefined shared dashboards added automatically: Team progress for waterfall work and Team sprint tracker for agile work. Space owners and editors can also create additional dashboards, add predefined or custom widgets bound to any Board column, and rename, duplicate, or delete them. Every dashboard is shared with everyone with access to the Board and can be shared with a direct link.

-   **[Enable sprint data collection for burnup and burndown widgets in a dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/cwm-activate-daily-sprint-data-collection-job.md)**

Activate the **CWM Daily Sprint Data Collection** scheduled job to populate the Sprint burnup and Sprint burndown widgets in the Board dashboards. Once the job is active, data for active sprints is collected daily, and chart data appears starting the day after the job first runs.


</td></tr><tr><td>

Common Governance, Risk, and Compliance features

</td><td>

-   **[Issue workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/issue-workflows.md)**

With GRC Issue Management version 23.0.5, you can configure issue-specific workflows with custom lifecycle states, layouts, guided activities, trigger conditions, approval requirements, and routing rules. Use different workflows for different categories of issues without customizing the issue table.

-   **[Issue approval flows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/issue-approval-flows.md)**

With GRC Issue Management version 23.0.5, you can add an approval checkpoint before an issue or remediation task advances. This applies to state changes or due date extensions. Track approval requests, decisions, and approval history directly on the associated record.

-   **[Entity lifecycle management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/entity-change-management.md)**

With GRC Profiles version 23.0.7, you can review the impact of proposed entity changes on associated risks and controls before applying the changes. Accept the changes or modify the entity filter to help prevent unintended changes.


</td></tr><tr><td>

Container Vulnerability Response

</td><td>

-   **[Enhancements to the Wiz Vulnerability Response Integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/security-management/wiz-container-runtime-exposure-cvr.md)**

Two new chained integrations for the Wiz container vulnerability pipeline:

    -   The Wiz Container Grouped Vulnerability Integration that retrieves vulnerability findings from Wiz that are grouped by image.
    -   The Wiz Container Deployment Context Integration that retrieves the complete deployment/execution context that includes clusters, namespaces, services for each image.
    -   View both integrations in your Vulnerability Integrations list alongside the existing Wiz Container Vulnerability Integration. The integrations are installed automatically and are activated by default.

**Note:** To disable this integration chain, set the sn\_vul\_wiz.deployment\_context\_gate\_writes system property to 'false'. This deactivates the Wiz Container Grouped Vulnerability and Wiz Container Deployment Context integrations so that container vulnerable item creation remains based on your existing settings with the Wiz Container Vulnerability Integration integration.


</td></tr><tr><td>

Continuous Authorization and Monitoring

</td><td>

-   **[Document reuse and version control across records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/c_cam_document_management_system.md)**

Link documents as shared resources across authorization packages, boundaries, and engagements. Set approval workflows to control who reviews and activates documents before they take effect.

-   **[Analyze documents with AI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/t_use_smart_docs_with_documents.md)**

Summarize documents, generate frequently asked questions with answers, or ask specific questions about document content, all from the Documents side panel in an authorization package, boundary, or engagement.

-   **[Voice-based document analysis](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/t_use_smart_docs_with_documents.md)**

Generate spoken audio summaries of documents and conduct voice-based Q&amp;A using the Voice Assist panel, from the Documents side panel in an authorization package, boundary, or engagement.

-   **[Connect documents to external cloud storage](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/t_connect_documents_to_external_cloud.md)**

Link documents from Google Drive, OneDrive, or SharePoint and keep them synchronized with authorization packages, boundaries, and engagements. Pull updates from cloud storage or push approved versions back, without manual downloads and uploads.

-   **[AI-generated authorization package summary](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/t_generate_authorization_package_summary.md)**

Using generative AI, the Authorization package summarization skill generates a summary of authorization package records. Each summary consolidates system purpose, impact level, operational status, and open POA&amp;M counts to show the package's current state.

-   **[POAM user role](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/cam-roles-list.md)**

Users with the POAM User role can view and update their assigned Plan of Action and Milestones \(POA&amp;Ms\), including viewing and updating tasks, accepting or rejecting acceptance tasks, and completing milestone tasks.


</td></tr><tr><td>

Contract Management Pro MCP Server

</td><td>

-   **[Contract Management Pro MCP Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/cmpro-negotiation-mcp.md)**

Review contract documents against organization's standards using an external AI tool connected to Contract Management Pro through the MCP Server. The MCP server retrieves the latest approved Contract Analysis Playbook containing organization's standard terms, approved clause language, and approved fallback language. The AI tool uses the playbook to suggest changes and redline the document.


</td></tr><tr><td>

Core Business Suite

</td><td>

-   **[Knowledge Base in Core Business Suite](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/core-business-suite/kb-cbs.md)**

Provide specific permissions for business unit admins to own and manage Knowledge Base and Knowledge Base articles in different departments within CBS.

The functionality is available with Core Business Suite version 3.3.2 along with ServiceNow Otto® for Setup version 5.0.20.


</td></tr><tr><td>

Customer Contracts and Entitlements

</td><td>

-   **[Contracts and entitlements for buyer organizations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/service-contract-form.md)**

Enable users to create contracts and entitlements for service organizations, in addition to accounts and consumers. When an order fulfilled for a buyer organization is processed to a contract or entitlement, the buyer organization information is populated in contracts and entitlements automatically.

-   **[Enhancements in Modify workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/cce-modify-service-contract-line.md)**

Enhanced Modify workflows by enabling users to modify an entire line, quantity, or end date through a single Modify action. The Modify workflow shows only the changes allowed for the selected lines, based on whether the line is configurable or a simple product.

-   **[Enhancements in Renewal workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/cce-renew-service-contract-line.md)**

Following enhancements have been made in the renewal workflow:

    -   If a customer contract or customer contract line that is terminated before its end date, it is excluded from the renewal workflow.
    -   If a contract line is terminated before its end date, then the renewal quote for that contract line is deleted.
    -   If a contract line is terminated before its end date, then the status of that contract line is updated to **Canceled** when the contract reaches its end date.

-   **Support ServiceNow® Quote Experience for Contracts and Entitlements**

Open quotes created from Customer Contracts and Entitlements lifecycle workflows in the ServiceNow® Quote Experience. Activating the Quote Experience plugin provides you a unified experience for creating, pricing, approving, and quote completion in a single interface. Quotes generated from contract renewal and amendment workflows in ServiceNow® Quote Experience maintains consistent workflows, pricing logic, and governance.


</td></tr><tr><td>

Customer Engagement Sequences

</td><td>

-   **[Lead nurturing email sequence](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/customize-lead-nurturing-email-sequence.md)**

Accelerate lead nurturing by creating an email-based sequence that automates outreach and follow-up. A sample sequence is available with the application. When a lead with an email address is created, the sequence assigns a sequence task to the lead's owner, sends an initial outreach email, and automatically sends a follow-up email if there's no reply. If the prospect still hasn't responded, the sequence escalates to two call attempts, then updates the lead's work notes if no response is received on any channel. The sequence exits as soon as the prospect replies to an email or a call is resolved.


</td></tr><tr><td>

Customer Success Management

</td><td>

-   **[Touchpoint meetings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/acct-lifecycle-events/account-lifecycle-meeting-page.md)**

Automate the generation, updating, and enrichment of conversation briefs by integrating meeting transcripts, emails, and notes. Identify key discussion topics, risks, issues, and action items.

-   **[AI generated success plays](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/acct-lifecycle-events/account-lifecycle-360-view-reco-actions.md)**

Guide customer success managers by recommending AI-generated success plays for users in neutral or positive states. Examples include sustained adoption, high CSAT or NPS scores, or value realization milestones.

-   **[Engagement brief](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/acct-lifecycle-events/account-lifecycle-exec-insight-gen.md)**

Monitor individual engagement health from the Engagement Record Page with a daily AI-generated summary. The summary synthesizes risk, declining metrics, opportunities, team activity changes, and upcoming changes into a prioritized, digestible brief.

-   **[Technology Account 360](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/proactive-service-exp-workflows/technology-account-360.md)**

Use the Technology Account 360 to get a unified view of customer or partner account details combining account health, financial, product usage, and open tasks.


</td></tr><tr><td>

Customer self-service for Sales Customer Relationship Management

</td><td>

-   **[Sales Cart APIs for external ordering systems](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/sales-cart-external-integration.md)**

Create and manage sales carts from third-party consumer portals, partner portals, and headless ordering applications by using the Sales Cart REST API. External systems can create and retrieve carts, add or update line items, delete carts or top-level line items, and submit validated carts to create orders without relying on the Business Portal user interface. Carts created externally use the same records and cart-processing logic as carts created in the Business Portal.

-   **[Digital ordering support for B2C consumers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/sales-cart-external-integration.md)**

Extend digital ordering to B2C consumers by enabling authenticated consumers, in addition to account-and-contact customers \(B2B users\), to build and submit carts through external ordering experiences. Consumer carts derive the currency from the consumer’s country, resolve the price list from that currency, and use address information from the consumer record.

-   **[Billing account and payment profile support](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/sales-cart-external-integration.md)**

Complete orders with line-level billing information by assigning a billing account and payment profile to each cart line item. Different lines in the same cart can use different billing accounts, and both values carry to the corresponding order line items when the cart is submitted, eliminating manual re-entry for downstream billing.

-   **[View contracts and entitlements on the Business Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/contracts-entitlements-self-service.md)**

View and access contracts and entitlements associated with your accounts on the Business Portal. Access contract and entitlement details including contract numbers, pricing details, dates, and contract line items.


</td></tr><tr><td>

Data Catalog

</td><td>

-   **Bulk import and export glossary terms**

Manage large volumes of glossary terms by importing and exporting them in bulk through XLSX files. Preview changes before committing, and get detailed feedback on any rows that fail so you can correct and re-upload. Reduce glossary enrichment time significantly.

-   **Cloud collectors for metadata collection**

Collect metadata from your data sources without hosting and maintaining a MID Server.

-   **Rich text editing and image embedding in data assets**

Document your data assets with rich text formatting and embedded images. Use bold, italics, lists, and links to format content, and embed images directly into catalog fields and resize them as needed.

-   **[SAP HANA metadata collector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/sap-hana-metadata-collector.md)**

Automatically collect and synchronize metadata from SAP HANA using metadata collectors.

-   **[Salesforce metadata collector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/salesforce-metadata-collector.md)**

Automatically collect and synchronize metadata from Salesforce using metadata collectors.


</td></tr><tr><td>

Data Center and Network Asset Management

</td><td>

-   **[Data Center and Network Asset Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/data-center-and-network-asset-management-release-notes-rn.md)**

Data Center and Network Asset Management includes Telecommunications Network Inventory \(TNI\) capabilities. For TNI-specific features and enhancements in this release, see the Telecommunications Network Inventory release notes.

-   **[Enterprise Asset Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/enterprise-asset-management-rn.md)**

Data Center and Network Asset Management includes Enterprise Asset Management \(EAM\) capabilities. For EAM-specific features and enhancements in this release, see the Enterprise Asset Management release notes.


</td></tr><tr><td>

Data Management for CSM

</td><td>

-   **[Restricted Customer Access now controls visibility](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/associate-customers-or-bus-loc-to-so.md)**

Extended the organization customer criteria for a business organization with a new **Restricted Customer Access** check box that controls visibility of customer records. When enabled, business organization staff can view only the customer and consumer records that satisfy the configured criteria at their business organization. This applies to both service and sales personas. Upgrade customers must run the one-time scheduled job, **Remove Legacy roles from Loc Mgr Contrib** to enable restricted customer access configuration.

-   **[New business organization-scoped contributor personas](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/csm-contributor-user-roles.md)**

Added two new roles, Business Org Account Contributor \[sn\_bus\_loc.business\_org\_account\_contributor\] and Business Org Consumer Contributor \[sn\_bus\_loc.business\_org\_account\_contributor\] that grant location-scoped equivalents of the existing Account Contributor and Consumer Contributor roles. With Business Org Account Contributor role, you can create cases for accounts supported by your business organization. You can also track and manage cases created by you for the accounts associated with your organization. With Business Org Consumer Contributor role, you can create cases for consumers or households supported by your business organization. You can also track and manage cases created by you for the consumers or households associated with your organization.

-   **Proactive Customer Service extended to business organizations**

Extended proactive customer service and major case management to business organizations, alongside the existing support for accounts and consumers. When a network alert affects install base items belonging to a business organization, the system can propose a major case and build a recipient list of the affected business organizations. If the major case manager accepts the proposal, they can create a child case for each affected business organization, so all affected business organizations are tracked and updated under a single major case. Business Organization staff can track cases from Business Organization Support Portal.

-   **[Billing account address](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/associate-location-with-billing-account.md)**

Associate one or more locations with a billing account using the new Billing Account Address \[sn\_billing\_account\_address\] table. Each address record captures the address type, identifies the primary address, and tracks whether the address is active or inactive.

-   **[Billing account payment profile](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/add-payment-profile-to-billing-account.md)**

Define payment information for a billing account using the new Billing Account Payment Profile \[sn\_billing\_account\_payment\_profile\] table, which captures the payment method and related payment details for the account.

-   **[Payment responsibility on billing accounts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/add-payment-profile-to-billing-account.md)**

Specify who pays for a billing account with the new Paying party and Paying billing account fields, supporting self, parent, and designated-account payment relationships.

-   **[Billing schedules on billing accounts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/set-up-billing-schedule-for-billing-account.md)**

Define when billing occurs for a billing account with the new Billing Schedule field, which links the account to a platform schedule and its schedule entry records. The new billing account schedule viewer \[sn\_billing\_account.schedule\_viewer\] and writer \[sn\_billing\_account.schedule\_writer\] roles control read and write access to these schedules.

-   **New fields across the Customer Data Foundation tables**

Added fields to the core customer data model tables to support segmentation, life cycle tracking, and external-system integration:

    -   **Account table**: Account stage, Account status, Customer since, Relationship tier, Market segment, Total ACV, and External ID
    -   **Contact table**: External ID
    -   **Consumer table**: Consumer stage, Consumer status, Customer since, Relationship tier, and External ID
    -   **Account Team Member table**: Active, Start date, and End date

</td></tr><tr><td>

DevOps Change Velocity

</td><td>

-   **[Rally authentication with OAuth 2.0](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/setting-up-rally-oauth-2-0-credentials-for-devops.md)**

Authenticate a Rally tool connection using OAuth 2.0 credentials to strengthen your tool security.

-   **[GitHub Data Residency support](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/playbook-enter-github-instance-details.md)**

Connect to GitHub Enterprise Server with data residency controls to keep your organization's code and data in your preferred geographic location.


</td></tr><tr><td>

Developer Sandboxes

</td><td>

-   **[Sandbox pooling for faster provisioning](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/allocating-sandboxes.md)**

Allocate sandboxes faster using pre-pooled instances. When you allocate a sandbox, you claim one from a pre-created pool rather than waiting for a new instance to be provisioned. Sandbox URLs are randomly generated strings and no longer match the sandbox display name. The display name remains configurable, but you can't change the URL.

**Note:** Because pooled sandboxes are precreated, they may be out of date from the current base instance state, but are refreshed every 24 hours.

-   **[Automatic update set sources](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/dsb-update-sets.md)**

Transfer update sets between production and sandbox instances without manual configuration. When a sandbox is created, an update set source pointing to the sandbox is automatically created on the base instance, and an update set source pointing to production is automatically created on the sandbox. When a sandbox is retired, both update set sources are automatically removed.


</td></tr><tr><td>

Discovery

</td><td>

-   **[Configure MID Server parameters for PowerShell 7](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/config-mid-params-ps7.md)**

Configure MID Server parameters to run File-based Discovery and Windows ADME on target hosts that use PowerShell 7. Beginning with Brazil, you can set two MID Server configuration parameters to prefer PowerShell 7 over the default PowerShell 5 on the MID Server and on remote target hosts.


-   **Configure certificate discovery from Discovery Admin Workspace**

Discovery Admin Workspace now supports certificate discovery configuration and management. Configure certificate discovery from a single location instead of switching between workspace and classic interfaces. The new **Certificate Discovery** tab on the Schedules page centralizes schedule management and access to discovered certificates. Certificate discovery can also use URL Monitoring data to automate discovery targets and reduce manual configuration. Existing certificate discovery configurations remain supported, and certificate discovery continues to respect role-based permissions.

-   **[View Shazzam insights in IP inventory](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/daw-ip-inventory.md)**

The IP Inventory page now includes a **Shazzam** tab that displays Shazzam Summary and Shazzam Status data alongside your other IP data. Previously, you had to leave the IP Inventory page and open the Shazzam Insights dashboard separately to review probe results. Now you can check which IPs are alive, active, or unreachable while working with your IP addresses, ranges, and networks in the same view

-   **[View Kubernetes resources in Discovery Admin Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/kubernetes-explorer-dash.md)**

Get a consolidated view of the Kubernetes resources discovered in your environment without leaving the Discovery Admin Workspace. The new Kubernetes explorer dashboard organizes discovered clusters, nodes, namespaces, services, workloads, pods, and Docker images across dedicated tabs. Each tab includes a resource table and visualizations such as data counts, bar charts, and donut charts. Interact with a visualization to filter the table on the same tab. You can also select a resource to open its details page. The details page shows the resource properties and a Dependency View of related configuration items.


</td></tr><tr><td>

Discovery store applications

</td><td>

-   **[New patterns for resource discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/c_MappingPatternsCustomization.md)**

Discover the following resources:

    -   [IBM Flash System storage servers, pools, volumes, network adapters, fibre channel ports, and controllers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/ibm-flash-system-pattern.md)
    -   [AWS Marketplace products \(product type: AMI and SaaS\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/aws-marketplace-pattern.md)
    -   [AWS Linux Server CIs \(cloud discovery\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/aws-linux-server-pattern.md)
    -   [AWS Windows Server CIs \(cloud discovery\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/aws-windows-server-pattern.md)
    -   [Oracle OCI hardware types \(shapes\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/oracle-cloud-hardware-type-pattern.md)
    -   [Oracle Access Manager](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/oracle-access-manager-pattern.md)
    -   [Oracle Coherence](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/oracle-coherence-pattern.md)
    -   [Oracle Enterprise Manager Management Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/oracle-oem-oms-pattern.md)
    -   [Oracle Forms](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/oracle-forms-pattern.md)
    -   [Oracle HTTP Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/oracle-http-server-pattern.md)
    -   [Oracle Internet Directory Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/oracle-oid-server-pattern.md)
    -   [Oracle Node Manager](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/oracle-node-manager-pattern.md)
    -   [Oracle Reports](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/oracle-reports-pattern.md)
    -   [Oracle Siebel CRM Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/oracle-siebel-crm-server-pattern.md)
    -   [Oracle Siebel Gateway Name Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/oracle-siebel-gateway-pattern.md)
    -   [Oracle TNS Listener](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/oracle-tns-listener-pattern.md)
    -   [Oracle Unified Directory](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/oracle-unified-directory-pattern.md)
    -   [Red Hat 389 Directory Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/red-hat-389-directory-server-pattern.md)
    -   [Red Hat JBoss Enterprise Application Platform Host Controller](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/red-hat-jboss-eap-hc-pattern.md)
    -   [Red Hat JBoss Enterprise Application Platform Server on UNIX](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/red-hat-jboss-eap-server-unix-pattern.md)
    -   [Red Hat JBoss Enterprise Application Platform Server on Windows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/red-hat-jboss-eap-server-pattern.md)
    -   [Red Hat Podman](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/red-hat-podman-pattern.md)
    -   [Red Hat Single Sign-On Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/red-hat-sso-server-pattern.md)
    -   [Red Hat WildFly Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/red-hat-wildfly-server-pattern.md)
-   **[OCI UK Sovereign Cloud support](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/create-oci-service-accounts.md)**

Discover Oracle OCI UK Sovereign Cloud accounts by configuring a UK Sovereign Cloud datacenter URL when creating an OCI service account.

-   **[Cisco Nexus Virtual Routing and Forwarding discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/network-router-patterns.md)**

Discover Virtual Routing and Forwarding \(VRF\) instances on Cisco Nexus switches using the "Network Switch" and "Network Router" patterns.

-   **[Kubernetes MID Server cluster high availability](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/kubernetes-discovery.md)**

Discover Kubernetes clusters using a MID Server cluster instead of a single MID Server for high availability and load balancing. Set up using a MID Server cluster by configuring the `sn_itom_pattern.k8s_midserver` property to a MID Server cluster name.

-   **[Oracle Wallet for Oracle Database discovery Windows support](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/oracle-wallet-authentication.md)**

Discover Oracle Databases on Windows using Oracle Wallet instead of storing applicative credentials on the ServiceNow AI Platform. Enable Oracle Wallet authentication by setting the **glide.discovery.oracle\_wallet\_authentication** property to **true**.

-   **[Kubernetes large-payload discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/kubernetes-discovery.md)**

Discover Kubernetes clusters using the "Kubernetes Cluster - Per-Namespace LP" pattern to handle large cluster payloads.


-   **[Discover portable software installed by package managers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/accvc-package-discovery.md)**

Discover software on endpoints that isn't discoverable by traditional checks and policies.

-   **[Create a custom filter rule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/create-custom-filter-rule.md)**

Create a custom software filter rule to exclude irrelevant entries from Discovery in your Software Asset Management \(SAM\) inventory.

-   **[Configure a license key discovery rule and write a parser script](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/configure-license-key-rule.md)**

Verify software legitimacy by creating license keys on your Windows, Linux and macOS devices.

-   **[Categorize software](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/acc-software-categorization.md)**

Use software categorization to group discovered software packages into business-relevant categories. Software categorization helps you avoid manually tagging software and provides administrative teams with an efficient inventory of software records.


-   **Life cycle management for service accounts, IP addresses, and tags**

Life cycle management is supported for service accounts, IP addresses, and tags.

-   **SNK delimiter and key structure migration for CI identification**

Updated SNK delimiter and key structure migration are used for Azure CI identification.

-   **Operating system domain mapping**

Operating system domain is mapped for imported Azure virtual machines.

-   **Naming alignment with Cloud Discovery patterns**

Azure datacenter \(location\) names are aligned with the naming used by Cloud Discovery patterns.

-   **Classification of Azure virtual desktop instances**

Azure virtual desktop instances are classified correctly even when their power state is off. Powered-down VDI resources are now correctly classified and included in imports.

-   **Logical datacenter relationship**

Managed database, multi workspace, and NIC are now related to their logical datacenter.

-   **Import of Azure Microsoft SQL managed instances**

Azure Microsoft SQL managed instances are imported into the CMDB.

-   **Import of multiple log analytics workspaces for a hardware connection**

Multiple log analytics workspaces can be imported for a single hardware connection.


-   **IMDS v2 support for discovery of Kubernetes resources**

Instance Metadata Service Version 2 \(IMDS v2\) is supported for the discovery of Kubernetes resources.

-   **Primary IP address for server records**

The primary IP address is populated in the imported server records.

-   **Operating system domain for AWS compute resources**

Imported AWS compute resources include operating system domain details.

-   **RDS allocated storage capacity information for AWS RDS database resources**

RDS allocated storage capacity information for AWS RDS database resources is populated in the cloud database table.

-   **Lookback time for service accounts**

The lookback time window isn’t applied when processing service accounts.

-   **Amazon FSx file system resources**

Amazon FSx file system resources are discovered and imported into the CMDB.


-   **Patch job discovery**

Patch job discovery doesn’t depend on the deprecated WMIC utility. Patch data is collected on Windows hosts where the WMIC utility is removed or deactivated.

-   **MAC address details added in Network Adapter records**

MAC address details are populated in the imported Network Adapter records.

-   **Mapping of operating system domain details**

Operating system domain details are mapped during imports.

-   **Automatic retry of failed assets during batch API calls**

Assets that fail during a batch API call are excluded and retried automatically.

-   **Lookback time for service accounts**

The lookback time window isn’t applied when processing service accounts.


</td></tr><tr><td>

Dispute Rules Content Pack for Mastercard

</td><td>

-   **New data field for Mastercard transit chargeback eligibility rules**

Assess transit chargeback eligibility using the transit transaction type indicator on the Financial Transaction table. The field is sourced from the **transitProgramCode** field of the Mastercard clearing API and supports Mastercard-defined values 01 through 10.

-   **New input variable for Mastercard chargeback ineligibility rule assessment decision tables**

Evaluate chargeback ineligibility conditions against a fixed Mastercard rule effective date without editing decision tables. The **days\_until\_mastercard\_rule\_effective\_date** parameter calculates the number of days until the rule takes effect. The parameter is used as a decision input across the reason code \(RC\) 4808 Authorization and RC 4837, RC 4849, RC 4870, and RC 4871 Fraud decision tables.


</td></tr><tr><td>

Employee Slate for ITSM

</td><td>

-   **[Use Employee Slate for ITSM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/use-employee-works-itsm.md)**
    -   Answer the questions in a survey assigned to you, save your progress, and submit your responses.
    -   Send email notifications to keep you updated on your walk-in visit.
    -   Send email notifications when a user subscribes or unsubscribes to a service to keep them informed of the subscription status.

-   **[Tech Lounge services](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/use-employee-works-itsm.md)**

Check tech lounge status, join a walk-in queue, or book an appointment using the Tech Lounge page.

-   **[Conversational assisted booking](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/use-employee-works-itsm.md)**

Complete a tech lounge appointment booking or reach the walk-up experience by making a request to Otto in natural language.


</td></tr><tr><td>

Encryption

</td><td>

-   **Edge Encryption proxy now supports Java 21**

Install and run the Edge Encryption proxy on systems with Java 21.0 or later. You can now use newer Java versions for enhanced security and performance benefits. Current supported versions are Java 21.0 or later in the 21.x version series, and Java 17.0.3 or later in the 17.x version series. For installation details, see [Installing Edge Encryption](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/c_InstallEdgeEncryptionProxy.md).


</td></tr><tr><td>

Encryption Key Management

</td><td>

-   **Added Unified Secrets Gateway API for secrets security**

Use the new Unified Secrets Gateway API to organize and control access to secrets through centralized alias groups, identity-based access control, multi-layer authorization, and comprehensive audit logging.


</td></tr><tr><td>

Enterprise Architecture

</td><td>

-   **[Technical debt settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-portfolio-management/eaw-setup-tech-debt.md)**

Control which server and reason criteria the **Populate TRM technical debts in the EA Workspace** scheduled job uses to create Technology Reference Model \(TRM\) technical debt records. Choose whether the job creates one technical debt record per server or a single record per software product regardless of how many servers it runs on, and select which of the standard reasons the job evaluates.

-   **[Persistent technical debt states](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-portfolio-management/eaw-manage-trm-technical-debt.md)**

Technical debt records now persist across scheduled job runs instead of being deleted and re-created. Each record moves between **Active**, **Resolved**, and **Archived** states as the underlying discovered technology or technical debt configuration changes, preserving history for reporting and trend analysis.

-   **[Governing TRM product fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-portfolio-management/eaw-trm-governing-fields.md)**

View the TRM product and product lifecycle that govern a discovered technology's obsolescence status directly on the TPM Technology Lifecycle record. The **Governing TRM Product** and **Governing TRM Product Lifecycle** fields update automatically as matches change on later scheduled job runs.

-   **[Run a scheduled job to update the TCO score range](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-portfolio-management/eaw-run-job-update-score-range-indicator-score.md)**

Starting with this release, the **Business applications by TCO score** widget on the **Portfolio TCO** tab reads the TCO score band from a **Score range** field on the **Indicator Score** record instead of from a database view. If you're upgrading from a previous release, your existing **Indicator Score** records don't have this field populated, and the widget shows **\(empty\)** as the X-axis label instead of the TCO score bands. Run the new **Update Score Range in Indicator Score Table** scheduled job to populate the field on your existing records. This is a one-time, on-demand job that's inactive by default. New installations aren't affected, because the field is populated automatically as indicator scores are generated.


</td></tr><tr><td>

Enterprise Asset Management

</td><td>

-   **[Bulk import enterprise models and assets by using AI-assisted import](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/importing-data-ai-eam.md)**

Streamline the bulk import process for your enterprise models and assets by using AI-assisted import. AI-assisted import automatically analyzes the external model and asset data that you upload into your ServiceNow instance. It then uses AI-powered column and value mappings to automatically align this data with ServiceNow table fields and values, eliminating the need for manual mapping. You can save your completed mappings as templates, further simplifying the import process across future imports. AI-assisted import also provides real-time feedback that helps you identify and resolve errors before you import any data. With AI-assisted import, you can reduce the time and effort that you spend on importing your enterprise models and assets.

-   **[Import enterprise models and assets through enhanced seeded templates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/download-seeded-template-manual-bulk-imports.md)**

Use enhanced seeded templates to manually import enterprise models and assets into your ServiceNow instance. Each template is preconfigured for a specific import scenario and includes a detailed implementation aid, providing immediate guidance on the fields and formatting required for a successful import.

-   **[Install the Enterprise Asset Management application from the Admin Home page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/install-eam-admin-home-page.md)**

Install the Enterprise Asset Management application or any Enterprise Asset Management dependent applications from the Admin Home page. The Admin Home page provides an overview of each application that you're entitled to install and configure.


</td></tr><tr><td>

Extended Security for Enterprise-Wide Deployment

</td><td>

-   **[Additional security on partitioned tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/enable-additional-security-extended-security-ewd.md)**

Enable additional security \(ACL enforcement\) for partitioned tables to strengthen access control validation. Administrators can configure enhanced security on individual partitioned tables \(Project, Demand, Portfolio, Program\) through the **Configure SPM** console under **Partitions** &gt; **Enable additional security**. When enabled, users without partition role access see transparent access-restricted messages and security constraint indicators, including row counts of records hidden due to partition access restrictions. This provides clear governance visibility without exposing sensitive data.

-   **[Supported tables for additional security](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/enable-additional-security-extended-security-ewd.md)**

When enabled additional security on a table, partition role validation becomes mandatory for all users accessing records in that table. Additional security is supported for the following tables.

    -   Project \(pm\_project\) — Enforce partition access on project records and its related records data.
    -   Demand \(dmn\_demand\) — Enforce partition access on demand records and its related records data.
    -   Program \(pm\_program\) — Enforce partition access on program records and its related records data.
    -   Portfolio \(pm\_portfolio\) — Enforce partition access on portfolio records and its related records data.

</td></tr><tr><td>

External Content Connectors

</td><td>

-   **[Connector health dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/resolve-health-issues-external-content-connector.md)**

View and resolve connector health issues using the connector health dashboard.

-   **[Index inspector tool](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/review-indexing-status-content-items.md)**

Verify indexing status and error counts for individual content items using the index inspector tool. Optionally review additional item details, see which users and groups can view the item in secure search, and view retrieval and indexing errors for the item.

-   **[Advanced connection settings for the Amazon S3 external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/create-ext-cont-connector-amazon-s3.md)**

Optionally specify advanced connection settings including the AWS region and Amazon S3 endpoint you want the connector to use. You can also specify a list of Amazon S3 buckets to retrieve content from, or leave this list empty to enable auto-discovery of buckets.

-   **[Delta content crawls for the Google Drive connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/delta-content-crawls-external-content-connectors.md)**

Reduce content crawl time with delta content crawls. Unlike full content crawls, delta content crawls ignore unchanged content items in a connector's source system. Delta content crawls are supported for the Google Drive external content connector.


</td></tr><tr><td>

Financial Services Card Operations

</td><td>

-   **Date facilities were withdrawn**

Dispute agents and cardholders can now record the date facilities were withdrawn by answering the question "Date of the facilities were withdrawn." This question displays only after answering Yes to "Certification that the facilities were withdrawn," and supports chargeback eligibility evaluation for reason code 13.2 \(Cancelled Recurring Transaction\).

-   **Date cardholder checked out from hotel**

Dispute agents and cardholders can now record the date a cardholder checked out from a hotel by answering the question "Date cardholder checked out from hotel." This question displays only for disputes filed as Not as Described \(reason code 13.3\) or for a services dispute, where the merchant is categorized under a hotel or lodging merchant category code \(MCC 7011, or the 3501-3856 hotel-chain range\).

-   **CE Transaction Details**

View compelling-evidence transaction details as a read-back field when reviewing Visa dispute details.


</td></tr><tr><td>

Firewall Audits and Reporting

</td><td>

-   **Fortinet FortiManager vendor support**

Manage and audit firewall rules from Fortinet FortiManager devices. The new vendor support extends firewall auditing and reporting capabilities to Fortinet environments, enabling centralized rule management and compliance reporting across FortiManager-managed firewalls.


</td></tr><tr><td>

Goal Framework for SPM

</td><td>

-   **[Automatic status calculation for targets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/automatic-status-calculation-targets.md)**

Automatically determine target status based on actual achievement percentages. When you enter actual values for a target period, the system compares the achievement percentage against predefined thresholds and automatically assigns a status \(Green, Yellow, or Red\). This eliminates manual status selection, reducing data entry errors and improving organizational governance.

Status is calculated and updated when you enter actual values using the formula: \(\(Actual Value - Start Value\) / \(Planned Target - Start Value\)\) x 100. Target owners can override automatically calculated status values at any time. If you update the actual value after a manual override, the system recalculates the status automatically.

-   **[Configure automatic status calculation thresholds](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/configure-automatic-status-calculation.md)**

Enable administrators to customize automatic status calculation thresholds and enable or disable the feature based on organizational requirements. By default, automatic status calculation is enabled with system-defined thresholds of Green \(≥90%\), Yellow \(75-89%\), and Red \(&lt;75%\).

Administrators can adjust threshold percentages using the system property **sn\_gfa.target.auto\_status.thresholds**. To disable automatic status calculation and revert to manual status selection, set the system property to `false`.


</td></tr><tr><td>

Hardware Asset Management

</td><td>

-   **[Hardware Asset Management installation from the Product Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/install-ham-from-product-hub.md)**

Install Hardware Asset Management and dependent applications from the Product Hub, the central location to view and manage all applications included in your subscription.

-   **[Set up Hardware Asset Management using the Configuration Console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/configure-ham-from-console.md)**

Streamline your asset management setup by configuring all Hardware Asset Management settings from a single location using the Configuration Console. Set up users, roles, asset lifecycle, inventory, asset integrations, and generative AI skills. You can also use the AI conversational interface to configure groups, users, and content service setup.

-   **[Hardware Asset Management integration with Contract Management Pro](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/ham-cm-pro-integration.md)**

Manage your hardware contract lifecycle across renewals, expirations, and obligations by integrating Hardware Asset Management with the Contract Management Pro application. Use the agentic workflow to extract key metadata and obligations from signed contract documents and track contractual commitments proactively to reduce unexpected costs.


</td></tr><tr><td>

Health Log Analytics

</td><td>

-   **[Sustained Alert feedback](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/hla-sustained-alert-apply.md)**

Suppress alerts on short-lived anomaly spikes and receive notifications only when an issue persists continuously. Apply Sustained Alert feedback per metric from the Alert Card or Express List \(single or bulk\), setting a fixed duration threshold to define what counts as sustained.

-   **[Smart Parser Gen AI enhancements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/hla-source-type-structure-adjustment.md)**

Increase confidence in Smart Parser Gen AI alerts by viewing the full parsing and alert generation flow, now backed by expanded automated testing.

-   **[MID-less integration setup through an MCP Client](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/hla-mid-less-integrations-concept.md)**

Admins with access to the ITOM MCP Server Console can use an AI-enabled MCP Client to set up MID-less integrations. You can use any MCP Client, such as AWS Claude, to create MID-less integrations through natural-language prompts, without navigating to the Integrations Launchpad.


</td></tr><tr><td>

ITOM AIOps

</td><td>

-   **[New navigation to the AIOps Managers home page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/service-operations-workspace-ui-itom.md)**

Navigate to AIOps Managers home page through **All** &gt; **AIOps Managers**, where you can onboard new specialists and manage them in one place.

-   **[Monitor agentic workflows with the AI Processing Experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/use-ai-insights-express-list.md)**

Monitor, supervise, and control agentic workflows from one standardized interface. View each workflow's execution state and steps, access its reasoning, and step in to intervene when needed.

-   **[Navigate to filtered alerts from the AI Supervising tab](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/service-operations-workspace-ui-itom.md)**

Navigate to Express List by selecting the action link in each tile on the **AI Supervising** tab. This way, you can investigate alerts faster, as the filters are pre-applied to match the alert category.

-   **[Filter AIOps Manager homepage alerts by assignment group](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/service-operations-workspace-ui-itom.md)**

Oversee multiple teams using a multi-select assignment group filter on the AIOps Manager homepage. Filter by groups you manage, groups you belong to, and unassigned alerts.


-   **[Alert auto-closure reasoning and transparency](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/reopen-ai-closed-alert.md)**

See the decision, reasoning, and supporting evidence for each auto-closed alert, including insignificance reasoning and execution traces, so you can verify autonomous closures.


-   **[Conversational connector setup with ServiceNow Otto](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/pull-connector.md)**

Configure vCenter, NagiosXI, SolarWinds, SCOM, and Zabbix by chatting with Otto in a side panel. You set them up without working through manual configuration fields.

-   **[Activation prompt for pull connectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/pull-connector.md)**

Activate the connector from the modal that appears after a connection test passes. It stays open until you act, so you don't forget to activate.

-   **[Push connector error details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/push-connector.md)**

View the last error message, timestamp, and detailed payload for a push connector. You diagnose and fix failures without leaving the Integration Launchpad.

-   **[Dynatrace Grail problem events](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/dynatrace-advanced-settings-fields.md)**

Create ServiceNow alerts from Dynatrace Grail problem events, with the root-cause entity, all affected CIs, a matching severity, and the problem's current lifecycle status already included. You see the cause and scope up front, so you can respond without investigating from scratch. This connector replaces the classic Dynatrace event integration.

-   **[JSON API support for vRealize](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/t_EMConfigurevRealizeConnectorJS.md)**

Connect vRealize through the JSON-based API. The connector keeps working on future VMware versions. XML remains supported.


</td></tr><tr><td>

ITOM MCP Server Console

</td><td>

-   **[Resolve alerts without leaving your MCP Client](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/itom-mcp-server-alert-actions.md)**

Assign, close, reopen, acknowledge, and annotate alerts through natural-language prompts in your MCP Client application, eliminating context switching between tools. This reduces resolution time and keeps you focused on the incident at hand. The tool automatically detects whether your request applies to a single alert or an alert group, so you can coordinate action across multiple related alerts in one request.

-   **[Coordinate response to related alerts in your MCP Client](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/itom-mcp-server-bulk-alert-actions.md)**

Assign, close, reopen, or acknowledge multiple related alerts as a group in a single request from your MCP Client. When a widespread outage affects several systems, you can route all related alerts to the responsible team and add investigation notes simultaneously. This keeps your response coordinated without repetitive manual work.

-   **[Review service dependencies and incident impact in your MCP Client](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/itom-mcp-server-ci-reliability.md)**

Assess configuration item \(CI\) reliability status, topology, and incident impact directly from your MCP Client application through natural-language prompts. Assess which upstream and downstream services are affected by an alert, so your team understands the full scope of impact before escalating or deciding on remediation steps. Create service level objectives \(SLOs\) for CIs that don't have them yet, and monitor active SLOs and related alerts, all without navigating to the ServiceNow UI.

-   **[Get remediation suggestions in your MCP Client](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/itom-mcp-server-alert-remediation.md)**

Request a remediation suggestion for an alert through natural-language prompts in your MCP Client application. The tool uses your existing workflows and knowledge base articles to recommend the next step, so you can resolve issues faster without navigating back to the ServiceNow UI. Review the suggestion or follow the deep link back to Service Operations Workspace to confirm and execute the remediation action.

-   **[Set up MID-less log ingestion for HLA from your MCP Client](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/itom-mcp-server-hla-ingest.md)**

Create and configure MID-less log ingestion integrations for Health Log Analytics directly from your AI-enabled MCP Client application, without navigating to the Integrations Launchpad. Request integration creation, activation, renaming, and token rotation entirely through natural-language prompts. The MCP Client returns all endpoint and credential details needed to configure your collector, eliminating manual UI navigation for integration setup and credential management.


</td></tr><tr><td>

ITSM MCP Server

</td><td>

-   **[Managing incidents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/manage-incidents-itsm-mcp-server.md)**

Use incident management tools to get details, update fields, and find similar incidents in the ITSM MCP Server.

For example:

    -   Get incident fields including state, priority, assignment, CI, description, and work notes with `incident.get_details`.
    -   Update incident fields and work notes through platform-native APIs with full business rule execution using `incident.modify`.
    -   Search for similar incidents using semantic search with `incident.search_similar`, and look up assignment groups and users with `lookup_assignment_groups` and `lookup_users`.
    -   Search similar Knowledge Base \(KB\) articles using `incident.search_similar_kb`, and retrieve details for a published KB article using `incident.get_kb_details`.
    -   Link a KB article to an incident as a related reference using `incident.attach_kb`.
-   **[Managing change requests](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/manage-change-requests-itsm-mcp-server.md)**

Use change management tools to query, analyze, and update change requests in the ITSM MCP Server.

For example:

    -   Create and update change requests, calculate risk, and manage planned outages with `change.lifecycle`.
    -   Analyze changes by recommending assignment groups, retrieving risk and impact data, and suggesting configuration items and templates with `change.analyze`.
    -   Retrieve, search, and aggregate change data, check schedules and conflicts, and score data quality with `change.query`.
    -   List tasks, affected CIs, approvals, incidents, problems, outages, and change policies with `change.relation`.
-   **[Managing request items](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/manage-employee-experience-itsm-mcp-server.md)**

Use request item tools to create and manage your own tickets in the ITSM MCP Server.

For example:

    -   Create incidents or request catalog items through a guided workflow that includes knowledge base deflection, catalog item redirection, and duplicate detection using `requester.create_incident`.
    -   Escalate an incident's urgency with a mandatory reason using `requester.escalate`.
    -   Add customer-visible comments to your open incidents or requested items using `requester.add_comment`.
-   **[Managing on-call schedules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/manage-on-call-schedule-itsm-mcp-server.md)**

Use on-call management tools to look up coverage and manage your on-call schedule in the ITSM MCP Server.

For example:

    -   Identify current on-call engineers by assignment group or shift name, and view your next or active on-call shift details using `oncall.on_call_lookup`.
    -   Request time off from an on-call shift and arrange coverage through a two-phase analyze-and-create workflow using `oncall.timeoff_request`.
-   **[Using ITSM MCP Server common tools](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/itsm-mcp-server-tools-reference.md)**

Use common tools to use with the ITSM MCP Server.

For example:

    -   Answer structured natural language questions about ITSM data, including details on incidents, change requests, and active catalog items using `itsm_knowledge_graph`.
    -   Approve or reject your oldest pending approval for a change or request items using `task_approval_decision`.
    -   Get the authenticated user's current session time zone and the current date and time in that time zone using `get_session_timezone`.

</td></tr><tr><td>

Impact

</td><td>

-   **[Product adoption](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/product-adoption.md)**

Access core Product adoption functionality, Capabilities Map and Product Adoption Roadmap without connecting to Service Exchange.

    -   View the capabilities map with a list of capabilities and their entitlement status. You can also edit the usage status manually for relevant capabilities.
    -   Create product adoption roadmaps using templates or manually, and manage capabilities for those new product adoption roadmaps.
    -   Receive a consistent message when functionality is limited by unavailable status or inability to edit existing product adoption roadmaps until Service Exchange connects with Guided Setup.
-   **[Latest Accelerators by Release](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/new-accelerators-australia-release.md)**
    -   Accelerate AI adoption and time to value by generating complete applications, surfacing automation opportunities, measuring AI investment impact, and migrating Virtual Agent topics.
    -   Reduce onboarding friction and technical risk by orienting teams to scoped app development and enabling secure, integration-free access to external data sources. Activate Field Encryption Enterprise as a core part of your Vault security strategy.
    -   Strengthen your governance foundation by structuring your CSDM data model, establishing sound IRM Entity Framework design, managing your demand pipeline, and improving Knowledge Management process maturity.
-   **[Platform Health](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/platform-health-idi.md)**
    -   Call the Scan Engine API to provide trigger scans on demand, check scan status and results, and integrate findings into pipeline approval gates.
    -   Use exception approval workflows with explicit Save Draft and Submit actions.
    -   Use configurable exception reason scope controls.
-   **[Value management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/impact-in-platform-business-outcomes.md)**
    -   View the same product line label in Impact Delivery Instance as Impact Store Application for the same product for example, IT Service Management instead of ITSM. Both legacy and current models in Impact Delivery Instance now map to the correct product line taxonomy.
    -   Filter outcomes by version using the new Outcome version filter, available on the Objectives &amp; Outcomes landing page and the Outcome Insights page in Impact Delivery Instance.

</td></tr><tr><td>

Incident Management

</td><td>

-   **[Scheduled job for auto installation of application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/activate-major-incident-management-plugin.md)**

A scheduled job is now available that executes a batch installation on a new instance to automatically install applications such as Major Incident Management only if you have the necessary entitlements for the application. This is applicable only on the newly provisioned zboot instance.

-   **[Auto resolve On-hold incident](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/incident-management-properties.md)**

When an incident is put to **On-Hold** state with reason as **Awaiting Caller Information**, a notification for input response is sent to the caller for a specific number of attempts or strikes within specific time intervals. The business days are considered for a time interval. If the caller adds a comment on the Service Portal or replies to the notification email, the incident automatically moves to the **In Progress** state, and the assigned agent receives a notification. If the caller does not respond after all attempts are exhausted, the incident is automatically resolved with the resolution code **Resolved - No response from caller** and a resolution note indicating no caller response. You can control the number of attempts or strikes and the time interval between the attempts, using the following incident properties:

    -   The number of attempts made before an incident that is waiting for a caller response is automatically resolved if no reply is received. Setting this value to 0 will disable the automation for this instance - By default, the value is set to 3.
    -   Wait period in business days between two attempts. Incidents will be auto resolved after all the attempts are completed - By default, the value is set to 1.
This is applicable only in the zboot instances.


</td></tr><tr><td>

Intelligent approvals

</td><td>

-   **[Create an intelligent approval from a KB article](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/build-workflows/create-an-intelligent-approval-from-a-kb-article.md)**

Use a KB article to create an intelligent approval. Have the system monitor the current state of the KB article and deactivate the intelligent approval when it is out of date or retired.

-   **[Create an intelligent approval from a conversation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/build-workflows/create-an-intelligent-approval.md)**

Create an intelligent approval from the ServiceNow Otto® chat interface.


</td></tr><tr><td>

Kubernetes Visibility Agent \(KVA\)

</td><td>

-   **Software decomposition tool using Syft Scanner**

Analyze container images and generate Software Bill of Materials \(SBOM\) using the integrated Syft Scanner. The new software decomposition tool helps administrators identify software components, dependencies, and vulnerabilities within containerized applications, supporting security compliance and risk management.

-   **FIPS 140 compliance**

Deploy Kubernetes Visibility Agent \(KVA\) with FIPS 140 compliant main informer and daemonset images. These images meet federal security standards for cryptographic modules, enabling deployment in regulated environments that require FIPS 140 compliance.


</td></tr><tr><td>

L1 IT Service Desk AI Specialist

</td><td>

-   **[Routing criteria configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/config-tasks-l1-sd-ai-spec-sow.md)**

Enable hand-offs between the AI specialist and human agents if work is better handled by a different group or requires additional human oversight.

-   **[Routing decision criteria over time analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/perf-overview-l1-sd-ai-spec.md)**

Shows how many incidents over time were reassigned because routing decision criteria matched.

-   **[Performance quality assessment analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/perf-quality-l1-sd-ai-spec.md)**

Review how the AI Specialist measures up in each quality area using automatically generated quality assessments. You can monitor scores, compare different coaching opportunities, and pinpoint areas where quality can be enhanced.


</td></tr><tr><td>

LEAP

</td><td>

-   **[Multi-taxonomy automation projects](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/automation-projects-leap.md)**

LEAP can be configured to ingest and analyze incidents from multiple taxonomies to produce clusters and automation opportunities for all configured taxonomies. Existing single-taxonomy deployments are unaffected. Multi-taxonomy can be configured by admins using LEAP Properties.

-   **[Generate LEAP knowledge base articles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/generate-aiops-leap-knowledge-base.md)**

When creating a KB article from a LEAP automation opportunity, users are prompted to select a knowledge base and category before the article is published, with the author field and article metadata auto-populated from the opportunity record. Admins can configure an list of eligible knowledge bases in LEAP Properties to control which options appear in the modal.

-   **[LEAP MCP Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/aiops-leap-mcp-server-overview.md)**

LEAP skills are now accessible to external clients through MCP tools, enabling integration with third-party systems and workflows.


</td></tr><tr><td>

Localization Workspace

</td><td>

-   **[Globalization Terminology Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/lw-terminology-agent.md)**

Use the generate glossary skill with Globalization Terminology Agent to create a glossary of English-language terms. Review and approve the terms and their definitions that the skill extracts from Knowledge Base articles. Store and edit the glossary in Language Asset Management.


</td></tr><tr><td>

MCP Server Console

</td><td>

-   **[Monitoring dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/monitoring-dashboard.md)**

Explore MCP Server monitoring dashboard to review the performance and usage of the MCP servers and tools in a specific time frame.

-   **[Create client authorizations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/create-client-authorizations.md)**

Explore an alternate way of OAth creation with Client Authorization option by integrating OAuth Client registration directly within the MCP Server Console. This feature eliminates the need to switch between different consoles.


</td></tr><tr><td>

MCP for Strategic Portfolio Management

</td><td>

-   **[SPM MCP server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/spm-mcp-server-landing-page.md)**

Connect any MCP-compatible AI assistant to your ServiceNow instance to query Strategic Portfolio Management data through natural language, without opening the ServiceNow application. The SPM MCP server ships as a standalone application \(com.sn.spm.mcp\) and is managed through the MCP Server Console console.

-   **[Goal tools](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/exploring-spm-mcp-server.md)**

Retrieve goals and generate AI-powered insights directly from your AI assistant. The Get Goals tool retrieves goals and objectives filtered by owner, department, or strategy. The Generate Goal Insights tool generates AI-powered insights for goals and targets by cross-referencing historical data and identifying trends.

-   **[Portfolio tools](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/exploring-spm-mcp-server.md)**

Retrieve portfolio plans and generate insights to support strategic decision-making. The Get Portfolio Plans tool retrieves portfolio plans including resource allocation and timeline details. The Get Portfolio Insights tool surfaces at-risk projects, delayed starts and ends, and dependencies to highlight potential bottlenecks.

-   **[Project tools](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/exploring-spm-mcp-server.md)**

Query project data and generate AI-driven reports and risk assessments from your AI assistant. The Get Projects tool retrieves projects with associated metadata such as ownership, deadlines, and budget constraints. The Generate Project Insights tool detects project risks and analyzes status trajectory using predictive modeling. The Get AI Status Report tool generates a Red, Amber, Green \(RAG\) status report across resources, cost, schedule, and scope. The Identify Project Risks tool detects AI-identified RIDAC risks and saves them to the risk table as AI drafts.


</td></tr><tr><td>

Mobile Platform

</td><td>

-   **[Voice to form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/mobile/voice-to-form.md)**

Fill an entire mobile form by speaking aloud using voice to form. On-device AI maps what you say to the correct fields, and you can review and edit the results before submitting the form.

-   **[Support for Microsoft Entra Shared Device Mode](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/mobile/shared-device-device-level.md)**

Enable secure multi-user device sharing with Microsoft Entra Shared Device Mode. Users authenticate once at the device level, and Microsoft Entra-enabled apps use this authentication as part of their own sign-in process. When users sign out, data is cleared across all apps, preparing the device for the next user. This setup is applicable for areas like kiosk and shift-based deployments managed through Microsoft Intune.


</td></tr><tr><td>

Next Experience Components

</td><td>

|Component|Description|
|---------|-----------|
|Telecom Customer 360|Provides telecom agents with a unified view of a customer account including contact details, interaction history, billing information, subscribed products, and related records.|

</td></tr><tr><td>

On-Call Scheduling

</td><td>

-   **[Delivery status tracking for On-Call Scheduling notifications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/delivery-status-tracking-oncall.md)**

Track on-call escalation notification delivery status from dispatch through acknowledgment across all supported channels. View failure reasons for each contact mode when notifications fail to reach recipients.


</td></tr><tr><td>

Operational Resilience

</td><td>

-   **[Enable contributor assignment in DRIR assessment cases](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/work-on-action-tasks.md)**

Assign contributor and collaborator roles to streamline multi-stakeholder DRIR investigations. You can now assign contributors and collaborators to DRIR assessment instances, with role-based access controls ensuring appropriate team members can participate. This simplifies accountability and coordination during incident responses.

-   **[Tracking field-level changes in linked source records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/integration-with-incident-management.md)**

Maintain DRIR cases current with evolving incident data by tracking field-level changes in linked source records. The application detects modifications to incidents after case creation, generates audit trail records with complete change details, and displays pending updates in a banner within the workspace.

-   **[Enhance regulatory compliance and data quality for DORA reporting](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/properties-dora.md)**

Improve financial data accuracy with better decimal handling, automated snapshot exports, and data quality warnings.

-   **[Define terminology for ROI export](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/opres-dora-roi-ter-def.md)**

Document register-of-information terminology directly in the workspace. Only the **Description** field is editable for each term. Term definitions are automatically included in the `B_99.01` CSV export through a scheduled quarterly job.

The scheduled job that generates this export is inactive by default; an administrator must activate it before it runs. The default frequency is quarterly, but administrators can adjust it. No email notification is sent for this job, because it runs as a system action rather than a user-initiated action.


</td></tr><tr><td>

Operational Technology Setup

</td><td>

-   **[OT use case for ServiceNow Otto for Setup](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/operational-technology/ot-sn-otto-setup.md)**

You can access the Admin Home, Product Hub, and OT Configuration Console to help automate the completion of admin tasks, such as user creation, group creation, and user or group role assignments.

**Note:** For ServiceNow Otto users, you can use the ServiceNow Otto panel for assistance. For non-ServiceNow Otto users, ServiceNow Otto panel isn't available for use.


</td></tr><tr><td>

Opportunity Management

</td><td>

-   **[ServiceNow Otto support on Opportunity Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/crm-conversational-query.md)**

Retrieve, update, and create opportunity records and related CRM data from ServiceNow Otto using natural language.


</td></tr><tr><td>

Partner Relationship Management

</td><td>

-   **[Register a deal using agentic AI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/register-deal-using-agentic-ai.md)Deal Registration AI agent**

Accelerate deal registration with an AI agent that assists users with deal intake, validation, and record creation. This helps reduce manual effort by guiding users through the deal registration process and supporting more accurate deal submissions.

The agent captures deal details, validates records, summarizes information for review, and creates the deal. If validation fails or additional information is needed, the agent suggests corrective actions.

-   **[Channel Partner components on workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/channel-partner-components.md)Partner criteria for deals**

Added filtering rules to control partner access to accounts and consumers when creating deals. These rules help verify partners select only relevant records, reducing errors and supporting cleaner transaction creation.


</td></tr><tr><td>

Portfolio Planning

</td><td>

-   **[RIDAC for portfolio plans](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/portfolio-plan-ridac-ppw.md)**

Access portfolio risks, issues, decisions, actions, and requested changes \(RIDAC\) directly from the portfolio plan using the dedicated RIDAC page within the portfolio plan. View all portfolio governance items in a single, integrated interface without navigating to the separate RIDAC menu. The RIDAC page reduces context-switching and improves portfolio visibility by consolidating governance data. The portfolio plan RIDAC displays the RIDAC items that match the portfolio plan's criteria or belong to the planning items of that portfolio plan.

-   **[Show or hide RIDAC page of a portfolio plan](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/show-or-hide-the-features-for-your-portfolio-plan-ppw.md)**

As a portfolio manager, show or hide the RIDAC page of your portfolio plan. This capability helps you share only the portfolio plan data that matters to your stakeholders and restrict access to the other data.

-   **[Programs enhanced experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/program-portfolio-plan-ppw.md)**

Access dedicated program planning views automatically created with zero setup. Navigate to the new Programs menu and click any program to open its dedicated plan with Prioritization, Roadmap, and Financials views. New programs get plans instantly; existing programs receive them through an automatic one-time backfill \(500 at a time, newest first\). Role-based access ensures users with the sn\_align\_core.ap\_read\_only role can read, users with the sn\_align\_core.apw\_user role can manage items, and program managers are automatic plan owners.

-   **[Program-scoped data with fiscal calendar support](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/program-portfolio-plan-ppw.md)**

View and manage program-scoped planning data in a focused, streamlined interface. Program plans display only that program's planning items. The Financials tab defaults to your fiscal calendar; if the fiscal calendar doesn't span the program dates, the system gracefully falls back to Gregorian with an explanatory message. Making the portfolio plan public and scenario planning for these program portfolio plans are hidden.

-   **[Automated email notification for scenario approval](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/approve-a-scenario-in-portfolio-planning.md)**

Receive email notification when a scenario is approved. The system sends the notification to the scenario approver and portfolio owner. During the approval process, the portfolio plan becomes read-only to prevent unintended modifications and maintain data integrity.

-   **[Copy and customize the demand summarization skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/clone-customize-demand-summarization-skill-ppw.md)**

Tailor demand summaries to your organization's process by copying the base demand summarization skill and customizing it with your own input fields, related entities, and prompt. When you activate a copy of the demand summarization skill, the previously active skill, either the base skill or an earlier copy, is automatically deactivated. Only one version of the skill can be active at a time.

-   **[Work with demands in Employee Slate](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/my-demands-widget-ppw.md)**

Create and track demands without leaving the conversation-first Employee Slate workspace. Describe the demand in a conversation to have matching catalog items identified and relevant fields prepopulated from your message, then track its status, activity, and progress using the new My Demands widget on your canvas or the standard Requests widget. Demands appear in Employee Slate only when both Project Workspace and Employee Slate Core apps are installed.


</td></tr><tr><td>

Predictive Intelligence

</td><td>

-   **[Test time explainability](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/predictive-intel-test-time-explain.md)**

Understand the reasons your machine learning solution made a specific prediction with Test time explainability, which returns a list of input features that influenced the prediction. Applies to Classification solutions only. Example script provided.


</td></tr><tr><td>

Pricing Management

</td><td>

-   **[Automatic addition of derived product lines](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/configuring-related-product-pricing.md)**

Accelerate quoting for derived pricing by automating the creation and alignment of derived product lines. Sellers add the source products and the derived product to the transaction. The pricing engine then generates the required derived lines, aligns their dates to the source lines that fund them, and keeps them synchronized as the sources change. The engine automatically splits derived lines when a source is ramped or amended, ensuring date ranges remain aligned across all related lines.

Previously, sellers manually calculated and aligned dates for derived lines. If a derived line's dates did not align with its sources, the line was excluded from the price calculation.

System-generated lines are marked with the System generated \[**system\_generated**\] field set to true, which distinguishes them from seller-added lines.

-   **[Configurable rounding precision for non-currency pricing fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/pricing-management-properties.md)**

Configure the rounding precision applied to non-currency pricing fields, such as margin percentage, to match your organization's rounding requirements. The default precision is 4 decimal digits. To use a different precision, set the **sn\_csm\_pricing.rounding.non\_currency\_max\_precision\_digits** property in the system properties. Viewing or setting this property requires the Price List Administrator \(sn\_csm\_pricing.pricelist\_administrator\) role.

-   **[Floor and ceiling price in the pricing response](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/sales_crm_pricing-POST-compute-price.md)**

Access floor and ceiling pricing values directly in pricing responses and persist them on custom quote or order line fields for downstream business processes and validations. To include these values in the response, the include\_floor\_ceiling pricing request setting must be set to true. When the setting is absent or false, floor and ceiling price are omitted from the response. If pricing\_elements setting isn't specified in the request, the PRICE element is included by default.


</td></tr><tr><td>

Privacy Management

</td><td>

-   **[AI-reviewer assist for control objective and risk statement recommendations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/ai-reccos-for-pia.md)**

When a privacy assessment task moves to the Review state, the assigned reviewer can generate AI-recommended control objectives and risk statements for the associated processing activity.

The Control Objective Recommender and Risk Statement Recommender skills analyze completed assessment responses and surface relevant records from the privacy library. Each recommendation includes an AI suggestion guide that explains why the record was suggested, citing the specific response or record detail that triggered it.

Each risk statement recommendation also surfaces related control objectives that serve as mitigating controls for the identified risks. When you accept a risk statement, this control-to-risk mapping is carried over to the processing activity.

Accepted records are automatically added to the Applicable scope tab on the assessment task. After you close the task, the corresponding controls and risks are automatically scoped to the processing activity.

-   **[Record data transfers in processing activities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/data-transfers.md)**

Data transfer records capture the movement of personal data between hierarchy nodes in a processing activity. These records are generated automatically from a privacy assessment when a business user defines relationships that send or receive personal data. Adding data subject types and their locations to these relationships generates additional transfer records, which capture each distinct movement between nodes and data subject locations.

You can review the records in the Data transfers tab of the privacy assessment task and remove those that don't apply. After you close the assessment task, the remaining transfer records appear in the **Regulatory details** &gt; **Data transfers** tab of a processing activity. You can also manually add or remove data transfers from this tab.

-   **[Transfer mechanisms for data transfers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/transfer-mechanisms.md)**
    -   Privacy analysts can add a transfer mechanism to a data transfer record to associate the legal safeguard that regulate the movement of personal data.
    -   Privacy managers can add new transfer mechanisms in the Privacy Workspace or update existing ones.
-   **[Multi-language support in the Personal Data Rights \(PDR\) external-facing form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/translate-pdr-form-text.md)**

The external-facing PDR form now supports translations in multiple languages. The selected language drives the form text, including labels, instructions, options, and error messages.

-   **[Mandatory fields in the Personal Data Rights \(PDR\) external-facing form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/map-request-type-to-ds.md)**

Configure mandatory and optional fields for each request type. Requesters must complete all mandatory fields on the external-facing PDR form to submit their request.


</td></tr><tr><td>

Process Mining

</td><td>

-   **[Meter-based usage guardrails and controls introduced](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/meter-based-guardrails.md)**

Configure table-level guardrails and mandatory filters to control entitlement usage and prevent unexpected overage charges. Projects with configured guardrails are automatically validated, capped, or flagged before mining starts.

-   **[Process Mining for Playbooks enhanced](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/playbook-project.md)**

Playbook projects are enhanced:

    -   to configure and analyze breakdowns based on the trigger record of a playbook
    -   to filter playbook executions by recency to focus on current performance trends
    -   to view execution-time histograms for each activity and phase to identify performance patterns and outliers
    -   to compare playbook variants on overall and per-activity efficiency
-   **[Evaluation project experience improved](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/evaluate-pm.md)**

Explore evaluation projects directly from the Process Mining workspace landing page, with guided onboarding that highlights key areas of the interface and suggests where to start exploring. Human Resources and Security Operations users get personal evaluation projects scoped to their own data access, so no administrator impersonation is required.

-   **[AI-assisted process configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/gen_process_config_ai.md)**

Generate process configuration field values with AI directly from the process configuration header, then review, select, and confirm the suggested fields before applying them. Map states to stakeholder responsibilities with AI in the Process details step.

-   **[Launch Process Mining from any ServiceNow workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/list-proj-crt.md)**

Create a Process Mining project directly from a list of records from any ServiceNow workspace.

-   **[Project sharing with edit rights](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/share-project.md)**

Share a project with other users as **Can view** or **Can edit**. Users with edit rights can modify the project definition and perform mining, but can't share or delete the project.

-   **[Contextual Task Mining project names](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/task-mining-naming.md)**

Task Mining projects launched from Process Mining include the triggering node or improvement opportunity name in the project name, making it easier to distinguish between multiple task mining projects.

-   **[Template creation and management introduced](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/pm_templates.md)**

Create multiple templates per table to support several distinct use cases instead of one generic configuration.

-   **[Preset filters for transitions introduced](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/filter-auto.md)**

Create filters from the available filters after selecting the Select quick starter from Process steps in Analyst workbench. This makes the process of creating filters easier and faster.

-   **[Three new system properties added](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/components-installed.md)**

The following three system properties are added:

    -   promin.metered\_usage.allow\_unrestricted
    -   promin.metered\_usage.warning\_limit
    -   promin.workspace.hide\_from\_navigation

</td></tr><tr><td>

Product Catalog Management

</td><td>

-   **[Extended product life cycle states for product offerings and specifications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/extended-product-lifecycle-states.md)**

Validate product offerings and specifications before publication by moving them through the In Test and Staged life cycle states. Build and test catalog hierarchies without publishing unfinished records, helping reduce unnecessary revisions and prevent incomplete catalog content from becoming available to users.

-   **[Channel-specific availability for product offerings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/channel-specific-availability.md)**

Coordinate phased product launches by releasing a published product offering to different distribution channels on different dates. Use channel overrides to align product availability with channel readiness, training, partner enablement, or regional rollout plans without delaying channels that are ready to launch. The offering stays hidden from a channel, in both catalog search and AI Search, until that channel's release date arrives.

A new table, Product Offering Channel Override \[sn\_prd\_pm\_product\_offering\_channel\_override\], has been introduced to support this feature.

-   **[Localized product catalog experiences](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/enable-multi-locale-catalogs.md)**

Generate language-specific versions of product catalogs and product offerings when they are published so sales agents can view product names, descriptions, and characteristics in their preferred language across configurator screens, carts, and quotes. If translated content isn't available for a language, the default-language version is displayed automatically.

The following new tables have been introduced to support this feature:

    -   Product Offering Translation \[sn\_prd\_pm\_product\_offering\_translation\]
    -   Product Offering Catalog Translation \[sn\_prd\_pm\_product\_offering\_catalog\_translation\]
-   **[Customize the display order of product offerings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/som-managing-product-catalogs.md)**

Help sales agents find relevant product offerings faster by defining how offerings appear in the Catalog UI, both on the CRM Workspace and Business Portal. Sales agents can sort product offerings by Display Order, making it easier to surface prioritized offerings while creating quotes and orders instead of sorting alphabetically. A catalog or category without a configured order continues to sort alphabetically.


</td></tr><tr><td>

Product Support for Technology

</td><td>

-   **[Executive Portfolio view](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/proactive-service-exp-workflows/executive-portfolio-page.md)**

The Executive Portfolio page provides account teams and leadership with a real-time view of account portfolio performance. Use this page to identify at-risk revenue, track renewal readiness, monitor product adoption, and understand customer experience trends.


</td></tr><tr><td>

Project Portfolio Management

</td><td>

-   **Budget Overrun insight card**

Identify portfolio plans at risk of exceeding their approved budget with the new Budget Overrun insight card in Portfolio Insights. The card compares each planning item's current fiscal year forecast against its approved budget and flags items where the forecast is higher. Flagged items include a root cause analysis — grouped by cost type and driven by factors such as rate changes, effort overruns, or foreign exchange impact — along with recommended actions like re-forecasting with finance or initiating change control.

-   **Cost Variance insight card**

Identify cost plans whose actual spend is running over or under plan for the current fiscal period with the new Cost Variance insight card in Portfolio Insights. The card flags cost plans where the variance between actual and planned costs exceeds a configurable threshold, in either direction, and groups the root causes by driver — such as rate-driven, effort or hours overrun, or actuals below plan — along with recommended next steps for each.

-   **[Copy and customize the demand summarization skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/clone-customize-the-demand-summarization-skill-ppm.md)**

Tailor demand summaries to your organization's process by copying the base demand summarization skill and customizing it with your own input fields, related entities, and prompt. When you activate a copy of the demand summarization skill, the previously active skill, either the base skill or an earlier copy, is automatically deactivated. Only one version of the skill can be active at a time.

-   **[Work with demands in Employee Slate](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/my-demands-widget-ppm.md)**

Create and track demands without leaving the conversation-first Employee Slate workspace. Describe the demand in a conversation to have matching catalog items identified and relevant fields prepopulated from your message, then track its status, activity, and progress using the new My Demands widget on your canvas or the standard Requests widget. Demands appear in Employee Slate only when both Project Workspace and Employee Slate Core apps are installed.


</td></tr><tr><td>

Project Workspace

</td><td>

-   **[List view for centralized navigation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/use-projects-pw.md#section_oz3_352_kkc)**

Centralized location for accessing all project-related entities such as My projects, All projects, Project templates, and RIDAC categories \(Risks, Issues, Decisions, Actions, Request changes\), streamlining navigation and improving productivity. Create and save custom lists in the My lists tab to organize your work according to your preferences.

-   **[Recalculate planned costs for projects](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/fin-recalculate-costs-pws.md)**

Recalculate the cost plans, benefit plans, and their rolled-up investment-level values directly from the Financials view using the **Recalculate costs** option.

-   **[Create dynamic docs template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/create-a-status-report-template-project-workspace.md)**

Customize the docs based on your organization and project requirements using the dynamic docs template in Project Workspace.


</td></tr><tr><td>

Public Sector Digital Services

</td><td>

-   **[Rolling grant approvals](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/government-industry/psds-gm-rolling-grant-approvals-concept.md)**

The Rolling grant approval feature enhances the grants management funding workflow. It gives grant program managers the flexibility to propose awards and declines for any scored subset of applications at any time. Grant program managers no longer need to wait for the entire proposal portfolio to complete review. They can process funding decisions incrementally as proposals are scored, or continue working in the traditional full-portfolio model.

The feature introduces the Funding Allocation Request as a new record type — an approval packet that groups a subset of proposals for Grant Program Director review. The Grant Program Director can approve the Funding Allocation Request or reject it. Rejection returns all proposals in the batch, regardless of whether they were on the funding or decline track. The proposals in the rejected batch feed back into the Grant Program Manager's working queue, re-entering the funding pool for future review and funding allocation opportunities. The Funding Allocation Requests introduce an alternative to the previous all-or-none approval model and enable continuous, long-running grant programs to operate on a single program record.

Release result letters per proposal for Rolling grant approval scenarios in Grants Management. Once a proposal’s funding or decline decision is approved through its Funding Allocation Request \(FAR\), the corresponding letter can be issued to that applicant. Award, decline, or ineligibility letters can be issued independently without waiting for program-wide completion.

-   **[Investigative Case Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/government-industry/psds-explore-inv-case-management.md)**

Create an investigative case using Investigative Case Management. Investigative Case Management guides investigators through the process of organizing, tracking, and resolving investigations, ​developing case details,​ assigning investigators and team members​, and track evidence with logging and metadata. The following features are available as part of Investigative Case Management:

    -   Entity Management
    -   Evidence Management
With Entity Management, investigators can create investigative tasks and workflows for investigative activities with automated metadata capture \(time, source, entities, classification\)​, as well as define processing with teams and attorneys and collaborate across agencies/divisions. With Evidence Management, investigators can log and triage evidence metadata \(digital, physical, testimonial\)​ and maintain an audit trail \(Chain of Custody logging\), as well as draft, review, and create reports with supporting evidence​​.

-   **[Task Tab and Field Service Management case escalation in Investigative Case Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/government-industry/psds-using-icm.md)**

Use the Tasks tab in the investigative case record to view and create investigative tasks directly within the case context. Use the **Create Work Order** to escalate a case directly to an Field Service Management work order without leaving the ICM workspace​​.

-   **[ServiceNow product tiers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/ai-native-sku-overview.md)**

The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets, and create your own
Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.

-   **[Use ServiceNow Otto for Public Sector Digital Services \(PSDS\) Skills to create case narratives and screen documents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/government-industry/now-assist-psds-using.md)**

Complete case narratives and make refinements to investigative case records using ServiceNow Otto for PSDS Gen-AI skills. Investigators can streamline case narrative refinement by editing content, adjusting tone, and regenerating the narrative for clarity and completeness.

-   **[Use the Case Narrative Refinement AI Agent to refine case narratives in Investigative Case Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/government-industry/psds-using-na-refine-icm-case-narrative.md)**

Produce clear, accurate, and well-structured case narratives using the Case narrative refinement AI agent, embedded within the case record page. This AI agent analyzes existing narratives and related case data to suggest improvements in clarity, structure, tone, and completeness, and highlighting gaps and inconsistencies.

-   **[Document Screening AI Skill for Social Benefits Playbook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/government-industry/psds-ai-skill-doc-screening.md)**

Validate large volumes of uploaded documents, verify information, flag issues, and highlight key details using the Document Screening AI Skill in Social Benefits Playbook, part of ServiceNow Otto for Public Sector Digital Services \(PSDS\).

-   **[GOV.UK Developer Toolkit GDS Service Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/government-industry/psds-gdsp-overview.md)**

Launch citizen-facing services using the GOV.UK Developer Toolkit. This collection of pre-built, GDS-compliant portal widgets enables developers and partners to build service portals for UK government agencies. The GOV.UK Developer toolkit includes standardized components such as homepage, FAQs, Registration, Profile, login, case detail, knowledge search, and record producers. Use these components to assemble portals that meet UK accessibility and design standards and comply with GOV.UK Design System patterns. The toolkit is WCAG 2.2AA compliant and supports 400% zoom and reflow.

-   **[Granular configuration admin roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/government-industry/roles-installed-with-public-sector-digital-services.md)**

Several new granular admin roles enable admins to complete administrative configuration tasks on the Public Sector Digital Services platform without requiring the full admin role. These granular access roles enable a high-level administrator to define and assign custom roles that contain only the specific permissions a user needs. This decreases the number of users with full administrative power over the instance. For more information on granular admin roles, see [Granular admin roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/granular-admin-roles.md).


</td></tr><tr><td>

Purchase Order Management

</td><td>

-   **[Automated purchase order confirmation creation from emails](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/source-to-pay-operations/automated-po-confirmation-creation-emails.md)**

Reduce manual tracking of supplier emails by automatically converting emails with purchase order details into draft confirmations.

-   **[Create a purchase order confirmation in Supplier Collaboration Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/source-to-pay-operations/create-po-confirmation-in-supplier-portal.md)**

Provide buyers certainty about their orders by creating purchase order confirmations directly from the Supplier Collaboration Portal.


</td></tr><tr><td>

Retail

</td><td>

-   **SPM-RO Better Together**

SPM-RO Better Together surfaces Customer Service Management and Strategic Portfolio Management project data inside Retail. Store personas can browse the store opening, closing, renovation, and relocation \(OCRR\) projects for their store, drill into individual project tasks, and assign, take, or close those tasks.

The experience is available in the Retail Service Portal and in Retail Mobile. It is a consumption layer over the CSM/SPM project tables — Retail adds no tables, roles, or access control rules of its own, and project visibility remains governed by the CSM/SPM access control layer.

-   **Track Plan dashboard**

Track the progress of a store plan in a single view from the **Track Plan** tab of a plan. The plan progress summary shows the percentage of store cases closed and the number of open, overdue, closed, and all store cases for the selected occurrence, and you can filter the summary by occurrence. Select a metric to open the matching list of cases.

The hierarchical list view provides a navigation tree of the cases and tasks in a plan, with **Open**, **Overdue**, **Closed**, and **All** tabs. The tree is plan-type agnostic and adapts to current and future plan types, including the plan types that you configure. The plan progress summary applies to the base-system HQ Communications and Store Audit plan types. Plan types with custom configurations or custom case or task states might require additional configuration.


</td></tr><tr><td>

Sales Agreement

</td><td>

-   **[Sales agreements for buyer organizations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/sales-agreement-mgmt-using.md)**

Users can create a sales agreement from a quote created for a service organization. The buyer organization and channel partner information from the quote is automatically carried over to the sales agreement.


</td></tr><tr><td>

Sales CRM Mobile

</td><td>

-   **[Home dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/view-your-day-sales-crm-mobile.md)**

View a personalized home dashboard summarizing your day, including today's meetings, tasks due, and opportunities in focus.

-   **[Manage sales records on Sales CRM Mobile](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/manage-accounts-consumers-contacts-sales-crm-mobile.md)**

Manage Accounts, Contacts, Leads, and Opportunities, including opportunity line items and pipeline health, directly from mobile list and record views.

-   **[Offline support](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/mobile-experience-sales-crm.md)**

Enable sales professionals to access the Sales CRM Mobile application in the offline mode to access their sales records when you don't have an internet connection.

-   **[ServiceNow Otto support](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/servicenow-otto-sales-crm-mobile.md)**

Access ServiceNow Otto to view an AI-generated summary and win probability scores and contextual insights for opportunity and lead records. You can use these insights to prioritize pipeline opportunities and identify risks. You can ask questions about your Accounts, Contacts, opportunities and more. ServiceNow Otto understands the context of the record you are viewing and responds accordingly enabling you to have a conversation.


</td></tr><tr><td>

Security Incident Response

</td><td>

-   **[MITRE ATLAS framework](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/security-management/about-mitre-atlas.md)**

Detect, classify, and respond to AI- and ML-specific threats — such as prompt injection, model poisoning, data extraction, and adversarial attacks — using the MITRE ATLAS framework alongside MITRE-ATT&amp;CK. ATLAS techniques associated with a security incident appear in the MITRE node map, incident timeline, and MITRE info card with a distinct icon. This lets you tell MITRE-ATT&amp;CK and ATLAS techniques apart at a glance. Administrators can configure ATLAS-related properties on the Threat Intelligence Properties page.

-   ****
-   **[Analyze security incident data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/security-management/analyze-data-sir.md)**

Ask questions about your security incident data in a conversational language, without writing queries or knowing how reports are structured. Ask follow-up questions in the same session or move to a different question. AI-generated responses include insights and recommendations rather than only direct answers.

-   **[Review Security Incident AI ROI Summary dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/security-management/ai-roi-summary-dashboard.md)**

Track the value your team realizes from the AI features under Security Incident Response Management. The metrics include time saved per capability, total assists consumed, assists per resolved incident, and daily unique users, so you can see which capabilities are adopted.

-   **[Map incident fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/security-management/pan-cortex-xsiam-mapping.md)**

Build Cortex XSIAM field mappings from a known incident. Select the Incident ID ingestion method and enter an ID in the XSIAM Incident ID field to retrieve its actual field values.

-   **[Automate incident updates and closures](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/security-management/pan-xsiam-automate-inc-updates.md)**

Map Security Incident fields to Cortex XSIAM on the new **SIR to XSIAM Mapping** panel using drag-and-drop, override, and transformation scripts. When the check box is selected, any new or updated data from SIR Incident will automatically sync with the corresponding fields in the XSIAM portal.


</td></tr><tr><td>

Self-service and omnichannel engagement for CSM

</td><td>

-   **[View work orders on the Consumer Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/workorders-consumerportal.md)**

View and track work orders directly in the Consumer Portal \(B2C\) using the new Work Orders page.

-   **[Use Voice call widget for portal communication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/portal-phone-widget.md)**

Customers can now make voice calls directly from portal pages or the Engagement Messenger. Call context stays intact as customers navigate between pages. These calls connect to AI Voice Agents to deliver conversational voice experiences without relying on contact center platforms.

-   **[Integrate ServiceNow Voice with Amazon Connect](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/integrate-ccc-amazonconnect.md)**

Use ServiceNow AI Voice Agents to build conversational voice experiences by routing calls from Amazon Connect, Five9, or NICE contact center channels to deliver natural, conversational customer interactions.


</td></tr><tr><td>

Service Catalog

</td><td>

-   **[Configurable subscription access enforcement for catalog items](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/r_ServiceCatalogProperties.md)**

Control whether service subscriptions can bypass "Available for" user criteria on catalog items using the `glide.sc.catalog_item.subscription_enforcement` property. This setting verifies that only users meeting specific criteria can access items, even with a parent service subscription.

The property controls this behavior with the following two modes:

    -   require\_criteria: Prevents access to users who don't meet the item's criteria, even if they are subscribed to the parent service offering.
    -   allow\_bypass: Preserves existing behavior that means users gain access through the "Available for" user criteria. "allow\_bypass" is a default value.
-   **[Migration from Core UI to Angular portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/migrate-core-ui-to-angular-catalog-exp.md)**

Migrate from the Core UI catalog experience to the Angular portal using the `com.glideapp.servicecatalog.ui16_portal` plugin, but only for upgraded instances.

Administrators on upgraded instances must install the`com.glideapp.servicecatalog.ui16_portal` plugin to move from the Core UI catalog experience to the Angular portal. On new instances, the plugin is active by default. Requesters view the Angular portal instead of Core UI while requesting a catalog item.


</td></tr><tr><td>

Service Exchange \(formerly Service Bridge\)

</td><td>

-   **[Knowledge article sync via FDS](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/service-exchange/knowledge-base-assignment.md)**

Assign knowledge articles from a source instance to a valid knowledge base on the target instance via Foundation Data Sync. The target instance creates a company knowledge base automatically when the source does not specify one.

-   **[Hide a synced knowledge article](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/service-exchange/hide-synced-knowledge-article.md)**

Hide a knowledge article that was synced to the target instance through Foundation Data Sync \(FDS\) so that it's no longer visible to other users. Knowledge articles synced from a source instance aren't owned by the target instance, so actions like Retire and Checkout don't apply to them.


</td></tr><tr><td>

Service Mapping

</td><td>

-   **[Service Mapping MCP tools](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/service-mapping-mcp-server.md)**

The Service Mapping tools, delivered as part of the CMDB MCP Server plugin, version 1.0.0, expose live application service data and enable AI clients such as Claude to query service topology, identify mapping gaps, and create new application services in natural language.

-   **[Service Mapping Lightweight Service Model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/sm-lightweight-service-model.md)**

Starting Service Mapping Plus version 1.24.4, you can improve service mapping performance by converting your Dynamic and Tag-Based services to Lightweight.


</td></tr><tr><td>

Service Operations Workspace for ITSM

</td><td>

-   **[Auto install SOW](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/getting-started-sow.md)**

A scheduled job is now available that executes a batch installation on a new instance to automatically install applications such as Service Operations Workspace for ITSM Advanced Applications only if the you have the necessary entitlements for the application. This is applicable only on newly provisioned zboot instance.


</td></tr><tr><td>

ServiceNow AI Platform core feature

</td><td>

-   **AI indicators now visible in Core UI lists**

Rows in Core UI lists that are created or modified by an AI agent now display an AI indicator. The indicator clears automatically when a user makes an inline edit to the row, keeping the indicator accurate as data changes.

-   **Caching for repeated metadata queries**

The platform caches repeated metadata queries to optimize processing of metadata requests.

-   **[Monitor daily slow-pattern trends](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/daily_slow_patterns.md)**

Track day-over-day trends in slow-pattern data with daily snapshots that automatically identify new or worsening patterns. High-significance changes are highlighted in list views, helping you quickly spot meaningful changes and prioritize investigation efforts. Built-in data retention and filtering keep historical comparisons accurate and relevant for up to 33 days.


</td></tr><tr><td>

ServiceNow Otto for IT Service Management \(ITSM\)

</td><td>

-   **[Create change request AI agent \(autonomous\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/itsm-change-create-change-ai-agent-auto.md)**

This AI agent creates structured change requests from conversational input by autonomously selecting the appropriate change model and template.

-   **[Change CI suggestion AI agent \(latest\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/itsm-change-ci-suggestion-ai-agent-auto.md)**

This AI agent autonomously identifies and populates both the primary configuration item \(CI\) and affected configuration items on a change request without requiring multiple user interactions.

-   **[Change request plans AI agent \(autonomous\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/itsm-change-request-plans-ai-agent-auto.md)**

This AI agent autonomously drafts change plan fields during the readiness phase. Field population is governed by a resolved change policy to ensure consistent behavior without requiring user input.

-   **[Change template suggestion AI agent \(autonomous\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/itsm-change-template-suggestion-ai-agent-auto.md)**

This AI agent identifies the most relevant change template and model for new change requests by analyzing request details and comparing them against available templates and historical data.


</td></tr><tr><td>

ServiceNow Otto for Virtual Agent

</td><td>

-   **[Display your assistant on Platform or ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/display-nap-assistant.md)**

For eligible new customers, premium chat is the default and the only available chat experience. If the assistant uses the Now LLM Service provider, the premium chat option isn't available.

-   **[Embed on third-party sites for enhanced chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/add-portable-va-client-website.md)**

Embed the chat widget for enhanced chat on third-party websites.

-   **[View all topics on the premium chat greeting screen](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/nava-integrated-chat.md)**

Select **View all topics** on the chat’s greeting screen to show all promoted topics in premium chat.


</td></tr><tr><td>

ServiceNow Quote Experience

</td><td>

-   **ServiceNow Quote Experience Experience integration with Contracts**

Amend simple and configurable products that originate from a contract, directly within a quote. Amend the products from a contract to complete upsell, downsell, and end-date changes, including early termination and extension. You can also renew the products from a contract using standard renewal, early renewal, or automatic renewal operations.

-   **ServiceNow Quote Experience Integration with Subscription Management**

Subscription Management integrates with ServiceNow Quote Experience, CPQ Configurator, and the Pricing Management to provide a unified experience throughout the Subscription Management lifecycle.

-   **ServiceNow Quote Experience integration with Pricing Management**

Calculate and adjust transaction pricing directly from a quote.

    -   Enable Pricing setup without manual field mappings. Set the pricing integration type to **productized**, and the application loads context-variable mappings from blueprint metadata and connects to the pricing service automatically when the blueprint is deployed.
    -   Reprice on demand or automatically. Recalculate transaction pricing with the Reprice action, or let it recalculate when a configuration is added to a quote. Administrators can turn off the default triggers for each event.
    -   Set automatic pricing behavior by stage. For example, enable automatic reprice in **Draft** stage, but disable for **Order Submitted** stage.
    -   Adjust prices manually. Apply a fixed-amount or percentage discount or uplift to a line or the header total. Each adjustment is preserved as a distinct input and tracked for audit.
    -   Apply automatic price adjustments. Use rules such as volume tiers, promotions, and contracted discounts during a pricing call. A manual adjustment always takes precedence over an automatic one on the same line or header.

</td></tr><tr><td>

ServiceNow Studio

</td><td>

-   **[ServiceNow Studio quick start](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/servicenow-studio-quick-start.md)**

Learn ServiceNow Studio efficiently with an updated course of quick start topics.

-   **[ServiceNow Studio user interface](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/servicenow-studio-user-interface.md)**

Personalize the new, agentic-first ServiceNow Studio user interface by choosing which components you want to use. Use the pro option with all features, vibe mode with minimal components, or custom, to choose your own.

-   **[Autonomous Engineer in Build Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ba-autonomous-engineer.md)**

ServiceNow Studio supports Build Agent spec mode, which generates a complete implementation plan from your requirements.


</td></tr><tr><td>

ServiceNow Vault

</td><td>

-   **[AI-generated security posture summary](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/vault-insights.md)**

Reduce the time you spend interpreting individual charts by reading an AI-generated summary of your data security, with a recommended next step for each area. Insights appears at the top of the Vault console home page and reports on data discovery, classification, and data protection.

-   **[Field encryption and auto-generate access policies agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/now-assist-vault-field-encryption-access-policies.md)**

Keep encrypted fields readable for the roles that need them by creating the module access policies as part of field encryption. Request encryption for a table field, review the roles that currently have access to it, and confirm the final list. The workflow creates a module access policy for each confirmed role and then encrypts the field, so you no longer review access control lists or Access Observer logs to build the role list yourself.

-   **[Zero Trust Access default policies](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/vault-default-policies-configs.md)**

Protect access to data from the start by automatically applying default step-up authentication policies when you install Zero Trust Access with ServiceNow Vault. Review these default policies at any time from Vault Console.

-   **[Code signing activity metrics in Vault Console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/vault-tools.md)**

Monitor code signing activity across your instance by tracking the create, update, and delete operations applied to code signing enabled records over the past week, and see which tables have the most such records.

-   **[Log Export Service export monitoring widget](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/vault-tools.md)**

Monitor your instance's log export activity by tracking total data exported over the past six months, the topics that export the most data, and the data exported by each topic so far in the current month.

-   **[ServiceNow Vault in Admin Home](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/install-vault-suite.md)**

Discover and install ServiceNow Vault from Admin Home. Instances with a ServiceNow Vault entitlement show a ServiceNow Vault tile, where an administrator can install Vault Suite and then open the Vault Console from the Configuration Console.

-   **Vault onboarding email notification**

Receive an email notification when ServiceNow Vault onboarding completes on your instance.


</td></tr><tr><td>

Smart Assessment Engine

</td><td>

-   **[Question bank](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/question-bank.md)**

With Smart Assessment version 23.0.2, you can create, manage, and reuse questions across multiple assessment templates with a centralized question bank. Questions move through a Draft, Ready to publish, Published, and Retired lifecycle. Add published questions to assessment templates as independent copies. Changes to the original or the copy don't affect each other.

-   **[Migrate a classic question bank or assessment template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/sae-asmnt-migrate-question-bank.md)**

With Smart Assessment Migration Tools version 23.0.3, you can migrate an existing classic question bank or the sections and questions of a Smart Assessment template into a new or existing question bank. Track migration status and review errors from the Question Bank Migrations list.

-   **[Delegation in Smart Assessment Engine](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/delegation-in-sae.md)**

With Smart Assessment version 23.0.2, you can delegate your assessments to another user for a set period using the platform delegation feature. A delegate of the primary responder can respond to and submit the assessment; a delegate of the requestor can cancel, reassign, and edit the due date. Delegation is off by default and is enabled from the template category.

-   **[Question change history](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/sae-question-change-history.md)**

With Smart Assessment version 23.0.2, you can review a log of every response, justification, and flag-state change made to a question throughout the lifecycle of an assessment, including who made each change and when. Consecutive changes to the same field by the same user within a configurable time window are merged into a single entry, while flag-state changes are logged individually.


</td></tr><tr><td>

Software Asset Management

</td><td>

-   **[Install the Software Asset Management application from the Product Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/sam-product-hub.md)**

Streamline onboarding by installing Software Asset Management and its dependent applications from the Product Hub. The Product Hub is the central location to view and manage all applications included in your Software Asset Management subscription. Access product documentation, videos, release notes, and community links from the same place.

-   **[Set up the Software Asset Management application using the Configuration Console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/config-console-sam.md)**

Reduce the time it takes to set up Software Asset Management after installing it from the Product Hub by using the Configuration Console, a one-stop shop for setup. Use predefined settings to smoothen the onboarding journey and configure software foundations, properties, AI skills, governance, team management, and data management from a single location. You can also use the AI conversational interface to configure groups, users, and Content Service setup.

-   **[Manage licenses for SAP S/4HANA Cloud, Private Edition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/sap-publisher-pack.md)**

Establish an accurate license position for your SAP S/4HANA Cloud, Private Edition delivered through RISE with SAP, without manually tracking user classifications or engine and database consumption. Collect usage data from your private cloud systems and calculate your Full Usage Equivalent \(FUE\) license position automatically with the Software Asset Management publisher pack for SAP. Reduce audit exposure and avoid unexpected compliance costs by measuring private cloud compliance alongside your existing on-premises SAP systems.

-   **[Manage all reclamation candidates from a consolidated Reclamation tab on the License usage view in the Software Asset Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/sam-workspace-workbench.md)**

Gain insights with a consolidated view of reclamation candidates across all publishers, SaaS integrations, installed software, and reconciliation flows. Drill down from the **Reclamation** tab into individual removal candidates for each publisher or integration, without switching between separate reclamation views. This enhancement gives your asset team a complete picture of reclamation opportunities across your software estate.

-   **[Improved license compliance reporting for Smartsheet SaaS integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/integrate-with-smartsheet.md)**

Improve visibility and compliance reporting of Smartsheet user licenses using the assigned seat type in the Smartsheet portal. The integration now retrieves users by seat type and creates subscription records for each category independently.

**Note:** The updated Smartsheet license reporting is supported starting from Software Asset Management - SaaS License Management \(sn\_sam\_saas\_int\) version 18.0.3.

-   **[Use expanded Microsoft Entra ID Single Sign-On \(SSO\) license reclamation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/saas-sso-integration.md)**

Expand your Microsoft Entra ID SSO integrations to improve identification of inactive users and surface group-assigned users as reclamation candidates. Update SSO subscription reclamation logic to improve stale subscription detection.

**Note:** The expanded Microsoft Entra ID capability is supported starting from Software Asset Management - SaaS License Management \(sn\_sam\_saas\_int\) version 18.0.3.

-   **[Automate suite license inference for improved compliance reporting](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-suites-inference.md)**

Enable automatic suite inference to calculate the optimal suite license for each software installation based on your actual footprint and entitlements. This feature reduces manual configuration required for the suite on the software model and improves compliance reporting.

-   **[Improve reporting of software installation inventory](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/deduplication-rule.md)**

Improve reporting of your software installation inventory by deploying rules that automatically consolidate duplicate product installations across your devices.

-   **[Onboard entitlements faster with additional predefined license metrics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/c_SAMLicenseMetrics.md)**

Reduce entitlement onboarding time by using additional predefined license metrics for supported publishers. These predefined license metrics help you track consumption, verify compliance, and reconcile deployments against entitlements. Review tier ranges and calculation factors on the new **License Metric Tier** tab of the Software entitlement page.

-   **[Analyze software spend transactions with AI in the Software Asset Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/spend-detection-ai-enhancements.md)**

Reduce manual software spend classification with AI-powered detection. The Software Asset Workspace now automatically identifies software purchases from imported transactions, extracts publisher and product details, and matches them to your Software Asset Management Content Library.


</td></tr><tr><td>

Strategic Planning

</td><td>

-   **[RIDAC for portfolio plans](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/portfolio-plan-ridac-spw.md)**

Access portfolio risks, issues, decisions, actions, and requested changes \(RIDAC\) directly from the portfolio plan using the dedicated RIDAC page within the portfolio plan. View all portfolio governance items in a single, integrated interface without navigating to the separate RIDAC menu. The RIDAC page reduces context-switching and improves portfolio visibility by consolidating governance data. The portfolio plan RIDAC displays the RIDAC items that match the portfolio plan's criteria or belong to the planning items of that portfolio plan.

-   **[Show or hide RIDAC page of a portfolio plan](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/show-or-hide-the-features-for-your-portfolio-plan-spw.md)**

As a portfolio manager, show or hide the RIDAC page of your portfolio plan. This capability helps you share only the portfolio plan data that matters to your stakeholders and restrict access to the other data.

-   **[Programs enhanced experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/program-portfolio-plan-spw.md)**

Access dedicated program planning views automatically created with zero setup. Navigate to the new Programs menu and click any program to open its dedicated plan with Prioritization, Roadmap, Kanban, and Financials views. New programs get plans instantly; existing programs receive them through an automatic one-time backfill \(500 at a time, newest first\). Role-based access ensures users with the sn\_align\_core.ap\_read\_only role can read, users with the sn\_align\_core.apw\_user role can manage items, and program managers are automatic plan owners.

-   **[Program-scoped data with fiscal calendar support](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/program-portfolio-plan-spw.md)**

View and manage program-scoped planning data in a focused, streamlined interface. Program plans display only that program's planning items. The Financials tab defaults to your fiscal calendar; if the fiscal calendar doesn't span the program dates, the system gracefully falls back to Gregorian with an explanatory message. Making the portfolio plan public and scenario planning for these program portfolio plans are hidden.

-   **[Automated email notification for scenario approval](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/approve-a-scenario-in-strategic-planning.md)**

Receive email notification when a scenario is approved. The system sends the notification to the scenario approver and portfolio owner. During the approval process, the portfolio plan becomes read-only to prevent unintended modifications and maintain data integrity.

-   **[Automatic status calculation for targets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/automatic-status-calculation-targets-spw.md)**

Automatically determine target status based on actual achievement percentages. When you enter actual values for a target period, the system compares the achievement percentage against predefined thresholds and automatically assigns a status \(Green, Yellow, or Red\). This eliminates manual status selection, reducing data entry errors and improving organizational governance.

Status is calculated and updated when you enter actual values using the formula: \(\(Actual Value - Start Value\) / \(Planned Target - Start Value\)\) x 100. Target owners can override automatically calculated status values at any time. If you update the actual value after a manual override, the system recalculates the status automatically.

-   **[Configure automatic status calculation thresholds](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/configure-automatic-status-calculation-spw.md)**

Enable administrators to customize automatic status calculation thresholds and enable or disable the feature based on organizational requirements. By default, automatic status calculation is enabled with system-defined thresholds of Green \(≥90%\), Yellow \(75-89%\), and Red \(&lt;75%\).

Administrators can adjust threshold percentages using the system property **sn\_gfa.target.auto\_status.thresholds**. To disable automatic status calculation and revert to manual status selection, set the system property to `false`.

-   **[Scrum Configuration in Enterprise Agile Planning](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/agile-configurations-in-eap.md)**

Set up teams that run Sprints without a Planning Interval above them by using the Scrum Configuration in Enterprise Agile Planning. It defines a single team level of the type Agile Team and allows the Epic and Story work item types. Story is the default work item type for that level and is mapped to the new **Scrum Sprint** planning calendar. The **Epic methodology** field is set to **Scrum**. Like the other default configurations, the Scrum Configuration is inactive until you activate it.

-   **[Unique iteration cadence for each team in Enterprise Agile Planning](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/simplified-iteration-creation-in-eap.md)**

Let each team set its own iteration dates by selecting **Allow unique cadence for each team** on an Enterprise Agile Planning configuration. If the configuration has planning calendars at more than one team level, each top-level team receives its own calendar. If the configuration has a single level of iterations, such as Sprints only, the iterations carry their own start and end dates instead of following a planning calendar entry. Teams that you add after you select this option receive a unique calendar, and teams that already exist continue to use the default calendar of the configuration.

-   **[Spillover and New scope fields on iterations in Enterprise Agile Planning](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/start-or-complete-iteration-in-eap.md)**

See how the scope of a Sprint moved during its run by using the **Spillover** and **New scope** fields on the Enterprise agile iteration \[sn\_apw\_advanced\_eap\_iteration\] record. Spillover is the sum of the story points of the committed stories that are no longer in the iteration when it completes. New scope is the sum of the story points of the stories that were added after the iteration started. Both fields are read-only and are calculated when you complete the iteration. Select a value to open the stories that it counts.

-   **[Copy and customize the demand summarization skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/clone-customize-demand-summarization-skill.md)**

Tailor demand summaries to your organization's process by copying the base demand summarization skill and customizing it with your own input fields, related entities, and prompt. When you activate a copy of the demand summarization skill, the previously active skill, either the base skill or an earlier copy, is automatically deactivated. Only one version of the skill can be active at a time.

-   **[Work with demands in Employee Slate](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/my-demands-widget.md)**

Create and track demands without leaving the conversation-first Employee Slate workspace. Describe the demand in a conversation to have matching catalog items identified and relevant fields prepopulated from your message, then track its status, activity, and progress using the new My Demands widget on your canvas or the standard Requests widget. Demands appear in Employee Slate only when both Project Workspace and Employee Slate Core apps are installed.


</td></tr><tr><td>

Stream Connect

</td><td>

-   **[Stream Producer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/stream-producer.md)**

Automatically stream changes from ServiceNow tables to Kafka topics with Stream Producer. Stream Producer uses change data capture \(CDC\) technology to capture inserts, updates, and deletes on selected tables. The captured changes are formatted as messages and sent to a Kafka topic, enabling real-time data synchronization with external applications.

-   **[Stream Producer schemas](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/schema-management.md)**

Stream Producer supports the Avro serialization format for message payloads. When using an Avro format, Stream Producer uses the selected table's auto-generated schema to convert CDC payloads to Avro before sending them to Kafka.

-   **[OAUTHBEARER authentication for Stream Connect message replication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/hla-data-input-kafka-credentials.md)**

Authenticate using OAUTHBEARER as part of the SASL credential framework for Stream Connect message replication. OAUTHBEARER authentication lets Stream Connect administrators meet customer requirements, improve security, and align with existing OAuth capabilities on the platform, enabling seamless integration with Kafka environments that require advanced authentication.

-   **[Stream Connect Dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/stream-connect-dashboard.md)**

Use the Stream Connect Dashboard to view data for Stream Producers, including the number of messages and bytes produced, the rate of production, and the number of messages still pending. Monitor and analyze Stream Producer performance with the Stream Producer CDC Statistics section on each Stream Producer's page. The Stream Connect Dashboard is available from the ServiceNow Store.


</td></tr><tr><td>

Supplier Lifecycle Operations

</td><td>

-   **[FedEx Dataworks Integration for Supplier Lifecycle Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/source-to-pay-operations/fedex-dataworks-overview.md)**

FedEx Dataworks combines unmatched, proprietary real-world data signals with advanced analytics to power ServiceNow's Source-to-Pay workflows. Relationship managers can use these signals during supplier onboarding to validate suppliers, evaluate risk, and benchmark supplier performance — without leaving the supplier workspace.

The FedEx Dataworks integration includes the following features:

    -   **Supplier validation in supplier onboarding Registration stage**: Verifies a supplier's details against FedEx Dataworks records to establish a FedEx Dataworks Supplier ID. This step is part of the supplier onboarding playbook and is required before risk assessment or performance benchmarking data can be retrieved.
    -   **FedEx Dataworks risk assessment in supplier onboarding Qualification stage**: Returns risk factor ratings for a matched supplier, covering customs risk, restricted country screening, and dangerous goods risk. Risk assessment is available in the supplier onboarding playbook after a successful supplier match.
    -   **Supplier performance benchmarking**: Retrieves FedEx Dataworks logistics performance metrics for a matched supplier, displayed in a dedicated section on the supplier profile page.
-   **[AI L1 SLO Service Desk Specialist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/source-to-pay-operations/ztsd-agent-slo.md)**

The AI L1 SLO Service Desk Specialist is a fully autonomous help desk automation solution that resolves supplier inquiries without manual intervention from a fulfiller.

For general inquiry cases, the AI L1 SLO Service Desk Specialist retrieves relevant information from published knowledge base articles and the FSC Common KG Tags added under the Enterprise knowledge graph to investigate the issue.

-   **[Generate a knowledge article from a closed supplier case](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/source-to-pay-operations/generate-article-case.md)**

Generate, review, and publish knowledge articles from closed supplier cases using ServiceNow Otto for SLO.

-   **[Generate a knowledge article from multiple closed cases](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/source-to-pay-operations/generate-article-multiple-cases.md)**

Generate, review, and publish a knowledge article from multiple closed supplier cases using ServiceNow Otto for SLO.

-   **[Verify tax information change request using Relish](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/source-to-pay-operations/validate-tax-information.md)**

Relish is a third-party supplier intelligence platform that validates supplier data while working on supplier cases.

When a tax information change request is assigned to a supplier manager and they start working on it, they can verify the tax details using Relish.

-   **[View supplier sanction status using Relish](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/source-to-pay-operations/view-supplier-sanction-status.md)**

Supplier managers can view the sanction status and last sanction check date for suppliers from the Manage Suppliers list.

These fields in the supplier list are available regardless of whether Relish is installed or not, but are updated only when Relish is integrated. If Relish is not integrated, users can edit the field manually if they want.


</td></tr><tr><td>

System Localization

</td><td>

-   **[Latin American Spanish](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/t_ActivateALanguage.md)**

Offer a more personalized experience to users in the Latin America region with a new language pack, I18N: Latin American Spanish Translations \(com.snc.i18n.latam\_spanish\).


</td></tr><tr><td>

Telecommunication Network Inventory

</td><td>

-   **[Viewing rack or cabinet equipment details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/telecom-network-inventory/viewing-rack-or-cabinet-equipment-details.md)**

View all network interfaces and physical connections for equipment in a rack or cabinet directly from the rack or cabinet record.

-   **[Create an inventory template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/telecom-network-inventory/create-inventory-templates.md)**

You can now create inventory templates that reference facility models. The full flow: facility model, inventory template, change request, and change task is now supported end to end.

-   **[Query range access for TNI tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/telecom-network-inventory/query-range-access-for-tni-tables.md)**

Added query range access control lists to 23 TNI tables. These include 14 NI Core tables, 2 CMDB CI class model tables, 6 TNI CMDB CI tables, and the Phone Territory table. Authenticated users with existing read roles automatically receive query range access. No new roles are required.


</td></tr><tr><td>

Telecommunications Customer 360

</td><td>

-   **[Party Relationship Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/telecom-media-technology/c360-prc-overview.md)**

View the network of entities connected to a consumer or account, including billing accounts, sold products, related parties, and active cases as an interactive node map from any Telecommunications Customer 360 record page.


</td></tr><tr><td>

Telecommunications Service Operations Management \(TSOM\)

</td><td>

-   **[Elastic event pull connectors for MPN](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/telecom-service-ops/configure-mpn-connectors-for-events-and-metrics.md)**

Collect metrics, including latency KPIs, from Nokia Med, Elastic, Prometheus, and Netcool KPI domains using a configurable Mobile Private Network \(MPN\) pull connector. Published metrics feed assurance monitoring and analytics.

-   **[MPN Latency Metrics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/telecom-service-ops/mpn-latency-dashboard.md)**

Monitor UE-to-switch latency and related KPIs across MPN-connected devices with combined and per-KPI trend views, an instance summary table, and a last-recorded-value panel.

-   **[Security log collection for MPN](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/telecom-service-ops/configure-security-log-collection-for-mpn.md)**

Collect MPN security logs with an out-of-box Health Log Analytics Elasticsearch data input. Raw logs are converted into structured log records for triage and analysis.

-   **[MPN health status collection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/telecom-service-ops/configure-mpn-rag-status-collection.md)**

Collect and aggregate red/amber/green health status from MPN Elastic index data at the tower and site level. Customize rules for calculating status based on your requirements.


</td></tr><tr><td>

Third-party Risk Management

</td><td>

-   **[Support for AI assets in element collection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/tprm-monitor-tp-elements.md)**

After upgrading to version 23.0.7, you can add, review, and manage third-party elements, including AI use cases and AI models, in the Elements grid. The grid is available directly on a third-party or engagement record in the Vendor Management Workspace, or embedded in a collection task in the Vendor Management Workspace or third-party portal. Elements linked to multiple engagements reuse existing assessment evidence across linked engagements without requiring a new assessment.

-   **[Internal tasks for due diligence and risk processes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/tprm-internal-tasks.md)**

After upgrading to version 23.0.7, and if you have the TPR assessor \[sn\_vdr\_risk\_asmt.vendor\_assessor\] role, you can create internal tasks to assign follow-up work to internal users for due diligence and risk processes. Internal tasks aren't visible to third-party contacts and don't appear in the third-party portal.

-   **[DORA register-of-information terminology definitions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/tprm-dora-roi-terminology-definitions.md)**

After upgrading the Digital Resilience Third-party Information Register application to version 23.0.3, and if you have the TPR assessor \[sn\_vdr\_risk\_asmt.vendor\_assessor\] role, you can document register-of-information terminology directly in the Vendor Management Workspace. Term definitions are included in the `B_99.01` CSV export when you generate a Register of Information report.

-   **[Document version comparison for third-party documents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/tprm-compare-document-versions.md)**

After upgrading to version 23.0.7, and if you have the TPR assessor \[sn\_vdr\_risk\_asmt.vendor\_assessor\] role, you can use the Document Management System to compare two versions of the same document type collected during third-party assessments. Only DOCX-to-DOCX and DOC-to-DOC formats are supported.


</td></tr><tr><td>

Threat Intelligence Security Center

</td><td>

-   **[Import data using AI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/security-management/import-data-using-ai.md)**

Import threat advisories as PDF or image files and let AI extract structured IOCs, threat actors, malware, and campaigns in seconds. Review extracted entities in a dedicated pane, grouped by type with AI extraction confidence score and reasoning, before they enter the library. Every AI-assisted import is captured in an audit record for full traceability.

-   **[Configure CrowdStrike NextGen SIEM sighting search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/security-management/tisc-crowdstrike-ngsiem-integration.md)**

Search CrowdStrike Falcon NextGen SIEM for observable sightings directly from the Threat Intelligence Library, case artifacts, or an automated workflow, with results captured as sighting records on the observable.

-   **[Configure Premium Threat Feed for CrowdStrike](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/security-management/premium-threat-feed-for-crowdstrike.md)**

Ingest and correlate threat intelligence with integrated vulnerability intelligence feed from CrowdStrike.

-   **[Add security incident to TISC case](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/security-management/add-incident-to-case.md)**

Link entities to security incidents directly from either the SIR workspace or the entity record without creating a TISC case first.

-   **[Create a related record to link](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/security-management/tisc-create-new-related-record.md)**

Add related intelligence without leaving your investigation. Create and link new records from within your workflow.

-   **[Observable extraction from indicator patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/security-management/tisc-extract-observables-from-indicators.md)**

Observables are extracted from STIX indicator pattern values during ingestion, added to the library, and related to the parent indicator automatically.


</td></tr><tr><td>

Unified Security Exposure Management \(USEM\)

</td><td>

-   **[SSVC decision values roll up from CVEs to third-party entries](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/security-management/nvd-ssvc-enrichment.md)**

USEM rolls up the Exploitation, Automatable, and Technical Impact SSVC \(Stakeholder-Specific Vulnerability Categorization\) values from CVE entries to the corresponding third-party entry \(TPE\) records. Changes to these values automatically trigger a risk score recalculation when the TPE risk calculator uses one or more of them.

-   **[Automatic re-evaluation of remediation tasks on Preferred solution change](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/security-management/sem-grouping-multiple-findings-remediation-tasks-processing.md)**

Remediation tasks can now automatically re-evaluate findings when their Preferred solution changes, so items are regrouped into the appropriate remediation task without manual intervention. This helps keep remediation tasks accurate and reduces manual cleanup.

-   **[Deploy multiple patches to multiple collections with Microsoft SCCM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/security-management/mspatch-integration.md)**

Deploy more than one patch to more than one collection in a single deployment, instead of one patch to one collection at a time. When you select more than one patch for a deployment, the integration automatically creates a Software Update Group in Microsoft SCCM to bundle the patches.

-   **[Deploy multiple patches to multiple computer groups with HCL BigFix](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/security-management/vr-bigfix-integration.md)**

Deploy more than one patch to more than one computer group in a single deployment, instead of one patch to one computer group at a time.

-   **[Resolve AI exposure tasks in workflow with Employee Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/security-management/ai-security-exposure-employee-workflow.md)**

AI Security Exposure Management integrates with Employee Center and third-party security tools to enable AI asset owners to remediate AI posture findings \(configuration issues\) directly through lightweight tasks.

-   **AI Service Graph Connector for Prisma AIRS**

This integration imports AI inventory data from Palo Alto Prisma AIRS and populates the CMDB in your ServiceNow AI Platform instance. In addition to inventory data, this integration imports key metrics related to AI model vulnerabilities, validation findings \(automated red teaming results\) that can be viewed in AI control tower.

-   **[Palo Alto Prisma AIRS Integration for AI Security Exposure Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/security-management/prisma-airs-integration.md)**

Import AI security exposures such as model vulnerabilities, model validation findings \(automated red teaming alerts\), and posture findings \(configuration/policy violations\) into AI Security Exposure Management and automate workflows for remediation.

-   **[Configure the Wiz Test Results Integration to import AI findings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/security-management/wiz-test-result-tab-filters.md)**

Import cloud configuration findings as Test Results into Configuration Compliance. Configuration issues related to AI assets, such as AI models and agents and AI security scans are routed into AI security exposure management tables \(AI posture findings\) if you have AI security exposure management activated.

-   **Attach findings to a penetration testing assessment request**

Admins can now link pentest findings to existing pentest requests during manual upload, enabling consolidation of findings from multiple vendors under a single request.

-   **[Remove older SBOM records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/security-management/sbom-cleanup.md)**

SBOM cleanup lets you create a one-time rule to purge older software bill of materials records that match specified conditions that you create. Cleanup runs are permanent and can't be reversed, and you must review the conditions you set carefully before running one.


</td></tr><tr><td>

Vulnerability Response

</td><td>

-   **[Automatic re-evaluation of remediation tasks on preferred solution change](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/security-management/vulnerability-groups.md)**

Remediation tasks can now automatically re-evaluate vulnerable items when their Preferred solution changes, so items are regrouped into the appropriate remediation task without manual intervention. This helps keep remediation tasks accurate and reduces manual cleanup.


</td></tr><tr><td>

Zero Copy Connectors

</td><td>

-   **[REST connectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/rest-connectors.md)**

Retrieve real-time metadata and data from REST-enabled systems without copying or duplicating the data. This release adds REST connectors for Oracle HCM \(Discovery\) and Acumatica, built on a generic metadata connector framework that supports filter, limit, and groupBy pushdown operations.

-   **Personal authentication for Databricks and Snowflake**

Authenticate to [Databricks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/databricks-zcc.md) and [Snowflake](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/snowflake-zcc.md) using your own credentials instead of a shared service account, so that access is individually authenticated at the source system.


</td></tr><tr><td>

Zing text indexing and search engine

</td><td>

-   **[Column-level query\_range read ACLs on table columns indexed for search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/verify-user-roles-access-searchable-tables.md)**

Improve security for search with Zing's support for column-level query\_range read ACLs on table columns that are indexed for search. When searching tables with legacy v3 format text indexes, Zing only displays search results if the current user's role has access to all of the table's indexed columns. For tables with v4 format text indexes, Zing only displays search matches in indexed columns accessible by the user's role. Use the new Text Search Query Range ACL Checker tool to verify that user roles have access to all indexed columns for your searchable tables.


</td></tr></tbody>
</table>**Parent Topic:**[Release notes summaries for Brazil features](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/release-notes-summaries.md)


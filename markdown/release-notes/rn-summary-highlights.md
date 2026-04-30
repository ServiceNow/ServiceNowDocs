---
title: Highlights for all Yokohama features and products
description: Cumulative release notes summary on highlights of Yokohama features and products.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2026-04-08"
reading_time_minutes: 122
breadcrumb: [Release notes summaries for Yokohama features, Release notes for upgrading from Xanadu, Learn about the Yokohama release, Yokohama release notes]
---

# Highlights for all Yokohama features and products

Cumulative release notes summary on highlights of Yokohama features and products.

Review the product highlights to learn what's new in Yokohama.

<table id="rn-summary-changes-table" class="custom-rows"><thead><tr><th class="filter">

Application or feature

</th><th>

Details

</th></tr></thead><tbody><tr><td>

AI Control Tower

</td><td>

[Yokohama Patch 11](../quality/yokohama-patch-11.md)

-   Review changes to Now Assist usage measurement.
-   Some Now Assist skills, agents, and agentic workflows are on by default.
-   Additional role configuration is required for agentic workflows and AI agents included with Now Assist applications.
-   AI connections are introduced in AI Control Tower using Service Graph Connectors. AI connections are combination of hyperscalars, AI apps, and agentic AI frameworks. The AI Service Graph Connectors available from March 2026:
    -   [AWS](https://www.servicenow.com/docs/access?context=aws_0&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)
    -   [Microsoft](https://www.servicenow.com/docs/access?context=microsoft&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)- Azure Foundry and Copilot
    -   [n8n](https://www.servicenow.com/docs/access?context=n8n&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)
    -   [GCP Vertex AI](https://www.servicenow.com/docs/access?context=gcp-vertex-ai&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)
    -   [LangGraph](https://www.servicenow.com/docs/access?context=langgraph&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)
    -   [Salesforce](https://www.servicenow.com/docs/access?context=salesforce&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)

[Yokohama Patch 6](../quality/yokohama-patch-6.md)

-   Monitor the performance of guardrails enabled through Now Assist Guardian using the Health tab.
-   Measure and improve the quality of interactions with virtual agents using the Evaluation tab.

[Yokohama Patch 3](../quality/yokohama-patch-3.md)

-   AI Control Tower helps customers manage and oversee performance, risk profile &amp; workforce transformation while also helping to seamlessly embed AI into enterprise strategy.

-   -   Create an AI steward role.
-   Use the AI Asset inventory to catalog AI-related artifacts.
-   Use the AI skills Approvals to review and approval flows.
-   Create a AI Control Tower Workspace.

</td></tr><tr><td>

AI Risk and Compliance

</td><td>

-   Manage AI systems, models, and datasets across their entire life-cycle with consistent governance for better visibility, control, and compliance.
-   Perform impact assessments for AI systems, models, and datasets to identify high-risk AI assets.
-   Perform risk assessments on individual risks associated with an AI asset based on additional information and testing.
-   Manage and oversee AI-related cases and incidents through a structured case management process.
-   Build a compliance-ready AI asset inventory aligned with regulatory requirements using the AI framework content pack.

See [AI Risk and Compliance](https://www.servicenow.com/docs/access?context=ai-risk-and-compliance&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US) for more information.

</td></tr><tr><td>

AI Search

</td><td>

[Yokohama Patch 11](../quality/yokohama-patch-11.md)

-   Improve search precision and contextual relevance with hybrid search, available for customers with Now Assist in AI Search installed.
-   Gain insights into search behavior with a refreshed and updated Search Preview UI.

[Yokohama Patch 6](../quality/yokohama-patch-6.md)

-   Search more intuitively with an updated, consumer-grade user experience in search portals, global search, and workspace search.

[Yokohama Early Availability](../quality/yokohama-security-notables.md)

-   Restrict index size and increase search performance with guardrails that limit the number of Task and Alert table records indexed for search
-   Customize the semantic vector search experience by configuring semantic indexing settings for your indexed sources
-   Improve the focus of search results by excluding search sources in a search profile from being used to generate search results or Genius Result answers
-   Expand search recall by indexing content from knowledge blocks
-   Highlight important search results by boosting relevancy for results that match synonyms in a synonym dictionary

See [AI Search](https://www.servicenow.com/docs/access?context=overview-ais&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US) for more information.

</td></tr><tr><td>

AIOps LEAP

</td><td>

-   Automation feedback and tracking for automation opportunities
-   Pin Automation Opportunities for ease of analysis
-   Customize filters for Automation Opportunities and published playbooks.
-   Customize columns on the Automation Opportunities and published playbooks pages.
-   Use published LEAP in SOW to resolve a new incident quickly.
-   Use a value dashboard for performance analysis and enhancement.

See [AIOps Learning Enhanced Automation Playbook \(LEAP\)](https://www.servicenow.com/docs/access?context=aiops-leap&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

API

</td><td>

-   Use server-side JavaScript APIs in scripts to change the application functionality.
-   Run client APIs whenever a client-based event occurs, such as when a form loads, a form is submitted, or a field value changes.
-   Use inbound REST APIs to interact with various ServiceNow functionalities within your application.

See [API implementation and reference](https://www.servicenow.com/docs/access?context=api-implementation-reference&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US) for more information.

</td></tr><tr><td>

Access Management

</td><td>

-   Security Data Filters are a powerful new feature designed to restrict access to sensitive records based on roles or security attributes. This ensures only authorized users can view data, regardless of how the data is accessed.
-   Related Record Access allows enforcement of consistent access rules across related tables, ensuring that users only see records associated with the data they are authorized to access.

See [Access Control List Rules](https://www.servicenow.com/docs/access?context=access-control-rules&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US) for more information.

</td></tr><tr><td>

Accounts Payable Operations

</td><td>

-   Leverage Accounts payable document classification skill to classify email attachments into invoice, credit memo, or supporting documents based on the AI recommended confidence score resulting in error free invoice data extraction.
-   Validate supplier provided tax against a system-calculated tax by integrating an enterprise-grade tax engine resulting in straight-through processing of invoice while improving accuracy, compliance, and operational efficiency
-   Introduced Agentic workflow in Accounts Payable Operations to resolve invoice inquiry cases raised by employees and suppliers thereby significantly reducing the involvement of human agents.
-   The ServiceNow® Now Assist offers generative AI purchase order line-mapping to improve accuracy and reduce manual work.
-   Experience the new generative AI skill for invoice data extraction, designed to enhance accuracy and reduce manual effort.
-   Leverage AI-powered GPT-4o-driven invoice data extraction with Document Intelligence for improved accuracy and reduced manual effort.
-   Get instant, real-time assistance from generative AI to summarize invoice case details through the Now Assist panel.
-   Use the Accounts Payable Operations properties page to control the configuration of APO properties.

</td></tr><tr><td>

Adoption Services

</td><td>

-   Execute Guided Setup in every domain, with guided setup player roles.
-   Experience the Guided Tours in dark and light themes.
-   Execute Guided Tours from any scoped application route.
-   Explore the What's New feature that's available in Help Center for all experiences.
-   Use the new Help Center UI features that provide a more enhanced experience.
-   Explore the enhanced Guided Setup that support running it multiple times.

See [Adoption services](https://www.servicenow.com/docs/access?context=adoption-services&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US) for more information.

</td></tr><tr><td>

Advanced AI Search Management Tools

</td><td>

[Yokohama Patch 11](../quality/yokohama-patch-11.md)

-   Review performance metrics and trends more easily with an updated and refreshed dashboard UI.
-   Analyze performance metrics and trends for search applications used in Recommended Actions.

[Yokohama Patch 6](../quality/yokohama-patch-6.md)

-   Analyze search trends from the preceding six months using the AI Search Analytics dashboard's **Date range** interactive filter.
-   Understand your mobile search traffic with support for the Mobile Platform search application in the AI Search Analytics dashboard's **Search application** interactive filter.

See [Platform Analytics Solution for Advanced AI Search Management Tools](https://www.servicenow.com/docs/access?context=adv-ais-mgmt-tools-content-pack&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US) for more information.

</td></tr><tr><td>

Advanced Risk

</td><td>

-   **[Some Now Assist skills, agents, and agentic workflows are turned on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

The skills are automatically available to appropriate role users for the application, such as ITIL roles on incident forms or change forms. This change simply activates the skill and does not touch the roles that may be needed to use the skill. The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills and agentic workflows are turned on automatically.
    -   Existing customers who are upgrading \(starting with Yokohama Patch 11\): Any previously unconfigured skill, agent, or agentic workflow is turned on automatically \(the AI asset was never configured and turned on, then turned off again\). Previously configured skills and agentic workflows that were turned on, then off, remain inactive.

-   Use generative AI to generate risk assessment summaries and highlight key insights for better context.
-   Reassess completed risk assessment projects to evaluate risks based on new insights or changing conditions.
-   Copy risk responses from a previous risk assessment during reassessment of a risk assessment project.
-   Reassign assessors for multiple risk assessment projects to optimize resource allocation.
-   Remove risks from a risk assessment project during the assessment to streamline focus on relevant risks.
-   Enable and manage the risk response task workflow from the Risk Assessment Methodology \(RAM\) form.

See [Advanced Risk Assessment](https://www.servicenow.com/docs/access?context=advanced-risk-assessment&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US) for more information.

</td></tr><tr><td>

Advanced Work Assignment

</td><td>

-   Run assignments on different nodes or cadences for different service channels to improve the AWA application's performance and resilience.
-   Provide wrap-up codes or notes for interactions or segments that the agent is involved in at the end of a call.

See [Advanced Work Assignment](https://www.servicenow.com/docs/access?context=awa-application-landing-page&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US) for more information.

</td></tr><tr><td>

Agent Client Collector

</td><td>

-   Agent Client Collector for Visibility: Starting in version 1.1.0, ACC for Visibility has been renamed Agent Client Collector for Visibility - Content. CNO for Visibility has been extracted from Agent Client Collector for Visibility - Content and is now a separate application.
-   Store instance credentials in the Google Cloud Secret Manager when the Kubernetes Visibility Agent Informer uses Google Kubernetes Engine \(GKE\).
-   Use a custom CA to enable Kubernetes Visibility Agent Informer to communicate with the instance when using a custom root Certificate Authority \(CA\).
-   Configure Agent Client Collector without a MID Server by ßusing MID-less configuration.

See [Agent Client Collector](https://www.servicenow.com/docs/access?context=acc-landing-page&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Agent Workspace for HR Case Management

</td><td>

-   The HR Triaging Dashboard enables you to review your teams' case assignments through cases displayed as cards. Once you set up a layout for HR services, priorities, or assignment groups, moving of case cards between lanes, auto-updates the HR service, user assignment, or priority of cases.
-   Provide a convenient and efficient way for deskless workers to seek in-person or remote assistance, report issues, and receive guidance from HR agents through designated walk-up centers.

See [Agent Workspace for HR Case Management \(Configurable\)](https://www.servicenow.com/docs/access?context=agent-ws-hr-case-mgmt-landing-page&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Agent experience for CSM

</td><td>

-   Alert agents about the status of current chats by using color-coded session tabs to indicate service level agreement \(SLA\) threshold timers, chat duration, and unread message counts.
-   Create form templates or modify existing templates with enhancements to the form template feature.
-   Integrate enhanced knowledge guidance on the Front-line case page and enable agents to attach and add links to knowledge articles in comments, work notes, or emails by using modeless dialogs.
-   Display native voice configurations in CSM Configurable Workspace with the Voice interaction record page that agents can use to handle phone calls.
-   Dedicate time after each call or chat for agents to finalize interaction details.

See [CSM Configurable Workspace](https://www.servicenow.com/docs/access?context=csm-workspaces-configure&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

App Engine Studio

</td><td>

Use the App Readiness and Compliance report in App Engine Management Center \(AEMC\) to check if apps are ready to go live.

See [App Readiness and Compliance Report](https://www.servicenow.com/docs/access?context=app-readiness-report&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US) for more information.

</td></tr><tr><td>

Application Manager

</td><td>

Yokohama patch 11

-   Reduce potential runtime errors by installing and updating Now Assist applications with suites of interdependent versions.
-   View all ServiceNow Store applications that are licensed or available for procurement from the **Available for you** tab.
-   Gain insights about application installation requirements and blockers with application state indicators.

See [Application Manager](https://www.servicenow.com/docs/access?context=application-manager&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US) for more information.

</td></tr><tr><td>

Application Vulnerability Response

</td><td>

-   Monitor your penetration test requests and findings, as well as your team's overall progress in the Penetration Test Workspace.
-   Reevaluate the risk score, assignments, remediation target date, exceptions, and remediation task for a specific set of application vulnerable items in the Vulnerability Manager Workspace.
-   Integrate with supported third-party scanners to import vulnerability data.
-   Compare application vulnerability-related data and determine if application vulnerabilities are found in an application.
-   Prioritize, remediate, and manage application vulnerable items \(AVIT\)s. Each application vulnerability represents a vulnerability entry in the Common Weakness Enumeration \(CWE\) or third-party libraries.
-   With the sn\_vul.app\_sec\_manager role, create application remediation tasks manually in the Vulnerability Manager Workspace.
-   With the sn\_vul.app\_security\_champion role, create application remediation tasks manually in the IT Remediation Workspace.

See [Application Vulnerability Response](https://www.servicenow.com/docs/access?context=avr-landing&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Audit Management

</td><td>

-   Analyze relationships between different variables, such as assessing risks and controls, by using the Matrix report in Audit Workspace.
-   Manage your documents and work papers in Audit Management as cloud files.
-   Upload documents from your local computer as cloud files and link them to any record in your ServiceNow instance.
-   Share a single cloud file with multiple records by linking it to any GRC record.
-   Benefit from accessibility improvements to create a configurable workspace that supports Web Content Accessibility Guidelines \(WCAG\) 2.1 Level AA conformance.

See [Audit Management](https://www.servicenow.com/docs/access?context=c_GRCAudits&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US) for more information.

</td></tr><tr><td>

Authentication

</td><td>

[Yokohama Patch 11](../quality/yokohama-patch-11.md)

-   **[Authentication factors for AI voice service](https://www.servicenow.com/docs/access?context=authentication-factors&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US)**

Enable caller access to AI voice agents by configuring the required identification and authentication factors.

-   **[OAuth enhancements](https://www.servicenow.com/docs/access?context=api-inbound-and-outbound&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US)**

Following are the OAuth enhancements:

    -   Use **Opaque** or **JWT token** option for your inbound integration endpoints.
    -   Use the **Allow access only to APIs in selected scope** option to enable access to the APIs that are explicitly listed in the selected scopes for your inbound integrations.
    -   Use the OAuth Entity Resource tab for outbound integrations to configure resource parameters so they flow into the OAuth token request and are reflected in the token from your OAuth provider.
-   **Provider name for Inbound integrations**

Use the Provider name field to enter the details of your inbound integrations to distinguish between different inbound integrations on your ServiceNow AI Platform®. Update the Provider name in your API integrations to improve monitoring capabilities:

    -   For OAuth integrations, update the provider name using the Provider name field. To know more, see [OAuth Inbound](https://www.servicenow.com/docs/access?context=oauth-inbound&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).
    -   For Basic authentication integrations, update the Provider name in the integration registration form.

[Yokohama Patch 7](../quality/yokohama-patch-7.md)

-   **OAuth token enhancement**

Use Opaque or JWT token option for your inbound integration endpoints.


Yokohama

-   Use Continuous Authentication to require step-up authentication or re-authentication to the users before allowing access to sensitive or high-privilege information.
-   Multi-factor Authentication \(MFA\) is enforced by default for all non-SSO login to ServiceNow®.
-   Use the Authorization code, resource owner password credential, SAML bearer, and JWT bearer OAuth grant types of OAuth for outbound integration requests through the MID Server.

See [Authentication](https://www.servicenow.com/docs/access?context=c_Authentication&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US) for more information.

</td></tr><tr><td>

Automated Test Framework

</td><td>

-   Reduce upgrade and development time by replacing manual testing with automated testing.
-   Design tests once and reuse them in different contexts and with different test data sets.
-   Keep test instances clean by rolling back test data and changes made after each test run.
-   Create and schedule test suites to organize and run tests in batches.
-   Reduce test design time by copying quick start tests and test suites. You can also create custom test steps to expand test coverage.

See [Automated Test Framework \(ATF\)](https://www.servicenow.com/docs/access?context=atf-landing-page&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US) for more information.

</td></tr><tr><td>

Benchmarks

</td><td>

1.  Experience the new Key Performance Indicator \(KPI\) for Now Assist under Productivity moments per user of ITSM Benchmarks to understand the benefits of Now Assist features like Knowledge Article generation.
2.  Benchmark the all new HRSM indicator to help evaluate the performance in comparison to your peers.

See [Benchmarks](https://www.servicenow.com/docs/access?context=r_Benchmarks&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Business Continuity Management

</td><td>

-   Use the latest assessment template to perform a Business Impact Analysis.
-   Create nested plans in an event so that you can activate cross-references to multiple plans.
-   Use the hierarchical view in the plans to organize nested event tasks according to their dependencies.
-   Use the Crisis map functionality that includes the latest UIB components.

See [Business Continuity Management](https://www.servicenow.com/docs/access?context=business-continuity-mangmt-overview&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US) for more information.

</td></tr><tr><td>

Care Team Operations for Biomed

</td><td>

-   Automate healthcare operations by enabling biomed support request creation and fulfillment.
-   Create biomed support requests from directly within the Care Team Portal.
-   Gain full visibility into reported biomed cases while enabling biomed teams to manage and fulfill them as work orders or work orders tasks when Clinical Device Management is installed.

See [Care Team Operations for Biomed](https://www.servicenow.com/docs/access?context=care-team-operations-for-biomed&version=yokohama&pubname=yokohama-healthcare-life-sciences&ft:locale=en-US) for more information.

</td></tr><tr><td>

Care Team Operations for Healthcare IT

</td><td>

-   Automate healthcare operations by enabling IT support request creation and fulfillment.
-   Create IT support requests from directly within the Care Team Portal.
-   Gain full visibility into reported IT cases while enabling IT teams to manage and fulfill them as incidents efficiently.

See [Care Team Operations for Healthcare IT](https://www.servicenow.com/docs/access?context=hcls-cto-it-app&version=yokohama&pubname=yokohama-healthcare-life-sciences&ft:locale=en-US) for more information.

</td></tr><tr><td>

Case and Knowledge Management

</td><td>

Use HR Benchmarks to provide instant visibility into your key performance indicators \(KPIs\) and trends, as well as comparative insight relative to the industry averages of your peers and to the industry top performers.

See [Case and Knowledge Management](https://www.servicenow.com/docs/access?context=case-knowledge-management-landing-page&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Case management for CSM

</td><td>

-   Create cases for invoice-related services such as invoice disputes or requested corrections with the Case management for Invoice Operations application.
-   Use process mining to mine the configured base system project to investigate the causes of long resolution times.

See [Case management for Customer Service Management](https://www.servicenow.com/docs/access?context=csm-case-management&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Change Management

</td><td>

-   Increase operational efficiency of tier 1 service desk agents with the dedicated sn\_service\_desk\_agent role.
-   Require specified field details to be updated before transitioning the state of a change request by converting existing optional fields to mandatory fields.
-   Restrict unauthorized access to Change Management tables using deny ACLs.

See [Change Management](https://www.servicenow.com/docs/access?context=c_ITILChangeManagement&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Cloud Account Management

</td><td>

-   Create and manage cloud accounts efficiently either by manual or automated processes.
-   Manage and track cloud account requests using the requester dashboard.
-   Visualize data tailored for the admin persona with deeper insights into cloud accounts.
-   Scan accounts for configuration violations and take appropriate actions for weak passwords, pending certifications, undefined account ownership, discovery schedules, and so on.
-   Provision both Terraform Cloud/Terraform Enterprise and cloud native interface accounts.

See [Cloud Account Management](https://www.servicenow.com/docs/access?context=cam-landing&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Code Signing

</td><td>

Use Code Signing Guardrails to improve checks during the signing process to create more secure workflows.

See [Code Signing](https://www.servicenow.com/docs/access?context=code-signing-landing&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US) for more information.

</td></tr><tr><td>

Collaborative Work Management

</td><td>

-   Improve focus on your working area through a simplified, distraction-free navigation experience.
-   Quickly identify task assignees without access to your Space and manage sharing permissions accordingly.
-   Improve collaboration efficiency by sharing the exact view of your Board or specific page of your Doc when sharing a URL with others.
-   Collaborate in real-time on Docs with multiple editors.
-   Benefit from accessibility improvements to create a configurable workspace that supports Web Content Accessibility Guidelines \(WCAG\) 2.1 Level AA conformance.

See [Collaborative Work Management](https://www.servicenow.com/docs/access?context=cwm-landing&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Common Core

</td><td>

-   Generate a GRC issue action plan by using the agentic AI workflow.
-   Segregate data by entities and granular access management when using entity-based access.
-   Summarize an issue by using generative AI to provide quicker context gathering and contextual awareness. With this feature, you can improve the efficiency and productivity of your analysts on GRC issues.
-   Use the enhanced GRC licensing summary dashboard to understand the licensing treatment for users that are added to the group by roles that are mapped or assigned to the group.
-   Select a user record on the licensing summary dashboard and select the role hierarchy to see all the parent roles that are assigned to the user and their role hierarchies.
-   Monitor the email activity from the Overview page for regulatory agencies.
-   Update and add content by using Microsoft 365 for ServiceNow Reporting, which is now integrated with the Document designer application.
-   Add up to 20 columns in a table and in a content block by using the Document designer application.
-   Select and reorder columns by using the Document designer Microsoft Word add-in while creating templates.

[Yokohama Patch 11](../quality/yokohama-patch-11.md)

-   Some Now Assist skills are now turned on by default.
-   Review changes to Now Assist usage measurements.

For detailed documentation, see [Common Governance, Risk, and Compliance features](https://www.servicenow.com/docs/access?context=common-grc-features&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US).

</td></tr><tr><td>

Compliance Case Management

</td><td>

-   Empower compliance professionals to perform assessments on compliance cases using the Smart Assessment Engine.
-   Utilize the unified **Tasks** page on Employee Center to complete your assessments.
-   Benefit from accessibility improvements to create a configurable workspace that supports Web Content Accessibility Guidelines \(WCAG\) 2.1 Level AA conformance.

See [Compliance Case Management](https://www.servicenow.com/docs/access?context=compliance-case-management&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US) for more information.

</td></tr><tr><td>

Configuration Compliance

</td><td>

-   With the sn\_vulc.admin role, create remediation tasks manually in the Vulnerability Manager Workspace.
-   With the sn\_vulc.remediation\_owner role, create remediation tasks manually in the IT Remediation Workspace.

See [Configuration Compliance](https://www.servicenow.com/docs/access?context=vr-config-compliance-landing&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

-   Access changes to the CMDB Editor and CMDB Admin user roles:
    -   Starting with Yokohama Patch 4, the sn\_cmdb\_editor and sn\_cmdb\_admin user roles no longer have create, update, or delete access to records in the Configuration Item \[cmdb\_ci\] class.
    -   Starting with Yokohama Patch 6, you can configure the sn\_cmdb\_admin and the sn\_cmdb\_editor user roles with the necessary permissions to perform some CMDB Workspace tasks by manually running a scheduled job.
-   Manually create a configuration item \(CI\) in CMDB Workspace that is verified by the Identification and Reconciliation Engine \(IRE\) and is unique within CMDB. Creating a CI using the IRE identification rules helps to maintain the integrity of CMDB.
-   Use the Now Assist for CMDB CI summarization skill to see a comprehensive summary for a CI, with details such as discovery and related incidents, directly on the configuration item \(CI\) form. Use the manage duplicate CIs skill for step-by-step guidance on how to use de-duplication templates to de-duplicate CIs.
-   The Configuration item summarizer AI agent accepts the sys\_id of a CI and returns a full summary of Configuration Management Database \(CMDB\) data for the CI. The agent isn’t typically used as a standalone agent and any use case can access it.
-   View the various counts, such as the number of CIs and the number of CI types, for the CIs that are connected to the home node in Unified Map.
-   Apply filters that were previously available only to the coverage charts in the CMDB 360 dashboard in CMDB Workspace to all charts in the Discovery sources tile.
-   Use a condition builder or a custom script to restrict the list of de-duplication tasks that are assigned to a de-duplication template when de-duplicating CIs.

See [Configuration Management](https://www.servicenow.com/docs/access?context=manage-cmdb&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US) for more information.

</td></tr><tr><td>

Container Vulnerability Response

</td><td>

-   With the sn\_vul\_container.vulnerability\_analyst or sn\_vul\_container.vulnerability\_admin role, create container remediation tasks manually in the Vulnerability Manager Workspace.
-   With the role sn\_vul\_container.remediation\_owner, create container remediation tasks manually in the IT Remediation Workspace.

See [Container Vulnerability Response](https://www.servicenow.com/docs/access?context=cvr-landing&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Continuous Authorization and Monitoring

</td><td>

-   Import catalog and System Security Plan \(SSP\) models with the new CAM Open Security Controls Assessment Language \(OSCAL\) import landing page.
-   Export and import SSP models and catalog models in the OSCAL format.
-   Export control objectives as a catalog in the OSCAL format.
-   Generate additional reports in Microsoft Word format, such as a Security Assessment Plan \(SAP\), Authorization to Operate \(ATO\) Letter, and Executive Summary.
-   Generate reports based on a Microsoft Word template.

See [Continuous Authorization and Monitoring](https://www.servicenow.com/docs/access?context=grc-cam-landing-page&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US) for more information.

</td></tr><tr><td>

Contract Management Pro

</td><td>

-   Link parent contracts during drafting and negotiation phases to inherit parent contract terms.
-   Pause and resume an in-progress signature process when updates to the signatory list are required.
-   Perform wet signature in the electronic signature workflow. The enhanced electronic signature workflow capability provides flexibility to complete the signature process when the signatories want to do a wet signature instead of an electronic signature.
-   Upload the contract document directly from the Microsoft Word add-in for ServiceNow Contracts instead of selecting it from your system.
-   Use Logout icon \(![Logout icon](../image/cmpro-addin-logout.png)\) to log out from Microsoft Word add-in for ServiceNow Contracts.
-   Change the application scope to edit a contract template in the Microsoft Word add-in for ServiceNow Contracts. This option is only visible to the administrators.

See [Contract Management Pro](https://www.servicenow.com/docs/access?context=cncore-cmpro-landing-page&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Contract Management Pro for Legal Service Delivery

</td><td>

-   Initiate and manage amendment requests for existing contracts.
-   Record producer to initiate an amendment request from the Employee Center.

See [Contract Management Pro for Legal Service Delivery](https://www.servicenow.com/docs/access?context=snlc-mgmt-pro-landing-page&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Conversation Insights

</td><td>

-   Augment conversations with insights based on the Inferred CSAT score. The Inferred CSAT framework provides an estimated score computed using AI in real time by analyzing the entire sequence of the conversation.
-   Use underlying factors like Resolution, Confusion, Effort, Empathy, Next Steps, Frustration, Transfers, and Escalations to provide explainability to the Inferred CSAT scores.
-   Leverage the Inferred CSAT framework and Conversation Insights \[sn\_aci\_insights\] table linked to the Conversation \[sys\_cs\_conversation\] table to create adhoc dashboards and workflows for conversational analytics applications.

See [Conversation Insights](https://www.servicenow.com/docs/access?context=conversation-insights&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US) for more information.

</td></tr><tr><td>

Creator Studio

</td><td>

-   Create forms quickly by using Now Assist.
-   As of Creator Studio version 27.2.2, revamped navigation means you can more easily see what's in your app.
-   Populate any question on the form based on the answer given for a record choice question.
-   Use answers to form questions to trigger an activity in playbooks.
-   Switch seamlessly between no-code, mid-skill, and pro-code app development experiences for a more unified development platform with the new experience switcher.

See [Creator Studio](https://www.servicenow.com/docs/access?context=creator-studio-landing&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US) for more information.

</td></tr><tr><td>

Customer Contracts and Entitlements

</td><td>

-   Enable customers to create contracts from product inventory.
-   Added a new workspace view for service contracts and entitlements in Customer Service Management workspace for efficiently managing service contracts and entitlements.
-   Enable initiation of contract renewal automatically based on the configured date and pricing details.
-   Calculate the price of future renewals of contracts with a markup or mark down percentage of the current contract price.
-   Validate the contract end date to the product offering end date.

See [Customer Contracts and Entitlements](https://www.servicenow.com/docs/access?context=exploring-post-sales-support&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Customer Success Management

</td><td>

-   Define, measure, and track the overall health of an engagement and monitor risk signals and issues.
-   Manage all customer interactions in a single place and organize them with the touchpoint calendar.​
-   Create templates to define common success objectives and outcomes and associate them with a product.
-   Use Now Assist for Telecommunications, Media and Technology \(TMT\) to summarize account onboarding cases, engagements, and touchpoints.
-   Integrate your ServiceNow instance with external Customer Relationship Management \(CRM\) platforms during the engagement life cycle.

See [Account Lifecycle Events](https://www.servicenow.com/docs/access?context=account-lifecycle-events-landing&version=yokohama&pubname=yokohama-acct-lifecycle-events&ft:locale=en-US) for more information.

</td></tr><tr><td>

Data Loss Prevention Incident Response

</td><td>

-   Enhanced the ability to securely store, manage, and track evidence files within the platform for all Data Loss Prevention Incident Response integrations.
-   Preview the evidence file of an incident from either the DLP IR analyst workspace or end user workspace.
-   Enhanced the DLP incident closure process by adding support for closure codes.
-   Introduced the Playbook feature in the DLP IR workspace to enhance operational efficiency.
-   Improved response to Data Loss Prevention \(DLP\) incidents through the initiation of SLA triggers.

See [Data Loss Prevention Incident Response](https://www.servicenow.com/docs/access?context=dlp-landing&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Data Management

</td><td>

-   View insights into storage consumption on your instance and implement data management policies directly from the Data Management Console.
-   Automatically delete older or unwanted records with improved table cleaner scalability.

See [Data Management](https://www.servicenow.com/docs/access?context=c_DataManagement&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US) for more information.

</td></tr><tr><td>

Data Privacy

</td><td>

-   Leverage Data Privacy in Now Assist to discover sensitive data in Now Assist prompts and data send to models.
-   Sanitize sensitive data from Now Assist prompts without impacting response.
-   Discover sensitive data from attachments using enhanced Data Discovery jobs.

See [Platform Privacy](https://www.servicenow.com/docs/access?context=privacy-landing-page&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US) for more information.

</td></tr><tr><td>

Data management for CSM

</td><td>

-   Track the status and other information that is related to the Customer Life Cycle workflows by using the Sales and Order Management Request Tracker \(sn\_tmt\_core\_inbound\_queue\) table.
-   Track pricing and subscription information for products and services on the CSM Configurable Workspace by using the revenue metrics on the sold product form.
-   Integrate Strategic Portfolio Management \(SPM\) project management with business locations to create and manage projects across your organization.

See [Data management for Customer Service Management](https://www.servicenow.com/docs/access?context=csm-data-management&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Decision Builder in Workflow Studio

</td><td>

-   Filter condition and result columns in decision tables to show only relevant rows, simplifying large table edits.
-   Use the lookup icon to select a reference record from the default list view and the info icon to preview the record.
-   Use the pagination feature to switch between pages by selecting the page you'd like to see.
-   Activate rows or Deactivate rows to include or exclude the logic in that row while executing the decision tables.

See [Exploring Decision Tables](https://www.servicenow.com/docs/access?context=decision-designer-overview&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US) for more information.

</td></tr><tr><td>

DevOps Change Velocity

</td><td>

-   Integrate with the Harness orchestration tool to discover Harness pipelines and enable change automation.
-   Detect anomalies and issues in your DevOps Change Velocity instance using health scans.

See [DevOps Change Velocity](https://www.servicenow.com/docs/access?context=devops-landing-page-new&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Digital End-User Experience

</td><td>

-   Monitor whether the devices across your organization are adhering to the established application and policy metric compliance rules using the System compliance report.
-   Identify high-performance devices and learn the correlation between your device performance and overall system health by monitoring critical metrics, such as CPU usage, in the System performance report.
-   Monitor the multiple facets of the end-user network performance, including connection details, connection stability and path metrics, and application network hops.
-   Manage what DEX metrics are collected for a DEX agent policy, turn off collection of a metric, or change the frequency for a metric collection.
-   Set up file management to track and manage executable files on your organization devices.
-   Track and manage the Windows registry keys configured for monitoring on your organization devices.
-   View client health metrics with the Microsoft Configuration Manager \(MCM\) application.
-   Track the impacted device details from the Service Operations Workspace landing page. You can also track the details of all the impacted users and impacted devices from the active alerts.
-   Determine the device location based on the pre-defined custom logic.
-   Diagnose and resolve device issues using the Device health check capability provided by Digital End-user Experience Self-service.
-   Track the digital experience scores of the applications and devices that your employees use with the Digital Experience Score​ dashboard.
-   The Proactive Engagement application is integrated as part of the DEX suite of applications and is installed along with DEX.

See [Digital End-User Experience](https://www.servicenow.com/docs/access?context=dex-landing&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Digital Portfolio Management

</td><td>

-   Updated the Digital Portfolio Management \(DPM\) Admin Center.
    -   Added a Troubleshoot tab to the DPM Admin Center landing page to help you recalculate availability results and indicators for service offerings.
    -   Added the ability to configure the personal portfolio solution cards and to view relationships of business applications and application services.
-   Updated the key performance indicator \(KPI\) behavior so that you can drill down on time series KPI information and use an Active flag to hide KPIs in a KPI group.
-   Updated the DPM data model to improve visibility and reporting when an incident, problem, or change is in the application service's Impacted services or Affected CIs related list. The updated model rolls up the incidents, problems, and changes so that you can see the impacts in related business applications \(in the KPIs and Needs attention panels\).

See [Digital Portfolio Management](https://www.servicenow.com/docs/access?context=dpm-landing&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Dispute Rules Content Pack for Visa

</td><td>

Apply Visa Resolve Online \(VROL\) release 25.2 revision changes to Dispute Rules Content Pack for Visa questionnaire.

See [Dispute Rules Content Pack for Visa](https://www.servicenow.com/docs/access?context=dispute-rules-content-pack-for-visa-landing-page-1&version=yokohama&pubname=yokohama-financial-services-operations&ft:locale=en-US) for more information.

</td></tr><tr><td>

Document Intelligence

</td><td>

[Yokohama Patch 6](../quality/yokohama-patch-6.md)

-   Summarize content in document and image attachments with the document and visual insights AI agent.
-   Use Google Gemini and Anthropic Claude on AWS as AI model providers for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.

[Yokohama Patch 3](../quality/yokohama-patch-3.md)

-   Boost productivity by using the document and visual insights AI agent in Now Assist to autonomously analyze and extract data from documents and images.

[Early Availability](../quality/yokohama-all-other-fixes.md)

-   Speed up your document processing workflows and quickly extract the text and tables from your documents by using Now Assist.
-   Save time looking for the information that you need in a document and quickly find the answers to predefined questions by using Now Assist.

See [Document Intelligence](https://www.servicenow.com/docs/access?context=document-intelligence-landing&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US) for more information.

</td></tr><tr><td>

Document Services

</td><td>

-   Improved PDF generation that includes accessibility support.
-   Accelerate documents insights with instant summaries for highlights and quick insights, interactive Q&amp;A, and FAQs.

See [Document Services](https://www.servicenow.com/docs/access?context=document-services-landing-page&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US) for more information.

</td></tr><tr><td>

Domain Separation

</td><td>

Enable domain separation in live environments by using the Post-Production Domain Separation Activation Utility.

See [Domain separation for service providers](https://www.servicenow.com/docs/access?context=domain-sep-landing-page&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US) for more information.

</td></tr><tr><td>

Dynamic Translation

</td><td>

-   Preserve text, such as product names or technical terms, during machine translation with the Exclusion Framework feature.
-   The APIs used by default translator configurations are upgraded to v4. If you want to use v4 APIs with customized translator configurations, you must migrate them manually.
-   The spoke for IBM Watson Translator Service for IBM Cloud \(com.glide.ibm\_translation\_spoke\) is removed.

See [Dynamic Translation](https://www.servicenow.com/docs/access?context=dynamic-translation-overview&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US) for more information.

</td></tr><tr><td>

ERP Semantic Mining

</td><td>

[Yokohama Patch 3](../quality/yokohama-patch-3.md)

-   Easily clear a blocked ETL \(extract, transform, and load\) processing flow when an automatic or manual synchronization of ERP data between the ERP system of record and your ServiceNow instance is not successful by using the **Reset AI/ML analysis** option.

[Yokohama Patch 1](../quality/yokohama-patch-1.md)

-   View charts and graphs on the new ERP Semantic Mining home page dashboard.
-   Take guided tours with interactive steps to learn about features and interactively complete tasks in ERP Semantic Mining.

See [ERP Semantic Mining \(ERP-CM\)](https://www.servicenow.com/docs/access?context=erp-customization-mining-overview&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US) for more information.

</td></tr><tr><td>

Employee Center

</td><td>

-   Resolve tasks created from submitted negative feedback with the Integrated experience and service feedback functionality.
-   Enable employees to seek assistance through virtual or in-person appointments, or by joining walk-up queues for immediate support.
-   Host live company events seamlessly in the employee portal with streamlined pre-event communications and a drag-and-drop editor for easy content creation.

See [Employee Center](https://www.servicenow.com/docs/access?context=employee-center-landing-page&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Encryption Key Management

</td><td>

-   Column Level Encryption has been rebranded and redesigned to now be called Field Encryption.
-   Use Access Observer to help plan for and troubleshoot Field Encryption implementations.
-   Edge Encryption administrators can use the new process to migrate from Edge Encryption to Field Encryption.

See [Key Management Framework](https://www.servicenow.com/docs/access?context=encryption&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US) for more information.

</td></tr><tr><td>

Enterprise Architecture \(formerly Application Portfolio Management\)

</td><td>

Yokohama Patch 6

-   Select a fiscal period on the Application Rationalization pages using the new fiscal period filter option. The fiscal period filter enables you to view application rationalization data for the selected fiscal period.
-   Evaluate the technical debt score for business applications using the Technology Reference Model \(TRM\) technical debt indicator. This helps you to identify high-risk business applications and enables you to prioritize modernization and rationalization.
-   Generate business process modeling diagrams and model the future state of the business processes using Enterprise Modeling and Visualization.
-   Associate business capabilities to a business application from the business application related list.
-   View the past due certification tasks for your business applications from the Application Portfolio tab of the Insights section.
-   Generate scores for indicators and scoring profiles in the Enterprise Architecture Workspace.
-   Read-only access to the  Enterprise Architecture Workspace is added to the business stakeholder role \(sn\_apm.apm\_read\).

Yokohama General Availability

-   Generate business process modeling diagrams and model the future state of the business processes using Enterprise Modeling and Visualization.
-   Associate business capabilities to a business application from the business application related list.
-   View the past due certification tasks for your business applications from the Application Portfolio tab of the Insights section.
-   Generate scores for indicators and scoring profiles in the Enterprise Architecture Workspace.
-   Read-only access to the  Enterprise Architecture Workspace is added to the business stakeholder role \(sn\_apm.apm\_read\).

</td></tr><tr><td>

Enterprise Asset Management

</td><td>

-   Streamline firmware management with the new Firmware model class.
-   Get normalization coverage for firmware that is embedded into your industrial and IT hardware-based Operational Technology \(OT\) assets.
-   Achieve synchronization between physical assets and configuration items \(CIs\) for Operational Technology \(OT\) assets through MAC addresses.
-   Streamline OT Asset Management \(OTAM\) licensing to include hardware resource categories for OT hardware assets to access OT Asset Management features and workflows.
-   Get support for hardware models and OT hardware assets in the OT Asset Management workspace.
-   Benefit from accessibility improvements to create a configurable workspace that supports Web Content Accessibility Guidelines \(WCAG\) 2.1 Level AA conformance.

See [Enterprise Asset Management](https://www.servicenow.com/docs/access?context=enterprise-asset-management&version=yokohama&pubname=yokohama-it-asset-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Event Management

</td><td>

-   Review network traffic-based alert grouping, which uses discovered TCP connections together with ML Service Mapping to correlate alerts on host CIs that have network traffic connections between them. This approach reduces noise, enhances visibility, and accelerates response times by focusing on critical connections and dependencies.
-   Starting in version 26.3.4, benefit from the new alert grouping based on network traffic correlations:
    -   Investigate network traffic-based alert groups by using Express List®.
    -   Review alert group analysis by Now Assist
    -   View connections between network traffic-based alerts in **Link View**.
-   Enable team-level operators to create and manage their own integrations, set up their own alert automations, and enhancing control over alert management for their teams by assigning the new team\_operator role.
-   Review relevant information in the Now Assist panel based on records selected in the Express List®.
-   Starting in version 2.15.1, you can configure metric connector instances for the Nagios, SolarWinds, and Zabbix monitoring tools to receive metrics directly from these monitoring tools. This enhancement provides the following benefits:
    -   Seamlessly integrate monitoring data from multiple sources into Metric Intelligence.
    -   Improve anomaly detection and alerting with real-time metric ingestion.

See [Event Management](https://www.servicenow.com/docs/access?context=c_EM&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

External Content Connectors

</td><td>

[Yokohama Patch 11](../quality/yokohama-patch-11.md)

-   Expand your search experience with external content connectors for Adobe Experience Manager as a Cloud Service, Asana, Docusign, Dropbox, GitHub Enterprise Cloud, HubSpot, Lucidchart, Miro, monday.com, Notion, SAP DMS, Smartsheet, Trello, WordPress, Workday, and Zoom source systems.
-   Customize user permission settings, choosing the fields you want to compare when mapping source system users to ServiceNow AI Platform® users.
-   Make external content connector crawl results searchable by linking connector search sources to search profiles from the connector editor.
-   Monitor connector behavior on individual crawl runs and over time with improved crawl statistics and analytics.

[Yokohama Patch 6](../quality/yokohama-patch-6.md)

-   Expand your search experience by indexing searchable content from your Amazon S3, Box, GitLab, Microsoft OneDrive, Microsoft Viva Engage, and Zendesk Guide source systems.
-   Search KB articles from your ServiceNow instance.
-   Make web content locally searchable by indexing pages from predefined or custom public web sites with the Webcrawler external content connector.
-   Configure connector settings and schedule crawls as part of connector creation using the revamped UI.

[Yokohama Patch 3](../quality/yokohama-patch-3.md)

-   Expand your search by indexing searchable content from your Atlassian Jira Cloud, Google Drive, Microsoft Teams, and Slack source systems.
-   Make web content locally searchable by indexing pages from predefined public web sites.
-   Find answers about your ServiceNow deployment by indexing searchable content from the ServiceNow product documentation.
-   Know when your external content connectors are approaching their crawl limits with new warning messages.
-   Expand the range of information available to Virtual Agent users by adding external content search results to Now Assist in Virtual Agent conversations.
-   Improve recall for external content searches with support for semantic vector indexing of crawled content.

See [External Content Connectors](https://www.servicenow.com/docs/access?context=ext-cont-connectors-landing-page&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US) for more information.

</td></tr><tr><td>

Field Service Management

</td><td>

-   Define configurable rules that you can use to derive recommendation scores and optimize your appointment booking slots.
-   Create advanced dependency relationships among tasks to enhance scheduling accuracy.
-   Optimize your task assignments by using dependencies that align with the overall objectives and constraints of your resource allocation.
-   Streamline your capacity and resource management by using enhanced visualization in the Capacity Console.
-   Calculate the work duration for a work order task more accurately by using the Agent Efficiency feature.

See [Field Service Management](https://www.servicenow.com/docs/access?context=fsm-application-landing-page&version=yokohama&pubname=yokohama-field-service-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Financial Services Card Operations

</td><td>

-   Resolve friendly fraud disputes by incorporating friendly fraud detection and resolution in the existing dispute flow for Visa transactions. You can take actions such as crediting the customer, denying the dispute, or initiating an exception process.
-   The Financial Services Card Operations data model is updated in this release with reparented tables to align the data and manage the dispute transactions more effectively. See [Financial Services Card Operations](https://www.servicenow.com/docs/access?context=card-ops-landing-page&version=yokohama&pubname=yokohama-financial-services-operations&ft:locale=en-US) for more information.
-   Enhance the card disputes process with an updated end-to-end Visa disputes playbook that now includes support for reviewing associated transactions and handling pre-arbitration, arbitration, and appeals.
-   Manage and work on multiple disputed transactions for a case with individual playbooks for each disputed transaction.
-   Integrate new VROL subflows into the enhanced Visa card disputes playbook.

</td></tr><tr><td>

Financial Services Operations Core

</td><td>

The Claim Base \[sn\_bom\_claim\_base\] table has been updated in this release with additional fields. These fields were previously available only to specific applications. They're available in the Claim Base table and can be used across all other claim applications in this release.

See [Financial Services Operations Core](https://www.servicenow.com/docs/access?context=financial-services-operations-core-data-model&version=yokohama&pubname=yokohama-financial-services-operations&ft:locale=en-US) for more information.

</td></tr><tr><td>

Financial Services Operations Integration with Visa

</td><td>

-   Enables Visa VROL dispute resolution process by providing features such as accept dispute and cardholder purchase enquiry.
-   Ensures Visa conformance through error handling and timely updates on chargeback status.

See [Financial Services Operations Integration with Visa](https://www.servicenow.com/docs/access?context=financial-services-operations-integration-with-visa-landing-page&version=yokohama&pubname=yokohama-financial-services-operations&ft:locale=en-US) for more information.

</td></tr><tr><td>

Flows, subflows, and actions in Workflow Studio

</td><td>

-   Create a flow or a subflow from an image by using Now Assist.
-   Debug flows and subflows from a dedicated debugging tab.
-   Pause a flow until it receives a specific message from the flow API.
-   Run a published Now Assist skill from an action.
-   Save flow triggers for reuse in other flows.

See [Exploring flows](https://www.servicenow.com/docs/access?context=exploring-flows&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US) for more information.

</td></tr><tr><td>

Generative AI Controller

</td><td>

[Yokohama Patch 11](../quality/yokohama-patch-11.md)

-   Review changes to Now Assist usage measurement.
-   Some Now Assist skills, agents, and agentic workflows are on by default.
-   Additional role configuration is required for agentic workflows and AI agents included with Now Assist applications.

Previous Patch releases

-   Protect your users by configuring settings for anonymization of personally identifiable information \(PII\) with the Data Privacy application.

See [Generative AI Controller](https://www.servicenow.com/docs/access?context=generative-ai-controller&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US) for more information.

</td></tr><tr><td>

Hardware Asset Management

</td><td>

-   Achieve asset data accuracy, improve asset utilization, and reduce risk through Asset Attestation.
-   Streamline Hardware Asset Management \(HAM\) licensing for only non-OT hardware assets to access Hardware Asset Management features and workflows.
-   Benefit from accessibility improvements to create a configurable workspace that supports Web Content Accessibility Guidelines \(WCAG\) 2.1 Level AA conformance.

See [Hardware Asset Management](https://www.servicenow.com/docs/access?context=ham-landing-page&version=yokohama&pubname=yokohama-it-asset-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Health Log Analytics

</td><td>

-   Use the enhanced Splunk data input to ingest data from Splunk in a preprocessed structured format. You can also pull data from Splunk regularly using the new Splunk Polling data input.
-   Take advantage of a unified interface for convenient data input integration by setting up integrations from the Integrations Launchpad.
-   Streamline HLA data ingestion with tools for handling large log volumes by using dedicated Cribl and Edge Delta data inputs.
-   Configure log data integrations for Splunk TCP/UDP, Splunk Poller, MID Server, Apache Kafka, Microsoft Azure Log Analytics, REST API, and Amazon Data Firehose conveniently from the Integrations Launchpad.
-   Generate a description of Health Log Analytics alerts using Now Assist.

See [Health Log Analytics](https://www.servicenow.com/docs/access?context=hla-landing-page&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Healthcare Operations Core

</td><td>

-   Gain visibility into operational cases that are related to your care team and create support requests using the Care Team Portal.
-   Expand operational cases to supporting services departments by leveraging the Healthcare Operations case type.
-   Utilize the streamlined admin experience for creating healthcare organizations and hierarchies.

See [Healthcare Operations Core](https://www.servicenow.com/docs/access?context=hcls-cto-app&version=yokohama&pubname=yokohama-healthcare-life-sciences&ft:locale=en-US) for more information.

</td></tr><tr><td>

Hermes Messaging Service

</td><td>

-   View the audit history for all topic operations.
-   Scan and inspect topic messages using keywords or regular expressions.
-   Monitor the health of Hermes components over time.

See [Hermes Messaging Service](https://www.servicenow.com/docs/access?context=hermes-messaging-service&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US) for more information.

</td></tr><tr><td>

ITOM AIOps

</td><td>

Health Log Analytics highlights:

-   Pull data from Splunk consistently over time using the Splunk Polling data input, which sends recurring queries \(polls\) to Splunk.
-   Use your Splunk data input to ingest data from Splunk in a pre-processed, structured format.
-   Integrate with log data connectors from the Integrations Launchpad
-   Use dedicated Cribl, Edge Delta and Vector Agent data inputs to streamline HLA data ingestion with tools handling large log volumes.
-   Generate a description of Health Log Analytics alerts using Now Assist.

Event Management highlights:

[Service Operations Workspace for ITOM](https://www.servicenow.com/docs/access?context=sow-landing-page-itom&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)

-   Starting with version 26.3.1, benefit from the new alert grouping based on network traffic correlation:
    -   Use Express List® to investigate network traffic-based alert groups
    -   View connections between network traffic-based alerts in Link View.
    -   Starting with version 2.5.3, review alert group analysis by Now Assist
-   Review relevant information in the Now Assist panel based on records selected in Express List®.
-   Enable team-level operators to create and manage new alert automations by assigning the new team\_operator role.
-   Map current alert field values to new specified values through the new **Change alert values** option in the Enrich automation section.
-   Track and optimize grouping efficiency by viewing key details such as total alerts, alert groups, ungrouped alerts, and compression in Group Automation. Simulate other group types, such as CMDB, ML, and text-based grouping.

Agent Client Collector highlights:

See [ITOM AIOps](https://www.servicenow.com/docs/access?context=itom-health-landing-page&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

ITOM Cloud Accelerate

</td><td>

Cloud Workspace highlights:

-   The new Cloud Workspace application has includes a new feature called Cloud Account Management, which automates account creation, improves transparency, and integrates policy-based governance and certification processes, enhancing efficiency and control across multiple cloud platforms.
-   Support for AWS account and Azure subscription requests via direct API integrations or Terraform and GitHub integrations.

Performance enhancements for the predefined catalog items in CSC Content Pack.

See [Cloud Governance](https://www.servicenow.com/docs/access?context=cloud-governance&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

ITOM Optimization

</td><td>

Legacy workflows have been upgraded and seamlessly migrated to the advanced Workflow Studio to align with the latest standards and ensure modern compliance. Additionally, all default \(Out of Box\) workflows have been redesigned to provide enhanced performance, improved usability, and a more streamlined experience.

See [ITOM Optimization](https://www.servicenow.com/docs/access?context=itom-optimization-landing-page&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

ITOM Visibility

</td><td>

-   Discovery and Service Mapping Patterns: Gain enhanced visibility into your AWS cloud services with 27 additional patterns starting with store version 1.25.0.
-   Starting with store version 1.1.0, ACC for Visibility has been renamed Agent Client Collector for Visibility - Content. The CNO for Visibility feature has been extracted from Agent Client Collector for Visibility - Content and is now a separate application.
-   Starting with Service Graph Connector for GCP store release 1.8, Service Graph Connector for AWS store release 2.9, and Service Graph Connector for Microsoft Azure store release 1.11, you can use Service Graph Connectors to ingest data into the Configuration Management Database \(CMDB\) from third-party sources.
-   Starting with store version 1.8.0, Discovery admins gain improved visibility into discovery issues and can address root causes using anomaly detection in the Discovery Admin Workspace.

See [ITOM Visibility](https://www.servicenow.com/docs/access?context=itom-visibility-landing-page&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

ITSM Mobile Agent

</td><td>

Starting in the 9.1 release, you can do the following:

-   Summarize the incident record and activity information when adding work notes to an incident record or while reassigning an incident.
-   Set different alert tones for incidents with different priority levels.
-   Set the incident impact and urgency levels to set the incident priority level automatically.
-   Redirect from the mobile web browser to the ITSM Mobile Agent app seamlessly when opening and viewing different task records.

See [ITSM Mobile Agent](https://www.servicenow.com/docs/access?context=itsm-mobile-agent&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

ITSM Success Dashboard

</td><td>

Experience the all new KPIs introduced for the Now Assist under Productivity moments per user in ITSM Success Dashboard to understand the benefits of using Now Assist features like Change Summarization, Change Risk Explanation, and Knowledge Article generation.

See [ITSM Success Dashboard indicators](https://www.servicenow.com/docs/access?context=success-dashboard-indicator-landing&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Identity

</td><td>

 

</td></tr><tr><td>

Impact

</td><td>

-   Adopt ServiceNow products and measure their value, gain access to expert guidance and personalized recommendations, maintain a high-performing platform, and enhance business continuity with 24 x 7 technical support.
-   Access the Impact Store Application integrated within your ServiceNow instance and connected to the Impact Delivery Instance \(IDI\) portal.
-   Use Proactive Code Check to track compliance against leading practices for coding and organizational standards.
-   Jumpstart your understanding and assessment of ServiceNow platform capabilities with new Accelerators that provide a demonstration of the possibilities and capabilities with instance features and maximize value exactly where you need it.

See [Impact Store Application](https://www.servicenow.com/docs/access?context=impact-store-app&version=yokohama&pubname=yokohama-impact&ft:locale=en-US) for more information.

</td></tr><tr><td>

Incident Management

</td><td>

-   Increase the operational efficiency of the tier 1 service desk agents with the dedicated sn\_service\_desk\_agent role.
-   Control whether an incident or major incident record link in an email notification redirects you to the record in the classic UI16 interface or Service Operations Workspace \(SOW\).
-   Enable agents with incident write access, callers, requesters, and **Opened by** end users to reopen a resolved incident from the Incident Management classic UI16 form, SOW, or Portal UIs.
-   Restrict unauthorized access to incident-related tables using deny ACLs.
-   Search for a configuration item \(CI\) in a list alphabetized by the CI name with an improved search performance.

See [Incident Management](https://www.servicenow.com/docs/access?context=c_IncidentManagement&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Industrial Process Manager

</td><td>

-   Identify sites on your equipment model entity that aren't in use with a new **Operational Status** field value in the Industrial Workspace.
-   Filter out **Not in use** or **Retired** equipment model entities in the Industrial Workspace using the **Operational Status** field value.
-   Sort equipment model entities for a Site using the new value **Processing Order**.
-   View the **Daily Activity** tab for a summarized version of the previous day's activities on Operational Technology \(OT\) devices.
-   Organize your OT device data by capturing the mapped equipment model entity for an OT device.
-   View the relationships between devices and other configuration items \(CIs\) with the Unified Map experience in the Industrial Workspace.

See [Industrial Process Manager](https://www.servicenow.com/docs/access?context=industrial-process-manager-overview&version=yokohama&pubname=yokohama-operational-technology&ft:locale=en-US) for more information.

</td></tr><tr><td>

Instance Data Replication

</td><td>

-   Replicate data that's frequently updated in large tables on your instance by scheduling data replication.
-   Queue multiple seeding requests from your producer instance.
-   Reseed missing or mismatched records automatically when creating a data comparison request.

See [Instance Data Replication](https://www.servicenow.com/docs/access?context=instance-data-replication&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US) for more information.

</td></tr><tr><td>

Insurance Claims Core

</td><td>

The Claim Incident \[sn\_ins\_claim\_property\] table has been updated in this release with additional fields. These fields were previously available only to specific applications. They're available in the Claim Incident table and can be used across all other claim applications in this release.

See [Insurance Claims Core](https://www.servicenow.com/docs/access?context=insurance-claims-core-data-model&version=yokohama&pubname=yokohama-financial-services-operations&ft:locale=en-US) for more information.

</td></tr><tr><td>

Integration Hub

</td><td>

-   Get alerts and alert notifications for your Stream Connect integrations.
-   Use error evaluation with Data Stream actions to catch step errors and specify error behavior for each step.
-   Edit, configure, and create connection aliases in the Action Properties section of actions in Workflow Studio.

See [Integration Hub](https://www.servicenow.com/docs/access?context=integrationhub&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US) for more information.

</td></tr><tr><td>

Intelligence for CSM

</td><td>

-   Enabled Recommended Actions for chat interactions so that agents can select relevant actions that are based on the chat context.
-   Integrated enhanced knowledge guidance on the Front-line case page and enable agents to attach and add links to knowledge articles in comments, work notes, or emails by using modeless dialogs.
-   Enabled Recommended Actions – AI search for CSM default record page and CSM interaction record pages for the video, chat, walk-up, and email channels.
-   Automated the mapping configuration for search results along with default guidances.

See [Intelligence for CSM](https://www.servicenow.com/docs/access?context=intelligence-csm&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Journey designer

</td><td>

Yokohama Patch 3

-   As a journey user, track your journey more effectively—view real-time journey states, follow your progress with an improved progress bar, and easily filter your journeys to find exactly what you need.
-   As a manager, request the status of an employee’s journey to quickly understand progress and take timely, informed action.
-   Managers can instantly summarize the information that appears on the Journey detail page to acquire an overview of an employee's journey. The summary that is generated also reflects the blockers that are impeding the journey's progress and the steps required to resume the journey's progress.
-   View banner messages on the Journey detail page when your journey status is marked as ‘Overdue’ due to others’ pending tasks. The messages are tailored based on personas and help you understand the reason of the overdue task.
-   Use the updated ‘All Tasks’ filter, which now matches the overall task count shown in the progress bar. Read the revised tooltip on the Progress Bar that states, ‘Completed tasks include skipped tasks.’ Check the information icon on the ‘All Tasks’ filter to understand that ‘Some of the total tasks may not be visible to you in this Journey,’ ensuring clarity on task visibility.

-   As a manager, managing the journey of reportees using Journey designer you can draft a journey with custom plans and tasks with help from Now Assist. Provide an AI prompt so that Now Assist can help you build a journey that matches your career goals and aspirations.
-   The following Lifecycle Events flows have been migrated to flows.
    -   HR Activity Set Trigger Check
    -   Lifecycle Event Notification
    -   Lifecycle Event Case Approval
    -   HR Activity Set Launcher
    -   HR Activity Launcher
    -   Account Notification
    -   Add LE activity user to Pulse Survey

See [Journey designer](https://www.servicenow.com/docs/access?context=jny-dsgnr-landing-page&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Knowledge Graph

</td><td>

[Yokohama Patch 11](../quality/yokohama-patch-11.md)

-   Review changes to Now Assist usage measurement.
-   Some Now Assist skills, agents, and agentic workflows are on by default.
-   Additional role configuration is required for agentic workflows and AI agents included with Now Assist applications.
-   Knowledge Graph now supports aggregate queries.
-   Improved accuracy for Now LLM Service.

[Yokohama Patch 8](../quality/yokohama-patch-8.md)

-   Admins can create Knowledge Graph schema with Workflow Data Fabric tables that enables users to retrieve data from different systems without moving them. This ensures efficiency and security when working with external tables.

Yokohama Patch 6

-   Use Google Gemini and Anthropic Claude on AWS as AI model providers for Knowledge Graph in addition to Now LLM Service and Azure OpenAI
-   Select your preferred large language model \(LLM\) provider for Now Assist platform. Apart from Now LLM Service, the platform supports Azure OpenAI GPT-4.1 and GPT-4.1 mini, Google Gemini 2.0 Flash and 2.5 Pro, and AWS Anthropic Claude 3.7 Sonnet LLM providers with ServiceNow® third-party model strategy.
-   Supports nodes from parent and grandparent nodes from the hierarchy.
-   Supports CMDB queries in Now Assist panel.

[Yokohama Patch 3](../quality/yokohama-patch-3.md)

-   Seamlessly integrated with Now Assist in Virtual Agent, AI Agents and AI Search enabling personalized search results and context driven skills execution.
-   Seamless Integration with Now Assist in Virtual Agent for Natural Language Query.
-   Use Knowledge Graph as a tool to complete custom tasks for AI Agents.

[Yokohama Patch 1](../quality/yokohama-patch-1.md)

-   Knowledge Graph helps you in transforming large amount of data into a semantic representation, fostering more connected and customized user experiences.
-   Knowledge Graph boosts Virtual Agent by enabling large language models \(LLMs\) to provide contextually relevant responses tailored to each user.
-   Knowledge Graph creates a complex data model called Knowledge Graph schema with numerous entities and their relation within a few steps.
-   Knowledge Graph admins can use Knowledge Graph to create and manage the Knowledge Graph schemas. These Knowledge Graph schemas are the customized Knowledge Graph that consist of nodes, node properties, and edges.

See [Knowledge Graph](https://www.servicenow.com/docs/access?context=knowledge-graph-landing&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US) for more information.

</td></tr><tr><td>

Knowledge Management

</td><td>

Yokohama Patch 6

-   Use Google Gemini and Anthropic Claude on AWS as AI model providers for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.
-   Customize prompts for AI model providers to generate Knowledge articles with Now Assist.

-   Identify and resolve accessibility-related issues during Knowledge article generation through a new accessibility checker button in the TinyMCE toolbar.
-   Enhance the creation and management of knowledge base through features in the Knowledge Management advanced plugin such as article versioning, article subscriptions, article templates, and an article quality index.

See [Knowledge Management](https://www.servicenow.com/docs/access?context=knowledge-management&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US) for more information.

</td></tr><tr><td>

Lead Management

</td><td>

-   REST APIs enable seamless integration of lead management with external applications and provide other capabilities.
-   REST APIs enable customers to create, update, and retrieve leads and lead line items from the ServiceNow instance.

See [Lead Management](https://www.servicenow.com/docs/access?context=lead-management&version=yokohama&pubname=yokohama-order-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Legal Hold Notification

</td><td>

-   Streamlined legal hold life cycle: Streamline the legal hold workflow by enabling you to create legal hold matters, assign custodians, issue notices, track acknowledgments, and ensure compliance throughout the process.
-   Enhance custodian engagement by sending them legal hold notifications and reminders to ensure timely acknowledgment and accountability throughout the legal hold process.
-   Reduce legal risk compliance with a controlled closure process. When the legal hold is officially closed, the Legal Hold Notification application stores detailed information about the preserved data.

See [Legal Hold Notification](https://www.servicenow.com/docs/access?context=lg-hold-notif-landing-page&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

MID Server

</td><td>

-   MID Server supports and requires a minimum JRE version 17. The MID Server is bundled with version 17.0.12 and the minimum JRE version supported is 17.0.10.
-   The MID Server can now be installed on Windows hosts directly as a LocalSystem or non-admin user with Start and Stop permissions.

See [MID Server](https://www.servicenow.com/docs/access?context=mid-server-landing&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US) for more information.

</td></tr><tr><td>

Manager Hub

</td><td>

-   Enable manager-employee conversation scheduling.
-   Track skill proficiency and assign targeted learning for effective development by using the Kill score analysis panel.
-   Enable managers to view all direct and indirect reports by using multi-manager reporting to improve team productivity and engagement.

See [Manager Hub](https://www.servicenow.com/docs/access?context=manager-hub-overview&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Manufacturing Commercial Operations

</td><td>

-   Enable manufacturers, customers, suppliers, channels, and partners to connect and track services directly between instances without configuring and maintaining custom integrations.
-   Enable B2B customers to configure products and place orders via an uptake of the Sales Customer Relationship Management self-service order placement feature​.​
-   Transform emails into interactions rather than cases with email interactions.
-   Enable the dealer and sales promotion framework and its user role and responsibilities.
-   Configure the Manufacturing Commercial Operations plugins.

See [Exploring Manufacturing Commercial Operations](https://www.servicenow.com/docs/access?context=manufacturing-explore&version=yokohama&pubname=yokohama-manufacturing&ft:locale=en-US) for more information.

</td></tr><tr><td>

Mastercard Spoke

</td><td>

-   Use the Mastercard Spoke to manage card disputes using the Mastercom API Suite and Mastercom Extended APIs.
-   Leverage Mastercard Spoke actions to manage disputes for cleared Single Message System original transactions with Mastercom Extended.

See [Mastercard Spoke](https://www.servicenow.com/docs/access?context=mastercard-spoke&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US) for more information.

</td></tr><tr><td>

Mentoring

</td><td>

-   Auto-close mentoring relationship a certain number of days after the due-date. Configure the number of days followed by a grace period to allow any final interactions before auto-closure.
-   Store a Mentoring snapshot of all overlapping preferences at the time of the relationship acceptance by the mentor. Derive skills tagged to Mentoring Relationships based on the snapshot.
-   As a mentee, view Match Insights with a particular Mentor to understand how well they are matched before choosing the Mentor.
-   As a mentee, share mentoring preferences and timeline information with your manager that help in the validation of your skills.

See [Mentoring](https://www.servicenow.com/docs/access?context=mentoring-egd-overview&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Mobile Platform

</td><td>

-   Write and refine text with the Now Assist Context Menu.
-   Use enhanced capabilities within the input form screen.

See [Mobile Platform](https://www.servicenow.com/docs/access?context=mobile-config-navigation&version=yokohama&pubname=yokohama-mobile&ft:locale=en-US) for more information.

</td></tr><tr><td>

Next Experience

</td><td>

-   Create personalized keyboard shortcuts to streamline your workflow and boost productivity.
-   Track the filters that you apply to your Workspace lists within the History menu. Each time you change your filter, the History menu displays a separate entry.
-   Quickly locate and adjust your user preferences by using the new streamlined search function.
-   User preference icons now adopt your theme colors.

See [Next Experience UI](https://www.servicenow.com/docs/access?context=next-experience-landing-page&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US) for more information.

</td></tr><tr><td>

Next Experience Components

</td><td>

-   Build rich UI experiences with prebuilt system or custom components. To view the Next Experience Components API reference, usage guidance, and ServiceNow® UI Builder setup documentation, visit the [Developer site Next Experience Components doc](https://developer.servicenow.com/dev.do#!/reference/next-experience/components%3Freleases%5B%5D=washingtondc%26query=%26order_by=nameAsc%26limit=120%26offset=0%26categories%5B%5D=uib_component%26categories%5B%5D=uib_macroponent-component%26categories%5B%5D=uib_facades).
-   Use common web component patterns and principles, such as a JavaScript framework, immutable data, and simple action handlers.
-   Reuse components across multiple user interfaces to create a cohesive experience for your end users.
-   Use preset property values to configure properties and event handlers automatically for a component so the component is ready to work when you add it to a page. Presets can connect to a controller that acts as a data resource for the component. For more information, see [Automatically configure components using presets](https://www.servicenow.com/docs/access?context=presets&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US) and [Bind data to UI Builder pages using controllers \(advanced feature\)](https://www.servicenow.com/docs/access?context=controllers&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US).

</td></tr><tr><td>

Next Experience Developer \(NED\) Tools

</td><td>

Reduce troubleshooting time with enhanced component visualization, filters for traces, and new event filters.

See [Next Experience Developer Tools](https://developer.servicenow.com/dev.do#!/reference/next-experience/yokohama/developer-tools/using-next-experience-developer-tools) for more information.

</td></tr><tr><td>

Notifications

</td><td>

-   Use the new email notifications dashboard with key metrics.
-   Use filter notifications that are based on categories, delivery channels, subscriptions, and digests for notification preferences.
-   Use the enhanced assignment group, advanced condition, and mandatory notifications for a provider framework.
-   Use the standard forms for custom notification preferences and delivery channels.

See [Notifications](https://www.servicenow.com/docs/access?context=notifications&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US) for more information.

</td></tr><tr><td>

Notify

</td><td>

-   Enhanced security for all client-callable script includes by enabling switching off the sandbox mode.
-   Enhanced security access for Notify tables.

See [Notify](https://www.servicenow.com/docs/access?context=notify-landing-page&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US) for more information.

</td></tr><tr><td>

Now Assist

</td><td>

[Yokohama Patch 11](../quality/yokohama-patch-11.md)

-   Review changes to Now Assist usage measurement.
-   Some Now Assist skills, agents, and agentic workflows are on by default.
-   Additional role configuration is required for agentic workflows and AI agents included with Now Assist applications.
-   Use the Now Assist context menu open prompt feature to create and edit knowledge articles.
-   Use Advanced settings to add conditions to hide or show the Now Assist Context Menu quick actions.
-   Create multiple Now Assist context menu configurations for the same field.
-   Use the Enable for extended tables option in parent table configuration, to enable or disable the inheritance model for the child table configurations.

[Yokohama Patch 8](../quality/yokohama-patch-8.md)

-   Use the Now Assist Readiness Evaluation app to automate the implementation assessment process before implementing Now Assist agentic and generative AI.

[Yokohama Patch 6](../quality/yokohama-patch-6.md)

-   Enable administrators to set up a security access control list \(ACL\) that checks user authentication for Now Assist context menu skills and new setup options. This gives them control over who can use Now Assist context menu skills and actions, as well as the built-in options like shorten, elaborate, and change tone.

-   Use Google Gemini and Anthropic Claude on AWS as AI model providers for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.
-   Select your preferred large language model \(LLM\) provider for Now Assist out-of-box skills. Apart from Now LLM Service, the platform supports Azure OpenAI GPT-4.1 and GPT-4.1 mini, Google Gemini 2.0 Flash and 2.5 Pro, and AWS Anthropic Claude 3.7 Sonnet LLM providers with ServiceNow® third-party model strategy.
-   Select a display option for custom Now Assist context menu event with an option to suppress the modeless window.
-   View the numbered citation and links to the source of information when you use Now Assist context menu for Email reply recommendation.

[Yokohama Patch 3](../quality/yokohama-patch-3.md)

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

See [Now Assist](https://www.servicenow.com/docs/access?context=platform-now-assist-landing&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US) for more information.

For more Platform Now Assist feature release notes, see the following topics:

-   [AI Search release notes](../now-platform-administration/ai-search-rn.md)
-   [Document Intelligence release notes](../analytics-intelligence-reporting/document-intelligence-rn.md)
-   [Now Assist Skill Kit release notes](../analytics-intelligence-reporting/na-skill-kit-rn.md)
-   [Now Assist in Virtual Agent release notes](../conversational-interfaces/now-assist-va-rn.md)

</td></tr><tr><td>

Now Assist AI agents

</td><td>

[Yokohama Patch 11](../quality/yokohama-patch-11.md)

-   Review changes to Now Assist usage measurement.
-   Execute agentic workflows, AI agents, and tools in AI Agent Studio with role masking.
-   Additional role configuration is required for agentic workflows and AI agents included with Now Assist applications.
-   Run and review agentic workflow executions on forms in the Core UI and workspaces.
-   Framework extensibility with a new condition builder.
-   Support multilingual conversations.

[Yokohama Patch 6](../quality/yokohama-patch-6.md)

-   Create and maintain versions of LLM instructions for AI agents and agentic workflows to help organize and iterate on prompts and test their effectiveness.
-   Follow updated guided setup steps for agentic workflows and AI agents with additional guidance for successful instructions sent to the LLM.
-   Duplicate existing script, record operations, and search retrieval tools to reduce the work needed to create unique AI agents.
-   Monitor new analytics in the AI Agents Analytics dashboard to track valuable insights in customer satisfaction with AI interactions.
-   Use Google Gemini and Anthropic Claude on AWS as AI model providers for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.
-   View the agentic workflow and AI agent activity on your AI Agent Studio.
-   Map the right agents for agentic workflow execution with Dynamic orchestrator in Virtual Agent for better performance and accuracy.
-   Create different types of AI agents.
-   Custom output transformation strategies for an AI agent.
-   Execute AI agents and agentic workflows from workspace or Core UI.
-   Run AI agents and agentic workflows in a non-interactive execution mode.

[Yokohama Patch 3](../quality/yokohama-patch-3.md)

-   Use cases in Now Assist AI agents are now called agentic workflows.
-   Choose either Azure OpenAI or Now LLM Service as your preferred large language model \(LLM\) for AI agents and agentic workflows in the AI Agent Studio settings.
-   Use Virtual Agent for AI agent interactions.
-   Execute agentic evaluation runs to evaluate agentic workflows based on execution log data to compare against benchmarks and monitor performance.
-   Improve the quality of LLM responses by passing information between tools.
-   Hide citations for an agentic workflow or AI agent.
-   Transactions done by an AI agent for an agentic workflow are recorded in the name of the AI agent.
-   Enable AI agents to store and retrieve memories with categories.
-   Use Knowledge graph and File retrieval as tools in creating an AI agent.

[Yokohama Patch 1](../quality/yokohama-patch-1.md)

-   Define agentic workflows with an execution plan for automatically resolving the incoming cases and incidents.
-   Use the Now Assist panel to communicate with the agent during issue resolution.
-   Clone existing AI agents and agentic workflows to save time and avoid manual configuration.
-   Enable Now Assist Guardian to automatically identify and block offensive messages.
-   View the usage and performance of your AI agents with the AI agent analytics dashboard.
-   Enable multiple conversations for AI agents on the Now Assist panel.

See [Now Assist AI agents](https://www.servicenow.com/docs/access?context=na-ai-agents&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US) for more information.

For the Platform Now Assist release notes, see [Now Assist release notes](../analytics-intelligence-reporting/now-assist-rn.md).

</td></tr><tr><td>

Now Assist Analytics

</td><td>

-   Track the usage and adoption of your Now Assist implementation.
-   Monitor the performance of guardrails enabled through Now Assist Guardian.
-   Gain insights into the search performance in Now Assist self-service experiences.
-   Track the estimated efficiency and productivity gains enabled through Now Assist.

See [Analyzing Now Assist performance](https://www.servicenow.com/docs/access?context=now-assist-analytics&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US) for more information.

</td></tr><tr><td>

Now Assist Skill Kit

</td><td>

[Yokohama Patch 11](../quality/yokohama-patch-11.md)

-   Review changes to Now Assist usage measurement.
-   Some Now Assist skills, agents, and agentic workflows are on by default.
-   Additional role configuration is required for agentic workflows and AI agents included with Now Assist applications.

Yokohama Patch 6

-   Use UI Builder to deploy custom skills.
-   Import data into Now Assist Skill Kit with a CSV file.
-   Use AI to create ground truth for your data.
-   Use a custom data generator to create synthetic datasets.

-   Users can create synthetic data in Now Assist Data Kit.
-   Generated synthetic data can be saved as a dataset.
-   Add and manage tools of a custom skill, visually in the new Tools editor, including conditional execution of tools.
-   Customize ServiceNow skills with new prompts or providers in Now Assist Skill Kit to suit your specific business needs.

See [Now Assist Skill Kit](https://www.servicenow.com/docs/access?context=now-assist-skill-kit-landing&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US) for more information.

</td></tr><tr><td>

Now Assist for App Engine

</td><td>

[Yokohama Patch 11](../quality/yokohama-patch-11.md)

-   Review changes to Now Assist usage measurement.
-   Some Now Assist skills, agents, and agentic workflows are on by default.
-   Additional role configuration is required for agentic workflows and AI agents included with Now Assist applications.

[Yokohama Patch 3](../quality/yokohama-patch-3.md)

-   Create and deploy AI agents within custom applications, helping to empower creators and accelerate time-to-value.
-   Build custom AI agents and skills for the unique workflow of an application using Now Assist Skill Kit and AI Agent Studio.
-   Leverage AI agents and skills created with Now Assist for App Engine in custom applications at runtime, helping improve efficiency.

See [Now Assist for App Engine](https://www.servicenow.com/docs/access?context=add-ai-to-custom-apps-with-now-assist-for-app-engine-enterprise&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US) for more information.

</td></tr><tr><td>

Now Assist for Collaborative Work Management

</td><td>

[Yokohama Patch 11](../quality/yokohama-patch-11.md)

-   Review changes to Now Assist usage measurement.
-   Some Now Assist skills, agents, and agentic workflows are on by default.
-   Additional role configuration is required for agentic workflows and AI agents included with Now Assist applications.

[Yokohama Patch 3](../quality/yokohama-patch-3.md)

-   Help increase efficiency by automatically creating tasks from the context of your CWM Docs and adding them to the required Board.
-   Enable saving time by summarizing and paraphrasing blocks of content or a whole page in CWM Docs using generative AI capabilities.

See [Now Assist for Collaborative Work Management \(CWM\)](https://www.servicenow.com/docs/access?context=now-assist-for-cwm-landing&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Now Assist for Configuration Management Database \(CMDB\)

</td><td>

[Yokohama Patch 11](../quality/yokohama-patch-11.md)

-   Review changes to Now Assist usage measurement.
-   Some Now Assist skills, agents, and agentic workflows are on by default.
-   Additional role configuration is required for agentic workflows and AI agents included with Now Assist applications.

Previous Patch releases

-   Select **Summarize** on a CI form, in the workspace, or from any list to view a concise summary of key CI data directly on the form: discovery and class details, associated business services, security vulnerabilities, and related records like incidents, alerts, problems, and change requests.
-   The 'Manage duplicate CIs' skill identifies duplicate CIs, populates remediation tasks, and then assigns the tasks to the appropriate group. You follow step-by-step guidance and can preview remediation results before selecting a template. The updated CI correctness scores enable the CMDB Health Dashboard to display accurate information.

See [Now Assist for Configuration Management Database \(CMDB\)](https://www.servicenow.com/docs/access?context=now-assist-landing-cmdb&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US) for more information.

</td></tr><tr><td>

Now Assist for Creator

</td><td>

[Yokohama Patch 11](../quality/yokohama-patch-11.md)

-   Review changes to Now Assist usage measurement.
-   Create, edit, and deploy fully functional ServiceNow applications using the Build Agent in the ServiceNow IDE.
-   Generate catalog items conversationally and preview them during the creation process with Now Assist in Catalog Builder.
-   Choose an AI model provider for all Now Assist for Code skills in the script editor.

[Yokohama Patch 8](../quality/yokohama-patch-8.md)

-   Removed the now.assist.creator role as a requirement for test generation.

[Yokohama Patch 6](../quality/yokohama-patch-6.md)

-   Use Google Gemini and Anthropic Claude on AWS as AI model providers for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.

**Note:** Additional AI model providers are supported for the following Now Assist for Creator skills:

    -   App generation
    -   App summarization
    -   Catalog item generation
    -   Code generation
    -   Flow generation
    -   Flow summarization
    -   Playbook generation
    -   Process Mining
    -   RPA bot generation
    -   Spoke generation
    -   Test generation

[Yokohama Patch 3](../quality/yokohama-patch-3.md)

-   Summarize what a flow or subflow does by using generative AI.
-   Generate playbooks from inputs that refer to active actions, flows, subflows, content from installed spokes, or activity definitions.
-   Create automation and UI components in Now Assist for app generation.
-   Use the code explain and summarize feature of Now Assist for Code to explain and summarize the code. This feature is supported by both Now LLM Service and the Azure OpenAI model providers.
-   Use the Client Script Summarization skill to generate a high-level summary and a detailed explanation of a client script.

[Yokohama Patch 1](../quality/yokohama-patch-1.md)

-   Enable your users to create applications by using the Now Assist for app generation skill even if they don't have the admin role.
-   Use the improved application preview before generating an application by using the Now Assist for app generation skill.
-   Enable your RPA Desktop Design Studio users to create and edit automations and activities, and extend automation logic flow with Now Assist for RPA Hub.
-   Enable your ServiceNow Studio users to generate a summary of an app.
-   Use the **Quick Actions** button in the Now Assist for Code enabled script editor to edit code and add comments.
-   Use the prompt modal in inline or floating mode with Now Assist for Code.
-   Now Assist for Code now supports both Now LLM Service and Azure OpenAI model providers. When you select the Azure OpenAI model provider, all requests for the Now Assist for Code model are redirected to Azure OpenAI for evaluation and response. Additionally, you get access to the Code Explain and Code Summarize features.
-   Use the auto-complete feature of Now Assist for Code to get contextually relevant code suggestions while typing.

See [Now Assist for Creator](https://www.servicenow.com/docs/access?context=now-assist-for-creator-landing&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US) for more information.

</td></tr><tr><td>

Now Assist for Customer Service Management \(CSM\)

</td><td>

[Yokohama Patch 11](../quality/yokohama-patch-11.md)

-   Review changes to Now Assist usage measurement.
-   Enabled is\_template for all Now Assist skills and added support to clone and customize any base system GenAI skill in the Now Assist Skill Kit.
-   Defined the navigation path for Sentiment Analysis dashboard in Core UI to make accessing sentiment analysis data easier.
-   Track trending case topics with insights, visualizations, and customizable filters for deeper analysis with the Trending topics dashboard.
-   Monitor customer sentiment across cases with LLM-powered insights and track the sentiment trends in the dashboard.
-   Enable agents to access customer, case, and product details instantly through natural language queries with the Provide customer 360 insight agentic workflow.
-   Auto-generate work notes and comment recommendations to help improve agent efficiency with the activity response generation skill.
-   Additional role configuration is required for agentic workflows and AI agents included with Now Assist applications.

[Yokohama Patch 6](../quality/yokohama-patch-6.md)

-   Enable security in Now Assist for CSM and AI agents and agentic workflows by enforcing access control lists \(ACLs\) and user identity-based permissions.

[Yokohama Patch 3](../quality/yokohama-patch-3.md)

-   Analyze your customers' sentiment and sentiment trends in your cases and the reasoning behind it.
-   Use case resolution steps to generate recommended actions based on the data clusters from previously closed cases.
-   Integrate the support for public web content in search queries for both standard and conversational search.
-   Use enhanced AI agents and new standalone AI agents for more specific tasks. For example, the Duplicate identifier AI agent identifies the duplicate interactions and cases from the customers and then consolidates the information.

[Yokohama Patch 1](../quality/yokohama-patch-1.md)

-   Improve agent productivity by managing long-running cases with the Triage cases AI agent.

Yokohama Early Availability

-   Use the Now LLM Service scheduling assistance when booking an appointment through Virtual Agent. You can use this scheduling assistance to schedule, reschedule, or cancel an appointment.
-   Help requesters find solutions by using Genius Results to reduce the number of cases created and decrease the effort needed by agents to close them.
-   Use the Now Assist panel global skill search to ask questions and fetch answers from knowledge articles.

See [Now Assist for Customer Service Management \(CSM\)](https://www.servicenow.com/docs/access?context=now-assist-csm&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Now Assist for Enterprise Architecture \(EA\)

</td><td>

[Yokohama Patch 11](../quality/yokohama-patch-11.md)

-   Review changes to Now Assist usage measurement.
-   Some Now Assist skills, agents, and agentic workflows are on by default.
-   Additional role configuration is required for agentic workflows and AI agents included with Now Assist applications.

Yokohama Patch 1: Generate and summarize Enterprise Modeling and Visualization diagrams for business applications hierarchy, using the Enterprise architecture diagrams AI agent.

Yokohama Early Availability

-   Generate a summary of Architectural Decision Records \(ADR\) in the Enterprise Architecture Workspace.
-   Request a business application or a digital integration using Now Assist in ServiceNow® Virtual Agent.

See [Now Assist for Enterprise Architecture \(EA\)](https://www.servicenow.com/docs/access?context=now-assist-ea&version=yokohama&pubname=yokohama-application-portfolio-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Now Assist for Field Service Management \(FSM\)

</td><td>

[Yokohama Patch 11](../quality/yokohama-patch-11.md)

-   Review changes to Now Assist usage measurement.
-   Some Now Assist skills, agents, and agentic workflows are on by default.
-   Additional role configuration is required for agentic workflows and AI agents included with Now Assist applications.

Yokohama Patch 6

-   Use Google Gemini and Anthropic Claude on AWS as AI model providers for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.
-   Clone and customize skills.
-   Edit prompts using the Now Assist skill kit.

Yokohama Patch 3

-   Enable Field Service technicians to access a virtual assistant from the mobile application with Now Assist in Virtual Agent.

-   Use Now Assist in Virtual Agent for mobile to summarize work order tasks.
-   Explore conversational search in the Now Assist panel with results from Knowledge Base articles.

See Now Assist for Field Service Management \(FSM\) for more information.

</td></tr><tr><td>

Now Assist for Financial Services Operations \(FSO\)

</td><td>

[Yokohama Patch 11](../quality/yokohama-patch-11.md)

-   Now Assist for FSO skills and AI agents support model updates in Now LLM Service.
-   Some Now Assist skills, agents, and agentic workflows are on by default.
-   Review changes to Now Assist usage measurement.
-   Additional role configuration is required for agentic workflows and AI agents included with Now Assist applications.

Yokohama Patch 6

-   Use Google Gemini and Anthropic Claude on AWS as AI model providers for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.
-   Implement security in Now Assist AI agents and Now Assist for FSO skills with Access Control Lists \(ACLs\).

Yokohama Patch 3

-   Streamline the friendly fraud dispute resolution process for human agents and make informed decisions by using the Now Assist friendly fraud AI agent.
-   Maintain positive customer relationships by using the AI agent to craft responses with the right tone and language.
-   Enable agents to evaluate and review the amount being disputed, the customer relationship, and the outcome of the detection logic.

Yokohama Patch 1

-   Streamline the card dispute submission process for cardholders with a dispute intake workflow by using Now Assist in Virtual Agent.
-   Use a conversational, natural language interface that makes data collection more engaging and less tedious compared to a traditional form.
-   Increase efficiency by inferring information from the customer’s responses in the conversation.

See [Now Assist for Financial Services Operations \(FSO\)](https://www.servicenow.com/docs/access?context=now-assist-for-financial-services-operations&version=yokohama&pubname=yokohama-financial-services-operations&ft:locale=en-US) for more information.

</td></tr><tr><td>

Now Assist for HR Service Delivery \(HRSD\)

</td><td>

[Yokohama Patch 11](../quality/yokohama-patch-11.md)

-   Review changes to Now Assist usage measurement.
-   Some Now Assist skills, agents, and agentic workflows are on by default.
-   Additional role configuration is required for agentic workflows and AI agents included with Now Assist applications.

Yokohama Patch 6

-   Use Google Gemini and Anthropic Claude on AWS as AI model providers for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.
-   Create a copy of the KB generation skill to create custom templates.
-   View the list of sources that are used to generate an email reply recommendation.
-   Select citations to view the source articles and industry research from Galileo AI Assistant for HR.
-   Leverage an AI agent to generate a step-wise fulfillment plan for an HR case from both Core UI and Agent Workspace for HR Case Management.
-   Make career conversations easy to create and track using the growth conversations agentic workflow.

Yokohama Patch 3

-   Automate the resolution of routine employee inquiries by using the Resolve noncritical HR cases agentic workflow.
-   Receive research-backed responses to HR management queries that are sourced from both internal knowledge bases and The Josh Bersin content library.
-   Use the new Growth &amp; Performance AI agents to streamline your employee growth discussions in Career Conversations.

Yokohama Patch 1: Improve agent productivity by managing long-running cases with the Triage cases AI agent.

Yokohama Early Availability

-   Use the new Virtual Agent topics to place employee requests in the Human Capital Management \(HCM\) system.
-   Use Knowledge Graph to create personalized knowledge models in the form of Knowledge Graph schemas.
-   Create Journey Accelerator plans by using Now Assist for HRSD in Journey designer.

See [Now Assist for HR Service Delivery \(HRSD\)](https://www.servicenow.com/docs/access?context=now-assist-hrsd&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Now Assist for Hardware Asset Management \(HAM\)

</td><td>

[Yokohama Patch 11](../quality/yokohama-patch-11.md)

-   Review changes to Now Assist usage measurement.
-   Some Now Assist skills, agents, and agentic workflows are on by default.
-   Additional role configuration is required for agentic workflows and AI agents included with Now Assist applications.

Yokohama Patch 6 - Automate the hardware asset repair process by using an agentic workflow and configure Access Control Lists \(ACLs\) for both AI agents and agentic workflows.

Yokohama Patch 4 - Automate and streamline your hardware asset request process by using an agentic workflow.

See [Now Assist for Hardware Asset Management \(HAM\)](https://www.servicenow.com/docs/access?context=now-assist-ham&version=yokohama&pubname=yokohama-it-asset-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Now Assist for IT Operations Management \(ITOM\)

</td><td>

[Yokohama Patch 11](../quality/yokohama-patch-11.md)

-   Review changes to Now Assist usage measurement.
-   Now Assist skills used in the analyze potential impact agentic workflow are turned on by default.
-   Use the new manage alerts autonomously workflow to efficiently manage alerts and minimize resolution times, including an AI agent for triage, impact analysis, and root cause investigation.
-   Additional role configuration is required for agentic workflows and AI agents included with Now Assist applications.

Yokohama Patch 6

-   Get deeper impact analysis in the Analyze alert impact agentic workflow with five new AI agents.
-   Review Alert analysis, and relevant information for new mixed alert groups in the Now Assist panel to help investigate alerts more effectively.
-   Use the Triage and analyze alert agentic workflow to perform initial triage and analysis in the context of an incident.
-   Enhance security for Now Assist AI agents with Access Control Lists \(ACLs\).
-   Use Google Gemini and Anthropic Claude on AWS as AI model providers for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.

Yokohama Patch 3

-   Investigate alerts and get the context that you need to respond efficiently using the Analyze alert impact agentic workflow.
-   Automatically perform initial alert triage and analysis tasks such as assigning alerts, analyzing alert history, and summarizing past incidents, with the Triage and analyze alert agentic workflow.


See [Now Assist for IT Operations Management \(ITOM\)](https://www.servicenow.com/docs/access?context=now-assist-itom&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Now Assist for IT Service Management \(ITSM\)

</td><td>

[Yokohama Patch 11](../quality/yokohama-patch-11.md)

-   Review changes to Now Assist usage measurement.
-   Some Now Assist skills, agents, and agentic workflows are on by default.
-   Additional role configuration is required for agentic workflows and AI agents included with Now Assist applications.
-   Some Now Assist skills are now turned on by default.
-   Add self-service and deflection to your phone channel with Voice AI agents.
-   Edit the incident summarization skill prompts and inputs within the Now Assist Skill Kit.
-   Use the Now Assist context menu \(NACM\) to create AI-powered generative text.
-   Use agentic workflows in Change Management to quickly link configuration items \(CIs\) to a change request, intuitively create change requests, and easily associate outages with a change request.
-   Empower service desk agents to diagnose and resolve incidents on DEX monitored devices quickly and efficiently by using the  DEX issue diagnosis and resolution agentic workflow.

Yokohama Patch 3

-   Identify the category, subcategory, and configuration item for a given incident automatically using a team of AI agents in the Triage and categorize ITSM incidents agentic workflow.
-   Get recommendations to resolve incidents by using a team of AI agents for catalog, knowledge, and past incidents in the Investigate and resolve ITSM incidents agentic workflow.
-   Manage Microsoft 365 group members using AI agents in the Manage Microsoft 365 group members agentic workflow.
-   Generate the **Risk and impact analysis** and the **Justification** fields using the AI agents in the Generate change request plans agentic workflow.

Yokohama Patch 1: Scale your workflows, enhance productivity, and complete work autonomously using the IT Service Management AI agent collection.

Yokohama Early Availability

-   Manage change risk explanations effectively by copying an existing change risk explanation skill and configuring it for your business needs.
-   Deflect IT issues in the ServiceNow portal with AI-powered solutions.
-   Automatically generate an email as a recommendation to help agents save time and learn efficient ways to respond to requesters.
-   View a summary of incidents and change requests in an intuitive summarization interface.
-   Track the status of common IT-related tasks by using the Now Assist application.

See [Now Assist for IT Service Management \(ITSM\)](https://www.servicenow.com/docs/access?context=now-assist-itsm&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Now Assist for Legal Service Delivery \(LSD\)

</td><td>

Yokohama Patch 11

-   Some Now Assist skills are now turned on by default.
-   Additional role configuration is required for agentic workflows and AI agents included with Now Assist applications.

Yokohama Patch 6

-   Use Google Gemini and Anthropic Claude on AWS as AI model providers for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.

See [Explore Now Assist for Legal Service Delivery \(LSD\)](https://www.servicenow.com/docs/access?context=now-assist-lsd-exploring&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Now Assist for Order Management

</td><td>

[Yokohama Patch 11](../quality/yokohama-patch-11.md)

-   Review changes to Now Assist usage measurement.

-   Enable business-to-business \(B2B\) customers to submit order cases autonomously from the Business Portal by simply describing their needs in natural language using the manage order operations agent.
-   Summarize complex orders across products, services, and fulfillment tasks, enabling agents to quickly understand status, take the right actions, and avoid navigating fragmented views to make next steps easier and improving productivity.

See [Now Assist for Order Management](https://www.servicenow.com/docs/access?context=now-assist-order-management&version=yokohama&pubname=yokohama-order-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Now Assist for Sales Force Automation \(SFA\)

</td><td>

[Yokohama Patch 11](../quality/yokohama-patch-11.md)

-   Review changes to Now Assist usage measurement.
-   Some Now Assist skills, agents, and agentic workflows are on by default.
-   Additional role configuration is required for agentic workflows and AI agents included with Now Assist applications.

Previous Patch releases

-   Now Assist for Sales Force Automation \(SFA\) application packages ServiceNow® platform AI capabilities to deliver AI-powered insights and automation to drive faster, smarter sales and order processes.

See [Now Assist for Sales Force Automation \(SFA\)](https://www.servicenow.com/docs/access?context=now-assist-for-sales-and-order-management-som&version=yokohama&pubname=yokohama-order-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Now Assist for Security Incident Response

</td><td>

[Yokohama Patch 11](../quality/yokohama-patch-11.md)

-   Review changes to Now Assist usage measurement.
-   Some Now Assist skills, agents, and agentic workflows are on by default.
-   Additional role configuration is required for agentic workflows and AI agents included with Now Assist applications.
-   Use generative AI to create a quality assessment report of a security incident.

-   Yokohama Patch 6

Help analysts to add security incidents details to the Shift Handover report by chatting with AI agents in the Now Assist panel.

    -   Use Google Gemini and Anthropic Claude on AWS as AI model providers for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.
-   Yokohama Patch 3

Help your analysts to gain insight into security incident record metrics with an agentic workflow. Chat with AI agents in natural language from the Now Assist panel.

Help your analysts to resolve security incidents by chatting with AI agents in the Now Assist panel where the AI agent provides a resolution plan.

-   Yokohama Patch 1

Help your analysts to close security incidents more efficiently by chatting with AI agents in natural language from the Now Assist panel.

-   Yokohama early availability

    -   Triage security incidents with long activity streams by reviewing work notes and contextual information quickly in a concise, easy-to-read format.
    -   Automatically generate resolution notes for security incidents by using generative AI.
    -   Generate recommended actions to resolve security incidents.
    -   Generate a post-incident analysis.
    -   Generate correlation insights to help you connect current incidents to past events. By identifying the affected users, configuration items \(CIs\), or observables \(IP addresses and file hashes\) from existing incidents, you can help to triage new security incidents.
For more information, see [Now Assist for Security Incident Response](https://www.servicenow.com/docs/access?context=now-assist-security-incident-landing&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US).


</td></tr><tr><td>

Now Assist for Software Asset Management \(SAM\)

</td><td>

[Yokohama Patch 11](../quality/yokohama-patch-11.md)

-   Review changes to Now Assist usage measurement.
-   Some Now Assist skills, agents, and agentic workflows are on by default.
-   Additional role configuration is required for agentic workflows and AI agents included with Now Assist applications.
-   Automate user resolution with AI for SaaS license management to support efficiency and accuracy in subscription management.

Yokohama Patch 6

-   Automate and streamline the software asset request process by using an agentic workflow.
-   Automate the process of creating reclamation rules by identifying software products suitable for reclamation using an agentic workflow.
-   Automate evaluation of unused and underutilized software installations for potential reclamation by using an agentic workflow.

Yokohama Patch 3

-   Obtain crucial information on products to mitigate license compliance risks through product summaries on software deployment, license compliance, configuration health, and optimization.
-   Manage product license compliance via recommendations that guide you to take steps to ensure the necessary compliance requirements.

Yokohama Early Availability: Leverage generative AI by using the Now Assist for SAM application to create publisher summaries on software deployment, license compliance, configuration health, and optimization.

See [Now Assist for Software Asset Management \(SAM\)](https://www.servicenow.com/docs/access?context=now-assist-sam&version=yokohama&pubname=yokohama-it-asset-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Now Assist for Source-to-Pay Operations

</td><td>

[Yokohama Patch 11](../quality/yokohama-patch-11.md)

-   Review changes to Now Assist usage measurement.
-   Some Now Assist skills, agents, and agentic workflows are on by default.
-   Additional role configuration is required for agentic workflows and AI agents included with Now Assist applications.

Previous Patch releases

-   Now Assist for Sourcing and Procurement Operations \(SPO\) supports enhanced AI search and the Retrieval-augmented generation \(RAG\) framework to recommend suppliers and products through semantic search and contextual filters, enhancing recommendations with criteria like preferred suppliers and previous purchases.
-   Now Assist for Supplier Lifecycle Operations \(SLO\) supports a conversational intake that helps suppliers to view and update supply information through a conversational flow.
-   Now Assist for Accounts Payable Operations \(APO\) supports a conversational intake to complete self-service tasks, such as submit a request or track a request status.

</td></tr><tr><td>

Now Assist for Strategic Portfolio Management \(SPM\)

</td><td>

[Yokohama Patch 11](../quality/yokohama-patch-11.md)

-   Review changes to Now Assist usage measurement.
-   Some Now Assist skills, agents, and agentic workflows are on by default.
-   Additional role configuration is required for agentic workflows and AI agents included with Now Assist applications.
-   Generate measurable targets from goals information and optional context with the target generation skill.
-   Use the identify similar records skill to find similar demands based on contextual similarity.
-   Enable the project task monitor AI agent to autonomously monitor project tasks on the critical path of a project.
-   Use the **Send preview** button to share a project insights email instantly.

[Yokohama Patch 6](../quality/yokohama-patch-6.md)

-   Use Google Gemini and Anthropic Claude on AWS as AI model providers for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.
-   Use a decorative loader to elevate visual interest during content loading in Strategic Planning.
-   Refine the planning item text descriptions by enabling AI assistance.
-   Use Now Assist for SPM AI agents to help optimize workflows, improve productivity, and automate your tasks.

See [Now Assist for Strategic Portfolio Management \(SPM\)](https://www.servicenow.com/docs/access?context=now-assist-spm&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Now Assist for Telecommunications, Media and Technology \(TMT\)

</td><td>

[Yokohama Patch 11](../quality/yokohama-patch-11.md)

-   Review changes to Now Assist usage measurement.
-   Some Now Assist skills, agents, and agentic workflows are on by default.
-   Additional role configuration is required for agentic workflows and AI agents included with Now Assist applications.
-   Address voice quality issues and validate tickets with RADCOM.
-   Summarize the risk signal and issues records along with respective risk solution and occurrence records.

Yokohama Patch 6

-   Manage and resolve billing inquiry case requests using a team of AI agents.
-   Analyze network incidents, correlate associated cases, and provide resolutions.
-   Summarize Knowledge Graph service details, success initiatives, internal plays, customer plays, and Zoom meeting details.
-   Analyze account health, trigger renewal flows, schedule, and manage touchpoint meetings.
-   Use agentic AI to quickly create consumer registrations.

Yokohama Patch 3

-   Monitor engagement health score and provide a trend analysis.
-   Monitor risks on a predefined schedule and provide common resolutions.

Yokohama Patch 1

-   Proactively identify service problems, diagnose, test, and resolve customer issues autonomously using the Now Assist for TMT AI agent collection.

Yokohama Early Availability

-   Summarize onboarding cases, engagements, and touchpoints by using agentic AI.
-   Enhance test summarization with metric descriptions and contextual notes.
-   Consolidate the information from multiple similar cases into a Knowledge article.
-   Dynamically configure prompts for case summarization.
-   Automate transformation mapping between provider and consumer instances in Service Exchange.

See [Now Assist for Telecommunications, Media and Technology \(TMT\)](https://www.servicenow.com/docs/access?context=now-assist-spmc&version=yokohama&pubname=yokohama-telecom-media-technology&ft:locale=en-US) for more information.

</td></tr><tr><td>

Now Assist for Vulnerability Response

</td><td>

[Yokohama Patch 11](../quality/yokohama-patch-11.md)

-   Review changes to Now Assist usage measurement. See the "Changed in this release" section below.
-   Some Now Assist skills, agents, and agentic workflows are on by default.
-   Additional role configuration is required for agentic workflows and AI agents included with Now Assist applications.
-   Use Now Assist for Vulnerability Response with Security Posture Control to help you with [Creating an API connector in the Security Posture Control workspace](https://www.servicenow.com/docs/access?context=using-now-assist-api-connector&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US).

-   [Yokohama Patch 6](../quality/yokohama-patch-6.md)

Help your analysts identify duplicate host vulnerable items and analyze available remediation options with generative AI skills with Now Assist for Vulnerability Response.

    -   Use Google Gemini and Anthropic Claude on AWS as AI model providers for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.
See [Now Assist for Vulnerability Response](https://www.servicenow.com/docs/access?context=now-assist-for-vulnerability-response-landing&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US) for more information.


</td></tr><tr><td>

Now Assist for Workplace Service Delivery \(WSD\)

</td><td>

[Yokohama Patch 11](../quality/yokohama-patch-11.md)

-   Review changes to Now Assist usage measurement.
-   Some Now Assist skills, agents, and agentic workflows are on by default.
-   Additional role configuration is required for agentic workflows and AI agents included with Now Assist applications.

Yokohama Patch 6

-   Help map admins configure the map during bulk updates to Indoor Mapping using the Automate map updates AI agentic workflow.
-   Optimize a maintenance case based on the space utilization rate of the location where a maintenance case is created using the Optimize cleaning activities AI agentic workflow.

Yokohama Patch 3

-   Manage temporary space closures AI agentic workflow for emergency meeting room maintenance. This team of AI agents block a space for maintenance and move any existing reservations from the blocked room to a new location.
-   Help manage workplace reservations for updating existing event planning reservations. This team of AI agents retrieve the reservation from workplace case details, analyze the reservation, and update the workplace case notes.

See [Now Assist for Workplace Service Delivery \(WSD\)](https://www.servicenow.com/docs/access?context=now-assist-wsd-landing&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Now Assist in AI Search

</td><td>

[Yokohama Patch 11](../quality/yokohama-patch-11.md)

-   Review changes to Now Assist usage measurement.
-   Some Now Assist skills, agents, and agentic workflows are on by default.
-   Additional role configuration is required for agentic workflows and AI agents included with Now Assist applications.
-   Simplify setup with automatic activation of Now Assist Multi-Content Response Genius Results for search profiles when you use Guided Setup to activate the Now Assist panel.
-   Increase search precision and contextual relevance for knowledge article, Catalog Item, external content, and topic retrieval searches with hybrid search.
-   Improve the enhanced chat experience by configuring the system to use AI Search as the source for Ask Now Assist suggestions.
-   Provide more focused auto-complete suggestions for enhanced chat that honor the search user's domain restriction and the exclusion list for unwanted suggestions.

[Yokohama Patch 6](../quality/yokohama-patch-6.md)

-   Use Google Gemini and Anthropic Claude on AWS as AI model providers for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.
-   Increase search recall with semantic indexing of Catalog Item short descriptions.

[Yokohama Patch 3](../quality/yokohama-patch-3.md)

-   Prompt users to log in to Microsoft SharePoint Online as needed to see files shared with them when viewing Knowledge Graph user citations in Now Assist Multi-Content Response Genius Result answers.

Yokohama Early Availability

-   Improve incident deflection for portal users by configuring record producers to display actionable and relevant Genius Results suggestions during submission of cases, incidents, problems, and similar tasks.

See [Now Assist in AI Search](https://www.servicenow.com/docs/access?context=now-assist-ais&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US) for more information.

</td></tr><tr><td>

Now Assist in Contract Management

</td><td>

[Yokohama Patch 11](../quality/yokohama-patch-11.md)

-   Review changes to Now Assist usage measurement.
-   Some Now Assist skills are now turned on by default.
-   Use AI-powered obligation extraction to automatically identify and capture key obligations from signed contracts, and then review, edit, approve, or reject them within the contract playbook to create obligation records automatically.
-   Activate the Contract obligation extraction skill in the Now Assist Admin console to enable automatic obligation extraction.
-   Use Now Assist powered conversational search to query contract documents using natural language and dialogue-driven queries, making it easier to find relevant information.
-   Additional role configuration is required for agentic workflows and AI agents included with Now Assist applications.

Yokohama Patch 6

-   Use the contract playbook to review and update the AI extracted metadata and reminder date for contract renewal or termination.
-   Use Google Gemini and Anthropic Claude on AWS as AI model providers for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.

Yokohama Patch 3

-   Activate and configure the contract metadata extraction skill for Contract Management Pro in the Now Assist Admin console.
-   Activate and configure the contract analysis skill for Contract Management Pro in the Now Assist Admin console.
-   Use the Manage contract repository agentic workflow to autonomously set milestone reminders for the notice period of contract renewals or the notice period for termination of contract renewals.

See [Now Assist in Contract Management](https://www.servicenow.com/docs/access?context=cncore-now-assit-landing&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Now Assist in Document Intelligence

</td><td>

Yokohama Patch 13

-   Now Assist in Document Intelligence skills are on by default.

[Yokohama Patch 11](../quality/yokohama-patch-11.md)

-   Review changes to Now Assist usage measurement.
-   Some Now Assist skills, agents, and agentic workflows are on by default.
-   Additional role configuration is required for agentic workflows and AI agents included with Now Assist applications.

[Yokohama Patch 6](../quality/yokohama-patch-6.md)

-   Summarize the content in document and image attachments with the document and visual insights AI agent.
-   Choose a large language model \(LLM\) to generate predictions for extraction and Q&amp;A \(question &amp; answer\) use cases.
-   Use Google Gemini and Anthropic Claude on AWS as AI model providers for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.

[Yokohama Patch 3](../quality/yokohama-patch-3.md)

-   Boost productivity by using the document and visual insights AI agent to autonomously analyze and extract data from documents and images.
-   Streamline document data extraction by automating document tasks.
-   Use Virtual Agent to ask questions about the document content.
-   Extract the data from invoices with Now Assist for Accounts Payable Operations \(APO\).

[Early Availability](../quality/yokohama-all-other-fixes.md)

-   Speed up your document processing workflows and quickly extract the text and tables from your documents.
-   Save time looking for the information that you need in a document, and quickly find the answers to predefined questions.

See [Now Assist in Document Intelligence](https://www.servicenow.com/docs/access?context=docintel-nowassist-landing&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US) for more information.

</td></tr><tr><td>

Now Assist in Platform Analytics

</td><td>

[Yokohama Patch 11](../quality/yokohama-patch-11.md)

-   Review changes to Now Assist usage measurement.
-   Some Now Assist skills, agents, and agentic workflows are on by default.
-   Additional role configuration is required for agentic workflows and AI agents included with Now Assist applications.
-   Create "explorations"—editable documents where you analyze data with the help of AI. Refine responses, add your own input, and collaborate with others to make data-informed decisions faster.

Previous Patch releases

-   Generate and export Platform Analytics artifacts from conversational interactions in the Now Assist panel.
-   Benefit from a single, smooth experience in asking questions across all Now Assist for Platform Analytics skills, as well as other applications that incorporate Platform Analytics and AI, through a shared backend.

See [Now Assist in Platform Analytics](https://www.servicenow.com/docs/access?context=now-assist-in-platform-analytics&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US) for more information.

</td></tr><tr><td>

Now Assist in Virtual Agent

</td><td>

[Yokohama Patch 11](../quality/yokohama-patch-11.md)

-   Review changes to Now Assist usage measurement.
-   Some Now Assist skills, agents, and agentic workflows are on by default.
-   Create and manage LLM-based chat and voice assistants within Assistant Designer, a centralized assistant administrator experience.
-   View a people citation's org chart in the interactive view. The interactive view opens to the right of the chat conversation area.
-   Notice several UI improvements to enhanced chat and enhanced chat's full-page experience, including an updated input bar, gradient borders, copy message icon for received messages, and more.
-   Enable voice input to allow users to use a microphone to type the input. Voice input is only available for Now Assist panel Platform assistant.

[Yokohama Patch 6](../quality/yokohama-patch-6.md)

-   Use Google Gemini and Anthropic Claude on AWS as AI model providers for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.
-   Use agentic conversations and view agentic conversational processing flow steps.
-   View extended entities and records in standard and enhanced chat conversations if they’re associated with the Knowledge Graph natural language query \(NLQ\) schema.
-   View suggested search queries previously performed in the portal's search bar within enhanced chat conversations.
-   Work with the simplified subheader of enhanced chat.
-   Delete closed enhanced chat conversations.
-   Expand the fallback options.
-   Enter into web search mode manually via the input bar.

[Yokohama Patch 3](../quality/yokohama-patch-3.md)

-   Use enhanced chat to provide users with a conversational experience within a resizable and movable chat window that includes the ability to have multiple active conversations. Enhanced chat enables users to choose their way of engaging with Now Assist on their ServiceNow portals from a variety of entry points. Enhanced chat includes synthesized responses after entering a search query into a portal's search bar. If Now Assist in AI Search is turned on, enhanced chat also offers an optional full-page experience where your users can enter into a full-page chat experience after entering a search query into a portal's search bar. Enhanced chat also offers an updated, modern look and feel along with chat controls to resize and move the chat window.
-   View an expanded list of inline citations for both standard and enhanced chat. New inline citations for external content and people searches are available.
-   View and work with suggested actions after completing an action in Now Assist in Virtual Agent.
-   Stream responses for Now Assist LLM - enhanced chat conversations.
-   Upload or drag documents and images into a standard or enhanced chat.
-   Automatically switch to the user's detected language in enhanced chat conversations when language detection is turned on.
-   Use the Web Search custom skill to search for an answer on the internet.

[Yokohama Patch 1](../quality/yokohama-patch-1.md)

-   Stream responses for Now Assist LLM chat conversations.

See [Now Assist in Virtual Agent](https://www.servicenow.com/docs/access?context=now-assist-in-va-landing&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US) for more information.

</td></tr><tr><td>

Now Mobile

</td><td>

Get personalized search results with the Now Assist genius results search functionality in Now Mobile®.

See [Now Mobile app](https://www.servicenow.com/docs/access?context=mobile-employee-experience&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

On-Call Scheduling

</td><td>

Control whether an on-call schedule or shift record link in all major on-call email notifications redirects you to Service Operations Workspace \(SOW\) or to the classic UI16 interface in On-Call Scheduling.

See [On-Call Scheduling](https://www.servicenow.com/docs/access?context=c_OnCallScheduling&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Operational Resilience

</td><td>

-   Align with the CSDM model to set up configurable main node configurations, which are used to retrieve CSDM and their dependency data.
-   Add the primary origin to an operational vulnerability, and the impacted areas are automatically included. The vulnerability can then be viewed from any impacted area.
-   All CSDM objects, dependencies, and their red flags can be rolled up based on the entity hierarchy.
-   Use Smart Assessment for evaluating an Operational vulnerability.

See [Operational Resilience](https://www.servicenow.com/docs/access?context=grc-opres-landing-page&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US) for more information.

</td></tr><tr><td>

Operational Sustainability Management

</td><td>

-   Model and prepare for potential outcomes with what-if scenario analysis tools that can help with your strategic planning.
-   Review the calculated metric definition data by using a formula tree so that you can access detailed information on the operands, metric definitions, metrics, and emission factors.
-   Streamline ESG metric tracking and enable trend analysis with enhanced Metric data tasks that support choice and HTML response formats and table improvements.
-   Import your historical metric data by using an import template to update and manage metric data within your organization.
-   Assign data owners dynamically for metrics that are based on configurations.

See [Operational Sustainability Management \(formerly Environmental, Social, and Governance\)](https://www.servicenow.com/docs/access?context=esg-landing-page&version=yokohama&pubname=yokohama-environmental-social-governance&ft:locale=en-US) for more information.

</td></tr><tr><td>

Operational Technology \(OT\) Manager Foundation

</td><td>

[Yokohama Patch 11](../quality/yokohama-patch-11.md)

-   Review changes to Now Assist usage measurement.
-   Some Now Assist skills, agents, and agentic workflows are on by default.
-   Additional role configuration is required for agentic workflows and AI agents included with Now Assist applications.

[Yokohama Patch 10](../quality/yokohama-patch-10.md)

-   Find OT Configuration Management Database \(CMDB\) records more quickly by using the OT CMDB search function.
-   Simplify the upload, validation, and import of your OT device data by using the Import OT device spreadsheet into OT CMDB agentic workflow.

See [Now Assist for Operational Technology Manager \(OTM\)](https://www.servicenow.com/docs/access?context=now-assist-for-otm-landing&version=yokohama&pubname=yokohama-operational-technology&ft:locale=en-US) for more information.

</td></tr><tr><td>

Operational Technology Change Management

</td><td>

In an OT change request record in the Industrial Workspace, use new related lists to create an OT incident record related to the OT change request, or link an existing OT incident record to the OT change request.

See [Operational Technology Change Management](https://www.servicenow.com/docs/access?context=operational-technology-change-management-landing-page&version=yokohama&pubname=yokohama-operational-technology&ft:locale=en-US) for more information.

</td></tr><tr><td>

Operational Technology Incident Management

</td><td>

Relate an OT incident to an OT change request by creating the incident from the change record in the Industrial Workspace.

See [Operational Technology Incident Management](https://www.servicenow.com/docs/access?context=operational-technology-incident-management-landing-page&version=yokohama&pubname=yokohama-operational-technology&ft:locale=en-US) for more information.

</td></tr><tr><td>

Operational Technology Manager

</td><td>

-   View the Operational Technology Manager \(OT\) device-to-device connections with additional information such as port and protocol values.
-   Review the OT applications and versions that you have installed on the About Industrial Workspace page.
-   Keep your OT device data updated by using the Configuration Management Database \(CMDB\) OT class model updates and UI enhancements.
-   Track your OT device data with the new Operational Technology Visibility dashboard.
-   Group OT devices using CMDB groups to support non-CMDB tables that must be converted from IT to OT.
-   Keep your OT device data updated by using the Configuration Management Database \(CMDB\) OT class model updates and UI enhancements.
-   Improve the processes for importing and classifying your OT device data with updates and UI enhancements for the Pre-import OT Worksheet Entry Review \(POWER\) tool.

See [Operational Technology Manager](https://www.servicenow.com/docs/access?context=operational-technology-manager&version=yokohama&pubname=yokohama-operational-technology&ft:locale=en-US) for more information.

</td></tr><tr><td>

Operational Technology Vulnerability Response

</td><td>

-   Configure Operational Technology Vulnerability Response from the Security Exposure Management Workspace \(SEM Workspace\).
-   Access the Operational Technology Vulnerability Response Risk Calculator plugin directly without loading the demo data.
-   View all vulnerable items that have been created from the OT Vulnerable Items list in the Industrial Workspace.
-   View all remediation tasks that have been created from the OT Remediation Tasks list in the Industrial Workspace.
-   View all vulnerability exceptions that have been created from the OT Vulnerability Exception Approvals list in the Industrial Workspace.
-   Hardware Vulnerability Assessment is available for firmware discovery models without normalized data.
-   Assess the vulnerabilities for the firmware of the OT assets with Hardware Vulnerability Assessment.
-   View solutions or details of a vulnerable item \(VIT\) with enhanced UI options.
-   Manage your vulnerable items and Operational Technology Vulnerability Response data with the enhanced OTVR \(PA\) dashboard in the Industrial Workspace.
-   View the risk score of your OT devices at each level of the equipment model with the OT Vulnerability Risk Rollup dashboard.

See [Operational Technology Vulnerability Response](https://www.servicenow.com/docs/access?context=oper-tech-vulnerability-response-landing-page&version=yokohama&pubname=yokohama-operational-technology&ft:locale=en-US) for more information.

</td></tr><tr><td>

Opportunity Management

</td><td>

1.  Enable customers to view the roll-up amount in the Kanban View.
2.  Enable sales representatives to customize bundled products and products with complex characteristics in the product catalog.

See [Opportunity Management](https://www.servicenow.com/docs/access?context=opportunity-management&version=yokohama&pubname=yokohama-order-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Opportunity Marketplace

</td><td>

-   Opportunity owners can select multiple user criteria when creating opportunities.
-   Import an opportunity from the ServiceNow Project Workspace. Importing a project from the Project Workspace is only available with the Project type opportunity.

See [Opportunity Marketplace overview](https://www.servicenow.com/docs/access?context=egd-opportunity-marketplace-ovrvw&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Order Management

</td><td>

-   Enable order agents to view price adjustment details while processing orders.
-   Enable customers to view the product catalog, add products to a shopping cart, and create orders by using the Business Portal.
-   Create cases for multiple orders or for specific order lines using the Business Portal.
-   Create cases for multiple invoices or for specific invoice lines.
-   Provide metrics that help sales agents and sales managers track and analyze the revenue impact of subscriptions.

See [Order Management](https://www.servicenow.com/docs/access?context=order-mgt-exploring&version=yokohama&pubname=yokohama-order-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Password Reset

</td><td>

-   Enhanced security for all client-callable script includes by switching off the sandbox mode.
-   Enhanced security access for Password Reset tables.

See [Password Reset](https://www.servicenow.com/docs/access?context=password-reset-landing-page&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US) for more information.

</td></tr><tr><td>

Performance Analytics

</td><td>

-   Track critical process metrics and trends.
-   Measure process health and behavior against organizational targets.
-   Identify process patterns and potential bottlenecks before they occur.
-   Continually visualize historical and real-time process statistics in role-based dashboards. The dashboards enable individual stakeholders to make informed decisions.

See [Performance Analytics \(Indicator data sources\)](https://www.servicenow.com/docs/access?context=pa-overview&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US) for more information.

</td></tr><tr><td>

Platform Analytics experience

</td><td>

-   Effortlessly create bold, meaningful data graphics by and refining the results in an AI-powered conversational interface.
-   Speed up the process of turning insights into actions with dynamic new features like suggested performance targets and more powerful data filtering.
-   Share data insights more broadly with enhanced Microsoft PowerPoint support.

See [Platform Analytics experience](https://www.servicenow.com/docs/access?context=par-workspace&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US) for more information.

</td></tr><tr><td>

Playbooks in Workflow Studio

</td><td>

-   Add custom translations for playbooks.
-   Restart playbook activities that have ended in error.
-   Create a checklist directly in the side panel without needing a checklist template.
-   Generate a playbook via API in other ServiceNow applications such as IT Operations Management \(ITOM\).
-   Generate playbooks from inputs that refer to active actions, flows, subflows, content from installed spokes, or activity definitions.

See [Exploring playbooks](https://www.servicenow.com/docs/access?context=process-automation-designer&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US) for more information.

</td></tr><tr><td>

Policy and Compliance Management

</td><td>

-   View the compliance score at the entity level based on the hierarchy of entities.
-   Eliminate duplicate citations associated with the authority documents when you download UCF content.
-   Revise your policies and update the policy text periodically by integrating with Microsoft SharePoint.
-   Enable policy owners and reviewers to collaborate, review, and redline policies by using policy authoring and the redlining feature.
-   The Issues widget has been removed from the Compliance Workspace landing page to enhance the performance.
-   Enable data access by implementing Entity-Based Access controls.
-   Recommend similar control objectives using generative AI. You can then retain, dismiss, or merge duplicate control objectives.

See [Policy and Compliance Management](https://www.servicenow.com/docs/access?context=r_PolicyComplianceMgmt&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US) for more information.

</td></tr><tr><td>

Portfolio Planning

</td><td>

-   View the rolled-up financial costs and benefits data of your planning items in the new **Financials** tab in the Planning page.
-   View the financial data of planning items while creating multiple prioritization scenarios to promote efficient use of budget and help increase the return on investment \(ROI\).
-   Monitor performance, track progress, and make informed decisions related to planning and execution using dashboards.
-   Create, edit, and switch views in portfolio plans and free-form roadmaps with display preferences.

See [Portfolio Planning](https://www.servicenow.com/docs/access?context=portfolio-planning-app-landing-page&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Predictive Intelligence

</td><td>

-   Learn which classes contribute the most to your model's predictions by adding Model Explainability to Workflow Classification solutions.
-   ITSM Predictive Intelligence Workbench is deprecated in the Yokohama release.
-   New advanced options for classification solutions are available from Yokohama Patch 4.

See [Predictive Intelligence](https://www.servicenow.com/docs/access?context=predictive-intelligence-landing&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US) for more information.

</td></tr><tr><td>

Privacy Management

</td><td>

-   Integrate criticality factors into assessments and processing activities thereby simplifying the assessment process, and reducing the workload for privacy teams.
-   Use the Smart Assessment Engine to capture details regarding information objects and hierarchies, updating all details within the assessments and eliminating the need to separately update processing activities.
-   Implement information Object \(IO\) categories such as biometric data, to align with regulatory classifications and bridge the gap between requirements and user understanding.
-   Empower privacy case analysts to perform assessments on privacy cases using the Smart Assessment Engine

See [Privacy Management](https://www.servicenow.com/docs/access?context=privacy-management&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US) for more information.

</td></tr><tr><td>

Problem Management

</td><td>

-   Increase operational efficiency of tier 1 service desk agents with the dedicated sn\_service\_desk\_agent role.
-   Simplify the management of problems and problem tasks using Problem Management models.

See [Problem Management](https://www.servicenow.com/docs/access?context=c_ProblemManagement&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Process Mining

</td><td>

-   Now Assist based work notes analysis
-   Process configuration builder introduced
-   Content pack importer introduced for process configurations
-   Process Mining evaluation project available for HR and CSM
-   Access control \(ACL\) rules updated

See [Process Mining](https://www.servicenow.com/docs/access?context=process-mining&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US) for more information.

</td></tr><tr><td>

Product Catalog Management and Pricing Management

</td><td>

-   Enable agents to create multiple configurations of child product offerings in configurable products and customize the options and characteristics for each child product instance.
-   Identify single-use product offerings, such as installation services, with a transient flag to differentiate them from products that are maintained as active sold products or product inventory.
-   Provide the options to choose a drop-down or radio control to display characteristics of type choice in the product configurator UI.
-   Give sales agents a list of recommended product offerings that can be added to complement or supplement products in quotes.
-   Enable pricing admins to set pricing adjustments based on the quantity of product offerings in a quote or order.

See [Product Catalog Management](https://www.servicenow.com/docs/access?context=product-catalog-managment&version=yokohama&pubname=yokohama-order-management&ft:locale=en-US) and [Pricing Management](https://www.servicenow.com/docs/access?context=pricing-management&version=yokohama&pubname=yokohama-order-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Project Portfolio Management

</td><td>

-   Move your old status reports to a new tool to maintain a consistent reporting process.
-   Secure your projects with confidentiality settings to safeguard all confidential data.
-   Build a checklist for your project tasks to track the task activities for completion.
-   Inline edit one or more cells in child resource assignments.
-   Explore the new heatmap modal to monitor resource status, available capacity, and utilization efforts.
-   Identify similar demand records based on contextual similarity in the name, description, and business case content using the identify similar records Now Assist skill.

For more information, see the [Project Workspace release notes](../it-business-management/project-workspace-rn.md).

</td></tr><tr><td>

Project Workspace

</td><td>

-   Import your old status reports to a new status report tool and optimize your reporting process.
-   Create a checklist in a project task to track items that must be completed in the task.
-   Inline edit one or more cells in child resource assignments.
-   Explore the heatmap modal to monitor resource status, available capacity, and utilization efforts.

See [Project Workspace](https://www.servicenow.com/docs/access?context=project-workspace-landing-page&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Public Sector Digital Services

</td><td>

-   Review requests for grants, and create new grant programs using Grants Management.
-   Connect multiple ServiceNow instances to provide seamless support and service experiences across the Public Sector​ using for Service Bridge for Public Sector Digital Services.
-   Utilize the Chat summarization skill, powered by Now LLM Service, to auto-generate chat summaries for customer-agent interactions in the Now Assist for Public Sector Digital Services \(PSDS\) application.

See [Public Sector Digital Services](https://www.servicenow.com/docs/access?context=bun-public-sector-landing-page&version=yokohama&pubname=yokohama-government-industry&ft:locale=en-US) for more information.

</td></tr><tr><td>

Quote Management

</td><td>

-   Enable agents to manage sales agreements in quotes.
-   Enable agents to view the price adjustments that are applied to the base and list price of a product in a quote.
-   Enable agents to create PDF documents from a quote using the ServiceNow PDF generator.
-   Use the hierarchical list view to view parent and child relationships within quote lines.
-   Provide agents with offer recommendations to upsell or cross-sell products that complement products in quotes.

See [Quote Management](https://www.servicenow.com/docs/access?context=quote-management&version=yokohama&pubname=yokohama-order-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

RPA Hub

</td><td>

-   Use generative AI to create and edit automations, activities, and extend automation logic flow through text instructions and preview options in the RPA Desktop Design Studio.
-   Run multiple unattended robots on different user sessions at the same time on the same Windows Server machine using the high-density robots feature.
-   Use new sample automations that were added in the RPA Desktop Design Studio that cater to different use cases.
-   Leverage the communication capabilities of the SSH protocol in the automation processes with the new Secure Shell \(SSH\) connector in the RPA Desktop Design Studio.
-   Use the SAP connector to identify the screens and elements and to automate workflows on SAP graphical user interfaces \(GUI\).
-   Use Google Gemini and Anthropic Claude on AWS as AI model providers for RPA bot generation skill in addition to Now LLM Service and Azure OpenAI.
-   Enhanced access controls for RPA bot generation skill.

See [Robotic Process Automation \(RPA\) Hub](https://www.servicenow.com/docs/access?context=rpa-main-landing-page&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US) for more information.

</td></tr><tr><td>

Recommended Actions for Operational Technology Service Management \(OTSM\)

</td><td>

Display relevant actions to users based on the context of an OT incident record.

See [Recommended Actions for Operational Technology Service Management \(OTSM\)](https://www.servicenow.com/docs/access?context=recommended-actions-for-otsm&version=yokohama&pubname=yokohama-operational-technology&ft:locale=en-US) for more information.

</td></tr><tr><td>

Regulatory Change Management

</td><td>

-   Summarize a regulatory alert by using the Now Assist summarization skill.
-   Use Regulatory mapping with AI to help organizations identify, track, and manage regulatory requirements that are specific to their industry.
-   Set up a recommendation context.
-   Analyze the potential impacts of a new regulation to assess whether it's likely to achieve the required business or regulatory compliance objectives.

[Yokohama Patch 11](../quality/yokohama-patch-11.md)

-   Some Now Assist skills are now turned on by default.
-   Review changes to Now Assist usage measurements.

See [Regulatory Change Management](https://www.servicenow.com/docs/access?context=reg-change-mgmt-landing-page&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US) for more information.

</td></tr><tr><td>

Request Management

</td><td>

-   Improve customer satisfaction and operational efficiency with the sn\_service\_desk\_agent role, which is dedicated to the tier 1 service desk agents.
-   Restrict unauthorized access to the Request Management tables using deny ACLs.
-   Quickly determine whether a configuration item \(CI\) is available to be added to the **Configuration item** field in the Requested item form by searching the an alphabetized list of available CIs rather than having to first find the CI class list.

See [Request Management](https://www.servicenow.com/docs/access?context=c_RequestManagement&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Resource Management Workspace

</td><td>

-   Access the new heatmap modal to view the resource status, remaining capacity, and utilization efforts of resource allocation.
-   Use the **Name**, **Notes**, and **Ready for review** fields while creating a New Resource Assignment.
-   Access the resource assignments and the parent resource assignment from the resource board.
-   Use the interactive dashboard to create and manage widgets to access the required set of resource data in board view.
-   Extend, adjust, and approve resource assignments using the row context menu from the side grid.

See [Resource Management Workspace](https://www.servicenow.com/docs/access?context=using-rmw&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Retail Core

</td><td>

Use the Retail Portal for an optimized and streamlined portal experience within your retail organization.

See [Retail](https://www.servicenow.com/docs/access?context=rahi-retail-operations-overview&version=yokohama&pubname=yokohama-retail-industry&ft:locale=en-US) for more information.

</td></tr><tr><td>

Retail Task Management Core

</td><td>

-   Assign work from HQ to multiple retail locations at once with the multi-store case generator.
-   View assigned tasks in the retail portal alongside other requests.
-   Track completion status across multiple locations assigned the same item.

See [Retail Task Management](https://www.servicenow.com/docs/access?context=rahi-retail-task-management-overview&version=yokohama&pubname=yokohama-retail-industry&ft:locale=en-US) for more information.

</td></tr><tr><td>

Sales Agreement Management

</td><td>

-   REST APIs enable customers to synchronize sales agreements with external systems.
-   Monitor the progress of sales agreement creation from quotes.

See [Sales Agreement Management](https://www.servicenow.com/docs/access?context=sales-agreement-mgmt&version=yokohama&pubname=yokohama-order-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Sales Forecasting

</td><td>

-   Project future sales and revenue with intuitive forecasting by sales representatives.
-   Access the Sales Forecast dashboard at all levels of the sales hierarchy.
-   Set and manage sales quotas for individual representatives and sales teams.
-   Track sales quota targets and their progress for individuals and sales teams across the hierarchy.

See [Sales Forecasting](https://www.servicenow.com/docs/access?context=sales-forecasting&version=yokohama&pubname=yokohama-order-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Security Incident Response

</td><td>

-   Identify inefficiencies and optimize the resolution process of security incidents for faster closure by using Process MIning.
-   Implemented CrowdStrike Next-Gen SIEM integration enabling real-time ingestion of correlated detections, and enrichment data.
-   Enhanced Splunk ES integrations to improve incident classification and enable efficient retrieval of historical data and alerts.
-   Include the number of VITs indirectly associated with a CVE through TPEs.
-   Help managers ensure there are no gaps in coverage and analysts are always available to address security incidents by configuring shifts for analysts.
-   Define default child nodes to populate in the relationship graph, and add or remove child nodes at the parent node level.

See [Security Incident Response](https://www.servicenow.com/docs/access?context=sir-landing-page&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Security Posture Control

</td><td>

-   Create and publish your own API connectors with a step-by-step process in the Connector builder module in the Security Posture Control workspace. You can use generative AI to automate some steps. See the [Now Assist for Security Incident Response release notes](../security-operations/secops-now-assist-security-operations-rn.md) for more information about the Now Assist skill.
-   Get insights into your overall security posture and configuration gaps in your security tools using new policies and asset proﬁles that are included with the Security Posture Control application.
-   Use the policies included with the application or custom policies that you create to monitor your assets for overall security tool coverage, compliance with internal configuration standards, critical combinations of security gaps and vulnerabilities, and possible internet exposure.

See [Security Posture Control](https://www.servicenow.com/docs/access?context=spc-landing&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Self-service and omnichannel engagement for CSM

</td><td>

-   Integrate with contact centers using Contact Center Integration Core to import data from a third party contact center as a service \(CCaaS\) application.
-   Better integrate with contact centers by adding call controls to Agent Workspace with Interaction Controls Component \(ICC\).
-   Enhance B2B customer support through ServiceNow® self-service capabilities with the new Business Portal.
-   Provide a consistent experience for agents handling omnichannel interactions through email interactions, which preserve the context for agents by associating the email conversation between the agent and the customer.
-   Improve contact center efficiency by helping avoid the creation of duplicate cases through the use of the Email as an Interaction feature.

See [Omnichannels for communicating with customers](https://www.servicenow.com/docs/access?context=omnichannels-communicating-customers&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US), [Self-service for Customer Service Management](https://www.servicenow.com/docs/access?context=self-service-options-csm-customers&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US), and [Playbooks for Portals](https://www.servicenow.com/docs/access?context=playbooks-for-portals&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Service Catalog

</td><td>

-   Enable your users to experience the flexibility of using supported languages when creating or editing catalog items in Catalog Builder.
-   Identify and resolve accessibility-related issues during catalog item generation through a new accessibility checker button in the TinyMCE toolbar in Service Catalog.

See [Service Catalog](https://www.servicenow.com/docs/access?context=service-catalog&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US) for more information.

</td></tr><tr><td>

Service Exchange

</td><td>

-   Providers can now include client and UI policy scripts in remote record producers, which consumers can review and approve.
-   Providers can now copy local catalog items to Service Exchange as remote record producers either in bulk or individually.
-   Providers can simplify and streamline choice-based transform mapping with ServiceNow Now Assist.
-   Consumers can now add variables to remote record producers for use in consumer pre-flows.

See [Service Exchange](https://www.servicenow.com/docs/access?context=tmt-service-bridge-both-landing-page&version=yokohama&pubname=yokohama-service-bridge&ft:locale=en-US) for more information.

</td></tr><tr><td>

Service Graph Connector Integration for Claroty CTD

</td><td>

-   View the class mappings available for the Service Graph Connector using the new Class Mappings menu
-   Filter out empty rack slots to help avoid importing blank rack slots into the ServiceNow. Configuration Management Database \(CMDB\).
-   Use the Firmware Installation \[cmdb\_firmware\_install\] table to capture the firmware version.
-   Avoid OT entity update issues by using the new ire\_criterion\_attribute attribute on the OT Entity \[cmdb\_ot\_entity\] table.
-   Clean the serial record entries from the Source \[sys\_object\_source\] table using a fix script.

See [Service Graph Connector Integration for Claroty CTD](https://www.servicenow.com/docs/access?context=sgc-cmdb-integration-claroty-ctd&version=yokohama&pubname=yokohama-operational-technology&ft:locale=en-US) for more information.

</td></tr><tr><td>

Service Graph Connector for Microsoft Defender for IoT \(Azure\)

</td><td>

-   View the class mappings available for the Service Graph Connector using the new Class Mappings menu
-   Use the Firmware Installation \[cmdb\_firmware\_install\] table to capture the firmware version.
-   Avoid OT entity update issues by using the new **ire\_criterion\_attribute** attribute on the OT Entity \[cmdb\_ot\_entity\] table.
-   Extend capabilities of the Service Graph Connector to import devices actively scanned by Microsoft Defender for IoT.
-   Ingest actively scanned devices from Microsoft Defender for IoT and assign them to a site in your ServiceNow instance automatically using the **Site Map** table.

See [Service Graph Connector for Microsoft Defender for IoT \(Azure\)](https://www.servicenow.com/docs/access?context=integration-sgc-microsoft-defender-iot-azure&version=yokohama&pubname=yokohama-operational-technology&ft:locale=en-US) for more information.

</td></tr><tr><td>

Service Level Management

</td><td>

Use Workflow Studio to build and automate the workflows for Service Level Management.

See [Service Level Management](https://www.servicenow.com/docs/access?context=service-level-mgmt-landing-page&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Service Observability

</td><td>

-   Connect operators with subject matter experts \(SMEs\) using critical signals from existing monitoring tools and the ServiceNow platform.
-   Centralize critical signals and bridge workflows to help increase agility and reliability.
-   Calculate the blast radius and help reduce mean time to resolution \(MTTR\) by viewing changes to your application and the underlying infrastructure.

See [Service Observability](https://www.servicenow.com/docs/access?context=service-observability&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Service Operations Workspace for ITSM

</td><td>

-   Streamline task management and reduce response times by approving the request, request item, catalog task, change request, and standard change proposal records directly from Service Operations Workspace \(SOW\).
-   Quickly find details helpful in resolving issues by using Recommended Actions and AI Search for request items and catalog items.
-   Enable agents with incident write access, callers, and end users who opened the incident to reopen a resolved incident from the incident record page in Service Operations Workspace.
-   Configure response templates and incident management properties from the Service Operations Workspace Admin Center.
-   Configure and use DEX Desktop Assistant as a channel in all incident and major incident-related communications.
-   Starting in version 7.1, you can do the following:
    -   Restrict unauthorized access to Incident Management in Service Operations Workspace using deny ACLs.
    -   Compose email using GenAI email templates for all major incident communications.
    -   Close a resolved incident with itil\_admin user role.
    -   Share the workaround for a problem and deflect additional incidents.
    -   Configure the On-Call Scheduling features from Service Operations Workspace Admin Center.
    -   Use visual indicators like colors and icons on chat session tabs to notify agents about unread messages to maintain the SLA for the chats in Service Operations Workspace.
    -   Configure the provider for Notify in SOW.
    -   Agents can see a transcript of voice calls while interacting with customers in Service Operations Workspace.
    -   Create Change Advisory Board \(CAB\) meetings and run them through CAB Workbench in Service Operations Workspace.

See [Service Operations Workspace for ITSM](https://www.servicenow.com/docs/access?context=sow-landing-page&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Service Portal

</td><td>

-   Analyze the performance of portal pages and their widgets.
-   Compare cloned widgets with the base widget from which they were cloned.
-   Use ECMAScript 2021 \(ES12\) JavaScript mode in widget server scripts.
-   Enable early single sign-on \(SSO\) redirection.
-   Specify the user roles that apply to a page route map.

See [Service Portal](https://www.servicenow.com/docs/access?context=c_ServicePortal&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US) for more information.

</td></tr><tr><td>

Service Portfolio Management

</td><td>

-   Use the added options to edit and manage your service portfolios.
    -   Add life cycle fields to the taxonomy node records of your portfolios to align with the Common Service Data Model \(CSDM\).
    -   Added more flexibility to remap taxonomy nodes. You can move an entire branch of a taxonomy from one portfolio to another, including the automatic move of its child nodes.
    -   Reparent taxonomy nodes when you move them to a new location in a portfolio. You can also add a new taxonomy node in the middle of an existing portfolio, either between two nodes or between a node and a service.
-   Recognize the updated label for technical services.

See [Service Portfolio Management](https://www.servicenow.com/docs/access?context=SPM2-landing-page&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Service Reliability Management

</td><td>

-   View and assess alerts in one place with Express List.
-   Starting in version 6.3, access SRM features on the go with ITOM Mobile Agent.
-   Starting in version 6.4, inform teams by setting up notification destinations and attaching them to error budget policies.
-   Starting in version 6.4, track, manage, and visualize service performance with the Service reliability dashboard.
-   Starting in version 6.4, get timely error budget updates that reflect the impact of ongoing, open alerts.

See [Service Reliability Management](https://www.servicenow.com/docs/access?context=sr-landing-page&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

ServiceNow AI Lens

</td><td>

[Yokohama Patch 11](../quality/yokohama-patch-11.md)

-   Trigger ServiceNow AI Lens from the Now Mobile® application to extract data from artifacts and auto-fill fields in a form.
-   Fill the Catalog Item form fields by triggering ServiceNow AI Lens from Service Portal.

[Yokohama Patch 6](../quality/yokohama-patch-6.md)

-   Use the Lens actions to define default instructions, trigger options, custom context, transform response logic, and post processing instructions for ServiceNow AI Lens execution.
-   Configure Lens actions to launch ServiceNow AI Lens from any part of the ServiceNow AI Platform, such as a workspace form or a portal.
-   Trigger ServiceNow AI Lens from a Virtual Agent conversation on a mobile device or in a portal.
-   View captured images that are now attached to the record that is auto-filled using ServiceNow AI Lens.
-   Use Google Gemini and Anthropic Claude on AWS as AI model providers for ServiceNow AI Lens in addition to Azure OpenAI.

[Yokohama Patch 3](../quality/yokohama-patch-3.md)

-   Boost productivity by scanning artifacts and auto-filling information into forms instead of manually entering the information into forms.
-   Provide specific instructions to ServiceNow AI Lens on what to do with the data that it captures.
-   Get insights from multiple images so that you know what actions to do next.

See [ServiceNow AI Lens](https://www.servicenow.com/docs/access?context=servicenow-lens-landing-page&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US) for more information.

</td></tr><tr><td>

ServiceNow AI Platform core feature

</td><td>

-   Streamline how you access help content on the system events and job scheduling dashboard by accessing the appropriate help content in each tab.
-   Insert, update, and delete data in an external data source from a remote table.

See [Administer the ServiceNow AI Platform](https://www.servicenow.com/docs/access?context=intro-now-platform-landing&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US) for more information.

</td></tr><tr><td>

ServiceNow Add-in for Microsoft 365

</td><td>

-   Access any catalog form in Employee Center and submit requests within Microsoft 365 apps.
-   Load any ServiceNow form or navigate to a link in Employee Center.
-   Map message or appointment fields in Microsoft Outlook to be auto-populated in ServiceNow catalogs or forms.
-   Configure extension points to support messages and appointments in read and compose modes.

See [ServiceNow Add-in for Microsoft 365](https://www.servicenow.com/docs/access?context=sn-addin-for-ms365&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

ServiceNow IDE

</td><td>

-   Convert existing scoped applications to support development in source code.
-   Use TypeScript in JavaScript modules.
-   Install and use npm packages from private registries.

See [ServiceNow IDE](https://www.servicenow.com/docs/access?context=servicenow-ide-landing&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US) for more information.

</td></tr><tr><td>

ServiceNow SDK

</td><td>

-   Create and develop applications in source code using an upgraded ServiceNow SDK CLI workflow.
-   Refer to content from a file from properties in ServiceNow Fluent APIs.

See [ServiceNow SDK](https://www.servicenow.com/docs/access?context=servicenow-sdk-landing&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US) for more information.

</td></tr><tr><td>

ServiceNow Studio

</td><td>

-   Work in the best development environment for your task by using the experience switcher to switch between developing in Creator Studio, ServiceNow Studio, and ServiceNow IDE.
-   As of version 27.2.4, the ServiceNow Studio File Navigator performance has been improved for large applications.
-   As of version 27.2.4, you can easily identify apps created in Creator Studio or ServiceNow IDE by looking at the App Details page in ServiceNow Studio.
-   As of version 27.2.4, the file creation experience is now a full-page, guided process with built-in security checks. Admins see all application files, while delegated developers only see file types they have permission to create within the specified scope.
-   As of version 27.2.4, users with Write permission for an application description can use Now Assist for app summary generation to generate an app summary. The Summarize button is disabled for users without access to edit the app description, preventing failures after clicking.

See [Building applications with ServiceNow Studio](https://www.servicenow.com/docs/access?context=servicenow-studio-landing&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US) for more information.

</td></tr><tr><td>

Sidebar

</td><td>

-   Integrate Sidebar with Slack to enable users of both platforms to communicate with each other.
-   Create standalone Sidebar conversations that aren’t associated with a record.
-   Create private discussions on a record that are accessible only to the participants within that discussion.

See [Sidebar](https://www.servicenow.com/docs/access?context=sidebar-landing&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US) for more information.

</td></tr><tr><td>

Site Reliability Operations

</td><td>

Site Reliability Operations and Site Reliability Metrics \(extends SRO\) store applications are replaced with Service Reliability Management application.

See [Service Reliability Management](https://www.servicenow.com/docs/access?context=sr-landing-page&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Skills Foundation

</td><td>

-   Skill Harmonization lets you import and combines skills from the external learning management system \(LMS\) to have one source for skills.
-   Integrating Workday Learning skills and Workday Employee skills into the current import flow and relate them to the respective employees in the ServiceNow system.
-   Support for dynamic skills import requests from Credly \(OOTB source\) and other external sources. The skills are verified with the skills library \(exact or mapped match\), and new skills are added to the queue for processing. The harmonized skills are then linked back to the source using metadata.

See [Skills Foundation](https://www.servicenow.com/docs/access?context=skills-intelligence&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Smart Assessment Engine

</td><td>

-   Configure default responses for questions.
-   Copy an existing SAE template with all questions, sections, instructions, and configurations to save time.
-   Filter questions in an assessment to display only unanswered questions.
-   Search for text within assessment sections, subsections, and questions.
-   Auto-copy responses to all assessments when combining assessments, saving time and effort.
-   Calculate scores for assessment responses at the assessment, section, or subsection levels.
-   Set up post-assessment actions based on assessment responses.
-   Benefit from accessibility improvements to create a configurable workspace that supports Web Content Accessibility Guidelines \(WCAG\) 2.1 Level AA conformance.
-   Descriptive images are now supported in the guidance section for questions.

See [Smart Assessment Engine](https://www.servicenow.com/docs/access?context=smart-asmnt-engine-landing-page&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US) for more information.

</td></tr><tr><td>

Software Asset Management

</td><td>

-   Leverage generative AI by using the Now Assist for Software Asset Management \(SAM\) application to create publisher summaries on software deployment, license compliance, configuration health, and optimization.
-   Manage the licenses for your Oracle Databases and WebLogic deployments on the Nutanix virtualization technology.
-   Integrate SAP Ariba and SAP S/4HANA Cloud with the Software Asset Management application to monitor and track software usage and subscriptions effectively.
-   Simplify the onboarding of your Software Asset Management \(SAM\) application by following the prescriptive guidance provided in the SAM Guided Setup and Microsoft 365 Guided Setup.
-   Track and optimize your IBM Cloud Pak licenses by using the Software Asset Management application.
-   Benefit from accessibility improvements to create a configurable workspace that supports Web Content Accessibility Guidelines \(WCAG\) 2.1 Level AA conformance.

See [Software Asset Management](https://www.servicenow.com/docs/access?context=c_SoftwareAssetMgmt&version=yokohama&pubname=yokohama-it-asset-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Sourcing and Procurement Operations

</td><td>

-   Enable shoppers to view and select their local currency throughout the Shopping Hub experience, including supplier cards, product detail pages, cart, checkout, my purchases, and request tracker.
-   Enable procurement admins to configure and render unique question types for quick and full checkout experiences for each product or service line.
-   Use dashboards and tabs in the Source-to-Pay Workspace to view spend, savings, and pipeline projects, identify savings opportunities, and create pipeline projects directly from filtered lists.
-   Easily track products and services from ordering to fulfillment using procurement record IDs or keywords.
-   Access both punchout and native catalog products from Categories or Suppliers on the Shopping Hub home page.

See [Sourcing and Procurement Operations](https://www.servicenow.com/docs/access?context=psm-overview&version=yokohama&pubname=yokohama-source-to-pay-operations&ft:locale=en-US) for more information.

</td></tr><tr><td>

Strategic Planning

</td><td>

-   Reduce time and effort by using story recommendations from Now Assist to break down your epics and features in Enterprise Agile Planning \(EAP\).
-   Collaborate in real time on docs with multiple editors.
-   View the rolled-up financial costs and benefits data of your planning items on the new **Financials** tab in the Planning page.
-   View the financial data of planning items while creating multiple prioritization scenarios for efficient use of budget and to get better ROI.
-   Use dashboards to monitor performance, track progress, and make informed decisions related to ideas, feedback, planning, and execution.
-   Create, edit, and switch between views with display preferences for portfolio plans and free-form roadmaps.
-   Enhance the quality of planning item descriptions by enabling AI assistance.

See [Strategic Planning](https://www.servicenow.com/docs/access?context=alignment-planner-workspace-landing-page&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Strategic Portfolio Management for Telecom

</td><td>

-   Use templates to customize requirements for your Fiber Rollout and 5G projects.
-   Address challenges that manual processes cause by using customized templates.

See [Strategic Portfolio Management for Telecom](https://www.servicenow.com/docs/access?context=spmt-overview&version=yokohama&pubname=yokohama-telecom-media-technology&ft:locale=en-US) for more information.

</td></tr><tr><td>

Subscription Management

</td><td>

-   View subscription allocations according to the number of active users.
-   Select all recommended groups when allocating subscriptions.
-   Manage subscriptions in an on-premise installation.
-   Manage custom application and table mapping through the platform, and learn why specific subscriptions are recommended when mapping custom tables and applications.
-   View subscribers by domain for user-based subscriptions.

See [Subscription Management](https://www.servicenow.com/docs/access?context=subscription-management-landing-page-v2&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US) for more information.

</td></tr><tr><td>

Supplier Lifecycle Operations

</td><td>

-   Advanced case management for supplier lifecycle events including onboarding, offboarding, and ongoing operations.
-   Identify and prioritize suppliers for credit card payment adoption.
-   Estimate card payment benefits using the savings calculator tool.
-   Conduct sanction screening and validate banking details and supplier location change requests via Relish integration.
-   Map multiple internal stakeholders \(legal, business, technical, risk teams\) to suppliers to improve visibility and governance of supplier relationships.
-   Support for many-to-many \(M2M\) mapping between supplier contacts and suppliers. A single supplier contact can be the contact for multiple suppliers, if the suppliers share a parent-subsidiary relationship.
-   Automated KPI templates for automated data collection, KPI template modifications, and calculations.
-   KPI Management enhancements enable improved threshold setup, error messaging, and dashboard visualizations for KPI tracking.
-   Support for self-registration for supplier contacts. They can register with a supplier company name, enabling multiple domains under a single supplier.

See [Supplier Lifecycle Operations](https://www.servicenow.com/docs/access?context=supp-mgmt-landing-page&version=yokohama&pubname=yokohama-source-to-pay-operations&ft:locale=en-US) for more information.

**Note:**

You can experience a longer upgrade time if you’re upgrading from Vancouver or an older release to Washington DC or any latest release. This delay is due to a mandatory script that runs for restructuring the Supplier Task \[sn\_slm\_task\] table and the duration of upgrade depends on the number of records in this table.

</td></tr><tr><td>

Synthetic monitoring

</td><td>

-   View real-world performance data from your services without needing actual users, catching issues before they're released to production.
-   Get real-time notifications for performance degradations or outages before they impact users.
-   Visualize synthetic test results and share insights with stakeholders.

See [Synthetic monitoring](https://www.servicenow.com/docs/access?context=synthetic-monitoring-landing-page&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

System Update Sets

</td><td>

-   Add specific apps/versions as an app installation instruction in an update set.
-   Actions and subflows are available for update set operations, such as create, complete, retrieve, preview, and commit.

See [System update sets](https://www.servicenow.com/docs/access?context=system-update-sets&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US) for more information.

</td></tr><tr><td>

Table Builder

</td><td>

See [Table Builder](https://www.servicenow.com/docs/access?context=tb-landing-page&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US) for more information.

</td></tr><tr><td>

Talent Development Core

</td><td>

Yokohama Patch 3

-   Use the new Growth &amp; Performance AI agents to streamline your employee growth discussions in Career Conversations.

-   As an employee, Credly integration now enables you to display your digital credentials better demonstrating your skills in a tangible way.
-   As an administrator, use Achievements and Credentials, to view various forms of digital credentials such as badges, awards, certifications.
-   As an employee that meets the Talent Development user criteria, you can add custom opportunities with help from ServiceNow® Now Assist. Provide an AI prompt so that Now Assist can help you build a growth plan that matches your career goals and aspirations.

See [Talent Development Core](https://www.servicenow.com/docs/access?context=egd-landing-page&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Talent Feedback

</td><td>

-   Add multiple perspectives by gathering skill feedback from an employee’s collaborators to gain a more well-rounded view of their capabilities.
-   Enhance skill visibility by assessing skills when managers don’t work closely with employees or have different domain expertise.
-   Support skill validation by providing managers with qualitative inputs to validate employees’ skills.
-   Identify growth opportunities by uncovering skill gaps and learning needs.

See [Talent Feedback](https://www.servicenow.com/docs/access?context=talent-feedback-landing&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Telecommunications Network Inventory

</td><td>

-   View the geographical location and the details of your network site
-   Design and assign a configuration item using a playbook and add custom states to a Change model.
-   Define a logical composite to track and manage its CI.
-   Import and export your collection of models and templates in JSON format.
-   Enable Deny ACL to ensure the compliance with the enhanced security model.

See [Telecommunications Network Inventory](https://www.servicenow.com/docs/access?context=telecom-network-inventory&version=yokohama&pubname=yokohama-telecom-network-inventory&ft:locale=en-US) for more information.

</td></tr><tr><td>

Telecommunications Service Operations Management \(TSOM\)

</td><td>

-   Perform deep network discovery of your networks via the Simple Network Management Protocol \(SNMP\) and command-line interface \(CLI\) by using Pattern-based Discovery.
-   Integrate with the Nokia Altiplano Service Graph Connector to discover the access network.
-   Handle Discrepancy Identification and Reconciliation between your discovered and inventoried data.

See [Telecommunications Service Operations Management](https://www.servicenow.com/docs/access?context=telecom-service-operations-mgt-overview&version=yokohama&pubname=yokohama-telecom-service-ops&ft:locale=en-US) for more information.

</td></tr><tr><td>

Theme Builder

</td><td>

-   Edit and style the Unified Navigation component to better suit your brand.
-   Make individual style edits on a component by double-clicking it to quickly access the Component Editor.
-   As of Theme Builder version 5.1, customize the colors of empty state illustrations from within Theme Builder.
-   As of Theme Builder version 5.1, use your own custom images by overriding the default empty state illustrations.

See [Working with themes in Next Experience](https://www.servicenow.com/docs/access?context=next-experience-theming&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US) for more information.

</td></tr><tr><td>

Third-party Risk Management

</td><td>

-   Pre-populate questionnaires for entities and engagements that are associated with the same active third party by using responses from complete questionnaires.
-   Respond to questionnaires by using a Microsoft Excel questionnaire template.
-   Explore and analyze assessment data at various levels by using the Third-party insights dashboard and the TPRM custom analytics dashboard.
-   Stay aligned with stricter regulatory compliance and emerging third-party risk governance by using the new Standardized Information Gathering \(SIG\) questionnaire content available for 2025.

See [Third-party Risk Management](https://www.servicenow.com/docs/access?context=third-party-risk-mgt-landing-page&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US) for more information.

</td></tr><tr><td>

Threat Intelligence Security Center

</td><td>

-   Integrate with Microsoft Defender to enable Cyber Threat Intelligence \(CTI\) analysts to automatically push malicious or suspicious IP addresses, domains, file hashes, and URLs from TISC to Microsoft Defender.
-   Added creation of security incident directly from a TISC case with an option to associate observable artifacts to the security incident.
-   Enhanced support to export observables, indicators, and cases from the list views in STIX 2.1 JSON, CSV, and Excel formats.
-   Added settings to ingest indicators of interest based on associations to threat actors, threat reports, or malware families, including an option to include indicators deleted on CrowdStrike.
-   Improved Threat Intelligence Feed configuration functionality to create a duplicate copy of the existing feed.

See [Threat Intelligence Security Center](https://www.servicenow.com/docs/access?context=tisc-landing-page&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Upgrade Center

</td><td>

-   Explore the different release versions available to you in the Upgrade Preview module.
-   Use the Upgrade Preview module to gain insights about the upgrade experience without actually upgrading your instance.
-   Monitor the status of any ongoing upgrade and view the summary of your latest upgrade in the Upgrade Monitor module.
-   View all your past upgrades in the Upgrade History module.
-   Accelerate your upgrades using the Upgrade Plan feature.

See [Upgrade Center](https://www.servicenow.com/docs/access?context=uc-landing-page&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US) for more information.

</td></tr><tr><td>

Usage Insights

</td><td>

-   Access analytics more quickly across tracked ServiceNow applications in the redesigned UI.
-   Add and use new custom user properties more easily in the application. This requires older custom properties to be reconfigured under the new setup.
-   Advanced querying capabilities including user segmentation across all usage data and filtering of events by event property.

See [User Experience Analytics](https://www.servicenow.com/docs/access?context=user-exp-analytics-landing&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US) for more information.

</td></tr><tr><td>

Virtual Agent

</td><td>

[Yokohama Patch 7](../quality/yokohama-patch-11.md)

-   Create and manage LLM-based chat and voice assistants within Assistant Designer, a centralized assistant administrator experience.

[Yokohama Patch 6](../quality/yokohama-patch-6.md)

-   Start the create flow for all supported conversational assets directly from Virtual Agent Designer.
-   Enhance the user experience with Slack response message streaming capability.

[Yokohama Patch 3](../quality/yokohama-patch-3.md)

-   View people information in the synthesized response along with people citation when you search a person in Microsoft Teams chat.
-   AI agent support for Virtual Agent.
-   View AI agents and agentic workflows in Virtual Agent Designer.
-   Select AI agents to handle tasks in the AI Connector utility. See [AI Connector utility](https://www.servicenow.com/docs/access?context=vad-ai-connector-utility&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US), [Managing AI agents in Assistant Designer](https://www.servicenow.com/docs/access?context=managing-use-cases-ai-agents&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US), and [Using AI agents in Virtual Agent topics](https://www.servicenow.com/docs/access?context=ai-agent-custom-skill&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US) for more information.

[Yokohama Patch 1](../quality/yokohama-patch-1.md)

-   Enhance the user experience with Microsoft Teams response message streaming capability.

[Yokohama Early Availability](../quality/yokohama-security-notables.md)

-   Enhance the overall voice-based chat experience in Conversational IVR with Now Assist.
-   Generate synthesized responses in Slack conversations with Now Assist.
-   Generate synthesized responses in Microsoft Teams conversations with Now Assist.
-   View custom skills in Virtual Agent Designer.

See [Virtual Agent](https://www.servicenow.com/docs/access?context=virtual-agent-landing-page&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US) for more information.

</td></tr><tr><td>

Visa Spoke

</td><td>

-   Manage card disputes with Visa Resolve Online \(VROL\) and card-on-file payments with the Visa Stop Payment Service \(VSPS\) API suite using Visa Spoke.
-   Accept and close dispute items in a queue with Visa Spoke actions.
-   Download images from an endpoint using Visa Spoke actions.
-   Handle card operations and dispute resolution services with Visa Spoke actions.

See [Visa Spoke](https://www.servicenow.com/docs/access?context=visa-spoke&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US) for more information.

</td></tr><tr><td>

Vulnerability Response

</td><td>

-   With the sn\_vul.vulnerability\_analyst or sn\_vul.vulnerability\_admin role, create host remediation tasks manually in the Vulnerability Manager Workspace.
-   With the sn\_vul.remediation\_owner role, create host remediation tasks manually in the IT Remediation Workspace.

See [Vulnerability Response](https://www.servicenow.com/docs/access?context=vuln-landing-page&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US) for more information about the Vulnerability Response application. See the [Vulnerability Response Compatibility Matrix and Release Schema Changes](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0856498) Knowledge Base article for more information about released Security Operations applications and their version compatibility.

</td></tr><tr><td>

Vulnerability Response Integration with Claroty CTD

</td><td>

Identify and import vulnerabilities by using additional filter properties.

See [Vulnerability Response Integration with Claroty CTD](https://www.servicenow.com/docs/access?context=vulnerability-response-integration-with-claroty-ctd&version=yokohama&pubname=yokohama-operational-technology&ft:locale=en-US) for more information.

</td></tr><tr><td>

Vulnerability Response integrations

</td><td>

The Tenable.io CI lookup rules prioritize and populate the non-empty network interface values \(FDQN, IPV4, and MacAddress\) for a discovered item.

See [Vulnerability Response integrations](https://www.servicenow.com/docs/access?context=vuln_integrations&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Workforce Optimization for Customer Service CSM

</td><td>

-   Equip managers with comprehensive, real-time insights for continuous optimization.
-   Enable managers to take prompt action with key alerts organized by priority.
-   Provide real-time visibility into performance KPIs, work item status, and agent performance.

See [Exploring Workforce Optimization for Customer Service](https://www.servicenow.com/docs/access?context=explore-configurable-wfo-cs&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Workforce Optimization for ITSM

</td><td>

When you upgrade to the Yokohama release, get the enhanced security features by installing the new plugin.

See [Workforce Optimization for ITSM](https://www.servicenow.com/docs/access?context=workforce-optimization-itsm-landing-page&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US) for more information.

</td></tr><tr><td>

Workspace

</td><td>

-   Navigate form templates with larger cards, sorting preferences, and favorites.
-   Add collapsible content to email templates and attach a display to knowledge base links.
-   Leverage the latest workspace features for email composer in the Core UI.
-   Use lists that have additional condition builder fields, infinite scroll, live updates, and saved temporary lists.
-   Provide role-based access control for viewing and editing tables in the Activity stream.

See [Workspace UI](https://www.servicenow.com/docs/access?context=workspace-landing-page&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US) for more information.

</td></tr><tr><td>

Zero Copy Connector Hub

</td><td>

-   Access enterprise data from external data warehouses including Snowflake, Google BigQuery, and Amazon Redshift, data lakes such as Databricks, and databases, including Oracle.
-   Retrieve data from external sources in real time without copying any data to your instance using zero copy connections.
-   Enrich AI agents and workflows on the ServiceNow AI Platform with external data using data fabric tables.

See [Workflow Data Fabric Hub](https://www.servicenow.com/docs/access?context=workflow-data-fabric&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US) for more information.

</td></tr><tr><td>

Zero Copy Connector for ERP

</td><td>

[Yokohama Patch 3](../quality/yokohama-patch-3.md)

-   View charts and graphs on the Zero Copy Connector for ERP home page dashboard.
-   Accelerate your adoption of Zero Copy Connector for ERP using content packs.
-   Preview entities in the Model Manager.

[Yokohama Patch 1](../quality/yokohama-patch-1.md)

-   The name of the application has been changed from ERP Data Hub to Zero Copy Connector for ERP.
-   Export and import custom ERP models between instances.
-   Enhance communication security between SAP systems and your ServiceNow instance by using the SAP Secure Network Communication \(SNC\) connection option.
-   Manually name, edit, and maintain model manager fields.

See [Zero Copy Connector for ERP](https://www.servicenow.com/docs/access?context=erp-integration-overview&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Release notes summaries for Yokohama features](../release-notes-summaries.md)


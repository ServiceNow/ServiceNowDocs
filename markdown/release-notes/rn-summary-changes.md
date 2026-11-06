---
title: Changes to Brazil features and products
description: Cumulative release notes summary on changes to Brazil features and products.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/release-notes/rn-summary-changes.html
release: australia
topic_type: reference
last_updated: "2026-11-04"
reading_time_minutes: 113
breadcrumb: [Release notes summaries for Brazil features, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# Changes to Brazil features and products

Cumulative release notes summary on changes to Brazil features and products.

Existing  products were updated and changed in Brazil. This includes the renaming of certain buttons or features.

<table id="rn-summary-changes-table" class="custom-rows"><thead><tr><th class="filter">

Application or feature

</th><th>

Details

</th></tr></thead><tbody><tr><td>

AI Admin Center

</td><td>

-   **Updated AI Admin Center experience**

The new AI Admin Center experience provides a fresh look and feel, featuring revised pages and navigation to enhance your user experience. The Next Experience AI Admin Center workspace is still supported in this release.


</td></tr><tr><td>

AI Admin Hub

</td><td>

-   **[One-step activation of AI skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/configure-a-now-assist-skill.md)**

Activate an AI skill in AI Admin Hub with only one step. This optional activation method can be used for default skills with default settings. For granular or custom configuration, the previous guided setup wizard remains available from Advanced setup. One-step activation isn't available with Next Experience in this release.


</td></tr><tr><td>

AI Agent Advisor

</td><td>

-   **Updated AI Admin Center experience**

The new AI Agent Advisor experience in AI Admin Center provides a fresh look and feel, featuring revised pages and navigation to enhance your user experience. The Next Experience AI Admin Center workspace is still supported in this release.


</td></tr><tr><td>

AI Agent Studio

</td><td>

-   **New setup processes for agentic AI assets in redesigned AI Agent Studio**

The redesigned AI Agent Studio reimagines the creation and deployment processes for agentic AI assets. New features include automated evaluations built in to the application and easy creation of AI agents for automation opportunities. See Configure AI Agent Studio settings for how to access the previous UI.


-   ****

The Analyze task trends agentic workflow now includes citations for representative records associated with a pattern. Configure the workflow to include open tickets in its analysis by enabling the setting and running a Group Action Framework job to reindex with the new records.


</td></tr><tr><td>

AI Control Tower

</td><td>

-   **View input and output in trace details**

Toggle between input and output when viewing trace details.

-   **Usability improvements to Security Overview metrics**

See only actionable items in your top recommendations on the Security Overview tab. In addition, the recommendations rank AI agent insights by number of critical security events and show the agent name, critical event count, and top threat categories. The security events list now matches the list on the Post-runtime tab. The Access issues detailed view includes a description that explains each access issue in plain language—identifying the agent, the operation, the resource, and the denial count.

-   ****

Review sensitive data metrics for ServiceNow AI systems in a domain-separated instance. Available on the Runtime tab in Security.

-   **Configure Excessive Agency in Security**

Control whether Excessive Agency is enabled in Post-runtime configuration in Security. This setting controls data for Access issues and Privileged AI agents metrics, as well as post-runtime metrics. The setting is off by default.

-   **Post-runtime Security probabilistic metrics and AI agent disabled by default**

To reduce token consumption, screening for data integrity incident detection, system prompt leakage, correctness detection, prompt injection, and agent goal deviation is disabled by default. In addition, the Security Analyzer agent that determines security event severity and insights is disabled by default. The default sampling rate for all metrics is 1%. If you're upgrading, your Detection enabled setting for each metric isn’t affected. After upgrading, check your settings in **Settings** &gt; **Rules and templates** &gt; **Security** and adjust if needed.


-   ****

Use AI Control Tower on a domain-separated instance. In Security, detail pages for Privileged AI agents, Dormant AI agents, Access issues, Security events detected, Agent map, Post-runtime, and AI asset security score include a Domain column that shows the domain the AI asset belongs to, or shows `global` or is empty if domain separation isn't configured. Your top recommendations is replaced by a Security events detected section on the Security dashboard, and Sensitive data metrics aren't shown for ServiceNow AI systems.

-   ****

Agent status is renamed to Access posture on the Security tab for an AI asset. Also, Detection time is now the first column in the list of events.

-   **Security design-time metrics reorganized into subtabs**

Design-time metrics are organized into three subtabs: AI security posture, AI vulnerabilities, and AI validation. If the AI Security Exposure Management plugin isn't installed, use the source dropdown to filter the metrics by source \(for example, Cisco or HiddenLayer\).

-   ****

On the Security tab for an AI asset, access issues and access posture metrics aren't shown for AI models because they're agent-level signals derived from agent identity and permissions. Therefore, they don't apply to AI models.

-   ****

AI agent containment \(kill switch\) supports retrying a failed or partial containment operation from the asset record or the agent containment list. You can also deactivate any managed AI agent directly from its asset record, whether or not it has an associated security event. AI agent containment \(kill switch\) is now available directly from an AI asset's Overview tab, not just its Security tab, for security events of any severity.

-   ****

The Security tab under **Settings** &gt; **Integrations** is renamed to Control Enforcement Points.

-   ****

The GCP Vertex AI security connector is renamed to Gemini Enterprise Agent Platform.

-   **Agent containment list**

The Kill Switch Protocol Log is renamed the Agent containment list, and the **View details** option on the containment banner is renamed **View containment options**. The list now includes Domain and Actions columns. Containment details now show how the containment was initiated \(Manual or Automated\) and identity and enforcement details. The list can be filtered using the All, In progress, or Contained options, which replace the previous Show all link.

-   **Security dates and times shown in UTC**

Date and time values in the Security tab — including the agent containment list, the Overview tab's Dormant AI agents and Privileged AI agents details, and the Post-runtime tab's security events — are now shown in Coordinated Universal Time \(UTC\) rather than your local timezone.

-   ****

Starting in the September 2026 release, AI Gateway is available in AI Control Tower.

-   ****
    -   The GCP Vertex AI connector is renamed to Gemini Enterprise Agent Platform.
    -   The application AI Service Graph Connector for GCP is renamed to AI Service Graph Connector for Google.
    -   The Salesforce connector is renamed to AI Connector for Salesforce.
-   **Veza connector authentication**

The Veza connector now authenticates using OAuth 2.0. Configure an OAuth profile and alias on the platform, then select it from **Settings** &gt; **Integrations** &gt; **Connectors**. Depending on which OAuth credential is active, tokens are either issued per user and tied to user identity, or shared at the system level, replacing API key authentication as the default method. The Veza tile appears in **Settings** &gt; **Integrations** &gt; **Control Enforcement Points**.

-   **Create Asset Task action renamed**

The **Create AI Task** action, available on AI asset security events, privileged AI agents, and dormant AI agents, is renamed to **Create Asset Task**.

-   **AI security posture metrics added and renamed**

On the Design-time tab in Security, AI security posture subtab, three metrics were added under **AI assets with critical findings**: **MCP servers**, **Tools**, and **System prompts**.

Several metrics on the same subtab were renamed for clarity:

    -   **Critical findings approaching remediation target** is renamed **Findings approaching remediation target**.
    -   **Critical findings with remediation overdue** is renamed **Findings with remediation overdue**.
    -   **Number of findings deferred** is renamed **Findings deferred**.
    -   **Findings by risk rating** is renamed **Posture findings by risk rating**.
    -   **Findings by OWASP LLM Top 10** is renamed **Critical findings by OWASP top ten**.
    -   **Findings by MITRE ATLAS techniques** is renamed **Critical findings by MITRE ATLAS technique**.
The **Critical findings by platform**, **Critical findings by OWASP top ten**, and **Critical findings by MITRE ATLAS technique** metrics require the AI Security Exposure Management plugin, and are no longer available in the base system.

-   **Updated default Sampling rate and Max skill calls**

In **Settings** &gt; **Rules and templates** &gt; **Security**, the default values for Sampling rate and Max skill calls have changed to help ensure efficient, predictable analysis. If you're upgrading, your Sampling rate and Max skill calls are updated to the new defaults. Your Detection enabled setting for each metric is not affected. After upgrading, check your Sampling rate and Max skill calls settings under **Settings** &gt; **Rules and templates** &gt; **Security** and adjust if needed.


</td></tr><tr><td>

AI Desktop Actions

</td><td>

-   **Claude Sonnet 4.6 supported**
    -   Adaptive desktop actions now support version 4.6 of Claude Sonnet. It is now the default model for adaptive desktop actions.
    -   Use function keys \(F1–F12\) and combo keys \(cmd+a, alt+F4, ctrl+c\) in desktop automation without manual intervention.

-   **Browser startup and tab behavior**

Browser session now opens to an empty page instead of Google's homepage. Automation actions within the same chat window now reuse the existing browser tab instead of opening a new tab for every action. A new tab opens only when a new chat session starts or you close the current tab.

-   **Improved security for adaptive desktop actions system properties**

Adaptive desktop actions system properties now require appropriate read and write roles. This change prevents unauthorized users from viewing or modifying the configuration settings, while automation continues to work as expected.


</td></tr><tr><td>

AI Risk and Compliance

</td><td>

-   ****

Domain separation is supported for AI Control Tower. Domain separation enables separation of data, processes, and administrative tasks into logical groupings called domains. Administrators can control several aspects of this separation, including which users can see and access data. For AI Risk and Compliance, domain separation isolates each domain's risk posture while letting administrators at a parent domain see and manage risk across their child domains.

-   ** for unmanaged AI systems**

After upgrading to version 23.0.3, unmanaged AI systems receive a risk classification and appear on the Regulatory risk classification donut chart. The risk classification is calculated from the **Use and purpose** fields completed when the asset is created. After the asset moves to the **Managed** state, the risk classification is revised based on updates to the **Use and purpose** fields or based on regulatory risk classification updates.

-   ****

After upgrading to version 23.0.3, the **Save** button in the Compliance evaluation enables AI Risk and Compliance Analyst \[sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_analyst\] to maintain the configuration changes in **Draft** state before publishing. A dedicated **Owner** field lets you specify the owner of individual compliance evaluation configurations and displays the owner name in a column. Assigning ownership adds accountability and shows users who configured the rule.


-   **Links to AI Control Tower updated for Employee Center submissions**

After upgrading AI Risk and Compliance to version 23.1.1, for AI use case, AI model, and dataset submissions in Employee Center, the **here** link in the confirmation message and the **Open in AI Control Tower** link on the post-submission page now open the corresponding record in AI Control Tower instead of the legacy AI Control Tower workspace. You still land on the Employee Center governance-details page immediately after submitting; only the destination of these links changed.

The Employee Center AI asset list view's redirection link was also updated to open the AI Control Tower inventory.

The AI system, AI model, and dataset record headers also display the corresponding record name and identifier after submission.

**Note:** AI case and AI inquiry submissions in Employee Center aren't affected by this change.


</td></tr><tr><td>

AI Search

</td><td>

-   **Expanded support for hybrid search**

Hybrid search now supports all indexed sources that have semantic vector indexing configured.


</td></tr><tr><td>

AI Workflow Factory Prime

</td><td>

-   ****

The AI Workflow Factory Prime Credit Dashboard doesn't populate capability data on initial install. Use the troubleshooting guide to resolve the issue.


</td></tr><tr><td>

Access Management

</td><td>

-   ****

Improve access control predictability by enforcing strict denial when none of the referenced roles referenced in an ACL exist on the instance. This behavior doesn't apply to ACLs that have a mix of valid and invalid roles. This behavior is on by default for new instances. If you upgraded to this release, use the **glide.security.acl\_with\_invalid\_roles\_strict\_deny** property to turn it on. Navigate to **All** &gt; **Access Management** &gt; **Access Findings** to find these ACLs in the Access Checks list.


</td></tr><tr><td>

Accounts Payable Operations

</td><td>

-   **[Email parser agent for APO](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/email-parser-agent-for-apo.md)**

The Email parser agent in Accounts Payable Operations has been updated to remove the Universal Request \(UR\) path. When an incoming email contains multiple intents, the agent now processes it through the standard AP intent-handling flow instead of routing the email into a Universal Request.


</td></tr><tr><td>

Agent experience for CSM

</td><td>

-   **Name change for CSM/FSM Configurable Workspace**

The name of the CSM/FSM Configurable Workspace has changed. The workspace name is dependent on the installed products.

    -   CRM Workspace: For customers using the Customer Service Management application or working in the Customer Relationship Management \(CRM\) environment.
    -   Industry-specific names: For customers using any of the industry products, such as Financial Services or Public Sector.
-   **[ServiceNow Otto for Customer Service Management \(CSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/now-assist-csm.md)**

Starting with Zurich Patch 12, ServiceNow Otto is the new AI experience brand. This change is reflected in the name of ServiceNow products, including ServiceNow Otto for Customer Service Management \(CSM\). Your product entitlements remain unchanged. Check your entitlements to determine your access to specific features.


</td></tr><tr><td>

Audit Management

</td><td>

-   **Create evidence requests with a two-step process**

Create evidence requests with a two-step process by selecting the **Skip collection detail** option, which moves the request directly to **Work in Progress** state. It also enables you to add evidence manually without creating an Evidence Collection Details record.


</td></tr><tr><td>

Authentication

</td><td>

-   **SAML certificate expiry notification**

Receive more timely alerts — the SAML certificate expiry notification triggers earlier and includes additional detail about affected keystores.

-   **Max age parameter handling**

Set the max\_age parameter in an authentication request to require that the end-user has authenticated within a specified number of seconds. When the elapsed time since the last authentication exceeds max\_age, the Authorization Server reauthenticates the end-user. The max\_age implementation has been refined to align with the OpenID Connect Core 1.0 specification.

-   **KBA for AI voice service**

Use the KBA setup to configure Knowledge-Based Authentication \(KBA\) for the voice channel. Choose from base system questions at both the identification level and the authentication level. AI voice service mappings are populated automatically from your Assistant Designer selection, so manually mapping voice services is no longer a mandatory step in the KBA setup.


</td></tr><tr><td>

Autonomous Workforce

</td><td>

-   **Advanced search turned on by default**

See more richer and more relevant results to searches performed by the AI specialist.

-   **Follow-up metric added to AI specialist performance dashboard**

Monitor where requests stall and where guidance can be clearer by tracking the follow-ups necessary after an initial response by the AI specialist.


</td></tr><tr><td>

Build Agent and Autonomous Engineer

</td><td>

-   **Autonomous Engineer Test Agent settings enabled by default**

The Test Agent settings for Autonomous Engineer are enabled by default.

-   **Larger input box for extended prompts**

The input field for Build Agent and Autonomous Engineer prompts and instructions now expands to accommodate longer text entries.


-   **Build Agent in ServiceNow Studio UI updates**

Several changes have been made to how you access Build Agent in ServiceNow Studio:

    -   The central chat area on the ServiceNow Studio home page is the starting point for new Build Agent conversations.
    -   To open an existing conversation, select the Conversations icon \[Omitted image "ba-sns-otto-nav-icon.png"\] Alt text: in the Navigator panel.
    -   The Build Agent panel now opens on the Navigator panel of ServiceNow Studio.

</td></tr><tr><td>

CRM API Core

</td><td>

-   **[Sales and Service API Core](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/sales-and-services-api-core.md)Sales and Services API Core renamed to CRM API Core**

Sales and Services API Core application has been renamed to CRM API Core.


</td></tr><tr><td>

CRM Core

</td><td>

-   **[Install and configure Lead to Cash Core](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/install-and-configure-lead-to-cash.md)Lead to Cash Core renamed to CRM Core**

Lead to Cash Core application has been renamed to CRM Core.


</td></tr><tr><td>

CRM Outlook Add-in

</td><td>

-   **[Associate an email with an existing CRM record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/associate-email-crm-outlook.md)**

Reduce user confusion when records can't be displayed or found.

    -   Previously, users saw a blank page when a linked record couldn't be displayed. Now, users receive information that helps them understand whether the record is unavailable or access is restricted, along with guidance on next steps.
    -   Previously, users saw a blank page when searches and filters returned no matching records on the Lead, Account, Contact, and Opportunity tabs. Now, users receive guidance to help them refine their search criteria or create a new record.

</td></tr><tr><td>

Cloud Cost Management

</td><td>

-   **Optimization view on the Cloud Cost Management Workspace**

The Recommendations have been moved from the Operations view to the newly added Optimization view in the Cloud Cost Management Workspace. The Optimization view shows savings opportunities and recommendations for you across Unused resources, Rightsizing, Business hours, and Commitments.


</td></tr><tr><td>

Collaborative Work Management \(CWM\)

</td><td>

-   **[Import tasks entry point](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/import-tasks-cwm-board.md)**

The **Import tasks** option moved from a standalone button on the Board header into the **Create with Otto** menu, alongside the **Generate tasks** option. From the Board header, select **Create with Otto**, and then select **Import tasks** to start the import wizard.

-   **[Sprint sync between EAP and CWM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/cwm-integration-with-eap.md)**

Sprint name, state, capacity, and dates sync automatically from Enterprise Agile Planning to Collaborative Work Management for Agile teams that use non-calendar-based iterations, in addition to calendar-based teams.


</td></tr><tr><td>

Common Governance, Risk, and Compliance features

</td><td>

-   **Automatic entity owner and class updates**

With GRC Profiles version 23.0.7, the system automatically re-evaluates and updates entity owner and entity class when source record data or entity-filter membership changes. This change keeps entity ownership and classification aligned with the applicable entity-filter configuration.

-   **Issue grouping**

With GRC Issue Management version 23.0.5, you can add existing standalone issues directly from the Child Issues related list when grouping issues. You can group issues that use different workflows, and each child issue continues to follow its own workflow.


</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

-   **CMDB Workspace merged with Service Graph Workspace features**

Service Graph Workspace is deprecated as of this release. CMDB Workspace will have Service Graph Workspace features.

-   **ServiceNow Otto replaces Now Assist name**

Now Assist and Moveworks experiences is renamed to ServiceNow Otto \(Duplicate CI Remediator\).

-   **Reset certification tasks**

Reset a certification task to restart the certification process for the task. Reset sets all certification results for the task to a 'Review not completed' state and removes any comments that were added.

-   ****

When opening a task that isn’t closed, the Review not completed tab is selected by default for a quick access to task review. An Important information panel is now available throughout the task review process, that provides key details for the task such as special instructions and the ‘Allow field updates’ setting. You can attach files, such as supporting documents for various findings, to a task, and also, a percent complete number shows on the task page. The percent complete number is calculated as various certification activities are complete and reflects on the task review progress in real time.

-   **app\_service\_owner role contains the app\_service\_user role**

Use the app\_service\_owner role to grant create, read, update, and delete access to Service Instance records without granting the broader itil role. The app\_service\_owner role also includes the app\_service\_user role.

-   **Dynamic IRE Adoption**

Dynamic IRE is now enabled by default on zBooted instances, while on upgraded instances that are using Static IRE you can switch into using Dynamic IRE. Key benefits from the new Dynamic IRE engine include CI identification using an improved dynamic process and automatic updates of IRE identification rules during ingestion of data payloads.

-   **Inaccesible Records Indicator**

You can now review details about the outcome of a policy execution in the policy record in the CMDB Data Management Policy Executions \[cmdb\_data\_management\_policy\_execution\] table. Review the Wok Notes and the Activities fields and use details such as the number of CIs that weren't processed because they exist in other tasks, and access issues preventing processing of CIs to mitigate issues, for example, by updating the policy configurations or by updating user permissions.

-   **Unified Map performance improvements for Safari**

Unified Map now detects when it's running in Safari and disables edge animations by default to avoid a severe performance issue. This behavior applies to any workspace using the Unified Map template and its shared components, so pages built on that template are protected from the same issue without additional configuration.


</td></tr><tr><td>

Container Vulnerability Response

</td><td>

-   **Container Vulnerability Response**
    -   Enhancements to improve handling of Wiz API error codes that include clearer notifications directing users to contact the Wiz support team when a vendor-side error occurs.
    -   Enhancements to improve the reliability of the data migration for Wiz Container Vulnerability Response.

</td></tr><tr><td>

Continuous Authorization and Monitoring

</td><td>

-   **OSCAL enhancements**

The OSCAL enhancements include:

    -   Import system-generated authority documents \(SSP, POA&amp;M, SAR, SAP, ATO Letter, Executive Summary reports\) and user-attached files at Authorization Package and Authorization Boundary levels during OSCAL import.
    -   Control objective IDs include source values during OSCAL import and export.
    -   Policy fields are included during OSCAL import and export.

</td></tr><tr><td>

Core Business Suite

</td><td>

-   **[Exploring employee support](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/core-business-suite/exploring-emp-home.md) [Exploring supplier support](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/core-business-suite/exploring-supplr-home.md)**

Provide CBS admins with ia\_admin and ia\_user roles to give them broader permissions and control. The roles aren't available for the CBS admin by default.


</td></tr><tr><td>

Customer Service Problem Management

</td><td>

-   ****

Add characteristics directly to Test Groups, map product specifications to the Test Group that should run. Propagate those values to Test Definitions through attribute mapping and decomposition rules. The right tests run with the correct inputs for each product, reducing manual configuration and errors.


</td></tr><tr><td>

Customer Success Management

</td><td>

-   **[Meeting page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/acct-lifecycle-events/account-lifecycle-meeting-page.md)**

The prep brief now uses real meeting data for its AI-generated summary, fixing issues that caused fabricated citations and inaccurate sentiment claims.


</td></tr><tr><td>

Customer self-service for Sales Customer Relationship Management

</td><td>

-   **Display values in cart read responses**

Get readable values in cart responses without extra lookups. Previously, retrieving a cart returned display values only for product offerings and characteristics. Now, display values are returned for every attribute on the cart, its line items, and line item characteristics for cart retrieval, line item retrieval, and cart queries. Create and update requests don't return display values.

-   **Order submission from a sales cart**

Submit orders faster and keep them ready for downstream processing \(PRB2089913, PRB2109260, PRB2080458\).

    -   Previously, submitting a cart with many line items through the /sn\_sales\_cart/sales\_cart/\{cart\_id\}/submitOrder API waited until the entire order was created before returning. Now, carts with more than 20 line items are submitted asynchronously. The response returns immediately with an inbound queue record ID, and the cart state tracks progress, moving from Processing to Complete or Cancelled. If submission fails, the cart moves to the Cancelled state and can't be resubmitted.
    -   Previously, customer orders created from a sales cart through the submit order API had no channel, so downstream processes couldn't distinguish self-service orders from agent-assisted orders. Now, orders submitted through the API have the channel set to Self-service portal.
    -   Previously, the submit order API created customer orders in the Draft state. Now, it creates them in the New state.

-   **Order number in the submit order response**

Reference a new order in downstream systems without a follow-up call to retrieve its number. Previously, the /sn\_sales\_cart/sales\_cart/\{cart\_id\}/submitOrder response returned only the order ID, so external ordering systems had to query the order record separately to obtain the order number. Now, the response returns the order number alongside the order ID.

-   **Product offering eligibility validation when creating a cart**

Prevent ineligible product offerings from reaching order submission by validating them as the cart is created.

    -   Previously, any product offering could be added to a cart regardless of eligibility, and the resulting issues surfaced only after the order was submitted. Now, the product offerings on a cart are validated against the configured eligibility rules, and the cart isn't created when any of them is ineligible.
    -   Previously, the response gave no indication of which product offerings caused a failure. Now, the response identifies each ineligible product offering so that you can resolve it before retrying.

</td></tr><tr><td>

Data Catalog

</td><td>

-   **Graph Explorer performance improvements**

Lineage views open faster by showing the nearest upstream and downstream connections first instead of waiting for the full diagram to load.

-   **ServiceNow collector lineage from Import Set Transform Maps**

The ServiceNow collector harvests lineage edges based on the platform's native Import Set Transform Map framework.


-   **Data assets lineage improvements**

Transform nodes now display transformations and processing steps in your lineage diagram with enhanced visualizations. Interact with transform nodes to view additional details about what data transformations occur at each step, to help you understand your data flow more clearly. Lineage graphs now load progressively by level, to reduce timeout risk when viewing large graphs. The system displays lineage in stages, allowing you to explore relationships without waiting for the entire graph to load, which improves overall responsiveness and performance.


</td></tr><tr><td>

Data Management for CSM

</td><td>

-   **[Product inventory configurations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/product_inventory_configurations.md)**

Order agents can modify, suspend, resume, or disconnect a consumer’s product inventory from the consumer record. Configuration updates reflect automatically on each quote or order to make sure customer's services are faster and more accurate.


-   **Service organizations as buyers on install base records**

Add service organizations as buyers on install base records to control access to their product inventory by user role. Use the Modify or Disconnect actions from the service organization record to enable service organizations to create orders or quotes.


-   **Project task assignment access for business organization staff**

Gain write access to the Assignment group and Assigned to field, and read access to the Priority field, on business organization project tasks with the Location Project Member \[sn\_bus\_loc.location\_project\_stakeholder\] or Location Project Manager Contributor \[sn\_bus\_loc.location\_manager\_project\_stakeholder\] role.

-   **[Billing account roles and responsibility access](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/granular-roles-and-supported-entities-CAM.md)**

Updated billing account roles and responsibility access to align with the expanded billing account capabilities. Extended access to Billing Account Address, Billing Account Payment Profile, and Billing Schedule \(schedule and schedule entry\) through:

    -   Billing Account platform granular and CRM granular roles
    -   Billing Account responsibilities through the customer access management \(CAM\) framework
-   **[Create a sold product](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/create-sold-item.md)**

Edit and view multiple related parties in the sold product enable users to review the details of a deal and review deal context without leaving the record. **Deal type** and **Route to Market** aren't captured on the sold product, with route to market options filtered automatically based on the selected deal type.

-   **Create return merchandize authorization \(RMA\) cases directly from the business portal**

Initiate an RMA case from the business portal without contacting an agent to reduce the back-and-forth for returns and replacements.

    -   Enable customer contacts to view the list of their RMA cases from the **Request** menu on the portal to track their requests in progress.
    -   Customer contacts can open individual RMA cases and drill into case lines to review its status and details.

</td></tr><tr><td>

Decision tables

</td><td>

-   ****

Decision table exports now apply the access control lists \(ACLs\) to the data that's exported. Access is determined by the ACLs on the referenced table. This issue is related to PRB2067404.

-   ****

Delegated developers can now create, read, edit, and delete decision tables that belong to an application they have delegated developer access to. This issue is related to PRB2065210.


</td></tr><tr><td>

Developer Sandboxes

</td><td>

-   **Manual sandbox enablement**

Starting with the Brazil Patch 2 release, installing the `com.glide.dsb` plugin no longer enables Developer Sandboxes automatically. Enable it manually by setting the following property on the instance before you add it through license management:

    -   `glide.dev_sandbox.enabled`: Set to `true`.

</td></tr><tr><td>

Digital End-User Experience

</td><td>

-   ****

The Devices page now includes a link to DEX dashboard, so users with multiple roles can reach the DEX homepage faster.

-   ****

The Diagnose view in Device Health Check now explains why a category shows a **Poor** or **Average** status with no pending actions. It tells users that their IT team is reviewing additional metrics.


</td></tr><tr><td>

Digital Product Release

</td><td>

-   **Charts exclude cancelled phases from the release dashboards**

Policies, phase tasks, and task approvals attached to a cancelled or restarted release phase are excluded from chart aggregates. They are also filtered out from the lists that opens on selecting a chart segment. This applies to the Digital Product Release landing page, Release Overview, Release Bundle Details, and the multi-product release dashboard.

-   **Digital Product Release home page widgets scoped to your releases**

The **My releases** chart on the Digital Product Release Workspace home page shows only releases where you're the release owner or a release team member.

-   **Release actions on all release pages**

From any release page, perform actions such as **Start release**, **Re-target release**, **Close release**, **Complete current phase**, and **Run policies**.

-   **Release template**

The **Manage release template** button on the Release template form is renamed **Edit release template**.

-   **Release creation wizard**

Additional Products fields are no longer required in the Create release flow.

-   ****

In a multi-product release, the policy status of a product added after the release starts rolls up to the main release.

-   **Product enhancement creation**

The **sn\_dpr\_workspace.enhancement\_work\_item\_types** system property controls which work item types auto-create product enhancements. Leave it empty to stop enhancement creation.


</td></tr><tr><td>

Discovery

</td><td>

-   **Scan options for credential-less discovery**

Credential-less Discovery can now check UDP ports and guess the operating system of a target host when it can't confirm an exact match. Enable each option by setting a MID Server property. Both options are inactive by default. Set **mid.discovery.credentialless.include\_udp\_scan** to `true` to check UDP ports and TCP ports. Set **mid.discovery.credentialless.include\_os\_scan\_guess** to `true` to let the scan guess the operating system of the target host.

-   **Increased default partitions for software discovery**

The default value of the **com.glide.ensurer.partitions.cmdb\_ci\_spkg** system property changed from `64` to `128`. This change improves software discovery performance on instances with a large number of discovered software installations and without Software Asset Management \(SAM\) installed. The change applies automatically on upgrade.


-   **IP Inventory multi-schedule link**

IP ranges and IP network discovery ranges that belong to a discovery range set used across multiple schedules now display a linked value in the **Discovery Schedule** column. Select the **Multiple** link to open the associated records in the Discovery Schedule Range \[discovery\_schedule\_range\] table, filtered by the relevant discovery range.


</td></tr><tr><td>

Discovery store applications

</td><td>

-   **Amazon Bedrock attribute updates**
    -   Version is now populated in the object ID and product instance ID fields.
    -   Vendor is populated in AI System Digital Asset \(alm\_ai\_system\_digital\_asset\) and AI Prompt Digital Asset \(alm\_ai\_prompt\_digital\_asset\).
    -   Manufacturer now populates from the **glide.appcreator.company.friendly\_name** system property instead of a hardcoded value in the AI System Component Product Model \(cmdb\_ai\_system\_component\_product\_model\) and AI Prompt Product Model \(cmdb\_ai\_prompt\_product\_model\) tables.
-   **Microsoft Foundry \(classic\) attribute updates**
    -   Vendor is populated in AI System Digital Asset \(alm\_ai\_system\_digital\_asset\) and AI Prompt Digital Asset \(alm\_ai\_prompt\_digital\_asset\).
    -   Manufacturer now populates from the **glide.appcreator.company.friendly\_name** system property instead of a hardcoded value in the AI System Component Product Model \(cmdb\_ai\_system\_component\_product\_model\) and AI Prompt Product Model \(cmdb\_ai\_prompt\_product\_model\) tables.

-   **AWS active datacenter discovery**

AWS discovery now uses the Resource Explorer API instead of the Config API to determine whether a datacenter region is active or passive. Use the `mid.cloud.discovery.sonar.exclude_resource_types` property to exclude specific resource types when evaluating a region's status.

-   **OCI virtual machine BYOL discovery**

The "Oracle OCI - Virtual Machine \(LP\)" pattern now discovers the Windows license type for OCI virtual machines \(VMs\), including Bring Your Own License \(BYOL\) and License Included.

-   **Service Account and Logical Datacenter job full resync**

The **Populate SA and LDC IN CMDB** job supports a full resync to reprocess all configuration item \(CI\) records. Configure the **sn\_itom\_pattern.populate\_saldc\_full\_resync** system property when service accounts or logical datacenters have incorrect or corrupted values for a CI.


-   ****

Resolved the issue where the connector uses a database view that breaks when sys\_object\_source is moved to a gateway database.

-   ****

Resolved the issue where a `Found multiple dependent relation items` error occurs when resources are moved between Azure datacenters.

-   ****

Resolved the issue where the Disk Space field isn’t populated with the correct size during hardware import. The error occurred because the temporary disk size \(returned in megabytes\) was written to the hardware template without being converted to gigabytes.

-   ****

Duplicate network interface card \(NIC\) CIs are created after SNK updates.

-   ****

The Install status and Disk Space fields are now populated with RTE mappings for the Server class and the Computer class.

-   ****

The Install status is now correctly updated for scale set virtual machines.

-   ****

Resolved the issue where the operational\_status of a virtual machine CI reverts from Retired to Deployed after the virtual machine is deleted because the ETL transform script reads only the provisioning state and doesn’t check the change type.

-   ****

Relationships are now created from Kubernetes Clusters and Azure Functions for service accounts.

-   ****

Resolved the issue where software removal responses that were returned as `modified` created new CIs, resulting in duplicate records.

-   ****

Resolved the issue where the hardware consolidation job and its underlying database view join filter on `PoweredState = ON`, which excludes powered-off virtual machines and can lead to incorrect data when the import runs outside business hours.

-   ****

CIDR information is now correctly populated.

-   ****

Resolved the issue where a datacenter is incorrectly marked as Passive when it contains only resource groups with no resources.


-   **New account state for AWS account API**

The response status \(Status field\) of the AWS account API is now mapped to the new account state \(State field\).

-   **aws\_lookback\_time\_in\_days connection property**

Resolved the issue with the aws\_lookback\_time\_in\_days connection property. Imports now follow the configured lookback window.

-   **aws\_lookback\_time\_in\_days connection property updated after full data load**

The aws\_lookback\_time\_in\_days connection property is now updated only after a full scheduled data import.

-   **ListAccounts API call handles deprecated Status field**

Resolved the issue where the ListAccounts API call didn’t handle the deprecation of the Status field, which could cause account imports to fail.

-   **Is Virtual attribute populated in Server records**

The Is Virtual attribute is populated in the Server records created by Get Inventory imports.

-   **AWS organization set as parent for Amazon Redshift cluster records**

The AWS organization is set as the parent for the Amazon Redshift cluster records that are created by the scheduled import.

-   **Version data populated for operating system record**

The version data is populated for the operating system record in the Software Installation table.

-   **EKS Cluster data source**

Resolved the issue where the EKS Cluster data source returned an error when the enableDbConfigLoad property is set to true.

-   **Flow execution contexts created for Get Inventory imports**

Flow execution contexts are created for Get Inventory imports.

-   **Updated CloudFormation templates**

The CloudFormation templates \(CFT\) used by the connector are updated to the latest versions available in SGC Central.

-   **GetS3Object transform doesn't overwrite names or create duplicate records**

Resolved the issue where duplicate server records were created because the GetS3Object transform overwrote the Name field.

-   **isLastImport function in AwsRemovalUtil**

Resolved the issue where the isLastImport function in AwsRemovalUtil only checked whether schedule imports were queued. The final import is now detected correctly.

-   **EKS ETL transformation for pod payloads with no volume mounts**

Resolved the issue where the EKS ETL transformation failed for pod payloads that contain no volume mounts. Such payloads are now transformed successfully.

-   **Server records for AWS SSM-managed instances**

Server records aren’t created for AWS Systems Manager \(SSM\) managed instances.

-   **EKS full scheduled import**

Resolved the issue where an EKS full scheduled import didn’t import EKS data when the sn\_aws\_integ.eks\_document\_processing\_time property is set to 100.

-   **Status field removed from ETL mapping for SG-AWS-Service-Account data source**

The deprecated Status field is removed from the ETL mapping for the SG-AWS-Service-Account data source.


-   **Deep discovery jobs on GCP VM instances**

Deep discovery jobs in the SG-GCP upgrade packages on GCP VM instances are now successful during discovery.

-   **Relationship created between cloud database and region**

A relationship is created between cloud database and region.


-   **Discover all URLs toggle**

Fixed a cross-application scope error that blocked the **Discover all URLs** toggle from working when a scope other than ITOM URL Discovery was active. Set the application scope to **ITOM URL Discovery** to turn the toggle on or off.


</td></tr><tr><td>

Dispute Rules Content Pack for Mastercard

</td><td>

-   **Updated Mastercard chargeback ineligibility decision tables for Colombian reversion of payment claims \(RC 4837, RC 4870, and RC 4871\)**

Review updated chargeback eligibility for Mastercard fraud disputes on Colombian transactions. Eligibility now depends on the dispute agent's answer to the reversion of payment claim question in the dispute questionnaire. The question asks whether the cardholder filed a reversion of payment claim \(RP-Reg\) under Law 1480 of 2011, Article 51, and Decree 587 of 2016. Under the Mastercard guide, RC 4837, RC 4870, and RC 4871 do not apply to a Colombian domestic transaction that the reversion of payments regulation addresses.

The following decision tables each change the ineligibility condition for their Colombia rule:

    -   **Mastercard 4837 - No Cardholder Authorization**
    -   **Mastercard 4870 - Chip Liability Shift**
    -   **Mastercard 4871 - Chip Liability Shift-Lost/Stolen/Never Received Issue \(NRI\) Fraud**
Before this release, each rule decided that a dispute was ineligible from the authorization data alone. A dispute was ineligible when the authorization had a fee collection function code or the original message type identifier 1740, the acceptor country was Colombia, and the cardholder billing currency was Colombian Peso \(170\). A dispute is now ineligible when the answer to the **This dispute is due to \(Mastercard\)** question on the dispute intake record matches the reason code of the decision table and the answer to the reversion of payment claim question is Yes. When the answer is No, this rule does not make the dispute ineligible.

The location and currency checks now apply to the question rather than to the rule. The dispute questionnaire asks the question only for Mastercard disputes with RC 4837, 4870, or 4871 when the acceptor country is Colombia and the cardholder billing currency is Colombian Peso. The dispute questionnaire change is described in the Financial Services Card Operations release notes.

-   **Updated Mastercard chargeback ineligibility decision tables for fraud report checks \(RC 4837, RC 4849, RC 4870, and RC 4871\)**

Review updated chargeback eligibility for Mastercard fraud disputes. Eligibility now depends on whether the transaction was reported as fraud before the chargeback. This reflects the Mastercard requirement that the issuer report the transaction as fraud on or before the date of the chargeback. The following decision tables each change the fraud report ID condition:

    -   **Mastercard 4837 - No Cardholder Authorization** for Mainland China domestic transactions and for all other transactions
    -   **Mastercard 4849 - Questionable Merchant Activity** for Mainland China domestic transactions and for all other transactions
    -   **Mastercard 4870 - Chip Liability Shift** for Mainland China domestic transactions
    -   **Mastercard 4871 - Chip Liability Shift-Lost/Stolen/Never Received Issue \(NRI\) Fraud** for the fraud report timing rule
Before this release, the RC 4837 conditions made a dispute ineligible when a fraud report ID was present, and the RC 4849 conditions made a dispute ineligible when both a fraud report ID and a Mastercard fraud type were present. A dispute is now ineligible when the fraud report ID is empty, and the RC 4849 conditions no longer check the fraud type. For RC 4870, a dispute for a Mainland China domestic transaction was ineligible when the fraud type was not 04 and a fraud report ID was present. The dispute is now ineligible when the fraud type is not 04 or the fraud report ID is empty. The chargeback ineligibility reason text for RC 4837 is updated to say that the transaction was not reported on or before initiating a chargeback.

For RC 4871, the rule that makes a dispute ineligible after the fraud report no longer requires a fraud report ID. A dispute is ineligible when the fraud type is 00, 01, or 02 and the dispute is raised more than three days after the fraud report date.

-   **Updated Mastercard chargeback ineligibility decision table for Credit Posted as a Purchase \(RC 4853\)**

Review the updated **Mastercard 4853 - Credit Posted as a Purchase** decision table, which changes the ineligibility condition for the **Refund posted as a purchase** dispute reason. Before this release, a dispute was ineligible when the disputed amount was not equal to twice the original transaction amount. A dispute is now ineligible when the disputed amount is more than twice the original transaction amount. The chargeback ineligibility reason text is updated to say that the disputed amount should not exceed twice the original transaction amount.

The decision input for the condition is renamed from **dispute\_amount\_neq\_twice\_transaction\_amount** to **dispute\_amount\_gt\_twice\_transaction\_amount**. If you reference the input in a customization, update the reference.

-   **Updated Mastercard chargeback ineligibility decision table for repeat fraud chargebacks and digital goods \(RC 4837\)**

Review two updated ineligibility conditions in the **Mastercard 4837 - No Cardholder Authorization** decision table.

The condition for repeat fraud chargebacks on the same Mastercard card account uses the **Fraud CB count before auth date** input. Before this release, a dispute was ineligible when the **Chargeback transactions count** was three or more, regardless of when the chargebacks were submitted. A dispute is now ineligible when the count is two or more. The new count includes only chargebacks that were submitted before the authorization date of the disputed transaction.

The condition for digital goods purchases of USD 25 or less now evaluates card data input mode S or R and the merchant category codes \(MCCs\) 5815, 5816, 5817, and 5818.

-   **Removed Mastercard chargeback ineligibility rules \(RC 4837, RC 4849, and RC 4871\)**

Review the following updated ineligibility rules, which no longer apply. Disputes that previously matched them are no longer ineligible on that basis:

    -   The **Mastercard 4849 - Questionable Merchant Activity** decision table no longer includes the rule that made a dispute ineligible when the cardholder had neither attempted to file a police complaint nor completed a coercion claim affidavit.
    -   The **Mastercard 4837 - No Cardholder Authorization** decision table no longer includes the rule for transactions with wallet identifier 101 and e-commerce indicator 221, 222, or 225.
    -   The **Mastercard 4871 - Chip Liability Shift-Lost/Stolen/Never Received Issue \(NRI\) Fraud** decision table no longer includes the rule that made a dispute ineligible when the POS card data terminal input capability was not 2, or when the cardholder authentication method was PIN and the response code was 00. The rule applied to all regions.
The removals apply to new and existing installations.


-   **Updated Mastercard chargeback ineligibility decision tables for fraud \(RC 4870 and RC 4871\)**

The ineligibility condition for RC 4871 \(Chip Liability Shift, Lost, Stolen, or Never Received Issue \(NRI\) Fraud\) in the **Mastercard 4871 - Chip Liability Shift-Lost/Stolen/Never Received Issue \(NRI\) Fraud** decision table reverses the comparison for the fraud-report timing window. Before this release, a dispute was ineligible when it was raised fewer than three days after the transaction was reported lost, stolen, or never received in the fraud and loss database. A dispute is ineligible when it is raised more than three days after the report. The condition also requires a fraud report ID to be present; this requirement is unchanged. The associated chargeback ineligibility reason text is updated to match the current wording in the Mastercard Chargeback Guide.

The **Mastercard 4870 - Chip Liability Shift** and **Mastercard 4871 - Chip Liability Shift-Lost/Stolen/Never Received Issue \(NRI\) Fraud** decision tables each change the ineligibility condition for repeat fraud chargebacks on the same Mastercard card account. Before this release, a dispute was ineligible when the **Chargeback transactions count** was three or more. The count included chargebacks under RC 4837, RC 4870, or RC 4871, regardless of when they were submitted. The condition uses a new input, **Fraud CB count before auth date**, and a dispute is ineligible when the count is two or more. The new count includes only chargebacks that were submitted before the authorization date of the disputed transaction. The chargeback ineligibility reason text in both decision tables is updated to specify fraud chargebacks.

-   **Updated Mastercard chargeback ineligibility decision table for Refund Not Processed \(RC 4853\)**

The **Mastercard 4853 - Credit Not Processed** decision table adds a condition to the ineligibility rule for RC 4853 \(Refund Not Processed\). Before this release, a dispute was ineligible when the transaction had one of the merchant category codes \(MCCs\) 3000 through 3999, 4411, 4511, 4722, 6513, 7011, 7512, 7519, or 7922. The MCC list is unchanged. A dispute with one of these MCCs is ineligible only when the merchant provided a voucher for future use and disclosed it in its terms and conditions. The new condition checks that the answer to the merchant voucher question in the dispute questionnaire is Yes. The chargeback ineligibility reason text is updated to describe the voucher condition.


-   **Updated Mastercard chargeback ineligibility rules for fraud**

Ineligibility rule conditions are updated for the following reason codes:

    -   RC 4837 \(No Cardholder Authorization\)
    -   RC 4849 \(Questionable Merchant Activity\)
    -   RC 4870 \(Chip Liability Shift\)
    -   RC 4871 \(Chip Liability Shift, Lost, Stolen, or Never Received Issue \(NRI\) Fraud\)
The Mastercard Commercial Payments Account ineligibility condition and its associated formula apply only until the Mastercard rule effective date of October 23, 2026. The same condition applies across all four reason codes. The chargeback ineligibility reason text for RC 4849 is also updated to match the wording in the Mastercard Chargeback Guide.

-   **Updated Mastercard chargeback ineligibility rules for authorization**

Ineligibility rule conditions are added or updated for the following RC 4808 Authorization sub-categories:

    -   Required Authorization Not Obtained \(RANO\). A new ineligibility condition applies to automated fuel dispenser transactions under merchant category code 5542 in Japan. The condition applies to transactions up to JPY 15,000 at CAT 1, CAT 2, and CAT 6 terminals. This condition takes effect after October 23, 2026.
    -   Transit First Ride Risk Framework Claims \(TFRR\) and Transit First Ride Issuer Liability Framework Claims \(FRIL\). Two conditions and their associated formula read the transit transaction type indicator from the Financial Transaction table instead of the Financial Transaction Authorization table.
-   **Transit transaction type indicator values**

The transit transaction type indicator values on the Financial Transaction Authorization table match the current Mastercard specification. Value 02 reads Deferred retail like, and values 09 and 10 are available for selection.


</td></tr><tr><td>

Enterprise Architecture

</td><td>

-   **[Business application insights trigger](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/generate-insights-into-ba.md)**

Choose how the ServiceNow Otto Business application insights skill is triggered on the **Define trigger** tab in the AI Admin Hub. With the **Automatic** option selected, business application insights are generated when you open a business application record page, and the side panel in the application rationalization bubble chart opens on the **Insights** tab.

With the **User trigger** option selected, business application insights are generated only when you select **Generate insights**, and the side panel opens on the **Details** tab.

-   **[Enterprise Architecture query agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/ea-qna-overview.md)**

Ask the Enterprise Architecture query agent about the impact of an infrastructure configuration item \(CI\), such as a database, database instance, server, or storage device. The agent follows CMDB relationships from the CI to the application services, business applications, and business capabilities that depend on it. You can also ask which infrastructure a business application or application service depends on.

-   **[ServiceNow Otto for Enterprise Architecture skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/exploring-now-assist-for-ea.md)**

Use the Gemma 4 model with ServiceNow Otto for Enterprise Architecture skills that run on the Now LLM Service.

-   **[Technical debt list and form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/view-trm-tech-debt.md)**

View the new **Number** field in the technical debt list and form. Select a value in the **Number** column in the Technology Portfolio page to open the technical debt record.


-   **[Domain separation for AI Control Tower integration with business applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-aict.md)**

Enterprise Architecture Workspace now supports domain separation for AI system associations with business applications. On domain-separated instances, the business applications available for association reflect the domain hierarchy: you can associate applications in the global domain and in your current domain, and viewing the association from a parent domain shows the AI system associations created in that domain and in all of its child domains.

-   **Technical debt list and form**
    -   New **State** field shows whether the record is **Active**, **Resolved**, or **Archived**.
    -   New **Edition** field shows the software edition when the technical debt is created from a TRM product lifecycle that matches on both version and edition. The edition is part of the record's identity: a technical debt for version X, edition A is a separate record from a technical debt for version X, edition B.
    -   On the technical debt record page, the new **Discovered Technology** related list shows the TLM discovered technology records that generated the technical debt. It can be used as a starting point for the technical debt remediation.
    -   Select a value in the **Reason** column of the technical debt list to open the technical debt record directly.
-   **TRM product and lifecycle requests**
    -   A single TRM product request or product lifecycle request can now include multiple lifecycle records. It can support up to 5 version-and-edition combinations or 5 hardware models, with up to 10 phases each. This applies both in the Enterprise Architecture Workspace and when requesting from the service catalog.
    -   A standalone TRM product lifecycle request can include multiple child lifecycle records in a single bulk request. Approving or rejecting the parent request determines the outcome for all associated child records.
    -   Approvers can review requested and existing lifecycle records side by side using the new **Requested Lifecycles** and **Existing Lifecycles** tabs before approving or rejecting a request. Approvers can edit request details without triggering an approval decision.
-   **TLM Technology Lifecycle data**

When multiple sources contribute lifecycle phase dates for the same product, the source with the highest configured rank now takes precedence, and phase dates are validated to stay in chronological order.


</td></tr><tr><td>

Enterprise Asset Management

</td><td>

-   **Product catalogs menu item**

In the navigation panel of the Admin center view, the **Product catalogs** menu item has been renamed to **Product catalog items**.


</td></tr><tr><td>

Export to PowerPoint

</td><td>

-   **[Dynamic timeline type for roadmap exports](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/export-a-portfolio-plan-to-powerpoint-strategic-planning.md)**

Get more granular roadmap exports with timeline types that now reflect the actual export range. Previously, the timeline type was hardcoded. The timeline type is now derived from the resolved export range length. Ranges of one year or less use months, ranges over one year up to two years use quarters, and ranges over two years use years.


</td></tr><tr><td>

External Content Connectors

</td><td>

-   **Secure search for the Amazon S3 external content connector**

The Amazon S3 external content connector adds support for secure search. The **Settings** tab for this connector includes a new **User mapping settings** screen. On this screen, you can select one of three permission modes for the connector and optionally configure user mappings. You can also configure user permission crawls for the connector if using a permission mode that requires them.

-   **Analytics for external content connectors**

The **Quota usage** metric has been renamed **Connector limit** for clarity.


-   **Crawl schedules tab renamed**

In the external content connector editor, the **Crawl schedules** tab has been renamed to **Manage crawls**.


</td></tr><tr><td>

Financial Services Card Operations

</td><td>

-   **Dispute Summarization component update**

The Now Assist context menu \(NACM\) component replaces the AI Summary Card component that generated Dispute Summarization on the dispute record page. Dispute agents can generate an AI-generated summary of a dispute from the dispute record page.

Dispute agents can share a generated summary to the claim's work notes from the summary component. Selecting **Share** opens an editable work notes dialog, where agents can edit the summary text before selecting **Save to work notes**.

Activate the Dispute Summarization skill configuration for the summary component to appear. If the skill configuration isn't active, the component doesn't display on the dispute record page.

-   **UI policy update for the merchant voucher question on Refund Not Processed disputes**

The Mastercard-specific merchant voucher question in the dispute questionnaire displays for Refund Not Processed disputes when the transaction has one of the following merchant category codes \(MCCs\): 3000 through 3999, 4411, 4511, 4722, 6513, 7011, 7512, 7519, or 7922. The UI policy **Field: TransactionMerchantVoucherFutureUseInd - Show/Hide/Mandatory \(Consumer\)** controls this display. Before this release, the UI policy displayed the question for Goods or Services Not Provided disputes and for Travel and Entertainment disputes where the merchant issued a voucher. The question and the MCC list are unchanged. Dispute agents answer whether the merchant provided a voucher for future use and disclosed it in its terms and conditions. When Dispute Rules Content Pack for Mastercard is installed, the answer determines whether a chargeback for reason code \(RC\) 4853 is eligible.


-   **Price-discrepancy question for Visa consumer disputes**

An existing question, originally used under the Processing Errors dispute category, has been repurposed for consumer disputes filed under reason code 13.3 \(Not as Described or Defective Merchandise/Services\). Dispute agents are asked "Is the dispute due to the difference between the quoted price and the actual charges made by the merchant?" and cardholders are asked "Is the dispute related to a discrepancy between the quoted price and the actual charges made by the merchant?" A Yes answer marks the dispute ineligible for reason code 13.3, since a price discrepancy is not a valid basis for that reason code under the Visa Chargeback Guide.


</td></tr><tr><td>

Financial Services Operations Core

</td><td>

-   **Claim Summarization component update**

Generate AI-powered claim summaries using the Now Assist context menu \(NACM\) component, which replaces the deprecated AI Summary Card component on the Claim Workspace and Claim Summary pages. Claims processors and adjusters can continue to generate an AI-generated summary of a claim: processors see it on the Claim Summary page, and adjusters see it on both the Claim Workspace and Claim Summary pages.

Share a generated summary to the claim's work notes from the summary component. Selecting **Share** opens an editable work notes dialog, where adjusters can edit the summary text before selecting **Save to work notes**.

Activate the Claim Summarization skill configuration for the summary component to appear on either page. If the skill configuration isn't active, the component doesn't display on either page.


</td></tr><tr><td>

Financial Services Operations Integration with Visa

</td><td>

-   **Processing code field values updated for Visa compliance**

Updated `processing_code` field choice values in the Financial transaction table align with current Visa data field specifications. Existing choice values have been updated with refined labels and descriptions; new choice values have been added to support additional transaction types.

The updated choice values include:

    -   `00` — Goods/Service Purchase - Debit
    -   `01` — Cash Disbursement \(for example, withdrawal or cash advance\) - Debit
    -   `02` — Adjustment - Debit
    -   `10` — Account Funding / Card Absent Account Funding
    -   `11` — Quasi-Cash Transaction - Debit or Internet Gambling Transaction
    -   `19` — Fee Collection - Debit
    -   `20` — Return of Goods - Credit, Credit Transaction, Credit Voucher
    -   `22` — Adjustment - Credit
    -   `26` — Original Credit
    -   `28` — Activation and Load / Load
    -   `29` — Funds Disbursement - Credit
    -   `30` — Available Funds Inquiry
    -   `39` — Eligibility Inquiry
    -   `50` — Bill Payment \(U.S. only\)
    -   `53` — Payment \(U.S. only\)
    -   `72` — Activation \(POS\)
Dispute agents and administrators see these updated labels and descriptions in transaction UI drop-down lists and data entry forms. No action is required on existing transactions. Existing choice values not listed here remain unchanged.


-   **Updated questionnaire field labels and validation**

Renamed the question "Explain why credit presented does not apply" to "Provide the Transaction Identifier\(s\) or Acquirer Reference Number\(s\) and the Transaction Date that the credit\(s\) was applied to and why the credit\(s\) does not resolve the Dispute," and renamed "Certification that the merchant facilities were withdrawn" to "Certification that the facilities were withdrawn." The Name field is no longer required, and Key Factors now accepts up to 200 characters.

-   **Updated Spoke action wiring for new questionnaire fields**

Added the Date facilities were withdrawn and Date cardholder checked out from hotel fields to the `Submit Dispute Questionnaire` and `Look up Dispute Details Response Parser` spoke actions, and added CE Transaction Details as a read-back field on `Look up Dispute Details Response Parser`. See [Financial Services Card Operations 2026 September Monthly release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/release-notes/financial-services-card-operations-rn.md) for the corresponding questionnaire questions.


</td></tr><tr><td>

Firewall Audits and Reporting

</td><td>

-   **Firewall rule compliance dashboard**

The compliance dashboard now includes additional metrics and visualizations to provide better insights into firewall rule compliance status and trends over time.


</td></tr><tr><td>

Goal Framework

</td><td>

-   **[Target type editable when actuals exist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/change-target-type-gf.md)**

You can change a target's **Type** after actual values have been recorded. Previously, the **Type** field became read-only once a target had progress. A confirmation message appears before the change is applied, and if you cancel, the **Type** goes back to its original value. Changing the **Type** clears the target's actual value and percent complete. The exceptions are changes between two Maintain types and changes to or from Milestone.

-   **[Type and unit of measure stay in sync](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/target-types-gf.md)**

Choosing a target **Type** sets a matching unit of measure:

    -   **Milestone**: Sets the unit of measure to Yes/No, or keeps a custom qualitative unit if one is already selected.
    -   **Maximize**, **Minimize**, or a Maintain type: Restores the last quantitative unit you used, or sets Count \(\#\) if there isn't one.
The **Type** list always shows all six types. The same pairing also applies to targets created or updated through imports or APIs.


</td></tr><tr><td>

Goal Framework for SPM

</td><td>

-   **[Target breakdown regeneration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/target-breakdowns-gf.md#section-target-breakdowns-maintain-types)**

Target breakdowns adjust to changes in a target's dates or final target value, and recorded actuals are kept:

    -   Moving the start date later removes the breakdowns before the new start date. The remaining breakdowns keep their planned targets and actuals.
    -   Moving the start date earlier adds breakdowns for the new periods, with the same planned target.
    -   Shortening or extending the end date removes or adds the matching breakdowns.
    -   Changing the final target value updates the planned target of every breakdown and recalculates status and progress.
-   **[Target type changes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/change-target-type-gf.md)**

Change the **Type** of a target after actual values are recorded, without deleting and recreating the target. When you change the type from Maximize to Minimize, or from Maximize to a Maintain type:

    -   The total actuals to date stay the same and are placed in the latest target breakdown period.
    -   Planned values are recalculated for the new type.
    -   Progress and attainment are recalculated using the new type's logic.
A warning appears before you save the change. The change is recorded in the audit history.

-   **[Number field in the target list view](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/target-form.md)**

The **Number** field appears as a link in the actual value automation list view. That list view opens when you view targets in Core UI.


-   **Default check-in frequency**

New quantitative targets now default to **Quarterly** check-in frequency to create target breakdowns when you save the target. You can change the check-in frequency before creating the target.

-   **Improved status labeling**

The **None** status option is now labeled **No status** for goals, strategic priorities, target progress, and target breakdowns, providing clearer communication about goal status states.


</td></tr><tr><td>

Health Log Analytics

</td><td>

-   **ServiceNow Otto®**

ServiceNow Otto® is the new AI experience brand. This change is reflected in the name of ServiceNow products, including Health Log Analytics. Your product entitlements remain unchanged. Check your entitlements to determine whether you have access to specific features.

-   **Health Log Analytics migration to LogDB for log storage**

Health Log Analytics stores short-term troubleshooting logs in LogDB instead of Elasticsearch for significantly better compression and faster ingestion. No action is required from your organization. Alerts generated before the transition still appear, but their surrounding logs aren't available because existing log data remains in Elasticsearch. New logs generated after the switch populate normally. If you notice anything unexpected, contact ServiceNow support.


</td></tr><tr><td>

Healthcare Operations

</td><td>

-   **Healthcare Orchestration roles**

Two new roles, `sn_hco_orc.loc_contributor` \(Healthcare Orchestration Location Contributor\) and `sn_hco_orc.loc_manager` \(Healthcare Orchestration Location Manager\), can now be assigned directly as a service organization member's type.

Location-level and hospital-level visibility and management permissions for orchestration functions resolve automatically, without requiring the Care Team Agent Manager role as a workaround.


-   **User criteria for Care Team Mobile quick actions**

Six out-of-the-box user criteria records ship with Care Team Operations so admins can control which Care Team Mobile quick-action icons each care team role sees, instead of building their own user criteria from scratch.


</td></tr><tr><td>

ITOM AIOps

</td><td>

-   **Configure alert grouping automation with AI from Alert Automation pages**

Launch the AI agent for alert grouping directly from Alert Automation pages. Select **Configure with AI** to open the ServiceNow Otto panel with a pre-populated prompt that guides rule creation.

-   **Assign AI Specialists to all groups**

Assign the AI Specialist to the new **All Groups** option to let it handle alerts from every assignment group. Previously, only the **Add specialist to specific group\(s\)** option was available, which limited the specialist to the groups you chose.


-   **Event Management Connectors**
    -   **Support for Datadog Work Items**

Configure Datadog Work Items to listen to events using the Datadog connector. Datadog Work Items are also named as Cases.

    -   **Enhanced Dynatrace Event connector**

Dynatrace Event connector enhanced to support the new third generation Dynatrace workflow.

    -   **Use of Fluent-based code and ServiceNow SDK**

Event Management Connectors app now uses Fluent-based code and the ServiceNow SDK for AI-native development and faster releases.


-   **Express List mode switching without searching**

Change the Express List view between **Essential** and **Extended** mode independently of any search parameter. The list updates immediately to reflect the selected mode, and when you add a search value, results return according to the already-selected mode.


-   **Credential setup for push connectors**

Select or generate a credential—Basic, API key, or OAuth—directly in the setup form, with API key now added as a new option. You configure the inbound endpoint in one place, without provisioning credentials elsewhere.


</td></tr><tr><td>

ITSM MCP Server

</td><td>

-   **Changes to the ITSM MCP Server tools**
    -   You need the sn\_mcp\_server.viewer role as the base role to access ITSM MCP server.
    -   The **sn\_itsm\_mcp\_server.incident.get\_details** and **sn\_itsm\_mcp\_server.incident.modify** incident tools are available to both fulfillers and requesters.
        -   As a fulfiller, you can use the **sn\_itsm\_mcp\_server.incident.modify** tool to also escalate incidents.
        -   As a requester, you can use the **sn\_itsm\_mcp\_server.incident.get\_details** to check the status of a specific incident.
    -   The **sn\_itsm\_mcp\_server.requester.add\_comment** tool has been renamed to **sn\_itsm\_mcp\_server.request.modify**.
        -   As a requester, you can use the **sn\_itsm\_mcp\_server.request.modify** tool to add customer-visible comments to the requested items.
        -   As a fulfiller, you can use the **sn\_itsm\_mcp\_server.incident.modify** to add customer-visible comments to incidents.

</td></tr><tr><td>

Identity

</td><td>

-   **Role masking in Now Assist AI agents**

Use role masking for AI agents and agentic workflows to limit the inherited roles during tool execution, verifying that AI agents run with restricted privileges, minimizing potential security risks and helping prevent unintended actions.

-   **Restrict the Conditional Script Writer group from assignment group selection on Scripting Governance Tool**

The Conditional Script Writer group can no longer be selected as the assignment group on any task or incident based — through the user interface with the base system configuration.

-   **Federated ID**

Choose any unique field — not just User ID — as the identifier in a federated ID criteria for the User table, as long as the criteria includes at least one unique field for generating federated ID.


</td></tr><tr><td>

Impact

</td><td>

-   ****

Defects and UI improvements are resolved across all assessment steps, including Overview, Assess, Review, Prioritize, and Action Plan. Additional UI changes include:

    -   Domain categories in the Assess Maturity questionnaire display in a reorganized layout with updated task labeling for clearer navigation during assessments.
    -   The target-setting step in the Prioritize and Target decision table uses a consolidated decision table with an improved UI for specifying target values.
-   **[Platform Health](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/platform-health-idi.md)**

On-demand definition scans complete in under one minute on average per instance, reducing wait times for Scan Engine operations.


-   **[Accelerator catalog](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/accelerator-catalog.md)**
    -   Success Readiness Assessment changed to Success Foundation Review.
    -   UX Accelerators moved from Architecture to the Technical sub-catalog.
    -   AI Readiness Assessment moved from Architecture to the Technical sub-catalog.
    -   Tuneup Your IT Asset Management changed to Tuneup Your ITSM Asset Management.
    -   Jumpstart Your App Engine changed to Jumpstart Your App Deployment Governance.
-   **[Platform Health](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/platform-health-idi.md)**
    -   Exception workflows in update set scans provide multiple governance improvements.
    -   Assign a dedicated exception approver role for governance separation.
    -   Control which finding levels are eligible for exception reasons, as an instance administrator.
    -   Access update set origin tracking on all scan findings.
    -   View the captured update set data that contains the violating code whenever a full or delta scan runs and produces a finding.
    -   Full-scan scope updates so only definitions explicitly configured for single-finding-per-table scanning are included.
    -   The Scan Engine Properties page now displays a dedicated warning when the company code is unset, with a link to the system property for resolution.
-   **[Value management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/impact-in-platform-business-outcomes.md)**

Access Hardware Asset Management \(HAM\) and Software Asset Management \(SAM\) functionality through a single, unified ITAM app, grouped under IT Asset Management. All previously collected data and configuration is carried over with no manual reinstallation, reconfiguration, required during the upgrade.


</td></tr><tr><td>

Incident Management

</td><td>

-   **Incident manager role changes**

The inherited itil role is now removed from the incident manager \[incident\_manager\] role and replaced with the incident\_write role. The is applicable only for the zboot instances. This change restricts access to incident records only, aligning permissions with the intended scope of the role and reducing unnecessary access to unrelated process areas.

-   **Major incident manager and communication plan manager role changes**

The major incident manager \[major\_incident\_manager\] and communication plan manager \[sn\_comm\_management.comm\_plan\_mgr\] roles no longer inherit the itil role. Instead, the roles inherit the sn\_incident\_write, sn\_problem\_write, sn\_change\_write, sn\_request\_write granular roles from the ITSM Roles plugin \(com.snc.itsm.roles\). This is applicable only for the zboot instances.

For the upgrade instances, the itil role remains inherited. Additionally, the sn\_incident\_write, sn\_problem\_write, sn\_change\_write, and sn\_request\_write granular roles are added if the ITSM Roles plugin \(com.snc.itsm.roles\) is installed.

-   **Communication plan viewer role changes**

The sn\_dex\_desktop.notification\_template\_admin role is now removed from the communication plan viewer \[sn\_comm\_management.comm\_plan\_viewer\] role and added to the sn\_incident\_write role when ITSM Roles plugin \(com.snc.itsm.roles\) is installed. In case, ITSM Roles plugin \(com.snc.itsm.roles\) is not installed, the sn\_dex\_desktop.notification\_template\_admin role is added to the itil role. These role changes are applicable only for the zboot instances.

-   **Itil role check removal from comm\_channel create and write ACLs**

The itil role reference check is now removed from the comm\_channel create and write ACLs. Create and access to the communication channel definition in the incident communication tasks is based on the commTaskGr.state.canWrite script and if you have the following roles:

    -   Communication plan manager \[sn\_comm\_management.comm\_plan\_mgr\]
    -   Communication plan admin \[sn\_comm\_management.comm\_plan\_admin\]
    -   Task communication management admin \[sn\_tcm\_admin\]
    -   ITSM granular roles such as sn\_incident\_write and the user assigned to the incident communication task and plan.
-   **Auto close resolved incidents behavior changes**

The resolved incidents are now automatically closed after a specific number of business days instead of calendar days. You can use configure the number of business days using **Number of days \(integer\) after which Resolved incidents are automatically closed. Zero \(0\) disables this feature** \[**glide.ui.autoclose.time**\] property. This changes helps the maintaining the internal organizational policies.


</td></tr><tr><td>

Kubernetes Visibility Agent \(KVA\)

</td><td>

-   **Kubernetes resource dependency views**

Resource details pages now include enhanced Dependency Views that show relationships between Kubernetes resources and related configuration items. The improved visualization helps administrators understand service dependencies and troubleshoot issues more effectively.


</td></tr><tr><td>

L1 IT Service Desk AI Specialist

</td><td>

-   **Catalog variable collection and messages**

The L1 IT Service Desk AI Specialist now fills catalog item variables from the incident and the caller's details and shows requesters what it already captured, so requesters answer fewer questions. It also now uses dynamic response authoring for L1 IT Service Desk AI Specialist Catalog submission responses. Default instructions are provided so the agent composes each message fresh instead of relying on a fixed template.


</td></tr><tr><td>

LEAP

</td><td>

-   **Hide archived automation opportunities**

Automation opportunities \(AOs\) from an earlier GAF \(Global Automation Framework\) run are now hidden by default. Previously, old AOs with resolution steps remained visible in the workspace after remapping. It was difficult to distinguish actionable AOs from old ones. After a GAF re-run, the old AOs are archived and no longer appear on the homepage. The artifacts of archived AOs are mapped to relevant new AOs.

-   **LEAP value dashboard expansion**

The LEAP value dashboard now surfaces metrics for all automation outcome types along with existing playbook data. New sections display Ansible execution counts, agent-hours saved, and top playbooks by tickets resolved, KB article creation counts and top contributing clusters, and problem record \(PRB\) creation counts and top clusters. A summary at the top of the dashboard breaks total automation activity and savings attribution by outcome type such as LEAP playbooks, Ansible playbooks, KB articles, and PRBs, each with a trend indicator. The dashboard also displays ServiceNow Otto consumption data to track the consumed per action.


</td></tr><tr><td>

MCP for Strategic Portfolio Management

</td><td>

-   **[Role-based tool access](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/exploring-spm-mcp-server.md)**

Control which SPM MCP server tools each user can run based on their assigned roles. Each tool is mapped to the SPM roles required to use it, and the MCP Server Console enforces that mapping through role-based access control.

-   **[Tool annotations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/exploring-spm-mcp-server.md)**

The SPM MCP server tools include annotation hints, such as title, readOnlyHint, and destructiveHint, in the tools/list response as defined by the MCP specification. AI assistants use these hints to apply the correct permission policies, so read-only tools are no longer treated as potentially destructive by default. Administrators can review and configure the annotations for each tool in the MCP Server Console.


</td></tr><tr><td>

Mobile Platform

</td><td>

-   **Android app build request form**

Meet Google's new Android security requirements for developer verification and app registration using the updated build request form and pipeline. The form now includes a developer verification section where you provide your snippet, and the pipeline automatically embeds it in your APK or generates a verification APK for manual registration.


</td></tr><tr><td>

Next Experience

</td><td>

-   **Now Assist &gt; ServiceNow Otto® announcement**

ServiceNow Otto introduced AI on the platform. As that experience has evolved, there's a new name for the experience. ServiceNow Otto® is the conversational AI platform integrated into ServiceNow workflows. It provides agentic capabilities, supports multimodal interactions across web, mobile, and messaging channels, and enables autonomous orchestration for cross-system workflows.

-   **ServiceNow Otto® onboarding slide added**

Next Experience onboarding now opens with a ServiceNow Otto slide. The slide appears only when the Generative AI Controller plugin \(sn\_generative\_ai\) is active on the instance. After a user selects “Got it,” the slide doesn’t appear again.


</td></tr><tr><td>

Next Experience Components

</td><td>

<table id="table_data_visualizations"><thead><tr><th>

Chart

</th><th>

Enhancement

</th></tr></thead><tbody><tr><td>

Appointment calendar

</td><td>

-   Apply the selected date format to all dates that display
-   Hide the time duration from the calendar header and appointment slot pills
-   Display the start and end time in each appointment slot pill

</td></tr><tr><td>

Bar

</td><td>

Enhanced data table \(including Pareto charts\)

</td></tr><tr><td>

Box plot

</td><td>

Enhanced data table

</td></tr><tr><td>

Bubble

</td><td>

-   Duplicate an existing data source to avoid re-entering custom filter conditions.
-   Enhanced data table

</td></tr><tr><td>

Calendar

</td><td>

-   Freeze section headers in a view
-   Scroll-based view data refresh
-   Add custom label and icon for calendar events
-   Reorder and hide event details such as time and description
-   Design token support

</td></tr><tr><td>

Dial

</td><td>

Update the data visualization in real time

</td></tr><tr><td>

Gauge

</td><td>

Update the data visualization in real time

</td></tr><tr><td>

Geomap

</td><td>

Enhanced data table

</td></tr><tr><td>

Heatmap

</td><td>

Enhanced data table

</td></tr><tr><td>

Indicator Scorecard

</td><td>

"Follow breakdown relation" provides the user with a list of defined breakdown relations based on the breakdown they choose.

</td></tr><tr><td>

Pie/Donut

</td><td>

Enhanced data table

</td></tr><tr><td>

Pivot table

</td><td>

Duplicate an existing data source to avoid re-entering custom filter conditions

</td></tr><tr><td>

Resizable panes

</td><td>

Pane position layout

</td></tr><tr><td>

Schedule recurrence

</td><td>

-   Create recurring events using voice or text input with generative AI support for pro plan users.
-   Update the event day automatically based on the event start date

</td></tr><tr><td>

Single Score

</td><td>

Update the data visualization in real time

</td></tr><tr><td>

Time Series

</td><td>

-   Compare multiple time periods "period over period" using the 'Compare period over period' setting available in the Config, Date Range section. When active, separates a data set into individual data sets and separates graphics that overlap in the chart. For area, line, spline, and step.
-   In addition to stacked columns and side-by-side columns, the normalized columns chart variation for comparing the relative balance of a series when the actual magnitude is secondary.
-   Duplicate an existing data source to avoid re-entering custom filter conditions
-   Data visualization chart migrated from Xenolith to Highcharts library. Charts are rendered by an updated charting engine, with no change to your existing charts, configurations, and data sources.
-   Visually refreshed charts and interaction improvements:
    -   Legend pagination
    -   Hover over legend item to highlight corresponding series in the chart
    -   Legend pagination
    -   Improved separation and readability of columns in charts
-   Enhanced data table

</td></tr></tbody>
</table>

</td></tr><tr><td>

Operational Resilience

</td><td>

-   **Pending updates displayed in the banner**

The pending updates for the DRIR case are displayed in a banner within the workspace.

-   **Decimal precision for DORA monetary values**

Monetary value fields now support up to two decimal places. Previously, only zero or negative values were accepted, with all monetary values defaulting to zero. Values greater than zero are no longer rounded down to zero during download.

-   **CSV download only references applied filters when selecting all records**

When a filter is applied to a list and users select all records for CSV download, only the filtered records are included. Previously, all records were downloaded regardless of the applied filter.

-   **Impact analysis correctly resolves Profile records**

Previously, impact analysis failed to resolve entities when a scheduled job processed GRC Profile records directly. This issue has been fixed. Impact analysis now correctly resolves Profile records in Operational Resilience and entity resolution completes as expected for all record types.

-   **Rank 1 supply chain records update automatically when a contract's service provider changes**

If you change the service provider on a DORA contract record, the associated Rank 1 supply chain records update automatically. The records reflect the new provider or recipient.

-   **Excel export for DORA Functions requests no longer fails on large datasets**

Exporting a Functions-type Excel drop-down download and upload request no longer fails when drop-down fields reference large CMDB or reference tables. Results are capped at 10,000 records per drop-down field.

-   **Parent record navigation added to DORA third-party and contract records**

A reference field is available on DORA third-party and third-party engagement records. Use it to navigate back to the originating contract record after arriving from a related list. Previously, there was no way to return to the parent contract or company record from these pages.

-   **Notice period fields accept a value of zero**

The notice period fields \(`B_02.02.0100` and `B_02.02.0110`\) now accept a value of `0`. Previously, a value of `0` was rejected as if the field were empty.


</td></tr><tr><td>

Operational Sustainability Management

</td><td>

-   **Enhanced content generation in Document Designer**

With Document Designer version 23.0.3, you can create HTML-based scripted columns for content blocks in your reports.


-   **[Threshold rating recalculation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/environmental-social-governance/thresholds-for-metrics.md)**

With GRC: Metrics version 23.1.2, threshold ratings and breach status are recalculated when you edit a threshold, delete a threshold, reopen a metric data task, or move it to the Estimated state. Ratings also update when you save or override a metric data value.


</td></tr><tr><td>

Performance Analytics

</td><td>

-   **[Create indicators on Workflow Data Fabric tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/data-fabric-tables-zcc.md)**

Create classic automated indicators on external data via Workflow Data Fabric. Use Workflow Data Fabric tables in indicator sources just as you would any other facts tables.

-   **Intraday scores supported on indicators with Data snapshots enabled**

If you enable Data snapshots on an existing classic automated indicator, you can collect intraday scores on the data snapshots indicator.

-   **Manage and troubleshoot your Data snapshots jobs more easily**

You now are provided with new estimates and more log information:

    -   Time estimates before a job starts
    -   Progress percentages for first-day mining, changes loader, and delta mining jobs
    -   Logs include the next scheduled run timestamp after incremental job completion

</td></tr><tr><td>

Platform Analytics experience

</td><td>

-   **[URL filter parameters for inline dashboards](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/url-filter-parameters.md)**

External pages and UI Builder pages can now pass filter values to Platform Analytics inline dashboards and the Visualization Designer using URL parameters. The feature introduces a standard mechanism that accepts filter payloads in `encodedQuery` format, validates and maps them to filter state, and applies them when the dashboard or visualization loads. Supported filter types include choice and Boolean. Deep links and drill-down workflows that previously relied on Classic or Core UI URL-based filtering are now supported in Platform Analytics experiences.

Copying a dashboard link now includes active filter state in the URL using the format `/unified-filters-param/filterId:value1,value2`, removing the back-end dependency on the `par_dashboard` filter record.

-   **[Updated creation flow for dashboards and data visualizations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/common-dashboard-tasks.md)**

The creation flow for Platform Analytics dashboards and data visualizations now clearly surfaces Next Experience as the recommended path. Core UI creation remains available for users who need it. The updated flow applies when the system properties `com.snc.par.coreui.dashboard_create.enabled` and `com.snc.par.coreui.report_create.enabled` are set to `true`. Instances where migration is complete and Core UI creation is inactive aren't affected. A new informational modal for data visualization creation has been added. The create flow now routes Core UI dashboard creation to the `pa_dashboard` record form and Core UI report creation to the Report Designer.

-   **[Configurable list view for drilldowns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/dv-chart-interactions.md)**

Dashboard and report designers can now select which list view opens when users drill down to data using the **Go to Data View** chart interaction. The configuration option is available in the **Chart Interaction** section of the Visualization and Dashboard Designers. Designers can specify a view from the `sys_ui_view_list` table, providing flexibility to target different views for different roles or use cases. Tooltip text in the visualization now dynamically reflects the configured destination — showing the data source name for **Go to Data View** interactions and the page name for **Go to URL** interactions. The **Go to URL** interaction now redirects in the same browser tab.

-   **Export quality improvements**
    -   A system property enables or disables the export button globally. A second property accepts a comma-separated list of roles permitted to export when the first property is enabled. When the roles list is empty, export is available to all users. This applies to on-demand export at both the dashboard and data visualization level, including client-side export.
    -   The export modal now includes a documentation link for supported and unsupported components. It also provides options to enable or disable sending exports via email and displays improved error messages after export failures. UI controls in export modals have been updated from toggles to check boxes.
    -   PDF exports now correctly apply the selected orientation \(landscape or portrait\) for list-type visualizations. Previously the orientation setting was recognized in the UI but exports always rendered in portrait.
    -   Users can select specific dashboard tabs to include when exporting to PDF, consistent with existing PPT export tab selection. Dashboards with applied filters respect the filter state in PDF exports.
    -   Scheduled export now supports additional file types and page format options that were previously available in Core UI but missing from the scheduled export UI. Day-of-week scheduling options \(Monday to Friday\) are now available. Core UI reports are hidden from the scheduled export library page.
-   **[Dashboard PDF export improvements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/export-pae-dashboard-ppt.md)**

Platform Analytics dashboard PDF and PowerPoint export includes the following improvements:

    -   You can now select which dashboard tabs to include when exporting to PDF, consistent with the existing tab selection available for PPT export.
    -   When exporting a dashboard to PDF, you can choose whether to apply or exclude the active dashboard filters in the exported output.
    -   Visualizations in exported PDF and PPT files now follow the layout order displayed on the dashboard, with the top layout rendered first and widgets ordered left to right.
    -   Filters, images, and headings are now included in dashboard PDF exports. Previously these components were excluded because `par_metadata` records were not present for them.
    -   When a dashboard contains only unsupported components, the export now returns a meaningful error message rather than an empty PDF.
    -   Dashboards containing only list visualizations no longer trigger an unnecessary export server call.
-   **[Library page bookmark icon theme alignment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/bookmark-dashboard-ac.md)**

The bookmark icon in the Dashboard library page and the Data Visualization library page now renders in the applied theme color, consistent with the Indicators library page. Previously the bookmark icon displayed in blue regardless of the active theme.


</td></tr><tr><td>

Portfolio Planning

</td><td>

-   **[Roadmap export range](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/export-portfolio-plan-status-to-ppt-portfolio-planning-workspace.md)**

The maximum date range for exporting a roadmap to PowerPoint increased from 1 year to 3 years, within the start and end dates of the portfolio. The exported timescale adjusts to the range you select: months for a range of 1 year or less, and quarters for a range longer than 1 year.

-   **[Program portfolio plan enhancements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/program-portfolio-plan-ppw.md)**
    -   **Program details** — Select the information icon next to the program name to view the planning item types, program timeline, and program manager.
    -   **Program value for new items** — When you create a demand or project from a program portfolio plan, the **Program** field is prefilled with that program.
    -   **Prioritization default layout** — The default **Prioritization** view shows the Rank, Name, Planning state, Planning item type, Status, Cost status, Resource status, Schedule status, Scope status, Percent complete, Primary goal, and Owner columns.
    -   **Goals tab** — Program portfolio plans include the **Goals** tab, which shows all primary and non-primary goals linked to the planning items in the plan, along with goals assigned directly to the program.
    -   **Public views** — Any user who can access a program portfolio plan can create and update its public views. Previously, only plan editors could create or update public views.
-   **[Resource assignment offsets when converting a demand to a project](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/data-migrated-from-demand-project-dw.md)**

When a demand with resource assignments is converted to a project, assignment offsets are recalculated against the project's schedule, which counts only the working days defined in the project schedule, instead of the demand, which has no schedule and counts every calendar day.

-   **[Execution URL on planning item demands](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/update-execution-urls-for-existing-demands.md)**

Run the **Update Demand Planning Item Execution URL** scheduled job to update the execution URLs on your existing demands to the latest format.


-   **Financials**

Added in-context help \(hover info icons\) on the Financials page widgets, explaining how the key fields like Budget, EAC, Planned Cost, Actuals, Return, ROI, and NPV are calculated.

-   **[Program planning updates and enhancements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/program-portfolio-plan-ppw.md)**
    -   **Programs menu addition** — A new Programs menu has been added to the workspace as L2 menu, positioned below Portfolio Plan. This menu lists every program in your portfolio and provides single-click navigation to each program's enhanced planning view.
    -   **Role-based access for program planning** — Users with the sn\_align\_core.ap\_read\_only role have read access to program plans \(where they already have program-level read access\). Users with the sn\_align\_core.apw\_admin and program manager roles receive full access to create, update, and manage planning items within program plans.
-   **[Summarize demands with the demand summarization skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/summarize-demands-in-ppw.md)**

The default trigger is not set to **Automatic** for demands in any state. You can select how you want the skill to be triggered for any state.


</td></tr><tr><td>

Pricing Management

</td><td>

-   **Extended product life cycle support in Price Management**

Validate pricing setup against catalog changes earlier in their life cycle by extending product offering life cycle visibility into Price Management.

    -   Previously, price list lines, cost book lines, and attribute adjustments could reference only Published product offerings. Now, when extended product life cycle states are enabled, they can also reference offerings in the In Test and Staged states. This enables the pricing admin to create price lists and define rules in pricing matrices for offerings that are in the In Test and Staged states.
    -   Previously, context variable rules and pricing matrix rules could filter on Published product offerings only. Now, they can also filter on offerings in the In Test and Staged states.
-   **[Delta price calculation for consolidated renewal lines](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/renewal-pricing-ramped-products.md)**

Calculate delta price more accurately for renewal lines that consolidate multiple contract line items affected by upsells or downsells. The calculation now uses the prior contract value over the subscription's full previous term, together with the new renewal price including uplift, to determine the delta price amount.


</td></tr><tr><td>

Privacy Management

</td><td>

-   **Data lineage map UI**

When you select the relationship line between two nodes in the data lineage map, a side pane opens with the relationship details, where you can edit or remove a relationship.

-   **Node location fields in the hierarchy modal**

The hierarchy modal now includes node location fields. The Define relationship step includes a **Primary node location** field, and the Relationship details step includes a **Related node location** field.

-   **Data subject selection in hierarchy relationships**

Privacy admins can enable data subject selection for custom relationship types in a hierarchy by modifying the sn\_privacy.relationship\_involving\_data\_subjects system property.

-   **Applicable scope tab in a privacy assessment task**

The Applicable scope tab on the assessment task record replaces the former Outcomes tab. It lists the control objectives and risk statements that have been scoped to the processing activity through manual addition, automation rules, or AI-assisted recommendations.

-   **External-facing Personal Data Rights \(PDR\) form layout**

The external-facing PDR form layout is updated to support mobile screens.


</td></tr><tr><td>

Process Mining

</td><td>

-   **Content packs availability changed**

Access content packs for the following automatically when the corresponding application plugin is active and the associated table is present:

    -   IT Service Management
    -   Customer Service Management
    -   HR Service Delivery
    -   Strategic Portfolio Management
    -   Security Incident Response
    -   Field Service Management

</td></tr><tr><td>

Product Catalog Management

</td><td>

-   **Catalog filtering for the eligible catalog-category hierarchy**

Retrieve only the catalog you need when loading the eligible catalog-category hierarchy. Previously, the response included the complete hierarchy for all eligible catalogs, even when a catalog was specified in the **selectedCatalog** parameter. Now, when you specify a catalog, the response includes only that catalog and its category hierarchy. The default value, `allCatalog`, still returns the complete hierarchy.

-   **Optional product details in catalog search results**

Reduce response size and processing time by requesting only the product details your integration needs.

    -   Previously, the search response didn't include product offering characteristics or categories. Now, you can include the **additionalFields** object in the request to return the product offering family, characteristics, and categories, for example, `"additionalFields": {"family": true, "characteristics": true, "categories": true}`. These fields aren't returned unless you request them.
    -   Previously, the search response included the **productOfferingFamily** object by default \(added in the September 2026 release\). Now, it's returned only when you set **family** to `true` in the **additionalFields** object. If your integration reads the product offering family from the search response, update your requests to include it.
-   **Improved search result ranking in the product catalog**

Reindex the product catalog to help agents and customers find the exact product offering they're looking for, even when several similar offerings are indexed. Previously, a product offering could rank lower in search results than other offerings that only referenced it, such as a bundle that included it. Now, admins can reindex the product catalog so that the offering that most closely matches a search term ranks highest.


-   **[Minor updates to published product offerings and specifications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/minor-updates-published-offerings-specs.md)**

Simplify updates to published product offerings by adding optional characteristics and optional child offerings without creating a new offering version. Set a future effective date for the child-offering relationship to control when the child becomes available for new purchases or order changes. Previously, these updates required a new version of the parent offering and replication of its related configuration.

Previously, turning on the transient setting for a published product offering required creating a new version. Now, turning it on doesn't require a new version. Turning it off still requires one.

-   **[Product catalog sort options](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/using-product-catalog.md)**

Previously, the sort drop-down menu in the product catalog was hidden unless AI Search was turned on. Now it is always available, and includes a new Display Order option that sorts by your configured display order. The Relevancy option still appears only when AI Search is on.

-   **Product Catalog Management data model changes**

New columns have been added to the Product Catalog Management tables to enable new life cycle states, channel-specific launch dates, and control the display sequence of offerings in the catalog.

    -   Value column has been added to the Distribution Channel \[sn\_prd\_pm\_distribution\_channel\] table. It canonically maps the channel name resolved from the context variable or the Sales CRM entity header to the sys\_id \(Name\) in the Distribution Channel \[sn\_prd\_pm\_distribution\_channel\] table.
    -   State column on the Product Offering \[sn\_prd\_pm\_product\_offering\] table now includes In Test and Staged values, sequenced between Draft and Published. A new Approval state column has been added, with values Not yet requested \(default\), In Review, Approved, Rejected, and Recalled. A new Active channels column has also been added. It's a read-only, comma-separated list of distribution channel references that stores the channels the offering is currently available on, so catalog search can filter on availability without a table join.
    -   State column on the Specification \[sn\_prd\_pm\_specification\] table now includes In Test and Staged values, sequenced between Draft and Published.
    -   Effective from column has been added to the Product Offering Relationship \[sn\_prd\_pm\_product\_offering\_relationship\] and Specification Relationship \[sn\_prd\_pm\_specification\_relationship\] tables.
    -   Order column has been added to the Catalog Category \[sn\_prd\_pm\_catalog\_category\_relationship\] and Product Offering Catalog \[sn\_prd\_pm\_product\_offering\_catalog\] tables.
    -   Display Order column has been added to the Product Offering \[sn\_prd\_pm\_product\_offering\] table
-   **Product offering family in catalog search results**

Identify the product offering family of each search result without a separate lookup. Previously, the catalog search REST API response didn't include the product offering family. Now, the response returns the **productOfferingFamily** object for each product offering, whether or not AI Search is turned on.


</td></tr><tr><td>

Product Support for Technology

</td><td>

-   **[Technology Account 360](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/proactive-service-exp-workflows/technology-account-360.md)**

Use the Technology Account 360 to get a unified view of customer or partner account details combining account health, financial, product usage, and open tasks.


</td></tr><tr><td>

Project Portfolio Management

</td><td>

-   **Portfolio Insights card order**

The AI Insights panel now displays insight cards in a fixed order based on prominence and impact: Projects at risk, Budget Overrun, Cost Variance, Items past planned end date, Delayed start, and Planned versus approved misalignment. Review the most critical financial and schedule risks first.

-   **Insight explanations in Portfolio Insights**

Each card in Portfolio Insights now includes an info icon. Select the icon to open a popover with a plain-language explanation of what the insight measures and how it's calculated, so you can interpret the insight without leaving the panel.

-   **[Navigation to Project Workspace in Next Experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/t_CreateAProject.md#steps_cmz_5wd_tw)**

View and access Project Workspace in Next Experience when you access project workspace from the All navigation menu.

-   **[Summarize demands with the demand summarization skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/demand-summary-demand-classic.md)**

The default trigger is not set to **Automatic** for demands in any state. You can select how you want the skill to be triggered for any state.


</td></tr><tr><td>

Project Workspace

</td><td>

-   **[Managing projects with Project Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/use-projects-pw.md)**

On project tasks with logged actuals, you can't change the Planned start or move the end date earlier than the last logged actual, whether you edit dates directly or a dependency recalculates them. When the Actual start and end dates are present, the restriction applies to them. This keeps the tasks and assignments in sync.

-   **[Preview attachments and manage excel files with dedicated prompts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/generate-project-using-ai-pw.md)**

When you generate a project plan, a preview of the attachment now appears before you proceed. This matches the existing behavior of [generating tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/generate-tasks-using-ai-pw.md). Excel attachments are now processed with a dedicated prompt tailored to tabular data, separate from word, pdf, and powerpoint attachments. This applies when generating a project plan or inserting tasks.


-   **UI options for RIDAC**

RIDAC section is expanded by default to view AI-Identified Risks and RIDAC.

-   **UI options for Financials**
    -   Added in-context help \(hover info icons\) on the Financials page widgets, explaining how the key fields like Budget, EAC, Planned Cost, Actuals, Return, ROI, and NPV are calculated.
    -   Added **Recalculate costs** option to recalculate the planned costs and planned benefit when labor rates or budget reference rates change.
-   **UI options for Project Workspace**
    -   Added **Export status report** in the more options menu in the Details page.
    -   Added **Save as new template** and **Project Diagnostics** in the more options menu in the Planning page.

</td></tr><tr><td>

Public Sector Digital Services

</td><td>

-   ****

Starting with the September 2026 release, Gemma 4 joins our growing portfolio of open-weight models available through Now LLM Service. The latest industry advancements are available alongside sovereignty-focused options. All models are hosted and governed by ServiceNow with the same infrastructure and data protections. Older models will remain available for existing published AI skills, agents, and agentic workflows, but will no longer be available for new development or configuration. For details, see the [KB3066214: ServiceNow Otto Model Upgrades](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3066214) article in the Now Support Knowledge Base.

-   **Now Assist &gt; ServiceNow Otto® announcement**

ServiceNow Otto introduced AI on the platform. As that experience has evolved, there's a new name for the experience. ServiceNow Otto® is the conversational AI platform integrated into ServiceNow workflows. It provides agentic capabilities, supports multimodal interactions across web, mobile, and messaging channels, and enables autonomous orchestration for cross-system workflows.

-   **[Enhancements to Grants Management: Program Setup](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/psds-using-grants-management-playbook.md)**
    -   [Establish the Grant Program Budget in Grants Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/psds-config-gmp-pgr-budget.md)

Use the restructured Program Budget step that is now organized into three sections: Program Budget, Budget Categories, and Award Allocation. Grant Program Managers can select from three award models—Single Award, Multiple Equal Awards, or Multiple Variable Awards—with budgets automatically derived from the Awards category. Real-time calculations update the Budget allocated and Balance left fields as you enter category percentages. This enhancement prevents completion until all of the program budget is allocated across the categories.

    -   [Configure program lifecycle stepper](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/psds-config-gmp-pgr-lifecycle-stepper.md)

Disable the six-step grant program lifecycle stepper at the instance level, reducing ambiguity about grant program state. By default, the stepper indicating the Preparing Program, Accepting Proposals, Evaluating, Awarding, Post-Award, and Closed states is hidden in the Grant Program record page. Admins can enable it if required for deployments that follow a batch or competitive grant lifecycle. When turned off, program state is conveyed through existing status fields.

-   **[Enhancements to Grants Management: Proposal Playbook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/psds-using-grants-management-playbook.md)**
    -   [Screen a grant proposal in the Grants Proposal Playbook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/psds-using-gmp-grant-proposal-screen.md)

Flag and route a document back to the applicant while reviewing the proposal details in the screening step. The document persists in the Flagged section with all metadata intact. Grant program managers and Grant program directors can reverse the flag by selecting the reset status icon to move it back to Requires Verification with no data loss. Select Request Documents at the bottom of the Verify Documents screen to route flagged documents back to applicants automatically. This action creates a case task assigned to the applicant, sends a notification in the applicant portal prompting re-upload, and changes the document status to Pending Resubmission. After the applicant uploads the corrected document, the Upload Additional Documents activity closes and you can continue verification, maintaining a complete audit trail throughout the process.

-   ****

The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets, and create your own
Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.


-   **[Enhancements to Investigative Case Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/psds-explore-inv-case-management.md)**
    -   Render all entities, evidence, tasks, and related cases as an interactive knowledge graph with Case Link Analysis Data Visualization, and set any node as the home node to re-map relationships. Add ​control and transparency to entity updates with Master Index Versioning, creating an immutable, time-stamped snapshot of that entity that cannot be altered, and a complete audit trail – who changed it, when they changed it, what changed. Update entities across all cases or create a case-specific version for an investigation for a unified, searchable record of every entity across your cases \(Persons, Vehicles, Organizations, Locations, Property, Firearms\).

    -   Manage field operations and view/create investigative tasks directly within the case context using the Tasks tab, found within an ICM investigative case record. Use the `Create Work Order` button to allow a case to be escalated to an Field Service Management work order without leaving the ICM workspace and context-switching between systems.

    -   Added lead management capabilities for lead submission, intake, triage, assignment, tracking, and investigation workflows, including portal experiences for submitting and monitoring leads.

-   **Use Page Patterns with GOV.UK Developer Toolkit**
    -   The GOV.UK Developer Toolkit has been updated to include three page patterns that confirm to GOV.UK Design System guidelines:

        -   Question pages: forms experience where the questions are surfaced one by one on the UI
        -   Step by step navigation: Where a user can view all the steps required to complete a task in one view
        -   Confirmation page: Where a user sees a confirmation page after submitting their answer to the last question
-   ****
    -   The Identity Provider Integration plugin \(sn\_idp\_integ\) allows provides ServiceNow developers with the data model foundation to develop OpenID Connect \(OIDC\) integrations that authenticate and verify constituent identities through approved government OpenID Connect \(OIDC\) providers — ID.me \(US\), myID \(Australia\), GOV.UK One Login \(UK\) — replacing email-only identification. It standardizes and enhances the identity verification process, delivering a provider-neutral OIDC framework for capturing and storing key identity provider data, including identity provider issuer, identity provider ID, and assurance level from OIDC providers on top of the existing Multi-Provider SSO \(MPSSO\) plugin.


-   **Now Assist &gt; ServiceNow Otto® announcement**

ServiceNow Otto introduced AI on the platform. As that experience has evolved, there's a new name for the experience. ServiceNow Otto® is the conversational AI platform integrated into ServiceNow workflows. It provides agentic capabilities, supports multimodal interactions across web, mobile, and messaging channels, and enables autonomous orchestration for cross-system workflows.


-   **[Enhancements to Grants Management: Program Setup](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/psds-using-grants-management-playbook.md)**
    -   [Establish the Grant Program Budget in Grants Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/psds-config-gmp-pgr-budget.md)

Use the restructured Program Budget step that is now organized into three sections: Program Budget, Budget Categories, and Award Allocation. Grant Program Managers can select from three award models—Single Award, Multiple Equal Awards, or Multiple Variable Awards—with budgets automatically derived from the Awards category. Real-time calculations update the Budget allocated and Balance left fields as you enter category percentages. This enhancement prevents completion until all of the program budget is allocated across the categories.

    -   [Configure program lifecycle stepper](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/psds-config-gmp-pgr-lifecycle-stepper.md)

Disable the six-step grant program lifecycle stepper at the instance level, reducing ambiguity about grant program state. By default, the stepper indicating the Preparing Program, Accepting Proposals, Evaluating, Awarding, Post-Award, and Closed states is hidden in the Grant Program record page and admins can enable it if required for deployments that follow a batch or competitive grant lifecycle. When turned off, program state is conveyed through existing status fields.

-   **[Enhancements to Grants Management: Proposal Playbook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/psds-using-grants-management-playbook.md)**
    -   [Screen a grant proposal in the Grants Proposal Playbook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/psds-using-gmp-grant-proposal-screen.md)

Flag and route a document back to the applicant while reviewing the proposal details in the screening step. The document persists in the Flagged section with all metadata intact. Grant program managers and Grant program directors can reverse the flag by selecting the reset status icon to move it back to Requires Verification with no data loss. Select Request Documents at the bottom of the Verify Documents screen to route flagged documents back to applicants automatically; this action creates a case task assigned to the applicant, sends a notification in the applicant portal prompting re-upload, and changes the document status to Pending Resubmission. Once the applicant uploads the corrected document, the Upload Additional Documents activity closes and you can continue verification, maintaining a complete audit trail throughout the process.



-   **Updated Coral theme**

The Coral theme has been improved to enhance usability across web, mobile, and portal experiences that use Next Experience and Core UI:

    -   A fully overhauled color system for smoother gradients and better contrast.
    -   Softer outlines and more rounded components for a new, accessible look.
    -   A significantly improved dark mode with deeper blue tones for reduced eye strain.
    -   New AI gradient styles and subtle animations to highlight intelligent features.
    -   Smarter focus behavior that reduces visual clutter for mouse users.
-   **[Enhancements to Constituent Service Portals](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/portals-psds-exploring.md)**

UI Enhancements have been made to all Public Sector Digital Services constituent portals by replacing legacy widgets \(for example, portal banners, data lists\) with standardized, CSM Configurable Widgets and components. The update verifies backward compatibility, migration guidance, usage analytics, and provide training for admins, and also enables dynamic data rendering, and better filtering across service flows.

-   **[Enhancements to Investigative Case Management Configurable Case role-based access](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/psds-config-icm-assign-user-roles-responsibilities.md)**

Extend write access and restrict read access to cases based on Assigned Office, Assignment Group, or both to allow automatic case access alignment with organizational units without managing the Teams tab manually.

-   **[Enhancements to Document Screening](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/psds-ai-skill-doc-screening.md)**

Applicants can select a specific document type from a pre-configured, category-scoped list during upload, stored on the document record and displayed read-only to internal agents in both portal and Workspace views.


-   ****

Starting with the September 2026 release, Gemma 4 joins our growing portfolio of open-weight models available through Now LLM Service. The latest industry advancements are available alongside sovereignty-focused options. All models are hosted and governed by ServiceNow with the same infrastructure and data protections. Older models will remain available for existing published AI skills, agents, and agentic workflows, but will no longer be available for new development or configuration. For details, see the [KB3066214: ServiceNow Otto Model Upgrades](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3066214) article in the Now Support Knowledge Base.

-   ****

The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets, and create your own
Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.


</td></tr><tr><td>

Purchase Order Management

</td><td>

-   **[Automated purchase order exception creation from emails](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/convert-emails-to-exceptions.md)**

Previously, emails containing multiple intents would create only a single case for the dominant intent and default to a Universal Request for others. Now each identified intent triggers its own case creation, eliminating manual conversion work.

-   **[Changes to the Purchase Order Confirmation Data Model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/po-confirmation-line-table.md)**

The Confirmation source and Status fields in the Purchase Order Confirmation \[sn\_poem\_po\_confirmation\] table have new values: AI Agent and Draft Retracted.


</td></tr><tr><td>

Regulatory Change Management

</td><td>

-   **Entity filtering in the risk assessment modal**

When you initiate a risk assessment from a regulatory alert, the Evaluate risk impact dialog box includes a **Filter by** drop-down. Use **Entities by Impacted Areas** or **Entities by Recommendations** to scope your entity selection.

-   **Regulatory alert summarization in all regulatory alert states**

Generate a regulatory alert summary in any state. The AI-generated summary includes new sections such as alert overview, scope, actions and outcomes, and velocity analysis. Select **Share to alert summary** to save the summary to the alert record.

-   **Enhanced input data for regulatory alert summarization**

The regulatory alert summarization skill uses additional input data to generate a summary. New input fields include enriched insights, coordinator details, functional domain, and alert type, among others. The skill also incorporates data from the impacted areas and regulatory change tasks related lists.

-   **Regulatory alert number on the Details tab of an alert**

The regulatory alert number is displayed on the Details tab of a regulatory alert.

-   **New column on regulatory assessment tasks**

The Regulatory assessments tab in **GRC Tasks** displays the regulatory alert for an assessment in the Record column.

-   **Compliance library items traced to their corresponding regulatory action tasks**

Compliance library records, including citations, control objectives, controls, and policies, feature a Regulatory action tasks tab that links the action tasks linked to these records. This enables you to navigate from the impacted area record in the compliance library directly to its action task in RCM. Similarly, from the Action tasks tab of a regulatory alert, you can navigate to the impacted citations, control objectives, controls, or policies.

-   **Email notification redirection to workspace**

Email notification links for RCM records redirect users to the Compliance Workspace instead of the classic environment.


</td></tr><tr><td>

Resource Management Workspace

</td><td>

-   **[End assignment UI option](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/end-resource-assignment-rmw.md)**

Added **End assignment** option in row context menu for assignments.


</td></tr><tr><td>

Retail

</td><td>

-   **Template item column for store plan cases**

New cases that are created from a store plan or a store audit plan will populate the **Template item** column, while the **Origin** field will no longer be populated for newly created cases.

**Note:** If you have a custom implementation that relies on the **Origin** field to determine the template item that a case was created from, those use cases will need to be updated accordingly.


</td></tr><tr><td>

SPM Enterprise-Wide Deployment

</td><td>

-   **[Portfolio project partition coverage](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/supported-tables-for-partition-ewd.md)**

Partition protection extends to the relationships between portfolios and projects, stored in the Portfolio Project \[`pm_m2m_portfolio_project`\] table. Users see portfolio-project relationships only for the partitions that they can access.


-   **[Restrict system administrator access to partitioned data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/configure-admin-access-to-all-partitions.md)**

Restrict system administrators from accessing partition-protected data through a new configurable system property. The system property **sn\_spm\_ewd.allow\_admin\_access\_to\_all\_partitions** controls whether system administrators can access all partitions by default. By default, this property is set to `false`, which means system administrators must have the appropriate partition role to access partition-protected data.

Users with the system administrator or sn\_spm\_ewd.ewd\_admin role can configure this property. This enforces strict data governance policies at all security levels and prevents unintended access to sensitive partition data. When partition access restrictions apply, all user roles, including system administrators, are subject to uniform partition role validation.


</td></tr><tr><td>

Sales CRM for Telecommunications

</td><td>

-   **[Legal name persistence during account creation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/account-details-form-fields.md)**

Legal name entered during account creation is now correctly persisted. Previously, the value was mapped to a database field that did not exist.

-   **[Order integrator role no longer blocks other roles from creating consumers and locations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/components-installed-with-order-management.md)**

Fixed an access control issue where the order integrator role's create permissions on Consumer and Location records inadvertently blocked other roles, such as CSM Agent, from creating those records.


</td></tr><tr><td>

Security Incident Response

</td><td>

-   **[Exploring Security incident quality assessment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/na-sir-quality-assessment.md)**

Customize or regenerate entire draft reports or specific sections within it, before you share it with stakeholders.


</td></tr><tr><td>

Self-service and omnichannel engagement for CSM

</td><td>

-   **[Usage calculation of self-service experiences](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/csm-portal-user-sessions-timeouts_2.md)**

Get more accurate portal usage data with an updated analytics definition that eliminates double-counting of guest user sessions.


</td></tr><tr><td>

Service Exchange \(formerly Service Bridge\)

</td><td>

-   ** and **

Upgrade consumer connections from Resource Owner Password Credentials \(ROPC\) to Client Credentials OAuth by using Upgrade Auth on the connection record, to authenticate connections as an application rather than of with a user's password, improving security and compliance. Run the upgrade once from the provider instance to update both instances, keep the connection active, and avoid off-boarding and re-onboarding the consumer.


</td></tr><tr><td>

Service Operations Workspace for ITSM

</td><td>

-   **Default Attached knowledge related list**

The attached knowledge related list now appears in the Related records tab by default, if any Knowledge article attached to the incident record.


</td></tr><tr><td>

Service Reliability Management

</td><td>

-   **Open alerts count for technology management services**

For technology management services on the **Services** page, the counts for **Open alerts** and **Open critical alerts** now include alerts from related CIs, up to three levels deep. To view the individual alerts and their associated CIs, select the service and then select the **Related alerts** tab.


</td></tr><tr><td>

Service Test Management

</td><td>

-   ****

Add characteristics directly to Test Groups, map product specifications to the Test Group that should run. Propagate those values to Test Definitions through attribute mapping and decomposition rules. The right tests run with the correct inputs for each product, reducing manual configuration and errors.


</td></tr><tr><td>

ServiceNow AI Platform core feature

</td><td>

-   **Improved cross-scope access security enforcement for getRefRecord\(\) JavaScript API**

The cross-scope security mechanism has been strengthened, supporting consistent application of authorization rules. For more information, see [KB3142985: Cross-Scope Access Security Enhancement \(Glide Element API: getRefRecord\(\)\)](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3142985).

-   **Default value of glide.sys.fencing.restricted\_caller\_access.invalidation\_mode is SCRIPT\_ENGINE**

The default value of the glide.sys.fencing.restricted\_caller\_access.invalidation\_mode system property changed from DB\_LISTENER to SCRIPT\_ENGINE. When the property is set to SCRIPT\_ENGINE, and an update set contains a script with changes, the script engine doesn't invalidate associated RCA records. To enable a database listener that monitors update set commits on source code tables and invalidates RCA records at the time of the commits, set the value to DB\_LISTENER.


-   **AI indicators updated for form fields**

AI indicators for form fields in Core UI and configurable workspaces now support AI color gradients and have been updated to reflect the latest ServiceNow Otto name and iconography.

-   **TinyMCE version 8.3.0 upgrade**

The HTML editor in Core UI and configurable workspaces is upgraded from TinyMCE version 6.8.2 to version 8.3.0.

-   **Text pattern configuration in the HTML editor**

Text patterns in the HTML editor can now be turned on or off using the **glide.ui.html.editor.textpatterns** system property.

-   **Configurable choice field empty option labels**

Configure choice fields to display either None or --None-- for empty options using the **glide.ui.choice.display\_none** system property.

-   **Base cross-scope access on the latest source code updates**

Control how the system invalidates Restricted Caller Access records when a source code record, such as a script include, in a cross-scope access table is committed in an update set with the glide.sys.fencing.restricted\_caller\_access.invalidation\_mode system property.

**Note:** In the Brazil Early Availability and Brazil Patch 1 releases, the default value is DB\_LISTENER. Beginning with the Brazil Patch 2 release, the default value is SCRIPT\_ENGINE.

-   **ECMAScript 2021 \(ES12\) JavaScript mode supports additional scripting features**

Use additional scripting features in applications or scripts that use the ECMAScript 2021 \(ES12\) JavaScript mode.

-   **JavaScript engine updated with changes from the Rhino engine**

The JavaScript engine on the ServiceNow AI Platform was updated to incorporate changes from the open-source Rhino JavaScript engine.

-   **Configure row threshold for exports to Excel**

Configure the row limit for exports to Excel using the properties **glide.export.xls.max.rows.per.sheet** and **glide.export.xlsx.max.rows.per.sheet**.


</td></tr><tr><td>

ServiceNow Arc

</td><td>

-   **Auto mode for each chat**

Users choose **Standard** or **Auto** approval for each chat in ServiceNow Arc from the message box, and set a default approval mode in **Settings** &gt; **Approvals** for new chats and background runs, such as scheduled tasks.

To make auto mode available, administrators turn on the Auto Mode capability \(**auto\_approval**\), which is off by default, and set tool gates to **Auto Approval** for the tools that auto mode can cover.

-   **Microsoft 365 connector permissions**

Users set each Microsoft 365 connector capability to **Allow**, **Ask me first**, or **Deny**. With **Ask me first**, an approval card asks the user to allow or deny the action every time it runs, and auto mode never skips it.

Administrators set the upper limit with the **Approval gate** field on each connector scope in a policy. Users can choose only a stricter setting, and capabilities the policy limits show **Set by your organization**. Microsoft 365 scopes turned off on the instance now appear in the list. Existing policies keep their behavior, and the audit log records policy changes and Microsoft 365 write actions.

-   **Clearer approvals**

Approval cards in ServiceNow Arc now name the action and describe what's at stake, such as what the action changes or sends and whether it can be undone. For a command under a hard gate, the card names the command that triggered it.

**Allow always** is renamed **Always Allow**, and standing approvals in **Settings** &gt; **Approvals** describe the whole group of actions they cover.

Accessing a folder outside the workspace asks for approval with a soft gate that offers **Always Allow**, unless an approval pattern in the policy applies a hard gate to that call.

-   **Schedules management**

Users create scheduled tasks from **Schedules** in the ServiceNow Arc sidebar or through chat. They can start from a blueprint or a custom reminder, and select **Reminder only** to get a notification instead of running a task.

The list shows every schedule, whether created in chat or in **Schedules**. Users can search the list, run, duplicate, edit, pause, or delete any schedule, and see when it last ran and when it runs next.


</td></tr><tr><td>

ServiceNow Lux Lab for VS Code

</td><td>

-   **Page collections renamed page variants**

Page collections are now called page variants. The **Lux: Create page variant** command and its prompts and messages use the new name. When you create a page variant in a new project, the extension saves it in the `_variants` folder. In projects that already have a `_collections` folder, the extension continues to create page variants in `_collections`.


</td></tr><tr><td>

ServiceNow Otto for Contract Management Pro

</td><td>

-   ****

Contract document-based conversational search queries now return all matching results instead of 10 results. Use Show more option to load the remaining results.

-   ****

In conversational search, introduced an option to preform in-document search after the contract metadata search results are available.


</td></tr><tr><td>

ServiceNow Otto for IT Service Management \(ITSM\)

</td><td>

-   ****

When the AI agent searches for similar change requests, it now returns only changes whose quality score meets a minimum threshold. The quality scores come from the AI Change Quality Scores table. If none of the similar changes meet the threshold, the results include changes that don't have a quality score yet.


</td></tr><tr><td>

ServiceNow Otto for Software Asset Management \(SAM\)

</td><td>

-   **Software Spend Detection Core UI**

The Software Spend Detection feature is no longer available in the Core UI. Software Spend Detection is now accessible from the Software Asset Workspace under License operations. Existing imports and spend transactions created in the Core UI are now accessible from the Software Asset Workspace.


</td></tr><tr><td>

ServiceNow Otto for Virtual Agent

</td><td>

-   ****

-   **[Enable additional chat features](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/additional-chat-features.md)**

The **Prioritize AI agents during skills discovery** option is available when configuring additional chat features. Because all assistants now use agentic orchestration by default, AI agent skills are available during skills discovery. Turning on this option gives AI agents priority over other assets \(such as knowledge bases and Q&amp;A modules\) when the assistant discovers skills. If your assistant has overlapping skills \(for example, a knowledge base article and an AI agent that both answer the same question\), this setting lets you decide which one is prioritized, so you can steer users toward the AI agent experience instead of a static article.

-   **[ServiceNow® Otto for Virtual Agent system properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/nava-sys-props.md)**

The **sn\_nowassist\_va.assistant\_personalization** system property is removed from the admin experience. This property previously let admins show or hide chat personalization options \(agent persona, tone, and response length\) when [branding an assistant](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/brand-assistant.md). By default, all settings are shown.


-   ****

Role-based configuration is no longer stored or managed within Assistant Designer.

-   **[Upload files improvements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/upload-documents-na-va.md)**

Upload up to 10 files or 50 MB for the following file types: PDF native, PDF OCR, Word, PPTX, Excel, CSV, TXT, JPEG, PNG for premium chat in ServiceNow Otto for Virtual Agent and Otto panel.

-   **[Updated ServiceNow Otto processing animation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/nava-integrated-chat.md)**

View an updated ServiceNow Otto processing animation.


</td></tr><tr><td>

ServiceNow Studio

</td><td>

-   ****

Update sets and changes linked to source control both display in the Changes tab, with clear tracking paths for both options and support for simultaneous update set and source control use.


-   ****

ServiceNow Studio user preferences and settings have moved from the top right corner to the bottom left corner of the interface. View what's new in ServiceNow Studio, access command palette and keyboard shortcut options, and update preferences.

-   **App summary generation moves to an agentic architecture**

ServiceNow Otto for app summary generation now uses an AI agent to generate application summaries. This change moves the App summary generation from a skill-based architecture to the AI agent orchestration model.

With this release, users who install the App summary plugin receive the App Summary AI agent.

The App Summary AI agent is turned off by default after plugin installation to help avoid unexpected charges. An administrator must enable the agent in AI Agent Studio before users can generate application summaries.

The end-user experience remains the same. The change affects only the underlying architecture, which now uses an agentic model instead of the earlier skill-based model.

-   **Deployment tab**

The **Deployment** tab, with lists of all update sets, applications, and deployment requests, has moved from the home page to the activity bar as a separate tab.


</td></tr><tr><td>

ServiceNow Vault

</td><td>

-   **Vault onboarding email design**

The Vault onboarding email uses an updated template design.


-   **ServiceNow Otto name change**

ServiceNow Otto introduced AI on the platform. As that experience has evolved, there's a new name for the experience. ServiceNow Otto® is the conversational AI platform integrated into ServiceNow workflows. It provides agentic capabilities, supports multimodal interactions across web, mobile, and messaging channels, and enables autonomous orchestration for cross-system workflows.

-   **Role masking in the Access Observer and Field Encryption workflows**

The security\_admin role isn't part of the sn\_vault\_console.vault\_console\_admin role. To use the Access Observer and Field Encryption agentic workflows, assign the security\_admin role to sn\_vault\_console.vault\_console\_admin users, and then elevate to security\_admin.

-   **Default policy naming**

Default policies provisioned for field encryption, data privacy, Zero Trust Access, and Log Export Service are prefixed with Vault by Default, so you can distinguish policies that ServiceNow provisioned from policies your organization created.


</td></tr><tr><td>

Smart Assessment Engine

</td><td>

-   **Create an assessment template category**

With Smart Assessment version 23.0.2, the assessment template category form includes two new fields: **QB category roles**, which controls access to the question banks associated with the category, and **Allow user delegation**, which lets users delegate their assessments in the category.

-   **UX improvements to assessment questions and responses**
    -   Drop-down list question — With Smart Assessment Designer version 23.0.5, reopening a drop-down list question now shows all response options again, not just the ones you previously selected.
    -   Reference question search — With Smart Assessment Core version 23.0.2, for single-select and multi-select reference questions, when a table has more than 10 matching records, select the search icon to browse the full set. This replaces the default behavior of showing only the first 10 records.
    -   Default focus when opening or reopening an assessment — With Smart Assessment Core version 23.0.2, the view defaults to the assessment instructions, if configured, or the first question of the first section or subsection. This applies even if you, a collaborator, or response automation has already answered later questions.

</td></tr><tr><td>

Software Asset Management

</td><td>

-   **Gain clearer visibility into SAP HANA user license types with the renamed License classification column**

The **Named user type** column is renamed to **License classification** in the SAP System Users \[samp\_sap\_system\_user\] table for improved visibility into SAP HANA user license types and entitlement reconciliation. The column appears on the SAP System Users related list of software models created for SAP S/4HANA products.

-   **Manage SAP S/4HANA Cloud, Public Edition entitlements with the renamed User Subscription metric**

The **Full Usage Equivalent** license metric for SAP S/4HANA Cloud, Public Edition is renamed to **User Subscription**, aligning with SAP's updated naming for this edition. The Full Usage Equivalent metric continues to apply to SAP S/4HANA Cloud, Private Edition. The calculation logic is unchanged.

-   **Manage software models with clearer licensing terminology**

Understand licensing scope at a glance from the renamed column in the Software Model \[cmdb\_software\_product\_model\] table. The **License all installs accessed by clients** column is renamed to **License all installs**. The new name reflects that all installs meeting the software model's conditions are licensed, not only those tied to client access records.

-   **Removal candidates tab replaced with the Reclamation tab in the License usage view**

The **Reclamation** tab in the License usage view on the Software Asset Workspace presents a consolidated view of reclamation candidates across all publishers, SaaS integrations, installed software, and reconciliation flows.


</td></tr><tr><td>

Strategic Planning

</td><td>

-   **Target import check-in frequencies**

Target import accepts Period as a check-in frequency. Import rejects a check-in frequency that the active calendar does not allow and shows a message that states the reason.

-   **[Duplicate target behavior](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/create-a-copy-of-a-goal-or-target.md)**

When you duplicate a target, the copy keeps the source check-in frequency only if the active calendar supports it. The copy gets new breakdowns from the active calendar and never copies the source breakdowns. The source target does not change.

-   **[Find the open sprints that block Planning Interval completion](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/start-or-complete-iteration-in-eap.md)**

When open child sprints prevent you from completing a Planning Interval, you must know which sprints to close. The completion alert now lists every open sprint by team. Each sprint links to the Agile board of the team for Agile Development 2.0 sprints. CWM teams link to the CWM board. All other sprints link to the EAP Backlog of the team.


-   **[Switching a team to Kanban in EAP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/switch-agile-team-to-kanban-in-eap.md)**

Sprints that aren't complete are cancelled when you set a team's Planning methodology to Kanban, including the team's current sprint. Completed and cancelled sprints aren't changed, and work items stay assigned to the sprints that were cancelled. A team connected to Collaborative Work Management \(CWM\) can't be switched to Kanban while it has active or planned sprints.

-   **[Planning methodology on existing teams in EAP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/scrum-and-kanban-teams-in-eap.md)**

Each existing agile team is assigned a planning methodology when you upgrade: Scrum if the team or its configuration has a business calendar, Kanban if neither has one. Because Kanban teams don't show sprint controls, review any team created without a business calendar and set its Planning methodology to Scrum if that team plans in sprints.

-   **[Automatic status for Maintain type targets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/automatic-status-calculation-targets-spw.md)**

Automatic status calculation extends to Maintain type targets. Each breakdown period is set to Green when its actual meets the Maintain condition and Red when it doesn't.

-   **[Target type changes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/target-types-overview.md)**

Change a target's type after actuals are recorded, without deleting and recreating the target. Actuals to date are kept and recorded in the latest breakdown period. Planned values are recalculated for the new type, and progress is evaluated under the new type's logic. A confirmation message appears before the change is applied, and selecting **Cancel** keeps the previous type and data. Type changes are captured in the audit history.

-   **[Unit of measure on targets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/set-targets-for-goal-egm.md)**

Select the target type before the unit of measure when you create a target. Milestone sets the unit of measure to Yes/No, and Maximize, Minimize, and Maintain types default to Count. Later type changes keep the unit of measure you selected. If it isn't valid for the new type, you're prompted to pick one. This applies to the target modals in Enterprise Goals and portfolio plan goals, and to inline editing in the target list.

-   **[No status label](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/components-installed-with-alignment-planner-workspace.md)**

The None status choice is labeled **No status** for goals, strategic priorities, targets, target progress, and target breakdowns.

-   **[RIDAC by portfolio and program](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/portfolio-plan-ridac-spw.md)**

View decisions alongside other RIDAC items for portfolios and programs when you open RIDAC from the Strategic Planning Workspace RIDAC menu. The **Portfolio Risks** and **Program Risks** menus are renamed **RIDAC by Portfolio** and **RIDAC by Program**.

-   **[Target generation for Maintain-type targets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/generate-targets-for-goal.md)**

Generate Maintain above, Maintain below, and Maintain constant targets with ServiceNow Otto target generation skill for goals that sustain a level rather than move toward one, such as platform uptime, a cost ceiling, or team headcount. When a Maintain type is suggested, the target modal shows the threshold value and hides the start value field. Review the suggested type and change it if needed before you save the target.

-   **[Goal insights for Maintain-type targets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/generate-insights-for-goal-spw.md)**

ServiceNow Otto goal insights include Maintain-type targets \(Maintain above, Maintain below, and Maintain constant\) when summarizing goal progress.

-   **[Resource assignment offsets when converting a demand to a project](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/data-migrated-from-demand-to-project-dw.md)**

When a demand with resource assignments is converted to a project, assignment offsets are recalculated against the project's schedule, which counts only the working days defined in the project schedule, instead of the demand, which has no schedule and counts every calendar day.

-   **[Execution URL on planning item demands](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/update-execution-url-for-demand-spw.md)**

Run the **Update Demand Planning Item Execution URL** scheduled job to update the execution URLs on your existing demands to the latest format.

-   **[Roadmap export range](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/export-a-portfolio-plan-to-powerpoint-strategic-planning.md)**

The maximum date range for exporting a roadmap to PowerPoint increased from 1 year to 3 years, within the start and end dates of the portfolio. The exported timescale adjusts to the range you select: months for a range of 1 year or less, and quarters for a range longer than 1 year.

-   **[Program portfolio plan enhancements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/program-portfolio-plan-spw.md)**
    -   **Program details** — Select the information icon next to the program name to view the planning item types, program timeline, and program manager.
    -   **Program value for new items** — When you create a demand or project from a program portfolio plan, the **Program** field is prefilled with that program.
    -   **Prioritization default layout** — The default **Prioritization** view shows the Rank, Name, Planning state, Planning item type, Status, Cost status, Resource status, Schedule status, Scope status, Percent complete, Primary goal, and Owner columns.
    -   **Goals tab** — Program portfolio plans include the **Goals** tab, which shows all primary and non-primary goals linked to the planning items in the plan, along with goals assigned directly to the program.
    -   **Public views** — Any user who can access a program portfolio plan can create and update its public views. Previously, only plan editors could create or update public views.

-   **Financials**

Added in-context help \(hover info icons\) on the Financials page widgets, explaining how the key fields like Budget, EAC, Planned Cost, Actuals, Return, ROI, and NPV are calculated.

-   **[Enterprise Agile Planning configuration options](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/create-eap-configuration.md)**
    -   The **Have unique calendars** option is renamed to **Allow unique cadence for each team**.
    -   An EAP admin can now clear the **Allow unique cadence for each team** option after selecting it. Selecting the option doesn't change the calendars or the iterations that already exist.
    -   The **Scrum Sprint** planning calendar type is available by default, alongside **Planning Interval** and **Sprint**.
-   **[Iteration dates in Enterprise Agile Planning](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/edit-pi-sprint-iteration-details-in-eap.md)**
    -   The **Enterprise agile calendar entry** field on the Enterprise agile iteration \[sn\_apw\_advanced\_eap\_iteration\] table is no longer mandatory, which supports iterations that carry their own start and end dates. A fix script makes the field optional when you upgrade.
    -   Users with the `sn_apw_advanced.eap_user` role can set the start date and the end date while they create an iteration. They can change those dates afterward on an iteration that doesn't follow a planning calendar entry. However, changing the dates on an iteration that follows a planning calendar entry still requires the `sn_apw_advanced.eap_scrum_master` role.
-   **[Sprint sync with Agile Development 2.0](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/sync-eap-and-agile-2.md)**
    -   Sprints that don't follow a planning calendar entry now sync to Agile Development 2.0 by using the start date and the end date on the iteration.
    -   Changing the start date or the end date of an iteration now updates the dates on the corresponding Sprint in Agile Development 2.0.
-   **[Program planning updates and enhancements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/program-portfolio-plan-spw.md)**
    -   **Programs menu addition** — A new Programs menu has been added to the workspace as L2 menu, positioned below Portfolio Plan. This menu lists every program in your portfolio and provides single-click navigation to each program's enhanced planning view.
    -   **Role-based access for program planning** — Users with the sn\_align\_core.ap\_read\_only role have read access to program plans \(where they already have program-level read access\). Users with the sn\_align\_core.apw\_admin and program manager roles receive full access to create, update, and manage planning items within program plans
-   **[Summarize demands with the demand summarization skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/summarize-demand-in-demand-workspace.md)**

The default trigger is not set to **Automatic** for demands in any state. You can select how you want the skill to be triggered for any state.


</td></tr><tr><td>

Subscription Management

</td><td>

-   **Account-level cloud capacity storage pool**

Cloud capacity storage is now pooled at the account level rather than capped at the instance level. This means your total storage entitlement can be used more flexibly, wherever it's needed across your environment.


-   **Support for Moveworks consumption tracking**

Moveworks consumption can now be measured as part of your Assist meter, following the same subscription rules as other assist-based products. For more information about the timeline and required steps for integration, see [Moveworks Assist in Subscription Management: Rollout Timeline, Customer Actions &amp; FAQ \[KB3147691\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3147691) on the Now Support Knowledge Base.


</td></tr><tr><td>

Supplier Lifecycle Operations

</td><td>

-   **[Verify bank account ownership using Relish](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/verify-banking-information.md)**

When a banking details change request is assigned to a supplier manager and they start working on it, they can verify the details using Relish.

By default, bank validation checks only the bank routing number and address details. Relish also verifies the bank account number and account ownership information when bank account ownership validation is enabled.

-   **[Conduct bulk sanction screening using Relish](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/perform-bulk-sanction-screening.md)**

When a sanction screening request for compliance verification is assigned to a supplier manager and they start working on it, they can verify the details using Relish.

Supplier managers can conduct sanction screening for multiple suppliers simultaneously using the bulk sanction screening feature.

-   **[AI driven supplier onboarding using ServiceNow Otto for SLO](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-onboarding-agentic-workflow.md)**
    -   Leverages Web search results to generate a supplier scorecard highlighting key strengths, positive indicators, and potential risk signals.
    -   If Craft is configured, the workflow leverages the Craft integration to generate a comprehensive, normalized supplier scorecard and risk assessment. It provides a structured evaluation of the supplier’s overall profile and associated risk factors.
    -   If Relish is integrated, the supplier's banking information is further validated and synchronized with Relish.

</td></tr><tr><td>

System Localization

</td><td>

-   **Improved visibility for the user's date format and time format settings.**

Date and time format settings can be edited in two locations: the user profile and the Language &amp; Region section within the user's Preferences. This update improves the visibility and availability of these important settings.


</td></tr><tr><td>

Telecommunication Network Inventory

</td><td>

-   **[Define a network model relationship](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/create-network-model-relationships.md)**
    -   Hardware models visible in Inventory Template picker: Template Managers can now select hardware models \(cmdb\_hardware\_product\_model\) from the Inventory Model picker when creating or editing an inventory template. Previously, models of this type were not visible in the picker if they were not tagged with a TNI inventory category. Hardware models created anywhere in the model catalog are now always included in the picker.
    -   Parent Model selection retained when relationship type changes: When a Catalog Manager changes the relationship type after already selecting a Parent Model, the selected model value is now retained if it is a valid model type. Previously, changing the relationship type could clear a validly selected Parent Model value.
-   **[Create an equipment model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/create-equipment-models.md)**

All model types are made visible in Model Relationship Parent Model picker: Catalog Managers can select any model type, including hardware models and product models, as the Parent Model when creating a model relationship, regardless of which relationship type is selected.


</td></tr><tr><td>

Telecommunications Customer 360

</td><td>

-   **[Billing card](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-media-technology/c360-billing-card.md)**

The Billing card in Customer 360 displays billing accounts of any Billing Account Type, including Customer Account, instead of only Company.

-   **[Party Relationship Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-media-technology/c360-prc-overview.md)**

Each node in the Relationship viewer shows its table label as a tagline, so you can identify the record type at a glance.


</td></tr><tr><td>

Telecommunications Service Operations Management \(TSOM\)

</td><td>

-   **[Fortinet discovery with large port counts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-service-ops/telecom-discovery-via-fortinet.md)**

Fortinet devices with more than 600 ports no longer fail discovery due to memory constraints. Ports are now processed in batches to prevent out-of-memory errors.


</td></tr><tr><td>

Third-party Risk Management

</td><td>

-   **Third-party and engagement element assessments**

After upgrading to version 23.0.7, you can review element-level assessments across all engagements for a third party. Element-level assessments are no longer scoped to a specific engagement. When you scope an assessment, issue, or task to an element, the **Element** field is required. This option is available only when the third party uses the Smart Assessment Engine. Third-party and engagement contacts respond to element-scoped assessments in the third-party portal the same way they respond to engagement-scoped assessments.

-   **Risk scoring for third-party elements**

After upgrading to version 23.0.7, element assessment scores roll up through relationship scores calculated from questionnaire-level evidence, replacing the previous entity-based rollup calculation. Engagement and third-party risk-area calculations include assessments sent on linked elements. Linking an element with existing assessment evidence to a new engagement calculates a risk rating for that link automatically, without requiring a new assessment.

-   **Access external and internal tasks from separate modules**

After upgrading to version 23.0.7, you can access external and internal tasks from separate modules. The Tasks module is split into **External Tasks** and **Internal Tasks** on the list page. This separates external tasks from the internal task functionality added in element collection.

-   **Expanded access to reassign Smart Assessment Engine questionnaires**

After upgrading to version 23.0.7, the TPR administrator \[sn\_vdr\_risk\_asmt.vendor\_risk\_admin\], TPR assessor \[sn\_vdr\_risk\_asmt.vendor\_assessor\], and TPR manager \[sn\_vdr\_risk\_asmt.vendor\_risk\_manager\] roles now include the sn\_smart\_asmt.reassign role. Users with these roles can reassign Smart Assessment Engine questionnaires.

-   **Decimal precision for DORA monetary values**

After upgrading the Digital Resilience Third-party Information Register application to version 23.0.3, and if you have the TPR administrator \[sn\_vdr\_risk\_asmt.vendor\_risk\_admin\] role, you can set decimal precision to `-6`, `-3`, `0`, or `2` for monetary value fields. Previously, only `-6`, `-3`, and `0` were supported. This applies to Master Template and CSV downloads. The default precision remains `0`. This change doesn't affect UI display, upload and validation, individual table downloads, or database storage.

-   **CSV download applies only filtered records when all records are selected**

After upgrading the Digital Resilience Third-party Information Register application to version 23.0.3, when a filter is applied to a list and you select all records for CSV download, only the filtered records are included. Previously, all records were downloaded regardless of the applied filter.

-   **Issue generation rules no longer create issues for hidden questions**

After upgrading to version 23.0.7, an issue generation rule that targets a question with a visibility condition no longer creates an issue when that question is isn't visible to the respondent. Previously, the rule could create an issue for a question the respondent never saw.

-   **Product model record created after SBOM document processing**

After upgrading to version 23.0.7, after a third party submits an SBOM file and processing completes, a product model record is created on the third-party record. The record is visible in the Product Models related list. A plugin dependency is added to support parallel processing.

-   **Legal person identifier validation warns instead of blocking for non-LEI/EUID codes**

After upgrading the Digital Resilience Third-party Information Register application to version 23.0.3, after a third-party service provider record with a legal person type and a non-LEI/EUID identification code is submitted, you receive a warning. The save is no longer blocked. This applies to both the Vendor Management Workspace and Excel Upload.

-   **Notice period fields accept a value of zero**

After upgrading the Digital Resilience Third-party Information Register application to version 23.0.3, the notice period fields \(`B_02.02.0100` and `B_02.02.0110`\) now accept a value of `0`. Previously, a value of `0` was rejected as if the field were empty.

-   **Data quality warnings CSV added to CSV ROI report package**

After upgrading the Digital Resilience Third-party Information Register application to version 23.0.3, the CSV report package includes a `Data_Quality_Warnings.csv` file in the `Consolidated_Reports.zip` archive. This file provides supplementary data quality checks beyond the Level 3 \(DPM\) and Level 4 \(LEI\) validations.

These warnings flag potential data inconsistencies — such as duplicate rows, missing assessments, orphaned contracts, supply chain gaps, and criticality conflicts — but don't prevent submission. Addressing them helps maintain data accuracy. Each warning includes the sheet name, row number, contract reference, and a descriptive message.

-   **Parent record navigation added to DORA third-party, third-party engagement, and contract records**

After upgrading the Digital Resilience Third-party Information Register application to version 23.0.3, a reference field is available on DORA third-party, third-party engagement, and contract records. Use it to navigate back to the related parent record after arriving from a related list. Previously, there was no way to return to the parent record from these pages.

-   **Excel export for DORA Functions requests no longer fails on large datasets**

After upgrading the Digital Resilience Third-party Information Register application to version 23.0.3, exporting a Functions-type Excel drop-down download and upload request no longer fails when drop-down fields reference large CMDB or reference tables. Results are capped at 10,000 records per drop-down field.

-   **Automated quarterly CSV download for Register of Information reports**

After upgrading the Digital Resilience Third-party Information Register application to version 23.0.3, a quarterly scheduled job \(**DORA: Quarterly CSV download**\) generates the CSV Register of Information report for the previous quarter automatically, copying settings from the most recent download request. Previously, a TPR administrator generated this report manually each quarter. The scheduled job is inactive by default; a TPR administrator \[sn\_vdr\_risk\_asmt.vendor\_risk\_admin\] can navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs** and activate it before it runs.

-   **Rank 1 supply chain records update automatically when a contract's service provider changes**

After upgrading the Digital Resilience Third-party Information Register application to version 23.0.3, and if you change the service provider on a DORA contract record, the associated Rank 1 supply chain records update automatically. The records reflect the new provider or recipient.

-   **Third party field pre-populated when creating an element from an engagement**

After upgrading to version 23.0.7, the **Third party** field is auto-populated when you create a third-party element from either the third-party record or an engagement's **Elements** tab. Previously, the field was editable and empty in both cases.

-   **Smart Assessment Engine rating scale available from workspace navigation**

After upgrading to version 23.0.7, the SAE default rating scale table is available from the Vendor Management Workspace navigation, under **Assessment Setup**. Previously, this table wasn't accessible from workspace navigation.


</td></tr><tr><td>

Threat Intelligence Security Center

</td><td>

-   **[Automated correlation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/automated-correlation-rules.md)**

Confirmed relationship rules now apply reputation checks and direction-agnostic deduplication, producing accurate source-of-traffic and destination-of-traffic relationships. Potential correlation rules are more selective and correlation requires a reputation match plus multiple shared observables.

-   **[TISC integration within SIR Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/tisc-sir-workspace.md)**

Directly link or unlink TISC entities in TISC Context tab of SIR workspace. The changes made in TISC context or TISC internal intelligence tab reflect bidirectionally.

-   **[CrowdStrike Falcon EDR integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/crowdstrike-edr-integration.md)**

Indicators sent to CrowdStrike Falcon EDR now carry "TISC Intelligence" as the source. A configuration option applies the TISC expiration time, falling back to the observable type expiration when the option is disabled. The Prevent action is supported alongside Detect.

-   **[Configure Premium Threat Feed for CrowdStrike](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/premium-threat-feed-for-crowdstrike.md)**

Ingest Vulnerability intelligence from CrowdStrike. Feed configurations are set to read-only when they're enabled, preventing changes that would disrupt an ingestion already in progress.

-   **[Review revoked MITRE tactic and technique associations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/tisc-review-revoked-mitre-associations.md)**

MITRE ingestion now provides a review queue for revoked technique-to-tactic associations that the newer MITRE ATT&amp;CK version no longer defines.


</td></tr><tr><td>

Unified Security Exposure Management \(USEM\)

</td><td>

-   **Risk rating options are no longer part of exception or deferral requests**

Changing a risk rating is no longer available from the Request Exception dialog, or from the Bulk Edit dialog by selecting **Mitigating Control in Place** as a deferral reason. Risk rating and compensating control fields have been removed from both. Use **Modify risk** or **Request risk modification**, according to your role, to change a risk rating instead for individual records or in bulk.


</td></tr><tr><td>

Vulnerability Response

</td><td>

-   **Risk rating options are no longer part of exception or deferral requests**

Changing a risk rating is no longer available from the Request Exception dialog, or from the Bulk Edit dialog by selecting **Mitigating Control in Place** as a deferral reason. Risk rating and compensating control fields have been removed from both. Use **Modify risk** or **Request risk modification**, according to your role, to change a risk rating instead for individual records or in bulk.


</td></tr><tr><td>

Zero Copy Connectors

</td><td>

-   **MySQL connector moved to Primary with Preview label**

The [MySQL](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/mysql-zcc.md) connector moved from the Community connector list to the Primary connector list. This connector is available with a **Preview** label, indicating that performance enhancements are ongoing.

-   **PostgreSQL connector moved to Primary**

The [PostgreSQL](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/postgresql-zcc.md) connector moved from the Community connector list to the Primary connector list.


</td></tr></tbody>
</table>**Parent Topic:**[Release notes summaries for Brazil features](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/release-notes/release-notes-summaries.md)


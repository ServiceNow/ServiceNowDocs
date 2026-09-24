---
title: Changes to Brazil features and products
description: Cumulative release notes summary on changes to Brazil features and products.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/rn-summary-changes.html
release: brazil
topic_type: reference
last_updated: "2026-09-23"
reading_time_minutes: 65
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

AI Agent Studio

</td><td>

-   **[New setup processes for agentic AI assets in redesigned AI Agent Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/aias-landing.md)**

The redesigned AI Agent Studio reimagines the creation and deployment processes for agentic AI assets. New features include automated evaluations built in to the application and easy creation of AI agents for automation opportunities. See [Configure AI Agent Studio settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/config-aias-settings-new.md) for how to access the previous UI.


-   **[Platform Analyze task trends agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/incident-trends.md)**

The Analyze task trends agentic workflow now includes citations for representative records associated with a pattern. Configure the workflow to include open tickets in its analysis by enabling the setting and running a Group Action Framework job to reindex with the new records.


</td></tr><tr><td>

AI Control Tower

</td><td>

-   **[Domain separation and AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/aict-domain-separation.md)**

Use AI Control Tower on a domain-separated instance. In Security, detail pages for Privileged AI agents, Dormant AI agents, Access issues, Security events detected, Agent map, Post-runtime, and AI asset security score include a Domain column that shows the domain the AI asset belongs to, or shows `global` or is empty if domain separation isn't configured. Your top recommendations is replaced by a Security events detected section on the Security dashboard, and Sensitive data metrics aren't shown for ServiceNow AI systems.

-   **[Governing AI asset security](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/gov-sec-ai-asset.md)**

Agent status is renamed to Access posture on the Security tab for an AI asset. Also, Detection time is now the first column in the list of events.

-   **[Security design-time metrics reorganized into subtabs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/gov-sec-reference.md)**

Design-time metrics are organized into three subtabs: AI security posture, AI vulnerabilities, and AI validation. If the AI Security Exposure Management plugin isn't installed, use the source dropdown to filter the metrics by source \(for example, Cisco or HiddenLayer\).

-   **[Governing AI asset security](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/gov-sec-ai-asset.md)**

On the Security tab for an AI asset, access issues and access posture metrics aren't shown for AI models because they're agent-level signals derived from agent identity and permissions. Therefore, they don't apply to AI models.

-   **[Contain AI agents manually using kill switch protocol](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/gov-sec-manage-ai-agents-using-kill-switch-protocol.md)**

AI agent containment \(kill switch\) supports retrying a failed or partial containment operation from the asset record or the agent containment list. You can also deactivate any managed AI agent directly from its asset record, whether or not it has an associated security event. AI agent containment \(kill switch\) is now available directly from an AI asset's Overview tab, not just its Security tab, for security events of any severity.

-   **[Configuring security connections](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/aict-configuring-security-connections.md)**

The Security tab under **Settings** &gt; **Integrations** is renamed to Control Enforcement Points.

-   **[Add a Gemini Enterprise Agent Platform connection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/aict-configure-gcp-vertex-ai-security-connection.md)**

The GCP Vertex AI security connector is renamed to Gemini Enterprise Agent Platform.

-   **[Agent containment list](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/gov-sec-review-kill-switch-protocol-log.md)**

The Kill Switch Protocol Log is renamed the Agent containment list, and the **View details** option on the containment banner is renamed **View containment options**. The list now includes Domain and Actions columns. Containment details now show how the containment was initiated \(Manual or Automated\) and identity and enforcement details. The list can be filtered using the All, In progress, or Contained options, which replace the previous Show all link.

-   **[Managing AI asset security reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/gov-sec-reference.md)Security dates and times shown in UTC**

Date and time values in the Security tab — including the agent containment list, the Overview tab's Dormant AI agents and Privileged AI agents details, and the Post-runtime tab's security events — are now shown in Coordinated Universal Time \(UTC\) rather than your local timezone.

-   **[AI Gateway](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/ai-gateway.md)**

Starting in the September 2026 release, AI Gateway is available in AI Control Tower.

-   **[Configuring connectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/aict-configuring-connectors.md)**
    -   The GCP Vertex AI connector is renamed to Gemini Enterprise Agent Platform.
    -   The application AI Service Graph Connector for GCP is renamed to AI Service Graph Connector for Google.
    -   The Salesforce connector is renamed to AI Connector for Salesforce.
-   **[Veza connector authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/aict-create-ai-connection-veza.md)**

The Veza connector now authenticates using OAuth 2.0. Configure an OAuth profile and alias on the platform, then select it from **Settings** &gt; **Integrations** &gt; **Connectors**. Depending on which OAuth credential is active, tokens are either issued per user and tied to user identity, or shared at the system level, replacing API key authentication as the default method. The Veza tile appears in **Settings** &gt; **Integrations** &gt; **Control Enforcement Points**.

-   **[Create Asset Task action renamed](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/gov-sec-use-events.md)**

The **Create AI Task** action, available on AI asset security events, privileged AI agents, and dormant AI agents, is renamed to **Create Asset Task**.

-   **[AI security posture metrics added and renamed](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/gov-sec-reference.md)**

On the Design-time tab in Security, AI security posture subtab, three metrics were added under **AI assets with critical findings**: **MCP servers**, **Tools**, and **System prompts**.

Several metrics on the same subtab were renamed for clarity:

    -   **Critical findings approaching remediation target** is renamed **Findings approaching remediation target**.
    -   **Critical findings with remediation overdue** is renamed **Findings with remediation overdue**.
    -   **Number of findings deferred** is renamed **Findings deferred**.
    -   **Findings by risk rating** is renamed **Posture findings by risk rating**.
    -   **Findings by OWASP LLM Top 10** is renamed **Critical findings by OWASP top ten**.
    -   **Findings by MITRE ATLAS techniques** is renamed **Critical findings by MITRE ATLAS technique**.
The **Critical findings by platform**, **Critical findings by OWASP top ten**, and **Critical findings by MITRE ATLAS technique** metrics require the AI Security Exposure Management plugin, and are no longer available in the base system.

-   **[Updated default Sampling rate and Max skill calls](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/gov-sec-configure-event-metrics.md)**

In **Settings** &gt; **Rules and templates** &gt; **Security**, the default values for Sampling rate and Max skill calls have changed to help ensure efficient, predictable analysis. If you're upgrading, your Sampling rate and Max skill calls are updated to the new defaults. Your Detection enabled setting for each metric is not affected. After upgrading, check your Sampling rate and Max skill calls settings under **Settings** &gt; **Rules and templates** &gt; **Security** and adjust if needed.


-   **[View input and output in trace details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/mon-ai-session-details.md)**

Toggle between input and output when viewing trace details.


</td></tr><tr><td>

AI Desktop Actions

</td><td>

-   **[Browser startup and tab behavior](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/na-ai-wa-access-using-nap.md)**

Browser session now opens to an empty page instead of Google's homepage. Automation actions within the same chat window now reuse the existing browser tab instead of opening a new tab for every action. A new tab opens only when a new chat session starts or you close the current tab.

-   **[Improved security for adaptive desktop actions system properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/components-installed-with-agentic-desktop.md)**

Adaptive desktop actions system properties now require appropriate read and write roles. This change prevents unauthorized users from viewing or modifying the configuration settings, while automation continues to work as expected.


</td></tr><tr><td>

AI Risk and Compliance

</td><td>

-   **[Domain separation and AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/aict-domain-separation.md)**

Domain separation is supported for AI Control Tower. Domain separation enables separation of data, processes, and administrative tasks into logical groupings called domains. Administrators can control several aspects of this separation, including which users can see and access data. For AI Risk and Compliance, domain separation isolates each domain's risk posture while letting administrators at a parent domain see and manage risk across their child domains.

-   **[Reviewing regulatory classification and compliance status](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/gov-airc-regulatory-status.md) for unmanaged AI systems**

Unmanaged AI systems now receive a risk classification and appear on the Regulatory risk classification donut chart. The risk classification is calculated based on the **Use and purpose** fields filled at the time of creating the asset and are assigned to the asset accordingly. Once the asset moves to the **Managed** state, the risk classification is revised based on updates to the **Use and purpose** fields or based on regulatory risk classification updates.

-   **Updates in [Continuous controls monitoring in the AI Risk and Compliance Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/airc-continuous-controls-monitoring.md)**

The **Save** button in the Compliance evaluation enables AI Risk and Compliance Analyst \[sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_analyst\] to maintain the configuration changes in Draft state before publishing. Additionally, the capability to specify the owner of individual compliance evaluation configurations has been introduced as a dedicated field. Assigning ownership helps introduce accountability to the rules and keep users informed who configured the rule.


</td></tr><tr><td>

Access Management

</td><td>

-   **[Explore Access Control Lists](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/exploring-access-control-list.md)**

Improve access control predictability by enforcing strict denial when none of the referenced roles referenced in an ACL exist on the instance. This behavior doesn't apply to ACLs that have a mix of valid and invalid roles. This behavior is on by default for new instances. If you upgraded to this release, use the **glide.security.acl\_with\_invalid\_roles\_strict\_deny** property to turn it on. Navigate to **All** &gt; **Access Management** &gt; **Access Findings** to find these ACLs in the Access Checks list.


</td></tr><tr><td>

Accounts Payable Operations

</td><td>

-   **[Email parser agent for APO](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/source-to-pay-operations/email-parser-agent-for-apo.md)**

The Email parser agent in Accounts Payable Operations has been updated to remove the Universal Request \(UR\) path. When an incoming email contains multiple intents, the agent now processes it through the standard AP intent-handling flow instead of routing the email into a Universal Request.


</td></tr><tr><td>

Agent experience for CSM

</td><td>

-   **[Name change for CSM/FSM Configurable Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/csm-config-ws-base-experience.md#section_cjb_ama_ljc)**

The name of the CSM/FSM Configurable Workspace has changed. The workspace name is dependent on the installed products.

    -   CRM Workspace: For customers using the Customer Service Management application or working in the Customer Relationship Management \(CRM\) environment.
    -   Industry-specific names: For customers using any of the industry products, such as Financial Services or Public Sector.
-   **[ServiceNow Otto for Customer Service Management \(CSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/now-assist-csm.md)**

Starting with Zurich Patch 12, ServiceNow Otto is the new AI experience brand. This change is reflected in the name of ServiceNow products, including ServiceNow Otto for Customer Service Management \(CSM\). Your product entitlements remain unchanged. Check your entitlements to determine your access to specific features.


</td></tr><tr><td>

Audit Management

</td><td>

-   **[Create evidence requests with a two-step process](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/request-evidence.md)**

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

-   **[Build Agent in ServiceNow Studio UI updates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/access-build-agent.md)**

Several changes have been made to how you access Build Agent in ServiceNow Studio:

    -   The central chat area on the ServiceNow Studio home page is the starting point for new Build Agent conversations.
    -   To open an existing conversation, select the Conversations icon \[Omitted image "ba-sns-otto-nav-icon.png"\] Alt text: in the Navigator panel.
    -   The Build Agent panel now opens on the Navigator panel of ServiceNow Studio.

</td></tr><tr><td>

CRM API Core

</td><td>

-   **[CRM API Core](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/sales-and-services-api-core.md)Sales and Services API Core renamed to CRM API Core**

Sales and Services API Core application has been renamed to CRM API Core.


</td></tr><tr><td>

CRM Core

</td><td>

-   **[Install and configure CRM Core](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/install-and-configure-lead-to-cash.md)Lead to Cash Core renamed to CRM Core**

Lead to Cash Core application has been renamed to CRM Core.


</td></tr><tr><td>

CRM Outlook Add-in

</td><td>

-   **[Associate an email with an existing CRM record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/associate-email-crm-outlook.md)**

Reduce user confusion when records can't be displayed or found.

    -   Previously, users saw a blank page when a linked record couldn't be displayed. Now, users receive information that helps them understand whether the record is unavailable or access is restricted, along with guidance on next steps.
    -   Previously, users saw a blank page when searches and filters returned no matching records on the Lead, Account, Contact, and Opportunity tabs. Now, users receive guidance to help them refine their search criteria or create a new record.

</td></tr><tr><td>

Care Team Work Management

</td><td>

-   **Healthcare Orchestration roles**

Two new roles, `sn_hco_orc.loc_contributor` \(Healthcare Orchestration Location Contributor\) and `sn_hco_orc.loc_manager` \(Healthcare Orchestration Location Manager\), can now be assigned directly as a service organization member's type.

Location-level and hospital-level visibility and management permissions for orchestration functions resolve automatically, without requiring the Care Team Agent Manager role as a workaround.


</td></tr><tr><td>

Case and Knowledge Management

</td><td>

-   ****

</td></tr><tr><td>

Cloud Cost Management

</td><td>

-   **[Optimization view on the Cloud Cost Management Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/optimization-view-ccm-ws.md)**

The Recommendations have been moved from the Operations view to the newly added Optimization view in the Cloud Cost Management Workspace. The Optimization view shows savings opportunities and recommendations for you across Unused resources, Rightsizing, Business hours, and Commitments.


</td></tr><tr><td>

Collaborative Work Management \(CWM\)

</td><td>

-   **[Import tasks entry point](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/import-tasks-cwm-board.md)**

The **Import tasks** option moved from a standalone button on the Board header into the **Create with Otto** menu, alongside the **Generate tasks** option. From the Board header, select **Create with Otto**, and then select **Import tasks** to start the import wizard.

-   **[Sprint sync between EAP and CWM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/cwm-integration-with-eap.md)**

Sprint name, state, capacity, and dates sync automatically from Enterprise Agile Planning to Collaborative Work Management for Agile teams that use non-calendar-based iterations, in addition to calendar-based teams.


</td></tr><tr><td>

Common Governance, Risk, and Compliance features

</td><td>

-   **[Automatic entity owner and class updates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/what-is-an-entity-filter.md)**

With GRC Profiles version 23.0.7, the system automatically re-evaluates and updates entity owner and entity class when source record data or entity-filter membership changes. This change keeps entity ownership and classification aligned with the applicable entity-filter configuration.

-   **[Issue grouping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/issue-grouping-in-workspaces.md)**

With GRC Issue Management version 23.0.5, you can add existing standalone issues directly from the Child Issues related list when grouping issues. You can group issues that use different workflows, and each child issue continues to follow its own workflow.


</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

-   **CMDB Workspace merged with Service Graph Workspace features**

Service Graph Workspace is deprecated as of this release. CMDB Workspace will have Service Graph Workspace features.

-   **[ServiceNow Otto replaces Now Assist name](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/reconcile-dup-task.md)**

Now Assist and Moveworks experiences is renamed to ServiceNow Otto \(Duplicate CI Remediator\).

-   **[Reset certification tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/data-certific-reset-task-wrkspc.md)**

Reset a certification task to restart the certification process for the task. Reset sets all certification results for the task to a 'Review not completed' state and removes any comments that were added.

-   **[Review certification tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/data-certific-review-tasks.md)**

When opening a task that isn’t closed, the Review not completed tab is selected by default for a quick access to task review. An Important information panel is now available throughout the task review process, that provides key details for the task such as special instructions and the ‘Allow field updates’ setting. You can attach files, such as supporting documents for various findings, to a task, and also, a percent complete number shows on the task page. The percent complete number is calculated as various certification activities are complete and reflects on the task review progress in real time.

-   **app\_service\_owner role contains the app\_service\_user role**

Use the app\_service\_owner role to grant create, read, update, and delete access to Service Instance records without granting the broader itil role. The app\_service\_owner role also includes the app\_service\_user role.

-   **Dynamic IRE Adoption**

Dynamic IRE is now enabled by default on zBooted instances, while on upgraded instances that are using Static IRE you can switch into using Dynamic IRE. Key benefits from the new Dynamic IRE engine include CI identification using an improved dynamic process and automatic updates of IRE identification rules during ingestion of data payloads.

-   **Inaccesible Records Indicator**

You can now review details about the outcome of a policy execution in the policy record in the CMDB Data Management Policy Executions \[cmdb\_data\_management\_policy\_execution\] table. Review the Wok Notes and the Activities fields and use details such as the number of CIs that weren't processed because they exist in other tasks, and access issues preventing processing of CIs to mitigate issues, for example, by updating the policy configurations or by updating user permissions.

-   **[Unified Map performance improvements for Safari](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/unified-map-config-browsers.md)**

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

-   **[OSCAL enhancements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/oscal-cam-ws.md)**

The OSCAL enhancements include:

    -   Import system-generated authority documents \(SSP, POA&amp;M, SAR, SAP, ATO Letter, Executive Summary reports\) and user-attached files at Authorization Package and Authorization Boundary levels during OSCAL import.
    -   Control objective IDs include source values during OSCAL import and export.
    -   Policy fields are included during OSCAL import and export.

</td></tr><tr><td>

Core Business Suite

</td><td>

-   **[Exploring employee support](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/core-business-suite/exploring-emp-home.md) [Exploring supplier support](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/core-business-suite/exploring-supplr-home.md)**

Provide CBS admins with ia\_admin and ia\_user roles to give them broader permissions and control. The roles aren't available for the CBS admin by default.


</td></tr><tr><td>

Data Catalog

</td><td>

-   **Data assets lineage improvements**

Transform nodes now display transformations and processing steps in your lineage diagram with enhanced visualizations. Interact with transform nodes to view additional details about what data transformations occur at each step, to help you understand your data flow more clearly. Lineage graphs now load progressively by level, to reduce timeout risk when viewing large graphs. The system displays lineage in stages, allowing you to explore relationships without waiting for the entire graph to load, which improves overall responsiveness and performance.


</td></tr><tr><td>

Data Management for CSM

</td><td>

-   **Project task assignment access for business organization staff**

Gain write access to the Assignment group and Assigned to field, and read access to the Priority field, on business organization project tasks with the Location Project Member \[sn\_bus\_loc.location\_project\_stakeholder\] or Location Project Manager Contributor \[sn\_bus\_loc.location\_manager\_project\_stakeholder\] role.

-   **[Billing account roles and responsibility access](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/granular-roles-and-supported-entities-CAM.md)**

Updated billing account roles and responsibility access to align with the expanded billing account capabilities. Extended access to Billing Account Address, Billing Account Payment Profile, and Billing Schedule \(schedule and schedule entry\) through:

    -   Billing Account platform granular and CRM granular roles
    -   Billing Account responsibilities through the customer access management \(CAM\) framework
-   **[Create a sold product](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/create-sold-item.md)**

Edit and view multiple related parties in the sold product enable users to review the details of a deal and review deal context without leaving the record. **Deal type** and **Route to Market** aren't captured on the sold product, with route to market options filtered automatically based on the selected deal type.

-   **[Create return merchandize authorization \(RMA\) cases directly from the business portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/rma-case-self-service.md)**

Initiate an RMA case from the business portal without contacting an agent to reduce the back-and-forth for returns and replacements.

    -   Enable customer contacts to view the list of their RMA cases from the **Request** menu on the portal to track their requests in progress.
    -   Customer contacts can open individual RMA cases and drill into case lines to review its status and details.

</td></tr><tr><td>

Discovery

</td><td>

-   **[Scan options for credential-less discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/nmap-credential-less-discovery.md)**

Credential-less Discovery can now check UDP ports and guess the operating system of a target host when it can't confirm an exact match. Enable each option by setting a MID Server property. Both options are inactive by default. Set **mid.discovery.credentialless.include\_udp\_scan** to `true` to check UDP ports and TCP ports. Set **mid.discovery.credentialless.include\_os\_scan\_guess** to `true` to let the scan guess the operating system of the target host.


-   **[IP Inventory multi-schedule link](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/daw-ip-inventory.md)**

IP ranges and IP network discovery ranges that belong to a discovery range set used across multiple schedules now display a linked value in the **Discovery Schedule** column. Select the **Multiple** link to open the associated records in the Discovery Schedule Range \[discovery\_schedule\_range\] table, filtered by the relevant discovery range.


</td></tr><tr><td>

Discovery store applications

</td><td>

-   **[AWS active datacenter discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/exclude-aws-resource-ldc-discovery.md)**

AWS discovery now uses the Resource Explorer API instead of the Config API to determine whether a datacenter region is active or passive. Use the `mid.cloud.discovery.sonar.exclude_resource_types` property to exclude specific resource types when evaluating a region's status.

-   **[OCI virtual machine BYOL discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/oracle-vm-pattern.md)**

The "Oracle OCI - Virtual Machine \(LP\)" pattern now discovers the Windows license type for OCI virtual machines \(VMs\), including Bring Your Own License \(BYOL\) and License Included.

-   **[Service Account and Logical Datacenter job full resync](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/configure-sa-ldc-full-resync.md)**

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


</td></tr><tr><td>

Dispute Rules Content Pack for Mastercard

</td><td>

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

Employee Slate for ITSM

</td><td>

-   ****

</td></tr><tr><td>

Enterprise Architecture

</td><td>

-   **[Domain separation for AI Control Tower integration with business applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-portfolio-management/eaw-aict.md)**

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

External Content Connectors

</td><td>

-   **Crawl schedules tab renamed**

In the external content connector editor, the **Crawl schedules** tab has been renamed to **Manage crawls**.


</td></tr><tr><td>

Financial Services Card Operations

</td><td>

-   **Price-discrepancy question for Visa consumer disputes**

An existing question, originally used under the Processing Errors dispute category, has been repurposed for consumer disputes filed under reason code 13.3 \(Not as Described or Defective Merchandise/Services\). Dispute agents are asked "Is the dispute due to the difference between the quoted price and the actual charges made by the merchant?" and cardholders are asked "Is the dispute related to a discrepancy between the quoted price and the actual charges made by the merchant?" A Yes answer marks the dispute ineligible for reason code 13.3, since a price discrepancy is not a valid basis for that reason code under the Visa Chargeback Guide.


</td></tr><tr><td>

Financial Services Operations Integration with Visa

</td><td>

-   **Updated questionnaire field labels and validation**

Renamed the question "Explain why credit presented does not apply" to "Provide the Transaction Identifier\(s\) or Acquirer Reference Number\(s\) and the Transaction Date that the credit\(s\) was applied to and why the credit\(s\) does not resolve the Dispute," and renamed "Certification that the merchant facilities were withdrawn" to "Certification that the facilities were withdrawn." The Name field is no longer required, and Key Factors now accepts up to 200 characters.

-   **Updated Spoke action wiring for new questionnaire fields**

Added the Date facilities were withdrawn and Date cardholder checked out from hotel fields to the `Submit Dispute Questionnaire` and `Look up Dispute Details Response Parser` spoke actions, and added CE Transaction Details as a read-back field on `Look up Dispute Details Response Parser`. See [Financial Services Card Operations 2026 September Monthly release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/financial-services-card-operations-rn.md) for the corresponding questionnaire questions.


</td></tr><tr><td>

Firewall Audits and Reporting

</td><td>

-   **Firewall rule compliance dashboard**

The compliance dashboard now includes additional metrics and visualizations to provide better insights into firewall rule compliance status and trends over time.


</td></tr><tr><td>

Goal Framework for SPM

</td><td>

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

ITOM AIOps

</td><td>

-   **[Configure alert grouping automation with AI from Alert Automation pages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/group-alert-sow-itom.md)**

Launch the AI agent for alert grouping directly from Alert Automation pages. Select **Configure with AI** to open the ServiceNow Otto panel with a pre-populated prompt that guides rule creation.

-   **Assign AI Specialists to all groups**

Assign the AI Specialist to the new **All Groups** option to let it handle alerts from every assignment group. Previously, only the **Add specialist to specific group\(s\)** option was available, which limited the specialist to the groups you chose.


-   **[Express List mode switching without searching](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/express-list.md)**

Change the Express List view between **Essential** and **Extended** mode independently of any search parameter. The list updates immediately to reflect the selected mode, and when you add a search value, results return according to the already-selected mode.


-   **[Credential setup for push connectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/push-connector.md)**

Select or generate a credential—Basic, API key, or OAuth—directly in the setup form, with API key now added as a new option. You configure the inbound endpoint in one place, without provisioning credentials elsewhere.


</td></tr><tr><td>

ITSM MCP Server

</td><td>

-   **[Changes to ITSM MCP server tools](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/itsm-mcp-server-tools-reference.md)**
    -   Added role restrictions for the ITSM MCP Change management tools.
    -   The **sn\_itsm\_mcp\_server.incident.get\_details**and **sn\_itsm\_mcp\_server.incident.modify** incident tools are available to both fulfillers and requesters. You use the **sn\_itsm\_mcp\_server.incident.modify** tool to also escalate incidents.
    -   The **sn\_itsm\_mcp\_server.requester.add\_comment** tool has been renamed to **sn\_itsm\_mcp\_server.request.modify**. Using this tool the requester can add customer-visible comments to their Requested Items. To add customer-visible comments to incidents, use the **sn\_itsm\_mcp\_server.incident.modify** tool.

</td></tr><tr><td>

Identity

</td><td>

-   **[Role masking in Now Assist AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/role-masking.md)**

Use role masking for AI agents and agentic workflows to limit the inherited roles during tool execution, verifying that AI agents run with restricted privileges, minimizing potential security risks and helping prevent unintended actions.

-   **[Restrict the Conditional Script Writer group from assignment group selection on Scripting Governance Tool](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/explore-sgt.md)**

The Conditional Script Writer group can no longer be selected as the assignment group on any task or incident based — through the user interface with the base system configuration.

-   **[Federated ID](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/federated-id.md)**

Choose any unique field — not just User ID — as the identifier in a federated ID criteria for the User table, as long as the criteria includes at least one unique field for generating federated ID.


</td></tr><tr><td>

Impact

</td><td>

-   **Accelerator Catalog**
    -   Success Readiness Assessment changed to Success Foundation Review.
    -   UX Accelerators moved from Architecture to Technical sub-catalog
    -   AI Readiness Assessment moved from Architecture to Technical sub-catalog
    -   Tuneup Your IT Asset Management changed to Tuneup Your ITSM Asset Management
    -   Jumpstart Your App Engine changed to Jumpstart Your App Deployment Governance
-   **[Platform Health](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/platform-health-idi.md)**
    -   Use exception workflows in update set scans now provide multiple governance improvements.
    -   Assign a dedicated exception approver role for governance separation
    -   As and Instance administrator, control which finding levels are eligible for exception reasons.
    -   Access update set origin tracking on all scan findings
    -   View the captured update set data that contains the violating code whenever a full or delta scan runs and produces a finding.
    -   Full-scan scope updates so only definitions explicitly configured for single-finding-per-table scanning are included.
    -   The Scan Engine Properties page now displays a dedicated warning when the company code is unset, with a link to the system property for resolution.
-   **[Value management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/impact-in-platform-business-outcomes.md)**

Access Hardware Asset Management \(HAM\) and Software Asset Management \(SAM\) functionality through a single, unified ITAM app, grouped under IT Asset Management. All previously collected data and configuration is carried over with no manual reinstallation, reconfiguration, required during the upgrade.


</td></tr><tr><td>

Incident Management

</td><td>

-   **[Incident manager role changes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/inci-roles-instld-itsm-roles.md)**

The inherited itil role is now removed from the incident manager \[incident\_manager\] role and replaced with the incident\_write role. The is applicable only for the zboot instances. This change restricts access to incident records only, aligning permissions with the intended scope of the role and reducing unnecessary access to unrelated process areas.

-   **[Major incident manager and communication plan manager role changes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/installed-with-mim.md)**

The major incident manager \[major\_incident\_manager\] and communication plan manager \[sn\_comm\_management.comm\_plan\_mgr\] roles no longer inherit the itil role. Instead, the roles inherit the sn\_incident\_write, sn\_problem\_write, sn\_change\_write, sn\_request\_write granular roles from the ITSM Roles plugin \(com.snc.itsm.roles\). This is applicable only for the zboot instances.

For the upgrade instances, the itil role remains inherited. Additionally, the sn\_incident\_write, sn\_problem\_write, sn\_change\_write, and sn\_request\_write granular roles are added if the ITSM Roles plugin \(com.snc.itsm.roles\) is installed.

-   **[Communication plan viewer role changes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/components-installed-with-icm.md)**

The sn\_dex\_desktop.notification\_template\_admin role is now removed from the communication plan viewer \[sn\_comm\_management.comm\_plan\_viewer\] role and added to the sn\_incident\_write role when ITSM Roles plugin \(com.snc.itsm.roles\) is installed. In case, ITSM Roles plugin \(com.snc.itsm.roles\) is not installed, the sn\_dex\_desktop.notification\_template\_admin role is added to the itil role. These role changes are applicable only for the zboot instances.

-   **[Itil role check removal from comm\_channel create and write ACLs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/components-installed-with-icm.md)**

The itil role reference check is now removed from the comm\_channel create and write ACLs. Create and access to the communication channel definition in the incident communication tasks is based on the commTaskGr.state.canWrite script and if you have the following roles:

    -   Communication plan manager \[sn\_comm\_management.comm\_plan\_mgr\]
    -   Communication plan admin \[sn\_comm\_management.comm\_plan\_admin\]
    -   Task communication management admin \[sn\_tcm\_admin\]
    -   ITSM granular roles such as sn\_incident\_write and the user assigned to the incident communication task and plan.
-   **[Auto close resolved incidents behavior changes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/incident-management-properties.md)**

The resolved incidents are now automatically closed after a specific number of business days instead of calendar days. You can use configure the number of business days using **Number of days \(integer\) after which Resolved incidents are automatically closed. Zero \(0\) disables this feature** \[**glide.ui.autoclose.time**\] property. This changes helps the maintaining the internal organizational policies.


</td></tr><tr><td>

Kubernetes Visibility Agent \(KVA\)

</td><td>

-   **Kubernetes resource dependency views**

Resource details pages now include enhanced Dependency Views that show relationships between Kubernetes resources and related configuration items. The improved visualization helps administrators understand service dependencies and troubleshoot issues more effectively.


</td></tr><tr><td>

LEAP

</td><td>

-   **[Hide archived automation opportunities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/automation-opportunities.md)**

Automation opportunities \(AOs\) from an earlier GAF \(Global Automation Framework\) run are now hidden by default. Previously, old AOs with resolution steps remained visible in the workspace after remapping. It was difficult to distinguish actionable AOs from old ones. After a GAF re-run, the old AOs are archived and no longer appear on the homepage. The artifacts of archived AOs are mapped to relevant new AOs.

-   **[LEAP value dashboard expansion](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/understand-the-aiops-leap-value-dashboard.md)**

The LEAP value dashboard now surfaces metrics for all automation outcome types along with existing playbook data. New sections display Ansible execution counts, agent-hours saved, and top playbooks by tickets resolved, KB article creation counts and top contributing clusters, and problem record \(PRB\) creation counts and top clusters. A summary at the top of the dashboard breaks total automation activity and savings attribution by outcome type such as LEAP playbooks, Ansible playbooks, KB articles, and PRBs, each with a trend indicator. The dashboard also displays ServiceNow Otto consumption data to track the consumed per action.


</td></tr><tr><td>

Mobile Platform

</td><td>

-   **Android app build request form**

Meet Google's new Android security requirements for developer verification and app registration using the updated build request form and pipeline. The form now includes a developer verification section where you provide your snippet, and the pipeline automatically embeds it in your APK or generates a verification APK for manual registration.


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

-   **[Pending updates displayed in the banner](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/integration-with-incident-management.md)**

The pending updates for the DRIR case are displayed in a banner within the workspace.

-   **[Decimal precision for DORA monetary values](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/opres-dora-validate-roi.md)**

Monetary value fields now support up to two decimal places. Previously, only zero or negative values were accepted, with all monetary values defaulting to zero. Values greater than zero are no longer rounded down to zero during download.

-   **[CSV download only references applied filters when selecting all records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/create-excel-upload-download-request.md)**

When a filter is applied to a list and users select all records for CSV download, only the filtered records are included. Previously, all records were downloaded regardless of the applied filter.

-   **[Impact analysis correctly resolves Profile records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/scheduled-jobs-installed-with-or.md)**

Previously, impact analysis failed to resolve entities when a scheduled job processed GRC Profile records directly. This issue has been fixed. Impact analysis now correctly resolves Profile records in Operational Resilience and entity resolution completes as expected for all record types.

-   **[Rank 1 supply chain records update automatically when a contract's service provider changes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/create-drtp-reg-supply-chain.md)**

If you change the service provider on a DORA contract record, the associated Rank 1 supply chain records update automatically. The records reflect the new provider or recipient.

-   **[Excel export for DORA Functions requests no longer fails on large datasets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/create-excel-upload-download-request.md)**

Exporting a Functions-type Excel drop-down download and upload request no longer fails when drop-down fields reference large CMDB or reference tables. Results are capped at 10,000 records per drop-down field.

-   **[Parent record navigation added to DORA third-party and contract records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/create-new-cont-arrange-form.md)**

A reference field is available on DORA third-party and third-party engagement records. Use it to navigate back to the originating contract record after arriving from a related list. Previously, there was no way to return to the parent contract or company record from these pages.

-   **[Notice period fields accept a value of zero](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/tprm-validation-roi.md)**

The notice period fields \(`B_02.02.0100` and `B_02.02.0110`\) now accept a value of `0`. Previously, a value of `0` was rejected as if the field were empty.


</td></tr><tr><td>

Operational Sustainability Management

</td><td>

-   **[Enhanced content generation in Document Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/configure-data-columns.md)**

With Document Designer version 23.0.3, you can create HTML-based scripted columns for content blocks in your reports.


</td></tr><tr><td>

Performance Analytics

</td><td>

-   **[Use bucket groups to breakdown Data Snapshots indicators by continuous data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/map-bucket-group-to-ds-source.md)**

To filter Data snapshots scores by a numeric field on the source table, map a bucket group to that field. The bucket group splits that field into value ranges.

-   **[Use calculated fields to break down Data Snapshots indicators by date](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/create-a-calculated-field.md)**

Create calculated fields to show the length of time that has passed between two date/time fields on a Data snapshots source table. For example, calculate Age as the difference between Created and Updated.

-   **[Create indicators on Workflow Data Fabric tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/data-fabric-tables-zcc.md)**

Create classic automated indicators on external data via Workflow Data Fabric. Use Workflow Data Fabric tables in indicator sources just as you would any other facts tables.

-   **[Intraday scores supported on indicators with Data snapshots enabled](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/ds-score-collection-enabled-indicators.md)**

You can now collect intraday scores on classic indicators with Data snapshots enabled instead of only on natively created Data snapshots indicators.

-   **[Manage and troubleshoot your Data snapshots jobs more easily](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/data-snapshots-logs.md)**

You now are provided with new estimates and more log information:

    -   Time estimates before a job starts
    -   Progress percentages for first-day mining, changes loader, and delta mining jobs
    -   Logs include the next scheduled run timestamp after incremental job completion

</td></tr><tr><td>

Portfolio Planning

</td><td>

-   **Financials**

Added in-context help \(hover info icons\) on the Financials page widgets, explaining how the key fields like Budget, EAC, Planned Cost, Actuals, Return, ROI, and NPV are calculated.

-   **[Program planning updates and enhancements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/program-portfolio-plan-ppw.md)**
    -   **Programs menu addition** — A new Programs menu has been added to the workspace as L2 menu, positioned below Portfolio Plan. This menu lists every program in your portfolio and provides single-click navigation to each program's enhanced planning view.
    -   **Role-based access for program planning** — Users with the sn\_align\_core.ap\_read\_only role have read access to program plans \(where they already have program-level read access\). Users with the sn\_align\_core.apw\_admin and program manager roles receive full access to create, update, and manage planning items within program plans.
-   **[Summarize demands with the demand summarization skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/summarize-demands-in-ppw.md)**

The default trigger is not set to **Automatic** for demands in any state. You can select how you want the skill to be triggered for any state.


</td></tr><tr><td>

Pricing Management

</td><td>

-   **[Extended product life cycle support in Price Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/extended-product-lifecycle-states.md)**

Validate pricing setup against catalog changes earlier in their life cycle by extending product offering life cycle visibility into Price Management.

    -   Previously, price list lines, cost book lines, and attribute adjustments could reference only Published product offerings. Now, when extended product life cycle states are enabled, they can also reference offerings in the In Test and Staged states. This enables the pricing admin to create price lists and define rules in pricing matrices for offerings that are in the In Test and Staged states.
    -   Previously, context variable rules and pricing matrix rules could filter on Published product offerings only. Now, they can also filter on offerings in the In Test and Staged states.
-   **[Delta price calculation for consolidated renewal lines](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/renewal-pricing-ramped-products.md)**

Calculate delta price more accurately for renewal lines that consolidate multiple contract line items affected by upsells or downsells. The calculation now uses the prior contract value over the subscription's full previous term, together with the new renewal price including uplift, to determine the delta price amount.


</td></tr><tr><td>

Privacy Management

</td><td>

-   **[Data lineage map UI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/editing-data-lineage.md)**

When you select the relationship line between two nodes in the data lineage map, a side pane opens with the relationship details, where you can edit or remove a relationship.

-   **[Node location fields in the hierarchy modal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/new-relationship-forms.md)**

The hierarchy modal now includes node location fields. The Define relationship step includes a **Primary node location** field, and the Relationship details step includes a **Related node location** field.

-   **[Data subject selection in hierarchy relationships](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/config-ds-sys-property-hierarchy.md)**

Privacy admins can enable data subject selection for custom relationship types in a hierarchy by modifying the sn\_privacy.relationship\_involving\_data\_subjects system property.

-   **[Applicable scope tab in a privacy assessment task](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/ai-reccos-for-pia.md#applicable-scope-tab-pia)**

The Applicable scope tab on the assessment task record replaces the former Outcomes tab. It lists the control objectives and risk statements that have been scoped to the processing activity through manual addition, automation rules, or AI-assisted recommendations.

-   **[External-facing Personal Data Rights \(PDR\) form layout](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/submit-privacy-request-external-pdr.md)**

The external-facing PDR form layout is updated to support mobile screens.


</td></tr><tr><td>

Process Mining

</td><td>

-   **[Content packs availability changed](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/process-mining-content-pack-delivery.md)**

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

-   **[Minor updates to published product offerings and specifications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/minor-updates-published-offerings-specs.md)**

Simplify updates to published product offerings by adding optional characteristics and optional child offerings without creating a new offering version. Set a future effective date for the child-offering relationship to control when the child becomes available for new purchases or order changes. Previously, these updates required a new version of the parent offering and replication of its related configuration.

Previously, turning on the transient setting for a published product offering required creating a new version. Now, turning it on doesn't require a new version. Turning it off still requires one.

-   **[Product catalog sort options](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/using-product-catalog.md)**

Previously, the sort drop-down menu in the product catalog was hidden unless AI Search was turned on. Now it is always available, and includes a new Display Order option that sorts by your configured display order. The Relevancy option still appears only when AI Search is on.

-   **Product Catalog Management data model changes**

New columns have been added to the Product Catalog Management tables to enable new life cycle states, channel-specific launch dates, and control the display sequence of offerings in the catalog.

    -   Value column has been added to the Distribution Channel \[sn\_prd\_pm\_distribution\_channel\] table. It canonically maps the channel name resolved from the context variable or the Sales CRM entity header to the sys\_id \(Name\) in the Distribution Channel \[sn\_prd\_pm\_distribution\_channel\] table.
    -   State column on the Product Offering \[sn\_prd\_pm\_product\_offering\] table now includes In Test and Staged values, sequenced between Draft and Published. A new Approval state column has been added, with values Not yet requested \(default\), In Review, Approved, Rejected, and Recalled. A new Active channels column has also been added. It's a read-only, comma-separated list of distribution channel references that stores the channels the offering is currently available on, so catalog search can filter on availability without a table join.
    -   State column on the Specification \[sn\_prd\_pm\_specification\] table now includes In Test and Staged values, sequenced between Draft and Published.
    -   Effective from column has been added to the Product Offering Relationship \[sn\_prd\_pm\_product\_offering\_relationship\] and Specification Relationship \[sn\_prd\_pm\_specification\_relationship\] tables.
    -   Order column has been added to the Catalog Category \[sn\_prd\_pm\_catalog\_category\_relationship\] and Product Offering Catalog \[sn\_prd\_pm\_product\_offering\_catalog\] tables.
    -   Display Order column has been added to the Product Offering \[sn\_prd\_pm\_product\_offering\] table

</td></tr><tr><td>

Product Support for Technology

</td><td>

-   **[Technology Account 360](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/proactive-service-exp-workflows/technology-account-360.md)**

Use the Technology Account 360 to get a unified view of customer or partner account details combining account health, financial, product usage, and open tasks.


</td></tr><tr><td>

Project Portfolio Management

</td><td>

-   **Portfolio Insights card order**

The AI Insights panel now displays insight cards in a fixed order based on prominence and impact: Projects at risk, Budget Overrun, Cost Variance, Items past planned end date, Delayed start, and Planned versus approved misalignment. Review the most critical financial and schedule risks first.

-   **Insight explanations in Portfolio Insights**

Each card in Portfolio Insights now includes an info icon. Select the icon to open a popover with a plain-language explanation of what the insight measures and how it's calculated, so you can interpret the insight without leaving the panel.

-   **[Navigation to Project Workspace in Next Experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/t_CreateAProject.md#steps_cmz_5wd_tw)**

View and access Project Workspace in Next Experience when you access project workspace from the All navigation menu.

-   **[Summarize demands with the demand summarization skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/demand-summary-demand-classic.md)**

The default trigger is not set to **Automatic** for demands in any state. You can select how you want the skill to be triggered for any state.


</td></tr><tr><td>

Project Workspace

</td><td>

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

-   **[Large language models on the ServiceNow AI Platform](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/exploring-large-language-models.md)**

Starting with the September 2026 release, Gemma 4 joins our growing portfolio of open-weight models available through Now LLM Service. The latest industry advancements are available alongside sovereignty-focused options. All models are hosted and governed by ServiceNow with the same infrastructure and data protections. Older models will remain available for existing published AI skills, agents, and agentic workflows, but will no longer be available for new development or configuration. For details, see the [KB3066214: ServiceNow Otto Model Upgrades](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3066214) article in the Now Support Knowledge Base.

-   **[Now Assist &gt; ServiceNow Otto® announcement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/sn-ai-implementation-landing.md)**

ServiceNow Otto introduced AI on the platform. As that experience has evolved, there's a new name for the experience. ServiceNow Otto® is the conversational AI platform integrated into ServiceNow workflows. It provides agentic capabilities, supports multimodal interactions across web, mobile, and messaging channels, and enables autonomous orchestration for cross-system workflows.

-   **[Enhancements to Grants Management: Program Setup](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/government-industry/psds-using-grants-management-playbook.md)**
    -   [Establish the Grant Program Budget in Grants Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/government-industry/psds-config-gmp-pgr-budget.md)

Use the restructured Program Budget step that is now organized into three sections: Program Budget, Budget Categories, and Award Allocation. Grant Program Managers can select from three award models—Single Award, Multiple Equal Awards, or Multiple Variable Awards—with budgets automatically derived from the Awards category. Real-time calculations update the Budget allocated and Balance left fields as you enter category percentages. This enhancement prevents completion until all of the program budget is allocated across the categories.

    -   [Configure program lifecycle stepper](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/government-industry/psds-config-gmp-pgr-lifecycle-stepper.md)

Disable the six-step grant program lifecycle stepper at the instance level, reducing ambiguity about grant program state. By default, the stepper indicating the Preparing Program, Accepting Proposals, Evaluating, Awarding, Post-Award, and Closed states is hidden in the Grant Program record page. Admins can enable it if required for deployments that follow a batch or competitive grant lifecycle. When turned off, program state is conveyed through existing status fields.

-   **[Enhancements to Grants Management: Proposal Playbook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/government-industry/psds-using-grants-management-playbook.md)**
    -   [Screen a grant proposal in the Grants Proposal Playbook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/government-industry/psds-using-gmp-grant-proposal-screen.md)

Flag and route a document back to the applicant while reviewing the proposal details in the screening step. The document persists in the Flagged section with all metadata intact. Grant program managers and Grant program directors can reverse the flag by selecting the reset status icon to move it back to Requires Verification with no data loss. Select Request Documents at the bottom of the Verify Documents screen to route flagged documents back to applicants automatically. This action creates a case task assigned to the applicant, sends a notification in the applicant portal prompting re-upload, and changes the document status to Pending Resubmission. After the applicant uploads the corrected document, the Upload Additional Documents activity closes and you can continue verification, maintaining a complete audit trail throughout the process.

-   **[ServiceNow product tiers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/ai-native-sku-overview.md)**

The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets, and create your own
Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.


</td></tr><tr><td>

Purchase Order Management

</td><td>

-   **[Automated purchase order exception creation from emails](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/source-to-pay-operations/convert-emails-to-exceptions.md)**

Previously, emails containing multiple intents would create only a single case for the dominant intent and default to a Universal Request for others. Now each identified intent triggers its own case creation, eliminating manual conversion work.

-   **[Changes to the Purchase Order Confirmation Data Model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/source-to-pay-operations/po-confirmation-line-table.md)**

The Confirmation source and Status fields in the Purchase Order Confirmation \[sn\_poem\_po\_confirmation\] table have new values: AI Agent and Draft Retracted.


</td></tr><tr><td>

Regulatory Change Management

</td><td>

-   **[Entity filtering in the risk assessment modal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/impact-assessment-tasks.md)**

When you initiate a risk assessment from a regulatory alert, the Evaluate risk impact dialog box includes a **Filter by** drop-down. Use **Entities by Impacted Areas** or **Entities by Recommendations** to scope your entity selection.

-   **[Regulatory alert summarization in all regulatory alert states](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/regulatory-alert-summarization.md)**

Generate a regulatory alert summary in any state. The AI-generated summary includes new sections such as alert overview, scope, actions and outcomes, and velocity analysis. Select **Share to alert summary** to save the summary to the alert record.

-   **[Enhanced input data for regulatory alert summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/input-data-rcm-skill.md)**

The regulatory alert summarization skill uses additional input data to generate a summary. New input fields include enriched insights, coordinator details, functional domain, and alert type, among others. The skill also incorporates data from the impacted areas and regulatory change tasks related lists.

-   **[Regulatory alert number on the Details tab of an alert](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/reg-feed-overview-in-ws.md)**

The regulatory alert number is displayed on the Details tab of a regulatory alert.

-   **[New column on regulatory assessment tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/respond-to-a-regulatory-assessment.md)**

The Regulatory assessments tab in **GRC Tasks** displays the regulatory alert for an assessment in the Record column.

-   **[Compliance library items traced to their corresponding regulatory action tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/action-tasks.md)**

Compliance library records, including citations, control objectives, controls, and policies, feature a Regulatory action tasks tab that links the action tasks linked to these records. This enables you to navigate from the impacted area record in the compliance library directly to its action task in RCM. Similarly, from the Action tasks tab of a regulatory alert, you can navigate to the impacted citations, control objectives, controls, or policies.

-   **[Email notification redirection to workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/email-notifications-in-rcm.md)**

Email notification links for RCM records redirect users to the Compliance Workspace instead of the classic environment.


</td></tr><tr><td>

Retail

</td><td>

-   **Template item column for store plan cases**

New cases that are created from a store plan or a store audit plan will populate the **Template item** column, while the **Origin** field will no longer be populated for newly created cases.

**Note:** If you have a custom implementation that relies on the **Origin** field to determine the template item that a case was created from, those use cases will need to be updated accordingly.


</td></tr><tr><td>

SPM Enterprise-Wide Deployment

</td><td>

-   **[Restrict system administrator access to partitioned data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/configure-admin-access-to-all-partitions.md)**

Restrict system administrators from accessing partition-protected data through a new configurable system property. The system property **sn\_spm\_ewd.allow\_admin\_access\_to\_all\_partitions** controls whether system administrators can access all partitions by default. By default, this property is set to `false`, which means system administrators must have the appropriate partition role to access partition-protected data.

Users with the system administrator or sn\_spm\_ewd.ewd\_admin role can configure this property. This enforces strict data governance policies at all security levels and prevents unintended access to sensitive partition data. When partition access restrictions apply, all user roles, including system administrators, are subject to uniform partition role validation.


</td></tr><tr><td>

Security Incident Response

</td><td>

-   **[Exploring Security incident quality assessment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/security-management/na-sir-quality-assessment.md)**

Customize or regenerate entire draft reports or specific sections within it, before you share it with stakeholders.


</td></tr><tr><td>

Self-service and omnichannel engagement for CSM

</td><td>

-   **[Usage calculation of self-service experiences](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/csm-portal-user-sessions-timeouts_2.md)**

Get more accurate portal usage data with an updated analytics definition that eliminates double-counting of guest user sessions.


</td></tr><tr><td>

Service Operations Workspace for ITSM

</td><td>

-   **[Default Attached knowledge related list](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/incident-sow.md)**

The attached knowledge related list now appears in the Related records tab by default, if any Knowledge article attached to the incident record.


</td></tr><tr><td>

ServiceNow AI Platform core feature

</td><td>

-   **[AI indicators updated for form fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/platai-ai-indicator-form-fields.md)**

AI indicators for form fields in Core UI and configurable workspaces now support AI color gradients and have been updated to reflect the latest ServiceNow Otto name and iconography.

-   **[TinyMCE version 8.3.0 upgrade](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/c_UseHTMLFields.md)**

The HTML editor in Core UI and configurable workspaces is upgraded from TinyMCE version 6.8.2 to version 8.3.0.

-   **[Text pattern configuration in the HTML editor](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/configuring-the.md-system-properties-in-tinymce.md)**

Text patterns in the HTML editor can now be turned on or off using the **glide.ui.html.editor.textpatterns** system property.

-   **[Configurable choice field empty option labels](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/r_AvailableSystemProperties.md)**

Configure choice fields to display either None or --None-- for empty options using the **glide.ui.choice.display\_none** system property.

-   **[Base cross-scope access on the latest source code updates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/r_AvailableSystemProperties.md)**

Control how the system invalidates Restricted Caller Access records when a source code record, such as a script include, in a cross-scope access table is committed in an update set with the glide.sys.fencing.restricted\_caller\_access.invalidation\_mode system property. By default, a database listener monitors update set commits on source code tables and invalidates RCA records at the time of the commits so that cross-scope access is based on the latest source code updates.

-   **[ECMAScript 2021 \(ES12\) JavaScript mode supports additional scripting features](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/scripts/javascript-engine-feature-support.md)**

Use additional scripting features in applications or scripts that use the ECMAScript 2021 \(ES12\) JavaScript mode.

-   **[JavaScript engine updated with changes from the Rhino engine](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/scripts/updates-javascript-engine.md)**

The JavaScript engine on the ServiceNow AI Platform was updated to incorporate changes from the open-source Rhino JavaScript engine.

-   **[Configure row threshold for exports to Excel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/c_ExportLimits.md)**

Configure the row limit for exports to Excel using the properties **glide.export.xls.max.rows.per.sheet** and **glide.export.xlsx.max.rows.per.sheet**.


</td></tr><tr><td>

ServiceNow Otto for Contract Management Pro

</td><td>

-   **[Search in contracts document](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/cmpro-na-converse-ask-ques-new.md)**

Contract document-based conversational search queries now return all matching results instead of 10 results. Use Show more option to load the remaining results.

-   **[Search in contract metadata](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/cmpro-na-search-metadata.md)**

In conversational search, introduced an option to preform in-document search after the contract metadata search results are available.


</td></tr><tr><td>

ServiceNow Otto for Virtual Agent

</td><td>

-   ****

Role-based configuration is no longer stored or managed within Assistant Designer.

-   **[Upload files improvements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/upload-documents-na-va.md)**

Upload up to 10 files or 50 MB for the following file types: PDF native, PDF OCR, Word, PPTX, Excel, CSV, TXT, JPEG, PNG for premium chat in ServiceNow Otto for Virtual Agent and Otto panel.

-   **[Updated ServiceNow Otto processing animation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/nava-integrated-chat.md)**

View an updated ServiceNow Otto processing animation.


</td></tr><tr><td>

ServiceNow Studio

</td><td>

-   **[ServiceNow Studio settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/servicenow-studio-settings.md)**

ServiceNow Studio user preferences and settings have moved from the top right corner to the bottom left corner of the interface. View what's new in ServiceNow Studio, access command palette and keyboard shortcut options, and update preferences.

-   **[App summary generation moves to an agentic architecture](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/sns-exploring-now-assist-app-summarize.md)**

ServiceNow Otto for app summary generation now uses an AI agent to generate application summaries. This change moves the App summary generation from a skill-based architecture to the AI agent orchestration model.

With this release, users who install the App summary plugin receive the App Summary AI agent.

The App Summary AI agent is turned off by default after plugin installation to help avoid unexpected charges. An administrator must enable the agent in AI Agent Studio before users can generate application summaries.

The end-user experience remains the same. The change affects only the underlying architecture, which now uses an agentic model instead of the earlier skill-based model.

-   **Deployment tab**

The **Deployment** tab, with lists of all update sets, applications, and deployment requests, has moved from the home page to the activity bar as a separate tab.


</td></tr><tr><td>

ServiceNow Vault

</td><td>

-   **[ServiceNow Otto name change](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/now-assist-vault-landing.md)**

ServiceNow Otto introduced AI on the platform. As that experience has evolved, there's a new name for the experience. ServiceNow Otto® is the conversational AI platform integrated into ServiceNow workflows. It provides agentic capabilities, supports multimodal interactions across web, mobile, and messaging channels, and enables autonomous orchestration for cross-system workflows.

-   **Role masking in the Access Observer and Field Encryption workflows**

The security\_admin role is no longer used as the role masking agent for the Access Observer and Field Encryption agentic workflows. Following least-privilege principles, these workflows run without elevating to security\_admin.

-   **Default policy naming**

Default policies provisioned for field encryption, data privacy, Zero Trust Access, and Log Export Service are prefixed with Vault by Default, so you can distinguish policies that ServiceNow provisioned from policies your organization created.


</td></tr><tr><td>

Smart Assessment Engine

</td><td>

-   **[Create an assessment template category](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/sae-asmnt-template-category-create.md)**

With Smart Assessment version 23.0.2, the assessment template category form includes two new fields: **QB category roles**, which controls access to the question banks associated with the category, and **Allow user delegation**, which lets users delegate their assessments in the category.

-   **UX improvements to assessment questions and responses**
    -   [Drop-down list question](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/sae-q-drop-down-create.md) — With Smart Assessment Designer version 23.0.5, reopening a drop-down list question now shows all response options again, not just the ones you previously selected.
    -   [Reference question search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/sae-respond-to-asmnt.md) — With Smart Assessment Core version 23.0.2, for single-select and multi-select reference questions, when a table has more than 10 matching records, select the search icon to browse the full set. This replaces the default behavior of showing only the first 10 records.
    -   [Default focus when opening or reopening an assessment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/sae-respond-to-asmnt.md) — With Smart Assessment Core version 23.0.2, the view defaults to the assessment instructions, if configured, or the first question of the first section or subsection. This applies even if you, a collaborator, or response automation has already answered later questions.

</td></tr><tr><td>

Software Asset Management

</td><td>

-   **[Gain clearer visibility into SAP HANA user license types with the renamed License classification column](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/view-sapusers-workspace.md)**

The **Named user type** column is renamed to **License classification** in the SAP System Users \[samp\_sap\_system\_user\] table for improved visibility into SAP HANA user license types and entitlement reconciliation. The column appears on the SAP System Users related list of software models created for SAP S/4HANA products.

-   **[Manage SAP S/4HANA Cloud, Public Edition entitlements with the renamed User Subscription metric](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/c_SAMLicenseMetrics.md)**

The **Full Usage Equivalent** license metric for SAP S/4HANA Cloud, Public Edition is renamed to **User Subscription**, aligning with SAP's updated naming for this edition. The Full Usage Equivalent metric continues to apply to SAP S/4HANA Cloud, Private Edition. The calculation logic is unchanged.

-   **[Manage software models with clearer licensing terminology](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-model-fields.md)**

Understand licensing scope at a glance from the renamed column in the Software Model \[cmdb\_software\_product\_model\] table. The **License all installs accessed by clients** column is renamed to **License all installs**. The new name reflects that all installs meeting the software model's conditions are licensed, not only those tied to client access records.

-   **[Removal candidates tab replaced with the Reclamation tab in the License usage view](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/sam-workspace-workbench.md)**

The **Reclamation** tab in the License usage view on the Software Asset Workspace presents a consolidated view of reclamation candidates across all publishers, SaaS integrations, installed software, and reconciliation flows.

-   **[Software Spend Detection Core UI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/spend-detection-sam-workspace.md)**

The Software Spend Detection feature is no longer available in the Core UI. Software Spend Detection is now accessible from the Software Asset Workspace under License operations. Existing imports and spend transactions created in the Core UI are now accessible from the Software Asset Workspace.


</td></tr><tr><td>

Strategic Planning

</td><td>

-   **Financials**

Added in-context help \(hover info icons\) on the Financials page widgets, explaining how the key fields like Budget, EAC, Planned Cost, Actuals, Return, ROI, and NPV are calculated.

-   **[Enterprise Agile Planning configuration options](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/create-eap-configuration.md)**
    -   The **Have unique calendars** option is renamed to **Allow unique cadence for each team**.
    -   An EAP admin can now clear the **Allow unique cadence for each team** option after selecting it. Selecting the option doesn't change the calendars or the iterations that already exist.
    -   The **Scrum Sprint** planning calendar type is available by default, alongside **Planning Interval** and **Sprint**.
-   **[Iteration dates in Enterprise Agile Planning](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/edit-pi-sprint-iteration-details-in-eap.md)**
    -   The **Enterprise agile calendar entry** field on the Enterprise agile iteration \[sn\_apw\_advanced\_eap\_iteration\] table is no longer mandatory, which supports iterations that carry their own start and end dates. A fix script makes the field optional when you upgrade.
    -   Users with the `sn_apw_advanced.eap_user` role can set the start date and the end date while they create an iteration. They can change those dates afterward on an iteration that doesn't follow a planning calendar entry. However, changing the dates on an iteration that follows a planning calendar entry still requires the `sn_apw_advanced.eap_scrum_master` role.
-   **[Sprint sync with Agile Development 2.0](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/sync-eap-and-agile-2.md)**
    -   Sprints that don't follow a planning calendar entry now sync to Agile Development 2.0 by using the start date and the end date on the iteration.
    -   Changing the start date or the end date of an iteration now updates the dates on the corresponding Sprint in Agile Development 2.0.
-   **[Program planning updates and enhancements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/program-portfolio-plan-spw.md)**
    -   **Programs menu addition** — A new Programs menu has been added to the workspace as L2 menu, positioned below Portfolio Plan. This menu lists every program in your portfolio and provides single-click navigation to each program's enhanced planning view.
    -   **Role-based access for program planning** — Users with the sn\_align\_core.ap\_read\_only role have read access to program plans \(where they already have program-level read access\). Users with the sn\_align\_core.apw\_admin and program manager roles receive full access to create, update, and manage planning items within program plans
-   **[Summarize demands with the demand summarization skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/summarize-demand-in-demand-workspace.md)**

The default trigger is not set to **Automatic** for demands in any state. You can select how you want the skill to be triggered for any state.


</td></tr><tr><td>

Subscription Management

</td><td>

-   **[Account-level cloud capacity storage pool](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/monitoring-cloud-entitlements.md)**

Cloud capacity storage is now pooled at the account level rather than capped at the instance level. This means your total storage entitlement can be used more flexibly, wherever it's needed across your environment.


</td></tr><tr><td>

Supplier Lifecycle Operations

</td><td>

-   **[Verify bank account ownership using Relish](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/source-to-pay-operations/verify-banking-information.md)**

When a banking details change request is assigned to a supplier manager and they start working on it, they can verify the details using Relish.

By default, bank validation checks only the bank routing number and address details. Relish also verifies the bank account number and account ownership information when bank account ownership validation is enabled.

-   **[Conduct bulk sanction screening using Relish](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/source-to-pay-operations/perform-bulk-sanction-screening.md)**

When a sanction screening request for compliance verification is assigned to a supplier manager and they start working on it, they can verify the details using Relish.

Supplier managers can conduct sanction screening for multiple suppliers simultaneously using the bulk sanction screening feature.

-   **[AI driven supplier onboarding using ServiceNow Otto for SLO](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/source-to-pay-operations/supplier-onboarding-agentic-workflow.md)**
    -   Leverages Web search results to generate a supplier scorecard highlighting key strengths, positive indicators, and potential risk signals.
    -   If Craft is configured, the workflow leverages the Craft integration to generate a comprehensive, normalized supplier scorecard and risk assessment. It provides a structured evaluation of the supplier’s overall profile and associated risk factors.
    -   If Relish is integrated, the supplier's banking information is further validated and synchronized with Relish.

</td></tr><tr><td>

System Localization

</td><td>

-   **[Improved visibility for the user's date format and time format settings.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-user-interface/next-experience-language-preferences.md)**

The date and time format settings are relocated from the user profile to the Language &amp; Region section within the user's Preferences. These important settings are now visible and editable in one place.


</td></tr><tr><td>

Telecommunication Network Inventory

</td><td>

-   **[Define a network model relationship](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/telecom-network-inventory/create-network-model-relationships.md)**
    -   Hardware models visible in Inventory Template picker: Template Managers can now select hardware models \(cmdb\_hardware\_product\_model\) from the Inventory Model picker when creating or editing an inventory template. Previously, models of this type were not visible in the picker if they were not tagged with a TNI inventory category. Hardware models created anywhere in the model catalog are now always included in the picker.
    -   Parent Model selection retained when relationship type changes: When a Catalog Manager changes the relationship type after already selecting a Parent Model, the selected model value is now retained if it is a valid model type. Previously, changing the relationship type could clear a validly selected Parent Model value.
-   **[Create an equipment model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/telecom-network-inventory/create-equipment-models.md)**

All model types are made visible in Model Relationship Parent Model picker: Catalog Managers can select any model type, including hardware models and product models, as the Parent Model when creating a model relationship, regardless of which relationship type is selected.


</td></tr><tr><td>

Telecommunications Service Operations Management \(TSOM\)

</td><td>

-   **[Fortinet discovery with large port counts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/telecom-service-ops/telecom-discovery-via-fortinet.md)**

Fortinet devices with more than 600 ports no longer fail discovery due to memory constraints. Ports are now processed in batches to prevent out-of-memory errors.


</td></tr><tr><td>

Third-party Risk Management

</td><td>

-   **[Third-party and engagement element assessments](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/tprm-monitor-tp-elements.md)**

After upgrading to version 23.0.7, you can review element-level assessments across all engagements for a third party. Element-level assessments are no longer scoped to a specific engagement. When you scope an assessment, issue, or task to an element, the **Element** field is required. This option is available only when the third party uses the Smart Assessment Engine. Third-party and engagement contacts respond to element-scoped assessments in the third-party portal the same way they respond to engagement-scoped assessments.

-   **[Risk scoring for third-party elements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/tprm-monitor-tp-elements.md)**

After upgrading to version 23.0.7, element assessment scores roll up through relationship scores calculated from questionnaire-level evidence, replacing the previous entity-based rollup calculation. Engagement and third-party risk-area calculations include assessments sent on linked elements. Linking an element with existing assessment evidence to a new engagement calculates a risk rating for that link automatically, without requiring a new assessment.

-   **[Access external and internal tasks from separate modules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/tprm-ws-list-page.md)**

After upgrading to version 23.0.7, you can access external and internal tasks from separate modules. The Tasks module is split into **External Tasks** and **Internal Tasks** on the list page. This separates external tasks from the internal task functionality added in element collection.

-   **[Expanded access to reassign Smart Assessment Engine questionnaires](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/tprm-portal-questionnaire-ownership.md)**

After upgrading to version 23.0.7, the TPR administrator \[sn\_vdr\_risk\_asmt.vendor\_risk\_admin\], TPR assessor \[sn\_vdr\_risk\_asmt.vendor\_assessor\], and TPR manager \[sn\_vdr\_risk\_asmt.vendor\_risk\_manager\] roles now include the sn\_smart\_asmt.reassign role. Users with these roles can reassign Smart Assessment Engine questionnaires.

-   **[Decimal precision for DORA monetary values](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/tprm-dora-roi.md)**

After upgrading the Digital Resilience Third-party Information Register application to version 23.0.3, and if you have the TPR administrator \[sn\_vdr\_risk\_asmt.vendor\_risk\_admin\] role, you can set decimal precision to `-6`, `-3`, `0`, or `2` for monetary value fields. Previously, only `-6`, `-3`, and `0` were supported. This applies to Master Template and CSV downloads. The default precision remains `0`. This change doesn't affect UI display, upload and validation, individual table downloads, or database storage.

-   **[CSV download applies only filtered records when all records are selected](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/tprm-excel-upload-download-request.md)**

After upgrading the Digital Resilience Third-party Information Register application to version 23.0.3, when a filter is applied to a list and you select all records for CSV download, only the filtered records are included. Previously, all records were downloaded regardless of the applied filter.

-   **[Issue generation rules no longer create issues for hidden questions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/tprm-generate-issue-rule.md)**

After upgrading to version 23.0.7, an issue generation rule that targets a question with a visibility condition no longer creates an issue when that question is isn't visible to the respondent. Previously, the rule could create an issue for a question the respondent never saw.

-   **[Product model record created after SBOM document processing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/sbom-activate.md)**

After upgrading to version 23.0.7, after a third party submits an SBOM file and processing completes, a product model record is created on the third-party record. The record is visible in the Product Models related list. A plugin dependency is added to support parallel processing.

-   **[Legal person identifier validation warns instead of blocking for non-LEI/EUID codes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/tprm-dora-roi.md)**

After upgrading the Digital Resilience Third-party Information Register application to version 23.0.3, after a third-party service provider record with a legal person type and a non-LEI/EUID identification code is submitted, you receive a warning. The save is no longer blocked. This applies to both the Vendor Management Workspace and Excel Upload.

-   **[Notice period fields accept a value of zero](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/tprm-validation-roi.md)**

After upgrading the Digital Resilience Third-party Information Register application to version 23.0.3, the notice period fields \(`B_02.02.0100` and `B_02.02.0110`\) now accept a value of `0`. Previously, a value of `0` was rejected as if the field were empty.

-   **[Data quality warnings CSV added to CSV ROI report package](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/tprm-validation-roi.md)**

After upgrading the Digital Resilience Third-party Information Register application to version 23.0.3, the CSV report package includes a `Data_Quality_Warnings.csv` file in the `Consolidated_Reports.zip` archive. This file provides supplementary data quality checks beyond the Level 3 \(DPM\) and Level 4 \(LEI\) validations.

These warnings flag potential data inconsistencies — such as duplicate rows, missing assessments, orphaned contracts, supply chain gaps, and criticality conflicts — but don't prevent submission. Addressing them helps maintain data accuracy. Each warning includes the sheet name, row number, contract reference, and a descriptive message.

-   **[Parent record navigation added to DORA third-party, third-party engagement, and contract records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/tprm-dora.md)**

After upgrading the Digital Resilience Third-party Information Register application to version 23.0.3, a reference field is available on DORA third-party, third-party engagement, and contract records. Use it to navigate back to the related parent record after arriving from a related list. Previously, there was no way to return to the parent record from these pages.

-   **[Excel export for DORA Functions requests no longer fails on large datasets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/tprm-dora.md)**

After upgrading the Digital Resilience Third-party Information Register application to version 23.0.3, exporting a Functions-type Excel drop-down download and upload request no longer fails when drop-down fields reference large CMDB or reference tables. Results are capped at 10,000 records per drop-down field.

-   **[Automated quarterly CSV download for Register of Information reports](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/tprm-dora-roi.md)**

After upgrading the Digital Resilience Third-party Information Register application to version 23.0.3, a quarterly scheduled job \(**DORA: Quarterly CSV download**\) generates the CSV Register of Information report for the previous quarter automatically, copying settings from the most recent download request. Previously, a TPR administrator generated this report manually each quarter. The scheduled job is inactive by default; a TPR administrator \[sn\_vdr\_risk\_asmt.vendor\_risk\_admin\] can navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs** and activate it before it runs.

-   **[Rank 1 supply chain records update automatically when a contract's service provider changes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/tprm-dora.md)**

After upgrading the Digital Resilience Third-party Information Register application to version 23.0.3, and if you change the service provider on a DORA contract record, the associated Rank 1 supply chain records update automatically. The records reflect the new provider or recipient.

-   **[Third party field pre-populated when creating an element from an engagement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/tprm-tpe-form.md)**

After upgrading to version 23.0.7, the **Third party** field is auto-populated when you create a third-party element from either the third-party record or an engagement's **Elements** tab. Previously, the field was editable and empty in both cases.

-   **[Smart Assessment Engine rating scale available from workspace navigation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/tprm-risk-rating-scales-config.md)**

After upgrading to version 23.0.7, the SAE default rating scale table is available from the Vendor Management Workspace navigation, under **Assessment Setup**. Previously, this table wasn't accessible from workspace navigation.


</td></tr><tr><td>

Threat Intelligence Security Center

</td><td>

-   **[Automated correlation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/security-management/automated-correlation-rules.md)**

Confirmed relationship rules now apply reputation checks and direction-agnostic deduplication, producing accurate source-of-traffic and destination-of-traffic relationships. Potential correlation rules are more selective and correlation requires a reputation match plus multiple shared observables.

-   **[TISC integration within SIR Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/security-management/tisc-sir-workspace.md)**

Directly link or unlink TISC entities in TISC Context tab of SIR workspace. The changes made in TISC context or TISC internal intelligence tab reflect bidirectionally.

-   **[CrowdStrike Falcon EDR integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/security-management/crowdstrike-edr-integration.md)**

Indicators sent to CrowdStrike Falcon EDR now carry "TISC Intelligence" as the source. A configuration option applies the TISC expiration time, falling back to the observable type expiration when the option is disabled. The Prevent action is supported alongside Detect.

-   **[Configure Premium Threat Feed for CrowdStrike](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/security-management/premium-threat-feed-for-crowdstrike.md)**

Ingest Vulnerability intelligence from CrowdStrike. Feed configurations are set to read-only when they're enabled, preventing changes that would disrupt an ingestion already in progress.

-   **[Review revoked MITRE tactic and technique associations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/security-management/tisc-review-revoked-mitre-associations.md)**

MITRE ingestion now provides a review queue for revoked technique-to-tactic associations that the newer MITRE ATT&amp;CK version no longer defines.


</td></tr><tr><td>

Zero Copy Connectors

</td><td>

-   **MySQL connector moved to Primary with Preview label**

The [MySQL](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/mysql-zcc.md) connector moved from the Community connector list to the Primary connector list. This connector is available with a **Preview** label, indicating that performance enhancements are ongoing.

-   **PostgreSQL connector moved to Primary**

The [PostgreSQL](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/postgresql-zcc.md) connector moved from the Community connector list to the Primary connector list.


</td></tr></tbody>
</table>**Parent Topic:**[Release notes summaries for Brazil features](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/release-notes-summaries.md)


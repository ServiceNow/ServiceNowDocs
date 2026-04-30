---
title: Zurich General Availability release highlights
description: High-level overview of products and features in the ServiceNow AI Platform Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 31
breadcrumb: [Zurich release notes]
---

# Zurich General Availability release highlights

High-level overview of products and features in the ServiceNow AI Platform Zurich release.

## Overview of the Zurich General Availability \(GA\) release

## ServiceNow AI Platform

-   **AI**
    -   Build Agent: Transform natural language prompts into complete, full-stack ServiceNow apps in minutes instead of days. Watch the AI agent plan, create, and edit in real-time for full transparency and control. Iteratively edit and refine existing apps with simple, conversational feedback until they are ready to deploy.
    -   AI Agent Fabric: Direct access to external data sources using Model Context Protocol \(MCP\). AI agents can now collaborate with other AI systems with Agent2Agent protocol. Build automations that work across your entire tech stack.
    -   Model provider flexibility: Match each AI workflow with the ideal model provider for its specific requirements. Rapidly test, switch, and update AI skills without rewriting workflows or managing APIs. Deploy with confidence and control with built-in governance, fallback logic, and real-time monitoring in AI Control Tower.
-   **Workflow**
    -   Agentic playbooks: Optimize workflows by exposing playbooks to AI agents and conversational interfaces. Increase productivity with humans and AI working side by side on the tasks that they can each execute the best. Keep humans in the loop as needed for verification, approval, or mandatory manual steps.
    -   Reusable triggers: Easily create schedules with time zone support, start/end day and time, and schedule frequency. Create custom external triggers that act like webhooks to launch ServiceNow automations. Empower low code users to reuse saved triggers without being exposed to the complexity of the overall workflow.
    -   Flow history: Easily access and revert to earlier versions of flows or subflows. Track workflow changes for transparency and increased collaboration across teams. Streamline workflow management in a single, action-driven workspace.
-   **Process Mining**
    -   Task Mining:

        Extend Process Mining reach into the last mile of user-level tasks for end-to- end process visibility and improvement. Analyze how users on Windows and Mac desktops execute tasks in any app \(eg Excel, SAP Business Client, browser\) within broader processes for end-to-end mining. Identify and act on improvement opportunities at the desktop level for AI Agents and automation.

    -   Process Mining enhancements: Surface easy to understand insights so business stakeholders can make faster, informed decisions on improvement opportunities. Accelerate legacy or low ROI app rationalization onto the ServiceNow AI Platform with Now Assist for playbook generation directly from the process map in Analyst workbench. Identify and prioritize automation and workforce optimization opportunities with touchpoint and idle time analysis.
-   **Security and Privacy**
    -   ServiceNow Vault Console: Enable guided data classification and protections for CSM and FSO. Leverage auto-classification and recommended actions for protecting your data. Visualize ServiceNow Vault tool performance with dashboards that showcase usage, impact and effectiveness in securing sensitive data.
    -   Data Privacy enhancements: Replace "Sensitive Data Handler" with Data Privacy to simplify and consolidate the handling of PII and PHI for Virtual Agent. Find sensitive data faster with Now Assist for Vault to Create data discovery jobs and use natural language to create custom regular expressions. Discover language-based data for scheduled jobs, like names, locations, groups, etc. \(NER\).
    -   Field Encryption enhancements: Define custom encryption rules for specific columns and rows for ease of compliance track. Assign specific keys to data within a row to allow visibility to only authorized users. Apply encryption-backed access control to the most sensitive data. View which role has access to encryption keys associated with a field, powered by Now Assist for Vault.
    -   Machine Identity Console: Discover and manage all machine identities across your ServiceNow instance. Monitor API access use and authentication methods for all integrations. Use the machine identity security score to see actions you can take to improve your machine identity security.

## Workflow Data Fabric

-   **Workflow Data Fabric Hub**
    -   Workflow Data Fabric Hub: Discover and manage external data from one interface, including Snowflake, data lakes, and data warehouses. Create data fabric tables to access external data as if it's native to the ServiceNow AI Platform. Enable zero copy to drive workflows, analytics, and AI with real-time external data.
    -   Zero Copy Connectors: Query external data as if local with federated SQL—no ETL, storage, or sync needed. Trigger AI and workflows in real time, acting on live, governed data without sync delays or duplication. Help protect sensitive data with scoped, time-bound access—minimizing risk and easing compliance.
    -   Zero Copy Connector for ERP: Enable bi-directional access to ERP objects—like data and orders—as reusable data products without copying data to ServiceNow. Use data products to query or update ERP in App Engine apps or power agentic AI with built-in business logic and semantics. Let developers build workflows and AI agents without ERP expertise—helping to save time and consulting costs.
    -   RPA Migration Accelerator: Scan and analyze existing bots automatically to evaluate complexity, usage, and migration readiness. Map legacy components to ServiceNow equivalents using predefined logic. Track migration progress and tasks in Automation Center with guided workflows.
    -   Workflow Data Fabric tokenization: Unify product consumption under a single fabric credit to reduce friction. Monitor usage across the Workflow Data Fabric portfolio with clear, consolidated dashboards. Activate flexible adoption with credit- based SKUs that support any Workflow Data Fabric product.
    -   AI Agents for Integration Hub: Use out-of-the-box AI agents to trigger Integration Hub actions across systems with minimal setup. Orchestrate complex workflows using the AI Agent Orchestrator to plan and coordinate multiple agents to fulfill business goals. Automate tasks with AI agents using spokes to drive cross-enterprise workflows that connect systems, apps, and departments.

## Technology Workflows

-   **IT Service Management &amp; DevOps**
    -   Digital End-User Experience \(DEX\): Proactively monitor and assist users with Microsoft Teams issues before they encounter problems during a call. Take remedial action in bulk on up to 1,000 devices simultaneously. Enable secure use of DEX for utility companies and government institutions within the United States through newly added GCC support.
    -   Digital Product Release: complex rollout plans: Differentiate between a validation release \(traditional use case\) and a rollout release \(new use case\). Connect CIs to release phases for future use in change requests and other activities. View connected CIs in a table view with selection boxes, making it easier to attach them to change requests.
    -   Self-service in AI agent &amp; voice: Submit tickets and requests instantly with a dynamic, conversational voice agent that eliminates tedious forms. Check, manage, and escalate tickets effortlessly via phone or Virtual Agent, keeping employees informed in real time. Troubleshoot IT issues step by step using a contextual voice agent that tailors every solution to each user’s profile
    -   AI agents for change management: Streamline effective change scheduling. Facilitate high quality change data through conversational change. Understand and mitigate potential conflicts and impacts caused by changes. Identify and assess risk factors associated with a change.
-   **IT Operations Management**
    -   Impact analysis: Minimize downtime of critical systems. Focus on the signal and root cause in alerts, ignore the noise. Collaborate with third party agents from leading Application Performance Monitoring \(APM\) and Observability solutions.
    -   Kubernetes visibility agent: Map critical service relationships via a Kubernetes visibility agent \(KVA\) that analyzes live network traffic. Reduce CMDB noise with smart filtering and ephemeral cleanup. Deploy visibility across clusters faster with new Helm chart options.
    -   Deep pattern discovery via AWS: Enrich the CMDB with AWS system agents - no additional credentials required. Discover complex software and dependencies for compliance and licensing. Eliminate the need for collectors or MID Servers for each Cloud Provider.
    -   Simplified Health Log Analytics: Get value early with ServiceNow logs - then add new integrations of industry leading solutions. Enjoy more flexible ways to host HLA including on-premises and cloud friendly options. Breeze through initial steps with less set- up, smarter parsing, and more automated mapping.
    -   Cloud Account Management compliance dashboard &amp; asset explorer: Address ownership gaps and policy drift quickly from a single compliance view. Map the full range of cloud assets clearly across all major providers. Streamline account setup from guided, configurable request forms.
    -   Key integrations for Service Observability: Amass critical health metrics via new APM and Cloud integrations. Utilize new Dynatrace and LogicMonitor agentic integrations for robust triage and remediation. Coordinate intelligent action with the ITOM Agent Fleet.
-   **Configuration Management Database \(CMDB\)**
    -   Retooled configuration management user experiences: Cleanly record critical new technology from a streamlined layout within the CMDB Workspace. Reduce user error and training time with a simpler, more consistent UI for creating and editing records. Accelerate insight with shared presets that let teams launch Unified Maps filtered to relevant services or domains.
    -   Data certification dashboard: Validate critical CI data from a focused dashboard that highlights gaps and drives accountability. Empower service and domain owners to take action with tailored views into their own data quality. Simplify audits and reporting by making certification status visible and trackable in one place.
-   **Software Asset Management**
    -   Help manage software asset requests: Accelerate hardware request fulfillment time with AI agents. Enhance fulfiller experience by automating a large volume of administrative tasks associated hardware requests. Reduce operational bottlenecks and optimize workflows for improved productivity at scale.
    -   Create software reclamation rule: Provide task workflow to putaway assets into their respective granular locations \(space/place\) in a warehouse. Automatically update asset records after assets are secured to maintain accurate inventory data. Mitigate the risk of losing or misplacing assets and improve inventory accuracy.
    -   Evaluate software removal candidate: Use AI agents to identify and recommend software installations. Continuously evaluate usage data and context to ensure appropriate actions are taken. Reduce manual effort, minimize compliance risk, and increase license cost savings.
    -   Microsoft Hyper-V virtualization support:Accurately showcase licenses required for compliance. Reduce licensing costs by performing optimization on Windows Server. Generate reports on on-premise optimization realized savings.
    -   Adobe SaaS guided setup: Configure Adobe integration with Software Asset Management with step- by-step, prescriptive guidance. Simplify complex setup process with clearly outlined setup phases. Decrease time to value by minimizing onboarding time and configuration errors.
    -   Organizational license positions: Use current reconciliation results in effective license position \(ELP\) reporting feature. Define how to group and filter license consumption by various organizational structure fields. Create and group custom fields for reconciliation results.
    -   SQL Server high availability compliance: Capture the complete architecture and key attributes of license consumptions using ServiceNow Discovery. Automatically determine passive failover SQL instances that don’t require a license. Calculate license compliance for SQL Server in always-on availability group.
-   **Cloud Cost Management**
    -   Enhanced support for MCA customers: Enable out-of-the-box support for Azure Microsoft Customer Agreement \(MCA\) accounts. Support automated ingestion and mapping of billing data tied to the MCA model. Reduce onboarding time and eliminate the need for customer configuration.
    -   Robust Azure billing data exports: Schedule actual or amortized cost exports in Azure and use CCM to directly retrieve them from Azure Blob Storage. Reduce reliance on throttled APIs and provide more predictable ingestion timing. Improve billing data visibility and reduce troubleshooting.
-   **Hardware Asset Management**
    -   Help manage hardware asset requests: Accelerate hardware request fulfillment time with AI agents from sourcing to procurement. Enhance employee experience in managing large volume of hardware requests and administrative tasks. Reduce operational bottlenecks and optimize workflows for improved productivity at scale.
    -   Asset putaway: Provide task workflow to putaway assets into their respective granular locations \(space/place\) in a warehouse. Automatically update asset records after assets are secured to maintain accurate inventory data. Mitigate the risk of losing or misplacing assets and improve inventory accuracy.
    -   Employee asset receiving: Prompt employees to receive assets in transit from Employee Center notifications. Automatically update any related PO, shipment, or asset task after an employee receives an asset. Increase data accuracy with real-time updates to asset records upon receipt.
    -   Stockroom receiving: Standardize the receiving process with an intuitive UI to reduce time spent receiving assets. Support flexible receiving to meet asset managers’ needs, including bulk and import options. Improve quality of data with prompts to encourage filling in blank data spots or creating assets upon receipt.
    -   Asset attestation remediation: Initiate, execute, and track asset attestation request from inventory workspace via playbook experience. Provide remediation tasks to investigate assets rejected by users. Introduce attestation via the Now Mobile application.
-   **Enterprise Asset Management &amp; Operational Technology Asset Management**
    -   Asset conditions: Provide structured, attribute-driven questionnaires enabled by work order tasks. Make proactive decisions about asset health with consistent assessment and improvement of equipment health. Enable consistent, scalable reporting across the organization.
    -   Asset performance: Report asset uptime/downtime with maintenance activities. Track asset failures by tracking mean time between failures \(MTBF\) and mean time to repair \(MTTR\). Increase uptime, output, and reduced scrap of assets to improve OEE.
    -   Inventory demand reporting: Provide 5 new reports for different asset counts and types of demand. Enable data-driven decisions that reduce stockouts or excess inventory with expanded reporting. Ensure that the right parts are available at the right time for the right price to improve planning accuracy, lower carrying costs, and enhance uptime.
-   **IT Asset Management for Financial Services**
    -   Asset Audit Response: Reduce legacy communication between asset management and compliance teams with workspace to manage requests for evidence. Deliver accurate responses to regulatory audits with out-of-the-box financial regulation content. Leverage guided experience and automation to fulfill evidence requests and maintain clear historical records of audit processes.
-   **Strategic Portfolio Management**
    -   AI strategy in AI Control Tower: Gain unified visibility into all AI-linked goals, work, risks and priorities. Empower AI leadership with department level and enterprise-level analytics. Drive strategic control by identifying trends, gap, and high-risk areas in AI execution.
    -   Financials on planning items: Enable financial planning directly on Epics, Demands and Projects without integration with core tasks. Reduce task dependencies for financials, which is ideal for lean and agile portfolios. Improved support for agile forecasting; capturing cost earlier in portfolio planning.
-   **Collaborative Work Management**
    -   Agile sprint planning: Leverage sprint planning tab to track backlog and create sprints. Create stories and epics directly in Collaborative Work Management \(CWM\). Plan any CWM task in an agile manner by create story points and adding them to sprints .
    -   Connected work: Easily import any work type, such as incidents, changes, stories and tasks into a CWM board. Plan and execute work across multiple work types with up-to-date information on a single pane of glass. Manage work flexibly with custom columns and views, such as List, Gantt, Kanban, and Sprint Planning.
-   **Enterprise Architecture**
    -   Monitor AI governance on portfolio tab: Get visibility to the AI portfolio in your company. Connect AI assets to other elements in your portfolio and CMDB.
    -   Manage TRM products within business applications: Associate business application with TRM products. Enforce governance policies more effectively.
    -   Map technical capabilities to business apps: Clearly define and manage technical functions across IT, systems, and software. Update product capabilities with business applications. Enhance governance by linking TRM to defined capabilities.
-   **Operational Technology Visibility**
    -   Operational technology shift summarization: Access a centralized and reliable list of OT changes using generative AI. Inform shift handovers with a summary of activities or changes from the past 24 hours. Monitor issues with detailed configuration item level summaries across ISA equipment entity.
    -   Agentic search for operational technology: Search in natural language to access OT CI-related information. Use AI agents to generate database query code for fast results. Get search results in the Industrial Workspace for quick access.
    -   Operational technology device import: Import OT devices into CMDB with a single upload step with ServiceNow AI Agents. Execute unstructured excel uploads with automated transformation into the template. Automatically create staging table records, with the option to correct the invalid records.
-   **Operational Technology Service Management**
    -   Operational technology incident summarization: Accelerate diagnosis and action through generative AI incident summarization. Resolve recurring issues faster with auto-generated knowledge and resolution notes. Improve root cause identification with access to historical incident patterns.
-   **Risk Products &amp; Environmental, Social and Governance \(ESG\)**
    -   AI strategy: Create AI demand, roadmap, portfolio, and scenario planning to achieve business outcomes. Track progress against AI strategic goals and targets in a unified way. Monitor AI work, investments, and proactively address project drifts.
    -   Unified AI asset inventory: Accelerate the discovery and management of AI agents across the enterprise. Manage the entire lifecycle of the model and data used for training and prediction. Automate via Rest APIs and integration with AWS Bedrock, Azure AI Agent Service &amp; Copilot.
    -   Enterprise AI value: Drive data-informed decisions regarding AI adoption using value metrics and performance indicators at your fingertips. Assess instantly the value and usefulness of your AI implementation. Customize your value dashboard to meet organizational requirements.
    -   AI Governance: Gain unified visibility, providing useful metrics to assess security and privacy issues for AI agents. Enable effective management of Now Assist and ServiceNow AI agents implementation through governance and control settings. Become proactive with an extensive AI risk and compliance scoring across the whole system.
    -   Bulk access update configuration for entity- based user access: Select one or more entities and associated record types to define the scope for access restriction. Preview impacted records by type and evaluate the scope and impact before applying changes. See the number of records impacted per record type; detailed result summaries and logs provide full auditability and traceability.
    -   Risk assessment projects in grid mode: Create an assessment project with appropriate context by adding attributes such as entity, RAM, etc. and defined stakeholders. Compare, edit and prioritize risks and controls quickly with a flexible, spreadsheet-style risk and control self- assessment. Address risks one at a time or in bulk individually or simultaneously with other stakeholders.
    -   Scoring normalization, collaboration and scanning for Smart Assessment Engine: Standardize different scoring scales to enable fair comparison across assessments with options for linear or custom formulas. Enhance collaboration by enabling multiple stakeholders to work simultaneously on a single assessment. Work across mobile and workspace platforms to drive efficiency and reduce manual data entry errors with barcode scanning.
    -   Now Assist for IRM: Leverage AI to summarize risk events into actionable insights to improved decisioning. Automate the mapping of incoming regulatory alerts to recommended controls with AI. Create common control objective and retire similar control objectives using Gen AI.
    -   Smart Assessment Engine for Operational Resilience: Design and execute assessments seamlessly while ensuring compliance and efficiency. Collaborate with multiple stakeholders on Importance and Impact Tolerance Assessments. Standardize different scoring scales, allowing for fair comparisons across assessments.
    -   O365 integration: Create management reports for Business Impact Analysis, Business Continuity Plans and events using the Microsoft Word add-in. Export reports to Word that can be sent to executives and management for review and approval. Leverage template to save time and create consistency in reporting.
    -   New processing activity layout: Reflects step-by-step workflows to improve readability and usability. Enables easier grouping, segmentation, and analysis of related actions. Supports more effective compliance assessments, risk evaluations, and collaborative reviews.
    -   New dashboarding experience: Intelligently map processing activities, issues, and controls to global regulatory requirements. Instantly visualize compliance posture across regulations. Proactively identify gaps against applicable laws and regulations.
    -   Data subject segmentation: Capture diverse data subject profiles within a single processing activity. Improve accuracy in risk scoring, DPIAs, and compliance mapping. Enable faster, data-driven analysis of privacy impact by user segment.
    -   Smart Assessment Engine for TPRM: Leverage the SAE for internal and external parties for better navigation, template use and question subsections. Take advantage of new collaboration and score normalization features within third-party assessments. Third-party portal undegraded to support Smart Assessments and published assessment usage.
    -   Now Assist for ESG: Automate accurate and scalable extraction of ESG-relevant data from energy and utility bills. Categorize energy consumption, carbon emissions and waste disposal from diverse invoice formats. Accelerate the turnaround time for sustainability insights across enterprise operations.
    -   Estimations for metric data: Provide an estimate for use in reporting and disclosure in cases where the actual data is not available. Select an estimation method for the data and submit. Replace the estimated data with actual when possible, for final disclosures and reporting.
    -   Tasks for automated metrics: Review data that is automatically collected for the sustainability program to ensure accuracy before it can be used for reporting. View the supporting data associated with the task for better transparency and ease of use. Update data with a justification, approve or reject metric data task.
    -   Real-time data from DEX - energy consumption visibility: Seamlessly ingest data from ServiceNow Digital End-User Experience into the Sustainable IT Dashboard. Enhance the accuracy and reliability of sustainability reporting for IT assets, such as desktops and laptops. Deliver more precise calculations of CO2e emissions with real-time usage data.
    -   Workspace reporting with Platform Analytics: Create and view reports directly within the ESG workspace for sharing with stakeholders. Build tailored dashboards using the platform’s configurable components to visualize emissions, diversity, compliance, and other ESG indicators. Embed reports into regular ESG review cycles with sustainability teams, executives, and auditors to improve visibility.

## Core Business Services

-   **HR Service Delivery**
    -   Company news and events AI agent: Access company updates with clear, conversational responses on demand. Filter news and events by location, time, or topic—no more digging through portals or emails. RSVP, get more details, or explore related updates directly from the chat.
    -   Interview setup for recruiters: Enable recruiters to set up interview phases with custom names, durations, and key parameters. Edit and update phases at any time before applying them to a requisition. Empower recruiters to reuse interview plans across roles to drive consistency and speed.
    -   Streamline employee-to-alumni transitions: Let employees update personal details to stay connected after offboarding. Allow alumni to self-register using system-verified employment details. Automatically create alumni accounts during offboarding with a configurable process.
    -   Browser extension for Employee Center: Give employees access to Employee Center content via a browser extension. Allow admins to curate various content types available on the browser extension for a given website. Equip employees with access to notifications and search on ServiceNow through the browser extension.

-   **Health and Safety**
    -   Contractor service center: Streamline communications and processes for contractors via a secure single portal. Facilitate work permits and access prequalification tasks and required safety protocols. Track contractor qualifications and gain insight into workflow approvals.
    -   Conversational incident reporting: Streamline safety reporting processes guided by AI. Empower employees to quickly log incidents with simple interactions. Reduce frustration and time delay from filling out lengthy forms.

-   **Workplace Service Delivery**
    -   Cleaning schedule optimization: Schedule cleaning based on how many people and spaces are used Adjust workplace cases based on space attendance. Automatically change reservable status for spaces as conditions change.
    -   Indoor mapping updates: Automatically detect CAD file changes and initiate the upload process based on predefined triggers. Apply the appropriate map configuration and carry out imports with minimal manual effort. Track success and errors, notifying map admins of both completed and failed attempts.
    -   Bulk workplace moves: Make creating and managing bulk move requests as simple as uploading a spreadsheet. Streamline managing employee relocations to reduce manual workload, minimize disruptions, and mitigate errors. Manage relocation conflicts and resolve data inconsistencies with a conflict resolution interface.

## CRM

-   **Customer Service Management**
    -   Task plan templates: Speed up case handling by auto- applying task templates based on predefined conditions. Enable process owners to adapt quickly to evolving business rules and regulations. Enhance task visibility with hierarchical parent-child case task templates.
    -   Record producer in CSM Configurable Workspace: Reduce admin effort of re-creating the portal intake process with a different service definition. Improve agent case creation efficiency by enabling an existing service definition to launch record producers. Streamline case experience for consumer and agent personas using a single intake view.
    -   Customer history component: Improve agent productivity with a view of customer activity in workspace. Filter by type or date or search to find specific activities. Available in the contextual side panel for easy access and visibility into the case.
    -   Data classification: Simplify administrator experience when viewing and applying protections to sensitive data. Decrease time to value for platform administrators by providing OOTB data classifications.
    -   Declarative framework enhancements: Improve admin experience with a UI- based experience for setting and viewing access controls. Reduce customization with additional filter options and table associations. Reduce time to value by leveraging pre-configured responsibility configurations.
-   **Sales and Order Management**
    -   Complex product modeling: Improve product modeling accuracy for complex, real-world product configurations within CPQ. Streamline data entry with structured input for faster, more accurate quote and order creation. Reduce fallout rates with clean, structured data that supports fulfillment automation.
    -   Characteristic-based costing: Calculate more accurate margins to help avoid overquoting or underquoting. Improve bottom-line and deal profits with better discount guidance and governance. Drive higher CSAT with competitive and transparent pricing on every quote, in every situation.
    -   Lead-to-cash command center: Boost operational productivity with centralized data, reduced swivel chairing, and streamlined workflows. Identify delays or issues early to reduce financial risk and operational impact. Proactively resolve milestone delays to help ensure timely revenue recognition.
    -   Powerful CPQ configurator via Logki.ai acquisition: Seamlessly sync SOM product data with the new CPQ configurator. Accelerate solution configuration and sales with new advanced guided engine embedded in SOM's CPQ engine. Boost quote-to-cash speed and accuracy with SOM pricing synced seamlessly with the new advanced configurator
-   **Field Service Management**
    -   Hybrid capacity model: Define and manage capacity using a blend of real-time schedules and forecasted availability. Improve appointment availability and planning accuracy—especially in hybrid workforce environments. Balance short-term precision and long- term planning, reducing SLA violations and improving customer satisfaction.
    -   Schedule Optimization enhancements: Assign technicians based on configurable weighted criteria like skill, efficiency, or cost—not just proximity. Optimize only a subset of agents and tasks, helping avoid unnecessary changes to the full schedule. Connect scheduling with business goals such as SLA compliance and first-time fix rates.
    -   Dispatcher Workspace enhancements: Display multiple time zones in the scheduling view to coordinate across regions without manual conversions. Expand technician pool to include those from outside their assigned groups or territories in response to demand spikes. Flag and assign tasks directly from list or record views without the need to switch into the Dispatcher Workspace.
    -   Smart Assessment for Field Service Questionnaire enhancement: Scan asset barcodes directly into mobile questionnaires, reducing manual entry and errors. Automatically generate work order tasks based on questionnaire responses or scores. Validate numeric inputs in real time, alerting technicians when values fall outside acceptable ranges. Flag failed uploads, allowing for retry or replacement without requiring form resubmission.

## Industry Solutions

-   **Financial Services Operations for Banking**
    -   Task plan templates: Establish consistent procedures for standard banking processes, such as remote check deposit enrollment. Increase process visibility by laying out all tasks, task statuses, and task owners. Enable permitted business users to create and change task templates. Dynamically adapt templates as needed with simple configuration.
    -   Card data enhancements: Transmit card data to networks while maintaining advanced, PCI-compliant tokenization. Reduce development costs by centralizing card-related data in a standard, reusable structure. Adapt quickly to new payment types with an extensible data model.
    -   Dispute analyst workspace enhancements: Enable dispute analysts to work in tandem with AI through a single user interface. Surface relevant tasks to dispute analysts throughout the chargeback process. Manage all dispute tasks and source insights directly in the workspace - without switching tabs. Support the complexity of dispute cases with more modular workspaces for analysts.
    -   Mastercard dispute processing enhancements: Accelerate the dispute case lifecycle with automated task creation and pre- populated data. Comply with Mastercard's required formats, SLAs, and input standards to maximize win rates. Receive acquirer updates in real-time with automatic data flows between ServiceNow and Mastercom. Reduce development costs and time to market with an out-of-the-box integration to Mastercard.
-   **Technology Industry**

    Technology Provider Service Management

    -   Support renewals &amp; expansion: Automatically assess renewal risk and expansion potential 120 days before contract end. Leverage personalized renewal strategies based on usage, engagement history, and outcomes. Empower CSMs to manage a higher volume of accounts with repeatable and scalable renewal processes.
    -   Trigger risk mitigation touchpoint: Auto-triggers draft meeting invites on high-risk signals for timely issue response. Simplifies meeting setup with pre-filled context, suggested agenda, and invitees based on risk. Helps CSMs prevent churn with timely prompts and consistent follow-up across large portfolios.
    -   Product Adoption Data: Gain a real-time view of product adoption across every customer engagement. Spot underused products or declining usage early, before it threatens renewals or growth. Launch targeted success plays and monitor customer health to drive value from real-time usage signals.
    -   Foundation data sync for Service Bridge: Reduce manual data transfers and give customers faster access to information. Improve service transparency by making CMDB and asset data available in near real time. Speed onboarding and improve provider-customer alignment with Service Bridge data sharing.
    -   Diagnostic framework support: Guide agents through system-suggested diagnostic steps to identify the root cause of product or service issues. Accelerate resolution by generating follow-up tasks and instructions tailored to the problem. Standardize troubleshooting with reusable diagnostic flows for faster, consistent service and quicker agent onboarding
-   **Telecommunications**

    Telecommunications Network Inventory \(TIN\)

    -   Floor map visualization with metric overlay: Maintain detailed floor maps of data centers and network sites that provide engineers with accurate visual access to equipment. See site and data center floor and equipment health with a color-coded view for incident, change, alerts, and metrics in real-time. Enhance efficiency, resolve faster, and meet SLAs by quickly identifying and addressing issues. Optimize floor space and capacity requirements for optimal allocation and utilization.
    -   Converged Service Operations Workspace: Use integrated network visualization and drill down to details from the Service Operations Workspace, and make informed decisions faster. Leverage a dedicated workspace tailored for different network and facility personas, enhancing role-based efficiency. Drill down to view the impact of incidents, change, and alerts on floor maps with equipment and rack health overlays, enabling faster issue resolution.
    -   CMDB classes for data center power management: Model all types of data center power equipment to gain comprehensive visibility. Model and visualize shared power connections between racks and equipment, quickly understand power incident or change. Enable customized rack grouping, owners can securely access and manage only their specific group of racks. Proactively monitor data center power equipment health in real time. Leverage insights into power incidents and change to proactively notify impacted customer services.
    Sales and Order Management for Telecom \(SOMT\)

    -   TM Forum API updates: Automate quote generation and improve win rates with TMF648 compliant, catalogue-driven customer quoting. Reduce order fallout by helping ensure accurate product and service eligibility with compliance to TMF679 standards. Streamline complex product and service order fulfillment through direct alignment with TMF622, TMF641, and TMF645 standards.
    Field Service Management for Telecom \(FSMT\)

    -   Work Order API: Help create, retrieve, update, and delete work orders, enabling smarter scheduling. Provide event notifications related to work orders, enhancing task visibility. Allow search of a work order on both external ID and the system ID aligned to the latest TM Forum industry standards.
    Telecom Service Management \(TSM\)

    -   Diagnose and repair service issues framework: Automate diagnostics and repairs across incident, case, and order workflows with a unified framework to streamline operations. Select and run tests dynamically with accuracy based on the product model and task context. Creates or updates repair tasks automatically based on test results and speed resolution. Make use of built-in flexibility and low- code capabilities to configure changes without heavy scripting.
    -   Analyze and resolve network incidents: Analyze incidents rapidly and reduce downtime. Identify the most likely cause and improve diagnostic accuracy. Assess affected customers, notify them proactively and prevent escalation. Provide consistent and actionable remediation plans and improve resolution time.
    -   Service summary using Knowledge Graph: Boost agent productivity and customer satisfaction with context-aware insights. Deliver intelligent, connected summaries of incidents, changes, and impacted services. Make use of Knowledge Graph to help eliminate manual investigation and speed resolution. Tailor operational workflows using customizable skills with editable questions and summarization prompts.
    -   TM Forum API updates: Unify customer and partner profiles across systems, supporting better engagement, onboarding and personalization with TMF 632. Helps ensure consistent and synchronized product information across channels in compliance with TMF 620 standards. Increases service reliability and speeds up resolution with built in automated diagnostics compliant with TMF 653 standards.
    Telecom Service Operations Management \(TSOM\)

    -   Telecom discovery builder framework: Leverage builder framework to enable rapid, no-code development of new network discovery service graph connectors. Reduce discovery service graph connectors build costs with no code development and maintenance framework. Improve discovery data quality with out- of-the-box data validation tools.
    -   Nokia Altiplano Service Graph Connector enhancement: Provide a comprehensive view of physical and logical resources from multi-vendor PON networks. Combine network discovery from multiple network management system instances and view and filter from a single view. Provide flexibility to set a specific range or type of elements to discover. Built using the Telecom Discovery Builder framework, helping ensure consistent development and maintenance across all Service Graph Connectors.
    -   Discrepancy audit enhancement: Identify and resolve physical and logical discrepancies between live network inventory and CMDB inventory to help ensure alignment and boost productivity. Reduce discrepancy noise and complexity with advanced filtering, enabling engineers to simplify discrepancy resolution efficiently. Support holistic discrepancy identification spanning across topology, resource, attribute, and values for detailed discrepancy analysis and resolution.

-   **Government**

    Grants Management

    -   Merit review: Track and review applications securely in one place - no more scattered notes or emails. Ensure transparency and reduce bias by automatically capturing and aggregating scores across set criteria. Instantly reassign reviews with built-in workflows, eliminating manual steps.
    -   Funding proposal and Award Decision: Quickly define, review, and confirm funding proposals in one workspace, reducing delays and accelerating funding decision. Help ensure speed and consistency with ready-to-go templates for award or rejection notifications. Keep applicants informed with real-time visibility into proposal status and delivering award notifications instantly through the workspace.
-   **Retail and Hospitality**

    Retail Service Management and Retail Operations

    -   Retail mobile app: Increase store productivity by enabling on-the-go access to assignments, help requests, and more. Improve store team experience with retail specific views to focus on key actions. Reduce time to value with a configurable OOTB mobile experience.
    -   Retail case types: Improve operational efficiency by standardizing common workflows such as customer complaints, in-store operations, and HQ processes. Reduce time to value with four new foundational case types that can be tailored to individual retailer needs.

-   **Manufacturing**

    Manufacturing Commercial Operations for Manufacturing

    -   Recalls - Campaigns Management: Manage campaigns centrally with defined phases, tasks, corrective actions, and impacted assets - all in one place. Streamline the assignment of corrective actions and charges such as parts, labor, external and miscellaneous. Increase transparency to dealers by publishing recall campaigns directly to the dealer portal.
    -   Recalls - Claims Management: Reduce claims submission time and errors with step-by-step clear guidelines and pre-filled data \(e.g., dealer name, vehicle VIN\). Improve OEM assessor productivity through detailed job charges breakdowns and flexible adjudication options. Enhance transparency and collaboration via real-time claim tracking and in- context communication.
    -   Warranty Claims Management: Provide a simplified, intuitive experience for dealers to submit, update, and track warranty repair claims. Enable OEM assessors to resolve claims efficiently with adjudication options— approve, reject, partial, or send back. Strengthen collaboration between dealer administrators and OEM assessors to accelerate resolutions.
    -   Sales Promotions - Campaigns Management: Define tailored sales promotion campaigns across multiple products, regions, and dealers using eligibility and visibility criteria. Boost productivity with configurable intake settings \(i.e., promotion type, attributes\) and checklist templates. Improve visibility and effectiveness by publishing sales promotion campaigns directly to the dealer portal.
    -   Sales Promotions - Claims Management: Boost dealer productivity by enabling multi-sales campaign claims and bulk uploads. Improve data quality and completeness through required field validations during claims submission. Streamline OEM assessor review and adjudication workflows \(e.g., approve all, reject all, partially approve, send back\).
    -   Dealer Portal: Easily look up cases and campaigns containing specific products using their serial numbers. Provide full visibility and easy access to recall and sales promotion campaigns including key details like scope and dates. Enhance dealer experience by enabling submission and tracking of claims and cases in one place.

## Application Development

-   **App Engine**
    -   Developer sandbox: Improve quality assurance with isolated testing environments that catch issues early. Facilitate safe branching and merging with modern Git-based workflows. Reduce delivery delays that result from manual coordination
    -   ServiceNow Studio enhancements: View and access AI components within the ServiceNow Studio taxonomy. Build AI agent-powered apps starting from ServiceNow Studio. Support faster prototyping and tighter integration across the platform’s AI ecosystem.

## ServiceNow Impact and Expert Services

-   **Impact: Value and Adoption**
    -   Value reporting enhancements: Set business objectives and success metrics directly inside ServiceNow Impact. Monitor outcomes and performance with real-time reporting and visualizations in an enhanced dashboard. Measure value delivered by ServiceNow capabilities in a single view.
    -   Strategic Portfolio Management integration: Convert Impact insights into Strategic Portfolio Management work items. View the status of generated work items directly inside Impact—via automatic progress syncing from SPM. Streamline execution with enhanced conversion options, visual status indicators, and a consistent, modern user experience.
-   **Impact: Health &amp; observability**
    -   Instance Observer - Root-cause summary: Analyze logs, metrics, and alerts faster by reading clear, GenAI-powered summaries of incident causes. Reduce mean time to detect \(MTTD\) and mean time to resolve \(MTTR\) by helping application owners quickly understand issues. Provide contextual insights on demand, without manual data analysis.
    -   Instance Observer - Alert enhancements: Customers with Impact Guided now have access to the six most common alerts used in Instance Observer. Notify platform owners or admins when specific performance thresholds are crossed, so they can take action before issues becomes critical. Use version history to see when alerts were last modified, by whom, and what changed.
-   **Impact: Expertise &amp; guidance**
    -   New AI Accelerators: Jumpstart Your Now Assist in Document Intelligence. Jumpstart Your External Content Connectors.
-   **Impact: Premium support**
    -   Preventive Care add-on: Enhance stability and scalability with bi- annual expert-led engagements. Get deep health insights to identify scalability constraints and reduce performance degradation. Receive guided implementation recommendations and validate improvements.
-   **Expert Services**

    Expert Services: Solution Architecture Advisory Service. Core Business Suite Implementation.


## Upgrading to the Zurich release

Upgrade to the ServiceNow AI Platform Zurich release today. Take advantage of these ServiceNow resources to help you stay current.

-   **Get your Zurich release upgrade kit**

    Go to the [Release and Upgrades](https://www.servicenow.com/community/releases-and-upgrades/ct-p/releases-and-upgrades) forum on the Community. Find everything you need to get started on your upgrade, including a summary of new features, demos, key resources, and more.

-   **ServiceNow Releases and Upgrades community**

    Ask questions and get answers from ServiceNow experts and peers, get access to the latest best practices and resources, and register for releases and upgrades community events for additional support.



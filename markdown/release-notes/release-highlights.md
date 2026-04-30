---
title: Yokohama General Availability release highlights
description: High-level overview of products and features in the ServiceNow AI Platform Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 29
breadcrumb: [Yokohama release notes]
---

# Yokohama General Availability release highlights

High-level overview of products and features in the ServiceNow AI Platform Yokohama release.

## Overview of the Yokohama General Availability \(GA\) release

## ServiceNow AI Platform

-   **ServiceNow AI Agents**
    -   ServiceNow AI Agent Studio: Design custom AI agents using natural language prompts. Allow multiple agents to work together and share data with chaining for smarter automation. Execute dynamic workflows and interact with and monitor agents in real time.
    -   Conversational subflows and actions: Create conversational subflows and actions in Workflow Studio to be deployed in Virtual Agent. Automatically generate flow inputs and outputs within conversational responses through Now LLM.
    -   Voice input for Now Assist: Use simple voice commands to unlock summarization skills with Now Assist. Improve accessibility and usability for people with disabilities. Help ensure more efficient and productive experiences for all users.
-   **Data**
    -   Workflow Data Fabric: Connect structured, unstructured, or streaming data to continuously monitor and improve operations.
    -   External Content Connectors for search: Index and search unstructured and document data across multiple enterprise sources. Extend AI Search to content and metadata repositories such as Confluence Cloud and SharePoint. The range of connectors will continually expand to bring in additional content sources such as Google Drive, Teams, Slack, Salesforce, Workday, and more.
    -   CSDM version 5: Extend unified data models from internal technology workflows to external products and services. Design responsible and compliant AI into technology workflows.
    -   User Experience Analytics: Visualize metrics and interactions through a comprehensive dashboard. Monitor and optimize operational key performance indicators \(KPIs\) to improve user experience and drive adoption.
    -   Data snapshots in Performance Analytics: Improve data analysis with multi-level breakdowns to group and filter indicator sources. Automate data collection to streamline workflows and reduce manual management.
-   **Accessibility**
    -   Text Adjust: Allow users to replace fonts and configure text spacing on ServiceNow or any web page. Enhance user experience with personalized solutions that improve visual and cognitive accessibility. Address WCAG 1.4.12 requirements.
-   **Platform Security**
    -   Data Privacy enhancements
        -   Data Privacy: Discover sensitive data using AI/ML. Find sensitive data that doesn’t conform to traditional rule-based patterns, such as names, street addresses, IP addresses, etc. Scheduled jobs can scan common attachment formats, PDF, DOC\(X\) and TXT and notify admins when sensitive data is discovered. Expanded discovery and anonymization capabilities to include data in journal fields for classic UI applications.
        -   Field Encryption Enterprise: Bring and manage your own key to comply with internal and regulatory requirements. Leverage Access Observer to discover which resources are accessing which field to inform encryption policies. Protect sensitive data without impacting workflow functionality or user experience.
    -   Authentication enhancements
        -   Zero Trust Access: 'Continuous authentication' enables customers to require a high assurance session before allowing access to sensitive data. The continuous authentication policy uses data classification or table designations as the criteria to require high assurance of a user’s identity before granting access to data.
        -   MFA enforced by default: MFA is required for all internal users\* as part of our commitment to strengthening instance security and helping to prevent unauthorized access. All internal users\* will self-enroll in MFA within a 30 - day period starting with the upgrade to Yokohama. Administrators will have the ability to modify the MFA policy to extend the enrollment window or exempt specific users, roles, or groups from the MFA requirement, if necessary.

            \*Single-sign-on and integration accounts are not affected.

    -   Authorization enhancements
        -   Security data filters: Replace the need for query business rules as a security control, alleviating complexity and reducing performance issues.
        -   Related records: Restrict or grant access to projects and their related or child entities, without relying on complex access controls.
        -   Access Analyzer: Reduce user access troubleshooting time by granting the new AA\_Admin role to authorized non-admin users.
    -   Log Export Service enhancements
        -   Planning storage requirements is simplified with Log Export Service \(LES\) reports which provides visibility into log consumption.
        -   Sending granular log contents to multiple sources is now supported with LES Kafka topics.
        -   The addition of topics allows for subscribing to multiple different subsets of tables in sys audit as well as enabling tailoring of retention policies in customer infrastructure.
    -   Domain Separation enhancements
        -   Existing instances can use Domain Separation guided setup to install Domain Separation.
        -   Automates common tasks such as Domain creation, index creation and delta data check.
        -   Creates a job summary report that highlights additional configurations needed prior to using Domain Separation.

## Workflow Data Fabric

-   **Now Assist updates**
    -   Rapidly create custom spokes and RPA bots using natural language.
    -   Execute spoke actions in third-party systems directly with Now Assist.
-   **Automation Center**
    -   Connection Manager: Manage integrations, pagination, and data mapping with guided instructions. Centralize third-party automation tools to manage integrations, ETL, processes, and lifecycle optimization.
    -   Evaluation projects: Discover out-of-the box evaluation projects on every Yokohama instance. Make HRSD &amp; CSM service managers aware of their ability to create process mining projects for case management. Utilize Process Mining insights to understand and optimize case management processes.
-   **Process Mining**
    -   Work notes analysis: Distill work notes on inefficient process transitions into actionable insights. Accelerate time to process improvements by understanding the detailed, documented reasons for bottlenecks.
    -   Process configuration Guided Setup: Enables SMEs \(process analysts\) to streamline and scale the creation of process configuration records. Increase business stakeholder adoption through pre-built process configurations from SMEs that makes it easier to set up a Process Mining project. Close the gap for tables where process configuration records aren’t available via BU content packs and custom tables.
-   **Integration Hub**
    -   External content connectors: Enable secure access to enterprise data with GenAI-powered search from a single-entry point. Integrate third-party content sources like SharePoint and Confluence natively into AI Search.

## Technology Workflows

-   **Service Operations**
    -   Digital End-User Experience enhancements
        -   DEX score: Combine application and device health, user sentiment, and service experience metrics for full digital experience visibility.
        -   Push notifications: Deliver pop-up alerts and status insight notifications to help employees be more informed and successful with self-service.
        -   Network experience: Analyze network /application issues to identify bottlenecks and proactively address potential issues.
-   **IT Service Management**
    -   AI Agents: Quickly deploy AI agents with out-of- the-box use cases for change, major incident, and incident processes. Utilize preset or custom guard rails to protect your data.
    -   Now Assist for IT Service Management enhancements: Revamped conversational chatbot and risk analysis to reduce incidents. Automated surfacing of relevant knowledge and catalog items as employees submit requests.
    -   Additional ITSM enhancements:
        -   DevOps: Enable DevOps teams to easily build custom orchestration integrations with intuitive tooling.
        -   Digital Product Release: Create release plans for complex, multi-product initiatives via guided setup experiences.
        -   Success Dashboard: Extend measurement of your implementation to AI Agents predefined success metrics.
        -   Service Operations Workspace: Automatically surface relevant user information via DEX when a major incident occurs directly to response teams.
-   **IT Operations Management**
    -   Service Observability: Centralize critical signals and bridge workflows to increase agility and reliability. Calculate blast radius and reduce mean time to resolution \(MTTR\) by overlaying changes to your application to underlying infrastructure. Define and track service goals that align to your business objectives.
    -   Synthetic monitoring: Trigger alerts when public or private endpoints become unavailable using remote monitors. Monitor availability and response time for critical HTTP and API endpoints. Reduce MTTI/MTTR by providing operators with relevant outage context quickly, including affected services.
    -   Alert correlation using network traffic: Address alerts and issues before they become incidents or outages. Reduce alert noise and streamline response by exploiting the hidden logic in network traffic. Group and manage relevant alerts even without a fully mature CMDB.
-   **Configuration Management Database \(CMDB\)**
    -   API Insights: Drive regulatory compliance by assessing APIs. Identify unauthorized endpoints or outdated protocols. Centralize API visibility from cloud and internal tools, including dependencies, optimizing configurations, and streamlining governance. Weave APIs into core IT workflow including change management, knowledge bases, and service operations.
    -   API Service Graph Connectors: Instantly establish API visibility using popular API management tools. Automatically ingest and refresh trusted data with connectors certified to work. Enable compliance to regulation and security initiatives with full API detail that also works with your established change and incident process.
    -   CSDM version 5: Extend unified data models from internal technology workflows to external products and services. Harmonize IT solutions on a single system of record and action for human and AI agents. Design responsible and compliant AI into every technology workflow.
-   **Software Asset Management**
    -   Now Assist for Software Asset Management
        -   Gather publisher insights on software estate across software inventory, configuration health, and license compliance. Simplify software publisher outcomes and opportunities based on complex licensing rules. Understand compliance requirements and determine necessary actions to remediate risk and optimize spend.
    -   Software Asset Management guided setup: Guide users through success goal creation to reconciliation with their chosen product setup. Improve user experience with easy-to-follow steps to set up a new product.
    -   SAP S/4HANA Cloud support – public: Use the Integration Hub spoke to connect to SAP S/4HANA Cloud public edition. Populate data in the user subscription table to capture user information and applied roles for the user. Track the number of licenses used with the reconciliation process that leverages the FUE conversion model.
-   **Hardware Asset Management**
    -   Asset attestation: Create, assign, and monitor the completion of asset attestations to reduce gaps in asset data. Validate serialized asset usage for hardware not contained in corporate offices. Minimize security and compliance risks by verifying asset chain of custody.
-   **Strategic Portfolio Management**
    -   Now Assist for Strategic Portfolio Management
        -   Project Task Monitoring: Autonomous monitoring and optimizing project operations. Real-time visibility into project health. Autonomous monitoring and optimizing project operation.
        -   Story Generation: Generate detailed, high-quality stories from epics with AI Agents.
    -   Portfolio financials
        -   Review cost rollups across approved, forecasted, and actuals. Analyze breakdowns by categories, cost types, or timeframes. Ensure alignment with budget to help prevent overspending.
-   **Enterprise Architecture \(formerly Application Portfolio Management\)**
    -   Now Assist for Enterprise Architecture
        -   Architecture decision record summarization: Simplify details into concise summaries for faster decisions and improved efficiency.
        -   Conversational Catalog requests: Create application, integration, and architecture review requests via a conversational interface.
        -   Enterprise Architecture Diagrammer: Generate models and summaries of models from simple text prompts.
-   **Operational Technology Asset Management**
    -   Unified OT workspace for industrial and hardware assets: Manage OT, OE, and hardware assets using a single, integrated interface. Streamline asset lifecycle workflows with a unified set of tasks to reduce downtime risks and improve asset tracking.
    -   Firmware management: Ingest data from third-party discovery tools, identify devices, and parse firmware models. Normalize data based on curated content library of firmware versions to provide actionable profiles. Enable ServiceNow OT security tools to manage vulnerabilities and operational disruptions.
    -   Firmware content library and normalization: Produce a normalized set of discovered firmware based on a content library curated by ServiceNow. Normalized firmware results in standardization of firmware publishers, version numbers, release dates and UNSPSC codes. Normalized firmware content is enriched with Common Platform Enumeration \(CPE\) vulnerability data per the National Institute of Standards and Technology group firmware.
-   **Risk and Resilience**
    -   Business Continuity Management \(BCM\)
        -   Smart Assessments for BIA templates: Leverage Smart Assessments capabilities, copy templates, prefill answers, scoring functions, filtering, etc. within BIA templates. Configure logic to calculate the RTO, RPO, Recovery Tier, CIA values based on the BIA responses. Enhanced user experience for building BIAs to address varied continuity requirements.
        -   Task management in exercises and crisis events: Identify duplicate tasks across exercises and crisis event to remove redundancy. Contextualize dependencies across plans to understand potential impact to RTO, RPO. Visualize the execution order of the tasks via a Gantt chart.
    -   Environmental, Social, and Governance Management \(ESGM\)
        -   Forecast planning and analysis: Create multiple what-if scenarios to model a future path. Assess potential changes and plan interventions by adjusting specific variables. Forecast data for metrics with predefined models.
        -   Formula tree: Gain a better understanding of complex calculations with an intuitive representation of the formula’s structure. View values in addition to calculations in the hierarchical formula tree. Identify errors or inconsistencies by breaking formulas down into their individual components.
    -   Integrated Risk Management \(IRM\)
        -   Now Assist for Integrated Risk Management: Leverage the Summarize button on the Issue Overview page to generate a summary of the entire issue including actions taken and resolution. Provide feedback on the issue, copy the summary, or post the summary into work notes.
        -   Smart Assessment Engine for compliance case analysis: Seamlessly integrate risk assessment into compliance case management on the app. Generate more meaningful assessment scores based on responses and data types. Automatically prefill responses.
        -   Digital Operational Resilience incident reporting, data model and service mapping visualization: Leverage a new workflow to meet regulatory reporting requirements for both IT and security incidents. Auto trigger compliance cases, notifications and assessments with relevant CMDB ties to drive informed remediation actions. Autogenerate initial, intermediate and final reports for DORA and classify major incidents appropriately.
    -   Privacy Management
        -   New privacy assessment experience: Information object categories help to streamline data governance, improve clarity for business users, and enhance accuracy. Automatically calculate and continuously monitor processing activity risk scores with new criticality factors.
    -   Third-party Risk Management \(TPRM\)
        -   Pre-populated questionnaires, Excel template: Pre-populated questionnaire responses for entities and engagements associated with the same active third-party. Leverage Microsoft Excel template for questionnaires – downloaded, completed, and imported in the vendor portal.
        -   Dashboards for third-party insights, custom analytics: Personalize the dashboard with a preferred layout to quickly gain insights. Explore assessment data at various levels to prioritize and analyze key metrics. Customize report layouts, widgets, and data views and workflows for oversight of entire TPRM program.
-   **Security Operations**
    -   Now Assist for Security Operations
        -   Security incident wrap-up generator: Automate workflows for analysts to close security incidents. Auto-generate close codes, resolution notes, and post incident analysis. Enable analysts to use natural language to ask follow-up questions and update content.
        -   Correlation insights: Provide analysts quick views or records correlated to the security incident based on asset, user, or observable.

## Core Business Services

-   **HR Service Delivery**
    -   Now Assist for HR Service Delivery
        -   Journey generation: Accelerate journey creation through intuitive, natural language design tools. Increase manager productivity with streamlined and personalized employee development creation paths. Enhance user experience by simplifying complex journey mapping processes.
        -   Growth plan generation: Enable employees to input details about their goals and growth outcomes in a simple text format. Generate draft growth plans with personalized activities, learning courses, and skill validation programs.
    -   HR appointment setting experience for deskless workers: Allow deskless workers to schedule in-person or virtual HR meetings via the employee service portal.
-   **Health and Safety**
    -   Exposure management: Identify exposures and link associated risk assessments and safety records. Conduct exposure assessments using a condition builder for precise tracking. Assign follow-up actions to help ensure worker safety and proper exposure management.
    -   Permit to Work: Request out-of-the-box permit types and add associated work orders, inspections, or safety records. Configure required checklist and approval flow to fit unique needs. Manage requested permits and directly cancel, suspend, or reopen permits within the Health and Safety Workspace.
-   **Workplace Service Delivery**
    -   Now Assist for Workplace Service Delivery
        -   Workplace Concierge: Speed up reservations, service requests, and guest management through a conversational AI. Access intelligent workplace assistance anywhere, on any device. Enable employees to add external visitors to a reservation during the reservation process.
    -   Kiosk Indoor Mapping experience: Employees and visitors can raise cases directly from kiosks throughout the workplace. Intuitive UI to search and navigate spaces, view space details, booking options, and occupancy data. Configure map display and activate map features like reservations and data displays.
    -   Map Printing: Configure and generate printable map formats with customizable options. Customize printing configurations including zoom, font size, collation, legend, numbering, location pin, etc. Print maps directly from the location directory and Workplace Central.
-   **Source to Pay Operations**
    -   Now Assist for Source to Pay Operations
        -   Decrease cases handled by support channels through self-service options. Minimize wait times for simple queries like payment inquiry status.

## CRM

-   **Customer Service Management**
    -   Now Assist for CSM
        -   Now Assist in portal case form: Provide answers directly in the case form instead of a list of articles.
        -   Virtual Agent topic scheduling assistant: Easily schedule, re-schedule, and cancel appointments.
    -   Voice interaction page and call controls: Manage call transfers, conferences, hold, and mute via third party CCaaS call controls. Create consistency in agent experience across all channels through universal inbox. Streamline efficiency with direct workspace access to consult and blind call transfer controls.
    -   Embedded CCaaS components: Merge AI and automation tools from CCaaS and ServiceNow into Agent Workspace. Empower agents with natively embedded Genesys tools.
    -   Unified routing on 3rd party CCaaS: Consolidate ServiceNow chat and case routing policies on third party CCaaS. Drive intelligent routing orchestration by centralizing routing for all channels into one system. Enhance agent experiences by enabling call acceptance directly from the agent. Inbox Lower administrative overhead by unifying routing policies, skills, and queue management into one system.
    -   Unified CCaaS Workforce Engagement Management: Embed Genesys WEM and key insights from ServiceNow in one place. Drive accurate forecasting, scheduling and optimize agent performance through bi-directional data syncs.
    -   Email as an interaction: Transform emails into interactions rather than automatically creating a case, reducing unnecessary cases. Promote clear distinction between interactions for initial receipt and cases for investigation and resolution of customer queries. Categorize and populate case intake through AI-generated recommendations.
-   **Sales and Order Management**
    -   Self-service order placement: Provide an omnichannel ordering experience via the self-service portal.
    -   Configure, Price, and Quote enhancements: Provide product recommendations during quote creation. Apply volume-based pricing to drive higher sales while also improving efficiency. Generate quote PDFs outlining product and pricing details. Display parent and child product offerings on quote lines in a hierarchical view.
    -   Case management for invoice operations: Capture and track invoice exceptions and disputes data to help ensure timely payments and improve cash flow.
-   **Field Service Management**
    -   Smart Assessment for Field Service Questionnaire: Streamline information capture with visualized instructional guidance. Generate questions based on conditional dependencies. Improved user experience with grouped inputs and the ability to add comments or upload attachments.
    -   Capacity console: Analyze and measure allocated versus used capacity across one or more territories to inform resourcing decisions. Identify and assign work to available resources based on configurable booking thresholds. Improve demand forecasting accuracy using selected date ranges and territories.
    -   Dispatcher enhanced territory filter: Navigate and multi-select territory hierarchies. Filter based on territory hierarchies, identifying resources at various levels of granularity.
    -   Advanced task dependencies: Define dependencies in the work order task template. Complete work sequentially to help ensure prerequisites are met by configuring task relationships. Proactively alert dispatchers when tasks are completed ahead of schedule or delayed.
    -   Appointment booking slot recommendations: Allow customers and agents to select from recommended time slots. Schedule technician visits based on the nature of the work and significance of the customer relationship. Suggest appointment slots that account for agent availability and capacity.

## Industry Solutions

-   **Financial Services Operations for Banking**
    -   Now Assist for Financial Services Operations
        -   Report a dispute: Manage rising dispute cases and inquiries with AI-powered case intake. Autonomously collect all relevant details from the cardholder and seamlessly hand-off cases to human agents. AI is grounded in pre-defined case intake requirements with a conversation audit trail stored on the case.
    -   Dispute Playbook enhancements
        -   Chargeback Flow: Automate chargebacks amongst dispute case stakeholders. Shorten resolution time by automatically triggering required actions to process a dispute case. Aggregate communication between merchants and acquiring banks into a single interface. Reduce development time with preconfigured chargeback flows for fraud and consumer disputes. Adhere to tight SLA time-frames by allowing individual transactions to progress independently.
        -   Full Visa Resolve Online \(VROL\) integration: Communicate directly with Visa Resolve Online \(VROL\) across the entire dispute process. Embed Visa callouts across resolution steps. Reduce manual errors by dynamically exchanging information between ServiceNow and VROL. Help prevent unnecessary disputes by identifying associated transactions, such as overlooked refunds.
    -   Ethoca Alerts integration: Strengthen customer satisfaction by stopping fraudulent transactions before merchants fulfill orders. Minimize dispute processing expenses and chargebacks by stopping orders prior to fulfillment.
    -   Updated rules content pack for Visa: Automatically maintain Visa rules updates with built-in, bi-annual rules maintenance. Easily re-deploy updated rules across your dispute processes for faster resolution experiences.
-   **Financial Services Operations for Insurance**
    -   Now Assist for Financial Services Operations
        -   Virtual Agent scheduling assistant: Schedule, re-schedule, and cancel appointments. Reduce case count with increased booking handled through Virtual Agent. Improve customer satisfaction with an easy-to-use, conversational experience.
    -   Insurance Claims: Manage complex claims via multi-adjuster support and persona-specific workspaces for improved productivity and customer satisfaction. Tailor claims processes to fit unique business needs and effortlessly deploy end-to-end claims workflows with intuitive configuration. Incorporate additional lines of business with ease through configurable framework and data model.
    -   Service Bridge for Financial Services Operations: Eliminate navigating multiple systems by sending and receiving requests within ServiceNow. Improve resolution times by receiving structured requests in a single system of action. Reduce the cost to serve with direct, actionable communication between relevant parties.
    -   Voice interaction page and call controls: Create consistency in agent experience across all channels through universal inbox. Expedite resolution times by eliminating back-and-forth between CCaaS CTI. Boost efficiency with direct workspace access to consult and blind call transfer controls.
    -   Embedded Contact Center as a Service \(CCaaS\) components: Merge AI and automation tools from CCaaS and ServiceNow into Agent Workspace. Natively embedded Genesys tools help to serve customers faster.
    -   Unified Routing on 3rd party CCaaS: Centralize routing for all channels into one system. Enable call acceptance directly from the Agent Inbox. Unify routing policies, skills and queue management into one system.
    -   Unified CCaaS Workforce Engagement Management \(WEM\): Embed Genesys WEM and key insights from ServiceNow in one place. Drive accurate forecasting, scheduling and optimize agent performance through bi-directional data syncs. Optimize staffing and scheduling decisions and reduce administrative effort.
    -   Email as an interaction: Transform emails into interactions rather than automatically creating a case, reducing unnecessary cases. Promote clear distinction between interactions for initial receipt and cases for investigation and resolution of customer queries. Categorize and populate case intake through AI-generated recommendations.
-   **Manufacturing Commercial Operations**
    -   Now Assist for Manufacturing Commercial Operations
        -   Intelligent answers in portal case form: Provide answers directly in the case form instead of a list of articles.
        -   Virtual Agent scheduling assistant: Schedule, re-schedule, and cancel appointments. Reduce case count with increased booking handled through Virtual Agent. Improve customer satisfaction with an easy-to-use, conversational experience.
    -   Order Management
        -   Self-Service Order Placement: Enable customers to configure products and place orders via self-service portal. Streamline order placement and fulfillment processes and increase conversion rates by making it simpler for customers to complete orders.
        -   Case Management for Invoice Operations: Create cases for multiple invoices or for specific invoice lines. Increase operational efficiency by avoiding bottlenecks and disruptions in invoice processing workflow.
    -   Quote PDF Generation in Quote Management: Generate quote PDFs outlining product and pricing details for customer review.
    -   Email Interactions: Transform emails into interactions rather than cases to avoid creating unnecessary case creations. Promote clear distinction between interactions for initial receipt and intake and cases for the investigation and resolution of customer queries. Categorize and populate case intake through AI-generated recommendations.
    -   Service Bridge - Copy from Service Catalog to Remote Catalog Item: Enables the copy of standard portal catalog items to the Service Bridge Remote Catalog, eliminating the need to manually recreate Service Catalog items in the Service Bridge Remote Catalog.
    -   Embedded CCaaS components: Merge AI and automation tools from CCaaS and ServiceNow into Agent Workspace. Utilize natively embedded Genesys tools.
    -   Unified routing on 3rd party CCaaS: Centralize routing for all channels into one system. Enable call acceptance directly from the Agent Inbox. Unify routing policies, skills and queue management into one system.
    -   Unified CCaaS workforce engagement management: Embed Genesys WEM and key insights from ServiceNow in one place to optimize staffing and scheduling decisions and reduce administrative effort. Drive accurate forecasting, scheduling and optimize agent performance through bi-directional data syncs.
-   **Technology**
    -   Now Assist for Technology, Media and Telecommunications \(TMT\)
        -   ALE - Case summarization for Customer Success: Use Gen AI to summarize records for customer success engagement and get a clear summary of key details. Quickly catch up on onboardings with AI-generated case summaries. Maintain constant communication with customers using AI-generated summaries for key touchpoints.
        -   Transform Mapping Assist: Auto-generate field transformations for fields mapped between instances, identifying matches to reduce time consuming and error prone manual entry. Leverage automation to boost productivity of Service Bridge administrators and reduce integration errors.
    -   Technology Provider Service Management
        -   ALE - Health and Risk Frameworks: Define, manage, and track key indicators to establish an overall health score for customer engagement. Define, create, and manage relational risks and take action to remediate. Get clear insights into risk signals and create repeatable plans to address them.
        -   ALE - Success Blueprint Builder and Initiative Roadmap: Customize and automate templates for success blueprints, objectives, and outcomes. Organize objectives, outcomes and initiatives with a timeline view to see the status, timing, and priority of all success initiatives.
        -   Test Diagnostics for Technology Product Support Case Type: Resolve issues with complex diagnostic tests that are configured and embedded directly into your workspace. Organize and run diagnostics directly in the platform to pinpoint root causes. Enable everyday support agents to diagnose issues independently.
-   **Telecommunications**
    -   Now Assist for Technology, Media and Telecommunications \(TMT\)
        -   Service Bridge mapping: Auto-generate field transformations for fields mapped between instances, identifying matches to reduce time consuming and error prone manual entry. Leverage automation to boost productivity of Service Bridge administrators and reduce integration errors.
        -   Test summarization extension for Customer Service Problem Management: Generate concise explanations and contextual notes, making test results easier to understand for quicker insights and more informed decision-making. Prioritize high priority issues with enriched summaries. Provide clear and contextual test summaries to align stakeholders, driving effective discussions and data-driven decisions.
        -   Case summarization for Customer Success: Accelerate onboarding and customer success engagement status with a clear summary of key details.
    -   Telecom Service Management \(TSM\)
        -   Health and Risk Frameworks for Customer Success: Define, manage, and track key indicators to establish an overall health score for customer engagement. Clarify, create, and manage relational risks and take action to remediate. Get clear insights into risk signals and create repeatable plans to address them.
        -   Remote Catalog Client Transcript for Service Bridge: Help ensure quality and accuracy with scripts reviewed and approved by the consumer administrator before activation.
    -   Telecom Service Operations Management \(TSOM\)
        -   Patterns-based network discovery: Discover physical network inventory directly from network elements using both SNMP and CLI interfaces. Keep inventory data up-to-date and synchronized with live network resource data, and maintain an accurate, complete CMDB with automated network discovery.
        -   Telecom Discovery Service Graph Connector: Standardize Nokia Atliplano vendor equipment integration with out-of-the-box multi-vendor PON network discovery. Discover a complete physical network inventory with detailed resource information by connecting to vendor management systems via REST APIs.
        -   Telecom Reconciliation: Identify and resolve discrepancies between live network inventory and CMDB inventory to help ensure alignment and boost productivity. Auto-generate discrepancy reports detailing the type of discrepancy. Provide engineers with recommended corrective actions and the flexibility and control to choose between manual or automated methods to resolve discrepancies. Improve operations by automatically aligning the operational status of network resources.
    -   Strategic Portfolio Management for Telecommunications \(SPMT\)
        -   Private 5G construction template: Provide pre-defined workflows for site assessment, equipment procurement and installations. Track milestones for spectrum licensing and regulatory approvals in real time. Integrate risk management module helping to ensure regulatory compliance. Allocate resources for multi-site deployments leading to reduced costs.
        -   Fiber broadband rollout template: Manage dependencies with workflow automation and tracker for permits and approvals. Offer centralized view of deployment progress to maximize coverage and minimize costs. Provide onboarding dashboards for customer-ready services, enhancing customer acquisition.
    -   Telecommunications Network Inventory \(TNI\)
        -   Design &amp; Assign Playbook Experience: Improve customer experience with faster network designs and fewer errors. Visualize a step-by-step canvas view of the design and assign process. Leverage an end-to-end playbook for comprehensive understanding of activities and actions. Leverage framework capability, build custom Design &amp; Assign playbooks to align with your unique products, services, and business processes.
        -   Network Site User Interface: See capacity threshold violations on a map and remove the need to sift through excessive data. Accelerate network issue resolution with color-coded operational statuses for sites, circuits, and topologies. Enhance CSAT and meet SLAs by quickly identifying and addressing network events.
        -   Enhanced Change Management - Multimodal: Leverage out-of-the-box change management status naming for a clear understanding of workflow stages. Reduce the time to plan, build, modify, and maintain network activities by configuring the platform to align with your business processes. Reduce design errors and fallout by aligning customer status with network status activities.
-   **Public Sector Digital Services**
    -   Now Assist for Public Sector Digital Services
        -   Chat summarization: Deliver faster services by allowing agents to quickly understand the context of newly-assigned cases. Boost customer experiences and reduce the need to repeat information already provided to virtual agent. Improve operations by collecting consistent case resolution data.
-   **Healthcare and Life Sciences Service Management**
    -   Healthcare Operations Core: Enable care teams to request support directly from EMR systems, connect with service departments, and track requests with full visibility. Configure healthcare organizations, manage hierarchies, and control access for care teams. Standardize and customize cases for support service departments, enabling care teams to efficiently report biomedical, IT, and general hospital operations issues.
    -   Care Team Portal: Enable full visibility into all support cases requested by care teams, including from other team members. Add or remove care team members dynamically to maintain up-to-date collaboration. Capture relevant Epic or other EMR parameters on cases, enriching data for IT and support teams.
    -   Care Team Operations for Healthcare IT: Standardize IT case management, enabling care teams to request support for EMR and IT-related needs. Facilitate IT support requests through the Care Team Portal with preconfigured, intuitive workflows. Synchronize healthcare IT cases with incidents, giving care teams visibility into reported IT issues while enabling IT teams to resolve them efficiently.
    -   Care Team Operations for Biomed: Streamline biomed case management, extending healthcare operations to address corrective maintenance needs. Enable direct biomed support requests through the Care Team Portal, using preconfigured record producers. Synchronize biomed cases and work orders, providing visibility into reported issues while allowing biomed teams to resolve them efficiently—without duplicative updates.
-   **Retail Service Management and Retail Operations**
    -   Retail multistore case generator: Minimize configuration needed for OOTB multi-location retail case assignment. Create child cases for multiple stores at once. Improve site productivity by assigning cases directly to managers and tracking completion at each location.
    -   Retail portal: Increase store productivity with centralized retail cases, catalog items, and quick links with a streamlined interface designed for store teams. Improve store team experience and highlight key metrics like case count and escalations based on store persona. Display retail-specific content OOTB, allowing teams to focus on tailoring the portal for their unique needs.

## Application Development

-   **App Engine**
    -   AI Agents for runtime workflows: Apply the same AI enhancements to custom applications as those offered in ServiceNow workflow solutions. Enhance user experiences and expand self-service through AI-powered runtime features. Create and deploy AI agents with custom applications.
    -   ServiceNow Studio: Build and scale automations faster with a unified development experience across all ServiceNow builders. Manage all metadata in one place with cross-scope editing. Track work, deploy safely, and maintain instance integrity with developer-friendly update set management.
    -   App Engine Management Center enhancements: Quickly assess whether an app meets production criteria with readiness score. Accelerate deployment of critical apps by using development best practices to determine automatic approvals. Gain confidence that deployed apps match company defined best practices.
    -   Creator Studio enhancements: Set parameters on forms to auto- populate fields based on selected values of another field. Make forms more useful for requesters by populating values on their behalf.
    -   Now Assist for Creator
        -   App summarization: Add AI generated app summaries to app descriptions in ServiceNow Studio. Enable admins to easily identify the purpose of applications during deployment and detect duplicate applications. Provide developers and admins deeper visibility into apps being deployed, what they do, and how they will function.
        -   Form generation: Use natural language to describe and create request forms in Creator Studio. Empower low-code developers with AI Agents embedded in Creator Studio.
        -   Table summarization: Provide admins with a summary of a table included in an app being deployed. Write a text summary of the purpose of the table.
        -   RPA bot generation: Generate bot workflows from instructions and process descriptions. Support the learning curve of RPA Desktop Design Studio by lowering the development barrier.
        -   Test generation: Increase automated test coverage by reducing the effort of creating and maintaining test cases. Generate ATF tests and test cases from text, Excel upload or story records. Reduce the barrier of adoption for Automated Test Framework.
        -   Now Assist in Process Mining: Identify root cause of inefficient process transitions and suggest remediations. Analyze work notes related to inefficient transitions and provide the most relevant reasons. Help process owners better understand stage transitions in their workflows.
-   **App Engine for Enterprise Resource Planning**
    -   OData query capabilities: Transform ERP data with advanced OData queries and customer fields in Model Manager. Order data by one or more fields in the 'Use ERP Data' flow action. Maintain the input, output field names per the business requirement.

## ServiceNow Impact

-   **Impact Store Application**
    -   Impact Store Application: Access Impact capabilities directly where you work using the new Impact store application. Take action on Impact insights and recommendations faster. Get a walk-through of the new experience and features in a guided tour.
-   **Value &amp; Adoption**
    -   Strategic Portfolio Management integration: Automatically transfer Impact recommendations and insights into Strategic Portfolio Management. Assign work items to the appropriate portfolio and track execution status. Improve accountability and help ensure recommendations are correctly actioned.
-   **Health &amp; Observability**
    -   Proactive code check: Reduce future tech debt by aligning new code to best practices. Scan code in sub-production environments to identify issues. Link directly to the issues to fix them before deploying to production.
    -   Instance Observer enhancements: Automate correlation analysis to identify root causes, reducing the need for manual data sifting. Improve efficiency in addressing issues by quickly pinpointing underlying problems through correlated metrics and logs.
-   **Expertise &amp; Training**
    -   Implement and adopt Now Assist quickly with these new Now Assist accelerators:
        -   Jumpstart Your Now Assist Skill Kit
        -   Jumpstart Your Now Assist for Customer Service Management
        -   Jumpstart Your Now Assist for Virtual Agent
-   **Expertise &amp; Guidance**
    -   Implement and adopt ServiceNow products quickly with these new accelerators:

        -   Jumpstart Your Employee Management
        -   Jumpstart Your Knowledge Management
        -   Jumpstart Your Resource Management
        -   Jumpstart Your Legacy Workflow Migration
        -   UX Fundamentals\*
        \*UX Fundamentals is only available for Advanced &amp; Total plans.

    -   Configuration Assist add-on: Get hands-on help from experts to deploy unused capabilities and act on Impact accelerator and platform health findings. Align a Technical Consultant or Business Process Consultant to a targeted product area. Choose the engagement length and coverage that best fits your needs.

## Upgrading to the Yokohama release

Upgrade to the ServiceNow AI Platform Yokohama release today. Take advantage of these ServiceNow resources to help you stay current.

-   **Get your Yokohama release upgrade kit**

    Go to the [Release and Upgrades](https://www.servicenow.com/community/releases-and-upgrades/ct-p/releases-and-upgrades) forum on the Community. Find everything you need to get started on your upgrade, including a summary of new features, demos, key resources, and more.

-   **ServiceNow Releases and Upgrades community**

    Ask questions and get answers from ServiceNow experts and peers, get access to the latest best practices and resources, and register for releases and upgrades community events for additional support.



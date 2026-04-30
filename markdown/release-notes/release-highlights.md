---
title: Xanadu General Availability release highlights
description: High-level overview of products and features in the ServiceNow AI Platform Xanadu General Availability \(GA\) release.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-09-24"
reading_time_minutes: 30
breadcrumb: [Xanadu release notes]
---

# Xanadu General Availability release highlights

High-level overview of products and features in the ServiceNow AI Platform Xanadu General Availability \(GA\) release.

## Overview of the Xanadu General Availability \(GA\) release

## ServiceNow AI Platform

-   **Now Assist**
    -   Data visualization generation: Enable users of any skill level to easily create analytics visualizations. Provides dynamically updated analytics for better decision-making and continuous data exploration.
    -   Chat and email reply generation: Auto-generate context-aware reply suggestions to help agents respond faster. Responses can be easily refined as needed.
    -   Custom skills development: Create GenAI skills with custom prompts, connecting to platform data for better accuracy. Users can choose models and deployment options.
    -   Microsoft Copilot integration: Combine two generative AI assistants into one experience, providing personalized solutions within the platform.
    -   Slack integration: Allow users to get answers and take actions directly from Slack, offering personalized, self-service solutions.
-   **Core Technology**

    -   RaptorDB: Improves transaction times by up to 53%1, runs reports, analytics, and list views up to 27 times2 faster, and unlocks up to a 3 times2 increase in transactional throughput so you can support more users and more workflows on your ServiceNow instance.
    -   Integrated Development Environment \(IDE\): Empower Visual Studio developers to build scoped applications with source code directly on the platform. Compile, execute code, and integrate seamlessly with familiar Git providers.
    1RaptorDB Professional vs MariaDB for a Global Hotel &amp; Resort Company

    2ServiceNow Benchmark on RaptorDB Professional vs MariaDB

-   **Platform Security**
    -   Data Privacy: Identify sensitive information in journal fields within modern UI applications. Use enhanced real-time discovery to apply existing rules for data anonymization and processing of inbound emails. Focus on specific fields containing Personally Identifiable Information \(PII\) instead of scanning entire tables.
    -   Access Controls: Establish detailed access controls on the platform using a combination of 'allow' and 'deny unless' Access Control lists. Implement new decision types that deny access to resources unless all specified conditions are met.
    -   Access Analyzer: Preview how changes to a user's roles or group memberships affect access to resources. Verify the effectiveness of modifications to minimize the risk of unintended access. Apply adjustments to group and role memberships after confirming the intended access assignments.
    -   Security Center
        -   Security Posture Dashboards: View in a single place all critical security KPIs across all instances.
        -   Security Event Notifications: Create policies without creating code that trigger notifications when users or system accounts take action in the ServiceNow AI Platform.
        -   Security Banner Announcements: Trigger new banners in instances that are visible to System Admins and inform them of new, urgent security threats with additional detail.

## Technology Workflows

-   **IT Service Management**
    -   Digital End-User Experience: Proactively alert end-users to device or application health, deflect incidents, and keep them focused on core tasks. Create reports with out-of-the-box insights on the health of key devices and applications. Embed Virtual Agent with Now Assist directly in the desktop client for streamlined support.
    -   Service Operations Workspace: Speed up incident resolutions with contextual recommendations and AI Search directly in the side panel. Reset passwords faster with tailored assistance based on the end-user scenario. Automate migration to Service Operations Workspace with only a few clicks.
    -   Digital Product Release: Accelerate migration from legacy Release Management with simplified utilities. Gain additional flexibility to manage product releases based on defined timelines or completion objectives. Simplify release and product management, as well as reporting, by defining parent and child relationships.
    -   Now Assist for IT Service Management: Quickly summarize change requests and related data. Seamlessly integrate Now Assist and Copilot to increase agent and employee productivity. Generate more accurate knowledge content by automatically drawing on information from multiple incidents powered by Now Assist.
-   **IT Operations Management**
    -   Service Reliability Management: Track and alert on business-critical services to improve uptime and reliability. Enable teams to take ownership of their services and increase innovation. Correlate alerts automatically with service level objectives \(SLOs\).
    -   Automated alert context: Add business context to alerts using fields and tags. Enable correlation without a fully mature CMDB. Use an intuitive UX to group alerts by common fields or tags, including exact match, fuzzy match, or patterns. Escalate alerts to incidents easily and set up email notifications for alert groups.
    -   Discovery Admin Workspace: Opt in to a new content service to enhance discovery capabilities. Improve visualizations of discovery processes. Jump from discovered applications to a unified map for a complete view of your technology.
    -   Manage ACME certificates alongside other certificates. Automate DNS challenges, renewals, and revocations—set up once and let workflows take over. Create custom webhooks and configure low-code scripts.
    -   Link view on Express List: Use map visualization to understand the impact of alerts based on alert tags. View relationships between alerts and technology elements, with or without a mature CMDB. Compatible with Vancouver family release and activated view through Link View application.
    -   Now Assist for IT Operations Management
        -   Alert analysis and incident population: Group alerts by tags, alert text, or CMDB relationships, and explain these groupings to operators. Simplify alerts using clear language from AI. Add technical context to help speed up resolution of alerts and incidents.
-   **Configuration Management Database \(CMDB\)**
    -   Service Graph Connectors for AWS, Azure, and Google Cloud Platform \(GCP\): Integrate major cloud providers into the CMDB using certified connectors. Support various platform outcomes, including visibility, software asset management, high-level architecture \(HLA\), and service operations. Benefit from iterative updates that enhance functionality with each store release to keep up with changing cloud offerings.
    -   Cloud Service Catalog support for Google Cloud Platform \(GCP\): Use Cloud Service templates to request Google Cloud resources quickly. Set up your Cloud Service Catalog in minutes with CSC Guided Setup. Integrate GCP easily. Manage services and instances from a dashboard to optimize resource allocation and control costs while minimizing sprawl.
-   **Software Asset Management**
    -   Software inventory analytics: Examine and address issues pertaining to discovery, normalization, end-of-life, and version sprawl using integrated workflow. Increase visibility with day 0 insights into software deployments, normalization, lifecycle, and application sprawl. Anticipate risk with workflows to remediate end-of-life software.
    -   SAP Digital Access license management: Create entitlements using new license metric for digital access. Gather document types and counts from various clients/systems for compliance view in ServiceNow. Show digital access over/under utilization and compliance with reconciliation process.
-   **Cloud Cost Management**
    -   Spend management for AI services: Gain insights into your AI service expenditures, including comparative analysis of major AI platforms to ensure each dollar contributes to strategic business value. Utilize budgets and alerting mechanisms to assess AI spending and align it with business needs. Streamline cost management processes to address data quality limitations from AI service providers.
-   **Hardware Asset Management**
    -   Device as a Service \(DaaS\): Use the command center view of DaaS inventory to fulfill orders and manage return merchandise authorizations \(RMAs\). Pick, pack, and ship incoming requests through the order fulfillment workflow. Address RMA requests to repair or replace customer assets using the RMA response workflow.
    -   Zero touch request: Save time and reduce logistical overhead with automated asset requests. Integrate with external providers to streamline asset fulfillment without local IT support. Ship assets directly from external vendors to employees.
-   **Hardware Asset Management**
    -   Inventory repair: Initiate, execute, and track asset repairs in repair deposits and warehouses. Troubleshoot to identify and resolve asset defects. Validate repaired assets to help ensure operational readiness or move them for disposal.
    -   Inventory picking with indoor maps: Retrieve stock from inventory for fulfillment via interactive pick task function. Leverage floor mapping and location info to provide directions to assets. Scan to select assets and utilize mobile UI with indoor maps to streamline user experience and improve accuracy.
-   **Enterprise Asset Management**
    -   Asset calibration: Automate calibration scheduling and tracking to minimize the risk of missed calibrations. Ensure all assets are calibrated according to industry standards and regulations with traceability. Use a guided experience with mobile compatibility to perform and document calibration events.
    -   Configurable workspaces: Manage specific asset classes such as industrial, medical, and facility with tailored workspaces for functional departments. Provide a holistic view of assets managed and help ensure that users only see relevant data to their asset class. Improve productivity by providing users with workspaces designed specifically for their functional area.
-   **Security Operations**
    -   Now Assist for Security Operations: Summarize security incidents \(with context on threat and impact\) for faster incident comprehension at any stage of the security incident. Generate resolution notes for faster incident closure. Understand incidents with on-demand incident lifecycle-driven contextualization.
    -   Security Response
        -   Native Sidebar chat: Facilitates seamless transition between shifts through detailed communication of critical information, tasks, and updates. Enhances operational continuity, reduces errors, and improves overall efficiency in the workplace.
        -   Security Incident Response Health dashboard: Obtain detailed information on alert sensors and their operational performance. Gain visibility into customization. Identify and highlight any issues or errors within the environment.
-   **Strategic Portfolio Management**
    -   Now Assist for Strategic Portfolio Management
        -   Multi-feedback summarization: Enhance decision making with actionable insights, enabling product managers to make better informed decisions. Boost efficiency by streamlining the feedback process, allowing for effective product development cycles. Quickly synthesize multiple feedback items into a concise summary, reducing the time needed for manual analysis and work item creation.
        -   Document summarization: Quickly summarize, shorten or elaborate text, making information across teams more accessible and manageable. Improved productivity allowing teams to focus on strategic tasks by reducing the manual effort required for document handling.
    -   Scenario Planning: Create multiple plan alternatives for trade-off analysis and strategic alignment. Accelerate planning with side-by-side scenario comparisons that highlight key differences and strategic impacts. Streamline the approval process by storing and sharing approved scenarios with clear decision rationales to improve efficiency and communication.
    -   Export roadmap to PPT: Enhance presentation with detailed and customizable exports. Visualize progress tracking enabled roadmaps on the presentations. Streamline stakeholder communication with clear, up-to-date timelines.
-   **Collaborative Work Management**
    -   My Work: Centralize tasks from CWM, projects, demands, RIDAC, and stories in one view to streamline work management. Quickly assess the status and volume of work to optimize time management. Identify high priority and overdue tasks, or filter by task type or date range.
-   **Enterprise Architecture**
    -   Enterprise Modeling &amp; Visualization: Intuitive one-click current state modeling with ServiceNow data. Support for standards such as ArchiMate shapes. Visualize and assess the impact of proposed changes and identify potential risks before implementing strategies or projects.
    -   Consolidated Technology Portfolio Management: Set and share standards with TRM category catalog for easy access. Request new product approvals from Enterprise Architecture Workspace. Advise organizations on approved software and hardware product standards.
    -   Enhanced Digital Integration Management: Create duplicate integrations with different applications. Reference subscriber and provider company information when creating new integrations. View and analyze past audit records in activity log.
-   **Operational Technology Management**
    -   Task-oriented landing page: Deliver a better experience with personalized landing pages based on persona and use cases. Increase OT engineer efficiency gains with easy to navigate user experience and task overviews that breakdown task type, status, and urgency level.
    -   Operational Technology Vulnerability Response \(OTVR\) solution management: Simplify workload by accessing authoritative OT recommendations directly from the vendor. Manage complex mixed-vendor ecosystems through a unified display by consolidating recommendations from multiple OEMs in one trusted source. Significantly reduce effort required to determine best action for OT vulnerabilities.
    -   OT request management: Enable users to access OT products and service catalog to create and fulfill complex, multi-step OT requests. Provide secure 3rd party remote access request so service providers and vendors can assist with OT management. Increase visibility of OT landscape with centralized platform to track, monitor, and manage OT requests.
-   **Risk and Resilience products**
    -   Business Continuity Management
        -   BIA and plan enhancements, task automation, nested related plans: Enhanced tracking of RTOs, RPOs, recovery tiers, tasks and dependencies for improved continuity awareness. Speed ITDR plan execution and automate updates of plan dependencies from the CMDB. Minimize impact of a crisis event with greater visibility into task execution and asset recovery order across multiple levels of nested recovery plans.
    -   Integrated Risk Management
        -   AI-powered recommendations to map incoming regulatory changes: AI/ML-powered recommendations identify the closest match between internal documents or citations and incoming alerts. Explore additional context and insights on recommended citations. Associate only those alerts that are relevant for your organization Regulatory Change Management.
        -   Cyber Risk Institute Accelerator powered by Smart Assessment Engine: Import CRI Profile containing related authority documents, citations and control objectives based on NIST CSF. Streamline the risk management process with automated tiering and selection of CRI assessment to be performed using the smart assessment engine. Enjoy automated control creation based on tier and a compliance score calculated from responses to the CRI assessment, rolling up to the entity level.
        -   Cybersecurity Executive Dashboard: Obtain a single pane of glass with security, risk, third party, compliance, business continuity, and audit metrics. Operational dashboard to track the Quarterly goals to improve security and risk posture. Peer benchmarking of security and risk metrics to report wins &amp; support budget planning.
        -   Personal Data Rights, visual data lineage: Efficiently collect, process, and respond to Data Subject Access Requests \(DSARs\) with ServiceNow Personal Data Rights. Capture and visualize data lineage spanning processing activities, business processes, applications, vendors, and more. Centralize and organize regulatory requirements and correspondence by regulatory agency, and automate breach notification based on regulator specifications.
    -   Third-party Risk Management
        -   New third-party element sub-hierarchy, visualization features: Leverage new flexible, user-defined third-party element sub-hierarchy for more granular risk assessments. Examine or aggregate risk scores across individual engagement elements –people, facilities, products, etc. – to make better informed decisions. Map risk at the element level to visualize risk concentration; understand potential geo-political, weather, ESG, or other global impacts to your third parties.
        -   New Risk Intelligence framework, enhanced IRQ scoring logic: Ingest broader Risk Intelligence content types – ex. sanction screening – for use within TPRM workspace. Leverage new Risk Intelligence framework to easily manage providers, normalize scores, order reports within the workspace for increased insights. Streamline workflow, reduce vendor fatigue with more complex IRQ logic, scoring criteria to trigger assessments.
-   **Environmental, Social, and Governance**
    -   Scope 3 dashboard: Track your organization’s GHG emissions for scope 1, 2, and 3. Define your own categories and representation of data. Utilize automated metric definitions.
    -   Metrics enhancements: Define custom labels in formula builder and view labels while constructing formulas. Collect data in custom fiscal calendars. Run metrics on demand.
    -   Content and integrations: Introduce additional emissions factors including emissions activity source into the content accelerator. Update the emissions factors to the most recent version. Add content for CDP, ISSB, and IFRS.

## Employee Workflows

-   **HR Service Delivery**
    -   Guided Decision Trees: Create decision trees with questions, navigation paths, and guidance for agents. Speed up time to resolution by providing guidance throughout the triage process for complex employee inquiries.
    -   Employee Journey Management: Create out of the box analytics dashboards with critical metrics and personas. Enable journey admins to create actionable analytics that drive journeys forward.
    -   Content engagement for Employee Center: Create configurable interactions for news article content including reactions, comments, replies, and views. Enable users to flag content for review and provide feedback. Build re-usable templates for consistent and effective news publishing.
    -   Guided Self-Service: Guide users to the correct article or catalog item through a visual Q&amp;A experience. Create use cases easily, with pre-built activities and templates for self-service help. Streamline the ability to author non-technical documents.
-   **Talent Development**
    -   Leader Hub: Visualize data of overall employee engagement with various talent development activities. Understand the organization's skill competency status. Explore individual skills and competencies with skills information and statistics.
    -   Gigs &amp; Projects: Create configurable opportunities for gigs, projects, volunteer roles, and custom job types. Enable employees to proactively search for opportunities of interest and receive system generated recommendations. Allow managers to quickly review an employee's interest and fit for a posted position.
    -   Now Assist - Proactive Prompts: Engage employees and managers with the relevant reminders to take action on pending activities, approvals, and more. Create conversational experiences for employees that support proactive behavior. Leverage the power of AI to assist employees in keeping up with important to-dos and milestones.
-   **Workplace Service Delivery**
    -   Workplace Services Kiosk: Enable visitors to autonomously register, check-in, and check-out of the workplace. Provide flexibility for workplace admins to configure check-in flows using passcode, phone number, visitor name, or email address.
    -   Multi-building scenario planning: Create and visualize scenario plans across multiple buildings. Facilitate granular allocation changes by accessing floor plans and stack plans of multiple buildings within the same scenario. Move departments, teams, and individuals from one building to another.
-   **Health and Safety**
    -   Health and Safety Case Management: Submit Health and Safety inquiries directly within Employee Center on any device. Enable safety teams to kick off the return to work process from an injury case to track medical clearance information and accommodations. Organize the return to work process cross departments with HRSD journey integrations to successfully coordinate an employee's return to work.
    -   Health and Safety Offline Inspections: Automatically assign scheduled Health and Safety inspections to employees. Enable employees to take Health and Safety inspections when there is no connectivity or Wi-Fi. Proactively identify hazards and reduce risk of employee incident or injuries.
-   **Legal Service Delivery**
    -   AI-powered request categorization and routing: Use machine learning to automatically categorize general legal requests. Automatically route requests to legal staff based on availability, capacity, and skills with Advanced Work Assignment.
    -   Microsoft Outlook integration: Enable fulfillers to create legal requests and pre-populate information directly from Outlook emails. Add emails and attachments to requests with drag and drop. Find legal requests related to emails or search for other requests directly in Outlook.
    -   Contract Management Pro for Sales and Order Management: Leverage one simplified experience to seamlessly integrate the contract workflow into the sales and order management workflow. Seamlessly handle the workflow for configuring, pricing, and quoting with Sales and Order Management. Provide contract creation and review capabilities with Contract Management Pro.
    -   Microsoft Word add-in for signature blocks: Leverage a Word add-in to create and customize signature blocks within contract templates. Add tags to signature blocks such as external vs internal signer, name, title, and date. Enable contract requesters and fulfillers to add additional signers to contracts directly within the document.
    -   Internal review framework: Initiate contract reviews from internal reviewers. Enable internal reviewers to accept or reject tasks and add comments to redlines. Track multiple reviews and their respective deadlines across multiple documents and reviewers.

## Hyperautomation and Low Code

-   **App Engine**
    -   Now Assist for Creator
        -   Data visualization generation: Create analytics visualizations through text, without needing to be an expert. Explore and refine analytics queries with ease for new business insight. Quickly create a data visualization from any KPI in Performance Analytics.
        -   Playbook generation enhancements: Generate previews for quick review and prototyping to build better playbooks. Re-prompt using simple text to ideate for ideal playbook creation. Automate using GenAI recommendations for activity placeholders.
-   **Automation Engine**
    -   Enhanced security in Integration Hub: Use personal authentication to reduce the need for super user/admin log in credentials to access third-party systems. Store OAuth tokens on MID Server and mTLS certificates in CyberArk. Unlock additional use cases in industries with stringent security requirements, such as in banking and healthcare.
    -   Queue efficiency tracker: Determine cost and time savings at the work-item level of an automation. Improve business processes, resource allocation, and reporting with granular automation value metrics.
    -   Sample automations: Jumpstart your automation journey with a library of pre-built sample automations.

## Customer Workflows

-   **Customer Service Management**
    -   Rich messaging in Service Catalog: Complete request intake during chat, eliminating pop-ups and lengthy Q&amp;As. Direct customers to service catalogs that trigger optimal process to resolution. Make service catalogs accessible on non-ServiceNow portals and native mobile apps \(with Engagement Messenger\).
    -   Service model foundation - Inter-organization support: Streamline communication for service organizations and improve visibility. Reduce back and forth communication by providing key context alongside cases for service organizations. Define support structures for service organizations through hierarchies or relationship criteria.
    -   Email enhancements for CSM Workspace: Enable agents to quickly and effectively respond to emails. Make it easier for agents to learn CSM Workspace based on similar UX \(e.g. Gmail\). Consolidate locations for common actions \(e.g. discards, drafts\) and increase real estate for composition.
-   **Now Assist for Customer Service Management**
    -   Email reply recommendations: Enable agents to quickly and effectively respond to customer emails while reducing manual errors. Personalize email replies to match customer tone and sentiment.
    -   Chat reply recommendations: Enable agents to respond to the customer quickly and effectively during chat interactions. Personalize chat responses to match customer tone and sentiment.
    -   Prompt configurability: Receive more comprehensive summaries, enabling agents to respond more accurately and quicker. Improve agent productivity with more complete and contextual summaries.
    -   Sidebar summarization: Summarize Sidebar conversations and make them easily shareable to the case.
-   **Sales and Order Management**
    -   Lead Management: Create or import leads, manage the end-to-end lead cycle, use Kanban view to change status via drag and drop. Launch needs analysis questionnaire to identify relevant product offers. Manage lead activities and view priority activities needing attention, like incoming email or upcoming tasks. Quickly create opportunities and map to accounts/contacts or consumers.
    -   Contract Management for Sales and Order Management: Automate creation of legal sales contracts from quotes to reduce manual steps and errors. Generate document with quote header, line details, terms, conditions and signatories. Configurable workflows ensure company-defined approval matrices are followed. Tailor contracts based on customer and products purchased to improve customer satisfaction.
    -   Quote Management Sales Agreements: Quickly convert quotes to sales agreements to accelerate revenue and improve operational efficiency. Create sales agreements in ServiceNow or sync externally created agreements for a consistent, unified view. Enforce agreements while creating orders by filtering catalogs and applying agreement-based prices.
    -   Opportunity Management integration with Field Service Management: Allows technicians to create opportunities during field engagements leveraging previously captured information. Upsell or cross-sell additional products and services during field service visits.
    -   Product Catalog Management enhancements: Associate product specifications to any level of product offer hierarchy to improve technical catalog mapping. Use eligibility rules to dynamically filter catalogs, categories, and product offers, increasing customer satisfaction, accuracy, and agent efficiency. Set default configurations and pre-populate values in configurator..
-   **Field Service Management \(FSM\)**
    -   Now Assist for Field Service Management
        -   Knowledge article generation: Generate draft knowledge articles based on task finalization. Share useful information with technicians from solutions implemented to address customer issues. Reduce the need for extensive research and information gathering to shorten repair times.
        -   Prompt configuration: Edit input configurations and output formats to customize out-of-the-box skills. Test generated responses to help ensure accuracy and relevancy. Customize Now Assist skill availability.
        -   Sidebar chat summarization: Minimize time spent searching and sifting through conversation histories with concise summaries. Acquire necessary information quickly to efficiently schedule and prepare tasks for completion.
        -   Extended work order task summary: Equip technicians with essential work order task details to expedite task completion. Fine-tune prompt through configuration to improve accuracy of work order task summary. Generate a concise work order task summary, inclusive of affected products, on one screen.
    -   Opportunity management with field service: Generate opportunities in the field with intuitive data capture, multimedia support, and real-time sync. View, search, and filter self-created opportunities with ease to track progression and maturation. Position technicians as trusted advisers to increase the conversion rate of opportunities into revenue.
    -   Collaborative mobile sidebar: Communicate with relevant parties natively in the Mobile Agent app. Seamlessly engage experts for issue resolution within the context of a task. Preserve task-related conversations for ongoing process enhancement.
    -   Temporary technician territory relocation: Designate destination territory, location assignment, and timeline enforcement for temporary placements. Match resource availability to task execution when addressing unscheduled work.
    -   Dispatcher Workspace scheduling options: Visualize and select work blocks in identification of the best technician available according to schedule. Schedule work order tasks from map view as opposed to hybrid mode.
    -   Multiple work configurations: Define distinct processes based on work type to execute tasks more accurately. Configure business rules, service level agreements, and questionnaires to improve data collection. Centralize enterprise processes within a single instance to avoid workflow consolidation.

## Industry Products

-   **Financial Services Operations \(FSO\) for Banking**
    -   Now Assist for Financial Services Operations
        -   Dispute summarization: Improve customer satisfaction with faster, informed communication. Boost agent productivity by automating tedious work, like digging through voluminous case details. Promote collaboration and seamless hand-offs amongst agents by automatically providing role-specific case details.
    -   Verifi integration: Bolster customer trust by handling disputes quickly, with timely merchant communications. Save money on operational costs with real-time notifications to merchants for pre-dispute resolutions. Consolidate systems with the flexibility to resolve Visa and non-Visa dispute cases on a single platform.
    -   Dispute rules content pack for Visa: Leverage proactive dispute resolution and the automated assignment of reason codes to drive faster resolutions. Decrease dispute costs with optimized processes that determine chargeback eligibility immediately, ahead of the submission network. Reduce IT costs on Visa rules updates with pre-configured integration and built-in ongoing rules maintenance.
    -   Dispute rules content pack for Mastercard: Leverage proactive dispute resolution and the automated assignment of reason codes to drive faster resolutions. Decrease dispute costs with optimized processes that determine chargeback eligibility immediately, ahead of the submission network. Reduce IT costs on Mastercard rules updates with pre-configured integration and built-in ongoing rules maintenance.
    -   Cardholder dispute portal: Improve customer experience through reduced back and forth with agents and self-service visibility on dispute status. Reduce contact center volumes by allowing customers to initiate a dispute through self-service, requiring sufficient details for the case agent. Minimize total time to resolve disputes by capturing all the relevant case details from the customer at the start.
    -   Dispute content pack for US regulations: Support timely resolutions of high priority disputes through automated prioritization, tracking, and reporting. Maintain compliance and provide customers with dispute status visibility through email templates, complete with in-process triggers aligned to regulation requirements. Help avoid fines and penalties by providing dispute agents with a convenient method to refund fees, interest, and issue provisional credits.
-   **Financial Services Operations for Insurance**
    -   Now Assist for Financial Services Operations
        -   Claim summarization: Provide users with crucial case context through straightforward and concise claim summaries. Boost customer satisfaction with better informed agents, minimizing the need to ask repeat questions to customers. Promote transparency and consistency across personas by easily inserting a synthesis of claim work and history directly into the claim file.
        -   Email reply recommendations: Enable users to quickly and effectively respond to customer emails while reducing manual errors. Personalize email replies to match customer tone and sentiment. Respond to customers faster, reducing time to resolve.
        -   Chat reply recommendations: Enable users to respond to customers quickly and effectively during chat interactions. Personalize chat responses to match customer tone and sentiment. Provide users with recommendations to help them effectively position offers at the right time.
        -   Prompt configurability: Receive better summaries, enabling users to know how and when best to act. Handle cases more effectively with more empathy and confidence. Improve user productivity with more complete summaries with full context.
    -   Life claims foundation: Relieve employees of time-consuming tasks with automation and task orchestration capabilities for the end-to-end life claims process. Avoid confusion and allow for quicker processing with multiple policies and beneficiaries supported from a single claim file. Increase speed to market with a robust foundation and data model that allows customers to easily expand use cases.
-   **Manufacturing Commercial Operations**
    -   Service Bridge enhancements: Streamline Service Catalog management across internal and provider requests. Enable real-time access to provider data during service request submissions. Facilitate seamless task-to-task integration between provider and consumer instances. Support version mismatches to allow providers to update while maintaining consumer compatibility.
    -   Configure Price Quote enhancements: Automate creation of legal sales contracts from quotes to reduce manual steps and errors. Generate comprehensive contract documents including quote details, terms, and signatories. Enable single-click conversion of quotes to sales agreements for faster revenue realization. Enforce agreement terms during order creation with filtered catalogs and agreement-based pricing. Enhance product catalog management with improved technical mapping and eligibility rules.
    -   Lead and Opportunity Management: Manage the complete lead lifecycle with Kanban view and needs analysis questionnaires. Quickly convert qualified leads to opportunities and map to accounts or contacts. Enable field service technicians to create sales opportunities during customer visits. Foster better customer relationships by identifying and capturing additional needs on-site. Improve upsell and cross-sell capabilities during field service engagements.
-   **Technology**
    -   Now Assist for Telecom, Media, and Technology
        -   Customer Service Problem Management: Self-service summaries make handoffs easier and provide both agents and customers real-time status updates as problems get resolved. Quickly and easily interpret test results in plain language and automate test results, diagnosing issues faster, and speeding up resolution. Save time with clear, concise resolution summaries that speed up case wrap-up, keep customers informed, and serve as future reference for agents.
-   **Technology Provider Service Management**
    -   Account Life cycle Events: Understand engagement details such as success initiatives, touchpoints, and risks in a single workspace. Enable customer success managers with automated, easy-to-trigger workflows without requiring technical knowledge. Increase customer lifetime value by ensuring product adoption, achieving business objectives, and measuring tangible success results.
    -   Customer Service Problem Management: Implement a structured approach to identify and resolve issues efficiently with diagnostic framework. Optimize service management by navigating through four core stages: Service Verification, Service Diagnostics, Resolution, and Test &amp; Closure. Utilize a defined diagnostic framework to effectively handle service issues.
    -   Service Bridge - Mismatched version support and configuration revisions: Improve scalability for providers and enhance customer support by accommodating different versions of Service Bridge. Enable providers to develop and deliver new capabilities to customers on recent application versions. Enhance deployment and support of Service Bridge entitlements with configuration revisions.
    -   Service Bridge - Consumer pre-flows: Enable consumers to initiate a flow before synchronizing Remote Record Producer requests with providers.
-   **Sales and Order Management for Technology Providers**
    -   Service Bridge - Order Management support: Providers can publish product and service offerings to Service Bridge connected customers as remote record producers. Order and manage product offerings published as RRPs on the customer instance. Facilitate new, disconnect, suspend, and resume product and service orders
    -   Order Management: Enable customers to easily request a service move via the channel of their choice. Streamline the process to validate and confirm the change order is feasible. Seamlessly disconnect and reconnect services to ensure smooth transitions between locations.
-   **Telecommunications**
    -   Now Assist for Telecom, Media, and Technology \(TMT\)
        -   Customer Service Problem Management: Self-service summaries make handoffs easier and provide both agents and customers real-time status updates as problems get resolved. Quickly and easily interpret test results in plain language and automate test results, diagnosing issues faster, and speeding up resolution. Save time with clear, concise resolution summaries that speed up case wrap-up, keep customers informed, and serve as future reference for agents.
-   **Telecommunications Service Management**
    -   Account Life cycle Events - Customer Success: Understand engagement details such as success initiatives, touchpoints, and risks in a single workspace. Empower customer success managers with automated, easy-to-trigger workflows, requiring no technical knowledge. Increase customer lifetime value by ensuring product adoption, achieving business objectives, and measuring tangible success results.
    -   Customer Service Problem Management: Implement a structured approach to identify and resolve issues efficiently with diagnostic framework. Optimize service management by navigating through four core stages: Service Verification, Service Diagnostics, Resolution, and Test &amp; Closure. Utilize a dedicated case type based on the TM Forum-defined framework.
    -   Service Bridge - Mismatched Version Support and Configuration Revisions: Improve scalability for providers and enhance customer support by accommodating different versions of Service Bridge. Enable providers to develop and deliver new capabilities to customers on recent application versions. Improve deployment and support of Service Bridge entitlements with configuration revisions.
    -   Service Bridge - Consumer Pre-flows: Enable consumers to initiate a flow before synchronizing Remote Record Producer requests with providers.
-   **Telecommunications Network Inventory**
    -   Enhanced Circuit Visualization: View current and historical designs of connections for informed decision- making during network upgrades. Display and manage redundancy paths of connections and deliver reliable networks. Assign card, slot, and port for connection elements and maintain accurate circuit data. Easily identify route topology connection points.
    -   Enhanced Planned Revision: Display logical connection details and connection elements in a single circuit overview page for accurate planning. Validate revised designs against the original design for a clear understanding of changes. Keep one year record of circuit design changes for historical reference and troubleshooting.
    -   Enhanced Rack Management User Interface: Add, move, or remove rack equipment with ease and increased flexibility and scalability to maintain rack inventory. Reserve rack units for future implementation or un-reserve when not required. View rack edits side-by-side to the current rack layout prior to saving edits and increase inventory accuracy. Display rack power and weight KPIs and monitor rack limitation.
-   **Sales and Order Management for Telecommunications**
    -   Service Bridge - Order Management Support: Providers can publish product and service offerings to Service Bridge connected customers as remote record producers. Customers gain easy access to order and manage product offerings published as RRPs on the customer instance. Facilitates new, disconnect, suspend, and resume product and service orders.
    -   Order Management - Change orders for location changes: Empower customers to easily request a service move via the channel of their choice. Streamline the process to validate and confirm the change order is feasible. Seamlessly disconnect and reconnect services to ensure smooth transitions between locations.
-   **Government**
    -   Information Request playbook enhancements: Process record requests efficiently with out of the box document redaction embedded directly into workflows. Reduce administrative burden with easy document search, text masking, change previews and version control. Securely obscure the sensitive and classified information in public records.
    -   Now Assist for Public Sector Digital Services \(PSDS\)
        -   Case summarization: Provide a summary of prior actions and recommended next steps for a seamless workflow. Speed up resolution times by reducing the effort needed for agents to begin their tasks.
    -   Retail Data Model: Reduce time to value with retail specific attributes within OOTB retail fields. Improve admin experience by including important retail attributes during configuration. Increase operational efficiency by providing foundational data required for retail cases and future automation.
    -   Retail Base Case: Reduce time to value with a retail case type for OOTB usage and to reduce customization needs. Improve agent experience by displaying key retail content for store support use cases. Improve store worker experience by tailoring default case submission forms to store use cases.
-   **Retail Operations &amp; Retail Service Management**
    -   Retail Data Model: Reduce time to value with retail specific attributes within OOTB retail fields. Improve admin experience by including important retail attributes during configuration. Increase operational efficiency by providing foundational data required for retail cases and future automation.
    -   Retail Base Case: Reduce time to value with a retail case type for OOTB usage and to reduce customization needs. Improve agent experience by displaying key retail content for store support use cases. Improve store worker experience by tailoring default case submission forms to store use cases.

## Finance &amp; Supply Chain Workflows

-   **Source-to-Pay Operations**
    -   Now Assist for Sourcing and Procurement Operations: Guide requesters using natural language to easily find and order the right products and services from the best suppliers. Create better procurement intake experience at scale without relying on experts or manual processes. Reduce costs, errors, and cycle times by automating the intake and fulfillment of requests.
    -   Sourcing &amp; Procurement Operations + Contract Management Pro: Streamlines contracting requests and creates an efficient end-to-end process. Reduces manual work and keeps teams focused on productive activities. Reduces risks by integrating compliance and risk mitigation into a collaborative contract lifecycle.

## ServiceNow Impact

-   **SeviceNow Impact**
    -   Impact adoption accelerators:
        -   Jumpstart Your Common Service Data Model \(CSDM\)
        -   Jumpstart Your Event Management
        -   Jumpstart Your Process Mining
        -   Jumpstart Your Issue Auto Resolution
        -   Jumpstart Your Document Intelligence
        -   Extend Your Employee Center to Pro
    -   Impact assessment accelerators:
        -   Integrated Risk Management
        -   Software Asset Management
        -   CSDM – Technical Services
        -   CSDM – Business Services
        -   UX Taxonomy Review &amp; Design
    -   AI recommendation engine enhancements: Receive relevant recommendations quickly, triggered by similar or related Impact initiatives completed. See the reasons behind each recommendation on the "All Recommendations" page that features an updated UI and richer contextual detail.
    -   Health assessment dashboard enhancements – automated insights: Act swiftly on detailed findings quickly after completing a health scan. Mitigate conflicting actions effectively. Begin work more quickly with streamlined prioritization process.
    -   Value blueprint enhancements: Generate a new value blueprint to replace one that is out of date. Build automated value blueprints for multiple instances. Automate data collection for App Engine and Enterprise Architecture \(formerly APM\) products.

## Upgrading to the Xanadu release

Upgrade to the ServiceNow AI Platform Xanadu release today. Take advantage of these ServiceNow resources to help you stay current.

Get your Xanadu release upgrade kit: Find everything you need to get started on your upgrade, including a summary of new features, demos, key resources, and more.

ServiceNow Releases and Upgrades community: Ask questions and get answers from ServiceNow experts and peers, get access to the latest best practices and resources, and register for releases and upgrades community events for additional support.


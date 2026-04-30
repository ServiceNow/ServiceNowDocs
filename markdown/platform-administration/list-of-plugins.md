---
title: List of plugins \(Zurich\)
description: List of all plugins that you can activate if you have the admin role.This table lists all plugins and ServiceNow Store applications that have been introduced in Zurich. You can activate or install these plugins or applications if you have the admin role.This table lists all plugins that you can activate if you have the admin role.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 234
breadcrumb: [ServiceNow plugins, Basic system configuration, Get started, Administer]
---

# List of plugins \(Zurich\)

List of all plugins that you can activate if you have the admin role.

If a plugin does not appear on this list, it may require activation by ServiceNow personnel. Request these plugins through the Now Support Customer Service System instead of activating them yourself.

-   For steps on activating a plugin yourself, see [Activate a plugin](../task/t_ActivateAPlugin.md).
-   For steps on requesting a plugin that you cannot activate yourself, see [Request a plugin](../task/t_RequestAPlugin.md).
-   For steps on installing a ServiceNow Store application, see [Install a ServiceNow Store application](../../../build/applications/task/t_InstallApplications.md).

**Note:** For a list of all new and changed plugins for this release, see [Changes to plugins in the Zurich release](https://www.servicenow.com/docs/access?context=plugin-changes&version=zurich&pubname=zurich-release-notes&ft:locale=en-US).

**Parent Topic:**[ServiceNow plugins](../concept/c_ServiceNowPlugins.md)

**Related topics**  


[Activate a plugin](../task/t_ActivateAPlugin.md)

[Request a plugin](../task/t_RequestAPlugin.md)

## New plugins in Zurich

This table lists all plugins and ServiceNow Store applications that have been introduced in Zurich. You can activate or install these plugins or applications if you have the admin role.

**Note:** By default, all ServiceNow Store applications listed in this table are compatible with Zurich unless a note is mentioned for the application.

<table id="table_v_plugins"><thead><tr><th>

Plugin \[ID\]

</th><th>

Description

</th><th>

State

</th><th>

Has Demo Data?

</th><th>

Dependencies

</th></tr></thead><tbody><tr><td>

AI discovery \[sn\_ai\_disc\] \(Available in the ServiceNow Store\)

</td><td>

Enables organizations to create hyperscaler connections with third party applications to discover AI assets.

</td><td>

Active

</td><td>

false

</td><td>

-   ServiceNow IntegrationHub Action Step - REST
-   ServiceNow IntegrationHub Runtime
-   Complex Object
-   ServiceNow IntegrationHub Action Step - Get Connection Info

</td></tr><tr><td>

AI Gateway \[app-awh-for-ai-control-tower\]

</td><td>

Enables enterprises to actively manage, govern and observe their MCP \(Model Context Protocol\) traffic, ensuring secure operation of Agentic workflows across enterprise boundaries.

</td><td>

Active

</td><td>

 

</td><td>

sn\_ai\_governance 5.0.6

 sn\_telemetry\_data 1.1.10

</td></tr><tr><td>

Asset Audit Response \[sn\_audit\_response\] \(Available in the ServiceNow Store\)

</td><td>

Includes a new Asset Governance workspace and components from Audit Management to help asset managers respond to and manage evidence requests for regulatory audits within the financial sector.

</td><td>

Inactive

</td><td>

false

</td><td>

-   com.sn\_grc\_advanced
-   com.sn\_compliance
-   com.sn\_audit\_workspace
-   com.sn\_grc\_ftr\_role com.sn\_finserv\_cntrl

</td></tr><tr><td>

Asset Management Integration for Sourcing and Procurement Operations \[sn\_spend\_asset\] \(Available in the ServiceNow Store\)

</td><td>

Integrates IT Asset Management with Sourcing and Procurement Operations, enabling a seamless experience where asset management processes align with Sourcing and Procurement Operation workflows.

</td><td>

Inactive

</td><td>

true

</td><td>

-   Sourcing and Purchasing Automation \[com.snc.sn\_pr\]
-   Procurement \[com.snc.procurement\]
-   Shopping Hub \[com.snc.uib.sn\_spend\_uib\]

</td></tr><tr><td>

Business Object Core \[sn\_bo\_core\] \(Available in the ServiceNow Store\)

</td><td>

Enables you to create and monitor sales process records using Lead-to-Cash Process Management application.

</td><td>

Active

</td><td>

true

</td><td>

 

</td></tr><tr><td>

Card data security \[sn\_data\_sec\] \(Available in the ServiceNow Store\)

</td><td>

Enables you to tokenize sensitive card data, such as primary account numbers \(PANs\), in Financial Services Operations dispute workflows.

</td><td>

Inactive

</td><td>

false

</td><td>

 

</td></tr><tr><td>

Care Team Operations Application \[sn\_cto\_apps\] \(Available in the ServiceNow Store\)

</td><td>

Enables care team members/managers to raise requests to various departments in the hospital.

</td><td>

Inactive

</td><td>

true

</td><td>

com.sn\_hco

</td></tr><tr><td>

Care Team Operations Core \[sn\_cto\_core\] \(Available in the ServiceNow Store\)

</td><td>

Contains the Care team portal and the base case for healthcare operations.

</td><td>

Inactive

</td><td>

false

</td><td>

com.sn\_hco

</td></tr><tr><td>

Care Team Operations for Environmental Services \[sn\_cto\_evs\] \(Available in the ServiceNow Store\)

</td><td>

Contains the case types to report and fulfill EVS issues.

</td><td>

Inactive

</td><td>

true

</td><td>

com.sn\_hco

</td></tr><tr><td>

Care Team Operations for Facilities \[sn\_cto\_facilities\] \(Available in the ServiceNow Store\)

</td><td>

Contains the case types to report and address facility issues.

</td><td>

Inactive

</td><td>

true

</td><td>

com.sn\_hco

</td></tr><tr><td>

Care Team Work Management \[sn\_cto\] \(Available in the ServiceNow Store\)

</td><td>

Supports the creation, assignment, tracking, and completion of non-EHR tasks. This capability provides a centralized, accessible platform that clearly delineates responsibilities, deadlines, status updates, and documentation, supporting audit readiness and continuous compliance with regulatory standards.

</td><td>

Inactive

</td><td>

false

</td><td>

com.sn\_hco

</td></tr><tr><td>

Integration - Multiple Provider Single Sign-On Installer \[com.snc.integration.sso.multi.installer\] \(Available in the ServiceNow Store\)

</td><td>

Enables organizations to authenticate against multiple IDPs \(Identity providers\) using SAML or OpenID connect \(OIDC\).

</td><td>

Active

</td><td>

false

</td><td>

 

</td></tr><tr><td>

CRM Task Plan Templates \(Available in the ServiceNow Store\)

</td><td>

Enables the business user to define repeatable tasks and other items needed to complete a business process.

</td><td>

Inactive

</td><td>

false

</td><td>

CSM Configurable Workspace \[com.snc.uib.csm\_agent\_workspace\]

</td></tr><tr><td>

CSM Data Classification \[com.snc.csm\_data\_privacy\] \(Available in the ServiceNow Store\)

</td><td>

Provides base system classifications for customer relationship management \(CRM\) data, categorizing it as internal, personally identifiable information \(PII\), confidential, and more.

</td><td>

Inactive

</td><td>

false

</td><td>

-   Customer Service plugin \[com.sn\_customerservice\]
-   Data Classification plugin \[com.glide.data\_classification\]

</td></tr><tr><td>

Customer Engagement Sequences \[sn\_crm\_sequence\] \(Available in the ServiceNow Store\)

</td><td>

Enables customer-focused teams to execute structured, personalized outreach and follow-up activities to engage customers throughout the time they’re associated with your business.

</td><td>

Active

</td><td>

false

</td><td>

Playbook experience \[com.playbook\_experience\]

</td></tr><tr><td>

Digital End-User Experience \(DEX\) for Microsoft 365 \[sn\_dex\_ms365\] \(Available in the ServiceNow Store\)

</td><td>

Integrates with Microsoft 365 services, such as Microsoft Teams. It enables seamless access to Microsoft 365 data and supports various integration scenarios, enhancing productivity and collaboration across the platform.

</td><td>

Active

</td><td>

false

</td><td>

ServiceNow IntegrationHub Action Step - REST \[com.glide.hub.action\_step.rest\]

</td></tr><tr><td>

Domain Extensions Installer Virtual Plugin \[com.glide.domain.msp\_extensions.installer\_virtual\]

</td><td>

Helps to coordinate other domain plugin installations. It acts as an intermediary to check whether it is safe to activate the Domain Extensions plugin on a given instance.

</td><td>

Inactive

</td><td>

false

</td><td>

Domain Separation with Data and process separation turned off.

</td></tr><tr><td>

Employee Center Browser Extension \[sn\_ex\_brw\_ext\] \(Available in the ServiceNow Store\)

</td><td>

Provides a Browser Extension to access different touch points of the Employee Center portal.

</td><td>

Inactive

</td><td>

false

</td><td>

Employee Center \[sn\_ex\_sp\]

</td></tr><tr><td>

Field Service Demo Work Configuration for Break fix \[com.snc.fsm\_mri\_scanner\_breakfix\_work\_config\]

</td><td>

Provides a sample work configuration to perform break fix on MRI scanners. The sample work configuration showcases extension of the base work order tasks to introduce attributes specific to break fix for MRI scanners.

</td><td>

Inactive

</td><td>

true

</td><td>

Field Service Work Configurations \[com.snc.fsm\_work\_types\]

</td></tr><tr><td>

Financial Services Operations Integration with Mastercard \(Available in the ServiceNow Store\)

</td><td>

Offers a streamlined and efficient solution for financial institutions to manage Mastercard disputes. By integrating with Mastercard's spoke actions, the application facilitates key dispute life cycle events, including transaction search, chargeback creation, pre-arbitration, arbitration, and fraud reporting.

</td><td>

Inactive

</td><td>

false

</td><td>

-   com.sn\_mc\_spoke
-   com.sn\_bom\_mcard\_cp

</td></tr><tr><td>

GRC: Continuous Authorization and Monitoring Advanced \[sn\_cam\_advanced\] \(Available in the ServiceNow Store\)

</td><td>

Enables full access to Continuous Authorization and Monitoring Workspace features for IRM Enterprise customers.

</td><td>

Active

</td><td>

false

</td><td>

 

</td></tr><tr><td>

ITAM common hub \[sn\_itam\_comm\_hub\] \(Available in the ServiceNow Store\)

</td><td>

The Asset Management Common Hub application aligns the features that are common to Hardware Asset Management, Software Asset Management, and Enterprise Asset Management.

</td><td>

Inactive

</td><td>

false

</td><td>

 

</td></tr><tr><td>

Lead-to-Cash Process Management \[app-l2c-cockpit\] \(Available in the ServiceNow Store\)

</td><td>

Provides sales managers and contract administrators with a real-time, consolidated view of tasks, emails, and other details related to sales entities such as opportunities, quotes, and orders in a hierarchical node map.

</td><td>

Active

</td><td>

true

</td><td>

Business Object Core \[sn\_bo\_core\]

</td></tr><tr><td>

Legal Hold Notification \[sn\_lg\_hold\] \(Available in the ServiceNow Store\)

</td><td>

Helps organizations manage their legal obligations to preserve relevant information when a legal hold is issued.

</td><td>

Inactive

</td><td>

false

</td><td>

 

</td></tr><tr><td>

Machine Identity Console \[com.glide.identity.machine\_identity\_console\]

</td><td>

Helps administrators to manage machine identities.

</td><td>

Inactive

</td><td>

false

</td><td>

 

</td></tr><tr><td>

Model Context Protocol Server \[sn\_mcp\_server\]

</td><td>

MCP Server Console enables secure and governed access to functionality on a ServiceNow instance for AI applications with Model Context Protocol \(MCP\) servers.

</td><td>

Inactive

</td><td>

false

</td><td>

Generative AI Controller

</td></tr><tr><td>

Mobile Requesting \[sn\_cto\_mobile\] \(Available in the ServiceNow Store\)

</td><td>

Provides care teams with an intuitive, native mobile experience for reporting, tracking, and managing cases.

</td><td>

Inactive

</td><td>

false

</td><td>

-   com.sn\_mab
-   sn\_mab\_api
-   com.sn\_hco

</td></tr><tr><td>

Notifications for Employee Center \[com.snc.employee\_center\_notifications\] \(Available in the ServiceNow Store\)

</td><td>

Provides employees with timely and relevant information across multiple departments promoting engagement and increasing productivity.

</td><td>

Inactive

</td><td>

false

</td><td>

Employee Center \[sn\_ex\_sp\]

</td></tr><tr><td>

Order Management for Business Location \[com.snc.business\_location\_orm\]

</td><td>

Streamlines agents to manage customer orders and empower channel partner staff to create, modify, and track orders throughout the sales process.

</td><td>

Active

</td><td>

false

</td><td>

 

</td></tr><tr><td>

Payment card \[sn\_payment\_card\] \(Available in the ServiceNow Store\)

</td><td>

Store the details of physical payment cards across the entire card life-cycle, from issuance to servicing. Store tokenized values for sensitive data, such as the primary account number \(PAN\).

</td><td>

Inactive

</td><td>

false

</td><td>

 

</td></tr><tr><td>

Performance Analyzer \[sn\_perf\_page\] \(Available in the ServiceNow Store\)

</td><td>

Performance Analyzer enables you to access page load time data, trends, and waterfall visualizations directly from your instance. It also helps you to identify page performance issues and bottlenecks in UX framework pages independently.

</td><td>

Active

</td><td>

false

</td><td>

 

</td></tr><tr><td>

Product capability core \[sn\_prod\_cap\_core\] \(Available in the ServiceNow Store\)

</td><td>

Enables organizations to define, manage, and assess capabilities across product models.

</td><td>

Active

</td><td>

true

</td><td>

-   com.sn\_data\_ctx\_engine
-   com.sn\_ti\_core
-   com.snc.install\_base
-   com.playbook\_experience
-   com.sn\_csm\_playbook
-   com.snc.csm\_case\_types
-   com.snc.sn\_record\_related\_items\_connected
-   com.snc.guided\_decisions\_playbook\_experience
-   com.snc.sn\_record\_lookup
-   com.sn\_meeting\_mgmt
-   com.snc.platform\_document\_management
-   sn\_roadmap
-   com.snc.csm\_action\_status
-   com.sn\_align\_core, com.servicenow\_now\_calendar

</td></tr><tr><td>

Quote Management for Business Locations \[com.snc.business\_organization\_qm\] \(Available in the ServiceNow Store\)

</td><td>

Streamlines the creation and tracking of quotes by channel partners during the sales life cycle of customers. It also ensures accurate pricing, optimal product selection, and timely responses to customer requests.

</td><td>

Active

</td><td>

true

</td><td>

-   app-business-location
-   app-l2c-quote-mgmt

</td></tr><tr><td>

Recall campaigns and claims \[sn\_rcl\_claim\_mgmt\] \(Available in the ServiceNow Store\)

</td><td>

Manage all entities and flows related to Recall Campaigns and Claims within MCO.

</td><td>

Active

</td><td>

true

</td><td>

 

</td></tr><tr><td>

Retail Customer Complaint \[sn\_rtl\_cs\_cmplnt\] \(Available in the ServiceNow Store\)

</td><td>

Improve the customer experience to capture store-related complaints from guests. This case type helps you coordinate effective responses, boosting operational efficiency.

</td><td>

Active

</td><td>

true

</td><td>

-   com.sn\_customerservice
-   com.sn\_retail\_core

</td></tr><tr><td>

Retail HQ Operations \[sn\_rtl\_hq\_ops\] \(Available in the ServiceNow Store\)

</td><td>

Initiate and coordinate large-scale actions across multiple stores, enhancing operational efficiency with the new HQ Communications case type.

</td><td>

Active

</td><td>

false

</td><td>

com.sn\_retail\_core

</td></tr><tr><td>

Retail In-store Operations \[sn\_rtl\_instore\_ops\] \(Available in the ServiceNow Store\)

</td><td>

Enhance operational efficiency by standardizing the reporting, tracking, and resolution of in-store issues with the new Retail In-store Operations case type. With structured task assignments and tracking, you can reduce the time to resolution.

</td><td>

Active

</td><td>

false

</td><td>

-   com.sn\_retail\_core
-   com.sn\_retail\_mobile
-   com.snc.work\_management

</td></tr><tr><td>

Retail Mobile application \[sn\_retail\_mobile\] \(Available in the ServiceNow Store\)

</td><td>

Efficiently manage operations and access key tools on the go, improving the store team’s experience and boosting productivity.

</td><td>

Active

</td><td>

false

</td><td>

-   com.glide.sg
-   com.glide.sg.offline
-   com.glide.sg.agent\_native\_client
-   com.sn\_retail\_core

</td></tr><tr><td>

Retail Store Services \[sn\_rtl\_stre\_servcs\] \(Available in the ServiceNow Store\)

</td><td>

Streamline the process for contacting HQ with the new Store Inquiry case type in Retail Store Services plugin, enhancing the store team experience. This case type provides a clearly defined workflow for resolution at HQ, enhancing operational efficiency.

</td><td>

Active

</td><td>

true

</td><td>

-   com.sn\_retail\_core
-   com.sn\_retail\_mobile

</td></tr><tr><td>

RMA Case Management \[com.sn\_csm\_rma\_case\]

</td><td>

The RMA Case application enables organizations to manage and triage return cases for customer products and services, addressing returns, replacements, and repair use cases.

</td><td>

Inactive

</td><td>

false

</td><td>

-   Lead to Cash Core \[com.snc.l2c\_core\]
-   Customer Service Install Base Management \[com.snc.install\_base\]
-   Case lines and workflows \[com.sn\_case\_line\]
-   Entitlements Verification \[com.sn\_ent\_verify\]

</td></tr><tr><td>

Sales Cart plugin \[sn\_sales\_cart\] \(Available in the ServiceNow Store\)

</td><td>

Provides new order checkout experience and improved cart capabilities, including cart persistence, ability to download the cart summary, and a guided order checkout process.

</td><td>

Active

</td><td>

false

</td><td>

-   Product Catalog Management Portal \[com.prd\_pm\_portal\]
-   Price Management \[com.sn\_csm\_pricing\]
-   Sales Common \[com.sn\_l2c\_sales\_common\]
-   Document Templates \[com.snc.document\_templates\]
-   Playbooks for Customer Service Management \[com.sn\_csm\_playbook\]

</td></tr><tr><td>

Sales promotion and claims \[sn\_sls\_prm\_clm\_mgt\] \(Available in the ServiceNow Store\)

</td><td>

Manage all entities and flows related to Sales Promotion Claims within MCO.

</td><td>

Active

</td><td>

true

</td><td>

 

</td></tr><tr><td>

Service Bridge Health \[sn\_sb\_health\] \(Available in the ServiceNow Store\)

</td><td>

Create and maintain Instance Scan Checks that proactively identify findings for the Service Bridge Audit.

</td><td>

Active

</td><td>

false

</td><td>

 

</td></tr><tr><td>

Sourcing Pipeline Management \[sn\_spend\_pipeline\] \(Available in the ServiceNow Store\)

</td><td>

Enables centralized creation, tracking, and execution of sourcing initiatives through pipeline projects. It streamlines savings tracking and forecasting with built-in workflow automation and also provides complete visibility into pipeline progress and impact.

</td><td>

Inactive

</td><td>

false

</td><td>

Spend and Savings Management \[sn\_spend\_mgmt\]

</td></tr><tr><td>

Supplier Operations \[sn\_so\] \(Available in the ServiceNow Store\)

</td><td>

Provides advanced case management capabilities to handle key supplier life-cycle events such as onboarding, offboarding, and ongoing operations.

</td><td>

Active

</td><td>

true

</td><td>

-   Supplier Case Management \[com.snc.sn\_supplier\_mgmt\]
-   Document Management \[com.snc.platform\_document\_management\]

</td></tr><tr><td>

Supplier Payment Optimization \[sn\_slm\_opt\] \(Available in the ServiceNow Store\)

</td><td>

View the potential returns or savings when suppliers accept commercial credit card payments and convert high-potential suppliers, and capture value through card-based payments.

</td><td>

Active

</td><td>

true

</td><td>

-   Supplier Operations \[com.snc.sn\_so\]
-   Source-to-Pay Workspace \[com.sn\_spend\_workspace\]
-   Source-to-Pay Common Architecture \[com.snc.sn\_shop\]

</td></tr><tr><td>

Warranty claims \[sn\_repr\_claim\_mgmt\] \(Available in the ServiceNow Store\)

</td><td>

Manage all entities and flows related to Repair Claims within MCO.

</td><td>

Active

</td><td>

true

</td><td>

 

</td></tr><tr><td>

WDF Tokenization \[sn\_wdf\_tokenization\] \(Available in the ServiceNow Store\)

</td><td>

Unifies usage meters from various WDF products, to fuel the consumption of these products.

</td><td>

Inactive

</td><td>

false

</td><td>

 

</td></tr><tr><td>

Workflow Data Fabric Hub \[sn\_data\_fabric\] \(Available in the ServiceNow Store\)

</td><td>

Access Workflow Data Fabric Hub and view data fabric tables on your instance. For the full experience, request the Zero Copy Connectors application \(sn\_data\_fabric\_zcc\). Workflow Data Fabric Hub is automatically activated when the Zero Copy Connectors plugin \(sn\_data\_fabric\_zcc\) is activated on your instance.

</td><td>

Inactive

</td><td>

false

</td><td>

 

</td></tr><tr><td>

Zero Copy Connectors \[sn\_data\_fabric\_zcc\] \(Available in the ServiceNow Store\)

</td><td>

Access data from external sources directly, without copying any data to the instance.

</td><td>

Inactive

</td><td>

false

</td><td>

Workflow Data Fabric Hub \[sn\_data\_fabric\]

</td></tr></tbody>
</table>## Existing plugins

This table lists all plugins that you can activate if you have the admin role.

<table id="table_v_plugins"><thead><tr><th>

Plugin \[ID\]

</th><th>

Description

</th><th>

State

</th><th>

Has Demo Data?

</th><th>

Dependencies

</th></tr></thead><tbody><tr><td>

Advanced Appointment Booking \[com.snc.advanced\_appointment\_booking\]

</td><td>

Enables customers and customer service agents to leverage advanced features like appointment slot recommendation.

</td><td>

Inactive

</td><td>

false

</td><td>

-   Appointment Booking \[com.snc.appointment\_booking\]
-   Resource Matching Engine \[com.snc.matching\_rule\]

</td></tr><tr><td>

Agent Efficiency \[com.snc.agent\_efficiency\]

</td><td>

Allows organizations to define and utilize the efficiency of agents.

</td><td>

Inactive

</td><td>

false

</td><td>

 

</td></tr><tr><td>

AI Search for Notifications \[com.glide.notification.ais\]

</td><td>

Installs AI search for notifications

</td><td>

Inactive

</td><td>

false

</td><td>

-   AI Search \[com.glide.ais\]
-   AI Search Index Source \[com.glide.ais.index\_sources\]

</td></tr><tr><td>

Business Portal \[com.snc.b2b\_portal\] \(Available in the ServiceNow Store\)

</td><td>

Search for information about a question or an issue, or request assistance from a customer service agent.

</td><td>

Inactive

</td><td>

true

</td><td>

 

</td></tr><tr><td>

Care Team Operations for Biomed \[sn\_cto\_biomed\] \(Available in the ServiceNow Store\)

</td><td>

Contains the case types to report and fulfill biomed issues.

</td><td>

Inactive

</td><td>

false

</td><td>

Healthcare Operations Core \[com.sn\_hco\]

</td></tr><tr><td>

Care Team Operations for Healthcare IT \[sn\_cto\_hcit\] \(Available in the ServiceNow Store\)

</td><td>

Contains the case types to report and fulfill healthcare IT issues.

</td><td>

Inactive

</td><td>

false

</td><td>

Healthcare Operations Core \[com.sn\_hco\]

</td></tr><tr><td>

Care Team Portal \[sn\_cto\_sp\] \(Available in the ServiceNow Store\)

</td><td>

Provides a responsive portal experience that can be used by clinicians in the hospitals to report and track issues for support services departments.

</td><td>

Inactive

</td><td>

false

</td><td>

Healthcare Operations Core \[com.sn\_hco\]

</td></tr><tr><td>

Change Management - Standard Change Flows \[com.snc.change\_management.standard\_change\_flows\]

</td><td>

Provides flows for use with Standard Change.

</td><td>

Inactive

</td><td>

false

</td><td>

-   Flow Designer - Installer \[com.glide.hub\]
-   Change Management - Standard Change Catalog \[com.snc.change\_management.standard\_change\_catalog\]

</td></tr><tr><td>

Email Interaction for CSM \[com.sn\_eaai\_csm\]

</td><td>

Email as an interaction for CSM.

</td><td>

Active

</td><td>

true

</td><td>

-   com.sn\_customservice
-   com.glide.messaging.awa
-   sn\_eaai\_core
-   sn\_cwf\_wrkspc
-   sn\_cs\_nb\_action

</td></tr><tr><td>

Credentials Core \[sn\_cred\] \(Available in the ServiceNow Store\)

</td><td>

Stores user achievement credentials \(badges\) data. One of the sources for this data is Credly Spoke.

</td><td>

Inactive

</td><td>

false

</td><td>

 

</td></tr><tr><td>

Credly Spoke \[sn.credly.spoke\] \(Available in the ServiceNow Store\)

</td><td>

Integration to get user credentials data from Credly.

</td><td>

Active

</td><td>

false

</td><td>

 

</td></tr><tr><td>

Data Snapshots \[com.snc.pa.mlb\]

</td><td>

Platform Analytics feature that allows you to capture and maintain historical data. It periodically snapshots the data from a selected platform table or database view, and stores them in a snapshot table for historical trend analysis using Performance Analytics indicators.

</td><td>

Inactive

</td><td>

false

</td><td>

 

</td></tr><tr><td>

Digital Experience Score \[sn\_dex\_score\] \(Available in the ServiceNow Store\)

</td><td>

Enables organizations to effectively measure and improve the overall employee digital experience.

</td><td>

Inactive

</td><td>

false

</td><td>

-   sn\_dex
-   sn\_dex\_feedbck\_sur
-   com.itom.jutils

</td></tr><tr><td>

Field Encryption Enterprise \[com.glide.field.encryption.enterprise\]

</td><td>

Utilizes the Key Management Framework \(KMF\) to enable you to customize and manage how fields and attachments are encrypted and decrypted on your instance.

</td><td>

Inactive

</td><td>

false

</td><td>

Field Encryption Starter \[com.glide.field.encryption.starter\]

</td></tr><tr><td>

Field Encryption Starter \[com.glide.field.encryption.starter\]

</td><td>

Field Encryption Starter

</td><td>

Inactive

</td><td>

false

</td><td>

 

</td></tr><tr><td>

Field Service Agent Efficiency \[com.snc.fsm\_agent\_efficiency\]

</td><td>

Enhances the capabilities of Field Service Management by integrating agent efficiency metrics. This plugin allows field service organizations to define and utilize the efficiency of field service agents to more accurately estimate the work duration for tasks.

</td><td>

Inactive

</td><td>

true

</td><td>

-   Agent Efficiency \[com.snc.agent\_efficiency\]
-   Field Service Management \[com.snc.work\_management\]

</td></tr><tr><td>

Field Service Questionnaires with Smart Assessments \[com.snc.fsm\_smart\_asmt\_questionnaire\] \(Available in the ServiceNow Store\)

</td><td>

Integrates Smart Assessment with Field Service Management \(FSM\) by providing new questionnaires tailored for FSM. It enables the use of Smart Assessment within Field Service.

</td><td>

Inactive

</td><td>

true

</td><td>

-   Field Service Questionnaire
-   Smart Assessment Core
-   Smart Assessment for Mobile

</td></tr><tr><td>

Field Service Task Dependency \[com.snc.fsm\_task\_dependency\]

</td><td>

Enables you to define dependency relationships between work orders.

</td><td>

Inactive

</td><td>

false

</td><td>

Field Service Management \[com.snc.work\_management\]

</td></tr><tr><td>

Forecast planning analysis \[sn\_grc\_forecast\] \(Available in the ServiceNow Store\)

</td><td>

Enables the creation of multiple analysis paths to model future scenarios and adjust specific variables to assess potential changes.

</td><td>

Inactive

</td><td>

false

</td><td>

 

</td></tr><tr><td>

GRC Common Generative AI \[sn\_grc\_genai\] \(Available in the ServiceNow Store\)

</td><td>

Holds common generative AI features that can be used across all GRC product lines

</td><td>

Inactive

</td><td>

false

</td><td>

 

</td></tr><tr><td>

Healthcare Operations Core \[sn\_hco\] \(Available in the ServiceNow Store\)

</td><td>

Provides clinicians a uniform interface to report and track issues related to their day-to-day operations.

</td><td>

Inactive

</td><td>

true

</td><td>

 

</td></tr><tr><td>

HR Multi Instance Integration Base \[sn\_hr\_mii\_base\] \(Available in the ServiceNow Store\)

</td><td>

Contains common configurations and features for multi Instance HRSD enablement on your instance.

</td><td>

Inactive

</td><td>

false

</td><td>

 

</td></tr><tr><td>

HR Multi Instance Integration for Consumer \[sn\_hr\_mii\_consumer\] \(Available in the ServiceNow Store\)

</td><td>

Contains configurations and features for HR services consumer experience in multi Instance HR service fulfillment environment.

</td><td>

Inactive

</td><td>

false

</td><td>

 

</td></tr><tr><td>

HR Multi Instance Integration for Provider \[sn\_hr\_mii\_provider\] \(Available in the ServiceNow Store\)

</td><td>

Contains configurations and features for service provider experience in multi instance HR service fulfillment environment.

</td><td>

Inactive

</td><td>

false

</td><td>

 

</td></tr><tr><td>

Industrial Core \[sn\_ot\_core\] \(Available in the ServiceNow Store\)

</td><td>

Serves as a centralized solution for OT-specific utilities and data model changes.

</td><td>

Active

</td><td>

false

</td><td>

-   CMDB CI Class Models \[com.sn\_cmdb\_ci\_class\]
-   ISA Equipment Model \[com.sn\_isa\_model\]
-   Industrial Workspace Common \[com.sn\_mfg\_common\]

</td></tr><tr><td>

ITSM Enhanced Security Features \[com.snc.itsm.enhanced\_security\]

</td><td>

Loads new enhanced security features for applications part of ITSM suite, read the release notes and documentation to understand the full impact of this plugin.

</td><td>

Inactive

</td><td>

false

</td><td>

 

</td></tr><tr><td>

Interaction Controls Component \[sn\_int\_control\] \(Available in the ServiceNow Store\[var.store-name\]\)

</td><td>

This plugin enables a Contact Center Platform to integrate with the ServiceNow Configurable Workspace. This framework provides a set of native voice call controls.

</td><td>

Active

</td><td>

false

</td><td>

-   Application spoke selector \[sn\_appss\]
-   Contact Center Integration Core \[sn\_ct\_ctr\_it\_core\]
-   External Agent Management Util Pack \[sn\_external\_agent\]
-   OpenFrame \[sn\_openframe\]
-   OpenFrame UXB Component \[sn\_openframe\_uxb\]
-   sn-timer \[sn\_timer\]
-   com.glide.cs.custom.adapter
-   com.glide.hub
-   com.sn\_openframe

</td></tr><tr><td>

Now Assist for IRM \[sn\_irm\_gen\_ai\] \(Available in the ServiceNow Store\)

</td><td>

Provides Gen AI features for IRM, powered by Now Assist.

</td><td>

Inactive

</td><td>

false

</td><td>

 

</td></tr><tr><td>

Now Assist for Process Mining \[com.sn\_now\_assist\_promin\]

</td><td>

Enables Now Assist functionality within Process Mining.

</td><td>

Inactive

</td><td>

false

</td><td>

 

</td></tr><tr><td>

Now Assist for Software Asset Management \[sn\_now\_assist\_sam\] \(Available in the ServiceNow Store\)

</td><td>

GenAI features for SAM.

</td><td>

Inactive

</td><td>

false

</td><td>

 

</td></tr><tr><td>

Now Assist for Workplace Service Delivery \(WSD\) \[sn\_wsd\_gen\_ai\] \(Available in the ServiceNow Store\)

</td><td>

Elevates your Workplace Services experience with generative AI capabilities.

</td><td>

Active

</td><td>

false

</td><td>

sn\_genai\_platform

</td></tr><tr><td>

Now Assist in Virtual Agent Configuration \[com.snc.nowassist\_va\_config\] \(Available in the ServiceNow Store\)

</td><td>

Metadata records for Now Assist in Virtual Agent.

</td><td>

Inactive

</td><td>

false

</td><td>

-   sn\_nowassist\_va
-   sn\_now\_assist\_cr

</td></tr><tr><td>

Post Assessment Actions for Smart Assessments \[sn\_smart\_imp\_auto\] \(Available in the ServiceNow Store\)

</td><td>

Business user definable rules based on assessment response or assessment data based on which any impact/action can be triggered.

</td><td>

Inactive

</td><td>

false

</td><td>

 

</td></tr><tr><td>

Release Management V2 Common \[com.snc.release\_management\_v2\_common\]

</td><td>

Adds entities such as Feature \[rm\_feature\], Release \[rm\_release\], Task \[rm\_task\], and other rules related to these entities

</td><td>

Inactive

</td><td>

true

</td><td>

com.snc.planned\_task\_v2

</td></tr><tr><td>

Response Automation \[sn\_smart\_resp\_auto\] \(Available in the ServiceNow Store\)

</td><td>

Enables to set up default responses for questions so that assessors can complete assessments more quickly

</td><td>

Inactive

</td><td>

false

</td><td>

 

</td></tr><tr><td>

Retail Task Management Core \[sn\_rtmc\] \(Available in the ServiceNow Store\)

</td><td>

Optimize the planning, organizing, and assigning of tasks to staff in your retail environment.

</td><td>

Inactive

</td><td>

false

</td><td>

-   com.sn\_retail\_core
-   com.sn\_multi\_case\_creation

</td></tr><tr><td>

Reusable Impact Framework \[sn\_impact\_fwk\] \(Available in the ServiceNow Store\)

</td><td>

Framework that supports creation of application specific wrapper on workflow action.

</td><td>

Inactive

</td><td>

false

</td><td>

 

</td></tr><tr><td>

Risk Score Calculator \[sn\_risk\_score\_calculator\] \(Available in the ServiceNow Store\)

</td><td>

Provides framework for Risk Score calculation and score storage table.

</td><td>

Inactive

</td><td>

false

</td><td>

 

</td></tr><tr><td>

Service Graph Connector for NOKIA Altiplano \[sn\_tsom\_altiplano\_connector\] \(Available in the ServiceNow Store\)

</td><td>

Integrates with Nokia NSP network management system \(NMS\).

</td><td>

Inactive

</td><td>

true

</td><td>

sn\_tsom\_core

</td></tr><tr><td>

Service Observability \[com.service\_observability\_app\] \(Available in the ServiceNow Store\)

</td><td>

Enables operations teams to effectively triage and manage incidents in a complex and distributed production system by combining telemetry and platform insights from multiple observability tools in a cohesive and centralized workflow.

</td><td>

Inactive

</td><td>

false

</td><td>

Service Reliability Management

</td></tr><tr><td>

Smart Assessment Mobile \[com.snc.smart\_assessment\_mobile\] \(Available in the ServiceNow Store\)

</td><td>

Offers common mobile functionalities for Smart Assessment. It includes shared mobile capabilities that can be utilized across various Smart Assessment applications.

</td><td>

Inactive

</td><td>

true

</td><td>

Field Service Questionnaire Smart Assessment Core

</td></tr><tr><td>

Smart Assessment Scoring \[sn\_smart\_scoring\] \(Available in the ServiceNow Store\)

</td><td>

Enables scoring for smart assessments.

</td><td>

Inactive

</td><td>

false

</td><td>

 

</td></tr><tr><td>

Workforce Optimization for CSM Configurable Workspace \[sn\_csm\_wfo\_workspa\] \(Available in the ServiceNow Store\)

</td><td>

Manages configurable workspace configurations for WFO modules.

</td><td>

Active

</td><td>

true

</td><td>

-   com.snc.skills\_management
-   com.snc.sre
-   com.snc.pa.customer\_service
-   sn\_wfo\_cfg\_ws
-   sn\_wfo\_work\_sched
-   sn\_uib\_agent\_sp
-   sn\_shift\_planning
-   sn\_coach\_lrn
-   sn\_agent\_forecast
-   sn\_channel\_mgmt
-   sn\_team\_perf
-   sn\_coaching
-   sn\_wfo\_outlook

</td></tr><tr><td>

SuccessFactors Learning Spoke \[sn.successfactorslrn.spk\] \(Available in the ServiceNow Store\)

</td><td>

Provides actions that a Process Analyst can use when designing flows. The actions allow them to automate SuccessFactors Learning.

</td><td>

Inactive

</td><td>

false

</td><td>

 

</td></tr><tr><td>

Synthetic Monitoring \[com.snc.uib.sow\_synthetics\] \(Available in the ServiceNow Store\)

</td><td>

Empowers organizations to proactively manage and enhance the performance and availability of critical services.

</td><td>

Inactive

</td><td>

false

</td><td>

-   Agent Client Collector - Framework \(ACC-F\) Event Management
-   Service Mapping Core Event Management

</td></tr><tr><td>

Telecom Discovery Patterns \[sn\_tsom\_patterns\] \(Available in the ServiceNow Store\)

</td><td>

Defines discovery patterns created specifically for telcom to handle deep discovery of the network elements.

</td><td>

Inactive

</td><td>

true

</td><td>

sn\_tsom\_core

</td></tr><tr><td>

Zero Trust - Continuous Authentication \[com.snc.zero\_trust\_continuous\_authentication\]

</td><td>

Enables security administrators to define security policies that require step-up authentication or reauthentication within a logged-in session, based on the data the user is accessing and the activities they’re performing.

</td><td>

Inactive

</td><td>

false

</td><td>

 

</td></tr><tr><td>

Project Advanced Security \[com.snc.project\_advanced\_security\]

</td><td>

Allows project managers to enhance security by enabling access controls and confidentiality settings, selectively restricting user access to sensitive projects.

</td><td>

Inactive

</td><td>

false

</td><td>

 

</td></tr><tr><td>

Tableau Spoke \[com.sn.tableau.spoke\] \(Available in the ServiceNow Store\)

</td><td>

Provides actions to view and analyze meaningful usage data for Tableau Cloud software subscriptions so that you can reclaim stale licenses.

</td><td>

Inactive

</td><td>

false

</td><td>

 

</td></tr><tr><td>

Enterprise Modeling and Visualization \[com.snc.apm\_modelling\_tool\] \(Available in the ServiceNow Store\)

</td><td>

Provides diagramming and modeling capabilities. It enables Enterprise Architects to model the future state of their IT business applications to assess the impact of proposed business application changes, evaluate different scenarios, and identify potential risks before implementing application strategies.

</td><td>

Inactive

</td><td>

true

</td><td>

 

</td></tr><tr><td>

APM Modelling tool Common \[com.snc.apm\_modelling\_tool\_common\] \(Available in the ServiceNow Store\)

</td><td>

Provides Base Data Model and API and UI Pages for Modelling Tools.

</td><td>

Inactive

</td><td>

false

</td><td>

Enterprise Modeling and Visualization \[com.snc.apm\_modelling\_tool\]

</td></tr><tr><td>

Field Service Work Types \[com.snc.fsm\_work\_types\] \(New in Xanadu\)

</td><td>

Enables customers to set up different work configurations for field service workflows as need by a business unit or department.

</td><td>

Inactive

</td><td>

true

</td><td>

Field Service Management \[com.snc.work\_management\]

</td></tr><tr><td>

ITSM Notifications Redirection \[com.snc.itsm.notifications\_redirection\] \(New in Xanadu\)

</td><td>

Provides notification redirection functionality to either SOW or UI16 based on user role for Incident, problem, change and request records.

</td><td>

Active

</td><td>

false

</td><td>

 

</td></tr><tr><td>

Problem - Models \[com.snc.problem.problem\_model\] \(New in Xanadu\)

</td><td>

Introduces support for problem and problem task models, allowing different models to be defined using the model reference field.

</td><td>

Active

</td><td>

false

</td><td>

 

</td></tr><tr><td>

ITSM Analytics \[com.snc.sn\_itsm\_analytics\] \(New in Xanadu\)

</td><td>

The ITSM Dashboards content pack provides several Platform Analytics Solutions that contain preconfigured dashboards.

</td><td>

Active

</td><td>

true

</td><td>

Success Dashboard

</td></tr><tr><td>

SPM Agile Common \[com.snc.spm\_agile\_common\] \(New in Xanadu\)

</td><td>

The SPM Agile Common plugin adds Agile entities such as Story \[rm\_story\], Story dependencies \[m2m\_story\_dependencies\], Scrum task \[rm\_scrum\_task\], and other rules related to Story \[rm\_story\].

</td><td>

Active

</td><td>

false

</td><td>

com.snc.sdlc.ranking, com.snc.release\_management\_v2

</td></tr><tr><td>

sn-apm-diagram-builder \[com.sn\_apm\_diagram\_builder\] \(Available in the ServiceNow Store\)

</td><td>

Component for Enterprise Modeling and Visualization \[com.snc.apm\_modelling\_tool\].

</td><td>

Inactive

</td><td>

false

</td><td>

Enterprise Modeling and Visualization \[com.snc.apm\_modelling\_tool\]

</td></tr><tr><td>

Scope 3 emissions management \[com.sn\_esg\_scope3\] \(Available in the ServiceNow Store\)

</td><td>

The Scope 3 dashboard helps you to calculate and track scope 3 emissions to gain a full understanding of your organization's environmental impact and ensure compliance with evolving regulations. Scope 3 emissions refer to indirect emissions in your value chain, for example, the emissions generated from procurement of equipment.

</td><td>

Inactive

</td><td>

true

</td><td>

sn\_esg

</td></tr><tr><td>

Field Service Quality Management \[com.sn\_fsm\_quality\] \(New in Xanadu\)

</td><td>

Allows for the review of tasks closed by field technicians to ensure quality and guidance.

</td><td>

Inactive

</td><td>

true

</td><td>

Field Service Management \[com.snc.work\_management\]

</td></tr><tr><td>

Field Service Mobile Sidebar \[com.sn\_fsm\_sidebar\] \(Available in the ServiceNow Store\)

</td><td>

Provide agents with sidebar collaboration on mobile to enable an in-app experience for chatting and collaborating with team members while preserving important information for future reference and historical context.

</td><td>

Inactive

</td><td>

false

</td><td>

-   Work Order Management \[com.snc.work\_management\]
-   Field Service Mobile \[com.sn\_fsm\_mobile\]
-   Omni-Experience Standard Feature Set \[sn-oe-sfs : 5.2.7\]

</td></tr><tr><td>

Software Asset Management integration with Tableau \[com.sn\_sam\_tableau\] \(Available in the ServiceNow Store\)

</td><td>

Enables you to track your Tableau Cloud software subscriptions and to reclaim stale licenses.

</td><td>

Inactive

</td><td>

false

</td><td>

Software Asset Management - SaaS License Management

</td></tr><tr><td>

Multi-Instance Framework - Client \[sn\_mif\] \(New in Xanadu\)

</td><td>

Enables communication between instances for applications.

</td><td>

Active

</td><td>

false

</td><td>

com.glide.kaa, com.glide.services

</td></tr><tr><td>

Dispute Content Pack for US Regulations \[sn\_disp\_reg\_cp\_us\] \(Available in the ServiceNow Store\)

</td><td>

Ensure compliance and protect cardholder interests with the Dispute Content Pack for US Regulations application, which helps U.S.-based issuers manage dispute cases effectively by providing access to regulatory SLA due dates.

</td><td>

Inactive

</td><td>

false

</td><td>

Financial Services Card Operation \[com.sn\_bom\_credit\_card\]

</td></tr><tr><td>

Verifi Spoke \[sn\_verifi\_spoke\] \(Available in the ServiceNow Store\)

</td><td>

Streamlines dispute management processes with the Verifi Spoke application, enabling financial institutions to utilize Verifi CDRN APIs for creating, managing, and retrieving case details efficiently.

</td><td>

Inactive

</td><td>

false

</td><td>

No

</td></tr><tr><td>

Now Assist for Financial Services Operations \(FSO\) \[sn\_fso\_gen\_ai\] \(Available in the ServiceNow Store\)

</td><td>

Summarize case information for insurance claims and card disputes.

</td><td>

Inactive

</td><td>

false

</td><td>

Now Assist for Platform

</td></tr><tr><td>

Individual Life Claims \[sn\_ins\_claim\_indl\] \(Available in the ServiceNow Store\)

</td><td>

Set up and manage the various stages of the individual life claim process, starting from first notice of loss to claim closure.

</td><td>

Inactive

</td><td>

true

</td><td>

Financial Services Operations Core, CSM Contributor User, CSM Playbook

</td></tr><tr><td>

Dispute Rules Content Pack for Mastercard \[sn\_bom\_mcard\_cp\] \(Available in the ServiceNow Store\)

</td><td>

Provides questionnaires for the intake of card dispute-related information under various dispute categories as per Mastercard guidelines.

</td><td>

Inactive

</td><td>

false

</td><td>

Financial Services Operations Core, Dispute Content Pack for Visa

</td></tr><tr><td>

Sales Agreement Management \[com.sn\_sales\_agmt\_wf\] \(Available in the ServiceNow Store\)

</td><td>

Provides workflows to create and manage sales agreements.

</td><td>

Inactive

</td><td>

true

</td><td>

Product Catalog Mgmt Core \[com.sn\_prd\_pm\],​ Price Management \[com.sn\_csm\_pricing\]

</td></tr><tr><td>

Workplace Services Kiosk \[sn\_wsd\_kiosk\] \(Available in the ServiceNow Store\)

</td><td>

Provide a customizable kiosk experience for workplace service delivery.

</td><td>

Inactive

</td><td>

true

</td><td>

Workplace Core \[sn\_wsd\_core\]

</td></tr><tr><td>

Smart Assessment Core plugin \[com.sn\_smart\_asmt\] \(Available in the ServiceNow Store\)

</td><td>

The Assessment Core is the fundamental plugin of the Smart Assessment Engine. This plugin contains all the essential components, and the plugins 'Smart Assessment Connected' and 'Smart Assessment Builder' are dependent on the core and get installed automatically when the core is installed.

</td><td>

Inactive

</td><td>

false

</td><td>

 

</td></tr><tr><td>

Smart Assessment Designer plugin \[com.sn\_smart\_asmt\_desg\] \(Available in the ServiceNow Store\)

</td><td>

Connected component for assessment designer.

</td><td>

Inactive

</td><td>

false

</td><td>

Smart Assessment Core \[com.sn\_smart\_asmt\]

</td></tr><tr><td>

Smart Assessment Migration Tools plugin \[com.sn\_smart\_asmt\_mig\] \(Available in the ServiceNow Store\)

</td><td>

The migration utility facilitates the transfer of an existing Metric type from the current ITSM assessments to a new template in draft state within the Smart Assessment Engine. Users can then verify and publish the newly migrated template. In this context, migrate refers to copying, so the original metric type remains unchanged.

</td><td>

Inactive

</td><td>

false

</td><td>

Smart Assessment Core \[com.sn\_smart\_asmt\]

</td></tr><tr><td>

Smart Assessment Connected plugin \[com.sn\_smart\_asmt\_connect\] \(Available in the ServiceNow Store\)

</td><td>

Connected component for assessment instance.

</td><td>

Inactive

</td><td>

false

</td><td>

Smart Assessment Core \[com.sn\_smart\_asmt\]

</td></tr><tr><td>

Smart Assessment Dependencies plugin \[com.sn\_smart\_asmt\_dep\] \(Available in the ServiceNow Store\)

</td><td>

The Smart Assessment Dependencies plugin includes utilities designed for use by the smart assessment engine.

</td><td>

Inactive

</td><td>

false

</td><td>

 

</td></tr><tr><td>

Regulatory Agency Library \[com.sn\_reg\_body\_mgmt\] \(Available in the ServiceNow Store\)

</td><td>

The Regulatory Agency Library application establishes a centralized library for identifying relevant regulatory authorities, responsible for overseeing specific industries or sectors within each jurisdiction, consolidating all regulatory communications via emails and implementing notification rules for data privacy/security breaches for the reported compliance cases. Lastly, stay informed about emerging regulatory trends, changes, and requirements that could impact business operations.

</td><td>

Inactive

</td><td>

true

</td><td>

GRC: Taxonomy Management \[com.sn\_grc\_taxonomy\]

</td></tr><tr><td>

ServiceNow IDE \[com.sn\_glider\] \(Available in the ServiceNow Store\)

</td><td>

The ServiceNow integrated development environment \(IDE\) application enables developers to create scoped applications in source code in an IDE based on Visual Studio Code for the Web on the ServiceNow AI Platform.

</td><td>

Active

</td><td>

false

</td><td>

 

</td></tr><tr><td>

Email Address Internationalization \[com.glide.email\_address\_internationalization\] \(New in Xanadu\)

</td><td>

The plugin contains the artifacts required for email address internationalization feature.

</td><td>

Inactive

</td><td>

false

</td><td>

 

</td></tr><tr><td>

Sensitive Data Redaction for Inbound Emails \[com.glide.email\_inbound.redaction\] \(New in Xanadu\)

</td><td>

Enables sensitive data redaction from inbound emails. Post installation, the default behavior is to redact sensitive data for records created in sys\_email \(Subject, Body, and Body Text fields\) table from the new inbound emails. As a pre-requisite, Install Store App - Data Discovery \(com.snc.data\_discovery\) for this plugin to work seamlessly.

</td><td>

Inactive

</td><td>

true

</td><td>

Data Privacy \(Classic\) \[com.glide.data\_privacy\], System Mailboxes \[com.glide.mailbox\]

</td></tr><tr><td>

Retail Operations Core \[com.sn\_retail\] \(Available in the ServiceNow Store\)

</td><td>

This plugin empowers frontline store managers, associates, and regional managers with proactive store operations tools, optimizing task management and enhancing visibility into store operations and performance.

</td><td>

Inactive

</td><td>

true

</td><td>

com.sn\_customerservice, com.snc.business\_location, com.snc.csm\_fsm\_integration

</td></tr><tr><td>

API Key and HMAC Authentication \[com.glide.tokenbased\_auth\] \(New in Washington DC\)

</td><td>

Support API tokens for REST API endpoints. Enable API key-based authentication to securely authenticate inbound webhook URL.

</td><td>

Active

</td><td>

false

</td><td>

-   com.glide.auth.scope
-   com.glide.rest.policy
-   com.glide.rest.auth.scope

</td></tr><tr><td>

Asset Warranty - Lenovo \[com.sn\_warranty\_integration\_lenovo\] \(Available in the ServiceNow Store\)

</td><td>

Get the warranty information of hardware assets by connecting to the Lenovo Warranty API.

</td><td>

Inactive

</td><td>

false

</td><td>

-   sn\_hamp
-   sn\_lenovo\_spoke

</td></tr><tr><td>

Capacity management \[sn\_cap\_mgmt\] \(Available in the ServiceNow Store\)

</td><td>

Enables an inventory user to view and action on the utilization of a resource. Any resource consumption will be tracked and provides a mechanism to trigger further inventory request based on capacity constraints defined.

</td><td>

Active

</td><td>

true

</td><td>

None

</td></tr><tr><td>

Contracts and Entitlement Workflows \[com.sn\_contract\_ent\_wf\] \(Available in the ServiceNow Store\)

</td><td>

Provides workflows to manage changes on Customer contracts and entitlements.

</td><td>

Active

</td><td>

true

</td><td>

-   Customer Contracts and Entitlements Foundation \[com.com.sn\_pss\_core\]​
-   Lead to Cash Primitives \[com.sn\_l2c\_core\]
-   Customer Life Cycle Management Workflows \[com.sn\_l2c\_cust\_flows\]​

</td></tr><tr><td>

Customer Contracts and Entitlements​ \[com.sn\_pss\_core\] \(Available in the ServiceNow Store\)

</td><td>

Provides foundational objects to manage customer contracts and entitlements.

</td><td>

Active

</td><td>

true

</td><td>

-   Customer Service Install Base Management \[com.snc.install\_base\]​
-   Product Catalog Management Core \[com.sn.prd\_pm\]

</td></tr><tr><td>

Customer Life Cycle Management Workflows \[com.snc.customer\_lifecycle\_mgmt\_workflows\] \(Available in the ServiceNow Store\)

</td><td>

Provides workflows to manage the life cycle of Sold Products to manage its configuration, suspend, resume and disconnect the sold product to meet customer’s business needs.

</td><td>

Inactive

</td><td>

true

</td><td>

-   Customer Service Install Base Management \[com.snc.install\_base\]
-   Product Catalog Management Core \[com.sn\_prd\_pm\]
-   Lead to Cash Core \[com.snc.l2c\_core\]

</td></tr><tr><td>

Desktop Assistant \[sn\_dex\_desktop\] \(Available in the ServiceNow Store\)

</td><td>

Establishes a continuous communication channel for employees, enabling them to easily access self-service options and receive timely notifications from the Service Desk. This effectively minimizes any barriers to employee productivity.

</td><td>

Inactive

</td><td>

true

</td><td>

com.snc.itom.license

</td></tr><tr><td>

DevOps Vulnerability Integrations \[sn\_devops\_vul\_ints \(Available in the ServiceNow Store\)

</td><td>

Provides speed time-to-market and an organization-wide view of risk exposure for application vulnerabilities.

</td><td>

Inactive

</td><td>

false

</td><td>

-   com.snc.ihub\_spoke\_util\_pack
-   com.glide.hub.usage.dashboard
-   com.glide.script.vtable
-   com.snc.security\_support.core
-   com.glide.hub.action\_step.rest
-   com.glide.hub.action\_type.datastream
-   com.glide.hub.integration.runtime
-   com.snc.vul\_dep

</td></tr><tr><td>

DEX Content Playbook \[sn\_dex\_content\] \(Available in the ServiceNow Store\)

</td><td>

Provides the content to assist with monitoring applications and devices, as well as offer support for remediating identified experience issues.

</td><td>

Inactive

</td><td>

true

</td><td>

sn\_dex \(scoped app\)

</td></tr><tr><td>

Digital End-User Experience \[sn\_dex\] \(Available in the ServiceNow Store\)

</td><td>

Monitors applications, networks, and devices in order to detect issues before they result in downtime and reduce employee productivity.

</td><td>

Inactive

</td><td>

true

</td><td>

-   com.sn\_acc\_visibility com.snc.clotho
-   com.glide.fenix com.sn\_itom\_cloud\_svc
-   com.glideapp.itom.snac com.snc.itom.license

</td></tr><tr><td>

Digital Product Release \[com.sn\_dpr\] \(Available in the ServiceNow Store\)

</td><td>

A dedicated release management solution designed to deliver a personalized experience for software-based release practices. Empowering central release management teams, it facilitates the definition of release policies, templates, and readiness dates.

</td><td>

Inactive

</td><td>

true

</td><td>

-   sn\_dpr\_model
-   sn\_dpr\_workspace
-   sn\_cmdb\_ci\_class
-   sn\_pace
-   sn\_pace\_builder
-   sn\_roadmap
-   sn\_playbook\_exp
-   now\_playbook\_exp
-   sn\_devops, sn\_devops\_ws

</td></tr><tr><td>

Digital Product Release Data Model \[sn\_dpr\_model\] \(Available in the ServiceNow Store\)

</td><td>

The data model for Digital Product Release. It defines the tables and relationships for release management.

</td><td>

Inactive

</td><td>

false

</td><td>

com.snc.sdlc.ranking

</td></tr><tr><td>

Digital Product Release Policy Content Pack \[sn\_dpr\_content\] \(Available in the ServiceNow Store\)

</td><td>

Automates and streamlines comprehensive verifications for your release process. Utilize Data Collectors and Policies aligned with the DevOps Data Model for efficient assessments of engineering completion, quality checks, and release readiness.

</td><td>

Inactive

</td><td>

false

</td><td>

None

</td></tr><tr><td>

Digital Product Release Workspace \[sn\_dpr\_workspace\] \(Available in the ServiceNow Store\)

</td><td>

Manage your Digital Products, Product Features and plan Versions for software release execution. The app provides capabilities required to support release execution using Digital Product Release.

</td><td>

Inactive

</td><td>

false

</td><td>

-   com.devsnc\_sn\_vtb
-   sn\_datagrid
-   sn\_dpr\_model

</td></tr><tr><td>

Dispute Rules Content Pack for Visa \[com.sn\_bom\_visa\_cp\] \(Available in the ServiceNow Store\)

</td><td>

Allows issuers to easily access card network rules for initiating and investigating card dispute cases.

</td><td>

Active

</td><td>

false

</td><td>

-   com.sn\_ga\_exp
-   com.sn\_bom\_credit\_card

</td></tr><tr><td>

Document Template integration with Digital Signatures using Smart Cards \[com.sn.dt-digital-signature-smart-card-integration\] \(Available in the ServiceNow Store\)

</td><td>

Enables workflows for digital signing using smart cards \(CAC/PIV cards\) by generating and sending auto-filled documents to be signed by different participants.

</td><td>

Inactive

</td><td>

false

</td><td>

-   com.snc.platform\_document\_management
-   com.glide.auth.mutual
-   com.snc.document\_templates

</td></tr><tr><td>

Talent Development Opportunity Marketplace \[com.sn\_egd\_opp\_market\] \(Available in the ServiceNow Store\)

</td><td>

Provides a single, unified place where organizations share opportunities that are easily discoverable by employees.

</td><td>

Active

</td><td>

true

</td><td>

None

</td></tr><tr><td>

Email - Bounce management \[com.glide.email.bounce\_management\] \(New in Washington DC\)

</td><td>

Enables the bounce management capability to help identify and prevent sending emails to addresses that are known to generate bounces by filtering them out while sending emails.

</td><td>

Active

</td><td>

false

</td><td>

com.glide.mailbox

</td></tr><tr><td>

Enterprise Asset Management for Healthcare \[com.sn\_eamhc\] \(Available in the ServiceNow Store\)

</td><td>

Provides Enterprise Asset Management functionality targeted towards healthcare-specific roles to manage healthcare-specific models and assets and related workflows.

</td><td>

Inactive

</td><td>

true

</td><td>

-   com.sn\_eam\_core
-   com.snc.procurement
-   com.sn\_itam\_recomm
-   com.snc.asset\_management
-   sn\_cmdb\_ci\_class
-   com.sn\_itam\_common
-   com.sn\_ent
-   com.sn\_risk\_heatmap
-   com.sn\_eam

</td></tr><tr><td>

Entitlement Verification \[com.sn\_ent\_verify\] \(Available in the ServiceNow Store\)

</td><td>

Provides APIs to verify Entitlements and characteristics​.

</td><td>

Active

</td><td>

true

</td><td>

Customer Contracts and Entitlements \[com.com.sn\_pss\_core\]​

</td></tr><tr><td>

Field Service Marketplace \[com.snc.fsm\_marketplace\] \(New in Washington DC\)

</td><td>

Push tasks to multiple eligible resources to get work done within stipulated time period and at a better cost.

</td><td>

Active

</td><td>

true

</td><td>

com.snc.marketplace\_core

</td></tr><tr><td>

Financial Services Operations Integration with Visa \[com.sn\_fso\_intg\_visa\] \(Available in the ServiceNow Store\)

</td><td>

Enables financial institutions to integrate with Visa Resolve Online \(VROL\) APIs using the Visa Spoke Actions to manage various dispute lifecycle events.

</td><td>

Active

</td><td>

false

</td><td>

-   com.sn\_visa\_spoke
-   com.sn\_bom\_visa\_cp

</td></tr><tr><td>

Flow Designer Proactive Analytics Trigger \[com.glide.hub.flow\_trigger.analytics\] \(New in Washington DC\)

</td><td>

Starts a flow when Proactive Analytics KPI score or KPI threshold values are met.

</td><td>

Active

</td><td>

false

</td><td>

-   com.glide.hub.flow\_trigger
-   com.snc.par.intelligence

</td></tr><tr><td>

GraphQL Explorer \[com.glide.graphql.explorer\] \(New in Washington DC\)

</td><td>

An integrated GraphQL testing tool.

</td><td>

Active

</td><td>

false

</td><td>

None

</td></tr><tr><td>

GRC: Management Reporting \[com.sn\_grc\_mgmt\_report\] \(Available in the ServiceNow Store\)

</td><td>

Provides the Reporting capabilities for importing GRC related data to Microsoft word document using Microsoft Office 365 plugin.

</td><td>

Inactive

</td><td>

false

</td><td>

com.sn\_esg\_msoff\_intg

</td></tr><tr><td>

Hardware Asset Management for TNI \[com.sn\_ham\_tni\] \(Available in the ServiceNow Store\)

</td><td>

Use only the Telecommunication Network Inventory \(TNI\) functionality with Hardware Asset Management \(HAM\).

</td><td>

Inactive

</td><td>

false

</td><td>

san\_hamp

</td></tr><tr><td>

Hardware Asset Management integration with Zero Touch Mobility \[com.sn\_ham\_ztm\] \(Available in the ServiceNow Store\)

</td><td>

Drive automation and prescriptive, standard practices for managing Mobile Device class assets throughout the end-to-end asset lifecycle from acquisition through disposition.

</td><td>

Inactive

</td><td>

false

</td><td>

sn\_hamp

</td></tr><tr><td>

Health and Safety Risk Management \[com.snc.sn\_hs\_rm\] \(Available in the ServiceNow Store\)

</td><td>

Identify, assess, and reduce potential hazards, prioritizing safety at workplace.

</td><td>

Active

</td><td>

true

</td><td>

None

</td></tr><tr><td>

Health log analytics prime \[com.sn\_hla\_gw\_stream\] \(Available in the ServiceNow Store\)

</td><td>

Enables transitioning to a regional data center.

</td><td>

Active

</td><td>

false

</td><td>

None

</td></tr><tr><td>

Hiring Core \[com.sn\_ta\_hiring\_core\] \(Available in the ServiceNow Store\)

</td><td>

Record tables to store third party platform data on the ServiceNow AI Platform.

</td><td>

Active

</td><td>

false

</td><td>

None

</td></tr><tr><td>

IPKI Certificate Generator \[com.sn\_app\_skytale\] \(New in Washington DC\)

</td><td>

Secure your Kafka topics by generating an instance-signed certificate.

</td><td>

Inactive

</td><td>

false

</td><td>

com.glide.uxbuilder

</td></tr><tr><td>

ITOM Content Service \[sn\_smart\_content\] \(Available in the ServiceNow Store\)

</td><td>

Offers extensive visibility of products in your infrastructure. The classification of processes identified by Predictive Intelligence enables wider discovery and weekly updates of new configuration items in the CMDB.

</td><td>

Inactive

</td><td>

false

</td><td>

-   Discovery \[com.snc.discovery\]
-   Normalization Data Services Client \[com.glide.data\_services\_canonicalization.client\]

</td></tr><tr><td>

I18N: Arabic Translations \[com.snc.i18n.arabic\] \(New in Washington DC\)

</td><td>

Provides Arabic translations of the base system UI string content in your instance.

</td><td>

Inactive

</td><td>

false

</td><td>

-   I18N: Internationalization \[com.glide.i18n\]
-   Localization Framework Installer \[com.glide.localization\_framework.installer\]
-   18N: Knowledge Management Internationalization Plugin v2 \[com.glideapp.knowledge.i18n2\]

</td></tr><tr><td>

JavaScript Module Support \[com.glide.module\_support\] \(New in Washington DC\)

</td><td>

Contains the schema for storing JavaScript modules in a file system structure.

</td><td>

Active

</td><td>

false

</td><td>

None

</td></tr><tr><td>

Localization Framework Hub \[com.sn.localization\_framework.hub\] \(New in Washington DC\)

</td><td>

Enables fulfilling the translation requests received from Localization Framework Spoke.

</td><td>

Inactive

</td><td>

false

</td><td>

com.glide.localization\_framework.installer

</td></tr><tr><td>

Localization Framework Spoke \[com.sn.localization\_framework.spoke\] \(New in Washington DC\)

</td><td>

Enable fulfilling translation requests using Localization Framework Hub.

</td><td>

Inactive

</td><td>

false

</td><td>

com.glide.localization\_framework.installer

</td></tr><tr><td>

Mentoring \[sn\_ecn\] \(Available in the ServiceNow Store\)

</td><td>

Employee Connections offers improved networking opportunities and enables individuals to forge meaningful connections. It equips employees with tools such as Mentoring, facilitating the search for guidance and suitable mentors to expedite their learning and amplify their potential for career advancement.

</td><td>

Inactive

</td><td>

true

</td><td>

Career Conversations

</td></tr><tr><td>

Mobile Gen AI \[com.glide.sg.gen\_ai\] \(New in Washington DC\)

</td><td>

Allows mobile to enable and integrate with generative AI capabilities.

</td><td>

Active

</td><td>

false

</td><td>

-   com.glide.one\_extend
-   com.glide.sg.one\_extend

</td></tr><tr><td>

Opportunity Management Application \[sn\_l2c\_oppty\_mgmt\] \(Available in the ServiceNow Store\)

</td><td>

Gives access to opportunity to Quote workflow and Kanban view.

</td><td>

Inactive

</td><td>

true

</td><td>

-   com.sn\_l2c\_oppty\_mgmt\_data\_model
-   com.snc.l2c\_core

</td></tr><tr><td>

Opportunity Management Data Model \[sn\_l2c\_oppty\_mgmt\_data\_model\] \(Available in the ServiceNow Store\)

</td><td>

Allows users to manage opportunities. It includes the Opportunity Data Model and the ability to create and manage new sales opportunities, as well as workflows to convert opportunities to quotes.

</td><td>

Inactive

</td><td>

true

</td><td>

-   com.sn\_customerservice
-   com.sn\_prd\_pm
-   com.sn\_l2c\_sales\_common

</td></tr><tr><td>

Opportunity Marketplace \[sn\_opp\_market\] \(Available in the ServiceNow Store\)

</td><td>

Improve employee engagement and retention with internal mobility.

</td><td>

Inactive

</td><td>

true

</td><td>

-   Talent Development Core
-   Talent Development Shared library
-   Hiring Core

</td></tr><tr><td>

Parallel Review and Feedback \[sn\_rvw\_feedback\] \(Available in the ServiceNow Store\)

</td><td>

Contains the basic workflow of raising a feedback and responding to feedback.

</td><td>

Inactive

</td><td>

true

</td><td>

None

</td></tr><tr><td>

Participant Suggestions \[com.glide.sn\_participant\_suggestions\] \(Available in the ServiceNow Store\)

</td><td>

Displays a list of users \(or participants\) who may be able to contribute to a Sidebar discussion.

</td><td>

Inactive

</td><td>

false

</td><td>

-   com.glide.one\_extend
-   com.glide.platform\_ml

</td></tr><tr><td>

Product Configurator \[sn\_prd\_config\_ui\] \(Available in the ServiceNow Store\)

</td><td>

Enables companies to configure products and services they market, sell, and deliver to customers.

</td><td>

Inactive

</td><td>

false

</td><td>

Product Catalog Management Core \[com.sn\_prd\_pm\]

</td></tr><tr><td>

Quote Management Application \[sn\_l2c\_quote\_mgmt\] \(Available in the ServiceNow Store\)

</td><td>

Used to create and manage product quotes

</td><td>

Inactive

</td><td>

true

</td><td>

-   com.sn\_l2c\_quote\_mgmt\_data\_model
-   com.sn\_l2c\_core

</td></tr><tr><td>

Quote Management Data Model \[sn\_l2c\_quote\_mgmt\_data\_model\] \(Available in the ServiceNow Store\)

</td><td>

Allows users to manage the quotation process.

</td><td>

Inactive

</td><td>

true

</td><td>

-   com.sn\_customerservice
-   com.sn\_prd\_pm
-   com.sn.csm\_pricing
-   com.sn\_l2c\_sales\_common

</td></tr><tr><td>

Rack visualization component \[sn\_rack\] \(Available in the ServiceNow Store\)

</td><td>

Capability to visualise the Rack and the equipment positioning inside the Rack. Enhances the capacity visualisation of Rack.

</td><td>

Active

</td><td>

true

</td><td>

None

</td></tr><tr><td>

ServiceNow Stream Connect Replication - Kafka \[com.glide.hub.stream\_connect.replication.kafka\] \(New in Washington DC\)

</td><td>

Enables support for replicating Stream Connect topics, via a MID Server, with a customer Kafka cluster.

</td><td>

Inactive

</td><td>

false

</td><td>

-   ServiceNow Stream Connect Replication Core \[com.glide.hub.stream\_connect.replication.core\]
-   Stream Connect Replication Certification \[com.sn\_stream\_connect.replication.cert\]

</td></tr><tr><td>

Site Mapping for Field Service Management \[com.snc.fsm\_site\_mapping\] \(Available in the ServiceNow Store\)

</td><td>

Navigate using wayfinding features and site maps within a native mobile application.

</td><td>

Active

</td><td>

false

</td><td>

-   com.snc.work\_management, sn\_map\_core
-   sn\_map\_component

</td></tr><tr><td>

Skills Industry Data \[com.sn\_skills\_data\] \(Available in the ServiceNow Store\)

</td><td>

Get industry skills data.

</td><td>

Active

</td><td>

true

</td><td>

Skills Intelligence plugin

</td></tr><tr><td>

Skills Intelligence Workspace \[com.sn\_skills\_int\_ws\] \(Available in the ServiceNow Store\)

</td><td>

A skills intelligence workspace experience.

</td><td>

Active

</td><td>

true

</td><td>

Skills Intelligence plugin

</td></tr><tr><td>

Sn Topology Map \[sn\_topology\_map\] \(Available in the ServiceNow Store\)

</td><td>

Enables an inventory manager to capture and visualise a topology along with its elements.

</td><td>

Active

</td><td>

true

</td><td>

None

</td></tr><tr><td>

sn-4q-bubble \[com.sn\_4\_q\_bubble\] \(Available in the ServiceNow Store\)

</td><td>

Application Portfolio Management bubble charts enables plotting indicator scores of your business applications. Strategize goals using these scores and create demands for your business applications.

</td><td>

Active

</td><td>

false

</td><td>

None

</td></tr><tr><td>

sn\_supplier\_tprm \[sn\_supplier\_tprm\] \(Available in the ServiceNow Store\)

</td><td>

Enables Supplier Managers to trigger risk assessments from onboarding workflows as well as allows risk data to be viewed and used within Supplier Lifecycle Operations.

</td><td>

Inactive

</td><td>

false

</td><td>

-   Supplier Lifecycle Operations \[com.snc.sn\_supplier\_mgmt\]
-   Third-party Risk Management \[com.sn\_vdr\_risk\_asmt\]

</td></tr><tr><td>

Strategic Portfolio Management for Telecom \[sn\_strg\_prtf\_mgmt\] \(Available in the ServiceNow Store\)

</td><td>

Telecom Project templates.

</td><td>

Inactive

</td><td>

true

</td><td>

None

</td></tr><tr><td>

Total Cost of Ownership \[sn\_apm\_tco\] \(Available in the ServiceNow Store\)

</td><td>

Helps enterprise architects to prioritize application portfolio by leveraging the application costs.

</td><td>

Active

</td><td>

true

</td><td>

None

</td></tr><tr><td>

Visa Spoke \[com.sn\_visa\_spoke\] \(Available in the ServiceNow Store\)

</td><td>

The Visa spoke allows connecting with Visa's REST APIs, providing customers quick access to payment, and security data. Customers can use the spoke to search for transactions, collaborate with merchants, manage disputes and perform other functions with enhanced security.

</td><td>

Active

</td><td>

false

</td><td>

None

</td></tr><tr><td>

Vulnerability Response Common Workspace \[sn\_vul\_cmn\_ws\] \(Available in the ServiceNow Store\)

</td><td>

Serves as a centralized hub for incorporating common workspace changes that apply across all modules or any new features that are being developed within the workspace environment.

</td><td>

Active

</td><td>

false

</td><td>

Vulnerability Response Common \[sn\_vul\_cmn\]

</td></tr><tr><td>

Access Analyzer\[com.snc.access\_analyzer\]

\(New in Vancouver\)

</td><td>

ServiceNow® Access Analyzer is an application that helps the administrators and developers to view permissions for the selected user, role, or group.

</td><td>

Active

</td><td>

false

</td><td>

 

</td></tr><tr><td>

Account Life Cycle Events\[com.sn\_acct\_lc\]

\(Available in the ServiceNow Store\)

</td><td>

Allows technology industry providers to structure a repeatable, onboarding experience for internal and external customers.

</td><td>

Active

</td><td>

false

</td><td>

-   com.snc.install\_base:sys
-   com.sn\_process\_automation\_designer:sys
-   com.glide.playbook\_experience.config:sys
-   com.snc.csm\_case\_types:sys
-   com.snc.uib.sn\_dyn\_rel\_rec:sys
-   sn\_csm\_playbook:3.1.0
-   sn\_ti\_core:1.0

</td></tr><tr><td>

Accounts Payable Invoice Processing\[sn\_ap\_apm\]

\(New in Vancouver\)

</td><td>

Provides invoice automation solution for Accounts Payable teams which helps businesses reduce risk and improve productivity without additional overhead.

</td><td>

Active

</td><td>

True

</td><td>

-   sn\_ap\_cm
-   sn\_ap\_ic

</td></tr><tr><td>

Accounts Payable Operations integration with Document Intelligence\[sn\_ap\_ic\]

\(New in Vancouver\)

</td><td>

Helps automate ingesting invoices incoming from various channels, such as email, portal, integrations etc.

</td><td>

Active

</td><td>

True

</td><td>

com.sn\_ap\_ic

</td></tr><tr><td>

Additional tables for Federal Agencies \[com.snc.fedtables\]

</td><td>

Provides Federal customers additional data elements that are frequently used or required in Federal forms to build out Federal HR services.

</td><td>

Active

</td><td>

false

</td><td>

com.sn\_hr\_core

</td></tr><tr><td>

Invoice Case Management\[sn\_ap\_cm\]

\(New in Vancouver\)

</td><td>

Allows accounts payable teams to manage invoice and payment related inquiries/requests submitted by suppliers/employees with the objective to faster supplier issue resolution, and improved supplier relations

</td><td>

Active

</td><td>

True

</td><td>

-   com.snc.sn\_shop
-   Supplier Collaboration Portal
-   [Source-to-Pay Operations](https://www.servicenow.com/docs/access?context=source-to-pay-operations-overview&version=zurich&pubname=zurich-source-to-pay-operations&ft:locale=en-US)

</td></tr><tr><td>

AIOPs Dashboards\[com.sn\_itom\_aiops\_dashboards\]

\(Available in the ServiceNow Store, compatible with Vancouver, Utah\)

</td><td>

One stop shop for all ITOM Health/AIOps dashboards for multiple personas - Admin, Manager, SME.

</td><td>

Inactive

</td><td>

false

</td><td>

 

</td></tr><tr><td>

AIOps Experience\[com.sn\_sow\_aiops\]

\(Available in the ServiceNow Store, compatible with Vancouver, Utah, Tokyo\)

</td><td>

AIOps Experience is a set of new experiences composed out of the Express list, Integration Launchpad and AIOps Dashboards.

</td><td>

Inactive

</td><td>

false

</td><td>

Service Operations Workspace ITOM Apps

</td></tr><tr><td>

App Client UX \[com.sn\_app\_client\_ux\]

\(New in Vancouver\)

</td><td>

Enables admins to install, update, and manage licensed applications and plugins on their instance.

</td><td>

Active

</td><td>

false

</td><td>

app-client \(sn\_appclient\)

</td></tr><tr><td>

Asset Management - Procurement Integration\[com.sn\_asset\_proc\_int\]

\(Available in the ServiceNow Store, compatible with Vancouver, Utah\)

</td><td>

Enables Software Asset Management \(SAM\) Admins to create purchase requisitions for software license requirements in the external purchasing system. Later, after the purchase order is received, the receiving transactions are used to automate the entitlement creation in Software Asset Management.

</td><td>

Active

</td><td>

false

</td><td>

-   Procurement \(com.snc.procurement\)
-   Coupa spoke \(sn\_coupa\_spoke\)

</td></tr><tr><td>

Beans.AI Spoke\[com.sn\_beans\_ai\_spoke\]

\(New in Vancouver\)

</td><td>

Beans.AI is the map provider that Schedule Optimization supports for travel time estimates. The plugin enables Schedule Optimization to calculate distances between agents and task.

</td><td>

Active

</td><td>

false

</td><td>

Integration Hub standard installation pack

</td></tr><tr><td>

CMDB CI Class Models\[sn\_cmdb\_ci\_class\]

</td><td>

Adds class models that extend the CMDB class hierarchy, including class descriptions, identification rules, identifier entries, and dependent relationships if applicable. Applications such as Discovery and Service Mapping can use these class extensions to populate configuration items \(CIs\) and discover various technologies and software.

</td><td>

Inactive

</td><td>

false

</td><td>

-   Configuration Management \(CMDB\) \(com.snc.cmdb\)
-   Expanded Model and Asset Classes \(sn\_ent\)
-   Data Foundation Model \(sn\_cmdb\_foundation\)

</td></tr><tr><td>

Customer Service Characteristics\[com.snc.characteristics\]

\(New in Vancouver\)

</td><td>

Enables customers to use the characteristics and related features.

</td><td>

Active

</td><td>

false

</td><td>

None

</td></tr><tr><td>

Customer Service Install Base Characteristics\[com.snc.install\_base\_characteristics\]

\(New in Vancouver\)

</td><td>

Enables customers to capture characteristics for their install bases.

</td><td>

Active

</td><td>

true

</td><td>

-   com.snc.install\_base
-   com.snc.characteristics

</td></tr><tr><td>

Equifax Spoke\[com.sn\_equifax\_spoke\]

\(Available in the ServiceNow Store\)

</td><td>

Enables you to access important information about the credit history for a customer, fraud alerts, digital identity verification, transaction screening, and other relevant data.

</td><td>

Active

</td><td>

false

</td><td>

None

</td></tr><tr><td>

Events and Jobs Dashboard \[sn\_async\_dashboard\]

\(New in Vancouver\)

</td><td>

Monitoring dashboard for System Events and Scheduled Jobs.

</td><td>

Active

</td><td>

false

</td><td>

com.glide.stats.event\_process\_monitoring

</td></tr><tr><td>

Enterprise portfolio\[enterprise\_portfolio\_admin\]

\(Available in the ServiceNow Store, compatible with Utah, not compatible with Vancouver\)

</td><td>

An application to create enterprise portfolios of types "business applications" and "application services" in Digital Portfolio Management \(DPM\).

</td><td>

Active

</td><td>

false

</td><td>

 

</td></tr><tr><td>

Generative AI Controller\[com.sn.generative.ai\]

\(Available in the ServiceNow Store, compatible with Vancouver, Utah, Tokyo\)

</td><td>

Natively integrates Generative AI APIs in the ServiceNow AI Platform.

</td><td>

Active

</td><td>

false

</td><td>

-   OpenAI Generative AI Spoke \(com.sn\_openai\)
-   Microsoft Azure OpenAI Generative AI Spoke \(sn\_azure\_openai\)

</td></tr><tr><td>

Glide Conversation Generative AI \[com.glide.cs.genai\] \(New in Zurich\)

</td><td>

Enables Now Assist

</td><td>

Inactive

</td><td>

true

</td><td>

Generative AI controller

</td></tr><tr><td>

GRC Compliance Case Management Advanced\[com.sn\_comp\_case\_adv\]

\(Available in the ServiceNow Store, compatible with Vancouver, Utah, Tokyo\)

</td><td>

An application to manage Compliance Case Management advanced solution for IRM PRO customers.

</td><td>

Active

</td><td>

false

</td><td>

GRC: Compliance Case Management \(com.sn\_comp\_case\)

</td></tr><tr><td>

GRC Compliance Case Management Full Access\[com.sn\_comp\_case\_fa\]

\(Available in the ServiceNow Store, compatible with Vancouver, Utah, Tokyo\)

</td><td>

An application to manage Compliance Case Management full access solution for IRM enterprise customers.

</td><td>

Active

</td><td>

false

</td><td>

GRC Compliance Case Management Advanced \(com.sn\_comp\_case\_adv\)

</td></tr><tr><td>

GRC Employee User\[com.sn\_grc\_emp\_user\]

\(Available in the ServiceNow Store, compatible with Vancouver, Utah, Tokyo\)

</td><td>

Using this plugin, all employees in the organization can:-   Report – Instances of policy/ compliance violations related to their organization.
-   Request – Policy modifications, clarifications, and so on, to the compliance teams.

</td><td>

Inactive

</td><td>

false

</td><td>

None

</td></tr><tr><td>

GRC: Third-party Due Diligence Request\[com.sn\_tprm\_onboarding\]

\(Available in the ServiceNow Store, compatible with Vancouver, Utah, Tokyo\)

</td><td>

Enables any user to submit a request for due diligence for an engagement with a third party.

</td><td>

Active

</td><td>

true

</td><td>

Third-Party Risk Management GRC: Approver Configurator

</td></tr><tr><td>

Clone Admin Console\[sn\_instance\_clone\]

\(Available in the ServiceNow Store, compatible with Vancouver, Utah\)

</td><td>

Enables the Clone Admin Console, which provides a unified admin experience and enhanced visibility for cloning data between instances, one of our most-used automations. The application includes a simplified clone request experience, a new scheduling tool to prevent timing conflicts, an on-demand backup option, ability to see all clone-related settings in one place, enhanced visibility via a dashboard to easily view current clone activity and more.

</td><td>

Active

</td><td>

false

</td><td>

High Availability Cloning \(com.snc.ha\) \(Requires Utah patch 2 or later\)

</td></tr><tr><td>

Manage Skills Configurable Page\[com.snc.sn\_skill\_cfg\_page\]

\(Available in the ServiceNow Store\)

</td><td>

Enables the management of skill assignments using the Next Experience user interface.

</td><td>

Active

</td><td>

true

</td><td>

Skills Management \(com.snc.skills\_management\)

</td></tr><tr><td>

Map Integrations for Field Service\[com.snc.app\_fsm\_map\_integr\]

\(New in Vancouver\)

</td><td>

Performs intelligent travel time estimates to allocate work order tasks to agents, taking into account both the agent's location and the task's location.

</td><td>

Active

</td><td>

true

</td><td>

Beans.AI Spoke \(com.sn\_beans\_ai\_spoke\)

</td></tr><tr><td>

Microsoft Azure DevOps Pipelines Spoke\[com.sn.azure.pipln.spk\]

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

MID Server Experience\[com.glideapp.agent.experience\]

\(New in Vancouver\)

</td><td>

Helps share meaningful information about your MID Servers Health, Performance, and Adoption. It’s based on Polaris Experience with new look and feel.

</td><td>

Active

</td><td>

false

</td><td>

-   com.glideapp.agent
-   Multiple PAR plugins

 \(All are activated automatically while activating MID Server Experience\)

</td></tr><tr><td>

Platform Document Intelligence\[com.glide.platform\_ml\_di\]

\(New in Vancouver\)

</td><td>

The base plugin for the Document Intelligence application.

</td><td>

Active

</td><td>

false

</td><td>

com.glide.platform\_ml

</td></tr><tr><td>

Post-Sales Support\[com.sn\_pss\_core\]

\(New in Vancouver\)

</td><td>

Provides entitlements and service contracts to enable post-sales support services to customer service users.

</td><td>

Active

</td><td>

true

</td><td>

-   com.sn\_customerservice
-   com.snc.install\_base
-   com.snc.csm\_case\_types
-   com.snc.characteristics

</td></tr><tr><td>

Sustainable IT\[sn\_esg\_sustain\]

\(Available in the ServiceNow Store, compatible with Vancouver, Utah, Tokyo\)

</td><td>

Allows you to effectively manage and monitor the emissions generated by your IT assets. Additionally, the application enables you to keep track of the energy consumption of your assets and their proper disposal after they reach the end of their lifespan.

</td><td>

Inactive

</td><td>

true

</td><td>

-   Hardware Asset Management \(HAM\) Pro
-   ESG Management

</td></tr><tr><td>

Skills Intelligence\[com.snc.skills\_management\]

\(Available in the ServiceNow Store\)

</td><td>

An AI-driven platform that you can use in your organization to develop a workforce that is based on skills.

</td><td>

Inactive

</td><td>

true

</td><td>

Employee Profile

</td></tr><tr><td>

Service Operations Workspace Express List\[com.sn\_itom\_aiops\_list\]

\(Available in the ServiceNow Store, compatible with Vancouver, Utah, Tokyo\)

</td><td>

The Express List is where operators can triage, analyze, and remediate alerts. It’s a live view of alerts, with dynamic filtering, enriched information in a preview panel, and have automation embedded for the user.

</td><td>

Active

</td><td>

false

</td><td>

Service Operations Workspace ITOM applications

</td></tr><tr><td>

Service Operations Workspace Integrations launchpad\[com.snc.uib.sow\_integrations\_launchpad\]

\(Available in the ServiceNow Store, compatible with Vancouver, Utah, Tokyo\)

</td><td>

A consolidated view for all available ITOM health integrations with easy and intuitive experience to configure event connectors. The application is activated automatically with AIOps experience.

</td><td>

Active

</td><td>

false

</td><td>

 

</td></tr><tr><td>

Service Operations Workspace Metric Explorer\[com.sn\_itom\_metric\_exp\]

\(Available in the ServiceNow Store, compatible with Vancouver, Utah, Tokyo\)

</td><td>

A new Metric Explorer application for SOW that replaces the earlier one. The application is installed automatically with ACC-M.

</td><td>

Inactive

</td><td>

false

</td><td>

 

</td></tr><tr><td>

Service Operations Workspace Metric Explorer APIs\[com.sn\_sow\_metric\_exp\]

\(Available in the ServiceNow Store, compatible with Vancouver, Utah, Tokyo\)

</td><td>

A new Metric Explorer application for SOW that replaces the earlier one. The application is installed automatically with ACC-M.

</td><td>

Inactive

</td><td>

false

</td><td>

 

</td></tr><tr><td>

Task Grouping\[com.snc.task\_grouping\]

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Task Intelligence for ITSM\[com.snc.itsm\_ml\_task\]

\(Available in the ServiceNow Store, compatible with Vancouver, Utah\)

</td><td>

Uses machine learning to set up, deploy, and track the solution-based models to achieve important business outcomes.

</td><td>

 

</td><td>

false

</td><td>

-   Recommended Actions for ITSM - Advanced \(com.snc.uib.sow\_itsm\_ra\_advanced\)
-   Task Intelligence Admin Console \(com.sn\_ti\_admin\)

</td></tr><tr><td>

Technology core\[com.sn\_ti\_core\]

\(Available in the ServiceNow Store\)

</td><td>

Technology industry vertical CSM extension.

</td><td>

Active

</td><td>

false

</td><td>

com.sn\_customerservice

</td></tr><tr><td>

Transporter\[com.sn\_transport\]

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Zero Trust - Location Based Access\[com.snc.zero\_trust\_location\_access\]

</td><td>

Location filter is a filter criteria that the admins can use while crafting the authentication policies based on the physical location of the device.

</td><td>

Active

</td><td>

false

</td><td>

Adaptive Authentication \(com.snc.adaptive\_authentication\)

</td></tr><tr><td>

Zero Trust - Policy Based Session Access\[com.snc.zero\_trust\_session\_access\]

</td><td>

ServiceNow® Zero Trust - Policy Based Session Access \(Session Access\) enables organizations to dynamically reduce user privilege in a web session based on a variety of factors, including IP address, location, authentication method, user’s role, group, user having MFA and attributes shared by the Identity Provider \(IDP\).

</td><td>

Active

</td><td>

false

</td><td>

Adaptive Authentication \(com.snc.adaptive\_authentication\)

</td></tr><tr><td>

Vulnerability Response Integration with Claroty CTD\[com.sn\_clarotyctdvr\]

\(Available in the ServiceNow Store, compatible with Vancouver, Utah\)

</td><td>

Uses vulnerability data imported from Claroty CTD to enable risk-based action with the production process context.

</td><td>

Active

</td><td>

false

</td><td>

-   Service Graph Connector Integration for Claroty CTD \(com.sn\_clarotyctdsgc\)
-   CMDB CI Class Models \(com.sn\_cmdb\_ci\_class\)

</td></tr><tr><td>

Workplace Connectors \(sn\_wsd\_wc\)\(Available in the ServiceNow Store, compatible with Vancouver, Utah\)

</td><td>

Workplace Connectors is a generic framework using which data from different kinds of workplace hardware/sensors \(such as badging systems, occupancy sensors\) can be brought into WSD product via the respective spokes.

</td><td>

Active

</td><td>

false

</td><td>

Workplace Central \(sn\_wsd\_central\)

</td></tr><tr><td>

Threat Intelligence Security Center for Security Operations\[com.snc.secops.threat.intel.security.center\]

\(Available in the ServiceNow Store, compatible with Vancouver, Utah, Tokyo\)

</td><td>

Allows you to find indicators of compromise \(IoC\) and enrich security incidents with threat intelligence security center data.

</td><td>

Inactive

</td><td>

false

</td><td>

-   Security Support Common \(com.snc.security\_support.common\)
-   Threat Intelligence Support Common \(com.snc.threat\)
-   Security Case Management common workspace components \(com.snc.escm.ws\_commons\)

</td></tr><tr><td>

Network Inventory Advanced\[sn\_ni\_adv\]

\(Available in the ServiceNow Store, compatible with Vancouver, Utah, Tokyo\)

</td><td>

Advanced capabilities of telecommunications network inventory.

</td><td>

Active

</td><td>

true

</td><td>

-   Inventory Number Management \(sn\_inv\_num\_mgmt\)
-   Attribute Pack \(sn\_attribute\_pack\)

</td></tr><tr><td>

Network Inventory Core\[sn\_ni\_core\]

\(Available in the ServiceNow Store, compatible with Vancouver, Utah, Tokyo\)

</td><td>

Application to manage network inventory.

</td><td>

Active

</td><td>

true

</td><td>

-   Inventory Number Management \(sn\_inv\_num\_mgmt\)
-   Attribute Pack \(sn\_attribute\_pack\)

</td></tr><tr><td>

Data Separation\[sn\_ds\]

\(Available in the ServiceNow Store\)

</td><td>

Enables organizations to restrict access to sensitive data based on a lens hierarchy and its leaf node. The application supports records, related items, planning consoles, workbenches, and reports.

</td><td>

Active

</td><td>

false

</td><td>

-   PPM Standard \(com.snc.financial\_planning\_pmo\)
-   Portfolio Planning \(sn\_align\_ws\)

</td></tr><tr><td>

DevOps Vulnerability Integrations\[sn\_devops\_vul\_ints\]

\(Available in the ServiceNow Store, compatible with Vancouver, Utah, Tokyo\)

</td><td>

Provides a new framework and data model for DevOps integration with application security tools. It’s an extensible framework that also enables you to create custom integrations with any application security tool.

</td><td>

Active

</td><td>

false

</td><td>

com.sn\_devops

</td></tr><tr><td>

Action Status Automation\[com.sn\_action\_status\]

</td><td>

This plugin tracks blocking records created for tasks and updates the action status indicators on the task list.

</td><td>

Active

</td><td>

true

</td><td>

 

</td></tr><tr><td>

Activate all Software Asset Management Professional plugins including Software Asset Workspace \[com.sn\_samp\_master\_ws\]

 \(New in Utah\)

</td><td>

Provides the capability to normalize software discovery information, reconcile entitlements with installs, and reclaiming unused software. Provides additional capabilities to reconcile publisher products.

</td><td>

Inactive

</td><td>

true

</td><td>

-   com.sn\_samp\_master
-   com.sn\_sam\_workspace

</td></tr><tr id="plugin_com.glide.ui_activity_formatter" class="plugin_reference"><td class="name">

Activity formatter\[com.glide.ui\_activity\_formatter\]

</td><td>

This plugin lets you quickly and easily filter the list of activities, or history, on a task form.

</td><td class="has_demo_data">

Active

</td><td class="requires">

false

</td><td class="name">

 

</td></tr><tr><td>

Admin Center\[sn\_admin\_center\]

 \(Available in the ServiceNow Store\)

</td><td>

Provides a central hub for platform owners and admins to access platform capabilities easily, discover new applications, and get intelligent, actionable insights.

</td><td>

Active

</td><td>

false

</td><td>

sn\_ace

</td></tr><tr><td>

Admin Experience Framework\[com.sn.ace\_framework\]

 \(New in Tokyo\)

</td><td>

Supports new UI framework used by various applications, including Admin Center.

</td><td>

Active

</td><td>

false

</td><td>

None

</td></tr><tr><td>

Adoption Blueprint for Technology Excellence\[sn\_itsm\_bus\_obj\]

 \(Available in the ServiceNow Store\)

</td><td>

Adoption blueprints, a part of Admin Center, displays a recommended set of applications and plugins available to you in an ideal order of installation and adoption to achieve business goals.

</td><td>

Active

</td><td>

false

</td><td>

sn\_admin\_center

</td></tr><tr><td>

Advanced AI Search Management Tools\[sn\_ais\_admin\_tools\]

</td><td>

Includes AI Search dashboards and Search Preview tool.

</td><td>

Inactive

</td><td>

false

</td><td>

 

</td></tr><tr><td>

Advanced Work Assignment\[com.glide.awa\]

</td><td>

Automatically assigns work items to agents based on their availability, capacity, and skills.

</td><td>

Active

</td><td>

false

</td><td>

com.snc.skills\_management

</td></tr><tr><td>

Advanced Work Assignment - Agent Affinity\[com.glide.awa.agent\_affinity\]

</td><td>

Enable work assignment to the best-suited agent based on the agent’s affinity to the work item.

</td><td>

Inactive

</td><td>

false

</td><td>

com.glide.awa

</td></tr><tr><td>

Advanced Work Assignment for HRSD\[com.sn\_hr\_awa\]

</td><td>

Contains out-of-box configuration data supporting routing, queuing, and assignment of HRSM cases, chats, and calls to agents.

</td><td>

Inactive

</td><td>

false

</td><td class="requires">

-   com.glide.awa
-   com.sn\_hr\_core
-   com.glide.interaction.awa

</td></tr><tr><td>

Advanced Work Assignment for Incidents\[com.snc.incident.awa\]

</td><td>

Default configuration to support Advanced Work Assignment for Incident

</td><td>

Active

</td><td>

false

</td><td class="requires">

-   com.glide.awa
-   com.snc.agent\_workspace.itsm

</td></tr><tr><td>

Advanced Work Assignment for Source-to-Pay Operations\[com.snc.sn\_spend\_awa\]

\(Available in the ServiceNow Store\)

</td><td>

Automatically assign work to your agent using advanced work assignment.

</td><td>

Inactive

</td><td>

true

</td><td>

-   Advanced Work Assignment \(com.glide.awa\)
-   Agent Chat \(com.glide.interaction.awa\)
-   Procurement Case Management \(com.sn\_spend\_psd\)

</td></tr><tr><td>

Advanced Work Assignment for Supplier Lifecycle Operations\[com.snc.sn\_slm\_awa\]

\(Available in the ServiceNow Store\)

</td><td>

Automatically assign supplier cases to agents based on availability and capacity.

</td><td>

Inactive

</td><td>

true

</td><td>

-   Advanced Work Assignment \(com.glide.awa\)
-   Agent Chat \(com.glide.interaction.awa\)
-   Glide Virtual Agent \(com.glide.cs.chatbot\)
-   Supplier Lifecycle Operations \(com.snc.sn\_supplier\_mgmt\)

</td></tr><tr><td>

Agent Chat\[com.glide.interaction.awa\]

</td><td>

Enables Workspace Agent Chat and the Chat service channel in Advanced Work Assignment.

</td><td>

Active

</td><td>

true

</td><td class="requires">

-   com.glide.interaction
-   com.glide.awa

</td></tr><tr><td>

Agent Client Collector Framework\[sn\_agent\]

 \(Available in the ServiceNow Store\)

</td><td>

Management of Agent Client Collector

</td><td>

Active

</td><td>

false

</td><td class="requires">

-   com.snc.sa.mid.webserver
-   com.snc.cmdb.scoped

</td></tr><tr><td>

Agent Client Collector Monitoring\[sn\_itmon\]

 \(Available in the ServiceNow Store\)

</td><td>

Monitoring solution using the Agent Client Collector

</td><td>

Active

</td><td>

false

</td><td>

 

</td></tr><tr><td>

Agent Client Collector for Investigation\[sn\_acc\_adapter\]

 \(Available in the ServiceNow Store\)

</td><td>

Enables you to retrieve and display the CI metrics information of the affected CIs.

</td><td>

Active

</td><td>

true

</td><td>

None

</td></tr><tr><td>

Agent Forecast\[com.sn\_agent\_forecast\]

</td><td>

Forecasts agents based on historical data.

</td><td>

 

</td><td>

false

</td><td>

com.snc.clotho

</td></tr><tr><td>

Agent Intelligence\[com.glide.platform\_ml\]

</td><td>

Renamed to Predictive Intelligence.

</td><td>

Active

</td><td>

false

</td><td>

com.glide.platform\_ml\_pa

</td></tr><tr><td>

Agent Intelligence Reports\[com.glide.platform\_ml\_pa\]

</td><td>

Renamed to Predictive Intelligence Reports.

</td><td>

Active

</td><td>

false

</td><td>

 

</td></tr><tr><td class="name">

Agent Schedule\[com.snc.agent\_schedule\]

</td><td>

Enables customer service agents and field service technicians to see work schedules and assignments and also add personal events such as meetings or appointments.

</td><td>

Active

</td><td>

false

</td><td>

com.snc.app.agent\_calendar\_widget

</td></tr><tr><td>

Agent Workspace\[com.agent\_workspace\]

</td><td>

It is a suite of tools that provide agents, case managers, help desk professionals, and managers with tools to help answer customer questions or resolve customer problems.

</td><td>

Active

</td><td>

false

</td><td class="requires">

-   com.glide.uxbuilder
-   com.glide.graphql
-   com.glide.interaction
-   com.snc.agent\_workspace.config
-   com.snc.agent\_workspace.ribbon
-   com.snc.agent\_workspace.list
-   com.snc.agent\_workspace.form
-   com.snc.agent\_workspace.global\_search
-   com.snc.agent\_workspace.declarative\_actions

</td></tr><tr><td>

Agent Workspace - Knowledge\[sn-component-workspace-knowledge\]

</td><td>

Enables use of Knowledge Base in Agent Assist.

</td><td>

Active

</td><td>

false

</td><td>

com.snc.agent\_workspace.config

</td></tr><tr><td>

Agent Workspace - List\[com.snc.agent\_workspace.list\]

</td><td>

Workspace List Configurations

</td><td>

Active

</td><td>

false

</td><td>

com.snc.agent\_workspace.config

</td></tr><tr><td>

Agent Workspace - Ribbon\[com.snc.agent\_workspace.ribbon\]

</td><td>

Workspace Ribbon Configurations

</td><td>

Active

</td><td>

false

</td><td class="requires">

-   com.glide.uxbuilder
-   com.snc.agent\_workspace.config
-   com.sn\_resolutionshaper

</td></tr><tr id="plugin_com.glide.web_service_aggregate" class="plugin_reference"><td class="name">

Aggregate Web Service\[com.glide.web\_service\_aggregate\]

</td><td class="description">

Provides SOAP Access to GlideAggregate functionality.

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

 

</td></tr><tr><td>

Agile Development 2.0\[com.snc.sdlc.agile.2.0\]

</td><td>

The Agile Development 2.0 plugin provides enhanced functionality on top of Agile Development. If you already have a customized version of Agile Development, delete the customizations before activating Agile Development 2.0 to ensure that all features work properly. Refer to the documentation for detailed steps to delete the customizations.

</td><td>

Active

</td><td>

true

</td><td class="requires">

-   com.snc.sdlc.scrum.ppm\_int
-   com.snc.planned\_task\_v2
-   com.snc.sdlc.agile.2.0.common
-   com.snc.sdlc.ranking

</td></tr><tr><td class="name">

Agile Development — Unified Backlog\[com.snc.sdlc.agile.multi\_task\]

</td><td class="description">

Enables you to maintain a centralized backlog containing records of different task types, such as defects, problems, incident tasks, and stories. Include any tasks into your agile workflow

</td><td>

Active

</td><td class="has demo data">

false

</td><td class="requires">

-   com.snc.sdlc.agile.2.0
-   com.snc.sdlc.agile.multi\_task.common

</td></tr><tr><td>

Agile - Scaled Agile Framework - Essential SAFe\[com.snc.sdlc.safe\]

</td><td>

Scaled Agile Framework was designed to apply Lean-Agile principles to the entire organization. Essential SAFe is the most basic configuration of the framework and it provides the minimal elements necessary to be successful with SAFe: manage your agile release train backlog, plan program increments,

</td><td>

Active

</td><td>

true

</td><td class="requires">

-   com.snc.sdlc.ranking
-   com.snc.sdlc.agile.2.0

</td></tr><tr><td>

Agile - Scaled Agile Framework - Portfolio SAFe\[com.snc.sdlc.portfolio\_safe\]

</td><td>

Use Portfolio SAFe to apply lean and agile principles to your portfolio work.

</td><td>

Active

</td><td>

true

</td><td class="requires">

-   com.snc.sdlc.safe
-   com.snc.portfolio\_management

</td></tr><tr><td>

Agile Development 2.0 - ATF Tests\[com.snc.sdlc.agile.2.0.atf\]

</td><td>

Agile Development 2.0 - ATF Tests provides you test cases and test suites that can be run on the Agile Development 2.0 application.

</td><td>

Active

</td><td>

false

</td><td>

 

</td></tr><tr><td>

AI Search\[com.glide.ais\]

</td><td>

Installs and enables AI Search capabilities, providing relevant, contextual, and personal search experiences across different interfaces.

</td><td>

Active

</td><td>

false

</td><td>

-   com.glide.search.signal\_data
-   com.glide.platform\_ml
-   com.glide.nlu
-   com.snc.nlu\_studio

</td></tr><tr><td>

AI Search Assist\[com.snc.ai\_search\_assist\]

</td><td>

Helps users deflect or quickly resolve their issues without involving the service desk operators. It can include results from Knowledge and Service catalog, allowing a user to directly order a catalog item from a search.

</td><td>

Active

</td><td>

false

</td><td>

com.glide.search

</td></tr><tr><td>

AI Search for Customer Portals\[com.snc.csm.portal\_ais\]

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

-   com.glide.ais
-   com.glide.ais\_enabler

</td></tr><tr><td>

AI Search Index Sources\[com.glide.ais.index\_sources\]

</td><td>

Includes [indexed source](../../ai-search/concept/indexed-sources-ais.md) definitions for ServiceNow AI Platform tables beyond those provided in the base system:-   Catalog Task \[sc\_task\]
-   Change \[change\_request\]
-   Change Task \[change\_task\]
-   Company \[core\_company\]
-   Group \[sys\_user\_group\]
-   Incident \[incident\]
-   Location \[cmn\_location\]
-   Problem \[problem\]
-   Request \[sc\_request\]
-   Requested Item \[sc\_req\_item\]

</td><td>

Inactive

</td><td>

false

</td><td>

 

</td></tr><tr><td>

AI Search Spoke\[sn\_ai\_spoke\]

 \(Available in the ServiceNow Store\)

</td><td>

Helps with Integration Hub execute AI search queries.

</td><td>

Active

</td><td>

false

</td><td>

com.glide.ais.external\_content

</td></tr><tr><td>

Alert Rules Management\[com.sn-em-arm\]

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Portfolio Planning\[sn\_align\_ws\]

 \(Available in the ServiceNow Store\)

</td><td>

Helps the product and portfolio managers drive organizational alignment and facilitate Agile transformation by combining waterfall and agile work streams.

</td><td>

Active

</td><td>

true

</td><td>

com.sn\_roadmap\_plng

</td></tr><tr><td>

Alignment Planner Workspace integration with Azure DevOps \(ADO\)\[com.sn\_align\_ado\_int\]

 \(New in San Diego\)

</td><td>

Enables import, export, and bidirectional synchronization of records between ServiceNow® Alignment Planner Workspace \(APW\) and Microsoft Azure DevOps by integrating the two applications.

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Analyst workspace for Security Incident Response\[com.snc.security\_incident.workspace\]

 \(New in Tokyo\)

</td><td>

Enables analysts and incident managers to prioritize their work using a dedicated workspace, monitor and view the status of incidents.

</td><td>

Active

</td><td>

false

</td><td>

-   sn\_si
-   sn\_sirw\_evam\_card

</td></tr><tr><td>

Analytics Center\[com.snc.pa.analytics\_center\]

</td><td>

Performance Analytics Center - Enables users to get answers about their data quickly using search-driven analytics.

</td><td>

Inactive

</td><td>

false

</td><td class="requires">

-   com.agent\_workspace
-   com.workspace\_core
-   sn-component-nlq
-   com.snc.par.nlq.core

</td></tr><tr><td>

Analytics Task\[com.snc.pa.analytics\_task\]

</td><td>

Provides the core framework for workflow related to Analytics. It consists of the analytics task table and related artifacts.

</td><td>

Active

</td><td>

false

</td><td>

 

</td></tr><tr id="plugin_com.glide.ui.ng.amb" class="plugin_reference"><td class="name">

Angular AMB Services\[com.glide.ui.ng.amb\]

</td><td class="description">

Angular Services for AMB

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

-   com.glide.ui.ng
-   com.glide.amb
-   com.glide.record\_watcher

</td></tr><tr><td>

Anonymous Connect Support\[com.glide.connect.anonymous\_support\]

</td><td>

Plugin to enable access and properties for Anonymous Connect Support.

</td><td>

Inactive

</td><td>

false

</td><td>

com.glide.connect.support

</td></tr><tr><td>

Anonymous Report Center\[com.sn\_anonymous\_report\_center\]

</td><td>

Enables users to submit cases without disclosing their identities to agents or admins within their organizations.

</td><td>

Active

</td><td>

false

</td><td>

com.sn\_content\_delivery

</td></tr><tr id="plugin_com.glide.api_analytics" class="plugin_reference"><td class="name">

API Analytics\[com.glide.api\_analytics\]

</td><td class="description">

Allows admins to view API Analytics statistics for web services.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

-   com.glide.db.query\_stats
-   com.snc.pa
-   com.glideapp.canvas

</td></tr><tr><td class="name">

API Stats\[com.glide.stats.api\]

</td><td class="description">

API Stats

</td><td>

Active

</td><td class="has demo data">

false

</td><td class="requires">

-   com.glide.db.query\_stats
-   com.snc.pa
-   com.glideapp.canvas

</td></tr><tr><td>

App APIs\[com.glide.app\_api\]

</td><td>

APIs for fetching Application and Application Rollback related information.

</td><td>

Active

</td><td>

true

</td><td>

 

</td></tr><tr><td>

App Collaboration\[com.glide.app\_collaboration\]

</td><td>

Plugin that complements Delegated Developer for facilitating application collaboration. Requires App Engine license.

</td><td>

Active

</td><td>

false

</td><td>

com.glide.delegated\_development

</td></tr><tr><td class="name">

App Dependency Client\[com.sn\_dependentclient\]

</td><td class="description">

Plugin to provide list of store applications/integrations based on their active plugins. Uses store's web service to create a cache of such applications on the customer instances itself.

</td><td>

Inactive

</td><td class="has demo data">

false

</td><td>

 

</td></tr><tr><td>

App Engine Management Center\[com.sn\_aemc\]

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td class="name">

App Engine Studio\[com.snc.app-engine-studio\]

</td><td class="description">

Installs and enables App Engine Studio, a development tool for creators of varying skill levels to build applications that meet the immediate needs of your organization.

</td><td>

Inactive

</td><td class="has_demo_data">

true

</td><td class="requires">

 

</td></tr><tr id="plugin_com.glide.sys.app_authorization" class="plugin_reference"><td class="name">

Application Authorization\[com.glide.sys.app\_authorization\]

</td><td class="description">

 

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

 

</td></tr><tr id="plugin_com.snc.apps_creator" class="plugin_reference"><td class="name">

Application Creator\[com.snc.apps\_creator\]

</td><td class="description">

Retired. Replaced by the Platform as a Service plugin.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

-   com.glide.ui.angular
-   com.glide.ui.heisenberg

</td></tr><tr id="plugin_com.snc.apps_creator_template" class="plugin_reference"><td class="name">

Application Creator Templates\[com.snc.apps\_creator\_template\]

</td><td class="description">

Hosts system application creator templates.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

 

</td></tr><tr id="plugin_com.glide.scope.design" class="plugin_reference"><td class="name">

Application Design Restrictions\[com.glide.scope.design\]

</td><td class="description">

System for restricting and capturing tables augmented by an application

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

 

</td></tr><tr><td>

Application Diagnostics Tool\[com.snc.app\_diagnostics\_tool\]

</td><td>

Helps you to diagnose the PPM Applications, with quick diagnostic scans and resolve the issues with fix scripts.

</td><td>

Active

</td><td>

false

</td><td>

 

</td></tr><tr id="plugin_com.snc.apps_file" class="plugin_reference"><td class="name">

Application File\[com.snc.apps\_file\]

</td><td class="description">

Associates configuration records with an application and tracks record metadata.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

 

</td></tr><tr><td>

Application Insights\[sn\_app\_insights\]

 \(Available in the ServiceNow Store\)

</td><td>

Provides a centralized location where you can visualize and monitor system health.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

com.snc.clotho

</td></tr><tr id="plugin_com.snc.metadata" class="plugin_reference"><td class="name">

Application Metadata\[com.snc.metadata\]

</td><td class="description">

Adds relationships and UI actions to work with metadata.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

 

</td></tr><tr><td>

Application Portfolio Management\[com.snc.apm\]

</td><td>

Helps enterprises have visibility into their business applications inventory and enables analysts to rationalize business applications. Provides Performance Analytics dashboards like Application 360, Landscape Analysis, and associated dashboards of Business Applications with Change requests, Incidents, and Problems. This plugin activates the following related plugins if they are not already active: -   Application Portfolio Management – Predictive Intelligence \(com.snc.apm.predictive\_intelligence\): Predicts application category by applying algorithms like similarity on business applications-related data.
-   Business Planner: Enables access to the Business Planning portal.

</td><td>

Active

</td><td class="has-demo-data">

true

</td><td class="requires">

-   com.snc.certification\_v2
-   com.snc.fiscal\_calendar
-   com.snc.treemap
-   com.snc.sp\_workbench\_widgets
-   com.snc.apm.business\_planner
-   com.snc.pa.apm
-   com.snc.demand\_core
-   com.snc.apm.predictive\_intelligence

</td></tr><tr><td>

Application Portfolio Management – ATF Test\[com.snc.apm.atf\]

</td><td>

Validates ATF tests for Application Portfolio Management

</td><td>

Active

</td><td>

false

</td><td>

com.snc.apm

</td></tr><tr><td>

Application Portfolio Management - Technology Reference Model \(TRM\)\[com.snc.apm\_trm\]

 \(New in Tokyo\)

</td><td>

Allows enterprise architects to approve or restrict the use of a software product within the organization.

</td><td>

Active

</td><td>

true

</td><td>

com.snc.apm

</td></tr><tr><td>

Application Portfolio Management Core\[com.snc.apm\_core\]

</td><td>

Enables register a new business application

</td><td>

Active

</td><td>

false

</td><td class="requires">

-   com.glideapp.servicecatalog.platform
-   com.glide.hub.designer\_backend.model

</td></tr><tr><td>

Application Portfolio Management Digital Integration Management\[com.snc.apm\_digital\_integration\]

 \(Available in the ServiceNow Store\)

</td><td>

Enables APM users to manage integrations in Application Portfolio Management.

</td><td>

Active

</td><td>

true

</td><td>

com.snc.apm

</td></tr><tr><td>

Application Portfolio Management Workspace\[sn\_apm\_ws\]

 \(Available in the ServiceNow Store\)

</td><td>

Enables Enterprise Architects to have a visibility in to all the important aspects of their applications in Application Portfolio Management.

</td><td>

Active

</td><td>

false

</td><td>

com.snc.apm

</td></tr><tr><td>

Application Service\[com.snc.cmdb.it\_service\]

</td><td>

Provides functionality and view for Application Service creation, editing and history view.

</td><td>

Active

</td><td>

false

</td><td class="requires">

-   com.snc.itom.ui
-   com.snc.cmdb
-   com.snc.cmdb.service.modeling
-   com.glide.ui.list\_v3\_components

</td></tr><tr id="plugin_com.snc.apps_access" class="plugin_reference"><td class="name">

Applications Access Control\[com.snc.apps\_access\]

</td><td class="description">

Implements file-level access for application development.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

-   com.snc.apps
-   com.snc.apps\_picker

</td></tr><tr id="plugin_com.snc.apps_picker" class="plugin_reference"><td class="name">

Applications Picker\[com.snc.apps\_picker\]

</td><td class="description">

Allows users to select the desired application during application development.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

 

</td></tr><tr><td class="name">

Apply Once APIs\[com.glide.system\_apply\_once\]

</td><td class="description">

APIs for altering the behavior of any 'apply\_once' update in a plugin during plugin activation/upgrade

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

 

</td></tr><tr><td>

Appointment Booking\[com.snc.appointment\_booking\]

</td><td>

Enables customers to book service appointments from the Customer and Consumer Service Portals.

</td><td>

Inactive

</td><td>

true

</td><td>

 

</td></tr><tr><td>

Appointment Booking Demo Data\[com.snc.appointment\_booking\_demo\]

</td><td>

Provides demo data for the appointment booking feature.

</td><td>

Inactive

</td><td>

false

</td><td>

 

</td></tr><tr id="plugin_com.glide.e_signature_approvals" class="plugin_reference"><td class="name">

Approvals with e-Signature\[com.glide.e\_signature\_approvals\]

</td><td class="description">

Adds a prompt for credentials when an approver attempts to approve a request via the list context menu or Approve UI Action on the Approval form.

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

 

</td></tr><tr id="plugin_com.snc.architecture_compliance" class="plugin_reference"><td class="name">

Architecture Compliance\[com.snc.architecture\_compliance\]

</td><td class="description">

Manages scheduled or on-demand audits of CMDB records, to determine if configuration items \(CI\) match expected attributes.

</td><td>

Inactive

</td><td class="has_demo_data">

true

</td><td class="requires">

com.snc.certification\_core

</td></tr><tr id="plugin_com.snc.assessment_core" class="plugin_reference"><td class="name">

Assessment\[com.snc.assessment\_core\]

</td><td class="description">

Provides capabilities to use custom questionnaires and scripted queries to evaluate, score, and compare any records in ServiceNow.

</td><td>

Active

</td><td class="has_demo_data">

true

</td><td class="requires">

-   com.glideapp.workflow
-   com.glideapp.survey
-   com.snc.bestpractice.task\_survey
-   com.glide.survey\_designer

</td></tr><tr id="plugin_com.snc.assessment" class="plugin_reference"><td class="name">

Assessment Designer\[com.glide.assessment\_designer\]

</td><td class="description">

Activates assessment designer that is a drag-and-drop interface to create assessments.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

com.glide.assessment\_designer.common

</td></tr><tr id="plugin_com.glide.assessment_designer.common" class="plugin_reference"><td class="name">

Assessment Designer Common\[com.glide.assessment\_designer.common\]

</td><td class="description">

Base plugin for assessment related designers like Quiz Designer, Survey Designer, Assessment designer. You must activate Assessment Designer Common plugin before using Quiz Designer, Survey Designer, or Assessment Designer. By default, this plugin is activated.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

com.glide.ui.ng.dc

</td></tr><tr id="plugin_com.snc.asset_management" class="plugin_reference"><td class="name">

Asset Management\[com.snc.asset\_management\]

</td><td class="description">

Lets you manage all your assets, consumables, and software licenses.

</td><td>

Active

</td><td class="has_demo_data">

true

</td><td class="requires">

-   com.snc.expense\_line
-   com.snc.model
-   com.snc.organization\_management
-   com.snc.fixed\_asset
-   com.snc.depreciation
-   com.snc.automation
-   com.glideapp.home

</td></tr><tr><td>

Asset Management Common\[com.sn\_itam\_common\]

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Asset Management Performance Analytics\[com.snc.ast\_mgmt\_pa\]

</td><td>

Performance Analytics for Asset Management out-of-the-box KPIs.

</td><td>

Active

</td><td>

false

</td><td>

 

</td></tr><tr><td>

Asset Management Workspace\[com.sn\_itam\_workspace\]

</td><td>

Enables ITAM capabilities in Workspace.

</td><td>

Active

</td><td>

false

</td><td>

-   com.sn\_itam\_recomm
-   com.snc.app\_shell\_aw
-   com.snc.uib.base\_agent\_workspace

</td></tr><tr><td>

Asset Management Workspace - Recommendations\[com.sn\_itam\_recomm\]

</td><td>

Recommendations feature for workspaces.

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Assignment Workbench\[com.snc.assignment\_workbench\]

</td><td>

Provides a workbench that customer service managers can use to evaluate agents based on configurable criteria, such as skills and availability, and then assign tasks to the desired agents.

</td><td>

Inactive

</td><td>

false

</td><td>

com.snc.matching\_rule

</td></tr><tr><td>

ATF Test Generator and Cloud Runner\[sn\_atf\_tg\]

 \(Available in the ServiceNow Store\)

</td><td>

One-click test generation and cloud execution for ATF.

</td><td>

Inactive

</td><td>

false

</td><td>

-   com.glide.automated\_testing\_framework
-   com.glide.auth.mutual

</td></tr><tr><td>

Availability\[com.snc.availability\]

 \(New in Tokyo\)

</td><td>

Allows organization to calculate availability for select configuration items.

</td><td>

Active

</td><td>

false

</td><td>

-   com.snc.cmdb
-   com.snc.service\_portfolio\_core

</td></tr><tr><td class="name">

Auto Recovery\[com.glide.autorecovery\]

</td><td class="description">

Enables Auto Recovery functionality.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

 

</td></tr><tr><td>

Automated Test Framework\[com.glide.automated\_testing\_framework\]

</td><td>

Testing framework and tools for creating automated tests

</td><td>

Active

</td><td>

true

</td><td class="requires">

-   com.glide.rollback
-   com.glide.ui.angular
-   com.glide.element\_mapping
-   com.glide.vars

</td></tr><tr><td>

Automated Test Framework - Application Navigator\[com.glide.automated\_testing\_impl.left\_nav\]

</td><td>

Provides ATF steps that validate access to the application navigator.

</td><td>

Active

</td><td>

false

</td><td>

com.glide.automated\_testing\_framework

</td></tr><tr><td>

Automated Test Framework - Custom UI\[com.glide.automated\_testing\_impl.custom\_ui\]

</td><td>

Adds ability to test custom UI.

</td><td>

Active

</td><td>

false

</td><td>

com.glide.automated\_testing\_framework

</td></tr><tr><td>

Automated Test Framework - Parameters\[com.glide.automated\_testing\_impl.parameters\]

</td><td>

Adds ability to parameterize ATF tests.

</td><td>

Active

</td><td>

false

</td><td>

com.glide.automated\_testing\_framework

</td></tr><tr><td>

Automated Test Framework - Reporting\[com.glide.automated\_testing\_impl.report\]

</td><td>

Automated Testing Framework Reporting test step configuration.

</td><td>

Active

</td><td>

false

</td><td class="requires">

-   com.glide.automated\_testing\_framework
-   com.glideapp.report

</td></tr><tr><td>

Automated Test Framework - Responsive Dashboards\[com.glide.automated\_testing\_impl.dashboards\]

</td><td>

Automated Testing Framework Responsive Dashboard test step configuration.

</td><td>

Active

</td><td>

false

</td><td class="requires">

-   com.glide.automated\_testing\_framework
-   com.glideapp.dashboards

</td></tr><tr><td>

Automated Test Framework - REST Inbound\[com.glide.automated\_testing\_impl.rest\_inbound\]

</td><td>

Automated Test Framework for inbound REST requests.

</td><td>

Active

</td><td>

true

</td><td>

com.glide.automated\_testing\_framework

</td></tr><tr><td>

Automated Test Framework - Schedule\[com.glide.automated\_testing\_impl.schedule\]

</td><td>

Tools for scheduling automated tests.

</td><td>

Active

</td><td>

false

</td><td>

com.glide.automated\_testing\_framework

</td></tr><tr><td>

Automated Test Framework - Allowed Errors\[com.glide.automated\_testing\_impl.wce\]

</td><td>

JavaScript errors found during UI test execution can be ignored or tracked as warnings. Test designers can complete their work while developers investigate and resolve scripting issues.

</td><td>

Active

</td><td>

false

</td><td>

com.glide.automated\_testing\_framework

</td></tr><tr><td>

Automated Test Framework Service Catalog\[com.glide.automated\_testing\_impl.service\_catalog\]

</td><td>

Automated Testing Framework Service Catalog test step configuration.

</td><td>

Active

</td><td>

true

</td><td class="requires">

-   com.glide.automated\_testing\_framework
-   com.glideapp.servicecatalog

</td></tr><tr><td>

Automated Test Framework Service Catalog Service Portal\[com.glide.automated\_testing\_impl.service\_catalog\_portal\]

</td><td>

Automated Testing Framework for Service Catalog widgets in Service Portal test step configuration.

</td><td>

Active

</td><td>

true

</td><td>

com.glide.automated\_testing\_impl.service\_catalog

</td></tr><tr><td>

Automated Test Framework Service Portal\[com.glide.automated\_testing\_impl.service\_portal\]

</td><td>

Automated Testing Framework Service Portal test step configuration. This plugin can only be activated by activating the "Service Portal - Core" plugin.

</td><td>

Active

</td><td>

false

</td><td>

com.glide.automated\_testing\_framework

</td></tr><tr><td>

Automated Test Scripts For Survey\[com.glide.automated\_testing\_impl.survey\]

</td><td>

Automated Test Scripts For Survey.

</td><td>

Active

</td><td>

false

</td><td class="requires">

-   com.glide.automated\_testing\_framework
-   com.snc.assessment\_core

</td></tr><tr><td>

Automated Testing for Virtual Agent\[com.glide.cs.atf\]

\(New in Utah\)

</td><td>

Activates the Automated Testing capabilities for Virtual Agent.

</td><td>

Active

</td><td>

false

</td><td>

com.glide.cs

</td></tr><tr id="plugin_com.snc.automatic_assignment" class="plugin_reference"><td class="name">

Automatic Assignment\[com.snc.automatic\_assignment\]

</td><td class="description">

Allows any application that uses tables that are children of Task \[task\] to use auto-assignment to automatically find eligible assignees for any task.

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

 

</td></tr><tr><td>

Automation Center\[com.sn\_coe\]

 \(Available in the ServiceNow Store\)

</td><td>

Integrates islands of automation and delivers centralized governance and management of cross-enterprise, multi-vendor automation in a single workspace.

</td><td>

Active

</td><td>

true

</td><td>

sn\_cmdb\_ci\_class \(1.38.0\)

</td></tr><tr><td>

Automation Center\[com.sn\_ac\]

 \(Available in the ServiceNow Store\)

</td><td>

Manages and monitors your entire automation landscape.

</td><td>

Active

</td><td>

true

</td><td>

com.sn\_cmdb\_ci\_class

</td></tr><tr><td>

Automation Discovery\[sn\_auto\_discovery\]

 \(Available in the ServiceNow Store\)

</td><td>

Creates reports from your data to show opportunities for automation.

</td><td>

Active

</td><td>

false

</td><td>

-   com.glide.nlu
-   com.glide.platform\_ml

</td></tr><tr><td>

AWA Channel Management\[com.sn\_channel\_management\]

</td><td>

Main plugin that supports various functionalities for AWA Service Channels and Queues under Manager Workspace

</td><td>

Active

</td><td>

false

</td><td class="requires">

-   com.glide.awa
-   com.snc.wfo

</td></tr><tr><td>

Azure Active Directory User Mapping\[sn\_now\_azure\]

 \(Available in the ServiceNow Store\)

</td><td>

Contains workflows and mappings for ServiceNow user to Azure Active Directory user.

</td><td>

Inactive

</td><td>

false

</td><td>

-   com.glide.channelproxy
-   com.snc.msteams.app.core

</td></tr><tr><td>

Badge Reader Integration\[com.snc.badge\_reader\]

</td><td>

Badge Reader Integration Framework which allows other applications to integrate with badge reader hardware.

</td><td>

Inactive

</td><td>

false

</td><td>

 

</td></tr><tr><td>

Base Upgrade Logger\[com.glide.base\_upgrade\_logger\]

</td><td>

 

</td><td>

Active

</td><td>

false

</td><td class="requires">

-   com.glide.ui.mergetool
-   com.glide.ui.diagnostics

</td></tr><tr id="plugin_com.glide.system_export_set" class="plugin_reference"><td class="name">

Basic Export Set Functionality\[com.glide.system\_export\_set\]

</td><td class="description">

 

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

 

</td></tr><tr><td class="name">

Benchmark Client\[com.sn\_bm\_client\]

</td><td class="description">

Benchmark Insights for Customers.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

com.sn\_bm\_common

</td></tr><tr><td class="name">

Benchmark Common\[com.sn\_bm\_common\]

</td><td class="description">

Common code for Benchmark Insights.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

 

</td></tr><tr><td>

Benchmarks Spoke\[com.sn\_bm\_client.spoke\]

</td><td>

Contains the evaluation framework for Benchmarks Recommendations.

</td><td>

Active

</td><td>

false

</td><td>

com.glide.hub

</td></tr><tr id="plugin_com.snc.bestpractice.bulkchange" class="plugin_reference"><td class="name">

Best Practice - Bulk CI Changes\[com.snc.bestpractice.bulkchange\]

</td><td class="description">

This plugin is intended to be used with the legacy Change Management state models, which were used prior to the Geneva release. It allows CMDB updates to be proposed and applied to one or more in scope configuration items as part of your change management process.

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

 

</td></tr><tr id="plugin_com.snc.bestpractice.change_risk" class="plugin_reference"><td class="name">

Best Practice - Change Risk Calculator\[com.snc.bestpractice.change\_risk\]

</td><td class="description">

Simple risk and impact calculations for change management.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

 

</td></tr><tr id="plugin_com.snc.bestpractice.incident" class="plugin_reference"><td class="name">

Best Practice - Incident Resolution Workflow\[com.snc.bestpractice.incident\]

</td><td class="description">

Best practices for incident resolution dictate that rather than closing the incident, the incident should have a state of Resolved. This state gives the service desk a mechanism to verify that caller is satisfied with the resolution, and that the customer agrees with closing the incident.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

 

</td></tr><tr id="plugin_com.snc.bestpractice.itil_kpi" class="plugin_reference"><td class="name">

Best Practice - ITIL KPI Reports\[com.snc.bestpractice.itil\_kpi\]

</td><td class="description">

Provides a series of reports that track the Key Performance Indicators \(KPI\) of incident management and problem management.

</td><td>

Active

</td><td class="has_demo_data">

true

</td><td class="requires">

com.glide.metrics

</td></tr><tr><td>

Business Location\[com.snc.business\_location\]

</td><td>

This plugin supports a data model where the corporation does business with customers through physical channels such as stores and branches.

</td><td>

Active

</td><td>

true

</td><td class="requires">

-   com.snc.service\_organization
-   com.snc.cs\_base\_extension

</td></tr><tr><td>

Business Roles\[com.snc.businessroles\]

</td><td>

Activates the Business Roles module. Combined with other licensed applications, provides business roles and hierarchy for employees with integration to Okta for access provisioning during onboarding.

</td><td>

Inactive

</td><td>

false

</td><td>

com.sn\_content\_delivery

</td></tr><tr id="plugin_com.glide.business_rule_v2" class="plugin_reference"><td class="name">

Business Rule V2\[com.glide.business\_rule\_v2\]

</td><td class="description">

Enhances business rules to support script-free conditions and behaviors.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

 

</td></tr><tr><td class="name">

Business Stakeholder\[com.snc.business\_stakeholder\]

</td><td>

Contains the Business Stakeholder role which authorizes the users to approve, view/read records across the organization and view reports. Note there is a fee associated with the Business Stakeholder role. Do not assign it to users without confirming your organization has the appropriate entitlement.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

 

</td></tr><tr><td>

Cache build stats\[com.glide.stats.cache\_build\]

</td><td>

Cache build stats.

</td><td>

Active

</td><td>

false

</td><td>

com.glide.stats

</td></tr><tr><td>

Card Operations\[com.sn\_bom\_credit\_card\]

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Case Assignment Workbench Demo\[com.snc.case\_assignment\_workbench\_demo\]

</td><td>

Provides demo data, such as sample cases and users, so that the Assignment Workbench product features can be demonstrated on a non-production instance. Not for use on customer production instances.

</td><td>

Inactive

</td><td>

true

</td><td class="requires">

-   com.snc.customerservice.demo
-   com.snc.assignment\_workbench

</td></tr><tr><td>

Case Digests\[com.sn\_csm\_case\_digest\]

</td><td>

Enables users to send case status updates and root cause analysis to customers and key internal stakeholders.

</td><td>

Inactive

</td><td>

true

</td><td class="requires">

-   com.sn\_customerservice
-   com.sn\_csm\_doc\_template
-   com.snc.documentviewer
-   com.sn\_publications

</td></tr><tr><td>

Case Playbook for Complaints\[com.sn\_csm\_complaint\_caseflow\]

</td><td>

Provides a complaint case type to capture the details for a customer complaint and a playbook that provides step-by-step guidance through the lifecycle of the complaint.

</td><td>

Active

</td><td>

true

</td><td>

 

</td></tr><tr><td>

Case Playbook for Onboarding\[com.sn\_csm\_onboarding\_caseflow\]

</td><td>

Provides an onboarding case type to capture the details when onboarding customers for a product or service and a playbook that provides step-by-step guidance through the lifecycle of the onboarding process.

</td><td>

Active

</td><td>

true

</td><td>

 

</td></tr><tr><td>

Case Playbook for Product Support\[com.sn\_csm\_product\_support\_playbook\]

</td><td>

Case Flow for Product Support guides customer service agents through the steps needed to resolve product issues.

</td><td>

Active

</td><td>

true

</td><td>

 

</td></tr><tr id="plugin_com.glide.ui.ng.cc" class="plugin_reference"><td class="name">

Catalog Designer Common\[com.glide.ui.ng.cc\]

</td><td class="description">

Catalog Designer Common.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

-   com.glide.ui.ng.dc
-   com.glideapp.workflow

</td></tr><tr><td>

CCG Content Pack\[sn\_itom\_ccg\_cp\]

 \(Available in the ServiceNow Store\)

</td><td>

Provides the base system contents such as policies, resource collectors, configuration collectors, and remediation actions for the Cloud Configuration Governance application.

</td><td>

Active

</td><td>

false

</td><td>

-   com.snc.cloud.core
-   com.glide.hub.action\_step.payload
-   com.glide.hub.action\_step.script\_mid
-   com.snc.itom.license
-   com.glide.hub.action\_step.get\_connection\_info
-   com.glide.hub.action\_step.rest
-   com.glide.hub.action\_step.xmlparser
-   com.glide.hub.action\_type.datastream
-   com.glide.hub.integration.runtime

</td></tr><tr id="plugin_com.snc.central_dispatch" class="plugin_reference"><td class="name">

Central Dispatch\[com.snc.central\_dispatch\]

</td><td class="description">

Allows visually allocating tasks to agents for a logged in dispatcher.

</td><td>

Inactive

</td><td class="has_demo_data">

true

</td><td class="requires">

com.snc.dhtmlx.scheduler

</td></tr><tr><td>

Centralized Connection and Credential\[com.snc.core.automation.connection\_credential\]

</td><td>

Centralized Connection and Credential components.

</td><td>

Active

</td><td>

false

</td><td>

 

</td></tr><tr id="plugin_com.snc.certification_core" class="plugin_reference"><td class="name">

Certification Core\[com.snc.certification\_core\]

</td><td class="description">

Core certification structures such as filters and templates. Certification Core is activated automatically when any of these applications are activated: -   Desired State Certification \(active by default\)
-   Architecture Compliance
-   Data Certification
-   IT Governance Risk and Compliance

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

-   com.glide.list\_v2
-   com.snc.version

</td></tr><tr><td>

Change Management - Approval Policy\[sn\_chg\_pol\_appr\]

</td><td>

Change Management feature that helps in generating and configuring approvals using the Change Approval policies.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td>

 

</td></tr><tr><td>

Change Management - ATF Tests\[com.snc.change\_management.atf\]

</td><td>

This plugin loads ATF tests for Change Management when the Change Management - State Model plugin is active. The demo data for this plugin is required to successfully execute these ATF tests.

</td><td>

Inactive

</td><td class="has_demo_data">

true

</td><td>

 

</td></tr><tr><td>

Change Management - CAB Workbench\[com.snc.change\_management.cab\]

</td><td class="description">

Change Management feature which allows CAB Managers to schedule, plan and manage CAB Meetings all on the NOW platform.

</td><td>

Active

</td><td>

true

</td><td class="requires">

-   com.snc.change\_management.cab.form\_layout
-   com.snc.app.calendar
-   com.glide.service-portal
-   com.snc.app\_common.service\_portal
-   com.glide.editor.tinymce

</td></tr><tr><td>

Change Management - Case Intelligence\[com.snc.change\_management.ml.ccbc\]

</td><td>

Change Management feature that uses Predictive Intelligence to automatically identify cases that may have been caused by change.

</td><td>

Inactive

</td><td>

false

</td><td>

-   com.snc.change\_management.ml
-   com.sn\_customerservice

</td></tr><tr><td>

Change Management - Change Model Foundation Data\[com.snc.change\_management.change\_model.foundation\]

</td><td>

Foundation data for Change Models, including State transitions and supporting flows.

</td><td>

Active

</td><td>

false

</td><td>

-   com.snc.change\_management.change\_model
-   com.glide.hub

</td></tr><tr><td>

Change Management - Change Models\[com.snc.change\_management.change\_model\]

</td><td>

Change Models allow flexible configuration of state and transition models for Change Requests.

</td><td>

Active

</td><td>

false

</td><td>

-   com.snc.itsm.state\_transition\_model
-   com.snc.itsm.state\_transition\_model.foundation

</td></tr><tr><td>

Change Management - Change Models Landing\[com.snc.change\_management.change\_model.landing\]

</td><td>

Comprises the user interface used to create Change Requests based on Change Models.

</td><td>

Active

</td><td>

false

</td><td>

com.snc.change\_management.change\_model

</td></tr><tr><td>

Change Management - Foundation Data\[com.snc.change\_management.foundation\]

</td><td>

Provides the Change Management foundation data, new states, priorities.

</td><td>

Active

</td><td>

true

</td><td>

com.snc.change\_management

</td></tr><tr><td>

Change Management - Change Related Incidents \(Maintenance mode\)\[com.snc.change\_management.icbc\]

</td><td>

UI and configuration for Change Related Incidents Classic environment

</td><td>

Active

</td><td>

false

</td><td>

com.snc.change\_request

</td></tr><tr><td>

Change Management - Change Schedule\[com.snc.change\_management.soc\]

</td><td>

Change Schedule.

</td><td>

Active

</td><td>

false

</td><td class="requires">

-   com.snc.dhtmlx.gantt
-   com.snc.change\_request
-   com.snc.change\_management.soc.color\_picker

</td></tr><tr><td>

Change Management - Change Schedule foundation\[com.snc.change\_management.soc.foundation\]

</td><td>

Change Management - Change Schedule Foundation Data.

</td><td>

Active

</td><td>

false

</td><td>

com.snc.change\_management.soc

</td></tr><tr><td>

Change Management - Change Success Score\[com.snc.change\_management.change\_success\_score\]

</td><td>

Change Success Score is a numerical expression that represents the change success history for a particular group. It can be used to evaluate the likelihood of future success and help determine the level of change rigor required.

</td><td>

Active

</td><td>

 

</td><td class="requires">

-   com.snc.change\_request
-   com.snc.pa
-   com.snc.change\_management.change\_success\_score.foundation

</td></tr><tr id="plugin_com.snc.change.collision" class="plugin_reference"><td class="name">

Change Management - Collision Detector\[com.snc.change.collision\]

</td><td class="description">

Conflict Detection is a feature of the Change Management application that identifies potential scheduling conflicts based on the configuration items in scope for the change or user or group assigned to fulfill a change.

</td><td>

Active

</td><td class="has_demo_data">

true

</td><td class="requires">

com.snc.maintenance\_schedules

</td></tr><tr><td>

Change Management - Color Picker\[com.snc.change\_management.soc.color\_picker\]

</td><td>

Color Picker

</td><td>

Active

</td><td>

false

</td><td>

 

</td></tr><tr id="plugin_com.snc.change_management" class="plugin_reference"><td class="name">

Change Management - Core\[com.snc.change\_management\]

</td><td class="description">

Core change management plugin which both Change Management State Model and Standard Change Catalog plugins depend on.

 This plugin updates the **Type** field on Change Request to have the values **Normal**, **Standard**, and **Emergency**.

 The Type value on existing Change Requests is updated:

-   Routine com.glide.context\_help-&gt; standard \(Standard\)
-   Comprehensive -&gt; normal \(Normal\)
-   Emergency -&gt; emergency \(Emergency\)

 When creating a Change Request, an interceptor prompts you for the type of Change you want to create.

</td><td>

Active

</td><td class="has_demo_data">

true

</td><td class="requires">

-   com.snc.change\_request
-   com.snc.change.collision

</td></tr><tr><td>

Change Management - Incident Intelligence\[com.snc.change\_management.ml.icbc\]

</td><td>

Change Management feature that uses Predictive Intelligence to automatically identify incidents that may have been caused by change.

</td><td>

Active

</td><td>

false

</td><td class="requires">

-   com.snc.change\_management.ml
-   com.snc.change\_management.icbc

</td></tr><tr id="plugin_com.snc.change_management.mass_update_ci" class="plugin_reference"><td class="name">

Change Management - Mass Update CI\[com.snc.change\_management.mass\_update\_ci\]

</td><td class="description">

Change Management feature which allows change requesters to propose and apply updates associated with a change request to one or more configuration items in scope for a change.

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

-   com.snc.change\_management.state\_model
-   com.snc.bestpractice.bulkchange

</td></tr><tr><td>

Change Management - Predictive Intelligence Core \(maintenance mode\)\[com.snc.change\_management.ml\]

</td><td>

Core plugin containing the common components used by the Change Management Intelligence features.

</td><td>

Active

</td><td>

false

</td><td class="requires">

-   com.snc.change\_request
-   com.glide.platform\_ml

</td></tr><tr><td>

Change Management - Risk Assessment\[com.snc.change\_management.risk\_assessment\]

</td><td>

Change Management feature which allows risk assessment questionnaires to be created and required to drive the assessment of risk associated with a requested change.

</td><td>

Inactive

</td><td>

true

</td><td class="requires">

-   com.snc.bestpractice.change\_risk
-   com.snc.assessment\_core
-   com.glide.assessment\_designer

</td></tr><tr id="plugin_com.snc.change_management.standard_change_catalog" class="plugin_reference"><td class="name">

Change Management - Standard Change Catalog\[com.snc.change\_management.standard\_change\_catalog\]

</td><td class="description">

Change Management feature which allows Standard change templates to be proposed, approved, and published in the ServiceNow Service Catalog.

</td><td>

Active

</td><td class="has_demo_data">

true

</td><td class="requires">

-   com.snc.change\_management
-   com.glideapp.servicecatalog

</td></tr><tr id="plugin_com.snc.change_management.state_model" class="plugin_reference"><td class="name">

Change Management - State Model\[com.snc.change\_management.state\_model\]

</td><td class="description">

This plugin provides the current Change Management state models for Standard, Normal and Emergency change types, originally released in the Geneva release.

</td><td>

Active

</td><td class="has_demo_data">

true

</td><td class="requires">

-   com.snc.change\_management
-   com.snc.process\_flow\_formatter

</td></tr><tr><td>

Change Management - Success Probability \[com.snc.change\_management.success\_probability\]

 \(New in Tokyo\)

</td><td>

Calculates a probability to indicate what are the chances of the Change Requests completing successfully without issues.

</td><td>

Active

</td><td>

false

</td><td>

com.snc.change\_management.change\_success\_score

</td></tr><tr id="plugin_com.glideapp.report.itsm.change.overview" class="plugin_reference"><td class="name">

Change Management Overview Homepage\[com.glideapp.report.itsm.change.overview\]

</td><td class="description">

Activates a Change Management Overview Dashboard in the Change Management application navigator.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

com.glideapp.report

</td></tr><tr><td>

Change Management - Risk Intelligence \(maintenance only\)\[com.snc.change\_management.ml.risk\]

</td><td>

Change Management feature that augments existing risk assessment capabilities with Predictive Intelligence to predict change risk.

</td><td>

Active

</td><td>

false

</td><td>

com.snc.change\_management.ml

</td></tr><tr><td>

Change Management - Standard Change Template Intelligence\[com.snc.change\_management.ml.sctp\]

</td><td>

Change Management feature that uses Predictive Intelligence to identify change clusters that may be candidates for standard change templates.

</td><td>

Active

</td><td>

false

</td><td>

com.snc.change\_management.ml

</td></tr><tr id="plugin_com.glideapp.workflow_change_management" class="plugin_reference"><td class="name">

Change Management Workflows\[com.glideapp.workflow\_change\_management\]

</td><td class="description">

This plugin activates the workflows which control the change processes associated with the Emergency, Standard, and Normal change types introduced in the Geneva release.

</td><td>

Active

</td><td class="has_demo_data">

true

</td><td class="requires">

com.glideapp.workflow

</td></tr><tr id="plugin_com.snc.change_request" class="plugin_reference"><td class="name">

Change Request\[com.snc.change\_request\]

</td><td class="description">

The base Change Request plugin that contains the core tables for Change Management, including the change request and change task tables.

</td><td>

Active

</td><td class="has_demo_data">

true

</td><td class="requires">

com.glideapp.report.itsm.change.overview

</td></tr><tr><td>

Change Request Calendar\[com.snc.change\_request\_calendar\]

</td><td>

This plugin activates the Change Conflict Calendar introduced in the Kingston release. It enables you to view a change request and its potential conflicts once a primary configuration item, planned start date, and planned end date have been provided within a Change request.

</td><td>

Active

</td><td>

false

</td><td>

com.snc.app.calendar

</td></tr><tr><td>

Channel Proxy\[com.glide.channelproxy\]

</td><td>

Contains the Business Stakeholder role which authorizes the users to approve, view/read records across the organization and view reports. Note there is a fee associated with the Business Stakeholder role. Do not assign it to users without confirming your organization has the appropriate entitlement.

</td><td>

inactive

</td><td>

false

</td><td>

com.glide.external.app

</td></tr><tr id="plugin_com.glide.ui.checklist" class="plugin_reference"><td class="name">

Checklist\[com.glide.ui.checklist\]

</td><td class="description">

Provides a simple way to track the progress of tasks without creating additional records, using checklists that can be added to any form.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

-   com.glide.ui.ng
-   com.glide.rest.service

</td></tr><tr><td>

CI Metrics and Remediation - MECM Adapter\[sn\_mecm\_adapter\]

 \(Available in the ServiceNow Store\)

</td><td>

Enables you to retrieve and display the CI metrics information of the affected CIs.

</td><td>

Active

</td><td>

true

</td><td>

None

</td></tr><tr><td>

CIDC Spoke\[com.sn\_cicd\_spoke\]

</td><td>

Provides subflows and actions to call the Continuous Integration Continuous Delivery REST API endpoints included in the com.glide.continuousdelivery plugin.

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

CIWF UI Components\[com.sn\_ciwf\_ui\_cmpnt\]

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td class="name">

Client Transaction Timings\[com.glide.client\_transaction\]

</td><td class="description">

The Client Transaction plugin provides support to track client rendering times at the server, lining the values up with the server transaction times.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

 

</td></tr><tr><td>

Cloud Action Library\[sn\_itom\_cal\]

 \(Available in the ServiceNow Store\)

</td><td>

Use the ready-to-use actions and subflows of the Cloud Action Library application to interact with the cloud resources of the organization. The ITOM Governance features, such as Cloud Configuration Governance, use these actions to operate.

</td><td>

Active

</td><td>

false

</td><td>

-   com.snc.cloud.core
-   com.glide.hub.action\_step.payload
-   com.glide.hub.action\_step.script\_mid
-   com.snc.itom.license
-   com.glide.hub.action\_step.get\_connection\_info
-   com.glide.hub.action\_step.rest
-   com.glide.hub.action\_step.xmlparser
-   com.glide.hub.action\_type.datastream
-   com.glide.hub.integration.runtime
-   sn\_itom\_licensing

</td></tr><tr><td>

Cloud API\[com.snc.cloud.api\]

</td><td>

Cloud API Framework.

</td><td>

Inactive

</td><td>

false

</td><td class="requires">

-   com.snc.core.automation
-   com.glide.ui.angular
-   com.glide.ui.heisenberg
-   com.snc.discovery.core

</td></tr><tr><td>

Cloud Config Management\[com.snc.config.mgmt\]

</td><td>

Config Management Framework.

</td><td>

Inactive

</td><td>

false

</td><td class="requires">

-   com.glide.rest
-   com.snc.cloud.core

</td></tr><tr><td>

Cloud Configuration Governance\[com.sn.itom.ccg\]

 \(Available in the ServiceNow Store\)

</td><td>

Use the application to check the configuration settings of cloud resources in your organization against a set of policies to identify violations. After identifying the violation, use remediation workflows to mitigate them.

</td><td>

Active

</td><td>

false

</td><td>

-   com.snc.cloud.core
-   com.glide.hub.action\_step.payload
-   com.glide.hub.action\_step.script\_mid
-   com.glide.hub.action\_step.get\_connection\_info
-   com.snc.itom.license
-   com.glide.hub.action\_step.rest
-   com.glide.hub.action\_step.xmlparser
-   com.glide.hub.action\_type.datastream
-   com.glide.hub.integration.runtime
-   sn\_itom\_licensing
-   sn.itom.cal

</td></tr><tr><td>

Cloud Configuration Governance: Content Pack\[com.sn.itom.ccg.cp\]

 \(Available in the ServiceNow Store\)

</td><td>

Provides the base-system policies, subflows, and flow designer actions for the Cloud Configuration Governance application.

</td><td>

Active

</td><td>

false

</td><td>

com.sn.itom.ccg

</td></tr><tr><td>

Cloud Insights Billing\[sn\_clin\_billing\]

 \(Available in the ServiceNow Store\)

</td><td>

Provides the tools to download the billing data for the provisioned Amazon Web Services \(AWS\) and Microsoft Azure resources and visualize the data in a dashboard. Use Cloud Insights Billing along with Cloud Provisioning and Governance running only on non-domain-separated instances.

</td><td>

Active

</td><td>

false

</td><td>

-   Plugin dependencies:
    -   Orchestration
    -   com.snc.cloud.api
    -   com.snc.cmdb.scoped
    -   com.itom.jutils
    -   com.snc.clotho
    -   com.snc.ng.pattern.designer
    -   com.glide.hub.integrations
-   Application dependencies:
    -   sn\_itom\_pattern
    -   sn\_cmdb\_ci\_class
    -   sn\_cai
    -   sn\_cld\_intg\_core
    -   sn\_cld\_intg\_aws
    -   sn\_cld\_intg\_azure
    -   sn\_cld\_intg\_gcp
    -   sn\_cld\_spend\_core
    -   sn\_cld\_spend\_aws
    -   sn\_cld\_spend\_azure
    -   sn\_cld\_spend\_gcp

</td></tr><tr><td>

Cloud Migration Assessment\[com.sn\_cloud\_migration\]

 \(Available in the ServiceNow Store\)

</td><td>

Allows you to plan, organize, and track the process of relocating your enterprise IT resources and workloads to cloud platforms.

</td><td>

Inactive

</td><td>

true

</td><td>

-   com.sn\_cloud\_mig\_base
-   com.sn\_itom\_licensing
-   com.snc.discovery

</td></tr><tr><td>

Cloud Migration Base\[com.sn\_cloud\_mig\_base\]

 \(Available in the ServiceNow Store\)

</td><td>

A base plugin for the Cloud Migration Assessment application.

</td><td>

Inactive

</td><td>

false

</td><td>

None

</td></tr><tr><td>

Cloud Operations Workspace\[com.cloud\_operations\_workspace\]

 \(Available in the ServiceNow Store\)

</td><td>

Offers a comprehensive solution to manage the cloud operations of your organization.

</td><td>

Active

</td><td>

false

</td><td>

-   com.snc.cloud.core
-   com.snc.ng.pattern.designer

</td></tr><tr><td>

Cloud Provisioning and Governance \[com.snc.cloud.mgmt\]

</td><td>

Cloud Provisioning and Governance - Integration with AWS, Azure, VMware OOB and extensible to add support for new clouds.

</td><td>

Inactive

</td><td>

false

</td><td class="requires">

-   com.glide.service-portal
-   com.snc.cloud.core
-   com.snc.config.mgmt
-   com.snc.runbook\_automation

</td></tr><tr><td>

Cloud Provisioning and Governance Core\[com.snc.cloud.core\]

</td><td>

Cloud Provisioning and Governance Core - Discovery and Resource Blocks.

</td><td>

Inactive

</td><td>

false

</td><td class="requires">

-   com.snc.discovery.core
-   com.snc.cloud.api

</td></tr><tr><td>

Cloud Provisioning and Governance: Google Cloud Connector \[sn\_cmp\_gcp\]

 \(Available in the ServiceNow Store\)

</td><td>

Enables integration with Google Cloud Platform.

</td><td>

Active

</td><td>

false

</td><td>

-   com.snc.cloud.mgmt
-   com.snc.pattern.designer
-   com.snc.ng.pattern.designer

</td></tr><tr><td>

Cloud Provisioning and Governance: Terraform Connector\[sn\_cmp\_terraform\]

 \(Available in the ServiceNow Store\)

</td><td>

Offers ability to provision to AWS, Azure, VMware and IBM Cloud. Develop at speed, ingest your Infrastructure as Code \(IaC\) template and create a ServiceNow catalog item in minutes.

</td><td>

Active

</td><td>

false

</td><td>

com.snc.cloud.mgmt

</td></tr><tr><td>

Cloud Spend Dashboard\[sn\_sam\_cld\_spend\]

 \(Available in the ServiceNow Store\)

</td><td>

This plugin provides Insights into SaaS, IaaS and PaaS Spend and Savings

</td><td>

Active

</td><td>

false

</td><td class="requires">

-   com.snc.cloud.api
-   com.snc.cmdb.scoped
-   com.snc.discovery
-   com.itom.jutils
-   com.sn\_itom\_opt\_licensing
-   com.snc.clotho
-   com.glide.hub.integration.runtime
-   com.glide.hub.integrations.standard
-   com.sn\_sam\_saas

</td></tr><tr><td>

CMDB-ATF Tests\[com.snc.cmdb.atf\]

</td><td>

Provides the CMDB Automated Test Framework \(ATF\) tests.

</td><td>

Inactive

</td><td>

false

</td><td>

com.snc.cmdb

</td></tr><tr><td>

CMDB and CSDM Data Foundations Dashboard\[sn\_getwell\]

 \(Available in the ServiceNow Store\)

</td><td>

Provides insights into the key foundational indicators of your CMDB and Common Service Data Model \(CSDM\) as well as recommendations to ensure that the CMDB and CSDM are properly configured for optimal usage and to mitigate any potential risks.

</td><td>

Active

</td><td>

false

</td><td>

None

</td></tr><tr><td>

CMDB Dashboard\[com.snc.cmdb.dashboard\]

</td><td>

Report overall CMDB and class level aggregated CI health.

</td><td>

Active

</td><td>

false

</td><td class="requires">

-   com.snc.cmdb
-   com.snc.pa
-   com.glideapp.canvas

</td></tr><tr><td>

CMDB Group\[com.snc.cmdb.group\]

</td><td>

Provides Configuration Item grouping capabilities.

</td><td>

Active

</td><td>

false

</td><td>

 

</td></tr><tr><td>

CMDB Group Dashboard\[com.snc.cmdb.group.dashboard\]

</td><td>

Report the health of CIs in CMDB Groups, on a dashboard.

</td><td>

Active

</td><td>

false

</td><td class="requires">

-   com.snc.cmdb
-   com.snc.pa
-   com.glideapp.canvas
-   com.snc.cmdb.group

</td></tr><tr id="plugin_com.snc.cmdb.mainframe" class="plugin_reference"><td class="name">

CMDB Mainframe\[com.snc.cmdb.mainframe\]

</td><td class="description">

One of the plugins included in the Extended CMDB plugin, used for mainframe configuration items.

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

com.snc.cmdb

</td></tr><tr id="plugin_com.snc.cmdb.radio.category" class="plugin_reference"><td class="name">

CMDB Radio Category\[com.snc.cmdb.radio.category\]

</td><td class="description">

One of the plugins included in the Extended CMDB plugin, used for radio configuration items.

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

com.snc.cmdb

</td></tr><tr><td>

CMDB Search\[com.snc.cmdb\_search\]

</td><td>

Query-like search on CMDB CIs and relationships. Converts a free-style query with configurable synonyms and stop words, into a properly formulated query on CMDB tables.

</td><td>

Active

</td><td>

false

</td><td>

com.snc.cmdb

</td></tr><tr id="plugin_com.snc.cmdb.telecom.category" class="plugin_reference"><td class="name">

CMDB Telecom Category\[com.snc.cmdb.telecom.category\]

</td><td class="description">

One of the plugins included in the Extended CMDB plugin, used for telecom configuration items.

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

com.snc.cmdb

</td></tr><tr id="plugin_com.snc.cmdb.test.equipment" class="plugin_reference"><td class="name">

CMDB Test Equipment\[com.snc.cmdb.test.equipment\]

</td><td class="description">

One of the plugins included in the Extended CMDB plugin, used for test equipment configuration items.

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

com.snc.cmdb

</td></tr><tr><td>

CMDB Agent Workspace\[com.cmdb-workspace\]

</td><td>

Enables CMDB capabilities in Agent Workspace.

</td><td>

Active

</td><td>

false

</td><td>

com.snc.agent\_workspace.itsm

</td></tr><tr id="plugin_com.snc.service_management.core.cms" class="plugin_reference"><td class="name">

CMS User Interface - Service Management Core\[com.snc.service\_management.core.cms\]

</td><td class="description">

All Content Management System items \(blocks, pages, and menus\) used to reference core IT self-service applications are packaged in this plugin. It is also the core foundation for all Service Management applications.

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

-   com.glide.cms
-   com.glide.cms.extensions
-   com.glide.db\_images

</td></tr><tr><td>

CMDB Workspace\[sn\_cmdb\_ws\]

 \(Available in the ServiceNow Store\)

</td><td>

A modern workspace where you can search the CMDB, understand CMDB health and CIs and access common tools

</td><td>

Active

</td><td>

true

</td><td>

-   sn\_cmdb\_pg\_templts
-   sn-cmdb-nlq-search

</td></tr><tr><td>

Coaching\[com.sn\_coaching\]

</td><td>

The Coaching module facilitates the coaching of employees on their work through the use of coaching opportunities \(critical moments in a process\) that can be conditionally configured.

</td><td>

Active

</td><td>

true

</td><td class="requires">

-   com.snc.planned\_task\_v2
-   com.snc.skills\_management
-   com.snc.organization\_management

</td></tr><tr id="plugin_com.glide.code-search" class="plugin_reference"><td class="name">

Code Search\[com.glide.code-search\]

</td><td class="description">

A configurable Code Search API.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

 

</td></tr><tr id="plugin_com.glide.collaboration" class="plugin_reference"><td class="name">

Collaboration\[com.glide.collaboration\]

</td><td class="description">

Retired. Replaced by the Connect plugin.

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

com.glide.connect

</td></tr><tr><td>

Collaboration Services\[sn\_tcm\_collab\_hook\]

 \(Available in the ServiceNow Store\)

</td><td>

Provides the ability to communicate over Slack. The application integrates collaboration tools with ServiceNow. You can directly use a collaboration tool from task records and as a channel within communication plans. You can Initiate a conversation from a task record with the collaboration tool of your choice. Enable Collaboration Services for communication plans to pre-define Slack or Microsoft Teams as a real-time collaboration and communication channel.

</td><td>

Inactive

</td><td>

false

</td><td>

None

</td></tr><tr><td>

Collision APIs\[com.glide.collision\_detector\]

</td><td>

APIs for predicting the behavior of the upgrade engine with regard to customizations.

</td><td>

Active

</td><td>

false

</td><td>

 

</td></tr><tr id="plugin_com.glide.encryption" class="plugin_reference"><td class="name">

Field Encryption\[com.glide.now.platform.encryption\]

</td><td class="description">

Allows text fields and attached files to be encrypted.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

com.glide.encryption.core

</td></tr><tr><td>

Column Statistics\[com.glide.column\_statistics\]

</td><td>

Column statistics used to suggest database indexes.

</td><td>

Active

</td><td>

true

</td><td>

 

</td></tr><tr><td>

Commercial Lines Claims\[com.sn\_ins\_claim\_cml\]

 \(Available in the ServiceNow Store\)

</td><td>

Commercial claims process digitization from First Notice of Loss \(FNOL\) through settlement.

</td><td>

Active

</td><td>

true

</td><td>

-   com.snc.csm\_contributor\_user
-   sn\_csm\_playbook \(2.0.2\)
-   sn\_bom \(1.8.0\)
-   sn\_ins\_siu \(1.0.0\)

</td></tr><tr><td>

Commercial Lines Servicing\[com.sn\_ins\_policy\_b2b\]

</td><td>

Enables insurance carriers to be agile and responsive in resolving mid-term policy changes and requests from commercial customers. Carriers can prioritize underwriting cases by premium value with intelligent business rules and eliminate low-value manual work from underwriting queues.

</td><td>

 

</td><td>

Yes

</td><td>

-   com.sn\_csm\_playbook
-   com.snc.csm\_contributor\_user
-   com.sn\_bom
-   com.sn\_bom\_document
-   com.sn\_ins\_uw\_b2b

</td></tr><tr><td>

Commercial Lines Underwriting\[com.sn\_ins\_uw\_b2b\]

</td><td>

Enables insurance carriers to route complex service requests instantly to underwriters based on their existing underwriting guidelines and rules. Underwriters can collaborate with distribution and servicing teams through an efficient and transparent workflow.

</td><td>

 

</td><td>

No

</td><td>

-   com.snc.csm\_contributor\_user
-   com.sn\_bom

</td></tr><tr><td>

Common ITSM Service Portal Application Components\[com.snc.app\_common.service\_portal\]

</td><td>

Common Application Components for Service Portal.

</td><td>

Active

</td><td>

false

</td><td>

com.glide.service-portal

</td></tr><tr><td>

Communities\[com.sn\_communities\]

</td><td>

Communities enable customers to interact with each other and share knowledge. There is no structured way to disseminate knowledge or capture knowledge from communities and make it a part of customer service and customer success.

</td><td>

Inactive

</td><td>

false

</td><td class="requires">

-   com.glide.service-portal
-   com.sn\_communities\_global
-   com.snc.activity\_subscriptions
-   com.snc.gamification
-   com.snc.csm\_unified\_theme
-   com.snc.assignment\_workbench
-   com.glide.processor.ics

</td></tr><tr><td>

Communities Demo Data\[com.sn\_communities\_demo\]

</td><td>

Loads demo data for the community application.

</td><td>

Inactive

</td><td>

false

</td><td class="requires">

-   com.sn\_communities
-   com.snc.csm\_unified\_theme.demo

</td></tr><tr id="plugin_com.glide.company" class="plugin_reference"><td class="name">

Company extension\[com.glide.company\]

</td><td class="description">

Adds currency columns to the Company \[core\_company\] table.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

com.glide.currency

</td></tr><tr><td>

Configuration Compliance\[snc\_vulc\]

 \(Available in the ServiceNow Store\)

</td><td>

Exposes your high-impact configuration-related security vulnerabilities, and orchestrates their remediation across frequently isolated information security, IT operations, and business process areas. Activation of this plugin on production instances may require a separate license. Contact ServiceNow for details.

</td><td>

Inactive

</td><td>

true

</td><td>

com.snc.security\_support.common

</td></tr><tr><td>

Configuration Compliance Dependencies\[snc\_vulc\_dep\]

</td><td>

System dependencies required by Configuration Compliance. Activation of this plugin on production instances may require a separate license. Contact ServiceNow for details.

</td><td>

 

</td><td>

false

</td><td>

 

</td></tr><tr id="plugin_com.snc.cmdb.enterprise" class="plugin_reference"><td class="name">

Configuration Management \(CMDB Enterprise Edition\)\[com.snc.cmdb.enterprise\]

</td><td class="description">

A collection of modules for specialized configuration items, such as radio hardware, test equipment, and voice system hardware.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

com.snc.cmdb

</td></tr><tr id="plugin_com.snc.cmdb" class="plugin_reference"><td class="name">

Configuration Management \(CMDB\)\[com.snc.cmdb\]

</td><td class="description">

Provides core functionality for the configuration management database, including enterprise hardware and configuration item relationships.

</td><td>

Active

</td><td class="has_demo_data">

true

</td><td class="requires">

-   com.glide.custom\_web\_service
-   com.sn\_cmdb\_content
-   com.snc.db.rotation
-   com.glide.ui.list\_v3\_components

</td></tr><tr><td class="name">

Configuration Management For Scoped Apps \(CMDB\)\[com.snc.cmdb.scoped\]

</td><td class="description">

Enables scoped apps access to Identification Engine APIs.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

com.snc.cmdb.enterprise

</td></tr><tr id="plugin_com.glide.connect" class="plugin_reference"><td class="name">

Connect\[com.glide.connect\]

</td><td class="description">

Provides a real-time messaging platform that connects you to your coworkers, bypassing email and static documents.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

-   com.glideapp.live\_feed
-   com.glideapp.live\_common
-   com.glide.ui.ng
-   com.glide.ui.angularui
-   com.glide.ui.ng.amb
-   com.glide.notification.push
-   com.glide.db\_audio

</td></tr><tr><td>

Connect Interaction UI\[com.connect-interaction-ui\]

</td><td>

User interface components to adapt Connect Support to use the interaction table as a source of truth.

</td><td>

inactive

</td><td>

false

</td><td class="requires">

-   com.glide.interaction
-   com.glide.graphql
-   com.glide.connect.support
-   com.glide.connect.ui\_components

</td></tr><tr><td>

Connect Scriptable APIs\[com.glide.connect.scriptable\]

</td><td>

Scriptable APIs for Connect.

</td><td>

Active

</td><td>

false

</td><td>

 

</td></tr><tr><td>

Connect Service Portal Widgets\[com.glide.connect.sp\_widgets\]

</td><td>

Connect Service Portal Widgets.

</td><td>

Inactive

</td><td>

false

</td><td class="requires">

-   com.glide.service-portal
-   com.glide.connect
-   com.glide.connect.ui\_components

</td></tr><tr><td>

Connect Spoke for Flow Designer\[com.glide.connect\_v3plus.core.ah\]

</td><td>

The Connect Spoke for the Flow Designer provides actions that a process analyst can use when designing flows. The actions allow them to automate the creation of conversations, to add users to a conversation, and to send messages to a conversation. These actions work with Connect API version 3 and later.

</td><td>

Active

</td><td>

false

</td><td>

com.glide.connect.scriptable

</td></tr><tr id="plugin_com.glide.connect.support" class="plugin_reference"><td class="name">

Connect Support\[com.glide.connect.support\]

</td><td class="description">

Builds on the Connect messaging platform and enables support agents to provide real-time assistance to end users, using queues.

</td><td>

Inactive

</td><td class="has_demo_data">

true

</td><td class="requires">

com.glide.connect

</td></tr><tr id="plugin_com.glide.connect.support.service-portal" class="plugin_reference"><td class="name">

Connect Support and Service Portal Integration\[com.glide.connect.support.service-portal\]

</td><td class="description">

Adds Connect Support components for use in the Service Portal.

</td><td>

Inactive

</td><td class="has_demo_data">

true

</td><td class="requires">

-   com.glide.service-portal
-   com.glide.connect.support

</td></tr><tr id="plugin_com.glide.connect.managers_dashboard" class="plugin_reference"><td class="name">

Connect Support Manager's Dashboard\[com.glide.connect.managers\_dashboard\]

</td><td class="description">

Provides a homepage and all the configuration records required to analyze Connect Support in reporting.

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

com.glideapp.report

</td></tr><tr><td>

Connect Support Routing\[com.glide.connect.support.routing\]

</td><td>

Plugin to enable processor for Routing Connect Support request to appropriate Chat Queue.

</td><td>

Inactive

</td><td>

false

</td><td class="requires">

-   com.snc.matching\_rule
-   com.glide.connect.support

</td></tr><tr><td>

Consumer Service Portal\[com.glide.service-portal.consumer-portal\]

</td><td>

Enables the Consumer Service Portal, a web-based portal based on the Service Portal application that your company can use to provide information and support to consumers.

</td><td>

Inactive

</td><td>

false

</td><td class="requires">

-   com.glide.service-portal.customer-service-base
-   com.glide.connect.anonymous\_support

</td></tr><tr><td>

Contact Center Integration Core \[sn\_ct\_ctr\_it\_core\] \(Available in the ServiceNow Store\[var.store-name\]\)

</td><td>

This plugin allows admins to automatically import data from a third party contact center as a service \(CCaaS\) application in order to facilitate external routing and third party telephony integration.

</td><td>

Active

</td><td>

true

</td><td>

-   Application spoke selector \[sn\_appss\]
-   External Agent Management Util Pack \[sn\_external\_agent\]
-   com.glide.cs.custom.adapter
-   com.glide.hub

</td></tr><tr><td>

Content Analytics\[com.sn\_content\_analytics\]

</td><td>

Content Analytics

</td><td>

Active

</td><td>

false

</td><td>

com.glide.scope.access.restricted\_caller

</td></tr><tr><td>

Content Automation\[com.sn\_content\_automation\]

</td><td>

Content automation functionality.

</td><td>

inactive

</td><td>

true

</td><td class="requires">

-   com.sn\_content\_delivery
-   com.glide.scope.access.restricted\_caller

</td></tr><tr><td>

Content Delivery\[com.sn\_content\_delivery\]

</td><td>

Content Delivery

</td><td>

inactive

</td><td>

true

</td><td class="requires">

-   com.glide.db\_images
-   com.glide.scope.access.restricted\_caller
-   com.glide.service-portal

</td></tr><tr><td>

Content Experiences\[com.sn\_content\_automation\]

</td><td>

Set up and package your content into a campaign using multiple channels to deliver the right message to the right audience at the right time.

</td><td>

Active

</td><td>

true

</td><td>

 

</td></tr><tr><td>

Content Governance\[sn\_cg\]

</td><td>

Content Governance provides communication employees a streamlined method to request content to be created for Content Publishing or Content Experiences.

</td><td>

Active

</td><td>

true

</td><td>

com.sn\_content\_publishing\_store

</td></tr><tr id="plugin_com.glide.cms" class="plugin_reference"><td class="name">

Content Management\[com.glide.cms\]

</td><td class="description">

Allows administrators to create custom, branded, web user interfaces on top of an existing ServiceNow instance.Use Service Portal for new development instead of CMS. Service Portal is an alternative to CMS with a refined user experience, and is active by default in the base system. For more information, see [Service Portal](https://www.servicenow.com/docs/access?context=c_ServicePortal&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US) and [Content Management and Service Portal](https://www.servicenow.com/docs/access?context=c_CMSAndSP&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US).

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

-   com.glideapp.home
-   com.glide.text\_search
-   com.glide.db\_images

</td></tr><tr id="plugin_com.glide.cms.types" class="plugin_reference"><td class="name">

Content Management Extended Types\[com.glide.cms.types\]

</td><td class="description">

An extension to Content Management that adds iFrames and Flash frames.Use Service Portal for new development instead of CMS. Service Portal is an alternative to CMS with a refined user experience, and is active by default in the base system. For more information, see [Service Portal](https://www.servicenow.com/docs/access?context=c_ServicePortal&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US) and [Content Management and Service Portal](https://www.servicenow.com/docs/access?context=c_CMSAndSP&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US).

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

-   com.glide.cms.type.flash
-   com.glide.cms.type.iframe

</td></tr><tr><td>

Content Publishing\[com.sn\_content\_publishing\_store\]

</td><td>

Content Publishing allows you to communicate with your employees using different methods.

</td><td>

Active

</td><td>

true

</td><td>

 

</td></tr><tr id="plugin_com.glide.sorting" class="plugin_reference"><td class="name">

Context Ranking\[com.glide.sorting\]

</td><td class="description">

Support for drag-and-drop lists and ranking dialog. Context ranking allows a user to sort a collection of records independently of the attributes of those records. Context Ranking is activated automatically with the SDLC - Scrum Process Pack plugin.

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

com.glide.list\_v2

</td></tr><tr id="plugin_com.glide.context_help" class="plugin_reference"><td class="name">

Context-Sensitive Help\[com.glide.context\_help\]

</td><td class="description">

Provides a context-sensitive help system, providing links to specific help pages. These help pages can be linked to the list or form view of any table, or to the form view of a specific record in a table.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

 

</td></tr><tr><td>

Context-Sensitive Help Rest API\[com.glide.context\_help.rest\_api\]

</td><td>

REST API for the context-sensitive help system

</td><td>

Active

</td><td>

false

</td><td class="requires">

-   com.glide.context\_help
-   com.glide.scripted\_rest\_services

</td></tr><tr id="plugin_com.snc.contextual_search" class="plugin_reference"><td class="name">

Contextual Search\[com.snc.contextual\_search\]

</td><td class="description">

Display related articles or service catalog items within a form or record producer.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

com.snc.application.json\_service

</td></tr><tr><td>

Contextual Search - Internal\[com.snc.contextual\_search.internal\]

</td><td>

An internal plugin component for Contextual Search.

</td><td>

Active

</td><td>

false

</td><td>

 

</td></tr><tr><td>

Contextual Search - Service Portal\[com.snc.contextual\_search.service-portal\]

</td><td>

Service Portal components for Contextual Search.

</td><td>

Active

</td><td>

false

</td><td class="requires">

-   com.snc.contextual\_search
-   com.snc.app\_common.service\_portal

</td></tr><tr id="plugin_com.glide.role_management" class="plugin_reference"><td class="name">

Contextual Security: Role Management\[com.glide.role\_management\]

</td><td class="description">

Provides the flexibility and power to protect information by controlling read/write/create/delete authorization.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

-   com.glide.db\_view
-   com.glide.ui\_page

</td></tr><tr id="plugin_com.glide.role_management.inh_count" class="plugin_reference"><td class="name">

Contextual Security: Role Management V2\[com.glide.role\_management.inh\_count\]

</td><td class="description">

Prevents duplicate entries in sys\_user\_has\_role for inherited roles, based on the value of the inh\_count column.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

com.glide.role\_management

</td></tr><tr id="plugin_com.glide.role_management.inh_count.rest_api" class="plugin_reference"><td class="name">

Contextual Security: Role Management V2 REST API\[com.glide.role\_management.inh\_count.rest\_api\]

</td><td class="description">

Prevents duplicate entries in sys\_user\_has\_role for inherited roles, based on the value of the inh\_count column.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

-   com.glide.role\_management.inh\_count
-   com.glide.scripted\_rest\_services

</td></tr><tr><td>

Continual Improvement Management \(CIM\)\[com.sn\_cim\]

</td><td>

Core plugin for Continual Improvement Management \(CIM\)

</td><td>

Active

</td><td>

true

</td><td class="requires">

-   com.snc.organization\_management
-   com.snc.planned\_task\_v2
-   com.snc.pa
-   com.snc.pa.spotlight
-   com.sn\_coaching
-   com.sn\_cim\_atf

</td></tr><tr><td>

Continual Improvement Management Automated Tests\[com.sn\_cim\_atf\]

</td><td>

ATF plugin for Continual Improvement Management \(CIM\)

</td><td>

Active

</td><td>

true

</td><td>

 

</td></tr><tr id="plugin_com.snc.contract_management" class="plugin_reference"><td class="name">

Contract Management\[com.snc.contract\_management\]

</td><td class="description">

Provides the ability to manage all types of contracts.

</td><td>

Active

</td><td class="has_demo_data">

true

</td><td class="requires">

com.snc.asset\_management

</td></tr><tr><td>

Contract Management - Form Layouts and Behavior\[com.snc.contract\_management.form\_layouts\]

</td><td>

Provides the ability to customize the Contract Management form layout.

</td><td>

Inactive

</td><td>

false

</td><td>

 

</td></tr><tr><td>

Conversation Branding Settings\[com.glide.cs.branding\]

</td><td>

Conversation Branding Settings for web chat client.

</td><td>

Active

</td><td>

false

</td><td>

 

</td></tr><tr><td>

Conversation General Settings\[com.glide.cs.settings\]

</td><td>

Conversation General Settings for Virtual Agent.

</td><td>

Active

</td><td>

false

</td><td>

 

</td></tr><tr><td>

Conversational Analytics\[sn\_ci\_analytics\]

 \(Available in the ServiceNow Store\)

</td><td>

A dashboard that helps you improve Virtual Agent \(VA\) interactions with users by providing deep insights into conversational data, discover which topics confuse users, and find out where users often transfer to live agents.

</td><td>

Active

</td><td>

false

</td><td>

-   com.glide.cs
-   com.glide.appsee

</td></tr><tr><td>

Conversational Integration with Alexa\[com.sn.va.alexa\]

 \(Available in the ServiceNow Store\)

</td><td>

Enables Virtual Agent to interact with requesters through the Amazon Alexa's voice interface using the Virtual Agent topics.

</td><td>

Active

</td><td>

false

</td><td>

 

</td></tr><tr><td>

Conversational Integration with LINE\[sn\_va\_line\]

</td><td>

The plugin helps engage with requesters who prefer the LINE messaging app to interact with your business. Requesters include customer contacts and consumers.

</td><td>

Active

</td><td>

true

</td><td>

-   com.glide.cs.custom.adapter
-   com.glide.hub.integration.runtime
-   com.snc.ihub\_spoke\_util\_pack
-   sn\_agent\_initiated

</td></tr><tr><td>

Conversational Integration with Microsoft Teams\[sn\_va\_teams\]

 \(Available in the ServiceNow Store\)

</td><td>

Enable requesters to chat with Microsoft Teams or live agents using the Microsoft Teams application.

</td><td>

Active

</td><td>

true

</td><td>

 

</td></tr><tr><td>

Conversational Interfaces - Diagnostics\[sn\_ci\_diagnostics\]

</td><td>

The CI Diagnostic Tool is a framework that allows a privileged user \(admin\) to perform a diagnosis of various products through scripts and powerful VA topics.

</td><td>

Active

</td><td>

false

</td><td>

com.glide.cs.chatbot.lite

</td></tr><tr><td>

Virtual Agent Topic Recommendations\[sn\_topic\_recommend\]

</td><td>

The plugin helps identify pre-built Virtual Agent topics that can be quickly implemented in your organization.

</td><td>

Active

</td><td>

false

</td><td>

 

</td></tr><tr><td>

Conversational Integration with WhatsApp \(powered by Twilio\)\[sn\_va\_whatsapp\_twi\]

</td><td>

The plugin enables customer engagement over the WhatsApp messaging app.

</td><td>

Active

</td><td>

true

</td><td>

-   sn\_twilio\_spoke
-   com.glide.hub.integration.runtime
-   com.glide.cs.custom.adapter
-   sn\_agent\_initiated
-   com.glide.cobject
-   com.glide.messaging.awa

</td></tr><tr><td>

Bot Interconnect\[sn\_va\_bot\_ic\]

\(Available in the ServiceNow Store\)

</td><td>

Virtual Agent Bot Interconnect functions as the primary bot in a diverse chat environment. It can help you reduce complexity and create a unified chat experience for your end users. Virtual Agent Bot Interconnect gives your end users access to multiple channels and a wide variety of enterprise tasks that are available from ServiceNow.

</td><td>

Active

</td><td>

false

</td><td>

com.glide.cs.chatbot

</td></tr><tr><td>

Conversational integration with Slack\[sn\_va\_slack\]

 \(Available in the ServiceNow Store\)

</td><td>

Enable requesters to chat with Virtual Agent or live agents using the Slack application

</td><td>

Active

</td><td>

false

</td><td>

 

</td></tr><tr><td>

Conversational integration with Workplace from Facebooksn\_va\_fb\_workplace

 \(Available in the ServiceNow Store\)

</td><td>

Enable requesters to chat with Virtual Agent or live agents using the Workplace from Facebook application.

</td><td>

Active

</td><td>

false

</td><td>

 

</td></tr><tr><td>

Conversational Integration with Facebook Messengersn\_va\_fb\_messenger

 \(Available in the ServiceNow Store\)

</td><td>

Enables users to interact with virtual and live agents using the Facebook Messenger application.

</td><td>

Active

</td><td>

true

</td><td>

 

</td></tr><tr><td>

Conversational IVR with Amazon Connect\[com.sn.va.amz.connect\]

 \(Available in the ServiceNow Store\)

</td><td>

Enables users to conduct conversations with a bot via the phone channel, in an interactive voice response.

</td><td>

Active

</td><td>

false

</td><td>

Virtual Agent API \(sn\_va\_as\_service\)

</td></tr><tr><td>

Virtual Agent APIsn\_va\_as\_service

 \(Available in the ServiceNow Store\)

</td><td>

Integrates any chat interface or a bot with Virtual Agent or Agent Chat.

</td><td>

Active

</td><td>

false

</td><td>

-   com.glide.cs.custom.adapter
-   com.glide.cs
-   com.glide.cs.chatbot
-   com.snc.ihub\_spoke\_util\_pack
-   com.sn\_ext\_agent\_management\_util

</td></tr><tr><td>

Conversational Interfaces Guided Setup\[com.glide.ci\_guided\_setup\]

</td><td>

Provides customers with a visual guidance to configure Conversational Interfaces.

</td><td>

Active

</td><td>

false

</td><td>

-   com.snc.guided\_setup
-   com.glide.guided\_setup\_config

</td></tr><tr><td>

Conversational Interfaces Landing Page\[com.glide.cs.landing\_experience\]

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Conversational Interfaces Settings\[com.glide.cs.admin\_console\]

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Conversational Messaging\[com.glide.messaging.awa\]

</td><td>

Conversational Messaging

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Conversational SMS Integration with Twilio\[com.sn.va.sms.twilio\]

 Maintenance mode

</td><td>

Integration to SMS for Advanced Work Assignment

</td><td>

Active

</td><td>

 

</td><td>

 

</td></tr><tr id="plugin_com.glide.rest.cors" class="plugin_reference"><td class="name">

CORS support for REST API\[com.glide.rest.cors\]

</td><td class="description">

CORS support for REST API

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

 

</td></tr><tr id="plugin_com.snc.cost_management" class="plugin_reference"><td class="name">

Cost Management\[com.snc.cost\_management\]

</td><td class="description">

Tracks operating costs for configuration items and task-related activities, allocates the costs to business consumers, and compares actual allocations to planned budgets.

</td><td>

Inactive

</td><td class="has_demo_data">

true

</td><td class="requires">

com.snc.expense\_line

</td></tr><tr><td>

Craft.co Integration for Supplier Lifecycle Operations\[com.snc.sn\_supplier\_craft\]

\(Available in the ServiceNow Store\)

</td><td>

Provides a pre-configured integration with Craft.io. Craft.io is a supplier intelligence platform that offers validated and comprehensive information about suppliers with which a company engages.

</td><td>

Inactive

</td><td>

false

</td><td>

com.snc.sn\_supplier\_mgmt

</td></tr><tr><td>

Cross-scope Access\[com.glide.scope.access\]

</td><td>

 

</td><td>

Inactive

</td><td>

false

</td><td>

 

</td></tr><tr id="plugin_com.glide.scope.privilege" class="plugin_reference"><td class="name">

Cross-scope App Privilege Enforcement\[com.glide.scope.privilege\]

</td><td class="description">

System for capturing and enforcing cross-scope privileges used by Scoped Apps

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

 

</td></tr><tr><td>

CSM Extension for Proxy Contacts\[com.snc.csm\_proxy\_contacts\]

</td><td>

Enables users who are internal to an organization to be the proxy case contact on behalf of customers.

</td><td>

Inactive

</td><td>

true

</td><td>

com.sn\_customerservice

</td></tr><tr><td>

CSM Order Management\[com.sn\_csm\_order\_mgmt\]

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr id="plugin_com.glide.ui.themes" class="plugin_reference"><td class="name">

CSS Theme support\[com.glide.ui.themes\]

</td><td class="description">

Provides support for CSS customizations to the user interface.

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

com.glide.ui.themes.core

</td></tr><tr id="plugin_com.glide.ui.themes.doctype" class="plugin_reference"><td class="name">

CSS Theme support - UI 14\[com.glide.ui.themes.doctype\]

</td><td class="description">

Provides UI15 themes.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

com.glide.ui.themes.core

</td></tr><tr><td>

CTI Demo Data for HRSD\[com.sn\_hr\_cti\_demo\]

</td><td>

Provides CTI Softphone application demo data for HRSD.

</td><td>

Inactive

</td><td>

false

</td><td class="requires">

-   com.snc.cti
-   com.sn\_hr\_core

</td></tr><tr><td>

CTI Softphone\[com.snc.cti\]

</td><td>

Enables Twilio integration using Notify and OpenFrame to provide softphone functions and call center capabilities. These include make, receive phone calls, transfer, hold and mute. Applications like Customer Service and Incident Management provide demo workflows for CTI.

</td><td>

Active

</td><td>

true

</td><td class="requires">

-   com.snc.matching\_rule
-   com.sn\_openframe
-   com.snc.notify
-   com.snc.notify.twilio\_direct

</td></tr><tr><td>

Credit Assessment\[com.sn\_bom\_credit\_asmt\]

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

CSM and FSM Configurable Workspace Foundation\[com.snc.uib.cwf\_workspace\]

</td><td>

Supports refactored version of customer workflow agent workspace.

</td><td>

Inactive

</td><td>

false

</td><td>

-   com.snc.app\_shell\_aw
-   com.snc.uib.base\_agent\_workspace
-   com.snc.uib.cwf\_workspace.integrations

</td></tr><tr><td>

CSM Configurable Workspace\[com.snc.uib.csm\_agent\_workspace\]

</td><td>

Supports refactored version of customer workflow customer service management agent workspace.

</td><td>

Active

</td><td>

true

</td><td>

-   com.snc.uib.cwf\_workspace
-   com.glideapp.servicecatalog.uxfworkspace
-   com.snc.uib.lookup\_verify
-   com.devsnc\_sn\_response\_templates

</td></tr><tr><td>

CSM Configurable Workspace\[sn\_csm\_wfo\_workspa\]

 \(Available in the ServiceNow Store\)

</td><td>

Provides a wide range of capabilities such as Channel Management, Scheduling, Coaching, and Teams applications in CSM Manager Workspace.

</td><td>

Active

</td><td>

true

</td><td>

-   com.snc.skills\_management
-   com.snc.sre
-   com.snc.pa.customer\_service

</td></tr><tr><td>

CSM Configurable Workspace Lookup and Verify\[com.snc.uib.lookup\_verify\]

</td><td>

Installs Lookup and Verify artifacts for the CSM Configurable Workspace that includes pages, macroponents, data brokers etc. and can be shared in different applications.

</td><td>

Inactive

</td><td>

true

</td><td>

com.snc.sn\_csm\_lookup\_verify

</td></tr><tr><td>

CSM Configurable Workspace Special Handling Notes\[com.snc.uib.special\_handling\_notes\]

</td><td>

Installs Special Handling Notes artifacts for the CSM Configurable Workspace that includes pages, macroponents, data brokers etc. and can be shared in different applications.

</td><td>

Inactive

</td><td>

false

</td><td>

 

</td></tr><tr><td>

CSM Contributor User\[com.snc.csm\_contributor\_user\]

</td><td>

Allows you to enable contributors to report and collaborate on cases created for customers, service organizations, or themselves.

</td><td>

Active

</td><td>

true

</td><td>

com.snc.cs\_base\_extension

</td></tr><tr><td>

CSM Query Rules\[com.snc.csm\_query\_rules\]

</td><td>

Plugin that contains the query rules for the CustomerService tables.

</td><td>

Inactive

</td><td>

false

</td><td>

com.snc.query\_rules

</td></tr><tr id="plugin_com.glideapp.servicecatalog.currency" class="plugin_reference"><td class="name">

Currency support for the service catalog\[com.glideapp.servicecatalog.currency\]

</td><td class="description">

Enables service catalog to support fully localized currencies for item prices and options.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

com.glide.currency

</td></tr><tr><td>

Custom URL\[com.snc.customurl\]

</td><td>

Activate this plugin to set up custom URL on the instance.

</td><td>

Inactive

</td><td>

false

</td><td>

com.snc.customurl.internal

</td></tr><tr><td>

Custom URL - Internal\[com.snc.customurl.internal\]

</td><td>

An internal plugin component to Scripted CustomURL APIs.

</td><td>

Inactive

</td><td>

false

</td><td>

 

</td></tr><tr><td>

Customer Communities\[com.sn\_customer\_communities\]

</td><td>

Enables you to connect, engage, and collaborate with your employees, customers, partners, and prospects. It is only available for customers who are licensed for Customer Services Management.

</td><td>

Inactive

</td><td>

false

</td><td class="requires">

-   com.sn\_external\_user\_register
-   com.sn\_communities

</td></tr><tr><td>

Customer Project Management\[com.snc.csm\_ppm\]

</td><td>

Provides the ability to create and manage projects for a customer account and gives end users visibility into their projects via the portal. This plugin requires the Customer Service plugin and the Project Portfolio Suite with Financials plugin.

</td><td>

Inactive

</td><td>

true

</td><td class="requires">

-   com.sn\_customerservice
-   com.snc.financial\_planning\_pmo

</td></tr><tr id="plugin_com.sn_customerservice" class="plugin_reference"><td class="name">

Customer Service\[com.sn\_customerservice\]

</td><td class="description">

Enables you to provide service and support for your external customers using several communication channels, such as email, web, and telephone. A case is created to track the issue reported or service requested, and assigned to groups or agents. Customer service agents in your organization work on the cases and resolve issues.

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

-   com.snc.asset\_management
-   com.snc.state\_flows
-   com.glide.connect.support
-   com.glide.connect.support.routing
-   com.snc.assignment\_workbench
-   com.snc.cs\_base
-   com.snc.skills\_management
-   com.snc.assessment\_core
-   com.snc.process\_flow\_formatter
-   com.snc.task\_relations
-   com.snc.task\_activity
-   com.snc.matching\_rule
-   com.sn\_resolutionshaper
-   com.sn\_openframe
-   com.sn\_shn
-   com.snc.contextual\_search.dynamic\_filters
-   com.sn\_cs\_social

</td></tr><tr><td>

Customer Service Base Extension Entities\[com.snc.cs\_base\_extension\]

</td><td>

This plugin provides granular access control through relationships, user profile attributes and roles.

</td><td>

Active

</td><td>

false

</td><td>

com.sn\_customerservice

</td></tr><tr><td>

Customer Service Case Types\[com.snc.csm\_case\_types\]

</td><td>

Enables customers to manage complex case processes by defining new case types. A case type represents an individual business process and is a collection of diverse inputs and tasks that an agent performs to resolve customer requests.

</td><td>

Inactive

</td><td>

true

</td><td>

com.sn\_customerservice

</td></tr><tr id="plugin_com.snc.customerservice_cti_demo" class="plugin_reference"><td class="name">

Customer Service CTI Demo Data\[com.snc.customerservice\_cti\_demo\]

</td><td class="description">

Provides demo data for the CTI Softphone application.

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

-   com.sn\_customerservice
-   com.snc.cti

</td></tr><tr><td>

Customer Service Household\[com.snc.household\]

</td><td>

Enables managing customer service for consumers belonging to the same household. Provides the ability to define the members of a household and relationships between them.

</td><td>

Active

</td><td>

true

</td><td>

com.snc.cs\_base\_extension

</td></tr><tr><td>

Customer Service Install Base Management\[com.snc.install\_base\]

</td><td>

Enables customers to capture the current state of a customer's install base and establish the relationship to any downstream entities that might impact their functioning.

</td><td>

Inactive

</td><td>

false

</td><td>

com.sn\_customerservice

</td></tr><tr id="plugin_com.snc.customerservice.demo" class="plugin_reference"><td class="name">

Customer Service Management Demo Data\[com.snc.customerservice.demo\]

</td><td class="description">

Provides demo data for the Customer Service Management application.

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires" id="entry_qmg_bmc_d1b">

-   com.sn\_customerservice
-   com.glide.service-portal.consumer-portal
-   com.glide.service-portal.customer-portal
-   com.snc.case\_assignment\_workbench\_demo
-   com.snc.work\_management.demo
-   com.snc.planned\_maintenance
-   com.snc.kb\_product\_entitlements
-   com.snc.publications\_demo
-   com.snc.shn\_demo
-   com.snc.csm.order
-   com.snc.csm\_fsm\_integration

</td></tr><tr><td>

Customer Service Management for Orders\[com.snc.csm.order\]

</td><td>

Extends the Customer Service Management application to support order-related issues by integrating with order management systems to create and resolve customer requests.

</td><td>

Inactive

</td><td>

true

</td><td>

com.sn\_customerservice

</td></tr><tr><td>

Customer Service Mobile\[com.sn\_csm\_mobile\]

</td><td>

Enables the mobile user interface for Customer Service Management.

</td><td>

Inactive

</td><td>

false

</td><td>

com.sn\_customerservice

</td></tr><tr><td>

Customer Service NLU Model for Virtual Agent Conversations\[com.sn\_csm.nlu\]

</td><td>

Enables CSM Virtual Agent conversations.

</td><td>

Active

</td><td>

false

</td><td class="requires">

-   com.sn\_customerservice
-   com.glide.cs.chatbot
-   com.glide.cs.sn-va-web-client-app

</td></tr><tr id="plugin_com.glide.service-portal.customer-portal" class="plugin_reference"><td class="name">

Customer Service Portal\[com.glide.service-portal.customer-portal\]

</td><td class="description">

Enables the Customer Service Portal, a web-based portal based on the Service Portal application that your company can use to provide information and support to customers.

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

com.glide.service-portal.customer-service-base

</td></tr><tr><td>

Customer Service Social Integration\[com.sn\_cs\_social\]

</td><td>

Customer Service Social integration, currently adds appropriate data schema changes needed for social integration scenarios.

</td><td>

Inactive

</td><td>

false

</td><td>

 

</td></tr><tr><td>

Customer Service Spoke\[com.snc.customer\_service.spoke\]

</td><td>

Enables Flow Designer users to automate the creation of customer service cases and updates to existing cases.

</td><td>

Inactive

</td><td>

false

</td><td>

Flow Designer - Installer \(com.glide.hub\)

</td></tr><tr><td>

Customer Service Virtual Agent Conversations\[com.sn\_csm.virtualagent\]

</td><td>

CSM Virtual Agent Conversations

</td><td>

Active

</td><td>

false

</td><td class="requires">

-   com.sn\_customerservice
-   com.glide.cs.chatbot
-   com.glide.cs.sn-va-web-client-app

</td></tr><tr><td>

Customer Service with Field Service Management\[com.snc.csm\_fsm\_integration\]

</td><td>

Enables Account, Contact, Partner, Partner Contact, Consumer information from Customer Service to Field Service Management.

</td><td>

Inactive

</td><td>

false

</td><td class="requires">

-   com.snc.work\_management
-   com.sn\_customerservice
-   com.glide.service-portal.customer-portal

</td></tr><tr><td>

Customer Service with Request Management\[com.sn\_cs\_sm\_request\]

</td><td>

Provides an integration between Customer Service Management and the Request Management application. Enables users to create request records from a Customer Service case.

</td><td>

Active

</td><td>

true

</td><td>

com.sn\_customerservice

</td></tr><tr><td>

Customer Service with Service Management\[com.sn\_cs\_sm\]

</td><td>

Provides an integration between Customer Service Management and the Incident, Problem and Change Management applications. Enables users to create incident, problem and change records from a Customer Service case.

</td><td>

Active

</td><td>

true

</td><td>

com.sn\_customerservice

</td></tr><tr><td>

Customer Service Install Base Management\[com.snc.install\_base\]

</td><td>

Enables customers to capture the current state of their install base and establish the relationship to any downstream entities that might impact their functioning.

</td><td>

Inactive

</td><td>

false

</td><td>

com.sn\_customerservice

</td></tr><tr><td>

Dashboard for Assessment and Survey\[com.snc.assessment\_core.dashboards\]

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Dashboard for Service Catalog\[com.glideapp.servicecatalog.dashboard\]

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr id="plugin_com.glide.auxdb" class="plugin_reference"><td class="name">

Data Archiving\[com.glide.auxdb\]

</td><td class="description">

Provides the ability to move a subset of data from large tables into the data archive. Typical candidates include historical ITIL documents such as incidents that were closed last year, but the functionality supports archiving of non ITIL documents as well.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

com.snc.db.replicate

</td></tr><tr><td>

Data Classification\[com.glide.data\_classification\]

</td><td>

 

</td><td>

Active

</td><td>

true

</td><td>

 

</td></tr><tr id="plugin_com.snc.certification_v2" class="plugin_reference"><td class="name">

Data Certification\[com.snc.certification\_v2\]

</td><td class="description">

Enables field-level certification of data, either scheduled or on-demand.

</td><td>

Inactive

</td><td class="has_demo_data">

true

</td><td class="requires">

-   com.glide.list\_v2
-   com.snc.certification\_core

</td></tr><tr><td>

Data Discovery APIs\[com.glide.data\_discovery\]

</td><td>

Provides the APIs to discover sensitive data.

</td><td>

Active

</td><td>

false

</td><td>

 

</td></tr><tr><td>

Data Filtration\[com.glide.data\_filtration\]

 \(New in Tokyo\)

</td><td>

Controls the access to tables and records based on subject attributes when performing read queries.

</td><td>

Inactive

</td><td>

false

</td><td>

None

</td></tr><tr id="plugin_com.glide.data_lookup" class="plugin_reference"><td class="name">

Data Lookup and Record Matching Support\[com.glide.data\_lookup\]

</td><td class="description">

Allows administrators to define rules that automatically set one or more field values when certain conditions are met. This plugin completely replaces Priority Lookup. Any custom logic defined in the CalculatePriority business rule must be manually translated into the new priority data lookup definition.

</td><td>

Active

</td><td class="has_demo_data">

true

</td><td class="requires">

 

</td></tr><tr id="plugin_com.glide.data_lookup.catalog" class="plugin_reference"><td class="name">

Data Lookup and Record Matching Support for Service Catalog\[com.glide.data\_lookup.catalog\]

</td><td class="description">

Allows administrators to perform data lookups for variables on service catalog item screens, on requested items, and on catalog tasks as a user fills out the values contained in variables.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

-   com.glideapp.servicecatalog.platform
-   com.glide.data\_lookup

</td></tr><tr id="plugin_com.glide.data_policy2" class="plugin_reference"><td class="name">

Data Policy 2\[com.glide.data\_policy2\]

</td><td class="description">

Defines mandatory or read-only requirements for table fields.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

 

</td></tr><tr id="plugin_com.snc.datastructure" class="plugin_reference"><td class="name">

Data Structures\[com.snc.datastructure\]

</td><td class="description">

Provides element types: DataStructure and DataObject for flyweight data that can be stored internally as JSON and utilized via the DataStructure API.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

 

</td></tr><tr><td>

Database Column Offrow Migration\[com.glide.db.offrow\_migration\]

</td><td>

UI/Script elements to allow for compatible columns to be moved offrow.

</td><td>

Inactive

</td><td>

false

</td><td>

 

</td></tr><tr id="plugin_com.snc.db.rotation" class="plugin_reference"><td class="name">

Database Rotation\[com.snc.db.rotation\]

</td><td class="description">

Provides the ability to break large tables into smaller, more manageable tables â€“ these smaller tables contain a specified period of data and the table with oldest data is purged on an on-going basis.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

 

</td></tr><tr id="plugin_com.snc.db.rotation_default_tables" class="plugin_reference"><td class="name">

Database Rotation with Default Tables\[com.snc.db.rotation\_default\_tables\]

</td><td class="description">

Adds database rotation functionality to default tables.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

com.snc.db.rotation

</td></tr><tr id="plugin_com.glide.db_audio" class="plugin_reference"><td class="name">

Database Storage for Audio Files\[com.glide.db\_audio\]

</td><td class="description">

Allows audio files to be uploaded and stored in the database, and referenced in HTML.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

 

</td></tr><tr id="plugin_com.glide.db_images" class="plugin_reference"><td class="name">

Database Storage for Images\[com.glide.db\_images\]

</td><td class="description">

Allows images to be uploaded and stored in the database, and referenced in HTML.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

 

</td></tr><tr id="plugin_com.glide.db_video" class="plugin_reference"><td class="name">

Database Storage for Video Files\[com.glide.db\_video\]

</td><td class="description">

Allows video files to be uploaded and stored in the database, and referenced in HTML.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

 

</td></tr><tr id="plugin_com.glide.db_view" class="plugin_reference"><td class="name">

Database Views\[com.glide.db\_view\]

</td><td class="description">

Allows you to define table joins for reporting purposes.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

 

</td></tr><tr id="plugin_com.snc.service.db_views" class="plugin_reference"><td class="name">

Database Views for Service Management\[com.snc.service.db\_views\]

</td><td class="description">

Predefined Database Views for Service Management.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

-   com.glide.db\_view
-   com.snc.service
-   com.snc.problem
-   com.snc.incident
-   com.glide.metrics

</td></tr><tr id="plugin_com.glide.ui.ng.datatables" class="plugin_reference"><td class="name">

DataTables 1.1.0 Components\[com.glide.ui.ng.datatables\]

</td><td class="description">

DataTables 1.1.0 Components

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

 

</td></tr><tr><td>

Default Financial Management Cost Model\[com.snc.financial\_management\_model\]

</td><td>

Provides a preconfigured Cost Model and artifacts to enable Financial Analysts to assemble spending data and generate reports. Activation of this plugin on production instances may have licensing implications.

 Contact your ServiceNow account team for details.

</td><td>

Inactive

</td><td>

true

</td><td>

com.snc.financial\_management

</td></tr><tr><td>

Delegated Dev User Administration\[com.sn\_dd\_user\_admin\]

</td><td>

Delegated Dev User Administration.

</td><td>

Active

</td><td>

false

</td><td>

 

</td></tr><tr id="plugin_com.glide.delegated_development" class="plugin_reference"><td class="name">

Delegated Development\[com.glide.delegated\_development\]

</td><td class="description">

Support for controlled development by users who do not have full administrative rights.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

 

</td></tr><tr><td>

Delegated Request Experience \(Maintenance mode\)\[com.glideapp.servicecatalog.request\_management.delegated\_request\_experience\]

</td><td>

Enables delegated requests for catalog items and activates the Requested For variable type and the Requested For field in Requested Item

</td><td>

Active

</td><td>

false

</td><td class="requires">

-   com.glideapp.servicecatalog.platform
-   com.glideapp.servicecatalog.requested\_for

</td></tr><tr><td>

Delete Recovery\[com.glide.delete\_recovery\]

</td><td>

Provides the ability to recover individual deleted items including all related cascaded deleted items.

</td><td>

Active

</td><td>

false

</td><td>

 

</td></tr><tr><td>

Delete Recovery: Partial Undelete Support\[com.glide.delete\_recovery.partial\_undelete\]

</td><td>

Extends the Delete Recovery plugin to support partially undeleting records from a transaction.

</td><td>

Active

</td><td>

false

</td><td>

com.glide.delete\_recovery

</td></tr><tr><td>

Demand Core\[com.snc.demand\_core\]

</td><td>

Demand Core Plugin aids in planning, organizing, and managing Demands with basic features.

</td><td>

Active

</td><td>

false

</td><td>

 

</td></tr><tr id="plugin_com.snc.demand_management" class="plugin_reference"><td class="name">

Demand Management\[com.snc.demand\_management\]

</td><td class="description">

Aids with capturing the demand and provides tools to screen, assess, and prioritize it. Only upgrade is allowed for this plugin. Activation should be done through PPM Standard plugin.

</td><td>

Inactive

</td><td class="has_demo_data">

true

</td><td class="requires">

-   com.snc.process\_flow\_formatter
-   com.snc.assessment\_core
-   com.snc.timeline\_visualization
-   com.snc.bubblechart\_workbench

</td></tr><tr id="plugin_com.snc.depreciation" class="plugin_reference"><td class="name">

Depreciation\[com.snc.depreciation\]

</td><td class="description">

Core depreciation capabilities.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

 

</td></tr><tr id="plugin_com.glide.ui.ng.dc" class="plugin_reference"><td class="name">

Designer Common\[com.glide.ui.ng.dc\]

</td><td class="description">

Provides common components required by designers such as the form designer and the quiz designer.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

-   com.glide.ui.tablet.theme
-   com.glide.ui.ng
-   com.glide.ui.themes.doctype

</td></tr><tr id="plugin_com.snc.certification_desired_state" class="plugin_reference"><td class="name">

Desired State Certification\[com.snc.certification\_desired\_state\]

</td><td class="description">

Evaluates records to see if they match a desired state, scheduled or on-demand.

</td><td>

Active

</td><td class="has_demo_data">

true

</td><td class="requires">

com.snc.certification\_core

</td></tr><tr><td>

DevOps\[sn\_devops\]

 \(Available in the ServiceNow Store\)

</td><td>

Provides data insights, accelerates change, and increases visibility into your DevOps environment.

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

DevOps Config\[sn\_devops\_config\]

 \(Available in the ServiceNow Store\)

</td><td>

Manages and validates configuration data in your DevOps environment using a single system.

</td><td>

Active

</td><td>

false

</td><td>

sn\_cdm

</td></tr><tr><td>

DevOps Insights\[sn\_devops\_insights\]

 \(Available in the ServiceNow Store\)

</td><td>

Shows the results of your overall DevOps process in a data-driven dashboard.

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

DevOps Integration with Rally\[sn\_devops\_rally\]

 \(Available in the ServiceNow Store\)

</td><td>

Provides integration with Broadcom Rally to expose data like projects, user stories, and defects from the Rally tool in DevOps Change acceleration. You can then associate these Rally planning objects to commits and pipelines for full change traceability and acceleration.

</td><td>

Active

</td><td>

false

</td><td>

com.sn\_devops

</td></tr><tr><td>

DevOps Util\[com.snc.sn\_devops\_util\]

 \(New in Tokyo\)

</td><td>

Serves as an interface to call global APIs from DevOps.

</td><td>

Active

</td><td>

false

</td><td>

 

</td></tr><tr id="plugin_com.snc.dhtmlx.gantt" class="plugin_reference"><td class="name">

DHTMLX Gantt Library\[com.snc.dhtmlx.gantt\]

</td><td class="description">

DHTMLX Gantt library.

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

 

</td></tr><tr id="plugin_com.snc.dhtmlx.scheduler" class="plugin_reference"><td class="name">

DHTMLX Scheduler Library\[com.snc.dhtmlx.scheduler\]

</td><td class="description">

DHTMLX Scheduler library.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

 

</td></tr><tr id="plugin_com.glide.monitor.diagnostics" class="plugin_reference"><td class="name">

Diagnostic Monitoring\[com.glide.monitor.diagnostics\]

</td><td class="description">

Provides advanced diagnostic monitoring of each node in a ServiceNow instance.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

 

</td></tr><tr id="plugin_com.glide.dictionary_override" class="plugin_reference"><td class="name">

Dictionary overrides\[com.glide.dictionary\_override\]

</td><td class="description">

Allows specific Dictionary values to be overridden for extended table elements. For example, this plugin allows the default value for the Assigned To field in the Incident table to be different than the default value specified for the Assigned To field in the Task table.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

 

</td></tr><tr><td>

Discovery and Service Mapping Patterns\[com.sn\_itom\_pattern\]

 \(Available in the ServiceNow Store\)

</td><td>

Deploys additional Discovery and Service Mapping Patterns.

</td><td>

Active

</td><td>

false

</td><td>

None

</td></tr><tr><td>

Discovery for Operational Technology\[com.sn\_otsm\_discovery\]

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Distribution Download Proxy\[com.glide.dist\_download\_proxy\]

</td><td>

Proxy for downloading a distribution. This plugin is activated automatically when the MID Server is activated, to handle the REST requests for file downloads that a MID Server sends to the instance.

</td><td>

Active

</td><td>

false

</td><td>

 

</td></tr><tr><td>

Document Intelligence Administration\[com.snc.docintel\_admin\]

 \(Available in the ServiceNow Store\)

</td><td>

Better administration experience for Document Intelligence.

</td><td>

Active

</td><td>

false

</td><td>

-   Document Intelligence \(sn\_docintel\)
-   Predictive Intelligence \(com.glide.platform\_ml\)

</td></tr><tr><td>

Document Service\[com.sn\_bom\_document\]

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Document Templates\[com.snc.document\_templates\]

 \(Available in the ServiceNow Store\)

</td><td>

Enables you to create HTML and PDF document templates to generate standard letters or documents. Automates and simplifies the process of filling, signing, and reviewing a document online.

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Document Template Integration with AdobeSign\[sn\_dt\_adobesign\]

 \(Available in the ServiceNow Store\)

</td><td>

Enables you to use the Adobe Sign application for signing documents that are generated from ServiceNow Document Templates.

</td><td>

Active

</td><td>

true

</td><td>

None

</td></tr><tr><td>

Document Template integration with DocuSign\[sn\_dt\_docusign\]

 \(Available in the ServiceNow Store\)

</td><td>

Enables you to use the DocuSign application for signing documents that are generated from ServiceNow Document Templates.

</td><td>

Active

</td><td>

true

</td><td>

None

</td></tr><tr><td>

Documents Configuration\[com.glide.doc.config\]

</td><td>

Provides a feature to create a Table of Contents configuration \(that is adding table of contents\) and a document configuration such as page numbers to a PDF document that is generated from an HTML document. The plugin provides features to navigate easily through the PDF using Table to Contents and Document Configuration.

</td><td>

Active

</td><td>

false

</td><td>

None

</td></tr><tr><td class="name">

Domain Support - Domain Extensions Installer\[com.glide.domain.msp\_extensions.installer\]

</td><td class="description">

Enables domain separation for Cloud Provisioning and Governance. Instances activating Domain separation should use this plugin. In addition to functionality in the Domain Support plugin, this plugin installs Domain Support - Domain Extensions that include further domain separation enhancements for all domain customers including Managed Service Providers. If the Domain Support plugin is already active, content in the Domain Support - Domain Extensions plugin will not be installed to the instance.

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Dynamic Related Records for Configurable Workspace\[com.snc.uib.sn\_dyn\_rel\_rec\]

</td><td>

Dynamic related records provide agents with access to relational information based on the context of the current record. Admin can configure related record definitions that increase agent productivity by making data available in context to the action that the agent is performing.

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td class="name">

Dynamic Scheduling\[com.snc.dynamic\_scheduling\]

</td><td class="description">

Dynamic scheduling for Service Management Applications with support for bulk task recommendations and interval based auto assignment.

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

-   com.snc.matching\_rule
-   com.snc.service\_management.core

</td></tr><tr><td>

Dynamic Translation\[com.glide.dynamic\_translation\]

</td><td>

Adds ability to translate the given text from source language to target language using external machine translation providers.

</td><td>

Active

</td><td>

false

</td><td>

com.glide.hub.integrations

</td></tr><tr><td>

Dynamic Translation for Virtual Agent\[com.glide.cs.dynamic.translation.virtual\_agent\]

 \(New in Tokyo\)

</td><td>

Activates the Dynamic Translation for Virtual Agent.

</td><td>

active

</td><td>

false

</td><td>

-   com.glide.dynamic\_translation
-   com.glide.dynamic\_translation.va\_async

</td></tr><tr><td>

Dynamic Translation Spoke\[com.glide.dynamic\_translation.spoke\]

</td><td>

Provides actions that enable the ability to translate text\(s\) from one language to other language\(s\) and to detect the language of given text.

</td><td>

Active

</td><td>

false

</td><td>

-   com.glide.hub
-   com.glide.hub.integration.runtime

</td></tr><tr id="plugin_com.glide.phone_number" class="plugin_reference"><td class="name">

E164 Compliant Phone Number\[com.glide.phone\_number\]

</td><td class="description">

Ensures that all necessary information for a phone number is included and properly formatted to successfully route an international call over a territory's public telephone network.

</td><td>

Active

</td><td class="has_demo_data">

true

</td><td class="requires">

 

</td></tr><tr id="plugin_com.glide.email.oauth" class="plugin_reference"><td class="name">

Email - OAUTH support for IMAP and SMTP\[com.glide.email.oauth\]

</td><td class="description">

Support for XOAUTH and XOAUTH2 email authentication.

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

-   com.glide.email\_accounts
-   com.snc.platform.security.oauth

</td></tr><tr><td>

Email - Support for Email Processing by Microsoft Graph API\[glide.email.graph\]

 \(New in Tokyo\)

</td><td>

Processes inbound emails using Microsoft Graph API.

</td><td>

Active

</td><td>

false

</td><td>

-   com.glide.email\_accounts
-   com.snc.platform.security.oauth
-   com.glide.email.oauth

</td></tr><tr><td>

Email Access Restriction\[com.glide.email\_access\_restriction\]

</td><td>

Allows email table ACL conditional overrides

</td><td>

Active

</td><td>

false

</td><td>

 

</td></tr><tr id="plugin_com.glide.email_accounts" class="plugin_reference"><td class="name">

Email Accounts\[com.glide.email\_accounts\]

</td><td class="description">

Enables you to define email accounts and settings in individual records.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

 

</td></tr><tr><td>

Email Address Filter\[com.glide.email\_address\_filter\]

</td><td>

APIs and data structures for email address filtering

</td><td>

Active

</td><td>

false

</td><td>

 

</td></tr><tr id="plugin_com.glide.email_createuser" class="plugin_reference"><td class="name">

Email Automatic User Creation\[com.glide.email\_createuser\]

</td><td class="description">

Sets glide.email.create\_userid\_from\_email=true so that when automatic user creation is enabled, the UserID of newly-created users matches the user's email address. Also widens sys\_user.user\_name column to 100 bytes to accommodate longer UserIDs based on email addresses.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

 

</td></tr><tr><td>

Email Client\[com.glide.email\_client\]

</td><td>

Enables you to send email directly from any record

</td><td>

Active

</td><td>

false

</td><td>

com.glide.email\_address\_filter

</td></tr><tr><td>

Email Client Template\[com.glide.email\_client\_template\]

</td><td>

Template defines default content for the Email Client.

</td><td>

Active

</td><td>

false

</td><td>

 

</td></tr><tr><td class="name">

Email Digest\[com.glide.email\_digest\]

</td><td>

Email Digest

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

-   Subscription Based Notifications
-   Outbound Email Notifications
-   com.glide.notification.preference.service

</td></tr><tr id="plugin_com.glide.email_filter" class="plugin_reference"><td class="name">

Email Filters\[com.glide.email\_filter\]

</td><td class="description">

Filters emails into different mailboxes or junk, depending on headers and subject. Ignores any email that contains a VCAL invitation.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

 

</td></tr><tr id="plugin_com.glide.email_notification_preview" class="plugin_reference"><td class="name">

Email Notification Preview Plugin\[com.glide.email\_notification\_preview\]

</td><td class="description">

Allows you to easily preview a ServiceNow email notification without sending the notification. This allows you to preview notifications at design time.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

 

</td></tr><tr><td>

Email Notification Script for Contextual Search Results\[com.snc.adv\_cxs\_results\_email\_script\]

</td><td class="description">

Provides script for embedding contextual search results based on Predictive Intelligence additional resources and search resources in email notifications.

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td>

 

</td></tr><tr id="plugin_com.glide.email_retention" class="plugin_reference"><td class="name">

Email Retention\[com.glide.email\_retention\]

</td><td class="description">

Provides retention policy for email.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

-   com.glide.mailbox
-   com.glide.auxdb

</td></tr><tr><td>

Email Service\[com.glide.email.service\]

</td><td>

Defines javascript and REST API for sending email.

</td><td>

Active

</td><td>

false

</td><td>

com.glide.mailbox

</td></tr><tr><td>

Email Unsubscribe\[com.glide.email\_unsubscribe\]

</td><td>

Adds the ability to include an unsubscribe link in notifications.

</td><td>

Active

</td><td>

false

</td><td class="requires">

-   com.glide.email\_ordered\_processing
-   com.glide.notification.subscription

</td></tr><tr id="plugin_com.glide.email_sms_separation" class="plugin_reference"><td class="name">

Email/SMS Separation\[com.glide.email\_sms\_separation\]

</td><td class="description">

Separation of the sending of SMS and email by adding a column to the email table. Prevents SMS messages from slowing down email message sending and vice versa. Activation of this plugin will cause email to stop sending during activation. On systems with large email tables this can take hours, and is not recommended.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

com.glide.notification

</td></tr><tr id="plugin_com.glide.embedded_help" class="plugin_reference"><td class="name">

Embedded Help\[com.glide.embedded\_help\]

</td><td class="description">

Provides targeted help content to a user in a UI page. Administrators can create customized embedded help to assist users with specific business processes within an organization.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

com.glide.ui.hopscotch

</td></tr><tr><td>

Embedded Help for ServiceNow Flow Designer\[com.glide.hub.flow\_designer\_embedded\_help\]

</td><td>

This plugin is for the embedded help panel in Flow Designer. In Quebec, there is a help panel to help users easily access documentation on Flow Designer without having to navigate to the documentation site.

</td><td>

Active

</td><td>

false

</td><td>

 

</td></tr><tr><td>

Employee Center\[com.snc.employee\_center\]

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Employee Center - Core\[com.snc.employee\_center\_core\]

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Employee Center - Pro\[com.snc.employee\_center\_pro\]

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Employee Center - Pro\[com.sn\_ex\_employee\_center\_pro\]

</td><td>

Employee Center Pro

</td><td>

False

</td><td>

Inactive

</td><td>

com.sn\_hr\_service\_portal

</td></tr><tr><td>

Employee Center integration with Zoom\[com.snc.sn\_ex\_ec\_zm\]

 \(Available in the ServiceNow Store\)

</td><td>

Enables Employee Center integration with Zoom.

</td><td>

Active

</td><td>

true

</td><td>

sn\_ex\_sp

</td></tr><tr><td>

Employee Document Management\[com.sn\_employee\_document\_management\]

</td><td>

Enables you to manage large numbers of employee documents efficiently. Provides storage space and a filing system that allows you to easily retrieve documents, as well as define who can view sensitive documents, and when to purge documents.**Important:** To use Employee Document Management, the Human Resources Scoped App: Core plugin must be licensed and activated.

</td><td>

Inactive

</td><td>

true

</td><td class="requires">

-   com.snc.documentviewer
-   com.glide.scope.access.restricted\_caller

</td></tr><tr><td>

Employee Relations integration with NAVEX EthicsPoint\[sn\_hr\_navex\_ep\]

 \(Available in the ServiceNow Store\)

</td><td>

Pulls employee relation cases from NAVEX EthicsPoint into ServiceNow Platform, enabling an HR Agent to work on employee relation cases from an ServiceNow instance.

</td><td>

Active

</td><td>

false

</td><td>

None

</td></tr><tr><td>

Employee Service Center\[com.sn\_hr\_service\_portal\]

</td><td>

Activates a portal framework that allows administrators to build a mobile-friendly self service experience for users.

</td><td>

Active

</td><td>

true

</td><td class="requires">

-   com.glide.connect.support
-   com.glide.connect.sp\_widgets
-   com.sn\_content\_delivery
-   com.sn\_content\_automation
-   com.glide.va.sp\_widgets
-   com.glideapp.user\_criteria.scoped.api

</td></tr><tr><td>

EMR Help\[sn\_ind\_rmt\_help\]

 \(Available in the ServiceNow Store\)

</td><td>

Simplifies and streamlines the process to submit ServiceNow IT service requests related to an electronic medical record \(EMR\) system.

</td><td>

Inactive

</td><td class="has_demo_data">

true

</td><td class="requires">

-   com.glide.encryption
-   com.sn\_ind

</td></tr><tr><td>

Encrypted Workflow Scratchpad\[com.snc.encrypted.scratchpad\]

</td><td>

Encrypted Scratchpad support on the Workflow Context and Workflow Executing Activities.

</td><td>

Active

</td><td>

false

</td><td class="requires">

-   com.glideapp.workflow
-   com.glide.encryption

</td></tr><tr><td>

Encryption Core\[com.glide.encryption.core\]

</td><td>

Common scripts and logic between Edge Encryption and Encryption Support.

</td><td>

Inactive

</td><td>

false

</td><td>

 

</td></tr><tr><td>

Encrypted Workflow Scratchpad\[com.snc.encrypted.scratchpad\]

</td><td>

Encrypted Scratchpad support on the Workflow Context and Workflow Executing Activities.

</td><td>

Inactive

</td><td>

false

</td><td class="requires">

-   com.glideapp.workflow
-   com.glide.encryption

</td></tr><tr id="plugin_com.glide.email_engine_notifs" class="plugin_reference"><td class="name">

Engine Based Notifications\[com.glide.email\_engine\_notifs\]

</td><td class="description">

Container for engine-based email notifications. Contains a set of default email notifications. Installed only on new z-boots.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

 

</td></tr><tr id="plugin_com.glide.web_service_provider_v2" class="plugin_reference"><td class="name">

Enhanced Web Service Provider - Common\[com.glide.web\_service\_provider\_v2\]

</td><td class="description">

 

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

com.glide.web\_service\_provider

</td></tr><tr><td>

Enterprise Asset Management\[com.sn\_eam\]

 \(Available in the ServiceNow Store\)

</td><td>

Provides a comprehensive end-to-end solution for managing the full lifecycle of non-IT assets, providing deep visibility into the asset estate, minimizing costly downtime, and maximizing the asset usable life.

</td><td>

Inactive

</td><td>

true

</td><td>

-   com.sn\_eam\_core
-   com.snc.procurement
-   com.sn\_itam\_recomm
-   com.snc.asset\_management
-   sn\_cmdb\_ci\_class
-   com.sn\_itam\_common
-   com.sn\_ent
-   com.sn\_risk\_heatmap

</td></tr><tr><td>

Environmental, Social, and Governance Management\[com.sn\_esg\]

 \(Available in the ServiceNow Store\)

</td><td>

Provides capabilities to collect, manage, and report organizational environmental, social, and governance \(ESG\) data and activities to stakeholders including investors, customers, and regulators.

</td><td>

Active

</td><td>

true

</td><td>

-   com.sn\_grc
-   com.sn\_grc\_workspace
-   com.sn\_compliance
-   com.snc.goal\_framework
-   com.sn\_grc\_metric

</td></tr><tr><td>

E-Signature\[com.snc.esign\]

</td><td>

Allows for the electronic signing of documents on both desktop and mobile. Signatories can sign with their credentials, as an acknowledgment, or as a typed or drawn e-signature.

</td><td>

Active

</td><td>

false

</td><td class="requires">

-   com.snc.signaturepad
-   com.snc.document\_management
-   com.snc.documentviewer

</td></tr><tr><td>

ERP Customization Mining \[com.snc.uib.sn\_erp\_mining\]

 \(Available in the ServiceNow Store\)

</td><td>

Enables use of ERP Customization Mining to identify customized application candidates for replatforming.

</td><td>

Active

</td><td>

true

</td><td>

-   com.snc.sn\_erp\_integration
-   com.glide.platform\_ml

</td></tr><tr><td>

ERP Canvas\[com.snc.sn\_erp\_integration\]

 \(Available in the ServiceNow Store\)

</td><td>

Enables access to remote tables for ERP Customization Mining.

</td><td>

Active

</td><td>

false

</td><td>

com.glide.script.vtable

</td></tr><tr id="plugin_com.glide.cms.extensions" class="plugin_reference"><td class="name">

ESS Portal \(implemented within Content Management\)\[com.glide.cms.extensions\]

</td><td class="description">

ESS portal content management application. Demo data includes the actual ESS portal. Use Service Portal for new development instead of CMS. Service Portal is an alternative to CMS with a refined user experience, and is active by default in the base system. For more information, see [Service Portal](https://www.servicenow.com/docs/access?context=c_ServicePortal&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US) and [Content Management and Service Portal](https://www.servicenow.com/docs/access?context=c_CMSAndSP&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US).

</td><td>

Active

</td><td class="has_demo_data">

true

</td><td class="requires">

com.glide.cms

</td></tr><tr><td>

Event Management Mobile Interface Content\[com.em-mobile-app\]

</td><td>

Content Of Event Management Mobile Interface Content.

</td><td>

Inactive

</td><td>

false

</td><td>

 

</td></tr><tr><td>

Event Management metric explorer\[com.sn-em-metric-explorer\]

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr id="plugin_com.glideapp.report.em" class="plugin_reference"><td class="name">

Event Management Overview Homepage\[com.glideapp.report.em\]

</td><td class="description">

Event Management Overview Homepage

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

-   com.glideapp.report
-   com.glideapp.itom.snac

</td></tr><tr><td>

Event stats\[com.glide.stats.event\]

</td><td>

Event stats.

</td><td>

Active

</td><td>

false

</td><td>

com.glide.stats

</td></tr><tr><td>

Evidence Management\[com.sn\_evidence\_management\]

</td><td>

Enables you to collect, categorize, retain, and secure evidence that can be used in cases that require gathering and reviewing artifacts for an investigation.

</td><td>

Active

</td><td>

true

</td><td>

 

</td></tr><tr id="plugin_com.glideapp.servicecatalog.execution_plan" class="plugin_reference"><td class="name">

Execution Plan support for the service catalog\[com.glideapp.servicecatalog.execution\_plan\]

</td><td class="description">

Service Catalog execution plans.

</td><td>

Active

</td><td class="has_demo_data">

true

</td><td class="requires">

com.glide.execution\_plan

</td></tr><tr id="plugin_com.snc.expense_line" class="plugin_reference"><td class="name">

Expense Line\[com.snc.expense\_line\]

</td><td class="description">

Core expense line table that enables cost tracking. Integrated with asset management, CMDB, cost management, and contract management.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

 

</td></tr><tr id="plugin_com.snc.extended_cmdb" class="plugin_reference"><td class="name">

Extended CMDB\[com.snc.extended\_cmdb\]

</td><td class="description">

Provides specialized configuration items, such as radio hardware, test equipment, and voice system hardware.

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

com.snc.cmdb

</td></tr><tr><td>

External Content for AI Search plugin \[com.glide.ais.external\_content\]

 \(New in Utah\)

</td><td>

Allows ingesting external content to AI search.

</td><td>

Active

</td><td>

false

</td><td>

None

</td></tr><tr><td>

External file data storage\[com.sn.external.files\]

</td><td>

Stores information about files in third-party systems and provides actions to manage the information.

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr id="plugin_com.snc.facilities_service_automation" class="plugin_reference"><td class="name">

Facilities Service Management clo\[com.snc.facilities\_service\_automation\]

</td><td class="description">

Manages facilities requests and enables users to report and track requests by their location. To view requests on a floor plan, the Facilities Visualization Workbench \(com.snc.facilities\_service\_automation.fvw\) plugin is required. Integration files installed when Facilities Visualization Workbench \(com.snc.facilities\_service\_automation.fvw\) is also installed.

Activation of this plugin on production instances may require a separate license. Contact ServiceNow for details.

</td><td>

Inactive

</td><td class="has_demo_data">

true

</td><td class="requires">

com.snc.service\_management.core

</td></tr><tr id="plugin_com.snc.facilities_service_automation.cms" class="plugin_reference"><td class="name">

Facilities Service Management CMS Portal \(Maintenance mode only\)\[com.snc.facilities\_service\_automation.cms\]

</td><td class="description">

Lets you launch Facilities Service Automation and other service management applications from a single CMS page. Manages facilities requests and enables users to report and track requests by their location on a floor plan. Activation of this plugin on production instances may require a separate license. Contact ServiceNow for details.

</td><td>

Inactive

</td><td class="has_demo_data">

true

</td><td class="requires">

-   com.snc.facilities\_service\_automation
-   com.snc.service\_management.core.cms

</td></tr><tr id="plugin_com.snc.facilities_service_automation_m" class="plugin_reference"><td class="name">

Facilities Service Management Mobile \(Maintenance mode only\)\[com.snc.facilities\_service\_automation\_m\]

</td><td class="description">

Manages facilities service management mobile components.

</td><td>

Inactive

</td><td class="has_demo_data">

true

</td><td class="requires">

-   com.snc.facilities\_service\_automation
-   com.snc.service\_management\_m

</td></tr><tr id="plugin_com.snc.field_normalization" class="plugin_reference"><td class="name">

Field Normalization\[com.snc.field\_normalization\]

</td><td class="description">

Provides support for cleaning up messy data through normalization and transformation.

</td><td>

Inactive

</td><td class="has_demo_data">

true

</td><td class="requires">

-   com.glide.vars
-   com.glide.system\_update\_set

</td></tr><tr><td>

Field Service Advanced Parts Sourcing\[com.snc.fsm\_advanced\_parts\_sourcing\]

 \(New in Tokyo\)

</td><td>

Enables Field Service agents to request and source multiple parts. Agents can receive mobile notifications when part requests are raised by their peers.

</td><td>

Inactive

</td><td>

true

</td><td>

com.snc.fsm\_advanced\_parts\_sourcing

</td></tr><tr><td>

Field Service Capacity Management\[com.snc.fsm\_capacity\_management\]

</td><td>

Provides capabilities to manage task capacity for groups and field agents.

</td><td>

Active

</td><td>

false

</td><td>

com.snc.work\_management

</td></tr><tr><td>

Field Service Contractor Management\[com.snc.fsm\_contractor\_management\]

</td><td>

Enables to outsource field service tasks. Contractor companies can re assign tasks to field agents and they can work on assigned tasks

</td><td>

Active

</td><td>

true

</td><td class="requires">

-   com.snc.work\_management
-   com.snc.outsourced\_service\_provider

</td></tr><tr><td>

Field Service Crew Operations\[com.snc.fsm\_crew\_scheduling\]

</td><td>

Helps organizations to assign the same set of resources repeatedly, to different tasks. This simplifies the scheduling process and allows field service agents to work together more consistently.

</td><td>

Active

</td><td>

true

</td><td>

com.snc.work\_management

</td></tr><tr id="plugin_com.snc.work_management" class="plugin_reference"><td class="name">

Field Service Management\[com.snc.work\_management\]

</td><td class="description">

Provides support for scheduling and managing on-location work tasks.

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

-   com.snc.service\_management.core
-   com.sn\_shn
-   com.snc.assignment\_workbench
-   com.snc.central\_dispatch
-   com.snc.wo\_signature\_pad
-   com.snc.wm\_questionnaire
-   com.snc.dynamic\_scheduling

</td></tr><tr><td>

Field Service Management Access Hours Management\[com.snc.fsm\_access\_hours\]

</td><td>

Enables the management of access hours for work order tasks.

</td><td>

Active

</td><td>

false

</td><td>

com.snc.work\_management

</td></tr><tr id="plugin_com.snc.work_management.cms" class="plugin_reference"><td class="name">

Field Service Management CMS Portal\[com.snc.work\_management.cms\]

</td><td class="description">

Lets you launch Field Service Automation and other service management applications from a single CMS page.

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

-   com.snc.work\_management
-   com.snc.service\_management.core.cms

</td></tr><tr><td>

Field Service Management Intelligent Task Recommendations\[com.snc.fsm\_task\_recommendations\]

</td><td>

Provides functionality to recommend tasks for assignment to field service technicians as well as manage criteria which can be used to make the task assignment recommendations.

</td><td>

Active

</td><td>

false

</td><td>

com.snc.work\_management,com.snc.task\_recommendations

</td></tr><tr><td>

Field Service Management Configurable Dispatcher Workspace\[com.snc.uib.fsm\_dispatcher\_workspace\]

</td><td>

Provides the FSM components and pages to support dispatcher flows on Agent Workspace.

</td><td>

Active

</td><td>

false

</td><td>

-   com.snc.uib.fsm\_agent\_workspace
-   com.sn\_fsm\_components

</td></tr><tr><td>

Field Service Management Configurable Workspace\[com.snc.uib.fsm\_agent\_workspace\]

</td><td>

Provides the FSM components, lists, and forms to support FSM on Agent Workspace.

</td><td>

Active

</td><td>

false

</td><td>

-   com.snc.uib.cwf\_workspace
-   com.snc.work\_management

</td></tr><tr><td>

Field Service Management - Customer Experience\[com.snc.fsm\_customer\_experience\]

</td><td>

Engage customers with relevant updates on reported issues

</td><td>

Active

</td><td>

false

</td><td class="requires">

-   com.snc.csm\_fsm\_integration
-   com.snc.notify.twilio\_direct

</td></tr><tr id="plugin_com.snc.work_management.demo" class="plugin_reference"><td class="name">

Field Service Management Demo Data\[com.snc.work\_management.demo\]

</td><td class="description">

Demonstration Data for Field Service Management covering the medical and telecommunication domains. NOTE: Installing this plugin adds new Configuration Item tables and relationships to the database.

</td><td>

Inactive

</td><td class="has_demo_data">

true

</td><td class="requires" id="entry_kbb_35c_d1b">

-   com.snc.work\_management
-   com.snc.wo\_signature\_pad

</td></tr><tr id="plugin_com.snc.work_management_geolocation.demo" class="plugin_reference"><td class="name">

Field Service Management Geolocation Demo Data\[com.snc.work\_management\_geolocation.demo\]

</td><td class="description">

Enables geolocation capabilities for the Field Service Management application.

</td><td>

Inactive

</td><td class="has_demo_data">

true

</td><td class="requires">

com.snc.work\_management.demo

</td></tr><tr id="plugin_com.snc.work_management_m" class="plugin_reference"><td class="name">

Field Service Management Mobile\[com.snc.work\_management\_m\]

</td><td class="description">

Adds the Field Service Management menu to the mobile user interface.

</td><td>

Inactive

</td><td class="has_demo_data">

true

</td><td class="requires">

-   com.snc.service\_management\_m
-   com.snc.work\_management

</td></tr><tr><td>

Field Service Management Scheduling Flow Designer Flows\[com.snc.sn\_app\_fsm\_scheduling\_flows\]

 \(New in Utah\)

</td><td>

Updates an agent’s schedule to maximize utilization if an unplanned event happens during their shift.

</td><td>

Inactive

</td><td>

false

</td><td>

-   com.snc.work\_management
-   com.snc.dynamic\_scheduling
-   com.snc.agent\_schedule

</td></tr><tr><td class="name">

Field Service - Questionnaire\[com.snc.wm\_questionnaire\]

</td><td class="description">

Create Questionnaires for Work Orders or Work Orders Tasks.

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

 

</td></tr><tr><td>

Field Service Map\[com.snc.fsm\_map\]

</td><td>

Displays the dispatch map for viewing agents, tasks, and agent routes.

</td><td>

Active

</td><td>

 

</td><td>

com.snc.work\_management

</td></tr><tr><td>

Field Service Management Agent Workspace\[com.snc.agent\_workspace.fsm\]

</td><td>

Enables field service users to manage work orders and tasks using the FSM agent workspace. This plugin activates the Agent Workspace \(com.agent\_workspace\) plugin.

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Field Service Multi-Day Task Scheduling\[com.snc.fsm\_multiday\_tasks\]

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td class="name">

Field Service - Signature Pad\[com.snc.wo\_signature\_pad\]

</td><td class="description">

Create PDFs for closed work orders that include the name and signature of the customer and a summary of the completed work.

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

-   com.snc.pdf\_generator
-   com.snc.signaturepad

</td></tr><tr><td>

Field Service Resource Scheduling \[com.snc.fsm\_resource\_scheduling\]

 \(New in Utah\)

</td><td>

Enables setup of shared equipment like cranes, diggers to be set up as schedulable resources.

</td><td>

Active

</td><td>

true

</td><td>

com.snc.fsm\_crew\_scheduling

</td></tr><tr><td>

Field Service Spoke\[com.snc.field\_service.spoke\]

</td><td>

Enables Flow Designer users to automate the creation of work orders and work order tasks and updates to existing work orders and work order tasks.

</td><td>

Inactive

</td><td>

false

</td><td>

Flow Designer - Installer \(com.glide.hub\)

</td></tr><tr><td>

Field Service Task Bundling\[com.snc.fsm\_task\_bundle\]

 \(Available in the ServiceNow Store\)

</td><td>

Enables the management of bundled work order tasks.

</td><td>

Active

</td><td>

false

</td><td>

com.snc.work\_management

</td></tr><tr><td>

Field Service Territory Planning\[com.snc.fsm\_territory\_planning\]

 \(New in Tokyo\)

</td><td>

Enables definition and management of Territories for Field Service specific use cases. By using Field Service Territory Management with work orders and resources, customers can make sure that work order tasks are scheduled only to field agents with a matching territory.

</td><td>

Active

</td><td>

true

</td><td>

-   com.snc.work\_management
-   com.snc.territory\_planning

</td></tr><tr><td>

Field Service with Project Management\[com.snc.wm\_ppm\]

</td><td>

Enables Field Service Management integration with the Project Management application. This plugin activates the Project Management plugin, which may require additional licenses.

</td><td>

Inactive

</td><td>

true

</td><td class="requires">

-   com.snc.work\_management
-   com.snc.financial\_planning\_pmo

</td></tr><tr><td>

Field Service with Project Management Demo\[com.snc.wm\_ppm\_demo\]

</td><td>

Demonstration data for the Field Service Management integration with the Project Management application.

</td><td>

Inactive

</td><td>

false

</td><td class="requires">

-   com.snc.wm\_ppm
-   com.snc.work\_management.demo
-   com.snc.customerservice.demo

</td></tr><tr><td>

Field Service with Service Locations support\[com.snc.fsm\_service\_locations\]

</td><td>

Enables to create a new service location from the WO/WOT whenever the preferred location does not exist among the stored locations.

</td><td>

Active

</td><td>

true

</td><td>

com.snc.work\_management,com.sn\_fsm\_components

</td></tr><tr><td>

Finance Close Automation\[sn\_fcms\]

</td><td>

Reduce close risk with intelligent task automation

</td><td>

Inactive

</td><td>

true

</td><td class="requires">

-   sn\_fin
-   sn\_fcms\_intg
-   com.glide.scope.access.restricted\_caller

</td></tr><tr><td>

Finance Common Architecture\[com.sn\_fin\]

\(Available in the ServiceNow Store\)

</td><td>

Maintains primary data such as Enterprise Resource Planning \(ERP\) sources, legal entities, accounting periods, and so on.

</td><td>

Inactive

</td><td>

true

</td><td>

-   com.snc.fiscal\_calendar
-   com.snc.fin\_dep
-   com.glide.scope.access.restricted\_caller
-   com.glide.web\_service\_insert\_multiple

</td></tr><tr><td>

Finance – ERP Integration\[com.sn\_fcms\_integrations\]

\(Starting with the Utah  release, Finance – ERP Integration is renamed as ERP Integration Framework.\)

\(Available in the ServiceNow Store\)

</td><td>

Provides integration support between the ServiceNow platform and common ERP systems.

</td><td>

Inactive

</td><td>

false

</td><td class="requires">

 

</td></tr><tr id="plugin_com.snc.finance_service_automation" class="plugin_reference"><td class="name">

Finance Service Management\[com.snc.finance\_service\_automation\]

 \(Maintenance mode only\)

 Planned for deprecation in March 2025 or subscription term end.

</td><td class="description">

Manages finance requests and enables users to report and track those requests. Activation of this plugin on production instances may require a separate license. Contact ServiceNow for details.

</td><td>

Inactive

</td><td class="has_demo_data">

true

</td><td class="requires">

com.snc.service\_management.core

</td></tr><tr id="plugin_com.snc.finance_service_automation_m" class="plugin_reference"><td class="name">

Finance Service Management Mobile\[com.snc.finance\_service\_automation\_m\]

</td><td class="description">

Manages Finance Service Management mobile components.

</td><td>

Inactive

</td><td class="has_demo_data">

true

</td><td class="requires">

-   com.snc.finance\_service\_automation
-   com.snc.service\_management\_m

</td></tr><tr><td>

Financial Charging\[com.snc.service\_charging\]

</td><td>

Enables financial analysts and business unit owners to measure and show charges based on the actual consumption of services. Get insight into your services and the utilization of those services by each department.

 Activation of this plugin on production instances may have licensing implications. Contact your ServiceNow account team for details.

</td><td>

Inactive

</td><td>

true

</td><td>

com.snc.itfm\_core

</td></tr><tr id="plugin_com.snc.financial_management" class="plugin_reference"><td class="name">

Modeling Engine\[com.snc.financial\_management\]

</td><td class="description">

Enables financial analysts to assemble spending data, build cost models, and generate reports to show how funds are being used. Activation of this plugin on production instances may have licensing implications. Contact your ServiceNow account team for details.

</td><td>

Inactive

</td><td class="has_demo_data">

true

</td><td class="requires">

-   com.snc.itfm\_core
-   com.snc.financial\_planning
-   com.snc.cost\_management
-   com.snc.service\_charging

</td></tr><tr><td>

Financial Management For APM\[com.snc.financial\_management\_for\_apm\]

</td><td>

Enables integration Financial Management with Application Portfolio Management providing preconfigured Cost Models.Activation of this plugin on production instances may have licensing implications. Contact your ServiceNow account team for details.

</td><td>

Active

</td><td>

false

</td><td>

com.snc.financial\_management

</td></tr><tr><td class="name">

Financial Management for CSM\[com.snc.financial\_management\_for\_csm\]

</td><td class="description">

Plugins for Customer Service Management and Field Service Management provide integration with the Financial Management application. These plugins add cost allocations for the CSM and FMS applications as well as dashboards and reports. Financial administrators can use these cost allocations on the Financial Management workbench to allocate, track, and report on expenses.

</td><td>

Inactive

</td><td class="has_demo_data">

true

</td><td class="requires">

-   com.snc.financial\_management
-   com.sn\_customerservice

</td></tr><tr><td>

Financial Management For FSM\[com.snc.financial\_management\_for\_fsm\]

</td><td>

Enables integration Financial Management with Field Service Management providing preconfigured Cost Models and a dashboard.

 Activation of this plugin on production instances may have licensing implications. Contact your ServiceNow account team for details.

</td><td>

Inactive

</td><td>

true

</td><td class="requires">

-   com.snc.financial\_management
-   com.snc.work\_management
-   com.snc.pa
-   com.snc.pa.fm.fsm

</td></tr><tr><td>

Financial Management for SPM\[com.snc.financial\_management\_for\_spm\]

</td><td>

Enables integration of Financial Management with Service Portfolio Management providing preconfigured Cost Models. Activation of this plugin on production instances may have licensing implications. Contact your ServiceNow account team for details.

</td><td>

Active

</td><td>

true

</td><td class="requires">

-   com.snc.financial\_management
-   com.spm\_owner\_workspace

</td></tr><tr><td>

Financial Planning\[com.snc.financial\_planning\_default\_definition\]

</td><td>

Provides preconfigured Financial Plan Definition and all its artifacts which enables Financial Analysts to plan for costs, make forecasts, and evaluate actual expenses versus planned expenses. Planning take into consideration a wide range of items in your infrastructure, including assets, labor, and the configuration items in the CMDB. Activation of this plugin on production instances may have licensing implications. Contact your ServiceNow account team for details.

</td><td>

Inactive

</td><td>

true

</td><td>

com.snc.financial\_planning

</td></tr><tr><td>

Financial Services Operations - Core\[com.sn\_bom\]

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Financial Services Business Customers Lifecycle Operations\[com.sn\_bom\_clo\_b2b\]

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Financial Services Business Deposit Operations\[com.sn\_bom\_deposit\_b2b\]

 \(New in San Diego\)

</td><td>

Application specific to business deposit operations focused on origination, servicing, and closure of deposit accounts and is part of the Financial Services Operations product.

</td><td>

Inactive

</td><td>

true

</td><td>

-   com.snc.csm\_contributor\_user
-   sn\_csm\_playbook
-   sn\_bom
-   sn\_bom\_document

</td></tr><tr><td>

Financial Services Complaint Management\[com.sn\_bom\_compl\]

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Financial Services Know Your Customer\[com.sn\_bom\_kyc\]

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Financial Services Personal Customers Lifecycle Operations\[com.sn\_bom\_clo\_b2c\]

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Financial Services Personal Deposit Operations\[com.sn\_bom\_deposit\_b2c\]

 \(New in San Diego\)

</td><td>

Application specific to personal deposit operations focused on origination, servicing, and closure of deposit accounts and is part of the Financial Services Operations product.

</td><td>

Inactive

</td><td>

true

</td><td>

-   com.snc.csm\_contributor\_user
-   sn\_csm\_playbook
-   sn\_bom
-   sn\_bom\_document

</td></tr><tr><td>

Financial Services Remote Tables\(New in San Diego\)

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Financial Services Treasury Operations\[com.sn\_bom\_treasury\]

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr id="plugin_com.snc.fiscal_calendar" class="plugin_reference"><td class="name">

Fiscal Calendar\[com.snc.fiscal\_calendar\]

</td><td class="description">

Enables to generate and manage different kinds of Fiscal calendar which is used in various Financial applications. Activation of this plugin on production instances may have licensing implications. Contact your ServiceNow account team for details.

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

com.glide.dynamic\_operands.datetime

</td></tr><tr id="plugin_com.snc.fixed_asset" class="plugin_reference"><td class="name">

Fixed Asset\[com.snc.fixed\_asset\]

</td><td class="description">

Core fixed asset tracking

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

 

</td></tr><tr><td>

Fixed Costs\[com.snc.fixed\_costs\]

</td><td>

Fixed Costs

</td><td>

Active

</td><td>

false

</td><td>

com.glide.metrics

</td></tr><tr><td>

Flow Client\[com.glide.hub.flow.client\]

</td><td>

The client side API for interacting with flows, subflows, and actions

</td><td>

Active

</td><td>

false

</td><td>

com.glide.hub.scriptable.plan.runners

</td></tr><tr><td>

Flow Designer - Designer\[com.glide.hub.designer\]

</td><td>

Flow Designer - Designer

</td><td>

Active

</td><td>

false

</td><td>

com.glide.hub.designer\_backend.suite

</td></tr><tr><td>

Flow Designer - Engine Reporting Dashboard\[com.glide.hub.flow\_reporting.dashboard\]

</td><td>

Flow Engine Reporting PA Dashboard for Flow Designer.

</td><td>

Active

</td><td>

false

</td><td class="requires">

-   com.glide.hub.flow\_reporting
-   com.glide.dashboards

</td></tr><tr><td>

Flow Designer - Flow Engine\[com.glide.hub.flow\_engine\]

</td><td>

Flow Designer runtime components.

</td><td>

Active

</td><td>

false

</td><td>

 

</td></tr><tr><td>

Flow Designer - Flow Engine Reporting\[com.glide.hub.flow\_reporting\]

</td><td>

Flow Engine Reporting components.

</td><td>

Active

</td><td>

false

</td><td class="requires">

-   com.glide.hub.flow\_engine
-   com.glideapp.dashboards

</td></tr><tr><td>

Flow Designer - Installer\[com.glide.hub\]

</td><td>

Suite of plugins necessary to support the Flow Designer Designer App.

</td><td>

Active

</td><td>

false

</td><td>

-   Flow Designer - Flow Engine
-   Flow Designer - Flow Engine Reporting
-   com.glide.hub.flow\_reporting.dashboard
-   Outbound Tracking
-   Flow Designer Action Step - Log
-   Flow Designer Action Step - Script
-   Flow Designer Action Step - CRUD
-   com.glide.hub.action\_step.notification
-   Flow Designer Action Step - CORE
-   com.glide.hub.action\_step.service\_catalog
-   com.glide.hub.designer\_backend.model
-   Flow Designer Action Step - Email
-   Flow Designer System Level Actions
-   Connect Spoke for Flow Designer
-   Flow Designer - Designer
-   com.glide.hub.action\_step.email\_header
-   com.glide.hub.action\_step.look\_up\_email\_attachments
-   App Dependency Client

</td></tr><tr><td>

Flow Designer Action Step - CORE\[com.glide.hub.action\_step.core\]

</td><td>

Action Step - Core operations on GlideRecord.

</td><td>

Active

</td><td>

false

</td><td>

com.glide.hub.action\_step.template

</td></tr><tr><td>

Flow Designer Action Step - CRUD\[com.glide.hub.action\_step.crud\]

</td><td>

Action Step - CRUD operations on GlideRecord.

</td><td>

Active

</td><td>

false

</td><td>

com.glide.hub.action\_step.template

</td></tr><tr><td>

Flow Designer Action Step - Email\[com.glide.hub.action\_step.email\]

</td><td>

Action step for emails.

</td><td>

Active

</td><td>

false

</td><td class="requires">

-   com.glide.email.service
-   com.glide.hub.action\_step.template

</td></tr><tr><td>

Flow Designer Action Step - Log\[com.glide.hub.action\_step.log\]

</td><td>

Action Step - Log.

</td><td>

Active

</td><td>

false

</td><td>

com.glide.hub.action\_step.template

</td></tr><tr><td>

Flow Designer Action Step - Notification\[com.glide.hub.action\_step.notification\]

</td><td>

Action steps for notifications.

</td><td>

Active

</td><td>

false

</td><td class="requires">

-   com.glide.notification
-   com.glide.hub.action\_step.template

</td></tr><tr><td>

Flow Designer Action Step - Payload Builder\[com.glide.hub.action\_step.payload\]

</td><td>

Action Step - Payload Builder

</td><td>

Active

</td><td>

false

</td><td>

com.glide.hub.action\_step.template

</td></tr><tr><td>

Flow Designer Action Step - Script\[com.glide.hub.action\_step.script\]

</td><td>

Action Step - Script.

</td><td>

Active

</td><td>

false

</td><td>

com.glide.hub.action\_step.template

</td></tr><tr><td>

Flow Designer Action Step - Service Catalog\[com.glide.hub.action\_step.service\_catalog\]

</td><td>

Action Step - Service Catalog.

</td><td>

Active

</td><td>

false

</td><td>

com.glide.hub.action\_step.template

</td></tr><tr><td>

Flow Designer Action Step Template\[com.glide.hub.action\_step.template\]

</td><td>

Action Step Template Design Time components.

</td><td>

Active

</td><td>

false

</td><td>

 

</td></tr><tr><td>

Flow Designer Action Trigger\[com.glide.hub.flow\_trigger\]

</td><td>

Action plans that map a Trigger \(Record, Email, REST\) to an Action.

</td><td>

Active

</td><td>

false

</td><td>

com.glide.hub.flow\_engine

</td></tr><tr><td>

Flow Designer Designer Backend\[com.glide.hub.designer\_backend.suite\]

</td><td>

Suite of plugins necessary to support the Flow Designer Designer App.

</td><td>

Active

</td><td>

false

</td><td class="requires">

-   com.glide.hub.action\_step.log
-   com.glide.hub.action\_step.script
-   com.glide.hub.action\_step.crud
-   com.glide.hub.action\_step.email
-   com.glide.hub.action\_step.notification
-   com.glide.hub.action\_step.core
-   com.glide.hub.designer\_backend.model
-   com.glide.hub.action\_type.system

</td></tr><tr><td>

Flow Designer Designer Model\[com.glide.hub.designer\_backend.model\]

</td><td>

Data model and REST API for representing Process Plans as Flows, Actions, and Steps.

</td><td>

Active

</td><td>

false

</td><td class="requires">

-   com.glide.element\_mapping
-   com.glide.hub.flow\_engine
-   com.glide.hub.flow\_trigger
-   com.glide.hub.flow\_reporting
-   com.glide.hub.action\_step.template

</td></tr><tr><td>

Flow Designer Scriptable Plan Runner API's\[com.glide.hub.scriptable.plan.runners\]

</td><td>

The API's needed to run flows, subflows, and actions through script.

</td><td>

Active

</td><td>

false

</td><td>

com.glide.hub.flow\_engine

</td></tr><tr><td>

Flow Designer support for the Service Catalog\[com.glideapp.servicecatalog.flow\_designer\]

</td><td>

Service Catalog Flow Designer

</td><td>

Active

</td><td>

true

</td><td>

com.glide.hub.flow\_trigger.catalog

</td></tr><tr><td>

Flow Designer System Level Actions\[com.glide.hub.action\_type.system\]

</td><td>

Action Type Definitions for low-level functions such as GlideRecord operations.

</td><td>

Active

</td><td>

false

</td><td>

com.glide.hub.designer\_backend.model

</td></tr><tr><td>

Flow Template Builder\[com.sn\_flow\_template\]

 \(New in San Diego\)

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr id="plugin_com.glide.ui.ng.fd" class="plugin_reference"><td class="name">

Form Designer\[com.glide.ui.ng.fd\]

</td><td class="description">

Form Designer

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

-   com.glide.ui.ng.dc
-   com.glide.ui.tablet.theme
-   com.glide.ui.ng
-   com.glide.ui.themes.doctype

</td></tr><tr id="plugin_com.glide.ui.personalize_form" class="plugin_reference"><td class="name">

Form Personalization\[com.glide.ui.personalize\_form\]

</td><td class="description">

Enables users to personalize the layout for any form view.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

com.glide.ui.doctype

</td></tr><tr><td>

FSM Agent Workspace\[com.snc.agent\_workspace.fsm\]

</td><td>

Enables users to manage work orders and tasks within the agent workspace.

</td><td>

Inactive

</td><td>

false

</td><td>

com.agent\_workspace

</td></tr><tr><td>

FSM Shift Scheduling \[com.snc.sn\_fsm\_shift\_schdl\]

 \(Available in the ServiceNow Store\)

</td><td>

Enables the management of agent shift Scheduling functionalities for Field Service Management Workforce Optimization.

</td><td>

Active

</td><td>

true

</td><td>

-   com.snc.sn\_wfo\_cfg\_ws
-   com.sn\_shift\_planning\_host
-   com.snc.uib.agent\_shift\_planning
-   com.snc.skills\_management
-   com.snc.skill\_determination
-   com.snc.sn\_wfo\_skill\_review
-   com.glide.dynamic\_translation

</td></tr><tr><td>

FSM Team Performance Management \[com.snc.sn\_fsm\_team\_mgmt\]

 \(Available in the ServiceNow Store\)

</td><td>

Manages the team performance functionalities for Field Service Management Workforce Optimization.

</td><td>

Active

</td><td>

true

</td><td>

-   com.snc.sn\_fsm\_shift\_schdl
-   com.sn\_team\_perf
-   com.snc.pa
-   com.snc.pa.insights
-   com.snc.pa.spotlight
-   com.snc.work\_management\_pa

</td></tr><tr><td>

FSO Process Optimization Content Pack\[sn\_bom\_po\]

 \(Available in the ServiceNow Store\)

</td><td>

Provides Process Optimization capabilities to Financial Services Operations applications.

</td><td>

Inactive

</td><td>

false

</td><td>

-   com.sn\_process\_optimization
-   sn\_bom

</td></tr><tr><td class="name">

Fullcalendar Library\[com.snc.fullcalendar\]

</td><td class="description">

Fullcalendar library v2.5.0.

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

 

</td></tr><tr id="plugin_com.snc.geolocation" class="plugin_reference"><td class="name">

Geolocation\[com.snc.geolocation\]

</td><td class="description">

Uses Google Maps to track users, plan efficient routes between locations, and assist in finding accurate travel times. The system locates users from latitude and longitude information provided by their mobile devices.

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

 

</td></tr><tr><td>

Github Spoke\[com.sn.github.spoke\]

</td><td>

The GitHub Spoke for IntegrationHub provides actions that a Process Analyst can use when designing flows. The actions allow them to automate GitHub tasks.

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Gitlab Spoke\[com.sn.gitlab.spoke\]

</td><td>

The GitLab Spoke for IntegrationHub provides actions that a Process Analyst can use when designing flows. The actions allow them to automate Gitlab.

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Glide Conversation Server\[com.glide.cs\]

</td><td>

Glide Conversation Server.

</td><td>

Inactive

</td><td>

true

</td><td class="requires">

-   com.glide.connect.support
-   com.glide.cs.branding
-   com.glide.cs.live\_agent\_settings
-   com.glide.cs.sn-va-web-client-app

</td></tr><tr><td>

Glide Conversation Server Adapters\[com.glide.cs.adapter\]

</td><td>

Glide Conversation Server Adapters

</td><td>

Active

</td><td>

false

</td><td class="requires">

-   com.glide.cs
-   com.glide.external.app
-   com.glide.channelproxy
-   com.snc.bot\_install\_ui

</td></tr><tr id="plugin_com.glide.metadata" class="plugin_reference"><td class="name">

Glide Metadata\[com.glide.metadata\]

</td><td class="description">

Core metadata support.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

 

</td></tr><tr id="plugin_com.glide.metadata_delete" class="plugin_reference"><td class="name">

Glide Metadata Delete\[com.glide.metadata\_delete\]

</td><td class="description">

Core metadata delete support.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

-   com.snc.metadata
-   com.snc.metadata\_tree

</td></tr><tr><td>

Glide Logging Framework Extensions\[com.glide.log\]

</td><td>

Contains extensions to glide logging framework and script API.

</td><td>

Active

</td><td>

false

</td><td>

None

</td></tr><tr><td>

Glide Notification Translation\[com.glide.notification.translation\]

 \(New in Tokyo\)

</td><td>

Adds the ability to send multi-lingual emails based on recipient preferences.

</td><td>

Active

</td><td>

false

</td><td>

com.glide.localization\_framework.installer

</td></tr><tr><td>

Glide Virtual Agent\[com.glide.cs.chatbot\]

</td><td>

Activates the Virtual Agent framework and the other necessary plugins.

</td><td>

Active

</td><td>

false

</td><td>

-   com.glide.cs.chatbot.lite
-   com.glide.cs.custom.adapter
-   com.glide.cs.nlu.topics
-   com.glide.nlu.intent.discovery
-   com.glide.nlu.ibmwatson.intent.discovery
-   com.glide.nlu.msluis.intent.discovery

</td></tr><tr><td>

Glide Virtual Agent Lite\[com.glide.cs.chatbot.lite\]

</td><td>

Activates the lite version of the Virtual Agent bot platform and other necessary plugins.

</td><td>

Active

</td><td>

false

</td><td>

-   com.glide.cs
-   com.glide.va.sp\_widgets
-   com.glide.cs.adapter
-   com.glide.cs.settings
-   com.glide.cs.topics
-   com.glide.service-portal.agent-chat
-   com.glide.cs.topic\_blocks
-   com.snc.conversation\_builder

</td></tr><tr><td>

Global Application File Management\[com.snc.global\_app\_files\]

</td><td>

UI components and utilities for managing application files in the global scope.

</td><td>

Active

</td><td>

false

</td><td class="requires">

-   com.glide.scripted\_rest\_services
-   com.glide.ui.ng

</td></tr><tr><td>

Goal Framework\[sn\_gf\]

 \(Available in the ServiceNow Store\)

</td><td>

Enables strategic planning and helps define and construct strategic priorities and associate goals for the organization. This application facilitates personas such as strategy officers, SRO, ePMO, and portfolio managers to track strategy execution by associating work and planning items such as demand, project, and portfolio to the defined goals.

</td><td>

Active

</td><td>

false

</td><td>

None

</td></tr><tr><td>

Goal Framework for SPM\[sn\_gfa\]

 \(Available in the ServiceNow Store\)

</td><td>

Provides the capability to monitor the goal progress in real time by automating the actual value of the targets from any source present on the ServiceNow AI Platform.

</td><td>

Active

</td><td>

true

</td><td>

sn\_gf

</td></tr><tr><td>

Google Calendar Spoke\[com.sn.gcalendar.spoke\]

</td><td>

The Google Calendar Spoke for IntegrationHub provides actions that a Process Analyst can use when designing flows. The actions allow them to automate Google Calendar.

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr id="plugin_com.glideapp.google_maps" class="plugin_reference"><td class="name">

Google Maps plugin\[com.glideapp.google\_maps\]

</td><td class="description">

Allows the display of Google Maps within the product as map pages.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

-   com.glide.ui.ng
-   com.glide.rest.service

</td></tr><tr><td>

Granular Delegation\[com.glide.granular\_service\_delegation\]

</td><td>

Delegate specific assignments and approvals to another user for a period of time.

</td><td>

Inactive

</td><td>

false

</td><td>

 

</td></tr><tr><td>

GraphQL Schema for Contextual Search\[com.snc.contextual\_search.graphql\]

</td><td>

Provides GraphQL schema for contextual search services

</td><td>

true

</td><td>

false

</td><td>

com.glide.graphql

</td></tr><tr><td>

GraphQL Schema for Knowledge in Contextual Search Application Portfolio Management\[com.snc.knowledge3.graphql\]

</td><td>

Provides GraphQL schema for contextual search sources like Knowledge

</td><td>

true

</td><td>

false

</td><td>

com.snc.contextual\_search.graphql

</td></tr><tr id="plugin_com.sn_audit" class="plugin_reference"><td class="name">

GRC: Audit Management\[com.sn\_audit\]

</td><td class="description">

The GRC: Audit Management application provides a centralized process for Internal Audit teams to automate the complete audit life cycle. Project driven audits allow auditors to quickly scope engagements, conduct fieldwork, collect control evidence, and track audit observations.

</td><td>

Inactive

</td><td class="has_demo_data">

true

</td><td class="requires">

-   com.sn\_grc
-   com.glide.ui.ng
-   com.snc.common\_workbench

</td></tr><tr><td>

GRC: Audit Management Workspace\[sn\_audit\_workspace\]

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

GRC: Business Continuity Management – Components\[sn\_bcm\_components\]

</td><td>

Provides seismic components for Business Continuity Management application

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

GRC: Business Continuity Management – Core\[sn\_bcm\]

</td><td>

Provides capabilities to configure the core data and workspace that are required for the business continuity management applications.

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

GRC: Business Continuity Planning\[sn\_bcp\]

</td><td>

Provides capabilities for business continuity management teams to create, review, and approve business continuity and disaster recovery plans.

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

GRC: Business Impact Analysis\[sn\_bia\]

</td><td>

Provides structured workflows for business continuity management teams to assess the impact of a disruption to critical resources such as business processes, applications, and locations.

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

GRC: Crisis Management\[sn\_recovery\]

</td><td>

Provides capabilities for business continuity management teams to activate business continuity plans during plan exercises and actual crisis events.

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

GRC: Compliance UCF\[com.sn\_comp\_ucf\]

</td><td>

The GRC: Compliance UCF plugin is an add-on that provides GRC: Policy and Compliance Management with the capability to download regulatory content and common controls from the Unified Compliance Framework \(UCF\).

</td><td>

Inactive

</td><td>

false

</td><td>

com.sn\_compliance

</td></tr><tr><td>

GRC:Mobile\[com.sn\_grc\_mobile\]

</td><td>

There are two GRC core applications that are viewed on the GRC Mobile app: Policy and Compliance Management and Risk Management. There are two GRC core applications that are viewed on the GRC Mobile app: Policy and Compliance Management and Risk Management.

</td><td>

Inactive

</td><td>

false

</td><td>

com.glide.sg , com.glide.sg.agent\_native\_client

</td></tr><tr><td>

GRC: Performance Analytics Integration\[com.sn\_grc\_pa\]

</td><td>

GRC: Performance Analytics Integration enables risk and compliance managers to continuously monitor key risk and control indicators using the advanced reporting capabilities provided by Performance Analytics.

</td><td>

Inactive

</td><td>

false

</td><td>

com.sn\_grc

</td></tr><tr id="plugin_com.sn_compliance" class="plugin_reference"><td class="name">

GRC: Policy and Compliance Management\[com.sn\_compliance\]

</td><td class="description">

The GRC: Policy and Compliance Management application provides a centralized process for creating and managing policies, standards, and internal control procedures that are cross-mapped to external regulations and best practices. The application provides structured workflows for the identification, assessment, and continuous monitoring of control activities.

</td><td>

Inactive

</td><td class="has_demo_data">

true

</td><td class="requires">

-   com.sn\_grc
-   com.snc.comp\_attest

</td></tr><tr><td>

GRC: Predictive Intelligence\[com.sn\_grc\_pred\_intel\]

</td><td>

Enables customers to utilize the machine learning algorithms for a wide variety of GRC use cases such as Issue Assignment. This plugin may require a separate license. Contact ServiceNow for details.

</td><td>

Inactive

</td><td>

false

</td><td class="requires">

-   com.glide.platform\_ml
-   com.sn\_grc

</td></tr><tr><td>

GRC: GRC Profile Dependencies\[com.snc.grc\_profile\_dep\]

</td><td>

Installs all the dependent plugins required to support the GRC Profile application.

</td><td>

Active

</td><td>

false

</td><td class="requires">

-   com.snc.grc.common
-   com.snc.planned\_task\_v2

</td></tr><tr><td>

GRC: Regulatory Change Management\[com.sn\_grc\_reg\_change\]

</td><td>

The Regulatory Change Management application enables customers to check upcoming regulatory changes, assess their impact, and implement risk and compliance-related changes, ensuring overall regulatory compliance.

</td><td>

Active

</td><td>

true

</td><td>

-   com.snc.grc\_policy\_dep
-   com.snc.grc\_profile\_dep
-   com.snc.grc\_risk\_dep
-   com.glide.hub.action\_step.sftp
-   com.glide.hub.action\_type.datastream
-   com.glide.hub.integration.runtime

</td></tr><tr><td>

GRC integration with Thomson Reuters Regulatory Intelligence\[com.sn\_grc\_int\_tr\]

</td><td>

Use the GRC integration with Thomson Reuters Regulatory Intelligence application to integrate with the Thomson Reuters platform and to consume the Thomson Reuters Regulatory Intelligence \(TRRI\) feeds into your ServiceNow  instance.

</td><td>

Active

</td><td>

true

</td><td>

-   com.snc.grc\_profile\_dep
-   com.snc.grc\_policy\_dep
-   com.snc.grc\_risk\_dep

</td></tr><tr><td>

GRC: Advanced Risk\[com.sn\_risk\_advanced\]

</td><td>

As a decision-maker, at any level of the business, you can view up-to-date information regarding your organization's risk posture. Link intermediate risk statements to risks, as well as enterprise-level risk statements. Your risk management team can provide a rollup of risk statements and scores from the most granular risk to the highest enterprise-level risk statement.​ Additionally, as a risk manager, you can monitor risk events, relate them to existing risks, perform root-cause analysis, and track all remediation tasks.

</td><td>

Active

</td><td>

true

</td><td class="requires">

-   com.snc.grc\_profile\_dep
-   com.snc.grc\_risk\_dep

</td></tr><tr><td>

GRC: DevOps Accelerator\[com.sn\_grc\_devops\]

 \(Available in the ServiceNow Store\)

</td><td>

Maps the control objectives drawn from regulations, standards, and frameworks, such as CIS controls, NIST 800-53, ISO 27002, PCI DSS etc., to DevOps Policy as a Code Engine \(PaCE\). These policies are provided by the DevOps Config Policy Content Pack. This allows compliance and DevOps managers to preventatively monitor control compliance, get real-time visibility into evidence of PaCE policy execution, and allow for exception management.

</td><td>

Active

</td><td>

false

</td><td>

None

</td></tr><tr id="plugin_com.sn_risk" class="plugin_reference"><td class="name">

GRC: Risk Management\[com.sn\_risk\]

</td><td class="description">

The GRC: Risk Management application provides a centralized process to identify, assess, respond to, and continuously monitor Enterprise and IT risks that may negatively impact business operations. The application also provides structured workflows for the management of risk assessments, risk indicators, and risk issues.

</td><td>

Inactive

</td><td class="has_demo_data">

true

</td><td class="requires">

-   com.sn\_grc
-   com.snc.risk\_asmt

</td></tr><tr><td>

GRC: Risk Management Dependencies\[com.snc.grc\_vrm\_dep\]

</td><td>

Installs all the dependent plugins required to support the GRC Risk Management application.

</td><td>

Active

</td><td>

false

</td><td class="requires">

-   com.snc.grc\_profile\_dep
-   com.snc.risk\_asmt

</td></tr><tr><td>

GRC: SIG Questionnaire Integration\[com.sn\_sig\_asmt\]

</td><td>

The GRC: SIG Questionnaire Integration plugin installs the Shared Assessments Standardized Information Gathering \(SIG\) questionnaire for use with the GRC: Vendor Risk Management application.

</td><td>

Inactive

</td><td>

true

</td><td class="requires">

-   com.snc.assessment\_core
-   com.sn\_vdr\_risk\_asmt
-   com.snc.sig\_asmt\_core
-   com.snc.document\_management

</td></tr><tr><td>

GRC: Vendor Risk Management\[com.sn\_vdr\_risk\_asmt\]

</td><td>

The GRC: Vendor Risk Management application allows risk management stakeholders to identify, assess, and manage risk across the vendor ecosystem.

</td><td>

Inactive

</td><td>

true

</td><td class="requires">

-   com.sn\_comp\_asmt
-   com.snc.vendor\_core
-   com.sn\_grc
-   com.snc.vdr\_risk\_asmt\_designer
-   com.snc.vendor\_portal

</td></tr><tr><td>

GRC: Vendor Risk Management Dependencies\[com.snc.grc\_vrm\_dep\]

</td><td>

Installs all the dependent plugins required to support the GRC Vendor Risk Management application.

</td><td>

Active

</td><td>

false

</td><td class="requires">

-   com.snc.grc\_profile\_dep
-   com.snc.vdr\_risk\_asmt\_designer
-   com.snc.vendor\_core
-   com.snc.sig\_asmt\_core
-   com.snc.assessment\_core
-   com.snc.document\_management
-   com.snc.vendor\_portal

</td></tr><tr><td>

GRC:Virtual Agent\[com.sn\_grc\_virtual\_agent\]

</td><td>

The GRC:Virtual Agent provides chat bot functionality for common GRC operations.

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

GRC: Workbench\[com.sn\_grc\_workbench\]

</td><td>

The GRC Workbench utilizes CMDB information to show the upstream and downstream relationships across all applications. These relationships enable consistent risk mapping and modeling across the enterprise. The GRC Workbench does not work with Legacy GRC.

</td><td>

Inactive

</td><td>

false

</td><td>

com.sn\_grc

</td></tr><tr><td>

Group Life Servicing\[com.sn\_ins\_group\_life\]

 \(Available in the ServiceNow Store\)

</td><td>

Group life insurance management.

</td><td>

Active

</td><td>

true

</td><td>

com.snc.csm\_contributor\_user

</td></tr><tr><td>

Guided Application Creator\[com.glide.sn-guided-app-creator\]

</td><td>

Enables users to set up custom business applications that are immediately ready to use.

</td><td>

Active

</td><td>

false

</td><td>

com.sn\_appcreator

</td></tr><tr><td>

Guided Decisions \(Maintenance mode only\)\[com.snc.guided\_decisions\]

</td><td>

Enables the framework and execution engine for creating guided decisions.

</td><td>

Active

</td><td>

false

</td><td class="requires">

-   com.glide.decision\_table
-   com.snc.guided\_decisions\_guidance
-   com.glide.hub

</td></tr><tr><td>

Guided Decisions - Guidance \(Maintenance mode only\)\[com.snc.guided\_decisions\_guidance\]

</td><td>

Enables the framework for creating a guidance for guided decisions.

</td><td>

Active

</td><td>

false

</td><td class="requires">

-   com.glide.hub
-   com.snc.guided\_decisions\_guidance\_global

</td></tr><tr><td>

Guided Decisions - Guidance Global Entities \(Maintenance mode only\)\[com.snc.guided\_decisions\_guidance\_global\]

</td><td>

This global plugin is loaded as dependant of Guided Decisions Guidance to access global entities.

</td><td>

Active

</td><td>

false

</td><td>

 

</td></tr><tr><td>

News Integration for Supplier Lifecycle Operations\[com.snc.sn\_supplier\_news\]

\(Available in the ServiceNow Store\)

</td><td>

Retrieve recent news and other articles from preferred news channels. There is a pre-configured integration with Microsoft Bing available with this application.

</td><td>

Inactive

</td><td>

false

</td><td>

None

</td></tr><tr><td>

Guided Decision - Next Best Action\[com.snc.next\_best\_action\]

</td><td>

Recommends relevant actions like Guided Decisions for a given context. The plugin enables defining rules to recommend Next Best Actions.

</td><td>

Active

</td><td>

false

</td><td>

com.sn\_next\_best\_action\_list

</td></tr><tr><td>

Guided Decisions for Playbook in Workspace\[com.snc.guided\_decisions\_playbook\_experience\]

</td><td>

Enables activity types, definitions, and UI components for the display of guided decisions in a playbook on Workspace.

</td><td>

Active

</td><td>

false

</td><td class="requires">

-   com.snc.guided\_decisions
-   com.snc.guided\_decisions\_guidance
-   com.glide.playbook\_experience.config

</td></tr><tr><td>

Guided Decisions Experience\[sn\_ga\_exp\]

 \(Available in the ServiceNow Store\)

</td><td>

Enables customers to use Guided Decisions with Playbooks, Recommended Actions, and other features.

</td><td>

Inactive

</td><td>

false

</td><td>

com.snc.guided\_decision

</td></tr><tr><td>

Guided Setup Configuration\[com.glide.guided\_setup\_config\]

</td><td>

Provides customers with a configuration on the Guided Setup Content.

</td><td>

Active

</td><td>

false

</td><td>

 

</td></tr><tr><td>

Guided Setup for CMDB\[com.snc.cmdb.guided\_setup\]

</td><td>

Provides customers with a visual guidance to configure CMDB. Requires Core UI.

</td><td>

Active

</td><td>

false

</td><td class="requires">

-   com.snc.guided\_setup
-   com.snc.cmdb

</td></tr><tr><td>

Guided Setup for Performance Analytics\[com.snc.pa.guided\_setup\]

</td><td>

Provides customers with visual guidance to configure Performance Analytics. Requires Core UI.

</td><td>

Active

</td><td>

false

</td><td class="requires">

-   com.snc.guided\_setup
-   com.snc.pa
-   com.glideapp.dashboards

</td></tr><tr><td>

Guided Setup for ServiceNow Flow Designer\[com.glide.hub.flow\_designer\_guided\_tours\]

</td><td>

A guided tour instructing users on how to start creating a flow.

</td><td>

Active

</td><td>

false

</td><td>

 

</td></tr><tr><td>

Guided Setup Framework\[com.snc.guided\_setup\]

</td><td>

Provides customers with visual guidance to configure ServiceNow applications.

</td><td>

Active

</td><td>

false

</td><td class="requires">

-   com.glideapp.ui\_components
-   com.glide.scripted\_rest\_services
-   com.glide.embedded\_help
-   com.glide.scoped\_analytics\_framework

</td></tr><tr><td>

Guided Tour Designer\[com.glide.sn\_tourbuilder\]

</td><td>

ServiceNow Guided Tour Designer, aka GTD is a simplified way to create a guided tour. It provides easy to use, drag and drop interface to quickly build guided tours without writing any code. You can add, delete, modify, reorder steps as well as test the tour by previewing it.

</td><td>

Active

</td><td>

false

</td><td>

 

</td></tr><tr><td>

Guided Tours\[com.glide.guided\_tours\]

</td><td>

A guided tour provides a walk-through of a procedure in a UI page. Administrators can develop customized guided tours to assist users with specific business processes within an organization.

</td><td>

Active

</td><td>

false

</td><td class="requires">

-   com.glide.ui.hopscotch
-   com.glide.embedded\_help

</td></tr><tr><td>

Hardware Asset Management \(Maintenance mode only\)\[com.sn\_hamp\]

</td><td>

Hardware Asset Management Professional focuses on driving automation and prescriptive, standard practices for managing physical hardware assets throughout the end-to-end asset lifecycle from acquisition through disposition.

</td><td>

Active

</td><td>

false

</td><td>

com.sn\_hwnorm

</td></tr><tr><td>

Hardware Model Normalization\[com.sn\_hwnorm\]

</td><td>

Hardware normalization is a net new app planned for limited access in the Orlando release. This feature will enable customers with ITAM hardware normalization plugin to received standardized content to normalize records for IT hardware manufacturers, models and model lifecycles.

</td><td>

Inactive

</td><td>

true

</td><td class="requires">

-   com.snc.model
-   com.glide.data\_services\_canonicalization.client
-   com.sn\_glidequery

</td></tr><tr><td>

Health and Safety Incident Management\[sn\_ohs\_im\]

 \(Available in the ServiceNow Store\)

</td><td>

Enables organizations to record, investigate, and report on health and safety related employee incidents and observations.

</td><td>

Active

</td><td>

true

</td><td>

-   Plugins dependency:
    -   com.snc.app\_shell\_aw
    -   com.snc.uib.base\_agent\_workspace
    -   com.glide.playbook\_experience.config
    -   com.glide.pad.license
-   Store app dependency:
    -   sn\_wsd\_core
    -   sn\_ohs\_comp
    -   sn\_ohs\_im\_pa
    -   sn\_imt\_core
    -   sn\_ent

</td></tr><tr><td>

Health and Safety Incident Management OSHA Content Pack\[com.snc.sn\_hs\_im\_osha\]

 \(Available in the ServiceNow Store\)

</td><td>

Adds Occupational Safety and Health Administration \(OSHA\) report autofill and export capability to the Health and Safety Incident Management application.

</td><td>

Active

</td><td>

true

</td><td>

 

</td></tr><tr><td>

Health Log Analytics Core\[com.glideapp.itom.occultus\]

</td><td>

Essential components for Health Log Analytics scoped application.

</td><td>

 

</td><td>

false

</td><td>

-   com.glide.indexed-docstore.es
-   com.snc.clotho
-   com.itom.jutils
-   com.glide.services
-   com.glide.auth.mutual
-   com.glideapp.itom.snac

</td></tr><tr><td>

Health Log Analytics Viewer\[com.sn-log-viewer\]

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr id="plugin_com.glide.high_security" class="plugin_reference"><td class="name">

High Security Settings\[com.glide.high\_security\]

</td><td class="description">

Enables a high-security environment, including high-security system properties and access controls.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

com.glide.role\_management

</td></tr><tr id="plugin_com.glide.history_set" class="plugin_reference"><td class="name">

History Sets\[com.glide.history\_set\]

</td><td class="description">

Maintains sys\_history\_set and sys\_history\_line tables to view a record's audit, email, and relationship data in a table format.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

 

</td></tr><tr><td>

History Walker\[com.glide.history\_walker\]

</td><td>

Provides script access to History Walker

</td><td>

Active

</td><td>

false

</td><td>

 

</td></tr><tr><td>

Homepage Deprecation Help Tool\[sn\_home\_page\_depr\]

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr id="plugin_com.glideapp.home.splash_page" class="plugin_reference"><td class="name">

Homepage Splash Page\[com.glideapp.home.splash\_page\]

</td><td class="description">

Provides a splash page for homepages. Upon logging in, instead of going to home.do, users go to a splash page that gives them the ability to cancel the home page transaction. This is useful when homepages take a long time to load.**Important:**

The functionality found in homepages, arranging information from your instance to tell a story about your data, is found in dashboards on new instances. On upgraded instances with Next Experience enabled, users can view existing homepages if they have a direct URL, but they can't create or edit them. Responsive dashboards and Analytics Center dashboards take over homepage functionality.

Use the [Homepage deprecation help tool](https://www.servicenow.com/docs/access?context=homepage-deprecation-help-tool&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US) to convert the homepages on your instance to responsive dashboards.

For more information, see:

-   [Dashboards in the Analytics Center](https://www.servicenow.com/docs/access?context=analytics-center-dashboards&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US).
-   [Working with responsive dashboards](https://www.servicenow.com/docs/access?context=c_ResponsiveDashboards&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US).

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

com.glideapp.home

</td></tr><tr id="plugin_com.glide.ui.hopscotch" class="plugin_reference"><td class="name">

Hopscotch\[com.glide.ui.hopscotch\]

</td><td class="description">

Hopscotch is a framework to make it easy for developers to add product tours to their pages. Hopscotch accepts a tour JSON object as input and provides an API for the developer to control rendering the tour display and managing the tour progress. To learn more about Hopscotch and the API, check out http://linkedin.github.io/hopscotch.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

 

</td></tr><tr><td>

HR Service Delivery integration with Microsoft Teams\[sn\_now\_teams\_hr\]

 \(Available in the ServiceNow Store\)

</td><td>

The integration provides a broad set of service-delivery capabilities within Microsoft Teams, to help resolve employees’ HR requests. Employees will be able to get answers to questions, stay up to date on the latest news and events, report issues, and discuss open HR Cases with fulfillers.

</td><td>

Inactive

</td><td>

false

</td><td>

-   sn\_hr\_va
-   sn\_now\_teams

</td></tr><tr><td>

HR Service Delivery Integration with SuccessFactors\[sn\_hr\_sf\]

 \(Available in the ServiceNow Store\)

</td><td>

Synchronizes employee to-dos so that employees can view and complete their to-dos from either system.

</td><td>

Active

</td><td>

false

</td><td>

-   sn\_successfactors
-   sn\_hr\_integr\_fw
-   com.sn\_hr\_core

</td></tr><tr><td>

HRSD Process Optimization Content Pack\[com.sn\_hr\_process\_optimization\]

 \(Available in the ServiceNow Store\)

</td><td>

Provides pre-configured process optimization models and improvement initiatives for HRSD processes.

</td><td>

Inactive

</td><td>

false

</td><td>

-   com.sn\_process\_optimization
-   com.sn\_hr\_core

</td></tr><tr id="plugin_com.glide.htmlsanitizer" class="plugin_reference"><td class="name">

HTML Sanitizer\[com.glide.htmlsanitizer\]

</td><td class="description">

Automatically cleans up HTML markup in all HTML fields to remove unwanted code to protect against security concerns such as cross-site scripting attacks.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

 

</td></tr><tr><td class="name">

Human Resources Application: Core CMS\[com.snc.hr.core.cms\]

 \(Maintenance mode only\)

</td><td class="description">

Provides case and knowledge management for HR. Standardizes the documentation, interaction, and fulfillment of employee inquires and requests while having visibility into the quantity and type of cases coming in.**Warning:** Be sure that you do not have plugin Human Resources Application: Core activated. This plugin is a new HR application that duplicates some functionality in Human Resources Application: Core. If you have any questions about this plugin, contact your ServiceNow account manager.

Activation of this plugin on production instances may require a separate license. Contact ServiceNow for details.

</td><td>

Inactive

</td><td class="has_demo_data">

true

</td><td class="requires">

-   com.glide.country
-   com.glide.db\_images
-   com.snc.appview
-   com.snc.document\_management
-   com.snc.knowledge3
-   com.snc.pdf\_generator
-   com.snc.sc\_catalog\_manager
-   com.snc.signaturepad
-   com.snc.skills\_management
-   com.snc.task\_activity
-   com.snc.matching\_rule
-   com.snc.hr.scoped\_security

</td></tr><tr><td class="name">

Human Resources Scoped App: Integrations\[com.sn\_hr\_integrations\]

</td><td class="description">

HR Integration provides the ability to integrate with multiple third-party HR systems for the scoped version of HRSM. HR Integration pushes HR profile information from HRSM to a third-party HR application and pulls HR profile information from a third-party HR application to HRSM.

</td><td class="active">

Inactive

</td><td class="has_demo_data">

true

</td><td class="requires">

com.glide.scope.access.restricted\_caller

</td></tr><tr><td class="name">

Human Resources Scoped App: Lifecycle Events\[com.sn\_hr\_lifecycle\_events\]

</td><td class="description">

Activates the **Lifecycle Event** module for HR. .Combined with other licensed applications, provides a full-service, employee journey experience such as onboarding or parental leave of absence for employees and those managing the process

</td><td>

Inactive

</td><td class="has_demo_data">

true

</td><td class="requires">

-   com.sn.hr.core
-   com.sn\_hr\_service\_portal

</td></tr><tr><td>

Human Resources Scoped App: Lifecycle Events for Enterprise\[com.sn\_hr\_lifecycle\_enthelene\]

</td><td>

Human Resources Scoped App: Lifecycle Events for Enterprise enables you to automate onboarding and other employee lifecycle events that span across multiple departments such as IT, Facilities, Finance, and Legal.

</td><td>

Inactive

</td><td>

true

</td><td class="requires">

-   com.sn\_hr\_lifecycle\_events
-   com.sn\_hr\_core
-   com.sn\_hr\_service\_portal
-   com.sn\_hr\_onboarding
-   com.snc.businessroles

</td></tr><tr><td>

Human Resources Scoped App: Mobile\[com.sn\_hr\_mobile\]

</td><td>

Activates the Mobile module for HR. Combined with Mobile Employee Experience Native Application plugin, items related to HR will be shown in the native mobile application.

</td><td>

Active

</td><td>

true

</td><td class="requires">

-   com.glide.mobile-employee
-   com.sn\_hr\_core

</td></tr><tr><td>

Human Resources Scoped App: Mobile Employee Onboarding\[com.sn\_hr\_onboarding\]

</td><td>

Enable your new hires to complete onboarding to-dos, ask questions, and view relevant content using the new Mobile Onboarding application.

</td><td>

Inactive

</td><td>

true

</td><td>

 

</td></tr><tr><td class="name">

Human Resources Scoped App: Security\[com.sn.hr.scoped\_security\]

</td><td class="description">

Activation of this plugin on production instances requires a separate license. Contact ServiceNow for details.Human Resources Scoped App: Core plugin requires this plugin.

</td><td class="active">

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

com.glide.service-portal

</td></tr><tr><td class="name">

Human Resources Scoped App: Service Portal\[com.sn.hr.service\_portal\]

</td><td class="description">

Provides a single place for employees to quickly and easily get all the HR services they need.

</td><td class="active">

Inactive

</td><td class="has_demo_data">

true

</td><td class="requires">

-   com.sn\_hr\_core
-   com.glide.connect.support

</td></tr><tr><td>

Human Resources Scoped App: Virtual Agent Conversations\[com.sn\_hr\_virtual\_agent\]

</td><td>

Activates a conversational bot platform for providing user assistance through conversations within a messaging interface for HR.**Important:** To use Virtual Agent for HR, the Human Resources Scoped App: Core and the Glide Virtual Agent plugins must be licensed and activated.

</td><td>

Active

</td><td>

false

</td><td class="requires">

-   com.glide.cs
-   com.sn\_hr\_core
-   com.glide.cs.chatbot
-   com.glide.cs.sn-va-web-client-app
-   com.sn\_hr\_service\_portal
-   com.glide.va.sp\_widgets

</td></tr><tr><td>

Human Resources Scoped App: Workspace\[sn\_hr\_agent\_workspace\]

</td><td>

Activates a configurable service desk application that provides agents with an integrated and graphically intuitive user experience for HR.**Important:** To use Agent Workspace for HR, the Human Resources Scoped App: Core plugin must be licensed and activated.

</td><td>

 

</td><td>

false

</td><td class="requires">

-   com.agent\_workspace
-   com.snc.sn\_lookup\_and\_verify\_config
-   com.sn\_hr\_core

</td></tr><tr><td>

IBM License Compliance for Software Asset Management\[com.sn\_samp\_ibm\_lic\]

 \(Available in the ServiceNow Store\)

</td><td>

Enables integration between the Software Asset Management publisher pack for IBM and the Anglepoint Elevate platform. With this integration, you can track and manage IBM licensing directly without having to integrate with the IBM License Metric Tool \(ILMT\) or BigFix Inventory.

</td><td>

Inactive

</td><td>

false

</td><td>

com.sn\_samp\_master\_ws

</td></tr><tr><td>

Individual Life Servicing\[com.sn\_ins\_indiv\_life\]

 \(Available in the ServiceNow Store\)

</td><td>

Individual life insurance policy management.

</td><td>

Active

</td><td>

true

</td><td>

-   com.snc.csm\_contributor\_user
-   sn\_csm\_playbook \(2.0.2\)
-   sn\_bom \(1.8.0\)
-   sn\_ins\_indiv\_uw \(1.0.1\)

</td></tr><tr><td>

Indoor Mapping\[sn\_map\_core\]

 \(Available in the ServiceNow Store\)

</td><td>

Provides the capabilities to build, visualize, and integrate digital maps into various ServiceNow products and use cases.

</td><td>

Active

</td><td>

true

</td><td>

sn\_wsd\_indoor\_map

</td></tr><tr><td>

Industrial Process Manager\[com.sn\_otsm\]

\(Available in the ServiceNow Store\)

</td><td>

Enables teams to map and visualize the industrial equipment models and associated production process at individual facilities.

</td><td>

Active

</td><td>

False

</td><td>

-   com.sn\_mfg\_common
-   com.sn\_cmdb\_ci\_class
-   com.sn\_isa\_model

</td></tr><tr><td>

Industrial Workspace Common\[com.sn\_mfg\_common\]

\(Available in the ServiceNow Store\)

</td><td>

Provides common components used in Industrial Process and Operational Technology products.

</td><td>

Active

</td><td>

True

</td><td>

com.snc.cmdb.workspace

</td></tr><tr><td>

Interaction Controls Component \[sn\_int\_control\] \(Available in the ServiceNow Store\[var.store-name\]\)

</td><td>

This plugin enables a Contact Center Platform to integrate with the ServiceNow Configurable Workspace. This framework provides a set of native voice call controls.

</td><td>

Active

</td><td>

false

</td><td>

-   Application spoke selector \[sn\_appss\]
-   Contact Center Integration Core \[sn\_ct\_ctr\_it\_core\]
-   External Agent Management Util Pack \[sn\_external\_agent\]
-   OpenFrame \[sn\_openframe\]
-   OpenFrame UXB Component \[sn\_openframe\_uxb\]
-   sn-timer \[sn\_timer\]
-   com.glide.cs.custom.adapter
-   com.glide.hub
-   com.sn\_openframe

</td></tr><tr><td>

ISA Equipment Model\[com.sn\_isa\_model\]

\(Available in the ServiceNow Store\)

</td><td>

Creates the ISA-95 Equipment Model data foundation that is required for the ServiceNow Operational Technology solution.

</td><td>

Active

</td><td>

True

</td><td>

com.snc.cmdb.integration\_util

</td></tr><tr><td>

Issue Auto Resolution for HR\[com.snc.hr.issue\_auto\_resolution\]

 \(New in Tokyo\)

</td><td>

Enables organizations to provide near real-time responses to routine and non-critical employee inquiries using self-service content already defined by the organisation. Employees can ask for help in their own natural language through the channel that is convenient to them and in the time frame that feels effective for them.

</td><td>

Active

</td><td>

false

</td><td>

com.sn\_hr\_core

</td></tr><tr><td>

ITAM Health Check application\[com.sn\_itam\_health\_chk\]

 \(Available in the ServiceNow Store\)

</td><td>

Performs Software Asset Management configuration scans to determine issues with configuration, that could impact software License compliance results. Additionally, you can get recommendations to fix the issues and thereafter create tasks for successful resolution.

</td><td>

Active

</td><td>

false

</td><td>

com.snc.samp

</td></tr><tr><td>

IntegrationHub ETL\[com.sn\_int\_studio\]

 \(Available in the ServiceNow Store\)

</td><td>

User interface for configuring templates to ingest CMDB data from third party sources.

</td><td>

Active

</td><td>

true

</td><td>

-   com.glide.integration\_studio
-   com.snc.cmdb.integration\_util

</td></tr><tr><td>

ITSM Success Dashboard\[com.snc.success\_dashboard\_itsm\]

 \(Available in the ServiceNow Store\)

</td><td>

Provides insights to the IT leadership teams and process owners to measure the performance and improvement of their ITSM implementation using the KPIs defined by ServiceNow.

</td><td>

Active

</td><td>

false

</td><td>

-   com.snc.pa.premium.all\_content
-   com.snc.self\_service\_analytics\_core

</td></tr><tr><td>

Journey Designer\[com.sn\_jny\]

 \(New in Tokyo\)

</td><td>

Enables managers and employees to engage in rich, collaborative journeys from onboarding to offboarding and everything in between.

</td><td>

Inactive

</td><td>

true

</td><td>

-   com.sn\_hr\_core
-   com.sn\_hr\_lifecycle\_ent
-   sn\_ex\_sp\_pro
-   sn\_ect sn\_cd

</td></tr><tr id="plugin_com.snc.i18n.brazilian_portuguese" class="plugin_reference"><td class="name">

I18N: Brazilian Portuguese Translations\[com.snc.i18n.brazilian\_portuguese\]

</td><td class="description">

An Internationalization plugin for language internationalization. Provides Brazilian Portuguese.

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

com.glide.i18n

</td></tr><tr id="plugin_com.snc.i18n.czech" class="plugin_reference"><td class="name">

I18N: Czech Translations\[com.snc.i18n.czech\]

</td><td class="description">

An Internationalization plugin for language internationalization. Provides Czech.

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

com.glide.i18n

</td></tr><tr id="plugin_com.snc.i18n.dutch" class="plugin_reference"><td class="name">

I18N: Dutch Translations\[com.snc.i18n.dutch\]

</td><td class="description">

An Internationalization plugin for language internationalization. Provides Dutch.

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

com.glide.i18n

</td></tr><tr id="plugin_com.snc.i18n.finnish" class="plugin_reference"><td class="name">

I18N: Finnish Translations\[com.snc.i18n.finnish\]

</td><td class="description">

An Internationalization plugin for language internationalization. Provides Finnish.

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

com.glide.i18n

</td></tr><tr id="plugin_com.snc.i18n.french-canada" class="plugin_reference"><td class="name">

I18N: French - Canada Translations\[com.snc.i18n.french-canada\]

</td><td class="description">

An Internationalization plugin for language internationalization. Provides French - Canadian.

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

com.glide.i18n

</td></tr><tr id="plugin_com.snc.i18n.french" class="plugin_reference"><td class="name">

I18N: French Translations\[com.snc.i18n.french\]

</td><td class="description">

An Internationalization plugin for language internationalization. Provides French.

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

com.glide.i18n

</td></tr><tr id="plugin_com.snc.i18n.german" class="plugin_reference"><td class="name">

I18N: German Translations\[com.snc.i18n.german\]

</td><td class="description">

An Internationalization plugin for language internationalization. Provides German.

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

com.glide.i18n

</td></tr><tr id="plugin_com.snc.i18n.hebrew" class="plugin_reference"><td class="name">

I18N: Hebrew Translations\[com.snc.i18n.hebrew\]

</td><td class="description">

An Internationalization plugin for language internationalization. Provides Hebrew.

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

com.glide.i18n

</td></tr><tr id="plugin_com.snc.i18n.hungarian" class="plugin_reference"><td class="name">

I18N: Hungarian Translations\[com.snc.i18n.hungarian\]

</td><td class="description">

An Internationalization plugin for language internationalization. Provides Hungarian.

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

com.glide.i18n

</td></tr><tr id="plugin_com.glide.i18n" class="plugin_reference"><td class="name">

I18N: Internationalization\[com.glide.i18n\]

</td><td class="description">

An Internationalization plugin for language internationalization. Provides the elements necessary for translating an instance without any translation preloaded.

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

-   com.glide.system\_import\_set
-   com.glideapp.knowledge.i18n2

</td></tr><tr id="plugin_com.glide.i18n.translation_helper" class="plugin_reference"><td class="name">

I18N: Internationalization Translation helper\[com.glide.i18n.translation\_helper\]

</td><td class="description">

Modules and import set maps to merge all languages into one table for translation maintenance.

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

com.glide.i18n

</td></tr><tr id="plugin_com.snc.i18n.italian" class="plugin_reference"><td class="name">

I18N: Italian Translations\[com.snc.i18n.italian\]

</td><td class="description">

An Internationalization plugin for language internationalization. Provides Italian.

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

com.glide.i18n

</td></tr><tr id="plugin_com.snc.i18n.japanese" class="plugin_reference"><td class="name">

I18N: Japanese Translations\[com.snc.i18n.japanese\]

</td><td class="description">

An Internationalization plugin for language internationalization. Provides Japanese.

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

com.glide.i18n

</td></tr><tr id="plugin_com.glideapp.knowledge.i18n2" class="plugin_reference"><td class="name">

I18N: Knowledge Management Internationalization Plugin v2\[com.glideapp.knowledge.i18n2\]

</td><td class="description">

Activating internationalization plugins for any of the available languages automatically activates this plugin. This plugin helps create and maintain translations of an article in various languages in a way that is easy to manage translations while authoring as well as viewing articles.

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

-   com.glideapp.knowledge3
-   com.glide.i18n

</td></tr><tr><td class="name">

I18N: Korean Translations\[com.snc.i18n.korean\]

</td><td class="description">

Korean Translations

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

com.glide.i18n

</td></tr><tr id="plugin_com.snc.i18n.polish" class="plugin_reference"><td class="name">

I18N: Polish Translations\[com.snc.i18n.polish\]

</td><td class="description">

An Internationalization plugin for language internationalization. Provides Polish.

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

com.glide.i18n

</td></tr><tr id="plugin_com.snc.i18n.portuguese" class="plugin_reference"><td class="name">

I18N: Portuguese Translations\[com.snc.i18n.portuguese\]

</td><td class="description">

An Internationalization plugin for language internationalization. Provides Portuguese.

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

com.glide.i18n

</td></tr><tr id="plugin_com.snc.i18n.russian" class="plugin_reference"><td class="name">

I18N: Russian Translations\[com.snc.i18n.russian\]

</td><td class="description">

An Internationalization plugin for language internationalization. Provides Russian.

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

com.glide.i18n

</td></tr><tr id="plugin_com.snc.i18n.chinese" class="plugin_reference"><td class="name">

I18N: Simplified Chinese Translations\[com.snc.i18n.chinese\]

</td><td class="description">

An Internationalization plugin for language internationalization. Provides Simplified Chinese.

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

com.glide.i18n

</td></tr><tr id="plugin_com.snc.i18n.spanish" class="plugin_reference"><td class="name">

I18N: Spanish Translations\[com.snc.i18n.spanish\]

</td><td class="description">

An Internationalization plugin for language internationalization. Provides Spanish.

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

com.glide.i18n

</td></tr><tr id="plugin_com.snc.i18n.thai" class="plugin_reference"><td class="name">

I18N: Thai Translations\[com.snc.i18n.thai\]

</td><td class="description">

An Internationalization plugin for language internationalization. Provides Thai.

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

com.glide.i18n

</td></tr><tr id="plugin_com.snc.i18n.traditional_chinese" class="plugin_reference"><td class="name">

I18N: Traditional Chinese Translations\[com.snc.i18n.traditional\_chinese\]

</td><td class="description">

An Internationalization plugin for language internationalization. Provides Traditional Chinese.

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

com.glide.i18n

</td></tr><tr id="plugin_com.snc.i18n.turkish" class="plugin_reference"><td class="name">

I18N: Turkish Translations\[com.snc.i18n.turkish\]

</td><td class="description">

An Internationalization plugin for language internationalization. Provides Turkish.

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

com.glide.i18n

</td></tr><tr><td>

IBM License Compliance for Software Asset Management\[com.sn\_samp\_ibm\_lic\]

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

IBM Watson Assistant Integration\[com.glide.cs.ibm.watson.assistant.topic\]

</td><td>

Enables the IBM Watson Assistant topic to run an IBM skill \(conversation\) created in IBM Watson with the Assistant V1 API. The topic runs in the Virtual Agent web client.

</td><td>

Inactive

</td><td>

false

</td><td>

 

</td></tr><tr><td>

IBM Watson Assistant Integration V2\[com.glide.cs.ibm.watson.assistant.v2.topic\]

</td><td>

Enables the IBM Watson Assistant Chat Integration to run a dialog skill \(conversation\) created in IBM Watson with the Assistant V2 API. The topics runs in the Virtual Agent web client.

</td><td>

Inactive

</td><td>

false

</td><td>

 

</td></tr><tr><td>

IBM Watson Translator Service Spoke\[com.glide.ibm\_translation\_spoke\]

</td><td>

Using IBM translation services, it adds ability to translate text from one language to another and detect the language of text.

</td><td>

Inactive

</td><td>

false

</td><td>

com.glide.hub.integrations

</td></tr><tr><td>

Ideation with PPM\[com.snc.ppm\_innovation\_management\]

</td><td>

Enables you to manage your demands, resources, portfolios and projects, and gives full visibility from idea to execution. Agile management and test management help you to improve productivity and service delivery. Enables you to manage ideas with full visibility from idea submission to execution. Collaborate with the idea submitter and other stakeholders to Identify ideas with the greatest potential and convert them into different work entities for execution.

</td><td>

Inactive

</td><td>

true

</td><td class="requires">

-   com.snc.project\_portfolio\_suite
-   com.snc.financial\_planning
-   com.snc.rate\_model
-   com.snc.comments\_and\_feedback

</td></tr><tr><td class="name">

Incident\[com.snc.incident\]

</td><td class="description">

Provides base functionality for Incident Management.

</td><td>

Active

</td><td class="has_demo_data">

true

</td><td class="requires">

-   com.snc.service
-   com.snc.incident\_notification
-   com.glideapp.report.itsm.incident.overview

</td></tr><tr><td>

Incident Management - ATF Tests\[com.snc.incident.atf\]

</td><td>

Delivers ATF tests for Incident Management.

</td><td>

Active

</td><td>

true

</td><td>

 

</td></tr><tr><td>

Innovation Management Utility\[com.snc.innovation\_management\_util\]

</td><td>

Provides capability to create a work entity like demand/project from an idea.

</td><td>

Active

</td><td>

false

</td><td>

 

</td></tr><tr id="plugin_com.snc.iam" class="plugin_reference"><td class="name">

Incident Assignment Workbench Demo\[com.snc.incident\_assignment\_workbench\_demo\]

</td><td class="description">

Intelligent agent recommendation through dynamic matching rules/criteria.

</td><td>

Inactive

</td><td class="has_demo_data">

true

</td><td class="requires">

-   com.snc.contact\_management
-   com.glideapp.live\_feed\_document
-   com.glide.phone\_number

</td></tr><tr><td class="name">

Incident Communications Management\[com.snc.iam\]

</td><td class="description">

Allows crisis managers to manage communications for major issues, to bring together all involved users via SMS, conference calls, email subscriptions, and live feed.

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

com.snc.assignment\_workbench

</td></tr><tr><td>

Incident Management - ATF Tests\[com.snc.incident.atf\]

</td><td>

Provides Incident Management ATF Tests.

</td><td>

Active

</td><td>

true

</td><td>

 

</td></tr><tr><td>

Incident Management - Major Incident Management\[com.snc.incident.mim\]

</td><td>

Provides a recommended incident response process for managing incidents a business critical incident with pre-defined incident communication plans and a workbench to handle different aspects of the process including communication, collaboration, and postmortem.

</td><td>

Inactive

</td><td>

true

</td><td class="requires">

-   com.snc.iam
-   com.snc.incident.updates
-   com.snc.task\_outage

</td></tr><tr id="plugin_com.snc.incident_notification" class="plugin_reference"><td class="name">

Incident Management Notification\[com.snc.incident\_notification\]

</td><td class="description">

Provides Notification functionality to Incident Management.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

 

</td></tr><tr><td>

Incident Management Best Practice - San Diego\[com.snc.best\_practice.incident.sandiego\]

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr id="plugin_com.glideapp.report.itsm.incident.overview" class="plugin_reference"><td class="name">

Incident Overview Homepage\[com.glideapp.report.itsm.incident.overview\]

</td><td class="description">

Provides Incident Overview Homepage.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

com.glideapp.report

</td></tr><tr id="plugin_com.snc.incident_resolution_fields" class="plugin_reference"><td class="name">

Incident Resolution Fields\[com.snc.incident\_resolution\_fields\]

</td><td class="description">

Adds **Resolved** and **Resolved by** fields to the Incident table, similar to **Closed** and **Closed by**, populated with a business rule when an incident is resolved or closed.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

 

</td></tr><tr><td>

Incident Updates\[com.snc.incident.updates\]

</td><td>

Incident Updates Plugin - Includes any updates to the Incident Base Plugin.

</td><td>

Active

</td><td>

true

</td><td>

 

</td></tr><tr><td class="name">

Index Suggestion\[com.glide.index\_suggestion\]

</td><td class="description">

Suggest database indexes for slow queries.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

Stats Tools, Column Statistics

</td></tr><tr><td>

Innovation Management\[com.snc.innovation\_management\]

</td><td>

Idea Management application enables idea managers to manage ideas at organization level.

</td><td>

Inactive

</td><td>

false

</td><td>

com.snc.comments\_and\_feedback

</td></tr><tr><td>

Innovation Management - ATF Tests\[com.snc.innovation\_management.atf\]

</td><td>

Innovation Management - ATF Tests provides you test cases and test suits that can be run on the Innovation Management Application.

</td><td>

Inactive

</td><td>

false

</td><td>

 

</td></tr><tr id="plugin_com.glide.web_service_insert_multiple" class="plugin_reference"><td class="name">

Insert Multiple Web Service\[com.glide.web\_service\_insert\_multiple\]

</td><td class="description">

Enables multiple inserts for the Direct SOAP API.

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

 

</td></tr><tr><td>

Instance Security Center\[com.glide.instance\_sec\_center\]

</td><td>

This plugin activates the Instance Security Center Portal. Search for Instance Security Center in the left navigation menu.

</td><td>

Active

</td><td>

false

</td><td class="requires">

-   com.snc.pa.instance\_sec\_dash
-   com.snc.pa.sp.widget
-   com.glide.service-portal.esm

</td></tr><tr><td>

Instance Data Replication\[com.glide.idr\]

</td><td>

Replicates records from one instance to one or more other instances.

</td><td>

Inactive

</td><td>

false

</td><td>

 

</td></tr><tr><td>

Instance Sync Connector\[sn\_instance\_sync\_connector\]

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Instance Sync Connector - Core\[com.snc.instance\_sync\_connector\_core\]

</td><td>

ITSM Instance Sync Connector Core plugin that provides an ability to activate and leverage Integration Hub Process Sync Framework.

</td><td>

Active

</td><td>

false

</td><td>

com.glide.hub.process.sync

</td></tr><tr id="plugin_com.snc.integration.common" class="plugin_reference"><td class="name">

Integration - Common Components\[com.snc.integration.common\]

</td><td class="description">

Provides common scripts for integrations.

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

-   com.glide.system\_import\_set
-   com.glide.web\_service\_provider
-   com.glide.system\_property\_categories

</td></tr><tr id="plugin_com.snc.integration.jdbc" class="plugin_reference"><td class="name">

Integration - JDBC\[com.snc.integration.jdbc\]

</td><td class="description">

Provides integration through JDBC.

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

-   com.glide.web\_service\_application
-   com.glideapp.agent
-   com.snc.integration.common

</td></tr><tr id="plugin_com.snc.integration.multifactor.authentication" class="plugin_reference"><td class="name">

Integration - Multifactor Authentication\[com.snc.integration.multifactor.authentication\]

</td><td class="description">

This plugin to set up Multifactor authentication on the instance.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

 

</td></tr><tr><td class="name">

Integration - Multiple Provider Single Sign-On Enhanced UI\[com.snc.integration.sso.multi.ui\]

</td><td class="description">

 

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

-   com.glide.ui.ng.guided\_flow
-   com.snc.integration.sso.multi.installer

</td></tr><tr id="plugin_com.snc.integration.sso.multi.installer" class="plugin_reference"><td class="name">

Integration - Multiple Provider Single Sign-On Installer\[com.snc.integration.sso.multi.installer\]

</td><td class="description">

Use this plugin instead of the Integration - Multiple Provider Single Sign-On plugin to activate the Multiple Provider Single Sign-On feature. The multiple provider single sign-on plugin enables organizations to authenticate against multiple IDPs \(Identity providers\) using SAML. It also supports authentication using multiple digest configurations.

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

 

</td></tr><tr id="plugin_com.snc.integration.tivoli_tec" class="plugin_reference"><td class="name">

Integration - Tivoli Enterprise Console \(TEC\) 2.0\[com.snc.integration.tivoli\_tec\]

</td><td class="description">

Provides version 2.0 integration with Tivoli Enterprise Console \(TEC\).

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

-   com.snc.integration.common
-   com.glide.web\_service\_application
-   com.glideapp.agent

</td></tr><tr id="plugin_com.snc.integration.verizon_ebonding" class="plugin_reference"><td class="name">

Integration - Verizon eBonding\[com.snc.integration.verizon\_ebonding\]

</td><td class="description">

Provides integration with Verizon eBonding.

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

-   com.snc.integration.common
-   com.glide.custom\_web\_service
-   com.glide.static\_wsdl
-   com.glide.custom\_web\_service
-   com.glideapp.ecc\_retry\_policy

</td></tr><tr><td>

IntegrationHub Remote Process Sync\[com.glide.hub.process.sync\]

</td><td>

 

</td><td>

 

</td><td>

false

</td><td>

-   com.glide.hub.process.sync.model
-   com.glide.hub.process.sync.jobs
-   com.glide.hub.process.sync.actions
-   com.glide.hub.action\_step.rest
-   com.glide.hub.integration.runtime
-   com.glide.hub.flow\_designer\_introspection

</td></tr><tr><td>

IntegrationHub Remote Process Sync License\[com.glide.hub.remote.process.sync.license\]

</td><td>

A ServiceNow AI Platform Remote Process Sync subscription enables use of Remote Process Sync with custom and platform tables.**Note:** Use of Remote Process Sync on custom apps or tables that extend from a ServiceNow created application requires that users be subscribed to both the application extended as well as ServiceNow AI Platform Remote Process Sync.

</td><td>

 

</td><td>

false

</td><td>

 

</td></tr><tr><td>

Integrations - External Authentication Framework\[com.glide.external.app\]

</td><td>

 

</td><td>

Inactive

</td><td>

false

</td><td>

 

</td></tr><tr><td>

Intent Discovery\[sn\_nlu\_discovery\]

 \(Available in the ServiceNow Store\)

</td><td>

Discovers user intents from your incidents, cases, or requests.

</td><td>

Active

</td><td>

false

</td><td>

-   com.glide.nlu
-   com.glide.platform\_ml

</td></tr><tr><td>

Interaction Logging, Routing, and Queueing\[com.glide.interaction\]

</td><td>

Interaction Logging, Routing, and Queueing.

</td><td>

Inactive

</td><td>

false

</td><td>

 

</td></tr><tr><td>

Interactions Management\[com.glide.interaction\]

</td><td>

Activates the Interactions Management System

</td><td>

Active

</td><td>

false

</td><td>

 

</td></tr><tr><td>

Interactive Analysis\[com.glideapp.interactive\_analysis\]

</td><td>

Interactive Analysis

</td><td>

Active

</td><td>

false

</td><td class="requires">

-   com.glideapp.home.publishers
-   com.glide.ui.ng
-   com.glide.ui.ng.amb
-   com.glide.ui.ng.form\_elements

</td></tr><tr><td>

Interview Templates\[com.sn\_interview\_templates\]

</td><td>

Enables you to create reusable interview templates that are consistent and efficient for use in investigations.

</td><td>

Active

</td><td>

true

</td><td>

com.sn\_component\_interview\_templates

</td></tr><tr><td>

Investment Funding\[sn\_invst\_pln\]

 \(Available in the ServiceNow Store\)

</td><td>

Enables you to plan and manage investments by allocating funds to investment entities, such as Business Units, Products, Teams, and so on.

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Investment Funding - ATF Tests\[com.snc.investment\_planning.atf\]

</td><td>

Investment Funding - ATF Tests provides you test cases and test suits that can be run on the Investment Funding Application.

</td><td>

Active

</td><td>

false

</td><td>

com.snc.financial\_planning\_pmo.atf

</td></tr><tr><td>

Investment Planning\[com.snc.investment\_planning\]

</td><td>

Enables continuous and flexible investment planning for the funding entities based on their priorities and strategic objectives. It provides the options of top-down and bottom-up funding and defunding an entity.

</td><td>

Active

</td><td>

false

</td><td class="requires">

-   com.snc.app.grid
-   com.snc.app.widgets
-   com.snc.fiscal\_calendar
-   com.snc.planned\_task\_v2

</td></tr><tr><td>

Investment Planning for PPM\[com.snc.investment\_planning\_pmo\]

</td><td>

Enables continuous and flexible investment planning for PPM funding entities based on their priorities and strategic objectives. It provides the options of top-down and bottom-up funding and defunding an entity.

</td><td>

Inactive

</td><td>

false

</td><td class="requires">

-   com.snc.investment\_planning
-   com.snc.financial\_planning\_pmo

</td></tr><tr id="plugin_com.snc.ipauthenticator" class="plugin_reference"><td class="name">

IP Range Based Authentication\[com.snc.ipauthenticator\]

</td><td class="description">

Controls access to an instance based on IP address.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

 

</td></tr><tr><td>

ISC NLU Model for Virtual Agent Conversations\[com.glide.isc\_nlu\]

</td><td>

Activates the Natural Language Understanding \(NLU\) content pack for the Instance Security Center.

</td><td>

Inactive

</td><td>

false

</td><td>

com.glide.isc\_virtualagent

</td></tr><tr><td>

ISC Virtual Agent Conversations\[com.glide.isc\_virtualagent\]

</td><td>

Activates the Virtual Agent content pack for the Instance Security Center.

</td><td>

Inactive

</td><td>

false

</td><td>

-   com.glide.cs.chatbot
-   com.snc.nlu\_studio

</td></tr><tr><td>

Issue Auto-Resolution\[com.glide.cs.auto\_resolution\]

</td><td>

Intercepts incidents submitted through the Service Portal or email and gives your end users an option to have Virtual Agent help find a resolution. **Note:** Activate Glide Virtual Agent plugin to enable this feature.

</td><td>

Inactive

</td><td>

false

</td><td>

com.glide.cs.chatbot

</td></tr><tr><td>

IT Asset Management Mobile\[com.sn\_itam\_mobile\]

</td><td>

Inventory manager can receive and create assets at the dock.

</td><td>

Active

</td><td>

false

</td><td class="requires">

-   com.glide.sg
-   com.glide.sg.offline

</td></tr><tr><td>

ITBM Security\[com.snc.itbm\_security\]

</td><td>

Common plugin to manage security within IT Business Management plugins.

</td><td>

Active

</td><td>

false

</td><td>

 

</td></tr><tr id="plugin_com.snc.it_data_mart" class="plugin_reference"><td class="name">

IT Data Mart\[com.snc.it\_data\_mart\]

</td><td class="description">

Stores the information that the IT Finance application uses to allocate expenses to specific accounts and segments in the general ledger.

</td><td>

Inactive

</td><td class="has_demo_data">

true

</td><td class="requires">

 

</td></tr><tr><td>

IT Service Management integration with Microsoft Teams\[sn\_now\_teams\_it\]

 \(Available in the ServiceNow Store\)

</td><td>

The integration enables employees to interact with the IT service desk, directly in Microsoft Teams. Employees can ask questions, report on issues, request services and chat with a virtual or live IT service desk agent to resolve issues.

</td><td>

Inactive

</td><td>

false

</td><td>

-   sn\_now\_teams
-   com.glide.cs.chatbot.lite

</td></tr><tr id="plugin_com.glideapp.servicecatalog.item_designer" class="plugin_reference"><td class="name">

Item Designer support for the service catalog\[com.glideapp.servicecatalog.item\_designer\]

</td><td class="description">

Service Catalog item designer.

</td><td>

Active

</td><td class="has_demo_data">

true

</td><td class="requires">

com.glideapp.servicecatalog

</td></tr><tr><td class="name">

ITOM Guided Setup\[com.snc.guided\_setup\_metadata.itom\]

</td><td class="description">

ITOM Guided Setup Metadata.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

com.snc.guided\_setup

</td></tr><tr id="plugin_com.snc.itsm_pa.demo" class="plugin_reference"><td class="name">

ITSM and PA Demo Data\[com.snc.itsm\_pa.demo\]

</td><td class="description">

Demo data for Incident, Problem, Change, Task SLAs, Business Services, Service Offering, Service Commitments, and Performance Analytics.

</td><td>

Inactive

</td><td class="has_demo_data">

true

</td><td class="requires">

-   com.snc.incident
-   com.snc.problem
-   com.snc.change\_request
-   com.snc.sla
-   com.snc.cmdb
-   com.snc.service\_portfolio
-   com.snc.service\_portfolio.sla

</td></tr><tr><td>

ITSM CSDM Best Practice - Quebec\[com.snc.best\_practice.itsm\_csdm.quebec\]

</td><td>

ITSM CSDM Best Practices for Quebec release includes best practice configurations to support Common Service Data Model \(CSDM\). This plugin includes a business rule that populates the assignment group on the incident, problem, and change request based on the support group field on the CI or Service Offering.

</td><td>

Inactive

</td><td>

false

</td><td>

 

</td></tr><tr><td class="name">

ITSM Guided Setup\[com.snc.guided\_setup\_metadata.itsm\]

</td><td class="description">

Contains metadata for ITSM Guided Setup. This plugin is for ServiceNow internal usage only.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

com.snc.guided\_setup

</td></tr><tr><td>

ITSM Mobile Agent\[com.sn\_itsm\_mobile\_agent\]

</td><td>

New redesigned ITSM Mobile experience for Incident Management and On-Call.

</td><td>

Active

</td><td>

false

</td><td>

 

</td></tr><tr><td>

ITSM NLU Model for Virtual Agent Conversations\[com.snc.itsm.nlu\]

</td><td>

This plugin contains NLU models used in the Virtual Agent topics for ITSM-related use cases.

</td><td>

Active

</td><td>

false

</td><td>

com.glide.platform\_ml com.glide.dev-studio, com.snc.nlu\_studio

</td></tr><tr><td>

ITSM Process Optimization Content Pack \(Maintenance mode only\)\[com.sn\_itsm\_process\_opt\_cp\]

</td><td>

Provides pre-configured process optimization models and improvement initiatives for the ITSM Processes.

</td><td>

Active

</td><td>

false

</td><td>

 

</td></tr><tr><td>

ITSM Roles - Change Management\[com.snc.itsm.roles.change\_management\]

</td><td>

This plugin is included with the ITSM Roles plugin. This plugin adds the sn\_change\_read and sn\_change\_write roles. It also updates the existing security model for Change Management to factor these new roles.

</td><td>

Inactive

</td><td>

false

</td><td>

 

</td></tr><tr><td>

ITSM Roles - Incident Management\[com.snc.itsm.roles.incident\_management\]

</td><td>

This plugin is included with the ITSM Roles plugin.This plugin adds the sn\_incident\_read and sn\_incident\_write roles. It also updates the existing security model for Incident Management to factor these new roles.

</td><td>

Inactive

</td><td>

false

</td><td>

 

</td></tr><tr><td>

ITSM Roles - Problem Management\[com.snc.itsm.roles.problem\_management\]

</td><td>

This plugin is loaded with the ITSM Roles plugin.

</td><td>

Inactive

</td><td>

false

</td><td>

 

</td></tr><tr><td>

ITSM Roles - Request Management\[com.snc.itsm.roles.request\_management\]

</td><td>

This plugin adds sn\_request\_read and sn\_request\_wirte. It also updates the existing security model for Request Management to factor these new roles.

</td><td>

Inactive

</td><td>

false

</td><td>

 

</td></tr><tr><td>

ITSM Shared VA Topic Blocks\[com.glideapp.cs.itsm\_topic\_blocks\]

</td><td>

Contains prebuilt reusable conversation topic blocks for common actions like ordering from the catalog and searching the knowledge base.

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

ITSM Spoke\[com.snc.itsm.spoke\]

</td><td>

This Spoke enables Flow Designers to automate and create flows and actions associated with ITSM

</td><td>

Active

</td><td>

false

</td><td>

com.glide.hub

</td></tr><tr><td>

ITSM Virtual Agent Conversations\[com.snc.itsm.virtualagent\]

</td><td>

Contains prebuilt conversation topics for ITSM related use cases.

</td><td>

Active

</td><td>

true

</td><td class="requires">

-   com.glide.cs.chatbot
-   com.glide.service-portal

</td></tr><tr><td>

ITSM Virtual Agent Conversation Topics Lite \(Maintenance mode\)\[com.snc.itsm.virtualagent.lite\]

</td><td>

Read only conversations for basic ITSM self service use cases, including opening incidents, checking status,searching the knowledge base, submitting requests, and checking for outages.

</td><td>

Active

</td><td>

false

</td><td class="requires">

-   com.glide.cs.chatbot.lite
-   com.glideapp.cs.sm\_topic\_blocks

</td></tr><tr><td>

ITSM Workspace\[com.snc.agent\_workspace.itsm\]

</td><td>

Provides you the functionality of ITSM Agent Workspace. The plugin is available by default for new and existing users. The ITSM Workspace plugin also activates the ITSM Workspace Landing Pages \(com.snc.agent\_workspace.itsm.landing\_page\) plugin.

</td><td>

Active

</td><td>

false

</td><td class="requires">

-   com.agent\_workspace
-   com.glideapp.servicecatalog.workspace
-   com.snc.agent\_recommend
-   com.snc.agent\_workspace.itsm.landing\_page

</td></tr><tr><td>

ITSM Workspace Landing Pages\[com.snc.agent\_workspace.itsm.landing\_page\]

</td><td>

Delivers ITSM Agent Workspace Landing Pages - basic version.

</td><td>

Inactive

</td><td>

true

</td><td>

 

</td></tr><tr><td>

ITSM Workspace Landing Pages - Premium\[com.snc.agent\_workspace.itsm.landing\_page\_premium\]

</td><td>

Delivers ITSM Agent Workspace Landing Pages - premium version.

</td><td>

Inactive

</td><td>

true

</td><td>

Agent Workspace, Performance Analytics - Content Pack - ITSM Dashboards

</td></tr><tr><td>

JDBC Step for\[com.glide.hub.action\_step.jdbc\]

 ServiceNow IntegrationHub

</td><td>

Activates the JDBC step in Flow Designer, enabling you to create a reusable action to send SQL commands to a relational database.

</td><td>

Inactive

</td><td>

false

</td><td>

com.glide.hub.action\_step.template

</td></tr><tr><td>

JS Code Coverage Debug\[com.glide.js.coverage\]

</td><td>

Debug utility that collects coverage data for server-side Javascript.

</td><td>

Inactive

</td><td>

false

</td><td class="requires">

-   com.glide.sessiondebug
-   com.glide.snc\_code\_editor

</td></tr><tr><td>

JSDebugger\[com.glide.glide-js-debugger\]

</td><td>

ServiceNow server-side scripts debugger.

</td><td>

Active

</td><td>

false

</td><td>

com.glide.glide-js-debugger-api

</td></tr><tr id="plugin_com.snc.application.json_service" class="plugin_reference"><td class="name">

JSON Service request/response model\[com.snc.application.json\_service\]

</td><td class="description">

Core components and helpers for a JSON request/response model. Includes JSON and XML transports for NG and GlideAjax support. An extension of the processor framework.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

 

</td></tr><tr><td>

KCS Integration for Incident Management\[com.snc.incident.knowledge\]

</td><td>

Provides integration of Incident Management with the Advanced Knowledge Management features.

</td><td>

Inactive

</td><td>

true

</td><td>

com.snc.knowledge\_advanced.installer

</td></tr><tr><td>

Keylines Business Service Maps\[com.snc.keylines\_bsm\_map\]

</td><td>

An interactive and graphical interface to visualize Configuration Items \(CIs\) and their relationships. Provides filtering capabilities to manage data being displayed, allowing for configuration by the user to view in context to their role. Additional capabilities provide for the displaying of related tasks such as Incidents, Problems, Changes and Certification Tasks.

</td><td>

Active

</td><td>

false

</td><td class="requires">

-   com.glide.diagrammer
-   com.glideapp.bsm\_map2

</td></tr><tr><td>

Knowledge API\[sn\_km\_api\]

</td><td>

Provides the ability to search, view, and fetch most-viewed and featured knowledge articles.

</td><td>

Inactive

</td><td>

false

</td><td>

 

</td></tr><tr><td>

Knowledge Blocks\[com.snc.knowledge\_blocks\]

</td><td>

This plugin adds an advanced editing feature to Knowledge Management which allows user to create re-usable content blocks that can be included in existing knowledge articles. This feature will give the ability to have one large article and be able to just display pieces of that article to specific users.

</td><td>

Active

</td><td>

true

</td><td>

com.snc.knowledge\_advanced.installer

</td></tr><tr><td>

Knowledge Capabilities in UI Builder\[com.snc.uib.knowledge\]

</td><td>

Enables configurable Knowledge Management artifacts \(Pages, Data transforms, and GraphQL queries\) in UI Builder.

</td><td>

Active

</td><td>

false

</td><td>

 

</td></tr><tr><td>

Knowledge Management Core\[com.glideapp.knowledge\]

</td><td>

Installs the core Knowledge Management items used to allow other Knowledge related plugins to work, such as Knowledge V3, Knowledge Advanced, Knowledge Service Portal. This plugin is activated by default.

</td><td>

Active

</td><td>

true

</td><td class="requires">

-   com.glide.ui.angular
-   com.glide.ui.ng
-   com.glideapp.user\_criteria
-   com.snc.db.rotation
-   com.glideapp.live\_feed\_v2
-   com.glideapp.report.knowledge.overview

</td></tr><tr id="plugin_com.snc.knowledge_document" class="plugin_reference"><td class="name">

Knowledge Document\[com.snc.knowledge\_document\]

</td><td class="description">

Adds knowledge-based functionalities to the Managed Documents plugin. You can create a knowledge article from a document, or update a knowledge document to a newer revision.

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

com.snc.document\_management

</td></tr><tr><td class="name">

Knowledge Management - External Content Integration\[com.snc.knowledge.external\_integration\]

</td><td>

Adds external content search capabilities to the knowledge management application. Once configured, this feature creates a copy of the external content on ServiceNow as knowledge articles, and then indexes the articles through Zing Search. You must have appropriate reuse and copy privileges before you configure an external source to be searchable using this feature.

</td><td>

Inactive

</td><td>

true

</td><td class="requires">

-   com.snc.core.automation.connection\_credential
-   com.snc.knowledge3
-   com.snc.knowledge\_advanced.installer

</td></tr><tr><td>

Knowledge Management - Mobile Requestor\[com.glideapp.knowledge.mobile\_requestor\]

</td><td>

This is a maintenance plugin used to activate Knowledge Management Mobile Requestor features.

</td><td>

Inactive

</td><td>

false

</td><td class="requires">

-   com.glideapp.knowledge
-   com.glide.script.vtable
-   com.glide.mobile-employee.webview
-   com.glide.mobile-employee.search

</td></tr><tr><td class="name">

Knowledge Management - Service portal\[com.snc.knowledge\_serviceportal\]

</td><td class="description">

Provides knowledge management features on the service portal.

</td><td>

Active

</td><td>

false

</td><td class="requires">

-   com.glide.service-portal.esm
-   com.snc.knowledge3

</td></tr><tr><td class="name">

Knowledge Management Advanced\[com.snc.knowledge\_advanced\]

</td><td class="description">

This plugin adds advanced features to Knowledge Management such as version control and subscriptions. It requires that all Knowledge bases are Knowledge v3. Please use Knowledge Management Advanced Installer plugin to activate.

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

com.snc.knowledge3

</td></tr><tr><td class="name">

Knowledge Management Advanced Installer\[com.snc.knowledge\_advanced.installer\]

</td><td class="description">

Use this plugin to install the Knowledge Advanced plugin. When you activate/upgrade this plugin, it will do validations on knowledge articles and knowledge bases to make sure that the Knowledge Advanced plugin can be successfully installed. If validation fails, look at the errors in the Plugin Activation Logs and follow instructions given to fix them. Once all the issues are fixed, please re-run this plugin to install Knowledge Advanced.

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

 

</td></tr><tr id="plugin_com.snc.knowledge3" class="plugin_reference"><td class="name">

Knowledge Management V3\[com.snc.knowledge3\]

</td><td class="description">

Activate this plugin when you upgrade from Eureka or earlier.

</td><td>

Active

</td><td class="has_demo_data">

true

</td><td class="requires">

-   com.glide.ui.angular
-   com.glide.ui.ng
-   com.glideapp.knowledge2
-   com.glideapp.user\_criteria
-   com.snc.contextual\_search
-   com.snc.db.rotation
-   com.glideapp.live\_feed\_v2
-   com.glideapp.report.knowledge.overview

</td></tr><tr id="plugin_com.glideapp.knowledge2.wiki" class="plugin_reference"><td class="name">

Knowledge Management Wiki Support\[com.glideapp.knowledge2.wiki\]

</td><td class="description">

Activate this plugin to enable support for Wiki type Knowledge articles.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

-   com.glide.wiki
-   com.glideapp.knowledge2

</td></tr><tr><td class="name">

Knowledge Management KCS Capabilities plugin \(com.snc.knowledge\_kcs\_capabilities\)\[com.snc.knowledge\_kcs\_capabilities\]

</td><td>

Activate this plugin to enable the use of KCS roles \(kcs\_contributor, kcs\_publisher, and kcs\_candidate\) and use the metadata fields for the KCS article state \(governance and confidence\).

</td><td>

Inactive

</td><td>

false

</td><td>

 

</td></tr><tr><td>

Knowledge Overview\[com.sn\_knowledge\_overview\]

 \(New in Tokyo\)

</td><td>

A dashboard to track knowledge anaytics in real time.

</td><td>

Active

</td><td>

false

</td><td>

-   com.glideapp.report.knowledge.overview
-   com.glideapp.knowledge
-   com.glideapp.dashboards

</td></tr><tr id="plugin_com.snc.kb_product_entitlements" class="plugin_reference"><td class="name" id="entry_wqr_smd_d1b">

Knowledge Product Entitlements\[com.snc.kb\_product\_entitlements\]

</td><td class="description">

Knowledge Product entitlements, enables Customer Service admins to restrict access to customers based on products they are entitled to.

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

com.sn\_customerservice

</td></tr><tr><td class="name">

Knowledge Management - Add-in for Microsoft Word\[com.snc.knowledge.ms\_word\]

</td><td class="description">

Enables authoring content in Microsoft Word and publishing it as a knowledge article using a Word add-in.

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

-   com.servicenow\_now\_kb\_office\_addin
-   com.glideapp.knowledge
-   com.sn\_outlook\_addin

</td></tr><tr><td>

KPI Composer\[sn\_kpi\_composer\]

</td><td>

KPI Composer is an application for designing KPIs and Dashboards by using performance measurement methodologies.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td>

 

</td></tr><tr><td>

KPI Details Workspace Integration\[com.snc.pa.kpi\_details\_ws\_intgn\]

</td><td>

Performance Analytics - KPI Details allows user to explore more for a certain KPI,this plugin used to integrate sn-kpi-details component to workspace.

</td><td>

Active

</td><td>

false

</td><td class="requires">

-   com.agent\_workspace
-   com.workspace\_core

</td></tr><tr id="plugin_com.glide.ldap.ui" class="plugin_reference"><td class="name">

LDAP Support Enhanced UI\[com.glide.ldap.ui\]

</td><td class="description">

 

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

-   com.glide.ui.ng.guided\_flow
-   com.glide.ldap

</td></tr><tr><td>

Legal Request Management \[sn\_lg\_ops\]

 \(Available in the ServiceNow Store\)

</td><td>

Enables employees in the organization to submit legal requests and to track their progress while users in the legal department with appropriate roles can work to resolve these requests.

</td><td>

Inactive

</td><td>

false

</td><td>

-   com.glide.ui.checklist
-   com.snc.planned\_task\_v2
-   com.workspace\_core
-   sn\_ex\_emp\_fd

</td></tr><tr><td>

Legal Matter Management \[sn\_lg\_matter\]

 \(Available in the ServiceNow Store\)

</td><td>

Enables you to complete legal requests that need cross-departmental tasking and a workflow with a mechanism to store supporting documents and track important milestones.

</td><td>

Inactive

</td><td>

false

</td><td>

sn\_lg\_ops

</td></tr><tr><td>

Legal Conflict of Interest \[sn\_lg\_coi\]

 \(Available in the ServiceNow Store\)

</td><td>

Enables you to manage the disclosure, approval, and registry of conflict of interest that might arise from employees having competing interests or loyalties.

</td><td>

Inactive

</td><td>

false

</td><td>

sn\_lg\_ops

</td></tr><tr><td>

Legal Investigations\[sn\_lg\_investigate\]

 \(Available in the ServiceNow Store\)

</td><td>

Enables you to streamline the process for investigating internal complaints.

</td><td>

Inactive

</td><td>

false

</td><td>

-   sn\_lg\_ops
-   sn\_lg\_matter

</td></tr><tr><td>

Legal Digital Forensics \[sn\_lg\_forensics\]

 \(Available in the ServiceNow Store\)

</td><td>

Enables you to handle digital forensics requests for data discovery related to custodial and non-custodial data sources that are subject to investigations or litigation.

</td><td>

Inactive

</td><td>

false

</td><td>

-   sn\_lg\_ops
-   sn\_lg\_matter

</td></tr><tr><td>

Legal Simple Contracts \[sn\_lg\_contracts\]

 \(Available in the ServiceNow Store\)

</td><td>

Enables employees to submit legal requests for getting legal support and guidance for contracts.

</td><td>

Inactive

</td><td>

false

</td><td>

-   sn\_lg\_ops
-   sn\_doc

</td></tr><tr><td>

Legal Stock Preclearance \[sn\_lg\_stock\_cp\]

 \(Available in the ServiceNow Store\)

</td><td>

Enables you to manage stock preclearance requests complying with the company’s stock preclearance policy.

</td><td>

Inactive

</td><td>

false

</td><td>

-   sn\_lg\_ops
-   com.snc.fiscal\_calendar

</td></tr><tr><td>

Legal Virtual Agent Conversations \[sn\_lg\_va\]

 \(Available in the ServiceNow Store\)

</td><td>

Provides predefined conversation topics to enable automated chats with employees seeking legal services.

</td><td>

Inactive

</td><td>

false

</td><td>

-   sn\_lg\_ops
-   com.glide.cs.chatbot

</td></tr><tr><td>

Legal Mobile \[sn\_lg\_mobile\]

 \(Available in the ServiceNow Store\)

</td><td>

Enables your employees to submit and track legal requests and lawyers to work on these requests on their mobile devices.

</td><td>

Inactive

</td><td>

false

</td><td>

-   sn\_lg\_ops
-   com.glide.sg.agent\_native\_client
-   com.glide.sg

</td></tr><tr><td>

Legal Counsel Center \[sn\_lg\_workspace\]

 \(Available in the ServiceNow Store\)

</td><td>

Enables legal department members to categorize, prioritize, and efficiently address legal issues.

</td><td>

Inactive

</td><td>

false

</td><td>

-   sn\_lg\_ops
-   sn\_lg\_ws\_comps

</td></tr><tr><td>

Legal Counsel Center Components\[sn\_lg\_ws\_comps\]

 \(Available in the ServiceNow Store\)

</td><td>

Seismic Components for Legal Counsel Center.

</td><td>

Inactive

</td><td>

false

</td><td>

-   com.servicenow\_now\_button
-   com.servicenow\_now\_chart\_bar

</td></tr><tr><td>

Performance Analytics Content Pack for Legal Service Delivery \[sn\_lg\_pa\]

 \(Available in the ServiceNow Store\)

</td><td>

Provides insights into legal operations to make data-driven decisions for your Legal department.

</td><td>

Inactive

</td><td>

false

</td><td>

-   sn\_lg\_ops
-   com.snc.pa
-   com.snc.pa.premium

</td></tr><tr><td>

Legal Practice Applications core\[com.sn\_lg\_lpa\_core\]

 \(Available in the ServiceNow Store\)

</td><td>

Provides pre-built legal workflows with configurable intake forms, process flows, disposition repository, analytics, and integrations with third-party tools.

</td><td>

Inactive

</td><td>

false

</td><td>

Legal Request Management \(sn\_lg\_ops\)

</td></tr><tr id="plugin_com.snc.legal_service_automation" class="plugin_reference"><td class="name">

Legal Service Management \(Maintenance mode only\) Planned for deprecation after Feb 1, 2023\[com.snc.legal\_service\_automation\]

</td><td class="description">

Manages legal matters and enables users to report and track matters. Activation of this plugin on production instances may require a separate license. Contact ServiceNow for details.

</td><td>

Inactive

</td><td class="has_demo_data">

true

</td><td class="requires">

com.snc.service\_management.core

</td></tr><tr id="plugin_com.snc.legal_service_automation_m" class="plugin_reference"><td class="name">

Legal Service Management Mobile\[com.snc.legal\_service\_automation\_m\]

</td><td class="description">

Manages Legal Service Management mobile components.

</td><td>

Inactive

</td><td class="has_demo_data">

true

</td><td class="requires">

-   com.snc.legal\_service\_automation
-   com.snc.service\_management\_m

</td></tr><tr><td>

Limit Concurrent Sessions\[com.glide.limit.concurrent.sessions\]

</td><td>

Activate this plugin to limit concurrent interactive sessions on the instance.

</td><td>

Inactive

</td><td>

false

</td><td>

 

</td></tr><tr><td>

Link Generator\[com.snc.linkgenerator\]

</td><td>

Activates the Link Generator that allows you to create deep links on an HR form to access information outside the application. You can generate URLs to manage content, knowledge articles, and catalogs or access social media or fulfillment requests

</td><td>

Inactive

</td><td>

true

</td><td>

 

</td></tr><tr id="plugin_com.glide.list_v2" class="plugin_reference"><td class="name">

List v2\[com.glide.list\_v2\]

</td><td class="description">

Updates to the display of lists that include a cleanup UI, hierarchical lists, and related lists embedded in forms.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

-   com.glide.tiny\_url
-   com.glide.ui\_list\_edit\_with\_form
-   com.glide.db\_context\_menu

</td></tr><tr id="plugin_com.glide.ui.list_v3_components" class="plugin_reference"><td class="name">

List v3 Components\[com.glide.ui.list\_v3\_components\]

</td><td class="description">

Provides components required for List v3, including REST endpoints and Angular components.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

-   com.glide.ui.list\_api
-   com.glide.ui.ng
-   com.glide.ui.ng.amb
-   com.glide.ui.ng.form\_elements
-   com.glide.ui.ng.filter
-   com.glideapp.report.charting\_v2

</td></tr><tr><td>

Live Agent Conversation Settings\[com.glide.cs.live\_agent\_settings\]

</td><td>

Live Agent Conversation Settings

</td><td>

Active

</td><td>

false

</td><td>

com.glide.interaction

</td></tr><tr id="plugin_com.glideapp.live_feed_v2" class="plugin_reference"><td class="name">

Live Feed\[com.glideapp.live\_feed\_v2\]

</td><td class="description">

Provides an updated application to post and share content in a ServiceNow instance.

</td><td>

Active

</td><td class="has_demo_data">

true

</td><td class="requires">

-   com.glideapp.live\_feed
-   com.glideapp.ui\_components

</td></tr><tr id="plugin_com.glideapp.live_feed" class="plugin_reference"><td class="name">

Live Feed\[com.glideapp.live\_feed\]

</td><td class="description">

Provides a place to post and share content in a ServiceNow instance.

</td><td>

Active

</td><td class="has_demo_data">

true

</td><td class="requires">

-   com.glide.custom\_web\_service
-   com.glideapp.live\_common
-   com.glide.notification

</td></tr><tr id="plugin_com.glideapp.live_feed_document" class="plugin_reference"><td class="name">

Live Feed Document - follow tasks \(Incident, Change, etc.\)\[com.glideapp.live\_feed\_document\]

</td><td class="description">

Enables you to manage your task conversations and comments from **My Feed** or a document group.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

com.glideapp.live\_feed

</td></tr><tr><td>

Localization Framework\[com.glide.localization\_framework\]

</td><td>

A framework to manage localization workflows across the platform and products. To activate this plugin, install the Localization Framework Installer plugin.

</td><td>

Active

</td><td>

false

</td><td>

-   com.glide.localization\_framework.sdl\_spoke
-   com.glide.localization\_framework.xtm\_spoke
-   com.glide.localization\_framework.va
-   com.glide.localization\_framework.service\_catalog
-   com.glide.i18n

</td></tr><tr><td>

Localization Framework for Service Catalog\[com.glide.localization\_framework.service\_catalog\]

</td><td>

Enables translation of catalog items using Localization Framework. To activate this plugin, install the Localization Framework Installer plugin.

</td><td>

Active

</td><td>

false

</td><td>

com.glide.localization\_framework

</td></tr><tr><td>

Localization Framework for Virtual Agent Topic\[com.glide.localization\_framework.va\]

</td><td>

Enables translation of Virtual Agent Topic using Localization Framework. To activate this plugin, install the Localization Framework Installer plugin.

</td><td>

Active

</td><td>

false

</td><td>

com.glide.localization\_framework

</td></tr><tr><td>

Localization Framework Installer\[com.glide.localization\_framework.installer\]

</td><td>

Enhances the existing experience of translating the artifacts in an instance by automating most of the manual tasks in the localization process.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td>

-   com.glide.hub.integrations
-   com.glide.localization\_framework
-   com.glide.localization\_framework.sdl\_spoke
-   com.glide.localization\_framework.xtm\_spoke
-   com.glide.localization\_framework.va
-   com.glide.localization\_framework.service\_catalog

</td></tr><tr><td>

Macroponent Catalog Item for UIB\[com.glideapp.servicecatalog.macroponent\]

</td><td>

Component for UI Builder for Catalog Item and Record Producer.

</td><td>

 

</td><td>

false

</td><td>

-   com.devsnc\_sn\_catalog\_form
-   com.devsnc\_sn\_catalog\_action
-   com.devsnc\_sn\_catalog\_description
-   com.devsnc\_sn\_catalog\_form\_connected
-   com.devsnc\_sn\_catalog\_price
-   com.devsnc\_sn\_catalog\_quantity
-   com.devsnc\_sn\_catalog\_additional\_details
-   com.devsnc\_sn\_catalog\_request\_for

</td></tr><tr id="plugin_com.glide.ui.magellan_navigator" class="plugin_reference"><td class="name">

Magellan Navigator\[com.glide.ui.magellan\_navigator\]

</td><td class="description">

Provides a redesigned application navigator for Core UI. Combines standard navigation capabilities, customizable favorites, and recently accessed items in a single responsive control.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

-   com.glide.ui.magellan\_navigator\_api
-   com.glide.ui.doctype
-   com.glide.ui.ng

</td></tr><tr id="plugin_com.snc.maintenance_schedules" class="plugin_reference"><td class="name">

Maintenance Schedules\[com.snc.maintenance\_schedules\]

</td><td class="description">

Links configuration items to maintenance schedules. The maintenance schedules are checked against the planned dates for changes, and those that appear outside the maintenance schedule are so marked.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

-   com.glide.schedules
-   com.snc.cmdb

</td></tr><tr><td>

Major Issue Management\[com.sn\_majorissue\_mgtdyn\]

</td><td>

A set of capabilities used to manage customer-facing communications and resolution processes for common issues.

</td><td>

Inactive

</td><td>

true

</td><td class="requires">

-   com.sn\_customerservice
-   com.sn\_publications
-   com.snc.task\_communication\_management

</td></tr><tr id="plugin_com.snc.document_management" class="plugin_reference"><td class="name">

Managed documents\[com.snc.document\_management\]

</td><td class="description">

-   Lightweight
-   ITIL-based solution for managing electronic documents within your ServiceNow instance. To enable the ability to publish to the knowledge base, activate the Knowledge Document plugin.

</td><td>

Inactive

</td><td class="has_demo_data">

true

</td><td class="requires">

 

</td></tr><tr><td>

Manager Hub\[sn\_mh\]

 \(Available in the ServiceNow Store\)

</td><td>

Increases managers self-service and proactive engagement with their team by providing insights and recommended actions for what's most urgent and important to drive team success. It enables managers to grow as leaders through curated and personalised resources.

</td><td>

Active

</td><td>

true

</td><td>

com.snc.employee\_center\_pro

</td></tr><tr><td>

Manager Workspace \[com.snc.manager\_workspace\]

 \(Maintenance mode only\)

</td><td>

Manager Workspace App core shell.Install ITSM Manager workspace or CSM Manager workspace to get the modules

</td><td>

Active

</td><td>

true

</td><td>

com.snc.wfo

</td></tr><tr id="plugin_com.snc.marketing_service_automation" class="plugin_reference"><td class="name">

Marketing Service Management\[com.snc.marketing\_service\_automation\]

 \(Maintenance mode only\) Planned for deprecation after Feb 1, 2023

</td><td class="description">

Manages marketing requests and enables users to report and track those requests. Activation of this plugin on production instances may require a separate license. Contact ServiceNow for details.

</td><td>

Inactive

</td><td class="has_demo_data">

true

</td><td class="requires">

com.snc.service\_management.core

</td></tr><tr id="plugin_com.snc.marketing_service_automation_m" class="plugin_reference"><td class="name">

Marketing Service Management Mobile\[com.snc.marketing\_service\_automation\_m\]

</td><td class="description">

Manages Marketing Service Management mobile components.

</td><td>

Inactive

</td><td class="has_demo_data">

true

</td><td class="requires">

-   com.snc.marketing\_service\_automation
-   com.snc.service\_management\_m

</td></tr><tr><td>

Meeting Extensions for Microsoft Teams\[sn\_now\_teams\_ext\]

 \(Available in the ServiceNow Store\)

</td><td>

Enables ServiceNow to be embedded directly within a Microsoft Teams meeting kicked off from a Major Incident.

</td><td>

Inactive

</td><td>

false

</td><td>

sn\_notify\_msteams

</td></tr><tr id="plugin_com.glide.ui.mergetool" class="plugin_reference"><td class="name">

Merge Tool\[com.glide.ui.mergetool\]

</td><td class="description">

User interface for performing merges between two payloads.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

-   com.glide.ui.angular
-   com.glide.snc\_code\_editor

</td></tr><tr id="plugin_com.glide.source_control" class="plugin_reference"><td class="name">

Metadata Source Control\[com.glide.source\_control\]

</td><td class="description">

Source control integration applies and commits changes in an external repository.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

com.glide.system\_update\_set

</td></tr><tr id="plugin_com.snc.metadata_tree" class="plugin_reference"><td class="name">

Metadata Tree\[com.snc.metadata\_tree\]

</td><td class="description">

Hierarchical representation of metadata.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

com.snc.apps\_file

</td></tr><tr><td>

Metadefender Integration\[com.snc.threat.metadefender\]

</td><td>

Activation of this plugin on production instances may require a separate license. Contact ServiceNow for details.

</td><td>

Inactive

</td><td>

false

</td><td>

com.snc.threat.intelligence

</td></tr><tr id="plugin_com.glide.metrics" class="plugin_reference"><td class="name">

Metric Definition\[com.glide.metrics\]

</td><td class="description">

Provides an easy, declarative way to define metrics and allows the definitions to be tracked and stored by the system.

</td><td>

Active

</td><td class="has_demo_data">

true

</td><td class="requires">

com.glide.schedules

</td></tr><tr><td>

MetricBase\[com.snc.clotho\]

</td><td>

Time-series data storage and processing.

</td><td>

Inactive

</td><td>

false

</td><td class="requires">

-   com.glide.highcharts
-   com.glide.hub.flow\_trigger

</td></tr><tr><td>

MetricBase Demo\[com.snc.clotho.demo\]

</td><td>

Sample time-series data you can use to explore MetricBase functionality.

</td><td>

Inactive

</td><td>

true

</td><td>

com.snc.clotho

</td></tr><tr><td>

Microsoft AD Spoke for IntegrationHub\[com.sn.ad.spoke\]

</td><td>

The AD Spoke for IntegrationHub provides actions that a Process Analyst can use when designing flows. The actions allow them to automate the management of users, groups, computers, and objects in AD.

</td><td>

Inactive

</td><td>

false

</td><td class="requires">

-   com.glide.hub.designer\_backend.model
-   com.glide.hub.action\_step.powershell

</td></tr><tr><td>

Microsoft AD Spoke for Password Reset\[com.snc.password\_reset.ms.ad.spoke\]

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Microsoft Azure AD Spoke for IntegrationHub\[com.sn.azure\_ad.spoke\]

</td><td>

The Azure AD Spoke for IntegrationHub provides actions that a Process Analyst can use when designing flows. The actions allow them to automate the management of users, security groups, and office groups. User management includes applying licenses that result in user provisioning into Office 365.

</td><td>

Inactive

</td><td>

false

</td><td class="requires">

-   com.glide.hub.designer\_backend.model
-   com.glide.hub.action\_step.rest

</td></tr><tr><td>

Microsoft Azure AD Spoke for Password Reset\[com.sn.password\_reset.aad.spoke\]

</td><td>

The Password Reset Azure AD Scoped App provides a prebuilt connection to credential stores in Azure AD, allowing reset and changing of password.

</td><td>

Active

</td><td>

false

</td><td class="requires">

-   com.sn.azure\_ad.spoke
-   com.glideapp.password\_reset
-   com.sn.password\_reset.ah

</td></tr><tr><td>

Microsoft Azure Translation Spoke\[com.glide.microsoft\_translation\_spoke\]

</td><td>

Using Microsoft translation services, adds ability to translate text from one language to another and detect the language of text.

</td><td>

Inactive

</td><td>

false

</td><td>

com.glide.hub.integrations

</td></tr><tr><td>

Microsoft Integrations - Core\[sn\_now\_teams\]

 \(Available in the ServiceNow Store\)

</td><td>

Scoped application for store release of Microsoft Teams integration with ServiceNow.

</td><td>

Inactive

</td><td>

false

</td><td>

-   com.glide.channelproxy
-   com.glide.cs.adapter
-   com.glide.hub.designer\_backend.model
-   com.snc.msteams.app.core
-   com.glide.hub.action\_step.rest
-   com.glide.hub.integration.runtime
-   sn\_msteams\_ahv2
-   sn\_tcm\_collab\_hook
-   sn\_now\_azure
-   sn\_va\_teams

</td></tr><tr><td>

Microsoft OneDrive Spoke\[com.sn.onedrive.spoke\]

</td><td>

Contains data model needed to integrate with third-party document service providers.

</td><td>

Active

</td><td>

false

</td><td>

 

</td></tr><tr><td>

Microsoft OneDrive document services Spoke\[com.sn.documents.onedrive\]

</td><td>

Collaborate in Microsoft OneDrive and perform copy, delete, restore, and version actions on documents directly in a ServiceNow instance. This integration is bi-directional: Changes are reflected in both Microsoft OneDrive and in the instance.

</td><td>

Active

</td><td>

false

</td><td>

-   com.snc.multiprovider\_documents
-   com.sn.onedrive.spoke
-   com.sn.azure\_ad.spoke

</td></tr><tr><td>

Microsoft SharePoint Spoke\[sn\_sp\_spoke\]

 \(Available in the ServiceNow Store\)

</td><td>

Enables the Integration Hub to connect with SharePoint.

</td><td>

Active

</td><td>

false

</td><td>

-   com.glide.cobject
-   com.glide.hub.dynamic\_inputs
-   com.glide.hub.action\_step.rest
-   com.glide.hub.action\_type.datastream
-   com.glide.hub.integration.runtime

</td></tr><tr id="plugin_com.glideapp.agent" class="plugin_reference"><td class="name">

MID Server\[com.glideapp.agent\]

</td><td class="description">

The Management, Instrumentation, and Discovery \(MID\) Server is a Java application that runs as a Windows service or UNIX daemon. The MID Server facilitates communication and movement of data between the ServiceNow platform and external applications, data sources, and services.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

com.glide.custom\_web\_service

</td></tr><tr><td>

MID Server Distributed Cluster\[com.snc.agent.distributed.cluster\]

</td><td>

Enables the MID Server distributed cluster type, for Operational Intelligence.

</td><td>

Inactive

</td><td>

false

</td><td>

com.snc.sa.metric

</td></tr><tr><td>

MID Server Key Management Framework Signature Configuration\[com.glideapp.agent.kmf\_config\]

</td><td>

Creates KMF signature configuration records for MID Server tables.

</td><td>

 

</td><td>

false

</td><td>

 

</td></tr><tr><td>

Mobile Analytics\[com.glide.mobile.analytics\]

</td><td>

Checks for new mobile applications to register, syncs Mobile Analytics instance settings to the ServiceNow server, and provides users access to the Mobile Analytics Dashboard​. This plugin adds the mobile\_analytics\_admin and mobile\_analytics\_viewer roles.

</td><td>

Active

</td><td>

false

</td><td>

com.glide.serviceproxy

</td></tr><tr><td>

Mobile App Builder\[sn\_mab\]

 \(Available in the ServiceNow Store\)

</td><td>

A ServiceNow builder for native mobile applications.

</td><td>

Active

</td><td>

false

</td><td>

sn\_mab\_api

</td></tr><tr><td>

Mobile App Builder API\[sn\_mab\_api\]

 \(Available in the ServiceNow Store\)

</td><td>

An API for mobile application support with access to mobile application configurations.

</td><td>

Active

</td><td>

false

</td><td>

None

</td></tr><tr><td>

Mobile Card Builder\[sn\_mobile\_card\_bui\]

 \(Available in the ServiceNow Store\)

</td><td>

An interactive item view, view template, and view config builder tool integrated with Mobile Studio.

</td><td>

Active

</td><td>

false

</td><td>

None

</td></tr><tr><td>

Mobile Employee My Assets\[com.glide.mobile-employee.myassets\]

</td><td>

This plugin contains the configuration and records to create the my assets view that are used in Mobile Employee Experience native application. Do not activate this plugin directly. Activating com.glide.mobile-employee will activate this plugin for you.

</td><td>

Inactive

</td><td>

false

</td><td>

 

</td></tr><tr id="plugin_com.snc.itil_mobile" class="plugin_reference"><td class="name">

Mobile Device ITIL and Service Management\[com.snc.itil\_mobile\]

</td><td class="description">

Applications and modules for ITIL and Service Management.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

-   com.glide.labels
-   com.glide.mobile

</td></tr><tr><td>

Mobile Location Tracking\[com.slide.sg.location.tracking\]

 \(New in Utah\)

</td><td>

Enables use of action-based location tracking. This tracking option starts and stops tracking based on actions the user performs. The manual tracking option isn’t dependent on the installation of this plugin.

</td><td>

Active

</td><td>

false

</td><td>

-   com.snc.geolocation
-   com.glide.sg

</td></tr><tr><td>

Mobile SDK\[com.snc.mobile\_sdk\]

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Mobile Studio\[com.glide.sg-studio\]

</td><td>

Plugin for Mobile Studio

</td><td>

Active

</td><td>

false

</td><td>

com.glide.sg

</td></tr><tr id="plugin_com.glide.ui.m" class="plugin_reference"><td class="name">

Mobile UI\[com.glide.ui.m\]

</td><td class="description">

User interface for mobile devices running iOS 6+ or Android 4+ with the Chrome browser. Provides nearly full-product functionality. Adds a System Mobile UI application to the application navigator in the standard UI for configuring the mobile UI.

</td><td>

Active

</td><td class="has_demo_data">

true

</td><td class="requires">

-   com.glide.wiki
-   com.glide.labels
-   com.glide.db\_images
-   com.glide.ui.font\_icons
-   com.glide.ui.ng
-   com.glide.ui.zepto
-   com.glide.ui.tablet.theme
-   com.glide.ui.recent\_selections
-   com.glide.ui.table\_titles
-   com.snc.platform.security.oauth
-   com.glide.ui.magellan\_navigator\_api
-   com.glide.ui.list\_api
-   com.glide.notification.push

</td></tr><tr><td>

Mobile Publishing\[com.glide.sn-mobile-whitelabel\]

</td><td>

Mobilew plugin to handle custom app branding requests, statuses, and publishing.

</td><td>

Inactive

</td><td>

false

</td><td>

 

</td></tr><tr id="plugin_com.snc.model" class="plugin_reference"><td class="name">

Model Management\[com.snc.model\]

</td><td class="description">

Enables you to manage and maintain model categories, models, suites, and bundled models.

</td><td>

Active

</td><td class="has_demo_data">

true

</td><td class="requires">

 

</td></tr><tr class="plugin_reference"><td class="name">

Modeling Engine\[com.snc.financial\_management\]

</td><td class="description">

Enables financial analysts to assemble spending data, build cost models, and generate reports to show how funds are being used. Activation of this plugin on production instances may have licensing implications. Contact your ServiceNow account team for details.

</td><td>

Inactive

</td><td class="has_demo_data">

true

</td><td class="requires">

-   com.snc.itfm\_core
-   com.snc.financial\_planning
-   com.snc.cost\_management
-   com.snc.service\_charging

</td></tr><tr><td>

Modeling Engine – ATF Tests\[com.snc.financial\_management.atf\]

</td><td>

ATF tests for Modeling Engine

</td><td>

Inactive

</td><td>

false

</td><td>

com.snc.financial\_management\_model

</td></tr><tr><td>

Multi Provider Document Services Framework\[com.snc.multiprovider\_documents\]

 \(New in Tokyo\)

</td><td>

Enables your team to collaborate in real time and add versions, store, copy, delete, restore, and upload documents.

</td><td>

Active

</td><td>

false

</td><td>

None

</td></tr><tr><td>

Mutex stats\[com.glide.stats.mutex\]

</td><td>

Mutex stats.

</td><td>

Active

</td><td>

false

</td><td>

com.glide.stats

</td></tr><tr id="plugin_com.snc.asset_myassets" class="plugin_reference"><td class="name">

My Assets\[com.snc.asset\_myassets\]

</td><td class="description">

Provides users with self-service access to their own assets, contracts, and requests.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

com.snc.asset\_management

</td></tr><tr><td>

Name-Value Pairs field editor\[com.glide.ui.name\_values\_editor\]

</td><td>

Adds a detailed editor for name-value pairs field types.

</td><td>

Active

</td><td>

false

</td><td>

com.glide.ui.ng

</td></tr><tr><td>

Natural Language Query\[com.snc.nlq\]

</td><td>

Translates natural language utterances into search queries to quickly find and filter data.

</td><td>

Inactive

</td><td>

false

</td><td>

com.glide.platform\_ml

</td></tr><tr><td>

Next Best Action for Customer Service\[com.snc.cs\_next\_best\_action\]

</td><td>

Provides Next Best Action and Guided Decision configurations and features specific to Customer Service.

</td><td>

Active

</td><td>

false

</td><td>

-   com.sn\_customerservice
-   com.snc.next\_best\_action

</td></tr><tr id="plugin_com.snc.ng_bsm" class="plugin_reference"><td class="name">

Next-Gen BSM\[com.snc.ng\_bsm\]

</td><td class="description">

Next Generation BSM \(NG-BSM\) built on D3 and Angular. Provides an enhanced, modern interactive graphical interface to visualize Configuration Items \(CIs\) and their relationships. Provides filtering capabilities to manage data being displayed and displays related information for CIs such as Events, Incidents, Problems, and Changes.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

com.glide.ui.heisenberg

</td></tr><tr id="plugin_com.glide.ui.ng.guided_flow" class="plugin_reference"><td class="name">

NG Common for the Guided Flow experience\[com.glide.ui.ng.guided\_flow\]

</td><td class="description">

Common Angular Components for the Guided Flow experience.

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

-   com.glide.ui.tablet.theme
-   com.glide.ui.ng
-   com.glide.ui.themes.doctype

</td></tr><tr id="plugin_com.glide.ui.ng" class="plugin_reference"><td class="name">

NG shared components\[com.glide.ui.ng\]

</td><td class="description">

Provides libraries and services common to plugins using Angular.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

-   com.glide.ui.angular
-   com.glide.ui.angularui
-   com.glide.ui.ng.amb

</td></tr><tr><td>

NLU Active Learning - Properties\[com.glide.nlu.active\_learning\_properties\]

</td><td>

Installs the required properties for NLU Active Learning.

</td><td>

Active

</td><td>

false

</td><td>

com.glide.nlu

</td></tr><tr><td>

NLU Common Model\[com.glide.nlu.model\]

</td><td>

The NLU Common Model plugin packages commonly used pattern entities that can be imported and used in any NLU model in the NLU Model Builder. Commonly used patterns like email, phone and ServiceNow specific pattern entities like INT, RITM are made available.

</td><td>

Inactive

</td><td>

false

</td><td>

com.glide.nlu

</td></tr><tr><td>

NLU Workbench\[com.snc.nlu\_studio\]

</td><td>

Enables the creation of Natural Language Understanding \(NLU\) models. These models can understand the intent \(action\) and entities \(details about the action\) for a given user utterance/sentence.

</td><td>

Active

</td><td>

 

</td><td>

 

</td></tr><tr><td>

NLU Workbench - Advanced Features\[com.snc.nlu.workbench.advanced\]

 \(Available in the ServiceNow Store\)

</td><td>

Adds additional features to NLU Workbench including NLU Conflict Review, NLU Batch Testing, and NLU Model Performance.

</td><td>

Active

</td><td>

false

</td><td>

-   com.snc.nlu\_studio
-   com.glide.nlu
-   com.glide.platform\_ml
-   sn\_nlu\_discovery \(store\)

</td></tr><tr><td>

NLU Workbench - Core\[com.glide.nlu\]

</td><td>

Core NLU. Installs the required tables for persisting NLU models that are created using the NLU Model Builder.

</td><td>

Active

</td><td>

false

</td><td>

 

</td></tr><tr><td>

Notify Connector for Microsoft Teams\[sn\_notify\_msteams\]

 \(Available in the ServiceNow Store\)

</td><td>

Expands the Notify providers by managing and initiating a Microsoft Teams meeting directly from any task record.

</td><td>

Inactive

</td><td>

false

</td><td>

-   com.snc.notify
-   sn\_now\_azure
-   sn\_msteams\_com\_spk

</td></tr><tr id="plugin_com.glide.data_services_canonicalization.client" class="plugin_reference"><td class="name">

Normalization Data Services Client\[com.glide.data\_services\_canonicalization.client\]

</td><td class="description">

Helps maintain consistency by ensuring that records for a given company refer to that company by the same name.

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

com.snc.cmdb

</td></tr><tr id="plugin_com.glide.data_services_canonicalization.config" class="plugin_reference"><td class="name">

Normalization Data Services Configuration\[com.glide.data\_services\_canonicalization.config\]

</td><td class="description">

Normalization Data Services Configuration.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

com.snc.guided\_setup

</td></tr><tr><td>

Notification Preference Service\[com.glide.notification.preference.service\]

</td><td>

Defines javascript and REST API for configuring notification preferences.

</td><td>

Active

</td><td>

false

</td><td>

com.glide.notification

</td></tr><tr><td class="name">

Notification Preference User Interface\[com.glide.notification.preference.ui\]

</td><td class="description">

Defines the user interface for the Notifications tab in the system settings menu.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

NG shared components, com.glide.notification.subscription, Notification System Push Addon, com.glide.notification.preference.service

</td></tr><tr id="plugin_com.glide.notification.push" class="plugin_reference"><td class="name">

Notification System Push Addon\[com.glide.notification.push\]

</td><td class="description">

Adds support for push notifications to the notification system.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

-   com.glide.notification
-   com.glide.push

</td></tr><tr id="plugin_com.snc.notify" class="plugin_reference"><td class="name">

Notify\[com.snc.notify\]

</td><td class="description">

Provides powerful platform features for workflow-driven voice calls, conference calls, and SMS messages making it possible to create flexible Interactive Voice Response \(IVR\) systems to do virtually anything. Requires the Twilio Driver and a separate contract with Twilio for SMS and Voice capabilities.

</td><td>

Inactive

</td><td class="has_demo_data">

true

</td><td class="requires">

-   com.glide.phone\_number
-   com.snc.notify.twilio

</td></tr><tr id="plugin_com.snc.notify.twilio" class="plugin_reference"><td class="name">

Notify-Twilio Direct driver\[com.snc.notify.twilio\_direct\]

</td><td class="description">

Provides Notify support for Twilio. Requires a separate contract with Twilio for SMS/Voice capabilities.

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

-   com.snc.sn\_context
-   com.snc.notify

</td></tr><tr><td>

Now Experience Analytics\[com.snc.now-experience-analytics\]

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

NowMQ v2 Messaging API\[com.snc.nowmq\_v2\]

</td><td>

Provides a simple-to-use queue with features like priorities, completion FIFO, custom states, and backend reconfiguration or migration without any client changes.

</td><td>

Active

</td><td>

false

</td><td>

com.snc.nowmq\_v2\_apis

</td></tr><tr><td>

Field Encryption Enterprise \[com.glide.now.platform.encryption\]

</td><td>

Field Encryption Enterprise enables field encryption with NIST best practice Key Management Framework \(KMF\) key lifecycle management and FIPS 140-2-L3 HSM key protection along with the automating Key and Data Migration jobs.

</td><td>

 

</td><td>

false

</td><td>

-   com.glide.kmf.global
-   com.glide.encryption

</td></tr><tr id="plugin_com.snc.platform.security.oauth" class="plugin_reference"><td class="name">

OAuth 2.0\[com.snc.platform.security.oauth\]

</td><td class="description">

The implementation of OAuth 2.0 to support token granting and authentication.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

-   com.glide.certificates
-   com.snc.platform.security.oauth.legacy

</td></tr><tr id="plugin_com.snc.platform.security.oauth.legacy" class="plugin_reference"><td class="name">

OAuth 2.0 legacy \(Do not activate. Use 'OAuth 2.0'\)\[com.snc.platform.security.oauth.legacy\]

</td><td class="description">

Legacy implementation of OAuth 2.0. Install com.snc.platform.security.oauth instead.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

 

</td></tr><tr id="plugin_com.glide.odbc.commons" class="plugin_reference"><td class="name">

ODBC Commons\[com.glide.odbc.commons\]

</td><td class="description">

ODBC Commons.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

 

</td></tr><tr><td>

Omni Experience - Standard Feature Set\[sn-oe-sfs\]

 \(Available in the ServiceNow Store\)

</td><td>

Contains multiple Conversational Interfaces applications, including Conversational Interfaces Admin Console, diagnostic content for Advanced Work Assignment, and Sidebar.

</td><td>

Active

</td><td>

true

</td><td>

-   com.glide.cs.collab com.glide.cs.chatbot.lite
-   com.sn.ace\_framework

</td></tr><tr><td>

Omnichannel Callback\[sn\_omni\_callback\]

 \(Available in the ServiceNow Store\)

</td><td>

Adds new set of platform capabilities that enable other ServiceNow applications to display or announce callback options to the users.

</td><td>

Active

</td><td>

false

</td><td>

-   com.glide.cs
-   com.glide.interaction.awa
-   com.glide.cs.custom.adapter
-   com.snc.appointment\_booking

</td></tr><tr><td>

Omnichannel Callback for Customer Service Management \[com.sn\_omnichannel\_callback\]

 \(Available in the ServiceNow Store\)

</td><td>

Extends Omnichannel Callback capabilities to support CSM specific use cases. This includes customer experience, agent experience and CSM data model support.

</td><td>

Active

</td><td>

false

</td><td>

-   com.sn.omnichannel.callback
-   com.sn\_customerservice

</td></tr><tr><td>

On-Call: Mobile Push Notifications\[com.sn\_on\_call\_m\_notif\]

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

On-Call: PA and Reports Content Pack\[com.snc.on\_call.par.content\]

</td><td class="requires">

-   Dashboards
-   Reports and Performance Analytics content pack for On-Call Schedules and Escalations

</td><td>

Active

</td><td>

false

</td><td class="requires">

-   com.glide.script.vtable
-   com.snc.on\_call\_rotation

</td></tr><tr id="plugin_com.snc.on_call_rotation" class="plugin_reference"><td class="name">

On-Call Scheduling\[com.snc.on\_call\_rotation\]

</td><td class="description">

Provides the ability to create on-call schedules and escalation trees. When an incident is created, dynamically route the escalation to an on-call resource. On Call allows you to configure and build different on-call schedules per process and assignment group. When utilizing the Notify plugin, resources can use SMS and Voice escalations to interact with the escalation to acknowledge incidents, and so on.

</td><td>

Inactive

</td><td class="has_demo_data">

true

</td><td class="requires">

-   com.glide.schedules
-   com.glide.notification
-   com.glide.ui.ng
-   com.snc.app.calendar
-   com.snc.fullcalendar

</td></tr><tr id="plugin_com.sn_openframe" class="plugin_reference"><td class="name">

Openframe\[com.sn\_openframe\]

</td><td class="description">

An interface to integrate external communication systems with ServiceNow. This plugin brings a UI frame that is accessible and available anywhere within ServiceNow screens.

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

com.glide.ui.ng

</td></tr><tr><td>

Openframe Integration App\[com.sn\_openframe\_integration\]

</td><td>

Holds records to support UIB framework.

</td><td>

Inactive

</td><td>

false

</td><td>

 

</td></tr><tr><td>

Operational Intelligence\[com.snc.sa.metric\]

</td><td>

Operational Intelligence provides the ability to capture, and then explore and analyze operational metrics data, identifying and indicating anomalies.

</td><td>

Active

</td><td>

false

</td><td class="requires">

-   com.glideapp.itom.snac
-   com.snc.sa.mid.webserver
-   com.snc.clotho
-   com.glide.highcharts
-   com.snc.agent.distributed.cluster
-   com.glide.ui.list\_v3\_components
-   com.snc.itom.ui
-   com.snc.sa.metric.health
-   com.oi-scoped-app,

</td></tr><tr><td>

Operational Intelligence - WS Scoped App\[com.oi-scoped-app\]

</td><td>

Operational Intelligence - Workspace Scoped App for different user interfaces.

</td><td>

Active

</td><td>

false

</td><td>

com.glide.graphq

</td></tr><tr><td>

Operational Technology Change Management\[com.sn\_ot\_chg\_mgmt\]

\(Available in the ServiceNow Store\)

</td><td>

Enables engineers to implement changes to Operational Technology assets and production processes.

</td><td>

Active

</td><td>

false

</td><td>

-   CMDB CI Class Models \(com.sn\_cmdb\_ci\_class\)
-   ISA Equipment Model \(com.sn\_isa\_model\)
-   Operational Technology Manager \(com.sn\_ot\_foundation\)

</td></tr><tr><td>

Operational Technology Incident Management\[com.sn\_ot\_inc\_mgmt\]

\(Available in the ServiceNow Store\)

</td><td>

Enables manufacturers to manage OT device incidents from open to closure.

</td><td>

Active

</td><td>

false

</td><td>

-   CMDB CI Class Models \(com.sn\_cmdb\_ci\_class\)
-   ISA Equipment Model \(com.sn\_isa\_model\)
-   Operational Technology Manager \(com.sn\_ot\_foundation\)

</td></tr><tr><td>

Operational Technology Manager\[com.sn\_ot\_foundation\]

\(Available in the ServiceNow Store\)

</td><td>

Enables manufacturers to aggregate OT data from multiple sources to build a solid data foundation of OT environments.

</td><td>

Active

</td><td>

False

</td><td>

-   com.sn\_mfg\_common
-   com.sn\_cmdb\_ci\_class
-   com.sn\_isa\_model
-   com.sn\_otsm\_sgc
-   com.sn\_datagrid

</td></tr><tr><td>

Order Guide Sequential Fulfillment\[com.glideapp.servicecatalog.order\_guide\_sequencing\]

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr id="plugin_com.glide.email_ordered_processing" class="plugin_reference"><td class="name">

Ordered Email Processing\[com.glide.email\_ordered\_processing\]

</td><td class="description">

Allows inbound email actions to be ordered, and programmatically stop processing.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

 

</td></tr><tr><td>

Organization Extension\[com.snc.organization\_extension\]

</td><td>

Provides Goals, Enterprise Strategy and Business Unit strategy entities.

</td><td>

Active

</td><td>

true

</td><td>

 

</td></tr><tr id="plugin_com.snc.organization_management" class="plugin_reference"><td class="name">

Organization Management\[com.snc.organization\_management\]

</td><td class="description">

 

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

 

</td></tr><tr><td>

Outage Numbering\[com.snc.outage\_numbering\]

</td><td>

This plugin will introduce a new unique identifier column for the outage table. This plugin is activated automatically for all instances except those who already have a number prefix column on the outage table. Please do not activate this plugin if you have a number prefix for this table.

</td><td>

Active

</td><td>

 

</td><td>

 

</td></tr><tr id="plugin_com.glide.email_outbound" class="plugin_reference"><td class="name">

Outbound Email Notifications\[com.glide.email\_outbound\]

</td><td class="description">

Enables outbound email notifications.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

 

</td></tr><tr><td>

Outbound HTTP Log\[com.glide.outbound\_http\_log\]

</td><td>

Outbound HTTP request log

</td><td>

Active

</td><td>

false

</td><td>

 

</td></tr><tr><td>

Outbound Tracking\[com.glide.outbound\_tracking\]

</td><td>

Outbound request tracking.

</td><td>

Active

</td><td>

false

</td><td>

com.glide.usageanalytics

</td></tr><tr><td>

Outlook Actionable Messages\[com.sn\_ms\_oam\]

</td><td>

Outlook Actionable Messages

</td><td>

Active

</td><td>

false

</td><td>

com.snc.platform.security.oauth

</td></tr><tr><td>

Outsourced Customer Service \(Maintenance mode only\)\[com.snc.outsourced\_service\_provider\]

</td><td>

Enables onboarding Outsourced Service Provider \(OSP\) organizations. An enterprise can engage OSPs to provide customer service to external customers for reasons such as regional support, different languages, seasonal availability and so on.

</td><td>

Active

</td><td>

false

</td><td class="requires">

-   com.sn\_customerservice
-   com.snc.outsourced\_service\_provider

</td></tr><tr id="plugin_com.glide.ui.overview_help" class="plugin_reference"><td class="name">

Overview Pages\[com.glide.ui.overview\_help\]

</td><td class="description">

Framework for Overview pages.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

com.glide.ui.angular

</td></tr><tr id="plugin_com.glide.script.packages_call_removal" class="plugin_reference"><td class="name">

Packages Call Removal Tool\[com.glide.script.packages\_call\_removal\]

</td><td class="description">

Scans scripts for Packages calls to ServiceNow Java classes, proposes changes to replace them with alternate scriptable names, and facilitates the script changes. Packages calls to ServiceNow Java classes will eventually be disallowed in a future ServiceNow release, and this utility helps prepare an instance for that.

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

 

</td></tr><tr><td>

PA Dashboard for NLU Model Builder\[com.glide.nlu.pa\]

</td><td>

The NLU Model Builder PA plugin tracks the performance of NLU models being used in Virtual Agent. The plugin packages an NLU Performance dashboard, which reports on how many predictions were correct, how many predictions were skipped by the NLU model and how many were considered wrong by Virtual Agent users.

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

PA New Model\[com.snc.pa.datamodel\]

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Package Optimizer\[com.glide.package\_optimizer\]

</td><td>

Optimizes the application upgrade process by comparing the generated file hashes from the previous install.

</td><td>

Active

</td><td>

false

</td><td>

None

</td></tr><tr><td>

PAR Intelligence\[com.snc.par.intelligence\]

 \(New in Utah\)

</td><td>

The core plugin for PAR Intelligence. The classpath for the Forecast Glide Scriptable API, which lets you apply Performance Analytics indicator forecasting to other data sources.

</td><td>

Active

</td><td>

false

</td><td>

 

</td></tr><tr><td>

PAR Visualization Migration\[com.snc.par.visualization.migration\]

</td><td>

Migrates the JSON structure of seismic visualization components in pre-San Diego instances to the new format. This plugin also migrates sn-component-visualization json to now-visualization-extensions json structure.

</td><td>

Active

</td><td>

false

</td><td>

now-visualization-extensions

</td></tr><tr id="plugin_com.glideapp.password_reset" class="plugin_reference"><td class="name">

Password Reset\[com.glideapp.password\_reset\]

</td><td class="description">

Provides the ability to create self-service and service desk password reset processes for a ServiceNow instance.

</td><td>

Active

</td><td class="has_demo_data">

true

</td><td class="requires">

-   com.snc.process\_flow\_formatter
-   com.glide.notification
-   com.glide.usageanalytics

</td></tr><tr><td>

Password Reset API \[com.glideapp.password\_reset.api\]

</td><td>

Contains scoped APIs related to the Password Reset application.

</td><td>

Active

</td><td>

false

</td><td>

 

</td></tr><tr><td>

Password Reset - Orchestration Add-on\[com.glideapp.password\_reset.addon.orchestration\]

</td><td>

Password reset add-on to enable the use of ServiceNow Orchestration. Includes support for Active Directory and remote SOAP based credential systems.

</td><td>

Inactive

</td><td>

 

</td><td>

Password Reset, Orchestration

</td></tr><tr><td>

Password Reset Spoke\[com.sn.password\_reset.ah\]

</td><td>

Provides subflows and actions in Integration Hub required for the Password Reset application.

</td><td>

Active

</td><td>

false

</td><td>

com.glide.hub.designer\_backend.model

</td></tr><tr><td class="name">

Password Reset Windows App\[com.glideapp.password\_reset\_desktop\]

</td><td class="description">

Password Reset Windows integration.

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

 

</td></tr><tr><td>

Pattern Designer Enhancements\[sn\_itom\_pde\]

 \(Available in the ServiceNow Store\)

</td><td>

Offers the Command Validation Framework. Provides discovery administrators with ability to validate credential access for specific commands, including Unix and Windows commands, SNMP queries, SNMP walk, Registry queries, HTTP GET calls.

</td><td>

Inactive

</td><td>

false

</td><td>

None

</td></tr><tr><td class="name">

Patient Support Services \[sn\_patientservice\]

 \(Available in the ServiceNow Store\)

</td><td class="description">

Streamlines the patient onboarding, education, and engagement for various patient support services such as discount plans, adherence programs, opioid, and diabetes management.

</td><td>

Inactive

</td><td class="has_demo_data">

true

</td><td class="requires">

-   com.snc.business\_location
-   com.snc.csm\_case\_types
-   com.snc.household
-   com.snc.install\_base
-   com.glide.encryption
-   com.sn\_external\_user\_register
-   com.snc.pdf\_generator
-   com.snc.signaturepad
-   com.glideapp.user\_criteria.scoped.api
-   sn\_hcls
-   sn\_csm\_playbook
-   com.sn\_ind
-   sn\_doc
-   sn\_prd\_pm
-   sn\_ciwf\_ui\_cmpnt

</td></tr><tr><td>

Payment Operations\[com.sn\_bom\_payment\]

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr id="plugin_com.snc.pdf_generator" class="plugin_reference"><td class="name">

PDF Generator\[com.snc.pdf\_generator\]

</td><td class="description">

Provides a tool to generate PDF documents.The Human Resources application uses this with various documents.

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

com.snc.signaturepad

</td></tr><tr id="plugin_com.snc.pa" class="plugin_reference"><td class="name">

Performance Analytics\[com.snc.pa\]

</td><td class="description">

Enables users to define and track key performance indicators \(KPIs\) and visualize these in scorecards and dashboards. Users can report and compare multiple time series, do advanced trend analysis, and compare their performance with preset targets.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

-   com.glide.ui.angular
-   com.glideapp.report
-   com.glideapp.home.publishers
-   com.snc.core.automation
-   com.glide.usageanalytics

</td></tr><tr><td>

Performance Analytics - Administrator Console\[com.snc.pa.administration.console\]

</td><td>

A single console where you can: -   Explore and manage Performance Analytics widgets and dashboards, including Platform Analytics Solutions
-   Diagnose and resolve configuration errors
-   View usage analytics
-   Modify advanced configuration settings
-   Access ServiceNow help.

</td><td>

Active

</td><td>

false

</td><td class="requires">

-   com.snc.pa
-   com.glide.ui.ng
-   com.glide.ui.ng.amb
-   com.snc.pa.diagnostics
-   com.snc.pa.usage.overview

</td></tr><tr id="plugin_com.snc.pa.configurationgenerator" class="plugin_reference"><td class="name">

Performance Analytics - Configuration Generator\[com.snc.pa.configurationgenerator\]

</td><td class="description">

Provides a configuration generator for creating a set of Performance Analytics indicators, breakdowns, dashboards, and widgets based on the task-derived table.

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

com.snc.pa

</td></tr><tr><td>

Performance Analytics - GRC: Advanced Dashboards\[com.sn\_grc\_pa\_advanced\]

</td><td>

Contains the Advanced Performance Analytics dashboards created for GRC.

</td><td>

Inactive

</td><td>

true

</td><td>

-   com.sn\_compliance
-   com.sn\_risk\_advanced
-   com.sn\_audit

</td></tr><tr><td>

Performance Analytics - Content Pack - Advanced Work Assignment\[com.snc.pa.awa\]

</td><td>

Provides Performance Analytics indicators and visualizations for Advanced Work Assignment. Activation of this plugin on production instances may require a separate Performance Analytics license. Contact ServiceNow for details.

</td><td>

Active

</td><td>

false

</td><td class="requires">

-   com.snc.pa
-   com.glide.awa

</td></tr><tr><td>

Performance Analytics - Content Pack - Application Portfolio Management\[com.snc.pa.apm\]

</td><td>

Application Portfolio Management dashboards developed using Performance analytics premium.

</td><td>

Inactive

</td><td>

true

</td><td class="requires">

-   com.snc.apm
-   com.snc.pa

</td></tr><tr><td>

Performance Analytics - Content Pack - Application Portfolio Management and Change Management\[com.snc.pa.apm.change\_request\]

</td><td>

Provides integration of Application Portfolio Management with Change Management that enables performance analytics dashboards of business applications associated with Change requests.Activation of this plugin on production instances may have licensing implications. Contact your ServiceNow account team for details.

</td><td>

Inactive

</td><td>

true

</td><td class="requires">

-   com.snc.apm
-   com.snc.pa
-   com.snc.pa.change

</td></tr><tr><td>

Performance Analytics - Content Pack - Application Portfolio Management and Problem Management\[com.snc.pa.apm.problem\]

</td><td>

Provides integration of Application Portfolio Management with Problem Management which enables performance analytics dashboards of business applications.Activation of this plugin on production instances may have licensing implications. Contact your ServiceNow account team for details.

</td><td>

Inactive

</td><td>

true

</td><td class="requires">

-   com.snc.apm
-   com.snc.pa
-   com.snc.pa.problem

</td></tr><tr id="plugin_com.snc.pa.change" class="plugin_reference"><td class="name">

Performance Analytics - Content Pack - Change Management\[com.snc.pa.change\]

</td><td class="description">

Provides Performance Analytics indicators and visualizations for Change Management. Activation of this plugin on production instances may require a separate Performance Analytics license. Contact ServiceNow for details.

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

-   com.snc.pa
-   com.glideapp.report.itsm.change.overview

</td></tr><tr><td>

Performance Analytics - Content Pack - Cloud Resources\[com.sn\_disco\_cd\]

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Performance Analytics - Content Pack - Communities\[com.snc.pa.communities\]

</td><td>

Provides Performance Analytics indicators and visualizations for Communities. Activation of this plugin on production instances may require a separate Performance Analytics license. Contact ServiceNow for details.

</td><td>

Inactive

</td><td>

false

</td><td class="requires">

-   com.snc.pa
-   com.sn\_communities

</td></tr><tr id="plugin_com.snc.pa.cmdb" class="plugin_reference"><td class="name">

Performance Analytics - Content Pack - Configuration Management \(CMDB\)\[com.snc.pa.cmdb\]

</td><td class="description">

Provides Performance Analytics indicators and visualizations for Configuration Management \(CMDB\). Activation of this plugin on production instances may require a separate Performance Analytics license. Contact ServiceNow for details.

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

-   com.snc.pa
-   com.snc.cmdb
-   com.snc.pa.change

</td></tr><tr><td>

Performance Analytics - Content Pack - Content Analytics\[com.snc.pa.premium.content\_analytics\]

</td><td>

Content Analytics - Performance Analytics

</td><td>

Active

</td><td>

false

</td><td class="requires">

-   com.sn\_content\_analytics
-   com.snc.pa.premium

</td></tr><tr><td>

Performance Analytics - Content Pack - Content Automation\[com.snc.pa.premium.content\_automation\]

</td><td>

Content Automation Analytics

</td><td>

Active

</td><td>

false

</td><td class="requires">

-   com.sn\_content\_analytics
-   com.sn\_content\_automation
-   com.snc.pa.premium

</td></tr><tr><td>

Performance Analytics - Content Pack - Customer Service Management - Advanced\[com.snc.pa.customer\_service\_advanced\]

</td><td>

Updates the Customer Service dashboard and incorporates indicators for the following plugins: Major Issue Management, Customer Service Case Action Status, Customer Service with Request Management, Customer Service with Service Management, Agent Chat, Advanced Work Assignment for CSM, and Performance Analytics - Content Pack - Advanced Work Assignment. Activate these plugins in order to view the related indicators. Without these plugins, indicators may not display correctly.

 Activation of the Performance Analytics â€“ Content Pack â€“ Customer Service Management - Advanced plugin on production instances may require a separate performance Analytics license. Contact ServiceNow for details.

</td><td>

Active

</td><td>

false

</td><td class="requires">

-   com.snc.pa
-   com.glideapp.report.customer\_service
-   com.sn\_customerservice
-   com.snc.pa.spotlight

</td></tr><tr id="plugin_com.snc.pa.customer_service" class="plugin_reference"><td class="name">

Performance Analytics - Content Pack - Customer Service\[com.snc.pa.customer\_service\]

</td><td class="description">

Provides Performance Analytics indicators and visualizations for Customer Service. Activation of this plugin on production instances may require a separate Performance Analytics license. Contact ServiceNow for details.

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

-   com.snc.pa
-   com.glideapp.report.customer\_service
-   com.sn\_customerservice
-   com.sn\_customerservice\_pa

</td></tr><tr><td>

Performance Analytics - Content Pack - Discovery\[com.snc.pa.discovery\]

</td><td>

Performance Analytics content pack for Discovery. Activation of this plugin on production instances may require a separate Performance Analytics license. Contact ServiceNow for details.

</td><td>

Inactive

</td><td>

false

</td><td class="requires">

-   com.snc.pa
-   com.snc.pa.cmdb
-   com.snc.discovery

</td></tr><tr id="plugin_com.snc.pa.em" class="plugin_reference"><td class="name">

Performance Analytics - Content Pack - Event Management\[com.snc.pa.em\]

</td><td class="description">

Performance Analytics content pack for Event Management core. Activation of this plugin on production instances may require a separate Performance Analytics license. Contact ServiceNow for details.

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

-   com.snc.pa
-   com.glideapp.itom.snac
-   com.glideapp.report.em

</td></tr><tr id="plugin_com.snc.work_management_pa" class="plugin_reference"><td class="name">

Performance Analytics - Content Pack - Field Service Management\[com.snc.work\_management\_pa\]

</td><td class="description">

Provides Performance Analytics content for Field Service Management. Activation of this plugin on production instances may require a separate license. Contact ServiceNow for details.

</td><td>

Inactive

</td><td class="has_demo_data">

true

</td><td class="requires">

-   com.snc.pa
-   com.snc.work\_management

</td></tr><tr id="plugin_com.snc.pa.fm" class="plugin_reference"><td class="name">

Performance Analytics - Content Pack - Financial Management\[com.snc.pa.fm\]

</td><td class="description">

Provides Performance Analytics indicators and visualizations for Financial Management. Activation of this plugin on production instances may require a separate Performance Analytics license. Contact ServiceNow for details.

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

-   com.snc.financial\_management
-   com.snc.pa

</td></tr><tr><td>

Performance Analytics - Content Pack - Financial Management for Customer Service\[com.snc.pa.fm.csm\]

</td><td>

Enables Performance Analytics dashboards for Financial Management associated with Customer Service Management.

 Activation of this plugin on production instances may require a separate Performance Analytics license. Contact ServiceNow for details.

</td><td>

Inactive

</td><td>

true

</td><td class="requires">

-   com.snc.financial\_management\_for\_csm
-   com.snc.pa

</td></tr><tr><td>

Performance Analytics - Content Pack - Financial Management for Field Service Management\[com.snc.pa.fm.fsm\]

</td><td>

Enables Performance Analytics dashboards for Financial Management associated with Field Service Management.

 Activation of this plugin on production instances may require a separate Performance Analytics license. Contact ServiceNow for details.

</td><td>

Inactive

</td><td>

false

</td><td class="requires">

-   com.snc.financial\_management\_for\_fsm
-   com.snc.pa

</td></tr><tr><td>

Performance Analytics - Content Pack - Financial Management for Financial Planning\[com.snc.pa.financial\_planning\]

</td><td>

Enables Performance analytics dashboards to associate to Financial Planning Process. Activation of this plugin on production instances may have licensing implications. Contact your ServiceNow account team for details.

</td><td>

Inactive

</td><td>

true

</td><td class="requires">

-   com.snc.financial\_planning
-   com.snc.pa

</td></tr><tr><td>

Performance Analytics - Content Pack - GRC: Audit Management\[com.sn\_audit\_pa\]

</td><td>

Provides Performance Analytics reports for the GRC Audit Management application. Activation of this plugin on production requires a PA Premium license. Contact ServiceNow for details.

</td><td>

Inactive

</td><td>

false

</td><td class="requires">

-   com.sn\_grc\_pa
-   com.sn\_audit

</td></tr><tr><td>

Performance Analytics - Content Pack - GRC: Policy and Compliance Management\[com.sn\_compliance\_pa\]

</td><td>

Provides Performance Analytics reports for the GRC Policy and Compliance Management application. Activation of this plugin on production requires a PA Premium license. Contact ServiceNow for details.

</td><td>

Inactive

</td><td>

false

</td><td class="requires">

-   com.sn\_grc\_pa
-   com.sn\_compliance

</td></tr><tr><td>

Performance Analytics - Content Pack - GRC: Risk Management\[com.sn\_risk\_pa\]

</td><td>

Provides Performance Analytics reports for the GRC Risk Management application. Activation of this plugin on production requires a PA Premium license. Contact ServiceNow for details.

</td><td>

Inactive

</td><td>

false

</td><td class="requires">

-   com.sn\_grc\_pa
-   com.sn\_risk

</td></tr><tr><td>

Performance Analytics - Content Pack - Human Resources Employee Document Management Scoped App\[com.sn\_hr\_employee\_files\_pa\]

</td><td>

Provides Performance Analytics reports and dashboards for Employee Document Management.

</td><td>

Inactive

</td><td>

false

</td><td class="requires">

-   com.sn\_employee\_document\_management
-   com.sn\_hr\_core

</td></tr><tr><td>

Performance Analytics - Content Pack -Vulnerability Response\[sn\_vul\_analytics\]

 \(Available in the ServiceNow Store\)

</td><td>

Provides an integration of Vulnerability Response with Performance Analytics for trend-based reporting. Activation of this plugin on production instances may require a separate license. Contact ServiceNow for details.

</td><td>

 

</td><td>

true

</td><td class="requires">

-   com.snc.pa
-   com.snc.treemap
-   sn\_vul

</td></tr><tr><td class="name">

Performance Analytics - Content Pack - Human Resources Lifecycle Events Scoped App\[com.sn\_hr\_lifecycle\_pa\]

</td><td class="description">

Enables you to define and track key performance indicators \(KPIs\) for Enterprise Onboarding and Transitions and show these in scorecards and dashboards. Activation of this plugin on production will require a PA Premium license. Contact ServiceNow for details.

</td><td class="active">

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

com.sn\_hr\_lifecycle\_events

</td></tr><tr><td>

Performance Analytics - Content Pack - Human Resources Scoped App\[com.sn\_hr\_pa\]

</td><td>

Enables you to define and track key performance indicators \(KPIs\) for HR and show these in scorecards and dashboards. Activation of this plugin on production will require a PA Premium license. Contact ServiceNow for details.

</td><td>

Inactive

</td><td>

true

</td><td>

com.sn\_hr\_core

</td></tr><tr id="plugin_com.snc.pa.sla" class="plugin_reference"><td class="name">

Performance Analytics - Content Pack - Incident SLA Management\[com.snc.pa.sla\]

</td><td class="description">

Performance Analytics content pack for Incident SLA Management. Activation of this plugin on production instances may require a separate Performance Analytics license. Contact ServiceNow for details.

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

com.snc.pa

</td></tr><tr><td>

Performance Analytics - Content Pack - ITSM Dashboards\[com.snc.pa.itsm\_dashboards\]

</td><td>

Performance Analytics content pack for ITSM Dashboards. Activation of this plugin on production instances may require a separate Performance Analytics license. Contact ServiceNow for details.

</td><td>

Inactive

</td><td>

false

</td><td class="requires">

-   com.snc.pa.change
-   com.snc.pa.problem
-   com.snc.pa.request
-   com.snc.pa.request2
-   com.snc.pa.knowledge
-   com.snc.pa.sla
-   com.snc.pa.spotlight.incident

</td></tr><tr id="plugin_com.snc.pa.knowledge" class="plugin_reference"><td class="name">

Performance Analytics - Content Pack - Knowledge Management\[com.snc.pa.knowledge\_v2\]

</td><td class="description">

Performance Analytics content pack for Knowledge Management. Activation of this plugin on production instances may require a separate Performance Analytics license. Contact ServiceNow for details.

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

-   com.snc.pa
-   com.snc.knowledge3
-   com.glideapp.report.knowledge.overview

</td></tr><tr><td>

Performance Analytics - Content Pack - Operational Intelligence\[com.snc.sa.metric.pa.content\]

</td><td>

Performance Analytics content pack for Analytics and Reporting Operational Intelligence Solution Dashboard and KPIs. Activation of this plugin on production instances may require a separate Performance Analytics license. Contact ServiceNow for details.

</td><td>

Inactive

</td><td>

false

</td><td class="requires">

-   com.snc.sa.metric
-   com.snc.pa
-   com.glideapp.canvas
-   com.snc.pa.em

</td></tr><tr id="plugin_com.snc.pa.problem" class="plugin_reference"><td class="name">

Performance Analytics - Content Pack - Problem Management\[com.snc.pa.problem\]

</td><td class="description">

Provides Performance Analytics indicators and visualizations for Problem Management. Activation of this plugin on production instances may require a separate Performance Analytics license. Contact ServiceNow for details.

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

-   com.snc.pa
-   com.glideapp.report.itsm.problem.overview

</td></tr><tr><td>

Performance Analytics Content Pack for Procurement Service Management\[com.sn\_spend\_pa\]

\(Starting with the Utah release, Performance Analytics Content Pack for Procurement Service Management is renamed as Performance Analytics for Sourcing and Procurement Operations.\)

\(Available in the ServiceNow Store\)

</td><td>

Provides a set of pre-configured metrics and dashboards to assess spend, operational efficiency, and team performance across the Sourcing and Procurement Operations product.

</td><td>

Inactive

</td><td>

false

</td><td>

-   com.snc.sn\_shop
-   com.snc.pa

</td></tr><tr id="plugin_com.snc.pa.ppm" class="plugin_reference"><td class="name">

Performance Analytics - Content Pack - PPM Standard Dashboards\[com.snc.pa.pmo\_dashboards\]

</td><td class="description">

Performance Analytics content pack for PPM Standard core. Activation of this plugin on production instances may require a separate Performance Analytics license. Contact ServiceNow for details.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

-   com.snc.pps\_dashboards
-   com.snc.financial\_planning\_pmo

</td></tr><tr><td>

Performance Analytics - Content Pack - PPM Standard\[com.snc.pps\_dashboards\]

</td><td>

Performance Analytics content pack for Project Portfolio Suite Dashboards core. Activation of this plugin on production instances may require a separate Performance Analytics license. Contact ServiceNow for details.

</td><td>

Inactive

</td><td>

false

</td><td class="requires">

-   com.snc.pa
-   com.snc.project\_portfolio\_suite

</td></tr><tr id="plugin_com.snc.pa.request" class="plugin_reference"><td class="name">

Performance Analytics - Content Pack - Request Management \(Requested Item\)\[com.snc.pa.request\]

</td><td class="description">

Performance Analytics content pack for Request Management for Requested Items. Installed with Performance Analytics - Premium. Activation of this plugin on production instances may require a separate Performance Analytics license. Contact ServiceNow for details.

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

com.snc.pa

</td></tr><tr id="plugin_com.snc.pa.request2" class="plugin_reference"><td class="name">

Performance Analytics - Content Pack - Request Management \(Requests\)\[com.snc.pa.request2\]

</td><td class="description">

Performance Analytics content pack for Request Management for Requests. Activation of this plugin on production instances may require a separate Performance Analytics license. Contact ServiceNow for details.

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

com.snc.pa

</td></tr><tr id="plugin_com.snc.pa.chat" class="plugin_reference"><td class="name">

Performance Analytics - Content Pack - Service Desk Chat\[com.snc.pa.chat\]

</td><td class="description">

Provides Performance Analytics indicators and visualizations for Service Desk Chat. Activation of this plugin on production instances may require a separate Performance Analytics license. Contact ServiceNow for details.

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

-   com.glide.connect
-   com.glide.connect.support
-   com.glide.connect.managers\_dashboard
-   com.snc.pa

</td></tr><tr><td>

Performance Analytics - Content Pack - Service Mapping\[com.snc.service-mapping.pa.content\]

</td><td>

Performance Analytics content pack for Service Mapping Dashboard and KPIs. Activation of this plugin on production instances may require a separate Performance Analytics license. Contact ServiceNow for details.

</td><td>

Inactive

</td><td>

false

</td><td class="requires">

-   com.snc.pa
-   com.snc.pa.cmdb

</td></tr><tr id="plugin_com.snc.pa.premium.all_content" class="plugin_reference"><td class="name">

Performance Analytics - Content Packs for ITSM\[com.snc.pa.premium.all\_content\]

</td><td class="description">

Installing this plugin installs content packs for Incident, Problem, Change, Incident SLA, Knowledge, and Requested Items for Performance Analytics.

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

-   com.snc.pa.change
-   com.snc.pa.problem
-   com.snc.pa.request
-   com.snc.pa.request2
-   com.snc.pa.knowledge
-   com.snc.pa.sla

</td></tr><tr><td>

Performance Analytics - Content Pack - Time Card Management\[com.snc.pa.time\_card\]

</td><td>

Performance Analytics content pack for Time card management. Activation of this plugin on production instances may require a separate Performance Analytics license. Contact ServiceNow for details.

</td><td>

Active

</td><td>

false

</td><td>

com.snc.pa

</td></tr><tr id="plugin_com.snc.pa.change.context_sensitive_analytics" class="plugin_reference"><td class="name">

Performance Analytics - Context Sensitive Analytics for Change Management\[com.snc.pa.change.context\_sensitive\_analytics\]

</td><td class="description">

Provides additional ability to open Performance Analytics context sensitive Performance Analytics dashboards in change request form based on UI actions.

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

-   com.snc.pa
-   com.snc.pa.change

</td></tr><tr id="plugin_com.snc.pa.chat.context_sensitive_analytics" class="plugin_reference"><td class="name">

Performance Analytics - Context Sensitive Analytics for Chat\[com.snc.pa.chat.context\_sensitive\_analytics\]

</td><td class="description">

Provides additional dashboard to analyze Connect Support metrics for support queues in Performance Analytics. Adds a related link to the Chat Queue Entry \[chat\_queue\_entry\] form to quickly display Performance Analytics metrics for the associated queue.

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

-   com.snc.pa
-   com.snc.pa.chat

</td></tr><tr id="plugin_com.snc.pa.cs.context_sensitive_analytics" class="plugin_reference"><td class="name">

Performance Analytics - Context Sensitive Analytics for Customer Service\[com.snc.pa.cs.context\_sensitive\_analytics\]

</td><td class="description">

Performance Analytics adding ability to open Performance Analytics context-sensitive dashboards in customer service form based on UI actions.

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

-   com.snc.pa
-   com.snc.pa.customer\_service
-   com.sn\_customerservice
-   com.snc.pa.customer\_service

</td></tr><tr id="plugin_com.snc.pa.incident.context_sensitive_analytics" class="plugin_reference"><td class="name">

Performance Analytics - Context Sensitive Analytics for Incident\[com.snc.pa.incident.context\_sensitive\_analytics\]

</td><td class="description">

Performance Analytics adding ability to open Performance Analytics context-sensitive dashboards in incident form based on UI actions.

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

com.snc.pa

</td></tr><tr id="plugin_com.snc.pa.problem.context_sensitive_analytics" class="plugin_reference"><td class="name">

Performance Analytics - Context Sensitive Analytics for Problem Management\[com.snc.pa.problem.context\_sensitive\_analytics\]

</td><td class="description">

Performance Analytics adding ability to open Performance Analytics context sensitive Performance Analytics dashboards in problem form based on UI actions.

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

-   com.snc.pa
-   com.snc.pa.problem

</td></tr><tr><td>

Performance Analytics - Diagnostics\[com.snc.pa.diagnostics\]

</td><td>

Enables users to run diagnostics on Performance Analytics records and related applications.

</td><td>

Active

</td><td>

false

</td><td>

com.snc.pa

</td></tr><tr><td>

Performance Analytics - Domain Support\[com.snc.pa.domain\_support\]

</td><td>

The Performance Analytics Domain Support plugin provides additional features to support scores collection on domain separated instances. This plugin requires the Domain Separation plugin to be installed.

</td><td>

Active

</td><td>

false

</td><td class="requires">

-   com.snc.pa.premium
-   com.glideapp.dashboards
-   com.glide.domain.msp\_extensions.installer

</td></tr><tr id="plugin_com.snc.pa.linkedin" class="plugin_reference"><td class="name">

Performance Analytics - Example - LinkedIn\[com.snc.pa.linkedin\]

</td><td class="description">

Automatically imports LinkedIn data historically and daily.

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

com.snc.pa

</td></tr><tr id="plugin_com.snc.pa.stock" class="plugin_reference"><td class="name">

Performance Analytics - Example - Stocks Quotes\[com.snc.pa.stock\]

</td><td class="description">

Automatically imports stock quotes data historically and daily.

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

com.snc.pa

</td></tr><tr id="plugin_com.snc.pa.twitter" class="plugin_reference"><td class="name">

Performance Analytics - Example - Twitter\[com.snc.pa.twitter\]

</td><td class="description">

Automatically import Twitter data historically and daily.

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

com.snc.pa

</td></tr><tr><td>

Performance Analytics - PA Solution Library\[com.snc.pa.solution.library\]

</td><td>

Allows you to upgrade the visuals of dashboards that are shipped in other content packs. Upgrade or duplicate whole dashboards or selected elements.

</td><td>

Active

</td><td>

false

</td><td>

com.snc.pa

</td></tr><tr><td>

Performance Analytics - Premium\[com.snc.pa.premium\]

</td><td>

Enables the functionality provided by the fully licensed version of Performance Analytics. Requires additional fee. Functionality includes the ability to:

 -   Create indicators, breakdowns, and other records
-   Create interactive filters and use interactive analysis
-   Create text analytics widgets
-   Use Performance Analytics with external data
-   Preserve scores beyond 180 days

</td><td>

Inactive

</td><td>

false

</td><td>

com.snc.pa

</td></tr><tr><td>

Performance Analytics - Scores Migration\[com.snc.pa.scores\_migration\]

</td><td>

Migrates scores from old tables to new tables. To provide optimal performance, the Scores \[pa\_scores\] table is being migrated to Scores Level 1 \[pa\_scores\_l1\] and Scores Level 2 \[pa\_scores\_l2\]. During migration you cannot collect, modify, or delete scores. Scheduled data collection and cleanup jobs will not run during migration.

</td><td>

Active

</td><td>

false

</td><td>

com.snc.pa

</td></tr><tr><td class="name">

Performance Analytics - Spotlight\[com.snc.pa.spotlight\]

</td><td class="description">

Enables records to be ranked by multiple weighted criteria. When a record surpasses a threshold of total weights, a Spotlight is created to highlight that record.

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

com.snc.pa

</td></tr><tr><td>

Performance Analytics - Spotlight - change spotlight content pack\[com.snc.pa.spotlight.change\]

</td><td>

Provides preconfigured Spotlight components and a dashboard to identify and prioritize Change records according to multiple weighted criteria. Requires fully licensed Performance Analytics.

</td><td>

Inactive

</td><td>

false

</td><td class="requires">

-   com.snc.pa.spotlight
-   com.snc.pa.change

</td></tr><tr><td class="name">

Performance Analytics - Spotlight - Incident Spotlight content pack\[com.snc.pa.spotlight.incident\]

</td><td class="description">

Provides preconfigured Spotlight components and a dashboard to identify and prioritize Incident records according to multiple weighted criteria.

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

-   com.snc.pa.spotlight
-   com.glideapp.canvas

</td></tr><tr><td>

Performance Analytics - Spotlight - Problem spotlight content pack\[com.snc.pa.spotlight.problem\]

</td><td>

Provides preconfigured Spotlight components and a dashboard to identify and prioritize Problem records according to multiple weighted criteria. Requires fully licensed Performance Analytics.

</td><td>

Inactive

</td><td>

false

</td><td class="requires">

-   com.snc.pa.spotlight
-   com.snc.pa.problem

</td></tr><tr><td>

Performance Analytics - Spotlight - Request spotlight content pack\[com.snc.pa.spotlight.request\]

</td><td>

Provides preconfigured Spotlight components and a dashboard to identify and prioritize Request records according to multiple weighted criteria. Requires fully licensed Performance Analytics.

</td><td>

Inactive

</td><td>

false

</td><td class="requires">

-   com.snc.pa.spotlight
-   com.snc.pa.request2

</td></tr><tr><td>

Performance Analytics and Reporting - Service Portal Widgets\[com.snc.pa.sp.widget\]

</td><td>

Support for Performance Analytics widgets in the Service Portal. A number of JavaScript and CSS libraries are included to be able to run Performance Analytics widgets independently in the Service Portal.

</td><td>

Active

</td><td>

false

</td><td>

com.glide.service-portal

</td></tr><tr><td>

Performance Analytics Content Pack for FSO\[sn\_bom\_pa\]

 \(Available in the ServiceNow Store\)

</td><td>

Provides Performance Analytic capabilities to Financial Services Operations applications.

</td><td>

Inactive

</td><td>

false

</td><td>

-   com.snc.pa
-   sn\_bom

</td></tr><tr><td>

Performance Analytics Content Pack for Major Incident Management\[com.snc.pa.incident.mim\]

</td><td>

Provides Performance Analytics indicators and visualizations for identifying and tracking major incidents. Extended functionality available with fully licensed Performance Analytics.

</td><td>

Inactive

</td><td>

false

</td><td>

com.snc.incident.mim

</td></tr><tr><td>

Performance Analytics Usage Overview\[com.snc.pa.usage.overview\]

</td><td>

This plugin contains dashboards, reports, and indicators to monitor Performance Analytics and Reporting usage.

</td><td>

Active

</td><td>

false

</td><td>

com.snc.pa

</td></tr><tr><td>

Performance Analytics Premium\[com.snc.pa.premium\]

</td><td>

Enables the functionality that you are entitled to with a subscription to Performance Analytics across all ServiceNow® products. Requires additional fee. Functionality includes the ability to: -   Create indicators, breakdowns, and other records
-   Create interactive filters and use interactive analysis
-   Create text analytics widgets
-   Use Performance Analytics with external data
-   Preserve scores beyond 180 days

</td><td>

Inactive

</td><td>

false

</td><td>

com.snc.pa

</td></tr><tr><td>

Performance Analytics and Reporting - Service Portal Widgets\[com.snc.pa.sp.widget\]

</td><td>

Support for Performance Analytics widgets in the Service Portal. A number of JavaScript and CSS libraries are included to be able to run Performance Analytics widgets independently in the Service Portal.

</td><td>

Inactive

</td><td>

false

</td><td>

com.glide.service-portal

</td></tr><tr><td>

Performance Analytics and Reporting for Universal Request\[com.snc.universal\_request.pa\]

</td><td>

Dashboards and reports for enhanced visibility on universal request metrics.

</td><td>

Active

</td><td>

false

</td><td>

com.snc.pa,com.snc.universal\_request.reporting

</td></tr><tr><td>

Performance Analytics Premium for APM\[com.snc.pa.premium.apm\]

</td><td>

Enables the Performance Analytics functionality that you are entitled to with a subscription that includes APM and Performance Analytics. Requires additional fee. Functionality includes the ability to: -   Create indicators, breakdowns, and other records
-   Create interactive filters and use interactive analysis
-   Create text analytics widgets
-   Use Performance Analytics with external data
-   Preserve scores beyond 180 days

</td><td>

Inactive

</td><td>

false

</td><td>

com.snc.pa

</td></tr><tr><td>

Performance Analytics Premium for Business Management\[com.snc.pa.premium.itbm\]

</td><td>

Enables the Performance Analytics functionality that you are entitled to with a subscription that includes Business Management and Performance Analytics. Requires additional fee. Functionality includes the ability to: -   Create indicators, breakdowns, and other records
-   Create interactive filters and use interactive analysis
-   Create text analytics widgets
-   Use Performance Analytics with external data
-   Preserve scores beyond 180 days

</td><td>

Inactive

</td><td>

false

</td><td>

com.snc.pa

</td></tr><tr><td>

Performance Analytics Premium for Cloud Control Center\[com.snc.pa.premium.ccc\]

</td><td>

Enables the Performance Analytics functionality that you are entitled to with a subscription that includes Cloud Control Center and Performance Analytics. Requires additional fee. Functionality includes the ability to: -   Create indicators, breakdowns, and other records
-   Create interactive filters and use interactive analysis
-   Create text analytics widgets
-   Use Performance Analytics with external data
-   Preserve scores beyond 180 days

</td><td>

Inactive

</td><td>

false

</td><td>

com.snc.pa

</td></tr><tr><td>

Performance Analytics Premium for Customer Service\[com.snc.pa.premium.cs\]

</td><td>

Enables the Performance Analytics functionality that you are entitled to with a subscription that includes Customer Service and Performance Analytics. Requires additional fee. Functionality includes the ability to: -   Create indicators, breakdowns, and other records
-   Create interactive filters and use interactive analysis
-   Create text analytics widgets
-   Use Performance Analytics with external data
-   Preserve scores beyond 180 days

</td><td>

Inactive

</td><td>

false

</td><td>

com.snc.pa

</td></tr><tr><td>

Performance Analytics Premium for Financial Management\[com.snc.pa.premium.fm\]

</td><td>

Enables the Performance Analytics functionality that you are entitled to with a subscription that includes Financial Management and Performance Analytics. Requires additional fee. Functionality includes the ability to: -   Create indicators, breakdowns, and other records
-   Create interactive filters and use interactive analysis
-   Create text analytics widgets
-   Use Performance Analytics with external data
-   Preserve scores beyond 180 days

</td><td>

Inactive

</td><td>

false

</td><td>

com.snc.pa

</td></tr><tr><td>

Performance Analytics Premium for Human Resource Management\[com.snc.pa.premium.hr\]

</td><td>

Enables the Performance Analytics functionality that you are entitled to with a subscription that includes Human Resource Management and Performance Analytics. Requires additional fee. Functionality includes the ability to: -   Create indicators, breakdowns, and other records
-   Create interactive filters and use interactive analysis
-   Create text analytics widgets
-   Use Performance Analytics with external data
-   Preserve scores beyond 180 days

</td><td>

Inactive

</td><td>

false

</td><td>

com.snc.pa

</td></tr><tr><td>

Performance Analytics Premium for IT Operations Management\[com.snc.pa.premium.itom\]

</td><td>

Enables the Performance Analytics functionality that you are entitled to with a subscription that includes ITOM and Performance Analytics. Requires additional fee. Functionality includes the ability to: -   Create indicators, breakdowns, and other records
-   Create interactive filters and use interactive analysis
-   Create text analytics widgets
-   Use Performance Analytics with external data
-   Preserve scores beyond 180 days

</td><td>

Inactive

</td><td>

false

</td><td>

com.snc.pa

</td></tr><tr><td>

Performance Analytics Premium for IT Operations Suite\[com.snc.pa.premium.itos\]

</td><td>

Enables the Performance Analytics functionality that you are entitled to with a subscription that includes IT Operations Suite and Performance Analytics. Requires additional fee. Functionality includes the ability to: -   Create indicators, breakdowns, and other records
-   Create interactive filters and use interactive analysis
-   Create text analytics widgets
-   Use Performance Analytics with external data
-   Preserve scores beyond 180 days

</td><td>

Inactive

</td><td>

false

</td><td>

com.snc.pa

</td></tr><tr><td>

Performance Analytics Premium for Project Portfolio Management\[com.snc.pa.premium.ppm\]

</td><td>

Enables the Performance Analytics functionality that you are entitled to with a subscription that includes PPM and Performance Analytics. Requires additional fee. Functionality includes the ability to: -   Create indicators, breakdowns, and other records
-   Create interactive filters and use interactive analysis
-   Create text analytics widgets
-   Use Performance Analytics with external data
-   Preserve scores beyond 180 days

</td><td>

Inactive

</td><td>

false

</td><td>

com.snc.pa

</td></tr><tr><td>

Performance Analytics Premium for Security Incident Response\[com.snc.pa.premium.sir\]

</td><td>

Enables the Performance Analytics functionality that you are entitled to with a subscription that includes SIR and Performance Analytics. Requires additional fee. Functionality includes the ability to: -   Create indicators, breakdowns, and other records
-   Create interactive filters and use interactive analysis
-   Create text analytics widgets
-   Use Performance Analytics with external data
-   Preserve scores beyond 180 days

</td><td>

Inactive

</td><td>

false

</td><td>

com.snc.pa

</td></tr><tr><td>

Performance Analytics Premium for Security Operations\[com.snc.pa.premium.sir\]

</td><td>

Enables the Performance Analytics functionality that you are entitled to with a subscription that includes Security Operations and Performance Analytics. Requires additional fee. Functionality includes the ability to: -   Create indicators, breakdowns, and other records
-   Create interactive filters and use interactive analysis
-   Create text analytics widgets
-   Use Performance Analytics with external data
-   Preserve scores beyond 180 days

</td><td>

Active

</td><td>

false

</td><td>

com.snc.pa

</td></tr><tr><td>

Performance Analytics Premium for Service Management\[com.snc.pa.premium.service\_management\]

</td><td>

Enables the Performance Analytics functionality that you are entitled to with a subscription that includes Service Management and Performance Analytics. Requires additional fee. Functionality includes the ability to: -   Create indicators, breakdowns, and other records
-   Create interactive filters and use interactive analysis
-   Create text analytics widgets
-   Use Performance Analytics with external data
-   Preserve scores beyond 180 days

</td><td>

Inactive

</td><td>

false

</td><td>

com.snc.pa

</td></tr><tr><td>

Performance Analytics Premium for Software Asset Management\[com.snc.pa.premium.sam\]

</td><td>

Enables the Performance Analytics functionality that you are entitled to with a subscription that includes Software Asset Management and Performance Analytics. Requires additional fee. Functionality includes the ability to: -   Create indicators, breakdowns, and other records
-   Create interactive filters and use interactive analysis
-   Create text analytics widgets
-   Use Performance Analytics with external data
-   Preserve scores beyond 180 days

</td><td>

Inactive

</td><td>

false

</td><td>

com.snc.pa

</td></tr><tr><td>

Performance Dashboards\[com.glide.performance\_dashboards\]

</td><td>

Performance Dashboards

</td><td>

Active

</td><td>

false

</td><td>

com.glide.cms

</td></tr><tr><td>

Performance Metrics for VTB\[com.glide.ui.vtb\_metrics\]

</td><td>

Provides profiler page for benchmarking Java methods in Visual Task Board.

</td><td>

Inactive

</td><td>

false

</td><td>

com.glide.ui.vtb

</td></tr><tr><td>

Personal Lines Servicing\[com.sn\_ins\_policy\_b2c\]

</td><td>

Enables insurance carriers to be agile and customer-centric in resolving mid-term policy changes and requests. Insurance carriers can prioritize underwriting cases by premium value with intelligent business rules and eliminate low-value manual work from underwriting queues.

</td><td>

 

</td><td>

Yes

</td><td>

-   com.sn\_csm\_playbook
-   com.snc.csm\_contributor\_user
-   com.sn\_bom
-   com.sn\_bom\_document
-   com.sn\_ins\_underwrite

</td></tr><tr><td>

Personal Lines Underwriting\[com.sn\_ins\_underwrite\]

</td><td>

Enables insurance carriers to route complex severing requests instantly to underwriters based on their existing underwriting guidelines and rules. Underwriters can collaborate with distribution and servicing teams though an efficient and transparent workflow.

</td><td>

 

</td><td>

No

</td><td>

-   com.snc.csm\_contributor\_user
-   com.sn\_bom

</td></tr><tr><td>

Planned Maintenance Management\[com.snc.fsm\_pm\]

 \(Available in the ServiceNow Store\)

</td><td>

Manages the regular preventive maintenance of assets.

</td><td>

Active

</td><td>

true

</td><td>

Field Service Management \(com.snc.work\_management\)

</td></tr><tr><td>

Planned Work Management \[com.snc.fsm\_planned\_work\_management\]

 \(Available in the ServiceNow Store\)

</td><td>

Enables organizations to create and manage the planned activities for assets that are scheduled to be executed periodically.

</td><td>

Active

</td><td>

true

</td><td>

-   com.snc.fsm\_template\_management
-   com.snc.planned\_maintenance

</td></tr><tr id="plugin_com.snc.paas" class="plugin_reference"><td class="name">

Platform as a Service\[com.snc.paas\]

</td><td class="description">

Allows the development of custom applications to meet business needs.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

com.glideapp.workflow

</td></tr><tr><td>

Playbooks for Customer Service Management\[com.sn\_csm\_playbook\]

</td><td>

Playbooks for Customer Service Management guides customer service agents through the various tasks and their sequence to resolve customer issues and visualizes the entire lifecycle ​across diverse and siloed processes​.

</td><td>

Active

</td><td>

false

</td><td class="requires">

-   com.glide.pad.core
-   com.glide.playbook\_experience.config
-   com.sn\_customerservice

</td></tr><tr><td>

Portal Next Experience Theme\[sn\_sppolaris\_theme\]

 \(Available in the ServiceNow Store\)

</td><td>

Allows the Next Experience theme to be used with the Customer Support \(csm\), Customer Service \(csp\), and Knowledge \(kb\) portals.

</td><td>

Inactive

</td><td>

false

</td><td>

com.glide.service-portal

</td></tr><tr><td>

Portfolio Management\[com.snc.portfolio\_management\]

</td><td>

The Portfolio Management plugin.

</td><td>

Inactive

</td><td>

false

</td><td>

 

</td></tr><tr><td>

PPM Mobile\[com.sn\_ppm.mobile\]

</td><td>

This plugin provides Project Portfolio Suite Mobile user experience. This provides access to project status and project status report in the agent mobile application. PPM Standard is required. But if it is not active, installing PPM Mobile also activates PPM Standard plugin.

</td><td>

Active

</td><td>

false

</td><td>

com.snc.financial\_planning\_pmo

</td></tr><tr><td>

PPM Ridac\[com.snc.ppm\_ridac\]

</td><td>

The PPM RIDAC flow actions plugin. Installs the flow actions needed for RIDAC conversions.

</td><td>

Active

</td><td>

false

</td><td>

 

</td></tr><tr><td>

PPM Standard Multicurrency\[com.snc.ppm\_multicurrency\]

</td><td>

Enable advanced ability to manage PPM financials in multiple currencies.

</td><td>

Inactive

</td><td>

true

</td><td class="requires">

-   com.snc.financial\_planning\_pmo
-   com.glide.currency2

</td></tr><tr><td>

Predictive Intelligence\[com.glide.platform\_ml\]

</td><td>

This is the new name for the Agent Intelligence plugin, effective in the New York release and beyond. Predictive Intelligence enables the creation of machine learning solutions using data in your instance. The plugin provides various capabilities and solution types for training the system to predict, recommend, and drive data outcomes.

</td><td>

Active

</td><td>

false

</td><td>

com.glide.platform\_ml\_pa

</td></tr><tr><td>

Predictive Intelligence - Enhanced UI\[com.snc.ml\_ui\]

</td><td>

This plugin enhances the UI for Predictive Intelligence.

</td><td>

Active

</td><td>

false

</td><td>

 

</td></tr><tr><td>

Predictive Intelligence for Contextual Search\[com.snc.contextual\_search\_ml\]

</td><td>

Enables customers to leverage machine-learning algorithms for searching with Contextual Search. For example: Similar Open Incidents.

 Activation of this plugin on production instances may require a separate license. Contact ServiceNow for details.

</td><td>

Inactive

</td><td>

false

</td><td class="requires">

-   com.snc.contextual\_search
-   com.glide.platform\_ml

</td></tr><tr><td>

Predictive Intelligence for Customer Service Management\[com.snc.csm\_ml\]

</td><td class="description">

Enables customers to leverage machine learning algorithms for searching related cases in Customer Service Management. Activation of this plugin on production instances may require a separate license. Contact ServiceNow for details.

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

-   com.sn\_customerservice
-   com.snc.contextual\_search\_ml
-   com.snc.adv\_cxs\_results\_email\_script

</td></tr><tr><td>

Predictive intelligence for CSM - Task intelligence\[com\_snc\_csm\_ml\_task\]

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Predictive Intelligence for Field Service Management\[com.snc.fsm\_ml\]

</td><td>

Provides various capabilities driven by machine-learning solutions. Activation of this plugin on production instances may require a separate license. Contact ServiceNow for details.

</td><td>

Active

</td><td>

true

</td><td>

-   com.snc.work\_management
-   com.snc.contextual\_search\_ml

</td></tr><tr><td class="name">

Predictive Intelligence for Incident\[com.snc.incident.ml\]

</td><td class="description">

Enables customers to leverage machine-learning algorithms with application logic for predicting Open change request and Open Problem for Incident. Activation of this plugin on production instances may require a separate license. Contact ServiceNow for details.

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td>

com.snc.contextual\_search\_ml

</td></tr><tr><td>

Predictive Intelligence for Incident Management\[com.snc.incident.ml\_solution\]

</td><td>

Predictive Intelligence for Incident Management provides solution definitions as templates so that you can build models without writing any code.

</td><td>

Inactive for new customers. Active for existing ITSM Pro customers.

</td><td>

false

</td><td>

NA

</td></tr><tr><td>

Predictive Intelligence for Major Incident Management\[com.snc.incident.mim.ml\_solution\]

</td><td>

Predictive Intelligence for Major Incident Management provides solution definitions as templates so that you can build models without writing any code.

</td><td>

Inactive for new customers. Active for existing ITSM Pro customers.

</td><td>

false

</td><td>

-   com.snc.incident.mim
-   com.snc.incident.ml\_solution

</td></tr><tr><td>

Predictive Intelligence for Knowledge Management\[com.snc.knowledge\_ml\]

</td><td>

 

</td><td>

Inactive

</td><td>

false

</td><td class="has_demo_data">

com.snc.contextual\_search\_ml

</td></tr><tr><td>

Predictive Intelligence for PPM\[com.snc.ppm\_ml\]

 \(Available in the ServiceNow Store\)

</td><td>

The Predictive Intelligence for Project Management capability uses machine-learning algorithms to search and display similar projects and demands.

</td><td>

Active

</td><td>

false

</td><td class="requires">

-   com.snc.contextual\_search\_ml
-   com.snc.financial\_planning\_pmo

</td></tr><tr><td>

Predictive Intelligence for Universal Request\[com.snc.universal\_request.ml\]

</td><td>

Contains the machine learning solutions for the Universal Request use cases.

</td><td>

Active

</td><td>

false

</td><td>

-   com.snc.universal\_request
-   com.glide.platform\_ml

</td></tr><tr><td>

Predictive Intelligence Incident Estimated Time to Resolve\[com.snc.incident.ml.ettr\]

</td><td>

Enables customers to leverage machine-learning algorithms with application logic for predicting the estimated time to resolve for an Incident. Activation of this plugin on production instances may require a separate license. Contact ServiceNow for details.**Important:** It is not recommended for customers to activate this plugin directly. To activate this plugin, follow the instructions given in KB0821555.

</td><td>

Inactive

</td><td>

false

</td><td>

-   com.glide.platform\_ml
-   com.sn\_itsm\_ettr\_card

</td></tr><tr><td>

Predictive Intelligence Workbench HRSD Content\[com.sn\_piwb\_hrsd\_content\]

</td><td>

Enables customers to seed HRSD specific content to provide implementation guidance for use cases created through Predictive Intelligence Workbench.

</td><td>

Active

</td><td>

false

</td><td class="requires">

-   com.sn\_hr\_core
-   com.glide.platform\_ml

</td></tr><tr><td>

Predictive Intelligence Reports\[com.glide.platform\_ml\_pa\]

</td><td>

This is the new name for the Agent Intelligence Reports plugin.

</td><td>

Active

</td><td>

false

</td><td>

 

</td></tr><tr><td>

Predictive Intelligence Workbench\[com.sn\_piwb\_ml\]

</td><td>

Predictive Intelligence Workbench core plugin provides a common framework for creating use case templates, managing use cases and dashboard to communicate value across all SN apps

</td><td>

Active

</td><td>

false

</td><td class="requires">

-   com.glide.platform\_ml
-   com.glide.platform\_ml\_pa

</td></tr><tr><td class="name">

Pre-Visit Management\[sn\_previsit\]

 \(Available in the ServiceNow Store\)

</td><td class="description">

Streamlines the scheduling process of procedure requests for patients and increase visibility to pre-authorization approvals prior to scheduled procedures.

</td><td>

Inactive

</td><td class="has_demo_data">

true

</td><td class="requires">

-   com.snc.business\_location
-   com.snc.csm\_case\_types
-   com.snc.household
-   com.snc.install\_base
-   com.glide.encryption
-   com.sn\_external\_user\_register
-   com.snc.pdf\_generator
-   com.snc.signaturepad
-   com.glideapp.user\_criteria.scoped.api
-   sn\_hcls
-   sn\_csm\_playbook
-   com.sn\_ind
-   sn\_doc
-   sn\_prd\_pm
-   sn\_ciwf\_ui\_cmpnt

</td></tr><tr><td>

Proactive Customer Service Operations\[com.snc.proactive\_cs\_ops\]

</td><td>

Enables customers to create cases proactively from alerts either manually or through automation and track the accounts and the corresponding install base items affected by the alert.

</td><td>

Active

</td><td>

false

</td><td class="requires">

-   com.sn\_majorissue\_mgt
-   com.snc.install\_base
-   com.glideapp.itom.snac
-   com.sn\_cs\_sm\_request
-   com.snc.csm\_action\_status

</td></tr><tr><td>

Proactive Customer Service Operations with Event Management\[com.snc.proactive\_cs\_itom\]

</td><td>

Provides an integration between Customer Service Management and ITOM Event Management. Enables customers to create cases proactively from alerts either manually or through automation and track the accounts and the corresponding install base items affected by the alert.

</td><td>

Inactive

</td><td>

false

</td><td class="requires">

-   com.snc.proactive\_cs\_ops
-   com.glideapp.itom.snac

</td></tr><tr><td>

Proactive Prompts\[com.sn\_pp\]

 \(Available in the ServiceNow Store\)

</td><td>

Enables contextual and proactive engagement for managers and employees by bringing actionable insights as prompts into their flow of work.

</td><td>

Active

</td><td>

true

</td><td>

com.glide.cs.chatbot

</td></tr><tr id="plugin_com.snc.problem" class="plugin_reference"><td class="name">

Problem Management\[com.snc.problem\]

</td><td class="description">

Helps to identify the cause of a service interruption reported by a significant or recurring incidents.

</td><td>

Active

</td><td class="has_demo_data">

true

</td><td class="requires">

-   com.snc.service
-   com.glideapp.report.itsm.problem.overview

</td></tr><tr><td class="name">

Problem Management — ATF Tests\[com.snc.problem.atf\]

</td><td>

Delivers ATF tests for Problem Management.

</td><td>

Active

</td><td>

true

</td><td>

 

</td></tr><tr id="plugin_com.glideapp.report.itsm.problem.overview" class="plugin_reference"><td class="name">

Problem Overview Homepage\[com.glideapp.report.itsm.problem.overview\]

</td><td class="description">

Displays Problem overview homepage.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

com.glideapp.report

</td></tr><tr><td>

Problem Management Best Practice - Madrid\[com.snc.best\_practice.problem.madrid\]

</td><td class="description">

Helps to identify the cause of a service interruption reported by a significant or recurring incidents. Provides roles for problem management including a problem coordinator, problem manager and problem administrator. Provides fields to record the category, where the issue was first reported, the workaround, the cause notes and the fix notes. Searches for and attaches knowledge articles. Communicates when a workaround or fix is available.

</td><td>

Active

</td><td class="has demo data">

true

</td><td class="requires">

-   com.snc.problem
-   com.snc.problem\_task

</td></tr><tr><td>

Problem Management Best Practice - Madrid - Knowledge Integration\[com.snc.best\_practice.problem.madrid.knowledge\]

</td><td class="description">

Helps to identify the cause of a service interruption reported by a significant or recurring incidents. Create Known Error articles for Incident Deflection \(requires Knowledge Management Advanced plugin to be activated\).

</td><td>

Active

</td><td class="has demo data">

true

</td><td class="requires">

-   Problem Management Best Practice - Madrid \(com.snc.best\_practice.problem.madrid\)
-   Knowledge Management Advanced Installer \(com.snc.knowledge\_advanced.installer\)

</td></tr><tr><td>

Problem Management Best Practice - Madrid - State Model\[com.snc.best\_practice.problem.madrid.state\_model\]

</td><td class="description">

Provides support for state management to control how a problem or problem task is allowed to transition through a predefined list of states.

</td><td>

Inactive

</td><td class="has demo data">

true

</td><td class="requires">

Problem Management Best Practice - Madrid \(com.snc.best\_practice.problem.madrid\)

</td></tr><tr><td>

Problem Overview Dashboard\[com.snc.pa.problem.dashboards\]

</td><td>

Displays Problem Overview Dashboard.

</td><td>

Active

</td><td>

false

</td><td>

com.snc.problem

</td></tr><tr id="plugin_com.snc.problem_task" class="plugin_reference"><td class="name">

Problem Tasks\[com.snc.problem\_task\]

</td><td class="description">

Adds a Problem Task table with a reference to the Problem table.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

 

</td></tr><tr><td>

Process Automation Designer for ITSM\[com.snc.itsm.playbook\]

</td><td>

Process Automation Designer enables business process owners to consolidate multiple flows across the enterprise into a single unified process. Process owners can create and manage cross-functional automated processes to provide end-users with a simplified, task-oriented interface to guide them through these processes, such as playbooks in Agent Workspace.Process Automation Designer for ITSM enables process owners to create and manage the cross-functional IT process flows.

</td><td>

Active

</td><td>

false

</td><td class="requires">

-   com.glide.pad.core
-   com.playbook\_experience
-   com.snc.incident

</td></tr><tr id="plugin_com.snc.process_flow_formatter" class="plugin_reference"><td class="name">

Process Flow Formatter\[com.snc.process\_flow\_formatter\]

</td><td class="description">

Quickly summarizes multiple pieces of information about a process and displays the stages graphically at the top of a form.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

 

</td></tr><tr><td>

Process Optimization\[com.sn\_process\_optimization\]

</td><td>

Creates business process flows from the data in audit trails. This allows in-depth analysis of business processes to improve outcomes.

</td><td>

Active

</td><td>

false

</td><td class="requires">

-   com.agent\_workspace
-   com.workspace\_core
-   com.devsnc\_sn\_promin\_workbench

</td></tr><tr><td>

Process Optimization Content Pack for CSM\[com.snc.csm\_process\_optimization\]

</td><td>

Provides pre-configured process optimization models and improvement initiatives for the CSM Processes.

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

-   com.sn\_customerservice
-   com.sn\_process\_optimization

</td></tr><tr><td>

Process Optimization Content Pack for FSM\[com.snc.fsm\_process\_optimization\]

 \(Available in the ServiceNow Store\)

</td><td>

Creates business process flows from the work order task data in audit trails, allowing process owners to perform in-depth analysis and discover process insights to improve business outcomes.

</td><td>

Active

</td><td>

true

</td><td>

-   sn\_po \(v23.0.22\)
-   com.snc.work\_management

</td></tr><tr><td>

Process Optimization for external data\[com.sn\_po\_extdata\]

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Process Optimization Workspace\[com.sn\_po\_workspace\]

</td><td>

Delivers the Process Optimization workspace feature for analyst users.

</td><td>

Inactive

</td><td>

false

</td><td>

-   com.agent\_workspace
-   com.sn\_process\_optimization
-   com.sn\_po\_workspace\_components

</td></tr><tr id="plugin_com.snc.procurement" class="plugin_reference"><td class="name">

Procurement\[com.snc.procurement\]

</td><td class="description">

Allows users to create purchase orders and obtain items for fulfilling service catalog requests.

</td><td>

Inactive

</td><td class="has_demo_data">

true

</td><td class="requires">

 

</td></tr><tr><td>

Procurement Case Management\[com.sn\_spend\_psd\]

\(Available in the ServiceNow Store\)

</td><td>

Enables all employees to request services from the procurement team, and allows the procurement team to manage those requests.

</td><td>

Inactive

</td><td>

true

</td><td>

-   com.sn\_spend\_sdc
-   com.sn\_spend\_workspace

</td></tr><tr><td>

Procurement File Transfer Framework\[com.sn\_spend\_ftp\_intg\]

\(Available in the ServiceNow Store\)

</td><td>

Extends the Procurement Integration Framework with SFTP and FTP functionality, designed for integrating with systems that do not support REST or SOAP-based integration methods.

</td><td>

Inactive

</td><td>

false

</td><td>

-   com.sn\_spend\_intg
-   com.glide.hub.action\_step.ssh
-   com.glide.hub.action\_step.sftp
-   com.glide.hub.flow\_trigger.rest

</td></tr><tr><td>

Procurement Integration Framework\[com.sn\_spend\_intg\]

\(Available in the ServiceNow Store\)

</td><td>

Provides a set of staging tables, transform maps, and workflows to integrate sourcing, third-party catalogs, ordering, shipments, and invoicing with Sourcing and Procurement Operations.

</td><td>

Inactive

</td><td>

false

</td><td>

-   com.glide.explicit\_roles
-   com.sn\_pr

</td></tr><tr><td>

Procurement Service Management NLU Model\[com.sn\_spend\_nlu\]

\(Starting with the Utah release, Procurement Service Management NLU Model is renamed as Natural Language Understanding Models for Sourcing and Procurement Operations.\)

\(Available in the ServiceNow Store\)

</td><td>

Provides Natural Language Understanding \(NLU\) models to enhance the virtual agent conversation interface, using natural human utterances to detect the correct conversations intended by employees.

</td><td>

Inactive

</td><td>

false

</td><td>

-   com.glide.cs.chatbot
-   com.sn\_shop\_va

</td></tr><tr><td>

Procurement with Project Management\[com.sn\_spend\_ppm\]

\(Starting with the Utah release, Procurement with Project Management is renamed as Project Costing for Sourcing and Procurement Operations.\)

\(Available in the ServiceNow Store\)

</td><td>

Provides a set of capabilities to automate the calculation of planned versus actual cost by linking purchase orders to cost plans within Project Portfolio Management.

</td><td>

Inactive

</td><td>

false

</td><td>

-   com.snc.sn\_pr
-   com.snc.financial\_planning\_pmo

</td></tr><tr id="plugin_com.snc.product_catalog" class="plugin_reference"><td class="name">

Product Catalog\[com.snc.product\_catalog\]

</td><td class="description">

Provides information about individual models. Models are specific versions or various configurations of an asset. Models published to the product catalog are automatically published to the service catalog.

</td><td>

Active

</td><td class="has_demo_data">

true

</td><td class="requires">

 

</td></tr><tr><td>

Product Catalog Advanced\[com.sn\_prd\_pm\_adv\]

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Product Inventory Advanced\[com.sn\_prd\_invt\]

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Program Common\[com.snc.program\_common\]

</td><td>

The Program Common plugin aids in planning, organizing, and managing programs with basic features.

</td><td>

Active

</td><td>

false

</td><td class="requires">

-   com.snc.planned\_task\_v2
-   com.snc.itbm\_security

</td></tr><tr><td>

Profanity filter for agent chat\[com.sn.va.profanity\]

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr id="plugin_com.snc.project_management_v3" class="plugin_reference"><td class="name">

Project Management\[com.snc.project\_management\_v3\]

</td><td class="description">

The Project Management application aids in planning, organizing and managing projects and resources in order to setup, execute, and complete a project faster and easier. Only upgrade is allowed for this plugin. Activation should be done through PPM Standard plugin.

</td><td>

Inactive

</td><td class="has_demo_data">

true

</td><td class="requires">

-   com.snc.project\_management\_delete
-   com.glide.schedules
-   com.snc.planned\_task\_v2
-   com.snc.time\_card
-   com.snc.skills\_management
-   com.snc.process\_flow\_formatter
-   com.snc.cost\_management
-   com.snc.project\_management\_db\_views
-   com.snc.project\_workbench
-   com.snc.timeline\_visualization
-   com.glide.ui.checklist

</td></tr><tr id="plugin_com.snc.ppm_teamspace_1" class="plugin_reference"><td class="name">

Project Management TeamSpace 1\[com.snc.ppm\_teamspace\_1\]

</td><td class="description">

Installs a Project TeamSpace so that each team or each department like Marketing, Finance, IT-Team1, IT-Team2 can implement PPM suitable to their needs without overstepping each other.

</td><td>

Inactive

</td><td class="has_demo_data">

true

</td><td class="requires">

com.snc.financial\_planning\_pmo

</td></tr><tr id="plugin_com.snc.ppm_teamspace_2" class="plugin_reference"><td class="name">

Project Management TeamSpace 2\[com.snc.ppm\_teamspace\_2\]

</td><td class="description">

Installs a Project TeamSpace so that each team or each department like Marketing, Finance, IT-Team1, IT-Team2 can implement PPM suitable to their needs without overstepping each other.

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

com.snc.financial\_planning\_pmo

</td></tr><tr id="plugin_com.snc.ppm_teamspace_3" class="plugin_reference"><td class="name">

Project Management TeamSpace 3\[com.snc.ppm\_teamspace\_3\]

</td><td class="description">

Installs a Project TeamSpace so that each team or each department like Marketing, Finance, IT-Team1, IT-Team2 can implement PPM suitable to their needs without overstepping each other.

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

com.snc.financial\_planning\_pmo

</td></tr><tr id="plugin_com.snc.ppm_teamspace_4" class="plugin_reference"><td class="name">

Project Management TeamSpace 4\[com.snc.ppm\_teamspace\_4\]

</td><td class="description">

Installs a Project TeamSpace so that each team or each department like Marketing, Finance, IT-Team1, IT-Team2 can implement PPM suitable to their needs without overstepping each other.

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

com.snc.financial\_planning\_pmo

</td></tr><tr id="plugin_com.snc.ppm_teamspace_5" class="plugin_reference"><td class="name">

Project Management TeamSpace 5\[com.snc.ppm\_teamspace\_5\]

</td><td class="description">

Installs a Project TeamSpace so that each team or each department like Marketing, Finance, IT-Team1, IT-Team2 can implement PPM suitable to their needs without overstepping each other.

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

com.snc.financial\_planning\_pmo

</td></tr><tr id="plugin_com.snc.project_portfolio_suite" class="plugin_reference"><td class="name">

Project Portfolio Suite\[com.snc.project\_portfolio\_suite\]

</td><td class="description">

The Project Portfolio Suite \(PPS\) plugin activates an integrated set of applications for project portfolio management and IT software development. Only upgrade is allowed for this plugin. Activation should be done through PPM Standard plugin.

</td><td>

Inactive

</td><td class="has_demo_data">

true

</td><td class="requires">

-   com.snc.project\_management\_v3
-   com.snc.demand\_management
-   com.snc.resource\_management
-   com.snc.test\_mgmt
-   com.snc.sdlc.scrum.ppm\_int
-   com.snc.test\_mgmt.ppm\_int
-   com.snc.program\_management

</td></tr><tr><td>

Project workspace\[com.snc.project\_workspace\]

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr id="plugin_com.snc.financial_planning_pmo" class="plugin_reference"><td class="name">

PPM Standard\[com.snc.financial\_planning\_pmo\]

</td><td class="description">

Enables you to manage your demands, resources, portfolios and projects, and gives full visibility from idea to execution. It also helps you plan, track, and manage cost and budget on projects and demands in a portfolio to strike a balance between investment and returns. Agile management and test management help you to improve productivity and service delivery.

</td><td>

Inactive

</td><td class="has_demo_data">

true

</td><td class="requires">

-   com.snc.project\_portfolio\_suite
-   com.snc.financial\_planning
-   com.snc.rate\_model

</td></tr><tr><td>

PPM Standard - ATF Tests\[com.snc.financial\_planning\_pmo.atf\]

</td><td>

ATF tests for PPM Standard

</td><td>

Active

</td><td>

false

</td><td>

 

</td></tr><tr id="plugin_com.glide.protocol_profile" class="plugin_reference"><td class="name">

Protocol Profile Manager\[com.glide.protocol\_profile\]

</td><td class="description">

Defines properties associated to protocols such as default port and keystore.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

 

</td></tr><tr><td>

Proxy Agent for connecting to Natural Language Understanding providers\[com.glide.nlu.proxy\]

</td><td>

The base NLU proxy agent for connecting to NLU providers. Intended for use by Virtual Agent and other clients.

</td><td>

Active

</td><td>

true

</td><td>

 

</td></tr><tr><td>

Proxy Agent to the IBM Watson Natural Language Understanding server\[com.glide.nlu.ibmwatson.intent.discovery\]

</td><td>

Activates the IBM Watson Assistant Intent and Entity integration, which enables Virtual Agent to use intents, entities, and utterances defined in IBM Watson Assistant.

</td><td>

Inactive

</td><td>

false

</td><td>

com.glide.nlu.proxy

</td></tr><tr><td>

Proxy Agent to the Microsoft LUIS Natural Language Understanding server\[com.glide.nlu.msluis.intent.discovery\]

</td><td>

Proxy agent to the Microsoft LUIS Natural Language Understanding server.

</td><td>

Inactive

</td><td>

false

</td><td>

com.glide.nlu.intent.discovery

</td></tr><tr><td>

Proxy Agent to the ServiceNow Natural Language Understanding server\[com.glide.nlu.intent.discovery\]

</td><td>

Proxy agent for connecting to ServiceNow's NLU server for NLU intent discovery. Intended for use by Virtual Agent and other clients.

</td><td>

Active

</td><td>

false

</td><td>

com.glide.nlu.proxy

</td></tr><tr><td>

Purchase and Receipt Automation\[com.snc.sn\_pr\]

\(Starting with the Tokyo release, Purchase and Receipt Automation is renamed as Sourcing and Purchasing Automation.\)

\(Available in the ServiceNow Store\)

</td><td>

Provides workflows and automation for sourcing requests, negotiations, and purchase requisitions.

</td><td>

Inactive

</td><td>

true

</td><td>

-   com.glide.graphql
-   com.glideapp.user\_criteria.scoped.api
-   sn\_shop
-   sn\_spend\_sdc
-   sn\_spend\_psd
-   sn\_spend\_workspace

</td></tr><tr><td>

Purchase Automation Integration with Risk Assessment\[com.sn\_spend\_vrm\]

\(Starting with the Utah release, Purchase Automation Integration with Risk Assessment is renamed as Risk Assessments Integration for Sourcing and Procurement Operations.\)

\(Available in the ServiceNow Store\)

</td><td>

Provides a set of capabilities to trigger risk assessments on a supplier during the sourcing or purchase requisition workflow using Vendor Risk Management.

</td><td>

Inactive

</td><td>

true

</td><td>

-   com.snc.sn\_pr
-   com.sn\_vdr\_risk\_asmt

</td></tr><tr><td>

Purchase Modification Experience Pack for Procurement Case Management\[com.sn\_spend\_cp\]

\(Starting with the Utah release, Purchase Modification Experience Pack for Procurement Case Management is renamed as Playbooks for Sourcing and Procurement Operations.\)

\(Available in the ServiceNow Store\)

</td><td>

Provides a set of pre-built playbooks, workflows, and experiences for employees, sourcing, and procurement to automate work that is typically managed through emails and spreadsheets.

</td><td>

Inactive

</td><td>

false

</td><td>

-   com.snc.sn\_shop
-   com.snc.sn\_pr

</td></tr><tr id="plugin_com.glide.push.feedback" class="plugin_reference"><td class="name">

Push Feedback\[com.glide.push.feedback\]

</td><td class="description">

Collects feedback from the Apple push notification service or another feedback service. Provides a REST API for other instances to collect from this service.

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

com.glide.push

</td></tr><tr id="plugin_com.glide.push" class="plugin_reference"><td class="name">

Push Notification\[com.glide.push\]

</td><td class="description">

Defines push notification message enqueuing and sending Responsible for processing push notifications to their next destination.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

 

</td></tr><tr><td class="name">

Push Retention\[com.glide.push\_retention\]

</td><td class="description">

Provides retention policy for push notifications.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

-   com.glide.push
-   com.glide.auxdb

</td></tr><tr id="plugin_com.snc.vulnerability.qualys" class="plugin_reference"><td class="name">

Qualys Vulnerability Integration\[snc\_vul\_qualys\]

 \(Available in the ServiceNow Store\)

</td><td class="description">

Provides the ability to integrate the ServiceNow Vulnerability Response application with the Qualys vulnerability scanner. Activation of this plugin on production instances may require a separate license. Contact ServiceNow for details.

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

snc\_vul

</td></tr><tr><td>

Query Rules\[com.snc.query\_rules\]

</td><td>

Plugin that brings in the table and the logic needed to generate encoded queries per table for a user based on the roles the user has.

</td><td>

Inactive

</td><td>

false

</td><td>

 

</td></tr><tr><td>

Query stats\[com.glide.stats.query\]

</td><td>

Query stats.

</td><td>

Active

</td><td>

false

</td><td>

com.glide.stats

</td></tr><tr><td>

Quick Actions\[com.glide.quickactions\]

</td><td>

Enables slash commands in Agent Workspace chat.

</td><td>

Active

</td><td>

false

</td><td>

 

</td></tr><tr id="plugin_com.glide.quiz_designer" class="plugin_reference"><td class="name">

Quiz Designer\[com.glide.quiz\_designer\]

</td><td class="description">

Provides the ability to send scored questionnaires quickly and easily to one or more users. A quiz may have categories of questions that are assigned only to some users.

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

-   com.glide.assessment\_designer.common
-   com.snc.assessment\_core

</td></tr><tr><td class="name">

Random Watermark Support\[com.glide.email.random\_watermark\]

</td><td class="description">

Generate unpredictable watermarks, and enable matching on these watermarks in inbound emails.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

com.glide.mailbox

</td></tr><tr><td>

Rapid7 Vulnerability Integration\[sn\_vul\_t7\]

 \(Available in the ServiceNow Store\)

</td><td>

Provides the ability to integrate the ServiceNow Vulnerability Response application with the Rapid7 Nexpose and InsightVM products. Activation of this plugin on production instances may require a separate license. Contact ServiceNow for details.

</td><td>

 

</td><td>

 

</td><td>

sn\_vul

</td></tr><tr><td>

Rate Limit for REST API\[com.glide.rest.rate\_limit\]

</td><td>

Rate Limit support for REST API

</td><td>

Active

</td><td>

true

</td><td>

 

</td></tr><tr><td>

Read only roles for Agile - Scaled Agile Framework\[com.snc.sdlc.safe\_read\_roles\]

</td><td>

Provides read-only roles for Agile - Scaled Agile Framework.

</td><td>

Active

</td><td>

false

</td><td>

com.snc.agile\_read\_roles

</td></tr><tr><td>

Read only roles for Agile Development 2.0\[com.snc.agile\_read\_roles\]

</td><td>

Provides the sn\_agile\_read role that has read-only access for all Agile Development 2.0 tables. The data from these tables can be used for generating reports.

</td><td>

Active

</td><td>

false

</td><td>

 

</td></tr><tr><td>

Read only roles for Application Portfolio Management\[com.snc.apm\_read\_roles\]

</td><td>

The plugin provides read only roles for Application Portfolio Management.

</td><td>

Active

</td><td>

false

</td><td>

 

</td></tr><tr><td>

Read only roles for PPM Standard\[com.snc.pmo\_read\_roles\]

</td><td>

Read only roles for PPM Standard.

</td><td>

Active

</td><td>

false

</td><td>

 

</td></tr><tr><td>

Read only roles for Release Management\[com.snc.release\_management\_read\_roles\]

</td><td>

Provides the sn\_release\_read role that has read-only access for all Release Management tables. The data from these tables can be used for generating reports.

</td><td>

Active

</td><td>

false

</td><td>

 

</td></tr><tr><td>

Read only roles for Test Management 1.0\[com.snc.tm1\_read\_roles\]

</td><td>

Provides the sn\_tm1\_read role that has read-only access for all Test Management 1.0 tables.

</td><td>

Active

</td><td>

false

</td><td>

 

</td></tr><tr><td>

Read only roles for Test Management 2.0\[com.snc.tm2\_read\_roles\]

</td><td>

Provides the sn\_tm2\_read role that has read-only access for all Test Management 2.0 tables. The data from these tables can be used for generating reports.

</td><td>

Active

</td><td>

false

</td><td>

 

</td></tr><tr id="plugin_com.snc.read_only.role" class="plugin_reference"><td class="name">

Read-Only User Role\[com.snc.read\_only.role\]

</td><td class="description">

Enables Read-Only user role functionality.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

 

</td></tr><tr><td>

Recommended Actions\[sn\_nb\_action\]

 \(Available in the ServiceNow Store\)

</td><td>

Recommends relevant actions, such as Guidances and Guided Decisions, for a given context. Enables users to define contexts and strategies to recommend these actions.

</td><td>

Inactive

</td><td>

false

</td><td>

-   sn\_gd\_guidance
-   com.snc.next\_best\_action
-   sn\_nba\_list

</td></tr><tr><td>

Recommended Actions Advanced\[sn\_nb\_action\_adv\]

 \(Available in the ServiceNow Store\)

</td><td>

Enables customers to create recommendations based on AI/ML models created with Predictive Intelligence.

</td><td>

Inactive

</td><td>

false

</td><td>

com.snc.recommended\_action

</td></tr><tr><td>

Recommended Actions for Customer Service\[sn\_cs\_nb\_action\]

 \(Available in the ServiceNow Store\)

</td><td>

Installs the Recommended Actions capability, which recommends relevant actions for a given context. These actions appear on the Case form in the CSM Workspaces if users have defined strategies for the provided Case context.

</td><td>

Inactive

</td><td>

false

</td><td>

-   com.sn\_customerservice
-   com.snc.recommended\_action

</td></tr><tr><td>

Redox Electronic Health Record Spoke\[sn\_redox\_spoke\]

 \(Available in the ServiceNow Store\)

</td><td>

An Integration Hub spoke that is used to facilitate Redox outbound calls.

</td><td>

Inactive

</td><td>

false

</td><td>

-   com.glide.hub.integration.runtime
-   com.glide.hub.action\_step.rest
-   com.glide.cobject

</td></tr><tr><td>

Redox Inbound Integration\[sn\_redox\]

 \(Available in the ServiceNow Store\)

</td><td>

Improves inbound and proactive outbound service scalability and capabilities to integrate with healthcare systems that use the Redox platform.

</td><td>

Inactive

</td><td>

false

</td><td>

None

</td></tr><tr id="plugin_com.glide.ui.relationship_layout" class="plugin_reference"><td class="name">

Relationship Layout\[com.glide.ui.relationship\_layout\]

</td><td class="description">

Enables scoped relationships to be associated to out-of-scope related list views.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

 

</td></tr><tr id="plugin_com.snc.release_management_v2" class="plugin_reference"><td class="name">

Release Management\[com.snc.release\_management\_v2\]

</td><td class="description">

The Release Management v2 plugin is a rewrite of the original release management module. All products, releases, features, and release tasks are planned\_task extensions, and much of the project management functionality \(Gantt charts, timelines, time cards\) is shared with release.

</td><td>

Active

</td><td class="has_demo_data">

true

</td><td class="requires">

-   com.snc.release\_management
-   com.snc.planned\_task
-   com.snc.process\_flow\_formatter

</td></tr><tr><td>

Remote Tables\[com.glide.script.vtable\_demo\]

</td><td>

Supports remote tables and associated script definitions that can be used to retrieve and optionally cache data from external sources.Tra

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td class="name">

Report - PDF Page Header Footer Templates\[com.glideapp.report\_page\_hdrftr\]

</td><td class="description">

Allows the user to configure and store page headers and footers for PDF reports.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

-   com.glideapp.report
-   com.glideapp.report2

</td></tr><tr><td>

Report Access Request\[com.glideapp.report.access\_request\]

</td><td>

Provides the ability to request access to reports that have been restricted by report\_view ACL.

</td><td>

 

</td><td>

false

</td><td>

 

</td></tr><tr><td>

Report ACL Assessment\[com.par\_report\_acl\_assessment\]

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr id="plugin_com.glideapp.report.charting_v2" class="plugin_reference"><td class="name">

Report Charting v2\[com.glideapp.report.charting\_v2\]

</td><td class="description">

Installs V2 of ServiceNow charts with HighCharts.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

-   com.glideapp.report
-   com.glideapp.report2

</td></tr><tr id="plugin_com.glideapp.summary_report_engine" class="plugin_reference"><td class="name">

Report Engine - use summary table for reports\[com.glideapp.summary\_report\_engine\]

</td><td class="description">

Causes the data from all reports, custom and standard, to be stored in the sys\_report\_summary table and separates the data from the rendering process for all reports. Report data is periodically purged from the sys\_report\_summary table \(approximately every two hours\).

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

com.glideapp.report2

</td></tr><tr><td class="name">

Report Security - enforce access control checks\[com.glideapp.report\_security\]

</td><td class="description">

Enforces ACL checks when reports are created, deleted or updated.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

-   com.glideapp.report
-   com.glideapp.report2

</td></tr><tr id="plugin_com.glideapp.report_statreports" class="plugin_reference"><td class="name">

Reporting Statistics Reports\[com.glideapp.report\_statreports\]

</td><td class="description">

Provides reports and dashboards on reporting statistics.

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

com.glideapp.report

</td></tr><tr id="plugin_com.snc.required_form_fields" class="plugin_reference"><td class="name">

Required Form Fields\[com.snc.required\_form\_fields\]

</td><td class="description">

Allows an administrator to specify required fields that cannot be removed from a form.

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

 

</td></tr><tr id="plugin_com.snc.resource_management" class="plugin_reference"><td class="name">

Resource Management\[com.snc.resource\_management\]

</td><td class="description">

Enables resource requesters and resource managers to plan, organize, and manage resources for both planned and unexpected work. Activating Resource Management automatically activates the Project Management plugin if it is not already active. Only upgrade is allowed for this plugin. Activation should be done through PPM Standard plugin.

</td><td>

Inactive

</td><td class="has_demo_data">

true

</td><td class="requires">

-   com.snc.schedule\_loader
-   com.snc.process\_flow\_formatter
-   com.snc.cost\_management
-   com.snc.pps\_portal\_common

</td></tr><tr id="plugin_com.snc.matching_rule" class="plugin_reference"><td class="name">

Resource Matching Engine\[com.snc.matching\_rule\]

</td><td class="description">

Provides a Resource Matching Engine.

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

-   com.snc.skills\_management
-   com.snc.agent\_schedule

</td></tr><tr id="plugin_com.glideapp.canvas" class="plugin_reference"><td class="name">

Responsive Canvas\[com.glideapp.canvas\]

</td><td class="description">

Enables responsive canvas. For dashboards, the responsive canvas dynamically responds to dashboard resizing and enables dragging to place and resize widgets. Easily find and preview widgets that you want to add directly from the canvas.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

-   com.glideapp.home
-   com.glide.text\_search
-   com.glide.db\_images
-   com.glide.ui.angular
-   com.glide.ui.ng

</td></tr><tr><td>

Responsive Dashboards\[com.glideapp.dashboards\]

</td><td>

Easily create, modify, and share dashboards using responsive and dynamic widget layouts.

</td><td>

Active

</td><td>

false

</td><td class="requires">

-   com.glideapp.canvas
-   com.glideapp.home
-   com.glide.text\_search
-   com.glide.db\_images
-   com.glide.ui.angular
-   com.glide.ui.ng
-   com.snc.pa

</td></tr><tr><td>

REST API Builder Backend\[com.glide.rest.api\_builder.backend\]

</td><td>

REST API Builder Framework data model and crud interfaces.

</td><td>

 

</td><td>

false

</td><td>

com.glide.api\_runtime

</td></tr><tr><td>

REST API for global text search\[com.glide.globalsearch\]

</td><td>

REST API for global text search.

</td><td>

Active

</td><td>

false

</td><td>

com.glide.rest

</td></tr><tr><td>

REST API Trigger Flow Designer\[com.glide.hub.flow\_trigger.rest\]

</td><td>

Adds ability for flow designers to create a REST endpoint that triggers a flow upon request.

</td><td>

 

</td><td>

false

</td><td>

-   com.glide.hub.flow\_trigger
-   com.glide.api\_runtime
-   com.glide.rest.api\_builder.backend

</td></tr><tr id="plugin_com.glide.rest" class="plugin_reference"><td class="name">

REST API Provider\[com.glide.rest\]

</td><td class="description">

Provides a REST API framework to support RESTful services.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

-   com.glide.ui.angular
-   com.glide.ui.heisenberg

</td></tr><tr id="plugin_com.snc.undelete" class="plugin_reference"><td class="name">

Restore Deleted Records\[com.snc.undelete\]

</td><td class="description">

Restores deleted records from audited tables and references to those records. Also restores any records that were deleted as a result of a cascade delete rule.

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

 

</td></tr><tr><td>

Robotic Process Automation \(RPA\) Hub\[com.sn\_rpa\_foundation\]

 \(Available in the ServiceNow Store\)

</td><td>

Provides the capability to integrate the ServiceNow platform with applications that do not support APIs.

</td><td>

Active

</td><td>

true

</td><td>

sn\_cmdb\_ci\_class \(1.36.0\)

</td></tr><tr><td>

RPA Sample Template\[com.sn\_rpa\_template\]

 \(Available in the ServiceNow Store\)

</td><td>

RPA templates are prebuilt automations that enable customers to kickstart their RPA initiatives. This template provides automating user password reset functionality for Oracle E-Business Suite \(EBS\) where APIs aren't available. It guides the ServiceNow developer to implement password reset functionality.

</td><td>

Active

</td><td>

false

</td><td>

com.sn\_rpa\_foundation \(3.0.7\)

</td></tr><tr id="plugin_com.snc.role_delegation" class="plugin_reference"><td class="name">

Role Delegation\[com.snc.role\_delegation\]

</td><td class="description">

Allows an administrator to designate role delegators, who can delegate any role they have to members of their group.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

com.glideapp.workflow

</td></tr><tr><td>

S/MIME Email\[com.glide.email.smime\]

 \(New in Tokyo\)

</td><td>

Enables sending/receiving signed and encrypted emails using S/MIME.

</td><td>

Active

</td><td>

false

</td><td>

-   com.glide.certificates
-   com.glide.kmf

</td></tr><tr id="plugin_com.snc.sfa2" class="plugin_reference"><td class="name">

Sales Force Automation application template\[com.snc.sfa2\]

</td><td class="description">

Provides tools to manage sales and marketing operations throughout the sales life cycle from lead generation through contract completion.

</td><td>

Inactive

</td><td class="has_demo_data">

true

</td><td class="requires">

com.snc.process\_flow\_formatter

</td></tr><tr><td>

Scenario Planning for PPM\[sn\_pw\_scenario\]

 \(Available in the ServiceNow Store\)

</td><td>

Scenario Planning is a simple system to create and compare scenarios for a portfolio.

</td><td>

Active

</td><td>

true

</td><td>

com.snc.financial\_planning\_pmo

</td></tr><tr><td>

Schedule Optimization \[com.snc\_schedule\_optimization\]

 \(New in Utah\)

</td><td>

Agent schedules are automatically optimized daily to consolidate tasks and minimize travel time.

</td><td>

Inactive

</td><td>

false

</td><td>

-   com.glide.platform\_ml
-   com.snc.work\_management
-   com.snc.app\_fsm\_sched\_model

</td></tr><tr><td>

Schedule Optimization - Common\[com.snc\_schedule\_optimization.common\]

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Schedule Optimization - UI components\[com.snc\_schedule\_optimization.ui\]

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr id="plugin_com.glide.erd" class="plugin_reference"><td class="name">

Schema Map v3\[com.glide.erd\]

</td><td class="description">

Displays the details of tables and their relationships in a visual manner, allowing administrators to view and easily access different parts of the database schema.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

com.glide.diagrammer

</td></tr><tr id="plugin_com.glide.scoped_analytics_framework" class="plugin_reference"><td class="name">

Scoped Analytics Framework\[com.glide.scoped\_analytics\_framework\]

</td><td class="description">

Analytics Framework for Scoped Applications.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

 

</td></tr><tr><td class="name">

Scoped Application Restricted Caller Access\[com.glide.scope.access.restricted\_caller\]

</td><td class="description">

Allow scoped applications to restrict access to public tables and script includes.

</td><td>

Inactive

</td><td class="has demo data">

false

</td><td>

 

</td></tr><tr><td>

Script Execution Context\[com.snc.sn\_context\]

</td><td>

Provides virtual closure mechanism.

</td><td>

Inactive

</td><td>

false

</td><td>

 

</td></tr><tr><td>

Script stats\[com.glide.stats.script\]

</td><td>

Script stats.

</td><td>

Active

</td><td>

false

</td><td>

com.glide.stats.script

</td></tr><tr id="plugin_com.glide.script.templates" class="plugin_reference"><td class="name">

Script Templates\[com.glide.script.templates\]

</td><td class="description">

Provides templates for some script fields.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

 

</td></tr><tr id="plugin_com.glide.script.whitelist" class="plugin_reference"><td class="name">

Script Allowlist Manager\[com.glide.script.whitelist\]

</td><td class="description">

Provides temporary support for continued direct invocation of Java Packages, Constructors, and Methods that are added to an allow list.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

 

</td></tr><tr id="plugin_com.glide.scripted_rest_services" class="plugin_reference"><td class="name">

Scripted REST APIs\[com.glide.scripted\_rest\_services\]

</td><td class="description">

Provides a framework for building Scripted REST APIs.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

-   com.glide.rest
-   com.glide.scripted\_rest\_services.internal
-   com.glide.scripted\_rest\_services.errors

</td></tr><tr id="plugin_com.glide.scripted_rest_services.errors" class="plugin_reference"><td class="name">

Scripted REST APIs - Error types\[com.glide.scripted\_rest\_services.errors\]

</td><td class="description">

An internal plugin component to Scripted REST APIs.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

 

</td></tr><tr id="plugin_com.glide.scripted_rest_services.internal" class="plugin_reference"><td class="name">

Scripted REST APIs - Internal\[com.glide.scripted\_rest\_services.internal\]

</td><td class="description">

An internal plugin component to Scripted REST APIs.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

 

</td></tr><tr><td>

Scrum Program\[com.snc.sdlc.scrum\_program\]

</td><td>

Plan and track the work across multiple Scrum teams that are working towards common objectives.

</td><td>

Inactive

</td><td>

true

</td><td class="requires">

-   com.snc.program\_common
-   com.snc.sdlc.agile.2.0

</td></tr><tr id="plugin_com.glide.ui.scss.bootstrap" class="plugin_reference"><td class="name">

SCSS Bootstrap Theme\[com.glide.ui.scss.bootstrap\]

</td><td class="description">

Theme assets for Bootstrap using SCSS.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

com.glide.ui.scss

</td></tr><tr id="plugin_com.glide.ui.scss" class="plugin_reference"><td class="name">

SCSS Content Provider\[com.glide.ui.scss\]

</td><td class="description">

SCSS Content Provider.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

 

</td></tr><tr><td>

SDL Translation Management System Spoke for Localization Framework\[com.glide.localization\_framework.sdl\_spoke\]

</td><td>

It integrates Localization Framework with the SDL - Translation Management System. To activate this plugin, install the Localization Framework Installer plugin.

</td><td>

Active

</td><td>

false

</td><td>

com.glide.localization\_framework

</td></tr><tr id="plugin_com.snc.sdlc.scrum" class="plugin_reference"><td class="name">

SDLC - SCRUM\[com.snc.sdlc.scrum\]

</td><td class="description">

Adds a release process specific to a Scrum development process. Sits on top of the SDLC application, adding additional agile notions like epics, stories, and sprints.

</td><td>

Inactive

</td><td class="has_demo_data">

true

</td><td class="requires">

com.snc.sdlc

</td></tr><tr><td>

Search Suggestions\[com.glide.search.suggestions\]

</td><td>

Provides suggestions when you enter text in a search field.

</td><td>

Active for new instances. Upgraded instances adopt the previous setting.

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Security Center\[com.sn.vault\_security\_center\]

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Security Dashboard\[com.glide.security.dashboard\]

</td><td>

Activates the Security Dashboard.

</td><td>

Inactive

</td><td>

false

</td><td>

com.snc.guided\_setup

</td></tr><tr id="plugin_com.snc.security_incident.analytics" class="plugin_reference"><td class="name">

Security Incident Analytics\[com.snc.security\_incident.analytics\]

</td><td class="description">

Provides an integration of Security Incident Response with Performance Analytics for trend-based reporting. Activation of this plugin on production instances may require a separate license. Contact ServiceNow for details.

</td><td>

Inactive

</td><td class="has_demo_data">

true

</td><td class="requires">

-   com.snc.pa
-   com.snc.treemap
-   com.snc.security\_incident

</td></tr><tr id="plugin_com.snc.security_incident" class="plugin_reference"><td class="name">

Security Incident Response\[com.snc.security\_incident\]

 \(Available in the ServiceNow Store\)

</td><td class="description">

Provides visibility into the state of an organization’s security using many of the same workflow and reporting capabilities ServiceNow is known for. Activation of this plugin on production instances may require a separate license. Contact ServiceNow for details.

</td><td>

Inactive

</td><td class="has_demo_data">

true

</td><td class="requires">

-   com.snc.service\_management.core
-   com.snc.task\_outage
-   com.snc.treemap
-   com.snc.secops.orchestration
-   com.snc.security\_support.sir
-   com.snc.whtp
-   com.snc.threat

</td></tr><tr><td>

Security Incident Response Dependencies\[com.snc.si\_dep\]

 \(Available in the ServiceNow Store\)

</td><td>

Installs all the dependent plugins required to support the Security Incident Response application.

</td><td>

Active

</td><td>

false

</td><td class="requires">

-   com.snc.security\_support.core
-   com.snc.security\_support.sir
-   com.snc.runbook\_automation.runtime
-   com.snc.task\_outage
-   com.snc.treemap
-   com.snc.whtp
-   com.glide.scope.access.restricted\_caller
-   com.sn\_dependentclient

</td></tr><tr><td>

Security Incident Response Mobile\[com.sn\_sir\_mobile\]

 \(Available in the ServiceNow Store\)

</td><td>

As a security operations center \(SOC\) manager or a user with the ServiceNow AI Platform security analyst role \(sn\_si.analyst\), you can log in to a ServiceNow AI Platform instance directly from your Android or iOS mobile device. With the Security Incident Response Mobile app, you can view, edit, and assign your most current and critical SIR security incidents and response tasks. Notifications inform you when critical security incidents assigned to you arrive.

</td><td>

Inactive

</td><td>

 

</td><td>

com.glide.sg.agent\_native\_client

</td></tr><tr><td>

Security Incident Response UI\[com.app\_secops\_ui\]

 \(Available in the ServiceNow Store\)

</td><td>

Provides an enhanced user interface for monitoring and resolving threats to an organization’s security. Activation of this plugin on production instances may require a separate license. Contact ServiceNow for details.

</td><td>

Inactive

</td><td>

true

</td><td>

com.snc.security\_incident

</td></tr><tr><td>

Security Integration Framework\[com.snc.sec.int.framework\]

 \(Available in the ServiceNow Store\)

</td><td>

Activation of this plugin on production instances may require a separate license. Contact ServiceNow for details.

</td><td>

Inactive

</td><td>

false

</td><td>

 

</td></tr><tr id="plugin_com.snc.system_security" class="plugin_reference"><td class="name">

Security Jump Start \(ACL Rules\)\[com.snc.system\_security\]

 \(Available in the ServiceNow Store\)

</td><td class="description">

Adds ACL rules to provide a jump-start on securing many system tables, making it easier for an organization to get into production more quickly.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

 

</td></tr><tr><td>

Security Operations 'Have I Been Pwned?' Integration\[com.snc.secops.pwned\]

 \(Available in the ServiceNow Store\)

</td><td>

Provides the ability to submit Whois lookups on domain names and URLs to obtain context on URL observables, and to make better determination on threats. Activation of this plugin on production instances may require a separate license. Contact ServiceNow for details.

</td><td>

Inactive

</td><td>

false

</td><td class="requires">

-   com.snc.threat
-   com.snc.security\_incident

</td></tr><tr><td>

Security Operations ArcSight Logger Integration\[com.snc.secops.arcsight.logger\]

 \(Available in the ServiceNow Store\)

</td><td>

Activation of this plugin on production instances may require a separate license. Contact ServiceNow for details.

</td><td>

Inactive

</td><td>

false

</td><td>

com.snc.security\_incident

</td></tr><tr><td>

Security Operations Carbon Black Integration\[com.snc.secops.carbonblack\]

 \(Available in the ServiceNow Store\)

</td><td>

Activation of this plugin on production instances may require a separate license. Contact ServiceNow for details.

</td><td>

Inactive

</td><td>

false

</td><td class="requires">

-   com.snc.secops.orchestration
-   com.snc.security\_incident

</td></tr><tr><td>

Security Operations CrowdStrike Host Integration\[com.snc.secops.crowdstrike.host\]

 \(Available in the ServiceNow Store\)

</td><td>

Activation of this plugin on production instances may require a separate license. Contact ServiceNow for details.

</td><td>

Inactive

</td><td>

false

</td><td>

com.snc.security\_incident

</td></tr><tr><td>

Security Operations CrowdStrike Intelligence Integration\[com.snc.secops.crowdstrike.intel\]

 \(Available in the ServiceNow Store\)

</td><td>

Activation of this plugin on production instances may require a separate license. Contact ServiceNow for details.

</td><td>

Inactive

</td><td>

false

</td><td class="requires">

-   com.snc.threat
-   com.snc.threat.intelligence

</td></tr><tr><td>

Security Operations Elasticsearch Integration\[com.snc.secops.elasticsearch\]

 \(Available in the ServiceNow Store\)

</td><td>

Searches your Elasticsearch logs and adds relevant sighting information to your security incidents. Activation of this plugin on production instances may require a separate license. Contact ServiceNow for details.

</td><td>

Inactive

</td><td>

false

</td><td>

com.snc.security\_incident

</td></tr><tr><td>

Security Operations McAfee ESM Integration\[com.snc.secops.mcafee.esm\]

 \(Available in the ServiceNow Store\)

</td><td>

Activation of this plugin on production instances may require a separate license. Contact ServiceNow for details.

</td><td>

Inactive

</td><td>

false

</td><td>

com.snc.security\_incident

</td></tr><tr><td>

Security Operations Microsoft Exchange Integration\[com.snc.secops.ms-exchange\]

 \(Available in the ServiceNow Store\)

</td><td>

Activation of this plugin on production instances may require a separate license. Contact ServiceNow for details.

</td><td>

Inactive

</td><td>

true

</td><td>

com.snc.security\_incident

</td></tr><tr><td>

Security Operations Palo Alto Networks - AutoFocus \[com.snc.secops.paloalto.autofocus\]

 \(Available in the ServiceNow Store\)

</td><td>

Provides the ability to integrate the ServiceNow Security Incident Response application with the Palo Alto Networks AutoFocus. Activation of this plugin on production instances may require a separate license. Contact ServiceNow for details.

</td><td>

Inactive

</td><td>

false

</td><td class="requires">

-   com.snc.security\_incident
-   com.snc.secops.orchestration

</td></tr><tr><td>

Security Operations Palo Alto Networks - Firewall\[com.snc.secops.paloalto\]

 \(Available in the ServiceNow Store\)

</td><td>

Activation of this plugin on production instances may require a separate license. Contact ServiceNow for details.

</td><td>

Inactive

</td><td>

false

</td><td class="requires">

-   com.snc.secops.orchestration
-   com.snc.security\_incident

</td></tr><tr><td>

Security Operations Palo Alto Networks - WildFire\[com.snc.secops.paloalto.wildfire\]

 \(Available in the ServiceNow Store\)

</td><td>

Provides the ability to integrate the ServiceNow Security Incident Response application with the Palo Alto Networks WildFire application. Activation of this plugin on production instances may require a separate license. Contact ServiceNow for details.

</td><td>

Inactive

</td><td>

false

</td><td class="requires">

-   com.snc.security\_incident
-   com.snc.secops.orchestration

</td></tr><tr><td>

Security Operations Splunk ES Event Ingestion Integration\[com.snc.secops.splunkes\]

 \(Available in the ServiceNow Store\)

</td><td>

This is the Splunk Enterprise Security Integration for Security Incident Response.

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Security Operations QRadar SIEM Integration \[com.snc.secops.qradar.siem\]

 \(Available in the ServiceNow Store\)

</td><td>

Provides the ability to integrate the ServiceNow Security Incident Response application with QRadar SIEM data. Activation of this plugin on production instances may require a separate license. Contact ServiceNow for details.

</td><td>

Inactive

</td><td>

false

</td><td>

com.snc.security\_incident

</td></tr><tr><td>

Security Operations Splunk Integration\[com.snc.secops.splunk\]

 \(Available in the ServiceNow Store\)

</td><td>

Searches your Splunk logs and adds relevant sighting information to your security incidents. Activation of this plugin on production instances may require a separate license. Contact ServiceNow for details.

</td><td>

Inactive

</td><td>

false

</td><td>

com.snc.security\_incident

</td></tr><tr><td>

Security Operations Spoke\[com.snc.secops.spoke\]

 \(Available in the ServiceNow Store\)

</td><td>

Provides the ability to use Security Operations flows and actions. Activation of this plugin on production instances may require a separate license. Contact ServiceNow for details.

</td><td>

Inactive

</td><td>

false

</td><td class="requires">

-   com.snc.security\_incident
-   com.glide.hub

</td></tr><tr><td>

Security Operations Tanium Integration \[com.snc.secops.tanium\]

 \(Available in the ServiceNow Store\)

</td><td>

Provides the ability to integrate the ServiceNow Security Incident Response application with Tanium data. Activation of this plugin on production instances may require a separate license. Contact ServiceNow for details.

</td><td>

Inactive

</td><td>

false

</td><td class="requires">

-   com.snc.security\_incident
-   com.snc.secops.orchestration

</td></tr><tr><td>

Security Operations WHOIS Integration\[com.snc.secops.whois\]

 \(Available in the ServiceNow Store\)

</td><td>

Activation of this plugin on production instances may require a separate license. Contact ServiceNow for details.

</td><td>

Inactive

</td><td>

false

</td><td>

com.snc.threat

</td></tr><tr id="plugin_com.snc.security_support.common" class="plugin_reference"><td class="name">

Security Support Common\[com.snc.security\_support.common\]

 \(Available in the ServiceNow Store\)

</td><td class="description">

Provides common functionality for use across the various security applications, such as Security Incident Response. Activation of this plugin on production instances may require a separate license. Contact ServiceNow for details.

</td><td>

Inactive

</td><td class="has_demo_data">

true

</td><td class="requires">

com.snc.security\_support.core

</td></tr><tr><td class="name">

Security Support Orchestration\[com.snc.secops.orchestration\]

</td><td>

Provides an integration of Security Operations with Orchestration to allow the facilitation of workflow activities within Security Incident Response, Threat Intelligence, or Vulnerability Response. Activation of this plugin on production instances may require a separate license. Contact ServiceNow for details.

</td><td>

Inactive

</td><td>

false

</td><td class="requires">

-   com.snc.runbook\_automation.runtime
-   com.snc.security\_support.common

</td></tr><tr><td>

Self-Service Analytics Core\[com.snc.self\_service\_analytics\_core\]

</td><td>

Provides the self-service analytics framework for configuring deflection contexts and activity patterns to collect the case reduction \(deflection\) metrics.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

com.snc.activity\_subscriptions

</td></tr><tr><td>

Self-Service Analytics for Customer Service\[com.snc.pa.self\_service\_analytics\_csm\]

</td><td>

Tracks case reduction \(deflection\) metrics and self-service KPIs using performance analytics dashboards. Activation of this plugin on production instances may require a separate Performance Analytics license. Contact ServiceNow for details.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

-   com.sn\_customerservice
-   com.snc.pa.self\_service\_analytics
-   com.snc.self\_service\_analytics\_core

</td></tr><tr><td>

Self-Service Analytics PA\[com.snc.pa.self\_service\_analytics\]

</td><td>

Enables users to define and track key performance indicators \(KPIs\) to measure the effectiveness of self-service channels such as knowledge, community, virtual agent, and service catalog. Activation of this plugin on production instances may require a separate Performance Analytics license. Contact ServiceNow for details.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

com.snc.pa

</td></tr><tr id="plugin_com.snc.password_reset" class="plugin_reference"><td class="name">

Self Service Password Reset\[com.snc.password\_reset\]

</td><td class="description">

Allows locally authenticated users to request a temporary password if they forget their current password.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

com.glideapp.password\_reset

</td></tr><tr><td>

Self-Service Portal for Analytics\[com.snc.pa.bi\_service\]

</td><td>

Self-Service Portal for Analytics - Allows users to request services related to dashboard access.

</td><td>

Inactive

</td><td>

false

</td><td>

com.snc.pa

</td></tr><tr><td>

Sensitive Data Handling\[com.glide.sensitive\_data\_handling\]

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Sentiment Analysis\[com.snc.sentiment\_analysis\]

</td><td>

This plugin is used for Sentiment Analysis

</td><td>

Inactive

</td><td>

false

</td><td>

com.snc.core.automation.connection\_credential

</td></tr><tr id="plugin_com.glide.debugger" class="plugin_reference"><td class="name">

Server-side JavaScript Debugger\[com.glide.debugger\]

</td><td class="description">

Allows application developers and administrators to efficiently debug scripts that drive the applications they develop and support.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

-   com.glide.ui.angular
-   com.glide.ui.zepto
-   com.glide.ui.font\_icons

</td></tr><tr><td>

Service Catalog - ATF Tests\[com.glideapp.servicecatalog.atf.test\]

</td><td>

Provides Service Catalog ATF Tests

</td><td>

Active

</td><td>

true

</td><td>

 

</td></tr><tr><td>

Service Catalog - Channel Source Analytics\[com.glideapp.servicecatalog.analytics\]

</td><td>

Enables the channel source analytics for Catalog Items.

</td><td>

Active

</td><td>

false

</td><td>

com.glideapp.servicecatalog

</td></tr><tr><td class="name">

Service Catalog - Domain Separation\[com.glideapp.servicecatalog.domain\_separation\]

</td><td>

Enables service providers to separate catalog items for different domains

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Service Catalog - Workspace\[com.glideapp.servicecatalog.workspace\]

</td><td>

Service Catalog - Workspace

</td><td>

false

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Service Catalog Builder\[com.glideapp.servicecatalog.catalog\_builder\]

</td><td>

Catalog builder for easy creation and maintenance of catalog items. Installation of this plugin allows creation and editing of catalog items as draft and each change needs to be published.

</td><td>

Active

</td><td>

true

</td><td>

-   com.glideapp.servicecatalog.platform
-   com.glideapp.servicecatalog.composite\_record\_producer
-   com.glideapp.servicecatalog.wizard
-   com.glideapp.servicecatalog.catalog\_template
-   com.glideapp.servicecatalog.catalog\_builder\_experience

</td></tr><tr><td>

Service Catalog Builder Experience\[com.glideapp.servicecatalog.catalog\_builder\_experience\]

</td><td>

This plugin is for catalog builder experience in UXF.

</td><td>

 

</td><td>

false

</td><td>

-   com.sn\_canvas\_blank
-   com.sn\_canvas\_chrome

</td></tr><tr><td>

Service Catalog Builder internal components\[com.glideapp.servicecatalog.builder.internal\_components\]

</td><td>

Internal components that make up Catalog Builder. Install this plugin to edit catalog builder experience.

</td><td>

 

</td><td>

false

</td><td>

 

</td></tr><tr class="plugin_reference"><td class="name">

Service Catalog CMS Extension\[com.glideapp.servicecatalog.cms\]

</td><td class="description">

Provides the ability to define the catalog experience within CMS.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

-   com.glideapp.servicecatalog.platform
-   com.glide.cms

</td></tr><tr><td>

Service Catalog Composite Record Producer\[com.glideapp.servicecatalog.composite\_record\_producer\]

</td><td>

Composite Record Producer allows records to be created and edited in multiple related tables without needing scripts.

</td><td>

 

</td><td>

false

</td><td>

com.glideapp.servicecatalog.platform

</td></tr><tr class="plugin_reference"><td class="name">

Service Catalog core applications\[com.glideapp.servicecatalog\]

</td><td class="description">

Allows customers to order predefined, bundled goods and services from your IT organization or other departments.

</td><td>

Active

</td><td class="has_demo_data">

true

</td><td class="requires">

-   com.glideapp.servicecatalog.platform
-   com.glideapp.servicecatalog.execution\_plan
-   com.glideapp.servicecatalog.currency

</td></tr><tr><td>

Service Catalog Macroponent internal components\[com.glideapp.servicecatalog.macroponent.internal\_components\]

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Service Catalog Manager\[com.snc.sc\_catalog\_manager\]

</td><td>

Provides utility for managing categories, catalog items, and Knowledge Base links for Service Catalogs.

</td><td>

Inactive

</td><td>

false

</td><td>

 

</td></tr><tr><td>

Service Catalog Mobile Employee\[com.glideapp.servicecatalog.mobile-employee\]

</td><td>

This plugin contains the configuration, records, and catalog webviews that are used in Mobile Employee Experience native application.**Note:** Do not activate this plugin directly. Activating com.glide.mobile-employee activates this plugin for you.

</td><td>

Inactive

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Service Catalog My Request for Mobile\[com.glideapp.servicecatalog.mobile-request-filter\]

</td><td>

This plugin contains the configuration, records that are used in Mobile native application for My Request. Do not activate this plugin directly. Activating com.glide.mobile-employee will activate this plugin for you.

</td><td>

Inactive

</td><td>

false

</td><td>

 

</td></tr><tr id="plugin_com.glideapp.servicecatalog.rest.api" class="plugin_reference"><td class="name">

Service Catalog REST API\[com.glideapp.servicecatalog.rest.api\]

</td><td class="description">

Service Catalog REST API.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

com.glideapp.servicecatalog.scoped.api

</td></tr><tr id="plugin_com.glideapp.servicecatalog.scoped.api" class="plugin_reference"><td class="name">

Service Catalog Scoped API\[com.glideapp.servicecatalog.scoped.api\]

</td><td class="description">

Service Catalog Scoped API to support application creation on Service Catalog platform.

</td><td>

Active

</td><td class="has_demo_data">

true

</td><td class="requires">

com.glideapp.servicecatalog

</td></tr><tr><td>

Service Catalog Template\[com.glideapp.servicecatalog.catalog\_template\]

</td><td>

Framework to create and maintain catalog templates.

</td><td>

 

</td><td>

false

</td><td>

com.glideapp.servicecatalog.platform

</td></tr><tr><td>

Service Catalog Wizard\[com.glideapp.servicecatalog.wizard\]

</td><td>

Activating this plugin creates the data model for wizards.

</td><td>

 

</td><td>

false

</td><td>

com.glideapp.servicecatalog.platform

</td></tr><tr id="plugin_com.glide.service_creator" class="plugin_reference"><td class="name">

Service Creator\[com.glide.service\_creator\]

</td><td class="description">

Enables a department to offer custom services through the service catalog, such as the HR department offering tuition reimbursement for further education.

</td><td>

Active

</td><td class="has_demo_data">

true

</td><td class="requires">

-   com.glide.ui.ng.cc
-   com.glideapp.servicecatalog.item\_designer

</td></tr><tr><td>

Service Credits\[com.sn\_service\_credits\]

</td><td>

Vendor service credits.

</td><td>

 

</td><td>

false

</td><td>

-   com.snc.service\_portfolio
-   com.snc.service\_portfolio.sla\_commitment
-   com.snc.task\_outage

</td></tr><tr><td>

Service Delivery Common\[com.sn\_spend\_sdc\]

\(Starting with the Utah release, Service Delivery Common is renamed as Common Service Delivery.\)

\(Available in the ServiceNow Store\)

</td><td>

Contains Service Task and Service Request tables, as well as other infrastructure that forms the basis of Finance and Supply Chain Workflows products.

</td><td>

Inactive

</td><td>

false

</td><td>

-   com.glide.pad.core
-   com.glide.pad.license
-   com.playbook\_experience

</td></tr><tr><td>

Service Fulfillment Steps\[com.glideapp.servicecatalog.service\_fulfillment\_steps\]

</td><td>

Adds support for Service Fulfillment using Data Driven Workflows.

</td><td>

Active

</td><td>

false

</td><td>

-   com.glideapp.servicecatalog.platform
-   com.glideapp.servicecatalog.catalog\_builder

</td></tr><tr><td>

Service Graph Connector for Microsoft Defender for IoT \(Azure\)\[com.sn\_msftd4iotazsgc\]

\(Available in the ServiceNow Store\)

</td><td>

Integrates Microsoft Defender for IoT \(Azure\) with the ServiceNow Operational Technology Manager application to import devices and sensor appliances.

</td><td>

Active

</td><td>

False

</td><td>

-   com.sn\_cmdb\_ci\_class
-   com.snc.cmdb.integration\_uti
-   com.glide.hub.action\_type.datastream
-   com.snc.itom.discovery.license
-   com.snc.itom.license

</td></tr><tr><td>

Service Graph Connector Integration for Claroty CTD\[com.sn\_clarotyctdsgc\]

\(Available in the ServiceNow Store\)

</td><td>

Integrates Claroty CTD with the ServiceNow Operational Technology Manager application to import sites, detected devices by each site, connection \(or baselines\), and installed programs.

</td><td>

Active

</td><td>

False

</td><td>

-   com.sn\_cmdb\_ci\_class
-   com.snc.cmdb.integration\_util
-   com.glide.hub.action\_type.datastream
-   com.snc.itom.discovery.license
-   com.snc.itom.license

</td></tr><tr><td>

Service Graph Connector for Operational Technology\[com.sn\_otsm\_sgc\]

\(Available in the ServiceNow Store\)

</td><td>

Enables you to import your existing Operational Technology data from a populated Microsoft Excel flat-file spreadsheet. You use it in the Integration Hub Extract Transform Load \(ETL\) to upload this data to the Configuration Management Database \(CMDB\).

</td><td>

Active

</td><td>

false

</td><td>

-   com.sn\_cmdb\_ci\_class
-   com.snc.cmdb.integration\_util
-   com.sn\_ot\_core

</td></tr><tr><td>

Service Integration and Management\[com.snc.siam\_core\]

</td><td>

SIAM Core plugin that provides support for Global scope access, required by applications like VMW and Service Onboarding.

</td><td>

Inactive

</td><td>

false

</td><td>

 

</td></tr><tr id="plugin_com.snc.sla" class="plugin_reference"><td class="name">

Service Level Management\[com.snc.sla\]

</td><td class="description">

Provides the core SLA functionality. SLA Definitions provide conditions to start, pause, stop, cancel and reset Task SLAs against any Task type. In addition, you can specify a schedule on the definition to define the working hours and also a workflow to run against each Task SLA, which is typically used to generate notifications.

</td><td>

Active

</td><td class="has_demo_data">

true

</td><td class="requires">

-   com.glideapp.workflow
-   com.glide.schedules
-   com.glide.relative\_duration

</td></tr><tr><td>

Service Level Management - Contract Management Integration\[com.snc.sla.contract2\]

</td><td>

Extends the existing SLA functionality, by utilizing a contract as the primary document that houses all appropriate data needed to drive the SLA processing of your task.The attach\_sla field is added.

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Service Level Management Dashboard\[com.snc.sla.overview\]

</td><td>

This plugin provides the My SLAs Dashboard for Service Level Management

</td><td>

Active

</td><td>

false

</td><td class="requires">

-   com.glideapp.canvas
-   com.snc.sla

</td></tr><tr><td>

Service Level Management Guided Tour\[com.snc.sla.guided\_tour\]

</td><td>

Provides the Guided tour of SLA functionality.

</td><td>

Active

</td><td>

false

</td><td>

 

</td></tr><tr><td>

Service Level Management PA Dashboard\[com.snc.pa.sla.overview\]

</td><td>

This plugin provides the SLA Overview \(Premium\) Dashboard. Activation of this plugin on production instances may require a separate Performance Analytics license. Contact ServiceNow for details.

</td><td>

Active

</td><td>

false

</td><td class="requires">

-   com.glideapp.canvas
-   com.snc.pa
-   com.snc.sla
-   com.snc.sla.breakdowns

</td></tr><tr><td>

Service Operations Workspace Service Dashboard\[com.sn\_itom\_service\_dashboard\]

 \(Available in the ServiceNow Store\)

</td><td>

Monitors the health of services in a dashboard.

</td><td>

 

</td><td>

false

</td><td>

Service Operations Workspace ITOM Applications

</td></tr><tr id="plugin_com.snc.service_management.geolocation" class="plugin_reference"><td class="name">

Service Management Geolocation\[com.snc.service\_management.geolocation\]

</td><td class="description">

Provides Service Management geolocation capabilities.

</td><td>

Inactive

</td><td class="has_demo_data">

true

</td><td class="requires">

com.snc.geolocation

</td></tr><tr id="plugin_com.snc.service_management_m" class="plugin_reference"><td class="name">

Service Management Geolocation Mobile\[com.snc.service\_management\_m\]

</td><td class="description">

Adds a menu in the new mobile UI for Service Management Geolocation.

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

-   com.glide.ui.m
-   com.snc.service\_management.geolocation

</td></tr><tr><td>

Service Management Virtual Agent Core\[com.glideapp.sm\_va\_core\]

</td><td>

Provides core functionality for Service Management Virtual Agent

</td><td>

Active

</td><td>

false

</td><td>

 

</td></tr><tr><td>

Service Management Virtual Agent Topic Blocks\[com.glideapp.cs.sm\_topic\_blocks\]

</td><td>

This plugin contains prebuilt re-usable conversation topic blocks for common actions like ordering from the catalog and searching the knowledge base.

</td><td>

Inactive

</td><td>

false

</td><td class="requires">

-   com.glide.cs.chatbot
-   com.snc.contextual\_search
-   com.glideapp.servicecatalog.platform

</td></tr><tr><td>

Service Mapping Plus\[sn\_sm\_scoped\_app\]

 \(Available in the ServiceNow Store\)

</td><td>

Offers the service mapping functionality enhanced with Machine Learning.

</td><td>

Inactive

</td><td>

false

</td><td>

com.snc.service-mapping

</td></tr><tr id="plugin_com.snc.cmdb.service.modeling" class="plugin_reference"><td class="name">

Service Modeling\[com.snc.cmdb.service.modeling\]

</td><td class="description">

Core infrastructure for Service Modeling used in Service Mapping and Delivery.

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

-   com.glide.vars
-   com.snc.cmdb.enterprise

</td></tr><tr><td>

Service Portal Analytics\[com.glide.service-portal.analytics\]

</td><td>

User Experience Analytics for Service Portal provides dashboard views for monitoring the key performance indicators \(KPIs\) of web applications built on Service Portal. You can use these insights to optimize your portal.

</td><td>

Active

</td><td>

false

</td><td>

com.glide.appsee

</td></tr><tr><td>

Service Portfolio Management Foundation Demo Data\[com.snc.service\_portfolio.demo\_data\]

</td><td>

Adds Demo Data for Service Portfolio Management Foundation and SLA Commitments. If you installed the SPM SLA Commitments plugin before New York, this activates the newer version.

</td><td>

Active

</td><td>

true

</td><td>

-   com.snc.service\_portfolio
-   com.snc.service\_portfolio.sla\_commitment

</td></tr><tr><td>

Service Request Criteria\[com.sn\_req\_criteria\]

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td class="name">

ServiceNow Add-Ins for Microsoft Office\[com.sn\_outlook\_addin\]

</td><td class="description">

Enables users to interact with ServiceNow from within Microsoft Office

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

-   com.snc.platform.security.oauth
-   com.glide.ui.vtb
-   com.glideapp.servicecatalog
-   com.glide.service-poortal

</td></tr><tr><td>

ServiceNow Application Repository\[com.snc.apprepo\]

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

ServiceNow Antivirus Program\[com.glide.snap\]

</td><td>

ServiceNow Antivirus Program

</td><td>

Active

</td><td>

false

</td><td>

 

</td></tr><tr><td>

ServiceNow Certificate Inventory and Management\[com.sn\_disco\_certmgmt\]

</td><td>

Automatically track certificates, provide awareness of upcoming expirations, and drive the workflow to renew them.

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

ServiceNow Cloud Encryption\[com.glide.platform.cloud\_encryption\]

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

ServiceNow Document Viewer\[com.snc.documentviewer\]

</td><td>

Document viewer is a platform feature that will enable users to view enterprise class documents inline within the platform attachment instead of downloading it to the local device and then opening the documents with a locally installed viewer.

</td><td>

Active

</td><td>

false

</td><td>

com.snc.apppdfgenerator

</td></tr><tr><td>

ServiceNow Flow Designer - Dynamic Inputs\[com.glide.hub.dynamic\_inputs\]

</td><td>

Enable flow designers to configure an action using input values that have been dynamically created. During flow design, when you add an action with dynamic inputs to a flow, it calls a data gathering action to collect data and dynamically shows choices based on that returned data. Use dynamic inputs to look up and display choices dynamically rather than using hard-coded options. For example, you can use a dynamic input to generate choices for a spoke integration.

</td><td>

Inactive

</td><td>

false

</td><td>

 

</td></tr><tr><td>

ServiceNow Flow Designer - Dynamic Outputs\[com.glide.hub.dynamic\_outputs\]

</td><td>

Enable flow designers to configure an action using output values that have been dynamically created. During flow design, when you add an action with dynamic outputs to a flow, it calls a data gathering action to create a complex object. Use dynamic outputs to create a complex object with a dynamic structure rather than creating a hard-coded object with a static structure. For example, you can use a dynamic output to generate a complex object for a spoke integration.

</td><td>

Inactive

</td><td>

false

</td><td>

 

</td></tr><tr><td>

ServiceNow Flow Designer - Introspection\[com.glide.hub.flow\_designer\_introspection\]

</td><td>

Enables the use of Dynamic Inputs and Dynamic Outputs for Actions, Subflows and Flows in Flow Designer.

</td><td>

Inactive

</td><td>

false

</td><td class="requires">

-   com.glide.hub.dynamic\_inputs
-   com.glide.hub.dynamic\_outputs

</td></tr><tr><td>

ServiceNow IntegrationHub Action Step - MFT\[com.glide.hub.action\_step.mft\]

</td><td>

Provides capabilities to copy directory using the SFTP step.

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

ServiceNow IntegrationHub Action Template - Data Streaming\[com.glide.hub.action\_type.datastream\]

</td><td>

Activates Data Stream actions in Flow Designer, enabling you to send REST or SOAP requests from Flow Designer to APIs that return a stream of response data larger than 10 MB. Parse stream data into a series of complex object outputs and use the data pills in other actions in a flow.

</td><td>

Inactive

</td><td>

false

</td><td>

com.glide.hub.action\_step.template

</td></tr><tr><td>

ServiceNow IntegrationHub Action Step - RTE\[com.glide.hub.action\_step.rte\]

</td><td>

Action Step - RTE.

</td><td>

 

</td><td>

false

</td><td>

com.glide.hub.action\_step.template

</td></tr><tr><td>

ServiceNow IntegrationHub Action Step - SFTP\[com.glide.hub.action\_step.sftp\]

</td><td>

Provides an SSH File Transfer Protocol step to create a reusable action that can access, transfer, or manage files.

</td><td>

Inactive

</td><td>

false

</td><td>

com.glide.hub.action\_step.template

</td></tr><tr><td>

ServiceNow IntegrationHub Enterprise Pack Installer\[com.glide.hub.integrations.enterprise\]

</td><td>

Installs IntegrationHub enterprise pack to automate human resources, customer relationship management, enterprise resource planning, and more. Includes IntegrationHub professional pack, Microsoft SCCM spoke, and Data Stream actions.

</td><td>

 

</td><td>

false

</td><td class="requires">

-   com.glide.hub.integrations.professional
-   com.sn.sccm.spoke

</td></tr><tr><td>

ServiceNow IntegrationHub Professional Pack Installer\[com.glide.hub.integrations.professional\]

</td><td>

Installs IntegrationHub professional pack plugins to automate IT operations. Includes IntegrationHub standard pack, Microsoft AD spoke, Microsoft Azure AD spoke, and SSH and Powershell steps.

</td><td>

 

</td><td>

false

</td><td class="requires">

-   com.glide.hub.integrations.standard
-   com.glide.hub.action\_step.powershell
-   com.sn.ad.spoke
-   com.sn.azure\_ad.spoke
-   com.glide.hub.action\_step.ssh

</td></tr><tr><td>

ServiceNow IntegrationHub Standard Pack Installer\[com.glide.hub.integrations.standard\]

</td><td>

Installs IntegrationHub standard pack plugins to automate developer operations. Includes IntegrationHub starter pack, and JDBC and XML parser steps.

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

ServiceNow IntegrationHub Starter Pack Installer\[com.glide.hub.integrations.starter\]

</td><td>

Installs IntegrationHub starter pack plugins to build your own integrations. Includes HipChat spoke, Microsoft Teams spoke, Slack spoke, Slack webhooks spoke, eBonding spoke, legacy IntegrationHub usage dashboard, and REST and SOAP steps.

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

ServiceNow ITOM Licensing\[com.sn\_itom\_licensing\]

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

ServiceNow Language Detection Service Spoke\[com.glide.language\_detection\_spoke\]

</td><td>

Using ServiceNow Language Detection service, it adds ability to detect the language of given text.

</td><td>

Active

</td><td>

false

</td><td>

-   com.glide.hub
-   com.glide.hub.integration.runtime

</td></tr><tr><td>

ServiceNow Mobile Request - My Request Filter\[com.glideapp.servicecatalog.mobile-request-filter\]

</td><td>

This plugin contains the configuration and records that are used in the Now Mobile app. Do not activate this plugin directly. Activating com.glide.mobile-employee will activate this plugin for you.

</td><td>

Inactive

</td><td>

false

</td><td>

 

</td></tr><tr><td>

ServiceNow Studio\[sn\_sns\]

</td><td>

ServiceNow Studio provides a unified experience for all ServiceNow development activities.

</td><td>

Active

</td><td>

false

</td><td>

-   sn\_udc
-   sn\_studio\_commons
-   sn\_app\_obj\_wizards
-   sn\_deploy\_pipeline

</td></tr><tr><td class="name">

ServiceNow Subscription Management\[com.snc.usage\_admin.snc\]

</td><td class="description">

ServiceNow Subscription Management.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

com.snc.usage\_admin.base

</td></tr><tr><td>

Service Owner Workspace \(Maintenance mode only\)\[com.spm\_owner\_workspace\]

</td><td>

Provides a premium Service Portfolio Management experience. Portfolio managers and service owners access an integrated and graphically intuitive user interface to manage and monitor portfolios and services.

</td><td>

Inactive

</td><td>

false

</td><td class="requires">

-   com.snc.pa.premium
-   com.snc.spm
-   com.snc.spm.spend
-   com.snc.service\_workspace

</td></tr><tr><td>

Service Portal Agent Chat\[com.glide.service-portal.agent-chat\]

</td><td>

This plugin brings Agent Chat to Service Portal.

</td><td>

Inactive

</td><td>

false

</td><td class="requires">

-   com.glide.cs
-   com.glide.cs.sn-va-web-client-app

</td></tr><tr><td>

Service Portal - Core\[com.glide.service-portal\]

</td><td>

Service Portal is a portal framework that allows administrators to build a mobile-friendly self service experience for users.

</td><td>

Active

</td><td>

false

</td><td class="requires">

-   com.glide.ui.web\_db\_types
-   com.glide.ui.angularui
-   com.glide.ui.ng.filter
-   com.glide.ui.spectrum
-   com.glide.ui.m
-   com.glide.connect
-   com.glide.ui.scss
-   com.glide.ui.scss.bootstrap
-   com.glide.service-portal.designer
-   com.glide.automated\_testing\_impl.service\_portal

</td></tr><tr><td>

Service Portal - Knowledge Base\[com.glide.service-portal.knowledge-base\]

</td><td>

Knowledge base for SP

</td><td>

Active

</td><td>

false

</td><td>

 

</td></tr><tr><td>

Service Portal La Jolla Brand Update\[com.glide.service-portal.themes.la-jolla\]

</td><td>

Updates your /sp and /sp\_config portals with the ServiceNow La Jolla branding. The logo, favicon, login page background image, hero banner, theme, and widget instance options are updated when the portal record has not been modified. When the portal record is modified no changes are made and an administrator can manually apply changes by downloading the La Jolla images from the db\_image table and applying as well as updating the theme setting of the portal record.

</td><td>

Active

</td><td>

false

</td><td>

com.glide.service-portal

</td></tr><tr><td>

Service Portal - Service Catalog\[com.glide.service-portal.service-catalog\]

</td><td>

Enables Service Catalog widgets for Service Portal.

</td><td>

Active

</td><td>

false

</td><td>

No

</td></tr><tr><td>

Service Portal - Service Catalog v2\[com.glideapp.servicecatalog.portal\]

</td><td>

Enables Service Catalog widgets for Service Portal.

</td><td>

Active

</td><td>

false

</td><td>

No

</td></tr><tr><td>

Service Organization\[com.snc.service\_organization\]

</td><td>

Provides the base framework to support any internal or external entity involved in the customer service value chain. E.g. Branches, Stores, Franchises, Institutions.

</td><td>

Active

</td><td>

false

</td><td>

 

</td></tr><tr id="plugin_com.glide.service-portal.service-status" class="plugin_reference"><td class="name">

Service Portal - Service Status\[com.glide.service-portal.service-status\]

</td><td class="description">

Service Status gives information on current, planned, and historical outages for Business Services so they do not have to call your Service Desk. Loading demo data randomly generates 90 days of outages for 19 demo data Business Services.

</td><td>

Active

</td><td class="has_demo_data">

true

</td><td class="requires">

com.glide.service-portal

</td></tr><tr><td class="name">

Service Portal Announcements\[com.glide.service-portal.announcements\]

</td><td class="description">

Enables administrators to broadcast announcements to Service Portal users.

</td><td>

Active

</td><td class="has demo data">

true

</td><td>

 

</td></tr><tr><td class="name">

Service Portal Configuration Pages\[com.glide.service-portal.config\]

</td><td class="description">

Service Portal Configuration Pages.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

com.glide.service-portal

</td></tr><tr id="plugin_com.glide.service-portal.designer" class="plugin_reference"><td class="name">

Service Portal Designer\[com.glide.service-portal.designer\]

</td><td class="description">

Drag-and-drop wysiwyg portal designer

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

com.glide.service-portal

</td></tr><tr id="plugin_com.glide.service-portal.esm" class="plugin_reference"><td class="name">

Service Portal for Enterprise Service Management\[com.glide.service-portal.esm\]

</td><td class="description">

Provides a default service portal with easy configuration and designer. End-user resources include Knowledge Base, Service Catalog, and Services Status.

</td><td>

Active

</td><td class="has_demo_data">

true

</td><td class="requires">

-   com.glide.service-portal
-   com.glide.service-portal.service-status
-   com.glide.service-portal.sqanda

</td></tr><tr><td>

Service Portal La Jolla Brand Update\[com.glide.service-portal.themes.la-jolla\]

</td><td>

This plugin updates your /sp and /sp\_config portals with the ServiceNow La Jolla branding. If the portal record has not been modified, the logo, favicon, login page background image, hero banner, theme, and widget instance options are updated.

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Service Portal Surveys\[com.glide.service-portal.survey\]

</td><td>

Service Portal Surveys and Assessments.

</td><td>

Active

</td><td>

false

</td><td>

 

</td></tr><tr><td>

Service Portal User Criteria Support\[com.glide.service-portal.user-criteria\]

</td><td>

Enables Service Portal User Criteria support. Installing this plugin will create new user criteria records for each of your widgets and pages that already have role-based permissions on them.

</td><td>

Inactive

</td><td class="has demo data">

false

</td><td class="requires">

-   com.glide.service-portal
-   com.glideapp.user\_criteria

</td></tr><tr id="plugin_com.snc.service_portfolio" class="plugin_reference"><td class="name">

Service Portfolio Management Foundation\[com.snc.service\_portfolio\]

</td><td class="description">

Allows an organization to document the business services it provides using a standardized, structured format. Performance against availability commitments is calculated and can be displayed in a homepage.

</td><td>

Inactive

</td><td class="has_demo_data">

true

</td><td class="requires">

-   com.snc.service\_portfolio\_core
-   com.glideapp.servicecatalog
-   com.glideapp.summary\_report\_engine

</td></tr><tr><td>

Service Portfolio Management Core\[com.snc.service\_portfolio\_core\]

</td><td>

This plugin contains core functionality for Service Portfolio Management available out of the box by default.

</td><td>

Inactive

</td><td>

false

</td><td>

com.snc.cmdb

</td></tr><tr><td>

Service Portfolio Management Premium\[com.snc.spm\]

</td><td>

Collects service offering metrics and allows for roll-up calculations to parent services and taxonomy nodes for performance scores and other metrics as viewed via the Service Owner Workspace plugin.

</td><td>

Inactive

</td><td>

false

</td><td class="requires">

-   com.snc.pa.premium
-   com.snc.service\_portfolio
-   com.snc.service\_portfolio.sla\_commitment
-   com.snc.task\_outage

</td></tr><tr><td>

Service Portfolio Management Estimated Spend\[com.snc.spm.spend\]

</td><td>

Collects service offering cost and allows for selection between local model and Financial Management model.

</td><td>

Inactive

</td><td>

false

</td><td>

com.snc.spm

</td></tr><tr id="plugin_com.snc.service_portfolio.sla" class="plugin_reference"><td class="name">

Service Portfolio Management SLA Commitments\[com.snc.service\_portfolio.sla\_commitment\]

</td><td class="description">

Allows commitments to be defined by an SLA, so that staff can track how efficiently the service desk meets commitments for a service offering.

</td><td>

Active

</td><td class="has_demo_data">

true

</td><td class="requires">

-   com.snc.service\_portfolio
-   com.snc.sla

</td></tr><tr><td>

Service Workspace\[com.snc.service\_workspace\]

</td><td>

Service Workspace application.

</td><td>

Inactive

</td><td>

false

</td><td>

com.workspace\_core

</td></tr><tr id="plugin_com.glide.sessiondebug" class="plugin_reference"><td class="name">

SessionDebug\[com.glide.sessiondebug\]

</td><td class="description">

Provides SessionDebug statements and filtering.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

 

</td></tr><tr><td>

Shift Planning \(Maintenance mode only\)\[com.sn\_shift\_planning\]

</td><td>

Shift Planning plugin. Plan team schedules, shifts and workflows for managing timeoffs and shift swaps requests.

</td><td>

Active

</td><td>

false

</td><td>

 

</td></tr><tr><td>

Shift Planning\[com.sn\_shift\_planning\_host\]

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Shodan Exploit Integration\[sn\_vul\_shodan\]

 \(Available in the ServiceNow Store\)

</td><td>

Provides the ability to integrate the ServiceNow Vulnerability Response application with the Shodan product. Activation of this plugin on production instances may require a separate license. Contact ServiceNow for details.

</td><td>

 

</td><td>

false

</td><td>

sn\_vul

</td></tr><tr><td>

ShoppingHub\[com.snc.sn\_shop\]

\(Starting with the Tokyo release, ShoppingHub is renamed as Procurement Common Architecture.\)

\(Starting with the Utah release, Procurement Common Architecture is renamed as Source-to-Pay Common Architecture.\)

\(Available in the ServiceNow Store\)

</td><td>

Provides an architecture to store purchase orders, requisitions, sourcing requests, and other objects that are commonly used across the source-to-pay business processes.

</td><td>

Inactive

</td><td>

true

</td><td>

-   com.sn\_fin
-   com.sn\_spend\_sdc

</td></tr><tr><td>

Shopping Hub\[com.snc.sn\_spend\_uib\]

\(Available in the ServiceNow Store\)

</td><td>

Provides a streamlined, e-commerce like experience for employees to self-service requests, and source or purchase products and services through the procurement organization. This is an add-on experience to Employee Center.

</td><td>

Inactive

</td><td>

false

</td><td>

-   com.sn\_pr
-   com.sn\_cmn\_uib\_comp

</td></tr><tr><td>

ShoppingHub Mobile\[com.sn\_shop\_mobile\]

\(Starting with the Utah release, ShoppingHub Mobile is renamed as Shopping Hub Mobile.\)

\(Available in the ServiceNow Store\)

</td><td>

Enables Shopping Hub and other employee experiences for procurement to be enabled within the Now Mobile application.

</td><td>

Inactive

</td><td>

false

</td><td>

-   com.glide.sg
-   com.snc.sn\_pr
-   com.glide.sg.agent\_native\_client

</td></tr><tr><td>

Sidebar Server\[com.glide.cs.collab\]

 \(New in Tokyo\)

</td><td>

A server for the Sidebar feature.

</td><td>

active

</td><td>

false

</td><td>

-   com.glide.cs
-   com.glide.cs.custom.adapter
-   com.glide.quickactions

</td></tr><tr id="plugin_com.snc.signaturepad" class="plugin_reference"><td class="name">

Signature Pad\[com.snc.signaturepad\]

</td><td class="description">

Provides a tool to allow a digital signature in a .pdf document. The Human Resources application uses this with various documents.

 Activation of this plugin on production instances may require a separate license. Contact ServiceNow for details.

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

com.glide.db\_images

</td></tr><tr><td>

Sitemap Generator\[sn\_ux\_seo\_sitemap\]

 \(Available in the ServiceNow Store\)

</td><td>

Helps you to define and automatically generate XML sitemaps to improve search engine optimization of your public portal pages.

</td><td>

Inactive

</td><td>

false

</td><td>

-   com.glide.scope.access.restricted\_caller
-   com.glide.hub.integration.runtime
-   com.glide.hub.action\_step.rest
-   com.glide.hub.action\_step.script

</td></tr><tr><td>

Skill Determination\[com.snc.skill\_determination\]

</td><td>

Automatically determine and assign skills for work items.

</td><td>

Active

</td><td>

false

</td><td>

com.snc.skills\_management

</td></tr><tr id="plugin_com.snc.skills_management" class="plugin_reference"><td class="name">

Skills Management\[com.snc.skills\_management\]

</td><td class="description">

The Skills Management application enables you to organize skills data of service agents and employees in a centralized location. You can use this data to assign tasks based on skills, analyze skill gaps to identify coaching and training needs, optimize your workforce, create career growth plans, and perform skill-based hiring.

</td><td>

Inactive

</td><td class="has_demo_data">

true

</td><td class="requires">

 

</td></tr><tr><td>

Skill Recommendation \[com.snc.sre\]

\(Maintenance mode only\)

</td><td>

Skill Recommendation - ML prediction model and workflow to recommend and assign skills to agents

</td><td>

Active

</td><td>

false

</td><td class="requires">

-   com.snc.skills\_management
-   com.glide.platform\_ml

</td></tr><tr><td>

Skills Library Data for Skills Management\[com.snc.skills\_management.seed\_data\]

</td><td>

Provides a library of skill categories and skills that you can start using for quick on-boarding.

</td><td>

Active

</td><td>

true

</td><td>

com.snc.skills\_management

</td></tr><tr><td>

SLA Breakdowns\[com.snc.sla.breakdowns\]

</td><td>

Provides the ability to generate breakdown data for each Task SLA record. For example, you can generate breakdown data on the basis of the **Assignment group** and **Assigned to** fields.

**Note:** You need to have up-to-date versions of script includes TaskSLAController and RepairTaskSLAController before activating this plugin to ensure that breakdown data is generated correctly. If you have customized versions of the script includes TaskSLAController and RepairTaskSLAController, you need to incorporate all customizations into the versions of these files from the most recent upgrade.

</td><td>

Active

</td><td>

false

</td><td>

com.snc.sla

</td></tr><tr id="plugin_com.snc.sla.timeline" class="plugin_reference"><td class="name">

SLA Timeline\[com.snc.sla.timeline\]

</td><td class="description">

Provides the ability to view an SLA in a timeline.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

 

</td></tr><tr id="plugin_com.snc.planned_maintenance" class="plugin_reference"><td class="name">

SM Planned Maintenance\[com.snc.planned\_maintenance\]

</td><td class="description">

Allows setup and configuration for repeating and triggered requests. Activation of this plugin on production instances may require a separate license. Contact ServiceNow for details.

</td><td>

Inactive

</td><td class="has_demo_data">

true

</td><td class="requires">

com.snc.service\_management.core

</td></tr><tr><td>

SMS Preferences\[com.snc.sms\_pref\]

</td><td>

Provides ability to set SMS preferences for receiving messages from different providers.

</td><td>

Inactive

</td><td>

false

</td><td>

 

</td></tr><tr><td>

sn-custom-tinymce-scoped-app\[com.sn-custom-tinymce-scoped-app\]

</td><td>

Scoped app providing custom tinymce build

</td><td>

Inactive

</td><td>

false

</td><td>

 

</td></tr><tr><td>

sn-openframe-uxb\[com.devsnc\_sn\_openframe\_uxb\]

</td><td>

Openframe component.

</td><td>

Active

</td><td>

false

</td><td>

-   com.glide.uxbuilder
-   com.servicenow\_behavior\_key\_binding
-   com.servicenow\_sass\_generic
-   com.servicenow\_sass\_global
-   com.servicenow\_now\_legacy\_icon
-   com.servicenow\_ui\_core
-   com.servicenow\_ui\_effect\_graphql
-   com.servicenow\_ui\_effect\_amb
-   com.servicenow\_ui\_effect\_http
-   com.servicenow\_ui\_effect\_update\_state
-   com.servicenow\_ui\_renderer\_snabbdom
-   com.sn\_seismic\_post\_message
-   com.sn\_uxpage\_presource
-   com.sn\_translate
-   com.devsnc\_library\_enhanced\_test
-   com.devsnc\_library\_uxf
-   com.servicenow\_behavior\_rtl

</td></tr><tr id="plugin_com.glide.snc_code_editor" class="plugin_reference"><td class="name">

SNC Code Editor\[com.glide.snc\_code\_editor\]

</td><td class="description">

 

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

 

</td></tr><tr><td>

sn-process-automation-designer\[com.sn\_process\_automation\_designer\]

</td><td>

This plugin is the Process Automation Designer application

</td><td>

Active

</td><td>

false

</td><td class="requires">

-   com.glide.uxbuilder
-   com.devsnc\_sn\_glide\_form\_controls
-   com.devsnc\_sn\_record\_input
-   com.servicenow\_now\_alert
-   com.servicenow\_now\_button
-   com.servicenow\_now\_card
-   com.servicenow\_now\_dropdown
-   com.servicenow\_now\_heading
-   com.servicenow\_now\_icon
-   com.servicenow\_now\_label\_value
-   com.servicenow\_now\_modal
-   com.servicenow\_now\_record\_list\_connected
-   com.servicenow\_now\_text\_link
-   com.servicenow\_now\_radio\_buttons
-   com.servicenow\_now\_visual\_board
-   com.servicenow\_sass\_generic
-   com.servicenow\_sass\_global
-   com.servicenow\_ui\_core
-   com.servicenow\_ui\_effect\_graphql
-   com.servicenow\_ui\_effect\_helpers
-   com.servicenow\_ui\_effect\_http
-   com.servicenow\_ui\_enzyme\_adapter
-   com.servicenow\_ui\_renderer\_snabbdom
-   com.sn\_component\_error\_handler
-   com.sn\_pd\_picker
-   com.sn\_uxpage\_presource

</td></tr><tr><td>

sn-ui-builder\[com.sn\_ui\_builder\]

</td><td>

UI Builder is an enjoyable, easy to use builder for creating UIs at ServiceNow.

</td><td>

Active

</td><td>

false

</td><td class="requires">

-   com.glide.uxbuilder
-   com.servicenow\_behavior\_focus
-   @servicenow/now-alert
-   @servicenow/now-modal
-   @servicenow/now-text-link
-   sn-devx-components
-   com.sn\_http\_request
-   com.sn\_translate
-   sn-ui-builder-components
-   sn-uxf-builder-middleware

</td></tr><tr><td>

Software Asset Management Machine Learning Normalization\[com.sn\_sam\_ml\_normalization\]

</td><td>

Provides core capabilities to normalize unrecognized discovered software using machine learning. Requires Software Asset Management Enterprise.

</td><td>

 

</td><td>

false

</td><td>

-   com.snc.samp
-   com.glide.platform\_ml

</td></tr><tr><td>

Software Asset Workspace\[com.sn\_sam\_workspace\]

</td><td>

Enables the Software Asset Management \(SAM\) capabilities in workspace.

</td><td>

 

</td><td>

false

</td><td>

-   com.snc.app\_shell\_aw
-   com.snc.uib.base\_agent\_workspace
-   com.sn\_itam\_card
-   com.snc.sams

</td></tr><tr id="plugin_com.snc.sdlc" class="plugin_reference"><td class="name">

Software Development Lifecycle \(SDLC\)\[com.snc.sdlc\]

</td><td class="description">

Extends the Release Management v2 plugin by adding some new structures to accommodate the software development life cycle. This plugin is designed to accommodate most non-agile development methodologies, including the common waterfall method of development.

</td><td>

Inactive

</td><td class="has_demo_data">

true

</td><td class="requires">

com.snc.release\_management\_v2

</td></tr><tr><td>

Source-to-Pay Workspace\[com.sn\_spend\_workspace\]

\(Available in the ServiceNow Store\)

</td><td>

Provides a single environment for Procurement Specialists to work on purchase requisitions, sourcing requests, negotiations, procurement requests, and more.

</td><td>

Inactive

</td><td>

false

</td><td>

com.snc.uib.sn\_dyn\_rel\_rec

</td></tr><tr id="plugin_com.sn_shn" class="plugin_reference"><td class="name">

Special Handling Notes\[com.sn\_shn\]

</td><td class="description">

Special Handling Notes.

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

 

</td></tr><tr id="plugin_com.snc.shn_demo" class="plugin_reference"><td class="name">

Special Handling Notes Demo Data\[com.snc.shn\_demo\]

</td><td class="description">

Special Handling Notes application demo data.

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

-   com.sn\_shn
-   com.snc.customerservice.demo

</td></tr><tr id="plugin_com.snc.state_flows" class="plugin_reference"><td class="name">

State Flows\[com.snc.state\_flows\]

</td><td class="description">

Enables advanced users to customize the state flow of any task table that uses states.

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

 

</td></tr><tr><td>

State Transition Models\[com.snc.itsm.state\_transition\_model\]

</td><td>

State Transition Models allow flexible configuration of state and transition models.

</td><td>

Active

</td><td>

false

</td><td>

 

</td></tr><tr><td>

State Transition Models - Foundation Data\[com.snc.itsm.state\_transition\_model.foundation\]

</td><td>

Foundation data for State Transition Models, including State transition conditions.

</td><td>

Active

</td><td>

false

</td><td>

com.snc.itsm.state\_transition\_model

</td></tr><tr id="plugin_com.glide.db.query_stats" class="plugin_reference"><td class="name">

Stats Tools\[com.glide.db.query\_stats\]

</td><td class="description">

Records statistics for system activities that affect performance. Query, Script, and Transaction stats, database performance tuning tools.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

com.glide.monitor.round\_robin\_database

</td></tr><tr><td>

Strategic Planning\[sn\_apw\_advanced\]

</td><td>

Helps to prioritize all work, align goals, visually roadmap, and track progress when using Agile, waterfall, or hybrid approaches.

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Strategic Spend Tracking for PPM\[sn\_ppm\_sst\]

 \(Available in the ServiceNow Store\)

</td><td>

Evaluate strategic value of your projects and demands.

</td><td>

Active

</td><td>

True

</td><td>

com.snc.financial\_planning\_pmo

</td></tr><tr id="plugin_com.glide.dev-studio" class="plugin_reference"><td class="name">

Studio\[com.glide.dev-studio\]

</td><td class="description">

Allows developers to add and update application files.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

-   com.glide.code-search
-   com.sn\_appcreator

</td></tr><tr id="plugin_com.snc.usage_admin.base" class="plugin_reference"><td class="name">

Subscription Administration Base\[com.snc.usage\_admin.base\]

</td><td class="description">

Subscription Administration Base.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

com.glide.subscription\_framework

</td></tr><tr id="plugin_com.glide.notification" class="plugin_reference"><td class="name">

Subscription Based Notifications\[com.glide.notification\]

</td><td class="description">

Allows users to subscribe to notifications on a task or CI without being on the watchlist or being one of the assigned users.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

-   com.glide.ui\_policy
-   com.glide.email\_notification\_preview

</td></tr><tr id="plugin_com.glide.notification.subscription" class="plugin_reference"><td class="name">

Subscription Based Notifications 2.0\[com.glide.notification.subscription\]

</td><td class="description">

The notification subscription model - improved and simplified.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

com.glide.notification

</td></tr><tr id="plugin_com.glide.subscription_framework" class="plugin_reference"><td class="name">

Subscription Management and Enforcement Framework\[com.glide.subscription\_framework\]

</td><td class="description">

Subscription Management and Enforcement Framework.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

com.glide.usageanalytics

</td></tr><tr><td class="name">

Subscriptions and Activity Feed Framework\[com.snc.activity\_subscriptions\]

</td><td class="description">

This plugin provides a generic set of artifacts to handle subscriptions for any defined subscribable object. Any entity can be defined as a subscribable object and a set of subscribers can subscribe to the objects. When a event occurs related to the subscribable object, activities can be tracked and subscribers can be notified.

</td><td>

Inactive

</td><td class="has_demo_data">

true

</td><td class="requires">

 

</td></tr><tr><td>

Success Indicators\[com.snc.vendor.insights\]

</td><td>

Leverages odds ratio and ML capabilities for apps like Vendor Manager Workspace, etc.

</td><td>

Active

</td><td>

false

</td><td>

 

</td></tr><tr><td>

Supplier Collaboration Portal\[com.snc.sn\_supplier\_sp\]

\(Available in the ServiceNow Store\)

</td><td>

Provides a single, one-stop experience for suppliers to get self-service, complete tasks and make requests into an organization.

</td><td>

Inactive

</td><td>

true

</td><td>

-   Supplier Common Architecture \(com.snc.sn\_slm\)
-   Service Portal \(com.glide.service-portal\)
-   E-signature \(com.snc.esign\)
-   Employee Center \(com.snc.employee\_center\)

</td></tr><tr><td>

Supplier Common Architecture\[com.snc.sn\_slm\]

\(Available in the ServiceNow Store\)

</td><td>

Provides a common architecture to track data objects related to a supplier used in both Supplier Lifecycle Operations and Supplier Collaboration Portal.

</td><td>

Inactive

</td><td>

false

</td><td>

-   Finance Common Architecture \(com.sn\_fin\)
-   Service Delivery Common \(com.sn\_spend\_sdc\)
-   Document Management \(com.snc.platform\_document\_management\)
-   External User Registration \(com.snc.external\_user\_self\_registration\)
-   Common Vendor Core \(com.snc.sn\_vendor\_core\) and \(com.snc.vendor\_core\)

</td></tr><tr><td>

Supplier Lifecycle Operations\[com.snc.sn\_supplier\_mgmt\]

\(Available in the ServiceNow Store\)

</td><td>

Collaborate with suppliers, manage supplier relationships, monitor risk, compliance, and performance across the supplier life cycle.

</td><td>

Inactive

</td><td>

true

</td><td>

-   Supplier Common Architecture \(com.snc.sn\_slm\)
-   Playbook Experience \(com.playbook\_experience\)
-   Employee Experience Foundation \(com.snc.sn\_ex\_emp\_fd\)
-   News Integration for Supplier Lifecycle Operations \(com.snc.sn\_supplier\_news\)
-   Map UI Component for threat and alert data feeds \(com.sn\_fam\_map\)

</td></tr><tr><td>

Supplier Lifecycle Operations Integration with SAP\[sn\_slm\_sap\_int\]

\(Available in the ServiceNow Store\)

</td><td>

Send suppliers created in Supplier Lifecycle Operations to SAP ECC and SAP S4 HANA.

</td><td>

Inactive

</td><td>

false

</td><td>

-   Finance Common Architecture \(com.sn\_fin\)
-   Finance – ERP Integration \(com.sn\_fcms\_integrations\)
-   Primary Data Integration with SAP \(sn\_sap\_data\_int\)

</td></tr><tr id="plugin_com.glide.survey_designer" class="plugin_reference"><td class="name">

Survey Designer\[com.glide.survey\_designer\]

</td><td class="description">

Activates survey designer that is a drag-and-drop interface to create surveys.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

com.glide.assessment\_designer.common

</td></tr><tr id="plugin_com.glide.syntax_editor" class="plugin_reference"><td class="name">

Syntax Editor\[com.glide.syntax\_editor\]

</td><td class="description">

 

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

com.glide.snc\_code\_editor

</td></tr><tr id="plugin_com.snc.apps" class="plugin_reference"><td class="name">

System Applications Core\[com.snc.apps\]

</td><td class="description">

Core applications development.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

com.snc.apps\_picker

</td></tr><tr id="plugin_com.snc.apps_complete" class="plugin_reference"><td class="name">

System Applications Support\[com.snc.apps\_complete\]

</td><td class="description">

Provides support for creating and managing applications.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

-   com.snc.apps
-   com.snc.apps\_picker
-   com.snc.apps\_access
-   com.snc.apps\_file
-   com.snc.apps\_hub
-   com.snc.apps\_legacy
-   com.snc.metadata
-   com.snc.metadata\_tree
-   com.snc.apps\_creator
-   com.glide.sessiondebug
-   com.glide.autorecovery
-   com.glide.transaction\_scope
-   com.glide.ui.mergetool
-   com.glide.ui.relationship\_layout

</td></tr><tr id="plugin_com.glide.system_import_set" class="plugin_reference"><td class="name">

System Import Sets\[com.glide.system\_import\_set\]

</td><td class="description">

Provides the functionality for import sets.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

-   com.snc.automation
-   com.glide.ui\_policy
-   com.glide.system\_import\_data\_source

</td></tr><tr id="plugin_com.glide.system_update_set_picker" class="plugin_reference"><td class="name">

System Update Set Picker\[com.glide.system\_update\_set\_picker\]

</td><td class="description">

Allows users to choose an update set for tracking customizations.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

com.glide.system\_update\_set

</td></tr><tr id="plugin_com.glide.local_update_set" class="plugin_reference"><td class="name">

System Update Sets \(viewer\)\[com.glide.local\_update\_set\]

</td><td class="description">

Provides useful descriptions for update set entries and supports viewing contents of update sets.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

 

</td></tr><tr id="plugin_com.glide.system_update_set" class="plugin_reference"><td class="name">

System Update Sets \(with remote update set support\)\[com.glide.system\_update\_set\]

</td><td class="description">

Facilitates moving customizations between systems. Supports viewing contents of update sets.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

-   com.snc.apps\_hub
-   com.glide.system\_update\_set\_picker
-   com.glide.system\_update\_set\_preview

</td></tr><tr id="plugin_com.glide.system_update_set_preview" class="plugin_reference"><td class="name">

System Update Sets Preview\[com.glide.system\_update\_set\_preview\]

</td><td class="description">

Allows users to preview the changes that are performed by an update set and predict whether there will be any collisions in attempting to apply the update set.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

com.glide.system\_update\_set

</td></tr><tr id="plugin_com.glide.web_service_application" class="plugin_reference"><td class="name">

System Web Services\[com.glide.web\_service\_application\]

</td><td class="description">

Provides a series of web service import sets.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

-   com.glide.web\_service\_provider
-   com.glide.web\_service\_import\_sets
-   com.snc.web\_service\_import\_set\_tables

</td></tr><tr id="plugin_com.glide.ui.tablet" class="plugin_reference"><td class="name">

Tablet Device Support - iPad with iOS 6+\[com.glide.ui.tablet\]

</td><td class="description">

Provides a UI supporting nearly full-product functionality on the Apple iPad.

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

-   com.glide.context\_help
-   com.glide.ui.font\_icons
-   com.glide.ui.tablet.theme

</td></tr><tr><td>

Tag Data Governance\[com.sn\_itom\_tag\]

 \(Maintenance mode only\)

</td><td>

This store application\(beta\) provides customers a way to get their cloud resources tagged per enterprise norms, in order to improve return on investments.

</td><td>

Active

</td><td>

false

</td><td>

 

</td></tr><tr><td>

Tag Governance\[sn\_itom\_tag\]

 \(Available in the ServiceNow Store\)

</td><td>

Use the application to identify on-premises or cloud resources that are inconsistent and don't comply with the tag policies of your organization. When covered by the ITOM Governance subscription, you can also fix tag compliance issues. Use remediation scripts to add or modify cloud tags.

</td><td>

Active

</td><td>

false

</td><td>

-   com.snc.discovery
-   com.snc.itom.vis.license
-   com.glide.hub.integrations
-   sn\_cai

</td></tr><tr id="plugin_com.sn_publications" class="plugin_reference"><td class="name">

Targeted Communications\[com.sn\_publications\]

</td><td class="description">

Provides a way to publish and send out newsletter like articles to targeted internal/external customers.

</td><td>

Inactive

</td><td class="has_demo_data">

true

</td><td class="requires">

com.snc.cs\_base

</td></tr><tr id="plugin_com.snc.publications_demo" class="plugin_reference"><td class="name">

Targeted Communications Demo Data\[com.snc.publications\_demo\]

</td><td class="description">

Targeted Communications application demo data.

</td><td>

Inactive

</td><td class="has_demo_data">

true

</td><td class="requires">

com.sn\_publications

</td></tr><tr id="plugin_com.snc.task_activity" class="plugin_reference"><td class="name">

Task Activities\[com.snc.task\_activity\]

</td><td class="description">

Enables support for activities on task tables.

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

 

</td></tr><tr><td>

Task Intelligence for Customer Service\[com.snc.csm\_ml\_task\]

 \(Available in the ServiceNow Store\)

</td><td>

Offers several AI capabilities including language detection, multi-lingual email and case categorization, case sentiment analysis, and document intelligence. These features automate several routine tasks across the case lifecycle, enabling agents to focus on case resolution.

</td><td>

Active

</td><td>

false

</td><td>

-   sn\_ti\_admin.com.sn\_ti\_admin
-   sn\_docintel.com.snc.docintel
-   com.sn\_customerservice
-   com.glide.platform\_ml\_task
-   com.glide.i18n
-   com.glide.dynamic\_translation

</td></tr><tr id="plugin_com.snc.task_outage" class="plugin_reference"><td class="name">

Task-Outage Relationship\[com.snc.task\_outage\]

</td><td class="description">

Allows users to create an outage from an incident and a problem form. Incidents and problems have many to many relationship with outages. For new instances from Jakarta only, this feature is also available on the Change form.

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

 

</td></tr><tr id="plugin_com.snc.apps_hub" class="plugin_reference"><td class="name">

Team Development\[com.snc.apps\_hub\]

</td><td class="description">

Supports parallel development on multiple, non-production ServiceNow instances by providing branching operations, the ability to compare a development instance to other development instances, and a central dashboard for all team development activities.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

-   com.snc.apps
-   com.glide.ui.angular

</td></tr><tr><td>

Team Performance\[com.sn\_team\_perf\]

</td><td>

Team Performance module for Workforce Optimization

</td><td>

Active

</td><td>

false

</td><td>

com.snc.wfo

</td></tr><tr><td>

Template Management for Field Service\[com.snc.fsm\_template\_management\]

 \(New in Tokyo\)

</td><td>

Enables administrators to configure work order templates to process data dynamically rather than using the static information described in the work order templates. It fetches information from the source table to populate fields in the work order form and creates relevant tasks for a work order.

</td><td>

Active

</td><td>

false

</td><td>

com.snc.work\_management

</td></tr><tr><td>

Templated Snippets\[com.sn\_templated\_snip\]

</td><td>

Activated with Human Resources Scoped App: Core \[com.sn\_hr\_core\]. Creates pre-defined and reusable responses that can be added to any table extending the task table including the HR Case table.

</td><td>

Inactive

</td><td>

true

</td><td>

com.glide.scope.access.restricted\_caller

</td></tr><tr id="plugin_com.snc.test_mgmt" class="plugin_reference"><td class="name">

Test Management\[com.snc.test\_mgmt\]

</td><td class="description">

Provides a tool for manual software testing.

</td><td>

Inactive

</td><td class="has_demo_data">

true

</td><td class="requires">

com.snc.planned\_task\_v2

</td></tr><tr><td class="name">

Test Management 2.0\[com.snc.test\_management.2.0\]

</td><td class="description">

Enables you to manage testing processes and deliver software products more efficiently, with fewer errors.

</td><td>

Inactive

</td><td class="has demo data">

false

</td><td class="requires">

-   com.snc.planned\_task\_v2
-   com.snc.sdlc.agile.2.0.common

</td></tr><tr><td>

Test Migration 2.0 - Data Migration\[com.snc.test\_migration\_v1\_v2\]

</td><td>

The Test Migration plugin provides functionality for migrating Test Case, Test and Test Suite to Test Management 2.0 Test version, Test Step and Test Set.

</td><td>

Active

</td><td>

false

</td><td class="requires">

-   com.snc.test\_mgmt
-   com.snc.test\_management.2.0

</td></tr><tr id="plugin_com.glide.text_index_attachments" class="plugin_reference"><td class="name">

Text Index Attachments\[com.glide.text\_index\_attachments\]

</td><td class="description">

Text Index Attachments - natural language search using Lucene syntax.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

com.glide.text\_index

</td></tr><tr id="plugin_com.glide.text_search" class="plugin_reference"><td class="name">

Text Search\[com.glide.text\_search\]

</td><td class="description">

Text Searching across multiple tables.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

com.glide.text\_index

</td></tr><tr><td>

Threat Core\[com.snc.threat\]

</td><td>

Integrates Threat Intelligence with other Security Operations applications. Activation of this plugin on production instances may require a separate license. Contact ServiceNow for details.

</td><td>

Inactive

</td><td>

false

</td><td>

com.snc.secops.orchestration

</td></tr><tr><td>

Threat Intelligence\[com.snc.threat.intelligence\]

</td><td>

Provides a point of reference for your company's Structured Threat Information Expression \(STIX\) data. Included in Threat Intelligence is the Security Case Management application. Activation of this plugin on production instances may require a separate license. Contact ServiceNow for details.

</td><td>

Inactive

</td><td>

true

</td><td>

com.snc.threat

</td></tr><tr id="plugin_com.snc.time_card" class="plugin_reference"><td class="name">

Time card management\[com.snc.time\_card\]

</td><td class="description">

Works with the Task table to record time worked on projects, incidents, problems, and change requests. Task assignees can record time worked in the **Time worked** field on a task record or enter hours directly onto a time card.

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

com.snc.time\_card\_portal

</td></tr><tr><td>

Time Recording for Customer Service\[com.snc.csm\_time\_recording\]

</td><td>

Enables customer service ages to record time on cases, case tasks, and other activities. Recording time automatically generates time cards and time sheets for approval by customer service managers.

</td><td>

Inactive

</td><td>

false

</td><td class="requires">

-   com.snc.wm\_time\_recording
-   com.sn\_customerservice

</td></tr><tr><td class="name">

Time Recording for Field Service\[com.snc.time\_recording\_fsm\]

</td><td class="description">

Extends the functionality of the Time Card Management and Cost Management applications to Field Service Management. Field service agents record time worked on tasks and other activities. These time worked entries automatically create time cards and weekly time sheets. Managers can review and approve time sheets as well as view and create labor rate cards.

</td><td>

Inactive

</td><td class="has_demo_data">

true

</td><td class="requires">

-   com.snc.work\_management
-   com.snc.wm\_time\_recording

</td></tr><tr id="plugin_com.snc.timeline_visualization" class="plugin_reference"><td class="name">

Timeline Visualization\[com.snc.timeline\_visualization\]

</td><td class="description">

Enables graphical representation of activities over time to provide a high-level view of strategic and operational activities in your organization such as incidents, problems, changes, and projects. A base system visualization provided by this plugin is the CIO Roadmap. This roadmap shows projects grouped by portfolios. Organization leaders can use the CIO roadmap to monitor and evaluate the status of current and upcoming projects.

</td><td>

Inactive

</td><td class="has_demo_data">

true

</td><td class="requires">

com.snc.project\_management\_v3

</td></tr><tr id="plugin_com.glide.tiny_url" class="plugin_reference"><td class="name">

Tiny URL Support\[com.glide.tiny\_url\]

</td><td class="description">

Enables support for generating shortened URLs to eliminate problems with very long URLs in Internet Explorer. New properties will be added to the System properties page.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

 

</td></tr><tr id="plugin_com.glide.editor.tinymce" class="plugin_reference"><td class="name">

TinyMCE HTML Field Editor\[com.glide.editor.tinymce\]

</td><td class="description">

Enables users to edit HMTL fields with the TinyMCE editor instead of the legacy \(htmlArea\) editor.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

 

</td></tr><tr id="plugin_com.glide.transaction_scope" class="plugin_reference"><td class="name">

Transaction Design Scope\[com.glide.transaction\_scope\]

</td><td class="description">

Handles transaction design scope management.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

 

</td></tr><tr id="plugin_com.glide.quota" class="plugin_reference"><td class="name">

Transaction Quotas\[com.glide.quota\]

</td><td class="description">

Allows definition of quota policies for different types of transactions. A transaction quota cancels any transaction in violation of the policy and notifies the user of the cancellation.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

 

</td></tr><tr><td>

Transform Definitions\[com.glide.transform.definitions\]

</td><td>

Activates transform functions which enables flow designers to transform a data pill or field's data type without writing a script.

</td><td>

Active

</td><td>

false

</td><td>

com.glide.transform

</td></tr><tr><td>

Transform Service\[com.glide.transform\]

</td><td>

Supports use of Transform APIs associated with the Remote Tables functionality.

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Translated Email Retention\[com.glide.email\_retention.translation\]

 \(New in Tokyo\)

</td><td>

Provides retention policy for Email translations.

</td><td>

Inactive

</td><td>

false

</td><td>

com.glide.notification.translation

</td></tr><tr><td>

Transaction stats\[com.glide.stats.transaction\]

</td><td>

Transaction stats.

</td><td>

Active

</td><td>

false

</td><td>

com.glide.stats

</td></tr><tr id="plugin_com.snc.treemap" class="plugin_reference"><td class="name">

Tree map\[com.snc.treemap\]

</td><td class="description">

Enables support for treemap view on any applications.

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

com.snc.pa

</td></tr><tr><td>

Trusted Security Circles Client\[com.snc.intel\_sharing.client\]

</td><td>

Provides the ability to set up communication channels that connect sets of Trusted Security Circles customers who have some kind of underlying relationship. Activation of this plugin on production instances may require a separate license. Contact ServiceNow for details.

</td><td>

Inactive

</td><td>

true

</td><td>

com.snc.threat

</td></tr><tr><td>

Trusted Security Circles Client \(Advanced\)\[com.snc.intel\_sharing.clnt.adv\]

</td><td>

Provides the capabilities of the basic level, along with the ability to join any available trusted circle and initiate an unlimited number of threat shares per day. Activation of this plugin on production instances may require a separate license. Contact ServiceNow for details.

</td><td>

Inactive

</td><td>

false

</td><td>

com.snc.intel\_sharing.client

</td></tr><tr id="plugin_com.glide.ui.doctype" class="plugin_reference"><td class="name">

UI 15\[com.glide.ui.doctype\]

</td><td class="description">

Enables UI15, a user interface for modern browsers with refined colors and usability enhancements.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

-   com.glide.ui11
-   com.glide.ui.recent\_selections
-   com.glide.ui.themes.doctype
-   com.glide.ui.font\_icons
-   com.glide.ui.ng
-   com.glide.editor.tinymce
-   com.glide.ui.personalize\_form
-   com.glide.ui.overview\_help

</td></tr><tr id="plugin_com.glide.ui.common" class="plugin_reference"><td class="name">

UI Common\[com.glide.ui.common\]

</td><td class="description">

Glide UI Common

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

 

</td></tr><tr id="plugin_com.glideapp.ui_components" class="plugin_reference"><td class="name">

UI Components\[com.glideapp.ui\_components\]

</td><td class="description">

Provides all common angular components for apps.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

-   com.glide.ui.ng
-   com.glide.ui.angularui
-   com.glide.ui.heisenberg

</td></tr><tr id="plugin_com.glide.ui.ui16" class="plugin_reference"><td class="name">

UI16\[com.glide.ui.ui16\]

</td><td class="description">

Enables Core UI, a user interface that provides an updated look and usability improvements. Notable features include real-time form updates, user presence, a redesigned application navigator with tabs for favorites and history, and enhanced activity streams.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

-   com.glide.ui.doctype
-   com.glide.ui.concourse
-   com.glide.ui.form\_presence
-   com.glide.ui.snippets

</td></tr><tr><td>

Universal Request Integration for Incident management\[com.snc.incident.universal\_request\]

</td><td>

This plugin delivers Universal Request Integration for Incident Management. It is a developer plugin.

</td><td>

False

</td><td>

True

</td><td>

com.snc.universal\_request

</td></tr><tr><td>

Universal Request Integration with Microsoft Teams\[com.snc.universal\_request.ms\_teams\]

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Universal Request: Advanced Work Assignment\[com.snc.universal\_request.awa\]

</td><td>

Enables to use Advanced Work Assignment and automatically assign work items to your agents, based on their availability in the Universal Request application.

</td><td>

False

</td><td>

True

</td><td>

com.snc.universal\_request

</td></tr><tr><td>

Universal Request: NLU Model for Virtual Agent Conversations\[com.snc.universal\_request.nlu\]

</td><td>

Allows the use of NLU for virtual agent conversations in Universal Request.

</td><td>

False

</td><td>

True

</td><td>

 

</td></tr><tr><td>

Universal Request: Reporting\[com.snc.universal\_request.reporting\]

</td><td>

Enables to use reports in Universal Request.

</td><td>

False

</td><td>

True

</td><td>

 

</td></tr><tr><td>

Universal Request: Virtual Agent Conversations\[com.snc.universal\_request.va\]

</td><td>

Helps to set up and use Virtual Agent in Universal Request.

</td><td>

False

</td><td>

True

</td><td>

 

</td></tr><tr><td>

Predictive Intelligence for Universal Request\[com.snc.universal\_request.ml\]

</td><td>

Facilitates to use machine-learning solutions in the Universal Request application, if you have the admin role.

</td><td>

False

</td><td>

True

</td><td>

-   com.snc.universal\_request
-   com.glide.platform\_ml

</td></tr><tr><td>

Performance Analytics and Reporting for Universal Request\[com.snc.universal\_request.pa\]

</td><td>

Contains Performance Analytic and Reporting dashboard created for Universal Request.

</td><td>

False

</td><td>

False

</td><td>

 

</td></tr><tr><td>

Universal Request integration with Microsoft Teams\[sn\_uni\_req\_msteams\]

</td><td>

Enables to use Microsoft Teams in the Universal Request application.

</td><td>

False

</td><td>

True

</td><td>

-   com.glide.cs.chatbot
-   com.snc.universal\_request.va
-   sn\_now\_teams

</td></tr><tr><td>

Universal Request\[com.snc.universal\_request\]

</td><td>

Install this plugin to use the Universal Request application.

</td><td>

False

</td><td>

True

</td><td>

 

</td></tr><tr><td>

Update Set Batching\[com.glide.system\_hierarchy\_update\_set\]

</td><td>

Deploy update sets in a group.

</td><td>

Active

</td><td>

false

</td><td>

com.glide.system\_update\_set

</td></tr><tr id="plugin_com.glide.upgrade_blame" class="plugin_reference"><td class="name">

Upgrade Blame Tool\[com.glide.upgrade\_blame\]

</td><td class="description">

Tracks the affected table records touched \(insert/update/delete\) by the load files during system upgrade, zboot, or plugin activation/upgrade. This plugin adds application modules to allow ServiceNow employees to access the upgrade blame log and to turn on/off the feature. It also adds security access control rules to prevent user from modifying the upgrade blame logs table.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

 

</td></tr><tr><td>

Upgrade Metric\[com.glide.upgrade\_metric\]

</td><td>

This plugin uses the Upgrade Metric table to track the changes that take a long time to load during upgrades.

</td><td>

Active

</td><td>

false

</td><td>

 

</td></tr><tr><td>

User Criteria Scoped API\[com.glideapp.user\_criteria.scoped.api\]

</td><td>

User Criteria Scoped API to support CRUD operations on User Criteria.

</td><td>

Inactive

</td><td>

false

</td><td>

com.glideapp.user\_criteria

</td></tr><tr id="plugin_com.glide.user_guide" class="plugin_reference"><td class="name">

User Guide\[com.glide.user\_guide\]

</td><td class="description">

Provides the ability to create end-user help documentation that is specific to the policies and procedures of your organization. A default help page is provided in the base system that displays Core UI help documents for system navigation and other basic operations.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

 

</td></tr><tr><td>

User Experience Analytics \[com.glide.appsee\]

</td><td>

Checks for new web and mobile applications to register and provides users access to the Dashboard​.

</td><td>

Active

</td><td>

false

</td><td>

com.glide.serviceproxy

</td></tr><tr id="plugin_com.snc.user_registration" class="plugin_reference"><td class="name">

User Registration Request\[com.snc.user\_registration\]

</td><td class="description">

Provides the ability for unregistered users to request access to a ServiceNow instance.

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

 

</td></tr><tr><td class="name">

Vaccine Administration Management\[com.sn\_vaccine\_sm\]

 \(Available in the ServiceNow Store\)

</td><td class="description">

Enables governments and healthcare providers to deliver vaccines, on a deadline and with finite resources.

</td><td>

Inactive

</td><td class="has_demo_data">

true

</td><td class="requires">

-   com.snc.appointment\_booking
-   com.snc.business\_location
-   com.snc.csm\_case\_types
-   com.snc.household
-   com.snc.install\_base
-   com.glide.encryption
-   com.sn\_external\_user\_register
-   com.snc.pdf\_generator
-   com.snc.signaturepad
-   com.glideapp.user\_criteria.scoped.api
-   sn\_hcls
-   sn\_csm\_playbook
-   com.sn\_ind
-   sn\_doc
-   sn\_prd\_pm
-   sn\_ciwf\_ui\_cmpnt

</td></tr><tr><td>

Vendor Manager Workspace\[com.snc.vlm.vmw\]

</td><td>

Access to the Vendor Manager Workspace.

</td><td>

Inactive

</td><td>

false

</td><td>

-   Performance Analytics - Premium
-   Service Workspace, Vendor Manager Workspace - Core
-   Service Owner Workspace, UX Framework
-   GraphQL Plugin
-   Interactions Management
-   Agent Workspace - Main Configuration
-   Agent Workspace - Ribbon
-   Agent Workspace - List
-   Agent Workspace - Form
-   com.snc.agent\_workspace.global\_search
-   com.snc.agent\_workspace.declarative\_actions
-   com.snc.agent\_workspace.highlighted\_values

</td></tr><tr><td>

Vendor Manager Workspace - Core\[com.snc.vlm\]

</td><td>

Configure the Vendor Manager Workspace.

</td><td>

Inactive

</td><td>

false

</td><td>

 

</td></tr><tr><td>

Vendor Success Indicators \[com.snc.vendor.insights\] \(Maintenance mode only\). Planned for deprecation after August 1, 2024

</td><td>

Vendor Success Indicators to utilize Odds Ratio and other ML capabilities for Vendor Manager Workspace.

</td><td>

Inactive

</td><td>

false

</td><td>

com.snc.app.ml.insights

</td></tr><tr id="plugin_com.snc.version" class="plugin_reference"><td class="name">

Version Management\[com.snc.version\]

</td><td class="description">

Provides the ability to track, compare, and revert to multiple versions of table records.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

 

</td></tr><tr id="plugin_com.glideapp.version" class="plugin_reference"><td class="name">

Version Support\[com.glideapp.version\]

</td><td class="description">

Supports tracking versions of files that are stored in update sets, including the ability to compare and revert to previous versions.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

 

</td></tr><tr><td>

Virtual Agent Experience Pack for Procurement Service Management\[com.sn\_shop\_va\]

\(Starting with the Utah release, Virtual Agent Experience Pack for Procurement Service Management is renamed as Virtual Agent for Sourcing and Procurement Operations.\)

\(Available in the ServiceNow Store\)

</td><td>

Provides pre-configured topics for sourcing and procurement within a conversational interface, for employees to raise requests, find knowledge, and complete tasks.

</td><td>

Inactive

</td><td>

false

</td><td>

-   com.snc.sn\_pr
-   com.glide.cs.chatbot

</td></tr><tr><td>

Virtual Agent integration with actionable notifications\[com.glide.cs.actionable.notification\]

</td><td>

Enables ServiceNow actionable notifications on Virtual Agent chat channels.

</td><td>

Active

</td><td>

false

</td><td>

com.glide.cs.notification

</td></tr><tr><td>

Virtual Agent integration with notifications\[com.glide.cs.notification\]

</td><td>

Enable ServiceNow notifications on Virtual Agent chat channels.

</td><td>

Inactive

</td><td>

false

</td><td class="requires">

-   com.glide.cs
-   com.glide.notification.provider

</td></tr><tr><td>

Virtual Agent Language Detection and Translation\[com.glide.cs.runtime\_language\_detection\_translation\]

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Virtual Agent Platform Topics\[com.glide.cs.topics\]

</td><td>

Core conversation topics that support Virtual Agent platform conversation flows.

</td><td>

Inactive

</td><td>

false

</td><td>

com.glide.cs

</td></tr><tr><td>

Virtual Agent Platform Topic Blocks\[com.glide.cs.topic\_blocks\]

</td><td>

Topic blocks required to support core Virtual Agent platform conversation topics

</td><td>

Inactive

</td><td>

false

</td><td>

com.glide.cs

</td></tr><tr><td>

Virtual Agent Service Portal Widgets\[com.glide.va.sp\_widgets\]

</td><td>

Virtual Agent Service Portal Widgets

</td><td>

Inactive

</td><td>

true

</td><td class="requires">

-   com.glide.service-portal
-   com.glide.cs
-   com.glide.cs.sn-va-web-client-app

</td></tr><tr><td>

Virtual Agent Spoke\[com.glide.cs.va\_spoke\]

</td><td>

Virtual Agent Integration Hub actions and flows.

</td><td>

Active

</td><td>

false

</td><td>

 

</td></tr><tr><td>

Virtual Agent Web Client\[com.glide.cs.sn-va-web-client-app\]

</td><td>

Scoped app for the virtual agent web client.

</td><td>

Inactive

</td><td>

false

</td><td>

 

</td></tr><tr><td>

VirusTotal Integration\[com.snc.threat.virustotal\]

</td><td>

Enables the VirusTotal scanner in Threat Intelligence. Activation of this plugin on production instances may require a separate license. Contact ServiceNow for details.

</td><td>

Inactive

</td><td>

true

</td><td>

com.snc.threat

</td></tr><tr><td>

Visibility Content \[sn\_pattern\_design\]

 \(Available in the ServiceNow Store\)

</td><td>

Supplies the updated version of the patterns that were part of the family releases up until Tokyo.

</td><td>

Active

</td><td>

false

</td><td>

com.sn\_itom\_pattern

</td></tr><tr><td>

Visual Task Board Flow Designer Spoke\[com.glide.ui.vtb.ah\]

</td><td>

The Visual Task Board \(VTB\) Spoke for the Flow Designer provides Actions enable process analysts to compose flows that manipulate task boards, cards, board members, and assignees on given tasks without having to write code. The Visual Task Board Plugin \(com.glide.ui.vtb.ah\) should be installed to use these actions.

</td><td>

Active

</td><td>

false

</td><td class="requires">

-   com.glide.ui.vtb
-   com.glide.hub.designer\_backend.model

</td></tr><tr id="plugin_com.glide.ui.vtb" class="plugin_reference"><td class="name">

Visual Task Boards\[com.glide.ui.vtb\]

</td><td class="description">

Allows users to organize, modify, and track progress of multiple tasks from an intuitive, Kanban-inspired interface.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

-   com.glide.ui.ng
-   com.glide.ui.font\_icons
-   com.glide.task
-   com.glide.ui.checklist
-   com.glide.ui.ng.amb
-   com.glide.rest.service
-   com.glide.ui.ng.filter
-   com.glide.ui.magellan\_navigator\_api

</td></tr><tr id="plugin_com.snc.vulnerability" class="plugin_reference"><td class="name">

Vulnerability Response \[com.snc.vulnerability\]

 \(Available in the ServiceNow Store\)

</td><td class="description">

Allows security users to compare security data pulled from internal and external sources and, if CIs or software are found to be vulnerable, changes and security incidents can be created using Vulnerability Groups. Activation of this plugin on production instances may require a separate license. Contact ServiceNow for details.

</td><td>

Inactive

</td><td class="has_demo_data">

true

</td><td class="requires">

-   com.snc.sam.core
-   com.snc.secops.orchestration
-   com.snc.security\_support.vul

</td></tr><tr><td>

Vulnerability Response Common \[sn\_vul\_cmn\]\(Available in the ServiceNow Store\)

</td><td>

Framework that provides the necessary functionality to support  the Vulnerability Response applications like Vulnerability Response, Application Vulnerability Response, Container Vulnerability Response and Configuration Compliance.

</td><td>

Active

</td><td>

false

</td><td>

Security Support Common \[sn\_sec\_cmn\]

</td></tr><tr><td>

Vulnerability Response Dependencies\[com.snc.vul\_dep\]

</td><td>

System dependencies required by Vulnerability Response. Activation of this plugin on production instances may require a separate license. Contact ServiceNow for details.

</td><td>

 

</td><td>

false

</td><td>

 

</td></tr><tr><td>

Vulnerability Response Mobile\[com.snc.vul\_mobile\]

 \(Available in the ServiceNow Store\)

</td><td>

As a remediation owner, you can access the Vulnerability Response \(VR\) application on your ServiceNow AI Platform instance with your Android or iOS mobile device.

</td><td>

Active

</td><td>

false

</td><td>

com.glide.sg.agent\_native\_client

</td></tr><tr><td>

Vulnerability Solution Management\[com.snc.vulnerability.solution\]

 \(Available in the ServiceNow Store\)

</td><td>

Vulnerability Solution Management automatically correlates solutions with vulnerabilities, identifies preferred solutions to reduce risk, and tracks deployment progress. The Vulnerability Solution Management application enables the Vulnerability Solution Management feature in Vulnerability Response.

</td><td>

Active

</td><td>

 

</td><td>

 

</td></tr><tr><td class="name">

Walk-up Experience\[com.snc.walkup\]

</td><td class="description">

Enables your IT organization to set up a contact channel to support both online check-in and onsite check-in to a pre-established walk-up service center.

</td><td>

Inactive

</td><td class="has_demo_data">

true

</td><td class="requires">

-   com.snc.agent\_workspace.itsm
-   com.glide.awa
-   com.glide.interaction
-   com.snc.asset\_management
-   com.glide.service-portal
-   com.snc.appointment\_booking
-   com.glide.db\_audio

</td></tr><tr><td>

Walk-Up for CSM \(Maintenance mode only\)\[com.snc.walkup\_for\_csm\]

</td><td>

Walk-up experience for Customer Service enables in-store support to assist onsite check-ins, managing queues, and customer interactions

</td><td>

Active

</td><td>

false

</td><td class="requires">

-   com.snc.walkup
-   com.sn\_customerservice

</td></tr><tr id="plugin_com.glide.web_service_consumer" class="plugin_reference"><td class="name">

Web Service Consumer\[com.glide.web\_service\_consumer\]

</td><td class="description">

Provides a SOAP Message module for developing, prototyping, and saving outbound SOAP messages that can be reused in business rules and scripts.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

-   com.glide.vars
-   com.glideapp.ecc

</td></tr><tr id="plugin_com.snc.web_service_import_set_tables" class="plugin_reference"><td class="name">

Web Service Import Set Tables\[com.snc.web\_service\_import\_set\_tables\]

</td><td class="description">

Complements direct web services and scripted web services in providing a web service interface to import set tables.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

-   com.glide.web\_service\_import\_sets
-   com.glide.web\_service\_application

</td></tr><tr id="plugin_com.glide.web_service_import_sets" class="plugin_reference"><td class="name">

Web Service Import Sets\[com.glide.web\_service\_import\_sets\]

</td><td class="description">

Complements direct web services and scripted web services in providing a web service interface to import sets.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

-   com.glide.table\_editor
-   com.glide.web\_service\_provider

</td></tr><tr id="plugin_com.glide.web_service_provider" class="plugin_reference"><td class="name">

Web Service Provider - Common\[com.glide.web\_service\_provider\]

</td><td class="description">

Provides scripted web service and SOAP message resources.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

-   com.glide.vars
-   com.glide.system\_property\_categories
-   com.glide.system\_import\_set

</td></tr><tr id="plugin_com.glide.static_wsdl" class="plugin_reference"><td class="name">

Web Service Provider - Custom WSDL\[com.glide.static\_wsdl\]

</td><td class="description">

Provides the ability to create a scripted web service to accept any WSDL format.

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

 

</td></tr><tr id="plugin_com.glide.custom_web_service" class="plugin_reference"><td class="name">

Web Service Provider - Scripted\[com.glide.custom\_web\_service\]

</td><td class="description">

Enables users to create web services that are not addressed by the system. Allows a user to define input and output parameters and use JavaScript to do everything in between.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

-   com.glide.web\_service\_provider
-   com.glide.web\_service\_consumer

</td></tr><tr id="plugin_com.glide.wiki" class="plugin_reference"><td class="name">

WebKit HTML to PDF\[com.snc.whtp\]

</td><td class="description">

Enables the instance to use the service WebKit HTML to PDF.

</td><td>

Inactive

</td><td class="has_demo_data">

false

</td><td class="requires">

com.snc.platform.security.oauth

</td></tr><tr><td>

WFO Mobile\[com.snc.wfo.mobile\]

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Widgets\[com.snc.app.widgets\]

</td><td>

Provides widget infrastructure along with Angular UI carousel module.

</td><td>

Inactive

</td><td>

false

</td><td>

 

</td></tr><tr><td>

Workday ESG integration \[sn\_esg\_workday\]

 \(Available in the ServiceNow Store\)

</td><td>

Enables ESG users to pull critical HR data from Workday in to ESG instances.

</td><td>

Active

</td><td>

true

</td><td>

ESG Management

</td></tr><tr id="plugin_com.glideapp.workflow.authoring" class="plugin_reference"><td class="name">

Workflow Authoring Tools\[com.glideapp.workflow.authoring\]

</td><td class="description">

Allows you to define and modify workflows by arranging and connecting activities with transitions.

</td><td>

Active

</td><td class="has_demo_data">

true

</td><td class="requires">

com.glideapp.workflow

</td></tr><tr><td>

Workflow Pause Utility\[com.glideapp.workflow.pause\]

</td><td>

Allows you to pause and resume workflows.

</td><td>

Inactive

</td><td>

false

</td><td>

 

</td></tr><tr id="plugin_com.glideapp.workflow" class="plugin_reference"><td class="name">

Workflow Runtime Engine\[com.glideapp.workflow\]

</td><td class="description">

Enables the creation of workflows that drive automated processes. This may entail generating tasks based on conditions, running scripts, generating approvals, or other actions. Satisfies the same need as the Execution Plans plugin but with greater control and an easier interface.

</td><td>

Active

</td><td class="has_demo_data">

false

</td><td class="requires">

-   com.glide.diagrammer
-   com.glide.vars
-   com.glide.schedules
-   com.glide.relative\_duration
-   com.glide.web\_service\_application
-   com.glide.service\_api
-   com.snc.datastructure
-   com.glideapp.live\_feed

</td></tr><tr><td>

Workflow/Stages element support\[com.glide.stages\]

</td><td>

Support for Workflow-type elements and stage displays.

</td><td>

Active

</td><td>

false

</td><td>

 

</td></tr><tr><td>

Workforce Optimization \(Maintenance mode only\)\[com.snc.wfo\]

</td><td>

Activation of this plugin on production instances may require a separate license. Contact ServiceNow for details.

</td><td>

Active

</td><td>

false

</td><td>

 

</td></tr><tr><td>

Workforce Optimization Common\[com.sn\_wfo\_common\]

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Workforce Optimization Dependencies\[com.sn\_wfo\_dependency\]

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Workforce Optimization for Customer Service \(Maintenance mode only\)\[com.snc.wfo.csm\]

</td><td>

The Workforce Optimization for Customer Service application provides Channel Management, Team Performance, Scheduling, Skill Determination and Coaching capabilities for managers, supervisors, and team leads to improve quality and efficiency of their customer service teams and enhance team satisfaction.

</td><td>

Active

</td><td>

false

</td><td class="requires">

-   com.snc.manager\_workspace
-   com.sn\_customerservice
-   com.glide.interaction.awa
-   com.sn\_channel\_management
-   com.snc.wfo
-   com.sn\_shift\_planning
-   com.snc.skills\_management
-   com.manager\_workspace\_components
-   com.sn\_coaching
-   com.snc.sre
-   com.sn\_team\_perf

</td></tr><tr><td>

Workforce Optimization for Field Service Management\[sn\_fsm\_wfo\]

 \(Available in the ServiceNow Store\)

</td><td>

Helps to manage and maintain the productivity of your workforce from a single application using Workforce Optimization for Field Service.

</td><td>

Active

</td><td>

true

</td><td>

-   FSM Team Performance Management \(com.snc.sn\_fsm\_team\_mgmt\)
-   FSM Shift Scheduling \(com.snc.sn\_fsm\_shift\_schdl\)
-   Skill Recommendation Engine \(com.snc.sre\)
-   Coaching \(com.sn\_coach\_learning, com.sn\_coaching\)

</td></tr><tr><td>

Workforce Optimization for HR\[com.sn\_hr\_wfo\]

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Workforce Optimization for ITSM \[com.snc.wfo\_itsm\]

 \(Maintenance mode only\)

</td><td>

Workforce Optimization bundle for IT Service Management

</td><td>

Active

</td><td>

false

</td><td class="requires">

-   com.snc.wfo
-   com.sn\_shift\_planning
-   com.snc.skills\_management
-   com.snc.manager\_workspace
-   com.manager\_workspace\_components
-   com.sn\_coaching
-   com.snc.sre
-   com.sn\_team\_perf
-   com.sn\_channel\_management
-   com.snc.incident.awa
-   com.snc.walkup
-   com.glide.interaction.awa

</td></tr><tr><td>

Workspace Core\[com.workspace\_core\]

</td><td>

Core Workspace app for enabling CSM/ITSM agents to provide world-class service at light speed.

</td><td>

Active

</td><td>

false

</td><td class="requires">

-   com.glide.uxbuilder
-   com.snc.agent\_workspace.config
-   com.snc.agent\_workspace.global\_search

</td></tr><tr><td>

Workplace Indoor Mapping\[sn\_wsd\_indoor\_map\]

 \(Available in the ServiceNow Store\)

</td><td>

Enables organizations to digitalize their workplace floor plans. Using the Map Studio, map admins can create and update maps that can be used across the Workplace Delivery Suite.

</td><td>

Active

</td><td>

true

</td><td>

-   sn\_wsd\_suite
-   sn\_wsd\_space\_map

</td></tr><tr><td>

XML Parser for ServiceNow IntegrationHub\[com.glide.hub.action\_step.xmlparser\]

</td><td>

Activates the XML parser step in Flow Designer, enabling you to identify structured data from an XML payload without having to write script.

</td><td>

Inactive

</td><td>

false

</td><td>

com.glide.hub.action\_step.template

</td></tr><tr><td>

XTM Translation Management System Spoke for Localization Framework\[com.glide.localization\_framework.xtm\_spoke\]

</td><td>

Integrates Localization Framework with the XTM - Translation Management System. To activate this plugin, install the Localization Framework Installer plugin.

</td><td>

Active

</td><td>

false

</td><td>

com.glide.localization\_framework

</td></tr><tr><td>

Zoom extension for Omnichannel Callback\[com.sn.zoom.callback\]

 \(Available in the ServiceNow Store\)

</td><td>

Enables customers to request for a visual engagement session using Zoom.

</td><td>

Active

</td><td>

false

</td><td>

-   com.snc.notify.zoom
-   com.sn.omnichannel.callback

</td></tr></tbody>
</table>
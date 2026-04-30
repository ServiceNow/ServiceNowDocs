---
title: Changes to plugins in the Yokohama release
description: This table lists the existing plugins that were deprecated, planned for deprecation, renamed, or changed in some way.This table lists the existing plugins that were deprecated in Yokohama and Xanadu that weren't previously listed as planned for deprecation.This table lists the existing plugins that were planned for deprecation in a future release.This table lists the existing plugins that were renamed or changed in Yokohama or Xanadu.This table lists the existing plugins that are in maintenance mode.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 15
breadcrumb: [Release notes for upgrading from Xanadu, Learn about the Yokohama release, Yokohama release notes]
---

# Changes to plugins in the Yokohama release

This table lists the existing plugins that were deprecated, planned for deprecation, renamed, or changed in some way.

-   Planned for deprecation: In preparation for the future deprecation. The application is being prepared for future deprecation. The plugin will be hidden and no longer available for activation but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support knowledge base.
-   Deprecated: The application is no longer deployed, enhanced, or supported. For details, see the [Deprecation Process \[KB0867184\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support knowledge base.
-   Maintenance mode: The application will have no new enhancements or activations but will have continued support.

## Deprecated plugins

This table lists the existing plugins that were deprecated in Yokohama and Xanadu that weren't previously listed as planned for deprecation.

<table id="table_xcl_5mj_tx"><thead><tr><th>

Plugin

</th><th>

Status

</th><th>

Description

</th><th>

Details

</th></tr></thead><tbody><tr><td>

Cloud Provisioning and Governance: Google Cloud Connector \[sn\_cmp\_gcp\]

</td><td>

Deprecated in Yokohama

</td><td>

Integrate Cloud Management Google Cloud Connector scoped application with CMP

</td><td>

Install the Cloud Provisioning and Governance: Terraform Connector application from the ServiceNow Store and review the [Cloud Services Catalog Terraform Connector](https://www.servicenow.com/docs/access?context=cpg-terraform-connector-landing-page&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US) documentation.

</td></tr><tr><td>

Conversational Integration with Google Business Messages \[sn\_gbm\_adapter\]

</td><td>

Deprecated in Yokohama

</td><td>

Interact with requesters on the Google Business Messages app.

</td><td>

There is no replacement for this application.

</td></tr><tr><td>

Column Level Encryption \[com.glide.encryption\]

</td><td>

Deprecated in Yokohama

</td><td>

Enables support for encryption of fields and attachments.

</td><td>

Use either Field Encryption Starter or Field Encryption Enterprise under the new entitlement structure. For more information, see [Activate Field Encryption Enterprise](https://www.servicenow.com/docs/access?context=activate-platform-encryption&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).

</td></tr><tr><td>

CTI Demo Data for HRSD \[sn\_hr\_cti\_demo\]

</td><td>

Deprecated in Yokohama

</td><td>

Provides CTI Softphone application demo data for HRSD.

</td><td>

Install the ServiceNow Voice for HR Service Delivery \(HRSD\) application.

</td></tr><tr><td>

Customer Service Management IoT Demo \[com.snc.csm.iot.demo\]

</td><td>

Deprecated in Yokohama

</td><td align="center">

—

</td><td>

There is no replacement for this plugin.

</td></tr><tr><td>

Employee Campaigns for Workplace from Facebook\[sn\_fb\_wp\_campaigns\]

</td><td>

Deprecated in Yokohama

</td><td>

Enables you to package your content into a campaign and publish the content to groups on Workplace from Facebook.

</td><td>

There is no replacement for this application. If you are using this application, you have the option to maintain the unsupported application as custom code.

</td></tr><tr><td>

IBM Watson Language Translator Service Spoke \[com.glide.ibm\_translation\_spoke\]

</td><td>

Deprecated in Yokohama

</td><td>

In ServiceNow's Dynamic Translation app, this spoke connected to the third-party machine translation service provided by IBM Watson

</td><td>

As an alternative, customers can create accounts with other third-party translation services such as Google or Microsoft Azure

</td></tr><tr><td>

HR Agent Workspace\[com.sn\_hr\_agent\_workspace\]

</td><td>

Deprecated in Xanadu

</td><td>

Use the HR Service Delivery Agent Workspace to interact with employees, respond to inquiries, and resolve issues quickly.

</td><td>

Install and configure the HRSD Configurable Agent Workspace for Case Management. For guidance, see [Agent Workspace for HR Case Management \(Configurable\)](https://www.servicenow.com/docs/access?context=agent-ws-hr-case-mgmt-landing-page&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US) and this [Community Article](https://www.servicenow.com/community/hrsd-articles/hr-agent-workspace-migration-guidelines-from-classic-to/ta-p/2310606).

</td></tr><tr><td>

HR Service Delivery v1.0 \(Legacy\)\[com.snc.hr.core.cms, com.snc.hr.core, com.snc.hr.hr\_connect, con.snc.hr.pa, com.snc.hr.service\_portal\]

</td><td>

Deprecated in Xanadu

</td><td>

Unlocks enterprise productivity and give your employees the service experience they deserve.

</td><td>

Migrate to the Human Resources Core v2.0 scoped application \[com.sn\_hr\_core\].

</td></tr><tr><td>

FSM Agent Classic Workspace\[com.snc.agent\_workspace.fsm\]

</td><td>

Deprecated in Xanadu

</td><td align="center">

—

</td><td>

Install and configure the Field Service Dispatcher workspace. For guidance, see [Configuring Dispatcher Workspace](https://www.servicenow.com/docs/access?context=configuring-dispatcher-workspace&version=yokohama&pubname=yokohama-field-service-management&ft:locale=en-US).

</td></tr><tr><td>

HR Agent Mobile\[com.sn\_hr\_mobile\_agent\]

</td><td>

Deprecated in Xanadu

</td><td align="center">

—

</td><td>

No replacement. If you are using this plugin, you have the option to maintain the unsupported plugin as custom code.

</td></tr><tr><td>

Instance Security Center\[sn\_isc\_core, sn\_isc\_nlu, sn\_isc\_va\]

</td><td>

Deprecated in Xanadu

</td><td>

Monitors the compliance level of instance security controls, view security event monitoring metrics, and configure and maintain instance security settings all from within the Instance Security Center.

</td><td>

Install ServiceNow Security Center on the ServiceNow Store. For guidance, see [Security Center](https://www.servicenow.com/docs/access?context=sec-center-v2&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).

</td></tr><tr><td>

Field Service Map\[com.snc.fsm\_map\]

</td><td>

Deprecated in Xanadu

</td><td>

Displays the dispatch map for viewing agents, tasks, and agent routes.

</td><td>

Install and configure the Field Service Dispatcher workspace. For guidance, see [Configuring Dispatcher Workspace](https://www.servicenow.com/docs/access?context=configuring-dispatcher-workspace&version=yokohama&pubname=yokohama-field-service-management&ft:locale=en-US).

</td></tr><tr><td>

Cloud Discovery setup using classic Cloud Discovery

</td><td>

Deprecated in Xanadu

</td><td>

Enables you to set up Cloud Discovery for performing cloud discovery and using Cloud Provisioning and Governance for managing discovered cloud resources.

</td><td>

Install Cloud Operations Workspace \(COW\) on the ServiceNow Store.

</td></tr><tr><td>

Cloud Spend Dashboard\[sn\_sam\_cld\_spend\]

</td><td>

Deprecated in Xanadu

</td><td>

Helps you view all cloud spend on a single dashboard, including software, platform, and infrastructure.

</td><td>

Install the Asset Executive Workspace on the ServiceNow Store.

</td></tr><tr><td>

Global Reporting Initiative \(GRI\) Content Accelerator for ESG\[com.sn\_esg\_gri\]

</td><td>

Deprecated in Xanadu

</td><td>

Offers ESG frameworks such as authority documents and citations and provides the related metric definitions.

</td><td>

Install the ESG Content Accelerator application from the ServiceNow Store. For guidance, see [ESG content accelerator](https://www.servicenow.com/docs/access?context=esg-content-accelerator&version=yokohama&pubname=yokohama-environmental-social-governance&ft:locale=en-US).

</td></tr><tr><td>

RPA Sample Template \[com.sn\_rpa\_template\]

</td><td>

Deprecated in Xanadu

</td><td>

RPA templates are prebuilt automations that enable customers to kickstart their RPA initiatives.

</td><td>

Install RPA Hub version 9.0.0 or later from the ServiceNow Store.-   Download and install RPA Desktop Design Studio using the guidance in the documentation.
-   You can access the templates \(referred to as sample automations\) within the RPA Desktop Design Studio home page. Open RPA Desktop Design Studio and on the Home page, select “Automation Projects” to view a list of sample automations. For more information, see the documentation.

</td></tr><tr><td>

Sustainability Accounting Standards Board \(SASB\) Content Accelerator for ESG\[com.sn\_esg\_sasb\]

</td><td>

Deprecated in Xanadu

</td><td>

The SASB Accelerator is designed for use with the ESG Management and Reporting application to enable customers to easily adopt the SASB framework to produce their ESG disclosures.

</td><td>

Install the ESG Content Accelerator application from the ServiceNow Store. For guidance, see [ESG content accelerator](https://www.servicenow.com/docs/access?context=esg-content-accelerator&version=yokohama&pubname=yokohama-environmental-social-governance&ft:locale=en-US).

</td></tr><tr><td>

Service Bridge for Providers \(Legacy\) \[com.sn\_nowebonding\_provider\]

</td><td>

Deprecated in Xanadu

</td><td>

Allows providers to publish catalogs for customers and receive and fulfill customer service requests.

</td><td>

-   Install the [Service Bridge for Providers](https://www.servicenow.com/docs/access?context=service-bridge-providers-landing-page&version=yokohama&pubname=yokohama-service-bridge&ft:locale=en-US) application from the ServiceNow Store and review the documentation.
-   Follow the guidance in KB1499823 to: Migrate your configurations Have your consumers install the new Service Bridge for Consumers application from the ServiceNow store. Test the new application with your consumers. Once it has been validated, remove the entitlements for the Service Bridge \(Legacy\) content and entitle the content for Service Bridge for Providers.

</td></tr><tr><td>

Service Bridge \(Legacy\) \[com.sn\_nowebonding\]

</td><td>

Deprecated in Xanadu

</td><td>

Allows customers to submit service requests to their provider and monitor these requests.

</td><td>

-   Install the [Service Bridge for Consumers](https://www.servicenow.com/docs/access?context=service-bridge-consumers-landing-page&version=yokohama&pubname=yokohama-service-bridge&ft:locale=en-US) application from the ServiceNow Store and review the documentation.
-   Reach out to your Service Bridge Provider to coordinate the migration to the new Service Bridge application. They’ll need to coordinate the migration with you along with any testing. Once ready, they’ll send you a registration link to connect the new application.

</td></tr><tr><td>

Jenkins plug-in for ServiceNow DevOps

</td><td>

Deprecated in Xanadu

</td><td>

The ServiceNow DevOps plugin extends the default behaviors of Jenkins, and provides a mechanism to control job executions via the ServiceNow Change Management application.

</td><td>

Install all future releases of this application directly from the [Jenkins store](https://plugins.jenkins.io/servicenow-devops/).

</td></tr><tr><td>

Human Resources Scoped App: Parental Journey \[com.sn\_hr\_parental\_journey\]

</td><td>

Deprecated in Xanadu

</td><td>

Provides a prepackaged configuration for parental leaves of absence \(LOAs\) in an HR organization. Parental LOAs include maternity, paternity, or adoption leave.

</td><td align="center">

—

</td></tr><tr><td>

Human Resources Scoped App: Data Migration \[sn\_hr\_migration\]

</td><td>

Deprecated in Xanadu

</td><td>

Allows you to migrate HR tables and roles from the non-scoped to the scoped version of HR.

</td><td align="center">

—

</td></tr><tr><td>

Service Graph Connector for Extra Hop\[com.snc.cmdb.extrahop\_integration\]

</td><td>

Deprecated in Xanadu

</td><td>

Provides capabilities to pull data from the ExtraHop application into your ServiceNow instance.

</td><td>

Install the Service Graph Connector for ExtraHop Reveal\(x\) application on the ServiceNow Store. This application is owned by ExtraHop.

</td></tr></tbody>
</table>## Plugins planned for deprecation

This table lists the existing plugins that were planned for deprecation in a future release.

<table id="table_xcl_5mj_tx"><thead><tr><th>

Plugin

</th><th>

Status

</th><th>

Description

</th><th>

Details

</th></tr></thead><tbody><tr><td>

Customer Service CTI Demo Data \[com.snc.customerservice\_cti\_demo\]

</td><td>

Planned for deprecation in the A release

</td><td>

Load demo data for CTI Softphone.

</td><td>

Install the ServiceNow Voice with Amazon Connect application and all its dependencies from the ServiceNow Store and review the [Integrate ServiceNow Voice with Amazon Connect](https://www.servicenow.com/docs/access?context=integrate-ccc-amazonconnect&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US) documentation.

</td></tr><tr><td>

Data Filtration \[com.glide.data\_filtration\]

</td><td>

Planned for deprecation in the A release

</td><td>

Controls the access to tables and records based on subject attributes when performing read queries.

</td><td>

Migrate to the Security Data Filter plugin, which is active by default on all instances on the Yokohama release or later.

</td></tr><tr><td>

Data Separation \[sn\_ds\]

</td><td>

Planned for deprecation in the A release

</td><td>

The ServiceNow Data Separation application helps organizations restrict access to sensitive data based on a lens hierarchy and its leaf node.

</td><td>

Use Data Filters and access control lists \(ACLs\) to configure data separation for your use cases. For details on how to enable data separation for different use cases using data filters and ACLs, see the [Managing data separation using data filters and ACLs \[KB0558290\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1772519) article in the Now Support Knowledge Base.

</td></tr><tr><td>

Gremlin Spoke \[sn\_gremlin\_spoke\]

</td><td>

Planned for deprecation December 2030 or contract term end date \(whichever is earlier\)

</td><td>

Simulate outages and manage attacks using Gremlin instance from your instance.

</td><td>

Install the Spoke Generator application from the ServiceNow Store, import API documentation for Gremlin, and use it to create actions/custom spokes.

</td></tr><tr><td>

Legal Simple Contracts \[sn\_lg\_contracts\]

</td><td>

Planned for deprecation in the B release

</td><td>

Enables employees to submit legal requests for getting legal support and guidance for contracts.

</td><td>

Install the Contract Management Pro application from the ServiceNow Store.

</td></tr><tr><td>

Microsoft Teams Spoke for ServiceNow IntegrationHub \[sn.ms\_teams.ah\]

</td><td>

Planned for deprecation May 2031 or contract term end date \(whichever is earlier\)

</td><td>

Configure the actions that a process analyst can use when creating configurations to automate sending messages about alerts to a Microsoft Teams channel.

</td><td>

Install the Microsoft Teams Graph Spoke application from the ServiceNow Store and review the [Migration Guide: Microsoft Teams Spoke for ServiceNow Integration Hub to Microsoft Teams Graph Spoke \[KB1650148\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1650148) article in the Now Support Knowledge Base.

</td></tr><tr><td>

Password Reset Orchestration Add-on \[com.glideapp.password\_reset.addon.orchestration\]

</td><td>

Planned for deprecation in the A release

</td><td>

Password reset add-on to enable the use of ServiceNow Orchestration. Includes support for Active Directory and remote SOAP-based credential systems.

</td><td>

Install the Password Reset integration for Microsoft Active Directory application from the ServiceNow Store and review the [Integrate Password Reset with your Active Directory service](https://www.servicenow.com/docs/access?context=t_ConPassResetActiveDir&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US) documentation.

</td></tr><tr><td>

Patient Support Services \[sn\_patientservice\]

</td><td>

Planned for deprecation November 2028 or contract term end date \(whichever is earlier\)

</td><td>

Streamlines the patient onboarding, education, and engagement for various patient support services such as discount plans, adherence programs, opioid, and diabetes management.

</td><td>

There is no replacement for this application.

</td></tr><tr><td>

Performance Analytics - Content Pack - GRC: Audit Management \[sn\_audit\_pa\]

</td><td>

Planned for deprecation in the A release

</td><td>

Provides Performance Analytics reports for the GRC Audit Management application.

</td><td>

Test the migrated GRC: Audit Management Core UI analytics assets in Platform Analytics.

</td></tr><tr><td>

Performance Analytics - Content Pack - GRC: Policy and Compliance Management \[sn\_compliance\_pa\]

</td><td>

Planned for deprecation in the A release

</td><td>

Provides Performance Analytics reports for the GRC Policy and Compliance Management application.

</td><td>

Test the migrated GRC: Policy and Compliance Management Core UI analytics assets in Platform Analytics.

</td></tr><tr><td>

Performance Analytics - Content Pack - GRC: Risk Management \[sn\_risk\_pa\]

</td><td>

Planned for deprecation in the A release

</td><td>

Provides Performance Analytics reports for the GRC Risk Management application.

</td><td>

Test the migrated GRC: Risk Management Core UI analytics assets in Platform Analytics.

</td></tr><tr><td>

Performance Analytics Content Pack - Vendor Management Workspace \[com.snc.sn\_itsm\_vendor\_pa\]

</td><td>

Planned for deprecation in the A release

</td><td>

Contains performance analytics indicators used by the Vendor Management Workspace.

</td><td>

There is no replacement for this application.

</td></tr><tr><td>

Pre-Visit Management \[sn\_previsit\]

</td><td>

Planned for deprecation October 2029 or contract term end date \(whichever is earlier\)

</td><td>

Streamlines the scheduling process of procedure requests for patients and increases visibility to pre-authorization approvals prior to scheduled procedures.

</td><td>

There is no replacement for this application.

</td></tr><tr><td>

Redox Electronic Health Record Spoke \[sn\_redox\_spoke\]

</td><td>

Planned for deprecation in the A release

</td><td>

Enable communications with your customers using the Redox platform from your ServiceNow instance.

</td><td>

There is no replacement for this application.

</td></tr><tr><td>

Redox Inbound Integration \[sn\_redox\]

</td><td>

Planned for deprecation in the A release

</td><td>

Use the real-time bidirectional data exchange with external healthcare systems via the Redox platform​.

</td><td>

There is no replacement for this application.

</td></tr><tr><td>

Security Incident Response UI \[com.app\_secops\_ui\]

</td><td>

Planned for deprecation in the A release

</td><td>

Provides an enhanced user interface for monitoring and resolving threats to an organization’s security. Activation of this plugin on production instances may require a separate license. Contact ServiceNow for details.

</td><td>

Install Security Incident Response version 13.4.5 or higher from the ServiceNow Store and review the [Security Incident Response Workspace](https://www.servicenow.com/docs/access?context=sir-workspace-landing-page&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US) documentation.

</td></tr><tr><td>

Service Credits \[com.sn\_service\_credits\]

</td><td>

Planned for deprecation in the A release

</td><td>

Track and manage the compensation that your vendors owe your organization when they breach the service agreement you have with them.

</td><td>

There is no replacement for this application.

</td></tr><tr><td>

Service Graph Connector for Microsoft Defender for IoT \(On-premises Management Console\) \[sn\_msftd4iotsgc\]

</td><td>

Planned for deprecation in the A release

</td><td>

Integrate Microsoft Defender for IoT \(On-premises Management Console\) with the ServiceNow Operational Technology Manager application to automate import of sensor appliances, OT devices, and network connections.

</td><td>

There is no replacement for this application.

</td></tr><tr><td>

SharePoint Online Search Connector \[com.snc.sharepoint\_online\]

</td><td>

Planned for deprecation in the A release

</td><td>

Offers a consumer-grade search configuration to manage your information resources.

</td><td>

Install the External Content Connectors ServiceNow application from the ServiceNow Store.

</td></tr><tr><td>

Vaccine Administration Management \[sn\_vaccine\_sm\]

</td><td>

Planned for deprecation October 2029 or contract term end date \(whichever is earlier\)

</td><td>

Enables governments and healthcare providers to deliver vaccines, on a deadline and with finite resources.

</td><td>

There is no replacement for this application.

</td></tr><tr><td>

Vendor Management Mobile \[com.sn\_vendor\_mobile\]

</td><td>

Planned for deprecation in the A release

</td><td>

Provides a mobile interface for vendor managers to view relevant information filtered by the vendors they are responsible for, as well as all other vendors.

</td><td>

There is no replacement for this application.

</td></tr><tr><td>

Vendor Management Workspace UI Components \[com.app\_itsm\_vendor\_components\]

</td><td>

Planned for deprecation in the A release

</td><td>

Contains a set of shared UI components used by Vendor Management products.

</td><td>

There is no replacement for this application.

</td></tr><tr><td>

Vendor Manager Workspace Demo Data \[com.snc.vmw.demo\]

</td><td>

Planned for deprecation in the A release

</td><td>

Provides demo data for Vendor Manager Workspace.

</td><td>

There is no replacement for this application.

</td></tr><tr><td>

Vulnerability Response Integration with Microsoft Defender for IoT \(On-premises Management Console\) \[sn\_msftd4iotvr\]

</td><td>

Planned for deprecation in the A release

</td><td>

Use the Vulnerability Response for Microsoft Defender for IoT \(On-premises Management Console\) application to track, prioritize, and resolve vulnerabilities on devices used in the production process.

</td><td>

There is no replacement for this application.

</td></tr></tbody>
</table>## Renamed and changed plugins

This table lists the existing plugins that were renamed or changed in Yokohama or Xanadu.

|Plugin|Status|Description|Details|
|------|------|-----------|-------|
|ERP Data Hub \[sn\_erp\_integration\]|Renamed in Yokohama|ERP Canvas \(Enterprise Resource Planning\) enables you to retrieve and update ERP data from the system of record, such as SAP.|This product used to be named ERP Canvas, then was changed to ERP Data Hub, and iswash now returning to ERP Canvas.|
|Smart Assessment Connected \[sn\_smart\_assessment\_connected\]|Renamed in Yokohama|Connected component for assessment instance.|Renamed to Smart Assessment Connected \[sn\_smart\_assessment\_conn\]|
|Smart Assessment Designer \[sn-smart-assessment-builder\]|Renamed in Yokohama|Connected component for assessment designer.|Renamed to Smart Assessment Designer \[sn\_smart\_asmt\_desg\]|
|Application Portfolio Management Core \[com.snc.apm\_core\]|Renamed in Xanadu|This plugin contains core functionality for Enterprise Architecture available out of the box by default.|Renamed to Enterprise Architecture Core \[com.snc.apm\_core\]|
|Read only roles for Application Portfolio Management \[com.snc.apm\_read\_roles\]|Renamed in Xanadu|The plugin provides read-only roles for Enterprise Architecture.|Renamed to Read only roles for Enterprise Architecture \[com.snc.apm\_read\_roles\]|
|Application Portfolio Management - TRM \[com.snc.apm\_trm\]|Renamed in Xanadu|This plugin includes TRM lifecycles for Enterprise Architecture.|Renamed to Enterprise Architecture - TRM \[com.snc.apm\_trm\]|
|Performance Analytics - Content Pack - Application Portfolio Management \[com.snc.pa.apm\]|Renamed in Xanadu|Enterprise Architecture dashboards developed using Performance analytics premium.|Renamed to Performance Analytics - Content Pack - Enterprise Architecture \[com.snc.pa.apm\]|
|Performance Analytics - Content Pack - Application Portfolio Management and Change Management \[com.snc.pa.apm.change\_request\]|Renamed in Xanadu|Provides integration of Enterprise Architecture with Change Management, which includes performance analytics dashboards of business applications associated with Change requests.|Renamed to Performance Analytics - Content Pack - Enterprise Architecture and Change Management \[com.snc.pa.apm.change\_request\]|
|Performance Analytics - Content Pack - Application Portfolio Management and Problem Management \[com.snc.pa.apm.problem\]|Renamed in Xanadu|Provides integration of Enterprise Architecture with Problem Management, which includes performance analytics dashboards of business applications.|Renamed to Performance Analytics - Content Pack - Enterprise Architecture and Problem Management \[com.snc.pa.apm.problem\]|
|Application Portfolio Management Digital Integration Management \[com.snc.apm\_digital\_integration\]|Renamed in Xanadu|Provides modeling and flow for managing digital integrations between business applications.|Renamed to Digital Integration Management plugin \[com.snc.apm\_di\]|
|Application Portfolio Management - Predictive Intelligence \[com.snc.apm.predictive\_intelligence\]|Renamed in Xanadu|This plugin provides Predictive Intelligence Solutions for Enterprise Architecture. It helps in prediction by applying algorithms like similarity on business applications-related data.|Renamed to Enterprise Architecture - Predictive Intelligence \[com.snc.apm.predictive\_intelligence\]|
|Application Portfolio Management - ATF Tests \[com.snc.apm.atf\]|Renamed in Xanadu|The plugin provides ATF test cases and test suites that can be run on Enterprise Architecture.|Renamed to Enterprise Architecture - ATF Tests \[com.snc.apm.atf\]|
|Application Portfolio Management \[com.snc.apm\]|Renamed in Xanadu|The plugin helps enterprises have visibility into their Business Applications Inventory, rationalize Business Applications, provide business context, and determine business value of each Business Application. It also helps with understanding of the technology \(Software and Hardware\) components of Business Applications, capture the organizations Information Assets and Business Applications use of those Information Assets.|Renamed to Enterprise Architecture \[com.snc.apm\]|

## Plugins in maintenance mode

This table lists the existing plugins that are in maintenance mode.

<table id="table_xcl_5mj_tx"><thead><tr><th>

Plugin

</th><th>

Status

</th><th>

Description

</th><th>

Details

</th></tr></thead><tbody><tr><td>

Advanced Work Assignment for CSM\[com.sn\_csm.awa\]

</td><td>

Maintenance mode only.

</td><td>

Activating Customer Service \(com.sn\_customerservice\) plugin will activate this plugin.

</td><td align="center">

—

</td></tr><tr><td>

CMS User Interface - Service Management Core\[com.snc.service\_management.core.cms\]

</td><td>

Maintenance mode only.

</td><td>

All Content Management System items \(blocks, pages, and menus\) used to reference core IT self-service applications are packaged in this plugin. It is also the core foundation for all Service Management applications.

</td><td align="center">

—

</td></tr><tr><td>

Content Management\[com.glide.cms\]

</td><td>

Maintenance mode only.

</td><td align="center">

—

</td><td align="center">

—

</td></tr><tr><td>

Content Management Extended Types\[com.glide.cms.types\]

</td><td>

Maintenance mode only.

</td><td class="description">

An extension to Content Management that adds iFrames and Flash frames.Use Service Portal for new development instead of CMS. Service Portal is an alternative to CMS with a refined user experience, and is active by default in the base system. For more information, see [Service Portal](https://www.servicenow.com/docs/access?context=c_ServicePortal&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US) and [Content Management and Service Portal](https://www.servicenow.com/docs/access?context=c_CMSAndSP&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US).

</td><td align="center">

—

</td></tr><tr><td>

Content Management IFrame Type\[com.glide.cms.type.iframe\]

</td><td>

Maintenance mode only.

</td><td align="center">

—

</td><td align="center">

—

</td></tr><tr><td>

Content Management Flash Type\[com.glide.cms.type.flash\]

</td><td>

Maintenance mode only.

</td><td align="center">

—

</td><td align="center">

—

</td></tr><tr><td>

CSM Account Hierarchy\[com.snc.sn\_csm\_account\_hierarchy\]

</td><td>

Maintenance mode only.

</td><td align="center">

—

</td><td align="center">

—

</td></tr><tr><td>

CSM Lookup and Verify\[com.snc.sn\_csm\_lookup\_verify\]

</td><td>

Maintenance mode only.

</td><td align="center">

—

</td><td align="center">

—

</td></tr><tr><td>

CSM Workspace - Components\[com.csm\_workspace\_components\]

</td><td>

Maintenance mode only.

</td><td align="center">

—

</td><td align="center">

—

</td></tr><tr><td>

Facilities Move Management\[com.snc.facilities\_service\_automation.move\]

</td><td>

Maintenance mode only.Planned for deprecation in March 2025 or subscription term end.

</td><td>

Enables single user move functionality as well as Enterprise Move and move planning functionality.

</td><td>

Transition to Workplace Service Delivery.

</td></tr><tr><td>

Facilities Service Management CMS Portal\[com.snc.facilities\_service\_automation.cms\]

</td><td>

Maintenance mode only.

</td><td align="center">

—

</td><td align="center">

—

</td></tr><tr><td>

Facilities Service Management Mobile\[com.snc.facilities\_service\_automation\_m\]

</td><td>

Maintenance mode only.

</td><td>

Manages facilities service management mobile components.

</td><td align="center">

—

</td></tr><tr><td>

Field Service Management CMS Portal\[com.snc.work\_management.cms\]

</td><td>

Maintenance mode only.

</td><td>

Lets you launch Field Service Automation and other service management applications from a single CMS page.

</td><td align="center">

—

</td></tr><tr><td>

Human Resources Application: Core CMS\[com.snc.hr.core.cms\]

</td><td>

Maintenance mode only.

</td><td>

Provides case and knowledge management for HR. Standardizes the documentation, interaction, and fulfillment of employee inquires and requests while having visibility into the quantity and type of cases coming in.

</td><td align="center">

—

</td></tr><tr><td>

Lookup and Verify\[com.snc.sn\_lookup\_and\_verify\_config\]

</td><td>

Maintenance mode only.

</td><td align="center">

—

</td><td align="center">

—

</td></tr><tr><td>

Service Catalog CMS Extension\[com.glideapp.servicecatalog.cms\]

</td><td>

Maintenance mode only.

</td><td>

Provides the ability to define the catalog experience within CMS.

</td><td align="center">

—

</td></tr></tbody>
</table>
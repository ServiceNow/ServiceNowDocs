---
title: Changes to plugins from Xanadu to Zurich
description: Before you upgrade from Xanadu to Zurich, read the release notes for information about new plugins and existing plugins that were deprecated, renamed, or changed in some way.This table lists the existing plugins that were deprecated in Xanadu, Yokohama, or Zurich.This table lists the existing plugins that were planned for deprecation in a future release.This table lists the existing plugins that were renamed or changed in Xanadu, Yokohama, or Zurich.This table lists the existing plugins that are in maintenance mode.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 16
breadcrumb: [Release notes for upgrading from Xanadu, Learn about the Zurich release, Zurich release notes]
---

# Changes to plugins from Xanadu to Zurich

Before you upgrade from Xanadu to Zurich, read the release notes for information about new plugins and existing plugins that were deprecated, renamed, or changed in some way.

## Xanadu and Yokohama plugin changes

See [Xanadu plugin changes](https://www.servicenow.com/docs/bundle/xanadu-release-notes/page/administer/plugins/reference/plugin-changes.html) for more information.

See [Yokohama plugin changes](https://www.servicenow.com/docs/bundle/yokohama-release-notes/page/administer/plugins/reference/plugin-changes.html) for more information.

## Deprecated plugins from Xanadu to Zurich

This table lists the existing plugins that were deprecated in Xanadu, Yokohama, or Zurich.

<table id="table_xcl_5mj_tx"><thead><tr><th>

Plugin

</th><th>

Status

</th><th>

Description

</th><th>

Details

</th></tr></thead><tbody><tr><td>

Agent Client Collector for Security Incident Response \[sn\_secops\_acc\]

</td><td>

Deprecated in Zurich

</td><td>

Automate security operations center \(SOC\) tasks for gathering details and enriching data.

</td><td>

Use the already installed Security Incident Response workflows and integrations or the ACC Spoke.

</td></tr><tr><td>

Aleph Alpha Spoke \[sn\_aleph\_alpha\_spk\]

</td><td>

Deprecated in Zurich

</td><td>

Aleph Alpha Spoke enables integration of Generative AI capabilities from Aleph Alpha in the Generative AI Controller store app. You can leverage the spoke via the Generative AI Controller Store App.

</td><td>

There is no replacement for this application.

</td></tr><tr><td>

Cloud Discovery setup using classic Cloud Discovery

</td><td>

Deprecated in Xanadu

</td><td>

Enables you to set up Cloud Discovery for performing cloud discovery and using Cloud Provisioning and Governance for managing discovered cloud resources.

</td><td>

Install Cloud Operations Workspace \(COW\) on the ServiceNow Store.

</td></tr><tr><td>

Cloud Migration Assessment \[sn\_cloud\_migration\]

</td><td>

Deprecated in Zurich

</td><td>

Plan and organize the process of relocating your enterprise IT resources and workloads to cloud platforms.

</td><td>

There is no replacement for this application.

</td></tr><tr><td>

Cloud Provisioning and Governance: Google Cloud Connector \[sn\_cmp\_gcp\]

</td><td>

Deprecated in Yokohama

</td><td>

Integrate Cloud Management Google Cloud Connector scoped application with CMP

</td><td>

Install the Cloud Provisioning and Governance: Terraform Connector application from the ServiceNow Store and review the [Cloud Services Catalog Terraform Connector](https://www.servicenow.com/docs/access?context=cpg-terraform-connector-landing-page&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US) documentation.

</td></tr><tr><td>

Cloud Spend Dashboard\[sn\_sam\_cld\_spend\]

</td><td>

Deprecated in Xanadu

</td><td>

Helps you view all cloud spend on a single dashboard, including software, platform, and infrastructure.

</td><td>

Install the Asset Executive Workspace on the ServiceNow Store.

</td></tr><tr><td>

Conversational Integration with Google Business Messages \[sn\_gbm\_adapter\]

</td><td>

Deprecated in Yokohama

</td><td>

Interact with requesters on the Google Business Messages app.

</td><td>

There is no replacement for this application.

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

Data Certification \[com.snc.certification\_v2\]

</td><td>

Deprecated in Zurich

</td><td>

Manage scheduled and on-demand validations of the configuration management database \(CMDB\) data.

</td><td>

Install the CMDB Workspace v6.0+ application \(compatible with Washington D.C. and later\) from the ServiceNow Store to use the CMDB Data Manager feature. See [Working with CMDB Data Manager](https://www.servicenow.com/docs/access?context=cmdb-data-management&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td>

Employee Campaigns for Workplace from Facebook\[com.snc.sn\_fb\_wp\_campaigns\]

</td><td>

Deprecated in Xanadu

</td><td>

Enables you to package your content into a campaign and publish the content to groups on Workplace from Facebook.

</td><td>

No replacement. If you are using this application, you have the option to maintain the unsupported application as custom code.

</td></tr><tr><td>

Employee Campaigns for Workplace from Facebook\[sn\_fb\_wp\_campaigns\]

</td><td>

Deprecated in Yokohama

</td><td>

Enables you to package your content into a campaign and publish the content to groups on Workplace from Facebook.

</td><td>

There is no replacement for this application. If you are using this application, you have the option to maintain the unsupported application as custom code.

</td></tr><tr><td>

Field Service Map\[com.snc.fsm\_map\]

</td><td>

Deprecated in Xanadu

</td><td>

Displays the dispatch map for viewing agents, tasks, and agent routes.

</td><td>

Install and configure the Field Service Dispatcher workspace. For guidance, see [Configuring Dispatcher Workspace](https://www.servicenow.com/docs/access?context=configuring-dispatcher-workspace&version=zurich&pubname=zurich-field-service-management&ft:locale=en-US).

</td></tr><tr><td>

FSM Agent Classic Workspace\[com.snc.agent\_workspace.fsm\]

</td><td>

Deprecated in Xanadu

</td><td align="center">

—

</td><td>

Install and configure the Field Service Dispatcher workspace. For guidance, see [Configuring Dispatcher Workspace](https://www.servicenow.com/docs/access?context=configuring-dispatcher-workspace&version=zurich&pubname=zurich-field-service-management&ft:locale=en-US).

</td></tr><tr><td>

Global Reporting Initiative \(GRI\) Content Accelerator for ESG\[com.sn\_esg\_gri\]

</td><td>

Deprecated in Xanadu

</td><td>

Offers ESG frameworks such as authority documents and citations and provides the related metric definitions.

</td><td>

Install the ESG Content Accelerator application from the ServiceNow Store. For guidance, see [ESG content accelerator](https://www.servicenow.com/docs/access?context=esg-content-accelerator&version=zurich&pubname=zurich-environmental-social-governance&ft:locale=en-US).

</td></tr><tr><td>

HR Agent Mobile\[com.sn\_hr\_mobile\_agent\]

</td><td>

Deprecated in Xanadu

</td><td align="center">

—

</td><td>

No replacement. If you are using this plugin, you have the option to maintain the unsupported plugin as custom code.

</td></tr><tr><td>

HR Agent Workspace\[com.sn\_hr\_agent\_workspace\]

</td><td>

Deprecated in Xanadu

</td><td>

Use the HR Service Delivery Agent Workspace to interact with employees, respond to inquiries, and resolve issues quickly.

</td><td>

Install and configure the HRSD Configurable Agent Workspace for Case Management. For guidance, see [Agent Workspace for HR Case Management](https://www.servicenow.com/docs/access?context=agent-ws-hr-case-mgmt-landing-page&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US) and this [Community Article](https://www.servicenow.com/community/hrsd-articles/hr-agent-workspace-migration-guidelines-from-classic-to/ta-p/2310606).

</td></tr><tr><td>

HR Service Delivery v1.0 \(Legacy\)\[com.snc.hr.core.cms, com.snc.hr.core, com.snc.hr.hr\_connect, con.snc.hr.pa, com.snc.hr.service\_portal\]

</td><td>

Deprecated in Xanadu

</td><td>

Unlocks enterprise productivity and give your employees the service experience they deserve.

</td><td>

Migrate to the Human Resources Core v2.0 scoped application \[com.sn\_hr\_core\].

</td></tr><tr><td>

Human Resources Scoped App: Data Migration \[sn\_hr\_migration\]

</td><td>

Deprecated in Xanadu

</td><td>

Allows you to migrate HR tables and roles from the non-scoped to the scoped version of HR.

</td><td align="center">

—

</td></tr><tr><td>

Human Resources Scoped App: Parental Journey \[com.sn\_hr\_parental\_journey\]

</td><td>

Deprecated in Xanadu

</td><td>

Provides a prepackaged configuration for parental leaves of absence \(LOAs\) in an HR organization. Parental LOAs include maternity, paternity, or adoption leave.

</td><td align="center">

—

</td></tr><tr><td>

IBM Watson Language Translator Service Spoke \[com.glide.ibm\_translation\_spoke\]

</td><td>

Deprecated in Yokohama

</td><td>

In ServiceNow's Dynamic Translation app, this spoke connected to the third-party machine translation service provided by IBM Watson

</td><td>

As an alternative, customers can create accounts with other third-party translation services such as Google or Microsoft Azure

</td></tr><tr><td>

IE11 Support for Virtual Agent\[com.glide.cs.chatbot, com.glide.cs.chatbot.lite\]

</td><td>

Support ended for the IE11 browser.

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Instance Security Center\[sn\_isc\_core, sn\_isc\_nlu, sn\_isc\_va\]

</td><td>

Deprecated in Xanadu

</td><td>

Monitors the compliance level of instance security controls, view security event monitoring metrics, and configure and maintain instance security settings all from within the Instance Security Center.

</td><td>

Install ServiceNow Security Center on the ServiceNow Store. For guidance, see .

</td></tr><tr><td>

Jenkins plug-in for ServiceNow DevOps

</td><td>

Deprecated in Xanadu

</td><td>

The ServiceNow DevOps plugin extends the default behaviors of Jenkins, and provides a mechanism to control job executions via the ServiceNow Change Management application.

</td><td>

Install all future releases of this application directly from the [Jenkins store](https://plugins.jenkins.io/servicenow-devops/).

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

Service Bridge \(Legacy\) \[com.sn\_nowebonding\]

</td><td>

Deprecated in Xanadu

</td><td>

Allows customers to submit service requests to their provider and monitor these requests.

</td><td>

-   Install the [Service Bridge for Consumers](https://www.servicenow.com/docs/access?context=service-bridge-consumers-landing-page&version=zurich&pubname=zurich-service-bridge&ft:locale=en-US) application from the ServiceNow Store and review the documentation.
-   Reach out to your Service Bridge Provider to coordinate the migration to the new Service Bridge application. They’ll need to coordinate the migration with you along with any testing. Once ready, they’ll send you a registration link to connect the new application.

</td></tr><tr><td>

Service Bridge for Providers \(Legacy\) \[com.sn\_nowebonding\_provider\]

</td><td>

Deprecated in Xanadu

</td><td>

Allows providers to publish catalogs for customers and receive and fulfill customer service requests.

</td><td>

-   Install the [Service Bridge for Providers](https://www.servicenow.com/docs/access?context=service-bridge-providers-landing-page&version=zurich&pubname=zurich-service-bridge&ft:locale=en-US) application from the ServiceNow Store and review the documentation.
-   Follow the guidance in KB1499823 to: Migrate your configurations Have your consumers install the new Service Bridge for Consumers application from the ServiceNow store. Test the new application with your consumers. Once it has been validated, remove the entitlements for the Service Bridge \(Legacy\) content and entitle the content for Service Bridge for Providers.

</td></tr><tr><td>

Service Graph Connector for Extra Hop\[com.snc.cmdb.extrahop\_integration\]

</td><td>

Deprecated in Xanadu

</td><td>

Provides capabilities to pull data from the ExtraHop application into your ServiceNow instance.

</td><td>

Install the Service Graph Connector for ExtraHop Reveal\(x\) application on the ServiceNow Store. This application is owned by ExtraHop.

</td></tr><tr><td>

Sustainability Accounting Standards Board \(SASB\) Content Accelerator for ESG\[com.sn\_esg\_sasb\]

</td><td>

Deprecated in Xanadu

</td><td>

The SASB Accelerator is designed for use with the ESG Management and Reporting application to enable customers to easily adopt the SASB framework to produce their ESG disclosures.

</td><td>

Install the ESG Content Accelerator application from the ServiceNow Store. For guidance, see [ESG content accelerator](https://www.servicenow.com/docs/access?context=esg-content-accelerator&version=zurich&pubname=zurich-environmental-social-governance&ft:locale=en-US).

</td></tr></tbody>
</table>## Plugins planned for deprecation

This table lists the existing plugins that were planned for deprecation in a future release.

|Plugin|Status|Description|Details|
|------|------|-----------|-------|
|Automation Discovery \[sn\_auto\_discovery\]|Planned for deprecation in the B release|Identifies opportunities that can be automated by ServiceNow products, such as Virtual Agent, Auto-Routing, and Agent Assist.|There is no replacement for this application.|
|Cloud Discovery Workspace \[sn\_cloud\_ops\_ws\]|Planned for deprecation in the B release|Manage the cloud operations of your organization.|Use the already installed Discovery Admin Workspace application.|
|Conversational Integration with Facebook Messenger \[sn\_va\_fb\_messenger\]|Planned for deprecation in September 2025|Enable brands to engage with their customers using the Facebook Messenger app.|There is no replacement for this application.|
|CTI Softphone \[com.snc.cti\]|Planned for deprecation in the B release|Enables Twilio integration using Notify and OpenFrame to provide softphone functions and call center capabilities.|Install the ServiceNow Voice with Amazon Connect application from the ServiceNow Store.|
|Customer Service Case Types \[com.snc.csm\_case\_types\]|Planned for deprecation in the B release|Manage complex case processes by defining new case types.|Upgrade the instance to Zurich or higher release versions.|
|Document Intelligence Admin \[sn\_docintel\_admin\]|Planned for deprecation in the B release|Provides a dedicated administration experience for Document Intelligence.|Install the Now Assist for Platform application from the ServiceNow Store.|
|Guided Application Creator \[com.glide.sn-guided-app-creator\]|Planned for deprecation in the B release|Quickly and effortlessly create new applications.|Install the ServiceNow Studio application from the ServiceNow Store.|
|Learning Posts \[sn\_lnp\]|Planned for deprecation in the B release|Empower employees by delivering in-moment learning experiences and personalized learning recommendations when and where employees need it.|Install the Journey Designer v6.0.0 application from the ServiceNow Store.|
|Listening Posts \[sn\_lp\]|Planned for deprecation in the B release|Capture employee feedback across various touch points, gain insights, and take action to quickly improve the employee service experience.|Install the Employee Center Pro application from the ServiceNow Store and use Integrated Experience and Service Feedback.|
|Now Assist for Service Graph Connectors \[sn\_nowassist\_sgc\]|Planned for deprecation in March 2030|Get easy-to-understand assistance with setting up, managing, and troubleshooting Service Graph Connectors, reducing manual effort and decreasing the time required to succeed.|Uninstall the Now Assist for Service Graph Connector and install the Now Assist for Configuration Management Database \(CMDB\) v2.1.0.|
|Retail Task Management Core \[com.sn\_retail\_task\_management\_core\]|Planned for deprecation in the A release|Optimize the planning, organizing, and assigning of tasks to staff in retail environment.|Use retail case types \(HQ communications\) along with the task plan template plugin for retail task management.|
|Sensitive Data Handling \[com.glide.sensitive\_data\_handling\]|Planned for deprecation in the B release|Detects and masks sensitive data shared by users of both conversational and non-conversational channels.|Install the Data Privacy application from the ServiceNow Store.|
|Service Creator \[com.glide.service\_creator \]|Planned for deprecation in the B release|Service creator makes it easy for departments to create their own services in the catalog.|Install the Creator Studio application from the ServiceNow Store.|
|Studio \[com.glide.dev-studio\]|Planned for deprecation in the B release|Provides an Integrated Development Environment \(IDE\)-like interface for application developers to work on custom applications in one centralized location.|Install the ServiceNow Studio application from the ServiceNow Store.|
|Password Reset Orchestration Add-on \[com.glideapp.password\_reset.addon.orchestration\]|Planned for deprecation in the A release|Password reset add-on to enable the use of ServiceNow Orchestration. Includes support for Active Directory and remote SOAP-based credential systems.|Install the Password Reset integration for Microsoft Active Directory application from the ServiceNow Store and review the [Integrate Password Reset with your Active Directory service](https://www.servicenow.com/docs/access?context=t_ConPassResetActiveDir&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US) documentation.|
|Patient Support Services \[sn\_patientservice\]|Planned for deprecation November 2028 or contract term end date \(whichever is earlier\)|Streamlines the patient onboarding, education, and engagement for various patient support services such as discount plans, adherence programs, opioid, and diabetes management.|There is no replacement for this application.|
|Performance Analytics - Content Pack - GRC: Audit Management \[sn\_audit\_pa\]|Planned for deprecation in the A release|Provides Performance Analytics reports for the GRC Audit Management application.|Test the migrated GRC: Audit Management Core UI analytics assets in Platform Analytics.|
|Performance Analytics - Content Pack - GRC: Policy and Compliance Management \[sn\_compliance\_pa\]|Planned for deprecation in the A release|Provides Performance Analytics reports for the GRC Policy and Compliance Management application.|Test the migrated GRC: Policy and Compliance Management Core UI analytics assets in Platform Analytics.|
|Performance Analytics - Content Pack - GRC: Risk Management \[sn\_risk\_pa\]|Planned for deprecation in the A release|Provides Performance Analytics reports for the GRC Risk Management application.|Test the migrated GRC: Risk Management Core UI analytics assets in Platform Analytics.|
|Pre-Visit Management \[sn\_previsit\]|Planned for deprecation October 2029 or contract term end date \(whichever is earlier\)|Streamlines the scheduling process of procedure requests for patients and increases visibility to pre-authorization approvals prior to scheduled procedures.|There is no replacement for this application.|
|Redox Electronic Health Record Spoke \[sn\_redox\_spoke\]|Planned for deprecation in the A release|Enable communications with your customers using the Redox platform from your ServiceNow instance.|There is no replacement for this application.|
|Redox Inbound Integration \[sn\_redox\]|Planned for deprecation in the A release|Use the real-time bidirectional data exchange with external healthcare systems via the Redox platform​.|There is no replacement for this application.|
|Security Incident Response UI \[com.app\_secops\_ui\]|Planned for deprecation in the A release|Provides an enhanced user interface for monitoring and resolving threats to an organization’s security. Activation of this plugin on production instances may require a separate license. Contact ServiceNow for details.|Install Security Incident Response version 13.4.5 or higher from the ServiceNow Store and review the [Security Incident Response Workspace](https://www.servicenow.com/docs/access?context=sir-workspace-landing-page&version=zurich&pubname=zurich-security-management&ft:locale=en-US) documentation.|
|Service Graph Connector for Microsoft Defender for IoT \(On-premises Management Console\) \[sn\_msftd4iotsgc\]|Planned for deprecation in the A release|Integrate Microsoft Defender for IoT \(On-premises Management Console\) with the ServiceNow Operational Technology Manager application to automate import of sensor appliances, OT devices, and network connections.|There is no replacement for this application.|
|SharePoint Online Search Connector \[com.snc.sharepoint\_online\]|Planned for deprecation in the A release|Offers a consumer-grade search configuration to manage your information resources.|Install the External Content Connectors ServiceNow application from the ServiceNow Store.|
|Vaccine Administration Management \[sn\_vaccine\_sm\]|Planned for deprecation October 2029 or contract term end date \(whichever is earlier\)|Enables governments and healthcare providers to deliver vaccines, on a deadline and with finite resources.|There is no replacement for this application.|
|Vulnerability Response Integration with Microsoft Defender for IoT \(On-premises Management Console\) \[sn\_msftd4iotvr\]|Planned for deprecation in the A release|Use the Vulnerability Response for Microsoft Defender for IoT \(On-premises Management Console\) application to track, prioritize, and resolve vulnerabilities on devices used in the production process.|There is no replacement for this application.|

## Renamed and changed plugins from Xanadu to Zurich

This table lists the existing plugins that were renamed or changed in Xanadu, Yokohama, or Zurich.

|Plugin|Status|Description|Details|
|------|------|-----------|-------|
|Application Portfolio Management \[com.snc.apm\]|Renamed in Xanadu|The plugin helps enterprises have visibility into their Business Applications Inventory, rationalize Business Applications, provide business context, and determine business value of each Business Application. It also helps with understanding of the technology \(Software and Hardware\) components of Business Applications, capture the organizations Information Assets and Business Applications use of those Information Assets.|The plugin name is changed to Enterprise Architecture \[com.snc.apm\]|
|Application Portfolio Management - ATF Tests \[com.snc.apm.atf\]|Renamed in Xanadu|The plugin provides ATF test cases and test suites that can be run on Enterprise Architecture.|The plugin name is changed to Enterprise Architecture - ATF Tests \[com.snc.apm.atf\]|
|Application Portfolio Management Core \[com.snc.apm\_core\]|Renamed in Xanadu|This plugin contains core functionality for Enterprise Architecture available out of the box by default.|The plugin name is changed to Enterprise Architecture Core \[com.snc.apm\_core\]|
|Application Portfolio Management Digital Integration Management \[com.snc.apm\_digital\_integration\]|Renamed in Xanadu|Provides modeling and flow for managing digital integrations between business applications.|The plugin name is changed to Digital Integration Management plugin \[com.snc.apm\_di\]|
|Application Portfolio Management - Predictive Intelligence \[com.snc.apm.predictive\_intelligence\]|Renamed in Xanadu|This plugin provides Predictive Intelligence Solutions for Enterprise Architecture. It helps in prediction by applying algorithms like similarity on business applications-related data.|The plugin name is changed to Enterprise Architecture - Predictive Intelligence \[com.snc.apm.predictive\_intelligence\]|
|Application Portfolio Management - TRM \[com.snc.apm\_trm\]|Renamed in Xanadu|This plugin includes TRM lifecycles for Enterprise Architecture.|The plugin name is changed to Enterprise Architecture - TRM \[com.snc.apm\_trm\]|
|ERP Data Hub \[sn\_erp\_integration\]|Renamed in Yokohama|ERP Canvas \(Enterprise Resource Planning\) enables you to retrieve and update ERP data from the system of record, such as SAP.|This product used to be named ERP Canvas, then was changed to ERP Data Hub, and is now returning to ERP Canvas.|
|Performance Analytics - Content Pack - Application Portfolio Management \[com.snc.pa.apm\]|Renamed in Xanadu|Enterprise Architecture dashboards developed using Performance analytics premium.|The plugin name is changed to Performance Analytics - Content Pack - Enterprise Architecture \[com.snc.pa.apm\]|
|Performance Analytics - Content Pack - Application Portfolio Management and Change Management \[com.snc.pa.apm.change\_request\]|Renamed in Xanadu|Provides integration of Enterprise Architecture with Change Management, which includes performance analytics dashboards of business applications associated with Change requests.|The plugin name is changed to Performance Analytics - Content Pack - Enterprise Architecture and Change Management \[com.snc.pa.apm.change\_request\]|
|Performance Analytics - Content Pack - Application Portfolio Management and Problem Management \[com.snc.pa.apm.problem\]|Renamed in Xanadu|Provides integration of Enterprise Architecture with Problem Management, which includes performance analytics dashboards of business applications.|The plugin name is changed to Performance Analytics - Content Pack - Enterprise Architecture and Problem Management \[com.snc.pa.apm.problem\]|
|Read only roles for Application Portfolio Management \[com.snc.apm\_read\_roles\]|Renamed in Xanadu|The plugin provides read-only roles for Enterprise Architecture.|The plugin name is changed to Read only roles for Enterprise Architecture \[com.snc.apm\_read\_roles\]|
|SAM Workspace plugin \[com.sn\_sam\_workspace\]|Replaced by a store application in Zurich|Store application required to use the Software Asset Workspace, the new user interface of the Software Asset Management application.|The SAM Workspace plugin \[com.sn\_sam\_workspace\] has been moved from the family release to the Software Asset Management store application.|
|Smart Assessment Connected \[sn\_smart\_assessment\_connected\]|Renamed in Yokohama|Connected component for assessment instance.|Renamed to Smart Assessment Connected \[sn\_smart\_assessment\_conn\]|
|Smart Assessment Designer \[sn-smart-assessment-builder\]|Renamed in Yokohama|Connected component for assessment designer.|Renamed to Smart Assessment Designer \[sn\_smart\_asmt\_desg\]|

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

An extension to Content Management that adds iFrames and Flash frames.Use Service Portal for new development instead of CMS. Service Portal is an alternative to CMS with a refined user experience, and is active by default in the base system. For more information, see [Service Portal](https://www.servicenow.com/docs/access?context=c_ServicePortal&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US) and [Content Management and Service Portal](https://www.servicenow.com/docs/access?context=c_CMSAndSP&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US).

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
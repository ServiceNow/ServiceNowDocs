---
title: Changes to plugins in the Zurich release
description: This table lists the existing plugins that were deprecated, planned for deprecation, renamed, or changed in some way.This table lists the existing plugins that were deprecated in Zurich and Yokohama that weren't previously listed as planned for deprecation.This table lists the existing plugins that were planned for deprecation in a future release.This table lists the existing plugins that were renamed or changed in Zurich or Yokohama.This table lists the existing plugins that are in maintenance mode.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 11
breadcrumb: [Release notes for upgrading from Yokohama, Learn about the Zurich release, Zurich release notes]
---

# Changes to plugins in the Zurich release

This table lists the existing plugins that were deprecated, planned for deprecation, renamed, or changed in some way.

-   Planned for deprecation: In preparation for the future deprecation. The application is being prepared for future deprecation. The plugin will be hidden and no longer available for activation but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support knowledge base.
-   Deprecated: The application is no longer deployed, enhanced, or supported. For details, see the [Deprecation Process \[KB0867184\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support knowledge base.
-   Maintenance mode: The application will have no new enhancements or activations but will have continued support.

## Deprecated plugins

This table lists the existing plugins that were deprecated in Zurich and Yokohama that weren't previously listed as planned for deprecation.

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

Cloud Migration Assessment \[sn\_cloud\_migration\]

</td><td>

Deprecated in Zurich

</td><td>

Plan and organize the process of relocating your enterprise IT resources and workloads to cloud platforms.

</td><td>

There is no replacement for this application.

</td></tr><tr><td>

Timeline Visualization/CIO Roadmap \[com.snc.timeline\_visualization\]

</td><td>

Deprecated in Zurich

</td><td>

Enables graphical representation of activities over time to provide a high-level view of strategic and operational activities in your organization such as incidents, problems, changes, and projects.

</td><td>

Install the [Portfolio Planning](https://store.servicenow.com/sn_appstore_store.do#!/store/application/9aa0eddcc70c2010d302670f6ec260c4/8.2.0?referer=%2Fstore%2Fsearch%3Flistingtype%3Dallintegrations%25253Bancillary_app%25253Bcertified_apps%25253Bcontent%25253Bindustry_solution%25253Boem%25253Butility%25253Btemplate%25253Bgenerative_ai%25253Bsnow_solution%26q%3Dportfolio%2520planning&sl=sh) \(standard customers\) or [Strategic Planning](https://store.servicenow.com/sn_appstore_store.do#!/store/application/a38ac49ccbf511104abddcbcf7076dec/4.1.3?referer=%2Fstore%2Fsearch%3Flistingtype%3Dallintegrations%25253Bancillary_app%25253Bcertified_apps%25253Bcontent%25253Bindustry_solution%25253Boem%25253Butility%25253Btemplate%25253Bgenerative_ai%25253Bsnow_solution%26q%3Dportfolio%2520planning&sl=sh) \(Pro customers\) application from the ServiceNow Store. Review the [Planning roadmaps in Portfolio Planning](https://www.servicenow.com/docs/access?context=planning-roadmaps-in-portfolio-planning&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US) or [Roadmaps in Strategic Planning](https://www.servicenow.com/docs/access?context=roadmap-planning-overview&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US) documentation for guidance on the roadmap functionality available within these workspaces. Migrate to the Portfolio Planning Workspace \(SPM Standard\) application that provides latest experience for this functionality.

</td></tr><tr><td>

Data Certification \[com.snc.certification\_v2\]

</td><td>

Deprecated in Zurich

</td><td>

Manage scheduled and on-demand validations of the configuration management database \(CMDB\) data.

</td><td>

Install the CMDB Workspace v6.0+ application \(compatible with Washington D.C. and later\) from the ServiceNow Store to use the CMDB Data Manager feature. See [Working with CMDB Data Manager](https://www.servicenow.com/docs/access?context=cmdb-data-management&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td>

Cloud Provisioning and Governance: Google Cloud Connector \[sn\_cmp\_gcp\]

</td><td>

Deprecated in Yokohama

</td><td>

Integrate Cloud Management Google Cloud Connector scoped application with CMP.

</td><td>

Install the Cloud Provisioning and Governance: Terraform Connector application from the ServiceNow Store and review the [Cloud Services Catalog Terraform Connector](https://www.servicenow.com/docs/access?context=cpg-terraform-connector-landing-page&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US) documentation.

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

In ServiceNow's Dynamic Translation app, this spoke connected to the third-party machine translation service provided by IBM Watson.

</td><td>

As an alternative, customers can create accounts with other third-party translation services such as Google or Microsoft Azure.

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

## Renamed and changed plugins

This table lists the existing plugins that were renamed or changed in Zurich or Yokohama.

|Plugin|Status|Description|Details|
|------|------|-----------|-------|
|SAM Workspace plugin \[com.sn\_sam\_workspace\]|Replaced by a store application in Zurich|Store application required to use the Software Asset Workspace, the new user interface of the Software Asset Management application.|The SAM Workspace plugin \[com.sn\_sam\_workspace\] has been moved from the family release to the Software Asset Management store application.|
|ERP Data Hub \[sn\_erp\_integration\]|Renamed in Yokohama|ERP Canvas \(Enterprise Resource Planning\) enables you to retrieve and update ERP data from the system of record, such as SAP.|This product used to be named ERP Canvas, then was changed to ERP Data Hub, and iswash now returning to ERP Canvas.|
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
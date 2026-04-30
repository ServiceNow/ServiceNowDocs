---
title: Changes to plugins in the Xanadu release
description: This table lists the existing plugins that were deprecated, planned for deprecation, renamed, or changed in some way.This table lists the existing plugins that were deprecated in Xanadu and Washington DC that weren't previously listed as planned for deprecation.This table lists the existing plugins that were planned for deprecation in a future release.This table lists the existing plugins that were renamed or changed in Xanadu or Washington DC.This table lists the existing plugins that are in maintenance mode.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 20
breadcrumb: [Release notes for upgrading from Washington DC, Learn about the Xanadu release, Xanadu release notes]
---

# Changes to plugins in the Xanadu release

This table lists the existing plugins that were deprecated, planned for deprecation, renamed, or changed in some way.

-   Planned for deprecation: In preparation for the future deprecation. The application is being prepared for future deprecation. The plugin will be hidden and no longer available for activation but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support knowledge base.
-   Deprecated: The application is no longer deployed, enhanced, or supported. For details, see the [Deprecation Process \[KB0867184\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support knowledge base.
-   Maintenance mode: The application will have no new enhancements or activations but will have continued support.

## Deprecated plugins

This table lists the existing plugins that were deprecated in Xanadu and Washington DC that weren't previously listed as planned for deprecation.

<table id="table_xcl_5mj_tx"><thead><tr><th>

Plugin

</th><th>

Status

</th><th>

Description

</th><th>

Details

</th></tr></thead><tbody><tr><td>

HR Agent Workspace\[com.sn\_hr\_agent\_workspace\]

</td><td>

Deprecated in Xanadu

</td><td>

Use the HR Service Delivery Agent Workspace to interact with employees, respond to inquiries, and resolve issues quickly.

</td><td>

Install and configure the HRSD Configurable Agent Workspace for Case Management. For guidance, see [Agent Workspace for HR Case Management \(Configurable\)](https://www.servicenow.com/docs/access?context=agent-ws-hr-case-mgmt-landing-page&version=xanadu&pubname=xanadu-employee-service-management&ft:locale=en-US) and this [Community Article](https://www.servicenow.com/community/hrsd-articles/hr-agent-workspace-migration-guidelines-from-classic-to/ta-p/2310606).

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

Install and configure the Field Service Dispatcher workspace. For guidance, see [Configuring Dispatcher Workspace](https://www.servicenow.com/docs/access?context=configuring-dispatcher-workspace&version=xanadu&pubname=xanadu-field-service-management&ft:locale=en-US).

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

Install ServiceNow Security Center on the ServiceNow Store. For guidance, see [Security Center](https://www.servicenow.com/docs/access?context=sec-center-v2&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US).

</td></tr><tr><td>

Field Service Map\[com.snc.fsm\_map\]

</td><td>

Deprecated in Xanadu

</td><td>

Displays the dispatch map for viewing agents, tasks, and agent routes.

</td><td>

Install and configure the Field Service Dispatcher workspace. For guidance, see [Configuring Dispatcher Workspace](https://www.servicenow.com/docs/access?context=configuring-dispatcher-workspace&version=xanadu&pubname=xanadu-field-service-management&ft:locale=en-US).

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

Install the ESG Content Accelerator application from the ServiceNow Store. For guidance, see [ESG content accelerator](https://www.servicenow.com/docs/access?context=esg-content-accelerator&version=xanadu&pubname=xanadu-environmental-social-governance&ft:locale=en-US).

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

Install the ESG Content Accelerator application from the ServiceNow Store. For guidance, see [ESG content accelerator](https://www.servicenow.com/docs/access?context=esg-content-accelerator&version=xanadu&pubname=xanadu-environmental-social-governance&ft:locale=en-US).

</td></tr><tr><td>

Service Bridge for Providers \(Legacy\) \[com.sn\_nowebonding\_provider\]

</td><td>

Deprecated in Xanadu

</td><td>

Allows providers to publish catalogs for customers and receive and fulfill customer service requests.

</td><td>

-   Install the [Service Bridge for Providers](https://www.servicenow.com/docs/access?context=service-bridge-providers-landing-page&version=xanadu&pubname=xanadu-service-bridge&ft:locale=en-US) application from the ServiceNow Store and review the documentation.
-   Follow the guidance in KB1499823 to: Migrate your configurations Have your consumers install the new Service Bridge for Consumers application from the ServiceNow store. Test the new application with your consumers. Once it has been validated, remove the entitlements for the Service Bridge \(Legacy\) content and entitle the content for Service Bridge for Providers.

</td></tr><tr><td>

Service Bridge \(Legacy\) \[com.sn\_nowebonding\]

</td><td>

Deprecated in Xanadu

</td><td>

Allows customers to submit service requests to their provider and monitor these requests.

</td><td>

-   Install the [Service Bridge for Consumers](https://www.servicenow.com/docs/access?context=service-bridge-consumers-landing-page&version=xanadu&pubname=xanadu-service-bridge&ft:locale=en-US) application from the ServiceNow Store and review the documentation.
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

</td></tr><tr><td>

Cloud Native Operations \[sn\_k8s\]

</td><td>

Deprecated in Washington DC

</td><td>

Use Cloud Native Operations to perform continuous discovery and monitoring of the Kubernetes platforms.

</td><td>

Install the Agent Client Collector for Visibility \(ACC-V\) application from the ServiceNow Store and review the [Agent Client Collector for Visibility](https://www.servicenow.com/docs/access?context=acc-visibility-landing-page&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US) documentation.

</td></tr><tr><td>

Item Designer \[com.glideapp.servicecatalog.item\_designer\]

</td><td>

Deprecated in Washington DC

</td><td>

The Service Catalog item designer enables non-administrators to create, maintain, and publish catalog items. It uses a structured design and publishing process to ensure consistency of usage.

</td><td>

The Catalog Builder plugin is activated by default on all instances \(com.glideapp.servicecatalog.catalog\_builder\).

</td></tr><tr><td>

CSM Agent Workspace \[com.snc.agent\_workspace.csm\]

</td><td>

Deprecated in Washington DC

</td><td>

CSM Agent Workspace enables you to integrate Customer Service Management with other applications.

</td><td>

Install the CSM Configurable Workspace application from the ServiceNow Store.

</td></tr><tr><td>

Customer Service Management for Orders \[com.snc.csm.order\]

</td><td>

Deprecated in Washington DC

</td><td>

The Customer Service Management for Orders feature adds support for orders and order line items to the Customer Service Management application.

</td><td>

Install the Order Management store application.

</td></tr><tr><td>

Product Model and Catalog Items Relationship \[com.snc.product\_catalog\_relationship\]

</td><td>

Deprecated in Washington DC

</td><td>

Enables self-service for customers to request services on products by creating relationships between product models and catalog items.

</td><td>

Install the Customer Service Case Types plugin \(com.snc.csm\_case\_types\) and use the service definition feature.

</td></tr><tr><td>

Central Dispatch \[com.snc.central\_dispatch\]

</td><td>

Deprecated in Washington DC

</td><td>

Provides both a list and calendar view of unassigned tasks.

</td><td>

Install and configure the Dispatcher Workspace plugin \(com.snc.uib.fsm\_dispatcher\_workspace\).

</td></tr><tr><td>

Journey Accelerator v4.0.3 and below \[com.sn\_ja\]

</td><td>

Deprecated in Washington DC

</td><td>

Helps to create templates for plans and to-do tasks. Managers then use the templates to create and publish customized plans for key employee transitions. Managers, employees, and mentors can access the plans from the Employee Center \(EC\).

</td><td>

Migrate to a replacement Journey Designer application. Journey designer will automatically install Journey Accelerator v5.0+ which is the supported version with Journey designer.

</td></tr><tr><td>

Mobile Studio \[com.glide.sg-studio\]

</td><td>

Deprecated in Washington DC

</td><td>

Use Mobile Studio to create and modify mobile components for use in any of the ServiceNow mobile apps.

</td><td>

Transition to replacement Mobile App Builder.

</td></tr><tr><td>

HTML Processor

</td><td>

Deprecated in Washington DC

</td><td align="center">

—

</td><td>

Review KB1119956 for steps to disable this feature on your instance.

</td></tr><tr><td>

Badge Reader Integration for Walk-up Experience \(Removed from com.snc.badge\_reader\)

</td><td>

Deprecated in Washington DC

</td><td>

Improve Walk-up Experience user satisfaction by using the Badge Reader Integration application at your on-site walk-up queue locations.

</td><td>

Review the guidance for building a customer badge reader client.

</td></tr><tr><td>

ITSM Agent Workspace and CMDB Agent Workspace \[com.snc.agent\_workspace.itsm, com.snc.agent\_workspace.itsm.landing\_page, com.snc.agent\_workspace.itsm.landing\_page\_premium, com.cmdb-workspace\]

</td><td>

Deprecated in Washington DC

</td><td>

Improve your ITSM agent experience and manage your IT fulfillment volume more efficiently using ITSM Agent Workspace.

</td><td>

Install the Service Operations Workspace for ITSM application from the ServiceNow Store.

</td></tr><tr><td>

Operator Workspace and CMDB Agent Workspace \[com.itom-noc-app, com.oi-scoped-app, com.sn-em-ai-action, com.sn-em-hidden-component com.sn-em-ai-overview, com.sn-em-metric, com.sn\_log\_viewer com.cmdb-workspace\]

</td><td>

Deprecated in Washington DC

</td><td align="center">

—

</td><td>

Install the Service Operations Workspace for ITOM application from the ServiceNow Store.

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

Release Management \[com.snc.release\_management\_v2\]

</td><td>

Planned for June 2031 or contract term end date \(whichever is earlier\)

</td><td>

Provides release tables that store information about the planned release and tasks that are required to execute the release.

</td><td>

—

</td></tr><tr><td>

Healthcare Computerized Maintenance Management System \[com.sn\_hcls\_cmms\]

</td><td>

Planned for deprecation September 2029 or contract term end date \(whichever is earlier\)

</td><td>

Manage medical device-related in-service process, alternative equipment maintenance \(AEM\) review process, medical device issues, and out-of-service process

</td><td>

Enterprise Asset Management for Healthcare requires the CDMv2 SKU. Contact your Account Executive for assistance. -   Install the Enterprise Asset Management for Healthcare application from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/application/6bd1ba63c37631106ed63d061840dd22/1.0.0?referer=%2Fstore%2Fsearch%3Flistingtype%3Dallintegrations%25253Bancillary_app%25253Bcertified_apps%25253Bcontent%25253Bindustry_solution%25253Boem%25253Butility%25253Btemplate%25253Bgenerative_ai%25253Bsnow_solution%26q%3Denterprise%2520asset%2520management%2520for%2520healthcare&sl=sh) and review the configuration guidance in the [Install Enterprise Asset Management for healthcare](https://www.servicenow.com/docs/access?context=install-eam-for-healthcare&version=xanadu&pubname=xanadu-it-asset-management&ft:locale=en-US) documentation.
-   Review the [Managing work orders for your enterprise assets](https://www.servicenow.com/docs/access?context=create-manage-wo-enterprise-assets&version=xanadu&pubname=xanadu-it-asset-management&ft:locale=en-US) documentation for creating and managing work orders for your Enterprise Assets.
-   [Field Service Management](https://www.servicenow.com/docs/access?context=fsm-application-landing-page&version=xanadu&pubname=xanadu-field-service-management&ft:locale=en-US) must be installed as a pre-requisite as it is a dependency for EAM for Healthcare.

</td></tr><tr><td>

Cloud Insights Billing \[sn\_clin\_billing\]

</td><td>

Planned for deprecation in the Z release

</td><td>

The Cloud Insights Billing application provides the tools to download the billing data for the provisioned Amazon Web Services \(AWS\), Google Cloud Platform \(GCP\) and Microsoft Azure resources and visualize the data in a dashboard.

</td><td>

—

</td></tr><tr><td>

Performance Analytics - Content Pack - GRC: Policy and Compliance Management \[app-compliance-pa\]

</td><td>

Planned for deprecation in the Z release

</td><td align="center">

—

</td><td align="center">

—

</td></tr><tr><td>

Performance Analytics - Content Pack - GRC: Risk Management \[app-risk-pa\]

</td><td>

Planned for deprecation in the Z release

</td><td align="center">

—

</td><td align="center">

—

</td></tr><tr><td>

Performance Analytics - GRC: Audit Management \[app-audit-pa\]

</td><td>

Planned for deprecation in the Z release

</td><td align="center">

—

</td><td align="center">

—

</td></tr><tr><td>

Vendor Success Indicators \[com.snc.vendor.insights\]

</td><td>

Planned for deprecation in the Z release

</td><td>

Vendor Success Indicators to utilize Odds Ratio and other ML capabilities for Vendor Manager Workspace.

</td><td>

Install the Vendor Manager Workspace from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/application/5c66d489fc528b4699eee8535382a8f5/3.3.0?referer=%2Fstore%2Fsearch%3Flistingtype%3Dallintegrations%25253Bancillary_app%25253Bcertified_apps%25253Bcontent%25253Bindustry_solution%25253Boem%25253Butility%25253Btemplate%25253Bgenerative_ai%25253Bsnow_solution%26q%3Dvendor%2520management&sl=sh) and use the KPI Groups feature. Review the [Create KPI groups to track metrics for your vendors](https://www.servicenow.com/docs/access?context=create-kpi-groups-vendors-configurable-workspace&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US) documentation.

</td></tr><tr><td>

Safe Workplace Dashboard \[sn\_imt\_dashboard\]

</td><td>

Planned for deprecation in the Z release

</td><td>

Quickly assess workplace and employee safety information.

</td><td align="center">

—

</td></tr><tr><td>

Scaled Agile Framework \[com.sn\_safe\_dashboards, com.snc.sdlc.safe.atf, com.snc.sdlc.safe.multi\_task, com.snc.sdlc.portfolio\_safe, com.snc.sdlc.safe, sn\_safe\_progress, com.snc.business\_stakeholder\]

</td><td>

Planned for deprecation September 2030 or contract term end date \(whichever is earlier\)

</td><td>

Helps you apply lean and agile principles to your large enterprise enabling you to develop and deliver software products with fewer defects in the shortest viable lead time.

</td><td>

Select and activate a replacement application. Enterprise Agile Planning requires an SPM Pro subscription. If you aren’t a Pro customer, work with your Account Executive to discuss your options. Install the Strategic Planning Workspace application from the ServiceNow Store to start using Enterprise Agile Planning.

</td></tr><tr><td>

Employee Campaigns for Workplace from Facebook\[com.snc.sn\_fb\_wp\_campaigns\]

</td><td>

Planned for deprecation September 2025

</td><td>

Enables you to package your content into a campaign and publish the content to groups on Workplace from Facebook.

</td><td>

No replacement. If you are using this application, you have the option to maintain the unsupported application as custom code.

</td></tr><tr><td>

Timeline Visualization/CIO Roadmap \[com.snc.timeline\_visualization\]

</td><td>

Planned for deprecation in the Z release

</td><td>

Enables graphical representation of activities over time to provide a high-level view of strategic and operational activities in your organization such as incidents, problems, changes, and projects.

</td><td>

Install the [Portfolio Planning](https://store.servicenow.com/sn_appstore_store.do#!/store/application/9aa0eddcc70c2010d302670f6ec260c4/8.2.0?referer=%2Fstore%2Fsearch%3Flistingtype%3Dallintegrations%25253Bancillary_app%25253Bcertified_apps%25253Bcontent%25253Bindustry_solution%25253Boem%25253Butility%25253Btemplate%25253Bgenerative_ai%25253Bsnow_solution%26q%3Dportfolio%2520planning&sl=sh) \(standard customers\) or [Strategic Planning](https://store.servicenow.com/sn_appstore_store.do#!/store/application/a38ac49ccbf511104abddcbcf7076dec/4.1.3?referer=%2Fstore%2Fsearch%3Flistingtype%3Dallintegrations%25253Bancillary_app%25253Bcertified_apps%25253Bcontent%25253Bindustry_solution%25253Boem%25253Butility%25253Btemplate%25253Bgenerative_ai%25253Bsnow_solution%26q%3Dportfolio%2520planning&sl=sh) \(Pro customers\) application from the ServiceNow Store. Review the [Planning roadmaps in Portfolio Planning](https://www.servicenow.com/docs/access?context=planning-roadmaps-in-portfolio-planning&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US) or [Roadmaps in Strategic Planning](https://www.servicenow.com/docs/access?context=roadmap-planning-overview&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US) documentation for guidance on the roadmap functionality available within these workspaces. Migrate to the Portfolio Planning Workspace \(SPM Standard\) application that provides latest experience for this functionality.

</td></tr><tr><td>

Human Resources: Lifecycle Events - Performance Analytics \[com.sn\_hr\_lifecycle\_pa\]

</td><td>

Planned for deprecation in the Z release

</td><td align="center">

—

</td><td align="center">

—

</td></tr><tr><td>

Data Certification \[com.snc.certification\_v2\]

</td><td>

Planned for deprecation in the Z release

</td><td>

Data Certification manages scheduled and on-demand validations of the configuration management database \(CMDB\) data.

</td><td>

Install the CMDB Workspace v6.0+ application \(compatible with Washington D.C. and later\) from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/application/c8ab76825371201032b7ddeeff7b1280) to use the CMDB Data Manager feature. See [Working with CMDB Data Manager](https://www.servicenow.com/docs/access?context=cmdb-data-management&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td>

Instance Troubleshooter \[com.sn\_troubleshooter\]

</td><td>

Planned for deprecation in the Y release

</td><td align="center">

—

</td><td>

Transition to one of the following alternative applications: -   Use the instance scan tool installed on your instance by default. Review the [Product Documentation](https://servicenow.com/docs/bundle/washingtondc-platform-administration/page/administer/health-scan/reference/hs-landing-page.html).
-   Evaluate the [HealthScan product](https://servicenow.com/docs/bundle/washingtondc-impact/page/product/impact/concept/healthscan.html) available with the [ServiceNow Impact packages](https://servicenow.com/docs/bundle/washingtondc-impact/page/product/impact/reference/impact-packages.html). Work with your Account Team to procure an Impact package required to use this product.

</td></tr><tr><td>

Enterprise Employee Experience Pack \[app-hr-swc-content\]

</td><td>

Planned for deprecation in the Z release

</td><td>

Delivers preconfigured process flows and sample content to help you quickly implement enterprise-wide use cases across multiple departments.

</td><td align="center">

—

</td></tr><tr><td>

Application Insights \[sn\_app\_insights\]

</td><td>

Planned for deprecation in the Z release

</td><td>

Application Insights provides a centralized location where you can visualize and monitor system health.

</td><td>

Evaluate the [Impact Instance Observer](https://www.servicenow.com/docs/access?context=io-overview&version=xanadu&pubname=xanadu-impact&ft:locale=en-US) product available with the [Impact packages](https://www.servicenow.com/docs/access?context=impact-packages&version=xanadu&pubname=xanadu-impact&ft:locale=en-US). Work with your Account Team to procure an Impact package required to use this product.

</td></tr><tr><td>

Workplace Service Delivery Integration with Mappedin \[com.sn\_wsd\_mappedin\]

</td><td>

Planned for deprecation in the Z release

</td><td>

Provides interactive digital mapping solution.

</td><td>

Install the Indoor Mapping application from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/application/fa60558563b044509d2cba84af9c019c/1.9.1?referer=%2Fstore%2Fsearch%3Flistingtype%3Dallintegrations%25253Bancillary_app%25253Bcertified_apps%25253Bcontent%25253Bindustry_solution%25253Boem%25253Butility%25253Btemplate%25253Bgenerative_ai%25253Bsnow_solution%26q%3Dindoor%2520mapping&sl=sh).

</td></tr><tr><td>

DevOps Config \[com.snc.devops\_config\]-   DevOps Config Exporter Content Pack \[com.snc.devops.config.exporter.content\]
-   DevOps Config Policy Content Pack \[com.snc.devops.config.policy.content\]
-   Configuration Data Management \[com.sn\_cdm\]
-   Context Menu Component for Configuration Data Management UI \[com.servicenow\_cdm\_context\_menu\]

</td><td>

Planned for deprecation on customer's specific contract end term for the DevOps Config application.

</td><td>

Manages and validates configuration data in your DevOps environment using a single system.

</td><td align="center">

—

</td></tr><tr><td>

GRC: DevOps Accelerator \[com.sn\_grc\_devops\]

</td><td>

Planned for deprecation in the Y release

</td><td>

Enables your customers to evaluate the compliance for DevOps policies and GRC control objectives integrating with Policy as a Code Engine \(PaCE\).

</td><td align="center">

—

</td></tr><tr><td>

Predictive Intelligence Workbench for ITSM \[com.sn\_piwb\_itsm\_content\]

</td><td>

Planned for deprecation in the Y release

</td><td>

Enables a customer to seed domain-specific content to provide implementation guidance for use cases created through Predictive Intelligence Workbench

</td><td>

Install the Task Intelligence for ITSM application from the ServiceNow Store and use the Task Intelligence Admin Console. For more information, see the [Task Intelligence for ITSM](https://www.servicenow.com/docs/access?context=c-itsm-task-intelligence&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US) documentation.

</td></tr><tr><td>

Legal Counsel Center Classic \[com.sn\_lg\_workspace\] and Legal Counsel Center Components \[com.sn\_lg\_ws\_comps\]

</td><td>

Planned for deprecation in the Y release

</td><td>

Legal Counsel Center Classic enables legal department members to categorize, prioritize, and efficiently address legal issues.

</td><td>

Install the Legal Counsel Center application from the ServiceNow Store and review the [Legal Counsel Center](https://www.servicenow.com/docs/access?context=legal-counsel-center-landing&version=xanadu&pubname=xanadu-employee-service-management&ft:locale=en-US) documentation.

</td></tr><tr><td>

Order Management for Customer Service Management \[com.sn\_csm\_order\_mgmt\]

</td><td>

Planned for deprecation in September 2028 or Order Management subscription term end date \(whichever is earlier\)

</td><td>

Order Management provides the ability to create, manage, and track orders.

</td><td>

Install the new Order Management application from the ServiceNow Store.

</td></tr><tr><td>

IBM Dynamic Translation \[com.glide.ibm\_translation\_spoke\)\]

</td><td>

Planned for deprecation in December 2024

</td><td>

This spoke is available in the Store, and it works with ServiceNow's Dynamic Translation plugin. There are alternative translation services \(Google, Microsoft\) available.

</td><td>

[IBM announced](https://cloud.ibm.com/docs/language-translator?topic=language-translator-about) end of life of the Watson Language Translator with end of support on June 10, 2024 and permanent removal on December 10, 2024. Review the [Dynamic Translation](https://www.servicenow.com/docs/access?context=dynamic-translation-overview&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US) documentation to explore the available Dynamic Translation services with Google and Microsoft.

</td></tr><tr><td>

Site Reliability Metrics and \[com.sn\_srm\]

</td><td>

Planned for deprecation in the Y release

</td><td>

Captures application performance signals from the Application Performance Management \(APM\) tool, typically referred to as Service Level Indicators \(SLIs\). The SRM application then allows for the creation of Service Level Objectives \(SLOs\), Error Budgets \(EB\), and policy-based actions.

</td><td>

Install the Service Reliability Management application from the ServiceNow Store and review the [launch blog](https://www.servicenow.com/community/service-operations-workspace/introducing-service-reliability-management-for-service/ta-p/2677832) to learn more about the application and features.

</td></tr><tr><td>

Site Reliability Operations \[com.sn\_srops\]

</td><td>

Planned for deprecation in the Y release

</td><td>

Increases the visibility of microservices in a single workspace by onboarding teams and registering services in minutes. ​It improves observability by quickly connecting to telemetry via Webhook integrations and resolves incidents faster with alert automation.

</td><td>

Install the Service Reliability Management application from the ServiceNow Store and review the [launch blog](https://www.servicenow.com/community/service-operations-workspace/introducing-service-reliability-management-for-service/ta-p/2677832) to learn more about the application and features.

</td></tr><tr><td>

Knowledge Management v3 \[com.snc.knowledge3\]

</td><td>

Planned for deprecation in the Y release

</td><td>

The Knowledge Management v3 homepage will no longer be deployed or activated beginning in the Washington DC release.

</td><td>

Install and configure the Knowledge Management Service Portal plugin \(com.snc.knowledge\_serviceportal\) using the guidance in [Configuring Knowledge Management](https://www.servicenow.com/docs/access?context=configuring-knowledge-management&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US), and set the **sn\_km\_portal.glide.knowman.serviceportal.enable\_redirect** system property to true to activate redirection from the v3 homepage to the Portal.

</td></tr><tr><td>

Facilities Service Management\[com.snc.facilities\_service\_automation\]

</td><td>

Planned for deprecation in March 2025 or last subscription term end.

</td><td>

Manages facilities requests and enables users to report and track requests by their location. To view requests on a floor plan, the Facilities Visualization Workbench \(com.snc.facilities\_service\_automation.fvw\) plugin is required.

</td><td>

Transition to Workplace Service Delivery.

</td></tr><tr><td>

Facilities Visualization Workbench\[com.snc.facilities\_service\_automation.fvw\]

</td><td>

Planned for deprecation in March 2025 or subscription term end.

</td><td>

Enables the interactive floor plan functionality.

</td><td>

Transition to Workplace Service Delivery.

</td></tr><tr><td>

Finance Service Management\[com.snc.finance\_service\_automation\]

</td><td>

Planned for deprecation in February 2023 or last subscription term end.

</td><td>

Lets you launch Finance Service Automation and other service management applications. Activation of this plugin on production instances may require a separate license. Contact ServiceNow for details.

</td><td align="center">

—

</td></tr><tr><td>

ITSM Pro - Service Owner Workspace\[com.spm\_owner\_workspace\]

</td><td>

Planned for deprecation on subscription term end or on migration to Digital Portfolio Management.

</td><td>

Provides a premium Service Portfolio Management experience. Portfolio managers and service owners access an integrated and graphically intuitive user interface to manage and monitor portfolios and services.

</td><td>

Migrate to Digital Portfolio Management on the ServiceNow Store.

</td></tr><tr><td>

MaestroRS\[app-irm-bcm\]

</td><td>

Planned for deprecation on customer's specific contract end term for MaestroRS application.

</td><td>

—

</td><td>

Activate the four Business Continuity Management replacement applications on the ServiceNow Store;-   GRC: Business Continuity Management – Core
-   GRC: Business Continuity Planning
-   GRC: Business Impact Analysis
-   GRC: Business Continuity Management – Components

</td></tr><tr><td>

Marketing Service Management\[com.snc.marketing\_service\_automation\]

</td><td>

Planned for deprecation in February 2023 or last subscription term end.

</td><td>

Lets you launch Marketing Service Automation and other service management applications. Activation of this plugin on production instances may require a separate license. Contact ServiceNow for details.

</td><td align="center">

—

</td></tr><tr><td>

Microsoft AD Spoke for IntegrationHub\[com.sn.ad.spoke\]

</td><td>

Planned for deprecation on contract end date or March 2028 \(whichever is earlier\).

</td><td>

Provides actions that a Process Analyst can use when designing flows. The actions allow them to automate the management of users, groups, computers, and objects in AD.

</td><td>

Install the Microsoft Active Directory v2 Spoke application on the ServiceNow Store For guidance, see [Migration Guide \[KB1284583\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1284583).

</td></tr><tr><td>

Social Q&amp;A\[com.sn\_kb\_social\_qa\]

</td><td>

Planned for deprecation in a future release.

</td><td>

Allows users to ask and respond to questions and vote on questions and answers. Social Q&amp;A extends the Knowledge application and uses existing Knowledge functionality such as user criteria and multiple knowledge bases.

</td><td align="center">

—

</td></tr><tr><td>

Trusted Security Circles\[sn\_ti\], \[sn\_tis\_a\]

</td><td>

Planned for deprecation in September 2023 or last subscription term end.

</td><td>

—

</td><td align="center">

—

</td></tr><tr><td>

Vendor Performance Management\[com.snc.vendor\_performance\], \[com.snc.vendor\_ticket\]

</td><td>

Planned for deprecation in March 2024 or subscription term end.

</td><td>

Provides capabilities to measure, manage, and track vendor data and compare performance characteristics in unique graphical views.

</td><td>

Transition to Vendor Manager Workspace, included in ITSM Pro v2 subscription package.

</td></tr></tbody>
</table>## Renamed and changed plugins

This table lists the existing plugins that were renamed or changed in Xanadu or Washington DC.

|Plugin|Status|Description|Details|
|------|------|-----------|-------|
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
|Virtual Agent API \(sn\_va\_as\_service\)|Changed in Washington DC|Integrates any chat interface or a bot with Virtual Agent or Agent Chat.|The com.sn.omnichannel.callback plugin has been removed and the com.sn\_ext\_agent\_management\_util plugin is now a dependency.|

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

An extension to Content Management that adds iFrames and Flash frames.Use Service Portal for new development instead of CMS. Service Portal is an alternative to CMS with a refined user experience, and is active by default in the base system. For more information, see [Service Portal](https://www.servicenow.com/docs/access?context=c_ServicePortal&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US) and [Content Management and Service Portal](https://www.servicenow.com/docs/access?context=c_CMSAndSP&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US).

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
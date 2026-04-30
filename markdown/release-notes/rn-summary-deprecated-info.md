---
title: Deprecation information for all Xanadu features and products
description: Cumulative release notes summary on deprecation information for Xanadu features and products.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2026-04-08"
reading_time_minutes: 14
breadcrumb: [Release notes summaries for Xanadu features, Release notes for upgrading from Washington DC, Learn about the Xanadu release, Xanadu release notes]
---

# Deprecation information for all Xanadu features and products

Cumulative release notes summary on deprecation information for Xanadu features and products.

For information about deprecated plugins in Xanadu, refer to Plugin information[Plugin information for all features and productsPlugin information](https://www.servicenow.com/docs/r/release-notes/rn-summary-plugin-info.html)

<table id="rn-summary-accessibility-table" class="custom-rows"><thead><tr><th class="filter">

Application or feature

</th><th>

Details

</th></tr></thead><tbody><tr><td>

AI Search

</td><td>

Starting with the Now Assist in AI Search 8.0 release, the External Content Q&amp;A Genius Results feature is being prepared for future deprecation. It will continue to be supported until it is deprecated. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

</td></tr><tr><td>

Advanced Risk

</td><td>

-   The Risk portal has been deprecated, and a navigation link has been added to access the new Risk portal.

</td></tr><tr><td>

Agent experience for CSM

</td><td>

Starting with the Xanadu release, CSM Agent Workspace is no longer deployed, enhanced, or supported. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support knowledge base. [CSM Configurable Workspace](https://www.servicenow.com/docs/access?context=csm-workspaces-configure&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US) provides the latest experience for this functionality.

</td></tr><tr><td>

Analytics, Intelligence, and Reporting

</td><td>

-   Core UI Reporting functionality is deprecated in favor of [Data visualizations in Platform Analytics](https://www.servicenow.com/docs/access?context=analytics-center-data-visualizations&version=xanadu&pubname=xanadu-now-intelligence&ft:locale=en-US) for new instances and instances that have migrated to the Platform Analytics experience.
-   Core UI Dashboards functionality is deprecated in favor of [Dashboards in Platform Analytics](https://www.servicenow.com/docs/access?context=analytics-center-dashboards&version=xanadu&pubname=xanadu-now-intelligence&ft:locale=en-US) for new instances and instances that have migrated to the Platform Analytics experience.

</td></tr><tr><td>

Authentication

</td><td>

-   The MultiSSO v1 plugin is deprecated. Upgrade to MutliSSO v2 from MultiSSO v1. For more information on how to upgrade to MultiSSO v2, refer to the knowledge article [MultiSSO v2 upgrade instructions \[KB9756504\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0756504) in the Now Support Knowledge Base.
-   The SAML 1.1 and SAML 1.1 Single Sign-On - Update 1 plugin is deprecated. The SAML-based identity providers \(IdP\) have already migrated to SAML 2.0. To use SAML 2.0, you must activate the MultiSSO v2 plugin and configure your identity provider.
-   The OpenID SSO plugin is deprecated. To use OpenID Connect \(OIDC\), you must activate the MultiSSO v2 and configure your OIDC-based identity provider.

</td></tr><tr><td>

Business Continuity Management

</td><td>

-   The BCM Classic Workspace isn’t compatible with the new features and enhancements that were introduced with the Xanadu release. Any issues and errors encountered with its continued use aren't supported. To avoid any disruptions, transition to the BCM Configurable Workspace.

**Note:** Although the BCM Classic Workspace is still available through the URLs after its deprecation, it doesn't appear in the navigation menu.


</td></tr><tr><td>

Case and Knowledge Management

</td><td>

Starting with the Xanadu release, HR Document Templates is being prepared for deprecation. HR Document Templates is hidden and is no longer installed on new instances but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base. You can use the ServiceNow Document Templates application instead of HR Document templates.

</td></tr><tr><td>

Case management for CSM

</td><td>

Starting with the Xanadu release, CSM Agent Workspace is no longer deployed, enhanced, or supported. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support knowledge base. [CSM Configurable Workspace](https://www.servicenow.com/docs/access?context=csm-workspaces-configure&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US) provides the latest experience for this functionality.

</td></tr><tr><td>

Cloud Cost Management 8.0.0

</td><td>

Starting with the Xanadu release, note the following deprecations:

-   The Core UI interface for the Cloud Cost Management application is no longer deployed, enhanced, or supported. For continued access and functionality, transition to the Cloud Cost Management Workspace. For more information, see [Cloud Cost Management Workspace](https://www.servicenow.com/docs/access?context=ci-workspace&version=xanadu&pubname=xanadu-it-asset-management&ft:locale=en-US).
-   The Cloud Spend Dashboard is no longer deployed, enhanced, or supported. The Asset Executive Workspace provides this functionality. For more information, see [Visibility into Cloud Cost Management KPIs using the Asset Management Executive Dashboard](https://www.servicenow.com/docs/access?context=itam-exec-dashboard-cloudinsights&version=xanadu&pubname=xanadu-it-asset-management&ft:locale=en-US).
-   The Cloud Insights Billing application, which supports the Cloud Provisioning and Governance product with limited functionality, is being prepared for future deprecation. It will not be available on ServiceNow Store for download and installation but will continue to be supported.

For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

-   Starting with the Xanadu release, the Data Certification plugin \(com.snc.certification\_v2\) is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. The [CMDB Workspace store app](https://www.servicenow.com/docs/access?context=cmdb-workspace&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US) provides the latest experience for this functionality. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view_customer.do?sysparm_article=KB0867184]) article in the Now Support knowledge base.
-   ServiceNow hosted Service Graph Connector for ExtraHop is now deprecated and no longer supported or available for new activation. Service Graph Connector for ExtraHop provides the latest experience for this functionality. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

</td></tr><tr><td>

Core ServiceNow AI Platform

</td><td>

-   The System Performance Dashboard is deprecated as of the Xanadu release. [Impact Instance Observer](https://www.servicenow.com/docs/access?context=io-overview&version=xanadu&pubname=xanadu-impact&ft:locale=en-US) offers a powerful solution for enhancing system performance. Contact your account manager to discover more.
-   Starting with the Xanadu release, Application Insights is being prepared for future deprecation. It will be hidden and no longer available in the ServiceNow Store but will continue to be supported. Instead, [Impact Instance Observer](https://www.servicenow.com/docs/access?context=io-overview&version=xanadu&pubname=xanadu-impact&ft:locale=en-US) offers a powerful solution for enhancing system performance. Contact your account manager to discover more. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

</td></tr><tr><td>

Dynamic Translation

</td><td>

With the Xanadu release, the IBM Watson Translator Service integration is no longer available in the ServiceNow® Store. For more information, see [https://cloud.ibm.com/docs/language-translator?topic=language-translator-release-notes](https://cloud.ibm.com/docs/language-translator?topic=language-translator-release-notes).

</td></tr><tr><td>

Enterprise Architecture \(formerly Application Portfolio Management\)

</td><td>

Starting with the Xanadu release, some modules are deprecated from Enterprise Architecture \(formerly known as Application Portfolio Management\). The navigation links to the deprecated modules are removed from the **All** menu. If you’re an existing customer, you can continue to use these navigation links. However, if you’re a new activation customer, navigation to these modules using the navigation links from the **All** menu won’t be available. All the deprecated modules are available within the Enterprise Architecture Workspace. You’re encouraged to use the Enterprise Architecture Workspace to leverage those features and functionalities. The deprecated modules are:

-   Application Portfolio Management Home
-   Application Portfolio
-   Application Portfolio Analysis
-   Architectural Artifacts
-   Business Application Lifecycles - Service Requests
-   Application Ratings
-   Capability Ratings
-   Information Portfolio
-   Technology Portfolio Management
-   Technology Reference Model
-   Administration
    -   Business Processes
    -   Business Capabilities
    -   Application Families
    -   Application Category Groups
    -   Application Categories
    -   Application Indicators
    -   Scoring Profiles
    -   Bubble Chart
    -   Demand Actions
    -   Portfolio

</td></tr><tr><td>

Event Management

</td><td>

The following dashboards have been deprecated:

-   Event Management scorecards
-   Event Management insights
-   Event Management overview
-   Health Log Analytics Overview

The Service Management dashboard is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. For details, see the Deprecation Process article [\(KB0867184\)](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184) in the Now Support knowledge base.

</td></tr><tr><td>

Field Service Management

</td><td>

-   Starting with the Xanadu release, FSM Agent Classic Workspace plugin \(com.snc.agent\_workspace.fsm\) is no longer deployed, enhanced, or supported. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.
-   Starting with the Zurich release, the **Enable capacity** constraint for Schedule Optimization is being prepared for future deprecation. It will be no longer be applied for Schedule Optimization. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

</td></tr><tr><td>

Hardware Asset Management 11.0.0

</td><td>

Beginning with the Xanadu release, the following Core UI Performance Analytics dashboards aren't available to new users of Hardware Asset Management:

-   Hardware Asset Dashboard
-   Hardware Normalization Dashboard
-   My Assets
-   Procurement Overview
-   Asset Contract Overview
-   Asset Overview

**Note:** The Core UI Performance Analytics dashboards are available to the existing users of Hardware Asset Management.

</td></tr><tr><td>

Healthcare Computerized Maintenance Management System

</td><td>

Starting with the Xanadu release, Healthcare Computerized Maintenance Management System is being prepared for future deprecation. It will be hidden and no longer installed on new instances but will continue to be supported. For details on this process, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base. For information on maintenance and servicing, please see [Field Service Management.](https://www.servicenow.com/docs/access?context=fsm-application-landing-page&version=xanadu&pubname=xanadu-field-service-management&ft:locale=en-US) For information on inventory and management, please see [Enterprise Asset Management for Healthcare](https://www.servicenow.com/docs/access?context=eam-for-healthcare&version=xanadu&pubname=xanadu-it-asset-management&ft:locale=en-US).

</td></tr><tr><td>

ITOM AIOps

</td><td>

The following dashboards have been deprecated:

-   Event Management scorecards
-   Event Management insights
-   Event Management overview
-   Health Log Analytics Overview

Service Management Dashboard is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. For details, see the Deprecation Process \[KB0867184\] article in the Now Support knowledge base.

</td></tr><tr><td>

ITOM Optimization

</td><td>

Deprecation of Cloud API \(CAPI\)- based Cloud Discovery on new instances:

-   CAPI-based Discovery is deprecated for new instances with Xanadu.
-   Contact your administrator to install the latest version of the Discovery and Service Mapping Patterns ServiceNow® Store application to use the Discovery feature.
-   For an existing instance, manually migrate to Patterns-based Discovery.
-   The **Discover Schedules** tab in the Cloud Admin Portal is going to redirect to Cloud Discovery Workspace.

**Note:** See [Migrate from CAPI to Patterns](https://www.servicenow.com/docs/access?context=migrate-from-capi-to-pattern&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US) to learn more about the migration from CAPI to Patterns-based Discovery.

For details, see the [Application/Plugin Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184) article in the Now Support Knowledge Base.

</td></tr><tr><td>

ITOM Visibility

</td><td>

Starting with the Xanadu release, the Discovery Dashboard is no longer part of the Discovery plugin. Use [Discovery Admin Workspace](https://www.servicenow.com/docs/access?context=discovery-admin-workspace&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US) instead.

</td></tr><tr><td>

Operational Sustainability Management

</td><td>

-   Starting with the Xanadu release, the Global Reporting Initiative \(GRI\) content accelerator is deprecated. It will be hidden and no longer activated on new instances but will continue to be supported. The ESG content accelerator application provides the latest experience for this functionality.
-   Starting with the Xanadu release, the Sustainability Accounting Standards Board \(SASB\) content accelerator is deprecated. It will be hidden and no longer activated on new instances but will continue to be supported. The ESG content accelerator application provides the latest experience for this functionality.

</td></tr><tr><td>

Operational Technology Manager

</td><td>

-   The OT Manager dashboard is no longer available in the Industrial Workspace.
-   Starting with the Yokohama release, Service Graph Connector for Microsoft Defender for IoT \(On-premises Management Console\) is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported.

</td></tr><tr><td>

Operational Technology Vulnerability Response

</td><td>

-   The **OT Vulnerabilities** tab is no longer available on the OT Manager dashboard in the Industrial Workspace.
-   Starting with the Xanadu release, **Vulnerability Response Integration with Microsoft Defender for IoT \(On-premises Management Console\)** integration is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported.

</td></tr><tr><td>

Opportunity Management

</td><td>

The following fields are deprecated in the **Details** tab on Opportunity record.

-   Total Monthly Recurring Price
-   Total Annual Recurring Price
-   ARR
-   Budget Type

The following fields are depracated in the **Details** tab on Opportunity Line Items record.

    -   Estimated Unit Price
    -   Estimated Total Price
    -   Total Recurring Price

</td></tr><tr><td>

Performance Analytics

</td><td>

-   Performance Analytics widgets are not available on new instances. Use Platform Analytics data visualizations with indicator data sources instead. Users with the admin and pa\_admin roles will still be able to use Performance Analytics widgets for Service Portal.
-   The Analytics Hub is not available on new instances or instances that have fully migrated to Platform Analytics. Use KPI Details instead.
-   The Performance Analytics admin console is deprecated on new instances. For upgrading customers, the console is available but does not show data from the new Platform Analytics artifacts.

</td></tr><tr><td>

Platform Analytics experience

</td><td>

-   Reporting is not available on new instances. Use Platform Analytics data visualizations with table data sources instead. Users with admin and report\_admin roles will still be able to use Reporting for Service Portal.
-   Performance Analytics widgets are not available for new customers. Use Platform Analytics data visualizations with indicator data sources instead. Users with the admin and pa\_admin roles will still be able to use Performance Analytics widgets for Service Portal.
-   Responsive dashboards are not available for new customers. Create dashboards in Platform Analytics instead.
-   Interactive filters are not available for new customers. Create filters in Platform Analytics instead.
-   The Analytics Hub is not available for new customers. Use KPI Details instead.
-   For new customers, interactive analysis is available only for Core UI lists.
-   In-form analytics are deprecated on new instances and after migrating to Platform Analytics. The feature does not apply to Platform Analytics artifacts.
-   The Performance Analytics admin console is deprecated on new instances and after migrating to Platform Analytics. The feature does not apply to Platform Analytics artifacts.
-   Dependency assessment is deprecated on new instances and after migrating to Platform Analytics. The feature does not apply to Platform Analytics artifacts.

</td></tr><tr><td>

Predictive Intelligence

</td><td>

The dashboard for Solution Statistics has been deprecated. Upgrading customers can continue to use their existing Solutions Statistics dashboards from the application menu. For new customers onboarding with the Xanadu release, the Solutions Statistics dashboard is not available. For more information, see [Review classification solution statistics](https://www.servicenow.com/docs/access?context=review-solution-statistics&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US).

</td></tr><tr><td>

Project Workspace

</td><td>

Starting with Xanadu release, Classic Project Workspace is being prepared for future deprecation. It will be hidden and no longer available for installation but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

</td></tr><tr><td>

Quote Management

</td><td>

The following table columns are deprecated from Quote Management.

|Table name|Column name|
|----------|-----------|
|sn\_quote\_mgmt\_core\_quote\_line\_item|cumulative\_monthly\_recurring\_price, cumulative\_annual\_recurring\_price|
|sn\_quote\_mgmt\_core\_quote|total\_monthly\_recurring\_price, total\_annual\_recurring\_price, total\_recurring\_price|

</td></tr><tr><td>

RPA Hub

</td><td>

-   The RPA Sample templates store application is deprecated and is no longer supported or available for new activation. RPA Desktop Design Studio provides the latest experience for this functionality. For more information, see [RPA Desktop Design Studio user interface](https://www.servicenow.com/docs/access?context=rpa-studio-ui&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US).
-   In RPA Hub, the **Is Request Content Sensitive** field in the Queues form was deprecated.
-   In RPA Hub the **Credential Set** field in the Process Robot Credentials form was deprecated.

</td></tr><tr><td>

Regulatory Change Management

</td><td>

-   No plans to enhance the Calendar reporting view in the Classic UI that is shipped with the application.
-   No plans to enhance the Overview dashboard in the Classic UI that is shipped with the application.

</td></tr><tr><td>

Release Management

</td><td>

Starting with the Xanadu release, Release Management v2 is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. Digital Product Release provides the latest experience for this functionality. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184) article in the Now Support Knowledge Base.

</td></tr><tr><td>

Scaled Agile Framework \(SAFe\)

</td><td>

The following SAFe-related plugins are planned for deprecation and can no longer be deployed for new activation. However, existing users can continue to use them.

-   Essential SAFe \(com.snc.sdlc.safe\)
-   Portfolio SAFe \(com.snc.sdlc.portfolio\_safe\)
-   Performance Analytics Content Pack for Essential SAFe \(com.sn\_safe\_dashboards\)
-   Work Progress Status for SAFe \(com.sn\_safe\_progress\)
-   Agile - Scaled Agile Framework - Unified Backlog \(com.snc.sdlc.safe.multi\_task\)
-   Read-only roles for SAFe

For more information on the deprecation process and its impact, see the [Application/Plugin Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.


As an alternative, you can use the Enterprise Agile Planning \(EAP\) capability within the Strategic Planning application, which provides SAFe features with flexible team and work hierarchy configurations. With an interactive workspace experience, EAP helps you to streamline communication and collaboration between your teams. For more information, see [Enterprise Agile Planning](https://www.servicenow.com/docs/access?context=eap-landing&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US).

</td></tr><tr><td>

Security Center

</td><td>

Beginning with the ServiceNow AI Platform Xanadu release, ServiceNow will end support for Instance Security Center.

For details, see the [Deprecation Process](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184) article \(KB 0867184\) in the Now Support Knowledge Base.

</td></tr><tr><td>

Service Exchange

</td><td>

-   Service Exchange \(legacy\) application is now deprecated and no longer supported or available for new activation. The Service Exchange for Consumers application provides the latest experience for this functionality.
-   Service Exchange for Providers \(legacy\) application is now deprecated and no longer supported or available for new activation. The Service Exchange for Providers application provides the latest experience for this functionality.

See [KB1499823](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1499823) for details on migrating from the legacy version.

</td></tr><tr><td>

Software Asset Management

</td><td>

-   In the Software installation \[cmdb\_sam\_sw\_install\] table, the Installs associated to lifecycle column is deprecated.
-   In the Software lifecycle Reports \[sam\_sw\_product\_lifecycle\_report\] table, the Installs column is deprecated. You can view the Software installation related list by selecting the Name column.

</td></tr><tr><td>

Sourcing and Procurement Operations

</td><td>

-   SAP ECC and SAP4HANA are deprecated and no longer supported or available for new activation. Source-to-Pay Integration with SAP ECC and SAP S4 HANA provides the latest experience for this functionality.
-   The SPO classic dashboards are now deprecated and no longer supported or available for new activation. The following Next Experience dashboards provide the latest experience for this functionality:
    -   Procurement Buyer Dashboard
    -   Procurement Strategy &amp; Ops Dashboard
    -   Procurement Team Performance Dashboard
    -   Procurement Case Management Dashboard
-   The classic ShoppingHub \[com.snc.sn\_shop\] portal is now deprecated and no longer supported or available for new activation. The new Shopping Hub \[com.snc.sn\_spend\_uib\] portal provides the latest UIB-enabled experience for this functionality.

</td></tr><tr><td>

Supplier Lifecycle Operations

</td><td>

-   **[Source-to-Pay Workspace](https://www.servicenow.com/docs/access?context=supplier-manager-workspace&version=xanadu&pubname=xanadu-source-to-pay-operations&ft:locale=en-US)**

Starting with the Washington DC release, Supplier Manager Workspace is being prepared for future deprecation. It will be hidden and no longer be activated on new instances but will continue to be supported. Source-to-Pay Workspace provides the latest experience for this functionality.


</td></tr><tr><td>

Third-party Risk Management

</td><td>

-   **[Reminder workflows](https://www.servicenow.com/docs/access?context=tprm-workflow-in-workspace&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

Starting with version 19.1.x of the Third-party Risk Management application, the tiering questionnaire and external assessment reminders workflows are deprecated and migrated to Workflow Studio. If you have customized these workflows, they won’t be deprecated or migrated as part of this change.


</td></tr><tr><td>

Vendor Management Workspace

</td><td>

Starting with the Xanadu release, the Vendor Success Indicators plugin \(com.snc.vendor.insights\) is being prepared for future deprecation. It will be hidden and no longer installed on new instances but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

</td></tr><tr><td>

Virtual Agent

</td><td>

-   Starting with the Xanadu release, the Conversational Analytics dashboard is being prepared for future deprecation. It will be hidden and no longer available for installation but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

</td></tr></tbody>
</table>**Parent Topic:**[Release notes summaries for Xanadu features](../release-notes-summaries.md)


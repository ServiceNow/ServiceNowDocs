---
title: Deprecation information for all Yokohama features and products
description: Cumulative release notes summary on deprecation information for Yokohama features and products.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/release-notes/rn-summary-deprecated-info.html
release: yokohama
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 7
breadcrumb: [Release notes summaries for Yokohama features, Release notes for upgrading from Xanadu, Learn about the Yokohama release, Yokohama release notes]
---

# Deprecation information for all Yokohama features and products

Cumulative release notes summary on deprecation information for Yokohama features and products.

For information about deprecated plugins in Yokohama, refer to

<table id="rn-summary-accessibility-table" class="custom-rows"><thead><tr><th class="filter">

Application or feature

</th><th>

Details

</th></tr></thead><tbody><tr><td>

AI Control Tower

</td><td>

AI Gateway application is deprecated from the Yokohama release and are no longer supported.

</td></tr><tr><td>

AI Search

</td><td>

Starting with the Now Assist in AI Search 8.0 release, the External Content Q&amp;A Genius Results feature is being prepared for future deprecation. It will continue to be supported until it is deprecated. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

</td></tr><tr><td>

Advanced AI Search Management Tools

</td><td>

-   **AI Search Profile dashboard**

The **Searchable Documents** and **Documents by Search Source** visualizations have been removed. These visualizations depended on scheduled jobs and legacy dashboard tables which are no longer available.


</td></tr><tr><td>

Agent experience for CSM

</td><td>

Starting with the Yokohama release, Customer Service CTI Demo Data is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. ServiceNow Voice with Amazon Connect provide the latest experience for this functionality. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184) article in the Now Support Knowledge Base.

</td></tr><tr><td>

Case and Knowledge Management

</td><td>

The CTI Demo Data for HRSD \(com.sn\_hr\_cti\_demo\) plugin is being deprecated. Use Workflow Studio instead.

</td></tr><tr><td>

Case management for CSM

</td><td>

Starting with the Yokohama release, Customer Service CTI Demo Data is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. ServiceNow Voice with Amazon Connect provides the latest experience for this functionality. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184) article in the Now Support Knowledge Base.

</td></tr><tr><td>

Change Management

</td><td>

Change Management workflows have been removed and replaced by flows for new customers. Existing customers that use these workflows are unaffected. The flows are available to both new and existing customers. You can use ServiceNow® Workflow Studio to customize or extend these flows. For more information, see [Flow Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/application-development/flow-designer.md).

</td></tr><tr><td>

Common Core

</td><td>

The template data relationship table has been removed and deprecated for the Document designer application.

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

CMDB Data manager on Core UI is now deprecated and no longer supported or available for new activation. CMDB Workspace provides the latest experience for this functionality. For more information, see [CMDB Data Manager experience in CMDB Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/servicenow-platform/data-mgr-exp-cmdb-workspace.md).

</td></tr><tr><td>

Data Separation

</td><td>

Starting with the Yokohama release, Data Separation is being prepared for future deprecation and it will be hidden. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base. Alternatively, you can define data filters along with other configurations to restrict access to sensitive data \(enable data separation\). For details on how to enable data separation for different use cases using data filters and ACLs, see the [Managing data separation using data filters and ACLs \[KB1772519\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB1772519) article in the Now SupportKnowledge Base.

</td></tr><tr><td>

Dynamic Translation

</td><td>

The spoke for IBM Watson Translator Service for IBM Cloud \(com.glide.ibm\_translation\_spoke\) is no longer available because IBM has withdrawn this translation service. For more information, see [IBM Watson Language Translator Service spoke](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/ibm-translation-spoke.md).

</td></tr><tr><td>

Generative AI Controller

</td><td>

The dependency on Sensitive Data Handler has been removed. Regular expressions that are configured with Sensitive Data Handler are applied to the Data Privacy application with a fix script when you upgrade to Yokohama.

</td></tr><tr><td>

Hardware Asset Management

</td><td>

The MAC address \[mac\_address\] field in the Hardware \[alm\_hardware\] table is deprecated. The data in this field is available in the new MAC address \(mac\_addr\) field in the Asset \[alm\_asset\] table.

</td></tr><tr><td>

ITOM Visibility

</td><td>

-   **[Application/Plugin Deprecation Process \[KB0867184\]Discovery CLI](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184)**

Starting with version 3.5.0, Discovery CLI is no longer available in the Pattern Designer Enhancements Store App.


</td></tr><tr><td>

ITSM Predictive Intelligence Workbench

</td><td>

Starting with the Yokohama release, ITSM Predictive Intelligence Workbench is deprecated and is no longer deployed, enhanced, or supported. To get the latest experience for this functionality, you must install the Task Intelligence for ITSM application plugin \(com.snc.itsm\_ml\_task\). For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184) article in the Now Support Knowledge Base.

</td></tr><tr><td>

Impact

</td><td>

The Expert Connect Accelerator is no longer supported as of Yokohama.

</td></tr><tr><td>

Instance Data Replication

</td><td>

Legacy replication sets are planned for deprecation by the Zurich release. To continue replicating data in Zurich, you must upgrade all legacy replication sets to V2. For details on upgrading legacy replication sets to V2 before the upgrade, see [Upgrading legacy replication sets to V2 in Instance Data Replication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/servicenow-platform/upgrading-legacy-replication-sets-v2.md).

</td></tr><tr><td>

Legacy Application Manager

</td><td>

Starting with Yokohama patch 11, Legacy Application Manager is being prepared for future deprecation. It will be hidden but will continue to be supported. For details, see the [Application/Plugin Deprecation Process \[KB0867184\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

</td></tr><tr><td>

Operational Sustainability Management

</td><td>

Business rules were deactivated and moved to common script include methods as part of GRC Metrics. For more information, see the KB article: [KB1734660](https://support.servicenow.com/nav_to.do?uri=%2Fkb%3Fid%3Dkb_article_view%26sys_kb_id%3De92f82dd476a9610b8a4aa25126d4356).

</td></tr><tr><td>

Password Reset

</td><td>

Password Reset workflows are deprecated and have been replaced by flows in the base system for most users. zBoot users must still use the Password Reset flows.

</td></tr><tr><td>

Patient Support Services

</td><td>

Starting with the Yokohama release, Patient Support Services is being prepared for future deprecation. It will be hidden and no longer installed on new instances but will continue to be supported. For details on this process, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

</td></tr><tr><td>

Policy and Compliance Management

</td><td>

GRC DevOps Accelerator is now deprecated and no longer supported or available for new activation. For details, see the [Deprecation process \[KB0867184\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

</td></tr><tr><td>

Pre-Visit Management

</td><td>

Starting with the Yokohama release, Pre-Visit Management is being prepared for future deprecation. It will be hidden and no longer installed on new instances but will continue to be supported. For details on this process, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

</td></tr><tr><td>

Predictive Intelligence

</td><td>

With the Yokohama release, ITSM Predictive Intelligence Workbench is deprecated and no longer supported. To obtain the latest experience for this functionality, install the Task Intelligence for ITSM application \(com.snc.itsm\_ml\_task\). For more information, see [ITSM Predictive Intelligence Workbench release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/itsm-predictive-intelligence-workbench-rn.md).

</td></tr><tr><td>

Quote Management

</td><td>

The Subscription start date and Subscription end date have been deprecated starting with the Q2 2024 release. Use the Contract start date and Contract end date to calculate Terms for setting subscriptions for recurring products.

</td></tr><tr><td>

Redox Inbound Integration

</td><td>

Starting with the Yokohama release, Redox Inbound Integration is being prepared for future deprecation. It will be hidden and no longer installed on new instances but will continue to be supported. For details on this process, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

</td></tr><tr><td>

Service Level Management

</td><td>

Service Level Management workflows have been removed and replaced by flows for new customers. Existing customers that use these workflows are unaffected. The flows are available to both new and existing customers. You can use ServiceNow® Workflow Studio to customize or extend these flows. For more information, see [Flow Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/application-development/flow-designer.md).

</td></tr><tr><td>

Service Reliability Management

</td><td>

The **Alerts** tab has been removed from the Reliability tasks page.

</td></tr><tr><td>

ServiceNow Otto for IT Service Management \(ITSM\)

</td><td>

The Escalate IT Ticket core ITSM Virtual Agent topic is being deprecated in this release. The topic is renamed to **\(Deprecated\) Escalate IT Ticket**. This capability will be available in the Platform Request Status AI agent in a future release.

</td></tr><tr><td>

Site Reliability Operations

</td><td>

Starting with the Yokohama release, Release Management v2 is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. Digital Product Release provides the latest experience for this functionality. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184) article in the Now Support Knowledge Base.

</td></tr><tr><td>

Sourcing and Procurement Operations

</td><td>

The **All categories** option has been removed from the **Categories** tab in Shopping Hub due to low usage and its impact on system performance.

</td></tr><tr><td>

Subscription Management

</td><td>

The Custom tables chart has been removed from the subscription details page.

</td></tr><tr><td>

Supplier Lifecycle Operations

</td><td>

-   **[Source-to-Pay Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/source-to-pay-operations/supplier-manager-workspace.md)**

Supplier Manager Workspace is being prepared for future deprecation. It’s hidden and no longer activated on new instances. Source-to-Pay Workspace provides the latest experience for this functionality.


</td></tr><tr><td>

Usage Insights

</td><td>

-   **[User Experience Analytics in Xanadu](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/now-intelligence/user-exp-analytics-landing.md)**

User Experience Analytics is no longer supported in the Xanadu release. Upgrade to Yokohama, Zurich, or Australia to continue using User Experience Analytics.


</td></tr><tr><td>

Virtual Agent

</td><td>

Support for Now Assist in Conversational IVR was removed.

</td></tr><tr><td>

Zero Copy Connector for ERP

</td><td>

The sn\_erp\_integration.enableJobModification property has been removed and is no longer required in order to schedule an extraction.

</td></tr></tbody>
</table>**Parent Topic:**[Release notes summaries for Yokohama features](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/release-notes-summaries.md)


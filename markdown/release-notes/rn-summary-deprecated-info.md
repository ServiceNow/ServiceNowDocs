---
title: Deprecation information for all Yokohama features and products
description: Cumulative release notes summary on deprecation information for Yokohama features and products.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2026-04-08"
reading_time_minutes: 9
breadcrumb: [Release notes summaries for Yokohama features, Release notes for upgrading from Xanadu, Learn about the Yokohama release, Yokohama release notes]
---

# Deprecation information for all Yokohama features and products

Cumulative release notes summary on deprecation information for Yokohama features and products.

For information about deprecated plugins in Yokohama, refer to Plugin information[Plugin information for all features and productsPlugin information](https://www.servicenow.com/docs/r/release-notes/rn-summary-plugin-info.html)

<table id="rn-summary-accessibility-table" class="custom-rows"><thead><tr><th class="filter">

Application or feature

</th><th>

Details

</th></tr></thead><tbody><tr><td>

AI Search

</td><td>

Starting with the Now Assist in AI Search 8.0 release, the External Content Q&amp;A Genius Results feature is being prepared for future deprecation. It will continue to be supported until it is deprecated. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

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

Common Core

</td><td>

The template data relationship table has been removed and deprecated for the Document designer application.

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

CMDB Data manager on Core UI is now deprecated and no longer supported or available for new activation. CMDB Workspace provides the latest experience for this functionality. For more information, see [CMDB Data Manager experience in CMDB Workspace](https://www.servicenow.com/docs/access?context=data-mgr-exp-cmdb-workspace&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td>

Data Separation

</td><td>

Starting with the Yokohama release, Data Separation is being prepared for future deprecation and it will be hidden. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base. Alternatively, you can define data filters along with other configurations to restrict access to sensitive data \(enable data separation\). For details on how to enable data separation for different use cases using data filters and ACLs, see the [Managing data separation using data filters and ACLs \[KB1772519\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB1772519) article in the Now SupportKnowledge Base.

</td></tr><tr><td>

Field Service Management

</td><td>

-   Starting with the Yokohama release, Approval Workflow for FSM is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.
-   Starting with the Zurich release, the **Enable capacity** constraint for Schedule Optimization is being prepared for future deprecation. It will be no longer be applied for Schedule Optimization. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

</td></tr><tr><td>

Generative AI Controller

</td><td>

The dependency on Sensitive Data Handler has been removed. Regular expressions that are configured with Sensitive Data Handler are applied to the Data Privacy application with a fix script when you upgrade to Yokohama.

</td></tr><tr><td>

Hardware Asset Management

</td><td>

The MAC address \[mac\_address\] field in the Hardware \[alm\_hardware\] table is deprecated. The data in this field is available in the new MAC address \(mac\_addr\) field in the Asset \[alm\_asset\] table.

</td></tr><tr><td>

ITOM Cloud Accelerate

</td><td>

-   Support for Cloud Provisioning and Governance: Google Cloud Connector has been removed. If you are on a legacy release, you cannot continue to use the Google Cloud Connector but you can use the Cloud Services Catalog Terraform Connector.
-   Support for Cloud Migration Assessment has been removed.

</td></tr><tr><td>

ITOM Optimization

</td><td>

These workflows have been deprecated:

-   Retrieve cloud billing data
-   Retrieve cloud billing month
-   Cloud operation step workflow launcher

**Note:** See  to learn more about the workflow migration.

For details, see the [Application/Plugin Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184) article in the Now Support Knowledge Base.

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

Instance Data Replication

</td><td>

Legacy replication sets are planned for deprecation by the Zurich release. To continue replicating data in Zurich, you must upgrade all legacy replication sets to V2. For details on upgrading legacy replication sets to V2 before the upgrade, see [Upgrading legacy replication sets to V2 in Instance Data Replication](https://www.servicenow.com/docs/access?context=upgrading-legacy-replication-sets-v2&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td>

Legacy Application Manager

</td><td>

Starting with Yokohama patch 11, Legacy Application Manager is being prepared for future deprecation. It will be hidden but will continue to be supported. For details, see the [Application/Plugin Deprecation Process \[KB0867184\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

</td></tr><tr><td>

Now Assist for IT Service Management \(ITSM\)

</td><td>

The Escalate IT Ticket core ITSM Virtual Agent topic is being deprecated in this release. The topic is renamed to **\(Deprecated\) Escalate IT Ticket**. This capability will be available in the Platform Request Status AI agent in a future release.

</td></tr><tr><td>

Now Assist in Virtual Agent

</td><td>

-   In Patch 11, **sn\_aia.use\_agents\_in\_planner** system property has been removed. The system property was used for configuring AI agent discovery behavior.
-   In Patch 11, Now Assist skills page in the assistant admin guided setup has been removed due to the skills being turned on by default.
-   In Patch 6, Bing support for the searching and scraping search result type is no longer supported when adding a web search tool in Now Assist Skill Kit.
-   In Patch 4, support for Now Assist in Conversational IVR was removed.

</td></tr><tr><td>

Operational Sustainability Management

</td><td>

Business rules were deactivated and moved to common script include methods as part of GRC Metrics. For more information, see the KB article: [KB1734660](https://support.servicenow.com/nav_to.do?uri=%2Fkb%3Fid%3Dkb_article_view%26sys_kb_id%3De92f82dd476a9610b8a4aa25126d4356).

</td></tr><tr><td>

Operational Technology Manager

</td><td>

-   For the Service Graph Connector for Microsoft Excel, the following items were deprecated on the ServiceNow AI Platform:
    -   The SG OT Excel Staging Task table
    -   The Staging task reference on the SG OT Excel Staging table
-   The OT Manager dashboard is no longer available in the Industrial Workspace.
-   Starting with the Yokohama release, Service Graph Connector for Microsoft Defender for IoT \(On-premises Management Console\) is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported.

</td></tr><tr><td>

Operational Technology Vulnerability Response

</td><td>

-   The **OT Vulnerabilities** tab is no longer available on the OT Manager dashboard in the Industrial Workspace.
-   Starting with the Yokohama release, **Vulnerability Response Integration with Microsoft Defender for IoT \(On-premises Management Console\)** integration is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported.

</td></tr><tr><td>

Order Management

</td><td>

-   The Subscription start and end dates have been deprecated starting with the Q2 2025 release. Use the Contract start date and Contract end date to calculate Terms for setting subscriptions for recurring products.
-   The fields listed for the following tables are no longer supported.

    |Table name|Fields|
    |----------|------|
    |Order \(sn\_ind\_tmt\_orm\_order\)|Total monthly recurring price, Total annual recurring price|
    |Order line item \(sn\_ind\_tmt\_orm\_order\_line\_item\)|Cumulative monthly recurring price, Cumulative annual recurring price, Subscription start date, Subscription end date|
    |Order line item \(sn\_csm\_om\_order\_line\_item\)|Total recurring price|


</td></tr><tr><td>

Patient Support Services

</td><td>

Starting with the Yokohama release, Patient Support Services is being prepared for future deprecation. It will be hidden and no longer installed on new instances but will continue to be supported. For details on this process, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

</td></tr><tr><td>

Playbooks in Workflow Studio

</td><td>

-   If you have the old Create Task activity in your existing playbooks, it will continue to function. You just can't add the extra fields that are available only in the new Create Task activity.
-   If you have the old Checklist activity in your existing playbooks, it will continue to function. You just won't be able to update the checklist directly in Workflow Studio the way that you can with the new Checklist activity.

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

With the Yokohama release, ITSM Predictive Intelligence Workbench is deprecated and no longer supported. To obtain the latest experience for this functionality, install the Task Intelligence for ITSM application \(com.snc.itsm\_ml\_task\). For more information, see [ITSM Predictive Intelligence Workbench release notes](../it-service-management/itsm-predictive-intelligence-workbench-rn.md).

</td></tr><tr><td>

Quote Management

</td><td>

The Subscription start date and Subscription end date have been deprecated starting with the Q2 2024 release. Use the Contract start date and Contract end date to calculate Terms for setting subscriptions for recurring products.

</td></tr><tr><td>

Redox Inbound Integration

</td><td>

Starting with the Yokohama release, Redox Inbound Integration is being prepared for future deprecation. It will be hidden and no longer installed on new instances but will continue to be supported. For details on this process, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

</td></tr><tr><td>

Site Reliability Operations

</td><td>

Starting with the Yokohama release, Release Management v2 is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. Digital Product Release provides the latest experience for this functionality. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184) article in the Now Support Knowledge Base.

</td></tr><tr><td>

Supplier Lifecycle Operations

</td><td>

-   **[Source-to-Pay Workspace](https://www.servicenow.com/docs/access?context=supplier-manager-workspace&version=yokohama&pubname=yokohama-source-to-pay-operations&ft:locale=en-US)**

Supplier Manager Workspace is being prepared for future deprecation. It’s hidden and no longer activated on new instances. Source-to-Pay Workspace provides the latest experience for this functionality.


</td></tr><tr><td>

Vendor Management Workspace

</td><td>

Starting with Yokohama release, the following applications within Vendor Management Workspace are being prepared for future deprecation. They will be hidden and no longer available for activation but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

-   Performance Analytics Content Pack - Vendor Management Workspace
-   Vendor Management Workspace UI Components
-   Vendor Manager Workspace Demo Data
-   Service Credits
-   Vendor Management Mobile

</td></tr><tr><td>

Virtual Agent

</td><td>

Support for Now Assist in Conversational IVR was removed.

</td></tr></tbody>
</table>**Parent Topic:**[Release notes summaries for Yokohama features](../release-notes-summaries.md)


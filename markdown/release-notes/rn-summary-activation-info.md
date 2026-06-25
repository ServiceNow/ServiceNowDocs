---
title: Activation information for all Xanadu features and products
description: Cumulative release notes summary on activation information for Xanadu features and products.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/release-notes/rn-summary-activation-info.html
release: xanadu
topic_type: reference
last_updated: "2026-06-13"
reading_time_minutes: 47
breadcrumb: [Release notes summaries for Xanadu features, Release notes for upgrading from Washington DC, Learn about the Xanadu release, Xanadu release notes]
---

# Activation information for all Xanadu features and products

Cumulative release notes summary on activation information for Xanadu features and products.

Some products and features require specific subscriptions, roles, or licenses. Other features are part of the  and are active by default.

<table id="rn-summary-activation-table" class="custom-rows"><thead><tr><th class="filter">

Application or feature

</th><th>

Details

</th></tr></thead><tbody><tr><td>

AI Search

</td><td>

AI Search is a ServiceNow AI Platform feature that is active by default.

</td></tr><tr><td>

AIOps LEAP

</td><td>

Install AIOps LEAP by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

Use one of the following steps to activate **AIOps LEAP**.

<table id="table_iwc_std_52c"><thead><tr><th>

Activate from

</th><th>

Steps

</th></tr></thead><tbody><tr><td>

Workspaces

</td><td>

1.  Select **Workspaces** on top, select **AIOps LEAP**.
2.  Select **Now Assist Admin Workspace**, select **Activate**.

</td></tr><tr><td>

Now Assist Admin

</td><td>

1.  Select **Admin** &gt; **Now Assist Admin** &gt; **Now Assist Skills**
2.  In the navigation pane, select **ITOM**.
3.  Select **Activate AIOps LEAP**.

</td></tr></tbody>
</table>

</td></tr><tr><td>

API

</td><td>

The following APIs are available by default:

-   Cloud Services Catalog API
-   DynamicSchemaAPI
-   GlideAggregate
-   GlideDate
-   GlideDynamicAttributeStore
-   GlideElementAttributeStore
-   GlideRecord
-   HistoryWalker
-   NumberFormatter
-   openFrameAPI
-   PDAutomationProvider
-   PDFGenerationAPI
-   PlaybookExperience
-   Product Catalog Open API
-   Service Order Open API

The following APIs require plugin activation:

-   The Appointment Open API requires the following plugins to be activated:
    -   Appointment Booking \(com.snc.appointment\_booking\)
    -   Field Service Management \(com.snc.work\_management\)
    -   Field Service Management for Telecommunications \(com.sn\_fsmt\)
    -   Telecommunication Open APIs \(com.sn\_tmf\_api\)
-   The AWA Manual Assignment API requires the Advanced Work Assignment \(com.glide.awa\) plugin to be activated.
-   The LeadtoCashCore script include requires the Lead to Cash Core \(com.snd.l2c.core\) plugin to be activated.
-   The PersonalAuthAPI requires the Personal Authentication \(com.snc.sn\_ihub\_personal\_auth\) plugin to be activated.
-   The Proactive Engagement API requires the Proactive Engagement \(proactive-engagement\) plugin to be activated.
-   The PSBPublicAPIUtil requires the Service Exchange for Providers application \(sn\_sb\_pro\) and the Service Exchange Base \(sn\_sb\) plugins to be activated.
-   The Resource Inventory Open API requires the Customer Network Inventory Core application \(com.app-ni-core\) plugin to be activated.
-   The Service Contract API requires the following plugins to be activated:
    -   Customer Contracts and Entitlements \(com.sn\_pss\_core\)
    -   Customer Service Install Base Management \(com.snc.install\)
    -   Product Catalog Management Core \(com.sn\_prd\)
-   The Service Test Management Open API requires the Customer Service Problem Management \(com.sn\_sprb\_mgmt\) plugin to be activated.
-   The Verify Entitlements API requires the Entitlement Verification \(sn\_ent\_verify\) plugin to be activated.
-   The WSD Extra Service Request API requires the Workplace Reservation Management \(com.sn\_wsd\_rsv\) plugin to be activated.
-   The WSD Reservable API requires the Workplace Reservation Management \(com.sn\_wsd\_rsv\) plugin to be activated.
-   The WSD Reservable V2 API requires the Workplace Reservation Management \(com.sn\_wsd\_rsv\) plugin to be activated.

</td></tr><tr><td>

Access Management

</td><td>

Access Management is a ServiceNow AI Platform feature that is active by default.

</td></tr><tr><td>

Accounts Payable Operations

</td><td>

Install Accounts Payable Operations by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

</td></tr><tr><td>

Adoption Services

</td><td>

Adoption Services is a ServiceNow AI Platform feature that is active by default.

</td></tr><tr><td>

Advanced AI Search Management Tools

</td><td>

Install Advanced AI Search Management Tools by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

</td></tr><tr><td>

Advanced Risk

</td><td>

Install Advanced Risk by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

</td></tr><tr><td>

Advanced Work Assignment

</td><td>

Advanced Work Assignment is a ServiceNow AI Platform feature that is available with activation of the Glide Advanced Work Assignment plugin \(com.glide.awa\). For details, see [Activate Advanced Work Assignment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/servicenow-platform/advanced-work-assignment/awa-activate.md).

To use the External routing functionality on your instance, you must activate the External Routing Support plugin \(com.glide.awa-external\).

</td></tr><tr><td>

Agent Chat

</td><td>

Agent Chat is a ServiceNow AI Platform feature that is available with activation of the Agent Chat plugin \(com.glide.interaction.awa\). For details, see [Configuring Agent Chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/conversational-interfaces/agent-chat/ci-agent-chat-configuring.md).

</td></tr><tr><td>

Agent Client Collector

</td><td>

Agent Client Collector is available with activation of the Agent Client Collector Framework plugin \(sn\_agent\) and the Agent Client Collector Monitoring plugin \(sn\_itmon\) in an instance on which Event Management is installed.

</td></tr><tr><td>

Agent Workspace for HR Case Management

</td><td>

Install Agent Workspace for HR Case Management by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

</td></tr><tr><td>

Agent experience for CSM

</td><td>

Install CSM Configurable Workspace by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

</td></tr><tr><td>

Analytics, Intelligence, and Reporting

</td><td>

Analytics, Intelligence, and Reporting functionality is a ServiceNow AI Platform feature that is active by default. Some data sources, such as indicators, may require a subscription.

</td></tr><tr><td>

App Engine Studio

</td><td>

Install App Engine Studio by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

</td></tr><tr><td>

Application Manager

</td><td>

Application Manager is a ServiceNow AI Platform feature that is active by default.

</td></tr><tr><td>

Application Vulnerability Response

</td><td>

Install Application Vulnerability Response by requesting it from the ServiceNow Store. Application Vulnerability Response is included as a part of the Vulnerability Response application. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

</td></tr><tr><td>

Assessments and Surveys

</td><td>

Assessments and Surveys is a ServiceNow AI Platform feature that is active by default.

</td></tr><tr><td>

Audit Management

</td><td>

Install Policy and Compliance Management by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

</td></tr><tr><td>

Authentication

</td><td>

Authentication is a ServiceNow AI Platform product that is active by default.

</td></tr><tr><td>

Benchmarks

</td><td>

Benchmarks is a ServiceNow AI Platform feature that is active by default. The new Benchmarks dashboard is automatically installed with Xanadu and is available from the ServiceNow Store.

</td></tr><tr><td>

Business Continuity Management

</td><td>

Install Business Continuity Management by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

</td></tr><tr><td>

Case and Knowledge Management

</td><td>

Case and Knowledge Management is a ServiceNow AI Platform feature that is available with activation of the Human Resources Scoped App: Core \[com.sn\_hr\_core\].

</td></tr><tr><td>

Case management for CSM

</td><td>

Customer Service Management is a ServiceNow AI Platform feature that is available with activation of the Customer Service Management plugin \(com.sn\_customerservice\). For details, see .

Additional Customer Service Management features are available with the activation of other plugins. For details, see .

</td></tr><tr><td>

Cloud Cost Management 8.0.0

</td><td>

Activate Cloud Cost Management by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

</td></tr><tr><td>

Collaborative Work Management

</td><td>

Install Collaborative Work Management by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

</td></tr><tr><td>

Common Governance, Risk, and Compliance feature

</td><td>

Install GRC by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

</td></tr><tr><td>

Compliance Case Management

</td><td>

Install the Regulatory Agency Library by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

CMDB is a ServiceNow AI Platform feature that is active by default.

</td></tr><tr><td>

Continuous Authorization and Monitoring

</td><td>

Install Continuous Authorization and Monitoring by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

</td></tr><tr><td>

Core ServiceNow AI Platform

</td><td>

ServiceNow AI Platform is a ServiceNow AI Platform feature that is active by default.

</td></tr><tr><td>

Creator Studio

</td><td>

Install Creator Studio by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

</td></tr><tr><td>

Customer Contracts and Entitlements

</td><td>

Install Customer Contracts and Entitlements by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

Customer Contracts and Entitlements is available with activation of the Customer Contracts and Entitlements \(com.sn\_pss\_core\) plugin, which requires a separate subscription. For details, see .

**Note:** With the activation of Customer Contracts and Entitlements, new contracts and entitlements are created using the new data model only. The new entitlement verification APIs and change workflows are based on the new data model. Older contracts and entitlements remain available for viewing.

</td></tr><tr><td>

Customer Success Management

</td><td>

Install Account Lifecycle Events by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

</td></tr><tr><td>

Data Management

</td><td>

Data Management is a ServiceNow AI Platform feature that is active by default.

</td></tr><tr><td>

Data management for CSM

</td><td>

Customer Service Management is a ServiceNow AI Platform feature that is available with activation of the Customer Service Management plugin \(com.sn\_customerservice\). For details, see .

Additional Customer Service Management features are available with the activation of other plugins. For details, see .

Sales Customer Relationship Management is a ServiceNow AI Platform feature that is available with the activation of the Lead to Cash Core plugin \(com.snd.l2c.core\). For details, see [Exploring Sales Customer Relationship Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/order-management/sales-and-order-management/som-exploring.md).

</td></tr><tr><td>

DevOps Change Velocity

</td><td>

Activate DevOps Change Velocity by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

</td></tr><tr><td>

Digital End-User Experience

</td><td>

Install DEX by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

</td></tr><tr><td>

Digital Portfolio Management

</td><td>

Install Digital Portfolio Management by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

</td></tr><tr><td>

Dispute Content Pack for US Regulations

</td><td>

Install Dispute Content Pack for US Regulations by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

</td></tr><tr><td>

Dispute Rules Content Pack for Mastercard

</td><td>

Install Dispute Rules Content Pack for Mastercard by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

</td></tr><tr><td>

Dispute Rules Content Pack for Visa

</td><td>

Install Dispute Rules Content Pack for Visa by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

</td></tr><tr><td>

Document Intelligence

</td><td>

Install Document Intelligence by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html). The Document Intelligence application \(sn\_docintel\) depends on the Document Intelligence plugin \(com.glide.platform\_ml\_di\), the Predictive Intelligence plugin \(com.glide.platform\_ml\), and the Document Intelligence UIB component \(com.sn\_docintel\_iframe\). For more details, see Install Document Intelligence.

</td></tr><tr><td>

Document Services

</td><td>

Document Services is a ServiceNow AI Platform feature that is active by default.

Document Management is available with activation of the Document Management plugin \(com.snc.platform\_document\_management\). For details, see [Activate Document Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/servicenow-platform/document-management-services/activate-doc-mgmt-plugin.md).

[Multi Provider Document Services Framework](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/servicenow-platform/document-management-services/multi-provider-documents-framework.md) Install Multi Provider Document Services Framework by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

</td></tr><tr><td>

Document Templates

</td><td>

Install Document Templates by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

</td></tr><tr><td>

Dynamic Translation

</td><td>

Dynamic Translation is a ServiceNow AI Platform feature that is available with activation of the Dynamic Translation plugin \(com.glide.dynamic\_translation\). For details, see .

</td></tr><tr><td>

ERP Semantic Mining

</td><td>

Install ERP Customization Mining by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

</td></tr><tr><td>

Employee Center

</td><td>

Install Employee Center plugins by requesting them from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

</td></tr><tr><td>

Employee Relations

</td><td>

Employee Relations is a ServiceNow AI Platform feature that is available with activation of the Employee Relations plugin \(com.sn\_hr\_employee\_relations\). For details, see [Activate Employee Relations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/employee-service-management/hr-service-delivery/activate-hr-employee-relations.md).

</td></tr><tr><td>

Encryption Key Management

</td><td>

The Platform Encryption subscription bundle is a group commercial entitlement that includes Column Level Encryption Enterprise, Cloud Encryption, and Database Encryption.

Column Level Encryption Enterprise is the unlimited license of Column Level Encryption. The Enterprise plugin is available with the activation of the com.glide.now.platform.encryption plugin. For details, see [Encryption and Key Management subscription bundle](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/platform-security/platform-encryption/encryption-sku.md).

</td></tr><tr><td>

Enterprise Architecture \(formerly Application Portfolio Management\)

</td><td>

Enterprise Architecture \(formerly Application Portfolio Management\) is available with activation of the Enterprise Architecture \(com.snc.apm\), which requires a separate subscription. For details, see [Enterprise Architecture](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/application-portfolio-management/enterprise-architecture/application-portfolio-management-landing-page.md).

</td></tr><tr><td>

Enterprise Asset Management

</td><td>

Install the following applications by requesting them from the ServiceNow Store:

-   Enterprise Asset Management
-   Enterprise Asset Management for Healthcare
-   OT Asset Management
-   Expanded Model and Asset Classes

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

</td></tr><tr><td>

Event Management

</td><td>

Event Management is available with activation of the Event Management plugin \(com.glideapp.itom.snac\). For details, see [Request Event Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/it-operations-management/event-management/t_EMActivatePlugin.md).

</td></tr><tr><td>

External Content Connectors

</td><td>

Install External Content Connectors by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

</td></tr><tr><td>

Field Service Management

</td><td>

Field Service Management is a ServiceNow AI Platform feature that is available with activation of the Field Service Management plugin \(field\_service\_management\). For details, see [Activate Field Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/field-service-management/t_ActivateFieldServiceManagement.md).

Additional Field Service Management features are available with the activation of other plugins. For details, see [Additional plugins for Field Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/field-service-management/field-service-additional-plugins.md).

Enable field service technicians to initiate and monitor sales opportunities directly through the Now Mobile Agent application by activating Technician driven sales with the Field Service \(com.snc.fsm\_technician\_sales\) plugin.

</td></tr><tr><td>

Field Service Management for Telecommunication

</td><td>

Telecommunications appointment booking feature is available with activation of the Telecommunications Open API \(com.sn\_tmf\_api\), Appointment Booking \(com.snc.appointment\_booking\), Field Service Management \(com.snc.work\_management\), Field Service Management for Telecommunications \(com.sn\_fsmt\), and Telecommunications, Media and Technology Core \(com.sn\_tmt\_core\) applications. Install these applications by requesting them from the ServiceNow Store.

</td></tr><tr><td>

Financial Services Card Operations

</td><td>

Install Financial Services Card Operations by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

</td></tr><tr><td>

Financial Services Operations Integration with Visa

</td><td>

Install Now Assist for FSO by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

</td></tr><tr><td>

Flows, subflows, and actions in Workflow Studio

</td><td>

Workflow Studio is a ServiceNow AI Platform feature that is active by default.

</td></tr><tr><td>

Generative AI Controller

</td><td>

Generative AI Controller is a ServiceNow AI Platform feature that is available with activation of any ServiceNow® Now Assist application. For details, see Installing Generative AI Controller.

</td></tr><tr><td>

Goal Framework

</td><td>

Install Goal Framework by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

</td></tr><tr><td>

Goal Framework for SPM

</td><td>

Install Goal Framework for SPM by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

</td></tr><tr><td>

HR Service Delivery for Healthcare

</td><td>

Install HR Service Delivery for Healthcare by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

</td></tr><tr><td>

Hardware Asset Management 11.0.0

</td><td>

Install Hardware Asset Management by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

</td></tr><tr><td>

Health Log Analytics

</td><td>

Install Health Log Analytics by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

</td></tr><tr><td>

Healthcare and Life Sciences Service Management Core

</td><td>

Install Healthcare and Life Sciences Service Management Core by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

</td></tr><tr><td>

Hermes Messaging Service

</td><td>

Hermes Messaging Service is a ServiceNow AI Platform feature that is available with activation of the ServiceNow Stream Connect Installer \(com.glide.hub.stream\_connect.installer\) plugin or installation of the Log Export Service application. For details, see [Hermes Messaging Service activation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/servicenow-platform/multi-instance-framework-hermes/hermes-messaging-service-activation.md).

</td></tr><tr><td>

ITOM AIOps

</td><td>

ITOM Health is available with activation of the Event Management plugin \(com.glideapp.itom.snac\). To work with Health Log Analytics, you must purchase ITOM Predictive AIOps, a more comprehensive ITOM Health package. For details, see [Event Management setup](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/it-operations-management/event-management/c_EMConfiguration.md).

Install Service Operations Workspace \(ITOM\) by installing the AIOps Experience \[sn\_sow\_aiops\] application from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

</td></tr><tr><td>

ITOM Cloud Accelerate

</td><td>

The ITOM Cloud Accelerate features are available as an application with the activation of the Cloud Accelerate plugin, which requires a Cloud Governance subscription. Contact your ServiceNow sales representative to procure the ITOM Cloud Accelerate entitlement.

The [Cloud Services Catalog](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/it-operations-management/cloud-services-catalog/csc-home.md) application is available with the [ITOM Cloud Accelerate](https://www.servicenow.com/docs/access?context=cloud-governance&version=xanadu) entitlements. Alternatively, you can install it by requesting them from [https://store.servicenow.com/sn\_appstore\_store.do\#!/store/application/bc3429fc24e02910f877b722d6bbdcaf](https://store.servicenow.com/sn_appstore_store.do#!/store/application/bc3429fc24e02910f877b722d6bbdcaf).

You must have Employee Center as a prerequisite to launch and use the [Cloud Service Catalog](https://www.servicenow.com/docs/access?context=csc-home&version=xanadu) application.

</td></tr><tr><td>

ITOM Visibility

</td><td>

ITOM Visibility is available with activation of the Discovery \(com.snc.discovery\) plugin and the Service Mapping \(com.snc.service-mapping\) plugin, which require an ITOM Visibility subscription. For details, see [Request Discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/it-operations-management/discovery/t_ActivateTheDiscoveryPlugin.md) and [Request Service Mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/it-operations-management/service-mapping/t_ActivateServiceMappingPlugin.md). For full ITOM Visibility functionality, install the latest ITOM Visibility out-of-band applications from the ServiceNow Store. For cumulative release note information for all released apps, see the ServiceNow Store version history release notes.

</td></tr><tr><td>

ITSM Mobile Agent

</td><td>

Install ITSM Mobile Agent by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

</td></tr><tr><td>

ITSM Success Dashboard

</td><td>

Install ITSM Success Dashboard by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

</td></tr><tr><td>

Identity

</td><td>

Identity is a ServiceNow AI Platform product that is active by default.

</td></tr><tr><td>

Incident Management

</td><td>

Incident Management is a ServiceNow AI Platform feature that is active by default.

</td></tr><tr><td>

Individual Life Claims

</td><td>

Install Individual Life Claims by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

</td></tr><tr><td>

Industrial Process Manager

</td><td>

Install Industrial Process Manager by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

**Note:** Industrial Process Manager is automatically installed with Operational Technology Incident Management and Operational Technology Change Management.

</td></tr><tr><td>

Insurance claims

</td><td>

Install Insurance claims by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

</td></tr><tr><td>

Integration Hub

</td><td>

Integration Hub is included in Workflow Data Fabric and is available with activation of an Workflow Data Fabric subscription package. For details, see [https://www.servicenow.com/products/automation-engine.html](https://www.servicenow.com/products/automation-engine.html).

</td></tr><tr><td>

Intelligence for CSM

</td><td>

Install the Guided Decisions, Recommended Actions, and Task Intelligence applications by requesting them from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

</td></tr><tr><td>

Journey designer

</td><td>

Install Journey designer by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

</td></tr><tr><td>

Knowledge Management

</td><td>

Knowledge Management is a ServiceNow AI Platform feature that is active by default.

</td></tr><tr><td>

Lead Management

</td><td>

Install Lead Management by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

</td></tr><tr><td>

Leader Hub

</td><td>

Install Leader Hub by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

</td></tr><tr><td>

Localization Framework

</td><td>

Localization Framework is a ServiceNow AI Platform feature that is available with activation of the Localization Framework installer \(com.glide.localization\_framework.installer\). For details, see .

</td></tr><tr><td>

MID Server

</td><td>

MID Server is a ServiceNow AI Platform feature that is active by default.

</td></tr><tr><td>

Manufacturing Commercial Operations

</td><td>

Install Manufacturing applications by requesting them from the ServiceNow Store. For details on installing the applications, see [Configuring Manufacturing Commercial Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/manufacturing/configuring-manufacturing-foundation.md). Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

</td></tr><tr><td>

Microsoft Azure DevOps Integration for Agile Development

</td><td>

Install Microsoft Azure DevOps Integration for Agile Development by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

</td></tr><tr><td>

Mobile Platform

</td><td>

ServiceNow Mobile Platform is a ServiceNow AI Platform® feature that is active by default.

</td></tr><tr><td>

Next Experience

</td><td>

Next Experience is a ServiceNow AI Platform feature that is active by default when the user loads or upgrades to the Xanadu release. An opt-out system property can be created prior to upgrade if there are known problems with turning on Next Experience on an instance.

Install Theme Builder by requesting it from the ServiceNow Store.

</td></tr><tr><td>

Next Experience Components

</td><td>

Next Experience Components is a ServiceNow AI Platform feature that is active by default.

</td></tr><tr><td>

Notifications

</td><td>

Notifications is a ServiceNow AI Platform feature that is active by default.

</td></tr><tr><td>

Notify

</td><td>

Notify is a ServiceNow AI Platform feature that is available with activation of the Notify \(com.snc.notify\) plugin. For details, see [Notify](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/servicenow-platform/notify/notify-landing-page.md).

</td></tr><tr><td>

Now Assist

</td><td>

Now Assist features are available with activation of any Now Assist plugin from the ServiceNow Store. The following plugins are available:

-   [Now Assist for Accounts Payable Operations \(APO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/source-to-pay-operations/accounts-payable-operations/now-assist-apo.md)
-   [Now Assist for Configuration Management Database \(CMDB\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/servicenow-platform/now-assist-for-configuration-management-database-cmdb/now-assist-landing-cmdb.md)
-   
-   
-   [Now Assist for Field Service Management \(FSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/field-service-management/now-assist-for-field-service-management-fsm/now-assist-fsm.md)
-   [Now Assist for Financial Services Operations \(FSO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/financial-services-operations/now-assist-for-financial-services-operations-fso/now-assist-for-financial-services-operations.md)
-   [Now Assist for Health and Safety](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/employee-service-management/now-assist-for-health-and-safety/now-assist-hs-landing.md)
-   [Now Assist for HR Service Delivery \(HRSD\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/employee-service-management/now-assist-for-hrsd/now-assist-hrsd.md)
-   [Now Assist for IT Operations Management \(ITOM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/it-operations-management/now-assist-for-it-operations-management/now-assist-itom.md)
-   [Now Assist for IT Service Management \(ITSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/it-service-management/now-assist-for-it-service-management-itsm/now-assist-itsm.md)
-   [Now Assist for Legal Service Delivery \(LSD\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/employee-service-management/now-assist-for-legal-service-delivery/now-assist-lsd-landing.md)
-   [Now Assist for PSDS](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/government-industry/public-sector-digital-services/now-assist-for-psds.md)
-   [Now Assist for Security Incident Response](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/security-management/now-assist-for-security-incident-response-sir/now-assist-security-incident-landing.md)
-   [Now Assist for Supplier Lifecycle Operations \(SLO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/source-to-pay-operations/supplier-lifecycle-operations/now-assist-slo.md)
-   [Now Assist for Sourcing and Procurement Operations \(SPO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/source-to-pay-operations/sourcing-and-procurement-operations/now-assist-spo.md)
-   [Now Assist for Strategic Portfolio Management \(SPM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/it-business-management/now-assist-for-strategic-portfolio-management-spm/now-assist-spm.md)
-   [Now Assist for Telecommunications, Media and Technology \(TMT\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/telecom-media-technology/now-assist-for-telecom-media-and-technology/now-assist-spmc.md)

For more information, see .

</td></tr><tr><td>

Now Assist AI agents

</td><td>

Now Assist in AI agents is available with activation of any Now Assist plugin from the ServiceNow Store. For more information about the prerequisites for using Now Assist, see .

</td></tr><tr><td>

Now Assist for Creator

</td><td>

Install Now Assist for Creator by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

</td></tr><tr><td>

Now Assist for Customer Service Management \(CSM\)

</td><td>

Now Assist features are available with activation of the Now Assist for CSM plugin. For more information, see .

Starting with Vancouver Patch 4, Now Assist for CSM is supported.

Starting with Xanadu Patch 7, Customer Service Management AI agent collection is supported.

</td></tr><tr><td>

Now Assist for Enterprise Architecture \(EA\)

</td><td>

Now Assist features are available with activation of the Now Assist for Enterprise Architecture \(EA\) plugin. The [Now Assist for Enterprise Architecture \(EA\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/application-portfolio-management/enterprise-architecture/now-assist-ea.md) application requires an Enterprise Architecture Pro plus license. For more information, see .

</td></tr><tr><td>

Now Assist for Field Service Management \(FSM\)

</td><td>

Now Assist features are available with activation of the Now Assist for FSM plugin. For more information, see .

</td></tr><tr><td>

Now Assist for Financial Services Operations \(FSO\)

</td><td>

Install Now Assist for FSO by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

</td></tr><tr><td>

Now Assist for Hardware Asset Management \(HAM\)

</td><td>

Install Now Assist for Hardware Asset Management \(HAM\) by requesting it from the ServiceNow Store.

**Note:** To take full advantage of the Now Assist for HAM features, you should upgrade to Xanadu Patch 10 and install the Now Assist for Hardware Asset Management \(HAM\) store application.

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

</td></tr><tr><td>

Now Assist for IT Operations Management \(ITOM\)

</td><td>

Install Now Assist for ITOM by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

</td></tr><tr><td>

Now Assist for IT Service Management \(ITSM\)

</td><td>

Install Now Assist for ITSM by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

-   **Important:** To enable the display of the Generate post incident reviews use case, you must activate the Incident Management - Major Incident Management plugin \(com.snc.incident.mim\). For more information, see [Activate Incident Management - Major Incident Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/it-service-management/incident-management/activate-major-incident-management-plugin.md).

-   **Important:** To enable the display of the Notify users with Twilio use case, you must activate the Twilio Spoke plugin \(sn\_twilio\_spoke\). For more information, see .


</td></tr><tr><td>

Now Assist for Security Operations

</td><td>

Install Now Assist for Security Operations by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

</td></tr><tr><td>

Now Assist for Source-to-Pay Operations

</td><td>

Install Now Assist for Source-to-Pay Operations by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

</td></tr><tr><td>

Now Assist for Strategic Portfolio Management \(SPM\)

</td><td>

Now Assist features are available with activation of the [Now Assist for Strategic Portfolio Management \(SPM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/it-business-management/now-assist-for-strategic-portfolio-management-spm/now-assist-spm.md) plugin. For more information, see .

</td></tr><tr><td>

Now Assist for Telecommunications, Media and Technology \(TMT\)

</td><td>

Now Assist features are available with activation of the Now Assist for TMT plugin. For more information, see Install Now Assist plugins.

</td></tr><tr><td>

Now Assist in AI Search

</td><td>

Now Assist in AI Search is installed when you install any of the following licensed applications from the ServiceNow Store.

-   
Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

</td></tr><tr><td>

Now Assist in Virtual Agent

</td><td>

Now Assist features are available with activation of any Now Assist plugin from the ServiceNow Store. The following plugins are available:

-   [Now Assist for Accounts Payable Operations \(APO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/source-to-pay-operations/accounts-payable-operations/now-assist-apo.md)
-   [Now Assist for Configuration Management Database \(CMDB\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/servicenow-platform/now-assist-for-configuration-management-database-cmdb/now-assist-landing-cmdb.md)
-   
-   
-   [Now Assist for Field Service Management \(FSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/field-service-management/now-assist-for-field-service-management-fsm/now-assist-fsm.md)
-   [Now Assist for Financial Services Operations \(FSO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/financial-services-operations/now-assist-for-financial-services-operations-fso/now-assist-for-financial-services-operations.md)
-   [Now Assist for Health and Safety](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/employee-service-management/now-assist-for-health-and-safety/now-assist-hs-landing.md)
-   [Now Assist for HR Service Delivery \(HRSD\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/employee-service-management/now-assist-for-hrsd/now-assist-hrsd.md)
-   [Now Assist for IT Operations Management \(ITOM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/it-operations-management/now-assist-for-it-operations-management/now-assist-itom.md)
-   [Now Assist for IT Service Management \(ITSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/it-service-management/now-assist-for-it-service-management-itsm/now-assist-itsm.md)
-   [Now Assist for Legal Service Delivery \(LSD\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/employee-service-management/now-assist-for-legal-service-delivery/now-assist-lsd-landing.md)
-   [Now Assist for PSDS](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/government-industry/public-sector-digital-services/now-assist-for-psds.md)
-   [Now Assist for Security Incident Response](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/security-management/now-assist-for-security-incident-response-sir/now-assist-security-incident-landing.md)
-   [Now Assist for Supplier Lifecycle Operations \(SLO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/source-to-pay-operations/supplier-lifecycle-operations/now-assist-slo.md)
-   [Now Assist for Sourcing and Procurement Operations \(SPO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/source-to-pay-operations/sourcing-and-procurement-operations/now-assist-spo.md)
-   [Now Assist for Strategic Portfolio Management \(SPM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/it-business-management/now-assist-for-strategic-portfolio-management-spm/now-assist-spm.md)
-   [Now Assist for Telecommunications, Media and Technology \(TMT\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/telecom-media-technology/now-assist-for-telecom-media-and-technology/now-assist-spmc.md)

For more information, see [Configuring Now Assist in Virtual Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/conversational-interfaces/now-assist-in-virtual-agent/configure-now-assist-va.md).

</td></tr><tr><td>

On-Call Scheduling

</td><td>

On-Call Scheduling is available with activation of the ServiceNow AI Platform On-Call Scheduling plugin \(com.snc.on\_call\_rotation\). For details, see [Activate On-Call Scheduling](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/it-service-management/on-call-scheduling/t_ActivateOnCallScheduling.md). Activating this plugin activates the following third-party libraries:

-   FullCalendar library
-   DHTMLX scheduler

**Note:** The On-Call Scheduling \(com.snc.on\_call\_rotation\) plugin is active by default for zBoot customers.

</td></tr><tr><td>

Operational Resilience

</td><td>

Install Operational Resilience by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

</td></tr><tr><td>

Operational Sustainability Management

</td><td>

Install ESG Management by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

</td></tr><tr><td>

Operational Technology Change Management

</td><td>

Install Operational Technology Change Management by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

**Note:** Operational Technology Change Management now includes the Industrial Process Manager, and can be used with or without Operational Technology Manager.

</td></tr><tr><td>

Operational Technology Incident Management

</td><td>

Install Operational Technology Incident Management by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

**Note:** Operational Technology Incident Management now includes the Industrial Process Manager, and can be used with or without Operational Technology Manager.

</td></tr><tr><td>

Operational Technology Manager

</td><td>

Install Operational Technology Manager by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

</td></tr><tr><td>

Operational Technology Request Management

</td><td>

Operational Technology Request Management is included with the Industrial Workspace Common. No additional plugins are needed.

</td></tr><tr><td>

Operational Technology Vulnerability Response

</td><td>

Install Operational Technology Vulnerability Response by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

</td></tr><tr><td>

Opportunity Management

</td><td>

Install Opportunity Management by requesting it from ServiceNow Store.

</td></tr><tr><td>

Order Management

</td><td>

Install Order Management by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

</td></tr><tr><td>

Password Reset

</td><td>

Password Reset is a ServiceNow AI Platform feature that is active by default.

</td></tr><tr><td>

Performance Analytics

</td><td>

Complimentary Performance Analytics for Incident Management is active by default. You cannot create indicators or breakdowns with this application.

The full features of Performance Analytics are available with a subscription. Activate the Performance Analytics plugin that matches your subscription. For details, see .

</td></tr><tr><td>

Platform Analytics experience

</td><td>

Platform Analytics is a ServiceNow AI Platform feature that is active by default. Some data sources, such as indicators, may require a subscription.

</td></tr><tr><td>

Playbooks in Workflow Studio

</td><td>

The application comes with the Workflow Studio ServiceNow Store app. Workflow Studio is part of the ServiceNow AI Platform® and is available by default. Get the latest Workflow Studio features by downloading the app in the ServiceNow Store, as well as related applications like the Process Automation Experience Demo application.

To use the playbook generation feature in Workflow Studio, download the [Now Assist for Creator](https://store.servicenow.com/sn_appstore_store.do#!/store/application/8178fec0ce0431105a7c9305875b2dca) application.

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

</td></tr><tr><td>

Policy and Compliance Management

</td><td>

Install Policy and Compliance Management by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

</td></tr><tr><td>

Portfolio Planning

</td><td>

Install Portfolio Planning by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

</td></tr><tr><td>

Predictive Intelligence

</td><td>

Predictive Intelligence is a ServiceNow AI Platform feature that is available with activation of the Predictive Intelligence Reports \(com.glide.platform\_ml\_pa\) plugin and its dependent Predictive Intelligence \(com.glide.platform\_ml\) plugin. For details, see .

</td></tr><tr><td>

Privacy Management

</td><td>

Install Privacy Management by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

</td></tr><tr><td>

Proactive Engagement

</td><td>

Install Proactive Engagement by requesting it from the ServiceNow Store. Activate the following plugins:

-   Proactive Engagement \(sn\_pren\)
-   DEX Application and Device Health \(sn\_dex\)
-   Glide Virtual Agent \(com.glide.cs.chatbot\)

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes.](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html)

</td></tr><tr><td>

Proactive Service Experience Workflows

</td><td>

Install Proactive Service Experience Workflows by requesting it from the ServiceNow Store.

</td></tr><tr><td>

Problem Management

</td><td>

[Problem Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/it-service-management/problem-management/c_ProblemManagement.md) is a ServiceNow AI Platform feature that is active by default.

</td></tr><tr><td>

Process Mining

</td><td>

Process Mining is available with activation of the sn\_po plugin.

</td></tr><tr><td>

Product Catalog Management and Pricing Management

</td><td>

The Product Catalog Management and Pricing Management features are included with each store application and don’t need activation. Depending on your entitlements, you can install the Product and Pricing Rules application for pricing and product eligibility matrices and the Product Configurator feature from the ServiceNow Store.

</td></tr><tr><td>

Project Portfolio Management

</td><td>

Project Portfolio Management is a ServiceNow AI Platform feature that is active by default.

</td></tr><tr><td>

Project Workspace

</td><td>

Install Project Workspace by requesting it from the ServiceNow Store. Starting with the Xanadu release, installing the PPM Standard plugin \(com.snc.financial\_planning\_pmo\) also installs the Project Workspace application.

</td></tr><tr><td>

Public Sector Digital Services

</td><td>

Install Public Sector Digital Services applications by requesting them from the ServiceNow Store. For details on installing the applications, see [Configuring Public Sector Digital Services](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/government-industry/public-sector-digital-services/configuring-public-sector-digital-services.md). Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

</td></tr><tr><td>

Quote Management

</td><td>

Install Quote Management by requesting it from the ServiceNow Store.

</td></tr><tr><td>

RPA Hub

</td><td>

Install RPA Hub by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

For cumulative release notes information on RPA Hub, see RPA Hub release notes.

For cumulative release notes information on RPA Desktop Design Studio, see RPA Plugin Bundle release notes.

If you have previously downloaded the application from the ServiceNow Store and a new version is available, you can update it in your ServiceNow AI Platform instance at **All** &gt; **System Applications** &gt; **All Available Applications**.

</td></tr><tr><td>

Regulatory Change Management

</td><td>

Install Regulatory Change Management by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

</td></tr><tr><td>

Release Management

</td><td>

Release Management is available with activation of the Release Management plugin \(com.snc.release\_management\_v2\). For details, see [Activate Release Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/it-service-management/release-management/t_ActivateReleaseManagement.md).

</td></tr><tr><td>

Resource Management Workspace

</td><td>

Install the Resource Management Workspace application by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

</td></tr><tr><td>

Retail Operations

</td><td>

Install Retail Operations by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

</td></tr><tr><td>

Security Center

</td><td>

Security Center v1.5 is installed by default with the Xanadu family release. Version 1.6 provides significant enhancements. To get Security Center v1,6, visit the [ServiceNow store](https://store.servicenow.com/sn_appstore_store.do#!/store/home).

</td></tr><tr><td>

Security Incident Response

</td><td>

Install Security Incident Response by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

</td></tr><tr><td>

Security Posture Control

</td><td>

Install Security Posture Control by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

</td></tr><tr><td>

Service Catalog

</td><td>

Service Catalog is a ServiceNow AI Platform feature that is active by default.

</td></tr><tr><td>

Service Exchange

</td><td>

Install Service Exchange by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

</td></tr><tr><td>

Service Graph Connector Integration for Claroty CTD

</td><td>

Install Service Graph Connector Integration for Claroty CTD by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

**Note:** Claroty CTD v5.1 is also supported for the Service Graph Connector Integration for Claroty CTD application.

</td></tr><tr><td>

Service Graph Connector for Microsoft Defender for IoT \(Azure\)

</td><td>

Install Service Graph Connector for Microsoft Defender for IoT \(Azure\) by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

</td></tr><tr><td>

Service Operations Workspace for ITSM

</td><td>

Service Operations Workspace for ITSM is active by default and its default version is 5.0 in Xanadu. When you upgrade from any previous release to Xanadu from ServiceNow Store, Service Operations Workspace for ITSM 5.0 is automatically installed.

</td></tr><tr><td>

Service Portal

</td><td>

Service Portal is a ServiceNow AI Platform feature that is active by default.

</td></tr><tr><td>

Service Portfolio Management

</td><td>

The Service Portfolio Management Core plugin \[com.snc.service\_portfolio\_core\] is available by default for IT Service Management licensed customers. For more information, see [Activate Service Portfolio Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/it-service-management/service-portfolio-management/activate-SPM2-plugin.md).

</td></tr><tr><td>

Service Reliability Management

</td><td>

Install Service Reliability Management by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

</td></tr><tr><td>

ServiceNow IDE

</td><td>

Install ServiceNow IDE \(sn\_glider\) by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

</td></tr><tr><td>

ServiceNow SDK

</td><td>

The ServiceNow SDK is available as an npm package from the [public npm registry](https://www.npmjs.com/package/@servicenow/sdk) and installed locally. For information about installing the ServiceNow SDK, see .

</td></tr><tr><td>

ServiceNow Studio

</td><td>

Install ServiceNow Studio by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

</td></tr><tr><td>

Sidebar

</td><td>

Install Sidebar by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

</td></tr><tr><td>

Skills Intelligence

</td><td>

Install Skills Foundation by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

</td></tr><tr><td>

Skills Management

</td><td>

Skills Management is available with the activation of the Skills Management \(com.snc.skills\_management\) plugin. For details, see [Activating Skills Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/servicenow-platform/skills-management/skills-management.md).

</td></tr><tr><td>

Smart Assessment Engine

</td><td>

Install SAE by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

</td></tr><tr><td>

Software Asset Management

</td><td>

Software Asset Management is available with activation of the Activate all Software Asset Management Professional plugins, including the Software Asset Workspace plugin \(com.sn\_samp\_master\_ws\). Activating this plugin automatically activates the Activate all Software Asset Management Professional plugin \(com.sn\_samp\_master\) and the Software Asset Workspace plugin \(com.sn\_sam\_workspace\). After the new plugin is activated, you can't access the classic user interface. For details about the plugins and how to request them, see [Components installed with Software Asset Management Professional](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/it-asset-management/software-asset-management/sam-installed-components.md).

In the ServiceNow AI Platform® Xanadu release, there's limited support for the Software Asset Management classic user interface. While it remains active in your instance, including when you upgrade to a new ServiceNow AI Platform® release, you can move to the new workspace for an intuitive and personalized experience.

For releases prior to Utah, if you activated the older Software Asset Management Professional plugin \(com.sn\_samp\_master\), the Software Asset Workspace is available with activation of the Software Asset Workspace plugin \(com.sn\_sam\_workspace\). After the Workspace plugin is activated, you can't revert to the classic user interface. For details about the plugins and how to request them, see [Request the Software Asset Management plugins](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/it-asset-management/software-asset-management/t_RequSoftwareAssetMgmt.md).

To activate Next Experience, make sure that the **glide.ui.polaris.experience** system property in your instance is set to true.

Install the following Software Asset Management applications by requesting them from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

-   Software Asset Management - SaaS License Management
-   Data Collection for Oracle Global Licensing and Advisory Services
-   IBM License Compliance for Software Asset Management
-   ITAM Health Check
-   Software Asset Management Guided Experiences

</td></tr><tr><td>

Sourcing and Procurement Operations

</td><td>

Install Sourcing and Procurement Operations by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

</td></tr><tr><td>

Strategic Planning

</td><td>

Install Strategic Planning by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

</td></tr><tr><td>

Stream Connect dashboard

</td><td>

Install the Stream Connect dashboard by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

</td></tr><tr><td>

Subscription Management

</td><td>

Subscription Management is a ServiceNow AI Platform feature that is active by default. Updates for Subscription Management are available through the [https://store.servicenow.com/sn\_appstore\_store.do\#!/store/home](https://store.servicenow.com/sn_appstore_store.do#!/store/home). For cumulative release notes information for applications available on the ServiceNow AI Platform, see [ServiceNow Store release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

</td></tr><tr><td>

Supplier Lifecycle Operations

</td><td>

Install Supplier Lifecycle Operations by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

</td></tr><tr><td>

Task Intelligence for ITSM

</td><td>

Install Task Intelligence for ITSM by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

</td></tr><tr><td>

Telecommunications Network Inventory

</td><td>

The Telecommunications Network Inventory application is a ServiceNow AI Platform feature that is available with activation of the Network Inventory Advanced plugin \(sn\_ni\_adv\). For details, see [Install Telecommunications Network Inventory](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/telecom-network-inventory/telecommunications-network-inventory/installing-telecommunications-network-inventory.md).

</td></tr><tr><td>

Theme Builder

</td><td>

Install Theme Builder by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

**Note:** As of Theme Builder version 4.1, you see when a new Theme Builder update is available from within the Editor page view.

</td></tr><tr><td>

Third-party Risk Management

</td><td>

Install Third-party Risk Management by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

[Quick start tests for TPRM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/governance-risk-compliance/third-party-risk-management/quick-start-tests-grc-vrm.md). After upgrades and deployments of new applications or integrations, run quick start tests to verify that TPRM works as expected. If you customized TPRM, copy the quick start tests and configure them for your customizations.

</td></tr><tr><td>

Threat Intelligence Security Center

</td><td>

Install Threat Intelligence Security Center by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

-   **[Security Operations common functionality](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/security-management/security-operations/sec-ops-common-functionality.md)**

When any of the plugins for the main Security Operations applications \(Security Incident Response, Vulnerability Response, Threat Intelligence, or Configuration Compliance\) are activated, the Security Support Common plugin is activated.


</td></tr><tr><td>

UI Builder

</td><td>

UI Builder is active by default. You can update to the latest version of UI Builder by downloading it from the ServiceNow Store.

</td></tr><tr><td>

UI Component CLI Extension

</td><td>

To install the UI Component CLI extension, install the ServiceNow CLI and add the UI component extension. For details, see [Environment Setup](https://developer.servicenow.com/dev.do#!/reference/next-experience/xanadu/cli/getting-started).

</td></tr><tr><td>

Upgrade Center

</td><td>

Upgrade Center is a ServiceNow AI Platform feature that is active by default.

</td></tr><tr><td>

Vendor Management Workspace

</td><td>

Install Vendor Management Workspace by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html). For more information, see [Activate Vendor Management Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/it-service-management/vendor-management-workspace/activate-vendor-management-configurable-workspace.md).

</td></tr><tr><td>

Verifi Spoke

</td><td>

Install Verifi Spoke by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

</td></tr><tr><td>

Virtual Agent

</td><td>

Virtual Agent is a ServiceNow AI Platform feature that is available with activation of the Glide Virtual Agent plugin \(com.glide.cs.chatbot\), which requires a separate subscription. For details, see [Activate Virtual Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/conversational-interfaces/virtual-agent/activate-virtual-agent.md).

**Note:** The Glide Virtual Agent plugin initially installs the Topic Recommendations and Conversational Analytics apps. Subsequent updates to these apps must be installed from the ServiceNow Store.

ServiceNow® Virtual Agent Lite is a subset of the Virtual Agent platform that is available to ServiceNow® IT Service Management \(ITSM\) customers. It doesn't require activation and works with ITSM Virtual Agent Lite conversations, which are also available to ITSM customers.

</td></tr><tr><td>

Visa Spoke

</td><td>

Install Now Assist for FSO by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

</td></tr><tr><td>

Vulnerability Response Integration with Claroty CTD

</td><td>

Install Vulnerability Response Integration with Claroty CTD by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

</td></tr><tr><td>

Workflow Studio

</td><td>

Install Workflow Studio by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

</td></tr><tr><td>

Workforce Optimization for Customer Service CSM

</td><td>

Install Workforce Optimization for Customer Service by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

</td></tr><tr><td>

Workforce Optimization for ITSM

</td><td>

Activate the Workforce Optimization for ITSM plugin \(sn\_wfo\_cfg\_itsm\) by requesting it from the ServiceNow Store. For details, see [Activate Workforce Optimization for ITSM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/it-service-management/workforce-optimization-for-it-service-management/activate-configurable-workforce-optimization-itsm.md) Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

</td></tr><tr><td>

Workspace

</td><td>

Workspace is a ServiceNow AI Platform feature that is active by default.

</td></tr><tr><td>

Zero Copy Connector for ERP

</td><td>

Install ERP Data Hub by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

</td></tr></tbody>
</table>**Parent Topic:**[Release notes summaries for Xanadu features](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/release-notes/release-notes-summaries.md)


---
title: Deprecation information for all Zurich features and products
description: Cumulative release notes summary on deprecation information for Zurich features and products.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/release-notes/rn-summary-deprecated-info.html
release: zurich
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 7
breadcrumb: [Release notes summaries for Zurich features, Release notes for upgrading from Yokohama, Learn about the Zurich release, Zurich release notes]
---

# Deprecation information for all Zurich features and products

Cumulative release notes summary on deprecation information for Zurich features and products.

For information about deprecated plugins in Zurich, refer to

<table id="rn-summary-accessibility-table" class="custom-rows"><thead><tr><th class="filter">

Application or feature

</th><th>

Details

</th></tr></thead><tbody><tr><td>

AI Control Tower

</td><td>

-   **[Now LLM Service deprecation notice](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/exploring-large-language-models.md)**

Starting with the September 2026 release, Now LLM Service is being prepared for future deprecation. The Now LLM Service is no longer the default model provider for new or inactive AI assets, and it is no longer selected by default in AI Control Tower. A third-party LLM is now selected by default for AI assets, while existing configurations using the Now LLM Service continue unchanged. The Now LLM Service is still available for manual selection. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.


The AI Gateway application is deprecated in the Australia release and is no longer supported.

</td></tr><tr><td>

Advanced AI Search Management Tools

</td><td>

-   **AI Search Profile dashboard**

The **Searchable Documents** and **Documents by Search Source** visualizations have been removed. These visualizations depended on scheduled jobs and legacy dashboard tables which are no longer available.


</td></tr><tr><td>

Advanced Risk

</td><td>

To enhance the Risk Workspace home page load performance and reduce latency, the **Tasks** widget has been removed from the home page.

</td></tr><tr><td>

Agent Client Collector

</td><td>

Agent Client Collector Security Incident Response is no longer supported. For details on replacement options, see the [Deprecation guidance for Agent Client Collector Security Incident Response \[KB2249776\] article](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2249776) in the Now Support Knowledge Base.

</td></tr><tr><td>

Agent experience for CSM

</td><td>

Starting with the Yokohama release, Customer Service CTI Demo Data is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. ServiceNow Voice with Amazon Connect provides the latest experience for this functionality. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184) article in the Now Support Knowledge Base.

</td></tr><tr><td>

App Engine Studio

</td><td>

The ui\_builder\_admin role was removed from the AES Portal UI Template plugin in the Zurich release. Admin and delegated developer roles can still access the AES Portal UI Template plugin \(sn\_portal\_starte\_0\).

</td></tr><tr><td>

Automation Discovery

</td><td>

Starting with the Zurich release, Automation Discovery has been deprecated. It will be hidden and no longer installed on new instances but will continue to be supported in this release. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base. For more information about this application see [Automation Discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/now-intelligence/automation-discovery.md).

</td></tr><tr><td>

Cloud Cost Management

</td><td>

The current mechanism for the Azure billing download is planned for deprecation. With this deprecation, the Export option remains the default method for the Azure billing download.

</td></tr><tr><td>

Data Management

</td><td>

The Data Usage Visualization Console dashboard has been deprecated in the Zurich release. Instead, you can monitor the growth of data on your instance using the Data Management Console.

</td></tr><tr><td>

Dispute Rules Content Pack for Mastercard

</td><td>

For July store release, the sub-category RC 4834 — Late Presentment has been removed.

</td></tr><tr><td>

Document Intelligence

</td><td>

The Document Intelligence application has been removed from the application navigator.

</td></tr><tr><td>

Encryption

</td><td>

-   **[Prepare your instance for GlideEncrypter deprecation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-security/check-3des.md)**

Encrypted string keys 3DES format is no longer supported. Key Management Framework \(KMF\) is the supported format.


</td></tr><tr><td>

Enterprise Asset Management

</td><td>

The Classification \(classification\) column in the Enterprise good model \[sn\_ent\_model\] table has been deprecated and renamed as Classification \(Deprecated\). The data from this column is available in the new Classification \(classification\_code\) column in the Product model \[cmdb\_model\] table.

</td></tr><tr><td>

HR Service Delivery integration with Accurate Background service

</td><td>

Starting with Zurich release, HR Service Delivery integration with Accurate Background service is being prepared for future deprecation. It will be hidden and no longer available for activation but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support knowledge base.

</td></tr><tr><td>

HR Service Delivery integration with First Advantage service

</td><td>

Starting with Zurich release, HR Service Delivery integration with First Advantage service is being prepared for future deprecation. It will be hidden and no longer available for activation but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support knowledge base.

</td></tr><tr><td>

HR Service Delivery integration with Sterling Talent Solutions service

</td><td>

Starting with Zurich release, HR Service Delivery integration with Sterling Talent Solutions service is being prepared for future deprecation. It will be hidden and no longer available for activation but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support knowledge base.

</td></tr><tr><td>

ITOM Visibility

</td><td>

Starting with the Zurich release, Cloud Discovery Workspace is being prepared for future deprecation. It’s hidden and no longer activated on new instances but continues to be supported. Discovery Admin Workspace provides the latest experience for this functionality. For details, see the [Application/Plugin Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184) article in the Now Support knowledge base.

</td></tr><tr><td>

Impact

</td><td>

Starting with Impact Zurich version 6.0.8 ServiceNow Store release, Proactive Code Check is being prepared for future deprecation. It will be hidden and no longer installed on new instances but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

The Jumpstart Your Document Intelligence Accelerator has been removed.

</td></tr><tr><td>

Instance Data Replication

</td><td>

Legacy replication sets have been deprecated in the Zurich release and are no longer supported.

</td></tr><tr><td>

Learning Posts

</td><td>

Starting with the zurich release, Learning Posts is being deprecated. It will be hidden and no longer available for activation. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184) article in the Now Support Knowledge Base.

</td></tr><tr><td>

Legacy Application Manager

</td><td>

Legacy Application Manager is being deprecated as of Zurich patch 8. Bookmarks to Legacy Application Manager redirect to the new Application Manager experience.

</td></tr><tr><td>

Legacy Studio

</td><td>

Starting with the Zurich release, Legacy Studio is being prepared for future deprecation. It will be hidden and no longer installed on new instances but will continue to be supported. For details on this process, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base. For more information about app development on the ServiceNow AI Platform®, see .

</td></tr><tr><td>

Listening Posts

</td><td>

Starting with the zurich release, Listening Posts is being deprecated. It will be hidden and no longer available for activation. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184) article in the Now Support Knowledge Base.

</td></tr><tr><td>

Operational Resilience

</td><td>

The Operational Resilience application previously stored the entire dependency chain in the \[sn\_oper\_res\_profile\] table, which resulted in redundant data and potential performance issues. The **Update CSDM and other dependencies** scheduled job script has been optimized to address this issue. Any node can now be at the top level. Data retrieval is more efficient because you can store the impacted objects in a single table.

</td></tr><tr><td>

Project Portfolio Management

</td><td>

-   **[Resource Management reports](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-business-management/c_UsingResourceManagementReports.md)**

Starting with the Zurich release, Resource Management reports are deprecated. You can start using the interactive Overview dashboard in Resource Management Workspace to work on reporting.

For more information on the Overview dashboard, see [Using Resource Management Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-business-management/using-rmw.md#section_v4k_rtg_1fc).

-   **[Resource Management classic](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-business-management/c_ResourceManagement.md)**

Starting with the Zurich release, the Resource Allocation workbench and Capacity planning overview are removed from the product navigation of Resource Management for new customers.


</td></tr><tr><td>

Self-service and omnichannel engagement for CSM

</td><td>

Starting with the Zurich release, Customer Service CTI Demo Data Plugin and CTI Softphone Plugin are no longer deployed, enhanced, or supported. For details, see the [Deprecation Process \[KB0867184\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base, [Components installed with Customer Service CTI Demo Data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/r_InstalledWithCustServCTIDemoData.md), and [Components installed with CTI Softphone](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/r_InstalledWithCCTISoftphone.md).

</td></tr><tr><td>

Service Creator

</td><td>

Starting with Zurich release, Service Creator is being prepared for future deprecation. It will be hidden and no longer available for activation but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184) article in the Now Support Knowledge Base.

</td></tr><tr><td>

ServiceNow AI Platform core feature

</td><td>

Starting with the Zurich release, Application Insights is no longer deployed, enhanced, or supported. Instead, [Overview of Instance Observer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/impact/io-overview.md) offers a powerful solution for enhancing system performance. Contact your account manager to discover more. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

</td></tr><tr><td>

ServiceNow Otto for IT Operations Management \(ITOM\)

</td><td>

In [Zurich Patch 12](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-12.md), the Google Gemini Cloud Assist agent is being prepared for future deprecation. To continue receiving Google Cloud insights, use the analyze alert impact agentic workflow which includes the Gemini Cloud Assist A2A Investigation Agent. For configuration instructions, see .

In [Zurich Patch 7](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-7.md), the Dynatrace analysis AI agent is being prepared for future deprecation. To continue getting Dynatrace insights in agentic workflows, deactivate the Dynatrace analysis AI agent and set up the Dynatrace MCP server agent. For configuration details, see .

</td></tr><tr><td>

Strategic Planning

</td><td>

The **Investment class** and **Investment type** fields have been deprecated from the Project \[sn\_align\_core\_project\] and Demand \[sn\_align\_core\_demand\] tables.

</td></tr><tr><td>

Usage Insights

</td><td>

-   **[Usage Insights in Xanadu](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/now-intelligence/user-exp-analytics-landing.md)**

Usage Insights is no longer supported in the Xanadu release. Upgrade to Yokohama, Zurich, or Australia to continue using Usage Insights.


</td></tr></tbody>
</table>**Parent Topic:**[Release notes summaries for Zurich features](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/release-notes-summaries.md)


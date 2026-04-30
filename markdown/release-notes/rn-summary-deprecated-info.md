---
title: Deprecation information for all Zurich features and products
description: Cumulative release notes summary on deprecation information for Zurich features and products.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2026-04-08"
reading_time_minutes: 13
breadcrumb: [Release notes summaries for Zurich features, Release notes for upgrading from Yokohama, Learn about the Zurich release, Zurich release notes]
---

# Deprecation information for all Zurich features and products

Cumulative release notes summary on deprecation information for Zurich features and products.

For information about deprecated plugins in Zurich, refer to Plugin information[Plugin information for all features and productsPlugin information](https://www.servicenow.com/docs/r/release-notes/rn-summary-plugin-info.html)

<table id="rn-summary-accessibility-table" class="custom-rows"><thead><tr><th class="filter">

Application or feature

</th><th>

Details

</th></tr></thead><tbody><tr><td>

API

</td><td>

-   The GlideEncrypter API no longer supports Triple Data Encryption Standard \(3DES\) due to updated [NIST 800-131A Rev 2](https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-131Ar2.pdf) guidelines.
    -   For existing instances that upgrade to the Zurich release, the GlideEncrypter API is available for use but has been updated to automatically use the Key Management Framework algorithm. See [GlideEncrypter - Global \(deprecated\)](https://www.servicenow.com/docs/access?context=GlideEncrypterAPI&version=zurich&pubname=zurich-api-reference&ft:locale=en-US) for more information on how to continue calling this API.
    -   For all new instances created starting with the Zurich release, the GlideEncrypter API is no longer supported. Directly use the [Key Management Framework](https://www.servicenow.com/docs/access?context=encryption&version=zurich&pubname=zurich-platform-security&ft:locale=en-US) instead for all cryptography operations.
-   Dynamic groups have been removed from dynamic schema in Core Platform. For dynamic attributes defined with an associated dynamic attribute group before the Zurich release, the [GlideDynamicAttribute](https://www.servicenow.com/docs/access?context=GlideDynamicAttributeAPI&version=zurich&pubname=zurich-api-reference&ft:locale=en-US) getGroupName\(\) method originally designed for dynamic attribute groups continues to work for backwards compatibility.

The getGroupName\(\) method returns null for migrated attributes and newly created attributes.

Customers are urged to migrate to the current [Dynamic Attribute](https://www.servicenow.com/docs/access?context=working-with-dynamic-schema&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US) definitions to take advantage of future improvements in features and functionality. For migration details, see the [Dynamic Schema Zurich Migration Guide \[KB2146133\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2146133) article in the Now Support Knowledge Base.


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

Authentication

</td><td>

Due to the launch of new simplified inbound integration configuration in Machine Identity Console, the following inbound integrations configurations in the Application registry page are deprecated:

-   OAuth API endpoint for external clients
-   OAuth JWT API endpoint for external clients
-   OIDC provider to verify ID tokens

</td></tr><tr><td>

Automation Discovery

</td><td>

Starting with the Zurich release, Automation Discovery has been deprecated. It will be hidden and no longer installed on new instances but will continue to be supported in this release. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base. For more information about this application see [Automation Discovery](https://www.servicenow.com/docs/access?context=automation-discovery&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US).

</td></tr><tr><td>

Case management for CSM

</td><td>

-   Starting with the Yokohama release, Customer Service CTI Demo Data is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. ServiceNow Voice with Amazon Connect provides the latest experience for this functionality. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184) article in the Now Support Knowledge Base.
-   Starting with the Zurich release, the Customer Service Case Types plugin is available as a store plugin and, as such, the family version of the plugin is being prepared for future deprecation. Upon upgrading, customers will automatically move to the store version of the plugin. It will be hidden from the family plugins and no longer installed on new instances but will continue to be supported as a store plugin. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

</td></tr><tr><td>

Classic Workflow

</td><td>

 

</td></tr><tr><td>

Clone Admin Console

</td><td>

-   The legacy clone request page clone\_instance.DO is going to be retired in the A release.
-   Update to the latest version for the best experience and performance improvements. To update Clone Admin Console, see [Clone Admin Console](https://www.servicenow.com/docs/access?context=Clone-UI&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

</td></tr><tr><td>

Cloud Cost Management 9.0

</td><td>

The current mechanism for the Azure billing download is planned for deprecation. With this deprecation, the Export option remains the default method for the Azure billing download.

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

-   The Data Certification plugin \(com.snc.certification\_v2\) is now deprecated and no longer supported or available for new activation. The latest experience for this functionality is included with CMDB Workspace.


</td></tr><tr><td>

Data Management

</td><td>

The Data Usage Visualization Console dashboard has been deprecated in the Zurich release. Instead, you can monitor the growth of data on your instance using the Data Management Console.

</td></tr><tr><td>

Data Management for CSM

</td><td>

The following legacy base system workflows have been deprecated:

-   Escalation Master-Approval
-   Escalation-Approval

Custom workflows remain supported, and you can continue to create them as needed. However, any new business requirements must be implemented using the new or updated flow-based framework rather than with the legacy workflows.

</td></tr><tr><td>

Document Intelligence

</td><td>

-   Starting with Zurich release, the document extraction feature in Document Intelligence is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184) article in the Now Support Knowledge Base. Instead, you can extract information from documents using the Now Assist in Document Intelligence application. For more information, see .
-   The Document Intelligence Admin \(sn\_docintel\_admin\) plugin is planned for deprecation in the B release.

</td></tr><tr><td>

Encryption

</td><td>

-   **[Prepare your instance for GlideEncrypter deprecation](https://www.servicenow.com/docs/access?context=check-3des&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)**

Encrypted string keys 3DES format is no longer supported. Key Management Framework \(KMF\) is the supported format.


</td></tr><tr><td>

Enterprise Asset Management

</td><td>

The Classification \(classification\) column in the Enterprise good model \[sn\_ent\_model\] table has been deprecated and renamed as Classification \(Deprecated\). The data from this column is available in the new Classification \(classification\_code\) column in the Product model \[cmdb\_model\] table.

</td></tr><tr><td>

Event Management

</td><td>

-   Event Management connector: Deprecate unused V1 connector definitions during Event Management connector upgrades.
-   vRealize connector: Enhance the vRealize event connector by replacing the deprecated XML API with a JSON-based API, ensuring compatibility with future versions.
-   The "em\_alert\_lists\_auto\_refresh" table no longer controls live alert list updates in the Service Operation Workspace Lists. Use the new property, table sys\_ux\_list, to turn on and off live incoming alert updates.

</td></tr><tr><td>

Field Service Management

</td><td>

-   Non-collapsed mode is being deprecated and removed from Dispatcher Workspace. Dispatchers must use collapsed mode to see available resources in Dispatcher Workspace.
-   Starting with the Zurich release, the **Enable capacity** constraint for Schedule Optimization is being deprecated. It will no longer be applied for Schedule Optimization. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

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

Hardware Asset Management

</td><td>

Starting from the Zurich release, the following workflows are being prepared for future deprecation:

-   Procurement Process Flow – Hardware
-   Procurement Process Flow – Mobile
-   Procurement Process Flow - Default
-   Transfer Order
-   Transfer Order Line
-   Source Request
-   Contract Approval

**Note:** Procurement Process Flow-Default and Procurement Process Flow – Mobile are demo data workflows displayed in the workflow studio when the Workflow Authoring Tools \(com.glideapp.workflow.authoring\) plugin is installed.

These impacted workflows are migrated to Workflow Studio flows. After upgrading to the Zurich release, you must transition to the new Workflow Studio flows. For more information about the deprecation process and its impact, see the [Application/Plugin Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184) article in the Now Support Knowledge Base.

</td></tr><tr><td>

ITOM AIOps

</td><td>

-   The "em\_alert\_lists\_auto\_refresh" table no longer controls live alert list updates in the Service Operation Workspace Lists. Use the new property, table sys\_ux\_list, to turn on and off live incoming alert updates.

</td></tr><tr><td>

ITOM Visibility

</td><td>

Starting with the Zurich release, Cloud Discovery Workspace is being prepared for future deprecation. It’s hidden and no longer activated on new instances but continues to be supported. Discovery Admin Workspace provides the latest experience for this functionality. For details, see the [Application/Plugin Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184) article in the Now Support knowledge base.

</td></tr><tr><td>

Impact

</td><td>

Starting with Impact Zurich version 6.0.8 ServiceNow Store release, Proactive Code Check is being prepared for future deprecation. It will be hidden and no longer installed on new instances but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

</td></tr><tr><td>

Instance Data Replication

</td><td>

Legacy replication sets have been deprecated in the Zurich release and are no longer supported.

</td></tr><tr><td>

Journey designer

</td><td>

-   Learning Posts. All Learning Posts capabilities are now integrated within Journey designer. For more information, see [Learning Posts release notes](../hr-service-delivery/learning-posts-rn.md).
-   Listening Posts. For more information, see [Listening Posts release notes](../hr-service-delivery/listening-posts-rn.md).

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

Starting with the Zurich release, Legacy Studio is being prepared for future deprecation. It will be hidden and no longer installed on new instances but will continue to be supported. For details on this process, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base. For more information about app development on the ServiceNow AI Platform®, see [ServiceNow Studio](https://www.servicenow.com/docs/access?context=servicenow-studio-landing&version=zurich&pubname=zurich-application-development&ft:locale=en-US).

</td></tr><tr><td>

Listening Posts

</td><td>

Starting with the zurich release, Listening Posts is being deprecated. It will be hidden and no longer available for activation. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184) article in the Now Support Knowledge Base.

</td></tr><tr><td>

Now Assist

</td><td>

-   In Patch 5, the **Select Use Case** drop-down menu was removed from the Agentic AI - ITSM tab.

</td></tr><tr><td>

Now Assist AI agents

</td><td>

-   The support for manually integrating external agents has been deprecated from [Zurich Patch 8](../quality/zurich-patch-8.md) release.

</td></tr><tr><td>

Now Assist for IT Operations Management \(ITOM\)

</td><td>

In [Zurich Patch 7](../quality/zurich-patch-7.md), the Dynatrace analysis AI agent is being prepared for future deprecation. To continue getting Dynatrace insights in agentic workflows, deactivate the Dynatrace analysis AI agent and set up the Dynatrace MCP server agent. For configuration details, see [Configure the Dynatrace MCP server agent](https://www.servicenow.com/docs/access?context=now-assist-itom-config-dynatrace-mcp&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US).

</td></tr><tr><td>

Now Assist for IT Service Management \(ITSM\)

</td><td>

The Escalate IT Ticket core ITSM Virtual Agent topic is being deprecated in this release. The topic is renamed to **\(Deprecated\) Escalate IT Ticket**. This capability will be available in the Platform Request Status AI agent in a future release.

</td></tr><tr><td>

Now Assist in Virtual Agent

</td><td>

-   In Patch 4, **sn\_aia.use\_agents\_in\_planner** system property has been removed. The system property was used for configuring AI agent discovery behavior.
-   In Patch 4, Now Assist skills page in the assistant admin guided setup has been removed due to the skills being turned on by default.
-   In Patch 1, Bing support for the searching and scraping search result type is no longer supported when adding a web search tool in Now Assist Skill Kit.

</td></tr><tr><td>

Operational Resilience

</td><td>

The Operational Resilience application previously stored the entire dependency chain in the \[sn\_oper\_res\_profile\] table, which resulted in redundant data and potential performance issues. The **Update CSDM and other dependencies** scheduled job script has been optimized to address this issue. Any node can now be at the top level. Data retrieval is more efficient because you can store the impacted objects in a single table.

</td></tr><tr><td>

Operational Technology Manager

</td><td>

For the Service Graph Connector for Microsoft Excel, the following items were deprecated on the ServiceNow AI Platform:

-   The SG OT Excel Staging Task table
-   The Staging task reference on the SG OT Excel Staging table

</td></tr><tr><td>

Playbooks in Workflow Studio

</td><td>

-   now.assist.creator role

</td></tr><tr><td>

Project Portfolio Management

</td><td>

-   **[Resource Management reports](https://www.servicenow.com/docs/access?context=c_UsingResourceManagementReports&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)**

Starting with the Zurich release, Resource Management reports are deprecated. You can start using the interactive Overview dashboard in Resource Management Workspace to work on reporting.

For more information on the Overview dashboard, see [Using Resource Management Workspace](https://www.servicenow.com/docs/access?context=using-rmw&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US#section_v4k_rtg_1fc).

-   **[Resource Management classic](https://www.servicenow.com/docs/access?context=c_ResourceManagement&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)**

Starting with the Zurich release, the Resource Allocation workbench and Capacity planning overview are removed from the product navigation of Resource Management for new customers.


</td></tr><tr><td>

Self-service and omnichannel engagement for CSM

</td><td>

Starting with the Zurich release, Customer Service CTI Demo Data Plugin and CTI Softphone Plugin are no longer deployed, enhanced, or supported. For details, see the [Deprecation Process \[KB0867184\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base, [Components installed with Customer Service CTI Demo Data](https://www.servicenow.com/docs/access?context=r_InstalledWithCustServCTIDemoData&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US), and [Components installed with CTI Softphone](https://www.servicenow.com/docs/access?context=r_InstalledWithCCTISoftphone&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US).

</td></tr><tr><td>

Service Creator

</td><td>

Starting with Zurich release, Service Creator is being prepared for future deprecation. It will be hidden and no longer available for activation but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184) article in the Now Support Knowledge Base.

</td></tr><tr><td>

ServiceNow AI Platform core feature

</td><td>

Starting with the Zurich release, Application Insights is no longer deployed, enhanced, or supported. Instead, [Overview of Instance Observer](https://www.servicenow.com/docs/access?context=io-overview&version=zurich&pubname=zurich-impact&ft:locale=en-US) offers a powerful solution for enhancing system performance. Contact your account manager to discover more. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

</td></tr><tr><td>

ServiceNow SDK

</td><td>

-   The $id property is deprecated in the List API and Role API.
-   Property names that use snake case are deprecated in all ServiceNow Fluent APIs. Use the equivalent property name in camel case instead.

</td></tr><tr><td>

Software Asset Management

</td><td>

Starting from the Zurich release, the following workflows are being prepared for future deprecation:

-   Reclamation workflow
-   Procurement Process Flow - Auto allocation enabled

</td></tr><tr><td>

Strategic Planning

</td><td>

The **Investment class** and **Investment type** fields have been deprecated from the Project \[sn\_align\_core\_project\] and Demand \[sn\_align\_core\_demand\] tables.

</td></tr><tr><td>

Telecommunications Service Operations Management \(TSOM\)

</td><td>

-   The two previous Extract, Transform, Load \(ETLs\) for Optical Line Terminal \(OLT\) and Optical Network Unit \(ONU\) have been merged into a unified ETL that supports both physical and logical data and have been deprecated and phased out.
-   The previous Service Operation CMDB Compliance Audit has been deprecated and replaced by the Telecom Discrepancy Audit.

</td></tr><tr><td>

Virtual Agent

</td><td>

-   Starting with the Zurich release, [Sensitive Data Handler](https://www.servicenow.com/docs/access?context=ac-sensitive-data-overview&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US) and the [Sensitive Data Masking capability](https://www.servicenow.com/docs/access?context=va-sensitive-data-masking&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US) are being prepared for future deprecation. They will be hidden and no longer available for installation but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support knowledge base.

Install the Data Privacy application as a replacement. For more information, see [Data Privacy](https://www.servicenow.com/docs/access?context=data-privacy-landing&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

-   Starting with the Zurich release, Microsoft LUIS is no longer deployed, enhanced, or supported. For details, see the [Deprecation Process \[KB0867184\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support knowledge base.


</td></tr></tbody>
</table>**Parent Topic:**[Release notes summaries for Zurich features](../release-notes-summaries.md)


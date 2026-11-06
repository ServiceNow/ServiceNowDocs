---
title: Plugins or applications installed with ITOM Visibility
description: Plugins and applications are installed with ITOM Visibility, and application dependencies are installed when you update.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-operations-management/itom-visibility/plugin-app-itom-visibility.html
release: australia
product: ITOM Visibility
classification: itom-visibility
topic_type: reference
last_updated: "2026-10-07"
reading_time_minutes: 7
breadcrumb: [ITOM Visibility reference, ITOM Visibility, IT Operations Management]
---

# Plugins or applications installed with ITOM Visibility

Plugins and applications are installed with ITOM Visibility, and application dependencies are installed when you update.

## Discovery

|Plugin or application name|Description|
|--------------------------|-----------|
|Cloud Provisioning and Governance Core \(com.snc.cloud.core\)|Contains resource blocks and cloud Application Programming Interface \(cloud API\) mappings related to Cloud API-based discovery and events processed by either response mapping or calling patterns.|
|Service Watch Suite commons \(com.snc.service-watch.commons\)|Contains common UI components for Discovery and Service Mapping.|
|Discovery - IP Based \(com.snc.discovery.ip\_based\)|Contains shared components of horizontal discovery used by Discovery and Service Mapping.|
|ITOM Smart Content \(com.snc.itom.smart.content\)|Delivers curated discovery and classification content that improves application and service identification and helps maintain accurate configuration data.|
|ITOM Discovery Framework Core \(com.snc.discovery.framework.core\)|Provides the core functionality for the Discovery Framework.|
|ITOM Discovery Admin Workspace \(com.snc.itom.daw\)|Enables the Discovery Admin Workspace experience for managing and monitoring Discovery operations.|

## Discovery Admin Workspace

|Plugin or application name|Description|
|--------------------------|-----------|
|ITOMDiscovery Admin Workspace \(com.snc.itom.daw\)|Enables the Discovery Admin Workspace experience for managing and monitoring Discovery operations.|
|Service Operations WorkspaceService Reliability Management \(SRM\) Common \(sn\_sow\_srm\_common\)|Delivers common configurations for Service Reliability Management, which are stored globally, such as access control changes. This configuration is installed only as a result of enabling the Service Reliability Management application.|
|CMDB Workspace \(sn\_cmdb\_ws\)|Provides a centralized experience for managing CMDB data health, governance, and insights. Use it to assess CMDB quality, investigate data issues, and gain visibility into configuration data so you can maintain a trusted CMDB.|
|Discovery and Service Mapping Patterns \(sn\_itom\_pattern\)|Provides the latest versions of the Discovery and Service Mapping Patterns released on the ServiceNow Store. ServiceNow releases new patterns on the ServiceNow® Store on a monthly basis, enabling your organization to discover the latest industry-standard devices and applications.|
|ITOM Configuration Console \(sn\_itom\_admin\)|Delivers structured onboarding journeys for both Event Management and Discovery, with step-by-step workflows covering monitoring tool integration, alert response configuration, CI classification, and diagnostics validation.|
|ITOM Guided Setup - New \(sn\_sow\_guide\_setup\)|Provides a structured onboarding experience to help users quickly implement and realize value from ITOM.|
|CMDB CI Class Models \(sn\_cmdb\_ci\_class\)|Adds class models that extend the CMDB class hierarchy, including class descriptions, identification rules, identifier entries, and dependent relationships if applicable. Applications such as Discovery and Service Mapping can use these class extensions to populate configuration items \(CIs\) and discover various technologies and software.|

## Service Mapping

|Plugin or application name|Description|
|--------------------------|-----------|
|Service Mapping – Map \(com.itom-map-app\)|A dependent internal plugin necessary to support the core components of the Service Mapping, Event Management, and Service Operations Workspace ITOM applications.|
|Discovery \(com.snc.discovery\)|Finds applications and devices on your network, and then updates the CMDB with the information it finds.|
|Event Management and Service Mapping Core \(com.snc.service-watch\)|Comprises the common components of Event Management and Service Mapping.|
|Cloud Provisioning and Governance Core \(com.snc.cloud.core\)|Contains resource blocks and cloud Application Programming Interface \(cloud API\) mappings related to Cloud API-based discovery and events processed by either response mapping or calling patterns.|
|Pattern Designer \(NG version\) \(com.snc.ng.pattern.designer\)|The next generation \(NG\) version of the Pattern Designer that enables you to create, edit, and debug patterns used by horizontal and top-down discovery.|
|Service Mapping Plus \(sn\_sm\_scoped\_app\)|Offers extended features for Service Mapping, and if related ServiceNow® Store applications and plugins aren't already installed, it installs them.|

## Tag Governance

|Plugin or application name|Description|
|--------------------------|-----------|
|Cloud Access Interface \(sn\_cai\)|Provides easy access to the cloud through scripting. You can use this ServiceNow Store application to perform actions on virtual machines provisioned on Amazon Web Services \(AWS\) and Microsoft Azure.|
|Certification Core \(com.snc.certification\_core\)|Contains core certification structures such as filters and templates, and provides compliance functionality.|
|ITOM Visibility License \(com.snc.itom.vis.license\)|Enables the activation of any ServiceNow Store application that requires ITOM Visibility licensing.|
|ITOM/OT SU Licensing \(sn\_itom\_licensing\)|Calculates and displays how many subscriptions for ITOM applications your organization purchases and consumes.|
|Discovery \(com.snc.discovery\)|Finds applications and devices on your network, and then updates the CMDB with the information it finds.|
|Flow Designer Action Step - Script on MID \(com.glide.hub.action\_step.script\_mid\)|Provides an action step to execute custom JavaScript within a reusable action on a MID Server.|

## Cloud Discovery Workspace

**Important:** Cloud Discovery Workspace is now deprecated and no longer supported or available for new activation. [Discovery Admin Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/discovery/discovery-admin-workspace.md) provides the latest experience for this functionality. For details, see the [Application/Plugin Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184) article in the Now Support knowledge base.

|Plugin or application name|Description|
|--------------------------|-----------|
|Discovery and Service Mapping Patterns \(sn\_itom\_pattern\)|Provides the latest versions of the Discovery and Service Mapping Patterns released on the ServiceNow Store. ServiceNow releases new patterns on the ServiceNow® Store on a monthly basis, enabling your organization to discover the latest industry-standard devices and applications.|
|Cloud Provisioning and Governance Core \(com.snc.cloud.core\)|Contains resource blocks and cloud Application Programming Interface \(cloud API\) mappings related to Cloud API-based discovery and events processed by either response mapping or calling patterns.|
|Performance Analytics Content Pack for Cloud Resources \(sn\_disco\_cd\)|Displays the aggregated view of all your Cloud Resources. It also provides analytics tables and views that associate tags with resources, enabling you to build your own custom dashboards and reports.|
|Pattern Designer \(NG version\) \(com.snc.ng.pattern.designer\)|The next generation \(NG\) version of the Pattern Designer that enables you to create, edit, and debug patterns used by horizontal and top-down discovery.|

## Agent Client Collector for Visibility Content

|Plugin or application name|Description|
|--------------------------|-----------|
|Agent Client Collector for Visibility Content Content \(sn\_acc\_vis\_content\)|Provides agent-based infrastructure discovery and collects Software Asset Management \(SAM\) metrics to support Discovery and Digital End-User Experience \(DEX\) applications.|
|Discovery \(com.snc.discovery\)|Finds applications and devices on your network, and then updates the CMDB with the information it finds.|
|Agent Client Collector Framework \(sn\_agent\)|Manages Agent Client Collector on the ServiceNow instance and the MID Server.|
|CMDB CI Class Models \(sn\_cmdb\_ci\_class\)|Adds class models that extend the CMDB class hierarchy, including class descriptions, identification rules, identifier entries, and dependent relationships if applicable. Applications such as Discovery and Service Mapping can use these class extensions to populate configuration items \(CIs\) and discover various technologies and software.|

## Agent Client Collector for Visibility Content Content

|Plugin or application name|Description|
|--------------------------|-----------|
|Expanded Model and Asset Classes \(sn\_ent\)|Provides new, expanded model classes, asset classes, and model categories that come with the base system, defined by ServiceNow. Install the Asset Management \(com.snc.asset\_management\) plugin as a prerequisite for using this application.|
|Discovery – IP Based \(com.snc.discovery.ip\_based\)|Contains shared components of horizontal discovery used by Discovery and Service Mapping.|
|Agent Client Collector Framework \(sn\_agent\)|Manages Agent Client Collector on the ServiceNow instance and the MID Server.|
|CMDB CI Class Models \(sn\_cmdb\_ci\_class\)|Adds class models that extend the CMDB class hierarchy, including class descriptions, identification rules, identifier entries, and dependent relationships if applicable. Applications such as Discovery and Service Mapping can use these class extensions to populate configuration items \(CIs\) and discover various technologies and software.|

**Parent Topic:**[ITOM Visibility reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/itom-visibility/visibility-reference.md)

**Related topics**  


[Plugins or applications installed with ITOM Cloud Accelerate](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/itom-cloud-accelerate/plugin-app-cloud-accelerate.md)

[Plugins or applications installed with ITOM AIOps](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/plugin-app-itom-health.md)

[Plugins activated with ITOM Optimization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/plugin-itom-optimization.md)

[Applications installed with ServiceNow Otto for ITOM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/app-now-assist-itom.md)


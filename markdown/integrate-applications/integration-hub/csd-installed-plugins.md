---
title: Plugins installed
description: These plugins are installed with the Client Software Distribution plugin, if they are not already active.
locale: en-US
release: yokohama
product: Integration Hub
classification: integration-hub
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Components installed with client software distribution, Client Software Distribution using Integration Hub, Integration Hub available solutions, Building integrations in Integration Hub, Integration Hub, Data and Automation]
---

# Plugins installed

These plugins are installed with the Client Software Distribution plugin, if they are not already active.

For instructions on requesting activation of Client Software Distribution \(CSD\) see [Request client software distribution](../tasks/request-csd-ihub.md).

|Plugin|Description|
|------|-----------|
|Orchestration - System Center Configuration Manager \(com.snc.orchestration.sccm\_mgnt\)|Installs the custom SCCM Orchestration activities that do work on the SCCM target host.|
|Orchestration - Asset Lease Management \(com.snc.orchestration.asset\_lease\_management\)|Installs the [lease functionality](../tasks/csd-license.md#) for software distributed through the Service Catalog. This includes starting, stopping, and extending leases.|
|Service Catalog Scoped API \(com.glideapp.servicecatalog.scoped.api\)|Installs the API to support application creation in the Service Catalog.|
|Software Asset Management Core \(com.snc.sam.core\)|Provides the base tables for software asset management. Includes software installations, usages, suite calculations, and discovery models.|
|||
|ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)|Enables execution of IntegrationHub actions and flows.|
|Flow Designer support for the Service Catalog \(com.glideapp.servicecatalog.flow\_designer\)|Provides support for Workflow Studio in Service Catalog.|
|Microsoft SCCM Spoke for IntegrationHub \(com.sn.sccm.spoke\)|Provides actions in Workflow Studio that a Process Analyst can use to automate the management of user collections, device collections, and application deployments.|
|Software Asset Management Spoke \(com.sn\_sam\_spoke\)|Provides actions in Workflow Studio for Software Asset Management activities.|
|Responsive Dashboards \(com.glideapp.dashboard\)|Creates, modifies, and shares dashboards using responsive and dynamic widget layouts.|
|Outbound Tracking \(com.glide.outbound\_tracking\)|Tracks outbound requests.|

**Parent Topic:**[Components installed with client software distribution](comp-installed-csd-ihub.md)

